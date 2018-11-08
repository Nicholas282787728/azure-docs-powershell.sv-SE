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
ms.openlocfilehash: eec8b5960f787fa9ca1130b4f8b49c9d896aa99e
ms.sourcegitcommit: 1f699b72bf544d92459da9d888cc0091f9415b65
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/06/2018
ms.locfileid: "50971983"
---
# <a name="release-notes"></a><span data-ttu-id="e44fe-103">Viktig information</span><span class="sxs-lookup"><span data-stu-id="e44fe-103">Release notes</span></span>

<span data-ttu-id="e44fe-104">Det här är en lista över ändringar som har gjorts i Azure PowerShell i den här versionen.</span><span class="sxs-lookup"><span data-stu-id="e44fe-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="6110---october-2018"></a><span data-ttu-id="e44fe-105">6.11.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="e44fe-105">6.11.0 - October 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="e44fe-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="e44fe-106">AzureRM.Profile</span></span>
* <span data-ttu-id="e44fe-107">Åtgärda problemet med Get-AzureRmSubscription i CloudShell</span><span class="sxs-lookup"><span data-stu-id="e44fe-107">Fix issue with Get-AzureRmSubscription in CloudShell</span></span>
* <span data-ttu-id="e44fe-108">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="e44fe-108">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="e44fe-109">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="e44fe-109">AzureRM.Backup</span></span>
* <span data-ttu-id="e44fe-110">Inaktuella Azure Backup-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="e44fe-110">Deprecated Azure Backup cmdlets.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="e44fe-111">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="e44fe-111">AzureRM.Compute</span></span>
* <span data-ttu-id="e44fe-112">Nya storlekar har lagts till i listan över godkända VM-storlekar för vilka accelererat nätverk kommer att aktiveras vid användning av den enkla parameteruppsättningen för ”New-AzureRmVm”</span><span class="sxs-lookup"><span data-stu-id="e44fe-112">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzureRmVm'</span></span>
* <span data-ttu-id="e44fe-113">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="e44fe-113">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="e44fe-114">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e44fe-114">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="e44fe-115">Lägger till stöd för virtuella nätverksregler</span><span class="sxs-lookup"><span data-stu-id="e44fe-115">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="e44fe-116">Get-AzureRmDataLakeStoreVirtualNetworkRule: Hämtar eller lägger till regel för virtuellt nätverk i Azure Data Lake Store i en lista.</span><span class="sxs-lookup"><span data-stu-id="e44fe-116">Get-AzureRmDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="e44fe-117">Add-AzureRmDataLakeStoreVirtualNetworkRule: Lägger till en virtuell nätverksregel till det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="e44fe-117">Add-AzureRmDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="e44fe-118">Set-AzureRmDataLakeStoreVirtualNetworkRule: Ändrar den angivna virtuella nätverksregeln i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="e44fe-118">Set-AzureRmDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="e44fe-119">Remove-AzureRmDataLakeStoreVirtualNetworkRule: Tar bort en regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e44fe-119">Remove-AzureRmDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="e44fe-120">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="e44fe-120">AzureRM.Network</span></span>
* <span data-ttu-id="e44fe-121">Skicka protokollvärdet till serverdelen för att uppdatera cmdleten Test-AzureRmNetworkWatcherConnectivity.</span><span class="sxs-lookup"><span data-stu-id="e44fe-121">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="e44fe-122">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="e44fe-122">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="e44fe-123">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="e44fe-123">AzureRM.Resources</span></span>
* <span data-ttu-id="e44fe-124">Åtgärda problem där Get-AzureRMRoleDefinition genererar ett oläsligt undantag (när standardprofilen inte innehåller någon prenumeration och ingen omfattning har angetts) genom att lägga till ett beskrivande undantag i scenariot.</span><span class="sxs-lookup"><span data-stu-id="e44fe-124">Fix isssue where Get-AzureRMRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="e44fe-125">Ställ in ”RoleDefinitionNameParameterSet” som standardparameteruppsättning.</span><span class="sxs-lookup"><span data-stu-id="e44fe-125">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="6100---october-2018"></a><span data-ttu-id="e44fe-126">6.10.0 – Oktober 2018</span><span class="sxs-lookup"><span data-stu-id="e44fe-126">6.10.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="e44fe-127">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="e44fe-127">Azure.Storage</span></span>
* <span data-ttu-id="e44fe-128">Åtgärda fel där Kopiera blob/fil inte kopierar metadata när målplatsen har ett problem med metadata</span><span class="sxs-lookup"><span data-stu-id="e44fe-128">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="e44fe-129">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="e44fe-129">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="e44fe-130">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="e44fe-130">Start-AzureStorageFileCopy</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="e44fe-131">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e44fe-131">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="e44fe-132">Stöd för Get-AzureRmCognitiveServicesAccountSkus utan ett befintligt konto.</span><span class="sxs-lookup"><span data-stu-id="e44fe-132">Support Get-AzureRmCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="e44fe-133">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="e44fe-133">AzureRM.Compute</span></span>
* <span data-ttu-id="e44fe-134">Åtgärda fel där Get-AzureRmVM -ResourceGroupName <rg> returnerar fler än 50 resultat om det behövs</span><span class="sxs-lookup"><span data-stu-id="e44fe-134">Fix Get-AzureRmVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="e44fe-135">Ett exempel för ”SimpleParameterSet” har lagts till i hjälpen för cmdleten New-AzureRmVmss.</span><span class="sxs-lookup"><span data-stu-id="e44fe-135">Added an example of the 'SimpleParameterSet' to New-AzureRmVmss cmdlet help.</span></span>
* <span data-ttu-id="e44fe-136">Ett stavfel i förloppsmeddelandet för Azure Disk Encryption har korrigerats</span><span class="sxs-lookup"><span data-stu-id="e44fe-136">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="e44fe-137">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="e44fe-137">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="e44fe-138">ADF .Net SDK-versionen har uppdaterats till 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="e44fe-138">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="e44fe-139">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="e44fe-139">AzureRM.Network</span></span>
* <span data-ttu-id="e44fe-140">Funktionalitet för NetworkProfile har lagts till.</span><span class="sxs-lookup"><span data-stu-id="e44fe-140">Added NetworkProfile functionality.</span></span> <span data-ttu-id="e44fe-141">nya cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="e44fe-141">new cmdlets added</span></span>
    - <span data-ttu-id="e44fe-142">Get-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e44fe-142">Get-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="e44fe-143">New-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e44fe-143">New-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="e44fe-144">Remove-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e44fe-144">Remove-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="e44fe-145">Set-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e44fe-145">Set-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="e44fe-146">New-AzureRMContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="e44fe-146">New-AzureRMContainerNicConfig</span></span>
    - <span data-ttu-id="e44fe-147">New-AzureRmContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="e44fe-147">New-AzureRmContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="e44fe-148">Länk för tjänstassociering på modell för undernät har lagts till</span><span class="sxs-lookup"><span data-stu-id="e44fe-148">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="e44fe-149">De nya cmdletarna New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap och Remove-AzureRmVirtualNetworkTap har lagts till</span><span class="sxs-lookup"><span data-stu-id="e44fe-149">Added cmdlet New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap, Remove-AzureRmVirtualNetworkTap</span></span>
* <span data-ttu-id="e44fe-150">Cmdletarna Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig och Remove-AzureRmNEtworkInterfaceTapConfig har lagts till</span><span class="sxs-lookup"><span data-stu-id="e44fe-150">Added cmdlet Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig, Remove-AzureRmNEtworkInterfaceTapConfig</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="e44fe-151">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="e44fe-151">AzureRM.RedisCache</span></span>
* <span data-ttu-id="e44fe-152">Tillåt att alla strängar används som storleksparametrar framöver.</span><span class="sxs-lookup"><span data-stu-id="e44fe-152">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="e44fe-153">Lägg till P5 i popup-fönstret PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="e44fe-153">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="e44fe-154">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="e44fe-154">AzureRM.Resources</span></span>
* <span data-ttu-id="e44fe-155">Parametern -Mode som saknades i Set-AzureRmPolicyDefinition har lagts till</span><span class="sxs-lookup"><span data-stu-id="e44fe-155">Add missing -Mode parameter to Set-AzureRmPolicyDefinition</span></span>
* <span data-ttu-id="e44fe-156">Åtgärda buggen för cmdleten Get-AzureRmProviderOperation för åtgärder med ursprung som innehåller användare</span><span class="sxs-lookup"><span data-stu-id="e44fe-156">Fix Get-AzureRmProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="e44fe-157">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="e44fe-157">AzureRM.Sql</span></span>
* <span data-ttu-id="e44fe-158">Ett problem där vissa cmdletar för säkerhetskopiering inte kunde identifiera den aktuella azure-prenumerationen har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="e44fe-158">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="e44fe-159">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="e44fe-159">AzureRM.Storage</span></span>
* <span data-ttu-id="e44fe-160">Stöd för att hämta användningsinformation om en Storage-resurs för en specifik plats och för att lägga till ett varningsmeddelande för att hämta användningsinformation om en global Storage-resurs är inaktuellt.</span><span class="sxs-lookup"><span data-stu-id="e44fe-160">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="e44fe-161">Get-AzureRmStorageUsage</span><span class="sxs-lookup"><span data-stu-id="e44fe-161">Get-AzureRmStorageUsage</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="e44fe-162">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="e44fe-162">AzureRM.Websites</span></span>
* <span data-ttu-id="e44fe-163">Ny cmdlet: Get-AzureRMWebAppContainerContinuousDeploymentUrl – Hämtar webhook-URL:en för kontinuerlig distribution av container</span><span class="sxs-lookup"><span data-stu-id="e44fe-163">New Cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="e44fe-164">Nya cmdletar: New-AzureRMWebAppContainerPSSession och Enter-WebAppContainerPSSession – Startar en PowerShell-fjärrsession i en containerapp för windows</span><span class="sxs-lookup"><span data-stu-id="e44fe-164">New Cmdlets New-AzureRMWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="690---september-2018"></a><span data-ttu-id="e44fe-165">6.9.0 – September 2018</span><span class="sxs-lookup"><span data-stu-id="e44fe-165">6.9.0 - September 2018</span></span>
#### <a name="general"></a><span data-ttu-id="e44fe-166">Allmänt</span><span class="sxs-lookup"><span data-stu-id="e44fe-166">General</span></span>
* <span data-ttu-id="e44fe-167">AzureRM.SignalR har lagts till i samlingsmodulen för AzureRM</span><span class="sxs-lookup"><span data-stu-id="e44fe-167">AzureRM.SignalR was added to the AzureRM rollup module</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="e44fe-168">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="e44fe-168">AzureRM.Profile</span></span>
* <span data-ttu-id="e44fe-169">Mindre ändringar i den gemensamma koden för lagring</span><span class="sxs-lookup"><span data-stu-id="e44fe-169">Minor changes to the storage common code</span></span>
* <span data-ttu-id="e44fe-170">Hjälpfiler har uppdaterats för att innehålla fullständiga parametertyper.</span><span class="sxs-lookup"><span data-stu-id="e44fe-170">Updated help files to include full parameter types.</span></span>
- <span data-ttu-id="e44fe-171">-ServicePrincipal har ändrats så att den inte längre är obligatorisk i parameteruppsättningen ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e44fe-171">Changed -ServicePrincipal to non-mandatory in the ServicePrincipalCertificateWithSubscriptionId parameter set</span></span> 

#### <a name="azurestorage"></a><span data-ttu-id="e44fe-172">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="e44fe-172">Azure.Storage</span></span>
* <span data-ttu-id="e44fe-173">Stöd för att skapa lagringskontext med OAuth.</span><span class="sxs-lookup"><span data-stu-id="e44fe-173">Support create Storage Context with OAuth.</span></span> 
    - <span data-ttu-id="e44fe-174">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="e44fe-174">New-AzureStorageContext</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="e44fe-175">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="e44fe-175">AzureRM.Cdn</span></span>
* <span data-ttu-id="e44fe-176">Standard_Microsoft har lagts till i SKU:n för CDN-prissättning.</span><span class="sxs-lookup"><span data-stu-id="e44fe-176">Added Standard_Microsoft in Cdn pricing sku.</span></span> 

#### <a name="azurermcompute"></a><span data-ttu-id="e44fe-177">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="e44fe-177">AzureRM.Compute</span></span>
* <span data-ttu-id="e44fe-178">Flytta beroenden i nyckelvalv och minne till de gemensamma beroendena</span><span class="sxs-lookup"><span data-stu-id="e44fe-178">Move dependencies on Keyvault and Storage to the common dependencies</span></span>
* <span data-ttu-id="e44fe-179">Lägg till stöd för flera storlekar av virtuella datorer i AEM-cmdletar</span><span class="sxs-lookup"><span data-stu-id="e44fe-179">Add support for more virutal machine sizes to AEM cmdlets</span></span>
* <span data-ttu-id="e44fe-180">Lägg till parametern PublicIPPrefix i New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="e44fe-180">Add PublicIPPrefix parameter to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="e44fe-181">Lägg till parametern ResourceId till cmdleten Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="e44fe-181">Add ResourceId parameter to Invoke-AzureRmVMRunCommand cmdelt</span></span>
* <span data-ttu-id="e44fe-182">Lägg till cmdleten Invoke-AzureRmVmssVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="e44fe-182">Add Invoke-AzureRmVmssVMRunCommand cmdlet</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="e44fe-183">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="e44fe-183">AzureRM.Dns</span></span>
* <span data-ttu-id="e44fe-184">Stöd har lagts till för aliasposter när DNS-poster skapas</span><span class="sxs-lookup"><span data-stu-id="e44fe-184">Added support for alias record during dns record creation</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="e44fe-185">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="e44fe-185">AzureRM.Insights</span></span>
* <span data-ttu-id="e44fe-186">Problem #6833 och #7102 (området Diagnostikinställningar) har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="e44fe-186">Fixed issues #6833 and #7102 (Diagnostic Settings area)</span></span>
    - <span data-ttu-id="e44fe-187">Problem med standardnamnet, d.v.s. ”tjänsten” när diagnostikinställningar skapas och listas/hämtas</span><span class="sxs-lookup"><span data-stu-id="e44fe-187">Issues with the default name, i.e. 'service', during creation and listing/getting of diagnostic settings</span></span>
    - <span data-ttu-id="e44fe-188">Problem med att skapa diagnostikinställningar med kategorier</span><span class="sxs-lookup"><span data-stu-id="e44fe-188">Issues creating diagnostic settings with categories</span></span>
* <span data-ttu-id="e44fe-189">Utfasningsmeddelande har lagts till för tidsintervallsparametrar för mått</span><span class="sxs-lookup"><span data-stu-id="e44fe-189">Added deprecation message for metrics time grains parameters</span></span>
    - <span data-ttu-id="e44fe-190">Tidsintervallsparametrar går fortfarande att använda (det här är en bakåtkompatibel ändring), men de ignoreras i serverdelen eftersom endast PT1M är giltigt</span><span class="sxs-lookup"><span data-stu-id="e44fe-190">Timegrains parameters are still being accepted (this is a non-breaking change,) but they are ignored in the backend since only PT1M is valid</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="e44fe-191">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="e44fe-191">AzureRM.Network</span></span>
* <span data-ttu-id="e44fe-192">Ändringar i LoadBalancer-cmdletar</span><span class="sxs-lookup"><span data-stu-id="e44fe-192">Changes to LoadBalancer cmdlets</span></span>
  - <span data-ttu-id="e44fe-193">LoadBalancerInboundNatPoolConfig: parametrarna IdleTimeoutInMinutes, EnableFloatingIp och EnableTcpReset har lagts till</span><span class="sxs-lookup"><span data-stu-id="e44fe-193">LoadBalancerInboundNatPoolConfig: added parameters IdleTimeoutInMinutes, EnableFloatingIp and EnableTcpReset</span></span>
  - <span data-ttu-id="e44fe-194">LoadBalancerInboundNatRuleConfig: parametern EnableTcpReset har lagts till</span><span class="sxs-lookup"><span data-stu-id="e44fe-194">LoadBalancerInboundNatRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="e44fe-195">LoadBalancerRuleConfig: parametern EnableTcpReset har lagts till</span><span class="sxs-lookup"><span data-stu-id="e44fe-195">LoadBalancerRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="e44fe-196">LoadBalancerProbeConfig: stöd för värdet ”Https” för parameterprotokoll har lagts till</span><span class="sxs-lookup"><span data-stu-id="e44fe-196">LoadBalancerProbeConfig: added support for value "Https" for parameter Protocol</span></span>
* <span data-ttu-id="e44fe-197">Nya kommandon för den nya underresursen för LoadBalancers OutboundRule har lagts till</span><span class="sxs-lookup"><span data-stu-id="e44fe-197">Added new commands for new LoadBalancer's subresource OutboundRule</span></span>
  - <span data-ttu-id="e44fe-198">Add-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e44fe-198">Add-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="e44fe-199">Get-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e44fe-199">Get-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="e44fe-200">New-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e44fe-200">New-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="e44fe-201">Set-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e44fe-201">Set-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="e44fe-202">Remove-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e44fe-202">Remove-AzureRmLoadBalancerOutboundRuleConfig</span></span>
* <span data-ttu-id="e44fe-203">Ny HostedWorkloads-egenskap har lagts till för PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="e44fe-203">Added new HostedWorkloads property for PSNetworkInterface</span></span>
* <span data-ttu-id="e44fe-204">Nya cmdletar har lagts till för funktionen: Azure Firewall via ARM</span><span class="sxs-lookup"><span data-stu-id="e44fe-204">Added new cmdlets for feature: Azure Firewall via ARM</span></span>
  - <span data-ttu-id="e44fe-205">Get-AzureRmFirewall har lagts till</span><span class="sxs-lookup"><span data-stu-id="e44fe-205">Added Get-AzureRmFirewall</span></span>
  - <span data-ttu-id="e44fe-206">Set-AzureRmFirewall har lagts till</span><span class="sxs-lookup"><span data-stu-id="e44fe-206">Added Set-AzureRmFirewall</span></span>
  - <span data-ttu-id="e44fe-207">New-AzureRmFirewall har lagts till</span><span class="sxs-lookup"><span data-stu-id="e44fe-207">Added New-AzureRmFirewall</span></span>
  - <span data-ttu-id="e44fe-208">Remove-AzureRmFirewall har lagts till</span><span class="sxs-lookup"><span data-stu-id="e44fe-208">Added Remove-AzureRmFirewall</span></span>
  - <span data-ttu-id="e44fe-209">New-AzureRmFirewallApplicationRuleCollection har lagts till</span><span class="sxs-lookup"><span data-stu-id="e44fe-209">Added New-AzureRmFirewallApplicationRuleCollection</span></span>
  - <span data-ttu-id="e44fe-210">New-AzureRmFirewallApplicationRule har lagts till</span><span class="sxs-lookup"><span data-stu-id="e44fe-210">Added New-AzureRmFirewallApplicationRule</span></span>
  - <span data-ttu-id="e44fe-211">New-AzureRmFirewallNatRuleCollection har lagts till</span><span class="sxs-lookup"><span data-stu-id="e44fe-211">Added New-AzureRmFirewallNatRuleCollection</span></span>
  - <span data-ttu-id="e44fe-212">New-AzureRmFirewallNatRule har lagts till</span><span class="sxs-lookup"><span data-stu-id="e44fe-212">Added New-AzureRmFirewallNatRule</span></span>
  - <span data-ttu-id="e44fe-213">New-AzureRmFirewallNetworkRuleCollection har lagts till</span><span class="sxs-lookup"><span data-stu-id="e44fe-213">Added New-AzureRmFirewallNetworkRuleCollection</span></span>
  - <span data-ttu-id="e44fe-214">New-AzureRmFirewallNetworkRule har lagts till</span><span class="sxs-lookup"><span data-stu-id="e44fe-214">Added New-AzureRmFirewallNetworkRule</span></span>
* <span data-ttu-id="e44fe-215">Stöd för betrott rotcertifikat och konfiguration för autoskalning har lagts till i Application Gateway</span><span class="sxs-lookup"><span data-stu-id="e44fe-215">Added support for Trusted Root certificate and Autoscale configuration in Application Gateway</span></span>
  - <span data-ttu-id="e44fe-216">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="e44fe-216">New Cmdlets added:</span></span>
      - <span data-ttu-id="e44fe-217">Add-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="e44fe-217">Add-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="e44fe-218">Get-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="e44fe-218">Get-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="e44fe-219">New-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="e44fe-219">New-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="e44fe-220">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="e44fe-220">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="e44fe-221">Set-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="e44fe-221">Set-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="e44fe-222">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="e44fe-222">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="e44fe-223">New-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="e44fe-223">New-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="e44fe-224">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="e44fe-224">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="e44fe-225">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="e44fe-225">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
  - <span data-ttu-id="e44fe-226">Cmdletar har uppdaterats med valfri parameter – TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="e44fe-226">Cmdlets updated with optonal parameter -TrustedRootCertificate</span></span>
      - <span data-ttu-id="e44fe-227">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e44fe-227">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="e44fe-228">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e44fe-228">Set-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="e44fe-229">New-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="e44fe-229">New-AzureRmApplicationGatewayBackendHttpSetting</span></span>
      - <span data-ttu-id="e44fe-230">Set-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="e44fe-230">Set-AzureRmApplicationGatewayBackendHttpSetting</span></span>
  - <span data-ttu-id="e44fe-231">Cmdletar har uppdaterats med valfri parameter – AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="e44fe-231">Cmdlets updated with optonal parameter -AutoscaleConfiguration</span></span>
      - <span data-ttu-id="e44fe-232">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e44fe-232">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="e44fe-233">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e44fe-233">Set-AzureRmApplicationGateway</span></span>
* <span data-ttu-id="e44fe-234">Lägg till cmdlet för gränssnittsslutpunkten Get-AzureInterfaceEndpoint</span><span class="sxs-lookup"><span data-stu-id="e44fe-234">Add cmdlet for Interface Endpoint Get-AzureInterfaceEndpoint</span></span>
* <span data-ttu-id="e44fe-235">Stöd för flera adressprefix i ett undernät har lagts till.</span><span class="sxs-lookup"><span data-stu-id="e44fe-235">Added support for multiple address prefixes in a subnet.</span></span> <span data-ttu-id="e44fe-236">Uppdaterade cmdletar:</span><span class="sxs-lookup"><span data-stu-id="e44fe-236">Updated cmdlets:</span></span>
  - <span data-ttu-id="e44fe-237">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="e44fe-237">New-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="e44fe-238">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="e44fe-238">Set-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="e44fe-239">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="e44fe-239">Add-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="e44fe-240">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="e44fe-240">Get-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="e44fe-241">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="e44fe-241">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>
  - <span data-ttu-id="e44fe-242">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="e44fe-242">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="e44fe-243">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="e44fe-243">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="e44fe-244">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="e44fe-244">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="e44fe-245">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="e44fe-245">Add-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="e44fe-246">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="e44fe-246">New-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="e44fe-247">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="e44fe-247">Set-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="e44fe-248">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="e44fe-248">Add-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="e44fe-249">New-AzureRmNetworkInterfaceIpConfig – Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="e44fe-249">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="e44fe-250">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="e44fe-250">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="e44fe-251">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="e44fe-251">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="e44fe-252">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="e44fe-252">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="e44fe-253">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="e44fe-253">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="e44fe-254">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="e44fe-254">New-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="e44fe-255">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="e44fe-255">New-AzureRmNetworkInterface</span></span>
* <span data-ttu-id="e44fe-256">Lägger till cmdletar för delegering av undernät.</span><span class="sxs-lookup"><span data-stu-id="e44fe-256">Adding cmdlets for subnet delegation.</span></span>
  - <span data-ttu-id="e44fe-257">New-AzureRmDelegation: Skapar en ny delegering som kan läggas till i ett undernät</span><span class="sxs-lookup"><span data-stu-id="e44fe-257">New-AzureRmDelegation: Creates a new delegation, which can be added to a subnet</span></span>
  - <span data-ttu-id="e44fe-258">Remove-AzureRmDelegation: Hämtar ett undernät och tar bort det angivna delegeringsnamnet från undernätet</span><span class="sxs-lookup"><span data-stu-id="e44fe-258">Remove-AzureRmDelegation: Takes in a subnet and removes the provided delegation name from that subnet</span></span>
  - <span data-ttu-id="e44fe-259">Add-AzureRmDelegation: Hämtar ett undernät och lägger till det angivna tjänstnamnet som en delegering till undernätet</span><span class="sxs-lookup"><span data-stu-id="e44fe-259">Add-AzureRmDelegation: Takes in a subnet and adds the provided service name as a delegation to that subnet</span></span>
  - <span data-ttu-id="e44fe-260">Get-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="e44fe-260">Get-AzureRmDelegation</span></span>
  - <span data-ttu-id="e44fe-261">Get-AzureRmAvailableServiceDelegations</span><span class="sxs-lookup"><span data-stu-id="e44fe-261">Get-AzureRmAvailableServiceDelegations</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="e44fe-262">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e44fe-262">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="e44fe-263">Stöd för hanterad disk</span><span class="sxs-lookup"><span data-stu-id="e44fe-263">Support for managed Managed disk</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="e44fe-264">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="e44fe-264">AzureRM.RedisCache</span></span>
* <span data-ttu-id="e44fe-265">Insights-beroende har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="e44fe-265">Updated Insights dependency.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="e44fe-266">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="e44fe-266">AzureRM.Resources</span></span>
* <span data-ttu-id="e44fe-267">Uppdatera New-AzureRmResourceGroupDeployment med den nya parametern RollbackAction</span><span class="sxs-lookup"><span data-stu-id="e44fe-267">Update New-AzureRmResourceGroupDeployment with new parameter RollbackAction</span></span>
    - <span data-ttu-id="e44fe-268">Lägg till stöd för OnErrorDeployment med den nya parametern.</span><span class="sxs-lookup"><span data-stu-id="e44fe-268">Add support for OnErrorDeployment with the new parameter.</span></span>
* <span data-ttu-id="e44fe-269">Stöd för hanterad identitet på principtilldelningar.</span><span class="sxs-lookup"><span data-stu-id="e44fe-269">Support managed identity on policy assignments.</span></span>
* <span data-ttu-id="e44fe-270">Parametrar med standardvärden krävs inte längre när du tilldelar en princip med ”New-AzureRmPolicyAssignment”</span><span class="sxs-lookup"><span data-stu-id="e44fe-270">Parameters with default values are no longer requred when assigning a policy with 'New-AzureRmPolicyAssignment'</span></span>
* <span data-ttu-id="e44fe-271">Lägg till den nya cmdleten Get-AzureRmPolicyAlias för att hämta principalias</span><span class="sxs-lookup"><span data-stu-id="e44fe-271">Add new cmdlet Get-AzureRmPolicyAlias for retrieving policy aliases</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="e44fe-272">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e44fe-272">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="e44fe-273">Problem #7161 har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="e44fe-273">Fixed issue #7161</span></span>

#### <a name="azurermsignalr"></a><span data-ttu-id="e44fe-274">AzureRM.SignalR</span><span class="sxs-lookup"><span data-stu-id="e44fe-274">AzureRM.SignalR</span></span>
* <span data-ttu-id="e44fe-275">Uppdatera SKU-namn till Free_F1 och Standard_S1</span><span class="sxs-lookup"><span data-stu-id="e44fe-275">Update SKU names to Free_F1 and Standard_S1</span></span>
* <span data-ttu-id="e44fe-276">Lägg till versionsfältet i PSSignalRResource-objektet och en anslutningssträng i PSSignalRKeys-objektet.</span><span class="sxs-lookup"><span data-stu-id="e44fe-276">Add version field to the PSSignalRResource object and connection string to the PSSignalRKeys object.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="e44fe-277">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="e44fe-277">AzureRM.Storage</span></span>
* <span data-ttu-id="e44fe-278">Stöd för oföränderlighetsprincip i AzureRm.Storage</span><span class="sxs-lookup"><span data-stu-id="e44fe-278">Support Immutability Policy in AzureRm.Storage</span></span> 
    - <span data-ttu-id="e44fe-279">Remove-AzureRmStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="e44fe-279">Remove-AzureRmStorageAccountNetworkRule</span></span>
    - <span data-ttu-id="e44fe-280">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="e44fe-280">Get-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="e44fe-281">Update-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="e44fe-281">Update-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="e44fe-282">New-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="e44fe-282">New-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="e44fe-283">Remove-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="e44fe-283">Remove-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="e44fe-284">Add-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="e44fe-284">Add-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="e44fe-285">Remove-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="e44fe-285">Remove-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="e44fe-286">Set-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="e44fe-286">Set-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="e44fe-287">Get-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="e44fe-287">Get-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="e44fe-288">Remove-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="e44fe-288">Remove-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="e44fe-289">Lock-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="e44fe-289">Lock-AzureRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="e44fe-290">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="e44fe-290">AzureRM.Websites</span></span>
* <span data-ttu-id="e44fe-291">Två nya cmdletar har lagts till: Get-AzureRmDeletedWebApp och Restore-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="e44fe-291">Added two new cmdlets: Get-AzureRmDeletedWebApp and Restore-AzureRmDeletedWebApp</span></span>
* <span data-ttu-id="e44fe-292">New-AzureRmAppServicePlan – En HyperV-växel har lagts till för skapa en app service-plan med Windows-containrar</span><span class="sxs-lookup"><span data-stu-id="e44fe-292">New-AzureRmAppServicePlan -HyperV switch is added for create app service plan with windows container</span></span>
* <span data-ttu-id="e44fe-293">New-AzureRmWebApp/New-AzureRmWebAppSlot/Set-AzureRmWebApp/Set-AzureRmWebAppSlot – Nya parametrar (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) har lagts till för att skapa och hantera Windows-containerappar</span><span class="sxs-lookup"><span data-stu-id="e44fe-293">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - New parameters (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) added for creating and managing windows container app</span></span>

## <a name="681---august-2018"></a><span data-ttu-id="e44fe-294">6.8.1 – augusti 2018</span><span class="sxs-lookup"><span data-stu-id="e44fe-294">6.8.1 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="e44fe-295">Allmänt</span><span class="sxs-lookup"><span data-stu-id="e44fe-295">General</span></span>
* <span data-ttu-id="e44fe-296">Problem med standardresursgrupp som inte har konfigurerats har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="e44fe-296">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="e44fe-297">Uppdaterade Common Runtime-sammansättningar</span><span class="sxs-lookup"><span data-stu-id="e44fe-297">Updated common runtime assemblies</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="e44fe-298">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e44fe-298">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="e44fe-299">Problem med standardresursgrupp som inte har konfigurerats har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="e44fe-299">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="e44fe-300">Åtgärdat problem https://github.com/Azure/azure-powershell/issues/6603</span><span class="sxs-lookup"><span data-stu-id="e44fe-300">Fixed issue https://github.com/Azure/azure-powershell/issues/6603</span></span>
    - <span data-ttu-id="e44fe-301">Import-AzureRmApiManagementApi- och \*-AzureRmApiManagementCertificate-cmdletar kan nu hantera relativa sökvägar</span><span class="sxs-lookup"><span data-stu-id="e44fe-301">Import-AzureRmApiManagementApi and \*-AzureRmApiManagementCertificate cmdlets now handle relative Paths</span></span>
* <span data-ttu-id="e44fe-302">Åtgärdat problem https://github.com/Azure/azure-powershell/issues/6879</span><span class="sxs-lookup"><span data-stu-id="e44fe-302">Fixed issue https://github.com/Azure/azure-powershell/issues/6879</span></span>
    - <span data-ttu-id="e44fe-303">CertificateInformation är en inställbar egenskap som gör att Set-AzureRmApiManagement-cmdleten fungerar ordentligt.</span><span class="sxs-lookup"><span data-stu-id="e44fe-303">The CertificateInformation is a settable property allowing for Set-AzureRmApiManagement cmdlet to work property.</span></span> <span data-ttu-id="e44fe-304">Åtgärdat genom uppgradering till NuGet för 4.0.4-preview</span><span class="sxs-lookup"><span data-stu-id="e44fe-304">Fixed by upgrading to 4.0.4-preview nuget</span></span>
* <span data-ttu-id="e44fe-305">Åtgärdat problem https://github.com/Azure/azure-powershell/issues/6853</span><span class="sxs-lookup"><span data-stu-id="e44fe-305">Fixed issue https://github.com/Azure/azure-powershell/issues/6853</span></span>
    - <span data-ttu-id="e44fe-306">Odata-filtret för sökning efter namn på produkt har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="e44fe-306">Fixed the Odata filter for Search by Name on Product</span></span>
* <span data-ttu-id="e44fe-307">Åtgärdat problem https://github.com/Azure/azure-powershell/issues/6814</span><span class="sxs-lookup"><span data-stu-id="e44fe-307">Fixed issue https://github.com/Azure/azure-powershell/issues/6814</span></span>
    - <span data-ttu-id="e44fe-308">Odata-filtret för sökning efter namn på API har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="e44fe-308">Fixed the Odata filter for Search by Name on Api</span></span>
* <span data-ttu-id="e44fe-309">Stöd har lagts till för AzureMonitor-loggare</span><span class="sxs-lookup"><span data-stu-id="e44fe-309">Added support for AzureMonitor logger</span></span>


#### <a name="azurermcompute"></a><span data-ttu-id="e44fe-310">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="e44fe-310">AzureRM.Compute</span></span>
* <span data-ttu-id="e44fe-311">Ett problem med att mål saknas i felutdata har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="e44fe-311">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="e44fe-312">Problem med lagringskontotyper för virtuell dator med en hanterad disk har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="e44fe-312">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="e44fe-313">Problem med standardresursgrupp som inte har konfigurerats har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="e44fe-313">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="e44fe-314">Åtgärda cmdletar för AEM-tillägg för andra miljöer, till exempel Azure Kina</span><span class="sxs-lookup"><span data-stu-id="e44fe-314">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="e44fe-315">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="e44fe-315">AzureRM.Network</span></span>
* <span data-ttu-id="e44fe-316">Standardvisning av cmdlet-utdata har ändrats för att visas i tabellvy</span><span class="sxs-lookup"><span data-stu-id="e44fe-316">Changed default cmdlet output presentation to table view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="e44fe-317">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="e44fe-317">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="e44fe-318">Åtgärda fel i Update-AzureRmPowerBIEmbeddedCapacity vid försök att skala pausad kapacitet</span><span class="sxs-lookup"><span data-stu-id="e44fe-318">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>


#### <a name="azurermresources"></a><span data-ttu-id="e44fe-319">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="e44fe-319">AzureRM.Resources</span></span>
* <span data-ttu-id="e44fe-320">Ett problem med att skapa hanterade program från MarketPlace har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="e44fe-320">Fixed issue with creating managed applications from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="e44fe-321">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e44fe-321">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="e44fe-322">Åtgärdade problem</span><span class="sxs-lookup"><span data-stu-id="e44fe-322">Fixed issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="e44fe-323">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="e44fe-323">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="e44fe-324">Stöd har lagts till för trafikroutningsmetoden MultiValue</span><span class="sxs-lookup"><span data-stu-id="e44fe-324">Added Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="e44fe-325">Ny parameter, ”MaxReturn”, för MultiValue-routning</span><span class="sxs-lookup"><span data-stu-id="e44fe-325">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="e44fe-326">Stöd har lagts till för trafikroutningsmetod för undernät</span><span class="sxs-lookup"><span data-stu-id="e44fe-326">Added Support for the Subnet routing method</span></span>
    - <span data-ttu-id="e44fe-327">Stöd för IP-adressintervall (undernät) i slutpunkter</span><span class="sxs-lookup"><span data-stu-id="e44fe-327">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="e44fe-328">Stöd har lagts till för anpassade rubriker i profiler</span><span class="sxs-lookup"><span data-stu-id="e44fe-328">Added Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="e44fe-329">Stöd har lagts till för förväntade statuskodintervall i profiler</span><span class="sxs-lookup"><span data-stu-id="e44fe-329">Added Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="e44fe-330">Stöd har lagts till för anpassade rubriker i slutpunkter</span><span class="sxs-lookup"><span data-stu-id="e44fe-330">Added Support for Custom Headers in endpoints</span></span>

## <a name="680---august-2018"></a><span data-ttu-id="e44fe-331">6.8.0 – augusti 2018</span><span class="sxs-lookup"><span data-stu-id="e44fe-331">6.8.0 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="e44fe-332">Allmänt</span><span class="sxs-lookup"><span data-stu-id="e44fe-332">General</span></span>
* <span data-ttu-id="e44fe-333">Problem med standardresursgrupp som inte har konfigurerats har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="e44fe-333">Fixed issue with default resource groups not being set.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="e44fe-334">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="e44fe-334">AzureRM.Profile</span></span>
* <span data-ttu-id="e44fe-335">Utgångsegenskap har lagts till i token som returneras under Connect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="e44fe-335">Added expiration property to tokens returned during Connect-AzureRmAccount</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="e44fe-336">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="e44fe-336">AzureRM.Compute</span></span>
* <span data-ttu-id="e44fe-337">Ett problem med att mål saknas i felutdata har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="e44fe-337">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="e44fe-338">Problem med lagringskontotyper för virtuell dator med en hanterad disk har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="e44fe-338">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="e44fe-339">Åtgärda cmdletar för AEM-tillägg för andra miljöer, till exempel Azure Kina</span><span class="sxs-lookup"><span data-stu-id="e44fe-339">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="e44fe-340">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="e44fe-340">AzureRM.IotHub</span></span>
* <span data-ttu-id="e44fe-341">Korrigera exempel för New-AzureRmIotHubExportDevices och New-AzureRmIotHubImportDevices</span><span class="sxs-lookup"><span data-stu-id="e44fe-341">Fix examples for New-AzureRmIotHubExportDevices and New-AzureRmIotHubImportDevices</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="e44fe-342">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="e44fe-342">AzureRM.Network</span></span>
* <span data-ttu-id="e44fe-343">Standardmodeller har ändrats för att visas i tabellvy</span><span class="sxs-lookup"><span data-stu-id="e44fe-343">Changed default models representation to table-view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="e44fe-344">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="e44fe-344">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="e44fe-345">Åtgärda fel i Update-AzureRmPowerBIEmbeddedCapacity vid försök att skala pausad kapacitet</span><span class="sxs-lookup"><span data-stu-id="e44fe-345">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="e44fe-346">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="e44fe-346">AzureRM.Resources</span></span>
* <span data-ttu-id="e44fe-347">Ett problem med att skapa hanterade program från MarketPlace har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="e44fe-347">Fixed issue with creating managed application from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="e44fe-348">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e44fe-348">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="e44fe-349">Korrigeringar för problem</span><span class="sxs-lookup"><span data-stu-id="e44fe-349">Fix for issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="e44fe-350">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="e44fe-350">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="e44fe-351">Stöd för trafikroutningsmetoden MultiValue</span><span class="sxs-lookup"><span data-stu-id="e44fe-351">Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="e44fe-352">Ny parameter, ”MaxReturn”, för MultiValue-routning</span><span class="sxs-lookup"><span data-stu-id="e44fe-352">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="e44fe-353">Stöd för trafikroutningsmetod för undernät</span><span class="sxs-lookup"><span data-stu-id="e44fe-353">Support for the Subnet routing method</span></span>
    - <span data-ttu-id="e44fe-354">Stöd för IP-adressintervall (undernät) i slutpunkter</span><span class="sxs-lookup"><span data-stu-id="e44fe-354">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="e44fe-355">Stöd för anpassade rubriker i profiler</span><span class="sxs-lookup"><span data-stu-id="e44fe-355">Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="e44fe-356">Stöd för förväntade statuskodintervall i profiler</span><span class="sxs-lookup"><span data-stu-id="e44fe-356">Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="e44fe-357">Stöd för anpassade rubriker i slutpunkter</span><span class="sxs-lookup"><span data-stu-id="e44fe-357">Support for Custom Headers in endpoints</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="e44fe-358">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="e44fe-358">AzureRM.Websites</span></span>
* <span data-ttu-id="e44fe-359">Problem med standardresursgrupp som inte har konfigurerats korrekt har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="e44fe-359">Fixed issue with default resource group being set incorrectly.</span></span>

## <a name="670---august-2018"></a><span data-ttu-id="e44fe-360">6.7.0 – augusti 2018</span><span class="sxs-lookup"><span data-stu-id="e44fe-360">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="e44fe-361">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="e44fe-361">AzureRM.Profile</span></span>
* <span data-ttu-id="e44fe-362">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e44fe-362">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="e44fe-363">Lägg till användar-id i standardkontextnamnet för att undvika kontextkonflikter</span><span class="sxs-lookup"><span data-stu-id="e44fe-363">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="e44fe-364">Åtgärda problem med Clear-AzureRmContext som orsakade problem med att välja en kontext #6398</span><span class="sxs-lookup"><span data-stu-id="e44fe-364">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="e44fe-365">Aktivera den klientorganisationsdomän som ska skickas till parametern -TenantId för Connect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="e44fe-365">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="e44fe-366">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="e44fe-366">Azure.Storage</span></span>
* <span data-ttu-id="e44fe-367">Ta bort begränsningen på 5 TB för Azure-filresurskvoten</span><span class="sxs-lookup"><span data-stu-id="e44fe-367">Remove the 5TB limitation for Azure File Share quota</span></span>
- <span data-ttu-id="e44fe-368">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="e44fe-368">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="e44fe-369">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="e44fe-369">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="e44fe-370">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e44fe-370">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="e44fe-371">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="e44fe-371">Azure.AnalysisServices</span></span>
* <span data-ttu-id="e44fe-372">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e44fe-372">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="e44fe-373">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e44fe-373">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="e44fe-374">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e44fe-374">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="e44fe-375">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="e44fe-375">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="e44fe-376">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e44fe-376">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="e44fe-377">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="e44fe-377">AzureRM.Automation</span></span>
* <span data-ttu-id="e44fe-378">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e44fe-378">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="e44fe-379">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="e44fe-379">AzureRM.Backup</span></span>
* <span data-ttu-id="e44fe-380">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e44fe-380">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="e44fe-381">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="e44fe-381">AzureRM.Batch</span></span>
* <span data-ttu-id="e44fe-382">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e44fe-382">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="e44fe-383">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="e44fe-383">AzureRM.Billing</span></span>
* <span data-ttu-id="e44fe-384">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e44fe-384">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="e44fe-385">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="e44fe-385">AzureRM.Cdn</span></span>
* <span data-ttu-id="e44fe-386">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e44fe-386">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="e44fe-387">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e44fe-387">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="e44fe-388">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e44fe-388">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="e44fe-389">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="e44fe-389">AzureRM.Compute</span></span>
* <span data-ttu-id="e44fe-390">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e44fe-390">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="e44fe-391">Lägg till parametern EvictionPolicy i New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="e44fe-391">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="e44fe-392">Använd standardplatsen i DiskFileParameterSet för New-AzureRmVm om ingen plats har angetts.</span><span class="sxs-lookup"><span data-stu-id="e44fe-392">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="e44fe-393">Korrigera parameterbeskrivningen i Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="e44fe-393">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="e44fe-394">Korrigera cmdleten Get-AzureRmVMDiskEncryptionStatus för vissa singlepass-relaterade scenarier</span><span class="sxs-lookup"><span data-stu-id="e44fe-394">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="e44fe-395">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="e44fe-395">AzureRM.Consumption</span></span>
* <span data-ttu-id="e44fe-396">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e44fe-396">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="e44fe-397">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="e44fe-397">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="e44fe-398">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e44fe-398">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="e44fe-399">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="e44fe-399">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="e44fe-400">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e44fe-400">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="e44fe-401">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="e44fe-401">AzureRM.DataFactories</span></span>
* <span data-ttu-id="e44fe-402">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e44fe-402">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="e44fe-403">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="e44fe-403">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="e44fe-404">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e44fe-404">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="e44fe-405">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="e44fe-405">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="e44fe-406">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e44fe-406">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="e44fe-407">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e44fe-407">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="e44fe-408">Korrigera felsökning när DebugPreference anges från powershell-kommandoraden</span><span class="sxs-lookup"><span data-stu-id="e44fe-408">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="e44fe-409">Uppdatera exemplet för Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="e44fe-409">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="e44fe-410">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e44fe-410">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="e44fe-411">Uppdatera exemplet för Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="e44fe-411">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="e44fe-412">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="e44fe-412">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="e44fe-413">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e44fe-413">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="e44fe-414">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="e44fe-414">AzureRM.Dns</span></span>
* <span data-ttu-id="e44fe-415">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e44fe-415">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="e44fe-416">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="e44fe-416">AzureRM.EventGrid</span></span>
* <span data-ttu-id="e44fe-417">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e44fe-417">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="e44fe-418">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="e44fe-418">AzureRM.EventHub</span></span>
* <span data-ttu-id="e44fe-419">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e44fe-419">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="e44fe-420">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="e44fe-420">AzureRM.HDInsight</span></span>
* <span data-ttu-id="e44fe-421">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e44fe-421">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="e44fe-422">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="e44fe-422">AzureRM.Insights</span></span>
* <span data-ttu-id="e44fe-423">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e44fe-423">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="e44fe-424">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="e44fe-424">AzureRM.IotHub</span></span>
* <span data-ttu-id="e44fe-425">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e44fe-425">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="e44fe-426">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e44fe-426">AzureRM.KeyVault</span></span>
* <span data-ttu-id="e44fe-427">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e44fe-427">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="e44fe-428">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="e44fe-428">AzureRM.LogicApp</span></span>
* <span data-ttu-id="e44fe-429">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e44fe-429">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="e44fe-430">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="e44fe-430">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="e44fe-431">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e44fe-431">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="e44fe-432">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="e44fe-432">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="e44fe-433">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e44fe-433">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="e44fe-434">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="e44fe-434">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="e44fe-435">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e44fe-435">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="e44fe-436">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="e44fe-436">AzureRM.Media</span></span>
* <span data-ttu-id="e44fe-437">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e44fe-437">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="e44fe-438">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="e44fe-438">AzureRM.Network</span></span>
* <span data-ttu-id="e44fe-439">Exempel för Set-AzureRmLocalNetworkGateway har lagts till</span><span class="sxs-lookup"><span data-stu-id="e44fe-439">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="e44fe-440">Exempel och beskrivningar för Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey och New-AzureRmVirtualNetworkGatewayConnection har lagts till</span><span class="sxs-lookup"><span data-stu-id="e44fe-440">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="e44fe-441">Exempel för Remove-AzureRmVirtualNetworkGatewayIpConfig och Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e44fe-441">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="e44fe-442">Exempel för Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey har lagts till</span><span class="sxs-lookup"><span data-stu-id="e44fe-442">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="e44fe-443">Exempel för Set-AzureRmVirtualNetworkGatewayConnectionSharedKey har lagts till</span><span class="sxs-lookup"><span data-stu-id="e44fe-443">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="e44fe-444">Exempel för Set-AzureRmVirtualNetworkGatewayConnection har lagts till</span><span class="sxs-lookup"><span data-stu-id="e44fe-444">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="e44fe-445">Cmdletar för ApplicationSecurityGroup, RouteTable and Usage har genererats om med den senaste kodgeneratorn</span><span class="sxs-lookup"><span data-stu-id="e44fe-445">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="e44fe-446">Förtydligade ett felmeddelande för Get-AzureRmVirtualNetworkSubnetConfig vid försök att hämta ett undernät som inte avslutas</span><span class="sxs-lookup"><span data-stu-id="e44fe-446">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="e44fe-447">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="e44fe-447">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="e44fe-448">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e44fe-448">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="e44fe-449">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e44fe-449">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="e44fe-450">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e44fe-450">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="e44fe-451">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="e44fe-451">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="e44fe-452">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e44fe-452">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="e44fe-453">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="e44fe-453">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="e44fe-454">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e44fe-454">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="e44fe-455">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e44fe-455">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="e44fe-456">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e44fe-456">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="e44fe-457">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e44fe-457">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="e44fe-458">Lade till principfilter i cmdleten Get-AzureRmRecoveryServicesBackItem.</span><span class="sxs-lookup"><span data-stu-id="e44fe-458">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="e44fe-459">Kommandot returnerar listan med säkerhetskopieringsobjekt som skyddas av det angivna princip-ID:t.</span><span class="sxs-lookup"><span data-stu-id="e44fe-459">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="e44fe-460">Microsoft.Azure.Management.RecoveryServices.Backup uppdaterades till förhandsversionen av 3.0.0.</span><span class="sxs-lookup"><span data-stu-id="e44fe-460">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="e44fe-461">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e44fe-461">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="e44fe-462">Parametern TargetResourceGroupName lades till i Restore-AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="e44fe-462">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="e44fe-463">Den resursgrupp som de hanterade diskarna återställs till.</span><span class="sxs-lookup"><span data-stu-id="e44fe-463">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="e44fe-464">Gäller för säkerhetskopiering av virtuell dator med hanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="e44fe-464">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="e44fe-465">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e44fe-465">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="e44fe-466">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e44fe-466">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="e44fe-467">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="e44fe-467">AzureRM.RedisCache</span></span>
* <span data-ttu-id="e44fe-468">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e44fe-468">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="e44fe-469">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="e44fe-469">AzureRM.Relay</span></span>
* <span data-ttu-id="e44fe-470">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e44fe-470">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="e44fe-471">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="e44fe-471">AzureRM.Resources</span></span>
* <span data-ttu-id="e44fe-472">Distribution av supportmall i prenumerationsomfånget.</span><span class="sxs-lookup"><span data-stu-id="e44fe-472">Support template deployment at subscription scope.</span></span> <span data-ttu-id="e44fe-473">Lägg till nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="e44fe-473">Add new Cmdlets:</span></span>
    - <span data-ttu-id="e44fe-474">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="e44fe-474">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="e44fe-475">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="e44fe-475">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="e44fe-476">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="e44fe-476">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="e44fe-477">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="e44fe-477">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="e44fe-478">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="e44fe-478">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="e44fe-479">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="e44fe-479">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="e44fe-480">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="e44fe-480">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="e44fe-481">Korrigera ett problem där fel inträffar när en kontext skickas till Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="e44fe-481">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="e44fe-482">Korrigera exempel i New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e44fe-482">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="e44fe-483">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e44fe-483">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="e44fe-484">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="e44fe-484">AzureRM.Scheduler</span></span>
* <span data-ttu-id="e44fe-485">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e44fe-485">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="e44fe-486">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e44fe-486">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="e44fe-487">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e44fe-487">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="e44fe-488">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e44fe-488">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="e44fe-489">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e44fe-489">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="e44fe-490">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="e44fe-490">AzureRM.Sql</span></span>
* <span data-ttu-id="e44fe-491">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e44fe-491">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="e44fe-492">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="e44fe-492">AzureRM.Storage</span></span>
* <span data-ttu-id="e44fe-493">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e44fe-493">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="e44fe-494">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="e44fe-494">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="e44fe-495">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e44fe-495">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="e44fe-496">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="e44fe-496">AzureRM.Tags</span></span>
* <span data-ttu-id="e44fe-497">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e44fe-497">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="e44fe-498">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="e44fe-498">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="e44fe-499">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e44fe-499">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="e44fe-500">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="e44fe-500">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="e44fe-501">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e44fe-501">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="e44fe-502">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="e44fe-502">AzureRM.Websites</span></span>
* <span data-ttu-id="e44fe-503">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e44fe-503">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="e44fe-504">6.6.0 – juli 2018</span><span class="sxs-lookup"><span data-stu-id="e44fe-504">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="e44fe-505">Allmänt</span><span class="sxs-lookup"><span data-stu-id="e44fe-505">General</span></span>
* <span data-ttu-id="e44fe-506">Alla hjälpfiler har uppdaterats för att ta med fullständiga parametertyper och korrekta indata-/utdatatyper.</span><span class="sxs-lookup"><span data-stu-id="e44fe-506">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="e44fe-507">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="e44fe-507">AzureRM.Profile</span></span>
* <span data-ttu-id="e44fe-508">Common.Strategy-biblioteket har uppdaterats för att kunna verifiera att den aktuella konfigurationsfilen för en resurs är kompatibel med målresursen.</span><span class="sxs-lookup"><span data-stu-id="e44fe-508">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="e44fe-509">ps1xml-typer har lagts till i Common.Storage</span><span class="sxs-lookup"><span data-stu-id="e44fe-509">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="e44fe-510">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="e44fe-510">Azure.Storage</span></span>
* <span data-ttu-id="e44fe-511">Lade till stöd för hämtning av lagringskontext från DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e44fe-511">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="e44fe-512">Lade till Ps1XmlAttribute till utdatatypegenskaper för cmdletar.</span><span class="sxs-lookup"><span data-stu-id="e44fe-512">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="e44fe-513">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e44fe-513">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="e44fe-514">Åtgärdat problem https://github.com/Azure/azure-powershell/issues/6370</span><span class="sxs-lookup"><span data-stu-id="e44fe-514">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="e44fe-515">En bugg har åtgärdats i Automapper för att översätta PsApiManagementApi till ApiContract</span><span class="sxs-lookup"><span data-stu-id="e44fe-515">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="e44fe-516">Åtgärdat problem https://github.com/Azure/azure-powershell/issues/6515</span><span class="sxs-lookup"><span data-stu-id="e44fe-516">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="e44fe-517">En bugg har åtgärdats i File.Save för att inte överbelasta kodningstypen</span><span class="sxs-lookup"><span data-stu-id="e44fe-517">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="e44fe-518">Åtgärdat problem https://github.com/Azure/azure-powershell/issues/6560</span><span class="sxs-lookup"><span data-stu-id="e44fe-518">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="e44fe-519">Har uppgraderats till Nuget-versionen 4.0.3 vilket åtgärdar mönsterundantaget på apiId</span><span class="sxs-lookup"><span data-stu-id="e44fe-519">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="e44fe-520">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="e44fe-520">AzureRM.Compute</span></span>
* <span data-ttu-id="e44fe-521">Åtgärda problem med fel vid skapandet av en virtuell dator med hjälp av DiskFileParameterSet i New-AzureRmVm på grund av namnbyte på PremiumLRS-lagringskontotypen.</span><span class="sxs-lookup"><span data-stu-id="e44fe-521">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="e44fe-522">Åtgärda cmdleten Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="e44fe-522">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="e44fe-523">Uppdatera Get-AzureRmAvailabilitySet för att aktivera funktionen för att lista alla tillgänglighetsuppsättningar i en prenumeration.</span><span class="sxs-lookup"><span data-stu-id="e44fe-523">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="e44fe-524">(Parametern ResouceGroupName är nu frivillig.)</span><span class="sxs-lookup"><span data-stu-id="e44fe-524">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="e44fe-525">Uppdatera SimpleParameterSet för "New-AzureRmVm" för att aktivera accelererat nätverk på berättigade virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="e44fe-525">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="e44fe-526">Uppdatera den enkla parameteruppsättningen för New-AzureRmVmss så att det inte går att skapa de virtuella datorerna när en användarangiven lastbalanserare redan finns.</span><span class="sxs-lookup"><span data-stu-id="e44fe-526">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="e44fe-527">Uppdatera exempel för New-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="e44fe-527">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="e44fe-528">Lägg till exempel för "New-AzureRmVM"</span><span class="sxs-lookup"><span data-stu-id="e44fe-528">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="e44fe-529">Uppdatera beskrivning för Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="e44fe-529">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="e44fe-530">Uppdatera Exempel 1 för Set-AzureRmVMBginfoExtension för stavningskontroll och prefix.</span><span class="sxs-lookup"><span data-stu-id="e44fe-530">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="e44fe-531">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="e44fe-531">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="e44fe-532">ADF .Net SDK-versionen har uppdaterats till 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="e44fe-532">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="e44fe-533">Stöd för delning av Integration Runtime (lokal installation) mellan datafabriker.</span><span class="sxs-lookup"><span data-stu-id="e44fe-533">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="e44fe-534">Lägg till ny parameter – SharedIntegrationRuntimeResourceId i cmdleten Set-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="e44fe-534">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="e44fe-535">Lägg till ny valfri parameter – LinkedDataFactoryName i cmdleten Remove-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="e44fe-535">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="e44fe-536">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e44fe-536">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="e44fe-537">DataPlane SDK-versionen (Microsoft.Azure.DataLake.Store) har uppdaterats till 1.1.9</span><span class="sxs-lookup"><span data-stu-id="e44fe-537">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="e44fe-538">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="e44fe-538">AzureRM.EventHub</span></span>
* <span data-ttu-id="e44fe-539">Piping för InputObject and ResourceId i borttagna cmdletar har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="e44fe-539">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="e44fe-540">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="e44fe-540">AzureRM.Insights</span></span>
* <span data-ttu-id="e44fe-541">Formatering har åtgärdats för OutputType i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="e44fe-541">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="e44fe-542">Använda Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span><span class="sxs-lookup"><span data-stu-id="e44fe-542">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="e44fe-543">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e44fe-543">AzureRM.KeyVault</span></span>
* <span data-ttu-id="e44fe-544">Åtgärda problem med piping i Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e44fe-544">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="e44fe-545">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="e44fe-545">AzureRM.Network</span></span>
* <span data-ttu-id="e44fe-546">Exempel har lagts till för LoadBalancerInboundNatPoolConfig-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="e44fe-546">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="e44fe-547">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="e44fe-547">AzureRM.Resources</span></span>
* <span data-ttu-id="e44fe-548">Åtgärda problem när både taggnamn och värde anges för "Get-AzureRmResource"</span><span class="sxs-lookup"><span data-stu-id="e44fe-548">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="e44fe-549">Åtgärda pipingscenario med "Set-AzureRmResource"</span><span class="sxs-lookup"><span data-stu-id="e44fe-549">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="e44fe-550">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e44fe-550">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="e44fe-551">Piping för InputObject and ResourceId i borttagna cmdletar har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="e44fe-551">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="e44fe-552">några problem har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="e44fe-552">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="e44fe-553">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="e44fe-553">AzureRM.Sql</span></span>
* <span data-ttu-id="e44fe-554">Lägg till stöd för Server Advanced Threat Protection med följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="e44fe-554">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="e44fe-555">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="e44fe-555">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="e44fe-556">Lägg till stöd för Sårbarhetsbedömning med följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="e44fe-556">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="e44fe-557">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="e44fe-557">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="e44fe-558">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="e44fe-558">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="e44fe-559">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="e44fe-559">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="e44fe-560">Exempel i Remove-AzureRmSqlServerFirewallRule har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="e44fe-560">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="e44fe-561">Åtgärda felaktig hantering av datum och tid för andra kulturer än usa-baserade kulturer i Get-AzureSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="e44fe-561">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="e44fe-562">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="e44fe-562">AzureRM.Storage</span></span>
* <span data-ttu-id="e44fe-563">Lägg till Ps1XmlAttribute i utdatatypegenskaper för cmdletar</span><span class="sxs-lookup"><span data-stu-id="e44fe-563">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="e44fe-564">Visa utdata för cmdleten StorageAccount i tabellvyn</span><span class="sxs-lookup"><span data-stu-id="e44fe-564">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="e44fe-565">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e44fe-565">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="e44fe-566">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e44fe-566">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="e44fe-567">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e44fe-567">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="e44fe-568">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="e44fe-568">AzureRM.Tags</span></span>
* <span data-ttu-id="e44fe-569">Ta bort felaktig instruktion från hjälpen för cmdleten Tag</span><span class="sxs-lookup"><span data-stu-id="e44fe-569">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="e44fe-570">6.5.0 – juli 2018</span><span class="sxs-lookup"><span data-stu-id="e44fe-570">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="e44fe-571">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="e44fe-571">AzureRM.Profile</span></span>
* <span data-ttu-id="e44fe-572">Hjälp för ”Get-AzureRmContextAutosaveSetting” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="e44fe-572">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="e44fe-573">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="e44fe-573">Azure.Storage</span></span>
* <span data-ttu-id="e44fe-574">Stöd för uppladdning av blob eller fil med lässkyddad SAS-token</span><span class="sxs-lookup"><span data-stu-id="e44fe-574">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="e44fe-575">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="e44fe-575">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="e44fe-576">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="e44fe-576">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="e44fe-577">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="e44fe-577">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="e44fe-578">Lägg till den nödvändiga egenskapen ResourceGroupName i AS.</span><span class="sxs-lookup"><span data-stu-id="e44fe-578">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="e44fe-579">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="e44fe-579">AzureRM.Automation</span></span>
* <span data-ttu-id="e44fe-580">Uppdatera hjälp och lägg till exempel för ”New-AzureRMAutomationSchedule”</span><span class="sxs-lookup"><span data-stu-id="e44fe-580">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="e44fe-581">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="e44fe-581">AzureRM.Compute</span></span>
* <span data-ttu-id="e44fe-582">Lägg till parametern -Tag förUpdate/New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="e44fe-582">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="e44fe-583">Lägg till exempel för ”Add-AzureRmVmssExtension”</span><span class="sxs-lookup"><span data-stu-id="e44fe-583">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="e44fe-584">Lägg till exempel för ”Remove-AzureRmVmssExtension”</span><span class="sxs-lookup"><span data-stu-id="e44fe-584">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="e44fe-585">Uppdatera hjälp för ”Set-AzureRmVMAccessExtension”</span><span class="sxs-lookup"><span data-stu-id="e44fe-585">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="e44fe-586">Uppdatera SimpleParameterSet för New-AzureRmVmss för att ställa in SinglePlacementGroup på falskt som standard och lägg till växlingsparametern ”SinglePlacementGroup” som gör att användare kan skapa VMSS i en enda placeringsgrupp.</span><span class="sxs-lookup"><span data-stu-id="e44fe-586">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="e44fe-587">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="e44fe-587">AzureRM.EventHub</span></span>
* <span data-ttu-id="e44fe-588">En skrivskyddad egenskap, ”PendingReplicationOperationsCount”, har lagts till för klassen PSEventHubDRConfigurationAttributes som anger antalet väntande replikeringsåtgärder medan replikeringen pågår</span><span class="sxs-lookup"><span data-stu-id="e44fe-588">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="e44fe-589">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e44fe-589">AzureRM.KeyVault</span></span>
* <span data-ttu-id="e44fe-590">Uppdatera felmeddelande för Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e44fe-590">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="e44fe-591">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="e44fe-591">AzureRM.LogicApp</span></span>
* <span data-ttu-id="e44fe-592">Felet ”parameteruppsättningen gick inte att matcha” har korrigerats i New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="e44fe-592">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="e44fe-593">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="e44fe-593">AzureRM.Network</span></span>
* <span data-ttu-id="e44fe-594">Aktivera peering mellan virtuella nätverk i flera klienter för Set/Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="e44fe-594">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="e44fe-595">Nedanstående cmdletar för Application Gateway har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="e44fe-595">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="e44fe-596">New-AzureRmApplicationGateway: EnableFIPS-flagga har lagts till för stöd för zoner</span><span class="sxs-lookup"><span data-stu-id="e44fe-596">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="e44fe-597">New-AzureRmApplicationGatewaySku: nya SKU:er, Standard_v2 och WAF_v2, har lagts till</span><span class="sxs-lookup"><span data-stu-id="e44fe-597">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="e44fe-598">Set-AzureRmApplicationGatewaySku: nya SKU:er, Standard_v2 och WAF_v2, har lagts till</span><span class="sxs-lookup"><span data-stu-id="e44fe-598">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="e44fe-599">RouteTable-cmdletar har återskapats med den senaste versionen av generatorn</span><span class="sxs-lookup"><span data-stu-id="e44fe-599">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="e44fe-600">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="e44fe-600">AzureRM.Relay</span></span>
* <span data-ttu-id="e44fe-601">Markdown-filer har uppdaterats och korrigerar problem med parameternamn i exemplet</span><span class="sxs-lookup"><span data-stu-id="e44fe-601">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="e44fe-602">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="e44fe-602">AzureRM.Resources</span></span>
* <span data-ttu-id="e44fe-603">Uppdatera cmdletar för rolltilldelning och rolldefinition:</span><span class="sxs-lookup"><span data-stu-id="e44fe-603">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="e44fe-604">Ta bort extra anrop för rolldefinitioner som görs som en del av sidindelning.</span><span class="sxs-lookup"><span data-stu-id="e44fe-604">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="e44fe-605">Åtgärda Get-AzureRMRoleAssignment-cmdlet</span><span class="sxs-lookup"><span data-stu-id="e44fe-605">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="e44fe-606">Åtgärda parameterfunktioner för kommandot -ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="e44fe-606">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="e44fe-607">Åtgärda problem med ”Get-AzureRmResource” där ”-ResourceType”-parametern var skiftlägeskänsligt</span><span class="sxs-lookup"><span data-stu-id="e44fe-607">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="e44fe-608">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e44fe-608">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="e44fe-609">Parametrar för att stoppa och hoppa över har lagts till i listan över cmdletar</span><span class="sxs-lookup"><span data-stu-id="e44fe-609">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="e44fe-610">Cmdletar för migrering från Standard- till Premium-namnområden har lagts till:</span><span class="sxs-lookup"><span data-stu-id="e44fe-610">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="e44fe-611">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="e44fe-611">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="e44fe-612">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="e44fe-612">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="e44fe-613">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="e44fe-613">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="e44fe-614">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="e44fe-614">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="e44fe-615">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="e44fe-615">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="e44fe-616">En skrivskyddad egenskap, ”PendingReplicationOperationsCount” har lagts till för klassen PSServiceBusDRConfigurationAttributes som anger antalet väntande replikeringsåtgärder medan replikeringen pågår</span><span class="sxs-lookup"><span data-stu-id="e44fe-616">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="e44fe-617">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e44fe-617">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="e44fe-618">Uppdatera exempel för ”New-AzureRmServiceFabricCluster”</span><span class="sxs-lookup"><span data-stu-id="e44fe-618">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="e44fe-619">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="e44fe-619">AzureRM.Sql</span></span>
* <span data-ttu-id="e44fe-620">Nya cmdletar för Management.Sql som gör att kunderna kan lägga till certifikat för transparent datakryptering till SQL Server-instans eller en hanterad instans har lagts till</span><span class="sxs-lookup"><span data-stu-id="e44fe-620">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="e44fe-621">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="e44fe-621">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="e44fe-622">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="e44fe-622">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="e44fe-623">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="e44fe-623">AzureRM.Websites</span></span>
* <span data-ttu-id="e44fe-624">När `Set-AzureRmWebApp -AssignIdentity` och `Set-AzureRmWebAppSlot -AssignIdentity` är inställda på falskt tar de nu bort identitetsegenskapen från platsobjektet. Även förhandsgranskningstaggen tas bort.</span><span class="sxs-lookup"><span data-stu-id="e44fe-624">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="e44fe-625">`Get-AzureRmWebAppMetrics`, `Get-AzureRmAppServicePlanMetrics`-exempel har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="e44fe-625">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="e44fe-626">`Set-AzureRmWebApp -PhpVersion` har stöd för ”av” som en giltig php-version</span><span class="sxs-lookup"><span data-stu-id="e44fe-626">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="e44fe-627">6.4.0 – juli 2018</span><span class="sxs-lookup"><span data-stu-id="e44fe-627">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="e44fe-628">Allmänt</span><span class="sxs-lookup"><span data-stu-id="e44fe-628">General</span></span>
* <span data-ttu-id="e44fe-629">Formatering av OutputType i hjälpfiler har korrigerats för de flesta moduler</span><span class="sxs-lookup"><span data-stu-id="e44fe-629">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="e44fe-630">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="e44fe-630">AzureRM.Profile</span></span>
* <span data-ttu-id="e44fe-631">Ps1Xml-attribut har lagts till för grundläggande utdatatyper</span><span class="sxs-lookup"><span data-stu-id="e44fe-631">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="e44fe-632">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="e44fe-632">AzureRM.Compute</span></span>
* <span data-ttu-id="e44fe-633">IP-tagg-funktioner för VMSS</span><span class="sxs-lookup"><span data-stu-id="e44fe-633">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="e44fe-634">"New-AzureRmVmssIpTagConfig"-cmdlet har lagts till</span><span class="sxs-lookup"><span data-stu-id="e44fe-634">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="e44fe-635">IpTag-parameter har lagts till för New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="e44fe-635">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="e44fe-636">Automatisk återställningsfunktion för operativsystem för VMSS</span><span class="sxs-lookup"><span data-stu-id="e44fe-636">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="e44fe-637">DisableAutoRollback-parametrar har lagts till för New-AzureRmVmssConfig och Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e44fe-637">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="e44fe-638">Funktion för uppgraderingshistorik för operativsystem för Vmss</span><span class="sxs-lookup"><span data-stu-id="e44fe-638">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="e44fe-639">OSUpgradeHistory-växlingsparametern har lagts till för Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e44fe-639">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="e44fe-640">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="e44fe-640">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="e44fe-641">Lägg till stöd för katalog-ACL:er med hjälp av följande kommandon:</span><span class="sxs-lookup"><span data-stu-id="e44fe-641">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="e44fe-642">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="e44fe-642">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="e44fe-643">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="e44fe-643">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="e44fe-644">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="e44fe-644">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="e44fe-645">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e44fe-645">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="e44fe-646">Lägg till stöd för annullering och förloppsspårning för Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="e44fe-646">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="e44fe-647">Lägg till stöd för annullering för Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="e44fe-647">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="e44fe-648">Åtgärda tömning av felsökningsmeddelanden för cmdletar som gör rekursiva åtgärder</span><span class="sxs-lookup"><span data-stu-id="e44fe-648">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="e44fe-649">Åtgärda platsen för testning av DataLake-cmdletar</span><span class="sxs-lookup"><span data-stu-id="e44fe-649">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="e44fe-650">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="e44fe-650">AzureRM.EventHub</span></span>
* <span data-ttu-id="e44fe-651">Parametrar för optimalt maxantal har lagts till i liståtgärds-cmdletarna Get-AzureRmEventHub och Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="e44fe-651">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="e44fe-652">Ett problem i New-AzureRmEventHub-cmdleten har åtgärdats där minst en parameter behövdes när du skapade en ny EventHub.</span><span class="sxs-lookup"><span data-stu-id="e44fe-652">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="e44fe-653">Angiven standardparameter har ställts in.</span><span class="sxs-lookup"><span data-stu-id="e44fe-653">Provided Default Parameter set.</span></span>
* <span data-ttu-id="e44fe-654">Valfri parameter för KeyValue har lagts till för New-AzureRmEventHubKey-cmdleten, vilket gör det möjligt att ange KeyValue.</span><span class="sxs-lookup"><span data-stu-id="e44fe-654">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="e44fe-655">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e44fe-655">AzureRM.KeyVault</span></span>
* <span data-ttu-id="e44fe-656">Åtgärda problem där alla resurser returnerades av Get-AzureRmKeyVault-taggen</span><span class="sxs-lookup"><span data-stu-id="e44fe-656">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="e44fe-657">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="e44fe-657">AzureRM.Network</span></span>
* <span data-ttu-id="e44fe-658">Gör nya SKU:er tillgängliga för zonredundanta VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="e44fe-658">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="e44fe-659">Nya kommandon har lagts till för funktionen: ExpressRoute Partner APIs via ARM</span><span class="sxs-lookup"><span data-stu-id="e44fe-659">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="e44fe-660">Get-AzureRmExpressRouteCrossConnection har lagts till</span><span class="sxs-lookup"><span data-stu-id="e44fe-660">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="e44fe-661">Set-AzureRmExpressRouteCrossConnection har lagts till</span><span class="sxs-lookup"><span data-stu-id="e44fe-661">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="e44fe-662">Add-AzureRmExpressRouteCrossConnectionPeering har lagts till</span><span class="sxs-lookup"><span data-stu-id="e44fe-662">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="e44fe-663">Get-AzureRmExpressRouteCrossConnectionPeering har lagts till</span><span class="sxs-lookup"><span data-stu-id="e44fe-663">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="e44fe-664">Remove-AzureRmExpressRouteCrossConnectionPeering har lagts till</span><span class="sxs-lookup"><span data-stu-id="e44fe-664">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="e44fe-665">Get-AzureRMExpressRouteCrossConnectionArpTable har lagts till</span><span class="sxs-lookup"><span data-stu-id="e44fe-665">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="e44fe-666">Get-AzureRMExpressRouteCrossConnectionRouteTable har lagts till</span><span class="sxs-lookup"><span data-stu-id="e44fe-666">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="e44fe-667">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary har lagts till</span><span class="sxs-lookup"><span data-stu-id="e44fe-667">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="e44fe-668">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e44fe-668">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="e44fe-669">Get-AzureRmRecoveryServicesBackupStatus-cmdlet har lagts till.</span><span class="sxs-lookup"><span data-stu-id="e44fe-669">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="e44fe-670">Denna cmdlet tar ett ID för virtuell dator och kontrollerar om den virtuella datorn skyddas av ett valv i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="e44fe-670">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="e44fe-671">Om ett sådant valv finns returnerar cmdleten valvinformationen.</span><span class="sxs-lookup"><span data-stu-id="e44fe-671">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="e44fe-672">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="e44fe-672">AzureRM.Resources</span></span>
* <span data-ttu-id="e44fe-673">Uppdatera Get-AzureRmPolicyAssignment-cmdletar:</span><span class="sxs-lookup"><span data-stu-id="e44fe-673">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="e44fe-674">Lägg till stöd för att lista -Scope-värden på hanteringsgruppsnivå</span><span class="sxs-lookup"><span data-stu-id="e44fe-674">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="e44fe-675">Lägg till stöd för hämtning av enskilda tilldelningar med -Scope-värden på hanteringsgruppsnivå.</span><span class="sxs-lookup"><span data-stu-id="e44fe-675">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="e44fe-676">Lägg till växlar för -Effective och -All till kontrollparametrar</span><span class="sxs-lookup"><span data-stu-id="e44fe-676">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="e44fe-677">Uppdatera Get/New/Remove/Set-AzureRmPolicyDefinition-cmdletar</span><span class="sxs-lookup"><span data-stu-id="e44fe-677">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="e44fe-678">Lägg till parameter för -ManagementGroupName om du vill tillämpa åtgärder för en viss hanteringsgrupp</span><span class="sxs-lookup"><span data-stu-id="e44fe-678">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="e44fe-679">Lägg till parameter för -SubscriptionId om du vill tillämpa åtgärder för en viss prenumeration</span><span class="sxs-lookup"><span data-stu-id="e44fe-679">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="e44fe-680">Uppdatera Get/New/Remove/Set-AzureRmPolicySetDefinition-cmdletar</span><span class="sxs-lookup"><span data-stu-id="e44fe-680">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="e44fe-681">Lägg till parameter för -ManagementGroupName om du vill tillämpa åtgärder för en viss hanteringsgrupp</span><span class="sxs-lookup"><span data-stu-id="e44fe-681">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="e44fe-682">Lägg till parameter för -SubscriptionId om du vill tillämpa åtgärder för en viss prenumeration</span><span class="sxs-lookup"><span data-stu-id="e44fe-682">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="e44fe-683">Lägg till stöd för hemliga KeyVault-referenser i parametrar när du använder "TemplateParameterObject" i "New-AzureRmResourceGroupDeployment"</span><span class="sxs-lookup"><span data-stu-id="e44fe-683">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="e44fe-684">Åtgärda problem med att "-EndDate"-parametern ignorerades på grund av "New-AzureRmADAppCredential"</span><span class="sxs-lookup"><span data-stu-id="e44fe-684">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="e44fe-685">Åtgärda problem med att felaktig URL användes i "New-AzureRmADAppCredential" vid begäran</span><span class="sxs-lookup"><span data-stu-id="e44fe-685">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="e44fe-686">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e44fe-686">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="e44fe-687">Valfri parameter för -KeyValue har lagts till för New-AzureRmServiceBusKey-cmdleten, vilket gör det möjligt att ange KeyValue.</span><span class="sxs-lookup"><span data-stu-id="e44fe-687">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="e44fe-688">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="e44fe-688">AzureRM.Sql</span></span>
* <span data-ttu-id="e44fe-689">Användardefinierade återställningspunkter har klargjorts för SQLDW i New-AzureRmSqlDatabaseRestorePoint-hjälpen</span><span class="sxs-lookup"><span data-stu-id="e44fe-689">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="e44fe-690">Dokumentationen om parametern -ComputeGeneration har uppdaterats i fler cmdletar</span><span class="sxs-lookup"><span data-stu-id="e44fe-690">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="e44fe-691">6.3.0 – juni 2018</span><span class="sxs-lookup"><span data-stu-id="e44fe-691">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="e44fe-692">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="e44fe-692">AzureRM.Profile</span></span>
* <span data-ttu-id="e44fe-693">Uppdaterade felmeddelanden för Enable-AzureRmContextAutoSave</span><span class="sxs-lookup"><span data-stu-id="e44fe-693">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="e44fe-694">Skapa en kontext för varje prenumeration när du kör ”Connect-AzureRmAccount” utan tidigare kontext</span><span class="sxs-lookup"><span data-stu-id="e44fe-694">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="e44fe-695">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="e44fe-695">Azure.Storage</span></span>
* <span data-ttu-id="e44fe-696">Ytterligare information om parametern -Permissions har lagts till i hjälpfilerna.</span><span class="sxs-lookup"><span data-stu-id="e44fe-696">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="e44fe-697">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="e44fe-697">AzureRM.Compute</span></span>
* <span data-ttu-id="e44fe-698">”Get-AzureRmVmDiskEncryptionStatus” korrigerar ett problem för virtuella datorer utan datadiskar</span><span class="sxs-lookup"><span data-stu-id="e44fe-698">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="e44fe-699">Uppdatera version av klientbibliotek för Compute för att korrigera följande cmdletar</span><span class="sxs-lookup"><span data-stu-id="e44fe-699">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="e44fe-700">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="e44fe-700">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="e44fe-701">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="e44fe-701">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="e44fe-702">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="e44fe-702">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="e44fe-703">Följande cmdletar har åtgärdats för att visa ”Åtgärds-ID” och ”Åtgärdsstatus” på ett korrekt sätt:</span><span class="sxs-lookup"><span data-stu-id="e44fe-703">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="e44fe-704">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="e44fe-704">Start-AzureRmVM</span></span>
    - <span data-ttu-id="e44fe-705">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="e44fe-705">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="e44fe-706">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="e44fe-706">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="e44fe-707">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="e44fe-707">Set-AzureRmVM</span></span>
    - <span data-ttu-id="e44fe-708">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="e44fe-708">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="e44fe-709">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e44fe-709">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="e44fe-710">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="e44fe-710">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="e44fe-711">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="e44fe-711">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="e44fe-712">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e44fe-712">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="e44fe-713">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e44fe-713">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="e44fe-714">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e44fe-714">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="e44fe-715">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e44fe-715">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="e44fe-716">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="e44fe-716">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="e44fe-717">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="e44fe-717">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="e44fe-718">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="e44fe-718">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="e44fe-719">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="e44fe-719">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="e44fe-720">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="e44fe-720">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="e44fe-721">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="e44fe-721">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="e44fe-722">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="e44fe-722">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="e44fe-723">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="e44fe-723">AzureRM.EventGrid</span></span>
* <span data-ttu-id="e44fe-724">Ta bort verifieringsvillkoren ValidateNotNullOrEmpty för SubjectBeginsWith/SubjectEndsWith i cmdleten Update-AzureRmEventGridSubscription för att ändra de här parametrarna till en tom sträng om det behövs.</span><span class="sxs-lookup"><span data-stu-id="e44fe-724">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="e44fe-725">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e44fe-725">AzureRM.KeyVault</span></span>
* <span data-ttu-id="e44fe-726">Åtgärda problem där inga taggar returneras när Get-AzureRmKeyVault -Tag körs</span><span class="sxs-lookup"><span data-stu-id="e44fe-726">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="e44fe-727">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="e44fe-727">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="e44fe-728">Offentlig lansering av cmdletar för Policy Insights</span><span class="sxs-lookup"><span data-stu-id="e44fe-728">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="e44fe-729">Använd API-version 2018-04-04</span><span class="sxs-lookup"><span data-stu-id="e44fe-729">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="e44fe-730">Lägg till PolicyDefinitionReferenceId i resultaten för Get-AzureRmPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="e44fe-730">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="e44fe-731">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e44fe-731">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="e44fe-732">Parametern -Vault har lagts till i cmdletarna för RecoveryServices.Backup.</span><span class="sxs-lookup"><span data-stu-id="e44fe-732">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="e44fe-733">När den godkänns åsidosätts cmdleten Set-AzureRmRecoveryServicesContext.</span><span class="sxs-lookup"><span data-stu-id="e44fe-733">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="e44fe-734">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="e44fe-734">AzureRM.Sql</span></span>
* <span data-ttu-id="e44fe-735">Exemplet i hjälpfilen för Get-AzureRmSqlDatabaseExpanded har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="e44fe-735">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="e44fe-736">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="e44fe-736">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="e44fe-737">Hjälpfilen för Add-AzureRmTrafficManagerEndpointConfig har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="e44fe-737">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="e44fe-738">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="e44fe-738">AzureRM.Websites</span></span>
* <span data-ttu-id="e44fe-739">”Set-AzureRmWebApp” har uppdaterats så att den inte skriver över appinställningarna när du använder -AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="e44fe-739">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="e44fe-740">”New-AzureRMWebAppSlot” har uppdaterats för att visa att AppServicePlan är en valfri parameter</span><span class="sxs-lookup"><span data-stu-id="e44fe-740">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="e44fe-741">6.2.1 – juni 2018</span><span class="sxs-lookup"><span data-stu-id="e44fe-741">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="e44fe-742">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e44fe-742">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="e44fe-743">PSWorkspace-modellen har uppdaterats för att tillåta att nätverket använder typ som en parameter</span><span class="sxs-lookup"><span data-stu-id="e44fe-743">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="e44fe-744">6.2.0 – juni 2018</span><span class="sxs-lookup"><span data-stu-id="e44fe-744">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="e44fe-745">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="e44fe-745">AzureRM.Profile</span></span>
* <span data-ttu-id="e44fe-746">Åtgärda problemet med att version 10.0.3 av Newtonsoft.Json inte lästes in vid modulimporten</span><span class="sxs-lookup"><span data-stu-id="e44fe-746">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="e44fe-747">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="e44fe-747">AzureRM.Compute</span></span>
* <span data-ttu-id="e44fe-748">VMSS VM-uppdateringsfunktion</span><span class="sxs-lookup"><span data-stu-id="e44fe-748">VMSS VM Update feature</span></span>
    - <span data-ttu-id="e44fe-749">Cmdletarna Update-AzureRmVmssVM och New-AzureRmVMDataDisk har lagts till</span><span class="sxs-lookup"><span data-stu-id="e44fe-749">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="e44fe-750">Lägg till parametern VirtualMachineScaleSetVM till cmdleten Add-AzureRmVMDataDisk så att det går att lägga till en datadisk i den virtuella Vmss-datorn.</span><span class="sxs-lookup"><span data-stu-id="e44fe-750">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="e44fe-751">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="e44fe-751">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="e44fe-752">SDK:n för ADF .Net har uppdaterats till version 0.8.0-preview som innehåller följande ändringar:</span><span class="sxs-lookup"><span data-stu-id="e44fe-752">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="e44fe-753">Åtgärden för att konfigurera fabrikslagringsplatsen har lagts till</span><span class="sxs-lookup"><span data-stu-id="e44fe-753">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="e44fe-754">QuickBooks LinkedService har uppdaterats för att visa egenskaperna consumerKey och consumerSecret</span><span class="sxs-lookup"><span data-stu-id="e44fe-754">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="e44fe-755">Flera modelltyper från SecretBase till Object har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="e44fe-755">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="e44fe-756">Utlösaren Blob Events har lagts till</span><span class="sxs-lookup"><span data-stu-id="e44fe-756">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="e44fe-757">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e44fe-757">AzureRM.KeyVault</span></span>
* <span data-ttu-id="e44fe-758">Uppdatera dokumentation med exempel på utdata</span><span class="sxs-lookup"><span data-stu-id="e44fe-758">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="e44fe-759">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="e44fe-759">AzureRM.Network</span></span>
* <span data-ttu-id="e44fe-760">Aktivera Trafikanalys-parametrar på Network Watcher-cmdletar</span><span class="sxs-lookup"><span data-stu-id="e44fe-760">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="e44fe-761">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="e44fe-761">AzureRM.Resources</span></span>
* <span data-ttu-id="e44fe-762">Åtgärda problemet med egenskapen "Properties" för objekt(en) "PSResource" som returneras från "Get-AzureRmResource"</span><span class="sxs-lookup"><span data-stu-id="e44fe-762">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="e44fe-763">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="e44fe-763">AzureRM.Scheduler</span></span>
* <span data-ttu-id="e44fe-764">Åtgärda problemet med att nya autentiseringsvärden inte anges vid uppdatering av ServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="e44fe-764">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="e44fe-765">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="e44fe-765">AzureRM.Sql</span></span>
* <span data-ttu-id="e44fe-766">Följande cmdletar har uppdaterats med valfri LicenseType-parameter</span><span class="sxs-lookup"><span data-stu-id="e44fe-766">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="e44fe-767">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e44fe-767">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="e44fe-768">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="e44fe-768">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="e44fe-769">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="e44fe-769">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="e44fe-770">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="e44fe-770">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="e44fe-771">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e44fe-771">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="e44fe-772">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="e44fe-772">AzureRM.Websites</span></span>
* <span data-ttu-id="e44fe-773">New-AzureRMWebApp har uppdaterats för att använda vanliga algoritmer från biblioteket Strategy.</span><span class="sxs-lookup"><span data-stu-id="e44fe-773">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="e44fe-774">6.1.0 – maj 2018</span><span class="sxs-lookup"><span data-stu-id="e44fe-774">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="e44fe-775">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="e44fe-775">AzureRM.Profile</span></span>
* <span data-ttu-id="e44fe-776">Åtgärda problem där en körning av Clear-AzureRmContext skulle bevara en tom kontext med namnet på den föregående standardkontexten som gjorde att användaren inte kunde skapa en ny kontext med det gamla namnet</span><span class="sxs-lookup"><span data-stu-id="e44fe-776">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="e44fe-777">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="e44fe-777">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="e44fe-778">Aktivera Gateway associerings- och avassocieringsåtgärder på AS.</span><span class="sxs-lookup"><span data-stu-id="e44fe-778">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="e44fe-779">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e44fe-779">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="e44fe-780">Stöd för ApiVersions, ApiReleases och ApiRevisions har lagts till</span><span class="sxs-lookup"><span data-stu-id="e44fe-780">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="e44fe-781">Stöd för serverdelen på ServiceFabric har lagts till</span><span class="sxs-lookup"><span data-stu-id="e44fe-781">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="e44fe-782">Stöd för Application Insights-loggare har lagts till</span><span class="sxs-lookup"><span data-stu-id="e44fe-782">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="e44fe-783">Stöd för att identifiera SKU:n ”Basic” som en giltig SKU för Api Management-tjänsten har lagts till</span><span class="sxs-lookup"><span data-stu-id="e44fe-783">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="e44fe-784">Stöd för att installera certifikat som utfärdats av privata certifikatutfärdare som rot eller certifikatutfärdare har lagts till</span><span class="sxs-lookup"><span data-stu-id="e44fe-784">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="e44fe-785">Stöd för att godkänna anpassade SSL-certifikat via KeyVault och flera proxy-värdnamn har lagts till</span><span class="sxs-lookup"><span data-stu-id="e44fe-785">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="e44fe-786">Stöd för MSI-identitet har lagts till</span><span class="sxs-lookup"><span data-stu-id="e44fe-786">Added support for MSI identity</span></span>
* <span data-ttu-id="e44fe-787">Stöd för att godkänna principer via URL har lagts till. Obs! Följande cmdletar blir inaktuella i framtida versioner</span><span class="sxs-lookup"><span data-stu-id="e44fe-787">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="e44fe-788">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="e44fe-788">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="e44fe-789">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="e44fe-789">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="e44fe-790">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="e44fe-790">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="e44fe-791">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="e44fe-791">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="e44fe-792">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="e44fe-792">AzureRM.Batch</span></span>
* <span data-ttu-id="e44fe-793">Släpp nya cmdleten Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="e44fe-793">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="e44fe-794">Släpp nya cmdleten Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="e44fe-794">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="e44fe-795">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="e44fe-795">AzureRM.Consumption</span></span>
* <span data-ttu-id="e44fe-796">Lägg till nya parametrar Expand, ResourceGroup, InstanceName, InstanceId, Tags och Top på cmdleten Get-AzureRmConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="e44fe-796">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="e44fe-797">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e44fe-797">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="e44fe-798">Åtgärda exempel för Export AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="e44fe-798">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="e44fe-799">Åtgärda undantag för null-parameter för rekursivt ärende i Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="e44fe-799">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="e44fe-800">Åtgärda hjälpfilerna för Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="e44fe-800">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="e44fe-801">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="e44fe-801">AzureRM.Network</span></span>
* <span data-ttu-id="e44fe-802">Öka nätverkets SDK-version från förhandsversionen 18.0.0 till förhandsversionen 19.0.0</span><span class="sxs-lookup"><span data-stu-id="e44fe-802">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="e44fe-803">Cmdlet har lagts till för att skapa protokollinformation</span><span class="sxs-lookup"><span data-stu-id="e44fe-803">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="e44fe-804">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="e44fe-804">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="e44fe-805">Cmdlet har lagts till för att lägga till en ny kretsanslutning till en befintlig expressroute-krets.</span><span class="sxs-lookup"><span data-stu-id="e44fe-805">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="e44fe-806">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="e44fe-806">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="e44fe-807">Cmdlet har lagts till för att ta bort en kretsanslutning från en befintlig expressroute-krets.</span><span class="sxs-lookup"><span data-stu-id="e44fe-807">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="e44fe-808">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="e44fe-808">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="e44fe-809">Cmdlet har lagts till för att hämta en kretsanslutning</span><span class="sxs-lookup"><span data-stu-id="e44fe-809">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="e44fe-810">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="e44fe-810">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="e44fe-811">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e44fe-811">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="e44fe-812">Användning med serverautentisering med genererade certifikat (problem #5998) har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="e44fe-812">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="e44fe-813">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="e44fe-813">AzureRM.Sql</span></span>
* <span data-ttu-id="e44fe-814">Cmdletar för granskning för att ta bort AuditActions eller AuditActionGroups har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="e44fe-814">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="e44fe-815">Åtgärdade problem med Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy vid konfigurering av en ny flexibel bevarandeprincip där kommandot misslyckas med ett meddelande om att konfigurering av långsiktig bevarandeprincip med Azure Recovery Service-valv och principen inte längre stöds,</span><span class="sxs-lookup"><span data-stu-id="e44fe-815">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="e44fe-816">och att en begäran med den nya flexibla bevarandeprincipen ska skickas.</span><span class="sxs-lookup"><span data-stu-id="e44fe-816">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="e44fe-817">Uppdatera alla Azure Sql Database/ElasticPool Creation/Update-relaterade cmdletar för att använda det nya databas-API:et som stöder SKU-egenskaper för skalnings- och nivårelaterade egenskaper.</span><span class="sxs-lookup"><span data-stu-id="e44fe-817">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="e44fe-818">Cmdletar har uppdaterats, inklusive:</span><span class="sxs-lookup"><span data-stu-id="e44fe-818">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="e44fe-819">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e44fe-819">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="e44fe-820">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="e44fe-820">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="e44fe-821">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="e44fe-821">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="e44fe-822">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="e44fe-822">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="e44fe-823">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e44fe-823">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="e44fe-824">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="e44fe-824">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="e44fe-825">Uppdatera parametrarna för Get-AzureRmTrafficManagerProfile så att ResourceGroupName-parametern blir obligatorisk när du använder Name-parametern.</span><span class="sxs-lookup"><span data-stu-id="e44fe-825">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
