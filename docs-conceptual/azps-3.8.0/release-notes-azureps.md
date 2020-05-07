---
title: Viktig information om Azure PowerShell
description: Lär dig mer om alla de senaste uppdateringarna för Azure PowerShell-modulerna.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.openlocfilehash: a9c5394a5fac8a8a3de96925b3563776783ea9fe
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/05/2020
ms.locfileid: "82080206"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="43970-103">Viktig information om Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="43970-103">Azure PowerShell release notes</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="43970-104">3.8.0 – April 2020</span><span class="sxs-lookup"><span data-stu-id="43970-104">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="43970-105">Höjdpunkter sedan den senaste uppdateringen</span><span class="sxs-lookup"><span data-stu-id="43970-105">Highlights since the last release</span></span>
* <span data-ttu-id="43970-106">PowerShell-versioner som Az.Storage stöder: Windows PowerShell 5.1, PowerShell Core 6.2.4+ och PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="43970-106">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="43970-107">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="43970-107">Az.Accounts</span></span>
* <span data-ttu-id="43970-108">Uppdaterade URL:en för Azure PowerShell-enkäten i ”Resolve-AzError” [#11507]</span><span class="sxs-lookup"><span data-stu-id="43970-108">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="43970-109">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="43970-109">Az.ApiManagement</span></span>
* <span data-ttu-id="43970-110">Lade till meddelande om icke-bakåtkompatibel ändring vid ändring i utdata för Azure File-cmdletar i en framtida version</span><span class="sxs-lookup"><span data-stu-id="43970-110">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="43970-111">"Set-AzApiManagementGroup" Uppdaterad dokumentation för att ange GroupId-parametern</span><span class="sxs-lookup"><span data-stu-id="43970-111">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="43970-112">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="43970-112">Az.Cdn</span></span>
* <span data-ttu-id="43970-113">Fast ChinaCDN-relaterad prissättning för SKU-visning</span><span class="sxs-lookup"><span data-stu-id="43970-113">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="43970-114">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="43970-114">Az.CognitiveServices</span></span>
* <span data-ttu-id="43970-115">Identitet som stöds, kryptering, UserOwnedStorage</span><span class="sxs-lookup"><span data-stu-id="43970-115">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="43970-116">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="43970-116">Az.Compute</span></span>
* <span data-ttu-id="43970-117">Cmdleten ”Set-AzVmssOrchestrationServiceState” har lagts till.</span><span class="sxs-lookup"><span data-stu-id="43970-117">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="43970-118">”Get-AzVmss” med -InstanceView visar OrchestrationService-tillstånd.</span><span class="sxs-lookup"><span data-stu-id="43970-118">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="43970-119">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="43970-119">Az.IotHub</span></span>
* <span data-ttu-id="43970-120">Hantera den dubbla konfigurationen för IoT-enheter, nya cmdletar är:</span><span class="sxs-lookup"><span data-stu-id="43970-120">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="43970-121">'Get-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="43970-121">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="43970-122">'Update-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="43970-122">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="43970-123">En cmdlet har lagts till för att anropa direkt metod på en enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="43970-123">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="43970-124">Hantera dubbel konfiguration för IoT-enhetsmodul, nya cmdletar är:</span><span class="sxs-lookup"><span data-stu-id="43970-124">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="43970-125">'Get-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="43970-125">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="43970-126">'Update-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="43970-126">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="43970-127">Hantera IoT-automatisk konfiguration av enhetshantering i stor skala.</span><span class="sxs-lookup"><span data-stu-id="43970-127">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="43970-128">Nya cmdlet:ar är:</span><span class="sxs-lookup"><span data-stu-id="43970-128">New cmdlets are:</span></span>
    - <span data-ttu-id="43970-129">'Add-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="43970-129">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="43970-130">'Get-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="43970-130">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="43970-131">'Remove-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="43970-131">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="43970-132">'Set-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="43970-132">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="43970-133">En cmdlet har lagts till för att anropa en edge-modulmetod i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="43970-133">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="43970-134">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="43970-134">Az.KeyVault</span></span>
* <span data-ttu-id="43970-135">Har lagt till en ny cmdlet, "Update-AzKeyVault", som kan aktivera mjuk borttagning och rensning av skydd i ett valv</span><span class="sxs-lookup"><span data-stu-id="43970-135">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="43970-136">Har lagt till stöd i Microsoft.PowerShell.SecretManagement [#11178]</span><span class="sxs-lookup"><span data-stu-id="43970-136">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="43970-137">Åtgärdat fel i exemplen i 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span><span class="sxs-lookup"><span data-stu-id="43970-137">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="43970-138">Har lagt till stöd för privat slutpunkt</span><span class="sxs-lookup"><span data-stu-id="43970-138">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="43970-139">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="43970-139">Az.Maintenance</span></span>
* <span data-ttu-id="43970-140">Publicerar slutversion av underhålls-cmdletar för GA</span><span class="sxs-lookup"><span data-stu-id="43970-140">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="43970-141">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="43970-141">Az.Monitor</span></span>
* <span data-ttu-id="43970-142">Har lagt till cmdletar för privat länkomfång</span><span class="sxs-lookup"><span data-stu-id="43970-142">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="43970-143">'Get-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="43970-143">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="43970-144">'Remove-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="43970-144">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="43970-145">'New-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="43970-145">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="43970-146">'Update-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="43970-146">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="43970-147">'Get-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="43970-147">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="43970-148">'New-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="43970-148">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="43970-149">'Remove-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="43970-149">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="43970-150">Az.Network</span><span class="sxs-lookup"><span data-stu-id="43970-150">Az.Network</span></span>
* <span data-ttu-id="43970-151">Uppdaterade cmdletar för att aktivera anslutning på privat IP för Virtual Network Gateway.</span><span class="sxs-lookup"><span data-stu-id="43970-151">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="43970-152">'New-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="43970-152">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="43970-153">'Set-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="43970-153">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="43970-154">'New-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="43970-154">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="43970-155">'Set-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="43970-155">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="43970-156">Uppdaterade cmdletar för att aktivera FQDN-baserade LocalNetworkGateways och VpnSites</span><span class="sxs-lookup"><span data-stu-id="43970-156">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="43970-157">'New-AzLocalNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="43970-157">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="43970-158">'New-AzVpnSiteLink'</span><span class="sxs-lookup"><span data-stu-id="43970-158">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="43970-159">Stöd har lagts till för IPv6-adresstypen i ExpressRouteCircuitConnectionConfig (Global Reach)</span><span class="sxs-lookup"><span data-stu-id="43970-159">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="43970-160">Lade till 'Set-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="43970-160">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="43970-161">tillåter inställning av alla befintliga egenskaper inklusive IPv6CircuitConnectionProperties</span><span class="sxs-lookup"><span data-stu-id="43970-161">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="43970-162">Uppdaterade 'Add-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="43970-162">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="43970-163">Lade till en ytterligare valfri parameter, AddressPrefixType, för att specificera adresstypen för adressprefix</span><span class="sxs-lookup"><span data-stu-id="43970-163">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="43970-164">Uppdaterade cmdletar för att aktivera inställningen för DPD-timeout på Virtual Network Gateway-anslutningar.</span><span class="sxs-lookup"><span data-stu-id="43970-164">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="43970-165">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="43970-165">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="43970-166">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="43970-166">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="43970-167">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="43970-167">Az.PolicyInsights</span></span>
* <span data-ttu-id="43970-168">Cmdleten "Start-AzPolicyComplianceScan" har lagts till för att utlösa genomsökningar av principefterlevnad</span><span class="sxs-lookup"><span data-stu-id="43970-168">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="43970-169">Principdefinition, uppsättningsdefinition och tilldelningsversioner har lagts till i "Get-AzPolicyState"-utdata</span><span class="sxs-lookup"><span data-stu-id="43970-169">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="43970-170">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="43970-170">Az.ServiceFabric</span></span>
* <span data-ttu-id="43970-171">Förbättrad kodformatering och användbarhet för "New-AzServiceFabricCluster"-exempel</span><span class="sxs-lookup"><span data-stu-id="43970-171">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="43970-172">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="43970-172">Az.Sql</span></span>
* <span data-ttu-id="43970-173">Lade till cmdletarna "Get-AzSqlInstanceOperation" och "Stop-AzSqlInstanceOperation"</span><span class="sxs-lookup"><span data-stu-id="43970-173">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="43970-174">Stöd för granskning för ett lagringskonto i VNet.</span><span class="sxs-lookup"><span data-stu-id="43970-174">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="43970-175">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="43970-175">Az.Storage</span></span>
* <span data-ttu-id="43970-176">Lade till meddelande om icke-bakåtkompatibel ändring vid ändring i utdata för Azure File-cmdletar i en framtida version</span><span class="sxs-lookup"><span data-stu-id="43970-176">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="43970-177">Stöd för nya SkuName StandardGZRS, StandardRAGZRS när ett lagringskonto skapas/uppdateras</span><span class="sxs-lookup"><span data-stu-id="43970-177">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="43970-178">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="43970-178">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="43970-179">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="43970-179">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="43970-180">Stöd för DataLake Gen2</span><span class="sxs-lookup"><span data-stu-id="43970-180">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="43970-181">'New-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="43970-181">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="43970-182">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="43970-182">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="43970-183">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="43970-183">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="43970-184">'Move-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="43970-184">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="43970-185">'Set-AzDataLakeGen2ItemAclObject'</span><span class="sxs-lookup"><span data-stu-id="43970-185">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="43970-186">'Update-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="43970-186">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="43970-187">'Get-AzDataLakeGen2ItemContent'</span><span class="sxs-lookup"><span data-stu-id="43970-187">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="43970-188">'Remove-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="43970-188">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="43970-189">0.10.0-förhandsversion – April 2020</span><span class="sxs-lookup"><span data-stu-id="43970-189">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="43970-190">Allmänt</span><span class="sxs-lookup"><span data-stu-id="43970-190">General</span></span>
* <span data-ttu-id="43970-191">Az-moduler är nu tillgängliga i förhandsversion på Azure Stack Hub.</span><span class="sxs-lookup"><span data-stu-id="43970-191">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="43970-192">Därmed möjliggörs kompatibilitet för flera plattformar med Linux och macOs.</span><span class="sxs-lookup"><span data-stu-id="43970-192">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="43970-193">Azure Stack Hub stöder nu PowerShell Core med AZ-moduler. Mer information finns [här](https://aka.ms/az4AzureStack)</span><span class="sxs-lookup"><span data-stu-id="43970-193">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](https://aka.ms/az4AzureStack)</span></span>
* <span data-ttu-id="43970-194">Supportprofil för AZ-moduler 2019-03-01-hybrid:</span><span class="sxs-lookup"><span data-stu-id="43970-194">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="43970-195">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="43970-195">Az.Billing</span></span>
  - <span data-ttu-id="43970-196">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="43970-196">Az.Compute</span></span>
  - <span data-ttu-id="43970-197">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="43970-197">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="43970-198">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="43970-198">Az.EventHub</span></span>
  - <span data-ttu-id="43970-199">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="43970-199">Az.IotHub</span></span>
  - <span data-ttu-id="43970-200">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="43970-200">Az.KeyVault</span></span>
  - <span data-ttu-id="43970-201">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="43970-201">Az.Monitor</span></span>
  - <span data-ttu-id="43970-202">Az.Network</span><span class="sxs-lookup"><span data-stu-id="43970-202">Az.Network</span></span>
  - <span data-ttu-id="43970-203">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="43970-203">Az.Resources</span></span>
  - <span data-ttu-id="43970-204">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="43970-204">Az.Storage</span></span>
  - <span data-ttu-id="43970-205">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="43970-205">Az.Websites</span></span>
* <span data-ttu-id="43970-206">Tre nya PowerShell-moduler för AZ har introducerats som fungerar med Azure Stack Hub, och de är Az.Databox, Az.IotHub och Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="43970-206">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="43970-207">Kommandona är i princip oförändrade, med endast mindre ändringar som att AzureRM ändras till AZ</span><span class="sxs-lookup"><span data-stu-id="43970-207">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="43970-208">En uppdaterad länk till PowerShell-dokumentationen för Azure Stack Hub finns [här](https://aka.ms/InstallASHPowerShell)</span><span class="sxs-lookup"><span data-stu-id="43970-208">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](https://aka.ms/InstallASHPowerShell)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="43970-209">3.7.0 – mars 2020</span><span class="sxs-lookup"><span data-stu-id="43970-209">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="43970-210">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="43970-210">Az.Accounts</span></span>
* <span data-ttu-id="43970-211">Åtgärdade ”Get-AzTenant”/”Get-AzDefault”/”Set-AzDefault”-utlösning av NullReferenceException när du inte är inloggad [#10292]</span><span class="sxs-lookup"><span data-stu-id="43970-211">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="43970-212">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="43970-212">Az.Compute</span></span>
* <span data-ttu-id="43970-213">Följande parametrar har lagts till i cmdleten ”New-AzDiskConfig”:</span><span class="sxs-lookup"><span data-stu-id="43970-213">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="43970-214">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="43970-214">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="43970-215">Tillåten krypteringsegenskap till målparametern för cmdleten ”New-AzGalleryImageVersion”.</span><span class="sxs-lookup"><span data-stu-id="43970-215">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="43970-216">Åtgärdade tempDisk-problem för cmdletarna ”Set-AzVmss”-Reimage och ”Invoke-AzVMReimage”.</span><span class="sxs-lookup"><span data-stu-id="43970-216">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="43970-217">[#11354]</span><span class="sxs-lookup"><span data-stu-id="43970-217">[#11354]</span></span>
* <span data-ttu-id="43970-218">Stöd har lagts till i nedanstående cmdletar för nytt SAP-tillägg</span><span class="sxs-lookup"><span data-stu-id="43970-218">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="43970-219">”Set-AzVMAEMExtension”</span><span class="sxs-lookup"><span data-stu-id="43970-219">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="43970-220">”Get-AzVMAEMExtension”</span><span class="sxs-lookup"><span data-stu-id="43970-220">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="43970-221">”Remove-AzVMAEMExtension”</span><span class="sxs-lookup"><span data-stu-id="43970-221">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="43970-222">”Update-AzVMAEMExtension”</span><span class="sxs-lookup"><span data-stu-id="43970-222">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="43970-223">Åtgärdade fel i exempel på hjälpdokument</span><span class="sxs-lookup"><span data-stu-id="43970-223">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="43970-224">Visade det exakta strängvärdet för VM PowerState i tabellformat.</span><span class="sxs-lookup"><span data-stu-id="43970-224">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="43970-225">”New-AzVmssConfig”: den fasta serialiseringen av egenskapen AutomaticRepairs när SinglePlacementGroup är inaktiverad.</span><span class="sxs-lookup"><span data-stu-id="43970-225">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="43970-226">[#11257]</span><span class="sxs-lookup"><span data-stu-id="43970-226">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="43970-227">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="43970-227">Az.DataFactory</span></span>
* <span data-ttu-id="43970-228">ADF .Net SDK har uppdaterats till 4.8.0</span><span class="sxs-lookup"><span data-stu-id="43970-228">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="43970-229">Valfria parametrar har lagts till i kommandot ”Invoke-AzDataFactoryV2Pipeline” för att stödja omkörning</span><span class="sxs-lookup"><span data-stu-id="43970-229">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="43970-230">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="43970-230">Az.DataLakeStore</span></span>
* <span data-ttu-id="43970-231">Lade till beskrivning för icke-bakåtkompatibel ändring för ”Export-AzDataLakeStoreItem” och ”Import-AzDataLakeStoreItem”</span><span class="sxs-lookup"><span data-stu-id="43970-231">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="43970-232">Lade till alternativ för bytekodning för ”New-AzDataLakeStoreItem”, ”Add-AzDAtaLakeStoreItemContent” och ”Get-AzDAtaLakeStoreItemContent”</span><span class="sxs-lookup"><span data-stu-id="43970-232">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="43970-233">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="43970-233">Az.HDInsight</span></span>
* <span data-ttu-id="43970-234">Stöd för att ange en minimal TLS-version som stöds när klustret skapas.</span><span class="sxs-lookup"><span data-stu-id="43970-234">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="43970-235">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="43970-235">Az.IotHub</span></span>
* <span data-ttu-id="43970-236">Stöd har lagts till för att hantera distribuerade inställningar per enhet.</span><span class="sxs-lookup"><span data-stu-id="43970-236">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="43970-237">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="43970-237">New Cmdlets are:</span></span>
    - <span data-ttu-id="43970-238">”Get-AzIotHubDistributedTracing”</span><span class="sxs-lookup"><span data-stu-id="43970-238">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="43970-239">”Set-AzIotHubDistributedTracing”</span><span class="sxs-lookup"><span data-stu-id="43970-239">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="43970-240">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="43970-240">Az.KeyVault</span></span>
* <span data-ttu-id="43970-241">Ändrade attribut för icke-bakåtkompatibel ändring lades till för ”New-AzKeyVault”</span><span class="sxs-lookup"><span data-stu-id="43970-241">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="43970-242">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="43970-242">Az.Monitor</span></span>
* <span data-ttu-id="43970-243">Uppdaterad dokumentation för ”New-AzScheduledQueryRuleLogMetricTrigger”</span><span class="sxs-lookup"><span data-stu-id="43970-243">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="43970-244">Az.Network</span><span class="sxs-lookup"><span data-stu-id="43970-244">Az.Network</span></span>
* <span data-ttu-id="43970-245">Uppdaterade cmdletar för att tillåta VirtualHubVnetConnections mellan klienter</span><span class="sxs-lookup"><span data-stu-id="43970-245">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="43970-246">”New-AzVirtualHubVnetConnection”</span><span class="sxs-lookup"><span data-stu-id="43970-246">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="43970-247">”Update-AzVirtualHubVnetConnection”</span><span class="sxs-lookup"><span data-stu-id="43970-247">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="43970-248">”New-AzVirtualHub”</span><span class="sxs-lookup"><span data-stu-id="43970-248">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="43970-249">”Update-AzVirtualHub”</span><span class="sxs-lookup"><span data-stu-id="43970-249">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="43970-250">SQL Management SDK-beroende har tagits bort</span><span class="sxs-lookup"><span data-stu-id="43970-250">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="43970-251">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="43970-251">Az.PolicyInsights</span></span>
* <span data-ttu-id="43970-252">Förbättrade felmeddelanden</span><span class="sxs-lookup"><span data-stu-id="43970-252">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="43970-253">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="43970-253">Az.RecoveryServices</span></span>
* <span data-ttu-id="43970-254">Azure Site Recovery har lagt till stöd för återaktivering av skydd och uppdaterade VM-egenskaper för virtuella Azure-datorer med krypterad disk.</span><span class="sxs-lookup"><span data-stu-id="43970-254">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="43970-255">Lade till Azure Site Recovery VmwareToAzure-egenskaper för DR-övervakning</span><span class="sxs-lookup"><span data-stu-id="43970-255">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="43970-256">Azure Backup har lagt till stöd för att försöka uppdatera principuppdateringen för misslyckade objekt på nytt.</span><span class="sxs-lookup"><span data-stu-id="43970-256">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="43970-257">Azure Backup lagt till stöd för diskundantagsinställningar under säkerhetskopiering och återställning.</span><span class="sxs-lookup"><span data-stu-id="43970-257">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="43970-258">Azure Backup lagt till stöd för att återställa flera filer/mappar i AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="43970-258">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="43970-259">Azure Backup lade till support för användardefinierad Resourcegroup-support vid uppdatering av IaasVM-princip</span><span class="sxs-lookup"><span data-stu-id="43970-259">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="43970-260">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="43970-260">Az.Resources</span></span>
* <span data-ttu-id="43970-261">Åtgärdade ”Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType” så att den använder den faktisk apiVersion av resurser i stället för standard-apiVersion [#11267]</span><span class="sxs-lookup"><span data-stu-id="43970-261">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="43970-262">Lade till correlationId-loggning för felscenarier</span><span class="sxs-lookup"><span data-stu-id="43970-262">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="43970-263">Liten dokumentationsändring för ”Get-AzResourceLock”.</span><span class="sxs-lookup"><span data-stu-id="43970-263">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="43970-264">Lade till exempel.</span><span class="sxs-lookup"><span data-stu-id="43970-264">Added example.</span></span>
* <span data-ttu-id="43970-265">Undantaget enkelt citattecken i parametervärde för ”Get-AzADUser” [#11317]</span><span class="sxs-lookup"><span data-stu-id="43970-265">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="43970-266">Nya cmdletar har lagts till för distributionsskript (”Get-AzDeploymentScript”, ”Get-AzDeploymentScriptLog”, ”Save-AzDeploymentScriptLog”, ”Remove-AzDeploymentScript”)</span><span class="sxs-lookup"><span data-stu-id="43970-266">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="43970-267">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="43970-267">Az.Sql</span></span>
* <span data-ttu-id="43970-268">En läsbar sekundär parameter har lagts till i Invoke-AzSqlDatabaseFailover</span><span class="sxs-lookup"><span data-stu-id="43970-268">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="43970-269">Cmdleten Disable-AzSqlServerActiveDirectoryOnlyAuthentication har lagts till</span><span class="sxs-lookup"><span data-stu-id="43970-269">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="43970-270">Den sparade känslighet rangordningen när kolumner klassificeras i databasen.</span><span class="sxs-lookup"><span data-stu-id="43970-270">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="43970-271">Az.Support</span><span class="sxs-lookup"><span data-stu-id="43970-271">Az.Support</span></span>
* <span data-ttu-id="43970-272">Allmän tillgänglighet för ”Az.Support”-modulen</span><span class="sxs-lookup"><span data-stu-id="43970-272">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="43970-273">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="43970-273">Az.Websites</span></span>
* <span data-ttu-id="43970-274">Stöd har lagts till för att arbeta med trafikdirigeringsregler för webbappar under nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="43970-274">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="43970-275">”Get-AzWebAppTrafficRouting”</span><span class="sxs-lookup"><span data-stu-id="43970-275">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="43970-276">”Update-AzWebAppTrafficRouting”</span><span class="sxs-lookup"><span data-stu-id="43970-276">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="43970-277">”Add-AzWebAppTrafficRouting”</span><span class="sxs-lookup"><span data-stu-id="43970-277">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="43970-278">”Remove-AzWebAppTrafficRouting”</span><span class="sxs-lookup"><span data-stu-id="43970-278">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="43970-279">3.6.1 – mars 2020</span><span class="sxs-lookup"><span data-stu-id="43970-279">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="43970-280">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="43970-280">Az.Accounts</span></span>
* <span data-ttu-id="43970-281">Öppna sidan med Azure PowerShell-enkäten i ”Send-Feedback” [#11020]</span><span class="sxs-lookup"><span data-stu-id="43970-281">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="43970-282">Visa URL:en för Azure PowerShell-enkäten i ”Resolve-Error” [#11021]</span><span class="sxs-lookup"><span data-stu-id="43970-282">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="43970-283">Az-version har lagts till i UserAgent</span><span class="sxs-lookup"><span data-stu-id="43970-283">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="43970-284">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="43970-284">Az.ApiManagement</span></span>
* <span data-ttu-id="43970-285">Stöd har lagts till för att hämta och konfigurera en anpassad domän på DeveloperPortal-slutpunkten [#11007]</span><span class="sxs-lookup"><span data-stu-id="43970-285">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="43970-286">”Export-AzApiManagementApi” Stöd har lagts till för att ladda ned API-definition i Json-format [#9987]</span><span class="sxs-lookup"><span data-stu-id="43970-286">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="43970-287">”Import-AzApiManagementApi” Stöd har lagts till för att importera OpenApi 3.0-definition från Json-dokument</span><span class="sxs-lookup"><span data-stu-id="43970-287">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="43970-288">”New-AzApiManagementIdentityProvider” och ”Set-AzApiManagementIdentityProvider” Stöd har lagts till för att konfigurera ”Signin Tenant” för AAD B2C-provider [#9784]</span><span class="sxs-lookup"><span data-stu-id="43970-288">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="43970-289">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="43970-289">Az.DataLakeStore</span></span>
* <span data-ttu-id="43970-290">En referens har uttryckligen lagts till för System.Buffers i csproj och psd1.</span><span class="sxs-lookup"><span data-stu-id="43970-290">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="43970-291">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="43970-291">Az.IotHub</span></span>
* <span data-ttu-id="43970-292">Lade till stöd för att hantera enheter i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="43970-292">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="43970-293">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="43970-293">New Cmdlets are:</span></span>
    - <span data-ttu-id="43970-294">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="43970-294">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="43970-295">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="43970-295">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="43970-296">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="43970-296">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="43970-297">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="43970-297">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="43970-298">Stöd har lagts till för att hantera moduler på en mål-IoT-enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="43970-298">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="43970-299">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="43970-299">New Cmdlets are:</span></span>
    - <span data-ttu-id="43970-300">”Add-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="43970-300">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="43970-301">”Get-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="43970-301">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="43970-302">”Remove-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="43970-302">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="43970-303">”Set-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="43970-303">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="43970-304">Cmdlet har lagts till för att hämta anslutningssträngen för en mål-IoT-enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="43970-304">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="43970-305">Cmdlet har lagts till för att hämta anslutningssträngen för en modul på en mål-IoT-enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="43970-305">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="43970-306">Stöd har lagts till för att hämta/ange en överordnad enhet för en IoT-enhet.</span><span class="sxs-lookup"><span data-stu-id="43970-306">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="43970-307">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="43970-307">New Cmdlets are:</span></span>
    - <span data-ttu-id="43970-308">”Get-AzIotHubDeviceParent”</span><span class="sxs-lookup"><span data-stu-id="43970-308">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="43970-309">”Set-AzIotHubDeviceParent”</span><span class="sxs-lookup"><span data-stu-id="43970-309">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="43970-310">Stöd har lagts till för att hantera en enhets överordnade och underordnade relationer.</span><span class="sxs-lookup"><span data-stu-id="43970-310">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="43970-311">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="43970-311">Az.Monitor</span></span>
* <span data-ttu-id="43970-312">Utdatavärdet har åtgärdats för ”Get-AzMetricDefinition” [#9714]</span><span class="sxs-lookup"><span data-stu-id="43970-312">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="43970-313">Az.Network</span><span class="sxs-lookup"><span data-stu-id="43970-313">Az.Network</span></span>
* <span data-ttu-id="43970-314">SQL Management SDK har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="43970-314">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="43970-315">Ett problem har åtgärdats med namngivningsskillnader i klassen PrivateLinkServiceConnectionState.</span><span class="sxs-lookup"><span data-stu-id="43970-315">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="43970-316">Fältet ActionsRequired mappar till ActionRequired.</span><span class="sxs-lookup"><span data-stu-id="43970-316">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="43970-317">PublicNetworkAccess har lagts till i ”New-AzSqlServer” och ”Set-AzSqlServer”</span><span class="sxs-lookup"><span data-stu-id="43970-317">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="43970-318">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="43970-318">Az.Resources</span></span>
* <span data-ttu-id="43970-319">Null-referensfel har åtgärdats i ”Get-AzRoleAssignment”</span><span class="sxs-lookup"><span data-stu-id="43970-319">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="43970-320">Växlarna ”-Force” och ”-PassThru” är valfria i ”Remove-AzADGroup” [#10849]</span><span class="sxs-lookup"><span data-stu-id="43970-320">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="43970-321">Ett problem har åtgärdats som gjorde att ”MailNickname” inte returnerades i ”Remove-AzADGroup” [#11167]</span><span class="sxs-lookup"><span data-stu-id="43970-321">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="43970-322">Ett problem har åtgärdats som gjorde att pipe-åtgärden ”Remove-AzADGroup” inte fungerar [#11171]</span><span class="sxs-lookup"><span data-stu-id="43970-322">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="43970-323">Ett null-referensfel har åtgärdats i GetAzureRoleAssignmentCommand</span><span class="sxs-lookup"><span data-stu-id="43970-323">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="43970-324">Attribut för icke-bakåtkompatibla ändringar har lagts till för kommande ändringar i cmdlets för principer</span><span class="sxs-lookup"><span data-stu-id="43970-324">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="43970-325">”Get-AzResourceGroup” har uppdaterats för att utföra taggfiltrering för resursgrupper på serversidan</span><span class="sxs-lookup"><span data-stu-id="43970-325">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="43970-326">Utökade Tag-cmdlets stöder -ResourceId</span><span class="sxs-lookup"><span data-stu-id="43970-326">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="43970-327">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="43970-327">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="43970-328">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="43970-328">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="43970-329">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="43970-329">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="43970-330">Ny Tag-cmdlet har lagts till</span><span class="sxs-lookup"><span data-stu-id="43970-330">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="43970-331">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="43970-331">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="43970-332">Flyttade ScopedDeployment från SDK 3.3.0</span><span class="sxs-lookup"><span data-stu-id="43970-332">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="43970-333">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="43970-333">Az.Sql</span></span>
* <span data-ttu-id="43970-334">PublicNetworkAccess har lagts till i ”New-AzSqlServer” och ”Set-AzSqlServer”</span><span class="sxs-lookup"><span data-stu-id="43970-334">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="43970-335">Stöd har lagts till för konfiguration av säkerhetskopiering för långsiktig kvarhållning för hanterade databaser</span><span class="sxs-lookup"><span data-stu-id="43970-335">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="43970-336">Hämta/ange LTR-princip på en hanterad databas</span><span class="sxs-lookup"><span data-stu-id="43970-336">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="43970-337">Hämta LTR-säkerhetskopior efter hanterad databas, hanterad instans eller plats</span><span class="sxs-lookup"><span data-stu-id="43970-337">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="43970-338">Ta bort en LTR-säkerhetskopia</span><span class="sxs-lookup"><span data-stu-id="43970-338">Remove an LTR backup</span></span>
    - <span data-ttu-id="43970-339">Återställa en LTR-säkerhetskopia för att skapa en ny hanterad databas</span><span class="sxs-lookup"><span data-stu-id="43970-339">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="43970-340">MinimalTlsVersion har lagts till för New-AzSqlServer och Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="43970-340">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="43970-341">MinimalTlsVersion har lagts till för New-AzSqlInstance och Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="43970-341">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="43970-342">SQL SDK-versionen för Az.Network har ändrats</span><span class="sxs-lookup"><span data-stu-id="43970-342">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="43970-343">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="43970-343">Az.Storage</span></span>
* <span data-ttu-id="43970-344">AllowProtectedAppendWrite stöds i ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="43970-344">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="43970-345">”Set-AzRmStorageContainerImmutabilityPolicy”</span><span class="sxs-lookup"><span data-stu-id="43970-345">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="43970-346">Varningsmeddelande har lagts till om icke-bakåtkompatibel ändring för ändring av typen AzureStorageTable i en senare version</span><span class="sxs-lookup"><span data-stu-id="43970-346">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="43970-347">”New-AzStorageTable”</span><span class="sxs-lookup"><span data-stu-id="43970-347">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="43970-348">”Get-AzStorageTable”</span><span class="sxs-lookup"><span data-stu-id="43970-348">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="43970-349">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="43970-349">Az.Websites</span></span>
* <span data-ttu-id="43970-350">Tag-parametern har lagts till för ”New-AzAppServicePlan” och ”Set-AzAppServicePlan”</span><span class="sxs-lookup"><span data-stu-id="43970-350">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="43970-351">Stoppa cmdlet-körning om ett undantag uppstår när en anpassad domän läggs till på en webbplats</span><span class="sxs-lookup"><span data-stu-id="43970-351">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="43970-352">Stöd har lagts till för att utföra åtgärder för App Services som inte tillhör samma resursgrupp som App Services-planen</span><span class="sxs-lookup"><span data-stu-id="43970-352">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="43970-353">Åtkomstbegränsning har tillämpats på WebApp/Function i olika resursgrupper</span><span class="sxs-lookup"><span data-stu-id="43970-353">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="43970-354">Ett problem har åtgärdats för att ange anpassade värdnamn för WebAppSlots</span><span class="sxs-lookup"><span data-stu-id="43970-354">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="43970-355">3.5.0 – februari 2020</span><span class="sxs-lookup"><span data-stu-id="43970-355">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="43970-356">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="43970-356">Highlights since the last major release</span></span>
* <span data-ttu-id="43970-357">Uppdaterade telemetri på klientsidan.</span><span class="sxs-lookup"><span data-stu-id="43970-357">Updated client side telemetry.</span></span>
* <span data-ttu-id="43970-358">Az.IotHub lade till cmdletar som stöd för att hantera enheter.</span><span class="sxs-lookup"><span data-stu-id="43970-358">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="43970-359">Az.SqlVirtualMachine lade till cmdletar för lyssningsfunktion för tillgänglighetsgrupp.</span><span class="sxs-lookup"><span data-stu-id="43970-359">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="43970-360">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="43970-360">Az.Accounts</span></span>
* <span data-ttu-id="43970-361">Lade till SubscriptionId, TenantId och körningstid i data för telemetri på klientsidan</span><span class="sxs-lookup"><span data-stu-id="43970-361">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="43970-362">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="43970-362">Az.Automation</span></span>
* <span data-ttu-id="43970-363">Åtgärdade skrivfel i exempel 1 i referensdokumentation för ”New-AzAutomationSoftwareUpdateConfiguration”</span><span class="sxs-lookup"><span data-stu-id="43970-363">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="43970-364">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="43970-364">Az.CognitiveServices</span></span>
* <span data-ttu-id="43970-365">Uppdaterade SDK till 7.0</span><span class="sxs-lookup"><span data-stu-id="43970-365">Updated SDK to 7.0</span></span>
* <span data-ttu-id="43970-366">Förbättrade felmeddelande vid serversvar om tom brödtext</span><span class="sxs-lookup"><span data-stu-id="43970-366">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="43970-367">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="43970-367">Az.Compute</span></span>
* <span data-ttu-id="43970-368">Tillät tomt värde för ProximityPlacementGroupId under uppdatering</span><span class="sxs-lookup"><span data-stu-id="43970-368">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="43970-369">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="43970-369">Az.FrontDoor</span></span>
* <span data-ttu-id="43970-370">Lade till cmdlet för att hämta hanterade regeldefinitioner som kan användas i WAF</span><span class="sxs-lookup"><span data-stu-id="43970-370">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="43970-371">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="43970-371">Az.IotHub</span></span>
* <span data-ttu-id="43970-372">Lade till stöd för att hantera enheter i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="43970-372">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="43970-373">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="43970-373">New Cmdlets are:</span></span>
    - <span data-ttu-id="43970-374">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="43970-374">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="43970-375">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="43970-375">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="43970-376">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="43970-376">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="43970-377">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="43970-377">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="43970-378">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="43970-378">Az.KeyVault</span></span>
* <span data-ttu-id="43970-379">Åtgärdade duplicerad text för Add-AzKeyVaultKey.md</span><span class="sxs-lookup"><span data-stu-id="43970-379">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="43970-380">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="43970-380">Az.Monitor</span></span>
* <span data-ttu-id="43970-381">Åtgärdade beskrivning av cmdleten Get-AzLog.</span><span class="sxs-lookup"><span data-stu-id="43970-381">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="43970-382">En ny parameter med namnet ActionGroupId har lagts till i kommandot ”New-AzMetricAlertRuleV2”.</span><span class="sxs-lookup"><span data-stu-id="43970-382">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="43970-383">Användaren kan ange ActionGroupId(string) eller ActionGroup(ActivityLogAlertActionGroup).</span><span class="sxs-lookup"><span data-stu-id="43970-383">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="43970-384">Az.Network</span><span class="sxs-lookup"><span data-stu-id="43970-384">Az.Network</span></span>
* <span data-ttu-id="43970-385">Lade till en extra parameteranteckning för parametern ”-EnableProxyProtocol” för cmdleten ”New-AzPrivateLinkService”.</span><span class="sxs-lookup"><span data-stu-id="43970-385">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="43970-386">Åtgärdade FilterData-exempel i Start-AzVirtualNetworkGatewayConnectionPacketCapture.md och Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="43970-386">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="43970-387">Lade till paketinsamlingsexempel för att samla in alla inre och yttre paket i Start-AzVirtualNetworkGatewayConnectionPacketCapture.md och Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="43970-387">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="43970-388">Lade till stöd för Azure-brandväggsprincip på VNet-brandväggar</span><span class="sxs-lookup"><span data-stu-id="43970-388">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="43970-389">Inga nya cmdletar har lagts till.</span><span class="sxs-lookup"><span data-stu-id="43970-389">No new cmdlets are added.</span></span> <span data-ttu-id="43970-390">Lättar begränsningen för brandväggsprincip på VNet-brandväggar</span><span class="sxs-lookup"><span data-stu-id="43970-390">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="43970-391">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="43970-391">Az.RecoveryServices</span></span>
* <span data-ttu-id="43970-392">Lade till stöd för Restore-as-files för SQL-databaser.</span><span class="sxs-lookup"><span data-stu-id="43970-392">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="43970-393">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="43970-393">Az.Resources</span></span>
* <span data-ttu-id="43970-394">Omstrukturerade cmdletar för malldistribution</span><span class="sxs-lookup"><span data-stu-id="43970-394">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="43970-395">Lade till nya cmdletar för att hantera distributioner i hanteringsgruppen: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="43970-395">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="43970-396">Lade till nya cmdletar för att hantera distributioner i klientorganisationsområdet: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="43970-396">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="43970-397">Omstrukturerade \*-AzDeployment-cmdletar för att fungera specifikt i prenumerationsomfattningen</span><span class="sxs-lookup"><span data-stu-id="43970-397">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="43970-398">Skapade alias \*-AzSubscriptionDeployment för \*-AzDeployment-cmdletar</span><span class="sxs-lookup"><span data-stu-id="43970-398">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="43970-399">Åtgärdade ”Update-AzADApplication” när parametern ”AvailableToOtherTenants” inte har angetts</span><span class="sxs-lookup"><span data-stu-id="43970-399">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="43970-400">Tog bort ApplicationObjectWithoutCredentialParameterSet för att undvika AmbiguousParameterSetException.</span><span class="sxs-lookup"><span data-stu-id="43970-400">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="43970-401">Återskapade hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="43970-401">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="43970-402">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="43970-402">Az.Sql</span></span>
* <span data-ttu-id="43970-403">Lade till stöd för återställning till tidpunkt mellan prenumerationer på hanterade instanser.</span><span class="sxs-lookup"><span data-stu-id="43970-403">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="43970-404">Lade till stöd för att ändra befintlig SQL Managed Instance-maskinvarugenerering</span><span class="sxs-lookup"><span data-stu-id="43970-404">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="43970-405">Åtgärdade ”Update-AzSqlServerVulnerabilityAssessmentSetting”-hjälpexempel: parameter/egenskapsutdata - EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="43970-405">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="43970-406">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="43970-406">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="43970-407">Lade till cmdletar för lyssningsfunktion för tillgänglighetsgrupp</span><span class="sxs-lookup"><span data-stu-id="43970-407">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="43970-408">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="43970-408">Az.StorageSync</span></span>
* <span data-ttu-id="43970-409">Uppdaterade teckenuppsättningar som stöds i ”Invoke-AzStorageSyncCompatibilityCheck”.</span><span class="sxs-lookup"><span data-stu-id="43970-409">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="43970-410">3.4.0 – februari 2020</span><span class="sxs-lookup"><span data-stu-id="43970-410">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="43970-411">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="43970-411">Highlights since the last major release</span></span>
* <span data-ttu-id="43970-412">Första Az.CosmosDB-versionen 0.1.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="43970-412">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="43970-413">Stöd för Az.Network ConnectionMonitor V2 har lagts till</span><span class="sxs-lookup"><span data-stu-id="43970-413">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="43970-414">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="43970-414">Az.Accounts</span></span>
* <span data-ttu-id="43970-415">Inaktivera automatisk sparande av kontext när AzureRmContext.json inte är tillgängligt</span><span class="sxs-lookup"><span data-stu-id="43970-415">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="43970-416">Uppdatera referensen till Azure Powershell Common till 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="43970-416">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="43970-417">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="43970-417">Az.ApiManagement</span></span>
* <span data-ttu-id="43970-418">**Get-AzApiManagementApiSchema** Hämtning av Open-Api-schema som är associerat med ett API har åtgärdats   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="43970-418">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="43970-419">**New-AzApiManagementProduct**\* och **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="43970-419">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="43970-420">Åtgärda dokumentation för https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="43970-420">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="43970-421">**Set-AzApiManagementApi** Exempel för att visa hur ServiceUrl uppdateras med hjälp av cmdleten har lagts till</span><span class="sxs-lookup"><span data-stu-id="43970-421">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="43970-422">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="43970-422">Az.Compute</span></span>
* <span data-ttu-id="43970-423">Begränsa antalet VM-status till 100 för att undvika begränsning när Get-AzVM -Status utförs utan VM-namn.</span><span class="sxs-lookup"><span data-stu-id="43970-423">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="43970-424">Lägg till cmdleten Update-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="43970-424">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="43970-425">Lägg till parametrarna EncryptionType och DiskEncryptionSetId i följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="43970-425">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="43970-426">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="43970-426">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="43970-427">Lägg till parametern ColocationStatus för cmdleten Get-AzProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="43970-427">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="43970-428">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="43970-428">Az.DataFactory</span></span>
* <span data-ttu-id="43970-429">Uppdatera ADF .Net SDK-versionen till 4.7.0</span><span class="sxs-lookup"><span data-stu-id="43970-429">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="43970-430">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="43970-430">Az.DeploymentManager</span></span>
* <span data-ttu-id="43970-431">Lägger till LIST-åtgärder för resurser</span><span class="sxs-lookup"><span data-stu-id="43970-431">Adds LIST operations for resources</span></span>
* <span data-ttu-id="43970-432">Lägger till funktion för att utföra åtgärder för hälsokontrollsteg</span><span class="sxs-lookup"><span data-stu-id="43970-432">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="43970-433">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="43970-433">Az.HDInsight</span></span>
* <span data-ttu-id="43970-434">Åtgärda dokumentfel för New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="43970-434">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="43970-435">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="43970-435">Az.KeyVault</span></span>
* <span data-ttu-id="43970-436">Lägg till Name-alias för attributet VaultName så att Remove-AzureKeyVault stämmer överens med New-AzureKeyVault.</span><span class="sxs-lookup"><span data-stu-id="43970-436">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="43970-437">Az.Network</span><span class="sxs-lookup"><span data-stu-id="43970-437">Az.Network</span></span>
* <span data-ttu-id="43970-438">Nytt exempel har lagts till i Set-AzNetworkWatcherConfigFlowLog.md för att demonstrera ett inaktiveringsscenario för Trafikanalys.</span><span class="sxs-lookup"><span data-stu-id="43970-438">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="43970-439">Lägg till stöd för att tilldela konfiguration av hanterings-IP till Azure Firewall – ett dedikerat undernät och en offentlig IP som brandväggen använder för dess hanteringstrafik</span><span class="sxs-lookup"><span data-stu-id="43970-439">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="43970-440">Cmdleten New-AzFirewall har uppdaterats:</span><span class="sxs-lookup"><span data-stu-id="43970-440">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="43970-441">Parametern -ManagementPublicIpAddress (inte obligatorisk) som accepterar ett offentligt IP-adressobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="43970-441">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="43970-442">Metoden SetManagementIpConfiguration har lagts till för brandväggsobjekt – kräver ett undernät och en offentlig IP-adress som indata – undernätets namn måste vara ”AzureFirewallManagementSubnet”</span><span class="sxs-lookup"><span data-stu-id="43970-442">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="43970-443">Exempel för Get-AzNetworkSecurityGroup har korrigerats så att exempel visas för NSG:er i stället för nätverksgränssnitt.</span><span class="sxs-lookup"><span data-stu-id="43970-443">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="43970-444">Ett skrivfel har åtgärdats i kommandot New-AzVpnSite som hindrade kompletteraren för resurs-ID från att fylla i en parameter.</span><span class="sxs-lookup"><span data-stu-id="43970-444">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="43970-445">Stöd för Url-konfiguration i åtgärdsuppsättningen för omskrivningsregler i Application Gateway har lagts till</span><span class="sxs-lookup"><span data-stu-id="43970-445">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="43970-446">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="43970-446">New cmdlets added:</span></span>
        - <span data-ttu-id="43970-447">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="43970-447">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="43970-448">Cmdletar har uppdaterats med den valfria parametern -UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="43970-448">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="43970-449">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="43970-449">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="43970-450">Lägg till stöd för resurser för NetworkWatcher ConnectionMonitor version 2</span><span class="sxs-lookup"><span data-stu-id="43970-450">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="43970-451">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="43970-451">Az.PolicyInsights</span></span>
* <span data-ttu-id="43970-452">Stöd för utvärdering av efterlevnad innan fastställande av vilken resurs som ska åtgärdas</span><span class="sxs-lookup"><span data-stu-id="43970-452">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="43970-453">Lägg till parametern ”-ResourceDiscoverMode” för Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="43970-453">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="43970-454">Lägg till cmdleten Get-AzPolicyMetadata för att hämta resurser för principmetadata</span><span class="sxs-lookup"><span data-stu-id="43970-454">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="43970-455">Get-AzPolicyState och Get-AzPolicyStateSummary för API-versionen 2019-10-01 har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="43970-455">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="43970-456">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="43970-456">Az.RecoveryServices</span></span>
* <span data-ttu-id="43970-457">Azure Site Recovery-stöd för att ta bort en replikerad disk.</span><span class="sxs-lookup"><span data-stu-id="43970-457">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="43970-458">Tillagt Azure Backup-stöd för att lägga till taggar när ett Recovery Services-valv skapas.</span><span class="sxs-lookup"><span data-stu-id="43970-458">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="43970-459">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="43970-459">Az.Resources</span></span>
* <span data-ttu-id="43970-460">Gör -Scope valfritt i cmdletarna \*-AzPolicyAssignment med standardinställning till kontextprenumeration</span><span class="sxs-lookup"><span data-stu-id="43970-460">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="43970-461">Lägg till exempel på att skapa ADServicePrincipal med lösenord och nyckelautentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="43970-461">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="43970-462">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="43970-462">Az.Sql</span></span>
<span data-ttu-id="43970-463">Åtgärda cmdleten New-AzSqlDatabaseSecondary så att existensen PartnerDatabaseName kontrolleras i stället för existensen DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="43970-463">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="43970-464">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="43970-464">Az.Storage</span></span>
* <span data-ttu-id="43970-465">Stöd för angivning av krypteringsnyckeltyp för Tabell/kö i Skapa lagringskonto</span><span class="sxs-lookup"><span data-stu-id="43970-465">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="43970-466">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="43970-466">New-AzStorageAccount</span></span>
* <span data-ttu-id="43970-467">Visa RequestId när StorageException inte har ExtendedErrorInformation</span><span class="sxs-lookup"><span data-stu-id="43970-467">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="43970-468">Åtgärda exempel 6 för cmdleten Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="43970-468">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="43970-469">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="43970-469">Az.Websites</span></span>
* <span data-ttu-id="43970-470">Set-AzWebapp och Set-AzWebappSlot stöder egenskaperna AlwaysOn, MinTls och FtpsState</span><span class="sxs-lookup"><span data-stu-id="43970-470">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="43970-471">Åtgärdar problemet där inställning av HttpsOnly samtidigt som AppservicePlan ändrades med det enskilda kommandot Set-AzWebApp återställde HttpsOnly till standardvärdet</span><span class="sxs-lookup"><span data-stu-id="43970-471">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="43970-472">3.3.0 – januari 2020</span><span class="sxs-lookup"><span data-stu-id="43970-472">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="43970-473">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="43970-473">Az.Accounts</span></span>
* <span data-ttu-id="43970-474">Nu stöder Add-AzEnvironment och Set-AzEnvironment parametrarna AzureAttestationServiceEndpointResourceId och AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="43970-474">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="43970-475">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="43970-475">Az.Cdn</span></span>
* <span data-ttu-id="43970-476">Information om felsvar visas i New-AzCdnEndpoint-cmdleten</span><span class="sxs-lookup"><span data-stu-id="43970-476">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="43970-477">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="43970-477">Az.Compute</span></span>
* <span data-ttu-id="43970-478">Set-AzVMCustomScriptExtension-cmdleten har åtgärdats för en virtuell dator med hanterad OD-disk som inte har någon operativsystemprofil.</span><span class="sxs-lookup"><span data-stu-id="43970-478">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="43970-479">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="43970-479">Az.ContainerInstance</span></span>
* <span data-ttu-id="43970-480">Parameternamn som används med New-AzContainerGroup-exempel har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="43970-480">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="43970-481">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="43970-481">Az.DataBoxEdge</span></span>
* <span data-ttu-id="43970-482">Cmdleten ”Get-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="43970-482">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="43970-483">Hämta gränslagringscontainern</span><span class="sxs-lookup"><span data-stu-id="43970-483">Get the Edge Storage Container</span></span>
* <span data-ttu-id="43970-484">Cmdleten ”New-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="43970-484">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="43970-485">Skapa en ny gränslagringscontainer</span><span class="sxs-lookup"><span data-stu-id="43970-485">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="43970-486">Cmdleten ”Remove-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="43970-486">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="43970-487">Ta bort gränslagringscontainern</span><span class="sxs-lookup"><span data-stu-id="43970-487">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="43970-488">Cmdleten ”Invoke-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="43970-488">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="43970-489">Anropa åtgärd för att uppdatera data i gränslagringscontainer</span><span class="sxs-lookup"><span data-stu-id="43970-489">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="43970-490">Cmdleten ”Get-AzDataBoxEdgeStorageAccount” har lagts till</span><span class="sxs-lookup"><span data-stu-id="43970-490">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="43970-491">Hämta gränslagringskontot</span><span class="sxs-lookup"><span data-stu-id="43970-491">Get the Edge Storage Account</span></span>
* <span data-ttu-id="43970-492">Cmdleten ”New-AzDataBoxEdgeStorageAccount” har lagts till</span><span class="sxs-lookup"><span data-stu-id="43970-492">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="43970-493">Skapa ett nytt gränslagringskonto</span><span class="sxs-lookup"><span data-stu-id="43970-493">Create new Edge Storage Account</span></span>
* <span data-ttu-id="43970-494">Cmdleten ”Remove-AzDataBoxEdgeStorageAccount” har lagts till</span><span class="sxs-lookup"><span data-stu-id="43970-494">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="43970-495">Ta bort gränslagringskontot</span><span class="sxs-lookup"><span data-stu-id="43970-495">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="43970-496">Anropa cmdleten ”Invoke-AzDataBoxEdgeShare”</span><span class="sxs-lookup"><span data-stu-id="43970-496">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="43970-497">Anropa åtgärd för att uppdatera resursdata</span><span class="sxs-lookup"><span data-stu-id="43970-497">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="43970-498">Cmdleten ”Set-AzDataBoxEdgeStorageAccountCredential” har lagts till</span><span class="sxs-lookup"><span data-stu-id="43970-498">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="43970-499">Ange autentiseringsuppgifter för az databoxedge-lagringskonto</span><span class="sxs-lookup"><span data-stu-id="43970-499">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="43970-500">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="43970-500">Az.DataFactory</span></span>
* <span data-ttu-id="43970-501">Lägg till AutoUpdateETA-, LatestVersion-, PushedVersion-, TaskQueueId- och VersionStatus-egenskaper för Get-AzDataFactoryV2IntegrationRuntime-cmd</span><span class="sxs-lookup"><span data-stu-id="43970-501">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="43970-502">Uppdatera ADF .Net SDK-versionen till 4.6.0</span><span class="sxs-lookup"><span data-stu-id="43970-502">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="43970-503">Lägg till parametern ”PublicIPs” för ”Set-AzureRmDataFactoryV2IntegrationRuntime”-cmd så att Azure-SSIS IR kan skapas med statiska offentliga IP-adresser.</span><span class="sxs-lookup"><span data-stu-id="43970-503">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="43970-504">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="43970-504">Az.DevTestLabs</span></span>
* <span data-ttu-id="43970-505">Ta bort den brutna länken i Get-AzDtlAllowedVMSizesPolicy.md</span><span class="sxs-lookup"><span data-stu-id="43970-505">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="43970-506">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="43970-506">Az.EventHub</span></span>
* <span data-ttu-id="43970-507">Korrigering av problem 10634: Åtgärda referensen till null-objekt för eventhubnamespace-borttagning</span><span class="sxs-lookup"><span data-stu-id="43970-507">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="43970-508">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="43970-508">Az.HDInsight</span></span>
* <span data-ttu-id="43970-509">Åtgärda Invoke-AzHDInsightHiveJob.md-fel.</span><span class="sxs-lookup"><span data-stu-id="43970-509">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="43970-510">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="43970-510">Az.MachineLearning</span></span>
* <span data-ttu-id="43970-511">Nedanstående cmdletar har tagits bort eftersom MachineLearningCompute inte längre är tillgängligt</span><span class="sxs-lookup"><span data-stu-id="43970-511">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="43970-512">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="43970-512">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="43970-513">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="43970-513">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="43970-514">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="43970-514">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="43970-515">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="43970-515">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="43970-516">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="43970-516">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="43970-517">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="43970-517">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="43970-518">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="43970-518">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="43970-519">Az.Network</span><span class="sxs-lookup"><span data-stu-id="43970-519">Az.Network</span></span>
* <span data-ttu-id="43970-520">Uppgradera beroende av Microsoft.Azure.Management.Sql från 1.36-preview till 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="43970-520">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="43970-521">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="43970-521">Az.RecoveryServices</span></span>
* <span data-ttu-id="43970-522">Ändrat Azure Site Recovery-stöd för krypterade vilande data på virtuella datorer med hanterade diskar med kundhanterade nycklar för Azure till Azure-providern.</span><span class="sxs-lookup"><span data-stu-id="43970-522">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="43970-523">Azure Site Recovery-stöd för att ange ID för diskkrypteringsuppsättning som valfri inmatning för aktivering av skydd för VMware till Azure.</span><span class="sxs-lookup"><span data-stu-id="43970-523">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="43970-524">Azure Site Recovery-stöd för att ange ID för diskkrypteringsuppsättning som valfri inmatning på disknivå för aktivering av skydd för VMware till Azure.</span><span class="sxs-lookup"><span data-stu-id="43970-524">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="43970-525">Azure Site Recovery-stöd för att uppdatera replikeringsskyddade objekt med mappning för diskkrypteringsuppsättning för HyperV till Azure.</span><span class="sxs-lookup"><span data-stu-id="43970-525">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="43970-526">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="43970-526">Az.Resources</span></span>
* <span data-ttu-id="43970-527">Åtgärda ett fel i hjälpdokument för ”Remove-AzTag”.</span><span class="sxs-lookup"><span data-stu-id="43970-527">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="43970-528">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="43970-528">Az.Sql</span></span>
* <span data-ttu-id="43970-529">Åtgärda funktioner i cmdletar för att ange baslinjen för sårbarhetsbedömning för arbete med huvuddatabasen för Azure-databasen och begränsa den för systemdatabaser på hanterade instanser.</span><span class="sxs-lookup"><span data-stu-id="43970-529">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="43970-530">Åtgärda ett fel när en redundansgrupp för en SQL-instans skapas</span><span class="sxs-lookup"><span data-stu-id="43970-530">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="43970-531">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="43970-531">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="43970-532">Lägg till DR som en ny giltig licenstyp</span><span class="sxs-lookup"><span data-stu-id="43970-532">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="43970-533">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="43970-533">Az.Storage</span></span>
* <span data-ttu-id="43970-534">Lägg till varningsmeddelande om icke-bakåtkompatibel ändring för DefaultAction-värdeändring i en framtida version</span><span class="sxs-lookup"><span data-stu-id="43970-534">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="43970-535">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="43970-535">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="43970-536">Stöd för att hämta lagringskontots senaste synkroniseringstid genom att köra get-AzureRMStorageAccount med parametern -IncludeGeoReplicationStats</span><span class="sxs-lookup"><span data-stu-id="43970-536">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="43970-537">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="43970-537">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="43970-538">3.2.0 – December 2019</span><span class="sxs-lookup"><span data-stu-id="43970-538">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="43970-539">Allmänt</span><span class="sxs-lookup"><span data-stu-id="43970-539">General</span></span>
* <span data-ttu-id="43970-540">Uppdatera referenser i .psd1 för att använda relativa sökvägar för alla moduler</span><span class="sxs-lookup"><span data-stu-id="43970-540">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="43970-541">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="43970-541">Az.Accounts</span></span>
* <span data-ttu-id="43970-542">Ange rätt UserAgent för telemetri på klientsidan för Az 4.0 preview</span><span class="sxs-lookup"><span data-stu-id="43970-542">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="43970-543">Visa användarvänligt felmeddelande när kontexten är null i Az 4.0 preview</span><span class="sxs-lookup"><span data-stu-id="43970-543">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="43970-544">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="43970-544">Az.Batch</span></span>
* <span data-ttu-id="43970-545">Korrigera problem [#10602](https://github.com/Azure/azure-powershell/issues/10602), där **New-AzBatchPool** skickade VirtualMachineConfiguration.ContainerConfiguration eller VirtualMachineConfiguration.DataDisks på ett felaktigt sätt till servern.</span><span class="sxs-lookup"><span data-stu-id="43970-545">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="43970-546">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="43970-546">Az.DataFactory</span></span>
* <span data-ttu-id="43970-547">Uppdatera ADF .Net SDK-versionen till 4.5.0</span><span class="sxs-lookup"><span data-stu-id="43970-547">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="43970-548">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="43970-548">Az.FrontDoor</span></span>
* <span data-ttu-id="43970-549">Stöd har lagts till för undantag för hanterade regler för brandväggen för webbaserade program</span><span class="sxs-lookup"><span data-stu-id="43970-549">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="43970-550">Lägg till SocketAddr för automatisk komplettering</span><span class="sxs-lookup"><span data-stu-id="43970-550">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="43970-551">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="43970-551">Az.HealthcareApis</span></span>
* <span data-ttu-id="43970-552">Undantagshantering</span><span class="sxs-lookup"><span data-stu-id="43970-552">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="43970-553">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="43970-553">Az.KeyVault</span></span>
* <span data-ttu-id="43970-554">Åtgärdat fel vid åtkomst av värde som kanske inte har angetts</span><span class="sxs-lookup"><span data-stu-id="43970-554">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="43970-555">Hantering av ECC-certifikat (Elliptic Curve Cryptography)</span><span class="sxs-lookup"><span data-stu-id="43970-555">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="43970-556">Stöd har lagts till för att ange kurvan för certifikatprinciper</span><span class="sxs-lookup"><span data-stu-id="43970-556">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="43970-557">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="43970-557">Az.Monitor</span></span>
* <span data-ttu-id="43970-558">Lägger till valfritt argument i kommandot Lägg till diagnostikinställningar.</span><span class="sxs-lookup"><span data-stu-id="43970-558">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="43970-559">Ett växelargument som om det finns visar att exporten till Log Analytics måste ske till ett fast schema (kallas även</span><span class="sxs-lookup"><span data-stu-id="43970-559">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="43970-560">dedikerad, datatyp)</span><span class="sxs-lookup"><span data-stu-id="43970-560">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="43970-561">Az.Network</span><span class="sxs-lookup"><span data-stu-id="43970-561">Az.Network</span></span>
* <span data-ttu-id="43970-562">Stöd för IpGroups i program-, NAT- och nätverksregler för Azure Firewall.</span><span class="sxs-lookup"><span data-stu-id="43970-562">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="43970-563">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="43970-563">Az.Resources</span></span>
* <span data-ttu-id="43970-564">Åtgärda ett problem där malldistributionen inte kan läsa en mallparameter om dess namn står i konflikt med ett inbyggt parameternamn.</span><span class="sxs-lookup"><span data-stu-id="43970-564">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="43970-565">Uppdaterade princip-cmdletar för att använda den nya API-versionen 2019-09-01 som introducerar grupperingsstöd inom principuppsättningsdefinitioner.</span><span class="sxs-lookup"><span data-stu-id="43970-565">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="43970-566">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="43970-566">Az.Sql</span></span>
* <span data-ttu-id="43970-567">Uppgraderad funktion för att skapa lagring i automatisk aktivering av sårbarhetsbedömning till StorageV2</span><span class="sxs-lookup"><span data-stu-id="43970-567">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="43970-568">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="43970-568">Az.Storage</span></span>
* <span data-ttu-id="43970-569">Stöd för generering av blob/container-identitetsbaserad SAS-token med lagringskontextbaserad på OAuth-autentisering</span><span class="sxs-lookup"><span data-stu-id="43970-569">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="43970-570">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="43970-570">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="43970-571">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="43970-571">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="43970-572">Stöd för återkallning av användardelegeringsnycklar för lagringskonto för att återkalla alla SAS-token</span><span class="sxs-lookup"><span data-stu-id="43970-572">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="43970-573">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="43970-573">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="43970-574">Uppgradera till Microsoft.Azure.Management.Storage 14.2.0 för att stödja den nya API-versionen 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="43970-574">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="43970-575">Stöd för QuotaGiB (resurskvot i Gibibye) för värden över 5120 i hanteringsplanet för cmdletar för filresurser och parameteraliaset. Quota har också lagts till för parametern ”QuotaGiB”.</span><span class="sxs-lookup"><span data-stu-id="43970-575">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="43970-576">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="43970-576">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="43970-577">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="43970-577">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="43970-578">Lägg till parameteraliaset QuotaGiB i parametern Quota</span><span class="sxs-lookup"><span data-stu-id="43970-578">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="43970-579">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="43970-579">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="43970-580">Åtgärda problemet att Set-AzStorageContainerAcl kan rensa den lagrade åtkomstprincipen</span><span class="sxs-lookup"><span data-stu-id="43970-580">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="43970-581">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="43970-581">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="43970-582">3.1.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="43970-582">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="43970-583">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="43970-583">Highlights since the last major release</span></span>
* <span data-ttu-id="43970-584">Az.DataBoxEdge 1.0.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="43970-584">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="43970-585">Az.SqlVirtualMachine 1.0.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="43970-585">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="43970-586">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="43970-586">Az.Compute</span></span>
* <span data-ttu-id="43970-587">Funktion för att använda en virtuell dator igen</span><span class="sxs-lookup"><span data-stu-id="43970-587">VM Reapply feature</span></span>
    - <span data-ttu-id="43970-588">Lägg till parameter för att använda igen till cmdleten Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="43970-588">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="43970-589">Funktionen AutomaticRepairs i VM-skalningsuppsättningar:</span><span class="sxs-lookup"><span data-stu-id="43970-589">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="43970-590">Lägg till parametrarna EnableAutomaticRepair, AutomaticRepairGracePeriod och AutomaticRepairMaxInstanceRepairsPercent till följande cmdletar:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="43970-590">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="43970-591">Stöd för galleriavbildningar i flera klientorganisationer för New-AzVM</span><span class="sxs-lookup"><span data-stu-id="43970-591">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="43970-592">Lägg till "Spot" till argumentslutföraren i prioritetsparametern i cmdletarna New-AzVM, New-AzVMConfig och New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="43970-592">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="43970-593">Lägg till parametrarna DiskIOPSReadWrite och DiskMBpsReadWrite till cmdleten Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="43970-593">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="43970-594">Ändra parametern SourceImageId för cmdleten New-AzGalleryImageVersion till valfri</span><span class="sxs-lookup"><span data-stu-id="43970-594">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="43970-595">Lägg till parametrarna OSDiskImage och DataDiskImage till cmdleten New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="43970-595">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="43970-596">Lägg till parametern HyperVGeneration till cmdleten New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="43970-596">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="43970-597">Lägg till parametern SkipExtensionsOnOverprovisionedVMs till cmdletarna New-AzVmss, New-AzVmssConfig och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="43970-597">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="43970-598">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="43970-598">Az.DataBoxEdge</span></span>
* <span data-ttu-id="43970-599">Cmdleten `Get-AzDataBoxEdgeOrder` har lagts till</span><span class="sxs-lookup"><span data-stu-id="43970-599">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="43970-600">Hämta ordning</span><span class="sxs-lookup"><span data-stu-id="43970-600">Get the Order</span></span>
* <span data-ttu-id="43970-601">Cmdleten `New-AzDataBoxEdgeOrder` har lagts till</span><span class="sxs-lookup"><span data-stu-id="43970-601">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="43970-602">Skapa ny ordning</span><span class="sxs-lookup"><span data-stu-id="43970-602">Create new Order</span></span>
* <span data-ttu-id="43970-603">Cmdleten `Remove-AzDataBoxEdgeOrder` har lagts till</span><span class="sxs-lookup"><span data-stu-id="43970-603">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="43970-604">Ta bort ordning</span><span class="sxs-lookup"><span data-stu-id="43970-604">Remove the Order</span></span>
* <span data-ttu-id="43970-605">Cmdleten `New-AzDataBoxEdgeShare` har ändrats</span><span class="sxs-lookup"><span data-stu-id="43970-605">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="43970-606">Nu skapas lokal filresurs</span><span class="sxs-lookup"><span data-stu-id="43970-606">Now creates Local Share</span></span>
* <span data-ttu-id="43970-607">Cmdleten `Set-AzDataBoxEdgeRole` har lagts till</span><span class="sxs-lookup"><span data-stu-id="43970-607">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="43970-608">Nu kan IotRole mappas till filresursen</span><span class="sxs-lookup"><span data-stu-id="43970-608">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="43970-609">Cmdleten `Invoke-AzDataBoxEdgeDevice` har lagts till</span><span class="sxs-lookup"><span data-stu-id="43970-609">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="43970-610">Anropa genomsökningsuppdatering, ladda ned uppdatering, installera uppdateringar på enheten</span><span class="sxs-lookup"><span data-stu-id="43970-610">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="43970-611">Cmdleten `Get-AzDataBoxEdgeTrigger` har lagts till</span><span class="sxs-lookup"><span data-stu-id="43970-611">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="43970-612">Hämtar information om utlösare</span><span class="sxs-lookup"><span data-stu-id="43970-612">Gets the information about Triggers</span></span>
* <span data-ttu-id="43970-613">Cmdleten `New-AzDataBoxEdgeTrigger` har lagts till</span><span class="sxs-lookup"><span data-stu-id="43970-613">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="43970-614">Skapa nya utlösare</span><span class="sxs-lookup"><span data-stu-id="43970-614">Create new Triggers</span></span>
* <span data-ttu-id="43970-615">Cmdleten `Remove-AzDataBoxEdgeTrigger` har lagts till</span><span class="sxs-lookup"><span data-stu-id="43970-615">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="43970-616">Ta bort utlösare</span><span class="sxs-lookup"><span data-stu-id="43970-616">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="43970-617">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="43970-617">Az.DataFactory</span></span>
* <span data-ttu-id="43970-618">Uppdatera ADF .Net SDK-versionen till 4.4.0</span><span class="sxs-lookup"><span data-stu-id="43970-618">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="43970-619">Lägg till parametern ExpressCustomSetup för kommandot Set-AzureRmDataFactoryV2IntegrationRuntime för att aktivera installationskonfigurationer och komponenter från tredje part utan anpassat konfigurationsskript.</span><span class="sxs-lookup"><span data-stu-id="43970-619">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="43970-620">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="43970-620">Az.DataLakeStore</span></span>
* <span data-ttu-id="43970-621">Uppdatera dokumentation för Get-AzDataLakeStoreDeletedItem och Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="43970-621">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="43970-622">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="43970-622">Az.EventHub</span></span>
* <span data-ttu-id="43970-623">Korrigering av problem #10301: Korrigera datumformat för SAS-token</span><span class="sxs-lookup"><span data-stu-id="43970-623">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="43970-624">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="43970-624">Az.FrontDoor</span></span>
* <span data-ttu-id="43970-625">Lägg till parametern MinimumTlsVersion till Enable-AzFrontDoorCustomDomainHttps och New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="43970-625">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="43970-626">Lägg till parametrarna HealthProbeMethod och EnabledState till New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="43970-626">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="43970-627">Lägg till en ny cmdlet för att skapa BackendPoolsSettings-objekt som passar i skapande/uppdatering av Front Door</span><span class="sxs-lookup"><span data-stu-id="43970-627">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="43970-628">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="43970-628">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="43970-629">Az.Network</span><span class="sxs-lookup"><span data-stu-id="43970-629">Az.Network</span></span>
* <span data-ttu-id="43970-630">Ändra alternativexemplen Start-AzVirtualNetworkGatewayConnectionPacketCapture.md och Start-AzVirtualnetworkGatewayPacketCapture.md för FilterData.</span><span class="sxs-lookup"><span data-stu-id="43970-630">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="43970-631">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="43970-631">Az.PrivateDns</span></span>
* <span data-ttu-id="43970-632">Uppdaterade PrivateDns .NET SDK till version 1.0.0</span><span class="sxs-lookup"><span data-stu-id="43970-632">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="43970-633">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="43970-633">Az.RecoveryServices</span></span>
* <span data-ttu-id="43970-634">Stöd för att välja disktyp vid aktivering av skydd i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="43970-634">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="43970-635">Korrigering av bugg för åtgärdsredigering av återställningsplan i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="43970-635">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="43970-636">Återställningsstöd för att godkänna filestream-databaser i Azure Backup SQL.</span><span class="sxs-lookup"><span data-stu-id="43970-636">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="43970-637">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="43970-637">Az.RedisCache</span></span>
* <span data-ttu-id="43970-638">Parametern MinimumTlsVersion har lagts till i cmdletarna New-AzRedisCache och Set-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="43970-638">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="43970-639">Dessutom har MinimumTlsVersion lagts till i utdata för cmdleten Get-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="43970-639">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="43970-640">Verifiering har lagts till på parametern -Size i cmdletarna Set-AzRedisCache och New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="43970-640">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="43970-641">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="43970-641">Az.Resources</span></span>
- <span data-ttu-id="43970-642">Uppdaterade policy-cmdletar för att använda den nya API-versionen 2019-06-01 som har en ny EnforcementMode-egenskap i policytilldelningen.</span><span class="sxs-lookup"><span data-stu-id="43970-642">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="43970-643">Uppdaterade hjälpexempel för skapandet av policydefinition</span><span class="sxs-lookup"><span data-stu-id="43970-643">Updated create policy definition help example</span></span>
- <span data-ttu-id="43970-644">Åtgärda bugg i Remove-AZADServicePrincipal -ServicePrincipalName, utlös null-referens när tjänstens huvudnamn inte hittas.</span><span class="sxs-lookup"><span data-stu-id="43970-644">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="43970-645">Åtgärda bugg i New-AZADServicePrincipal, utlös null-referens när klientorganisationen inte har någon prenumeration.</span><span class="sxs-lookup"><span data-stu-id="43970-645">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="43970-646">Ändra New-AzAdServicePrincipal för att endast lägga till autentiseringsuppgifter för det associerade programmet.</span><span class="sxs-lookup"><span data-stu-id="43970-646">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="43970-647">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="43970-647">Az.Sql</span></span>
* <span data-ttu-id="43970-648">Stöd har lagts till för databasen ReadReplicaCount.</span><span class="sxs-lookup"><span data-stu-id="43970-648">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="43970-649">Korrigerade Set-AzSqlDatabase när zonredundans inte har angetts</span><span class="sxs-lookup"><span data-stu-id="43970-649">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="43970-650">3.0.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="43970-650">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="43970-651">Allmänt</span><span class="sxs-lookup"><span data-stu-id="43970-651">General</span></span>
* <span data-ttu-id="43970-652">Az. PrivateDns 1.0.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="43970-652">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="43970-653">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="43970-653">Az.Accounts</span></span>
* <span data-ttu-id="43970-654">Lägg till ett utfasningsmeddelande för aliaset Resolve-error.</span><span class="sxs-lookup"><span data-stu-id="43970-654">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="43970-655">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="43970-655">Az.Advisor</span></span>
* <span data-ttu-id="43970-656">Den nya kategorin Operational Excellence har lagts till i cmdleten Get-AzAdvisorRecommendation.</span><span class="sxs-lookup"><span data-stu-id="43970-656">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="43970-657">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="43970-657">Az.Batch</span></span>
* <span data-ttu-id="43970-658">`CoreQuota` på `BatchAccountContext` har bytt namn till `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="43970-658">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="43970-659">Det finns även en ny `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="43970-659">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="43970-660">Detta påverkar **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="43970-660">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="43970-661">**New-AzBatchTask** `-ResourceFile`-parametern tar nu en samling `PSResourceFile`-objekt som kan skapas med hjälp av den nya cmdleten **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="43970-661">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="43970-662">Ny **New-AzBatchResourceFile**-cmdlet för att skapa `PSResourceFile`-objekt.</span><span class="sxs-lookup"><span data-stu-id="43970-662">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="43970-663">Dessa kan tillhandahållas till **New-AzBatchTask** på `-ResourceFile`-parametern.</span><span class="sxs-lookup"><span data-stu-id="43970-663">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="43970-664">Detta stöder två nya typer av resursfiler förutom det befintliga sättet med `HttpUrl`:</span><span class="sxs-lookup"><span data-stu-id="43970-664">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="43970-665">`AutoStorageContainerName`-baserade resursfiler laddar ned en hel container för automatisk lagring till Batch-noden.</span><span class="sxs-lookup"><span data-stu-id="43970-665">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="43970-666">`StorageContainerUrl`-baserade resursfiler laddar ned containern som anges i webbadressen till Batch-noden.</span><span class="sxs-lookup"><span data-stu-id="43970-666">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="43970-667">Tog bort egenskapen `ApplicationPackages` för `PSApplication` som returnerades av **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="43970-667">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="43970-668">Specifika paket i ett program kan nu hämtas med hjälp av **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="43970-668">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="43970-669">Till exempel: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="43970-669">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="43970-670">Bytt namn på `ApplicationId` till `ApplicationName` på **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** och **Set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="43970-670">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="43970-671">`ApplicationId` är nu ett alias för `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="43970-671">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="43970-672">Ny `PSWindowsUserConfiguration`-egenskap till `PSUserAccount` lades till.</span><span class="sxs-lookup"><span data-stu-id="43970-672">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="43970-673">Bytte namn på `Version` till `Name` på `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="43970-673">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="43970-674">Bytte namn på `BlobSource` till `HttpUrl` på `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="43970-674">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="43970-675">Tog bort egenskapen `OSDisk` från `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="43970-675">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="43970-676">Tog bort **Set-AzBatchPoolOSVersion**.</span><span class="sxs-lookup"><span data-stu-id="43970-676">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="43970-677">Den här åtgärden stöds inte längre.</span><span class="sxs-lookup"><span data-stu-id="43970-677">This operation is no longer supported.</span></span>
* <span data-ttu-id="43970-678">`TargetOSVersion` har tagits bort från `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="43970-678">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="43970-679">Bytte namn på `CurrentOSVersion` till `OSVersion` på `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="43970-679">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="43970-680">`DataEgressGiB` och `DataIngressGiB` har tagits bort från `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="43970-680">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="43970-681">Tog bort **Get-AzBatchNodeAgentSku** och ersatte det med **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="43970-681">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="43970-682">**Get-AzBatchSupportedImage** returnerar samma data som **Get-AzBatchNodeAgentSku** men i ett mer användarvänligt format.</span><span class="sxs-lookup"><span data-stu-id="43970-682">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="43970-683">Nya icke-verifierade avbildningar returneras nu också.</span><span class="sxs-lookup"><span data-stu-id="43970-683">New non-verified images are also now returned.</span></span> <span data-ttu-id="43970-684">Ytterligare information om `Capabilities` och `BatchSupportEndOfLife` för varje avbildning inkluderas också.</span><span class="sxs-lookup"><span data-stu-id="43970-684">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="43970-685">Lade till möjlighet att montera fjärrfilsystem på varje nod i en pool via den nya parametern `MountConfiguration` för **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="43970-685">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="43970-686">Har nu stöd för nätverkssäkerhetsregler som blockerar nätverksåtkomst till en pool baserat på källportens trafik.</span><span class="sxs-lookup"><span data-stu-id="43970-686">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="43970-687">Detta görs via egenskapen `SourcePortRanges` på `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="43970-687">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="43970-688">När du kör en container stöder nu Batch körningen av uppgiften i arbetskatalogen för containern eller i arbetskatalogen för Batch-uppgiften.</span><span class="sxs-lookup"><span data-stu-id="43970-688">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="43970-689">Detta styrs av egenskapen `WorkingDirectory` på `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="43970-689">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="43970-690">Lade till en funktion för att ange en samling av offentliga IP-adresser på `PSNetworkConfiguration` via den nya egenskapen `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="43970-690">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="43970-691">Detta garanterar att noderna i poolen har en IP-adress från listan över IP-adresser som tillhandahållits av användare.</span><span class="sxs-lookup"><span data-stu-id="43970-691">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="43970-692">Om inget värde anges är standardvärdet för `WaitForSuccess` på `PSSTartTask` nu `$True` (var tidigare `$False`).</span><span class="sxs-lookup"><span data-stu-id="43970-692">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="43970-693">Om inget värde anges är standardvärdet för `Scope` på `PSAutoUserSpecification` nu `Pool` (var tidigare `Task` på Windows och `Pool` på Linux).</span><span class="sxs-lookup"><span data-stu-id="43970-693">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="43970-694">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="43970-694">Az.Cdn</span></span>
* <span data-ttu-id="43970-695">Introducerade UrlRewriteAction och CacheKeyQueryStringAction till RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="43970-695">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="43970-696">Åtgärdade flera buggar, som saknade indata för ”väljare” i cmdleten New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="43970-696">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="43970-697">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="43970-697">Az.Compute</span></span>
* <span data-ttu-id="43970-698">Funktion för diskkrypteringsuppsättning</span><span class="sxs-lookup"><span data-stu-id="43970-698">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="43970-699">Nya cmdletar:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="43970-699">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="43970-700">Parametern DiskEncryptionSetId har lagts till i följande cmdletar:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="43970-700">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="43970-701">Parametrarna DiskEncryptionSetId och EncryptionType har lagts till i följande cmdletar:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="43970-701">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="43970-702">Lägg till parametern PublicIPAddressVersion i New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="43970-702">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="43970-703">Flytta FileUris för anpassat skripttillägg från offentlig inställning till skyddad inställning</span><span class="sxs-lookup"><span data-stu-id="43970-703">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="43970-704">Lägg till ScaleInPolicy i cmdletarna New-AzVmss, New-AzVmssConfig och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="43970-704">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="43970-705">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="43970-705">Breaking changes</span></span>
    - <span data-ttu-id="43970-706">Parametern UploadSizeInBytes används istället för DiskSizeGB för New-AzDiskConfig när CreateOption är Uppladdning</span><span class="sxs-lookup"><span data-stu-id="43970-706">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="43970-707">PublishingProfile.Source.ManagedImage.Id ersätts med StorageProfile.Source.Id i objektet GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="43970-707">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="43970-708">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="43970-708">Az.DataFactory</span></span>
* <span data-ttu-id="43970-709">Uppdatera ADF .Net SDK-versionen till 4.3.0</span><span class="sxs-lookup"><span data-stu-id="43970-709">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="43970-710">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="43970-710">Az.DataLakeStore</span></span>
* <span data-ttu-id="43970-711">Uppdatera ADLS SDK-version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) innehåller följande korrigeringar</span><span class="sxs-lookup"><span data-stu-id="43970-711">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="43970-712">Undvik att utlösa undantag när det inte går att deserialisera creationtime för inmatning av papperskorg eller katalog.</span><span class="sxs-lookup"><span data-stu-id="43970-712">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="43970-713">Gör inställning tillgänglig per tidsgräns för förfrågan i adlsclient</span><span class="sxs-lookup"><span data-stu-id="43970-713">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="43970-714">Korrigera överföringen av ursprunglig syncflag för badoffset-återställning</span><span class="sxs-lookup"><span data-stu-id="43970-714">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="43970-715">Korrigera EnumerateDirectory för att hämta fortsättningstoken när svar har kontrollerats</span><span class="sxs-lookup"><span data-stu-id="43970-715">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="43970-716">Korrigera bugg i Concat</span><span class="sxs-lookup"><span data-stu-id="43970-716">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="43970-717">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="43970-717">Az.FrontDoor</span></span>
* <span data-ttu-id="43970-718">Åtgärdade diverse stavfel i modul</span><span class="sxs-lookup"><span data-stu-id="43970-718">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="43970-719">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="43970-719">Az.HDInsight</span></span>
* <span data-ttu-id="43970-720">Korrigerade buggen att kunder får felet ”inte en giltig Base-64-sträng” vid användning av Get-AzHDInsightCluster för att hämta klustret med ADLSGen1-lagring.</span><span class="sxs-lookup"><span data-stu-id="43970-720">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="43970-721">Lägg till en parameter med namnet ”ApplicationId” i de tre cmdletarna Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig och New-AzHDInsightCluster så att kunden kan tillhandahålla tjänstens huvudnamn för program-ID för åtkomst till Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="43970-721">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="43970-722">Ändrade Microsoft.Azure.Management.HDInsight från 2.1.0 till 5.1.0</span><span class="sxs-lookup"><span data-stu-id="43970-722">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="43970-723">Fem cmdletar har tagits bort:</span><span class="sxs-lookup"><span data-stu-id="43970-723">Removed five cmdlets:</span></span>
    - <span data-ttu-id="43970-724">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="43970-724">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="43970-725">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="43970-725">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="43970-726">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="43970-726">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="43970-727">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="43970-727">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="43970-728">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="43970-728">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="43970-729">Tre cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="43970-729">Added three cmdlets:</span></span>
    - <span data-ttu-id="43970-730">Get-AzHDInsightMonitoring som ersätter Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="43970-730">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="43970-731">Enable-AzHDInsightMonitoring som ersätter Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="43970-731">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="43970-732">Disable-AzHDInsightMonitoring som ersätter Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="43970-732">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="43970-733">Korrigerade cmdleten Get-AzHDInsightProperties för att stödja hämtning av funktionsinformation från en viss plats.</span><span class="sxs-lookup"><span data-stu-id="43970-733">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="43970-734">Parameteruppsättningarna (Spark1 och Spark2) har tagits bort från Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="43970-734">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="43970-735">Lägg till exempel för cmdleten Add-AzHDInsightSecurityProfile till hjälpdokumenten.</span><span class="sxs-lookup"><span data-stu-id="43970-735">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="43970-736">Ändrade utdatatyp för följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="43970-736">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="43970-737">Ändrade utdatatyp för Get-AzHDInsightProperties från CapabilitiesResponse till AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="43970-737">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="43970-738">Ändrade utdatatyp för Remove-AzHDInsightCluster från ClusterGetResponse till bool.</span><span class="sxs-lookup"><span data-stu-id="43970-738">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="43970-739">Ändrade utdatatyp för Set-AzHDInsightGatewaySettings HttpConnectivitySettings till GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="43970-739">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="43970-740">Lade till testfall för vissa scenarier.</span><span class="sxs-lookup"><span data-stu-id="43970-740">Added some scenario test cases.</span></span>
* <span data-ttu-id="43970-741">Ta bort vissa alias: Add-AzHDInsightConfigValues, Get-AzHDInsightProperties.</span><span class="sxs-lookup"><span data-stu-id="43970-741">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="43970-742">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="43970-742">Az.IotHub</span></span>
* <span data-ttu-id="43970-743">Icke-bakåtkompatibla ändringar:</span><span class="sxs-lookup"><span data-stu-id="43970-743">Breaking changes:</span></span>
    - <span data-ttu-id="43970-744">Cmdleten Add-AzIotHubEventHubConsumerGroup har inte längre stöd för parametern EventHubEndpointName och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="43970-744">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="43970-745">Parameteruppsättningen __AllParameterSets för cmdleten Add-AzIotHubEventHubConsumerGroup har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="43970-745">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="43970-746">Cmdleten Get-AzIotHubEventHubConsumerGroup har inte längre stöd för parametern EventHubEndpointName och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="43970-746">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="43970-747">Parameteruppsättningen __AllParameterSets för cmdleten Get-AzIotHubEventHubConsumerGroup har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="43970-747">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="43970-748">Egenskapen OperationsMonitoringProperties av typen Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="43970-748">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="43970-749">Egenskapen OperationsMonitoringProperties av typen Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="43970-749">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="43970-750">Cmdleten New-AzIotHubExportDevice stöder inte längre aliaset New-AzIotHubExportDevices.</span><span class="sxs-lookup"><span data-stu-id="43970-750">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="43970-751">Cmdleten New-AzIotHubImportDevice stöder inte längre aliaset New-AzIotHubImportDevices.</span><span class="sxs-lookup"><span data-stu-id="43970-751">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="43970-752">Cmdleten Remove-AzIotHubEventHubConsumerGroup har inte längre stöd för parametern EventHubEndpointName och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="43970-752">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="43970-753">Parameteruppsättningen __AllParameterSets för cmdleten Remove-AzIotHubEventHubConsumerGroup har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="43970-753">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="43970-754">Cmdleten Set-AzIotHub har inte längre stöd för parametern OperationsMonitoringProperties och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="43970-754">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="43970-755">Parameteruppsättningen UpdateOperationsMonitoringProperties för cmdleten Set-AzIotHub har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="43970-755">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="43970-756">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="43970-756">Az.RecoveryServices</span></span>
* <span data-ttu-id="43970-757">Azure Site Recovery-stöd för att konfigurera nätverksresurser som NSG, offentliga IP-adresser och interna lastbalanserare för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="43970-757">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="43970-758">Azure Site Recovery-stöd för att skriva till hanterad disk för vMWare till Azure.</span><span class="sxs-lookup"><span data-stu-id="43970-758">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="43970-759">Azure Site Recovery-stöd för NIC-reduktion för vMWare till Azure.</span><span class="sxs-lookup"><span data-stu-id="43970-759">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="43970-760">Azure Site Recovery-stöd för accelererat nätverk för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="43970-760">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="43970-761">Azure Site Recovery-stöd för automatisk uppdatering av agent för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="43970-761">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="43970-762">Azure Site Recovery-stöd för Standard SSD för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="43970-762">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="43970-763">Azure Site Recovery-stöd för tvåstegskryptering i Azure Disk Encryption för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="43970-763">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="43970-764">Azure Site Recovery-stöd för att skydda nyligen tillagda diskar för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="43970-764">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="43970-765">En funktion för mjuk borttagning av virtuella datorer samt tester för mjuk borttagning har tagits bort</span><span class="sxs-lookup"><span data-stu-id="43970-765">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="43970-766">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="43970-766">Az.Resources</span></span>
* <span data-ttu-id="43970-767">Uppdatera beroendesammansättning för Microsoft.Extensions.Caching.Memory från 1.1.1 till 2.2</span><span class="sxs-lookup"><span data-stu-id="43970-767">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="43970-768">Az.Network</span><span class="sxs-lookup"><span data-stu-id="43970-768">Az.Network</span></span>
* <span data-ttu-id="43970-769">Ändra alla cmdletar för PrivateEndpointConnection så att de stöder generiska tjänstleverantörer.</span><span class="sxs-lookup"><span data-stu-id="43970-769">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="43970-770">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="43970-770">Updated cmdlet:</span></span>
        - <span data-ttu-id="43970-771">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="43970-771">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="43970-772">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="43970-772">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="43970-773">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="43970-773">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="43970-774">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="43970-774">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="43970-775">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="43970-775">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="43970-776">Lägg till ny cmdlet för PrivateLinkResource så att det också stöder generiska tjänstleverantörer.</span><span class="sxs-lookup"><span data-stu-id="43970-776">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="43970-777">Ny cmdlet:</span><span class="sxs-lookup"><span data-stu-id="43970-777">New cmdlet:</span></span>
        - <span data-ttu-id="43970-778">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="43970-778">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="43970-779">Lägg till nya fält och parametrar för funktionen Proxy Protocol V2.</span><span class="sxs-lookup"><span data-stu-id="43970-779">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="43970-780">Lägg till egenskapen EnableProxyProtocol i PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="43970-780">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="43970-781">Lägg till egenskapen LinkIdentifier i PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="43970-781">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="43970-782">Uppdaterade New-AzPrivateLinkService för att lägga till den nya valfria parametern EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="43970-782">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="43970-783">Korrigera felaktig beskrivning av parameter i referensdokumentationen för New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="43970-783">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="43970-784">Nya cmdletar som stöder Azure-brandväggsprincipen</span><span class="sxs-lookup"><span data-stu-id="43970-784">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="43970-785">Lägg till stöd för den underordnade resursen RouteTables för VirtualHub</span><span class="sxs-lookup"><span data-stu-id="43970-785">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="43970-786">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="43970-786">New cmdlets added:</span></span>
        - <span data-ttu-id="43970-787">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="43970-787">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="43970-788">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="43970-788">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="43970-789">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="43970-789">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="43970-790">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="43970-790">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="43970-791">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="43970-791">Set-AzVirtualHub</span></span>
* <span data-ttu-id="43970-792">Lägg till stöd för ny egenskaps-SKU för VirtualHub och VirtualWANType för VirtualWan</span><span class="sxs-lookup"><span data-stu-id="43970-792">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="43970-793">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="43970-793">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="43970-794">New-AzVirtualHub: lade till parameter-SKU</span><span class="sxs-lookup"><span data-stu-id="43970-794">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="43970-795">Update-AzVirtualHub: lade till parameter-SKU</span><span class="sxs-lookup"><span data-stu-id="43970-795">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="43970-796">New-AzVirtualWan: lade till parametern VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="43970-796">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="43970-797">Update-AzVirtualWan: lade till parametern VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="43970-797">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="43970-798">Lägg till stöd för egenskapen EnableInternetSecurity för HubVnetConnection, VpnConnection och ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="43970-798">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="43970-799">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="43970-799">New cmdlets added:</span></span>
        - <span data-ttu-id="43970-800">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="43970-800">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="43970-801">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="43970-801">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="43970-802">New-AzureRmVirtualHubVnetConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="43970-802">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="43970-803">New-AzureRmVpnConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="43970-803">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="43970-804">Update-AzureRmVpnConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="43970-804">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="43970-805">New-AzureRmExpressRouteConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="43970-805">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="43970-806">Set-AzureRmExpressRouteConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="43970-806">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="43970-807">Lägg till stöd för att konfigurera TopLevel WebApplicationFirewall-princip</span><span class="sxs-lookup"><span data-stu-id="43970-807">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="43970-808">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="43970-808">New cmdlets added:</span></span>
        - <span data-ttu-id="43970-809">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="43970-809">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="43970-810">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="43970-810">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="43970-811">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="43970-811">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="43970-812">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="43970-812">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="43970-813">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="43970-813">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="43970-814">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="43970-814">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="43970-815">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="43970-815">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="43970-816">New-AzApplicationGatewayFirewallPolicy: parametrarna PolicySetting, ManagedRule har lagts till</span><span class="sxs-lookup"><span data-stu-id="43970-816">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="43970-817">Stöd för operator för geomatchning har lagts till på CustomRule</span><span class="sxs-lookup"><span data-stu-id="43970-817">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="43970-818">Geomatchning har lagts till i operatorn på FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="43970-818">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="43970-819">Stöd har lagts till för brandväggsprinciperna perListener och perSite</span><span class="sxs-lookup"><span data-stu-id="43970-819">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="43970-820">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="43970-820">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="43970-821">New-AzApplicationGatewayHttpListener: parametrarna FirewallPolicy, FirewallPolicyId har lagts till</span><span class="sxs-lookup"><span data-stu-id="43970-821">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="43970-822">New-AzApplicationGatewayPathRuleConfig: parametrarna FirewallPolicy, FirewallPolicyId har lagts till</span><span class="sxs-lookup"><span data-stu-id="43970-822">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="43970-823">Åtgärdat så att nödvändigt undernät med namnet AzureBastionSubnet i PSBastion kan vara skiftlägesokänsligt</span><span class="sxs-lookup"><span data-stu-id="43970-823">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="43970-824">Stöd för mål-FQDN:er i nätverksregler och översatt FQDN i NAT-regler för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="43970-824">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="43970-825">Lägg till stöd för resursen RouteTables för IpGroup på den högsta nivån</span><span class="sxs-lookup"><span data-stu-id="43970-825">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="43970-826">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="43970-826">New cmdlets added:</span></span>
        - <span data-ttu-id="43970-827">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="43970-827">New-AzIpGroup</span></span>
        - <span data-ttu-id="43970-828">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="43970-828">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="43970-829">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="43970-829">Get-AzIpGroup</span></span>
        - <span data-ttu-id="43970-830">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="43970-830">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="43970-831">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="43970-831">Az.ServiceFabric</span></span>
* <span data-ttu-id="43970-832">Ta bort cmdleten Add-AzServiceFabricApplicationCertificate eftersom det här scenariot omfattas av Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="43970-832">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="43970-833">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="43970-833">Az.Sql</span></span>
* <span data-ttu-id="43970-834">Stöd har lagts till för återställning av utelämnade databaser på hanterade instanser.</span><span class="sxs-lookup"><span data-stu-id="43970-834">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="43970-835">Inaktuella gamla cmdletar för granskning från kod.</span><span class="sxs-lookup"><span data-stu-id="43970-835">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="43970-836">Tog bort inaktuella alias:</span><span class="sxs-lookup"><span data-stu-id="43970-836">Removed deprecated aliases:</span></span>
* <span data-ttu-id="43970-837">Get-AzSqlDatabaseIndexRecommendations (använd Get-AzSqlDatabaseIndexRecommendation istället)</span><span class="sxs-lookup"><span data-stu-id="43970-837">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="43970-838">Get-AzSqlDatabaseRestorePoints (använd Get-AzSqlDatabaseRestorePoint istället)</span><span class="sxs-lookup"><span data-stu-id="43970-838">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="43970-839">Ta bort cmdleten Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="43970-839">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="43970-840">Ta bort alias för inaktuella cmdletar för inställningar för utvärdering av säkerhetsrisk</span><span class="sxs-lookup"><span data-stu-id="43970-840">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="43970-841">Inaktualisera cmdletar för inställningar för avancerad hotidentifiering</span><span class="sxs-lookup"><span data-stu-id="43970-841">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="43970-842">Lägga till cmdletar för att inaktivera och aktivera känslighetsrekommendationer på kolumner i en databas.</span><span class="sxs-lookup"><span data-stu-id="43970-842">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="43970-843">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="43970-843">Az.Storage</span></span>
* <span data-ttu-id="43970-844">Stöd för att aktivera stora filresurser vid skapande eller uppdatering av lagringskonto</span><span class="sxs-lookup"><span data-stu-id="43970-844">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="43970-845">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="43970-845">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="43970-846">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="43970-846">Set-AzStorageAccount</span></span>
* <span data-ttu-id="43970-847">När du stänger/hämtar en filreferens kan du hoppa över kontrollen av huruvida indatasökvägen är en filkatalog eller en fil för att undvika problem med objekt som har status DeletePending</span><span class="sxs-lookup"><span data-stu-id="43970-847">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="43970-848">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="43970-848">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="43970-849">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="43970-849">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="43970-850">2.8.0 – oktober 2019</span><span class="sxs-lookup"><span data-stu-id="43970-850">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="43970-851">Allmänt</span><span class="sxs-lookup"><span data-stu-id="43970-851">General</span></span>
* <span data-ttu-id="43970-852">AZ. HealthcareApis 1.0.0-version</span><span class="sxs-lookup"><span data-stu-id="43970-852">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="43970-853">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="43970-853">Az.Accounts</span></span>
* <span data-ttu-id="43970-854">Uppdatera telemetri och URL-omskrivning för genererade moduler, korrigera Windows-enhetstester.</span><span class="sxs-lookup"><span data-stu-id="43970-854">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="43970-855">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="43970-855">Az.ApiManagement</span></span>
* <span data-ttu-id="43970-856">**Set-AzApiManagementApi** – Tillagt stöd för att uppdatera Api till ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="43970-856">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="43970-857">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="43970-857">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="43970-858">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="43970-858">Az.Automation</span></span>
* <span data-ttu-id="43970-859">Åtgärdade cmdleten New-AzureAutomationSoftwareUpdateConfiguration för parametern för inställning av Linux-omstart.</span><span class="sxs-lookup"><span data-stu-id="43970-859">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="43970-860">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="43970-860">Az.Batch</span></span>
* <span data-ttu-id="43970-861">**Get-AzBatchNodeAgentSku** är inaktuell och ersätts av **Get-AzBatchSupportImage** i version 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="43970-861">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="43970-862">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="43970-862">Az.Compute</span></span>
* <span data-ttu-id="43970-863">Lägg till parametrarna Priority, EvictionPolicy och MaxPrice till cmdletarna New-AzVM och New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="43970-863">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="43970-864">Korrigera varningsmeddelande och hjälpdokument för cmdletarna Add-AzVMAdditionalUnattendContent och Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="43970-864">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="43970-865">Åtgärda – skipVmBackup-undantag för virtuella Linux-datorer med hanterade diskar för Set-AzVMDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="43970-865">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="43970-866">Åtgärda fel i uppdatera krypteringsinställningarna i set-AzVMDiskEncryptionExtension, scenario i två steg.</span><span class="sxs-lookup"><span data-stu-id="43970-866">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="43970-867">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="43970-867">Az.DataFactory</span></span>
* <span data-ttu-id="43970-868">Lägga till CRUD-kommandon för ADF V2-dataflödet: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow och Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="43970-868">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="43970-869">Lägger till åtgärdskommandon för ADF V2-dataflödesfelsökningssession: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand och Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="43970-869">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="43970-870">Uppdatera ADF .Net SDK-versionen till 4.2.0</span><span class="sxs-lookup"><span data-stu-id="43970-870">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="43970-871">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="43970-871">Az.DataLakeStore</span></span>
* <span data-ttu-id="43970-872">Korrigera kontovalidering så att konton med ”-” kan skickas utan domän</span><span class="sxs-lookup"><span data-stu-id="43970-872">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="43970-873">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="43970-873">Az.HealthcareApis</span></span>
* <span data-ttu-id="43970-874">PowerShell-versionen har uppdaterats till 1.0.0</span><span class="sxs-lookup"><span data-stu-id="43970-874">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="43970-875">Uppdaterade SDK-versionen till 1.0.2</span><span class="sxs-lookup"><span data-stu-id="43970-875">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="43970-876">Uppdatera i tester för att referera till en ny SDK-version</span><span class="sxs-lookup"><span data-stu-id="43970-876">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="43970-877">Utdatastrukturen har uppdaterats från kapslad till förenklad.</span><span class="sxs-lookup"><span data-stu-id="43970-877">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="43970-878">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="43970-878">Az.IotHub</span></span>
* <span data-ttu-id="43970-879">Lägg till ny routningskälla: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="43970-879">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="43970-880">Mindre felkorrigering: Get-AzIothub returnerar inte subscriptionId</span><span class="sxs-lookup"><span data-stu-id="43970-880">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="43970-881">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="43970-881">Az.Monitor</span></span>
* <span data-ttu-id="43970-882">Nya åtgärdsgruppsmottagare har lagts till för åtgärdsgrupp   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="43970-882">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="43970-883">Använd vanligt aviseringsschema som är aktiverat för mottagarna.</span><span class="sxs-lookup"><span data-stu-id="43970-883">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="43970-884">Detta gäller inte för SMS, push för Azure-app, ITSM och röstmottagare</span><span class="sxs-lookup"><span data-stu-id="43970-884">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="43970-885">Webhooks har nu stöd för Azure Active Directory-autentisering.</span><span class="sxs-lookup"><span data-stu-id="43970-885">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="43970-886">Az.Network</span><span class="sxs-lookup"><span data-stu-id="43970-886">Az.Network</span></span>
* <span data-ttu-id="43970-887">Lägg till ny cmdlet Get-AzAvailableServiceAlias som kan anropas för att hämta de alias som kan användas för tjänstslutpunktsprinciper.</span><span class="sxs-lookup"><span data-stu-id="43970-887">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="43970-888">Stöd för tillägg av trafikväljare har lagts till i gatewayanslutningar för virtuella nätverk</span><span class="sxs-lookup"><span data-stu-id="43970-888">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="43970-889">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="43970-889">New cmdlets added:</span></span>
        - <span data-ttu-id="43970-890">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="43970-890">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="43970-891">Cmdletar har uppdaterats med valfri parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="43970-891">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="43970-892">Lägg till stöd för ESP- och AH-protokoll i konfiguration av nätverkssäkerhetsregler</span><span class="sxs-lookup"><span data-stu-id="43970-892">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="43970-893">Uppdaterade cmdletar:</span><span class="sxs-lookup"><span data-stu-id="43970-893">Updated cmdlets:</span></span>
        - <span data-ttu-id="43970-894">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="43970-894">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="43970-895">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="43970-895">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="43970-896">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="43970-896">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="43970-897">Förbättra hanteringen av undantag i Cortex-cmdletar</span><span class="sxs-lookup"><span data-stu-id="43970-897">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="43970-898">Nya generationer och SKU:er för VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="43970-898">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="43970-899">Introducera nya generationer för VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="43970-899">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="43970-900">Introducera nya SKU:er med högt dataflöde för VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="43970-900">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="43970-901">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="43970-901">Az.RedisCache</span></span>
* <span data-ttu-id="43970-902">Uppdaterad referensdokumentation för ”set-AzRedisCache” för att inkludera saknade värden för parametern ”size”</span><span class="sxs-lookup"><span data-stu-id="43970-902">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="43970-903">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="43970-903">Az.Sql</span></span>
* <span data-ttu-id="43970-904">Lägg till stöd för inställningen Active Directory administratör på den hanterade instansen</span><span class="sxs-lookup"><span data-stu-id="43970-904">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="43970-905">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="43970-905">Az.Storage</span></span>
* <span data-ttu-id="43970-906">Uppdatera Lagringsklientbibliotek till 11.1.0</span><span class="sxs-lookup"><span data-stu-id="43970-906">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="43970-907">Lista containrar med hanteringsplans-API, kommer att listas med NextPageLink</span><span class="sxs-lookup"><span data-stu-id="43970-907">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="43970-908">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="43970-908">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="43970-909">Lista lagringskonton från prenumerationen, kommer att listas med NextPageLink</span><span class="sxs-lookup"><span data-stu-id="43970-909">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="43970-910">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="43970-910">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="43970-911">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="43970-911">Az.StorageSync</span></span>
* <span data-ttu-id="43970-912">Åtgärda problemet 9810 i Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="43970-912">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="43970-913">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="43970-913">Az.Websites</span></span>
* <span data-ttu-id="43970-914">Set-AzWebApp – uppdatering av ASP för en app misslyckades</span><span class="sxs-lookup"><span data-stu-id="43970-914">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="43970-915">2.7.0 – september 2019</span><span class="sxs-lookup"><span data-stu-id="43970-915">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="43970-916">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="43970-916">Az.ApiManagement</span></span>
* <span data-ttu-id="43970-917">Uppdatera ”-Format”-parameterbeskrivningen i ”Set-AzApiManagementPolicy”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="43970-917">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="43970-918">Referenser för den föråldrade cmdleten ”Update-AzApiManagementDeployment” har tagits bort från referensdokumentationen.</span><span class="sxs-lookup"><span data-stu-id="43970-918">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="43970-919">Använd ”Set-AzApiManagement” i stället.</span><span class="sxs-lookup"><span data-stu-id="43970-919">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="43970-920">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="43970-920">Az.Automation</span></span>
* <span data-ttu-id="43970-921">Stavfel har korrigerats i exempel i referensdokumentationen för ”Register-AzAutomationDscNode”</span><span class="sxs-lookup"><span data-stu-id="43970-921">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="43970-922">Klargörande har lagts till om OS-begränsningar för Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="43970-922">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="43970-923">Null-referensundantag har korrigerats för -Wait-alternativet i Start-AzAutomationRunbook-cmdleten.</span><span class="sxs-lookup"><span data-stu-id="43970-923">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="43970-924">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="43970-924">Az.Compute</span></span>
* <span data-ttu-id="43970-925">Lägg till UploadSizeInBytes-parameter till New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="43970-925">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="43970-926">Lägg till Incremental-parameter till New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="43970-926">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="43970-927">Lägg till en funktion för virtuella datorer med låg prioritet:</span><span class="sxs-lookup"><span data-stu-id="43970-927">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="43970-928">MaxPrice-, EvictionPolicy- och Priority-parametrar har lagts till i New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="43970-928">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="43970-929">MaxPrice-parametern har lagts till i New-AzVmssConfig-, Update-AzVM- och Update-AzVmss-cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="43970-929">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="43970-930">Åtgärda problem med VM-referenser för Get-AzAvailabilitySet-cmdleten när alla tillgänglighetsuppsättningar i prenumerationen visas.</span><span class="sxs-lookup"><span data-stu-id="43970-930">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="43970-931">Korrigera null-undantaget för Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="43970-931">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="43970-932">Korrigera VHD-metoden för sökning relativt till slut.</span><span class="sxs-lookup"><span data-stu-id="43970-932">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="43970-933">Åtgärda UltraSSD-problem för New-AzVM och Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="43970-933">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="43970-934">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="43970-934">Az.DataFactory</span></span>
* <span data-ttu-id="43970-935">Lägger till 3 nya kommandon för ADF V2 – Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription och Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="43970-935">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="43970-936">ADF .Net SDK har uppdaterats till 4.1.3</span><span class="sxs-lookup"><span data-stu-id="43970-936">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="43970-937">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="43970-937">Az.HDInsight</span></span>
* <span data-ttu-id="43970-938">Anrop för icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="43970-938">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="43970-939">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="43970-939">Az.IotHub</span></span>
* <span data-ttu-id="43970-940">Lägg till stöd för att anropa redundans för en IotHub till den geo-länkade katastrofåterställningsregionen.</span><span class="sxs-lookup"><span data-stu-id="43970-940">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="43970-941">Lägg till stöd för att hantera meddelandeberikning för en IotHub.</span><span class="sxs-lookup"><span data-stu-id="43970-941">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="43970-942">Nya cmdlet:ar är:</span><span class="sxs-lookup"><span data-stu-id="43970-942">New cmdlets are:</span></span>
    - <span data-ttu-id="43970-943">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="43970-943">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="43970-944">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="43970-944">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="43970-945">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="43970-945">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="43970-946">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="43970-946">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="43970-947">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="43970-947">Az.Monitor</span></span>
* <span data-ttu-id="43970-948">Pekar på den senaste Monitor SDK:n, dvs. 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="43970-948">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="43970-949">Lägger till bakåtkompatibla ändringar i Metrics-cmdletarna, dvs. enhetsuppräkningen stöder flera nya värden.</span><span class="sxs-lookup"><span data-stu-id="43970-949">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="43970-950">Detta är skrivskyddade cmdletar, så det förekommer inga ändringar i inmatningen för cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="43970-950">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="43970-951">API-versionen för **ActionGroups**-begäranden är nu **2019-06-01**. Tidigare var den **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="43970-951">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="43970-952">Test av scenarier har uppdaterats för att anpassas till den här ändringen.</span><span class="sxs-lookup"><span data-stu-id="43970-952">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="43970-953">Ett nytt obligatoriskt argument har lagts till för konstruktorerna för klasserna **EmailReceiver** och **WebhookReceiver** – ett booleskt värde med namnet **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="43970-953">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="43970-954">Värdet är för närvarande fast till **false** så att den här icke-bakåtkompatibla ändringen är dold från cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="43970-954">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="43970-955">**Obs!** Det här är en tillfällig ändring som måste verifieras av Alerts-teamet.</span><span class="sxs-lookup"><span data-stu-id="43970-955">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="43970-956">Ordningen på argumenten för konstruktorn för klassen **Source** (relaterad till klassen **ScheduledQueryRuleSource**) har ändrats från den tidigare SDK:n.</span><span class="sxs-lookup"><span data-stu-id="43970-956">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="43970-957">Den här ändringen krävde korrigering av två enhetstest: de kompilerades, men testerna skickades inte.</span><span class="sxs-lookup"><span data-stu-id="43970-957">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="43970-958">Ordningen på argumenten för konstruktorn för klassen **AlertingAction** (relaterad till klassen **ScheduledQueryRuleSource**) har ändrats från den tidigare SDK:n.</span><span class="sxs-lookup"><span data-stu-id="43970-958">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="43970-959">Den här ändringen krävde korrigering av två enhetstest: de kompilerades, men testerna skickades inte.</span><span class="sxs-lookup"><span data-stu-id="43970-959">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="43970-960">Stöd för kriterier för dynamiskt tröskelvärde för måttavisering v2</span><span class="sxs-lookup"><span data-stu-id="43970-960">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="43970-961">New-AzMetricAlertRuleV2Criteria: skapar nu även kriterier för dynamiskt tröskelvärde</span><span class="sxs-lookup"><span data-stu-id="43970-961">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="43970-962">Add-AzMetricAlertRuleV2: accepterar nu även kriterier för dynamiskt tröskelvärde</span><span class="sxs-lookup"><span data-stu-id="43970-962">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="43970-963">Förbättringar i schemalagd frågeregel (SQR)</span><span class="sxs-lookup"><span data-stu-id="43970-963">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="43970-964">Cmdletar accepterar ”Location”-parameter i båda formaten, antingen platsen (t.ex. eastus) eller platsens visningsnamn (t.ex. USA, östra)</span><span class="sxs-lookup"><span data-stu-id="43970-964">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="43970-965">”Enabled”-parametern illustreras korrekt i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="43970-965">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="43970-966">Exempel för den valfria parametern ”ActionGroup” har lagts till</span><span class="sxs-lookup"><span data-stu-id="43970-966">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="43970-967">Förbättrade hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="43970-967">Overall improved help files</span></span>
* <span data-ttu-id="43970-968">Åtgärda bugg då omfattningstypen fastställs för ”Set-AzActionRule”</span><span class="sxs-lookup"><span data-stu-id="43970-968">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="43970-969">Az.Network</span><span class="sxs-lookup"><span data-stu-id="43970-969">Az.Network</span></span>
* <span data-ttu-id="43970-970">Korrigera felaktigt exempel i referensdokumentationen för ”New-AzApplicationGateway”</span><span class="sxs-lookup"><span data-stu-id="43970-970">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="43970-971">Lägg till anmärkning i ”Get-AzNetworkWatcherPacketCapture”-referensdokumentationen om hämtning av alla egenskaper för en paketinsamling</span><span class="sxs-lookup"><span data-stu-id="43970-971">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="43970-972">Exempel har korrigerats i ”Test-AzNetworkWatcherIPFlow”-referensdokumentationen för korrekt uppräkning av nätverkskort</span><span class="sxs-lookup"><span data-stu-id="43970-972">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="43970-973">Förbättrad tolkning av molnundantag för att visa eventuell ytterligare information</span><span class="sxs-lookup"><span data-stu-id="43970-973">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="43970-974">Förbättrad tolkning av molnundantag för att hantera ytterligare en typ av SDK-undantag</span><span class="sxs-lookup"><span data-stu-id="43970-974">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="43970-975">Felaktig mappning av säkerhetsregelmodeller har korrigerats</span><span class="sxs-lookup"><span data-stu-id="43970-975">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="43970-976">Egenskaper har lagts till för nätverksgränssnittet för funktionen Privat IP</span><span class="sxs-lookup"><span data-stu-id="43970-976">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="43970-977">Egenskapen ”PrivateEndpoint” har lagts till som en typ av PSResourceId till PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="43970-977">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="43970-978">Egenskapen ”PrivateLinkConnectionProperties” har lagts till som en typ av PSIpConfigurationConnectivityInformation till PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="43970-978">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="43970-979">Modellklassen PSIpConfigurationConnectivityInformation har lagts till</span><span class="sxs-lookup"><span data-stu-id="43970-979">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="43970-980">ApplicationRuleProtocolType ”mssql” har lagts till för Azure Firewall-resurs</span><span class="sxs-lookup"><span data-stu-id="43970-980">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="43970-981">MultiLink-stöd i virtuellt WAN</span><span class="sxs-lookup"><span data-stu-id="43970-981">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="43970-982">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="43970-982">New cmdlets</span></span>
        - <span data-ttu-id="43970-983">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="43970-983">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="43970-984">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="43970-984">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="43970-985">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="43970-985">Updated cmdlet:</span></span>
        - <span data-ttu-id="43970-986">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="43970-986">New-VpnSite</span></span>
        - <span data-ttu-id="43970-987">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="43970-987">Update-VpnSite</span></span>
        - <span data-ttu-id="43970-988">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="43970-988">New-VpnConnection</span></span>
        - <span data-ttu-id="43970-989">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="43970-989">Update-VpnConnection</span></span>
* <span data-ttu-id="43970-990">Dokument för vissa PowerShell-exempel har korrigerats så att Az-cmdletar används i stället för AzureRM-cmdletar</span><span class="sxs-lookup"><span data-stu-id="43970-990">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="43970-991">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="43970-991">Az.RecoveryServices</span></span>
* <span data-ttu-id="43970-992">Uppdatera AzureVMpolicy-objekt med ProtectedItemsCount-attribut</span><span class="sxs-lookup"><span data-stu-id="43970-992">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="43970-993">Ytterligare tester har lagts till för VM-princip och återställning av ursprungligt lagringskonto</span><span class="sxs-lookup"><span data-stu-id="43970-993">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="43970-994">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="43970-994">Az.Resources</span></span>
* <span data-ttu-id="43970-995">Åtgärda fel där det inte gick att anropa New-AzRoleAssignment utan parametern Scope.</span><span class="sxs-lookup"><span data-stu-id="43970-995">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="43970-996">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="43970-996">Az.ServiceFabric</span></span>
* <span data-ttu-id="43970-997">Stavfel har korrigerats i exempel för ”Update-AzServiceFabricReliability”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="43970-997">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="43970-998">Lägger till nya cmdletar för att hantera program och tjänster:</span><span class="sxs-lookup"><span data-stu-id="43970-998">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="43970-999">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="43970-999">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="43970-1000">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="43970-1000">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="43970-1001">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="43970-1001">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="43970-1002">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="43970-1002">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="43970-1003">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="43970-1003">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="43970-1004">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="43970-1004">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="43970-1005">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="43970-1005">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="43970-1006">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="43970-1006">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="43970-1007">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="43970-1007">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="43970-1008">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="43970-1008">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="43970-1009">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="43970-1009">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="43970-1010">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="43970-1010">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="43970-1011">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="43970-1011">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="43970-1012">Service Fabric SDK har uppgraderats till version 1.2.0 som använder Service Fabric-resursprovidern med API-version 2019-03-01.</span><span class="sxs-lookup"><span data-stu-id="43970-1012">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="43970-1013">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="43970-1013">Az.SignalR</span></span>
* <span data-ttu-id="43970-1014">Lägg till Update-, Restart-, CheckNameAvailability- och GetUsage-cmdletar</span><span class="sxs-lookup"><span data-stu-id="43970-1014">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="43970-1015">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="43970-1015">Az.Sql</span></span>
* <span data-ttu-id="43970-1016">Uppdatera exempel i referensdokumentationen för ”Get-AzSqlElasticPool”</span><span class="sxs-lookup"><span data-stu-id="43970-1016">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="43970-1017">vCore-exempel för att skapa en elastisk pool (New-AzSqlElasticPool) har lagts till.</span><span class="sxs-lookup"><span data-stu-id="43970-1017">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="43970-1018">Ta bort verifieringen av EmailAddresses och kontrollen som bekräftar att EmailAdmins inte är falskt när EmailAddresses är tomt i Set-AzSqlServerAdvancedThreatProtectionPolicy och Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="43970-1018">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="43970-1019">Server-/databasgranskningsinställningar kan tas bort när det finns flera diagnostikinställningar som aktiverar granskningskategorin.</span><span class="sxs-lookup"><span data-stu-id="43970-1019">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="43970-1020">Åtgärda verifiering av e-postadresser i flera Sql Vulnerability Assessment-cmdletar (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting och Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="43970-1020">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="43970-1021">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="43970-1021">Az.Storage</span></span>
* <span data-ttu-id="43970-1022">Exempel i referensdokumentationen för ”Get-AzStorageAccountKey” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="43970-1022">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="43970-1023">Vid upp- och nedladdning av en Azure-fil kan SMB-egenskaperna för källfilen (t.ex. filattribut, tidpunkten då filen skapades och tidpunkten för den senaste skrivningen) sparas i målfilen</span><span class="sxs-lookup"><span data-stu-id="43970-1023">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="43970-1024">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="43970-1024">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="43970-1025">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="43970-1025">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="43970-1026">Korrigera problem med uppladdningen av blockblob med egenskaper/metadata för ImmutabilityPolicy i containrar.</span><span class="sxs-lookup"><span data-stu-id="43970-1026">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="43970-1027">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="43970-1027">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="43970-1028">Stöd för hantering av Azure-filresurser med API för hanteringsplan</span><span class="sxs-lookup"><span data-stu-id="43970-1028">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="43970-1029">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="43970-1029">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="43970-1030">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="43970-1030">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="43970-1031">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="43970-1031">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="43970-1032">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="43970-1032">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="43970-1033">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="43970-1033">Az.Websites</span></span>
* <span data-ttu-id="43970-1034">Åtgärdar problemet där webapp-taggar togs bort när appen migrerades till nya ASP</span><span class="sxs-lookup"><span data-stu-id="43970-1034">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="43970-1035">Åtgärda Publish-AzureWebapp så att det fungerar i Linux och Windows</span><span class="sxs-lookup"><span data-stu-id="43970-1035">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="43970-1036">Uppdatera exempel i ”Get-AzWebAppPublishingProfile”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="43970-1036">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="43970-1037">2.6.0 – augusti 2019</span><span class="sxs-lookup"><span data-stu-id="43970-1037">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="43970-1038">Allmänt</span><span class="sxs-lookup"><span data-stu-id="43970-1038">General</span></span>
* <span data-ttu-id="43970-1039">Åtgärdade diverse skrivfel i flera moduler</span><span class="sxs-lookup"><span data-stu-id="43970-1039">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="43970-1040">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="43970-1040">Az.Accounts</span></span>
* <span data-ttu-id="43970-1041">Stöd för användartilldelat MSI i Azure Functions-autentisering (#9479)</span><span class="sxs-lookup"><span data-stu-id="43970-1041">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="43970-1042">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="43970-1042">Az.Aks</span></span>
* <span data-ttu-id="43970-1043">Åtgärda problem med utdata för "Get-AzAks"</span><span class="sxs-lookup"><span data-stu-id="43970-1043">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="43970-1044">Mer information här: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="43970-1044">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="43970-1045">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="43970-1045">Az.ApiManagement</span></span>
* <span data-ttu-id="43970-1046">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="43970-1046">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="43970-1047">Uppdatera .net-NuGet-versionen, som inte tillämpar begränsningar för productId, apiId och userId</span><span class="sxs-lookup"><span data-stu-id="43970-1047">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="43970-1048">**Get-AzApiManagementProduct** – Lade till stöd för frågekörning mot produkter via API.</span><span class="sxs-lookup"><span data-stu-id="43970-1048">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="43970-1049">**New-AzApiManagementApiRevision** – Korrigering för problem där ApiRevisionDescription inte angavs vid skapande av ny API-revision https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="43970-1049">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="43970-1050">Åtgärdade skrivfel i modellen "PsApiManagementOAuth2AuthrozationServer" till "PsApiManagementOAuth2AuthorizationServer"</span><span class="sxs-lookup"><span data-stu-id="43970-1050">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="43970-1051">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="43970-1051">Az.Batch</span></span>
* <span data-ttu-id="43970-1052">Åtgärdade skrivfel i hjälpmeddelande och dokumentation till att skriva Windows med versaler</span><span class="sxs-lookup"><span data-stu-id="43970-1052">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="43970-1053">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="43970-1053">Az.Cdn</span></span>
* <span data-ttu-id="43970-1054">Åtgärdade skrivfel i CDN-modulens konverteringshjälp</span><span class="sxs-lookup"><span data-stu-id="43970-1054">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="43970-1055">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="43970-1055">Az.Compute</span></span>
* <span data-ttu-id="43970-1056">Lägg till VmssId i New-AzVMConfig-cmdleten</span><span class="sxs-lookup"><span data-stu-id="43970-1056">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="43970-1057">Lägg till parametrarna TerminateScheduledEvents och TerminateScheduledEventNotBeforeTimeoutInMinutes i New-AzVmssConfig och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="43970-1057">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="43970-1058">Lägg till egenskapen HyperVGeneration till avbildningsobjekt för virtuell dator</span><span class="sxs-lookup"><span data-stu-id="43970-1058">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="43970-1059">Lägg till funktioner för Host och HostGroup</span><span class="sxs-lookup"><span data-stu-id="43970-1059">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="43970-1060">Nya cmdletar:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="43970-1060">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="43970-1061">HostId-parametern läggs till i New-AzVMConfig och New-AzVM</span><span class="sxs-lookup"><span data-stu-id="43970-1061">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="43970-1062">Uppdatera exempel i "Invoke-AzVMRunCommand"-dokumentationen till att använda rätt parameternamn</span><span class="sxs-lookup"><span data-stu-id="43970-1062">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="43970-1063">Uppdatera "-VolumeType"-beskrivningen i referensdokumentationen för "set-AzVMDiskEncryptionExtension" och "set-AzVmssDiskEncryptionExtension"</span><span class="sxs-lookup"><span data-stu-id="43970-1063">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="43970-1064">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="43970-1064">Az.DataFactory</span></span>
* <span data-ttu-id="43970-1065">Åtgärda skrivfel till att använda versaler för "Windows" i "New-AzDataFactoryEncryptValue"-dokumentationen</span><span class="sxs-lookup"><span data-stu-id="43970-1065">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="43970-1066">Uppdaterade ADF .Net SDK-versionen till 4.1.2</span><span class="sxs-lookup"><span data-stu-id="43970-1066">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="43970-1067">Lägg till parametrarna "DataProxyIntegrationRuntimeName", "DataProxyStagingLinkedServiceName" och "DataProxyStagingPath" för "Set-AzureRmDataFactoryV2IntegrationRuntime"-cmd för att aktivera konfiguration av lokalt installerad integrationskörning som en proxy för SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="43970-1067">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="43970-1068">Uppdaterade PSTriggerRun till att visa utlöst pipeline, meddelande och egenskaper samt PSActivityRun till att visa aktivitetstypen</span><span class="sxs-lookup"><span data-stu-id="43970-1068">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="43970-1069">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="43970-1069">Az.DataLakeStore</span></span>
* <span data-ttu-id="43970-1070">Korrigering av frysning av Get-DataLakeStoreDeletedItem för fel eller fjärrundantag.</span><span class="sxs-lookup"><span data-stu-id="43970-1070">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="43970-1071">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="43970-1071">Az.EventHub</span></span>
* <span data-ttu-id="43970-1072">Korrigering av problem #9658 : Skrivfel i parametern VirtualNteworkRule i Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="43970-1072">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="43970-1073">Korrigering av problem #9558 : Set-AzEventHubNamespace använder PATCH i stället för PUT</span><span class="sxs-lookup"><span data-stu-id="43970-1073">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="43970-1074">lade till parametern EnableKafka i Set-AzEventHubNamespace-cmdleten</span><span class="sxs-lookup"><span data-stu-id="43970-1074">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="43970-1075">Korrigering av problem #9786 : kan inte skapa en regel med Endast lyssna-behörighet</span><span class="sxs-lookup"><span data-stu-id="43970-1075">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="43970-1076">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="43970-1076">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="43970-1077">Åtgärdade skrivfel i dokumentation där "Azure" skrevs helt med gemener</span><span class="sxs-lookup"><span data-stu-id="43970-1077">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="43970-1078">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="43970-1078">Az.Monitor</span></span>
* <span data-ttu-id="43970-1079">Åtgärdade felaktigt parameternamn i hjälpdokumentationen</span><span class="sxs-lookup"><span data-stu-id="43970-1079">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="43970-1080">Az.Network</span><span class="sxs-lookup"><span data-stu-id="43970-1080">Az.Network</span></span>
* <span data-ttu-id="43970-1081">Uppdaterade New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="43970-1081">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="43970-1082">Gjorde parametern "PublicIpAddress" inaktuell eftersom den aldrig används på serversidan.</span><span class="sxs-lookup"><span data-stu-id="43970-1082">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="43970-1083">Lade till den valfria parametern "Primary", som anger huruvida den aktuella IP-konfigurationen är den primära.</span><span class="sxs-lookup"><span data-stu-id="43970-1083">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="43970-1084">Förbättrade hanteringen av felundantag för begärande från SDK – åtgärdar problemet att tidigare SDK-undantag inte hanteras på rätt sätt, vilket leder till att viktig felinformation inte visas</span><span class="sxs-lookup"><span data-stu-id="43970-1084">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="43970-1085">Justerade valideringslogiken för IPv6-IP-prefix till att kontrollera korrekt IPv6-prefixlängd.</span><span class="sxs-lookup"><span data-stu-id="43970-1085">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="43970-1086">Uppdaterade Get-AzVirtualNetworkSubnetConfig: Lade till parameter som anges till get av undernätets resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="43970-1086">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="43970-1087">Uppdaterade beskrivningen av parametern Location för AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="43970-1087">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="43970-1088">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="43970-1088">Az.OperationalInsights</span></span>
* <span data-ttu-id="43970-1089">Uppdaterade dokumentation för "New-AzOperationalInsightsLinuxSyslogDataSource"</span><span class="sxs-lookup"><span data-stu-id="43970-1089">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="43970-1090">Lade till exempel</span><span class="sxs-lookup"><span data-stu-id="43970-1090">Added example</span></span>
    - <span data-ttu-id="43970-1091">Uppdaterade beskrivningen av parametern "-Name"</span><span class="sxs-lookup"><span data-stu-id="43970-1091">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="43970-1092">Lade till ett exempel för New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="43970-1092">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="43970-1093">Ändrade beskrivningen av parametern -Name för New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="43970-1093">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="43970-1094">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="43970-1094">Az.RecoveryServices</span></span>
* <span data-ttu-id="43970-1095">Uppdatera "Get-AzRecoveryServicesBackupJobDetail.md"</span><span class="sxs-lookup"><span data-stu-id="43970-1095">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="43970-1096">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="43970-1096">Az.Resources</span></span>
* <span data-ttu-id="43970-1097">Lägg till stöd för den nya API-versionen från 2019-05-10 för Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="43970-1097">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="43970-1098">Lägg till stöd för "copy.count = 0" för variabler, resurser och egenskaper</span><span class="sxs-lookup"><span data-stu-id="43970-1098">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="43970-1099">Resurser med "condition = false" eller "copy.count = 0" tas bort i complete-läget</span><span class="sxs-lookup"><span data-stu-id="43970-1099">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="43970-1100">Lägg till ett exempel på tilldelning av princip på prenumerationsnivå i hjälpdokumentationen</span><span class="sxs-lookup"><span data-stu-id="43970-1100">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="43970-1101">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="43970-1101">Az.ServiceBus</span></span>
* <span data-ttu-id="43970-1102">Korrigering av problem #9658 : Skrivfel i parametern VirtualNetworkRule i set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="43970-1102">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="43970-1103">Korrigering av problem #9786 : kan inte skapa en regel med Endast lyssna-behörighet</span><span class="sxs-lookup"><span data-stu-id="43970-1103">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="43970-1104">Lade till det nya kommandot "Test-AzServiceBusNameAvailability" för att kontrollera namntillgängligheten för kö och ämne</span><span class="sxs-lookup"><span data-stu-id="43970-1104">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="43970-1105">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="43970-1105">Az.ServiceFabric</span></span>
* <span data-ttu-id="43970-1106">Åtgärda buggar med tillägg av nodtyps-cmdlet:</span><span class="sxs-lookup"><span data-stu-id="43970-1106">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="43970-1107">NullReferenceException-bugg när resursgrupp hade annan vmss som inte är relaterad till Service Fabric-klustret.</span><span class="sxs-lookup"><span data-stu-id="43970-1107">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="43970-1108">Åtgärdar problemet: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="43970-1108">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="43970-1109">Åtgärda bugg där cmdleten misslyckades om virtualNetwork var i en annan resursgrupp än klustret.</span><span class="sxs-lookup"><span data-stu-id="43970-1109">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="43970-1110">Åtgärdar problemet: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="43970-1110">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="43970-1111">AzServiceFabricApplicationCertificate-cmdleten görs inaktuell</span><span class="sxs-lookup"><span data-stu-id="43970-1111">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="43970-1112">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="43970-1112">Az.Sql</span></span>
* <span data-ttu-id="43970-1113">Uppdatera dokumentation om gamla gransknings-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="43970-1113">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="43970-1114">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="43970-1114">Az.Storage</span></span>
* <span data-ttu-id="43970-1115">Uppdatera hjälpen för Get/Close-AzStorageFileHandle genom att lägga till fler scenarier i cmdlet-exempel och uppdatera parameterbeskrivningar</span><span class="sxs-lookup"><span data-stu-id="43970-1115">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="43970-1116">Stöd för StandardBlobTier i uppladdningsblob och kopieringsblob</span><span class="sxs-lookup"><span data-stu-id="43970-1116">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="43970-1117">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="43970-1117">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="43970-1118">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="43970-1118">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="43970-1119">Stöd för rehydratiseringsprioritet i kopieringsblob</span><span class="sxs-lookup"><span data-stu-id="43970-1119">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="43970-1120">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="43970-1120">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="43970-1121">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="43970-1121">Az.Websites</span></span>
* <span data-ttu-id="43970-1122">Lägg till klargöranden gällande parametern -AppSettings i Set-AzWebApp och Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="43970-1122">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="43970-1123">2.5.0 – July 2019</span><span class="sxs-lookup"><span data-stu-id="43970-1123">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="43970-1124">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="43970-1124">Az.Accounts</span></span>
* <span data-ttu-id="43970-1125">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="43970-1125">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="43970-1126">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="43970-1126">Az.ApplicationInsights</span></span>
* <span data-ttu-id="43970-1127">Korrigera skrivfel i exempel i dokumentationen för Remove-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="43970-1127">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="43970-1128">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="43970-1128">Az.Automation</span></span>
* <span data-ttu-id="43970-1129">Korrigera skrivfel i resurssträng</span><span class="sxs-lookup"><span data-stu-id="43970-1129">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="43970-1130">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="43970-1130">Az.CognitiveServices</span></span>
* <span data-ttu-id="43970-1131">Stöd för NetworkRuleSet har lagts till.</span><span class="sxs-lookup"><span data-stu-id="43970-1131">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="43970-1132">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="43970-1132">Az.Compute</span></span>
* <span data-ttu-id="43970-1133">Lägg till saknade egenskaper (ComputerName, OsName, OsVersion och HyperVGeneration) för visningsobjekt i den virtuella datorinstansen.</span><span class="sxs-lookup"><span data-stu-id="43970-1133">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="43970-1134">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="43970-1134">Az.ContainerRegistry</span></span>
* <span data-ttu-id="43970-1135">Åtgärda skrivfel i Remove-AzContainerRegistryReplication för parametern Replication</span><span class="sxs-lookup"><span data-stu-id="43970-1135">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="43970-1136">Mer information finns här: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="43970-1136">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="43970-1137">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="43970-1137">Az.DataFactory</span></span>
* <span data-ttu-id="43970-1138">ADF .Net SDK-versionen har uppdaterats till 4.1.0</span><span class="sxs-lookup"><span data-stu-id="43970-1138">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="43970-1139">Korrigera skrivfel i dokumentationen för Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="43970-1139">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="43970-1140">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="43970-1140">Az.EventHub</span></span>
* <span data-ttu-id="43970-1141">Ny cmmdlet har lagts till för att skapa SAS-token: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="43970-1141">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="43970-1142">verifierings- och felmeddelande har lagts till för authorizationrules-rättigheter om endast "hantera" har tilldelats</span><span class="sxs-lookup"><span data-stu-id="43970-1142">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="43970-1143">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="43970-1143">Az.KeyVault</span></span>
* <span data-ttu-id="43970-1144">Stöd har lagts till för att ange KeySize för certifikatprinciper</span><span class="sxs-lookup"><span data-stu-id="43970-1144">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="43970-1145">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="43970-1145">Az.LogicApp</span></span>
* <span data-ttu-id="43970-1146">Korrigering för Get-AzIntegrationAccountMap för att lista alla mappningstyper</span><span class="sxs-lookup"><span data-stu-id="43970-1146">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="43970-1147">Ny MapType-parameter har lagts till för filtrering</span><span class="sxs-lookup"><span data-stu-id="43970-1147">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="43970-1148">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="43970-1148">Az.ManagedServices</span></span>
* <span data-ttu-id="43970-1149">Stöd för API-versionen 2019-06-01 (GA) har lagts till</span><span class="sxs-lookup"><span data-stu-id="43970-1149">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="43970-1150">Az.Network</span><span class="sxs-lookup"><span data-stu-id="43970-1150">Az.Network</span></span>
* <span data-ttu-id="43970-1151">Lägg till stöd för privat slutpunkt och privat länktjänst</span><span class="sxs-lookup"><span data-stu-id="43970-1151">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="43970-1152">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="43970-1152">New cmdlets</span></span>
        - <span data-ttu-id="43970-1153">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="43970-1153">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="43970-1154">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="43970-1154">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="43970-1155">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="43970-1155">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="43970-1156">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="43970-1156">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="43970-1157">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="43970-1157">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="43970-1158">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="43970-1158">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="43970-1159">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="43970-1159">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="43970-1160">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="43970-1160">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="43970-1161">Nedanstående kommandon för funktionen har uppdaterats: Flaggan PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies på undernätet i VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="43970-1161">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="43970-1162">Uppdaterade New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="43970-1162">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="43970-1163">Valfri parameter har lagts till – PrivateEndpointNetworkPoliciesFlag som konfigurerar huruvida nätverksprinciper ska tillämpas på en privat slutpunkt i det här undernätet.</span><span class="sxs-lookup"><span data-stu-id="43970-1163">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="43970-1164">Valfri parameter har lagts till – PrivateLinkServiceNetworkPoliciesFlag som konfigurerar huruvida nätverksprinciper ska tillämpas på en privat länktjänst i det här undernätet.</span><span class="sxs-lookup"><span data-stu-id="43970-1164">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="43970-1165">AzPrivateLinkService för cmdlet-parametern ServiceName har bytt namn till Name med aliaset ServiceName för bakåtkompatibilitet</span><span class="sxs-lookup"><span data-stu-id="43970-1165">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="43970-1166">Aktivera ICMP-protokoll för konfiguration av nätverkssäkerhetsregler</span><span class="sxs-lookup"><span data-stu-id="43970-1166">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="43970-1167">Uppdaterade cmdletar</span><span class="sxs-lookup"><span data-stu-id="43970-1167">Updated cmdlets</span></span>
        - <span data-ttu-id="43970-1168">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="43970-1168">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="43970-1169">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="43970-1169">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="43970-1170">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="43970-1170">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="43970-1171">Lägg till ConnectionProtocolType (Ikev1/Ikev2) som en konfigurerbar parameter för New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="43970-1171">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="43970-1172">Lägg till PrivateIpAddressVersion i LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="43970-1172">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="43970-1173">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="43970-1173">Updated cmdlet:</span></span>
        - <span data-ttu-id="43970-1174">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="43970-1174">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="43970-1175">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="43970-1175">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="43970-1176">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="43970-1176">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="43970-1177">Uppdatering av Application Gateway-kommandot New-AzApplicationGatewayProbeConfig för stöd av anpassad port i Probe</span><span class="sxs-lookup"><span data-stu-id="43970-1177">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="43970-1178">Uppdaterade New-AzApplicationGatewayProbeConfig: Den valfria parametern Port som används för avsökning i serverdelen har lagts till.</span><span class="sxs-lookup"><span data-stu-id="43970-1178">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="43970-1179">Denna parameter gäller för SKU:erna Standard_V2 och WAF_V2.</span><span class="sxs-lookup"><span data-stu-id="43970-1179">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="43970-1180">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="43970-1180">Az.OperationalInsights</span></span>
* <span data-ttu-id="43970-1181">Uppdaterade standardversionen för sparade sökningar till 1.</span><span class="sxs-lookup"><span data-stu-id="43970-1181">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="43970-1182">Åtgärdade hantering av anpassad log null regex</span><span class="sxs-lookup"><span data-stu-id="43970-1182">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="43970-1183">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="43970-1183">Az.RecoveryServices</span></span>
* <span data-ttu-id="43970-1184">Uppdatera Get-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="43970-1184">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="43970-1185">Uppdatera Get-AzRecoveryServicesBackupContainer.md</span><span class="sxs-lookup"><span data-stu-id="43970-1185">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="43970-1186">Uppdatera Get-AzRecoveryServicesVault.md</span><span class="sxs-lookup"><span data-stu-id="43970-1186">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="43970-1187">Uppdatera Wait-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="43970-1187">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="43970-1188">Uppdatera Set-AzRecoveryServicesVaultContext.md</span><span class="sxs-lookup"><span data-stu-id="43970-1188">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="43970-1189">Uppdatera Get-AzRecoveryServicesBackupItem.md</span><span class="sxs-lookup"><span data-stu-id="43970-1189">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="43970-1190">Uppdatera Get-AzRecoveryServicesBackupRecoveryPoint.md</span><span class="sxs-lookup"><span data-stu-id="43970-1190">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="43970-1191">Uppdatera Restore-AzRecoveryServicesBackupItem.md</span><span class="sxs-lookup"><span data-stu-id="43970-1191">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="43970-1192">Uppdaterat tjänstanrop för avregistrering av container för Azure-filresurs</span><span class="sxs-lookup"><span data-stu-id="43970-1192">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="43970-1193">Uppdatera Set-AzRecoveryServicesAsrAlertSetting.md</span><span class="sxs-lookup"><span data-stu-id="43970-1193">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="43970-1194">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="43970-1194">Az.Resources</span></span>
- <span data-ttu-id="43970-1195">Ta bort den cmdlet som saknas och som refereras i dokumentationen till New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="43970-1195">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="43970-1196">Princip-cmdletar har uppdaterats så att de använder den nya API-versionen 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="43970-1196">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="43970-1197">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="43970-1197">Az.ServiceBus</span></span>
* <span data-ttu-id="43970-1198">Ny cmmdlet har lagts till för att skapa SAS-token: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="43970-1198">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="43970-1199">verifierings- och felmeddelande har lagts till för authorizationrules-rättigheter om endast "hantera" har tilldelats</span><span class="sxs-lookup"><span data-stu-id="43970-1199">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="43970-1200">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="43970-1200">Az.Sql</span></span>
* <span data-ttu-id="43970-1201">Åtgärda saknade exempel för Set-AzSqlDatabaseSecondary cmdlet</span><span class="sxs-lookup"><span data-stu-id="43970-1201">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="43970-1202">Åtgärda angivna återkommande genomsökningar för bedömning av säkerhetsrisk utan angivna e-postadresser</span><span class="sxs-lookup"><span data-stu-id="43970-1202">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="43970-1203">Korrigera ett skrivfel i ett varningsmeddelande.</span><span class="sxs-lookup"><span data-stu-id="43970-1203">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="43970-1204">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="43970-1204">Az.Storage</span></span>
* <span data-ttu-id="43970-1205">Uppdatera exempel i referensdokumentationen för Get-AzStorageAccount så att rätt parameternamn används</span><span class="sxs-lookup"><span data-stu-id="43970-1205">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="43970-1206">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="43970-1206">Az.StorageSync</span></span>
* <span data-ttu-id="43970-1207">Lägger till cmdleten Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="43970-1207">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="43970-1208">Åtgärda problem 9551 så att TierFilesOlderThanDays föredras</span><span class="sxs-lookup"><span data-stu-id="43970-1208">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="43970-1209">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="43970-1209">Az.Websites</span></span>
* <span data-ttu-id="43970-1210">Åtgärdar ett fel där vissa SiteConfig-egenskaper inte returnerades av Get-AzWebApp och Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="43970-1210">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="43970-1211">Lägger till en ny platsparameter för Get-AzDeletedWebApp och Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="43970-1211">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="43970-1212">Åtgärdar ett fel i kloning av webbapp-platser som använder New-AzWebApp-IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="43970-1212">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="43970-1213">2.4.0 – juli 2019</span><span class="sxs-lookup"><span data-stu-id="43970-1213">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="43970-1214">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="43970-1214">Az.Accounts</span></span>
* <span data-ttu-id="43970-1215">Lägg till stöd för profil-cmdletar</span><span class="sxs-lookup"><span data-stu-id="43970-1215">Add support for profile cmdlets</span></span>
* <span data-ttu-id="43970-1216">Lägg till stöd för miljöer och dataplaner i genererade cmdletar</span><span class="sxs-lookup"><span data-stu-id="43970-1216">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="43970-1217">Åtgärda bugg där fel slutpunkt i vissa fall användes för cmdletar för dataplaner i Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="43970-1217">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="43970-1218">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="43970-1218">Az.Advisor</span></span>
* <span data-ttu-id="43970-1219">GA-version av Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="43970-1219">GA release of Az.Advisor</span></span>
* <span data-ttu-id="43970-1220">Den här modulen ingår nu som en del av `Az`-sammanslagningsmodulen</span><span class="sxs-lookup"><span data-stu-id="43970-1220">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="43970-1221">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="43970-1221">Az.ApiManagement</span></span>
* <span data-ttu-id="43970-1222">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="43970-1222">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="43970-1223">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="43970-1223">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="43970-1224">Stöd för att fråga prenumerationer efter användare och produkt har lagts till</span><span class="sxs-lookup"><span data-stu-id="43970-1224">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="43970-1225">Stöd för att fråga med hjälp av omfång ”/”, ”/apis”, ”/apis/echo-api” har lagts till</span><span class="sxs-lookup"><span data-stu-id="43970-1225">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="43970-1226">Korrigering av problem https://github.com/Azure/azure-powershell/issues/9307 och https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="43970-1226">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="43970-1227">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="43970-1227">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="43970-1228">Stöd för att ange ”ApiVersion” och ”ApiVersionSetId” när API:er importeras har lagts till</span><span class="sxs-lookup"><span data-stu-id="43970-1228">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="43970-1229">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="43970-1229">Az.Automation</span></span>
* <span data-ttu-id="43970-1230">Bugg med cmdleten Set-AzAutomationConnectionFieldValue för att hantera strängvärde har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="43970-1230">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="43970-1231">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="43970-1231">Az.Compute</span></span>
* <span data-ttu-id="43970-1232">Lägg till parametern HyperVGeneration i New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="43970-1232">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="43970-1233">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="43970-1233">Az.DataFactory</span></span>
* <span data-ttu-id="43970-1234">Uppdaterar utdata från ADF-cmdletar som hämtar aktivitetskörningar, hämtar pipelinekörningar och hämtar utlösarkörningar för stöd för Select-Object-pipe.</span><span class="sxs-lookup"><span data-stu-id="43970-1234">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="43970-1235">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="43970-1235">Az.EventGrid</span></span>
* <span data-ttu-id="43970-1236">Korrigera stavfel i dokumentation om ”New-AzEventGridSubscription”</span><span class="sxs-lookup"><span data-stu-id="43970-1236">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="43970-1237">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="43970-1237">Az.IotHub</span></span>
* <span data-ttu-id="43970-1238">Lägg till stöd för att återskapa principnycklar för auktorisering.</span><span class="sxs-lookup"><span data-stu-id="43970-1238">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="43970-1239">Az.Network</span><span class="sxs-lookup"><span data-stu-id="43970-1239">Az.Network</span></span>
* <span data-ttu-id="43970-1240">”RoutingPreference” har lagts till i offentliga IP-taggar</span><span class="sxs-lookup"><span data-stu-id="43970-1240">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="43970-1241">Förbättra exempel för referensdokumentation om ”Get-AzNetworkServiceTag”</span><span class="sxs-lookup"><span data-stu-id="43970-1241">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="43970-1242">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="43970-1242">Az.PolicyInsights</span></span>
* <span data-ttu-id="43970-1243">Åtgärda problem med null-referens i Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="43970-1243">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="43970-1244">Mer information här: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="43970-1244">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="43970-1245">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="43970-1245">Az.OperationalInsights</span></span>
* <span data-ttu-id="43970-1246">Modellen för CustomLog-datakälla som returneras i Get-AzOperationalInsightsDataSource har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="43970-1246">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="43970-1247">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="43970-1247">Az.RecoveryServices</span></span>
* <span data-ttu-id="43970-1248">Kommandot get-policy för IaaSVM:er har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="43970-1248">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="43970-1249">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="43970-1249">Az.Resources</span></span>
    - <span data-ttu-id="43970-1250">Korrigera hjälptext för den översta parametern i Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="43970-1250">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="43970-1251">Lägg till växlingsstöd på klientsidan för Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="43970-1251">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="43970-1252">Lägg till nya parametrar för Set-AzPolicyAssignment, -PolicyParameters och -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="43970-1252">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="43970-1253">En mängd dokument- och exempeluppdateringar för Policy-cmdletar</span><span class="sxs-lookup"><span data-stu-id="43970-1253">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="43970-1254">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="43970-1254">Az.ServiceBus</span></span>
* <span data-ttu-id="43970-1255">Korrigering av problem #4938 – New-AzureRmServiceBusQueue returnerar BadRequest vid konfiguration av MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="43970-1255">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="43970-1256">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="43970-1256">Az.Sql</span></span>
* <span data-ttu-id="43970-1257">Lägg till cmdletar för instansredundansgrupper från förhandsversion till offentlig version</span><span class="sxs-lookup"><span data-stu-id="43970-1257">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="43970-1258">Stöd för granskning för Azure SQL Server\Database med nya cmdletar.</span><span class="sxs-lookup"><span data-stu-id="43970-1258">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="43970-1259">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="43970-1259">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="43970-1260">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="43970-1260">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="43970-1261">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="43970-1261">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="43970-1262">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="43970-1262">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="43970-1263">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="43970-1263">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="43970-1264">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="43970-1264">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="43970-1265">Ta bort begränsningar för e-post från inställningarna för sårbarhetsbedömning</span><span class="sxs-lookup"><span data-stu-id="43970-1265">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="43970-1266">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="43970-1266">Az.Storage</span></span>
* <span data-ttu-id="43970-1267">Ändra två parametrar ”-IndexDocument” och ”-ErrorDocument404Path” från ”krävs” till ”valfri” i cmdlet:</span><span class="sxs-lookup"><span data-stu-id="43970-1267">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="43970-1268">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="43970-1268">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="43970-1269">Uppdatera hjälpen för Get-AzStorageBlobContent genom att lägga till ett exempel</span><span class="sxs-lookup"><span data-stu-id="43970-1269">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="43970-1270">Visa mer felinformation när cmdleten misslyckas med StorageException</span><span class="sxs-lookup"><span data-stu-id="43970-1270">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="43970-1271">Stöd för att skapa eller uppdatera lagringskonto med Azure Files AAD DS-autentisering</span><span class="sxs-lookup"><span data-stu-id="43970-1271">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="43970-1272">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="43970-1272">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="43970-1273">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="43970-1273">Set-AzStorageAccount</span></span>
* <span data-ttu-id="43970-1274">Stöd för att lista eller stänga filreferenser för en filresurs, filkatalog eller en fil</span><span class="sxs-lookup"><span data-stu-id="43970-1274">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="43970-1275">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="43970-1275">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="43970-1276">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="43970-1276">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="43970-1277">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="43970-1277">Az.StorageSync</span></span>
* <span data-ttu-id="43970-1278">Den här modulen ingår nu som en del av `Az`-sammanslagningsmodulen</span><span class="sxs-lookup"><span data-stu-id="43970-1278">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="43970-1279">2.3.2 – juni 2019</span><span class="sxs-lookup"><span data-stu-id="43970-1279">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="43970-1280">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="43970-1280">Az.Accounts</span></span>
* <span data-ttu-id="43970-1281">Åtgärda bugg med felaktiga webbadresser som i vissa fall användes för Functions-anrop</span><span class="sxs-lookup"><span data-stu-id="43970-1281">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="43970-1282">Mer information här: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="43970-1282">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="43970-1283">Åtgärda problem med alias från AzureRM i Az-cmdletar</span><span class="sxs-lookup"><span data-stu-id="43970-1283">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="43970-1284">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="43970-1284">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="43970-1285">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="43970-1285">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="43970-1286">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="43970-1286">Az.Compute</span></span>
* <span data-ttu-id="43970-1287">Parameteruppsättningarna New-AzVm och New-AzVmss accepterar nu parametern ”ProximityPlacementGroup”.</span><span class="sxs-lookup"><span data-stu-id="43970-1287">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="43970-1288">Stavfel i referensdokumentationen för ”New-AzVM” har korrigerats</span><span class="sxs-lookup"><span data-stu-id="43970-1288">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="43970-1289">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="43970-1289">Az.Dns</span></span>
* <span data-ttu-id="43970-1290">Stavfel i hjälpexempel för ”Set-AzDnsZone” har korrigerats.</span><span class="sxs-lookup"><span data-stu-id="43970-1290">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="43970-1291">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="43970-1291">Az.EventGrid</span></span>
* <span data-ttu-id="43970-1292">Har uppdaterats för att använda API-versionen 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="43970-1292">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="43970-1293">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="43970-1293">New cmdlets:</span></span>
    - <span data-ttu-id="43970-1294">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="43970-1294">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="43970-1295">Skapar en ny Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="43970-1295">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="43970-1296">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="43970-1296">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="43970-1297">Hämtar information om en Event Grid-domän eller hämtar en lista med alla Event Grid-domäner i den aktuella Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="43970-1297">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="43970-1298">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="43970-1298">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="43970-1299">Tar bort en Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="43970-1299">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="43970-1300">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="43970-1300">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="43970-1301">Återskapar nyckeln för delad åtkomst för en Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="43970-1301">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="43970-1302">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="43970-1302">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="43970-1303">Hämtar de nycklar för delad åtkomst som används för att publicera händelser till en Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="43970-1303">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="43970-1304">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="43970-1304">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="43970-1305">Skapar ett nytt Azure Event Grid-domänämne.</span><span class="sxs-lookup"><span data-stu-id="43970-1305">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="43970-1306">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="43970-1306">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="43970-1307">Hämtar information om ett Event Grid-domänämne eller hämtar en lista med alla Event Grid-domänämnen under en specifik Event Grid-domän i nuvarande Azure</span><span class="sxs-lookup"><span data-stu-id="43970-1307">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="43970-1308">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="43970-1308">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="43970-1309">Tar bort ett befintligt Azure Event Grid-domänämne.</span><span class="sxs-lookup"><span data-stu-id="43970-1309">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="43970-1310">Uppdaterade cmdletar:</span><span class="sxs-lookup"><span data-stu-id="43970-1310">Updated cmdlets:</span></span>
    - <span data-ttu-id="43970-1311">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="43970-1311">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="43970-1312">Lägg till nya obligatoriska parametrar för att stödja piping för den nya Event Grid-domänen och Event Grid-domänämnet för att göra det möjligt att skapa nya händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="43970-1312">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="43970-1313">Lägg till nya obligatoriska parametrar för att ange det nya Event Grid-domännamnet och/eller namnet på Event Grid-domänämnet för att göra det möjligt att skapa nya händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="43970-1313">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="43970-1314">Lägg till ny parameteruppsättningar för domäner och domänämnen för att göra det möjligt att återanvända befintliga parametrar (t.ex. EndPointType, SubjectBeginsWith osv).</span><span class="sxs-lookup"><span data-stu-id="43970-1314">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="43970-1315">Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="43970-1315">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="43970-1316">Förfallodatum för händelseprenumeration</span><span class="sxs-lookup"><span data-stu-id="43970-1316">Event subscription expiration date,</span></span>
            - <span data-ttu-id="43970-1317">Avancerade filterparametrar.</span><span class="sxs-lookup"><span data-stu-id="43970-1317">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="43970-1318">Lägg till ny uppräkning för servicebusqueue som mål.</span><span class="sxs-lookup"><span data-stu-id="43970-1318">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="43970-1319">Tillåt inte användning av ”Alla” i alternativet -IncludedEventType och ersätt det med</span><span class="sxs-lookup"><span data-stu-id="43970-1319">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="43970-1320">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="43970-1320">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="43970-1321">Lägg till ny valfria parametrar (Top, ODataQuery och NextLink) för att stödja sidnumrering och filtrering av resultat.</span><span class="sxs-lookup"><span data-stu-id="43970-1321">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="43970-1322">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="43970-1322">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="43970-1323">Lägg till nya obligatoriska parametrar för att stödja piping för en Event Grid-domän och Event Grid-domänämnen för att göra det möjligt att ta bort befintliga händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="43970-1323">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="43970-1324">Lägg till nya obligatoriska parametrar för att ange Event Grid-domännamnet och/eller namnet på Event Grid-domänämnet för att göra det möjligt att ta bort befintliga händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="43970-1324">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="43970-1325">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="43970-1325">Az.FrontDoor</span></span>
* <span data-ttu-id="43970-1326">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="43970-1326">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="43970-1327">Lägg till stöd för transformeringar och nytt värde för automatisk komplettering för operatorer (RegEx)</span><span class="sxs-lookup"><span data-stu-id="43970-1327">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="43970-1328">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="43970-1328">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="43970-1329">Lägg till nya värden för automatisk komplettering</span><span class="sxs-lookup"><span data-stu-id="43970-1329">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="43970-1330">Az.Network</span><span class="sxs-lookup"><span data-stu-id="43970-1330">Az.Network</span></span>
* <span data-ttu-id="43970-1331">Lägg till stöd för resurs för virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="43970-1331">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="43970-1332">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="43970-1332">New cmdlets</span></span>
        - <span data-ttu-id="43970-1333">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="43970-1333">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="43970-1334">Lägg till AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="43970-1334">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="43970-1335">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="43970-1335">New cmdlets</span></span>
        - <span data-ttu-id="43970-1336">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="43970-1336">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="43970-1337">Lägg till PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="43970-1337">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="43970-1338">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="43970-1338">New cmdlets</span></span>
        - <span data-ttu-id="43970-1339">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="43970-1339">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="43970-1340">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="43970-1340">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="43970-1341">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="43970-1341">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="43970-1342">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="43970-1342">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="43970-1343">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="43970-1343">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="43970-1344">Lägg till PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="43970-1344">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="43970-1345">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="43970-1345">New cmdlets</span></span>
        - <span data-ttu-id="43970-1346">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="43970-1346">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="43970-1347">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="43970-1347">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="43970-1348">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="43970-1348">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="43970-1349">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="43970-1349">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="43970-1350">Nedanstående kommandon för funktionen har uppdaterats: Flaggan UseLocalAzureIpAddress på VpnConnection</span><span class="sxs-lookup"><span data-stu-id="43970-1350">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="43970-1351">New-AzVpnConnection har uppdaterats: Den valfria parametern -UseLocalAzureIpAddress har lagts till för att visa att en lokal IP-adress i Azure ska användas som källadress när anslutningen initieras.</span><span class="sxs-lookup"><span data-stu-id="43970-1351">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="43970-1352">Set-AzVpnConnection har uppdaterats: Den valfria parametern -UseLocalAzureIpAddress har lagts till för att visa att en lokal IP-adress i Azure ska användas som källadress när anslutningen initieras.</span><span class="sxs-lookup"><span data-stu-id="43970-1352">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="43970-1353">Det skrivskyddade fältet PeeredConnections har lagts till i ExpressRoute-peering.</span><span class="sxs-lookup"><span data-stu-id="43970-1353">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="43970-1354">Det skrivskyddade fältet GlobalReachEnabled har lagts till i ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="43970-1354">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="43970-1355">Ett attribut för icke-bakåtkompatibla ändringar har lagts till för att lyfta fram utfasning av fältet AllowGlobalReach i modellen ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="43970-1355">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="43970-1356">Problem 8756 har åtgärdats: Fel vid användning av TargetListenerID med AzApplicationGatewayRedirectConfiguration-cmdletar</span><span class="sxs-lookup"><span data-stu-id="43970-1356">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="43970-1357">En bugg i New-AzApplicationGatewayPathRuleConfig som gjorde att regeluppsättningen för att återskapa inte kunde anges har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="43970-1357">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="43970-1358">Visningen av VirtualNetworkTaps i NetworkInterfaceIpConfiguration har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="43970-1358">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="43970-1359">Cortex Get-cmdletar för att visa en lista med alla delar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="43970-1359">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="43970-1360">Funktionen för att skapa VirtualHub-referenser för ExpressRouteGateways och VpnGateway har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="43970-1360">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="43970-1361">Stöd för tillgänglighetszoner i AzureFirewall och NatGateway har lagts till</span><span class="sxs-lookup"><span data-stu-id="43970-1361">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="43970-1362">Cmdleten Get-AzNetworkServiceTag har lagts till</span><span class="sxs-lookup"><span data-stu-id="43970-1362">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="43970-1363">Lägg till stöd för flera offentliga IP-adresser för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="43970-1363">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="43970-1364">Cmdleten New-AzFirewall har uppdaterats:</span><span class="sxs-lookup"><span data-stu-id="43970-1364">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="43970-1365">Parametern -PublicIpAddress som accepterar ett eller flera offentliga IP-adressobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="43970-1365">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="43970-1366">Parametern -VirtualNetwork som accepterar ett virtuellt nätverksobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="43970-1366">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="43970-1367">Metoderna AddPublicIpAddress och RemovePublicIpAddress har lagts till på brandväggsobjekt – dessa accepterar ett offentligt IP-adressobjekt som indata</span><span class="sxs-lookup"><span data-stu-id="43970-1367">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="43970-1368">Inaktuella parametrar -PublicIpName och -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="43970-1368">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="43970-1369">Nedanstående kommandon för funktionen har uppdaterats: Ange autentiseringsalternativ för VpnClient AAD till resurser för virtuella nätverksgatewayer.</span><span class="sxs-lookup"><span data-stu-id="43970-1369">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="43970-1370">New-AzVirtualNetworkGateway har uppdaterats: De valfria parametrarna AadTenantUri, AadAudienceId och AadIssuerUri för att ange VpnClient AAD-autentiseringsalternativ på en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="43970-1370">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="43970-1371">Set-AzVirtualNetworkGateway har uppdaterats: De valfria parametrarna AadTenantUri, AadAudienceId och AadIssuerUri för att ange VpnClient AAD-autentiseringsalternativ på en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="43970-1371">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="43970-1372">Set-AzVirtualNetworkGateway har uppdaterats: Den valfria växelparametern RemoveAadAuthentication som tar bort VpnClient AAD-autentiseringsalternativ från en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="43970-1372">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="43970-1373">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="43970-1373">Az.OperationalInsights</span></span>
* <span data-ttu-id="43970-1374">Aktivera prisnivån **pergb2018** i kommandot ”New-AzureRmOperationalInsightsWorkspace”</span><span class="sxs-lookup"><span data-stu-id="43970-1374">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="43970-1375">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="43970-1375">Az.Resources</span></span>
* <span data-ttu-id="43970-1376">Stöd för ytterligare alternativ för att exportera en mall</span><span class="sxs-lookup"><span data-stu-id="43970-1376">Support for additional Template Export options</span></span>
    - <span data-ttu-id="43970-1377">Lägg till parametern ”-SkipResourceNameParameterization” till Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="43970-1377">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="43970-1378">Lägg till parametern ”-SkipAllParameterization” till Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="43970-1378">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="43970-1379">Lägg till parametern ”-Resource” till Export-AzResourceGroup för exporterad resursfiltrering</span><span class="sxs-lookup"><span data-stu-id="43970-1379">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="43970-1380">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="43970-1380">Az.ServiceFabric</span></span>
* <span data-ttu-id="43970-1381">Åtgärda att fel tumavtryck används vid tilläggning av certifikat i ByExistingKeyVault i vissa fall</span><span class="sxs-lookup"><span data-stu-id="43970-1381">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="43970-1382">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="43970-1382">Az.Sql</span></span>
* <span data-ttu-id="43970-1383">Åtgärda suffix för lagringsslutpunkt i Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="43970-1383">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="43970-1384">Åtgärda att aktivering av Advanced Data Security åsidosätter Advanced Threat Protection-princip</span><span class="sxs-lookup"><span data-stu-id="43970-1384">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="43970-1385">Nya cmdletar för Management.Sql som gör att kunderna kan lägga till nycklar för transparent datakryptering (TDE) och ange TDE-skydd för hanterade instanser</span><span class="sxs-lookup"><span data-stu-id="43970-1385">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="43970-1386">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="43970-1386">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="43970-1387">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="43970-1387">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="43970-1388">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="43970-1388">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="43970-1389">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="43970-1389">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="43970-1390">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="43970-1390">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="43970-1391">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="43970-1391">Az.Storage</span></span>
* <span data-ttu-id="43970-1392">Stöd för typerna FileStorage och SkuName Premium_ZRS när lagringskonton skapas</span><span class="sxs-lookup"><span data-stu-id="43970-1392">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="43970-1393">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="43970-1393">New-AzStorageAccount</span></span>
* <span data-ttu-id="43970-1394">Beskrivningen av cmdleten för bloboföränderlighet har förtydligats</span><span class="sxs-lookup"><span data-stu-id="43970-1394">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="43970-1395">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="43970-1395">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="43970-1396">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="43970-1396">Az.Websites</span></span>
* <span data-ttu-id="43970-1397">Optimerar Get-AzWebAppCertificate för att filtrera efter resursgrupp på servern i stället för klienten</span><span class="sxs-lookup"><span data-stu-id="43970-1397">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="43970-1398">Lägger till växlingsparametern -UseDisasterRecovery till Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="43970-1398">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="43970-1399">2.2.0 – juni 2019</span><span class="sxs-lookup"><span data-stu-id="43970-1399">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="43970-1400">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="43970-1400">Az.Cdn</span></span>
* <span data-ttu-id="43970-1401">Uppdaterade cmdletar för att ge stöd för rulesEngine-funktion baserat på API-version 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="43970-1401">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="43970-1402">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="43970-1402">Az.Compute</span></span>
* <span data-ttu-id="43970-1403">Lade till parameter `NoWait` som startar åtgärden och returnerar omedelbart, innan åtgärden har slutförts.</span><span class="sxs-lookup"><span data-stu-id="43970-1403">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="43970-1404">Uppdaterade cmdletar:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="43970-1404">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="43970-1405">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="43970-1405">Az.EventHub</span></span>
* <span data-ttu-id="43970-1406">Korrigering för #9231 – Get-AzEventHubNamespace returnerar inga taggar</span><span class="sxs-lookup"><span data-stu-id="43970-1406">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="43970-1407">Korrigering för #9230 – Get-AzEventHubNamespace returnerar ResourceGroup istället för ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43970-1407">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="43970-1408">Az.Network</span><span class="sxs-lookup"><span data-stu-id="43970-1408">Az.Network</span></span>
* <span data-ttu-id="43970-1409">Uppdatera ResourceId och InputObject för NAT-gateway</span><span class="sxs-lookup"><span data-stu-id="43970-1409">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="43970-1410">Lägg till alias för ResourceId och InputObject</span><span class="sxs-lookup"><span data-stu-id="43970-1410">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="43970-1411">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="43970-1411">Az.PolicyInsights</span></span>
* <span data-ttu-id="43970-1412">Åtgärda Null-referensproblem i Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="43970-1412">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="43970-1413">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="43970-1413">Az.RecoveryServices</span></span>
* <span data-ttu-id="43970-1414">Minsta kvarhållning för IaaSVM-policy i dagar ändrat till 7 från 1</span><span class="sxs-lookup"><span data-stu-id="43970-1414">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="43970-1415">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="43970-1415">Az.ServiceBus</span></span>
* <span data-ttu-id="43970-1416">Korrigering för ärende #9182 – Get-AzServiceBusNamespace returnerar ResourceGroup istället för ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43970-1416">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="43970-1417">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="43970-1417">Az.ServiceFabric</span></span>
* <span data-ttu-id="43970-1418">Åtgärda stavfel i felmeddelandet för Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="43970-1418">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="43970-1419">Åtgärda saknat tecken i Service Fabric-kommandorader</span><span class="sxs-lookup"><span data-stu-id="43970-1419">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="43970-1420">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="43970-1420">Az.Sql</span></span>
* <span data-ttu-id="43970-1421">Lägg till parametern DnsZonePartner för New-AzureSqlInstance-cmdlet för att ge stöd för AutoDr för hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="43970-1421">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="43970-1422">Avvecklar cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="43970-1422">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="43970-1423">Döp om cmdletar för hotidentifiering till Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="43970-1423">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="43970-1424">Parametrarna New-AzSqlInstance -StorageSizeInGB och -LicenseType är nu valfria.</span><span class="sxs-lookup"><span data-stu-id="43970-1424">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="43970-1425">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="43970-1425">Az.Websites</span></span>
* <span data-ttu-id="43970-1426">åtgärdar problemet där användningen av Set-AzWebApp och Set-AzWebAppSlot med -WebApp-egenskap tog bort taggarna</span><span class="sxs-lookup"><span data-stu-id="43970-1426">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="43970-1427">2.1.0 – maj 2019</span><span class="sxs-lookup"><span data-stu-id="43970-1427">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="43970-1428">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="43970-1428">Az.ApiManagement</span></span>
* <span data-ttu-id="43970-1429">Skapade nya cmdletar för att hantera diagnostik för global- och API-omfång</span><span class="sxs-lookup"><span data-stu-id="43970-1429">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="43970-1430">**Get-AzApiManagementDiagnostic** – Skaffa diagnostik konfigurerad för global- eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="43970-1430">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="43970-1431">**New-AzApiManagementDiagnostic** – Skapa ny diagnostik för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="43970-1431">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="43970-1432">**New-AzApiManagementHttpMessageDiagnostic** – Skapa diagnostikinställning om vilka rubriker som ska loggas och storleken på brödtextbyte</span><span class="sxs-lookup"><span data-stu-id="43970-1432">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="43970-1433">**New-AzApiManagementPipelineDiagnosticSetting** – Skapa diagnostikinställningar för inkommande/utgående HTTP-meddelanden till gatewayen.</span><span class="sxs-lookup"><span data-stu-id="43970-1433">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="43970-1434">**New-AzApiManagementSamplingSetting** – Skapa samplinginställningar för begäranden/svar för en diagnostik</span><span class="sxs-lookup"><span data-stu-id="43970-1434">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="43970-1435">**Remove-AzApiManagementDiagnostic** – Ta bort en diagnostikenhet för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="43970-1435">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="43970-1436">**Set-AzApiManagementDiagnostic** – Uppdatera en diagnostikenhet för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="43970-1436">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="43970-1437">Skapade nya cmdletar för hantering av cacheminne i ApiManagement-tjänsten</span><span class="sxs-lookup"><span data-stu-id="43970-1437">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="43970-1438">**Get-AzApiManagementCache** – Hämta information om cacheminnet som anges av identifierare eller alla cacheminnen</span><span class="sxs-lookup"><span data-stu-id="43970-1438">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="43970-1439">**New-AzApiManagementCache** – Skapa ett nytt default-cacheminne eller cacheminne i en viss Azure-region</span><span class="sxs-lookup"><span data-stu-id="43970-1439">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="43970-1440">**Remove-AzApiManagementCache** – Ta bort ett cacheminne</span><span class="sxs-lookup"><span data-stu-id="43970-1440">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="43970-1441">**Remove-AzApiManagementCache** – Ta bort ett cacheminne</span><span class="sxs-lookup"><span data-stu-id="43970-1441">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="43970-1442">Skapade nya cmdletar för hantering av API-schema</span><span class="sxs-lookup"><span data-stu-id="43970-1442">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="43970-1443">**New-AzApiManagementSchema** – Skapa ett nytt schema för ett API</span><span class="sxs-lookup"><span data-stu-id="43970-1443">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="43970-1444">**Get-AzApiManagementSchema** – Hämta de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="43970-1444">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="43970-1445">**Remove-AzApiManagementSchema** – Ta bort de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="43970-1445">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="43970-1446">**Set-AzApiManagementSchema** – Uppdatera de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="43970-1446">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="43970-1447">Skapa ny cmdlet för att generera en användartoken.</span><span class="sxs-lookup"><span data-stu-id="43970-1447">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="43970-1448">**New-AzApiManagementUserToken** – Skapa en ny användartoken som enligt standardinställning är giltig i 8 timmar. Token för GIT-användaren kan skapas med den här cmdleten./</span><span class="sxs-lookup"><span data-stu-id="43970-1448">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="43970-1449">Skapade en ny cmdlet för att hämta nätverksstatus</span><span class="sxs-lookup"><span data-stu-id="43970-1449">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="43970-1450">**Get-AzApiManagementNetworkStatus** – Hämta nätverksstatusanslutningen för resurserna som API Management-tjänsten är beroende av.</span><span class="sxs-lookup"><span data-stu-id="43970-1450">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="43970-1451">Det här är användbart när du distribuerar ApiManagement-tjänsten i ett virtuellt nätverk och validerar om något beroende är brutet.</span><span class="sxs-lookup"><span data-stu-id="43970-1451">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="43970-1452">Uppdaterade cmdlet **New-AzApiManagement** för att hantera ApiManagement-tjänsten</span><span class="sxs-lookup"><span data-stu-id="43970-1452">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="43970-1453">Lade till stöd för den nya SKU:n Consumption</span><span class="sxs-lookup"><span data-stu-id="43970-1453">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="43970-1454">Aktiverade stöd för att slå på flaggan EnableClientCertificate för SKU:n Consumption</span><span class="sxs-lookup"><span data-stu-id="43970-1454">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="43970-1455">Den nya cmdleten **New-AzApiManagementSslSetting** gör det möjligt att ställa in TLS/SSL-inställningen på ”Backend” och ”Frontend” (serverdel och klientdel).</span><span class="sxs-lookup"><span data-stu-id="43970-1455">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="43970-1456">Det här kan också användas till att konfigurera chiffer som 3DES och ServerProtocols som Http2 för Frontend för en ApiManagement-tjänst.</span><span class="sxs-lookup"><span data-stu-id="43970-1456">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="43970-1457">Stöd har lagts till för att konfigurera värdnamnet DeveloperPortal på ApiManagement-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="43970-1457">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="43970-1458">Uppdaterade cmdletar **Get-AzApiManagementSsoToken** för att ta PsApiManagement-objekt som indata</span><span class="sxs-lookup"><span data-stu-id="43970-1458">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="43970-1459">Uppdaterad cmdleten för att visa infogade felmeddelanden</span><span class="sxs-lookup"><span data-stu-id="43970-1459">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="43970-1460">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Felkod: Felmeddelande av typen ValidationError: Ett eller flera fält innehåller felaktiga värden: Felinformation:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="43970-1460">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="43970-1461">Uppdaterade cmdlet **Export-AzApiManagementApi** för att exportera API:er i OpenApi 3.0-format</span><span class="sxs-lookup"><span data-stu-id="43970-1461">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="43970-1462">Uppdaterade cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="43970-1462">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="43970-1463">Importera API från dokumentspecifikationen OpenApi 3.0</span><span class="sxs-lookup"><span data-stu-id="43970-1463">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="43970-1464">Om du vill åsidosätta egenskapen PsApiManagementSchema specificerad i ett dokument (Swagger, Wadl, Wsdl, OpenApi).</span><span class="sxs-lookup"><span data-stu-id="43970-1464">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="43970-1465">Åsidosätta egenskapen ServiceUrl som specificeras i ett dokument.</span><span class="sxs-lookup"><span data-stu-id="43970-1465">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="43970-1466">Uppdaterade cmdlet **Get-AzApiManagementPolicy** för att returnera policy i undantaget format av typen icke-XML med rawxml</span><span class="sxs-lookup"><span data-stu-id="43970-1466">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="43970-1467">Uppdaterade cmdlet **Set-AzApiManagementPolicy** för att godkänna policy i undantaget format av typen icke-XML med rawxml och XML undantaget med xml</span><span class="sxs-lookup"><span data-stu-id="43970-1467">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="43970-1468">Uppdaterad cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="43970-1468">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="43970-1469">Konfigurera API med OpenId auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="43970-1469">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="43970-1470">Skapa ett API i ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="43970-1470">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="43970-1471">Klona ett API med SourceApiId och SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="43970-1471">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="43970-1472">Möjlighet att konfigurera SubscriptionRequired i API-omfattningen.</span><span class="sxs-lookup"><span data-stu-id="43970-1472">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="43970-1473">Uppdaterad cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="43970-1473">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="43970-1474">Konfigurera API med OpenId auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="43970-1474">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="43970-1475">Uppdatera ett API till ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="43970-1475">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="43970-1476">Möjlighet att konfigurera SubscriptionRequired i API-omfattningen.</span><span class="sxs-lookup"><span data-stu-id="43970-1476">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="43970-1477">Uppdaterad cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="43970-1477">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="43970-1478">Klona en befintlig version med hjälp av SourceApiRevision (kopiera taggar, produkter, åtgärder och principer).</span><span class="sxs-lookup"><span data-stu-id="43970-1478">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="43970-1479">Den nya revisionen antar ApiId från den överordnade instansen.</span><span class="sxs-lookup"><span data-stu-id="43970-1479">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="43970-1480">Tillhandahålla ApiRevisionDescription</span><span class="sxs-lookup"><span data-stu-id="43970-1480">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="43970-1481">Åsidosätta ServiceUrl vid kloning av ett API.</span><span class="sxs-lookup"><span data-stu-id="43970-1481">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="43970-1482">Uppdaterad cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="43970-1482">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="43970-1483">Konfigurera AAD eller AADB2C med en Authority</span><span class="sxs-lookup"><span data-stu-id="43970-1483">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="43970-1484">Konfigurera SignupPolicy, SigninPolicy, ProfileEditingPolicy och PasswordResetPolicy</span><span class="sxs-lookup"><span data-stu-id="43970-1484">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="43970-1485">Uppdaterad cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="43970-1485">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="43970-1486">Kompensera för ny SubscriptonModel med Scope och UserId</span><span class="sxs-lookup"><span data-stu-id="43970-1486">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="43970-1487">Kompensera för gammal prenumerationsmodell med ProductId och UserId</span><span class="sxs-lookup"><span data-stu-id="43970-1487">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="43970-1488">Lägg till funktion för att aktivera AllowTracing på prenumerationsnivå.</span><span class="sxs-lookup"><span data-stu-id="43970-1488">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="43970-1489">Uppdaterad cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="43970-1489">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="43970-1490">Kompensera för ny SubscriptonModel med Scope och UserId</span><span class="sxs-lookup"><span data-stu-id="43970-1490">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="43970-1491">Kompensera för gammal prenumerationsmodell med ProductId och UserId</span><span class="sxs-lookup"><span data-stu-id="43970-1491">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="43970-1492">Lägg till funktion för att aktivera AllowTracing på prenumerationsnivå.</span><span class="sxs-lookup"><span data-stu-id="43970-1492">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="43970-1493">Uppdaterade följande cmdletar för att acceptera ResourceId som indata</span><span class="sxs-lookup"><span data-stu-id="43970-1493">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="43970-1494">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="43970-1494">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="43970-1495">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="43970-1495">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="43970-1496">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="43970-1496">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="43970-1497">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="43970-1497">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="43970-1498">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="43970-1498">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="43970-1499">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="43970-1499">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="43970-1500">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="43970-1500">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="43970-1501">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="43970-1501">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="43970-1502">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="43970-1502">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="43970-1503">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="43970-1503">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="43970-1504">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="43970-1504">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="43970-1505">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="43970-1505">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="43970-1506">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="43970-1506">Az.Automation</span></span>
* <span data-ttu-id="43970-1507">Uppdaterade Get-AzAutomationJobOutputRecord för att hantera postvärden av typen JSON och Text.</span><span class="sxs-lookup"><span data-stu-id="43970-1507">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="43970-1508">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="43970-1508">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="43970-1509">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="43970-1509">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="43970-1510">Ändrade beteende för Start-AzAutomationDscCompilationJob till att bara starta jobbet istället för att vänta på slutförandet.</span><span class="sxs-lookup"><span data-stu-id="43970-1510">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="43970-1511">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="43970-1511">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="43970-1512">Korrigering för Get-AzAutomationDscNode när using -Name returnerar alla noder.</span><span class="sxs-lookup"><span data-stu-id="43970-1512">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="43970-1513">Nu returnerar den endast den matchande noden.</span><span class="sxs-lookup"><span data-stu-id="43970-1513">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="43970-1514">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="43970-1514">Az.Compute</span></span>
* <span data-ttu-id="43970-1515">Lägg till parametrarna ProtectFromScaleIn och ProtectFromScaleSetAction i cmdleten Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="43970-1515">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="43970-1516">Nu är standardinställningen att vimpelparametern New-AzVM använder en tillgänglig plats om USA, östra inte stöds</span><span class="sxs-lookup"><span data-stu-id="43970-1516">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="43970-1517">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="43970-1517">Az.DataLakeStore</span></span>
* <span data-ttu-id="43970-1518">Uppdatera ADLS-sdk för att använda httpclient, integrera dataplanstestning med Azure-ramverk</span><span class="sxs-lookup"><span data-stu-id="43970-1518">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="43970-1519">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="43970-1519">Az.Monitor</span></span>
* <span data-ttu-id="43970-1520">Korrigera felaktiga parameternamn i hjälpexempel</span><span class="sxs-lookup"><span data-stu-id="43970-1520">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="43970-1521">Az.Network</span><span class="sxs-lookup"><span data-stu-id="43970-1521">Az.Network</span></span>
* <span data-ttu-id="43970-1522">Lägg till flaggan DisableBgpRoutePropagation i utdata för effektiv routningstabell</span><span class="sxs-lookup"><span data-stu-id="43970-1522">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="43970-1523">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="43970-1523">Updated cmdlet:</span></span>
        - <span data-ttu-id="43970-1524">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="43970-1524">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="43970-1525">Åtgärda dubbelstreck i dokumentationen New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="43970-1525">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="43970-1526">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="43970-1526">Az.Resources</span></span>
* <span data-ttu-id="43970-1527">Lägg till ny cmdlet Get-AzureRmDenyAssignment för att hämta tilldelningsnekanden</span><span class="sxs-lookup"><span data-stu-id="43970-1527">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="43970-1528">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="43970-1528">Az.Sql</span></span>
* <span data-ttu-id="43970-1529">Döp om Advanced Threat Protection-cmdletar för Advanced Data Security och aktivera Vulnerability Assessment som standard</span><span class="sxs-lookup"><span data-stu-id="43970-1529">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="43970-1530">2.0.0 – maj 2019</span><span class="sxs-lookup"><span data-stu-id="43970-1530">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="43970-1531">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="43970-1531">Az.Accounts</span></span>
* <span data-ttu-id="43970-1532">Uppdatera autentiseringsbiblioteket för att åtgärda ADFS-problem med autentisering av användarnamn/lösenord</span><span class="sxs-lookup"><span data-stu-id="43970-1532">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="43970-1533">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="43970-1533">Az.CognitiveServices</span></span>
* <span data-ttu-id="43970-1534">Visa endast Bing-ansvarsfriskrivning för Bing-sökningstjänster.</span><span class="sxs-lookup"><span data-stu-id="43970-1534">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="43970-1535">Förbättra felmeddelande när det inte går att skapa konton.</span><span class="sxs-lookup"><span data-stu-id="43970-1535">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="43970-1536">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="43970-1536">Az.Compute</span></span>
* <span data-ttu-id="43970-1537">Funktion för närhetsplaceringsgrupper.</span><span class="sxs-lookup"><span data-stu-id="43970-1537">Proximity placement group feature.</span></span>
    - <span data-ttu-id="43970-1538">Följande nya cmdletar har lagts till:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="43970-1538">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="43970-1539">Den nya parametern ProximityPlacementGroupId har lagts till i följande cmdletar:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="43970-1539">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="43970-1540">Parametern StorageAccountType har lagts till i New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="43970-1540">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="43970-1541">TargetRegion för New-AzGalleryImageVersion kan innehålla StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="43970-1541">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="43970-1542">Växlingsparametern SkipShutdown har lagts till i Stop-AzVM och Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="43970-1542">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="43970-1543">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="43970-1543">Breaking changes</span></span>
    - <span data-ttu-id="43970-1544">Set-AzVMBootDiagnostics har ändrats till Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="43970-1544">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="43970-1545">Export-AzLogAnalyticThrottledRequests har ändrats till Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="43970-1545">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="43970-1546">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="43970-1546">Az.DeploymentManager</span></span>
* <span data-ttu-id="43970-1547">De första allmänt tillgängliga versionerna av cmdletar för Distributionshanteraren i Azure</span><span class="sxs-lookup"><span data-stu-id="43970-1547">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="43970-1548">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="43970-1548">Az.Dns</span></span>
* <span data-ttu-id="43970-1549">Automatisk delegering av DNS för NameServer</span><span class="sxs-lookup"><span data-stu-id="43970-1549">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="43970-1550">Det överordnade zonnamnet kan användas som ytterligare valfri parameter i cmdleten för att skapa DNS-zoner.</span><span class="sxs-lookup"><span data-stu-id="43970-1550">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="43970-1551">Lägger till NS-poster för en nyligen skapad underordnad zon i den överordnade zonen.</span><span class="sxs-lookup"><span data-stu-id="43970-1551">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="43970-1552">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="43970-1552">Az.FrontDoor</span></span>
* <span data-ttu-id="43970-1553">De första allmänt tillgängliga versionerna av cmdletar för Azure FrontDoor</span><span class="sxs-lookup"><span data-stu-id="43970-1553">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="43970-1554">Byt namn på WAF-cmdletar så att de omfattar ”Waf”</span><span class="sxs-lookup"><span data-stu-id="43970-1554">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="43970-1555">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="43970-1555">Az.HDInsight</span></span>
* <span data-ttu-id="43970-1556">Två cmdletar har tagits bort:</span><span class="sxs-lookup"><span data-stu-id="43970-1556">Removed two cmdlets:</span></span>
    - <span data-ttu-id="43970-1557">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="43970-1557">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="43970-1558">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="43970-1558">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="43970-1559">En ny cmdlet har lagts till, Set-AzHDInsightGatewayCredential, som ersätter Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="43970-1559">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="43970-1560">Uppdatera cmdleten Get-AzHDInsightJobOutput för att skilja mellan läsarrollen och HDInsight-operatörsrollen:</span><span class="sxs-lookup"><span data-stu-id="43970-1560">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="43970-1561">Användare med läsarrollen måste uttryckligen ange parametern ”DefaultStorageAccountKey”, annars uppstår fel.</span><span class="sxs-lookup"><span data-stu-id="43970-1561">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="43970-1562">Användare med HDInsight-operatörsrollen påverkas inte.</span><span class="sxs-lookup"><span data-stu-id="43970-1562">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="43970-1563">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="43970-1563">Az.Monitor</span></span>
* <span data-ttu-id="43970-1564">Nya cmdletar för SQR API (schemalagd frågeregel)</span><span class="sxs-lookup"><span data-stu-id="43970-1564">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="43970-1565">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="43970-1565">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="43970-1566">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="43970-1566">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="43970-1567">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="43970-1567">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="43970-1568">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="43970-1568">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="43970-1569">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="43970-1569">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="43970-1570">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="43970-1570">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="43970-1571">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="43970-1571">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="43970-1572">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="43970-1572">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="43970-1573">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="43970-1573">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="43970-1574">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="43970-1574">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="43970-1575">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="43970-1575">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="43970-1576">[Mer](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information om SQR API</span><span class="sxs-lookup"><span data-stu-id="43970-1576">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="43970-1577">Az.Monitor.md har uppdaterats för att omfatta cmdletar för måttbaserade aviseringsregler i GenV2 (inte klassiska)</span><span class="sxs-lookup"><span data-stu-id="43970-1577">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="43970-1578">Az.Network</span><span class="sxs-lookup"><span data-stu-id="43970-1578">Az.Network</span></span>
* <span data-ttu-id="43970-1579">Lägg till stöd för NAT Gateway-resurs</span><span class="sxs-lookup"><span data-stu-id="43970-1579">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="43970-1580">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="43970-1580">New cmdlets</span></span>
        - <span data-ttu-id="43970-1581">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="43970-1581">New-AzNatGateway</span></span>
        - <span data-ttu-id="43970-1582">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="43970-1582">Get-AzNatGateway</span></span>
        - <span data-ttu-id="43970-1583">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="43970-1583">Set-AzNatGateway</span></span>
        - <span data-ttu-id="43970-1584">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="43970-1584">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="43970-1585">Uppdaterade cmdletar</span><span class="sxs-lookup"><span data-stu-id="43970-1585">Updated cmdlets</span></span>
        - <span data-ttu-id="43970-1586">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="43970-1586">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="43970-1587">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="43970-1587">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="43970-1588">Nedanstående kommandon för funktionen har uppdaterats: Ange/ta bort anpassade vägar på Brooklyn Gateway.</span><span class="sxs-lookup"><span data-stu-id="43970-1588">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="43970-1589">New-AzVirtualNetworkGateway har uppdaterats: Den valfria parametern -CustomRoute har lagts till för att ställa in adressprefix som anpassade vägar för att ange gateway.</span><span class="sxs-lookup"><span data-stu-id="43970-1589">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="43970-1590">Set-AzVirtualNetworkGateway har uppdaterats: Den valfria parametern -CustomRoute har lagts till för att ange adressprefix som anpassade vägar för att ange gateway.</span><span class="sxs-lookup"><span data-stu-id="43970-1590">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="43970-1591">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="43970-1591">Az.PolicyInsights</span></span>
* <span data-ttu-id="43970-1592">Stöd för att fråga efter information om principutvärdering.</span><span class="sxs-lookup"><span data-stu-id="43970-1592">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="43970-1593">Lägg till parametern ”-Expand” för Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="43970-1593">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="43970-1594">Stöd för -Expand PolicyEvaluationDetails.</span><span class="sxs-lookup"><span data-stu-id="43970-1594">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="43970-1595">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="43970-1595">Az.RecoveryServices</span></span>
* <span data-ttu-id="43970-1596">Stöd för att dela prenumeration mellan Azure och Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="43970-1596">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="43970-1597">Markering av kommande icke-bakåtkompatibla ändringar för Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="43970-1597">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="43970-1598">Korrigering för återställningsplan och åtgärdsplan i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="43970-1598">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="43970-1599">Korrigering för mappning av uppdateringsnätverk i Azure Site Recovery för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="43970-1599">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="43970-1600">Korrigering för instruktioner för uppdateringsskydd i Azure Site Recovery för Azure till Azure för hanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="43970-1600">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="43970-1601">Andra mindre korrigeringar.</span><span class="sxs-lookup"><span data-stu-id="43970-1601">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="43970-1602">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="43970-1602">Az.Relay</span></span>
* <span data-ttu-id="43970-1603">Korrigera stavfel i kundriktade meddelanden</span><span class="sxs-lookup"><span data-stu-id="43970-1603">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="43970-1604">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="43970-1604">Az.ServiceBus</span></span>
* <span data-ttu-id="43970-1605">Nya cmdletar har lagts till för NetworkRuleSet för namnområden</span><span class="sxs-lookup"><span data-stu-id="43970-1605">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="43970-1606">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="43970-1606">Az.Storage</span></span>
* <span data-ttu-id="43970-1607">Uppgradera till lagringsklientbiblioteket 10.0.1 (namnområdet för alla objekt från detta SDK ändras från ”Microsoft.WindowsAzure.Storage. *till ”Microsoft.Azure.Storage.* ”)</span><span class="sxs-lookup"><span data-stu-id="43970-1607">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="43970-1608">Uppgradera till Microsoft.Azure.Management.Storage 11.0.0 för att stödja den nya API-versionen 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="43970-1608">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="43970-1609">Standardlagringskontot i Skapa lagringskonto ändras från ”Storage” till ”StorageV2”</span><span class="sxs-lookup"><span data-stu-id="43970-1609">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="43970-1610">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="43970-1610">New-AzStorageAccount</span></span>
* <span data-ttu-id="43970-1611">Ändra lagringskontots cmdlet-utdata Sku.Name för att passa med indata-SkuName genom att lägga till ”-”. Till exempel ändras ”StandardLRS” till ”Standard_LRS”</span><span class="sxs-lookup"><span data-stu-id="43970-1611">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="43970-1612">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="43970-1612">New-AzStorageAccount</span></span>
    - <span data-ttu-id="43970-1613">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="43970-1613">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="43970-1614">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="43970-1614">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="43970-1615">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="43970-1615">Az.Websites</span></span>
* <span data-ttu-id="43970-1616">Egenskapen ”typ” konfigureras nu för PSSite-objekt som returneras av Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="43970-1616">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="43970-1617">Get-AzWebApp\*Metrics och Get-AzAppServicePlanMetrics markeras som inaktuella</span><span class="sxs-lookup"><span data-stu-id="43970-1617">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="43970-1618">1.8.0 – april 2019</span><span class="sxs-lookup"><span data-stu-id="43970-1618">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="43970-1619">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="43970-1619">Highlights since the last major release</span></span>
* <span data-ttu-id="43970-1620">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="43970-1620">General availability of `Az` module</span></span>
* <span data-ttu-id="43970-1621">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="43970-1621">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="43970-1622">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="43970-1622">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="43970-1623">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="43970-1623">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="43970-1624">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="43970-1624">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="43970-1625">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="43970-1625">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="43970-1626">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="43970-1626">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="43970-1627">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="43970-1627">Az.Accounts</span></span>
* <span data-ttu-id="43970-1628">Uppdatera Uninstall-AzureRm för att ta bort moduler i Mac på ett korrekt sätt</span><span class="sxs-lookup"><span data-stu-id="43970-1628">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="43970-1629">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="43970-1629">Az.Batch</span></span>
* <span data-ttu-id="43970-1630">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="43970-1630">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="43970-1631">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="43970-1631">Az.Cdn</span></span>
* <span data-ttu-id="43970-1632">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="43970-1632">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="43970-1633">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="43970-1633">Az.CognitiveServices</span></span>
* <span data-ttu-id="43970-1634">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="43970-1634">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="43970-1635">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="43970-1635">Az.Compute</span></span>
* <span data-ttu-id="43970-1636">Åtgärda problem med AEM-installationen om resurs-ID:n för diskar innehåller resourcegroups i gemener i resurs-ID:n</span><span class="sxs-lookup"><span data-stu-id="43970-1636">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="43970-1637">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="43970-1637">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="43970-1638">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="43970-1638">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="43970-1639">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="43970-1639">Az.DataFactory</span></span>
* <span data-ttu-id="43970-1640">Lägg till SsisProperties om NodeCount inte är null för hanterad integreringskörning.</span><span class="sxs-lookup"><span data-stu-id="43970-1640">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="43970-1641">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="43970-1641">Az.DataLakeStore</span></span>
* <span data-ttu-id="43970-1642">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="43970-1642">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="43970-1643">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="43970-1643">Az.EventGrid</span></span>
* <span data-ttu-id="43970-1644">Hjälptexten för slutpunkten har uppdaterats för att visa att resurser ska skapas innan cmdletarna för att skapa/uppdatera händelseprenumerationer används.</span><span class="sxs-lookup"><span data-stu-id="43970-1644">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="43970-1645">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="43970-1645">Az.EventHub</span></span>
* <span data-ttu-id="43970-1646">Nya cmdletar har lagts till för NetworkRuleSet för namnområden</span><span class="sxs-lookup"><span data-stu-id="43970-1646">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="43970-1647">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="43970-1647">Az.HDInsight</span></span>
* <span data-ttu-id="43970-1648">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="43970-1648">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="43970-1649">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="43970-1649">Az.IotHub</span></span>
* <span data-ttu-id="43970-1650">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="43970-1650">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="43970-1651">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="43970-1651">Az.KeyVault</span></span>
* <span data-ttu-id="43970-1652">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="43970-1652">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="43970-1653">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="43970-1653">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="43970-1654">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="43970-1654">Az.MachineLearning</span></span>
* <span data-ttu-id="43970-1655">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="43970-1655">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="43970-1656">Az.Media</span><span class="sxs-lookup"><span data-stu-id="43970-1656">Az.Media</span></span>
* <span data-ttu-id="43970-1657">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="43970-1657">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="43970-1658">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="43970-1658">Az.Monitor</span></span>
  * <span data-ttu-id="43970-1659">Nya cmdletar för måttbaserad aviseringsregel i GenV2 (inte klassisk)</span><span class="sxs-lookup"><span data-stu-id="43970-1659">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="43970-1660">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="43970-1660">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="43970-1661">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="43970-1661">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="43970-1662">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="43970-1662">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="43970-1663">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="43970-1663">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="43970-1664">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="43970-1664">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="43970-1665">Monitor SDK har uppdaterats till version 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="43970-1665">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="43970-1666">Az.Network</span><span class="sxs-lookup"><span data-stu-id="43970-1666">Az.Network</span></span>
* <span data-ttu-id="43970-1667">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="43970-1667">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="43970-1668">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="43970-1668">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="43970-1669">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="43970-1669">Az.NotificationHubs</span></span>
* <span data-ttu-id="43970-1670">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="43970-1670">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="43970-1671">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="43970-1671">Az.OperationalInsights</span></span>
* <span data-ttu-id="43970-1672">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="43970-1672">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="43970-1673">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="43970-1673">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="43970-1674">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="43970-1674">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="43970-1675">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="43970-1675">Az.RecoveryServices</span></span>
* <span data-ttu-id="43970-1676">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="43970-1676">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="43970-1677">Tabellformatet för SQL i virtuella Azure-datorer har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="43970-1677">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="43970-1678">En alternativ metod för att hämta platser i AzureFileShare har lagts till</span><span class="sxs-lookup"><span data-stu-id="43970-1678">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="43970-1679">ScheduleRunDays i SchedulePolicy-objekt har uppdaterats enligt tidszon</span><span class="sxs-lookup"><span data-stu-id="43970-1679">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="43970-1680">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="43970-1680">Az.RedisCache</span></span>
* <span data-ttu-id="43970-1681">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="43970-1681">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="43970-1682">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="43970-1682">Az.Resources</span></span>
* <span data-ttu-id="43970-1683">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="43970-1683">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="43970-1684">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="43970-1684">Az.Sql</span></span>
* <span data-ttu-id="43970-1685">Ersätt Monitor SDK-beroende med vanlig kod</span><span class="sxs-lookup"><span data-stu-id="43970-1685">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="43970-1686">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="43970-1686">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="43970-1687">Förbättrad process för klassificering av flera kolumner.</span><span class="sxs-lookup"><span data-stu-id="43970-1687">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="43970-1688">Inkludera SKU-egenskaper (SKU-namn, serie, kapacitet) i svaret från Get-AzSqlServerServiceObjective och formatera som tabell som standard.</span><span class="sxs-lookup"><span data-stu-id="43970-1688">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="43970-1689">Möjlighet att använda Get-AzSqlServerServiceObjective efter plats utan att behöva en redan befintlig server i regionen.</span><span class="sxs-lookup"><span data-stu-id="43970-1689">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="43970-1690">Stöd för tidszonsparametern när hanterade instanser skapas.</span><span class="sxs-lookup"><span data-stu-id="43970-1690">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="43970-1691">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="43970-1691">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="43970-1692">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="43970-1692">Az.Websites</span></span>
* <span data-ttu-id="43970-1693">åtgärdar Set-AzWebApp och Set-AzWebAppSlot så att de inte tar bort taggar vid körning</span><span class="sxs-lookup"><span data-stu-id="43970-1693">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="43970-1694">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="43970-1694">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="43970-1695">SDK för WebSites har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="43970-1695">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="43970-1696">Egenskapen AdminSiteName har tagits bort från PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="43970-1696">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="43970-1697">1.7.0 – april 2019</span><span class="sxs-lookup"><span data-stu-id="43970-1697">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="43970-1698">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="43970-1698">Highlights since the last major release</span></span>
* <span data-ttu-id="43970-1699">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="43970-1699">General availability of `Az` module</span></span>
* <span data-ttu-id="43970-1700">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="43970-1700">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="43970-1701">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="43970-1701">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="43970-1702">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="43970-1702">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="43970-1703">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="43970-1703">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="43970-1704">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="43970-1704">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="43970-1705">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="43970-1705">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="43970-1706">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="43970-1706">Az.Accounts</span></span>
* <span data-ttu-id="43970-1707">Add-AzEnvironment och Set-AzEnvironment har uppdaterats för att godkänna parametern AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="43970-1707">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="43970-1708">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="43970-1708">Az.AnalysisServices</span></span>
* <span data-ttu-id="43970-1709">ServiceClient används i cmdletar för dataplan och den ursprungliga autentiseringslogiken har tagits bort</span><span class="sxs-lookup"><span data-stu-id="43970-1709">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="43970-1710">Add-AzureASAccount används för omslutning av Connect-AzAccount för att undvika en icke-bakåtkompatibel ändring</span><span class="sxs-lookup"><span data-stu-id="43970-1710">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="43970-1711">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="43970-1711">Az.Automation</span></span>
* <span data-ttu-id="43970-1712">Buggen för cmdleten New-AzAutomationSoftwareUpdateConfiguration för inkluderingar har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="43970-1712">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="43970-1713">Nu bör parametern IncludedKbNumber och IncludedPackageNameMask fungera.</span><span class="sxs-lookup"><span data-stu-id="43970-1713">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="43970-1714">Felkorrigering för dynamiska grupper i uppdateringshanteringen för azure automation</span><span class="sxs-lookup"><span data-stu-id="43970-1714">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="43970-1715">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="43970-1715">Az.Compute</span></span>
* <span data-ttu-id="43970-1716">Lägg till parametern HyperVGeneration i New-AzDiskConfig och New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="43970-1716">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="43970-1717">Tillåt att virtuella datorer skapas med galleribilder från andra klientorganisationer.</span><span class="sxs-lookup"><span data-stu-id="43970-1717">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="43970-1718">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="43970-1718">Az.ContainerInstance</span></span>
* <span data-ttu-id="43970-1719">Ett problem har åtgärdats i parametern -Command för New-AzContainerGroup som lade till ett avslutande tomt argument</span><span class="sxs-lookup"><span data-stu-id="43970-1719">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="43970-1720">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="43970-1720">Az.DataFactory</span></span>
* <span data-ttu-id="43970-1721">ADF .Net SDK-versionen har uppdaterats till 3.0.2</span><span class="sxs-lookup"><span data-stu-id="43970-1721">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="43970-1722">Cmdleten Set-AzDataFactoryV2 har uppdaterats med extra parametrar för inställningar som rör RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="43970-1722">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="43970-1723">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="43970-1723">Az.Resources</span></span>
* <span data-ttu-id="43970-1724">Förbättra hanteringen av providrar för Get-AzResource när parametrarna -ResourceId eller -ResourceGroupName, -Name och -ResourceType tillhandahålls</span><span class="sxs-lookup"><span data-stu-id="43970-1724">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="43970-1725">Förbättra felhanteringen för ”Test-AzDeployment” och ”Test-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="43970-1725">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="43970-1726">Hantera fel utanför distributionsvalideringen och ta med dem i kommandoutdata istället</span><span class="sxs-lookup"><span data-stu-id="43970-1726">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="43970-1727">Mer information här: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="43970-1727">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="43970-1728">Lägg till växlingsparametern -IgnoreDynamicParameters till en uppsättning av cmdletar för distribution för att hoppa över fråga i skript och jobbscenarier</span><span class="sxs-lookup"><span data-stu-id="43970-1728">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="43970-1729">Mer information här: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="43970-1729">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="43970-1730">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="43970-1730">Az.Sql</span></span>
* <span data-ttu-id="43970-1731">Stöd för dataklassificering av databaser.</span><span class="sxs-lookup"><span data-stu-id="43970-1731">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="43970-1732">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="43970-1732">Az.Storage</span></span>
* <span data-ttu-id="43970-1733">Rapportera detaljfel när lagringskontext skapas med parametern -UseConnectedAccount, men utan inloggning på Azure-kontot</span><span class="sxs-lookup"><span data-stu-id="43970-1733">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="43970-1734">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="43970-1734">New-AzStorageContext</span></span>
* <span data-ttu-id="43970-1735">Stöd för att hantera Blob Service-egenskaper för ett angivet lagringskonto med API:et för hanteringsplan</span><span class="sxs-lookup"><span data-stu-id="43970-1735">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="43970-1736">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="43970-1736">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="43970-1737">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="43970-1737">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="43970-1738">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="43970-1738">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="43970-1739">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="43970-1739">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="43970-1740">Stöd för -AsJob-cmdletar för att ladda upp och ladda ned blobar och filer</span><span class="sxs-lookup"><span data-stu-id="43970-1740">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="43970-1741">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="43970-1741">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="43970-1742">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="43970-1742">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="43970-1743">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="43970-1743">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="43970-1744">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="43970-1744">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="43970-1745">1.6.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="43970-1745">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="43970-1746">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="43970-1746">Highlights since the last major release</span></span>
* <span data-ttu-id="43970-1747">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="43970-1747">General availability of `Az` module</span></span>
* <span data-ttu-id="43970-1748">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="43970-1748">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="43970-1749">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="43970-1749">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="43970-1750">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="43970-1750">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="43970-1751">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="43970-1751">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="43970-1752">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="43970-1752">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="43970-1753">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="43970-1753">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="43970-1754">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="43970-1754">Az.Automation</span></span>
* <span data-ttu-id="43970-1755">Azure Automation – ändring av uppdateringshantering för stöd för de nya funktionerna:</span><span class="sxs-lookup"><span data-stu-id="43970-1755">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="43970-1756">Dynamisk gruppering</span><span class="sxs-lookup"><span data-stu-id="43970-1756">Dynamic grouping</span></span>
    * <span data-ttu-id="43970-1757">För-/efterskrift</span><span class="sxs-lookup"><span data-stu-id="43970-1757">Pre-Post script</span></span>
    * <span data-ttu-id="43970-1758">Inställning för omstart</span><span class="sxs-lookup"><span data-stu-id="43970-1758">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="43970-1759">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="43970-1759">Az.Compute</span></span>
* <span data-ttu-id="43970-1760">Åtgärda problem med sökvägsmatchning i Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="43970-1760">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="43970-1761">Uppdatera Compute-klientbibliotek till 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="43970-1761">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="43970-1762">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="43970-1762">Az.KeyVault</span></span>
* <span data-ttu-id="43970-1763">Stöd för jokertecken för KeyVault-cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="43970-1763">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="43970-1764">Az.Network</span><span class="sxs-lookup"><span data-stu-id="43970-1764">Az.Network</span></span>
* <span data-ttu-id="43970-1765">Lägg till stöd för Threat Intelligence för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="43970-1765">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="43970-1766">Lägg till resurs för brandväggsprincip på översta nivå och anpassade regler för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="43970-1766">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="43970-1767">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="43970-1767">Az.RecoveryServices</span></span>
* <span data-ttu-id="43970-1768">SnapshotRetentionInDays har lagts till i Azure-principen för virtuella datorer för stöd av Instant RP</span><span class="sxs-lookup"><span data-stu-id="43970-1768">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="43970-1769">Pipe-stöd för avregistrering av container har lagts till</span><span class="sxs-lookup"><span data-stu-id="43970-1769">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="43970-1770">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="43970-1770">Az.Resources</span></span>
* <span data-ttu-id="43970-1771">Uppdatera stöd för jokertecken för Get-AzResource och Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="43970-1771">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="43970-1772">Uppdatera autentiseringsuppgifter som används vid allmänna anrop till ARM</span><span class="sxs-lookup"><span data-stu-id="43970-1772">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="43970-1773">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="43970-1773">Az.Sql</span></span>
* <span data-ttu-id="43970-1774">Cmdlet-parametern (ExcludeDetectionType) för Hotidentifiering ändrades från DetectionType till sträng[] för att framtidssäkra den när nya DetectionTypes läggs till, och även för att stödja automatisk ifyllning.</span><span class="sxs-lookup"><span data-stu-id="43970-1774">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="43970-1775">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="43970-1775">Az.Storage</span></span>
* <span data-ttu-id="43970-1776">Stöd för att hämta/ange/ta bort hanteringsprincip på ett lagringskonto</span><span class="sxs-lookup"><span data-stu-id="43970-1776">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="43970-1777">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="43970-1777">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="43970-1778">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="43970-1778">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="43970-1779">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="43970-1779">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="43970-1780">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="43970-1780">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="43970-1781">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="43970-1781">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="43970-1782">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="43970-1782">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="43970-1783">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="43970-1783">Az.Websites</span></span>
* <span data-ttu-id="43970-1784">Åtgärda fel med ARM-mall som avbryter kloning av alla platser med 'New-AzWebApp -IncludeSourceWebAppSlots'</span><span class="sxs-lookup"><span data-stu-id="43970-1784">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="43970-1785">1.5.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="43970-1785">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="43970-1786">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="43970-1786">Az.Accounts</span></span>
* <span data-ttu-id="43970-1787">Lägg till kommandot Register-AzModule för stöd för AutoRest-genererade cmdletar</span><span class="sxs-lookup"><span data-stu-id="43970-1787">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="43970-1788">Uppdatera exempel för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="43970-1788">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="43970-1789">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="43970-1789">Az.Automation</span></span>
* <span data-ttu-id="43970-1790">Problem med att hämta vissa månadsscheman i flera Azure Automation-cmdletar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="43970-1790">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="43970-1791">Åtgärda problem med att Get-AzAutomationDscNode bara returnerar de 20 översta noderna.</span><span class="sxs-lookup"><span data-stu-id="43970-1791">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="43970-1792">Nu returneras alla noder</span><span class="sxs-lookup"><span data-stu-id="43970-1792">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="43970-1793">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="43970-1793">Az.Cdn</span></span>
* <span data-ttu-id="43970-1794">Nya Powershell-cmdletar för att aktivera/inaktivera anpassade domän-HTTPS har lagts till och de gamla har gjorts inaktuella</span><span class="sxs-lookup"><span data-stu-id="43970-1794">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="43970-1795">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="43970-1795">Az.Compute</span></span>
* <span data-ttu-id="43970-1796">Lägg till stöd för jokertecken för Get-cmdletar</span><span class="sxs-lookup"><span data-stu-id="43970-1796">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="43970-1797">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="43970-1797">Az.DataFactory</span></span>
* <span data-ttu-id="43970-1798">ADF .Net SDK-versionen har uppdaterats till 3.0.1</span><span class="sxs-lookup"><span data-stu-id="43970-1798">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="43970-1799">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="43970-1799">Az.LogicApp</span></span>
* <span data-ttu-id="43970-1800">Åtgärda problemet med att ListWorkflows endast hämtar den första sidan med resultat</span><span class="sxs-lookup"><span data-stu-id="43970-1800">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="43970-1801">Az.Network</span><span class="sxs-lookup"><span data-stu-id="43970-1801">Az.Network</span></span>
* <span data-ttu-id="43970-1802">Lägg till stöd för jokertecken för Network-cmdletar</span><span class="sxs-lookup"><span data-stu-id="43970-1802">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="43970-1803">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="43970-1803">Az.RecoveryServices</span></span>
* <span data-ttu-id="43970-1804">Stöd har lagts till för SQL Server i virtuella Azure-datorer</span><span class="sxs-lookup"><span data-stu-id="43970-1804">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="43970-1805">SDK-uppdatering</span><span class="sxs-lookup"><span data-stu-id="43970-1805">SDK Update</span></span>
* <span data-ttu-id="43970-1806">Get-ProtectableItem-incheckning i VMappContainer har tagits bort</span><span class="sxs-lookup"><span data-stu-id="43970-1806">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="43970-1807">Name och ServerName har lagts till som parametrar för Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="43970-1807">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="43970-1808">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="43970-1808">Az.Resources</span></span>
* <span data-ttu-id="43970-1809">Lägg till parametern `-TemplateObject` i cmdletar för distribution</span><span class="sxs-lookup"><span data-stu-id="43970-1809">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="43970-1810">Mer information här: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="43970-1810">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="43970-1811">Åtgärda problem med piping av resultatet i `Get-AzResource` till `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="43970-1811">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="43970-1812">Mer information här: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="43970-1812">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="43970-1813">Åtgärda problem med ändring av JSON-datatyp när `Set-AzResource` körs</span><span class="sxs-lookup"><span data-stu-id="43970-1813">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="43970-1814">Mer information här: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="43970-1814">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="43970-1815">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="43970-1815">Az.Sql</span></span>
* <span data-ttu-id="43970-1816">AuditingEndpointsCommunicator uppdateras.</span><span class="sxs-lookup"><span data-stu-id="43970-1816">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="43970-1817">Åtgärdar beteendet hos ett gränsscenario när nya diagnostikinställningar skapas.</span><span class="sxs-lookup"><span data-stu-id="43970-1817">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="43970-1818">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="43970-1818">Az.Storage</span></span>
* <span data-ttu-id="43970-1819">Stöd för BlockBlobStorage när Storage-konto skapas      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="43970-1819">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="43970-1820">1.4.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="43970-1820">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="43970-1821">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="43970-1821">Az.AnalysisServices</span></span>
* <span data-ttu-id="43970-1822">Inaktuell AddAzureASAccount-cmdlet</span><span class="sxs-lookup"><span data-stu-id="43970-1822">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="43970-1823">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="43970-1823">Az.Automation</span></span>
* <span data-ttu-id="43970-1824">Hjälpen för Import-AzAutomationDscNodeConfiguration har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="43970-1824">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="43970-1825">Konfigurationsnamnsvalidering har lagts till i cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="43970-1825">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="43970-1826">Förbättrad felhantering för cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="43970-1826">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="43970-1827">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="43970-1827">Az.CognitiveServices</span></span>
* <span data-ttu-id="43970-1828">CustomSubdomainName har lagts till som en ny valfri parameter för New-AzCognitiveServicesAccount, som används för att ange underdomän för resursen.</span><span class="sxs-lookup"><span data-stu-id="43970-1828">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="43970-1829">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="43970-1829">Az.Compute</span></span>
* <span data-ttu-id="43970-1830">Problemet med ID-parameteruppsättningar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="43970-1830">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="43970-1831">Get-AzVMExtension har uppdaterats så att alla installerade tillägg visas om parametern Name inte har angetts</span><span class="sxs-lookup"><span data-stu-id="43970-1831">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="43970-1832">Parametrarna Tag och ResourceId har lagts till i cmdleten Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="43970-1832">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="43970-1833">Get-AzVmssVM utan instans-ID och med InstanceView kan visa virtuella VMSS-datorer med instansvyn.</span><span class="sxs-lookup"><span data-stu-id="43970-1833">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="43970-1834">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="43970-1834">Az.DataLakeStore</span></span>
* <span data-ttu-id="43970-1835">Cmdletar har lagts till för uppräkning och återställning av borttagna objekt i ADL</span><span class="sxs-lookup"><span data-stu-id="43970-1835">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="43970-1836">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="43970-1836">Az.EventHub</span></span>
* <span data-ttu-id="43970-1837">Ny boolesk egenskap SkipEmptyArchives har lagts till i Skip Empty Archives i CaptureDescription-klassen i Eventhub</span><span class="sxs-lookup"><span data-stu-id="43970-1837">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="43970-1838">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="43970-1838">Az.KeyVault</span></span>
* <span data-ttu-id="43970-1839">Taggning i Set-AzKeyVaultSecret har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="43970-1839">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="43970-1840">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="43970-1840">Az.LogicApp</span></span>
* <span data-ttu-id="43970-1841">Grundläggande SKU har lagts till för Integrationskonton</span><span class="sxs-lookup"><span data-stu-id="43970-1841">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="43970-1842">XSLT 2.0, XSLT 3.0 och Flytande mappningstyper har lagts till</span><span class="sxs-lookup"><span data-stu-id="43970-1842">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="43970-1843">Nya cmdletar för integrationskontosammansättningar</span><span class="sxs-lookup"><span data-stu-id="43970-1843">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="43970-1844">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="43970-1844">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="43970-1845">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="43970-1845">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="43970-1846">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="43970-1846">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="43970-1847">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="43970-1847">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="43970-1848">Nya cmdletar för batchkonfiguration för integrationskonto</span><span class="sxs-lookup"><span data-stu-id="43970-1848">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="43970-1849">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="43970-1849">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="43970-1850">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="43970-1850">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="43970-1851">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="43970-1851">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="43970-1852">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="43970-1852">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="43970-1853">Logic App-SDK har uppdaterats till version 4.1.0</span><span class="sxs-lookup"><span data-stu-id="43970-1853">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="43970-1854">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="43970-1854">Az.Monitor</span></span>
* <span data-ttu-id="43970-1855">Hjälpen för Get-AzMetric har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="43970-1855">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="43970-1856">Az.Network</span><span class="sxs-lookup"><span data-stu-id="43970-1856">Az.Network</span></span>
* <span data-ttu-id="43970-1857">Hjälpexempel för Add-AzApplicationGatewayCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="43970-1857">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="43970-1858">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="43970-1858">Az.OperationalInsights</span></span>
* <span data-ttu-id="43970-1859">Ytterligare stöd för datakällorna New och Get ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="43970-1859">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="43970-1860">Ny ApplicationInsights-typ har lagts till för att ge stöd för ”Get specific” och ”Get all” för ApplicationInsights-datakällor för angiven arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="43970-1860">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="43970-1861">Cmdleten New-AzOperationalInsightsApplicationInsightsDataSource har lagts till för att skapa datakälla med angivna parametrar för Application Insights-resurs: subscription Id, resourceGroupName och name.</span><span class="sxs-lookup"><span data-stu-id="43970-1861">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="43970-1862">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="43970-1862">Az.Resources</span></span>
* <span data-ttu-id="43970-1863">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="43970-1863">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="43970-1864">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="43970-1864">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="43970-1865">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="43970-1865">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="43970-1866">Fel som gör att KeyCredentials inte kan skapas upprepade gånger har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="43970-1866">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="43970-1867">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="43970-1867">Az.Sql</span></span>
* <span data-ttu-id="43970-1868">Lägg till stöd för hyperskalanivån för SQL DB</span><span class="sxs-lookup"><span data-stu-id="43970-1868">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="43970-1869">Ett fel har åtgärdats där återställningen kunde misslyckas på grund av onödiga inställningsegenskaper i restore-förfrågan</span><span class="sxs-lookup"><span data-stu-id="43970-1869">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="43970-1870">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="43970-1870">Az.Websites</span></span>
* <span data-ttu-id="43970-1871">Rätt exempel i Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="43970-1871">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="43970-1872">1.3.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="43970-1872">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="43970-1873">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="43970-1873">Az.Accounts</span></span>
* <span data-ttu-id="43970-1874">Uppdatera till den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="43970-1874">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="43970-1875">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="43970-1875">Az.AnalysisServices</span></span>
<span data-ttu-id="43970-1876">Allmän tillgänglighet för Az.AnalysisServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="43970-1876">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="43970-1877">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="43970-1877">Az.Compute</span></span>
* <span data-ttu-id="43970-1878">AEM-tillägg: Lägg till stöd för UltraSSD-, P60-, P70- och P80-diskar</span><span class="sxs-lookup"><span data-stu-id="43970-1878">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="43970-1879">Uppdatera hjälpbeskrivning för Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="43970-1879">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="43970-1880">Uppdatera hjälpbeskrivning och exempel för Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="43970-1880">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="43970-1881">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="43970-1881">Az.RecoveryServices</span></span>
<span data-ttu-id="43970-1882">Allmän tillgänglighet för Az.RecoveryServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="43970-1882">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="43970-1883">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="43970-1883">Az.Resources</span></span>
* <span data-ttu-id="43970-1884">Korrigera taggar för resursgrupper</span><span class="sxs-lookup"><span data-stu-id="43970-1884">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="43970-1885">Mer information här: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="43970-1885">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="43970-1886">Åtgärda problem där `Get-AzureRmRoleAssignment` inte respekterar -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="43970-1886">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="43970-1887">Mer information här: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="43970-1887">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="43970-1888">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="43970-1888">Az.Sql</span></span>
* <span data-ttu-id="43970-1889">Lägga till Get/Set-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="43970-1889">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="43970-1890">Åtgärda problem där ett nullref-undantag uppstår när du kör SQL-cmdletar och inte är inloggad på ett Azure-konto</span><span class="sxs-lookup"><span data-stu-id="43970-1890">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="43970-1891">Åtgärda nullref-undantag i Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="43970-1891">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="43970-1892">1.2.1 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="43970-1892">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="43970-1893">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="43970-1893">Az.Accounts</span></span>
* <span data-ttu-id="43970-1894">Version med rätt version av autentisering</span><span class="sxs-lookup"><span data-stu-id="43970-1894">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="43970-1895">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="43970-1895">Az.AnalysisServices</span></span>
* <span data-ttu-id="43970-1896">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="43970-1896">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="43970-1897">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="43970-1897">Az.RecoveryServices</span></span>
* <span data-ttu-id="43970-1898">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="43970-1898">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="43970-1899">1.2.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="43970-1899">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="43970-1900">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="43970-1900">Az.Accounts</span></span>
* <span data-ttu-id="43970-1901">Lägga till interaktiv autentisering och autentisering med användarnamn/lösenord för endast Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="43970-1901">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="43970-1902">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="43970-1902">Update incorrect online help URLs</span></span>
* <span data-ttu-id="43970-1903">Lägga till varningsmeddelande i PS Core för Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="43970-1903">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="43970-1904">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="43970-1904">Az.Aks</span></span>
* <span data-ttu-id="43970-1905">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="43970-1905">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="43970-1906">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="43970-1906">Az.Automation</span></span>
* <span data-ttu-id="43970-1907">Stöd för Python 2-runbookflöden har lagts till</span><span class="sxs-lookup"><span data-stu-id="43970-1907">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="43970-1908">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="43970-1908">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="43970-1909">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="43970-1909">Az.Cdn</span></span>
* <span data-ttu-id="43970-1910">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="43970-1910">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="43970-1911">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="43970-1911">Az.Compute</span></span>
* <span data-ttu-id="43970-1912">Lägga till cmdleten Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="43970-1912">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="43970-1913">Lägga till TempDisk-parameter i Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="43970-1913">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="43970-1914">Korrigera varningsmeddelande för New-AzVM</span><span class="sxs-lookup"><span data-stu-id="43970-1914">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="43970-1915">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="43970-1915">Az.ContainerRegistry</span></span>
* <span data-ttu-id="43970-1916">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="43970-1916">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="43970-1917">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="43970-1917">Az.DataFactory</span></span>
* <span data-ttu-id="43970-1918">ADF .Net SDK-versionen har uppdaterats till 3.0.0</span><span class="sxs-lookup"><span data-stu-id="43970-1918">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="43970-1919">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="43970-1919">Az.DataLakeStore</span></span>
* <span data-ttu-id="43970-1920">Åtgärda problem med ADLS-slutpunkt vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="43970-1920">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="43970-1921">Mer information här: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="43970-1921">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="43970-1922">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="43970-1922">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="43970-1923">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="43970-1923">Az.IotHub</span></span>
* <span data-ttu-id="43970-1924">Lägga till kodningsformat i cmdleten Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="43970-1924">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="43970-1925">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="43970-1925">Az.KeyVault</span></span>
* <span data-ttu-id="43970-1926">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="43970-1926">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="43970-1927">Az.Network</span><span class="sxs-lookup"><span data-stu-id="43970-1927">Az.Network</span></span>
* <span data-ttu-id="43970-1928">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="43970-1928">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="43970-1929">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="43970-1929">Az.Resources</span></span>
* <span data-ttu-id="43970-1930">Åtgärda felaktiga exempel i referensdokumentationen ”New-AzADAppCredential” och ”New-AzADSpCredential”</span><span class="sxs-lookup"><span data-stu-id="43970-1930">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="43970-1931">Åtgärda problem där sökvägen för parametern ”-TemplateFile” inte omvandlas innan cmdletarna för distribution i resursgruppen körs</span><span class="sxs-lookup"><span data-stu-id="43970-1931">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="43970-1932">Az.Resources: Korrigera dokumentationen om standardvärdet för New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="43970-1932">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="43970-1933">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="43970-1933">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="43970-1934">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="43970-1934">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="43970-1935">Åtgärda formateringsproblemet med objektet ”PSResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="43970-1935">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="43970-1936">Mer information här: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="43970-1936">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="43970-1937">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="43970-1937">Az.ServiceFabric</span></span>
* <span data-ttu-id="43970-1938">Återställ när ett certifikat läggs till i en Virtual Machine Scale Sets-modell men ett undantag genereras. Detta har gjorts för att åtgärda följande fel: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="43970-1938">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="43970-1939">Korrigera några felmeddelanden.</span><span class="sxs-lookup"><span data-stu-id="43970-1939">Fix some error messages.</span></span>
* <span data-ttu-id="43970-1940">Korrigering av skapande av kluster med ARM-mall som är standard för New-AzServiceFabriCluster som inte fungerade med migrering till Az.</span><span class="sxs-lookup"><span data-stu-id="43970-1940">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="43970-1941">Korrigering av tilläggning av kluster/programcertifikat så att endast VM Scale Sets som motsvarar klustret läggs till genom att kontrollera ID för klustret i tillägget.</span><span class="sxs-lookup"><span data-stu-id="43970-1941">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="43970-1942">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="43970-1942">Az.SignalR</span></span>
* <span data-ttu-id="43970-1943">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="43970-1943">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="43970-1944">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="43970-1944">Az.Sql</span></span>
* <span data-ttu-id="43970-1945">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="43970-1945">Update incorrect online help URLs</span></span>
* <span data-ttu-id="43970-1946">Uppdaterad parameterbeskrivning för LicenseType-parameter med möjliga värden</span><span class="sxs-lookup"><span data-stu-id="43970-1946">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="43970-1947">Korrigering för att uppdatera hanterad instansidentitet som inte fungerar när det är den enda uppdaterade egenskapen</span><span class="sxs-lookup"><span data-stu-id="43970-1947">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="43970-1948">Stöd för anpassad sortering på hanterad instans</span><span class="sxs-lookup"><span data-stu-id="43970-1948">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="43970-1949">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="43970-1949">Az.Storage</span></span>
* <span data-ttu-id="43970-1950">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="43970-1950">Update incorrect online help URLs</span></span>
* <span data-ttu-id="43970-1951">Tillhandahåll detaljerat felmeddelande när en användare försöker hämta/konfigurera klassisk loggning/mått på ett Premium Storage-konto eftersom Premium Storage-kontot inte har stöd för klassisk loggning/mått.</span><span class="sxs-lookup"><span data-stu-id="43970-1951">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="43970-1952">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="43970-1952">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="43970-1953">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="43970-1953">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="43970-1954">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="43970-1954">Az.TrafficManager</span></span>
* <span data-ttu-id="43970-1955">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="43970-1955">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="43970-1956">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="43970-1956">Az.Websites</span></span>
* <span data-ttu-id="43970-1957">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="43970-1957">Update incorrect online help URLs</span></span>
* <span data-ttu-id="43970-1958">Korrigerar ”New-AzWebAppSSLBinding” så att certifikatet laddas upp till rätt resursgrupp och plats om appen finns i en ASE.</span><span class="sxs-lookup"><span data-stu-id="43970-1958">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="43970-1959">Korrigerar ”New-AzWebAppSSLBinding” så att taggarna inte skrivs över på en bindning av ett SSL-certifikat till en app</span><span class="sxs-lookup"><span data-stu-id="43970-1959">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="43970-1960">1.1.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="43970-1960">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="43970-1961">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="43970-1961">Az.Accounts</span></span>
* <span data-ttu-id="43970-1962">Lade till omfattningen ”Lokal” till Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="43970-1962">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="43970-1963">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="43970-1963">Az.Compute</span></span>
* <span data-ttu-id="43970-1964">Namn är nu valfritt i ID-parametern för Restart/Start/Stop/Remove/Set-AzVM och Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="43970-1964">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="43970-1965">Uppdaterade beskrivningen av ID i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="43970-1965">Updated the description of ID in help files</span></span>
* <span data-ttu-id="43970-1966">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="43970-1966">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="43970-1967">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="43970-1967">Az.DataLakeStore</span></span>
* <span data-ttu-id="43970-1968">Uppdatera sdk-versionen av dataplanet till 1.1.14 för SDK-korrigeringar.</span><span class="sxs-lookup"><span data-stu-id="43970-1968">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="43970-1969">Korrigerade hanteringen av negativ accesstime och modificationtime för getfilestatus och liststatus; korrigera asynkront annulleringstoken</span><span class="sxs-lookup"><span data-stu-id="43970-1969">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="43970-1970">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="43970-1970">Az.EventGrid</span></span>
* <span data-ttu-id="43970-1971">Uppdaterat för användning av API-versionen 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="43970-1971">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="43970-1972">Uppdaterade följande cmdletar för att stödja nytt scenario i API-versionen 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="43970-1972">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="43970-1973">New-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="43970-1973">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="43970-1974">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="43970-1974">Event Time-To-Live,</span></span>
        - <span data-ttu-id="43970-1975">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="43970-1975">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="43970-1976">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="43970-1976">Dead letter endpoint.</span></span>
    - <span data-ttu-id="43970-1977">Update-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="43970-1977">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="43970-1978">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="43970-1978">Event Time-To-Live,</span></span>
        - <span data-ttu-id="43970-1979">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="43970-1979">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="43970-1980">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="43970-1980">Dead letter endpoint.</span></span>
* <span data-ttu-id="43970-1981">Lade till nya enum-värden (storageQueue och hybridConnection) för alternativet EndpointType i cmdletarna New-AzureRmEventGridSubscription och Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="43970-1981">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="43970-1982">Visa varningsmeddelanden om skapande eller uppdatering av händelseprenumerationen förväntas medföra manuell åtgärd från användaren.</span><span class="sxs-lookup"><span data-stu-id="43970-1982">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="43970-1983">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="43970-1983">Az.IotHub</span></span>
* <span data-ttu-id="43970-1984">Har uppdaterats till den senaste versionen av SDK:n lotHub</span><span class="sxs-lookup"><span data-stu-id="43970-1984">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="43970-1985">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="43970-1985">Az.LogicApp</span></span>
* <span data-ttu-id="43970-1986">Get-AzLogicApp visar en lista över alla som inte har angivet namn</span><span class="sxs-lookup"><span data-stu-id="43970-1986">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="43970-1987">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="43970-1987">Az.Resources</span></span>
* <span data-ttu-id="43970-1988">Åtgärdade problem med parameteruppsättningen när parametrarna -ODataQuery och -ResourceId anges för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="43970-1988">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="43970-1989">Mer information här: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="43970-1989">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="43970-1990">Åtgärdade hantering av parametern -Custom i New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="43970-1990">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="43970-1991">Korrigerade stavfel i New-AzDeployment-dokumentationen</span><span class="sxs-lookup"><span data-stu-id="43970-1991">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="43970-1992">Gjorde parametern -MailNickname obligatorisk för New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="43970-1992">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="43970-1993">Mer information här: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="43970-1993">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="43970-1994">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="43970-1994">Az.SignalR</span></span>
* <span data-ttu-id="43970-1995">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="43970-1995">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="43970-1996">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="43970-1996">Az.Sql</span></span>
* <span data-ttu-id="43970-1997">Konverterade lagringshanteringsklientens beroende av den normala SDK-implementeringen.</span><span class="sxs-lookup"><span data-stu-id="43970-1997">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="43970-1998">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="43970-1998">Az.Storage</span></span>
* <span data-ttu-id="43970-1999">Angav StorageAccountName för lagringskontext som det verkliga namnet på lagringskontot när det skapas med Sas Token, OAuth eller Anonymous</span><span class="sxs-lookup"><span data-stu-id="43970-1999">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="43970-2000">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="43970-2000">New-AzStorageContext</span></span>
* <span data-ttu-id="43970-2001">Skapade Sas Token för Blob Snapshot-objekt med parametern -FullUri, åtgärdade den returnerade URI:n så att den blir URI för ögonblicksbild</span><span class="sxs-lookup"><span data-stu-id="43970-2001">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="43970-2002">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="43970-2002">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="43970-2003">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="43970-2003">Az.Websites</span></span>
* <span data-ttu-id="43970-2004">Åtgärdade en bugg i datumparsningen i Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="43970-2004">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="43970-2005">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="43970-2005">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="43970-2006">1.0.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="43970-2006">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="43970-2007">Allmänt</span><span class="sxs-lookup"><span data-stu-id="43970-2007">General</span></span>

- <span data-ttu-id="43970-2008">Allmän tillgänglighet för Az-modulen</span><span class="sxs-lookup"><span data-stu-id="43970-2008">General Availability of Az Module</span></span>
- <span data-ttu-id="43970-2009">Onlinehjälp för varje modul</span><span class="sxs-lookup"><span data-stu-id="43970-2009">Online help for each module</span></span>
- <span data-ttu-id="43970-2010">Mer information och en översikt finns på [Az-informationssidan](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="43970-2010">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="43970-2011">Information om hur du migrerar från AzureRM finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="43970-2011">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="43970-2012">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="43970-2012">Az.Accounts</span></span>
- <span data-ttu-id="43970-2013">Har ändrats från Az.Profile</span><span class="sxs-lookup"><span data-stu-id="43970-2013">Changed from Az.Profile</span></span>
- <span data-ttu-id="43970-2014">Fasta tabellformat för profil- och kontexttyper</span><span class="sxs-lookup"><span data-stu-id="43970-2014">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="43970-2015">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="43970-2015">Az.ApiManagement</span></span>
- <span data-ttu-id="43970-2016">Korrigeringar för #7002</span><span class="sxs-lookup"><span data-stu-id="43970-2016">Fixes for #7002</span></span>
- <span data-ttu-id="43970-2017">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="43970-2017">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="43970-2018">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="43970-2018">Az.Batch</span></span>
- <span data-ttu-id="43970-2019">Lade till möjligheten att se vilken version av Azure Batch Node Agent som körs på var och en av de virtuella datorerna i en pool, via den nya egenskapen `NodeAgentInformation` på `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="43970-2019">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="43970-2020">Standarden `Caching` för `PSDataDisk` är nu `ReadWrite` i stället för `None`.</span><span class="sxs-lookup"><span data-stu-id="43970-2020">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="43970-2021">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="43970-2021">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="43970-2022">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="43970-2022">Az.Billing</span></span>
- <span data-ttu-id="43970-2023">Kombinerar cmdletarna för fakturering, förbrukning och UsageAggregates. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="43970-2023">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="43970-2024">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="43970-2024">Az.CognitivServices</span></span>
- <span data-ttu-id="43970-2025">Lade till kompletterare för SkuName och Typem som är tillgängliga i New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="43970-2025">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="43970-2026">Tog bort parameteruppsättningen GetSkusWithAccountParamSetName från Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="43970-2026">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="43970-2027">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="43970-2027">Az.ContainerInstance</span></span>
- <span data-ttu-id="43970-2028">Stöd för ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="43970-2028">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="43970-2029">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="43970-2029">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="43970-2030">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="43970-2030">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="43970-2031">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="43970-2031">Az.DataLakeStore</span></span>
- <span data-ttu-id="43970-2032">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="43970-2032">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="43970-2033">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="43970-2033">Az.Monitor</span></span>
- <span data-ttu-id="43970-2034">Döpte om Az.Insights till Az.Monitor och andra mindre icke-bakåtkompatibla ändringar. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="43970-2034">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="43970-2035">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="43970-2035">Az.KeyVault</span></span>
- <span data-ttu-id="43970-2036">Tog bort den inaktuella egenskapen PurgeDisabled från utdatatyper</span><span class="sxs-lookup"><span data-stu-id="43970-2036">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="43970-2037">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="43970-2037">Az.MachineLearning</span></span>
- <span data-ttu-id="43970-2038">Inkluderade cmdletarna från modulen Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="43970-2038">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="43970-2039">Az.Media</span><span class="sxs-lookup"><span data-stu-id="43970-2039">Az.Media</span></span>
- <span data-ttu-id="43970-2040">Tog bort inaktuella -Tags-alias från New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="43970-2040">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="43970-2041">Az.Network</span><span class="sxs-lookup"><span data-stu-id="43970-2041">Az.Network</span></span>
<span data-ttu-id="43970-2042">Stöd har lagts till för konfiguration av RewriteRuleSets i Application Gateway</span><span class="sxs-lookup"><span data-stu-id="43970-2042">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="43970-2043">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="43970-2043">New cmdlets added:</span></span>
        - <span data-ttu-id="43970-2044">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="43970-2044">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="43970-2045">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="43970-2045">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="43970-2046">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="43970-2046">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="43970-2047">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="43970-2047">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="43970-2048">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="43970-2048">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="43970-2049">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="43970-2049">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="43970-2050">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="43970-2050">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="43970-2051">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="43970-2051">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="43970-2052">Cmdletar har uppdaterats med den valfria parametern -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="43970-2052">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="43970-2053">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="43970-2053">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="43970-2054">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="43970-2054">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="43970-2055">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="43970-2055">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="43970-2056">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="43970-2056">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="43970-2057">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="43970-2057">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="43970-2058">New-AzureRmApplicationGatewayUrlPathMapConfig har lagt till KeyVault-stöd för Application Gateway med Identity.</span><span class="sxs-lookup"><span data-stu-id="43970-2058">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="43970-2059">Cmdletar har uppdaterats med den valfria parametern -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="43970-2059">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="43970-2060">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="43970-2060">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="43970-2061">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="43970-2061">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="43970-2062">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="43970-2062">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="43970-2063">Cmdleten New-AzApplicationGateway har uppdaterats med den valfria parametern -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="43970-2063">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="43970-2064">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="43970-2064">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="43970-2065">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="43970-2065">Az.OperationalInsights</span></span>
- <span data-ttu-id="43970-2066">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="43970-2066">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="43970-2067">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="43970-2067">Az.Profile</span></span>
- <span data-ttu-id="43970-2068">Modulnamnet har ändrats till Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="43970-2068">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="43970-2069">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="43970-2069">Az.RecoveryServices</span></span>
- <span data-ttu-id="43970-2070">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="43970-2070">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="43970-2071">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="43970-2071">Az.Resources</span></span>
- <span data-ttu-id="43970-2072">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="43970-2072">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="43970-2073">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="43970-2073">Az.ServiceFabric</span></span>
- <span data-ttu-id="43970-2074">Stöd för specificering av certifikat efter eget namn och tumavtryck</span><span class="sxs-lookup"><span data-stu-id="43970-2074">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="43970-2075">Information om fler icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="43970-2075">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="43970-2076">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="43970-2076">Az.SIgnalR</span></span>
- <span data-ttu-id="43970-2077">Allmän tillgänglighet för PowerShell-cmdletar för SIgnalR</span><span class="sxs-lookup"><span data-stu-id="43970-2077">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="43970-2078">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="43970-2078">Az.Sql</span></span>
- <span data-ttu-id="43970-2079">Lade till de nya identifieringstyperna Data_Exfiltration och Unsafe_Action i Threat Detection-cmdletar</span><span class="sxs-lookup"><span data-stu-id="43970-2079">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="43970-2080">Uppdaterade dokumentationsexempel för Sql Auditing-cmdletar</span><span class="sxs-lookup"><span data-stu-id="43970-2080">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="43970-2081">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="43970-2081">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="43970-2082">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="43970-2082">Az.Storage</span></span>
- <span data-ttu-id="43970-2083">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="43970-2083">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="43970-2084">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="43970-2084">Az.Websites</span></span>
- <span data-ttu-id="43970-2085">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="43970-2085">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="43970-2086">0.7.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="43970-2086">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="43970-2087">Allmänt</span><span class="sxs-lookup"><span data-stu-id="43970-2087">General</span></span>

* <span data-ttu-id="43970-2088">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="43970-2088">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="43970-2089">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="43970-2089">Az.Compute</span></span>

* <span data-ttu-id="43970-2090">Lade till stöd för UltraSSD och Galleriavbildningar i de enkla parameteruppsättningarna för `New-AzVm(ss)`-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="43970-2090">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="43970-2091">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="43970-2091">Az.DataLakeStore</span></span>

* <span data-ttu-id="43970-2092">Åtgärdade avslutande snedstreck i domänen för adls-konto</span><span class="sxs-lookup"><span data-stu-id="43970-2092">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="43970-2093">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="43970-2093">Az.FrontDoor</span></span>

* <span data-ttu-id="43970-2094">Brutna länkar korrigerades</span><span class="sxs-lookup"><span data-stu-id="43970-2094">Fixed some broken links</span></span>
    - <span data-ttu-id="43970-2095">I artiklarna New-AzureRmFrontDoor och Set-AzureRmFrontDoor artiklar korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="43970-2095">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="43970-2096">I artikeln New-AzureRmFrontDoorManagedRuleObject korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="43970-2096">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="43970-2097">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="43970-2097">Az.RecoveryServices</span></span>

* <span data-ttu-id="43970-2098">Lade till valideringar på klientsidan för Azure-filresurs med återställningsåtgärder.</span><span class="sxs-lookup"><span data-stu-id="43970-2098">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="43970-2099">Gjorde storageAccountName och storageAccountResourceGroupName valfritt för afs-återställning.</span><span class="sxs-lookup"><span data-stu-id="43970-2099">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="43970-2100">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="43970-2100">Az.Resources</span></span>

* <span data-ttu-id="43970-2101">Korrigering för https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="43970-2101">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="43970-2102">Uppdaterade Get-AzureRmRoleAssignment så att prenumerationsomfattningen används om den anges vid begäran om klassiska administratörer.</span><span class="sxs-lookup"><span data-stu-id="43970-2102">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="43970-2103">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="43970-2103">Az.Sql</span></span>

* <span data-ttu-id="43970-2104">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="43970-2104">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="43970-2105">Korrigerade ett problem med Get-AzureRmSqlDatabaseVulnerabilityAssessment med DotNet-kärna</span><span class="sxs-lookup"><span data-stu-id="43970-2105">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="43970-2106">Ändrade dokumentationen för hjälpmeddelanden som rör SQL Auditing-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="43970-2106">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="43970-2107">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="43970-2107">Az.Storage</span></span>

* <span data-ttu-id="43970-2108">Lade till -EnableHierarchicalNamespace i New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="43970-2108">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="43970-2109">Åtgärdade problemet med att cmdleten Copy File inte kunde återanvända källkontexten på målet om inte -DestContext angetts</span><span class="sxs-lookup"><span data-stu-id="43970-2109">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="43970-2110">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="43970-2110">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="43970-2111">Stöd för statisk webbplatskonfiguration</span><span class="sxs-lookup"><span data-stu-id="43970-2111">Support Static Website configuration</span></span>
    - <span data-ttu-id="43970-2112">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="43970-2112">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="43970-2113">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="43970-2113">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="43970-2114">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="43970-2114">Az.Websites</span></span>

* <span data-ttu-id="43970-2115">Set-AzureRmWebApp och Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="43970-2115">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="43970-2116">Ny parameter (-AzureStoragePath) har lagts till för att ange att Azure Storage-sökvägar ska monteras i containerappar i Windows och Linux.</span><span class="sxs-lookup"><span data-stu-id="43970-2116">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="43970-2117">Använder utdata från den nya cmdleten New-AzureRmWebAppAzureStoragePath som en parameter för att ange sökvägar för Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="43970-2117">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="43970-2118">0.6.1 – november 2018</span><span class="sxs-lookup"><span data-stu-id="43970-2118">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="43970-2119">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="43970-2119">Az.ApiManagement</span></span>
* <span data-ttu-id="43970-2120">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="43970-2120">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="43970-2121">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="43970-2121">Az.Automation</span></span>
* <span data-ttu-id="43970-2122">Swagger baserade Azure Automation-cmdletar</span><span class="sxs-lookup"><span data-stu-id="43970-2122">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="43970-2123">Cmdletar för Uppdateringshantering har lagts till</span><span class="sxs-lookup"><span data-stu-id="43970-2123">Added Update Management cmdlets</span></span>
* <span data-ttu-id="43970-2124">Cmdletar för källkontroll har lagts till</span><span class="sxs-lookup"><span data-stu-id="43970-2124">Added Source Control cmdlets</span></span>
* <span data-ttu-id="43970-2125">Remove-AzureRmAutomationHybridWorkerGroup-cmdlet har lagts till</span><span class="sxs-lookup"><span data-stu-id="43970-2125">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="43970-2126">Kommandot för DSC-registreringsnod har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="43970-2126">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="43970-2127">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="43970-2127">Az.Compute</span></span>
* <span data-ttu-id="43970-2128">Problem med SystemAssigned-identitet har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="43970-2128">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="43970-2129">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="43970-2129">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="43970-2130">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="43970-2130">Az.ContainerInstance</span></span>
* <span data-ttu-id="43970-2131">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="43970-2131">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="43970-2132">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="43970-2132">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="43970-2133">uppdatera exempelbeskrivningen för marketplace-cmdletar</span><span class="sxs-lookup"><span data-stu-id="43970-2133">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="43970-2134">Az.Network</span><span class="sxs-lookup"><span data-stu-id="43970-2134">Az.Network</span></span>
* <span data-ttu-id="43970-2135">Cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomErreller Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="43970-2135">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="43970-2136">ICMP tillbaka till stöd för Azure Firewall-nätverksprotokoll har lagts till</span><span class="sxs-lookup"><span data-stu-id="43970-2136">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="43970-2137">Uppdatera cmdlet Test-AzureRmNetworkWatcherConnectivity, lägga till verifiering av mål-id, adress och port.</span><span class="sxs-lookup"><span data-stu-id="43970-2137">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="43970-2138">Åtgärda problem med minnesanvändning i VirtualNetwork-karta</span><span class="sxs-lookup"><span data-stu-id="43970-2138">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="43970-2139">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="43970-2139">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="43970-2140">Åtgärda för att ändra principen för en skyddad fildelning.</span><span class="sxs-lookup"><span data-stu-id="43970-2140">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="43970-2141">Tidszonsprincipen har konverterats till versaler.</span><span class="sxs-lookup"><span data-stu-id="43970-2141">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="43970-2142">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="43970-2142">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="43970-2143">Exempel i New-AzureRmRecoveryServicesAsrProtectableItem har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="43970-2143">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="43970-2144">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="43970-2144">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="43970-2145">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="43970-2145">Az.Relay</span></span>
* <span data-ttu-id="43970-2146">Valfri parameter -KeyValue till New-AzureRmRelayKey cmdlet har lagts till, vilket gör det möjligt för användare att tillhandahålla KeyValue.</span><span class="sxs-lookup"><span data-stu-id="43970-2146">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="43970-2147">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="43970-2147">Az.Resources</span></span>
* <span data-ttu-id="43970-2148">Uppdatera hjälpdokumentation för resursidentitet kopplad till parametrar i `New-AzureRmPolicyAssignment` och `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="43970-2148">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="43970-2149">Lägg till ett exempel för New-AzureRmPolicyDefinition som använder -Metadata</span><span class="sxs-lookup"><span data-stu-id="43970-2149">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="43970-2150">Korrigera så att skiftläge behålls i taggnycklar i NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="43970-2150">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="43970-2151">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="43970-2151">Az.ServiceFabric</span></span>
* <span data-ttu-id="43970-2152">Lägg till utfasningsmeddelanden för kommande icke-kompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="43970-2152">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="43970-2153">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="43970-2153">Az.Sql</span></span>
* <span data-ttu-id="43970-2154">Nya cmdletar för CRUD-åtgärder på Azure Sql Database-hanterad instans och Azure Sql-hanterad databas</span><span class="sxs-lookup"><span data-stu-id="43970-2154">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="43970-2155">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="43970-2155">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="43970-2156">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="43970-2156">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="43970-2157">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="43970-2157">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="43970-2158">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="43970-2158">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="43970-2159">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="43970-2159">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="43970-2160">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="43970-2160">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="43970-2161">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="43970-2161">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="43970-2162">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="43970-2162">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="43970-2163">Hantering av utökad granskningsprincip på en server eller en databas har aktiverats.</span><span class="sxs-lookup"><span data-stu-id="43970-2163">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="43970-2164">Ny parameter (PredicateExpression) har lagts till för att aktivera filtrering av granskningsloggar.</span><span class="sxs-lookup"><span data-stu-id="43970-2164">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="43970-2165">Cmdletar har ändrats så att de använder SQL-klienter i stället för äldre klienter.</span><span class="sxs-lookup"><span data-stu-id="43970-2165">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="43970-2166">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="43970-2166">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="43970-2167">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="43970-2167">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="43970-2168">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="43970-2168">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="43970-2169">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="43970-2169">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="43970-2170">Problem med att använda Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings med lagringskontots namnparameter har korrigerats</span><span class="sxs-lookup"><span data-stu-id="43970-2170">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="43970-2171">0.5.0 – november 2018</span><span class="sxs-lookup"><span data-stu-id="43970-2171">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="43970-2172">Allmänt</span><span class="sxs-lookup"><span data-stu-id="43970-2172">General</span></span>
* <span data-ttu-id="43970-2173">Lade till resurskompletterare till många kärn-cmdletar – dessa gör att du kan stega genom befintliga resursnamn med TABB vid interaktiva anrop till cmdletar</span><span class="sxs-lookup"><span data-stu-id="43970-2173">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="43970-2174">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="43970-2174">Az.Profile</span></span>
* <span data-ttu-id="43970-2175">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="43970-2175">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="43970-2176">Bytte namn på parametern TenantId i cmdleten Connect-AzAccount till Tenant och lade till ett alias för TenantId</span><span class="sxs-lookup"><span data-stu-id="43970-2176">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="43970-2177">Uppdaterade TenantId-beskrivningen för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="43970-2177">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="43970-2178">Åtgärda felmeddelande för misslyckad inloggning när du tillhandahåller klientdomän</span><span class="sxs-lookup"><span data-stu-id="43970-2178">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="43970-2179">Åtgärda problem med att kontextnamn hamnar i konflikt för konton utan prenumerationer i klientorganisationen</span><span class="sxs-lookup"><span data-stu-id="43970-2179">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="43970-2180">Åtgärda problem med DataLake-slutpunkter vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="43970-2180">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="43970-2181">Åtgärdade problem med att Disconnect-AzAccount kastades om den inte anslöts</span><span class="sxs-lookup"><span data-stu-id="43970-2181">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="43970-2182">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="43970-2182">Az.CognitiveServices</span></span>
* <span data-ttu-id="43970-2183">Lade till åtgärden Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="43970-2183">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="43970-2184">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="43970-2184">Az.Compute</span></span>
* <span data-ttu-id="43970-2185">Lade till cmdletarna Add-AzVmssVMDataDisk och Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="43970-2185">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="43970-2186">Get-AzVMImage visar AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="43970-2186">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="43970-2187">Åtgärdade att värdena för alternativen SetAzVMChefExtension -BootstrapOptions och -JsonAttribute inte angavs i json-format.</span><span class="sxs-lookup"><span data-stu-id="43970-2187">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="43970-2188">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="43970-2188">Az.DataLakeStore</span></span>
* <span data-ttu-id="43970-2189">Uppdatera DataLake-paketet till 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="43970-2189">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="43970-2190">Lägg till standardsamtidighet för flertrådade åtgärder.</span><span class="sxs-lookup"><span data-stu-id="43970-2190">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="43970-2191">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="43970-2191">Az.Insights</span></span>
* <span data-ttu-id="43970-2192">Åtgärdade problem #7267 (autoskalningsområde)</span><span class="sxs-lookup"><span data-stu-id="43970-2192">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="43970-2193">Problem med att uppräknade parametrar inte ställdes in ordentligt när du skapade en ny autoskalningsregel (de ställdes alltid in med standardvärdet).</span><span class="sxs-lookup"><span data-stu-id="43970-2193">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="43970-2194">Åtgärdade problem #7513 [Insights] Set-AzDiagnosticSetting kräver uttrycklig specifikation av kategorier när inställningar skapas</span><span class="sxs-lookup"><span data-stu-id="43970-2194">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="43970-2195">Nu kräver inte cmdleten uttrycklig anvisning av kategorierna för att aktiveras under skapande, d.v.s. den fungerar enligt beskrivning</span><span class="sxs-lookup"><span data-stu-id="43970-2195">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="43970-2196">Az.Network</span><span class="sxs-lookup"><span data-stu-id="43970-2196">Az.Network</span></span>
* <span data-ttu-id="43970-2197">PeeringType ändrades till en obligatorisk parameter för följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="43970-2197">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="43970-2198">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="43970-2198">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="43970-2199">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="43970-2199">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="43970-2200">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="43970-2200">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="43970-2201">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="43970-2201">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="43970-2202">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="43970-2202">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="43970-2203">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="43970-2203">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="43970-2204">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="43970-2204">Az.PolicyInsights</span></span>
* <span data-ttu-id="43970-2205">Cmdletar för principreparation har lagts till</span><span class="sxs-lookup"><span data-stu-id="43970-2205">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="43970-2206">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="43970-2206">Az.Resources</span></span>
* <span data-ttu-id="43970-2207">Korrigering för https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="43970-2207">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="43970-2208">Tillåt att resurser listas med parametern -ResourceId för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="43970-2208">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="43970-2209">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="43970-2209">Az.ServiceBus</span></span>
* <span data-ttu-id="43970-2210">Skrivskyddad MigrationState-egenskap har lagts till i PSServiceBusMigrationConfigurationAttributes, som hjälper till att hålla koll på migreringstillståndet.</span><span class="sxs-lookup"><span data-stu-id="43970-2210">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="43970-2211">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="43970-2211">Az.ServiceFabric</span></span>
* <span data-ttu-id="43970-2212">Åtgärda att lägga till certifikat till Linux-Vmss.</span><span class="sxs-lookup"><span data-stu-id="43970-2212">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="43970-2213">Åtgärdade Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="43970-2213">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="43970-2214">Använd rätt tumavtryck från nya certifikat (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="43970-2214">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="43970-2215">Visa undantag korrekt (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="43970-2215">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="43970-2216">Åtgärdade Update-AzServiceFabricDurability så att klusterkonfigurationen uppdateras innan Vmss-åtgärden CreateOrUpdate påbörjas.</span><span class="sxs-lookup"><span data-stu-id="43970-2216">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="43970-2217">0.4.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="43970-2217">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="43970-2218">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="43970-2218">Az.Profile</span></span>
* <span data-ttu-id="43970-2219">Åtgärdade problemet med Get-AzSubscription i CloudShell</span><span class="sxs-lookup"><span data-stu-id="43970-2219">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="43970-2220">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="43970-2220">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="43970-2221">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="43970-2221">Az.Compute</span></span>
* <span data-ttu-id="43970-2222">Nya storlekar lades till i listan över godkända VM-storlekar för vilka accelererat nätverk kommer att aktiveras vid användning av den enkla parameteruppsättningen för New-AzVm</span><span class="sxs-lookup"><span data-stu-id="43970-2222">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="43970-2223">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="43970-2223">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="43970-2224">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="43970-2224">Az.DataLakeStore</span></span>
* <span data-ttu-id="43970-2225">Lägger till stöd för regler för virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="43970-2225">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="43970-2226">Get-AzDataLakeStoreVirtualNetworkRule: Hämtar eller listar regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="43970-2226">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="43970-2227">Add-AzDataLakeStoreVirtualNetworkRule: Lägger till en regel för virtuellt nätverk i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="43970-2227">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="43970-2228">Set-AzDataLakeStoreVirtualNetworkRule: Ändrar den angivna regeln för virtuellt nätverk i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="43970-2228">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="43970-2229">Remove-AzDataLakeStoreVirtualNetworkRule: Tar bort en regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="43970-2229">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="43970-2230">Az.Network</span><span class="sxs-lookup"><span data-stu-id="43970-2230">Az.Network</span></span>
* <span data-ttu-id="43970-2231">Skicka protokollvärdet till serverdelen för att uppdatera cmdleten Test-AzNetworkWatcherConnectivity.</span><span class="sxs-lookup"><span data-stu-id="43970-2231">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="43970-2232">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="43970-2232">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="43970-2233">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="43970-2233">Az.Resources</span></span>
* <span data-ttu-id="43970-2234">Åtgärdade problem där Get-AzRoleDefinition genererar ett oläsligt undantag (när standardprofilen inte innehåller någon prenumeration och ingen omfattning har angetts) genom att lägga till ett beskrivande undantag i scenariot.</span><span class="sxs-lookup"><span data-stu-id="43970-2234">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="43970-2235">Ställ in ”RoleDefinitionNameParameterSet” som standardparameteruppsättning.</span><span class="sxs-lookup"><span data-stu-id="43970-2235">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="43970-2236">0.3.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="43970-2236">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="43970-2237">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="43970-2237">Azure.Storage</span></span>
* <span data-ttu-id="43970-2238">Åtgärda fel där Kopiera blob/fil inte kopierar metadata när målplatsen har ett problem med metadata</span><span class="sxs-lookup"><span data-stu-id="43970-2238">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="43970-2239">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="43970-2239">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="43970-2240">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="43970-2240">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="43970-2241">Stöd för att hämta användningsinformation om en Storage-resurs för en specifik plats och för att lägga till ett varningsmeddelande för att hämta användningsinformation om en global Storage-resurs är inaktuellt.</span><span class="sxs-lookup"><span data-stu-id="43970-2241">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="43970-2242">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="43970-2242">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="43970-2243">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="43970-2243">Az.CognitiveServices</span></span>
* <span data-ttu-id="43970-2244">Stöd för Get-AzCognitiveServicesAccountSkus utan ett befintligt konto.</span><span class="sxs-lookup"><span data-stu-id="43970-2244">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="43970-2245">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="43970-2245">Az.Compute</span></span>
* <span data-ttu-id="43970-2246">Åtgärdade fel där Get-AzVM -ResourceGroupName <rg> returnerar fler än 50 resultat om det behövs</span><span class="sxs-lookup"><span data-stu-id="43970-2246">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="43970-2247">Lade till ett exempel för SimpleParameterSet i hjälpen för cmdleten New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="43970-2247">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="43970-2248">Ett stavfel i förloppsmeddelandet för Azure Disk Encryption har korrigerats</span><span class="sxs-lookup"><span data-stu-id="43970-2248">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="43970-2249">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="43970-2249">Az.DataFactoryV2</span></span>
* <span data-ttu-id="43970-2250">ADF .Net SDK-versionen har uppdaterats till 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="43970-2250">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="43970-2251">Az.Network</span><span class="sxs-lookup"><span data-stu-id="43970-2251">Az.Network</span></span>
* <span data-ttu-id="43970-2252">Funktionalitet för NetworkProfile har lagts till.</span><span class="sxs-lookup"><span data-stu-id="43970-2252">Added NetworkProfile functionality.</span></span> <span data-ttu-id="43970-2253">nya cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="43970-2253">new cmdlets added</span></span>
    - <span data-ttu-id="43970-2254">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="43970-2254">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="43970-2255">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="43970-2255">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="43970-2256">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="43970-2256">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="43970-2257">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="43970-2257">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="43970-2258">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="43970-2258">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="43970-2259">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="43970-2259">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="43970-2260">Länk för tjänstassociering på modell för undernät har lagts till</span><span class="sxs-lookup"><span data-stu-id="43970-2260">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="43970-2261">Cmdletarna New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap och Remove-AzVirtualNetworkTap har lagts till</span><span class="sxs-lookup"><span data-stu-id="43970-2261">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="43970-2262">Cmdletarna Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig och Remove-AzNEtworkInterfaceTapConfig har lagts till</span><span class="sxs-lookup"><span data-stu-id="43970-2262">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="43970-2263">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="43970-2263">Az.RedisCache</span></span>
* <span data-ttu-id="43970-2264">Tillåt att alla strängar används som storleksparametrar framöver.</span><span class="sxs-lookup"><span data-stu-id="43970-2264">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="43970-2265">Lägg till P5 i popup-fönstret PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="43970-2265">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="43970-2266">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="43970-2266">Az.Resources</span></span>
* <span data-ttu-id="43970-2267">Parametern -Mode som saknades i Set-AzPolicyDefinition har lagts till</span><span class="sxs-lookup"><span data-stu-id="43970-2267">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="43970-2268">Åtgärdade buggen för cmdleten Get-AzProviderOperation för åtgärder med ursprung som innehåller användare</span><span class="sxs-lookup"><span data-stu-id="43970-2268">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="43970-2269">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="43970-2269">Az.Sql</span></span>
* <span data-ttu-id="43970-2270">Ett problem där vissa cmdletar för säkerhetskopiering inte kunde identifiera den aktuella azure-prenumerationen har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="43970-2270">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="43970-2271">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="43970-2271">Az.Websites</span></span>
* <span data-ttu-id="43970-2272">Ny cmdlet: Get-AzWebAppContainerContinuousDeploymentUrl – Hämtar webhook-URL:en för kontinuerlig distribution av container</span><span class="sxs-lookup"><span data-stu-id="43970-2272">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="43970-2273">Nya cmdletar: New-AzWebAppContainerPSSession och Enter-WebAppContainerPSSession – Startar en PowerShell-fjärrsession i en containerapp för windows</span><span class="sxs-lookup"><span data-stu-id="43970-2273">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="43970-2274">0.2.0 – september 2018</span><span class="sxs-lookup"><span data-stu-id="43970-2274">0.2.0 - September 2018</span></span>
 <span data-ttu-id="43970-2275">Första versionen</span><span class="sxs-lookup"><span data-stu-id="43970-2275">Initial Release</span></span>
