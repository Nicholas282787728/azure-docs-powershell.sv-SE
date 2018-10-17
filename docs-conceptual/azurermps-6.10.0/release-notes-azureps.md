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
ms.openlocfilehash: 6a33d1a85fc61d0281bf1183163185b0dc4d3a12
ms.sourcegitcommit: a749eb729f583c9d0dd86141bbd04984d77ae9ab
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/11/2018
ms.locfileid: "48882249"
---
# <a name="release-notes"></a><span data-ttu-id="ae236-103">Viktig information</span><span class="sxs-lookup"><span data-stu-id="ae236-103">Release notes</span></span>

<span data-ttu-id="ae236-104">Det här är en lista över ändringar som har gjorts i Azure PowerShell i den här versionen.</span><span class="sxs-lookup"><span data-stu-id="ae236-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="6100---october-2018"></a><span data-ttu-id="ae236-105">6.10.0 – Oktober 2018</span><span class="sxs-lookup"><span data-stu-id="ae236-105">6.10.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="ae236-106">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="ae236-106">Azure.Storage</span></span>
* <span data-ttu-id="ae236-107">Åtgärda fel där Kopiera blob/fil inte kopierar metadata när målplatsen har ett problem med metadata</span><span class="sxs-lookup"><span data-stu-id="ae236-107">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="ae236-108">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="ae236-108">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="ae236-109">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="ae236-109">Start-AzureStorageFileCopy</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="ae236-110">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ae236-110">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="ae236-111">Stöd för Get-AzureRmCognitiveServicesAccountSkus utan ett befintligt konto.</span><span class="sxs-lookup"><span data-stu-id="ae236-111">Support Get-AzureRmCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="ae236-112">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ae236-112">AzureRM.Compute</span></span>
* <span data-ttu-id="ae236-113">Åtgärda fel där Get-AzureRmVM -ResourceGroupName <rg> returnerar fler än 50 resultat om det behövs</span><span class="sxs-lookup"><span data-stu-id="ae236-113">Fix Get-AzureRmVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="ae236-114">Ett exempel för ”SimpleParameterSet” har lagts till i hjälpen för cmdleten New-AzureRmVmss.</span><span class="sxs-lookup"><span data-stu-id="ae236-114">Added an example of the 'SimpleParameterSet' to New-AzureRmVmss cmdlet help.</span></span>
* <span data-ttu-id="ae236-115">Ett stavfel i förloppsmeddelandet för Azure Disk Encryption har korrigerats</span><span class="sxs-lookup"><span data-stu-id="ae236-115">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="ae236-116">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="ae236-116">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="ae236-117">ADF .Net SDK-versionen har uppdaterats till 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="ae236-117">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="ae236-118">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ae236-118">AzureRM.Network</span></span>
* <span data-ttu-id="ae236-119">Funktionalitet för NetworkProfile har lagts till.</span><span class="sxs-lookup"><span data-stu-id="ae236-119">Added NetworkProfile functionality.</span></span> <span data-ttu-id="ae236-120">nya cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="ae236-120">new cmdlets added</span></span>
    - <span data-ttu-id="ae236-121">Get-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ae236-121">Get-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="ae236-122">New-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ae236-122">New-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="ae236-123">Remove-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ae236-123">Remove-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="ae236-124">Set-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ae236-124">Set-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="ae236-125">New-AzureRMContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="ae236-125">New-AzureRMContainerNicConfig</span></span>
    - <span data-ttu-id="ae236-126">New-AzureRmContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="ae236-126">New-AzureRmContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="ae236-127">Länk för tjänstassociering på modell för undernät har lagts till</span><span class="sxs-lookup"><span data-stu-id="ae236-127">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="ae236-128">De nya cmdletarna New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap och Remove-AzureRmVirtualNetworkTap har lagts till</span><span class="sxs-lookup"><span data-stu-id="ae236-128">Added cmdlet New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap, Remove-AzureRmVirtualNetworkTap</span></span>
* <span data-ttu-id="ae236-129">Cmdletarna Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig och Remove-AzureRmNEtworkInterfaceTapConfig har lagts till</span><span class="sxs-lookup"><span data-stu-id="ae236-129">Added cmdlet Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig, Remove-AzureRmNEtworkInterfaceTapConfig</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="ae236-130">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="ae236-130">AzureRM.RedisCache</span></span>
* <span data-ttu-id="ae236-131">Tillåt att alla strängar används som storleksparametrar framöver.</span><span class="sxs-lookup"><span data-stu-id="ae236-131">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="ae236-132">Lägg till P5 i popup-fönstret PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="ae236-132">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="ae236-133">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="ae236-133">AzureRM.Resources</span></span>
* <span data-ttu-id="ae236-134">Parametern -Mode som saknades i Set-AzureRmPolicyDefinition har lagts till</span><span class="sxs-lookup"><span data-stu-id="ae236-134">Add missing -Mode parameter to Set-AzureRmPolicyDefinition</span></span>
* <span data-ttu-id="ae236-135">Åtgärda buggen för cmdleten Get-AzureRmProviderOperation för åtgärder med ursprung som innehåller användare</span><span class="sxs-lookup"><span data-stu-id="ae236-135">Fix Get-AzureRmProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="ae236-136">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="ae236-136">AzureRM.Sql</span></span>
* <span data-ttu-id="ae236-137">Ett problem där vissa cmdletar för säkerhetskopiering inte kunde identifiera den aktuella azure-prenumerationen har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="ae236-137">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="ae236-138">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="ae236-138">AzureRM.Storage</span></span>
* <span data-ttu-id="ae236-139">Stöd för att hämta användningsinformation om en Storage-resurs för en specifik plats och för att lägga till ett varningsmeddelande för att hämta användningsinformation om en global Storage-resurs är inaktuellt.</span><span class="sxs-lookup"><span data-stu-id="ae236-139">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="ae236-140">Get-AzureRmStorageUsage</span><span class="sxs-lookup"><span data-stu-id="ae236-140">Get-AzureRmStorageUsage</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="ae236-141">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="ae236-141">AzureRM.Websites</span></span>
* <span data-ttu-id="ae236-142">Ny cmdlet: Get-AzureRMWebAppContainerContinuousDeploymentUrl – Hämtar webhook-URL:en för kontinuerlig distribution av container</span><span class="sxs-lookup"><span data-stu-id="ae236-142">New Cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="ae236-143">Nya cmdletar: New-AzureRMWebAppContainerPSSession och Enter-WebAppContainerPSSession – Startar en PowerShell-fjärrsession i en containerapp för windows</span><span class="sxs-lookup"><span data-stu-id="ae236-143">New Cmdlets New-AzureRMWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="690---september-2018"></a><span data-ttu-id="ae236-144">6.9.0 – September 2018</span><span class="sxs-lookup"><span data-stu-id="ae236-144">6.9.0 - September 2018</span></span>
#### <a name="general"></a><span data-ttu-id="ae236-145">Allmänt</span><span class="sxs-lookup"><span data-stu-id="ae236-145">General</span></span>
* <span data-ttu-id="ae236-146">AzureRM.SignalR har lagts till i samlingsmodulen för AzureRM</span><span class="sxs-lookup"><span data-stu-id="ae236-146">AzureRM.SignalR was added to the AzureRM rollup module</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="ae236-147">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ae236-147">AzureRM.Profile</span></span>
* <span data-ttu-id="ae236-148">Mindre ändringar i den gemensamma koden för lagring</span><span class="sxs-lookup"><span data-stu-id="ae236-148">Minor changes to the storage common code</span></span>
* <span data-ttu-id="ae236-149">Hjälpfiler har uppdaterats för att innehålla fullständiga parametertyper.</span><span class="sxs-lookup"><span data-stu-id="ae236-149">Updated help files to include full parameter types.</span></span>
- <span data-ttu-id="ae236-150">-ServicePrincipal har ändrats så att den inte längre är obligatorisk i parameteruppsättningen ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ae236-150">Changed -ServicePrincipal to non-mandatory in the ServicePrincipalCertificateWithSubscriptionId parameter set</span></span> 

#### <a name="azurestorage"></a><span data-ttu-id="ae236-151">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="ae236-151">Azure.Storage</span></span>
* <span data-ttu-id="ae236-152">Stöd för att skapa lagringskontext med OAuth.</span><span class="sxs-lookup"><span data-stu-id="ae236-152">Support create Storage Context with OAuth.</span></span> 
    - <span data-ttu-id="ae236-153">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="ae236-153">New-AzureStorageContext</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="ae236-154">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="ae236-154">AzureRM.Cdn</span></span>
* <span data-ttu-id="ae236-155">Standard_Microsoft har lagts till i SKU:n för CDN-prissättning.</span><span class="sxs-lookup"><span data-stu-id="ae236-155">Added Standard_Microsoft in Cdn pricing sku.</span></span> 

#### <a name="azurermcompute"></a><span data-ttu-id="ae236-156">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ae236-156">AzureRM.Compute</span></span>
* <span data-ttu-id="ae236-157">Flytta beroenden i nyckelvalv och minne till de gemensamma beroendena</span><span class="sxs-lookup"><span data-stu-id="ae236-157">Move dependencies on Keyvault and Storage to the common dependencies</span></span>
* <span data-ttu-id="ae236-158">Lägg till stöd för flera storlekar av virtuella datorer i AEM-cmdletar</span><span class="sxs-lookup"><span data-stu-id="ae236-158">Add support for more virutal machine sizes to AEM cmdlets</span></span>
* <span data-ttu-id="ae236-159">Lägg till parametern PublicIPPrefix i New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="ae236-159">Add PublicIPPrefix parameter to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="ae236-160">Lägg till parametern ResourceId till cmdleten Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="ae236-160">Add ResourceId parameter to Invoke-AzureRmVMRunCommand cmdelt</span></span>
* <span data-ttu-id="ae236-161">Lägg till cmdleten Invoke-AzureRmVmssVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="ae236-161">Add Invoke-AzureRmVmssVMRunCommand cmdlet</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="ae236-162">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="ae236-162">AzureRM.Dns</span></span>
* <span data-ttu-id="ae236-163">Stöd har lagts till för aliasposter när DNS-poster skapas</span><span class="sxs-lookup"><span data-stu-id="ae236-163">Added support for alias record during dns record creation</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="ae236-164">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="ae236-164">AzureRM.Insights</span></span>
* <span data-ttu-id="ae236-165">Problem #6833 och #7102 (området Diagnostikinställningar) har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="ae236-165">Fixed issues #6833 and #7102 (Diagnostic Settings area)</span></span>
    - <span data-ttu-id="ae236-166">Problem med standardnamnet, d.v.s. ”tjänsten” när diagnostikinställningar skapas och listas/hämtas</span><span class="sxs-lookup"><span data-stu-id="ae236-166">Issues with the default name, i.e. 'service', during creation and listing/getting of diagnostic settings</span></span>
    - <span data-ttu-id="ae236-167">Problem med att skapa diagnostikinställningar med kategorier</span><span class="sxs-lookup"><span data-stu-id="ae236-167">Issues creating diagnostic settings with categories</span></span>
* <span data-ttu-id="ae236-168">Utfasningsmeddelande har lagts till för tidsintervallsparametrar för mått</span><span class="sxs-lookup"><span data-stu-id="ae236-168">Added deprecation message for metrics time grains parameters</span></span>
    - <span data-ttu-id="ae236-169">Tidsintervallsparametrar går fortfarande att använda (det här är en bakåtkompatibel ändring), men de ignoreras i serverdelen eftersom endast PT1M är giltigt</span><span class="sxs-lookup"><span data-stu-id="ae236-169">Timegrains parameters are still being accepted (this is a non-breaking change,) but they are ignored in the backend since only PT1M is valid</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="ae236-170">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ae236-170">AzureRM.Network</span></span>
* <span data-ttu-id="ae236-171">Ändringar i LoadBalancer-cmdletar</span><span class="sxs-lookup"><span data-stu-id="ae236-171">Changes to LoadBalancer cmdlets</span></span>
  - <span data-ttu-id="ae236-172">LoadBalancerInboundNatPoolConfig: parametrarna IdleTimeoutInMinutes, EnableFloatingIp och EnableTcpReset har lagts till</span><span class="sxs-lookup"><span data-stu-id="ae236-172">LoadBalancerInboundNatPoolConfig: added parameters IdleTimeoutInMinutes, EnableFloatingIp and EnableTcpReset</span></span>
  - <span data-ttu-id="ae236-173">LoadBalancerInboundNatRuleConfig: parametern EnableTcpReset har lagts till</span><span class="sxs-lookup"><span data-stu-id="ae236-173">LoadBalancerInboundNatRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="ae236-174">LoadBalancerRuleConfig: parametern EnableTcpReset har lagts till</span><span class="sxs-lookup"><span data-stu-id="ae236-174">LoadBalancerRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="ae236-175">LoadBalancerProbeConfig: stöd för värdet ”Https” för parameterprotokoll har lagts till</span><span class="sxs-lookup"><span data-stu-id="ae236-175">LoadBalancerProbeConfig: added support for value "Https" for parameter Protocol</span></span>
* <span data-ttu-id="ae236-176">Nya kommandon för den nya underresursen för LoadBalancers OutboundRule har lagts till</span><span class="sxs-lookup"><span data-stu-id="ae236-176">Added new commands for new LoadBalancer's subresource OutboundRule</span></span>
  - <span data-ttu-id="ae236-177">Add-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ae236-177">Add-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="ae236-178">Get-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ae236-178">Get-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="ae236-179">New-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ae236-179">New-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="ae236-180">Set-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ae236-180">Set-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="ae236-181">Remove-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ae236-181">Remove-AzureRmLoadBalancerOutboundRuleConfig</span></span>
* <span data-ttu-id="ae236-182">Ny HostedWorkloads-egenskap har lagts till för PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="ae236-182">Added new HostedWorkloads property for PSNetworkInterface</span></span>
* <span data-ttu-id="ae236-183">Nya cmdletar har lagts till för funktionen: Azure Firewall via ARM</span><span class="sxs-lookup"><span data-stu-id="ae236-183">Added new cmdlets for feature: Azure Firewall via ARM</span></span>
  - <span data-ttu-id="ae236-184">Get-AzureRmFirewall har lagts till</span><span class="sxs-lookup"><span data-stu-id="ae236-184">Added Get-AzureRmFirewall</span></span>
  - <span data-ttu-id="ae236-185">Set-AzureRmFirewall har lagts till</span><span class="sxs-lookup"><span data-stu-id="ae236-185">Added Set-AzureRmFirewall</span></span>
  - <span data-ttu-id="ae236-186">New-AzureRmFirewall har lagts till</span><span class="sxs-lookup"><span data-stu-id="ae236-186">Added New-AzureRmFirewall</span></span>
  - <span data-ttu-id="ae236-187">Remove-AzureRmFirewall har lagts till</span><span class="sxs-lookup"><span data-stu-id="ae236-187">Added Remove-AzureRmFirewall</span></span>
  - <span data-ttu-id="ae236-188">New-AzureRmFirewallApplicationRuleCollection har lagts till</span><span class="sxs-lookup"><span data-stu-id="ae236-188">Added New-AzureRmFirewallApplicationRuleCollection</span></span>
  - <span data-ttu-id="ae236-189">New-AzureRmFirewallApplicationRule har lagts till</span><span class="sxs-lookup"><span data-stu-id="ae236-189">Added New-AzureRmFirewallApplicationRule</span></span>
  - <span data-ttu-id="ae236-190">New-AzureRmFirewallNatRuleCollection har lagts till</span><span class="sxs-lookup"><span data-stu-id="ae236-190">Added New-AzureRmFirewallNatRuleCollection</span></span>
  - <span data-ttu-id="ae236-191">New-AzureRmFirewallNatRule har lagts till</span><span class="sxs-lookup"><span data-stu-id="ae236-191">Added New-AzureRmFirewallNatRule</span></span>
  - <span data-ttu-id="ae236-192">New-AzureRmFirewallNetworkRuleCollection har lagts till</span><span class="sxs-lookup"><span data-stu-id="ae236-192">Added New-AzureRmFirewallNetworkRuleCollection</span></span>
  - <span data-ttu-id="ae236-193">New-AzureRmFirewallNetworkRule har lagts till</span><span class="sxs-lookup"><span data-stu-id="ae236-193">Added New-AzureRmFirewallNetworkRule</span></span>
* <span data-ttu-id="ae236-194">Stöd för betrott rotcertifikat och konfiguration för autoskalning har lagts till i Application Gateway</span><span class="sxs-lookup"><span data-stu-id="ae236-194">Added support for Trusted Root certificate and Autoscale configuration in Application Gateway</span></span>
  - <span data-ttu-id="ae236-195">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="ae236-195">New Cmdlets added:</span></span>
      - <span data-ttu-id="ae236-196">Add-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="ae236-196">Add-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="ae236-197">Get-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="ae236-197">Get-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="ae236-198">New-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="ae236-198">New-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="ae236-199">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="ae236-199">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="ae236-200">Set-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="ae236-200">Set-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="ae236-201">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ae236-201">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="ae236-202">New-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ae236-202">New-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="ae236-203">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ae236-203">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="ae236-204">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ae236-204">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
  - <span data-ttu-id="ae236-205">Cmdletar har uppdaterats med valfri parameter – TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="ae236-205">Cmdlets updated with optonal parameter -TrustedRootCertificate</span></span>
      - <span data-ttu-id="ae236-206">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ae236-206">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="ae236-207">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ae236-207">Set-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="ae236-208">New-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="ae236-208">New-AzureRmApplicationGatewayBackendHttpSetting</span></span>
      - <span data-ttu-id="ae236-209">Set-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="ae236-209">Set-AzureRmApplicationGatewayBackendHttpSetting</span></span>
  - <span data-ttu-id="ae236-210">Cmdletar har uppdaterats med valfri parameter – AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ae236-210">Cmdlets updated with optonal parameter -AutoscaleConfiguration</span></span>
      - <span data-ttu-id="ae236-211">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ae236-211">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="ae236-212">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ae236-212">Set-AzureRmApplicationGateway</span></span>
* <span data-ttu-id="ae236-213">Lägg till cmdlet för gränssnittsslutpunkten Get-AzureInterfaceEndpoint</span><span class="sxs-lookup"><span data-stu-id="ae236-213">Add cmdlet for Interface Endpoint Get-AzureInterfaceEndpoint</span></span>
* <span data-ttu-id="ae236-214">Stöd för flera adressprefix i ett undernät har lagts till.</span><span class="sxs-lookup"><span data-stu-id="ae236-214">Added support for multiple address prefixes in a subnet.</span></span> <span data-ttu-id="ae236-215">Uppdaterade cmdletar:</span><span class="sxs-lookup"><span data-stu-id="ae236-215">Updated cmdlets:</span></span>
  - <span data-ttu-id="ae236-216">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="ae236-216">New-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="ae236-217">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="ae236-217">Set-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="ae236-218">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="ae236-218">Add-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="ae236-219">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="ae236-219">Get-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="ae236-220">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ae236-220">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>
  - <span data-ttu-id="ae236-221">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="ae236-221">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="ae236-222">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="ae236-222">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="ae236-223">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="ae236-223">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="ae236-224">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ae236-224">Add-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="ae236-225">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ae236-225">New-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="ae236-226">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ae236-226">Set-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="ae236-227">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="ae236-227">Add-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="ae236-228">New-AzureRmNetworkInterfaceIpConfig – Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="ae236-228">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="ae236-229">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="ae236-229">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="ae236-230">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="ae236-230">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="ae236-231">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ae236-231">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="ae236-232">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ae236-232">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="ae236-233">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ae236-233">New-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="ae236-234">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="ae236-234">New-AzureRmNetworkInterface</span></span>
* <span data-ttu-id="ae236-235">Lägger till cmdletar för delegering av undernät.</span><span class="sxs-lookup"><span data-stu-id="ae236-235">Adding cmdlets for subnet delegation.</span></span>
  - <span data-ttu-id="ae236-236">New-AzureRmDelegation: Skapar en ny delegering som kan läggas till i ett undernät</span><span class="sxs-lookup"><span data-stu-id="ae236-236">New-AzureRmDelegation: Creates a new delegation, which can be added to a subnet</span></span>
  - <span data-ttu-id="ae236-237">Remove-AzureRmDelegation: Hämtar ett undernät och tar bort det angivna delegeringsnamnet från undernätet</span><span class="sxs-lookup"><span data-stu-id="ae236-237">Remove-AzureRmDelegation: Takes in a subnet and removes the provided delegation name from that subnet</span></span>
  - <span data-ttu-id="ae236-238">Add-AzureRmDelegation: Hämtar ett undernät och lägger till det angivna tjänstnamnet som en delegering till undernätet</span><span class="sxs-lookup"><span data-stu-id="ae236-238">Add-AzureRmDelegation: Takes in a subnet and adds the provided service name as a delegation to that subnet</span></span>
  - <span data-ttu-id="ae236-239">Get-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="ae236-239">Get-AzureRmDelegation</span></span>
  - <span data-ttu-id="ae236-240">Get-AzureRmAvailableServiceDelegations</span><span class="sxs-lookup"><span data-stu-id="ae236-240">Get-AzureRmAvailableServiceDelegations</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="ae236-241">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ae236-241">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="ae236-242">Stöd för hanterad disk</span><span class="sxs-lookup"><span data-stu-id="ae236-242">Support for managed Managed disk</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="ae236-243">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="ae236-243">AzureRM.RedisCache</span></span>
* <span data-ttu-id="ae236-244">Insights-beroende har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="ae236-244">Updated Insights dependency.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="ae236-245">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="ae236-245">AzureRM.Resources</span></span>
* <span data-ttu-id="ae236-246">Uppdatera New-AzureRmResourceGroupDeployment med den nya parametern RollbackAction</span><span class="sxs-lookup"><span data-stu-id="ae236-246">Update New-AzureRmResourceGroupDeployment with new parameter RollbackAction</span></span>
    - <span data-ttu-id="ae236-247">Lägg till stöd för OnErrorDeployment med den nya parametern.</span><span class="sxs-lookup"><span data-stu-id="ae236-247">Add support for OnErrorDeployment with the new parameter.</span></span>
* <span data-ttu-id="ae236-248">Stöd för hanterad identitet på principtilldelningar.</span><span class="sxs-lookup"><span data-stu-id="ae236-248">Support managed identity on policy assignments.</span></span>
* <span data-ttu-id="ae236-249">Parametrar med standardvärden krävs inte längre när du tilldelar en princip med ”New-AzureRmPolicyAssignment”</span><span class="sxs-lookup"><span data-stu-id="ae236-249">Parameters with default values are no longer requred when assigning a policy with 'New-AzureRmPolicyAssignment'</span></span>
* <span data-ttu-id="ae236-250">Lägg till den nya cmdleten Get-AzureRmPolicyAlias för att hämta principalias</span><span class="sxs-lookup"><span data-stu-id="ae236-250">Add new cmdlet Get-AzureRmPolicyAlias for retrieving policy aliases</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="ae236-251">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ae236-251">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="ae236-252">Problem #7161 har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="ae236-252">Fixed issue #7161</span></span>

#### <a name="azurermsignalr"></a><span data-ttu-id="ae236-253">AzureRM.SignalR</span><span class="sxs-lookup"><span data-stu-id="ae236-253">AzureRM.SignalR</span></span>
* <span data-ttu-id="ae236-254">Uppdatera SKU-namn till Free_F1 och Standard_S1</span><span class="sxs-lookup"><span data-stu-id="ae236-254">Update SKU names to Free_F1 and Standard_S1</span></span>
* <span data-ttu-id="ae236-255">Lägg till versionsfältet i PSSignalRResource-objektet och en anslutningssträng i PSSignalRKeys-objektet.</span><span class="sxs-lookup"><span data-stu-id="ae236-255">Add version field to the PSSignalRResource object and connection string to the PSSignalRKeys object.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="ae236-256">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="ae236-256">AzureRM.Storage</span></span>
* <span data-ttu-id="ae236-257">Stöd för oföränderlighetsprincip i AzureRm.Storage</span><span class="sxs-lookup"><span data-stu-id="ae236-257">Support Immutability Policy in AzureRm.Storage</span></span> 
    - <span data-ttu-id="ae236-258">Remove-AzureRmStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ae236-258">Remove-AzureRmStorageAccountNetworkRule</span></span>
    - <span data-ttu-id="ae236-259">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ae236-259">Get-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="ae236-260">Update-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ae236-260">Update-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="ae236-261">New-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ae236-261">New-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="ae236-262">Remove-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ae236-262">Remove-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="ae236-263">Add-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="ae236-263">Add-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="ae236-264">Remove-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="ae236-264">Remove-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="ae236-265">Set-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="ae236-265">Set-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="ae236-266">Get-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="ae236-266">Get-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="ae236-267">Remove-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="ae236-267">Remove-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="ae236-268">Lock-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="ae236-268">Lock-AzureRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="ae236-269">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="ae236-269">AzureRM.Websites</span></span>
* <span data-ttu-id="ae236-270">Två nya cmdletar har lagts till: Get-AzureRmDeletedWebApp och Restore-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="ae236-270">Added two new cmdlets: Get-AzureRmDeletedWebApp and Restore-AzureRmDeletedWebApp</span></span>
* <span data-ttu-id="ae236-271">New-AzureRmAppServicePlan – En HyperV-växel har lagts till för skapa en app service-plan med Windows-containrar</span><span class="sxs-lookup"><span data-stu-id="ae236-271">New-AzureRmAppServicePlan -HyperV switch is added for create app service plan with windows container</span></span>
* <span data-ttu-id="ae236-272">New-AzureRmWebApp/New-AzureRmWebAppSlot/Set-AzureRmWebApp/Set-AzureRmWebAppSlot – Nya parametrar (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) har lagts till för att skapa och hantera Windows-containerappar</span><span class="sxs-lookup"><span data-stu-id="ae236-272">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - New parameters (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) added for creating and managing windows container app</span></span>

## <a name="681---august-2018"></a><span data-ttu-id="ae236-273">6.8.1 – augusti 2018</span><span class="sxs-lookup"><span data-stu-id="ae236-273">6.8.1 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="ae236-274">Allmänt</span><span class="sxs-lookup"><span data-stu-id="ae236-274">General</span></span>
* <span data-ttu-id="ae236-275">Problem med standardresursgrupp som inte har konfigurerats har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="ae236-275">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="ae236-276">Uppdaterade Common Runtime-sammansättningar</span><span class="sxs-lookup"><span data-stu-id="ae236-276">Updated common runtime assemblies</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="ae236-277">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ae236-277">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="ae236-278">Problem med standardresursgrupp som inte har konfigurerats har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="ae236-278">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="ae236-279">Åtgärdat problem https://github.com/Azure/azure-powershell/issues/6603</span><span class="sxs-lookup"><span data-stu-id="ae236-279">Fixed issue https://github.com/Azure/azure-powershell/issues/6603</span></span>
    - <span data-ttu-id="ae236-280">Import-AzureRmApiManagementApi- och \*-AzureRmApiManagementCertificate-cmdletar kan nu hantera relativa sökvägar</span><span class="sxs-lookup"><span data-stu-id="ae236-280">Import-AzureRmApiManagementApi and \*-AzureRmApiManagementCertificate cmdlets now handle relative Paths</span></span>
* <span data-ttu-id="ae236-281">Åtgärdat problem https://github.com/Azure/azure-powershell/issues/6879</span><span class="sxs-lookup"><span data-stu-id="ae236-281">Fixed issue https://github.com/Azure/azure-powershell/issues/6879</span></span>
    - <span data-ttu-id="ae236-282">CertificateInformation är en inställbar egenskap som gör att Set-AzureRmApiManagement-cmdleten fungerar ordentligt.</span><span class="sxs-lookup"><span data-stu-id="ae236-282">The CertificateInformation is a settable property allowing for Set-AzureRmApiManagement cmdlet to work property.</span></span> <span data-ttu-id="ae236-283">Åtgärdat genom uppgradering till NuGet för 4.0.4-preview</span><span class="sxs-lookup"><span data-stu-id="ae236-283">Fixed by upgrading to 4.0.4-preview nuget</span></span>
* <span data-ttu-id="ae236-284">Åtgärdat problem https://github.com/Azure/azure-powershell/issues/6853</span><span class="sxs-lookup"><span data-stu-id="ae236-284">Fixed issue https://github.com/Azure/azure-powershell/issues/6853</span></span>
    - <span data-ttu-id="ae236-285">Odata-filtret för sökning efter namn på produkt har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="ae236-285">Fixed the Odata filter for Search by Name on Product</span></span>
* <span data-ttu-id="ae236-286">Åtgärdat problem https://github.com/Azure/azure-powershell/issues/6814</span><span class="sxs-lookup"><span data-stu-id="ae236-286">Fixed issue https://github.com/Azure/azure-powershell/issues/6814</span></span>
    - <span data-ttu-id="ae236-287">Odata-filtret för sökning efter namn på API har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="ae236-287">Fixed the Odata filter for Search by Name on Api</span></span>
* <span data-ttu-id="ae236-288">Stöd har lagts till för AzureMonitor-loggare</span><span class="sxs-lookup"><span data-stu-id="ae236-288">Added support for AzureMonitor logger</span></span>


#### <a name="azurermcompute"></a><span data-ttu-id="ae236-289">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ae236-289">AzureRM.Compute</span></span>
* <span data-ttu-id="ae236-290">Ett problem med att mål saknas i felutdata har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="ae236-290">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="ae236-291">Problem med lagringskontotyper för virtuell dator med en hanterad disk har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="ae236-291">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="ae236-292">Problem med standardresursgrupp som inte har konfigurerats har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="ae236-292">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="ae236-293">Åtgärda cmdletar för AEM-tillägg för andra miljöer, till exempel Azure Kina</span><span class="sxs-lookup"><span data-stu-id="ae236-293">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="ae236-294">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ae236-294">AzureRM.Network</span></span>
* <span data-ttu-id="ae236-295">Standardvisning av cmdlet-utdata har ändrats för att visas i tabellvy</span><span class="sxs-lookup"><span data-stu-id="ae236-295">Changed default cmdlet output presentation to table view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="ae236-296">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="ae236-296">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="ae236-297">Åtgärda fel i Update-AzureRmPowerBIEmbeddedCapacity vid försök att skala pausad kapacitet</span><span class="sxs-lookup"><span data-stu-id="ae236-297">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>


#### <a name="azurermresources"></a><span data-ttu-id="ae236-298">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="ae236-298">AzureRM.Resources</span></span>
* <span data-ttu-id="ae236-299">Ett problem med att skapa hanterade program från MarketPlace har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="ae236-299">Fixed issue with creating managed applications from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="ae236-300">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ae236-300">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="ae236-301">Åtgärdade problem</span><span class="sxs-lookup"><span data-stu-id="ae236-301">Fixed issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="ae236-302">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="ae236-302">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="ae236-303">Stöd har lagts till för trafikroutningsmetoden MultiValue</span><span class="sxs-lookup"><span data-stu-id="ae236-303">Added Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="ae236-304">Ny parameter, ”MaxReturn”, för MultiValue-routning</span><span class="sxs-lookup"><span data-stu-id="ae236-304">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="ae236-305">Stöd har lagts till för trafikroutningsmetod för undernät</span><span class="sxs-lookup"><span data-stu-id="ae236-305">Added Support for the Subnet routing method</span></span>
    - <span data-ttu-id="ae236-306">Stöd för IP-adressintervall (undernät) i slutpunkter</span><span class="sxs-lookup"><span data-stu-id="ae236-306">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="ae236-307">Stöd har lagts till för anpassade rubriker i profiler</span><span class="sxs-lookup"><span data-stu-id="ae236-307">Added Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="ae236-308">Stöd har lagts till för förväntade statuskodintervall i profiler</span><span class="sxs-lookup"><span data-stu-id="ae236-308">Added Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="ae236-309">Stöd har lagts till för anpassade rubriker i slutpunkter</span><span class="sxs-lookup"><span data-stu-id="ae236-309">Added Support for Custom Headers in endpoints</span></span>

## <a name="680---august-2018"></a><span data-ttu-id="ae236-310">6.8.0 – augusti 2018</span><span class="sxs-lookup"><span data-stu-id="ae236-310">6.8.0 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="ae236-311">Allmänt</span><span class="sxs-lookup"><span data-stu-id="ae236-311">General</span></span>
* <span data-ttu-id="ae236-312">Problem med standardresursgrupp som inte har konfigurerats har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="ae236-312">Fixed issue with default resource groups not being set.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="ae236-313">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ae236-313">AzureRM.Profile</span></span>
* <span data-ttu-id="ae236-314">Utgångsegenskap har lagts till i token som returneras under Connect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="ae236-314">Added expiration property to tokens returned during Connect-AzureRmAccount</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="ae236-315">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ae236-315">AzureRM.Compute</span></span>
* <span data-ttu-id="ae236-316">Ett problem med att mål saknas i felutdata har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="ae236-316">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="ae236-317">Problem med lagringskontotyper för virtuell dator med en hanterad disk har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="ae236-317">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="ae236-318">Åtgärda cmdletar för AEM-tillägg för andra miljöer, till exempel Azure Kina</span><span class="sxs-lookup"><span data-stu-id="ae236-318">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="ae236-319">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="ae236-319">AzureRM.IotHub</span></span>
* <span data-ttu-id="ae236-320">Korrigera exempel för New-AzureRmIotHubExportDevices och New-AzureRmIotHubImportDevices</span><span class="sxs-lookup"><span data-stu-id="ae236-320">Fix examples for New-AzureRmIotHubExportDevices and New-AzureRmIotHubImportDevices</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="ae236-321">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ae236-321">AzureRM.Network</span></span>
* <span data-ttu-id="ae236-322">Standardmodeller har ändrats för att visas i tabellvy</span><span class="sxs-lookup"><span data-stu-id="ae236-322">Changed default models representation to table-view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="ae236-323">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="ae236-323">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="ae236-324">Åtgärda fel i Update-AzureRmPowerBIEmbeddedCapacity vid försök att skala pausad kapacitet</span><span class="sxs-lookup"><span data-stu-id="ae236-324">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="ae236-325">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="ae236-325">AzureRM.Resources</span></span>
* <span data-ttu-id="ae236-326">Ett problem med att skapa hanterade program från MarketPlace har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="ae236-326">Fixed issue with creating managed application from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="ae236-327">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ae236-327">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="ae236-328">Korrigeringar för problem</span><span class="sxs-lookup"><span data-stu-id="ae236-328">Fix for issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="ae236-329">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="ae236-329">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="ae236-330">Stöd för trafikroutningsmetoden MultiValue</span><span class="sxs-lookup"><span data-stu-id="ae236-330">Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="ae236-331">Ny parameter, ”MaxReturn”, för MultiValue-routning</span><span class="sxs-lookup"><span data-stu-id="ae236-331">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="ae236-332">Stöd för trafikroutningsmetod för undernät</span><span class="sxs-lookup"><span data-stu-id="ae236-332">Support for the Subnet routing method</span></span>
    - <span data-ttu-id="ae236-333">Stöd för IP-adressintervall (undernät) i slutpunkter</span><span class="sxs-lookup"><span data-stu-id="ae236-333">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="ae236-334">Stöd för anpassade rubriker i profiler</span><span class="sxs-lookup"><span data-stu-id="ae236-334">Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="ae236-335">Stöd för förväntade statuskodintervall i profiler</span><span class="sxs-lookup"><span data-stu-id="ae236-335">Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="ae236-336">Stöd för anpassade rubriker i slutpunkter</span><span class="sxs-lookup"><span data-stu-id="ae236-336">Support for Custom Headers in endpoints</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="ae236-337">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="ae236-337">AzureRM.Websites</span></span>
* <span data-ttu-id="ae236-338">Problem med standardresursgrupp som inte har konfigurerats korrekt har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="ae236-338">Fixed issue with default resource group being set incorrectly.</span></span>

## <a name="670---august-2018"></a><span data-ttu-id="ae236-339">6.7.0 – augusti 2018</span><span class="sxs-lookup"><span data-stu-id="ae236-339">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="ae236-340">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ae236-340">AzureRM.Profile</span></span>
* <span data-ttu-id="ae236-341">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ae236-341">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="ae236-342">Lägg till användar-id i standardkontextnamnet för att undvika kontextkonflikter</span><span class="sxs-lookup"><span data-stu-id="ae236-342">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="ae236-343">Åtgärda problem med Clear-AzureRmContext som orsakade problem med att välja en kontext #6398</span><span class="sxs-lookup"><span data-stu-id="ae236-343">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="ae236-344">Aktivera den klientorganisationsdomän som ska skickas till parametern -TenantId för Connect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="ae236-344">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="ae236-345">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="ae236-345">Azure.Storage</span></span>
* <span data-ttu-id="ae236-346">Ta bort begränsningen på 5 TB för Azure-filresurskvoten</span><span class="sxs-lookup"><span data-stu-id="ae236-346">Remove the 5TB limitation for Azure File Share quota</span></span>
- <span data-ttu-id="ae236-347">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="ae236-347">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="ae236-348">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ae236-348">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="ae236-349">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ae236-349">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="ae236-350">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ae236-350">Azure.AnalysisServices</span></span>
* <span data-ttu-id="ae236-351">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ae236-351">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="ae236-352">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ae236-352">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="ae236-353">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ae236-353">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="ae236-354">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="ae236-354">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="ae236-355">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ae236-355">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="ae236-356">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="ae236-356">AzureRM.Automation</span></span>
* <span data-ttu-id="ae236-357">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ae236-357">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="ae236-358">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="ae236-358">AzureRM.Backup</span></span>
* <span data-ttu-id="ae236-359">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ae236-359">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="ae236-360">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="ae236-360">AzureRM.Batch</span></span>
* <span data-ttu-id="ae236-361">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ae236-361">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="ae236-362">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="ae236-362">AzureRM.Billing</span></span>
* <span data-ttu-id="ae236-363">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ae236-363">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="ae236-364">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="ae236-364">AzureRM.Cdn</span></span>
* <span data-ttu-id="ae236-365">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ae236-365">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="ae236-366">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ae236-366">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="ae236-367">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ae236-367">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="ae236-368">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ae236-368">AzureRM.Compute</span></span>
* <span data-ttu-id="ae236-369">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ae236-369">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="ae236-370">Lägg till parametern EvictionPolicy i New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="ae236-370">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="ae236-371">Använd standardplatsen i DiskFileParameterSet för New-AzureRmVm om ingen plats har angetts.</span><span class="sxs-lookup"><span data-stu-id="ae236-371">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="ae236-372">Korrigera parameterbeskrivningen i Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="ae236-372">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="ae236-373">Korrigera cmdleten Get-AzureRmVMDiskEncryptionStatus för vissa singlepass-relaterade scenarier</span><span class="sxs-lookup"><span data-stu-id="ae236-373">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="ae236-374">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="ae236-374">AzureRM.Consumption</span></span>
* <span data-ttu-id="ae236-375">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ae236-375">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="ae236-376">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="ae236-376">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="ae236-377">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ae236-377">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="ae236-378">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ae236-378">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="ae236-379">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ae236-379">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="ae236-380">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="ae236-380">AzureRM.DataFactories</span></span>
* <span data-ttu-id="ae236-381">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ae236-381">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="ae236-382">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="ae236-382">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="ae236-383">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ae236-383">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="ae236-384">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="ae236-384">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="ae236-385">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ae236-385">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="ae236-386">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ae236-386">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="ae236-387">Korrigera felsökning när DebugPreference anges från powershell-kommandoraden</span><span class="sxs-lookup"><span data-stu-id="ae236-387">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="ae236-388">Uppdatera exemplet för Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="ae236-388">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="ae236-389">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ae236-389">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="ae236-390">Uppdatera exemplet för Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="ae236-390">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="ae236-391">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="ae236-391">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="ae236-392">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ae236-392">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="ae236-393">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="ae236-393">AzureRM.Dns</span></span>
* <span data-ttu-id="ae236-394">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ae236-394">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="ae236-395">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="ae236-395">AzureRM.EventGrid</span></span>
* <span data-ttu-id="ae236-396">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ae236-396">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="ae236-397">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="ae236-397">AzureRM.EventHub</span></span>
* <span data-ttu-id="ae236-398">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ae236-398">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="ae236-399">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="ae236-399">AzureRM.HDInsight</span></span>
* <span data-ttu-id="ae236-400">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ae236-400">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="ae236-401">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="ae236-401">AzureRM.Insights</span></span>
* <span data-ttu-id="ae236-402">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ae236-402">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="ae236-403">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="ae236-403">AzureRM.IotHub</span></span>
* <span data-ttu-id="ae236-404">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ae236-404">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="ae236-405">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ae236-405">AzureRM.KeyVault</span></span>
* <span data-ttu-id="ae236-406">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ae236-406">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="ae236-407">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="ae236-407">AzureRM.LogicApp</span></span>
* <span data-ttu-id="ae236-408">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ae236-408">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="ae236-409">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="ae236-409">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="ae236-410">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ae236-410">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="ae236-411">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="ae236-411">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="ae236-412">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ae236-412">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="ae236-413">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="ae236-413">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="ae236-414">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ae236-414">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="ae236-415">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="ae236-415">AzureRM.Media</span></span>
* <span data-ttu-id="ae236-416">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ae236-416">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="ae236-417">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ae236-417">AzureRM.Network</span></span>
* <span data-ttu-id="ae236-418">Exempel för Set-AzureRmLocalNetworkGateway har lagts till</span><span class="sxs-lookup"><span data-stu-id="ae236-418">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="ae236-419">Exempel och beskrivningar för Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey och New-AzureRmVirtualNetworkGatewayConnection har lagts till</span><span class="sxs-lookup"><span data-stu-id="ae236-419">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="ae236-420">Exempel för Remove-AzureRmVirtualNetworkGatewayIpConfig och Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ae236-420">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="ae236-421">Exempel för Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey har lagts till</span><span class="sxs-lookup"><span data-stu-id="ae236-421">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="ae236-422">Exempel för Set-AzureRmVirtualNetworkGatewayConnectionSharedKey har lagts till</span><span class="sxs-lookup"><span data-stu-id="ae236-422">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="ae236-423">Exempel för Set-AzureRmVirtualNetworkGatewayConnection har lagts till</span><span class="sxs-lookup"><span data-stu-id="ae236-423">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="ae236-424">Cmdletar för ApplicationSecurityGroup, RouteTable and Usage har genererats om med den senaste kodgeneratorn</span><span class="sxs-lookup"><span data-stu-id="ae236-424">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="ae236-425">Förtydligade ett felmeddelande för Get-AzureRmVirtualNetworkSubnetConfig vid försök att hämta ett undernät som inte avslutas</span><span class="sxs-lookup"><span data-stu-id="ae236-425">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="ae236-426">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="ae236-426">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="ae236-427">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ae236-427">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="ae236-428">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ae236-428">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="ae236-429">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ae236-429">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="ae236-430">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="ae236-430">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="ae236-431">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ae236-431">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="ae236-432">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="ae236-432">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="ae236-433">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ae236-433">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="ae236-434">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ae236-434">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="ae236-435">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ae236-435">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="ae236-436">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ae236-436">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="ae236-437">Lade till principfilter i cmdleten Get-AzureRmRecoveryServicesBackItem.</span><span class="sxs-lookup"><span data-stu-id="ae236-437">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="ae236-438">Kommandot returnerar listan med säkerhetskopieringsobjekt som skyddas av det angivna princip-ID:t.</span><span class="sxs-lookup"><span data-stu-id="ae236-438">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="ae236-439">Microsoft.Azure.Management.RecoveryServices.Backup uppdaterades till förhandsversionen av 3.0.0.</span><span class="sxs-lookup"><span data-stu-id="ae236-439">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="ae236-440">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ae236-440">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="ae236-441">Parametern TargetResourceGroupName lades till i Restore-AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="ae236-441">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="ae236-442">Den resursgrupp som de hanterade diskarna återställs till.</span><span class="sxs-lookup"><span data-stu-id="ae236-442">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="ae236-443">Gäller för säkerhetskopiering av virtuell dator med hanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="ae236-443">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="ae236-444">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ae236-444">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="ae236-445">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ae236-445">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="ae236-446">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="ae236-446">AzureRM.RedisCache</span></span>
* <span data-ttu-id="ae236-447">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ae236-447">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="ae236-448">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="ae236-448">AzureRM.Relay</span></span>
* <span data-ttu-id="ae236-449">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ae236-449">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="ae236-450">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="ae236-450">AzureRM.Resources</span></span>
* <span data-ttu-id="ae236-451">Distribution av supportmall i prenumerationsomfånget.</span><span class="sxs-lookup"><span data-stu-id="ae236-451">Support template deployment at subscription scope.</span></span> <span data-ttu-id="ae236-452">Lägg till nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="ae236-452">Add new Cmdlets:</span></span>
    - <span data-ttu-id="ae236-453">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="ae236-453">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="ae236-454">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="ae236-454">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="ae236-455">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="ae236-455">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="ae236-456">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="ae236-456">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="ae236-457">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="ae236-457">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="ae236-458">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="ae236-458">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="ae236-459">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="ae236-459">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="ae236-460">Korrigera ett problem där fel inträffar när en kontext skickas till Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="ae236-460">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="ae236-461">Korrigera exempel i New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ae236-461">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="ae236-462">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ae236-462">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="ae236-463">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="ae236-463">AzureRM.Scheduler</span></span>
* <span data-ttu-id="ae236-464">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ae236-464">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="ae236-465">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ae236-465">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="ae236-466">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ae236-466">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="ae236-467">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ae236-467">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="ae236-468">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ae236-468">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="ae236-469">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="ae236-469">AzureRM.Sql</span></span>
* <span data-ttu-id="ae236-470">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ae236-470">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="ae236-471">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="ae236-471">AzureRM.Storage</span></span>
* <span data-ttu-id="ae236-472">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ae236-472">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="ae236-473">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="ae236-473">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="ae236-474">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ae236-474">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="ae236-475">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="ae236-475">AzureRM.Tags</span></span>
* <span data-ttu-id="ae236-476">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ae236-476">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="ae236-477">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="ae236-477">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="ae236-478">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ae236-478">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="ae236-479">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="ae236-479">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="ae236-480">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ae236-480">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="ae236-481">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="ae236-481">AzureRM.Websites</span></span>
* <span data-ttu-id="ae236-482">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ae236-482">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="ae236-483">6.6.0 – juli 2018</span><span class="sxs-lookup"><span data-stu-id="ae236-483">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="ae236-484">Allmänt</span><span class="sxs-lookup"><span data-stu-id="ae236-484">General</span></span>
* <span data-ttu-id="ae236-485">Alla hjälpfiler har uppdaterats för att ta med fullständiga parametertyper och korrekta indata-/utdatatyper.</span><span class="sxs-lookup"><span data-stu-id="ae236-485">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="ae236-486">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ae236-486">AzureRM.Profile</span></span>
* <span data-ttu-id="ae236-487">Common.Strategy-biblioteket har uppdaterats för att kunna verifiera att den aktuella konfigurationsfilen för en resurs är kompatibel med målresursen.</span><span class="sxs-lookup"><span data-stu-id="ae236-487">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="ae236-488">ps1xml-typer har lagts till i Common.Storage</span><span class="sxs-lookup"><span data-stu-id="ae236-488">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="ae236-489">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="ae236-489">Azure.Storage</span></span>
* <span data-ttu-id="ae236-490">Lade till stöd för hämtning av lagringskontext från DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae236-490">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="ae236-491">Lade till Ps1XmlAttribute till utdatatypegenskaper för cmdletar.</span><span class="sxs-lookup"><span data-stu-id="ae236-491">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="ae236-492">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ae236-492">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="ae236-493">Åtgärdat problem https://github.com/Azure/azure-powershell/issues/6370</span><span class="sxs-lookup"><span data-stu-id="ae236-493">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="ae236-494">En bugg har åtgärdats i Automapper för att översätta PsApiManagementApi till ApiContract</span><span class="sxs-lookup"><span data-stu-id="ae236-494">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="ae236-495">Åtgärdat problem https://github.com/Azure/azure-powershell/issues/6515</span><span class="sxs-lookup"><span data-stu-id="ae236-495">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="ae236-496">En bugg har åtgärdats i File.Save för att inte överbelasta kodningstypen</span><span class="sxs-lookup"><span data-stu-id="ae236-496">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="ae236-497">Åtgärdat problem https://github.com/Azure/azure-powershell/issues/6560</span><span class="sxs-lookup"><span data-stu-id="ae236-497">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="ae236-498">Har uppgraderats till Nuget-versionen 4.0.3 vilket åtgärdar mönsterundantaget på apiId</span><span class="sxs-lookup"><span data-stu-id="ae236-498">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="ae236-499">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ae236-499">AzureRM.Compute</span></span>
* <span data-ttu-id="ae236-500">Åtgärda problem med fel vid skapandet av en virtuell dator med hjälp av DiskFileParameterSet i New-AzureRmVm på grund av namnbyte på PremiumLRS-lagringskontotypen.</span><span class="sxs-lookup"><span data-stu-id="ae236-500">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="ae236-501">Åtgärda cmdleten Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="ae236-501">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="ae236-502">Uppdatera Get-AzureRmAvailabilitySet för att aktivera funktionen för att lista alla tillgänglighetsuppsättningar i en prenumeration.</span><span class="sxs-lookup"><span data-stu-id="ae236-502">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="ae236-503">(Parametern ResouceGroupName är nu frivillig.)</span><span class="sxs-lookup"><span data-stu-id="ae236-503">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="ae236-504">Uppdatera SimpleParameterSet för "New-AzureRmVm" för att aktivera accelererat nätverk på berättigade virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="ae236-504">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="ae236-505">Uppdatera den enkla parameteruppsättningen för New-AzureRmVmss så att det inte går att skapa de virtuella datorerna när en användarangiven lastbalanserare redan finns.</span><span class="sxs-lookup"><span data-stu-id="ae236-505">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="ae236-506">Uppdatera exempel för New-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="ae236-506">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="ae236-507">Lägg till exempel för "New-AzureRmVM"</span><span class="sxs-lookup"><span data-stu-id="ae236-507">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="ae236-508">Uppdatera beskrivning för Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="ae236-508">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="ae236-509">Uppdatera Exempel 1 för Set-AzureRmVMBginfoExtension för stavningskontroll och prefix.</span><span class="sxs-lookup"><span data-stu-id="ae236-509">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="ae236-510">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="ae236-510">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="ae236-511">ADF .Net SDK-versionen har uppdaterats till 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="ae236-511">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="ae236-512">Stöd för delning av Integration Runtime (lokal installation) mellan datafabriker.</span><span class="sxs-lookup"><span data-stu-id="ae236-512">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="ae236-513">Lägg till ny parameter – SharedIntegrationRuntimeResourceId i cmdleten Set-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="ae236-513">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="ae236-514">Lägg till ny valfri parameter – LinkedDataFactoryName i cmdleten Remove-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="ae236-514">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="ae236-515">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ae236-515">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="ae236-516">DataPlane SDK-versionen (Microsoft.Azure.DataLake.Store) har uppdaterats till 1.1.9</span><span class="sxs-lookup"><span data-stu-id="ae236-516">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="ae236-517">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="ae236-517">AzureRM.EventHub</span></span>
* <span data-ttu-id="ae236-518">Piping för InputObject and ResourceId i borttagna cmdletar har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="ae236-518">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="ae236-519">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="ae236-519">AzureRM.Insights</span></span>
* <span data-ttu-id="ae236-520">Formatering har åtgärdats för OutputType i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="ae236-520">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="ae236-521">Använda Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span><span class="sxs-lookup"><span data-stu-id="ae236-521">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="ae236-522">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ae236-522">AzureRM.KeyVault</span></span>
* <span data-ttu-id="ae236-523">Åtgärda problem med piping i Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ae236-523">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="ae236-524">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ae236-524">AzureRM.Network</span></span>
* <span data-ttu-id="ae236-525">Exempel har lagts till för LoadBalancerInboundNatPoolConfig-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="ae236-525">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="ae236-526">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="ae236-526">AzureRM.Resources</span></span>
* <span data-ttu-id="ae236-527">Åtgärda problem när både taggnamn och värde anges för "Get-AzureRmResource"</span><span class="sxs-lookup"><span data-stu-id="ae236-527">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="ae236-528">Åtgärda pipingscenario med "Set-AzureRmResource"</span><span class="sxs-lookup"><span data-stu-id="ae236-528">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="ae236-529">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ae236-529">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="ae236-530">Piping för InputObject and ResourceId i borttagna cmdletar har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="ae236-530">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="ae236-531">några problem har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="ae236-531">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="ae236-532">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="ae236-532">AzureRM.Sql</span></span>
* <span data-ttu-id="ae236-533">Lägg till stöd för Server Advanced Threat Protection med följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="ae236-533">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="ae236-534">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="ae236-534">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="ae236-535">Lägg till stöd för Sårbarhetsbedömning med följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="ae236-535">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="ae236-536">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="ae236-536">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="ae236-537">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="ae236-537">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="ae236-538">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="ae236-538">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="ae236-539">Exempel i Remove-AzureRmSqlServerFirewallRule har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="ae236-539">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="ae236-540">Åtgärda felaktig hantering av datum och tid för andra kulturer än usa-baserade kulturer i Get-AzureSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="ae236-540">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="ae236-541">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="ae236-541">AzureRM.Storage</span></span>
* <span data-ttu-id="ae236-542">Lägg till Ps1XmlAttribute i utdatatypegenskaper för cmdletar</span><span class="sxs-lookup"><span data-stu-id="ae236-542">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="ae236-543">Visa utdata för cmdleten StorageAccount i tabellvyn</span><span class="sxs-lookup"><span data-stu-id="ae236-543">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="ae236-544">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ae236-544">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="ae236-545">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ae236-545">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="ae236-546">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ae236-546">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="ae236-547">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="ae236-547">AzureRM.Tags</span></span>
* <span data-ttu-id="ae236-548">Ta bort felaktig instruktion från hjälpen för cmdleten Tag</span><span class="sxs-lookup"><span data-stu-id="ae236-548">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="ae236-549">6.5.0 – juli 2018</span><span class="sxs-lookup"><span data-stu-id="ae236-549">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="ae236-550">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ae236-550">AzureRM.Profile</span></span>
* <span data-ttu-id="ae236-551">Hjälp för ”Get-AzureRmContextAutosaveSetting” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="ae236-551">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="ae236-552">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="ae236-552">Azure.Storage</span></span>
* <span data-ttu-id="ae236-553">Stöd för uppladdning av blob eller fil med lässkyddad SAS-token</span><span class="sxs-lookup"><span data-stu-id="ae236-553">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="ae236-554">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="ae236-554">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="ae236-555">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="ae236-555">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="ae236-556">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ae236-556">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="ae236-557">Lägg till den nödvändiga egenskapen ResourceGroupName i AS.</span><span class="sxs-lookup"><span data-stu-id="ae236-557">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="ae236-558">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="ae236-558">AzureRM.Automation</span></span>
* <span data-ttu-id="ae236-559">Uppdatera hjälp och lägg till exempel för ”New-AzureRMAutomationSchedule”</span><span class="sxs-lookup"><span data-stu-id="ae236-559">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="ae236-560">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ae236-560">AzureRM.Compute</span></span>
* <span data-ttu-id="ae236-561">Lägg till parametern -Tag förUpdate/New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="ae236-561">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="ae236-562">Lägg till exempel för ”Add-AzureRmVmssExtension”</span><span class="sxs-lookup"><span data-stu-id="ae236-562">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="ae236-563">Lägg till exempel för ”Remove-AzureRmVmssExtension”</span><span class="sxs-lookup"><span data-stu-id="ae236-563">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="ae236-564">Uppdatera hjälp för ”Set-AzureRmVMAccessExtension”</span><span class="sxs-lookup"><span data-stu-id="ae236-564">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="ae236-565">Uppdatera SimpleParameterSet för New-AzureRmVmss för att ställa in SinglePlacementGroup på falskt som standard och lägg till växlingsparametern ”SinglePlacementGroup” som gör att användare kan skapa VMSS i en enda placeringsgrupp.</span><span class="sxs-lookup"><span data-stu-id="ae236-565">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="ae236-566">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="ae236-566">AzureRM.EventHub</span></span>
* <span data-ttu-id="ae236-567">En skrivskyddad egenskap, ”PendingReplicationOperationsCount”, har lagts till för klassen PSEventHubDRConfigurationAttributes som anger antalet väntande replikeringsåtgärder medan replikeringen pågår</span><span class="sxs-lookup"><span data-stu-id="ae236-567">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="ae236-568">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ae236-568">AzureRM.KeyVault</span></span>
* <span data-ttu-id="ae236-569">Uppdatera felmeddelande för Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ae236-569">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="ae236-570">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="ae236-570">AzureRM.LogicApp</span></span>
* <span data-ttu-id="ae236-571">Felet ”parameteruppsättningen gick inte att matcha” har korrigerats i New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="ae236-571">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="ae236-572">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ae236-572">AzureRM.Network</span></span>
* <span data-ttu-id="ae236-573">Aktivera peering mellan virtuella nätverk i flera klienter för Set/Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="ae236-573">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="ae236-574">Nedanstående cmdletar för Application Gateway har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="ae236-574">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="ae236-575">New-AzureRmApplicationGateway: EnableFIPS-flagga har lagts till för stöd för zoner</span><span class="sxs-lookup"><span data-stu-id="ae236-575">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="ae236-576">New-AzureRmApplicationGatewaySku: nya SKU:er, Standard_v2 och WAF_v2, har lagts till</span><span class="sxs-lookup"><span data-stu-id="ae236-576">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="ae236-577">Set-AzureRmApplicationGatewaySku: nya SKU:er, Standard_v2 och WAF_v2, har lagts till</span><span class="sxs-lookup"><span data-stu-id="ae236-577">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="ae236-578">RouteTable-cmdletar har återskapats med den senaste versionen av generatorn</span><span class="sxs-lookup"><span data-stu-id="ae236-578">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="ae236-579">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="ae236-579">AzureRM.Relay</span></span>
* <span data-ttu-id="ae236-580">Markdown-filer har uppdaterats och korrigerar problem med parameternamn i exemplet</span><span class="sxs-lookup"><span data-stu-id="ae236-580">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="ae236-581">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="ae236-581">AzureRM.Resources</span></span>
* <span data-ttu-id="ae236-582">Uppdatera cmdletar för rolltilldelning och rolldefinition:</span><span class="sxs-lookup"><span data-stu-id="ae236-582">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="ae236-583">Ta bort extra anrop för rolldefinitioner som görs som en del av sidindelning.</span><span class="sxs-lookup"><span data-stu-id="ae236-583">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="ae236-584">Åtgärda Get-AzureRMRoleAssignment-cmdlet</span><span class="sxs-lookup"><span data-stu-id="ae236-584">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="ae236-585">Åtgärda parameterfunktioner för kommandot -ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="ae236-585">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="ae236-586">Åtgärda problem med ”Get-AzureRmResource” där ”-ResourceType”-parametern var skiftlägeskänsligt</span><span class="sxs-lookup"><span data-stu-id="ae236-586">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="ae236-587">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ae236-587">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="ae236-588">Parametrar för att stoppa och hoppa över har lagts till i listan över cmdletar</span><span class="sxs-lookup"><span data-stu-id="ae236-588">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="ae236-589">Cmdletar för migrering från Standard- till Premium-namnområden har lagts till:</span><span class="sxs-lookup"><span data-stu-id="ae236-589">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="ae236-590">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="ae236-590">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="ae236-591">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="ae236-591">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="ae236-592">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="ae236-592">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="ae236-593">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="ae236-593">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="ae236-594">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="ae236-594">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="ae236-595">En skrivskyddad egenskap, ”PendingReplicationOperationsCount” har lagts till för klassen PSServiceBusDRConfigurationAttributes som anger antalet väntande replikeringsåtgärder medan replikeringen pågår</span><span class="sxs-lookup"><span data-stu-id="ae236-595">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="ae236-596">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ae236-596">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="ae236-597">Uppdatera exempel för ”New-AzureRmServiceFabricCluster”</span><span class="sxs-lookup"><span data-stu-id="ae236-597">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="ae236-598">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="ae236-598">AzureRM.Sql</span></span>
* <span data-ttu-id="ae236-599">Nya cmdletar för Management.Sql som gör att kunderna kan lägga till certifikat för transparent datakryptering till SQL Server-instans eller en hanterad instans har lagts till</span><span class="sxs-lookup"><span data-stu-id="ae236-599">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="ae236-600">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="ae236-600">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="ae236-601">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="ae236-601">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="ae236-602">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="ae236-602">AzureRM.Websites</span></span>
* <span data-ttu-id="ae236-603">När `Set-AzureRmWebApp -AssignIdentity` och `Set-AzureRmWebAppSlot -AssignIdentity` är inställda på falskt tar de nu bort identitetsegenskapen från platsobjektet. Även förhandsgranskningstaggen tas bort.</span><span class="sxs-lookup"><span data-stu-id="ae236-603">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="ae236-604">`Get-AzureRmWebAppMetrics`, `Get-AzureRmAppServicePlanMetrics`-exempel har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="ae236-604">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="ae236-605">`Set-AzureRmWebApp -PhpVersion` har stöd för ”av” som en giltig php-version</span><span class="sxs-lookup"><span data-stu-id="ae236-605">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="ae236-606">6.4.0 – juli 2018</span><span class="sxs-lookup"><span data-stu-id="ae236-606">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="ae236-607">Allmänt</span><span class="sxs-lookup"><span data-stu-id="ae236-607">General</span></span>
* <span data-ttu-id="ae236-608">Formatering av OutputType i hjälpfiler har korrigerats för de flesta moduler</span><span class="sxs-lookup"><span data-stu-id="ae236-608">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="ae236-609">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ae236-609">AzureRM.Profile</span></span>
* <span data-ttu-id="ae236-610">Ps1Xml-attribut har lagts till för grundläggande utdatatyper</span><span class="sxs-lookup"><span data-stu-id="ae236-610">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="ae236-611">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ae236-611">AzureRM.Compute</span></span>
* <span data-ttu-id="ae236-612">IP-tagg-funktioner för VMSS</span><span class="sxs-lookup"><span data-stu-id="ae236-612">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="ae236-613">"New-AzureRmVmssIpTagConfig"-cmdlet har lagts till</span><span class="sxs-lookup"><span data-stu-id="ae236-613">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="ae236-614">IpTag-parameter har lagts till för New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="ae236-614">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="ae236-615">Automatisk återställningsfunktion för operativsystem för VMSS</span><span class="sxs-lookup"><span data-stu-id="ae236-615">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="ae236-616">DisableAutoRollback-parametrar har lagts till för New-AzureRmVmssConfig och Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ae236-616">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="ae236-617">Funktion för uppgraderingshistorik för operativsystem för Vmss</span><span class="sxs-lookup"><span data-stu-id="ae236-617">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="ae236-618">OSUpgradeHistory-växlingsparametern har lagts till för Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ae236-618">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="ae236-619">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="ae236-619">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="ae236-620">Lägg till stöd för katalog-ACL:er med hjälp av följande kommandon:</span><span class="sxs-lookup"><span data-stu-id="ae236-620">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="ae236-621">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="ae236-621">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="ae236-622">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="ae236-622">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="ae236-623">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="ae236-623">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="ae236-624">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ae236-624">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="ae236-625">Lägg till stöd för annullering och förloppsspårning för Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="ae236-625">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="ae236-626">Lägg till stöd för annullering för Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="ae236-626">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="ae236-627">Åtgärda tömning av felsökningsmeddelanden för cmdletar som gör rekursiva åtgärder</span><span class="sxs-lookup"><span data-stu-id="ae236-627">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="ae236-628">Åtgärda platsen för testning av DataLake-cmdletar</span><span class="sxs-lookup"><span data-stu-id="ae236-628">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="ae236-629">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="ae236-629">AzureRM.EventHub</span></span>
* <span data-ttu-id="ae236-630">Parametrar för optimalt maxantal har lagts till i liståtgärds-cmdletarna Get-AzureRmEventHub och Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="ae236-630">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="ae236-631">Ett problem i New-AzureRmEventHub-cmdleten har åtgärdats där minst en parameter behövdes när du skapade en ny EventHub.</span><span class="sxs-lookup"><span data-stu-id="ae236-631">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="ae236-632">Angiven standardparameter har ställts in.</span><span class="sxs-lookup"><span data-stu-id="ae236-632">Provided Default Parameter set.</span></span>
* <span data-ttu-id="ae236-633">Valfri parameter för KeyValue har lagts till för New-AzureRmEventHubKey-cmdleten, vilket gör det möjligt att ange KeyValue.</span><span class="sxs-lookup"><span data-stu-id="ae236-633">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="ae236-634">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ae236-634">AzureRM.KeyVault</span></span>
* <span data-ttu-id="ae236-635">Åtgärda problem där alla resurser returnerades av Get-AzureRmKeyVault-taggen</span><span class="sxs-lookup"><span data-stu-id="ae236-635">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="ae236-636">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ae236-636">AzureRM.Network</span></span>
* <span data-ttu-id="ae236-637">Gör nya SKU:er tillgängliga för zonredundanta VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="ae236-637">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="ae236-638">Nya kommandon har lagts till för funktionen: ExpressRoute Partner APIs via ARM</span><span class="sxs-lookup"><span data-stu-id="ae236-638">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="ae236-639">Get-AzureRmExpressRouteCrossConnection har lagts till</span><span class="sxs-lookup"><span data-stu-id="ae236-639">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="ae236-640">Set-AzureRmExpressRouteCrossConnection har lagts till</span><span class="sxs-lookup"><span data-stu-id="ae236-640">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="ae236-641">Add-AzureRmExpressRouteCrossConnectionPeering har lagts till</span><span class="sxs-lookup"><span data-stu-id="ae236-641">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="ae236-642">Get-AzureRmExpressRouteCrossConnectionPeering har lagts till</span><span class="sxs-lookup"><span data-stu-id="ae236-642">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="ae236-643">Remove-AzureRmExpressRouteCrossConnectionPeering har lagts till</span><span class="sxs-lookup"><span data-stu-id="ae236-643">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="ae236-644">Get-AzureRMExpressRouteCrossConnectionArpTable har lagts till</span><span class="sxs-lookup"><span data-stu-id="ae236-644">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="ae236-645">Get-AzureRMExpressRouteCrossConnectionRouteTable har lagts till</span><span class="sxs-lookup"><span data-stu-id="ae236-645">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="ae236-646">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary har lagts till</span><span class="sxs-lookup"><span data-stu-id="ae236-646">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="ae236-647">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ae236-647">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="ae236-648">Get-AzureRmRecoveryServicesBackupStatus-cmdlet har lagts till.</span><span class="sxs-lookup"><span data-stu-id="ae236-648">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="ae236-649">Denna cmdlet tar ett ID för virtuell dator och kontrollerar om den virtuella datorn skyddas av ett valv i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="ae236-649">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="ae236-650">Om ett sådant valv finns returnerar cmdleten valvinformationen.</span><span class="sxs-lookup"><span data-stu-id="ae236-650">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="ae236-651">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="ae236-651">AzureRM.Resources</span></span>
* <span data-ttu-id="ae236-652">Uppdatera Get-AzureRmPolicyAssignment-cmdletar:</span><span class="sxs-lookup"><span data-stu-id="ae236-652">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="ae236-653">Lägg till stöd för att lista -Scope-värden på hanteringsgruppsnivå</span><span class="sxs-lookup"><span data-stu-id="ae236-653">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="ae236-654">Lägg till stöd för hämtning av enskilda tilldelningar med -Scope-värden på hanteringsgruppsnivå.</span><span class="sxs-lookup"><span data-stu-id="ae236-654">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="ae236-655">Lägg till växlar för -Effective och -All till kontrollparametrar</span><span class="sxs-lookup"><span data-stu-id="ae236-655">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="ae236-656">Uppdatera Get/New/Remove/Set-AzureRmPolicyDefinition-cmdletar</span><span class="sxs-lookup"><span data-stu-id="ae236-656">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="ae236-657">Lägg till parameter för -ManagementGroupName om du vill tillämpa åtgärder för en viss hanteringsgrupp</span><span class="sxs-lookup"><span data-stu-id="ae236-657">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="ae236-658">Lägg till parameter för -SubscriptionId om du vill tillämpa åtgärder för en viss prenumeration</span><span class="sxs-lookup"><span data-stu-id="ae236-658">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="ae236-659">Uppdatera Get/New/Remove/Set-AzureRmPolicySetDefinition-cmdletar</span><span class="sxs-lookup"><span data-stu-id="ae236-659">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="ae236-660">Lägg till parameter för -ManagementGroupName om du vill tillämpa åtgärder för en viss hanteringsgrupp</span><span class="sxs-lookup"><span data-stu-id="ae236-660">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="ae236-661">Lägg till parameter för -SubscriptionId om du vill tillämpa åtgärder för en viss prenumeration</span><span class="sxs-lookup"><span data-stu-id="ae236-661">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="ae236-662">Lägg till stöd för hemliga KeyVault-referenser i parametrar när du använder "TemplateParameterObject" i "New-AzureRmResourceGroupDeployment"</span><span class="sxs-lookup"><span data-stu-id="ae236-662">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="ae236-663">Åtgärda problem med att "-EndDate"-parametern ignorerades på grund av "New-AzureRmADAppCredential"</span><span class="sxs-lookup"><span data-stu-id="ae236-663">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="ae236-664">Åtgärda problem med att felaktig URL användes i "New-AzureRmADAppCredential" vid begäran</span><span class="sxs-lookup"><span data-stu-id="ae236-664">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="ae236-665">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ae236-665">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="ae236-666">Valfri parameter för -KeyValue har lagts till för New-AzureRmServiceBusKey-cmdleten, vilket gör det möjligt att ange KeyValue.</span><span class="sxs-lookup"><span data-stu-id="ae236-666">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="ae236-667">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="ae236-667">AzureRM.Sql</span></span>
* <span data-ttu-id="ae236-668">Användardefinierade återställningspunkter har klargjorts för SQLDW i New-AzureRmSqlDatabaseRestorePoint-hjälpen</span><span class="sxs-lookup"><span data-stu-id="ae236-668">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="ae236-669">Dokumentationen om parametern -ComputeGeneration har uppdaterats i fler cmdletar</span><span class="sxs-lookup"><span data-stu-id="ae236-669">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="ae236-670">6.3.0 – juni 2018</span><span class="sxs-lookup"><span data-stu-id="ae236-670">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="ae236-671">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ae236-671">AzureRM.Profile</span></span>
* <span data-ttu-id="ae236-672">Uppdaterade felmeddelanden för Enable-AzureRmContextAutoSave</span><span class="sxs-lookup"><span data-stu-id="ae236-672">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="ae236-673">Skapa en kontext för varje prenumeration när du kör ”Connect-AzureRmAccount” utan tidigare kontext</span><span class="sxs-lookup"><span data-stu-id="ae236-673">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="ae236-674">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="ae236-674">Azure.Storage</span></span>
* <span data-ttu-id="ae236-675">Ytterligare information om parametern -Permissions har lagts till i hjälpfilerna.</span><span class="sxs-lookup"><span data-stu-id="ae236-675">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="ae236-676">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ae236-676">AzureRM.Compute</span></span>
* <span data-ttu-id="ae236-677">”Get-AzureRmVmDiskEncryptionStatus” korrigerar ett problem för virtuella datorer utan datadiskar</span><span class="sxs-lookup"><span data-stu-id="ae236-677">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="ae236-678">Uppdatera version av klientbibliotek för Compute för att korrigera följande cmdletar</span><span class="sxs-lookup"><span data-stu-id="ae236-678">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="ae236-679">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="ae236-679">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="ae236-680">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="ae236-680">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="ae236-681">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="ae236-681">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="ae236-682">Följande cmdletar har åtgärdats för att visa ”Åtgärds-ID” och ”Åtgärdsstatus” på ett korrekt sätt:</span><span class="sxs-lookup"><span data-stu-id="ae236-682">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="ae236-683">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ae236-683">Start-AzureRmVM</span></span>
    - <span data-ttu-id="ae236-684">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ae236-684">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="ae236-685">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ae236-685">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="ae236-686">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ae236-686">Set-AzureRmVM</span></span>
    - <span data-ttu-id="ae236-687">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="ae236-687">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="ae236-688">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ae236-688">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="ae236-689">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="ae236-689">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="ae236-690">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="ae236-690">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="ae236-691">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ae236-691">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="ae236-692">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ae236-692">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="ae236-693">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ae236-693">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="ae236-694">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ae236-694">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="ae236-695">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="ae236-695">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="ae236-696">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="ae236-696">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="ae236-697">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="ae236-697">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="ae236-698">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="ae236-698">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="ae236-699">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="ae236-699">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="ae236-700">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="ae236-700">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="ae236-701">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="ae236-701">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="ae236-702">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="ae236-702">AzureRM.EventGrid</span></span>
* <span data-ttu-id="ae236-703">Ta bort verifieringsvillkoren ValidateNotNullOrEmpty för SubjectBeginsWith/SubjectEndsWith i cmdleten Update-AzureRmEventGridSubscription för att ändra de här parametrarna till en tom sträng om det behövs.</span><span class="sxs-lookup"><span data-stu-id="ae236-703">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="ae236-704">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ae236-704">AzureRM.KeyVault</span></span>
* <span data-ttu-id="ae236-705">Åtgärda problem där inga taggar returneras när Get-AzureRmKeyVault -Tag körs</span><span class="sxs-lookup"><span data-stu-id="ae236-705">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="ae236-706">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="ae236-706">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="ae236-707">Offentlig lansering av cmdletar för Policy Insights</span><span class="sxs-lookup"><span data-stu-id="ae236-707">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="ae236-708">Använd API-version 2018-04-04</span><span class="sxs-lookup"><span data-stu-id="ae236-708">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="ae236-709">Lägg till PolicyDefinitionReferenceId i resultaten för Get-AzureRmPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="ae236-709">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="ae236-710">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ae236-710">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="ae236-711">Parametern -Vault har lagts till i cmdletarna för RecoveryServices.Backup.</span><span class="sxs-lookup"><span data-stu-id="ae236-711">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="ae236-712">När den godkänns åsidosätts cmdleten Set-AzureRmRecoveryServicesContext.</span><span class="sxs-lookup"><span data-stu-id="ae236-712">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="ae236-713">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="ae236-713">AzureRM.Sql</span></span>
* <span data-ttu-id="ae236-714">Exemplet i hjälpfilen för Get-AzureRmSqlDatabaseExpanded har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="ae236-714">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="ae236-715">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="ae236-715">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="ae236-716">Hjälpfilen för Add-AzureRmTrafficManagerEndpointConfig har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="ae236-716">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="ae236-717">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="ae236-717">AzureRM.Websites</span></span>
* <span data-ttu-id="ae236-718">”Set-AzureRmWebApp” har uppdaterats så att den inte skriver över appinställningarna när du använder -AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="ae236-718">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="ae236-719">”New-AzureRMWebAppSlot” har uppdaterats för att visa att AppServicePlan är en valfri parameter</span><span class="sxs-lookup"><span data-stu-id="ae236-719">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="ae236-720">6.2.1 – juni 2018</span><span class="sxs-lookup"><span data-stu-id="ae236-720">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="ae236-721">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ae236-721">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="ae236-722">PSWorkspace-modellen har uppdaterats för att tillåta att nätverket använder typ som en parameter</span><span class="sxs-lookup"><span data-stu-id="ae236-722">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="ae236-723">6.2.0 – juni 2018</span><span class="sxs-lookup"><span data-stu-id="ae236-723">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="ae236-724">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ae236-724">AzureRM.Profile</span></span>
* <span data-ttu-id="ae236-725">Åtgärda problemet med att version 10.0.3 av Newtonsoft.Json inte lästes in vid modulimporten</span><span class="sxs-lookup"><span data-stu-id="ae236-725">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="ae236-726">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ae236-726">AzureRM.Compute</span></span>
* <span data-ttu-id="ae236-727">VMSS VM-uppdateringsfunktion</span><span class="sxs-lookup"><span data-stu-id="ae236-727">VMSS VM Update feature</span></span>
    - <span data-ttu-id="ae236-728">Cmdletarna Update-AzureRmVmssVM och New-AzureRmVMDataDisk har lagts till</span><span class="sxs-lookup"><span data-stu-id="ae236-728">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="ae236-729">Lägg till parametern VirtualMachineScaleSetVM till cmdleten Add-AzureRmVMDataDisk så att det går att lägga till en datadisk i den virtuella Vmss-datorn.</span><span class="sxs-lookup"><span data-stu-id="ae236-729">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="ae236-730">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="ae236-730">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="ae236-731">SDK:n för ADF .Net har uppdaterats till version 0.8.0-preview som innehåller följande ändringar:</span><span class="sxs-lookup"><span data-stu-id="ae236-731">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="ae236-732">Åtgärden för att konfigurera fabrikslagringsplatsen har lagts till</span><span class="sxs-lookup"><span data-stu-id="ae236-732">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="ae236-733">QuickBooks LinkedService har uppdaterats för att visa egenskaperna consumerKey och consumerSecret</span><span class="sxs-lookup"><span data-stu-id="ae236-733">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="ae236-734">Flera modelltyper från SecretBase till Object har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="ae236-734">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="ae236-735">Utlösaren Blob Events har lagts till</span><span class="sxs-lookup"><span data-stu-id="ae236-735">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="ae236-736">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ae236-736">AzureRM.KeyVault</span></span>
* <span data-ttu-id="ae236-737">Uppdatera dokumentation med exempel på utdata</span><span class="sxs-lookup"><span data-stu-id="ae236-737">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="ae236-738">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ae236-738">AzureRM.Network</span></span>
* <span data-ttu-id="ae236-739">Aktivera Trafikanalys-parametrar på Network Watcher-cmdletar</span><span class="sxs-lookup"><span data-stu-id="ae236-739">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="ae236-740">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="ae236-740">AzureRM.Resources</span></span>
* <span data-ttu-id="ae236-741">Åtgärda problemet med egenskapen "Properties" för objekt(en) "PSResource" som returneras från "Get-AzureRmResource"</span><span class="sxs-lookup"><span data-stu-id="ae236-741">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="ae236-742">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="ae236-742">AzureRM.Scheduler</span></span>
* <span data-ttu-id="ae236-743">Åtgärda problemet med att nya autentiseringsvärden inte anges vid uppdatering av ServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="ae236-743">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="ae236-744">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="ae236-744">AzureRM.Sql</span></span>
* <span data-ttu-id="ae236-745">Följande cmdletar har uppdaterats med valfri LicenseType-parameter</span><span class="sxs-lookup"><span data-stu-id="ae236-745">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="ae236-746">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ae236-746">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="ae236-747">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="ae236-747">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="ae236-748">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="ae236-748">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="ae236-749">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="ae236-749">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="ae236-750">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ae236-750">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="ae236-751">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="ae236-751">AzureRM.Websites</span></span>
* <span data-ttu-id="ae236-752">New-AzureRMWebApp har uppdaterats för att använda vanliga algoritmer från biblioteket Strategy.</span><span class="sxs-lookup"><span data-stu-id="ae236-752">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="ae236-753">6.1.0 – maj 2018</span><span class="sxs-lookup"><span data-stu-id="ae236-753">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="ae236-754">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ae236-754">AzureRM.Profile</span></span>
* <span data-ttu-id="ae236-755">Åtgärda problem där en körning av Clear-AzureRmContext skulle bevara en tom kontext med namnet på den föregående standardkontexten som gjorde att användaren inte kunde skapa en ny kontext med det gamla namnet</span><span class="sxs-lookup"><span data-stu-id="ae236-755">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="ae236-756">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ae236-756">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="ae236-757">Aktivera Gateway associerings- och avassocieringsåtgärder på AS.</span><span class="sxs-lookup"><span data-stu-id="ae236-757">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="ae236-758">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ae236-758">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="ae236-759">Stöd för ApiVersions, ApiReleases och ApiRevisions har lagts till</span><span class="sxs-lookup"><span data-stu-id="ae236-759">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="ae236-760">Stöd för serverdelen på ServiceFabric har lagts till</span><span class="sxs-lookup"><span data-stu-id="ae236-760">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="ae236-761">Stöd för Application Insights-loggare har lagts till</span><span class="sxs-lookup"><span data-stu-id="ae236-761">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="ae236-762">Stöd för att identifiera SKU:n ”Basic” som en giltig SKU för Api Management-tjänsten har lagts till</span><span class="sxs-lookup"><span data-stu-id="ae236-762">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="ae236-763">Stöd för att installera certifikat som utfärdats av privata certifikatutfärdare som rot eller certifikatutfärdare har lagts till</span><span class="sxs-lookup"><span data-stu-id="ae236-763">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="ae236-764">Stöd för att godkänna anpassade SSL-certifikat via KeyVault och flera proxy-värdnamn har lagts till</span><span class="sxs-lookup"><span data-stu-id="ae236-764">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="ae236-765">Stöd för MSI-identitet har lagts till</span><span class="sxs-lookup"><span data-stu-id="ae236-765">Added support for MSI identity</span></span>
* <span data-ttu-id="ae236-766">Stöd för att godkänna principer via URL har lagts till. Obs! Följande cmdletar blir inaktuella i framtida versioner</span><span class="sxs-lookup"><span data-stu-id="ae236-766">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="ae236-767">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="ae236-767">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="ae236-768">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="ae236-768">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="ae236-769">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="ae236-769">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="ae236-770">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="ae236-770">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="ae236-771">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="ae236-771">AzureRM.Batch</span></span>
* <span data-ttu-id="ae236-772">Släpp nya cmdleten Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="ae236-772">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="ae236-773">Släpp nya cmdleten Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="ae236-773">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="ae236-774">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="ae236-774">AzureRM.Consumption</span></span>
* <span data-ttu-id="ae236-775">Lägg till nya parametrar Expand, ResourceGroup, InstanceName, InstanceId, Tags och Top på cmdleten Get-AzureRmConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="ae236-775">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="ae236-776">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ae236-776">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="ae236-777">Åtgärda exempel för Export AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="ae236-777">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="ae236-778">Åtgärda undantag för null-parameter för rekursivt ärende i Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="ae236-778">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="ae236-779">Åtgärda hjälpfilerna för Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="ae236-779">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="ae236-780">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ae236-780">AzureRM.Network</span></span>
* <span data-ttu-id="ae236-781">Öka nätverkets SDK-version från förhandsversionen 18.0.0 till förhandsversionen 19.0.0</span><span class="sxs-lookup"><span data-stu-id="ae236-781">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="ae236-782">Cmdlet har lagts till för att skapa protokollinformation</span><span class="sxs-lookup"><span data-stu-id="ae236-782">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="ae236-783">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="ae236-783">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="ae236-784">Cmdlet har lagts till för att lägga till en ny kretsanslutning till en befintlig expressroute-krets.</span><span class="sxs-lookup"><span data-stu-id="ae236-784">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="ae236-785">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="ae236-785">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="ae236-786">Cmdlet har lagts till för att ta bort en kretsanslutning från en befintlig expressroute-krets.</span><span class="sxs-lookup"><span data-stu-id="ae236-786">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="ae236-787">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="ae236-787">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="ae236-788">Cmdlet har lagts till för att hämta en kretsanslutning</span><span class="sxs-lookup"><span data-stu-id="ae236-788">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="ae236-789">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="ae236-789">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="ae236-790">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ae236-790">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="ae236-791">Användning med serverautentisering med genererade certifikat (problem #5998) har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="ae236-791">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="ae236-792">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="ae236-792">AzureRM.Sql</span></span>
* <span data-ttu-id="ae236-793">Cmdletar för granskning för att ta bort AuditActions eller AuditActionGroups har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="ae236-793">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="ae236-794">Åtgärdade problem med Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy vid konfigurering av en ny flexibel bevarandeprincip där kommandot misslyckas med ett meddelande om att konfigurering av långsiktig bevarandeprincip med Azure Recovery Service-valv och principen inte längre stöds,</span><span class="sxs-lookup"><span data-stu-id="ae236-794">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="ae236-795">och att en begäran med den nya flexibla bevarandeprincipen ska skickas.</span><span class="sxs-lookup"><span data-stu-id="ae236-795">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="ae236-796">Uppdatera alla Azure Sql Database/ElasticPool Creation/Update-relaterade cmdletar för att använda det nya databas-API:et som stöder SKU-egenskaper för skalnings- och nivårelaterade egenskaper.</span><span class="sxs-lookup"><span data-stu-id="ae236-796">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="ae236-797">Cmdletar har uppdaterats, inklusive:</span><span class="sxs-lookup"><span data-stu-id="ae236-797">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="ae236-798">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ae236-798">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="ae236-799">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="ae236-799">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="ae236-800">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="ae236-800">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="ae236-801">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="ae236-801">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="ae236-802">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ae236-802">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="ae236-803">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="ae236-803">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="ae236-804">Uppdatera parametrarna för Get-AzureRmTrafficManagerProfile så att ResourceGroupName-parametern blir obligatorisk när du använder Name-parametern.</span><span class="sxs-lookup"><span data-stu-id="ae236-804">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
