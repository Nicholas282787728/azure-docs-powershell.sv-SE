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
ms.openlocfilehash: 255e26aea5ea3cea866faa0d095cdf643c8ef0a8
ms.sourcegitcommit: de0e60800df1add9f3400166faacca202ef567d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/03/2018
ms.locfileid: "37406672"
---
# <a name="release-notes"></a><span data-ttu-id="7a256-103">Viktig information</span><span class="sxs-lookup"><span data-stu-id="7a256-103">Release notes</span></span>

<span data-ttu-id="7a256-104">Det här är en lista över ändringar som har gjorts i Azure PowerShell i den här versionen.</span><span class="sxs-lookup"><span data-stu-id="7a256-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="640---july-2018"></a><span data-ttu-id="7a256-105">6.4.0 – juli 2018</span><span class="sxs-lookup"><span data-stu-id="7a256-105">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="7a256-106">Allmänt</span><span class="sxs-lookup"><span data-stu-id="7a256-106">General</span></span>
* <span data-ttu-id="7a256-107">Formatering av OutputType i hjälpfiler har korrigerats för de flesta moduler</span><span class="sxs-lookup"><span data-stu-id="7a256-107">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="7a256-108">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="7a256-108">AzureRM.Profile</span></span>
* <span data-ttu-id="7a256-109">Ps1Xml-attribut har lagts till för grundläggande utdatatyper</span><span class="sxs-lookup"><span data-stu-id="7a256-109">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="7a256-110">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="7a256-110">AzureRM.Compute</span></span>
* <span data-ttu-id="7a256-111">IP-tagg-funktioner för VMSS</span><span class="sxs-lookup"><span data-stu-id="7a256-111">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="7a256-112">"New-AzureRmVmssIpTagConfig"-cmdlet har lagts till</span><span class="sxs-lookup"><span data-stu-id="7a256-112">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="7a256-113">IpTag-parameter har lagts till för New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="7a256-113">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="7a256-114">Automatisk återställningsfunktion för operativsystem för VMSS</span><span class="sxs-lookup"><span data-stu-id="7a256-114">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="7a256-115">DisableAutoRollback-parametrar har lagts till för New-AzureRmVmssConfig och Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="7a256-115">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="7a256-116">Funktion för uppgraderingshistorik för operativsystem för Vmss</span><span class="sxs-lookup"><span data-stu-id="7a256-116">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="7a256-117">OSUpgradeHistory-växlingsparametern har lagts till för Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="7a256-117">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="7a256-118">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="7a256-118">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="7a256-119">Lägg till stöd för katalog-ACL:er med hjälp av följande kommandon:</span><span class="sxs-lookup"><span data-stu-id="7a256-119">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="7a256-120">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="7a256-120">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="7a256-121">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="7a256-121">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="7a256-122">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="7a256-122">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="7a256-123">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7a256-123">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="7a256-124">Lägg till stöd för annullering och förloppsspårning för Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="7a256-124">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="7a256-125">Lägg till stöd för annullering för Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="7a256-125">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="7a256-126">Åtgärda tömning av felsökningsmeddelanden för cmdletar som gör rekursiva åtgärder</span><span class="sxs-lookup"><span data-stu-id="7a256-126">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="7a256-127">Åtgärda platsen för testning av DataLake-cmdletar</span><span class="sxs-lookup"><span data-stu-id="7a256-127">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="7a256-128">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="7a256-128">AzureRM.EventHub</span></span>
* <span data-ttu-id="7a256-129">Parametrar för optimalt maxantal har lagts till i liståtgärds-cmdletarna Get-AzureRmEventHub och Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="7a256-129">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="7a256-130">Ett problem i New-AzureRmEventHub-cmdleten har åtgärdats där minst en parameter behövdes när du skapade en ny EventHub.</span><span class="sxs-lookup"><span data-stu-id="7a256-130">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="7a256-131">Angiven standardparameter har ställts in.</span><span class="sxs-lookup"><span data-stu-id="7a256-131">Provided Default Parameter set.</span></span>
* <span data-ttu-id="7a256-132">Valfri parameter för KeyValue har lagts till för New-AzureRmEventHubKey-cmdleten, vilket gör det möjligt att ange KeyValue.</span><span class="sxs-lookup"><span data-stu-id="7a256-132">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="7a256-133">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7a256-133">AzureRM.KeyVault</span></span>
* <span data-ttu-id="7a256-134">Åtgärda problem där alla resurser returnerades av Get-AzureRmKeyVault-taggen</span><span class="sxs-lookup"><span data-stu-id="7a256-134">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="7a256-135">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="7a256-135">AzureRM.Network</span></span>
* <span data-ttu-id="7a256-136">Gör nya SKU:er tillgängliga för zonredundanta VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="7a256-136">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="7a256-137">Nya kommandon har lagts till för funktionen: ExpressRoute Partner APIs via ARM</span><span class="sxs-lookup"><span data-stu-id="7a256-137">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="7a256-138">Get-AzureRmExpressRouteCrossConnection har lagts till</span><span class="sxs-lookup"><span data-stu-id="7a256-138">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="7a256-139">Set-AzureRmExpressRouteCrossConnection har lagts till</span><span class="sxs-lookup"><span data-stu-id="7a256-139">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="7a256-140">Add-AzureRmExpressRouteCrossConnectionPeering har lagts till</span><span class="sxs-lookup"><span data-stu-id="7a256-140">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="7a256-141">Get-AzureRmExpressRouteCrossConnectionPeering har lagts till</span><span class="sxs-lookup"><span data-stu-id="7a256-141">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="7a256-142">Remove-AzureRmExpressRouteCrossConnectionPeering har lagts till</span><span class="sxs-lookup"><span data-stu-id="7a256-142">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="7a256-143">Get-AzureRMExpressRouteCrossConnectionArpTable har lagts till</span><span class="sxs-lookup"><span data-stu-id="7a256-143">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="7a256-144">Get-AzureRMExpressRouteCrossConnectionRouteTable har lagts till</span><span class="sxs-lookup"><span data-stu-id="7a256-144">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="7a256-145">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary har lagts till</span><span class="sxs-lookup"><span data-stu-id="7a256-145">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="7a256-146">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7a256-146">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="7a256-147">Get-AzureRmRecoveryServicesBackupStatus-cmdlet har lagts till.</span><span class="sxs-lookup"><span data-stu-id="7a256-147">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="7a256-148">Denna cmdlet tar ett ID för virtuell dator och kontrollerar om den virtuella datorn skyddas av ett valv i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="7a256-148">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="7a256-149">Om ett sådant valv finns returnerar cmdleten valvinformationen.</span><span class="sxs-lookup"><span data-stu-id="7a256-149">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="7a256-150">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="7a256-150">AzureRM.Resources</span></span>
* <span data-ttu-id="7a256-151">Uppdatera Get-AzureRmPolicyAssignment-cmdletar:</span><span class="sxs-lookup"><span data-stu-id="7a256-151">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="7a256-152">Lägg till stöd för att lista -Scope-värden på hanteringsgruppsnivå</span><span class="sxs-lookup"><span data-stu-id="7a256-152">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="7a256-153">Lägg till stöd för hämtning av enskilda tilldelningar med -Scope-värden på hanteringsgruppsnivå.</span><span class="sxs-lookup"><span data-stu-id="7a256-153">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="7a256-154">Lägg till växlar för -Effective och -All till kontrollparametrar</span><span class="sxs-lookup"><span data-stu-id="7a256-154">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="7a256-155">Uppdatera Get/New/Remove/Set-AzureRmPolicyDefinition-cmdletar</span><span class="sxs-lookup"><span data-stu-id="7a256-155">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="7a256-156">Lägg till parameter för -ManagementGroupName om du vill tillämpa åtgärder för en viss hanteringsgrupp</span><span class="sxs-lookup"><span data-stu-id="7a256-156">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="7a256-157">Lägg till parameter för -SubscriptionId om du vill tillämpa åtgärder för en viss prenumeration</span><span class="sxs-lookup"><span data-stu-id="7a256-157">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="7a256-158">Uppdatera Get/New/Remove/Set-AzureRmPolicySetDefinition-cmdletar</span><span class="sxs-lookup"><span data-stu-id="7a256-158">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="7a256-159">Lägg till parameter för -ManagementGroupName om du vill tillämpa åtgärder för en viss hanteringsgrupp</span><span class="sxs-lookup"><span data-stu-id="7a256-159">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="7a256-160">Lägg till parameter för -SubscriptionId om du vill tillämpa åtgärder för en viss prenumeration</span><span class="sxs-lookup"><span data-stu-id="7a256-160">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="7a256-161">Lägg till stöd för hemliga KeyVault-referenser i parametrar när du använder "TemplateParameterObject" i "New-AzureRmResourceGroupDeployment"</span><span class="sxs-lookup"><span data-stu-id="7a256-161">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="7a256-162">Åtgärda problem med att "-EndDate"-parametern ignorerades på grund av "New-AzureRmADAppCredential"</span><span class="sxs-lookup"><span data-stu-id="7a256-162">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="7a256-163">Åtgärda problem med att felaktig URL användes i "New-AzureRmADAppCredential" vid begäran</span><span class="sxs-lookup"><span data-stu-id="7a256-163">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="7a256-164">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="7a256-164">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="7a256-165">Valfri parameter för -KeyValue har lagts till för New-AzureRmServiceBusKey-cmdleten, vilket gör det möjligt att ange KeyValue.</span><span class="sxs-lookup"><span data-stu-id="7a256-165">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="7a256-166">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="7a256-166">AzureRM.Sql</span></span>
* <span data-ttu-id="7a256-167">Användardefinierade återställningspunkter har klargjorts för SQLDW i New-AzureRmSqlDatabaseRestorePoint-hjälpen</span><span class="sxs-lookup"><span data-stu-id="7a256-167">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="7a256-168">Dokumentationen om parametern -ComputeGeneration har uppdaterats i fler cmdletar</span><span class="sxs-lookup"><span data-stu-id="7a256-168">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="7a256-169">6.3.0 – juni 2018</span><span class="sxs-lookup"><span data-stu-id="7a256-169">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="7a256-170">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="7a256-170">AzureRM.Profile</span></span>
* <span data-ttu-id="7a256-171">Uppdaterade felmeddelanden för Enable-AzureRmContextAutoSave</span><span class="sxs-lookup"><span data-stu-id="7a256-171">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="7a256-172">Skapa en kontext för varje prenumeration när du kör ”Connect-AzureRmAccount” utan tidigare kontext</span><span class="sxs-lookup"><span data-stu-id="7a256-172">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="7a256-173">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="7a256-173">Azure.Storage</span></span>
* <span data-ttu-id="7a256-174">Ytterligare information om parametern -Permissions har lagts till i hjälpfilerna.</span><span class="sxs-lookup"><span data-stu-id="7a256-174">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="7a256-175">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="7a256-175">AzureRM.Compute</span></span>
* <span data-ttu-id="7a256-176">”Get-AzureRmVmDiskEncryptionStatus” korrigerar ett problem för virtuella datorer utan datadiskar</span><span class="sxs-lookup"><span data-stu-id="7a256-176">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="7a256-177">Uppdatera version av klientbibliotek för Compute för att korrigera följande cmdletar</span><span class="sxs-lookup"><span data-stu-id="7a256-177">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="7a256-178">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="7a256-178">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="7a256-179">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="7a256-179">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="7a256-180">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="7a256-180">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="7a256-181">Följande cmdletar har åtgärdats för att visa ”Åtgärds-ID” och ”Åtgärdsstatus” på ett korrekt sätt:</span><span class="sxs-lookup"><span data-stu-id="7a256-181">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="7a256-182">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="7a256-182">Start-AzureRmVM</span></span>
    - <span data-ttu-id="7a256-183">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="7a256-183">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="7a256-184">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="7a256-184">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="7a256-185">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="7a256-185">Set-AzureRmVM</span></span>
    - <span data-ttu-id="7a256-186">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="7a256-186">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="7a256-187">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="7a256-187">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="7a256-188">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="7a256-188">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="7a256-189">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="7a256-189">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="7a256-190">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="7a256-190">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="7a256-191">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="7a256-191">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="7a256-192">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="7a256-192">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="7a256-193">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="7a256-193">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="7a256-194">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="7a256-194">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="7a256-195">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="7a256-195">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="7a256-196">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="7a256-196">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="7a256-197">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="7a256-197">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="7a256-198">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="7a256-198">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="7a256-199">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="7a256-199">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="7a256-200">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="7a256-200">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="7a256-201">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="7a256-201">AzureRM.EventGrid</span></span>
* <span data-ttu-id="7a256-202">Ta bort verifieringsvillkoren ValidateNotNullOrEmpty för SubjectBeginsWith/SubjectEndsWith i cmdleten Update-AzureRmEventGridSubscription för att ändra de här parametrarna till en tom sträng om det behövs.</span><span class="sxs-lookup"><span data-stu-id="7a256-202">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="7a256-203">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7a256-203">AzureRM.KeyVault</span></span>
* <span data-ttu-id="7a256-204">Åtgärda problem där inga taggar returneras när Get-AzureRmKeyVault -Tag körs</span><span class="sxs-lookup"><span data-stu-id="7a256-204">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="7a256-205">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="7a256-205">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="7a256-206">Offentlig lansering av cmdletar för Policy Insights</span><span class="sxs-lookup"><span data-stu-id="7a256-206">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="7a256-207">Använd API-version 2018-04-04</span><span class="sxs-lookup"><span data-stu-id="7a256-207">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="7a256-208">Lägg till PolicyDefinitionReferenceId i resultaten för Get-AzureRmPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="7a256-208">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="7a256-209">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7a256-209">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="7a256-210">Parametern -Vault har lagts till i cmdletarna för RecoveryServices.Backup.</span><span class="sxs-lookup"><span data-stu-id="7a256-210">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="7a256-211">När den godkänns åsidosätts cmdleten Set-AzureRmRecoveryServicesContext.</span><span class="sxs-lookup"><span data-stu-id="7a256-211">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="7a256-212">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="7a256-212">AzureRM.Sql</span></span>
* <span data-ttu-id="7a256-213">Exemplet i hjälpfilen för Get-AzureRmSqlDatabaseExpanded har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="7a256-213">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="7a256-214">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="7a256-214">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="7a256-215">Hjälpfilen för Add-AzureRmTrafficManagerEndpointConfig har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="7a256-215">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="7a256-216">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="7a256-216">AzureRM.Websites</span></span>
* <span data-ttu-id="7a256-217">”Set-AzureRmWebApp” har uppdaterats så att den inte skriver över appinställningarna när du använder -AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="7a256-217">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="7a256-218">”New-AzureRMWebAppSlot” har uppdaterats för att visa att AppServicePlan är en valfri parameter</span><span class="sxs-lookup"><span data-stu-id="7a256-218">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="7a256-219">6.2.1 – juni 2018</span><span class="sxs-lookup"><span data-stu-id="7a256-219">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="7a256-220">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7a256-220">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="7a256-221">PSWorkspace-modellen har uppdaterats för att tillåta att nätverket använder typ som en parameter</span><span class="sxs-lookup"><span data-stu-id="7a256-221">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="7a256-222">6.2.0 – juni 2018</span><span class="sxs-lookup"><span data-stu-id="7a256-222">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="7a256-223">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="7a256-223">AzureRM.Profile</span></span>
* <span data-ttu-id="7a256-224">Åtgärda problemet med att version 10.0.3 av Newtonsoft.Json inte lästes in vid modulimporten</span><span class="sxs-lookup"><span data-stu-id="7a256-224">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="7a256-225">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="7a256-225">AzureRM.Compute</span></span>
* <span data-ttu-id="7a256-226">VMSS VM-uppdateringsfunktion</span><span class="sxs-lookup"><span data-stu-id="7a256-226">VMSS VM Update feature</span></span>
    - <span data-ttu-id="7a256-227">Cmdletarna Update-AzureRmVmssVM och New-AzureRmVMDataDisk har lagts till</span><span class="sxs-lookup"><span data-stu-id="7a256-227">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="7a256-228">Lägg till parametern VirtualMachineScaleSetVM till cmdleten Add-AzureRmVMDataDisk så att det går att lägga till en datadisk i den virtuella Vmss-datorn.</span><span class="sxs-lookup"><span data-stu-id="7a256-228">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="7a256-229">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="7a256-229">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="7a256-230">SDK:n för ADF .Net har uppdaterats till version 0.8.0-preview som innehåller följande ändringar:</span><span class="sxs-lookup"><span data-stu-id="7a256-230">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="7a256-231">Åtgärden för att konfigurera fabrikslagringsplatsen har lagts till</span><span class="sxs-lookup"><span data-stu-id="7a256-231">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="7a256-232">QuickBooks LinkedService har uppdaterats för att visa egenskaperna consumerKey och consumerSecret</span><span class="sxs-lookup"><span data-stu-id="7a256-232">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="7a256-233">Flera modelltyper från SecretBase till Object har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="7a256-233">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="7a256-234">Utlösaren Blob Events har lagts till</span><span class="sxs-lookup"><span data-stu-id="7a256-234">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="7a256-235">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7a256-235">AzureRM.KeyVault</span></span>
* <span data-ttu-id="7a256-236">Uppdatera dokumentation med exempel på utdata</span><span class="sxs-lookup"><span data-stu-id="7a256-236">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="7a256-237">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="7a256-237">AzureRM.Network</span></span>
* <span data-ttu-id="7a256-238">Aktivera Trafikanalys-parametrar på Network Watcher-cmdletar</span><span class="sxs-lookup"><span data-stu-id="7a256-238">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="7a256-239">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="7a256-239">AzureRM.Resources</span></span>
* <span data-ttu-id="7a256-240">Åtgärda problemet med egenskapen "Properties" för objekt(en) "PSResource" som returneras från "Get-AzureRmResource"</span><span class="sxs-lookup"><span data-stu-id="7a256-240">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="7a256-241">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="7a256-241">AzureRM.Scheduler</span></span>
* <span data-ttu-id="7a256-242">Åtgärda problemet med att nya autentiseringsvärden inte anges vid uppdatering av ServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="7a256-242">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="7a256-243">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="7a256-243">AzureRM.Sql</span></span>
* <span data-ttu-id="7a256-244">Följande cmdletar har uppdaterats med valfri LicenseType-parameter</span><span class="sxs-lookup"><span data-stu-id="7a256-244">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="7a256-245">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="7a256-245">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="7a256-246">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="7a256-246">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="7a256-247">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="7a256-247">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="7a256-248">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="7a256-248">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="7a256-249">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="7a256-249">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="7a256-250">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="7a256-250">AzureRM.Websites</span></span>
* <span data-ttu-id="7a256-251">New-AzureRMWebApp har uppdaterats för att använda vanliga algoritmer från biblioteket Strategy.</span><span class="sxs-lookup"><span data-stu-id="7a256-251">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="7a256-252">6.1.0 – maj 2018</span><span class="sxs-lookup"><span data-stu-id="7a256-252">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="7a256-253">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="7a256-253">AzureRM.Profile</span></span>
* <span data-ttu-id="7a256-254">Åtgärda problem där en körning av Clear-AzureRmContext skulle bevara en tom kontext med namnet på den föregående standardkontexten som gjorde att användaren inte kunde skapa en ny kontext med det gamla namnet</span><span class="sxs-lookup"><span data-stu-id="7a256-254">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="7a256-255">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="7a256-255">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="7a256-256">Aktivera Gateway associerings- och avassocieringsåtgärder på AS.</span><span class="sxs-lookup"><span data-stu-id="7a256-256">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="7a256-257">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7a256-257">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="7a256-258">Stöd för ApiVersions, ApiReleases och ApiRevisions har lagts till</span><span class="sxs-lookup"><span data-stu-id="7a256-258">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="7a256-259">Stöd för serverdelen på ServiceFabric har lagts till</span><span class="sxs-lookup"><span data-stu-id="7a256-259">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="7a256-260">Stöd för Application Insights-loggare har lagts till</span><span class="sxs-lookup"><span data-stu-id="7a256-260">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="7a256-261">Stöd för att identifiera SKU:n ”Basic” som en giltig SKU för Api Management-tjänsten har lagts till</span><span class="sxs-lookup"><span data-stu-id="7a256-261">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="7a256-262">Stöd för att installera certifikat som utfärdats av privata certifikatutfärdare som rot eller certifikatutfärdare har lagts till</span><span class="sxs-lookup"><span data-stu-id="7a256-262">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="7a256-263">Stöd för att godkänna anpassade SSL-certifikat via KeyVault och flera proxy-värdnamn har lagts till</span><span class="sxs-lookup"><span data-stu-id="7a256-263">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="7a256-264">Stöd för MSI-identitet har lagts till</span><span class="sxs-lookup"><span data-stu-id="7a256-264">Added support for MSI identity</span></span>
* <span data-ttu-id="7a256-265">Stöd för att godkänna principer via URL har lagts till. Obs! Följande cmdletar blir inaktuella i framtida versioner</span><span class="sxs-lookup"><span data-stu-id="7a256-265">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="7a256-266">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="7a256-266">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="7a256-267">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="7a256-267">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="7a256-268">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="7a256-268">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="7a256-269">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="7a256-269">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="7a256-270">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="7a256-270">AzureRM.Batch</span></span>
* <span data-ttu-id="7a256-271">Släpp nya cmdleten Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="7a256-271">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="7a256-272">Släpp nya cmdleten Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="7a256-272">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="7a256-273">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="7a256-273">AzureRM.Consumption</span></span>
* <span data-ttu-id="7a256-274">Lägg till nya parametrar Expand, ResourceGroup, InstanceName, InstanceId, Tags och Top på cmdleten Get-AzureRmConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="7a256-274">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="7a256-275">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7a256-275">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="7a256-276">Åtgärda exempel för Export AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="7a256-276">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="7a256-277">Åtgärda undantag för null-parameter för rekursivt ärende i Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="7a256-277">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="7a256-278">Åtgärda hjälpfilerna för Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="7a256-278">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="7a256-279">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="7a256-279">AzureRM.Network</span></span>
* <span data-ttu-id="7a256-280">Öka nätverkets SDK-version från förhandsversionen 18.0.0 till förhandsversionen 19.0.0</span><span class="sxs-lookup"><span data-stu-id="7a256-280">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="7a256-281">Cmdlet har lagts till för att skapa protokollinformation</span><span class="sxs-lookup"><span data-stu-id="7a256-281">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="7a256-282">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="7a256-282">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="7a256-283">Cmdlet har lagts till för att lägga till en ny kretsanslutning till en befintlig expressroute-krets.</span><span class="sxs-lookup"><span data-stu-id="7a256-283">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="7a256-284">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="7a256-284">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="7a256-285">Cmdlet har lagts till för att ta bort en kretsanslutning från en befintlig expressroute-krets.</span><span class="sxs-lookup"><span data-stu-id="7a256-285">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="7a256-286">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="7a256-286">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="7a256-287">Cmdlet har lagts till för att hämta en kretsanslutning</span><span class="sxs-lookup"><span data-stu-id="7a256-287">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="7a256-288">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="7a256-288">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="7a256-289">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7a256-289">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="7a256-290">Användning med serverautentisering med genererade certifikat (problem #5998) har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="7a256-290">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="7a256-291">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="7a256-291">AzureRM.Sql</span></span>
* <span data-ttu-id="7a256-292">Cmdletar för granskning för att ta bort AuditActions eller AuditActionGroups har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="7a256-292">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="7a256-293">Åtgärdade problem med Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy vid konfigurering av en ny flexibel bevarandeprincip där kommandot misslyckas med ett meddelande om att konfigurering av långsiktig bevarandeprincip med Azure Recovery Service-valv och principen inte längre stöds,</span><span class="sxs-lookup"><span data-stu-id="7a256-293">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="7a256-294">och att en begäran med den nya flexibla bevarandeprincipen ska skickas.</span><span class="sxs-lookup"><span data-stu-id="7a256-294">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="7a256-295">Uppdatera alla Azure Sql Database/ElasticPool Creation/Update-relaterade cmdletar för att använda det nya databas-API:et som stöder SKU-egenskaper för skalnings- och nivårelaterade egenskaper.</span><span class="sxs-lookup"><span data-stu-id="7a256-295">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="7a256-296">Cmdletar har uppdaterats, inklusive:</span><span class="sxs-lookup"><span data-stu-id="7a256-296">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="7a256-297">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="7a256-297">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="7a256-298">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="7a256-298">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="7a256-299">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="7a256-299">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="7a256-300">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="7a256-300">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="7a256-301">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="7a256-301">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="7a256-302">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="7a256-302">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="7a256-303">Uppdatera parametrarna för Get-AzureRmTrafficManagerProfile så att ResourceGroupName-parametern blir obligatorisk när du använder Name-parametern.</span><span class="sxs-lookup"><span data-stu-id="7a256-303">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>