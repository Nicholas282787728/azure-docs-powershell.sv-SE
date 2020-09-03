---
title: Ändringslogg för Azure PowerShell | Microsoft Docs
description: Det här är en historik över de ändringar som gjorts i den senaste versionen av Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 08/28/2018
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 189b360f8825b7de93b67b0b2cbe670d00187327
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/01/2020
ms.locfileid: "89241363"
---
# <a name="release-notes"></a><span data-ttu-id="eeb17-103">Viktig information</span><span class="sxs-lookup"><span data-stu-id="eeb17-103">Release notes</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

<span data-ttu-id="eeb17-104">Det här är en lista över ändringar som har gjorts i Azure PowerShell i den här versionen.</span><span class="sxs-lookup"><span data-stu-id="eeb17-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="6130---november-2018"></a><span data-ttu-id="eeb17-105">6.13.0 – november 2018</span><span class="sxs-lookup"><span data-stu-id="eeb17-105">6.13.0 - November 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="eeb17-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="eeb17-106">AzureRM.Profile</span></span>
* <span data-ttu-id="eeb17-107">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="eeb17-107">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="eeb17-108">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="eeb17-108">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="eeb17-109">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="eeb17-109">Update dependencies for type mapping issue</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="eeb17-110">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="eeb17-110">AzureRM.Automation</span></span>
* <span data-ttu-id="eeb17-111">Swagger baserade Azure Automation-cmdletar</span><span class="sxs-lookup"><span data-stu-id="eeb17-111">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="eeb17-112">Cmdletar för Uppdateringshantering har lagts till</span><span class="sxs-lookup"><span data-stu-id="eeb17-112">Added Update Management cmdlets</span></span>
* <span data-ttu-id="eeb17-113">Cmdletar för källkontroll har lagts till</span><span class="sxs-lookup"><span data-stu-id="eeb17-113">Added Source Control cmdlets</span></span>
* <span data-ttu-id="eeb17-114">Remove-AzureRmAutomationHybridWorkerGroup-cmdlet har lagts till</span><span class="sxs-lookup"><span data-stu-id="eeb17-114">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="eeb17-115">Kommandot för DSC-registreringsnod har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="eeb17-115">Fixed the DSC Register Node command</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="eeb17-116">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="eeb17-116">AzureRM.Compute</span></span>
* <span data-ttu-id="eeb17-117">Problem med SystemAssigned-identitet har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="eeb17-117">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="eeb17-118">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="eeb17-118">Update dependencies for type mapping issue</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="eeb17-119">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="eeb17-119">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="eeb17-120">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="eeb17-120">Update dependencies for type mapping issue</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="eeb17-121">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="eeb17-121">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="eeb17-122">uppdatera exempelbeskrivningen för marketplace-cmdletar</span><span class="sxs-lookup"><span data-stu-id="eeb17-122">update the examples description for marketplace cmdlets</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="eeb17-123">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="eeb17-123">AzureRM.Network</span></span>
* <span data-ttu-id="eeb17-124">Cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomErreller Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="eeb17-124">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="eeb17-125">ICMP tillbaka till stöd för Azure Firewall-nätverksprotokoll har lagts till</span><span class="sxs-lookup"><span data-stu-id="eeb17-125">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="eeb17-126">Uppdatera cmdlet Test-AzureRmNetworkWatcherConnectivity, lägga till verifiering av mål-id, adress och port.</span><span class="sxs-lookup"><span data-stu-id="eeb17-126">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="eeb17-127">Åtgärda problem med minnesanvändning i VirtualNetwork-karta</span><span class="sxs-lookup"><span data-stu-id="eeb17-127">Fix issues with memory usage in VirtualNetwork map</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="eeb17-128">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="eeb17-128">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="eeb17-129">Åtgärda för att ändra principen för en skyddad fildelning.</span><span class="sxs-lookup"><span data-stu-id="eeb17-129">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="eeb17-130">Tidszonsprincipen har konverterats till versaler.</span><span class="sxs-lookup"><span data-stu-id="eeb17-130">Converted policy timezone to uppercase.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="eeb17-131">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="eeb17-131">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="eeb17-132">Exempel i New-AzureRmRecoveryServicesAsrProtectableItem har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="eeb17-132">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="eeb17-133">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="eeb17-133">Update dependencies for type mapping issue</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="eeb17-134">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="eeb17-134">AzureRM.Relay</span></span>
* <span data-ttu-id="eeb17-135">Valfri parameter -KeyValue till New-AzureRmRelayKey cmdlet har lagts till, vilket gör det möjligt för användare att tillhandahålla KeyValue.</span><span class="sxs-lookup"><span data-stu-id="eeb17-135">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="eeb17-136">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="eeb17-136">AzureRM.Resources</span></span>
* <span data-ttu-id="eeb17-137">Uppdatera hjälpdokumentation för resursidentitet kopplad till parametrar i `New-AzureRmPolicyAssignment` och `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="eeb17-137">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="eeb17-138">Lägg till ett exempel för New-AzureRmPolicyDefinition som använder -Metadata</span><span class="sxs-lookup"><span data-stu-id="eeb17-138">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="eeb17-139">Korrigera så att skiftläge behålls i taggnycklar i NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="eeb17-139">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="eeb17-140">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="eeb17-140">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="eeb17-141">Lägg till utfasningsmeddelanden för kommande icke-kompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="eeb17-141">Add deprecation messages for upcoming breaking changes</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="eeb17-142">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="eeb17-142">AzureRM.Sql</span></span>
* <span data-ttu-id="eeb17-143">Nya cmdletar för CRUD-åtgärder på Azure Sql Database-hanterad instans och Azure Sql-hanterad databas</span><span class="sxs-lookup"><span data-stu-id="eeb17-143">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="eeb17-144">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="eeb17-144">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="eeb17-145">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="eeb17-145">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="eeb17-146">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="eeb17-146">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="eeb17-147">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="eeb17-147">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="eeb17-148">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="eeb17-148">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="eeb17-149">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="eeb17-149">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="eeb17-150">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="eeb17-150">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="eeb17-151">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="eeb17-151">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="eeb17-152">Hantering av utökad granskningsprincip på en server eller en databas har aktiverats.</span><span class="sxs-lookup"><span data-stu-id="eeb17-152">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="eeb17-153">Ny parameter (PredicateExpression) har lagts till för att aktivera filtrering av granskningsloggar.</span><span class="sxs-lookup"><span data-stu-id="eeb17-153">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="eeb17-154">Cmdletar har ändrats så att de använder SQL-klienter i stället för äldre klienter.</span><span class="sxs-lookup"><span data-stu-id="eeb17-154">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="eeb17-155">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="eeb17-155">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="eeb17-156">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="eeb17-156">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="eeb17-157">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="eeb17-157">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="eeb17-158">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="eeb17-158">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="eeb17-159">Problem med att använda Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings med lagringskontots namnparameter har korrigerats</span><span class="sxs-lookup"><span data-stu-id="eeb17-159">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="6120---november-2018"></a><span data-ttu-id="eeb17-160">6.12.0 – november 2018</span><span class="sxs-lookup"><span data-stu-id="eeb17-160">6.12.0 - November 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="eeb17-161">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="eeb17-161">AzureRM.Profile</span></span>
* <span data-ttu-id="eeb17-162">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="eeb17-162">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="eeb17-163">Byt namn på parametern TenantId i cmdleten Connect-AzureRmAccount till Tenant och lägg till ett alias för TenantId</span><span class="sxs-lookup"><span data-stu-id="eeb17-163">Rename param TenantId in cmdlet Connect-AzureRmAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="eeb17-164">Uppdatera TenantId-beskrivning för Connect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="eeb17-164">Updated TenantId description for Connect-AzureRmAccount</span></span>
* <span data-ttu-id="eeb17-165">Åtgärda felmeddelande för misslyckad inloggning när du tillhandahåller klientdomän</span><span class="sxs-lookup"><span data-stu-id="eeb17-165">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="eeb17-166">Åtgärda problem med att kontextnamn hamnar i konflikt för konton utan prenumerationer i klientorganisationen</span><span class="sxs-lookup"><span data-stu-id="eeb17-166">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="eeb17-167">Åtgärda problem med DataLake-slutpunkter vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="eeb17-167">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="eeb17-168">Åtgärda problem med att Disconnect-AzureRmAccount kastades om den inte anslöts</span><span class="sxs-lookup"><span data-stu-id="eeb17-168">Fix issue where 'Disconnect-AzureRmAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azurermautomation"></a><span data-ttu-id="eeb17-169">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="eeb17-169">AzureRM.Automation</span></span>
* <span data-ttu-id="eeb17-170">Bytte namn på cmdlet DLL-filnamnet till Microsoft.Azure.Commands.Automation.dll</span><span class="sxs-lookup"><span data-stu-id="eeb17-170">Renamed cmdlet DLL filename to Microsoft.Azure.Commands.Automation.dll</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="eeb17-171">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="eeb17-171">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="eeb17-172">Lägg till åtgärden Get-AzureRmCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="eeb17-172">Add Get-AzureRmCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="eeb17-173">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="eeb17-173">AzureRM.Compute</span></span>
* <span data-ttu-id="eeb17-174">Lägg till cmdletarna Add-AzureRmVmssVMDataDisk och Remove-AzureRmVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="eeb17-174">Add Add-AzureRmVmssVMDataDisk and Remove-AzureRmVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="eeb17-175">Get-AzureRmVMImage visar AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="eeb17-175">Get-AzureRmVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="eeb17-176">Åtgärdade att alternativvärden för SetAzureRmVMChefExtension -BootstrapOptions och -JsonAttribute inte ställdes in som json-format.</span><span class="sxs-lookup"><span data-stu-id="eeb17-176">Fixed SetAzureRmVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="eeb17-177">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="eeb17-177">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="eeb17-178">Uppdatera DataLake-paketet till 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="eeb17-178">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="eeb17-179">Lägg till standardsamtidighet för flertrådade åtgärder.</span><span class="sxs-lookup"><span data-stu-id="eeb17-179">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="eeb17-180">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="eeb17-180">AzureRM.Insights</span></span>
* <span data-ttu-id="eeb17-181">Åtgärdade problem #7267 (autoskalningsområde)</span><span class="sxs-lookup"><span data-stu-id="eeb17-181">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="eeb17-182">Problem med att uppräknade parametrar inte ställdes in ordentligt när du skapade en ny autoskalningsregel (de ställdes alltid in med standardvärdet).</span><span class="sxs-lookup"><span data-stu-id="eeb17-182">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="eeb17-183">Åtgärdade problem #7513 [Insights] Set-AzureRMDiagnosticSetting kräver uttrycklig specifikation av kategorier när inställningar skapas</span><span class="sxs-lookup"><span data-stu-id="eeb17-183">Fixed issue #7513 [Insights] Set-AzureRMDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="eeb17-184">Nu kräver inte cmdleten uttrycklig anvisning av kategorierna för att aktiveras under skapande, d.v.s. den fungerar enligt beskrivning</span><span class="sxs-lookup"><span data-stu-id="eeb17-184">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="eeb17-185">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="eeb17-185">AzureRM.Network</span></span>
* <span data-ttu-id="eeb17-186">PeeringType ändrades till en obligatorisk parameter för följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="eeb17-186">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="eeb17-187">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="eeb17-187">Get-AzureRmExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="eeb17-188">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="eeb17-188">Get-AzureRmExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="eeb17-189">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="eeb17-189">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="eeb17-190">Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="eeb17-190">Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="eeb17-191">Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="eeb17-191">Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="eeb17-192">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="eeb17-192">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="eeb17-193">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="eeb17-193">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="eeb17-194">Cmdletar för principreparation har lagts till</span><span class="sxs-lookup"><span data-stu-id="eeb17-194">Added policy remediation cmdlets</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="eeb17-195">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="eeb17-195">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="eeb17-196">Stöd har lagts till för Azure-filresurser i återställningstjänster.</span><span class="sxs-lookup"><span data-stu-id="eeb17-196">Added support for azure file shares in recovery services.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="eeb17-197">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="eeb17-197">AzureRM.Resources</span></span>
* <span data-ttu-id="eeb17-198">Korrigering för https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="eeb17-198">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="eeb17-199">Tillåt att resurser listas med parametern -ResourceId för Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="eeb17-199">Allow listing resources using the '-ResourceId' parameter for 'Get-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="eeb17-200">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="eeb17-200">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="eeb17-201">Skrivskyddad MigrationState-egenskap har lagts till i PSServiceBusMigrationConfigurationAttributes, som hjälper till att hålla koll på migreringstillståndet.</span><span class="sxs-lookup"><span data-stu-id="eeb17-201">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="eeb17-202">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="eeb17-202">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="eeb17-203">Åtgärda att lägga till certifikat till Linux-Vmss.</span><span class="sxs-lookup"><span data-stu-id="eeb17-203">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="eeb17-204">Åtgärda Add-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="eeb17-204">Fix 'Add-AzureRmServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="eeb17-205">Använd rätt tumavtryck från nya certifikat (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="eeb17-205">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="eeb17-206">Visa undantag korrekt (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="eeb17-206">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="eeb17-207">Åtgärda Update-AzureRmServiceFabricDurability så att klusterkonfigurationen uppdateras innan Vmss-åtgärden CreateOrUpdate påbörjas.</span><span class="sxs-lookup"><span data-stu-id="eeb17-207">Fix 'Update-AzureRmServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="6110---october-2018"></a><span data-ttu-id="eeb17-208">6.11.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="eeb17-208">6.11.0 - October 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="eeb17-209">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="eeb17-209">AzureRM.Profile</span></span>
* <span data-ttu-id="eeb17-210">Åtgärda problemet med Get-AzureRmSubscription i CloudShell</span><span class="sxs-lookup"><span data-stu-id="eeb17-210">Fix issue with Get-AzureRmSubscription in CloudShell</span></span>
* <span data-ttu-id="eeb17-211">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="eeb17-211">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="eeb17-212">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="eeb17-212">AzureRM.Backup</span></span>
* <span data-ttu-id="eeb17-213">Inaktuella Azure Backup-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="eeb17-213">Deprecated Azure Backup cmdlets.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="eeb17-214">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="eeb17-214">AzureRM.Compute</span></span>
* <span data-ttu-id="eeb17-215">Nya storlekar har lagts till i listan över godkända VM-storlekar för vilka accelererat nätverk kommer att aktiveras vid användning av den enkla parameteruppsättningen för ”New-AzureRmVm”</span><span class="sxs-lookup"><span data-stu-id="eeb17-215">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzureRmVm'</span></span>
* <span data-ttu-id="eeb17-216">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="eeb17-216">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="eeb17-217">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="eeb17-217">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="eeb17-218">Lägger till stöd för regler för virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="eeb17-218">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="eeb17-219">Get-AzureRmDataLakeStoreVirtualNetworkRule: Hämtar eller listar regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="eeb17-219">Get-AzureRmDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="eeb17-220">Add-AzureRmDataLakeStoreVirtualNetworkRule: Lägger till en regel för virtuellt nätverk i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="eeb17-220">Add-AzureRmDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="eeb17-221">Set-AzureRmDataLakeStoreVirtualNetworkRule: Ändrar den angivna regeln för virtuellt nätverk i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="eeb17-221">Set-AzureRmDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="eeb17-222">Remove-AzureRmDataLakeStoreVirtualNetworkRule: Tar bort en regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="eeb17-222">Remove-AzureRmDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="eeb17-223">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="eeb17-223">AzureRM.Network</span></span>
* <span data-ttu-id="eeb17-224">Skicka protokollvärdet till serverdelen för att uppdatera cmdleten Test-AzureRmNetworkWatcherConnectivity.</span><span class="sxs-lookup"><span data-stu-id="eeb17-224">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="eeb17-225">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="eeb17-225">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="eeb17-226">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="eeb17-226">AzureRM.Resources</span></span>
* <span data-ttu-id="eeb17-227">Åtgärda problem där Get-AzureRMRoleDefinition genererar ett oläsligt undantag (när standardprofilen inte innehåller någon prenumeration och ingen omfattning har angetts) genom att lägga till ett beskrivande undantag i scenariot.</span><span class="sxs-lookup"><span data-stu-id="eeb17-227">Fix isssue where Get-AzureRMRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="eeb17-228">Ställ in ”RoleDefinitionNameParameterSet” som standardparameteruppsättning.</span><span class="sxs-lookup"><span data-stu-id="eeb17-228">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="6100---october-2018"></a><span data-ttu-id="eeb17-229">6.10.0 – Oktober 2018</span><span class="sxs-lookup"><span data-stu-id="eeb17-229">6.10.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="eeb17-230">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="eeb17-230">Azure.Storage</span></span>
* <span data-ttu-id="eeb17-231">Åtgärda fel där Kopiera blob/fil inte kopierar metadata när målplatsen har ett problem med metadata</span><span class="sxs-lookup"><span data-stu-id="eeb17-231">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="eeb17-232">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="eeb17-232">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="eeb17-233">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="eeb17-233">Start-AzureStorageFileCopy</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="eeb17-234">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="eeb17-234">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="eeb17-235">Stöd för Get-AzureRmCognitiveServicesAccountSkus utan ett befintligt konto.</span><span class="sxs-lookup"><span data-stu-id="eeb17-235">Support Get-AzureRmCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="eeb17-236">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="eeb17-236">AzureRM.Compute</span></span>
* <span data-ttu-id="eeb17-237">Åtgärda fel där Get-AzureRmVM -ResourceGroupName <rg> returnerar fler än 50 resultat om det behövs</span><span class="sxs-lookup"><span data-stu-id="eeb17-237">Fix Get-AzureRmVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="eeb17-238">Ett exempel för ”SimpleParameterSet” har lagts till i hjälpen för cmdleten New-AzureRmVmss.</span><span class="sxs-lookup"><span data-stu-id="eeb17-238">Added an example of the 'SimpleParameterSet' to New-AzureRmVmss cmdlet help.</span></span>
* <span data-ttu-id="eeb17-239">Ett stavfel i förloppsmeddelandet för Azure Disk Encryption har korrigerats</span><span class="sxs-lookup"><span data-stu-id="eeb17-239">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="eeb17-240">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="eeb17-240">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="eeb17-241">ADF .Net SDK-versionen har uppdaterats till 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="eeb17-241">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="eeb17-242">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="eeb17-242">AzureRM.Network</span></span>
* <span data-ttu-id="eeb17-243">Funktionalitet för NetworkProfile har lagts till.</span><span class="sxs-lookup"><span data-stu-id="eeb17-243">Added NetworkProfile functionality.</span></span> <span data-ttu-id="eeb17-244">nya cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="eeb17-244">new cmdlets added</span></span>
    - <span data-ttu-id="eeb17-245">Get-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="eeb17-245">Get-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="eeb17-246">New-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="eeb17-246">New-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="eeb17-247">Remove-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="eeb17-247">Remove-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="eeb17-248">Set-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="eeb17-248">Set-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="eeb17-249">New-AzureRMContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="eeb17-249">New-AzureRMContainerNicConfig</span></span>
    - <span data-ttu-id="eeb17-250">New-AzureRmContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="eeb17-250">New-AzureRmContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="eeb17-251">Länk för tjänstassociering på modell för undernät har lagts till</span><span class="sxs-lookup"><span data-stu-id="eeb17-251">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="eeb17-252">De nya cmdletarna New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap och Remove-AzureRmVirtualNetworkTap har lagts till</span><span class="sxs-lookup"><span data-stu-id="eeb17-252">Added cmdlet New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap, Remove-AzureRmVirtualNetworkTap</span></span>
* <span data-ttu-id="eeb17-253">Cmdletarna Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig och Remove-AzureRmNEtworkInterfaceTapConfig har lagts till</span><span class="sxs-lookup"><span data-stu-id="eeb17-253">Added cmdlet Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig, Remove-AzureRmNEtworkInterfaceTapConfig</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="eeb17-254">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="eeb17-254">AzureRM.RedisCache</span></span>
* <span data-ttu-id="eeb17-255">Tillåt att alla strängar används som storleksparametrar framöver.</span><span class="sxs-lookup"><span data-stu-id="eeb17-255">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="eeb17-256">Lägg till P5 i popup-fönstret PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="eeb17-256">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="eeb17-257">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="eeb17-257">AzureRM.Resources</span></span>
* <span data-ttu-id="eeb17-258">Parametern -Mode som saknades i Set-AzureRmPolicyDefinition har lagts till</span><span class="sxs-lookup"><span data-stu-id="eeb17-258">Add missing -Mode parameter to Set-AzureRmPolicyDefinition</span></span>
* <span data-ttu-id="eeb17-259">Åtgärda buggen för cmdleten Get-AzureRmProviderOperation för åtgärder med ursprung som innehåller användare</span><span class="sxs-lookup"><span data-stu-id="eeb17-259">Fix Get-AzureRmProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="eeb17-260">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="eeb17-260">AzureRM.Sql</span></span>
* <span data-ttu-id="eeb17-261">Ett problem där vissa cmdletar för säkerhetskopiering inte kunde identifiera den aktuella azure-prenumerationen har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="eeb17-261">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="eeb17-262">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="eeb17-262">AzureRM.Storage</span></span>
* <span data-ttu-id="eeb17-263">Stöd för att hämta användningsinformation om en Storage-resurs för en specifik plats och för att lägga till ett varningsmeddelande för att hämta användningsinformation om en global Storage-resurs är inaktuellt.</span><span class="sxs-lookup"><span data-stu-id="eeb17-263">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="eeb17-264">Get-AzureRmStorageUsage</span><span class="sxs-lookup"><span data-stu-id="eeb17-264">Get-AzureRmStorageUsage</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="eeb17-265">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="eeb17-265">AzureRM.Websites</span></span>
* <span data-ttu-id="eeb17-266">Ny cmdlet: Get-AzureRMWebAppContainerContinuousDeploymentUrl – Hämtar webhook-URL:en för kontinuerlig distribution av container</span><span class="sxs-lookup"><span data-stu-id="eeb17-266">New Cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="eeb17-267">Nya cmdletar: New-AzureRMWebAppContainerPSSession och Enter-WebAppContainerPSSession – Startar en PowerShell-fjärrsession i en containerapp för windows</span><span class="sxs-lookup"><span data-stu-id="eeb17-267">New Cmdlets New-AzureRMWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="690---september-2018"></a><span data-ttu-id="eeb17-268">6.9.0 – September 2018</span><span class="sxs-lookup"><span data-stu-id="eeb17-268">6.9.0 - September 2018</span></span>
#### <a name="general"></a><span data-ttu-id="eeb17-269">Allmänt</span><span class="sxs-lookup"><span data-stu-id="eeb17-269">General</span></span>
* <span data-ttu-id="eeb17-270">AzureRM.SignalR har lagts till i samlingsmodulen för AzureRM</span><span class="sxs-lookup"><span data-stu-id="eeb17-270">AzureRM.SignalR was added to the AzureRM rollup module</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="eeb17-271">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="eeb17-271">AzureRM.Profile</span></span>
* <span data-ttu-id="eeb17-272">Mindre ändringar i den gemensamma koden för lagring</span><span class="sxs-lookup"><span data-stu-id="eeb17-272">Minor changes to the storage common code</span></span>
* <span data-ttu-id="eeb17-273">Hjälpfiler har uppdaterats för att innehålla fullständiga parametertyper.</span><span class="sxs-lookup"><span data-stu-id="eeb17-273">Updated help files to include full parameter types.</span></span>
* <span data-ttu-id="eeb17-274">-ServicePrincipal har ändrats så att den inte längre är obligatorisk i parameteruppsättningen ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="eeb17-274">Changed -ServicePrincipal to non-mandatory in the ServicePrincipalCertificateWithSubscriptionId parameter set</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="eeb17-275">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="eeb17-275">Azure.Storage</span></span>
* <span data-ttu-id="eeb17-276">Stöd för att skapa lagringskontext med OAuth.</span><span class="sxs-lookup"><span data-stu-id="eeb17-276">Support create Storage Context with OAuth.</span></span>
    - <span data-ttu-id="eeb17-277">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="eeb17-277">New-AzureStorageContext</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="eeb17-278">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="eeb17-278">AzureRM.Cdn</span></span>
* <span data-ttu-id="eeb17-279">Standard_Microsoft har lagts till i SKU:n för CDN-prissättning.</span><span class="sxs-lookup"><span data-stu-id="eeb17-279">Added Standard_Microsoft in Cdn pricing sku.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="eeb17-280">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="eeb17-280">AzureRM.Compute</span></span>
* <span data-ttu-id="eeb17-281">Flytta beroenden i nyckelvalv och minne till de gemensamma beroendena</span><span class="sxs-lookup"><span data-stu-id="eeb17-281">Move dependencies on Keyvault and Storage to the common dependencies</span></span>
* <span data-ttu-id="eeb17-282">Lägg till stöd för flera storlekar av virtuella datorer i AEM-cmdletar</span><span class="sxs-lookup"><span data-stu-id="eeb17-282">Add support for more virutal machine sizes to AEM cmdlets</span></span>
* <span data-ttu-id="eeb17-283">Lägg till parametern PublicIPPrefix i New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="eeb17-283">Add PublicIPPrefix parameter to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="eeb17-284">Lägg till parametern ResourceId till cmdleten Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="eeb17-284">Add ResourceId parameter to Invoke-AzureRmVMRunCommand cmdelt</span></span>
* <span data-ttu-id="eeb17-285">Lägg till cmdleten Invoke-AzureRmVmssVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="eeb17-285">Add Invoke-AzureRmVmssVMRunCommand cmdlet</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="eeb17-286">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="eeb17-286">AzureRM.Dns</span></span>
* <span data-ttu-id="eeb17-287">Stöd har lagts till för aliasposter när DNS-poster skapas</span><span class="sxs-lookup"><span data-stu-id="eeb17-287">Added support for alias record during dns record creation</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="eeb17-288">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="eeb17-288">AzureRM.Insights</span></span>
* <span data-ttu-id="eeb17-289">Problem #6833 och #7102 (området Diagnostikinställningar) har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="eeb17-289">Fixed issues #6833 and #7102 (Diagnostic Settings area)</span></span>
    - <span data-ttu-id="eeb17-290">Problem med standardnamnet, d.v.s. ”tjänsten” när diagnostikinställningar skapas och listas/hämtas</span><span class="sxs-lookup"><span data-stu-id="eeb17-290">Issues with the default name, i.e. 'service', during creation and listing/getting of diagnostic settings</span></span>
    - <span data-ttu-id="eeb17-291">Problem med att skapa diagnostikinställningar med kategorier</span><span class="sxs-lookup"><span data-stu-id="eeb17-291">Issues creating diagnostic settings with categories</span></span>
* <span data-ttu-id="eeb17-292">Utfasningsmeddelande har lagts till för tidsintervallsparametrar för mått</span><span class="sxs-lookup"><span data-stu-id="eeb17-292">Added deprecation message for metrics time grains parameters</span></span>
    - <span data-ttu-id="eeb17-293">Tidsintervallsparametrar går fortfarande att använda (det här är en bakåtkompatibel ändring), men de ignoreras i serverdelen eftersom endast PT1M är giltigt</span><span class="sxs-lookup"><span data-stu-id="eeb17-293">Timegrains parameters are still being accepted (this is a non-breaking change,) but they are ignored in the backend since only PT1M is valid</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="eeb17-294">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="eeb17-294">AzureRM.Network</span></span>
* <span data-ttu-id="eeb17-295">Ändringar i LoadBalancer-cmdletar</span><span class="sxs-lookup"><span data-stu-id="eeb17-295">Changes to LoadBalancer cmdlets</span></span>
  - <span data-ttu-id="eeb17-296">LoadBalancerInboundNatPoolConfig: parametrarna IdleTimeoutInMinutes, EnableFloatingIp och EnableTcpReset har lagts till</span><span class="sxs-lookup"><span data-stu-id="eeb17-296">LoadBalancerInboundNatPoolConfig: added parameters IdleTimeoutInMinutes, EnableFloatingIp and EnableTcpReset</span></span>
  - <span data-ttu-id="eeb17-297">LoadBalancerInboundNatRuleConfig: parametern EnableTcpReset har lagts till</span><span class="sxs-lookup"><span data-stu-id="eeb17-297">LoadBalancerInboundNatRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="eeb17-298">LoadBalancerRuleConfig: parametern EnableTcpReset har lagts till</span><span class="sxs-lookup"><span data-stu-id="eeb17-298">LoadBalancerRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="eeb17-299">LoadBalancerProbeConfig: stöd för värdet ”Https” för parameterprotokoll har lagts till</span><span class="sxs-lookup"><span data-stu-id="eeb17-299">LoadBalancerProbeConfig: added support for value "Https" for parameter Protocol</span></span>
* <span data-ttu-id="eeb17-300">Nya kommandon för den nya underresursen för LoadBalancers OutboundRule har lagts till</span><span class="sxs-lookup"><span data-stu-id="eeb17-300">Added new commands for new LoadBalancer's subresource OutboundRule</span></span>
  - <span data-ttu-id="eeb17-301">Add-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="eeb17-301">Add-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="eeb17-302">Get-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="eeb17-302">Get-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="eeb17-303">New-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="eeb17-303">New-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="eeb17-304">Set-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="eeb17-304">Set-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="eeb17-305">Remove-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="eeb17-305">Remove-AzureRmLoadBalancerOutboundRuleConfig</span></span>
* <span data-ttu-id="eeb17-306">Ny HostedWorkloads-egenskap har lagts till för PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="eeb17-306">Added new HostedWorkloads property for PSNetworkInterface</span></span>
* <span data-ttu-id="eeb17-307">Nya cmdletar har lagts till för funktionen: Azure Firewall via ARM</span><span class="sxs-lookup"><span data-stu-id="eeb17-307">Added new cmdlets for feature: Azure Firewall via ARM</span></span>
  - <span data-ttu-id="eeb17-308">Get-AzureRmFirewall har lagts till</span><span class="sxs-lookup"><span data-stu-id="eeb17-308">Added Get-AzureRmFirewall</span></span>
  - <span data-ttu-id="eeb17-309">Set-AzureRmFirewall har lagts till</span><span class="sxs-lookup"><span data-stu-id="eeb17-309">Added Set-AzureRmFirewall</span></span>
  - <span data-ttu-id="eeb17-310">New-AzureRmFirewall har lagts till</span><span class="sxs-lookup"><span data-stu-id="eeb17-310">Added New-AzureRmFirewall</span></span>
  - <span data-ttu-id="eeb17-311">Remove-AzureRmFirewall har lagts till</span><span class="sxs-lookup"><span data-stu-id="eeb17-311">Added Remove-AzureRmFirewall</span></span>
  - <span data-ttu-id="eeb17-312">New-AzureRmFirewallApplicationRuleCollection har lagts till</span><span class="sxs-lookup"><span data-stu-id="eeb17-312">Added New-AzureRmFirewallApplicationRuleCollection</span></span>
  - <span data-ttu-id="eeb17-313">New-AzureRmFirewallApplicationRule har lagts till</span><span class="sxs-lookup"><span data-stu-id="eeb17-313">Added New-AzureRmFirewallApplicationRule</span></span>
  - <span data-ttu-id="eeb17-314">New-AzureRmFirewallNatRuleCollection har lagts till</span><span class="sxs-lookup"><span data-stu-id="eeb17-314">Added New-AzureRmFirewallNatRuleCollection</span></span>
  - <span data-ttu-id="eeb17-315">New-AzureRmFirewallNatRule har lagts till</span><span class="sxs-lookup"><span data-stu-id="eeb17-315">Added New-AzureRmFirewallNatRule</span></span>
  - <span data-ttu-id="eeb17-316">New-AzureRmFirewallNetworkRuleCollection har lagts till</span><span class="sxs-lookup"><span data-stu-id="eeb17-316">Added New-AzureRmFirewallNetworkRuleCollection</span></span>
  - <span data-ttu-id="eeb17-317">New-AzureRmFirewallNetworkRule har lagts till</span><span class="sxs-lookup"><span data-stu-id="eeb17-317">Added New-AzureRmFirewallNetworkRule</span></span>
* <span data-ttu-id="eeb17-318">Stöd för betrott rotcertifikat och konfiguration för autoskalning har lagts till i Application Gateway</span><span class="sxs-lookup"><span data-stu-id="eeb17-318">Added support for Trusted Root certificate and Autoscale configuration in Application Gateway</span></span>
  - <span data-ttu-id="eeb17-319">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="eeb17-319">New Cmdlets added:</span></span>
      - <span data-ttu-id="eeb17-320">Add-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="eeb17-320">Add-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="eeb17-321">Get-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="eeb17-321">Get-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="eeb17-322">New-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="eeb17-322">New-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="eeb17-323">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="eeb17-323">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="eeb17-324">Set-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="eeb17-324">Set-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="eeb17-325">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="eeb17-325">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="eeb17-326">New-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="eeb17-326">New-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="eeb17-327">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="eeb17-327">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="eeb17-328">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="eeb17-328">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
  - <span data-ttu-id="eeb17-329">Cmdletar har uppdaterats med valfri parameter – TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="eeb17-329">Cmdlets updated with optonal parameter -TrustedRootCertificate</span></span>
      - <span data-ttu-id="eeb17-330">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="eeb17-330">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="eeb17-331">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="eeb17-331">Set-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="eeb17-332">New-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="eeb17-332">New-AzureRmApplicationGatewayBackendHttpSetting</span></span>
      - <span data-ttu-id="eeb17-333">Set-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="eeb17-333">Set-AzureRmApplicationGatewayBackendHttpSetting</span></span>
  - <span data-ttu-id="eeb17-334">Cmdletar har uppdaterats med valfri parameter – AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="eeb17-334">Cmdlets updated with optonal parameter -AutoscaleConfiguration</span></span>
      - <span data-ttu-id="eeb17-335">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="eeb17-335">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="eeb17-336">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="eeb17-336">Set-AzureRmApplicationGateway</span></span>
* <span data-ttu-id="eeb17-337">Lägg till cmdlet för gränssnittsslutpunkten Get-AzureInterfaceEndpoint</span><span class="sxs-lookup"><span data-stu-id="eeb17-337">Add cmdlet for Interface Endpoint Get-AzureInterfaceEndpoint</span></span>
* <span data-ttu-id="eeb17-338">Stöd för flera adressprefix i ett undernät har lagts till.</span><span class="sxs-lookup"><span data-stu-id="eeb17-338">Added support for multiple address prefixes in a subnet.</span></span> <span data-ttu-id="eeb17-339">Uppdaterade cmdletar:</span><span class="sxs-lookup"><span data-stu-id="eeb17-339">Updated cmdlets:</span></span>
  - <span data-ttu-id="eeb17-340">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="eeb17-340">New-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="eeb17-341">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="eeb17-341">Set-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="eeb17-342">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="eeb17-342">Add-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="eeb17-343">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="eeb17-343">Get-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="eeb17-344">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="eeb17-344">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>
  - <span data-ttu-id="eeb17-345">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="eeb17-345">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="eeb17-346">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="eeb17-346">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="eeb17-347">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="eeb17-347">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="eeb17-348">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="eeb17-348">Add-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="eeb17-349">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="eeb17-349">New-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="eeb17-350">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="eeb17-350">Set-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="eeb17-351">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="eeb17-351">Add-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="eeb17-352">New-AzureRmNetworkInterfaceIpConfig – Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="eeb17-352">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="eeb17-353">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="eeb17-353">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="eeb17-354">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="eeb17-354">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="eeb17-355">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="eeb17-355">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="eeb17-356">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="eeb17-356">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="eeb17-357">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="eeb17-357">New-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="eeb17-358">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="eeb17-358">New-AzureRmNetworkInterface</span></span>
* <span data-ttu-id="eeb17-359">Lägger till cmdletar för delegering av undernät.</span><span class="sxs-lookup"><span data-stu-id="eeb17-359">Adding cmdlets for subnet delegation.</span></span>
  - <span data-ttu-id="eeb17-360">New-AzureRmDelegation: Skapar en ny delegering som kan läggas till i ett undernät</span><span class="sxs-lookup"><span data-stu-id="eeb17-360">New-AzureRmDelegation: Creates a new delegation, which can be added to a subnet</span></span>
  - <span data-ttu-id="eeb17-361">Remove-AzureRmDelegation: Hämtar ett undernät och tar bort det angivna delegeringsnamnet från undernätet</span><span class="sxs-lookup"><span data-stu-id="eeb17-361">Remove-AzureRmDelegation: Takes in a subnet and removes the provided delegation name from that subnet</span></span>
  - <span data-ttu-id="eeb17-362">Add-AzureRmDelegation: Hämtar ett undernät och lägger till det angivna tjänstnamnet som en delegering till undernätet</span><span class="sxs-lookup"><span data-stu-id="eeb17-362">Add-AzureRmDelegation: Takes in a subnet and adds the provided service name as a delegation to that subnet</span></span>
  - <span data-ttu-id="eeb17-363">Get-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="eeb17-363">Get-AzureRmDelegation</span></span>
  - <span data-ttu-id="eeb17-364">Get-AzureRmAvailableServiceDelegations</span><span class="sxs-lookup"><span data-stu-id="eeb17-364">Get-AzureRmAvailableServiceDelegations</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="eeb17-365">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="eeb17-365">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="eeb17-366">Stöd för hanterad disk</span><span class="sxs-lookup"><span data-stu-id="eeb17-366">Support for managed Managed disk</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="eeb17-367">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="eeb17-367">AzureRM.RedisCache</span></span>
* <span data-ttu-id="eeb17-368">Insights-beroende har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="eeb17-368">Updated Insights dependency.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="eeb17-369">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="eeb17-369">AzureRM.Resources</span></span>
* <span data-ttu-id="eeb17-370">Uppdatera New-AzureRmResourceGroupDeployment med den nya parametern RollbackAction</span><span class="sxs-lookup"><span data-stu-id="eeb17-370">Update New-AzureRmResourceGroupDeployment with new parameter RollbackAction</span></span>
    - <span data-ttu-id="eeb17-371">Lägg till stöd för OnErrorDeployment med den nya parametern.</span><span class="sxs-lookup"><span data-stu-id="eeb17-371">Add support for OnErrorDeployment with the new parameter.</span></span>
* <span data-ttu-id="eeb17-372">Stöd för hanterad identitet på principtilldelningar.</span><span class="sxs-lookup"><span data-stu-id="eeb17-372">Support managed identity on policy assignments.</span></span>
* <span data-ttu-id="eeb17-373">Parametrar med standardvärden krävs inte längre när du tilldelar en princip med ”New-AzureRmPolicyAssignment”</span><span class="sxs-lookup"><span data-stu-id="eeb17-373">Parameters with default values are no longer requred when assigning a policy with 'New-AzureRmPolicyAssignment'</span></span>
* <span data-ttu-id="eeb17-374">Lägg till den nya cmdleten Get-AzureRmPolicyAlias för att hämta principalias</span><span class="sxs-lookup"><span data-stu-id="eeb17-374">Add new cmdlet Get-AzureRmPolicyAlias for retrieving policy aliases</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="eeb17-375">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="eeb17-375">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="eeb17-376">Problem #7161 har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="eeb17-376">Fixed issue #7161</span></span>

#### <a name="azurermsignalr"></a><span data-ttu-id="eeb17-377">AzureRM.SignalR</span><span class="sxs-lookup"><span data-stu-id="eeb17-377">AzureRM.SignalR</span></span>
* <span data-ttu-id="eeb17-378">Uppdatera SKU-namn till Free_F1 och Standard_S1</span><span class="sxs-lookup"><span data-stu-id="eeb17-378">Update SKU names to Free_F1 and Standard_S1</span></span>
* <span data-ttu-id="eeb17-379">Lägg till versionsfältet i PSSignalRResource-objektet och en anslutningssträng i PSSignalRKeys-objektet.</span><span class="sxs-lookup"><span data-stu-id="eeb17-379">Add version field to the PSSignalRResource object and connection string to the PSSignalRKeys object.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="eeb17-380">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="eeb17-380">AzureRM.Storage</span></span>
* <span data-ttu-id="eeb17-381">Stöd för oföränderlighetsprincip i AzureRm.Storage</span><span class="sxs-lookup"><span data-stu-id="eeb17-381">Support Immutability Policy in AzureRm.Storage</span></span>
    - <span data-ttu-id="eeb17-382">Remove-AzureRmStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="eeb17-382">Remove-AzureRmStorageAccountNetworkRule</span></span>
    - <span data-ttu-id="eeb17-383">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="eeb17-383">Get-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="eeb17-384">Update-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="eeb17-384">Update-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="eeb17-385">New-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="eeb17-385">New-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="eeb17-386">Remove-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="eeb17-386">Remove-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="eeb17-387">Add-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="eeb17-387">Add-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="eeb17-388">Remove-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="eeb17-388">Remove-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="eeb17-389">Set-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="eeb17-389">Set-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="eeb17-390">Get-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="eeb17-390">Get-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="eeb17-391">Remove-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="eeb17-391">Remove-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="eeb17-392">Lock-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="eeb17-392">Lock-AzureRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="eeb17-393">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="eeb17-393">AzureRM.Websites</span></span>
* <span data-ttu-id="eeb17-394">Två nya cmdletar har lagts till: Get-AzureRmDeletedWebApp och Restore-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="eeb17-394">Added two new cmdlets: Get-AzureRmDeletedWebApp and Restore-AzureRmDeletedWebApp</span></span>
* <span data-ttu-id="eeb17-395">New-AzureRmAppServicePlan – En HyperV-växel har lagts till för skapa en app service-plan med Windows-containrar</span><span class="sxs-lookup"><span data-stu-id="eeb17-395">New-AzureRmAppServicePlan -HyperV switch is added for create app service plan with windows container</span></span>
* <span data-ttu-id="eeb17-396">New-AzureRmWebApp/New-AzureRmWebAppSlot/Set-AzureRmWebApp/Set-AzureRmWebAppSlot – Nya parametrar (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) har lagts till för att skapa och hantera Windows-containerappar</span><span class="sxs-lookup"><span data-stu-id="eeb17-396">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - New parameters (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) added for creating and managing windows container app</span></span>

## <a name="681---august-2018"></a><span data-ttu-id="eeb17-397">6.8.1 – augusti 2018</span><span class="sxs-lookup"><span data-stu-id="eeb17-397">6.8.1 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="eeb17-398">Allmänt</span><span class="sxs-lookup"><span data-stu-id="eeb17-398">General</span></span>
* <span data-ttu-id="eeb17-399">Problem med standardresursgrupp som inte har konfigurerats har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="eeb17-399">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="eeb17-400">Uppdaterade Common Runtime-sammansättningar</span><span class="sxs-lookup"><span data-stu-id="eeb17-400">Updated common runtime assemblies</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="eeb17-401">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="eeb17-401">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="eeb17-402">Problem med standardresursgrupp som inte har konfigurerats har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="eeb17-402">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="eeb17-403">Åtgärdat problem https://github.com/Azure/azure-powershell/issues/6603</span><span class="sxs-lookup"><span data-stu-id="eeb17-403">Fixed issue https://github.com/Azure/azure-powershell/issues/6603</span></span>
    - <span data-ttu-id="eeb17-404">Import-AzureRmApiManagementApi- och \*-AzureRmApiManagementCertificate-cmdletar kan nu hantera relativa sökvägar</span><span class="sxs-lookup"><span data-stu-id="eeb17-404">Import-AzureRmApiManagementApi and \*-AzureRmApiManagementCertificate cmdlets now handle relative Paths</span></span>
* <span data-ttu-id="eeb17-405">Åtgärdat problem https://github.com/Azure/azure-powershell/issues/6879</span><span class="sxs-lookup"><span data-stu-id="eeb17-405">Fixed issue https://github.com/Azure/azure-powershell/issues/6879</span></span>
    - <span data-ttu-id="eeb17-406">CertificateInformation är en inställbar egenskap som gör att Set-AzureRmApiManagement-cmdleten fungerar ordentligt.</span><span class="sxs-lookup"><span data-stu-id="eeb17-406">The CertificateInformation is a settable property allowing for Set-AzureRmApiManagement cmdlet to work property.</span></span> <span data-ttu-id="eeb17-407">Åtgärdat genom uppgradering till NuGet för 4.0.4-preview</span><span class="sxs-lookup"><span data-stu-id="eeb17-407">Fixed by upgrading to 4.0.4-preview nuget</span></span>
* <span data-ttu-id="eeb17-408">Åtgärdat problem https://github.com/Azure/azure-powershell/issues/6853</span><span class="sxs-lookup"><span data-stu-id="eeb17-408">Fixed issue https://github.com/Azure/azure-powershell/issues/6853</span></span>
    - <span data-ttu-id="eeb17-409">Odata-filtret för sökning efter namn på produkt har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="eeb17-409">Fixed the Odata filter for Search by Name on Product</span></span>
* <span data-ttu-id="eeb17-410">Åtgärdat problem https://github.com/Azure/azure-powershell/issues/6814</span><span class="sxs-lookup"><span data-stu-id="eeb17-410">Fixed issue https://github.com/Azure/azure-powershell/issues/6814</span></span>
    - <span data-ttu-id="eeb17-411">Odata-filtret för sökning efter namn på API har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="eeb17-411">Fixed the Odata filter for Search by Name on Api</span></span>
* <span data-ttu-id="eeb17-412">Stöd har lagts till för AzureMonitor-loggare</span><span class="sxs-lookup"><span data-stu-id="eeb17-412">Added support for AzureMonitor logger</span></span>


#### <a name="azurermcompute"></a><span data-ttu-id="eeb17-413">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="eeb17-413">AzureRM.Compute</span></span>
* <span data-ttu-id="eeb17-414">Ett problem med att mål saknas i felutdata har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="eeb17-414">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="eeb17-415">Problem med lagringskontotyper för virtuell dator med en hanterad disk har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="eeb17-415">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="eeb17-416">Problem med standardresursgrupp som inte har konfigurerats har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="eeb17-416">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="eeb17-417">Åtgärda cmdletar för AEM-tillägg för andra miljöer, till exempel Azure Kina</span><span class="sxs-lookup"><span data-stu-id="eeb17-417">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="eeb17-418">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="eeb17-418">AzureRM.Network</span></span>
* <span data-ttu-id="eeb17-419">Standardvisning av cmdlet-utdata har ändrats för att visas i tabellvy</span><span class="sxs-lookup"><span data-stu-id="eeb17-419">Changed default cmdlet output presentation to table view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="eeb17-420">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="eeb17-420">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="eeb17-421">Åtgärda fel i Update-AzureRmPowerBIEmbeddedCapacity vid försök att skala pausad kapacitet</span><span class="sxs-lookup"><span data-stu-id="eeb17-421">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>


#### <a name="azurermresources"></a><span data-ttu-id="eeb17-422">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="eeb17-422">AzureRM.Resources</span></span>
* <span data-ttu-id="eeb17-423">Ett problem med att skapa hanterade program från MarketPlace har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="eeb17-423">Fixed issue with creating managed applications from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="eeb17-424">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="eeb17-424">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="eeb17-425">Åtgärdade problem</span><span class="sxs-lookup"><span data-stu-id="eeb17-425">Fixed issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="eeb17-426">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="eeb17-426">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="eeb17-427">Stöd har lagts till för trafikroutningsmetoden MultiValue</span><span class="sxs-lookup"><span data-stu-id="eeb17-427">Added Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="eeb17-428">Ny parameter, ”MaxReturn”, för MultiValue-routning</span><span class="sxs-lookup"><span data-stu-id="eeb17-428">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="eeb17-429">Stöd har lagts till för trafikroutningsmetod för undernät</span><span class="sxs-lookup"><span data-stu-id="eeb17-429">Added Support for the Subnet routing method</span></span>
    - <span data-ttu-id="eeb17-430">Stöd för IP-adressintervall (undernät) i slutpunkter</span><span class="sxs-lookup"><span data-stu-id="eeb17-430">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="eeb17-431">Stöd har lagts till för anpassade rubriker i profiler</span><span class="sxs-lookup"><span data-stu-id="eeb17-431">Added Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="eeb17-432">Stöd har lagts till för förväntade statuskodintervall i profiler</span><span class="sxs-lookup"><span data-stu-id="eeb17-432">Added Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="eeb17-433">Stöd har lagts till för anpassade rubriker i slutpunkter</span><span class="sxs-lookup"><span data-stu-id="eeb17-433">Added Support for Custom Headers in endpoints</span></span>

## <a name="680---august-2018"></a><span data-ttu-id="eeb17-434">6.8.0 – augusti 2018</span><span class="sxs-lookup"><span data-stu-id="eeb17-434">6.8.0 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="eeb17-435">Allmänt</span><span class="sxs-lookup"><span data-stu-id="eeb17-435">General</span></span>
* <span data-ttu-id="eeb17-436">Problem med standardresursgrupp som inte har konfigurerats har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="eeb17-436">Fixed issue with default resource groups not being set.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="eeb17-437">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="eeb17-437">AzureRM.Profile</span></span>
* <span data-ttu-id="eeb17-438">Utgångsegenskap har lagts till i token som returneras under Connect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="eeb17-438">Added expiration property to tokens returned during Connect-AzureRmAccount</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="eeb17-439">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="eeb17-439">AzureRM.Compute</span></span>
* <span data-ttu-id="eeb17-440">Ett problem med att mål saknas i felutdata har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="eeb17-440">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="eeb17-441">Problem med lagringskontotyper för virtuell dator med en hanterad disk har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="eeb17-441">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="eeb17-442">Åtgärda cmdletar för AEM-tillägg för andra miljöer, till exempel Azure Kina</span><span class="sxs-lookup"><span data-stu-id="eeb17-442">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="eeb17-443">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="eeb17-443">AzureRM.IotHub</span></span>
* <span data-ttu-id="eeb17-444">Korrigera exempel för New-AzureRmIotHubExportDevices och New-AzureRmIotHubImportDevices</span><span class="sxs-lookup"><span data-stu-id="eeb17-444">Fix examples for New-AzureRmIotHubExportDevices and New-AzureRmIotHubImportDevices</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="eeb17-445">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="eeb17-445">AzureRM.Network</span></span>
* <span data-ttu-id="eeb17-446">Standardmodeller har ändrats för att visas i tabellvy</span><span class="sxs-lookup"><span data-stu-id="eeb17-446">Changed default models representation to table-view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="eeb17-447">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="eeb17-447">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="eeb17-448">Åtgärda fel i Update-AzureRmPowerBIEmbeddedCapacity vid försök att skala pausad kapacitet</span><span class="sxs-lookup"><span data-stu-id="eeb17-448">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="eeb17-449">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="eeb17-449">AzureRM.Resources</span></span>
* <span data-ttu-id="eeb17-450">Ett problem med att skapa hanterade program från MarketPlace har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="eeb17-450">Fixed issue with creating managed application from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="eeb17-451">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="eeb17-451">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="eeb17-452">Korrigeringar för problem</span><span class="sxs-lookup"><span data-stu-id="eeb17-452">Fix for issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="eeb17-453">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="eeb17-453">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="eeb17-454">Stöd för trafikroutningsmetoden MultiValue</span><span class="sxs-lookup"><span data-stu-id="eeb17-454">Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="eeb17-455">Ny parameter, ”MaxReturn”, för MultiValue-routning</span><span class="sxs-lookup"><span data-stu-id="eeb17-455">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="eeb17-456">Stöd för trafikroutningsmetod för undernät</span><span class="sxs-lookup"><span data-stu-id="eeb17-456">Support for the Subnet routing method</span></span>
    - <span data-ttu-id="eeb17-457">Stöd för IP-adressintervall (undernät) i slutpunkter</span><span class="sxs-lookup"><span data-stu-id="eeb17-457">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="eeb17-458">Stöd för anpassade rubriker i profiler</span><span class="sxs-lookup"><span data-stu-id="eeb17-458">Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="eeb17-459">Stöd för förväntade statuskodintervall i profiler</span><span class="sxs-lookup"><span data-stu-id="eeb17-459">Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="eeb17-460">Stöd för anpassade rubriker i slutpunkter</span><span class="sxs-lookup"><span data-stu-id="eeb17-460">Support for Custom Headers in endpoints</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="eeb17-461">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="eeb17-461">AzureRM.Websites</span></span>
* <span data-ttu-id="eeb17-462">Problem med standardresursgrupp som inte har konfigurerats korrekt har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="eeb17-462">Fixed issue with default resource group being set incorrectly.</span></span>

## <a name="670---august-2018"></a><span data-ttu-id="eeb17-463">6.7.0 – augusti 2018</span><span class="sxs-lookup"><span data-stu-id="eeb17-463">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="eeb17-464">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="eeb17-464">AzureRM.Profile</span></span>
* <span data-ttu-id="eeb17-465">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="eeb17-465">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="eeb17-466">Lägg till användar-id i standardkontextnamnet för att undvika kontextkonflikter</span><span class="sxs-lookup"><span data-stu-id="eeb17-466">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="eeb17-467">Åtgärda problem med Clear-AzureRmContext som orsakade problem med att välja en kontext #6398</span><span class="sxs-lookup"><span data-stu-id="eeb17-467">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="eeb17-468">Aktivera den klientorganisationsdomän som ska skickas till parametern -TenantId för Connect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="eeb17-468">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="eeb17-469">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="eeb17-469">Azure.Storage</span></span>
* <span data-ttu-id="eeb17-470">Ta bort begränsningen på 5 TB för Azure-filresurskvoten</span><span class="sxs-lookup"><span data-stu-id="eeb17-470">Remove the 5TB limitation for Azure File Share quota</span></span>
* <span data-ttu-id="eeb17-471">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="eeb17-471">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="eeb17-472">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="eeb17-472">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="eeb17-473">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="eeb17-473">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="eeb17-474">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="eeb17-474">Azure.AnalysisServices</span></span>
* <span data-ttu-id="eeb17-475">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="eeb17-475">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="eeb17-476">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="eeb17-476">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="eeb17-477">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="eeb17-477">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="eeb17-478">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="eeb17-478">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="eeb17-479">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="eeb17-479">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="eeb17-480">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="eeb17-480">AzureRM.Automation</span></span>
* <span data-ttu-id="eeb17-481">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="eeb17-481">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="eeb17-482">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="eeb17-482">AzureRM.Backup</span></span>
* <span data-ttu-id="eeb17-483">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="eeb17-483">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="eeb17-484">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="eeb17-484">AzureRM.Batch</span></span>
* <span data-ttu-id="eeb17-485">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="eeb17-485">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="eeb17-486">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="eeb17-486">AzureRM.Billing</span></span>
* <span data-ttu-id="eeb17-487">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="eeb17-487">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="eeb17-488">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="eeb17-488">AzureRM.Cdn</span></span>
* <span data-ttu-id="eeb17-489">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="eeb17-489">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="eeb17-490">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="eeb17-490">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="eeb17-491">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="eeb17-491">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="eeb17-492">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="eeb17-492">AzureRM.Compute</span></span>
* <span data-ttu-id="eeb17-493">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="eeb17-493">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="eeb17-494">Lägg till parametern EvictionPolicy i New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="eeb17-494">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="eeb17-495">Använd standardplatsen i DiskFileParameterSet för New-AzureRmVm om ingen plats har angetts.</span><span class="sxs-lookup"><span data-stu-id="eeb17-495">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="eeb17-496">Korrigera parameterbeskrivningen i Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="eeb17-496">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="eeb17-497">Korrigera cmdleten Get-AzureRmVMDiskEncryptionStatus för vissa singlepass-relaterade scenarier</span><span class="sxs-lookup"><span data-stu-id="eeb17-497">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="eeb17-498">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="eeb17-498">AzureRM.Consumption</span></span>
* <span data-ttu-id="eeb17-499">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="eeb17-499">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="eeb17-500">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="eeb17-500">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="eeb17-501">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="eeb17-501">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="eeb17-502">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="eeb17-502">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="eeb17-503">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="eeb17-503">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="eeb17-504">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="eeb17-504">AzureRM.DataFactories</span></span>
* <span data-ttu-id="eeb17-505">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="eeb17-505">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="eeb17-506">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="eeb17-506">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="eeb17-507">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="eeb17-507">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="eeb17-508">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="eeb17-508">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="eeb17-509">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="eeb17-509">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="eeb17-510">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="eeb17-510">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="eeb17-511">Korrigera felsökning när DebugPreference anges från powershell-kommandoraden</span><span class="sxs-lookup"><span data-stu-id="eeb17-511">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="eeb17-512">Uppdatera exemplet för Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="eeb17-512">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="eeb17-513">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="eeb17-513">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="eeb17-514">Uppdatera exemplet för Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="eeb17-514">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="eeb17-515">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="eeb17-515">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="eeb17-516">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="eeb17-516">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="eeb17-517">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="eeb17-517">AzureRM.Dns</span></span>
* <span data-ttu-id="eeb17-518">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="eeb17-518">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="eeb17-519">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="eeb17-519">AzureRM.EventGrid</span></span>
* <span data-ttu-id="eeb17-520">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="eeb17-520">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="eeb17-521">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="eeb17-521">AzureRM.EventHub</span></span>
* <span data-ttu-id="eeb17-522">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="eeb17-522">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="eeb17-523">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="eeb17-523">AzureRM.HDInsight</span></span>
* <span data-ttu-id="eeb17-524">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="eeb17-524">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="eeb17-525">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="eeb17-525">AzureRM.Insights</span></span>
* <span data-ttu-id="eeb17-526">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="eeb17-526">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="eeb17-527">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="eeb17-527">AzureRM.IotHub</span></span>
* <span data-ttu-id="eeb17-528">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="eeb17-528">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="eeb17-529">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="eeb17-529">AzureRM.KeyVault</span></span>
* <span data-ttu-id="eeb17-530">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="eeb17-530">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="eeb17-531">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="eeb17-531">AzureRM.LogicApp</span></span>
* <span data-ttu-id="eeb17-532">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="eeb17-532">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="eeb17-533">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="eeb17-533">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="eeb17-534">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="eeb17-534">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="eeb17-535">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="eeb17-535">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="eeb17-536">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="eeb17-536">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="eeb17-537">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="eeb17-537">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="eeb17-538">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="eeb17-538">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="eeb17-539">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="eeb17-539">AzureRM.Media</span></span>
* <span data-ttu-id="eeb17-540">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="eeb17-540">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="eeb17-541">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="eeb17-541">AzureRM.Network</span></span>
* <span data-ttu-id="eeb17-542">Exempel för Set-AzureRmLocalNetworkGateway har lagts till</span><span class="sxs-lookup"><span data-stu-id="eeb17-542">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="eeb17-543">Exempel och beskrivningar för Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey och New-AzureRmVirtualNetworkGatewayConnection har lagts till</span><span class="sxs-lookup"><span data-stu-id="eeb17-543">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="eeb17-544">Exempel för Remove-AzureRmVirtualNetworkGatewayIpConfig och Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="eeb17-544">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="eeb17-545">Exempel för Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey har lagts till</span><span class="sxs-lookup"><span data-stu-id="eeb17-545">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="eeb17-546">Exempel för Set-AzureRmVirtualNetworkGatewayConnectionSharedKey har lagts till</span><span class="sxs-lookup"><span data-stu-id="eeb17-546">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="eeb17-547">Exempel för Set-AzureRmVirtualNetworkGatewayConnection har lagts till</span><span class="sxs-lookup"><span data-stu-id="eeb17-547">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="eeb17-548">Cmdletar för ApplicationSecurityGroup, RouteTable and Usage har genererats om med den senaste kodgeneratorn</span><span class="sxs-lookup"><span data-stu-id="eeb17-548">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="eeb17-549">Förtydligade ett felmeddelande för Get-AzureRmVirtualNetworkSubnetConfig vid försök att hämta ett undernät som inte avslutas</span><span class="sxs-lookup"><span data-stu-id="eeb17-549">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="eeb17-550">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="eeb17-550">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="eeb17-551">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="eeb17-551">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="eeb17-552">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="eeb17-552">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="eeb17-553">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="eeb17-553">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="eeb17-554">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="eeb17-554">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="eeb17-555">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="eeb17-555">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="eeb17-556">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="eeb17-556">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="eeb17-557">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="eeb17-557">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="eeb17-558">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="eeb17-558">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="eeb17-559">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="eeb17-559">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="eeb17-560">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="eeb17-560">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="eeb17-561">Lade till principfilter i cmdleten Get-AzureRmRecoveryServicesBackItem.</span><span class="sxs-lookup"><span data-stu-id="eeb17-561">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="eeb17-562">Kommandot returnerar listan med säkerhetskopieringsobjekt som skyddas av det angivna princip-ID:t.</span><span class="sxs-lookup"><span data-stu-id="eeb17-562">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="eeb17-563">Microsoft.Azure.Management.RecoveryServices.Backup uppdaterades till förhandsversionen av 3.0.0.</span><span class="sxs-lookup"><span data-stu-id="eeb17-563">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="eeb17-564">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="eeb17-564">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="eeb17-565">Parametern TargetResourceGroupName lades till i Restore-AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="eeb17-565">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="eeb17-566">Den resursgrupp som de hanterade diskarna återställs till.</span><span class="sxs-lookup"><span data-stu-id="eeb17-566">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="eeb17-567">Gäller för säkerhetskopiering av virtuell dator med hanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="eeb17-567">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="eeb17-568">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="eeb17-568">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="eeb17-569">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="eeb17-569">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="eeb17-570">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="eeb17-570">AzureRM.RedisCache</span></span>
* <span data-ttu-id="eeb17-571">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="eeb17-571">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="eeb17-572">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="eeb17-572">AzureRM.Relay</span></span>
* <span data-ttu-id="eeb17-573">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="eeb17-573">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="eeb17-574">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="eeb17-574">AzureRM.Resources</span></span>
* <span data-ttu-id="eeb17-575">Distribution av supportmall i prenumerationsomfånget.</span><span class="sxs-lookup"><span data-stu-id="eeb17-575">Support template deployment at subscription scope.</span></span> <span data-ttu-id="eeb17-576">Lägg till nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="eeb17-576">Add new Cmdlets:</span></span>
    - <span data-ttu-id="eeb17-577">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="eeb17-577">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="eeb17-578">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="eeb17-578">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="eeb17-579">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="eeb17-579">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="eeb17-580">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="eeb17-580">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="eeb17-581">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="eeb17-581">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="eeb17-582">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="eeb17-582">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="eeb17-583">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="eeb17-583">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="eeb17-584">Korrigera ett problem där fel inträffar när en kontext skickas till Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="eeb17-584">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="eeb17-585">Korrigera exempel i New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="eeb17-585">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="eeb17-586">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="eeb17-586">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="eeb17-587">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="eeb17-587">AzureRM.Scheduler</span></span>
* <span data-ttu-id="eeb17-588">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="eeb17-588">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="eeb17-589">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="eeb17-589">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="eeb17-590">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="eeb17-590">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="eeb17-591">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="eeb17-591">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="eeb17-592">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="eeb17-592">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="eeb17-593">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="eeb17-593">AzureRM.Sql</span></span>
* <span data-ttu-id="eeb17-594">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="eeb17-594">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="eeb17-595">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="eeb17-595">AzureRM.Storage</span></span>
* <span data-ttu-id="eeb17-596">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="eeb17-596">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="eeb17-597">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="eeb17-597">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="eeb17-598">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="eeb17-598">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="eeb17-599">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="eeb17-599">AzureRM.Tags</span></span>
* <span data-ttu-id="eeb17-600">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="eeb17-600">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="eeb17-601">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="eeb17-601">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="eeb17-602">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="eeb17-602">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="eeb17-603">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="eeb17-603">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="eeb17-604">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="eeb17-604">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="eeb17-605">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="eeb17-605">AzureRM.Websites</span></span>
* <span data-ttu-id="eeb17-606">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="eeb17-606">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="eeb17-607">6.6.0 – juli 2018</span><span class="sxs-lookup"><span data-stu-id="eeb17-607">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="eeb17-608">Allmänt</span><span class="sxs-lookup"><span data-stu-id="eeb17-608">General</span></span>
* <span data-ttu-id="eeb17-609">Alla hjälpfiler har uppdaterats för att ta med fullständiga parametertyper och korrekta indata-/utdatatyper.</span><span class="sxs-lookup"><span data-stu-id="eeb17-609">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="eeb17-610">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="eeb17-610">AzureRM.Profile</span></span>
* <span data-ttu-id="eeb17-611">Common.Strategy-biblioteket har uppdaterats för att kunna verifiera att den aktuella konfigurationsfilen för en resurs är kompatibel med målresursen.</span><span class="sxs-lookup"><span data-stu-id="eeb17-611">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="eeb17-612">ps1xml-typer har lagts till i Common.Storage</span><span class="sxs-lookup"><span data-stu-id="eeb17-612">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="eeb17-613">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="eeb17-613">Azure.Storage</span></span>
* <span data-ttu-id="eeb17-614">Lade till stöd för hämtning av lagringskontext från DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eeb17-614">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="eeb17-615">Lade till Ps1XmlAttribute till utdatatypegenskaper för cmdletar.</span><span class="sxs-lookup"><span data-stu-id="eeb17-615">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="eeb17-616">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="eeb17-616">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="eeb17-617">Åtgärdat problem https://github.com/Azure/azure-powershell/issues/6370</span><span class="sxs-lookup"><span data-stu-id="eeb17-617">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="eeb17-618">En bugg har åtgärdats i Automapper för att översätta PsApiManagementApi till ApiContract</span><span class="sxs-lookup"><span data-stu-id="eeb17-618">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="eeb17-619">Åtgärdat problem https://github.com/Azure/azure-powershell/issues/6515</span><span class="sxs-lookup"><span data-stu-id="eeb17-619">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="eeb17-620">En bugg har åtgärdats i File.Save för att inte överbelasta kodningstypen</span><span class="sxs-lookup"><span data-stu-id="eeb17-620">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="eeb17-621">Åtgärdat problem https://github.com/Azure/azure-powershell/issues/6560</span><span class="sxs-lookup"><span data-stu-id="eeb17-621">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="eeb17-622">Har uppgraderats till Nuget-versionen 4.0.3 vilket åtgärdar mönsterundantaget på apiId</span><span class="sxs-lookup"><span data-stu-id="eeb17-622">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="eeb17-623">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="eeb17-623">AzureRM.Compute</span></span>
* <span data-ttu-id="eeb17-624">Åtgärda problem med fel vid skapandet av en virtuell dator med hjälp av DiskFileParameterSet i New-AzureRmVm på grund av namnbyte på PremiumLRS-lagringskontotypen.</span><span class="sxs-lookup"><span data-stu-id="eeb17-624">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="eeb17-625">Åtgärda cmdleten Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="eeb17-625">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="eeb17-626">Uppdatera Get-AzureRmAvailabilitySet för att aktivera funktionen för att lista alla tillgänglighetsuppsättningar i en prenumeration.</span><span class="sxs-lookup"><span data-stu-id="eeb17-626">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="eeb17-627">(Parametern ResouceGroupName är nu frivillig.)</span><span class="sxs-lookup"><span data-stu-id="eeb17-627">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="eeb17-628">Uppdatera SimpleParameterSet för "New-AzureRmVm" för att aktivera accelererat nätverk på berättigade virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="eeb17-628">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="eeb17-629">Uppdatera den enkla parameteruppsättningen för New-AzureRmVmss så att det inte går att skapa de virtuella datorerna när en användarangiven lastbalanserare redan finns.</span><span class="sxs-lookup"><span data-stu-id="eeb17-629">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="eeb17-630">Uppdatera exempel för New-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="eeb17-630">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="eeb17-631">Lägg till exempel för "New-AzureRmVM"</span><span class="sxs-lookup"><span data-stu-id="eeb17-631">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="eeb17-632">Uppdatera beskrivning för Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="eeb17-632">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="eeb17-633">Uppdatera Exempel 1 för Set-AzureRmVMBginfoExtension för stavningskontroll och prefix.</span><span class="sxs-lookup"><span data-stu-id="eeb17-633">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="eeb17-634">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="eeb17-634">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="eeb17-635">ADF .Net SDK-versionen har uppdaterats till 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="eeb17-635">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="eeb17-636">Stöd för delning av Integration Runtime (lokal installation) mellan datafabriker.</span><span class="sxs-lookup"><span data-stu-id="eeb17-636">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="eeb17-637">Lägg till ny parameter – SharedIntegrationRuntimeResourceId i cmdleten Set-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="eeb17-637">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="eeb17-638">Lägg till ny valfri parameter – LinkedDataFactoryName i cmdleten Remove-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="eeb17-638">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="eeb17-639">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="eeb17-639">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="eeb17-640">DataPlane SDK-versionen (Microsoft.Azure.DataLake.Store) har uppdaterats till 1.1.9</span><span class="sxs-lookup"><span data-stu-id="eeb17-640">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="eeb17-641">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="eeb17-641">AzureRM.EventHub</span></span>
* <span data-ttu-id="eeb17-642">Piping för InputObject and ResourceId i borttagna cmdletar har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="eeb17-642">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="eeb17-643">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="eeb17-643">AzureRM.Insights</span></span>
* <span data-ttu-id="eeb17-644">Formatering har åtgärdats för OutputType i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="eeb17-644">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="eeb17-645">Använda Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span><span class="sxs-lookup"><span data-stu-id="eeb17-645">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="eeb17-646">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="eeb17-646">AzureRM.KeyVault</span></span>
* <span data-ttu-id="eeb17-647">Åtgärda problem med piping i Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="eeb17-647">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="eeb17-648">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="eeb17-648">AzureRM.Network</span></span>
* <span data-ttu-id="eeb17-649">Exempel har lagts till för LoadBalancerInboundNatPoolConfig-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="eeb17-649">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="eeb17-650">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="eeb17-650">AzureRM.Resources</span></span>
* <span data-ttu-id="eeb17-651">Åtgärda problem när både taggnamn och värde anges för "Get-AzureRmResource"</span><span class="sxs-lookup"><span data-stu-id="eeb17-651">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="eeb17-652">Åtgärda pipingscenario med "Set-AzureRmResource"</span><span class="sxs-lookup"><span data-stu-id="eeb17-652">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="eeb17-653">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="eeb17-653">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="eeb17-654">Piping för InputObject and ResourceId i borttagna cmdletar har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="eeb17-654">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="eeb17-655">några problem har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="eeb17-655">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="eeb17-656">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="eeb17-656">AzureRM.Sql</span></span>
* <span data-ttu-id="eeb17-657">Lägg till stöd för Server Advanced Threat Protection med följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="eeb17-657">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="eeb17-658">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="eeb17-658">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="eeb17-659">Lägg till stöd för Sårbarhetsbedömning med följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="eeb17-659">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="eeb17-660">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="eeb17-660">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="eeb17-661">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="eeb17-661">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="eeb17-662">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="eeb17-662">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="eeb17-663">Exempel i Remove-AzureRmSqlServerFirewallRule har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="eeb17-663">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="eeb17-664">Åtgärda felaktig hantering av datum och tid för andra kulturer än usa-baserade kulturer i Get-AzureSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="eeb17-664">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="eeb17-665">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="eeb17-665">AzureRM.Storage</span></span>
* <span data-ttu-id="eeb17-666">Lägg till Ps1XmlAttribute i utdatatypegenskaper för cmdletar</span><span class="sxs-lookup"><span data-stu-id="eeb17-666">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="eeb17-667">Visa utdata för cmdleten StorageAccount i tabellvyn</span><span class="sxs-lookup"><span data-stu-id="eeb17-667">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="eeb17-668">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="eeb17-668">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="eeb17-669">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="eeb17-669">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="eeb17-670">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="eeb17-670">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="eeb17-671">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="eeb17-671">AzureRM.Tags</span></span>
* <span data-ttu-id="eeb17-672">Ta bort felaktig instruktion från hjälpen för cmdleten Tag</span><span class="sxs-lookup"><span data-stu-id="eeb17-672">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="eeb17-673">6.5.0 – juli 2018</span><span class="sxs-lookup"><span data-stu-id="eeb17-673">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="eeb17-674">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="eeb17-674">AzureRM.Profile</span></span>
* <span data-ttu-id="eeb17-675">Hjälp för ”Get-AzureRmContextAutosaveSetting” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="eeb17-675">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="eeb17-676">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="eeb17-676">Azure.Storage</span></span>
* <span data-ttu-id="eeb17-677">Stöd för uppladdning av blob eller fil med lässkyddad SAS-token</span><span class="sxs-lookup"><span data-stu-id="eeb17-677">Support Upload Blob or File with write only Sas token</span></span>
* <span data-ttu-id="eeb17-678">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="eeb17-678">Set-AzureStorageBlobContent</span></span>
* <span data-ttu-id="eeb17-679">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="eeb17-679">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="eeb17-680">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="eeb17-680">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="eeb17-681">Lägg till den nödvändiga egenskapen ResourceGroupName i AS.</span><span class="sxs-lookup"><span data-stu-id="eeb17-681">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="eeb17-682">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="eeb17-682">AzureRM.Automation</span></span>
* <span data-ttu-id="eeb17-683">Uppdatera hjälp och lägg till exempel för ”New-AzureRMAutomationSchedule”</span><span class="sxs-lookup"><span data-stu-id="eeb17-683">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="eeb17-684">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="eeb17-684">AzureRM.Compute</span></span>
* <span data-ttu-id="eeb17-685">Lägg till parametern -Tag förUpdate/New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="eeb17-685">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="eeb17-686">Lägg till exempel för ”Add-AzureRmVmssExtension”</span><span class="sxs-lookup"><span data-stu-id="eeb17-686">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="eeb17-687">Lägg till exempel för ”Remove-AzureRmVmssExtension”</span><span class="sxs-lookup"><span data-stu-id="eeb17-687">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="eeb17-688">Uppdatera hjälp för ”Set-AzureRmVMAccessExtension”</span><span class="sxs-lookup"><span data-stu-id="eeb17-688">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="eeb17-689">Uppdatera SimpleParameterSet för New-AzureRmVmss för att ställa in SinglePlacementGroup på falskt som standard och lägg till växlingsparametern ”SinglePlacementGroup” som gör att användare kan skapa VMSS i en enda placeringsgrupp.</span><span class="sxs-lookup"><span data-stu-id="eeb17-689">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="eeb17-690">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="eeb17-690">AzureRM.EventHub</span></span>
* <span data-ttu-id="eeb17-691">En skrivskyddad egenskap, ”PendingReplicationOperationsCount”, har lagts till för klassen PSEventHubDRConfigurationAttributes som anger antalet väntande replikeringsåtgärder medan replikeringen pågår</span><span class="sxs-lookup"><span data-stu-id="eeb17-691">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="eeb17-692">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="eeb17-692">AzureRM.KeyVault</span></span>
* <span data-ttu-id="eeb17-693">Uppdatera felmeddelande för Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="eeb17-693">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="eeb17-694">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="eeb17-694">AzureRM.LogicApp</span></span>
* <span data-ttu-id="eeb17-695">Felet ”parameteruppsättningen gick inte att matcha” har korrigerats i New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="eeb17-695">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="eeb17-696">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="eeb17-696">AzureRM.Network</span></span>
* <span data-ttu-id="eeb17-697">Aktivera peering mellan virtuella nätverk i flera klienter för Set/Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="eeb17-697">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="eeb17-698">Nedanstående cmdletar för Application Gateway har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="eeb17-698">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="eeb17-699">New-AzureRmApplicationGateway: EnableFIPS-flagga har lagts till för stöd för zoner</span><span class="sxs-lookup"><span data-stu-id="eeb17-699">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="eeb17-700">New-AzureRmApplicationGatewaySku: nya SKU:er, Standard_v2 och WAF_v2, har lagts till</span><span class="sxs-lookup"><span data-stu-id="eeb17-700">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="eeb17-701">Set-AzureRmApplicationGatewaySku : nya SKU:er, Standard_v2 och WAF_v2, har lagts till</span><span class="sxs-lookup"><span data-stu-id="eeb17-701">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="eeb17-702">RouteTable-cmdletar har återskapats med den senaste versionen av generatorn</span><span class="sxs-lookup"><span data-stu-id="eeb17-702">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="eeb17-703">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="eeb17-703">AzureRM.Relay</span></span>
* <span data-ttu-id="eeb17-704">Markdown-filer har uppdaterats och korrigerar problem med parameternamn i exemplet</span><span class="sxs-lookup"><span data-stu-id="eeb17-704">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="eeb17-705">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="eeb17-705">AzureRM.Resources</span></span>
* <span data-ttu-id="eeb17-706">Uppdatera cmdletar för rolltilldelning och rolldefinition:</span><span class="sxs-lookup"><span data-stu-id="eeb17-706">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="eeb17-707">Ta bort extra anrop för rolldefinitioner som görs som en del av sidindelning.</span><span class="sxs-lookup"><span data-stu-id="eeb17-707">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="eeb17-708">Åtgärda Get-AzureRMRoleAssignment-cmdlet</span><span class="sxs-lookup"><span data-stu-id="eeb17-708">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="eeb17-709">Åtgärda parameterfunktioner för kommandot -ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="eeb17-709">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="eeb17-710">Åtgärda problem med ”Get-AzureRmResource” där ”-ResourceType”-parametern var skiftlägeskänsligt</span><span class="sxs-lookup"><span data-stu-id="eeb17-710">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="eeb17-711">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="eeb17-711">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="eeb17-712">Parametrar för att stoppa och hoppa över har lagts till i listan över cmdletar</span><span class="sxs-lookup"><span data-stu-id="eeb17-712">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="eeb17-713">Cmdletar för migrering från Standard- till Premium-namnområden har lagts till:</span><span class="sxs-lookup"><span data-stu-id="eeb17-713">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="eeb17-714">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="eeb17-714">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="eeb17-715">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="eeb17-715">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="eeb17-716">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="eeb17-716">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="eeb17-717">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="eeb17-717">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="eeb17-718">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="eeb17-718">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="eeb17-719">En skrivskyddad egenskap, ”PendingReplicationOperationsCount” har lagts till för klassen PSServiceBusDRConfigurationAttributes som anger antalet väntande replikeringsåtgärder medan replikeringen pågår</span><span class="sxs-lookup"><span data-stu-id="eeb17-719">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="eeb17-720">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="eeb17-720">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="eeb17-721">Uppdatera exempel för ”New-AzureRmServiceFabricCluster”</span><span class="sxs-lookup"><span data-stu-id="eeb17-721">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="eeb17-722">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="eeb17-722">AzureRM.Sql</span></span>
* <span data-ttu-id="eeb17-723">Nya cmdletar för Management.Sql som gör att kunderna kan lägga till certifikat för transparent datakryptering till SQL Server-instans eller en hanterad instans har lagts till</span><span class="sxs-lookup"><span data-stu-id="eeb17-723">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="eeb17-724">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="eeb17-724">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="eeb17-725">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="eeb17-725">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="eeb17-726">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="eeb17-726">AzureRM.Websites</span></span>
* <span data-ttu-id="eeb17-727">När `Set-AzureRmWebApp -AssignIdentity` och `Set-AzureRmWebAppSlot -AssignIdentity` är inställda på falskt tar de nu bort identitetsegenskapen från platsobjektet. Även förhandsgranskningstaggen tas bort.</span><span class="sxs-lookup"><span data-stu-id="eeb17-727">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="eeb17-728">`Get-AzureRmWebAppMetrics`, `Get-AzureRmAppServicePlanMetrics`-exempel har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="eeb17-728">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="eeb17-729">`Set-AzureRmWebApp -PhpVersion` har stöd för ”av” som en giltig php-version</span><span class="sxs-lookup"><span data-stu-id="eeb17-729">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="eeb17-730">6.4.0 – juli 2018</span><span class="sxs-lookup"><span data-stu-id="eeb17-730">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="eeb17-731">Allmänt</span><span class="sxs-lookup"><span data-stu-id="eeb17-731">General</span></span>
* <span data-ttu-id="eeb17-732">Formatering av OutputType i hjälpfiler har korrigerats för de flesta moduler</span><span class="sxs-lookup"><span data-stu-id="eeb17-732">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="eeb17-733">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="eeb17-733">AzureRM.Profile</span></span>
* <span data-ttu-id="eeb17-734">Ps1Xml-attribut har lagts till för grundläggande utdatatyper</span><span class="sxs-lookup"><span data-stu-id="eeb17-734">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="eeb17-735">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="eeb17-735">AzureRM.Compute</span></span>
* <span data-ttu-id="eeb17-736">IP-tagg-funktioner för VMSS</span><span class="sxs-lookup"><span data-stu-id="eeb17-736">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="eeb17-737">"New-AzureRmVmssIpTagConfig"-cmdlet har lagts till</span><span class="sxs-lookup"><span data-stu-id="eeb17-737">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="eeb17-738">IpTag-parameter har lagts till för New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="eeb17-738">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="eeb17-739">Automatisk återställningsfunktion för operativsystem för VMSS</span><span class="sxs-lookup"><span data-stu-id="eeb17-739">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="eeb17-740">DisableAutoRollback-parametrar har lagts till för New-AzureRmVmssConfig och Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="eeb17-740">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="eeb17-741">Funktion för uppgraderingshistorik för operativsystem för Vmss</span><span class="sxs-lookup"><span data-stu-id="eeb17-741">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="eeb17-742">OSUpgradeHistory-växlingsparametern har lagts till för Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="eeb17-742">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="eeb17-743">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="eeb17-743">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="eeb17-744">Lägg till stöd för katalog-ACL:er med hjälp av följande kommandon:</span><span class="sxs-lookup"><span data-stu-id="eeb17-744">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="eeb17-745">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="eeb17-745">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="eeb17-746">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="eeb17-746">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="eeb17-747">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="eeb17-747">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="eeb17-748">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="eeb17-748">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="eeb17-749">Lägg till stöd för annullering och förloppsspårning för Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="eeb17-749">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="eeb17-750">Lägg till stöd för annullering för Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="eeb17-750">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="eeb17-751">Åtgärda tömning av felsökningsmeddelanden för cmdletar som gör rekursiva åtgärder</span><span class="sxs-lookup"><span data-stu-id="eeb17-751">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="eeb17-752">Åtgärda platsen för testning av DataLake-cmdletar</span><span class="sxs-lookup"><span data-stu-id="eeb17-752">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="eeb17-753">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="eeb17-753">AzureRM.EventHub</span></span>
* <span data-ttu-id="eeb17-754">Parametrar för optimalt maxantal har lagts till i liståtgärds-cmdletarna Get-AzureRmEventHub och Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="eeb17-754">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="eeb17-755">Ett problem i New-AzureRmEventHub-cmdleten har åtgärdats där minst en parameter behövdes när du skapade en ny EventHub.</span><span class="sxs-lookup"><span data-stu-id="eeb17-755">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="eeb17-756">Angiven standardparameter har ställts in.</span><span class="sxs-lookup"><span data-stu-id="eeb17-756">Provided Default Parameter set.</span></span>
* <span data-ttu-id="eeb17-757">Valfri parameter för KeyValue har lagts till för New-AzureRmEventHubKey-cmdleten, vilket gör det möjligt att ange KeyValue.</span><span class="sxs-lookup"><span data-stu-id="eeb17-757">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="eeb17-758">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="eeb17-758">AzureRM.KeyVault</span></span>
* <span data-ttu-id="eeb17-759">Åtgärda problem där alla resurser returnerades av Get-AzureRmKeyVault-taggen</span><span class="sxs-lookup"><span data-stu-id="eeb17-759">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="eeb17-760">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="eeb17-760">AzureRM.Network</span></span>
* <span data-ttu-id="eeb17-761">Gör nya SKU:er tillgängliga för zonredundanta VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="eeb17-761">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="eeb17-762">Nya kommandon har lagts till för funktionen: ExpressRoute Partner API:er via ARM</span><span class="sxs-lookup"><span data-stu-id="eeb17-762">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="eeb17-763">Get-AzureRmExpressRouteCrossConnection har lagts till</span><span class="sxs-lookup"><span data-stu-id="eeb17-763">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="eeb17-764">Set-AzureRmExpressRouteCrossConnection har lagts till</span><span class="sxs-lookup"><span data-stu-id="eeb17-764">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="eeb17-765">Add-AzureRmExpressRouteCrossConnectionPeering har lagts till</span><span class="sxs-lookup"><span data-stu-id="eeb17-765">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="eeb17-766">Get-AzureRmExpressRouteCrossConnectionPeering har lagts till</span><span class="sxs-lookup"><span data-stu-id="eeb17-766">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="eeb17-767">Remove-AzureRmExpressRouteCrossConnectionPeering har lagts till</span><span class="sxs-lookup"><span data-stu-id="eeb17-767">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="eeb17-768">Get-AzureRMExpressRouteCrossConnectionArpTable har lagts till</span><span class="sxs-lookup"><span data-stu-id="eeb17-768">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="eeb17-769">Get-AzureRMExpressRouteCrossConnectionRouteTable har lagts till</span><span class="sxs-lookup"><span data-stu-id="eeb17-769">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="eeb17-770">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary har lagts till</span><span class="sxs-lookup"><span data-stu-id="eeb17-770">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="eeb17-771">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="eeb17-771">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="eeb17-772">Get-AzureRmRecoveryServicesBackupStatus-cmdlet har lagts till.</span><span class="sxs-lookup"><span data-stu-id="eeb17-772">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="eeb17-773">Denna cmdlet tar ett ID för virtuell dator och kontrollerar om den virtuella datorn skyddas av ett valv i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="eeb17-773">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="eeb17-774">Om ett sådant valv finns returnerar cmdleten valvinformationen.</span><span class="sxs-lookup"><span data-stu-id="eeb17-774">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="eeb17-775">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="eeb17-775">AzureRM.Resources</span></span>
* <span data-ttu-id="eeb17-776">Uppdatera Get-AzureRmPolicyAssignment-cmdletar:</span><span class="sxs-lookup"><span data-stu-id="eeb17-776">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="eeb17-777">Lägg till stöd för att lista -Scope-värden på hanteringsgruppsnivå</span><span class="sxs-lookup"><span data-stu-id="eeb17-777">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="eeb17-778">Lägg till stöd för hämtning av enskilda tilldelningar med -Scope-värden på hanteringsgruppsnivå.</span><span class="sxs-lookup"><span data-stu-id="eeb17-778">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="eeb17-779">Lägg till växlar för -Effective och -All till kontrollparametrar</span><span class="sxs-lookup"><span data-stu-id="eeb17-779">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="eeb17-780">Uppdatera Get/New/Remove/Set-AzureRmPolicyDefinition-cmdletar</span><span class="sxs-lookup"><span data-stu-id="eeb17-780">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="eeb17-781">Lägg till parameter för -ManagementGroupName om du vill tillämpa åtgärder för en viss hanteringsgrupp</span><span class="sxs-lookup"><span data-stu-id="eeb17-781">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="eeb17-782">Lägg till parameter för -SubscriptionId om du vill tillämpa åtgärder för en viss prenumeration</span><span class="sxs-lookup"><span data-stu-id="eeb17-782">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="eeb17-783">Uppdatera Get/New/Remove/Set-AzureRmPolicySetDefinition-cmdletar</span><span class="sxs-lookup"><span data-stu-id="eeb17-783">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="eeb17-784">Lägg till parameter för -ManagementGroupName om du vill tillämpa åtgärder för en viss hanteringsgrupp</span><span class="sxs-lookup"><span data-stu-id="eeb17-784">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="eeb17-785">Lägg till parameter för -SubscriptionId om du vill tillämpa åtgärder för en viss prenumeration</span><span class="sxs-lookup"><span data-stu-id="eeb17-785">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="eeb17-786">Lägg till stöd för hemliga KeyVault-referenser i parametrar när du använder "TemplateParameterObject" i "New-AzureRmResourceGroupDeployment"</span><span class="sxs-lookup"><span data-stu-id="eeb17-786">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="eeb17-787">Åtgärda problem med att "-EndDate"-parametern ignorerades på grund av "New-AzureRmADAppCredential"</span><span class="sxs-lookup"><span data-stu-id="eeb17-787">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="eeb17-788">Åtgärda problem med att felaktig URL användes i "New-AzureRmADAppCredential" vid begäran</span><span class="sxs-lookup"><span data-stu-id="eeb17-788">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="eeb17-789">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="eeb17-789">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="eeb17-790">Valfri parameter för -KeyValue har lagts till för New-AzureRmServiceBusKey-cmdleten, vilket gör det möjligt att ange KeyValue.</span><span class="sxs-lookup"><span data-stu-id="eeb17-790">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="eeb17-791">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="eeb17-791">AzureRM.Sql</span></span>
* <span data-ttu-id="eeb17-792">Användardefinierade återställningspunkter har klargjorts för SQLDW i New-AzureRmSqlDatabaseRestorePoint-hjälpen</span><span class="sxs-lookup"><span data-stu-id="eeb17-792">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="eeb17-793">Dokumentationen om parametern -ComputeGeneration har uppdaterats i fler cmdletar</span><span class="sxs-lookup"><span data-stu-id="eeb17-793">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="eeb17-794">6.3.0 – juni 2018</span><span class="sxs-lookup"><span data-stu-id="eeb17-794">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="eeb17-795">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="eeb17-795">AzureRM.Profile</span></span>
* <span data-ttu-id="eeb17-796">Uppdaterade felmeddelanden för Enable-AzureRmContextAutoSave</span><span class="sxs-lookup"><span data-stu-id="eeb17-796">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="eeb17-797">Skapa en kontext för varje prenumeration när du kör ”Connect-AzureRmAccount” utan tidigare kontext</span><span class="sxs-lookup"><span data-stu-id="eeb17-797">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="eeb17-798">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="eeb17-798">Azure.Storage</span></span>
* <span data-ttu-id="eeb17-799">Ytterligare information om parametern -Permissions har lagts till i hjälpfilerna.</span><span class="sxs-lookup"><span data-stu-id="eeb17-799">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="eeb17-800">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="eeb17-800">AzureRM.Compute</span></span>
* <span data-ttu-id="eeb17-801">”Get-AzureRmVmDiskEncryptionStatus” korrigerar ett problem för virtuella datorer utan datadiskar</span><span class="sxs-lookup"><span data-stu-id="eeb17-801">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span>
* <span data-ttu-id="eeb17-802">Uppdatera version av klientbibliotek för Compute för att korrigera följande cmdletar</span><span class="sxs-lookup"><span data-stu-id="eeb17-802">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="eeb17-803">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="eeb17-803">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="eeb17-804">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="eeb17-804">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="eeb17-805">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="eeb17-805">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="eeb17-806">Följande cmdletar har åtgärdats för att visa ”Åtgärds-ID” och ”Åtgärdsstatus” på ett korrekt sätt:</span><span class="sxs-lookup"><span data-stu-id="eeb17-806">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="eeb17-807">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="eeb17-807">Start-AzureRmVM</span></span>
    - <span data-ttu-id="eeb17-808">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="eeb17-808">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="eeb17-809">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="eeb17-809">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="eeb17-810">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="eeb17-810">Set-AzureRmVM</span></span>
    - <span data-ttu-id="eeb17-811">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="eeb17-811">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="eeb17-812">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="eeb17-812">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="eeb17-813">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="eeb17-813">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="eeb17-814">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="eeb17-814">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="eeb17-815">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="eeb17-815">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="eeb17-816">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="eeb17-816">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="eeb17-817">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="eeb17-817">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="eeb17-818">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="eeb17-818">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="eeb17-819">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="eeb17-819">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="eeb17-820">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="eeb17-820">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="eeb17-821">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="eeb17-821">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="eeb17-822">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="eeb17-822">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="eeb17-823">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="eeb17-823">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="eeb17-824">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="eeb17-824">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="eeb17-825">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="eeb17-825">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="eeb17-826">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="eeb17-826">AzureRM.EventGrid</span></span>
* <span data-ttu-id="eeb17-827">Ta bort verifieringsvillkoren ValidateNotNullOrEmpty för SubjectBeginsWith/SubjectEndsWith i cmdleten Update-AzureRmEventGridSubscription för att ändra de här parametrarna till en tom sträng om det behövs.</span><span class="sxs-lookup"><span data-stu-id="eeb17-827">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="eeb17-828">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="eeb17-828">AzureRM.KeyVault</span></span>
* <span data-ttu-id="eeb17-829">Åtgärda problem där inga taggar returneras när Get-AzureRmKeyVault -Tag körs</span><span class="sxs-lookup"><span data-stu-id="eeb17-829">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="eeb17-830">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="eeb17-830">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="eeb17-831">Offentlig lansering av cmdletar för Policy Insights</span><span class="sxs-lookup"><span data-stu-id="eeb17-831">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="eeb17-832">Använd API-version 2018-04-04</span><span class="sxs-lookup"><span data-stu-id="eeb17-832">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="eeb17-833">Lägg till PolicyDefinitionReferenceId i resultaten för Get-AzureRmPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="eeb17-833">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="eeb17-834">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="eeb17-834">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="eeb17-835">Parametern -Vault har lagts till i cmdletarna för RecoveryServices.Backup.</span><span class="sxs-lookup"><span data-stu-id="eeb17-835">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="eeb17-836">När den godkänns åsidosätts cmdleten Set-AzureRmRecoveryServicesContext.</span><span class="sxs-lookup"><span data-stu-id="eeb17-836">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="eeb17-837">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="eeb17-837">AzureRM.Sql</span></span>
* <span data-ttu-id="eeb17-838">Exemplet i hjälpfilen för Get-AzureRmSqlDatabaseExpanded har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="eeb17-838">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="eeb17-839">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="eeb17-839">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="eeb17-840">Hjälpfilen för Add-AzureRmTrafficManagerEndpointConfig har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="eeb17-840">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="eeb17-841">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="eeb17-841">AzureRM.Websites</span></span>
* <span data-ttu-id="eeb17-842">”Set-AzureRmWebApp” har uppdaterats så att den inte skriver över appinställningarna när du använder -AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="eeb17-842">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="eeb17-843">”New-AzureRMWebAppSlot” har uppdaterats för att visa att AppServicePlan är en valfri parameter</span><span class="sxs-lookup"><span data-stu-id="eeb17-843">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="eeb17-844">6.2.1 – juni 2018</span><span class="sxs-lookup"><span data-stu-id="eeb17-844">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="eeb17-845">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="eeb17-845">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="eeb17-846">PSWorkspace-modellen har uppdaterats för att tillåta att nätverket använder typ som en parameter</span><span class="sxs-lookup"><span data-stu-id="eeb17-846">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="eeb17-847">6.2.0 – juni 2018</span><span class="sxs-lookup"><span data-stu-id="eeb17-847">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="eeb17-848">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="eeb17-848">AzureRM.Profile</span></span>
* <span data-ttu-id="eeb17-849">Åtgärda problemet med att version 10.0.3 av Newtonsoft.Json inte lästes in vid modulimporten</span><span class="sxs-lookup"><span data-stu-id="eeb17-849">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="eeb17-850">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="eeb17-850">AzureRM.Compute</span></span>
* <span data-ttu-id="eeb17-851">VMSS VM-uppdateringsfunktion</span><span class="sxs-lookup"><span data-stu-id="eeb17-851">VMSS VM Update feature</span></span>
    - <span data-ttu-id="eeb17-852">Cmdletarna Update-AzureRmVmssVM och New-AzureRmVMDataDisk har lagts till</span><span class="sxs-lookup"><span data-stu-id="eeb17-852">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="eeb17-853">Lägg till parametern VirtualMachineScaleSetVM till cmdleten Add-AzureRmVMDataDisk så att det går att lägga till en datadisk i den virtuella Vmss-datorn.</span><span class="sxs-lookup"><span data-stu-id="eeb17-853">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="eeb17-854">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="eeb17-854">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="eeb17-855">SDK:n för ADF .Net har uppdaterats till version 0.8.0-preview som innehåller följande ändringar:</span><span class="sxs-lookup"><span data-stu-id="eeb17-855">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="eeb17-856">Åtgärden för att konfigurera fabrikslagringsplatsen har lagts till</span><span class="sxs-lookup"><span data-stu-id="eeb17-856">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="eeb17-857">QuickBooks LinkedService har uppdaterats för att visa egenskaperna consumerKey och consumerSecret</span><span class="sxs-lookup"><span data-stu-id="eeb17-857">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="eeb17-858">Flera modelltyper från SecretBase till Object har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="eeb17-858">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="eeb17-859">Utlösaren Blob Events har lagts till</span><span class="sxs-lookup"><span data-stu-id="eeb17-859">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="eeb17-860">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="eeb17-860">AzureRM.KeyVault</span></span>
* <span data-ttu-id="eeb17-861">Uppdatera dokumentation med exempel på utdata</span><span class="sxs-lookup"><span data-stu-id="eeb17-861">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="eeb17-862">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="eeb17-862">AzureRM.Network</span></span>
* <span data-ttu-id="eeb17-863">Aktivera Trafikanalys-parametrar på Network Watcher-cmdletar</span><span class="sxs-lookup"><span data-stu-id="eeb17-863">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="eeb17-864">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="eeb17-864">AzureRM.Resources</span></span>
* <span data-ttu-id="eeb17-865">Åtgärda problemet med egenskapen "Properties" för objekt(en) "PSResource" som returneras från "Get-AzureRmResource"</span><span class="sxs-lookup"><span data-stu-id="eeb17-865">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="eeb17-866">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="eeb17-866">AzureRM.Scheduler</span></span>
* <span data-ttu-id="eeb17-867">Åtgärda problemet med att nya autentiseringsvärden inte anges vid uppdatering av ServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="eeb17-867">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="eeb17-868">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="eeb17-868">AzureRM.Sql</span></span>
* <span data-ttu-id="eeb17-869">Följande cmdletar har uppdaterats med valfri LicenseType-parameter</span><span class="sxs-lookup"><span data-stu-id="eeb17-869">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="eeb17-870">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="eeb17-870">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="eeb17-871">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="eeb17-871">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="eeb17-872">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="eeb17-872">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="eeb17-873">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="eeb17-873">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="eeb17-874">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="eeb17-874">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="eeb17-875">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="eeb17-875">AzureRM.Websites</span></span>
* <span data-ttu-id="eeb17-876">New-AzureRMWebApp har uppdaterats för att använda vanliga algoritmer från biblioteket Strategy.</span><span class="sxs-lookup"><span data-stu-id="eeb17-876">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="eeb17-877">6.1.0 – maj 2018</span><span class="sxs-lookup"><span data-stu-id="eeb17-877">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="eeb17-878">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="eeb17-878">AzureRM.Profile</span></span>
* <span data-ttu-id="eeb17-879">Åtgärda problem där en körning av Clear-AzureRmContext skulle bevara en tom kontext med namnet på den föregående standardkontexten som gjorde att användaren inte kunde skapa en ny kontext med det gamla namnet</span><span class="sxs-lookup"><span data-stu-id="eeb17-879">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="eeb17-880">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="eeb17-880">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="eeb17-881">Aktivera Gateway associerings- och avassocieringsåtgärder på AS.</span><span class="sxs-lookup"><span data-stu-id="eeb17-881">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="eeb17-882">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="eeb17-882">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="eeb17-883">Stöd för ApiVersions, ApiReleases och ApiRevisions har lagts till</span><span class="sxs-lookup"><span data-stu-id="eeb17-883">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="eeb17-884">Stöd för serverdelen på ServiceFabric har lagts till</span><span class="sxs-lookup"><span data-stu-id="eeb17-884">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="eeb17-885">Stöd för Application Insights-loggare har lagts till</span><span class="sxs-lookup"><span data-stu-id="eeb17-885">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="eeb17-886">Stöd för att identifiera SKU:n ”Basic” som en giltig SKU för Api Management-tjänsten har lagts till</span><span class="sxs-lookup"><span data-stu-id="eeb17-886">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="eeb17-887">Stöd för att installera certifikat som utfärdats av privata certifikatutfärdare som rot eller certifikatutfärdare har lagts till</span><span class="sxs-lookup"><span data-stu-id="eeb17-887">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="eeb17-888">Stöd för att godkänna anpassade SSL-certifikat via KeyVault och flera proxy-värdnamn har lagts till</span><span class="sxs-lookup"><span data-stu-id="eeb17-888">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="eeb17-889">Stöd för MSI-identitet har lagts till</span><span class="sxs-lookup"><span data-stu-id="eeb17-889">Added support for MSI identity</span></span>
* <span data-ttu-id="eeb17-890">Stöd för att godkänna principer via URL har lagts till. Obs! Följande cmdletar blir inaktuella i framtida versioner</span><span class="sxs-lookup"><span data-stu-id="eeb17-890">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="eeb17-891">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="eeb17-891">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="eeb17-892">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="eeb17-892">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="eeb17-893">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="eeb17-893">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="eeb17-894">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="eeb17-894">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="eeb17-895">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="eeb17-895">AzureRM.Batch</span></span>
* <span data-ttu-id="eeb17-896">Släpp nya cmdleten Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="eeb17-896">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="eeb17-897">Släpp nya cmdleten Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="eeb17-897">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="eeb17-898">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="eeb17-898">AzureRM.Consumption</span></span>
* <span data-ttu-id="eeb17-899">Lägg till nya parametrar Expand, ResourceGroup, InstanceName, InstanceId, Tags och Top på cmdleten Get-AzureRmConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="eeb17-899">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="eeb17-900">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="eeb17-900">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="eeb17-901">Åtgärda exempel för Export AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="eeb17-901">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="eeb17-902">Åtgärda undantag för null-parameter för rekursivt ärende i Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="eeb17-902">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span>
* <span data-ttu-id="eeb17-903">Åtgärda hjälpfilerna för Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="eeb17-903">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="eeb17-904">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="eeb17-904">AzureRM.Network</span></span>
* <span data-ttu-id="eeb17-905">Öka nätverkets SDK-version från förhandsversionen 18.0.0 till förhandsversionen 19.0.0</span><span class="sxs-lookup"><span data-stu-id="eeb17-905">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="eeb17-906">Cmdlet har lagts till för att skapa protokollinformation</span><span class="sxs-lookup"><span data-stu-id="eeb17-906">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="eeb17-907">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="eeb17-907">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="eeb17-908">Cmdlet har lagts till för att lägga till en ny kretsanslutning till en befintlig expressroute-krets.</span><span class="sxs-lookup"><span data-stu-id="eeb17-908">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="eeb17-909">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="eeb17-909">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="eeb17-910">Cmdlet har lagts till för att ta bort en kretsanslutning från en befintlig expressroute-krets.</span><span class="sxs-lookup"><span data-stu-id="eeb17-910">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="eeb17-911">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="eeb17-911">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="eeb17-912">Cmdlet har lagts till för att hämta en kretsanslutning</span><span class="sxs-lookup"><span data-stu-id="eeb17-912">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="eeb17-913">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="eeb17-913">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="eeb17-914">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="eeb17-914">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="eeb17-915">Användning med serverautentisering med genererade certifikat (problem #5998) har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="eeb17-915">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="eeb17-916">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="eeb17-916">AzureRM.Sql</span></span>
* <span data-ttu-id="eeb17-917">Cmdletar för granskning för att ta bort AuditActions eller AuditActionGroups har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="eeb17-917">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="eeb17-918">Åtgärdade problem med Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy vid konfigurering av en ny flexibel bevarandeprincip där kommandot misslyckas med ett meddelande om att konfigurering av långsiktig bevarandeprincip med Azure Recovery Service-valv och principen inte längre stöds,</span><span class="sxs-lookup"><span data-stu-id="eeb17-918">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="eeb17-919">och att en begäran med den nya flexibla bevarandeprincipen ska skickas.</span><span class="sxs-lookup"><span data-stu-id="eeb17-919">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="eeb17-920">Uppdatera alla Azure Sql Database/ElasticPool Creation/Update-relaterade cmdletar för att använda det nya databas-API:et som stöder SKU-egenskaper för skalnings- och nivårelaterade egenskaper.</span><span class="sxs-lookup"><span data-stu-id="eeb17-920">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="eeb17-921">Cmdletar har uppdaterats, inklusive:</span><span class="sxs-lookup"><span data-stu-id="eeb17-921">The updated cmdlets including:</span></span>
    - <span data-ttu-id="eeb17-922">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="eeb17-922">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="eeb17-923">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="eeb17-923">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="eeb17-924">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="eeb17-924">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="eeb17-925">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="eeb17-925">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="eeb17-926">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="eeb17-926">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="eeb17-927">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="eeb17-927">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="eeb17-928">Uppdatera parametrarna för Get-AzureRmTrafficManagerProfile så att ResourceGroupName-parametern blir obligatorisk när du använder Name-parametern.</span><span class="sxs-lookup"><span data-stu-id="eeb17-928">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
