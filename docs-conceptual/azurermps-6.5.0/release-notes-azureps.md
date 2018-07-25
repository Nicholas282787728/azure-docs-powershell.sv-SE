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
ms.openlocfilehash: e9fa2d75c1c4e6ffaa2f7dd8e400f5b13dd4527d
ms.sourcegitcommit: 8b882d1c27d9e323447ff85f56d11bbf5e244d7f
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2018
ms.locfileid: "39110491"
---
# <a name="release-notes"></a><span data-ttu-id="8a20d-103">Viktig information</span><span class="sxs-lookup"><span data-stu-id="8a20d-103">Release notes</span></span>

<span data-ttu-id="8a20d-104">Det här är en lista över ändringar som har gjorts i Azure PowerShell i den här versionen.</span><span class="sxs-lookup"><span data-stu-id="8a20d-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="650---july-2018"></a><span data-ttu-id="8a20d-105">6.5.0 – juli 2018</span><span class="sxs-lookup"><span data-stu-id="8a20d-105">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="8a20d-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="8a20d-106">AzureRM.Profile</span></span>
* <span data-ttu-id="8a20d-107">Hjälp för ”Get-AzureRmContextAutosaveSetting” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="8a20d-107">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="8a20d-108">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="8a20d-108">Azure.Storage</span></span>
* <span data-ttu-id="8a20d-109">Stöd för uppladdning av blob eller fil med lässkyddad SAS-token</span><span class="sxs-lookup"><span data-stu-id="8a20d-109">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="8a20d-110">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="8a20d-110">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="8a20d-111">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="8a20d-111">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="8a20d-112">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="8a20d-112">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="8a20d-113">Lägg till den nödvändiga egenskapen ResourceGroupName i AS.</span><span class="sxs-lookup"><span data-stu-id="8a20d-113">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="8a20d-114">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="8a20d-114">AzureRM.Automation</span></span>
* <span data-ttu-id="8a20d-115">Uppdatera hjälp och lägg till exempel för ”New-AzureRMAutomationSchedule”</span><span class="sxs-lookup"><span data-stu-id="8a20d-115">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="8a20d-116">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="8a20d-116">AzureRM.Compute</span></span>
* <span data-ttu-id="8a20d-117">Lägg till parametern -Tag förUpdate/New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="8a20d-117">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="8a20d-118">Lägg till exempel för ”Add-AzureRmVmssExtension”</span><span class="sxs-lookup"><span data-stu-id="8a20d-118">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="8a20d-119">Lägg till exempel för ”Remove-AzureRmVmssExtension”</span><span class="sxs-lookup"><span data-stu-id="8a20d-119">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="8a20d-120">Uppdatera hjälp för ”Set-AzureRmVMAccessExtension”</span><span class="sxs-lookup"><span data-stu-id="8a20d-120">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="8a20d-121">Uppdatera SimpleParameterSet för New-AzureRmVmss för att ställa in SinglePlacementGroup på falskt som standard och lägg till växlingsparametern ”SinglePlacementGroup” som gör att användare kan skapa VMSS i en enda placeringsgrupp.</span><span class="sxs-lookup"><span data-stu-id="8a20d-121">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="8a20d-122">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="8a20d-122">AzureRM.EventHub</span></span>
* <span data-ttu-id="8a20d-123">En skrivskyddad egenskap, ”PendingReplicationOperationsCount”, har lagts till för klassen PSEventHubDRConfigurationAttributes som anger antalet väntande replikeringsåtgärder medan replikeringen pågår</span><span class="sxs-lookup"><span data-stu-id="8a20d-123">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="8a20d-124">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8a20d-124">AzureRM.KeyVault</span></span>
* <span data-ttu-id="8a20d-125">Uppdatera felmeddelande för Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8a20d-125">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="8a20d-126">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="8a20d-126">AzureRM.LogicApp</span></span>
* <span data-ttu-id="8a20d-127">Felet ”parameteruppsättningen gick inte att matcha” har korrigerats i New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="8a20d-127">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="8a20d-128">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="8a20d-128">AzureRM.Network</span></span>
* <span data-ttu-id="8a20d-129">Aktivera peering mellan virtuella nätverk i flera klienter för Set/Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="8a20d-129">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="8a20d-130">Nedanstående cmdletar för Application Gateway har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="8a20d-130">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="8a20d-131">New-AzureRmApplicationGateway: EnableFIPS-flagga har lagts till för stöd för zoner</span><span class="sxs-lookup"><span data-stu-id="8a20d-131">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="8a20d-132">New-AzureRmApplicationGatewaySku: nya SKU:er, Standard_v2 och WAF_v2, har lagts till</span><span class="sxs-lookup"><span data-stu-id="8a20d-132">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="8a20d-133">Set-AzureRmApplicationGatewaySku: nya SKU:er, Standard_v2 och WAF_v2, har lagts till</span><span class="sxs-lookup"><span data-stu-id="8a20d-133">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="8a20d-134">RouteTable-cmdletar har återskapats med den senaste versionen av generatorn</span><span class="sxs-lookup"><span data-stu-id="8a20d-134">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="8a20d-135">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="8a20d-135">AzureRM.Relay</span></span>
* <span data-ttu-id="8a20d-136">Markdown-filer har uppdaterats och korrigerar problem med parameternamn i exemplet</span><span class="sxs-lookup"><span data-stu-id="8a20d-136">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="8a20d-137">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="8a20d-137">AzureRM.Resources</span></span>
* <span data-ttu-id="8a20d-138">Uppdatera cmdletar för rolltilldelning och rolldefinition:</span><span class="sxs-lookup"><span data-stu-id="8a20d-138">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="8a20d-139">Ta bort extra anrop för rolldefinitioner som görs som en del av sidindelning.</span><span class="sxs-lookup"><span data-stu-id="8a20d-139">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="8a20d-140">Åtgärda Get-AzureRMRoleAssignment-cmdlet</span><span class="sxs-lookup"><span data-stu-id="8a20d-140">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="8a20d-141">Åtgärda parameterfunktioner för kommandot -ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="8a20d-141">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="8a20d-142">Åtgärda problem med ”Get-AzureRmResource” där ”-ResourceType”-parametern var skiftlägeskänsligt</span><span class="sxs-lookup"><span data-stu-id="8a20d-142">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="8a20d-143">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8a20d-143">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="8a20d-144">Parametrar för att stoppa och hoppa över har lagts till i listan över cmdletar</span><span class="sxs-lookup"><span data-stu-id="8a20d-144">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="8a20d-145">Cmdletar för migrering från Standard- till Premium-namnområden har lagts till:</span><span class="sxs-lookup"><span data-stu-id="8a20d-145">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="8a20d-146">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="8a20d-146">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="8a20d-147">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="8a20d-147">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="8a20d-148">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="8a20d-148">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="8a20d-149">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="8a20d-149">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="8a20d-150">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="8a20d-150">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="8a20d-151">En skrivskyddad egenskap, ”PendingReplicationOperationsCount” har lagts till för klassen PSServiceBusDRConfigurationAttributes som anger antalet väntande replikeringsåtgärder medan replikeringen pågår</span><span class="sxs-lookup"><span data-stu-id="8a20d-151">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="8a20d-152">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8a20d-152">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="8a20d-153">Uppdatera exempel för ”New-AzureRmServiceFabricCluster”</span><span class="sxs-lookup"><span data-stu-id="8a20d-153">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="8a20d-154">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="8a20d-154">AzureRM.Sql</span></span>
* <span data-ttu-id="8a20d-155">Nya cmdletar för Management.Sql som gör att kunderna kan lägga till certifikat för transparent datakryptering till SQL Server-instans eller en hanterad instans har lagts till</span><span class="sxs-lookup"><span data-stu-id="8a20d-155">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="8a20d-156">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="8a20d-156">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="8a20d-157">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="8a20d-157">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="8a20d-158">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="8a20d-158">AzureRM.Websites</span></span>
* <span data-ttu-id="8a20d-159">När `Set-AzureRmWebApp -AssignIdentity` och `Set-AzureRmWebAppSlot -AssignIdentity` är inställda på falskt tar de nu bort identitetsegenskapen från platsobjektet. Även förhandsgranskningstaggen tas bort.</span><span class="sxs-lookup"><span data-stu-id="8a20d-159">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="8a20d-160">`Get-AzureRmWebAppMetrics`, `Get-AzureRmAppServicePlanMetrics`-exempel har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="8a20d-160">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="8a20d-161">`Set-AzureRmWebApp -PhpVersion` har stöd för ”av” som en giltig php-version</span><span class="sxs-lookup"><span data-stu-id="8a20d-161">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="8a20d-162">6.4.0 – juli 2018</span><span class="sxs-lookup"><span data-stu-id="8a20d-162">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="8a20d-163">Allmänt</span><span class="sxs-lookup"><span data-stu-id="8a20d-163">General</span></span>
* <span data-ttu-id="8a20d-164">Formatering av OutputType i hjälpfiler har korrigerats för de flesta moduler</span><span class="sxs-lookup"><span data-stu-id="8a20d-164">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="8a20d-165">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="8a20d-165">AzureRM.Profile</span></span>
* <span data-ttu-id="8a20d-166">Ps1Xml-attribut har lagts till för grundläggande utdatatyper</span><span class="sxs-lookup"><span data-stu-id="8a20d-166">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="8a20d-167">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="8a20d-167">AzureRM.Compute</span></span>
* <span data-ttu-id="8a20d-168">IP-tagg-funktioner för VMSS</span><span class="sxs-lookup"><span data-stu-id="8a20d-168">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="8a20d-169">"New-AzureRmVmssIpTagConfig"-cmdlet har lagts till</span><span class="sxs-lookup"><span data-stu-id="8a20d-169">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="8a20d-170">IpTag-parameter har lagts till för New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="8a20d-170">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="8a20d-171">Automatisk återställningsfunktion för operativsystem för VMSS</span><span class="sxs-lookup"><span data-stu-id="8a20d-171">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="8a20d-172">DisableAutoRollback-parametrar har lagts till för New-AzureRmVmssConfig och Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="8a20d-172">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="8a20d-173">Funktion för uppgraderingshistorik för operativsystem för Vmss</span><span class="sxs-lookup"><span data-stu-id="8a20d-173">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="8a20d-174">OSUpgradeHistory-växlingsparametern har lagts till för Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="8a20d-174">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="8a20d-175">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="8a20d-175">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="8a20d-176">Lägg till stöd för katalog-ACL:er med hjälp av följande kommandon:</span><span class="sxs-lookup"><span data-stu-id="8a20d-176">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="8a20d-177">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="8a20d-177">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="8a20d-178">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="8a20d-178">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="8a20d-179">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="8a20d-179">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="8a20d-180">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8a20d-180">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="8a20d-181">Lägg till stöd för annullering och förloppsspårning för Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="8a20d-181">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="8a20d-182">Lägg till stöd för annullering för Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="8a20d-182">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="8a20d-183">Åtgärda tömning av felsökningsmeddelanden för cmdletar som gör rekursiva åtgärder</span><span class="sxs-lookup"><span data-stu-id="8a20d-183">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="8a20d-184">Åtgärda platsen för testning av DataLake-cmdletar</span><span class="sxs-lookup"><span data-stu-id="8a20d-184">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="8a20d-185">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="8a20d-185">AzureRM.EventHub</span></span>
* <span data-ttu-id="8a20d-186">Parametrar för optimalt maxantal har lagts till i liståtgärds-cmdletarna Get-AzureRmEventHub och Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="8a20d-186">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="8a20d-187">Ett problem i New-AzureRmEventHub-cmdleten har åtgärdats där minst en parameter behövdes när du skapade en ny EventHub.</span><span class="sxs-lookup"><span data-stu-id="8a20d-187">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="8a20d-188">Angiven standardparameter har ställts in.</span><span class="sxs-lookup"><span data-stu-id="8a20d-188">Provided Default Parameter set.</span></span>
* <span data-ttu-id="8a20d-189">Valfri parameter för KeyValue har lagts till för New-AzureRmEventHubKey-cmdleten, vilket gör det möjligt att ange KeyValue.</span><span class="sxs-lookup"><span data-stu-id="8a20d-189">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="8a20d-190">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8a20d-190">AzureRM.KeyVault</span></span>
* <span data-ttu-id="8a20d-191">Åtgärda problem där alla resurser returnerades av Get-AzureRmKeyVault-taggen</span><span class="sxs-lookup"><span data-stu-id="8a20d-191">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="8a20d-192">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="8a20d-192">AzureRM.Network</span></span>
* <span data-ttu-id="8a20d-193">Gör nya SKU:er tillgängliga för zonredundanta VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="8a20d-193">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="8a20d-194">Nya kommandon har lagts till för funktionen: ExpressRoute Partner APIs via ARM</span><span class="sxs-lookup"><span data-stu-id="8a20d-194">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="8a20d-195">Get-AzureRmExpressRouteCrossConnection har lagts till</span><span class="sxs-lookup"><span data-stu-id="8a20d-195">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="8a20d-196">Set-AzureRmExpressRouteCrossConnection har lagts till</span><span class="sxs-lookup"><span data-stu-id="8a20d-196">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="8a20d-197">Add-AzureRmExpressRouteCrossConnectionPeering har lagts till</span><span class="sxs-lookup"><span data-stu-id="8a20d-197">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="8a20d-198">Get-AzureRmExpressRouteCrossConnectionPeering har lagts till</span><span class="sxs-lookup"><span data-stu-id="8a20d-198">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="8a20d-199">Remove-AzureRmExpressRouteCrossConnectionPeering har lagts till</span><span class="sxs-lookup"><span data-stu-id="8a20d-199">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="8a20d-200">Get-AzureRMExpressRouteCrossConnectionArpTable har lagts till</span><span class="sxs-lookup"><span data-stu-id="8a20d-200">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="8a20d-201">Get-AzureRMExpressRouteCrossConnectionRouteTable har lagts till</span><span class="sxs-lookup"><span data-stu-id="8a20d-201">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="8a20d-202">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary har lagts till</span><span class="sxs-lookup"><span data-stu-id="8a20d-202">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="8a20d-203">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8a20d-203">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="8a20d-204">Get-AzureRmRecoveryServicesBackupStatus-cmdlet har lagts till.</span><span class="sxs-lookup"><span data-stu-id="8a20d-204">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="8a20d-205">Denna cmdlet tar ett ID för virtuell dator och kontrollerar om den virtuella datorn skyddas av ett valv i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="8a20d-205">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="8a20d-206">Om ett sådant valv finns returnerar cmdleten valvinformationen.</span><span class="sxs-lookup"><span data-stu-id="8a20d-206">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="8a20d-207">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="8a20d-207">AzureRM.Resources</span></span>
* <span data-ttu-id="8a20d-208">Uppdatera Get-AzureRmPolicyAssignment-cmdletar:</span><span class="sxs-lookup"><span data-stu-id="8a20d-208">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="8a20d-209">Lägg till stöd för att lista -Scope-värden på hanteringsgruppsnivå</span><span class="sxs-lookup"><span data-stu-id="8a20d-209">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="8a20d-210">Lägg till stöd för hämtning av enskilda tilldelningar med -Scope-värden på hanteringsgruppsnivå.</span><span class="sxs-lookup"><span data-stu-id="8a20d-210">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="8a20d-211">Lägg till växlar för -Effective och -All till kontrollparametrar</span><span class="sxs-lookup"><span data-stu-id="8a20d-211">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="8a20d-212">Uppdatera Get/New/Remove/Set-AzureRmPolicyDefinition-cmdletar</span><span class="sxs-lookup"><span data-stu-id="8a20d-212">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="8a20d-213">Lägg till parameter för -ManagementGroupName om du vill tillämpa åtgärder för en viss hanteringsgrupp</span><span class="sxs-lookup"><span data-stu-id="8a20d-213">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="8a20d-214">Lägg till parameter för -SubscriptionId om du vill tillämpa åtgärder för en viss prenumeration</span><span class="sxs-lookup"><span data-stu-id="8a20d-214">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="8a20d-215">Uppdatera Get/New/Remove/Set-AzureRmPolicySetDefinition-cmdletar</span><span class="sxs-lookup"><span data-stu-id="8a20d-215">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="8a20d-216">Lägg till parameter för -ManagementGroupName om du vill tillämpa åtgärder för en viss hanteringsgrupp</span><span class="sxs-lookup"><span data-stu-id="8a20d-216">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="8a20d-217">Lägg till parameter för -SubscriptionId om du vill tillämpa åtgärder för en viss prenumeration</span><span class="sxs-lookup"><span data-stu-id="8a20d-217">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="8a20d-218">Lägg till stöd för hemliga KeyVault-referenser i parametrar när du använder "TemplateParameterObject" i "New-AzureRmResourceGroupDeployment"</span><span class="sxs-lookup"><span data-stu-id="8a20d-218">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="8a20d-219">Åtgärda problem med att "-EndDate"-parametern ignorerades på grund av "New-AzureRmADAppCredential"</span><span class="sxs-lookup"><span data-stu-id="8a20d-219">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="8a20d-220">Åtgärda problem med att felaktig URL användes i "New-AzureRmADAppCredential" vid begäran</span><span class="sxs-lookup"><span data-stu-id="8a20d-220">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="8a20d-221">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8a20d-221">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="8a20d-222">Valfri parameter för -KeyValue har lagts till för New-AzureRmServiceBusKey-cmdleten, vilket gör det möjligt att ange KeyValue.</span><span class="sxs-lookup"><span data-stu-id="8a20d-222">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="8a20d-223">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="8a20d-223">AzureRM.Sql</span></span>
* <span data-ttu-id="8a20d-224">Användardefinierade återställningspunkter har klargjorts för SQLDW i New-AzureRmSqlDatabaseRestorePoint-hjälpen</span><span class="sxs-lookup"><span data-stu-id="8a20d-224">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="8a20d-225">Dokumentationen om parametern -ComputeGeneration har uppdaterats i fler cmdletar</span><span class="sxs-lookup"><span data-stu-id="8a20d-225">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="8a20d-226">6.3.0 – juni 2018</span><span class="sxs-lookup"><span data-stu-id="8a20d-226">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="8a20d-227">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="8a20d-227">AzureRM.Profile</span></span>
* <span data-ttu-id="8a20d-228">Uppdaterade felmeddelanden för Enable-AzureRmContextAutoSave</span><span class="sxs-lookup"><span data-stu-id="8a20d-228">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="8a20d-229">Skapa en kontext för varje prenumeration när du kör ”Connect-AzureRmAccount” utan tidigare kontext</span><span class="sxs-lookup"><span data-stu-id="8a20d-229">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="8a20d-230">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="8a20d-230">Azure.Storage</span></span>
* <span data-ttu-id="8a20d-231">Ytterligare information om parametern -Permissions har lagts till i hjälpfilerna.</span><span class="sxs-lookup"><span data-stu-id="8a20d-231">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="8a20d-232">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="8a20d-232">AzureRM.Compute</span></span>
* <span data-ttu-id="8a20d-233">”Get-AzureRmVmDiskEncryptionStatus” korrigerar ett problem för virtuella datorer utan datadiskar</span><span class="sxs-lookup"><span data-stu-id="8a20d-233">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="8a20d-234">Uppdatera version av klientbibliotek för Compute för att korrigera följande cmdletar</span><span class="sxs-lookup"><span data-stu-id="8a20d-234">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="8a20d-235">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="8a20d-235">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="8a20d-236">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="8a20d-236">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="8a20d-237">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="8a20d-237">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="8a20d-238">Följande cmdletar har åtgärdats för att visa ”Åtgärds-ID” och ”Åtgärdsstatus” på ett korrekt sätt:</span><span class="sxs-lookup"><span data-stu-id="8a20d-238">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="8a20d-239">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8a20d-239">Start-AzureRmVM</span></span>
    - <span data-ttu-id="8a20d-240">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8a20d-240">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="8a20d-241">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8a20d-241">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="8a20d-242">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8a20d-242">Set-AzureRmVM</span></span>
    - <span data-ttu-id="8a20d-243">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="8a20d-243">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="8a20d-244">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="8a20d-244">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="8a20d-245">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="8a20d-245">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="8a20d-246">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="8a20d-246">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="8a20d-247">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="8a20d-247">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="8a20d-248">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="8a20d-248">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="8a20d-249">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="8a20d-249">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="8a20d-250">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="8a20d-250">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="8a20d-251">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="8a20d-251">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="8a20d-252">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="8a20d-252">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="8a20d-253">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="8a20d-253">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="8a20d-254">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="8a20d-254">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="8a20d-255">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="8a20d-255">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="8a20d-256">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="8a20d-256">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="8a20d-257">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="8a20d-257">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="8a20d-258">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="8a20d-258">AzureRM.EventGrid</span></span>
* <span data-ttu-id="8a20d-259">Ta bort verifieringsvillkoren ValidateNotNullOrEmpty för SubjectBeginsWith/SubjectEndsWith i cmdleten Update-AzureRmEventGridSubscription för att ändra de här parametrarna till en tom sträng om det behövs.</span><span class="sxs-lookup"><span data-stu-id="8a20d-259">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="8a20d-260">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8a20d-260">AzureRM.KeyVault</span></span>
* <span data-ttu-id="8a20d-261">Åtgärda problem där inga taggar returneras när Get-AzureRmKeyVault -Tag körs</span><span class="sxs-lookup"><span data-stu-id="8a20d-261">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="8a20d-262">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="8a20d-262">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="8a20d-263">Offentlig lansering av cmdletar för Policy Insights</span><span class="sxs-lookup"><span data-stu-id="8a20d-263">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="8a20d-264">Använd API-version 2018-04-04</span><span class="sxs-lookup"><span data-stu-id="8a20d-264">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="8a20d-265">Lägg till PolicyDefinitionReferenceId i resultaten för Get-AzureRmPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="8a20d-265">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="8a20d-266">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8a20d-266">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="8a20d-267">Parametern -Vault har lagts till i cmdletarna för RecoveryServices.Backup.</span><span class="sxs-lookup"><span data-stu-id="8a20d-267">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="8a20d-268">När den godkänns åsidosätts cmdleten Set-AzureRmRecoveryServicesContext.</span><span class="sxs-lookup"><span data-stu-id="8a20d-268">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="8a20d-269">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="8a20d-269">AzureRM.Sql</span></span>
* <span data-ttu-id="8a20d-270">Exemplet i hjälpfilen för Get-AzureRmSqlDatabaseExpanded har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="8a20d-270">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="8a20d-271">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="8a20d-271">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="8a20d-272">Hjälpfilen för Add-AzureRmTrafficManagerEndpointConfig har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="8a20d-272">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="8a20d-273">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="8a20d-273">AzureRM.Websites</span></span>
* <span data-ttu-id="8a20d-274">”Set-AzureRmWebApp” har uppdaterats så att den inte skriver över appinställningarna när du använder -AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="8a20d-274">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="8a20d-275">”New-AzureRMWebAppSlot” har uppdaterats för att visa att AppServicePlan är en valfri parameter</span><span class="sxs-lookup"><span data-stu-id="8a20d-275">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="8a20d-276">6.2.1 – juni 2018</span><span class="sxs-lookup"><span data-stu-id="8a20d-276">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="8a20d-277">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8a20d-277">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="8a20d-278">PSWorkspace-modellen har uppdaterats för att tillåta att nätverket använder typ som en parameter</span><span class="sxs-lookup"><span data-stu-id="8a20d-278">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="8a20d-279">6.2.0 – juni 2018</span><span class="sxs-lookup"><span data-stu-id="8a20d-279">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="8a20d-280">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="8a20d-280">AzureRM.Profile</span></span>
* <span data-ttu-id="8a20d-281">Åtgärda problemet med att version 10.0.3 av Newtonsoft.Json inte lästes in vid modulimporten</span><span class="sxs-lookup"><span data-stu-id="8a20d-281">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="8a20d-282">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="8a20d-282">AzureRM.Compute</span></span>
* <span data-ttu-id="8a20d-283">VMSS VM-uppdateringsfunktion</span><span class="sxs-lookup"><span data-stu-id="8a20d-283">VMSS VM Update feature</span></span>
    - <span data-ttu-id="8a20d-284">Cmdletarna Update-AzureRmVmssVM och New-AzureRmVMDataDisk har lagts till</span><span class="sxs-lookup"><span data-stu-id="8a20d-284">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="8a20d-285">Lägg till parametern VirtualMachineScaleSetVM till cmdleten Add-AzureRmVMDataDisk så att det går att lägga till en datadisk i den virtuella Vmss-datorn.</span><span class="sxs-lookup"><span data-stu-id="8a20d-285">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="8a20d-286">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="8a20d-286">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="8a20d-287">SDK:n för ADF .Net har uppdaterats till version 0.8.0-preview som innehåller följande ändringar:</span><span class="sxs-lookup"><span data-stu-id="8a20d-287">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="8a20d-288">Åtgärden för att konfigurera fabrikslagringsplatsen har lagts till</span><span class="sxs-lookup"><span data-stu-id="8a20d-288">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="8a20d-289">QuickBooks LinkedService har uppdaterats för att visa egenskaperna consumerKey och consumerSecret</span><span class="sxs-lookup"><span data-stu-id="8a20d-289">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="8a20d-290">Flera modelltyper från SecretBase till Object har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="8a20d-290">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="8a20d-291">Utlösaren Blob Events har lagts till</span><span class="sxs-lookup"><span data-stu-id="8a20d-291">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="8a20d-292">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8a20d-292">AzureRM.KeyVault</span></span>
* <span data-ttu-id="8a20d-293">Uppdatera dokumentation med exempel på utdata</span><span class="sxs-lookup"><span data-stu-id="8a20d-293">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="8a20d-294">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="8a20d-294">AzureRM.Network</span></span>
* <span data-ttu-id="8a20d-295">Aktivera Trafikanalys-parametrar på Network Watcher-cmdletar</span><span class="sxs-lookup"><span data-stu-id="8a20d-295">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="8a20d-296">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="8a20d-296">AzureRM.Resources</span></span>
* <span data-ttu-id="8a20d-297">Åtgärda problemet med egenskapen "Properties" för objekt(en) "PSResource" som returneras från "Get-AzureRmResource"</span><span class="sxs-lookup"><span data-stu-id="8a20d-297">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="8a20d-298">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="8a20d-298">AzureRM.Scheduler</span></span>
* <span data-ttu-id="8a20d-299">Åtgärda problemet med att nya autentiseringsvärden inte anges vid uppdatering av ServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="8a20d-299">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="8a20d-300">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="8a20d-300">AzureRM.Sql</span></span>
* <span data-ttu-id="8a20d-301">Följande cmdletar har uppdaterats med valfri LicenseType-parameter</span><span class="sxs-lookup"><span data-stu-id="8a20d-301">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="8a20d-302">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8a20d-302">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="8a20d-303">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="8a20d-303">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="8a20d-304">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="8a20d-304">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="8a20d-305">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="8a20d-305">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="8a20d-306">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8a20d-306">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="8a20d-307">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="8a20d-307">AzureRM.Websites</span></span>
* <span data-ttu-id="8a20d-308">New-AzureRMWebApp har uppdaterats för att använda vanliga algoritmer från biblioteket Strategy.</span><span class="sxs-lookup"><span data-stu-id="8a20d-308">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="8a20d-309">6.1.0 – maj 2018</span><span class="sxs-lookup"><span data-stu-id="8a20d-309">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="8a20d-310">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="8a20d-310">AzureRM.Profile</span></span>
* <span data-ttu-id="8a20d-311">Åtgärda problem där en körning av Clear-AzureRmContext skulle bevara en tom kontext med namnet på den föregående standardkontexten som gjorde att användaren inte kunde skapa en ny kontext med det gamla namnet</span><span class="sxs-lookup"><span data-stu-id="8a20d-311">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="8a20d-312">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="8a20d-312">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="8a20d-313">Aktivera Gateway associerings- och avassocieringsåtgärder på AS.</span><span class="sxs-lookup"><span data-stu-id="8a20d-313">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="8a20d-314">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8a20d-314">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="8a20d-315">Stöd för ApiVersions, ApiReleases och ApiRevisions har lagts till</span><span class="sxs-lookup"><span data-stu-id="8a20d-315">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="8a20d-316">Stöd för serverdelen på ServiceFabric har lagts till</span><span class="sxs-lookup"><span data-stu-id="8a20d-316">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="8a20d-317">Stöd för Application Insights-loggare har lagts till</span><span class="sxs-lookup"><span data-stu-id="8a20d-317">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="8a20d-318">Stöd för att identifiera SKU:n ”Basic” som en giltig SKU för Api Management-tjänsten har lagts till</span><span class="sxs-lookup"><span data-stu-id="8a20d-318">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="8a20d-319">Stöd för att installera certifikat som utfärdats av privata certifikatutfärdare som rot eller certifikatutfärdare har lagts till</span><span class="sxs-lookup"><span data-stu-id="8a20d-319">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="8a20d-320">Stöd för att godkänna anpassade SSL-certifikat via KeyVault och flera proxy-värdnamn har lagts till</span><span class="sxs-lookup"><span data-stu-id="8a20d-320">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="8a20d-321">Stöd för MSI-identitet har lagts till</span><span class="sxs-lookup"><span data-stu-id="8a20d-321">Added support for MSI identity</span></span>
* <span data-ttu-id="8a20d-322">Stöd för att godkänna principer via URL har lagts till. Obs! Följande cmdletar blir inaktuella i framtida versioner</span><span class="sxs-lookup"><span data-stu-id="8a20d-322">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="8a20d-323">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="8a20d-323">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="8a20d-324">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="8a20d-324">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="8a20d-325">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="8a20d-325">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="8a20d-326">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="8a20d-326">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="8a20d-327">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="8a20d-327">AzureRM.Batch</span></span>
* <span data-ttu-id="8a20d-328">Släpp nya cmdleten Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="8a20d-328">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="8a20d-329">Släpp nya cmdleten Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="8a20d-329">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="8a20d-330">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="8a20d-330">AzureRM.Consumption</span></span>
* <span data-ttu-id="8a20d-331">Lägg till nya parametrar Expand, ResourceGroup, InstanceName, InstanceId, Tags och Top på cmdleten Get-AzureRmConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="8a20d-331">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="8a20d-332">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8a20d-332">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="8a20d-333">Åtgärda exempel för Export AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="8a20d-333">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="8a20d-334">Åtgärda undantag för null-parameter för rekursivt ärende i Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="8a20d-334">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="8a20d-335">Åtgärda hjälpfilerna för Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="8a20d-335">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="8a20d-336">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="8a20d-336">AzureRM.Network</span></span>
* <span data-ttu-id="8a20d-337">Öka nätverkets SDK-version från förhandsversionen 18.0.0 till förhandsversionen 19.0.0</span><span class="sxs-lookup"><span data-stu-id="8a20d-337">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="8a20d-338">Cmdlet har lagts till för att skapa protokollinformation</span><span class="sxs-lookup"><span data-stu-id="8a20d-338">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="8a20d-339">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="8a20d-339">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="8a20d-340">Cmdlet har lagts till för att lägga till en ny kretsanslutning till en befintlig expressroute-krets.</span><span class="sxs-lookup"><span data-stu-id="8a20d-340">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="8a20d-341">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="8a20d-341">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="8a20d-342">Cmdlet har lagts till för att ta bort en kretsanslutning från en befintlig expressroute-krets.</span><span class="sxs-lookup"><span data-stu-id="8a20d-342">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="8a20d-343">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="8a20d-343">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="8a20d-344">Cmdlet har lagts till för att hämta en kretsanslutning</span><span class="sxs-lookup"><span data-stu-id="8a20d-344">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="8a20d-345">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="8a20d-345">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="8a20d-346">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8a20d-346">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="8a20d-347">Användning med serverautentisering med genererade certifikat (problem #5998) har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8a20d-347">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="8a20d-348">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="8a20d-348">AzureRM.Sql</span></span>
* <span data-ttu-id="8a20d-349">Cmdletar för granskning för att ta bort AuditActions eller AuditActionGroups har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="8a20d-349">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="8a20d-350">Åtgärdade problem med Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy vid konfigurering av en ny flexibel bevarandeprincip där kommandot misslyckas med ett meddelande om att konfigurering av långsiktig bevarandeprincip med Azure Recovery Service-valv och principen inte längre stöds,</span><span class="sxs-lookup"><span data-stu-id="8a20d-350">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="8a20d-351">och att en begäran med den nya flexibla bevarandeprincipen ska skickas.</span><span class="sxs-lookup"><span data-stu-id="8a20d-351">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="8a20d-352">Uppdatera alla Azure Sql Database/ElasticPool Creation/Update-relaterade cmdletar för att använda det nya databas-API:et som stöder SKU-egenskaper för skalnings- och nivårelaterade egenskaper.</span><span class="sxs-lookup"><span data-stu-id="8a20d-352">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="8a20d-353">Cmdletar har uppdaterats, inklusive:</span><span class="sxs-lookup"><span data-stu-id="8a20d-353">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="8a20d-354">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8a20d-354">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="8a20d-355">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="8a20d-355">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="8a20d-356">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="8a20d-356">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="8a20d-357">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="8a20d-357">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="8a20d-358">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8a20d-358">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="8a20d-359">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="8a20d-359">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="8a20d-360">Uppdatera parametrarna för Get-AzureRmTrafficManagerProfile så att ResourceGroupName-parametern blir obligatorisk när du använder Name-parametern.</span><span class="sxs-lookup"><span data-stu-id="8a20d-360">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>