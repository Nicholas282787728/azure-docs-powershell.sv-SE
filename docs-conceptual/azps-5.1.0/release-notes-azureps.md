---
title: Viktig information om Azure PowerShell
description: Lär dig mer om alla de senaste uppdateringarna för Azure PowerShell-modulerna.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 280486e45dad73c935f03cedc619c0de762deb12
ms.sourcegitcommit: d81c3b0f0f7289104be03869eb675128b61db7d3
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/17/2020
ms.locfileid: "94715662"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="96a62-103">Viktig information om Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="96a62-103">Azure PowerShell release notes</span></span>

## <a name="510---november-2020"></a><span data-ttu-id="96a62-104">5.1.0 – November 2020</span><span class="sxs-lookup"><span data-stu-id="96a62-104">5.1.0 - November 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="96a62-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="96a62-105">Az.Accounts</span></span>
* <span data-ttu-id="96a62-106">Korrigerade ett problem där TenantId kanske inte kan respekteras när ”Connect-AzAccount -DeviceCode” används [#13477]</span><span class="sxs-lookup"><span data-stu-id="96a62-106">Fixed an issue that TenantId may be not respected if using 'Connect-AzAccount -DeviceCode'[#13477]</span></span>
* <span data-ttu-id="96a62-107">Lade till en ny cmdlet: ”Get-AzAccessToken”</span><span class="sxs-lookup"><span data-stu-id="96a62-107">Added new cmdlet 'Get-AzAccessToken'</span></span>
* <span data-ttu-id="96a62-108">Korrigerade ett problem som uppstår om det inte går att komma åt sökvägen till användarprofilen</span><span class="sxs-lookup"><span data-stu-id="96a62-108">Fixed an issue that error happens if user profile path is inaccessible</span></span>
* <span data-ttu-id="96a62-109">Korrigerade ett problem som orsakar ett skriv-objektfel under Connect-AzAccount [#13419]</span><span class="sxs-lookup"><span data-stu-id="96a62-109">Fixed an issue causing Write-Object error during Connect-AzAccount [#13419]</span></span>
* <span data-ttu-id="96a62-110">Lade till parametern ”ContainerRegistryEndpointSuffix” för: ”Add-AzEnvironment”, ”Set-AzEnvironment”</span><span class="sxs-lookup"><span data-stu-id="96a62-110">Added parameter 'ContainerRegistryEndpointSuffix' to: 'Add-AzEnvironment', 'Set-AzEnvironment'</span></span> 
* <span data-ttu-id="96a62-111">Stöd för att avbryta inloggning genom att trycka på <kbd>CTRL</kbd>+<kbd>C</kbd></span><span class="sxs-lookup"><span data-stu-id="96a62-111">Supported interrupting login by hitting <kbd>CTRL</kbd>+<kbd>C</kbd></span></span>
* <span data-ttu-id="96a62-112">Korrigerade ett problem som gjorde att ”Connect-AzAccount -KeyVaultAccessToken” inte fungerade [#13127]</span><span class="sxs-lookup"><span data-stu-id="96a62-112">Fixed an issue causing 'Connect-AzAccount -KeyVaultAccessToken' not working [#13127]</span></span>
* <span data-ttu-id="96a62-113">Korrigerade null-referens och skiftlägesokänslig metod i ”Invoke-AzRestMethod”</span><span class="sxs-lookup"><span data-stu-id="96a62-113">Fixed null reference and method case insensitive in 'Invoke-AzRestMethod'</span></span>

#### <a name="azaks"></a><span data-ttu-id="96a62-114">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="96a62-114">Az.Aks</span></span>
* <span data-ttu-id="96a62-115">Korrigerade problemet att användaren inte kunde använda tjänstens huvudnamn för att skapa ett nytt Kubernetes-kluster.</span><span class="sxs-lookup"><span data-stu-id="96a62-115">Fixed the issue that user cannot use service principal to create a new Kubernetes cluster.</span></span> <span data-ttu-id="96a62-116">[#13012]</span><span class="sxs-lookup"><span data-stu-id="96a62-116">[#13012]</span></span>

#### <a name="azappconfiguration"></a><span data-ttu-id="96a62-117">Az.AppConfiguration</span><span class="sxs-lookup"><span data-stu-id="96a62-117">Az.AppConfiguration</span></span>
* <span data-ttu-id="96a62-118">Allmän tillgänglighet för modulen ”Az.AppConfiguration”</span><span class="sxs-lookup"><span data-stu-id="96a62-118">General availability of 'Az.AppConfiguration' module</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="96a62-119">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="96a62-119">Az.DataFactory</span></span>
* <span data-ttu-id="96a62-120">Förbättrade felmeddelandet för kommandot ”New-AzDataFactoryV2LinkedServiceEncryptedCredential”</span><span class="sxs-lookup"><span data-stu-id="96a62-120">Improved error message of 'New-AzDataFactoryV2LinkedServiceEncryptedCredential' command</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="96a62-121">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="96a62-121">Az.DataLakeStore</span></span>
* <span data-ttu-id="96a62-122">Uppdaterade SDK för ADLS-dataplanen till 1.2.4-alpha.</span><span class="sxs-lookup"><span data-stu-id="96a62-122">Updated ADLS dataplane SDK to 1.2.4-alpha.</span></span> <span data-ttu-id="96a62-123">Ändringar: https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-124-alpha</span><span class="sxs-lookup"><span data-stu-id="96a62-123">Changes:https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-124-alpha</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="96a62-124">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="96a62-124">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="96a62-125">Lade till nya cmdletar för MSIX-paket och uppdaterade program-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="96a62-125">Added new MSIX Package cmdlets and updated Applications cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="96a62-126">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="96a62-126">Az.EventHub</span></span>
* <span data-ttu-id="96a62-127">Korrigerade klusterkommandon för EventHub-kluster utan taggar</span><span class="sxs-lookup"><span data-stu-id="96a62-127">Fixed Cluster commands for EventHub cluster without tags</span></span>
* <span data-ttu-id="96a62-128">Uppdaterade hjälptext för PartnerNamespace i AzEventHubGeoDRConfiguration-kommandon</span><span class="sxs-lookup"><span data-stu-id="96a62-128">Updated help text for PartnerNamespace of AzEventHubGeoDRConfiguration commands</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="96a62-129">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="96a62-129">Az.HDInsight</span></span>
* <span data-ttu-id="96a62-130">Lade till parametrarna ”ResourceProviderConnection” och ”PrivateLink” till cmdleten ”New-AzHDInsightCluster” för att stödja funktionen för att vidarebefordra utgående och privata länkar</span><span class="sxs-lookup"><span data-stu-id="96a62-130">Add parameters 'ResourceProviderConnection' and 'PrivateLink' to cmdlet 'New-AzHDInsightCluster' to support relay outbound and private link feature</span></span>
* <span data-ttu-id="96a62-131">Lade till parametern ”AmbariDatabase” till cmdleten ”New-AzHDInsightCluster” för att stödja en anpassad Ambari-databasfunktion</span><span class="sxs-lookup"><span data-stu-id="96a62-131">Add parameter 'AmbariDatabase' to cmdlet 'New-AzHDInsightCluster' to support custom Ambari database feature</span></span>
* <span data-ttu-id="96a62-132">Lade till det accepterade värdet ”AmbariDatabase” till parametern ”MetastoreType” för cmdleten ”Add-AzHDInsightMetastore”</span><span class="sxs-lookup"><span data-stu-id="96a62-132">Add accept value 'AmbariDatabase' to the parameter 'MetastoreType' of the cmdlet 'Add-AzHDInsightMetastore'</span></span>

#### <a name="aziothub"></a><span data-ttu-id="96a62-133">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="96a62-133">Az.IotHub</span></span>
* <span data-ttu-id="96a62-134">Tillät taggar i cmdlet för att skapa i IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="96a62-134">Allowed tags in IoT Hub create cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="96a62-135">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="96a62-135">Az.KeyVault</span></span>
* <span data-ttu-id="96a62-136">Stöd för att uppdatera nyckelvalvstagg</span><span class="sxs-lookup"><span data-stu-id="96a62-136">Supported updating key vault tag</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="96a62-137">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="96a62-137">Az.LogicApp</span></span>
* <span data-ttu-id="96a62-138">Korrigerade så att Get-AzLogicAppRunHistory endast hämtar den första sidan med resultat</span><span class="sxs-lookup"><span data-stu-id="96a62-138">Fixed for Get-AzLogicAppRunHistory only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="96a62-139">Az.Network</span><span class="sxs-lookup"><span data-stu-id="96a62-139">Az.Network</span></span>
* <span data-ttu-id="96a62-140">Uppdaterade cmdletarna här under</span><span class="sxs-lookup"><span data-stu-id="96a62-140">Updated below cmdlet</span></span> 
    - <span data-ttu-id="96a62-141">”New-AzLoadBalancerFrontendIpConfigCommand”, ”Set-AzLoadBalancerFrontendIpConfigCommand”, ”Add-AzLoadBalancerFrontendIpConfigCommand”:</span><span class="sxs-lookup"><span data-stu-id="96a62-141">'New-AzLoadBalancerFrontendIpConfigCommand', 'Set-AzLoadBalancerFrontendIpConfigCommand', 'Add-AzLoadBalancerFrontendIpConfigCommand':</span></span>
        - <span data-ttu-id="96a62-142">Lade till egenskapen PublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="96a62-142">Added PublicIpAddressPrefix property</span></span>
        - <span data-ttu-id="96a62-143">Lade till egenskapen PublicIpAddressPrefixId</span><span class="sxs-lookup"><span data-stu-id="96a62-143">Added PublicIpAddressPrefixId property</span></span>
* <span data-ttu-id="96a62-144">Lade till nya egenskaper till i följande cmdletar för att möjliggöra global belastningsutjämning:</span><span class="sxs-lookup"><span data-stu-id="96a62-144">Added new properties to the following cmdlets to allow for global load balancing</span></span>
    - <span data-ttu-id="96a62-145">”New-AzLoadBalancer”:</span><span class="sxs-lookup"><span data-stu-id="96a62-145">'New-AzLoadBalancer':</span></span>
        - <span data-ttu-id="96a62-146">Lade till egenskapen SKU-nivå</span><span class="sxs-lookup"><span data-stu-id="96a62-146">Added Sku Tier property</span></span>
    - <span data-ttu-id="96a62-147">”New-AzPuplicIpAddress”:</span><span class="sxs-lookup"><span data-stu-id="96a62-147">'New-AzPuplicIpAddress':</span></span>
        - <span data-ttu-id="96a62-148">Lade till egenskapen SKU-nivå</span><span class="sxs-lookup"><span data-stu-id="96a62-148">Added Sku Tier property</span></span>
    - <span data-ttu-id="96a62-149">”New-AzPublicIpPrefix”:</span><span class="sxs-lookup"><span data-stu-id="96a62-149">'New-AzPublicIpPrefix':</span></span>
        - <span data-ttu-id="96a62-150">Lade till egenskapen SKU-nivå</span><span class="sxs-lookup"><span data-stu-id="96a62-150">Added Sku Tier property</span></span>
    - <span data-ttu-id="96a62-151">”New-AzLoadBalancerBackendAddressConfig”:</span><span class="sxs-lookup"><span data-stu-id="96a62-151">'New-AzLoadBalancerBackendAddressConfig':</span></span>
        - <span data-ttu-id="96a62-152">Lade till egenskapen LoadBalancerFrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="96a62-152">Added LoadBalancerFrontendIPConfigurationId property</span></span>
* <span data-ttu-id="96a62-153">Uppdaterade planer att göra varningar för följande cmdletar inaktuella: -”New-AzVirtualHubRoute”, -”New-AzVirtualHubRouteTable”, -”Add-AzVirtualHubRoute”, -”Add-AzVirtualHubRouteTable” -”Get-AzVirtualHubRouteTable” och -”Remove-AzVirtualHubRouteTable”</span><span class="sxs-lookup"><span data-stu-id="96a62-153">Updated planning to deprecate warnings for the following cmdlets   -'New-AzVirtualHubRoute'   -'New-AzVirtualHubRouteTable'   -'Add-AzVirtualHubRoute'   -'Add-AzVirtualHubRouteTable'   -'Get-AzVirtualHubRouteTable'   -'Remove-AzVirtualHubRouteTable'</span></span>
* <span data-ttu-id="96a62-154">Lade till planer att göra varningar för argumentet ”RouteTable” inaktuella för följande cmdletar: -”New-AzVirtualHub”, -”Set-AzVirtualHub” och -”Update-AzVirtualHub”</span><span class="sxs-lookup"><span data-stu-id="96a62-154">Added planning to deprecate warnings on the argument 'RouteTable' for the following cmdlets   -'New-AzVirtualHub'   -'Set-AzVirtualHub'   -'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="96a62-155">Gjorde argumenten ”-MinScaleUnits” och ”-MaxScaleUnits” valfria i ”Set-AzExpressRouteGateway”</span><span class="sxs-lookup"><span data-stu-id="96a62-155">Made arguments '-MinScaleUnits' and '-MaxScaleUnits' optional in 'Set-AzExpressRouteGateway'</span></span>
* <span data-ttu-id="96a62-156">Lade till nya cmdletar för att stödja ömsesidig autentisering och SSL-profiler på Application Gateway</span><span class="sxs-lookup"><span data-stu-id="96a62-156">Added new cmdlets to support Mutual Authentication and SSL Profiles on Application Gateway</span></span>
    - <span data-ttu-id="96a62-157">”Get-AzApplicationGatewayClientAuthConfiguration”</span><span class="sxs-lookup"><span data-stu-id="96a62-157">'Get-AzApplicationGatewayClientAuthConfiguration'</span></span>
    - <span data-ttu-id="96a62-158">”New-AzApplicationGatewayClientAuthConfiguration”</span><span class="sxs-lookup"><span data-stu-id="96a62-158">'New-AzApplicationGatewayClientAuthConfiguration'</span></span>
    - <span data-ttu-id="96a62-159">”Remove-AzApplicationGatewayClientAuthConfiguration”</span><span class="sxs-lookup"><span data-stu-id="96a62-159">'Remove-AzApplicationGatewayClientAuthConfiguration'</span></span>
    - <span data-ttu-id="96a62-160">”Set-AzApplicationGatewayClientAuthConfiguration”</span><span class="sxs-lookup"><span data-stu-id="96a62-160">'Set-AzApplicationGatewayClientAuthConfiguration'</span></span>
    - <span data-ttu-id="96a62-161">”Add-AzApplicationGatewayTrustedClientCertificate”</span><span class="sxs-lookup"><span data-stu-id="96a62-161">'Add-AzApplicationGatewayTrustedClientCertificate'</span></span> 
    - <span data-ttu-id="96a62-162">”Get-AzApplicationGatewayTrustedClientCertificate”</span><span class="sxs-lookup"><span data-stu-id="96a62-162">'Get-AzApplicationGatewayTrustedClientCertificate'</span></span> 
    - <span data-ttu-id="96a62-163">”New-AzApplicationGatewayTrustedClientCertificate”</span><span class="sxs-lookup"><span data-stu-id="96a62-163">'New-AzApplicationGatewayTrustedClientCertificate'</span></span> 
    - <span data-ttu-id="96a62-164">”Remove-AzApplicationGatewayTrustedClientCertificate”</span><span class="sxs-lookup"><span data-stu-id="96a62-164">'Remove-AzApplicationGatewayTrustedClientCertificate'</span></span> 
    - <span data-ttu-id="96a62-165">”Set-AzApplicationGatewayTrustedClientCertificate”</span><span class="sxs-lookup"><span data-stu-id="96a62-165">'Set-AzApplicationGatewayTrustedClientCertificate'</span></span>
    - <span data-ttu-id="96a62-166">”Add-AzApplicationGatewaySslProfile”</span><span class="sxs-lookup"><span data-stu-id="96a62-166">'Add-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="96a62-167">”Get-AzApplicationGatewaySslProfile”</span><span class="sxs-lookup"><span data-stu-id="96a62-167">'Get-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="96a62-168">”New-AzApplicationGatewaySslProfile”</span><span class="sxs-lookup"><span data-stu-id="96a62-168">'New-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="96a62-169">”Remove-AzApplicationGatewaySslProfile”</span><span class="sxs-lookup"><span data-stu-id="96a62-169">'Remove-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="96a62-170">”Set-AzApplicationGatewaySslProfile”</span><span class="sxs-lookup"><span data-stu-id="96a62-170">'Set-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="96a62-171">”Get-AzApplicationGatewaySslProfilePolicy”</span><span class="sxs-lookup"><span data-stu-id="96a62-171">'Get-AzApplicationGatewaySslProfilePolicy'</span></span>
    - <span data-ttu-id="96a62-172">”Remove-AzApplicationGatewaySslProfilePolicy”</span><span class="sxs-lookup"><span data-stu-id="96a62-172">'Remove-AzApplicationGatewaySslProfilePolicy'</span></span>
    - <span data-ttu-id="96a62-173">”Set-AzApplicationGatewaySslProfilePolicy”</span><span class="sxs-lookup"><span data-stu-id="96a62-173">'Set-AzApplicationGatewaySslProfilePolicy'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="96a62-174">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="96a62-174">Az.RecoveryServices</span></span>
* <span data-ttu-id="96a62-175">Specificera att principen BackupTime är i UTC.</span><span class="sxs-lookup"><span data-stu-id="96a62-175">Specifying policy BackupTime is in UTC.</span></span>
* <span data-ttu-id="96a62-176">Ändra varning för icke-bakåtkompatibel ändring i cmdleten Get-AzRecoveryServicesBackupJobDetails.</span><span class="sxs-lookup"><span data-stu-id="96a62-176">Modifying breaking change warning in Get-AzRecoveryServicesBackupJobDetails cmdlet.</span></span>
* <span data-ttu-id="96a62-177">Uppdaterar exempelskriptets hjälptext för cmdleten Set-AzRecoveryServicesBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="96a62-177">Updating sample script help text for Set-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="96a62-178">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="96a62-178">Az.Resources</span></span>
* <span data-ttu-id="96a62-179">Korrigerade ett problem där konsekvensgranskning visade två omfång för resursgrupper med olika skiftlägen</span><span class="sxs-lookup"><span data-stu-id="96a62-179">Fixed an issue where What-If shows two resource group scopes with different casing</span></span>
* <span data-ttu-id="96a62-180">Uppdaterade ”Export-AzResourceGroup” för att använda SDK.</span><span class="sxs-lookup"><span data-stu-id="96a62-180">Updated 'Export-AzResourceGroup' to use the SDK.</span></span>
* <span data-ttu-id="96a62-181">Lade till kulturinformation för att parsa metoder</span><span class="sxs-lookup"><span data-stu-id="96a62-181">Added culture info to parse methods</span></span>

#### <a name="azsql"></a><span data-ttu-id="96a62-182">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="96a62-182">Az.Sql</span></span>
* <span data-ttu-id="96a62-183">Korrigerade problem där Set-AzSqlDatabaseAudit inte hade stöd för databas i hyperskala och databasversionen inte kunde fastställas</span><span class="sxs-lookup"><span data-stu-id="96a62-183">Fixed issues where Set-AzSqlDatabaseAudit were not support Hyperscale database and database edition cannot be determined</span></span>
* <span data-ttu-id="96a62-184">Lade till MaintenanceConfigurationId för ”New-AzSqlInstance” och ”Set-AzSqlInstance”</span><span class="sxs-lookup"><span data-stu-id="96a62-184">Added MaintenanceConfigurationId to 'New-AzSqlInstance' and 'Set-AzSqlInstance'</span></span>
* <span data-ttu-id="96a62-185">Korrigerade en bugg i GetAzureSqlDatabaseReplicationLink.cs där parametern PartnerServerName kontrollerades efter värde i stället för nyckel</span><span class="sxs-lookup"><span data-stu-id="96a62-185">Fixed a bug in GetAzureSqlDatabaseReplicationLink.cs where PartnerServerName parameter was being checked for by value instead of key</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="96a62-186">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="96a62-186">Az.Websites</span></span>
* <span data-ttu-id="96a62-187">Lade till stöd för nya funktioner för åtkomstbegränsning: ServiceTag, flera IP-adresser och HTTP-rubriker</span><span class="sxs-lookup"><span data-stu-id="96a62-187">Added support for new access restriction features: ServiceTag, multi-ip and http-headers</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="96a62-188">Tack till våra community-deltagare</span><span class="sxs-lookup"><span data-stu-id="96a62-188">Thanks to our community contributors</span></span>
* <span data-ttu-id="96a62-189">John Q. Martin (@johnmart82), lägger till nödvändig brandväggsinformation (#13385)</span><span class="sxs-lookup"><span data-stu-id="96a62-189">John Q. Martin (@johnmart82), Adding firewall prerequisite information (#13385)</span></span>
* <span data-ttu-id="96a62-190">Manikandan Duraisamy (@madurais-msft), korrigerade argumentet PublicSubnetName (#13417)</span><span class="sxs-lookup"><span data-stu-id="96a62-190">Manikandan Duraisamy (@madurais-msft), Corrected the PublicSubnetName argument (#13417)</span></span>
* <span data-ttu-id="96a62-191">@mahortas, uppdatera parametervärden för -HostName (#13349)</span><span class="sxs-lookup"><span data-stu-id="96a62-191">@mahortas, Update for -HostNames parameter values (#13349)</span></span>
* <span data-ttu-id="96a62-192">@MariachiForHire, lade till TrafficAnalyticsInterval-värden som stöds (#13304)</span><span class="sxs-lookup"><span data-stu-id="96a62-192">@MariachiForHire, added supported TrafficAnalyticsInterval values (#13304)</span></span>
* <span data-ttu-id="96a62-193">Michael Jonas (@mikejwhat), tillåt att Get-AzLogicAppRunHistory returnerar fler än 30 poster (#13393)</span><span class="sxs-lookup"><span data-stu-id="96a62-193">Michael James (@mikejwhat), Allow Get-AzLogicAppRunHistory to return more than 30 entries (#13393)</span></span>
* <span data-ttu-id="96a62-194">Shashikant Shakya (@shshakya), uppdatera Restore-AzSqlInstanceDatabase.md (#13404)</span><span class="sxs-lookup"><span data-stu-id="96a62-194">Shashikant Shakya (@shshakya), Update Restore-AzSqlInstanceDatabase.md (#13404)</span></span>

## <a name="500---october-2020"></a><span data-ttu-id="96a62-195">5.0.0 – Oktober 2020</span><span class="sxs-lookup"><span data-stu-id="96a62-195">5.0.0 - October 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="96a62-196">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="96a62-196">Az.Accounts</span></span>
* <span data-ttu-id="96a62-197">[Icke-bakåtkompatibel ändring] Tog bort ”Get-AzProfile” och ”Select-AzProfile”</span><span class="sxs-lookup"><span data-stu-id="96a62-197">[Breaking Change] Removed 'Get-AzProfile' and 'Select-AzProfile'</span></span>
* <span data-ttu-id="96a62-198">Ersatte Azure Directory Authentication Library med Microsoft Authentication Library (MSAL)</span><span class="sxs-lookup"><span data-stu-id="96a62-198">Replaced Azure Directory Authentication Library with Microsoft Authentication Library(MSAL)</span></span>

#### <a name="azaks"></a><span data-ttu-id="96a62-199">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="96a62-199">Az.Aks</span></span>
* <span data-ttu-id="96a62-200">[Icke-bakåtkompatibel ändring] Tog bort aliaset ”ClientIdAndSecret” i ”New-AzAksCluster” och ”Set-AzAksCluster”.</span><span class="sxs-lookup"><span data-stu-id="96a62-200">[Breaking Change] Removed parameter alias 'ClientIdAndSecret' in 'New-AzAksCluster' and 'Set-AzAksCluster'.</span></span>
* <span data-ttu-id="96a62-201">[Icke-bakåtkompatibel ändring] Ändrade standardvärdet för ”NodeVmSetType” i ”New-AzAksCluster” från ”AvailabilitySet” till ”VirtualMachineScaleSets”.</span><span class="sxs-lookup"><span data-stu-id="96a62-201">[Breaking Change] Changed the default value of 'NodeVmSetType' in 'New-AzAksCluster' from 'AvailabilitySet' to 'VirtualMachineScaleSets'.</span></span>
* <span data-ttu-id="96a62-202">[Icke-bakåtkompatibel ändring] Ändrade standardvärdet för ”NetworkPlugin” i ”New-AzAksCluster” från ”None” till ”azure”.</span><span class="sxs-lookup"><span data-stu-id="96a62-202">[Breaking Change] Changed the default value of 'NetworkPlugin' in 'New-AzAksCluster' from 'None' to 'azure'.</span></span>
* <span data-ttu-id="96a62-203">[Icke-bakåtkompatibel ändring] Tog bort parametern ”NodeOsType” i ”New-AzAksCluster” eftersom den endast har stöd för Linux med ett värde.</span><span class="sxs-lookup"><span data-stu-id="96a62-203">[Breaking Change] Removed parameter 'NodeOsType' in 'New-AzAksCluster' as it supports only one value Linux.</span></span>

#### <a name="azbilling"></a><span data-ttu-id="96a62-204">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="96a62-204">Az.Billing</span></span>
* <span data-ttu-id="96a62-205">Lade till cmdleten ”Get-AzBillingAccount”</span><span class="sxs-lookup"><span data-stu-id="96a62-205">Added 'Get-AzBillingAccount' cmdlet</span></span>
* <span data-ttu-id="96a62-206">Lade till cmdleten ”Get-AzBillingProfile”</span><span class="sxs-lookup"><span data-stu-id="96a62-206">Added 'Get-AzBillingProfile' cmdlet</span></span>
* <span data-ttu-id="96a62-207">Lade till cmdleten ”Get-AzInvoiceSection”</span><span class="sxs-lookup"><span data-stu-id="96a62-207">Added 'Get-AzInvoiceSection' cmdlet</span></span>
* <span data-ttu-id="96a62-208">Lade till nya parametrar i cmdleten ”Get-AzBillingInvoice”</span><span class="sxs-lookup"><span data-stu-id="96a62-208">Added new parameters in 'Get-AzBillingInvoice' cmdlet</span></span>
* <span data-ttu-id="96a62-209">Tog bort egenskaperna ”DownloadUrlExpiry”, ”Type” och ”BillingPeriodNames” från svaret för cmdleten ”Get-AzBillingInvoic”</span><span class="sxs-lookup"><span data-stu-id="96a62-209">Removed properties DownloadUrlExpiry, Type, BillingPeriodNames from the response of Get-AzBillingInvoice cmdlet</span></span>

#### <a name="azcdn"></a><span data-ttu-id="96a62-210">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="96a62-210">Az.Cdn</span></span>
* <span data-ttu-id="96a62-211">Lade till cmdletar för att stödja funktioner för flera ursprung och privat länk</span><span class="sxs-lookup"><span data-stu-id="96a62-211">Added cmdlets to support multi-origin and private link functionality</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="96a62-212">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="96a62-212">Az.CognitiveServices</span></span>
* <span data-ttu-id="96a62-213">Uppdaterade SDK till 7.4.0-preview.</span><span class="sxs-lookup"><span data-stu-id="96a62-213">Updated SDK to 7.4.0-preview.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="96a62-214">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="96a62-214">Az.Compute</span></span>
* <span data-ttu-id="96a62-215">Lade till parametern ”-VmssId” till ”New-AzVm”</span><span class="sxs-lookup"><span data-stu-id="96a62-215">Added '-VmssId' parameter to 'New-AzVm'</span></span>
* <span data-ttu-id="96a62-216">Lade till parametern ”PlatformFaultDomainCount” till cmdleten ”New-AzVmss”.</span><span class="sxs-lookup"><span data-stu-id="96a62-216">Added 'PlatformFaultDomainCount' parameter to the 'New-AzVmss' cmdlet.</span></span>
* <span data-ttu-id="96a62-217">Ny cmdlet: ”Get-AzDiskEncryptionSetAssociatedResource”</span><span class="sxs-lookup"><span data-stu-id="96a62-217">New cmdlet 'Get-AzDiskEncryptionSetAssociatedResource'</span></span>
* <span data-ttu-id="96a62-218">Lade till de valfria parametrarna ”Tier” och ”LogicalSectorSize” till cmdleten ”New-AzDiskConfig”.</span><span class="sxs-lookup"><span data-stu-id="96a62-218">Added 'Tier' and 'LogicalSectorSize' optional parameters to the New-AzDiskConfig cmdlet.</span></span> 
* <span data-ttu-id="96a62-219">Lade till de valfria parametrarna ”Tier”, ”MaxSharesCount”, ”DiskIOPSReadOnly” och ”DiskMBpsReadOnly” till cmdleten ”New-AzDiskUpdateConfig”.</span><span class="sxs-lookup"><span data-stu-id="96a62-219">Added 'Tier', 'MaxSharesCount', 'DiskIOPSReadOnly', and 'DiskMBpsReadOnly' optional parameters to the 'New-AzDiskUpdateConfig' cmdlet.</span></span> 

#### <a name="azcontainerregistry"></a><span data-ttu-id="96a62-220">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="96a62-220">Az.ContainerRegistry</span></span>
* <span data-ttu-id="96a62-221">[Icke-bakåtkompatibel ändring] Uppdaterar API-versionen till 2019-05-01</span><span class="sxs-lookup"><span data-stu-id="96a62-221">[Breaking Change] Updates API version to 2019-05-01</span></span>
* <span data-ttu-id="96a62-222">[Icke-bakåtkompatibel ändring] Tog bort SKU:n ”Classic” och parametern ”StorageAccountName” från ”New-AzContainerRegistry”</span><span class="sxs-lookup"><span data-stu-id="96a62-222">[Breaking Change] Removed SKU 'Classic' and parameter 'StorageAccountName' from 'New-AzContainerRegistry'</span></span>
* <span data-ttu-id="96a62-223">Lade till nya cmdletar: ”Connect-AzContainerRegistry”, ”Import-AzContainerRegistry”, ”Get-AzContainerRegistryUsage”, ”New-AzContainerRegistryNetworkRule”, ”Set-AzContainerRegistryNetworkRule”</span><span class="sxs-lookup"><span data-stu-id="96a62-223">Added New cmdlets: 'Connect-AzContainerRegistry', 'Import-AzContainerRegistry', 'Get-AzContainerRegistryUsage', 'New-AzContainerRegistryNetworkRule', 'Set-AzContainerRegistryNetworkRule'</span></span>
* <span data-ttu-id="96a62-224">Lade till den nya parametern ”NetworkRuleSet” till ”Update-AzContainerRegistry”</span><span class="sxs-lookup"><span data-stu-id="96a62-224">Added new parameter 'NetworkRuleSet' to 'Update-AzContainerRegistry'</span></span>

#### <a name="azdatabricks"></a><span data-ttu-id="96a62-225">Az.Databricks</span><span class="sxs-lookup"><span data-stu-id="96a62-225">Az.Databricks</span></span>
* <span data-ttu-id="96a62-226">Korrigerade en bugg som kunde leda till att en uppdatering av en Databricks-arbetsyta utan `-EncryptionKeyVersion` misslyckades.</span><span class="sxs-lookup"><span data-stu-id="96a62-226">Fixed a bug that may cause updating databricks workspace without `-EncryptionKeyVersion` to fail.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="96a62-227">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="96a62-227">Az.DataFactory</span></span>
* <span data-ttu-id="96a62-228">Uppdaterade ADF .Net SDK-versionen till 4.12.0</span><span class="sxs-lookup"><span data-stu-id="96a62-228">Updated ADF .Net SDK version to 4.12.0</span></span>
* <span data-ttu-id="96a62-229">Uppdaterade ADF-krypteringsklientens SDK-version till 4.14.7587.7</span><span class="sxs-lookup"><span data-stu-id="96a62-229">Updated ADF encryption client SDK version to 4.14.7587.7</span></span>
* <span data-ttu-id="96a62-230">Lade till kommandona ”Stop-AzDataFactoryV2TriggerRun” och ”Invoke-AzDataFactoryV2TriggerRun”</span><span class="sxs-lookup"><span data-stu-id="96a62-230">Added 'Stop-AzDataFactoryV2TriggerRun' and 'Invoke-AzDataFactoryV2TriggerRun' commands</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="96a62-231">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="96a62-231">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="96a62-232">Kräv egenskapen Plats för att skapa ARM-objekt på högsta nivån.</span><span class="sxs-lookup"><span data-stu-id="96a62-232">Require Location property for creating top level arm objects.</span></span>
        <span data-ttu-id="96a62-233">\* Gjorde så att `ApplicationGroupType` krävs för `New-AzWvdApplicationGroup`.</span><span class="sxs-lookup"><span data-stu-id="96a62-233">\* Made `ApplicationGroupType` required for `New-AzWvdApplicationGroup`.</span></span>
        <span data-ttu-id="96a62-234">\* Gjorde så att `HostPoolArmPath` krävs för `New-AzWvdApplicationGroup`.</span><span class="sxs-lookup"><span data-stu-id="96a62-234">\* Made `HostPoolArmPath` required for `New-AzWvdApplicationGroup`.</span></span>
        <span data-ttu-id="96a62-235">\* `PreferredAppGroupType` har lagts till för `New-AzWvdHostPool`.</span><span class="sxs-lookup"><span data-stu-id="96a62-235">\* Added `PreferredAppGroupType` for `New-AzWvdHostPool`.</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="96a62-236">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="96a62-236">Az.Functions</span></span>
* <span data-ttu-id="96a62-237">[Icke-bakåtkompatibel ändring] Tog bort växelparametern ”IncludeSlot” från alla förutom en parameteruppsättning i ”Get-AzFunctionApp”.</span><span class="sxs-lookup"><span data-stu-id="96a62-237">[Breaking Change] Removed 'IncludeSlot' switch parameter from all but one parameter set of 'Get-AzFunctionApp'.</span></span> <span data-ttu-id="96a62-238">Cmdleten stöder nu hämtning av distributionsfack i resultaten när ”-IncludeSlot” anges.</span><span class="sxs-lookup"><span data-stu-id="96a62-238">The cmdlet now supports retrieving deployment slots in the results when '-IncludeSlot' is specified.</span></span> 
* <span data-ttu-id="96a62-239">Uppdaterade ”New-AzFunctionApp”:</span><span class="sxs-lookup"><span data-stu-id="96a62-239">Updated 'New-AzFunctionApp':</span></span>
  - <span data-ttu-id="96a62-240">Korrigerade ”-DisableApplicationInsights” så att inga Application Insights-projekt skapas när det här alternativet har angetts.</span><span class="sxs-lookup"><span data-stu-id="96a62-240">Fixed -DisableApplicationInsights so that no application insights project is created when this option is specified.</span></span> <span data-ttu-id="96a62-241">[#12728]</span><span class="sxs-lookup"><span data-stu-id="96a62-241">[#12728]</span></span>
  - <span data-ttu-id="96a62-242">[Icke-bakåtkompatibel ändring] Tog bort stöd för att skapa PowerShell 6.2-funktionsappar.</span><span class="sxs-lookup"><span data-stu-id="96a62-242">[Breaking Change] Removed support to create PowerShell 6.2 function apps.</span></span>
  - <span data-ttu-id="96a62-243">[Icke-bakåtkompatibel ändring] Ändrade körningsversionen som är standard i Functions version 3 i Windows för PowerShell-funktionsappar från 6.2 till 7.0 när parametern RuntimeVersion inte har angetts.</span><span class="sxs-lookup"><span data-stu-id="96a62-243">[Breaking Change] Changed the default runtime version in Functions version 3 on Windows for PowerShell function apps from 6.2 to 7.0 when the RuntimeVersion parameter is not specified.</span></span>
  - <span data-ttu-id="96a62-244">[Icke-bakåtkompatibel ändring] Ändrade körningsversionen som är standard i Functions version 3 i Windows och Linux för Node-funktionsappar från 10 till 12 när parametern RuntimeVersion inte har angetts.</span><span class="sxs-lookup"><span data-stu-id="96a62-244">[Breaking Change] Changed the default runtime version in Functions version 3 on Windows and Linux for Node function apps from 10 to 12 when the RuntimeVersion parameter is not specified.</span></span>
  - <span data-ttu-id="96a62-245">[Icke-bakåtkompatibel ändring] Ändrade körningsversionen som är standard i Functions version 3 i Linux för Python-funktionsappar från 3.7 till 3.8 när parametern RuntimeVersion inte har angetts.</span><span class="sxs-lookup"><span data-stu-id="96a62-245">[Breaking Change] Changed the default runtime version in Functions version 3 on Linux for Python function apps from 3.7 to 3.8 when the RuntimeVersion parameter is not specified.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="96a62-246">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="96a62-246">Az.HDInsight</span></span>
 * <span data-ttu-id="96a62-247">För cmdleten New-AzHDInsightCluster:</span><span class="sxs-lookup"><span data-stu-id="96a62-247">For New-AzHDInsightCluster cmdlet:</span></span>
     - <span data-ttu-id="96a62-248">Ersatte parametern ”DefaultStorageAccountName” med ”StorageAccountResourceId”</span><span class="sxs-lookup"><span data-stu-id="96a62-248">Replaced parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
     - <span data-ttu-id="96a62-249">Ersatte parametern ”DefaultStorageAccountKey” med ”StorageAccountKey”</span><span class="sxs-lookup"><span data-stu-id="96a62-249">Replaced parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
     - <span data-ttu-id="96a62-250">Ersatte parametern ”DefaultStorageAccountType” med ”StorageAccountType”</span><span class="sxs-lookup"><span data-stu-id="96a62-250">Replaced parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
     - <span data-ttu-id="96a62-251">Tog bort parametern ”PublicNetworkAccessType”</span><span class="sxs-lookup"><span data-stu-id="96a62-251">Removed parameter 'PublicNetworkAccessType'</span></span>
     - <span data-ttu-id="96a62-252">Ta bort parametern ”OutboundPublicNetworkAccessType”</span><span class="sxs-lookup"><span data-stu-id="96a62-252">Removed parameter 'OutboundPublicNetworkAccessType'</span></span>
     - <span data-ttu-id="96a62-253">Lade till nya parametrar: ”StorageFileSystem” och ”StorageAccountManagedIdentity” för att stödja ADLSGen2</span><span class="sxs-lookup"><span data-stu-id="96a62-253">Added new parameters: 'StorageFileSystem' and 'StorageAccountManagedIdentity' to support ADLSGen2</span></span>
     - <span data-ttu-id="96a62-254">Lade till den nya parametern ”EnableIDBroker” för att stödja ID-förmedlaren i HDInsight</span><span class="sxs-lookup"><span data-stu-id="96a62-254">Added new parameter 'EnableIDBroker' to Support HDInsight ID Broker</span></span>
     - <span data-ttu-id="96a62-255">Lade till nya parametrar: ”KafkaClientGroupId”, ”KafkaClientGroupName” och ”KafkaManagementNodeSize” för att stödja Kafka REST-proxy</span><span class="sxs-lookup"><span data-stu-id="96a62-255">Added new parameters: 'KafkaClientGroupId', 'KafkaClientGroupName' and 'KafkaManagementNodeSize' to support Kafka Rest Proxy</span></span>
 * <span data-ttu-id="96a62-256">För cmdleten New-AzHDInsightClusterConfig:</span><span class="sxs-lookup"><span data-stu-id="96a62-256">For New-AzHDInsightClusterConfig cmdlet:</span></span>
     - <span data-ttu-id="96a62-257">Ersatte parametern ”DefaultStorageAccountName” med ”StorageAccountResourceId”</span><span class="sxs-lookup"><span data-stu-id="96a62-257">Replaced parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
     - <span data-ttu-id="96a62-258">Ersatte parametern ”DefaultStorageAccountKey” med ”StorageAccountKey”</span><span class="sxs-lookup"><span data-stu-id="96a62-258">Replaced parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
     - <span data-ttu-id="96a62-259">Ersatte parametern ”DefaultStorageAccountType” med ”StorageAccountType”</span><span class="sxs-lookup"><span data-stu-id="96a62-259">Replaced parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
     - <span data-ttu-id="96a62-260">Tog bort parametern ”PublicNetworkAccessType”</span><span class="sxs-lookup"><span data-stu-id="96a62-260">Removed parameter 'PublicNetworkAccessType'</span></span>
     - <span data-ttu-id="96a62-261">Ta bort parametern ”OutboundPublicNetworkAccessType”</span><span class="sxs-lookup"><span data-stu-id="96a62-261">Removed parameter 'OutboundPublicNetworkAccessType'</span></span>
* <span data-ttu-id="96a62-262">För cmdleten Set-AzHDInsightDefaultStorage:</span><span class="sxs-lookup"><span data-stu-id="96a62-262">For Set-AzHDInsightDefaultStorage cmdlet:</span></span>
    - <span data-ttu-id="96a62-263">Ersatte parametern ”StorageAccountName” med ”StorageAccountResourceId”</span><span class="sxs-lookup"><span data-stu-id="96a62-263">Replaced parameter 'StorageAccountName' with 'StorageAccountResourceId'</span></span>
* <span data-ttu-id="96a62-264">För cmdleten Add-AzHDInsightSecurityProfile:</span><span class="sxs-lookup"><span data-stu-id="96a62-264">For Add-AzHDInsightSecurityProfile cmdlet:</span></span>
    - <span data-ttu-id="96a62-265">Ersatte parametern ”Domain” med ”DomainResourceId”</span><span class="sxs-lookup"><span data-stu-id="96a62-265">Replaced parameter 'Domain' with 'DomainResourceId'</span></span>
    - <span data-ttu-id="96a62-266">Tog bort det obligatoriska kravet för parametern ”OrganizationalUnitDN”</span><span class="sxs-lookup"><span data-stu-id="96a62-266">Removed the mandatory requirement for parameter 'OrganizationalUnitDN'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="96a62-267">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="96a62-267">Az.KeyVault</span></span>
* <span data-ttu-id="96a62-268">[Icke-bakåtkompatibel ändring] Parametrarna DisableSoftDelete i ”New-AzKeyVault” och EnableSoftDelete i ”Update-AzKeyVault” har gjorts inaktuella</span><span class="sxs-lookup"><span data-stu-id="96a62-268">[Breaking Change] Deprecated parameter DisableSoftDelete in 'New-AzKeyVault' and EnableSoftDelete in 'Update-AzKeyVault'</span></span>
* <span data-ttu-id="96a62-269">[Icke-bakåtkompatibel ändring] Tog bort attributet SecretValueText för att undvika att SecretValue visas direkt [#12266]</span><span class="sxs-lookup"><span data-stu-id="96a62-269">[Breaking Change] Removed attribute SecretValueText to avoid displaying SecretValue directly [#12266]</span></span>
* <span data-ttu-id="96a62-270">Stöd för ny resurstyp: hanterad HSM</span><span class="sxs-lookup"><span data-stu-id="96a62-270">Supported new resource type: managed HSM</span></span>
    - <span data-ttu-id="96a62-271">CRUD för hanterad HSM och cmdleter för att köra nycklar på hanterad HSM</span><span class="sxs-lookup"><span data-stu-id="96a62-271">CRUD of managed HSM and cmdlets to operate keys on managed HSM</span></span>
    - <span data-ttu-id="96a62-272">Fullständig HSM-säkerhetskopiering/återställning, skapande av AES-nyckel, säkerhetskopiering/återställning av domän, RBAC</span><span class="sxs-lookup"><span data-stu-id="96a62-272">Full HSM backup/restore, AES key creation, security domain backup/restore, RBAC</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="96a62-273">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="96a62-273">Az.ManagedServices</span></span>
* <span data-ttu-id="96a62-274">[Icke-bakåtkompatibel ändring] Uppdaterade namngivningskonventioner för parametrar och associerade exempel</span><span class="sxs-lookup"><span data-stu-id="96a62-274">[Breaking Change] Updated parameters naming conventions and associated examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="96a62-275">Az.Network</span><span class="sxs-lookup"><span data-stu-id="96a62-275">Az.Network</span></span>
* <span data-ttu-id="96a62-276">[Icke-bakåtkompatibel ändring] Tog bort parametern ”HostedSubnet” och lade till ”Subnet” i stället</span><span class="sxs-lookup"><span data-stu-id="96a62-276">[Breaking Change] Removed parameter 'HostedSubnet' and added 'Subnet' instead</span></span>
* <span data-ttu-id="96a62-277">Lade till nya cmdletar för peeringvägar för virtuella routrar</span><span class="sxs-lookup"><span data-stu-id="96a62-277">Added new cmdlets for Virtual Router Peer Routes</span></span>
    - <span data-ttu-id="96a62-278">”Get-AzVirtualRouterPeerLearnedRoute”</span><span class="sxs-lookup"><span data-stu-id="96a62-278">'Get-AzVirtualRouterPeerLearnedRoute'</span></span>
    - <span data-ttu-id="96a62-279">”Get-AzVirtualRouterPeerAdvertisedRoute”</span><span class="sxs-lookup"><span data-stu-id="96a62-279">'Get-AzVirtualRouterPeerAdvertisedRoute'</span></span>
* <span data-ttu-id="96a62-280">Cmdleten New-AzFirewall har uppdaterats:</span><span class="sxs-lookup"><span data-stu-id="96a62-280">Updated New-AzFirewall cmdlet:</span></span>
    - <span data-ttu-id="96a62-281">Lade till parametern ”-SkuTier”</span><span class="sxs-lookup"><span data-stu-id="96a62-281">Added parameter '-SkuTier'</span></span>
    - <span data-ttu-id="96a62-282">Lade till parametern ”-SkuName” och gjorde Sku till ett alias för den</span><span class="sxs-lookup"><span data-stu-id="96a62-282">Added parameter '-SkuName' and made Sku as Alias for this</span></span>
    - <span data-ttu-id="96a62-283">Tog bort parametern ”-Sku”</span><span class="sxs-lookup"><span data-stu-id="96a62-283">Removed parameter '-Sku'</span></span>
* <span data-ttu-id="96a62-284">[Icke-bakåtkompatibel ändring] Gjorde argumentet ”Connectionlink” obligatoriskt i ”Start-AzVpnConnectionPacketCapture” och ”Stop-AzVpnConnectionPacketCapture”</span><span class="sxs-lookup"><span data-stu-id="96a62-284">[Breaking Change] Made 'Connectionlink' argument mandatory in 'Start-AzVpnConnectionPacketCapture' and 'Stop-AzVpnConnectionPacketCapture'</span></span>
* <span data-ttu-id="96a62-285">[Icke-bakåtkompatibel ändring] Uppdaterade ”New-AzNetworkWatcherConnectionMonitorEndPointObject” för att ta bort parametern ”-Filter”</span><span class="sxs-lookup"><span data-stu-id="96a62-285">[Breaking Change] Updated 'New-AzNetworkWatcherConnectionMonitorEndPointObject' to remove parameter '-Filter'</span></span>
* <span data-ttu-id="96a62-286">[Icke-bakåtkompatibel ändring] Ersatte cmdleten ”New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject” med ”New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject”</span><span class="sxs-lookup"><span data-stu-id="96a62-286">[Breaking Change] Replaced 'New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject' cmdlet with 'New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject'</span></span>
* <span data-ttu-id="96a62-287">Uppdaterade cmdleten ”New-AzNetworkWatcherConnectionMonitorEndPointObject”:</span><span class="sxs-lookup"><span data-stu-id="96a62-287">Updated 'New-AzNetworkWatcherConnectionMonitorEndPointObject' cmdlet:</span></span>
    - <span data-ttu-id="96a62-288">Lade till parametern ”-Type”</span><span class="sxs-lookup"><span data-stu-id="96a62-288">Added parameter '-Type'</span></span>
    - <span data-ttu-id="96a62-289">Lade till parametern ”-CoverageLevel”</span><span class="sxs-lookup"><span data-stu-id="96a62-289">Added parameter '-CoverageLevel'</span></span>
    - <span data-ttu-id="96a62-290">Lade till parametern ”-Scope”</span><span class="sxs-lookup"><span data-stu-id="96a62-290">Added parameter '-Scope'</span></span>
* <span data-ttu-id="96a62-291">Uppdaterade cmdleten ”New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject” med den nya parametern ”-DestinationPortBehavior”</span><span class="sxs-lookup"><span data-stu-id="96a62-291">Updated 'New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject' cmdlet with new parameter '-DestinationPortBehavior'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="96a62-292">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="96a62-292">Az.RecoveryServices</span></span>
* <span data-ttu-id="96a62-293">Korrigerar återställning av arbetsbelastningar för behörigheter för deltagare.</span><span class="sxs-lookup"><span data-stu-id="96a62-293">Fixing Workload Restore for contributor permissions.</span></span>
* <span data-ttu-id="96a62-294">Lade till nya parameteruppsättningar och valideringar för cmdleten ”Restore-AzRecoveryServicesBackupItem”.</span><span class="sxs-lookup"><span data-stu-id="96a62-294">Added new parameter sets and validations for Restore-AzRecoveryServicesBackupItem cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="96a62-295">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="96a62-295">Az.Resources</span></span>
* <span data-ttu-id="96a62-296">Korrigerade en bugg vid parsning</span><span class="sxs-lookup"><span data-stu-id="96a62-296">Fixed parsing bug</span></span>
* <span data-ttu-id="96a62-297">Uppdaterade What-If-cmdletar i ARM-mall för att ta bort förhandsgranskningsmeddelandet från resultaten</span><span class="sxs-lookup"><span data-stu-id="96a62-297">Updated ARM template What-If cmdlets to remove preview message from results</span></span>
* <span data-ttu-id="96a62-298">Korrigerade ett problem där cmdletar för mall-distribution kraschar om ”-WhatIf” har ställts in på ett högre omfång [#13038]</span><span class="sxs-lookup"><span data-stu-id="96a62-298">Fixed an issue where template deployment cmdlets crash if '-WhatIf' is set at a higher scope [#13038]</span></span>
* <span data-ttu-id="96a62-299">Korrigerade ett problem där cmdletar för malldistribution inte bevarar skiftläget för mallparametrar</span><span class="sxs-lookup"><span data-stu-id="96a62-299">Fixed an issue where template deployment cmdlets does not preserve case for template parameters</span></span>
* <span data-ttu-id="96a62-300">Lade till en standard-API-version som kan användas i cmdleten ”Export-AzResourceGroup”</span><span class="sxs-lookup"><span data-stu-id="96a62-300">Added a default API version to be used in 'Export-AzResourceGroup' cmdlet</span></span>
* <span data-ttu-id="96a62-301">Lade till cmdletar för mallspecifikationer (”Get-AzTemplateSpec”, ”Set-AzTemplateSpec”, ”New-AzTemplateSpec”, ”Remove-AzTemplateSpec”, ”Export-AzTemplateSpec”)</span><span class="sxs-lookup"><span data-stu-id="96a62-301">Added cmdlets for Template Specs ('Get-AzTemplateSpec', 'Set-AzTemplateSpec', 'New-AzTemplateSpec', 'Remove-AzTemplateSpec', 'Export-AzTemplateSpec')</span></span>
* <span data-ttu-id="96a62-302">Lade till stöd för att distribuera mallspecifikationer med befintliga cmdletar för distribution (via den nya parametern ”-TemplateSpecId”)</span><span class="sxs-lookup"><span data-stu-id="96a62-302">Added support for deploying Template Specs using existing deployment cmdlets (via the new -TemplateSpecId parameter)</span></span> 
* <span data-ttu-id="96a62-303">Uppdaterade ”Get-AzResourceGroupDeploymentOperation” för att använda SDK.</span><span class="sxs-lookup"><span data-stu-id="96a62-303">Updated 'Get-AzResourceGroupDeploymentOperation' to use the SDK.</span></span>
* <span data-ttu-id="96a62-304">Tog bort parametern ”ApiVersion” från cmdletarna ”\*-AzDeployment”.</span><span class="sxs-lookup"><span data-stu-id="96a62-304">Removed '-ApiVersion' parameter from '\*-AzDeployment' cmdlets.</span></span>

#### <a name="azsql"></a><span data-ttu-id="96a62-305">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="96a62-305">Az.Sql</span></span>
* <span data-ttu-id="96a62-306">Korrigerade ett problem där New-AzSqlDatabaseExport misslyckas om networkIsolation inte har angetts [#13097]</span><span class="sxs-lookup"><span data-stu-id="96a62-306">Fixed issue where New-AzSqlDatabaseExport fails if networkIsolation not specified [#13097]</span></span>
* <span data-ttu-id="96a62-307">Korrigerade ett problem där New-AzSqlDatabaseExport och New-AzSqlDatabaseImport inte returnerade OperationStatusLink i resultatobjektet [#13097]</span><span class="sxs-lookup"><span data-stu-id="96a62-307">Fixed issue where New-AzSqlDatabaseExport and New-AzSqlDatabaseImport were not returning OperationStatusLink in the result object [#13097]</span></span>
* <span data-ttu-id="96a62-308">Uppdatera webbadresser för Azure-kopplade regioner i redundansvarningar för Backup Storage</span><span class="sxs-lookup"><span data-stu-id="96a62-308">Update Azure Paired Regions URL in Backup Storage Redundancy Warnings</span></span> 

#### <a name="azstorage"></a><span data-ttu-id="96a62-309">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="96a62-309">Az.Storage</span></span>
* <span data-ttu-id="96a62-310">Tog bort den föråldrade egenskapen RestorePolicy.LastEnabledTime</span><span class="sxs-lookup"><span data-stu-id="96a62-310">Removed obsolete property RestorePolicy.LastEnabledTime</span></span>
    - <span data-ttu-id="96a62-311">"Enable-AzStorageBlobRestorePolicy"</span><span class="sxs-lookup"><span data-stu-id="96a62-311">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="96a62-312">"Disable-AzStorageBlobRestorePolicy"</span><span class="sxs-lookup"><span data-stu-id="96a62-312">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="96a62-313">”Get-AzStorageBlobServiceProperty”</span><span class="sxs-lookup"><span data-stu-id="96a62-313">'Get-AzStorageBlobServiceProperty'</span></span>
    - <span data-ttu-id="96a62-314">”Update-AzStorageBlobServiceProperty”</span><span class="sxs-lookup"><span data-stu-id="96a62-314">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="96a62-315">Vill du ändra typen av DaysAfterModificationGreaterThan från int till int?</span><span class="sxs-lookup"><span data-stu-id="96a62-315">Change Type of DaysAfterModificationGreaterThan from int to int?</span></span>
    - <span data-ttu-id="96a62-316">"Set-AzStorageAccountManagementPolicy"</span><span class="sxs-lookup"><span data-stu-id="96a62-316">'Set-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="96a62-317">"Get-AzStorageAccountManagementPolicy"</span><span class="sxs-lookup"><span data-stu-id="96a62-317">'Get-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="96a62-318">"Add-AzStorageAccountManagementPolicyAction"</span><span class="sxs-lookup"><span data-stu-id="96a62-318">'Add-AzStorageAccountManagementPolicyAction'</span></span>
    - <span data-ttu-id="96a62-319">"New-AzStorageAccountManagementPolicyRule"</span><span class="sxs-lookup"><span data-stu-id="96a62-319">'New-AzStorageAccountManagementPolicyRule'</span></span>
* <span data-ttu-id="96a62-320">Stöd för skapa/uppdatera filresurs med åtkomstnivå</span><span class="sxs-lookup"><span data-stu-id="96a62-320">Supported create/update file share with access tier</span></span>
    - <span data-ttu-id="96a62-321">”New-AzRmStorageShare”</span><span class="sxs-lookup"><span data-stu-id="96a62-321">'New-AzRmStorageShare'</span></span>
    - <span data-ttu-id="96a62-322">”Update-AzRmStorageShare”</span><span class="sxs-lookup"><span data-stu-id="96a62-322">'Update-AzRmStorageShare'</span></span>
* <span data-ttu-id="96a62-323">Stöd för att konfigurera/uppdatera/ta bort ACL som stöds rekursivt på Datalake Gen2-objekt</span><span class="sxs-lookup"><span data-stu-id="96a62-323">Supported set/update/remove Acl recursively on Datalake Gen2 item</span></span> 
    -  <span data-ttu-id="96a62-324">”Set-AzDataLakeGen2AclRecursive”</span><span class="sxs-lookup"><span data-stu-id="96a62-324">'Set-AzDataLakeGen2AclRecursive'</span></span> 
    -  <span data-ttu-id="96a62-325">”Update-AzDataLakeGen2AclRecursive”</span><span class="sxs-lookup"><span data-stu-id="96a62-325">'Update-AzDataLakeGen2AclRecursive'</span></span> 
    -  <span data-ttu-id="96a62-326">”Remove-AzDataLakeGen2AclRecursive”</span><span class="sxs-lookup"><span data-stu-id="96a62-326">'Remove-AzDataLakeGen2AclRecursive'</span></span>
* <span data-ttu-id="96a62-327">Stöd för åtkomstprincip för containrar med de nya behörigheterna x, t</span><span class="sxs-lookup"><span data-stu-id="96a62-327">Supported Container access policy with new permission x,t</span></span>
    -  <span data-ttu-id="96a62-328">”New-AzStorageContainerStoredAccessPolicy”</span><span class="sxs-lookup"><span data-stu-id="96a62-328">'New-AzStorageContainerStoredAccessPolicy'</span></span>
    -  <span data-ttu-id="96a62-329">"Set-AzStorageContainerStoredAccessPolicy"</span><span class="sxs-lookup"><span data-stu-id="96a62-329">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
* <span data-ttu-id="96a62-330">Ändrade utdata från cmdleten hämta/ange åtkomstprincip för containrar genom att ändra behörighetstypen för den underordnade egenskapen från uppräkning till sträng</span><span class="sxs-lookup"><span data-stu-id="96a62-330">Changed the output of get/set Container access policy cmdlet, by change the child property Permission type from enum to String</span></span>
    -  <span data-ttu-id="96a62-331">"Get-AzStorageContainerStoredAccessPolicy"</span><span class="sxs-lookup"><span data-stu-id="96a62-331">'Get-AzStorageContainerStoredAccessPolicy'</span></span>
    -  <span data-ttu-id="96a62-332">"Set-AzStorageContainerStoredAccessPolicy"</span><span class="sxs-lookup"><span data-stu-id="96a62-332">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
* <span data-ttu-id="96a62-333">Korrigerade ett problem med exempelskript för att ange hanteringsprincip med JSON</span><span class="sxs-lookup"><span data-stu-id="96a62-333">Fixed a sample script issue of set management policy with json</span></span>
    -  <span data-ttu-id="96a62-334">"Set-AzStorageAccountManagementPolicy"</span><span class="sxs-lookup"><span data-stu-id="96a62-334">'Set-AzStorageAccountManagementPolicy'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="96a62-335">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="96a62-335">Az.Websites</span></span>
* <span data-ttu-id="96a62-336">Lade till stöd för Premium V3-prisnivån</span><span class="sxs-lookup"><span data-stu-id="96a62-336">Added support for Premium V3 pricing tier</span></span>
* <span data-ttu-id="96a62-337">Uppdaterade SDK för WebSites till 3.1.0</span><span class="sxs-lookup"><span data-stu-id="96a62-337">Updated the WebSites SDK to 3.1.0</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="96a62-338">Tack till våra community-deltagare</span><span class="sxs-lookup"><span data-stu-id="96a62-338">Thanks to our community contributors</span></span>
* <span data-ttu-id="96a62-339">@atul-ram, uppdatera Get-AzDelegation.md (#13176)</span><span class="sxs-lookup"><span data-stu-id="96a62-339">@atul-ram, Update Get-AzDelegation.md (#13176)</span></span>
* <span data-ttu-id="96a62-340">@dineshreddy007, hämta approller som har tilldelats korrekt om Stack HCI-registrering använder WAC-token.</span><span class="sxs-lookup"><span data-stu-id="96a62-340">@dineshreddy007, Get the App Roles assigned correctly in case of Stack HCI registration using WAC token.</span></span> <span data-ttu-id="96a62-341">(#13249)</span><span class="sxs-lookup"><span data-stu-id="96a62-341">(#13249)</span></span>
* <span data-ttu-id="96a62-342">@kongou-ae, uppdatera New-AzOffice365PolicyProperty.md (#13217)</span><span class="sxs-lookup"><span data-stu-id="96a62-342">@kongou-ae, Update New-AzOffice365PolicyProperty.md (#13217)</span></span>
* <span data-ttu-id="96a62-343">Lohith Chowdary Chilukuri (@Lochiluk), uppdatera Set-AzApplicationGateway.md (#13150)</span><span class="sxs-lookup"><span data-stu-id="96a62-343">Lohith Chowdary Chilukuri (@Lochiluk), Update Set-AzApplicationGateway.md (#13150)</span></span>
* <span data-ttu-id="96a62-344">Matthew Burleigh (@mburleigh)</span><span class="sxs-lookup"><span data-stu-id="96a62-344">Matthew Burleigh (@mburleigh)</span></span>
  * <span data-ttu-id="96a62-345">Lägg till länkar till de PowerShell-cmdletar som refereras i dokumentet (#13203)</span><span class="sxs-lookup"><span data-stu-id="96a62-345">Add links to PowerShell cmdlets referenced in the document (#13203)</span></span>
  * <span data-ttu-id="96a62-346">Lägg till länkar till de PowerShell-cmdletar som refereras i dokumentet (#13190)</span><span class="sxs-lookup"><span data-stu-id="96a62-346">Add links to PowerShell cmdlets referenced in the document (#13190)</span></span>
  * <span data-ttu-id="96a62-347">Lägg till länkar till de PowerShell-cmdletar som refereras i dokumentet (#13189)</span><span class="sxs-lookup"><span data-stu-id="96a62-347">Add links to PowerShell cmdlets referenced in the document (#13189)</span></span>
  * <span data-ttu-id="96a62-348">lägg till länkar till cmdletar som refereras (#13137)</span><span class="sxs-lookup"><span data-stu-id="96a62-348">add links to referenced cmdlets (#13137)</span></span>
  * <span data-ttu-id="96a62-349">Lägg till länkar till de PowerShell-cmdletar som refereras i dokumentet (#13204)</span><span class="sxs-lookup"><span data-stu-id="96a62-349">Add links to PowerShell cmdlets referenced in the document (#13204)</span></span>
  * <span data-ttu-id="96a62-350">Lägg till länkar till de PowerShell-cmdletar som refereras i dokumentet (#13205)</span><span class="sxs-lookup"><span data-stu-id="96a62-350">Add links to PowerShell cmdlets referenced in the document (#13205)</span></span>

## <a name="480---october-2020"></a><span data-ttu-id="96a62-351">4.8.0 – oktober 2020</span><span class="sxs-lookup"><span data-stu-id="96a62-351">4.8.0 - October 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="96a62-352">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="96a62-352">Az.Accounts</span></span>
* <span data-ttu-id="96a62-353">Åtgärdat DateTime-parsningsfel i vanliga bibliotek [#13045]</span><span class="sxs-lookup"><span data-stu-id="96a62-353">Fixed DateTime parse issue in common libraries [#13045]</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="96a62-354">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="96a62-354">Az.CognitiveServices</span></span>
* <span data-ttu-id="96a62-355">Cmdleten New-AzCognitiveServicesAccountApiProperty har lagts till.</span><span class="sxs-lookup"><span data-stu-id="96a62-355">Added 'New-AzCognitiveServicesAccountApiProperty' cmdlet.</span></span>
* <span data-ttu-id="96a62-356">Stöd för parametern ApiProperty för New-AzCognitiveServicesAccount och Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="96a62-356">Supported 'ApiProperty' parameter for 'New-AzCognitiveServicesAccount' and 'Set-AzCognitiveServicesAccount'</span></span>

#### <a name="azcompute"></a><span data-ttu-id="96a62-357">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="96a62-357">Az.Compute</span></span>
* <span data-ttu-id="96a62-358">Åtgärdat problem i Update-ASRRecoveryPlan genom att fylla i FailoverTypes</span><span class="sxs-lookup"><span data-stu-id="96a62-358">Fixed issue in 'Update-ASRRecoveryPlan' by populating FailoverTypes</span></span>
* <span data-ttu-id="96a62-359">De valfria parametrarna -Top och -OrderBy har lagts till i cmdleten Get-AzVmImage.</span><span class="sxs-lookup"><span data-stu-id="96a62-359">Added the '-Top' and '-OrderBy' optional parameters to the 'Get-AzVmImage' cmdlet.</span></span> 

#### <a name="azdatabricks"></a><span data-ttu-id="96a62-360">Az.Databricks</span><span class="sxs-lookup"><span data-stu-id="96a62-360">Az.Databricks</span></span>
* <span data-ttu-id="96a62-361">Allmän tillgänglighet för modulen Az.Databricks</span><span class="sxs-lookup"><span data-stu-id="96a62-361">General availability of 'Az.Databricks' module</span></span>
* <span data-ttu-id="96a62-362">Stöd har lagts till för virtuell nätverkspeering</span><span class="sxs-lookup"><span data-stu-id="96a62-362">Added support for virtual network peering</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="96a62-363">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="96a62-363">Az.DataFactory</span></span>
* <span data-ttu-id="96a62-364">Skrivfel har åtgärdats i utdatameddelanden</span><span class="sxs-lookup"><span data-stu-id="96a62-364">Fixed typo in output messages</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="96a62-365">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="96a62-365">Az.EventHub</span></span>
* <span data-ttu-id="96a62-366">Den valfria switchparametern TrustedServiceAccessEnabled har lagts till i cmdleten Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="96a62-366">Added optional switch parameter 'TrustedServiceAccessEnabled' to 'Set-AzEventHubNetworkRuleSet' cmdlet</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="96a62-367">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="96a62-367">Az.HDInsight</span></span>
* <span data-ttu-id="96a62-368">Ett varningsmeddelande om att parametrarna PublicNetworkAccessType och OutboundPublicNetworkAccessType planeras att göras inaktuella har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-368">Added warning message for planning to deprecate the parameters 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType'</span></span>
* <span data-ttu-id="96a62-369">Ett varningsmeddelande om att parametern DefaultStorageAccountName planeras att ersättas med StorageAccountResourceId har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-369">Added warning message for planning to replace the parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
* <span data-ttu-id="96a62-370">Ett varningsmeddelande om att parametern DefaultStorageAccountKey planeras att ersättas med StorageAccountKey har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-370">Added warning message for planning to replace the parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
* <span data-ttu-id="96a62-371">Ett varningsmeddelande om att parametern DefaultStorageAccountType planeras att ersättas med StorageAccountType har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-371">Added warning message for planning to replace the parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
* <span data-ttu-id="96a62-372">Ett varningsmeddelande om att parametern DefaultStorageContainer planeras att ersättas med StorageContainer har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-372">Added warning message for planning to replace the parameter 'DefaultStorageContainer' with 'StorageContainer'</span></span>
* <span data-ttu-id="96a62-373">Ett varningsmeddelande om att parametern DefaultStorageRootPath planeras att ersättas med StorageRootPath har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-373">Added warning message for planning to replace the parameter 'DefaultStorageRootPath' with 'StorageRootPath'</span></span>

#### <a name="aziothub"></a><span data-ttu-id="96a62-374">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="96a62-374">Az.IotHub</span></span>
* <span data-ttu-id="96a62-375">SDK för enheter har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="96a62-375">Updated devices sdk.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="96a62-376">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="96a62-376">Az.KeyVault</span></span>
* <span data-ttu-id="96a62-377">Detaljerat datum för borttagning av egenskapen SecretValueText har tillhandahållits</span><span class="sxs-lookup"><span data-stu-id="96a62-377">Provided the detailed date of removing property SecretValueText</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="96a62-378">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="96a62-378">Az.ManagedServices</span></span>
* <span data-ttu-id="96a62-379">Varningar om icke-bakåtkompatibla ändringar för cmdletar för tilldelning och definition av hanterade tjänster har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="96a62-379">Updated breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="96a62-380">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="96a62-380">Az.Monitor</span></span>
* <span data-ttu-id="96a62-381">Felet som gjorde att ett varningsmeddelande inte kunde ignoreras har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="96a62-381">Fixed the bug that warning message cannot be suppressed.</span></span> <span data-ttu-id="96a62-382">[#12889]</span><span class="sxs-lookup"><span data-stu-id="96a62-382">[#12889]</span></span>
* <span data-ttu-id="96a62-383">Stöd för parametern SkipMetricValidation i aviseringsregelvillkor.</span><span class="sxs-lookup"><span data-stu-id="96a62-383">Supported 'SkipMetricValidation' parameter in alert rule criteria.</span></span> <span data-ttu-id="96a62-384">Tillåter att du skapar en aviseringsregel för ett anpassat mått som inte har genererats än, genom att göra så att måttverifieringen hoppas över.</span><span class="sxs-lookup"><span data-stu-id="96a62-384">Allows creating an alert rule on a custom metric that isn't yet emitted, by causing the metric validation to be skipped.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="96a62-385">Az.Network</span><span class="sxs-lookup"><span data-stu-id="96a62-385">Az.Network</span></span>
* <span data-ttu-id="96a62-386">Office365-princip har lagts till för VPNSite-resurs</span><span class="sxs-lookup"><span data-stu-id="96a62-386">Added Office365 Policy to VPNSite Resource</span></span>
    - <span data-ttu-id="96a62-387">New-AzO365PolicyProperty</span><span class="sxs-lookup"><span data-stu-id="96a62-387">'New-AzO365PolicyProperty'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="96a62-388">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="96a62-388">Az.RecoveryServices</span></span>
* <span data-ttu-id="96a62-389">Verifiering av containernamn har lagts till för arbetsbelastningssäkerhetskopior.</span><span class="sxs-lookup"><span data-stu-id="96a62-389">Added container name validation for workload backup.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="96a62-390">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="96a62-390">Az.RedisCache</span></span>
* <span data-ttu-id="96a62-391">En korrigering har gjorts så att cmdletarna New-AzRedisCache och Set-AzRedisCache inte misslyckas på grund av behörighetsproblem som rör registrering av Microsoft.Cache RP</span><span class="sxs-lookup"><span data-stu-id="96a62-391">Made 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets not fail because of permission issue related to registering Microsoft.Cache RP</span></span>

#### <a name="azsql"></a><span data-ttu-id="96a62-392">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="96a62-392">Az.Sql</span></span>
* <span data-ttu-id="96a62-393">BackupStorageRedundancy har lagts till i:</span><span class="sxs-lookup"><span data-stu-id="96a62-393">Added BackupStorageRedundancy to the following:</span></span> 
    - <span data-ttu-id="96a62-394">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="96a62-394">'Restore-AzureRmSqlDatabase'</span></span>
    - <span data-ttu-id="96a62-395">New-AzSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="96a62-395">'New-AzSqlDatabaseCopy'</span></span>
    - <span data-ttu-id="96a62-396">New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="96a62-396">'New-AzSqlDatabaseSecondary'</span></span>
* <span data-ttu-id="96a62-397">Skiftlägeskänslighet har tagits bort för parametern BackupStorageRedundancy för alla SQL DB-referenser</span><span class="sxs-lookup"><span data-stu-id="96a62-397">Removed case sensitivity for BackupStorageRedundancy parameter for all SQL DB references</span></span> 
* <span data-ttu-id="96a62-398">Namnen på BackupStorageRedundancy-varningsmeddelanden har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="96a62-398">Updated BackupStorageRedundancy warning message names</span></span>

#### <a name="azstorage"></a><span data-ttu-id="96a62-399">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="96a62-399">Az.Storage</span></span>
* <span data-ttu-id="96a62-400">Stöd för att aktivera/inaktivera/hämta egenskaper för mjuk borttagning av resurser för filtjänst för ett lagringskonto</span><span class="sxs-lookup"><span data-stu-id="96a62-400">Supported enable/disable/get share soft delete properties on file Service of a Storage account</span></span>
    - <span data-ttu-id="96a62-401">Update-AzStorageFileServiceProperty</span><span class="sxs-lookup"><span data-stu-id="96a62-401">'Update-AzStorageFileServiceProperty'</span></span>
    - <span data-ttu-id="96a62-402">Get-AzStorageFileServiceProperty</span><span class="sxs-lookup"><span data-stu-id="96a62-402">'Get-AzStorageFileServiceProperty'</span></span>
* <span data-ttu-id="96a62-403">Stöd för att visa filresurser inkluderar borttagna filresurser för ett lagringskonto och hämta förbrukning av enskild filresurs</span><span class="sxs-lookup"><span data-stu-id="96a62-403">Supported list file shares include the deleted ones of a Storage account, and Get single file share usage</span></span>
    - <span data-ttu-id="96a62-404">”Get-AzRmStorageShare”</span><span class="sxs-lookup"><span data-stu-id="96a62-404">'Get-AzRmStorageShare'</span></span>
* <span data-ttu-id="96a62-405">Stöd för återställning av en borttagen filresurs</span><span class="sxs-lookup"><span data-stu-id="96a62-405">Supported restore a deleted file share</span></span>
    - <span data-ttu-id="96a62-406">Restore-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="96a62-406">'Restore-AzRmStorageShare'</span></span>
* <span data-ttu-id="96a62-407">Cmdletarna för ändring av egenskaper för Blob Service har ändrats. De ursprungliga egenskaperna hämtas inte från servern utan anger bara de ändrade egenskaperna till servern.</span><span class="sxs-lookup"><span data-stu-id="96a62-407">Changed the cmdlets for modify blob service properties, won't get the original properties from server, but only set the modified properties to server.</span></span>
    - <span data-ttu-id="96a62-408">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="96a62-408">'Enable-AzStorageBlobDeleteRetentionPolicy'</span></span>
    - <span data-ttu-id="96a62-409">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="96a62-409">'Disable-AzStorageBlobDeleteRetentionPolicy'</span></span>  
    - <span data-ttu-id="96a62-410">"Enable-AzStorageBlobRestorePolicy"</span><span class="sxs-lookup"><span data-stu-id="96a62-410">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="96a62-411">"Disable-AzStorageBlobRestorePolicy"</span><span class="sxs-lookup"><span data-stu-id="96a62-411">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="96a62-412">”Update-AzStorageBlobServiceProperty”</span><span class="sxs-lookup"><span data-stu-id="96a62-412">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="96a62-413">Åtgärdat hjälpproblem för New-AzStorageAccount-parametern -Kind default value [#12189]</span><span class="sxs-lookup"><span data-stu-id="96a62-413">Fixed help issue for New-AzStorageAccount parameter -Kind default value [#12189]</span></span>
* <span data-ttu-id="96a62-414">Åtgärdat problem genom att lägga till exempel som visar hur ContentType anges på korrekt sätt i en blobuppladdning [#12989]</span><span class="sxs-lookup"><span data-stu-id="96a62-414">Fixed issue by add example to show how to set correct ContentType in blob upload [#12989]</span></span>

## <a name="470---september-2020"></a><span data-ttu-id="96a62-415">4.7.0 – September 2020</span><span class="sxs-lookup"><span data-stu-id="96a62-415">4.7.0 - September 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="96a62-416">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="96a62-416">Az.Accounts</span></span>
* <span data-ttu-id="96a62-417">Formaterat kommande meddelanden om icke-bakåtkompatibel ändring</span><span class="sxs-lookup"><span data-stu-id="96a62-417">Formatted the upcoming breaking change messages</span></span>
* <span data-ttu-id="96a62-418">Uppdaterat Azure.Core till 1.4.1</span><span class="sxs-lookup"><span data-stu-id="96a62-418">Updated Azure.Core to 1.4.1</span></span>

#### <a name="azaks"></a><span data-ttu-id="96a62-419">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="96a62-419">Az.Aks</span></span>
* <span data-ttu-id="96a62-420">Valideringslogiken för parametern "New-AzAksCluster", "Set-AzAksCluster" och "New-AzAksNodePool" har lagts till på klientsidan.</span><span class="sxs-lookup"><span data-stu-id="96a62-420">Added client side parameter validation logic for 'New-AzAksCluster', 'Set-AzAksCluster' and 'New-AzAksNodePool'.</span></span> <span data-ttu-id="96a62-421">[#12372]</span><span class="sxs-lookup"><span data-stu-id="96a62-421">[#12372]</span></span>
* <span data-ttu-id="96a62-422">Stöd har lagts till för tillägg i "New-AzAksCluster".</span><span class="sxs-lookup"><span data-stu-id="96a62-422">Added support for add-ons in 'New-AzAksCluster'.</span></span> <span data-ttu-id="96a62-423">[#11239]</span><span class="sxs-lookup"><span data-stu-id="96a62-423">[#11239]</span></span>
* <span data-ttu-id="96a62-424">Cmdlet:arna "Enable-AzAksAddOn" och "Disable-AzAksAddOn" har lagts till för tillägg.</span><span class="sxs-lookup"><span data-stu-id="96a62-424">Added cmdlets 'Enable-AzAksAddOn' and 'Disable-AzAksAddOn' for add-ons.</span></span> <span data-ttu-id="96a62-425">[#11239]</span><span class="sxs-lookup"><span data-stu-id="96a62-425">[#11239]</span></span>
* <span data-ttu-id="96a62-426">Parametern "GenerateSshKey" har lagts till för "New-AzAksCluster".</span><span class="sxs-lookup"><span data-stu-id="96a62-426">Added parameter 'GenerateSshKey' for 'New-AzAksCluster'.</span></span> <span data-ttu-id="96a62-427">[#12371]</span><span class="sxs-lookup"><span data-stu-id="96a62-427">[#12371]</span></span>
* <span data-ttu-id="96a62-428">API-versionen har uppdaterats till 2020-06-01.</span><span class="sxs-lookup"><span data-stu-id="96a62-428">Updated api version to 2020-06-01.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="96a62-429">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="96a62-429">Az.CognitiveServices</span></span>
* <span data-ttu-id="96a62-430">Visade ytterligare juridiska villkor för vissa API:er.</span><span class="sxs-lookup"><span data-stu-id="96a62-430">Showed additional legal terms for certain APIs.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="96a62-431">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="96a62-431">Az.Compute</span></span>
* <span data-ttu-id="96a62-432">Den valfria parametern "EncryptionType" har lagts till i "New-AzVmDiskEncryptionSetConfig"</span><span class="sxs-lookup"><span data-stu-id="96a62-432">Added the '-EncryptionType' optional parameter to 'New-AzVmDiskEncryptionSetConfig'</span></span>
* <span data-ttu-id="96a62-433">Nya cmdlet:ar för ny resurs typ: DiskAccess "Get-AzDiskAccess", "New-AzDiskAccess", "Get-AzDiskAccess"</span><span class="sxs-lookup"><span data-stu-id="96a62-433">New cmdlets for new resource type: DiskAccess 'Get-AzDiskAccess', 'New-AzDiskAccess', 'Get-AzDiskAccess'</span></span>
* <span data-ttu-id="96a62-434">De valfria parametrarna "-DiskAccessId" och "-NetworkAccessPolicy" har lagts till i "New-AzSnapshotConfig"</span><span class="sxs-lookup"><span data-stu-id="96a62-434">Added optional parameters '-DiskAccessId' and '-NetworkAccessPolicy' to 'New-AzSnapshotConfig'</span></span>
* <span data-ttu-id="96a62-435">De valfria parametrarna "-DiskAccessId" och "-NetworkAccessPolicy" har lagts till i "New-AzDiskConfig"</span><span class="sxs-lookup"><span data-stu-id="96a62-435">Added optional parameters '-DiskAccessId' and '-NetworkAccessPolicy' to 'New-AzDiskConfig'</span></span>
* <span data-ttu-id="96a62-436">PatchStatus-egenskapen har lagts till i VirtualMachine-instansvyn</span><span class="sxs-lookup"><span data-stu-id="96a62-436">Added 'PatchStatus' property to VirtualMachine Instance View</span></span>
* <span data-ttu-id="96a62-437">Egenskapen "VMHealth" har lagts till i den virtuella datorns instansvy, vilket är det returnerade objektet när "get-AzVm" anropas med "-Status"</span><span class="sxs-lookup"><span data-stu-id="96a62-437">Added 'VMHealth' property to the virtual machine's instance view, which is the returned object when 'Get-AzVm' is invoked with '-Status'</span></span>
* <span data-ttu-id="96a62-438">Fältet "AssignedHost" har lagts till i instansvyerna "Get-AzVM" och "Get-AzVmss".</span><span class="sxs-lookup"><span data-stu-id="96a62-438">Added 'AssignedHost' field to 'Get-AzVM' and 'Get-AzVmss' instance views.</span></span> <span data-ttu-id="96a62-439">I fältet visas resurs-ID för den virtuella datorinstansen</span><span class="sxs-lookup"><span data-stu-id="96a62-439">The field shows the resource id of the virtual machine instance</span></span>
* <span data-ttu-id="96a62-440">Den valfria parametern "-SupportAutomaticPlacement" har lagts till i "New-AzHostGroup"</span><span class="sxs-lookup"><span data-stu-id="96a62-440">Added optional parameter '-SupportAutomaticPlacement' to 'New-AzHostGroup'</span></span> 
* <span data-ttu-id="96a62-441">Parametern "-HostGroupId" har lagts till i "New-AzVm" och "New-AzVmss"</span><span class="sxs-lookup"><span data-stu-id="96a62-441">Added the '-HostGroupId' parameter to 'New-AzVm' and 'New-AzVmss'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="96a62-442">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="96a62-442">Az.DataFactory</span></span>
* <span data-ttu-id="96a62-443">ADF .Net SDK har uppdaterats till version 4.11.0</span><span class="sxs-lookup"><span data-stu-id="96a62-443">Updated ADF .Net SDK version to 4.11.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="96a62-444">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="96a62-444">Az.EventHub</span></span>
* <span data-ttu-id="96a62-445">Nya kluster-cmdlet:ar – "New-AzEventHubCluster", "Set-AzEventHubCluster", "Get-AzEventHubCluster", "Remove-AzEventHubCluster", "Get-AzEventHubClustersAvailableRegions" har lagts till.</span><span class="sxs-lookup"><span data-stu-id="96a62-445">Added new Cluster cmdlets - 'New-AzEventHubCluster', 'Set-AzEventHubCluster', 'Get-AzEventHubCluster', 'Remove-AzEventHubCluster', 'Get-AzEventHubClustersAvailableRegions'.</span></span>
* <span data-ttu-id="96a62-446">Åtgärdat för ärende #10722 : Korrigering för tilldelning av enbart lyssning till AuthorizationRule-rättigheter.</span><span class="sxs-lookup"><span data-stu-id="96a62-446">Fixed for issue #10722 : Fix for assigning only 'Listen' to AuthorizationRule rights.</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="96a62-447">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="96a62-447">Az.Functions</span></span>
* <span data-ttu-id="96a62-448">Möjligheten att skapa v2-funktioner i regioner som inte stöder det har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="96a62-448">Removed the ability to create v2 Functions in regions that do not support it.</span></span>
* <span data-ttu-id="96a62-449">Föråldrad PowerShell 6.2.</span><span class="sxs-lookup"><span data-stu-id="96a62-449">Deprecated PowerShell 6.2.</span></span> <span data-ttu-id="96a62-450">En varning har lagts till när en användare skapar en PowerShell 6.2-funktionsapp som uppmanar till att skapa en PowerShell 7.0-funktionsapp i stället.</span><span class="sxs-lookup"><span data-stu-id="96a62-450">Added a warning for when a user creates a PowerShell 6.2 function app that advises them to create a PowerShell 7.0 function app instead.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="96a62-451">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="96a62-451">Az.HDInsight</span></span>
* <span data-ttu-id="96a62-452">Stöd för att skapa kluster med automatisk skalningskonfiguration</span><span class="sxs-lookup"><span data-stu-id="96a62-452">Supported creating cluster with Autoscale configuration</span></span>
    - <span data-ttu-id="96a62-453">Lägg till den nya parametern "AutoscaleConfiguration" till cmdleten ”New-AzHDInsightCluster”</span><span class="sxs-lookup"><span data-stu-id="96a62-453">Add new parameter 'AutoscaleConfiguration' to the cmdlet 'New-AzHDInsightCluster'</span></span>
* <span data-ttu-id="96a62-454">Stöd för att använda automatisk skalningskonfiguration i kluster</span><span class="sxs-lookup"><span data-stu-id="96a62-454">Supported operating cluster's Autoscale configuration</span></span>
    - <span data-ttu-id="96a62-455">Lägg till ny cmdlet "Get-AzHDInsihgtClusterAutoscaleConfiguration"</span><span class="sxs-lookup"><span data-stu-id="96a62-455">Add new cmdlet 'Get-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="96a62-456">Lägg till ny cmdlet "New-AzHDInsihgtClusterAutoscaleConfiguration"</span><span class="sxs-lookup"><span data-stu-id="96a62-456">Add new cmdlet 'New-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="96a62-457">Lägg till ny cmdlet "Set-AzHDInsihgtClusterAutoscaleConfiguration"</span><span class="sxs-lookup"><span data-stu-id="96a62-457">Add new cmdlet 'Set-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="96a62-458">Lägg till ny cmdlet "Remove-AzHDInsihgtClusterAutoscaleConfiguration"</span><span class="sxs-lookup"><span data-stu-id="96a62-458">Add new cmdlet 'Remove-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="96a62-459">Lägg till ny cmdlet "New-AzHDInsihgtClusterAutoscaleScheduleCondition"</span><span class="sxs-lookup"><span data-stu-id="96a62-459">Add new cmdlet 'New-AzHDInsihgtClusterAutoscaleScheduleCondition'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="96a62-460">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="96a62-460">Az.KeyVault</span></span>
* <span data-ttu-id="96a62-461">Stöd har lagts till för RBAC-auktorisering [#10557]</span><span class="sxs-lookup"><span data-stu-id="96a62-461">Added support for RBAC authorization [#10557]</span></span>
* <span data-ttu-id="96a62-462">Förbättrad felhantering i "Set-AzKeyVaultAccessPolicy" [#4007]</span><span class="sxs-lookup"><span data-stu-id="96a62-462">Enhanced error handling in 'Set-AzKeyVaultAccessPolicy' [#4007]</span></span>

#### <a name="azkusto"></a><span data-ttu-id="96a62-463">Az.Kusto</span><span class="sxs-lookup"><span data-stu-id="96a62-463">Az.Kusto</span></span>
* <span data-ttu-id="96a62-464">Allmän tillgänglighet för "Az.Kusto"-modulen</span><span class="sxs-lookup"><span data-stu-id="96a62-464">General availability of 'Az.Kusto' module</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="96a62-465">Az.Network</span><span class="sxs-lookup"><span data-stu-id="96a62-465">Az.Network</span></span>
* <span data-ttu-id="96a62-466">[Viktig ändring] Uppdaterade nedanstående cmdlets för att justera resursens virtuella router och virtuella hubb</span><span class="sxs-lookup"><span data-stu-id="96a62-466">[Breaking Change] Updated below cmdlets to align resource virtual router and virtual hub</span></span>
    - <span data-ttu-id="96a62-467">"New-AzVirtualRouter":</span><span class="sxs-lookup"><span data-stu-id="96a62-467">'New-AzVirtualRouter':</span></span> 
        - <span data-ttu-id="96a62-468">Parametern-HostedSubnet har lagts till för att stödja underordnad resurs för IP-konfiguration</span><span class="sxs-lookup"><span data-stu-id="96a62-468">Added -HostedSubnet parameter to support IP configuration child resource</span></span>
        - <span data-ttu-id="96a62-469">-HostedGateway och -HostedGatewayId har tagits bort</span><span class="sxs-lookup"><span data-stu-id="96a62-469">deleted -HostedGateway and -HostedGatewayId</span></span>
    - <span data-ttu-id="96a62-470">'Get-AzVirtualRouter':</span><span class="sxs-lookup"><span data-stu-id="96a62-470">'Get-AzVirtualRouter':</span></span>
        - <span data-ttu-id="96a62-471">Parameteruppsättningen har lagts till på prenumerationsnivå</span><span class="sxs-lookup"><span data-stu-id="96a62-471">Added subscription level parameter set</span></span>
    - <span data-ttu-id="96a62-472">"Remove-AzVirtualRouter"</span><span class="sxs-lookup"><span data-stu-id="96a62-472">'Remove-AzVirtualRouter'</span></span>
    - <span data-ttu-id="96a62-473">"Add-AzVirtualRouterPeer"</span><span class="sxs-lookup"><span data-stu-id="96a62-473">'Add-AzVirtualRouterPeer'</span></span>
    - <span data-ttu-id="96a62-474">"Get-AzVirtualRouterPeer"</span><span class="sxs-lookup"><span data-stu-id="96a62-474">'Get-AzVirtualRouterPeer'</span></span>
    - <span data-ttu-id="96a62-475">"Remove-AzVirtualRouterPeer"</span><span class="sxs-lookup"><span data-stu-id="96a62-475">'Remove-AzVirtualRouterPeer'</span></span>
* <span data-ttu-id="96a62-476">Ny cmdlet har lagts till för Azure Express Route-port</span><span class="sxs-lookup"><span data-stu-id="96a62-476">Added new cmdlet for Azure Express Route Port</span></span>
    - <span data-ttu-id="96a62-477">"New-AzExpressRoutePortLOA"</span><span class="sxs-lookup"><span data-stu-id="96a62-477">'New-AzExpressRoutePortLOA'</span></span>
* <span data-ttu-id="96a62-478">Egenskapen RemoteBgpCommunities har lagts till i VirtualNetwork Peering-resursen</span><span class="sxs-lookup"><span data-stu-id="96a62-478">Added RemoteBgpCommunities property to the VirtualNetwork Peering Resource</span></span>
* <span data-ttu-id="96a62-479">Ändrade varningsmeddelandet för ”New-AzLoadBalancerFrontendIpConfig”, ”New-AzPublicIpAddress” och ”New-AzPublicIpPrefix”.</span><span class="sxs-lookup"><span data-stu-id="96a62-479">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>
* <span data-ttu-id="96a62-480">Lade till VpnGatewayIpConfigurations till "Get-AzVpnGateway"-utdata</span><span class="sxs-lookup"><span data-stu-id="96a62-480">Added VpnGatewayIpConfigurations to 'Get-AzVpnGateway' output</span></span>
* <span data-ttu-id="96a62-481">Åtgärdade bugg för "Set-AzApplicationGatewaySslCertificate" [#9488]</span><span class="sxs-lookup"><span data-stu-id="96a62-481">Fixed bug for 'Set-AzApplicationGatewaySslCertificate' [#9488]</span></span>
* <span data-ttu-id="96a62-482">Parametern "AllowActiveFTP" har lagts till i "AzureFirewall"</span><span class="sxs-lookup"><span data-stu-id="96a62-482">Added 'AllowActiveFTP' parameter to 'AzureFirewall'</span></span>
* <span data-ttu-id="96a62-483">Nedanstående kommandon för funktionen har uppdaterats: Aktivera konfiguration/borttagning för Internetsäkerhet på VirtualWan P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="96a62-483">Updated below commands for feature: Enable internet security set/remove on VirtualWan P2SVpnGateway.</span></span>
- <span data-ttu-id="96a62-484">"New-AzP2sVpnGateway" har uppdaterats": Den valfria växelparametern "EnableInternetSecurityFlag" har lagts till för kunder som anger värdet true för att aktivera Internetsäkerhet på P2SVpnGateway, som ska användas för plats-till-plats-klienter.</span><span class="sxs-lookup"><span data-stu-id="96a62-484">Updated 'New-AzP2sVpnGateway': Added optional switch parameter 'EnableInternetSecurityFlag' for customers to set true to enable internet security on P2SVpnGateway, which will be applied for Point to site clients.</span></span>
- <span data-ttu-id="96a62-485">"Update-AzP2sVpnGateway" har uppdaterats: De valfria växelparametrarna "EnableInternetSecurityFlag" eller "DisableInternetSecurityFlag" har lagts till för kunder som anger värdet true/false för att aktivera/inaktivera Internetsäkerhet på P2SVpnGateway, som ska användas för plats-till-plats-klienter.</span><span class="sxs-lookup"><span data-stu-id="96a62-485">Updated 'Update-AzP2sVpnGateway': Added optional switch parameters 'EnableInternetSecurityFlag' or 'DisableInternetSecurityFlag' for customers to set true/false to enable/disable internet security on P2SVpnGateway, which will be applied for Point to site clients.</span></span>
* <span data-ttu-id="96a62-486">Den nya cmdleten "Reset-AzP2sVpnGateway" har lagts till för att kunder ska kunna återställa/starta om sina VirtualWan-P2SVpnGateway för felsökning.</span><span class="sxs-lookup"><span data-stu-id="96a62-486">Added new cmdlet 'Reset-AzP2sVpnGateway' for customers to reset/reboot their VirtualWan P2SVpnGateway for troubleshooting.</span></span>
* <span data-ttu-id="96a62-487">Den nya cmdleten "Reset-AzVpnGateway" har lagts till för att kunder ska kunna återställa/starta om VirtualWan VpnGateway för felsökning.</span><span class="sxs-lookup"><span data-stu-id="96a62-487">Added new cmdlet 'Reset-AzVpnGateway' for customers to reset/reboot their VirtualWan VpnGateway for troubleshooting.</span></span>
* <span data-ttu-id="96a62-488">"Set-AzVirtualNetworkSubnetConfig" har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="96a62-488">Updated 'Set-AzVirtualNetworkSubnetConfig'</span></span>
    - <span data-ttu-id="96a62-489">Ange egenskaper för NSG och routningstabell för undernät till null om det anges explicit i parametrarna [#1548] [#9718]</span><span class="sxs-lookup"><span data-stu-id="96a62-489">Set NSG and Route Table properties of subnet to null if explicitly set in parameters [#1548][#9718]</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="96a62-490">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="96a62-490">Az.RecoveryServices</span></span>
* <span data-ttu-id="96a62-491">Åtgärdat borttagningstillståndet för säkerhetskopieringsobjekt.</span><span class="sxs-lookup"><span data-stu-id="96a62-491">Fixed the Delete State for workload Backup Items.</span></span>

#### <a name="azresources"></a><span data-ttu-id="96a62-492">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="96a62-492">Az.Resources</span></span>
* <span data-ttu-id="96a62-493">Lagt till saknad kontroll för Set-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="96a62-493">Added missing check for Set-AzRoleAssignment</span></span>
* <span data-ttu-id="96a62-494">Attribut som medför icke-bakåtkompatibel ändring har lagts till i parametern "SubscriptionId" i "Get-AzResourceGroupDeploymentOperation"</span><span class="sxs-lookup"><span data-stu-id="96a62-494">Added breaking change attribute to 'SubscriptionId' parameter of 'Get-AzResourceGroupDeploymentOperation'</span></span>
* <span data-ttu-id="96a62-495">Uppdaterat What-If-cmdlets i ARM-mall så att resursändringar av typen 'Ignorera' visas sist</span><span class="sxs-lookup"><span data-stu-id="96a62-495">Updated ARM template What-If cmdlets to show 'Ignore' resource changes last</span></span>
* <span data-ttu-id="96a62-496">Åtgärdat serialiseringsproblem med säkra parametrar och matrisparametrar för distributionscmdlets [#12773]</span><span class="sxs-lookup"><span data-stu-id="96a62-496">Fixed secure and array parameter serialization issues for deployment cmdlets [#12773]</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="96a62-497">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="96a62-497">Az.ServiceFabric</span></span>
* <span data-ttu-id="96a62-498">Nya cmdletar har lagts till för hanterade kluster och nodtyper:</span><span class="sxs-lookup"><span data-stu-id="96a62-498">Added new cmdlets for managed clusters and node types:</span></span>
    - <span data-ttu-id="96a62-499">"New-AzServiceFabricManagedCluster"</span><span class="sxs-lookup"><span data-stu-id="96a62-499">'New-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="96a62-500">"Get-AzServiceFabricManagedCluster"</span><span class="sxs-lookup"><span data-stu-id="96a62-500">'Get-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="96a62-501">"Set-AzServiceFabricManagedCluster"</span><span class="sxs-lookup"><span data-stu-id="96a62-501">'Set-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="96a62-502">"Remove-AzServiceFabricManagedCluster"</span><span class="sxs-lookup"><span data-stu-id="96a62-502">'Remove-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="96a62-503">"Add-AzServiceFabricManagedClusterClientCertificate"</span><span class="sxs-lookup"><span data-stu-id="96a62-503">'Add-AzServiceFabricManagedClusterClientCertificate'</span></span>
    - <span data-ttu-id="96a62-504">"Remove-AzServiceFabricManagedClusterClientCertificate"</span><span class="sxs-lookup"><span data-stu-id="96a62-504">'Remove-AzServiceFabricManagedClusterClientCertificate'</span></span>
    - <span data-ttu-id="96a62-505">"New-AzServiceFabricManagedNodeType"</span><span class="sxs-lookup"><span data-stu-id="96a62-505">'New-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="96a62-506">"Get-AzServiceFabricManagedNodeType"</span><span class="sxs-lookup"><span data-stu-id="96a62-506">'Get-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="96a62-507">"Set-AzServiceFabricManagedNodeType"</span><span class="sxs-lookup"><span data-stu-id="96a62-507">'Set-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="96a62-508">"Remove-AzServiceFabricManagedNodeType"</span><span class="sxs-lookup"><span data-stu-id="96a62-508">'Remove-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="96a62-509">"Add-AzServiceFabricManagedNodeTypeVMExtension"</span><span class="sxs-lookup"><span data-stu-id="96a62-509">'Add-AzServiceFabricManagedNodeTypeVMExtension'</span></span>
    - <span data-ttu-id="96a62-510">"Add-AzServiceFabricManagedNodeTypeVMSecret"</span><span class="sxs-lookup"><span data-stu-id="96a62-510">'Add-AzServiceFabricManagedNodeTypeVMSecret'</span></span>
    - <span data-ttu-id="96a62-511">"Remove-AzServiceFabricManagedNodeTypeVMExtension"</span><span class="sxs-lookup"><span data-stu-id="96a62-511">'Remove-AzServiceFabricManagedNodeTypeVMExtension'</span></span>
    - <span data-ttu-id="96a62-512">"Restart-AzServiceFabricManagedNodeTyp"</span><span class="sxs-lookup"><span data-stu-id="96a62-512">'Restart-AzServiceFabricManagedNodeTyp'</span></span>
* <span data-ttu-id="96a62-513">Service Fabric SDK har uppgraderats till version 1.2.0 som använder Service Fabric-resursprovidern med API-version 2020-03-01 för aktuell modell och 2020-01-01-förhandsversion för hanterade kluster.</span><span class="sxs-lookup"><span data-stu-id="96a62-513">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2020-03-01 for the current model and 2020-01-01-preview for managed clusters.</span></span>

#### <a name="azsql"></a><span data-ttu-id="96a62-514">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="96a62-514">Az.Sql</span></span>
* <span data-ttu-id="96a62-515">BackupStorageRedundancy har lagts till i "New-AzSqlInstance" och "Get-AzSqlInstance"</span><span class="sxs-lookup"><span data-stu-id="96a62-515">Added BackupStorageRedundancy to 'New-AzSqlInstance' and 'Get-AzSqlInstance'</span></span>
* <span data-ttu-id="96a62-516">Cmdlet:en "Get-AzSqlServerActiveDirectoryOnlyAuthentication" har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-516">Added cmdlet 'Get-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="96a62-517">Cmdlet:en "Enable-AzSqlServerActiveDirectoryOnlyAuthentication" har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-517">Added cmdlet 'Enable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="96a62-518">Force-parametern har lagts till i "New-AzSqlInstance"</span><span class="sxs-lookup"><span data-stu-id="96a62-518">Added Force parameter to 'New-AzSqlInstance'</span></span>
* <span data-ttu-id="96a62-519">Cmdlet:ar för logguppspelningstjänst för hanterade databaser har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-519">Added cmdlets for Managed Database Log Replay service</span></span>
    - <span data-ttu-id="96a62-520">"Start-AzSqlInstanceDatabaseLogReplay"</span><span class="sxs-lookup"><span data-stu-id="96a62-520">'Start-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="96a62-521">"Get-AzSqlInstanceDatabaseLogReplay"</span><span class="sxs-lookup"><span data-stu-id="96a62-521">'Get-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="96a62-522">"Complete-AzSqlInstanceDatabaseLogReplay"</span><span class="sxs-lookup"><span data-stu-id="96a62-522">'Complete-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="96a62-523">"Stop-AzSqlInstanceDatabaseLogReplay"</span><span class="sxs-lookup"><span data-stu-id="96a62-523">'Stop-AzSqlInstanceDatabaseLogReplay'</span></span>
* <span data-ttu-id="96a62-524">Cmdlet:en "Get-AzSqlInstanceActiveDirectoryOnlyAuthentication" har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-524">Added cmdlet 'Get-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="96a62-525">Cmdlet:en "Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication" har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-525">Added cmdlet 'Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="96a62-526">Cmdlet:en "Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication" har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-526">Added cmdlet 'Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="96a62-527">Cmdletarna "New-AzSqlDatabaseImport" och "New-AzSqlDatabaseExport" har uppdaterats för att stödja funktioner för nätverksisolering</span><span class="sxs-lookup"><span data-stu-id="96a62-527">Updated cmdlets 'New-AzSqlDatabaseImport' and 'New-AzSqlDatabaseExport' to support network isolation functionality</span></span>
* <span data-ttu-id="96a62-528">Cmdleten "New-AzSqlDatabaseImportExisting" har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-528">Added cmdlet 'New-AzSqlDatabaseImportExisting'</span></span>
* <span data-ttu-id="96a62-529">Uppdaterade databas-cmdlet:ar som stöder typspecifikation av lagringsenhet för säkerhetskopiering</span><span class="sxs-lookup"><span data-stu-id="96a62-529">Updated Databases cmdlets to support backup storage type specification</span></span>
* <span data-ttu-id="96a62-530">Force-parametern har lagts till i "New-AzSqlDatabase"</span><span class="sxs-lookup"><span data-stu-id="96a62-530">Added Force parameter to 'New-AzSqlDatabase'</span></span>
* <span data-ttu-id="96a62-531">Varning för BackupStorageRedundancy-konfiguration har lagts till i utvalda regioner i "New-AzSqlDatabase"</span><span class="sxs-lookup"><span data-stu-id="96a62-531">Added warning for BackupStorageRedundancy configuration in select regions in 'New-AzSqlDatabase'</span></span>
* <span data-ttu-id="96a62-532">Uppdaterade ActiveDirectoryOnlyAuthentication-cmdletar för server och instans så att de innehåller ResourceId och InputObject</span><span class="sxs-lookup"><span data-stu-id="96a62-532">Updated ActiveDirectoryOnlyAuthentication cmdlets for server and instance to include ResourceId and InputObject</span></span>

#### <a name="azstorage"></a><span data-ttu-id="96a62-533">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="96a62-533">Az.Storage</span></span>
* <span data-ttu-id="96a62-534">Åtgärdade fel vid uppladdning av blob genom uppgradering till Microsoft.Azure.Storage.DataMovement 2.0.0 [#12220]</span><span class="sxs-lookup"><span data-stu-id="96a62-534">Fixed upload blob fail by upgrade to Microsoft.Azure.Storage.DataMovement 2.0.0 [#12220]</span></span>
* <span data-ttu-id="96a62-535">Stöd för återställning baserat på tidpunkt</span><span class="sxs-lookup"><span data-stu-id="96a62-535">Supported Point In Time Restore</span></span>
    - <span data-ttu-id="96a62-536">"Enable-AzStorageBlobRestorePolicy"</span><span class="sxs-lookup"><span data-stu-id="96a62-536">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="96a62-537">"Disable-AzStorageBlobRestorePolicy"</span><span class="sxs-lookup"><span data-stu-id="96a62-537">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="96a62-538">"New-AzStorageBlobRangeToRestore"</span><span class="sxs-lookup"><span data-stu-id="96a62-538">'New-AzStorageBlobRangeToRestore'</span></span>
    - <span data-ttu-id="96a62-539">"Restore-AzStorageBlobRange"</span><span class="sxs-lookup"><span data-stu-id="96a62-539">'Restore-AzStorageBlobRange'</span></span>
* <span data-ttu-id="96a62-540">Stöd för att hämta status för blobåterställning genom att köra get-AzureRMStorageAccount med parametern -IncludeBlobRestoreStatus</span><span class="sxs-lookup"><span data-stu-id="96a62-540">Supported get blob restore status of Storage account by run get-AzureRMStorageAccount with parameter -IncludeBlobRestoreStatus</span></span> 
    - <span data-ttu-id="96a62-541">"Get-AzureRMStorageAccount"</span><span class="sxs-lookup"><span data-stu-id="96a62-541">'Get-AzureRMStorageAccount'</span></span>
* <span data-ttu-id="96a62-542">Meddelande om icke-bakåtkompatibel ändring för kommande ändring av cmdlet-utdata har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-542">Added breaking change warning message for upcoming cmdlet output change</span></span>
    - <span data-ttu-id="96a62-543">"Get-AzStorageContainerStoredAccessPolicy"</span><span class="sxs-lookup"><span data-stu-id="96a62-543">'Get-AzStorageContainerStoredAccessPolicy'</span></span>
    - <span data-ttu-id="96a62-544">"Set-AzStorageContainerStoredAccessPolicy"</span><span class="sxs-lookup"><span data-stu-id="96a62-544">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
    - <span data-ttu-id="96a62-545">"Set-AzStorageAccountManagementPolicy"</span><span class="sxs-lookup"><span data-stu-id="96a62-545">'Set-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="96a62-546">"Get-AzStorageAccountManagementPolicy"</span><span class="sxs-lookup"><span data-stu-id="96a62-546">'Get-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="96a62-547">"Add-AzStorageAccountManagementPolicyAction"</span><span class="sxs-lookup"><span data-stu-id="96a62-547">'Add-AzStorageAccountManagementPolicyAction'</span></span>
    - <span data-ttu-id="96a62-548">"New-AzStorageAccountManagementPolicyRule"</span><span class="sxs-lookup"><span data-stu-id="96a62-548">'New-AzStorageAccountManagementPolicyRule'</span></span>
* <span data-ttu-id="96a62-549">Uppgraderade Microsoft.Azure.Cosmos.Table SDK till 1.0.8</span><span class="sxs-lookup"><span data-stu-id="96a62-549">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.8</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="96a62-550">Tack till våra community-deltagare</span><span class="sxs-lookup"><span data-stu-id="96a62-550">Thanks to our community contributors</span></span>
* <span data-ttu-id="96a62-551">Thomas Van Laere (@ThomVanL), Lägg till Dockerfile-alpine-3.10 (#12911)</span><span class="sxs-lookup"><span data-stu-id="96a62-551">Thomas Van Laere (@ThomVanL), Add Dockerfile-alpine-3.10 (#12911)</span></span> 
* <span data-ttu-id="96a62-552">Lohith Chowdary Chilukuri (@Lochiluk), Uppdatering av Remove-AzNetworkInterfaceIpConfig.md (#12807)</span><span class="sxs-lookup"><span data-stu-id="96a62-552">Lohith Chowdary Chilukuri (@Lochiluk), Update Remove-AzNetworkInterfaceIpConfig.md (#12807)</span></span> 
* <span data-ttu-id="96a62-553">Roberth Strand (@roberthstrand), Get-AzResourceGroup – Nytt exempel och rensning (#12828)</span><span class="sxs-lookup"><span data-stu-id="96a62-553">Roberth Strand (@roberthstrand), Get-AzResourceGroup - New example, and cleanup (#12828)</span></span> 
* <span data-ttu-id="96a62-554">Ravi Mishra (@inmishrar), uppdatering av Azure Web App-körningsstack till DOTNETCORE (#12833)</span><span class="sxs-lookup"><span data-stu-id="96a62-554">Ravi Mishra (@inmishrar), update Azure Web App runtime stack to DOTNETCORE (#12833)</span></span> 
* <span data-ttu-id="96a62-555">@jack-education, uppdaterat set-AzVirtualNetworkSubnetConfig för att tillåta att NSG och routningstabell tas bort från undernät (#12351)</span><span class="sxs-lookup"><span data-stu-id="96a62-555">@jack-education, Updated Set-AzVirtualNetworkSubnetConfig to allow NSG and Route Table to be removed from subnet (#12351)</span></span> 
* <span data-ttu-id="96a62-556">@hagop-globanet, uppdatering av Add-AzApplicationGatewayCustomError.md (#12784)</span><span class="sxs-lookup"><span data-stu-id="96a62-556">@hagop-globanet, Update Add-AzApplicationGatewayCustomError.md (#12784)</span></span> 
* <span data-ttu-id="96a62-557">Joshua Van Daalen (@greenSacrifice)</span><span class="sxs-lookup"><span data-stu-id="96a62-557">Joshua Van Daalen (@greenSacrifice)</span></span>
  * <span data-ttu-id="96a62-558">Uppdatering av stavning av egenskaper till egenskaper (#12821)</span><span class="sxs-lookup"><span data-stu-id="96a62-558">Update spelling of Property to Property (#12821)</span></span> 
  * <span data-ttu-id="96a62-559">Uppdatering av New-AzResourceLock.md-exempel (#12806)</span><span class="sxs-lookup"><span data-stu-id="96a62-559">Update New-AzResourceLock.md examples (#12806)</span></span>
* <span data-ttu-id="96a62-560">Eragon Riddle (@eragonriddle), korrigerat fältnamn för parameter i exemplet (#12825)</span><span class="sxs-lookup"><span data-stu-id="96a62-560">Eragon Riddle (@eragonriddle), Corrected parameter field name in the example (#12825)</span></span> 
* <span data-ttu-id="96a62-561">@rossifumax, åtgärdat skrivfel i New-AzConfigurationAssignment.md (#12701)</span><span class="sxs-lookup"><span data-stu-id="96a62-561">@rossifumax, Fix typo in New-AzConfigurationAssignment.md (#12701)</span></span>

## <a name="461---august-2020"></a><span data-ttu-id="96a62-562">4.6.1 – augusti 2020</span><span class="sxs-lookup"><span data-stu-id="96a62-562">4.6.1 - August 2020</span></span>
#### <a name="azcompute"></a><span data-ttu-id="96a62-563">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="96a62-563">Az.Compute</span></span>
* <span data-ttu-id="96a62-564">Korrigerade EncryptionAtHost-parametern i New-AzVm för att ta bort standardvärdet FALSE [#12776]</span><span class="sxs-lookup"><span data-stu-id="96a62-564">Patched '-EncryptionAtHost' parameter in 'New-AzVm' to remove default value of false [#12776]</span></span>

## <a name="460---august-2020"></a><span data-ttu-id="96a62-565">4.6.0 – augusti 2020</span><span class="sxs-lookup"><span data-stu-id="96a62-565">4.6.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="96a62-566">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="96a62-566">Az.Accounts</span></span>
* <span data-ttu-id="96a62-567">Alla offentliga molnmiljöer läses in när slutpunktsidentifieringen inte returnerar AzureCloud (standard) eller andra offentliga miljöer [#12633]</span><span class="sxs-lookup"><span data-stu-id="96a62-567">Loaded all public cloud environments when discovery endpoint doesn't return default AzureCloud or other public environments [#12633]</span></span>
* <span data-ttu-id="96a62-568">SubscriptionPolicies har exponerats i Get-AzSubscription [#12551]</span><span class="sxs-lookup"><span data-stu-id="96a62-568">Exposed SubscriptionPolicies in 'Get-AzSubscription' [#12551]</span></span>

#### <a name="azautomation"></a><span data-ttu-id="96a62-569">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="96a62-569">Az.Automation</span></span>
* <span data-ttu-id="96a62-570">Parametern -RunOn har lagts till i Set-AzAutomationWebhook för att ange en Hybrid Worker-grupp</span><span class="sxs-lookup"><span data-stu-id="96a62-570">Added '-RunOn' parameters to 'Set-AzAutomationWebhook' to specify a Hybrid Worker Group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="96a62-571">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="96a62-571">Az.Compute</span></span>
* <span data-ttu-id="96a62-572">Parametern -EncryptionAtHost har lagts till i New-AzVm, New-AzVmss, New-AzVMConfig, New-AzVmssConfig, Update-AzVM och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="96a62-572">Added '-EncryptionAtHost' parameter to 'New-AzVm', 'New-AzVmss', 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVM', and 'Update-AzVmss'</span></span>
* <span data-ttu-id="96a62-573">SecurityProfile har lagts till i Get-AzVM och Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="96a62-573">Added 'SecurityProfile' to 'Get-AzVM' and 'Get-AzVmss' return object</span></span>
* <span data-ttu-id="96a62-574">Växeln -InstanceView har lagts till som valfri parameter i Get-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="96a62-574">Added '-InstanceView' switch as optional parameter to 'Get-AzHostGroup'</span></span>
* <span data-ttu-id="96a62-575">En ny cmdlet, Invoke-AzVmPatchAssessment, har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-575">Added new cmdlet 'Invoke-AzVmPatchAssessment'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="96a62-576">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="96a62-576">Az.DataFactory</span></span>
* <span data-ttu-id="96a62-577">Saknade egenskaper har lagts till i klassen PSPipelineRun.</span><span class="sxs-lookup"><span data-stu-id="96a62-577">Added missing properties to PSPipelineRun class.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="96a62-578">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="96a62-578">Az.HDInsight</span></span>
* <span data-ttu-id="96a62-579">Stöd för att skapa kluster med funktionen för kryptering under överföring.</span><span class="sxs-lookup"><span data-stu-id="96a62-579">Supported creating cluster with encryption at host feature.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="96a62-580">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="96a62-580">Az.KeyVault</span></span>
* <span data-ttu-id="96a62-581">Varningsmeddelanden har lagts till för planering att inaktivera mjuk borttagning</span><span class="sxs-lookup"><span data-stu-id="96a62-581">Added warning messages for planning to disable soft delete</span></span>
* <span data-ttu-id="96a62-582">Varningsmeddelanden har lagts till för planering att ta bort attributet SecretValueText</span><span class="sxs-lookup"><span data-stu-id="96a62-582">Added warning messages for planning to remove attribute SecretValueText</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="96a62-583">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="96a62-583">Az.Maintenance</span></span>
* <span data-ttu-id="96a62-584">Valfria schemarelaterade fält har lagts till i New-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="96a62-584">Added optional schedule related fields to 'New-AzMaintenanceConfiguration'</span></span>
* <span data-ttu-id="96a62-585">En ny cmdlet har lagts till för Get-AzMaintenancePublicConfiguration</span><span class="sxs-lookup"><span data-stu-id="96a62-585">Added new cmdlet for 'Get-AzMaintenancePublicConfiguration'</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="96a62-586">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="96a62-586">Az.ManagedServices</span></span>
* <span data-ttu-id="96a62-587">Varningar har lagts till om icke-bakåtkompatibla ändringar för cmdletar för tilldelning och definition av hanterade tjänster</span><span class="sxs-lookup"><span data-stu-id="96a62-587">Added breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="96a62-588">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="96a62-588">Az.Monitor</span></span>
* <span data-ttu-id="96a62-589">Utökade parametern som angetts i Set-AzDiagnosticSetting för separering av aktivering av loggar och mått [#12482]</span><span class="sxs-lookup"><span data-stu-id="96a62-589">Extended the parameter set in 'Set-AzDiagnosticSetting' for separation of Logs and Metrics enablement [#12482]</span></span>
* <span data-ttu-id="96a62-590">Åtgärdat fel för Add-AzMetricAlertRuleV2 vid hämtning av måttavisering från pipelinen</span><span class="sxs-lookup"><span data-stu-id="96a62-590">Fixed bug for 'Add-AzMetricAlertRuleV2' when getting metric alert from pipeline</span></span>

#### <a name="azresources"></a><span data-ttu-id="96a62-591">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="96a62-591">Az.Resources</span></span>
* <span data-ttu-id="96a62-592">Get-AzPolicyAlias-svaret har uppdaterats för att ta med information som anger om aliaset kan ändras eller inte av Azure Policy.</span><span class="sxs-lookup"><span data-stu-id="96a62-592">Updated 'Get-AzPolicyAlias' response to include information indicating whether the alias is modifiable by Azure Policy.</span></span>
* <span data-ttu-id="96a62-593">Skapade en ny cmdlet, set-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="96a62-593">Created new cmdlet 'Set-AzRoleAssignment'</span></span>
* <span data-ttu-id="96a62-594">Get-AzDeploymentManagementGroupWhatIfResult har lagts till för att hämta What-If-resultat för ARM-mall i hanteringsgruppsomfånget</span><span class="sxs-lookup"><span data-stu-id="96a62-594">Added 'Get-AzDeploymentManagementGroupWhatIfResult' for getting ARM template What-If results at management Group scope</span></span>
* <span data-ttu-id="96a62-595">En ny cmdlet, Get-AzTenantWhatIfResult, har lagts till för att hämta What-If-resultat för ARM-mall i klientorganisationsomfånget</span><span class="sxs-lookup"><span data-stu-id="96a62-595">Added 'Get-AzTenantWhatIfResult' new cmdlet for getting ARM template What-If results at tenant scope</span></span>
* <span data-ttu-id="96a62-596">-WhatIf och -Confirm har åsidosatts för New-AzManagementGroupDeployment och New-AzTenantDeployment för att använda What-If-resultat för ARM-mall</span><span class="sxs-lookup"><span data-stu-id="96a62-596">Overrode '-WhatIf' and '-Confirm' for 'New-AzManagementGroupDeployment' and 'New-AzTenantDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="96a62-597">Beteenden har åtgärdats för -WhatIf och -Confirm för nya cmdletar för distribution så att de stämmer överens med False och</span><span class="sxs-lookup"><span data-stu-id="96a62-597">Fixed the behaviors of '-WhatIf' and '-Confirm' for new deployment cmdlets so they comply with False and</span></span> 
* <span data-ttu-id="96a62-598">Serialiseringsfel har åtgärdats för -TemplateObject och TemplateParameterObject [#1528] [#6292]</span><span class="sxs-lookup"><span data-stu-id="96a62-598">Fixed serialization error for '-TemplateObject' and 'TemplateParameterObject' [#1528] [#6292]</span></span>
* <span data-ttu-id="96a62-599">Attribut som medför icke-bakåtkompatibel ändring har lagts till i Get-AzResourceGroupDeploymentOperation för den kommande ändringen av utdatatyp</span><span class="sxs-lookup"><span data-stu-id="96a62-599">Added breaking change attribute to 'Get-AzResourceGroupDeploymentOperation' for the upcoming output type change</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="96a62-600">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="96a62-600">Az.SignalR</span></span>
* <span data-ttu-id="96a62-601">Fel i hjälpfilerna Restart-AzSignalR och Update-AzSignalR har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="96a62-601">Fixed 'Restart-AzSignalR' and 'Update-AzSignalR' help files errors</span></span>
* <span data-ttu-id="96a62-602">Cmdletarna Update-AzSignalRNetworkAcl och Set-AzSignalRUpstream har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-602">Added cmdlets 'Update-AzSignalRNetworkAcl', 'Set-AzSignalRUpstream'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="96a62-603">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="96a62-603">Az.Storage</span></span>
* <span data-ttu-id="96a62-604">Stöd för blobfrågeacceleration</span><span class="sxs-lookup"><span data-stu-id="96a62-604">Supported blob query acceleration</span></span>
    -  <span data-ttu-id="96a62-605">Get-AzStorageBlobQueryResult</span><span class="sxs-lookup"><span data-stu-id="96a62-605">'Get-AzStorageBlobQueryResult'</span></span>
    -  <span data-ttu-id="96a62-606">New-AzStorageBlobQueryConfig</span><span class="sxs-lookup"><span data-stu-id="96a62-606">'New-AzStorageBlobQueryConfig'</span></span>
* <span data-ttu-id="96a62-607">Hjälpfil har lagts till, ytterligare beskrivning har lagts till och stavfel har korrigerats</span><span class="sxs-lookup"><span data-stu-id="96a62-607">Updated help file, added more description, and fixed typo</span></span>
    -  <span data-ttu-id="96a62-608">”Start-AzStorageBlobCopy”</span><span class="sxs-lookup"><span data-stu-id="96a62-608">'Start-AzStorageBlobCopy'</span></span>
    -  <span data-ttu-id="96a62-609">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="96a62-609">'Get-AzDataLakeGen2Item'</span></span>
* <span data-ttu-id="96a62-610">Problem med att ladda ned blob när relaterad underordnad katalog saknas har åtgärdats [#12592]</span><span class="sxs-lookup"><span data-stu-id="96a62-610">Fixed download blob fail when related sub directory not exist [#12592]</span></span>
    -  <span data-ttu-id="96a62-611">”Get-AzStorageBlobContent”</span><span class="sxs-lookup"><span data-stu-id="96a62-611">'Get-AzStorageBlobContent'</span></span>
* <span data-ttu-id="96a62-612">Replikeringsprincip för att ange, hämta, ta bort objekt på Storage-konton stöds</span><span class="sxs-lookup"><span data-stu-id="96a62-612">Supported Set/Get/Remove Object Replication Policy on Storage accounts</span></span>
    - <span data-ttu-id="96a62-613">New-AzStorageObjectReplicationPolicyRule</span><span class="sxs-lookup"><span data-stu-id="96a62-613">'New-AzStorageObjectReplicationPolicyRule'</span></span>
    - <span data-ttu-id="96a62-614">Set-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="96a62-614">'Set-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="96a62-615">Get-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="96a62-615">'Get-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="96a62-616">Remove-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="96a62-616">'Remove-AzStorageObjectReplicationPolicy'</span></span>
* <span data-ttu-id="96a62-617">Stöd har lagts till för att aktivera/inaktivera ChangeFeed i Blob Service för ett Storage-konto</span><span class="sxs-lookup"><span data-stu-id="96a62-617">Supported enable/disable ChangeFeed on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="96a62-618">”Update-AzStorageBlobServiceProperty”</span><span class="sxs-lookup"><span data-stu-id="96a62-618">'Update-AzStorageBlobServiceProperty'</span></span>

## <a name="450---august-2020"></a><span data-ttu-id="96a62-619">4.5.0 – augusti 2020</span><span class="sxs-lookup"><span data-stu-id="96a62-619">4.5.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="96a62-620">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="96a62-620">Az.Accounts</span></span>
* <span data-ttu-id="96a62-621">Uppdaterade ”Connect-AzAccount” så att det accepterar parametern ”MaxContextPopulation” [#9865]</span><span class="sxs-lookup"><span data-stu-id="96a62-621">Updated 'Connect-AzAccount' to accept parameter 'MaxContextPopulation' [#9865]</span></span>
* <span data-ttu-id="96a62-622">Uppdaterade SubscriptionClient-versionen till 2019-06-01 och visa klientdomäner [#9838]</span><span class="sxs-lookup"><span data-stu-id="96a62-622">Updated SubscriptionClient version to 2019-06-01 and display tenant domains [#9838]</span></span>
* <span data-ttu-id="96a62-623">Information om hemklientorganisation och managedBy-klientorganisation som stöds för prenumerationen</span><span class="sxs-lookup"><span data-stu-id="96a62-623">Supported home tenant and managedBy tenant information of subscription</span></span>
* <span data-ttu-id="96a62-624">Korrigerade modulnamn, versionsinformation i telemetridata</span><span class="sxs-lookup"><span data-stu-id="96a62-624">Corrected module name, version info in telemetry data</span></span>
* <span data-ttu-id="96a62-625">Justerade SqlDatabaseDnsSuffix och ServiceManagementUrl om miljöns slutpunkt för metadata returnerar ett inkompatibelt värde</span><span class="sxs-lookup"><span data-stu-id="96a62-625">Adjusted SqlDatabaseDnsSuffix and ServiceManagementUrl if environment metadata endpoint returns incompatible value</span></span>

#### <a name="azaks"></a><span data-ttu-id="96a62-626">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="96a62-626">Az.Aks</span></span>
* <span data-ttu-id="96a62-627">Tog bort ”ClientIdAndSecret” för ”ServicePrincipalIdAndSecret” och ställde in ”ClientIdAndSecret” som ett alias [#12381].</span><span class="sxs-lookup"><span data-stu-id="96a62-627">Removed 'ClientIdAndSecret' to 'ServicePrincipalIdAndSecret' and set 'ClientIdAndSecret' as an alias [#12381].</span></span>
* <span data-ttu-id="96a62-628">Tog bort ”Get-AzAks”/”New-AzAks”/”Remove-AzAks”/”Set-AzAks” för ”Get-AzAksCluster”/”New-AzAksCluster”/”Remove-AzAksCluster”/”Set-AzAksCluster” och ställde in de ursprungliga som alias [#12373].</span><span class="sxs-lookup"><span data-stu-id="96a62-628">Removed 'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks' to 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster' and set the original ones as alias [#12373].</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="96a62-629">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="96a62-629">Az.ApiManagement</span></span>
* <span data-ttu-id="96a62-630">Lade till ny cmdlet: ”Add-AzApiManagementApiToGateway”.</span><span class="sxs-lookup"><span data-stu-id="96a62-630">Added new 'Add-AzApiManagementApiToGateway' cmdlet.</span></span>
* <span data-ttu-id="96a62-631">Lade till ny cmdlet: ”Get-AzApiManagementGateway”.</span><span class="sxs-lookup"><span data-stu-id="96a62-631">Added new 'Get-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="96a62-632">Lade till ny cmdlet: ”Get-AzApiManagementGatewayHostnameConfiguration”.</span><span class="sxs-lookup"><span data-stu-id="96a62-632">Added new 'Get-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="96a62-633">Lade till ny cmdlet: ”Get-AzApiManagementGatewayKey”.</span><span class="sxs-lookup"><span data-stu-id="96a62-633">Added new 'Get-AzApiManagementGatewayKey' cmdlet.</span></span>
* <span data-ttu-id="96a62-634">Lade till ny cmdlet: ”New-AzApiManagementGateway”.</span><span class="sxs-lookup"><span data-stu-id="96a62-634">Added new 'New-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="96a62-635">Lade till ny cmdlet: ”New-AzApiManagementGatewayHostnameConfiguration”.</span><span class="sxs-lookup"><span data-stu-id="96a62-635">Added new 'New-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="96a62-636">Lade till ny cmdlet: ”New-AzApiManagementResourceLocationObject”.</span><span class="sxs-lookup"><span data-stu-id="96a62-636">Added new 'New-AzApiManagementResourceLocationObject' cmdlet.</span></span>
* <span data-ttu-id="96a62-637">Lade till ny cmdlet: ”Remove-AzApiManagementApiFromGateway”.</span><span class="sxs-lookup"><span data-stu-id="96a62-637">Added new 'Remove-AzApiManagementApiFromGateway' cmdlet.</span></span>
* <span data-ttu-id="96a62-638">Lade till ny cmdlet: ”Remove-AzApiManagementGateway”.</span><span class="sxs-lookup"><span data-stu-id="96a62-638">Added new 'Remove-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="96a62-639">Lade till ny cmdlet: ”Remove-AzApiManagementGatewayHostnameConfiguration”.</span><span class="sxs-lookup"><span data-stu-id="96a62-639">Added new 'Remove-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="96a62-640">Lade till ny cmdlet: ”Update-AzApiManagementGateway”.</span><span class="sxs-lookup"><span data-stu-id="96a62-640">Added new 'Update-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="96a62-641">Lade till den nya valfria parametern [-GatewayId] till cmdleten ”Get-AzApiManagementApi”.</span><span class="sxs-lookup"><span data-stu-id="96a62-641">Added new optional [-GatewayId] parameter to the 'Get-AzApiManagementApi' cmdlet.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="96a62-642">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="96a62-642">Az.CognitiveServices</span></span>
* <span data-ttu-id="96a62-643">Använde ”Neka” som standardåtgärd för NetworkRules.</span><span class="sxs-lookup"><span data-stu-id="96a62-643">Used 'Deny' specifically as NetworkRules default action.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="96a62-644">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="96a62-644">Az.FrontDoor</span></span>
* <span data-ttu-id="96a62-645">Åtgärdade ett problem där ett undantag uppstår när Enum.Parse försöker att tvinga ett null-värde till aktiverade eller inaktiverade uppräkningsvärden [#12344]</span><span class="sxs-lookup"><span data-stu-id="96a62-645">Fixed an issue where an exception is being thrown when Enum.Parse tries to coerce a null value to an Enabled or Disabled enum values [#12344]</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="96a62-646">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="96a62-646">Az.HDInsight</span></span>
* <span data-ttu-id="96a62-647">Stöd för att skapa kluster med funktionen Kryptering under överföring.</span><span class="sxs-lookup"><span data-stu-id="96a62-647">Supported creating cluster with encryption in transit feature.</span></span>
    - <span data-ttu-id="96a62-648">Lägg till den nya parametern ”EncryptionInTransit” till cmdleten ”New-AzHDInsightCluster”</span><span class="sxs-lookup"><span data-stu-id="96a62-648">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="96a62-649">Lägg till den nya parametern ”EncryptionInTransit” till cmdleten ”New-AzHDInsightClusterConfig”</span><span class="sxs-lookup"><span data-stu-id="96a62-649">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="96a62-650">Stöd för att skapa kluster med funktionen privat länk:</span><span class="sxs-lookup"><span data-stu-id="96a62-650">Supported creating cluster with private link feature:</span></span>
    - <span data-ttu-id="96a62-651">Lägg till de nya parametrarna ”PublicNetworkAccessType” och ”OutboundPublicNetworkAccessType” till cmdleten ”New-AzHDInsightCluster”</span><span class="sxs-lookup"><span data-stu-id="96a62-651">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="96a62-652">Lägg till de nya parametrarna ”PublicNetworkAccessType” och ”OutboundPublicNetworkAccessType” till cmdleten ”New-AzHDInsightClusterConfig”</span><span class="sxs-lookup"><span data-stu-id="96a62-652">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="96a62-653">Returnerade information om det virtuella nätverket vid anrop till ”New-AzHDInsightCluster” eller ”Get-AzHDInsightCluster”</span><span class="sxs-lookup"><span data-stu-id="96a62-653">Returned virtual network information when calling 'New-AzHDInsightCluster' or 'Get-AzHDInsightCluster'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="96a62-654">Az.Network</span><span class="sxs-lookup"><span data-stu-id="96a62-654">Az.Network</span></span>
* <span data-ttu-id="96a62-655">Stöd har lagts till för parametern AddressPrefixType i ”Remove-AzExpressRouteCircuitConnectionConfig”</span><span class="sxs-lookup"><span data-stu-id="96a62-655">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="96a62-656">Lade till bakåtkompatibel ändringar: PeerAddressType-funktioner för privat peering i ”Remove-AzExpressRouteCircutPeeringConfig”.</span><span class="sxs-lookup"><span data-stu-id="96a62-656">Added non-breaking changes: PeerAddressType functionality for Private Peering in 'Remove-AzExpressRouteCircutPeeringConfig'.</span></span>
* <span data-ttu-id="96a62-657">Koden ändrades för att ignorera skiftläge för parametrarna AddressPrefixType och PeerAddressType.</span><span class="sxs-lookup"><span data-stu-id="96a62-657">Code changed to ignore case for AddressPrefixType and PeerAddressType parameter.</span></span>
* <span data-ttu-id="96a62-658">Ändrade varningsmeddelandet för ”New-AzLoadBalancerFrontendIpConfig”, ”New-AzPublicIpAddress” och ”New-AzPublicIpPrefix”.</span><span class="sxs-lookup"><span data-stu-id="96a62-658">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="96a62-659">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="96a62-659">Az.OperationalInsights</span></span>
* <span data-ttu-id="96a62-660">Lade till alternativet ”-ForceDelete” för ”Remove-AzOperationalInsightsworkspace”</span><span class="sxs-lookup"><span data-stu-id="96a62-660">Added '-ForceDelete' option for 'Remove-AzOperationalInsightsworkspace'</span></span>
* <span data-ttu-id="96a62-661">Lade till ny cmdlet: ”Get-AzOperationalInsightsDeletedWorkspace”</span><span class="sxs-lookup"><span data-stu-id="96a62-661">Added new cmdlet 'Get-AzOperationalInsightsDeletedWorkspace'</span></span>
* <span data-ttu-id="96a62-662">Lade till ny cmdlet: ”Restore-AzOperationalInsightsWorkspace”</span><span class="sxs-lookup"><span data-stu-id="96a62-662">Added new cmdlet 'Restore-AzOperationalInsightsWorkspace'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="96a62-663">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="96a62-663">Az.RecoveryServices</span></span>
* <span data-ttu-id="96a62-664">Förbättrade sättet Azure Backup-containrar/objekt identifieras.</span><span class="sxs-lookup"><span data-stu-id="96a62-664">Improved the Azure Backup container/item discovery experience.</span></span>

#### <a name="azresources"></a><span data-ttu-id="96a62-665">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="96a62-665">Az.Resources</span></span>
* <span data-ttu-id="96a62-666">Lade till egenskaperna ”Condition”, ”ConditionVersion” och ”Description” till ”New-AzRoleAssignment”</span><span class="sxs-lookup"><span data-stu-id="96a62-666">Added properties 'Condition', 'ConditionVersion' and 'Description' to 'New-AzRoleAssignment'</span></span>
    - <span data-ttu-id="96a62-667">Detta omfattade alla relevanta ändringar av datamodellerna</span><span class="sxs-lookup"><span data-stu-id="96a62-667">This included all the relevant changes to the data models</span></span>

#### <a name="azsql"></a><span data-ttu-id="96a62-668">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="96a62-668">Az.Sql</span></span>
* <span data-ttu-id="96a62-669">Korrigerade ett potentiellt fel med skiftlägesokänsliga servernamn i ”New-AzSqlServer” och ”Set-AzSqlServer”</span><span class="sxs-lookup"><span data-stu-id="96a62-669">Fixed potential server name case insensitive error in 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="96a62-670">Korrigerade att fel databasnamn returnerades vid ett befintligt databasfel i ”New-AzSqlDatabaseSecondary”</span><span class="sxs-lookup"><span data-stu-id="96a62-670">Fixed wrong database name returned on existing database error in 'New-AzSqlDatabaseSecondary'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="96a62-671">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="96a62-671">Az.Storage</span></span>
* <span data-ttu-id="96a62-672">Stöd för att skapa container/blob för SAS-token med de nya behörigheterna x, t</span><span class="sxs-lookup"><span data-stu-id="96a62-672">Supported create container/blob Sas token with new permission x,t</span></span>
    -  <span data-ttu-id="96a62-673">”New-AzStorageBlobSASToken”</span><span class="sxs-lookup"><span data-stu-id="96a62-673">'New-AzStorageBlobSASToken'</span></span>
    -  <span data-ttu-id="96a62-674">”New-AzStorageContainerSASToken”</span><span class="sxs-lookup"><span data-stu-id="96a62-674">'New-AzStorageContainerSASToken'</span></span>
* <span data-ttu-id="96a62-675">Stöd för att skapa konto för SAS-token med de nya behörigheterna x, t, f</span><span class="sxs-lookup"><span data-stu-id="96a62-675">Supported create account Sas token with new permission x,t,f</span></span>
    -  <span data-ttu-id="96a62-676">”New-AzStorageAccountSASToken”</span><span class="sxs-lookup"><span data-stu-id="96a62-676">'New-AzStorageAccountSASToken'</span></span>
* <span data-ttu-id="96a62-677">Stöd för att hämta förbrukning av enskild filresurs</span><span class="sxs-lookup"><span data-stu-id="96a62-677">Supported get single file share usage</span></span>
    - <span data-ttu-id="96a62-678">”Get-AzRmStorageShare”</span><span class="sxs-lookup"><span data-stu-id="96a62-678">'Get-AzRmStorageShare'</span></span>

## <a name="440---july-2020"></a><span data-ttu-id="96a62-679">4.4.0 – juli 2020</span><span class="sxs-lookup"><span data-stu-id="96a62-679">4.4.0 - July 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="96a62-680">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="96a62-680">Az.Accounts</span></span>
* <span data-ttu-id="96a62-681">En ny cmdlet, ”Invoke-AzRestMethod”, har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-681">Added new cmdlet 'Invoke-AzRestMethod'</span></span>
* <span data-ttu-id="96a62-682">Ett problem åtgärdades som kan orsaka autentiseringsfel i scenarier med fler processer, t.ex. när flera Azure PowerShell-cmdletar körs med ”Start-Job” [#9448]</span><span class="sxs-lookup"><span data-stu-id="96a62-682">Fixed an issue that may cause authentication errors in multi-process scenarios such as running multiple Azure PowerShell cmdlets using 'Start-Job' [#9448]</span></span>

#### <a name="azaks"></a><span data-ttu-id="96a62-683">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="96a62-683">Az.Aks</span></span>
* <span data-ttu-id="96a62-684">Felet som gjorde att ”Get-AzAks” inte hämtade alla kluster har åtgärdats [#12296]</span><span class="sxs-lookup"><span data-stu-id="96a62-684">Fixed bug 'Get-AzAks' doesn't get all clusters [#12296]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="96a62-685">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="96a62-685">Az.AnalysisServices</span></span>
* <span data-ttu-id="96a62-686">Projektreferensen till autentisering har tagits bort</span><span class="sxs-lookup"><span data-stu-id="96a62-686">Removed project reference to Authentication</span></span>

#### <a name="azautomation"></a><span data-ttu-id="96a62-687">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="96a62-687">Az.Automation</span></span>
* <span data-ttu-id="96a62-688">Problemet som gjorde att strängar med escape-tecken inte kunde konverteras till JSON-objekt har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="96a62-688">Fixed the issue that string with escape chars cannot be converted into json object.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="96a62-689">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="96a62-689">Az.Compute</span></span>
* <span data-ttu-id="96a62-690">En varning har lats till som visas när ”New-AzVmss” används utan den senaste avbildningsversionen</span><span class="sxs-lookup"><span data-stu-id="96a62-690">Added warning when using 'New-AzVmss' without 'latest' image version</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="96a62-691">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="96a62-691">Az.DataFactory</span></span>
* <span data-ttu-id="96a62-692">Globala parametrar har lagts till för Data Factory.</span><span class="sxs-lookup"><span data-stu-id="96a62-692">Added global parameters to Data Factory.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="96a62-693">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="96a62-693">Az.EventGrid</span></span>
* <span data-ttu-id="96a62-694">Modulen har uppdaterats så att API-version 2020-06-01 används.</span><span class="sxs-lookup"><span data-stu-id="96a62-694">Updated to use the 2020-06-01 API version.</span></span>
* <span data-ttu-id="96a62-695">Nya funktioner har lagts till:</span><span class="sxs-lookup"><span data-stu-id="96a62-695">Added new features:</span></span>
    - <span data-ttu-id="96a62-696">Indatamappning</span><span class="sxs-lookup"><span data-stu-id="96a62-696">Input mapping</span></span>
    - <span data-ttu-id="96a62-697">Schema för händelseleverans</span><span class="sxs-lookup"><span data-stu-id="96a62-697">Event Delivery Schema</span></span>
    - <span data-ttu-id="96a62-698">Private Link</span><span class="sxs-lookup"><span data-stu-id="96a62-698">Private Link</span></span>
    - <span data-ttu-id="96a62-699">Cloud Event V10 Schema</span><span class="sxs-lookup"><span data-stu-id="96a62-699">Cloud Event V10 Schema</span></span>
    - <span data-ttu-id="96a62-700">Service Bus-ämne som mål</span><span class="sxs-lookup"><span data-stu-id="96a62-700">Service Bus Topic As Destination</span></span>
    - <span data-ttu-id="96a62-701">Azure-funktion som mål</span><span class="sxs-lookup"><span data-stu-id="96a62-701">Azure Function As Destination</span></span>
    - <span data-ttu-id="96a62-702">Webhook-batchbearbetning</span><span class="sxs-lookup"><span data-stu-id="96a62-702">WebHook Batching</span></span>
    - <span data-ttu-id="96a62-703">Säker webhook (AAD-stöd)</span><span class="sxs-lookup"><span data-stu-id="96a62-703">Secure webhook (AAD support)</span></span>
    - <span data-ttu-id="96a62-704">IpFiltering</span><span class="sxs-lookup"><span data-stu-id="96a62-704">IpFiltering</span></span>
* <span data-ttu-id="96a62-705">Uppdaterade cmdletar:</span><span class="sxs-lookup"><span data-stu-id="96a62-705">Updated cmdlets:</span></span>
    - <span data-ttu-id="96a62-706">”New-AzEventGridSubscription”/”Update-AzEventGridSubscription”:</span><span class="sxs-lookup"><span data-stu-id="96a62-706">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span></span>
        - <span data-ttu-id="96a62-707">Lägg till nya valfria parametrar för att ge stöd för webhook-batchbearbetning.</span><span class="sxs-lookup"><span data-stu-id="96a62-707">Add new optional parameters to support webhook batching.</span></span>
        - <span data-ttu-id="96a62-708">Lägg till nya valfria parametrar för att ge stöd för skyddad webhook med AAD.</span><span class="sxs-lookup"><span data-stu-id="96a62-708">Add new optional parameters to support secured webhook using AAD.</span></span>
        - <span data-ttu-id="96a62-709">Lägg till ny enum (uppräkning) för EndpointType-parametern för att ge stöd för Azure-funktion och Service Bus-ämne som nya mål.</span><span class="sxs-lookup"><span data-stu-id="96a62-709">Add new enum for EndpointType parameter to support azure function and service bus topic as new destinations.</span></span>
        - <span data-ttu-id="96a62-710">Lägg till ny valfri parameter för leveransschema.</span><span class="sxs-lookup"><span data-stu-id="96a62-710">Add new optional parameter for delivery schema.</span></span>
    - <span data-ttu-id="96a62-711">”New-AzEventGridTopic”/”Update-AzEventGridTopic” och ”New-AzEventGridDomain”/”Update-AzEventGridDomain”:</span><span class="sxs-lookup"><span data-stu-id="96a62-711">'New-AzEventGridTopic'/'Update-AzEventGridTopic' and 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span></span>
        - <span data-ttu-id="96a62-712">Lägg till nya valfria parametrar för att ge stöd för IpFiltering.</span><span class="sxs-lookup"><span data-stu-id="96a62-712">Add new optional parameters to support IpFiltering.</span></span>
    - <span data-ttu-id="96a62-713">”New-AzEventGridTopic”/”New-AzEventGridDomain”:</span><span class="sxs-lookup"><span data-stu-id="96a62-713">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span></span>
        - <span data-ttu-id="96a62-714">Lägg till nya valfria parametrar för att ge stöd för indatamappning.</span><span class="sxs-lookup"><span data-stu-id="96a62-714">Add new optional parameters to support Input mapping.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="96a62-715">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="96a62-715">Az.FrontDoor</span></span>
* <span data-ttu-id="96a62-716">Modulen har uppdaterats så att API 2020-05-01 används</span><span class="sxs-lookup"><span data-stu-id="96a62-716">Updated module to use API 2020-05-01</span></span>
* <span data-ttu-id="96a62-717">Stöd för privat länk har lagts till för Storage-, KeyVault- och Web App Service-resurser</span><span class="sxs-lookup"><span data-stu-id="96a62-717">Added Private link support for Storage, Keyvault and Web App Service resources</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="96a62-718">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="96a62-718">Az.HDInsight</span></span>
* <span data-ttu-id="96a62-719">Stöd för att skapa kluster med ADLSGen1/2-lagring i nationella moln.</span><span class="sxs-lookup"><span data-stu-id="96a62-719">Supported creating cluster with ADLSGen1/2 storage in national clouds.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="96a62-720">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="96a62-720">Az.Monitor</span></span>
* <span data-ttu-id="96a62-721">Bugg som orsakade fel med ”Get-AzDiagnosticSetting” när mått eller loggar var null har åtgärdats [#12272]</span><span class="sxs-lookup"><span data-stu-id="96a62-721">Fixed bug for 'Get-AzDiagnosticSetting' when metrics or logs are null [#12272]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="96a62-722">Az.Network</span><span class="sxs-lookup"><span data-stu-id="96a62-722">Az.Network</span></span>
* <span data-ttu-id="96a62-723">Parameterväxlingen i VWan HubVnet-anslutningar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="96a62-723">Fixed parameters swap in VWan HubVnet connection</span></span>
* <span data-ttu-id="96a62-724">Nya cmdletar har lagts till för platser för virtuella installationer i Azure-nätverk</span><span class="sxs-lookup"><span data-stu-id="96a62-724">Added new cmdlets for Azure Network Virtual Appliance Sites</span></span>
    - <span data-ttu-id="96a62-725">”Get-AzVirtualApplianceSite”</span><span class="sxs-lookup"><span data-stu-id="96a62-725">'Get-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="96a62-726">”New-AzVirtualApplianceSite”</span><span class="sxs-lookup"><span data-stu-id="96a62-726">'New-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="96a62-727">”Remove-AzVirtualApplianceSite”</span><span class="sxs-lookup"><span data-stu-id="96a62-727">'Remove-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="96a62-728">”Update-AzVirtualApplianceSite”</span><span class="sxs-lookup"><span data-stu-id="96a62-728">'Update-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="96a62-729">”New-AzOffice365PolicyProperty”</span><span class="sxs-lookup"><span data-stu-id="96a62-729">'New-AzOffice365PolicyProperty'</span></span>
* <span data-ttu-id="96a62-730">Nya cmdletar har lagts till för virtuella installationer i Azure-nätverk</span><span class="sxs-lookup"><span data-stu-id="96a62-730">Added new cmdlets for Azure Network Virtual Appliance</span></span>
    - <span data-ttu-id="96a62-731">”Get-AzNetworkVirtualAppliance”</span><span class="sxs-lookup"><span data-stu-id="96a62-731">'Get-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="96a62-732">”New-AzNetworkVirtualAppliance”</span><span class="sxs-lookup"><span data-stu-id="96a62-732">'New-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="96a62-733">”Remove-AzNetworkVirtualAppliance”</span><span class="sxs-lookup"><span data-stu-id="96a62-733">'Remove-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="96a62-734">”Update-AzNetworkVirtualAppliance”</span><span class="sxs-lookup"><span data-stu-id="96a62-734">'Update-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="96a62-735">”Get-AzNetworkVirtualApplianceSku”</span><span class="sxs-lookup"><span data-stu-id="96a62-735">'Get-AzNetworkVirtualApplianceSku'</span></span>
    - <span data-ttu-id="96a62-736">”New-AzVirtualApplianceSkuProperty”</span><span class="sxs-lookup"><span data-stu-id="96a62-736">'New-AzVirtualApplianceSkuProperty'</span></span>
* <span data-ttu-id="96a62-737">Application Gateway har introducerats i vanliga cmdletar för Private Link</span><span class="sxs-lookup"><span data-stu-id="96a62-737">Onboarded Application Gateway to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="96a62-738">StorageSync har introducerats i vanliga cmdletar för Private Link</span><span class="sxs-lookup"><span data-stu-id="96a62-738">Onboarded StorageSync to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="96a62-739">SignalR har introducerats i vanliga cmdletar för Private Link</span><span class="sxs-lookup"><span data-stu-id="96a62-739">Onboarded SignalR to Private Link Common Cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="96a62-740">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="96a62-740">Az.RecoveryServices</span></span>
* <span data-ttu-id="96a62-741">Projektreferensen till autentisering har tagits bort</span><span class="sxs-lookup"><span data-stu-id="96a62-741">Removed project reference to Authentication</span></span>
* <span data-ttu-id="96a62-742">Azure Backup-anpassade cmdletar gör text mer korrekt.</span><span class="sxs-lookup"><span data-stu-id="96a62-742">Azure Backup tuned cmdlets help text to be more accurate.</span></span>
* <span data-ttu-id="96a62-743">Stöd har lagts till som gör att Azure Backup kan hämta MAB-agentjobb med cmdleten ”Get-AzRecoveryServicesBackupJob”.</span><span class="sxs-lookup"><span data-stu-id="96a62-743">Azure Backup added support for fetching MAB agent jobs using 'Get-AzRecoveryServicesBackupJob' cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="96a62-744">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="96a62-744">Az.Resources</span></span>
* <span data-ttu-id="96a62-745">”Save-AzResourceGroupDeploymentTemplate” har uppdaterats för att använda SDK:n.</span><span class="sxs-lookup"><span data-stu-id="96a62-745">Updated 'Save-AzResourceGroupDeploymentTemplate' to use the SDK.</span></span>
* <span data-ttu-id="96a62-746">Cmdleten ”Unregister-AzResourceProvider” har lagts till.</span><span class="sxs-lookup"><span data-stu-id="96a62-746">Added 'Unregister-AzResourceProvider' cmdlet.</span></span>

#### <a name="azsql"></a><span data-ttu-id="96a62-747">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="96a62-747">Az.Sql</span></span>
* <span data-ttu-id="96a62-748">Stöd har lagts till för SPN och gästanvändare i cmdleten ”Set-AzSqlInstanceActiveDirectoryAdministrator”</span><span class="sxs-lookup"><span data-stu-id="96a62-748">Added support for Service principal and guest users in Set-AzSqlInstanceActiveDirectoryAdministrator cmdlet'</span></span>
* <span data-ttu-id="96a62-749">En bugg har åtgärdats i cmdletar för dataklassificering.</span><span class="sxs-lookup"><span data-stu-id="96a62-749">Fixed a bug in Data Classification cmdlets.'</span></span>
* <span data-ttu-id="96a62-750">Stöd har lagts till för redundansväxling med Azure SQL Managed Instance: ”Invoke-AzSqlInstanceFailover”</span><span class="sxs-lookup"><span data-stu-id="96a62-750">Added support for Azure SQL Managed Instance failover: 'Invoke-AzSqlInstanceFailover'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="96a62-751">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="96a62-751">Az.Storage</span></span>
* <span data-ttu-id="96a62-752">Problemet som gjorde att UserAgent inte lades till för vissa cmdletar för dataplanet har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="96a62-752">Fixed the issue that UserAgent is not added for some data plane cmdlets.</span></span>
* <span data-ttu-id="96a62-753">Stöd har lagts till för att skapa/uppdatera Storage-konto med MinimumTlsVersion och AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="96a62-753">Supported create/update Storage account with MinimumTlsVersion and AllowBlobPublicAccess</span></span>
    -  <span data-ttu-id="96a62-754">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="96a62-754">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="96a62-755">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="96a62-755">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="96a62-756">Stöd har lagts till för att aktivera/inaktivera versionshantering i Blob Service för ett Storage-konto</span><span class="sxs-lookup"><span data-stu-id="96a62-756">Support enable/disable versioning on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="96a62-757">”Update-AzStorageBlobServiceProperty”</span><span class="sxs-lookup"><span data-stu-id="96a62-757">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="96a62-758">Stöd har lagts till för att visa blobar med blobversioner</span><span class="sxs-lookup"><span data-stu-id="96a62-758">Support list blobs with blob versions</span></span>
    - <span data-ttu-id="96a62-759">”Get-AzStorageBlob”</span><span class="sxs-lookup"><span data-stu-id="96a62-759">'Get-AzStorageBlob'</span></span>
* <span data-ttu-id="96a62-760">Stöd har lagts till för att hämta/ta bort enskilda ögonblicksbilder av blobar eller blobversioner</span><span class="sxs-lookup"><span data-stu-id="96a62-760">Support get/remove single blob snapshot or blob version</span></span>
    - <span data-ttu-id="96a62-761">”Get-AzStorageBlob”</span><span class="sxs-lookup"><span data-stu-id="96a62-761">'Get-AzStorageBlob'</span></span>
    - <span data-ttu-id="96a62-762">”Remove-AzStorageBlob”</span><span class="sxs-lookup"><span data-stu-id="96a62-762">'Remove-AzStorageBlob'</span></span>
* <span data-ttu-id="96a62-763">Stöd har lagts till för pipelines från blobobjekt genererade av Azure.Storage.Blobs V12</span><span class="sxs-lookup"><span data-stu-id="96a62-763">Support pipeline from blob object generated from Azure.Storage.Blobs V12</span></span>
    - <span data-ttu-id="96a62-764">”Get-AzStorageBlobContent”</span><span class="sxs-lookup"><span data-stu-id="96a62-764">'Get-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="96a62-765">”New-AzStorageBlobSASToken”</span><span class="sxs-lookup"><span data-stu-id="96a62-765">'New-AzStorageBlobSASToken'</span></span>
    - <span data-ttu-id="96a62-766">”Remove-AzStorageBlob”</span><span class="sxs-lookup"><span data-stu-id="96a62-766">'Remove-AzStorageBlob'</span></span>
    - <span data-ttu-id="96a62-767">”Set-AzStorageBlobContent”</span><span class="sxs-lookup"><span data-stu-id="96a62-767">'Set-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="96a62-768">”Start-AzStorageBlobCopy”</span><span class="sxs-lookup"><span data-stu-id="96a62-768">'Start-AzStorageBlobCopy'</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="96a62-769">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="96a62-769">Az.StorageSync</span></span>
* <span data-ttu-id="96a62-770">En ny version har lagts till för StorageSync SDK som körs mot ApiVersion 2020-03-01</span><span class="sxs-lookup"><span data-stu-id="96a62-770">Added a new version StorageSync SDK targeting ApiVersion 2020-03-01</span></span>
* <span data-ttu-id="96a62-771">En cmdlet för synkroniseringstjänsten för lagringsuppdatering har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-771">Added Update Storage Sync Service cmdlet</span></span>
    - <span data-ttu-id="96a62-772">”Set-AzStorageSyncService”</span><span class="sxs-lookup"><span data-stu-id="96a62-772">'Set-AzStorageSyncService'</span></span>
* <span data-ttu-id="96a62-773">IncomingTrafficPolicy och PrivateEndpointConnections har lagts till för StorageSyncService-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="96a62-773">Added IncomingTrafficPolicy and PrivateEndpointConnections to StorageSyncService cmdlets.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="96a62-774">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="96a62-774">Az.Websites</span></span>
* <span data-ttu-id="96a62-775">Stöd har lagts till för att utföra åtgärder för platser som inte tillhör samma resursgrupp som App Services-planen</span><span class="sxs-lookup"><span data-stu-id="96a62-775">Added support to perform operations for Slots not in the same resource group as the App Service Plan</span></span>

## <a name="430---june-2020"></a><span data-ttu-id="96a62-776">4.3.0 – juni 2020</span><span class="sxs-lookup"><span data-stu-id="96a62-776">4.3.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="96a62-777">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="96a62-777">Az.Accounts</span></span>
* <span data-ttu-id="96a62-778">Stöd för identifiering av miljöinställning som standard och tillägg av miljön via ”Add-AzEnvironment”</span><span class="sxs-lookup"><span data-stu-id="96a62-778">Supported discovering environment setting by default and adding environment via 'Add-AzEnvironment'</span></span>
* <span data-ttu-id="96a62-779">Uppdatera förinlästa sammansättningar [#12024], [#11976]</span><span class="sxs-lookup"><span data-stu-id="96a62-779">Update preloaded assemblies [#12024], [#11976]</span></span>
* <span data-ttu-id="96a62-780">Uppdaterad Azure.Core-sammansättning</span><span class="sxs-lookup"><span data-stu-id="96a62-780">Updated Azure.Core assembly</span></span>
* <span data-ttu-id="96a62-781">Ett problem har åtgärdats som kan orsaka att ”Connect-AzAccount” misslyckas vid körning av flera trådar [#11201]</span><span class="sxs-lookup"><span data-stu-id="96a62-781">Fixed an issue that may cause 'Connect-AzAccount' to fail in multi-threaded execution [#11201]</span></span>

#### <a name="azaks"></a><span data-ttu-id="96a62-782">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="96a62-782">Az.Aks</span></span>
* <span data-ttu-id="96a62-783">Användning av gamla [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) ersattes med anrop till API:erna [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) och [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials)</span><span class="sxs-lookup"><span data-stu-id="96a62-783">Replaced usage of old [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) with calls to [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) and [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials) APIs</span></span>

#### <a name="azbatch"></a><span data-ttu-id="96a62-784">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="96a62-784">Az.Batch</span></span>
* <span data-ttu-id="96a62-785">Az.Batch har uppdaterats att använda ”Microsoft.Azure.Management.Batch” SDK till och med version 11.0.0.</span><span class="sxs-lookup"><span data-stu-id="96a62-785">Updated Az.Batch to use 'Microsoft.Azure.Management.Batch' SDK version to 11.0.0</span></span>
* <span data-ttu-id="96a62-786">Möjligheten att ange BatchAccount-identiteten har lagts till i cmdleten ”New-AzBatchAccount”</span><span class="sxs-lookup"><span data-stu-id="96a62-786">Added the ability to set the BatchAccount Identity in the 'New-AzBatchAccount' cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="96a62-787">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="96a62-787">Az.CognitiveServices</span></span>
* <span data-ttu-id="96a62-788">Stöd för att visa kontofunktioner.</span><span class="sxs-lookup"><span data-stu-id="96a62-788">Supported displaying account capabilities.</span></span>
* <span data-ttu-id="96a62-789">Stöd för att ändra PublicNetworkAccess.</span><span class="sxs-lookup"><span data-stu-id="96a62-789">Supported modifying PublicNetworkAccess.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="96a62-790">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="96a62-790">Az.Compute</span></span>
* <span data-ttu-id="96a62-791">Parametern SimulateEviction har lagts till i cmdletarna set-AzVM och set-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="96a62-791">Added SimulateEviction parameter to Set-AzVM and Set-AzVmssVM cmdlets.</span></span>
* <span data-ttu-id="96a62-792">”Premium_LRS” har lagts till i argumentslutföraren för parametern StorageAccountType för cmdleten New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="96a62-792">Added 'Premium_LRS' to the argument completer of StorageAccountType parameter for New-AzGalleryImageVersion cmdlet.</span></span>
* <span data-ttu-id="96a62-793">Understatusar har lagts till i VMCustomScriptExtension [#11297]</span><span class="sxs-lookup"><span data-stu-id="96a62-793">Added Substatuses to VMCustomScriptExtension [#11297]</span></span>
* <span data-ttu-id="96a62-794">”Delete” har lagts till i argumentslutföraren för parametern EvictionPolicy för cmdletarna New-AzVM och New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="96a62-794">Added 'Delete' to the argument completer of EvictionPolicy parameter for New-AzVM and New-AzVMConfig cmdlets.</span></span>
* <span data-ttu-id="96a62-795">Åtgärdat namn för nytt VM-tillägg för SAP</span><span class="sxs-lookup"><span data-stu-id="96a62-795">Fixed name of new VM Extension for SAP</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="96a62-796">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="96a62-796">Az.DataFactory</span></span>
* <span data-ttu-id="96a62-797">ADF .Net SDK har uppdaterats till 4.9.0</span><span class="sxs-lookup"><span data-stu-id="96a62-797">Updated ADF .Net SDK version to 4.9.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="96a62-798">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="96a62-798">Az.EventHub</span></span>
* <span data-ttu-id="96a62-799">Parametrar för hanterad identitet har lagts till i cmdletarna ”New-AzEventHubNamespace” och ”set-AzEventHubNamespace”</span><span class="sxs-lookup"><span data-stu-id="96a62-799">Added Managed Identity parameters to 'New-AzEventHubNamespace' and 'Set-AzEventHubNamespace' cmdlets</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="96a62-800">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="96a62-800">Az.Functions</span></span>
* <span data-ttu-id="96a62-801">Stöd har lagts till för att skapa PowerShell 7.0- och Java 11-funktionsappar</span><span class="sxs-lookup"><span data-stu-id="96a62-801">Added support to create PowerShell 7.0 and Java 11 function apps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="96a62-802">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="96a62-802">Az.HDInsight</span></span>
* <span data-ttu-id="96a62-803">Stöd för listning av värdar och omstart för specifika värdar i HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="96a62-803">Supported listing hosts and restart specific hosts of the HDInsight cluster.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="96a62-804">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="96a62-804">Az.HealthcareApis</span></span>
* <span data-ttu-id="96a62-805">Uppdaterade SDK-versionen till 1.1.0</span><span class="sxs-lookup"><span data-stu-id="96a62-805">Updated the SDK version to 1.1.0</span></span>
* <span data-ttu-id="96a62-806">Stöd har lagts till för exportinställningar och hanterad identitet</span><span class="sxs-lookup"><span data-stu-id="96a62-806">Added support for Export settings and Managed Identity</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="96a62-807">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="96a62-807">Az.Monitor</span></span>
* <span data-ttu-id="96a62-808">Parameter för inmatningsobjekt har åtgärdats för ”Set-AzActivityLogAlert”</span><span class="sxs-lookup"><span data-stu-id="96a62-808">Fixed input object parameter for 'Set-AzActivityLogAlert'</span></span>
* <span data-ttu-id="96a62-809">Parametern ”InputObject” har åtgärdats för ”Set-AzActionGroup” [#10868]</span><span class="sxs-lookup"><span data-stu-id="96a62-809">Fixed 'InputObject' parameter for 'Set-AzActionGroup' [#10868]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="96a62-810">Az.Network</span><span class="sxs-lookup"><span data-stu-id="96a62-810">Az.Network</span></span>
* <span data-ttu-id="96a62-811">Stöd har lagts till för parametern AddressPrefixType i ”Remove-AzExpressRouteCircuitConnectionConfig”</span><span class="sxs-lookup"><span data-stu-id="96a62-811">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="96a62-812">Nya cmdletar har lagts till för Azure FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="96a62-812">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="96a62-813">”New-AzFirewallPolicyDnsSetting”</span><span class="sxs-lookup"><span data-stu-id="96a62-813">'New-AzFirewallPolicyDnsSetting'</span></span>
    - <span data-ttu-id="96a62-814">Stöd för mål-FQDN i nätverksregler för brandväggsprincip</span><span class="sxs-lookup"><span data-stu-id="96a62-814">Support for Destination FQDN in Network Rules for Firewall Policy</span></span>
* <span data-ttu-id="96a62-815">Stöd har lagts till för åtgärder i serverdelsadresspooler</span><span class="sxs-lookup"><span data-stu-id="96a62-815">Added support for backend address pool operations</span></span>
    - <span data-ttu-id="96a62-816">”New-AzLoadBalancerBackendAddressConfig”</span><span class="sxs-lookup"><span data-stu-id="96a62-816">'New-AzLoadBalancerBackendAddressConfig'</span></span>
    - <span data-ttu-id="96a62-817">”New-AzLoadBalancerBackendAddressPool”</span><span class="sxs-lookup"><span data-stu-id="96a62-817">'New-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="96a62-818">”Set-AzLoadBalancerBackendAddressPool”</span><span class="sxs-lookup"><span data-stu-id="96a62-818">'Set-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="96a62-819">”Remove-AzLoadBalancerBackendAddressPool”</span><span class="sxs-lookup"><span data-stu-id="96a62-819">'Remove-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="96a62-820">”Get-AzLoadBalancerBackendAddressPool”</span><span class="sxs-lookup"><span data-stu-id="96a62-820">'Get-AzLoadBalancerBackendAddressPool'</span></span>
* <span data-ttu-id="96a62-821">Namnvalidering har lagts till för ”New-AzIpGroup”</span><span class="sxs-lookup"><span data-stu-id="96a62-821">Added name validation for 'New-AzIpGroup'</span></span>
* <span data-ttu-id="96a62-822">Nya cmdletar har lagts till för Azure FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="96a62-822">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="96a62-823">”New-AzFirewallPolicyThreatIntelWhitelist”</span><span class="sxs-lookup"><span data-stu-id="96a62-823">'New-AzFirewallPolicyThreatIntelWhitelist'</span></span>
* <span data-ttu-id="96a62-824">Nedanstående kommandon för funktionen har uppdaterats: Konfiguration/borttagning av anpassade DNS-servrar på VirtualWan P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="96a62-824">Updated below commands for feature: Custom dns servers set/remove on VirtualWan P2SVpnGateway.</span></span>
    - <span data-ttu-id="96a62-825">New-AzP2sVpnGateway har uppdaterats: Den valfria parametern ”-CustomDnsServer” har lagts till för att kunder ska kunna ange att deras DNS-servrar ska konfigureras på P2SVpnGateway, som kan användas av punkt-till-plats-klienter.</span><span class="sxs-lookup"><span data-stu-id="96a62-825">Updated New-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
    - <span data-ttu-id="96a62-826">Update-AzP2sVpnGateway har uppdaterats: Den valfria parametern ”-CustomDnsServer” har lagts till för att kunder ska kunna ange att deras DNS-servrar ska konfigureras på P2SVpnGateway, som kan användas av punkt-till-plats-klienter.</span><span class="sxs-lookup"><span data-stu-id="96a62-826">Updated Update-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
* <span data-ttu-id="96a62-827">”Update-AzVpnGateway” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="96a62-827">Updated 'Update-AzVpnGateway'</span></span>
    - <span data-ttu-id="96a62-828">Den valfria parametern ”-BgpPeeringAddress” har lagts till för att kunder ska kunna ange sina anpassade BGP:er som ska konfigurerar på VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="96a62-828">Added optional parameter '-BgpPeeringAddress' for customers to specify their custom bgps to set on VpnGateway.</span></span>
* <span data-ttu-id="96a62-829">Ny cmdlet har lagts till för att stödja återställning av en VirtualHub-resurs routningsstatus:</span><span class="sxs-lookup"><span data-stu-id="96a62-829">Added new cmdlet to support resetting the routing state of a VirtualHub resource:</span></span>
    - <span data-ttu-id="96a62-830">”Reset-AzHubRouter”</span><span class="sxs-lookup"><span data-stu-id="96a62-830">'Reset-AzHubRouter'</span></span>
* <span data-ttu-id="96a62-831">Nedanstående saker har uppdaterats baserat på den senaste Swagger-ändringen för brandväggspolicyn</span><span class="sxs-lookup"><span data-stu-id="96a62-831">Updated below things based on recent swagger change for Firewall Policy</span></span>
    - <span data-ttu-id="96a62-832">Namn ändras för RuleGroup, RuleCollectionGroup och RuleType</span><span class="sxs-lookup"><span data-stu-id="96a62-832">Changes names for RuleGroup, RuleCollectionGroup and RuleType</span></span>
    - <span data-ttu-id="96a62-833">Stöd har lagts till för NAT-regelsamlingar för brandväggsprincip så att flera NAT-regelsamlingar stöds</span><span class="sxs-lookup"><span data-stu-id="96a62-833">Added support for Firewall Policy NAT Rule Collections to support multiple NAT Rule Collection</span></span>
* <span data-ttu-id="96a62-834">[Icke-bakåtkompatibel ändring] Den obligatoriska parametern ”SourceIpGroup” har lagts till för ”New-AzFirewallPolicyApplicationRule” och ”New-AzFirewallPolicyNetworkRule”.</span><span class="sxs-lookup"><span data-stu-id="96a62-834">[Breaking Change] Added mandatory parameter 'SourceIpGroup' for 'New-AzFirewallPolicyApplicationRule' and 'New-AzFirewallPolicyNetworkRule'.</span></span>
* <span data-ttu-id="96a62-835">[Icke-bakåtkompatibel ändring] ”New-AzFirewallPolicyApplicationRule” har åtgärdats, parametern ”SourceAddress” är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="96a62-835">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="96a62-836">[Icke-bakåtkompatibel ändring] ”New-AzFirewallPolicyApplicationRule” har åtgärdats, parametern ”SourceAddress” är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="96a62-836">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="96a62-837">[Icke-bakåtkompatibel ändring] Obligatoriska parametrar har tagits bort: ”TranslatedAddress”, ”TranslatedPort” för ”New-AzFirewallPolicyNatRuleCollection”.</span><span class="sxs-lookup"><span data-stu-id="96a62-837">[Breaking Change] Removed mandatory parameters: 'TranslatedAddress', 'TranslatedPort' for 'New-AzFirewallPolicyNatRuleCollection'.</span></span>
* <span data-ttu-id="96a62-838">Nya cmdletar har lagts till för att stödja PrivateLink på Application Gateway</span><span class="sxs-lookup"><span data-stu-id="96a62-838">Added new cmdlets to support PrivateLink On Application Gateway</span></span>
    - <span data-ttu-id="96a62-839">”New-AzApplicationGatewayPrivateLinkConfiguration”</span><span class="sxs-lookup"><span data-stu-id="96a62-839">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="96a62-840">”Get-AzApplicationGatewayPrivateLinkConfiguration”</span><span class="sxs-lookup"><span data-stu-id="96a62-840">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="96a62-841">”New-AzApplicationGatewayPrivateLinkConfiguration”</span><span class="sxs-lookup"><span data-stu-id="96a62-841">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="96a62-842">”Set-AzApplicationGatewayPrivateLinkConfiguration”</span><span class="sxs-lookup"><span data-stu-id="96a62-842">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="96a62-843">”Remove-AzApplicationGatewayPrivateLinkConfiguration”</span><span class="sxs-lookup"><span data-stu-id="96a62-843">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="96a62-844">”New-AzApplicationGatewayPrivateLinkIpConfiguration”</span><span class="sxs-lookup"><span data-stu-id="96a62-844">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span></span>
* <span data-ttu-id="96a62-845">Nya cmdletar har lagts till för VirtualHubs underordnade resurs HubRouteTables.</span><span class="sxs-lookup"><span data-stu-id="96a62-845">Added new cmdlets for HubRouteTables child resource of VirtualHub.</span></span>
    - <span data-ttu-id="96a62-846">”New-AzVHubRoute”</span><span class="sxs-lookup"><span data-stu-id="96a62-846">'New-AzVHubRoute'</span></span>
    - <span data-ttu-id="96a62-847">”New-AzVHubRouteTable”</span><span class="sxs-lookup"><span data-stu-id="96a62-847">'New-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="96a62-848">”Get-AzVHubRouteTable”</span><span class="sxs-lookup"><span data-stu-id="96a62-848">'Get-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="96a62-849">”Update-AzVHubRouteTable”</span><span class="sxs-lookup"><span data-stu-id="96a62-849">'Update-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="96a62-850">”Remove-AzVHubRouteTable”</span><span class="sxs-lookup"><span data-stu-id="96a62-850">'Remove-AzVHubRouteTable'</span></span>
* <span data-ttu-id="96a62-851">Befintliga cmdletar har uppdaterats för att stödja valfri RoutingConfiguration-indataparameter för anpassad routning i VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="96a62-851">Updated existing cmdlets to support optional RoutingConfiguration input parameter for custom routing in VirtualWan.</span></span>
    - <span data-ttu-id="96a62-852">”New-AzExpressRouteConnection”</span><span class="sxs-lookup"><span data-stu-id="96a62-852">'New-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="96a62-853">”Set-AzExpressRouteConnection”</span><span class="sxs-lookup"><span data-stu-id="96a62-853">'Set-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="96a62-854">”New-AzVirtualHubVnetConnection”</span><span class="sxs-lookup"><span data-stu-id="96a62-854">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="96a62-855">”Update-AzVirtualHubVnetConnection”</span><span class="sxs-lookup"><span data-stu-id="96a62-855">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="96a62-856">”New-AzVpnConnection”</span><span class="sxs-lookup"><span data-stu-id="96a62-856">'New-AzVpnConnection'</span></span>
    - <span data-ttu-id="96a62-857">”Update-AzVpnConnection”</span><span class="sxs-lookup"><span data-stu-id="96a62-857">'Update-AzVpnConnection'</span></span>
    - <span data-ttu-id="96a62-858">”New-AzP2sVpnGateway”</span><span class="sxs-lookup"><span data-stu-id="96a62-858">'New-AzP2sVpnGateway'</span></span>
    - <span data-ttu-id="96a62-859">”Update-AzP2sVpnGateway”</span><span class="sxs-lookup"><span data-stu-id="96a62-859">'Update-AzP2sVpnGateway'</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="96a62-860">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="96a62-860">Az.OperationalInsights</span></span>
* <span data-ttu-id="96a62-861">Fast fel PSWorkspace implementerar inte IOperationalInsightsWorkspace [#12135]</span><span class="sxs-lookup"><span data-stu-id="96a62-861">Fixed bug PSWorkspace doesn't implement IOperationalInsightsWorkspace [#12135]</span></span>
* <span data-ttu-id="96a62-862">”pergb2018” har lagts till i uppsättningen med giltiga värden för parametern ”Sku” i ”Set-AzOperationalInsightsWorkspace”</span><span class="sxs-lookup"><span data-stu-id="96a62-862">Added 'pergb2018' to valid value set of parameter 'Sku' in 'Set-AzOperationalInsightsWorkspace'</span></span> 
* <span data-ttu-id="96a62-863">Alias ”FunctionParameters” lades till för parametern ”FunctionParameter” till</span><span class="sxs-lookup"><span data-stu-id="96a62-863">Added alias 'FunctionParameters' for parameter 'FunctionParameter' to</span></span>
    - <span data-ttu-id="96a62-864">”New-AzOperationalInsightsSavedSearch”</span><span class="sxs-lookup"><span data-stu-id="96a62-864">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="96a62-865">”Set-AzOperationalInsightsSavedSearch”</span><span class="sxs-lookup"><span data-stu-id="96a62-865">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="96a62-866">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="96a62-866">Az.RecoveryServices</span></span>
* <span data-ttu-id="96a62-867">Azure Backup har fått stöd för att hämta MAB-objekt.</span><span class="sxs-lookup"><span data-stu-id="96a62-867">Azure Backup added support for fetching MAB items.</span></span>
* <span data-ttu-id="96a62-868">Azure Site Recovery stöder disktypen ”StandardSSD_LRS”</span><span class="sxs-lookup"><span data-stu-id="96a62-868">Azure Site Recovery supports disk type 'StandardSSD_LRS'</span></span>

#### <a name="azresources"></a><span data-ttu-id="96a62-869">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="96a62-869">Az.Resources</span></span>
* <span data-ttu-id="96a62-870">”UsageLocation”, ”GivenName”, ”Surname”, ”AccountEnabled”, ”MailNickname”, ”Mail” på ”PSADUser” lades till [#10526] [#10497]</span><span class="sxs-lookup"><span data-stu-id="96a62-870">Added 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' on 'PSADUser' [#10526] [#10497]</span></span>
* <span data-ttu-id="96a62-871">Problem med att ”-Mail” inte fungerar på ”Get-AzADUser” har åtgärdats [#11981]</span><span class="sxs-lookup"><span data-stu-id="96a62-871">Fixed issue that '-Mail' doesn't work on 'Get-AzADUser' [#11981]</span></span>
* <span data-ttu-id="96a62-872">Parametern ”-ExcludeChangeType” har lagts till i ”Get-AzDeploymentWhatIfResult” och ”Get-AzResourceGroupDeploymentWhatIfResult”</span><span class="sxs-lookup"><span data-stu-id="96a62-872">Added '-ExcludeChangeType' parameter to 'Get-AzDeploymentWhatIfResult' and 'Get-AzResourceGroupDeploymentWhatIfResult'</span></span>
* <span data-ttu-id="96a62-873">Parametern ”-WhatIfExcludeChangeType” har lagts till i ”New-AzDeployment” och ”New-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="96a62-873">Added '-WhatIfExcludeChangeType' parameter to 'New-AzDeployment' and 'New-AzResourceGroupDeployment'</span></span>
* <span data-ttu-id="96a62-874">Cmdletar för ”Test-Az\*Deployment” har uppdaterats för att visa bättre felmeddelanden</span><span class="sxs-lookup"><span data-stu-id="96a62-874">Updated 'Test-Az\*Deployment' cmdlets to show better error messages</span></span>
* <span data-ttu-id="96a62-875">Hjälpmeddelandet för parametern ”-Name” i distributionsskapande och What If-cmdletar</span><span class="sxs-lookup"><span data-stu-id="96a62-875">Fixed help message for '-Name' parameter of deployment create and What-If cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="96a62-876">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="96a62-876">Az.Sql</span></span>
* <span data-ttu-id="96a62-877">Stöd för tjänsthuvudnamn har lagts till för administratörs-cmdlet för SQL Server Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="96a62-877">Added support for service principal for Set SQL Server Azure Active Directory Admin cmdlet</span></span>
* <span data-ttu-id="96a62-878">Synkroniseringsproblem i Data Classification-cmdletar har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="96a62-878">Fixed sync issue in Data Classification cmdlets.</span></span>
* <span data-ttu-id="96a62-879">Stöd för att söka efter användare via e-postadress på ”Set-AzSqlServerActiveDirectoryAdministrator” [#12192]</span><span class="sxs-lookup"><span data-stu-id="96a62-879">Supported searching user by mail on 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span></span>

#### <a name="azstorage"></a><span data-ttu-id="96a62-880">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="96a62-880">Az.Storage</span></span>
* <span data-ttu-id="96a62-881">Skapa lagringskonto med RequireInfrastructureEncryption stöds</span><span class="sxs-lookup"><span data-stu-id="96a62-881">Supported create Storage account with RequireInfrastructureEncryption</span></span>
    -  <span data-ttu-id="96a62-882">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="96a62-882">'New-AzStorageAccount'</span></span>
* <span data-ttu-id="96a62-883">Logiken för inläsning av Azure.Core flyttades till Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="96a62-883">Moved the logic of loading Azure.Core to Az.Accounts</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="96a62-884">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="96a62-884">Az.Websites</span></span>
* <span data-ttu-id="96a62-885">Skydd för att ta bort skapad webapp om återställningen misslyckades har lagts till i ”Restore-AzDeletedWebApp”</span><span class="sxs-lookup"><span data-stu-id="96a62-885">Added safeguard to delete created webapp if restore failed in 'Restore-AzDeletedWebApp'</span></span>
* <span data-ttu-id="96a62-886">”SourceWebApp.Location” har lagts till för ”New-AzWebApp” och ”New-AzWebAppSlot”</span><span class="sxs-lookup"><span data-stu-id="96a62-886">Added 'SourceWebApp.Location' for 'New-AzWebApp' and 'New-AzWebAppSlot'</span></span>
* <span data-ttu-id="96a62-887">Fel som förhindrade ändring av containerinställningar i ”Set-AzWebApp” och ”Set-AzWebAppSlot” har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="96a62-887">Fixed bug that prevented changing Container settings in 'Set-AzWebApp' and 'Set-AzWebAppSlot'</span></span>
* <span data-ttu-id="96a62-888">Ett fel för att hämta SiteConfig när -Name inte anges för Get-AzWebApp har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="96a62-888">Fixed bug to get SiteConfig when -Name is not given for Get-AzWebApp</span></span>
* <span data-ttu-id="96a62-889">Stöd har lagts till för att skapa ASP för Linux-appar</span><span class="sxs-lookup"><span data-stu-id="96a62-889">Added a support to create ASP for Linux Apps</span></span>
* <span data-ttu-id="96a62-890">Undantag har lagts till för kloning över resursgrupper</span><span class="sxs-lookup"><span data-stu-id="96a62-890">Added exceptions for clone across resource groups</span></span>

## <a name="420---june-2020"></a><span data-ttu-id="96a62-891">4.2.0 – juni 2020</span><span class="sxs-lookup"><span data-stu-id="96a62-891">4.2.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="96a62-892">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="96a62-892">Az.Accounts</span></span>
* <span data-ttu-id="96a62-893">Åtgärdade ett problem som kan få Az att hoppa över loggar i Azure Automation- eller PowerShell-jobb [#11492]</span><span class="sxs-lookup"><span data-stu-id="96a62-893">Fixed an issue that may cause Az to skip logs in Azure Automation or PowerShell jobs [#11492]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="96a62-894">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="96a62-894">Az.AnalysisServices</span></span>
* <span data-ttu-id="96a62-895">Uppdaterad sammansättningsversion för dataplan-cmdletar</span><span class="sxs-lookup"><span data-stu-id="96a62-895">Updated assembly version of data plane cmdlets</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="96a62-896">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="96a62-896">Az.ApiManagement</span></span>
* <span data-ttu-id="96a62-897">Uppdaterad sammansättningsversion för cmdletar för tjänsthantering</span><span class="sxs-lookup"><span data-stu-id="96a62-897">Updated assembly version of service management cmdlets</span></span>

#### <a name="azbilling"></a><span data-ttu-id="96a62-898">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="96a62-898">Az.Billing</span></span>
* <span data-ttu-id="96a62-899">Uppdaterad sammansättningsversion för förbrukningscmdletar</span><span class="sxs-lookup"><span data-stu-id="96a62-899">Updated assembly version of consumption cmdlets</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="96a62-900">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="96a62-900">Az.CognitiveServices</span></span>
* <span data-ttu-id="96a62-901">Stöd för PrivateEndpoint- och PublicNetworkAccess-kontroll.</span><span class="sxs-lookup"><span data-stu-id="96a62-901">Support PrivateEndpoint and PublicNetworkAccess control.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="96a62-902">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="96a62-902">Az.DataFactory</span></span>
* <span data-ttu-id="96a62-903">Uppdaterad sammansättningsversion för datafabrik V2-cmdletar</span><span class="sxs-lookup"><span data-stu-id="96a62-903">Updated assembly version of data factory V2 cmdlets</span></span>

#### <a name="azdatashare"></a><span data-ttu-id="96a62-904">Az.DataShare</span><span class="sxs-lookup"><span data-stu-id="96a62-904">Az.DataShare</span></span>
* <span data-ttu-id="96a62-905">Allmän tillgänglighet för modulen ”Az.DataShare”</span><span class="sxs-lookup"><span data-stu-id="96a62-905">General availability of ''Az.DataShare'' module</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="96a62-906">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="96a62-906">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="96a62-907">Allmän tillgänglighet för modulen ”Az.DesktopVirtualization”</span><span class="sxs-lookup"><span data-stu-id="96a62-907">General availability of ''Az.DesktopVirtualization'' module</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="96a62-908">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="96a62-908">Az.OperationalInsights</span></span>
* <span data-ttu-id="96a62-909">Uppgraderad SDK till 0.21.0</span><span class="sxs-lookup"><span data-stu-id="96a62-909">Upgraded SDK to 0.21.0</span></span>
* <span data-ttu-id="96a62-910">Lade till valfria parametrar till</span><span class="sxs-lookup"><span data-stu-id="96a62-910">Added optional parameters to</span></span> 
    - <span data-ttu-id="96a62-911">”New-AzOperationalInsightsSavedSearch”</span><span class="sxs-lookup"><span data-stu-id="96a62-911">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="96a62-912">”Set-AzOperationalInsightsSavedSearch”</span><span class="sxs-lookup"><span data-stu-id="96a62-912">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="96a62-913">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="96a62-913">Az.PolicyInsights</span></span>
* <span data-ttu-id="96a62-914">Korrigerade exempel 3 för ”Start-AzPolicyComplianceScan”</span><span class="sxs-lookup"><span data-stu-id="96a62-914">Corrected example 3 for 'Start-AzPolicyComplianceScan'</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="96a62-915">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="96a62-915">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="96a62-916">Uppdaterad sammansättningsversion för PowerBI-cmdletar</span><span class="sxs-lookup"><span data-stu-id="96a62-916">Updated assembly version of PowerBI cmdlets</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="96a62-917">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="96a62-917">Az.PrivateDns</span></span>
* <span data-ttu-id="96a62-918">Korrigerade formatering av utförlig utdatasträng för Remove-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="96a62-918">Corrected verbose output string formatting for Remove-AzPrivateDnsRecordSet</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="96a62-919">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="96a62-919">Az.RecoveryServices</span></span>
* <span data-ttu-id="96a62-920">Azure Site Recovery-stöd för att skapa en återställningsplan för replikering mellan zoner från xml-indata.</span><span class="sxs-lookup"><span data-stu-id="96a62-920">Azure Site Recovery support for creating recovery plan for zone to zone replication from xml input.</span></span>
* <span data-ttu-id="96a62-921">Uppdaterad sammansättningsversion för cmdletar för SiteRecovery och Backup</span><span class="sxs-lookup"><span data-stu-id="96a62-921">Updated assembly version of SiteRecovery and Backup cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="96a62-922">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="96a62-922">Az.Resources</span></span>
* <span data-ttu-id="96a62-923">Lade till slutparameter för cmdletarna Get-AzDeploymentScriptLog och Save-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="96a62-923">Added Tail parameter to Get-AzDeploymentScriptLog and Save-AzDeploymentScriptLog cmdlets</span></span>
* <span data-ttu-id="96a62-924">Formaterad utdataegenskap så att den kan visas i cmdlet-utdata för Get-AzDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="96a62-924">Formatted Output property and show it on the Get-AzDeploymentScript cmdlet output</span></span>
* <span data-ttu-id="96a62-925">Bytte namn på parametern -DeploymentScriptInputObject till -DeploymentScriptObject</span><span class="sxs-lookup"><span data-stu-id="96a62-925">Renamed -DeploymentScriptInputObject parameter to -DeploymentScriptObject</span></span>
* <span data-ttu-id="96a62-926">Åtgärdade saknade fil/målnamn i cmdlet-meddelanden.</span><span class="sxs-lookup"><span data-stu-id="96a62-926">Fixed missing file/target name in cmdlet messages.</span></span>
* <span data-ttu-id="96a62-927">Uppdaterad sammansättningsversion för cmdletar för resurshanterare och taggar</span><span class="sxs-lookup"><span data-stu-id="96a62-927">Updated assembly version of resource manager and tags cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="96a62-928">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="96a62-928">Az.Sql</span></span>
* <span data-ttu-id="96a62-929">Lade till UsePrivateLinkConnection till ”New-AzSqlSyncGroup”, ”Update-AzSqlSyncGroup”, ”New-AzSqlSyncMember” och ”Update-AzSqlSyncMember”</span><span class="sxs-lookup"><span data-stu-id="96a62-929">Added UsePrivateLinkConnection to 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="96a62-930">Lade till SyncMemberAzureDatabaseResourceId till ”New-AzSqlSyncMember” and ”Update-AzSqlSyncMember”</span><span class="sxs-lookup"><span data-stu-id="96a62-930">Added SyncMemberAzureDatabaseResourceId to 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="96a62-931">Lade till stöd för att söka efter gästanvändare för att ange administratörs-cmdlet för SQL Server Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="96a62-931">Added Guest user lookup support to Set SQL Server Azure Active Directory Admin cmdlet</span></span>

#### <a name="azstorage"></a><span data-ttu-id="96a62-932">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="96a62-932">Az.Storage</span></span>
* <span data-ttu-id="96a62-933">Uppdaterad sammansättningsversion för dataplan-cmdletar</span><span class="sxs-lookup"><span data-stu-id="96a62-933">Updated assembly version of data plane cmdlets</span></span>

## <a name="410---may-2020"></a><span data-ttu-id="96a62-934">4.1.0 – maj 2020</span><span class="sxs-lookup"><span data-stu-id="96a62-934">4.1.0 - May 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="96a62-935">Höjdpunkter sedan den senaste uppdateringen</span><span class="sxs-lookup"><span data-stu-id="96a62-935">Highlights since the last release</span></span>
* <span data-ttu-id="96a62-936">PowerShell-versioner som stöds: Windows PowerShell 5.1, PowerShell Core 6.2.4+ och PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="96a62-936">Supported PowerShell versions: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>
* <span data-ttu-id="96a62-937">Allmän tillgänglighet för Az.Functions</span><span class="sxs-lookup"><span data-stu-id="96a62-937">General availability of Az.Functions</span></span> 
* <span data-ttu-id="96a62-938">Nya stora uppdateringar har gjorts för Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources och Az.Storage</span><span class="sxs-lookup"><span data-stu-id="96a62-938">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources, and Az.Storage have major release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="96a62-939">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="96a62-939">Az.Accounts</span></span>
* <span data-ttu-id="96a62-940">”Add-AzEnvironment” och ”Set-AzEnvironment” har uppdaterats med stöd för parametrarna ”AzureSynapseAnalyticsEndpointResourceId” och ”AzureSynapseAnalyticsEndpointSuffix”</span><span class="sxs-lookup"><span data-stu-id="96a62-940">Updated 'Add-AzEnvironment' and 'Set-AzEnvironment' to accept parameters 'AzureSynapseAnalyticsEndpointResourceId' and 'AzureSynapseAnalyticsEndpointSuffix'</span></span>
* <span data-ttu-id="96a62-941">Azure.Core-relaterade sammansättningar har lagts till i Az.Accounts; PowerShell-plattformar som stöds är Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span><span class="sxs-lookup"><span data-stu-id="96a62-941">Added Azure.Core related assemblies into Az.Accounts, supported PowerShell platforms include Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span></span>

#### <a name="azaks"></a><span data-ttu-id="96a62-942">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="96a62-942">Az.Aks</span></span>
* <span data-ttu-id="96a62-943">API-versionen har uppgraderats till 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="96a62-943">Upgraded API Version to 2019-10-01</span></span>
* <span data-ttu-id="96a62-944">Stöds för att skapa AKS med hjälp av Windows-container</span><span class="sxs-lookup"><span data-stu-id="96a62-944">Supported to create AKS using Windows container</span></span>
* <span data-ttu-id="96a62-945">Nya cmdletar är tillgängliga: ”New-AzAksNodePool”, ”Update-AzAksNodePool”, ”Remove-AzAksNodePool”,        ”Get-AzAksNodePool”, ”Install-AzAksKubectl”, ”Get-AzAksVersion”</span><span class="sxs-lookup"><span data-stu-id="96a62-945">Provided new cmdlets: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="96a62-946">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="96a62-946">Az.ApiManagement</span></span>
* <span data-ttu-id="96a62-947">Parametrarna ”New-AzApiManagement” och ”Set-AzApiManagement”: [-AssignIdentity] har bytt namn till [-SystemAssignedIdentity]</span><span class="sxs-lookup"><span data-stu-id="96a62-947">'New-AzApiManagement' and 'Set-AzApiManagement': [-AssignIdentity] parameter renamed as [-SystemAssignedIdentity]</span></span>
* <span data-ttu-id="96a62-948">”New-AzApiManagement” och ”Set-AzApiManagement”: En ny parameter har lagts till: [-UserAssignedIdentity <String[]>]</span><span class="sxs-lookup"><span data-stu-id="96a62-948">'New-AzApiManagement' and 'Set-AzApiManagement': New parameter added: [-UserAssignedIdentity <String[]>]</span></span>
* <span data-ttu-id="96a62-949">”Get-AzApiManagementProperty” har bytt namn till ”Get-AzApiManagementNamedValue”.</span><span class="sxs-lookup"><span data-stu-id="96a62-949">'Get-AzApiManagementProperty': renamed as 'Get-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="96a62-950">PropertyId-parametern har bytt namn till NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="96a62-950">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="96a62-951">”New-AzApiManagementProperty” har bytt namn till ”New-AzApiManagementNamedValue”.</span><span class="sxs-lookup"><span data-stu-id="96a62-951">'New-AzApiManagementProperty': renamed as 'New-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="96a62-952">PropertyId-parametern har bytt namn till NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="96a62-952">PropertyId parameter renamed as NamedValueId.</span></span> 
* <span data-ttu-id="96a62-953">”Set-AzApiManagementProperty” har bytt namn till ”Set-AzApiManagementNamedValue”.</span><span class="sxs-lookup"><span data-stu-id="96a62-953">'Set-AzApiManagementProperty': renamed as 'Set-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="96a62-954">PropertyId-parametern har bytt namn till NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="96a62-954">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="96a62-955">”Remove-AzApiManagementProperty” har bytt namn till ”Remove-AzApiManagementNamedValue”.</span><span class="sxs-lookup"><span data-stu-id="96a62-955">'Remove-AzApiManagementProperty': renamed as 'Remove-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="96a62-956">PropertyId-parametern har bytt namn till NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="96a62-956">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="96a62-957">Den nya cmdleten Get-AzApiManagementAuthorizationServerClientSecret gör att ”Get-AzApiManagementAuthorizationServer” inte längre returnerar klienthemligheter.</span><span class="sxs-lookup"><span data-stu-id="96a62-957">Added new 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet and 'Get-AzApiManagementAuthorizationServer' will not return client secret anymore.</span></span>
* <span data-ttu-id="96a62-958">Den nya cmdleten ”Get-AzApiManagementNamedValueSecretValue” gör att ”Get-AzApiManagementNamedValue” inte returnerar värdet för en hemlighet.</span><span class="sxs-lookup"><span data-stu-id="96a62-958">Added new 'Get-AzApiManagementNamedValueSecretValue' cmdlet and 'Get-AzApiManagementNamedValue' will not return secret value.</span></span>
* <span data-ttu-id="96a62-959">Den nya cmdleten ”Get-AzApiManagementOpenIdConnectProviderClientSecret” gör att ”Get-AzApiManagementOpenIdConnectProvider” inte längre returnerar klienthemligheter.</span><span class="sxs-lookup"><span data-stu-id="96a62-959">Added new 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet and 'Get-AzApiManagementOpenIdConnectProvider' will not return client secret anymore.</span></span>
* <span data-ttu-id="96a62-960">Den nya cmdleten ”Get-AzApiManagementSubscriptionKey” gör att ”Get-AzApiManagementSubscription” inte längre returnerar prenumerationsnycklar.</span><span class="sxs-lookup"><span data-stu-id="96a62-960">Added new 'Get-AzApiManagementSubscriptionKey' cmdlet and 'Get-AzApiManagementSubscription' will not return subscription keys anymore.</span></span>
* <span data-ttu-id="96a62-961">Den nya cmdleten ”Get-AzApiManagementTenantAccessSecret” gör att ”Get-AzApiManagementTenantAccess” inte längre returnerar nycklar.</span><span class="sxs-lookup"><span data-stu-id="96a62-961">Added new 'Get-AzApiManagementTenantAccessSecret' cmdlet and 'Get-AzApiManagementTenantAccess' will not return keys anymore.</span></span>
* <span data-ttu-id="96a62-962">Den nya cmdleten ”Get-AzApiManagementTenantGitAccessSecret” gör att ”Get-AzApiManagementTenantGitAccess” inte längre returnerar nycklar.</span><span class="sxs-lookup"><span data-stu-id="96a62-962">Added new 'Get-AzApiManagementTenantGitAccessSecret' cmdlet and 'Get-AzApiManagementTenantGitAccess' will not return keys anymore.</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="96a62-963">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="96a62-963">Az.ApplicationInsights</span></span>
* <span data-ttu-id="96a62-964">Tillagda parametrar: ”RetentionInDays” ”PublicNetworkAccessForIngestion” ”PublicNetworkAccessForQuery” för ”New-AzApplicationInsights”</span><span class="sxs-lookup"><span data-stu-id="96a62-964">Added Parameters: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span></span>
* <span data-ttu-id="96a62-965">Cmdleten ”Update-AzApplicationInsights” har skapats</span><span class="sxs-lookup"><span data-stu-id="96a62-965">Created cmdlet 'Update-AzApplicationInsights'</span></span>
* <span data-ttu-id="96a62-966">Cmdletar har skapats för länkat lagringskonto</span><span class="sxs-lookup"><span data-stu-id="96a62-966">Created cmdlets for Linked Storage Account</span></span>

#### <a name="azbatch"></a><span data-ttu-id="96a62-967">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="96a62-967">Az.Batch</span></span>
* <span data-ttu-id="96a62-968">Az.Batch har uppdaterats att använda ”Microsoft.Azure.Batch” SDK version 13.0.0 och ”Microsoft.Azure.Management.Batch” SDK version 9.0.0.</span><span class="sxs-lookup"><span data-stu-id="96a62-968">Updated Az.Batch to use 'Microsoft.Azure.Batch' SDK version 13.0.0 and 'Microsoft.Azure.Management.Batch' SDK version 9.0.0.</span></span>
* <span data-ttu-id="96a62-969">Nu kan du välja vilken typ av certifikat du lägger till genom att använda den nya parametern ”-CertificateKind” med ”New-AzBatchCertificate”.</span><span class="sxs-lookup"><span data-stu-id="96a62-969">Added the ability to select the kind of certificate being added using the new '-CertificateKind' parameter to 'New-AzBatchCertificate'.</span></span>
* <span data-ttu-id="96a62-970">Egenskapen ”ApplicationPackages” har tagits bort från ”PSApplication”, som tidigare alltid var ''.</span><span class="sxs-lookup"><span data-stu-id="96a62-970">Removed 'ApplicationPackages' property from 'PSApplication' which was previously always ''.</span></span>
  - <span data-ttu-id="96a62-971">Specifika paket i ett program kan nu hämtas med hjälp av ”Get-AzBatchApplicationPackage”.</span><span class="sxs-lookup"><span data-stu-id="96a62-971">The specific packages inside of an application now can be retrieved using 'Get-AzBatchApplicationPackage'.</span></span> <span data-ttu-id="96a62-972">Till exempel: ”Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication”.</span><span class="sxs-lookup"><span data-stu-id="96a62-972">For example: 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span></span>
* <span data-ttu-id="96a62-973">Nu när du skapar en pool med hjälp av ”New-AzBatchPool” kan egenskapen ”VirtualMachineImageId” för ”PSImageReference” endast referera till en Shared Image Gallery-avbildning.</span><span class="sxs-lookup"><span data-stu-id="96a62-973">When creating a pool using 'New-AzBatchPool', the 'VirtualMachineImageId' property of 'PSImageReference' can now only refer to a Shared Image Gallery image.</span></span>
* <span data-ttu-id="96a62-974">När du skapar en pool med hjälp av ”New-AzBatchPool” kan poolen etableras utan en offentlig IP-adress med hjälp av den nya egenskapen ”PublicIPAddressConfiguration” för ”PSNetworkConfiguration”.</span><span class="sxs-lookup"><span data-stu-id="96a62-974">When creating a pool using 'New-AzBatchPool', the pool can be provisioned without a public IP using the new 'PublicIPAddressConfiguration' property of 'PSNetworkConfiguration'.</span></span>
  - <span data-ttu-id="96a62-975">Egenskapen ”PublicIPs” för ”PSNetworkConfiguration” har också flyttats till ”PSPublicIPAddressConfiguration”.</span><span class="sxs-lookup"><span data-stu-id="96a62-975">The 'PublicIPs' property of 'PSNetworkConfiguration' has moved in to 'PSPublicIPAddressConfiguration' as well.</span></span> <span data-ttu-id="96a62-976">Den här egenskapen kan bara anges om ”IPAddressProvisioningType” är ”UserManaged”.</span><span class="sxs-lookup"><span data-stu-id="96a62-976">This property can only be specified if 'IPAddressProvisioningType' is 'UserManaged'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="96a62-977">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="96a62-977">Az.Compute</span></span>
* <span data-ttu-id="96a62-978">Parametern HostId har lagts till för cmdleten ”Update-AzVM”t</span><span class="sxs-lookup"><span data-stu-id="96a62-978">Added HostId parameter to 'Update-AzVM' cmdlet</span></span>
* <span data-ttu-id="96a62-979">Hjälpdokumenten har uppdaterats för cmdletarna ”New-AzVMConfig”, ”New-AzVmssConfig”, ”Update-AzVmss”, ”Set-AzVMOperatingSystem” och ”Set-AzVmssOsProfile”.</span><span class="sxs-lookup"><span data-stu-id="96a62-979">Updated Help documents for 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' and 'Set-AzVmssOsProfile' cmdlets.</span></span>
* <span data-ttu-id="96a62-980">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="96a62-980">Breaking changes</span></span>
    - <span data-ttu-id="96a62-981">Parametern FilterExpression tas bort från cmdleten ”Get-AzVMImage”.</span><span class="sxs-lookup"><span data-stu-id="96a62-981">FilterExpression parameter is removed from 'Get-AzVMImage' cmdlet.</span></span>
    - <span data-ttu-id="96a62-982">Parametern AssignIdentity tas bort från cmdletarna ”New-AzVmssConfig”, ”New-AzVMConfig” och ”Update-AzVM”.</span><span class="sxs-lookup"><span data-stu-id="96a62-982">AssignIdentity parameter is removed from 'New-AzVmssConfig', 'New-AzVMConfig' and 'Update-AzVM' cmdlets.</span></span>
    - <span data-ttu-id="96a62-983">AutomaticRepairMaxInstanceRepairsPercent tas bort från cmdletarna ”New-AzVmssConfig” och ”Update-AzVmss”.</span><span class="sxs-lookup"><span data-stu-id="96a62-983">AutomaticRepairMaxInstanceRepairsPercent is removed from 'New-AzVmssConfig' and 'Update-AzVmss' cmdlets.</span></span>
    - <span data-ttu-id="96a62-984">Egenskaperna AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus och VirtualMachineScaleSetsColocationStatus tas bort från ProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="96a62-984">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus and VirtualMachineScaleSetsColocationStatus properties are removed from ProximityPlacementGroup.</span></span>
    - <span data-ttu-id="96a62-985">Egenskapen MaxInstanceRepairsPercent tas bort från AutomaticRepairsPolicy.</span><span class="sxs-lookup"><span data-stu-id="96a62-985">MaxInstanceRepairsPercent property is removed from AutomaticRepairsPolicy.</span></span>
    - <span data-ttu-id="96a62-986">Typerna AvailabilitySets, VirtualMachines och VirtualMachineScaleSets ändras från IList<SubResource> till IList<SubResourceWithColocationStatus>.</span><span class="sxs-lookup"><span data-stu-id="96a62-986">The types of AvailabilitySets, VirtualMachines and VirtualMachineScaleSets are changed from IList<SubResource> to IList<SubResourceWithColocationStatus>.</span></span>
* <span data-ttu-id="96a62-987">Beskrivningen för cmdleten ”Get-AzVM” har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="96a62-987">Description for 'Get-AzVM' cmdlet has been updated to better describe it.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="96a62-988">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="96a62-988">Az.DataFactory</span></span>
* <span data-ttu-id="96a62-989">CRUD-stöd för egenskaper för dataflödeskörning  i hanterad IR.</span><span class="sxs-lookup"><span data-stu-id="96a62-989">Supported CRUD of data flow runtime properties in Managed IR.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="96a62-990">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="96a62-990">Az.FrontDoor</span></span>
* <span data-ttu-id="96a62-991">Nya cmdletar har lagts till för att skapa, uppdatera, hämta och ta bort (CRUD) Front Door-regelmotorobjekt</span><span class="sxs-lookup"><span data-stu-id="96a62-991">Added new cmdlets for creation, update, retreival, and deletion of Front Door Rules Engine object</span></span>
* <span data-ttu-id="96a62-992">Hjälp-cmdletar har lagts till för konstruktion av Front Door-regelmotorobjekt</span><span class="sxs-lookup"><span data-stu-id="96a62-992">Added helper cmdlets for construction of Front Door Rules Engine object</span></span>
* <span data-ttu-id="96a62-993">Regelmotorreferens har lagts till för Front Door-hanteringsregelobjekt.</span><span class="sxs-lookup"><span data-stu-id="96a62-993">Added Rules Engine reference to Front Door Routing Rule object.</span></span>
* <span data-ttu-id="96a62-994">Parametrar för Private Link har lagts till för Front Door-serverdelsobjekt</span><span class="sxs-lookup"><span data-stu-id="96a62-994">Added Private Link parameters to Front Door Backend object</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="96a62-995">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="96a62-995">Az.Functions</span></span>
* <span data-ttu-id="96a62-996">Allmän tillgänglighet för ”Az.Functions”-modulen</span><span class="sxs-lookup"><span data-stu-id="96a62-996">General availability of ''Az.Functions'' module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="96a62-997">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="96a62-997">Az.HDInsight</span></span>
* <span data-ttu-id="96a62-998">Stöd för diskkryptering med kundhanterad nyckel.</span><span class="sxs-lookup"><span data-stu-id="96a62-998">Supported Customer-managed key disk encryption.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="96a62-999">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="96a62-999">Az.HealthcareApis</span></span>
* <span data-ttu-id="96a62-1000">Åtkomstprinciper använder inte längre det aktiva huvudkontot som standard</span><span class="sxs-lookup"><span data-stu-id="96a62-1000">Access policies are no longer defaulted to the current principal</span></span>

#### <a name="aziothub"></a><span data-ttu-id="96a62-1001">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="96a62-1001">Az.IotHub</span></span>
* <span data-ttu-id="96a62-1002">En cmdlet har lagts till som anropar en fråga i en IoT-hubb för att hämta information med ett SQL-liknande språk.</span><span class="sxs-lookup"><span data-stu-id="96a62-1002">Added cmdlet to invoke a query in an IoT hub to retrieve information using a SQL-like language.</span></span>
* <span data-ttu-id="96a62-1003">Problemet som gjorde att ”Add-AzIotHubDevice” inte skapade en Edge-aktiverad enhet utan underordnade enheter har åtgärdats [#11597]</span><span class="sxs-lookup"><span data-stu-id="96a62-1003">Fix issue that 'Add-AzIotHubDevice' fails to create Edge Enabled Device without child devices [#11597]</span></span>
* <span data-ttu-id="96a62-1004">En cmdlet har lagts till för att generera SAS-token för en Iot-hubb, enhet eller modul.</span><span class="sxs-lookup"><span data-stu-id="96a62-1004">Added cmdlet to generate SAS token for Iot Hub, device or module.</span></span>
* <span data-ttu-id="96a62-1005">En cmdlet har lagts till för att anropa en måttfråga om konfiguration.</span><span class="sxs-lookup"><span data-stu-id="96a62-1005">Added cmdlet to invoke configuration metrics query.</span></span>
* <span data-ttu-id="96a62-1006">Hantera automatisk distribution av IoT Edge i stor skala.</span><span class="sxs-lookup"><span data-stu-id="96a62-1006">Manage IoT Edge automatic deployment at scale.</span></span> <span data-ttu-id="96a62-1007">Nya cmdlet:ar är:</span><span class="sxs-lookup"><span data-stu-id="96a62-1007">New cmdlets are:</span></span>
    - <span data-ttu-id="96a62-1008">”Add-AzIotHubDeployment”</span><span class="sxs-lookup"><span data-stu-id="96a62-1008">'Add-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="96a62-1009">”Get-AzIotHubDeployment”</span><span class="sxs-lookup"><span data-stu-id="96a62-1009">'Get-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="96a62-1010">”Remove-AzIotHubDeployment”</span><span class="sxs-lookup"><span data-stu-id="96a62-1010">'Remove-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="96a62-1011">”Set-AzIotHubDeployment”</span><span class="sxs-lookup"><span data-stu-id="96a62-1011">'Set-AzIotHubDeployment'</span></span>
* <span data-ttu-id="96a62-1012">En cmdlet har lagts till för att anropa en måttfråga om IoT Edge-distribution.</span><span class="sxs-lookup"><span data-stu-id="96a62-1012">Added cmdlet to invoke an IoT Edge deployment metrics query.</span></span>
* <span data-ttu-id="96a62-1013">En cmdlet har lagts till för att tillämpa konfigurationsinnehåll på den angivna gränsenheten.</span><span class="sxs-lookup"><span data-stu-id="96a62-1013">Added cmdlet to apply the configuration content to the specified edge device.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="96a62-1014">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="96a62-1014">Az.KeyVault</span></span>
* <span data-ttu-id="96a62-1015">Två alias har tagits bort: ”New-AzKeyVaultCertificateAdministratorDetails” och ”New-AzKeyVaultCertificateOrganizationDetails”</span><span class="sxs-lookup"><span data-stu-id="96a62-1015">Removed two aliases: 'New-AzKeyVaultCertificateAdministratorDetails' and 'New-AzKeyVaultCertificateOrganizationDetails'</span></span>
* <span data-ttu-id="96a62-1016">Nu är mjuk borttagning aktiverat som standard när ett nyckelvalv skapas</span><span class="sxs-lookup"><span data-stu-id="96a62-1016">Enabled soft delete by default when creating a key vault</span></span>
* <span data-ttu-id="96a62-1017">Nätverksregler kan ställas in för att styra åtkomsten från särskilda nätverksplatser när du skapar ett nyckelvalv</span><span class="sxs-lookup"><span data-stu-id="96a62-1017">Network rules can be set to govern the accessibility from specific network locations when creating a key vault</span></span>
* <span data-ttu-id="96a62-1018">Stöd för BYOK (Bring Your Own Key) har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-1018">Added support to bring your own key (BYOK)</span></span>
    - <span data-ttu-id="96a62-1019">”Add-AzKeyVaultKey” stöder generering av en KeyExchange-nyckel</span><span class="sxs-lookup"><span data-stu-id="96a62-1019">'Add-AzKeyVaultKey' supports generating a key exchange key</span></span>
    - <span data-ttu-id="96a62-1020">”Get-AzKeyVaultKey” stöder nedladdning av en offentlig nyckel i PEM-format</span><span class="sxs-lookup"><span data-stu-id="96a62-1020">'Get-AzKeyVaultKey' supports downloading a public key in PEM format</span></span>
* <span data-ttu-id="96a62-1021">”KeyOps”-delen av hjälpdokumentet för ”Add-AzKeyVaultKey” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="96a62-1021">Updated the 'KeyOps' part of the help document of 'Add-AzKeyVaultKey'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="96a62-1022">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="96a62-1022">Az.Monitor</span></span>
* <span data-ttu-id="96a62-1023">Bugg för ”Set-AzDiagnosticSettings” har åtgärdats; kvarhållningsprincipen tillämpas inte på alla kategorier [#11589]</span><span class="sxs-lookup"><span data-stu-id="96a62-1023">Fixed bug for 'Set-AzDiagnosticSettings', retention policy won't apply to all categories [#11589]</span></span>
* <span data-ttu-id="96a62-1024">Stöd för WebTest-tillgänglighetskriterier för måttavisering V2</span><span class="sxs-lookup"><span data-stu-id="96a62-1024">Supported WebTest availability criteria for metric alert V2</span></span>
    - <span data-ttu-id="96a62-1025">”New-AzMetricAlertRuleV2Criteria”: ett alternativ för att skapa tillgänglighetskriterier för webbtest har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-1025">'New-AzMetricAlertRuleV2Criteria': an option to create webtest availability criteria was added</span></span>
    - <span data-ttu-id="96a62-1026">”Add-AzMetricAlertRuleV2”: stöd för de nya tillgänglighetskriterierna för webbtest</span><span class="sxs-lookup"><span data-stu-id="96a62-1026">'Add-AzMetricAlertRuleV2': supports the new webtest availability criteria</span></span>
* <span data-ttu-id="96a62-1027">Redundant definition har tagits bort för RetentionPolicy i PSLogProfile [#7608]</span><span class="sxs-lookup"><span data-stu-id="96a62-1027">Removed redundant definition for RetentionPolicy in PSLogProfile [#7608]</span></span>
* <span data-ttu-id="96a62-1028">Redundanta egenskaper som definierats i PSEventData har tagits bort [#11353]</span><span class="sxs-lookup"><span data-stu-id="96a62-1028">Removed redundant properties difined in PSEventData [#11353]</span></span>
* <span data-ttu-id="96a62-1029">”Get-AzLog” har bytt namn till ”Get-AzActivityLog”</span><span class="sxs-lookup"><span data-stu-id="96a62-1029">Renamed 'Get-AzLog' to 'Get-AzActivityLog'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="96a62-1030">Az.Network</span><span class="sxs-lookup"><span data-stu-id="96a62-1030">Az.Network</span></span>
* <span data-ttu-id="96a62-1031">Attribut för icke-bakåtkompatibel ändring har lagts till för att meddela att standardbeteendet för zoner kommer att ändras</span><span class="sxs-lookup"><span data-stu-id="96a62-1031">Added breaking change attribute to notify that Zone default behaviour will be changed</span></span>
    - <span data-ttu-id="96a62-1032">”New-AzPublicIpAddress”</span><span class="sxs-lookup"><span data-stu-id="96a62-1032">'New-AzPublicIpAddress'</span></span>
    - <span data-ttu-id="96a62-1033">”New-AzPublicIpPrefix”</span><span class="sxs-lookup"><span data-stu-id="96a62-1033">'New-AzPublicIpPrefix'</span></span>
    - <span data-ttu-id="96a62-1034">”New-AzLoadBalancerFrontendIpConfig”</span><span class="sxs-lookup"><span data-stu-id="96a62-1034">'New-AzLoadBalancerFrontendIpConfig'</span></span>
* <span data-ttu-id="96a62-1035">Stöd har lagts till för en ny resurs på den översta nivån, SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="96a62-1035">Added support for a new top level resource SecurityPartnerProvider</span></span>
    - <span data-ttu-id="96a62-1036">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="96a62-1036">New cmdlets added:</span></span>
        - <span data-ttu-id="96a62-1037">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="96a62-1037">New-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="96a62-1038">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="96a62-1038">Remove-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="96a62-1039">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="96a62-1039">Get-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="96a62-1040">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="96a62-1040">Set-AzSecurityPartnerProvider</span></span>
* <span data-ttu-id="96a62-1041">”RequiredZoneNames” har lagts till för ”PSPrivateLinkResource” och ”GroupId” för ”PSPrivateEndpointConnection”</span><span class="sxs-lookup"><span data-stu-id="96a62-1041">Added 'RequiredZoneNames' on 'PSPrivateLinkResource' and 'GroupId' on 'PSPrivateEndpointConnection'</span></span>
* <span data-ttu-id="96a62-1042">Fel parametertyp för SuccessThresholdRoundTripTimeMs-parametern för New-AzNetworkWatcherConnectionMonitorTestConfigurationObject har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="96a62-1042">Fixed incorrect type of SuccessThresholdRoundTripTimeMs parameter for New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>
* <span data-ttu-id="96a62-1043">VirtualWan-cmdletar har uppdaterats för att ange AllowVnetToVnetTraffic-argumentets standardvärde till True.</span><span class="sxs-lookup"><span data-stu-id="96a62-1043">Updated VirtualWan cmdlets to set default value of AllowVnetToVnetTraffic argument to True.</span></span>
    - <span data-ttu-id="96a62-1044">”New-AzVirtualWan”</span><span class="sxs-lookup"><span data-stu-id="96a62-1044">'New-AzVirtualWan'</span></span>
    - <span data-ttu-id="96a62-1045">”Update-AzVirtualWan”</span><span class="sxs-lookup"><span data-stu-id="96a62-1045">'Update-AzVirtualWan'</span></span>
* <span data-ttu-id="96a62-1046">Nya cmdletar har lagts till för att stödja DNS-zongrupp för privat slutpunkt</span><span class="sxs-lookup"><span data-stu-id="96a62-1046">Added new cmdlets to support DNS zone group for private endpoint</span></span>
    - <span data-ttu-id="96a62-1047">”New-AzPrivateDnsZoneConfig”</span><span class="sxs-lookup"><span data-stu-id="96a62-1047">'New-AzPrivateDnsZoneConfig'</span></span>
    - <span data-ttu-id="96a62-1048">”Get-AzPrivateDnsZoneGroup”</span><span class="sxs-lookup"><span data-stu-id="96a62-1048">'Get-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="96a62-1049">”New-AzPrivateDnsZoneGroup”</span><span class="sxs-lookup"><span data-stu-id="96a62-1049">'New-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="96a62-1050">”Set-AzPrivateDnsZoneGroup”</span><span class="sxs-lookup"><span data-stu-id="96a62-1050">'Set-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="96a62-1051">”Remove-AzPrivateDnsZoneGroup”</span><span class="sxs-lookup"><span data-stu-id="96a62-1051">'Remove-AzPrivateDnsZoneGroup'</span></span>
* <span data-ttu-id="96a62-1052">Parametrarna ”DNSEnableProxy”, ”DNSRequireProxyForNetworkRules” och ”DNSServers” har lagts till för ”AzureFirewall”</span><span class="sxs-lookup"><span data-stu-id="96a62-1052">Added 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' and 'DNSServers' parameters to 'AzureFirewall'</span></span>
* <span data-ttu-id="96a62-1053">Parametrarna ”EnableDnsProxy”, ”DnsProxyNotRequiredForNetworkRule” och ”DnsServer” har lagts till för ”AzureFirewall”</span><span class="sxs-lookup"><span data-stu-id="96a62-1053">Added 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' and 'DnsServer' parameters to 'AzureFirewall'</span></span>
    - <span data-ttu-id="96a62-1054">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="96a62-1054">Updated cmdlet:</span></span>
        - <span data-ttu-id="96a62-1055">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="96a62-1055">New-AzFirewall</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="96a62-1056">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="96a62-1056">Az.OperationalInsights</span></span>
* <span data-ttu-id="96a62-1057">Äldre kod har uppdaterats för att tillämpa ny genererad SDK</span><span class="sxs-lookup"><span data-stu-id="96a62-1057">Updated legacy code to apply new generated SDK</span></span>
* <span data-ttu-id="96a62-1058">Cmdletar har tagits bort på grund av föråldrade API:er</span><span class="sxs-lookup"><span data-stu-id="96a62-1058">Deleted cmdlets due to deprecated APIs</span></span>
    - <span data-ttu-id="96a62-1059">”Get-AzOperationalInsightsSavedSearchResult” (alias ”Get-AzOperationalInsightsSavedSearchResults”)</span><span class="sxs-lookup"><span data-stu-id="96a62-1059">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span></span>
    - <span data-ttu-id="96a62-1060">”Get-AzOperationalInsightsSearchResult” (alias ”Get-AzOperationalInsightsSearchResults”)</span><span class="sxs-lookup"><span data-stu-id="96a62-1060">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span></span>
    - <span data-ttu-id="96a62-1061">”Get-AzOperationalInsightsLinkTarget” (alias ”Get-AzOperationalInsightsLinkTargets”)</span><span class="sxs-lookup"><span data-stu-id="96a62-1061">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span></span>
* <span data-ttu-id="96a62-1062">Parametrar har lagts till för ”Set-AzOperationalInsightsWorkspace” och ”New-AzOperationalInsightsWorkspace”</span><span class="sxs-lookup"><span data-stu-id="96a62-1062">Added parameters for 'Set-AzOperationalInsightsWorkspace' and 'New-AzOperationalInsightsWorkspace'</span></span>
* <span data-ttu-id="96a62-1063">Cmdletar har skapats för länkat lagringskonto</span><span class="sxs-lookup"><span data-stu-id="96a62-1063">Created cmdlets for Linked Stoarge Account</span></span>
* <span data-ttu-id="96a62-1064">Cmdletar har skapats för kluster och länkad tjänst</span><span class="sxs-lookup"><span data-stu-id="96a62-1064">Created cmdlets for Clusters and Linked Service</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="96a62-1065">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="96a62-1065">Az.RecoveryServices</span></span>
* <span data-ttu-id="96a62-1066">Azure Site Recovery: Stöd har lagts till för att skydda VM-närhetsplaceringsgrupper för Azure till Azure-provider.</span><span class="sxs-lookup"><span data-stu-id="96a62-1066">Azure Site Recovery added support for protecting proximity placement group virtual machines for Azure to Azure provider.</span></span>
* <span data-ttu-id="96a62-1067">Azure Site Recovery: Stöd har lagts till för replikering mellan zoner.</span><span class="sxs-lookup"><span data-stu-id="96a62-1067">Azure Site Recovery added support for zone to zone replication.</span></span>
* <span data-ttu-id="96a62-1068">Azure Backup: Stöd har lagts till för långsiktig kvarhållning för Azure FileShare-återställningspunkter.</span><span class="sxs-lookup"><span data-stu-id="96a62-1068">Azure Backup Added Long term retention support for Azure FileShare Recovery Points.</span></span>
* <span data-ttu-id="96a62-1069">Azure Backup: Egenskaper för diskexkludering har lagts till för cmdlet-utdata från ”Get-AzRecoveryServicesBackupItem”.</span><span class="sxs-lookup"><span data-stu-id="96a62-1069">Azure Backup Added disk exclusion properties to 'Get-AzRecoveryServicesBackupItem' cmdlet output.</span></span>
* <span data-ttu-id="96a62-1070">En privat slutpunkt har lagts till för filen med valvets autentiseringsuppgifter för Site Recovery-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="96a62-1070">Added private endpoint for Vault credential file for site recovery service.</span></span>

#### <a name="azresources"></a><span data-ttu-id="96a62-1071">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="96a62-1071">Az.Resources</span></span>
* <span data-ttu-id="96a62-1072">En varning har lagts till om visningsfördröjning när en ny rolldefinition skapas</span><span class="sxs-lookup"><span data-stu-id="96a62-1072">Added message warning about view delay when creating a new Role Definition</span></span>
* <span data-ttu-id="96a62-1073">Princip-cmdletar har ändrats för utmatning av starkt typifierade objekt</span><span class="sxs-lookup"><span data-stu-id="96a62-1073">Changed policy cmdlets to output strongly-typed objects</span></span>
* <span data-ttu-id="96a62-1074">Parametern ”-TenantLevel” har tagits bort för användning med ”Get-AzResourceLock” [#11335]</span><span class="sxs-lookup"><span data-stu-id="96a62-1074">Removed '-TenantLevel' parameter used for on the 'Get-AzResourceLock' cmdlet [#11335]</span></span>
* <span data-ttu-id="96a62-1075">”Remove-AzResourceGroup -Id ResourceId” har åtgärdats [#9882]</span><span class="sxs-lookup"><span data-stu-id="96a62-1075">Fixed 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span></span>
* <span data-ttu-id="96a62-1076">En ny cmdlet har lagts till för att hämta What-If-resultat för ARM-mallar i omfånget för resursgrupper: ”Get-AzDeploymentResourceGroupWhatIfResult”</span><span class="sxs-lookup"><span data-stu-id="96a62-1076">Added new cmdlet for getting ARM template What-If results at resource group scope: 'Get-AzDeploymentResourceGroupWhatIfResult'</span></span>
* <span data-ttu-id="96a62-1077">En ny cmdlet har lagts till för att hämta What-If-resultat för ARM-mallar i prenumerationsomfånget: ”Get-AzDeploymentWhatIfResult”</span><span class="sxs-lookup"><span data-stu-id="96a62-1077">Added new cmdlet for getting ARM template What-If results at subscription scope: 'Get-AzDeploymentWhatIfResult'</span></span>
   - <span data-ttu-id="96a62-1078">Alias: ”Get-AzSubscriptionDeploymentWhatIf”</span><span class="sxs-lookup"><span data-stu-id="96a62-1078">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span></span>
* <span data-ttu-id="96a62-1079">Parametrarna ”-WhatIf” och ”-Confirm” har åsidosatts för ”New-AzDeployment” och ”New-AzResourceGroupDeployment” för att använda What-If-resultat för ARM-mallar</span><span class="sxs-lookup"><span data-stu-id="96a62-1079">Overrode '-WhatIf' and '-Confirm' parameters for 'New-AzDeployment' and 'New-AzResourceGroupDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="96a62-1080">Ett utfasningsmeddelande har lagts till för parametern ”ApiVersion” i distributions-cmdletar</span><span class="sxs-lookup"><span data-stu-id="96a62-1080">Added deprecation message for 'ApiVersion' parameter in deployment cmdlets</span></span>
* <span data-ttu-id="96a62-1081">En funktion har lagts till för att visa förbättrade felmeddelanden för distributionsfel</span><span class="sxs-lookup"><span data-stu-id="96a62-1081">Added capability to show improved error messages for deployment failures</span></span>
* <span data-ttu-id="96a62-1082">CorrelationId-loggning har lagts till för distributionsfel</span><span class="sxs-lookup"><span data-stu-id="96a62-1082">Added correlationId logging for deployment failures</span></span>
* <span data-ttu-id="96a62-1083">Egenskapen ”error” har lagts till i utdata från distributionsskript</span><span class="sxs-lookup"><span data-stu-id="96a62-1083">Added 'error' property to the deployment script output</span></span>
* <span data-ttu-id="96a62-1084">Nuget Microsoft.Azure.Management.ResourceManager har uppdaterats till ”3.7.1-preview”</span><span class="sxs-lookup"><span data-stu-id="96a62-1084">Updated nuget Microsoft.Azure.Management.ResourceManager to '3.7.1-preview'</span></span>
* <span data-ttu-id="96a62-1085">Specifika testfall har tagits bort då egenskapen Error i DeploymentValidateResult har ändrats till lässkyddad från nuget 3.7.1-preview</span><span class="sxs-lookup"><span data-stu-id="96a62-1085">Removed specific test cases as Error property in DeploymentValidateResult has changed to readonly from nuget 3.7.1-preview</span></span>
* <span data-ttu-id="96a62-1086">GenericResourceExpanded har flyttats från SDK ResourceManager 3.7.1-preview</span><span class="sxs-lookup"><span data-stu-id="96a62-1086">Brought GenericResourceExpanded from SDK ResourceManager 3.7.1-preview</span></span>
* <span data-ttu-id="96a62-1087">Stöd för taggar har lagts till för alla Get-cmdletar för distribution, samt</span><span class="sxs-lookup"><span data-stu-id="96a62-1087">Added tag support for all Get cmdlets for deployment, as well as</span></span>
    - <span data-ttu-id="96a62-1088">”New-AzDeployment”</span><span class="sxs-lookup"><span data-stu-id="96a62-1088">'New-AzDeployment'</span></span>
    - <span data-ttu-id="96a62-1089">”New-AzManagementGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="96a62-1089">'New-AzManagementGroupDeployment'</span></span>
    - <span data-ttu-id="96a62-1090">”New-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="96a62-1090">'New-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="96a62-1091">”New-AzTenantDeployment”</span><span class="sxs-lookup"><span data-stu-id="96a62-1091">'New-AzTenantDeployment'</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="96a62-1092">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="96a62-1092">Az.ServiceFabric</span></span>
* <span data-ttu-id="96a62-1093">En bugg har åtgärdats som gjorde att --SecretIdentifier fick fel tumavtryck för certifikat när ett certifikat lades till</span><span class="sxs-lookup"><span data-stu-id="96a62-1093">Fixed bug in add certificate using --SecretIdentifier that was getting the wrong certificate thumbprint</span></span>

#### <a name="azsql"></a><span data-ttu-id="96a62-1094">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="96a62-1094">Az.Sql</span></span>
* <span data-ttu-id="96a62-1095">Förbättrade prestanda för:</span><span class="sxs-lookup"><span data-stu-id="96a62-1095">Enhance performance of:</span></span>
    - <span data-ttu-id="96a62-1096">”Set-AzSqlDatabaseSensitivityClassification”</span><span class="sxs-lookup"><span data-stu-id="96a62-1096">'Set-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="96a62-1097">”Set-AzSqlInstanceDatabaseSensitivityClassification”</span><span class="sxs-lookup"><span data-stu-id="96a62-1097">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="96a62-1098">”Remove-AzSqlDatabaseSensitivityClassification”</span><span class="sxs-lookup"><span data-stu-id="96a62-1098">'Remove-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="96a62-1099">”Remove-AzSqlInstanceDatabaseSensitivityClassification”</span><span class="sxs-lookup"><span data-stu-id="96a62-1099">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="96a62-1100">”Enable-AzSqlDatabaseSensitivityRecommendation”</span><span class="sxs-lookup"><span data-stu-id="96a62-1100">'Enable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="96a62-1101">”Enable-AzSqlInstanceDatabaseSensitivityRecommendation”</span><span class="sxs-lookup"><span data-stu-id="96a62-1101">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="96a62-1102">”Disable-AzSqlDatabaseSensitivityRecommendation”</span><span class="sxs-lookup"><span data-stu-id="96a62-1102">'Disable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="96a62-1103">”Disable-AzSqlInstanceDatabaseSensitivityRecommendation”</span><span class="sxs-lookup"><span data-stu-id="96a62-1103">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
* <span data-ttu-id="96a62-1104">Validering på klientsidan har tagits bort för parametern ”RetentionDays” från cmdleten ”Set-AzSqlDatabaseBackupShortTermRetentionPolicy”</span><span class="sxs-lookup"><span data-stu-id="96a62-1104">Removed client-side validation of 'RetentionDays' parameter from cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span>
* <span data-ttu-id="96a62-1105">Granskning av ett lagringskonto i Vnet; en bugg har åtgärdats som orsakade fel när en Storage Blob Data-deltagarroll skapades.</span><span class="sxs-lookup"><span data-stu-id="96a62-1105">Auditing to a storage account in Vnet, fixing a bug when creating a Storage Blob Data Contributor role.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="96a62-1106">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="96a62-1106">Az.Storage</span></span>
* <span data-ttu-id="96a62-1107">”-AsJob” har lagts till för att hämta/lista konto med cmdleten ”Get-AzStorageAccount”</span><span class="sxs-lookup"><span data-stu-id="96a62-1107">Added '-AsJob' to get/list account cmdlet 'Get-AzStorageAccount'</span></span>
* <span data-ttu-id="96a62-1108">Gör KeyVersion valfri när lagringskontot uppdateras med KeyvaultEncryption, för att ge stöd för automatisk nyckelrotation</span><span class="sxs-lookup"><span data-stu-id="96a62-1108">Make KeyVersion to optional when update Storage account with KeyvaultEncryption, to support key auto-rotation</span></span>
    - <span data-ttu-id="96a62-1109">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="96a62-1109">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="96a62-1110">Problemet med borttagning av Azure-filkatalog i pipeline har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="96a62-1110">Fixed remove Azure File Directory fail with pipeline</span></span>
    - <span data-ttu-id="96a62-1111">”Remove-AzStorageDirectory”</span><span class="sxs-lookup"><span data-stu-id="96a62-1111">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="96a62-1112">Åtgärdat [#9880]: Definitionen av DefaultAction-värdet för NetWorkRule har ändrats för konsekvens med Swagger.</span><span class="sxs-lookup"><span data-stu-id="96a62-1112">Fixed [#9880]: Change NetWorkRule DefaultAction value defination to align with swagger.</span></span>
    - <span data-ttu-id="96a62-1113">”Update-AzStorageAccountNetworkRuleSet”</span><span class="sxs-lookup"><span data-stu-id="96a62-1113">'Update-AzStorageAccountNetworkRuleSet'</span></span>
    - <span data-ttu-id="96a62-1114">”Get-AzStorageAccountNetworkRuleSet”</span><span class="sxs-lookup"><span data-stu-id="96a62-1114">'Get-AzStorageAccountNetworkRuleSet'</span></span>
* <span data-ttu-id="96a62-1115">Åtgärdat [#11624]: Hoppa över dubblettregler när NetworkRules läggs till, för att undvika serverfel</span><span class="sxs-lookup"><span data-stu-id="96a62-1115">Fixed [#11624]: Skip duplicated rules when add NetworkRules, to avoid server failure</span></span>
    - <span data-ttu-id="96a62-1116">”Add-AzStorageAccountNetworkRule”</span><span class="sxs-lookup"><span data-stu-id="96a62-1116">'Add-AzStorageAccountNetworkRule'</span></span>
* <span data-ttu-id="96a62-1117">Microsoft.Azure.Cosmos.Table SDK har uppgraderats till 1.0.7</span><span class="sxs-lookup"><span data-stu-id="96a62-1117">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.7</span></span>
* <span data-ttu-id="96a62-1118">Ett varningsmeddelande har lagts till för att påminna användaren om att lista igen med ContinuationToken när endast delobjekt returneras i listan med DataLake Gen2-objekt,</span><span class="sxs-lookup"><span data-stu-id="96a62-1118">Added a warning message to remind user to list again with ContinuationToken when only part items are returned in list DataLake Gen2 Items,</span></span>
    - <span data-ttu-id="96a62-1119">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="96a62-1119">'Get-AzDataLakeGen2ChildItem'</span></span>
* <span data-ttu-id="96a62-1120">Stöd för att skapa eller uppdatera lagringskonto med Azure Files Active Directory Domain Service-autentisering</span><span class="sxs-lookup"><span data-stu-id="96a62-1120">Supported to create or update Storage account with Azure Files Active Directory Domain Service Authentication</span></span>
    -  <span data-ttu-id="96a62-1121">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="96a62-1121">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="96a62-1122">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="96a62-1122">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="96a62-1123">Stöd för nya eller listade Kerberos-nycklar för lagringskontot</span><span class="sxs-lookup"><span data-stu-id="96a62-1123">Supported to new or list Kerberos keys of Storage account</span></span>
    -  <span data-ttu-id="96a62-1124">”New-AzStorageAccountKey”</span><span class="sxs-lookup"><span data-stu-id="96a62-1124">'New-AzStorageAccountKey'</span></span>
    -  <span data-ttu-id="96a62-1125">”Get-AzStorageAccountKey”</span><span class="sxs-lookup"><span data-stu-id="96a62-1125">'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="96a62-1126">Stöd för redundans med lagringskonto</span><span class="sxs-lookup"><span data-stu-id="96a62-1126">Supported failover Storage account</span></span>
    - <span data-ttu-id="96a62-1127">”Invoke-AzStorageAccountFailover”</span><span class="sxs-lookup"><span data-stu-id="96a62-1127">'Invoke-AzStorageAccountFailover'</span></span>
* <span data-ttu-id="96a62-1128">Hjälpen för ”Get-AzStorageBlobCopyState” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="96a62-1128">Updated help of 'Get-AzStorageBlobCopyState'</span></span>
* <span data-ttu-id="96a62-1129">Hjälpen för ”Get-AzStorageFileCopyState” och ”Start-AzStorageBlobCopy” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="96a62-1129">Updated help of 'Get-AzStorageFileCopyState' and 'Start-AzStorageBlobCopy'</span></span>
* <span data-ttu-id="96a62-1130">Lagringsklientbibliotek v12 har integrerats med Queue- och File-cmdletar</span><span class="sxs-lookup"><span data-stu-id="96a62-1130">Integrated Storage client library v12 to Queue and File cmdlets</span></span>
* <span data-ttu-id="96a62-1131">Utdatatypen har ändrats från CloudFile till AzureStorageFile; ursprungliga utdata blir en underordnad egenskap i den nya utmatningen</span><span class="sxs-lookup"><span data-stu-id="96a62-1131">Changed output type from CloudFile to AzureStorageFile, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="96a62-1132">”Get-AzStorageFile”</span><span class="sxs-lookup"><span data-stu-id="96a62-1132">'Get-AzStorageFile'</span></span>
    - <span data-ttu-id="96a62-1133">”Remove-AzStorageFile”</span><span class="sxs-lookup"><span data-stu-id="96a62-1133">'Remove-AzStorageFile'</span></span>
    - <span data-ttu-id="96a62-1134">”Get-AzStorageFileContent”</span><span class="sxs-lookup"><span data-stu-id="96a62-1134">'Get-AzStorageFileContent'</span></span>
    - <span data-ttu-id="96a62-1135">”Set-AzStorageFileContent”</span><span class="sxs-lookup"><span data-stu-id="96a62-1135">'Set-AzStorageFileContent'</span></span>
    - <span data-ttu-id="96a62-1136">”Start-AzStorageFileCopy”</span><span class="sxs-lookup"><span data-stu-id="96a62-1136">'Start-AzStorageFileCopy'</span></span>
* <span data-ttu-id="96a62-1137">Utdatatypen har ändrats från CloudFileDirectory till AzureStorageFileDirectory; ursprungliga utdata blir en underordnad egenskap i den nya utmatningen</span><span class="sxs-lookup"><span data-stu-id="96a62-1137">Changed output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="96a62-1138">”New-AzStorageDirectory”</span><span class="sxs-lookup"><span data-stu-id="96a62-1138">'New-AzStorageDirectory'</span></span>
    - <span data-ttu-id="96a62-1139">”Remove-AzStorageDirectory”</span><span class="sxs-lookup"><span data-stu-id="96a62-1139">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="96a62-1140">Utdatatypen har ändrats från CloudFileShare till AzureStorageFileShare; ursprungliga utdata blir en underordnad egenskap i den nya utmatningen</span><span class="sxs-lookup"><span data-stu-id="96a62-1140">Changed output type from CloudFileShare to AzureStorageFileShare, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="96a62-1141">”Get-AzStorageShare”</span><span class="sxs-lookup"><span data-stu-id="96a62-1141">'Get-AzStorageShare'</span></span>
    - <span data-ttu-id="96a62-1142">”New-AzStorageShare”</span><span class="sxs-lookup"><span data-stu-id="96a62-1142">'New-AzStorageShare'</span></span>
    - <span data-ttu-id="96a62-1143">”Remove-AzStorageShare”</span><span class="sxs-lookup"><span data-stu-id="96a62-1143">'Remove-AzStorageShare'</span></span>
* <span data-ttu-id="96a62-1144">Utdatatypen har ändrats från FileShareProperties till AzureStorageFileShare; ursprungliga utdata blir en underordnad egenskap i den nya utmatningen</span><span class="sxs-lookup"><span data-stu-id="96a62-1144">Changed output type from FileShareProperties to AzureStorageFileShare, the original output will become a sub child property of the new output</span></span>
    - <span data-ttu-id="96a62-1145">”Set-AzStorageShareQuota”</span><span class="sxs-lookup"><span data-stu-id="96a62-1145">'Set-AzStorageShareQuota'</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="96a62-1146">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="96a62-1146">Az.TrafficManager</span></span>
* <span data-ttu-id="96a62-1147">Felaktigt profilnamn har åtgärdats i utförliga utdata för ”DisableAzureTrafficManagerEndpoint”</span><span class="sxs-lookup"><span data-stu-id="96a62-1147">Fixed incorrect profile name in 'DisableAzureTrafficManagerEndpoint' verbose output</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="96a62-1148">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="96a62-1148">Az.Websites</span></span>
* <span data-ttu-id="96a62-1149">Stavfel har åtgärdats i hjälpen för ”Update-AzWebAppAccessRestrictionConfig”.</span><span class="sxs-lookup"><span data-stu-id="96a62-1149">Fixed typo on help of 'Update-AzWebAppAccessRestrictionConfig'.</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="96a62-1150">3.8.0 – April 2020</span><span class="sxs-lookup"><span data-stu-id="96a62-1150">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="96a62-1151">Höjdpunkter sedan den senaste uppdateringen</span><span class="sxs-lookup"><span data-stu-id="96a62-1151">Highlights since the last release</span></span>
* <span data-ttu-id="96a62-1152">PowerShell-versioner som Az.Storage stöder: Windows PowerShell 5.1, PowerShell Core 6.2.4+ och PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="96a62-1152">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="96a62-1153">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="96a62-1153">Az.Accounts</span></span>
* <span data-ttu-id="96a62-1154">Uppdaterade URL:en för Azure PowerShell-enkäten i ”Resolve-AzError” [#11507]</span><span class="sxs-lookup"><span data-stu-id="96a62-1154">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="96a62-1155">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="96a62-1155">Az.ApiManagement</span></span>
* <span data-ttu-id="96a62-1156">Lade till meddelande om icke-bakåtkompatibel ändring vid ändring i utdata för Azure File-cmdletar i en framtida version</span><span class="sxs-lookup"><span data-stu-id="96a62-1156">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="96a62-1157">"Set-AzApiManagementGroup" Uppdaterad dokumentation för att ange GroupId-parametern</span><span class="sxs-lookup"><span data-stu-id="96a62-1157">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="96a62-1158">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="96a62-1158">Az.Cdn</span></span>
* <span data-ttu-id="96a62-1159">Fast ChinaCDN-relaterad prissättning för SKU-visning</span><span class="sxs-lookup"><span data-stu-id="96a62-1159">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="96a62-1160">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="96a62-1160">Az.CognitiveServices</span></span>
* <span data-ttu-id="96a62-1161">Identitet som stöds, kryptering, UserOwnedStorage</span><span class="sxs-lookup"><span data-stu-id="96a62-1161">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="96a62-1162">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="96a62-1162">Az.Compute</span></span>
* <span data-ttu-id="96a62-1163">Cmdleten ”Set-AzVmssOrchestrationServiceState” har lagts till.</span><span class="sxs-lookup"><span data-stu-id="96a62-1163">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="96a62-1164">”Get-AzVmss” med -InstanceView visar OrchestrationService-tillstånd.</span><span class="sxs-lookup"><span data-stu-id="96a62-1164">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="96a62-1165">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="96a62-1165">Az.IotHub</span></span>
* <span data-ttu-id="96a62-1166">Hantera den dubbla konfigurationen för IoT-enheter, nya cmdletar är:</span><span class="sxs-lookup"><span data-stu-id="96a62-1166">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="96a62-1167">'Get-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="96a62-1167">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="96a62-1168">'Update-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="96a62-1168">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="96a62-1169">En cmdlet har lagts till för att anropa direkt metod på en enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="96a62-1169">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="96a62-1170">Hantera dubbel konfiguration för IoT-enhetsmodul, nya cmdletar är:</span><span class="sxs-lookup"><span data-stu-id="96a62-1170">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="96a62-1171">'Get-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="96a62-1171">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="96a62-1172">'Update-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="96a62-1172">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="96a62-1173">Hantera IoT-automatisk konfiguration av enhetshantering i stor skala.</span><span class="sxs-lookup"><span data-stu-id="96a62-1173">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="96a62-1174">Nya cmdlet:ar är:</span><span class="sxs-lookup"><span data-stu-id="96a62-1174">New cmdlets are:</span></span>
    - <span data-ttu-id="96a62-1175">'Add-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="96a62-1175">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="96a62-1176">'Get-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="96a62-1176">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="96a62-1177">'Remove-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="96a62-1177">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="96a62-1178">'Set-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="96a62-1178">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="96a62-1179">En cmdlet har lagts till för att anropa en edge-modulmetod i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="96a62-1179">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="96a62-1180">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="96a62-1180">Az.KeyVault</span></span>
* <span data-ttu-id="96a62-1181">Har lagt till en ny cmdlet, "Update-AzKeyVault", som kan aktivera mjuk borttagning och rensning av skydd i ett valv</span><span class="sxs-lookup"><span data-stu-id="96a62-1181">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="96a62-1182">Har lagt till stöd i Microsoft.PowerShell.SecretManagement [#11178]</span><span class="sxs-lookup"><span data-stu-id="96a62-1182">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="96a62-1183">Åtgärdat fel i exemplen i 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span><span class="sxs-lookup"><span data-stu-id="96a62-1183">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="96a62-1184">Har lagt till stöd för privat slutpunkt</span><span class="sxs-lookup"><span data-stu-id="96a62-1184">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="96a62-1185">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="96a62-1185">Az.Maintenance</span></span>
* <span data-ttu-id="96a62-1186">Publicerar slutversion av underhålls-cmdletar för GA</span><span class="sxs-lookup"><span data-stu-id="96a62-1186">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="96a62-1187">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="96a62-1187">Az.Monitor</span></span>
* <span data-ttu-id="96a62-1188">Har lagt till cmdletar för privat länkomfång</span><span class="sxs-lookup"><span data-stu-id="96a62-1188">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="96a62-1189">'Get-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="96a62-1189">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="96a62-1190">'Remove-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="96a62-1190">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="96a62-1191">'New-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="96a62-1191">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="96a62-1192">'Update-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="96a62-1192">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="96a62-1193">'Get-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="96a62-1193">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="96a62-1194">'New-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="96a62-1194">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="96a62-1195">'Remove-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="96a62-1195">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="96a62-1196">Az.Network</span><span class="sxs-lookup"><span data-stu-id="96a62-1196">Az.Network</span></span>
* <span data-ttu-id="96a62-1197">Uppdaterade cmdletar för att aktivera anslutning på privat IP för Virtual Network Gateway.</span><span class="sxs-lookup"><span data-stu-id="96a62-1197">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="96a62-1198">'New-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="96a62-1198">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="96a62-1199">'Set-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="96a62-1199">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="96a62-1200">'New-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="96a62-1200">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="96a62-1201">'Set-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="96a62-1201">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="96a62-1202">Uppdaterade cmdletar för att aktivera FQDN-baserade LocalNetworkGateways och VpnSites</span><span class="sxs-lookup"><span data-stu-id="96a62-1202">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="96a62-1203">'New-AzLocalNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="96a62-1203">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="96a62-1204">'New-AzVpnSiteLink'</span><span class="sxs-lookup"><span data-stu-id="96a62-1204">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="96a62-1205">Stöd har lagts till för IPv6-adresstypen i ExpressRouteCircuitConnectionConfig (Global Reach)</span><span class="sxs-lookup"><span data-stu-id="96a62-1205">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="96a62-1206">Lade till 'Set-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="96a62-1206">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="96a62-1207">tillåter inställning av alla befintliga egenskaper inklusive IPv6CircuitConnectionProperties</span><span class="sxs-lookup"><span data-stu-id="96a62-1207">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="96a62-1208">Uppdaterade 'Add-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="96a62-1208">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="96a62-1209">Lade till en ytterligare valfri parameter, AddressPrefixType, för att specificera adresstypen för adressprefix</span><span class="sxs-lookup"><span data-stu-id="96a62-1209">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="96a62-1210">Uppdaterade cmdletar för att aktivera inställningen för DPD-timeout på Virtual Network Gateway-anslutningar.</span><span class="sxs-lookup"><span data-stu-id="96a62-1210">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="96a62-1211">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="96a62-1211">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="96a62-1212">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="96a62-1212">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="96a62-1213">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="96a62-1213">Az.PolicyInsights</span></span>
* <span data-ttu-id="96a62-1214">Cmdleten "Start-AzPolicyComplianceScan" har lagts till för att utlösa genomsökningar av principefterlevnad</span><span class="sxs-lookup"><span data-stu-id="96a62-1214">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="96a62-1215">Principdefinition, uppsättningsdefinition och tilldelningsversioner har lagts till i "Get-AzPolicyState"-utdata</span><span class="sxs-lookup"><span data-stu-id="96a62-1215">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="96a62-1216">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="96a62-1216">Az.ServiceFabric</span></span>
* <span data-ttu-id="96a62-1217">Förbättrad kodformatering och användbarhet för "New-AzServiceFabricCluster"-exempel</span><span class="sxs-lookup"><span data-stu-id="96a62-1217">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="96a62-1218">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="96a62-1218">Az.Sql</span></span>
* <span data-ttu-id="96a62-1219">Lade till cmdletarna "Get-AzSqlInstanceOperation" och "Stop-AzSqlInstanceOperation"</span><span class="sxs-lookup"><span data-stu-id="96a62-1219">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="96a62-1220">Stöd för granskning för ett lagringskonto i VNet.</span><span class="sxs-lookup"><span data-stu-id="96a62-1220">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="96a62-1221">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="96a62-1221">Az.Storage</span></span>
* <span data-ttu-id="96a62-1222">Lade till meddelande om icke-bakåtkompatibel ändring vid ändring i utdata för Azure File-cmdletar i en framtida version</span><span class="sxs-lookup"><span data-stu-id="96a62-1222">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="96a62-1223">Stöd för nya SkuName StandardGZRS, StandardRAGZRS när ett lagringskonto skapas/uppdateras</span><span class="sxs-lookup"><span data-stu-id="96a62-1223">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="96a62-1224">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="96a62-1224">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="96a62-1225">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="96a62-1225">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="96a62-1226">Stöd för DataLake Gen2</span><span class="sxs-lookup"><span data-stu-id="96a62-1226">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="96a62-1227">'New-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="96a62-1227">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="96a62-1228">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="96a62-1228">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="96a62-1229">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="96a62-1229">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="96a62-1230">'Move-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="96a62-1230">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="96a62-1231">'Set-AzDataLakeGen2ItemAclObject'</span><span class="sxs-lookup"><span data-stu-id="96a62-1231">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="96a62-1232">'Update-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="96a62-1232">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="96a62-1233">'Get-AzDataLakeGen2ItemContent'</span><span class="sxs-lookup"><span data-stu-id="96a62-1233">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="96a62-1234">'Remove-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="96a62-1234">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="96a62-1235">0.10.0-förhandsversion – April 2020</span><span class="sxs-lookup"><span data-stu-id="96a62-1235">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="96a62-1236">Allmänt</span><span class="sxs-lookup"><span data-stu-id="96a62-1236">General</span></span>
* <span data-ttu-id="96a62-1237">Az-moduler är nu tillgängliga i förhandsversion på Azure Stack Hub.</span><span class="sxs-lookup"><span data-stu-id="96a62-1237">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="96a62-1238">Därmed möjliggörs kompatibilitet för flera plattformar med Linux och macOs.</span><span class="sxs-lookup"><span data-stu-id="96a62-1238">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="96a62-1239">Azure Stack Hub stöder nu PowerShell Core med AZ-moduler. Mer information finns [här](https://aka.ms/az4AzureStack)</span><span class="sxs-lookup"><span data-stu-id="96a62-1239">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](https://aka.ms/az4AzureStack)</span></span>
* <span data-ttu-id="96a62-1240">Supportprofil för AZ-moduler 2019-03-01-hybrid:</span><span class="sxs-lookup"><span data-stu-id="96a62-1240">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="96a62-1241">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="96a62-1241">Az.Billing</span></span>
  - <span data-ttu-id="96a62-1242">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="96a62-1242">Az.Compute</span></span>
  - <span data-ttu-id="96a62-1243">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="96a62-1243">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="96a62-1244">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="96a62-1244">Az.EventHub</span></span>
  - <span data-ttu-id="96a62-1245">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="96a62-1245">Az.IotHub</span></span>
  - <span data-ttu-id="96a62-1246">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="96a62-1246">Az.KeyVault</span></span>
  - <span data-ttu-id="96a62-1247">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="96a62-1247">Az.Monitor</span></span>
  - <span data-ttu-id="96a62-1248">Az.Network</span><span class="sxs-lookup"><span data-stu-id="96a62-1248">Az.Network</span></span>
  - <span data-ttu-id="96a62-1249">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="96a62-1249">Az.Resources</span></span>
  - <span data-ttu-id="96a62-1250">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="96a62-1250">Az.Storage</span></span>
  - <span data-ttu-id="96a62-1251">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="96a62-1251">Az.Websites</span></span>
* <span data-ttu-id="96a62-1252">Tre nya PowerShell-moduler för AZ har introducerats som fungerar med Azure Stack Hub, och de är Az.Databox, Az.IotHub och Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="96a62-1252">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="96a62-1253">Kommandona är i princip oförändrade, med endast mindre ändringar som att AzureRM ändras till AZ</span><span class="sxs-lookup"><span data-stu-id="96a62-1253">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="96a62-1254">En uppdaterad länk till PowerShell-dokumentationen för Azure Stack Hub finns [här](https://aka.ms/InstallASHPowerShell)</span><span class="sxs-lookup"><span data-stu-id="96a62-1254">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](https://aka.ms/InstallASHPowerShell)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="96a62-1255">3.7.0 – mars 2020</span><span class="sxs-lookup"><span data-stu-id="96a62-1255">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="96a62-1256">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="96a62-1256">Az.Accounts</span></span>
* <span data-ttu-id="96a62-1257">Åtgärdade ”Get-AzTenant”/”Get-AzDefault”/”Set-AzDefault”-utlösning av NullReferenceException när du inte är inloggad [#10292]</span><span class="sxs-lookup"><span data-stu-id="96a62-1257">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="96a62-1258">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="96a62-1258">Az.Compute</span></span>
* <span data-ttu-id="96a62-1259">Följande parametrar har lagts till i cmdleten ”New-AzDiskConfig”:</span><span class="sxs-lookup"><span data-stu-id="96a62-1259">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="96a62-1260">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="96a62-1260">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="96a62-1261">Tillåten krypteringsegenskap till målparametern för cmdleten ”New-AzGalleryImageVersion”.</span><span class="sxs-lookup"><span data-stu-id="96a62-1261">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="96a62-1262">Åtgärdade tempDisk-problem för cmdletarna ”Set-AzVmss”-Reimage och ”Invoke-AzVMReimage”.</span><span class="sxs-lookup"><span data-stu-id="96a62-1262">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="96a62-1263">[#11354]</span><span class="sxs-lookup"><span data-stu-id="96a62-1263">[#11354]</span></span>
* <span data-ttu-id="96a62-1264">Stöd har lagts till i nedanstående cmdletar för nytt SAP-tillägg</span><span class="sxs-lookup"><span data-stu-id="96a62-1264">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="96a62-1265">”Set-AzVMAEMExtension”</span><span class="sxs-lookup"><span data-stu-id="96a62-1265">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="96a62-1266">”Get-AzVMAEMExtension”</span><span class="sxs-lookup"><span data-stu-id="96a62-1266">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="96a62-1267">”Remove-AzVMAEMExtension”</span><span class="sxs-lookup"><span data-stu-id="96a62-1267">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="96a62-1268">”Update-AzVMAEMExtension”</span><span class="sxs-lookup"><span data-stu-id="96a62-1268">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="96a62-1269">Åtgärdade fel i exempel på hjälpdokument</span><span class="sxs-lookup"><span data-stu-id="96a62-1269">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="96a62-1270">Visade det exakta strängvärdet för VM PowerState i tabellformat.</span><span class="sxs-lookup"><span data-stu-id="96a62-1270">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="96a62-1271">”New-AzVmssConfig”: den fasta serialiseringen av egenskapen AutomaticRepairs när SinglePlacementGroup är inaktiverad.</span><span class="sxs-lookup"><span data-stu-id="96a62-1271">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="96a62-1272">[#11257]</span><span class="sxs-lookup"><span data-stu-id="96a62-1272">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="96a62-1273">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="96a62-1273">Az.DataFactory</span></span>
* <span data-ttu-id="96a62-1274">ADF .Net SDK har uppdaterats till 4.8.0</span><span class="sxs-lookup"><span data-stu-id="96a62-1274">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="96a62-1275">Valfria parametrar har lagts till i kommandot ”Invoke-AzDataFactoryV2Pipeline” för att stödja omkörning</span><span class="sxs-lookup"><span data-stu-id="96a62-1275">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="96a62-1276">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="96a62-1276">Az.DataLakeStore</span></span>
* <span data-ttu-id="96a62-1277">Lade till beskrivning för icke-bakåtkompatibel ändring för ”Export-AzDataLakeStoreItem” och ”Import-AzDataLakeStoreItem”</span><span class="sxs-lookup"><span data-stu-id="96a62-1277">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="96a62-1278">Lade till alternativ för bytekodning för ”New-AzDataLakeStoreItem”, ”Add-AzDAtaLakeStoreItemContent” och ”Get-AzDAtaLakeStoreItemContent”</span><span class="sxs-lookup"><span data-stu-id="96a62-1278">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="96a62-1279">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="96a62-1279">Az.HDInsight</span></span>
* <span data-ttu-id="96a62-1280">Stöd för att ange en minimal TLS-version som stöds när klustret skapas.</span><span class="sxs-lookup"><span data-stu-id="96a62-1280">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="96a62-1281">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="96a62-1281">Az.IotHub</span></span>
* <span data-ttu-id="96a62-1282">Stöd har lagts till för att hantera distribuerade inställningar per enhet.</span><span class="sxs-lookup"><span data-stu-id="96a62-1282">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="96a62-1283">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="96a62-1283">New Cmdlets are:</span></span>
    - <span data-ttu-id="96a62-1284">”Get-AzIotHubDistributedTracing”</span><span class="sxs-lookup"><span data-stu-id="96a62-1284">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="96a62-1285">”Set-AzIotHubDistributedTracing”</span><span class="sxs-lookup"><span data-stu-id="96a62-1285">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="96a62-1286">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="96a62-1286">Az.KeyVault</span></span>
* <span data-ttu-id="96a62-1287">Ändrade attribut för icke-bakåtkompatibel ändring lades till för ”New-AzKeyVault”</span><span class="sxs-lookup"><span data-stu-id="96a62-1287">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="96a62-1288">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="96a62-1288">Az.Monitor</span></span>
* <span data-ttu-id="96a62-1289">Uppdaterad dokumentation för ”New-AzScheduledQueryRuleLogMetricTrigger”</span><span class="sxs-lookup"><span data-stu-id="96a62-1289">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="96a62-1290">Az.Network</span><span class="sxs-lookup"><span data-stu-id="96a62-1290">Az.Network</span></span>
* <span data-ttu-id="96a62-1291">Uppdaterade cmdletar för att tillåta VirtualHubVnetConnections mellan klienter</span><span class="sxs-lookup"><span data-stu-id="96a62-1291">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="96a62-1292">”New-AzVirtualHubVnetConnection”</span><span class="sxs-lookup"><span data-stu-id="96a62-1292">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="96a62-1293">”Update-AzVirtualHubVnetConnection”</span><span class="sxs-lookup"><span data-stu-id="96a62-1293">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="96a62-1294">”New-AzVirtualHub”</span><span class="sxs-lookup"><span data-stu-id="96a62-1294">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="96a62-1295">”Update-AzVirtualHub”</span><span class="sxs-lookup"><span data-stu-id="96a62-1295">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="96a62-1296">SQL Management SDK-beroende har tagits bort</span><span class="sxs-lookup"><span data-stu-id="96a62-1296">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="96a62-1297">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="96a62-1297">Az.PolicyInsights</span></span>
* <span data-ttu-id="96a62-1298">Förbättrade felmeddelanden</span><span class="sxs-lookup"><span data-stu-id="96a62-1298">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="96a62-1299">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="96a62-1299">Az.RecoveryServices</span></span>
* <span data-ttu-id="96a62-1300">Azure Site Recovery har lagt till stöd för återaktivering av skydd och uppdaterade VM-egenskaper för virtuella Azure-datorer med krypterad disk.</span><span class="sxs-lookup"><span data-stu-id="96a62-1300">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="96a62-1301">Lade till Azure Site Recovery VmwareToAzure-egenskaper för DR-övervakning</span><span class="sxs-lookup"><span data-stu-id="96a62-1301">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="96a62-1302">Azure Backup har lagt till stöd för att försöka uppdatera principuppdateringen för misslyckade objekt på nytt.</span><span class="sxs-lookup"><span data-stu-id="96a62-1302">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="96a62-1303">Azure Backup lagt till stöd för diskundantagsinställningar under säkerhetskopiering och återställning.</span><span class="sxs-lookup"><span data-stu-id="96a62-1303">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="96a62-1304">Azure Backup lagt till stöd för att återställa flera filer/mappar i AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="96a62-1304">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="96a62-1305">Azure Backup lade till support för användardefinierad Resourcegroup-support vid uppdatering av IaasVM-princip</span><span class="sxs-lookup"><span data-stu-id="96a62-1305">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="96a62-1306">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="96a62-1306">Az.Resources</span></span>
* <span data-ttu-id="96a62-1307">Åtgärdade ”Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType” så att den använder den faktisk apiVersion av resurser i stället för standard-apiVersion [#11267]</span><span class="sxs-lookup"><span data-stu-id="96a62-1307">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="96a62-1308">Lade till correlationId-loggning för felscenarier</span><span class="sxs-lookup"><span data-stu-id="96a62-1308">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="96a62-1309">Liten dokumentationsändring för ”Get-AzResourceLock”.</span><span class="sxs-lookup"><span data-stu-id="96a62-1309">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="96a62-1310">Lade till exempel.</span><span class="sxs-lookup"><span data-stu-id="96a62-1310">Added example.</span></span>
* <span data-ttu-id="96a62-1311">Undantaget enkelt citattecken i parametervärde för ”Get-AzADUser” [#11317]</span><span class="sxs-lookup"><span data-stu-id="96a62-1311">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="96a62-1312">Nya cmdletar har lagts till för distributionsskript (”Get-AzDeploymentScript”, ”Get-AzDeploymentScriptLog”, ”Save-AzDeploymentScriptLog”, ”Remove-AzDeploymentScript”)</span><span class="sxs-lookup"><span data-stu-id="96a62-1312">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="96a62-1313">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="96a62-1313">Az.Sql</span></span>
* <span data-ttu-id="96a62-1314">En läsbar sekundär parameter har lagts till i Invoke-AzSqlDatabaseFailover</span><span class="sxs-lookup"><span data-stu-id="96a62-1314">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="96a62-1315">Cmdleten Disable-AzSqlServerActiveDirectoryOnlyAuthentication har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-1315">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="96a62-1316">Den sparade känslighet rangordningen när kolumner klassificeras i databasen.</span><span class="sxs-lookup"><span data-stu-id="96a62-1316">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="96a62-1317">Az.Support</span><span class="sxs-lookup"><span data-stu-id="96a62-1317">Az.Support</span></span>
* <span data-ttu-id="96a62-1318">Allmän tillgänglighet för ”Az.Support”-modulen</span><span class="sxs-lookup"><span data-stu-id="96a62-1318">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="96a62-1319">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="96a62-1319">Az.Websites</span></span>
* <span data-ttu-id="96a62-1320">Stöd har lagts till för att arbeta med trafikdirigeringsregler för webbappar under nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="96a62-1320">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="96a62-1321">”Get-AzWebAppTrafficRouting”</span><span class="sxs-lookup"><span data-stu-id="96a62-1321">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="96a62-1322">”Update-AzWebAppTrafficRouting”</span><span class="sxs-lookup"><span data-stu-id="96a62-1322">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="96a62-1323">”Add-AzWebAppTrafficRouting”</span><span class="sxs-lookup"><span data-stu-id="96a62-1323">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="96a62-1324">”Remove-AzWebAppTrafficRouting”</span><span class="sxs-lookup"><span data-stu-id="96a62-1324">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="96a62-1325">3.6.1 – mars 2020</span><span class="sxs-lookup"><span data-stu-id="96a62-1325">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="96a62-1326">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="96a62-1326">Az.Accounts</span></span>
* <span data-ttu-id="96a62-1327">Öppna sidan med Azure PowerShell-enkäten i ”Send-Feedback” [#11020]</span><span class="sxs-lookup"><span data-stu-id="96a62-1327">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="96a62-1328">Visa URL:en för Azure PowerShell-enkäten i ”Resolve-Error” [#11021]</span><span class="sxs-lookup"><span data-stu-id="96a62-1328">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="96a62-1329">Az-version har lagts till i UserAgent</span><span class="sxs-lookup"><span data-stu-id="96a62-1329">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="96a62-1330">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="96a62-1330">Az.ApiManagement</span></span>
* <span data-ttu-id="96a62-1331">Stöd har lagts till för att hämta och konfigurera en anpassad domän på DeveloperPortal-slutpunkten [#11007]</span><span class="sxs-lookup"><span data-stu-id="96a62-1331">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="96a62-1332">”Export-AzApiManagementApi” Stöd har lagts till för att ladda ned API-definition i Json-format [#9987]</span><span class="sxs-lookup"><span data-stu-id="96a62-1332">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="96a62-1333">”Import-AzApiManagementApi” Stöd har lagts till för att importera OpenApi 3.0-definition från Json-dokument</span><span class="sxs-lookup"><span data-stu-id="96a62-1333">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="96a62-1334">”New-AzApiManagementIdentityProvider” och ”Set-AzApiManagementIdentityProvider” Stöd har lagts till för att konfigurera ”Signin Tenant” för AAD B2C-provider [#9784]</span><span class="sxs-lookup"><span data-stu-id="96a62-1334">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="96a62-1335">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="96a62-1335">Az.DataLakeStore</span></span>
* <span data-ttu-id="96a62-1336">En referens har uttryckligen lagts till för System.Buffers i csproj och psd1.</span><span class="sxs-lookup"><span data-stu-id="96a62-1336">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="96a62-1337">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="96a62-1337">Az.IotHub</span></span>
* <span data-ttu-id="96a62-1338">Lade till stöd för att hantera enheter i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="96a62-1338">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="96a62-1339">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="96a62-1339">New Cmdlets are:</span></span>
    - <span data-ttu-id="96a62-1340">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="96a62-1340">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="96a62-1341">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="96a62-1341">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="96a62-1342">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="96a62-1342">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="96a62-1343">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="96a62-1343">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="96a62-1344">Stöd har lagts till för att hantera moduler på en mål-IoT-enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="96a62-1344">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="96a62-1345">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="96a62-1345">New Cmdlets are:</span></span>
    - <span data-ttu-id="96a62-1346">”Add-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="96a62-1346">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="96a62-1347">”Get-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="96a62-1347">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="96a62-1348">”Remove-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="96a62-1348">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="96a62-1349">”Set-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="96a62-1349">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="96a62-1350">Cmdlet har lagts till för att hämta anslutningssträngen för en mål-IoT-enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="96a62-1350">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="96a62-1351">Cmdlet har lagts till för att hämta anslutningssträngen för en modul på en mål-IoT-enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="96a62-1351">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="96a62-1352">Stöd har lagts till för att hämta/ange en överordnad enhet för en IoT-enhet.</span><span class="sxs-lookup"><span data-stu-id="96a62-1352">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="96a62-1353">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="96a62-1353">New Cmdlets are:</span></span>
    - <span data-ttu-id="96a62-1354">”Get-AzIotHubDeviceParent”</span><span class="sxs-lookup"><span data-stu-id="96a62-1354">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="96a62-1355">”Set-AzIotHubDeviceParent”</span><span class="sxs-lookup"><span data-stu-id="96a62-1355">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="96a62-1356">Stöd har lagts till för att hantera en enhets överordnade och underordnade relationer.</span><span class="sxs-lookup"><span data-stu-id="96a62-1356">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="96a62-1357">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="96a62-1357">Az.Monitor</span></span>
* <span data-ttu-id="96a62-1358">Utdatavärdet har åtgärdats för ”Get-AzMetricDefinition” [#9714]</span><span class="sxs-lookup"><span data-stu-id="96a62-1358">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="96a62-1359">Az.Network</span><span class="sxs-lookup"><span data-stu-id="96a62-1359">Az.Network</span></span>
* <span data-ttu-id="96a62-1360">SQL Management SDK har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="96a62-1360">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="96a62-1361">Ett problem har åtgärdats med namngivningsskillnader i klassen PrivateLinkServiceConnectionState.</span><span class="sxs-lookup"><span data-stu-id="96a62-1361">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="96a62-1362">Fältet ActionsRequired mappar till ActionRequired.</span><span class="sxs-lookup"><span data-stu-id="96a62-1362">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="96a62-1363">PublicNetworkAccess har lagts till i ”New-AzSqlServer” och ”Set-AzSqlServer”</span><span class="sxs-lookup"><span data-stu-id="96a62-1363">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="96a62-1364">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="96a62-1364">Az.Resources</span></span>
* <span data-ttu-id="96a62-1365">Null-referensfel har åtgärdats i ”Get-AzRoleAssignment”</span><span class="sxs-lookup"><span data-stu-id="96a62-1365">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="96a62-1366">Växlarna ”-Force” och ”-PassThru” är valfria i ”Remove-AzADGroup” [#10849]</span><span class="sxs-lookup"><span data-stu-id="96a62-1366">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="96a62-1367">Ett problem har åtgärdats som gjorde att ”MailNickname” inte returnerades i ”Remove-AzADGroup” [#11167]</span><span class="sxs-lookup"><span data-stu-id="96a62-1367">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="96a62-1368">Ett problem har åtgärdats som gjorde att pipe-åtgärden ”Remove-AzADGroup” inte fungerar [#11171]</span><span class="sxs-lookup"><span data-stu-id="96a62-1368">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="96a62-1369">Ett null-referensfel har åtgärdats i GetAzureRoleAssignmentCommand</span><span class="sxs-lookup"><span data-stu-id="96a62-1369">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="96a62-1370">Attribut för icke-bakåtkompatibla ändringar har lagts till för kommande ändringar i cmdlets för principer</span><span class="sxs-lookup"><span data-stu-id="96a62-1370">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="96a62-1371">”Get-AzResourceGroup” har uppdaterats för att utföra taggfiltrering för resursgrupper på serversidan</span><span class="sxs-lookup"><span data-stu-id="96a62-1371">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="96a62-1372">Utökade Tag-cmdlets stöder -ResourceId</span><span class="sxs-lookup"><span data-stu-id="96a62-1372">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="96a62-1373">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="96a62-1373">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="96a62-1374">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="96a62-1374">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="96a62-1375">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="96a62-1375">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="96a62-1376">Ny Tag-cmdlet har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-1376">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="96a62-1377">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="96a62-1377">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="96a62-1378">Flyttade ScopedDeployment från SDK 3.3.0</span><span class="sxs-lookup"><span data-stu-id="96a62-1378">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="96a62-1379">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="96a62-1379">Az.Sql</span></span>
* <span data-ttu-id="96a62-1380">PublicNetworkAccess har lagts till i ”New-AzSqlServer” och ”Set-AzSqlServer”</span><span class="sxs-lookup"><span data-stu-id="96a62-1380">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="96a62-1381">Stöd har lagts till för konfiguration av säkerhetskopiering för långsiktig kvarhållning för hanterade databaser</span><span class="sxs-lookup"><span data-stu-id="96a62-1381">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="96a62-1382">Hämta/ange LTR-princip på en hanterad databas</span><span class="sxs-lookup"><span data-stu-id="96a62-1382">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="96a62-1383">Hämta LTR-säkerhetskopior efter hanterad databas, hanterad instans eller plats</span><span class="sxs-lookup"><span data-stu-id="96a62-1383">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="96a62-1384">Ta bort en LTR-säkerhetskopia</span><span class="sxs-lookup"><span data-stu-id="96a62-1384">Remove an LTR backup</span></span>
    - <span data-ttu-id="96a62-1385">Återställa en LTR-säkerhetskopia för att skapa en ny hanterad databas</span><span class="sxs-lookup"><span data-stu-id="96a62-1385">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="96a62-1386">MinimalTlsVersion har lagts till för New-AzSqlServer och Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="96a62-1386">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="96a62-1387">MinimalTlsVersion har lagts till för New-AzSqlInstance och Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="96a62-1387">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="96a62-1388">SQL SDK-versionen för Az.Network har ändrats</span><span class="sxs-lookup"><span data-stu-id="96a62-1388">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="96a62-1389">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="96a62-1389">Az.Storage</span></span>
* <span data-ttu-id="96a62-1390">AllowProtectedAppendWrite stöds i ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="96a62-1390">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="96a62-1391">”Set-AzRmStorageContainerImmutabilityPolicy”</span><span class="sxs-lookup"><span data-stu-id="96a62-1391">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="96a62-1392">Varningsmeddelande har lagts till om icke-bakåtkompatibel ändring för ändring av typen AzureStorageTable i en senare version</span><span class="sxs-lookup"><span data-stu-id="96a62-1392">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="96a62-1393">”New-AzStorageTable”</span><span class="sxs-lookup"><span data-stu-id="96a62-1393">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="96a62-1394">”Get-AzStorageTable”</span><span class="sxs-lookup"><span data-stu-id="96a62-1394">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="96a62-1395">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="96a62-1395">Az.Websites</span></span>
* <span data-ttu-id="96a62-1396">Tag-parametern har lagts till för ”New-AzAppServicePlan” och ”Set-AzAppServicePlan”</span><span class="sxs-lookup"><span data-stu-id="96a62-1396">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="96a62-1397">Stoppa cmdlet-körning om ett undantag uppstår när en anpassad domän läggs till på en webbplats</span><span class="sxs-lookup"><span data-stu-id="96a62-1397">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="96a62-1398">Stöd har lagts till för att utföra åtgärder för App Services som inte tillhör samma resursgrupp som App Services-planen</span><span class="sxs-lookup"><span data-stu-id="96a62-1398">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="96a62-1399">Åtkomstbegränsning har tillämpats på WebApp/Function i olika resursgrupper</span><span class="sxs-lookup"><span data-stu-id="96a62-1399">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="96a62-1400">Ett problem har åtgärdats för att ange anpassade värdnamn för WebAppSlots</span><span class="sxs-lookup"><span data-stu-id="96a62-1400">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="96a62-1401">3.5.0 – februari 2020</span><span class="sxs-lookup"><span data-stu-id="96a62-1401">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="96a62-1402">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="96a62-1402">Highlights since the last major release</span></span>
* <span data-ttu-id="96a62-1403">Uppdaterade telemetri på klientsidan.</span><span class="sxs-lookup"><span data-stu-id="96a62-1403">Updated client side telemetry.</span></span>
* <span data-ttu-id="96a62-1404">Az.IotHub lade till cmdletar som stöd för att hantera enheter.</span><span class="sxs-lookup"><span data-stu-id="96a62-1404">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="96a62-1405">Az.SqlVirtualMachine lade till cmdletar för lyssningsfunktion för tillgänglighetsgrupp.</span><span class="sxs-lookup"><span data-stu-id="96a62-1405">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="96a62-1406">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="96a62-1406">Az.Accounts</span></span>
* <span data-ttu-id="96a62-1407">Lade till SubscriptionId, TenantId och körningstid i data för telemetri på klientsidan</span><span class="sxs-lookup"><span data-stu-id="96a62-1407">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="96a62-1408">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="96a62-1408">Az.Automation</span></span>
* <span data-ttu-id="96a62-1409">Åtgärdade skrivfel i exempel 1 i referensdokumentation för ”New-AzAutomationSoftwareUpdateConfiguration”</span><span class="sxs-lookup"><span data-stu-id="96a62-1409">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="96a62-1410">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="96a62-1410">Az.CognitiveServices</span></span>
* <span data-ttu-id="96a62-1411">Uppdaterade SDK till 7.0</span><span class="sxs-lookup"><span data-stu-id="96a62-1411">Updated SDK to 7.0</span></span>
* <span data-ttu-id="96a62-1412">Förbättrade felmeddelande vid serversvar om tom brödtext</span><span class="sxs-lookup"><span data-stu-id="96a62-1412">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="96a62-1413">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="96a62-1413">Az.Compute</span></span>
* <span data-ttu-id="96a62-1414">Tillät tomt värde för ProximityPlacementGroupId under uppdatering</span><span class="sxs-lookup"><span data-stu-id="96a62-1414">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="96a62-1415">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="96a62-1415">Az.FrontDoor</span></span>
* <span data-ttu-id="96a62-1416">Lade till cmdlet för att hämta hanterade regeldefinitioner som kan användas i WAF</span><span class="sxs-lookup"><span data-stu-id="96a62-1416">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="96a62-1417">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="96a62-1417">Az.IotHub</span></span>
* <span data-ttu-id="96a62-1418">Lade till stöd för att hantera enheter i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="96a62-1418">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="96a62-1419">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="96a62-1419">New Cmdlets are:</span></span>
    - <span data-ttu-id="96a62-1420">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="96a62-1420">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="96a62-1421">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="96a62-1421">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="96a62-1422">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="96a62-1422">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="96a62-1423">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="96a62-1423">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="96a62-1424">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="96a62-1424">Az.KeyVault</span></span>
* <span data-ttu-id="96a62-1425">Åtgärdade duplicerad text för Add-AzKeyVaultKey.md</span><span class="sxs-lookup"><span data-stu-id="96a62-1425">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="96a62-1426">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="96a62-1426">Az.Monitor</span></span>
* <span data-ttu-id="96a62-1427">Åtgärdade beskrivning av cmdleten Get-AzLog.</span><span class="sxs-lookup"><span data-stu-id="96a62-1427">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="96a62-1428">En ny parameter med namnet ActionGroupId har lagts till i kommandot ”New-AzMetricAlertRuleV2”.</span><span class="sxs-lookup"><span data-stu-id="96a62-1428">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="96a62-1429">Användaren kan ange ActionGroupId(string) eller ActionGroup(ActivityLogAlertActionGroup).</span><span class="sxs-lookup"><span data-stu-id="96a62-1429">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="96a62-1430">Az.Network</span><span class="sxs-lookup"><span data-stu-id="96a62-1430">Az.Network</span></span>
* <span data-ttu-id="96a62-1431">Lade till en extra parameteranteckning för parametern ”-EnableProxyProtocol” för cmdleten ”New-AzPrivateLinkService”.</span><span class="sxs-lookup"><span data-stu-id="96a62-1431">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="96a62-1432">Åtgärdade FilterData-exempel i Start-AzVirtualNetworkGatewayConnectionPacketCapture.md och Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="96a62-1432">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="96a62-1433">Lade till paketinsamlingsexempel för att samla in alla inre och yttre paket i Start-AzVirtualNetworkGatewayConnectionPacketCapture.md och Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="96a62-1433">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="96a62-1434">Lade till stöd för Azure-brandväggsprincip på VNet-brandväggar</span><span class="sxs-lookup"><span data-stu-id="96a62-1434">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="96a62-1435">Inga nya cmdletar har lagts till.</span><span class="sxs-lookup"><span data-stu-id="96a62-1435">No new cmdlets are added.</span></span> <span data-ttu-id="96a62-1436">Lättar begränsningen för brandväggsprincip på VNet-brandväggar</span><span class="sxs-lookup"><span data-stu-id="96a62-1436">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="96a62-1437">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="96a62-1437">Az.RecoveryServices</span></span>
* <span data-ttu-id="96a62-1438">Lade till stöd för Restore-as-files för SQL-databaser.</span><span class="sxs-lookup"><span data-stu-id="96a62-1438">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="96a62-1439">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="96a62-1439">Az.Resources</span></span>
* <span data-ttu-id="96a62-1440">Omstrukturerade cmdletar för malldistribution</span><span class="sxs-lookup"><span data-stu-id="96a62-1440">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="96a62-1441">Lade till nya cmdletar för att hantera distributioner i hanteringsgruppen: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="96a62-1441">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="96a62-1442">Lade till nya cmdletar för att hantera distributioner i klientorganisationsområdet: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="96a62-1442">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="96a62-1443">Omstrukturerade \*-AzDeployment-cmdletar för att fungera specifikt i prenumerationsomfattningen</span><span class="sxs-lookup"><span data-stu-id="96a62-1443">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="96a62-1444">Skapade alias \*-AzSubscriptionDeployment för \*-AzDeployment-cmdletar</span><span class="sxs-lookup"><span data-stu-id="96a62-1444">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="96a62-1445">Åtgärdade ”Update-AzADApplication” när parametern ”AvailableToOtherTenants” inte har angetts</span><span class="sxs-lookup"><span data-stu-id="96a62-1445">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="96a62-1446">Tog bort ApplicationObjectWithoutCredentialParameterSet för att undvika AmbiguousParameterSetException.</span><span class="sxs-lookup"><span data-stu-id="96a62-1446">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="96a62-1447">Återskapade hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="96a62-1447">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="96a62-1448">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="96a62-1448">Az.Sql</span></span>
* <span data-ttu-id="96a62-1449">Lade till stöd för återställning till tidpunkt mellan prenumerationer på hanterade instanser.</span><span class="sxs-lookup"><span data-stu-id="96a62-1449">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="96a62-1450">Lade till stöd för att ändra befintlig SQL Managed Instance-maskinvarugenerering</span><span class="sxs-lookup"><span data-stu-id="96a62-1450">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="96a62-1451">Åtgärdade ”Update-AzSqlServerVulnerabilityAssessmentSetting”-hjälpexempel: parameter/egenskapsutdata - EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="96a62-1451">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="96a62-1452">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="96a62-1452">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="96a62-1453">Lade till cmdletar för lyssningsfunktion för tillgänglighetsgrupp</span><span class="sxs-lookup"><span data-stu-id="96a62-1453">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="96a62-1454">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="96a62-1454">Az.StorageSync</span></span>
* <span data-ttu-id="96a62-1455">Uppdaterade teckenuppsättningar som stöds i ”Invoke-AzStorageSyncCompatibilityCheck”.</span><span class="sxs-lookup"><span data-stu-id="96a62-1455">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="96a62-1456">3.4.0 – februari 2020</span><span class="sxs-lookup"><span data-stu-id="96a62-1456">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="96a62-1457">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="96a62-1457">Highlights since the last major release</span></span>
* <span data-ttu-id="96a62-1458">Första Az.CosmosDB-versionen 0.1.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="96a62-1458">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="96a62-1459">Stöd för Az.Network ConnectionMonitor V2 har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-1459">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="96a62-1460">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="96a62-1460">Az.Accounts</span></span>
* <span data-ttu-id="96a62-1461">Inaktivera automatisk sparande av kontext när AzureRmContext.json inte är tillgängligt</span><span class="sxs-lookup"><span data-stu-id="96a62-1461">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="96a62-1462">Uppdatera referensen till Azure Powershell Common till 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="96a62-1462">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="96a62-1463">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="96a62-1463">Az.ApiManagement</span></span>
* <span data-ttu-id="96a62-1464">**Get-AzApiManagementApiSchema** Hämtning av Open-Api-schema som är associerat med ett API har åtgärdats   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="96a62-1464">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="96a62-1465">**New-AzApiManagementProduct** _ och _ *Set-AzApiManagementProduct*\*</span><span class="sxs-lookup"><span data-stu-id="96a62-1465">**New-AzApiManagementProduct** _ and _ *Set-AzApiManagementProduct*\*</span></span>
  - <span data-ttu-id="96a62-1466">Åtgärda dokumentation för https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="96a62-1466">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="96a62-1467">**Set-AzApiManagementApi** Exempel för att visa hur ServiceUrl uppdateras med hjälp av cmdleten har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-1467">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="96a62-1468">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="96a62-1468">Az.Compute</span></span>
* <span data-ttu-id="96a62-1469">Begränsa antalet VM-status till 100 för att undvika begränsning när Get-AzVM -Status utförs utan VM-namn.</span><span class="sxs-lookup"><span data-stu-id="96a62-1469">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="96a62-1470">Lägg till cmdleten Update-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="96a62-1470">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="96a62-1471">Lägg till parametrarna EncryptionType och DiskEncryptionSetId i följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="96a62-1471">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="96a62-1472">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="96a62-1472">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="96a62-1473">Lägg till parametern ColocationStatus för cmdleten Get-AzProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="96a62-1473">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="96a62-1474">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="96a62-1474">Az.DataFactory</span></span>
* <span data-ttu-id="96a62-1475">Uppdatera ADF .Net SDK-versionen till 4.7.0</span><span class="sxs-lookup"><span data-stu-id="96a62-1475">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="96a62-1476">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="96a62-1476">Az.DeploymentManager</span></span>
* <span data-ttu-id="96a62-1477">Lägger till LIST-åtgärder för resurser</span><span class="sxs-lookup"><span data-stu-id="96a62-1477">Adds LIST operations for resources</span></span>
* <span data-ttu-id="96a62-1478">Lägger till funktion för att utföra åtgärder för hälsokontrollsteg</span><span class="sxs-lookup"><span data-stu-id="96a62-1478">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="96a62-1479">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="96a62-1479">Az.HDInsight</span></span>
* <span data-ttu-id="96a62-1480">Åtgärda dokumentfel för New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="96a62-1480">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="96a62-1481">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="96a62-1481">Az.KeyVault</span></span>
* <span data-ttu-id="96a62-1482">Lägg till Name-alias för attributet VaultName så att Remove-AzureKeyVault stämmer överens med New-AzureKeyVault.</span><span class="sxs-lookup"><span data-stu-id="96a62-1482">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="96a62-1483">Az.Network</span><span class="sxs-lookup"><span data-stu-id="96a62-1483">Az.Network</span></span>
* <span data-ttu-id="96a62-1484">Nytt exempel har lagts till i Set-AzNetworkWatcherConfigFlowLog.md för att demonstrera ett inaktiveringsscenario för Trafikanalys.</span><span class="sxs-lookup"><span data-stu-id="96a62-1484">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="96a62-1485">Lägg till stöd för att tilldela konfiguration av hanterings-IP till Azure Firewall – ett dedikerat undernät och en offentlig IP som brandväggen använder för dess hanteringstrafik</span><span class="sxs-lookup"><span data-stu-id="96a62-1485">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="96a62-1486">Cmdleten New-AzFirewall har uppdaterats:</span><span class="sxs-lookup"><span data-stu-id="96a62-1486">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="96a62-1487">Parametern -ManagementPublicIpAddress (inte obligatorisk) som accepterar ett offentligt IP-adressobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-1487">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="96a62-1488">Metoden SetManagementIpConfiguration har lagts till för brandväggsobjekt – kräver ett undernät och en offentlig IP-adress som indata – undernätets namn måste vara ”AzureFirewallManagementSubnet”</span><span class="sxs-lookup"><span data-stu-id="96a62-1488">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="96a62-1489">Exempel för Get-AzNetworkSecurityGroup har korrigerats så att exempel visas för NSG:er i stället för nätverksgränssnitt.</span><span class="sxs-lookup"><span data-stu-id="96a62-1489">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="96a62-1490">Ett skrivfel har åtgärdats i kommandot New-AzVpnSite som hindrade kompletteraren för resurs-ID från att fylla i en parameter.</span><span class="sxs-lookup"><span data-stu-id="96a62-1490">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="96a62-1491">Stöd för Url-konfiguration i åtgärdsuppsättningen för omskrivningsregler i Application Gateway har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-1491">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="96a62-1492">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="96a62-1492">New cmdlets added:</span></span>
        - <span data-ttu-id="96a62-1493">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="96a62-1493">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="96a62-1494">Cmdletar har uppdaterats med den valfria parametern -UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="96a62-1494">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="96a62-1495">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="96a62-1495">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="96a62-1496">Lägg till stöd för resurser för NetworkWatcher ConnectionMonitor version 2</span><span class="sxs-lookup"><span data-stu-id="96a62-1496">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="96a62-1497">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="96a62-1497">Az.PolicyInsights</span></span>
* <span data-ttu-id="96a62-1498">Stöd för utvärdering av efterlevnad innan fastställande av vilken resurs som ska åtgärdas</span><span class="sxs-lookup"><span data-stu-id="96a62-1498">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="96a62-1499">Lägg till parametern ”-ResourceDiscoverMode” för Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="96a62-1499">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="96a62-1500">Lägg till cmdleten Get-AzPolicyMetadata för att hämta resurser för principmetadata</span><span class="sxs-lookup"><span data-stu-id="96a62-1500">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="96a62-1501">Get-AzPolicyState och Get-AzPolicyStateSummary för API-versionen 2019-10-01 har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="96a62-1501">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="96a62-1502">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="96a62-1502">Az.RecoveryServices</span></span>
* <span data-ttu-id="96a62-1503">Azure Site Recovery-stöd för att ta bort en replikerad disk.</span><span class="sxs-lookup"><span data-stu-id="96a62-1503">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="96a62-1504">Tillagt Azure Backup-stöd för att lägga till taggar när ett Recovery Services-valv skapas.</span><span class="sxs-lookup"><span data-stu-id="96a62-1504">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="96a62-1505">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="96a62-1505">Az.Resources</span></span>
* <span data-ttu-id="96a62-1506">Gör -Scope valfritt i cmdletarna \*-AzPolicyAssignment med standardinställning till kontextprenumeration</span><span class="sxs-lookup"><span data-stu-id="96a62-1506">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="96a62-1507">Lägg till exempel på att skapa ADServicePrincipal med lösenord och nyckelautentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="96a62-1507">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="96a62-1508">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="96a62-1508">Az.Sql</span></span>
<span data-ttu-id="96a62-1509">Åtgärda cmdleten New-AzSqlDatabaseSecondary så att existensen PartnerDatabaseName kontrolleras i stället för existensen DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="96a62-1509">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="96a62-1510">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="96a62-1510">Az.Storage</span></span>
* <span data-ttu-id="96a62-1511">Stöd för angivning av krypteringsnyckeltyp för Tabell/kö i Skapa lagringskonto</span><span class="sxs-lookup"><span data-stu-id="96a62-1511">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="96a62-1512">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="96a62-1512">New-AzStorageAccount</span></span>
* <span data-ttu-id="96a62-1513">Visa RequestId när StorageException inte har ExtendedErrorInformation</span><span class="sxs-lookup"><span data-stu-id="96a62-1513">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="96a62-1514">Åtgärda exempel 6 för cmdleten Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="96a62-1514">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="96a62-1515">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="96a62-1515">Az.Websites</span></span>
* <span data-ttu-id="96a62-1516">Set-AzWebapp och Set-AzWebappSlot stöder egenskaperna AlwaysOn, MinTls och FtpsState</span><span class="sxs-lookup"><span data-stu-id="96a62-1516">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="96a62-1517">Åtgärdar problemet där inställning av HttpsOnly samtidigt som AppservicePlan ändrades med det enskilda kommandot Set-AzWebApp återställde HttpsOnly till standardvärdet</span><span class="sxs-lookup"><span data-stu-id="96a62-1517">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="96a62-1518">3.3.0 – januari 2020</span><span class="sxs-lookup"><span data-stu-id="96a62-1518">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="96a62-1519">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="96a62-1519">Az.Accounts</span></span>
* <span data-ttu-id="96a62-1520">Nu stöder Add-AzEnvironment och Set-AzEnvironment parametrarna AzureAttestationServiceEndpointResourceId och AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="96a62-1520">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="96a62-1521">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="96a62-1521">Az.Cdn</span></span>
* <span data-ttu-id="96a62-1522">Information om felsvar visas i New-AzCdnEndpoint-cmdleten</span><span class="sxs-lookup"><span data-stu-id="96a62-1522">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="96a62-1523">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="96a62-1523">Az.Compute</span></span>
* <span data-ttu-id="96a62-1524">Set-AzVMCustomScriptExtension-cmdleten har åtgärdats för en virtuell dator med hanterad OD-disk som inte har någon operativsystemprofil.</span><span class="sxs-lookup"><span data-stu-id="96a62-1524">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="96a62-1525">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="96a62-1525">Az.ContainerInstance</span></span>
* <span data-ttu-id="96a62-1526">Parameternamn som används med New-AzContainerGroup-exempel har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="96a62-1526">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="96a62-1527">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="96a62-1527">Az.DataBoxEdge</span></span>
* <span data-ttu-id="96a62-1528">Cmdleten ”Get-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-1528">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="96a62-1529">Hämta gränslagringscontainern</span><span class="sxs-lookup"><span data-stu-id="96a62-1529">Get the Edge Storage Container</span></span>
* <span data-ttu-id="96a62-1530">Cmdleten ”New-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-1530">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="96a62-1531">Skapa en ny gränslagringscontainer</span><span class="sxs-lookup"><span data-stu-id="96a62-1531">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="96a62-1532">Cmdleten ”Remove-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-1532">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="96a62-1533">Ta bort gränslagringscontainern</span><span class="sxs-lookup"><span data-stu-id="96a62-1533">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="96a62-1534">Cmdleten ”Invoke-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-1534">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="96a62-1535">Anropa åtgärd för att uppdatera data i gränslagringscontainer</span><span class="sxs-lookup"><span data-stu-id="96a62-1535">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="96a62-1536">Cmdleten ”Get-AzDataBoxEdgeStorageAccount” har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-1536">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="96a62-1537">Hämta gränslagringskontot</span><span class="sxs-lookup"><span data-stu-id="96a62-1537">Get the Edge Storage Account</span></span>
* <span data-ttu-id="96a62-1538">Cmdleten ”New-AzDataBoxEdgeStorageAccount” har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-1538">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="96a62-1539">Skapa ett nytt gränslagringskonto</span><span class="sxs-lookup"><span data-stu-id="96a62-1539">Create new Edge Storage Account</span></span>
* <span data-ttu-id="96a62-1540">Cmdleten ”Remove-AzDataBoxEdgeStorageAccount” har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-1540">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="96a62-1541">Ta bort gränslagringskontot</span><span class="sxs-lookup"><span data-stu-id="96a62-1541">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="96a62-1542">Anropa cmdleten ”Invoke-AzDataBoxEdgeShare”</span><span class="sxs-lookup"><span data-stu-id="96a62-1542">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="96a62-1543">Anropa åtgärd för att uppdatera resursdata</span><span class="sxs-lookup"><span data-stu-id="96a62-1543">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="96a62-1544">Cmdleten ”Set-AzDataBoxEdgeStorageAccountCredential” har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-1544">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="96a62-1545">Ange autentiseringsuppgifter för az databoxedge-lagringskonto</span><span class="sxs-lookup"><span data-stu-id="96a62-1545">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="96a62-1546">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="96a62-1546">Az.DataFactory</span></span>
* <span data-ttu-id="96a62-1547">Lägg till AutoUpdateETA-, LatestVersion-, PushedVersion-, TaskQueueId- och VersionStatus-egenskaper för Get-AzDataFactoryV2IntegrationRuntime-cmd</span><span class="sxs-lookup"><span data-stu-id="96a62-1547">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="96a62-1548">Uppdatera ADF .Net SDK-versionen till 4.6.0</span><span class="sxs-lookup"><span data-stu-id="96a62-1548">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="96a62-1549">Lägg till parametern ”PublicIPs” för ”Set-AzureRmDataFactoryV2IntegrationRuntime”-cmd så att Azure-SSIS IR kan skapas med statiska offentliga IP-adresser.</span><span class="sxs-lookup"><span data-stu-id="96a62-1549">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="96a62-1550">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="96a62-1550">Az.DevTestLabs</span></span>
* <span data-ttu-id="96a62-1551">Ta bort den brutna länken i Get-AzDtlAllowedVMSizesPolicy.md</span><span class="sxs-lookup"><span data-stu-id="96a62-1551">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="96a62-1552">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="96a62-1552">Az.EventHub</span></span>
* <span data-ttu-id="96a62-1553">Korrigering av problem 10634: Åtgärda referensen till null-objekt för eventhubnamespace-borttagning</span><span class="sxs-lookup"><span data-stu-id="96a62-1553">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="96a62-1554">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="96a62-1554">Az.HDInsight</span></span>
* <span data-ttu-id="96a62-1555">Åtgärda Invoke-AzHDInsightHiveJob.md-fel.</span><span class="sxs-lookup"><span data-stu-id="96a62-1555">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="96a62-1556">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="96a62-1556">Az.MachineLearning</span></span>
* <span data-ttu-id="96a62-1557">Nedanstående cmdletar har tagits bort eftersom MachineLearningCompute inte längre är tillgängligt</span><span class="sxs-lookup"><span data-stu-id="96a62-1557">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="96a62-1558">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="96a62-1558">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="96a62-1559">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="96a62-1559">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="96a62-1560">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="96a62-1560">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="96a62-1561">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="96a62-1561">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="96a62-1562">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="96a62-1562">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="96a62-1563">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="96a62-1563">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="96a62-1564">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="96a62-1564">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="96a62-1565">Az.Network</span><span class="sxs-lookup"><span data-stu-id="96a62-1565">Az.Network</span></span>
* <span data-ttu-id="96a62-1566">Uppgradera beroende av Microsoft.Azure.Management.Sql från 1.36-preview till 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="96a62-1566">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="96a62-1567">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="96a62-1567">Az.RecoveryServices</span></span>
* <span data-ttu-id="96a62-1568">Ändrat Azure Site Recovery-stöd för krypterade vilande data på virtuella datorer med hanterade diskar med kundhanterade nycklar för Azure till Azure-providern.</span><span class="sxs-lookup"><span data-stu-id="96a62-1568">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="96a62-1569">Azure Site Recovery-stöd för att ange ID för diskkrypteringsuppsättning som valfri inmatning för aktivering av skydd för VMware till Azure.</span><span class="sxs-lookup"><span data-stu-id="96a62-1569">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="96a62-1570">Azure Site Recovery-stöd för att ange ID för diskkrypteringsuppsättning som valfri inmatning på disknivå för aktivering av skydd för VMware till Azure.</span><span class="sxs-lookup"><span data-stu-id="96a62-1570">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="96a62-1571">Azure Site Recovery-stöd för att uppdatera replikeringsskyddade objekt med mappning för diskkrypteringsuppsättning för HyperV till Azure.</span><span class="sxs-lookup"><span data-stu-id="96a62-1571">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="96a62-1572">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="96a62-1572">Az.Resources</span></span>
* <span data-ttu-id="96a62-1573">Åtgärda ett fel i hjälpdokument för ”Remove-AzTag”.</span><span class="sxs-lookup"><span data-stu-id="96a62-1573">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="96a62-1574">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="96a62-1574">Az.Sql</span></span>
* <span data-ttu-id="96a62-1575">Åtgärda funktioner i cmdletar för att ange baslinjen för sårbarhetsbedömning för arbete med huvuddatabasen för Azure-databasen och begränsa den för systemdatabaser på hanterade instanser.</span><span class="sxs-lookup"><span data-stu-id="96a62-1575">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="96a62-1576">Åtgärda ett fel när en redundansgrupp för en SQL-instans skapas</span><span class="sxs-lookup"><span data-stu-id="96a62-1576">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="96a62-1577">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="96a62-1577">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="96a62-1578">Lägg till DR som en ny giltig licenstyp</span><span class="sxs-lookup"><span data-stu-id="96a62-1578">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="96a62-1579">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="96a62-1579">Az.Storage</span></span>
* <span data-ttu-id="96a62-1580">Lägg till varningsmeddelande om icke-bakåtkompatibel ändring för DefaultAction-värdeändring i en framtida version</span><span class="sxs-lookup"><span data-stu-id="96a62-1580">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="96a62-1581">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="96a62-1581">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="96a62-1582">Stöd för att hämta lagringskontots senaste synkroniseringstid genom att köra get-AzureRMStorageAccount med parametern -IncludeGeoReplicationStats</span><span class="sxs-lookup"><span data-stu-id="96a62-1582">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="96a62-1583">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="96a62-1583">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="96a62-1584">3.2.0 – December 2019</span><span class="sxs-lookup"><span data-stu-id="96a62-1584">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="96a62-1585">Allmänt</span><span class="sxs-lookup"><span data-stu-id="96a62-1585">General</span></span>
* <span data-ttu-id="96a62-1586">Uppdatera referenser i .psd1 för att använda relativa sökvägar för alla moduler</span><span class="sxs-lookup"><span data-stu-id="96a62-1586">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="96a62-1587">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="96a62-1587">Az.Accounts</span></span>
* <span data-ttu-id="96a62-1588">Ange rätt UserAgent för telemetri på klientsidan för Az 4.0 preview</span><span class="sxs-lookup"><span data-stu-id="96a62-1588">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="96a62-1589">Visa användarvänligt felmeddelande när kontexten är null i Az 4.0 preview</span><span class="sxs-lookup"><span data-stu-id="96a62-1589">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="96a62-1590">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="96a62-1590">Az.Batch</span></span>
* <span data-ttu-id="96a62-1591">Korrigera problem [#10602](https://github.com/Azure/azure-powershell/issues/10602), där **New-AzBatchPool** skickade VirtualMachineConfiguration.ContainerConfiguration eller VirtualMachineConfiguration.DataDisks på ett felaktigt sätt till servern.</span><span class="sxs-lookup"><span data-stu-id="96a62-1591">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="96a62-1592">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="96a62-1592">Az.DataFactory</span></span>
* <span data-ttu-id="96a62-1593">Uppdatera ADF .Net SDK-versionen till 4.5.0</span><span class="sxs-lookup"><span data-stu-id="96a62-1593">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="96a62-1594">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="96a62-1594">Az.FrontDoor</span></span>
* <span data-ttu-id="96a62-1595">Stöd har lagts till för undantag för hanterade regler för brandväggen för webbaserade program</span><span class="sxs-lookup"><span data-stu-id="96a62-1595">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="96a62-1596">Lägg till SocketAddr för automatisk komplettering</span><span class="sxs-lookup"><span data-stu-id="96a62-1596">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="96a62-1597">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="96a62-1597">Az.HealthcareApis</span></span>
* <span data-ttu-id="96a62-1598">Undantagshantering</span><span class="sxs-lookup"><span data-stu-id="96a62-1598">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="96a62-1599">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="96a62-1599">Az.KeyVault</span></span>
* <span data-ttu-id="96a62-1600">Åtgärdat fel vid åtkomst av värde som kanske inte har angetts</span><span class="sxs-lookup"><span data-stu-id="96a62-1600">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="96a62-1601">Hantering av ECC-certifikat (Elliptic Curve Cryptography)</span><span class="sxs-lookup"><span data-stu-id="96a62-1601">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="96a62-1602">Stöd har lagts till för att ange kurvan för certifikatprinciper</span><span class="sxs-lookup"><span data-stu-id="96a62-1602">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="96a62-1603">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="96a62-1603">Az.Monitor</span></span>
* <span data-ttu-id="96a62-1604">Lägger till valfritt argument i kommandot Lägg till diagnostikinställningar.</span><span class="sxs-lookup"><span data-stu-id="96a62-1604">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="96a62-1605">Ett växelargument som om det finns visar att exporten till Log Analytics måste ske till ett fast schema (kallas även</span><span class="sxs-lookup"><span data-stu-id="96a62-1605">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="96a62-1606">dedikerad, datatyp)</span><span class="sxs-lookup"><span data-stu-id="96a62-1606">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="96a62-1607">Az.Network</span><span class="sxs-lookup"><span data-stu-id="96a62-1607">Az.Network</span></span>
* <span data-ttu-id="96a62-1608">Stöd för IpGroups i program-, NAT- och nätverksregler för Azure Firewall.</span><span class="sxs-lookup"><span data-stu-id="96a62-1608">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="96a62-1609">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="96a62-1609">Az.Resources</span></span>
* <span data-ttu-id="96a62-1610">Åtgärda ett problem där malldistributionen inte kan läsa en mallparameter om dess namn står i konflikt med ett inbyggt parameternamn.</span><span class="sxs-lookup"><span data-stu-id="96a62-1610">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="96a62-1611">Uppdaterade princip-cmdletar för att använda den nya API-versionen 2019-09-01 som introducerar grupperingsstöd inom principuppsättningsdefinitioner.</span><span class="sxs-lookup"><span data-stu-id="96a62-1611">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="96a62-1612">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="96a62-1612">Az.Sql</span></span>
* <span data-ttu-id="96a62-1613">Uppgraderad funktion för att skapa lagring i automatisk aktivering av sårbarhetsbedömning till StorageV2</span><span class="sxs-lookup"><span data-stu-id="96a62-1613">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="96a62-1614">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="96a62-1614">Az.Storage</span></span>
* <span data-ttu-id="96a62-1615">Stöd för generering av blob/container-identitetsbaserad SAS-token med lagringskontextbaserad på OAuth-autentisering</span><span class="sxs-lookup"><span data-stu-id="96a62-1615">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="96a62-1616">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="96a62-1616">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="96a62-1617">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="96a62-1617">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="96a62-1618">Stöd för återkallning av användardelegeringsnycklar för lagringskonto för att återkalla alla SAS-token</span><span class="sxs-lookup"><span data-stu-id="96a62-1618">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="96a62-1619">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="96a62-1619">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="96a62-1620">Uppgradera till Microsoft.Azure.Management.Storage 14.2.0 för att stödja den nya API-versionen 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="96a62-1620">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="96a62-1621">Stöd för QuotaGiB (resurskvot i Gibibye) för värden över 5120 i hanteringsplanet för cmdletar för filresurser och parameteraliaset. Quota har också lagts till för parametern ”QuotaGiB”.</span><span class="sxs-lookup"><span data-stu-id="96a62-1621">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="96a62-1622">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="96a62-1622">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="96a62-1623">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="96a62-1623">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="96a62-1624">Lägg till parameteraliaset QuotaGiB i parametern Quota</span><span class="sxs-lookup"><span data-stu-id="96a62-1624">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="96a62-1625">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="96a62-1625">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="96a62-1626">Åtgärda problemet att Set-AzStorageContainerAcl kan rensa den lagrade åtkomstprincipen</span><span class="sxs-lookup"><span data-stu-id="96a62-1626">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="96a62-1627">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="96a62-1627">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="96a62-1628">3.1.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="96a62-1628">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="96a62-1629">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="96a62-1629">Highlights since the last major release</span></span>
* <span data-ttu-id="96a62-1630">Az.DataBoxEdge 1.0.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="96a62-1630">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="96a62-1631">Az.SqlVirtualMachine 1.0.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="96a62-1631">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="96a62-1632">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="96a62-1632">Az.Compute</span></span>
* <span data-ttu-id="96a62-1633">Funktion för att använda en virtuell dator igen</span><span class="sxs-lookup"><span data-stu-id="96a62-1633">VM Reapply feature</span></span>
    - <span data-ttu-id="96a62-1634">Lägg till parameter för att använda igen till cmdleten Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="96a62-1634">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="96a62-1635">Funktionen AutomaticRepairs i VM-skalningsuppsättningar:</span><span class="sxs-lookup"><span data-stu-id="96a62-1635">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="96a62-1636">Lägg till parametrarna EnableAutomaticRepair, AutomaticRepairGracePeriod och AutomaticRepairMaxInstanceRepairsPercent till följande cmdletar:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="96a62-1636">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="96a62-1637">Stöd för galleriavbildningar i flera klientorganisationer för New-AzVM</span><span class="sxs-lookup"><span data-stu-id="96a62-1637">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="96a62-1638">Lägg till "Spot" till argumentslutföraren i prioritetsparametern i cmdletarna New-AzVM, New-AzVMConfig och New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="96a62-1638">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="96a62-1639">Lägg till parametrarna DiskIOPSReadWrite och DiskMBpsReadWrite till cmdleten Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="96a62-1639">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="96a62-1640">Ändra parametern SourceImageId för cmdleten New-AzGalleryImageVersion till valfri</span><span class="sxs-lookup"><span data-stu-id="96a62-1640">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="96a62-1641">Lägg till parametrarna OSDiskImage och DataDiskImage till cmdleten New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="96a62-1641">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="96a62-1642">Lägg till parametern HyperVGeneration till cmdleten New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="96a62-1642">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="96a62-1643">Lägg till parametern SkipExtensionsOnOverprovisionedVMs till cmdletarna New-AzVmss, New-AzVmssConfig och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="96a62-1643">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="96a62-1644">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="96a62-1644">Az.DataBoxEdge</span></span>
* <span data-ttu-id="96a62-1645">Cmdleten `Get-AzDataBoxEdgeOrder` har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-1645">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="96a62-1646">Hämta ordning</span><span class="sxs-lookup"><span data-stu-id="96a62-1646">Get the Order</span></span>
* <span data-ttu-id="96a62-1647">Cmdleten `New-AzDataBoxEdgeOrder` har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-1647">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="96a62-1648">Skapa ny ordning</span><span class="sxs-lookup"><span data-stu-id="96a62-1648">Create new Order</span></span>
* <span data-ttu-id="96a62-1649">Cmdleten `Remove-AzDataBoxEdgeOrder` har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-1649">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="96a62-1650">Ta bort ordning</span><span class="sxs-lookup"><span data-stu-id="96a62-1650">Remove the Order</span></span>
* <span data-ttu-id="96a62-1651">Cmdleten `New-AzDataBoxEdgeShare` har ändrats</span><span class="sxs-lookup"><span data-stu-id="96a62-1651">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="96a62-1652">Nu skapas lokal filresurs</span><span class="sxs-lookup"><span data-stu-id="96a62-1652">Now creates Local Share</span></span>
* <span data-ttu-id="96a62-1653">Cmdleten `Set-AzDataBoxEdgeRole` har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-1653">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="96a62-1654">Nu kan IotRole mappas till filresursen</span><span class="sxs-lookup"><span data-stu-id="96a62-1654">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="96a62-1655">Cmdleten `Invoke-AzDataBoxEdgeDevice` har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-1655">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="96a62-1656">Anropa genomsökningsuppdatering, ladda ned uppdatering, installera uppdateringar på enheten</span><span class="sxs-lookup"><span data-stu-id="96a62-1656">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="96a62-1657">Cmdleten `Get-AzDataBoxEdgeTrigger` har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-1657">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="96a62-1658">Hämtar information om utlösare</span><span class="sxs-lookup"><span data-stu-id="96a62-1658">Gets the information about Triggers</span></span>
* <span data-ttu-id="96a62-1659">Cmdleten `New-AzDataBoxEdgeTrigger` har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-1659">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="96a62-1660">Skapa nya utlösare</span><span class="sxs-lookup"><span data-stu-id="96a62-1660">Create new Triggers</span></span>
* <span data-ttu-id="96a62-1661">Cmdleten `Remove-AzDataBoxEdgeTrigger` har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-1661">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="96a62-1662">Ta bort utlösare</span><span class="sxs-lookup"><span data-stu-id="96a62-1662">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="96a62-1663">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="96a62-1663">Az.DataFactory</span></span>
* <span data-ttu-id="96a62-1664">Uppdatera ADF .Net SDK-versionen till 4.4.0</span><span class="sxs-lookup"><span data-stu-id="96a62-1664">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="96a62-1665">Lägg till parametern ExpressCustomSetup för kommandot Set-AzureRmDataFactoryV2IntegrationRuntime för att aktivera installationskonfigurationer och komponenter från tredje part utan anpassat konfigurationsskript.</span><span class="sxs-lookup"><span data-stu-id="96a62-1665">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="96a62-1666">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="96a62-1666">Az.DataLakeStore</span></span>
* <span data-ttu-id="96a62-1667">Uppdatera dokumentation för Get-AzDataLakeStoreDeletedItem och Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="96a62-1667">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="96a62-1668">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="96a62-1668">Az.EventHub</span></span>
* <span data-ttu-id="96a62-1669">Korrigering av problem #10301: Korrigera datumformat för SAS-token</span><span class="sxs-lookup"><span data-stu-id="96a62-1669">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="96a62-1670">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="96a62-1670">Az.FrontDoor</span></span>
* <span data-ttu-id="96a62-1671">Lägg till parametern MinimumTlsVersion till Enable-AzFrontDoorCustomDomainHttps och New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="96a62-1671">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="96a62-1672">Lägg till parametrarna HealthProbeMethod och EnabledState till New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="96a62-1672">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="96a62-1673">Lägg till en ny cmdlet för att skapa BackendPoolsSettings-objekt som passar i skapande/uppdatering av Front Door</span><span class="sxs-lookup"><span data-stu-id="96a62-1673">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="96a62-1674">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="96a62-1674">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="96a62-1675">Az.Network</span><span class="sxs-lookup"><span data-stu-id="96a62-1675">Az.Network</span></span>
* <span data-ttu-id="96a62-1676">Ändra alternativexemplen Start-AzVirtualNetworkGatewayConnectionPacketCapture.md och Start-AzVirtualnetworkGatewayPacketCapture.md för FilterData.</span><span class="sxs-lookup"><span data-stu-id="96a62-1676">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="96a62-1677">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="96a62-1677">Az.PrivateDns</span></span>
* <span data-ttu-id="96a62-1678">Uppdaterade PrivateDns .NET SDK till version 1.0.0</span><span class="sxs-lookup"><span data-stu-id="96a62-1678">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="96a62-1679">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="96a62-1679">Az.RecoveryServices</span></span>
* <span data-ttu-id="96a62-1680">Stöd för att välja disktyp vid aktivering av skydd i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="96a62-1680">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="96a62-1681">Korrigering av bugg för åtgärdsredigering av återställningsplan i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="96a62-1681">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="96a62-1682">Återställningsstöd för att godkänna filestream-databaser i Azure Backup SQL.</span><span class="sxs-lookup"><span data-stu-id="96a62-1682">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="96a62-1683">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="96a62-1683">Az.RedisCache</span></span>
* <span data-ttu-id="96a62-1684">Parametern MinimumTlsVersion har lagts till i cmdletarna New-AzRedisCache och Set-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="96a62-1684">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="96a62-1685">Dessutom har MinimumTlsVersion lagts till i utdata för cmdleten Get-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="96a62-1685">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="96a62-1686">Verifiering har lagts till på parametern -Size i cmdletarna Set-AzRedisCache och New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="96a62-1686">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="96a62-1687">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="96a62-1687">Az.Resources</span></span>
- <span data-ttu-id="96a62-1688">Uppdaterade policy-cmdletar för att använda den nya API-versionen 2019-06-01 som har en ny EnforcementMode-egenskap i policytilldelningen.</span><span class="sxs-lookup"><span data-stu-id="96a62-1688">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="96a62-1689">Uppdaterade hjälpexempel för skapandet av policydefinition</span><span class="sxs-lookup"><span data-stu-id="96a62-1689">Updated create policy definition help example</span></span>
- <span data-ttu-id="96a62-1690">Åtgärda bugg i Remove-AZADServicePrincipal -ServicePrincipalName, utlös null-referens när tjänstens huvudnamn inte hittas.</span><span class="sxs-lookup"><span data-stu-id="96a62-1690">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="96a62-1691">Åtgärda bugg i New-AZADServicePrincipal, utlös null-referens när klientorganisationen inte har någon prenumeration.</span><span class="sxs-lookup"><span data-stu-id="96a62-1691">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="96a62-1692">Ändra New-AzAdServicePrincipal för att endast lägga till autentiseringsuppgifter för det associerade programmet.</span><span class="sxs-lookup"><span data-stu-id="96a62-1692">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="96a62-1693">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="96a62-1693">Az.Sql</span></span>
* <span data-ttu-id="96a62-1694">Stöd har lagts till för databasen ReadReplicaCount.</span><span class="sxs-lookup"><span data-stu-id="96a62-1694">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="96a62-1695">Korrigerade Set-AzSqlDatabase när zonredundans inte har angetts</span><span class="sxs-lookup"><span data-stu-id="96a62-1695">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="96a62-1696">3.0.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="96a62-1696">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="96a62-1697">Allmänt</span><span class="sxs-lookup"><span data-stu-id="96a62-1697">General</span></span>
* <span data-ttu-id="96a62-1698">Az. PrivateDns 1.0.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="96a62-1698">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="96a62-1699">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="96a62-1699">Az.Accounts</span></span>
* <span data-ttu-id="96a62-1700">Lägg till ett utfasningsmeddelande för aliaset Resolve-error.</span><span class="sxs-lookup"><span data-stu-id="96a62-1700">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="96a62-1701">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="96a62-1701">Az.Advisor</span></span>
* <span data-ttu-id="96a62-1702">Den nya kategorin Operational Excellence har lagts till i cmdleten Get-AzAdvisorRecommendation.</span><span class="sxs-lookup"><span data-stu-id="96a62-1702">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="96a62-1703">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="96a62-1703">Az.Batch</span></span>
* <span data-ttu-id="96a62-1704">`CoreQuota` på `BatchAccountContext` har bytt namn till `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="96a62-1704">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="96a62-1705">Det finns även en ny `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="96a62-1705">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="96a62-1706">Detta påverkar **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="96a62-1706">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="96a62-1707">**New-AzBatchTask** `-ResourceFile`-parametern tar nu en samling `PSResourceFile`-objekt som kan skapas med hjälp av den nya cmdleten **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="96a62-1707">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="96a62-1708">Ny **New-AzBatchResourceFile**-cmdlet för att skapa `PSResourceFile`-objekt.</span><span class="sxs-lookup"><span data-stu-id="96a62-1708">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="96a62-1709">Dessa kan tillhandahållas till **New-AzBatchTask** på `-ResourceFile`-parametern.</span><span class="sxs-lookup"><span data-stu-id="96a62-1709">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="96a62-1710">Detta stöder två nya typer av resursfiler förutom det befintliga sättet med `HttpUrl`:</span><span class="sxs-lookup"><span data-stu-id="96a62-1710">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="96a62-1711">`AutoStorageContainerName`-baserade resursfiler laddar ned en hel container för automatisk lagring till Batch-noden.</span><span class="sxs-lookup"><span data-stu-id="96a62-1711">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="96a62-1712">`StorageContainerUrl`-baserade resursfiler laddar ned containern som anges i webbadressen till Batch-noden.</span><span class="sxs-lookup"><span data-stu-id="96a62-1712">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="96a62-1713">Tog bort egenskapen `ApplicationPackages` för `PSApplication` som returnerades av **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="96a62-1713">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="96a62-1714">Specifika paket i ett program kan nu hämtas med hjälp av **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="96a62-1714">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="96a62-1715">Till exempel: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="96a62-1715">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="96a62-1716">Bytt namn på `ApplicationId` till `ApplicationName` på **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** och **Set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="96a62-1716">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="96a62-1717">`ApplicationId` är nu ett alias för `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="96a62-1717">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="96a62-1718">Ny `PSWindowsUserConfiguration`-egenskap till `PSUserAccount` lades till.</span><span class="sxs-lookup"><span data-stu-id="96a62-1718">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="96a62-1719">Bytte namn på `Version` till `Name` på `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="96a62-1719">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="96a62-1720">Bytte namn på `BlobSource` till `HttpUrl` på `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="96a62-1720">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="96a62-1721">Tog bort egenskapen `OSDisk` från `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="96a62-1721">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="96a62-1722">Tog bort **Set-AzBatchPoolOSVersion**.</span><span class="sxs-lookup"><span data-stu-id="96a62-1722">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="96a62-1723">Den här åtgärden stöds inte längre.</span><span class="sxs-lookup"><span data-stu-id="96a62-1723">This operation is no longer supported.</span></span>
* <span data-ttu-id="96a62-1724">`TargetOSVersion` har tagits bort från `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="96a62-1724">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="96a62-1725">Bytte namn på `CurrentOSVersion` till `OSVersion` på `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="96a62-1725">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="96a62-1726">`DataEgressGiB` och `DataIngressGiB` har tagits bort från `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="96a62-1726">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="96a62-1727">Tog bort **Get-AzBatchNodeAgentSku** och ersatte det med **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="96a62-1727">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="96a62-1728">**Get-AzBatchSupportedImage** returnerar samma data som **Get-AzBatchNodeAgentSku** men i ett mer användarvänligt format.</span><span class="sxs-lookup"><span data-stu-id="96a62-1728">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="96a62-1729">Nya icke-verifierade avbildningar returneras nu också.</span><span class="sxs-lookup"><span data-stu-id="96a62-1729">New non-verified images are also now returned.</span></span> <span data-ttu-id="96a62-1730">Ytterligare information om `Capabilities` och `BatchSupportEndOfLife` för varje avbildning inkluderas också.</span><span class="sxs-lookup"><span data-stu-id="96a62-1730">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="96a62-1731">Lade till möjlighet att montera fjärrfilsystem på varje nod i en pool via den nya parametern `MountConfiguration` för **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="96a62-1731">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="96a62-1732">Har nu stöd för nätverkssäkerhetsregler som blockerar nätverksåtkomst till en pool baserat på källportens trafik.</span><span class="sxs-lookup"><span data-stu-id="96a62-1732">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="96a62-1733">Detta görs via egenskapen `SourcePortRanges` på `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="96a62-1733">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="96a62-1734">När du kör en container stöder nu Batch körningen av uppgiften i arbetskatalogen för containern eller i arbetskatalogen för Batch-uppgiften.</span><span class="sxs-lookup"><span data-stu-id="96a62-1734">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="96a62-1735">Detta styrs av egenskapen `WorkingDirectory` på `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="96a62-1735">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="96a62-1736">Lade till en funktion för att ange en samling av offentliga IP-adresser på `PSNetworkConfiguration` via den nya egenskapen `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="96a62-1736">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="96a62-1737">Detta garanterar att noderna i poolen har en IP-adress från listan över IP-adresser som tillhandahållits av användare.</span><span class="sxs-lookup"><span data-stu-id="96a62-1737">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="96a62-1738">Om inget värde anges är standardvärdet för `WaitForSuccess` på `PSSTartTask` nu `$True` (var tidigare `$False`).</span><span class="sxs-lookup"><span data-stu-id="96a62-1738">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="96a62-1739">Om inget värde anges är standardvärdet för `Scope` på `PSAutoUserSpecification` nu `Pool` (var tidigare `Task` på Windows och `Pool` på Linux).</span><span class="sxs-lookup"><span data-stu-id="96a62-1739">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="96a62-1740">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="96a62-1740">Az.Cdn</span></span>
* <span data-ttu-id="96a62-1741">Introducerade UrlRewriteAction och CacheKeyQueryStringAction till RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="96a62-1741">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="96a62-1742">Åtgärdade flera buggar, som saknade indata för ”väljare” i cmdleten New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="96a62-1742">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="96a62-1743">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="96a62-1743">Az.Compute</span></span>
* <span data-ttu-id="96a62-1744">Funktion för diskkrypteringsuppsättning</span><span class="sxs-lookup"><span data-stu-id="96a62-1744">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="96a62-1745">Nya cmdletar:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="96a62-1745">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="96a62-1746">Parametern DiskEncryptionSetId har lagts till i följande cmdletar:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="96a62-1746">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="96a62-1747">Parametrarna DiskEncryptionSetId och EncryptionType har lagts till i följande cmdletar:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="96a62-1747">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="96a62-1748">Lägg till parametern PublicIPAddressVersion i New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="96a62-1748">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="96a62-1749">Flytta FileUris för anpassat skripttillägg från offentlig inställning till skyddad inställning</span><span class="sxs-lookup"><span data-stu-id="96a62-1749">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="96a62-1750">Lägg till ScaleInPolicy i cmdletarna New-AzVmss, New-AzVmssConfig och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="96a62-1750">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="96a62-1751">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="96a62-1751">Breaking changes</span></span>
    - <span data-ttu-id="96a62-1752">Parametern UploadSizeInBytes används istället för DiskSizeGB för New-AzDiskConfig när CreateOption är Uppladdning</span><span class="sxs-lookup"><span data-stu-id="96a62-1752">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="96a62-1753">PublishingProfile.Source.ManagedImage.Id ersätts med StorageProfile.Source.Id i objektet GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="96a62-1753">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="96a62-1754">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="96a62-1754">Az.DataFactory</span></span>
* <span data-ttu-id="96a62-1755">Uppdatera ADF .Net SDK-versionen till 4.3.0</span><span class="sxs-lookup"><span data-stu-id="96a62-1755">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="96a62-1756">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="96a62-1756">Az.DataLakeStore</span></span>
* <span data-ttu-id="96a62-1757">Uppdatera ADLS SDK-version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) innehåller följande korrigeringar</span><span class="sxs-lookup"><span data-stu-id="96a62-1757">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="96a62-1758">Undvik att utlösa undantag när det inte går att deserialisera creationtime för inmatning av papperskorg eller katalog.</span><span class="sxs-lookup"><span data-stu-id="96a62-1758">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="96a62-1759">Gör inställning tillgänglig per tidsgräns för förfrågan i adlsclient</span><span class="sxs-lookup"><span data-stu-id="96a62-1759">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="96a62-1760">Korrigera överföringen av ursprunglig syncflag för badoffset-återställning</span><span class="sxs-lookup"><span data-stu-id="96a62-1760">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="96a62-1761">Korrigera EnumerateDirectory för att hämta fortsättningstoken när svar har kontrollerats</span><span class="sxs-lookup"><span data-stu-id="96a62-1761">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="96a62-1762">Korrigera bugg i Concat</span><span class="sxs-lookup"><span data-stu-id="96a62-1762">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="96a62-1763">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="96a62-1763">Az.FrontDoor</span></span>
* <span data-ttu-id="96a62-1764">Åtgärdade diverse stavfel i modul</span><span class="sxs-lookup"><span data-stu-id="96a62-1764">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="96a62-1765">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="96a62-1765">Az.HDInsight</span></span>
* <span data-ttu-id="96a62-1766">Korrigerade buggen att kunder får felet ”inte en giltig Base-64-sträng” vid användning av Get-AzHDInsightCluster för att hämta klustret med ADLSGen1-lagring.</span><span class="sxs-lookup"><span data-stu-id="96a62-1766">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="96a62-1767">Lägg till en parameter med namnet ”ApplicationId” i de tre cmdletarna Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig och New-AzHDInsightCluster så att kunden kan tillhandahålla tjänstens huvudnamn för program-ID för åtkomst till Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="96a62-1767">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="96a62-1768">Ändrade Microsoft.Azure.Management.HDInsight från 2.1.0 till 5.1.0</span><span class="sxs-lookup"><span data-stu-id="96a62-1768">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="96a62-1769">Fem cmdletar har tagits bort:</span><span class="sxs-lookup"><span data-stu-id="96a62-1769">Removed five cmdlets:</span></span>
    - <span data-ttu-id="96a62-1770">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="96a62-1770">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="96a62-1771">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="96a62-1771">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="96a62-1772">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="96a62-1772">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="96a62-1773">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="96a62-1773">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="96a62-1774">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="96a62-1774">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="96a62-1775">Tre cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="96a62-1775">Added three cmdlets:</span></span>
    - <span data-ttu-id="96a62-1776">Get-AzHDInsightMonitoring som ersätter Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="96a62-1776">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="96a62-1777">Enable-AzHDInsightMonitoring som ersätter Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="96a62-1777">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="96a62-1778">Disable-AzHDInsightMonitoring som ersätter Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="96a62-1778">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="96a62-1779">Korrigerade cmdleten Get-AzHDInsightProperties för att stödja hämtning av funktionsinformation från en viss plats.</span><span class="sxs-lookup"><span data-stu-id="96a62-1779">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="96a62-1780">Parameteruppsättningarna (Spark1 och Spark2) har tagits bort från Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="96a62-1780">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="96a62-1781">Lägg till exempel för cmdleten Add-AzHDInsightSecurityProfile till hjälpdokumenten.</span><span class="sxs-lookup"><span data-stu-id="96a62-1781">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="96a62-1782">Ändrade utdatatyp för följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="96a62-1782">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="96a62-1783">Ändrade utdatatyp för Get-AzHDInsightProperties från CapabilitiesResponse till AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="96a62-1783">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="96a62-1784">Ändrade utdatatyp för Remove-AzHDInsightCluster från ClusterGetResponse till bool.</span><span class="sxs-lookup"><span data-stu-id="96a62-1784">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="96a62-1785">Ändrade utdatatyp för Set-AzHDInsightGatewaySettings HttpConnectivitySettings till GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="96a62-1785">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="96a62-1786">Lade till testfall för vissa scenarier.</span><span class="sxs-lookup"><span data-stu-id="96a62-1786">Added some scenario test cases.</span></span>
* <span data-ttu-id="96a62-1787">Ta bort vissa alias: Add-AzHDInsightConfigValues, Get-AzHDInsightProperties.</span><span class="sxs-lookup"><span data-stu-id="96a62-1787">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="96a62-1788">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="96a62-1788">Az.IotHub</span></span>
* <span data-ttu-id="96a62-1789">Icke-bakåtkompatibla ändringar:</span><span class="sxs-lookup"><span data-stu-id="96a62-1789">Breaking changes:</span></span>
    - <span data-ttu-id="96a62-1790">Cmdleten Add-AzIotHubEventHubConsumerGroup har inte längre stöd för parametern EventHubEndpointName och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="96a62-1790">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="96a62-1791">Parameteruppsättningen __AllParameterSets för cmdleten Add-AzIotHubEventHubConsumerGroup har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="96a62-1791">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="96a62-1792">Cmdleten Get-AzIotHubEventHubConsumerGroup har inte längre stöd för parametern EventHubEndpointName och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="96a62-1792">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="96a62-1793">Parameteruppsättningen __AllParameterSets för cmdleten Get-AzIotHubEventHubConsumerGroup har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="96a62-1793">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="96a62-1794">Egenskapen OperationsMonitoringProperties av typen Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="96a62-1794">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="96a62-1795">Egenskapen OperationsMonitoringProperties av typen Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="96a62-1795">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="96a62-1796">Cmdleten New-AzIotHubExportDevice stöder inte längre aliaset New-AzIotHubExportDevices.</span><span class="sxs-lookup"><span data-stu-id="96a62-1796">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="96a62-1797">Cmdleten New-AzIotHubImportDevice stöder inte längre aliaset New-AzIotHubImportDevices.</span><span class="sxs-lookup"><span data-stu-id="96a62-1797">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="96a62-1798">Cmdleten Remove-AzIotHubEventHubConsumerGroup har inte längre stöd för parametern EventHubEndpointName och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="96a62-1798">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="96a62-1799">Parameteruppsättningen __AllParameterSets för cmdleten Remove-AzIotHubEventHubConsumerGroup har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="96a62-1799">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="96a62-1800">Cmdleten Set-AzIotHub har inte längre stöd för parametern OperationsMonitoringProperties och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="96a62-1800">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="96a62-1801">Parameteruppsättningen UpdateOperationsMonitoringProperties för cmdleten Set-AzIotHub har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="96a62-1801">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="96a62-1802">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="96a62-1802">Az.RecoveryServices</span></span>
* <span data-ttu-id="96a62-1803">Azure Site Recovery-stöd för att konfigurera nätverksresurser som NSG, offentliga IP-adresser och interna lastbalanserare för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="96a62-1803">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="96a62-1804">Azure Site Recovery-stöd för att skriva till hanterad disk för vMWare till Azure.</span><span class="sxs-lookup"><span data-stu-id="96a62-1804">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="96a62-1805">Azure Site Recovery-stöd för NIC-reduktion för vMWare till Azure.</span><span class="sxs-lookup"><span data-stu-id="96a62-1805">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="96a62-1806">Azure Site Recovery-stöd för accelererat nätverk för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="96a62-1806">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="96a62-1807">Azure Site Recovery-stöd för automatisk uppdatering av agent för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="96a62-1807">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="96a62-1808">Azure Site Recovery-stöd för Standard SSD för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="96a62-1808">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="96a62-1809">Azure Site Recovery-stöd för tvåstegskryptering i Azure Disk Encryption för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="96a62-1809">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="96a62-1810">Azure Site Recovery-stöd för att skydda nyligen tillagda diskar för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="96a62-1810">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="96a62-1811">En funktion för mjuk borttagning av virtuella datorer samt tester för mjuk borttagning har tagits bort</span><span class="sxs-lookup"><span data-stu-id="96a62-1811">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="96a62-1812">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="96a62-1812">Az.Resources</span></span>
* <span data-ttu-id="96a62-1813">Uppdatera beroendesammansättning för Microsoft.Extensions.Caching.Memory från 1.1.1 till 2.2</span><span class="sxs-lookup"><span data-stu-id="96a62-1813">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="96a62-1814">Az.Network</span><span class="sxs-lookup"><span data-stu-id="96a62-1814">Az.Network</span></span>
* <span data-ttu-id="96a62-1815">Ändra alla cmdletar för PrivateEndpointConnection så att de stöder generiska tjänstleverantörer.</span><span class="sxs-lookup"><span data-stu-id="96a62-1815">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="96a62-1816">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="96a62-1816">Updated cmdlet:</span></span>
        - <span data-ttu-id="96a62-1817">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="96a62-1817">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="96a62-1818">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="96a62-1818">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="96a62-1819">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="96a62-1819">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="96a62-1820">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="96a62-1820">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="96a62-1821">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="96a62-1821">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="96a62-1822">Lägg till ny cmdlet för PrivateLinkResource så att det också stöder generiska tjänstleverantörer.</span><span class="sxs-lookup"><span data-stu-id="96a62-1822">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="96a62-1823">Ny cmdlet:</span><span class="sxs-lookup"><span data-stu-id="96a62-1823">New cmdlet:</span></span>
        - <span data-ttu-id="96a62-1824">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="96a62-1824">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="96a62-1825">Lägg till nya fält och parametrar för funktionen Proxy Protocol V2.</span><span class="sxs-lookup"><span data-stu-id="96a62-1825">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="96a62-1826">Lägg till egenskapen EnableProxyProtocol i PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="96a62-1826">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="96a62-1827">Lägg till egenskapen LinkIdentifier i PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="96a62-1827">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="96a62-1828">Uppdaterade New-AzPrivateLinkService för att lägga till den nya valfria parametern EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="96a62-1828">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="96a62-1829">Korrigera felaktig beskrivning av parameter i referensdokumentationen för New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="96a62-1829">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="96a62-1830">Nya cmdletar som stöder Azure-brandväggsprincipen</span><span class="sxs-lookup"><span data-stu-id="96a62-1830">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="96a62-1831">Lägg till stöd för den underordnade resursen RouteTables för VirtualHub</span><span class="sxs-lookup"><span data-stu-id="96a62-1831">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="96a62-1832">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="96a62-1832">New cmdlets added:</span></span>
        - <span data-ttu-id="96a62-1833">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="96a62-1833">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="96a62-1834">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="96a62-1834">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="96a62-1835">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="96a62-1835">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="96a62-1836">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="96a62-1836">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="96a62-1837">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="96a62-1837">Set-AzVirtualHub</span></span>
* <span data-ttu-id="96a62-1838">Lägg till stöd för ny egenskaps-SKU för VirtualHub och VirtualWANType för VirtualWan</span><span class="sxs-lookup"><span data-stu-id="96a62-1838">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="96a62-1839">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="96a62-1839">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="96a62-1840">New-AzVirtualHub: lade till parameter-SKU</span><span class="sxs-lookup"><span data-stu-id="96a62-1840">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="96a62-1841">Update-AzVirtualHub: lade till parameter-SKU</span><span class="sxs-lookup"><span data-stu-id="96a62-1841">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="96a62-1842">New-AzVirtualWan: lade till parametern VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="96a62-1842">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="96a62-1843">Update-AzVirtualWan: lade till parametern VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="96a62-1843">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="96a62-1844">Lägg till stöd för egenskapen EnableInternetSecurity för HubVnetConnection, VpnConnection och ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="96a62-1844">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="96a62-1845">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="96a62-1845">New cmdlets added:</span></span>
        - <span data-ttu-id="96a62-1846">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="96a62-1846">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="96a62-1847">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="96a62-1847">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="96a62-1848">New-AzureRmVirtualHubVnetConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-1848">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="96a62-1849">New-AzureRmVpnConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-1849">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="96a62-1850">Update-AzureRmVpnConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-1850">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="96a62-1851">New-AzureRmExpressRouteConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-1851">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="96a62-1852">Set-AzureRmExpressRouteConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-1852">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="96a62-1853">Lägg till stöd för att konfigurera TopLevel WebApplicationFirewall-princip</span><span class="sxs-lookup"><span data-stu-id="96a62-1853">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="96a62-1854">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="96a62-1854">New cmdlets added:</span></span>
        - <span data-ttu-id="96a62-1855">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="96a62-1855">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="96a62-1856">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="96a62-1856">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="96a62-1857">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="96a62-1857">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="96a62-1858">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="96a62-1858">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="96a62-1859">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="96a62-1859">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="96a62-1860">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="96a62-1860">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="96a62-1861">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="96a62-1861">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="96a62-1862">New-AzApplicationGatewayFirewallPolicy: parametrarna PolicySetting, ManagedRule har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-1862">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="96a62-1863">Stöd för operator för geomatchning har lagts till på CustomRule</span><span class="sxs-lookup"><span data-stu-id="96a62-1863">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="96a62-1864">Geomatchning har lagts till i operatorn på FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="96a62-1864">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="96a62-1865">Stöd har lagts till för brandväggsprinciperna perListener och perSite</span><span class="sxs-lookup"><span data-stu-id="96a62-1865">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="96a62-1866">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="96a62-1866">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="96a62-1867">New-AzApplicationGatewayHttpListener: parametrarna FirewallPolicy, FirewallPolicyId har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-1867">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="96a62-1868">New-AzApplicationGatewayPathRuleConfig: parametrarna FirewallPolicy, FirewallPolicyId har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-1868">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="96a62-1869">Åtgärdat så att nödvändigt undernät med namnet AzureBastionSubnet i PSBastion kan vara skiftlägesokänsligt</span><span class="sxs-lookup"><span data-stu-id="96a62-1869">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="96a62-1870">Stöd för mål-FQDN:er i nätverksregler och översatt FQDN i NAT-regler för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="96a62-1870">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="96a62-1871">Lägg till stöd för resursen RouteTables för IpGroup på den högsta nivån</span><span class="sxs-lookup"><span data-stu-id="96a62-1871">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="96a62-1872">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="96a62-1872">New cmdlets added:</span></span>
        - <span data-ttu-id="96a62-1873">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="96a62-1873">New-AzIpGroup</span></span>
        - <span data-ttu-id="96a62-1874">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="96a62-1874">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="96a62-1875">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="96a62-1875">Get-AzIpGroup</span></span>
        - <span data-ttu-id="96a62-1876">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="96a62-1876">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="96a62-1877">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="96a62-1877">Az.ServiceFabric</span></span>
* <span data-ttu-id="96a62-1878">Ta bort cmdleten Add-AzServiceFabricApplicationCertificate eftersom det här scenariot omfattas av Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="96a62-1878">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="96a62-1879">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="96a62-1879">Az.Sql</span></span>
* <span data-ttu-id="96a62-1880">Stöd har lagts till för återställning av utelämnade databaser på hanterade instanser.</span><span class="sxs-lookup"><span data-stu-id="96a62-1880">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="96a62-1881">Inaktuella gamla cmdletar för granskning från kod.</span><span class="sxs-lookup"><span data-stu-id="96a62-1881">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="96a62-1882">Tog bort inaktuella alias:</span><span class="sxs-lookup"><span data-stu-id="96a62-1882">Removed deprecated aliases:</span></span>
* <span data-ttu-id="96a62-1883">Get-AzSqlDatabaseIndexRecommendations (använd Get-AzSqlDatabaseIndexRecommendation istället)</span><span class="sxs-lookup"><span data-stu-id="96a62-1883">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="96a62-1884">Get-AzSqlDatabaseRestorePoints (använd Get-AzSqlDatabaseRestorePoint istället)</span><span class="sxs-lookup"><span data-stu-id="96a62-1884">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="96a62-1885">Ta bort cmdleten Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="96a62-1885">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="96a62-1886">Ta bort alias för inaktuella cmdletar för inställningar för utvärdering av säkerhetsrisk</span><span class="sxs-lookup"><span data-stu-id="96a62-1886">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="96a62-1887">Inaktualisera cmdletar för inställningar för avancerad hotidentifiering</span><span class="sxs-lookup"><span data-stu-id="96a62-1887">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="96a62-1888">Lägga till cmdletar för att inaktivera och aktivera känslighetsrekommendationer på kolumner i en databas.</span><span class="sxs-lookup"><span data-stu-id="96a62-1888">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="96a62-1889">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="96a62-1889">Az.Storage</span></span>
* <span data-ttu-id="96a62-1890">Stöd för att aktivera stora filresurser vid skapande eller uppdatering av lagringskonto</span><span class="sxs-lookup"><span data-stu-id="96a62-1890">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="96a62-1891">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="96a62-1891">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="96a62-1892">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="96a62-1892">Set-AzStorageAccount</span></span>
* <span data-ttu-id="96a62-1893">När du stänger/hämtar en filreferens kan du hoppa över kontrollen av huruvida indatasökvägen är en filkatalog eller en fil för att undvika problem med objekt som har status DeletePending</span><span class="sxs-lookup"><span data-stu-id="96a62-1893">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="96a62-1894">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="96a62-1894">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="96a62-1895">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="96a62-1895">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="96a62-1896">2.8.0 – oktober 2019</span><span class="sxs-lookup"><span data-stu-id="96a62-1896">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="96a62-1897">Allmänt</span><span class="sxs-lookup"><span data-stu-id="96a62-1897">General</span></span>
* <span data-ttu-id="96a62-1898">AZ. HealthcareApis 1.0.0-version</span><span class="sxs-lookup"><span data-stu-id="96a62-1898">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="96a62-1899">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="96a62-1899">Az.Accounts</span></span>
* <span data-ttu-id="96a62-1900">Uppdatera telemetri och URL-omskrivning för genererade moduler, korrigera Windows-enhetstester.</span><span class="sxs-lookup"><span data-stu-id="96a62-1900">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="96a62-1901">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="96a62-1901">Az.ApiManagement</span></span>
* <span data-ttu-id="96a62-1902">**Set-AzApiManagementApi** – Tillagt stöd för att uppdatera Api till ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="96a62-1902">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="96a62-1903">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="96a62-1903">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="96a62-1904">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="96a62-1904">Az.Automation</span></span>
* <span data-ttu-id="96a62-1905">Åtgärdade cmdleten New-AzureAutomationSoftwareUpdateConfiguration för parametern för inställning av Linux-omstart.</span><span class="sxs-lookup"><span data-stu-id="96a62-1905">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="96a62-1906">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="96a62-1906">Az.Batch</span></span>
* <span data-ttu-id="96a62-1907">**Get-AzBatchNodeAgentSku** är inaktuell och ersätts av **Get-AzBatchSupportImage** i version 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="96a62-1907">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="96a62-1908">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="96a62-1908">Az.Compute</span></span>
* <span data-ttu-id="96a62-1909">Lägg till parametrarna Priority, EvictionPolicy och MaxPrice till cmdletarna New-AzVM och New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="96a62-1909">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="96a62-1910">Korrigera varningsmeddelande och hjälpdokument för cmdletarna Add-AzVMAdditionalUnattendContent och Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="96a62-1910">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="96a62-1911">Åtgärda – skipVmBackup-undantag för virtuella Linux-datorer med hanterade diskar för Set-AzVMDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="96a62-1911">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="96a62-1912">Åtgärda fel i uppdatera krypteringsinställningarna i set-AzVMDiskEncryptionExtension, scenario i två steg.</span><span class="sxs-lookup"><span data-stu-id="96a62-1912">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="96a62-1913">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="96a62-1913">Az.DataFactory</span></span>
* <span data-ttu-id="96a62-1914">Lägga till CRUD-kommandon för ADF V2-dataflödet: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow och Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="96a62-1914">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="96a62-1915">Lägger till åtgärdskommandon för ADF V2-dataflödesfelsökningssession: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand och Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="96a62-1915">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="96a62-1916">Uppdatera ADF .Net SDK-versionen till 4.2.0</span><span class="sxs-lookup"><span data-stu-id="96a62-1916">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="96a62-1917">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="96a62-1917">Az.DataLakeStore</span></span>
* <span data-ttu-id="96a62-1918">Korrigera kontovalidering så att konton med ”-” kan skickas utan domän</span><span class="sxs-lookup"><span data-stu-id="96a62-1918">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="96a62-1919">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="96a62-1919">Az.HealthcareApis</span></span>
* <span data-ttu-id="96a62-1920">PowerShell-versionen har uppdaterats till 1.0.0</span><span class="sxs-lookup"><span data-stu-id="96a62-1920">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="96a62-1921">Uppdaterade SDK-versionen till 1.0.2</span><span class="sxs-lookup"><span data-stu-id="96a62-1921">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="96a62-1922">Uppdatera i tester för att referera till en ny SDK-version</span><span class="sxs-lookup"><span data-stu-id="96a62-1922">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="96a62-1923">Utdatastrukturen har uppdaterats från kapslad till förenklad.</span><span class="sxs-lookup"><span data-stu-id="96a62-1923">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="96a62-1924">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="96a62-1924">Az.IotHub</span></span>
* <span data-ttu-id="96a62-1925">Lägg till ny routningskälla: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="96a62-1925">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="96a62-1926">Mindre felkorrigering: Get-AzIothub returnerar inte subscriptionId</span><span class="sxs-lookup"><span data-stu-id="96a62-1926">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="96a62-1927">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="96a62-1927">Az.Monitor</span></span>
* <span data-ttu-id="96a62-1928">Nya åtgärdsgruppsmottagare har lagts till för åtgärdsgrupp   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="96a62-1928">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="96a62-1929">Använd vanligt aviseringsschema som är aktiverat för mottagarna.</span><span class="sxs-lookup"><span data-stu-id="96a62-1929">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="96a62-1930">Detta gäller inte för SMS, push för Azure-app, ITSM och röstmottagare</span><span class="sxs-lookup"><span data-stu-id="96a62-1930">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="96a62-1931">Webhooks har nu stöd för Azure Active Directory-autentisering.</span><span class="sxs-lookup"><span data-stu-id="96a62-1931">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="96a62-1932">Az.Network</span><span class="sxs-lookup"><span data-stu-id="96a62-1932">Az.Network</span></span>
* <span data-ttu-id="96a62-1933">Lägg till ny cmdlet Get-AzAvailableServiceAlias som kan anropas för att hämta de alias som kan användas för tjänstslutpunktsprinciper.</span><span class="sxs-lookup"><span data-stu-id="96a62-1933">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="96a62-1934">Stöd för tillägg av trafikväljare har lagts till i gatewayanslutningar för virtuella nätverk</span><span class="sxs-lookup"><span data-stu-id="96a62-1934">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="96a62-1935">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="96a62-1935">New cmdlets added:</span></span>
        - <span data-ttu-id="96a62-1936">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="96a62-1936">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="96a62-1937">Cmdletar har uppdaterats med valfri parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="96a62-1937">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="96a62-1938">Lägg till stöd för ESP- och AH-protokoll i konfiguration av nätverkssäkerhetsregler</span><span class="sxs-lookup"><span data-stu-id="96a62-1938">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="96a62-1939">Uppdaterade cmdletar:</span><span class="sxs-lookup"><span data-stu-id="96a62-1939">Updated cmdlets:</span></span>
        - <span data-ttu-id="96a62-1940">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="96a62-1940">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="96a62-1941">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="96a62-1941">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="96a62-1942">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="96a62-1942">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="96a62-1943">Förbättra hanteringen av undantag i Cortex-cmdletar</span><span class="sxs-lookup"><span data-stu-id="96a62-1943">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="96a62-1944">Nya generationer och SKU:er för VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="96a62-1944">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="96a62-1945">Introducera nya generationer för VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="96a62-1945">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="96a62-1946">Introducera nya SKU:er med högt dataflöde för VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="96a62-1946">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="96a62-1947">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="96a62-1947">Az.RedisCache</span></span>
* <span data-ttu-id="96a62-1948">Uppdaterad referensdokumentation för ”set-AzRedisCache” för att inkludera saknade värden för parametern ”size”</span><span class="sxs-lookup"><span data-stu-id="96a62-1948">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="96a62-1949">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="96a62-1949">Az.Sql</span></span>
* <span data-ttu-id="96a62-1950">Lägg till stöd för inställningen Active Directory administratör på den hanterade instansen</span><span class="sxs-lookup"><span data-stu-id="96a62-1950">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="96a62-1951">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="96a62-1951">Az.Storage</span></span>
* <span data-ttu-id="96a62-1952">Uppdatera Lagringsklientbibliotek till 11.1.0</span><span class="sxs-lookup"><span data-stu-id="96a62-1952">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="96a62-1953">Lista containrar med hanteringsplans-API, kommer att listas med NextPageLink</span><span class="sxs-lookup"><span data-stu-id="96a62-1953">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="96a62-1954">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="96a62-1954">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="96a62-1955">Lista lagringskonton från prenumerationen, kommer att listas med NextPageLink</span><span class="sxs-lookup"><span data-stu-id="96a62-1955">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="96a62-1956">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="96a62-1956">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="96a62-1957">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="96a62-1957">Az.StorageSync</span></span>
* <span data-ttu-id="96a62-1958">Åtgärda problemet 9810 i Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="96a62-1958">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="96a62-1959">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="96a62-1959">Az.Websites</span></span>
* <span data-ttu-id="96a62-1960">Set-AzWebApp – uppdatering av ASP för en app misslyckades</span><span class="sxs-lookup"><span data-stu-id="96a62-1960">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="96a62-1961">2.7.0 – september 2019</span><span class="sxs-lookup"><span data-stu-id="96a62-1961">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="96a62-1962">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="96a62-1962">Az.ApiManagement</span></span>
* <span data-ttu-id="96a62-1963">Uppdatera ”-Format”-parameterbeskrivningen i ”Set-AzApiManagementPolicy”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="96a62-1963">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="96a62-1964">Referenser för den föråldrade cmdleten ”Update-AzApiManagementDeployment” har tagits bort från referensdokumentationen.</span><span class="sxs-lookup"><span data-stu-id="96a62-1964">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="96a62-1965">Använd ”Set-AzApiManagement” i stället.</span><span class="sxs-lookup"><span data-stu-id="96a62-1965">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="96a62-1966">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="96a62-1966">Az.Automation</span></span>
* <span data-ttu-id="96a62-1967">Stavfel har korrigerats i exempel i referensdokumentationen för ”Register-AzAutomationDscNode”</span><span class="sxs-lookup"><span data-stu-id="96a62-1967">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="96a62-1968">Klargörande har lagts till om OS-begränsningar för Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="96a62-1968">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="96a62-1969">Null-referensundantag har korrigerats för -Wait-alternativet i Start-AzAutomationRunbook-cmdleten.</span><span class="sxs-lookup"><span data-stu-id="96a62-1969">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="96a62-1970">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="96a62-1970">Az.Compute</span></span>
* <span data-ttu-id="96a62-1971">Lägg till UploadSizeInBytes-parameter till New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="96a62-1971">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="96a62-1972">Lägg till Incremental-parameter till New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="96a62-1972">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="96a62-1973">Lägg till en funktion för virtuella datorer med låg prioritet:</span><span class="sxs-lookup"><span data-stu-id="96a62-1973">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="96a62-1974">MaxPrice-, EvictionPolicy- och Priority-parametrar har lagts till i New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="96a62-1974">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="96a62-1975">MaxPrice-parametern har lagts till i New-AzVmssConfig-, Update-AzVM- och Update-AzVmss-cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="96a62-1975">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="96a62-1976">Åtgärda problem med VM-referenser för Get-AzAvailabilitySet-cmdleten när alla tillgänglighetsuppsättningar i prenumerationen visas.</span><span class="sxs-lookup"><span data-stu-id="96a62-1976">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="96a62-1977">Korrigera null-undantaget för Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="96a62-1977">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="96a62-1978">Korrigera VHD-metoden för sökning relativt till slut.</span><span class="sxs-lookup"><span data-stu-id="96a62-1978">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="96a62-1979">Åtgärda UltraSSD-problem för New-AzVM och Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="96a62-1979">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="96a62-1980">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="96a62-1980">Az.DataFactory</span></span>
* <span data-ttu-id="96a62-1981">Lägger till 3 nya kommandon för ADF V2 – Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription och Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="96a62-1981">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="96a62-1982">ADF .Net SDK har uppdaterats till 4.1.3</span><span class="sxs-lookup"><span data-stu-id="96a62-1982">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="96a62-1983">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="96a62-1983">Az.HDInsight</span></span>
* <span data-ttu-id="96a62-1984">Anrop för icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="96a62-1984">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="96a62-1985">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="96a62-1985">Az.IotHub</span></span>
* <span data-ttu-id="96a62-1986">Lägg till stöd för att anropa redundans för en IotHub till den geo-länkade katastrofåterställningsregionen.</span><span class="sxs-lookup"><span data-stu-id="96a62-1986">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="96a62-1987">Lägg till stöd för att hantera meddelandeberikning för en IotHub.</span><span class="sxs-lookup"><span data-stu-id="96a62-1987">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="96a62-1988">Nya cmdlet:ar är:</span><span class="sxs-lookup"><span data-stu-id="96a62-1988">New cmdlets are:</span></span>
    - <span data-ttu-id="96a62-1989">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="96a62-1989">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="96a62-1990">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="96a62-1990">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="96a62-1991">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="96a62-1991">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="96a62-1992">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="96a62-1992">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="96a62-1993">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="96a62-1993">Az.Monitor</span></span>
* <span data-ttu-id="96a62-1994">Pekar på den senaste Monitor SDK:n, dvs. 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="96a62-1994">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="96a62-1995">Lägger till bakåtkompatibla ändringar i Metrics-cmdletarna, dvs. enhetsuppräkningen stöder flera nya värden.</span><span class="sxs-lookup"><span data-stu-id="96a62-1995">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="96a62-1996">Detta är skrivskyddade cmdletar, så det förekommer inga ändringar i inmatningen för cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="96a62-1996">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="96a62-1997">API-versionen för **ActionGroups**-begäranden är nu **2019-06-01**. Tidigare var den **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="96a62-1997">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="96a62-1998">Test av scenarier har uppdaterats för att anpassas till den här ändringen.</span><span class="sxs-lookup"><span data-stu-id="96a62-1998">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="96a62-1999">Ett nytt obligatoriskt argument har lagts till för konstruktorerna för klasserna **EmailReceiver** och **WebhookReceiver** – ett booleskt värde med namnet **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="96a62-1999">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="96a62-2000">Värdet är för närvarande fast till **false** så att den här icke-bakåtkompatibla ändringen är dold från cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="96a62-2000">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="96a62-2001">**Obs!** Det här är en tillfällig ändring som måste verifieras av Alerts-teamet.</span><span class="sxs-lookup"><span data-stu-id="96a62-2001">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="96a62-2002">Ordningen på argumenten för konstruktorn för klassen **Source** (relaterad till klassen **ScheduledQueryRuleSource**) har ändrats från den tidigare SDK:n.</span><span class="sxs-lookup"><span data-stu-id="96a62-2002">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="96a62-2003">Den här ändringen krävde korrigering av två enhetstest: de kompilerades, men testerna skickades inte.</span><span class="sxs-lookup"><span data-stu-id="96a62-2003">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="96a62-2004">Ordningen på argumenten för konstruktorn för klassen **AlertingAction** (relaterad till klassen **ScheduledQueryRuleSource**) har ändrats från den tidigare SDK:n.</span><span class="sxs-lookup"><span data-stu-id="96a62-2004">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="96a62-2005">Den här ändringen krävde korrigering av två enhetstest: de kompilerades, men testerna skickades inte.</span><span class="sxs-lookup"><span data-stu-id="96a62-2005">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="96a62-2006">Stöd för kriterier för dynamiskt tröskelvärde för måttavisering v2</span><span class="sxs-lookup"><span data-stu-id="96a62-2006">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="96a62-2007">New-AzMetricAlertRuleV2Criteria: skapar nu även kriterier för dynamiskt tröskelvärde</span><span class="sxs-lookup"><span data-stu-id="96a62-2007">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="96a62-2008">Add-AzMetricAlertRuleV2: accepterar nu även kriterier för dynamiskt tröskelvärde</span><span class="sxs-lookup"><span data-stu-id="96a62-2008">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="96a62-2009">Förbättringar i schemalagd frågeregel (SQR)</span><span class="sxs-lookup"><span data-stu-id="96a62-2009">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="96a62-2010">Cmdletar accepterar ”Location”-parameter i båda formaten, antingen platsen (t.ex. eastus) eller platsens visningsnamn (t.ex. USA, östra)</span><span class="sxs-lookup"><span data-stu-id="96a62-2010">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="96a62-2011">”Enabled”-parametern illustreras korrekt i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="96a62-2011">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="96a62-2012">Exempel för den valfria parametern ”ActionGroup” har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-2012">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="96a62-2013">Förbättrade hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="96a62-2013">Overall improved help files</span></span>
* <span data-ttu-id="96a62-2014">Åtgärda bugg då omfattningstypen fastställs för ”Set-AzActionRule”</span><span class="sxs-lookup"><span data-stu-id="96a62-2014">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="96a62-2015">Az.Network</span><span class="sxs-lookup"><span data-stu-id="96a62-2015">Az.Network</span></span>
* <span data-ttu-id="96a62-2016">Korrigera felaktigt exempel i referensdokumentationen för ”New-AzApplicationGateway”</span><span class="sxs-lookup"><span data-stu-id="96a62-2016">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="96a62-2017">Lägg till anmärkning i ”Get-AzNetworkWatcherPacketCapture”-referensdokumentationen om hämtning av alla egenskaper för en paketinsamling</span><span class="sxs-lookup"><span data-stu-id="96a62-2017">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="96a62-2018">Exempel har korrigerats i ”Test-AzNetworkWatcherIPFlow”-referensdokumentationen för korrekt uppräkning av nätverkskort</span><span class="sxs-lookup"><span data-stu-id="96a62-2018">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="96a62-2019">Förbättrad tolkning av molnundantag för att visa eventuell ytterligare information</span><span class="sxs-lookup"><span data-stu-id="96a62-2019">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="96a62-2020">Förbättrad tolkning av molnundantag för att hantera ytterligare en typ av SDK-undantag</span><span class="sxs-lookup"><span data-stu-id="96a62-2020">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="96a62-2021">Felaktig mappning av säkerhetsregelmodeller har korrigerats</span><span class="sxs-lookup"><span data-stu-id="96a62-2021">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="96a62-2022">Egenskaper har lagts till för nätverksgränssnittet för funktionen Privat IP</span><span class="sxs-lookup"><span data-stu-id="96a62-2022">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="96a62-2023">Egenskapen ”PrivateEndpoint” har lagts till som en typ av PSResourceId till PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="96a62-2023">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="96a62-2024">Egenskapen ”PrivateLinkConnectionProperties” har lagts till som en typ av PSIpConfigurationConnectivityInformation till PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="96a62-2024">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="96a62-2025">Modellklassen PSIpConfigurationConnectivityInformation har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-2025">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="96a62-2026">ApplicationRuleProtocolType ”mssql” har lagts till för Azure Firewall-resurs</span><span class="sxs-lookup"><span data-stu-id="96a62-2026">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="96a62-2027">MultiLink-stöd i virtuellt WAN</span><span class="sxs-lookup"><span data-stu-id="96a62-2027">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="96a62-2028">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="96a62-2028">New cmdlets</span></span>
        - <span data-ttu-id="96a62-2029">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="96a62-2029">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="96a62-2030">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="96a62-2030">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="96a62-2031">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="96a62-2031">Updated cmdlet:</span></span>
        - <span data-ttu-id="96a62-2032">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="96a62-2032">New-VpnSite</span></span>
        - <span data-ttu-id="96a62-2033">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="96a62-2033">Update-VpnSite</span></span>
        - <span data-ttu-id="96a62-2034">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="96a62-2034">New-VpnConnection</span></span>
        - <span data-ttu-id="96a62-2035">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="96a62-2035">Update-VpnConnection</span></span>
* <span data-ttu-id="96a62-2036">Dokument för vissa PowerShell-exempel har korrigerats så att Az-cmdletar används i stället för AzureRM-cmdletar</span><span class="sxs-lookup"><span data-stu-id="96a62-2036">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="96a62-2037">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="96a62-2037">Az.RecoveryServices</span></span>
* <span data-ttu-id="96a62-2038">Uppdatera AzureVMpolicy-objekt med ProtectedItemsCount-attribut</span><span class="sxs-lookup"><span data-stu-id="96a62-2038">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="96a62-2039">Ytterligare tester har lagts till för VM-princip och återställning av ursprungligt lagringskonto</span><span class="sxs-lookup"><span data-stu-id="96a62-2039">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="96a62-2040">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="96a62-2040">Az.Resources</span></span>
* <span data-ttu-id="96a62-2041">Åtgärda fel där det inte gick att anropa New-AzRoleAssignment utan parametern Scope.</span><span class="sxs-lookup"><span data-stu-id="96a62-2041">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="96a62-2042">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="96a62-2042">Az.ServiceFabric</span></span>
* <span data-ttu-id="96a62-2043">Stavfel har korrigerats i exempel för ”Update-AzServiceFabricReliability”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="96a62-2043">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="96a62-2044">Lägger till nya cmdletar för att hantera program och tjänster:</span><span class="sxs-lookup"><span data-stu-id="96a62-2044">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="96a62-2045">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="96a62-2045">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="96a62-2046">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="96a62-2046">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="96a62-2047">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="96a62-2047">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="96a62-2048">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="96a62-2048">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="96a62-2049">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="96a62-2049">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="96a62-2050">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="96a62-2050">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="96a62-2051">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="96a62-2051">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="96a62-2052">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="96a62-2052">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="96a62-2053">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="96a62-2053">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="96a62-2054">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="96a62-2054">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="96a62-2055">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="96a62-2055">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="96a62-2056">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="96a62-2056">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="96a62-2057">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="96a62-2057">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="96a62-2058">Service Fabric SDK har uppgraderats till version 1.2.0 som använder Service Fabric-resursprovidern med API-version 2019-03-01.</span><span class="sxs-lookup"><span data-stu-id="96a62-2058">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="96a62-2059">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="96a62-2059">Az.SignalR</span></span>
* <span data-ttu-id="96a62-2060">Lägg till Update-, Restart-, CheckNameAvailability- och GetUsage-cmdletar</span><span class="sxs-lookup"><span data-stu-id="96a62-2060">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="96a62-2061">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="96a62-2061">Az.Sql</span></span>
* <span data-ttu-id="96a62-2062">Uppdatera exempel i referensdokumentationen för ”Get-AzSqlElasticPool”</span><span class="sxs-lookup"><span data-stu-id="96a62-2062">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="96a62-2063">vCore-exempel för att skapa en elastisk pool (New-AzSqlElasticPool) har lagts till.</span><span class="sxs-lookup"><span data-stu-id="96a62-2063">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="96a62-2064">Ta bort verifieringen av EmailAddresses och kontrollen som bekräftar att EmailAdmins inte är falskt när EmailAddresses är tomt i Set-AzSqlServerAdvancedThreatProtectionPolicy och Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="96a62-2064">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="96a62-2065">Server-/databasgranskningsinställningar kan tas bort när det finns flera diagnostikinställningar som aktiverar granskningskategorin.</span><span class="sxs-lookup"><span data-stu-id="96a62-2065">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="96a62-2066">Åtgärda verifiering av e-postadresser i flera Sql Vulnerability Assessment-cmdletar (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting och Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="96a62-2066">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="96a62-2067">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="96a62-2067">Az.Storage</span></span>
* <span data-ttu-id="96a62-2068">Exempel i referensdokumentationen för ”Get-AzStorageAccountKey” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="96a62-2068">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="96a62-2069">Vid upp- och nedladdning av en Azure-fil kan SMB-egenskaperna för källfilen (t.ex. filattribut, tidpunkten då filen skapades och tidpunkten för den senaste skrivningen) sparas i målfilen</span><span class="sxs-lookup"><span data-stu-id="96a62-2069">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="96a62-2070">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="96a62-2070">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="96a62-2071">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="96a62-2071">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="96a62-2072">Korrigera problem med uppladdningen av blockblob med egenskaper/metadata för ImmutabilityPolicy i containrar.</span><span class="sxs-lookup"><span data-stu-id="96a62-2072">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="96a62-2073">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="96a62-2073">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="96a62-2074">Stöd för hantering av Azure-filresurser med API för hanteringsplan</span><span class="sxs-lookup"><span data-stu-id="96a62-2074">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="96a62-2075">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="96a62-2075">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="96a62-2076">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="96a62-2076">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="96a62-2077">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="96a62-2077">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="96a62-2078">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="96a62-2078">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="96a62-2079">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="96a62-2079">Az.Websites</span></span>
* <span data-ttu-id="96a62-2080">Åtgärdar problemet där webapp-taggar togs bort när appen migrerades till nya ASP</span><span class="sxs-lookup"><span data-stu-id="96a62-2080">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="96a62-2081">Åtgärda Publish-AzureWebapp så att det fungerar i Linux och Windows</span><span class="sxs-lookup"><span data-stu-id="96a62-2081">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="96a62-2082">Uppdatera exempel i ”Get-AzWebAppPublishingProfile”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="96a62-2082">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="96a62-2083">2.6.0 – augusti 2019</span><span class="sxs-lookup"><span data-stu-id="96a62-2083">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="96a62-2084">Allmänt</span><span class="sxs-lookup"><span data-stu-id="96a62-2084">General</span></span>
* <span data-ttu-id="96a62-2085">Åtgärdade diverse skrivfel i flera moduler</span><span class="sxs-lookup"><span data-stu-id="96a62-2085">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="96a62-2086">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="96a62-2086">Az.Accounts</span></span>
* <span data-ttu-id="96a62-2087">Stöd för användartilldelat MSI i Azure Functions-autentisering (#9479)</span><span class="sxs-lookup"><span data-stu-id="96a62-2087">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="96a62-2088">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="96a62-2088">Az.Aks</span></span>
* <span data-ttu-id="96a62-2089">Åtgärda problem med utdata för "Get-AzAks"</span><span class="sxs-lookup"><span data-stu-id="96a62-2089">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="96a62-2090">Mer information här: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="96a62-2090">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="96a62-2091">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="96a62-2091">Az.ApiManagement</span></span>
* <span data-ttu-id="96a62-2092">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="96a62-2092">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="96a62-2093">Uppdatera .net-NuGet-versionen, som inte tillämpar begränsningar för productId, apiId och userId</span><span class="sxs-lookup"><span data-stu-id="96a62-2093">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="96a62-2094">**Get-AzApiManagementProduct** – Lade till stöd för frågekörning mot produkter via API.</span><span class="sxs-lookup"><span data-stu-id="96a62-2094">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="96a62-2095">**New-AzApiManagementApiRevision** – Korrigering för problem där ApiRevisionDescription inte angavs vid skapande av ny API-revision https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="96a62-2095">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="96a62-2096">Åtgärdade skrivfel i modellen "PsApiManagementOAuth2AuthrozationServer" till "PsApiManagementOAuth2AuthorizationServer"</span><span class="sxs-lookup"><span data-stu-id="96a62-2096">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="96a62-2097">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="96a62-2097">Az.Batch</span></span>
* <span data-ttu-id="96a62-2098">Åtgärdade skrivfel i hjälpmeddelande och dokumentation till att skriva Windows med versaler</span><span class="sxs-lookup"><span data-stu-id="96a62-2098">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="96a62-2099">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="96a62-2099">Az.Cdn</span></span>
* <span data-ttu-id="96a62-2100">Åtgärdade skrivfel i CDN-modulens konverteringshjälp</span><span class="sxs-lookup"><span data-stu-id="96a62-2100">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="96a62-2101">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="96a62-2101">Az.Compute</span></span>
* <span data-ttu-id="96a62-2102">Lägg till VmssId i New-AzVMConfig-cmdleten</span><span class="sxs-lookup"><span data-stu-id="96a62-2102">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="96a62-2103">Lägg till parametrarna TerminateScheduledEvents och TerminateScheduledEventNotBeforeTimeoutInMinutes i New-AzVmssConfig och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="96a62-2103">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="96a62-2104">Lägg till egenskapen HyperVGeneration till avbildningsobjekt för virtuell dator</span><span class="sxs-lookup"><span data-stu-id="96a62-2104">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="96a62-2105">Lägg till funktioner för Host och HostGroup</span><span class="sxs-lookup"><span data-stu-id="96a62-2105">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="96a62-2106">Nya cmdletar:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="96a62-2106">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="96a62-2107">HostId-parametern läggs till i New-AzVMConfig och New-AzVM</span><span class="sxs-lookup"><span data-stu-id="96a62-2107">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="96a62-2108">Uppdatera exempel i "Invoke-AzVMRunCommand"-dokumentationen till att använda rätt parameternamn</span><span class="sxs-lookup"><span data-stu-id="96a62-2108">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="96a62-2109">Uppdatera "-VolumeType"-beskrivningen i referensdokumentationen för "set-AzVMDiskEncryptionExtension" och "set-AzVmssDiskEncryptionExtension"</span><span class="sxs-lookup"><span data-stu-id="96a62-2109">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="96a62-2110">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="96a62-2110">Az.DataFactory</span></span>
* <span data-ttu-id="96a62-2111">Åtgärda skrivfel till att använda versaler för "Windows" i "New-AzDataFactoryEncryptValue"-dokumentationen</span><span class="sxs-lookup"><span data-stu-id="96a62-2111">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="96a62-2112">Uppdaterade ADF .Net SDK-versionen till 4.1.2</span><span class="sxs-lookup"><span data-stu-id="96a62-2112">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="96a62-2113">Lägg till parametrarna "DataProxyIntegrationRuntimeName", "DataProxyStagingLinkedServiceName" och "DataProxyStagingPath" för "Set-AzureRmDataFactoryV2IntegrationRuntime"-cmd för att aktivera konfiguration av lokalt installerad integrationskörning som en proxy för SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="96a62-2113">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="96a62-2114">Uppdaterade PSTriggerRun till att visa utlöst pipeline, meddelande och egenskaper samt PSActivityRun till att visa aktivitetstypen</span><span class="sxs-lookup"><span data-stu-id="96a62-2114">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="96a62-2115">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="96a62-2115">Az.DataLakeStore</span></span>
* <span data-ttu-id="96a62-2116">Korrigering av frysning av Get-DataLakeStoreDeletedItem för fel eller fjärrundantag.</span><span class="sxs-lookup"><span data-stu-id="96a62-2116">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="96a62-2117">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="96a62-2117">Az.EventHub</span></span>
* <span data-ttu-id="96a62-2118">Korrigering av problem #9658 : Skrivfel i parametern VirtualNteworkRule i Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="96a62-2118">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="96a62-2119">Korrigering av problem #9558 : Set-AzEventHubNamespace använder PATCH i stället för PUT</span><span class="sxs-lookup"><span data-stu-id="96a62-2119">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="96a62-2120">lade till parametern EnableKafka i Set-AzEventHubNamespace-cmdleten</span><span class="sxs-lookup"><span data-stu-id="96a62-2120">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="96a62-2121">Korrigering av problem #9786 : kan inte skapa en regel med Endast lyssna-behörighet</span><span class="sxs-lookup"><span data-stu-id="96a62-2121">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="96a62-2122">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="96a62-2122">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="96a62-2123">Åtgärdade skrivfel i dokumentation där "Azure" skrevs helt med gemener</span><span class="sxs-lookup"><span data-stu-id="96a62-2123">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="96a62-2124">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="96a62-2124">Az.Monitor</span></span>
* <span data-ttu-id="96a62-2125">Åtgärdade felaktigt parameternamn i hjälpdokumentationen</span><span class="sxs-lookup"><span data-stu-id="96a62-2125">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="96a62-2126">Az.Network</span><span class="sxs-lookup"><span data-stu-id="96a62-2126">Az.Network</span></span>
* <span data-ttu-id="96a62-2127">Uppdaterade New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="96a62-2127">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="96a62-2128">Gjorde parametern "PublicIpAddress" inaktuell eftersom den aldrig används på serversidan.</span><span class="sxs-lookup"><span data-stu-id="96a62-2128">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="96a62-2129">Lade till den valfria parametern "Primary", som anger huruvida den aktuella IP-konfigurationen är den primära.</span><span class="sxs-lookup"><span data-stu-id="96a62-2129">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="96a62-2130">Förbättrade hanteringen av felundantag för begärande från SDK – åtgärdar problemet att tidigare SDK-undantag inte hanteras på rätt sätt, vilket leder till att viktig felinformation inte visas</span><span class="sxs-lookup"><span data-stu-id="96a62-2130">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="96a62-2131">Justerade valideringslogiken för IPv6-IP-prefix till att kontrollera korrekt IPv6-prefixlängd.</span><span class="sxs-lookup"><span data-stu-id="96a62-2131">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="96a62-2132">Uppdaterade Get-AzVirtualNetworkSubnetConfig: Lade till parameter som anges till get av undernätets resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="96a62-2132">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="96a62-2133">Uppdaterade beskrivningen av parametern Location för AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="96a62-2133">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="96a62-2134">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="96a62-2134">Az.OperationalInsights</span></span>
* <span data-ttu-id="96a62-2135">Uppdaterade dokumentation för "New-AzOperationalInsightsLinuxSyslogDataSource"</span><span class="sxs-lookup"><span data-stu-id="96a62-2135">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="96a62-2136">Lade till exempel</span><span class="sxs-lookup"><span data-stu-id="96a62-2136">Added example</span></span>
    - <span data-ttu-id="96a62-2137">Uppdaterade beskrivningen av parametern "-Name"</span><span class="sxs-lookup"><span data-stu-id="96a62-2137">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="96a62-2138">Lade till ett exempel för New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="96a62-2138">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="96a62-2139">Ändrade beskrivningen av parametern -Name för New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="96a62-2139">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="96a62-2140">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="96a62-2140">Az.RecoveryServices</span></span>
* <span data-ttu-id="96a62-2141">Uppdatera "Get-AzRecoveryServicesBackupJobDetail.md"</span><span class="sxs-lookup"><span data-stu-id="96a62-2141">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="96a62-2142">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="96a62-2142">Az.Resources</span></span>
* <span data-ttu-id="96a62-2143">Lägg till stöd för den nya API-versionen från 2019-05-10 för Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="96a62-2143">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="96a62-2144">Lägg till stöd för "copy.count = 0" för variabler, resurser och egenskaper</span><span class="sxs-lookup"><span data-stu-id="96a62-2144">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="96a62-2145">Resurser med "condition = false" eller "copy.count = 0" tas bort i complete-läget</span><span class="sxs-lookup"><span data-stu-id="96a62-2145">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="96a62-2146">Lägg till ett exempel på tilldelning av princip på prenumerationsnivå i hjälpdokumentationen</span><span class="sxs-lookup"><span data-stu-id="96a62-2146">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="96a62-2147">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="96a62-2147">Az.ServiceBus</span></span>
* <span data-ttu-id="96a62-2148">Korrigering av problem #9658 : Skrivfel i parametern VirtualNetworkRule i set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="96a62-2148">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="96a62-2149">Korrigering av problem #9786 : kan inte skapa en regel med Endast lyssna-behörighet</span><span class="sxs-lookup"><span data-stu-id="96a62-2149">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="96a62-2150">Lade till det nya kommandot "Test-AzServiceBusNameAvailability" för att kontrollera namntillgängligheten för kö och ämne</span><span class="sxs-lookup"><span data-stu-id="96a62-2150">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="96a62-2151">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="96a62-2151">Az.ServiceFabric</span></span>
* <span data-ttu-id="96a62-2152">Åtgärda buggar med tillägg av nodtyps-cmdlet:</span><span class="sxs-lookup"><span data-stu-id="96a62-2152">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="96a62-2153">NullReferenceException-bugg när resursgrupp hade annan vmss som inte är relaterad till Service Fabric-klustret.</span><span class="sxs-lookup"><span data-stu-id="96a62-2153">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="96a62-2154">Åtgärdar problemet: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="96a62-2154">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="96a62-2155">Åtgärda bugg där cmdleten misslyckades om virtualNetwork var i en annan resursgrupp än klustret.</span><span class="sxs-lookup"><span data-stu-id="96a62-2155">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="96a62-2156">Åtgärdar problemet: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="96a62-2156">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="96a62-2157">AzServiceFabricApplicationCertificate-cmdleten görs inaktuell</span><span class="sxs-lookup"><span data-stu-id="96a62-2157">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="96a62-2158">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="96a62-2158">Az.Sql</span></span>
* <span data-ttu-id="96a62-2159">Uppdatera dokumentation om gamla gransknings-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="96a62-2159">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="96a62-2160">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="96a62-2160">Az.Storage</span></span>
* <span data-ttu-id="96a62-2161">Uppdatera hjälpen för Get/Close-AzStorageFileHandle genom att lägga till fler scenarier i cmdlet-exempel och uppdatera parameterbeskrivningar</span><span class="sxs-lookup"><span data-stu-id="96a62-2161">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="96a62-2162">Stöd för StandardBlobTier i uppladdningsblob och kopieringsblob</span><span class="sxs-lookup"><span data-stu-id="96a62-2162">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="96a62-2163">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="96a62-2163">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="96a62-2164">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="96a62-2164">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="96a62-2165">Stöd för rehydratiseringsprioritet i kopieringsblob</span><span class="sxs-lookup"><span data-stu-id="96a62-2165">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="96a62-2166">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="96a62-2166">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="96a62-2167">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="96a62-2167">Az.Websites</span></span>
* <span data-ttu-id="96a62-2168">Lägg till klargöranden gällande parametern -AppSettings i Set-AzWebApp och Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="96a62-2168">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="96a62-2169">2.5.0 – July 2019</span><span class="sxs-lookup"><span data-stu-id="96a62-2169">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="96a62-2170">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="96a62-2170">Az.Accounts</span></span>
* <span data-ttu-id="96a62-2171">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="96a62-2171">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="96a62-2172">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="96a62-2172">Az.ApplicationInsights</span></span>
* <span data-ttu-id="96a62-2173">Korrigera skrivfel i exempel i dokumentationen för Remove-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="96a62-2173">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="96a62-2174">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="96a62-2174">Az.Automation</span></span>
* <span data-ttu-id="96a62-2175">Korrigera skrivfel i resurssträng</span><span class="sxs-lookup"><span data-stu-id="96a62-2175">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="96a62-2176">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="96a62-2176">Az.CognitiveServices</span></span>
* <span data-ttu-id="96a62-2177">Stöd för NetworkRuleSet har lagts till.</span><span class="sxs-lookup"><span data-stu-id="96a62-2177">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="96a62-2178">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="96a62-2178">Az.Compute</span></span>
* <span data-ttu-id="96a62-2179">Lägg till saknade egenskaper (ComputerName, OsName, OsVersion och HyperVGeneration) för visningsobjekt i den virtuella datorinstansen.</span><span class="sxs-lookup"><span data-stu-id="96a62-2179">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="96a62-2180">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="96a62-2180">Az.ContainerRegistry</span></span>
* <span data-ttu-id="96a62-2181">Åtgärda skrivfel i Remove-AzContainerRegistryReplication för parametern Replication</span><span class="sxs-lookup"><span data-stu-id="96a62-2181">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="96a62-2182">Mer information finns här: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="96a62-2182">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="96a62-2183">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="96a62-2183">Az.DataFactory</span></span>
* <span data-ttu-id="96a62-2184">ADF .Net SDK-versionen har uppdaterats till 4.1.0</span><span class="sxs-lookup"><span data-stu-id="96a62-2184">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="96a62-2185">Korrigera skrivfel i dokumentationen för Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="96a62-2185">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="96a62-2186">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="96a62-2186">Az.EventHub</span></span>
* <span data-ttu-id="96a62-2187">Ny cmmdlet har lagts till för att skapa SAS-token: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="96a62-2187">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="96a62-2188">verifierings- och felmeddelande har lagts till för authorizationrules-rättigheter om endast "hantera" har tilldelats</span><span class="sxs-lookup"><span data-stu-id="96a62-2188">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="96a62-2189">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="96a62-2189">Az.KeyVault</span></span>
* <span data-ttu-id="96a62-2190">Stöd har lagts till för att ange KeySize för certifikatprinciper</span><span class="sxs-lookup"><span data-stu-id="96a62-2190">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="96a62-2191">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="96a62-2191">Az.LogicApp</span></span>
* <span data-ttu-id="96a62-2192">Korrigering för Get-AzIntegrationAccountMap för att lista alla mappningstyper</span><span class="sxs-lookup"><span data-stu-id="96a62-2192">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="96a62-2193">Ny MapType-parameter har lagts till för filtrering</span><span class="sxs-lookup"><span data-stu-id="96a62-2193">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="96a62-2194">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="96a62-2194">Az.ManagedServices</span></span>
* <span data-ttu-id="96a62-2195">Stöd för API-versionen 2019-06-01 (GA) har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-2195">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="96a62-2196">Az.Network</span><span class="sxs-lookup"><span data-stu-id="96a62-2196">Az.Network</span></span>
* <span data-ttu-id="96a62-2197">Lägg till stöd för privat slutpunkt och privat länktjänst</span><span class="sxs-lookup"><span data-stu-id="96a62-2197">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="96a62-2198">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="96a62-2198">New cmdlets</span></span>
        - <span data-ttu-id="96a62-2199">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="96a62-2199">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="96a62-2200">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="96a62-2200">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="96a62-2201">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="96a62-2201">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="96a62-2202">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="96a62-2202">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="96a62-2203">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="96a62-2203">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="96a62-2204">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="96a62-2204">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="96a62-2205">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="96a62-2205">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="96a62-2206">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="96a62-2206">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="96a62-2207">Nedanstående kommandon för funktionen har uppdaterats: Flaggan PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies på undernätet i VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="96a62-2207">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="96a62-2208">Uppdaterade New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="96a62-2208">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="96a62-2209">Valfri parameter har lagts till – PrivateEndpointNetworkPoliciesFlag som konfigurerar huruvida nätverksprinciper ska tillämpas på en privat slutpunkt i det här undernätet.</span><span class="sxs-lookup"><span data-stu-id="96a62-2209">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="96a62-2210">Valfri parameter har lagts till – PrivateLinkServiceNetworkPoliciesFlag som konfigurerar huruvida nätverksprinciper ska tillämpas på en privat länktjänst i det här undernätet.</span><span class="sxs-lookup"><span data-stu-id="96a62-2210">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="96a62-2211">AzPrivateLinkService för cmdlet-parametern ServiceName har bytt namn till Name med aliaset ServiceName för bakåtkompatibilitet</span><span class="sxs-lookup"><span data-stu-id="96a62-2211">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="96a62-2212">Aktivera ICMP-protokoll för konfiguration av nätverkssäkerhetsregler</span><span class="sxs-lookup"><span data-stu-id="96a62-2212">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="96a62-2213">Uppdaterade cmdletar</span><span class="sxs-lookup"><span data-stu-id="96a62-2213">Updated cmdlets</span></span>
        - <span data-ttu-id="96a62-2214">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="96a62-2214">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="96a62-2215">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="96a62-2215">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="96a62-2216">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="96a62-2216">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="96a62-2217">Lägg till ConnectionProtocolType (Ikev1/Ikev2) som en konfigurerbar parameter för New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="96a62-2217">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="96a62-2218">Lägg till PrivateIpAddressVersion i LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="96a62-2218">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="96a62-2219">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="96a62-2219">Updated cmdlet:</span></span>
        - <span data-ttu-id="96a62-2220">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="96a62-2220">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="96a62-2221">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="96a62-2221">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="96a62-2222">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="96a62-2222">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="96a62-2223">Uppdatering av Application Gateway-kommandot New-AzApplicationGatewayProbeConfig för stöd av anpassad port i Probe</span><span class="sxs-lookup"><span data-stu-id="96a62-2223">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="96a62-2224">Uppdaterade New-AzApplicationGatewayProbeConfig: Den valfria parametern Port som används för avsökning i serverdelen har lagts till.</span><span class="sxs-lookup"><span data-stu-id="96a62-2224">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="96a62-2225">Denna parameter gäller för SKU:erna Standard_V2 och WAF_V2.</span><span class="sxs-lookup"><span data-stu-id="96a62-2225">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="96a62-2226">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="96a62-2226">Az.OperationalInsights</span></span>
* <span data-ttu-id="96a62-2227">Uppdaterade standardversionen för sparade sökningar till 1.</span><span class="sxs-lookup"><span data-stu-id="96a62-2227">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="96a62-2228">Åtgärdade hantering av anpassad log null regex</span><span class="sxs-lookup"><span data-stu-id="96a62-2228">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="96a62-2229">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="96a62-2229">Az.RecoveryServices</span></span>
* <span data-ttu-id="96a62-2230">Uppdatera Get-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="96a62-2230">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="96a62-2231">Uppdatera Get-AzRecoveryServicesBackupContainer.md</span><span class="sxs-lookup"><span data-stu-id="96a62-2231">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="96a62-2232">Uppdatera Get-AzRecoveryServicesVault.md</span><span class="sxs-lookup"><span data-stu-id="96a62-2232">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="96a62-2233">Uppdatera Wait-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="96a62-2233">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="96a62-2234">Uppdatera Set-AzRecoveryServicesVaultContext.md</span><span class="sxs-lookup"><span data-stu-id="96a62-2234">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="96a62-2235">Uppdatera Get-AzRecoveryServicesBackupItem.md</span><span class="sxs-lookup"><span data-stu-id="96a62-2235">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="96a62-2236">Uppdatera Get-AzRecoveryServicesBackupRecoveryPoint.md</span><span class="sxs-lookup"><span data-stu-id="96a62-2236">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="96a62-2237">Uppdatera Restore-AzRecoveryServicesBackupItem.md</span><span class="sxs-lookup"><span data-stu-id="96a62-2237">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="96a62-2238">Uppdaterat tjänstanrop för avregistrering av container för Azure-filresurs</span><span class="sxs-lookup"><span data-stu-id="96a62-2238">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="96a62-2239">Uppdatera Set-AzRecoveryServicesAsrAlertSetting.md</span><span class="sxs-lookup"><span data-stu-id="96a62-2239">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="96a62-2240">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="96a62-2240">Az.Resources</span></span>
- <span data-ttu-id="96a62-2241">Ta bort den cmdlet som saknas och som refereras i dokumentationen till New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="96a62-2241">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="96a62-2242">Princip-cmdletar har uppdaterats så att de använder den nya API-versionen 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="96a62-2242">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="96a62-2243">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="96a62-2243">Az.ServiceBus</span></span>
* <span data-ttu-id="96a62-2244">Ny cmmdlet har lagts till för att skapa SAS-token: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="96a62-2244">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="96a62-2245">verifierings- och felmeddelande har lagts till för authorizationrules-rättigheter om endast "hantera" har tilldelats</span><span class="sxs-lookup"><span data-stu-id="96a62-2245">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="96a62-2246">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="96a62-2246">Az.Sql</span></span>
* <span data-ttu-id="96a62-2247">Åtgärda saknade exempel för Set-AzSqlDatabaseSecondary cmdlet</span><span class="sxs-lookup"><span data-stu-id="96a62-2247">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="96a62-2248">Åtgärda angivna återkommande genomsökningar för bedömning av säkerhetsrisk utan angivna e-postadresser</span><span class="sxs-lookup"><span data-stu-id="96a62-2248">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="96a62-2249">Korrigera ett skrivfel i ett varningsmeddelande.</span><span class="sxs-lookup"><span data-stu-id="96a62-2249">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="96a62-2250">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="96a62-2250">Az.Storage</span></span>
* <span data-ttu-id="96a62-2251">Uppdatera exempel i referensdokumentationen för Get-AzStorageAccount så att rätt parameternamn används</span><span class="sxs-lookup"><span data-stu-id="96a62-2251">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="96a62-2252">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="96a62-2252">Az.StorageSync</span></span>
* <span data-ttu-id="96a62-2253">Lägger till cmdleten Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="96a62-2253">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="96a62-2254">Åtgärda problem 9551 så att TierFilesOlderThanDays föredras</span><span class="sxs-lookup"><span data-stu-id="96a62-2254">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="96a62-2255">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="96a62-2255">Az.Websites</span></span>
* <span data-ttu-id="96a62-2256">Åtgärdar ett fel där vissa SiteConfig-egenskaper inte returnerades av Get-AzWebApp och Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="96a62-2256">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="96a62-2257">Lägger till en ny platsparameter för Get-AzDeletedWebApp och Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="96a62-2257">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="96a62-2258">Åtgärdar ett fel i kloning av webbapp-platser som använder New-AzWebApp-IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="96a62-2258">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="96a62-2259">2.4.0 – juli 2019</span><span class="sxs-lookup"><span data-stu-id="96a62-2259">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="96a62-2260">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="96a62-2260">Az.Accounts</span></span>
* <span data-ttu-id="96a62-2261">Lägg till stöd för profil-cmdletar</span><span class="sxs-lookup"><span data-stu-id="96a62-2261">Add support for profile cmdlets</span></span>
* <span data-ttu-id="96a62-2262">Lägg till stöd för miljöer och dataplaner i genererade cmdletar</span><span class="sxs-lookup"><span data-stu-id="96a62-2262">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="96a62-2263">Åtgärda bugg där fel slutpunkt i vissa fall användes för cmdletar för dataplaner i Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="96a62-2263">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="96a62-2264">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="96a62-2264">Az.Advisor</span></span>
* <span data-ttu-id="96a62-2265">GA-version av Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="96a62-2265">GA release of Az.Advisor</span></span>
* <span data-ttu-id="96a62-2266">Den här modulen ingår nu som en del av `Az`-sammanslagningsmodulen</span><span class="sxs-lookup"><span data-stu-id="96a62-2266">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="96a62-2267">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="96a62-2267">Az.ApiManagement</span></span>
* <span data-ttu-id="96a62-2268">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="96a62-2268">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="96a62-2269">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="96a62-2269">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="96a62-2270">Stöd för att fråga prenumerationer efter användare och produkt har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-2270">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="96a62-2271">Stöd för att fråga med hjälp av omfång ”/”, ”/apis”, ”/apis/echo-api” har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-2271">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="96a62-2272">Korrigering av problem https://github.com/Azure/azure-powershell/issues/9307 och https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="96a62-2272">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="96a62-2273">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="96a62-2273">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="96a62-2274">Stöd för att ange ”ApiVersion” och ”ApiVersionSetId” när API:er importeras har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-2274">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="96a62-2275">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="96a62-2275">Az.Automation</span></span>
* <span data-ttu-id="96a62-2276">Bugg med cmdleten Set-AzAutomationConnectionFieldValue för att hantera strängvärde har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="96a62-2276">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="96a62-2277">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="96a62-2277">Az.Compute</span></span>
* <span data-ttu-id="96a62-2278">Lägg till parametern HyperVGeneration i New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="96a62-2278">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="96a62-2279">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="96a62-2279">Az.DataFactory</span></span>
* <span data-ttu-id="96a62-2280">Uppdaterar utdata från ADF-cmdletar som hämtar aktivitetskörningar, hämtar pipelinekörningar och hämtar utlösarkörningar för stöd för Select-Object-pipe.</span><span class="sxs-lookup"><span data-stu-id="96a62-2280">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="96a62-2281">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="96a62-2281">Az.EventGrid</span></span>
* <span data-ttu-id="96a62-2282">Korrigera stavfel i dokumentation om ”New-AzEventGridSubscription”</span><span class="sxs-lookup"><span data-stu-id="96a62-2282">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="96a62-2283">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="96a62-2283">Az.IotHub</span></span>
* <span data-ttu-id="96a62-2284">Lägg till stöd för att återskapa principnycklar för auktorisering.</span><span class="sxs-lookup"><span data-stu-id="96a62-2284">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="96a62-2285">Az.Network</span><span class="sxs-lookup"><span data-stu-id="96a62-2285">Az.Network</span></span>
* <span data-ttu-id="96a62-2286">”RoutingPreference” har lagts till i offentliga IP-taggar</span><span class="sxs-lookup"><span data-stu-id="96a62-2286">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="96a62-2287">Förbättra exempel för referensdokumentation om ”Get-AzNetworkServiceTag”</span><span class="sxs-lookup"><span data-stu-id="96a62-2287">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="96a62-2288">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="96a62-2288">Az.PolicyInsights</span></span>
* <span data-ttu-id="96a62-2289">Åtgärda problem med null-referens i Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="96a62-2289">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="96a62-2290">Mer information här: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="96a62-2290">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="96a62-2291">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="96a62-2291">Az.OperationalInsights</span></span>
* <span data-ttu-id="96a62-2292">Modellen för CustomLog-datakälla som returneras i Get-AzOperationalInsightsDataSource har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="96a62-2292">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="96a62-2293">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="96a62-2293">Az.RecoveryServices</span></span>
* <span data-ttu-id="96a62-2294">Kommandot get-policy för IaaSVM:er har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="96a62-2294">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="96a62-2295">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="96a62-2295">Az.Resources</span></span>
    - <span data-ttu-id="96a62-2296">Korrigera hjälptext för den översta parametern i Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="96a62-2296">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="96a62-2297">Lägg till växlingsstöd på klientsidan för Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="96a62-2297">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="96a62-2298">Lägg till nya parametrar för Set-AzPolicyAssignment, -PolicyParameters och -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="96a62-2298">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="96a62-2299">En mängd dokument- och exempeluppdateringar för Policy-cmdletar</span><span class="sxs-lookup"><span data-stu-id="96a62-2299">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="96a62-2300">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="96a62-2300">Az.ServiceBus</span></span>
* <span data-ttu-id="96a62-2301">Korrigering av problem #4938 – New-AzureRmServiceBusQueue returnerar BadRequest vid konfiguration av MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="96a62-2301">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="96a62-2302">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="96a62-2302">Az.Sql</span></span>
* <span data-ttu-id="96a62-2303">Lägg till cmdletar för instansredundansgrupper från förhandsversion till offentlig version</span><span class="sxs-lookup"><span data-stu-id="96a62-2303">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="96a62-2304">Stöd för granskning för Azure SQL Server\Database med nya cmdletar.</span><span class="sxs-lookup"><span data-stu-id="96a62-2304">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="96a62-2305">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="96a62-2305">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="96a62-2306">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="96a62-2306">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="96a62-2307">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="96a62-2307">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="96a62-2308">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="96a62-2308">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="96a62-2309">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="96a62-2309">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="96a62-2310">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="96a62-2310">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="96a62-2311">Ta bort begränsningar för e-post från inställningarna för sårbarhetsbedömning</span><span class="sxs-lookup"><span data-stu-id="96a62-2311">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="96a62-2312">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="96a62-2312">Az.Storage</span></span>
* <span data-ttu-id="96a62-2313">Ändra två parametrar ”-IndexDocument” och ”-ErrorDocument404Path” från ”krävs” till ”valfri” i cmdlet:</span><span class="sxs-lookup"><span data-stu-id="96a62-2313">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="96a62-2314">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="96a62-2314">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="96a62-2315">Uppdatera hjälpen för Get-AzStorageBlobContent genom att lägga till ett exempel</span><span class="sxs-lookup"><span data-stu-id="96a62-2315">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="96a62-2316">Visa mer felinformation när cmdleten misslyckas med StorageException</span><span class="sxs-lookup"><span data-stu-id="96a62-2316">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="96a62-2317">Stöd för att skapa eller uppdatera lagringskonto med Azure Files AAD DS-autentisering</span><span class="sxs-lookup"><span data-stu-id="96a62-2317">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="96a62-2318">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="96a62-2318">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="96a62-2319">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="96a62-2319">Set-AzStorageAccount</span></span>
* <span data-ttu-id="96a62-2320">Stöd för att lista eller stänga filreferenser för en filresurs, filkatalog eller en fil</span><span class="sxs-lookup"><span data-stu-id="96a62-2320">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="96a62-2321">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="96a62-2321">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="96a62-2322">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="96a62-2322">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="96a62-2323">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="96a62-2323">Az.StorageSync</span></span>
* <span data-ttu-id="96a62-2324">Den här modulen ingår nu som en del av `Az`-sammanslagningsmodulen</span><span class="sxs-lookup"><span data-stu-id="96a62-2324">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="96a62-2325">2.3.2 – juni 2019</span><span class="sxs-lookup"><span data-stu-id="96a62-2325">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="96a62-2326">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="96a62-2326">Az.Accounts</span></span>
* <span data-ttu-id="96a62-2327">Åtgärda bugg med felaktiga webbadresser som i vissa fall användes för Functions-anrop</span><span class="sxs-lookup"><span data-stu-id="96a62-2327">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="96a62-2328">Mer information här: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="96a62-2328">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="96a62-2329">Åtgärda problem med alias från AzureRM i Az-cmdletar</span><span class="sxs-lookup"><span data-stu-id="96a62-2329">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="96a62-2330">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="96a62-2330">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="96a62-2331">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="96a62-2331">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="96a62-2332">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="96a62-2332">Az.Compute</span></span>
* <span data-ttu-id="96a62-2333">Parameteruppsättningarna New-AzVm och New-AzVmss accepterar nu parametern ”ProximityPlacementGroup”.</span><span class="sxs-lookup"><span data-stu-id="96a62-2333">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="96a62-2334">Stavfel i referensdokumentationen för ”New-AzVM” har korrigerats</span><span class="sxs-lookup"><span data-stu-id="96a62-2334">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="96a62-2335">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="96a62-2335">Az.Dns</span></span>
* <span data-ttu-id="96a62-2336">Stavfel i hjälpexempel för ”Set-AzDnsZone” har korrigerats.</span><span class="sxs-lookup"><span data-stu-id="96a62-2336">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="96a62-2337">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="96a62-2337">Az.EventGrid</span></span>
* <span data-ttu-id="96a62-2338">Har uppdaterats för att använda API-versionen 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="96a62-2338">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="96a62-2339">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="96a62-2339">New cmdlets:</span></span>
    - <span data-ttu-id="96a62-2340">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="96a62-2340">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="96a62-2341">Skapar en ny Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="96a62-2341">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="96a62-2342">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="96a62-2342">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="96a62-2343">Hämtar information om en Event Grid-domän eller hämtar en lista med alla Event Grid-domäner i den aktuella Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="96a62-2343">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="96a62-2344">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="96a62-2344">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="96a62-2345">Tar bort en Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="96a62-2345">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="96a62-2346">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="96a62-2346">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="96a62-2347">Återskapar nyckeln för delad åtkomst för en Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="96a62-2347">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="96a62-2348">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="96a62-2348">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="96a62-2349">Hämtar de nycklar för delad åtkomst som används för att publicera händelser till en Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="96a62-2349">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="96a62-2350">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="96a62-2350">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="96a62-2351">Skapar ett nytt Azure Event Grid-domänämne.</span><span class="sxs-lookup"><span data-stu-id="96a62-2351">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="96a62-2352">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="96a62-2352">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="96a62-2353">Hämtar information om ett Event Grid-domänämne eller hämtar en lista med alla Event Grid-domänämnen under en specifik Event Grid-domän i nuvarande Azure</span><span class="sxs-lookup"><span data-stu-id="96a62-2353">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="96a62-2354">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="96a62-2354">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="96a62-2355">Tar bort ett befintligt Azure Event Grid-domänämne.</span><span class="sxs-lookup"><span data-stu-id="96a62-2355">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="96a62-2356">Uppdaterade cmdletar:</span><span class="sxs-lookup"><span data-stu-id="96a62-2356">Updated cmdlets:</span></span>
    - <span data-ttu-id="96a62-2357">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="96a62-2357">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="96a62-2358">Lägg till nya obligatoriska parametrar för att stödja piping för den nya Event Grid-domänen och Event Grid-domänämnet för att göra det möjligt att skapa nya händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="96a62-2358">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="96a62-2359">Lägg till nya obligatoriska parametrar för att ange det nya Event Grid-domännamnet och/eller namnet på Event Grid-domänämnet för att göra det möjligt att skapa nya händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="96a62-2359">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="96a62-2360">Lägg till ny parameteruppsättningar för domäner och domänämnen för att göra det möjligt att återanvända befintliga parametrar (t.ex. EndPointType, SubjectBeginsWith osv).</span><span class="sxs-lookup"><span data-stu-id="96a62-2360">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="96a62-2361">Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="96a62-2361">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="96a62-2362">Förfallodatum för händelseprenumeration</span><span class="sxs-lookup"><span data-stu-id="96a62-2362">Event subscription expiration date,</span></span>
            - <span data-ttu-id="96a62-2363">Avancerade filterparametrar.</span><span class="sxs-lookup"><span data-stu-id="96a62-2363">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="96a62-2364">Lägg till ny uppräkning för servicebusqueue som mål.</span><span class="sxs-lookup"><span data-stu-id="96a62-2364">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="96a62-2365">Tillåt inte användning av ”Alla” i alternativet -IncludedEventType och ersätt det med</span><span class="sxs-lookup"><span data-stu-id="96a62-2365">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="96a62-2366">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="96a62-2366">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="96a62-2367">Lägg till ny valfria parametrar (Top, ODataQuery och NextLink) för att stödja sidnumrering och filtrering av resultat.</span><span class="sxs-lookup"><span data-stu-id="96a62-2367">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="96a62-2368">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="96a62-2368">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="96a62-2369">Lägg till nya obligatoriska parametrar för att stödja piping för en Event Grid-domän och Event Grid-domänämnen för att göra det möjligt att ta bort befintliga händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="96a62-2369">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="96a62-2370">Lägg till nya obligatoriska parametrar för att ange Event Grid-domännamnet och/eller namnet på Event Grid-domänämnet för att göra det möjligt att ta bort befintliga händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="96a62-2370">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="96a62-2371">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="96a62-2371">Az.FrontDoor</span></span>
* <span data-ttu-id="96a62-2372">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="96a62-2372">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="96a62-2373">Lägg till stöd för transformeringar och nytt värde för automatisk komplettering för operatorer (RegEx)</span><span class="sxs-lookup"><span data-stu-id="96a62-2373">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="96a62-2374">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="96a62-2374">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="96a62-2375">Lägg till nya värden för automatisk komplettering</span><span class="sxs-lookup"><span data-stu-id="96a62-2375">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="96a62-2376">Az.Network</span><span class="sxs-lookup"><span data-stu-id="96a62-2376">Az.Network</span></span>
* <span data-ttu-id="96a62-2377">Lägg till stöd för resurs för virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="96a62-2377">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="96a62-2378">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="96a62-2378">New cmdlets</span></span>
        - <span data-ttu-id="96a62-2379">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="96a62-2379">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="96a62-2380">Lägg till AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="96a62-2380">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="96a62-2381">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="96a62-2381">New cmdlets</span></span>
        - <span data-ttu-id="96a62-2382">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="96a62-2382">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="96a62-2383">Lägg till PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="96a62-2383">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="96a62-2384">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="96a62-2384">New cmdlets</span></span>
        - <span data-ttu-id="96a62-2385">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="96a62-2385">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="96a62-2386">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="96a62-2386">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="96a62-2387">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="96a62-2387">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="96a62-2388">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="96a62-2388">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="96a62-2389">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="96a62-2389">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="96a62-2390">Lägg till PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="96a62-2390">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="96a62-2391">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="96a62-2391">New cmdlets</span></span>
        - <span data-ttu-id="96a62-2392">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="96a62-2392">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="96a62-2393">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="96a62-2393">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="96a62-2394">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="96a62-2394">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="96a62-2395">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="96a62-2395">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="96a62-2396">Nedanstående kommandon för funktionen har uppdaterats: Flaggan UseLocalAzureIpAddress på VpnConnection</span><span class="sxs-lookup"><span data-stu-id="96a62-2396">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="96a62-2397">New-AzVpnConnection har uppdaterats: Den valfria parametern -UseLocalAzureIpAddress har lagts till för att visa att en lokal IP-adress i Azure ska användas som källadress när anslutningen initieras.</span><span class="sxs-lookup"><span data-stu-id="96a62-2397">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="96a62-2398">Set-AzVpnConnection har uppdaterats: Den valfria parametern -UseLocalAzureIpAddress har lagts till för att visa att en lokal IP-adress i Azure ska användas som källadress när anslutningen initieras.</span><span class="sxs-lookup"><span data-stu-id="96a62-2398">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="96a62-2399">Det skrivskyddade fältet PeeredConnections har lagts till i ExpressRoute-peering.</span><span class="sxs-lookup"><span data-stu-id="96a62-2399">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="96a62-2400">Det skrivskyddade fältet GlobalReachEnabled har lagts till i ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="96a62-2400">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="96a62-2401">Ett attribut för icke-bakåtkompatibla ändringar har lagts till för att lyfta fram utfasning av fältet AllowGlobalReach i modellen ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="96a62-2401">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="96a62-2402">Problem 8756 har åtgärdats: Fel vid användning av TargetListenerID med AzApplicationGatewayRedirectConfiguration-cmdletar</span><span class="sxs-lookup"><span data-stu-id="96a62-2402">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="96a62-2403">En bugg i New-AzApplicationGatewayPathRuleConfig som gjorde att regeluppsättningen för att återskapa inte kunde anges har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="96a62-2403">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="96a62-2404">Visningen av VirtualNetworkTaps i NetworkInterfaceIpConfiguration har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="96a62-2404">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="96a62-2405">Cortex Get-cmdletar för att visa en lista med alla delar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="96a62-2405">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="96a62-2406">Funktionen för att skapa VirtualHub-referenser för ExpressRouteGateways och VpnGateway har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="96a62-2406">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="96a62-2407">Stöd för tillgänglighetszoner i AzureFirewall och NatGateway har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-2407">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="96a62-2408">Cmdleten Get-AzNetworkServiceTag har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-2408">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="96a62-2409">Lägg till stöd för flera offentliga IP-adresser för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="96a62-2409">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="96a62-2410">Cmdleten New-AzFirewall har uppdaterats:</span><span class="sxs-lookup"><span data-stu-id="96a62-2410">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="96a62-2411">Parametern -PublicIpAddress som accepterar ett eller flera offentliga IP-adressobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-2411">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="96a62-2412">Parametern -VirtualNetwork som accepterar ett virtuellt nätverksobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-2412">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="96a62-2413">Metoderna AddPublicIpAddress och RemovePublicIpAddress har lagts till på brandväggsobjekt – dessa accepterar ett offentligt IP-adressobjekt som indata</span><span class="sxs-lookup"><span data-stu-id="96a62-2413">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="96a62-2414">Inaktuella parametrar -PublicIpName och -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="96a62-2414">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="96a62-2415">Nedanstående kommandon för funktionen har uppdaterats: Ange autentiseringsalternativ för VpnClient AAD till resurser för virtuella nätverksgatewayer.</span><span class="sxs-lookup"><span data-stu-id="96a62-2415">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="96a62-2416">New-AzVirtualNetworkGateway har uppdaterats: De valfria parametrarna AadTenantUri, AadAudienceId och AadIssuerUri för att ange VpnClient AAD-autentiseringsalternativ på en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="96a62-2416">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="96a62-2417">Set-AzVirtualNetworkGateway har uppdaterats: De valfria parametrarna AadTenantUri, AadAudienceId och AadIssuerUri för att ange VpnClient AAD-autentiseringsalternativ på en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="96a62-2417">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="96a62-2418">Set-AzVirtualNetworkGateway har uppdaterats: Den valfria växelparametern RemoveAadAuthentication som tar bort VpnClient AAD-autentiseringsalternativ från en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="96a62-2418">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="96a62-2419">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="96a62-2419">Az.OperationalInsights</span></span>
* <span data-ttu-id="96a62-2420">Aktivera prisnivån **pergb2018** i kommandot ”New-AzureRmOperationalInsightsWorkspace”</span><span class="sxs-lookup"><span data-stu-id="96a62-2420">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="96a62-2421">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="96a62-2421">Az.Resources</span></span>
* <span data-ttu-id="96a62-2422">Stöd för ytterligare alternativ för att exportera en mall</span><span class="sxs-lookup"><span data-stu-id="96a62-2422">Support for additional Template Export options</span></span>
    - <span data-ttu-id="96a62-2423">Lägg till parametern ”-SkipResourceNameParameterization” till Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="96a62-2423">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="96a62-2424">Lägg till parametern ”-SkipAllParameterization” till Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="96a62-2424">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="96a62-2425">Lägg till parametern ”-Resource” till Export-AzResourceGroup för exporterad resursfiltrering</span><span class="sxs-lookup"><span data-stu-id="96a62-2425">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="96a62-2426">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="96a62-2426">Az.ServiceFabric</span></span>
* <span data-ttu-id="96a62-2427">Åtgärda att fel tumavtryck används vid tilläggning av certifikat i ByExistingKeyVault i vissa fall</span><span class="sxs-lookup"><span data-stu-id="96a62-2427">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="96a62-2428">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="96a62-2428">Az.Sql</span></span>
* <span data-ttu-id="96a62-2429">Åtgärda suffix för lagringsslutpunkt i Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="96a62-2429">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="96a62-2430">Åtgärda att aktivering av Advanced Data Security åsidosätter Advanced Threat Protection-princip</span><span class="sxs-lookup"><span data-stu-id="96a62-2430">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="96a62-2431">Nya cmdletar för Management.Sql som gör att kunderna kan lägga till nycklar för transparent datakryptering (TDE) och ange TDE-skydd för hanterade instanser</span><span class="sxs-lookup"><span data-stu-id="96a62-2431">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="96a62-2432">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="96a62-2432">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="96a62-2433">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="96a62-2433">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="96a62-2434">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="96a62-2434">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="96a62-2435">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="96a62-2435">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="96a62-2436">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="96a62-2436">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="96a62-2437">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="96a62-2437">Az.Storage</span></span>
* <span data-ttu-id="96a62-2438">Stöd för typerna FileStorage och SkuName Premium_ZRS när lagringskonton skapas</span><span class="sxs-lookup"><span data-stu-id="96a62-2438">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="96a62-2439">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="96a62-2439">New-AzStorageAccount</span></span>
* <span data-ttu-id="96a62-2440">Beskrivningen av cmdleten för bloboföränderlighet har förtydligats</span><span class="sxs-lookup"><span data-stu-id="96a62-2440">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="96a62-2441">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="96a62-2441">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="96a62-2442">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="96a62-2442">Az.Websites</span></span>
* <span data-ttu-id="96a62-2443">Optimerar Get-AzWebAppCertificate för att filtrera efter resursgrupp på servern i stället för klienten</span><span class="sxs-lookup"><span data-stu-id="96a62-2443">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="96a62-2444">Lägger till växlingsparametern -UseDisasterRecovery till Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="96a62-2444">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="96a62-2445">2.2.0 – juni 2019</span><span class="sxs-lookup"><span data-stu-id="96a62-2445">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="96a62-2446">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="96a62-2446">Az.Cdn</span></span>
* <span data-ttu-id="96a62-2447">Uppdaterade cmdletar för att ge stöd för rulesEngine-funktion baserat på API-version 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="96a62-2447">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="96a62-2448">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="96a62-2448">Az.Compute</span></span>
* <span data-ttu-id="96a62-2449">Lade till parameter `NoWait` som startar åtgärden och returnerar omedelbart, innan åtgärden har slutförts.</span><span class="sxs-lookup"><span data-stu-id="96a62-2449">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="96a62-2450">Uppdaterade cmdletar:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="96a62-2450">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="96a62-2451">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="96a62-2451">Az.EventHub</span></span>
* <span data-ttu-id="96a62-2452">Korrigering för #9231 – Get-AzEventHubNamespace returnerar inga taggar</span><span class="sxs-lookup"><span data-stu-id="96a62-2452">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="96a62-2453">Korrigering för #9230 – Get-AzEventHubNamespace returnerar ResourceGroup istället för ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96a62-2453">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="96a62-2454">Az.Network</span><span class="sxs-lookup"><span data-stu-id="96a62-2454">Az.Network</span></span>
* <span data-ttu-id="96a62-2455">Uppdatera ResourceId och InputObject för NAT-gateway</span><span class="sxs-lookup"><span data-stu-id="96a62-2455">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="96a62-2456">Lägg till alias för ResourceId och InputObject</span><span class="sxs-lookup"><span data-stu-id="96a62-2456">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="96a62-2457">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="96a62-2457">Az.PolicyInsights</span></span>
* <span data-ttu-id="96a62-2458">Åtgärda Null-referensproblem i Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="96a62-2458">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="96a62-2459">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="96a62-2459">Az.RecoveryServices</span></span>
* <span data-ttu-id="96a62-2460">Minsta kvarhållning för IaaSVM-policy i dagar ändrat till 7 från 1</span><span class="sxs-lookup"><span data-stu-id="96a62-2460">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="96a62-2461">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="96a62-2461">Az.ServiceBus</span></span>
* <span data-ttu-id="96a62-2462">Korrigering för ärende #9182 – Get-AzServiceBusNamespace returnerar ResourceGroup istället för ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96a62-2462">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="96a62-2463">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="96a62-2463">Az.ServiceFabric</span></span>
* <span data-ttu-id="96a62-2464">Åtgärda stavfel i felmeddelandet för Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="96a62-2464">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="96a62-2465">Åtgärda saknat tecken i Service Fabric-kommandorader</span><span class="sxs-lookup"><span data-stu-id="96a62-2465">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="96a62-2466">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="96a62-2466">Az.Sql</span></span>
* <span data-ttu-id="96a62-2467">Lägg till parametern DnsZonePartner för New-AzureSqlInstance-cmdlet för att ge stöd för AutoDr för hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="96a62-2467">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="96a62-2468">Avvecklar cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="96a62-2468">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="96a62-2469">Döp om cmdletar för hotidentifiering till Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="96a62-2469">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="96a62-2470">Parametrarna New-AzSqlInstance -StorageSizeInGB och -LicenseType är nu valfria.</span><span class="sxs-lookup"><span data-stu-id="96a62-2470">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="96a62-2471">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="96a62-2471">Az.Websites</span></span>
* <span data-ttu-id="96a62-2472">åtgärdar problemet där användningen av Set-AzWebApp och Set-AzWebAppSlot med -WebApp-egenskap tog bort taggarna</span><span class="sxs-lookup"><span data-stu-id="96a62-2472">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="96a62-2473">2.1.0 – maj 2019</span><span class="sxs-lookup"><span data-stu-id="96a62-2473">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="96a62-2474">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="96a62-2474">Az.ApiManagement</span></span>
* <span data-ttu-id="96a62-2475">Skapade nya cmdletar för att hantera diagnostik för global- och API-omfång</span><span class="sxs-lookup"><span data-stu-id="96a62-2475">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="96a62-2476">**Get-AzApiManagementDiagnostic** – Skaffa diagnostik konfigurerad för global- eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="96a62-2476">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="96a62-2477">**New-AzApiManagementDiagnostic** – Skapa ny diagnostik för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="96a62-2477">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="96a62-2478">**New-AzApiManagementHttpMessageDiagnostic** – Skapa diagnostikinställning om vilka rubriker som ska loggas och storleken på brödtextbyte</span><span class="sxs-lookup"><span data-stu-id="96a62-2478">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="96a62-2479">**New-AzApiManagementPipelineDiagnosticSetting** – Skapa diagnostikinställningar för inkommande/utgående HTTP-meddelanden till gatewayen.</span><span class="sxs-lookup"><span data-stu-id="96a62-2479">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="96a62-2480">**New-AzApiManagementSamplingSetting** – Skapa samplinginställningar för begäranden/svar för en diagnostik</span><span class="sxs-lookup"><span data-stu-id="96a62-2480">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="96a62-2481">**Remove-AzApiManagementDiagnostic** – Ta bort en diagnostikenhet för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="96a62-2481">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="96a62-2482">**Set-AzApiManagementDiagnostic** – Uppdatera en diagnostikenhet för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="96a62-2482">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="96a62-2483">Skapade nya cmdletar för hantering av cacheminne i ApiManagement-tjänsten</span><span class="sxs-lookup"><span data-stu-id="96a62-2483">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="96a62-2484">**Get-AzApiManagementCache** – Hämta information om cacheminnet som anges av identifierare eller alla cacheminnen</span><span class="sxs-lookup"><span data-stu-id="96a62-2484">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="96a62-2485">**New-AzApiManagementCache** – Skapa ett nytt default-cacheminne eller cacheminne i en viss Azure-region</span><span class="sxs-lookup"><span data-stu-id="96a62-2485">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="96a62-2486">**Remove-AzApiManagementCache** – Ta bort ett cacheminne</span><span class="sxs-lookup"><span data-stu-id="96a62-2486">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="96a62-2487">**Remove-AzApiManagementCache** – Ta bort ett cacheminne</span><span class="sxs-lookup"><span data-stu-id="96a62-2487">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="96a62-2488">Skapade nya cmdletar för hantering av API-schema</span><span class="sxs-lookup"><span data-stu-id="96a62-2488">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="96a62-2489">**New-AzApiManagementSchema** – Skapa ett nytt schema för ett API</span><span class="sxs-lookup"><span data-stu-id="96a62-2489">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="96a62-2490">**Get-AzApiManagementSchema** – Hämta de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="96a62-2490">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="96a62-2491">**Remove-AzApiManagementSchema** – Ta bort de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="96a62-2491">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="96a62-2492">**Set-AzApiManagementSchema** – Uppdatera de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="96a62-2492">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="96a62-2493">Skapa ny cmdlet för att generera en användartoken.</span><span class="sxs-lookup"><span data-stu-id="96a62-2493">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="96a62-2494">**New-AzApiManagementUserToken** – Skapa en ny användartoken som enligt standardinställning är giltig i 8 timmar. Token för GIT-användaren kan skapas med den här cmdleten./</span><span class="sxs-lookup"><span data-stu-id="96a62-2494">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="96a62-2495">Skapade en ny cmdlet för att hämta nätverksstatus</span><span class="sxs-lookup"><span data-stu-id="96a62-2495">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="96a62-2496">**Get-AzApiManagementNetworkStatus** – Hämta nätverksstatusanslutningen för resurserna som API Management-tjänsten är beroende av.</span><span class="sxs-lookup"><span data-stu-id="96a62-2496">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="96a62-2497">Det här är användbart när du distribuerar ApiManagement-tjänsten i ett virtuellt nätverk och validerar om något beroende är brutet.</span><span class="sxs-lookup"><span data-stu-id="96a62-2497">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="96a62-2498">Uppdaterade cmdlet **New-AzApiManagement** för att hantera ApiManagement-tjänsten</span><span class="sxs-lookup"><span data-stu-id="96a62-2498">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="96a62-2499">Lade till stöd för den nya SKU:n Consumption</span><span class="sxs-lookup"><span data-stu-id="96a62-2499">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="96a62-2500">Aktiverade stöd för att slå på flaggan EnableClientCertificate för SKU:n Consumption</span><span class="sxs-lookup"><span data-stu-id="96a62-2500">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="96a62-2501">Den nya cmdleten **New-AzApiManagementSslSetting** gör det möjligt att ställa in TLS/SSL-inställningen på ”Backend” och ”Frontend” (serverdel och klientdel).</span><span class="sxs-lookup"><span data-stu-id="96a62-2501">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="96a62-2502">Det här kan också användas till att konfigurera chiffer som 3DES och ServerProtocols som Http2 för Frontend för en ApiManagement-tjänst.</span><span class="sxs-lookup"><span data-stu-id="96a62-2502">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="96a62-2503">Stöd har lagts till för att konfigurera värdnamnet DeveloperPortal på ApiManagement-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="96a62-2503">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="96a62-2504">Uppdaterade cmdletar **Get-AzApiManagementSsoToken** för att ta PsApiManagement-objekt som indata</span><span class="sxs-lookup"><span data-stu-id="96a62-2504">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="96a62-2505">Uppdaterad cmdleten för att visa infogade felmeddelanden</span><span class="sxs-lookup"><span data-stu-id="96a62-2505">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="96a62-2506">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Felkod: Felmeddelande av typen ValidationError: Ett eller flera fält innehåller felaktiga värden: Felinformation:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="96a62-2506">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="96a62-2507">Uppdaterade cmdlet **Export-AzApiManagementApi** för att exportera API:er i OpenApi 3.0-format</span><span class="sxs-lookup"><span data-stu-id="96a62-2507">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="96a62-2508">Uppdaterade cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="96a62-2508">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="96a62-2509">Importera API från dokumentspecifikationen OpenApi 3.0</span><span class="sxs-lookup"><span data-stu-id="96a62-2509">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="96a62-2510">Om du vill åsidosätta egenskapen PsApiManagementSchema specificerad i ett dokument (Swagger, Wadl, Wsdl, OpenApi).</span><span class="sxs-lookup"><span data-stu-id="96a62-2510">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="96a62-2511">Åsidosätta egenskapen ServiceUrl som specificeras i ett dokument.</span><span class="sxs-lookup"><span data-stu-id="96a62-2511">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="96a62-2512">Uppdaterade cmdlet **Get-AzApiManagementPolicy** för att returnera policy i undantaget format av typen icke-XML med rawxml</span><span class="sxs-lookup"><span data-stu-id="96a62-2512">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="96a62-2513">Uppdaterade cmdlet **Set-AzApiManagementPolicy** för att godkänna policy i undantaget format av typen icke-XML med rawxml och XML undantaget med xml</span><span class="sxs-lookup"><span data-stu-id="96a62-2513">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="96a62-2514">Uppdaterad cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="96a62-2514">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="96a62-2515">Konfigurera API med OpenId auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="96a62-2515">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="96a62-2516">Skapa ett API i ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="96a62-2516">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="96a62-2517">Klona ett API med SourceApiId och SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="96a62-2517">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="96a62-2518">Möjlighet att konfigurera SubscriptionRequired i API-omfattningen.</span><span class="sxs-lookup"><span data-stu-id="96a62-2518">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="96a62-2519">Uppdaterad cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="96a62-2519">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="96a62-2520">Konfigurera API med OpenId auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="96a62-2520">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="96a62-2521">Uppdatera ett API till ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="96a62-2521">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="96a62-2522">Möjlighet att konfigurera SubscriptionRequired i API-omfattningen.</span><span class="sxs-lookup"><span data-stu-id="96a62-2522">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="96a62-2523">Uppdaterad cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="96a62-2523">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="96a62-2524">Klona en befintlig version med hjälp av SourceApiRevision (kopiera taggar, produkter, åtgärder och principer).</span><span class="sxs-lookup"><span data-stu-id="96a62-2524">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="96a62-2525">Den nya revisionen antar ApiId från den överordnade instansen.</span><span class="sxs-lookup"><span data-stu-id="96a62-2525">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="96a62-2526">Tillhandahålla ApiRevisionDescription</span><span class="sxs-lookup"><span data-stu-id="96a62-2526">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="96a62-2527">Åsidosätta ServiceUrl vid kloning av ett API.</span><span class="sxs-lookup"><span data-stu-id="96a62-2527">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="96a62-2528">Uppdaterad cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="96a62-2528">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="96a62-2529">Konfigurera AAD eller AADB2C med en Authority</span><span class="sxs-lookup"><span data-stu-id="96a62-2529">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="96a62-2530">Konfigurera SignupPolicy, SigninPolicy, ProfileEditingPolicy och PasswordResetPolicy</span><span class="sxs-lookup"><span data-stu-id="96a62-2530">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="96a62-2531">Uppdaterad cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="96a62-2531">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="96a62-2532">Kompensera för ny SubscriptonModel med Scope och UserId</span><span class="sxs-lookup"><span data-stu-id="96a62-2532">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="96a62-2533">Kompensera för gammal prenumerationsmodell med ProductId och UserId</span><span class="sxs-lookup"><span data-stu-id="96a62-2533">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="96a62-2534">Lägg till funktion för att aktivera AllowTracing på prenumerationsnivå.</span><span class="sxs-lookup"><span data-stu-id="96a62-2534">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="96a62-2535">Uppdaterad cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="96a62-2535">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="96a62-2536">Kompensera för ny SubscriptonModel med Scope och UserId</span><span class="sxs-lookup"><span data-stu-id="96a62-2536">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="96a62-2537">Kompensera för gammal prenumerationsmodell med ProductId och UserId</span><span class="sxs-lookup"><span data-stu-id="96a62-2537">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="96a62-2538">Lägg till funktion för att aktivera AllowTracing på prenumerationsnivå.</span><span class="sxs-lookup"><span data-stu-id="96a62-2538">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="96a62-2539">Uppdaterade följande cmdletar för att acceptera ResourceId som indata</span><span class="sxs-lookup"><span data-stu-id="96a62-2539">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="96a62-2540">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="96a62-2540">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="96a62-2541">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="96a62-2541">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="96a62-2542">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="96a62-2542">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="96a62-2543">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="96a62-2543">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="96a62-2544">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="96a62-2544">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="96a62-2545">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="96a62-2545">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="96a62-2546">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="96a62-2546">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="96a62-2547">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="96a62-2547">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="96a62-2548">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="96a62-2548">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="96a62-2549">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="96a62-2549">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="96a62-2550">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="96a62-2550">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="96a62-2551">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="96a62-2551">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="96a62-2552">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="96a62-2552">Az.Automation</span></span>
* <span data-ttu-id="96a62-2553">Uppdaterade Get-AzAutomationJobOutputRecord för att hantera postvärden av typen JSON och Text.</span><span class="sxs-lookup"><span data-stu-id="96a62-2553">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="96a62-2554">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="96a62-2554">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="96a62-2555">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="96a62-2555">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="96a62-2556">Ändrade beteende för Start-AzAutomationDscCompilationJob till att bara starta jobbet istället för att vänta på slutförandet.</span><span class="sxs-lookup"><span data-stu-id="96a62-2556">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="96a62-2557">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="96a62-2557">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="96a62-2558">Korrigering för Get-AzAutomationDscNode när using -Name returnerar alla noder.</span><span class="sxs-lookup"><span data-stu-id="96a62-2558">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="96a62-2559">Nu returnerar den endast den matchande noden.</span><span class="sxs-lookup"><span data-stu-id="96a62-2559">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="96a62-2560">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="96a62-2560">Az.Compute</span></span>
* <span data-ttu-id="96a62-2561">Lägg till parametrarna ProtectFromScaleIn och ProtectFromScaleSetAction i cmdleten Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="96a62-2561">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="96a62-2562">Nu är standardinställningen att vimpelparametern New-AzVM använder en tillgänglig plats om USA, östra inte stöds</span><span class="sxs-lookup"><span data-stu-id="96a62-2562">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="96a62-2563">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="96a62-2563">Az.DataLakeStore</span></span>
* <span data-ttu-id="96a62-2564">Uppdatera ADLS-sdk för att använda httpclient, integrera dataplanstestning med Azure-ramverk</span><span class="sxs-lookup"><span data-stu-id="96a62-2564">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="96a62-2565">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="96a62-2565">Az.Monitor</span></span>
* <span data-ttu-id="96a62-2566">Korrigera felaktiga parameternamn i hjälpexempel</span><span class="sxs-lookup"><span data-stu-id="96a62-2566">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="96a62-2567">Az.Network</span><span class="sxs-lookup"><span data-stu-id="96a62-2567">Az.Network</span></span>
* <span data-ttu-id="96a62-2568">Lägg till flaggan DisableBgpRoutePropagation i utdata för effektiv routningstabell</span><span class="sxs-lookup"><span data-stu-id="96a62-2568">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="96a62-2569">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="96a62-2569">Updated cmdlet:</span></span>
        - <span data-ttu-id="96a62-2570">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="96a62-2570">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="96a62-2571">Åtgärda dubbelstreck i dokumentationen New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="96a62-2571">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="96a62-2572">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="96a62-2572">Az.Resources</span></span>
* <span data-ttu-id="96a62-2573">Lägg till ny cmdlet Get-AzureRmDenyAssignment för att hämta tilldelningsnekanden</span><span class="sxs-lookup"><span data-stu-id="96a62-2573">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="96a62-2574">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="96a62-2574">Az.Sql</span></span>
* <span data-ttu-id="96a62-2575">Döp om Advanced Threat Protection-cmdletar för Advanced Data Security och aktivera Vulnerability Assessment som standard</span><span class="sxs-lookup"><span data-stu-id="96a62-2575">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="96a62-2576">2.0.0 – maj 2019</span><span class="sxs-lookup"><span data-stu-id="96a62-2576">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="96a62-2577">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="96a62-2577">Az.Accounts</span></span>
* <span data-ttu-id="96a62-2578">Uppdatera autentiseringsbiblioteket för att åtgärda ADFS-problem med autentisering av användarnamn/lösenord</span><span class="sxs-lookup"><span data-stu-id="96a62-2578">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="96a62-2579">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="96a62-2579">Az.CognitiveServices</span></span>
* <span data-ttu-id="96a62-2580">Visa endast Bing-ansvarsfriskrivning för Bing-sökningstjänster.</span><span class="sxs-lookup"><span data-stu-id="96a62-2580">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="96a62-2581">Förbättra felmeddelande när det inte går att skapa konton.</span><span class="sxs-lookup"><span data-stu-id="96a62-2581">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="96a62-2582">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="96a62-2582">Az.Compute</span></span>
* <span data-ttu-id="96a62-2583">Funktion för närhetsplaceringsgrupper.</span><span class="sxs-lookup"><span data-stu-id="96a62-2583">Proximity placement group feature.</span></span>
    - <span data-ttu-id="96a62-2584">Följande nya cmdletar har lagts till:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="96a62-2584">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="96a62-2585">Den nya parametern ProximityPlacementGroupId har lagts till i följande cmdletar:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="96a62-2585">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="96a62-2586">Parametern StorageAccountType har lagts till i New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="96a62-2586">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="96a62-2587">TargetRegion för New-AzGalleryImageVersion kan innehålla StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="96a62-2587">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="96a62-2588">Växlingsparametern SkipShutdown har lagts till i Stop-AzVM och Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="96a62-2588">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="96a62-2589">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="96a62-2589">Breaking changes</span></span>
    - <span data-ttu-id="96a62-2590">Set-AzVMBootDiagnostics har ändrats till Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="96a62-2590">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="96a62-2591">Export-AzLogAnalyticThrottledRequests har ändrats till Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="96a62-2591">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="96a62-2592">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="96a62-2592">Az.DeploymentManager</span></span>
* <span data-ttu-id="96a62-2593">De första allmänt tillgängliga versionerna av cmdletar för Distributionshanteraren i Azure</span><span class="sxs-lookup"><span data-stu-id="96a62-2593">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="96a62-2594">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="96a62-2594">Az.Dns</span></span>
* <span data-ttu-id="96a62-2595">Automatisk delegering av DNS för NameServer</span><span class="sxs-lookup"><span data-stu-id="96a62-2595">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="96a62-2596">Det överordnade zonnamnet kan användas som ytterligare valfri parameter i cmdleten för att skapa DNS-zoner.</span><span class="sxs-lookup"><span data-stu-id="96a62-2596">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="96a62-2597">Lägger till NS-poster för en nyligen skapad underordnad zon i den överordnade zonen.</span><span class="sxs-lookup"><span data-stu-id="96a62-2597">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="96a62-2598">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="96a62-2598">Az.FrontDoor</span></span>
* <span data-ttu-id="96a62-2599">De första allmänt tillgängliga versionerna av cmdletar för Azure FrontDoor</span><span class="sxs-lookup"><span data-stu-id="96a62-2599">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="96a62-2600">Byt namn på WAF-cmdletar så att de omfattar ”Waf”</span><span class="sxs-lookup"><span data-stu-id="96a62-2600">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="96a62-2601">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="96a62-2601">Az.HDInsight</span></span>
* <span data-ttu-id="96a62-2602">Två cmdletar har tagits bort:</span><span class="sxs-lookup"><span data-stu-id="96a62-2602">Removed two cmdlets:</span></span>
    - <span data-ttu-id="96a62-2603">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="96a62-2603">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="96a62-2604">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="96a62-2604">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="96a62-2605">En ny cmdlet har lagts till, Set-AzHDInsightGatewayCredential, som ersätter Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="96a62-2605">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="96a62-2606">Uppdatera cmdleten Get-AzHDInsightJobOutput för att skilja mellan läsarrollen och HDInsight-operatörsrollen:</span><span class="sxs-lookup"><span data-stu-id="96a62-2606">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="96a62-2607">Användare med läsarrollen måste uttryckligen ange parametern ”DefaultStorageAccountKey”, annars uppstår fel.</span><span class="sxs-lookup"><span data-stu-id="96a62-2607">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="96a62-2608">Användare med HDInsight-operatörsrollen påverkas inte.</span><span class="sxs-lookup"><span data-stu-id="96a62-2608">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="96a62-2609">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="96a62-2609">Az.Monitor</span></span>
* <span data-ttu-id="96a62-2610">Nya cmdletar för SQR API (schemalagd frågeregel)</span><span class="sxs-lookup"><span data-stu-id="96a62-2610">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="96a62-2611">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="96a62-2611">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="96a62-2612">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="96a62-2612">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="96a62-2613">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="96a62-2613">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="96a62-2614">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="96a62-2614">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="96a62-2615">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="96a62-2615">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="96a62-2616">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="96a62-2616">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="96a62-2617">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="96a62-2617">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="96a62-2618">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="96a62-2618">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="96a62-2619">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="96a62-2619">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="96a62-2620">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="96a62-2620">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="96a62-2621">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="96a62-2621">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="96a62-2622">[Mer](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information om SQR API</span><span class="sxs-lookup"><span data-stu-id="96a62-2622">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="96a62-2623">Az.Monitor.md har uppdaterats för att omfatta cmdletar för måttbaserade aviseringsregler i GenV2 (inte klassiska)</span><span class="sxs-lookup"><span data-stu-id="96a62-2623">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="96a62-2624">Az.Network</span><span class="sxs-lookup"><span data-stu-id="96a62-2624">Az.Network</span></span>
* <span data-ttu-id="96a62-2625">Lägg till stöd för NAT Gateway-resurs</span><span class="sxs-lookup"><span data-stu-id="96a62-2625">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="96a62-2626">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="96a62-2626">New cmdlets</span></span>
        - <span data-ttu-id="96a62-2627">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="96a62-2627">New-AzNatGateway</span></span>
        - <span data-ttu-id="96a62-2628">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="96a62-2628">Get-AzNatGateway</span></span>
        - <span data-ttu-id="96a62-2629">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="96a62-2629">Set-AzNatGateway</span></span>
        - <span data-ttu-id="96a62-2630">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="96a62-2630">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="96a62-2631">Uppdaterade cmdletar</span><span class="sxs-lookup"><span data-stu-id="96a62-2631">Updated cmdlets</span></span>
        - <span data-ttu-id="96a62-2632">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="96a62-2632">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="96a62-2633">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="96a62-2633">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="96a62-2634">Nedanstående kommandon för funktionen har uppdaterats: Ange/ta bort anpassade vägar på Brooklyn Gateway.</span><span class="sxs-lookup"><span data-stu-id="96a62-2634">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="96a62-2635">New-AzVirtualNetworkGateway har uppdaterats: Den valfria parametern -CustomRoute har lagts till för att ställa in adressprefix som anpassade vägar för att ange gateway.</span><span class="sxs-lookup"><span data-stu-id="96a62-2635">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="96a62-2636">Set-AzVirtualNetworkGateway har uppdaterats: Den valfria parametern -CustomRoute har lagts till för att ange adressprefix som anpassade vägar för att ange gateway.</span><span class="sxs-lookup"><span data-stu-id="96a62-2636">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="96a62-2637">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="96a62-2637">Az.PolicyInsights</span></span>
* <span data-ttu-id="96a62-2638">Stöd för att fråga efter information om principutvärdering.</span><span class="sxs-lookup"><span data-stu-id="96a62-2638">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="96a62-2639">Lägg till parametern ”-Expand” för Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="96a62-2639">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="96a62-2640">Stöd för -Expand PolicyEvaluationDetails.</span><span class="sxs-lookup"><span data-stu-id="96a62-2640">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="96a62-2641">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="96a62-2641">Az.RecoveryServices</span></span>
* <span data-ttu-id="96a62-2642">Stöd för att dela prenumeration mellan Azure och Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="96a62-2642">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="96a62-2643">Markering av kommande icke-bakåtkompatibla ändringar för Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="96a62-2643">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="96a62-2644">Korrigering för återställningsplan och åtgärdsplan i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="96a62-2644">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="96a62-2645">Korrigering för mappning av uppdateringsnätverk i Azure Site Recovery för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="96a62-2645">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="96a62-2646">Korrigering för instruktioner för uppdateringsskydd i Azure Site Recovery för Azure till Azure för hanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="96a62-2646">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="96a62-2647">Andra mindre korrigeringar.</span><span class="sxs-lookup"><span data-stu-id="96a62-2647">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="96a62-2648">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="96a62-2648">Az.Relay</span></span>
* <span data-ttu-id="96a62-2649">Korrigera stavfel i kundriktade meddelanden</span><span class="sxs-lookup"><span data-stu-id="96a62-2649">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="96a62-2650">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="96a62-2650">Az.ServiceBus</span></span>
* <span data-ttu-id="96a62-2651">Nya cmdletar har lagts till för NetworkRuleSet för namnområden</span><span class="sxs-lookup"><span data-stu-id="96a62-2651">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="96a62-2652">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="96a62-2652">Az.Storage</span></span>
* <span data-ttu-id="96a62-2653">Uppgradera till lagringsklientbiblioteket 10.0.1 (namnområdet för alla objekt från detta SDK ändras från ”Microsoft.WindowsAzure.Storage. *till ”Microsoft.Azure.Storage.* ”)</span><span class="sxs-lookup"><span data-stu-id="96a62-2653">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="96a62-2654">Uppgradera till Microsoft.Azure.Management.Storage 11.0.0 för att stödja den nya API-versionen 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="96a62-2654">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="96a62-2655">Standardlagringskontot i Skapa lagringskonto ändras från ”Storage” till ”StorageV2”</span><span class="sxs-lookup"><span data-stu-id="96a62-2655">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="96a62-2656">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="96a62-2656">New-AzStorageAccount</span></span>
* <span data-ttu-id="96a62-2657">Ändra lagringskontots cmdlet-utdata Sku.Name för att passa med indata-SkuName genom att lägga till ”-”. Till exempel ändras ”StandardLRS” till ”Standard_LRS”</span><span class="sxs-lookup"><span data-stu-id="96a62-2657">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="96a62-2658">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="96a62-2658">New-AzStorageAccount</span></span>
    - <span data-ttu-id="96a62-2659">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="96a62-2659">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="96a62-2660">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="96a62-2660">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="96a62-2661">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="96a62-2661">Az.Websites</span></span>
* <span data-ttu-id="96a62-2662">Egenskapen ”typ” konfigureras nu för PSSite-objekt som returneras av Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="96a62-2662">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="96a62-2663">Get-AzWebApp\*Metrics och Get-AzAppServicePlanMetrics markeras som inaktuella</span><span class="sxs-lookup"><span data-stu-id="96a62-2663">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="96a62-2664">1.8.0 – april 2019</span><span class="sxs-lookup"><span data-stu-id="96a62-2664">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="96a62-2665">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="96a62-2665">Highlights since the last major release</span></span>
* <span data-ttu-id="96a62-2666">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="96a62-2666">General availability of `Az` module</span></span>
* <span data-ttu-id="96a62-2667">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="96a62-2667">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="96a62-2668">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="96a62-2668">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="96a62-2669">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-2669">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="96a62-2670">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-2670">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="96a62-2671">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-2671">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="96a62-2672">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="96a62-2672">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="96a62-2673">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="96a62-2673">Az.Accounts</span></span>
* <span data-ttu-id="96a62-2674">Uppdatera Uninstall-AzureRm för att ta bort moduler i Mac på ett korrekt sätt</span><span class="sxs-lookup"><span data-stu-id="96a62-2674">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="96a62-2675">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="96a62-2675">Az.Batch</span></span>
* <span data-ttu-id="96a62-2676">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="96a62-2676">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="96a62-2677">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="96a62-2677">Az.Cdn</span></span>
* <span data-ttu-id="96a62-2678">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="96a62-2678">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="96a62-2679">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="96a62-2679">Az.CognitiveServices</span></span>
* <span data-ttu-id="96a62-2680">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="96a62-2680">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="96a62-2681">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="96a62-2681">Az.Compute</span></span>
* <span data-ttu-id="96a62-2682">Åtgärda problem med AEM-installationen om resurs-ID:n för diskar innehåller resourcegroups i gemener i resurs-ID:n</span><span class="sxs-lookup"><span data-stu-id="96a62-2682">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="96a62-2683">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="96a62-2683">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="96a62-2684">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="96a62-2684">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="96a62-2685">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="96a62-2685">Az.DataFactory</span></span>
* <span data-ttu-id="96a62-2686">Lägg till SsisProperties om NodeCount inte är null för hanterad integreringskörning.</span><span class="sxs-lookup"><span data-stu-id="96a62-2686">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="96a62-2687">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="96a62-2687">Az.DataLakeStore</span></span>
* <span data-ttu-id="96a62-2688">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="96a62-2688">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="96a62-2689">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="96a62-2689">Az.EventGrid</span></span>
* <span data-ttu-id="96a62-2690">Hjälptexten för slutpunkten har uppdaterats för att visa att resurser ska skapas innan cmdletarna för att skapa/uppdatera händelseprenumerationer används.</span><span class="sxs-lookup"><span data-stu-id="96a62-2690">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="96a62-2691">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="96a62-2691">Az.EventHub</span></span>
* <span data-ttu-id="96a62-2692">Nya cmdletar har lagts till för NetworkRuleSet för namnområden</span><span class="sxs-lookup"><span data-stu-id="96a62-2692">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="96a62-2693">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="96a62-2693">Az.HDInsight</span></span>
* <span data-ttu-id="96a62-2694">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="96a62-2694">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="96a62-2695">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="96a62-2695">Az.IotHub</span></span>
* <span data-ttu-id="96a62-2696">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="96a62-2696">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="96a62-2697">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="96a62-2697">Az.KeyVault</span></span>
* <span data-ttu-id="96a62-2698">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="96a62-2698">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="96a62-2699">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="96a62-2699">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="96a62-2700">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="96a62-2700">Az.MachineLearning</span></span>
* <span data-ttu-id="96a62-2701">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="96a62-2701">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="96a62-2702">Az.Media</span><span class="sxs-lookup"><span data-stu-id="96a62-2702">Az.Media</span></span>
* <span data-ttu-id="96a62-2703">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="96a62-2703">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="96a62-2704">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="96a62-2704">Az.Monitor</span></span>
  * <span data-ttu-id="96a62-2705">Nya cmdletar för måttbaserad aviseringsregel i GenV2 (inte klassisk)</span><span class="sxs-lookup"><span data-stu-id="96a62-2705">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="96a62-2706">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="96a62-2706">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="96a62-2707">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="96a62-2707">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="96a62-2708">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="96a62-2708">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="96a62-2709">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="96a62-2709">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="96a62-2710">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="96a62-2710">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="96a62-2711">Monitor SDK har uppdaterats till version 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="96a62-2711">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="96a62-2712">Az.Network</span><span class="sxs-lookup"><span data-stu-id="96a62-2712">Az.Network</span></span>
* <span data-ttu-id="96a62-2713">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="96a62-2713">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="96a62-2714">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="96a62-2714">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="96a62-2715">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="96a62-2715">Az.NotificationHubs</span></span>
* <span data-ttu-id="96a62-2716">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="96a62-2716">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="96a62-2717">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="96a62-2717">Az.OperationalInsights</span></span>
* <span data-ttu-id="96a62-2718">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="96a62-2718">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="96a62-2719">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="96a62-2719">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="96a62-2720">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="96a62-2720">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="96a62-2721">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="96a62-2721">Az.RecoveryServices</span></span>
* <span data-ttu-id="96a62-2722">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="96a62-2722">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="96a62-2723">Tabellformatet för SQL i virtuella Azure-datorer har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="96a62-2723">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="96a62-2724">En alternativ metod för att hämta platser i AzureFileShare har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-2724">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="96a62-2725">ScheduleRunDays i SchedulePolicy-objekt har uppdaterats enligt tidszon</span><span class="sxs-lookup"><span data-stu-id="96a62-2725">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="96a62-2726">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="96a62-2726">Az.RedisCache</span></span>
* <span data-ttu-id="96a62-2727">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="96a62-2727">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="96a62-2728">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="96a62-2728">Az.Resources</span></span>
* <span data-ttu-id="96a62-2729">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="96a62-2729">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="96a62-2730">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="96a62-2730">Az.Sql</span></span>
* <span data-ttu-id="96a62-2731">Ersätt Monitor SDK-beroende med vanlig kod</span><span class="sxs-lookup"><span data-stu-id="96a62-2731">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="96a62-2732">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="96a62-2732">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="96a62-2733">Förbättrad process för klassificering av flera kolumner.</span><span class="sxs-lookup"><span data-stu-id="96a62-2733">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="96a62-2734">Inkludera SKU-egenskaper (SKU-namn, serie, kapacitet) i svaret från Get-AzSqlServerServiceObjective och formatera som tabell som standard.</span><span class="sxs-lookup"><span data-stu-id="96a62-2734">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="96a62-2735">Möjlighet att använda Get-AzSqlServerServiceObjective efter plats utan att behöva en redan befintlig server i regionen.</span><span class="sxs-lookup"><span data-stu-id="96a62-2735">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="96a62-2736">Stöd för tidszonsparametern när hanterade instanser skapas.</span><span class="sxs-lookup"><span data-stu-id="96a62-2736">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="96a62-2737">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="96a62-2737">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="96a62-2738">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="96a62-2738">Az.Websites</span></span>
* <span data-ttu-id="96a62-2739">åtgärdar Set-AzWebApp och Set-AzWebAppSlot så att de inte tar bort taggar vid körning</span><span class="sxs-lookup"><span data-stu-id="96a62-2739">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="96a62-2740">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="96a62-2740">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="96a62-2741">SDK för WebSites har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="96a62-2741">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="96a62-2742">Egenskapen AdminSiteName har tagits bort från PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="96a62-2742">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="96a62-2743">1.7.0 – april 2019</span><span class="sxs-lookup"><span data-stu-id="96a62-2743">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="96a62-2744">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="96a62-2744">Highlights since the last major release</span></span>
* <span data-ttu-id="96a62-2745">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="96a62-2745">General availability of `Az` module</span></span>
* <span data-ttu-id="96a62-2746">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="96a62-2746">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="96a62-2747">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="96a62-2747">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="96a62-2748">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-2748">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="96a62-2749">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-2749">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="96a62-2750">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-2750">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="96a62-2751">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="96a62-2751">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="96a62-2752">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="96a62-2752">Az.Accounts</span></span>
* <span data-ttu-id="96a62-2753">Add-AzEnvironment och Set-AzEnvironment har uppdaterats för att godkänna parametern AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="96a62-2753">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="96a62-2754">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="96a62-2754">Az.AnalysisServices</span></span>
* <span data-ttu-id="96a62-2755">ServiceClient används i cmdletar för dataplan och den ursprungliga autentiseringslogiken har tagits bort</span><span class="sxs-lookup"><span data-stu-id="96a62-2755">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="96a62-2756">Add-AzureASAccount används för omslutning av Connect-AzAccount för att undvika en icke-bakåtkompatibel ändring</span><span class="sxs-lookup"><span data-stu-id="96a62-2756">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="96a62-2757">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="96a62-2757">Az.Automation</span></span>
* <span data-ttu-id="96a62-2758">Buggen för cmdleten New-AzAutomationSoftwareUpdateConfiguration för inkluderingar har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="96a62-2758">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="96a62-2759">Nu bör parametern IncludedKbNumber och IncludedPackageNameMask fungera.</span><span class="sxs-lookup"><span data-stu-id="96a62-2759">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="96a62-2760">Felkorrigering för dynamiska grupper i uppdateringshanteringen för azure automation</span><span class="sxs-lookup"><span data-stu-id="96a62-2760">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="96a62-2761">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="96a62-2761">Az.Compute</span></span>
* <span data-ttu-id="96a62-2762">Lägg till parametern HyperVGeneration i New-AzDiskConfig och New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="96a62-2762">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="96a62-2763">Tillåt att virtuella datorer skapas med galleribilder från andra klientorganisationer.</span><span class="sxs-lookup"><span data-stu-id="96a62-2763">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="96a62-2764">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="96a62-2764">Az.ContainerInstance</span></span>
* <span data-ttu-id="96a62-2765">Ett problem har åtgärdats i parametern -Command för New-AzContainerGroup som lade till ett avslutande tomt argument</span><span class="sxs-lookup"><span data-stu-id="96a62-2765">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="96a62-2766">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="96a62-2766">Az.DataFactory</span></span>
* <span data-ttu-id="96a62-2767">ADF .Net SDK-versionen har uppdaterats till 3.0.2</span><span class="sxs-lookup"><span data-stu-id="96a62-2767">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="96a62-2768">Cmdleten Set-AzDataFactoryV2 har uppdaterats med extra parametrar för inställningar som rör RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="96a62-2768">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="96a62-2769">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="96a62-2769">Az.Resources</span></span>
* <span data-ttu-id="96a62-2770">Förbättra hanteringen av providrar för Get-AzResource när parametrarna -ResourceId eller -ResourceGroupName, -Name och -ResourceType tillhandahålls</span><span class="sxs-lookup"><span data-stu-id="96a62-2770">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="96a62-2771">Förbättra felhanteringen för ”Test-AzDeployment” och ”Test-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="96a62-2771">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="96a62-2772">Hantera fel utanför distributionsvalideringen och ta med dem i kommandoutdata istället</span><span class="sxs-lookup"><span data-stu-id="96a62-2772">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="96a62-2773">Mer information här: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="96a62-2773">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="96a62-2774">Lägg till växlingsparametern -IgnoreDynamicParameters till en uppsättning av cmdletar för distribution för att hoppa över fråga i skript och jobbscenarier</span><span class="sxs-lookup"><span data-stu-id="96a62-2774">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="96a62-2775">Mer information här: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="96a62-2775">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="96a62-2776">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="96a62-2776">Az.Sql</span></span>
* <span data-ttu-id="96a62-2777">Stöd för dataklassificering av databaser.</span><span class="sxs-lookup"><span data-stu-id="96a62-2777">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="96a62-2778">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="96a62-2778">Az.Storage</span></span>
* <span data-ttu-id="96a62-2779">Rapportera detaljfel när lagringskontext skapas med parametern -UseConnectedAccount, men utan inloggning på Azure-kontot</span><span class="sxs-lookup"><span data-stu-id="96a62-2779">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="96a62-2780">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="96a62-2780">New-AzStorageContext</span></span>
* <span data-ttu-id="96a62-2781">Stöd för att hantera Blob Service-egenskaper för ett angivet lagringskonto med API:et för hanteringsplan</span><span class="sxs-lookup"><span data-stu-id="96a62-2781">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="96a62-2782">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="96a62-2782">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="96a62-2783">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="96a62-2783">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="96a62-2784">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="96a62-2784">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="96a62-2785">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="96a62-2785">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="96a62-2786">Stöd för -AsJob-cmdletar för att ladda upp och ladda ned blobar och filer</span><span class="sxs-lookup"><span data-stu-id="96a62-2786">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="96a62-2787">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="96a62-2787">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="96a62-2788">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="96a62-2788">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="96a62-2789">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="96a62-2789">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="96a62-2790">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="96a62-2790">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="96a62-2791">1.6.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="96a62-2791">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="96a62-2792">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="96a62-2792">Highlights since the last major release</span></span>
* <span data-ttu-id="96a62-2793">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="96a62-2793">General availability of `Az` module</span></span>
* <span data-ttu-id="96a62-2794">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="96a62-2794">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="96a62-2795">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="96a62-2795">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="96a62-2796">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-2796">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="96a62-2797">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-2797">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="96a62-2798">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-2798">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="96a62-2799">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="96a62-2799">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="96a62-2800">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="96a62-2800">Az.Automation</span></span>
* <span data-ttu-id="96a62-2801">Azure Automation – ändring av uppdateringshantering för stöd för de nya funktionerna:</span><span class="sxs-lookup"><span data-stu-id="96a62-2801">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="96a62-2802">Dynamisk gruppering</span><span class="sxs-lookup"><span data-stu-id="96a62-2802">Dynamic grouping</span></span>
    * <span data-ttu-id="96a62-2803">För-/efterskrift</span><span class="sxs-lookup"><span data-stu-id="96a62-2803">Pre-Post script</span></span>
    * <span data-ttu-id="96a62-2804">Inställning för omstart</span><span class="sxs-lookup"><span data-stu-id="96a62-2804">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="96a62-2805">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="96a62-2805">Az.Compute</span></span>
* <span data-ttu-id="96a62-2806">Åtgärda problem med sökvägsmatchning i Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="96a62-2806">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="96a62-2807">Uppdatera Compute-klientbibliotek till 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="96a62-2807">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="96a62-2808">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="96a62-2808">Az.KeyVault</span></span>
* <span data-ttu-id="96a62-2809">Stöd för jokertecken för KeyVault-cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-2809">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="96a62-2810">Az.Network</span><span class="sxs-lookup"><span data-stu-id="96a62-2810">Az.Network</span></span>
* <span data-ttu-id="96a62-2811">Lägg till stöd för Threat Intelligence för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="96a62-2811">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="96a62-2812">Lägg till resurs för brandväggsprincip på översta nivå och anpassade regler för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="96a62-2812">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="96a62-2813">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="96a62-2813">Az.RecoveryServices</span></span>
* <span data-ttu-id="96a62-2814">SnapshotRetentionInDays har lagts till i Azure-principen för virtuella datorer för stöd av Instant RP</span><span class="sxs-lookup"><span data-stu-id="96a62-2814">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="96a62-2815">Pipe-stöd för avregistrering av container har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-2815">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="96a62-2816">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="96a62-2816">Az.Resources</span></span>
* <span data-ttu-id="96a62-2817">Uppdatera stöd för jokertecken för Get-AzResource och Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="96a62-2817">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="96a62-2818">Uppdatera autentiseringsuppgifter som används vid allmänna anrop till ARM</span><span class="sxs-lookup"><span data-stu-id="96a62-2818">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="96a62-2819">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="96a62-2819">Az.Sql</span></span>
* <span data-ttu-id="96a62-2820">Cmdlet-parametern (ExcludeDetectionType) för Hotidentifiering ändrades från DetectionType till sträng[] för att framtidssäkra den när nya DetectionTypes läggs till, och även för att stödja automatisk ifyllning.</span><span class="sxs-lookup"><span data-stu-id="96a62-2820">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="96a62-2821">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="96a62-2821">Az.Storage</span></span>
* <span data-ttu-id="96a62-2822">Stöd för att hämta/ange/ta bort hanteringsprincip på ett lagringskonto</span><span class="sxs-lookup"><span data-stu-id="96a62-2822">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="96a62-2823">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="96a62-2823">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="96a62-2824">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="96a62-2824">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="96a62-2825">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="96a62-2825">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="96a62-2826">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="96a62-2826">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="96a62-2827">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="96a62-2827">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="96a62-2828">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="96a62-2828">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="96a62-2829">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="96a62-2829">Az.Websites</span></span>
* <span data-ttu-id="96a62-2830">Åtgärda fel med ARM-mall som avbryter kloning av alla platser med 'New-AzWebApp -IncludeSourceWebAppSlots'</span><span class="sxs-lookup"><span data-stu-id="96a62-2830">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="96a62-2831">1.5.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="96a62-2831">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="96a62-2832">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="96a62-2832">Az.Accounts</span></span>
* <span data-ttu-id="96a62-2833">Lägg till kommandot Register-AzModule för stöd för AutoRest-genererade cmdletar</span><span class="sxs-lookup"><span data-stu-id="96a62-2833">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="96a62-2834">Uppdatera exempel för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="96a62-2834">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="96a62-2835">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="96a62-2835">Az.Automation</span></span>
* <span data-ttu-id="96a62-2836">Problem med att hämta vissa månadsscheman i flera Azure Automation-cmdletar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="96a62-2836">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="96a62-2837">Åtgärda problem med att Get-AzAutomationDscNode bara returnerar de 20 översta noderna.</span><span class="sxs-lookup"><span data-stu-id="96a62-2837">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="96a62-2838">Nu returneras alla noder</span><span class="sxs-lookup"><span data-stu-id="96a62-2838">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="96a62-2839">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="96a62-2839">Az.Cdn</span></span>
* <span data-ttu-id="96a62-2840">Nya Powershell-cmdletar för att aktivera/inaktivera anpassade domän-HTTPS har lagts till och de gamla har gjorts inaktuella</span><span class="sxs-lookup"><span data-stu-id="96a62-2840">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="96a62-2841">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="96a62-2841">Az.Compute</span></span>
* <span data-ttu-id="96a62-2842">Lägg till stöd för jokertecken för Get-cmdletar</span><span class="sxs-lookup"><span data-stu-id="96a62-2842">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="96a62-2843">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="96a62-2843">Az.DataFactory</span></span>
* <span data-ttu-id="96a62-2844">ADF .Net SDK-versionen har uppdaterats till 3.0.1</span><span class="sxs-lookup"><span data-stu-id="96a62-2844">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="96a62-2845">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="96a62-2845">Az.LogicApp</span></span>
* <span data-ttu-id="96a62-2846">Åtgärda problemet med att ListWorkflows endast hämtar den första sidan med resultat</span><span class="sxs-lookup"><span data-stu-id="96a62-2846">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="96a62-2847">Az.Network</span><span class="sxs-lookup"><span data-stu-id="96a62-2847">Az.Network</span></span>
* <span data-ttu-id="96a62-2848">Lägg till stöd för jokertecken för Network-cmdletar</span><span class="sxs-lookup"><span data-stu-id="96a62-2848">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="96a62-2849">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="96a62-2849">Az.RecoveryServices</span></span>
* <span data-ttu-id="96a62-2850">Stöd har lagts till för SQL Server i virtuella Azure-datorer</span><span class="sxs-lookup"><span data-stu-id="96a62-2850">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="96a62-2851">SDK-uppdatering</span><span class="sxs-lookup"><span data-stu-id="96a62-2851">SDK Update</span></span>
* <span data-ttu-id="96a62-2852">Get-ProtectableItem-incheckning i VMappContainer har tagits bort</span><span class="sxs-lookup"><span data-stu-id="96a62-2852">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="96a62-2853">Name och ServerName har lagts till som parametrar för Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="96a62-2853">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="96a62-2854">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="96a62-2854">Az.Resources</span></span>
* <span data-ttu-id="96a62-2855">Lägg till parametern `-TemplateObject` i cmdletar för distribution</span><span class="sxs-lookup"><span data-stu-id="96a62-2855">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="96a62-2856">Mer information här: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="96a62-2856">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="96a62-2857">Åtgärda problem med piping av resultatet i `Get-AzResource` till `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="96a62-2857">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="96a62-2858">Mer information här: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="96a62-2858">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="96a62-2859">Åtgärda problem med ändring av JSON-datatyp när `Set-AzResource` körs</span><span class="sxs-lookup"><span data-stu-id="96a62-2859">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="96a62-2860">Mer information här: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="96a62-2860">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="96a62-2861">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="96a62-2861">Az.Sql</span></span>
* <span data-ttu-id="96a62-2862">AuditingEndpointsCommunicator uppdateras.</span><span class="sxs-lookup"><span data-stu-id="96a62-2862">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="96a62-2863">Åtgärdar beteendet hos ett gränsscenario när nya diagnostikinställningar skapas.</span><span class="sxs-lookup"><span data-stu-id="96a62-2863">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="96a62-2864">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="96a62-2864">Az.Storage</span></span>
* <span data-ttu-id="96a62-2865">Stöd för BlockBlobStorage när Storage-konto skapas      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="96a62-2865">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="96a62-2866">1.4.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="96a62-2866">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="96a62-2867">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="96a62-2867">Az.AnalysisServices</span></span>
* <span data-ttu-id="96a62-2868">Inaktuell AddAzureASAccount-cmdlet</span><span class="sxs-lookup"><span data-stu-id="96a62-2868">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="96a62-2869">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="96a62-2869">Az.Automation</span></span>
* <span data-ttu-id="96a62-2870">Hjälpen för Import-AzAutomationDscNodeConfiguration har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="96a62-2870">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="96a62-2871">Konfigurationsnamnsvalidering har lagts till i cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="96a62-2871">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="96a62-2872">Förbättrad felhantering för cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="96a62-2872">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="96a62-2873">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="96a62-2873">Az.CognitiveServices</span></span>
* <span data-ttu-id="96a62-2874">CustomSubdomainName har lagts till som en ny valfri parameter för New-AzCognitiveServicesAccount, som används för att ange underdomän för resursen.</span><span class="sxs-lookup"><span data-stu-id="96a62-2874">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="96a62-2875">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="96a62-2875">Az.Compute</span></span>
* <span data-ttu-id="96a62-2876">Problemet med ID-parameteruppsättningar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="96a62-2876">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="96a62-2877">Get-AzVMExtension har uppdaterats så att alla installerade tillägg visas om parametern Name inte har angetts</span><span class="sxs-lookup"><span data-stu-id="96a62-2877">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="96a62-2878">Parametrarna Tag och ResourceId har lagts till i cmdleten Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="96a62-2878">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="96a62-2879">Get-AzVmssVM utan instans-ID och med InstanceView kan visa virtuella VMSS-datorer med instansvyn.</span><span class="sxs-lookup"><span data-stu-id="96a62-2879">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="96a62-2880">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="96a62-2880">Az.DataLakeStore</span></span>
* <span data-ttu-id="96a62-2881">Cmdletar har lagts till för uppräkning och återställning av borttagna objekt i ADL</span><span class="sxs-lookup"><span data-stu-id="96a62-2881">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="96a62-2882">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="96a62-2882">Az.EventHub</span></span>
* <span data-ttu-id="96a62-2883">Ny boolesk egenskap SkipEmptyArchives har lagts till i Skip Empty Archives i CaptureDescription-klassen i Eventhub</span><span class="sxs-lookup"><span data-stu-id="96a62-2883">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="96a62-2884">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="96a62-2884">Az.KeyVault</span></span>
* <span data-ttu-id="96a62-2885">Taggning i Set-AzKeyVaultSecret har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="96a62-2885">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="96a62-2886">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="96a62-2886">Az.LogicApp</span></span>
* <span data-ttu-id="96a62-2887">Grundläggande SKU har lagts till för Integrationskonton</span><span class="sxs-lookup"><span data-stu-id="96a62-2887">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="96a62-2888">XSLT 2.0, XSLT 3.0 och Flytande mappningstyper har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-2888">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="96a62-2889">Nya cmdletar för integrationskontosammansättningar</span><span class="sxs-lookup"><span data-stu-id="96a62-2889">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="96a62-2890">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="96a62-2890">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="96a62-2891">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="96a62-2891">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="96a62-2892">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="96a62-2892">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="96a62-2893">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="96a62-2893">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="96a62-2894">Nya cmdletar för batchkonfiguration för integrationskonto</span><span class="sxs-lookup"><span data-stu-id="96a62-2894">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="96a62-2895">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="96a62-2895">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="96a62-2896">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="96a62-2896">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="96a62-2897">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="96a62-2897">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="96a62-2898">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="96a62-2898">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="96a62-2899">Logic App-SDK har uppdaterats till version 4.1.0</span><span class="sxs-lookup"><span data-stu-id="96a62-2899">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="96a62-2900">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="96a62-2900">Az.Monitor</span></span>
* <span data-ttu-id="96a62-2901">Hjälpen för Get-AzMetric har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="96a62-2901">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="96a62-2902">Az.Network</span><span class="sxs-lookup"><span data-stu-id="96a62-2902">Az.Network</span></span>
* <span data-ttu-id="96a62-2903">Hjälpexempel för Add-AzApplicationGatewayCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-2903">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="96a62-2904">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="96a62-2904">Az.OperationalInsights</span></span>
* <span data-ttu-id="96a62-2905">Ytterligare stöd för datakällorna New och Get ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="96a62-2905">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="96a62-2906">Ny ApplicationInsights-typ har lagts till för att ge stöd för ”Get specific” och ”Get all” för ApplicationInsights-datakällor för angiven arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="96a62-2906">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="96a62-2907">Cmdleten New-AzOperationalInsightsApplicationInsightsDataSource har lagts till för att skapa datakälla med angivna parametrar för Application Insights-resurs: subscription Id, resourceGroupName och name.</span><span class="sxs-lookup"><span data-stu-id="96a62-2907">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="96a62-2908">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="96a62-2908">Az.Resources</span></span>
* <span data-ttu-id="96a62-2909">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="96a62-2909">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="96a62-2910">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="96a62-2910">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="96a62-2911">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="96a62-2911">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="96a62-2912">Fel som gör att KeyCredentials inte kan skapas upprepade gånger har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="96a62-2912">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="96a62-2913">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="96a62-2913">Az.Sql</span></span>
* <span data-ttu-id="96a62-2914">Lägg till stöd för hyperskalanivån för SQL DB</span><span class="sxs-lookup"><span data-stu-id="96a62-2914">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="96a62-2915">Ett fel har åtgärdats där återställningen kunde misslyckas på grund av onödiga inställningsegenskaper i restore-förfrågan</span><span class="sxs-lookup"><span data-stu-id="96a62-2915">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="96a62-2916">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="96a62-2916">Az.Websites</span></span>
* <span data-ttu-id="96a62-2917">Rätt exempel i Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="96a62-2917">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="96a62-2918">1.3.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="96a62-2918">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="96a62-2919">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="96a62-2919">Az.Accounts</span></span>
* <span data-ttu-id="96a62-2920">Uppdatera till den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="96a62-2920">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="96a62-2921">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="96a62-2921">Az.AnalysisServices</span></span>
<span data-ttu-id="96a62-2922">Allmän tillgänglighet för Az.AnalysisServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="96a62-2922">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="96a62-2923">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="96a62-2923">Az.Compute</span></span>
* <span data-ttu-id="96a62-2924">AEM-tillägg: Lägg till stöd för UltraSSD-, P60-, P70- och P80-diskar</span><span class="sxs-lookup"><span data-stu-id="96a62-2924">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="96a62-2925">Uppdatera hjälpbeskrivning för Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="96a62-2925">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="96a62-2926">Uppdatera hjälpbeskrivning och exempel för Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="96a62-2926">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="96a62-2927">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="96a62-2927">Az.RecoveryServices</span></span>
<span data-ttu-id="96a62-2928">Allmän tillgänglighet för Az.RecoveryServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="96a62-2928">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="96a62-2929">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="96a62-2929">Az.Resources</span></span>
* <span data-ttu-id="96a62-2930">Korrigera taggar för resursgrupper</span><span class="sxs-lookup"><span data-stu-id="96a62-2930">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="96a62-2931">Mer information här: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="96a62-2931">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="96a62-2932">Åtgärda problem där `Get-AzureRmRoleAssignment` inte respekterar -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="96a62-2932">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="96a62-2933">Mer information här: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="96a62-2933">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="96a62-2934">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="96a62-2934">Az.Sql</span></span>
* <span data-ttu-id="96a62-2935">Lägga till Get/Set-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="96a62-2935">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="96a62-2936">Åtgärda problem där ett nullref-undantag uppstår när du kör SQL-cmdletar och inte är inloggad på ett Azure-konto</span><span class="sxs-lookup"><span data-stu-id="96a62-2936">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="96a62-2937">Åtgärda nullref-undantag i Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="96a62-2937">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="96a62-2938">1.2.1 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="96a62-2938">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="96a62-2939">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="96a62-2939">Az.Accounts</span></span>
* <span data-ttu-id="96a62-2940">Version med rätt version av autentisering</span><span class="sxs-lookup"><span data-stu-id="96a62-2940">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="96a62-2941">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="96a62-2941">Az.AnalysisServices</span></span>
* <span data-ttu-id="96a62-2942">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="96a62-2942">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="96a62-2943">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="96a62-2943">Az.RecoveryServices</span></span>
* <span data-ttu-id="96a62-2944">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="96a62-2944">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="96a62-2945">1.2.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="96a62-2945">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="96a62-2946">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="96a62-2946">Az.Accounts</span></span>
* <span data-ttu-id="96a62-2947">Lägga till interaktiv autentisering och autentisering med användarnamn/lösenord för endast Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="96a62-2947">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="96a62-2948">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="96a62-2948">Update incorrect online help URLs</span></span>
* <span data-ttu-id="96a62-2949">Lägga till varningsmeddelande i PS Core för Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="96a62-2949">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="96a62-2950">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="96a62-2950">Az.Aks</span></span>
* <span data-ttu-id="96a62-2951">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="96a62-2951">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="96a62-2952">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="96a62-2952">Az.Automation</span></span>
* <span data-ttu-id="96a62-2953">Stöd för Python 2-runbookflöden har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-2953">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="96a62-2954">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="96a62-2954">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="96a62-2955">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="96a62-2955">Az.Cdn</span></span>
* <span data-ttu-id="96a62-2956">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="96a62-2956">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="96a62-2957">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="96a62-2957">Az.Compute</span></span>
* <span data-ttu-id="96a62-2958">Lägga till cmdleten Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="96a62-2958">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="96a62-2959">Lägga till TempDisk-parameter i Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="96a62-2959">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="96a62-2960">Korrigera varningsmeddelande för New-AzVM</span><span class="sxs-lookup"><span data-stu-id="96a62-2960">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="96a62-2961">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="96a62-2961">Az.ContainerRegistry</span></span>
* <span data-ttu-id="96a62-2962">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="96a62-2962">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="96a62-2963">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="96a62-2963">Az.DataFactory</span></span>
* <span data-ttu-id="96a62-2964">ADF .Net SDK-versionen har uppdaterats till 3.0.0</span><span class="sxs-lookup"><span data-stu-id="96a62-2964">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="96a62-2965">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="96a62-2965">Az.DataLakeStore</span></span>
* <span data-ttu-id="96a62-2966">Åtgärda problem med ADLS-slutpunkt vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="96a62-2966">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="96a62-2967">Mer information här: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="96a62-2967">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="96a62-2968">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="96a62-2968">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="96a62-2969">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="96a62-2969">Az.IotHub</span></span>
* <span data-ttu-id="96a62-2970">Lägga till kodningsformat i cmdleten Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="96a62-2970">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="96a62-2971">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="96a62-2971">Az.KeyVault</span></span>
* <span data-ttu-id="96a62-2972">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="96a62-2972">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="96a62-2973">Az.Network</span><span class="sxs-lookup"><span data-stu-id="96a62-2973">Az.Network</span></span>
* <span data-ttu-id="96a62-2974">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="96a62-2974">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="96a62-2975">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="96a62-2975">Az.Resources</span></span>
* <span data-ttu-id="96a62-2976">Åtgärda felaktiga exempel i referensdokumentationen ”New-AzADAppCredential” och ”New-AzADSpCredential”</span><span class="sxs-lookup"><span data-stu-id="96a62-2976">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="96a62-2977">Åtgärda problem där sökvägen för parametern ”-TemplateFile” inte omvandlas innan cmdletarna för distribution i resursgruppen körs</span><span class="sxs-lookup"><span data-stu-id="96a62-2977">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="96a62-2978">Az.Resources: Korrigera dokumentationen om standardvärdet för New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="96a62-2978">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="96a62-2979">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="96a62-2979">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="96a62-2980">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="96a62-2980">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="96a62-2981">Åtgärda formateringsproblemet med objektet ”PSResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="96a62-2981">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="96a62-2982">Mer information här: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="96a62-2982">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="96a62-2983">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="96a62-2983">Az.ServiceFabric</span></span>
* <span data-ttu-id="96a62-2984">Återställ när ett certifikat läggs till i en Virtual Machine Scale Sets-modell men ett undantag genereras. Detta har gjorts för att åtgärda följande fel: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="96a62-2984">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="96a62-2985">Korrigera några felmeddelanden.</span><span class="sxs-lookup"><span data-stu-id="96a62-2985">Fix some error messages.</span></span>
* <span data-ttu-id="96a62-2986">Korrigering av skapande av kluster med ARM-mall som är standard för New-AzServiceFabriCluster som inte fungerade med migrering till Az.</span><span class="sxs-lookup"><span data-stu-id="96a62-2986">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="96a62-2987">Korrigering av tilläggning av kluster/programcertifikat så att endast VM Scale Sets som motsvarar klustret läggs till genom att kontrollera ID för klustret i tillägget.</span><span class="sxs-lookup"><span data-stu-id="96a62-2987">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="96a62-2988">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="96a62-2988">Az.SignalR</span></span>
* <span data-ttu-id="96a62-2989">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="96a62-2989">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="96a62-2990">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="96a62-2990">Az.Sql</span></span>
* <span data-ttu-id="96a62-2991">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="96a62-2991">Update incorrect online help URLs</span></span>
* <span data-ttu-id="96a62-2992">Uppdaterad parameterbeskrivning för LicenseType-parameter med möjliga värden</span><span class="sxs-lookup"><span data-stu-id="96a62-2992">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="96a62-2993">Korrigering för att uppdatera hanterad instansidentitet som inte fungerar när det är den enda uppdaterade egenskapen</span><span class="sxs-lookup"><span data-stu-id="96a62-2993">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="96a62-2994">Stöd för anpassad sortering på hanterad instans</span><span class="sxs-lookup"><span data-stu-id="96a62-2994">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="96a62-2995">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="96a62-2995">Az.Storage</span></span>
* <span data-ttu-id="96a62-2996">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="96a62-2996">Update incorrect online help URLs</span></span>
* <span data-ttu-id="96a62-2997">Tillhandahåll detaljerat felmeddelande när en användare försöker hämta/konfigurera klassisk loggning/mått på ett Premium Storage-konto eftersom Premium Storage-kontot inte har stöd för klassisk loggning/mått.</span><span class="sxs-lookup"><span data-stu-id="96a62-2997">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="96a62-2998">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="96a62-2998">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="96a62-2999">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="96a62-2999">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="96a62-3000">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="96a62-3000">Az.TrafficManager</span></span>
* <span data-ttu-id="96a62-3001">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="96a62-3001">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="96a62-3002">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="96a62-3002">Az.Websites</span></span>
* <span data-ttu-id="96a62-3003">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="96a62-3003">Update incorrect online help URLs</span></span>
* <span data-ttu-id="96a62-3004">Korrigerar ”New-AzWebAppSSLBinding” så att certifikatet laddas upp till rätt resursgrupp och plats om appen finns i en ASE.</span><span class="sxs-lookup"><span data-stu-id="96a62-3004">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="96a62-3005">Korrigerar ”New-AzWebAppSSLBinding” så att taggarna inte skrivs över på en bindning av ett SSL-certifikat till en app</span><span class="sxs-lookup"><span data-stu-id="96a62-3005">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="96a62-3006">1.1.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="96a62-3006">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="96a62-3007">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="96a62-3007">Az.Accounts</span></span>
* <span data-ttu-id="96a62-3008">Lade till omfattningen ”Lokal” till Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="96a62-3008">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="96a62-3009">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="96a62-3009">Az.Compute</span></span>
* <span data-ttu-id="96a62-3010">Namn är nu valfritt i ID-parametern för Restart/Start/Stop/Remove/Set-AzVM och Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="96a62-3010">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="96a62-3011">Uppdaterade beskrivningen av ID i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="96a62-3011">Updated the description of ID in help files</span></span>
* <span data-ttu-id="96a62-3012">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="96a62-3012">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="96a62-3013">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="96a62-3013">Az.DataLakeStore</span></span>
* <span data-ttu-id="96a62-3014">Uppdatera sdk-versionen av dataplanet till 1.1.14 för SDK-korrigeringar.</span><span class="sxs-lookup"><span data-stu-id="96a62-3014">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="96a62-3015">Korrigerade hanteringen av negativ accesstime och modificationtime för getfilestatus och liststatus; korrigera asynkront annulleringstoken</span><span class="sxs-lookup"><span data-stu-id="96a62-3015">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="96a62-3016">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="96a62-3016">Az.EventGrid</span></span>
* <span data-ttu-id="96a62-3017">Uppdaterat för användning av API-versionen 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="96a62-3017">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="96a62-3018">Uppdaterade följande cmdletar för att stödja nytt scenario i API-versionen 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="96a62-3018">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="96a62-3019">New-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="96a62-3019">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="96a62-3020">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="96a62-3020">Event Time-To-Live,</span></span>
        - <span data-ttu-id="96a62-3021">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="96a62-3021">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="96a62-3022">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="96a62-3022">Dead letter endpoint.</span></span>
    - <span data-ttu-id="96a62-3023">Update-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="96a62-3023">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="96a62-3024">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="96a62-3024">Event Time-To-Live,</span></span>
        - <span data-ttu-id="96a62-3025">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="96a62-3025">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="96a62-3026">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="96a62-3026">Dead letter endpoint.</span></span>
* <span data-ttu-id="96a62-3027">Lade till nya enum-värden (storageQueue och hybridConnection) för alternativet EndpointType i cmdletarna New-AzureRmEventGridSubscription och Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="96a62-3027">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="96a62-3028">Visa varningsmeddelanden om skapande eller uppdatering av händelseprenumerationen förväntas medföra manuell åtgärd från användaren.</span><span class="sxs-lookup"><span data-stu-id="96a62-3028">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="96a62-3029">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="96a62-3029">Az.IotHub</span></span>
* <span data-ttu-id="96a62-3030">Har uppdaterats till den senaste versionen av SDK:n lotHub</span><span class="sxs-lookup"><span data-stu-id="96a62-3030">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="96a62-3031">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="96a62-3031">Az.LogicApp</span></span>
* <span data-ttu-id="96a62-3032">Get-AzLogicApp visar en lista över alla som inte har angivet namn</span><span class="sxs-lookup"><span data-stu-id="96a62-3032">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="96a62-3033">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="96a62-3033">Az.Resources</span></span>
* <span data-ttu-id="96a62-3034">Åtgärdade problem med parameteruppsättningen när parametrarna -ODataQuery och -ResourceId anges för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="96a62-3034">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="96a62-3035">Mer information här: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="96a62-3035">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="96a62-3036">Åtgärdade hantering av parametern -Custom i New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="96a62-3036">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="96a62-3037">Korrigerade stavfel i New-AzDeployment-dokumentationen</span><span class="sxs-lookup"><span data-stu-id="96a62-3037">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="96a62-3038">Gjorde parametern -MailNickname obligatorisk för New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="96a62-3038">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="96a62-3039">Mer information här: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="96a62-3039">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="96a62-3040">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="96a62-3040">Az.SignalR</span></span>
* <span data-ttu-id="96a62-3041">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="96a62-3041">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="96a62-3042">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="96a62-3042">Az.Sql</span></span>
* <span data-ttu-id="96a62-3043">Konverterade lagringshanteringsklientens beroende av den normala SDK-implementeringen.</span><span class="sxs-lookup"><span data-stu-id="96a62-3043">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="96a62-3044">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="96a62-3044">Az.Storage</span></span>
* <span data-ttu-id="96a62-3045">Angav StorageAccountName för lagringskontext som det verkliga namnet på lagringskontot när det skapas med Sas Token, OAuth eller Anonymous</span><span class="sxs-lookup"><span data-stu-id="96a62-3045">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="96a62-3046">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="96a62-3046">New-AzStorageContext</span></span>
* <span data-ttu-id="96a62-3047">Skapade Sas Token för Blob Snapshot-objekt med parametern -FullUri, åtgärdade den returnerade URI:n så att den blir URI för ögonblicksbild</span><span class="sxs-lookup"><span data-stu-id="96a62-3047">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="96a62-3048">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="96a62-3048">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="96a62-3049">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="96a62-3049">Az.Websites</span></span>
* <span data-ttu-id="96a62-3050">Åtgärdade en bugg i datumparsningen i Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="96a62-3050">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="96a62-3051">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="96a62-3051">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="96a62-3052">1.0.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="96a62-3052">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="96a62-3053">Allmänt</span><span class="sxs-lookup"><span data-stu-id="96a62-3053">General</span></span>

- <span data-ttu-id="96a62-3054">Allmän tillgänglighet för Az-modulen</span><span class="sxs-lookup"><span data-stu-id="96a62-3054">General Availability of Az Module</span></span>
- <span data-ttu-id="96a62-3055">Onlinehjälp för varje modul</span><span class="sxs-lookup"><span data-stu-id="96a62-3055">Online help for each module</span></span>
- <span data-ttu-id="96a62-3056">Mer information och en översikt finns på [Az-informationssidan](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="96a62-3056">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="96a62-3057">Information om hur du migrerar från AzureRM finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="96a62-3057">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="96a62-3058">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="96a62-3058">Az.Accounts</span></span>
- <span data-ttu-id="96a62-3059">Har ändrats från Az.Profile</span><span class="sxs-lookup"><span data-stu-id="96a62-3059">Changed from Az.Profile</span></span>
- <span data-ttu-id="96a62-3060">Fasta tabellformat för profil- och kontexttyper</span><span class="sxs-lookup"><span data-stu-id="96a62-3060">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="96a62-3061">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="96a62-3061">Az.ApiManagement</span></span>
- <span data-ttu-id="96a62-3062">Korrigeringar för #7002</span><span class="sxs-lookup"><span data-stu-id="96a62-3062">Fixes for #7002</span></span>
- <span data-ttu-id="96a62-3063">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="96a62-3063">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="96a62-3064">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="96a62-3064">Az.Batch</span></span>
- <span data-ttu-id="96a62-3065">Lade till möjligheten att se vilken version av Azure Batch Node Agent som körs på var och en av de virtuella datorerna i en pool, via den nya egenskapen `NodeAgentInformation` på `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="96a62-3065">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="96a62-3066">Standarden `Caching` för `PSDataDisk` är nu `ReadWrite` i stället för `None`.</span><span class="sxs-lookup"><span data-stu-id="96a62-3066">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="96a62-3067">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="96a62-3067">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="96a62-3068">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="96a62-3068">Az.Billing</span></span>
- <span data-ttu-id="96a62-3069">Kombinerar cmdletarna för fakturering, förbrukning och UsageAggregates. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="96a62-3069">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="96a62-3070">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="96a62-3070">Az.CognitivServices</span></span>
- <span data-ttu-id="96a62-3071">Lade till kompletterare för SkuName och Typem som är tillgängliga i New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="96a62-3071">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="96a62-3072">Tog bort parameteruppsättningen GetSkusWithAccountParamSetName från Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="96a62-3072">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="96a62-3073">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="96a62-3073">Az.ContainerInstance</span></span>
- <span data-ttu-id="96a62-3074">Stöd för ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="96a62-3074">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="96a62-3075">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="96a62-3075">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="96a62-3076">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="96a62-3076">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="96a62-3077">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="96a62-3077">Az.DataLakeStore</span></span>
- <span data-ttu-id="96a62-3078">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="96a62-3078">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="96a62-3079">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="96a62-3079">Az.Monitor</span></span>
- <span data-ttu-id="96a62-3080">Döpte om Az.Insights till Az.Monitor och andra mindre icke-bakåtkompatibla ändringar. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="96a62-3080">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="96a62-3081">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="96a62-3081">Az.KeyVault</span></span>
- <span data-ttu-id="96a62-3082">Tog bort den inaktuella egenskapen PurgeDisabled från utdatatyper</span><span class="sxs-lookup"><span data-stu-id="96a62-3082">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="96a62-3083">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="96a62-3083">Az.MachineLearning</span></span>
- <span data-ttu-id="96a62-3084">Inkluderade cmdletarna från modulen Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="96a62-3084">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="96a62-3085">Az.Media</span><span class="sxs-lookup"><span data-stu-id="96a62-3085">Az.Media</span></span>
- <span data-ttu-id="96a62-3086">Tog bort inaktuella -Tags-alias från New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="96a62-3086">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="96a62-3087">Az.Network</span><span class="sxs-lookup"><span data-stu-id="96a62-3087">Az.Network</span></span>
<span data-ttu-id="96a62-3088">Stöd har lagts till för konfiguration av RewriteRuleSets i Application Gateway</span><span class="sxs-lookup"><span data-stu-id="96a62-3088">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="96a62-3089">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="96a62-3089">New cmdlets added:</span></span>
        - <span data-ttu-id="96a62-3090">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="96a62-3090">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="96a62-3091">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="96a62-3091">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="96a62-3092">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="96a62-3092">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="96a62-3093">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="96a62-3093">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="96a62-3094">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="96a62-3094">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="96a62-3095">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="96a62-3095">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="96a62-3096">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="96a62-3096">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="96a62-3097">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="96a62-3097">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="96a62-3098">Cmdletar har uppdaterats med den valfria parametern -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="96a62-3098">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="96a62-3099">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="96a62-3099">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="96a62-3100">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="96a62-3100">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="96a62-3101">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="96a62-3101">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="96a62-3102">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="96a62-3102">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="96a62-3103">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="96a62-3103">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="96a62-3104">New-AzureRmApplicationGatewayUrlPathMapConfig har lagt till KeyVault-stöd för Application Gateway med Identity.</span><span class="sxs-lookup"><span data-stu-id="96a62-3104">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="96a62-3105">Cmdletar har uppdaterats med den valfria parametern -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="96a62-3105">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="96a62-3106">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="96a62-3106">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="96a62-3107">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="96a62-3107">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="96a62-3108">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="96a62-3108">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="96a62-3109">Cmdleten New-AzApplicationGateway har uppdaterats med den valfria parametern -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="96a62-3109">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="96a62-3110">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="96a62-3110">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="96a62-3111">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="96a62-3111">Az.OperationalInsights</span></span>
- <span data-ttu-id="96a62-3112">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="96a62-3112">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="96a62-3113">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="96a62-3113">Az.Profile</span></span>
- <span data-ttu-id="96a62-3114">Modulnamnet har ändrats till Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="96a62-3114">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="96a62-3115">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="96a62-3115">Az.RecoveryServices</span></span>
- <span data-ttu-id="96a62-3116">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="96a62-3116">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="96a62-3117">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="96a62-3117">Az.Resources</span></span>
- <span data-ttu-id="96a62-3118">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="96a62-3118">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="96a62-3119">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="96a62-3119">Az.ServiceFabric</span></span>
- <span data-ttu-id="96a62-3120">Stöd för specificering av certifikat efter eget namn och tumavtryck</span><span class="sxs-lookup"><span data-stu-id="96a62-3120">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="96a62-3121">Information om fler icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="96a62-3121">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="96a62-3122">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="96a62-3122">Az.SIgnalR</span></span>
- <span data-ttu-id="96a62-3123">Allmän tillgänglighet för PowerShell-cmdletar för SIgnalR</span><span class="sxs-lookup"><span data-stu-id="96a62-3123">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="96a62-3124">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="96a62-3124">Az.Sql</span></span>
- <span data-ttu-id="96a62-3125">Lade till de nya identifieringstyperna Data_Exfiltration och Unsafe_Action i Threat Detection-cmdletar</span><span class="sxs-lookup"><span data-stu-id="96a62-3125">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="96a62-3126">Uppdaterade dokumentationsexempel för Sql Auditing-cmdletar</span><span class="sxs-lookup"><span data-stu-id="96a62-3126">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="96a62-3127">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="96a62-3127">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="96a62-3128">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="96a62-3128">Az.Storage</span></span>
- <span data-ttu-id="96a62-3129">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="96a62-3129">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="96a62-3130">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="96a62-3130">Az.Websites</span></span>
- <span data-ttu-id="96a62-3131">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="96a62-3131">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="96a62-3132">0.7.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="96a62-3132">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="96a62-3133">Allmänt</span><span class="sxs-lookup"><span data-stu-id="96a62-3133">General</span></span>

* <span data-ttu-id="96a62-3134">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="96a62-3134">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="96a62-3135">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="96a62-3135">Az.Compute</span></span>

* <span data-ttu-id="96a62-3136">Lade till stöd för UltraSSD och Galleriavbildningar i de enkla parameteruppsättningarna för `New-AzVm(ss)`-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="96a62-3136">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="96a62-3137">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="96a62-3137">Az.DataLakeStore</span></span>

* <span data-ttu-id="96a62-3138">Åtgärdade avslutande snedstreck i domänen för adls-konto</span><span class="sxs-lookup"><span data-stu-id="96a62-3138">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="96a62-3139">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="96a62-3139">Az.FrontDoor</span></span>

* <span data-ttu-id="96a62-3140">Brutna länkar korrigerades</span><span class="sxs-lookup"><span data-stu-id="96a62-3140">Fixed some broken links</span></span>
    - <span data-ttu-id="96a62-3141">I artiklarna New-AzureRmFrontDoor och Set-AzureRmFrontDoor artiklar korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="96a62-3141">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="96a62-3142">I artikeln New-AzureRmFrontDoorManagedRuleObject korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="96a62-3142">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="96a62-3143">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="96a62-3143">Az.RecoveryServices</span></span>

* <span data-ttu-id="96a62-3144">Lade till valideringar på klientsidan för Azure-filresurs med återställningsåtgärder.</span><span class="sxs-lookup"><span data-stu-id="96a62-3144">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="96a62-3145">Gjorde storageAccountName och storageAccountResourceGroupName valfritt för afs-återställning.</span><span class="sxs-lookup"><span data-stu-id="96a62-3145">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="96a62-3146">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="96a62-3146">Az.Resources</span></span>

* <span data-ttu-id="96a62-3147">Korrigering för https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="96a62-3147">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="96a62-3148">Uppdaterade Get-AzureRmRoleAssignment så att prenumerationsomfattningen används om den anges vid begäran om klassiska administratörer.</span><span class="sxs-lookup"><span data-stu-id="96a62-3148">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="96a62-3149">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="96a62-3149">Az.Sql</span></span>

* <span data-ttu-id="96a62-3150">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="96a62-3150">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="96a62-3151">Korrigerade ett problem med Get-AzureRmSqlDatabaseVulnerabilityAssessment med DotNet-kärna</span><span class="sxs-lookup"><span data-stu-id="96a62-3151">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="96a62-3152">Ändrade dokumentationen för hjälpmeddelanden som rör SQL Auditing-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="96a62-3152">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="96a62-3153">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="96a62-3153">Az.Storage</span></span>

* <span data-ttu-id="96a62-3154">Lade till -EnableHierarchicalNamespace i New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="96a62-3154">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="96a62-3155">Åtgärdade problemet med att cmdleten Copy File inte kunde återanvända källkontexten på målet om inte -DestContext angetts</span><span class="sxs-lookup"><span data-stu-id="96a62-3155">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="96a62-3156">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="96a62-3156">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="96a62-3157">Stöd för statisk webbplatskonfiguration</span><span class="sxs-lookup"><span data-stu-id="96a62-3157">Support Static Website configuration</span></span>
    - <span data-ttu-id="96a62-3158">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="96a62-3158">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="96a62-3159">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="96a62-3159">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="96a62-3160">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="96a62-3160">Az.Websites</span></span>

* <span data-ttu-id="96a62-3161">Set-AzureRmWebApp och Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="96a62-3161">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="96a62-3162">Ny parameter (-AzureStoragePath) har lagts till för att ange att Azure Storage-sökvägar ska monteras i containerappar i Windows och Linux.</span><span class="sxs-lookup"><span data-stu-id="96a62-3162">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="96a62-3163">Använder utdata från den nya cmdleten New-AzureRmWebAppAzureStoragePath som en parameter för att ange sökvägar för Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="96a62-3163">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="96a62-3164">0.6.1 – november 2018</span><span class="sxs-lookup"><span data-stu-id="96a62-3164">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="96a62-3165">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="96a62-3165">Az.ApiManagement</span></span>
* <span data-ttu-id="96a62-3166">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="96a62-3166">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="96a62-3167">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="96a62-3167">Az.Automation</span></span>
* <span data-ttu-id="96a62-3168">Swagger baserade Azure Automation-cmdletar</span><span class="sxs-lookup"><span data-stu-id="96a62-3168">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="96a62-3169">Cmdletar för Uppdateringshantering har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-3169">Added Update Management cmdlets</span></span>
* <span data-ttu-id="96a62-3170">Cmdletar för källkontroll har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-3170">Added Source Control cmdlets</span></span>
* <span data-ttu-id="96a62-3171">Remove-AzureRmAutomationHybridWorkerGroup-cmdlet har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-3171">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="96a62-3172">Kommandot för DSC-registreringsnod har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="96a62-3172">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="96a62-3173">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="96a62-3173">Az.Compute</span></span>
* <span data-ttu-id="96a62-3174">Problem med SystemAssigned-identitet har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="96a62-3174">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="96a62-3175">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="96a62-3175">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="96a62-3176">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="96a62-3176">Az.ContainerInstance</span></span>
* <span data-ttu-id="96a62-3177">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="96a62-3177">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="96a62-3178">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="96a62-3178">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="96a62-3179">uppdatera exempelbeskrivningen för marketplace-cmdletar</span><span class="sxs-lookup"><span data-stu-id="96a62-3179">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="96a62-3180">Az.Network</span><span class="sxs-lookup"><span data-stu-id="96a62-3180">Az.Network</span></span>
* <span data-ttu-id="96a62-3181">Cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomErreller Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-3181">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="96a62-3182">ICMP tillbaka till stöd för Azure Firewall-nätverksprotokoll har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-3182">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="96a62-3183">Uppdatera cmdlet Test-AzureRmNetworkWatcherConnectivity, lägga till verifiering av mål-id, adress och port.</span><span class="sxs-lookup"><span data-stu-id="96a62-3183">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="96a62-3184">Åtgärda problem med minnesanvändning i VirtualNetwork-karta</span><span class="sxs-lookup"><span data-stu-id="96a62-3184">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="96a62-3185">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="96a62-3185">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="96a62-3186">Åtgärda för att ändra principen för en skyddad fildelning.</span><span class="sxs-lookup"><span data-stu-id="96a62-3186">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="96a62-3187">Tidszonsprincipen har konverterats till versaler.</span><span class="sxs-lookup"><span data-stu-id="96a62-3187">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="96a62-3188">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="96a62-3188">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="96a62-3189">Exempel i New-AzureRmRecoveryServicesAsrProtectableItem har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="96a62-3189">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="96a62-3190">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="96a62-3190">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="96a62-3191">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="96a62-3191">Az.Relay</span></span>
* <span data-ttu-id="96a62-3192">Valfri parameter -KeyValue till New-AzureRmRelayKey cmdlet har lagts till, vilket gör det möjligt för användare att tillhandahålla KeyValue.</span><span class="sxs-lookup"><span data-stu-id="96a62-3192">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="96a62-3193">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="96a62-3193">Az.Resources</span></span>
* <span data-ttu-id="96a62-3194">Uppdatera hjälpdokumentation för resursidentitet kopplad till parametrar i `New-AzureRmPolicyAssignment` och `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="96a62-3194">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="96a62-3195">Lägg till ett exempel för New-AzureRmPolicyDefinition som använder -Metadata</span><span class="sxs-lookup"><span data-stu-id="96a62-3195">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="96a62-3196">Korrigera så att skiftläge behålls i taggnycklar i NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="96a62-3196">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="96a62-3197">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="96a62-3197">Az.ServiceFabric</span></span>
* <span data-ttu-id="96a62-3198">Lägg till utfasningsmeddelanden för kommande icke-kompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="96a62-3198">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="96a62-3199">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="96a62-3199">Az.Sql</span></span>
* <span data-ttu-id="96a62-3200">Nya cmdletar för CRUD-åtgärder på Azure Sql Database-hanterad instans och Azure Sql-hanterad databas</span><span class="sxs-lookup"><span data-stu-id="96a62-3200">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="96a62-3201">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="96a62-3201">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="96a62-3202">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="96a62-3202">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="96a62-3203">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="96a62-3203">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="96a62-3204">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="96a62-3204">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="96a62-3205">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="96a62-3205">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="96a62-3206">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="96a62-3206">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="96a62-3207">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="96a62-3207">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="96a62-3208">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="96a62-3208">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="96a62-3209">Hantering av utökad granskningsprincip på en server eller en databas har aktiverats.</span><span class="sxs-lookup"><span data-stu-id="96a62-3209">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="96a62-3210">Ny parameter (PredicateExpression) har lagts till för att aktivera filtrering av granskningsloggar.</span><span class="sxs-lookup"><span data-stu-id="96a62-3210">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="96a62-3211">Cmdletar har ändrats så att de använder SQL-klienter i stället för äldre klienter.</span><span class="sxs-lookup"><span data-stu-id="96a62-3211">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="96a62-3212">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="96a62-3212">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="96a62-3213">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="96a62-3213">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="96a62-3214">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="96a62-3214">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="96a62-3215">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="96a62-3215">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="96a62-3216">Problem med att använda Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings med lagringskontots namnparameter har korrigerats</span><span class="sxs-lookup"><span data-stu-id="96a62-3216">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="96a62-3217">0.5.0 – november 2018</span><span class="sxs-lookup"><span data-stu-id="96a62-3217">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="96a62-3218">Allmänt</span><span class="sxs-lookup"><span data-stu-id="96a62-3218">General</span></span>
* <span data-ttu-id="96a62-3219">Lade till resurskompletterare till många kärn-cmdletar – dessa gör att du kan stega genom befintliga resursnamn med TABB vid interaktiva anrop till cmdletar</span><span class="sxs-lookup"><span data-stu-id="96a62-3219">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="96a62-3220">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="96a62-3220">Az.Profile</span></span>
* <span data-ttu-id="96a62-3221">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="96a62-3221">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="96a62-3222">Bytte namn på parametern TenantId i cmdleten Connect-AzAccount till Tenant och lade till ett alias för TenantId</span><span class="sxs-lookup"><span data-stu-id="96a62-3222">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="96a62-3223">Uppdaterade TenantId-beskrivningen för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="96a62-3223">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="96a62-3224">Åtgärda felmeddelande för misslyckad inloggning när du tillhandahåller klientdomän</span><span class="sxs-lookup"><span data-stu-id="96a62-3224">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="96a62-3225">Åtgärda problem med att kontextnamn hamnar i konflikt för konton utan prenumerationer i klientorganisationen</span><span class="sxs-lookup"><span data-stu-id="96a62-3225">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="96a62-3226">Åtgärda problem med DataLake-slutpunkter vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="96a62-3226">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="96a62-3227">Åtgärdade problem med att Disconnect-AzAccount kastades om den inte anslöts</span><span class="sxs-lookup"><span data-stu-id="96a62-3227">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="96a62-3228">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="96a62-3228">Az.CognitiveServices</span></span>
* <span data-ttu-id="96a62-3229">Lade till åtgärden Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="96a62-3229">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="96a62-3230">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="96a62-3230">Az.Compute</span></span>
* <span data-ttu-id="96a62-3231">Lade till cmdletarna Add-AzVmssVMDataDisk och Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="96a62-3231">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="96a62-3232">Get-AzVMImage visar AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="96a62-3232">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="96a62-3233">Åtgärdade att värdena för alternativen SetAzVMChefExtension -BootstrapOptions och -JsonAttribute inte angavs i json-format.</span><span class="sxs-lookup"><span data-stu-id="96a62-3233">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="96a62-3234">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="96a62-3234">Az.DataLakeStore</span></span>
* <span data-ttu-id="96a62-3235">Uppdatera DataLake-paketet till 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="96a62-3235">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="96a62-3236">Lägg till standardsamtidighet för flertrådade åtgärder.</span><span class="sxs-lookup"><span data-stu-id="96a62-3236">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="96a62-3237">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="96a62-3237">Az.Insights</span></span>
* <span data-ttu-id="96a62-3238">Åtgärdade problem #7267 (autoskalningsområde)</span><span class="sxs-lookup"><span data-stu-id="96a62-3238">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="96a62-3239">Problem med att uppräknade parametrar inte ställdes in ordentligt när du skapade en ny autoskalningsregel (de ställdes alltid in med standardvärdet).</span><span class="sxs-lookup"><span data-stu-id="96a62-3239">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="96a62-3240">Åtgärdade problem #7513 [Insights] Set-AzDiagnosticSetting kräver uttrycklig specifikation av kategorier när inställningar skapas</span><span class="sxs-lookup"><span data-stu-id="96a62-3240">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="96a62-3241">Nu kräver inte cmdleten uttrycklig anvisning av kategorierna för att aktiveras under skapande, d.v.s. den fungerar enligt beskrivning</span><span class="sxs-lookup"><span data-stu-id="96a62-3241">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="96a62-3242">Az.Network</span><span class="sxs-lookup"><span data-stu-id="96a62-3242">Az.Network</span></span>
* <span data-ttu-id="96a62-3243">PeeringType ändrades till en obligatorisk parameter för följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="96a62-3243">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="96a62-3244">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="96a62-3244">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="96a62-3245">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="96a62-3245">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="96a62-3246">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="96a62-3246">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="96a62-3247">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="96a62-3247">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="96a62-3248">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="96a62-3248">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="96a62-3249">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="96a62-3249">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="96a62-3250">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="96a62-3250">Az.PolicyInsights</span></span>
* <span data-ttu-id="96a62-3251">Cmdletar för principreparation har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-3251">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="96a62-3252">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="96a62-3252">Az.Resources</span></span>
* <span data-ttu-id="96a62-3253">Korrigering för https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="96a62-3253">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="96a62-3254">Tillåt att resurser listas med parametern -ResourceId för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="96a62-3254">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="96a62-3255">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="96a62-3255">Az.ServiceBus</span></span>
* <span data-ttu-id="96a62-3256">Skrivskyddad MigrationState-egenskap har lagts till i PSServiceBusMigrationConfigurationAttributes, som hjälper till att hålla koll på migreringstillståndet.</span><span class="sxs-lookup"><span data-stu-id="96a62-3256">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="96a62-3257">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="96a62-3257">Az.ServiceFabric</span></span>
* <span data-ttu-id="96a62-3258">Åtgärda att lägga till certifikat till Linux-Vmss.</span><span class="sxs-lookup"><span data-stu-id="96a62-3258">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="96a62-3259">Åtgärdade Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="96a62-3259">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="96a62-3260">Använd rätt tumavtryck från nya certifikat (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="96a62-3260">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="96a62-3261">Visa undantag korrekt (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="96a62-3261">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="96a62-3262">Åtgärdade Update-AzServiceFabricDurability så att klusterkonfigurationen uppdateras innan Vmss-åtgärden CreateOrUpdate påbörjas.</span><span class="sxs-lookup"><span data-stu-id="96a62-3262">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="96a62-3263">0.4.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="96a62-3263">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="96a62-3264">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="96a62-3264">Az.Profile</span></span>
* <span data-ttu-id="96a62-3265">Åtgärdade problemet med Get-AzSubscription i CloudShell</span><span class="sxs-lookup"><span data-stu-id="96a62-3265">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="96a62-3266">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="96a62-3266">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="96a62-3267">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="96a62-3267">Az.Compute</span></span>
* <span data-ttu-id="96a62-3268">Nya storlekar lades till i listan över godkända VM-storlekar för vilka accelererat nätverk kommer att aktiveras vid användning av den enkla parameteruppsättningen för New-AzVm</span><span class="sxs-lookup"><span data-stu-id="96a62-3268">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="96a62-3269">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="96a62-3269">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="96a62-3270">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="96a62-3270">Az.DataLakeStore</span></span>
* <span data-ttu-id="96a62-3271">Lägger till stöd för regler för virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="96a62-3271">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="96a62-3272">Get-AzDataLakeStoreVirtualNetworkRule: Hämtar eller listar regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="96a62-3272">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="96a62-3273">Add-AzDataLakeStoreVirtualNetworkRule: Lägger till en regel för virtuellt nätverk i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="96a62-3273">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="96a62-3274">Set-AzDataLakeStoreVirtualNetworkRule: Ändrar den angivna regeln för virtuellt nätverk i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="96a62-3274">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="96a62-3275">Remove-AzDataLakeStoreVirtualNetworkRule: Tar bort en regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="96a62-3275">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="96a62-3276">Az.Network</span><span class="sxs-lookup"><span data-stu-id="96a62-3276">Az.Network</span></span>
* <span data-ttu-id="96a62-3277">Skicka protokollvärdet till serverdelen för att uppdatera cmdleten Test-AzNetworkWatcherConnectivity.</span><span class="sxs-lookup"><span data-stu-id="96a62-3277">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="96a62-3278">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="96a62-3278">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="96a62-3279">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="96a62-3279">Az.Resources</span></span>
* <span data-ttu-id="96a62-3280">Åtgärdade problem där Get-AzRoleDefinition genererar ett oläsligt undantag (när standardprofilen inte innehåller någon prenumeration och ingen omfattning har angetts) genom att lägga till ett beskrivande undantag i scenariot.</span><span class="sxs-lookup"><span data-stu-id="96a62-3280">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="96a62-3281">Ställ in ”RoleDefinitionNameParameterSet” som standardparameteruppsättning.</span><span class="sxs-lookup"><span data-stu-id="96a62-3281">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="96a62-3282">0.3.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="96a62-3282">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="96a62-3283">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="96a62-3283">Azure.Storage</span></span>
* <span data-ttu-id="96a62-3284">Åtgärda fel där Kopiera blob/fil inte kopierar metadata när målplatsen har ett problem med metadata</span><span class="sxs-lookup"><span data-stu-id="96a62-3284">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="96a62-3285">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="96a62-3285">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="96a62-3286">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="96a62-3286">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="96a62-3287">Stöd för att hämta användningsinformation om en Storage-resurs för en specifik plats och för att lägga till ett varningsmeddelande för att hämta användningsinformation om en global Storage-resurs är inaktuellt.</span><span class="sxs-lookup"><span data-stu-id="96a62-3287">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="96a62-3288">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="96a62-3288">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="96a62-3289">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="96a62-3289">Az.CognitiveServices</span></span>
* <span data-ttu-id="96a62-3290">Stöd för Get-AzCognitiveServicesAccountSkus utan ett befintligt konto.</span><span class="sxs-lookup"><span data-stu-id="96a62-3290">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="96a62-3291">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="96a62-3291">Az.Compute</span></span>
* <span data-ttu-id="96a62-3292">Åtgärdade fel där Get-AzVM -ResourceGroupName <rg> returnerar fler än 50 resultat om det behövs</span><span class="sxs-lookup"><span data-stu-id="96a62-3292">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="96a62-3293">Lade till ett exempel för SimpleParameterSet i hjälpen för cmdleten New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="96a62-3293">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="96a62-3294">Ett stavfel i förloppsmeddelandet för Azure Disk Encryption har korrigerats</span><span class="sxs-lookup"><span data-stu-id="96a62-3294">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="96a62-3295">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="96a62-3295">Az.DataFactoryV2</span></span>
* <span data-ttu-id="96a62-3296">ADF .Net SDK-versionen har uppdaterats till 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="96a62-3296">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="96a62-3297">Az.Network</span><span class="sxs-lookup"><span data-stu-id="96a62-3297">Az.Network</span></span>
* <span data-ttu-id="96a62-3298">Funktionalitet för NetworkProfile har lagts till.</span><span class="sxs-lookup"><span data-stu-id="96a62-3298">Added NetworkProfile functionality.</span></span> <span data-ttu-id="96a62-3299">nya cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-3299">new cmdlets added</span></span>
    - <span data-ttu-id="96a62-3300">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="96a62-3300">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="96a62-3301">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="96a62-3301">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="96a62-3302">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="96a62-3302">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="96a62-3303">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="96a62-3303">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="96a62-3304">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="96a62-3304">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="96a62-3305">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="96a62-3305">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="96a62-3306">Länk för tjänstassociering på modell för undernät har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-3306">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="96a62-3307">Cmdletarna New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap och Remove-AzVirtualNetworkTap har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-3307">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="96a62-3308">Cmdletarna Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig och Remove-AzNEtworkInterfaceTapConfig har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-3308">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="96a62-3309">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="96a62-3309">Az.RedisCache</span></span>
* <span data-ttu-id="96a62-3310">Tillåt att alla strängar används som storleksparametrar framöver.</span><span class="sxs-lookup"><span data-stu-id="96a62-3310">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="96a62-3311">Lägg till P5 i popup-fönstret PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="96a62-3311">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="96a62-3312">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="96a62-3312">Az.Resources</span></span>
* <span data-ttu-id="96a62-3313">Parametern -Mode som saknades i Set-AzPolicyDefinition har lagts till</span><span class="sxs-lookup"><span data-stu-id="96a62-3313">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="96a62-3314">Åtgärdade buggen för cmdleten Get-AzProviderOperation för åtgärder med ursprung som innehåller användare</span><span class="sxs-lookup"><span data-stu-id="96a62-3314">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="96a62-3315">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="96a62-3315">Az.Sql</span></span>
* <span data-ttu-id="96a62-3316">Ett problem där vissa cmdletar för säkerhetskopiering inte kunde identifiera den aktuella azure-prenumerationen har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="96a62-3316">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="96a62-3317">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="96a62-3317">Az.Websites</span></span>
* <span data-ttu-id="96a62-3318">Ny cmdlet: Get-AzWebAppContainerContinuousDeploymentUrl – Hämtar webhook-URL:en för kontinuerlig distribution av container</span><span class="sxs-lookup"><span data-stu-id="96a62-3318">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="96a62-3319">Nya cmdletar: New-AzWebAppContainerPSSession och Enter-WebAppContainerPSSession – Startar en PowerShell-fjärrsession i en containerapp för windows</span><span class="sxs-lookup"><span data-stu-id="96a62-3319">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="96a62-3320">0.2.0 – september 2018</span><span class="sxs-lookup"><span data-stu-id="96a62-3320">0.2.0 - September 2018</span></span>
 <span data-ttu-id="96a62-3321">Första versionen</span><span class="sxs-lookup"><span data-stu-id="96a62-3321">Initial Release</span></span>
