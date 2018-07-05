---
title: Ändringslogg för Azure PowerShell | Microsoft Docs
description: Det här är en historik över de ändringar som gjorts i den senaste versionen av Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 5/1/2018
ms.openlocfilehash: 3811e28dda69d194d23934943fb47d562f869fc4
ms.sourcegitcommit: 5a5b6dd216d5f805204244146cf6f88ad2f34fb4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/19/2018
ms.locfileid: "36238070"
---
# <a name="release-notes"></a><span data-ttu-id="2c774-103">Viktig information</span><span class="sxs-lookup"><span data-stu-id="2c774-103">Release notes</span></span>

<span data-ttu-id="2c774-104">Det här är en lista över ändringar som har gjorts i Azure PowerShell i den här versionen.</span><span class="sxs-lookup"><span data-stu-id="2c774-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="630---june-2018"></a><span data-ttu-id="2c774-105">6.3.0 – juni 2018</span><span class="sxs-lookup"><span data-stu-id="2c774-105">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="2c774-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="2c774-106">AzureRM.Profile</span></span>
* <span data-ttu-id="2c774-107">Uppdaterade felmeddelanden för Enable-AzureRmContextAutoSave</span><span class="sxs-lookup"><span data-stu-id="2c774-107">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="2c774-108">Skapa en kontext för varje prenumeration när du kör ”Connect-AzureRmAccount” utan tidigare kontext</span><span class="sxs-lookup"><span data-stu-id="2c774-108">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="2c774-109">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="2c774-109">Azure.Storage</span></span>
* <span data-ttu-id="2c774-110">Ytterligare information om parametern -Permissions har lagts till i hjälpfilerna.</span><span class="sxs-lookup"><span data-stu-id="2c774-110">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="2c774-111">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="2c774-111">AzureRM.Compute</span></span>
* <span data-ttu-id="2c774-112">”Get-AzureRmVmDiskEncryptionStatus” korrigerar ett problem för virtuella datorer utan datadiskar</span><span class="sxs-lookup"><span data-stu-id="2c774-112">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="2c774-113">Uppdatera version av klientbibliotek för Compute för att korrigera följande cmdletar</span><span class="sxs-lookup"><span data-stu-id="2c774-113">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="2c774-114">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="2c774-114">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="2c774-115">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="2c774-115">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="2c774-116">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="2c774-116">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="2c774-117">Följande cmdletar har åtgärdats för att visa ”Åtgärds-ID” och ”Åtgärdsstatus” på ett korrekt sätt:</span><span class="sxs-lookup"><span data-stu-id="2c774-117">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="2c774-118">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="2c774-118">Start-AzureRmVM</span></span>
    - <span data-ttu-id="2c774-119">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="2c774-119">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="2c774-120">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="2c774-120">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="2c774-121">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="2c774-121">Set-AzureRmVM</span></span>
    - <span data-ttu-id="2c774-122">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="2c774-122">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="2c774-123">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="2c774-123">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="2c774-124">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="2c774-124">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="2c774-125">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="2c774-125">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="2c774-126">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="2c774-126">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="2c774-127">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="2c774-127">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="2c774-128">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="2c774-128">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="2c774-129">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="2c774-129">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="2c774-130">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="2c774-130">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="2c774-131">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="2c774-131">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="2c774-132">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="2c774-132">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="2c774-133">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="2c774-133">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="2c774-134">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="2c774-134">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="2c774-135">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="2c774-135">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="2c774-136">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="2c774-136">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="2c774-137">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="2c774-137">AzureRM.EventGrid</span></span>
* <span data-ttu-id="2c774-138">Ta bort verifieringsvillkoren ValidateNotNullOrEmpty för SubjectBeginsWith/SubjectEndsWith i cmdleten Update-AzureRmEventGridSubscription för att ändra de här parametrarna till en tom sträng om det behövs.</span><span class="sxs-lookup"><span data-stu-id="2c774-138">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="2c774-139">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2c774-139">AzureRM.KeyVault</span></span>
* <span data-ttu-id="2c774-140">Åtgärda problem där inga taggar returneras när Get-AzureRmKeyVault -Tag körs</span><span class="sxs-lookup"><span data-stu-id="2c774-140">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="2c774-141">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="2c774-141">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="2c774-142">Offentlig lansering av cmdletar för Policy Insights</span><span class="sxs-lookup"><span data-stu-id="2c774-142">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="2c774-143">Använd API-version 2018-04-04</span><span class="sxs-lookup"><span data-stu-id="2c774-143">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="2c774-144">Lägg till PolicyDefinitionReferenceId i resultaten för Get-AzureRmPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="2c774-144">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="2c774-145">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2c774-145">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="2c774-146">Parametern -Vault har lagts till i cmdletarna för RecoveryServices.Backup.</span><span class="sxs-lookup"><span data-stu-id="2c774-146">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="2c774-147">När den godkänns åsidosätts cmdleten Set-AzureRmRecoveryServicesContext.</span><span class="sxs-lookup"><span data-stu-id="2c774-147">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="2c774-148">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="2c774-148">AzureRM.Sql</span></span>
* <span data-ttu-id="2c774-149">Exemplet i hjälpfilen för Get-AzureRmSqlDatabaseExpanded har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="2c774-149">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="2c774-150">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="2c774-150">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="2c774-151">Hjälpfilen för Add-AzureRmTrafficManagerEndpointConfig har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="2c774-151">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="2c774-152">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="2c774-152">AzureRM.Websites</span></span>
* <span data-ttu-id="2c774-153">”Set-AzureRmWebApp” har uppdaterats så att den inte skriver över appinställningarna när du använder -AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="2c774-153">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="2c774-154">”New-AzureRMWebAppSlot” har uppdaterats för att visa att AppServicePlan är en valfri parameter</span><span class="sxs-lookup"><span data-stu-id="2c774-154">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="2c774-155">6.2.1 – juni 2018</span><span class="sxs-lookup"><span data-stu-id="2c774-155">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="2c774-156">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2c774-156">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="2c774-157">PSWorkspace-modellen har uppdaterats för att tillåta att nätverket använder typ som en parameter</span><span class="sxs-lookup"><span data-stu-id="2c774-157">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="2c774-158">6.2.0 – juni 2018</span><span class="sxs-lookup"><span data-stu-id="2c774-158">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="2c774-159">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="2c774-159">AzureRM.Profile</span></span>
* <span data-ttu-id="2c774-160">Åtgärda problemet med att version 10.0.3 av Newtonsoft.Json inte lästes in vid modulimporten</span><span class="sxs-lookup"><span data-stu-id="2c774-160">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="2c774-161">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="2c774-161">AzureRM.Compute</span></span>
* <span data-ttu-id="2c774-162">VMSS VM-uppdateringsfunktion</span><span class="sxs-lookup"><span data-stu-id="2c774-162">VMSS VM Update feature</span></span>
    - <span data-ttu-id="2c774-163">Cmdletarna Update-AzureRmVmssVM och New-AzureRmVMDataDisk har lagts till</span><span class="sxs-lookup"><span data-stu-id="2c774-163">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="2c774-164">Lägg till parametern VirtualMachineScaleSetVM till cmdleten Add-AzureRmVMDataDisk så att det går att lägga till en datadisk i den virtuella Vmss-datorn.</span><span class="sxs-lookup"><span data-stu-id="2c774-164">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="2c774-165">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="2c774-165">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="2c774-166">SDK:n för ADF .Net har uppdaterats till version 0.8.0-preview som innehåller följande ändringar:</span><span class="sxs-lookup"><span data-stu-id="2c774-166">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="2c774-167">Åtgärden för att konfigurera fabrikslagringsplatsen har lagts till</span><span class="sxs-lookup"><span data-stu-id="2c774-167">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="2c774-168">QuickBooks LinkedService har uppdaterats för att visa egenskaperna consumerKey och consumerSecret</span><span class="sxs-lookup"><span data-stu-id="2c774-168">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="2c774-169">Flera modelltyper från SecretBase till Object har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="2c774-169">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="2c774-170">Utlösaren Blob Events har lagts till</span><span class="sxs-lookup"><span data-stu-id="2c774-170">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="2c774-171">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2c774-171">AzureRM.KeyVault</span></span>
* <span data-ttu-id="2c774-172">Uppdatera dokumentation med exempel på utdata</span><span class="sxs-lookup"><span data-stu-id="2c774-172">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="2c774-173">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="2c774-173">AzureRM.Network</span></span>
* <span data-ttu-id="2c774-174">Aktivera Trafikanalys-parametrar på Network Watcher-cmdletar</span><span class="sxs-lookup"><span data-stu-id="2c774-174">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="2c774-175">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="2c774-175">AzureRM.Resources</span></span>
* <span data-ttu-id="2c774-176">Åtgärda problemet med egenskapen "Properties" för objekt(en) "PSResource" som returneras från "Get-AzureRmResource"</span><span class="sxs-lookup"><span data-stu-id="2c774-176">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="2c774-177">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="2c774-177">AzureRM.Scheduler</span></span>
* <span data-ttu-id="2c774-178">Åtgärda problemet med att nya autentiseringsvärden inte anges vid uppdatering av ServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="2c774-178">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="2c774-179">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="2c774-179">AzureRM.Sql</span></span>
* <span data-ttu-id="2c774-180">Följande cmdletar har uppdaterats med valfri LicenseType-parameter</span><span class="sxs-lookup"><span data-stu-id="2c774-180">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="2c774-181">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="2c774-181">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="2c774-182">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="2c774-182">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="2c774-183">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="2c774-183">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="2c774-184">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="2c774-184">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="2c774-185">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="2c774-185">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="2c774-186">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="2c774-186">AzureRM.Websites</span></span>
* <span data-ttu-id="2c774-187">New-AzureRMWebApp har uppdaterats för att använda vanliga algoritmer från biblioteket Strategy.</span><span class="sxs-lookup"><span data-stu-id="2c774-187">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="2c774-188">6.1.0 – maj 2018</span><span class="sxs-lookup"><span data-stu-id="2c774-188">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="2c774-189">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="2c774-189">AzureRM.Profile</span></span>
* <span data-ttu-id="2c774-190">Åtgärda problem där en körning av Clear-AzureRmContext skulle bevara en tom kontext med namnet på den föregående standardkontexten som gjorde att användaren inte kunde skapa en ny kontext med det gamla namnet</span><span class="sxs-lookup"><span data-stu-id="2c774-190">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="2c774-191">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="2c774-191">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="2c774-192">Aktivera Gateway associerings- och avassocieringsåtgärder på AS.</span><span class="sxs-lookup"><span data-stu-id="2c774-192">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="2c774-193">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2c774-193">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="2c774-194">Stöd för ApiVersions, ApiReleases och ApiRevisions har lagts till</span><span class="sxs-lookup"><span data-stu-id="2c774-194">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="2c774-195">Stöd för serverdelen på ServiceFabric har lagts till</span><span class="sxs-lookup"><span data-stu-id="2c774-195">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="2c774-196">Stöd för Application Insights-loggare har lagts till</span><span class="sxs-lookup"><span data-stu-id="2c774-196">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="2c774-197">Stöd för att identifiera SKU:n ”Basic” som en giltig SKU för Api Management-tjänsten har lagts till</span><span class="sxs-lookup"><span data-stu-id="2c774-197">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="2c774-198">Stöd för att installera certifikat som utfärdats av privata certifikatutfärdare som rot eller certifikatutfärdare har lagts till</span><span class="sxs-lookup"><span data-stu-id="2c774-198">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="2c774-199">Stöd för att godkänna anpassade SSL-certifikat via KeyVault och flera proxy-värdnamn har lagts till</span><span class="sxs-lookup"><span data-stu-id="2c774-199">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="2c774-200">Stöd för MSI-identitet har lagts till</span><span class="sxs-lookup"><span data-stu-id="2c774-200">Added support for MSI identity</span></span>
* <span data-ttu-id="2c774-201">Stöd för att godkänna principer via URL har lagts till. Obs! Följande cmdletar blir inaktuella i framtida versioner</span><span class="sxs-lookup"><span data-stu-id="2c774-201">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="2c774-202">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="2c774-202">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="2c774-203">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="2c774-203">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="2c774-204">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="2c774-204">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="2c774-205">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="2c774-205">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="2c774-206">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="2c774-206">AzureRM.Batch</span></span>
* <span data-ttu-id="2c774-207">Släpp nya cmdleten Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="2c774-207">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="2c774-208">Släpp nya cmdleten Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="2c774-208">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="2c774-209">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="2c774-209">AzureRM.Consumption</span></span>
* <span data-ttu-id="2c774-210">Lägg till nya parametrar Expand, ResourceGroup, InstanceName, InstanceId, Tags och Top på cmdleten Get-AzureRmConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="2c774-210">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="2c774-211">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2c774-211">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="2c774-212">Åtgärda exempel för Export AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="2c774-212">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="2c774-213">Åtgärda undantag för null-parameter för rekursivt ärende i Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="2c774-213">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="2c774-214">Åtgärda hjälpfilerna för Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="2c774-214">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="2c774-215">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="2c774-215">AzureRM.Network</span></span>
* <span data-ttu-id="2c774-216">Öka nätverkets SDK-version från förhandsversionen 18.0.0 till förhandsversionen 19.0.0</span><span class="sxs-lookup"><span data-stu-id="2c774-216">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="2c774-217">Cmdlet har lagts till för att skapa protokollinformation</span><span class="sxs-lookup"><span data-stu-id="2c774-217">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="2c774-218">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="2c774-218">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="2c774-219">Cmdlet har lagts till för att lägga till en ny kretsanslutning till en befintlig expressroute-krets.</span><span class="sxs-lookup"><span data-stu-id="2c774-219">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="2c774-220">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="2c774-220">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="2c774-221">Cmdlet har lagts till för att ta bort en kretsanslutning från en befintlig expressroute-krets.</span><span class="sxs-lookup"><span data-stu-id="2c774-221">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="2c774-222">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="2c774-222">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="2c774-223">Cmdlet har lagts till för att hämta en kretsanslutning</span><span class="sxs-lookup"><span data-stu-id="2c774-223">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="2c774-224">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="2c774-224">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="2c774-225">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2c774-225">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="2c774-226">Användning med serverautentisering med genererade certifikat (problem #5998) har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="2c774-226">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="2c774-227">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="2c774-227">AzureRM.Sql</span></span>
* <span data-ttu-id="2c774-228">Cmdletar för granskning för att ta bort AuditActions eller AuditActionGroups har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="2c774-228">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="2c774-229">Åtgärdade problem med Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy vid konfigurering av en ny flexibel bevarandeprincip där kommandot misslyckas med ett meddelande om att konfigurering av långsiktig bevarandeprincip med Azure Recovery Service-valv och principen inte längre stöds,</span><span class="sxs-lookup"><span data-stu-id="2c774-229">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="2c774-230">och att en begäran med den nya flexibla bevarandeprincipen ska skickas.</span><span class="sxs-lookup"><span data-stu-id="2c774-230">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="2c774-231">Uppdatera alla Azure Sql Database/ElasticPool Creation/Update-relaterade cmdletar för att använda det nya databas-API:et som stöder SKU-egenskaper för skalnings- och nivårelaterade egenskaper.</span><span class="sxs-lookup"><span data-stu-id="2c774-231">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="2c774-232">Cmdletar har uppdaterats, inklusive:</span><span class="sxs-lookup"><span data-stu-id="2c774-232">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="2c774-233">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="2c774-233">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="2c774-234">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="2c774-234">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="2c774-235">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="2c774-235">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="2c774-236">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="2c774-236">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="2c774-237">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="2c774-237">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="2c774-238">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="2c774-238">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="2c774-239">Uppdatera parametrarna för Get-AzureRmTrafficManagerProfile så att ResourceGroupName-parametern blir obligatorisk när du använder Name-parametern.</span><span class="sxs-lookup"><span data-stu-id="2c774-239">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>