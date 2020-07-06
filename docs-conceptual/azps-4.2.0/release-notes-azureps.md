---
title: Viktig information om Azure PowerShell
description: Lär dig mer om alla de senaste uppdateringarna för Azure PowerShell-modulerna.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.openlocfilehash: a9ec7589ab155553da29612096a607d82a078321
ms.sourcegitcommit: 5523170e571fbd1dc93bd0fa4223aba3b324d3b0
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/25/2020
ms.locfileid: "85363701"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="f9e89-103">Viktig information om Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="f9e89-103">Azure PowerShell release notes</span></span>

## <a name="430---june-2020"></a><span data-ttu-id="f9e89-104">4.3.0 – juni 2020</span><span class="sxs-lookup"><span data-stu-id="f9e89-104">4.3.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f9e89-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f9e89-105">Az.Accounts</span></span>
* <span data-ttu-id="f9e89-106">Stöd för identifiering av miljöinställning som standard och tillägg av miljön via ”Add-AzEnvironment”</span><span class="sxs-lookup"><span data-stu-id="f9e89-106">Supported discovering environment setting by default and adding environment via 'Add-AzEnvironment'</span></span>
* <span data-ttu-id="f9e89-107">Uppdatera förinlästa sammansättningar [#12024], [#11976]</span><span class="sxs-lookup"><span data-stu-id="f9e89-107">Update preloaded assemblies [#12024], [#11976]</span></span>
* <span data-ttu-id="f9e89-108">Uppdaterad Azure.Core-sammansättning</span><span class="sxs-lookup"><span data-stu-id="f9e89-108">Updated Azure.Core assembly</span></span>
* <span data-ttu-id="f9e89-109">Ett problem har åtgärdats som kan orsaka att ”Connect-AzAccount” misslyckas vid körning av flera trådar [#11201]</span><span class="sxs-lookup"><span data-stu-id="f9e89-109">Fixed an issue that may cause 'Connect-AzAccount' to fail in multi-threaded execution [#11201]</span></span>

#### <a name="azaks"></a><span data-ttu-id="f9e89-110">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="f9e89-110">Az.Aks</span></span>
* <span data-ttu-id="f9e89-111">Användning av gamla [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) ersattes med anrop till API:erna [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) och [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials)</span><span class="sxs-lookup"><span data-stu-id="f9e89-111">Replaced usage of old [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) with calls to [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) and [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials) APIs</span></span>

#### <a name="azbatch"></a><span data-ttu-id="f9e89-112">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="f9e89-112">Az.Batch</span></span>
* <span data-ttu-id="f9e89-113">Az.Batch har uppdaterats att använda ”Microsoft.Azure.Management.Batch” SDK till och med version 11.0.0.</span><span class="sxs-lookup"><span data-stu-id="f9e89-113">Updated Az.Batch to use 'Microsoft.Azure.Management.Batch' SDK version to 11.0.0</span></span>
* <span data-ttu-id="f9e89-114">Möjligheten att ange BatchAccount-identiteten har lagts till i cmdleten ”New-AzBatchAccount”</span><span class="sxs-lookup"><span data-stu-id="f9e89-114">Added the ability to set the BatchAccount Identity in the 'New-AzBatchAccount' cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f9e89-115">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f9e89-115">Az.CognitiveServices</span></span>
* <span data-ttu-id="f9e89-116">Stöd för att visa kontofunktioner.</span><span class="sxs-lookup"><span data-stu-id="f9e89-116">Supported displaying account capabilities.</span></span>
* <span data-ttu-id="f9e89-117">Stöd för att ändra PublicNetworkAccess.</span><span class="sxs-lookup"><span data-stu-id="f9e89-117">Supported modifying PublicNetworkAccess.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f9e89-118">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f9e89-118">Az.Compute</span></span>
* <span data-ttu-id="f9e89-119">Parametern SimulateEviction har lagts till i cmdletarna set-AzVM och set-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="f9e89-119">Added SimulateEviction parameter to Set-AzVM and Set-AzVmssVM cmdlets.</span></span>
* <span data-ttu-id="f9e89-120">”Premium_LRS” har lagts till i argumentslutföraren för parametern StorageAccountType för cmdleten New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="f9e89-120">Added 'Premium_LRS' to the argument completer of StorageAccountType parameter for New-AzGalleryImageVersion cmdlet.</span></span>
* <span data-ttu-id="f9e89-121">Understatusar har lagts till i VMCustomScriptExtension [#11297]</span><span class="sxs-lookup"><span data-stu-id="f9e89-121">Added Substatuses to VMCustomScriptExtension [#11297]</span></span>
* <span data-ttu-id="f9e89-122">”Delete” har lagts till i argumentslutföraren för parametern EvictionPolicy för cmdletarna New-AzVM och New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="f9e89-122">Added 'Delete' to the argument completer of EvictionPolicy parameter for New-AzVM and New-AzVMConfig cmdlets.</span></span>
* <span data-ttu-id="f9e89-123">Åtgärdat namn för nytt VM-tillägg för SAP</span><span class="sxs-lookup"><span data-stu-id="f9e89-123">Fixed name of new VM Extension for SAP</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f9e89-124">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f9e89-124">Az.DataFactory</span></span>
* <span data-ttu-id="f9e89-125">ADF .Net SDK har uppdaterats till 4.9.0</span><span class="sxs-lookup"><span data-stu-id="f9e89-125">Updated ADF .Net SDK version to 4.9.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f9e89-126">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f9e89-126">Az.EventHub</span></span>
* <span data-ttu-id="f9e89-127">Parametrar för hanterad identitet har lagts till i cmdletarna ”New-AzEventHubNamespace” och ”set-AzEventHubNamespace”</span><span class="sxs-lookup"><span data-stu-id="f9e89-127">Added Managed Identity parameters to 'New-AzEventHubNamespace' and 'Set-AzEventHubNamespace' cmdlets</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="f9e89-128">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="f9e89-128">Az.Functions</span></span>
* <span data-ttu-id="f9e89-129">Stöd har lagts till för att skapa PowerShell 7.0- och Java 11-funktionsappar</span><span class="sxs-lookup"><span data-stu-id="f9e89-129">Added support to create PowerShell 7.0 and Java 11 function apps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="f9e89-130">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f9e89-130">Az.HDInsight</span></span>
* <span data-ttu-id="f9e89-131">Stöd för listning av värdar och omstart för specifika värdar i HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="f9e89-131">Supported listing hosts and restart specific hosts of the HDInsight cluster.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="f9e89-132">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="f9e89-132">Az.HealthcareApis</span></span>
* <span data-ttu-id="f9e89-133">Uppdaterade SDK-versionen till 1.1.0</span><span class="sxs-lookup"><span data-stu-id="f9e89-133">Updated the SDK version to 1.1.0</span></span>
* <span data-ttu-id="f9e89-134">Stöd har lagts till för exportinställningar och hanterad identitet</span><span class="sxs-lookup"><span data-stu-id="f9e89-134">Added support for Export settings and Managed Identity</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f9e89-135">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f9e89-135">Az.Monitor</span></span>
* <span data-ttu-id="f9e89-136">Parameter för inmatningsobjekt har åtgärdats för ”Set-AzActivityLogAlert”</span><span class="sxs-lookup"><span data-stu-id="f9e89-136">Fixed input object parameter for 'Set-AzActivityLogAlert'</span></span>
* <span data-ttu-id="f9e89-137">Parametern ”InputObject” har åtgärdats för ”Set-AzActionGroup” [#10868]</span><span class="sxs-lookup"><span data-stu-id="f9e89-137">Fixed 'InputObject' parameter for 'Set-AzActionGroup' [#10868]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f9e89-138">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f9e89-138">Az.Network</span></span>
* <span data-ttu-id="f9e89-139">Stöd har lagts till för parametern AddressPrefixType i ”Remove-AzExpressRouteCircuitConnectionConfig”</span><span class="sxs-lookup"><span data-stu-id="f9e89-139">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="f9e89-140">Nya cmdletar har lagts till för Azure FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="f9e89-140">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="f9e89-141">”New-AzFirewallPolicyDnsSetting”</span><span class="sxs-lookup"><span data-stu-id="f9e89-141">'New-AzFirewallPolicyDnsSetting'</span></span>
    - <span data-ttu-id="f9e89-142">Stöd för mål-FQDN i nätverksregler för brandväggsprincip</span><span class="sxs-lookup"><span data-stu-id="f9e89-142">Support for Destination FQDN in Network Rules for Firewall Policy</span></span>
* <span data-ttu-id="f9e89-143">Stöd har lagts till för åtgärder i serverdelsadresspooler</span><span class="sxs-lookup"><span data-stu-id="f9e89-143">Added support for backend address pool operations</span></span>
    - <span data-ttu-id="f9e89-144">”New-AzLoadBalancerBackendAddressConfig”</span><span class="sxs-lookup"><span data-stu-id="f9e89-144">'New-AzLoadBalancerBackendAddressConfig'</span></span>
    - <span data-ttu-id="f9e89-145">”New-AzLoadBalancerBackendAddressPool”</span><span class="sxs-lookup"><span data-stu-id="f9e89-145">'New-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="f9e89-146">”Set-AzLoadBalancerBackendAddressPool”</span><span class="sxs-lookup"><span data-stu-id="f9e89-146">'Set-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="f9e89-147">”Remove-AzLoadBalancerBackendAddressPool”</span><span class="sxs-lookup"><span data-stu-id="f9e89-147">'Remove-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="f9e89-148">”Get-AzLoadBalancerBackendAddressPool”</span><span class="sxs-lookup"><span data-stu-id="f9e89-148">'Get-AzLoadBalancerBackendAddressPool'</span></span>
* <span data-ttu-id="f9e89-149">Namnvalidering har lagts till för ”New-AzIpGroup”</span><span class="sxs-lookup"><span data-stu-id="f9e89-149">Added name validation for 'New-AzIpGroup'</span></span>
* <span data-ttu-id="f9e89-150">Nya cmdletar har lagts till för Azure FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="f9e89-150">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="f9e89-151">”New-AzFirewallPolicyThreatIntelWhitelist”</span><span class="sxs-lookup"><span data-stu-id="f9e89-151">'New-AzFirewallPolicyThreatIntelWhitelist'</span></span>
* <span data-ttu-id="f9e89-152">Nedanstående kommandon för funktionen har uppdaterats: Konfiguration/borttagning av anpassade DNS-servrar på VirtualWan P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="f9e89-152">Updated below commands for feature: Custom dns servers set/remove on VirtualWan P2SVpnGateway.</span></span>
    - <span data-ttu-id="f9e89-153">New-AzP2sVpnGateway har uppdaterats: Den valfria parametern ”-CustomDnsServer” har lagts till för att kunder ska kunna ange att deras DNS-servrar ska konfigureras på P2SVpnGateway, som kan användas av punkt-till-plats-klienter.</span><span class="sxs-lookup"><span data-stu-id="f9e89-153">Updated New-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
    - <span data-ttu-id="f9e89-154">Update-AzP2sVpnGateway har uppdaterats: Den valfria parametern ”-CustomDnsServer” har lagts till för att kunder ska kunna ange att deras DNS-servrar ska konfigureras på P2SVpnGateway, som kan användas av punkt-till-plats-klienter.</span><span class="sxs-lookup"><span data-stu-id="f9e89-154">Updated Update-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
* <span data-ttu-id="f9e89-155">”Update-AzVpnGateway” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="f9e89-155">Updated 'Update-AzVpnGateway'</span></span>
    - <span data-ttu-id="f9e89-156">Den valfria parametern ”-BgpPeeringAddress” har lagts till för att kunder ska kunna ange sina anpassade BGP:er som ska konfigurerar på VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="f9e89-156">Added optional parameter '-BgpPeeringAddress' for customers to specify their custom bgps to set on VpnGateway.</span></span>
* <span data-ttu-id="f9e89-157">Ny cmdlet har lagts till för att stödja återställning av en VirtualHub-resurs routningsstatus:</span><span class="sxs-lookup"><span data-stu-id="f9e89-157">Added new cmdlet to support resetting the routing state of a VirtualHub resource:</span></span>
    - <span data-ttu-id="f9e89-158">”Reset-AzHubRouter”</span><span class="sxs-lookup"><span data-stu-id="f9e89-158">'Reset-AzHubRouter'</span></span>
* <span data-ttu-id="f9e89-159">Nedanstående saker har uppdaterats baserat på den senaste Swagger-ändringen för brandväggspolicyn</span><span class="sxs-lookup"><span data-stu-id="f9e89-159">Updated below things based on recent swagger change for Firewall Policy</span></span>
    - <span data-ttu-id="f9e89-160">Namn ändras för RuleGroup, RuleCollectionGroup och RuleType</span><span class="sxs-lookup"><span data-stu-id="f9e89-160">Changes names for RuleGroup, RuleCollectionGroup and RuleType</span></span>
    - <span data-ttu-id="f9e89-161">Stöd har lagts till för NAT-regelsamlingar för brandväggsprincip så att flera NAT-regelsamlingar stöds</span><span class="sxs-lookup"><span data-stu-id="f9e89-161">Added support for Firewall Policy NAT Rule Collections to support multiple NAT Rule Collection</span></span>
* <span data-ttu-id="f9e89-162">[Icke-bakåtkompatibel ändring] Den obligatoriska parametern ”SourceIpGroup” har lagts till för ”New-AzFirewallPolicyApplicationRule” och ”New-AzFirewallPolicyNetworkRule”.</span><span class="sxs-lookup"><span data-stu-id="f9e89-162">[Breaking Change] Added mandatory parameter 'SourceIpGroup' for 'New-AzFirewallPolicyApplicationRule' and 'New-AzFirewallPolicyNetworkRule'.</span></span>
* <span data-ttu-id="f9e89-163">[Icke-bakåtkompatibel ändring] ”New-AzFirewallPolicyApplicationRule” har åtgärdats, parametern ”SourceAddress” är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="f9e89-163">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="f9e89-164">[Icke-bakåtkompatibel ändring] ”New-AzFirewallPolicyApplicationRule” har åtgärdats, parametern ”SourceAddress” är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="f9e89-164">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="f9e89-165">[Icke-bakåtkompatibel ändring] Obligatoriska parametrar har tagits bort: ”TranslatedAddress”, ”TranslatedPort” för ”New-AzFirewallPolicyNatRuleCollection”.</span><span class="sxs-lookup"><span data-stu-id="f9e89-165">[Breaking Change] Removed mandatory parameters: 'TranslatedAddress', 'TranslatedPort' for 'New-AzFirewallPolicyNatRuleCollection'.</span></span>
* <span data-ttu-id="f9e89-166">Nya cmdletar har lagts till för att stödja PrivateLink på Application Gateway</span><span class="sxs-lookup"><span data-stu-id="f9e89-166">Added new cmdlets to support PrivateLink On Application Gateway</span></span>
    - <span data-ttu-id="f9e89-167">”New-AzApplicationGatewayPrivateLinkConfiguration”</span><span class="sxs-lookup"><span data-stu-id="f9e89-167">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="f9e89-168">”Get-AzApplicationGatewayPrivateLinkConfiguration”</span><span class="sxs-lookup"><span data-stu-id="f9e89-168">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="f9e89-169">”New-AzApplicationGatewayPrivateLinkConfiguration”</span><span class="sxs-lookup"><span data-stu-id="f9e89-169">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="f9e89-170">”Set-AzApplicationGatewayPrivateLinkConfiguration”</span><span class="sxs-lookup"><span data-stu-id="f9e89-170">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="f9e89-171">”Remove-AzApplicationGatewayPrivateLinkConfiguration”</span><span class="sxs-lookup"><span data-stu-id="f9e89-171">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="f9e89-172">”New-AzApplicationGatewayPrivateLinkIpConfiguration”</span><span class="sxs-lookup"><span data-stu-id="f9e89-172">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span></span>
* <span data-ttu-id="f9e89-173">Nya cmdletar har lagts till för VirtualHubs underordnade resurs HubRouteTables.</span><span class="sxs-lookup"><span data-stu-id="f9e89-173">Added new cmdlets for HubRouteTables child resource of VirtualHub.</span></span>
    - <span data-ttu-id="f9e89-174">”New-AzVHubRoute”</span><span class="sxs-lookup"><span data-stu-id="f9e89-174">'New-AzVHubRoute'</span></span>
    - <span data-ttu-id="f9e89-175">”New-AzVHubRouteTable”</span><span class="sxs-lookup"><span data-stu-id="f9e89-175">'New-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="f9e89-176">”Get-AzVHubRouteTable”</span><span class="sxs-lookup"><span data-stu-id="f9e89-176">'Get-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="f9e89-177">”Update-AzVHubRouteTable”</span><span class="sxs-lookup"><span data-stu-id="f9e89-177">'Update-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="f9e89-178">”Remove-AzVHubRouteTable”</span><span class="sxs-lookup"><span data-stu-id="f9e89-178">'Remove-AzVHubRouteTable'</span></span>
* <span data-ttu-id="f9e89-179">Befintliga cmdletar har uppdaterats för att stödja valfri RoutingConfiguration-indataparameter för anpassad routning i VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="f9e89-179">Updated existing cmdlets to support optional RoutingConfiguration input parameter for custom routing in VirtualWan.</span></span>
    - <span data-ttu-id="f9e89-180">”New-AzExpressRouteConnection”</span><span class="sxs-lookup"><span data-stu-id="f9e89-180">'New-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="f9e89-181">”Set-AzExpressRouteConnection”</span><span class="sxs-lookup"><span data-stu-id="f9e89-181">'Set-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="f9e89-182">”New-AzVirtualHubVnetConnection”</span><span class="sxs-lookup"><span data-stu-id="f9e89-182">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="f9e89-183">”Update-AzVirtualHubVnetConnection”</span><span class="sxs-lookup"><span data-stu-id="f9e89-183">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="f9e89-184">”New-AzVpnConnection”</span><span class="sxs-lookup"><span data-stu-id="f9e89-184">'New-AzVpnConnection'</span></span>
    - <span data-ttu-id="f9e89-185">”Update-AzVpnConnection”</span><span class="sxs-lookup"><span data-stu-id="f9e89-185">'Update-AzVpnConnection'</span></span>
    - <span data-ttu-id="f9e89-186">”New-AzP2sVpnGateway”</span><span class="sxs-lookup"><span data-stu-id="f9e89-186">'New-AzP2sVpnGateway'</span></span>
    - <span data-ttu-id="f9e89-187">”Update-AzP2sVpnGateway”</span><span class="sxs-lookup"><span data-stu-id="f9e89-187">'Update-AzP2sVpnGateway'</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f9e89-188">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f9e89-188">Az.OperationalInsights</span></span>
* <span data-ttu-id="f9e89-189">Fast fel PSWorkspace implementerar inte IOperationalInsightsWorkspace [#12135]</span><span class="sxs-lookup"><span data-stu-id="f9e89-189">Fixed bug PSWorkspace doesn't implement IOperationalInsightsWorkspace [#12135]</span></span>
* <span data-ttu-id="f9e89-190">”pergb2018” har lagts till i uppsättningen med giltiga värden för parametern ”Sku” i ”Set-AzOperationalInsightsWorkspace”</span><span class="sxs-lookup"><span data-stu-id="f9e89-190">Added 'pergb2018' to valid value set of parameter 'Sku' in 'Set-AzOperationalInsightsWorkspace'</span></span> 
* <span data-ttu-id="f9e89-191">Alias ”FunctionParameters” lades till för parametern ”FunctionParameter” till</span><span class="sxs-lookup"><span data-stu-id="f9e89-191">Added alias 'FunctionParameters' for parameter 'FunctionParameter' to</span></span>
    - <span data-ttu-id="f9e89-192">”New-AzOperationalInsightsSavedSearch”</span><span class="sxs-lookup"><span data-stu-id="f9e89-192">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="f9e89-193">”Set-AzOperationalInsightsSavedSearch”</span><span class="sxs-lookup"><span data-stu-id="f9e89-193">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f9e89-194">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f9e89-194">Az.RecoveryServices</span></span>
* <span data-ttu-id="f9e89-195">Azure Backup har fått stöd för att hämta MAB-objekt.</span><span class="sxs-lookup"><span data-stu-id="f9e89-195">Azure Backup added support for fetching MAB items.</span></span>
* <span data-ttu-id="f9e89-196">Azure Site Recovery stöder disktypen ”StandardSSD_LRS”</span><span class="sxs-lookup"><span data-stu-id="f9e89-196">Azure Site Recovery supports disk type 'StandardSSD_LRS'</span></span>

#### <a name="azresources"></a><span data-ttu-id="f9e89-197">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f9e89-197">Az.Resources</span></span>
* <span data-ttu-id="f9e89-198">”UsageLocation”, ”GivenName”, ”Surname”, ”AccountEnabled”, ”MailNickname”, ”Mail” på ”PSADUser” lades till [#10526] [#10497]</span><span class="sxs-lookup"><span data-stu-id="f9e89-198">Added 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' on 'PSADUser' [#10526] [#10497]</span></span>
* <span data-ttu-id="f9e89-199">Problem med att ”-Mail” inte fungerar på ”Get-AzADUser” har åtgärdats [#11981]</span><span class="sxs-lookup"><span data-stu-id="f9e89-199">Fixed issue that '-Mail' doesn't work on 'Get-AzADUser' [#11981]</span></span>
* <span data-ttu-id="f9e89-200">Parametern ”-ExcludeChangeType” har lagts till i ”Get-AzDeploymentWhatIfResult” och ”Get-AzResourceGroupDeploymentWhatIfResult”</span><span class="sxs-lookup"><span data-stu-id="f9e89-200">Added '-ExcludeChangeType' parameter to 'Get-AzDeploymentWhatIfResult' and 'Get-AzResourceGroupDeploymentWhatIfResult'</span></span>
* <span data-ttu-id="f9e89-201">Parametern ”-WhatIfExcludeChangeType” har lagts till i ”New-AzDeployment” och ”New-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="f9e89-201">Added '-WhatIfExcludeChangeType' parameter to 'New-AzDeployment' and 'New-AzResourceGroupDeployment'</span></span>
* <span data-ttu-id="f9e89-202">Cmdletar för ”Test-Az\*Deployment” har uppdaterats för att visa bättre felmeddelanden</span><span class="sxs-lookup"><span data-stu-id="f9e89-202">Updated 'Test-Az\*Deployment' cmdlets to show better error messages</span></span>
* <span data-ttu-id="f9e89-203">Hjälpmeddelandet för parametern ”-Name” i distributionsskapande och What If-cmdletar</span><span class="sxs-lookup"><span data-stu-id="f9e89-203">Fixed help message for '-Name' parameter of deployment create and What-If cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="f9e89-204">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f9e89-204">Az.Sql</span></span>
* <span data-ttu-id="f9e89-205">Stöd för tjänsthuvudnamn har lagts till för administratörs-cmdlet för SQL Server Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="f9e89-205">Added support for service principal for Set SQL Server Azure Active Directory Admin cmdlet</span></span>
* <span data-ttu-id="f9e89-206">Synkroniseringsproblem i Data Classification-cmdletar har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="f9e89-206">Fixed sync issue in Data Classification cmdlets.</span></span>
* <span data-ttu-id="f9e89-207">Stöd för att söka efter användare via e-postadress på ”Set-AzSqlServerActiveDirectoryAdministrator” [#12192]</span><span class="sxs-lookup"><span data-stu-id="f9e89-207">Supported searching user by mail on 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f9e89-208">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f9e89-208">Az.Storage</span></span>
* <span data-ttu-id="f9e89-209">Skapa lagringskonto med RequireInfrastructureEncryption stöds</span><span class="sxs-lookup"><span data-stu-id="f9e89-209">Supported create Storage account with RequireInfrastructureEncryption</span></span>
    -  <span data-ttu-id="f9e89-210">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="f9e89-210">'New-AzStorageAccount'</span></span>
* <span data-ttu-id="f9e89-211">Logiken för inläsning av Azure.Core flyttades till Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f9e89-211">Moved the logic of loading Azure.Core to Az.Accounts</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f9e89-212">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f9e89-212">Az.Websites</span></span>
* <span data-ttu-id="f9e89-213">Skydd för att ta bort skapad webapp om återställningen misslyckades har lagts till i ”Restore-AzDeletedWebApp”</span><span class="sxs-lookup"><span data-stu-id="f9e89-213">Added safeguard to delete created webapp if restore failed in 'Restore-AzDeletedWebApp'</span></span>
* <span data-ttu-id="f9e89-214">”SourceWebApp.Location” har lagts till för ”New-AzWebApp” och ”New-AzWebAppSlot”</span><span class="sxs-lookup"><span data-stu-id="f9e89-214">Added 'SourceWebApp.Location' for 'New-AzWebApp' and 'New-AzWebAppSlot'</span></span>
* <span data-ttu-id="f9e89-215">Fel som förhindrade ändring av containerinställningar i ”Set-AzWebApp” och ”Set-AzWebAppSlot” har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="f9e89-215">Fixed bug that prevented changing Container settings in 'Set-AzWebApp' and 'Set-AzWebAppSlot'</span></span>
* <span data-ttu-id="f9e89-216">Ett fel för att hämta SiteConfig när -Name inte anges för Get-AzWebApp har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="f9e89-216">Fixed bug to get SiteConfig when -Name is not given for Get-AzWebApp</span></span>
* <span data-ttu-id="f9e89-217">Stöd har lagts till för att skapa ASP för Linux-appar</span><span class="sxs-lookup"><span data-stu-id="f9e89-217">Added a support to create ASP for Linux Apps</span></span>
* <span data-ttu-id="f9e89-218">Undantag har lagts till för kloning över resursgrupper</span><span class="sxs-lookup"><span data-stu-id="f9e89-218">Added exceptions for clone across resource groups</span></span>

## <a name="420---june-2020"></a><span data-ttu-id="f9e89-219">4.2.0 – juni 2020</span><span class="sxs-lookup"><span data-stu-id="f9e89-219">4.2.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f9e89-220">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f9e89-220">Az.Accounts</span></span>
* <span data-ttu-id="f9e89-221">Åtgärdade ett problem som kan få Az att hoppa över loggar i Azure Automation- eller PowerShell-jobb [#11492]</span><span class="sxs-lookup"><span data-stu-id="f9e89-221">Fixed an issue that may cause Az to skip logs in Azure Automation or PowerShell jobs [#11492]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="f9e89-222">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f9e89-222">Az.AnalysisServices</span></span>
* <span data-ttu-id="f9e89-223">Uppdaterad sammansättningsversion för dataplan-cmdletar</span><span class="sxs-lookup"><span data-stu-id="f9e89-223">Updated assembly version of data plane cmdlets</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="f9e89-224">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f9e89-224">Az.ApiManagement</span></span>
* <span data-ttu-id="f9e89-225">Uppdaterad sammansättningsversion för cmdletar för tjänsthantering</span><span class="sxs-lookup"><span data-stu-id="f9e89-225">Updated assembly version of service management cmdlets</span></span>

#### <a name="azbilling"></a><span data-ttu-id="f9e89-226">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="f9e89-226">Az.Billing</span></span>
* <span data-ttu-id="f9e89-227">Uppdaterad sammansättningsversion för förbrukningscmdletar</span><span class="sxs-lookup"><span data-stu-id="f9e89-227">Updated assembly version of consumption cmdlets</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f9e89-228">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f9e89-228">Az.CognitiveServices</span></span>
* <span data-ttu-id="f9e89-229">Stöd för PrivateEndpoint- och PublicNetworkAccess-kontroll.</span><span class="sxs-lookup"><span data-stu-id="f9e89-229">Support PrivateEndpoint and PublicNetworkAccess control.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="f9e89-230">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f9e89-230">Az.DataFactory</span></span>
* <span data-ttu-id="f9e89-231">Uppdaterad sammansättningsversion för datafabrik V2-cmdletar</span><span class="sxs-lookup"><span data-stu-id="f9e89-231">Updated assembly version of data factory V2 cmdlets</span></span>

#### <a name="azdatashare"></a><span data-ttu-id="f9e89-232">Az.DataShare</span><span class="sxs-lookup"><span data-stu-id="f9e89-232">Az.DataShare</span></span>
* <span data-ttu-id="f9e89-233">Allmän tillgänglighet för modulen ”Az.DataShare”</span><span class="sxs-lookup"><span data-stu-id="f9e89-233">General availability of ''Az.DataShare'' module</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="f9e89-234">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="f9e89-234">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="f9e89-235">Allmän tillgänglighet för modulen ”Az.DesktopVirtualization”</span><span class="sxs-lookup"><span data-stu-id="f9e89-235">General availability of ''Az.DesktopVirtualization'' module</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f9e89-236">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f9e89-236">Az.OperationalInsights</span></span>
* <span data-ttu-id="f9e89-237">Uppgraderad SDK till 0.21.0</span><span class="sxs-lookup"><span data-stu-id="f9e89-237">Upgraded SDK to 0.21.0</span></span>
* <span data-ttu-id="f9e89-238">Lade till valfria parametrar till</span><span class="sxs-lookup"><span data-stu-id="f9e89-238">Added optional parameters to</span></span> 
    - <span data-ttu-id="f9e89-239">”New-AzOperationalInsightsSavedSearch”</span><span class="sxs-lookup"><span data-stu-id="f9e89-239">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="f9e89-240">”Set-AzOperationalInsightsSavedSearch”</span><span class="sxs-lookup"><span data-stu-id="f9e89-240">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f9e89-241">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f9e89-241">Az.PolicyInsights</span></span>
* <span data-ttu-id="f9e89-242">Korrigerade exempel 3 för ”Start-AzPolicyComplianceScan”</span><span class="sxs-lookup"><span data-stu-id="f9e89-242">Corrected example 3 for 'Start-AzPolicyComplianceScan'</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="f9e89-243">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="f9e89-243">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="f9e89-244">Uppdaterad sammansättningsversion för PowerBI-cmdletar</span><span class="sxs-lookup"><span data-stu-id="f9e89-244">Updated assembly version of PowerBI cmdlets</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="f9e89-245">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="f9e89-245">Az.PrivateDns</span></span>
* <span data-ttu-id="f9e89-246">Korrigerade formatering av utförlig utdatasträng för Remove-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="f9e89-246">Corrected verbose output string formatting for Remove-AzPrivateDnsRecordSet</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f9e89-247">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f9e89-247">Az.RecoveryServices</span></span>
* <span data-ttu-id="f9e89-248">Azure Site Recovery-stöd för att skapa en återställningsplan för replikering mellan zoner från xml-indata.</span><span class="sxs-lookup"><span data-stu-id="f9e89-248">Azure Site Recovery support for creating recovery plan for zone to zone replication from xml input.</span></span>
* <span data-ttu-id="f9e89-249">Uppdaterad sammansättningsversion för cmdletar för SiteRecovery och Backup</span><span class="sxs-lookup"><span data-stu-id="f9e89-249">Updated assembly version of SiteRecovery and Backup cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="f9e89-250">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f9e89-250">Az.Resources</span></span>
* <span data-ttu-id="f9e89-251">Lade till slutparameter för cmdletarna Get-AzDeploymentScriptLog och Save-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="f9e89-251">Added Tail parameter to Get-AzDeploymentScriptLog and Save-AzDeploymentScriptLog cmdlets</span></span>
* <span data-ttu-id="f9e89-252">Formaterad utdataegenskap så att den kan visas i cmdlet-utdata för Get-AzDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="f9e89-252">Formatted Output property and show it on the Get-AzDeploymentScript cmdlet output</span></span>
* <span data-ttu-id="f9e89-253">Bytte namn på parametern -DeploymentScriptInputObject till -DeploymentScriptObject</span><span class="sxs-lookup"><span data-stu-id="f9e89-253">Renamed -DeploymentScriptInputObject parameter to -DeploymentScriptObject</span></span>
* <span data-ttu-id="f9e89-254">Åtgärdade saknade fil/målnamn i cmdlet-meddelanden.</span><span class="sxs-lookup"><span data-stu-id="f9e89-254">Fixed missing file/target name in cmdlet messages.</span></span>
* <span data-ttu-id="f9e89-255">Uppdaterad sammansättningsversion för cmdletar för resurshanterare och taggar</span><span class="sxs-lookup"><span data-stu-id="f9e89-255">Updated assembly version of resource manager and tags cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="f9e89-256">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f9e89-256">Az.Sql</span></span>
* <span data-ttu-id="f9e89-257">Lade till UsePrivateLinkConnection till ”New-AzSqlSyncGroup”, ”Update-AzSqlSyncGroup”, ”New-AzSqlSyncMember” och ”Update-AzSqlSyncMember”</span><span class="sxs-lookup"><span data-stu-id="f9e89-257">Added UsePrivateLinkConnection to 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="f9e89-258">Lade till SyncMemberAzureDatabaseResourceId till ”New-AzSqlSyncMember” and ”Update-AzSqlSyncMember”</span><span class="sxs-lookup"><span data-stu-id="f9e89-258">Added SyncMemberAzureDatabaseResourceId to 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="f9e89-259">Lade till stöd för att söka efter gästanvändare för att ange administratörs-cmdlet för SQL Server Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="f9e89-259">Added Guest user lookup support to Set SQL Server Azure Active Directory Admin cmdlet</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f9e89-260">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f9e89-260">Az.Storage</span></span>
* <span data-ttu-id="f9e89-261">Uppdaterad sammansättningsversion för dataplan-cmdletar</span><span class="sxs-lookup"><span data-stu-id="f9e89-261">Updated assembly version of data plane cmdlets</span></span>

## <a name="410---may-2020"></a><span data-ttu-id="f9e89-262">4.1.0 – maj 2020</span><span class="sxs-lookup"><span data-stu-id="f9e89-262">4.1.0 - May 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="f9e89-263">Höjdpunkter sedan den senaste uppdateringen</span><span class="sxs-lookup"><span data-stu-id="f9e89-263">Highlights since the last release</span></span>
* <span data-ttu-id="f9e89-264">PowerShell-versioner som stöds: Windows PowerShell 5.1, PowerShell Core 6.2.4+ och PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="f9e89-264">Supported PowerShell versions: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>
* <span data-ttu-id="f9e89-265">Allmän tillgänglighet för Az.Functions</span><span class="sxs-lookup"><span data-stu-id="f9e89-265">General availability of Az.Functions</span></span> 
* <span data-ttu-id="f9e89-266">Nya stora uppdateringar har gjorts för Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources och Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f9e89-266">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources, and Az.Storage have major release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f9e89-267">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f9e89-267">Az.Accounts</span></span>
* <span data-ttu-id="f9e89-268">”Add-AzEnvironment” och ”Set-AzEnvironment” har uppdaterats med stöd för parametrarna ”AzureSynapseAnalyticsEndpointResourceId” och ”AzureSynapseAnalyticsEndpointSuffix”</span><span class="sxs-lookup"><span data-stu-id="f9e89-268">Updated 'Add-AzEnvironment' and 'Set-AzEnvironment' to accept parameters 'AzureSynapseAnalyticsEndpointResourceId' and 'AzureSynapseAnalyticsEndpointSuffix'</span></span>
* <span data-ttu-id="f9e89-269">Azure.Core-relaterade sammansättningar har lagts till i Az.Accounts; PowerShell-plattformar som stöds är Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span><span class="sxs-lookup"><span data-stu-id="f9e89-269">Added Azure.Core related assemblies into Az.Accounts, supported PowerShell platforms include Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span></span>

#### <a name="azaks"></a><span data-ttu-id="f9e89-270">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="f9e89-270">Az.Aks</span></span>
* <span data-ttu-id="f9e89-271">API-versionen har uppgraderats till 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="f9e89-271">Upgraded API Version to 2019-10-01</span></span>
* <span data-ttu-id="f9e89-272">Stöds för att skapa AKS med hjälp av Windows-container</span><span class="sxs-lookup"><span data-stu-id="f9e89-272">Supported to create AKS using Windows container</span></span>
* <span data-ttu-id="f9e89-273">Nya cmdletar är tillgängliga: ”New-AzAksNodePool”, ”Update-AzAksNodePool”, ”Remove-AzAksNodePool”,        ”Get-AzAksNodePool”, ”Install-AzAksKubectl”, ”Get-AzAksVersion”</span><span class="sxs-lookup"><span data-stu-id="f9e89-273">Provided new cmdlets: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="f9e89-274">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f9e89-274">Az.ApiManagement</span></span>
* <span data-ttu-id="f9e89-275">Parametrarna ”New-AzApiManagement” och ”Set-AzApiManagement”: [-AssignIdentity] har bytt namn till [-SystemAssignedIdentity]</span><span class="sxs-lookup"><span data-stu-id="f9e89-275">'New-AzApiManagement' and 'Set-AzApiManagement': [-AssignIdentity] parameter renamed as [-SystemAssignedIdentity]</span></span>
* <span data-ttu-id="f9e89-276">”New-AzApiManagement” och ”Set-AzApiManagement”: En ny parameter har lagts till: [-UserAssignedIdentity <String[]>]</span><span class="sxs-lookup"><span data-stu-id="f9e89-276">'New-AzApiManagement' and 'Set-AzApiManagement': New parameter added: [-UserAssignedIdentity <String[]>]</span></span>
* <span data-ttu-id="f9e89-277">”Get-AzApiManagementProperty” har bytt namn till ”Get-AzApiManagementNamedValue”.</span><span class="sxs-lookup"><span data-stu-id="f9e89-277">'Get-AzApiManagementProperty': renamed as 'Get-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="f9e89-278">PropertyId-parametern har bytt namn till NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="f9e89-278">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="f9e89-279">”New-AzApiManagementProperty” har bytt namn till ”New-AzApiManagementNamedValue”.</span><span class="sxs-lookup"><span data-stu-id="f9e89-279">'New-AzApiManagementProperty': renamed as 'New-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="f9e89-280">PropertyId-parametern har bytt namn till NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="f9e89-280">PropertyId parameter renamed as NamedValueId.</span></span> 
* <span data-ttu-id="f9e89-281">”Set-AzApiManagementProperty” har bytt namn till ”Set-AzApiManagementNamedValue”.</span><span class="sxs-lookup"><span data-stu-id="f9e89-281">'Set-AzApiManagementProperty': renamed as 'Set-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="f9e89-282">PropertyId-parametern har bytt namn till NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="f9e89-282">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="f9e89-283">”Remove-AzApiManagementProperty” har bytt namn till ”Remove-AzApiManagementNamedValue”.</span><span class="sxs-lookup"><span data-stu-id="f9e89-283">'Remove-AzApiManagementProperty': renamed as 'Remove-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="f9e89-284">PropertyId-parametern har bytt namn till NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="f9e89-284">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="f9e89-285">Den nya cmdleten Get-AzApiManagementAuthorizationServerClientSecret gör att ”Get-AzApiManagementAuthorizationServer” inte längre returnerar klienthemligheter.</span><span class="sxs-lookup"><span data-stu-id="f9e89-285">Added new 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet and 'Get-AzApiManagementAuthorizationServer' will not return client secret anymore.</span></span>
* <span data-ttu-id="f9e89-286">Den nya cmdleten ”Get-AzApiManagementNamedValueSecretValue” gör att ”Get-AzApiManagementNamedValue” inte returnerar värdet för en hemlighet.</span><span class="sxs-lookup"><span data-stu-id="f9e89-286">Added new 'Get-AzApiManagementNamedValueSecretValue' cmdlet and 'Get-AzApiManagementNamedValue' will not return secret value.</span></span>
* <span data-ttu-id="f9e89-287">Den nya cmdleten ”Get-AzApiManagementOpenIdConnectProviderClientSecret” gör att ”Get-AzApiManagementOpenIdConnectProvider” inte längre returnerar klienthemligheter.</span><span class="sxs-lookup"><span data-stu-id="f9e89-287">Added new 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet and 'Get-AzApiManagementOpenIdConnectProvider' will not return client secret anymore.</span></span>
* <span data-ttu-id="f9e89-288">Den nya cmdleten ”Get-AzApiManagementSubscriptionKey” gör att ”Get-AzApiManagementSubscription” inte längre returnerar prenumerationsnycklar.</span><span class="sxs-lookup"><span data-stu-id="f9e89-288">Added new 'Get-AzApiManagementSubscriptionKey' cmdlet and 'Get-AzApiManagementSubscription' will not return subscription keys anymore.</span></span>
* <span data-ttu-id="f9e89-289">Den nya cmdleten ”Get-AzApiManagementTenantAccessSecret” gör att ”Get-AzApiManagementTenantAccess” inte längre returnerar nycklar.</span><span class="sxs-lookup"><span data-stu-id="f9e89-289">Added new 'Get-AzApiManagementTenantAccessSecret' cmdlet and 'Get-AzApiManagementTenantAccess' will not return keys anymore.</span></span>
* <span data-ttu-id="f9e89-290">Den nya cmdleten ”Get-AzApiManagementTenantGitAccessSecret” gör att ”Get-AzApiManagementTenantGitAccess” inte längre returnerar nycklar.</span><span class="sxs-lookup"><span data-stu-id="f9e89-290">Added new 'Get-AzApiManagementTenantGitAccessSecret' cmdlet and 'Get-AzApiManagementTenantGitAccess' will not return keys anymore.</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="f9e89-291">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="f9e89-291">Az.ApplicationInsights</span></span>
* <span data-ttu-id="f9e89-292">Tillagda parametrar: ”RetentionInDays” ”PublicNetworkAccessForIngestion” ”PublicNetworkAccessForQuery” för ”New-AzApplicationInsights”</span><span class="sxs-lookup"><span data-stu-id="f9e89-292">Added Parameters: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span></span>
* <span data-ttu-id="f9e89-293">Cmdleten ”Update-AzApplicationInsights” har skapats</span><span class="sxs-lookup"><span data-stu-id="f9e89-293">Created cmdlet 'Update-AzApplicationInsights'</span></span>
* <span data-ttu-id="f9e89-294">Cmdletar har skapats för länkat lagringskonto</span><span class="sxs-lookup"><span data-stu-id="f9e89-294">Created cmdlets for Linked Storage Account</span></span>

#### <a name="azbatch"></a><span data-ttu-id="f9e89-295">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="f9e89-295">Az.Batch</span></span>
* <span data-ttu-id="f9e89-296">Az.Batch har uppdaterats att använda ”Microsoft.Azure.Batch” SDK version 13.0.0 och ”Microsoft.Azure.Management.Batch” SDK version 9.0.0.</span><span class="sxs-lookup"><span data-stu-id="f9e89-296">Updated Az.Batch to use 'Microsoft.Azure.Batch' SDK version 13.0.0 and 'Microsoft.Azure.Management.Batch' SDK version 9.0.0.</span></span>
* <span data-ttu-id="f9e89-297">Nu kan du välja vilken typ av certifikat du lägger till genom att använda den nya parametern ”-CertificateKind” med ”New-AzBatchCertificate”.</span><span class="sxs-lookup"><span data-stu-id="f9e89-297">Added the ability to select the kind of certificate being added using the new '-CertificateKind' parameter to 'New-AzBatchCertificate'.</span></span>
* <span data-ttu-id="f9e89-298">Egenskapen ”ApplicationPackages” har tagits bort från ”PSApplication”, som tidigare alltid var ''.</span><span class="sxs-lookup"><span data-stu-id="f9e89-298">Removed 'ApplicationPackages' property from 'PSApplication' which was previously always ''.</span></span>
  - <span data-ttu-id="f9e89-299">Specifika paket i ett program kan nu hämtas med hjälp av ”Get-AzBatchApplicationPackage”.</span><span class="sxs-lookup"><span data-stu-id="f9e89-299">The specific packages inside of an application now can be retrieved using 'Get-AzBatchApplicationPackage'.</span></span> <span data-ttu-id="f9e89-300">Ett exempel: ”Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication”.</span><span class="sxs-lookup"><span data-stu-id="f9e89-300">For example: 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span></span>
* <span data-ttu-id="f9e89-301">Nu när du skapar en pool med hjälp av ”New-AzBatchPool” kan egenskapen ”VirtualMachineImageId” för ”PSImageReference” endast referera till en Shared Image Gallery-avbildning.</span><span class="sxs-lookup"><span data-stu-id="f9e89-301">When creating a pool using 'New-AzBatchPool', the 'VirtualMachineImageId' property of 'PSImageReference' can now only refer to a Shared Image Gallery image.</span></span>
* <span data-ttu-id="f9e89-302">När du skapar en pool med hjälp av ”New-AzBatchPool” kan poolen etableras utan en offentlig IP-adress med hjälp av den nya egenskapen ”PublicIPAddressConfiguration” för ”PSNetworkConfiguration”.</span><span class="sxs-lookup"><span data-stu-id="f9e89-302">When creating a pool using 'New-AzBatchPool', the pool can be provisioned without a public IP using the new 'PublicIPAddressConfiguration' property of 'PSNetworkConfiguration'.</span></span>
  - <span data-ttu-id="f9e89-303">Egenskapen ”PublicIPs” för ”PSNetworkConfiguration” har också flyttats till ”PSPublicIPAddressConfiguration”.</span><span class="sxs-lookup"><span data-stu-id="f9e89-303">The 'PublicIPs' property of 'PSNetworkConfiguration' has moved in to 'PSPublicIPAddressConfiguration' as well.</span></span> <span data-ttu-id="f9e89-304">Den här egenskapen kan bara anges om ”IPAddressProvisioningType” är ”UserManaged”.</span><span class="sxs-lookup"><span data-stu-id="f9e89-304">This property can only be specified if 'IPAddressProvisioningType' is 'UserManaged'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f9e89-305">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f9e89-305">Az.Compute</span></span>
* <span data-ttu-id="f9e89-306">Parametern HostId har lagts till för cmdleten ”Update-AzVM”t</span><span class="sxs-lookup"><span data-stu-id="f9e89-306">Added HostId parameter to 'Update-AzVM' cmdlet</span></span>
* <span data-ttu-id="f9e89-307">Hjälpdokumenten har uppdaterats för cmdletarna ”New-AzVMConfig”, ”New-AzVmssConfig”, ”Update-AzVmss”, ”Set-AzVMOperatingSystem” och ”Set-AzVmssOsProfile”.</span><span class="sxs-lookup"><span data-stu-id="f9e89-307">Updated Help documents for 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' and 'Set-AzVmssOsProfile' cmdlets.</span></span>
* <span data-ttu-id="f9e89-308">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="f9e89-308">Breaking changes</span></span>
    - <span data-ttu-id="f9e89-309">Parametern FilterExpression tas bort från cmdleten ”Get-AzVMImage”.</span><span class="sxs-lookup"><span data-stu-id="f9e89-309">FilterExpression parameter is removed from 'Get-AzVMImage' cmdlet.</span></span>
    - <span data-ttu-id="f9e89-310">Parametern AssignIdentity tas bort från cmdletarna ”New-AzVmssConfig”, ”New-AzVMConfig” och ”Update-AzVM”.</span><span class="sxs-lookup"><span data-stu-id="f9e89-310">AssignIdentity parameter is removed from 'New-AzVmssConfig', 'New-AzVMConfig' and 'Update-AzVM' cmdlets.</span></span>
    - <span data-ttu-id="f9e89-311">AutomaticRepairMaxInstanceRepairsPercent tas bort från cmdletarna ”New-AzVmssConfig” och ”Update-AzVmss”.</span><span class="sxs-lookup"><span data-stu-id="f9e89-311">AutomaticRepairMaxInstanceRepairsPercent is removed from 'New-AzVmssConfig' and 'Update-AzVmss' cmdlets.</span></span>
    - <span data-ttu-id="f9e89-312">Egenskaperna AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus och VirtualMachineScaleSetsColocationStatus tas bort från ProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="f9e89-312">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus and VirtualMachineScaleSetsColocationStatus properties are removed from ProximityPlacementGroup.</span></span>
    - <span data-ttu-id="f9e89-313">Egenskapen MaxInstanceRepairsPercent tas bort från AutomaticRepairsPolicy.</span><span class="sxs-lookup"><span data-stu-id="f9e89-313">MaxInstanceRepairsPercent property is removed from AutomaticRepairsPolicy.</span></span>
    - <span data-ttu-id="f9e89-314">Typerna AvailabilitySets, VirtualMachines och VirtualMachineScaleSets ändras från IList<SubResource> till IList<SubResourceWithColocationStatus>.</span><span class="sxs-lookup"><span data-stu-id="f9e89-314">The types of AvailabilitySets, VirtualMachines and VirtualMachineScaleSets are changed from IList<SubResource> to IList<SubResourceWithColocationStatus>.</span></span>
* <span data-ttu-id="f9e89-315">Beskrivningen för cmdleten ”Get-AzVM” har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="f9e89-315">Description for 'Get-AzVM' cmdlet has been updated to better describe it.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="f9e89-316">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f9e89-316">Az.DataFactory</span></span>
* <span data-ttu-id="f9e89-317">CRUD-stöd för egenskaper för dataflödeskörning  i hanterad IR.</span><span class="sxs-lookup"><span data-stu-id="f9e89-317">Supported CRUD of data flow runtime properties in Managed IR.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="f9e89-318">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f9e89-318">Az.FrontDoor</span></span>
* <span data-ttu-id="f9e89-319">Nya cmdletar har lagts till för att skapa, uppdatera, hämta och ta bort (CRUD) Front Door-regelmotorobjekt</span><span class="sxs-lookup"><span data-stu-id="f9e89-319">Added new cmdlets for creation, update, retreival, and deletion of Front Door Rules Engine object</span></span>
* <span data-ttu-id="f9e89-320">Hjälp-cmdletar har lagts till för konstruktion av Front Door-regelmotorobjekt</span><span class="sxs-lookup"><span data-stu-id="f9e89-320">Added helper cmdlets for construction of Front Door Rules Engine object</span></span>
* <span data-ttu-id="f9e89-321">Regelmotorreferens har lagts till för Front Door-hanteringsregelobjekt.</span><span class="sxs-lookup"><span data-stu-id="f9e89-321">Added Rules Engine reference to Front Door Routing Rule object.</span></span>
* <span data-ttu-id="f9e89-322">Parametrar för Private Link har lagts till för Front Door-serverdelsobjekt</span><span class="sxs-lookup"><span data-stu-id="f9e89-322">Added Private Link parameters to Front Door Backend object</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="f9e89-323">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="f9e89-323">Az.Functions</span></span>
* <span data-ttu-id="f9e89-324">Allmän tillgänglighet för ”Az.Functions”-modulen</span><span class="sxs-lookup"><span data-stu-id="f9e89-324">General availability of ''Az.Functions'' module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="f9e89-325">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f9e89-325">Az.HDInsight</span></span>
* <span data-ttu-id="f9e89-326">Stöd för diskkryptering med kundhanterad nyckel.</span><span class="sxs-lookup"><span data-stu-id="f9e89-326">Supported Customer-managed key disk encryption.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="f9e89-327">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="f9e89-327">Az.HealthcareApis</span></span>
* <span data-ttu-id="f9e89-328">Åtkomstprinciper använder inte längre det aktiva huvudkontot som standard</span><span class="sxs-lookup"><span data-stu-id="f9e89-328">Access policies are no longer defaulted to the current principal</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f9e89-329">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f9e89-329">Az.IotHub</span></span>
* <span data-ttu-id="f9e89-330">En cmdlet har lagts till som anropar en fråga i en IoT-hubb för att hämta information med ett SQL-liknande språk.</span><span class="sxs-lookup"><span data-stu-id="f9e89-330">Added cmdlet to invoke a query in an IoT hub to retrieve information using a SQL-like language.</span></span>
* <span data-ttu-id="f9e89-331">Problemet som gjorde att ”Add-AzIotHubDevice” inte skapade en Edge-aktiverad enhet utan underordnade enheter har åtgärdats [#11597]</span><span class="sxs-lookup"><span data-stu-id="f9e89-331">Fix issue that 'Add-AzIotHubDevice' fails to create Edge Enabled Device without child devices [#11597]</span></span>
* <span data-ttu-id="f9e89-332">En cmdlet har lagts till för att generera SAS-token för en Iot-hubb, enhet eller modul.</span><span class="sxs-lookup"><span data-stu-id="f9e89-332">Added cmdlet to generate SAS token for Iot Hub, device or module.</span></span>
* <span data-ttu-id="f9e89-333">En cmdlet har lagts till för att anropa en måttfråga om konfiguration.</span><span class="sxs-lookup"><span data-stu-id="f9e89-333">Added cmdlet to invoke configuration metrics query.</span></span>
* <span data-ttu-id="f9e89-334">Hantera automatisk distribution av IoT Edge i stor skala.</span><span class="sxs-lookup"><span data-stu-id="f9e89-334">Manage IoT Edge automatic deployment at scale.</span></span> <span data-ttu-id="f9e89-335">Nya cmdlet:ar är:</span><span class="sxs-lookup"><span data-stu-id="f9e89-335">New cmdlets are:</span></span>
    - <span data-ttu-id="f9e89-336">”Add-AzIotHubDeployment”</span><span class="sxs-lookup"><span data-stu-id="f9e89-336">'Add-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="f9e89-337">”Get-AzIotHubDeployment”</span><span class="sxs-lookup"><span data-stu-id="f9e89-337">'Get-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="f9e89-338">”Remove-AzIotHubDeployment”</span><span class="sxs-lookup"><span data-stu-id="f9e89-338">'Remove-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="f9e89-339">”Set-AzIotHubDeployment”</span><span class="sxs-lookup"><span data-stu-id="f9e89-339">'Set-AzIotHubDeployment'</span></span>
* <span data-ttu-id="f9e89-340">En cmdlet har lagts till för att anropa en måttfråga om IoT Edge-distribution.</span><span class="sxs-lookup"><span data-stu-id="f9e89-340">Added cmdlet to invoke an IoT Edge deployment metrics query.</span></span>
* <span data-ttu-id="f9e89-341">En cmdlet har lagts till för att tillämpa konfigurationsinnehåll på den angivna gränsenheten.</span><span class="sxs-lookup"><span data-stu-id="f9e89-341">Added cmdlet to apply the configuration content to the specified edge device.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f9e89-342">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f9e89-342">Az.KeyVault</span></span>
* <span data-ttu-id="f9e89-343">Två alias har tagits bort: ”New-AzKeyVaultCertificateAdministratorDetails” och ”New-AzKeyVaultCertificateOrganizationDetails”</span><span class="sxs-lookup"><span data-stu-id="f9e89-343">Removed two aliases: 'New-AzKeyVaultCertificateAdministratorDetails' and 'New-AzKeyVaultCertificateOrganizationDetails'</span></span>
* <span data-ttu-id="f9e89-344">Nu är mjuk borttagning aktiverat som standard när ett nyckelvalv skapas</span><span class="sxs-lookup"><span data-stu-id="f9e89-344">Enabled soft delete by default when creating a key vault</span></span>
* <span data-ttu-id="f9e89-345">Nätverksregler kan ställas in för att styra åtkomsten från särskilda nätverksplatser när du skapar ett nyckelvalv</span><span class="sxs-lookup"><span data-stu-id="f9e89-345">Network rules can be set to govern the accessibility from specific network locations when creating a key vault</span></span>
* <span data-ttu-id="f9e89-346">Stöd för BYOK (Bring Your Own Key) har lagts till</span><span class="sxs-lookup"><span data-stu-id="f9e89-346">Added support to bring your own key (BYOK)</span></span>
    - <span data-ttu-id="f9e89-347">”Add-AzKeyVaultKey” stöder generering av en KeyExchange-nyckel</span><span class="sxs-lookup"><span data-stu-id="f9e89-347">'Add-AzKeyVaultKey' supports generating a key exchange key</span></span>
    - <span data-ttu-id="f9e89-348">”Get-AzKeyVaultKey” stöder nedladdning av en offentlig nyckel i PEM-format</span><span class="sxs-lookup"><span data-stu-id="f9e89-348">'Get-AzKeyVaultKey' supports downloading a public key in PEM format</span></span>
* <span data-ttu-id="f9e89-349">”KeyOps”-delen av hjälpdokumentet för ”Add-AzKeyVaultKey” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="f9e89-349">Updated the 'KeyOps' part of the help document of 'Add-AzKeyVaultKey'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f9e89-350">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f9e89-350">Az.Monitor</span></span>
* <span data-ttu-id="f9e89-351">Bugg för ”Set-AzDiagnosticSettings” har åtgärdats; kvarhållningsprincipen tillämpas inte på alla kategorier [#11589]</span><span class="sxs-lookup"><span data-stu-id="f9e89-351">Fixed bug for 'Set-AzDiagnosticSettings', retention policy won't apply to all categories [#11589]</span></span>
* <span data-ttu-id="f9e89-352">Stöd för WebTest-tillgänglighetskriterier för måttavisering V2</span><span class="sxs-lookup"><span data-stu-id="f9e89-352">Supported WebTest availability criteria for metric alert V2</span></span>
    - <span data-ttu-id="f9e89-353">”New-AzMetricAlertRuleV2Criteria”: ett alternativ för att skapa tillgänglighetskriterier för webbtest har lagts till</span><span class="sxs-lookup"><span data-stu-id="f9e89-353">'New-AzMetricAlertRuleV2Criteria': an option to create webtest availability criteria was added</span></span>
    - <span data-ttu-id="f9e89-354">”Add-AzMetricAlertRuleV2”: stöd för de nya tillgänglighetskriterierna för webbtest</span><span class="sxs-lookup"><span data-stu-id="f9e89-354">'Add-AzMetricAlertRuleV2': supports the new webtest availability criteria</span></span>
* <span data-ttu-id="f9e89-355">Redundant definition har tagits bort för RetentionPolicy i PSLogProfile [#7608]</span><span class="sxs-lookup"><span data-stu-id="f9e89-355">Removed redundant definition for RetentionPolicy in PSLogProfile [#7608]</span></span>
* <span data-ttu-id="f9e89-356">Redundanta egenskaper som definierats i PSEventData har tagits bort [#11353]</span><span class="sxs-lookup"><span data-stu-id="f9e89-356">Removed redundant properties difined in PSEventData [#11353]</span></span>
* <span data-ttu-id="f9e89-357">”Get-AzLog” har bytt namn till ”Get-AzActivityLog”</span><span class="sxs-lookup"><span data-stu-id="f9e89-357">Renamed 'Get-AzLog' to 'Get-AzActivityLog'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f9e89-358">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f9e89-358">Az.Network</span></span>
* <span data-ttu-id="f9e89-359">Attribut för icke-bakåtkompatibel ändring har lagts till för att meddela att standardbeteendet för zoner kommer att ändras</span><span class="sxs-lookup"><span data-stu-id="f9e89-359">Added breaking change attribute to notify that Zone default behaviour will be changed</span></span>
    - <span data-ttu-id="f9e89-360">”New-AzPublicIpAddress”</span><span class="sxs-lookup"><span data-stu-id="f9e89-360">'New-AzPublicIpAddress'</span></span>
    - <span data-ttu-id="f9e89-361">”New-AzPublicIpPrefix”</span><span class="sxs-lookup"><span data-stu-id="f9e89-361">'New-AzPublicIpPrefix'</span></span>
    - <span data-ttu-id="f9e89-362">”New-AzLoadBalancerFrontendIpConfig”</span><span class="sxs-lookup"><span data-stu-id="f9e89-362">'New-AzLoadBalancerFrontendIpConfig'</span></span>
* <span data-ttu-id="f9e89-363">Stöd har lagts till för en ny resurs på den översta nivån, SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="f9e89-363">Added support for a new top level resource SecurityPartnerProvider</span></span>
    - <span data-ttu-id="f9e89-364">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="f9e89-364">New cmdlets added:</span></span>
        - <span data-ttu-id="f9e89-365">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="f9e89-365">New-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="f9e89-366">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="f9e89-366">Remove-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="f9e89-367">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="f9e89-367">Get-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="f9e89-368">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="f9e89-368">Set-AzSecurityPartnerProvider</span></span>
* <span data-ttu-id="f9e89-369">”RequiredZoneNames” har lagts till för ”PSPrivateLinkResource” och ”GroupId” för ”PSPrivateEndpointConnection”</span><span class="sxs-lookup"><span data-stu-id="f9e89-369">Added 'RequiredZoneNames' on 'PSPrivateLinkResource' and 'GroupId' on 'PSPrivateEndpointConnection'</span></span>
* <span data-ttu-id="f9e89-370">Fel parametertyp för SuccessThresholdRoundTripTimeMs-parametern för New-AzNetworkWatcherConnectionMonitorTestConfigurationObject har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="f9e89-370">Fixed incorrect type of SuccessThresholdRoundTripTimeMs parameter for New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>
* <span data-ttu-id="f9e89-371">VirtualWan-cmdletar har uppdaterats för att ange AllowVnetToVnetTraffic-argumentets standardvärde till True.</span><span class="sxs-lookup"><span data-stu-id="f9e89-371">Updated VirtualWan cmdlets to set default value of AllowVnetToVnetTraffic argument to True.</span></span>
    - <span data-ttu-id="f9e89-372">”New-AzVirtualWan”</span><span class="sxs-lookup"><span data-stu-id="f9e89-372">'New-AzVirtualWan'</span></span>
    - <span data-ttu-id="f9e89-373">”Update-AzVirtualWan”</span><span class="sxs-lookup"><span data-stu-id="f9e89-373">'Update-AzVirtualWan'</span></span>
* <span data-ttu-id="f9e89-374">Nya cmdletar har lagts till för att stödja DNS-zongrupp för privat slutpunkt</span><span class="sxs-lookup"><span data-stu-id="f9e89-374">Added new cmdlets to support DNS zone group for private endpoint</span></span>
    - <span data-ttu-id="f9e89-375">”New-AzPrivateDnsZoneConfig”</span><span class="sxs-lookup"><span data-stu-id="f9e89-375">'New-AzPrivateDnsZoneConfig'</span></span>
    - <span data-ttu-id="f9e89-376">”Get-AzPrivateDnsZoneGroup”</span><span class="sxs-lookup"><span data-stu-id="f9e89-376">'Get-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="f9e89-377">”New-AzPrivateDnsZoneGroup”</span><span class="sxs-lookup"><span data-stu-id="f9e89-377">'New-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="f9e89-378">”Set-AzPrivateDnsZoneGroup”</span><span class="sxs-lookup"><span data-stu-id="f9e89-378">'Set-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="f9e89-379">”Remove-AzPrivateDnsZoneGroup”</span><span class="sxs-lookup"><span data-stu-id="f9e89-379">'Remove-AzPrivateDnsZoneGroup'</span></span>
* <span data-ttu-id="f9e89-380">Parametrarna ”DNSEnableProxy”, ”DNSRequireProxyForNetworkRules” och ”DNSServers” har lagts till för ”AzureFirewall”</span><span class="sxs-lookup"><span data-stu-id="f9e89-380">Added 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' and 'DNSServers' parameters to 'AzureFirewall'</span></span>
* <span data-ttu-id="f9e89-381">Parametrarna ”EnableDnsProxy”, ”DnsProxyNotRequiredForNetworkRule” och ”DnsServer” har lagts till för ”AzureFirewall”</span><span class="sxs-lookup"><span data-stu-id="f9e89-381">Added 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' and 'DnsServer' parameters to 'AzureFirewall'</span></span>
    - <span data-ttu-id="f9e89-382">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="f9e89-382">Updated cmdlet:</span></span>
        - <span data-ttu-id="f9e89-383">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="f9e89-383">New-AzFirewall</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f9e89-384">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f9e89-384">Az.OperationalInsights</span></span>
* <span data-ttu-id="f9e89-385">Äldre kod har uppdaterats för att tillämpa ny genererad SDK</span><span class="sxs-lookup"><span data-stu-id="f9e89-385">Updated legacy code to apply new generated SDK</span></span>
* <span data-ttu-id="f9e89-386">Cmdletar har tagits bort på grund av föråldrade API:er</span><span class="sxs-lookup"><span data-stu-id="f9e89-386">Deleted cmdlets due to deprecated APIs</span></span>
    - <span data-ttu-id="f9e89-387">”Get-AzOperationalInsightsSavedSearchResult” (alias ”Get-AzOperationalInsightsSavedSearchResults”)</span><span class="sxs-lookup"><span data-stu-id="f9e89-387">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span></span>
    - <span data-ttu-id="f9e89-388">”Get-AzOperationalInsightsSearchResult” (alias ”Get-AzOperationalInsightsSearchResults”)</span><span class="sxs-lookup"><span data-stu-id="f9e89-388">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span></span>
    - <span data-ttu-id="f9e89-389">”Get-AzOperationalInsightsLinkTarget” (alias ”Get-AzOperationalInsightsLinkTargets”)</span><span class="sxs-lookup"><span data-stu-id="f9e89-389">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span></span>
* <span data-ttu-id="f9e89-390">Parametrar har lagts till för ”Set-AzOperationalInsightsWorkspace” och ”New-AzOperationalInsightsWorkspace”</span><span class="sxs-lookup"><span data-stu-id="f9e89-390">Added parameters for 'Set-AzOperationalInsightsWorkspace' and 'New-AzOperationalInsightsWorkspace'</span></span>
* <span data-ttu-id="f9e89-391">Cmdletar har skapats för länkat lagringskonto</span><span class="sxs-lookup"><span data-stu-id="f9e89-391">Created cmdlets for Linked Stoarge Account</span></span>
* <span data-ttu-id="f9e89-392">Cmdletar har skapats för kluster och länkad tjänst</span><span class="sxs-lookup"><span data-stu-id="f9e89-392">Created cmdlets for Clusters and Linked Service</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f9e89-393">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f9e89-393">Az.RecoveryServices</span></span>
* <span data-ttu-id="f9e89-394">Azure Site Recovery: Stöd har lagts till för att skydda VM-närhetsplaceringsgrupper för Azure till Azure-provider.</span><span class="sxs-lookup"><span data-stu-id="f9e89-394">Azure Site Recovery added support for protecting proximity placement group virtual machines for Azure to Azure provider.</span></span>
* <span data-ttu-id="f9e89-395">Azure Site Recovery: Stöd har lagts till för replikering mellan zoner.</span><span class="sxs-lookup"><span data-stu-id="f9e89-395">Azure Site Recovery added support for zone to zone replication.</span></span>
* <span data-ttu-id="f9e89-396">Azure Backup: Stöd har lagts till för långsiktig kvarhållning för Azure FileShare-återställningspunkter.</span><span class="sxs-lookup"><span data-stu-id="f9e89-396">Azure Backup Added Long term retention support for Azure FileShare Recovery Points.</span></span>
* <span data-ttu-id="f9e89-397">Azure Backup: Egenskaper för diskexkludering har lagts till för cmdlet-utdata från ”Get-AzRecoveryServicesBackupItem”.</span><span class="sxs-lookup"><span data-stu-id="f9e89-397">Azure Backup Added disk exclusion properties to 'Get-AzRecoveryServicesBackupItem' cmdlet output.</span></span>
* <span data-ttu-id="f9e89-398">En privat slutpunkt har lagts till för filen med valvets autentiseringsuppgifter för Site Recovery-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="f9e89-398">Added private endpoint for Vault credential file for site recovery service.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f9e89-399">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f9e89-399">Az.Resources</span></span>
* <span data-ttu-id="f9e89-400">En varning har lagts till om visningsfördröjning när en ny rolldefinition skapas</span><span class="sxs-lookup"><span data-stu-id="f9e89-400">Added message warning about view delay when creating a new Role Definition</span></span>
* <span data-ttu-id="f9e89-401">Princip-cmdletar har ändrats för utmatning av starkt typifierade objekt</span><span class="sxs-lookup"><span data-stu-id="f9e89-401">Changed policy cmdlets to output strongly-typed objects</span></span>
* <span data-ttu-id="f9e89-402">Parametern ”-TenantLevel” har tagits bort för användning med ”Get-AzResourceLock” [#11335]</span><span class="sxs-lookup"><span data-stu-id="f9e89-402">Removed '-TenantLevel' parameter used for on the 'Get-AzResourceLock' cmdlet [#11335]</span></span>
* <span data-ttu-id="f9e89-403">”Remove-AzResourceGroup -Id ResourceId” har åtgärdats [#9882]</span><span class="sxs-lookup"><span data-stu-id="f9e89-403">Fixed 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span></span>
* <span data-ttu-id="f9e89-404">En ny cmdlet har lagts till för att hämta What-If-resultat för ARM-mallar i omfånget för resursgrupper: ”Get-AzDeploymentResourceGroupWhatIfResult”</span><span class="sxs-lookup"><span data-stu-id="f9e89-404">Added new cmdlet for getting ARM template What-If results at resource group scope: 'Get-AzDeploymentResourceGroupWhatIfResult'</span></span>
* <span data-ttu-id="f9e89-405">En ny cmdlet har lagts till för att hämta What-If-resultat för ARM-mallar i prenumerationsomfånget: ”Get-AzDeploymentWhatIfResult”</span><span class="sxs-lookup"><span data-stu-id="f9e89-405">Added new cmdlet for getting ARM template What-If results at subscription scope: 'Get-AzDeploymentWhatIfResult'</span></span>
   - <span data-ttu-id="f9e89-406">Alias: ”Get-AzSubscriptionDeploymentWhatIf”</span><span class="sxs-lookup"><span data-stu-id="f9e89-406">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span></span>
* <span data-ttu-id="f9e89-407">Parametrarna ”-WhatIf” och ”-Confirm” har åsidosatts för ”New-AzDeployment” och ”New-AzResourceGroupDeployment” för att använda What-If-resultat för ARM-mallar</span><span class="sxs-lookup"><span data-stu-id="f9e89-407">Overrode '-WhatIf' and '-Confirm' parameters for 'New-AzDeployment' and 'New-AzResourceGroupDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="f9e89-408">Ett utfasningsmeddelande har lagts till för parametern ”ApiVersion” i distributions-cmdletar</span><span class="sxs-lookup"><span data-stu-id="f9e89-408">Added deprecation message for 'ApiVersion' parameter in deployment cmdlets</span></span>
* <span data-ttu-id="f9e89-409">En funktion har lagts till för att visa förbättrade felmeddelanden för distributionsfel</span><span class="sxs-lookup"><span data-stu-id="f9e89-409">Added capability to show improved error messages for deployment failures</span></span>
* <span data-ttu-id="f9e89-410">CorrelationId-loggning har lagts till för distributionsfel</span><span class="sxs-lookup"><span data-stu-id="f9e89-410">Added correlationId logging for deployment failures</span></span>
* <span data-ttu-id="f9e89-411">Egenskapen ”error” har lagts till i utdata från distributionsskript</span><span class="sxs-lookup"><span data-stu-id="f9e89-411">Added 'error' property to the deployment script output</span></span>
* <span data-ttu-id="f9e89-412">Nuget Microsoft.Azure.Management.ResourceManager har uppdaterats till ”3.7.1-preview”</span><span class="sxs-lookup"><span data-stu-id="f9e89-412">Updated nuget Microsoft.Azure.Management.ResourceManager to '3.7.1-preview'</span></span>
* <span data-ttu-id="f9e89-413">Specifika testfall har tagits bort då egenskapen Error i DeploymentValidateResult har ändrats till lässkyddad från nuget 3.7.1-preview</span><span class="sxs-lookup"><span data-stu-id="f9e89-413">Removed specific test cases as Error property in DeploymentValidateResult has changed to readonly from nuget 3.7.1-preview</span></span>
* <span data-ttu-id="f9e89-414">GenericResourceExpanded har flyttats från SDK ResourceManager 3.7.1-preview</span><span class="sxs-lookup"><span data-stu-id="f9e89-414">Brought GenericResourceExpanded from SDK ResourceManager 3.7.1-preview</span></span>
* <span data-ttu-id="f9e89-415">Stöd för taggar har lagts till för alla Get-cmdletar för distribution, samt</span><span class="sxs-lookup"><span data-stu-id="f9e89-415">Added tag support for all Get cmdlets for deployment, as well as</span></span>
    - <span data-ttu-id="f9e89-416">”New-AzDeployment”</span><span class="sxs-lookup"><span data-stu-id="f9e89-416">'New-AzDeployment'</span></span>
    - <span data-ttu-id="f9e89-417">”New-AzManagementGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="f9e89-417">'New-AzManagementGroupDeployment'</span></span>
    - <span data-ttu-id="f9e89-418">”New-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="f9e89-418">'New-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="f9e89-419">”New-AzTenantDeployment”</span><span class="sxs-lookup"><span data-stu-id="f9e89-419">'New-AzTenantDeployment'</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f9e89-420">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f9e89-420">Az.ServiceFabric</span></span>
* <span data-ttu-id="f9e89-421">En bugg har åtgärdats som gjorde att --SecretIdentifier fick fel tumavtryck för certifikat när ett certifikat lades till</span><span class="sxs-lookup"><span data-stu-id="f9e89-421">Fixed bug in add certificate using --SecretIdentifier that was getting the wrong certificate thumbprint</span></span>

#### <a name="azsql"></a><span data-ttu-id="f9e89-422">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f9e89-422">Az.Sql</span></span>
* <span data-ttu-id="f9e89-423">Förbättrade prestanda för:</span><span class="sxs-lookup"><span data-stu-id="f9e89-423">Enhance performance of:</span></span>
    - <span data-ttu-id="f9e89-424">”Set-AzSqlDatabaseSensitivityClassification”</span><span class="sxs-lookup"><span data-stu-id="f9e89-424">'Set-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="f9e89-425">”Set-AzSqlInstanceDatabaseSensitivityClassification”</span><span class="sxs-lookup"><span data-stu-id="f9e89-425">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="f9e89-426">”Remove-AzSqlDatabaseSensitivityClassification”</span><span class="sxs-lookup"><span data-stu-id="f9e89-426">'Remove-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="f9e89-427">”Remove-AzSqlInstanceDatabaseSensitivityClassification”</span><span class="sxs-lookup"><span data-stu-id="f9e89-427">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="f9e89-428">”Enable-AzSqlDatabaseSensitivityRecommendation”</span><span class="sxs-lookup"><span data-stu-id="f9e89-428">'Enable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="f9e89-429">”Enable-AzSqlInstanceDatabaseSensitivityRecommendation”</span><span class="sxs-lookup"><span data-stu-id="f9e89-429">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="f9e89-430">”Disable-AzSqlDatabaseSensitivityRecommendation”</span><span class="sxs-lookup"><span data-stu-id="f9e89-430">'Disable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="f9e89-431">”Disable-AzSqlInstanceDatabaseSensitivityRecommendation”</span><span class="sxs-lookup"><span data-stu-id="f9e89-431">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
* <span data-ttu-id="f9e89-432">Validering på klientsidan har tagits bort för parametern ”RetentionDays” från cmdleten ”Set-AzSqlDatabaseBackupShortTermRetentionPolicy”</span><span class="sxs-lookup"><span data-stu-id="f9e89-432">Removed client-side validation of 'RetentionDays' parameter from cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span>
* <span data-ttu-id="f9e89-433">Granskning av ett lagringskonto i Vnet; en bugg har åtgärdats som orsakade fel när en Storage Blob Data-deltagarroll skapades.</span><span class="sxs-lookup"><span data-stu-id="f9e89-433">Auditing to a storage account in Vnet, fixing a bug when creating a Storage Blob Data Contributor role.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f9e89-434">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f9e89-434">Az.Storage</span></span>
* <span data-ttu-id="f9e89-435">”-AsJob” har lagts till för att hämta/lista konto med cmdleten ”Get-AzStorageAccount”</span><span class="sxs-lookup"><span data-stu-id="f9e89-435">Added '-AsJob' to get/list account cmdlet 'Get-AzStorageAccount'</span></span>
* <span data-ttu-id="f9e89-436">Gör KeyVersion valfri när lagringskontot uppdateras med KeyvaultEncryption, för att ge stöd för automatisk nyckelrotation</span><span class="sxs-lookup"><span data-stu-id="f9e89-436">Make KeyVersion to optional when update Storage account with KeyvaultEncryption, to support key auto-rotation</span></span>
    - <span data-ttu-id="f9e89-437">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="f9e89-437">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="f9e89-438">Problemet med borttagning av Azure-filkatalog i pipeline har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="f9e89-438">Fixed remove Azure File Directory fail with pipeline</span></span>
    - <span data-ttu-id="f9e89-439">”Remove-AzStorageDirectory”</span><span class="sxs-lookup"><span data-stu-id="f9e89-439">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="f9e89-440">Åtgärdat [#9880]: Definitionen av DefaultAction-värdet för NetWorkRule har ändrats för konsekvens med Swagger.</span><span class="sxs-lookup"><span data-stu-id="f9e89-440">Fixed [#9880]: Change NetWorkRule DefaultAction value defination to align with swagger.</span></span>
    - <span data-ttu-id="f9e89-441">”Update-AzStorageAccountNetworkRuleSet”</span><span class="sxs-lookup"><span data-stu-id="f9e89-441">'Update-AzStorageAccountNetworkRuleSet'</span></span>
    - <span data-ttu-id="f9e89-442">”Get-AzStorageAccountNetworkRuleSet”</span><span class="sxs-lookup"><span data-stu-id="f9e89-442">'Get-AzStorageAccountNetworkRuleSet'</span></span>
* <span data-ttu-id="f9e89-443">Åtgärdat [#11624]: Hoppa över dubblettregler när NetworkRules läggs till, för att undvika serverfel</span><span class="sxs-lookup"><span data-stu-id="f9e89-443">Fixed [#11624]: Skip duplicated rules when add NetworkRules, to avoid server failure</span></span>
    - <span data-ttu-id="f9e89-444">”Add-AzStorageAccountNetworkRule”</span><span class="sxs-lookup"><span data-stu-id="f9e89-444">'Add-AzStorageAccountNetworkRule'</span></span>
* <span data-ttu-id="f9e89-445">Microsoft.Azure.Cosmos.Table SDK har uppgraderats till 1.0.7</span><span class="sxs-lookup"><span data-stu-id="f9e89-445">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.7</span></span>
* <span data-ttu-id="f9e89-446">Ett varningsmeddelande har lagts till för att påminna användaren om att lista igen med ContinuationToken när endast delobjekt returneras i listan med DataLake Gen2-objekt,</span><span class="sxs-lookup"><span data-stu-id="f9e89-446">Added a warning message to remind user to list again with ContinuationToken when only part items are returned in list DataLake Gen2 Items,</span></span>
    - <span data-ttu-id="f9e89-447">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="f9e89-447">'Get-AzDataLakeGen2ChildItem'</span></span>
* <span data-ttu-id="f9e89-448">Stöd för att skapa eller uppdatera lagringskonto med Azure Files Active Directory Domain Service-autentisering</span><span class="sxs-lookup"><span data-stu-id="f9e89-448">Supported to create or update Storage account with Azure Files Active Directory Domain Service Authentication</span></span>
    -  <span data-ttu-id="f9e89-449">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="f9e89-449">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="f9e89-450">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="f9e89-450">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="f9e89-451">Stöd för nya eller listade Kerberos-nycklar för lagringskontot</span><span class="sxs-lookup"><span data-stu-id="f9e89-451">Supported to new or list Kerberos keys of Storage account</span></span>
    -  <span data-ttu-id="f9e89-452">”New-AzStorageAccountKey”</span><span class="sxs-lookup"><span data-stu-id="f9e89-452">'New-AzStorageAccountKey'</span></span>
    -  <span data-ttu-id="f9e89-453">”Get-AzStorageAccountKey”</span><span class="sxs-lookup"><span data-stu-id="f9e89-453">'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="f9e89-454">Stöd för redundans med lagringskonto</span><span class="sxs-lookup"><span data-stu-id="f9e89-454">Supported failover Storage account</span></span>
    - <span data-ttu-id="f9e89-455">”Invoke-AzStorageAccountFailover”</span><span class="sxs-lookup"><span data-stu-id="f9e89-455">'Invoke-AzStorageAccountFailover'</span></span>
* <span data-ttu-id="f9e89-456">Hjälpen för ”Get-AzStorageBlobCopyState” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="f9e89-456">Updated help of 'Get-AzStorageBlobCopyState'</span></span>
* <span data-ttu-id="f9e89-457">Hjälpen för ”Get-AzStorageFileCopyState” och ”Start-AzStorageBlobCopy” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="f9e89-457">Updated help of 'Get-AzStorageFileCopyState' and 'Start-AzStorageBlobCopy'</span></span>
* <span data-ttu-id="f9e89-458">Lagringsklientbibliotek v12 har integrerats med Queue- och File-cmdletar</span><span class="sxs-lookup"><span data-stu-id="f9e89-458">Integrated Storage client library v12 to Queue and File cmdlets</span></span>
* <span data-ttu-id="f9e89-459">Utdatatypen har ändrats från CloudFile till AzureStorageFile; ursprungliga utdata blir en underordnad egenskap i den nya utmatningen</span><span class="sxs-lookup"><span data-stu-id="f9e89-459">Changed output type from CloudFile to AzureStorageFile, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="f9e89-460">”Get-AzStorageFile”</span><span class="sxs-lookup"><span data-stu-id="f9e89-460">'Get-AzStorageFile'</span></span>
    - <span data-ttu-id="f9e89-461">”Remove-AzStorageFile”</span><span class="sxs-lookup"><span data-stu-id="f9e89-461">'Remove-AzStorageFile'</span></span>
    - <span data-ttu-id="f9e89-462">”Get-AzStorageFileContent”</span><span class="sxs-lookup"><span data-stu-id="f9e89-462">'Get-AzStorageFileContent'</span></span>
    - <span data-ttu-id="f9e89-463">”Set-AzStorageFileContent”</span><span class="sxs-lookup"><span data-stu-id="f9e89-463">'Set-AzStorageFileContent'</span></span>
    - <span data-ttu-id="f9e89-464">”Start-AzStorageFileCopy”</span><span class="sxs-lookup"><span data-stu-id="f9e89-464">'Start-AzStorageFileCopy'</span></span>
* <span data-ttu-id="f9e89-465">Utdatatypen har ändrats från CloudFileDirectory till AzureStorageFileDirectory; ursprungliga utdata blir en underordnad egenskap i den nya utmatningen</span><span class="sxs-lookup"><span data-stu-id="f9e89-465">Changed output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="f9e89-466">”New-AzStorageDirectory”</span><span class="sxs-lookup"><span data-stu-id="f9e89-466">'New-AzStorageDirectory'</span></span>
    - <span data-ttu-id="f9e89-467">”Remove-AzStorageDirectory”</span><span class="sxs-lookup"><span data-stu-id="f9e89-467">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="f9e89-468">Utdatatypen har ändrats från CloudFileShare till AzureStorageFileShare; ursprungliga utdata blir en underordnad egenskap i den nya utmatningen</span><span class="sxs-lookup"><span data-stu-id="f9e89-468">Changed output type from CloudFileShare to AzureStorageFileShare, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="f9e89-469">”Get-AzStorageShare”</span><span class="sxs-lookup"><span data-stu-id="f9e89-469">'Get-AzStorageShare'</span></span>
    - <span data-ttu-id="f9e89-470">”New-AzStorageShare”</span><span class="sxs-lookup"><span data-stu-id="f9e89-470">'New-AzStorageShare'</span></span>
    - <span data-ttu-id="f9e89-471">”Remove-AzStorageShare”</span><span class="sxs-lookup"><span data-stu-id="f9e89-471">'Remove-AzStorageShare'</span></span>
* <span data-ttu-id="f9e89-472">Utdatatypen har ändrats från FileShareProperties till AzureStorageFileShare; ursprungliga utdata blir en underordnad egenskap i den nya utmatningen</span><span class="sxs-lookup"><span data-stu-id="f9e89-472">Changed output type from FileShareProperties to AzureStorageFileShare, the original output will become a sub child property of the new output</span></span>
    - <span data-ttu-id="f9e89-473">”Set-AzStorageShareQuota”</span><span class="sxs-lookup"><span data-stu-id="f9e89-473">'Set-AzStorageShareQuota'</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="f9e89-474">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="f9e89-474">Az.TrafficManager</span></span>
* <span data-ttu-id="f9e89-475">Felaktigt profilnamn har åtgärdats i utförliga utdata för ”DisableAzureTrafficManagerEndpoint”</span><span class="sxs-lookup"><span data-stu-id="f9e89-475">Fixed incorrect profile name in 'DisableAzureTrafficManagerEndpoint' verbose output</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f9e89-476">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f9e89-476">Az.Websites</span></span>
* <span data-ttu-id="f9e89-477">Stavfel har åtgärdats i hjälpen för ”Update-AzWebAppAccessRestrictionConfig”.</span><span class="sxs-lookup"><span data-stu-id="f9e89-477">Fixed typo on help of 'Update-AzWebAppAccessRestrictionConfig'.</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="f9e89-478">3.8.0 – April 2020</span><span class="sxs-lookup"><span data-stu-id="f9e89-478">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="f9e89-479">Höjdpunkter sedan den senaste uppdateringen</span><span class="sxs-lookup"><span data-stu-id="f9e89-479">Highlights since the last release</span></span>
* <span data-ttu-id="f9e89-480">PowerShell-versioner som Az.Storage stöder: Windows PowerShell 5.1, PowerShell Core 6.2.4+ och PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="f9e89-480">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f9e89-481">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f9e89-481">Az.Accounts</span></span>
* <span data-ttu-id="f9e89-482">Uppdaterade URL:en för Azure PowerShell-enkäten i ”Resolve-AzError” [#11507]</span><span class="sxs-lookup"><span data-stu-id="f9e89-482">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="f9e89-483">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f9e89-483">Az.ApiManagement</span></span>
* <span data-ttu-id="f9e89-484">Lade till meddelande om icke-bakåtkompatibel ändring vid ändring i utdata för Azure File-cmdletar i en framtida version</span><span class="sxs-lookup"><span data-stu-id="f9e89-484">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="f9e89-485">"Set-AzApiManagementGroup" Uppdaterad dokumentation för att ange GroupId-parametern</span><span class="sxs-lookup"><span data-stu-id="f9e89-485">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="f9e89-486">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f9e89-486">Az.Cdn</span></span>
* <span data-ttu-id="f9e89-487">Fast ChinaCDN-relaterad prissättning för SKU-visning</span><span class="sxs-lookup"><span data-stu-id="f9e89-487">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f9e89-488">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f9e89-488">Az.CognitiveServices</span></span>
* <span data-ttu-id="f9e89-489">Identitet som stöds, kryptering, UserOwnedStorage</span><span class="sxs-lookup"><span data-stu-id="f9e89-489">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f9e89-490">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f9e89-490">Az.Compute</span></span>
* <span data-ttu-id="f9e89-491">Cmdleten ”Set-AzVmssOrchestrationServiceState” har lagts till.</span><span class="sxs-lookup"><span data-stu-id="f9e89-491">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="f9e89-492">”Get-AzVmss” med -InstanceView visar OrchestrationService-tillstånd.</span><span class="sxs-lookup"><span data-stu-id="f9e89-492">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f9e89-493">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f9e89-493">Az.IotHub</span></span>
* <span data-ttu-id="f9e89-494">Hantera den dubbla konfigurationen för IoT-enheter, nya cmdletar är:</span><span class="sxs-lookup"><span data-stu-id="f9e89-494">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="f9e89-495">'Get-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="f9e89-495">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="f9e89-496">'Update-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="f9e89-496">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="f9e89-497">En cmdlet har lagts till för att anropa direkt metod på en enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="f9e89-497">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="f9e89-498">Hantera dubbel konfiguration för IoT-enhetsmodul, nya cmdletar är:</span><span class="sxs-lookup"><span data-stu-id="f9e89-498">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="f9e89-499">'Get-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="f9e89-499">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="f9e89-500">'Update-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="f9e89-500">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="f9e89-501">Hantera IoT-automatisk konfiguration av enhetshantering i stor skala.</span><span class="sxs-lookup"><span data-stu-id="f9e89-501">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="f9e89-502">Nya cmdlet:ar är:</span><span class="sxs-lookup"><span data-stu-id="f9e89-502">New cmdlets are:</span></span>
    - <span data-ttu-id="f9e89-503">'Add-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="f9e89-503">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="f9e89-504">'Get-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="f9e89-504">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="f9e89-505">'Remove-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="f9e89-505">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="f9e89-506">'Set-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="f9e89-506">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="f9e89-507">En cmdlet har lagts till för att anropa en edge-modulmetod i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="f9e89-507">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f9e89-508">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f9e89-508">Az.KeyVault</span></span>
* <span data-ttu-id="f9e89-509">Har lagt till en ny cmdlet, "Update-AzKeyVault", som kan aktivera mjuk borttagning och rensning av skydd i ett valv</span><span class="sxs-lookup"><span data-stu-id="f9e89-509">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="f9e89-510">Har lagt till stöd i Microsoft.PowerShell.SecretManagement [#11178]</span><span class="sxs-lookup"><span data-stu-id="f9e89-510">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="f9e89-511">Åtgärdat fel i exemplen i 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span><span class="sxs-lookup"><span data-stu-id="f9e89-511">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="f9e89-512">Har lagt till stöd för privat slutpunkt</span><span class="sxs-lookup"><span data-stu-id="f9e89-512">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="f9e89-513">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="f9e89-513">Az.Maintenance</span></span>
* <span data-ttu-id="f9e89-514">Publicerar slutversion av underhålls-cmdletar för GA</span><span class="sxs-lookup"><span data-stu-id="f9e89-514">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f9e89-515">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f9e89-515">Az.Monitor</span></span>
* <span data-ttu-id="f9e89-516">Har lagt till cmdletar för privat länkomfång</span><span class="sxs-lookup"><span data-stu-id="f9e89-516">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="f9e89-517">'Get-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="f9e89-517">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="f9e89-518">'Remove-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="f9e89-518">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="f9e89-519">'New-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="f9e89-519">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="f9e89-520">'Update-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="f9e89-520">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="f9e89-521">'Get-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="f9e89-521">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="f9e89-522">'New-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="f9e89-522">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="f9e89-523">'Remove-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="f9e89-523">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f9e89-524">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f9e89-524">Az.Network</span></span>
* <span data-ttu-id="f9e89-525">Uppdaterade cmdletar för att aktivera anslutning på privat IP för Virtual Network Gateway.</span><span class="sxs-lookup"><span data-stu-id="f9e89-525">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="f9e89-526">'New-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="f9e89-526">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="f9e89-527">'Set-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="f9e89-527">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="f9e89-528">'New-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="f9e89-528">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="f9e89-529">'Set-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="f9e89-529">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="f9e89-530">Uppdaterade cmdletar för att aktivera FQDN-baserade LocalNetworkGateways och VpnSites</span><span class="sxs-lookup"><span data-stu-id="f9e89-530">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="f9e89-531">'New-AzLocalNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="f9e89-531">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="f9e89-532">'New-AzVpnSiteLink'</span><span class="sxs-lookup"><span data-stu-id="f9e89-532">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="f9e89-533">Stöd har lagts till för IPv6-adresstypen i ExpressRouteCircuitConnectionConfig (Global Reach)</span><span class="sxs-lookup"><span data-stu-id="f9e89-533">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="f9e89-534">Lade till 'Set-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="f9e89-534">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="f9e89-535">tillåter inställning av alla befintliga egenskaper inklusive IPv6CircuitConnectionProperties</span><span class="sxs-lookup"><span data-stu-id="f9e89-535">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="f9e89-536">Uppdaterade 'Add-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="f9e89-536">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="f9e89-537">Lade till en ytterligare valfri parameter, AddressPrefixType, för att specificera adresstypen för adressprefix</span><span class="sxs-lookup"><span data-stu-id="f9e89-537">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="f9e89-538">Uppdaterade cmdletar för att aktivera inställningen för DPD-timeout på Virtual Network Gateway-anslutningar.</span><span class="sxs-lookup"><span data-stu-id="f9e89-538">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="f9e89-539">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f9e89-539">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="f9e89-540">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f9e89-540">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f9e89-541">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f9e89-541">Az.PolicyInsights</span></span>
* <span data-ttu-id="f9e89-542">Cmdleten "Start-AzPolicyComplianceScan" har lagts till för att utlösa genomsökningar av principefterlevnad</span><span class="sxs-lookup"><span data-stu-id="f9e89-542">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="f9e89-543">Principdefinition, uppsättningsdefinition och tilldelningsversioner har lagts till i "Get-AzPolicyState"-utdata</span><span class="sxs-lookup"><span data-stu-id="f9e89-543">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f9e89-544">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f9e89-544">Az.ServiceFabric</span></span>
* <span data-ttu-id="f9e89-545">Förbättrad kodformatering och användbarhet för "New-AzServiceFabricCluster"-exempel</span><span class="sxs-lookup"><span data-stu-id="f9e89-545">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="f9e89-546">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f9e89-546">Az.Sql</span></span>
* <span data-ttu-id="f9e89-547">Lade till cmdletarna "Get-AzSqlInstanceOperation" och "Stop-AzSqlInstanceOperation"</span><span class="sxs-lookup"><span data-stu-id="f9e89-547">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="f9e89-548">Stöd för granskning för ett lagringskonto i VNet.</span><span class="sxs-lookup"><span data-stu-id="f9e89-548">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f9e89-549">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f9e89-549">Az.Storage</span></span>
* <span data-ttu-id="f9e89-550">Lade till meddelande om icke-bakåtkompatibel ändring vid ändring i utdata för Azure File-cmdletar i en framtida version</span><span class="sxs-lookup"><span data-stu-id="f9e89-550">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="f9e89-551">Stöd för nya SkuName StandardGZRS, StandardRAGZRS när ett lagringskonto skapas/uppdateras</span><span class="sxs-lookup"><span data-stu-id="f9e89-551">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="f9e89-552">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="f9e89-552">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="f9e89-553">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="f9e89-553">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="f9e89-554">Stöd för DataLake Gen2</span><span class="sxs-lookup"><span data-stu-id="f9e89-554">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="f9e89-555">'New-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="f9e89-555">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="f9e89-556">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="f9e89-556">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="f9e89-557">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="f9e89-557">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="f9e89-558">'Move-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="f9e89-558">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="f9e89-559">'Set-AzDataLakeGen2ItemAclObject'</span><span class="sxs-lookup"><span data-stu-id="f9e89-559">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="f9e89-560">'Update-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="f9e89-560">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="f9e89-561">'Get-AzDataLakeGen2ItemContent'</span><span class="sxs-lookup"><span data-stu-id="f9e89-561">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="f9e89-562">'Remove-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="f9e89-562">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="f9e89-563">0.10.0-förhandsversion – April 2020</span><span class="sxs-lookup"><span data-stu-id="f9e89-563">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="f9e89-564">Allmänt</span><span class="sxs-lookup"><span data-stu-id="f9e89-564">General</span></span>
* <span data-ttu-id="f9e89-565">Az-moduler är nu tillgängliga i förhandsversion på Azure Stack Hub.</span><span class="sxs-lookup"><span data-stu-id="f9e89-565">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="f9e89-566">Därmed möjliggörs kompatibilitet för flera plattformar med Linux och macOs.</span><span class="sxs-lookup"><span data-stu-id="f9e89-566">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="f9e89-567">Azure Stack Hub stöder nu PowerShell Core med AZ-moduler. Mer information finns [här](https://aka.ms/az4AzureStack)</span><span class="sxs-lookup"><span data-stu-id="f9e89-567">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](https://aka.ms/az4AzureStack)</span></span>
* <span data-ttu-id="f9e89-568">Supportprofil för AZ-moduler 2019-03-01-hybrid:</span><span class="sxs-lookup"><span data-stu-id="f9e89-568">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="f9e89-569">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="f9e89-569">Az.Billing</span></span>
  - <span data-ttu-id="f9e89-570">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f9e89-570">Az.Compute</span></span>
  - <span data-ttu-id="f9e89-571">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="f9e89-571">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="f9e89-572">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f9e89-572">Az.EventHub</span></span>
  - <span data-ttu-id="f9e89-573">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f9e89-573">Az.IotHub</span></span>
  - <span data-ttu-id="f9e89-574">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f9e89-574">Az.KeyVault</span></span>
  - <span data-ttu-id="f9e89-575">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f9e89-575">Az.Monitor</span></span>
  - <span data-ttu-id="f9e89-576">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f9e89-576">Az.Network</span></span>
  - <span data-ttu-id="f9e89-577">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f9e89-577">Az.Resources</span></span>
  - <span data-ttu-id="f9e89-578">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f9e89-578">Az.Storage</span></span>
  - <span data-ttu-id="f9e89-579">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f9e89-579">Az.Websites</span></span>
* <span data-ttu-id="f9e89-580">Tre nya PowerShell-moduler för AZ har introducerats som fungerar med Azure Stack Hub, och de är Az.Databox, Az.IotHub och Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f9e89-580">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="f9e89-581">Kommandona är i princip oförändrade, med endast mindre ändringar som att AzureRM ändras till AZ</span><span class="sxs-lookup"><span data-stu-id="f9e89-581">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="f9e89-582">En uppdaterad länk till PowerShell-dokumentationen för Azure Stack Hub finns [här](https://aka.ms/InstallASHPowerShell)</span><span class="sxs-lookup"><span data-stu-id="f9e89-582">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](https://aka.ms/InstallASHPowerShell)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="f9e89-583">3.7.0 – mars 2020</span><span class="sxs-lookup"><span data-stu-id="f9e89-583">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f9e89-584">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f9e89-584">Az.Accounts</span></span>
* <span data-ttu-id="f9e89-585">Åtgärdade ”Get-AzTenant”/”Get-AzDefault”/”Set-AzDefault”-utlösning av NullReferenceException när du inte är inloggad [#10292]</span><span class="sxs-lookup"><span data-stu-id="f9e89-585">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f9e89-586">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f9e89-586">Az.Compute</span></span>
* <span data-ttu-id="f9e89-587">Följande parametrar har lagts till i cmdleten ”New-AzDiskConfig”:</span><span class="sxs-lookup"><span data-stu-id="f9e89-587">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="f9e89-588">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="f9e89-588">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="f9e89-589">Tillåten krypteringsegenskap till målparametern för cmdleten ”New-AzGalleryImageVersion”.</span><span class="sxs-lookup"><span data-stu-id="f9e89-589">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="f9e89-590">Åtgärdade tempDisk-problem för cmdletarna ”Set-AzVmss”-Reimage och ”Invoke-AzVMReimage”.</span><span class="sxs-lookup"><span data-stu-id="f9e89-590">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="f9e89-591">[#11354]</span><span class="sxs-lookup"><span data-stu-id="f9e89-591">[#11354]</span></span>
* <span data-ttu-id="f9e89-592">Stöd har lagts till i nedanstående cmdletar för nytt SAP-tillägg</span><span class="sxs-lookup"><span data-stu-id="f9e89-592">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="f9e89-593">”Set-AzVMAEMExtension”</span><span class="sxs-lookup"><span data-stu-id="f9e89-593">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="f9e89-594">”Get-AzVMAEMExtension”</span><span class="sxs-lookup"><span data-stu-id="f9e89-594">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="f9e89-595">”Remove-AzVMAEMExtension”</span><span class="sxs-lookup"><span data-stu-id="f9e89-595">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="f9e89-596">”Update-AzVMAEMExtension”</span><span class="sxs-lookup"><span data-stu-id="f9e89-596">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="f9e89-597">Åtgärdade fel i exempel på hjälpdokument</span><span class="sxs-lookup"><span data-stu-id="f9e89-597">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="f9e89-598">Visade det exakta strängvärdet för VM PowerState i tabellformat.</span><span class="sxs-lookup"><span data-stu-id="f9e89-598">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="f9e89-599">”New-AzVmssConfig”: den fasta serialiseringen av egenskapen AutomaticRepairs när SinglePlacementGroup är inaktiverad.</span><span class="sxs-lookup"><span data-stu-id="f9e89-599">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="f9e89-600">[#11257]</span><span class="sxs-lookup"><span data-stu-id="f9e89-600">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f9e89-601">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f9e89-601">Az.DataFactory</span></span>
* <span data-ttu-id="f9e89-602">ADF .Net SDK har uppdaterats till 4.8.0</span><span class="sxs-lookup"><span data-stu-id="f9e89-602">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="f9e89-603">Valfria parametrar har lagts till i kommandot ”Invoke-AzDataFactoryV2Pipeline” för att stödja omkörning</span><span class="sxs-lookup"><span data-stu-id="f9e89-603">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f9e89-604">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f9e89-604">Az.DataLakeStore</span></span>
* <span data-ttu-id="f9e89-605">Lade till beskrivning för icke-bakåtkompatibel ändring för ”Export-AzDataLakeStoreItem” och ”Import-AzDataLakeStoreItem”</span><span class="sxs-lookup"><span data-stu-id="f9e89-605">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="f9e89-606">Lade till alternativ för bytekodning för ”New-AzDataLakeStoreItem”, ”Add-AzDAtaLakeStoreItemContent” och ”Get-AzDAtaLakeStoreItemContent”</span><span class="sxs-lookup"><span data-stu-id="f9e89-606">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="f9e89-607">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f9e89-607">Az.HDInsight</span></span>
* <span data-ttu-id="f9e89-608">Stöd för att ange en minimal TLS-version som stöds när klustret skapas.</span><span class="sxs-lookup"><span data-stu-id="f9e89-608">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f9e89-609">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f9e89-609">Az.IotHub</span></span>
* <span data-ttu-id="f9e89-610">Stöd har lagts till för att hantera distribuerade inställningar per enhet.</span><span class="sxs-lookup"><span data-stu-id="f9e89-610">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="f9e89-611">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="f9e89-611">New Cmdlets are:</span></span>
    - <span data-ttu-id="f9e89-612">”Get-AzIotHubDistributedTracing”</span><span class="sxs-lookup"><span data-stu-id="f9e89-612">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="f9e89-613">”Set-AzIotHubDistributedTracing”</span><span class="sxs-lookup"><span data-stu-id="f9e89-613">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f9e89-614">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f9e89-614">Az.KeyVault</span></span>
* <span data-ttu-id="f9e89-615">Ändrade attribut för icke-bakåtkompatibel ändring lades till för ”New-AzKeyVault”</span><span class="sxs-lookup"><span data-stu-id="f9e89-615">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f9e89-616">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f9e89-616">Az.Monitor</span></span>
* <span data-ttu-id="f9e89-617">Uppdaterad dokumentation för ”New-AzScheduledQueryRuleLogMetricTrigger”</span><span class="sxs-lookup"><span data-stu-id="f9e89-617">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f9e89-618">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f9e89-618">Az.Network</span></span>
* <span data-ttu-id="f9e89-619">Uppdaterade cmdletar för att tillåta VirtualHubVnetConnections mellan klienter</span><span class="sxs-lookup"><span data-stu-id="f9e89-619">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="f9e89-620">”New-AzVirtualHubVnetConnection”</span><span class="sxs-lookup"><span data-stu-id="f9e89-620">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="f9e89-621">”Update-AzVirtualHubVnetConnection”</span><span class="sxs-lookup"><span data-stu-id="f9e89-621">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="f9e89-622">”New-AzVirtualHub”</span><span class="sxs-lookup"><span data-stu-id="f9e89-622">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="f9e89-623">”Update-AzVirtualHub”</span><span class="sxs-lookup"><span data-stu-id="f9e89-623">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="f9e89-624">SQL Management SDK-beroende har tagits bort</span><span class="sxs-lookup"><span data-stu-id="f9e89-624">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f9e89-625">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f9e89-625">Az.PolicyInsights</span></span>
* <span data-ttu-id="f9e89-626">Förbättrade felmeddelanden</span><span class="sxs-lookup"><span data-stu-id="f9e89-626">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f9e89-627">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f9e89-627">Az.RecoveryServices</span></span>
* <span data-ttu-id="f9e89-628">Azure Site Recovery har lagt till stöd för återaktivering av skydd och uppdaterade VM-egenskaper för virtuella Azure-datorer med krypterad disk.</span><span class="sxs-lookup"><span data-stu-id="f9e89-628">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="f9e89-629">Lade till Azure Site Recovery VmwareToAzure-egenskaper för DR-övervakning</span><span class="sxs-lookup"><span data-stu-id="f9e89-629">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="f9e89-630">Azure Backup har lagt till stöd för att försöka uppdatera principuppdateringen för misslyckade objekt på nytt.</span><span class="sxs-lookup"><span data-stu-id="f9e89-630">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="f9e89-631">Azure Backup lagt till stöd för diskundantagsinställningar under säkerhetskopiering och återställning.</span><span class="sxs-lookup"><span data-stu-id="f9e89-631">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="f9e89-632">Azure Backup lagt till stöd för att återställa flera filer/mappar i AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="f9e89-632">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="f9e89-633">Azure Backup lade till support för användardefinierad Resourcegroup-support vid uppdatering av IaasVM-princip</span><span class="sxs-lookup"><span data-stu-id="f9e89-633">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="f9e89-634">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f9e89-634">Az.Resources</span></span>
* <span data-ttu-id="f9e89-635">Åtgärdade ”Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType” så att den använder den faktisk apiVersion av resurser i stället för standard-apiVersion [#11267]</span><span class="sxs-lookup"><span data-stu-id="f9e89-635">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="f9e89-636">Lade till correlationId-loggning för felscenarier</span><span class="sxs-lookup"><span data-stu-id="f9e89-636">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="f9e89-637">Liten dokumentationsändring för ”Get-AzResourceLock”.</span><span class="sxs-lookup"><span data-stu-id="f9e89-637">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="f9e89-638">Lade till exempel.</span><span class="sxs-lookup"><span data-stu-id="f9e89-638">Added example.</span></span>
* <span data-ttu-id="f9e89-639">Undantaget enkelt citattecken i parametervärde för ”Get-AzADUser” [#11317]</span><span class="sxs-lookup"><span data-stu-id="f9e89-639">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="f9e89-640">Nya cmdletar har lagts till för distributionsskript (”Get-AzDeploymentScript”, ”Get-AzDeploymentScriptLog”, ”Save-AzDeploymentScriptLog”, ”Remove-AzDeploymentScript”)</span><span class="sxs-lookup"><span data-stu-id="f9e89-640">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="f9e89-641">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f9e89-641">Az.Sql</span></span>
* <span data-ttu-id="f9e89-642">En läsbar sekundär parameter har lagts till i Invoke-AzSqlDatabaseFailover</span><span class="sxs-lookup"><span data-stu-id="f9e89-642">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="f9e89-643">Cmdleten Disable-AzSqlServerActiveDirectoryOnlyAuthentication har lagts till</span><span class="sxs-lookup"><span data-stu-id="f9e89-643">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="f9e89-644">Den sparade känslighet rangordningen när kolumner klassificeras i databasen.</span><span class="sxs-lookup"><span data-stu-id="f9e89-644">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="f9e89-645">Az.Support</span><span class="sxs-lookup"><span data-stu-id="f9e89-645">Az.Support</span></span>
* <span data-ttu-id="f9e89-646">Allmän tillgänglighet för ”Az.Support”-modulen</span><span class="sxs-lookup"><span data-stu-id="f9e89-646">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f9e89-647">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f9e89-647">Az.Websites</span></span>
* <span data-ttu-id="f9e89-648">Stöd har lagts till för att arbeta med trafikdirigeringsregler för webbappar under nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="f9e89-648">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="f9e89-649">”Get-AzWebAppTrafficRouting”</span><span class="sxs-lookup"><span data-stu-id="f9e89-649">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="f9e89-650">”Update-AzWebAppTrafficRouting”</span><span class="sxs-lookup"><span data-stu-id="f9e89-650">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="f9e89-651">”Add-AzWebAppTrafficRouting”</span><span class="sxs-lookup"><span data-stu-id="f9e89-651">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="f9e89-652">”Remove-AzWebAppTrafficRouting”</span><span class="sxs-lookup"><span data-stu-id="f9e89-652">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="f9e89-653">3.6.1 – mars 2020</span><span class="sxs-lookup"><span data-stu-id="f9e89-653">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f9e89-654">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f9e89-654">Az.Accounts</span></span>
* <span data-ttu-id="f9e89-655">Öppna sidan med Azure PowerShell-enkäten i ”Send-Feedback” [#11020]</span><span class="sxs-lookup"><span data-stu-id="f9e89-655">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="f9e89-656">Visa URL:en för Azure PowerShell-enkäten i ”Resolve-Error” [#11021]</span><span class="sxs-lookup"><span data-stu-id="f9e89-656">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="f9e89-657">Az-version har lagts till i UserAgent</span><span class="sxs-lookup"><span data-stu-id="f9e89-657">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="f9e89-658">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f9e89-658">Az.ApiManagement</span></span>
* <span data-ttu-id="f9e89-659">Stöd har lagts till för att hämta och konfigurera en anpassad domän på DeveloperPortal-slutpunkten [#11007]</span><span class="sxs-lookup"><span data-stu-id="f9e89-659">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="f9e89-660">”Export-AzApiManagementApi” Stöd har lagts till för att ladda ned API-definition i Json-format [#9987]</span><span class="sxs-lookup"><span data-stu-id="f9e89-660">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="f9e89-661">”Import-AzApiManagementApi” Stöd har lagts till för att importera OpenApi 3.0-definition från Json-dokument</span><span class="sxs-lookup"><span data-stu-id="f9e89-661">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="f9e89-662">”New-AzApiManagementIdentityProvider” och ”Set-AzApiManagementIdentityProvider” Stöd har lagts till för att konfigurera ”Signin Tenant” för AAD B2C-provider [#9784]</span><span class="sxs-lookup"><span data-stu-id="f9e89-662">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f9e89-663">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f9e89-663">Az.DataLakeStore</span></span>
* <span data-ttu-id="f9e89-664">En referens har uttryckligen lagts till för System.Buffers i csproj och psd1.</span><span class="sxs-lookup"><span data-stu-id="f9e89-664">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f9e89-665">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f9e89-665">Az.IotHub</span></span>
* <span data-ttu-id="f9e89-666">Lade till stöd för att hantera enheter i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="f9e89-666">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="f9e89-667">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="f9e89-667">New Cmdlets are:</span></span>
    - <span data-ttu-id="f9e89-668">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="f9e89-668">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="f9e89-669">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="f9e89-669">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="f9e89-670">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="f9e89-670">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="f9e89-671">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="f9e89-671">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="f9e89-672">Stöd har lagts till för att hantera moduler på en mål-IoT-enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="f9e89-672">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="f9e89-673">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="f9e89-673">New Cmdlets are:</span></span>
    - <span data-ttu-id="f9e89-674">”Add-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="f9e89-674">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="f9e89-675">”Get-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="f9e89-675">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="f9e89-676">”Remove-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="f9e89-676">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="f9e89-677">”Set-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="f9e89-677">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="f9e89-678">Cmdlet har lagts till för att hämta anslutningssträngen för en mål-IoT-enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="f9e89-678">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="f9e89-679">Cmdlet har lagts till för att hämta anslutningssträngen för en modul på en mål-IoT-enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="f9e89-679">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="f9e89-680">Stöd har lagts till för att hämta/ange en överordnad enhet för en IoT-enhet.</span><span class="sxs-lookup"><span data-stu-id="f9e89-680">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="f9e89-681">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="f9e89-681">New Cmdlets are:</span></span>
    - <span data-ttu-id="f9e89-682">”Get-AzIotHubDeviceParent”</span><span class="sxs-lookup"><span data-stu-id="f9e89-682">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="f9e89-683">”Set-AzIotHubDeviceParent”</span><span class="sxs-lookup"><span data-stu-id="f9e89-683">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="f9e89-684">Stöd har lagts till för att hantera en enhets överordnade och underordnade relationer.</span><span class="sxs-lookup"><span data-stu-id="f9e89-684">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f9e89-685">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f9e89-685">Az.Monitor</span></span>
* <span data-ttu-id="f9e89-686">Utdatavärdet har åtgärdats för ”Get-AzMetricDefinition” [#9714]</span><span class="sxs-lookup"><span data-stu-id="f9e89-686">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f9e89-687">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f9e89-687">Az.Network</span></span>
* <span data-ttu-id="f9e89-688">SQL Management SDK har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="f9e89-688">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="f9e89-689">Ett problem har åtgärdats med namngivningsskillnader i klassen PrivateLinkServiceConnectionState.</span><span class="sxs-lookup"><span data-stu-id="f9e89-689">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="f9e89-690">Fältet ActionsRequired mappar till ActionRequired.</span><span class="sxs-lookup"><span data-stu-id="f9e89-690">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="f9e89-691">PublicNetworkAccess har lagts till i ”New-AzSqlServer” och ”Set-AzSqlServer”</span><span class="sxs-lookup"><span data-stu-id="f9e89-691">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="f9e89-692">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f9e89-692">Az.Resources</span></span>
* <span data-ttu-id="f9e89-693">Null-referensfel har åtgärdats i ”Get-AzRoleAssignment”</span><span class="sxs-lookup"><span data-stu-id="f9e89-693">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="f9e89-694">Växlarna ”-Force” och ”-PassThru” är valfria i ”Remove-AzADGroup” [#10849]</span><span class="sxs-lookup"><span data-stu-id="f9e89-694">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="f9e89-695">Ett problem har åtgärdats som gjorde att ”MailNickname” inte returnerades i ”Remove-AzADGroup” [#11167]</span><span class="sxs-lookup"><span data-stu-id="f9e89-695">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="f9e89-696">Ett problem har åtgärdats som gjorde att pipe-åtgärden ”Remove-AzADGroup” inte fungerar [#11171]</span><span class="sxs-lookup"><span data-stu-id="f9e89-696">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="f9e89-697">Ett null-referensfel har åtgärdats i GetAzureRoleAssignmentCommand</span><span class="sxs-lookup"><span data-stu-id="f9e89-697">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="f9e89-698">Attribut för icke-bakåtkompatibla ändringar har lagts till för kommande ändringar i cmdlets för principer</span><span class="sxs-lookup"><span data-stu-id="f9e89-698">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="f9e89-699">”Get-AzResourceGroup” har uppdaterats för att utföra taggfiltrering för resursgrupper på serversidan</span><span class="sxs-lookup"><span data-stu-id="f9e89-699">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="f9e89-700">Utökade Tag-cmdlets stöder -ResourceId</span><span class="sxs-lookup"><span data-stu-id="f9e89-700">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="f9e89-701">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="f9e89-701">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="f9e89-702">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="f9e89-702">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="f9e89-703">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="f9e89-703">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="f9e89-704">Ny Tag-cmdlet har lagts till</span><span class="sxs-lookup"><span data-stu-id="f9e89-704">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="f9e89-705">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="f9e89-705">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="f9e89-706">Flyttade ScopedDeployment från SDK 3.3.0</span><span class="sxs-lookup"><span data-stu-id="f9e89-706">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="f9e89-707">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f9e89-707">Az.Sql</span></span>
* <span data-ttu-id="f9e89-708">PublicNetworkAccess har lagts till i ”New-AzSqlServer” och ”Set-AzSqlServer”</span><span class="sxs-lookup"><span data-stu-id="f9e89-708">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="f9e89-709">Stöd har lagts till för konfiguration av säkerhetskopiering för långsiktig kvarhållning för hanterade databaser</span><span class="sxs-lookup"><span data-stu-id="f9e89-709">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="f9e89-710">Hämta/ange LTR-princip på en hanterad databas</span><span class="sxs-lookup"><span data-stu-id="f9e89-710">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="f9e89-711">Hämta LTR-säkerhetskopior efter hanterad databas, hanterad instans eller plats</span><span class="sxs-lookup"><span data-stu-id="f9e89-711">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="f9e89-712">Ta bort en LTR-säkerhetskopia</span><span class="sxs-lookup"><span data-stu-id="f9e89-712">Remove an LTR backup</span></span>
    - <span data-ttu-id="f9e89-713">Återställa en LTR-säkerhetskopia för att skapa en ny hanterad databas</span><span class="sxs-lookup"><span data-stu-id="f9e89-713">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="f9e89-714">MinimalTlsVersion har lagts till för New-AzSqlServer och Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="f9e89-714">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="f9e89-715">MinimalTlsVersion har lagts till för New-AzSqlInstance och Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="f9e89-715">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="f9e89-716">SQL SDK-versionen för Az.Network har ändrats</span><span class="sxs-lookup"><span data-stu-id="f9e89-716">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f9e89-717">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f9e89-717">Az.Storage</span></span>
* <span data-ttu-id="f9e89-718">AllowProtectedAppendWrite stöds i ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="f9e89-718">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="f9e89-719">”Set-AzRmStorageContainerImmutabilityPolicy”</span><span class="sxs-lookup"><span data-stu-id="f9e89-719">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="f9e89-720">Varningsmeddelande har lagts till om icke-bakåtkompatibel ändring för ändring av typen AzureStorageTable i en senare version</span><span class="sxs-lookup"><span data-stu-id="f9e89-720">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="f9e89-721">”New-AzStorageTable”</span><span class="sxs-lookup"><span data-stu-id="f9e89-721">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="f9e89-722">”Get-AzStorageTable”</span><span class="sxs-lookup"><span data-stu-id="f9e89-722">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f9e89-723">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f9e89-723">Az.Websites</span></span>
* <span data-ttu-id="f9e89-724">Tag-parametern har lagts till för ”New-AzAppServicePlan” och ”Set-AzAppServicePlan”</span><span class="sxs-lookup"><span data-stu-id="f9e89-724">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="f9e89-725">Stoppa cmdlet-körning om ett undantag uppstår när en anpassad domän läggs till på en webbplats</span><span class="sxs-lookup"><span data-stu-id="f9e89-725">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="f9e89-726">Stöd har lagts till för att utföra åtgärder för App Services som inte tillhör samma resursgrupp som App Services-planen</span><span class="sxs-lookup"><span data-stu-id="f9e89-726">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="f9e89-727">Åtkomstbegränsning har tillämpats på WebApp/Function i olika resursgrupper</span><span class="sxs-lookup"><span data-stu-id="f9e89-727">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="f9e89-728">Ett problem har åtgärdats för att ange anpassade värdnamn för WebAppSlots</span><span class="sxs-lookup"><span data-stu-id="f9e89-728">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="f9e89-729">3.5.0 – februari 2020</span><span class="sxs-lookup"><span data-stu-id="f9e89-729">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="f9e89-730">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="f9e89-730">Highlights since the last major release</span></span>
* <span data-ttu-id="f9e89-731">Uppdaterade telemetri på klientsidan.</span><span class="sxs-lookup"><span data-stu-id="f9e89-731">Updated client side telemetry.</span></span>
* <span data-ttu-id="f9e89-732">Az.IotHub lade till cmdletar som stöd för att hantera enheter.</span><span class="sxs-lookup"><span data-stu-id="f9e89-732">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="f9e89-733">Az.SqlVirtualMachine lade till cmdletar för lyssningsfunktion för tillgänglighetsgrupp.</span><span class="sxs-lookup"><span data-stu-id="f9e89-733">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f9e89-734">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f9e89-734">Az.Accounts</span></span>
* <span data-ttu-id="f9e89-735">Lade till SubscriptionId, TenantId och körningstid i data för telemetri på klientsidan</span><span class="sxs-lookup"><span data-stu-id="f9e89-735">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f9e89-736">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f9e89-736">Az.Automation</span></span>
* <span data-ttu-id="f9e89-737">Åtgärdade skrivfel i exempel 1 i referensdokumentation för ”New-AzAutomationSoftwareUpdateConfiguration”</span><span class="sxs-lookup"><span data-stu-id="f9e89-737">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f9e89-738">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f9e89-738">Az.CognitiveServices</span></span>
* <span data-ttu-id="f9e89-739">Uppdaterade SDK till 7.0</span><span class="sxs-lookup"><span data-stu-id="f9e89-739">Updated SDK to 7.0</span></span>
* <span data-ttu-id="f9e89-740">Förbättrade felmeddelande vid serversvar om tom brödtext</span><span class="sxs-lookup"><span data-stu-id="f9e89-740">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f9e89-741">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f9e89-741">Az.Compute</span></span>
* <span data-ttu-id="f9e89-742">Tillät tomt värde för ProximityPlacementGroupId under uppdatering</span><span class="sxs-lookup"><span data-stu-id="f9e89-742">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="f9e89-743">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f9e89-743">Az.FrontDoor</span></span>
* <span data-ttu-id="f9e89-744">Lade till cmdlet för att hämta hanterade regeldefinitioner som kan användas i WAF</span><span class="sxs-lookup"><span data-stu-id="f9e89-744">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f9e89-745">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f9e89-745">Az.IotHub</span></span>
* <span data-ttu-id="f9e89-746">Lade till stöd för att hantera enheter i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="f9e89-746">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="f9e89-747">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="f9e89-747">New Cmdlets are:</span></span>
    - <span data-ttu-id="f9e89-748">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="f9e89-748">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="f9e89-749">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="f9e89-749">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="f9e89-750">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="f9e89-750">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="f9e89-751">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="f9e89-751">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f9e89-752">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f9e89-752">Az.KeyVault</span></span>
* <span data-ttu-id="f9e89-753">Åtgärdade duplicerad text för Add-AzKeyVaultKey.md</span><span class="sxs-lookup"><span data-stu-id="f9e89-753">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f9e89-754">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f9e89-754">Az.Monitor</span></span>
* <span data-ttu-id="f9e89-755">Åtgärdade beskrivning av cmdleten Get-AzLog.</span><span class="sxs-lookup"><span data-stu-id="f9e89-755">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="f9e89-756">En ny parameter med namnet ActionGroupId har lagts till i kommandot ”New-AzMetricAlertRuleV2”.</span><span class="sxs-lookup"><span data-stu-id="f9e89-756">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="f9e89-757">Användaren kan ange ActionGroupId(string) eller ActionGroup(ActivityLogAlertActionGroup).</span><span class="sxs-lookup"><span data-stu-id="f9e89-757">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f9e89-758">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f9e89-758">Az.Network</span></span>
* <span data-ttu-id="f9e89-759">Lade till en extra parameteranteckning för parametern ”-EnableProxyProtocol” för cmdleten ”New-AzPrivateLinkService”.</span><span class="sxs-lookup"><span data-stu-id="f9e89-759">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="f9e89-760">Åtgärdade FilterData-exempel i Start-AzVirtualNetworkGatewayConnectionPacketCapture.md och Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="f9e89-760">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="f9e89-761">Lade till paketinsamlingsexempel för att samla in alla inre och yttre paket i Start-AzVirtualNetworkGatewayConnectionPacketCapture.md och Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="f9e89-761">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="f9e89-762">Lade till stöd för Azure-brandväggsprincip på VNet-brandväggar</span><span class="sxs-lookup"><span data-stu-id="f9e89-762">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="f9e89-763">Inga nya cmdletar har lagts till.</span><span class="sxs-lookup"><span data-stu-id="f9e89-763">No new cmdlets are added.</span></span> <span data-ttu-id="f9e89-764">Lättar begränsningen för brandväggsprincip på VNet-brandväggar</span><span class="sxs-lookup"><span data-stu-id="f9e89-764">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f9e89-765">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f9e89-765">Az.RecoveryServices</span></span>
* <span data-ttu-id="f9e89-766">Lade till stöd för Restore-as-files för SQL-databaser.</span><span class="sxs-lookup"><span data-stu-id="f9e89-766">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f9e89-767">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f9e89-767">Az.Resources</span></span>
* <span data-ttu-id="f9e89-768">Omstrukturerade cmdletar för malldistribution</span><span class="sxs-lookup"><span data-stu-id="f9e89-768">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="f9e89-769">Lade till nya cmdletar för att hantera distributioner i hanteringsgruppen: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f9e89-769">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="f9e89-770">Lade till nya cmdletar för att hantera distributioner i klientorganisationsområdet: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="f9e89-770">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="f9e89-771">Omstrukturerade \*-AzDeployment-cmdletar för att fungera specifikt i prenumerationsomfattningen</span><span class="sxs-lookup"><span data-stu-id="f9e89-771">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="f9e89-772">Skapade alias \*-AzSubscriptionDeployment för \*-AzDeployment-cmdletar</span><span class="sxs-lookup"><span data-stu-id="f9e89-772">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="f9e89-773">Åtgärdade ”Update-AzADApplication” när parametern ”AvailableToOtherTenants” inte har angetts</span><span class="sxs-lookup"><span data-stu-id="f9e89-773">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="f9e89-774">Tog bort ApplicationObjectWithoutCredentialParameterSet för att undvika AmbiguousParameterSetException.</span><span class="sxs-lookup"><span data-stu-id="f9e89-774">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="f9e89-775">Återskapade hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="f9e89-775">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="f9e89-776">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f9e89-776">Az.Sql</span></span>
* <span data-ttu-id="f9e89-777">Lade till stöd för återställning till tidpunkt mellan prenumerationer på hanterade instanser.</span><span class="sxs-lookup"><span data-stu-id="f9e89-777">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="f9e89-778">Lade till stöd för att ändra befintlig SQL Managed Instance-maskinvarugenerering</span><span class="sxs-lookup"><span data-stu-id="f9e89-778">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="f9e89-779">Åtgärdade ”Update-AzSqlServerVulnerabilityAssessmentSetting”-hjälpexempel: parameter/egenskapsutdata - EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="f9e89-779">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="f9e89-780">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="f9e89-780">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="f9e89-781">Lade till cmdletar för lyssningsfunktion för tillgänglighetsgrupp</span><span class="sxs-lookup"><span data-stu-id="f9e89-781">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="f9e89-782">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="f9e89-782">Az.StorageSync</span></span>
* <span data-ttu-id="f9e89-783">Uppdaterade teckenuppsättningar som stöds i ”Invoke-AzStorageSyncCompatibilityCheck”.</span><span class="sxs-lookup"><span data-stu-id="f9e89-783">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="f9e89-784">3.4.0 – februari 2020</span><span class="sxs-lookup"><span data-stu-id="f9e89-784">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="f9e89-785">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="f9e89-785">Highlights since the last major release</span></span>
* <span data-ttu-id="f9e89-786">Första Az.CosmosDB-versionen 0.1.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="f9e89-786">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="f9e89-787">Stöd för Az.Network ConnectionMonitor V2 har lagts till</span><span class="sxs-lookup"><span data-stu-id="f9e89-787">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f9e89-788">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f9e89-788">Az.Accounts</span></span>
* <span data-ttu-id="f9e89-789">Inaktivera automatisk sparande av kontext när AzureRmContext.json inte är tillgängligt</span><span class="sxs-lookup"><span data-stu-id="f9e89-789">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="f9e89-790">Uppdatera referensen till Azure Powershell Common till 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="f9e89-790">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="f9e89-791">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f9e89-791">Az.ApiManagement</span></span>
* <span data-ttu-id="f9e89-792">**Get-AzApiManagementApiSchema** Hämtning av Open-Api-schema som är associerat med ett API har åtgärdats   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="f9e89-792">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="f9e89-793">**New-AzApiManagementProduct**\* och **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="f9e89-793">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="f9e89-794">Åtgärda dokumentation för https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="f9e89-794">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="f9e89-795">**Set-AzApiManagementApi** Exempel för att visa hur ServiceUrl uppdateras med hjälp av cmdleten har lagts till</span><span class="sxs-lookup"><span data-stu-id="f9e89-795">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f9e89-796">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f9e89-796">Az.Compute</span></span>
* <span data-ttu-id="f9e89-797">Begränsa antalet VM-status till 100 för att undvika begränsning när Get-AzVM -Status utförs utan VM-namn.</span><span class="sxs-lookup"><span data-stu-id="f9e89-797">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="f9e89-798">Lägg till cmdleten Update-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="f9e89-798">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="f9e89-799">Lägg till parametrarna EncryptionType och DiskEncryptionSetId i följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="f9e89-799">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="f9e89-800">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="f9e89-800">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="f9e89-801">Lägg till parametern ColocationStatus för cmdleten Get-AzProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="f9e89-801">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f9e89-802">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f9e89-802">Az.DataFactory</span></span>
* <span data-ttu-id="f9e89-803">Uppdatera ADF .Net SDK-versionen till 4.7.0</span><span class="sxs-lookup"><span data-stu-id="f9e89-803">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="f9e89-804">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="f9e89-804">Az.DeploymentManager</span></span>
* <span data-ttu-id="f9e89-805">Lägger till LIST-åtgärder för resurser</span><span class="sxs-lookup"><span data-stu-id="f9e89-805">Adds LIST operations for resources</span></span>
* <span data-ttu-id="f9e89-806">Lägger till funktion för att utföra åtgärder för hälsokontrollsteg</span><span class="sxs-lookup"><span data-stu-id="f9e89-806">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="f9e89-807">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f9e89-807">Az.HDInsight</span></span>
* <span data-ttu-id="f9e89-808">Åtgärda dokumentfel för New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="f9e89-808">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f9e89-809">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f9e89-809">Az.KeyVault</span></span>
* <span data-ttu-id="f9e89-810">Lägg till Name-alias för attributet VaultName så att Remove-AzureKeyVault stämmer överens med New-AzureKeyVault.</span><span class="sxs-lookup"><span data-stu-id="f9e89-810">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f9e89-811">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f9e89-811">Az.Network</span></span>
* <span data-ttu-id="f9e89-812">Nytt exempel har lagts till i Set-AzNetworkWatcherConfigFlowLog.md för att demonstrera ett inaktiveringsscenario för Trafikanalys.</span><span class="sxs-lookup"><span data-stu-id="f9e89-812">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="f9e89-813">Lägg till stöd för att tilldela konfiguration av hanterings-IP till Azure Firewall – ett dedikerat undernät och en offentlig IP som brandväggen använder för dess hanteringstrafik</span><span class="sxs-lookup"><span data-stu-id="f9e89-813">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="f9e89-814">Cmdleten New-AzFirewall har uppdaterats:</span><span class="sxs-lookup"><span data-stu-id="f9e89-814">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="f9e89-815">Parametern -ManagementPublicIpAddress (inte obligatorisk) som accepterar ett offentligt IP-adressobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="f9e89-815">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="f9e89-816">Metoden SetManagementIpConfiguration har lagts till för brandväggsobjekt – kräver ett undernät och en offentlig IP-adress som indata – undernätets namn måste vara ”AzureFirewallManagementSubnet”</span><span class="sxs-lookup"><span data-stu-id="f9e89-816">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="f9e89-817">Exempel för Get-AzNetworkSecurityGroup har korrigerats så att exempel visas för NSG:er i stället för nätverksgränssnitt.</span><span class="sxs-lookup"><span data-stu-id="f9e89-817">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="f9e89-818">Ett skrivfel har åtgärdats i kommandot New-AzVpnSite som hindrade kompletteraren för resurs-ID från att fylla i en parameter.</span><span class="sxs-lookup"><span data-stu-id="f9e89-818">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="f9e89-819">Stöd för Url-konfiguration i åtgärdsuppsättningen för omskrivningsregler i Application Gateway har lagts till</span><span class="sxs-lookup"><span data-stu-id="f9e89-819">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="f9e89-820">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="f9e89-820">New cmdlets added:</span></span>
        - <span data-ttu-id="f9e89-821">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="f9e89-821">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="f9e89-822">Cmdletar har uppdaterats med den valfria parametern -UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="f9e89-822">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="f9e89-823">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="f9e89-823">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="f9e89-824">Lägg till stöd för resurser för NetworkWatcher ConnectionMonitor version 2</span><span class="sxs-lookup"><span data-stu-id="f9e89-824">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f9e89-825">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f9e89-825">Az.PolicyInsights</span></span>
* <span data-ttu-id="f9e89-826">Stöd för utvärdering av efterlevnad innan fastställande av vilken resurs som ska åtgärdas</span><span class="sxs-lookup"><span data-stu-id="f9e89-826">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="f9e89-827">Lägg till parametern ”-ResourceDiscoverMode” för Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="f9e89-827">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="f9e89-828">Lägg till cmdleten Get-AzPolicyMetadata för att hämta resurser för principmetadata</span><span class="sxs-lookup"><span data-stu-id="f9e89-828">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="f9e89-829">Get-AzPolicyState och Get-AzPolicyStateSummary för API-versionen 2019-10-01 har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="f9e89-829">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f9e89-830">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f9e89-830">Az.RecoveryServices</span></span>
* <span data-ttu-id="f9e89-831">Azure Site Recovery-stöd för att ta bort en replikerad disk.</span><span class="sxs-lookup"><span data-stu-id="f9e89-831">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="f9e89-832">Tillagt Azure Backup-stöd för att lägga till taggar när ett Recovery Services-valv skapas.</span><span class="sxs-lookup"><span data-stu-id="f9e89-832">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f9e89-833">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f9e89-833">Az.Resources</span></span>
* <span data-ttu-id="f9e89-834">Gör -Scope valfritt i cmdletarna \*-AzPolicyAssignment med standardinställning till kontextprenumeration</span><span class="sxs-lookup"><span data-stu-id="f9e89-834">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="f9e89-835">Lägg till exempel på att skapa ADServicePrincipal med lösenord och nyckelautentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="f9e89-835">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="f9e89-836">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f9e89-836">Az.Sql</span></span>
<span data-ttu-id="f9e89-837">Åtgärda cmdleten New-AzSqlDatabaseSecondary så att existensen PartnerDatabaseName kontrolleras i stället för existensen DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="f9e89-837">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f9e89-838">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f9e89-838">Az.Storage</span></span>
* <span data-ttu-id="f9e89-839">Stöd för angivning av krypteringsnyckeltyp för Tabell/kö i Skapa lagringskonto</span><span class="sxs-lookup"><span data-stu-id="f9e89-839">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="f9e89-840">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f9e89-840">New-AzStorageAccount</span></span>
* <span data-ttu-id="f9e89-841">Visa RequestId när StorageException inte har ExtendedErrorInformation</span><span class="sxs-lookup"><span data-stu-id="f9e89-841">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="f9e89-842">Åtgärda exempel 6 för cmdleten Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="f9e89-842">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f9e89-843">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f9e89-843">Az.Websites</span></span>
* <span data-ttu-id="f9e89-844">Set-AzWebapp och Set-AzWebappSlot stöder egenskaperna AlwaysOn, MinTls och FtpsState</span><span class="sxs-lookup"><span data-stu-id="f9e89-844">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="f9e89-845">Åtgärdar problemet där inställning av HttpsOnly samtidigt som AppservicePlan ändrades med det enskilda kommandot Set-AzWebApp återställde HttpsOnly till standardvärdet</span><span class="sxs-lookup"><span data-stu-id="f9e89-845">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="f9e89-846">3.3.0 – januari 2020</span><span class="sxs-lookup"><span data-stu-id="f9e89-846">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f9e89-847">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f9e89-847">Az.Accounts</span></span>
* <span data-ttu-id="f9e89-848">Nu stöder Add-AzEnvironment och Set-AzEnvironment parametrarna AzureAttestationServiceEndpointResourceId och AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="f9e89-848">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="f9e89-849">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f9e89-849">Az.Cdn</span></span>
* <span data-ttu-id="f9e89-850">Information om felsvar visas i New-AzCdnEndpoint-cmdleten</span><span class="sxs-lookup"><span data-stu-id="f9e89-850">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f9e89-851">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f9e89-851">Az.Compute</span></span>
* <span data-ttu-id="f9e89-852">Set-AzVMCustomScriptExtension-cmdleten har åtgärdats för en virtuell dator med hanterad OD-disk som inte har någon operativsystemprofil.</span><span class="sxs-lookup"><span data-stu-id="f9e89-852">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="f9e89-853">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="f9e89-853">Az.ContainerInstance</span></span>
* <span data-ttu-id="f9e89-854">Parameternamn som används med New-AzContainerGroup-exempel har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="f9e89-854">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="f9e89-855">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="f9e89-855">Az.DataBoxEdge</span></span>
* <span data-ttu-id="f9e89-856">Cmdleten ”Get-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="f9e89-856">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="f9e89-857">Hämta gränslagringscontainern</span><span class="sxs-lookup"><span data-stu-id="f9e89-857">Get the Edge Storage Container</span></span>
* <span data-ttu-id="f9e89-858">Cmdleten ”New-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="f9e89-858">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="f9e89-859">Skapa en ny gränslagringscontainer</span><span class="sxs-lookup"><span data-stu-id="f9e89-859">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="f9e89-860">Cmdleten ”Remove-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="f9e89-860">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="f9e89-861">Ta bort gränslagringscontainern</span><span class="sxs-lookup"><span data-stu-id="f9e89-861">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="f9e89-862">Cmdleten ”Invoke-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="f9e89-862">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="f9e89-863">Anropa åtgärd för att uppdatera data i gränslagringscontainer</span><span class="sxs-lookup"><span data-stu-id="f9e89-863">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="f9e89-864">Cmdleten ”Get-AzDataBoxEdgeStorageAccount” har lagts till</span><span class="sxs-lookup"><span data-stu-id="f9e89-864">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="f9e89-865">Hämta gränslagringskontot</span><span class="sxs-lookup"><span data-stu-id="f9e89-865">Get the Edge Storage Account</span></span>
* <span data-ttu-id="f9e89-866">Cmdleten ”New-AzDataBoxEdgeStorageAccount” har lagts till</span><span class="sxs-lookup"><span data-stu-id="f9e89-866">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="f9e89-867">Skapa ett nytt gränslagringskonto</span><span class="sxs-lookup"><span data-stu-id="f9e89-867">Create new Edge Storage Account</span></span>
* <span data-ttu-id="f9e89-868">Cmdleten ”Remove-AzDataBoxEdgeStorageAccount” har lagts till</span><span class="sxs-lookup"><span data-stu-id="f9e89-868">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="f9e89-869">Ta bort gränslagringskontot</span><span class="sxs-lookup"><span data-stu-id="f9e89-869">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="f9e89-870">Anropa cmdleten ”Invoke-AzDataBoxEdgeShare”</span><span class="sxs-lookup"><span data-stu-id="f9e89-870">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="f9e89-871">Anropa åtgärd för att uppdatera resursdata</span><span class="sxs-lookup"><span data-stu-id="f9e89-871">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="f9e89-872">Cmdleten ”Set-AzDataBoxEdgeStorageAccountCredential” har lagts till</span><span class="sxs-lookup"><span data-stu-id="f9e89-872">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="f9e89-873">Ange autentiseringsuppgifter för az databoxedge-lagringskonto</span><span class="sxs-lookup"><span data-stu-id="f9e89-873">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f9e89-874">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f9e89-874">Az.DataFactory</span></span>
* <span data-ttu-id="f9e89-875">Lägg till AutoUpdateETA-, LatestVersion-, PushedVersion-, TaskQueueId- och VersionStatus-egenskaper för Get-AzDataFactoryV2IntegrationRuntime-cmd</span><span class="sxs-lookup"><span data-stu-id="f9e89-875">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="f9e89-876">Uppdatera ADF .Net SDK-versionen till 4.6.0</span><span class="sxs-lookup"><span data-stu-id="f9e89-876">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="f9e89-877">Lägg till parametern ”PublicIPs” för ”Set-AzureRmDataFactoryV2IntegrationRuntime”-cmd så att Azure-SSIS IR kan skapas med statiska offentliga IP-adresser.</span><span class="sxs-lookup"><span data-stu-id="f9e89-877">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="f9e89-878">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="f9e89-878">Az.DevTestLabs</span></span>
* <span data-ttu-id="f9e89-879">Ta bort den brutna länken i Get-AzDtlAllowedVMSizesPolicy.md</span><span class="sxs-lookup"><span data-stu-id="f9e89-879">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f9e89-880">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f9e89-880">Az.EventHub</span></span>
* <span data-ttu-id="f9e89-881">Korrigering av problem 10634: Åtgärda referensen till null-objekt för eventhubnamespace-borttagning</span><span class="sxs-lookup"><span data-stu-id="f9e89-881">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="f9e89-882">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f9e89-882">Az.HDInsight</span></span>
* <span data-ttu-id="f9e89-883">Åtgärda Invoke-AzHDInsightHiveJob.md-fel.</span><span class="sxs-lookup"><span data-stu-id="f9e89-883">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="f9e89-884">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="f9e89-884">Az.MachineLearning</span></span>
* <span data-ttu-id="f9e89-885">Nedanstående cmdletar har tagits bort eftersom MachineLearningCompute inte längre är tillgängligt</span><span class="sxs-lookup"><span data-stu-id="f9e89-885">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="f9e89-886">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="f9e89-886">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="f9e89-887">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="f9e89-887">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="f9e89-888">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="f9e89-888">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="f9e89-889">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="f9e89-889">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="f9e89-890">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="f9e89-890">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="f9e89-891">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="f9e89-891">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="f9e89-892">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="f9e89-892">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f9e89-893">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f9e89-893">Az.Network</span></span>
* <span data-ttu-id="f9e89-894">Uppgradera beroende av Microsoft.Azure.Management.Sql från 1.36-preview till 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="f9e89-894">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f9e89-895">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f9e89-895">Az.RecoveryServices</span></span>
* <span data-ttu-id="f9e89-896">Ändrat Azure Site Recovery-stöd för krypterade vilande data på virtuella datorer med hanterade diskar med kundhanterade nycklar för Azure till Azure-providern.</span><span class="sxs-lookup"><span data-stu-id="f9e89-896">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="f9e89-897">Azure Site Recovery-stöd för att ange ID för diskkrypteringsuppsättning som valfri inmatning för aktivering av skydd för VMware till Azure.</span><span class="sxs-lookup"><span data-stu-id="f9e89-897">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="f9e89-898">Azure Site Recovery-stöd för att ange ID för diskkrypteringsuppsättning som valfri inmatning på disknivå för aktivering av skydd för VMware till Azure.</span><span class="sxs-lookup"><span data-stu-id="f9e89-898">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="f9e89-899">Azure Site Recovery-stöd för att uppdatera replikeringsskyddade objekt med mappning för diskkrypteringsuppsättning för HyperV till Azure.</span><span class="sxs-lookup"><span data-stu-id="f9e89-899">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f9e89-900">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f9e89-900">Az.Resources</span></span>
* <span data-ttu-id="f9e89-901">Åtgärda ett fel i hjälpdokument för ”Remove-AzTag”.</span><span class="sxs-lookup"><span data-stu-id="f9e89-901">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="f9e89-902">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f9e89-902">Az.Sql</span></span>
* <span data-ttu-id="f9e89-903">Åtgärda funktioner i cmdletar för att ange baslinjen för sårbarhetsbedömning för arbete med huvuddatabasen för Azure-databasen och begränsa den för systemdatabaser på hanterade instanser.</span><span class="sxs-lookup"><span data-stu-id="f9e89-903">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="f9e89-904">Åtgärda ett fel när en redundansgrupp för en SQL-instans skapas</span><span class="sxs-lookup"><span data-stu-id="f9e89-904">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="f9e89-905">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="f9e89-905">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="f9e89-906">Lägg till DR som en ny giltig licenstyp</span><span class="sxs-lookup"><span data-stu-id="f9e89-906">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f9e89-907">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f9e89-907">Az.Storage</span></span>
* <span data-ttu-id="f9e89-908">Lägg till varningsmeddelande om icke-bakåtkompatibel ändring för DefaultAction-värdeändring i en framtida version</span><span class="sxs-lookup"><span data-stu-id="f9e89-908">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="f9e89-909">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="f9e89-909">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="f9e89-910">Stöd för att hämta lagringskontots senaste synkroniseringstid genom att köra get-AzureRMStorageAccount med parametern -IncludeGeoReplicationStats</span><span class="sxs-lookup"><span data-stu-id="f9e89-910">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="f9e89-911">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f9e89-911">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="f9e89-912">3.2.0 – December 2019</span><span class="sxs-lookup"><span data-stu-id="f9e89-912">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="f9e89-913">Allmänt</span><span class="sxs-lookup"><span data-stu-id="f9e89-913">General</span></span>
* <span data-ttu-id="f9e89-914">Uppdatera referenser i .psd1 för att använda relativa sökvägar för alla moduler</span><span class="sxs-lookup"><span data-stu-id="f9e89-914">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f9e89-915">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f9e89-915">Az.Accounts</span></span>
* <span data-ttu-id="f9e89-916">Ange rätt UserAgent för telemetri på klientsidan för Az 4.0 preview</span><span class="sxs-lookup"><span data-stu-id="f9e89-916">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="f9e89-917">Visa användarvänligt felmeddelande när kontexten är null i Az 4.0 preview</span><span class="sxs-lookup"><span data-stu-id="f9e89-917">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="f9e89-918">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="f9e89-918">Az.Batch</span></span>
* <span data-ttu-id="f9e89-919">Korrigera problem [#10602](https://github.com/Azure/azure-powershell/issues/10602), där **New-AzBatchPool** skickade VirtualMachineConfiguration.ContainerConfiguration eller VirtualMachineConfiguration.DataDisks på ett felaktigt sätt till servern.</span><span class="sxs-lookup"><span data-stu-id="f9e89-919">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f9e89-920">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f9e89-920">Az.DataFactory</span></span>
* <span data-ttu-id="f9e89-921">Uppdatera ADF .Net SDK-versionen till 4.5.0</span><span class="sxs-lookup"><span data-stu-id="f9e89-921">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="f9e89-922">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f9e89-922">Az.FrontDoor</span></span>
* <span data-ttu-id="f9e89-923">Stöd har lagts till för undantag för hanterade regler för brandväggen för webbaserade program</span><span class="sxs-lookup"><span data-stu-id="f9e89-923">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="f9e89-924">Lägg till SocketAddr för automatisk komplettering</span><span class="sxs-lookup"><span data-stu-id="f9e89-924">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="f9e89-925">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="f9e89-925">Az.HealthcareApis</span></span>
* <span data-ttu-id="f9e89-926">Undantagshantering</span><span class="sxs-lookup"><span data-stu-id="f9e89-926">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f9e89-927">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f9e89-927">Az.KeyVault</span></span>
* <span data-ttu-id="f9e89-928">Åtgärdat fel vid åtkomst av värde som kanske inte har angetts</span><span class="sxs-lookup"><span data-stu-id="f9e89-928">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="f9e89-929">Hantering av ECC-certifikat (Elliptic Curve Cryptography)</span><span class="sxs-lookup"><span data-stu-id="f9e89-929">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="f9e89-930">Stöd har lagts till för att ange kurvan för certifikatprinciper</span><span class="sxs-lookup"><span data-stu-id="f9e89-930">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f9e89-931">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f9e89-931">Az.Monitor</span></span>
* <span data-ttu-id="f9e89-932">Lägger till valfritt argument i kommandot Lägg till diagnostikinställningar.</span><span class="sxs-lookup"><span data-stu-id="f9e89-932">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="f9e89-933">Ett växelargument som om det finns visar att exporten till Log Analytics måste ske till ett fast schema (kallas även</span><span class="sxs-lookup"><span data-stu-id="f9e89-933">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="f9e89-934">dedikerad, datatyp)</span><span class="sxs-lookup"><span data-stu-id="f9e89-934">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f9e89-935">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f9e89-935">Az.Network</span></span>
* <span data-ttu-id="f9e89-936">Stöd för IpGroups i program-, NAT- och nätverksregler för Azure Firewall.</span><span class="sxs-lookup"><span data-stu-id="f9e89-936">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f9e89-937">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f9e89-937">Az.Resources</span></span>
* <span data-ttu-id="f9e89-938">Åtgärda ett problem där malldistributionen inte kan läsa en mallparameter om dess namn står i konflikt med ett inbyggt parameternamn.</span><span class="sxs-lookup"><span data-stu-id="f9e89-938">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="f9e89-939">Uppdaterade princip-cmdletar för att använda den nya API-versionen 2019-09-01 som introducerar grupperingsstöd inom principuppsättningsdefinitioner.</span><span class="sxs-lookup"><span data-stu-id="f9e89-939">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="f9e89-940">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f9e89-940">Az.Sql</span></span>
* <span data-ttu-id="f9e89-941">Uppgraderad funktion för att skapa lagring i automatisk aktivering av sårbarhetsbedömning till StorageV2</span><span class="sxs-lookup"><span data-stu-id="f9e89-941">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f9e89-942">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f9e89-942">Az.Storage</span></span>
* <span data-ttu-id="f9e89-943">Stöd för generering av blob/container-identitetsbaserad SAS-token med lagringskontextbaserad på OAuth-autentisering</span><span class="sxs-lookup"><span data-stu-id="f9e89-943">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="f9e89-944">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="f9e89-944">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="f9e89-945">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="f9e89-945">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="f9e89-946">Stöd för återkallning av användardelegeringsnycklar för lagringskonto för att återkalla alla SAS-token</span><span class="sxs-lookup"><span data-stu-id="f9e89-946">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="f9e89-947">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="f9e89-947">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="f9e89-948">Uppgradera till Microsoft.Azure.Management.Storage 14.2.0 för att stödja den nya API-versionen 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="f9e89-948">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="f9e89-949">Stöd för QuotaGiB (resurskvot i Gibibye) för värden över 5120 i hanteringsplanet för cmdletar för filresurser och parameteraliaset. Quota har också lagts till för parametern ”QuotaGiB”.</span><span class="sxs-lookup"><span data-stu-id="f9e89-949">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="f9e89-950">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="f9e89-950">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="f9e89-951">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="f9e89-951">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="f9e89-952">Lägg till parameteraliaset QuotaGiB i parametern Quota</span><span class="sxs-lookup"><span data-stu-id="f9e89-952">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="f9e89-953">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="f9e89-953">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="f9e89-954">Åtgärda problemet att Set-AzStorageContainerAcl kan rensa den lagrade åtkomstprincipen</span><span class="sxs-lookup"><span data-stu-id="f9e89-954">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="f9e89-955">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="f9e89-955">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="f9e89-956">3.1.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="f9e89-956">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="f9e89-957">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="f9e89-957">Highlights since the last major release</span></span>
* <span data-ttu-id="f9e89-958">Az.DataBoxEdge 1.0.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="f9e89-958">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="f9e89-959">Az.SqlVirtualMachine 1.0.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="f9e89-959">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f9e89-960">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f9e89-960">Az.Compute</span></span>
* <span data-ttu-id="f9e89-961">Funktion för att använda en virtuell dator igen</span><span class="sxs-lookup"><span data-stu-id="f9e89-961">VM Reapply feature</span></span>
    - <span data-ttu-id="f9e89-962">Lägg till parameter för att använda igen till cmdleten Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="f9e89-962">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="f9e89-963">Funktionen AutomaticRepairs i VM-skalningsuppsättningar:</span><span class="sxs-lookup"><span data-stu-id="f9e89-963">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="f9e89-964">Lägg till parametrarna EnableAutomaticRepair, AutomaticRepairGracePeriod och AutomaticRepairMaxInstanceRepairsPercent till följande cmdletar:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f9e89-964">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="f9e89-965">Stöd för galleriavbildningar i flera klientorganisationer för New-AzVM</span><span class="sxs-lookup"><span data-stu-id="f9e89-965">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="f9e89-966">Lägg till "Spot" till argumentslutföraren i prioritetsparametern i cmdletarna New-AzVM, New-AzVMConfig och New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f9e89-966">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="f9e89-967">Lägg till parametrarna DiskIOPSReadWrite och DiskMBpsReadWrite till cmdleten Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="f9e89-967">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="f9e89-968">Ändra parametern SourceImageId för cmdleten New-AzGalleryImageVersion till valfri</span><span class="sxs-lookup"><span data-stu-id="f9e89-968">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="f9e89-969">Lägg till parametrarna OSDiskImage och DataDiskImage till cmdleten New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="f9e89-969">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="f9e89-970">Lägg till parametern HyperVGeneration till cmdleten New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="f9e89-970">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="f9e89-971">Lägg till parametern SkipExtensionsOnOverprovisionedVMs till cmdletarna New-AzVmss, New-AzVmssConfig och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f9e89-971">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="f9e89-972">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="f9e89-972">Az.DataBoxEdge</span></span>
* <span data-ttu-id="f9e89-973">Cmdleten `Get-AzDataBoxEdgeOrder` har lagts till</span><span class="sxs-lookup"><span data-stu-id="f9e89-973">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="f9e89-974">Hämta ordning</span><span class="sxs-lookup"><span data-stu-id="f9e89-974">Get the Order</span></span>
* <span data-ttu-id="f9e89-975">Cmdleten `New-AzDataBoxEdgeOrder` har lagts till</span><span class="sxs-lookup"><span data-stu-id="f9e89-975">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="f9e89-976">Skapa ny ordning</span><span class="sxs-lookup"><span data-stu-id="f9e89-976">Create new Order</span></span>
* <span data-ttu-id="f9e89-977">Cmdleten `Remove-AzDataBoxEdgeOrder` har lagts till</span><span class="sxs-lookup"><span data-stu-id="f9e89-977">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="f9e89-978">Ta bort ordning</span><span class="sxs-lookup"><span data-stu-id="f9e89-978">Remove the Order</span></span>
* <span data-ttu-id="f9e89-979">Cmdleten `New-AzDataBoxEdgeShare` har ändrats</span><span class="sxs-lookup"><span data-stu-id="f9e89-979">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="f9e89-980">Nu skapas lokal filresurs</span><span class="sxs-lookup"><span data-stu-id="f9e89-980">Now creates Local Share</span></span>
* <span data-ttu-id="f9e89-981">Cmdleten `Set-AzDataBoxEdgeRole` har lagts till</span><span class="sxs-lookup"><span data-stu-id="f9e89-981">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="f9e89-982">Nu kan IotRole mappas till filresursen</span><span class="sxs-lookup"><span data-stu-id="f9e89-982">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="f9e89-983">Cmdleten `Invoke-AzDataBoxEdgeDevice` har lagts till</span><span class="sxs-lookup"><span data-stu-id="f9e89-983">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="f9e89-984">Anropa genomsökningsuppdatering, ladda ned uppdatering, installera uppdateringar på enheten</span><span class="sxs-lookup"><span data-stu-id="f9e89-984">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="f9e89-985">Cmdleten `Get-AzDataBoxEdgeTrigger` har lagts till</span><span class="sxs-lookup"><span data-stu-id="f9e89-985">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="f9e89-986">Hämtar information om utlösare</span><span class="sxs-lookup"><span data-stu-id="f9e89-986">Gets the information about Triggers</span></span>
* <span data-ttu-id="f9e89-987">Cmdleten `New-AzDataBoxEdgeTrigger` har lagts till</span><span class="sxs-lookup"><span data-stu-id="f9e89-987">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="f9e89-988">Skapa nya utlösare</span><span class="sxs-lookup"><span data-stu-id="f9e89-988">Create new Triggers</span></span>
* <span data-ttu-id="f9e89-989">Cmdleten `Remove-AzDataBoxEdgeTrigger` har lagts till</span><span class="sxs-lookup"><span data-stu-id="f9e89-989">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="f9e89-990">Ta bort utlösare</span><span class="sxs-lookup"><span data-stu-id="f9e89-990">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f9e89-991">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f9e89-991">Az.DataFactory</span></span>
* <span data-ttu-id="f9e89-992">Uppdatera ADF .Net SDK-versionen till 4.4.0</span><span class="sxs-lookup"><span data-stu-id="f9e89-992">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="f9e89-993">Lägg till parametern ExpressCustomSetup för kommandot Set-AzureRmDataFactoryV2IntegrationRuntime för att aktivera installationskonfigurationer och komponenter från tredje part utan anpassat konfigurationsskript.</span><span class="sxs-lookup"><span data-stu-id="f9e89-993">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f9e89-994">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f9e89-994">Az.DataLakeStore</span></span>
* <span data-ttu-id="f9e89-995">Uppdatera dokumentation för Get-AzDataLakeStoreDeletedItem och Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="f9e89-995">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f9e89-996">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f9e89-996">Az.EventHub</span></span>
* <span data-ttu-id="f9e89-997">Korrigering av problem #10301: Korrigera datumformat för SAS-token</span><span class="sxs-lookup"><span data-stu-id="f9e89-997">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="f9e89-998">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f9e89-998">Az.FrontDoor</span></span>
* <span data-ttu-id="f9e89-999">Lägg till parametern MinimumTlsVersion till Enable-AzFrontDoorCustomDomainHttps och New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="f9e89-999">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="f9e89-1000">Lägg till parametrarna HealthProbeMethod och EnabledState till New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="f9e89-1000">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="f9e89-1001">Lägg till en ny cmdlet för att skapa BackendPoolsSettings-objekt som passar i skapande/uppdatering av Front Door</span><span class="sxs-lookup"><span data-stu-id="f9e89-1001">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="f9e89-1002">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="f9e89-1002">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f9e89-1003">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f9e89-1003">Az.Network</span></span>
* <span data-ttu-id="f9e89-1004">Ändra alternativexemplen Start-AzVirtualNetworkGatewayConnectionPacketCapture.md och Start-AzVirtualnetworkGatewayPacketCapture.md för FilterData.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1004">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="f9e89-1005">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="f9e89-1005">Az.PrivateDns</span></span>
* <span data-ttu-id="f9e89-1006">Uppdaterade PrivateDns .NET SDK till version 1.0.0</span><span class="sxs-lookup"><span data-stu-id="f9e89-1006">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f9e89-1007">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f9e89-1007">Az.RecoveryServices</span></span>
* <span data-ttu-id="f9e89-1008">Stöd för att välja disktyp vid aktivering av skydd i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1008">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="f9e89-1009">Korrigering av bugg för åtgärdsredigering av återställningsplan i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1009">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="f9e89-1010">Återställningsstöd för att godkänna filestream-databaser i Azure Backup SQL.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1010">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="f9e89-1011">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="f9e89-1011">Az.RedisCache</span></span>
* <span data-ttu-id="f9e89-1012">Parametern MinimumTlsVersion har lagts till i cmdletarna New-AzRedisCache och Set-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1012">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="f9e89-1013">Dessutom har MinimumTlsVersion lagts till i utdata för cmdleten Get-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1013">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="f9e89-1014">Verifiering har lagts till på parametern -Size i cmdletarna Set-AzRedisCache och New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="f9e89-1014">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="f9e89-1015">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f9e89-1015">Az.Resources</span></span>
- <span data-ttu-id="f9e89-1016">Uppdaterade policy-cmdletar för att använda den nya API-versionen 2019-06-01 som har en ny EnforcementMode-egenskap i policytilldelningen.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1016">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="f9e89-1017">Uppdaterade hjälpexempel för skapandet av policydefinition</span><span class="sxs-lookup"><span data-stu-id="f9e89-1017">Updated create policy definition help example</span></span>
- <span data-ttu-id="f9e89-1018">Åtgärda bugg i Remove-AZADServicePrincipal -ServicePrincipalName, utlös null-referens när tjänstens huvudnamn inte hittas.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1018">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="f9e89-1019">Åtgärda bugg i New-AZADServicePrincipal, utlös null-referens när klientorganisationen inte har någon prenumeration.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1019">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="f9e89-1020">Ändra New-AzAdServicePrincipal för att endast lägga till autentiseringsuppgifter för det associerade programmet.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1020">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="f9e89-1021">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f9e89-1021">Az.Sql</span></span>
* <span data-ttu-id="f9e89-1022">Stöd har lagts till för databasen ReadReplicaCount.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1022">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="f9e89-1023">Korrigerade Set-AzSqlDatabase när zonredundans inte har angetts</span><span class="sxs-lookup"><span data-stu-id="f9e89-1023">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="f9e89-1024">3.0.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="f9e89-1024">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="f9e89-1025">Allmänt</span><span class="sxs-lookup"><span data-stu-id="f9e89-1025">General</span></span>
* <span data-ttu-id="f9e89-1026">Az. PrivateDns 1.0.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="f9e89-1026">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f9e89-1027">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f9e89-1027">Az.Accounts</span></span>
* <span data-ttu-id="f9e89-1028">Lägg till ett utfasningsmeddelande för aliaset Resolve-error.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1028">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="f9e89-1029">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="f9e89-1029">Az.Advisor</span></span>
* <span data-ttu-id="f9e89-1030">Den nya kategorin Operational Excellence har lagts till i cmdleten Get-AzAdvisorRecommendation.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1030">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="f9e89-1031">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="f9e89-1031">Az.Batch</span></span>
* <span data-ttu-id="f9e89-1032">`CoreQuota` på `BatchAccountContext` har bytt namn till `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1032">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="f9e89-1033">Det finns även en ny `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1033">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="f9e89-1034">Detta påverkar **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1034">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="f9e89-1035">**New-AzBatchTask** `-ResourceFile`-parametern tar nu en samling `PSResourceFile`-objekt som kan skapas med hjälp av den nya cmdleten **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1035">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="f9e89-1036">Ny **New-AzBatchResourceFile**-cmdlet för att skapa `PSResourceFile`-objekt.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1036">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="f9e89-1037">Dessa kan tillhandahållas till **New-AzBatchTask** på `-ResourceFile`-parametern.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1037">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="f9e89-1038">Detta stöder två nya typer av resursfiler förutom det befintliga sättet med `HttpUrl`:</span><span class="sxs-lookup"><span data-stu-id="f9e89-1038">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="f9e89-1039">`AutoStorageContainerName`-baserade resursfiler laddar ned en hel container för automatisk lagring till Batch-noden.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1039">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="f9e89-1040">`StorageContainerUrl`-baserade resursfiler laddar ned containern som anges i webbadressen till Batch-noden.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1040">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="f9e89-1041">Tog bort egenskapen `ApplicationPackages` för `PSApplication` som returnerades av **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1041">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="f9e89-1042">Specifika paket i ett program kan nu hämtas med hjälp av **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1042">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="f9e89-1043">Till exempel: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1043">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="f9e89-1044">Bytt namn på `ApplicationId` till `ApplicationName` på **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** och **Set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1044">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="f9e89-1045">`ApplicationId` är nu ett alias för `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1045">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="f9e89-1046">Ny `PSWindowsUserConfiguration`-egenskap till `PSUserAccount` lades till.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1046">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="f9e89-1047">Bytte namn på `Version` till `Name` på `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1047">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="f9e89-1048">Bytte namn på `BlobSource` till `HttpUrl` på `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1048">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="f9e89-1049">Tog bort egenskapen `OSDisk` från `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1049">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="f9e89-1050">Tog bort **Set-AzBatchPoolOSVersion**.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1050">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="f9e89-1051">Den här åtgärden stöds inte längre.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1051">This operation is no longer supported.</span></span>
* <span data-ttu-id="f9e89-1052">`TargetOSVersion` har tagits bort från `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1052">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="f9e89-1053">Bytte namn på `CurrentOSVersion` till `OSVersion` på `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1053">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="f9e89-1054">`DataEgressGiB` och `DataIngressGiB` har tagits bort från `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1054">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="f9e89-1055">Tog bort **Get-AzBatchNodeAgentSku** och ersatte det med **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1055">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="f9e89-1056">**Get-AzBatchSupportedImage** returnerar samma data som **Get-AzBatchNodeAgentSku** men i ett mer användarvänligt format.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1056">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="f9e89-1057">Nya icke-verifierade avbildningar returneras nu också.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1057">New non-verified images are also now returned.</span></span> <span data-ttu-id="f9e89-1058">Ytterligare information om `Capabilities` och `BatchSupportEndOfLife` för varje avbildning inkluderas också.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1058">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="f9e89-1059">Lade till möjlighet att montera fjärrfilsystem på varje nod i en pool via den nya parametern `MountConfiguration` för **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1059">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="f9e89-1060">Har nu stöd för nätverkssäkerhetsregler som blockerar nätverksåtkomst till en pool baserat på källportens trafik.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1060">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="f9e89-1061">Detta görs via egenskapen `SourcePortRanges` på `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1061">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="f9e89-1062">När du kör en container stöder nu Batch körningen av uppgiften i arbetskatalogen för containern eller i arbetskatalogen för Batch-uppgiften.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1062">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="f9e89-1063">Detta styrs av egenskapen `WorkingDirectory` på `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1063">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="f9e89-1064">Lade till en funktion för att ange en samling av offentliga IP-adresser på `PSNetworkConfiguration` via den nya egenskapen `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1064">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="f9e89-1065">Detta garanterar att noderna i poolen har en IP-adress från listan över IP-adresser som tillhandahållits av användare.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1065">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="f9e89-1066">Om inget värde anges är standardvärdet för `WaitForSuccess` på `PSSTartTask` nu `$True` (var tidigare `$False`).</span><span class="sxs-lookup"><span data-stu-id="f9e89-1066">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="f9e89-1067">Om inget värde anges är standardvärdet för `Scope` på `PSAutoUserSpecification` nu `Pool` (var tidigare `Task` på Windows och `Pool` på Linux).</span><span class="sxs-lookup"><span data-stu-id="f9e89-1067">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="f9e89-1068">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f9e89-1068">Az.Cdn</span></span>
* <span data-ttu-id="f9e89-1069">Introducerade UrlRewriteAction och CacheKeyQueryStringAction till RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1069">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="f9e89-1070">Åtgärdade flera buggar, som saknade indata för ”väljare” i cmdleten New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1070">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f9e89-1071">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f9e89-1071">Az.Compute</span></span>
* <span data-ttu-id="f9e89-1072">Funktion för diskkrypteringsuppsättning</span><span class="sxs-lookup"><span data-stu-id="f9e89-1072">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="f9e89-1073">Nya cmdletar:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="f9e89-1073">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="f9e89-1074">Parametern DiskEncryptionSetId har lagts till i följande cmdletar:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="f9e89-1074">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="f9e89-1075">Parametrarna DiskEncryptionSetId och EncryptionType har lagts till i följande cmdletar:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="f9e89-1075">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="f9e89-1076">Lägg till parametern PublicIPAddressVersion i New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="f9e89-1076">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="f9e89-1077">Flytta FileUris för anpassat skripttillägg från offentlig inställning till skyddad inställning</span><span class="sxs-lookup"><span data-stu-id="f9e89-1077">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="f9e89-1078">Lägg till ScaleInPolicy i cmdletarna New-AzVmss, New-AzVmssConfig och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f9e89-1078">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="f9e89-1079">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="f9e89-1079">Breaking changes</span></span>
    - <span data-ttu-id="f9e89-1080">Parametern UploadSizeInBytes används istället för DiskSizeGB för New-AzDiskConfig när CreateOption är Uppladdning</span><span class="sxs-lookup"><span data-stu-id="f9e89-1080">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="f9e89-1081">PublishingProfile.Source.ManagedImage.Id ersätts med StorageProfile.Source.Id i objektet GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="f9e89-1081">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f9e89-1082">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f9e89-1082">Az.DataFactory</span></span>
* <span data-ttu-id="f9e89-1083">Uppdatera ADF .Net SDK-versionen till 4.3.0</span><span class="sxs-lookup"><span data-stu-id="f9e89-1083">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f9e89-1084">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f9e89-1084">Az.DataLakeStore</span></span>
* <span data-ttu-id="f9e89-1085">Uppdatera ADLS SDK-version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) innehåller följande korrigeringar</span><span class="sxs-lookup"><span data-stu-id="f9e89-1085">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="f9e89-1086">Undvik att utlösa undantag när det inte går att deserialisera creationtime för inmatning av papperskorg eller katalog.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1086">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="f9e89-1087">Gör inställning tillgänglig per tidsgräns för förfrågan i adlsclient</span><span class="sxs-lookup"><span data-stu-id="f9e89-1087">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="f9e89-1088">Korrigera överföringen av ursprunglig syncflag för badoffset-återställning</span><span class="sxs-lookup"><span data-stu-id="f9e89-1088">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="f9e89-1089">Korrigera EnumerateDirectory för att hämta fortsättningstoken när svar har kontrollerats</span><span class="sxs-lookup"><span data-stu-id="f9e89-1089">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="f9e89-1090">Korrigera bugg i Concat</span><span class="sxs-lookup"><span data-stu-id="f9e89-1090">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="f9e89-1091">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f9e89-1091">Az.FrontDoor</span></span>
* <span data-ttu-id="f9e89-1092">Åtgärdade diverse stavfel i modul</span><span class="sxs-lookup"><span data-stu-id="f9e89-1092">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="f9e89-1093">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f9e89-1093">Az.HDInsight</span></span>
* <span data-ttu-id="f9e89-1094">Korrigerade buggen att kunder får felet ”inte en giltig Base-64-sträng” vid användning av Get-AzHDInsightCluster för att hämta klustret med ADLSGen1-lagring.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1094">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="f9e89-1095">Lägg till en parameter med namnet ”ApplicationId” i de tre cmdletarna Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig och New-AzHDInsightCluster så att kunden kan tillhandahålla tjänstens huvudnamn för program-ID för åtkomst till Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1095">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="f9e89-1096">Ändrade Microsoft.Azure.Management.HDInsight från 2.1.0 till 5.1.0</span><span class="sxs-lookup"><span data-stu-id="f9e89-1096">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="f9e89-1097">Fem cmdletar har tagits bort:</span><span class="sxs-lookup"><span data-stu-id="f9e89-1097">Removed five cmdlets:</span></span>
    - <span data-ttu-id="f9e89-1098">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="f9e89-1098">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="f9e89-1099">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="f9e89-1099">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="f9e89-1100">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="f9e89-1100">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="f9e89-1101">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="f9e89-1101">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="f9e89-1102">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="f9e89-1102">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="f9e89-1103">Tre cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="f9e89-1103">Added three cmdlets:</span></span>
    - <span data-ttu-id="f9e89-1104">Get-AzHDInsightMonitoring som ersätter Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1104">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="f9e89-1105">Enable-AzHDInsightMonitoring som ersätter Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1105">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="f9e89-1106">Disable-AzHDInsightMonitoring som ersätter Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1106">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="f9e89-1107">Korrigerade cmdleten Get-AzHDInsightProperties för att stödja hämtning av funktionsinformation från en viss plats.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1107">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="f9e89-1108">Parameteruppsättningarna (Spark1 och Spark2) har tagits bort från Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1108">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="f9e89-1109">Lägg till exempel för cmdleten Add-AzHDInsightSecurityProfile till hjälpdokumenten.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1109">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="f9e89-1110">Ändrade utdatatyp för följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="f9e89-1110">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="f9e89-1111">Ändrade utdatatyp för Get-AzHDInsightProperties från CapabilitiesResponse till AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1111">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="f9e89-1112">Ändrade utdatatyp för Remove-AzHDInsightCluster från ClusterGetResponse till bool.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1112">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="f9e89-1113">Ändrade utdatatyp för Set-AzHDInsightGatewaySettings HttpConnectivitySettings till GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1113">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="f9e89-1114">Lade till testfall för vissa scenarier.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1114">Added some scenario test cases.</span></span>
* <span data-ttu-id="f9e89-1115">Ta bort vissa alias: Add-AzHDInsightConfigValues, Get-AzHDInsightProperties.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1115">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f9e89-1116">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f9e89-1116">Az.IotHub</span></span>
* <span data-ttu-id="f9e89-1117">Icke-bakåtkompatibla ändringar:</span><span class="sxs-lookup"><span data-stu-id="f9e89-1117">Breaking changes:</span></span>
    - <span data-ttu-id="f9e89-1118">Cmdleten Add-AzIotHubEventHubConsumerGroup har inte längre stöd för parametern EventHubEndpointName och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1118">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="f9e89-1119">Parameteruppsättningen __AllParameterSets för cmdleten Add-AzIotHubEventHubConsumerGroup har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1119">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="f9e89-1120">Cmdleten Get-AzIotHubEventHubConsumerGroup har inte längre stöd för parametern EventHubEndpointName och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1120">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="f9e89-1121">Parameteruppsättningen __AllParameterSets för cmdleten Get-AzIotHubEventHubConsumerGroup har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1121">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="f9e89-1122">Egenskapen OperationsMonitoringProperties av typen Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1122">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="f9e89-1123">Egenskapen OperationsMonitoringProperties av typen Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1123">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="f9e89-1124">Cmdleten New-AzIotHubExportDevice stöder inte längre aliaset New-AzIotHubExportDevices.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1124">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="f9e89-1125">Cmdleten New-AzIotHubImportDevice stöder inte längre aliaset New-AzIotHubImportDevices.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1125">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="f9e89-1126">Cmdleten Remove-AzIotHubEventHubConsumerGroup har inte längre stöd för parametern EventHubEndpointName och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1126">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="f9e89-1127">Parameteruppsättningen __AllParameterSets för cmdleten Remove-AzIotHubEventHubConsumerGroup har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1127">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="f9e89-1128">Cmdleten Set-AzIotHub har inte längre stöd för parametern OperationsMonitoringProperties och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1128">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="f9e89-1129">Parameteruppsättningen UpdateOperationsMonitoringProperties för cmdleten Set-AzIotHub har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1129">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f9e89-1130">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f9e89-1130">Az.RecoveryServices</span></span>
* <span data-ttu-id="f9e89-1131">Azure Site Recovery-stöd för att konfigurera nätverksresurser som NSG, offentliga IP-adresser och interna lastbalanserare för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1131">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="f9e89-1132">Azure Site Recovery-stöd för att skriva till hanterad disk för vMWare till Azure.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1132">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="f9e89-1133">Azure Site Recovery-stöd för NIC-reduktion för vMWare till Azure.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1133">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="f9e89-1134">Azure Site Recovery-stöd för accelererat nätverk för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1134">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="f9e89-1135">Azure Site Recovery-stöd för automatisk uppdatering av agent för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1135">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="f9e89-1136">Azure Site Recovery-stöd för Standard SSD för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1136">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="f9e89-1137">Azure Site Recovery-stöd för tvåstegskryptering i Azure Disk Encryption för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1137">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="f9e89-1138">Azure Site Recovery-stöd för att skydda nyligen tillagda diskar för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1138">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="f9e89-1139">En funktion för mjuk borttagning av virtuella datorer samt tester för mjuk borttagning har tagits bort</span><span class="sxs-lookup"><span data-stu-id="f9e89-1139">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="f9e89-1140">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f9e89-1140">Az.Resources</span></span>
* <span data-ttu-id="f9e89-1141">Uppdatera beroendesammansättning för Microsoft.Extensions.Caching.Memory från 1.1.1 till 2.2</span><span class="sxs-lookup"><span data-stu-id="f9e89-1141">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f9e89-1142">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f9e89-1142">Az.Network</span></span>
* <span data-ttu-id="f9e89-1143">Ändra alla cmdletar för PrivateEndpointConnection så att de stöder generiska tjänstleverantörer.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1143">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="f9e89-1144">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="f9e89-1144">Updated cmdlet:</span></span>
        - <span data-ttu-id="f9e89-1145">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f9e89-1145">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="f9e89-1146">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f9e89-1146">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="f9e89-1147">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f9e89-1147">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="f9e89-1148">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f9e89-1148">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="f9e89-1149">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f9e89-1149">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="f9e89-1150">Lägg till ny cmdlet för PrivateLinkResource så att det också stöder generiska tjänstleverantörer.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1150">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="f9e89-1151">Ny cmdlet:</span><span class="sxs-lookup"><span data-stu-id="f9e89-1151">New cmdlet:</span></span>
        - <span data-ttu-id="f9e89-1152">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="f9e89-1152">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="f9e89-1153">Lägg till nya fält och parametrar för funktionen Proxy Protocol V2.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1153">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="f9e89-1154">Lägg till egenskapen EnableProxyProtocol i PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f9e89-1154">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="f9e89-1155">Lägg till egenskapen LinkIdentifier i PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f9e89-1155">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="f9e89-1156">Uppdaterade New-AzPrivateLinkService för att lägga till den nya valfria parametern EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1156">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="f9e89-1157">Korrigera felaktig beskrivning av parameter i referensdokumentationen för New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="f9e89-1157">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="f9e89-1158">Nya cmdletar som stöder Azure-brandväggsprincipen</span><span class="sxs-lookup"><span data-stu-id="f9e89-1158">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="f9e89-1159">Lägg till stöd för den underordnade resursen RouteTables för VirtualHub</span><span class="sxs-lookup"><span data-stu-id="f9e89-1159">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="f9e89-1160">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="f9e89-1160">New cmdlets added:</span></span>
        - <span data-ttu-id="f9e89-1161">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="f9e89-1161">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="f9e89-1162">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="f9e89-1162">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="f9e89-1163">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="f9e89-1163">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="f9e89-1164">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="f9e89-1164">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="f9e89-1165">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="f9e89-1165">Set-AzVirtualHub</span></span>
* <span data-ttu-id="f9e89-1166">Lägg till stöd för ny egenskaps-SKU för VirtualHub och VirtualWANType för VirtualWan</span><span class="sxs-lookup"><span data-stu-id="f9e89-1166">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="f9e89-1167">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="f9e89-1167">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="f9e89-1168">New-AzVirtualHub: lade till parameter-SKU</span><span class="sxs-lookup"><span data-stu-id="f9e89-1168">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="f9e89-1169">Update-AzVirtualHub: lade till parameter-SKU</span><span class="sxs-lookup"><span data-stu-id="f9e89-1169">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="f9e89-1170">New-AzVirtualWan: lade till parametern VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="f9e89-1170">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="f9e89-1171">Update-AzVirtualWan: lade till parametern VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="f9e89-1171">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="f9e89-1172">Lägg till stöd för egenskapen EnableInternetSecurity för HubVnetConnection, VpnConnection och ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="f9e89-1172">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="f9e89-1173">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="f9e89-1173">New cmdlets added:</span></span>
        - <span data-ttu-id="f9e89-1174">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="f9e89-1174">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="f9e89-1175">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="f9e89-1175">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="f9e89-1176">New-AzureRmVirtualHubVnetConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="f9e89-1176">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="f9e89-1177">New-AzureRmVpnConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="f9e89-1177">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="f9e89-1178">Update-AzureRmVpnConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="f9e89-1178">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="f9e89-1179">New-AzureRmExpressRouteConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="f9e89-1179">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="f9e89-1180">Set-AzureRmExpressRouteConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="f9e89-1180">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="f9e89-1181">Lägg till stöd för att konfigurera TopLevel WebApplicationFirewall-princip</span><span class="sxs-lookup"><span data-stu-id="f9e89-1181">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="f9e89-1182">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="f9e89-1182">New cmdlets added:</span></span>
        - <span data-ttu-id="f9e89-1183">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="f9e89-1183">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="f9e89-1184">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="f9e89-1184">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="f9e89-1185">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="f9e89-1185">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="f9e89-1186">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="f9e89-1186">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="f9e89-1187">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="f9e89-1187">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="f9e89-1188">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="f9e89-1188">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="f9e89-1189">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="f9e89-1189">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="f9e89-1190">New-AzApplicationGatewayFirewallPolicy: parametrarna PolicySetting, ManagedRule har lagts till</span><span class="sxs-lookup"><span data-stu-id="f9e89-1190">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="f9e89-1191">Stöd för operator för geomatchning har lagts till på CustomRule</span><span class="sxs-lookup"><span data-stu-id="f9e89-1191">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="f9e89-1192">Geomatchning har lagts till i operatorn på FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="f9e89-1192">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="f9e89-1193">Stöd har lagts till för brandväggsprinciperna perListener och perSite</span><span class="sxs-lookup"><span data-stu-id="f9e89-1193">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="f9e89-1194">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="f9e89-1194">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="f9e89-1195">New-AzApplicationGatewayHttpListener: parametrarna FirewallPolicy, FirewallPolicyId har lagts till</span><span class="sxs-lookup"><span data-stu-id="f9e89-1195">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="f9e89-1196">New-AzApplicationGatewayPathRuleConfig: parametrarna FirewallPolicy, FirewallPolicyId har lagts till</span><span class="sxs-lookup"><span data-stu-id="f9e89-1196">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="f9e89-1197">Åtgärdat så att nödvändigt undernät med namnet AzureBastionSubnet i PSBastion kan vara skiftlägesokänsligt</span><span class="sxs-lookup"><span data-stu-id="f9e89-1197">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="f9e89-1198">Stöd för mål-FQDN:er i nätverksregler och översatt FQDN i NAT-regler för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="f9e89-1198">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="f9e89-1199">Lägg till stöd för resursen RouteTables för IpGroup på den högsta nivån</span><span class="sxs-lookup"><span data-stu-id="f9e89-1199">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="f9e89-1200">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="f9e89-1200">New cmdlets added:</span></span>
        - <span data-ttu-id="f9e89-1201">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="f9e89-1201">New-AzIpGroup</span></span>
        - <span data-ttu-id="f9e89-1202">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="f9e89-1202">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="f9e89-1203">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="f9e89-1203">Get-AzIpGroup</span></span>
        - <span data-ttu-id="f9e89-1204">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="f9e89-1204">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f9e89-1205">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f9e89-1205">Az.ServiceFabric</span></span>
* <span data-ttu-id="f9e89-1206">Ta bort cmdleten Add-AzServiceFabricApplicationCertificate eftersom det här scenariot omfattas av Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1206">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="f9e89-1207">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f9e89-1207">Az.Sql</span></span>
* <span data-ttu-id="f9e89-1208">Stöd har lagts till för återställning av utelämnade databaser på hanterade instanser.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1208">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="f9e89-1209">Inaktuella gamla cmdletar för granskning från kod.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1209">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="f9e89-1210">Tog bort inaktuella alias:</span><span class="sxs-lookup"><span data-stu-id="f9e89-1210">Removed deprecated aliases:</span></span>
* <span data-ttu-id="f9e89-1211">Get-AzSqlDatabaseIndexRecommendations (använd Get-AzSqlDatabaseIndexRecommendation istället)</span><span class="sxs-lookup"><span data-stu-id="f9e89-1211">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="f9e89-1212">Get-AzSqlDatabaseRestorePoints (använd Get-AzSqlDatabaseRestorePoint istället)</span><span class="sxs-lookup"><span data-stu-id="f9e89-1212">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="f9e89-1213">Ta bort cmdleten Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="f9e89-1213">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="f9e89-1214">Ta bort alias för inaktuella cmdletar för inställningar för utvärdering av säkerhetsrisk</span><span class="sxs-lookup"><span data-stu-id="f9e89-1214">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="f9e89-1215">Inaktualisera cmdletar för inställningar för avancerad hotidentifiering</span><span class="sxs-lookup"><span data-stu-id="f9e89-1215">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="f9e89-1216">Lägga till cmdletar för att inaktivera och aktivera känslighetsrekommendationer på kolumner i en databas.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1216">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f9e89-1217">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f9e89-1217">Az.Storage</span></span>
* <span data-ttu-id="f9e89-1218">Stöd för att aktivera stora filresurser vid skapande eller uppdatering av lagringskonto</span><span class="sxs-lookup"><span data-stu-id="f9e89-1218">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="f9e89-1219">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f9e89-1219">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="f9e89-1220">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f9e89-1220">Set-AzStorageAccount</span></span>
* <span data-ttu-id="f9e89-1221">När du stänger/hämtar en filreferens kan du hoppa över kontrollen av huruvida indatasökvägen är en filkatalog eller en fil för att undvika problem med objekt som har status DeletePending</span><span class="sxs-lookup"><span data-stu-id="f9e89-1221">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="f9e89-1222">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="f9e89-1222">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="f9e89-1223">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="f9e89-1223">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="f9e89-1224">2.8.0 – oktober 2019</span><span class="sxs-lookup"><span data-stu-id="f9e89-1224">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="f9e89-1225">Allmänt</span><span class="sxs-lookup"><span data-stu-id="f9e89-1225">General</span></span>
* <span data-ttu-id="f9e89-1226">AZ. HealthcareApis 1.0.0-version</span><span class="sxs-lookup"><span data-stu-id="f9e89-1226">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f9e89-1227">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f9e89-1227">Az.Accounts</span></span>
* <span data-ttu-id="f9e89-1228">Uppdatera telemetri och URL-omskrivning för genererade moduler, korrigera Windows-enhetstester.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1228">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="f9e89-1229">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f9e89-1229">Az.ApiManagement</span></span>
* <span data-ttu-id="f9e89-1230">**Set-AzApiManagementApi** – Tillagt stöd för att uppdatera Api till ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="f9e89-1230">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="f9e89-1231">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="f9e89-1231">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f9e89-1232">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f9e89-1232">Az.Automation</span></span>
* <span data-ttu-id="f9e89-1233">Åtgärdade cmdleten New-AzureAutomationSoftwareUpdateConfiguration för parametern för inställning av Linux-omstart.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1233">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="f9e89-1234">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="f9e89-1234">Az.Batch</span></span>
* <span data-ttu-id="f9e89-1235">**Get-AzBatchNodeAgentSku** är inaktuell och ersätts av **Get-AzBatchSupportImage** i version 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1235">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f9e89-1236">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f9e89-1236">Az.Compute</span></span>
* <span data-ttu-id="f9e89-1237">Lägg till parametrarna Priority, EvictionPolicy och MaxPrice till cmdletarna New-AzVM och New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f9e89-1237">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="f9e89-1238">Korrigera varningsmeddelande och hjälpdokument för cmdletarna Add-AzVMAdditionalUnattendContent och Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="f9e89-1238">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="f9e89-1239">Åtgärda – skipVmBackup-undantag för virtuella Linux-datorer med hanterade diskar för Set-AzVMDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1239">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="f9e89-1240">Åtgärda fel i uppdatera krypteringsinställningarna i set-AzVMDiskEncryptionExtension, scenario i två steg.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1240">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f9e89-1241">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f9e89-1241">Az.DataFactory</span></span>
* <span data-ttu-id="f9e89-1242">Lägga till CRUD-kommandon för ADF V2-dataflödet: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow och Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1242">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="f9e89-1243">Lägger till åtgärdskommandon för ADF V2-dataflödesfelsökningssession: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand och Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1243">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="f9e89-1244">Uppdatera ADF .Net SDK-versionen till 4.2.0</span><span class="sxs-lookup"><span data-stu-id="f9e89-1244">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f9e89-1245">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f9e89-1245">Az.DataLakeStore</span></span>
* <span data-ttu-id="f9e89-1246">Korrigera kontovalidering så att konton med ”-” kan skickas utan domän</span><span class="sxs-lookup"><span data-stu-id="f9e89-1246">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="f9e89-1247">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="f9e89-1247">Az.HealthcareApis</span></span>
* <span data-ttu-id="f9e89-1248">PowerShell-versionen har uppdaterats till 1.0.0</span><span class="sxs-lookup"><span data-stu-id="f9e89-1248">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="f9e89-1249">Uppdaterade SDK-versionen till 1.0.2</span><span class="sxs-lookup"><span data-stu-id="f9e89-1249">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="f9e89-1250">Uppdatera i tester för att referera till en ny SDK-version</span><span class="sxs-lookup"><span data-stu-id="f9e89-1250">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="f9e89-1251">Utdatastrukturen har uppdaterats från kapslad till förenklad.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1251">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f9e89-1252">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f9e89-1252">Az.IotHub</span></span>
* <span data-ttu-id="f9e89-1253">Lägg till ny routningskälla: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="f9e89-1253">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="f9e89-1254">Mindre felkorrigering: Get-AzIothub returnerar inte subscriptionId</span><span class="sxs-lookup"><span data-stu-id="f9e89-1254">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f9e89-1255">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f9e89-1255">Az.Monitor</span></span>
* <span data-ttu-id="f9e89-1256">Nya åtgärdsgruppsmottagare har lagts till för åtgärdsgrupp   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="f9e89-1256">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="f9e89-1257">Använd vanligt aviseringsschema som är aktiverat för mottagarna.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1257">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="f9e89-1258">Detta gäller inte för SMS, push för Azure-app, ITSM och röstmottagare</span><span class="sxs-lookup"><span data-stu-id="f9e89-1258">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="f9e89-1259">Webhooks har nu stöd för Azure Active Directory-autentisering.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1259">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f9e89-1260">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f9e89-1260">Az.Network</span></span>
* <span data-ttu-id="f9e89-1261">Lägg till ny cmdlet Get-AzAvailableServiceAlias som kan anropas för att hämta de alias som kan användas för tjänstslutpunktsprinciper.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1261">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="f9e89-1262">Stöd för tillägg av trafikväljare har lagts till i gatewayanslutningar för virtuella nätverk</span><span class="sxs-lookup"><span data-stu-id="f9e89-1262">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="f9e89-1263">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="f9e89-1263">New cmdlets added:</span></span>
        - <span data-ttu-id="f9e89-1264">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="f9e89-1264">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="f9e89-1265">Cmdletar har uppdaterats med valfri parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f9e89-1265">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="f9e89-1266">Lägg till stöd för ESP- och AH-protokoll i konfiguration av nätverkssäkerhetsregler</span><span class="sxs-lookup"><span data-stu-id="f9e89-1266">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="f9e89-1267">Uppdaterade cmdletar:</span><span class="sxs-lookup"><span data-stu-id="f9e89-1267">Updated cmdlets:</span></span>
        - <span data-ttu-id="f9e89-1268">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f9e89-1268">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="f9e89-1269">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f9e89-1269">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="f9e89-1270">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f9e89-1270">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="f9e89-1271">Förbättra hanteringen av undantag i Cortex-cmdletar</span><span class="sxs-lookup"><span data-stu-id="f9e89-1271">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="f9e89-1272">Nya generationer och SKU:er för VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="f9e89-1272">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="f9e89-1273">Introducera nya generationer för VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1273">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="f9e89-1274">Introducera nya SKU:er med högt dataflöde för VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1274">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="f9e89-1275">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="f9e89-1275">Az.RedisCache</span></span>
* <span data-ttu-id="f9e89-1276">Uppdaterad referensdokumentation för ”set-AzRedisCache” för att inkludera saknade värden för parametern ”size”</span><span class="sxs-lookup"><span data-stu-id="f9e89-1276">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="f9e89-1277">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f9e89-1277">Az.Sql</span></span>
* <span data-ttu-id="f9e89-1278">Lägg till stöd för inställningen Active Directory administratör på den hanterade instansen</span><span class="sxs-lookup"><span data-stu-id="f9e89-1278">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f9e89-1279">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f9e89-1279">Az.Storage</span></span>
* <span data-ttu-id="f9e89-1280">Uppdatera Lagringsklientbibliotek till 11.1.0</span><span class="sxs-lookup"><span data-stu-id="f9e89-1280">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="f9e89-1281">Lista containrar med hanteringsplans-API, kommer att listas med NextPageLink</span><span class="sxs-lookup"><span data-stu-id="f9e89-1281">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="f9e89-1282">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="f9e89-1282">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="f9e89-1283">Lista lagringskonton från prenumerationen, kommer att listas med NextPageLink</span><span class="sxs-lookup"><span data-stu-id="f9e89-1283">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="f9e89-1284">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f9e89-1284">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="f9e89-1285">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="f9e89-1285">Az.StorageSync</span></span>
* <span data-ttu-id="f9e89-1286">Åtgärda problemet 9810 i Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1286">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f9e89-1287">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f9e89-1287">Az.Websites</span></span>
* <span data-ttu-id="f9e89-1288">Set-AzWebApp – uppdatering av ASP för en app misslyckades</span><span class="sxs-lookup"><span data-stu-id="f9e89-1288">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="f9e89-1289">2.7.0 – september 2019</span><span class="sxs-lookup"><span data-stu-id="f9e89-1289">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="f9e89-1290">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f9e89-1290">Az.ApiManagement</span></span>
* <span data-ttu-id="f9e89-1291">Uppdatera ”-Format”-parameterbeskrivningen i ”Set-AzApiManagementPolicy”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="f9e89-1291">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="f9e89-1292">Referenser för den föråldrade cmdleten ”Update-AzApiManagementDeployment” har tagits bort från referensdokumentationen.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1292">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="f9e89-1293">Använd ”Set-AzApiManagement” i stället.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1293">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f9e89-1294">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f9e89-1294">Az.Automation</span></span>
* <span data-ttu-id="f9e89-1295">Stavfel har korrigerats i exempel i referensdokumentationen för ”Register-AzAutomationDscNode”</span><span class="sxs-lookup"><span data-stu-id="f9e89-1295">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="f9e89-1296">Klargörande har lagts till om OS-begränsningar för Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="f9e89-1296">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="f9e89-1297">Null-referensundantag har korrigerats för -Wait-alternativet i Start-AzAutomationRunbook-cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1297">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f9e89-1298">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f9e89-1298">Az.Compute</span></span>
* <span data-ttu-id="f9e89-1299">Lägg till UploadSizeInBytes-parameter till New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="f9e89-1299">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="f9e89-1300">Lägg till Incremental-parameter till New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="f9e89-1300">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="f9e89-1301">Lägg till en funktion för virtuella datorer med låg prioritet:</span><span class="sxs-lookup"><span data-stu-id="f9e89-1301">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="f9e89-1302">MaxPrice-, EvictionPolicy- och Priority-parametrar har lagts till i New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1302">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="f9e89-1303">MaxPrice-parametern har lagts till i New-AzVmssConfig-, Update-AzVM- och Update-AzVmss-cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1303">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="f9e89-1304">Åtgärda problem med VM-referenser för Get-AzAvailabilitySet-cmdleten när alla tillgänglighetsuppsättningar i prenumerationen visas.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1304">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="f9e89-1305">Korrigera null-undantaget för Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1305">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="f9e89-1306">Korrigera VHD-metoden för sökning relativt till slut.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1306">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="f9e89-1307">Åtgärda UltraSSD-problem för New-AzVM och Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1307">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f9e89-1308">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f9e89-1308">Az.DataFactory</span></span>
* <span data-ttu-id="f9e89-1309">Lägger till 3 nya kommandon för ADF V2 – Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription och Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="f9e89-1309">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="f9e89-1310">ADF .Net SDK har uppdaterats till 4.1.3</span><span class="sxs-lookup"><span data-stu-id="f9e89-1310">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="f9e89-1311">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f9e89-1311">Az.HDInsight</span></span>
* <span data-ttu-id="f9e89-1312">Anrop för icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="f9e89-1312">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f9e89-1313">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f9e89-1313">Az.IotHub</span></span>
* <span data-ttu-id="f9e89-1314">Lägg till stöd för att anropa redundans för en IotHub till den geo-länkade katastrofåterställningsregionen.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1314">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="f9e89-1315">Lägg till stöd för att hantera meddelandeberikning för en IotHub.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1315">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="f9e89-1316">Nya cmdlet:ar är:</span><span class="sxs-lookup"><span data-stu-id="f9e89-1316">New cmdlets are:</span></span>
    - <span data-ttu-id="f9e89-1317">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="f9e89-1317">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="f9e89-1318">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="f9e89-1318">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="f9e89-1319">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="f9e89-1319">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="f9e89-1320">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="f9e89-1320">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f9e89-1321">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f9e89-1321">Az.Monitor</span></span>
* <span data-ttu-id="f9e89-1322">Pekar på den senaste Monitor SDK:n, dvs. 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="f9e89-1322">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="f9e89-1323">Lägger till bakåtkompatibla ändringar i Metrics-cmdletarna, dvs. enhetsuppräkningen stöder flera nya värden.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1323">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="f9e89-1324">Detta är skrivskyddade cmdletar, så det förekommer inga ändringar i inmatningen för cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1324">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="f9e89-1325">API-versionen för **ActionGroups**-begäranden är nu **2019-06-01**. Tidigare var den **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1325">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="f9e89-1326">Test av scenarier har uppdaterats för att anpassas till den här ändringen.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1326">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="f9e89-1327">Ett nytt obligatoriskt argument har lagts till för konstruktorerna för klasserna **EmailReceiver** och **WebhookReceiver** – ett booleskt värde med namnet **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1327">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="f9e89-1328">Värdet är för närvarande fast till **false** så att den här icke-bakåtkompatibla ändringen är dold från cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1328">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="f9e89-1329">**Obs!** Det här är en tillfällig ändring som måste verifieras av Alerts-teamet.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1329">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="f9e89-1330">Ordningen på argumenten för konstruktorn för klassen **Source** (relaterad till klassen **ScheduledQueryRuleSource**) har ändrats från den tidigare SDK:n.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1330">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="f9e89-1331">Den här ändringen krävde korrigering av två enhetstest: de kompilerades, men testerna skickades inte.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1331">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="f9e89-1332">Ordningen på argumenten för konstruktorn för klassen **AlertingAction** (relaterad till klassen **ScheduledQueryRuleSource**) har ändrats från den tidigare SDK:n.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1332">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="f9e89-1333">Den här ändringen krävde korrigering av två enhetstest: de kompilerades, men testerna skickades inte.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1333">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="f9e89-1334">Stöd för kriterier för dynamiskt tröskelvärde för måttavisering v2</span><span class="sxs-lookup"><span data-stu-id="f9e89-1334">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="f9e89-1335">New-AzMetricAlertRuleV2Criteria: skapar nu även kriterier för dynamiskt tröskelvärde</span><span class="sxs-lookup"><span data-stu-id="f9e89-1335">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="f9e89-1336">Add-AzMetricAlertRuleV2: accepterar nu även kriterier för dynamiskt tröskelvärde</span><span class="sxs-lookup"><span data-stu-id="f9e89-1336">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="f9e89-1337">Förbättringar i schemalagd frågeregel (SQR)</span><span class="sxs-lookup"><span data-stu-id="f9e89-1337">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="f9e89-1338">Cmdletar accepterar ”Location”-parameter i båda formaten, antingen platsen (t.ex. eastus) eller platsens visningsnamn (t.ex. USA, östra)</span><span class="sxs-lookup"><span data-stu-id="f9e89-1338">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="f9e89-1339">”Enabled”-parametern illustreras korrekt i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="f9e89-1339">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="f9e89-1340">Exempel för den valfria parametern ”ActionGroup” har lagts till</span><span class="sxs-lookup"><span data-stu-id="f9e89-1340">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="f9e89-1341">Förbättrade hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="f9e89-1341">Overall improved help files</span></span>
* <span data-ttu-id="f9e89-1342">Åtgärda bugg då omfattningstypen fastställs för ”Set-AzActionRule”</span><span class="sxs-lookup"><span data-stu-id="f9e89-1342">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f9e89-1343">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f9e89-1343">Az.Network</span></span>
* <span data-ttu-id="f9e89-1344">Korrigera felaktigt exempel i referensdokumentationen för ”New-AzApplicationGateway”</span><span class="sxs-lookup"><span data-stu-id="f9e89-1344">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="f9e89-1345">Lägg till anmärkning i ”Get-AzNetworkWatcherPacketCapture”-referensdokumentationen om hämtning av alla egenskaper för en paketinsamling</span><span class="sxs-lookup"><span data-stu-id="f9e89-1345">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="f9e89-1346">Exempel har korrigerats i ”Test-AzNetworkWatcherIPFlow”-referensdokumentationen för korrekt uppräkning av nätverkskort</span><span class="sxs-lookup"><span data-stu-id="f9e89-1346">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="f9e89-1347">Förbättrad tolkning av molnundantag för att visa eventuell ytterligare information</span><span class="sxs-lookup"><span data-stu-id="f9e89-1347">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="f9e89-1348">Förbättrad tolkning av molnundantag för att hantera ytterligare en typ av SDK-undantag</span><span class="sxs-lookup"><span data-stu-id="f9e89-1348">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="f9e89-1349">Felaktig mappning av säkerhetsregelmodeller har korrigerats</span><span class="sxs-lookup"><span data-stu-id="f9e89-1349">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="f9e89-1350">Egenskaper har lagts till för nätverksgränssnittet för funktionen Privat IP</span><span class="sxs-lookup"><span data-stu-id="f9e89-1350">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="f9e89-1351">Egenskapen ”PrivateEndpoint” har lagts till som en typ av PSResourceId till PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="f9e89-1351">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="f9e89-1352">Egenskapen ”PrivateLinkConnectionProperties” har lagts till som en typ av PSIpConfigurationConnectivityInformation till PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="f9e89-1352">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="f9e89-1353">Modellklassen PSIpConfigurationConnectivityInformation har lagts till</span><span class="sxs-lookup"><span data-stu-id="f9e89-1353">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="f9e89-1354">ApplicationRuleProtocolType ”mssql” har lagts till för Azure Firewall-resurs</span><span class="sxs-lookup"><span data-stu-id="f9e89-1354">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="f9e89-1355">MultiLink-stöd i virtuellt WAN</span><span class="sxs-lookup"><span data-stu-id="f9e89-1355">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="f9e89-1356">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="f9e89-1356">New cmdlets</span></span>
        - <span data-ttu-id="f9e89-1357">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="f9e89-1357">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="f9e89-1358">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="f9e89-1358">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="f9e89-1359">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="f9e89-1359">Updated cmdlet:</span></span>
        - <span data-ttu-id="f9e89-1360">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="f9e89-1360">New-VpnSite</span></span>
        - <span data-ttu-id="f9e89-1361">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="f9e89-1361">Update-VpnSite</span></span>
        - <span data-ttu-id="f9e89-1362">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="f9e89-1362">New-VpnConnection</span></span>
        - <span data-ttu-id="f9e89-1363">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="f9e89-1363">Update-VpnConnection</span></span>
* <span data-ttu-id="f9e89-1364">Dokument för vissa PowerShell-exempel har korrigerats så att Az-cmdletar används i stället för AzureRM-cmdletar</span><span class="sxs-lookup"><span data-stu-id="f9e89-1364">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f9e89-1365">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f9e89-1365">Az.RecoveryServices</span></span>
* <span data-ttu-id="f9e89-1366">Uppdatera AzureVMpolicy-objekt med ProtectedItemsCount-attribut</span><span class="sxs-lookup"><span data-stu-id="f9e89-1366">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="f9e89-1367">Ytterligare tester har lagts till för VM-princip och återställning av ursprungligt lagringskonto</span><span class="sxs-lookup"><span data-stu-id="f9e89-1367">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="f9e89-1368">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f9e89-1368">Az.Resources</span></span>
* <span data-ttu-id="f9e89-1369">Åtgärda fel där det inte gick att anropa New-AzRoleAssignment utan parametern Scope.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1369">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f9e89-1370">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f9e89-1370">Az.ServiceFabric</span></span>
* <span data-ttu-id="f9e89-1371">Stavfel har korrigerats i exempel för ”Update-AzServiceFabricReliability”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="f9e89-1371">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="f9e89-1372">Lägger till nya cmdletar för att hantera program och tjänster:</span><span class="sxs-lookup"><span data-stu-id="f9e89-1372">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="f9e89-1373">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="f9e89-1373">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="f9e89-1374">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="f9e89-1374">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="f9e89-1375">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="f9e89-1375">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="f9e89-1376">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="f9e89-1376">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="f9e89-1377">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="f9e89-1377">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="f9e89-1378">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="f9e89-1378">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="f9e89-1379">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="f9e89-1379">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="f9e89-1380">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="f9e89-1380">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="f9e89-1381">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="f9e89-1381">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="f9e89-1382">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="f9e89-1382">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="f9e89-1383">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="f9e89-1383">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="f9e89-1384">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="f9e89-1384">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="f9e89-1385">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="f9e89-1385">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="f9e89-1386">Service Fabric SDK har uppgraderats till version 1.2.0 som använder Service Fabric-resursprovidern med API-version 2019-03-01.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1386">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="f9e89-1387">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="f9e89-1387">Az.SignalR</span></span>
* <span data-ttu-id="f9e89-1388">Lägg till Update-, Restart-, CheckNameAvailability- och GetUsage-cmdletar</span><span class="sxs-lookup"><span data-stu-id="f9e89-1388">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="f9e89-1389">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f9e89-1389">Az.Sql</span></span>
* <span data-ttu-id="f9e89-1390">Uppdatera exempel i referensdokumentationen för ”Get-AzSqlElasticPool”</span><span class="sxs-lookup"><span data-stu-id="f9e89-1390">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="f9e89-1391">vCore-exempel för att skapa en elastisk pool (New-AzSqlElasticPool) har lagts till.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1391">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="f9e89-1392">Ta bort verifieringen av EmailAddresses och kontrollen som bekräftar att EmailAdmins inte är falskt när EmailAddresses är tomt i Set-AzSqlServerAdvancedThreatProtectionPolicy och Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="f9e89-1392">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="f9e89-1393">Server-/databasgranskningsinställningar kan tas bort när det finns flera diagnostikinställningar som aktiverar granskningskategorin.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1393">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="f9e89-1394">Åtgärda verifiering av e-postadresser i flera Sql Vulnerability Assessment-cmdletar (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting och Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="f9e89-1394">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f9e89-1395">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f9e89-1395">Az.Storage</span></span>
* <span data-ttu-id="f9e89-1396">Exempel i referensdokumentationen för ”Get-AzStorageAccountKey” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="f9e89-1396">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="f9e89-1397">Vid upp- och nedladdning av en Azure-fil kan SMB-egenskaperna för källfilen (t.ex. filattribut, tidpunkten då filen skapades och tidpunkten för den senaste skrivningen) sparas i målfilen</span><span class="sxs-lookup"><span data-stu-id="f9e89-1397">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="f9e89-1398">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="f9e89-1398">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="f9e89-1399">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="f9e89-1399">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="f9e89-1400">Korrigera problem med uppladdningen av blockblob med egenskaper/metadata för ImmutabilityPolicy i containrar.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1400">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="f9e89-1401">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="f9e89-1401">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="f9e89-1402">Stöd för hantering av Azure-filresurser med API för hanteringsplan</span><span class="sxs-lookup"><span data-stu-id="f9e89-1402">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="f9e89-1403">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="f9e89-1403">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="f9e89-1404">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="f9e89-1404">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="f9e89-1405">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="f9e89-1405">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="f9e89-1406">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="f9e89-1406">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f9e89-1407">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f9e89-1407">Az.Websites</span></span>
* <span data-ttu-id="f9e89-1408">Åtgärdar problemet där webapp-taggar togs bort när appen migrerades till nya ASP</span><span class="sxs-lookup"><span data-stu-id="f9e89-1408">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="f9e89-1409">Åtgärda Publish-AzureWebapp så att det fungerar i Linux och Windows</span><span class="sxs-lookup"><span data-stu-id="f9e89-1409">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="f9e89-1410">Uppdatera exempel i ”Get-AzWebAppPublishingProfile”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="f9e89-1410">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="f9e89-1411">2.6.0 – augusti 2019</span><span class="sxs-lookup"><span data-stu-id="f9e89-1411">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="f9e89-1412">Allmänt</span><span class="sxs-lookup"><span data-stu-id="f9e89-1412">General</span></span>
* <span data-ttu-id="f9e89-1413">Åtgärdade diverse skrivfel i flera moduler</span><span class="sxs-lookup"><span data-stu-id="f9e89-1413">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f9e89-1414">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f9e89-1414">Az.Accounts</span></span>
* <span data-ttu-id="f9e89-1415">Stöd för användartilldelat MSI i Azure Functions-autentisering (#9479)</span><span class="sxs-lookup"><span data-stu-id="f9e89-1415">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="f9e89-1416">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="f9e89-1416">Az.Aks</span></span>
* <span data-ttu-id="f9e89-1417">Åtgärda problem med utdata för "Get-AzAks"</span><span class="sxs-lookup"><span data-stu-id="f9e89-1417">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="f9e89-1418">Mer information här: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="f9e89-1418">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="f9e89-1419">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f9e89-1419">Az.ApiManagement</span></span>
* <span data-ttu-id="f9e89-1420">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="f9e89-1420">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="f9e89-1421">Uppdatera .net-NuGet-versionen, som inte tillämpar begränsningar för productId, apiId och userId</span><span class="sxs-lookup"><span data-stu-id="f9e89-1421">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="f9e89-1422">**Get-AzApiManagementProduct** – Lade till stöd för frågekörning mot produkter via API.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1422">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="f9e89-1423">**New-AzApiManagementApiRevision** – Korrigering för problem där ApiRevisionDescription inte angavs vid skapande av ny API-revision https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="f9e89-1423">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="f9e89-1424">Åtgärdade skrivfel i modellen "PsApiManagementOAuth2AuthrozationServer" till "PsApiManagementOAuth2AuthorizationServer"</span><span class="sxs-lookup"><span data-stu-id="f9e89-1424">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="f9e89-1425">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="f9e89-1425">Az.Batch</span></span>
* <span data-ttu-id="f9e89-1426">Åtgärdade skrivfel i hjälpmeddelande och dokumentation till att skriva Windows med versaler</span><span class="sxs-lookup"><span data-stu-id="f9e89-1426">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="f9e89-1427">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f9e89-1427">Az.Cdn</span></span>
* <span data-ttu-id="f9e89-1428">Åtgärdade skrivfel i CDN-modulens konverteringshjälp</span><span class="sxs-lookup"><span data-stu-id="f9e89-1428">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f9e89-1429">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f9e89-1429">Az.Compute</span></span>
* <span data-ttu-id="f9e89-1430">Lägg till VmssId i New-AzVMConfig-cmdleten</span><span class="sxs-lookup"><span data-stu-id="f9e89-1430">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="f9e89-1431">Lägg till parametrarna TerminateScheduledEvents och TerminateScheduledEventNotBeforeTimeoutInMinutes i New-AzVmssConfig och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f9e89-1431">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="f9e89-1432">Lägg till egenskapen HyperVGeneration till avbildningsobjekt för virtuell dator</span><span class="sxs-lookup"><span data-stu-id="f9e89-1432">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="f9e89-1433">Lägg till funktioner för Host och HostGroup</span><span class="sxs-lookup"><span data-stu-id="f9e89-1433">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="f9e89-1434">Nya cmdletar:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="f9e89-1434">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="f9e89-1435">HostId-parametern läggs till i New-AzVMConfig och New-AzVM</span><span class="sxs-lookup"><span data-stu-id="f9e89-1435">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="f9e89-1436">Uppdatera exempel i "Invoke-AzVMRunCommand"-dokumentationen till att använda rätt parameternamn</span><span class="sxs-lookup"><span data-stu-id="f9e89-1436">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="f9e89-1437">Uppdatera "-VolumeType"-beskrivningen i referensdokumentationen för "set-AzVMDiskEncryptionExtension" och "set-AzVmssDiskEncryptionExtension"</span><span class="sxs-lookup"><span data-stu-id="f9e89-1437">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f9e89-1438">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f9e89-1438">Az.DataFactory</span></span>
* <span data-ttu-id="f9e89-1439">Åtgärda skrivfel till att använda versaler för "Windows" i "New-AzDataFactoryEncryptValue"-dokumentationen</span><span class="sxs-lookup"><span data-stu-id="f9e89-1439">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="f9e89-1440">Uppdaterade ADF .Net SDK-versionen till 4.1.2</span><span class="sxs-lookup"><span data-stu-id="f9e89-1440">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="f9e89-1441">Lägg till parametrarna "DataProxyIntegrationRuntimeName", "DataProxyStagingLinkedServiceName" och "DataProxyStagingPath" för "Set-AzureRmDataFactoryV2IntegrationRuntime"-cmd för att aktivera konfiguration av lokalt installerad integrationskörning som en proxy för SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="f9e89-1441">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="f9e89-1442">Uppdaterade PSTriggerRun till att visa utlöst pipeline, meddelande och egenskaper samt PSActivityRun till att visa aktivitetstypen</span><span class="sxs-lookup"><span data-stu-id="f9e89-1442">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f9e89-1443">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f9e89-1443">Az.DataLakeStore</span></span>
* <span data-ttu-id="f9e89-1444">Korrigering av frysning av Get-DataLakeStoreDeletedItem för fel eller fjärrundantag.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1444">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f9e89-1445">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f9e89-1445">Az.EventHub</span></span>
* <span data-ttu-id="f9e89-1446">Korrigering av problem #9658 : Skrivfel i parametern VirtualNteworkRule i Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="f9e89-1446">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="f9e89-1447">Korrigering av problem #9558 : Set-AzEventHubNamespace använder PATCH i stället för PUT</span><span class="sxs-lookup"><span data-stu-id="f9e89-1447">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="f9e89-1448">lade till parametern EnableKafka i Set-AzEventHubNamespace-cmdleten</span><span class="sxs-lookup"><span data-stu-id="f9e89-1448">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="f9e89-1449">Korrigering av problem #9786 : kan inte skapa en regel med Endast lyssna-behörighet</span><span class="sxs-lookup"><span data-stu-id="f9e89-1449">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="f9e89-1450">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="f9e89-1450">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="f9e89-1451">Åtgärdade skrivfel i dokumentation där "Azure" skrevs helt med gemener</span><span class="sxs-lookup"><span data-stu-id="f9e89-1451">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f9e89-1452">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f9e89-1452">Az.Monitor</span></span>
* <span data-ttu-id="f9e89-1453">Åtgärdade felaktigt parameternamn i hjälpdokumentationen</span><span class="sxs-lookup"><span data-stu-id="f9e89-1453">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f9e89-1454">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f9e89-1454">Az.Network</span></span>
* <span data-ttu-id="f9e89-1455">Uppdaterade New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="f9e89-1455">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="f9e89-1456">Gjorde parametern "PublicIpAddress" inaktuell eftersom den aldrig används på serversidan.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1456">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="f9e89-1457">Lade till den valfria parametern "Primary", som anger huruvida den aktuella IP-konfigurationen är den primära.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1457">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="f9e89-1458">Förbättrade hanteringen av felundantag för begärande från SDK – åtgärdar problemet att tidigare SDK-undantag inte hanteras på rätt sätt, vilket leder till att viktig felinformation inte visas</span><span class="sxs-lookup"><span data-stu-id="f9e89-1458">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="f9e89-1459">Justerade valideringslogiken för IPv6-IP-prefix till att kontrollera korrekt IPv6-prefixlängd.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1459">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="f9e89-1460">Uppdaterade Get-AzVirtualNetworkSubnetConfig: Lade till parameter som anges till get av undernätets resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1460">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="f9e89-1461">Uppdaterade beskrivningen av parametern Location för AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="f9e89-1461">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f9e89-1462">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f9e89-1462">Az.OperationalInsights</span></span>
* <span data-ttu-id="f9e89-1463">Uppdaterade dokumentation för "New-AzOperationalInsightsLinuxSyslogDataSource"</span><span class="sxs-lookup"><span data-stu-id="f9e89-1463">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="f9e89-1464">Lade till exempel</span><span class="sxs-lookup"><span data-stu-id="f9e89-1464">Added example</span></span>
    - <span data-ttu-id="f9e89-1465">Uppdaterade beskrivningen av parametern "-Name"</span><span class="sxs-lookup"><span data-stu-id="f9e89-1465">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="f9e89-1466">Lade till ett exempel för New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="f9e89-1466">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="f9e89-1467">Ändrade beskrivningen av parametern -Name för New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="f9e89-1467">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f9e89-1468">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f9e89-1468">Az.RecoveryServices</span></span>
* <span data-ttu-id="f9e89-1469">Uppdatera "Get-AzRecoveryServicesBackupJobDetail.md"</span><span class="sxs-lookup"><span data-stu-id="f9e89-1469">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="f9e89-1470">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f9e89-1470">Az.Resources</span></span>
* <span data-ttu-id="f9e89-1471">Lägg till stöd för den nya API-versionen från 2019-05-10 för Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="f9e89-1471">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="f9e89-1472">Lägg till stöd för "copy.count = 0" för variabler, resurser och egenskaper</span><span class="sxs-lookup"><span data-stu-id="f9e89-1472">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="f9e89-1473">Resurser med "condition = false" eller "copy.count = 0" tas bort i complete-läget</span><span class="sxs-lookup"><span data-stu-id="f9e89-1473">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="f9e89-1474">Lägg till ett exempel på tilldelning av princip på prenumerationsnivå i hjälpdokumentationen</span><span class="sxs-lookup"><span data-stu-id="f9e89-1474">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="f9e89-1475">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f9e89-1475">Az.ServiceBus</span></span>
* <span data-ttu-id="f9e89-1476">Korrigering av problem #9658 : Skrivfel i parametern VirtualNetworkRule i set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="f9e89-1476">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="f9e89-1477">Korrigering av problem #9786 : kan inte skapa en regel med Endast lyssna-behörighet</span><span class="sxs-lookup"><span data-stu-id="f9e89-1477">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="f9e89-1478">Lade till det nya kommandot "Test-AzServiceBusNameAvailability" för att kontrollera namntillgängligheten för kö och ämne</span><span class="sxs-lookup"><span data-stu-id="f9e89-1478">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f9e89-1479">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f9e89-1479">Az.ServiceFabric</span></span>
* <span data-ttu-id="f9e89-1480">Åtgärda buggar med tillägg av nodtyps-cmdlet:</span><span class="sxs-lookup"><span data-stu-id="f9e89-1480">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="f9e89-1481">NullReferenceException-bugg när resursgrupp hade annan vmss som inte är relaterad till Service Fabric-klustret.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1481">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="f9e89-1482">Åtgärdar problemet: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="f9e89-1482">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="f9e89-1483">Åtgärda bugg där cmdleten misslyckades om virtualNetwork var i en annan resursgrupp än klustret.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1483">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="f9e89-1484">Åtgärdar problemet: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="f9e89-1484">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="f9e89-1485">AzServiceFabricApplicationCertificate-cmdleten görs inaktuell</span><span class="sxs-lookup"><span data-stu-id="f9e89-1485">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="f9e89-1486">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f9e89-1486">Az.Sql</span></span>
* <span data-ttu-id="f9e89-1487">Uppdatera dokumentation om gamla gransknings-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1487">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f9e89-1488">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f9e89-1488">Az.Storage</span></span>
* <span data-ttu-id="f9e89-1489">Uppdatera hjälpen för Get/Close-AzStorageFileHandle genom att lägga till fler scenarier i cmdlet-exempel och uppdatera parameterbeskrivningar</span><span class="sxs-lookup"><span data-stu-id="f9e89-1489">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="f9e89-1490">Stöd för StandardBlobTier i uppladdningsblob och kopieringsblob</span><span class="sxs-lookup"><span data-stu-id="f9e89-1490">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="f9e89-1491">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="f9e89-1491">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="f9e89-1492">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="f9e89-1492">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="f9e89-1493">Stöd för rehydratiseringsprioritet i kopieringsblob</span><span class="sxs-lookup"><span data-stu-id="f9e89-1493">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="f9e89-1494">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="f9e89-1494">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f9e89-1495">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f9e89-1495">Az.Websites</span></span>
* <span data-ttu-id="f9e89-1496">Lägg till klargöranden gällande parametern -AppSettings i Set-AzWebApp och Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f9e89-1496">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="f9e89-1497">2.5.0 – July 2019</span><span class="sxs-lookup"><span data-stu-id="f9e89-1497">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f9e89-1498">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f9e89-1498">Az.Accounts</span></span>
* <span data-ttu-id="f9e89-1499">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="f9e89-1499">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="f9e89-1500">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="f9e89-1500">Az.ApplicationInsights</span></span>
* <span data-ttu-id="f9e89-1501">Korrigera skrivfel i exempel i dokumentationen för Remove-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="f9e89-1501">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f9e89-1502">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f9e89-1502">Az.Automation</span></span>
* <span data-ttu-id="f9e89-1503">Korrigera skrivfel i resurssträng</span><span class="sxs-lookup"><span data-stu-id="f9e89-1503">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f9e89-1504">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f9e89-1504">Az.CognitiveServices</span></span>
* <span data-ttu-id="f9e89-1505">Stöd för NetworkRuleSet har lagts till.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1505">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f9e89-1506">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f9e89-1506">Az.Compute</span></span>
* <span data-ttu-id="f9e89-1507">Lägg till saknade egenskaper (ComputerName, OsName, OsVersion och HyperVGeneration) för visningsobjekt i den virtuella datorinstansen.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1507">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="f9e89-1508">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f9e89-1508">Az.ContainerRegistry</span></span>
* <span data-ttu-id="f9e89-1509">Åtgärda skrivfel i Remove-AzContainerRegistryReplication för parametern Replication</span><span class="sxs-lookup"><span data-stu-id="f9e89-1509">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="f9e89-1510">Mer information finns här: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="f9e89-1510">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f9e89-1511">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f9e89-1511">Az.DataFactory</span></span>
* <span data-ttu-id="f9e89-1512">ADF .Net SDK-versionen har uppdaterats till 4.1.0</span><span class="sxs-lookup"><span data-stu-id="f9e89-1512">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="f9e89-1513">Korrigera skrivfel i dokumentationen för Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="f9e89-1513">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f9e89-1514">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f9e89-1514">Az.EventHub</span></span>
* <span data-ttu-id="f9e89-1515">Ny cmmdlet har lagts till för att skapa SAS-token: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="f9e89-1515">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="f9e89-1516">verifierings- och felmeddelande har lagts till för authorizationrules-rättigheter om endast "hantera" har tilldelats</span><span class="sxs-lookup"><span data-stu-id="f9e89-1516">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f9e89-1517">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f9e89-1517">Az.KeyVault</span></span>
* <span data-ttu-id="f9e89-1518">Stöd har lagts till för att ange KeySize för certifikatprinciper</span><span class="sxs-lookup"><span data-stu-id="f9e89-1518">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="f9e89-1519">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="f9e89-1519">Az.LogicApp</span></span>
* <span data-ttu-id="f9e89-1520">Korrigering för Get-AzIntegrationAccountMap för att lista alla mappningstyper</span><span class="sxs-lookup"><span data-stu-id="f9e89-1520">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="f9e89-1521">Ny MapType-parameter har lagts till för filtrering</span><span class="sxs-lookup"><span data-stu-id="f9e89-1521">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="f9e89-1522">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="f9e89-1522">Az.ManagedServices</span></span>
* <span data-ttu-id="f9e89-1523">Stöd för API-versionen 2019-06-01 (GA) har lagts till</span><span class="sxs-lookup"><span data-stu-id="f9e89-1523">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f9e89-1524">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f9e89-1524">Az.Network</span></span>
* <span data-ttu-id="f9e89-1525">Lägg till stöd för privat slutpunkt och privat länktjänst</span><span class="sxs-lookup"><span data-stu-id="f9e89-1525">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="f9e89-1526">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="f9e89-1526">New cmdlets</span></span>
        - <span data-ttu-id="f9e89-1527">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f9e89-1527">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="f9e89-1528">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f9e89-1528">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="f9e89-1529">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f9e89-1529">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="f9e89-1530">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f9e89-1530">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="f9e89-1531">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f9e89-1531">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="f9e89-1532">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f9e89-1532">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="f9e89-1533">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="f9e89-1533">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="f9e89-1534">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f9e89-1534">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="f9e89-1535">Nedanstående kommandon för funktionen har uppdaterats: Flaggan PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies på undernätet i VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f9e89-1535">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="f9e89-1536">Uppdaterade New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="f9e89-1536">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="f9e89-1537">Valfri parameter har lagts till – PrivateEndpointNetworkPoliciesFlag som konfigurerar huruvida nätverksprinciper ska tillämpas på en privat slutpunkt i det här undernätet.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1537">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="f9e89-1538">Valfri parameter har lagts till – PrivateLinkServiceNetworkPoliciesFlag som konfigurerar huruvida nätverksprinciper ska tillämpas på en privat länktjänst i det här undernätet.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1538">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="f9e89-1539">AzPrivateLinkService för cmdlet-parametern ServiceName har bytt namn till Name med aliaset ServiceName för bakåtkompatibilitet</span><span class="sxs-lookup"><span data-stu-id="f9e89-1539">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="f9e89-1540">Aktivera ICMP-protokoll för konfiguration av nätverkssäkerhetsregler</span><span class="sxs-lookup"><span data-stu-id="f9e89-1540">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="f9e89-1541">Uppdaterade cmdletar</span><span class="sxs-lookup"><span data-stu-id="f9e89-1541">Updated cmdlets</span></span>
        - <span data-ttu-id="f9e89-1542">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f9e89-1542">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="f9e89-1543">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f9e89-1543">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="f9e89-1544">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f9e89-1544">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="f9e89-1545">Lägg till ConnectionProtocolType (Ikev1/Ikev2) som en konfigurerbar parameter för New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f9e89-1545">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="f9e89-1546">Lägg till PrivateIpAddressVersion i LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="f9e89-1546">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="f9e89-1547">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="f9e89-1547">Updated cmdlet:</span></span>
        - <span data-ttu-id="f9e89-1548">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f9e89-1548">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="f9e89-1549">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f9e89-1549">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="f9e89-1550">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f9e89-1550">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="f9e89-1551">Uppdatering av Application Gateway-kommandot New-AzApplicationGatewayProbeConfig för stöd av anpassad port i Probe</span><span class="sxs-lookup"><span data-stu-id="f9e89-1551">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="f9e89-1552">Uppdaterade New-AzApplicationGatewayProbeConfig: Den valfria parametern Port som används för avsökning i serverdelen har lagts till.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1552">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="f9e89-1553">Denna parameter gäller för SKU:erna Standard_V2 och WAF_V2.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1553">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f9e89-1554">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f9e89-1554">Az.OperationalInsights</span></span>
* <span data-ttu-id="f9e89-1555">Uppdaterade standardversionen för sparade sökningar till 1.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1555">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="f9e89-1556">Åtgärdade hantering av anpassad log null regex</span><span class="sxs-lookup"><span data-stu-id="f9e89-1556">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f9e89-1557">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f9e89-1557">Az.RecoveryServices</span></span>
* <span data-ttu-id="f9e89-1558">Uppdatera Get-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="f9e89-1558">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="f9e89-1559">Uppdatera Get-AzRecoveryServicesBackupContainer.md</span><span class="sxs-lookup"><span data-stu-id="f9e89-1559">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="f9e89-1560">Uppdatera Get-AzRecoveryServicesVault.md</span><span class="sxs-lookup"><span data-stu-id="f9e89-1560">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="f9e89-1561">Uppdatera Wait-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="f9e89-1561">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="f9e89-1562">Uppdatera Set-AzRecoveryServicesVaultContext.md</span><span class="sxs-lookup"><span data-stu-id="f9e89-1562">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="f9e89-1563">Uppdatera Get-AzRecoveryServicesBackupItem.md</span><span class="sxs-lookup"><span data-stu-id="f9e89-1563">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="f9e89-1564">Uppdatera Get-AzRecoveryServicesBackupRecoveryPoint.md</span><span class="sxs-lookup"><span data-stu-id="f9e89-1564">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="f9e89-1565">Uppdatera Restore-AzRecoveryServicesBackupItem.md</span><span class="sxs-lookup"><span data-stu-id="f9e89-1565">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="f9e89-1566">Uppdaterat tjänstanrop för avregistrering av container för Azure-filresurs</span><span class="sxs-lookup"><span data-stu-id="f9e89-1566">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="f9e89-1567">Uppdatera Set-AzRecoveryServicesAsrAlertSetting.md</span><span class="sxs-lookup"><span data-stu-id="f9e89-1567">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="f9e89-1568">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f9e89-1568">Az.Resources</span></span>
- <span data-ttu-id="f9e89-1569">Ta bort den cmdlet som saknas och som refereras i dokumentationen till New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f9e89-1569">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="f9e89-1570">Princip-cmdletar har uppdaterats så att de använder den nya API-versionen 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="f9e89-1570">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="f9e89-1571">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f9e89-1571">Az.ServiceBus</span></span>
* <span data-ttu-id="f9e89-1572">Ny cmmdlet har lagts till för att skapa SAS-token: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="f9e89-1572">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="f9e89-1573">verifierings- och felmeddelande har lagts till för authorizationrules-rättigheter om endast "hantera" har tilldelats</span><span class="sxs-lookup"><span data-stu-id="f9e89-1573">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="f9e89-1574">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f9e89-1574">Az.Sql</span></span>
* <span data-ttu-id="f9e89-1575">Åtgärda saknade exempel för Set-AzSqlDatabaseSecondary cmdlet</span><span class="sxs-lookup"><span data-stu-id="f9e89-1575">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="f9e89-1576">Åtgärda angivna återkommande genomsökningar för bedömning av säkerhetsrisk utan angivna e-postadresser</span><span class="sxs-lookup"><span data-stu-id="f9e89-1576">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="f9e89-1577">Korrigera ett skrivfel i ett varningsmeddelande.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1577">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f9e89-1578">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f9e89-1578">Az.Storage</span></span>
* <span data-ttu-id="f9e89-1579">Uppdatera exempel i referensdokumentationen för Get-AzStorageAccount så att rätt parameternamn används</span><span class="sxs-lookup"><span data-stu-id="f9e89-1579">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="f9e89-1580">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="f9e89-1580">Az.StorageSync</span></span>
* <span data-ttu-id="f9e89-1581">Lägger till cmdleten Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1581">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="f9e89-1582">Åtgärda problem 9551 så att TierFilesOlderThanDays föredras</span><span class="sxs-lookup"><span data-stu-id="f9e89-1582">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f9e89-1583">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f9e89-1583">Az.Websites</span></span>
* <span data-ttu-id="f9e89-1584">Åtgärdar ett fel där vissa SiteConfig-egenskaper inte returnerades av Get-AzWebApp och Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="f9e89-1584">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="f9e89-1585">Lägger till en ny platsparameter för Get-AzDeletedWebApp och Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="f9e89-1585">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="f9e89-1586">Åtgärdar ett fel i kloning av webbapp-platser som använder New-AzWebApp-IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="f9e89-1586">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="f9e89-1587">2.4.0 – juli 2019</span><span class="sxs-lookup"><span data-stu-id="f9e89-1587">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f9e89-1588">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f9e89-1588">Az.Accounts</span></span>
* <span data-ttu-id="f9e89-1589">Lägg till stöd för profil-cmdletar</span><span class="sxs-lookup"><span data-stu-id="f9e89-1589">Add support for profile cmdlets</span></span>
* <span data-ttu-id="f9e89-1590">Lägg till stöd för miljöer och dataplaner i genererade cmdletar</span><span class="sxs-lookup"><span data-stu-id="f9e89-1590">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="f9e89-1591">Åtgärda bugg där fel slutpunkt i vissa fall användes för cmdletar för dataplaner i Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="f9e89-1591">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="f9e89-1592">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="f9e89-1592">Az.Advisor</span></span>
* <span data-ttu-id="f9e89-1593">GA-version av Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="f9e89-1593">GA release of Az.Advisor</span></span>
* <span data-ttu-id="f9e89-1594">Den här modulen ingår nu som en del av `Az`-sammanslagningsmodulen</span><span class="sxs-lookup"><span data-stu-id="f9e89-1594">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="f9e89-1595">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f9e89-1595">Az.ApiManagement</span></span>
* <span data-ttu-id="f9e89-1596">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="f9e89-1596">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="f9e89-1597">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="f9e89-1597">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="f9e89-1598">Stöd för att fråga prenumerationer efter användare och produkt har lagts till</span><span class="sxs-lookup"><span data-stu-id="f9e89-1598">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="f9e89-1599">Stöd för att fråga med hjälp av omfång ”/”, ”/apis”, ”/apis/echo-api” har lagts till</span><span class="sxs-lookup"><span data-stu-id="f9e89-1599">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="f9e89-1600">Korrigering av problem https://github.com/Azure/azure-powershell/issues/9307 och https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="f9e89-1600">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="f9e89-1601">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="f9e89-1601">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="f9e89-1602">Stöd för att ange ”ApiVersion” och ”ApiVersionSetId” när API:er importeras har lagts till</span><span class="sxs-lookup"><span data-stu-id="f9e89-1602">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f9e89-1603">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f9e89-1603">Az.Automation</span></span>
* <span data-ttu-id="f9e89-1604">Bugg med cmdleten Set-AzAutomationConnectionFieldValue för att hantera strängvärde har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1604">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f9e89-1605">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f9e89-1605">Az.Compute</span></span>
* <span data-ttu-id="f9e89-1606">Lägg till parametern HyperVGeneration i New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="f9e89-1606">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f9e89-1607">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f9e89-1607">Az.DataFactory</span></span>
* <span data-ttu-id="f9e89-1608">Uppdaterar utdata från ADF-cmdletar som hämtar aktivitetskörningar, hämtar pipelinekörningar och hämtar utlösarkörningar för stöd för Select-Object-pipe.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1608">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="f9e89-1609">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="f9e89-1609">Az.EventGrid</span></span>
* <span data-ttu-id="f9e89-1610">Korrigera stavfel i dokumentation om ”New-AzEventGridSubscription”</span><span class="sxs-lookup"><span data-stu-id="f9e89-1610">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f9e89-1611">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f9e89-1611">Az.IotHub</span></span>
* <span data-ttu-id="f9e89-1612">Lägg till stöd för att återskapa principnycklar för auktorisering.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1612">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f9e89-1613">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f9e89-1613">Az.Network</span></span>
* <span data-ttu-id="f9e89-1614">”RoutingPreference” har lagts till i offentliga IP-taggar</span><span class="sxs-lookup"><span data-stu-id="f9e89-1614">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="f9e89-1615">Förbättra exempel för referensdokumentation om ”Get-AzNetworkServiceTag”</span><span class="sxs-lookup"><span data-stu-id="f9e89-1615">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f9e89-1616">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f9e89-1616">Az.PolicyInsights</span></span>
* <span data-ttu-id="f9e89-1617">Åtgärda problem med null-referens i Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="f9e89-1617">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="f9e89-1618">Mer information här: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="f9e89-1618">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f9e89-1619">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f9e89-1619">Az.OperationalInsights</span></span>
* <span data-ttu-id="f9e89-1620">Modellen för CustomLog-datakälla som returneras i Get-AzOperationalInsightsDataSource har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="f9e89-1620">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f9e89-1621">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f9e89-1621">Az.RecoveryServices</span></span>
* <span data-ttu-id="f9e89-1622">Kommandot get-policy för IaaSVM:er har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="f9e89-1622">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="f9e89-1623">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f9e89-1623">Az.Resources</span></span>
    - <span data-ttu-id="f9e89-1624">Korrigera hjälptext för den översta parametern i Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="f9e89-1624">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="f9e89-1625">Lägg till växlingsstöd på klientsidan för Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="f9e89-1625">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="f9e89-1626">Lägg till nya parametrar för Set-AzPolicyAssignment, -PolicyParameters och -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="f9e89-1626">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="f9e89-1627">En mängd dokument- och exempeluppdateringar för Policy-cmdletar</span><span class="sxs-lookup"><span data-stu-id="f9e89-1627">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="f9e89-1628">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f9e89-1628">Az.ServiceBus</span></span>
* <span data-ttu-id="f9e89-1629">Korrigering av problem #4938 – New-AzureRmServiceBusQueue returnerar BadRequest vid konfiguration av MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="f9e89-1629">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="f9e89-1630">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f9e89-1630">Az.Sql</span></span>
* <span data-ttu-id="f9e89-1631">Lägg till cmdletar för instansredundansgrupper från förhandsversion till offentlig version</span><span class="sxs-lookup"><span data-stu-id="f9e89-1631">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="f9e89-1632">Stöd för granskning för Azure SQL Server\Database med nya cmdletar.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1632">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="f9e89-1633">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="f9e89-1633">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="f9e89-1634">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="f9e89-1634">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="f9e89-1635">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="f9e89-1635">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="f9e89-1636">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="f9e89-1636">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="f9e89-1637">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="f9e89-1637">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="f9e89-1638">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="f9e89-1638">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="f9e89-1639">Ta bort begränsningar för e-post från inställningarna för sårbarhetsbedömning</span><span class="sxs-lookup"><span data-stu-id="f9e89-1639">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f9e89-1640">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f9e89-1640">Az.Storage</span></span>
* <span data-ttu-id="f9e89-1641">Ändra två parametrar ”-IndexDocument” och ”-ErrorDocument404Path” från ”krävs” till ”valfri” i cmdlet:</span><span class="sxs-lookup"><span data-stu-id="f9e89-1641">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="f9e89-1642">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="f9e89-1642">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="f9e89-1643">Uppdatera hjälpen för Get-AzStorageBlobContent genom att lägga till ett exempel</span><span class="sxs-lookup"><span data-stu-id="f9e89-1643">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="f9e89-1644">Visa mer felinformation när cmdleten misslyckas med StorageException</span><span class="sxs-lookup"><span data-stu-id="f9e89-1644">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="f9e89-1645">Stöd för att skapa eller uppdatera lagringskonto med Azure Files AAD DS-autentisering</span><span class="sxs-lookup"><span data-stu-id="f9e89-1645">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="f9e89-1646">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f9e89-1646">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="f9e89-1647">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f9e89-1647">Set-AzStorageAccount</span></span>
* <span data-ttu-id="f9e89-1648">Stöd för att lista eller stänga filreferenser för en filresurs, filkatalog eller en fil</span><span class="sxs-lookup"><span data-stu-id="f9e89-1648">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="f9e89-1649">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="f9e89-1649">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="f9e89-1650">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="f9e89-1650">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="f9e89-1651">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="f9e89-1651">Az.StorageSync</span></span>
* <span data-ttu-id="f9e89-1652">Den här modulen ingår nu som en del av `Az`-sammanslagningsmodulen</span><span class="sxs-lookup"><span data-stu-id="f9e89-1652">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="f9e89-1653">2.3.2 – juni 2019</span><span class="sxs-lookup"><span data-stu-id="f9e89-1653">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f9e89-1654">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f9e89-1654">Az.Accounts</span></span>
* <span data-ttu-id="f9e89-1655">Åtgärda bugg med felaktiga webbadresser som i vissa fall användes för Functions-anrop</span><span class="sxs-lookup"><span data-stu-id="f9e89-1655">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="f9e89-1656">Mer information här: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="f9e89-1656">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="f9e89-1657">Åtgärda problem med alias från AzureRM i Az-cmdletar</span><span class="sxs-lookup"><span data-stu-id="f9e89-1657">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="f9e89-1658">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="f9e89-1658">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="f9e89-1659">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="f9e89-1659">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f9e89-1660">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f9e89-1660">Az.Compute</span></span>
* <span data-ttu-id="f9e89-1661">Parameteruppsättningarna New-AzVm och New-AzVmss accepterar nu parametern ”ProximityPlacementGroup”.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1661">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="f9e89-1662">Stavfel i referensdokumentationen för ”New-AzVM” har korrigerats</span><span class="sxs-lookup"><span data-stu-id="f9e89-1662">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="f9e89-1663">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="f9e89-1663">Az.Dns</span></span>
* <span data-ttu-id="f9e89-1664">Stavfel i hjälpexempel för ”Set-AzDnsZone” har korrigerats.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1664">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="f9e89-1665">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="f9e89-1665">Az.EventGrid</span></span>
* <span data-ttu-id="f9e89-1666">Har uppdaterats för att använda API-versionen 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1666">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="f9e89-1667">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="f9e89-1667">New cmdlets:</span></span>
    - <span data-ttu-id="f9e89-1668">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="f9e89-1668">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="f9e89-1669">Skapar en ny Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1669">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="f9e89-1670">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="f9e89-1670">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="f9e89-1671">Hämtar information om en Event Grid-domän eller hämtar en lista med alla Event Grid-domäner i den aktuella Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1671">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="f9e89-1672">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="f9e89-1672">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="f9e89-1673">Tar bort en Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1673">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="f9e89-1674">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="f9e89-1674">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="f9e89-1675">Återskapar nyckeln för delad åtkomst för en Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1675">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="f9e89-1676">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="f9e89-1676">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="f9e89-1677">Hämtar de nycklar för delad åtkomst som används för att publicera händelser till en Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1677">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="f9e89-1678">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="f9e89-1678">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="f9e89-1679">Skapar ett nytt Azure Event Grid-domänämne.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1679">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="f9e89-1680">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="f9e89-1680">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="f9e89-1681">Hämtar information om ett Event Grid-domänämne eller hämtar en lista med alla Event Grid-domänämnen under en specifik Event Grid-domän i nuvarande Azure</span><span class="sxs-lookup"><span data-stu-id="f9e89-1681">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="f9e89-1682">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="f9e89-1682">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="f9e89-1683">Tar bort ett befintligt Azure Event Grid-domänämne.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1683">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="f9e89-1684">Uppdaterade cmdletar:</span><span class="sxs-lookup"><span data-stu-id="f9e89-1684">Updated cmdlets:</span></span>
    - <span data-ttu-id="f9e89-1685">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="f9e89-1685">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="f9e89-1686">Lägg till nya obligatoriska parametrar för att stödja piping för den nya Event Grid-domänen och Event Grid-domänämnet för att göra det möjligt att skapa nya händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1686">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="f9e89-1687">Lägg till nya obligatoriska parametrar för att ange det nya Event Grid-domännamnet och/eller namnet på Event Grid-domänämnet för att göra det möjligt att skapa nya händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1687">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="f9e89-1688">Lägg till ny parameteruppsättningar för domäner och domänämnen för att göra det möjligt att återanvända befintliga parametrar (t.ex. EndPointType, SubjectBeginsWith osv).</span><span class="sxs-lookup"><span data-stu-id="f9e89-1688">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="f9e89-1689">Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="f9e89-1689">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="f9e89-1690">Förfallodatum för händelseprenumeration</span><span class="sxs-lookup"><span data-stu-id="f9e89-1690">Event subscription expiration date,</span></span>
            - <span data-ttu-id="f9e89-1691">Avancerade filterparametrar.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1691">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="f9e89-1692">Lägg till ny uppräkning för servicebusqueue som mål.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1692">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="f9e89-1693">Tillåt inte användning av ”Alla” i alternativet -IncludedEventType och ersätt det med</span><span class="sxs-lookup"><span data-stu-id="f9e89-1693">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="f9e89-1694">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="f9e89-1694">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="f9e89-1695">Lägg till ny valfria parametrar (Top, ODataQuery och NextLink) för att stödja sidnumrering och filtrering av resultat.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1695">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="f9e89-1696">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="f9e89-1696">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="f9e89-1697">Lägg till nya obligatoriska parametrar för att stödja piping för en Event Grid-domän och Event Grid-domänämnen för att göra det möjligt att ta bort befintliga händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1697">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="f9e89-1698">Lägg till nya obligatoriska parametrar för att ange Event Grid-domännamnet och/eller namnet på Event Grid-domänämnet för att göra det möjligt att ta bort befintliga händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1698">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="f9e89-1699">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f9e89-1699">Az.FrontDoor</span></span>
* <span data-ttu-id="f9e89-1700">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="f9e89-1700">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="f9e89-1701">Lägg till stöd för transformeringar och nytt värde för automatisk komplettering för operatorer (RegEx)</span><span class="sxs-lookup"><span data-stu-id="f9e89-1701">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="f9e89-1702">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="f9e89-1702">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="f9e89-1703">Lägg till nya värden för automatisk komplettering</span><span class="sxs-lookup"><span data-stu-id="f9e89-1703">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f9e89-1704">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f9e89-1704">Az.Network</span></span>
* <span data-ttu-id="f9e89-1705">Lägg till stöd för resurs för virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="f9e89-1705">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="f9e89-1706">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="f9e89-1706">New cmdlets</span></span>
        - <span data-ttu-id="f9e89-1707">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="f9e89-1707">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="f9e89-1708">Lägg till AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="f9e89-1708">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="f9e89-1709">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="f9e89-1709">New cmdlets</span></span>
        - <span data-ttu-id="f9e89-1710">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="f9e89-1710">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="f9e89-1711">Lägg till PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f9e89-1711">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="f9e89-1712">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="f9e89-1712">New cmdlets</span></span>
        - <span data-ttu-id="f9e89-1713">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f9e89-1713">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="f9e89-1714">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f9e89-1714">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="f9e89-1715">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f9e89-1715">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="f9e89-1716">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="f9e89-1716">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="f9e89-1717">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f9e89-1717">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="f9e89-1718">Lägg till PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f9e89-1718">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="f9e89-1719">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="f9e89-1719">New cmdlets</span></span>
        - <span data-ttu-id="f9e89-1720">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f9e89-1720">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="f9e89-1721">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f9e89-1721">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="f9e89-1722">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f9e89-1722">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="f9e89-1723">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="f9e89-1723">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="f9e89-1724">Nedanstående kommandon för funktionen har uppdaterats: Flaggan UseLocalAzureIpAddress på VpnConnection</span><span class="sxs-lookup"><span data-stu-id="f9e89-1724">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="f9e89-1725">New-AzVpnConnection har uppdaterats: Den valfria parametern -UseLocalAzureIpAddress har lagts till för att visa att en lokal IP-adress i Azure ska användas som källadress när anslutningen initieras.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1725">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="f9e89-1726">Set-AzVpnConnection har uppdaterats: Den valfria parametern -UseLocalAzureIpAddress har lagts till för att visa att en lokal IP-adress i Azure ska användas som källadress när anslutningen initieras.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1726">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="f9e89-1727">Det skrivskyddade fältet PeeredConnections har lagts till i ExpressRoute-peering.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1727">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="f9e89-1728">Det skrivskyddade fältet GlobalReachEnabled har lagts till i ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1728">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="f9e89-1729">Ett attribut för icke-bakåtkompatibla ändringar har lagts till för att lyfta fram utfasning av fältet AllowGlobalReach i modellen ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f9e89-1729">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="f9e89-1730">Problem 8756 har åtgärdats: Fel vid användning av TargetListenerID med AzApplicationGatewayRedirectConfiguration-cmdletar</span><span class="sxs-lookup"><span data-stu-id="f9e89-1730">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="f9e89-1731">En bugg i New-AzApplicationGatewayPathRuleConfig som gjorde att regeluppsättningen för att återskapa inte kunde anges har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1731">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="f9e89-1732">Visningen av VirtualNetworkTaps i NetworkInterfaceIpConfiguration har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="f9e89-1732">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="f9e89-1733">Cortex Get-cmdletar för att visa en lista med alla delar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="f9e89-1733">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="f9e89-1734">Funktionen för att skapa VirtualHub-referenser för ExpressRouteGateways och VpnGateway har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="f9e89-1734">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="f9e89-1735">Stöd för tillgänglighetszoner i AzureFirewall och NatGateway har lagts till</span><span class="sxs-lookup"><span data-stu-id="f9e89-1735">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="f9e89-1736">Cmdleten Get-AzNetworkServiceTag har lagts till</span><span class="sxs-lookup"><span data-stu-id="f9e89-1736">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="f9e89-1737">Lägg till stöd för flera offentliga IP-adresser för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="f9e89-1737">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="f9e89-1738">Cmdleten New-AzFirewall har uppdaterats:</span><span class="sxs-lookup"><span data-stu-id="f9e89-1738">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="f9e89-1739">Parametern -PublicIpAddress som accepterar ett eller flera offentliga IP-adressobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="f9e89-1739">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="f9e89-1740">Parametern -VirtualNetwork som accepterar ett virtuellt nätverksobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="f9e89-1740">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="f9e89-1741">Metoderna AddPublicIpAddress och RemovePublicIpAddress har lagts till på brandväggsobjekt – dessa accepterar ett offentligt IP-adressobjekt som indata</span><span class="sxs-lookup"><span data-stu-id="f9e89-1741">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="f9e89-1742">Inaktuella parametrar -PublicIpName och -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="f9e89-1742">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="f9e89-1743">Nedanstående kommandon för funktionen har uppdaterats: Ange autentiseringsalternativ för VpnClient AAD till resurser för virtuella nätverksgatewayer.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1743">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="f9e89-1744">New-AzVirtualNetworkGateway har uppdaterats: De valfria parametrarna AadTenantUri, AadAudienceId och AadIssuerUri för att ange VpnClient AAD-autentiseringsalternativ på en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1744">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="f9e89-1745">Set-AzVirtualNetworkGateway har uppdaterats: De valfria parametrarna AadTenantUri, AadAudienceId och AadIssuerUri för att ange VpnClient AAD-autentiseringsalternativ på en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1745">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="f9e89-1746">Set-AzVirtualNetworkGateway har uppdaterats: Den valfria växelparametern RemoveAadAuthentication som tar bort VpnClient AAD-autentiseringsalternativ från en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1746">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f9e89-1747">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f9e89-1747">Az.OperationalInsights</span></span>
* <span data-ttu-id="f9e89-1748">Aktivera prisnivån **pergb2018** i kommandot ”New-AzureRmOperationalInsightsWorkspace”</span><span class="sxs-lookup"><span data-stu-id="f9e89-1748">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="f9e89-1749">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f9e89-1749">Az.Resources</span></span>
* <span data-ttu-id="f9e89-1750">Stöd för ytterligare alternativ för att exportera en mall</span><span class="sxs-lookup"><span data-stu-id="f9e89-1750">Support for additional Template Export options</span></span>
    - <span data-ttu-id="f9e89-1751">Lägg till parametern ”-SkipResourceNameParameterization” till Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f9e89-1751">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="f9e89-1752">Lägg till parametern ”-SkipAllParameterization” till Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f9e89-1752">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="f9e89-1753">Lägg till parametern ”-Resource” till Export-AzResourceGroup för exporterad resursfiltrering</span><span class="sxs-lookup"><span data-stu-id="f9e89-1753">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f9e89-1754">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f9e89-1754">Az.ServiceFabric</span></span>
* <span data-ttu-id="f9e89-1755">Åtgärda att fel tumavtryck används vid tilläggning av certifikat i ByExistingKeyVault i vissa fall</span><span class="sxs-lookup"><span data-stu-id="f9e89-1755">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="f9e89-1756">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f9e89-1756">Az.Sql</span></span>
* <span data-ttu-id="f9e89-1757">Åtgärda suffix för lagringsslutpunkt i Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="f9e89-1757">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="f9e89-1758">Åtgärda att aktivering av Advanced Data Security åsidosätter Advanced Threat Protection-princip</span><span class="sxs-lookup"><span data-stu-id="f9e89-1758">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="f9e89-1759">Nya cmdletar för Management.Sql som gör att kunderna kan lägga till nycklar för transparent datakryptering (TDE) och ange TDE-skydd för hanterade instanser</span><span class="sxs-lookup"><span data-stu-id="f9e89-1759">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="f9e89-1760">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="f9e89-1760">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="f9e89-1761">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="f9e89-1761">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="f9e89-1762">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="f9e89-1762">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="f9e89-1763">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="f9e89-1763">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="f9e89-1764">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="f9e89-1764">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f9e89-1765">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f9e89-1765">Az.Storage</span></span>
* <span data-ttu-id="f9e89-1766">Stöd för typerna FileStorage och SkuName Premium_ZRS när lagringskonton skapas</span><span class="sxs-lookup"><span data-stu-id="f9e89-1766">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="f9e89-1767">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f9e89-1767">New-AzStorageAccount</span></span>
* <span data-ttu-id="f9e89-1768">Beskrivningen av cmdleten för bloboföränderlighet har förtydligats</span><span class="sxs-lookup"><span data-stu-id="f9e89-1768">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="f9e89-1769">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="f9e89-1769">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f9e89-1770">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f9e89-1770">Az.Websites</span></span>
* <span data-ttu-id="f9e89-1771">Optimerar Get-AzWebAppCertificate för att filtrera efter resursgrupp på servern i stället för klienten</span><span class="sxs-lookup"><span data-stu-id="f9e89-1771">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="f9e89-1772">Lägger till växlingsparametern -UseDisasterRecovery till Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="f9e89-1772">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="f9e89-1773">2.2.0 – juni 2019</span><span class="sxs-lookup"><span data-stu-id="f9e89-1773">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="f9e89-1774">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f9e89-1774">Az.Cdn</span></span>
* <span data-ttu-id="f9e89-1775">Uppdaterade cmdletar för att ge stöd för rulesEngine-funktion baserat på API-version 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1775">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f9e89-1776">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f9e89-1776">Az.Compute</span></span>
* <span data-ttu-id="f9e89-1777">Lade till parameter `NoWait` som startar åtgärden och returnerar omedelbart, innan åtgärden har slutförts.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1777">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="f9e89-1778">Uppdaterade cmdletar:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="f9e89-1778">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f9e89-1779">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f9e89-1779">Az.EventHub</span></span>
* <span data-ttu-id="f9e89-1780">Korrigering för #9231 – Get-AzEventHubNamespace returnerar inga taggar</span><span class="sxs-lookup"><span data-stu-id="f9e89-1780">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="f9e89-1781">Korrigering för #9230 – Get-AzEventHubNamespace returnerar ResourceGroup istället för ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9e89-1781">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f9e89-1782">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f9e89-1782">Az.Network</span></span>
* <span data-ttu-id="f9e89-1783">Uppdatera ResourceId och InputObject för NAT-gateway</span><span class="sxs-lookup"><span data-stu-id="f9e89-1783">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="f9e89-1784">Lägg till alias för ResourceId och InputObject</span><span class="sxs-lookup"><span data-stu-id="f9e89-1784">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f9e89-1785">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f9e89-1785">Az.PolicyInsights</span></span>
* <span data-ttu-id="f9e89-1786">Åtgärda Null-referensproblem i Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="f9e89-1786">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f9e89-1787">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f9e89-1787">Az.RecoveryServices</span></span>
* <span data-ttu-id="f9e89-1788">Minsta kvarhållning för IaaSVM-policy i dagar ändrat till 7 från 1</span><span class="sxs-lookup"><span data-stu-id="f9e89-1788">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="f9e89-1789">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f9e89-1789">Az.ServiceBus</span></span>
* <span data-ttu-id="f9e89-1790">Korrigering för ärende #9182 – Get-AzServiceBusNamespace returnerar ResourceGroup istället för ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9e89-1790">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f9e89-1791">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f9e89-1791">Az.ServiceFabric</span></span>
* <span data-ttu-id="f9e89-1792">Åtgärda stavfel i felmeddelandet för Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="f9e89-1792">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="f9e89-1793">Åtgärda saknat tecken i Service Fabric-kommandorader</span><span class="sxs-lookup"><span data-stu-id="f9e89-1793">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="f9e89-1794">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f9e89-1794">Az.Sql</span></span>
* <span data-ttu-id="f9e89-1795">Lägg till parametern DnsZonePartner för New-AzureSqlInstance-cmdlet för att ge stöd för AutoDr för hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1795">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="f9e89-1796">Avvecklar cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="f9e89-1796">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="f9e89-1797">Döp om cmdletar för hotidentifiering till Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="f9e89-1797">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="f9e89-1798">Parametrarna New-AzSqlInstance -StorageSizeInGB och -LicenseType är nu valfria.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1798">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f9e89-1799">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f9e89-1799">Az.Websites</span></span>
* <span data-ttu-id="f9e89-1800">åtgärdar problemet där användningen av Set-AzWebApp och Set-AzWebAppSlot med -WebApp-egenskap tog bort taggarna</span><span class="sxs-lookup"><span data-stu-id="f9e89-1800">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="f9e89-1801">2.1.0 – maj 2019</span><span class="sxs-lookup"><span data-stu-id="f9e89-1801">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="f9e89-1802">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f9e89-1802">Az.ApiManagement</span></span>
* <span data-ttu-id="f9e89-1803">Skapade nya cmdletar för att hantera diagnostik för global- och API-omfång</span><span class="sxs-lookup"><span data-stu-id="f9e89-1803">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="f9e89-1804">**Get-AzApiManagementDiagnostic** – Skaffa diagnostik konfigurerad för global- eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="f9e89-1804">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="f9e89-1805">**New-AzApiManagementDiagnostic** – Skapa ny diagnostik för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="f9e89-1805">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="f9e89-1806">**New-AzApiManagementHttpMessageDiagnostic** – Skapa diagnostikinställning om vilka rubriker som ska loggas och storleken på brödtextbyte</span><span class="sxs-lookup"><span data-stu-id="f9e89-1806">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="f9e89-1807">**New-AzApiManagementPipelineDiagnosticSetting** – Skapa diagnostikinställningar för inkommande/utgående HTTP-meddelanden till gatewayen.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1807">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="f9e89-1808">**New-AzApiManagementSamplingSetting** – Skapa samplinginställningar för begäranden/svar för en diagnostik</span><span class="sxs-lookup"><span data-stu-id="f9e89-1808">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="f9e89-1809">**Remove-AzApiManagementDiagnostic** – Ta bort en diagnostikenhet för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="f9e89-1809">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="f9e89-1810">**Set-AzApiManagementDiagnostic** – Uppdatera en diagnostikenhet för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="f9e89-1810">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="f9e89-1811">Skapade nya cmdletar för hantering av cacheminne i ApiManagement-tjänsten</span><span class="sxs-lookup"><span data-stu-id="f9e89-1811">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="f9e89-1812">**Get-AzApiManagementCache** – Hämta information om cacheminnet som anges av identifierare eller alla cacheminnen</span><span class="sxs-lookup"><span data-stu-id="f9e89-1812">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="f9e89-1813">**New-AzApiManagementCache** – Skapa ett nytt default-cacheminne eller cacheminne i en viss Azure-region</span><span class="sxs-lookup"><span data-stu-id="f9e89-1813">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="f9e89-1814">**Remove-AzApiManagementCache** – Ta bort ett cacheminne</span><span class="sxs-lookup"><span data-stu-id="f9e89-1814">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="f9e89-1815">**Remove-AzApiManagementCache** – Ta bort ett cacheminne</span><span class="sxs-lookup"><span data-stu-id="f9e89-1815">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="f9e89-1816">Skapade nya cmdletar för hantering av API-schema</span><span class="sxs-lookup"><span data-stu-id="f9e89-1816">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="f9e89-1817">**New-AzApiManagementSchema** – Skapa ett nytt schema för ett API</span><span class="sxs-lookup"><span data-stu-id="f9e89-1817">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="f9e89-1818">**Get-AzApiManagementSchema** – Hämta de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="f9e89-1818">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="f9e89-1819">**Remove-AzApiManagementSchema** – Ta bort de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="f9e89-1819">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="f9e89-1820">**Set-AzApiManagementSchema** – Uppdatera de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="f9e89-1820">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="f9e89-1821">Skapa ny cmdlet för att generera en användartoken.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1821">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="f9e89-1822">**New-AzApiManagementUserToken** – Skapa en ny användartoken som enligt standardinställning är giltig i 8 timmar. Token för GIT-användaren kan skapas med den här cmdleten./</span><span class="sxs-lookup"><span data-stu-id="f9e89-1822">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="f9e89-1823">Skapade en ny cmdlet för att hämta nätverksstatus</span><span class="sxs-lookup"><span data-stu-id="f9e89-1823">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="f9e89-1824">**Get-AzApiManagementNetworkStatus** – Hämta nätverksstatusanslutningen för resurserna som API Management-tjänsten är beroende av.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1824">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="f9e89-1825">Det här är användbart när du distribuerar ApiManagement-tjänsten i ett virtuellt nätverk och validerar om något beroende är brutet.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1825">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="f9e89-1826">Uppdaterade cmdlet **New-AzApiManagement** för att hantera ApiManagement-tjänsten</span><span class="sxs-lookup"><span data-stu-id="f9e89-1826">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="f9e89-1827">Lade till stöd för den nya SKU:n Consumption</span><span class="sxs-lookup"><span data-stu-id="f9e89-1827">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="f9e89-1828">Aktiverade stöd för att slå på flaggan EnableClientCertificate för SKU:n Consumption</span><span class="sxs-lookup"><span data-stu-id="f9e89-1828">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="f9e89-1829">Den nya cmdleten **New-AzApiManagementSslSetting** gör det möjligt att ställa in TLS/SSL-inställningen på ”Backend” och ”Frontend” (serverdel och klientdel).</span><span class="sxs-lookup"><span data-stu-id="f9e89-1829">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="f9e89-1830">Det här kan också användas till att konfigurera chiffer som 3DES och ServerProtocols som Http2 för Frontend för en ApiManagement-tjänst.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1830">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="f9e89-1831">Stöd har lagts till för att konfigurera värdnamnet DeveloperPortal på ApiManagement-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1831">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="f9e89-1832">Uppdaterade cmdletar **Get-AzApiManagementSsoToken** för att ta PsApiManagement-objekt som indata</span><span class="sxs-lookup"><span data-stu-id="f9e89-1832">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="f9e89-1833">Uppdaterad cmdleten för att visa infogade felmeddelanden</span><span class="sxs-lookup"><span data-stu-id="f9e89-1833">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="f9e89-1834">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Felkod: Felmeddelande av typen ValidationError: Ett eller flera fält innehåller felaktiga värden: Felinformation:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="f9e89-1834">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="f9e89-1835">Uppdaterade cmdlet **Export-AzApiManagementApi** för att exportera API:er i OpenApi 3.0-format</span><span class="sxs-lookup"><span data-stu-id="f9e89-1835">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="f9e89-1836">Uppdaterade cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="f9e89-1836">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="f9e89-1837">Importera API från dokumentspecifikationen OpenApi 3.0</span><span class="sxs-lookup"><span data-stu-id="f9e89-1837">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="f9e89-1838">Om du vill åsidosätta egenskapen PsApiManagementSchema specificerad i ett dokument (Swagger, Wadl, Wsdl, OpenApi).</span><span class="sxs-lookup"><span data-stu-id="f9e89-1838">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="f9e89-1839">Åsidosätta egenskapen ServiceUrl som specificeras i ett dokument.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1839">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="f9e89-1840">Uppdaterade cmdlet **Get-AzApiManagementPolicy** för att returnera policy i undantaget format av typen icke-XML med rawxml</span><span class="sxs-lookup"><span data-stu-id="f9e89-1840">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="f9e89-1841">Uppdaterade cmdlet **Set-AzApiManagementPolicy** för att godkänna policy i undantaget format av typen icke-XML med rawxml och XML undantaget med xml</span><span class="sxs-lookup"><span data-stu-id="f9e89-1841">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="f9e89-1842">Uppdaterad cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="f9e89-1842">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="f9e89-1843">Konfigurera API med OpenId auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1843">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="f9e89-1844">Skapa ett API i ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="f9e89-1844">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="f9e89-1845">Klona ett API med SourceApiId och SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1845">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="f9e89-1846">Möjlighet att konfigurera SubscriptionRequired i API-omfattningen.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1846">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="f9e89-1847">Uppdaterad cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="f9e89-1847">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="f9e89-1848">Konfigurera API med OpenId auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1848">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="f9e89-1849">Uppdatera ett API till ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="f9e89-1849">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="f9e89-1850">Möjlighet att konfigurera SubscriptionRequired i API-omfattningen.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1850">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="f9e89-1851">Uppdaterad cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="f9e89-1851">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="f9e89-1852">Klona en befintlig version med hjälp av SourceApiRevision (kopiera taggar, produkter, åtgärder och principer).</span><span class="sxs-lookup"><span data-stu-id="f9e89-1852">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="f9e89-1853">Den nya revisionen antar ApiId från den överordnade instansen.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1853">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="f9e89-1854">Tillhandahålla ApiRevisionDescription</span><span class="sxs-lookup"><span data-stu-id="f9e89-1854">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="f9e89-1855">Åsidosätta ServiceUrl vid kloning av ett API.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1855">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="f9e89-1856">Uppdaterad cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="f9e89-1856">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="f9e89-1857">Konfigurera AAD eller AADB2C med en Authority</span><span class="sxs-lookup"><span data-stu-id="f9e89-1857">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="f9e89-1858">Konfigurera SignupPolicy, SigninPolicy, ProfileEditingPolicy och PasswordResetPolicy</span><span class="sxs-lookup"><span data-stu-id="f9e89-1858">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="f9e89-1859">Uppdaterad cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="f9e89-1859">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="f9e89-1860">Kompensera för ny SubscriptonModel med Scope och UserId</span><span class="sxs-lookup"><span data-stu-id="f9e89-1860">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="f9e89-1861">Kompensera för gammal prenumerationsmodell med ProductId och UserId</span><span class="sxs-lookup"><span data-stu-id="f9e89-1861">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="f9e89-1862">Lägg till funktion för att aktivera AllowTracing på prenumerationsnivå.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1862">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="f9e89-1863">Uppdaterad cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="f9e89-1863">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="f9e89-1864">Kompensera för ny SubscriptonModel med Scope och UserId</span><span class="sxs-lookup"><span data-stu-id="f9e89-1864">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="f9e89-1865">Kompensera för gammal prenumerationsmodell med ProductId och UserId</span><span class="sxs-lookup"><span data-stu-id="f9e89-1865">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="f9e89-1866">Lägg till funktion för att aktivera AllowTracing på prenumerationsnivå.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1866">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="f9e89-1867">Uppdaterade följande cmdletar för att acceptera ResourceId som indata</span><span class="sxs-lookup"><span data-stu-id="f9e89-1867">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="f9e89-1868">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f9e89-1868">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="f9e89-1869">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="f9e89-1869">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="f9e89-1870">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="f9e89-1870">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="f9e89-1871">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="f9e89-1871">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="f9e89-1872">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="f9e89-1872">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="f9e89-1873">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="f9e89-1873">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="f9e89-1874">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="f9e89-1874">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="f9e89-1875">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="f9e89-1875">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="f9e89-1876">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="f9e89-1876">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="f9e89-1877">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="f9e89-1877">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="f9e89-1878">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="f9e89-1878">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="f9e89-1879">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="f9e89-1879">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f9e89-1880">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f9e89-1880">Az.Automation</span></span>
* <span data-ttu-id="f9e89-1881">Uppdaterade Get-AzAutomationJobOutputRecord för att hantera postvärden av typen JSON och Text.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1881">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="f9e89-1882">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="f9e89-1882">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="f9e89-1883">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="f9e89-1883">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="f9e89-1884">Ändrade beteende för Start-AzAutomationDscCompilationJob till att bara starta jobbet istället för att vänta på slutförandet.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1884">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="f9e89-1885">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="f9e89-1885">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="f9e89-1886">Korrigering för Get-AzAutomationDscNode när using -Name returnerar alla noder.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1886">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="f9e89-1887">Nu returnerar den endast den matchande noden.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1887">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f9e89-1888">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f9e89-1888">Az.Compute</span></span>
* <span data-ttu-id="f9e89-1889">Lägg till parametrarna ProtectFromScaleIn och ProtectFromScaleSetAction i cmdleten Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1889">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="f9e89-1890">Nu är standardinställningen att vimpelparametern New-AzVM använder en tillgänglig plats om USA, östra inte stöds</span><span class="sxs-lookup"><span data-stu-id="f9e89-1890">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f9e89-1891">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f9e89-1891">Az.DataLakeStore</span></span>
* <span data-ttu-id="f9e89-1892">Uppdatera ADLS-sdk för att använda httpclient, integrera dataplanstestning med Azure-ramverk</span><span class="sxs-lookup"><span data-stu-id="f9e89-1892">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f9e89-1893">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f9e89-1893">Az.Monitor</span></span>
* <span data-ttu-id="f9e89-1894">Korrigera felaktiga parameternamn i hjälpexempel</span><span class="sxs-lookup"><span data-stu-id="f9e89-1894">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f9e89-1895">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f9e89-1895">Az.Network</span></span>
* <span data-ttu-id="f9e89-1896">Lägg till flaggan DisableBgpRoutePropagation i utdata för effektiv routningstabell</span><span class="sxs-lookup"><span data-stu-id="f9e89-1896">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="f9e89-1897">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="f9e89-1897">Updated cmdlet:</span></span>
        - <span data-ttu-id="f9e89-1898">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="f9e89-1898">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="f9e89-1899">Åtgärda dubbelstreck i dokumentationen New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f9e89-1899">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="f9e89-1900">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f9e89-1900">Az.Resources</span></span>
* <span data-ttu-id="f9e89-1901">Lägg till ny cmdlet Get-AzureRmDenyAssignment för att hämta tilldelningsnekanden</span><span class="sxs-lookup"><span data-stu-id="f9e89-1901">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="f9e89-1902">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f9e89-1902">Az.Sql</span></span>
* <span data-ttu-id="f9e89-1903">Döp om Advanced Threat Protection-cmdletar för Advanced Data Security och aktivera Vulnerability Assessment som standard</span><span class="sxs-lookup"><span data-stu-id="f9e89-1903">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="f9e89-1904">2.0.0 – maj 2019</span><span class="sxs-lookup"><span data-stu-id="f9e89-1904">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f9e89-1905">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f9e89-1905">Az.Accounts</span></span>
* <span data-ttu-id="f9e89-1906">Uppdatera autentiseringsbiblioteket för att åtgärda ADFS-problem med autentisering av användarnamn/lösenord</span><span class="sxs-lookup"><span data-stu-id="f9e89-1906">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f9e89-1907">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f9e89-1907">Az.CognitiveServices</span></span>
* <span data-ttu-id="f9e89-1908">Visa endast Bing-ansvarsfriskrivning för Bing-sökningstjänster.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1908">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="f9e89-1909">Förbättra felmeddelande när det inte går att skapa konton.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1909">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f9e89-1910">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f9e89-1910">Az.Compute</span></span>
* <span data-ttu-id="f9e89-1911">Funktion för närhetsplaceringsgrupper.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1911">Proximity placement group feature.</span></span>
    - <span data-ttu-id="f9e89-1912">Följande nya cmdletar har lagts till:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="f9e89-1912">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="f9e89-1913">Den nya parametern ProximityPlacementGroupId har lagts till i följande cmdletar:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="f9e89-1913">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="f9e89-1914">Parametern StorageAccountType har lagts till i New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1914">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="f9e89-1915">TargetRegion för New-AzGalleryImageVersion kan innehålla StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1915">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="f9e89-1916">Växlingsparametern SkipShutdown har lagts till i Stop-AzVM och Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f9e89-1916">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="f9e89-1917">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="f9e89-1917">Breaking changes</span></span>
    - <span data-ttu-id="f9e89-1918">Set-AzVMBootDiagnostics har ändrats till Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1918">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="f9e89-1919">Export-AzLogAnalyticThrottledRequests har ändrats till Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1919">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="f9e89-1920">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="f9e89-1920">Az.DeploymentManager</span></span>
* <span data-ttu-id="f9e89-1921">De första allmänt tillgängliga versionerna av cmdletar för Distributionshanteraren i Azure</span><span class="sxs-lookup"><span data-stu-id="f9e89-1921">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="f9e89-1922">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="f9e89-1922">Az.Dns</span></span>
* <span data-ttu-id="f9e89-1923">Automatisk delegering av DNS för NameServer</span><span class="sxs-lookup"><span data-stu-id="f9e89-1923">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="f9e89-1924">Det överordnade zonnamnet kan användas som ytterligare valfri parameter i cmdleten för att skapa DNS-zoner.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1924">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="f9e89-1925">Lägger till NS-poster för en nyligen skapad underordnad zon i den överordnade zonen.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1925">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="f9e89-1926">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f9e89-1926">Az.FrontDoor</span></span>
* <span data-ttu-id="f9e89-1927">De första allmänt tillgängliga versionerna av cmdletar för Azure FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f9e89-1927">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="f9e89-1928">Byt namn på WAF-cmdletar så att de omfattar ”Waf”</span><span class="sxs-lookup"><span data-stu-id="f9e89-1928">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="f9e89-1929">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f9e89-1929">Az.HDInsight</span></span>
* <span data-ttu-id="f9e89-1930">Två cmdletar har tagits bort:</span><span class="sxs-lookup"><span data-stu-id="f9e89-1930">Removed two cmdlets:</span></span>
    - <span data-ttu-id="f9e89-1931">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="f9e89-1931">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="f9e89-1932">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="f9e89-1932">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="f9e89-1933">En ny cmdlet har lagts till, Set-AzHDInsightGatewayCredential, som ersätter Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="f9e89-1933">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="f9e89-1934">Uppdatera cmdleten Get-AzHDInsightJobOutput för att skilja mellan läsarrollen och HDInsight-operatörsrollen:</span><span class="sxs-lookup"><span data-stu-id="f9e89-1934">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="f9e89-1935">Användare med läsarrollen måste uttryckligen ange parametern ”DefaultStorageAccountKey”, annars uppstår fel.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1935">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="f9e89-1936">Användare med HDInsight-operatörsrollen påverkas inte.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1936">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f9e89-1937">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f9e89-1937">Az.Monitor</span></span>
* <span data-ttu-id="f9e89-1938">Nya cmdletar för SQR API (schemalagd frågeregel)</span><span class="sxs-lookup"><span data-stu-id="f9e89-1938">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="f9e89-1939">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="f9e89-1939">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="f9e89-1940">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="f9e89-1940">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="f9e89-1941">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="f9e89-1941">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="f9e89-1942">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="f9e89-1942">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="f9e89-1943">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="f9e89-1943">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="f9e89-1944">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="f9e89-1944">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="f9e89-1945">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="f9e89-1945">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="f9e89-1946">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="f9e89-1946">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="f9e89-1947">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="f9e89-1947">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="f9e89-1948">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="f9e89-1948">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="f9e89-1949">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="f9e89-1949">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="f9e89-1950">[Mer](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information om SQR API</span><span class="sxs-lookup"><span data-stu-id="f9e89-1950">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="f9e89-1951">Az.Monitor.md har uppdaterats för att omfatta cmdletar för måttbaserade aviseringsregler i GenV2 (inte klassiska)</span><span class="sxs-lookup"><span data-stu-id="f9e89-1951">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f9e89-1952">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f9e89-1952">Az.Network</span></span>
* <span data-ttu-id="f9e89-1953">Lägg till stöd för NAT Gateway-resurs</span><span class="sxs-lookup"><span data-stu-id="f9e89-1953">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="f9e89-1954">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="f9e89-1954">New cmdlets</span></span>
        - <span data-ttu-id="f9e89-1955">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="f9e89-1955">New-AzNatGateway</span></span>
        - <span data-ttu-id="f9e89-1956">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="f9e89-1956">Get-AzNatGateway</span></span>
        - <span data-ttu-id="f9e89-1957">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="f9e89-1957">Set-AzNatGateway</span></span>
        - <span data-ttu-id="f9e89-1958">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="f9e89-1958">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="f9e89-1959">Uppdaterade cmdletar</span><span class="sxs-lookup"><span data-stu-id="f9e89-1959">Updated cmdlets</span></span>
        - <span data-ttu-id="f9e89-1960">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="f9e89-1960">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="f9e89-1961">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="f9e89-1961">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="f9e89-1962">Nedanstående kommandon för funktionen har uppdaterats: Ange/ta bort anpassade vägar på Brooklyn Gateway.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1962">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="f9e89-1963">New-AzVirtualNetworkGateway har uppdaterats: Den valfria parametern -CustomRoute har lagts till för att ställa in adressprefix som anpassade vägar för att ange gateway.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1963">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="f9e89-1964">Set-AzVirtualNetworkGateway har uppdaterats: Den valfria parametern -CustomRoute har lagts till för att ange adressprefix som anpassade vägar för att ange gateway.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1964">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f9e89-1965">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f9e89-1965">Az.PolicyInsights</span></span>
* <span data-ttu-id="f9e89-1966">Stöd för att fråga efter information om principutvärdering.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1966">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="f9e89-1967">Lägg till parametern ”-Expand” för Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1967">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="f9e89-1968">Stöd för -Expand PolicyEvaluationDetails.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1968">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f9e89-1969">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f9e89-1969">Az.RecoveryServices</span></span>
* <span data-ttu-id="f9e89-1970">Stöd för att dela prenumeration mellan Azure och Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1970">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="f9e89-1971">Markering av kommande icke-bakåtkompatibla ändringar för Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1971">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="f9e89-1972">Korrigering för återställningsplan och åtgärdsplan i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1972">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="f9e89-1973">Korrigering för mappning av uppdateringsnätverk i Azure Site Recovery för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1973">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="f9e89-1974">Korrigering för instruktioner för uppdateringsskydd i Azure Site Recovery för Azure till Azure för hanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1974">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="f9e89-1975">Andra mindre korrigeringar.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1975">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="f9e89-1976">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="f9e89-1976">Az.Relay</span></span>
* <span data-ttu-id="f9e89-1977">Korrigera stavfel i kundriktade meddelanden</span><span class="sxs-lookup"><span data-stu-id="f9e89-1977">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="f9e89-1978">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f9e89-1978">Az.ServiceBus</span></span>
* <span data-ttu-id="f9e89-1979">Nya cmdletar har lagts till för NetworkRuleSet för namnområden</span><span class="sxs-lookup"><span data-stu-id="f9e89-1979">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f9e89-1980">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f9e89-1980">Az.Storage</span></span>
* <span data-ttu-id="f9e89-1981">Uppgradera till lagringsklientbiblioteket 10.0.1 (namnområdet för alla objekt från detta SDK ändras från ”Microsoft.WindowsAzure.Storage. *till ”Microsoft.Azure.Storage.* ”)</span><span class="sxs-lookup"><span data-stu-id="f9e89-1981">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="f9e89-1982">Uppgradera till Microsoft.Azure.Management.Storage 11.0.0 för att stödja den nya API-versionen 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="f9e89-1982">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="f9e89-1983">Standardlagringskontot i Skapa lagringskonto ändras från ”Storage” till ”StorageV2”</span><span class="sxs-lookup"><span data-stu-id="f9e89-1983">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="f9e89-1984">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f9e89-1984">New-AzStorageAccount</span></span>
* <span data-ttu-id="f9e89-1985">Ändra lagringskontots cmdlet-utdata Sku.Name för att passa med indata-SkuName genom att lägga till ”-”. Till exempel ändras ”StandardLRS” till ”Standard_LRS”</span><span class="sxs-lookup"><span data-stu-id="f9e89-1985">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="f9e89-1986">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f9e89-1986">New-AzStorageAccount</span></span>
    - <span data-ttu-id="f9e89-1987">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f9e89-1987">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="f9e89-1988">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f9e89-1988">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f9e89-1989">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f9e89-1989">Az.Websites</span></span>
* <span data-ttu-id="f9e89-1990">Egenskapen ”typ” konfigureras nu för PSSite-objekt som returneras av Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="f9e89-1990">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="f9e89-1991">Get-AzWebApp\*Metrics och Get-AzAppServicePlanMetrics markeras som inaktuella</span><span class="sxs-lookup"><span data-stu-id="f9e89-1991">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="f9e89-1992">1.8.0 – april 2019</span><span class="sxs-lookup"><span data-stu-id="f9e89-1992">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="f9e89-1993">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="f9e89-1993">Highlights since the last major release</span></span>
* <span data-ttu-id="f9e89-1994">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="f9e89-1994">General availability of `Az` module</span></span>
* <span data-ttu-id="f9e89-1995">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="f9e89-1995">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="f9e89-1996">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="f9e89-1996">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="f9e89-1997">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="f9e89-1997">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="f9e89-1998">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="f9e89-1998">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="f9e89-1999">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="f9e89-1999">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="f9e89-2000">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="f9e89-2000">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f9e89-2001">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f9e89-2001">Az.Accounts</span></span>
* <span data-ttu-id="f9e89-2002">Uppdatera Uninstall-AzureRm för att ta bort moduler i Mac på ett korrekt sätt</span><span class="sxs-lookup"><span data-stu-id="f9e89-2002">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="f9e89-2003">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="f9e89-2003">Az.Batch</span></span>
* <span data-ttu-id="f9e89-2004">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2004">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="f9e89-2005">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f9e89-2005">Az.Cdn</span></span>
* <span data-ttu-id="f9e89-2006">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2006">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f9e89-2007">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f9e89-2007">Az.CognitiveServices</span></span>
* <span data-ttu-id="f9e89-2008">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2008">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f9e89-2009">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f9e89-2009">Az.Compute</span></span>
* <span data-ttu-id="f9e89-2010">Åtgärda problem med AEM-installationen om resurs-ID:n för diskar innehåller resourcegroups i gemener i resurs-ID:n</span><span class="sxs-lookup"><span data-stu-id="f9e89-2010">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="f9e89-2011">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2011">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f9e89-2012">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="f9e89-2012">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f9e89-2013">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f9e89-2013">Az.DataFactory</span></span>
* <span data-ttu-id="f9e89-2014">Lägg till SsisProperties om NodeCount inte är null för hanterad integreringskörning.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2014">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f9e89-2015">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f9e89-2015">Az.DataLakeStore</span></span>
* <span data-ttu-id="f9e89-2016">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2016">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="f9e89-2017">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="f9e89-2017">Az.EventGrid</span></span>
* <span data-ttu-id="f9e89-2018">Hjälptexten för slutpunkten har uppdaterats för att visa att resurser ska skapas innan cmdletarna för att skapa/uppdatera händelseprenumerationer används.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2018">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f9e89-2019">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f9e89-2019">Az.EventHub</span></span>
* <span data-ttu-id="f9e89-2020">Nya cmdletar har lagts till för NetworkRuleSet för namnområden</span><span class="sxs-lookup"><span data-stu-id="f9e89-2020">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="f9e89-2021">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f9e89-2021">Az.HDInsight</span></span>
* <span data-ttu-id="f9e89-2022">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2022">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f9e89-2023">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f9e89-2023">Az.IotHub</span></span>
* <span data-ttu-id="f9e89-2024">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2024">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f9e89-2025">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f9e89-2025">Az.KeyVault</span></span>
* <span data-ttu-id="f9e89-2026">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2026">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f9e89-2027">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="f9e89-2027">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="f9e89-2028">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="f9e89-2028">Az.MachineLearning</span></span>
* <span data-ttu-id="f9e89-2029">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2029">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="f9e89-2030">Az.Media</span><span class="sxs-lookup"><span data-stu-id="f9e89-2030">Az.Media</span></span>
* <span data-ttu-id="f9e89-2031">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2031">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f9e89-2032">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f9e89-2032">Az.Monitor</span></span>
  * <span data-ttu-id="f9e89-2033">Nya cmdletar för måttbaserad aviseringsregel i GenV2 (inte klassisk)</span><span class="sxs-lookup"><span data-stu-id="f9e89-2033">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="f9e89-2034">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="f9e89-2034">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="f9e89-2035">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="f9e89-2035">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="f9e89-2036">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="f9e89-2036">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="f9e89-2037">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="f9e89-2037">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="f9e89-2038">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="f9e89-2038">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="f9e89-2039">Monitor SDK har uppdaterats till version 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="f9e89-2039">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f9e89-2040">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f9e89-2040">Az.Network</span></span>
* <span data-ttu-id="f9e89-2041">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2041">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f9e89-2042">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="f9e89-2042">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="f9e89-2043">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="f9e89-2043">Az.NotificationHubs</span></span>
* <span data-ttu-id="f9e89-2044">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2044">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f9e89-2045">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f9e89-2045">Az.OperationalInsights</span></span>
* <span data-ttu-id="f9e89-2046">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2046">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="f9e89-2047">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="f9e89-2047">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="f9e89-2048">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2048">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f9e89-2049">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f9e89-2049">Az.RecoveryServices</span></span>
* <span data-ttu-id="f9e89-2050">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2050">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f9e89-2051">Tabellformatet för SQL i virtuella Azure-datorer har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="f9e89-2051">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="f9e89-2052">En alternativ metod för att hämta platser i AzureFileShare har lagts till</span><span class="sxs-lookup"><span data-stu-id="f9e89-2052">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="f9e89-2053">ScheduleRunDays i SchedulePolicy-objekt har uppdaterats enligt tidszon</span><span class="sxs-lookup"><span data-stu-id="f9e89-2053">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="f9e89-2054">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="f9e89-2054">Az.RedisCache</span></span>
* <span data-ttu-id="f9e89-2055">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2055">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f9e89-2056">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f9e89-2056">Az.Resources</span></span>
* <span data-ttu-id="f9e89-2057">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="f9e89-2057">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="f9e89-2058">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f9e89-2058">Az.Sql</span></span>
* <span data-ttu-id="f9e89-2059">Ersätt Monitor SDK-beroende med vanlig kod</span><span class="sxs-lookup"><span data-stu-id="f9e89-2059">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="f9e89-2060">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2060">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f9e89-2061">Förbättrad process för klassificering av flera kolumner.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2061">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="f9e89-2062">Inkludera SKU-egenskaper (SKU-namn, serie, kapacitet) i svaret från Get-AzSqlServerServiceObjective och formatera som tabell som standard.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2062">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="f9e89-2063">Möjlighet att använda Get-AzSqlServerServiceObjective efter plats utan att behöva en redan befintlig server i regionen.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2063">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="f9e89-2064">Stöd för tidszonsparametern när hanterade instanser skapas.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2064">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="f9e89-2065">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="f9e89-2065">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f9e89-2066">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f9e89-2066">Az.Websites</span></span>
* <span data-ttu-id="f9e89-2067">åtgärdar Set-AzWebApp och Set-AzWebAppSlot så att de inte tar bort taggar vid körning</span><span class="sxs-lookup"><span data-stu-id="f9e89-2067">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="f9e89-2068">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2068">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f9e89-2069">SDK för WebSites har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2069">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="f9e89-2070">Egenskapen AdminSiteName har tagits bort från PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2070">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="f9e89-2071">1.7.0 – april 2019</span><span class="sxs-lookup"><span data-stu-id="f9e89-2071">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="f9e89-2072">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="f9e89-2072">Highlights since the last major release</span></span>
* <span data-ttu-id="f9e89-2073">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="f9e89-2073">General availability of `Az` module</span></span>
* <span data-ttu-id="f9e89-2074">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="f9e89-2074">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="f9e89-2075">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="f9e89-2075">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="f9e89-2076">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="f9e89-2076">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="f9e89-2077">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="f9e89-2077">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="f9e89-2078">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="f9e89-2078">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="f9e89-2079">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="f9e89-2079">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f9e89-2080">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f9e89-2080">Az.Accounts</span></span>
* <span data-ttu-id="f9e89-2081">Add-AzEnvironment och Set-AzEnvironment har uppdaterats för att godkänna parametern AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="f9e89-2081">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="f9e89-2082">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f9e89-2082">Az.AnalysisServices</span></span>
* <span data-ttu-id="f9e89-2083">ServiceClient används i cmdletar för dataplan och den ursprungliga autentiseringslogiken har tagits bort</span><span class="sxs-lookup"><span data-stu-id="f9e89-2083">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="f9e89-2084">Add-AzureASAccount används för omslutning av Connect-AzAccount för att undvika en icke-bakåtkompatibel ändring</span><span class="sxs-lookup"><span data-stu-id="f9e89-2084">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f9e89-2085">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f9e89-2085">Az.Automation</span></span>
* <span data-ttu-id="f9e89-2086">Buggen för cmdleten New-AzAutomationSoftwareUpdateConfiguration för inkluderingar har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2086">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="f9e89-2087">Nu bör parametern IncludedKbNumber och IncludedPackageNameMask fungera.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2087">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="f9e89-2088">Felkorrigering för dynamiska grupper i uppdateringshanteringen för azure automation</span><span class="sxs-lookup"><span data-stu-id="f9e89-2088">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f9e89-2089">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f9e89-2089">Az.Compute</span></span>
* <span data-ttu-id="f9e89-2090">Lägg till parametern HyperVGeneration i New-AzDiskConfig och New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="f9e89-2090">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="f9e89-2091">Tillåt att virtuella datorer skapas med galleribilder från andra klientorganisationer.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2091">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="f9e89-2092">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="f9e89-2092">Az.ContainerInstance</span></span>
* <span data-ttu-id="f9e89-2093">Ett problem har åtgärdats i parametern -Command för New-AzContainerGroup som lade till ett avslutande tomt argument</span><span class="sxs-lookup"><span data-stu-id="f9e89-2093">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f9e89-2094">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f9e89-2094">Az.DataFactory</span></span>
* <span data-ttu-id="f9e89-2095">ADF .Net SDK-versionen har uppdaterats till 3.0.2</span><span class="sxs-lookup"><span data-stu-id="f9e89-2095">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="f9e89-2096">Cmdleten Set-AzDataFactoryV2 har uppdaterats med extra parametrar för inställningar som rör RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2096">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f9e89-2097">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f9e89-2097">Az.Resources</span></span>
* <span data-ttu-id="f9e89-2098">Förbättra hanteringen av providrar för Get-AzResource när parametrarna -ResourceId eller -ResourceGroupName, -Name och -ResourceType tillhandahålls</span><span class="sxs-lookup"><span data-stu-id="f9e89-2098">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="f9e89-2099">Förbättra felhanteringen för ”Test-AzDeployment” och ”Test-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="f9e89-2099">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="f9e89-2100">Hantera fel utanför distributionsvalideringen och ta med dem i kommandoutdata istället</span><span class="sxs-lookup"><span data-stu-id="f9e89-2100">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="f9e89-2101">Mer information här: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="f9e89-2101">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="f9e89-2102">Lägg till växlingsparametern -IgnoreDynamicParameters till en uppsättning av cmdletar för distribution för att hoppa över fråga i skript och jobbscenarier</span><span class="sxs-lookup"><span data-stu-id="f9e89-2102">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="f9e89-2103">Mer information här: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="f9e89-2103">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="f9e89-2104">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f9e89-2104">Az.Sql</span></span>
* <span data-ttu-id="f9e89-2105">Stöd för dataklassificering av databaser.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2105">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f9e89-2106">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f9e89-2106">Az.Storage</span></span>
* <span data-ttu-id="f9e89-2107">Rapportera detaljfel när lagringskontext skapas med parametern -UseConnectedAccount, men utan inloggning på Azure-kontot</span><span class="sxs-lookup"><span data-stu-id="f9e89-2107">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="f9e89-2108">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="f9e89-2108">New-AzStorageContext</span></span>
* <span data-ttu-id="f9e89-2109">Stöd för att hantera Blob Service-egenskaper för ett angivet lagringskonto med API:et för hanteringsplan</span><span class="sxs-lookup"><span data-stu-id="f9e89-2109">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="f9e89-2110">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="f9e89-2110">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="f9e89-2111">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="f9e89-2111">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="f9e89-2112">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="f9e89-2112">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="f9e89-2113">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="f9e89-2113">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="f9e89-2114">Stöd för -AsJob-cmdletar för att ladda upp och ladda ned blobar och filer</span><span class="sxs-lookup"><span data-stu-id="f9e89-2114">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="f9e89-2115">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="f9e89-2115">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="f9e89-2116">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="f9e89-2116">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="f9e89-2117">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="f9e89-2117">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="f9e89-2118">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="f9e89-2118">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="f9e89-2119">1.6.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="f9e89-2119">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="f9e89-2120">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="f9e89-2120">Highlights since the last major release</span></span>
* <span data-ttu-id="f9e89-2121">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="f9e89-2121">General availability of `Az` module</span></span>
* <span data-ttu-id="f9e89-2122">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="f9e89-2122">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="f9e89-2123">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="f9e89-2123">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="f9e89-2124">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="f9e89-2124">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="f9e89-2125">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="f9e89-2125">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="f9e89-2126">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="f9e89-2126">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="f9e89-2127">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="f9e89-2127">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f9e89-2128">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f9e89-2128">Az.Automation</span></span>
* <span data-ttu-id="f9e89-2129">Azure Automation – ändring av uppdateringshantering för stöd för de nya funktionerna:</span><span class="sxs-lookup"><span data-stu-id="f9e89-2129">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="f9e89-2130">Dynamisk gruppering</span><span class="sxs-lookup"><span data-stu-id="f9e89-2130">Dynamic grouping</span></span>
    * <span data-ttu-id="f9e89-2131">För-/efterskrift</span><span class="sxs-lookup"><span data-stu-id="f9e89-2131">Pre-Post script</span></span>
    * <span data-ttu-id="f9e89-2132">Inställning för omstart</span><span class="sxs-lookup"><span data-stu-id="f9e89-2132">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f9e89-2133">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f9e89-2133">Az.Compute</span></span>
* <span data-ttu-id="f9e89-2134">Åtgärda problem med sökvägsmatchning i Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="f9e89-2134">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="f9e89-2135">Uppdatera Compute-klientbibliotek till 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2135">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f9e89-2136">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f9e89-2136">Az.KeyVault</span></span>
* <span data-ttu-id="f9e89-2137">Stöd för jokertecken för KeyVault-cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="f9e89-2137">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f9e89-2138">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f9e89-2138">Az.Network</span></span>
* <span data-ttu-id="f9e89-2139">Lägg till stöd för Threat Intelligence för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="f9e89-2139">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="f9e89-2140">Lägg till resurs för brandväggsprincip på översta nivå och anpassade regler för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="f9e89-2140">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f9e89-2141">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f9e89-2141">Az.RecoveryServices</span></span>
* <span data-ttu-id="f9e89-2142">SnapshotRetentionInDays har lagts till i Azure-principen för virtuella datorer för stöd av Instant RP</span><span class="sxs-lookup"><span data-stu-id="f9e89-2142">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="f9e89-2143">Pipe-stöd för avregistrering av container har lagts till</span><span class="sxs-lookup"><span data-stu-id="f9e89-2143">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="f9e89-2144">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f9e89-2144">Az.Resources</span></span>
* <span data-ttu-id="f9e89-2145">Uppdatera stöd för jokertecken för Get-AzResource och Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f9e89-2145">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="f9e89-2146">Uppdatera autentiseringsuppgifter som används vid allmänna anrop till ARM</span><span class="sxs-lookup"><span data-stu-id="f9e89-2146">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="f9e89-2147">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f9e89-2147">Az.Sql</span></span>
* <span data-ttu-id="f9e89-2148">Cmdlet-parametern (ExcludeDetectionType) för Hotidentifiering ändrades från DetectionType till sträng[] för att framtidssäkra den när nya DetectionTypes läggs till, och även för att stödja automatisk ifyllning.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2148">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f9e89-2149">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f9e89-2149">Az.Storage</span></span>
* <span data-ttu-id="f9e89-2150">Stöd för att hämta/ange/ta bort hanteringsprincip på ett lagringskonto</span><span class="sxs-lookup"><span data-stu-id="f9e89-2150">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="f9e89-2151">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="f9e89-2151">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="f9e89-2152">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="f9e89-2152">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="f9e89-2153">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="f9e89-2153">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="f9e89-2154">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="f9e89-2154">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="f9e89-2155">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="f9e89-2155">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="f9e89-2156">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="f9e89-2156">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f9e89-2157">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f9e89-2157">Az.Websites</span></span>
* <span data-ttu-id="f9e89-2158">Åtgärda fel med ARM-mall som avbryter kloning av alla platser med 'New-AzWebApp -IncludeSourceWebAppSlots'</span><span class="sxs-lookup"><span data-stu-id="f9e89-2158">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="f9e89-2159">1.5.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="f9e89-2159">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f9e89-2160">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f9e89-2160">Az.Accounts</span></span>
* <span data-ttu-id="f9e89-2161">Lägg till kommandot Register-AzModule för stöd för AutoRest-genererade cmdletar</span><span class="sxs-lookup"><span data-stu-id="f9e89-2161">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="f9e89-2162">Uppdatera exempel för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="f9e89-2162">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f9e89-2163">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f9e89-2163">Az.Automation</span></span>
* <span data-ttu-id="f9e89-2164">Problem med att hämta vissa månadsscheman i flera Azure Automation-cmdletar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="f9e89-2164">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="f9e89-2165">Åtgärda problem med att Get-AzAutomationDscNode bara returnerar de 20 översta noderna.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2165">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="f9e89-2166">Nu returneras alla noder</span><span class="sxs-lookup"><span data-stu-id="f9e89-2166">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="f9e89-2167">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f9e89-2167">Az.Cdn</span></span>
* <span data-ttu-id="f9e89-2168">Nya Powershell-cmdletar för att aktivera/inaktivera anpassade domän-HTTPS har lagts till och de gamla har gjorts inaktuella</span><span class="sxs-lookup"><span data-stu-id="f9e89-2168">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f9e89-2169">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f9e89-2169">Az.Compute</span></span>
* <span data-ttu-id="f9e89-2170">Lägg till stöd för jokertecken för Get-cmdletar</span><span class="sxs-lookup"><span data-stu-id="f9e89-2170">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f9e89-2171">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f9e89-2171">Az.DataFactory</span></span>
* <span data-ttu-id="f9e89-2172">ADF .Net SDK-versionen har uppdaterats till 3.0.1</span><span class="sxs-lookup"><span data-stu-id="f9e89-2172">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="f9e89-2173">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="f9e89-2173">Az.LogicApp</span></span>
* <span data-ttu-id="f9e89-2174">Åtgärda problemet med att ListWorkflows endast hämtar den första sidan med resultat</span><span class="sxs-lookup"><span data-stu-id="f9e89-2174">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f9e89-2175">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f9e89-2175">Az.Network</span></span>
* <span data-ttu-id="f9e89-2176">Lägg till stöd för jokertecken för Network-cmdletar</span><span class="sxs-lookup"><span data-stu-id="f9e89-2176">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f9e89-2177">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f9e89-2177">Az.RecoveryServices</span></span>
* <span data-ttu-id="f9e89-2178">Stöd har lagts till för SQL Server i virtuella Azure-datorer</span><span class="sxs-lookup"><span data-stu-id="f9e89-2178">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="f9e89-2179">SDK-uppdatering</span><span class="sxs-lookup"><span data-stu-id="f9e89-2179">SDK Update</span></span>
* <span data-ttu-id="f9e89-2180">Get-ProtectableItem-incheckning i VMappContainer har tagits bort</span><span class="sxs-lookup"><span data-stu-id="f9e89-2180">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="f9e89-2181">Name och ServerName har lagts till som parametrar för Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="f9e89-2181">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="f9e89-2182">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f9e89-2182">Az.Resources</span></span>
* <span data-ttu-id="f9e89-2183">Lägg till parametern `-TemplateObject` i cmdletar för distribution</span><span class="sxs-lookup"><span data-stu-id="f9e89-2183">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="f9e89-2184">Mer information här: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="f9e89-2184">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="f9e89-2185">Åtgärda problem med piping av resultatet i `Get-AzResource` till `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="f9e89-2185">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="f9e89-2186">Mer information här: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="f9e89-2186">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="f9e89-2187">Åtgärda problem med ändring av JSON-datatyp när `Set-AzResource` körs</span><span class="sxs-lookup"><span data-stu-id="f9e89-2187">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="f9e89-2188">Mer information här: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="f9e89-2188">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="f9e89-2189">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f9e89-2189">Az.Sql</span></span>
* <span data-ttu-id="f9e89-2190">AuditingEndpointsCommunicator uppdateras.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2190">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="f9e89-2191">Åtgärdar beteendet hos ett gränsscenario när nya diagnostikinställningar skapas.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2191">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f9e89-2192">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f9e89-2192">Az.Storage</span></span>
* <span data-ttu-id="f9e89-2193">Stöd för BlockBlobStorage när Storage-konto skapas      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f9e89-2193">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="f9e89-2194">1.4.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="f9e89-2194">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="f9e89-2195">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f9e89-2195">Az.AnalysisServices</span></span>
* <span data-ttu-id="f9e89-2196">Inaktuell AddAzureASAccount-cmdlet</span><span class="sxs-lookup"><span data-stu-id="f9e89-2196">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f9e89-2197">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f9e89-2197">Az.Automation</span></span>
* <span data-ttu-id="f9e89-2198">Hjälpen för Import-AzAutomationDscNodeConfiguration har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="f9e89-2198">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="f9e89-2199">Konfigurationsnamnsvalidering har lagts till i cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="f9e89-2199">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="f9e89-2200">Förbättrad felhantering för cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="f9e89-2200">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f9e89-2201">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f9e89-2201">Az.CognitiveServices</span></span>
* <span data-ttu-id="f9e89-2202">CustomSubdomainName har lagts till som en ny valfri parameter för New-AzCognitiveServicesAccount, som används för att ange underdomän för resursen.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2202">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f9e89-2203">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f9e89-2203">Az.Compute</span></span>
* <span data-ttu-id="f9e89-2204">Problemet med ID-parameteruppsättningar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="f9e89-2204">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="f9e89-2205">Get-AzVMExtension har uppdaterats så att alla installerade tillägg visas om parametern Name inte har angetts</span><span class="sxs-lookup"><span data-stu-id="f9e89-2205">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="f9e89-2206">Parametrarna Tag och ResourceId har lagts till i cmdleten Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="f9e89-2206">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="f9e89-2207">Get-AzVmssVM utan instans-ID och med InstanceView kan visa virtuella VMSS-datorer med instansvyn.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2207">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f9e89-2208">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f9e89-2208">Az.DataLakeStore</span></span>
* <span data-ttu-id="f9e89-2209">Cmdletar har lagts till för uppräkning och återställning av borttagna objekt i ADL</span><span class="sxs-lookup"><span data-stu-id="f9e89-2209">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f9e89-2210">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f9e89-2210">Az.EventHub</span></span>
* <span data-ttu-id="f9e89-2211">Ny boolesk egenskap SkipEmptyArchives har lagts till i Skip Empty Archives i CaptureDescription-klassen i Eventhub</span><span class="sxs-lookup"><span data-stu-id="f9e89-2211">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f9e89-2212">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f9e89-2212">Az.KeyVault</span></span>
* <span data-ttu-id="f9e89-2213">Taggning i Set-AzKeyVaultSecret har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="f9e89-2213">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="f9e89-2214">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="f9e89-2214">Az.LogicApp</span></span>
* <span data-ttu-id="f9e89-2215">Grundläggande SKU har lagts till för Integrationskonton</span><span class="sxs-lookup"><span data-stu-id="f9e89-2215">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="f9e89-2216">XSLT 2.0, XSLT 3.0 och Flytande mappningstyper har lagts till</span><span class="sxs-lookup"><span data-stu-id="f9e89-2216">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="f9e89-2217">Nya cmdletar för integrationskontosammansättningar</span><span class="sxs-lookup"><span data-stu-id="f9e89-2217">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="f9e89-2218">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="f9e89-2218">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="f9e89-2219">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="f9e89-2219">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="f9e89-2220">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="f9e89-2220">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="f9e89-2221">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="f9e89-2221">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="f9e89-2222">Nya cmdletar för batchkonfiguration för integrationskonto</span><span class="sxs-lookup"><span data-stu-id="f9e89-2222">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="f9e89-2223">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="f9e89-2223">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="f9e89-2224">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="f9e89-2224">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="f9e89-2225">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="f9e89-2225">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="f9e89-2226">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="f9e89-2226">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="f9e89-2227">Logic App-SDK har uppdaterats till version 4.1.0</span><span class="sxs-lookup"><span data-stu-id="f9e89-2227">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f9e89-2228">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f9e89-2228">Az.Monitor</span></span>
* <span data-ttu-id="f9e89-2229">Hjälpen för Get-AzMetric har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="f9e89-2229">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f9e89-2230">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f9e89-2230">Az.Network</span></span>
* <span data-ttu-id="f9e89-2231">Hjälpexempel för Add-AzApplicationGatewayCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="f9e89-2231">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f9e89-2232">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f9e89-2232">Az.OperationalInsights</span></span>
* <span data-ttu-id="f9e89-2233">Ytterligare stöd för datakällorna New och Get ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2233">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="f9e89-2234">Ny ApplicationInsights-typ har lagts till för att ge stöd för ”Get specific” och ”Get all” för ApplicationInsights-datakällor för angiven arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2234">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="f9e89-2235">Cmdleten New-AzOperationalInsightsApplicationInsightsDataSource har lagts till för att skapa datakälla med angivna parametrar för Application Insights-resurs: subscription Id, resourceGroupName och name.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2235">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f9e89-2236">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f9e89-2236">Az.Resources</span></span>
* <span data-ttu-id="f9e89-2237">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="f9e89-2237">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="f9e89-2238">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="f9e89-2238">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="f9e89-2239">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="f9e89-2239">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="f9e89-2240">Fel som gör att KeyCredentials inte kan skapas upprepade gånger har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="f9e89-2240">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="f9e89-2241">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f9e89-2241">Az.Sql</span></span>
* <span data-ttu-id="f9e89-2242">Lägg till stöd för hyperskalanivån för SQL DB</span><span class="sxs-lookup"><span data-stu-id="f9e89-2242">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="f9e89-2243">Ett fel har åtgärdats där återställningen kunde misslyckas på grund av onödiga inställningsegenskaper i restore-förfrågan</span><span class="sxs-lookup"><span data-stu-id="f9e89-2243">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f9e89-2244">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f9e89-2244">Az.Websites</span></span>
* <span data-ttu-id="f9e89-2245">Rätt exempel i Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="f9e89-2245">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="f9e89-2246">1.3.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="f9e89-2246">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f9e89-2247">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f9e89-2247">Az.Accounts</span></span>
* <span data-ttu-id="f9e89-2248">Uppdatera till den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="f9e89-2248">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="f9e89-2249">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f9e89-2249">Az.AnalysisServices</span></span>
<span data-ttu-id="f9e89-2250">Allmän tillgänglighet för Az.AnalysisServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2250">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f9e89-2251">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f9e89-2251">Az.Compute</span></span>
* <span data-ttu-id="f9e89-2252">AEM-tillägg: Lägg till stöd för UltraSSD-, P60-, P70- och P80-diskar</span><span class="sxs-lookup"><span data-stu-id="f9e89-2252">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="f9e89-2253">Uppdatera hjälpbeskrivning för Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="f9e89-2253">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="f9e89-2254">Uppdatera hjälpbeskrivning och exempel för Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="f9e89-2254">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f9e89-2255">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f9e89-2255">Az.RecoveryServices</span></span>
<span data-ttu-id="f9e89-2256">Allmän tillgänglighet för Az.RecoveryServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2256">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f9e89-2257">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f9e89-2257">Az.Resources</span></span>
* <span data-ttu-id="f9e89-2258">Korrigera taggar för resursgrupper</span><span class="sxs-lookup"><span data-stu-id="f9e89-2258">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="f9e89-2259">Mer information här: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="f9e89-2259">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="f9e89-2260">Åtgärda problem där `Get-AzureRmRoleAssignment` inte respekterar -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="f9e89-2260">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="f9e89-2261">Mer information här: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="f9e89-2261">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="f9e89-2262">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f9e89-2262">Az.Sql</span></span>
* <span data-ttu-id="f9e89-2263">Lägga till Get/Set-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="f9e89-2263">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="f9e89-2264">Åtgärda problem där ett nullref-undantag uppstår när du kör SQL-cmdletar och inte är inloggad på ett Azure-konto</span><span class="sxs-lookup"><span data-stu-id="f9e89-2264">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="f9e89-2265">Åtgärda nullref-undantag i Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="f9e89-2265">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="f9e89-2266">1.2.1 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="f9e89-2266">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f9e89-2267">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f9e89-2267">Az.Accounts</span></span>
* <span data-ttu-id="f9e89-2268">Version med rätt version av autentisering</span><span class="sxs-lookup"><span data-stu-id="f9e89-2268">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="f9e89-2269">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f9e89-2269">Az.AnalysisServices</span></span>
* <span data-ttu-id="f9e89-2270">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="f9e89-2270">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f9e89-2271">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f9e89-2271">Az.RecoveryServices</span></span>
* <span data-ttu-id="f9e89-2272">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="f9e89-2272">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="f9e89-2273">1.2.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="f9e89-2273">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f9e89-2274">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f9e89-2274">Az.Accounts</span></span>
* <span data-ttu-id="f9e89-2275">Lägga till interaktiv autentisering och autentisering med användarnamn/lösenord för endast Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="f9e89-2275">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="f9e89-2276">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="f9e89-2276">Update incorrect online help URLs</span></span>
* <span data-ttu-id="f9e89-2277">Lägga till varningsmeddelande i PS Core för Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="f9e89-2277">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="f9e89-2278">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="f9e89-2278">Az.Aks</span></span>
* <span data-ttu-id="f9e89-2279">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="f9e89-2279">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f9e89-2280">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f9e89-2280">Az.Automation</span></span>
* <span data-ttu-id="f9e89-2281">Stöd för Python 2-runbookflöden har lagts till</span><span class="sxs-lookup"><span data-stu-id="f9e89-2281">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="f9e89-2282">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="f9e89-2282">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="f9e89-2283">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f9e89-2283">Az.Cdn</span></span>
* <span data-ttu-id="f9e89-2284">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="f9e89-2284">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f9e89-2285">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f9e89-2285">Az.Compute</span></span>
* <span data-ttu-id="f9e89-2286">Lägga till cmdleten Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="f9e89-2286">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="f9e89-2287">Lägga till TempDisk-parameter i Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f9e89-2287">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="f9e89-2288">Korrigera varningsmeddelande för New-AzVM</span><span class="sxs-lookup"><span data-stu-id="f9e89-2288">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="f9e89-2289">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f9e89-2289">Az.ContainerRegistry</span></span>
* <span data-ttu-id="f9e89-2290">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="f9e89-2290">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f9e89-2291">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f9e89-2291">Az.DataFactory</span></span>
* <span data-ttu-id="f9e89-2292">ADF .Net SDK-versionen har uppdaterats till 3.0.0</span><span class="sxs-lookup"><span data-stu-id="f9e89-2292">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f9e89-2293">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f9e89-2293">Az.DataLakeStore</span></span>
* <span data-ttu-id="f9e89-2294">Åtgärda problem med ADLS-slutpunkt vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="f9e89-2294">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="f9e89-2295">Mer information här: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="f9e89-2295">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="f9e89-2296">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="f9e89-2296">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f9e89-2297">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f9e89-2297">Az.IotHub</span></span>
* <span data-ttu-id="f9e89-2298">Lägga till kodningsformat i cmdleten Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2298">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f9e89-2299">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f9e89-2299">Az.KeyVault</span></span>
* <span data-ttu-id="f9e89-2300">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="f9e89-2300">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f9e89-2301">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f9e89-2301">Az.Network</span></span>
* <span data-ttu-id="f9e89-2302">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="f9e89-2302">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="f9e89-2303">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f9e89-2303">Az.Resources</span></span>
* <span data-ttu-id="f9e89-2304">Åtgärda felaktiga exempel i referensdokumentationen ”New-AzADAppCredential” och ”New-AzADSpCredential”</span><span class="sxs-lookup"><span data-stu-id="f9e89-2304">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="f9e89-2305">Åtgärda problem där sökvägen för parametern ”-TemplateFile” inte omvandlas innan cmdletarna för distribution i resursgruppen körs</span><span class="sxs-lookup"><span data-stu-id="f9e89-2305">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="f9e89-2306">Az.Resources: Korrigera dokumentationen om standardvärdet för New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="f9e89-2306">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="f9e89-2307">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="f9e89-2307">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="f9e89-2308">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="f9e89-2308">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="f9e89-2309">Åtgärda formateringsproblemet med objektet ”PSResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="f9e89-2309">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="f9e89-2310">Mer information här: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="f9e89-2310">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f9e89-2311">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f9e89-2311">Az.ServiceFabric</span></span>
* <span data-ttu-id="f9e89-2312">Återställ när ett certifikat läggs till i en Virtual Machine Scale Sets-modell men ett undantag genereras. Detta har gjorts för att åtgärda följande fel: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="f9e89-2312">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="f9e89-2313">Korrigera några felmeddelanden.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2313">Fix some error messages.</span></span>
* <span data-ttu-id="f9e89-2314">Korrigering av skapande av kluster med ARM-mall som är standard för New-AzServiceFabriCluster som inte fungerade med migrering till Az.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2314">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="f9e89-2315">Korrigering av tilläggning av kluster/programcertifikat så att endast VM Scale Sets som motsvarar klustret läggs till genom att kontrollera ID för klustret i tillägget.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2315">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="f9e89-2316">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="f9e89-2316">Az.SignalR</span></span>
* <span data-ttu-id="f9e89-2317">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="f9e89-2317">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="f9e89-2318">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f9e89-2318">Az.Sql</span></span>
* <span data-ttu-id="f9e89-2319">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="f9e89-2319">Update incorrect online help URLs</span></span>
* <span data-ttu-id="f9e89-2320">Uppdaterad parameterbeskrivning för LicenseType-parameter med möjliga värden</span><span class="sxs-lookup"><span data-stu-id="f9e89-2320">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="f9e89-2321">Korrigering för att uppdatera hanterad instansidentitet som inte fungerar när det är den enda uppdaterade egenskapen</span><span class="sxs-lookup"><span data-stu-id="f9e89-2321">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="f9e89-2322">Stöd för anpassad sortering på hanterad instans</span><span class="sxs-lookup"><span data-stu-id="f9e89-2322">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f9e89-2323">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f9e89-2323">Az.Storage</span></span>
* <span data-ttu-id="f9e89-2324">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="f9e89-2324">Update incorrect online help URLs</span></span>
* <span data-ttu-id="f9e89-2325">Tillhandahåll detaljerat felmeddelande när en användare försöker hämta/konfigurera klassisk loggning/mått på ett Premium Storage-konto eftersom Premium Storage-kontot inte har stöd för klassisk loggning/mått.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2325">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="f9e89-2326">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="f9e89-2326">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="f9e89-2327">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="f9e89-2327">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="f9e89-2328">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="f9e89-2328">Az.TrafficManager</span></span>
* <span data-ttu-id="f9e89-2329">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="f9e89-2329">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f9e89-2330">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f9e89-2330">Az.Websites</span></span>
* <span data-ttu-id="f9e89-2331">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="f9e89-2331">Update incorrect online help URLs</span></span>
* <span data-ttu-id="f9e89-2332">Korrigerar ”New-AzWebAppSSLBinding” så att certifikatet laddas upp till rätt resursgrupp och plats om appen finns i en ASE.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2332">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="f9e89-2333">Korrigerar ”New-AzWebAppSSLBinding” så att taggarna inte skrivs över på en bindning av ett SSL-certifikat till en app</span><span class="sxs-lookup"><span data-stu-id="f9e89-2333">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="f9e89-2334">1.1.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="f9e89-2334">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f9e89-2335">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f9e89-2335">Az.Accounts</span></span>
* <span data-ttu-id="f9e89-2336">Lade till omfattningen ”Lokal” till Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="f9e89-2336">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f9e89-2337">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f9e89-2337">Az.Compute</span></span>
* <span data-ttu-id="f9e89-2338">Namn är nu valfritt i ID-parametern för Restart/Start/Stop/Remove/Set-AzVM och Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="f9e89-2338">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="f9e89-2339">Uppdaterade beskrivningen av ID i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="f9e89-2339">Updated the description of ID in help files</span></span>
* <span data-ttu-id="f9e89-2340">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f9e89-2340">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f9e89-2341">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f9e89-2341">Az.DataLakeStore</span></span>
* <span data-ttu-id="f9e89-2342">Uppdatera sdk-versionen av dataplanet till 1.1.14 för SDK-korrigeringar.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2342">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="f9e89-2343">Korrigerade hanteringen av negativ accesstime och modificationtime för getfilestatus och liststatus; korrigera asynkront annulleringstoken</span><span class="sxs-lookup"><span data-stu-id="f9e89-2343">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="f9e89-2344">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="f9e89-2344">Az.EventGrid</span></span>
* <span data-ttu-id="f9e89-2345">Uppdaterat för användning av API-versionen 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2345">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="f9e89-2346">Uppdaterade följande cmdletar för att stödja nytt scenario i API-versionen 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="f9e89-2346">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="f9e89-2347">New-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="f9e89-2347">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="f9e89-2348">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="f9e89-2348">Event Time-To-Live,</span></span>
        - <span data-ttu-id="f9e89-2349">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="f9e89-2349">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="f9e89-2350">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2350">Dead letter endpoint.</span></span>
    - <span data-ttu-id="f9e89-2351">Update-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="f9e89-2351">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="f9e89-2352">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="f9e89-2352">Event Time-To-Live,</span></span>
        - <span data-ttu-id="f9e89-2353">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="f9e89-2353">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="f9e89-2354">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2354">Dead letter endpoint.</span></span>
* <span data-ttu-id="f9e89-2355">Lade till nya enum-värden (storageQueue och hybridConnection) för alternativet EndpointType i cmdletarna New-AzureRmEventGridSubscription och Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2355">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="f9e89-2356">Visa varningsmeddelanden om skapande eller uppdatering av händelseprenumerationen förväntas medföra manuell åtgärd från användaren.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2356">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f9e89-2357">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f9e89-2357">Az.IotHub</span></span>
* <span data-ttu-id="f9e89-2358">Har uppdaterats till den senaste versionen av SDK:n lotHub</span><span class="sxs-lookup"><span data-stu-id="f9e89-2358">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="f9e89-2359">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="f9e89-2359">Az.LogicApp</span></span>
* <span data-ttu-id="f9e89-2360">Get-AzLogicApp visar en lista över alla som inte har angivet namn</span><span class="sxs-lookup"><span data-stu-id="f9e89-2360">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="f9e89-2361">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f9e89-2361">Az.Resources</span></span>
* <span data-ttu-id="f9e89-2362">Åtgärdade problem med parameteruppsättningen när parametrarna -ODataQuery och -ResourceId anges för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="f9e89-2362">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="f9e89-2363">Mer information här: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="f9e89-2363">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="f9e89-2364">Åtgärdade hantering av parametern -Custom i New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f9e89-2364">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="f9e89-2365">Korrigerade stavfel i New-AzDeployment-dokumentationen</span><span class="sxs-lookup"><span data-stu-id="f9e89-2365">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="f9e89-2366">Gjorde parametern -MailNickname obligatorisk för New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="f9e89-2366">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="f9e89-2367">Mer information här: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="f9e89-2367">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="f9e89-2368">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="f9e89-2368">Az.SignalR</span></span>
* <span data-ttu-id="f9e89-2369">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f9e89-2369">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="f9e89-2370">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f9e89-2370">Az.Sql</span></span>
* <span data-ttu-id="f9e89-2371">Konverterade lagringshanteringsklientens beroende av den normala SDK-implementeringen.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2371">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f9e89-2372">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f9e89-2372">Az.Storage</span></span>
* <span data-ttu-id="f9e89-2373">Angav StorageAccountName för lagringskontext som det verkliga namnet på lagringskontot när det skapas med Sas Token, OAuth eller Anonymous</span><span class="sxs-lookup"><span data-stu-id="f9e89-2373">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="f9e89-2374">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="f9e89-2374">New-AzStorageContext</span></span>
* <span data-ttu-id="f9e89-2375">Skapade Sas Token för Blob Snapshot-objekt med parametern -FullUri, åtgärdade den returnerade URI:n så att den blir URI för ögonblicksbild</span><span class="sxs-lookup"><span data-stu-id="f9e89-2375">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="f9e89-2376">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="f9e89-2376">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f9e89-2377">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f9e89-2377">Az.Websites</span></span>
* <span data-ttu-id="f9e89-2378">Åtgärdade en bugg i datumparsningen i Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="f9e89-2378">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="f9e89-2379">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f9e89-2379">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="f9e89-2380">1.0.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="f9e89-2380">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="f9e89-2381">Allmänt</span><span class="sxs-lookup"><span data-stu-id="f9e89-2381">General</span></span>

- <span data-ttu-id="f9e89-2382">Allmän tillgänglighet för Az-modulen</span><span class="sxs-lookup"><span data-stu-id="f9e89-2382">General Availability of Az Module</span></span>
- <span data-ttu-id="f9e89-2383">Onlinehjälp för varje modul</span><span class="sxs-lookup"><span data-stu-id="f9e89-2383">Online help for each module</span></span>
- <span data-ttu-id="f9e89-2384">Mer information och en översikt finns på [Az-informationssidan](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="f9e89-2384">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="f9e89-2385">Information om hur du migrerar från AzureRM finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f9e89-2385">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="f9e89-2386">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f9e89-2386">Az.Accounts</span></span>
- <span data-ttu-id="f9e89-2387">Har ändrats från Az.Profile</span><span class="sxs-lookup"><span data-stu-id="f9e89-2387">Changed from Az.Profile</span></span>
- <span data-ttu-id="f9e89-2388">Fasta tabellformat för profil- och kontexttyper</span><span class="sxs-lookup"><span data-stu-id="f9e89-2388">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="f9e89-2389">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f9e89-2389">Az.ApiManagement</span></span>
- <span data-ttu-id="f9e89-2390">Korrigeringar för #7002</span><span class="sxs-lookup"><span data-stu-id="f9e89-2390">Fixes for #7002</span></span>
- <span data-ttu-id="f9e89-2391">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f9e89-2391">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="f9e89-2392">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="f9e89-2392">Az.Batch</span></span>
- <span data-ttu-id="f9e89-2393">Lade till möjligheten att se vilken version av Azure Batch Node Agent som körs på var och en av de virtuella datorerna i en pool, via den nya egenskapen `NodeAgentInformation` på `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2393">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="f9e89-2394">Standarden `Caching` för `PSDataDisk` är nu `ReadWrite` i stället för `None`.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2394">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="f9e89-2395">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f9e89-2395">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="f9e89-2396">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="f9e89-2396">Az.Billing</span></span>
- <span data-ttu-id="f9e89-2397">Kombinerar cmdletarna för fakturering, förbrukning och UsageAggregates. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f9e89-2397">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="f9e89-2398">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="f9e89-2398">Az.CognitivServices</span></span>
- <span data-ttu-id="f9e89-2399">Lade till kompletterare för SkuName och Typem som är tillgängliga i New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="f9e89-2399">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="f9e89-2400">Tog bort parameteruppsättningen GetSkusWithAccountParamSetName från Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="f9e89-2400">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="f9e89-2401">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="f9e89-2401">Az.ContainerInstance</span></span>
- <span data-ttu-id="f9e89-2402">Stöd för ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="f9e89-2402">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="f9e89-2403">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="f9e89-2403">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="f9e89-2404">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f9e89-2404">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="f9e89-2405">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f9e89-2405">Az.DataLakeStore</span></span>
- <span data-ttu-id="f9e89-2406">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f9e89-2406">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="f9e89-2407">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f9e89-2407">Az.Monitor</span></span>
- <span data-ttu-id="f9e89-2408">Döpte om Az.Insights till Az.Monitor och andra mindre icke-bakåtkompatibla ändringar. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f9e89-2408">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="f9e89-2409">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f9e89-2409">Az.KeyVault</span></span>
- <span data-ttu-id="f9e89-2410">Tog bort den inaktuella egenskapen PurgeDisabled från utdatatyper</span><span class="sxs-lookup"><span data-stu-id="f9e89-2410">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="f9e89-2411">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="f9e89-2411">Az.MachineLearning</span></span>
- <span data-ttu-id="f9e89-2412">Inkluderade cmdletarna från modulen Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="f9e89-2412">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="f9e89-2413">Az.Media</span><span class="sxs-lookup"><span data-stu-id="f9e89-2413">Az.Media</span></span>
- <span data-ttu-id="f9e89-2414">Tog bort inaktuella -Tags-alias från New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="f9e89-2414">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="f9e89-2415">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f9e89-2415">Az.Network</span></span>
<span data-ttu-id="f9e89-2416">Stöd har lagts till för konfiguration av RewriteRuleSets i Application Gateway</span><span class="sxs-lookup"><span data-stu-id="f9e89-2416">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="f9e89-2417">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="f9e89-2417">New cmdlets added:</span></span>
        - <span data-ttu-id="f9e89-2418">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f9e89-2418">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="f9e89-2419">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f9e89-2419">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="f9e89-2420">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f9e89-2420">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="f9e89-2421">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f9e89-2421">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="f9e89-2422">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f9e89-2422">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="f9e89-2423">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="f9e89-2423">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="f9e89-2424">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="f9e89-2424">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="f9e89-2425">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="f9e89-2425">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="f9e89-2426">Cmdletar har uppdaterats med den valfria parametern -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f9e89-2426">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="f9e89-2427">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f9e89-2427">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="f9e89-2428">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f9e89-2428">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="f9e89-2429">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f9e89-2429">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="f9e89-2430">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f9e89-2430">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="f9e89-2431">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="f9e89-2431">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="f9e89-2432">New-AzureRmApplicationGatewayUrlPathMapConfig har lagt till KeyVault-stöd för Application Gateway med Identity.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2432">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="f9e89-2433">Cmdletar har uppdaterats med den valfria parametern -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="f9e89-2433">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="f9e89-2434">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f9e89-2434">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="f9e89-2435">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f9e89-2435">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="f9e89-2436">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f9e89-2436">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="f9e89-2437">Cmdleten New-AzApplicationGateway har uppdaterats med den valfria parametern -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="f9e89-2437">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="f9e89-2438">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f9e89-2438">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="f9e89-2439">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f9e89-2439">Az.OperationalInsights</span></span>
- <span data-ttu-id="f9e89-2440">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f9e89-2440">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="f9e89-2441">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="f9e89-2441">Az.Profile</span></span>
- <span data-ttu-id="f9e89-2442">Modulnamnet har ändrats till Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f9e89-2442">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="f9e89-2443">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f9e89-2443">Az.RecoveryServices</span></span>
- <span data-ttu-id="f9e89-2444">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f9e89-2444">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="f9e89-2445">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f9e89-2445">Az.Resources</span></span>
- <span data-ttu-id="f9e89-2446">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f9e89-2446">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="f9e89-2447">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f9e89-2447">Az.ServiceFabric</span></span>
- <span data-ttu-id="f9e89-2448">Stöd för specificering av certifikat efter eget namn och tumavtryck</span><span class="sxs-lookup"><span data-stu-id="f9e89-2448">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="f9e89-2449">Information om fler icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f9e89-2449">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="f9e89-2450">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="f9e89-2450">Az.SIgnalR</span></span>
- <span data-ttu-id="f9e89-2451">Allmän tillgänglighet för PowerShell-cmdletar för SIgnalR</span><span class="sxs-lookup"><span data-stu-id="f9e89-2451">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="f9e89-2452">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f9e89-2452">Az.Sql</span></span>
- <span data-ttu-id="f9e89-2453">Lade till de nya identifieringstyperna Data_Exfiltration och Unsafe_Action i Threat Detection-cmdletar</span><span class="sxs-lookup"><span data-stu-id="f9e89-2453">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="f9e89-2454">Uppdaterade dokumentationsexempel för Sql Auditing-cmdletar</span><span class="sxs-lookup"><span data-stu-id="f9e89-2454">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="f9e89-2455">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f9e89-2455">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="f9e89-2456">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f9e89-2456">Az.Storage</span></span>
- <span data-ttu-id="f9e89-2457">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f9e89-2457">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="f9e89-2458">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f9e89-2458">Az.Websites</span></span>
- <span data-ttu-id="f9e89-2459">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f9e89-2459">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="f9e89-2460">0.7.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="f9e89-2460">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="f9e89-2461">Allmänt</span><span class="sxs-lookup"><span data-stu-id="f9e89-2461">General</span></span>

* <span data-ttu-id="f9e89-2462">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="f9e89-2462">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="f9e89-2463">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f9e89-2463">Az.Compute</span></span>

* <span data-ttu-id="f9e89-2464">Lade till stöd för UltraSSD och Galleriavbildningar i de enkla parameteruppsättningarna för `New-AzVm(ss)`-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2464">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="f9e89-2465">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f9e89-2465">Az.DataLakeStore</span></span>

* <span data-ttu-id="f9e89-2466">Åtgärdade avslutande snedstreck i domänen för adls-konto</span><span class="sxs-lookup"><span data-stu-id="f9e89-2466">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="f9e89-2467">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f9e89-2467">Az.FrontDoor</span></span>

* <span data-ttu-id="f9e89-2468">Brutna länkar korrigerades</span><span class="sxs-lookup"><span data-stu-id="f9e89-2468">Fixed some broken links</span></span>
    - <span data-ttu-id="f9e89-2469">I artiklarna New-AzureRmFrontDoor och Set-AzureRmFrontDoor artiklar korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2469">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="f9e89-2470">I artikeln New-AzureRmFrontDoorManagedRuleObject korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2470">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="f9e89-2471">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f9e89-2471">Az.RecoveryServices</span></span>

* <span data-ttu-id="f9e89-2472">Lade till valideringar på klientsidan för Azure-filresurs med återställningsåtgärder.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2472">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="f9e89-2473">Gjorde storageAccountName och storageAccountResourceGroupName valfritt för afs-återställning.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2473">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="f9e89-2474">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f9e89-2474">Az.Resources</span></span>

* <span data-ttu-id="f9e89-2475">Korrigering för https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="f9e89-2475">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="f9e89-2476">Uppdaterade Get-AzureRmRoleAssignment så att prenumerationsomfattningen används om den anges vid begäran om klassiska administratörer.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2476">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="f9e89-2477">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f9e89-2477">Az.Sql</span></span>

* <span data-ttu-id="f9e89-2478">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="f9e89-2478">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="f9e89-2479">Korrigerade ett problem med Get-AzureRmSqlDatabaseVulnerabilityAssessment med DotNet-kärna</span><span class="sxs-lookup"><span data-stu-id="f9e89-2479">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="f9e89-2480">Ändrade dokumentationen för hjälpmeddelanden som rör SQL Auditing-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2480">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="f9e89-2481">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f9e89-2481">Az.Storage</span></span>

* <span data-ttu-id="f9e89-2482">Lade till -EnableHierarchicalNamespace i New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f9e89-2482">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="f9e89-2483">Åtgärdade problemet med att cmdleten Copy File inte kunde återanvända källkontexten på målet om inte -DestContext angetts</span><span class="sxs-lookup"><span data-stu-id="f9e89-2483">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="f9e89-2484">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="f9e89-2484">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="f9e89-2485">Stöd för statisk webbplatskonfiguration</span><span class="sxs-lookup"><span data-stu-id="f9e89-2485">Support Static Website configuration</span></span>
    - <span data-ttu-id="f9e89-2486">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="f9e89-2486">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="f9e89-2487">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="f9e89-2487">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="f9e89-2488">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f9e89-2488">Az.Websites</span></span>

* <span data-ttu-id="f9e89-2489">Set-AzureRmWebApp och Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f9e89-2489">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="f9e89-2490">Ny parameter (-AzureStoragePath) har lagts till för att ange att Azure Storage-sökvägar ska monteras i containerappar i Windows och Linux.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2490">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="f9e89-2491">Använder utdata från den nya cmdleten New-AzureRmWebAppAzureStoragePath som en parameter för att ange sökvägar för Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2491">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="f9e89-2492">0.6.1 – november 2018</span><span class="sxs-lookup"><span data-stu-id="f9e89-2492">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="f9e89-2493">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f9e89-2493">Az.ApiManagement</span></span>
* <span data-ttu-id="f9e89-2494">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="f9e89-2494">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="f9e89-2495">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f9e89-2495">Az.Automation</span></span>
* <span data-ttu-id="f9e89-2496">Swagger baserade Azure Automation-cmdletar</span><span class="sxs-lookup"><span data-stu-id="f9e89-2496">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="f9e89-2497">Cmdletar för Uppdateringshantering har lagts till</span><span class="sxs-lookup"><span data-stu-id="f9e89-2497">Added Update Management cmdlets</span></span>
* <span data-ttu-id="f9e89-2498">Cmdletar för källkontroll har lagts till</span><span class="sxs-lookup"><span data-stu-id="f9e89-2498">Added Source Control cmdlets</span></span>
* <span data-ttu-id="f9e89-2499">Remove-AzureRmAutomationHybridWorkerGroup-cmdlet har lagts till</span><span class="sxs-lookup"><span data-stu-id="f9e89-2499">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="f9e89-2500">Kommandot för DSC-registreringsnod har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="f9e89-2500">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="f9e89-2501">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f9e89-2501">Az.Compute</span></span>
* <span data-ttu-id="f9e89-2502">Problem med SystemAssigned-identitet har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="f9e89-2502">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="f9e89-2503">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="f9e89-2503">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="f9e89-2504">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="f9e89-2504">Az.ContainerInstance</span></span>
* <span data-ttu-id="f9e89-2505">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="f9e89-2505">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="f9e89-2506">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="f9e89-2506">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="f9e89-2507">uppdatera exempelbeskrivningen för marketplace-cmdletar</span><span class="sxs-lookup"><span data-stu-id="f9e89-2507">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="f9e89-2508">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f9e89-2508">Az.Network</span></span>
* <span data-ttu-id="f9e89-2509">Cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomErreller Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="f9e89-2509">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="f9e89-2510">ICMP tillbaka till stöd för Azure Firewall-nätverksprotokoll har lagts till</span><span class="sxs-lookup"><span data-stu-id="f9e89-2510">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="f9e89-2511">Uppdatera cmdlet Test-AzureRmNetworkWatcherConnectivity, lägga till verifiering av mål-id, adress och port.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2511">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="f9e89-2512">Åtgärda problem med minnesanvändning i VirtualNetwork-karta</span><span class="sxs-lookup"><span data-stu-id="f9e89-2512">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="f9e89-2513">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="f9e89-2513">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="f9e89-2514">Åtgärda för att ändra principen för en skyddad fildelning.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2514">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="f9e89-2515">Tidszonsprincipen har konverterats till versaler.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2515">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="f9e89-2516">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="f9e89-2516">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="f9e89-2517">Exempel i New-AzureRmRecoveryServicesAsrProtectableItem har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="f9e89-2517">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="f9e89-2518">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="f9e89-2518">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="f9e89-2519">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="f9e89-2519">Az.Relay</span></span>
* <span data-ttu-id="f9e89-2520">Valfri parameter -KeyValue till New-AzureRmRelayKey cmdlet har lagts till, vilket gör det möjligt för användare att tillhandahålla KeyValue.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2520">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="f9e89-2521">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f9e89-2521">Az.Resources</span></span>
* <span data-ttu-id="f9e89-2522">Uppdatera hjälpdokumentation för resursidentitet kopplad till parametrar i `New-AzureRmPolicyAssignment` och `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="f9e89-2522">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="f9e89-2523">Lägg till ett exempel för New-AzureRmPolicyDefinition som använder -Metadata</span><span class="sxs-lookup"><span data-stu-id="f9e89-2523">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="f9e89-2524">Korrigera så att skiftläge behålls i taggnycklar i NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="f9e89-2524">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="f9e89-2525">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f9e89-2525">Az.ServiceFabric</span></span>
* <span data-ttu-id="f9e89-2526">Lägg till utfasningsmeddelanden för kommande icke-kompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="f9e89-2526">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="f9e89-2527">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f9e89-2527">Az.Sql</span></span>
* <span data-ttu-id="f9e89-2528">Nya cmdletar för CRUD-åtgärder på Azure Sql Database-hanterad instans och Azure Sql-hanterad databas</span><span class="sxs-lookup"><span data-stu-id="f9e89-2528">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="f9e89-2529">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="f9e89-2529">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="f9e89-2530">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="f9e89-2530">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="f9e89-2531">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="f9e89-2531">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="f9e89-2532">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="f9e89-2532">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="f9e89-2533">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="f9e89-2533">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="f9e89-2534">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="f9e89-2534">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="f9e89-2535">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="f9e89-2535">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="f9e89-2536">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="f9e89-2536">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="f9e89-2537">Hantering av utökad granskningsprincip på en server eller en databas har aktiverats.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2537">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="f9e89-2538">Ny parameter (PredicateExpression) har lagts till för att aktivera filtrering av granskningsloggar.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2538">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="f9e89-2539">Cmdletar har ändrats så att de använder SQL-klienter i stället för äldre klienter.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2539">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="f9e89-2540">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2540">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="f9e89-2541">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2541">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="f9e89-2542">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2542">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="f9e89-2543">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2543">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="f9e89-2544">Problem med att använda Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings med lagringskontots namnparameter har korrigerats</span><span class="sxs-lookup"><span data-stu-id="f9e89-2544">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="f9e89-2545">0.5.0 – november 2018</span><span class="sxs-lookup"><span data-stu-id="f9e89-2545">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="f9e89-2546">Allmänt</span><span class="sxs-lookup"><span data-stu-id="f9e89-2546">General</span></span>
* <span data-ttu-id="f9e89-2547">Lade till resurskompletterare till många kärn-cmdletar – dessa gör att du kan stega genom befintliga resursnamn med TABB vid interaktiva anrop till cmdletar</span><span class="sxs-lookup"><span data-stu-id="f9e89-2547">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="f9e89-2548">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="f9e89-2548">Az.Profile</span></span>
* <span data-ttu-id="f9e89-2549">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="f9e89-2549">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="f9e89-2550">Bytte namn på parametern TenantId i cmdleten Connect-AzAccount till Tenant och lade till ett alias för TenantId</span><span class="sxs-lookup"><span data-stu-id="f9e89-2550">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="f9e89-2551">Uppdaterade TenantId-beskrivningen för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="f9e89-2551">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="f9e89-2552">Åtgärda felmeddelande för misslyckad inloggning när du tillhandahåller klientdomän</span><span class="sxs-lookup"><span data-stu-id="f9e89-2552">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="f9e89-2553">Åtgärda problem med att kontextnamn hamnar i konflikt för konton utan prenumerationer i klientorganisationen</span><span class="sxs-lookup"><span data-stu-id="f9e89-2553">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="f9e89-2554">Åtgärda problem med DataLake-slutpunkter vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="f9e89-2554">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="f9e89-2555">Åtgärdade problem med att Disconnect-AzAccount kastades om den inte anslöts</span><span class="sxs-lookup"><span data-stu-id="f9e89-2555">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="f9e89-2556">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f9e89-2556">Az.CognitiveServices</span></span>
* <span data-ttu-id="f9e89-2557">Lade till åtgärden Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2557">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f9e89-2558">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f9e89-2558">Az.Compute</span></span>
* <span data-ttu-id="f9e89-2559">Lade till cmdletarna Add-AzVmssVMDataDisk och Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="f9e89-2559">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="f9e89-2560">Get-AzVMImage visar AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="f9e89-2560">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="f9e89-2561">Åtgärdade att värdena för alternativen SetAzVMChefExtension -BootstrapOptions och -JsonAttribute inte angavs i json-format.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2561">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f9e89-2562">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f9e89-2562">Az.DataLakeStore</span></span>
* <span data-ttu-id="f9e89-2563">Uppdatera DataLake-paketet till 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2563">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="f9e89-2564">Lägg till standardsamtidighet för flertrådade åtgärder.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2564">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="f9e89-2565">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="f9e89-2565">Az.Insights</span></span>
* <span data-ttu-id="f9e89-2566">Åtgärdade problem #7267 (autoskalningsområde)</span><span class="sxs-lookup"><span data-stu-id="f9e89-2566">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="f9e89-2567">Problem med att uppräknade parametrar inte ställdes in ordentligt när du skapade en ny autoskalningsregel (de ställdes alltid in med standardvärdet).</span><span class="sxs-lookup"><span data-stu-id="f9e89-2567">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="f9e89-2568">Åtgärdade problem #7513 [Insights] Set-AzDiagnosticSetting kräver uttrycklig specifikation av kategorier när inställningar skapas</span><span class="sxs-lookup"><span data-stu-id="f9e89-2568">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="f9e89-2569">Nu kräver inte cmdleten uttrycklig anvisning av kategorierna för att aktiveras under skapande, d.v.s. den fungerar enligt beskrivning</span><span class="sxs-lookup"><span data-stu-id="f9e89-2569">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f9e89-2570">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f9e89-2570">Az.Network</span></span>
* <span data-ttu-id="f9e89-2571">PeeringType ändrades till en obligatorisk parameter för följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="f9e89-2571">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="f9e89-2572">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="f9e89-2572">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="f9e89-2573">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="f9e89-2573">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="f9e89-2574">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="f9e89-2574">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="f9e89-2575">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="f9e89-2575">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="f9e89-2576">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="f9e89-2576">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="f9e89-2577">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="f9e89-2577">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f9e89-2578">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f9e89-2578">Az.PolicyInsights</span></span>
* <span data-ttu-id="f9e89-2579">Cmdletar för principreparation har lagts till</span><span class="sxs-lookup"><span data-stu-id="f9e89-2579">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="f9e89-2580">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f9e89-2580">Az.Resources</span></span>
* <span data-ttu-id="f9e89-2581">Korrigering för https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="f9e89-2581">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="f9e89-2582">Tillåt att resurser listas med parametern -ResourceId för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="f9e89-2582">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="f9e89-2583">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f9e89-2583">Az.ServiceBus</span></span>
* <span data-ttu-id="f9e89-2584">Skrivskyddad MigrationState-egenskap har lagts till i PSServiceBusMigrationConfigurationAttributes, som hjälper till att hålla koll på migreringstillståndet.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2584">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f9e89-2585">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f9e89-2585">Az.ServiceFabric</span></span>
* <span data-ttu-id="f9e89-2586">Åtgärda att lägga till certifikat till Linux-Vmss.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2586">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="f9e89-2587">Åtgärdade Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="f9e89-2587">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="f9e89-2588">Använd rätt tumavtryck från nya certifikat (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="f9e89-2588">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="f9e89-2589">Visa undantag korrekt (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="f9e89-2589">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="f9e89-2590">Åtgärdade Update-AzServiceFabricDurability så att klusterkonfigurationen uppdateras innan Vmss-åtgärden CreateOrUpdate påbörjas.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2590">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="f9e89-2591">0.4.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="f9e89-2591">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="f9e89-2592">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="f9e89-2592">Az.Profile</span></span>
* <span data-ttu-id="f9e89-2593">Åtgärdade problemet med Get-AzSubscription i CloudShell</span><span class="sxs-lookup"><span data-stu-id="f9e89-2593">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="f9e89-2594">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="f9e89-2594">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f9e89-2595">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f9e89-2595">Az.Compute</span></span>
* <span data-ttu-id="f9e89-2596">Nya storlekar lades till i listan över godkända VM-storlekar för vilka accelererat nätverk kommer att aktiveras vid användning av den enkla parameteruppsättningen för New-AzVm</span><span class="sxs-lookup"><span data-stu-id="f9e89-2596">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="f9e89-2597">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2597">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f9e89-2598">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f9e89-2598">Az.DataLakeStore</span></span>
* <span data-ttu-id="f9e89-2599">Lägger till stöd för regler för virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="f9e89-2599">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="f9e89-2600">Get-AzDataLakeStoreVirtualNetworkRule: Hämtar eller listar regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2600">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="f9e89-2601">Add-AzDataLakeStoreVirtualNetworkRule: Lägger till en regel för virtuellt nätverk i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2601">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="f9e89-2602">Set-AzDataLakeStoreVirtualNetworkRule: Ändrar den angivna regeln för virtuellt nätverk i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2602">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="f9e89-2603">Remove-AzDataLakeStoreVirtualNetworkRule: Tar bort en regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2603">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f9e89-2604">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f9e89-2604">Az.Network</span></span>
* <span data-ttu-id="f9e89-2605">Skicka protokollvärdet till serverdelen för att uppdatera cmdleten Test-AzNetworkWatcherConnectivity.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2605">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="f9e89-2606">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2606">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f9e89-2607">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f9e89-2607">Az.Resources</span></span>
* <span data-ttu-id="f9e89-2608">Åtgärdade problem där Get-AzRoleDefinition genererar ett oläsligt undantag (när standardprofilen inte innehåller någon prenumeration och ingen omfattning har angetts) genom att lägga till ett beskrivande undantag i scenariot.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2608">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="f9e89-2609">Ställ in ”RoleDefinitionNameParameterSet” som standardparameteruppsättning.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2609">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="f9e89-2610">0.3.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="f9e89-2610">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="f9e89-2611">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="f9e89-2611">Azure.Storage</span></span>
* <span data-ttu-id="f9e89-2612">Åtgärda fel där Kopiera blob/fil inte kopierar metadata när målplatsen har ett problem med metadata</span><span class="sxs-lookup"><span data-stu-id="f9e89-2612">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="f9e89-2613">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="f9e89-2613">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="f9e89-2614">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="f9e89-2614">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="f9e89-2615">Stöd för att hämta användningsinformation om en Storage-resurs för en specifik plats och för att lägga till ett varningsmeddelande för att hämta användningsinformation om en global Storage-resurs är inaktuellt.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2615">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="f9e89-2616">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="f9e89-2616">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f9e89-2617">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f9e89-2617">Az.CognitiveServices</span></span>
* <span data-ttu-id="f9e89-2618">Stöd för Get-AzCognitiveServicesAccountSkus utan ett befintligt konto.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2618">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f9e89-2619">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f9e89-2619">Az.Compute</span></span>
* <span data-ttu-id="f9e89-2620">Åtgärdade fel där Get-AzVM -ResourceGroupName <rg> returnerar fler än 50 resultat om det behövs</span><span class="sxs-lookup"><span data-stu-id="f9e89-2620">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="f9e89-2621">Lade till ett exempel för SimpleParameterSet i hjälpen för cmdleten New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2621">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="f9e89-2622">Ett stavfel i förloppsmeddelandet för Azure Disk Encryption har korrigerats</span><span class="sxs-lookup"><span data-stu-id="f9e89-2622">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="f9e89-2623">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="f9e89-2623">Az.DataFactoryV2</span></span>
* <span data-ttu-id="f9e89-2624">ADF .Net SDK-versionen har uppdaterats till 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2624">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f9e89-2625">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f9e89-2625">Az.Network</span></span>
* <span data-ttu-id="f9e89-2626">Funktionalitet för NetworkProfile har lagts till.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2626">Added NetworkProfile functionality.</span></span> <span data-ttu-id="f9e89-2627">nya cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="f9e89-2627">new cmdlets added</span></span>
    - <span data-ttu-id="f9e89-2628">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f9e89-2628">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="f9e89-2629">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f9e89-2629">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="f9e89-2630">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f9e89-2630">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="f9e89-2631">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f9e89-2631">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="f9e89-2632">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="f9e89-2632">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="f9e89-2633">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="f9e89-2633">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="f9e89-2634">Länk för tjänstassociering på modell för undernät har lagts till</span><span class="sxs-lookup"><span data-stu-id="f9e89-2634">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="f9e89-2635">Cmdletarna New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap och Remove-AzVirtualNetworkTap har lagts till</span><span class="sxs-lookup"><span data-stu-id="f9e89-2635">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="f9e89-2636">Cmdletarna Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig och Remove-AzNEtworkInterfaceTapConfig har lagts till</span><span class="sxs-lookup"><span data-stu-id="f9e89-2636">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="f9e89-2637">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="f9e89-2637">Az.RedisCache</span></span>
* <span data-ttu-id="f9e89-2638">Tillåt att alla strängar används som storleksparametrar framöver.</span><span class="sxs-lookup"><span data-stu-id="f9e89-2638">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="f9e89-2639">Lägg till P5 i popup-fönstret PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="f9e89-2639">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="f9e89-2640">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f9e89-2640">Az.Resources</span></span>
* <span data-ttu-id="f9e89-2641">Parametern -Mode som saknades i Set-AzPolicyDefinition har lagts till</span><span class="sxs-lookup"><span data-stu-id="f9e89-2641">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="f9e89-2642">Åtgärdade buggen för cmdleten Get-AzProviderOperation för åtgärder med ursprung som innehåller användare</span><span class="sxs-lookup"><span data-stu-id="f9e89-2642">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="f9e89-2643">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f9e89-2643">Az.Sql</span></span>
* <span data-ttu-id="f9e89-2644">Ett problem där vissa cmdletar för säkerhetskopiering inte kunde identifiera den aktuella azure-prenumerationen har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="f9e89-2644">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f9e89-2645">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f9e89-2645">Az.Websites</span></span>
* <span data-ttu-id="f9e89-2646">Ny cmdlet: Get-AzWebAppContainerContinuousDeploymentUrl – Hämtar webhook-URL:en för kontinuerlig distribution av container</span><span class="sxs-lookup"><span data-stu-id="f9e89-2646">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="f9e89-2647">Nya cmdletar: New-AzWebAppContainerPSSession och Enter-WebAppContainerPSSession – Startar en PowerShell-fjärrsession i en containerapp för windows</span><span class="sxs-lookup"><span data-stu-id="f9e89-2647">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="f9e89-2648">0.2.0 – september 2018</span><span class="sxs-lookup"><span data-stu-id="f9e89-2648">0.2.0 - September 2018</span></span>
 <span data-ttu-id="f9e89-2649">Första versionen</span><span class="sxs-lookup"><span data-stu-id="f9e89-2649">Initial Release</span></span>
