---
title: Ändringslogg för Azure PowerShell | Microsoft Docs
description: Det här är en historik över de ändringar som gjorts i den senaste versionen av Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 08/28/2018
ms.openlocfilehash: 3cb71087a61a0fcd06c014394e8f9e5654d4c1a8
ms.sourcegitcommit: 6c38e86e16da99f65cd183c63e34f7176b121ab8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/04/2018
ms.locfileid: "47425031"
---
# <a name="release-notes"></a><span data-ttu-id="0a4c2-103">Viktig information</span><span class="sxs-lookup"><span data-stu-id="0a4c2-103">Release notes</span></span>

<span data-ttu-id="0a4c2-104">Det här är en lista över ändringar som har gjorts i Azure PowerShell i den här versionen.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="690---september-2018"></a><span data-ttu-id="0a4c2-105">6.9.0 – September 2018</span><span class="sxs-lookup"><span data-stu-id="0a4c2-105">6.9.0 - September 2018</span></span>
#### <a name="general"></a><span data-ttu-id="0a4c2-106">Allmänt</span><span class="sxs-lookup"><span data-stu-id="0a4c2-106">General</span></span>
* <span data-ttu-id="0a4c2-107">AzureRM.SignalR har lagts till i samlingsmodulen för AzureRM</span><span class="sxs-lookup"><span data-stu-id="0a4c2-107">AzureRM.SignalR was added to the AzureRM rollup module</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="0a4c2-108">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="0a4c2-108">AzureRM.Profile</span></span>
* <span data-ttu-id="0a4c2-109">Mindre ändringar i den gemensamma koden för lagring</span><span class="sxs-lookup"><span data-stu-id="0a4c2-109">Minor changes to the storage common code</span></span>
* <span data-ttu-id="0a4c2-110">Hjälpfiler har uppdaterats för att innehålla fullständiga parametertyper.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-110">Updated help files to include full parameter types.</span></span>
- <span data-ttu-id="0a4c2-111">-ServicePrincipal har ändrats så att den inte längre är obligatorisk i parameteruppsättningen ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0a4c2-111">Changed -ServicePrincipal to non-mandatory in the ServicePrincipalCertificateWithSubscriptionId parameter set</span></span> 

#### <a name="azurestorage"></a><span data-ttu-id="0a4c2-112">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="0a4c2-112">Azure.Storage</span></span>
* <span data-ttu-id="0a4c2-113">Stöd för att skapa lagringskontext med OAuth.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-113">Support create Storage Context with OAuth.</span></span> 
    - <span data-ttu-id="0a4c2-114">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="0a4c2-114">New-AzureStorageContext</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="0a4c2-115">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="0a4c2-115">AzureRM.Cdn</span></span>
* <span data-ttu-id="0a4c2-116">Standard_Microsoft har lagts till i SKU:n för CDN-prissättning.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-116">Added Standard_Microsoft in Cdn pricing sku.</span></span> 

#### <a name="azurermcompute"></a><span data-ttu-id="0a4c2-117">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="0a4c2-117">AzureRM.Compute</span></span>
* <span data-ttu-id="0a4c2-118">Flytta beroenden i nyckelvalv och minne till de gemensamma beroendena</span><span class="sxs-lookup"><span data-stu-id="0a4c2-118">Move dependencies on Keyvault and Storage to the common dependencies</span></span>
* <span data-ttu-id="0a4c2-119">Lägg till stöd för flera storlekar av virtuella datorer i AEM-cmdletar</span><span class="sxs-lookup"><span data-stu-id="0a4c2-119">Add support for more virutal machine sizes to AEM cmdlets</span></span>
* <span data-ttu-id="0a4c2-120">Lägg till parametern PublicIPPrefix i New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="0a4c2-120">Add PublicIPPrefix parameter to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="0a4c2-121">Lägg till parametern ResourceId till cmdleten Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="0a4c2-121">Add ResourceId parameter to Invoke-AzureRmVMRunCommand cmdelt</span></span>
* <span data-ttu-id="0a4c2-122">Lägg till cmdleten Invoke-AzureRmVmssVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="0a4c2-122">Add Invoke-AzureRmVmssVMRunCommand cmdlet</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="0a4c2-123">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="0a4c2-123">AzureRM.Dns</span></span>
* <span data-ttu-id="0a4c2-124">Stöd har lagts till för aliasposter när DNS-poster skapas</span><span class="sxs-lookup"><span data-stu-id="0a4c2-124">Added support for alias record during dns record creation</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="0a4c2-125">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="0a4c2-125">AzureRM.Insights</span></span>
* <span data-ttu-id="0a4c2-126">Problem #6833 och #7102 (området Diagnostikinställningar) har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="0a4c2-126">Fixed issues #6833 and #7102 (Diagnostic Settings area)</span></span>
    - <span data-ttu-id="0a4c2-127">Problem med standardnamnet, d.v.s. ”tjänsten” när diagnostikinställningar skapas och listas/hämtas</span><span class="sxs-lookup"><span data-stu-id="0a4c2-127">Issues with the default name, i.e. 'service', during creation and listing/getting of diagnostic settings</span></span>
    - <span data-ttu-id="0a4c2-128">Problem med att skapa diagnostikinställningar med kategorier</span><span class="sxs-lookup"><span data-stu-id="0a4c2-128">Issues creating diagnostic settings with categories</span></span>
* <span data-ttu-id="0a4c2-129">Utfasningsmeddelande har lagts till för tidsintervallsparametrar för mått</span><span class="sxs-lookup"><span data-stu-id="0a4c2-129">Added deprecation message for metrics time grains parameters</span></span>
    - <span data-ttu-id="0a4c2-130">Tidsintervallsparametrar går fortfarande att använda (det här är en bakåtkompatibel ändring), men de ignoreras i serverdelen eftersom endast PT1M är giltigt</span><span class="sxs-lookup"><span data-stu-id="0a4c2-130">Timegrains parameters are still being accepted (this is a non-breaking change,) but they are ignored in the backend since only PT1M is valid</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="0a4c2-131">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="0a4c2-131">AzureRM.Network</span></span>
* <span data-ttu-id="0a4c2-132">Ändringar i LoadBalancer-cmdletar</span><span class="sxs-lookup"><span data-stu-id="0a4c2-132">Changes to LoadBalancer cmdlets</span></span>
  - <span data-ttu-id="0a4c2-133">LoadBalancerInboundNatPoolConfig: parametrarna IdleTimeoutInMinutes, EnableFloatingIp och EnableTcpReset har lagts till</span><span class="sxs-lookup"><span data-stu-id="0a4c2-133">LoadBalancerInboundNatPoolConfig: added parameters IdleTimeoutInMinutes, EnableFloatingIp and EnableTcpReset</span></span>
  - <span data-ttu-id="0a4c2-134">LoadBalancerInboundNatRuleConfig: parametern EnableTcpReset har lagts till</span><span class="sxs-lookup"><span data-stu-id="0a4c2-134">LoadBalancerInboundNatRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="0a4c2-135">LoadBalancerRuleConfig: parametern EnableTcpReset har lagts till</span><span class="sxs-lookup"><span data-stu-id="0a4c2-135">LoadBalancerRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="0a4c2-136">LoadBalancerProbeConfig: stöd för värdet ”Https” för parameterprotokoll har lagts till</span><span class="sxs-lookup"><span data-stu-id="0a4c2-136">LoadBalancerProbeConfig: added support for value "Https" for parameter Protocol</span></span>
* <span data-ttu-id="0a4c2-137">Nya kommandon för den nya underresursen för LoadBalancers OutboundRule har lagts till</span><span class="sxs-lookup"><span data-stu-id="0a4c2-137">Added new commands for new LoadBalancer's subresource OutboundRule</span></span>
  - <span data-ttu-id="0a4c2-138">Add-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0a4c2-138">Add-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="0a4c2-139">Get-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0a4c2-139">Get-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="0a4c2-140">New-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0a4c2-140">New-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="0a4c2-141">Set-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0a4c2-141">Set-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="0a4c2-142">Remove-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0a4c2-142">Remove-AzureRmLoadBalancerOutboundRuleConfig</span></span>
* <span data-ttu-id="0a4c2-143">Ny HostedWorkloads-egenskap har lagts till för PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="0a4c2-143">Added new HostedWorkloads property for PSNetworkInterface</span></span>
* <span data-ttu-id="0a4c2-144">Nya cmdletar har lagts till för funktionen: Azure Firewall via ARM</span><span class="sxs-lookup"><span data-stu-id="0a4c2-144">Added new cmdlets for feature: Azure Firewall via ARM</span></span>
  - <span data-ttu-id="0a4c2-145">Get-AzureRmFirewall har lagts till</span><span class="sxs-lookup"><span data-stu-id="0a4c2-145">Added Get-AzureRmFirewall</span></span>
  - <span data-ttu-id="0a4c2-146">Set-AzureRmFirewall har lagts till</span><span class="sxs-lookup"><span data-stu-id="0a4c2-146">Added Set-AzureRmFirewall</span></span>
  - <span data-ttu-id="0a4c2-147">New-AzureRmFirewall har lagts till</span><span class="sxs-lookup"><span data-stu-id="0a4c2-147">Added New-AzureRmFirewall</span></span>
  - <span data-ttu-id="0a4c2-148">Remove-AzureRmFirewall har lagts till</span><span class="sxs-lookup"><span data-stu-id="0a4c2-148">Added Remove-AzureRmFirewall</span></span>
  - <span data-ttu-id="0a4c2-149">New-AzureRmFirewallApplicationRuleCollection har lagts till</span><span class="sxs-lookup"><span data-stu-id="0a4c2-149">Added New-AzureRmFirewallApplicationRuleCollection</span></span>
  - <span data-ttu-id="0a4c2-150">New-AzureRmFirewallApplicationRule har lagts till</span><span class="sxs-lookup"><span data-stu-id="0a4c2-150">Added New-AzureRmFirewallApplicationRule</span></span>
  - <span data-ttu-id="0a4c2-151">New-AzureRmFirewallNatRuleCollection har lagts till</span><span class="sxs-lookup"><span data-stu-id="0a4c2-151">Added New-AzureRmFirewallNatRuleCollection</span></span>
  - <span data-ttu-id="0a4c2-152">New-AzureRmFirewallNatRule har lagts till</span><span class="sxs-lookup"><span data-stu-id="0a4c2-152">Added New-AzureRmFirewallNatRule</span></span>
  - <span data-ttu-id="0a4c2-153">New-AzureRmFirewallNetworkRuleCollection har lagts till</span><span class="sxs-lookup"><span data-stu-id="0a4c2-153">Added New-AzureRmFirewallNetworkRuleCollection</span></span>
  - <span data-ttu-id="0a4c2-154">New-AzureRmFirewallNetworkRule har lagts till</span><span class="sxs-lookup"><span data-stu-id="0a4c2-154">Added New-AzureRmFirewallNetworkRule</span></span>
* <span data-ttu-id="0a4c2-155">Stöd för betrott rotcertifikat och konfiguration för autoskalning har lagts till i Application Gateway</span><span class="sxs-lookup"><span data-stu-id="0a4c2-155">Added support for Trusted Root certificate and Autoscale configuration in Application Gateway</span></span>
  - <span data-ttu-id="0a4c2-156">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="0a4c2-156">New Cmdlets added:</span></span>
      - <span data-ttu-id="0a4c2-157">Add-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="0a4c2-157">Add-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="0a4c2-158">Get-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="0a4c2-158">Get-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="0a4c2-159">New-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="0a4c2-159">New-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="0a4c2-160">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="0a4c2-160">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="0a4c2-161">Set-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="0a4c2-161">Set-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="0a4c2-162">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="0a4c2-162">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="0a4c2-163">New-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="0a4c2-163">New-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="0a4c2-164">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="0a4c2-164">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="0a4c2-165">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="0a4c2-165">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
  - <span data-ttu-id="0a4c2-166">Cmdletar har uppdaterats med valfri parameter – TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="0a4c2-166">Cmdlets updated with optonal parameter -TrustedRootCertificate</span></span>
      - <span data-ttu-id="0a4c2-167">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0a4c2-167">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="0a4c2-168">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0a4c2-168">Set-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="0a4c2-169">New-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="0a4c2-169">New-AzureRmApplicationGatewayBackendHttpSetting</span></span>
      - <span data-ttu-id="0a4c2-170">Set-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="0a4c2-170">Set-AzureRmApplicationGatewayBackendHttpSetting</span></span>
  - <span data-ttu-id="0a4c2-171">Cmdletar har uppdaterats med valfri parameter – AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="0a4c2-171">Cmdlets updated with optonal parameter -AutoscaleConfiguration</span></span>
      - <span data-ttu-id="0a4c2-172">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0a4c2-172">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="0a4c2-173">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0a4c2-173">Set-AzureRmApplicationGateway</span></span>
* <span data-ttu-id="0a4c2-174">Lägg till cmdlet för gränssnittsslutpunkten Get-AzureInterfaceEndpoint</span><span class="sxs-lookup"><span data-stu-id="0a4c2-174">Add cmdlet for Interface Endpoint Get-AzureInterfaceEndpoint</span></span>
* <span data-ttu-id="0a4c2-175">Stöd för flera adressprefix i ett undernät har lagts till.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-175">Added support for multiple address prefixes in a subnet.</span></span> <span data-ttu-id="0a4c2-176">Uppdaterade cmdletar:</span><span class="sxs-lookup"><span data-stu-id="0a4c2-176">Updated cmdlets:</span></span>
  - <span data-ttu-id="0a4c2-177">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="0a4c2-177">New-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="0a4c2-178">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="0a4c2-178">Set-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="0a4c2-179">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="0a4c2-179">Add-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="0a4c2-180">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="0a4c2-180">Get-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="0a4c2-181">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="0a4c2-181">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>
  - <span data-ttu-id="0a4c2-182">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="0a4c2-182">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="0a4c2-183">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="0a4c2-183">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="0a4c2-184">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="0a4c2-184">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="0a4c2-185">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="0a4c2-185">Add-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="0a4c2-186">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="0a4c2-186">New-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="0a4c2-187">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="0a4c2-187">Set-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="0a4c2-188">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="0a4c2-188">Add-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="0a4c2-189">New-AzureRmNetworkInterfaceIpConfig – Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="0a4c2-189">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="0a4c2-190">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="0a4c2-190">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="0a4c2-191">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="0a4c2-191">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="0a4c2-192">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="0a4c2-192">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="0a4c2-193">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="0a4c2-193">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="0a4c2-194">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="0a4c2-194">New-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="0a4c2-195">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="0a4c2-195">New-AzureRmNetworkInterface</span></span>
* <span data-ttu-id="0a4c2-196">Lägger till cmdletar för delegering av undernät.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-196">Adding cmdlets for subnet delegation.</span></span>
  - <span data-ttu-id="0a4c2-197">New-AzureRmDelegation: Skapar en ny delegering som kan läggas till i ett undernät</span><span class="sxs-lookup"><span data-stu-id="0a4c2-197">New-AzureRmDelegation: Creates a new delegation, which can be added to a subnet</span></span>
  - <span data-ttu-id="0a4c2-198">Remove-AzureRmDelegation: Hämtar ett undernät och tar bort det angivna delegeringsnamnet från undernätet</span><span class="sxs-lookup"><span data-stu-id="0a4c2-198">Remove-AzureRmDelegation: Takes in a subnet and removes the provided delegation name from that subnet</span></span>
  - <span data-ttu-id="0a4c2-199">Add-AzureRmDelegation: Hämtar ett undernät och lägger till det angivna tjänstnamnet som en delegering till undernätet</span><span class="sxs-lookup"><span data-stu-id="0a4c2-199">Add-AzureRmDelegation: Takes in a subnet and adds the provided service name as a delegation to that subnet</span></span>
  - <span data-ttu-id="0a4c2-200">Get-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="0a4c2-200">Get-AzureRmDelegation</span></span>
  - <span data-ttu-id="0a4c2-201">Get-AzureRmAvailableServiceDelegations</span><span class="sxs-lookup"><span data-stu-id="0a4c2-201">Get-AzureRmAvailableServiceDelegations</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="0a4c2-202">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0a4c2-202">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="0a4c2-203">Stöd för hanterad disk</span><span class="sxs-lookup"><span data-stu-id="0a4c2-203">Support for managed Managed disk</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="0a4c2-204">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="0a4c2-204">AzureRM.RedisCache</span></span>
* <span data-ttu-id="0a4c2-205">Insights-beroende har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-205">Updated Insights dependency.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="0a4c2-206">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="0a4c2-206">AzureRM.Resources</span></span>
* <span data-ttu-id="0a4c2-207">Uppdatera New-AzureRmResourceGroupDeployment med den nya parametern RollbackAction</span><span class="sxs-lookup"><span data-stu-id="0a4c2-207">Update New-AzureRmResourceGroupDeployment with new parameter RollbackAction</span></span>
    - <span data-ttu-id="0a4c2-208">Lägg till stöd för OnErrorDeployment med den nya parametern.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-208">Add support for OnErrorDeployment with the new parameter.</span></span>
* <span data-ttu-id="0a4c2-209">Stöd för hanterad identitet på principtilldelningar.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-209">Support managed identity on policy assignments.</span></span>
* <span data-ttu-id="0a4c2-210">Parametrar med standardvärden krävs inte längre när du tilldelar en princip med ”New-AzureRmPolicyAssignment”</span><span class="sxs-lookup"><span data-stu-id="0a4c2-210">Parameters with default values are no longer requred when assigning a policy with 'New-AzureRmPolicyAssignment'</span></span>
* <span data-ttu-id="0a4c2-211">Lägg till den nya cmdleten Get-AzureRmPolicyAlias för att hämta principalias</span><span class="sxs-lookup"><span data-stu-id="0a4c2-211">Add new cmdlet Get-AzureRmPolicyAlias for retrieving policy aliases</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="0a4c2-212">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="0a4c2-212">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="0a4c2-213">Problem #7161 har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="0a4c2-213">Fixed issue #7161</span></span>

#### <a name="azurermsignalr"></a><span data-ttu-id="0a4c2-214">AzureRM.SignalR</span><span class="sxs-lookup"><span data-stu-id="0a4c2-214">AzureRM.SignalR</span></span>
* <span data-ttu-id="0a4c2-215">Uppdatera SKU-namn till Free_F1 och Standard_S1</span><span class="sxs-lookup"><span data-stu-id="0a4c2-215">Update SKU names to Free_F1 and Standard_S1</span></span>
* <span data-ttu-id="0a4c2-216">Lägg till versionsfältet i PSSignalRResource-objektet och en anslutningssträng i PSSignalRKeys-objektet.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-216">Add version field to the PSSignalRResource object and connection string to the PSSignalRKeys object.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="0a4c2-217">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="0a4c2-217">AzureRM.Storage</span></span>
* <span data-ttu-id="0a4c2-218">Stöd för oföränderlighetsprincip i AzureRm.Storage</span><span class="sxs-lookup"><span data-stu-id="0a4c2-218">Support Immutability Policy in AzureRm.Storage</span></span> 
    - <span data-ttu-id="0a4c2-219">Remove-AzureRmStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="0a4c2-219">Remove-AzureRmStorageAccountNetworkRule</span></span>
    - <span data-ttu-id="0a4c2-220">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="0a4c2-220">Get-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="0a4c2-221">Update-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="0a4c2-221">Update-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="0a4c2-222">New-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="0a4c2-222">New-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="0a4c2-223">Remove-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="0a4c2-223">Remove-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="0a4c2-224">Add-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="0a4c2-224">Add-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="0a4c2-225">Remove-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="0a4c2-225">Remove-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="0a4c2-226">Set-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="0a4c2-226">Set-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="0a4c2-227">Get-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="0a4c2-227">Get-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="0a4c2-228">Remove-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="0a4c2-228">Remove-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="0a4c2-229">Lock-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="0a4c2-229">Lock-AzureRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="0a4c2-230">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="0a4c2-230">AzureRM.Websites</span></span>
* <span data-ttu-id="0a4c2-231">Två nya cmdletar har lagts till: Get-AzureRmDeletedWebApp och Restore-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="0a4c2-231">Added two new cmdlets: Get-AzureRmDeletedWebApp and Restore-AzureRmDeletedWebApp</span></span>
* <span data-ttu-id="0a4c2-232">New-AzureRmAppServicePlan – En HyperV-växel har lagts till för skapa en app service-plan med Windows-containrar</span><span class="sxs-lookup"><span data-stu-id="0a4c2-232">New-AzureRmAppServicePlan -HyperV switch is added for create app service plan with windows container</span></span>
* <span data-ttu-id="0a4c2-233">New-AzureRmWebApp/New-AzureRmWebAppSlot/Set-AzureRmWebApp/Set-AzureRmWebAppSlot – Nya parametrar (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) har lagts till för att skapa och hantera Windows-containerappar</span><span class="sxs-lookup"><span data-stu-id="0a4c2-233">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - New parameters (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) added for creating and managing windows container app</span></span>

## <a name="681---august-2018"></a><span data-ttu-id="0a4c2-234">6.8.1 – augusti 2018</span><span class="sxs-lookup"><span data-stu-id="0a4c2-234">6.8.1 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="0a4c2-235">Allmänt</span><span class="sxs-lookup"><span data-stu-id="0a4c2-235">General</span></span>
* <span data-ttu-id="0a4c2-236">Problem med standardresursgrupp som inte har konfigurerats har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-236">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="0a4c2-237">Uppdaterade Common Runtime-sammansättningar</span><span class="sxs-lookup"><span data-stu-id="0a4c2-237">Updated common runtime assemblies</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="0a4c2-238">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0a4c2-238">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="0a4c2-239">Problem med standardresursgrupp som inte har konfigurerats har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-239">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="0a4c2-240">Åtgärdat problem https://github.com/Azure/azure-powershell/issues/6603</span><span class="sxs-lookup"><span data-stu-id="0a4c2-240">Fixed issue https://github.com/Azure/azure-powershell/issues/6603</span></span>
    - <span data-ttu-id="0a4c2-241">Import-AzureRmApiManagementApi- och \*-AzureRmApiManagementCertificate-cmdletar kan nu hantera relativa sökvägar</span><span class="sxs-lookup"><span data-stu-id="0a4c2-241">Import-AzureRmApiManagementApi and \*-AzureRmApiManagementCertificate cmdlets now handle relative Paths</span></span>
* <span data-ttu-id="0a4c2-242">Åtgärdat problem https://github.com/Azure/azure-powershell/issues/6879</span><span class="sxs-lookup"><span data-stu-id="0a4c2-242">Fixed issue https://github.com/Azure/azure-powershell/issues/6879</span></span>
    - <span data-ttu-id="0a4c2-243">CertificateInformation är en inställbar egenskap som gör att Set-AzureRmApiManagement-cmdleten fungerar ordentligt.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-243">The CertificateInformation is a settable property allowing for Set-AzureRmApiManagement cmdlet to work property.</span></span> <span data-ttu-id="0a4c2-244">Åtgärdat genom uppgradering till NuGet för 4.0.4-preview</span><span class="sxs-lookup"><span data-stu-id="0a4c2-244">Fixed by upgrading to 4.0.4-preview nuget</span></span>
* <span data-ttu-id="0a4c2-245">Åtgärdat problem https://github.com/Azure/azure-powershell/issues/6853</span><span class="sxs-lookup"><span data-stu-id="0a4c2-245">Fixed issue https://github.com/Azure/azure-powershell/issues/6853</span></span>
    - <span data-ttu-id="0a4c2-246">Odata-filtret för sökning efter namn på produkt har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="0a4c2-246">Fixed the Odata filter for Search by Name on Product</span></span>
* <span data-ttu-id="0a4c2-247">Åtgärdat problem https://github.com/Azure/azure-powershell/issues/6814</span><span class="sxs-lookup"><span data-stu-id="0a4c2-247">Fixed issue https://github.com/Azure/azure-powershell/issues/6814</span></span>
    - <span data-ttu-id="0a4c2-248">Odata-filtret för sökning efter namn på API har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="0a4c2-248">Fixed the Odata filter for Search by Name on Api</span></span>
* <span data-ttu-id="0a4c2-249">Stöd har lagts till för AzureMonitor-loggare</span><span class="sxs-lookup"><span data-stu-id="0a4c2-249">Added support for AzureMonitor logger</span></span>


#### <a name="azurermcompute"></a><span data-ttu-id="0a4c2-250">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="0a4c2-250">AzureRM.Compute</span></span>
* <span data-ttu-id="0a4c2-251">Ett problem med att mål saknas i felutdata har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-251">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="0a4c2-252">Problem med lagringskontotyper för virtuell dator med en hanterad disk har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="0a4c2-252">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="0a4c2-253">Problem med standardresursgrupp som inte har konfigurerats har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-253">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="0a4c2-254">Åtgärda cmdletar för AEM-tillägg för andra miljöer, till exempel Azure Kina</span><span class="sxs-lookup"><span data-stu-id="0a4c2-254">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="0a4c2-255">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="0a4c2-255">AzureRM.Network</span></span>
* <span data-ttu-id="0a4c2-256">Standardvisning av cmdlet-utdata har ändrats för att visas i tabellvy</span><span class="sxs-lookup"><span data-stu-id="0a4c2-256">Changed default cmdlet output presentation to table view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="0a4c2-257">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="0a4c2-257">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="0a4c2-258">Åtgärda fel i Update-AzureRmPowerBIEmbeddedCapacity vid försök att skala pausad kapacitet</span><span class="sxs-lookup"><span data-stu-id="0a4c2-258">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>


#### <a name="azurermresources"></a><span data-ttu-id="0a4c2-259">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="0a4c2-259">AzureRM.Resources</span></span>
* <span data-ttu-id="0a4c2-260">Ett problem med att skapa hanterade program från MarketPlace har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-260">Fixed issue with creating managed applications from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="0a4c2-261">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="0a4c2-261">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="0a4c2-262">Åtgärdade problem</span><span class="sxs-lookup"><span data-stu-id="0a4c2-262">Fixed issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="0a4c2-263">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="0a4c2-263">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="0a4c2-264">Stöd har lagts till för trafikroutningsmetoden MultiValue</span><span class="sxs-lookup"><span data-stu-id="0a4c2-264">Added Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="0a4c2-265">Ny parameter, ”MaxReturn”, för MultiValue-routning</span><span class="sxs-lookup"><span data-stu-id="0a4c2-265">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="0a4c2-266">Stöd har lagts till för trafikroutningsmetod för undernät</span><span class="sxs-lookup"><span data-stu-id="0a4c2-266">Added Support for the Subnet routing method</span></span>
    - <span data-ttu-id="0a4c2-267">Stöd för IP-adressintervall (undernät) i slutpunkter</span><span class="sxs-lookup"><span data-stu-id="0a4c2-267">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="0a4c2-268">Stöd har lagts till för anpassade rubriker i profiler</span><span class="sxs-lookup"><span data-stu-id="0a4c2-268">Added Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="0a4c2-269">Stöd har lagts till för förväntade statuskodintervall i profiler</span><span class="sxs-lookup"><span data-stu-id="0a4c2-269">Added Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="0a4c2-270">Stöd har lagts till för anpassade rubriker i slutpunkter</span><span class="sxs-lookup"><span data-stu-id="0a4c2-270">Added Support for Custom Headers in endpoints</span></span>

## <a name="680---august-2018"></a><span data-ttu-id="0a4c2-271">6.8.0 – augusti 2018</span><span class="sxs-lookup"><span data-stu-id="0a4c2-271">6.8.0 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="0a4c2-272">Allmänt</span><span class="sxs-lookup"><span data-stu-id="0a4c2-272">General</span></span>
* <span data-ttu-id="0a4c2-273">Problem med standardresursgrupp som inte har konfigurerats har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-273">Fixed issue with default resource groups not being set.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="0a4c2-274">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="0a4c2-274">AzureRM.Profile</span></span>
* <span data-ttu-id="0a4c2-275">Utgångsegenskap har lagts till i token som returneras under Connect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="0a4c2-275">Added expiration property to tokens returned during Connect-AzureRmAccount</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="0a4c2-276">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="0a4c2-276">AzureRM.Compute</span></span>
* <span data-ttu-id="0a4c2-277">Ett problem med att mål saknas i felutdata har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-277">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="0a4c2-278">Problem med lagringskontotyper för virtuell dator med en hanterad disk har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="0a4c2-278">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="0a4c2-279">Åtgärda cmdletar för AEM-tillägg för andra miljöer, till exempel Azure Kina</span><span class="sxs-lookup"><span data-stu-id="0a4c2-279">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="0a4c2-280">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="0a4c2-280">AzureRM.IotHub</span></span>
* <span data-ttu-id="0a4c2-281">Korrigera exempel för New-AzureRmIotHubExportDevices och New-AzureRmIotHubImportDevices</span><span class="sxs-lookup"><span data-stu-id="0a4c2-281">Fix examples for New-AzureRmIotHubExportDevices and New-AzureRmIotHubImportDevices</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="0a4c2-282">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="0a4c2-282">AzureRM.Network</span></span>
* <span data-ttu-id="0a4c2-283">Standardmodeller har ändrats för att visas i tabellvy</span><span class="sxs-lookup"><span data-stu-id="0a4c2-283">Changed default models representation to table-view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="0a4c2-284">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="0a4c2-284">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="0a4c2-285">Åtgärda fel i Update-AzureRmPowerBIEmbeddedCapacity vid försök att skala pausad kapacitet</span><span class="sxs-lookup"><span data-stu-id="0a4c2-285">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="0a4c2-286">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="0a4c2-286">AzureRM.Resources</span></span>
* <span data-ttu-id="0a4c2-287">Ett problem med att skapa hanterade program från MarketPlace har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-287">Fixed issue with creating managed application from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="0a4c2-288">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="0a4c2-288">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="0a4c2-289">Korrigeringar för problem</span><span class="sxs-lookup"><span data-stu-id="0a4c2-289">Fix for issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="0a4c2-290">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="0a4c2-290">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="0a4c2-291">Stöd för trafikroutningsmetoden MultiValue</span><span class="sxs-lookup"><span data-stu-id="0a4c2-291">Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="0a4c2-292">Ny parameter, ”MaxReturn”, för MultiValue-routning</span><span class="sxs-lookup"><span data-stu-id="0a4c2-292">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="0a4c2-293">Stöd för trafikroutningsmetod för undernät</span><span class="sxs-lookup"><span data-stu-id="0a4c2-293">Support for the Subnet routing method</span></span>
    - <span data-ttu-id="0a4c2-294">Stöd för IP-adressintervall (undernät) i slutpunkter</span><span class="sxs-lookup"><span data-stu-id="0a4c2-294">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="0a4c2-295">Stöd för anpassade rubriker i profiler</span><span class="sxs-lookup"><span data-stu-id="0a4c2-295">Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="0a4c2-296">Stöd för förväntade statuskodintervall i profiler</span><span class="sxs-lookup"><span data-stu-id="0a4c2-296">Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="0a4c2-297">Stöd för anpassade rubriker i slutpunkter</span><span class="sxs-lookup"><span data-stu-id="0a4c2-297">Support for Custom Headers in endpoints</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="0a4c2-298">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="0a4c2-298">AzureRM.Websites</span></span>
* <span data-ttu-id="0a4c2-299">Problem med standardresursgrupp som inte har konfigurerats korrekt har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-299">Fixed issue with default resource group being set incorrectly.</span></span>

## <a name="670---august-2018"></a><span data-ttu-id="0a4c2-300">6.7.0 – augusti 2018</span><span class="sxs-lookup"><span data-stu-id="0a4c2-300">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="0a4c2-301">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="0a4c2-301">AzureRM.Profile</span></span>
* <span data-ttu-id="0a4c2-302">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-302">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="0a4c2-303">Lägg till användar-id i standardkontextnamnet för att undvika kontextkonflikter</span><span class="sxs-lookup"><span data-stu-id="0a4c2-303">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="0a4c2-304">Åtgärda problem med Clear-AzureRmContext som orsakade problem med att välja en kontext #6398</span><span class="sxs-lookup"><span data-stu-id="0a4c2-304">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="0a4c2-305">Aktivera den klientorganisationsdomän som ska skickas till parametern -TenantId för Connect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="0a4c2-305">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="0a4c2-306">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="0a4c2-306">Azure.Storage</span></span>
* <span data-ttu-id="0a4c2-307">Ta bort begränsningen på 5 TB för Azure-filresurskvoten</span><span class="sxs-lookup"><span data-stu-id="0a4c2-307">Remove the 5TB limitation for Azure File Share quota</span></span>
- <span data-ttu-id="0a4c2-308">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="0a4c2-308">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="0a4c2-309">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="0a4c2-309">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="0a4c2-310">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-310">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="0a4c2-311">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="0a4c2-311">Azure.AnalysisServices</span></span>
* <span data-ttu-id="0a4c2-312">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-312">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="0a4c2-313">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0a4c2-313">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="0a4c2-314">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-314">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="0a4c2-315">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="0a4c2-315">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="0a4c2-316">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-316">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="0a4c2-317">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="0a4c2-317">AzureRM.Automation</span></span>
* <span data-ttu-id="0a4c2-318">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-318">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="0a4c2-319">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="0a4c2-319">AzureRM.Backup</span></span>
* <span data-ttu-id="0a4c2-320">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-320">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="0a4c2-321">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="0a4c2-321">AzureRM.Batch</span></span>
* <span data-ttu-id="0a4c2-322">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-322">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="0a4c2-323">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="0a4c2-323">AzureRM.Billing</span></span>
* <span data-ttu-id="0a4c2-324">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-324">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="0a4c2-325">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="0a4c2-325">AzureRM.Cdn</span></span>
* <span data-ttu-id="0a4c2-326">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-326">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="0a4c2-327">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="0a4c2-327">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="0a4c2-328">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-328">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="0a4c2-329">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="0a4c2-329">AzureRM.Compute</span></span>
* <span data-ttu-id="0a4c2-330">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-330">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="0a4c2-331">Lägg till parametern EvictionPolicy i New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="0a4c2-331">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="0a4c2-332">Använd standardplatsen i DiskFileParameterSet för New-AzureRmVm om ingen plats har angetts.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-332">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="0a4c2-333">Korrigera parameterbeskrivningen i Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="0a4c2-333">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="0a4c2-334">Korrigera cmdleten Get-AzureRmVMDiskEncryptionStatus för vissa singlepass-relaterade scenarier</span><span class="sxs-lookup"><span data-stu-id="0a4c2-334">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="0a4c2-335">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="0a4c2-335">AzureRM.Consumption</span></span>
* <span data-ttu-id="0a4c2-336">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-336">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="0a4c2-337">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="0a4c2-337">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="0a4c2-338">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-338">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="0a4c2-339">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="0a4c2-339">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="0a4c2-340">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-340">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="0a4c2-341">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="0a4c2-341">AzureRM.DataFactories</span></span>
* <span data-ttu-id="0a4c2-342">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-342">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="0a4c2-343">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="0a4c2-343">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="0a4c2-344">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-344">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="0a4c2-345">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="0a4c2-345">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="0a4c2-346">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-346">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="0a4c2-347">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0a4c2-347">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="0a4c2-348">Korrigera felsökning när DebugPreference anges från powershell-kommandoraden</span><span class="sxs-lookup"><span data-stu-id="0a4c2-348">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="0a4c2-349">Uppdatera exemplet för Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="0a4c2-349">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="0a4c2-350">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-350">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="0a4c2-351">Uppdatera exemplet för Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="0a4c2-351">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="0a4c2-352">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="0a4c2-352">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="0a4c2-353">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-353">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="0a4c2-354">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="0a4c2-354">AzureRM.Dns</span></span>
* <span data-ttu-id="0a4c2-355">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-355">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="0a4c2-356">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="0a4c2-356">AzureRM.EventGrid</span></span>
* <span data-ttu-id="0a4c2-357">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-357">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="0a4c2-358">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="0a4c2-358">AzureRM.EventHub</span></span>
* <span data-ttu-id="0a4c2-359">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-359">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="0a4c2-360">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="0a4c2-360">AzureRM.HDInsight</span></span>
* <span data-ttu-id="0a4c2-361">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-361">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="0a4c2-362">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="0a4c2-362">AzureRM.Insights</span></span>
* <span data-ttu-id="0a4c2-363">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-363">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="0a4c2-364">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="0a4c2-364">AzureRM.IotHub</span></span>
* <span data-ttu-id="0a4c2-365">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-365">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="0a4c2-366">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0a4c2-366">AzureRM.KeyVault</span></span>
* <span data-ttu-id="0a4c2-367">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-367">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="0a4c2-368">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="0a4c2-368">AzureRM.LogicApp</span></span>
* <span data-ttu-id="0a4c2-369">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-369">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="0a4c2-370">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="0a4c2-370">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="0a4c2-371">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-371">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="0a4c2-372">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="0a4c2-372">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="0a4c2-373">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-373">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="0a4c2-374">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="0a4c2-374">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="0a4c2-375">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-375">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="0a4c2-376">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="0a4c2-376">AzureRM.Media</span></span>
* <span data-ttu-id="0a4c2-377">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-377">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="0a4c2-378">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="0a4c2-378">AzureRM.Network</span></span>
* <span data-ttu-id="0a4c2-379">Exempel för Set-AzureRmLocalNetworkGateway har lagts till</span><span class="sxs-lookup"><span data-stu-id="0a4c2-379">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="0a4c2-380">Exempel och beskrivningar för Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey och New-AzureRmVirtualNetworkGatewayConnection har lagts till</span><span class="sxs-lookup"><span data-stu-id="0a4c2-380">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="0a4c2-381">Exempel för Remove-AzureRmVirtualNetworkGatewayIpConfig och Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="0a4c2-381">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="0a4c2-382">Exempel för Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey har lagts till</span><span class="sxs-lookup"><span data-stu-id="0a4c2-382">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="0a4c2-383">Exempel för Set-AzureRmVirtualNetworkGatewayConnectionSharedKey har lagts till</span><span class="sxs-lookup"><span data-stu-id="0a4c2-383">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="0a4c2-384">Exempel för Set-AzureRmVirtualNetworkGatewayConnection har lagts till</span><span class="sxs-lookup"><span data-stu-id="0a4c2-384">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="0a4c2-385">Cmdletar för ApplicationSecurityGroup, RouteTable and Usage har genererats om med den senaste kodgeneratorn</span><span class="sxs-lookup"><span data-stu-id="0a4c2-385">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="0a4c2-386">Förtydligade ett felmeddelande för Get-AzureRmVirtualNetworkSubnetConfig vid försök att hämta ett undernät som inte avslutas</span><span class="sxs-lookup"><span data-stu-id="0a4c2-386">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="0a4c2-387">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="0a4c2-387">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="0a4c2-388">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-388">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="0a4c2-389">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="0a4c2-389">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="0a4c2-390">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-390">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="0a4c2-391">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="0a4c2-391">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="0a4c2-392">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-392">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="0a4c2-393">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="0a4c2-393">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="0a4c2-394">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-394">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="0a4c2-395">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0a4c2-395">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="0a4c2-396">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-396">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="0a4c2-397">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0a4c2-397">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="0a4c2-398">Lade till principfilter i cmdleten Get-AzureRmRecoveryServicesBackItem.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-398">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="0a4c2-399">Kommandot returnerar listan med säkerhetskopieringsobjekt som skyddas av det angivna princip-ID:t.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-399">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="0a4c2-400">Microsoft.Azure.Management.RecoveryServices.Backup uppdaterades till förhandsversionen av 3.0.0.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-400">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="0a4c2-401">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-401">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="0a4c2-402">Parametern TargetResourceGroupName lades till i Restore-AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-402">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="0a4c2-403">Den resursgrupp som de hanterade diskarna återställs till.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-403">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="0a4c2-404">Gäller för säkerhetskopiering av virtuell dator med hanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-404">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="0a4c2-405">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0a4c2-405">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="0a4c2-406">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-406">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="0a4c2-407">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="0a4c2-407">AzureRM.RedisCache</span></span>
* <span data-ttu-id="0a4c2-408">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-408">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="0a4c2-409">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="0a4c2-409">AzureRM.Relay</span></span>
* <span data-ttu-id="0a4c2-410">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-410">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="0a4c2-411">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="0a4c2-411">AzureRM.Resources</span></span>
* <span data-ttu-id="0a4c2-412">Distribution av supportmall i prenumerationsomfånget.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-412">Support template deployment at subscription scope.</span></span> <span data-ttu-id="0a4c2-413">Lägg till nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="0a4c2-413">Add new Cmdlets:</span></span>
    - <span data-ttu-id="0a4c2-414">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="0a4c2-414">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="0a4c2-415">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="0a4c2-415">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="0a4c2-416">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="0a4c2-416">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="0a4c2-417">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="0a4c2-417">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="0a4c2-418">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="0a4c2-418">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="0a4c2-419">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="0a4c2-419">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="0a4c2-420">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="0a4c2-420">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="0a4c2-421">Korrigera ett problem där fel inträffar när en kontext skickas till Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="0a4c2-421">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="0a4c2-422">Korrigera exempel i New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0a4c2-422">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="0a4c2-423">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-423">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="0a4c2-424">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="0a4c2-424">AzureRM.Scheduler</span></span>
* <span data-ttu-id="0a4c2-425">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-425">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="0a4c2-426">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="0a4c2-426">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="0a4c2-427">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-427">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="0a4c2-428">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0a4c2-428">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="0a4c2-429">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-429">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="0a4c2-430">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="0a4c2-430">AzureRM.Sql</span></span>
* <span data-ttu-id="0a4c2-431">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-431">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="0a4c2-432">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="0a4c2-432">AzureRM.Storage</span></span>
* <span data-ttu-id="0a4c2-433">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-433">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="0a4c2-434">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="0a4c2-434">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="0a4c2-435">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-435">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="0a4c2-436">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="0a4c2-436">AzureRM.Tags</span></span>
* <span data-ttu-id="0a4c2-437">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-437">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="0a4c2-438">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="0a4c2-438">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="0a4c2-439">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-439">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="0a4c2-440">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="0a4c2-440">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="0a4c2-441">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-441">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="0a4c2-442">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="0a4c2-442">AzureRM.Websites</span></span>
* <span data-ttu-id="0a4c2-443">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-443">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="0a4c2-444">6.6.0 – juli 2018</span><span class="sxs-lookup"><span data-stu-id="0a4c2-444">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="0a4c2-445">Allmänt</span><span class="sxs-lookup"><span data-stu-id="0a4c2-445">General</span></span>
* <span data-ttu-id="0a4c2-446">Alla hjälpfiler har uppdaterats för att ta med fullständiga parametertyper och korrekta indata-/utdatatyper.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-446">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="0a4c2-447">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="0a4c2-447">AzureRM.Profile</span></span>
* <span data-ttu-id="0a4c2-448">Common.Strategy-biblioteket har uppdaterats för att kunna verifiera att den aktuella konfigurationsfilen för en resurs är kompatibel med målresursen.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-448">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="0a4c2-449">ps1xml-typer har lagts till i Common.Storage</span><span class="sxs-lookup"><span data-stu-id="0a4c2-449">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="0a4c2-450">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="0a4c2-450">Azure.Storage</span></span>
* <span data-ttu-id="0a4c2-451">Lade till stöd för hämtning av lagringskontext från DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a4c2-451">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="0a4c2-452">Lade till Ps1XmlAttribute till utdatatypegenskaper för cmdletar.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-452">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="0a4c2-453">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0a4c2-453">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="0a4c2-454">Åtgärdat problem https://github.com/Azure/azure-powershell/issues/6370</span><span class="sxs-lookup"><span data-stu-id="0a4c2-454">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="0a4c2-455">En bugg har åtgärdats i Automapper för att översätta PsApiManagementApi till ApiContract</span><span class="sxs-lookup"><span data-stu-id="0a4c2-455">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="0a4c2-456">Åtgärdat problem https://github.com/Azure/azure-powershell/issues/6515</span><span class="sxs-lookup"><span data-stu-id="0a4c2-456">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="0a4c2-457">En bugg har åtgärdats i File.Save för att inte överbelasta kodningstypen</span><span class="sxs-lookup"><span data-stu-id="0a4c2-457">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="0a4c2-458">Åtgärdat problem https://github.com/Azure/azure-powershell/issues/6560</span><span class="sxs-lookup"><span data-stu-id="0a4c2-458">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="0a4c2-459">Har uppgraderats till Nuget-versionen 4.0.3 vilket åtgärdar mönsterundantaget på apiId</span><span class="sxs-lookup"><span data-stu-id="0a4c2-459">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="0a4c2-460">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="0a4c2-460">AzureRM.Compute</span></span>
* <span data-ttu-id="0a4c2-461">Åtgärda problem med fel vid skapandet av en virtuell dator med hjälp av DiskFileParameterSet i New-AzureRmVm på grund av namnbyte på PremiumLRS-lagringskontotypen.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-461">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="0a4c2-462">Åtgärda cmdleten Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="0a4c2-462">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="0a4c2-463">Uppdatera Get-AzureRmAvailabilitySet för att aktivera funktionen för att lista alla tillgänglighetsuppsättningar i en prenumeration.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-463">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="0a4c2-464">(Parametern ResouceGroupName är nu frivillig.)</span><span class="sxs-lookup"><span data-stu-id="0a4c2-464">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="0a4c2-465">Uppdatera SimpleParameterSet för "New-AzureRmVm" för att aktivera accelererat nätverk på berättigade virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-465">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="0a4c2-466">Uppdatera den enkla parameteruppsättningen för New-AzureRmVmss så att det inte går att skapa de virtuella datorerna när en användarangiven lastbalanserare redan finns.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-466">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="0a4c2-467">Uppdatera exempel för New-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="0a4c2-467">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="0a4c2-468">Lägg till exempel för "New-AzureRmVM"</span><span class="sxs-lookup"><span data-stu-id="0a4c2-468">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="0a4c2-469">Uppdatera beskrivning för Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="0a4c2-469">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="0a4c2-470">Uppdatera Exempel 1 för Set-AzureRmVMBginfoExtension för stavningskontroll och prefix.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-470">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="0a4c2-471">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="0a4c2-471">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="0a4c2-472">ADF .Net SDK-versionen har uppdaterats till 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-472">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="0a4c2-473">Stöd för delning av Integration Runtime (lokal installation) mellan datafabriker.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-473">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="0a4c2-474">Lägg till ny parameter – SharedIntegrationRuntimeResourceId i cmdleten Set-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-474">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="0a4c2-475">Lägg till ny valfri parameter – LinkedDataFactoryName i cmdleten Remove-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-475">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="0a4c2-476">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0a4c2-476">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="0a4c2-477">DataPlane SDK-versionen (Microsoft.Azure.DataLake.Store) har uppdaterats till 1.1.9</span><span class="sxs-lookup"><span data-stu-id="0a4c2-477">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="0a4c2-478">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="0a4c2-478">AzureRM.EventHub</span></span>
* <span data-ttu-id="0a4c2-479">Piping för InputObject and ResourceId i borttagna cmdletar har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="0a4c2-479">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="0a4c2-480">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="0a4c2-480">AzureRM.Insights</span></span>
* <span data-ttu-id="0a4c2-481">Formatering har åtgärdats för OutputType i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="0a4c2-481">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="0a4c2-482">Använda Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span><span class="sxs-lookup"><span data-stu-id="0a4c2-482">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="0a4c2-483">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0a4c2-483">AzureRM.KeyVault</span></span>
* <span data-ttu-id="0a4c2-484">Åtgärda problem med piping i Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="0a4c2-484">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="0a4c2-485">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="0a4c2-485">AzureRM.Network</span></span>
* <span data-ttu-id="0a4c2-486">Exempel har lagts till för LoadBalancerInboundNatPoolConfig-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-486">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="0a4c2-487">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="0a4c2-487">AzureRM.Resources</span></span>
* <span data-ttu-id="0a4c2-488">Åtgärda problem när både taggnamn och värde anges för "Get-AzureRmResource"</span><span class="sxs-lookup"><span data-stu-id="0a4c2-488">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="0a4c2-489">Åtgärda pipingscenario med "Set-AzureRmResource"</span><span class="sxs-lookup"><span data-stu-id="0a4c2-489">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="0a4c2-490">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="0a4c2-490">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="0a4c2-491">Piping för InputObject and ResourceId i borttagna cmdletar har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="0a4c2-491">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="0a4c2-492">några problem har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="0a4c2-492">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="0a4c2-493">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="0a4c2-493">AzureRM.Sql</span></span>
* <span data-ttu-id="0a4c2-494">Lägg till stöd för Server Advanced Threat Protection med följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="0a4c2-494">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="0a4c2-495">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="0a4c2-495">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="0a4c2-496">Lägg till stöd för Sårbarhetsbedömning med följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="0a4c2-496">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="0a4c2-497">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="0a4c2-497">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="0a4c2-498">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="0a4c2-498">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="0a4c2-499">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="0a4c2-499">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="0a4c2-500">Exempel i Remove-AzureRmSqlServerFirewallRule har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="0a4c2-500">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="0a4c2-501">Åtgärda felaktig hantering av datum och tid för andra kulturer än usa-baserade kulturer i Get-AzureSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="0a4c2-501">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="0a4c2-502">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="0a4c2-502">AzureRM.Storage</span></span>
* <span data-ttu-id="0a4c2-503">Lägg till Ps1XmlAttribute i utdatatypegenskaper för cmdletar</span><span class="sxs-lookup"><span data-stu-id="0a4c2-503">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="0a4c2-504">Visa utdata för cmdleten StorageAccount i tabellvyn</span><span class="sxs-lookup"><span data-stu-id="0a4c2-504">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="0a4c2-505">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0a4c2-505">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="0a4c2-506">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0a4c2-506">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="0a4c2-507">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0a4c2-507">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="0a4c2-508">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="0a4c2-508">AzureRM.Tags</span></span>
* <span data-ttu-id="0a4c2-509">Ta bort felaktig instruktion från hjälpen för cmdleten Tag</span><span class="sxs-lookup"><span data-stu-id="0a4c2-509">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="0a4c2-510">6.5.0 – juli 2018</span><span class="sxs-lookup"><span data-stu-id="0a4c2-510">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="0a4c2-511">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="0a4c2-511">AzureRM.Profile</span></span>
* <span data-ttu-id="0a4c2-512">Hjälp för ”Get-AzureRmContextAutosaveSetting” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="0a4c2-512">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="0a4c2-513">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="0a4c2-513">Azure.Storage</span></span>
* <span data-ttu-id="0a4c2-514">Stöd för uppladdning av blob eller fil med lässkyddad SAS-token</span><span class="sxs-lookup"><span data-stu-id="0a4c2-514">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="0a4c2-515">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="0a4c2-515">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="0a4c2-516">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="0a4c2-516">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="0a4c2-517">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="0a4c2-517">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="0a4c2-518">Lägg till den nödvändiga egenskapen ResourceGroupName i AS.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-518">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="0a4c2-519">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="0a4c2-519">AzureRM.Automation</span></span>
* <span data-ttu-id="0a4c2-520">Uppdatera hjälp och lägg till exempel för ”New-AzureRMAutomationSchedule”</span><span class="sxs-lookup"><span data-stu-id="0a4c2-520">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="0a4c2-521">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="0a4c2-521">AzureRM.Compute</span></span>
* <span data-ttu-id="0a4c2-522">Lägg till parametern -Tag förUpdate/New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="0a4c2-522">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="0a4c2-523">Lägg till exempel för ”Add-AzureRmVmssExtension”</span><span class="sxs-lookup"><span data-stu-id="0a4c2-523">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="0a4c2-524">Lägg till exempel för ”Remove-AzureRmVmssExtension”</span><span class="sxs-lookup"><span data-stu-id="0a4c2-524">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="0a4c2-525">Uppdatera hjälp för ”Set-AzureRmVMAccessExtension”</span><span class="sxs-lookup"><span data-stu-id="0a4c2-525">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="0a4c2-526">Uppdatera SimpleParameterSet för New-AzureRmVmss för att ställa in SinglePlacementGroup på falskt som standard och lägg till växlingsparametern ”SinglePlacementGroup” som gör att användare kan skapa VMSS i en enda placeringsgrupp.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-526">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="0a4c2-527">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="0a4c2-527">AzureRM.EventHub</span></span>
* <span data-ttu-id="0a4c2-528">En skrivskyddad egenskap, ”PendingReplicationOperationsCount”, har lagts till för klassen PSEventHubDRConfigurationAttributes som anger antalet väntande replikeringsåtgärder medan replikeringen pågår</span><span class="sxs-lookup"><span data-stu-id="0a4c2-528">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="0a4c2-529">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0a4c2-529">AzureRM.KeyVault</span></span>
* <span data-ttu-id="0a4c2-530">Uppdatera felmeddelande för Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="0a4c2-530">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="0a4c2-531">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="0a4c2-531">AzureRM.LogicApp</span></span>
* <span data-ttu-id="0a4c2-532">Felet ”parameteruppsättningen gick inte att matcha” har korrigerats i New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="0a4c2-532">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="0a4c2-533">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="0a4c2-533">AzureRM.Network</span></span>
* <span data-ttu-id="0a4c2-534">Aktivera peering mellan virtuella nätverk i flera klienter för Set/Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="0a4c2-534">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="0a4c2-535">Nedanstående cmdletar för Application Gateway har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="0a4c2-535">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="0a4c2-536">New-AzureRmApplicationGateway: EnableFIPS-flagga har lagts till för stöd för zoner</span><span class="sxs-lookup"><span data-stu-id="0a4c2-536">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="0a4c2-537">New-AzureRmApplicationGatewaySku: nya SKU:er, Standard_v2 och WAF_v2, har lagts till</span><span class="sxs-lookup"><span data-stu-id="0a4c2-537">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="0a4c2-538">Set-AzureRmApplicationGatewaySku: nya SKU:er, Standard_v2 och WAF_v2, har lagts till</span><span class="sxs-lookup"><span data-stu-id="0a4c2-538">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="0a4c2-539">RouteTable-cmdletar har återskapats med den senaste versionen av generatorn</span><span class="sxs-lookup"><span data-stu-id="0a4c2-539">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="0a4c2-540">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="0a4c2-540">AzureRM.Relay</span></span>
* <span data-ttu-id="0a4c2-541">Markdown-filer har uppdaterats och korrigerar problem med parameternamn i exemplet</span><span class="sxs-lookup"><span data-stu-id="0a4c2-541">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="0a4c2-542">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="0a4c2-542">AzureRM.Resources</span></span>
* <span data-ttu-id="0a4c2-543">Uppdatera cmdletar för rolltilldelning och rolldefinition:</span><span class="sxs-lookup"><span data-stu-id="0a4c2-543">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="0a4c2-544">Ta bort extra anrop för rolldefinitioner som görs som en del av sidindelning.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-544">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="0a4c2-545">Åtgärda Get-AzureRMRoleAssignment-cmdlet</span><span class="sxs-lookup"><span data-stu-id="0a4c2-545">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="0a4c2-546">Åtgärda parameterfunktioner för kommandot -ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="0a4c2-546">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="0a4c2-547">Åtgärda problem med ”Get-AzureRmResource” där ”-ResourceType”-parametern var skiftlägeskänsligt</span><span class="sxs-lookup"><span data-stu-id="0a4c2-547">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="0a4c2-548">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="0a4c2-548">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="0a4c2-549">Parametrar för att stoppa och hoppa över har lagts till i listan över cmdletar</span><span class="sxs-lookup"><span data-stu-id="0a4c2-549">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="0a4c2-550">Cmdletar för migrering från Standard- till Premium-namnområden har lagts till:</span><span class="sxs-lookup"><span data-stu-id="0a4c2-550">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="0a4c2-551">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="0a4c2-551">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="0a4c2-552">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="0a4c2-552">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="0a4c2-553">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="0a4c2-553">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="0a4c2-554">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="0a4c2-554">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="0a4c2-555">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="0a4c2-555">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="0a4c2-556">En skrivskyddad egenskap, ”PendingReplicationOperationsCount” har lagts till för klassen PSServiceBusDRConfigurationAttributes som anger antalet väntande replikeringsåtgärder medan replikeringen pågår</span><span class="sxs-lookup"><span data-stu-id="0a4c2-556">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="0a4c2-557">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0a4c2-557">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="0a4c2-558">Uppdatera exempel för ”New-AzureRmServiceFabricCluster”</span><span class="sxs-lookup"><span data-stu-id="0a4c2-558">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="0a4c2-559">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="0a4c2-559">AzureRM.Sql</span></span>
* <span data-ttu-id="0a4c2-560">Nya cmdletar för Management.Sql som gör att kunderna kan lägga till certifikat för transparent datakryptering till SQL Server-instans eller en hanterad instans har lagts till</span><span class="sxs-lookup"><span data-stu-id="0a4c2-560">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="0a4c2-561">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="0a4c2-561">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="0a4c2-562">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="0a4c2-562">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="0a4c2-563">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="0a4c2-563">AzureRM.Websites</span></span>
* <span data-ttu-id="0a4c2-564">När `Set-AzureRmWebApp -AssignIdentity` och `Set-AzureRmWebAppSlot -AssignIdentity` är inställda på falskt tar de nu bort identitetsegenskapen från platsobjektet. Även förhandsgranskningstaggen tas bort.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-564">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="0a4c2-565">`Get-AzureRmWebAppMetrics`, `Get-AzureRmAppServicePlanMetrics`-exempel har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="0a4c2-565">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="0a4c2-566">`Set-AzureRmWebApp -PhpVersion` har stöd för ”av” som en giltig php-version</span><span class="sxs-lookup"><span data-stu-id="0a4c2-566">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="0a4c2-567">6.4.0 – juli 2018</span><span class="sxs-lookup"><span data-stu-id="0a4c2-567">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="0a4c2-568">Allmänt</span><span class="sxs-lookup"><span data-stu-id="0a4c2-568">General</span></span>
* <span data-ttu-id="0a4c2-569">Formatering av OutputType i hjälpfiler har korrigerats för de flesta moduler</span><span class="sxs-lookup"><span data-stu-id="0a4c2-569">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="0a4c2-570">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="0a4c2-570">AzureRM.Profile</span></span>
* <span data-ttu-id="0a4c2-571">Ps1Xml-attribut har lagts till för grundläggande utdatatyper</span><span class="sxs-lookup"><span data-stu-id="0a4c2-571">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="0a4c2-572">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="0a4c2-572">AzureRM.Compute</span></span>
* <span data-ttu-id="0a4c2-573">IP-tagg-funktioner för VMSS</span><span class="sxs-lookup"><span data-stu-id="0a4c2-573">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="0a4c2-574">"New-AzureRmVmssIpTagConfig"-cmdlet har lagts till</span><span class="sxs-lookup"><span data-stu-id="0a4c2-574">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="0a4c2-575">IpTag-parameter har lagts till för New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="0a4c2-575">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="0a4c2-576">Automatisk återställningsfunktion för operativsystem för VMSS</span><span class="sxs-lookup"><span data-stu-id="0a4c2-576">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="0a4c2-577">DisableAutoRollback-parametrar har lagts till för New-AzureRmVmssConfig och Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="0a4c2-577">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="0a4c2-578">Funktion för uppgraderingshistorik för operativsystem för Vmss</span><span class="sxs-lookup"><span data-stu-id="0a4c2-578">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="0a4c2-579">OSUpgradeHistory-växlingsparametern har lagts till för Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="0a4c2-579">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="0a4c2-580">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="0a4c2-580">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="0a4c2-581">Lägg till stöd för katalog-ACL:er med hjälp av följande kommandon:</span><span class="sxs-lookup"><span data-stu-id="0a4c2-581">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="0a4c2-582">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="0a4c2-582">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="0a4c2-583">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="0a4c2-583">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="0a4c2-584">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="0a4c2-584">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="0a4c2-585">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0a4c2-585">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="0a4c2-586">Lägg till stöd för annullering och förloppsspårning för Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="0a4c2-586">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="0a4c2-587">Lägg till stöd för annullering för Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="0a4c2-587">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="0a4c2-588">Åtgärda tömning av felsökningsmeddelanden för cmdletar som gör rekursiva åtgärder</span><span class="sxs-lookup"><span data-stu-id="0a4c2-588">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="0a4c2-589">Åtgärda platsen för testning av DataLake-cmdletar</span><span class="sxs-lookup"><span data-stu-id="0a4c2-589">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="0a4c2-590">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="0a4c2-590">AzureRM.EventHub</span></span>
* <span data-ttu-id="0a4c2-591">Parametrar för optimalt maxantal har lagts till i liståtgärds-cmdletarna Get-AzureRmEventHub och Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="0a4c2-591">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="0a4c2-592">Ett problem i New-AzureRmEventHub-cmdleten har åtgärdats där minst en parameter behövdes när du skapade en ny EventHub.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-592">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="0a4c2-593">Angiven standardparameter har ställts in.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-593">Provided Default Parameter set.</span></span>
* <span data-ttu-id="0a4c2-594">Valfri parameter för KeyValue har lagts till för New-AzureRmEventHubKey-cmdleten, vilket gör det möjligt att ange KeyValue.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-594">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="0a4c2-595">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0a4c2-595">AzureRM.KeyVault</span></span>
* <span data-ttu-id="0a4c2-596">Åtgärda problem där alla resurser returnerades av Get-AzureRmKeyVault-taggen</span><span class="sxs-lookup"><span data-stu-id="0a4c2-596">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="0a4c2-597">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="0a4c2-597">AzureRM.Network</span></span>
* <span data-ttu-id="0a4c2-598">Gör nya SKU:er tillgängliga för zonredundanta VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="0a4c2-598">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="0a4c2-599">Nya kommandon har lagts till för funktionen: ExpressRoute Partner APIs via ARM</span><span class="sxs-lookup"><span data-stu-id="0a4c2-599">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="0a4c2-600">Get-AzureRmExpressRouteCrossConnection har lagts till</span><span class="sxs-lookup"><span data-stu-id="0a4c2-600">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="0a4c2-601">Set-AzureRmExpressRouteCrossConnection har lagts till</span><span class="sxs-lookup"><span data-stu-id="0a4c2-601">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="0a4c2-602">Add-AzureRmExpressRouteCrossConnectionPeering har lagts till</span><span class="sxs-lookup"><span data-stu-id="0a4c2-602">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="0a4c2-603">Get-AzureRmExpressRouteCrossConnectionPeering har lagts till</span><span class="sxs-lookup"><span data-stu-id="0a4c2-603">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="0a4c2-604">Remove-AzureRmExpressRouteCrossConnectionPeering har lagts till</span><span class="sxs-lookup"><span data-stu-id="0a4c2-604">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="0a4c2-605">Get-AzureRMExpressRouteCrossConnectionArpTable har lagts till</span><span class="sxs-lookup"><span data-stu-id="0a4c2-605">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="0a4c2-606">Get-AzureRMExpressRouteCrossConnectionRouteTable har lagts till</span><span class="sxs-lookup"><span data-stu-id="0a4c2-606">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="0a4c2-607">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary har lagts till</span><span class="sxs-lookup"><span data-stu-id="0a4c2-607">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="0a4c2-608">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0a4c2-608">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="0a4c2-609">Get-AzureRmRecoveryServicesBackupStatus-cmdlet har lagts till.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-609">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="0a4c2-610">Denna cmdlet tar ett ID för virtuell dator och kontrollerar om den virtuella datorn skyddas av ett valv i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-610">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="0a4c2-611">Om ett sådant valv finns returnerar cmdleten valvinformationen.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-611">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="0a4c2-612">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="0a4c2-612">AzureRM.Resources</span></span>
* <span data-ttu-id="0a4c2-613">Uppdatera Get-AzureRmPolicyAssignment-cmdletar:</span><span class="sxs-lookup"><span data-stu-id="0a4c2-613">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="0a4c2-614">Lägg till stöd för att lista -Scope-värden på hanteringsgruppsnivå</span><span class="sxs-lookup"><span data-stu-id="0a4c2-614">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="0a4c2-615">Lägg till stöd för hämtning av enskilda tilldelningar med -Scope-värden på hanteringsgruppsnivå.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-615">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="0a4c2-616">Lägg till växlar för -Effective och -All till kontrollparametrar</span><span class="sxs-lookup"><span data-stu-id="0a4c2-616">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="0a4c2-617">Uppdatera Get/New/Remove/Set-AzureRmPolicyDefinition-cmdletar</span><span class="sxs-lookup"><span data-stu-id="0a4c2-617">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="0a4c2-618">Lägg till parameter för -ManagementGroupName om du vill tillämpa åtgärder för en viss hanteringsgrupp</span><span class="sxs-lookup"><span data-stu-id="0a4c2-618">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="0a4c2-619">Lägg till parameter för -SubscriptionId om du vill tillämpa åtgärder för en viss prenumeration</span><span class="sxs-lookup"><span data-stu-id="0a4c2-619">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="0a4c2-620">Uppdatera Get/New/Remove/Set-AzureRmPolicySetDefinition-cmdletar</span><span class="sxs-lookup"><span data-stu-id="0a4c2-620">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="0a4c2-621">Lägg till parameter för -ManagementGroupName om du vill tillämpa åtgärder för en viss hanteringsgrupp</span><span class="sxs-lookup"><span data-stu-id="0a4c2-621">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="0a4c2-622">Lägg till parameter för -SubscriptionId om du vill tillämpa åtgärder för en viss prenumeration</span><span class="sxs-lookup"><span data-stu-id="0a4c2-622">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="0a4c2-623">Lägg till stöd för hemliga KeyVault-referenser i parametrar när du använder "TemplateParameterObject" i "New-AzureRmResourceGroupDeployment"</span><span class="sxs-lookup"><span data-stu-id="0a4c2-623">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="0a4c2-624">Åtgärda problem med att "-EndDate"-parametern ignorerades på grund av "New-AzureRmADAppCredential"</span><span class="sxs-lookup"><span data-stu-id="0a4c2-624">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="0a4c2-625">Åtgärda problem med att felaktig URL användes i "New-AzureRmADAppCredential" vid begäran</span><span class="sxs-lookup"><span data-stu-id="0a4c2-625">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="0a4c2-626">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="0a4c2-626">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="0a4c2-627">Valfri parameter för -KeyValue har lagts till för New-AzureRmServiceBusKey-cmdleten, vilket gör det möjligt att ange KeyValue.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-627">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="0a4c2-628">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="0a4c2-628">AzureRM.Sql</span></span>
* <span data-ttu-id="0a4c2-629">Användardefinierade återställningspunkter har klargjorts för SQLDW i New-AzureRmSqlDatabaseRestorePoint-hjälpen</span><span class="sxs-lookup"><span data-stu-id="0a4c2-629">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="0a4c2-630">Dokumentationen om parametern -ComputeGeneration har uppdaterats i fler cmdletar</span><span class="sxs-lookup"><span data-stu-id="0a4c2-630">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="0a4c2-631">6.3.0 – juni 2018</span><span class="sxs-lookup"><span data-stu-id="0a4c2-631">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="0a4c2-632">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="0a4c2-632">AzureRM.Profile</span></span>
* <span data-ttu-id="0a4c2-633">Uppdaterade felmeddelanden för Enable-AzureRmContextAutoSave</span><span class="sxs-lookup"><span data-stu-id="0a4c2-633">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="0a4c2-634">Skapa en kontext för varje prenumeration när du kör ”Connect-AzureRmAccount” utan tidigare kontext</span><span class="sxs-lookup"><span data-stu-id="0a4c2-634">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="0a4c2-635">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="0a4c2-635">Azure.Storage</span></span>
* <span data-ttu-id="0a4c2-636">Ytterligare information om parametern -Permissions har lagts till i hjälpfilerna.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-636">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="0a4c2-637">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="0a4c2-637">AzureRM.Compute</span></span>
* <span data-ttu-id="0a4c2-638">”Get-AzureRmVmDiskEncryptionStatus” korrigerar ett problem för virtuella datorer utan datadiskar</span><span class="sxs-lookup"><span data-stu-id="0a4c2-638">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="0a4c2-639">Uppdatera version av klientbibliotek för Compute för att korrigera följande cmdletar</span><span class="sxs-lookup"><span data-stu-id="0a4c2-639">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="0a4c2-640">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="0a4c2-640">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="0a4c2-641">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="0a4c2-641">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="0a4c2-642">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="0a4c2-642">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="0a4c2-643">Följande cmdletar har åtgärdats för att visa ”Åtgärds-ID” och ”Åtgärdsstatus” på ett korrekt sätt:</span><span class="sxs-lookup"><span data-stu-id="0a4c2-643">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="0a4c2-644">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="0a4c2-644">Start-AzureRmVM</span></span>
    - <span data-ttu-id="0a4c2-645">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="0a4c2-645">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="0a4c2-646">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="0a4c2-646">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="0a4c2-647">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="0a4c2-647">Set-AzureRmVM</span></span>
    - <span data-ttu-id="0a4c2-648">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="0a4c2-648">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="0a4c2-649">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="0a4c2-649">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="0a4c2-650">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="0a4c2-650">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="0a4c2-651">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="0a4c2-651">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="0a4c2-652">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="0a4c2-652">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="0a4c2-653">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="0a4c2-653">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="0a4c2-654">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="0a4c2-654">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="0a4c2-655">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="0a4c2-655">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="0a4c2-656">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="0a4c2-656">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="0a4c2-657">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="0a4c2-657">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="0a4c2-658">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="0a4c2-658">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="0a4c2-659">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="0a4c2-659">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="0a4c2-660">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="0a4c2-660">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="0a4c2-661">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="0a4c2-661">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="0a4c2-662">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="0a4c2-662">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="0a4c2-663">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="0a4c2-663">AzureRM.EventGrid</span></span>
* <span data-ttu-id="0a4c2-664">Ta bort verifieringsvillkoren ValidateNotNullOrEmpty för SubjectBeginsWith/SubjectEndsWith i cmdleten Update-AzureRmEventGridSubscription för att ändra de här parametrarna till en tom sträng om det behövs.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-664">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="0a4c2-665">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0a4c2-665">AzureRM.KeyVault</span></span>
* <span data-ttu-id="0a4c2-666">Åtgärda problem där inga taggar returneras när Get-AzureRmKeyVault -Tag körs</span><span class="sxs-lookup"><span data-stu-id="0a4c2-666">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="0a4c2-667">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="0a4c2-667">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="0a4c2-668">Offentlig lansering av cmdletar för Policy Insights</span><span class="sxs-lookup"><span data-stu-id="0a4c2-668">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="0a4c2-669">Använd API-version 2018-04-04</span><span class="sxs-lookup"><span data-stu-id="0a4c2-669">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="0a4c2-670">Lägg till PolicyDefinitionReferenceId i resultaten för Get-AzureRmPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="0a4c2-670">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="0a4c2-671">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0a4c2-671">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="0a4c2-672">Parametern -Vault har lagts till i cmdletarna för RecoveryServices.Backup.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-672">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="0a4c2-673">När den godkänns åsidosätts cmdleten Set-AzureRmRecoveryServicesContext.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-673">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="0a4c2-674">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="0a4c2-674">AzureRM.Sql</span></span>
* <span data-ttu-id="0a4c2-675">Exemplet i hjälpfilen för Get-AzureRmSqlDatabaseExpanded har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="0a4c2-675">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="0a4c2-676">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="0a4c2-676">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="0a4c2-677">Hjälpfilen för Add-AzureRmTrafficManagerEndpointConfig har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="0a4c2-677">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="0a4c2-678">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="0a4c2-678">AzureRM.Websites</span></span>
* <span data-ttu-id="0a4c2-679">”Set-AzureRmWebApp” har uppdaterats så att den inte skriver över appinställningarna när du använder -AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="0a4c2-679">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="0a4c2-680">”New-AzureRMWebAppSlot” har uppdaterats för att visa att AppServicePlan är en valfri parameter</span><span class="sxs-lookup"><span data-stu-id="0a4c2-680">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="0a4c2-681">6.2.1 – juni 2018</span><span class="sxs-lookup"><span data-stu-id="0a4c2-681">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="0a4c2-682">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="0a4c2-682">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="0a4c2-683">PSWorkspace-modellen har uppdaterats för att tillåta att nätverket använder typ som en parameter</span><span class="sxs-lookup"><span data-stu-id="0a4c2-683">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="0a4c2-684">6.2.0 – juni 2018</span><span class="sxs-lookup"><span data-stu-id="0a4c2-684">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="0a4c2-685">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="0a4c2-685">AzureRM.Profile</span></span>
* <span data-ttu-id="0a4c2-686">Åtgärda problemet med att version 10.0.3 av Newtonsoft.Json inte lästes in vid modulimporten</span><span class="sxs-lookup"><span data-stu-id="0a4c2-686">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="0a4c2-687">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="0a4c2-687">AzureRM.Compute</span></span>
* <span data-ttu-id="0a4c2-688">VMSS VM-uppdateringsfunktion</span><span class="sxs-lookup"><span data-stu-id="0a4c2-688">VMSS VM Update feature</span></span>
    - <span data-ttu-id="0a4c2-689">Cmdletarna Update-AzureRmVmssVM och New-AzureRmVMDataDisk har lagts till</span><span class="sxs-lookup"><span data-stu-id="0a4c2-689">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="0a4c2-690">Lägg till parametern VirtualMachineScaleSetVM till cmdleten Add-AzureRmVMDataDisk så att det går att lägga till en datadisk i den virtuella Vmss-datorn.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-690">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="0a4c2-691">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="0a4c2-691">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="0a4c2-692">SDK:n för ADF .Net har uppdaterats till version 0.8.0-preview som innehåller följande ändringar:</span><span class="sxs-lookup"><span data-stu-id="0a4c2-692">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="0a4c2-693">Åtgärden för att konfigurera fabrikslagringsplatsen har lagts till</span><span class="sxs-lookup"><span data-stu-id="0a4c2-693">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="0a4c2-694">QuickBooks LinkedService har uppdaterats för att visa egenskaperna consumerKey och consumerSecret</span><span class="sxs-lookup"><span data-stu-id="0a4c2-694">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="0a4c2-695">Flera modelltyper från SecretBase till Object har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="0a4c2-695">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="0a4c2-696">Utlösaren Blob Events har lagts till</span><span class="sxs-lookup"><span data-stu-id="0a4c2-696">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="0a4c2-697">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0a4c2-697">AzureRM.KeyVault</span></span>
* <span data-ttu-id="0a4c2-698">Uppdatera dokumentation med exempel på utdata</span><span class="sxs-lookup"><span data-stu-id="0a4c2-698">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="0a4c2-699">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="0a4c2-699">AzureRM.Network</span></span>
* <span data-ttu-id="0a4c2-700">Aktivera Trafikanalys-parametrar på Network Watcher-cmdletar</span><span class="sxs-lookup"><span data-stu-id="0a4c2-700">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="0a4c2-701">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="0a4c2-701">AzureRM.Resources</span></span>
* <span data-ttu-id="0a4c2-702">Åtgärda problemet med egenskapen "Properties" för objekt(en) "PSResource" som returneras från "Get-AzureRmResource"</span><span class="sxs-lookup"><span data-stu-id="0a4c2-702">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="0a4c2-703">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="0a4c2-703">AzureRM.Scheduler</span></span>
* <span data-ttu-id="0a4c2-704">Åtgärda problemet med att nya autentiseringsvärden inte anges vid uppdatering av ServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="0a4c2-704">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="0a4c2-705">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="0a4c2-705">AzureRM.Sql</span></span>
* <span data-ttu-id="0a4c2-706">Följande cmdletar har uppdaterats med valfri LicenseType-parameter</span><span class="sxs-lookup"><span data-stu-id="0a4c2-706">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="0a4c2-707">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0a4c2-707">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="0a4c2-708">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="0a4c2-708">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="0a4c2-709">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="0a4c2-709">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="0a4c2-710">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="0a4c2-710">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="0a4c2-711">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0a4c2-711">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="0a4c2-712">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="0a4c2-712">AzureRM.Websites</span></span>
* <span data-ttu-id="0a4c2-713">New-AzureRMWebApp har uppdaterats för att använda vanliga algoritmer från biblioteket Strategy.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-713">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="0a4c2-714">6.1.0 – maj 2018</span><span class="sxs-lookup"><span data-stu-id="0a4c2-714">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="0a4c2-715">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="0a4c2-715">AzureRM.Profile</span></span>
* <span data-ttu-id="0a4c2-716">Åtgärda problem där en körning av Clear-AzureRmContext skulle bevara en tom kontext med namnet på den föregående standardkontexten som gjorde att användaren inte kunde skapa en ny kontext med det gamla namnet</span><span class="sxs-lookup"><span data-stu-id="0a4c2-716">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="0a4c2-717">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="0a4c2-717">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="0a4c2-718">Aktivera Gateway associerings- och avassocieringsåtgärder på AS.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-718">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="0a4c2-719">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0a4c2-719">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="0a4c2-720">Stöd för ApiVersions, ApiReleases och ApiRevisions har lagts till</span><span class="sxs-lookup"><span data-stu-id="0a4c2-720">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="0a4c2-721">Stöd för serverdelen på ServiceFabric har lagts till</span><span class="sxs-lookup"><span data-stu-id="0a4c2-721">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="0a4c2-722">Stöd för Application Insights-loggare har lagts till</span><span class="sxs-lookup"><span data-stu-id="0a4c2-722">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="0a4c2-723">Stöd för att identifiera SKU:n ”Basic” som en giltig SKU för Api Management-tjänsten har lagts till</span><span class="sxs-lookup"><span data-stu-id="0a4c2-723">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="0a4c2-724">Stöd för att installera certifikat som utfärdats av privata certifikatutfärdare som rot eller certifikatutfärdare har lagts till</span><span class="sxs-lookup"><span data-stu-id="0a4c2-724">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="0a4c2-725">Stöd för att godkänna anpassade SSL-certifikat via KeyVault och flera proxy-värdnamn har lagts till</span><span class="sxs-lookup"><span data-stu-id="0a4c2-725">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="0a4c2-726">Stöd för MSI-identitet har lagts till</span><span class="sxs-lookup"><span data-stu-id="0a4c2-726">Added support for MSI identity</span></span>
* <span data-ttu-id="0a4c2-727">Stöd för att godkänna principer via URL har lagts till. Obs! Följande cmdletar blir inaktuella i framtida versioner</span><span class="sxs-lookup"><span data-stu-id="0a4c2-727">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="0a4c2-728">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="0a4c2-728">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="0a4c2-729">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="0a4c2-729">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="0a4c2-730">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="0a4c2-730">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="0a4c2-731">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="0a4c2-731">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="0a4c2-732">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="0a4c2-732">AzureRM.Batch</span></span>
* <span data-ttu-id="0a4c2-733">Släpp nya cmdleten Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="0a4c2-733">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="0a4c2-734">Släpp nya cmdleten Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="0a4c2-734">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="0a4c2-735">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="0a4c2-735">AzureRM.Consumption</span></span>
* <span data-ttu-id="0a4c2-736">Lägg till nya parametrar Expand, ResourceGroup, InstanceName, InstanceId, Tags och Top på cmdleten Get-AzureRmConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="0a4c2-736">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="0a4c2-737">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0a4c2-737">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="0a4c2-738">Åtgärda exempel för Export AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="0a4c2-738">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="0a4c2-739">Åtgärda undantag för null-parameter för rekursivt ärende i Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="0a4c2-739">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="0a4c2-740">Åtgärda hjälpfilerna för Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="0a4c2-740">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="0a4c2-741">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="0a4c2-741">AzureRM.Network</span></span>
* <span data-ttu-id="0a4c2-742">Öka nätverkets SDK-version från förhandsversionen 18.0.0 till förhandsversionen 19.0.0</span><span class="sxs-lookup"><span data-stu-id="0a4c2-742">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="0a4c2-743">Cmdlet har lagts till för att skapa protokollinformation</span><span class="sxs-lookup"><span data-stu-id="0a4c2-743">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="0a4c2-744">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="0a4c2-744">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="0a4c2-745">Cmdlet har lagts till för att lägga till en ny kretsanslutning till en befintlig expressroute-krets.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-745">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="0a4c2-746">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="0a4c2-746">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="0a4c2-747">Cmdlet har lagts till för att ta bort en kretsanslutning från en befintlig expressroute-krets.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-747">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="0a4c2-748">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="0a4c2-748">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="0a4c2-749">Cmdlet har lagts till för att hämta en kretsanslutning</span><span class="sxs-lookup"><span data-stu-id="0a4c2-749">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="0a4c2-750">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="0a4c2-750">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="0a4c2-751">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0a4c2-751">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="0a4c2-752">Användning med serverautentisering med genererade certifikat (problem #5998) har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="0a4c2-752">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="0a4c2-753">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="0a4c2-753">AzureRM.Sql</span></span>
* <span data-ttu-id="0a4c2-754">Cmdletar för granskning för att ta bort AuditActions eller AuditActionGroups har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="0a4c2-754">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="0a4c2-755">Åtgärdade problem med Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy vid konfigurering av en ny flexibel bevarandeprincip där kommandot misslyckas med ett meddelande om att konfigurering av långsiktig bevarandeprincip med Azure Recovery Service-valv och principen inte längre stöds,</span><span class="sxs-lookup"><span data-stu-id="0a4c2-755">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="0a4c2-756">och att en begäran med den nya flexibla bevarandeprincipen ska skickas.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-756">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="0a4c2-757">Uppdatera alla Azure Sql Database/ElasticPool Creation/Update-relaterade cmdletar för att använda det nya databas-API:et som stöder SKU-egenskaper för skalnings- och nivårelaterade egenskaper.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-757">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="0a4c2-758">Cmdletar har uppdaterats, inklusive:</span><span class="sxs-lookup"><span data-stu-id="0a4c2-758">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="0a4c2-759">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0a4c2-759">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="0a4c2-760">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="0a4c2-760">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="0a4c2-761">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="0a4c2-761">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="0a4c2-762">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="0a4c2-762">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="0a4c2-763">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0a4c2-763">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="0a4c2-764">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="0a4c2-764">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="0a4c2-765">Uppdatera parametrarna för Get-AzureRmTrafficManagerProfile så att ResourceGroupName-parametern blir obligatorisk när du använder Name-parametern.</span><span class="sxs-lookup"><span data-stu-id="0a4c2-765">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
