---
title: Viktig information om Azure PowerShell
description: Lär dig mer om alla de senaste uppdateringarna för Azure PowerShell-modulerna.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/15/2019
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 2929d7ebaf26e069b12c5b6451e333255ae740af
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/01/2020
ms.locfileid: "89244338"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="ff5be-103">Viktig information om Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="ff5be-103">Azure PowerShell release notes</span></span>
## <a name="280---october-2019"></a><span data-ttu-id="ff5be-104">2.8.0 – oktober 2019</span><span class="sxs-lookup"><span data-stu-id="ff5be-104">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="ff5be-105">Allmänt</span><span class="sxs-lookup"><span data-stu-id="ff5be-105">General</span></span>
* <span data-ttu-id="ff5be-106">AZ. HealthcareApis 1.0.0-version</span><span class="sxs-lookup"><span data-stu-id="ff5be-106">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="ff5be-107">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ff5be-107">Az.Accounts</span></span>
* <span data-ttu-id="ff5be-108">Uppdatera telemetri och URL-omskrivning för genererade moduler, korrigera Windows-enhetstester.</span><span class="sxs-lookup"><span data-stu-id="ff5be-108">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="ff5be-109">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ff5be-109">Az.ApiManagement</span></span>
* <span data-ttu-id="ff5be-110">**Set-AzApiManagementApi** – Tillagt stöd för att uppdatera Api till ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="ff5be-110">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="ff5be-111">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="ff5be-111">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ff5be-112">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ff5be-112">Az.Automation</span></span>
* <span data-ttu-id="ff5be-113">Åtgärdade cmdleten New-AzureAutomationSoftwareUpdateConfiguration för parametern för inställning av Linux-omstart.</span><span class="sxs-lookup"><span data-stu-id="ff5be-113">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="ff5be-114">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="ff5be-114">Az.Batch</span></span>
* <span data-ttu-id="ff5be-115">**Get-AzBatchNodeAgentSku** är inaktuell och ersätts av **Get-AzBatchSupportImage** i version 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="ff5be-115">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ff5be-116">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ff5be-116">Az.Compute</span></span>
* <span data-ttu-id="ff5be-117">Lägg till parametrarna Priority, EvictionPolicy och MaxPrice till cmdletarna New-AzVM och New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ff5be-117">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="ff5be-118">Korrigera varningsmeddelande och hjälpdokument för cmdletarna Add-AzVMAdditionalUnattendContent och Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="ff5be-118">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="ff5be-119">Åtgärda – skipVmBackup-undantag för virtuella Linux-datorer med hanterade diskar för Set-AzVMDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="ff5be-119">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="ff5be-120">Åtgärda fel i uppdatera krypteringsinställningarna i set-AzVMDiskEncryptionExtension, scenario i två steg.</span><span class="sxs-lookup"><span data-stu-id="ff5be-120">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ff5be-121">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ff5be-121">Az.DataFactory</span></span>
* <span data-ttu-id="ff5be-122">Lägga till CRUD-kommandon för ADF V2-dataflödet: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow och Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="ff5be-122">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="ff5be-123">Lägger till åtgärdskommandon för ADF V2-dataflödesfelsökningssession: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand och Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="ff5be-123">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="ff5be-124">Uppdatera ADF .Net SDK-versionen till 4.2.0</span><span class="sxs-lookup"><span data-stu-id="ff5be-124">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ff5be-125">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ff5be-125">Az.DataLakeStore</span></span>
* <span data-ttu-id="ff5be-126">Korrigera kontovalidering så att konton med ”-” kan skickas utan domän</span><span class="sxs-lookup"><span data-stu-id="ff5be-126">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="ff5be-127">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="ff5be-127">Az.HealthcareApis</span></span>
* <span data-ttu-id="ff5be-128">PowerShell-versionen har uppdaterats till 1.0.0</span><span class="sxs-lookup"><span data-stu-id="ff5be-128">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="ff5be-129">Uppdaterade SDK-versionen till 1.0.2</span><span class="sxs-lookup"><span data-stu-id="ff5be-129">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="ff5be-130">Uppdatera i tester för att referera till en ny SDK-version</span><span class="sxs-lookup"><span data-stu-id="ff5be-130">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="ff5be-131">Utdatastrukturen har uppdaterats från kapslad till förenklad.</span><span class="sxs-lookup"><span data-stu-id="ff5be-131">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ff5be-132">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ff5be-132">Az.IotHub</span></span>
* <span data-ttu-id="ff5be-133">Lägg till ny routningskälla: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="ff5be-133">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="ff5be-134">Mindre felkorrigering: Get-AzIothub returnerar inte subscriptionId</span><span class="sxs-lookup"><span data-stu-id="ff5be-134">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ff5be-135">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ff5be-135">Az.Monitor</span></span>
* <span data-ttu-id="ff5be-136">Nya åtgärdsgruppsmottagare har lagts till för New-AzActionGroupReceiver:   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="ff5be-136">New action group receivers added for New-AzActionGroupReceiver:   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="ff5be-137">Använd vanligt aviseringsschema som är aktiverat för mottagarna.</span><span class="sxs-lookup"><span data-stu-id="ff5be-137">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="ff5be-138">Detta gäller inte för SMS, push för Azure-app, ITSM och röstmottagare</span><span class="sxs-lookup"><span data-stu-id="ff5be-138">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="ff5be-139">Webhooks har nu stöd för Azure Active Directory-autentisering.</span><span class="sxs-lookup"><span data-stu-id="ff5be-139">Webhooks now supports Azure active directory authentication.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ff5be-140">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ff5be-140">Az.Network</span></span>
* <span data-ttu-id="ff5be-141">Lägg till ny cmdlet Get-AzAvailableServiceAlias som kan anropas för att hämta de alias som kan användas för tjänstslutpunktsprinciper.</span><span class="sxs-lookup"><span data-stu-id="ff5be-141">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="ff5be-142">Stöd för tillägg av trafikväljare har lagts till i gatewayanslutningar för virtuella nätverk</span><span class="sxs-lookup"><span data-stu-id="ff5be-142">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="ff5be-143">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="ff5be-143">New cmdlets added:</span></span>
        - <span data-ttu-id="ff5be-144">New-AzIpsecTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="ff5be-144">New-AzIpsecTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="ff5be-145">Cmdletar har uppdaterats med den valfria parametern -TrafficSelectorPolicies</span><span class="sxs-lookup"><span data-stu-id="ff5be-145">Cmdlets updated with optional parameter -TrafficSelectorPolicies</span></span>
        - <span data-ttu-id="ff5be-146">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ff5be-146">New-AzVirtualNetworkGatewayConnection</span></span>
        - <span data-ttu-id="ff5be-147">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ff5be-147">Set-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="ff5be-148">Lägg till stöd för ESP- och AH-protokoll i konfiguration av nätverkssäkerhetsregler</span><span class="sxs-lookup"><span data-stu-id="ff5be-148">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="ff5be-149">Uppdaterade cmdletar:</span><span class="sxs-lookup"><span data-stu-id="ff5be-149">Updated cmdlets:</span></span>
        - <span data-ttu-id="ff5be-150">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ff5be-150">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="ff5be-151">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ff5be-151">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="ff5be-152">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ff5be-152">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="ff5be-153">Förbättra hanteringen av undantag i Cortex-cmdletar</span><span class="sxs-lookup"><span data-stu-id="ff5be-153">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="ff5be-154">Nya generationer och SKU:er för VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="ff5be-154">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="ff5be-155">Introducera nya generationer för VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="ff5be-155">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="ff5be-156">Introducera nya SKU:er med högt dataflöde för VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="ff5be-156">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="ff5be-157">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="ff5be-157">Az.RedisCache</span></span>
* <span data-ttu-id="ff5be-158">Uppdaterad referensdokumentation för ”set-AzRedisCache” för att inkludera saknade värden för parametern ”size”</span><span class="sxs-lookup"><span data-stu-id="ff5be-158">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="ff5be-159">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ff5be-159">Az.Sql</span></span>
* <span data-ttu-id="ff5be-160">Lägg till stöd för inställningen Active Directory administratör på den hanterade instansen</span><span class="sxs-lookup"><span data-stu-id="ff5be-160">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ff5be-161">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ff5be-161">Az.Storage</span></span>
* <span data-ttu-id="ff5be-162">Uppdatera Lagringsklientbibliotek till 11.1.0</span><span class="sxs-lookup"><span data-stu-id="ff5be-162">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="ff5be-163">Lista containrar med hanteringsplans-API, kommer att listas med NextPageLink</span><span class="sxs-lookup"><span data-stu-id="ff5be-163">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="ff5be-164">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ff5be-164">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="ff5be-165">Lista lagringskonton från prenumerationen, kommer att listas med NextPageLink</span><span class="sxs-lookup"><span data-stu-id="ff5be-165">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="ff5be-166">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ff5be-166">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="ff5be-167">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="ff5be-167">Az.StorageSync</span></span>
* <span data-ttu-id="ff5be-168">Åtgärda problemet 9810 i Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="ff5be-168">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ff5be-169">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ff5be-169">Az.Websites</span></span>
* <span data-ttu-id="ff5be-170">Set-AzWebApp – uppdatering av ASP för en app misslyckades</span><span class="sxs-lookup"><span data-stu-id="ff5be-170">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="ff5be-171">2.7.0 – september 2019</span><span class="sxs-lookup"><span data-stu-id="ff5be-171">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="ff5be-172">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ff5be-172">Az.ApiManagement</span></span>
* <span data-ttu-id="ff5be-173">Uppdatera ”-Format”-parameterbeskrivningen i ”Set-AzApiManagementPolicy”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="ff5be-173">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="ff5be-174">Referenser för den föråldrade cmdleten ”Update-AzApiManagementDeployment” har tagits bort från referensdokumentationen.</span><span class="sxs-lookup"><span data-stu-id="ff5be-174">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="ff5be-175">Använd ”Set-AzApiManagement” i stället.</span><span class="sxs-lookup"><span data-stu-id="ff5be-175">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ff5be-176">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ff5be-176">Az.Automation</span></span>
* <span data-ttu-id="ff5be-177">Stavfel har korrigerats i exempel i referensdokumentationen för ”Register-AzAutomationDscNode”</span><span class="sxs-lookup"><span data-stu-id="ff5be-177">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="ff5be-178">Klargörande har lagts till om OS-begränsningar för Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="ff5be-178">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="ff5be-179">Null-referensundantag har korrigerats för -Wait-alternativet i Start-AzAutomationRunbook-cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ff5be-179">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ff5be-180">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ff5be-180">Az.Compute</span></span>
* <span data-ttu-id="ff5be-181">Lägg till UploadSizeInBytes-parameter till New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="ff5be-181">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="ff5be-182">Lägg till Incremental-parameter till New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="ff5be-182">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="ff5be-183">Lägg till en funktion för virtuella datorer med låg prioritet:</span><span class="sxs-lookup"><span data-stu-id="ff5be-183">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="ff5be-184">MaxPrice-, EvictionPolicy- och Priority-parametrar har lagts till i New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="ff5be-184">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="ff5be-185">MaxPrice-parametern har lagts till i New-AzVmssConfig-, Update-AzVM- och Update-AzVmss-cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="ff5be-185">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="ff5be-186">Åtgärda problem med VM-referenser för Get-AzAvailabilitySet-cmdleten när alla tillgänglighetsuppsättningar i prenumerationen visas.</span><span class="sxs-lookup"><span data-stu-id="ff5be-186">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="ff5be-187">Korrigera null-undantaget för Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="ff5be-187">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="ff5be-188">Korrigera VHD-metoden för sökning relativt till slut.</span><span class="sxs-lookup"><span data-stu-id="ff5be-188">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="ff5be-189">Åtgärda UltraSSD-problem för New-AzVM och Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="ff5be-189">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ff5be-190">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ff5be-190">Az.DataFactory</span></span>
* <span data-ttu-id="ff5be-191">Lägger till 3 nya kommandon för ADF V2 – Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription och Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="ff5be-191">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="ff5be-192">ADF .Net SDK har uppdaterats till 4.1.3</span><span class="sxs-lookup"><span data-stu-id="ff5be-192">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="ff5be-193">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="ff5be-193">Az.HDInsight</span></span>
* <span data-ttu-id="ff5be-194">Anrop för icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="ff5be-194">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ff5be-195">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ff5be-195">Az.IotHub</span></span>
* <span data-ttu-id="ff5be-196">Lägg till stöd för att anropa redundans för en IotHub till den geo-länkade katastrofåterställningsregionen.</span><span class="sxs-lookup"><span data-stu-id="ff5be-196">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="ff5be-197">Lägg till stöd för att hantera meddelandeberikning för en IotHub.</span><span class="sxs-lookup"><span data-stu-id="ff5be-197">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="ff5be-198">Nya cmdlet:ar är:</span><span class="sxs-lookup"><span data-stu-id="ff5be-198">New cmdlets are:</span></span>
    - <span data-ttu-id="ff5be-199">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="ff5be-199">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="ff5be-200">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="ff5be-200">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="ff5be-201">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="ff5be-201">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="ff5be-202">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="ff5be-202">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ff5be-203">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ff5be-203">Az.Monitor</span></span>
* <span data-ttu-id="ff5be-204">Pekar på den senaste Monitor SDK:n, dvs. 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="ff5be-204">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="ff5be-205">Lägger till bakåtkompatibla ändringar i Metrics-cmdletarna, dvs. enhetsuppräkningen stöder flera nya värden.</span><span class="sxs-lookup"><span data-stu-id="ff5be-205">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="ff5be-206">Detta är skrivskyddade cmdletar, så det förekommer inga ändringar i inmatningen för cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="ff5be-206">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="ff5be-207">API-versionen för **ActionGroups**-begäranden är nu **2019-06-01**. Tidigare var den **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="ff5be-207">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="ff5be-208">Test av scenarier har uppdaterats för att anpassas till den här ändringen.</span><span class="sxs-lookup"><span data-stu-id="ff5be-208">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="ff5be-209">Ett nytt obligatoriskt argument har lagts till för konstruktorerna för klasserna **EmailReceiver** och **WebhookReceiver** – ett booleskt värde med namnet **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="ff5be-209">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="ff5be-210">Värdet är för närvarande fast till **false** så att den här icke-bakåtkompatibla ändringen är dold från cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="ff5be-210">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="ff5be-211">**Obs!** Det här är en tillfällig ändring som måste verifieras av Alerts-teamet.</span><span class="sxs-lookup"><span data-stu-id="ff5be-211">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="ff5be-212">Ordningen på argumenten för konstruktorn för klassen **Source** (relaterad till klassen **ScheduledQueryRuleSource**) har ändrats från den tidigare SDK:n.</span><span class="sxs-lookup"><span data-stu-id="ff5be-212">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="ff5be-213">Den här ändringen krävde korrigering av två enhetstest: de kompilerades, men testerna skickades inte.</span><span class="sxs-lookup"><span data-stu-id="ff5be-213">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="ff5be-214">Ordningen på argumenten för konstruktorn för klassen **AlertingAction** (relaterad till klassen **ScheduledQueryRuleSource**) har ändrats från den tidigare SDK:n.</span><span class="sxs-lookup"><span data-stu-id="ff5be-214">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="ff5be-215">Den här ändringen krävde korrigering av två enhetstest: de kompilerades, men testerna skickades inte.</span><span class="sxs-lookup"><span data-stu-id="ff5be-215">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="ff5be-216">Stöd för kriterier för dynamiskt tröskelvärde för måttavisering v2</span><span class="sxs-lookup"><span data-stu-id="ff5be-216">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="ff5be-217">New-AzMetricAlertRuleV2Criteria: skapar nu även kriterier för dynamiskt tröskelvärde</span><span class="sxs-lookup"><span data-stu-id="ff5be-217">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="ff5be-218">Add-AzMetricAlertRuleV2: accepterar nu även kriterier för dynamiskt tröskelvärde</span><span class="sxs-lookup"><span data-stu-id="ff5be-218">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="ff5be-219">Förbättringar i schemalagd frågeregel (SQR)</span><span class="sxs-lookup"><span data-stu-id="ff5be-219">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="ff5be-220">Cmdletar accepterar ”Location”-parameter i båda formaten, antingen platsen (t.ex. eastus) eller platsens visningsnamn (t.ex. USA, östra)</span><span class="sxs-lookup"><span data-stu-id="ff5be-220">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="ff5be-221">”Enabled”-parametern illustreras korrekt i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="ff5be-221">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="ff5be-222">Exempel för den valfria parametern ”ActionGroup” har lagts till</span><span class="sxs-lookup"><span data-stu-id="ff5be-222">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="ff5be-223">Förbättrade hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="ff5be-223">Overall improved help files</span></span>
* <span data-ttu-id="ff5be-224">Åtgärda bugg då omfattningstypen fastställs för ”Set-AzActionRule”</span><span class="sxs-lookup"><span data-stu-id="ff5be-224">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ff5be-225">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ff5be-225">Az.Network</span></span>
* <span data-ttu-id="ff5be-226">Korrigera felaktigt exempel i referensdokumentationen för ”New-AzApplicationGateway”</span><span class="sxs-lookup"><span data-stu-id="ff5be-226">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="ff5be-227">Lägg till anmärkning i ”Get-AzNetworkWatcherPacketCapture”-referensdokumentationen om hämtning av alla egenskaper för en paketinsamling</span><span class="sxs-lookup"><span data-stu-id="ff5be-227">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="ff5be-228">Exempel har korrigerats i ”Test-AzNetworkWatcherIPFlow”-referensdokumentationen för korrekt uppräkning av nätverkskort</span><span class="sxs-lookup"><span data-stu-id="ff5be-228">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="ff5be-229">Förbättrad tolkning av molnundantag för att visa eventuell ytterligare information</span><span class="sxs-lookup"><span data-stu-id="ff5be-229">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="ff5be-230">Förbättrad tolkning av molnundantag för att hantera ytterligare en typ av SDK-undantag</span><span class="sxs-lookup"><span data-stu-id="ff5be-230">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="ff5be-231">Felaktig mappning av säkerhetsregelmodeller har korrigerats</span><span class="sxs-lookup"><span data-stu-id="ff5be-231">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="ff5be-232">Egenskaper har lagts till för nätverksgränssnittet för funktionen Privat IP</span><span class="sxs-lookup"><span data-stu-id="ff5be-232">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="ff5be-233">Egenskapen ”PrivateEndpoint” har lagts till som en typ av PSResourceId till PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="ff5be-233">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="ff5be-234">Egenskapen ”PrivateLinkConnectionProperties” har lagts till som en typ av PSIpConfigurationConnectivityInformation till PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ff5be-234">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="ff5be-235">Modellklassen PSIpConfigurationConnectivityInformation har lagts till</span><span class="sxs-lookup"><span data-stu-id="ff5be-235">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="ff5be-236">ApplicationRuleProtocolType ”mssql” har lagts till för Azure Firewall-resurs</span><span class="sxs-lookup"><span data-stu-id="ff5be-236">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="ff5be-237">MultiLink-stöd i virtuellt WAN</span><span class="sxs-lookup"><span data-stu-id="ff5be-237">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="ff5be-238">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="ff5be-238">New cmdlets</span></span>
        - <span data-ttu-id="ff5be-239">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="ff5be-239">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="ff5be-240">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="ff5be-240">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="ff5be-241">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="ff5be-241">Updated cmdlet:</span></span>
        - <span data-ttu-id="ff5be-242">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="ff5be-242">New-VpnSite</span></span>
        - <span data-ttu-id="ff5be-243">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="ff5be-243">Update-VpnSite</span></span>
        - <span data-ttu-id="ff5be-244">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="ff5be-244">New-VpnConnection</span></span>
        - <span data-ttu-id="ff5be-245">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="ff5be-245">Update-VpnConnection</span></span>
* <span data-ttu-id="ff5be-246">Dokument för vissa PowerShell-exempel har korrigerats så att Az-cmdletar används i stället för AzureRM-cmdletar</span><span class="sxs-lookup"><span data-stu-id="ff5be-246">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ff5be-247">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ff5be-247">Az.RecoveryServices</span></span>
* <span data-ttu-id="ff5be-248">Uppdatera AzureVMpolicy-objekt med ProtectedItemsCount-attribut</span><span class="sxs-lookup"><span data-stu-id="ff5be-248">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="ff5be-249">Ytterligare tester har lagts till för VM-princip och återställning av ursprungligt lagringskonto</span><span class="sxs-lookup"><span data-stu-id="ff5be-249">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="ff5be-250">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ff5be-250">Az.Resources</span></span>
* <span data-ttu-id="ff5be-251">Åtgärda fel där det inte gick att anropa New-AzRoleAssignment utan parametern Scope.</span><span class="sxs-lookup"><span data-stu-id="ff5be-251">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="ff5be-252">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ff5be-252">Az.ServiceFabric</span></span>
* <span data-ttu-id="ff5be-253">Stavfel har korrigerats i exempel för ”Update-AzServiceFabricReliability”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="ff5be-253">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="ff5be-254">Lägger till nya cmdletar för att hantera program och tjänster:</span><span class="sxs-lookup"><span data-stu-id="ff5be-254">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="ff5be-255">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="ff5be-255">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="ff5be-256">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="ff5be-256">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="ff5be-257">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="ff5be-257">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="ff5be-258">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="ff5be-258">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="ff5be-259">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="ff5be-259">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="ff5be-260">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="ff5be-260">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="ff5be-261">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="ff5be-261">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="ff5be-262">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="ff5be-262">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="ff5be-263">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="ff5be-263">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="ff5be-264">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="ff5be-264">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="ff5be-265">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="ff5be-265">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="ff5be-266">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="ff5be-266">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="ff5be-267">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="ff5be-267">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="ff5be-268">Service Fabric SDK har uppgraderats till version 1.2.0 som använder Service Fabric-resursprovidern med API-version 2019-03-01.</span><span class="sxs-lookup"><span data-stu-id="ff5be-268">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="ff5be-269">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="ff5be-269">Az.SignalR</span></span>
* <span data-ttu-id="ff5be-270">Lägg till Update-, Restart-, CheckNameAvailability- och GetUsage-cmdletar</span><span class="sxs-lookup"><span data-stu-id="ff5be-270">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="ff5be-271">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ff5be-271">Az.Sql</span></span>
* <span data-ttu-id="ff5be-272">Uppdatera exempel i referensdokumentationen för ”Get-AzSqlElasticPool”</span><span class="sxs-lookup"><span data-stu-id="ff5be-272">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="ff5be-273">vCore-exempel för att skapa en elastisk pool (New-AzSqlElasticPool) har lagts till.</span><span class="sxs-lookup"><span data-stu-id="ff5be-273">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="ff5be-274">Ta bort verifieringen av EmailAddresses och kontrollen som bekräftar att EmailAdmins inte är falskt när EmailAddresses är tomt i Set-AzSqlServerAdvancedThreatProtectionPolicy och Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="ff5be-274">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="ff5be-275">Server-/databasgranskningsinställningar kan tas bort när det finns flera diagnostikinställningar som aktiverar granskningskategorin.</span><span class="sxs-lookup"><span data-stu-id="ff5be-275">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="ff5be-276">Åtgärda verifiering av e-postadresser i flera Sql Vulnerability Assessment-cmdletar (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting och Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="ff5be-276">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ff5be-277">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ff5be-277">Az.Storage</span></span>
* <span data-ttu-id="ff5be-278">Exempel i referensdokumentationen för ”Get-AzStorageAccountKey” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="ff5be-278">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="ff5be-279">Vid upp- och nedladdning av en Azure-fil kan SMB-egenskaperna för källfilen (t.ex. filattribut, tidpunkten då filen skapades och tidpunkten för den senaste skrivningen) sparas i målfilen</span><span class="sxs-lookup"><span data-stu-id="ff5be-279">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="ff5be-280">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="ff5be-280">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="ff5be-281">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="ff5be-281">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="ff5be-282">Korrigera problem med uppladdningen av blockblob med egenskaper/metadata för ImmutabilityPolicy i containrar.</span><span class="sxs-lookup"><span data-stu-id="ff5be-282">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="ff5be-283">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="ff5be-283">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="ff5be-284">Stöd för hantering av Azure-filresurser med API för hanteringsplan</span><span class="sxs-lookup"><span data-stu-id="ff5be-284">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="ff5be-285">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="ff5be-285">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="ff5be-286">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="ff5be-286">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="ff5be-287">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="ff5be-287">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="ff5be-288">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="ff5be-288">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ff5be-289">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ff5be-289">Az.Websites</span></span>
* <span data-ttu-id="ff5be-290">Åtgärda problemet där webbapp-taggar togs bort när appen migrerades till en ny ASP</span><span class="sxs-lookup"><span data-stu-id="ff5be-290">Fixing issue where webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="ff5be-291">Åtgärda Publish-AzureWebapp så att det fungerar i Linux och Windows</span><span class="sxs-lookup"><span data-stu-id="ff5be-291">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="ff5be-292">Uppdatera exempel i ”Get-AzWebAppPublishingProfile”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="ff5be-292">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="ff5be-293">2.6.0 – augusti 2019</span><span class="sxs-lookup"><span data-stu-id="ff5be-293">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="ff5be-294">Allmänt</span><span class="sxs-lookup"><span data-stu-id="ff5be-294">General</span></span>
* <span data-ttu-id="ff5be-295">Åtgärdade diverse skrivfel i flera moduler</span><span class="sxs-lookup"><span data-stu-id="ff5be-295">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="ff5be-296">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ff5be-296">Az.Accounts</span></span>
* <span data-ttu-id="ff5be-297">Stöd för användartilldelat MSI i Azure Functions-autentisering (#9479)</span><span class="sxs-lookup"><span data-stu-id="ff5be-297">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="ff5be-298">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="ff5be-298">Az.Aks</span></span>
* <span data-ttu-id="ff5be-299">Åtgärda problem med utdata för "Get-AzAks"</span><span class="sxs-lookup"><span data-stu-id="ff5be-299">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="ff5be-300">Mer information här: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="ff5be-300">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="ff5be-301">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ff5be-301">Az.ApiManagement</span></span>
* <span data-ttu-id="ff5be-302">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="ff5be-302">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="ff5be-303">Uppdatera .net-NuGet-versionen, som inte tillämpar begränsningar för productId, apiId och userId</span><span class="sxs-lookup"><span data-stu-id="ff5be-303">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="ff5be-304">**Get-AzApiManagementProduct** – Lade till stöd för frågekörning mot produkter via API.</span><span class="sxs-lookup"><span data-stu-id="ff5be-304">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="ff5be-305">**New-AzApiManagementApiRevision** – Korrigering för problem där ApiRevisionDescription inte angavs vid skapande av ny API-revision https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="ff5be-305">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="ff5be-306">Åtgärdade skrivfel i modellen "PsApiManagementOAuth2AuthrozationServer" till "PsApiManagementOAuth2AuthorizationServer"</span><span class="sxs-lookup"><span data-stu-id="ff5be-306">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="ff5be-307">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="ff5be-307">Az.Batch</span></span>
* <span data-ttu-id="ff5be-308">Åtgärdade skrivfel i hjälpmeddelande och dokumentation till att skriva Windows med versaler</span><span class="sxs-lookup"><span data-stu-id="ff5be-308">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="ff5be-309">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="ff5be-309">Az.Cdn</span></span>
* <span data-ttu-id="ff5be-310">Åtgärdade skrivfel i CDN-modulens konverteringshjälp</span><span class="sxs-lookup"><span data-stu-id="ff5be-310">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ff5be-311">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ff5be-311">Az.Compute</span></span>
* <span data-ttu-id="ff5be-312">Lägg till VmssId i New-AzVMConfig-cmdleten</span><span class="sxs-lookup"><span data-stu-id="ff5be-312">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="ff5be-313">Lägg till parametrarna TerminateScheduledEvents och TerminateScheduledEventNotBeforeTimeoutInMinutes i New-AzVmssConfig och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ff5be-313">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="ff5be-314">Lägg till egenskapen HyperVGeneration till avbildningsobjekt för virtuell dator</span><span class="sxs-lookup"><span data-stu-id="ff5be-314">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="ff5be-315">Lägg till funktioner för Host och HostGroup</span><span class="sxs-lookup"><span data-stu-id="ff5be-315">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="ff5be-316">Nya cmdletar:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="ff5be-316">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="ff5be-317">HostId-parametern läggs till i New-AzVMConfig och New-AzVM</span><span class="sxs-lookup"><span data-stu-id="ff5be-317">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="ff5be-318">Uppdatera exempel i "Invoke-AzVMRunCommand"-dokumentationen till att använda rätt parameternamn</span><span class="sxs-lookup"><span data-stu-id="ff5be-318">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="ff5be-319">Uppdatera "-VolumeType"-beskrivningen i referensdokumentationen för "set-AzVMDiskEncryptionExtension" och "set-AzVmssDiskEncryptionExtension"</span><span class="sxs-lookup"><span data-stu-id="ff5be-319">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ff5be-320">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ff5be-320">Az.DataFactory</span></span>
* <span data-ttu-id="ff5be-321">Åtgärda skrivfel till att använda versaler för "Windows" i "New-AzDataFactoryEncryptValue"-dokumentationen</span><span class="sxs-lookup"><span data-stu-id="ff5be-321">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="ff5be-322">Uppdaterade ADF .Net SDK-versionen till 4.1.2</span><span class="sxs-lookup"><span data-stu-id="ff5be-322">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="ff5be-323">Lägg till parametrarna "DataProxyIntegrationRuntimeName", "DataProxyStagingLinkedServiceName" och "DataProxyStagingPath" för "Set-AzureRmDataFactoryV2IntegrationRuntime"-cmd för att aktivera konfiguration av lokalt installerad integrationskörning som en proxy för SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="ff5be-323">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="ff5be-324">Uppdaterade PSTriggerRun till att visa utlöst pipeline, meddelande och egenskaper samt PSActivityRun till att visa aktivitetstypen</span><span class="sxs-lookup"><span data-stu-id="ff5be-324">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ff5be-325">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ff5be-325">Az.DataLakeStore</span></span>
* <span data-ttu-id="ff5be-326">Korrigering av frysning av Get-DataLakeStoreDeletedItem för fel eller fjärrundantag.</span><span class="sxs-lookup"><span data-stu-id="ff5be-326">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="ff5be-327">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="ff5be-327">Az.EventHub</span></span>
* <span data-ttu-id="ff5be-328">Korrigering av problem #9658 : Skrivfel i parametern VirtualNteworkRule i Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="ff5be-328">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="ff5be-329">Korrigering av problem #9558 : Set-AzEventHubNamespace använder PATCH i stället för PUT</span><span class="sxs-lookup"><span data-stu-id="ff5be-329">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="ff5be-330">lade till parametern EnableKafka i Set-AzEventHubNamespace-cmdleten</span><span class="sxs-lookup"><span data-stu-id="ff5be-330">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="ff5be-331">Korrigering av problem #9786 : kan inte skapa en regel med Endast lyssna-behörighet</span><span class="sxs-lookup"><span data-stu-id="ff5be-331">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="ff5be-332">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="ff5be-332">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="ff5be-333">Åtgärdade skrivfel i dokumentation där "Azure" skrevs helt med gemener</span><span class="sxs-lookup"><span data-stu-id="ff5be-333">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ff5be-334">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ff5be-334">Az.Monitor</span></span>
* <span data-ttu-id="ff5be-335">Åtgärdade felaktigt parameternamn i hjälpdokumentationen</span><span class="sxs-lookup"><span data-stu-id="ff5be-335">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ff5be-336">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ff5be-336">Az.Network</span></span>
* <span data-ttu-id="ff5be-337">Uppdaterade New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="ff5be-337">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="ff5be-338">Gjorde parametern "PublicIpAddress" inaktuell eftersom den aldrig används på serversidan.</span><span class="sxs-lookup"><span data-stu-id="ff5be-338">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="ff5be-339">Lade till den valfria parametern "Primary", som anger huruvida den aktuella IP-konfigurationen är den primära.</span><span class="sxs-lookup"><span data-stu-id="ff5be-339">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="ff5be-340">Förbättrade hanteringen av felundantag för begärande från SDK – åtgärdar problemet att tidigare SDK-undantag inte hanteras på rätt sätt, vilket leder till att viktig felinformation inte visas</span><span class="sxs-lookup"><span data-stu-id="ff5be-340">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="ff5be-341">Justerade valideringslogiken för IPv6-IP-prefix till att kontrollera korrekt IPv6-prefixlängd.</span><span class="sxs-lookup"><span data-stu-id="ff5be-341">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="ff5be-342">Uppdaterade Get-AzVirtualNetworkSubnetConfig: Lade till parameter som anges till get av undernätets resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="ff5be-342">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="ff5be-343">Uppdaterade beskrivningen av parametern Location för AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="ff5be-343">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="ff5be-344">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ff5be-344">Az.OperationalInsights</span></span>
* <span data-ttu-id="ff5be-345">Uppdaterade dokumentation för "New-AzOperationalInsightsLinuxSyslogDataSource"</span><span class="sxs-lookup"><span data-stu-id="ff5be-345">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="ff5be-346">Lade till exempel</span><span class="sxs-lookup"><span data-stu-id="ff5be-346">Added example</span></span>
    - <span data-ttu-id="ff5be-347">Uppdaterade beskrivningen av parametern "-Name"</span><span class="sxs-lookup"><span data-stu-id="ff5be-347">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="ff5be-348">Lade till ett exempel för New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="ff5be-348">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="ff5be-349">Ändrade beskrivningen av parametern -Name för New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="ff5be-349">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ff5be-350">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ff5be-350">Az.RecoveryServices</span></span>
* <span data-ttu-id="ff5be-351">Uppdatera "Get-AzRecoveryServicesBackupJobDetail.md"</span><span class="sxs-lookup"><span data-stu-id="ff5be-351">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="ff5be-352">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ff5be-352">Az.Resources</span></span>
* <span data-ttu-id="ff5be-353">Lägg till stöd för den nya API-versionen från 2019-05-10 för Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="ff5be-353">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="ff5be-354">Lägg till stöd för "copy.count = 0" för variabler, resurser och egenskaper</span><span class="sxs-lookup"><span data-stu-id="ff5be-354">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="ff5be-355">Resurser med "condition = false" eller "copy.count = 0" tas bort i complete-läget</span><span class="sxs-lookup"><span data-stu-id="ff5be-355">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="ff5be-356">Lägg till ett exempel på tilldelning av princip på prenumerationsnivå i hjälpdokumentationen</span><span class="sxs-lookup"><span data-stu-id="ff5be-356">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="ff5be-357">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ff5be-357">Az.ServiceBus</span></span>
* <span data-ttu-id="ff5be-358">Korrigering av problem #9658 : Skrivfel i parametern VirtualNetworkRule i set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="ff5be-358">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="ff5be-359">Korrigering av problem #9786 : kan inte skapa en regel med Endast lyssna-behörighet</span><span class="sxs-lookup"><span data-stu-id="ff5be-359">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="ff5be-360">Lade till det nya kommandot "Test-AzServiceBusNameAvailability" för att kontrollera namntillgängligheten för kö och ämne</span><span class="sxs-lookup"><span data-stu-id="ff5be-360">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="ff5be-361">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ff5be-361">Az.ServiceFabric</span></span>
* <span data-ttu-id="ff5be-362">Åtgärda buggar med tillägg av nodtyps-cmdlet:</span><span class="sxs-lookup"><span data-stu-id="ff5be-362">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="ff5be-363">NullReferenceException-bugg när resursgrupp hade annan vmss som inte är relaterad till Service Fabric-klustret.</span><span class="sxs-lookup"><span data-stu-id="ff5be-363">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="ff5be-364">Åtgärdar problemet: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="ff5be-364">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="ff5be-365">Åtgärda bugg där cmdleten misslyckades om virtualNetwork var i en annan resursgrupp än klustret.</span><span class="sxs-lookup"><span data-stu-id="ff5be-365">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="ff5be-366">Åtgärdar problemet: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="ff5be-366">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="ff5be-367">AzServiceFabricApplicationCertificate-cmdleten görs inaktuell</span><span class="sxs-lookup"><span data-stu-id="ff5be-367">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="ff5be-368">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ff5be-368">Az.Sql</span></span>
* <span data-ttu-id="ff5be-369">Uppdatera dokumentation om gamla gransknings-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="ff5be-369">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ff5be-370">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ff5be-370">Az.Storage</span></span>
* <span data-ttu-id="ff5be-371">Uppdatera hjälpen för Get/Close-AzStorageFileHandle genom att lägga till fler scenarier i cmdlet-exempel och uppdatera parameterbeskrivningar</span><span class="sxs-lookup"><span data-stu-id="ff5be-371">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="ff5be-372">Stöd för StandardBlobTier i uppladdningsblob och kopieringsblob</span><span class="sxs-lookup"><span data-stu-id="ff5be-372">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="ff5be-373">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="ff5be-373">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="ff5be-374">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="ff5be-374">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="ff5be-375">Stöd för rehydratiseringsprioritet i kopieringsblob</span><span class="sxs-lookup"><span data-stu-id="ff5be-375">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="ff5be-376">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="ff5be-376">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ff5be-377">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ff5be-377">Az.Websites</span></span>
* <span data-ttu-id="ff5be-378">Lägg till klargöranden gällande parametern -AppSettings i Set-AzWebApp och Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ff5be-378">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="ff5be-379">2.5.0 – July 2019</span><span class="sxs-lookup"><span data-stu-id="ff5be-379">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ff5be-380">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ff5be-380">Az.Accounts</span></span>
* <span data-ttu-id="ff5be-381">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="ff5be-381">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="ff5be-382">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="ff5be-382">Az.ApplicationInsights</span></span>
* <span data-ttu-id="ff5be-383">Korrigera skrivfel i exempel i dokumentationen för Remove-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="ff5be-383">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ff5be-384">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ff5be-384">Az.Automation</span></span>
* <span data-ttu-id="ff5be-385">Korrigera skrivfel i resurssträng</span><span class="sxs-lookup"><span data-stu-id="ff5be-385">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="ff5be-386">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ff5be-386">Az.CognitiveServices</span></span>
* <span data-ttu-id="ff5be-387">Stöd för NetworkRuleSet har lagts till.</span><span class="sxs-lookup"><span data-stu-id="ff5be-387">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ff5be-388">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ff5be-388">Az.Compute</span></span>
* <span data-ttu-id="ff5be-389">Lägg till saknade egenskaper (ComputerName, OsName, OsVersion och HyperVGeneration) för visningsobjekt i den virtuella datorinstansen.</span><span class="sxs-lookup"><span data-stu-id="ff5be-389">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="ff5be-390">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ff5be-390">Az.ContainerRegistry</span></span>
* <span data-ttu-id="ff5be-391">Åtgärda skrivfel i Remove-AzContainerRegistryReplication för parametern Replication</span><span class="sxs-lookup"><span data-stu-id="ff5be-391">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="ff5be-392">Mer information finns här: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="ff5be-392">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ff5be-393">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ff5be-393">Az.DataFactory</span></span>
* <span data-ttu-id="ff5be-394">ADF .Net SDK-versionen har uppdaterats till 4.1.0</span><span class="sxs-lookup"><span data-stu-id="ff5be-394">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="ff5be-395">Korrigera skrivfel i dokumentationen för Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="ff5be-395">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="ff5be-396">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="ff5be-396">Az.EventHub</span></span>
* <span data-ttu-id="ff5be-397">Ny cmmdlet har lagts till för att skapa SAS-token: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="ff5be-397">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="ff5be-398">verifierings- och felmeddelande har lagts till för authorizationrules-rättigheter om endast "hantera" har tilldelats</span><span class="sxs-lookup"><span data-stu-id="ff5be-398">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="ff5be-399">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ff5be-399">Az.KeyVault</span></span>
* <span data-ttu-id="ff5be-400">Stöd har lagts till för att ange KeySize för certifikatprinciper</span><span class="sxs-lookup"><span data-stu-id="ff5be-400">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="ff5be-401">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="ff5be-401">Az.LogicApp</span></span>
* <span data-ttu-id="ff5be-402">Korrigering för Get-AzIntegrationAccountMap för att lista alla mappningstyper</span><span class="sxs-lookup"><span data-stu-id="ff5be-402">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="ff5be-403">Ny MapType-parameter har lagts till för filtrering</span><span class="sxs-lookup"><span data-stu-id="ff5be-403">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="ff5be-404">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="ff5be-404">Az.ManagedServices</span></span>
* <span data-ttu-id="ff5be-405">Stöd för API-versionen 2019-06-01 (GA) har lagts till</span><span class="sxs-lookup"><span data-stu-id="ff5be-405">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ff5be-406">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ff5be-406">Az.Network</span></span>
* <span data-ttu-id="ff5be-407">Lägg till stöd för privat slutpunkt och privat länktjänst</span><span class="sxs-lookup"><span data-stu-id="ff5be-407">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="ff5be-408">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="ff5be-408">New cmdlets</span></span>
        - <span data-ttu-id="ff5be-409">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="ff5be-409">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="ff5be-410">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ff5be-410">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="ff5be-411">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ff5be-411">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="ff5be-412">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ff5be-412">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="ff5be-413">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ff5be-413">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="ff5be-414">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ff5be-414">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="ff5be-415">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="ff5be-415">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="ff5be-416">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ff5be-416">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="ff5be-417">Nedanstående kommandon för funktionen har uppdaterats: Flaggan PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies på undernätet i VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ff5be-417">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="ff5be-418">Uppdaterade New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="ff5be-418">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="ff5be-419">Valfri parameter har lagts till – PrivateEndpointNetworkPoliciesFlag som konfigurerar huruvida nätverksprinciper ska tillämpas på en privat slutpunkt i det här undernätet.</span><span class="sxs-lookup"><span data-stu-id="ff5be-419">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="ff5be-420">Valfri parameter har lagts till – PrivateLinkServiceNetworkPoliciesFlag som konfigurerar huruvida nätverksprinciper ska tillämpas på en privat länktjänst i det här undernätet.</span><span class="sxs-lookup"><span data-stu-id="ff5be-420">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="ff5be-421">AzPrivateLinkService för cmdlet-parametern ServiceName har bytt namn till Name med aliaset ServiceName för bakåtkompatibilitet</span><span class="sxs-lookup"><span data-stu-id="ff5be-421">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="ff5be-422">Aktivera ICMP-protokoll för konfiguration av nätverkssäkerhetsregler</span><span class="sxs-lookup"><span data-stu-id="ff5be-422">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="ff5be-423">Uppdaterade cmdletar</span><span class="sxs-lookup"><span data-stu-id="ff5be-423">Updated cmdlets</span></span>
        - <span data-ttu-id="ff5be-424">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ff5be-424">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="ff5be-425">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ff5be-425">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="ff5be-426">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ff5be-426">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="ff5be-427">Lägg till ConnectionProtocolType (Ikev1/Ikev2) som en konfigurerbar parameter för New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ff5be-427">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="ff5be-428">Lägg till PrivateIpAddressVersion i LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="ff5be-428">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="ff5be-429">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="ff5be-429">Updated cmdlet:</span></span>
        - <span data-ttu-id="ff5be-430">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ff5be-430">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="ff5be-431">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ff5be-431">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="ff5be-432">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ff5be-432">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="ff5be-433">Uppdatering av Application Gateway-kommandot New-AzApplicationGatewayProbeConfig för stöd av anpassad port i Probe</span><span class="sxs-lookup"><span data-stu-id="ff5be-433">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="ff5be-434">Uppdaterade New-AzApplicationGatewayProbeConfig: Den valfria parametern Port som används för avsökning i serverdelen har lagts till.</span><span class="sxs-lookup"><span data-stu-id="ff5be-434">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="ff5be-435">Denna parameter gäller för SKU:erna Standard_V2 och WAF_V2.</span><span class="sxs-lookup"><span data-stu-id="ff5be-435">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="ff5be-436">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ff5be-436">Az.OperationalInsights</span></span>
* <span data-ttu-id="ff5be-437">Uppdaterade standardversionen för sparade sökningar till 1.</span><span class="sxs-lookup"><span data-stu-id="ff5be-437">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="ff5be-438">Åtgärdade hantering av anpassad log null regex</span><span class="sxs-lookup"><span data-stu-id="ff5be-438">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ff5be-439">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ff5be-439">Az.RecoveryServices</span></span>
* <span data-ttu-id="ff5be-440">Uppdatera Get-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="ff5be-440">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="ff5be-441">Uppdatera Get-AzRecoveryServicesBackupContainer.md</span><span class="sxs-lookup"><span data-stu-id="ff5be-441">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="ff5be-442">Uppdatera Get-AzRecoveryServicesVault.md</span><span class="sxs-lookup"><span data-stu-id="ff5be-442">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="ff5be-443">Uppdatera Wait-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="ff5be-443">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="ff5be-444">Uppdatera Set-AzRecoveryServicesVaultContext.md</span><span class="sxs-lookup"><span data-stu-id="ff5be-444">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="ff5be-445">Uppdatera Get-AzRecoveryServicesBackupItem.md</span><span class="sxs-lookup"><span data-stu-id="ff5be-445">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="ff5be-446">Uppdatera Get-AzRecoveryServicesBackupRecoveryPoint.md</span><span class="sxs-lookup"><span data-stu-id="ff5be-446">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="ff5be-447">Uppdatera Restore-AzRecoveryServicesBackupItem.md</span><span class="sxs-lookup"><span data-stu-id="ff5be-447">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="ff5be-448">Uppdaterat tjänstanrop för avregistrering av container för Azure-filresurs</span><span class="sxs-lookup"><span data-stu-id="ff5be-448">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="ff5be-449">Uppdatera Set-AzRecoveryServicesAsrAlertSetting.md</span><span class="sxs-lookup"><span data-stu-id="ff5be-449">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="ff5be-450">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ff5be-450">Az.Resources</span></span>
- <span data-ttu-id="ff5be-451">Ta bort den cmdlet som saknas och som refereras i dokumentationen till New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ff5be-451">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="ff5be-452">Princip-cmdletar har uppdaterats så att de använder den nya API-versionen 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="ff5be-452">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="ff5be-453">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ff5be-453">Az.ServiceBus</span></span>
* <span data-ttu-id="ff5be-454">Ny cmmdlet har lagts till för att skapa SAS-token: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="ff5be-454">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="ff5be-455">verifierings- och felmeddelande har lagts till för authorizationrules-rättigheter om endast "hantera" har tilldelats</span><span class="sxs-lookup"><span data-stu-id="ff5be-455">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="ff5be-456">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ff5be-456">Az.Sql</span></span>
* <span data-ttu-id="ff5be-457">Åtgärda saknade exempel för Set-AzSqlDatabaseSecondary cmdlet</span><span class="sxs-lookup"><span data-stu-id="ff5be-457">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="ff5be-458">Åtgärda angivna återkommande genomsökningar för bedömning av säkerhetsrisk utan angivna e-postadresser</span><span class="sxs-lookup"><span data-stu-id="ff5be-458">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="ff5be-459">Korrigera ett skrivfel i ett varningsmeddelande.</span><span class="sxs-lookup"><span data-stu-id="ff5be-459">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ff5be-460">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ff5be-460">Az.Storage</span></span>
* <span data-ttu-id="ff5be-461">Uppdatera exempel i referensdokumentationen för Get-AzStorageAccount så att rätt parameternamn används</span><span class="sxs-lookup"><span data-stu-id="ff5be-461">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="ff5be-462">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="ff5be-462">Az.StorageSync</span></span>
* <span data-ttu-id="ff5be-463">Lägger till cmdleten Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="ff5be-463">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="ff5be-464">Åtgärda problem 9551 så att TierFilesOlderThanDays föredras</span><span class="sxs-lookup"><span data-stu-id="ff5be-464">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ff5be-465">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ff5be-465">Az.Websites</span></span>
* <span data-ttu-id="ff5be-466">Åtgärdar ett fel där vissa SiteConfig-egenskaper inte returnerades av Get-AzWebApp och Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ff5be-466">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="ff5be-467">Lägger till en ny platsparameter för Get-AzDeletedWebApp och Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="ff5be-467">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="ff5be-468">Åtgärdar ett fel i kloning av webbapp-platser som använder New-AzWebApp-IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="ff5be-468">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="ff5be-469">2.4.0 – juli 2019</span><span class="sxs-lookup"><span data-stu-id="ff5be-469">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ff5be-470">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ff5be-470">Az.Accounts</span></span>
* <span data-ttu-id="ff5be-471">Lägg till stöd för profil-cmdletar</span><span class="sxs-lookup"><span data-stu-id="ff5be-471">Add support for profile cmdlets</span></span>
* <span data-ttu-id="ff5be-472">Lägg till stöd för miljöer och dataplaner i genererade cmdletar</span><span class="sxs-lookup"><span data-stu-id="ff5be-472">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="ff5be-473">Åtgärda bugg där fel slutpunkt i vissa fall användes för cmdletar för dataplaner i Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="ff5be-473">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="ff5be-474">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="ff5be-474">Az.Advisor</span></span>
* <span data-ttu-id="ff5be-475">GA-version av Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="ff5be-475">GA release of Az.Advisor</span></span>
* <span data-ttu-id="ff5be-476">Den här modulen ingår nu som en del av `Az`-sammanslagningsmodulen</span><span class="sxs-lookup"><span data-stu-id="ff5be-476">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="ff5be-477">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ff5be-477">Az.ApiManagement</span></span>
* <span data-ttu-id="ff5be-478">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="ff5be-478">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="ff5be-479">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="ff5be-479">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="ff5be-480">Stöd för att fråga prenumerationer efter användare och produkt har lagts till</span><span class="sxs-lookup"><span data-stu-id="ff5be-480">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="ff5be-481">Stöd för att fråga med hjälp av omfång ”/”, ”/apis”, ”/apis/echo-api” har lagts till</span><span class="sxs-lookup"><span data-stu-id="ff5be-481">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="ff5be-482">Korrigering av problem https://github.com/Azure/azure-powershell/issues/9307 och https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="ff5be-482">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="ff5be-483">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="ff5be-483">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="ff5be-484">Stöd för att ange ”ApiVersion” och ”ApiVersionSetId” när API:er importeras har lagts till</span><span class="sxs-lookup"><span data-stu-id="ff5be-484">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ff5be-485">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ff5be-485">Az.Automation</span></span>
* <span data-ttu-id="ff5be-486">Bugg med cmdleten Set-AzAutomationConnectionFieldValue för att hantera strängvärde har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="ff5be-486">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ff5be-487">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ff5be-487">Az.Compute</span></span>
* <span data-ttu-id="ff5be-488">Lägg till parametern HyperVGeneration i New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="ff5be-488">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ff5be-489">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ff5be-489">Az.DataFactory</span></span>
* <span data-ttu-id="ff5be-490">Uppdaterar utdata från ADF-cmdletar som hämtar aktivitetskörningar, hämtar pipelinekörningar och hämtar utlösarkörningar för stöd för Select-Object-pipe.</span><span class="sxs-lookup"><span data-stu-id="ff5be-490">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="ff5be-491">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="ff5be-491">Az.EventGrid</span></span>
* <span data-ttu-id="ff5be-492">Korrigera stavfel i dokumentation om ”New-AzEventGridSubscription”</span><span class="sxs-lookup"><span data-stu-id="ff5be-492">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ff5be-493">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ff5be-493">Az.IotHub</span></span>
* <span data-ttu-id="ff5be-494">Lägg till stöd för att återskapa principnycklar för auktorisering.</span><span class="sxs-lookup"><span data-stu-id="ff5be-494">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ff5be-495">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ff5be-495">Az.Network</span></span>
* <span data-ttu-id="ff5be-496">”RoutingPreference” har lagts till i offentliga IP-taggar</span><span class="sxs-lookup"><span data-stu-id="ff5be-496">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="ff5be-497">Förbättra exempel för referensdokumentation om ”Get-AzNetworkServiceTag”</span><span class="sxs-lookup"><span data-stu-id="ff5be-497">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="ff5be-498">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="ff5be-498">Az.PolicyInsights</span></span>
* <span data-ttu-id="ff5be-499">Åtgärda problem med null-referens i Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="ff5be-499">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="ff5be-500">Mer information här: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="ff5be-500">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="ff5be-501">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ff5be-501">Az.OperationalInsights</span></span>
* <span data-ttu-id="ff5be-502">Modellen för CustomLog-datakälla som returneras i Get-AzOperationalInsightsDataSource har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="ff5be-502">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ff5be-503">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ff5be-503">Az.RecoveryServices</span></span>
* <span data-ttu-id="ff5be-504">Kommandot get-policy för IaaSVM:er har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="ff5be-504">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="ff5be-505">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ff5be-505">Az.Resources</span></span>
    - <span data-ttu-id="ff5be-506">Korrigera hjälptext för den översta parametern i Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="ff5be-506">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="ff5be-507">Lägg till växlingsstöd på klientsidan för Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="ff5be-507">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="ff5be-508">Lägg till nya parametrar för Set-AzPolicyAssignment, -PolicyParameters och -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="ff5be-508">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="ff5be-509">En mängd dokument- och exempeluppdateringar för Policy-cmdletar</span><span class="sxs-lookup"><span data-stu-id="ff5be-509">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="ff5be-510">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ff5be-510">Az.ServiceBus</span></span>
* <span data-ttu-id="ff5be-511">Korrigering av problem #4938 – New-AzureRmServiceBusQueue returnerar BadRequest vid konfiguration av MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="ff5be-511">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="ff5be-512">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ff5be-512">Az.Sql</span></span>
* <span data-ttu-id="ff5be-513">Lägg till cmdletar för instansredundansgrupper från förhandsversion till offentlig version</span><span class="sxs-lookup"><span data-stu-id="ff5be-513">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="ff5be-514">Stöd för granskning för Azure SQL Server\Database med nya cmdletar.</span><span class="sxs-lookup"><span data-stu-id="ff5be-514">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="ff5be-515">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="ff5be-515">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="ff5be-516">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="ff5be-516">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="ff5be-517">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="ff5be-517">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="ff5be-518">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="ff5be-518">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="ff5be-519">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="ff5be-519">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="ff5be-520">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="ff5be-520">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="ff5be-521">Ta bort begränsningar för e-post från inställningarna för sårbarhetsbedömning</span><span class="sxs-lookup"><span data-stu-id="ff5be-521">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ff5be-522">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ff5be-522">Az.Storage</span></span>
* <span data-ttu-id="ff5be-523">Ändra två parametrar ”-IndexDocument” och ”-ErrorDocument404Path” från ”krävs” till ”valfri” i cmdlet:</span><span class="sxs-lookup"><span data-stu-id="ff5be-523">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="ff5be-524">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="ff5be-524">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="ff5be-525">Uppdatera hjälpen för Get-AzStorageBlobContent genom att lägga till ett exempel</span><span class="sxs-lookup"><span data-stu-id="ff5be-525">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="ff5be-526">Visa mer felinformation när cmdleten misslyckas med StorageException</span><span class="sxs-lookup"><span data-stu-id="ff5be-526">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="ff5be-527">Stöd för att skapa eller uppdatera lagringskonto med Azure Files AAD DS-autentisering</span><span class="sxs-lookup"><span data-stu-id="ff5be-527">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="ff5be-528">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ff5be-528">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="ff5be-529">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ff5be-529">Set-AzStorageAccount</span></span>
* <span data-ttu-id="ff5be-530">Stöd för att lista eller stänga filreferenser för en filresurs, filkatalog eller en fil</span><span class="sxs-lookup"><span data-stu-id="ff5be-530">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="ff5be-531">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="ff5be-531">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="ff5be-532">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="ff5be-532">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="ff5be-533">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="ff5be-533">Az.StorageSync</span></span>
* <span data-ttu-id="ff5be-534">Den här modulen ingår nu som en del av `Az`-sammanslagningsmodulen</span><span class="sxs-lookup"><span data-stu-id="ff5be-534">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="ff5be-535">2.3.2 – juni 2019</span><span class="sxs-lookup"><span data-stu-id="ff5be-535">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ff5be-536">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ff5be-536">Az.Accounts</span></span>
* <span data-ttu-id="ff5be-537">Åtgärda bugg med felaktiga webbadresser som i vissa fall användes för Functions-anrop</span><span class="sxs-lookup"><span data-stu-id="ff5be-537">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="ff5be-538">Mer information här: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="ff5be-538">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="ff5be-539">Åtgärda problem med alias från AzureRM i Az-cmdletar</span><span class="sxs-lookup"><span data-stu-id="ff5be-539">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="ff5be-540">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="ff5be-540">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="ff5be-541">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="ff5be-541">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ff5be-542">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ff5be-542">Az.Compute</span></span>
* <span data-ttu-id="ff5be-543">Parameteruppsättningarna New-AzVm och New-AzVmss accepterar nu parametern ”ProximityPlacementGroup”.</span><span class="sxs-lookup"><span data-stu-id="ff5be-543">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="ff5be-544">Stavfel i referensdokumentationen för ”New-AzVM” har korrigerats</span><span class="sxs-lookup"><span data-stu-id="ff5be-544">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="ff5be-545">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="ff5be-545">Az.Dns</span></span>
* <span data-ttu-id="ff5be-546">Stavfel i hjälpexempel för ”Set-AzDnsZone” har korrigerats.</span><span class="sxs-lookup"><span data-stu-id="ff5be-546">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="ff5be-547">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="ff5be-547">Az.EventGrid</span></span>
* <span data-ttu-id="ff5be-548">Har uppdaterats för att använda API-versionen 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="ff5be-548">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="ff5be-549">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="ff5be-549">New cmdlets:</span></span>
    - <span data-ttu-id="ff5be-550">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="ff5be-550">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="ff5be-551">Skapar en ny Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="ff5be-551">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="ff5be-552">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="ff5be-552">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="ff5be-553">Hämtar information om en Event Grid-domän eller hämtar en lista med alla Event Grid-domäner i den aktuella Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="ff5be-553">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="ff5be-554">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="ff5be-554">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="ff5be-555">Tar bort en Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="ff5be-555">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="ff5be-556">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="ff5be-556">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="ff5be-557">Återskapar nyckeln för delad åtkomst för en Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="ff5be-557">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="ff5be-558">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="ff5be-558">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="ff5be-559">Hämtar de nycklar för delad åtkomst som används för att publicera händelser till en Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="ff5be-559">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="ff5be-560">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="ff5be-560">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="ff5be-561">Skapar ett nytt Azure Event Grid-domänämne.</span><span class="sxs-lookup"><span data-stu-id="ff5be-561">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="ff5be-562">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="ff5be-562">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="ff5be-563">Hämtar information om ett Event Grid-domänämne eller hämtar en lista med alla Event Grid-domänämnen under en specifik Event Grid-domän i nuvarande Azure</span><span class="sxs-lookup"><span data-stu-id="ff5be-563">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="ff5be-564">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="ff5be-564">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="ff5be-565">Tar bort ett befintligt Azure Event Grid-domänämne.</span><span class="sxs-lookup"><span data-stu-id="ff5be-565">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="ff5be-566">Uppdaterade cmdletar:</span><span class="sxs-lookup"><span data-stu-id="ff5be-566">Updated cmdlets:</span></span>
    - <span data-ttu-id="ff5be-567">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="ff5be-567">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="ff5be-568">Lägg till nya obligatoriska parametrar för att stödja piping för den nya Event Grid-domänen och Event Grid-domänämnet för att göra det möjligt att skapa nya händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="ff5be-568">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="ff5be-569">Lägg till nya obligatoriska parametrar för att ange det nya Event Grid-domännamnet och/eller namnet på Event Grid-domänämnet för att göra det möjligt att skapa nya händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="ff5be-569">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="ff5be-570">Lägg till ny parameteruppsättningar för domäner och domänämnen för att göra det möjligt att återanvända befintliga parametrar (t.ex. EndPointType, SubjectBeginsWith osv).</span><span class="sxs-lookup"><span data-stu-id="ff5be-570">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="ff5be-571">Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="ff5be-571">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="ff5be-572">Förfallodatum för händelseprenumeration</span><span class="sxs-lookup"><span data-stu-id="ff5be-572">Event subscription expiration date,</span></span>
            - <span data-ttu-id="ff5be-573">Avancerade filterparametrar.</span><span class="sxs-lookup"><span data-stu-id="ff5be-573">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="ff5be-574">Lägg till ny uppräkning för servicebusqueue som mål.</span><span class="sxs-lookup"><span data-stu-id="ff5be-574">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="ff5be-575">Tillåt inte användning av ”Alla” i alternativet -IncludedEventType och ersätt det med</span><span class="sxs-lookup"><span data-stu-id="ff5be-575">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="ff5be-576">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="ff5be-576">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="ff5be-577">Lägg till ny valfria parametrar (Top, ODataQuery och NextLink) för att stödja sidnumrering och filtrering av resultat.</span><span class="sxs-lookup"><span data-stu-id="ff5be-577">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="ff5be-578">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="ff5be-578">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="ff5be-579">Lägg till nya obligatoriska parametrar för att stödja piping för en Event Grid-domän och Event Grid-domänämnen för att göra det möjligt att ta bort befintliga händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="ff5be-579">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="ff5be-580">Lägg till nya obligatoriska parametrar för att ange Event Grid-domännamnet och/eller namnet på Event Grid-domänämnet för att göra det möjligt att ta bort befintliga händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="ff5be-580">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="ff5be-581">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="ff5be-581">Az.FrontDoor</span></span>
* <span data-ttu-id="ff5be-582">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="ff5be-582">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="ff5be-583">Lägg till stöd för transformeringar och nytt värde för automatisk komplettering för operatorer (RegEx)</span><span class="sxs-lookup"><span data-stu-id="ff5be-583">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="ff5be-584">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="ff5be-584">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="ff5be-585">Lägg till nya värden för automatisk komplettering</span><span class="sxs-lookup"><span data-stu-id="ff5be-585">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ff5be-586">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ff5be-586">Az.Network</span></span>
* <span data-ttu-id="ff5be-587">Lägg till stöd för resurs för virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="ff5be-587">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="ff5be-588">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="ff5be-588">New cmdlets</span></span>
        - <span data-ttu-id="ff5be-589">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="ff5be-589">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="ff5be-590">Lägg till AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="ff5be-590">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="ff5be-591">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="ff5be-591">New cmdlets</span></span>
        - <span data-ttu-id="ff5be-592">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="ff5be-592">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="ff5be-593">Lägg till PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ff5be-593">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="ff5be-594">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="ff5be-594">New cmdlets</span></span>
        - <span data-ttu-id="ff5be-595">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ff5be-595">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="ff5be-596">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ff5be-596">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="ff5be-597">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ff5be-597">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="ff5be-598">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="ff5be-598">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="ff5be-599">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ff5be-599">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="ff5be-600">Lägg till PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="ff5be-600">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="ff5be-601">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="ff5be-601">New cmdlets</span></span>
        - <span data-ttu-id="ff5be-602">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="ff5be-602">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="ff5be-603">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="ff5be-603">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="ff5be-604">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="ff5be-604">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="ff5be-605">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="ff5be-605">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="ff5be-606">Nedanstående kommandon för funktionen har uppdaterats: Flaggan UseLocalAzureIpAddress på VpnConnection</span><span class="sxs-lookup"><span data-stu-id="ff5be-606">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="ff5be-607">New-AzVpnConnection har uppdaterats: Den valfria parametern -UseLocalAzureIpAddress har lagts till för att visa att en lokal IP-adress i Azure ska användas som källadress när anslutningen initieras.</span><span class="sxs-lookup"><span data-stu-id="ff5be-607">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="ff5be-608">Set-AzVpnConnection har uppdaterats: Den valfria parametern -UseLocalAzureIpAddress har lagts till för att visa att en lokal IP-adress i Azure ska användas som källadress när anslutningen initieras.</span><span class="sxs-lookup"><span data-stu-id="ff5be-608">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="ff5be-609">Det skrivskyddade fältet PeeredConnections har lagts till i ExpressRoute-peering.</span><span class="sxs-lookup"><span data-stu-id="ff5be-609">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="ff5be-610">Det skrivskyddade fältet GlobalReachEnabled har lagts till i ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="ff5be-610">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="ff5be-611">Ett attribut för icke-bakåtkompatibla ändringar har lagts till för att lyfta fram utfasning av fältet AllowGlobalReach i modellen ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ff5be-611">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="ff5be-612">Problem 8756 har åtgärdats: Fel vid användning av TargetListenerID med AzApplicationGatewayRedirectConfiguration-cmdletar</span><span class="sxs-lookup"><span data-stu-id="ff5be-612">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="ff5be-613">En bugg i New-AzApplicationGatewayPathRuleConfig som gjorde att regeluppsättningen för att återskapa inte kunde anges har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="ff5be-613">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="ff5be-614">Visningen av VirtualNetworkTaps i NetworkInterfaceIpConfiguration har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="ff5be-614">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="ff5be-615">Cortex Get-cmdletar för att visa en lista med alla delar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="ff5be-615">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="ff5be-616">Funktionen för att skapa VirtualHub-referenser för ExpressRouteGateways och VpnGateway har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="ff5be-616">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="ff5be-617">Stöd för tillgänglighetszoner i AzureFirewall och NatGateway har lagts till</span><span class="sxs-lookup"><span data-stu-id="ff5be-617">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="ff5be-618">Cmdleten Get-AzNetworkServiceTag har lagts till</span><span class="sxs-lookup"><span data-stu-id="ff5be-618">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="ff5be-619">Lägg till stöd för flera offentliga IP-adresser för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="ff5be-619">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="ff5be-620">Cmdleten New-AzFirewall har uppdaterats:</span><span class="sxs-lookup"><span data-stu-id="ff5be-620">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="ff5be-621">Parametern -PublicIpAddress som accepterar ett eller flera offentliga IP-adressobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="ff5be-621">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="ff5be-622">Parametern -VirtualNetwork som accepterar ett virtuellt nätverksobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="ff5be-622">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="ff5be-623">Metoderna AddPublicIpAddress och RemovePublicIpAddress har lagts till på brandväggsobjekt – dessa accepterar ett offentligt IP-adressobjekt som indata</span><span class="sxs-lookup"><span data-stu-id="ff5be-623">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="ff5be-624">Inaktuella parametrar -PublicIpName och -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="ff5be-624">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="ff5be-625">Nedanstående kommandon för funktionen har uppdaterats: Ange autentiseringsalternativ för VpnClient AAD till resurser för virtuella nätverksgatewayer.</span><span class="sxs-lookup"><span data-stu-id="ff5be-625">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="ff5be-626">New-AzVirtualNetworkGateway har uppdaterats: De valfria parametrarna AadTenantUri, AadAudienceId och AadIssuerUri för att ange VpnClient AAD-autentiseringsalternativ på en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="ff5be-626">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="ff5be-627">Set-AzVirtualNetworkGateway har uppdaterats: De valfria parametrarna AadTenantUri, AadAudienceId och AadIssuerUri för att ange VpnClient AAD-autentiseringsalternativ på en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="ff5be-627">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="ff5be-628">Set-AzVirtualNetworkGateway har uppdaterats: Den valfria växelparametern RemoveAadAuthentication som tar bort VpnClient AAD-autentiseringsalternativ från en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="ff5be-628">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="ff5be-629">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ff5be-629">Az.OperationalInsights</span></span>
* <span data-ttu-id="ff5be-630">Aktivera prisnivån **pergb2018** i kommandot ”New-AzureRmOperationalInsightsWorkspace”</span><span class="sxs-lookup"><span data-stu-id="ff5be-630">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="ff5be-631">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ff5be-631">Az.Resources</span></span>
* <span data-ttu-id="ff5be-632">Stöd för ytterligare alternativ för att exportera en mall</span><span class="sxs-lookup"><span data-stu-id="ff5be-632">Support for additional Template Export options</span></span>
    - <span data-ttu-id="ff5be-633">Lägg till parametern ”-SkipResourceNameParameterization” till Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ff5be-633">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="ff5be-634">Lägg till parametern ”-SkipAllParameterization” till Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ff5be-634">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="ff5be-635">Lägg till parametern ”-Resource” till Export-AzResourceGroup för exporterad resursfiltrering</span><span class="sxs-lookup"><span data-stu-id="ff5be-635">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="ff5be-636">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ff5be-636">Az.ServiceFabric</span></span>
* <span data-ttu-id="ff5be-637">Åtgärda att fel tumavtryck används vid tilläggning av certifikat i ByExistingKeyVault i vissa fall</span><span class="sxs-lookup"><span data-stu-id="ff5be-637">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="ff5be-638">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ff5be-638">Az.Sql</span></span>
* <span data-ttu-id="ff5be-639">Åtgärda suffix för lagringsslutpunkt i Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="ff5be-639">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="ff5be-640">Åtgärda att aktivering av Advanced Data Security åsidosätter Advanced Threat Protection-princip</span><span class="sxs-lookup"><span data-stu-id="ff5be-640">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="ff5be-641">Nya cmdletar för Management.Sql som gör att kunderna kan lägga till nycklar för transparent datakryptering (TDE) och ange TDE-skydd för hanterade instanser</span><span class="sxs-lookup"><span data-stu-id="ff5be-641">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="ff5be-642">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ff5be-642">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="ff5be-643">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ff5be-643">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="ff5be-644">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ff5be-644">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="ff5be-645">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="ff5be-645">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="ff5be-646">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="ff5be-646">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ff5be-647">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ff5be-647">Az.Storage</span></span>
* <span data-ttu-id="ff5be-648">Stöd för typerna FileStorage och SkuName Premium_ZRS när lagringskonton skapas</span><span class="sxs-lookup"><span data-stu-id="ff5be-648">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="ff5be-649">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ff5be-649">New-AzStorageAccount</span></span>
* <span data-ttu-id="ff5be-650">Beskrivningen av cmdleten för bloboföränderlighet har förtydligats</span><span class="sxs-lookup"><span data-stu-id="ff5be-650">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="ff5be-651">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="ff5be-651">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ff5be-652">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ff5be-652">Az.Websites</span></span>
* <span data-ttu-id="ff5be-653">Optimerar Get-AzWebAppCertificate för att filtrera efter resursgrupp på servern i stället för klienten</span><span class="sxs-lookup"><span data-stu-id="ff5be-653">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="ff5be-654">Lägger till växlingsparametern -UseDisasterRecovery till Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="ff5be-654">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="ff5be-655">2.2.0 – juni 2019</span><span class="sxs-lookup"><span data-stu-id="ff5be-655">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="ff5be-656">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="ff5be-656">Az.Cdn</span></span>
* <span data-ttu-id="ff5be-657">Uppdaterade cmdletar för att ge stöd för rulesEngine-funktion baserat på API-version 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="ff5be-657">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ff5be-658">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ff5be-658">Az.Compute</span></span>
* <span data-ttu-id="ff5be-659">Lade till parameter `NoWait` som startar åtgärden och returnerar omedelbart, innan åtgärden har slutförts.</span><span class="sxs-lookup"><span data-stu-id="ff5be-659">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="ff5be-660">Uppdaterade cmdletar:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="ff5be-660">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="ff5be-661">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="ff5be-661">Az.EventHub</span></span>
* <span data-ttu-id="ff5be-662">Korrigering för #9231 – Get-AzEventHubNamespace returnerar inga taggar</span><span class="sxs-lookup"><span data-stu-id="ff5be-662">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="ff5be-663">Korrigering för #9230 – Get-AzEventHubNamespace returnerar ResourceGroup istället för ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff5be-663">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ff5be-664">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ff5be-664">Az.Network</span></span>
* <span data-ttu-id="ff5be-665">Uppdatera ResourceId och InputObject för NAT-gateway</span><span class="sxs-lookup"><span data-stu-id="ff5be-665">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="ff5be-666">Lägg till alias för ResourceId och InputObject</span><span class="sxs-lookup"><span data-stu-id="ff5be-666">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="ff5be-667">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="ff5be-667">Az.PolicyInsights</span></span>
* <span data-ttu-id="ff5be-668">Åtgärda Null-referensproblem i Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="ff5be-668">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ff5be-669">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ff5be-669">Az.RecoveryServices</span></span>
* <span data-ttu-id="ff5be-670">Minsta kvarhållning för IaaSVM-policy i dagar ändrat till 7 från 1</span><span class="sxs-lookup"><span data-stu-id="ff5be-670">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="ff5be-671">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ff5be-671">Az.ServiceBus</span></span>
* <span data-ttu-id="ff5be-672">Korrigering för ärende #9182 – Get-AzServiceBusNamespace returnerar ResourceGroup istället för ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff5be-672">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="ff5be-673">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ff5be-673">Az.ServiceFabric</span></span>
* <span data-ttu-id="ff5be-674">Åtgärda stavfel i felmeddelandet för Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="ff5be-674">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="ff5be-675">Åtgärda saknat tecken i Service Fabric-kommandorader</span><span class="sxs-lookup"><span data-stu-id="ff5be-675">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="ff5be-676">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ff5be-676">Az.Sql</span></span>
* <span data-ttu-id="ff5be-677">Lägg till parametern DnsZonePartner för New-AzureSqlInstance-cmdlet för att ge stöd för AutoDr för hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="ff5be-677">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="ff5be-678">Avvecklar cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="ff5be-678">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="ff5be-679">Döp om cmdletar för hotidentifiering till Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="ff5be-679">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="ff5be-680">Parametrarna New-AzSqlInstance -StorageSizeInGB och -LicenseType är nu valfria.</span><span class="sxs-lookup"><span data-stu-id="ff5be-680">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ff5be-681">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ff5be-681">Az.Websites</span></span>
* <span data-ttu-id="ff5be-682">åtgärdar problemet där användningen av Set-AzWebApp och Set-AzWebAppSlot med -WebApp-egenskap tog bort taggarna</span><span class="sxs-lookup"><span data-stu-id="ff5be-682">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="ff5be-683">2.1.0 – maj 2019</span><span class="sxs-lookup"><span data-stu-id="ff5be-683">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="ff5be-684">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ff5be-684">Az.ApiManagement</span></span>
* <span data-ttu-id="ff5be-685">Skapade nya cmdletar för att hantera diagnostik för global- och API-omfång</span><span class="sxs-lookup"><span data-stu-id="ff5be-685">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="ff5be-686">**Get-AzApiManagementDiagnostic** – Skaffa diagnostik konfigurerad för global- eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="ff5be-686">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="ff5be-687">**New-AzApiManagementDiagnostic** – Skapa ny diagnostik för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="ff5be-687">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="ff5be-688">**New-AzApiManagementHttpMessageDiagnostic** – Skapa diagnostikinställning om vilka rubriker som ska loggas och storleken på brödtextbyte</span><span class="sxs-lookup"><span data-stu-id="ff5be-688">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="ff5be-689">**New-AzApiManagementPipelineDiagnosticSetting** – Skapa diagnostikinställningar för inkommande/utgående HTTP-meddelanden till gatewayen.</span><span class="sxs-lookup"><span data-stu-id="ff5be-689">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="ff5be-690">**New-AzApiManagementSamplingSetting** – Skapa samplinginställningar för begäranden/svar för en diagnostik</span><span class="sxs-lookup"><span data-stu-id="ff5be-690">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="ff5be-691">**Remove-AzApiManagementDiagnostic** – Ta bort en diagnostikenhet för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="ff5be-691">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="ff5be-692">**Set-AzApiManagementDiagnostic** – Uppdatera en diagnostikenhet för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="ff5be-692">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="ff5be-693">Skapade nya cmdletar för hantering av cacheminne i ApiManagement-tjänsten</span><span class="sxs-lookup"><span data-stu-id="ff5be-693">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="ff5be-694">**Get-AzApiManagementCache** – Hämta information om cacheminnet som anges av identifierare eller alla cacheminnen</span><span class="sxs-lookup"><span data-stu-id="ff5be-694">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="ff5be-695">**New-AzApiManagementCache** – Skapa ett nytt default-cacheminne eller cacheminne i en viss Azure-region</span><span class="sxs-lookup"><span data-stu-id="ff5be-695">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="ff5be-696">**Remove-AzApiManagementCache** – Ta bort ett cacheminne</span><span class="sxs-lookup"><span data-stu-id="ff5be-696">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="ff5be-697">**Remove-AzApiManagementCache** – Ta bort ett cacheminne</span><span class="sxs-lookup"><span data-stu-id="ff5be-697">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="ff5be-698">Skapade nya cmdletar för hantering av API-schema</span><span class="sxs-lookup"><span data-stu-id="ff5be-698">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="ff5be-699">**New-AzApiManagementSchema** – Skapa ett nytt schema för ett API</span><span class="sxs-lookup"><span data-stu-id="ff5be-699">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="ff5be-700">**Get-AzApiManagementSchema** – Hämta de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="ff5be-700">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="ff5be-701">**Remove-AzApiManagementSchema** – Ta bort de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="ff5be-701">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="ff5be-702">**Set-AzApiManagementSchema** – Uppdatera de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="ff5be-702">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="ff5be-703">Skapa ny cmdlet för att generera en användartoken.</span><span class="sxs-lookup"><span data-stu-id="ff5be-703">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="ff5be-704">**New-AzApiManagementUserToken** – Skapa en ny användartoken som enligt standardinställning är giltig i 8 timmar. Token för GIT-användaren kan skapas med den här cmdleten./</span><span class="sxs-lookup"><span data-stu-id="ff5be-704">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="ff5be-705">Skapade en ny cmdlet för att hämta nätverksstatus</span><span class="sxs-lookup"><span data-stu-id="ff5be-705">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="ff5be-706">**Get-AzApiManagementNetworkStatus** – Hämta nätverksstatusanslutningen för resurserna som API Management-tjänsten är beroende av.</span><span class="sxs-lookup"><span data-stu-id="ff5be-706">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="ff5be-707">Det här är användbart när du distribuerar ApiManagement-tjänsten i ett virtuellt nätverk och validerar om något beroende är brutet.</span><span class="sxs-lookup"><span data-stu-id="ff5be-707">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="ff5be-708">Uppdaterade cmdlet **New-AzApiManagement** för att hantera ApiManagement-tjänsten</span><span class="sxs-lookup"><span data-stu-id="ff5be-708">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="ff5be-709">Lade till stöd för den nya SKU:n Consumption</span><span class="sxs-lookup"><span data-stu-id="ff5be-709">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="ff5be-710">Aktiverade stöd för att slå på flaggan EnableClientCertificate för SKU:n Consumption</span><span class="sxs-lookup"><span data-stu-id="ff5be-710">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="ff5be-711">Den nya cmdleten **New-AzApiManagementSslSetting** gör det möjligt att ställa in TLS/SSL-inställningen på ”Backend” och ”Frontend” (serverdel och klientdel).</span><span class="sxs-lookup"><span data-stu-id="ff5be-711">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="ff5be-712">Det här kan också användas till att konfigurera chiffer som 3DES och ServerProtocols som Http2 för Frontend för en ApiManagement-tjänst.</span><span class="sxs-lookup"><span data-stu-id="ff5be-712">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="ff5be-713">Stöd har lagts till för att konfigurera värdnamnet DeveloperPortal på ApiManagement-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="ff5be-713">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="ff5be-714">Uppdaterade cmdletar **Get-AzApiManagementSsoToken** för att ta PsApiManagement-objekt som indata</span><span class="sxs-lookup"><span data-stu-id="ff5be-714">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="ff5be-715">Uppdaterad cmdleten för att visa infogade felmeddelanden</span><span class="sxs-lookup"><span data-stu-id="ff5be-715">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="ff5be-716">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Felkod: Felmeddelande av typen ValidationError: Ett eller flera fält innehåller felaktiga värden: Felinformation:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="ff5be-716">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="ff5be-717">Uppdaterade cmdlet **Export-AzApiManagementApi** för att exportera API:er i OpenApi 3.0-format</span><span class="sxs-lookup"><span data-stu-id="ff5be-717">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="ff5be-718">Uppdaterade cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="ff5be-718">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="ff5be-719">Importera API från dokumentspecifikationen OpenApi 3.0</span><span class="sxs-lookup"><span data-stu-id="ff5be-719">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="ff5be-720">Om du vill åsidosätta egenskapen PsApiManagementSchema specificerad i ett dokument (Swagger, Wadl, Wsdl, OpenApi).</span><span class="sxs-lookup"><span data-stu-id="ff5be-720">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="ff5be-721">Åsidosätta egenskapen ServiceUrl som specificeras i ett dokument.</span><span class="sxs-lookup"><span data-stu-id="ff5be-721">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="ff5be-722">Uppdaterade cmdlet **Get-AzApiManagementPolicy** för att returnera policy i undantaget format av typen icke-XML med rawxml</span><span class="sxs-lookup"><span data-stu-id="ff5be-722">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="ff5be-723">Uppdaterade cmdlet **Set-AzApiManagementPolicy** för att godkänna policy i undantaget format av typen icke-XML med rawxml och XML undantaget med xml</span><span class="sxs-lookup"><span data-stu-id="ff5be-723">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="ff5be-724">Uppdaterad cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="ff5be-724">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="ff5be-725">Konfigurera API med OpenId auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="ff5be-725">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="ff5be-726">Skapa ett API i ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="ff5be-726">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="ff5be-727">Klona ett API med SourceApiId och SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="ff5be-727">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="ff5be-728">Möjlighet att konfigurera SubscriptionRequired i API-omfattningen.</span><span class="sxs-lookup"><span data-stu-id="ff5be-728">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="ff5be-729">Uppdaterad cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="ff5be-729">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="ff5be-730">Konfigurera API med OpenId auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="ff5be-730">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="ff5be-731">Uppdatera ett API till ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="ff5be-731">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="ff5be-732">Möjlighet att konfigurera SubscriptionRequired i API-omfattningen.</span><span class="sxs-lookup"><span data-stu-id="ff5be-732">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="ff5be-733">Uppdaterad cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="ff5be-733">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="ff5be-734">Klona en befintlig version med hjälp av SourceApiRevision (kopiera taggar, produkter, åtgärder och principer).</span><span class="sxs-lookup"><span data-stu-id="ff5be-734">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="ff5be-735">Den nya revisionen antar ApiId från den överordnade instansen.</span><span class="sxs-lookup"><span data-stu-id="ff5be-735">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="ff5be-736">Tillhandahålla ApiRevisionDescription</span><span class="sxs-lookup"><span data-stu-id="ff5be-736">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="ff5be-737">Åsidosätta ServiceUrl vid kloning av ett API.</span><span class="sxs-lookup"><span data-stu-id="ff5be-737">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="ff5be-738">Uppdaterad cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="ff5be-738">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="ff5be-739">Konfigurera AAD eller AADB2C med en Authority</span><span class="sxs-lookup"><span data-stu-id="ff5be-739">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="ff5be-740">Konfigurera SignupPolicy, SigninPolicy, ProfileEditingPolicy och PasswordResetPolicy</span><span class="sxs-lookup"><span data-stu-id="ff5be-740">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="ff5be-741">Uppdaterad cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="ff5be-741">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="ff5be-742">Kompensera för ny SubscriptonModel med Scope och UserId</span><span class="sxs-lookup"><span data-stu-id="ff5be-742">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="ff5be-743">Kompensera för gammal prenumerationsmodell med ProductId och UserId</span><span class="sxs-lookup"><span data-stu-id="ff5be-743">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="ff5be-744">Lägg till funktion för att aktivera AllowTracing på prenumerationsnivå.</span><span class="sxs-lookup"><span data-stu-id="ff5be-744">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="ff5be-745">Uppdaterad cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="ff5be-745">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="ff5be-746">Kompensera för ny SubscriptonModel med Scope och UserId</span><span class="sxs-lookup"><span data-stu-id="ff5be-746">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="ff5be-747">Kompensera för gammal prenumerationsmodell med ProductId och UserId</span><span class="sxs-lookup"><span data-stu-id="ff5be-747">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="ff5be-748">Lägg till funktion för att aktivera AllowTracing på prenumerationsnivå.</span><span class="sxs-lookup"><span data-stu-id="ff5be-748">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="ff5be-749">Uppdaterade följande cmdletar för att acceptera ResourceId som indata</span><span class="sxs-lookup"><span data-stu-id="ff5be-749">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="ff5be-750">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ff5be-750">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="ff5be-751">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="ff5be-751">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="ff5be-752">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="ff5be-752">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="ff5be-753">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="ff5be-753">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="ff5be-754">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="ff5be-754">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="ff5be-755">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="ff5be-755">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="ff5be-756">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="ff5be-756">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="ff5be-757">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="ff5be-757">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="ff5be-758">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="ff5be-758">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="ff5be-759">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="ff5be-759">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="ff5be-760">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="ff5be-760">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="ff5be-761">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="ff5be-761">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ff5be-762">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ff5be-762">Az.Automation</span></span>
* <span data-ttu-id="ff5be-763">Uppdaterade Get-AzAutomationJobOutputRecord för att hantera postvärden av typen JSON och Text.</span><span class="sxs-lookup"><span data-stu-id="ff5be-763">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="ff5be-764">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="ff5be-764">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="ff5be-765">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="ff5be-765">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="ff5be-766">Ändrade beteende för Start-AzAutomationDscCompilationJob till att bara starta jobbet istället för att vänta på slutförandet.</span><span class="sxs-lookup"><span data-stu-id="ff5be-766">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="ff5be-767">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="ff5be-767">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="ff5be-768">Korrigering för Get-AzAutomationDscNode när using -Name returnerar alla noder.</span><span class="sxs-lookup"><span data-stu-id="ff5be-768">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="ff5be-769">Nu returnerar den endast den matchande noden.</span><span class="sxs-lookup"><span data-stu-id="ff5be-769">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ff5be-770">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ff5be-770">Az.Compute</span></span>
* <span data-ttu-id="ff5be-771">Lägg till parametrarna ProtectFromScaleIn och ProtectFromScaleSetAction i cmdleten Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="ff5be-771">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="ff5be-772">Nu är standardinställningen att vimpelparametern New-AzVM använder en tillgänglig plats om USA, östra inte stöds</span><span class="sxs-lookup"><span data-stu-id="ff5be-772">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ff5be-773">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ff5be-773">Az.DataLakeStore</span></span>
* <span data-ttu-id="ff5be-774">Uppdatera ADLS-sdk för att använda httpclient, integrera dataplanstestning med Azure-ramverk</span><span class="sxs-lookup"><span data-stu-id="ff5be-774">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ff5be-775">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ff5be-775">Az.Monitor</span></span>
* <span data-ttu-id="ff5be-776">Korrigera felaktiga parameternamn i hjälpexempel</span><span class="sxs-lookup"><span data-stu-id="ff5be-776">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ff5be-777">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ff5be-777">Az.Network</span></span>
* <span data-ttu-id="ff5be-778">Lägg till flaggan DisableBgpRoutePropagation i utdata för effektiv routningstabell</span><span class="sxs-lookup"><span data-stu-id="ff5be-778">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="ff5be-779">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="ff5be-779">Updated cmdlet:</span></span>
        - <span data-ttu-id="ff5be-780">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="ff5be-780">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="ff5be-781">Åtgärda dubbelstreck i dokumentationen New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="ff5be-781">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="ff5be-782">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ff5be-782">Az.Resources</span></span>
* <span data-ttu-id="ff5be-783">Lägg till ny cmdlet Get-AzureRmDenyAssignment för att hämta tilldelningsnekanden</span><span class="sxs-lookup"><span data-stu-id="ff5be-783">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="ff5be-784">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ff5be-784">Az.Sql</span></span>
* <span data-ttu-id="ff5be-785">Döp om Advanced Threat Protection-cmdletar för Advanced Data Security och aktivera Vulnerability Assessment som standard</span><span class="sxs-lookup"><span data-stu-id="ff5be-785">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="ff5be-786">2.0.0 – maj 2019</span><span class="sxs-lookup"><span data-stu-id="ff5be-786">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ff5be-787">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ff5be-787">Az.Accounts</span></span>
* <span data-ttu-id="ff5be-788">Uppdatera autentiseringsbiblioteket för att åtgärda ADFS-problem med autentisering av användarnamn/lösenord</span><span class="sxs-lookup"><span data-stu-id="ff5be-788">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="ff5be-789">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ff5be-789">Az.CognitiveServices</span></span>
* <span data-ttu-id="ff5be-790">Visa endast Bing-ansvarsfriskrivning för Bing-sökningstjänster.</span><span class="sxs-lookup"><span data-stu-id="ff5be-790">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="ff5be-791">Förbättra felmeddelande när det inte går att skapa konton.</span><span class="sxs-lookup"><span data-stu-id="ff5be-791">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ff5be-792">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ff5be-792">Az.Compute</span></span>
* <span data-ttu-id="ff5be-793">Funktion för närhetsplaceringsgrupper.</span><span class="sxs-lookup"><span data-stu-id="ff5be-793">Proximity placement group feature.</span></span>
    - <span data-ttu-id="ff5be-794">Följande nya cmdletar har lagts till:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="ff5be-794">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="ff5be-795">Den nya parametern ProximityPlacementGroupId har lagts till i följande cmdletar:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="ff5be-795">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="ff5be-796">Parametern StorageAccountType har lagts till i New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="ff5be-796">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="ff5be-797">TargetRegion för New-AzGalleryImageVersion kan innehålla StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="ff5be-797">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="ff5be-798">Växlingsparametern SkipShutdown har lagts till i Stop-AzVM och Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ff5be-798">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="ff5be-799">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="ff5be-799">Breaking changes</span></span>
    - <span data-ttu-id="ff5be-800">Set-AzVMBootDiagnostics har ändrats till Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="ff5be-800">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="ff5be-801">Export-AzLogAnalyticThrottledRequests har ändrats till Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="ff5be-801">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="ff5be-802">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="ff5be-802">Az.DeploymentManager</span></span>
* <span data-ttu-id="ff5be-803">De första allmänt tillgängliga versionerna av cmdletar för Distributionshanteraren i Azure</span><span class="sxs-lookup"><span data-stu-id="ff5be-803">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="ff5be-804">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="ff5be-804">Az.Dns</span></span>
* <span data-ttu-id="ff5be-805">Automatisk delegering av DNS för NameServer</span><span class="sxs-lookup"><span data-stu-id="ff5be-805">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="ff5be-806">Det överordnade zonnamnet kan användas som ytterligare valfri parameter i cmdleten för att skapa DNS-zoner.</span><span class="sxs-lookup"><span data-stu-id="ff5be-806">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="ff5be-807">Lägger till NS-poster för en nyligen skapad underordnad zon i den överordnade zonen.</span><span class="sxs-lookup"><span data-stu-id="ff5be-807">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="ff5be-808">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="ff5be-808">Az.FrontDoor</span></span>
* <span data-ttu-id="ff5be-809">De första allmänt tillgängliga versionerna av cmdletar för Azure FrontDoor</span><span class="sxs-lookup"><span data-stu-id="ff5be-809">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="ff5be-810">Byt namn på WAF-cmdletar så att de omfattar ”Waf”</span><span class="sxs-lookup"><span data-stu-id="ff5be-810">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="ff5be-811">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="ff5be-811">Az.HDInsight</span></span>
* <span data-ttu-id="ff5be-812">Två cmdletar har tagits bort:</span><span class="sxs-lookup"><span data-stu-id="ff5be-812">Removed two cmdlets:</span></span>
    - <span data-ttu-id="ff5be-813">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="ff5be-813">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="ff5be-814">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="ff5be-814">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="ff5be-815">En ny cmdlet har lagts till, Set-AzHDInsightGatewayCredential, som ersätter Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="ff5be-815">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="ff5be-816">Uppdatera cmdleten Get-AzHDInsightJobOutput för att skilja mellan läsarrollen och HDInsight-operatörsrollen:</span><span class="sxs-lookup"><span data-stu-id="ff5be-816">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="ff5be-817">Användare med läsarrollen måste uttryckligen ange parametern ”DefaultStorageAccountKey”, annars uppstår fel.</span><span class="sxs-lookup"><span data-stu-id="ff5be-817">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="ff5be-818">Användare med HDInsight-operatörsrollen påverkas inte.</span><span class="sxs-lookup"><span data-stu-id="ff5be-818">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ff5be-819">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ff5be-819">Az.Monitor</span></span>
* <span data-ttu-id="ff5be-820">Nya cmdletar för SQR API (schemalagd frågeregel)</span><span class="sxs-lookup"><span data-stu-id="ff5be-820">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="ff5be-821">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="ff5be-821">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="ff5be-822">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="ff5be-822">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="ff5be-823">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="ff5be-823">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="ff5be-824">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="ff5be-824">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="ff5be-825">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="ff5be-825">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="ff5be-826">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="ff5be-826">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="ff5be-827">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="ff5be-827">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="ff5be-828">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="ff5be-828">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="ff5be-829">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="ff5be-829">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="ff5be-830">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="ff5be-830">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="ff5be-831">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="ff5be-831">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="ff5be-832">[Mer](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information om SQR API</span><span class="sxs-lookup"><span data-stu-id="ff5be-832">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="ff5be-833">Az.Monitor.md har uppdaterats för att omfatta cmdletar för måttbaserade aviseringsregler i GenV2 (inte klassiska)</span><span class="sxs-lookup"><span data-stu-id="ff5be-833">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ff5be-834">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ff5be-834">Az.Network</span></span>
* <span data-ttu-id="ff5be-835">Lägg till stöd för NAT Gateway-resurs</span><span class="sxs-lookup"><span data-stu-id="ff5be-835">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="ff5be-836">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="ff5be-836">New cmdlets</span></span>
        - <span data-ttu-id="ff5be-837">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="ff5be-837">New-AzNatGateway</span></span>
        - <span data-ttu-id="ff5be-838">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="ff5be-838">Get-AzNatGateway</span></span>
        - <span data-ttu-id="ff5be-839">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="ff5be-839">Set-AzNatGateway</span></span>
        - <span data-ttu-id="ff5be-840">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="ff5be-840">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="ff5be-841">Uppdaterade cmdletar</span><span class="sxs-lookup"><span data-stu-id="ff5be-841">Updated cmdlets</span></span>
        - <span data-ttu-id="ff5be-842">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="ff5be-842">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="ff5be-843">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="ff5be-843">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="ff5be-844">Nedanstående kommandon för funktionen har uppdaterats: Ange/ta bort anpassade vägar på Brooklyn Gateway.</span><span class="sxs-lookup"><span data-stu-id="ff5be-844">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="ff5be-845">New-AzVirtualNetworkGateway har uppdaterats: Den valfria parametern -CustomRoute har lagts till för att ställa in adressprefix som anpassade vägar för att ange gateway.</span><span class="sxs-lookup"><span data-stu-id="ff5be-845">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="ff5be-846">Set-AzVirtualNetworkGateway har uppdaterats: Den valfria parametern -CustomRoute har lagts till för att ange adressprefix som anpassade vägar för att ange gateway.</span><span class="sxs-lookup"><span data-stu-id="ff5be-846">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="ff5be-847">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="ff5be-847">Az.PolicyInsights</span></span>
* <span data-ttu-id="ff5be-848">Stöd för att fråga efter information om principutvärdering.</span><span class="sxs-lookup"><span data-stu-id="ff5be-848">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="ff5be-849">Lägg till parametern ”-Expand” för Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="ff5be-849">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="ff5be-850">Stöd för -Expand PolicyEvaluationDetails.</span><span class="sxs-lookup"><span data-stu-id="ff5be-850">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ff5be-851">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ff5be-851">Az.RecoveryServices</span></span>
* <span data-ttu-id="ff5be-852">Stöd för att dela prenumeration mellan Azure och Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="ff5be-852">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="ff5be-853">Markering av kommande icke-bakåtkompatibla ändringar för Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="ff5be-853">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="ff5be-854">Korrigering för återställningsplan och åtgärdsplan i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="ff5be-854">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="ff5be-855">Korrigering för mappning av uppdateringsnätverk i Azure Site Recovery för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="ff5be-855">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="ff5be-856">Korrigering för instruktioner för uppdateringsskydd i Azure Site Recovery för Azure till Azure för hanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="ff5be-856">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="ff5be-857">Andra mindre korrigeringar.</span><span class="sxs-lookup"><span data-stu-id="ff5be-857">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="ff5be-858">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="ff5be-858">Az.Relay</span></span>
* <span data-ttu-id="ff5be-859">Korrigera stavfel i kundriktade meddelanden</span><span class="sxs-lookup"><span data-stu-id="ff5be-859">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="ff5be-860">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ff5be-860">Az.ServiceBus</span></span>
* <span data-ttu-id="ff5be-861">Nya cmdletar har lagts till för NetworkRuleSet för namnområden</span><span class="sxs-lookup"><span data-stu-id="ff5be-861">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ff5be-862">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ff5be-862">Az.Storage</span></span>
* <span data-ttu-id="ff5be-863">Uppgradera till lagringsklientbiblioteket 10.0.1 (namnområdet för alla objekt från detta SDK ändras från ”Microsoft.WindowsAzure.Storage. *till ”Microsoft.Azure.Storage.* ”)</span><span class="sxs-lookup"><span data-stu-id="ff5be-863">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="ff5be-864">Uppgradera till Microsoft.Azure.Management.Storage 11.0.0 för att stödja den nya API-versionen 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="ff5be-864">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="ff5be-865">Standardlagringskontot i Skapa lagringskonto ändras från ”Storage” till ”StorageV2”</span><span class="sxs-lookup"><span data-stu-id="ff5be-865">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="ff5be-866">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ff5be-866">New-AzStorageAccount</span></span>
* <span data-ttu-id="ff5be-867">Ändra lagringskontots cmdlet-utdata Sku.Name för att passa med indata-SkuName genom att lägga till ”-”. Till exempel ändras ”StandardLRS” till ”Standard_LRS”</span><span class="sxs-lookup"><span data-stu-id="ff5be-867">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="ff5be-868">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ff5be-868">New-AzStorageAccount</span></span>
    - <span data-ttu-id="ff5be-869">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ff5be-869">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="ff5be-870">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ff5be-870">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ff5be-871">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ff5be-871">Az.Websites</span></span>
* <span data-ttu-id="ff5be-872">Egenskapen ”typ” konfigureras nu för PSSite-objekt som returneras av Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ff5be-872">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="ff5be-873">Get-AzWebApp\*Metrics och Get-AzAppServicePlanMetrics markeras som inaktuella</span><span class="sxs-lookup"><span data-stu-id="ff5be-873">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="ff5be-874">1.8.0 – april 2019</span><span class="sxs-lookup"><span data-stu-id="ff5be-874">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="ff5be-875">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="ff5be-875">Highlights since the last major release</span></span>
* <span data-ttu-id="ff5be-876">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="ff5be-876">General availability of `Az` module</span></span>
* <span data-ttu-id="ff5be-877">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="ff5be-877">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="ff5be-878">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="ff5be-878">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="ff5be-879">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="ff5be-879">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="ff5be-880">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="ff5be-880">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="ff5be-881">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="ff5be-881">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="ff5be-882">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="ff5be-882">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="ff5be-883">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ff5be-883">Az.Accounts</span></span>
* <span data-ttu-id="ff5be-884">Uppdatera Uninstall-AzureRm för att ta bort moduler i Mac på ett korrekt sätt</span><span class="sxs-lookup"><span data-stu-id="ff5be-884">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="ff5be-885">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="ff5be-885">Az.Batch</span></span>
* <span data-ttu-id="ff5be-886">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="ff5be-886">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="ff5be-887">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="ff5be-887">Az.Cdn</span></span>
* <span data-ttu-id="ff5be-888">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="ff5be-888">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="ff5be-889">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ff5be-889">Az.CognitiveServices</span></span>
* <span data-ttu-id="ff5be-890">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="ff5be-890">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ff5be-891">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ff5be-891">Az.Compute</span></span>
* <span data-ttu-id="ff5be-892">Åtgärda problem med AEM-installationen om resurs-ID:n för diskar innehåller resourcegroups i gemener i resurs-ID:n</span><span class="sxs-lookup"><span data-stu-id="ff5be-892">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="ff5be-893">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="ff5be-893">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="ff5be-894">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="ff5be-894">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ff5be-895">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ff5be-895">Az.DataFactory</span></span>
* <span data-ttu-id="ff5be-896">Lägg till SsisProperties om NodeCount inte är null för hanterad integreringskörning.</span><span class="sxs-lookup"><span data-stu-id="ff5be-896">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ff5be-897">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ff5be-897">Az.DataLakeStore</span></span>
* <span data-ttu-id="ff5be-898">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="ff5be-898">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="ff5be-899">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="ff5be-899">Az.EventGrid</span></span>
* <span data-ttu-id="ff5be-900">Hjälptexten för slutpunkten har uppdaterats för att visa att resurser ska skapas innan cmdletarna för att skapa/uppdatera händelseprenumerationer används.</span><span class="sxs-lookup"><span data-stu-id="ff5be-900">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="ff5be-901">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="ff5be-901">Az.EventHub</span></span>
* <span data-ttu-id="ff5be-902">Nya cmdletar har lagts till för NetworkRuleSet för namnområden</span><span class="sxs-lookup"><span data-stu-id="ff5be-902">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="ff5be-903">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="ff5be-903">Az.HDInsight</span></span>
* <span data-ttu-id="ff5be-904">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="ff5be-904">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ff5be-905">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ff5be-905">Az.IotHub</span></span>
* <span data-ttu-id="ff5be-906">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="ff5be-906">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="ff5be-907">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ff5be-907">Az.KeyVault</span></span>
* <span data-ttu-id="ff5be-908">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="ff5be-908">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="ff5be-909">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="ff5be-909">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="ff5be-910">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="ff5be-910">Az.MachineLearning</span></span>
* <span data-ttu-id="ff5be-911">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="ff5be-911">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="ff5be-912">Az.Media</span><span class="sxs-lookup"><span data-stu-id="ff5be-912">Az.Media</span></span>
* <span data-ttu-id="ff5be-913">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="ff5be-913">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ff5be-914">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ff5be-914">Az.Monitor</span></span>
  * <span data-ttu-id="ff5be-915">Nya cmdletar för måttbaserad aviseringsregel i GenV2 (inte klassisk)</span><span class="sxs-lookup"><span data-stu-id="ff5be-915">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="ff5be-916">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="ff5be-916">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="ff5be-917">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="ff5be-917">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="ff5be-918">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="ff5be-918">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="ff5be-919">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="ff5be-919">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="ff5be-920">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="ff5be-920">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="ff5be-921">Monitor SDK har uppdaterats till version 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="ff5be-921">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ff5be-922">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ff5be-922">Az.Network</span></span>
* <span data-ttu-id="ff5be-923">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="ff5be-923">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="ff5be-924">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="ff5be-924">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="ff5be-925">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="ff5be-925">Az.NotificationHubs</span></span>
* <span data-ttu-id="ff5be-926">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="ff5be-926">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="ff5be-927">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ff5be-927">Az.OperationalInsights</span></span>
* <span data-ttu-id="ff5be-928">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="ff5be-928">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="ff5be-929">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="ff5be-929">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="ff5be-930">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="ff5be-930">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ff5be-931">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ff5be-931">Az.RecoveryServices</span></span>
* <span data-ttu-id="ff5be-932">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="ff5be-932">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="ff5be-933">Tabellformatet för SQL i virtuella Azure-datorer har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="ff5be-933">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="ff5be-934">En alternativ metod för att hämta platser i AzureFileShare har lagts till</span><span class="sxs-lookup"><span data-stu-id="ff5be-934">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="ff5be-935">ScheduleRunDays i SchedulePolicy-objekt har uppdaterats enligt tidszon</span><span class="sxs-lookup"><span data-stu-id="ff5be-935">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="ff5be-936">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="ff5be-936">Az.RedisCache</span></span>
* <span data-ttu-id="ff5be-937">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="ff5be-937">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="ff5be-938">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ff5be-938">Az.Resources</span></span>
* <span data-ttu-id="ff5be-939">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="ff5be-939">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="ff5be-940">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ff5be-940">Az.Sql</span></span>
* <span data-ttu-id="ff5be-941">Ersätt Monitor SDK-beroende med vanlig kod</span><span class="sxs-lookup"><span data-stu-id="ff5be-941">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="ff5be-942">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="ff5be-942">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="ff5be-943">Förbättrad process för klassificering av flera kolumner.</span><span class="sxs-lookup"><span data-stu-id="ff5be-943">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="ff5be-944">Inkludera SKU-egenskaper (SKU-namn, serie, kapacitet) i svaret från Get-AzSqlServerServiceObjective och formatera som tabell som standard.</span><span class="sxs-lookup"><span data-stu-id="ff5be-944">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="ff5be-945">Möjlighet att använda Get-AzSqlServerServiceObjective efter plats utan att behöva en redan befintlig server i regionen.</span><span class="sxs-lookup"><span data-stu-id="ff5be-945">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="ff5be-946">Stöd för tidszonsparametern när hanterade instanser skapas.</span><span class="sxs-lookup"><span data-stu-id="ff5be-946">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="ff5be-947">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="ff5be-947">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ff5be-948">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ff5be-948">Az.Websites</span></span>
* <span data-ttu-id="ff5be-949">åtgärdar Set-AzWebApp och Set-AzWebAppSlot så att de inte tar bort taggar vid körning</span><span class="sxs-lookup"><span data-stu-id="ff5be-949">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="ff5be-950">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="ff5be-950">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="ff5be-951">SDK för WebSites har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="ff5be-951">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="ff5be-952">Egenskapen AdminSiteName har tagits bort från PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="ff5be-952">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="ff5be-953">1.7.0 – april 2019</span><span class="sxs-lookup"><span data-stu-id="ff5be-953">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="ff5be-954">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="ff5be-954">Highlights since the last major release</span></span>
* <span data-ttu-id="ff5be-955">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="ff5be-955">General availability of `Az` module</span></span>
* <span data-ttu-id="ff5be-956">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="ff5be-956">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="ff5be-957">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="ff5be-957">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="ff5be-958">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="ff5be-958">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="ff5be-959">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="ff5be-959">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="ff5be-960">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="ff5be-960">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="ff5be-961">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="ff5be-961">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="ff5be-962">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ff5be-962">Az.Accounts</span></span>
* <span data-ttu-id="ff5be-963">Add-AzEnvironment och Set-AzEnvironment har uppdaterats för att godkänna parametern AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="ff5be-963">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="ff5be-964">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ff5be-964">Az.AnalysisServices</span></span>
* <span data-ttu-id="ff5be-965">ServiceClient används i cmdletar för dataplan och den ursprungliga autentiseringslogiken har tagits bort</span><span class="sxs-lookup"><span data-stu-id="ff5be-965">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="ff5be-966">Add-AzureASAccount används för omslutning av Connect-AzAccount för att undvika en icke-bakåtkompatibel ändring</span><span class="sxs-lookup"><span data-stu-id="ff5be-966">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ff5be-967">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ff5be-967">Az.Automation</span></span>
* <span data-ttu-id="ff5be-968">Buggen för cmdleten New-AzAutomationSoftwareUpdateConfiguration för inkluderingar har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="ff5be-968">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="ff5be-969">Nu bör parametern IncludedKbNumber och IncludedPackageNameMask fungera.</span><span class="sxs-lookup"><span data-stu-id="ff5be-969">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="ff5be-970">Felkorrigering för dynamiska grupper i uppdateringshanteringen för azure automation</span><span class="sxs-lookup"><span data-stu-id="ff5be-970">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ff5be-971">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ff5be-971">Az.Compute</span></span>
* <span data-ttu-id="ff5be-972">Lägg till parametern HyperVGeneration i New-AzDiskConfig och New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="ff5be-972">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="ff5be-973">Tillåt att virtuella datorer skapas med galleribilder från andra klientorganisationer.</span><span class="sxs-lookup"><span data-stu-id="ff5be-973">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="ff5be-974">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="ff5be-974">Az.ContainerInstance</span></span>
* <span data-ttu-id="ff5be-975">Ett problem har åtgärdats i parametern -Command för New-AzContainerGroup som lade till ett avslutande tomt argument</span><span class="sxs-lookup"><span data-stu-id="ff5be-975">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ff5be-976">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ff5be-976">Az.DataFactory</span></span>
* <span data-ttu-id="ff5be-977">ADF .Net SDK-versionen har uppdaterats till 3.0.2</span><span class="sxs-lookup"><span data-stu-id="ff5be-977">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="ff5be-978">Cmdleten Set-AzDataFactoryV2 har uppdaterats med extra parametrar för inställningar som rör RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="ff5be-978">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="ff5be-979">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ff5be-979">Az.Resources</span></span>
* <span data-ttu-id="ff5be-980">Förbättra hanteringen av providrar för Get-AzResource när parametrarna -ResourceId eller -ResourceGroupName, -Name och -ResourceType tillhandahålls</span><span class="sxs-lookup"><span data-stu-id="ff5be-980">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="ff5be-981">Förbättra felhanteringen för ”Test-AzDeployment” och ”Test-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="ff5be-981">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="ff5be-982">Hantera fel utanför distributionsvalideringen och ta med dem i kommandoutdata istället</span><span class="sxs-lookup"><span data-stu-id="ff5be-982">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="ff5be-983">Mer information här: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="ff5be-983">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="ff5be-984">Lägg till växlingsparametern -IgnoreDynamicParameters till en uppsättning av cmdletar för distribution för att hoppa över fråga i skript och jobbscenarier</span><span class="sxs-lookup"><span data-stu-id="ff5be-984">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="ff5be-985">Mer information här: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="ff5be-985">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="ff5be-986">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ff5be-986">Az.Sql</span></span>
* <span data-ttu-id="ff5be-987">Stöd för dataklassificering av databaser.</span><span class="sxs-lookup"><span data-stu-id="ff5be-987">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ff5be-988">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ff5be-988">Az.Storage</span></span>
* <span data-ttu-id="ff5be-989">Rapportera detaljfel när lagringskontext skapas med parametern -UseConnectedAccount, men utan inloggning på Azure-kontot</span><span class="sxs-lookup"><span data-stu-id="ff5be-989">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="ff5be-990">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="ff5be-990">New-AzStorageContext</span></span>
* <span data-ttu-id="ff5be-991">Stöd för att hantera Blob Service-egenskaper för ett angivet lagringskonto med API:et för hanteringsplan</span><span class="sxs-lookup"><span data-stu-id="ff5be-991">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="ff5be-992">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="ff5be-992">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="ff5be-993">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="ff5be-993">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="ff5be-994">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="ff5be-994">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="ff5be-995">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="ff5be-995">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="ff5be-996">Stöd för -AsJob-cmdletar för att ladda upp och ladda ned blobar och filer</span><span class="sxs-lookup"><span data-stu-id="ff5be-996">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="ff5be-997">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="ff5be-997">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="ff5be-998">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="ff5be-998">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="ff5be-999">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="ff5be-999">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="ff5be-1000">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="ff5be-1000">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="ff5be-1001">1.6.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="ff5be-1001">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="ff5be-1002">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="ff5be-1002">Highlights since the last major release</span></span>
* <span data-ttu-id="ff5be-1003">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="ff5be-1003">General availability of `Az` module</span></span>
* <span data-ttu-id="ff5be-1004">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="ff5be-1004">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="ff5be-1005">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="ff5be-1005">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="ff5be-1006">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="ff5be-1006">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="ff5be-1007">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="ff5be-1007">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="ff5be-1008">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="ff5be-1008">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="ff5be-1009">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="ff5be-1009">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ff5be-1010">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ff5be-1010">Az.Automation</span></span>
* <span data-ttu-id="ff5be-1011">Azure Automation – ändring av uppdateringshantering för stöd för de nya funktionerna:</span><span class="sxs-lookup"><span data-stu-id="ff5be-1011">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="ff5be-1012">Dynamisk gruppering</span><span class="sxs-lookup"><span data-stu-id="ff5be-1012">Dynamic grouping</span></span>
    * <span data-ttu-id="ff5be-1013">För-/efterskrift</span><span class="sxs-lookup"><span data-stu-id="ff5be-1013">Pre-Post script</span></span>
    * <span data-ttu-id="ff5be-1014">Inställning för omstart</span><span class="sxs-lookup"><span data-stu-id="ff5be-1014">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ff5be-1015">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ff5be-1015">Az.Compute</span></span>
* <span data-ttu-id="ff5be-1016">Åtgärda problem med sökvägsmatchning i Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="ff5be-1016">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="ff5be-1017">Uppdatera Compute-klientbibliotek till 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="ff5be-1017">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="ff5be-1018">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ff5be-1018">Az.KeyVault</span></span>
* <span data-ttu-id="ff5be-1019">Stöd för jokertecken för KeyVault-cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="ff5be-1019">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ff5be-1020">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ff5be-1020">Az.Network</span></span>
* <span data-ttu-id="ff5be-1021">Lägg till stöd för Threat Intelligence för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="ff5be-1021">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="ff5be-1022">Lägg till resurs för brandväggsprincip på översta nivå och anpassade regler för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="ff5be-1022">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ff5be-1023">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ff5be-1023">Az.RecoveryServices</span></span>
* <span data-ttu-id="ff5be-1024">SnapshotRetentionInDays har lagts till i Azure-principen för virtuella datorer för stöd av Instant RP</span><span class="sxs-lookup"><span data-stu-id="ff5be-1024">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="ff5be-1025">Pipe-stöd för avregistrering av container har lagts till</span><span class="sxs-lookup"><span data-stu-id="ff5be-1025">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="ff5be-1026">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ff5be-1026">Az.Resources</span></span>
* <span data-ttu-id="ff5be-1027">Uppdatera stöd för jokertecken för Get-AzResource och Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ff5be-1027">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="ff5be-1028">Uppdatera autentiseringsuppgifter som används vid allmänna anrop till ARM</span><span class="sxs-lookup"><span data-stu-id="ff5be-1028">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="ff5be-1029">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ff5be-1029">Az.Sql</span></span>
* <span data-ttu-id="ff5be-1030">Cmdlet-parametern (ExcludeDetectionType) för Hotidentifiering ändrades från DetectionType till sträng[] för att framtidssäkra den när nya DetectionTypes läggs till, och även för att stödja automatisk ifyllning.</span><span class="sxs-lookup"><span data-stu-id="ff5be-1030">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ff5be-1031">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ff5be-1031">Az.Storage</span></span>
* <span data-ttu-id="ff5be-1032">Stöd för att hämta/ange/ta bort hanteringsprincip på ett lagringskonto</span><span class="sxs-lookup"><span data-stu-id="ff5be-1032">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="ff5be-1033">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="ff5be-1033">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="ff5be-1034">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="ff5be-1034">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="ff5be-1035">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="ff5be-1035">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="ff5be-1036">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="ff5be-1036">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="ff5be-1037">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="ff5be-1037">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="ff5be-1038">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="ff5be-1038">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ff5be-1039">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ff5be-1039">Az.Websites</span></span>
* <span data-ttu-id="ff5be-1040">Åtgärda fel med ARM-mall som avbryter kloning av alla platser med 'New-AzWebApp -IncludeSourceWebAppSlots'</span><span class="sxs-lookup"><span data-stu-id="ff5be-1040">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="ff5be-1041">1.5.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="ff5be-1041">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ff5be-1042">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ff5be-1042">Az.Accounts</span></span>
* <span data-ttu-id="ff5be-1043">Lägg till kommandot Register-AzModule för stöd för AutoRest-genererade cmdletar</span><span class="sxs-lookup"><span data-stu-id="ff5be-1043">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="ff5be-1044">Uppdatera exempel för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="ff5be-1044">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ff5be-1045">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ff5be-1045">Az.Automation</span></span>
* <span data-ttu-id="ff5be-1046">Problem med att hämta vissa månadsscheman i flera Azure Automation-cmdletar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="ff5be-1046">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="ff5be-1047">Åtgärda problem med att Get-AzAutomationDscNode bara returnerar de 20 översta noderna.</span><span class="sxs-lookup"><span data-stu-id="ff5be-1047">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="ff5be-1048">Nu returneras alla noder</span><span class="sxs-lookup"><span data-stu-id="ff5be-1048">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="ff5be-1049">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="ff5be-1049">Az.Cdn</span></span>
* <span data-ttu-id="ff5be-1050">Nya Powershell-cmdletar för att aktivera/inaktivera anpassade domän-HTTPS har lagts till och de gamla har gjorts inaktuella</span><span class="sxs-lookup"><span data-stu-id="ff5be-1050">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ff5be-1051">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ff5be-1051">Az.Compute</span></span>
* <span data-ttu-id="ff5be-1052">Lägg till stöd för jokertecken för Get-cmdletar</span><span class="sxs-lookup"><span data-stu-id="ff5be-1052">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ff5be-1053">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ff5be-1053">Az.DataFactory</span></span>
* <span data-ttu-id="ff5be-1054">ADF .Net SDK-versionen har uppdaterats till 3.0.1</span><span class="sxs-lookup"><span data-stu-id="ff5be-1054">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="ff5be-1055">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="ff5be-1055">Az.LogicApp</span></span>
* <span data-ttu-id="ff5be-1056">Åtgärda problemet med att ListWorkflows endast hämtar den första sidan med resultat</span><span class="sxs-lookup"><span data-stu-id="ff5be-1056">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ff5be-1057">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ff5be-1057">Az.Network</span></span>
* <span data-ttu-id="ff5be-1058">Lägg till stöd för jokertecken för Network-cmdletar</span><span class="sxs-lookup"><span data-stu-id="ff5be-1058">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ff5be-1059">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ff5be-1059">Az.RecoveryServices</span></span>
* <span data-ttu-id="ff5be-1060">Stöd har lagts till för SQL Server i virtuella Azure-datorer</span><span class="sxs-lookup"><span data-stu-id="ff5be-1060">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="ff5be-1061">SDK-uppdatering</span><span class="sxs-lookup"><span data-stu-id="ff5be-1061">SDK Update</span></span>
* <span data-ttu-id="ff5be-1062">Get-ProtectableItem-incheckning i VMappContainer har tagits bort</span><span class="sxs-lookup"><span data-stu-id="ff5be-1062">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="ff5be-1063">Name och ServerName har lagts till som parametrar för Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="ff5be-1063">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="ff5be-1064">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ff5be-1064">Az.Resources</span></span>
* <span data-ttu-id="ff5be-1065">Lägg till parametern `-TemplateObject` i cmdletar för distribution</span><span class="sxs-lookup"><span data-stu-id="ff5be-1065">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="ff5be-1066">Mer information här: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="ff5be-1066">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="ff5be-1067">Åtgärda problem med piping av resultatet i `Get-AzResource` till `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="ff5be-1067">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="ff5be-1068">Mer information här: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="ff5be-1068">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="ff5be-1069">Åtgärda problem med ändring av JSON-datatyp när `Set-AzResource` körs</span><span class="sxs-lookup"><span data-stu-id="ff5be-1069">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="ff5be-1070">Mer information här: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="ff5be-1070">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="ff5be-1071">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ff5be-1071">Az.Sql</span></span>
* <span data-ttu-id="ff5be-1072">AuditingEndpointsCommunicator uppdateras.</span><span class="sxs-lookup"><span data-stu-id="ff5be-1072">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="ff5be-1073">Åtgärdar beteendet hos ett gränsscenario när nya diagnostikinställningar skapas.</span><span class="sxs-lookup"><span data-stu-id="ff5be-1073">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ff5be-1074">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ff5be-1074">Az.Storage</span></span>
* <span data-ttu-id="ff5be-1075">Stöd för BlockBlobStorage när Storage-konto skapas      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ff5be-1075">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="ff5be-1076">1.4.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="ff5be-1076">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="ff5be-1077">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ff5be-1077">Az.AnalysisServices</span></span>
* <span data-ttu-id="ff5be-1078">Inaktuell AddAzureASAccount-cmdlet</span><span class="sxs-lookup"><span data-stu-id="ff5be-1078">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ff5be-1079">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ff5be-1079">Az.Automation</span></span>
* <span data-ttu-id="ff5be-1080">Hjälpen för Import-AzAutomationDscNodeConfiguration har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="ff5be-1080">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="ff5be-1081">Konfigurationsnamnsvalidering har lagts till i cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="ff5be-1081">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="ff5be-1082">Förbättrad felhantering för cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="ff5be-1082">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="ff5be-1083">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ff5be-1083">Az.CognitiveServices</span></span>
* <span data-ttu-id="ff5be-1084">CustomSubdomainName har lagts till som en ny valfri parameter för New-AzCognitiveServicesAccount, som används för att ange underdomän för resursen.</span><span class="sxs-lookup"><span data-stu-id="ff5be-1084">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ff5be-1085">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ff5be-1085">Az.Compute</span></span>
* <span data-ttu-id="ff5be-1086">Problemet med ID-parameteruppsättningar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="ff5be-1086">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="ff5be-1087">Get-AzVMExtension har uppdaterats så att alla installerade tillägg visas om parametern Name inte har angetts</span><span class="sxs-lookup"><span data-stu-id="ff5be-1087">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="ff5be-1088">Parametrarna Tag och ResourceId har lagts till i cmdleten Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="ff5be-1088">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="ff5be-1089">Get-AzVmssVM utan instans-ID och med InstanceView kan visa virtuella VMSS-datorer med instansvyn.</span><span class="sxs-lookup"><span data-stu-id="ff5be-1089">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ff5be-1090">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ff5be-1090">Az.DataLakeStore</span></span>
* <span data-ttu-id="ff5be-1091">Cmdletar har lagts till för uppräkning och återställning av borttagna objekt i ADL</span><span class="sxs-lookup"><span data-stu-id="ff5be-1091">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="ff5be-1092">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="ff5be-1092">Az.EventHub</span></span>
* <span data-ttu-id="ff5be-1093">Ny boolesk egenskap SkipEmptyArchives har lagts till i Skip Empty Archives i CaptureDescription-klassen i Eventhub</span><span class="sxs-lookup"><span data-stu-id="ff5be-1093">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="ff5be-1094">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ff5be-1094">Az.KeyVault</span></span>
* <span data-ttu-id="ff5be-1095">Taggning i Set-AzKeyVaultSecret har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="ff5be-1095">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="ff5be-1096">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="ff5be-1096">Az.LogicApp</span></span>
* <span data-ttu-id="ff5be-1097">Grundläggande SKU har lagts till för Integrationskonton</span><span class="sxs-lookup"><span data-stu-id="ff5be-1097">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="ff5be-1098">XSLT 2.0, XSLT 3.0 och Flytande mappningstyper har lagts till</span><span class="sxs-lookup"><span data-stu-id="ff5be-1098">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="ff5be-1099">Nya cmdletar för integrationskontosammansättningar</span><span class="sxs-lookup"><span data-stu-id="ff5be-1099">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="ff5be-1100">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="ff5be-1100">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="ff5be-1101">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="ff5be-1101">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="ff5be-1102">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="ff5be-1102">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="ff5be-1103">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="ff5be-1103">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="ff5be-1104">Nya cmdletar för batchkonfiguration för integrationskonto</span><span class="sxs-lookup"><span data-stu-id="ff5be-1104">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="ff5be-1105">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="ff5be-1105">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="ff5be-1106">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="ff5be-1106">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="ff5be-1107">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="ff5be-1107">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="ff5be-1108">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="ff5be-1108">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="ff5be-1109">Logic App-SDK har uppdaterats till version 4.1.0</span><span class="sxs-lookup"><span data-stu-id="ff5be-1109">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ff5be-1110">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ff5be-1110">Az.Monitor</span></span>
* <span data-ttu-id="ff5be-1111">Hjälpen för Get-AzMetric har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="ff5be-1111">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ff5be-1112">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ff5be-1112">Az.Network</span></span>
* <span data-ttu-id="ff5be-1113">Hjälpexempel för Add-AzApplicationGatewayCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="ff5be-1113">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="ff5be-1114">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ff5be-1114">Az.OperationalInsights</span></span>
* <span data-ttu-id="ff5be-1115">Ytterligare stöd för datakällorna New och Get ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="ff5be-1115">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="ff5be-1116">Ny ApplicationInsights-typ har lagts till för att ge stöd för ”Get specific” och ”Get all” för ApplicationInsights-datakällor för angiven arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="ff5be-1116">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="ff5be-1117">Cmdleten New-AzOperationalInsightsApplicationInsightsDataSource har lagts till för att skapa datakälla med angivna parametrar för Application Insights-resurs: subscription Id, resourceGroupName och name.</span><span class="sxs-lookup"><span data-stu-id="ff5be-1117">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="ff5be-1118">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ff5be-1118">Az.Resources</span></span>
* <span data-ttu-id="ff5be-1119">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="ff5be-1119">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="ff5be-1120">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="ff5be-1120">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="ff5be-1121">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="ff5be-1121">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="ff5be-1122">Fel som gör att KeyCredentials inte kan skapas upprepade gånger har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="ff5be-1122">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="ff5be-1123">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ff5be-1123">Az.Sql</span></span>
* <span data-ttu-id="ff5be-1124">Lägg till stöd för hyperskalanivån för SQL DB</span><span class="sxs-lookup"><span data-stu-id="ff5be-1124">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="ff5be-1125">Ett fel har åtgärdats där återställningen kunde misslyckas på grund av onödiga inställningsegenskaper i restore-förfrågan</span><span class="sxs-lookup"><span data-stu-id="ff5be-1125">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ff5be-1126">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ff5be-1126">Az.Websites</span></span>
* <span data-ttu-id="ff5be-1127">Rätt exempel i Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="ff5be-1127">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="ff5be-1128">1.3.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="ff5be-1128">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ff5be-1129">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ff5be-1129">Az.Accounts</span></span>
* <span data-ttu-id="ff5be-1130">Uppdatera till den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="ff5be-1130">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="ff5be-1131">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ff5be-1131">Az.AnalysisServices</span></span>
<span data-ttu-id="ff5be-1132">Allmän tillgänglighet för Az.AnalysisServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="ff5be-1132">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ff5be-1133">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ff5be-1133">Az.Compute</span></span>
* <span data-ttu-id="ff5be-1134">AEM-tillägg: Lägg till stöd för UltraSSD-, P60-, P70- och P80-diskar</span><span class="sxs-lookup"><span data-stu-id="ff5be-1134">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="ff5be-1135">Uppdatera hjälpbeskrivning för Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="ff5be-1135">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="ff5be-1136">Uppdatera hjälpbeskrivning och exempel för Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="ff5be-1136">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ff5be-1137">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ff5be-1137">Az.RecoveryServices</span></span>
<span data-ttu-id="ff5be-1138">Allmän tillgänglighet för Az.RecoveryServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="ff5be-1138">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="ff5be-1139">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ff5be-1139">Az.Resources</span></span>
* <span data-ttu-id="ff5be-1140">Korrigera taggar för resursgrupper</span><span class="sxs-lookup"><span data-stu-id="ff5be-1140">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="ff5be-1141">Mer information här: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="ff5be-1141">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="ff5be-1142">Åtgärda problem där `Get-AzureRmRoleAssignment` inte respekterar -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="ff5be-1142">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="ff5be-1143">Mer information här: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="ff5be-1143">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="ff5be-1144">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ff5be-1144">Az.Sql</span></span>
* <span data-ttu-id="ff5be-1145">Lägga till Get/Set-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="ff5be-1145">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="ff5be-1146">Åtgärda problem där ett nullref-undantag uppstår när du kör SQL-cmdletar och inte är inloggad på ett Azure-konto</span><span class="sxs-lookup"><span data-stu-id="ff5be-1146">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="ff5be-1147">Åtgärda nullref-undantag i Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="ff5be-1147">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="ff5be-1148">1.2.1 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="ff5be-1148">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ff5be-1149">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ff5be-1149">Az.Accounts</span></span>
* <span data-ttu-id="ff5be-1150">Version med rätt version av autentisering</span><span class="sxs-lookup"><span data-stu-id="ff5be-1150">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="ff5be-1151">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ff5be-1151">Az.AnalysisServices</span></span>
* <span data-ttu-id="ff5be-1152">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="ff5be-1152">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ff5be-1153">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ff5be-1153">Az.RecoveryServices</span></span>
* <span data-ttu-id="ff5be-1154">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="ff5be-1154">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="ff5be-1155">1.2.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="ff5be-1155">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ff5be-1156">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ff5be-1156">Az.Accounts</span></span>
* <span data-ttu-id="ff5be-1157">Lägga till interaktiv autentisering och autentisering med användarnamn/lösenord för endast Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="ff5be-1157">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="ff5be-1158">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="ff5be-1158">Update incorrect online help URLs</span></span>
* <span data-ttu-id="ff5be-1159">Lägga till varningsmeddelande i PS Core för Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="ff5be-1159">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="ff5be-1160">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="ff5be-1160">Az.Aks</span></span>
* <span data-ttu-id="ff5be-1161">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="ff5be-1161">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ff5be-1162">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ff5be-1162">Az.Automation</span></span>
* <span data-ttu-id="ff5be-1163">Stöd för Python 2-runbookflöden har lagts till</span><span class="sxs-lookup"><span data-stu-id="ff5be-1163">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="ff5be-1164">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="ff5be-1164">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="ff5be-1165">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="ff5be-1165">Az.Cdn</span></span>
* <span data-ttu-id="ff5be-1166">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="ff5be-1166">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ff5be-1167">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ff5be-1167">Az.Compute</span></span>
* <span data-ttu-id="ff5be-1168">Lägga till cmdleten Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="ff5be-1168">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="ff5be-1169">Lägga till TempDisk-parameter i Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ff5be-1169">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="ff5be-1170">Korrigera varningsmeddelande för New-AzVM</span><span class="sxs-lookup"><span data-stu-id="ff5be-1170">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="ff5be-1171">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ff5be-1171">Az.ContainerRegistry</span></span>
* <span data-ttu-id="ff5be-1172">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="ff5be-1172">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ff5be-1173">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ff5be-1173">Az.DataFactory</span></span>
* <span data-ttu-id="ff5be-1174">ADF .Net SDK-versionen har uppdaterats till 3.0.0</span><span class="sxs-lookup"><span data-stu-id="ff5be-1174">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ff5be-1175">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ff5be-1175">Az.DataLakeStore</span></span>
* <span data-ttu-id="ff5be-1176">Åtgärda problem med ADLS-slutpunkt vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="ff5be-1176">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="ff5be-1177">Mer information här: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="ff5be-1177">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="ff5be-1178">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="ff5be-1178">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ff5be-1179">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ff5be-1179">Az.IotHub</span></span>
* <span data-ttu-id="ff5be-1180">Lägga till kodningsformat i cmdleten Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="ff5be-1180">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="ff5be-1181">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ff5be-1181">Az.KeyVault</span></span>
* <span data-ttu-id="ff5be-1182">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="ff5be-1182">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ff5be-1183">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ff5be-1183">Az.Network</span></span>
* <span data-ttu-id="ff5be-1184">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="ff5be-1184">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="ff5be-1185">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ff5be-1185">Az.Resources</span></span>
* <span data-ttu-id="ff5be-1186">Åtgärda felaktiga exempel i referensdokumentationen ”New-AzADAppCredential” och ”New-AzADSpCredential”</span><span class="sxs-lookup"><span data-stu-id="ff5be-1186">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="ff5be-1187">Åtgärda problem där sökvägen för parametern ”-TemplateFile” inte omvandlas innan cmdletarna för distribution i resursgruppen körs</span><span class="sxs-lookup"><span data-stu-id="ff5be-1187">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="ff5be-1188">Az.Resources: Korrigera dokumentationen om standardvärdet för New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="ff5be-1188">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="ff5be-1189">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="ff5be-1189">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="ff5be-1190">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="ff5be-1190">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="ff5be-1191">Åtgärda formateringsproblemet med objektet ”PSResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="ff5be-1191">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="ff5be-1192">Mer information här: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="ff5be-1192">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="ff5be-1193">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ff5be-1193">Az.ServiceFabric</span></span>
* <span data-ttu-id="ff5be-1194">Återställ när ett certifikat läggs till i en Virtual Machine Scale Sets-modell men ett undantag genereras. Detta har gjorts för att åtgärda följande fel: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="ff5be-1194">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="ff5be-1195">Korrigera några felmeddelanden.</span><span class="sxs-lookup"><span data-stu-id="ff5be-1195">Fix some error messages.</span></span>
* <span data-ttu-id="ff5be-1196">Korrigering av skapande av kluster med ARM-mall som är standard för New-AzServiceFabriCluster som inte fungerade med migrering till Az.</span><span class="sxs-lookup"><span data-stu-id="ff5be-1196">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="ff5be-1197">Korrigering av tilläggning av kluster/programcertifikat så att endast VM Scale Sets som motsvarar klustret läggs till genom att kontrollera ID för klustret i tillägget.</span><span class="sxs-lookup"><span data-stu-id="ff5be-1197">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="ff5be-1198">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="ff5be-1198">Az.SignalR</span></span>
* <span data-ttu-id="ff5be-1199">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="ff5be-1199">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="ff5be-1200">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ff5be-1200">Az.Sql</span></span>
* <span data-ttu-id="ff5be-1201">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="ff5be-1201">Update incorrect online help URLs</span></span>
* <span data-ttu-id="ff5be-1202">Uppdaterad parameterbeskrivning för LicenseType-parameter med möjliga värden</span><span class="sxs-lookup"><span data-stu-id="ff5be-1202">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="ff5be-1203">Korrigering för att uppdatera hanterad instansidentitet som inte fungerar när det är den enda uppdaterade egenskapen</span><span class="sxs-lookup"><span data-stu-id="ff5be-1203">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="ff5be-1204">Stöd för anpassad sortering på hanterad instans</span><span class="sxs-lookup"><span data-stu-id="ff5be-1204">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ff5be-1205">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ff5be-1205">Az.Storage</span></span>
* <span data-ttu-id="ff5be-1206">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="ff5be-1206">Update incorrect online help URLs</span></span>
* <span data-ttu-id="ff5be-1207">Tillhandahåll detaljerat felmeddelande när en användare försöker hämta/konfigurera klassisk loggning/mått på ett Premium Storage-konto eftersom Premium Storage-kontot inte har stöd för klassisk loggning/mått.</span><span class="sxs-lookup"><span data-stu-id="ff5be-1207">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="ff5be-1208">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="ff5be-1208">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="ff5be-1209">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="ff5be-1209">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="ff5be-1210">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="ff5be-1210">Az.TrafficManager</span></span>
* <span data-ttu-id="ff5be-1211">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="ff5be-1211">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ff5be-1212">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ff5be-1212">Az.Websites</span></span>
* <span data-ttu-id="ff5be-1213">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="ff5be-1213">Update incorrect online help URLs</span></span>
* <span data-ttu-id="ff5be-1214">Korrigerar ”New-AzWebAppSSLBinding” så att certifikatet laddas upp till rätt resursgrupp och plats om appen finns i en ASE.</span><span class="sxs-lookup"><span data-stu-id="ff5be-1214">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="ff5be-1215">Korrigerar ”New-AzWebAppSSLBinding” så att taggarna inte skrivs över på en bindning av ett SSL-certifikat till en app</span><span class="sxs-lookup"><span data-stu-id="ff5be-1215">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="ff5be-1216">1.1.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="ff5be-1216">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ff5be-1217">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ff5be-1217">Az.Accounts</span></span>
* <span data-ttu-id="ff5be-1218">Lade till omfattningen ”Lokal” till Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="ff5be-1218">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ff5be-1219">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ff5be-1219">Az.Compute</span></span>
* <span data-ttu-id="ff5be-1220">Namn är nu valfritt i ID-parametern för Restart/Start/Stop/Remove/Set-AzVM och Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="ff5be-1220">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="ff5be-1221">Uppdaterade beskrivningen av ID i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="ff5be-1221">Updated the description of ID in help files</span></span>
* <span data-ttu-id="ff5be-1222">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ff5be-1222">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ff5be-1223">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ff5be-1223">Az.DataLakeStore</span></span>
* <span data-ttu-id="ff5be-1224">Uppdatera sdk-versionen av dataplanet till 1.1.14 för SDK-korrigeringar.</span><span class="sxs-lookup"><span data-stu-id="ff5be-1224">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="ff5be-1225">Korrigerade hanteringen av negativ accesstime och modificationtime för getfilestatus och liststatus; korrigera asynkront annulleringstoken</span><span class="sxs-lookup"><span data-stu-id="ff5be-1225">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="ff5be-1226">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="ff5be-1226">Az.EventGrid</span></span>
* <span data-ttu-id="ff5be-1227">Uppdaterat för användning av API-versionen 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="ff5be-1227">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="ff5be-1228">Uppdaterade följande cmdletar för att stödja nytt scenario i API-versionen 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="ff5be-1228">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="ff5be-1229">New-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="ff5be-1229">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="ff5be-1230">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="ff5be-1230">Event Time-To-Live,</span></span>
        - <span data-ttu-id="ff5be-1231">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="ff5be-1231">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="ff5be-1232">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="ff5be-1232">Dead letter endpoint.</span></span>
    - <span data-ttu-id="ff5be-1233">Update-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="ff5be-1233">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="ff5be-1234">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="ff5be-1234">Event Time-To-Live,</span></span>
        - <span data-ttu-id="ff5be-1235">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="ff5be-1235">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="ff5be-1236">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="ff5be-1236">Dead letter endpoint.</span></span>
* <span data-ttu-id="ff5be-1237">Lade till nya enum-värden (storageQueue och hybridConnection) för alternativet EndpointType i cmdletarna New-AzureRmEventGridSubscription och Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="ff5be-1237">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="ff5be-1238">Visa varningsmeddelanden om skapande eller uppdatering av händelseprenumerationen förväntas medföra manuell åtgärd från användaren.</span><span class="sxs-lookup"><span data-stu-id="ff5be-1238">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ff5be-1239">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ff5be-1239">Az.IotHub</span></span>
* <span data-ttu-id="ff5be-1240">Har uppdaterats till den senaste versionen av SDK:n lotHub</span><span class="sxs-lookup"><span data-stu-id="ff5be-1240">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="ff5be-1241">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="ff5be-1241">Az.LogicApp</span></span>
* <span data-ttu-id="ff5be-1242">Get-AzLogicApp visar en lista över alla som inte har angivet namn</span><span class="sxs-lookup"><span data-stu-id="ff5be-1242">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="ff5be-1243">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ff5be-1243">Az.Resources</span></span>
* <span data-ttu-id="ff5be-1244">Åtgärdade problem med parameteruppsättningen när parametrarna -ODataQuery och -ResourceId anges för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="ff5be-1244">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="ff5be-1245">Mer information här: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="ff5be-1245">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="ff5be-1246">Åtgärdade hantering av parametern -Custom i New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ff5be-1246">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="ff5be-1247">Korrigerade stavfel i New-AzDeployment-dokumentationen</span><span class="sxs-lookup"><span data-stu-id="ff5be-1247">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="ff5be-1248">Gjorde parametern -MailNickname obligatorisk för New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="ff5be-1248">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="ff5be-1249">Mer information här: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="ff5be-1249">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="ff5be-1250">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="ff5be-1250">Az.SignalR</span></span>
* <span data-ttu-id="ff5be-1251">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ff5be-1251">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="ff5be-1252">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ff5be-1252">Az.Sql</span></span>
* <span data-ttu-id="ff5be-1253">Konverterade lagringshanteringsklientens beroende av den normala SDK-implementeringen.</span><span class="sxs-lookup"><span data-stu-id="ff5be-1253">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ff5be-1254">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ff5be-1254">Az.Storage</span></span>
* <span data-ttu-id="ff5be-1255">Angav StorageAccountName för lagringskontext som det verkliga namnet på lagringskontot när det skapas med Sas Token, OAuth eller Anonymous</span><span class="sxs-lookup"><span data-stu-id="ff5be-1255">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="ff5be-1256">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="ff5be-1256">New-AzStorageContext</span></span>
* <span data-ttu-id="ff5be-1257">Skapade Sas Token för Blob Snapshot-objekt med parametern -FullUri, åtgärdade den returnerade URI:n så att den blir URI för ögonblicksbild</span><span class="sxs-lookup"><span data-stu-id="ff5be-1257">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="ff5be-1258">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="ff5be-1258">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ff5be-1259">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ff5be-1259">Az.Websites</span></span>
* <span data-ttu-id="ff5be-1260">Åtgärdade en bugg i datumparsningen i Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="ff5be-1260">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="ff5be-1261">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ff5be-1261">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="ff5be-1262">1.0.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="ff5be-1262">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="ff5be-1263">Allmänt</span><span class="sxs-lookup"><span data-stu-id="ff5be-1263">General</span></span>

- <span data-ttu-id="ff5be-1264">Allmän tillgänglighet för Az-modulen</span><span class="sxs-lookup"><span data-stu-id="ff5be-1264">General Availability of Az Module</span></span>
- <span data-ttu-id="ff5be-1265">Onlinehjälp för varje modul</span><span class="sxs-lookup"><span data-stu-id="ff5be-1265">Online help for each module</span></span>
- <span data-ttu-id="ff5be-1266">Mer information och en översikt finns på [Az-informationssidan](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="ff5be-1266">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="ff5be-1267">Information om hur du migrerar från AzureRM finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ff5be-1267">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="ff5be-1268">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ff5be-1268">Az.Accounts</span></span>
- <span data-ttu-id="ff5be-1269">Har ändrats från Az.Profile</span><span class="sxs-lookup"><span data-stu-id="ff5be-1269">Changed from Az.Profile</span></span>
- <span data-ttu-id="ff5be-1270">Fasta tabellformat för profil- och kontexttyper</span><span class="sxs-lookup"><span data-stu-id="ff5be-1270">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="ff5be-1271">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ff5be-1271">Az.ApiManagement</span></span>
- <span data-ttu-id="ff5be-1272">Korrigeringar för #7002</span><span class="sxs-lookup"><span data-stu-id="ff5be-1272">Fixes for #7002</span></span>
- <span data-ttu-id="ff5be-1273">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ff5be-1273">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="ff5be-1274">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="ff5be-1274">Az.Batch</span></span>
- <span data-ttu-id="ff5be-1275">Lade till möjligheten att se vilken version av Azure Batch Node Agent som körs på var och en av de virtuella datorerna i en pool, via den nya egenskapen `NodeAgentInformation` på `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="ff5be-1275">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="ff5be-1276">Standarden `Caching` för `PSDataDisk` är nu `ReadWrite` i stället för `None`.</span><span class="sxs-lookup"><span data-stu-id="ff5be-1276">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="ff5be-1277">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ff5be-1277">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="ff5be-1278">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="ff5be-1278">Az.Billing</span></span>
- <span data-ttu-id="ff5be-1279">Kombinerar cmdletarna för fakturering, förbrukning och UsageAggregates. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ff5be-1279">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="ff5be-1280">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="ff5be-1280">Az.CognitivServices</span></span>
- <span data-ttu-id="ff5be-1281">Lade till kompletterare för SkuName och Typem som är tillgängliga i New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="ff5be-1281">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="ff5be-1282">Tog bort parameteruppsättningen GetSkusWithAccountParamSetName från Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="ff5be-1282">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="ff5be-1283">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="ff5be-1283">Az.ContainerInstance</span></span>
- <span data-ttu-id="ff5be-1284">Stöd för ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="ff5be-1284">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="ff5be-1285">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="ff5be-1285">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="ff5be-1286">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ff5be-1286">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="ff5be-1287">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ff5be-1287">Az.DataLakeStore</span></span>
- <span data-ttu-id="ff5be-1288">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ff5be-1288">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="ff5be-1289">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ff5be-1289">Az.Monitor</span></span>
- <span data-ttu-id="ff5be-1290">Döpte om Az.Insights till Az.Monitor och andra mindre icke-bakåtkompatibla ändringar. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ff5be-1290">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="ff5be-1291">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ff5be-1291">Az.KeyVault</span></span>
- <span data-ttu-id="ff5be-1292">Tog bort den inaktuella egenskapen PurgeDisabled från utdatatyper</span><span class="sxs-lookup"><span data-stu-id="ff5be-1292">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="ff5be-1293">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="ff5be-1293">Az.MachineLearning</span></span>
- <span data-ttu-id="ff5be-1294">Inkluderade cmdletarna från modulen Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="ff5be-1294">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="ff5be-1295">Az.Media</span><span class="sxs-lookup"><span data-stu-id="ff5be-1295">Az.Media</span></span>
- <span data-ttu-id="ff5be-1296">Tog bort inaktuella -Tags-alias från New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="ff5be-1296">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="ff5be-1297">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ff5be-1297">Az.Network</span></span>
<span data-ttu-id="ff5be-1298">Stöd har lagts till för konfiguration av RewriteRuleSets i Application Gateway</span><span class="sxs-lookup"><span data-stu-id="ff5be-1298">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="ff5be-1299">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="ff5be-1299">New cmdlets added:</span></span>
        - <span data-ttu-id="ff5be-1300">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ff5be-1300">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="ff5be-1301">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ff5be-1301">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="ff5be-1302">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ff5be-1302">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="ff5be-1303">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ff5be-1303">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="ff5be-1304">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ff5be-1304">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="ff5be-1305">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="ff5be-1305">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="ff5be-1306">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="ff5be-1306">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="ff5be-1307">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="ff5be-1307">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="ff5be-1308">Cmdletar har uppdaterats med den valfria parametern -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ff5be-1308">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="ff5be-1309">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ff5be-1309">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="ff5be-1310">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="ff5be-1310">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="ff5be-1311">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="ff5be-1311">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="ff5be-1312">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ff5be-1312">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="ff5be-1313">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="ff5be-1313">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="ff5be-1314">New-AzureRmApplicationGatewayUrlPathMapConfig har lagt till KeyVault-stöd för Application Gateway med Identity.</span><span class="sxs-lookup"><span data-stu-id="ff5be-1314">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="ff5be-1315">Cmdletar har uppdaterats med den valfria parametern -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="ff5be-1315">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="ff5be-1316">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="ff5be-1316">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="ff5be-1317">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="ff5be-1317">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="ff5be-1318">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="ff5be-1318">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="ff5be-1319">Cmdleten New-AzApplicationGateway har uppdaterats med den valfria parametern -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="ff5be-1319">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="ff5be-1320">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ff5be-1320">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="ff5be-1321">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ff5be-1321">Az.OperationalInsights</span></span>
- <span data-ttu-id="ff5be-1322">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ff5be-1322">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="ff5be-1323">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="ff5be-1323">Az.Profile</span></span>
- <span data-ttu-id="ff5be-1324">Modulnamnet har ändrats till Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ff5be-1324">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="ff5be-1325">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ff5be-1325">Az.RecoveryServices</span></span>
- <span data-ttu-id="ff5be-1326">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ff5be-1326">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="ff5be-1327">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ff5be-1327">Az.Resources</span></span>
- <span data-ttu-id="ff5be-1328">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ff5be-1328">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="ff5be-1329">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ff5be-1329">Az.ServiceFabric</span></span>
- <span data-ttu-id="ff5be-1330">Stöd för specificering av certifikat efter eget namn och tumavtryck</span><span class="sxs-lookup"><span data-stu-id="ff5be-1330">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="ff5be-1331">Information om fler icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ff5be-1331">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="ff5be-1332">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="ff5be-1332">Az.SIgnalR</span></span>
- <span data-ttu-id="ff5be-1333">Allmän tillgänglighet för PowerShell-cmdletar för SIgnalR</span><span class="sxs-lookup"><span data-stu-id="ff5be-1333">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="ff5be-1334">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ff5be-1334">Az.Sql</span></span>
- <span data-ttu-id="ff5be-1335">Lade till de nya identifieringstyperna Data_Exfiltration och Unsafe_Action i Threat Detection-cmdletar</span><span class="sxs-lookup"><span data-stu-id="ff5be-1335">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="ff5be-1336">Uppdaterade dokumentationsexempel för Sql Auditing-cmdletar</span><span class="sxs-lookup"><span data-stu-id="ff5be-1336">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="ff5be-1337">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ff5be-1337">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="ff5be-1338">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ff5be-1338">Az.Storage</span></span>
- <span data-ttu-id="ff5be-1339">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ff5be-1339">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="ff5be-1340">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ff5be-1340">Az.Websites</span></span>
- <span data-ttu-id="ff5be-1341">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ff5be-1341">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="ff5be-1342">0.7.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="ff5be-1342">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="ff5be-1343">Allmänt</span><span class="sxs-lookup"><span data-stu-id="ff5be-1343">General</span></span>

* <span data-ttu-id="ff5be-1344">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="ff5be-1344">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="ff5be-1345">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ff5be-1345">Az.Compute</span></span>

* <span data-ttu-id="ff5be-1346">Lade till stöd för UltraSSD och Galleriavbildningar i de enkla parameteruppsättningarna för `New-AzVm(ss)`-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="ff5be-1346">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="ff5be-1347">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ff5be-1347">Az.DataLakeStore</span></span>

* <span data-ttu-id="ff5be-1348">Åtgärdade avslutande snedstreck i domänen för adls-konto</span><span class="sxs-lookup"><span data-stu-id="ff5be-1348">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="ff5be-1349">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="ff5be-1349">Az.FrontDoor</span></span>

* <span data-ttu-id="ff5be-1350">Brutna länkar korrigerades</span><span class="sxs-lookup"><span data-stu-id="ff5be-1350">Fixed some broken links</span></span>
    - <span data-ttu-id="ff5be-1351">I artiklarna New-AzureRmFrontDoor och Set-AzureRmFrontDoor artiklar korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="ff5be-1351">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="ff5be-1352">I artikeln New-AzureRmFrontDoorManagedRuleObject korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="ff5be-1352">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="ff5be-1353">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ff5be-1353">Az.RecoveryServices</span></span>

* <span data-ttu-id="ff5be-1354">Lade till valideringar på klientsidan för Azure-filresurs med återställningsåtgärder.</span><span class="sxs-lookup"><span data-stu-id="ff5be-1354">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="ff5be-1355">Gjorde storageAccountName och storageAccountResourceGroupName valfritt för afs-återställning.</span><span class="sxs-lookup"><span data-stu-id="ff5be-1355">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="ff5be-1356">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ff5be-1356">Az.Resources</span></span>

* <span data-ttu-id="ff5be-1357">Korrigering för https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="ff5be-1357">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="ff5be-1358">Uppdaterade Get-AzureRmRoleAssignment så att prenumerationsomfattningen används om den anges vid begäran om klassiska administratörer.</span><span class="sxs-lookup"><span data-stu-id="ff5be-1358">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="ff5be-1359">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ff5be-1359">Az.Sql</span></span>

* <span data-ttu-id="ff5be-1360">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="ff5be-1360">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="ff5be-1361">Korrigerade ett problem med Get-AzureRmSqlDatabaseVulnerabilityAssessment med DotNet-kärna</span><span class="sxs-lookup"><span data-stu-id="ff5be-1361">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="ff5be-1362">Ändrade dokumentationen för hjälpmeddelanden som rör SQL Auditing-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="ff5be-1362">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="ff5be-1363">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ff5be-1363">Az.Storage</span></span>

* <span data-ttu-id="ff5be-1364">Lade till -EnableHierarchicalNamespace i New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ff5be-1364">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="ff5be-1365">Åtgärdade problemet med att cmdleten Copy File inte kunde återanvända källkontexten på målet om inte -DestContext angetts</span><span class="sxs-lookup"><span data-stu-id="ff5be-1365">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="ff5be-1366">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="ff5be-1366">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="ff5be-1367">Stöd för statisk webbplatskonfiguration</span><span class="sxs-lookup"><span data-stu-id="ff5be-1367">Support Static Website configuration</span></span>
    - <span data-ttu-id="ff5be-1368">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="ff5be-1368">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="ff5be-1369">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="ff5be-1369">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="ff5be-1370">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ff5be-1370">Az.Websites</span></span>

* <span data-ttu-id="ff5be-1371">Set-AzureRmWebApp och Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ff5be-1371">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="ff5be-1372">Ny parameter (-AzureStoragePath) har lagts till för att ange att Azure Storage-sökvägar ska monteras i containerappar i Windows och Linux.</span><span class="sxs-lookup"><span data-stu-id="ff5be-1372">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="ff5be-1373">Använder utdata från den nya cmdleten New-AzureRmWebAppAzureStoragePath som en parameter för att ange sökvägar för Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="ff5be-1373">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="ff5be-1374">0.6.1 – november 2018</span><span class="sxs-lookup"><span data-stu-id="ff5be-1374">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="ff5be-1375">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ff5be-1375">Az.ApiManagement</span></span>
* <span data-ttu-id="ff5be-1376">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="ff5be-1376">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="ff5be-1377">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ff5be-1377">Az.Automation</span></span>
* <span data-ttu-id="ff5be-1378">Swagger baserade Azure Automation-cmdletar</span><span class="sxs-lookup"><span data-stu-id="ff5be-1378">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="ff5be-1379">Cmdletar för Uppdateringshantering har lagts till</span><span class="sxs-lookup"><span data-stu-id="ff5be-1379">Added Update Management cmdlets</span></span>
* <span data-ttu-id="ff5be-1380">Cmdletar för källkontroll har lagts till</span><span class="sxs-lookup"><span data-stu-id="ff5be-1380">Added Source Control cmdlets</span></span>
* <span data-ttu-id="ff5be-1381">Remove-AzureRmAutomationHybridWorkerGroup-cmdlet har lagts till</span><span class="sxs-lookup"><span data-stu-id="ff5be-1381">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="ff5be-1382">Kommandot för DSC-registreringsnod har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="ff5be-1382">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="ff5be-1383">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ff5be-1383">Az.Compute</span></span>
* <span data-ttu-id="ff5be-1384">Problem med SystemAssigned-identitet har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="ff5be-1384">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="ff5be-1385">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="ff5be-1385">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="ff5be-1386">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="ff5be-1386">Az.ContainerInstance</span></span>
* <span data-ttu-id="ff5be-1387">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="ff5be-1387">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="ff5be-1388">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="ff5be-1388">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="ff5be-1389">uppdatera exempelbeskrivningen för marketplace-cmdletar</span><span class="sxs-lookup"><span data-stu-id="ff5be-1389">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="ff5be-1390">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ff5be-1390">Az.Network</span></span>
* <span data-ttu-id="ff5be-1391">Cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomErreller Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="ff5be-1391">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="ff5be-1392">ICMP tillbaka till stöd för Azure Firewall-nätverksprotokoll har lagts till</span><span class="sxs-lookup"><span data-stu-id="ff5be-1392">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="ff5be-1393">Uppdatera cmdlet Test-AzureRmNetworkWatcherConnectivity, lägga till verifiering av mål-id, adress och port.</span><span class="sxs-lookup"><span data-stu-id="ff5be-1393">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="ff5be-1394">Åtgärda problem med minnesanvändning i VirtualNetwork-karta</span><span class="sxs-lookup"><span data-stu-id="ff5be-1394">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="ff5be-1395">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="ff5be-1395">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="ff5be-1396">Åtgärda för att ändra principen för en skyddad fildelning.</span><span class="sxs-lookup"><span data-stu-id="ff5be-1396">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="ff5be-1397">Tidszonsprincipen har konverterats till versaler.</span><span class="sxs-lookup"><span data-stu-id="ff5be-1397">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="ff5be-1398">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="ff5be-1398">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="ff5be-1399">Exempel i New-AzureRmRecoveryServicesAsrProtectableItem har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="ff5be-1399">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="ff5be-1400">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="ff5be-1400">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="ff5be-1401">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="ff5be-1401">Az.Relay</span></span>
* <span data-ttu-id="ff5be-1402">Valfri parameter -KeyValue till New-AzureRmRelayKey cmdlet har lagts till, vilket gör det möjligt för användare att tillhandahålla KeyValue.</span><span class="sxs-lookup"><span data-stu-id="ff5be-1402">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="ff5be-1403">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ff5be-1403">Az.Resources</span></span>
* <span data-ttu-id="ff5be-1404">Uppdatera hjälpdokumentation för resursidentitet kopplad till parametrar i `New-AzureRmPolicyAssignment` och `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="ff5be-1404">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="ff5be-1405">Lägg till ett exempel för New-AzureRmPolicyDefinition som använder -Metadata</span><span class="sxs-lookup"><span data-stu-id="ff5be-1405">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="ff5be-1406">Korrigera så att skiftläge behålls i taggnycklar i NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="ff5be-1406">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="ff5be-1407">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ff5be-1407">Az.ServiceFabric</span></span>
* <span data-ttu-id="ff5be-1408">Lägg till utfasningsmeddelanden för kommande icke-kompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="ff5be-1408">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="ff5be-1409">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ff5be-1409">Az.Sql</span></span>
* <span data-ttu-id="ff5be-1410">Nya cmdletar för CRUD-åtgärder på Azure Sql Database-hanterad instans och Azure Sql-hanterad databas</span><span class="sxs-lookup"><span data-stu-id="ff5be-1410">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="ff5be-1411">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="ff5be-1411">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="ff5be-1412">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="ff5be-1412">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="ff5be-1413">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="ff5be-1413">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="ff5be-1414">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="ff5be-1414">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="ff5be-1415">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="ff5be-1415">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="ff5be-1416">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="ff5be-1416">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="ff5be-1417">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="ff5be-1417">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="ff5be-1418">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="ff5be-1418">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="ff5be-1419">Hantering av utökad granskningsprincip på en server eller en databas har aktiverats.</span><span class="sxs-lookup"><span data-stu-id="ff5be-1419">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="ff5be-1420">Ny parameter (PredicateExpression) har lagts till för att aktivera filtrering av granskningsloggar.</span><span class="sxs-lookup"><span data-stu-id="ff5be-1420">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="ff5be-1421">Cmdletar har ändrats så att de använder SQL-klienter i stället för äldre klienter.</span><span class="sxs-lookup"><span data-stu-id="ff5be-1421">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="ff5be-1422">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="ff5be-1422">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="ff5be-1423">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="ff5be-1423">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="ff5be-1424">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="ff5be-1424">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="ff5be-1425">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="ff5be-1425">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="ff5be-1426">Problem med att använda Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings med lagringskontots namnparameter har korrigerats</span><span class="sxs-lookup"><span data-stu-id="ff5be-1426">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="ff5be-1427">0.5.0 – november 2018</span><span class="sxs-lookup"><span data-stu-id="ff5be-1427">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="ff5be-1428">Allmänt</span><span class="sxs-lookup"><span data-stu-id="ff5be-1428">General</span></span>
* <span data-ttu-id="ff5be-1429">Lade till resurskompletterare till många kärn-cmdletar – dessa gör att du kan stega genom befintliga resursnamn med TABB vid interaktiva anrop till cmdletar</span><span class="sxs-lookup"><span data-stu-id="ff5be-1429">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="ff5be-1430">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="ff5be-1430">Az.Profile</span></span>
* <span data-ttu-id="ff5be-1431">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="ff5be-1431">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="ff5be-1432">Bytte namn på parametern TenantId i cmdleten Connect-AzAccount till Tenant och lade till ett alias för TenantId</span><span class="sxs-lookup"><span data-stu-id="ff5be-1432">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="ff5be-1433">Uppdaterade TenantId-beskrivningen för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="ff5be-1433">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="ff5be-1434">Åtgärda felmeddelande för misslyckad inloggning när du tillhandahåller klientdomän</span><span class="sxs-lookup"><span data-stu-id="ff5be-1434">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="ff5be-1435">Åtgärda problem med att kontextnamn hamnar i konflikt för konton utan prenumerationer i klientorganisationen</span><span class="sxs-lookup"><span data-stu-id="ff5be-1435">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="ff5be-1436">Åtgärda problem med DataLake-slutpunkter vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="ff5be-1436">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="ff5be-1437">Åtgärdade problem med att Disconnect-AzAccount kastades om den inte anslöts</span><span class="sxs-lookup"><span data-stu-id="ff5be-1437">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="ff5be-1438">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ff5be-1438">Az.CognitiveServices</span></span>
* <span data-ttu-id="ff5be-1439">Lade till åtgärden Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="ff5be-1439">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ff5be-1440">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ff5be-1440">Az.Compute</span></span>
* <span data-ttu-id="ff5be-1441">Lade till cmdletarna Add-AzVmssVMDataDisk och Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="ff5be-1441">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="ff5be-1442">Get-AzVMImage visar AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="ff5be-1442">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="ff5be-1443">Åtgärdade att värdena för alternativen SetAzVMChefExtension -BootstrapOptions och -JsonAttribute inte angavs i json-format.</span><span class="sxs-lookup"><span data-stu-id="ff5be-1443">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ff5be-1444">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ff5be-1444">Az.DataLakeStore</span></span>
* <span data-ttu-id="ff5be-1445">Uppdatera DataLake-paketet till 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="ff5be-1445">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="ff5be-1446">Lägg till standardsamtidighet för flertrådade åtgärder.</span><span class="sxs-lookup"><span data-stu-id="ff5be-1446">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="ff5be-1447">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="ff5be-1447">Az.Insights</span></span>
* <span data-ttu-id="ff5be-1448">Åtgärdade problem #7267 (autoskalningsområde)</span><span class="sxs-lookup"><span data-stu-id="ff5be-1448">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="ff5be-1449">Problem med att uppräknade parametrar inte ställdes in ordentligt när du skapade en ny autoskalningsregel (de ställdes alltid in med standardvärdet).</span><span class="sxs-lookup"><span data-stu-id="ff5be-1449">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="ff5be-1450">Åtgärdade problem #7513 [Insights] Set-AzDiagnosticSetting kräver uttrycklig specifikation av kategorier när inställningar skapas</span><span class="sxs-lookup"><span data-stu-id="ff5be-1450">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="ff5be-1451">Nu kräver inte cmdleten uttrycklig anvisning av kategorierna för att aktiveras under skapande, d.v.s. den fungerar enligt beskrivning</span><span class="sxs-lookup"><span data-stu-id="ff5be-1451">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ff5be-1452">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ff5be-1452">Az.Network</span></span>
* <span data-ttu-id="ff5be-1453">PeeringType ändrades till en obligatorisk parameter för följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="ff5be-1453">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="ff5be-1454">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="ff5be-1454">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="ff5be-1455">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="ff5be-1455">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="ff5be-1456">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="ff5be-1456">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="ff5be-1457">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="ff5be-1457">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="ff5be-1458">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="ff5be-1458">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="ff5be-1459">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="ff5be-1459">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="ff5be-1460">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="ff5be-1460">Az.PolicyInsights</span></span>
* <span data-ttu-id="ff5be-1461">Cmdletar för principreparation har lagts till</span><span class="sxs-lookup"><span data-stu-id="ff5be-1461">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="ff5be-1462">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ff5be-1462">Az.Resources</span></span>
* <span data-ttu-id="ff5be-1463">Korrigering för https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="ff5be-1463">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="ff5be-1464">Tillåt att resurser listas med parametern -ResourceId för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="ff5be-1464">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="ff5be-1465">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ff5be-1465">Az.ServiceBus</span></span>
* <span data-ttu-id="ff5be-1466">Skrivskyddad MigrationState-egenskap har lagts till i PSServiceBusMigrationConfigurationAttributes, som hjälper till att hålla koll på migreringstillståndet.</span><span class="sxs-lookup"><span data-stu-id="ff5be-1466">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="ff5be-1467">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ff5be-1467">Az.ServiceFabric</span></span>
* <span data-ttu-id="ff5be-1468">Åtgärda att lägga till certifikat till Linux-Vmss.</span><span class="sxs-lookup"><span data-stu-id="ff5be-1468">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="ff5be-1469">Åtgärdade Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="ff5be-1469">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="ff5be-1470">Använd rätt tumavtryck från nya certifikat (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="ff5be-1470">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="ff5be-1471">Visa undantag korrekt (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="ff5be-1471">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="ff5be-1472">Åtgärdade Update-AzServiceFabricDurability så att klusterkonfigurationen uppdateras innan Vmss-åtgärden CreateOrUpdate påbörjas.</span><span class="sxs-lookup"><span data-stu-id="ff5be-1472">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="ff5be-1473">0.4.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="ff5be-1473">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="ff5be-1474">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="ff5be-1474">Az.Profile</span></span>
* <span data-ttu-id="ff5be-1475">Åtgärdade problemet med Get-AzSubscription i CloudShell</span><span class="sxs-lookup"><span data-stu-id="ff5be-1475">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="ff5be-1476">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="ff5be-1476">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ff5be-1477">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ff5be-1477">Az.Compute</span></span>
* <span data-ttu-id="ff5be-1478">Nya storlekar lades till i listan över godkända VM-storlekar för vilka accelererat nätverk kommer att aktiveras vid användning av den enkla parameteruppsättningen för New-AzVm</span><span class="sxs-lookup"><span data-stu-id="ff5be-1478">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="ff5be-1479">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="ff5be-1479">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ff5be-1480">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ff5be-1480">Az.DataLakeStore</span></span>
* <span data-ttu-id="ff5be-1481">Lägger till stöd för regler för virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="ff5be-1481">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="ff5be-1482">Get-AzDataLakeStoreVirtualNetworkRule: Hämtar eller listar regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ff5be-1482">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="ff5be-1483">Add-AzDataLakeStoreVirtualNetworkRule: Lägger till en regel för virtuellt nätverk i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="ff5be-1483">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="ff5be-1484">Set-AzDataLakeStoreVirtualNetworkRule: Ändrar den angivna regeln för virtuellt nätverk i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="ff5be-1484">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="ff5be-1485">Remove-AzDataLakeStoreVirtualNetworkRule: Tar bort en regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ff5be-1485">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ff5be-1486">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ff5be-1486">Az.Network</span></span>
* <span data-ttu-id="ff5be-1487">Skicka protokollvärdet till serverdelen för att uppdatera cmdleten Test-AzNetworkWatcherConnectivity.</span><span class="sxs-lookup"><span data-stu-id="ff5be-1487">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="ff5be-1488">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="ff5be-1488">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="ff5be-1489">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ff5be-1489">Az.Resources</span></span>
* <span data-ttu-id="ff5be-1490">Åtgärdade problem där Get-AzRoleDefinition genererar ett oläsligt undantag (när standardprofilen inte innehåller någon prenumeration och ingen omfattning har angetts) genom att lägga till ett beskrivande undantag i scenariot.</span><span class="sxs-lookup"><span data-stu-id="ff5be-1490">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="ff5be-1491">Ställ in ”RoleDefinitionNameParameterSet” som standardparameteruppsättning.</span><span class="sxs-lookup"><span data-stu-id="ff5be-1491">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="ff5be-1492">0.3.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="ff5be-1492">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="ff5be-1493">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="ff5be-1493">Azure.Storage</span></span>
* <span data-ttu-id="ff5be-1494">Åtgärda fel där Kopiera blob/fil inte kopierar metadata när målplatsen har ett problem med metadata</span><span class="sxs-lookup"><span data-stu-id="ff5be-1494">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="ff5be-1495">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="ff5be-1495">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="ff5be-1496">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="ff5be-1496">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="ff5be-1497">Stöd för att hämta användningsinformation om en Storage-resurs för en specifik plats och för att lägga till ett varningsmeddelande för att hämta användningsinformation om en global Storage-resurs är inaktuellt.</span><span class="sxs-lookup"><span data-stu-id="ff5be-1497">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="ff5be-1498">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="ff5be-1498">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="ff5be-1499">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ff5be-1499">Az.CognitiveServices</span></span>
* <span data-ttu-id="ff5be-1500">Stöd för Get-AzCognitiveServicesAccountSkus utan ett befintligt konto.</span><span class="sxs-lookup"><span data-stu-id="ff5be-1500">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ff5be-1501">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ff5be-1501">Az.Compute</span></span>
* <span data-ttu-id="ff5be-1502">Åtgärdade fel där Get-AzVM -ResourceGroupName <rg> returnerar fler än 50 resultat om det behövs</span><span class="sxs-lookup"><span data-stu-id="ff5be-1502">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="ff5be-1503">Lade till ett exempel för SimpleParameterSet i hjälpen för cmdleten New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="ff5be-1503">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="ff5be-1504">Ett stavfel i förloppsmeddelandet för Azure Disk Encryption har korrigerats</span><span class="sxs-lookup"><span data-stu-id="ff5be-1504">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="ff5be-1505">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="ff5be-1505">Az.DataFactoryV2</span></span>
* <span data-ttu-id="ff5be-1506">ADF .Net SDK-versionen har uppdaterats till 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="ff5be-1506">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ff5be-1507">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ff5be-1507">Az.Network</span></span>
* <span data-ttu-id="ff5be-1508">Funktionalitet för NetworkProfile har lagts till.</span><span class="sxs-lookup"><span data-stu-id="ff5be-1508">Added NetworkProfile functionality.</span></span> <span data-ttu-id="ff5be-1509">nya cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="ff5be-1509">new cmdlets added</span></span>
    - <span data-ttu-id="ff5be-1510">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ff5be-1510">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="ff5be-1511">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ff5be-1511">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="ff5be-1512">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ff5be-1512">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="ff5be-1513">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ff5be-1513">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="ff5be-1514">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="ff5be-1514">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="ff5be-1515">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="ff5be-1515">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="ff5be-1516">Länk för tjänstassociering på modell för undernät har lagts till</span><span class="sxs-lookup"><span data-stu-id="ff5be-1516">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="ff5be-1517">Cmdletarna New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap och Remove-AzVirtualNetworkTap har lagts till</span><span class="sxs-lookup"><span data-stu-id="ff5be-1517">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="ff5be-1518">Cmdletarna Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig och Remove-AzNEtworkInterfaceTapConfig har lagts till</span><span class="sxs-lookup"><span data-stu-id="ff5be-1518">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="ff5be-1519">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="ff5be-1519">Az.RedisCache</span></span>
* <span data-ttu-id="ff5be-1520">Tillåt att alla strängar används som storleksparametrar framöver.</span><span class="sxs-lookup"><span data-stu-id="ff5be-1520">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="ff5be-1521">Lägg till P5 i popup-fönstret PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="ff5be-1521">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="ff5be-1522">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ff5be-1522">Az.Resources</span></span>
* <span data-ttu-id="ff5be-1523">Parametern -Mode som saknades i Set-AzPolicyDefinition har lagts till</span><span class="sxs-lookup"><span data-stu-id="ff5be-1523">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="ff5be-1524">Åtgärdade buggen för cmdleten Get-AzProviderOperation för åtgärder med ursprung som innehåller användare</span><span class="sxs-lookup"><span data-stu-id="ff5be-1524">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="ff5be-1525">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ff5be-1525">Az.Sql</span></span>
* <span data-ttu-id="ff5be-1526">Ett problem där vissa cmdletar för säkerhetskopiering inte kunde identifiera den aktuella azure-prenumerationen har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="ff5be-1526">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ff5be-1527">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ff5be-1527">Az.Websites</span></span>
* <span data-ttu-id="ff5be-1528">Ny cmdlet: Get-AzWebAppContainerContinuousDeploymentUrl – Hämtar webhook-URL:en för kontinuerlig distribution av container</span><span class="sxs-lookup"><span data-stu-id="ff5be-1528">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="ff5be-1529">Nya cmdletar: New-AzWebAppContainerPSSession och Enter-WebAppContainerPSSession – Startar en PowerShell-fjärrsession i en containerapp för windows</span><span class="sxs-lookup"><span data-stu-id="ff5be-1529">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="ff5be-1530">0.2.0 – september 2018</span><span class="sxs-lookup"><span data-stu-id="ff5be-1530">0.2.0 - September 2018</span></span>
 <span data-ttu-id="ff5be-1531">Första versionen</span><span class="sxs-lookup"><span data-stu-id="ff5be-1531">Initial Release</span></span>
