---
ms.openlocfilehash: f89d13d6bbedaea29b62287942d8c7a509abe32b
ms.sourcegitcommit: abca342d8687ca638679c049792d0cef6045837d
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/27/2019
ms.locfileid: "70052642"
---
## <a name="260---august-2019"></a><span data-ttu-id="10a50-101">2.6.0 – augusti 2019</span><span class="sxs-lookup"><span data-stu-id="10a50-101">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="10a50-102">Allmänt</span><span class="sxs-lookup"><span data-stu-id="10a50-102">General</span></span>
* <span data-ttu-id="10a50-103">Åtgärdade diverse skrivfel i flera moduler</span><span class="sxs-lookup"><span data-stu-id="10a50-103">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="10a50-104">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="10a50-104">Az.Accounts</span></span>
* <span data-ttu-id="10a50-105">Stöd för användartilldelat MSI i Azure Functions-autentisering (#9479)</span><span class="sxs-lookup"><span data-stu-id="10a50-105">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="10a50-106">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="10a50-106">Az.Aks</span></span>
* <span data-ttu-id="10a50-107">Åtgärda problem med utdata för "Get-AzAks"</span><span class="sxs-lookup"><span data-stu-id="10a50-107">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="10a50-108">Mer information här: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="10a50-108">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="10a50-109">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="10a50-109">Az.ApiManagement</span></span>
* <span data-ttu-id="10a50-110">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="10a50-110">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="10a50-111">Uppdatera .net-NuGet-versionen, som inte tillämpar begränsningar för productId, apiId och userId</span><span class="sxs-lookup"><span data-stu-id="10a50-111">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="10a50-112">**Get-AzApiManagementProduct** – Lade till stöd för frågekörning mot produkter via API.</span><span class="sxs-lookup"><span data-stu-id="10a50-112">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="10a50-113">**New-AzApiManagementApiRevision** – Korrigering för problem där ApiRevisionDescription inte angavs vid skapande av ny API-revision https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="10a50-113">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="10a50-114">Åtgärdade skrivfel i modellen "PsApiManagementOAuth2AuthrozationServer" till "PsApiManagementOAuth2AuthorizationServer"</span><span class="sxs-lookup"><span data-stu-id="10a50-114">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="10a50-115">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="10a50-115">Az.Batch</span></span>
* <span data-ttu-id="10a50-116">Åtgärdade skrivfel i hjälpmeddelande och dokumentation till att skriva Windows med versaler</span><span class="sxs-lookup"><span data-stu-id="10a50-116">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="10a50-117">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="10a50-117">Az.Cdn</span></span>
* <span data-ttu-id="10a50-118">Åtgärdade skrivfel i CDN-modulens konverteringshjälp</span><span class="sxs-lookup"><span data-stu-id="10a50-118">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="10a50-119">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="10a50-119">Az.Compute</span></span>
* <span data-ttu-id="10a50-120">Lägg till VmssId i New-AzVMConfig-cmdleten</span><span class="sxs-lookup"><span data-stu-id="10a50-120">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="10a50-121">Lägg till parametrarna TerminateScheduledEvents och TerminateScheduledEventNotBeforeTimeoutInMinutes i New-AzVmssConfig och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="10a50-121">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="10a50-122">Lägg till egenskapen HyperVGeneration till avbildningsobjekt för virtuell dator</span><span class="sxs-lookup"><span data-stu-id="10a50-122">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="10a50-123">Lägg till funktioner för Host och HostGroup</span><span class="sxs-lookup"><span data-stu-id="10a50-123">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="10a50-124">Nya cmdletar:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="10a50-124">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="10a50-125">HostId-parametern läggs till i New-AzVMConfig och New-AzVM</span><span class="sxs-lookup"><span data-stu-id="10a50-125">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="10a50-126">Uppdatera exempel i "Invoke-AzVMRunCommand"-dokumentationen till att använda rätt parameternamn</span><span class="sxs-lookup"><span data-stu-id="10a50-126">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="10a50-127">Uppdatera "-VolumeType"-beskrivningen i referensdokumentationen för "set-AzVMDiskEncryptionExtension" och "set-AzVmssDiskEncryptionExtension"</span><span class="sxs-lookup"><span data-stu-id="10a50-127">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="10a50-128">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="10a50-128">Az.DataFactory</span></span>
* <span data-ttu-id="10a50-129">Åtgärda skrivfel till att använda versaler för "Windows" i "New-AzDataFactoryEncryptValue"-dokumentationen</span><span class="sxs-lookup"><span data-stu-id="10a50-129">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="10a50-130">Uppdaterade ADF .Net SDK-versionen till 4.1.2</span><span class="sxs-lookup"><span data-stu-id="10a50-130">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="10a50-131">Lägg till parametrarna "DataProxyIntegrationRuntimeName", "DataProxyStagingLinkedServiceName" och "DataProxyStagingPath" för "Set-AzureRmDataFactoryV2IntegrationRuntime"-cmd för att aktivera konfiguration av lokalt installerad integrationskörning som en proxy för SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="10a50-131">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="10a50-132">Uppdaterade PSTriggerRun till att visa utlöst pipeline, meddelande och egenskaper samt PSActivityRun till att visa aktivitetstypen</span><span class="sxs-lookup"><span data-stu-id="10a50-132">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="10a50-133">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="10a50-133">Az.DataLakeStore</span></span>
* <span data-ttu-id="10a50-134">Korrigering av frysning av Get-DataLakeStoreDeletedItem för fel eller fjärrundantag.</span><span class="sxs-lookup"><span data-stu-id="10a50-134">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="10a50-135">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="10a50-135">Az.EventHub</span></span>
* <span data-ttu-id="10a50-136">Korrigering av problem #9658 : Skrivfel i parametern VirtualNteworkRule i Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="10a50-136">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="10a50-137">Korrigering av problem #9558 : Set-AzEventHubNamespace använder PATCH i stället för PUT</span><span class="sxs-lookup"><span data-stu-id="10a50-137">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="10a50-138">lade till parametern EnableKafka i Set-AzEventHubNamespace-cmdleten</span><span class="sxs-lookup"><span data-stu-id="10a50-138">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="10a50-139">Korrigering av problem #9786 : kan inte skapa en regel med Endast lyssna-behörighet</span><span class="sxs-lookup"><span data-stu-id="10a50-139">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="10a50-140">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="10a50-140">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="10a50-141">Åtgärdade skrivfel i dokumentation där "Azure" skrevs helt med gemener</span><span class="sxs-lookup"><span data-stu-id="10a50-141">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="10a50-142">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="10a50-142">Az.Monitor</span></span>
* <span data-ttu-id="10a50-143">Åtgärdade felaktigt parameternamn i hjälpdokumentationen</span><span class="sxs-lookup"><span data-stu-id="10a50-143">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="10a50-144">Az.Network</span><span class="sxs-lookup"><span data-stu-id="10a50-144">Az.Network</span></span>
* <span data-ttu-id="10a50-145">Uppdaterade New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="10a50-145">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="10a50-146">Gjorde parametern "PublicIpAddress" inaktuell eftersom den aldrig används på serversidan.</span><span class="sxs-lookup"><span data-stu-id="10a50-146">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="10a50-147">Lade till den valfria parametern "Primary", som anger huruvida den aktuella IP-konfigurationen är den primära.</span><span class="sxs-lookup"><span data-stu-id="10a50-147">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="10a50-148">Förbättrade hanteringen av felundantag för begärande från SDK – åtgärdar problemet att tidigare SDK-undantag inte hanteras på rätt sätt, vilket leder till att viktig felinformation inte visas</span><span class="sxs-lookup"><span data-stu-id="10a50-148">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="10a50-149">Justerade valideringslogiken för IPv6-IP-prefix till att kontrollera korrekt IPv6-prefixlängd.</span><span class="sxs-lookup"><span data-stu-id="10a50-149">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="10a50-150">Uppdaterade Get-AzVirtualNetworkSubnetConfig: Lade till parameter som anges till get av undernätets resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="10a50-150">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="10a50-151">Uppdaterade beskrivningen av parametern Location för AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="10a50-151">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="10a50-152">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="10a50-152">Az.OperationalInsights</span></span>
* <span data-ttu-id="10a50-153">Uppdaterade dokumentation för "New-AzOperationalInsightsLinuxSyslogDataSource"</span><span class="sxs-lookup"><span data-stu-id="10a50-153">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="10a50-154">Lade till exempel</span><span class="sxs-lookup"><span data-stu-id="10a50-154">Added example</span></span>
    - <span data-ttu-id="10a50-155">Uppdaterade beskrivningen av parametern "-Name"</span><span class="sxs-lookup"><span data-stu-id="10a50-155">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="10a50-156">Lade till ett exempel för New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="10a50-156">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="10a50-157">Ändrade beskrivningen av parametern -Name för New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="10a50-157">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="10a50-158">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="10a50-158">Az.RecoveryServices</span></span>
* <span data-ttu-id="10a50-159">Uppdatera "Get-AzRecoveryServicesBackupJobDetail.md"</span><span class="sxs-lookup"><span data-stu-id="10a50-159">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="10a50-160">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="10a50-160">Az.Resources</span></span>
* <span data-ttu-id="10a50-161">Lägg till stöd för den nya API-versionen från 2019-05-10 för Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="10a50-161">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="10a50-162">Lägg till stöd för "copy.count = 0" för variabler, resurser och egenskaper</span><span class="sxs-lookup"><span data-stu-id="10a50-162">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="10a50-163">Resurser med "condition = false" eller "copy.count = 0" tas bort i complete-läget</span><span class="sxs-lookup"><span data-stu-id="10a50-163">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="10a50-164">Lägg till ett exempel på tilldelning av princip på prenumerationsnivå i hjälpdokumentationen</span><span class="sxs-lookup"><span data-stu-id="10a50-164">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="10a50-165">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="10a50-165">Az.ServiceBus</span></span>
* <span data-ttu-id="10a50-166">Korrigering av problem #9658 : Skrivfel i parametern VirtualNetworkRule i set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="10a50-166">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="10a50-167">Korrigering av problem #9786 : kan inte skapa en regel med Endast lyssna-behörighet</span><span class="sxs-lookup"><span data-stu-id="10a50-167">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="10a50-168">Lade till det nya kommandot "Test-AzServiceBusNameAvailability" för att kontrollera namntillgängligheten för kö och ämne</span><span class="sxs-lookup"><span data-stu-id="10a50-168">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="10a50-169">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="10a50-169">Az.ServiceFabric</span></span>
* <span data-ttu-id="10a50-170">Åtgärda buggar med tillägg av nodtyps-cmdlet:</span><span class="sxs-lookup"><span data-stu-id="10a50-170">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="10a50-171">NullReferenceException-bugg när resursgrupp hade annan vmss som inte är relaterad till Service Fabric-klustret.</span><span class="sxs-lookup"><span data-stu-id="10a50-171">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="10a50-172">Åtgärdar problemet: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="10a50-172">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="10a50-173">Åtgärda bugg där cmdleten misslyckades om virtualNetwork var i en annan resursgrupp än klustret.</span><span class="sxs-lookup"><span data-stu-id="10a50-173">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="10a50-174">Åtgärdar problemet: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="10a50-174">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="10a50-175">AzServiceFabricApplicationCertificate-cmdleten görs inaktuell</span><span class="sxs-lookup"><span data-stu-id="10a50-175">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="10a50-176">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="10a50-176">Az.Sql</span></span>
* <span data-ttu-id="10a50-177">Uppdatera dokumentation om gamla gransknings-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="10a50-177">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="10a50-178">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="10a50-178">Az.Storage</span></span>
* <span data-ttu-id="10a50-179">Uppdatera hjälpen för Get/Close-AzStorageFileHandle genom att lägga till fler scenarier i cmdlet-exempel och uppdatera parameterbeskrivningar</span><span class="sxs-lookup"><span data-stu-id="10a50-179">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="10a50-180">Stöd för StandardBlobTier i uppladdningsblob och kopieringsblob</span><span class="sxs-lookup"><span data-stu-id="10a50-180">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="10a50-181">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="10a50-181">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="10a50-182">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="10a50-182">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="10a50-183">Stöd för rehydratiseringsprioritet i kopieringsblob</span><span class="sxs-lookup"><span data-stu-id="10a50-183">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="10a50-184">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="10a50-184">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="10a50-185">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="10a50-185">Az.Websites</span></span>
* <span data-ttu-id="10a50-186">Lägg till klargöranden gällande parametern -AppSettings i Set-AzWebApp och Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="10a50-186">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="10a50-187">2.5.0 – July 2019</span><span class="sxs-lookup"><span data-stu-id="10a50-187">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="10a50-188">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="10a50-188">Az.Accounts</span></span>
* <span data-ttu-id="10a50-189">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="10a50-189">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="10a50-190">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="10a50-190">Az.ApplicationInsights</span></span>
* <span data-ttu-id="10a50-191">Korrigera skrivfel i exempel i dokumentationen för Remove-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="10a50-191">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="10a50-192">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="10a50-192">Az.Automation</span></span>
* <span data-ttu-id="10a50-193">Korrigera skrivfel i resurssträng</span><span class="sxs-lookup"><span data-stu-id="10a50-193">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="10a50-194">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="10a50-194">Az.CognitiveServices</span></span>
* <span data-ttu-id="10a50-195">Stöd för NetworkRuleSet har lagts till.</span><span class="sxs-lookup"><span data-stu-id="10a50-195">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="10a50-196">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="10a50-196">Az.Compute</span></span>
* <span data-ttu-id="10a50-197">Lägg till saknade egenskaper (ComputerName, OsName, OsVersion och HyperVGeneration) för visningsobjekt i den virtuella datorinstansen.</span><span class="sxs-lookup"><span data-stu-id="10a50-197">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="10a50-198">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="10a50-198">Az.ContainerRegistry</span></span>
* <span data-ttu-id="10a50-199">Åtgärda skrivfel i Remove-AzContainerRegistryReplication för parametern Replication</span><span class="sxs-lookup"><span data-stu-id="10a50-199">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="10a50-200">Mer information finns här: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="10a50-200">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="10a50-201">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="10a50-201">Az.DataFactory</span></span>
* <span data-ttu-id="10a50-202">ADF .Net SDK-versionen har uppdaterats till 4.1.0</span><span class="sxs-lookup"><span data-stu-id="10a50-202">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="10a50-203">Korrigera skrivfel i dokumentationen för Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="10a50-203">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="10a50-204">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="10a50-204">Az.EventHub</span></span>
* <span data-ttu-id="10a50-205">Ny cmmdlet har lagts till för att skapa SAS-token: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="10a50-205">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="10a50-206">verifierings- och felmeddelande har lagts till för authorizationrules-rättigheter om endast "hantera" har tilldelats</span><span class="sxs-lookup"><span data-stu-id="10a50-206">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="10a50-207">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="10a50-207">Az.KeyVault</span></span>
* <span data-ttu-id="10a50-208">Stöd har lagts till för att ange KeySize för certifikatprinciper</span><span class="sxs-lookup"><span data-stu-id="10a50-208">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="10a50-209">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="10a50-209">Az.LogicApp</span></span>
* <span data-ttu-id="10a50-210">Korrigering för Get-AzIntegrationAccountMap för att lista alla mappningstyper</span><span class="sxs-lookup"><span data-stu-id="10a50-210">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="10a50-211">Ny MapType-parameter har lagts till för filtrering</span><span class="sxs-lookup"><span data-stu-id="10a50-211">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="10a50-212">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="10a50-212">Az.ManagedServices</span></span>
* <span data-ttu-id="10a50-213">Stöd för API-versionen 2019-06-01 (GA) har lagts till</span><span class="sxs-lookup"><span data-stu-id="10a50-213">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="10a50-214">Az.Network</span><span class="sxs-lookup"><span data-stu-id="10a50-214">Az.Network</span></span>
* <span data-ttu-id="10a50-215">Lägg till stöd för privat slutpunkt och privat länktjänst</span><span class="sxs-lookup"><span data-stu-id="10a50-215">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="10a50-216">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="10a50-216">New cmdlets</span></span>
        - <span data-ttu-id="10a50-217">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="10a50-217">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="10a50-218">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="10a50-218">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="10a50-219">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="10a50-219">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="10a50-220">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="10a50-220">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="10a50-221">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="10a50-221">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="10a50-222">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="10a50-222">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="10a50-223">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="10a50-223">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="10a50-224">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="10a50-224">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="10a50-225">Nedanstående kommandon för funktionen har uppdaterats: Flaggan PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies på undernätet i VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="10a50-225">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="10a50-226">Uppdaterade New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="10a50-226">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="10a50-227">Valfri parameter -PrivateEndpointNetworkPoliciesFlag har lagts till för att indikera aktivering eller inaktivering av Tillämpa nätverksprinciper på privat slutpunkt i det här undernätet.</span><span class="sxs-lookup"><span data-stu-id="10a50-227">Added optional parameter -PrivateEndpointNetworkPoliciesFlag to indicate that enable or disable apply network policies on pivate endpoint in this subnet.</span></span>
        - <span data-ttu-id="10a50-228">Valfri parameter -PrivateEndpointNetworkPoliciesFlag har lagts till för att indikera aktivering eller inaktivering av Tillämpa nätverksprinciper på privat länktjänst i det här undernätet.</span><span class="sxs-lookup"><span data-stu-id="10a50-228">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag to indicate that enable or disable apply network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="10a50-229">AzPrivateLinkService för cmdlet-parametern ServiceName har bytt namn till Name med aliaset ServiceName för bakåtkompatibilitet</span><span class="sxs-lookup"><span data-stu-id="10a50-229">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="10a50-230">Aktivera ICMP-protokoll för konfiguration av nätverkssäkerhetsregler</span><span class="sxs-lookup"><span data-stu-id="10a50-230">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="10a50-231">Uppdaterade cmdletar</span><span class="sxs-lookup"><span data-stu-id="10a50-231">Updated cmdlets</span></span>
        - <span data-ttu-id="10a50-232">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="10a50-232">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="10a50-233">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="10a50-233">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="10a50-234">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="10a50-234">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="10a50-235">Lägg till ConnectionProtocolType (Ikev1/Ikev2) som en konfigurerbar parameter för New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="10a50-235">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="10a50-236">Lägg till PrivateIpAddressVersion i LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="10a50-236">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="10a50-237">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="10a50-237">Updated cmdlet:</span></span>
        - <span data-ttu-id="10a50-238">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="10a50-238">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="10a50-239">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="10a50-239">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="10a50-240">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="10a50-240">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="10a50-241">Uppdatering av Application Gateway-kommandot New-AzApplicationGatewayProbeConfig för stöd av anpassad port i Probe</span><span class="sxs-lookup"><span data-stu-id="10a50-241">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="10a50-242">Uppdaterade New-AzApplicationGatewayProbeConfig: Den valfria parametern Port som används för avsökning i serverdelen har lagts till.</span><span class="sxs-lookup"><span data-stu-id="10a50-242">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="10a50-243">Denna parameter gäller för SKU:erna Standard_V2 och WAF_V2.</span><span class="sxs-lookup"><span data-stu-id="10a50-243">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="10a50-244">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="10a50-244">Az.OperationalInsights</span></span>
* <span data-ttu-id="10a50-245">Uppdaterade standardversionen för sparade sökningar till 1.</span><span class="sxs-lookup"><span data-stu-id="10a50-245">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="10a50-246">Åtgärdade hantering av anpassad log null regex</span><span class="sxs-lookup"><span data-stu-id="10a50-246">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="10a50-247">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="10a50-247">Az.RecoveryServices</span></span>
* <span data-ttu-id="10a50-248">Uppdatera Get-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="10a50-248">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="10a50-249">Uppdatera Get-AzRecoveryServicesBackupContainer.md</span><span class="sxs-lookup"><span data-stu-id="10a50-249">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="10a50-250">Uppdatera Get-AzRecoveryServicesVault.md</span><span class="sxs-lookup"><span data-stu-id="10a50-250">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="10a50-251">Uppdatera Wait-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="10a50-251">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="10a50-252">Uppdatera Set-AzRecoveryServicesVaultContext.md</span><span class="sxs-lookup"><span data-stu-id="10a50-252">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="10a50-253">Uppdatera Get-AzRecoveryServicesBackupItem.md</span><span class="sxs-lookup"><span data-stu-id="10a50-253">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="10a50-254">Uppdatera Get-AzRecoveryServicesBackupRecoveryPoint.md</span><span class="sxs-lookup"><span data-stu-id="10a50-254">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="10a50-255">Uppdatera Restore-AzRecoveryServicesBackupItem.md</span><span class="sxs-lookup"><span data-stu-id="10a50-255">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="10a50-256">Uppdaterat tjänstanrop för avregistrering av container för Azure-filresurs</span><span class="sxs-lookup"><span data-stu-id="10a50-256">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="10a50-257">Uppdatera Set-AzRecoveryServicesAsrAlertSetting.md</span><span class="sxs-lookup"><span data-stu-id="10a50-257">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="10a50-258">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="10a50-258">Az.Resources</span></span>
- <span data-ttu-id="10a50-259">Ta bort den cmdlet som saknas och som refereras i dokumentationen till New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="10a50-259">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="10a50-260">Princip-cmdletar har uppdaterats så att de använder den nya API-versionen 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="10a50-260">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="10a50-261">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="10a50-261">Az.ServiceBus</span></span>
* <span data-ttu-id="10a50-262">Ny cmmdlet har lagts till för att skapa SAS-token: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="10a50-262">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="10a50-263">verifierings- och felmeddelande har lagts till för authorizationrules-rättigheter om endast "hantera" har tilldelats</span><span class="sxs-lookup"><span data-stu-id="10a50-263">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="10a50-264">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="10a50-264">Az.Sql</span></span>
* <span data-ttu-id="10a50-265">Åtgärda saknade exempel för Set-AzSqlDatabaseSecondary cmdlet</span><span class="sxs-lookup"><span data-stu-id="10a50-265">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="10a50-266">Åtgärda angivna återkommande genomsökningar för bedömning av säkerhetsrisk utan angivna e-postadresser</span><span class="sxs-lookup"><span data-stu-id="10a50-266">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="10a50-267">Korrigera ett skrivfel i ett varningsmeddelande.</span><span class="sxs-lookup"><span data-stu-id="10a50-267">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="10a50-268">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="10a50-268">Az.Storage</span></span>
* <span data-ttu-id="10a50-269">Uppdatera exempel i referensdokumentationen för Get-AzStorageAccount så att rätt parameternamn används</span><span class="sxs-lookup"><span data-stu-id="10a50-269">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="10a50-270">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="10a50-270">Az.StorageSync</span></span>
* <span data-ttu-id="10a50-271">Lägger till cmdleten Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="10a50-271">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="10a50-272">Åtgärda problem 9551 så att TierFilesOlderThanDays föredras</span><span class="sxs-lookup"><span data-stu-id="10a50-272">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="10a50-273">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="10a50-273">Az.Websites</span></span>
* <span data-ttu-id="10a50-274">Åtgärdar ett fel där vissa SiteConfig-egenskaper inte returnerades av Get-AzWebApp och Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="10a50-274">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="10a50-275">Lägger till en ny platsparameter för Get-AzDeletedWebApp och Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="10a50-275">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="10a50-276">Åtgärdar ett fel i kloning av webbapp-platser som använder New-AzWebApp-IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="10a50-276">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="10a50-277">2.4.0 – juli 2019</span><span class="sxs-lookup"><span data-stu-id="10a50-277">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="10a50-278">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="10a50-278">Az.Accounts</span></span>
* <span data-ttu-id="10a50-279">Lägg till stöd för profil-cmdletar</span><span class="sxs-lookup"><span data-stu-id="10a50-279">Add support for profile cmdlets</span></span>
* <span data-ttu-id="10a50-280">Lägg till stöd för miljöer och dataplaner i genererade cmdletar</span><span class="sxs-lookup"><span data-stu-id="10a50-280">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="10a50-281">Åtgärda bugg där fel slutpunkt i vissa fall användes för cmdletar för dataplaner i Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="10a50-281">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="10a50-282">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="10a50-282">Az.Advisor</span></span>
* <span data-ttu-id="10a50-283">GA-version av Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="10a50-283">GA release of Az.Advisor</span></span>
* <span data-ttu-id="10a50-284">Den här modulen ingår nu som en del av `Az`-sammanslagningsmodulen</span><span class="sxs-lookup"><span data-stu-id="10a50-284">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="10a50-285">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="10a50-285">Az.ApiManagement</span></span>
* <span data-ttu-id="10a50-286">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="10a50-286">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="10a50-287">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="10a50-287">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="10a50-288">Stöd för att fråga prenumerationer efter användare och produkt har lagts till</span><span class="sxs-lookup"><span data-stu-id="10a50-288">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="10a50-289">Stöd för att fråga med hjälp av omfång ”/”, ”/apis”, ”/apis/echo-api” har lagts till</span><span class="sxs-lookup"><span data-stu-id="10a50-289">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="10a50-290">Korrigering av problem https://github.com/Azure/azure-powershell/issues/9307 och https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="10a50-290">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="10a50-291">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="10a50-291">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="10a50-292">Stöd för att ange ”ApiVersion” och ”ApiVersionSetId” när API:er importeras har lagts till</span><span class="sxs-lookup"><span data-stu-id="10a50-292">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="10a50-293">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="10a50-293">Az.Automation</span></span>
* <span data-ttu-id="10a50-294">Bugg med cmdleten Set-AzAutomationConnectionFieldValue för att hantera strängvärde har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="10a50-294">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="10a50-295">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="10a50-295">Az.Compute</span></span>
* <span data-ttu-id="10a50-296">Lägg till parametern HyperVGeneration i New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="10a50-296">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="10a50-297">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="10a50-297">Az.DataFactory</span></span>
* <span data-ttu-id="10a50-298">Uppdaterar utdata från ADF-cmdletar som hämtar aktivitetskörningar, hämtar pipelinekörningar och hämtar utlösarkörningar för stöd för Select-Object-pipe.</span><span class="sxs-lookup"><span data-stu-id="10a50-298">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="10a50-299">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="10a50-299">Az.EventGrid</span></span>
* <span data-ttu-id="10a50-300">Korrigera stavfel i dokumentation om ”New-AzEventGridSubscription”</span><span class="sxs-lookup"><span data-stu-id="10a50-300">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="10a50-301">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="10a50-301">Az.IotHub</span></span>
* <span data-ttu-id="10a50-302">Lägg till stöd för att återskapa principnycklar för auktorisering.</span><span class="sxs-lookup"><span data-stu-id="10a50-302">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="10a50-303">Az.Network</span><span class="sxs-lookup"><span data-stu-id="10a50-303">Az.Network</span></span>
* <span data-ttu-id="10a50-304">”RoutingPreference” har lagts till i offentliga IP-taggar</span><span class="sxs-lookup"><span data-stu-id="10a50-304">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="10a50-305">Förbättra exempel för referensdokumentation om ”Get-AzNetworkServiceTag”</span><span class="sxs-lookup"><span data-stu-id="10a50-305">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="10a50-306">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="10a50-306">Az.PolicyInsights</span></span>
* <span data-ttu-id="10a50-307">Åtgärda problem med null-referens i Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="10a50-307">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="10a50-308">Mer information här: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="10a50-308">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="10a50-309">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="10a50-309">Az.OperationalInsights</span></span>
* <span data-ttu-id="10a50-310">Modellen för CustomLog-datakälla som returneras i Get-AzOperationalInsightsDataSource har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="10a50-310">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="10a50-311">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="10a50-311">Az.RecoveryServices</span></span>
* <span data-ttu-id="10a50-312">Kommandot get-policy för IaaSVM:er har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="10a50-312">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="10a50-313">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="10a50-313">Az.Resources</span></span>
    - <span data-ttu-id="10a50-314">Korrigera hjälptext för den översta parametern i Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="10a50-314">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="10a50-315">Lägg till växlingsstöd på klientsidan för Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="10a50-315">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="10a50-316">Lägg till nya parametrar för Set-AzPolicyAssignment, -PolicyParameters och -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="10a50-316">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="10a50-317">En mängd dokument- och exempeluppdateringar för Policy-cmdletar</span><span class="sxs-lookup"><span data-stu-id="10a50-317">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="10a50-318">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="10a50-318">Az.ServiceBus</span></span>
* <span data-ttu-id="10a50-319">Korrigering av problem #4938 – New-AzureRmServiceBusQueue returnerar BadRequest vid konfiguration av MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="10a50-319">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="10a50-320">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="10a50-320">Az.Sql</span></span>
* <span data-ttu-id="10a50-321">Lägg till cmdletar för instansredundansgrupper från förhandsversion till offentlig version</span><span class="sxs-lookup"><span data-stu-id="10a50-321">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="10a50-322">Stöd för granskning för Azure SQL Server\Database med nya cmdletar.</span><span class="sxs-lookup"><span data-stu-id="10a50-322">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="10a50-323">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="10a50-323">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="10a50-324">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="10a50-324">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="10a50-325">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="10a50-325">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="10a50-326">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="10a50-326">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="10a50-327">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="10a50-327">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="10a50-328">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="10a50-328">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="10a50-329">Ta bort begränsningar för e-post från inställningarna för sårbarhetsbedömning</span><span class="sxs-lookup"><span data-stu-id="10a50-329">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="10a50-330">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="10a50-330">Az.Storage</span></span>
* <span data-ttu-id="10a50-331">Ändra två parametrar ”-IndexDocument” och ”-ErrorDocument404Path” från ”krävs” till ”valfri” i cmdlet:</span><span class="sxs-lookup"><span data-stu-id="10a50-331">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="10a50-332">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="10a50-332">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="10a50-333">Uppdatera hjälpen för Get-AzStorageBlobContent genom att lägga till ett exempel</span><span class="sxs-lookup"><span data-stu-id="10a50-333">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="10a50-334">Visa mer felinformation när cmdleten misslyckas med StorageException</span><span class="sxs-lookup"><span data-stu-id="10a50-334">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="10a50-335">Stöd för att skapa eller uppdatera lagringskonto med Azure Files AAD DS-autentisering</span><span class="sxs-lookup"><span data-stu-id="10a50-335">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="10a50-336">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="10a50-336">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="10a50-337">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="10a50-337">Set-AzStorageAccount</span></span>
* <span data-ttu-id="10a50-338">Stöd för att lista eller stänga filreferenser för en filresurs, filkatalog eller en fil</span><span class="sxs-lookup"><span data-stu-id="10a50-338">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="10a50-339">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="10a50-339">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="10a50-340">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="10a50-340">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="10a50-341">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="10a50-341">Az.StorageSync</span></span>
* <span data-ttu-id="10a50-342">Den här modulen ingår nu som en del av `Az`-sammanslagningsmodulen</span><span class="sxs-lookup"><span data-stu-id="10a50-342">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="10a50-343">2.3.2 – juni 2019</span><span class="sxs-lookup"><span data-stu-id="10a50-343">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="10a50-344">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="10a50-344">Az.Accounts</span></span>
* <span data-ttu-id="10a50-345">Åtgärda bugg med felaktiga webbadresser som i vissa fall användes för Functions-anrop</span><span class="sxs-lookup"><span data-stu-id="10a50-345">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="10a50-346">Mer information här: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="10a50-346">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="10a50-347">Åtgärda problem med alias från AzureRM i Az-cmdletar</span><span class="sxs-lookup"><span data-stu-id="10a50-347">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="10a50-348">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="10a50-348">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="10a50-349">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="10a50-349">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="10a50-350">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="10a50-350">Az.Compute</span></span>
* <span data-ttu-id="10a50-351">Parameteruppsättningarna New-AzVm och New-AzVmss accepterar nu parametern ”ProximityPlacementGroup”.</span><span class="sxs-lookup"><span data-stu-id="10a50-351">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="10a50-352">Stavfel i referensdokumentationen för ”New-AzVM” har korrigerats</span><span class="sxs-lookup"><span data-stu-id="10a50-352">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="10a50-353">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="10a50-353">Az.Dns</span></span>
* <span data-ttu-id="10a50-354">Stavfel i hjälpexempel för ”Set-AzDnsZone” har korrigerats.</span><span class="sxs-lookup"><span data-stu-id="10a50-354">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="10a50-355">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="10a50-355">Az.EventGrid</span></span>
* <span data-ttu-id="10a50-356">Har uppdaterats för att använda API-versionen 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="10a50-356">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="10a50-357">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="10a50-357">New cmdlets:</span></span>
    - <span data-ttu-id="10a50-358">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="10a50-358">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="10a50-359">Skapar en ny Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="10a50-359">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="10a50-360">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="10a50-360">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="10a50-361">Hämtar information om en Event Grid-domän eller hämtar en lista med alla Event Grid-domäner i den aktuella Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="10a50-361">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="10a50-362">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="10a50-362">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="10a50-363">Tar bort en Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="10a50-363">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="10a50-364">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="10a50-364">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="10a50-365">Återskapar nyckeln för delad åtkomst för en Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="10a50-365">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="10a50-366">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="10a50-366">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="10a50-367">Hämtar de nycklar för delad åtkomst som används för att publicera händelser till en Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="10a50-367">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="10a50-368">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="10a50-368">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="10a50-369">Skapar ett nytt Azure Event Grid-domänämne.</span><span class="sxs-lookup"><span data-stu-id="10a50-369">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="10a50-370">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="10a50-370">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="10a50-371">Hämtar information om ett Event Grid-domänämne eller hämtar en lista med alla Event Grid-domänämnen under en specifik Event Grid-domän i nuvarande Azure</span><span class="sxs-lookup"><span data-stu-id="10a50-371">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="10a50-372">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="10a50-372">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="10a50-373">Tar bort ett befintligt Azure Event Grid-domänämne.</span><span class="sxs-lookup"><span data-stu-id="10a50-373">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="10a50-374">Uppdaterade cmdletar:</span><span class="sxs-lookup"><span data-stu-id="10a50-374">Updated cmdlets:</span></span>
    - <span data-ttu-id="10a50-375">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="10a50-375">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="10a50-376">Lägg till nya obligatoriska parametrar för att stödja piping för den nya Event Grid-domänen och Event Grid-domänämnet för att göra det möjligt att skapa nya händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="10a50-376">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="10a50-377">Lägg till nya obligatoriska parametrar för att ange det nya Event Grid-domännamnet och/eller namnet på Event Grid-domänämnet för att göra det möjligt att skapa nya händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="10a50-377">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="10a50-378">Lägg till ny parameteruppsättningar för domäner och domänämnen för att göra det möjligt att återanvända befintliga parametrar (t.ex. EndPointType, SubjectBeginsWith osv).</span><span class="sxs-lookup"><span data-stu-id="10a50-378">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="10a50-379">Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="10a50-379">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="10a50-380">Förfallodatum för händelseprenumeration</span><span class="sxs-lookup"><span data-stu-id="10a50-380">Event subscription expiration date,</span></span>
            - <span data-ttu-id="10a50-381">Avancerade filterparametrar.</span><span class="sxs-lookup"><span data-stu-id="10a50-381">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="10a50-382">Lägg till ny uppräkning för servicebusqueue som mål.</span><span class="sxs-lookup"><span data-stu-id="10a50-382">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="10a50-383">Tillåt inte användning av ”Alla” i alternativet -IncludedEventType och ersätt det med</span><span class="sxs-lookup"><span data-stu-id="10a50-383">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="10a50-384">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="10a50-384">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="10a50-385">Lägg till ny valfria parametrar (Top, ODataQuery och NextLink) för att stödja sidnumrering och filtrering av resultat.</span><span class="sxs-lookup"><span data-stu-id="10a50-385">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="10a50-386">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="10a50-386">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="10a50-387">Lägg till nya obligatoriska parametrar för att stödja piping för en Event Grid-domän och Event Grid-domänämnen för att göra det möjligt att ta bort befintliga händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="10a50-387">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="10a50-388">Lägg till nya obligatoriska parametrar för att ange Event Grid-domännamnet och/eller namnet på Event Grid-domänämnet för att göra det möjligt att ta bort befintliga händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="10a50-388">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="10a50-389">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="10a50-389">Az.FrontDoor</span></span>
* <span data-ttu-id="10a50-390">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="10a50-390">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="10a50-391">Lägg till stöd för transformeringar och nytt värde för automatisk komplettering för operatorer (RegEx)</span><span class="sxs-lookup"><span data-stu-id="10a50-391">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="10a50-392">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="10a50-392">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="10a50-393">Lägg till nya värden för automatisk komplettering</span><span class="sxs-lookup"><span data-stu-id="10a50-393">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="10a50-394">Az.Network</span><span class="sxs-lookup"><span data-stu-id="10a50-394">Az.Network</span></span>
* <span data-ttu-id="10a50-395">Lägg till stöd för resurs för virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="10a50-395">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="10a50-396">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="10a50-396">New cmdlets</span></span>
        - <span data-ttu-id="10a50-397">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="10a50-397">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="10a50-398">Lägg till AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="10a50-398">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="10a50-399">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="10a50-399">New cmdlets</span></span> 
        - <span data-ttu-id="10a50-400">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="10a50-400">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="10a50-401">Lägg till PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="10a50-401">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="10a50-402">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="10a50-402">New cmdlets</span></span> 
        - <span data-ttu-id="10a50-403">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="10a50-403">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="10a50-404">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="10a50-404">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="10a50-405">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="10a50-405">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="10a50-406">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="10a50-406">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="10a50-407">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="10a50-407">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="10a50-408">Lägg till PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="10a50-408">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="10a50-409">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="10a50-409">New cmdlets</span></span>
        - <span data-ttu-id="10a50-410">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="10a50-410">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="10a50-411">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="10a50-411">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="10a50-412">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="10a50-412">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="10a50-413">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="10a50-413">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="10a50-414">Nedanstående kommandon för funktionen har uppdaterats: Flaggan UseLocalAzureIpAddress på VpnConnection</span><span class="sxs-lookup"><span data-stu-id="10a50-414">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="10a50-415">New-AzVpnConnection har uppdaterats: Den valfria parametern -UseLocalAzureIpAddress har lagts till för att visa att en lokal IP-adress i Azure ska användas som källadress när anslutningen initieras.</span><span class="sxs-lookup"><span data-stu-id="10a50-415">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="10a50-416">Set-AzVpnConnection har uppdaterats: Den valfria parametern -UseLocalAzureIpAddress har lagts till för att visa att en lokal IP-adress i Azure ska användas som källadress när anslutningen initieras.</span><span class="sxs-lookup"><span data-stu-id="10a50-416">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="10a50-417">Det skrivskyddade fältet PeeredConnections har lagts till i ExpressRoute-peering.</span><span class="sxs-lookup"><span data-stu-id="10a50-417">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="10a50-418">Det skrivskyddade fältet GlobalReachEnabled har lagts till i ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="10a50-418">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="10a50-419">Ett attribut för icke-bakåtkompatibla ändringar har lagts till för att lyfta fram utfasning av fältet AllowGlobalReach i modellen ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="10a50-419">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="10a50-420">Problem 8756 har åtgärdats: Fel vid användning av TargetListenerID med AzApplicationGatewayRedirectConfiguration-cmdletar</span><span class="sxs-lookup"><span data-stu-id="10a50-420">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="10a50-421">En bugg i New-AzApplicationGatewayPathRuleConfig som gjorde att regeluppsättningen för att återskapa inte kunde anges har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="10a50-421">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="10a50-422">Visningen av VirtualNetworkTaps i NetworkInterfaceIpConfiguration har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="10a50-422">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="10a50-423">Cortex Get-cmdletar för att visa en lista med alla delar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="10a50-423">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="10a50-424">Funktionen för att skapa VirtualHub-referenser för ExpressRouteGateways och VpnGateway har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="10a50-424">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="10a50-425">Stöd för tillgänglighetszoner i AzureFirewall och NatGateway har lagts till</span><span class="sxs-lookup"><span data-stu-id="10a50-425">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="10a50-426">Cmdleten Get-AzNetworkServiceTag har lagts till</span><span class="sxs-lookup"><span data-stu-id="10a50-426">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="10a50-427">Lägg till stöd för flera offentliga IP-adresser för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="10a50-427">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="10a50-428">Cmdleten New-AzFirewall har uppdaterats:</span><span class="sxs-lookup"><span data-stu-id="10a50-428">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="10a50-429">Parametern -PublicIpAddress som accepterar ett eller flera offentliga IP-adressobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="10a50-429">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="10a50-430">Parametern -VirtualNetwork som accepterar ett virtuellt nätverksobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="10a50-430">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="10a50-431">Metoderna AddPublicIpAddress och RemovePublicIpAddress har lagts till på brandväggsobjekt – dessa accepterar ett offentligt IP-adressobjekt som indata</span><span class="sxs-lookup"><span data-stu-id="10a50-431">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="10a50-432">Inaktuella parametrar -PublicIpName och -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="10a50-432">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="10a50-433">Nedanstående kommandon för funktionen har uppdaterats: Ange autentiseringsalternativ för VpnClient AAD till resurser för virtuella nätverksgatewayer.</span><span class="sxs-lookup"><span data-stu-id="10a50-433">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="10a50-434">New-AzVirtualNetworkGateway har uppdaterats: De valfria parametrarna AadTenantUri, AadAudienceId och AadIssuerUri för att ange VpnClient AAD-autentiseringsalternativ på en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="10a50-434">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="10a50-435">Set-AzVirtualNetworkGateway har uppdaterats: De valfria parametrarna AadTenantUri, AadAudienceId och AadIssuerUri för att ange VpnClient AAD-autentiseringsalternativ på en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="10a50-435">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="10a50-436">Set-AzVirtualNetworkGateway har uppdaterats: Den valfria växelparametern RemoveAadAuthentication som tar bort VpnClient AAD-autentiseringsalternativ från en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="10a50-436">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="10a50-437">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="10a50-437">Az.OperationalInsights</span></span>
* <span data-ttu-id="10a50-438">Aktivera prisnivån **pergb2018** i kommandot ”New-AzureRmOperationalInsightsWorkspace”</span><span class="sxs-lookup"><span data-stu-id="10a50-438">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="10a50-439">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="10a50-439">Az.Resources</span></span>
* <span data-ttu-id="10a50-440">Stöd för ytterligare alternativ för att exportera en mall</span><span class="sxs-lookup"><span data-stu-id="10a50-440">Support for additional Template Export options</span></span>
    - <span data-ttu-id="10a50-441">Lägg till parametern ”-SkipResourceNameParameterization” till Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="10a50-441">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="10a50-442">Lägg till parametern ”-SkipAllParameterization” till Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="10a50-442">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="10a50-443">Lägg till parametern ”-Resource” till Export-AzResourceGroup för exporterad resursfiltrering</span><span class="sxs-lookup"><span data-stu-id="10a50-443">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="10a50-444">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="10a50-444">Az.ServiceFabric</span></span>
* <span data-ttu-id="10a50-445">Åtgärda att fel tumavtryck används vid tilläggning av certifikat i ByExistingKeyVault i vissa fall</span><span class="sxs-lookup"><span data-stu-id="10a50-445">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="10a50-446">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="10a50-446">Az.Sql</span></span>
* <span data-ttu-id="10a50-447">Åtgärda suffix för lagringsslutpunkt i Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="10a50-447">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="10a50-448">Åtgärda att aktivering av Advanced Data Security åsidosätter Advanced Threat Protection-princip</span><span class="sxs-lookup"><span data-stu-id="10a50-448">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="10a50-449">Nya cmdletar för Management.Sql som gör att kunderna kan lägga till nycklar för transparent datakryptering (TDE) och ange TDE-skydd för hanterade instanser</span><span class="sxs-lookup"><span data-stu-id="10a50-449">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="10a50-450">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="10a50-450">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="10a50-451">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="10a50-451">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="10a50-452">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="10a50-452">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="10a50-453">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="10a50-453">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="10a50-454">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="10a50-454">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="10a50-455">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="10a50-455">Az.Storage</span></span>
* <span data-ttu-id="10a50-456">Stöd för typerna FileStorage och SkuName Premium_ZRS när lagringskonton skapas</span><span class="sxs-lookup"><span data-stu-id="10a50-456">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="10a50-457">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="10a50-457">New-AzStorageAccount</span></span>
* <span data-ttu-id="10a50-458">Beskrivningen av cmdleten för bloboföränderlighet har förtydligats</span><span class="sxs-lookup"><span data-stu-id="10a50-458">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="10a50-459">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="10a50-459">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="10a50-460">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="10a50-460">Az.Websites</span></span>
* <span data-ttu-id="10a50-461">Optimerar Get-AzWebAppCertificate för att filtrera efter resursgrupp på servern i stället för klienten</span><span class="sxs-lookup"><span data-stu-id="10a50-461">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="10a50-462">Lägger till växlingsparametern -UseDisasterRecovery till Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="10a50-462">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="10a50-463">2.2.0 – juni 2019</span><span class="sxs-lookup"><span data-stu-id="10a50-463">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="10a50-464">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="10a50-464">Az.Cdn</span></span>
* <span data-ttu-id="10a50-465">Uppdaterade cmdletar för att ge stöd för rulesEngine-funktion baserat på API-version 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="10a50-465">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="10a50-466">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="10a50-466">Az.Compute</span></span>
* <span data-ttu-id="10a50-467">Lade till parameter `NoWait` som startar åtgärden och returnerar omedelbart, innan åtgärden har slutförts.</span><span class="sxs-lookup"><span data-stu-id="10a50-467">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="10a50-468">Uppdaterade cmdletar:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="10a50-468">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="10a50-469">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="10a50-469">Az.EventHub</span></span>
* <span data-ttu-id="10a50-470">Korrigering för #9231 – Get-AzEventHubNamespace returnerar inga taggar</span><span class="sxs-lookup"><span data-stu-id="10a50-470">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="10a50-471">Korrigering för #9230 – Get-AzEventHubNamespace returnerar ResourceGroup istället för ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10a50-471">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="10a50-472">Az.Network</span><span class="sxs-lookup"><span data-stu-id="10a50-472">Az.Network</span></span>
* <span data-ttu-id="10a50-473">Uppdatera ResourceId och InputObject för NAT-gateway</span><span class="sxs-lookup"><span data-stu-id="10a50-473">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="10a50-474">Lägg till alias för ResourceId och InputObject</span><span class="sxs-lookup"><span data-stu-id="10a50-474">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="10a50-475">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="10a50-475">Az.PolicyInsights</span></span>
* <span data-ttu-id="10a50-476">Åtgärda Null-referensproblem i Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="10a50-476">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="10a50-477">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="10a50-477">Az.RecoveryServices</span></span>
* <span data-ttu-id="10a50-478">Minsta kvarhållning för IaaSVM-policy i dagar ändrat till 7 från 1</span><span class="sxs-lookup"><span data-stu-id="10a50-478">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="10a50-479">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="10a50-479">Az.ServiceBus</span></span>
* <span data-ttu-id="10a50-480">Korrigering för ärende #9182 – Get-AzServiceBusNamespace returnerar ResourceGroup istället för ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10a50-480">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="10a50-481">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="10a50-481">Az.ServiceFabric</span></span>
* <span data-ttu-id="10a50-482">Åtgärda stavfel i felmeddelandet för Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="10a50-482">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="10a50-483">Åtgärda saknat tecken i Service Fabric-kommandorader</span><span class="sxs-lookup"><span data-stu-id="10a50-483">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="10a50-484">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="10a50-484">Az.Sql</span></span>
* <span data-ttu-id="10a50-485">Lägg till parametern DnsZonePartner för New-AzureSqlInstance-cmdlet för att ge stöd för AutoDr för hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="10a50-485">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="10a50-486">Avvecklar cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="10a50-486">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="10a50-487">Döp om cmdletar för hotidentifiering till Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="10a50-487">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="10a50-488">Parametrarna New-AzSqlInstance -StorageSizeInGB och -LicenseType är nu valfria.</span><span class="sxs-lookup"><span data-stu-id="10a50-488">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="10a50-489">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="10a50-489">Az.Websites</span></span>
* <span data-ttu-id="10a50-490">åtgärdar problemet där användningen av Set-AzWebApp och Set-AzWebAppSlot med -WebApp-egenskap tog bort taggarna</span><span class="sxs-lookup"><span data-stu-id="10a50-490">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="10a50-491">2.1.0 – maj 2019</span><span class="sxs-lookup"><span data-stu-id="10a50-491">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="10a50-492">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="10a50-492">Az.ApiManagement</span></span>
* <span data-ttu-id="10a50-493">Skapade nya cmdletar för att hantera diagnostik för global- och API-omfång</span><span class="sxs-lookup"><span data-stu-id="10a50-493">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="10a50-494">**Get-AzApiManagementDiagnostic** – Skaffa diagnostik konfigurerad för global- eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="10a50-494">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="10a50-495">**New-AzApiManagementDiagnostic** – Skapa ny diagnostik för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="10a50-495">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="10a50-496">**New-AzApiManagementHttpMessageDiagnostic** – Skapa diagnostikinställning om vilka rubriker som ska loggas och storleken på brödtextbyte</span><span class="sxs-lookup"><span data-stu-id="10a50-496">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="10a50-497">**New-AzApiManagementPipelineDiagnosticSetting** – Skapa diagnostikinställningar för inkommande/utgående HTTP-meddelanden till gatewayen.</span><span class="sxs-lookup"><span data-stu-id="10a50-497">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="10a50-498">**New-AzApiManagementSamplingSetting** – Skapa samplinginställningar för begäranden/svar för en diagnostik</span><span class="sxs-lookup"><span data-stu-id="10a50-498">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="10a50-499">**Remove-AzApiManagementDiagnostic** – Ta bort en diagnostikenhet för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="10a50-499">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="10a50-500">**Set-AzApiManagementDiagnostic** – Uppdatera en diagnostikenhet för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="10a50-500">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="10a50-501">Skapade nya cmdletar för hantering av cacheminne i ApiManagement-tjänsten</span><span class="sxs-lookup"><span data-stu-id="10a50-501">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="10a50-502">**Get-AzApiManagementCache** – Hämta information om cacheminnet som anges av identifierare eller alla cacheminnen</span><span class="sxs-lookup"><span data-stu-id="10a50-502">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="10a50-503">**New-AzApiManagementCache** – Skapa ett nytt default-cacheminne eller cacheminne i en viss Azure-region</span><span class="sxs-lookup"><span data-stu-id="10a50-503">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="10a50-504">**Remove-AzApiManagementCache** – Ta bort ett cacheminne</span><span class="sxs-lookup"><span data-stu-id="10a50-504">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="10a50-505">**Remove-AzApiManagementCache** – Ta bort ett cacheminne</span><span class="sxs-lookup"><span data-stu-id="10a50-505">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="10a50-506">Skapade nya cmdletar för hantering av API-schema</span><span class="sxs-lookup"><span data-stu-id="10a50-506">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="10a50-507">**New-AzApiManagementSchema** – Skapa ett nytt schema för ett API</span><span class="sxs-lookup"><span data-stu-id="10a50-507">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="10a50-508">**Get-AzApiManagementSchema** – Hämta de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="10a50-508">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="10a50-509">**Remove-AzApiManagementSchema** – Ta bort de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="10a50-509">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="10a50-510">**Set-AzApiManagementSchema** – Uppdatera de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="10a50-510">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="10a50-511">Skapa ny cmdlet för att generera en användartoken.</span><span class="sxs-lookup"><span data-stu-id="10a50-511">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="10a50-512">**New-AzApiManagementUserToken** – Skapa en ny användartoken som enligt standardinställning är giltig i 8 timmar. Token för GIT-användaren kan skapas med den här cmdleten./</span><span class="sxs-lookup"><span data-stu-id="10a50-512">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="10a50-513">Skapade en ny cmdlet för att hämta nätverksstatus</span><span class="sxs-lookup"><span data-stu-id="10a50-513">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="10a50-514">**Get-AzApiManagementNetworkStatus** – Hämta nätverksstatusanslutningen för resurserna som API Management-tjänsten är beroende av.</span><span class="sxs-lookup"><span data-stu-id="10a50-514">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="10a50-515">Det här är användbart när du distribuerar ApiManagement-tjänsten i ett virtuellt nätverk och validerar om något beroende är brutet.</span><span class="sxs-lookup"><span data-stu-id="10a50-515">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="10a50-516">Uppdaterade cmdlet **New-AzApiManagement** för att hantera ApiManagement-tjänsten</span><span class="sxs-lookup"><span data-stu-id="10a50-516">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="10a50-517">Lade till stöd för den nya SKU:n Consumption</span><span class="sxs-lookup"><span data-stu-id="10a50-517">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="10a50-518">Aktiverade stöd för att slå på flaggan EnableClientCertificate för SKU:n Consumption</span><span class="sxs-lookup"><span data-stu-id="10a50-518">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="10a50-519">Den nya cmdleten **New-AzApiManagementSslSetting** gör det möjligt att ställa in TLS/SSL-inställningen på ”Backend” och ”Frontend” (serverdel och klientdel).</span><span class="sxs-lookup"><span data-stu-id="10a50-519">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="10a50-520">Det här kan också användas till att konfigurera chiffer som 3DES och ServerProtocols som Http2 för Frontend för en ApiManagement-tjänst.</span><span class="sxs-lookup"><span data-stu-id="10a50-520">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="10a50-521">Stöd har lagts till för att konfigurera värdnamnet DeveloperPortal på ApiManagement-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="10a50-521">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="10a50-522">Uppdaterade cmdletar **Get-AzApiManagementSsoToken** för att ta PsApiManagement-objekt som indata</span><span class="sxs-lookup"><span data-stu-id="10a50-522">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="10a50-523">Uppdaterad cmdleten för att visa infogade felmeddelanden</span><span class="sxs-lookup"><span data-stu-id="10a50-523">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="10a50-524">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Felkod: Felmeddelande av typen ValidationError: Ett eller flera fält innehåller felaktiga värden: Felinformation:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="10a50-524">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="10a50-525">Uppdaterade cmdlet **Export-AzApiManagementApi** för att exportera API:er i OpenApi 3.0-format</span><span class="sxs-lookup"><span data-stu-id="10a50-525">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="10a50-526">Uppdaterade cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="10a50-526">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="10a50-527">Importera API från dokumentspecifikationen OpenApi 3.0</span><span class="sxs-lookup"><span data-stu-id="10a50-527">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="10a50-528">Om du vill åsidosätta egenskapen PsApiManagementSchema specificerad i ett dokument (Swagger, Wadl, Wsdl, OpenApi).</span><span class="sxs-lookup"><span data-stu-id="10a50-528">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="10a50-529">Åsidosätta egenskapen ServiceUrl som specificeras i ett dokument.</span><span class="sxs-lookup"><span data-stu-id="10a50-529">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="10a50-530">Uppdaterade cmdlet **Get-AzApiManagementPolicy** för att returnera policy i undantaget format av typen icke-XML med rawxml</span><span class="sxs-lookup"><span data-stu-id="10a50-530">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="10a50-531">Uppdaterade cmdlet **Set-AzApiManagementPolicy** för att godkänna policy i undantaget format av typen icke-XML med rawxml och XML undantaget med xml</span><span class="sxs-lookup"><span data-stu-id="10a50-531">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="10a50-532">Uppdaterad cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="10a50-532">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="10a50-533">Konfigurera API med OpenId auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="10a50-533">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="10a50-534">Skapa ett API i ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="10a50-534">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="10a50-535">Klona ett API med SourceApiId och SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="10a50-535">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="10a50-536">Möjlighet att konfigurera SubscriptionRequired i API-omfattningen.</span><span class="sxs-lookup"><span data-stu-id="10a50-536">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="10a50-537">Uppdaterad cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="10a50-537">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="10a50-538">Konfigurera API med OpenId auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="10a50-538">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="10a50-539">Uppdatera ett API till ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="10a50-539">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="10a50-540">Möjlighet att konfigurera SubscriptionRequired i API-omfattningen.</span><span class="sxs-lookup"><span data-stu-id="10a50-540">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="10a50-541">Uppdaterad cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="10a50-541">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="10a50-542">Klona en befintlig version med hjälp av SourceApiRevision (kopiera taggar, produkter, åtgärder och principer).</span><span class="sxs-lookup"><span data-stu-id="10a50-542">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="10a50-543">Den nya revisionen antar ApiId från den överordnade instansen.</span><span class="sxs-lookup"><span data-stu-id="10a50-543">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="10a50-544">Tillhandahålla ApiRevisionDescription</span><span class="sxs-lookup"><span data-stu-id="10a50-544">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="10a50-545">Åsidosätta ServiceUrl vid kloning av ett API.</span><span class="sxs-lookup"><span data-stu-id="10a50-545">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="10a50-546">Uppdaterad cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="10a50-546">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="10a50-547">Konfigurera AAD eller AADB2C med en Authority</span><span class="sxs-lookup"><span data-stu-id="10a50-547">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="10a50-548">Konfigurera SignupPolicy, SigninPolicy, ProfileEditingPolicy och PasswordResetPolicy</span><span class="sxs-lookup"><span data-stu-id="10a50-548">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="10a50-549">Uppdaterad cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="10a50-549">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="10a50-550">Kompensera för ny SubscriptonModel med Scope och UserId</span><span class="sxs-lookup"><span data-stu-id="10a50-550">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="10a50-551">Kompensera för gammal prenumerationsmodell med ProductId och UserId</span><span class="sxs-lookup"><span data-stu-id="10a50-551">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="10a50-552">Lägg till funktion för att aktivera AllowTracing på prenumerationsnivå.</span><span class="sxs-lookup"><span data-stu-id="10a50-552">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="10a50-553">Uppdaterad cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="10a50-553">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="10a50-554">Kompensera för ny SubscriptonModel med Scope och UserId</span><span class="sxs-lookup"><span data-stu-id="10a50-554">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="10a50-555">Kompensera för gammal prenumerationsmodell med ProductId och UserId</span><span class="sxs-lookup"><span data-stu-id="10a50-555">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="10a50-556">Lägg till funktion för att aktivera AllowTracing på prenumerationsnivå.</span><span class="sxs-lookup"><span data-stu-id="10a50-556">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="10a50-557">Uppdaterade följande cmdletar för att acceptera ResourceId som indata</span><span class="sxs-lookup"><span data-stu-id="10a50-557">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="10a50-558">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="10a50-558">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="10a50-559">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="10a50-559">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="10a50-560">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="10a50-560">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="10a50-561">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="10a50-561">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="10a50-562">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="10a50-562">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="10a50-563">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="10a50-563">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="10a50-564">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="10a50-564">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="10a50-565">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="10a50-565">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="10a50-566">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="10a50-566">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="10a50-567">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="10a50-567">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="10a50-568">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="10a50-568">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="10a50-569">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="10a50-569">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="10a50-570">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="10a50-570">Az.Automation</span></span>
* <span data-ttu-id="10a50-571">Uppdaterade Get-AzAutomationJobOutputRecord för att hantera postvärden av typen JSON och Text.</span><span class="sxs-lookup"><span data-stu-id="10a50-571">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="10a50-572">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="10a50-572">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="10a50-573">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="10a50-573">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="10a50-574">Ändrade beteende för Start-AzAutomationDscCompilationJob till att bara starta jobbet istället för att vänta på slutförandet.</span><span class="sxs-lookup"><span data-stu-id="10a50-574">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="10a50-575">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="10a50-575">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="10a50-576">Korrigering för Get-AzAutomationDscNode när using -Name returnerar alla noder.</span><span class="sxs-lookup"><span data-stu-id="10a50-576">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="10a50-577">Nu returnerar den endast den matchande noden.</span><span class="sxs-lookup"><span data-stu-id="10a50-577">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="10a50-578">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="10a50-578">Az.Compute</span></span>
* <span data-ttu-id="10a50-579">Lägg till parametrarna ProtectFromScaleIn och ProtectFromScaleSetAction i cmdleten Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="10a50-579">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="10a50-580">Nu är standardinställningen att vimpelparametern New-AzVM använder en tillgänglig plats om USA, östra inte stöds</span><span class="sxs-lookup"><span data-stu-id="10a50-580">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="10a50-581">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="10a50-581">Az.DataLakeStore</span></span>
* <span data-ttu-id="10a50-582">Uppdatera ADLS-sdk för att använda httpclient, integrera dataplanstestning med Azure-ramverk</span><span class="sxs-lookup"><span data-stu-id="10a50-582">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="10a50-583">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="10a50-583">Az.Monitor</span></span>
* <span data-ttu-id="10a50-584">Korrigera felaktiga parameternamn i hjälpexempel</span><span class="sxs-lookup"><span data-stu-id="10a50-584">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="10a50-585">Az.Network</span><span class="sxs-lookup"><span data-stu-id="10a50-585">Az.Network</span></span>
* <span data-ttu-id="10a50-586">Lägg till flaggan DisableBgpRoutePropagation i utdata för effektiv routningstabell</span><span class="sxs-lookup"><span data-stu-id="10a50-586">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="10a50-587">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="10a50-587">Updated cmdlet:</span></span>
        - <span data-ttu-id="10a50-588">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="10a50-588">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="10a50-589">Åtgärda dubbelstreck i dokumentationen New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="10a50-589">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="10a50-590">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="10a50-590">Az.Resources</span></span>
* <span data-ttu-id="10a50-591">Lägg till ny cmdlet Get-AzureRmDenyAssignment för att hämta tilldelningsnekanden</span><span class="sxs-lookup"><span data-stu-id="10a50-591">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="10a50-592">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="10a50-592">Az.Sql</span></span>
* <span data-ttu-id="10a50-593">Döp om Advanced Threat Protection-cmdletar för Advanced Data Security och aktivera Vulnerability Assessment som standard</span><span class="sxs-lookup"><span data-stu-id="10a50-593">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="10a50-594">2.0.0 – maj 2019</span><span class="sxs-lookup"><span data-stu-id="10a50-594">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="10a50-595">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="10a50-595">Az.Accounts</span></span>
* <span data-ttu-id="10a50-596">Uppdatera autentiseringsbiblioteket för att åtgärda ADFS-problem med autentisering av användarnamn/lösenord</span><span class="sxs-lookup"><span data-stu-id="10a50-596">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="10a50-597">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="10a50-597">Az.CognitiveServices</span></span>
* <span data-ttu-id="10a50-598">Visa endast Bing-ansvarsfriskrivning för Bing-sökningstjänster.</span><span class="sxs-lookup"><span data-stu-id="10a50-598">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="10a50-599">Förbättra felmeddelande när det inte går att skapa konton.</span><span class="sxs-lookup"><span data-stu-id="10a50-599">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="10a50-600">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="10a50-600">Az.Compute</span></span>
* <span data-ttu-id="10a50-601">Funktion för närhetsplaceringsgrupper.</span><span class="sxs-lookup"><span data-stu-id="10a50-601">Proximity placement group feature.</span></span>
    - <span data-ttu-id="10a50-602">Följande nya cmdletar har lagts till:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="10a50-602">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="10a50-603">Den nya parametern ProximityPlacementGroupId har lagts till i följande cmdletar:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="10a50-603">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="10a50-604">Parametern StorageAccountType har lagts till i New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="10a50-604">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="10a50-605">TargetRegion för New-AzGalleryImageVersion kan innehålla StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="10a50-605">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="10a50-606">Växlingsparametern SkipShutdown har lagts till i Stop-AzVM och Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="10a50-606">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="10a50-607">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="10a50-607">Breaking changes</span></span>
    - <span data-ttu-id="10a50-608">Set-AzVMBootDiagnostics har ändrats till Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="10a50-608">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="10a50-609">Export-AzLogAnalyticThrottledRequests har ändrats till Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="10a50-609">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="10a50-610">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="10a50-610">Az.DeploymentManager</span></span>
* <span data-ttu-id="10a50-611">De första allmänt tillgängliga versionerna av cmdletar för Distributionshanteraren i Azure</span><span class="sxs-lookup"><span data-stu-id="10a50-611">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="10a50-612">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="10a50-612">Az.Dns</span></span>
* <span data-ttu-id="10a50-613">Automatisk delegering av DNS för NameServer</span><span class="sxs-lookup"><span data-stu-id="10a50-613">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="10a50-614">Det överordnade zonnamnet kan användas som ytterligare valfri parameter i cmdleten för att skapa DNS-zoner.</span><span class="sxs-lookup"><span data-stu-id="10a50-614">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="10a50-615">Lägger till NS-poster för en nyligen skapad underordnad zon i den överordnade zonen.</span><span class="sxs-lookup"><span data-stu-id="10a50-615">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="10a50-616">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="10a50-616">Az.FrontDoor</span></span>
* <span data-ttu-id="10a50-617">De första allmänt tillgängliga versionerna av cmdletar för Azure FrontDoor</span><span class="sxs-lookup"><span data-stu-id="10a50-617">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="10a50-618">Byt namn på WAF-cmdletar så att de omfattar ”Waf”</span><span class="sxs-lookup"><span data-stu-id="10a50-618">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="10a50-619">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="10a50-619">Az.HDInsight</span></span>
* <span data-ttu-id="10a50-620">Två cmdletar har tagits bort:</span><span class="sxs-lookup"><span data-stu-id="10a50-620">Removed two cmdlets:</span></span>
    - <span data-ttu-id="10a50-621">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="10a50-621">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="10a50-622">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="10a50-622">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="10a50-623">En ny cmdlet har lagts till, Set-AzHDInsightGatewayCredential, som ersätter Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="10a50-623">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="10a50-624">Uppdatera cmdleten Get-AzHDInsightJobOutput för att skilja mellan läsarrollen och HDInsight-operatörsrollen:</span><span class="sxs-lookup"><span data-stu-id="10a50-624">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="10a50-625">Användare med läsarrollen måste uttryckligen ange parametern ”DefaultStorageAccountKey”, annars uppstår fel.</span><span class="sxs-lookup"><span data-stu-id="10a50-625">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="10a50-626">Användare med HDInsight-operatörsrollen påverkas inte.</span><span class="sxs-lookup"><span data-stu-id="10a50-626">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="10a50-627">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="10a50-627">Az.Monitor</span></span>
* <span data-ttu-id="10a50-628">Nya cmdletar för SQR API (schemalagd frågeregel)</span><span class="sxs-lookup"><span data-stu-id="10a50-628">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="10a50-629">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="10a50-629">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="10a50-630">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="10a50-630">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="10a50-631">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="10a50-631">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="10a50-632">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="10a50-632">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="10a50-633">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="10a50-633">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="10a50-634">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="10a50-634">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="10a50-635">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="10a50-635">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="10a50-636">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="10a50-636">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="10a50-637">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="10a50-637">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="10a50-638">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="10a50-638">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="10a50-639">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="10a50-639">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="10a50-640">[Mer](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information om SQR API</span><span class="sxs-lookup"><span data-stu-id="10a50-640">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="10a50-641">Az.Monitor.md har uppdaterats för att omfatta cmdletar för måttbaserade aviseringsregler i GenV2 (inte klassiska)</span><span class="sxs-lookup"><span data-stu-id="10a50-641">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="10a50-642">Az.Network</span><span class="sxs-lookup"><span data-stu-id="10a50-642">Az.Network</span></span>
* <span data-ttu-id="10a50-643">Lägg till stöd för NAT Gateway-resurs</span><span class="sxs-lookup"><span data-stu-id="10a50-643">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="10a50-644">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="10a50-644">New cmdlets</span></span>
        - <span data-ttu-id="10a50-645">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="10a50-645">New-AzNatGateway</span></span>
        - <span data-ttu-id="10a50-646">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="10a50-646">Get-AzNatGateway</span></span>
        - <span data-ttu-id="10a50-647">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="10a50-647">Set-AzNatGateway</span></span>
        - <span data-ttu-id="10a50-648">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="10a50-648">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="10a50-649">Uppdaterade cmdletar</span><span class="sxs-lookup"><span data-stu-id="10a50-649">Updated cmdlets</span></span>
        - <span data-ttu-id="10a50-650">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="10a50-650">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="10a50-651">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="10a50-651">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="10a50-652">Nedanstående kommandon för funktionen har uppdaterats: Ange/ta bort anpassade vägar på Brooklyn Gateway.</span><span class="sxs-lookup"><span data-stu-id="10a50-652">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="10a50-653">New-AzVirtualNetworkGateway har uppdaterats: Den valfria parametern -CustomRoute har lagts till för att ställa in adressprefix som anpassade vägar för att ange gateway.</span><span class="sxs-lookup"><span data-stu-id="10a50-653">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="10a50-654">Set-AzVirtualNetworkGateway har uppdaterats: Den valfria parametern -CustomRoute har lagts till för att ange adressprefix som anpassade vägar för att ange gateway.</span><span class="sxs-lookup"><span data-stu-id="10a50-654">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="10a50-655">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="10a50-655">Az.PolicyInsights</span></span>
* <span data-ttu-id="10a50-656">Stöd för att fråga efter information om principutvärdering.</span><span class="sxs-lookup"><span data-stu-id="10a50-656">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="10a50-657">Lägg till parametern ”-Expand” för Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="10a50-657">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="10a50-658">Stöd för -Expand PolicyEvaluationDetails.</span><span class="sxs-lookup"><span data-stu-id="10a50-658">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="10a50-659">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="10a50-659">Az.RecoveryServices</span></span>
* <span data-ttu-id="10a50-660">Stöd för att dela prenumeration mellan Azure och Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="10a50-660">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="10a50-661">Markering av kommande icke-bakåtkompatibla ändringar för Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="10a50-661">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="10a50-662">Korrigering för återställningsplan och åtgärdsplan i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="10a50-662">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="10a50-663">Korrigering för mappning av uppdateringsnätverk i Azure Site Recovery för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="10a50-663">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="10a50-664">Korrigering för instruktioner för uppdateringsskydd i Azure Site Recovery för Azure till Azure för hanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="10a50-664">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="10a50-665">Andra mindre korrigeringar.</span><span class="sxs-lookup"><span data-stu-id="10a50-665">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="10a50-666">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="10a50-666">Az.Relay</span></span>
* <span data-ttu-id="10a50-667">Korrigera stavfel i kundriktade meddelanden</span><span class="sxs-lookup"><span data-stu-id="10a50-667">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="10a50-668">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="10a50-668">Az.ServiceBus</span></span>
* <span data-ttu-id="10a50-669">Nya cmdletar har lagts till för NetworkRuleSet för namnområden</span><span class="sxs-lookup"><span data-stu-id="10a50-669">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="10a50-670">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="10a50-670">Az.Storage</span></span>
* <span data-ttu-id="10a50-671">Uppgradera till lagringsklientbiblioteket 10.0.1 (namnområdet för alla objekt från detta SDK ändras från ”Microsoft.WindowsAzure.Storage. *till ”Microsoft.Azure.Storage.* ”)</span><span class="sxs-lookup"><span data-stu-id="10a50-671">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="10a50-672">Uppgradera till Microsoft.Azure.Management.Storage 11.0.0 för att stödja den nya API-versionen 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="10a50-672">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="10a50-673">Standardlagringskontot i Skapa lagringskonto ändras från ”Storage” till ”StorageV2”</span><span class="sxs-lookup"><span data-stu-id="10a50-673">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="10a50-674">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="10a50-674">New-AzStorageAccount</span></span>
* <span data-ttu-id="10a50-675">Ändra lagringskontots cmdlet-utdata Sku.Name för att passa med indata-SkuName genom att lägga till ”-”. Till exempel ändras ”StandardLRS” till ”Standard_LRS”</span><span class="sxs-lookup"><span data-stu-id="10a50-675">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="10a50-676">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="10a50-676">New-AzStorageAccount</span></span>
    - <span data-ttu-id="10a50-677">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="10a50-677">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="10a50-678">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="10a50-678">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="10a50-679">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="10a50-679">Az.Websites</span></span>
* <span data-ttu-id="10a50-680">Egenskapen ”typ” konfigureras nu för PSSite-objekt som returneras av Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="10a50-680">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="10a50-681">Get-AzWebApp\*Metrics och Get-AzAppServicePlanMetrics markeras som inaktuella</span><span class="sxs-lookup"><span data-stu-id="10a50-681">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="10a50-682">1.8.0 – april 2019</span><span class="sxs-lookup"><span data-stu-id="10a50-682">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="10a50-683">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="10a50-683">Highlights since the last major release</span></span>
* <span data-ttu-id="10a50-684">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="10a50-684">General availability of `Az` module</span></span>
* <span data-ttu-id="10a50-685">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="10a50-685">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="10a50-686">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="10a50-686">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="10a50-687">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="10a50-687">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="10a50-688">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="10a50-688">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="10a50-689">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="10a50-689">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="10a50-690">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="10a50-690">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="10a50-691">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="10a50-691">Az.Accounts</span></span>
* <span data-ttu-id="10a50-692">Uppdatera Uninstall-AzureRm för att ta bort moduler i Mac på ett korrekt sätt</span><span class="sxs-lookup"><span data-stu-id="10a50-692">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="10a50-693">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="10a50-693">Az.Batch</span></span>
* <span data-ttu-id="10a50-694">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="10a50-694">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="10a50-695">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="10a50-695">Az.Cdn</span></span>
* <span data-ttu-id="10a50-696">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="10a50-696">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="10a50-697">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="10a50-697">Az.CognitiveServices</span></span>
* <span data-ttu-id="10a50-698">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="10a50-698">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="10a50-699">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="10a50-699">Az.Compute</span></span>
* <span data-ttu-id="10a50-700">Åtgärda problem med AEM-installationen om resurs-ID:n för diskar innehåller resourcegroups i gemener i resurs-ID:n</span><span class="sxs-lookup"><span data-stu-id="10a50-700">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="10a50-701">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="10a50-701">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="10a50-702">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="10a50-702">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="10a50-703">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="10a50-703">Az.DataFactory</span></span>
* <span data-ttu-id="10a50-704">Lägg till SsisProperties om NodeCount inte är null för hanterad integreringskörning.</span><span class="sxs-lookup"><span data-stu-id="10a50-704">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="10a50-705">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="10a50-705">Az.DataLakeStore</span></span>
* <span data-ttu-id="10a50-706">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="10a50-706">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="10a50-707">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="10a50-707">Az.EventGrid</span></span>
* <span data-ttu-id="10a50-708">Hjälptexten för slutpunkten har uppdaterats för att visa att resurser ska skapas innan cmdletarna för att skapa/uppdatera händelseprenumerationer används.</span><span class="sxs-lookup"><span data-stu-id="10a50-708">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="10a50-709">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="10a50-709">Az.EventHub</span></span>
* <span data-ttu-id="10a50-710">Nya cmdletar har lagts till för NetworkRuleSet för namnområden</span><span class="sxs-lookup"><span data-stu-id="10a50-710">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="10a50-711">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="10a50-711">Az.HDInsight</span></span>
* <span data-ttu-id="10a50-712">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="10a50-712">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="10a50-713">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="10a50-713">Az.IotHub</span></span>
* <span data-ttu-id="10a50-714">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="10a50-714">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="10a50-715">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="10a50-715">Az.KeyVault</span></span>
* <span data-ttu-id="10a50-716">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="10a50-716">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="10a50-717">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="10a50-717">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="10a50-718">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="10a50-718">Az.MachineLearning</span></span>
* <span data-ttu-id="10a50-719">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="10a50-719">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="10a50-720">Az.Media</span><span class="sxs-lookup"><span data-stu-id="10a50-720">Az.Media</span></span>
* <span data-ttu-id="10a50-721">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="10a50-721">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="10a50-722">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="10a50-722">Az.Monitor</span></span>
  * <span data-ttu-id="10a50-723">Nya cmdletar för måttbaserad aviseringsregel i GenV2 (inte klassisk)</span><span class="sxs-lookup"><span data-stu-id="10a50-723">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="10a50-724">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="10a50-724">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="10a50-725">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="10a50-725">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="10a50-726">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="10a50-726">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="10a50-727">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="10a50-727">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="10a50-728">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="10a50-728">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="10a50-729">Monitor SDK har uppdaterats till version 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="10a50-729">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="10a50-730">Az.Network</span><span class="sxs-lookup"><span data-stu-id="10a50-730">Az.Network</span></span>
* <span data-ttu-id="10a50-731">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="10a50-731">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="10a50-732">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="10a50-732">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="10a50-733">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="10a50-733">Az.NotificationHubs</span></span>
* <span data-ttu-id="10a50-734">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="10a50-734">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="10a50-735">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="10a50-735">Az.OperationalInsights</span></span>
* <span data-ttu-id="10a50-736">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="10a50-736">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="10a50-737">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="10a50-737">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="10a50-738">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="10a50-738">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="10a50-739">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="10a50-739">Az.RecoveryServices</span></span>
* <span data-ttu-id="10a50-740">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="10a50-740">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="10a50-741">Tabellformatet för SQL i virtuella Azure-datorer har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="10a50-741">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="10a50-742">En alternativ metod för att hämta platser i AzureFileShare har lagts till</span><span class="sxs-lookup"><span data-stu-id="10a50-742">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="10a50-743">ScheduleRunDays i SchedulePolicy-objekt har uppdaterats enligt tidszon</span><span class="sxs-lookup"><span data-stu-id="10a50-743">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="10a50-744">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="10a50-744">Az.RedisCache</span></span>
* <span data-ttu-id="10a50-745">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="10a50-745">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="10a50-746">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="10a50-746">Az.Resources</span></span>
* <span data-ttu-id="10a50-747">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="10a50-747">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="10a50-748">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="10a50-748">Az.Sql</span></span>
* <span data-ttu-id="10a50-749">Ersätt Monitor SDK-beroende med vanlig kod</span><span class="sxs-lookup"><span data-stu-id="10a50-749">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="10a50-750">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="10a50-750">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="10a50-751">Förbättrad process för klassificering av flera kolumner.</span><span class="sxs-lookup"><span data-stu-id="10a50-751">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="10a50-752">Inkludera SKU-egenskaper (SKU-namn, serie, kapacitet) i svaret från Get-AzSqlServerServiceObjective och formatera som tabell som standard.</span><span class="sxs-lookup"><span data-stu-id="10a50-752">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="10a50-753">Möjlighet att använda Get-AzSqlServerServiceObjective efter plats utan att behöva en redan befintlig server i regionen.</span><span class="sxs-lookup"><span data-stu-id="10a50-753">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="10a50-754">Stöd för tidszonsparametern när hanterade instanser skapas.</span><span class="sxs-lookup"><span data-stu-id="10a50-754">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="10a50-755">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="10a50-755">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="10a50-756">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="10a50-756">Az.Websites</span></span>
* <span data-ttu-id="10a50-757">åtgärdar Set-AzWebApp och Set-AzWebAppSlot så att de inte tar bort taggar vid körning</span><span class="sxs-lookup"><span data-stu-id="10a50-757">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="10a50-758">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="10a50-758">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="10a50-759">SDK för WebSites har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="10a50-759">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="10a50-760">Egenskapen AdminSiteName har tagits bort från PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="10a50-760">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="10a50-761">1.7.0 – april 2019</span><span class="sxs-lookup"><span data-stu-id="10a50-761">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="10a50-762">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="10a50-762">Highlights since the last major release</span></span>
* <span data-ttu-id="10a50-763">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="10a50-763">General availability of `Az` module</span></span>
* <span data-ttu-id="10a50-764">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="10a50-764">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="10a50-765">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="10a50-765">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="10a50-766">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="10a50-766">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="10a50-767">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="10a50-767">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="10a50-768">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="10a50-768">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="10a50-769">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="10a50-769">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="10a50-770">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="10a50-770">Az.Accounts</span></span>
* <span data-ttu-id="10a50-771">Add-AzEnvironment och Set-AzEnvironment har uppdaterats för att godkänna parametern AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="10a50-771">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="10a50-772">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="10a50-772">Az.AnalysisServices</span></span>
* <span data-ttu-id="10a50-773">ServiceClient används i cmdletar för dataplan och den ursprungliga autentiseringslogiken har tagits bort</span><span class="sxs-lookup"><span data-stu-id="10a50-773">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="10a50-774">Add-AzureASAccount används för omslutning av Connect-AzAccount för att undvika en icke-bakåtkompatibel ändring</span><span class="sxs-lookup"><span data-stu-id="10a50-774">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="10a50-775">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="10a50-775">Az.Automation</span></span>
* <span data-ttu-id="10a50-776">Buggen för cmdleten New-AzAutomationSoftwareUpdateConfiguration för inkluderingar har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="10a50-776">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="10a50-777">Nu bör parametern IncludedKbNumber och IncludedPackageNameMask fungera.</span><span class="sxs-lookup"><span data-stu-id="10a50-777">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="10a50-778">Felkorrigering för dynamiska grupper i uppdateringshanteringen för azure automation</span><span class="sxs-lookup"><span data-stu-id="10a50-778">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="10a50-779">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="10a50-779">Az.Compute</span></span>
* <span data-ttu-id="10a50-780">Lägg till parametern HyperVGeneration i New-AzDiskConfig och New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="10a50-780">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="10a50-781">Tillåt att virtuella datorer skapas med galleribilder från andra klientorganisationer.</span><span class="sxs-lookup"><span data-stu-id="10a50-781">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="10a50-782">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="10a50-782">Az.ContainerInstance</span></span>
* <span data-ttu-id="10a50-783">Ett problem har åtgärdats i parametern -Command för New-AzContainerGroup som lade till ett avslutande tomt argument</span><span class="sxs-lookup"><span data-stu-id="10a50-783">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="10a50-784">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="10a50-784">Az.DataFactory</span></span>
* <span data-ttu-id="10a50-785">ADF .Net SDK-versionen har uppdaterats till 3.0.2</span><span class="sxs-lookup"><span data-stu-id="10a50-785">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="10a50-786">Cmdleten Set-AzDataFactoryV2 har uppdaterats med extra parametrar för inställningar som rör RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="10a50-786">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="10a50-787">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="10a50-787">Az.Resources</span></span>
* <span data-ttu-id="10a50-788">Förbättra hanteringen av providrar för Get-AzResource när parametrarna -ResourceId eller -ResourceGroupName, -Name och -ResourceType tillhandahålls</span><span class="sxs-lookup"><span data-stu-id="10a50-788">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="10a50-789">Förbättra felhanteringen för ”Test-AzDeployment” och ”Test-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="10a50-789">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="10a50-790">Hantera fel utanför distributionsvalideringen och ta med dem i kommandoutdata istället</span><span class="sxs-lookup"><span data-stu-id="10a50-790">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="10a50-791">Mer information här: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="10a50-791">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="10a50-792">Lägg till växlingsparametern -IgnoreDynamicParameters till en uppsättning av cmdletar för distribution för att hoppa över fråga i skript och jobbscenarier</span><span class="sxs-lookup"><span data-stu-id="10a50-792">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="10a50-793">Mer information här: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="10a50-793">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="10a50-794">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="10a50-794">Az.Sql</span></span>
* <span data-ttu-id="10a50-795">Stöd för dataklassificering av databaser.</span><span class="sxs-lookup"><span data-stu-id="10a50-795">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="10a50-796">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="10a50-796">Az.Storage</span></span>
* <span data-ttu-id="10a50-797">Rapportera detaljfel när lagringskontext skapas med parametern -UseConnectedAccount, men utan inloggning på Azure-kontot</span><span class="sxs-lookup"><span data-stu-id="10a50-797">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="10a50-798">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="10a50-798">New-AzStorageContext</span></span>
* <span data-ttu-id="10a50-799">Stöd för att hantera Blob Service-egenskaper för ett angivet lagringskonto med API:et för hanteringsplan</span><span class="sxs-lookup"><span data-stu-id="10a50-799">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="10a50-800">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="10a50-800">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="10a50-801">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="10a50-801">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="10a50-802">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="10a50-802">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="10a50-803">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="10a50-803">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="10a50-804">Stöd för -AsJob-cmdletar för att ladda upp och ladda ned blobar och filer</span><span class="sxs-lookup"><span data-stu-id="10a50-804">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="10a50-805">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="10a50-805">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="10a50-806">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="10a50-806">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="10a50-807">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="10a50-807">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="10a50-808">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="10a50-808">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="10a50-809">1.6.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="10a50-809">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="10a50-810">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="10a50-810">Highlights since the last major release</span></span>
* <span data-ttu-id="10a50-811">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="10a50-811">General availability of `Az` module</span></span>
* <span data-ttu-id="10a50-812">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="10a50-812">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="10a50-813">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="10a50-813">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="10a50-814">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="10a50-814">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="10a50-815">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="10a50-815">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="10a50-816">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="10a50-816">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="10a50-817">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="10a50-817">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="10a50-818">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="10a50-818">Az.Automation</span></span>
* <span data-ttu-id="10a50-819">Azure Automation – ändring av uppdateringshantering för stöd för de nya funktionerna:</span><span class="sxs-lookup"><span data-stu-id="10a50-819">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="10a50-820">Dynamisk gruppering</span><span class="sxs-lookup"><span data-stu-id="10a50-820">Dynamic grouping</span></span>
    * <span data-ttu-id="10a50-821">För-/efterskrift</span><span class="sxs-lookup"><span data-stu-id="10a50-821">Pre-Post script</span></span>
    * <span data-ttu-id="10a50-822">Inställning för omstart</span><span class="sxs-lookup"><span data-stu-id="10a50-822">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="10a50-823">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="10a50-823">Az.Compute</span></span>
* <span data-ttu-id="10a50-824">Åtgärda problem med sökvägsmatchning i Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="10a50-824">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="10a50-825">Uppdatera Compute-klientbibliotek till 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="10a50-825">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="10a50-826">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="10a50-826">Az.KeyVault</span></span>
* <span data-ttu-id="10a50-827">Stöd för jokertecken för KeyVault-cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="10a50-827">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="10a50-828">Az.Network</span><span class="sxs-lookup"><span data-stu-id="10a50-828">Az.Network</span></span>
* <span data-ttu-id="10a50-829">Lägg till stöd för Threat Intelligence för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="10a50-829">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="10a50-830">Lägg till resurs för brandväggsprincip på översta nivå och anpassade regler för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="10a50-830">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="10a50-831">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="10a50-831">Az.RecoveryServices</span></span>
* <span data-ttu-id="10a50-832">SnapshotRetentionInDays har lagts till i Azure-principen för virtuella datorer för stöd av Instant RP</span><span class="sxs-lookup"><span data-stu-id="10a50-832">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="10a50-833">Pipe-stöd för avregistrering av container har lagts till</span><span class="sxs-lookup"><span data-stu-id="10a50-833">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="10a50-834">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="10a50-834">Az.Resources</span></span>
* <span data-ttu-id="10a50-835">Uppdatera stöd för jokertecken för Get-AzResource och Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="10a50-835">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="10a50-836">Uppdatera autentiseringsuppgifter som används vid allmänna anrop till ARM</span><span class="sxs-lookup"><span data-stu-id="10a50-836">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="10a50-837">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="10a50-837">Az.Sql</span></span>
* <span data-ttu-id="10a50-838">Cmdlet-parametern (ExcludeDetectionType) för Hotidentifiering ändrades från DetectionType till sträng[] för att framtidssäkra den när nya DetectionTypes läggs till, och även för att stödja automatisk ifyllning.</span><span class="sxs-lookup"><span data-stu-id="10a50-838">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="10a50-839">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="10a50-839">Az.Storage</span></span>
* <span data-ttu-id="10a50-840">Stöd för att hämta/ange/ta bort hanteringsprincip på ett lagringskonto</span><span class="sxs-lookup"><span data-stu-id="10a50-840">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="10a50-841">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="10a50-841">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="10a50-842">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="10a50-842">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="10a50-843">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="10a50-843">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="10a50-844">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="10a50-844">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="10a50-845">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="10a50-845">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="10a50-846">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="10a50-846">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="10a50-847">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="10a50-847">Az.Websites</span></span>
* <span data-ttu-id="10a50-848">Åtgärda fel med ARM-mall som avbryter kloning av alla platser med 'New-AzWebApp -IncludeSourceWebAppSlots'</span><span class="sxs-lookup"><span data-stu-id="10a50-848">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="10a50-849">1.5.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="10a50-849">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="10a50-850">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="10a50-850">Az.Accounts</span></span>
* <span data-ttu-id="10a50-851">Lägg till kommandot Register-AzModule för stöd för AutoRest-genererade cmdletar</span><span class="sxs-lookup"><span data-stu-id="10a50-851">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="10a50-852">Uppdatera exempel för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="10a50-852">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="10a50-853">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="10a50-853">Az.Automation</span></span>
* <span data-ttu-id="10a50-854">Problem med att hämta vissa månadsscheman i flera Azure Automation-cmdletar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="10a50-854">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="10a50-855">Åtgärda problem med att Get-AzAutomationDscNode bara returnerar de 20 översta noderna.</span><span class="sxs-lookup"><span data-stu-id="10a50-855">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="10a50-856">Nu returneras alla noder</span><span class="sxs-lookup"><span data-stu-id="10a50-856">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="10a50-857">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="10a50-857">Az.Cdn</span></span>
* <span data-ttu-id="10a50-858">Nya Powershell-cmdletar för att aktivera/inaktivera anpassade domän-HTTPS har lagts till och de gamla har gjorts inaktuella</span><span class="sxs-lookup"><span data-stu-id="10a50-858">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="10a50-859">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="10a50-859">Az.Compute</span></span>
* <span data-ttu-id="10a50-860">Lägg till stöd för jokertecken för Get-cmdletar</span><span class="sxs-lookup"><span data-stu-id="10a50-860">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="10a50-861">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="10a50-861">Az.DataFactory</span></span>
* <span data-ttu-id="10a50-862">ADF .Net SDK-versionen har uppdaterats till 3.0.1</span><span class="sxs-lookup"><span data-stu-id="10a50-862">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="10a50-863">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="10a50-863">Az.LogicApp</span></span>
* <span data-ttu-id="10a50-864">Åtgärda problemet med att ListWorkflows endast hämtar den första sidan med resultat</span><span class="sxs-lookup"><span data-stu-id="10a50-864">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="10a50-865">Az.Network</span><span class="sxs-lookup"><span data-stu-id="10a50-865">Az.Network</span></span>
* <span data-ttu-id="10a50-866">Lägg till stöd för jokertecken för Network-cmdletar</span><span class="sxs-lookup"><span data-stu-id="10a50-866">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="10a50-867">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="10a50-867">Az.RecoveryServices</span></span>
* <span data-ttu-id="10a50-868">Stöd har lagts till för SQL Server i virtuella Azure-datorer</span><span class="sxs-lookup"><span data-stu-id="10a50-868">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="10a50-869">SDK-uppdatering</span><span class="sxs-lookup"><span data-stu-id="10a50-869">SDK Update</span></span>
* <span data-ttu-id="10a50-870">Get-ProtectableItem-incheckning i VMappContainer har tagits bort</span><span class="sxs-lookup"><span data-stu-id="10a50-870">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="10a50-871">Name och ServerName har lagts till som parametrar för Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="10a50-871">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="10a50-872">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="10a50-872">Az.Resources</span></span>
* <span data-ttu-id="10a50-873">Lägg till parametern `-TemplateObject` i cmdletar för distribution</span><span class="sxs-lookup"><span data-stu-id="10a50-873">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="10a50-874">Mer information här: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="10a50-874">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="10a50-875">Åtgärda problem med piping av resultatet i `Get-AzResource` till `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="10a50-875">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="10a50-876">Mer information här: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="10a50-876">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="10a50-877">Åtgärda problem med ändring av JSON-datatyp när `Set-AzResource` körs</span><span class="sxs-lookup"><span data-stu-id="10a50-877">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="10a50-878">Mer information här: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="10a50-878">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="10a50-879">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="10a50-879">Az.Sql</span></span>
* <span data-ttu-id="10a50-880">AuditingEndpointsCommunicator uppdateras.</span><span class="sxs-lookup"><span data-stu-id="10a50-880">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="10a50-881">Åtgärdar beteendet hos ett gränsscenario när nya diagnostikinställningar skapas.</span><span class="sxs-lookup"><span data-stu-id="10a50-881">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="10a50-882">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="10a50-882">Az.Storage</span></span>
* <span data-ttu-id="10a50-883">Stöd för BlockBlobStorage när Storage-konto skapas      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="10a50-883">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="10a50-884">1.4.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="10a50-884">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="10a50-885">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="10a50-885">Az.AnalysisServices</span></span>
* <span data-ttu-id="10a50-886">Inaktuell AddAzureASAccount-cmdlet</span><span class="sxs-lookup"><span data-stu-id="10a50-886">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="10a50-887">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="10a50-887">Az.Automation</span></span>
* <span data-ttu-id="10a50-888">Hjälpen för Import-AzAutomationDscNodeConfiguration har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="10a50-888">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="10a50-889">Konfigurationsnamnsvalidering har lagts till i cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="10a50-889">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="10a50-890">Förbättrad felhantering för cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="10a50-890">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="10a50-891">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="10a50-891">Az.CognitiveServices</span></span>
* <span data-ttu-id="10a50-892">CustomSubdomainName har lagts till som en ny valfri parameter för New-AzCognitiveServicesAccount, som används för att ange underdomän för resursen.</span><span class="sxs-lookup"><span data-stu-id="10a50-892">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="10a50-893">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="10a50-893">Az.Compute</span></span>
* <span data-ttu-id="10a50-894">Problemet med ID-parameteruppsättningar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="10a50-894">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="10a50-895">Get-AzVMExtension har uppdaterats så att alla installerade tillägg visas om parametern Name inte har angetts</span><span class="sxs-lookup"><span data-stu-id="10a50-895">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="10a50-896">Parametrarna Tag och ResourceId har lagts till i cmdleten Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="10a50-896">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="10a50-897">Get-AzVmssVM utan instans-ID och med InstanceView kan visa virtuella VMSS-datorer med instansvyn.</span><span class="sxs-lookup"><span data-stu-id="10a50-897">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="10a50-898">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="10a50-898">Az.DataLakeStore</span></span>
* <span data-ttu-id="10a50-899">Cmdletar har lagts till för uppräkning och återställning av borttagna objekt i ADL</span><span class="sxs-lookup"><span data-stu-id="10a50-899">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="10a50-900">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="10a50-900">Az.EventHub</span></span>
* <span data-ttu-id="10a50-901">Ny boolesk egenskap SkipEmptyArchives har lagts till i Skip Empty Archives i CaptureDescription-klassen i Eventhub</span><span class="sxs-lookup"><span data-stu-id="10a50-901">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="10a50-902">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="10a50-902">Az.KeyVault</span></span>
* <span data-ttu-id="10a50-903">Taggning i Set-AzKeyVaultSecret har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="10a50-903">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="10a50-904">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="10a50-904">Az.LogicApp</span></span>
* <span data-ttu-id="10a50-905">Grundläggande SKU har lagts till för Integrationskonton</span><span class="sxs-lookup"><span data-stu-id="10a50-905">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="10a50-906">XSLT 2.0, XSLT 3.0 och Flytande mappningstyper har lagts till</span><span class="sxs-lookup"><span data-stu-id="10a50-906">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="10a50-907">Nya cmdletar för integrationskontosammansättningar</span><span class="sxs-lookup"><span data-stu-id="10a50-907">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="10a50-908">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="10a50-908">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="10a50-909">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="10a50-909">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="10a50-910">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="10a50-910">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="10a50-911">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="10a50-911">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="10a50-912">Nya cmdletar för batchkonfiguration för integrationskonto</span><span class="sxs-lookup"><span data-stu-id="10a50-912">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="10a50-913">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="10a50-913">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="10a50-914">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="10a50-914">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="10a50-915">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="10a50-915">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="10a50-916">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="10a50-916">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="10a50-917">Logic App-SDK har uppdaterats till version 4.1.0</span><span class="sxs-lookup"><span data-stu-id="10a50-917">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="10a50-918">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="10a50-918">Az.Monitor</span></span>
* <span data-ttu-id="10a50-919">Hjälpen för Get-AzMetric har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="10a50-919">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="10a50-920">Az.Network</span><span class="sxs-lookup"><span data-stu-id="10a50-920">Az.Network</span></span>
* <span data-ttu-id="10a50-921">Hjälpexempel för Add-AzApplicationGatewayCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="10a50-921">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="10a50-922">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="10a50-922">Az.OperationalInsights</span></span>
* <span data-ttu-id="10a50-923">Ytterligare stöd för datakällorna New och Get ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="10a50-923">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="10a50-924">Ny ApplicationInsights-typ har lagts till för att ge stöd för ”Get specific” och ”Get all” för ApplicationInsights-datakällor för angiven arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="10a50-924">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="10a50-925">Cmdleten New-AzOperationalInsightsApplicationInsightsDataSource har lagts till för att skapa datakälla med angivna parametrar för Application Insights-resurs: subscription Id, resourceGroupName och name.</span><span class="sxs-lookup"><span data-stu-id="10a50-925">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="10a50-926">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="10a50-926">Az.Resources</span></span>
* <span data-ttu-id="10a50-927">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="10a50-927">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="10a50-928">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="10a50-928">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="10a50-929">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="10a50-929">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="10a50-930">Fel som gör att KeyCredentials inte kan skapas upprepade gånger har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="10a50-930">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="10a50-931">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="10a50-931">Az.Sql</span></span>
* <span data-ttu-id="10a50-932">Lägg till stöd för hyperskalanivån för SQL DB</span><span class="sxs-lookup"><span data-stu-id="10a50-932">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="10a50-933">Ett fel har åtgärdats där återställningen kunde misslyckas på grund av onödiga inställningsegenskaper i restore-förfrågan</span><span class="sxs-lookup"><span data-stu-id="10a50-933">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="10a50-934">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="10a50-934">Az.Websites</span></span>
* <span data-ttu-id="10a50-935">Rätt exempel i Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="10a50-935">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="10a50-936">1.3.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="10a50-936">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="10a50-937">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="10a50-937">Az.Accounts</span></span>
* <span data-ttu-id="10a50-938">Uppdatera till den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="10a50-938">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="10a50-939">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="10a50-939">Az.AnalysisServices</span></span>
<span data-ttu-id="10a50-940">Allmän tillgänglighet för Az.AnalysisServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="10a50-940">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="10a50-941">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="10a50-941">Az.Compute</span></span>
* <span data-ttu-id="10a50-942">AEM-tillägg: Lägg till stöd för UltraSSD-, P60-, P70- och P80-diskar</span><span class="sxs-lookup"><span data-stu-id="10a50-942">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="10a50-943">Uppdatera hjälpbeskrivning för Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="10a50-943">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="10a50-944">Uppdatera hjälpbeskrivning och exempel för Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="10a50-944">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="10a50-945">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="10a50-945">Az.RecoveryServices</span></span>
<span data-ttu-id="10a50-946">Allmän tillgänglighet för Az.RecoveryServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="10a50-946">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="10a50-947">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="10a50-947">Az.Resources</span></span>
* <span data-ttu-id="10a50-948">Korrigera taggar för resursgrupper</span><span class="sxs-lookup"><span data-stu-id="10a50-948">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="10a50-949">Mer information här: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="10a50-949">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="10a50-950">Åtgärda problem där `Get-AzureRmRoleAssignment` inte respekterar -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="10a50-950">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="10a50-951">Mer information här: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="10a50-951">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="10a50-952">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="10a50-952">Az.Sql</span></span>
* <span data-ttu-id="10a50-953">Lägga till Get/Set-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="10a50-953">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="10a50-954">Åtgärda problem där ett nullref-undantag uppstår när du kör SQL-cmdletar och inte är inloggad på ett Azure-konto</span><span class="sxs-lookup"><span data-stu-id="10a50-954">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="10a50-955">Åtgärda nullref-undantag i Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="10a50-955">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="10a50-956">1.2.1 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="10a50-956">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="10a50-957">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="10a50-957">Az.Accounts</span></span>
* <span data-ttu-id="10a50-958">Version med rätt version av autentisering</span><span class="sxs-lookup"><span data-stu-id="10a50-958">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="10a50-959">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="10a50-959">Az.AnalysisServices</span></span>
* <span data-ttu-id="10a50-960">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="10a50-960">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="10a50-961">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="10a50-961">Az.RecoveryServices</span></span>
* <span data-ttu-id="10a50-962">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="10a50-962">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="10a50-963">1.2.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="10a50-963">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="10a50-964">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="10a50-964">Az.Accounts</span></span>
* <span data-ttu-id="10a50-965">Lägga till interaktiv autentisering och autentisering med användarnamn/lösenord för endast Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="10a50-965">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="10a50-966">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="10a50-966">Update incorrect online help URLs</span></span>
* <span data-ttu-id="10a50-967">Lägga till varningsmeddelande i PS Core för Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="10a50-967">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="10a50-968">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="10a50-968">Az.Aks</span></span>
* <span data-ttu-id="10a50-969">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="10a50-969">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="10a50-970">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="10a50-970">Az.Automation</span></span>
* <span data-ttu-id="10a50-971">Stöd för Python 2-runbookflöden har lagts till</span><span class="sxs-lookup"><span data-stu-id="10a50-971">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="10a50-972">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="10a50-972">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="10a50-973">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="10a50-973">Az.Cdn</span></span>
* <span data-ttu-id="10a50-974">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="10a50-974">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="10a50-975">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="10a50-975">Az.Compute</span></span>
* <span data-ttu-id="10a50-976">Lägga till cmdleten Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="10a50-976">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="10a50-977">Lägga till TempDisk-parameter i Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="10a50-977">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="10a50-978">Korrigera varningsmeddelande för New-AzVM</span><span class="sxs-lookup"><span data-stu-id="10a50-978">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="10a50-979">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="10a50-979">Az.ContainerRegistry</span></span>
* <span data-ttu-id="10a50-980">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="10a50-980">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="10a50-981">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="10a50-981">Az.DataFactory</span></span>
* <span data-ttu-id="10a50-982">ADF .Net SDK-versionen har uppdaterats till 3.0.0</span><span class="sxs-lookup"><span data-stu-id="10a50-982">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="10a50-983">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="10a50-983">Az.DataLakeStore</span></span>
* <span data-ttu-id="10a50-984">Åtgärda problem med ADLS-slutpunkt vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="10a50-984">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="10a50-985">Mer information här: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="10a50-985">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="10a50-986">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="10a50-986">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="10a50-987">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="10a50-987">Az.IotHub</span></span>
* <span data-ttu-id="10a50-988">Lägga till kodningsformat i cmdleten Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="10a50-988">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="10a50-989">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="10a50-989">Az.KeyVault</span></span>
* <span data-ttu-id="10a50-990">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="10a50-990">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="10a50-991">Az.Network</span><span class="sxs-lookup"><span data-stu-id="10a50-991">Az.Network</span></span>
* <span data-ttu-id="10a50-992">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="10a50-992">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="10a50-993">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="10a50-993">Az.Resources</span></span>
* <span data-ttu-id="10a50-994">Åtgärda felaktiga exempel i referensdokumentationen ”New-AzADAppCredential” och ”New-AzADSpCredential”</span><span class="sxs-lookup"><span data-stu-id="10a50-994">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="10a50-995">Åtgärda problem där sökvägen för parametern ”-TemplateFile” inte omvandlas innan cmdletarna för distribution i resursgruppen körs</span><span class="sxs-lookup"><span data-stu-id="10a50-995">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="10a50-996">Az.Resources: Korrigera dokumentationen om standardvärdet för New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="10a50-996">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="10a50-997">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="10a50-997">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="10a50-998">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="10a50-998">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="10a50-999">Åtgärda formateringsproblemet med objektet ”PSResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="10a50-999">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="10a50-1000">Mer information här: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="10a50-1000">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="10a50-1001">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="10a50-1001">Az.ServiceFabric</span></span>
* <span data-ttu-id="10a50-1002">Återställ när ett certifikat läggs till i en Virtual Machine Scale Sets-modell men ett undantag genereras. Detta har gjorts för att åtgärda följande fel: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="10a50-1002">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="10a50-1003">Korrigera några felmeddelanden.</span><span class="sxs-lookup"><span data-stu-id="10a50-1003">Fix some error messages.</span></span>
* <span data-ttu-id="10a50-1004">Korrigering av skapande av kluster med ARM-mall som är standard för New-AzServiceFabriCluster som inte fungerade med migrering till Az.</span><span class="sxs-lookup"><span data-stu-id="10a50-1004">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="10a50-1005">Korrigering av tilläggning av kluster/programcertifikat så att endast VM Scale Sets som motsvarar klustret läggs till genom att kontrollera ID för klustret i tillägget.</span><span class="sxs-lookup"><span data-stu-id="10a50-1005">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="10a50-1006">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="10a50-1006">Az.SignalR</span></span>
* <span data-ttu-id="10a50-1007">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="10a50-1007">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="10a50-1008">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="10a50-1008">Az.Sql</span></span>
* <span data-ttu-id="10a50-1009">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="10a50-1009">Update incorrect online help URLs</span></span>
* <span data-ttu-id="10a50-1010">Uppdaterad parameterbeskrivning för LicenseType-parameter med möjliga värden</span><span class="sxs-lookup"><span data-stu-id="10a50-1010">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="10a50-1011">Korrigering för att uppdatera hanterad instansidentitet som inte fungerar när det är den enda uppdaterade egenskapen</span><span class="sxs-lookup"><span data-stu-id="10a50-1011">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="10a50-1012">Stöd för anpassad sortering på hanterad instans</span><span class="sxs-lookup"><span data-stu-id="10a50-1012">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="10a50-1013">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="10a50-1013">Az.Storage</span></span>
* <span data-ttu-id="10a50-1014">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="10a50-1014">Update incorrect online help URLs</span></span>
* <span data-ttu-id="10a50-1015">Tillhandahåll detaljerat felmeddelande när en användare försöker hämta/konfigurera klassisk loggning/mått på ett Premium Storage-konto eftersom Premium Storage-kontot inte har stöd för klassisk loggning/mått.</span><span class="sxs-lookup"><span data-stu-id="10a50-1015">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="10a50-1016">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="10a50-1016">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="10a50-1017">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="10a50-1017">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="10a50-1018">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="10a50-1018">Az.TrafficManager</span></span>
* <span data-ttu-id="10a50-1019">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="10a50-1019">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="10a50-1020">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="10a50-1020">Az.Websites</span></span>
* <span data-ttu-id="10a50-1021">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="10a50-1021">Update incorrect online help URLs</span></span>
* <span data-ttu-id="10a50-1022">Korrigerar ”New-AzWebAppSSLBinding” så att certifikatet laddas upp till rätt resursgrupp och plats om appen finns i en ASE.</span><span class="sxs-lookup"><span data-stu-id="10a50-1022">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="10a50-1023">Korrigerar ”New-AzWebAppSSLBinding” så att taggarna inte skrivs över på en bindning av ett SSL-certifikat till en app</span><span class="sxs-lookup"><span data-stu-id="10a50-1023">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="10a50-1024">1.1.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="10a50-1024">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="10a50-1025">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="10a50-1025">Az.Accounts</span></span>
* <span data-ttu-id="10a50-1026">Lade till omfattningen ”Lokal” till Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="10a50-1026">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="10a50-1027">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="10a50-1027">Az.Compute</span></span>
* <span data-ttu-id="10a50-1028">Namn är nu valfritt i ID-parametern för Restart/Start/Stop/Remove/Set-AzVM och Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="10a50-1028">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="10a50-1029">Uppdaterade beskrivningen av ID i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="10a50-1029">Updated the description of ID in help files</span></span>
* <span data-ttu-id="10a50-1030">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="10a50-1030">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="10a50-1031">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="10a50-1031">Az.DataLakeStore</span></span>
* <span data-ttu-id="10a50-1032">Uppdatera sdk-versionen av dataplanet till 1.1.14 för SDK-korrigeringar.</span><span class="sxs-lookup"><span data-stu-id="10a50-1032">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="10a50-1033">Korrigerade hanteringen av negativ accesstime och modificationtime för getfilestatus och liststatus; korrigera asynkront annulleringstoken</span><span class="sxs-lookup"><span data-stu-id="10a50-1033">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="10a50-1034">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="10a50-1034">Az.EventGrid</span></span>
* <span data-ttu-id="10a50-1035">Uppdaterat för användning av API-versionen 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="10a50-1035">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="10a50-1036">Uppdaterade följande cmdletar för att stödja nytt scenario i API-versionen 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="10a50-1036">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="10a50-1037">New-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="10a50-1037">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="10a50-1038">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="10a50-1038">Event Time-To-Live,</span></span>
        - <span data-ttu-id="10a50-1039">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="10a50-1039">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="10a50-1040">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="10a50-1040">Dead letter endpoint.</span></span>
    - <span data-ttu-id="10a50-1041">Update-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="10a50-1041">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="10a50-1042">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="10a50-1042">Event Time-To-Live,</span></span>
        - <span data-ttu-id="10a50-1043">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="10a50-1043">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="10a50-1044">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="10a50-1044">Dead letter endpoint.</span></span>
* <span data-ttu-id="10a50-1045">Lade till nya enum-värden (storageQueue och hybridConnection) för alternativet EndpointType i cmdletarna New-AzureRmEventGridSubscription och Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="10a50-1045">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="10a50-1046">Visa varningsmeddelanden om skapande eller uppdatering av händelseprenumerationen förväntas medföra manuell åtgärd från användaren.</span><span class="sxs-lookup"><span data-stu-id="10a50-1046">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="10a50-1047">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="10a50-1047">Az.IotHub</span></span>
* <span data-ttu-id="10a50-1048">Har uppdaterats till den senaste versionen av SDK:n lotHub</span><span class="sxs-lookup"><span data-stu-id="10a50-1048">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="10a50-1049">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="10a50-1049">Az.LogicApp</span></span>
* <span data-ttu-id="10a50-1050">Get-AzLogicApp visar en lista över alla som inte har angivet namn</span><span class="sxs-lookup"><span data-stu-id="10a50-1050">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="10a50-1051">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="10a50-1051">Az.Resources</span></span>
* <span data-ttu-id="10a50-1052">Åtgärdade problem med parameteruppsättningen när parametrarna -ODataQuery och -ResourceId anges för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="10a50-1052">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="10a50-1053">Mer information här: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="10a50-1053">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="10a50-1054">Åtgärdade hantering av parametern -Custom i New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="10a50-1054">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="10a50-1055">Korrigerade stavfel i New-AzDeployment-dokumentationen</span><span class="sxs-lookup"><span data-stu-id="10a50-1055">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="10a50-1056">Gjorde parametern -MailNickname obligatorisk för New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="10a50-1056">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="10a50-1057">Mer information här: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="10a50-1057">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="10a50-1058">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="10a50-1058">Az.SignalR</span></span>
* <span data-ttu-id="10a50-1059">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="10a50-1059">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="10a50-1060">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="10a50-1060">Az.Sql</span></span>
* <span data-ttu-id="10a50-1061">Konverterade lagringshanteringsklientens beroende av den normala SDK-implementeringen.</span><span class="sxs-lookup"><span data-stu-id="10a50-1061">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="10a50-1062">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="10a50-1062">Az.Storage</span></span>
* <span data-ttu-id="10a50-1063">Angav StorageAccountName för lagringskontext som det verkliga namnet på lagringskontot när det skapas med Sas Token, OAuth eller Anonymous</span><span class="sxs-lookup"><span data-stu-id="10a50-1063">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="10a50-1064">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="10a50-1064">New-AzStorageContext</span></span>
* <span data-ttu-id="10a50-1065">Skapade Sas Token för Blob Snapshot-objekt med parametern -FullUri, åtgärdade den returnerade URI:n så att den blir URI för ögonblicksbild</span><span class="sxs-lookup"><span data-stu-id="10a50-1065">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="10a50-1066">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="10a50-1066">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="10a50-1067">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="10a50-1067">Az.Websites</span></span>
* <span data-ttu-id="10a50-1068">Åtgärdade en bugg i datumparsningen i Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="10a50-1068">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="10a50-1069">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="10a50-1069">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="10a50-1070">1.0.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="10a50-1070">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="10a50-1071">Allmänt</span><span class="sxs-lookup"><span data-stu-id="10a50-1071">General</span></span>

- <span data-ttu-id="10a50-1072">Allmän tillgänglighet för Az-modulen</span><span class="sxs-lookup"><span data-stu-id="10a50-1072">General Availability of Az Module</span></span>
- <span data-ttu-id="10a50-1073">Onlinehjälp för varje modul</span><span class="sxs-lookup"><span data-stu-id="10a50-1073">Online help for each module</span></span>
- <span data-ttu-id="10a50-1074">Mer information och en översikt finns på [Az-informationssidan](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="10a50-1074">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="10a50-1075">Information om hur du migrerar från AzureRM finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="10a50-1075">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="10a50-1076">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="10a50-1076">Az.Accounts</span></span>
- <span data-ttu-id="10a50-1077">Har ändrats från Az.Profile</span><span class="sxs-lookup"><span data-stu-id="10a50-1077">Changed from Az.Profile</span></span>
- <span data-ttu-id="10a50-1078">Fasta tabellformat för profil- och kontexttyper</span><span class="sxs-lookup"><span data-stu-id="10a50-1078">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="10a50-1079">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="10a50-1079">Az.ApiManagement</span></span>
- <span data-ttu-id="10a50-1080">Korrigeringar för #7002</span><span class="sxs-lookup"><span data-stu-id="10a50-1080">Fixes for #7002</span></span>
- <span data-ttu-id="10a50-1081">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="10a50-1081">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="10a50-1082">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="10a50-1082">Az.Batch</span></span>
- <span data-ttu-id="10a50-1083">Lade till möjligheten att se vilken version av Azure Batch Node Agent som körs på var och en av de virtuella datorerna i en pool, via den nya egenskapen `NodeAgentInformation` på `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="10a50-1083">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="10a50-1084">Standarden `Caching` för `PSDataDisk` är nu `ReadWrite` i stället för `None`.</span><span class="sxs-lookup"><span data-stu-id="10a50-1084">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="10a50-1085">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="10a50-1085">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="10a50-1086">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="10a50-1086">Az.Billing</span></span>
- <span data-ttu-id="10a50-1087">Kombinerar cmdletarna för fakturering, förbrukning och UsageAggregates. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="10a50-1087">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="10a50-1088">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="10a50-1088">Az.CognitivServices</span></span>
- <span data-ttu-id="10a50-1089">Lade till kompletterare för SkuName och Typem som är tillgängliga i New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="10a50-1089">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="10a50-1090">Tog bort parameteruppsättningen GetSkusWithAccountParamSetName från Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="10a50-1090">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="10a50-1091">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="10a50-1091">Az.ContainerInstance</span></span>
- <span data-ttu-id="10a50-1092">Stöd för ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="10a50-1092">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="10a50-1093">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="10a50-1093">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="10a50-1094">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="10a50-1094">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="10a50-1095">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="10a50-1095">Az.DataLakeStore</span></span>
- <span data-ttu-id="10a50-1096">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="10a50-1096">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="10a50-1097">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="10a50-1097">Az.Monitor</span></span>
- <span data-ttu-id="10a50-1098">Döpte om Az.Insights till Az.Monitor och andra mindre icke-bakåtkompatibla ändringar. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="10a50-1098">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="10a50-1099">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="10a50-1099">Az.KeyVault</span></span>
- <span data-ttu-id="10a50-1100">Tog bort den inaktuella egenskapen PurgeDisabled från utdatatyper</span><span class="sxs-lookup"><span data-stu-id="10a50-1100">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="10a50-1101">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="10a50-1101">Az.MachineLearning</span></span>
- <span data-ttu-id="10a50-1102">Inkluderade cmdletarna från modulen Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="10a50-1102">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="10a50-1103">Az.Media</span><span class="sxs-lookup"><span data-stu-id="10a50-1103">Az.Media</span></span>
- <span data-ttu-id="10a50-1104">Tog bort inaktuella -Tags-alias från New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="10a50-1104">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="10a50-1105">Az.Network</span><span class="sxs-lookup"><span data-stu-id="10a50-1105">Az.Network</span></span>
<span data-ttu-id="10a50-1106">Stöd har lagts till för konfiguration av RewriteRuleSets i Application Gateway</span><span class="sxs-lookup"><span data-stu-id="10a50-1106">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="10a50-1107">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="10a50-1107">New cmdlets added:</span></span>
        - <span data-ttu-id="10a50-1108">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="10a50-1108">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="10a50-1109">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="10a50-1109">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="10a50-1110">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="10a50-1110">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="10a50-1111">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="10a50-1111">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="10a50-1112">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="10a50-1112">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="10a50-1113">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="10a50-1113">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="10a50-1114">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="10a50-1114">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="10a50-1115">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="10a50-1115">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="10a50-1116">Cmdletar har uppdaterats med den valfria parametern -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="10a50-1116">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="10a50-1117">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="10a50-1117">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="10a50-1118">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="10a50-1118">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="10a50-1119">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="10a50-1119">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="10a50-1120">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="10a50-1120">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="10a50-1121">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="10a50-1121">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="10a50-1122">New-AzureRmApplicationGatewayUrlPathMapConfig har lagt till KeyVault-stöd för Application Gateway med Identity.</span><span class="sxs-lookup"><span data-stu-id="10a50-1122">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="10a50-1123">Cmdletar har uppdaterats med den valfria parametern -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="10a50-1123">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="10a50-1124">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="10a50-1124">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="10a50-1125">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="10a50-1125">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="10a50-1126">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="10a50-1126">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="10a50-1127">Cmdleten New-AzApplicationGateway har uppdaterats med den valfria parametern -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="10a50-1127">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="10a50-1128">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="10a50-1128">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="10a50-1129">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="10a50-1129">Az.OperationalInsights</span></span>
- <span data-ttu-id="10a50-1130">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="10a50-1130">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="10a50-1131">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="10a50-1131">Az.Profile</span></span>
- <span data-ttu-id="10a50-1132">Modulnamnet har ändrats till Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="10a50-1132">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="10a50-1133">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="10a50-1133">Az.RecoveryServices</span></span>
- <span data-ttu-id="10a50-1134">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="10a50-1134">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="10a50-1135">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="10a50-1135">Az.Resources</span></span>
- <span data-ttu-id="10a50-1136">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="10a50-1136">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="10a50-1137">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="10a50-1137">Az.ServiceFabric</span></span>
- <span data-ttu-id="10a50-1138">Stöd för specificering av certifikat efter eget namn och tumavtryck</span><span class="sxs-lookup"><span data-stu-id="10a50-1138">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="10a50-1139">Information om fler icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="10a50-1139">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="10a50-1140">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="10a50-1140">Az.SIgnalR</span></span>
- <span data-ttu-id="10a50-1141">Allmän tillgänglighet för PowerShell-cmdletar för SIgnalR</span><span class="sxs-lookup"><span data-stu-id="10a50-1141">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="10a50-1142">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="10a50-1142">Az.Sql</span></span>
- <span data-ttu-id="10a50-1143">Lade till de nya identifieringstyperna Data_Exfiltration och Unsafe_Action i Threat Detection-cmdletar</span><span class="sxs-lookup"><span data-stu-id="10a50-1143">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="10a50-1144">Uppdaterade dokumentationsexempel för Sql Auditing-cmdletar</span><span class="sxs-lookup"><span data-stu-id="10a50-1144">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="10a50-1145">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="10a50-1145">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="10a50-1146">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="10a50-1146">Az.Storage</span></span>
- <span data-ttu-id="10a50-1147">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="10a50-1147">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="10a50-1148">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="10a50-1148">Az.Websites</span></span>
- <span data-ttu-id="10a50-1149">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="10a50-1149">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="10a50-1150">0.7.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="10a50-1150">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="10a50-1151">Allmänt</span><span class="sxs-lookup"><span data-stu-id="10a50-1151">General</span></span>

* <span data-ttu-id="10a50-1152">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="10a50-1152">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="10a50-1153">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="10a50-1153">Az.Compute</span></span>

* <span data-ttu-id="10a50-1154">Lade till stöd för UltraSSD och Galleriavbildningar i de enkla parameteruppsättningarna för `New-AzVm(ss)`-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="10a50-1154">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="10a50-1155">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="10a50-1155">Az.DataLakeStore</span></span>

* <span data-ttu-id="10a50-1156">Åtgärdade avslutande snedstreck i domänen för adls-konto</span><span class="sxs-lookup"><span data-stu-id="10a50-1156">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="10a50-1157">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="10a50-1157">Az.FrontDoor</span></span>

* <span data-ttu-id="10a50-1158">Brutna länkar korrigerades</span><span class="sxs-lookup"><span data-stu-id="10a50-1158">Fixed some broken links</span></span>
    - <span data-ttu-id="10a50-1159">I artiklarna New-AzureRmFrontDoor och Set-AzureRmFrontDoor artiklar korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="10a50-1159">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="10a50-1160">I artikeln New-AzureRmFrontDoorManagedRuleObject korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="10a50-1160">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="10a50-1161">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="10a50-1161">Az.RecoveryServices</span></span>

* <span data-ttu-id="10a50-1162">Lade till valideringar på klientsidan för Azure-filresurs med återställningsåtgärder.</span><span class="sxs-lookup"><span data-stu-id="10a50-1162">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="10a50-1163">Gjorde storageAccountName och storageAccountResourceGroupName valfritt för afs-återställning.</span><span class="sxs-lookup"><span data-stu-id="10a50-1163">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="10a50-1164">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="10a50-1164">Az.Resources</span></span>

* <span data-ttu-id="10a50-1165">Korrigering för https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="10a50-1165">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="10a50-1166">Uppdaterade Get-AzureRmRoleAssignment så att prenumerationsomfattningen används om den anges vid begäran om klassiska administratörer.</span><span class="sxs-lookup"><span data-stu-id="10a50-1166">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="10a50-1167">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="10a50-1167">Az.Sql</span></span>

* <span data-ttu-id="10a50-1168">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="10a50-1168">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="10a50-1169">Korrigerade ett problem med Get-AzureRmSqlDatabaseVulnerabilityAssessment med DotNet-kärna</span><span class="sxs-lookup"><span data-stu-id="10a50-1169">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="10a50-1170">Ändrade dokumentationen för hjälpmeddelanden som rör SQL Auditing-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="10a50-1170">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="10a50-1171">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="10a50-1171">Az.Storage</span></span>

* <span data-ttu-id="10a50-1172">Lade till -EnableHierarchicalNamespace i New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="10a50-1172">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="10a50-1173">Åtgärdade problemet med att cmdleten Copy File inte kunde återanvända källkontexten på målet om inte -DestContext angetts</span><span class="sxs-lookup"><span data-stu-id="10a50-1173">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="10a50-1174">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="10a50-1174">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="10a50-1175">Stöd för statisk webbplatskonfiguration</span><span class="sxs-lookup"><span data-stu-id="10a50-1175">Support Static Website configuration</span></span>
    - <span data-ttu-id="10a50-1176">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="10a50-1176">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="10a50-1177">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="10a50-1177">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="10a50-1178">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="10a50-1178">Az.Websites</span></span>

* <span data-ttu-id="10a50-1179">Set-AzureRmWebApp och Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="10a50-1179">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="10a50-1180">Ny parameter (-AzureStoragePath) har lagts till för att ange att Azure Storage-sökvägar ska monteras i containerappar i Windows och Linux.</span><span class="sxs-lookup"><span data-stu-id="10a50-1180">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="10a50-1181">Använder utdata från den nya cmdleten New-AzureRmWebAppAzureStoragePath som en parameter för att ange sökvägar för Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="10a50-1181">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="10a50-1182">0.6.1 – november 2018</span><span class="sxs-lookup"><span data-stu-id="10a50-1182">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="10a50-1183">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="10a50-1183">Az.ApiManagement</span></span>
* <span data-ttu-id="10a50-1184">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="10a50-1184">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="10a50-1185">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="10a50-1185">Az.Automation</span></span>
* <span data-ttu-id="10a50-1186">Swagger baserade Azure Automation-cmdletar</span><span class="sxs-lookup"><span data-stu-id="10a50-1186">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="10a50-1187">Cmdletar för Uppdateringshantering har lagts till</span><span class="sxs-lookup"><span data-stu-id="10a50-1187">Added Update Management cmdlets</span></span>
* <span data-ttu-id="10a50-1188">Cmdletar för källkontroll har lagts till</span><span class="sxs-lookup"><span data-stu-id="10a50-1188">Added Source Control cmdlets</span></span>
* <span data-ttu-id="10a50-1189">Remove-AzureRmAutomationHybridWorkerGroup-cmdlet har lagts till</span><span class="sxs-lookup"><span data-stu-id="10a50-1189">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="10a50-1190">Kommandot för DSC-registreringsnod har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="10a50-1190">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="10a50-1191">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="10a50-1191">Az.Compute</span></span>
* <span data-ttu-id="10a50-1192">Problem med SystemAssigned-identitet har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="10a50-1192">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="10a50-1193">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="10a50-1193">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="10a50-1194">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="10a50-1194">Az.ContainerInstance</span></span>
* <span data-ttu-id="10a50-1195">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="10a50-1195">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="10a50-1196">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="10a50-1196">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="10a50-1197">uppdatera exempelbeskrivningen för marketplace-cmdletar</span><span class="sxs-lookup"><span data-stu-id="10a50-1197">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="10a50-1198">Az.Network</span><span class="sxs-lookup"><span data-stu-id="10a50-1198">Az.Network</span></span>
* <span data-ttu-id="10a50-1199">Cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomErreller Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="10a50-1199">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="10a50-1200">ICMP tillbaka till stöd för Azure Firewall-nätverksprotokoll har lagts till</span><span class="sxs-lookup"><span data-stu-id="10a50-1200">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="10a50-1201">Uppdatera cmdlet Test-AzureRmNetworkWatcherConnectivity, lägga till verifiering av mål-id, adress och port.</span><span class="sxs-lookup"><span data-stu-id="10a50-1201">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="10a50-1202">Åtgärda problem med minnesanvändning i VirtualNetwork-karta</span><span class="sxs-lookup"><span data-stu-id="10a50-1202">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="10a50-1203">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="10a50-1203">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="10a50-1204">Åtgärda för att ändra principen för en skyddad fildelning.</span><span class="sxs-lookup"><span data-stu-id="10a50-1204">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="10a50-1205">Tidszonsprincipen har konverterats till versaler.</span><span class="sxs-lookup"><span data-stu-id="10a50-1205">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="10a50-1206">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="10a50-1206">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="10a50-1207">Exempel i New-AzureRmRecoveryServicesAsrProtectableItem har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="10a50-1207">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="10a50-1208">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="10a50-1208">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="10a50-1209">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="10a50-1209">Az.Relay</span></span>
* <span data-ttu-id="10a50-1210">Valfri parameter -KeyValue till New-AzureRmRelayKey cmdlet har lagts till, vilket gör det möjligt för användare att tillhandahålla KeyValue.</span><span class="sxs-lookup"><span data-stu-id="10a50-1210">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="10a50-1211">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="10a50-1211">Az.Resources</span></span>
* <span data-ttu-id="10a50-1212">Uppdatera hjälpdokumentation för resursidentitet kopplad till parametrar i `New-AzureRmPolicyAssignment` och `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="10a50-1212">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="10a50-1213">Lägg till ett exempel för New-AzureRmPolicyDefinition som använder -Metadata</span><span class="sxs-lookup"><span data-stu-id="10a50-1213">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="10a50-1214">Korrigera så att skiftläge behålls i taggnycklar i NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="10a50-1214">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="10a50-1215">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="10a50-1215">Az.ServiceFabric</span></span>
* <span data-ttu-id="10a50-1216">Lägg till utfasningsmeddelanden för kommande icke-kompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="10a50-1216">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="10a50-1217">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="10a50-1217">Az.Sql</span></span>
* <span data-ttu-id="10a50-1218">Nya cmdletar för CRUD-åtgärder på Azure Sql Database-hanterad instans och Azure Sql-hanterad databas</span><span class="sxs-lookup"><span data-stu-id="10a50-1218">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="10a50-1219">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="10a50-1219">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="10a50-1220">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="10a50-1220">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="10a50-1221">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="10a50-1221">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="10a50-1222">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="10a50-1222">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="10a50-1223">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="10a50-1223">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="10a50-1224">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="10a50-1224">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="10a50-1225">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="10a50-1225">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="10a50-1226">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="10a50-1226">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="10a50-1227">Hantering av utökad granskningsprincip på en server eller en databas har aktiverats.</span><span class="sxs-lookup"><span data-stu-id="10a50-1227">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="10a50-1228">Ny parameter (PredicateExpression) har lagts till för att aktivera filtrering av granskningsloggar.</span><span class="sxs-lookup"><span data-stu-id="10a50-1228">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="10a50-1229">Cmdletar har ändrats så att de använder SQL-klienter i stället för äldre klienter.</span><span class="sxs-lookup"><span data-stu-id="10a50-1229">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="10a50-1230">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="10a50-1230">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="10a50-1231">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="10a50-1231">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="10a50-1232">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="10a50-1232">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="10a50-1233">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="10a50-1233">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="10a50-1234">Problem med att använda Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings med lagringskontots namnparameter har korrigerats</span><span class="sxs-lookup"><span data-stu-id="10a50-1234">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="10a50-1235">0.5.0 – november 2018</span><span class="sxs-lookup"><span data-stu-id="10a50-1235">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="10a50-1236">Allmänt</span><span class="sxs-lookup"><span data-stu-id="10a50-1236">General</span></span>
* <span data-ttu-id="10a50-1237">Lade till resurskompletterare till många kärn-cmdletar – dessa gör att du kan stega genom befintliga resursnamn med TABB vid interaktiva anrop till cmdletar</span><span class="sxs-lookup"><span data-stu-id="10a50-1237">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="10a50-1238">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="10a50-1238">Az.Profile</span></span>
* <span data-ttu-id="10a50-1239">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="10a50-1239">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="10a50-1240">Bytte namn på parametern TenantId i cmdleten Connect-AzAccount till Tenant och lade till ett alias för TenantId</span><span class="sxs-lookup"><span data-stu-id="10a50-1240">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="10a50-1241">Uppdaterade TenantId-beskrivningen för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="10a50-1241">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="10a50-1242">Åtgärda felmeddelande för misslyckad inloggning när du tillhandahåller klientdomän</span><span class="sxs-lookup"><span data-stu-id="10a50-1242">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="10a50-1243">Åtgärda problem med att kontextnamn hamnar i konflikt för konton utan prenumerationer i klientorganisationen</span><span class="sxs-lookup"><span data-stu-id="10a50-1243">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="10a50-1244">Åtgärda problem med DataLake-slutpunkter vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="10a50-1244">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="10a50-1245">Åtgärdade problem med att Disconnect-AzAccount kastades om den inte anslöts</span><span class="sxs-lookup"><span data-stu-id="10a50-1245">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="10a50-1246">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="10a50-1246">Az.CognitiveServices</span></span>
* <span data-ttu-id="10a50-1247">Lade till åtgärden Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="10a50-1247">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="10a50-1248">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="10a50-1248">Az.Compute</span></span>
* <span data-ttu-id="10a50-1249">Lade till cmdletarna Add-AzVmssVMDataDisk och Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="10a50-1249">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="10a50-1250">Get-AzVMImage visar AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="10a50-1250">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="10a50-1251">Åtgärdade att värdena för alternativen SetAzVMChefExtension -BootstrapOptions och -JsonAttribute inte angavs i json-format.</span><span class="sxs-lookup"><span data-stu-id="10a50-1251">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="10a50-1252">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="10a50-1252">Az.DataLakeStore</span></span>
* <span data-ttu-id="10a50-1253">Uppdatera DataLake-paketet till 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="10a50-1253">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="10a50-1254">Lägg till standardsamtidighet för flertrådade åtgärder.</span><span class="sxs-lookup"><span data-stu-id="10a50-1254">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="10a50-1255">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="10a50-1255">Az.Insights</span></span>
* <span data-ttu-id="10a50-1256">Åtgärdade problem #7267 (autoskalningsområde)</span><span class="sxs-lookup"><span data-stu-id="10a50-1256">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="10a50-1257">Problem med att uppräknade parametrar inte ställdes in ordentligt när du skapade en ny autoskalningsregel (de ställdes alltid in med standardvärdet).</span><span class="sxs-lookup"><span data-stu-id="10a50-1257">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="10a50-1258">Åtgärdade problem #7513 [Insights] Set-AzDiagnosticSetting kräver uttrycklig specifikation av kategorier när inställningar skapas</span><span class="sxs-lookup"><span data-stu-id="10a50-1258">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="10a50-1259">Nu kräver inte cmdleten uttrycklig anvisning av kategorierna för att aktiveras under skapande, d.v.s. den fungerar enligt beskrivning</span><span class="sxs-lookup"><span data-stu-id="10a50-1259">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="10a50-1260">Az.Network</span><span class="sxs-lookup"><span data-stu-id="10a50-1260">Az.Network</span></span>
* <span data-ttu-id="10a50-1261">PeeringType ändrades till en obligatorisk parameter för följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="10a50-1261">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="10a50-1262">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="10a50-1262">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="10a50-1263">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="10a50-1263">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="10a50-1264">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="10a50-1264">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="10a50-1265">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="10a50-1265">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="10a50-1266">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="10a50-1266">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="10a50-1267">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="10a50-1267">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="10a50-1268">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="10a50-1268">Az.PolicyInsights</span></span>
* <span data-ttu-id="10a50-1269">Cmdletar för principreparation har lagts till</span><span class="sxs-lookup"><span data-stu-id="10a50-1269">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="10a50-1270">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="10a50-1270">Az.Resources</span></span>
* <span data-ttu-id="10a50-1271">Korrigering för https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="10a50-1271">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="10a50-1272">Tillåt att resurser listas med parametern -ResourceId för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="10a50-1272">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="10a50-1273">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="10a50-1273">Az.ServiceBus</span></span>
* <span data-ttu-id="10a50-1274">Skrivskyddad MigrationState-egenskap har lagts till i PSServiceBusMigrationConfigurationAttributes, som hjälper till att hålla koll på migreringstillståndet.</span><span class="sxs-lookup"><span data-stu-id="10a50-1274">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="10a50-1275">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="10a50-1275">Az.ServiceFabric</span></span>
* <span data-ttu-id="10a50-1276">Åtgärda att lägga till certifikat till Linux-Vmss.</span><span class="sxs-lookup"><span data-stu-id="10a50-1276">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="10a50-1277">Åtgärdade Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="10a50-1277">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="10a50-1278">Använd rätt tumavtryck från nya certifikat (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="10a50-1278">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="10a50-1279">Visa undantag korrekt (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="10a50-1279">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="10a50-1280">Åtgärdade Update-AzServiceFabricDurability så att klusterkonfigurationen uppdateras innan Vmss-åtgärden CreateOrUpdate påbörjas.</span><span class="sxs-lookup"><span data-stu-id="10a50-1280">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="10a50-1281">0.4.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="10a50-1281">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="10a50-1282">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="10a50-1282">Az.Profile</span></span>
* <span data-ttu-id="10a50-1283">Åtgärdade problemet med Get-AzSubscription i CloudShell</span><span class="sxs-lookup"><span data-stu-id="10a50-1283">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="10a50-1284">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="10a50-1284">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="10a50-1285">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="10a50-1285">Az.Compute</span></span>
* <span data-ttu-id="10a50-1286">Nya storlekar lades till i listan över godkända VM-storlekar för vilka accelererat nätverk kommer att aktiveras vid användning av den enkla parameteruppsättningen för New-AzVm</span><span class="sxs-lookup"><span data-stu-id="10a50-1286">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="10a50-1287">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="10a50-1287">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="10a50-1288">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="10a50-1288">Az.DataLakeStore</span></span>
* <span data-ttu-id="10a50-1289">Lägger till stöd för regler för virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="10a50-1289">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="10a50-1290">Get-AzDataLakeStoreVirtualNetworkRule: Hämtar eller listar regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="10a50-1290">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="10a50-1291">Add-AzDataLakeStoreVirtualNetworkRule: Lägger till en regel för virtuellt nätverk i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="10a50-1291">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="10a50-1292">Set-AzDataLakeStoreVirtualNetworkRule: Ändrar den angivna regeln för virtuellt nätverk i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="10a50-1292">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="10a50-1293">Remove-AzDataLakeStoreVirtualNetworkRule: Tar bort en regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="10a50-1293">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="10a50-1294">Az.Network</span><span class="sxs-lookup"><span data-stu-id="10a50-1294">Az.Network</span></span>
* <span data-ttu-id="10a50-1295">Skicka protokollvärdet till serverdelen för att uppdatera cmdleten Test-AzNetworkWatcherConnectivity.</span><span class="sxs-lookup"><span data-stu-id="10a50-1295">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="10a50-1296">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="10a50-1296">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="10a50-1297">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="10a50-1297">Az.Resources</span></span>
* <span data-ttu-id="10a50-1298">Åtgärdade problem där Get-AzRoleDefinition genererar ett oläsligt undantag (när standardprofilen inte innehåller någon prenumeration och ingen omfattning har angetts) genom att lägga till ett beskrivande undantag i scenariot.</span><span class="sxs-lookup"><span data-stu-id="10a50-1298">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="10a50-1299">Ställ in ”RoleDefinitionNameParameterSet” som standardparameteruppsättning.</span><span class="sxs-lookup"><span data-stu-id="10a50-1299">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="10a50-1300">0.3.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="10a50-1300">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="10a50-1301">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="10a50-1301">Azure.Storage</span></span>
* <span data-ttu-id="10a50-1302">Åtgärda fel där Kopiera blob/fil inte kopierar metadata när målplatsen har ett problem med metadata</span><span class="sxs-lookup"><span data-stu-id="10a50-1302">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="10a50-1303">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="10a50-1303">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="10a50-1304">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="10a50-1304">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="10a50-1305">Stöd för att hämta användningsinformation om en Storage-resurs för en specifik plats och för att lägga till ett varningsmeddelande för att hämta användningsinformation om en global Storage-resurs är inaktuellt.</span><span class="sxs-lookup"><span data-stu-id="10a50-1305">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="10a50-1306">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="10a50-1306">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="10a50-1307">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="10a50-1307">Az.CognitiveServices</span></span>
* <span data-ttu-id="10a50-1308">Stöd för Get-AzCognitiveServicesAccountSkus utan ett befintligt konto.</span><span class="sxs-lookup"><span data-stu-id="10a50-1308">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="10a50-1309">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="10a50-1309">Az.Compute</span></span>
* <span data-ttu-id="10a50-1310">Åtgärdade fel där Get-AzVM -ResourceGroupName <rg> returnerar fler än 50 resultat om det behövs</span><span class="sxs-lookup"><span data-stu-id="10a50-1310">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="10a50-1311">Lade till ett exempel för SimpleParameterSet i hjälpen för cmdleten New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="10a50-1311">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="10a50-1312">Ett stavfel i förloppsmeddelandet för Azure Disk Encryption har korrigerats</span><span class="sxs-lookup"><span data-stu-id="10a50-1312">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="10a50-1313">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="10a50-1313">Az.DataFactoryV2</span></span>
* <span data-ttu-id="10a50-1314">ADF .Net SDK-versionen har uppdaterats till 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="10a50-1314">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="10a50-1315">Az.Network</span><span class="sxs-lookup"><span data-stu-id="10a50-1315">Az.Network</span></span>
* <span data-ttu-id="10a50-1316">Funktionalitet för NetworkProfile har lagts till.</span><span class="sxs-lookup"><span data-stu-id="10a50-1316">Added NetworkProfile functionality.</span></span> <span data-ttu-id="10a50-1317">nya cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="10a50-1317">new cmdlets added</span></span>
    - <span data-ttu-id="10a50-1318">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="10a50-1318">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="10a50-1319">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="10a50-1319">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="10a50-1320">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="10a50-1320">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="10a50-1321">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="10a50-1321">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="10a50-1322">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="10a50-1322">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="10a50-1323">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="10a50-1323">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="10a50-1324">Länk för tjänstassociering på modell för undernät har lagts till</span><span class="sxs-lookup"><span data-stu-id="10a50-1324">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="10a50-1325">Cmdletarna New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap och Remove-AzVirtualNetworkTap har lagts till</span><span class="sxs-lookup"><span data-stu-id="10a50-1325">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="10a50-1326">Cmdletarna Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig och Remove-AzNEtworkInterfaceTapConfig har lagts till</span><span class="sxs-lookup"><span data-stu-id="10a50-1326">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="10a50-1327">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="10a50-1327">Az.RedisCache</span></span>
* <span data-ttu-id="10a50-1328">Tillåt att alla strängar används som storleksparametrar framöver.</span><span class="sxs-lookup"><span data-stu-id="10a50-1328">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="10a50-1329">Lägg till P5 i popup-fönstret PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="10a50-1329">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="10a50-1330">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="10a50-1330">Az.Resources</span></span>
* <span data-ttu-id="10a50-1331">Parametern -Mode som saknades i Set-AzPolicyDefinition har lagts till</span><span class="sxs-lookup"><span data-stu-id="10a50-1331">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="10a50-1332">Åtgärdade buggen för cmdleten Get-AzProviderOperation för åtgärder med ursprung som innehåller användare</span><span class="sxs-lookup"><span data-stu-id="10a50-1332">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="10a50-1333">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="10a50-1333">Az.Sql</span></span>
* <span data-ttu-id="10a50-1334">Ett problem där vissa cmdletar för säkerhetskopiering inte kunde identifiera den aktuella azure-prenumerationen har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="10a50-1334">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="10a50-1335">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="10a50-1335">Az.Websites</span></span>
* <span data-ttu-id="10a50-1336">Ny cmdlet: Get-AzWebAppContainerContinuousDeploymentUrl – Hämtar webhook-URL:en för kontinuerlig distribution av container</span><span class="sxs-lookup"><span data-stu-id="10a50-1336">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="10a50-1337">Nya cmdletar: New-AzWebAppContainerPSSession och Enter-WebAppContainerPSSession – Startar en PowerShell-fjärrsession i en containerapp för windows</span><span class="sxs-lookup"><span data-stu-id="10a50-1337">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="10a50-1338">0.2.0 – september 2018</span><span class="sxs-lookup"><span data-stu-id="10a50-1338">0.2.0 - September 2018</span></span>
 <span data-ttu-id="10a50-1339">Första versionen</span><span class="sxs-lookup"><span data-stu-id="10a50-1339">Initial Release</span></span>