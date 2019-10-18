---
title: Viktig information om Azure PowerShell
description: Lär dig mer om alla de senaste uppdateringarna för Azure PowerShell-modulerna.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/25/2019
ms.openlocfilehash: 24cbfc44c2d23d37b35671f6dad21341cf31874f
ms.sourcegitcommit: 0b94b9566124331d0b15eb7f5a811305c254172e
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/15/2019
ms.locfileid: "72370213"
---
## <a name="280---october-2019"></a><span data-ttu-id="8eec2-103">2.8.0 – oktober 2019</span><span class="sxs-lookup"><span data-stu-id="8eec2-103">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="8eec2-104">Allmänt</span><span class="sxs-lookup"><span data-stu-id="8eec2-104">General</span></span>
* <span data-ttu-id="8eec2-105">AZ. HealthcareApis 1.0.0-version</span><span class="sxs-lookup"><span data-stu-id="8eec2-105">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="8eec2-106">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8eec2-106">Az.Accounts</span></span>
* <span data-ttu-id="8eec2-107">Uppdatera telemetri och URL-omskrivning för genererade moduler, korrigera Windows-enhetstester.</span><span class="sxs-lookup"><span data-stu-id="8eec2-107">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="8eec2-108">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8eec2-108">Az.ApiManagement</span></span>
* <span data-ttu-id="8eec2-109">**Set-AzApiManagementApi** – Tillagt stöd för att uppdatera Api till ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="8eec2-109">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="8eec2-110">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="8eec2-110">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8eec2-111">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8eec2-111">Az.Automation</span></span>
* <span data-ttu-id="8eec2-112">Åtgärdade cmdleten New-AzureAutomationSoftwareUpdateConfiguration för parametern för inställning av Linux-omstart.</span><span class="sxs-lookup"><span data-stu-id="8eec2-112">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span> 

#### <a name="azbatch"></a><span data-ttu-id="8eec2-113">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="8eec2-113">Az.Batch</span></span>
* <span data-ttu-id="8eec2-114">**Get-AzBatchNodeAgentSku** är inaktuell och ersätts av **Get-AzBatchSupportImage** i version 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="8eec2-114">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8eec2-115">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8eec2-115">Az.Compute</span></span>
* <span data-ttu-id="8eec2-116">Lägg till parametrarna Priority, EvictionPolicy och MaxPrice till cmdletarna New-AzVM och New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="8eec2-116">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="8eec2-117">Korrigera varningsmeddelande och hjälpdokument för cmdletarna Add-AzVMAdditionalUnattendContent och Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="8eec2-117">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="8eec2-118">Åtgärda – skipVmBackup-undantag för virtuella Linux-datorer med hanterade diskar för Set-AzVMDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="8eec2-118">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span> 
* <span data-ttu-id="8eec2-119">Åtgärda fel i uppdatera krypteringsinställningarna i set-AzVMDiskEncryptionExtension, scenario i två steg.</span><span class="sxs-lookup"><span data-stu-id="8eec2-119">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8eec2-120">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8eec2-120">Az.DataFactory</span></span>
* <span data-ttu-id="8eec2-121">Lägga till CRUD-kommandon för ADF V2-dataflödet: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow och Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="8eec2-121">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="8eec2-122">Lägger till åtgärdskommandon för ADF V2-dataflödesfelsökningssession: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand och Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="8eec2-122">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="8eec2-123">Uppdatera ADF .Net SDK-versionen till 4.2.0</span><span class="sxs-lookup"><span data-stu-id="8eec2-123">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8eec2-124">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8eec2-124">Az.DataLakeStore</span></span>
* <span data-ttu-id="8eec2-125">Korrigera kontovalidering så att konton med ”-” kan skickas utan domän</span><span class="sxs-lookup"><span data-stu-id="8eec2-125">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="8eec2-126">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="8eec2-126">Az.HealthcareApis</span></span>
* <span data-ttu-id="8eec2-127">PowerShell-versionen har uppdaterats till 1.0.0</span><span class="sxs-lookup"><span data-stu-id="8eec2-127">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="8eec2-128">Uppdaterade SDK-versionen till 1.0.2</span><span class="sxs-lookup"><span data-stu-id="8eec2-128">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="8eec2-129">Uppdatera i tester för att referera till en ny SDK-version</span><span class="sxs-lookup"><span data-stu-id="8eec2-129">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="8eec2-130">Utdatastrukturen har uppdaterats från kapslad till förenklad.</span><span class="sxs-lookup"><span data-stu-id="8eec2-130">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8eec2-131">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8eec2-131">Az.IotHub</span></span>
* <span data-ttu-id="8eec2-132">Lägg till ny routningskälla: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="8eec2-132">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="8eec2-133">Mindre felkorrigering: Get-AzIothub returnerar inte subscriptionId</span><span class="sxs-lookup"><span data-stu-id="8eec2-133">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span> 

#### <a name="azmonitor"></a><span data-ttu-id="8eec2-134">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8eec2-134">Az.Monitor</span></span>
* <span data-ttu-id="8eec2-135">Nya åtgärdsgruppsmottagare har lagts till för åtgärdsgrupp   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="8eec2-135">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="8eec2-136">Använd vanligt aviseringsschema som är aktiverat för mottagarna.</span><span class="sxs-lookup"><span data-stu-id="8eec2-136">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="8eec2-137">Detta gäller inte för SMS, push för Azure-app, ITSM och röstmottagare</span><span class="sxs-lookup"><span data-stu-id="8eec2-137">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="8eec2-138">Webhooks har nu stöd för Azure Active Directory-autentisering.</span><span class="sxs-lookup"><span data-stu-id="8eec2-138">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8eec2-139">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8eec2-139">Az.Network</span></span>
* <span data-ttu-id="8eec2-140">Lägg till ny cmdlet Get-AzAvailableServiceAlias som kan anropas för att hämta de alias som kan användas för tjänstslutpunktsprinciper.</span><span class="sxs-lookup"><span data-stu-id="8eec2-140">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="8eec2-141">Stöd för tillägg av trafikväljare har lagts till i gatewayanslutningar för virtuella nätverk</span><span class="sxs-lookup"><span data-stu-id="8eec2-141">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="8eec2-142">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="8eec2-142">New cmdlets added:</span></span>
        - <span data-ttu-id="8eec2-143">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="8eec2-143">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="8eec2-144">Cmdletar har uppdaterats med valfri parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="8eec2-144">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="8eec2-145">Lägg till stöd för ESP- och AH-protokoll i konfiguration av nätverkssäkerhetsregler</span><span class="sxs-lookup"><span data-stu-id="8eec2-145">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="8eec2-146">Uppdaterade cmdletar:</span><span class="sxs-lookup"><span data-stu-id="8eec2-146">Updated cmdlets:</span></span>
        - <span data-ttu-id="8eec2-147">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8eec2-147">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="8eec2-148">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8eec2-148">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="8eec2-149">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8eec2-149">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="8eec2-150">Förbättra hanteringen av undantag i Cortex-cmdletar</span><span class="sxs-lookup"><span data-stu-id="8eec2-150">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="8eec2-151">Nya generationer och SKU:er för VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="8eec2-151">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="8eec2-152">Introducera nya generationer för VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="8eec2-152">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="8eec2-153">Introducera nya SKU:er med högt dataflöde för VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="8eec2-153">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="8eec2-154">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="8eec2-154">Az.RedisCache</span></span>
* <span data-ttu-id="8eec2-155">Uppdaterad referensdokumentation för ”set-AzRedisCache” för att inkludera saknade värden för parametern ”size”</span><span class="sxs-lookup"><span data-stu-id="8eec2-155">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="8eec2-156">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8eec2-156">Az.Sql</span></span>
* <span data-ttu-id="8eec2-157">Lägg till stöd för inställningen Active Directory administratör på den hanterade instansen</span><span class="sxs-lookup"><span data-stu-id="8eec2-157">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8eec2-158">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8eec2-158">Az.Storage</span></span>
* <span data-ttu-id="8eec2-159">Uppdatera Lagringsklientbibliotek till 11.1.0</span><span class="sxs-lookup"><span data-stu-id="8eec2-159">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="8eec2-160">Lista containrar med hanteringsplans-API, kommer att listas med NextPageLink</span><span class="sxs-lookup"><span data-stu-id="8eec2-160">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="8eec2-161">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="8eec2-161">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="8eec2-162">Lista lagringskonton från prenumerationen, kommer att listas med NextPageLink</span><span class="sxs-lookup"><span data-stu-id="8eec2-162">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="8eec2-163">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8eec2-163">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="8eec2-164">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="8eec2-164">Az.StorageSync</span></span>
* <span data-ttu-id="8eec2-165">Åtgärda problemet 9810 i Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="8eec2-165">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8eec2-166">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8eec2-166">Az.Websites</span></span>
* <span data-ttu-id="8eec2-167">Set-AzWebApp – uppdatering av ASP för en app misslyckades</span><span class="sxs-lookup"><span data-stu-id="8eec2-167">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="8eec2-168">2.7.0 – september 2019</span><span class="sxs-lookup"><span data-stu-id="8eec2-168">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="8eec2-169">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8eec2-169">Az.ApiManagement</span></span>
* <span data-ttu-id="8eec2-170">Uppdatera ”-Format”-parameterbeskrivningen i ”Set-AzApiManagementPolicy”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="8eec2-170">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="8eec2-171">Referenser för den föråldrade cmdleten ”Update-AzApiManagementDeployment” har tagits bort från referensdokumentationen.</span><span class="sxs-lookup"><span data-stu-id="8eec2-171">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="8eec2-172">Använd ”Set-AzApiManagement” i stället.</span><span class="sxs-lookup"><span data-stu-id="8eec2-172">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8eec2-173">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8eec2-173">Az.Automation</span></span>
* <span data-ttu-id="8eec2-174">Stavfel har korrigerats i exempel i referensdokumentationen för ”Register-AzAutomationDscNode”</span><span class="sxs-lookup"><span data-stu-id="8eec2-174">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="8eec2-175">Klargörande har lagts till om OS-begränsningar för Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="8eec2-175">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="8eec2-176">Null-referensundantag har korrigerats för -Wait-alternativet i Start-AzAutomationRunbook-cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8eec2-176">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8eec2-177">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8eec2-177">Az.Compute</span></span>
* <span data-ttu-id="8eec2-178">Lägg till UploadSizeInBytes-parameter till New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="8eec2-178">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="8eec2-179">Lägg till Incremental-parameter till New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="8eec2-179">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="8eec2-180">Lägg till en funktion för virtuella datorer med låg prioritet:</span><span class="sxs-lookup"><span data-stu-id="8eec2-180">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="8eec2-181">MaxPrice-, EvictionPolicy- och Priority-parametrar har lagts till i New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="8eec2-181">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="8eec2-182">MaxPrice-parametern har lagts till i New-AzVmssConfig-, Update-AzVM- och Update-AzVmss-cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="8eec2-182">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="8eec2-183">Åtgärda problem med VM-referenser för Get-AzAvailabilitySet-cmdleten när alla tillgänglighetsuppsättningar i prenumerationen visas.</span><span class="sxs-lookup"><span data-stu-id="8eec2-183">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="8eec2-184">Korrigera null-undantaget för Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="8eec2-184">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="8eec2-185">Korrigera VHD-metoden för sökning relativt till slut.</span><span class="sxs-lookup"><span data-stu-id="8eec2-185">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="8eec2-186">Åtgärda UltraSSD-problem för New-AzVM och Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="8eec2-186">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8eec2-187">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8eec2-187">Az.DataFactory</span></span>
* <span data-ttu-id="8eec2-188">Lägger till 3 nya kommandon för ADF V2 – Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription och Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="8eec2-188">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="8eec2-189">ADF .Net SDK har uppdaterats till 4.1.3</span><span class="sxs-lookup"><span data-stu-id="8eec2-189">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="8eec2-190">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="8eec2-190">Az.HDInsight</span></span>
* <span data-ttu-id="8eec2-191">Anrop för icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="8eec2-191">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8eec2-192">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8eec2-192">Az.IotHub</span></span>
* <span data-ttu-id="8eec2-193">Lägg till stöd för att anropa redundans för en IotHub till den geo-länkade katastrofåterställningsregionen.</span><span class="sxs-lookup"><span data-stu-id="8eec2-193">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="8eec2-194">Lägg till stöd för att hantera meddelandeberikning för en IotHub.</span><span class="sxs-lookup"><span data-stu-id="8eec2-194">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="8eec2-195">Nya cmdlet:ar är:</span><span class="sxs-lookup"><span data-stu-id="8eec2-195">New cmdlets are:</span></span>
    - <span data-ttu-id="8eec2-196">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="8eec2-196">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="8eec2-197">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="8eec2-197">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="8eec2-198">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="8eec2-198">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="8eec2-199">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="8eec2-199">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8eec2-200">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8eec2-200">Az.Monitor</span></span>
* <span data-ttu-id="8eec2-201">Pekar på den senaste Monitor SDK:n, dvs. 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="8eec2-201">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="8eec2-202">Lägger till bakåtkompatibla ändringar i Metrics-cmdletarna, dvs. enhetsuppräkningen stöder flera nya värden.</span><span class="sxs-lookup"><span data-stu-id="8eec2-202">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="8eec2-203">Detta är skrivskyddade cmdletar, så det förekommer inga ändringar i inmatningen för cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="8eec2-203">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="8eec2-204">API-versionen för **ActionGroups**-begäranden är nu **2019-06-01**. Tidigare var den **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="8eec2-204">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="8eec2-205">Test av scenarier har uppdaterats för att anpassas till den här ändringen.</span><span class="sxs-lookup"><span data-stu-id="8eec2-205">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="8eec2-206">Ett nytt obligatoriskt argument har lagts till för konstruktorerna för klasserna **EmailReceiver** och **WebhookReceiver** – ett booleskt värde med namnet **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="8eec2-206">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="8eec2-207">Värdet är för närvarande fast till **false** så att den här icke-bakåtkompatibla ändringen är dold från cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="8eec2-207">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="8eec2-208">**Obs!** Det här är en tillfällig ändring som måste verifieras av Alerts-teamet.</span><span class="sxs-lookup"><span data-stu-id="8eec2-208">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="8eec2-209">Ordningen på argumenten för konstruktorn för klassen **Source** (relaterad till klassen **ScheduledQueryRuleSource**) har ändrats från den tidigare SDK:n.</span><span class="sxs-lookup"><span data-stu-id="8eec2-209">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="8eec2-210">Den här ändringen krävde korrigering av två enhetstest: de kompilerades, men testerna skickades inte.</span><span class="sxs-lookup"><span data-stu-id="8eec2-210">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="8eec2-211">Ordningen på argumenten för konstruktorn för klassen **AlertingAction** (relaterad till klassen **ScheduledQueryRuleSource**) har ändrats från den tidigare SDK:n.</span><span class="sxs-lookup"><span data-stu-id="8eec2-211">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="8eec2-212">Den här ändringen krävde korrigering av två enhetstest: de kompilerades, men testerna skickades inte.</span><span class="sxs-lookup"><span data-stu-id="8eec2-212">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="8eec2-213">Stöd för kriterier för dynamiskt tröskelvärde för måttavisering v2</span><span class="sxs-lookup"><span data-stu-id="8eec2-213">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="8eec2-214">New-AzMetricAlertRuleV2Criteria: skapar nu även kriterier för dynamiskt tröskelvärde</span><span class="sxs-lookup"><span data-stu-id="8eec2-214">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="8eec2-215">Add-AzMetricAlertRuleV2: accepterar nu även kriterier för dynamiskt tröskelvärde</span><span class="sxs-lookup"><span data-stu-id="8eec2-215">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="8eec2-216">Förbättringar i schemalagd frågeregel (SQR)</span><span class="sxs-lookup"><span data-stu-id="8eec2-216">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="8eec2-217">Cmdletar accepterar ”Location”-parameter i båda formaten, antingen platsen (t.ex. eastus) eller platsens visningsnamn (t.ex. USA, östra)</span><span class="sxs-lookup"><span data-stu-id="8eec2-217">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="8eec2-218">”Enabled”-parametern illustreras korrekt i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="8eec2-218">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="8eec2-219">Exempel för den valfria parametern ”ActionGroup” har lagts till</span><span class="sxs-lookup"><span data-stu-id="8eec2-219">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="8eec2-220">Förbättrade hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="8eec2-220">Overall improved help files</span></span>
* <span data-ttu-id="8eec2-221">Åtgärda bugg då omfattningstypen fastställs för ”Set-AzActionRule”</span><span class="sxs-lookup"><span data-stu-id="8eec2-221">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8eec2-222">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8eec2-222">Az.Network</span></span>
* <span data-ttu-id="8eec2-223">Korrigera felaktigt exempel i referensdokumentationen för ”New-AzApplicationGateway”</span><span class="sxs-lookup"><span data-stu-id="8eec2-223">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="8eec2-224">Lägg till anmärkning i ”Get-AzNetworkWatcherPacketCapture”-referensdokumentationen om hämtning av alla egenskaper för en paketinsamling</span><span class="sxs-lookup"><span data-stu-id="8eec2-224">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="8eec2-225">Exempel har korrigerats i ”Test-AzNetworkWatcherIPFlow”-referensdokumentationen för korrekt uppräkning av nätverkskort</span><span class="sxs-lookup"><span data-stu-id="8eec2-225">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="8eec2-226">Förbättrad tolkning av molnundantag för att visa eventuell ytterligare information</span><span class="sxs-lookup"><span data-stu-id="8eec2-226">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="8eec2-227">Förbättrad tolkning av molnundantag för att hantera ytterligare en typ av SDK-undantag</span><span class="sxs-lookup"><span data-stu-id="8eec2-227">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="8eec2-228">Felaktig mappning av säkerhetsregelmodeller har korrigerats</span><span class="sxs-lookup"><span data-stu-id="8eec2-228">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="8eec2-229">Egenskaper har lagts till för nätverksgränssnittet för funktionen Privat IP</span><span class="sxs-lookup"><span data-stu-id="8eec2-229">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="8eec2-230">Egenskapen ”PrivateEndpoint” har lagts till som en typ av PSResourceId till PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="8eec2-230">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="8eec2-231">Egenskapen ”PrivateLinkConnectionProperties” har lagts till som en typ av PSIpConfigurationConnectivityInformation till PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="8eec2-231">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="8eec2-232">Modellklassen PSIpConfigurationConnectivityInformation har lagts till</span><span class="sxs-lookup"><span data-stu-id="8eec2-232">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="8eec2-233">ApplicationRuleProtocolType ”mssql” har lagts till för Azure Firewall-resurs</span><span class="sxs-lookup"><span data-stu-id="8eec2-233">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="8eec2-234">MultiLink-stöd i virtuellt WAN</span><span class="sxs-lookup"><span data-stu-id="8eec2-234">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="8eec2-235">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="8eec2-235">New cmdlets</span></span>
        - <span data-ttu-id="8eec2-236">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="8eec2-236">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="8eec2-237">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="8eec2-237">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="8eec2-238">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="8eec2-238">Updated cmdlet:</span></span>
        - <span data-ttu-id="8eec2-239">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="8eec2-239">New-VpnSite</span></span>
        - <span data-ttu-id="8eec2-240">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="8eec2-240">Update-VpnSite</span></span>
        - <span data-ttu-id="8eec2-241">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="8eec2-241">New-VpnConnection</span></span>
        - <span data-ttu-id="8eec2-242">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="8eec2-242">Update-VpnConnection</span></span>
* <span data-ttu-id="8eec2-243">Dokument för vissa PowerShell-exempel har korrigerats så att Az-cmdletar används i stället för AzureRM-cmdletar</span><span class="sxs-lookup"><span data-stu-id="8eec2-243">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8eec2-244">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8eec2-244">Az.RecoveryServices</span></span>
* <span data-ttu-id="8eec2-245">Uppdatera AzureVMpolicy-objekt med ProtectedItemsCount-attribut</span><span class="sxs-lookup"><span data-stu-id="8eec2-245">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="8eec2-246">Ytterligare tester har lagts till för VM-princip och återställning av ursprungligt lagringskonto</span><span class="sxs-lookup"><span data-stu-id="8eec2-246">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="8eec2-247">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8eec2-247">Az.Resources</span></span>
* <span data-ttu-id="8eec2-248">Åtgärda fel där det inte gick att anropa New-AzRoleAssignment utan parametern Scope.</span><span class="sxs-lookup"><span data-stu-id="8eec2-248">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="8eec2-249">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8eec2-249">Az.ServiceFabric</span></span>
* <span data-ttu-id="8eec2-250">Stavfel har korrigerats i exempel för ”Update-AzServiceFabricReliability”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="8eec2-250">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="8eec2-251">Lägger till nya cmdletar för att hantera program och tjänster:</span><span class="sxs-lookup"><span data-stu-id="8eec2-251">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="8eec2-252">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="8eec2-252">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="8eec2-253">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="8eec2-253">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="8eec2-254">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="8eec2-254">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="8eec2-255">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="8eec2-255">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="8eec2-256">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="8eec2-256">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="8eec2-257">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="8eec2-257">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="8eec2-258">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="8eec2-258">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="8eec2-259">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="8eec2-259">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="8eec2-260">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="8eec2-260">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="8eec2-261">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="8eec2-261">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="8eec2-262">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="8eec2-262">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="8eec2-263">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="8eec2-263">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="8eec2-264">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="8eec2-264">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="8eec2-265">Service Fabric SDK har uppgraderats till version 1.2.0 som använder Service Fabric-resursprovidern med API-version 2019-03-01.</span><span class="sxs-lookup"><span data-stu-id="8eec2-265">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="8eec2-266">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="8eec2-266">Az.SignalR</span></span>
* <span data-ttu-id="8eec2-267">Lägg till Update-, Restart-, CheckNameAvailability- och GetUsage-cmdletar</span><span class="sxs-lookup"><span data-stu-id="8eec2-267">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="8eec2-268">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8eec2-268">Az.Sql</span></span>
* <span data-ttu-id="8eec2-269">Uppdatera exempel i referensdokumentationen för ”Get-AzSqlElasticPool”</span><span class="sxs-lookup"><span data-stu-id="8eec2-269">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="8eec2-270">vCore-exempel för att skapa en elastisk pool (New-AzSqlElasticPool) har lagts till.</span><span class="sxs-lookup"><span data-stu-id="8eec2-270">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="8eec2-271">Ta bort verifieringen av EmailAddresses och kontrollen som bekräftar att EmailAdmins inte är falskt när EmailAddresses är tomt i Set-AzSqlServerAdvancedThreatProtectionPolicy och Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="8eec2-271">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="8eec2-272">Server-/databasgranskningsinställningar kan tas bort när det finns flera diagnostikinställningar som aktiverar granskningskategorin.</span><span class="sxs-lookup"><span data-stu-id="8eec2-272">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="8eec2-273">Åtgärda verifiering av e-postadresser i flera Sql Vulnerability Assessment-cmdletar (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting och Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="8eec2-273">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8eec2-274">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8eec2-274">Az.Storage</span></span>
* <span data-ttu-id="8eec2-275">Exempel i referensdokumentationen för ”Get-AzStorageAccountKey” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="8eec2-275">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="8eec2-276">Vid upp- och nedladdning av en Azure-fil kan SMB-egenskaperna för källfilen (t.ex. filattribut, tidpunkten då filen skapades och tidpunkten för den senaste skrivningen) sparas i målfilen</span><span class="sxs-lookup"><span data-stu-id="8eec2-276">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="8eec2-277">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="8eec2-277">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="8eec2-278">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="8eec2-278">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="8eec2-279">Korrigera problem med uppladdningen av blockblob med egenskaper/metadata för ImmutabilityPolicy i containrar.</span><span class="sxs-lookup"><span data-stu-id="8eec2-279">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="8eec2-280">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="8eec2-280">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="8eec2-281">Stöd för hantering av Azure-filresurser med API för hanteringsplan</span><span class="sxs-lookup"><span data-stu-id="8eec2-281">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="8eec2-282">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="8eec2-282">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="8eec2-283">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="8eec2-283">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="8eec2-284">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="8eec2-284">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="8eec2-285">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="8eec2-285">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8eec2-286">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8eec2-286">Az.Websites</span></span>
* <span data-ttu-id="8eec2-287">Åtgärdar problemet där webapp-taggar togs bort när appen migrerades till nya ASP</span><span class="sxs-lookup"><span data-stu-id="8eec2-287">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="8eec2-288">Åtgärda Publish-AzureWebapp så att det fungerar i Linux och Windows</span><span class="sxs-lookup"><span data-stu-id="8eec2-288">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="8eec2-289">Uppdatera exempel i ”Get-AzWebAppPublishingProfile”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="8eec2-289">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="8eec2-290">2.6.0 – augusti 2019</span><span class="sxs-lookup"><span data-stu-id="8eec2-290">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="8eec2-291">Allmänt</span><span class="sxs-lookup"><span data-stu-id="8eec2-291">General</span></span>
* <span data-ttu-id="8eec2-292">Åtgärdade diverse skrivfel i flera moduler</span><span class="sxs-lookup"><span data-stu-id="8eec2-292">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="8eec2-293">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8eec2-293">Az.Accounts</span></span>
* <span data-ttu-id="8eec2-294">Stöd för användartilldelat MSI i Azure Functions-autentisering (#9479)</span><span class="sxs-lookup"><span data-stu-id="8eec2-294">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="8eec2-295">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="8eec2-295">Az.Aks</span></span>
* <span data-ttu-id="8eec2-296">Åtgärda problem med utdata för "Get-AzAks"</span><span class="sxs-lookup"><span data-stu-id="8eec2-296">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="8eec2-297">Mer information här: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="8eec2-297">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="8eec2-298">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8eec2-298">Az.ApiManagement</span></span>
* <span data-ttu-id="8eec2-299">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="8eec2-299">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="8eec2-300">Uppdatera .net-NuGet-versionen, som inte tillämpar begränsningar för productId, apiId och userId</span><span class="sxs-lookup"><span data-stu-id="8eec2-300">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="8eec2-301">**Get-AzApiManagementProduct** – Lade till stöd för frågekörning mot produkter via API.</span><span class="sxs-lookup"><span data-stu-id="8eec2-301">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="8eec2-302">**New-AzApiManagementApiRevision** – Korrigering för problem där ApiRevisionDescription inte angavs vid skapande av ny API-revision https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="8eec2-302">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="8eec2-303">Åtgärdade skrivfel i modellen "PsApiManagementOAuth2AuthrozationServer" till "PsApiManagementOAuth2AuthorizationServer"</span><span class="sxs-lookup"><span data-stu-id="8eec2-303">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="8eec2-304">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="8eec2-304">Az.Batch</span></span>
* <span data-ttu-id="8eec2-305">Åtgärdade skrivfel i hjälpmeddelande och dokumentation till att skriva Windows med versaler</span><span class="sxs-lookup"><span data-stu-id="8eec2-305">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="8eec2-306">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="8eec2-306">Az.Cdn</span></span>
* <span data-ttu-id="8eec2-307">Åtgärdade skrivfel i CDN-modulens konverteringshjälp</span><span class="sxs-lookup"><span data-stu-id="8eec2-307">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8eec2-308">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8eec2-308">Az.Compute</span></span>
* <span data-ttu-id="8eec2-309">Lägg till VmssId i New-AzVMConfig-cmdleten</span><span class="sxs-lookup"><span data-stu-id="8eec2-309">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="8eec2-310">Lägg till parametrarna TerminateScheduledEvents och TerminateScheduledEventNotBeforeTimeoutInMinutes i New-AzVmssConfig och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="8eec2-310">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="8eec2-311">Lägg till egenskapen HyperVGeneration till avbildningsobjekt för virtuell dator</span><span class="sxs-lookup"><span data-stu-id="8eec2-311">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="8eec2-312">Lägg till funktioner för Host och HostGroup</span><span class="sxs-lookup"><span data-stu-id="8eec2-312">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="8eec2-313">Nya cmdletar:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="8eec2-313">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="8eec2-314">HostId-parametern läggs till i New-AzVMConfig och New-AzVM</span><span class="sxs-lookup"><span data-stu-id="8eec2-314">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="8eec2-315">Uppdatera exempel i "Invoke-AzVMRunCommand"-dokumentationen till att använda rätt parameternamn</span><span class="sxs-lookup"><span data-stu-id="8eec2-315">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="8eec2-316">Uppdatera "-VolumeType"-beskrivningen i referensdokumentationen för "set-AzVMDiskEncryptionExtension" och "set-AzVmssDiskEncryptionExtension"</span><span class="sxs-lookup"><span data-stu-id="8eec2-316">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8eec2-317">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8eec2-317">Az.DataFactory</span></span>
* <span data-ttu-id="8eec2-318">Åtgärda skrivfel till att använda versaler för "Windows" i "New-AzDataFactoryEncryptValue"-dokumentationen</span><span class="sxs-lookup"><span data-stu-id="8eec2-318">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="8eec2-319">Uppdaterade ADF .Net SDK-versionen till 4.1.2</span><span class="sxs-lookup"><span data-stu-id="8eec2-319">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="8eec2-320">Lägg till parametrarna "DataProxyIntegrationRuntimeName", "DataProxyStagingLinkedServiceName" och "DataProxyStagingPath" för "Set-AzureRmDataFactoryV2IntegrationRuntime"-cmd för att aktivera konfiguration av lokalt installerad integrationskörning som en proxy för SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="8eec2-320">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="8eec2-321">Uppdaterade PSTriggerRun till att visa utlöst pipeline, meddelande och egenskaper samt PSActivityRun till att visa aktivitetstypen</span><span class="sxs-lookup"><span data-stu-id="8eec2-321">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8eec2-322">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8eec2-322">Az.DataLakeStore</span></span>
* <span data-ttu-id="8eec2-323">Korrigering av frysning av Get-DataLakeStoreDeletedItem för fel eller fjärrundantag.</span><span class="sxs-lookup"><span data-stu-id="8eec2-323">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="8eec2-324">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="8eec2-324">Az.EventHub</span></span>
* <span data-ttu-id="8eec2-325">Korrigering av problem #9658 : Skrivfel i parametern VirtualNteworkRule i Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="8eec2-325">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="8eec2-326">Korrigering av problem #9558 : Set-AzEventHubNamespace använder PATCH i stället för PUT</span><span class="sxs-lookup"><span data-stu-id="8eec2-326">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="8eec2-327">lade till parametern EnableKafka i Set-AzEventHubNamespace-cmdleten</span><span class="sxs-lookup"><span data-stu-id="8eec2-327">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="8eec2-328">Korrigering av problem #9786 : kan inte skapa en regel med Endast lyssna-behörighet</span><span class="sxs-lookup"><span data-stu-id="8eec2-328">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="8eec2-329">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="8eec2-329">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="8eec2-330">Åtgärdade skrivfel i dokumentation där "Azure" skrevs helt med gemener</span><span class="sxs-lookup"><span data-stu-id="8eec2-330">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8eec2-331">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8eec2-331">Az.Monitor</span></span>
* <span data-ttu-id="8eec2-332">Åtgärdade felaktigt parameternamn i hjälpdokumentationen</span><span class="sxs-lookup"><span data-stu-id="8eec2-332">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8eec2-333">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8eec2-333">Az.Network</span></span>
* <span data-ttu-id="8eec2-334">Uppdaterade New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="8eec2-334">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="8eec2-335">Gjorde parametern "PublicIpAddress" inaktuell eftersom den aldrig används på serversidan.</span><span class="sxs-lookup"><span data-stu-id="8eec2-335">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="8eec2-336">Lade till den valfria parametern "Primary", som anger huruvida den aktuella IP-konfigurationen är den primära.</span><span class="sxs-lookup"><span data-stu-id="8eec2-336">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="8eec2-337">Förbättrade hanteringen av felundantag för begärande från SDK – åtgärdar problemet att tidigare SDK-undantag inte hanteras på rätt sätt, vilket leder till att viktig felinformation inte visas</span><span class="sxs-lookup"><span data-stu-id="8eec2-337">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="8eec2-338">Justerade valideringslogiken för IPv6-IP-prefix till att kontrollera korrekt IPv6-prefixlängd.</span><span class="sxs-lookup"><span data-stu-id="8eec2-338">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="8eec2-339">Uppdaterade Get-AzVirtualNetworkSubnetConfig: Lade till parameter som anges till get av undernätets resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="8eec2-339">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="8eec2-340">Uppdaterade beskrivningen av parametern Location för AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="8eec2-340">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="8eec2-341">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8eec2-341">Az.OperationalInsights</span></span>
* <span data-ttu-id="8eec2-342">Uppdaterade dokumentation för "New-AzOperationalInsightsLinuxSyslogDataSource"</span><span class="sxs-lookup"><span data-stu-id="8eec2-342">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="8eec2-343">Lade till exempel</span><span class="sxs-lookup"><span data-stu-id="8eec2-343">Added example</span></span>
    - <span data-ttu-id="8eec2-344">Uppdaterade beskrivningen av parametern "-Name"</span><span class="sxs-lookup"><span data-stu-id="8eec2-344">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="8eec2-345">Lade till ett exempel för New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="8eec2-345">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="8eec2-346">Ändrade beskrivningen av parametern -Name för New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="8eec2-346">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8eec2-347">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8eec2-347">Az.RecoveryServices</span></span>
* <span data-ttu-id="8eec2-348">Uppdatera "Get-AzRecoveryServicesBackupJobDetail.md"</span><span class="sxs-lookup"><span data-stu-id="8eec2-348">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="8eec2-349">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8eec2-349">Az.Resources</span></span>
* <span data-ttu-id="8eec2-350">Lägg till stöd för den nya API-versionen från 2019-05-10 för Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="8eec2-350">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="8eec2-351">Lägg till stöd för "copy.count = 0" för variabler, resurser och egenskaper</span><span class="sxs-lookup"><span data-stu-id="8eec2-351">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="8eec2-352">Resurser med "condition = false" eller "copy.count = 0" tas bort i complete-läget</span><span class="sxs-lookup"><span data-stu-id="8eec2-352">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="8eec2-353">Lägg till ett exempel på tilldelning av princip på prenumerationsnivå i hjälpdokumentationen</span><span class="sxs-lookup"><span data-stu-id="8eec2-353">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="8eec2-354">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8eec2-354">Az.ServiceBus</span></span>
* <span data-ttu-id="8eec2-355">Korrigering av problem #9658 : Skrivfel i parametern VirtualNetworkRule i set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="8eec2-355">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="8eec2-356">Korrigering av problem #9786 : kan inte skapa en regel med Endast lyssna-behörighet</span><span class="sxs-lookup"><span data-stu-id="8eec2-356">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="8eec2-357">Lade till det nya kommandot "Test-AzServiceBusNameAvailability" för att kontrollera namntillgängligheten för kö och ämne</span><span class="sxs-lookup"><span data-stu-id="8eec2-357">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="8eec2-358">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8eec2-358">Az.ServiceFabric</span></span>
* <span data-ttu-id="8eec2-359">Åtgärda buggar med tillägg av nodtyps-cmdlet:</span><span class="sxs-lookup"><span data-stu-id="8eec2-359">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="8eec2-360">NullReferenceException-bugg när resursgrupp hade annan vmss som inte är relaterad till Service Fabric-klustret.</span><span class="sxs-lookup"><span data-stu-id="8eec2-360">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="8eec2-361">Åtgärdar problemet: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="8eec2-361">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="8eec2-362">Åtgärda bugg där cmdleten misslyckades om virtualNetwork var i en annan resursgrupp än klustret.</span><span class="sxs-lookup"><span data-stu-id="8eec2-362">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="8eec2-363">Åtgärdar problemet: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="8eec2-363">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="8eec2-364">AzServiceFabricApplicationCertificate-cmdleten görs inaktuell</span><span class="sxs-lookup"><span data-stu-id="8eec2-364">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="8eec2-365">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8eec2-365">Az.Sql</span></span>
* <span data-ttu-id="8eec2-366">Uppdatera dokumentation om gamla gransknings-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="8eec2-366">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8eec2-367">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8eec2-367">Az.Storage</span></span>
* <span data-ttu-id="8eec2-368">Uppdatera hjälpen för Get/Close-AzStorageFileHandle genom att lägga till fler scenarier i cmdlet-exempel och uppdatera parameterbeskrivningar</span><span class="sxs-lookup"><span data-stu-id="8eec2-368">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="8eec2-369">Stöd för StandardBlobTier i uppladdningsblob och kopieringsblob</span><span class="sxs-lookup"><span data-stu-id="8eec2-369">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="8eec2-370">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="8eec2-370">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="8eec2-371">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="8eec2-371">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="8eec2-372">Stöd för rehydratiseringsprioritet i kopieringsblob</span><span class="sxs-lookup"><span data-stu-id="8eec2-372">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="8eec2-373">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="8eec2-373">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8eec2-374">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8eec2-374">Az.Websites</span></span>
* <span data-ttu-id="8eec2-375">Lägg till klargöranden gällande parametern -AppSettings i Set-AzWebApp och Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8eec2-375">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="8eec2-376">2.5.0 – July 2019</span><span class="sxs-lookup"><span data-stu-id="8eec2-376">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8eec2-377">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8eec2-377">Az.Accounts</span></span>
* <span data-ttu-id="8eec2-378">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="8eec2-378">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="8eec2-379">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="8eec2-379">Az.ApplicationInsights</span></span>
* <span data-ttu-id="8eec2-380">Korrigera skrivfel i exempel i dokumentationen för Remove-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="8eec2-380">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="8eec2-381">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8eec2-381">Az.Automation</span></span>
* <span data-ttu-id="8eec2-382">Korrigera skrivfel i resurssträng</span><span class="sxs-lookup"><span data-stu-id="8eec2-382">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="8eec2-383">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8eec2-383">Az.CognitiveServices</span></span>
* <span data-ttu-id="8eec2-384">Stöd för NetworkRuleSet har lagts till.</span><span class="sxs-lookup"><span data-stu-id="8eec2-384">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8eec2-385">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8eec2-385">Az.Compute</span></span>
* <span data-ttu-id="8eec2-386">Lägg till saknade egenskaper (ComputerName, OsName, OsVersion och HyperVGeneration) för visningsobjekt i den virtuella datorinstansen.</span><span class="sxs-lookup"><span data-stu-id="8eec2-386">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="8eec2-387">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="8eec2-387">Az.ContainerRegistry</span></span>
* <span data-ttu-id="8eec2-388">Åtgärda skrivfel i Remove-AzContainerRegistryReplication för parametern Replication</span><span class="sxs-lookup"><span data-stu-id="8eec2-388">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="8eec2-389">Mer information finns här: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="8eec2-389">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8eec2-390">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8eec2-390">Az.DataFactory</span></span>
* <span data-ttu-id="8eec2-391">ADF .Net SDK-versionen har uppdaterats till 4.1.0</span><span class="sxs-lookup"><span data-stu-id="8eec2-391">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="8eec2-392">Korrigera skrivfel i dokumentationen för Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="8eec2-392">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="8eec2-393">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="8eec2-393">Az.EventHub</span></span>
* <span data-ttu-id="8eec2-394">Ny cmmdlet har lagts till för att skapa SAS-token: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="8eec2-394">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="8eec2-395">verifierings- och felmeddelande har lagts till för authorizationrules-rättigheter om endast "hantera" har tilldelats</span><span class="sxs-lookup"><span data-stu-id="8eec2-395">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8eec2-396">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8eec2-396">Az.KeyVault</span></span>
* <span data-ttu-id="8eec2-397">Stöd har lagts till för att ange KeySize för certifikatprinciper</span><span class="sxs-lookup"><span data-stu-id="8eec2-397">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="8eec2-398">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="8eec2-398">Az.LogicApp</span></span>
* <span data-ttu-id="8eec2-399">Korrigering för Get-AzIntegrationAccountMap för att lista alla mappningstyper</span><span class="sxs-lookup"><span data-stu-id="8eec2-399">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="8eec2-400">Ny MapType-parameter har lagts till för filtrering</span><span class="sxs-lookup"><span data-stu-id="8eec2-400">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="8eec2-401">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="8eec2-401">Az.ManagedServices</span></span>
* <span data-ttu-id="8eec2-402">Stöd för API-versionen 2019-06-01 (GA) har lagts till</span><span class="sxs-lookup"><span data-stu-id="8eec2-402">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8eec2-403">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8eec2-403">Az.Network</span></span>
* <span data-ttu-id="8eec2-404">Lägg till stöd för privat slutpunkt och privat länktjänst</span><span class="sxs-lookup"><span data-stu-id="8eec2-404">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="8eec2-405">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="8eec2-405">New cmdlets</span></span>
        - <span data-ttu-id="8eec2-406">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="8eec2-406">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="8eec2-407">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="8eec2-407">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="8eec2-408">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8eec2-408">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="8eec2-409">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8eec2-409">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="8eec2-410">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8eec2-410">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="8eec2-411">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8eec2-411">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="8eec2-412">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="8eec2-412">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="8eec2-413">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="8eec2-413">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="8eec2-414">Nedanstående kommandon för funktionen har uppdaterats: Flaggan PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies på undernätet i VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="8eec2-414">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="8eec2-415">Uppdaterade New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="8eec2-415">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="8eec2-416">Valfri parameter har lagts till – PrivateEndpointNetworkPoliciesFlag som konfigurerar huruvida nätverksprinciper ska tillämpas på en privat slutpunkt i det här undernätet.</span><span class="sxs-lookup"><span data-stu-id="8eec2-416">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="8eec2-417">Valfri parameter har lagts till – PrivateLinkServiceNetworkPoliciesFlag som konfigurerar huruvida nätverksprinciper ska tillämpas på en privat länktjänst i det här undernätet.</span><span class="sxs-lookup"><span data-stu-id="8eec2-417">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="8eec2-418">AzPrivateLinkService för cmdlet-parametern ServiceName har bytt namn till Name med aliaset ServiceName för bakåtkompatibilitet</span><span class="sxs-lookup"><span data-stu-id="8eec2-418">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="8eec2-419">Aktivera ICMP-protokoll för konfiguration av nätverkssäkerhetsregler</span><span class="sxs-lookup"><span data-stu-id="8eec2-419">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="8eec2-420">Uppdaterade cmdletar</span><span class="sxs-lookup"><span data-stu-id="8eec2-420">Updated cmdlets</span></span>
        - <span data-ttu-id="8eec2-421">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8eec2-421">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="8eec2-422">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8eec2-422">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="8eec2-423">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8eec2-423">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="8eec2-424">Lägg till ConnectionProtocolType (Ikev1/Ikev2) som en konfigurerbar parameter för New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="8eec2-424">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="8eec2-425">Lägg till PrivateIpAddressVersion i LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="8eec2-425">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="8eec2-426">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="8eec2-426">Updated cmdlet:</span></span>
        - <span data-ttu-id="8eec2-427">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="8eec2-427">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="8eec2-428">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="8eec2-428">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="8eec2-429">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="8eec2-429">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="8eec2-430">Uppdatering av Application Gateway-kommandot New-AzApplicationGatewayProbeConfig för stöd av anpassad port i Probe</span><span class="sxs-lookup"><span data-stu-id="8eec2-430">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="8eec2-431">Uppdaterade New-AzApplicationGatewayProbeConfig: Den valfria parametern Port som används för avsökning i serverdelen har lagts till.</span><span class="sxs-lookup"><span data-stu-id="8eec2-431">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="8eec2-432">Denna parameter gäller för SKU:erna Standard_V2 och WAF_V2.</span><span class="sxs-lookup"><span data-stu-id="8eec2-432">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="8eec2-433">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8eec2-433">Az.OperationalInsights</span></span>
* <span data-ttu-id="8eec2-434">Uppdaterade standardversionen för sparade sökningar till 1.</span><span class="sxs-lookup"><span data-stu-id="8eec2-434">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="8eec2-435">Åtgärdade hantering av anpassad log null regex</span><span class="sxs-lookup"><span data-stu-id="8eec2-435">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8eec2-436">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8eec2-436">Az.RecoveryServices</span></span>
* <span data-ttu-id="8eec2-437">Uppdatera Get-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="8eec2-437">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="8eec2-438">Uppdatera Get-AzRecoveryServicesBackupContainer.md</span><span class="sxs-lookup"><span data-stu-id="8eec2-438">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="8eec2-439">Uppdatera Get-AzRecoveryServicesVault.md</span><span class="sxs-lookup"><span data-stu-id="8eec2-439">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="8eec2-440">Uppdatera Wait-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="8eec2-440">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="8eec2-441">Uppdatera Set-AzRecoveryServicesVaultContext.md</span><span class="sxs-lookup"><span data-stu-id="8eec2-441">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="8eec2-442">Uppdatera Get-AzRecoveryServicesBackupItem.md</span><span class="sxs-lookup"><span data-stu-id="8eec2-442">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="8eec2-443">Uppdatera Get-AzRecoveryServicesBackupRecoveryPoint.md</span><span class="sxs-lookup"><span data-stu-id="8eec2-443">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="8eec2-444">Uppdatera Restore-AzRecoveryServicesBackupItem.md</span><span class="sxs-lookup"><span data-stu-id="8eec2-444">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="8eec2-445">Uppdaterat tjänstanrop för avregistrering av container för Azure-filresurs</span><span class="sxs-lookup"><span data-stu-id="8eec2-445">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="8eec2-446">Uppdatera Set-AzRecoveryServicesAsrAlertSetting.md</span><span class="sxs-lookup"><span data-stu-id="8eec2-446">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="8eec2-447">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8eec2-447">Az.Resources</span></span>
- <span data-ttu-id="8eec2-448">Ta bort den cmdlet som saknas och som refereras i dokumentationen till New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8eec2-448">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="8eec2-449">Princip-cmdletar har uppdaterats så att de använder den nya API-versionen 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="8eec2-449">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="8eec2-450">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8eec2-450">Az.ServiceBus</span></span>
* <span data-ttu-id="8eec2-451">Ny cmmdlet har lagts till för att skapa SAS-token: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="8eec2-451">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="8eec2-452">verifierings- och felmeddelande har lagts till för authorizationrules-rättigheter om endast "hantera" har tilldelats</span><span class="sxs-lookup"><span data-stu-id="8eec2-452">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="8eec2-453">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8eec2-453">Az.Sql</span></span>
* <span data-ttu-id="8eec2-454">Åtgärda saknade exempel för Set-AzSqlDatabaseSecondary cmdlet</span><span class="sxs-lookup"><span data-stu-id="8eec2-454">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="8eec2-455">Åtgärda angivna återkommande genomsökningar för bedömning av säkerhetsrisk utan angivna e-postadresser</span><span class="sxs-lookup"><span data-stu-id="8eec2-455">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="8eec2-456">Korrigera ett skrivfel i ett varningsmeddelande.</span><span class="sxs-lookup"><span data-stu-id="8eec2-456">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8eec2-457">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8eec2-457">Az.Storage</span></span>
* <span data-ttu-id="8eec2-458">Uppdatera exempel i referensdokumentationen för Get-AzStorageAccount så att rätt parameternamn används</span><span class="sxs-lookup"><span data-stu-id="8eec2-458">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="8eec2-459">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="8eec2-459">Az.StorageSync</span></span>
* <span data-ttu-id="8eec2-460">Lägger till cmdleten Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="8eec2-460">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="8eec2-461">Åtgärda problem 9551 så att TierFilesOlderThanDays föredras</span><span class="sxs-lookup"><span data-stu-id="8eec2-461">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8eec2-462">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8eec2-462">Az.Websites</span></span>
* <span data-ttu-id="8eec2-463">Åtgärdar ett fel där vissa SiteConfig-egenskaper inte returnerades av Get-AzWebApp och Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="8eec2-463">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="8eec2-464">Lägger till en ny platsparameter för Get-AzDeletedWebApp och Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="8eec2-464">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="8eec2-465">Åtgärdar ett fel i kloning av webbapp-platser som använder New-AzWebApp-IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="8eec2-465">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="8eec2-466">2.4.0 – juli 2019</span><span class="sxs-lookup"><span data-stu-id="8eec2-466">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8eec2-467">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8eec2-467">Az.Accounts</span></span>
* <span data-ttu-id="8eec2-468">Lägg till stöd för profil-cmdletar</span><span class="sxs-lookup"><span data-stu-id="8eec2-468">Add support for profile cmdlets</span></span>
* <span data-ttu-id="8eec2-469">Lägg till stöd för miljöer och dataplaner i genererade cmdletar</span><span class="sxs-lookup"><span data-stu-id="8eec2-469">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="8eec2-470">Åtgärda bugg där fel slutpunkt i vissa fall användes för cmdletar för dataplaner i Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="8eec2-470">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="8eec2-471">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="8eec2-471">Az.Advisor</span></span>
* <span data-ttu-id="8eec2-472">GA-version av Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="8eec2-472">GA release of Az.Advisor</span></span>
* <span data-ttu-id="8eec2-473">Den här modulen ingår nu som en del av `Az`-sammanslagningsmodulen</span><span class="sxs-lookup"><span data-stu-id="8eec2-473">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="8eec2-474">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8eec2-474">Az.ApiManagement</span></span>
* <span data-ttu-id="8eec2-475">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="8eec2-475">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="8eec2-476">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="8eec2-476">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="8eec2-477">Stöd för att fråga prenumerationer efter användare och produkt har lagts till</span><span class="sxs-lookup"><span data-stu-id="8eec2-477">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="8eec2-478">Stöd för att fråga med hjälp av omfång ”/”, ”/apis”, ”/apis/echo-api” har lagts till</span><span class="sxs-lookup"><span data-stu-id="8eec2-478">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="8eec2-479">Korrigering av problem https://github.com/Azure/azure-powershell/issues/9307 och https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="8eec2-479">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="8eec2-480">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="8eec2-480">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="8eec2-481">Stöd för att ange ”ApiVersion” och ”ApiVersionSetId” när API:er importeras har lagts till</span><span class="sxs-lookup"><span data-stu-id="8eec2-481">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8eec2-482">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8eec2-482">Az.Automation</span></span>
* <span data-ttu-id="8eec2-483">Bugg med cmdleten Set-AzAutomationConnectionFieldValue för att hantera strängvärde har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="8eec2-483">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8eec2-484">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8eec2-484">Az.Compute</span></span>
* <span data-ttu-id="8eec2-485">Lägg till parametern HyperVGeneration i New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="8eec2-485">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8eec2-486">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8eec2-486">Az.DataFactory</span></span>
* <span data-ttu-id="8eec2-487">Uppdaterar utdata från ADF-cmdletar som hämtar aktivitetskörningar, hämtar pipelinekörningar och hämtar utlösarkörningar för stöd för Select-Object-pipe.</span><span class="sxs-lookup"><span data-stu-id="8eec2-487">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="8eec2-488">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="8eec2-488">Az.EventGrid</span></span>
* <span data-ttu-id="8eec2-489">Korrigera stavfel i dokumentation om ”New-AzEventGridSubscription”</span><span class="sxs-lookup"><span data-stu-id="8eec2-489">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8eec2-490">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8eec2-490">Az.IotHub</span></span>
* <span data-ttu-id="8eec2-491">Lägg till stöd för att återskapa principnycklar för auktorisering.</span><span class="sxs-lookup"><span data-stu-id="8eec2-491">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8eec2-492">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8eec2-492">Az.Network</span></span>
* <span data-ttu-id="8eec2-493">”RoutingPreference” har lagts till i offentliga IP-taggar</span><span class="sxs-lookup"><span data-stu-id="8eec2-493">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="8eec2-494">Förbättra exempel för referensdokumentation om ”Get-AzNetworkServiceTag”</span><span class="sxs-lookup"><span data-stu-id="8eec2-494">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="8eec2-495">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="8eec2-495">Az.PolicyInsights</span></span>
* <span data-ttu-id="8eec2-496">Åtgärda problem med null-referens i Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="8eec2-496">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="8eec2-497">Mer information här: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="8eec2-497">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="8eec2-498">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8eec2-498">Az.OperationalInsights</span></span>
* <span data-ttu-id="8eec2-499">Modellen för CustomLog-datakälla som returneras i Get-AzOperationalInsightsDataSource har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8eec2-499">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8eec2-500">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8eec2-500">Az.RecoveryServices</span></span>
* <span data-ttu-id="8eec2-501">Kommandot get-policy för IaaSVM:er har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8eec2-501">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="8eec2-502">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8eec2-502">Az.Resources</span></span>
    - <span data-ttu-id="8eec2-503">Korrigera hjälptext för den översta parametern i Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="8eec2-503">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="8eec2-504">Lägg till växlingsstöd på klientsidan för Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="8eec2-504">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="8eec2-505">Lägg till nya parametrar för Set-AzPolicyAssignment, -PolicyParameters och -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="8eec2-505">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="8eec2-506">En mängd dokument- och exempeluppdateringar för Policy-cmdletar</span><span class="sxs-lookup"><span data-stu-id="8eec2-506">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="8eec2-507">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8eec2-507">Az.ServiceBus</span></span>
* <span data-ttu-id="8eec2-508">Korrigering av problem #4938 – New-AzureRmServiceBusQueue returnerar BadRequest vid konfiguration av MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="8eec2-508">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="8eec2-509">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8eec2-509">Az.Sql</span></span>
* <span data-ttu-id="8eec2-510">Lägg till cmdletar för instansredundansgrupper från förhandsversion till offentlig version</span><span class="sxs-lookup"><span data-stu-id="8eec2-510">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="8eec2-511">Stöd för granskning för Azure SQL Server\Database med nya cmdletar.</span><span class="sxs-lookup"><span data-stu-id="8eec2-511">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="8eec2-512">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="8eec2-512">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="8eec2-513">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="8eec2-513">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="8eec2-514">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="8eec2-514">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="8eec2-515">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="8eec2-515">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="8eec2-516">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="8eec2-516">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="8eec2-517">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="8eec2-517">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="8eec2-518">Ta bort begränsningar för e-post från inställningarna för sårbarhetsbedömning</span><span class="sxs-lookup"><span data-stu-id="8eec2-518">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8eec2-519">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8eec2-519">Az.Storage</span></span>
* <span data-ttu-id="8eec2-520">Ändra två parametrar ”-IndexDocument” och ”-ErrorDocument404Path” från ”krävs” till ”valfri” i cmdlet:</span><span class="sxs-lookup"><span data-stu-id="8eec2-520">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="8eec2-521">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="8eec2-521">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="8eec2-522">Uppdatera hjälpen för Get-AzStorageBlobContent genom att lägga till ett exempel</span><span class="sxs-lookup"><span data-stu-id="8eec2-522">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="8eec2-523">Visa mer felinformation när cmdleten misslyckas med StorageException</span><span class="sxs-lookup"><span data-stu-id="8eec2-523">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="8eec2-524">Stöd för att skapa eller uppdatera lagringskonto med Azure Files AAD DS-autentisering</span><span class="sxs-lookup"><span data-stu-id="8eec2-524">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="8eec2-525">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8eec2-525">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="8eec2-526">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8eec2-526">Set-AzStorageAccount</span></span>
* <span data-ttu-id="8eec2-527">Stöd för att lista eller stänga filreferenser för en filresurs, filkatalog eller en fil</span><span class="sxs-lookup"><span data-stu-id="8eec2-527">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="8eec2-528">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="8eec2-528">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="8eec2-529">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="8eec2-529">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="8eec2-530">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="8eec2-530">Az.StorageSync</span></span>
* <span data-ttu-id="8eec2-531">Den här modulen ingår nu som en del av `Az`-sammanslagningsmodulen</span><span class="sxs-lookup"><span data-stu-id="8eec2-531">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="8eec2-532">2.3.2 – juni 2019</span><span class="sxs-lookup"><span data-stu-id="8eec2-532">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8eec2-533">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8eec2-533">Az.Accounts</span></span>
* <span data-ttu-id="8eec2-534">Åtgärda bugg med felaktiga webbadresser som i vissa fall användes för Functions-anrop</span><span class="sxs-lookup"><span data-stu-id="8eec2-534">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="8eec2-535">Mer information här: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="8eec2-535">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="8eec2-536">Åtgärda problem med alias från AzureRM i Az-cmdletar</span><span class="sxs-lookup"><span data-stu-id="8eec2-536">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="8eec2-537">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="8eec2-537">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="8eec2-538">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="8eec2-538">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8eec2-539">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8eec2-539">Az.Compute</span></span>
* <span data-ttu-id="8eec2-540">Parameteruppsättningarna New-AzVm och New-AzVmss accepterar nu parametern ”ProximityPlacementGroup”.</span><span class="sxs-lookup"><span data-stu-id="8eec2-540">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="8eec2-541">Stavfel i referensdokumentationen för ”New-AzVM” har korrigerats</span><span class="sxs-lookup"><span data-stu-id="8eec2-541">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="8eec2-542">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="8eec2-542">Az.Dns</span></span>
* <span data-ttu-id="8eec2-543">Stavfel i hjälpexempel för ”Set-AzDnsZone” har korrigerats.</span><span class="sxs-lookup"><span data-stu-id="8eec2-543">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="8eec2-544">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="8eec2-544">Az.EventGrid</span></span>
* <span data-ttu-id="8eec2-545">Har uppdaterats för att använda API-versionen 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="8eec2-545">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="8eec2-546">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="8eec2-546">New cmdlets:</span></span>
    - <span data-ttu-id="8eec2-547">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="8eec2-547">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="8eec2-548">Skapar en ny Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="8eec2-548">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="8eec2-549">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="8eec2-549">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="8eec2-550">Hämtar information om en Event Grid-domän eller hämtar en lista med alla Event Grid-domäner i den aktuella Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="8eec2-550">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="8eec2-551">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="8eec2-551">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="8eec2-552">Tar bort en Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="8eec2-552">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="8eec2-553">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="8eec2-553">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="8eec2-554">Återskapar nyckeln för delad åtkomst för en Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="8eec2-554">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="8eec2-555">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="8eec2-555">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="8eec2-556">Hämtar de nycklar för delad åtkomst som används för att publicera händelser till en Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="8eec2-556">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="8eec2-557">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="8eec2-557">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="8eec2-558">Skapar ett nytt Azure Event Grid-domänämne.</span><span class="sxs-lookup"><span data-stu-id="8eec2-558">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="8eec2-559">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="8eec2-559">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="8eec2-560">Hämtar information om ett Event Grid-domänämne eller hämtar en lista med alla Event Grid-domänämnen under en specifik Event Grid-domän i nuvarande Azure</span><span class="sxs-lookup"><span data-stu-id="8eec2-560">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="8eec2-561">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="8eec2-561">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="8eec2-562">Tar bort ett befintligt Azure Event Grid-domänämne.</span><span class="sxs-lookup"><span data-stu-id="8eec2-562">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="8eec2-563">Uppdaterade cmdletar:</span><span class="sxs-lookup"><span data-stu-id="8eec2-563">Updated cmdlets:</span></span>
    - <span data-ttu-id="8eec2-564">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="8eec2-564">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="8eec2-565">Lägg till nya obligatoriska parametrar för att stödja piping för den nya Event Grid-domänen och Event Grid-domänämnet för att göra det möjligt att skapa nya händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="8eec2-565">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="8eec2-566">Lägg till nya obligatoriska parametrar för att ange det nya Event Grid-domännamnet och/eller namnet på Event Grid-domänämnet för att göra det möjligt att skapa nya händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="8eec2-566">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="8eec2-567">Lägg till ny parameteruppsättningar för domäner och domänämnen för att göra det möjligt att återanvända befintliga parametrar (t.ex. EndPointType, SubjectBeginsWith osv).</span><span class="sxs-lookup"><span data-stu-id="8eec2-567">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="8eec2-568">Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="8eec2-568">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="8eec2-569">Förfallodatum för händelseprenumeration</span><span class="sxs-lookup"><span data-stu-id="8eec2-569">Event subscription expiration date,</span></span>
            - <span data-ttu-id="8eec2-570">Avancerade filterparametrar.</span><span class="sxs-lookup"><span data-stu-id="8eec2-570">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="8eec2-571">Lägg till ny uppräkning för servicebusqueue som mål.</span><span class="sxs-lookup"><span data-stu-id="8eec2-571">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="8eec2-572">Tillåt inte användning av ”Alla” i alternativet -IncludedEventType och ersätt det med</span><span class="sxs-lookup"><span data-stu-id="8eec2-572">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="8eec2-573">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="8eec2-573">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="8eec2-574">Lägg till ny valfria parametrar (Top, ODataQuery och NextLink) för att stödja sidnumrering och filtrering av resultat.</span><span class="sxs-lookup"><span data-stu-id="8eec2-574">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="8eec2-575">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="8eec2-575">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="8eec2-576">Lägg till nya obligatoriska parametrar för att stödja piping för en Event Grid-domän och Event Grid-domänämnen för att göra det möjligt att ta bort befintliga händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="8eec2-576">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="8eec2-577">Lägg till nya obligatoriska parametrar för att ange Event Grid-domännamnet och/eller namnet på Event Grid-domänämnet för att göra det möjligt att ta bort befintliga händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="8eec2-577">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="8eec2-578">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="8eec2-578">Az.FrontDoor</span></span>
* <span data-ttu-id="8eec2-579">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="8eec2-579">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="8eec2-580">Lägg till stöd för transformeringar och nytt värde för automatisk komplettering för operatorer (RegEx)</span><span class="sxs-lookup"><span data-stu-id="8eec2-580">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="8eec2-581">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="8eec2-581">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="8eec2-582">Lägg till nya värden för automatisk komplettering</span><span class="sxs-lookup"><span data-stu-id="8eec2-582">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8eec2-583">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8eec2-583">Az.Network</span></span>
* <span data-ttu-id="8eec2-584">Lägg till stöd för resurs för virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="8eec2-584">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="8eec2-585">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="8eec2-585">New cmdlets</span></span>
        - <span data-ttu-id="8eec2-586">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="8eec2-586">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="8eec2-587">Lägg till AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="8eec2-587">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="8eec2-588">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="8eec2-588">New cmdlets</span></span> 
        - <span data-ttu-id="8eec2-589">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="8eec2-589">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="8eec2-590">Lägg till PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="8eec2-590">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="8eec2-591">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="8eec2-591">New cmdlets</span></span> 
        - <span data-ttu-id="8eec2-592">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="8eec2-592">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="8eec2-593">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="8eec2-593">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="8eec2-594">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="8eec2-594">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="8eec2-595">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="8eec2-595">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="8eec2-596">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8eec2-596">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="8eec2-597">Lägg till PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="8eec2-597">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="8eec2-598">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="8eec2-598">New cmdlets</span></span>
        - <span data-ttu-id="8eec2-599">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="8eec2-599">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="8eec2-600">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="8eec2-600">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="8eec2-601">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="8eec2-601">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="8eec2-602">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="8eec2-602">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="8eec2-603">Nedanstående kommandon för funktionen har uppdaterats: Flaggan UseLocalAzureIpAddress på VpnConnection</span><span class="sxs-lookup"><span data-stu-id="8eec2-603">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="8eec2-604">New-AzVpnConnection har uppdaterats: Den valfria parametern -UseLocalAzureIpAddress har lagts till för att visa att en lokal IP-adress i Azure ska användas som källadress när anslutningen initieras.</span><span class="sxs-lookup"><span data-stu-id="8eec2-604">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="8eec2-605">Set-AzVpnConnection har uppdaterats: Den valfria parametern -UseLocalAzureIpAddress har lagts till för att visa att en lokal IP-adress i Azure ska användas som källadress när anslutningen initieras.</span><span class="sxs-lookup"><span data-stu-id="8eec2-605">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="8eec2-606">Det skrivskyddade fältet PeeredConnections har lagts till i ExpressRoute-peering.</span><span class="sxs-lookup"><span data-stu-id="8eec2-606">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="8eec2-607">Det skrivskyddade fältet GlobalReachEnabled har lagts till i ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="8eec2-607">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="8eec2-608">Ett attribut för icke-bakåtkompatibla ändringar har lagts till för att lyfta fram utfasning av fältet AllowGlobalReach i modellen ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8eec2-608">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="8eec2-609">Problem 8756 har åtgärdats: Fel vid användning av TargetListenerID med AzApplicationGatewayRedirectConfiguration-cmdletar</span><span class="sxs-lookup"><span data-stu-id="8eec2-609">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="8eec2-610">En bugg i New-AzApplicationGatewayPathRuleConfig som gjorde att regeluppsättningen för att återskapa inte kunde anges har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="8eec2-610">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="8eec2-611">Visningen av VirtualNetworkTaps i NetworkInterfaceIpConfiguration har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8eec2-611">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="8eec2-612">Cortex Get-cmdletar för att visa en lista med alla delar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8eec2-612">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="8eec2-613">Funktionen för att skapa VirtualHub-referenser för ExpressRouteGateways och VpnGateway har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8eec2-613">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="8eec2-614">Stöd för tillgänglighetszoner i AzureFirewall och NatGateway har lagts till</span><span class="sxs-lookup"><span data-stu-id="8eec2-614">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="8eec2-615">Cmdleten Get-AzNetworkServiceTag har lagts till</span><span class="sxs-lookup"><span data-stu-id="8eec2-615">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="8eec2-616">Lägg till stöd för flera offentliga IP-adresser för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="8eec2-616">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="8eec2-617">Cmdleten New-AzFirewall har uppdaterats:</span><span class="sxs-lookup"><span data-stu-id="8eec2-617">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="8eec2-618">Parametern -PublicIpAddress som accepterar ett eller flera offentliga IP-adressobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="8eec2-618">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="8eec2-619">Parametern -VirtualNetwork som accepterar ett virtuellt nätverksobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="8eec2-619">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="8eec2-620">Metoderna AddPublicIpAddress och RemovePublicIpAddress har lagts till på brandväggsobjekt – dessa accepterar ett offentligt IP-adressobjekt som indata</span><span class="sxs-lookup"><span data-stu-id="8eec2-620">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="8eec2-621">Inaktuella parametrar -PublicIpName och -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="8eec2-621">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="8eec2-622">Nedanstående kommandon för funktionen har uppdaterats: Ange autentiseringsalternativ för VpnClient AAD till resurser för virtuella nätverksgatewayer.</span><span class="sxs-lookup"><span data-stu-id="8eec2-622">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="8eec2-623">New-AzVirtualNetworkGateway har uppdaterats: De valfria parametrarna AadTenantUri, AadAudienceId och AadIssuerUri för att ange VpnClient AAD-autentiseringsalternativ på en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="8eec2-623">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="8eec2-624">Set-AzVirtualNetworkGateway har uppdaterats: De valfria parametrarna AadTenantUri, AadAudienceId och AadIssuerUri för att ange VpnClient AAD-autentiseringsalternativ på en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="8eec2-624">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="8eec2-625">Set-AzVirtualNetworkGateway har uppdaterats: Den valfria växelparametern RemoveAadAuthentication som tar bort VpnClient AAD-autentiseringsalternativ från en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="8eec2-625">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="8eec2-626">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8eec2-626">Az.OperationalInsights</span></span>
* <span data-ttu-id="8eec2-627">Aktivera prisnivån **pergb2018** i kommandot ”New-AzureRmOperationalInsightsWorkspace”</span><span class="sxs-lookup"><span data-stu-id="8eec2-627">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="8eec2-628">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8eec2-628">Az.Resources</span></span>
* <span data-ttu-id="8eec2-629">Stöd för ytterligare alternativ för att exportera en mall</span><span class="sxs-lookup"><span data-stu-id="8eec2-629">Support for additional Template Export options</span></span>
    - <span data-ttu-id="8eec2-630">Lägg till parametern ”-SkipResourceNameParameterization” till Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8eec2-630">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="8eec2-631">Lägg till parametern ”-SkipAllParameterization” till Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8eec2-631">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="8eec2-632">Lägg till parametern ”-Resource” till Export-AzResourceGroup för exporterad resursfiltrering</span><span class="sxs-lookup"><span data-stu-id="8eec2-632">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="8eec2-633">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8eec2-633">Az.ServiceFabric</span></span>
* <span data-ttu-id="8eec2-634">Åtgärda att fel tumavtryck används vid tilläggning av certifikat i ByExistingKeyVault i vissa fall</span><span class="sxs-lookup"><span data-stu-id="8eec2-634">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="8eec2-635">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8eec2-635">Az.Sql</span></span>
* <span data-ttu-id="8eec2-636">Åtgärda suffix för lagringsslutpunkt i Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="8eec2-636">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="8eec2-637">Åtgärda att aktivering av Advanced Data Security åsidosätter Advanced Threat Protection-princip</span><span class="sxs-lookup"><span data-stu-id="8eec2-637">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="8eec2-638">Nya cmdletar för Management.Sql som gör att kunderna kan lägga till nycklar för transparent datakryptering (TDE) och ange TDE-skydd för hanterade instanser</span><span class="sxs-lookup"><span data-stu-id="8eec2-638">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="8eec2-639">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="8eec2-639">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="8eec2-640">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="8eec2-640">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="8eec2-641">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="8eec2-641">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="8eec2-642">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="8eec2-642">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="8eec2-643">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="8eec2-643">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8eec2-644">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8eec2-644">Az.Storage</span></span>
* <span data-ttu-id="8eec2-645">Stöd för typerna FileStorage och SkuName Premium_ZRS när lagringskonton skapas</span><span class="sxs-lookup"><span data-stu-id="8eec2-645">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="8eec2-646">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8eec2-646">New-AzStorageAccount</span></span>
* <span data-ttu-id="8eec2-647">Beskrivningen av cmdleten för bloboföränderlighet har förtydligats</span><span class="sxs-lookup"><span data-stu-id="8eec2-647">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="8eec2-648">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="8eec2-648">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8eec2-649">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8eec2-649">Az.Websites</span></span>
* <span data-ttu-id="8eec2-650">Optimerar Get-AzWebAppCertificate för att filtrera efter resursgrupp på servern i stället för klienten</span><span class="sxs-lookup"><span data-stu-id="8eec2-650">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="8eec2-651">Lägger till växlingsparametern -UseDisasterRecovery till Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="8eec2-651">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="8eec2-652">2.2.0 – juni 2019</span><span class="sxs-lookup"><span data-stu-id="8eec2-652">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="8eec2-653">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="8eec2-653">Az.Cdn</span></span>
* <span data-ttu-id="8eec2-654">Uppdaterade cmdletar för att ge stöd för rulesEngine-funktion baserat på API-version 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="8eec2-654">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8eec2-655">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8eec2-655">Az.Compute</span></span>
* <span data-ttu-id="8eec2-656">Lade till parameter `NoWait` som startar åtgärden och returnerar omedelbart, innan åtgärden har slutförts.</span><span class="sxs-lookup"><span data-stu-id="8eec2-656">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="8eec2-657">Uppdaterade cmdletar:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="8eec2-657">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="8eec2-658">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="8eec2-658">Az.EventHub</span></span>
* <span data-ttu-id="8eec2-659">Korrigering för #9231 – Get-AzEventHubNamespace returnerar inga taggar</span><span class="sxs-lookup"><span data-stu-id="8eec2-659">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="8eec2-660">Korrigering för #9230 – Get-AzEventHubNamespace returnerar ResourceGroup istället för ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8eec2-660">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8eec2-661">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8eec2-661">Az.Network</span></span>
* <span data-ttu-id="8eec2-662">Uppdatera ResourceId och InputObject för NAT-gateway</span><span class="sxs-lookup"><span data-stu-id="8eec2-662">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="8eec2-663">Lägg till alias för ResourceId och InputObject</span><span class="sxs-lookup"><span data-stu-id="8eec2-663">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="8eec2-664">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="8eec2-664">Az.PolicyInsights</span></span>
* <span data-ttu-id="8eec2-665">Åtgärda Null-referensproblem i Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="8eec2-665">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8eec2-666">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8eec2-666">Az.RecoveryServices</span></span>
* <span data-ttu-id="8eec2-667">Minsta kvarhållning för IaaSVM-policy i dagar ändrat till 7 från 1</span><span class="sxs-lookup"><span data-stu-id="8eec2-667">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="8eec2-668">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8eec2-668">Az.ServiceBus</span></span>
* <span data-ttu-id="8eec2-669">Korrigering för ärende #9182 – Get-AzServiceBusNamespace returnerar ResourceGroup istället för ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8eec2-669">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="8eec2-670">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8eec2-670">Az.ServiceFabric</span></span>
* <span data-ttu-id="8eec2-671">Åtgärda stavfel i felmeddelandet för Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="8eec2-671">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="8eec2-672">Åtgärda saknat tecken i Service Fabric-kommandorader</span><span class="sxs-lookup"><span data-stu-id="8eec2-672">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="8eec2-673">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8eec2-673">Az.Sql</span></span>
* <span data-ttu-id="8eec2-674">Lägg till parametern DnsZonePartner för New-AzureSqlInstance-cmdlet för att ge stöd för AutoDr för hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="8eec2-674">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="8eec2-675">Avvecklar cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="8eec2-675">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="8eec2-676">Döp om cmdletar för hotidentifiering till Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="8eec2-676">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="8eec2-677">Parametrarna New-AzSqlInstance -StorageSizeInGB och -LicenseType är nu valfria.</span><span class="sxs-lookup"><span data-stu-id="8eec2-677">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8eec2-678">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8eec2-678">Az.Websites</span></span>
* <span data-ttu-id="8eec2-679">åtgärdar problemet där användningen av Set-AzWebApp och Set-AzWebAppSlot med -WebApp-egenskap tog bort taggarna</span><span class="sxs-lookup"><span data-stu-id="8eec2-679">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="8eec2-680">2.1.0 – maj 2019</span><span class="sxs-lookup"><span data-stu-id="8eec2-680">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="8eec2-681">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8eec2-681">Az.ApiManagement</span></span>
* <span data-ttu-id="8eec2-682">Skapade nya cmdletar för att hantera diagnostik för global- och API-omfång</span><span class="sxs-lookup"><span data-stu-id="8eec2-682">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="8eec2-683">**Get-AzApiManagementDiagnostic** – Skaffa diagnostik konfigurerad för global- eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="8eec2-683">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="8eec2-684">**New-AzApiManagementDiagnostic** – Skapa ny diagnostik för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="8eec2-684">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="8eec2-685">**New-AzApiManagementHttpMessageDiagnostic** – Skapa diagnostikinställning om vilka rubriker som ska loggas och storleken på brödtextbyte</span><span class="sxs-lookup"><span data-stu-id="8eec2-685">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="8eec2-686">**New-AzApiManagementPipelineDiagnosticSetting** – Skapa diagnostikinställningar för inkommande/utgående HTTP-meddelanden till gatewayen.</span><span class="sxs-lookup"><span data-stu-id="8eec2-686">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="8eec2-687">**New-AzApiManagementSamplingSetting** – Skapa samplinginställningar för begäranden/svar för en diagnostik</span><span class="sxs-lookup"><span data-stu-id="8eec2-687">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="8eec2-688">**Remove-AzApiManagementDiagnostic** – Ta bort en diagnostikenhet för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="8eec2-688">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="8eec2-689">**Set-AzApiManagementDiagnostic** – Uppdatera en diagnostikenhet för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="8eec2-689">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="8eec2-690">Skapade nya cmdletar för hantering av cacheminne i ApiManagement-tjänsten</span><span class="sxs-lookup"><span data-stu-id="8eec2-690">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="8eec2-691">**Get-AzApiManagementCache** – Hämta information om cacheminnet som anges av identifierare eller alla cacheminnen</span><span class="sxs-lookup"><span data-stu-id="8eec2-691">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="8eec2-692">**New-AzApiManagementCache** – Skapa ett nytt default-cacheminne eller cacheminne i en viss Azure-region</span><span class="sxs-lookup"><span data-stu-id="8eec2-692">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="8eec2-693">**Remove-AzApiManagementCache** – Ta bort ett cacheminne</span><span class="sxs-lookup"><span data-stu-id="8eec2-693">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="8eec2-694">**Remove-AzApiManagementCache** – Ta bort ett cacheminne</span><span class="sxs-lookup"><span data-stu-id="8eec2-694">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="8eec2-695">Skapade nya cmdletar för hantering av API-schema</span><span class="sxs-lookup"><span data-stu-id="8eec2-695">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="8eec2-696">**New-AzApiManagementSchema** – Skapa ett nytt schema för ett API</span><span class="sxs-lookup"><span data-stu-id="8eec2-696">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="8eec2-697">**Get-AzApiManagementSchema** – Hämta de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="8eec2-697">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="8eec2-698">**Remove-AzApiManagementSchema** – Ta bort de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="8eec2-698">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="8eec2-699">**Set-AzApiManagementSchema** – Uppdatera de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="8eec2-699">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="8eec2-700">Skapa ny cmdlet för att generera en användartoken.</span><span class="sxs-lookup"><span data-stu-id="8eec2-700">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="8eec2-701">**New-AzApiManagementUserToken** – Skapa en ny användartoken som enligt standardinställning är giltig i 8 timmar. Token för GIT-användaren kan skapas med den här cmdleten./</span><span class="sxs-lookup"><span data-stu-id="8eec2-701">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="8eec2-702">Skapade en ny cmdlet för att hämta nätverksstatus</span><span class="sxs-lookup"><span data-stu-id="8eec2-702">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="8eec2-703">**Get-AzApiManagementNetworkStatus** – Hämta nätverksstatusanslutningen för resurserna som API Management-tjänsten är beroende av.</span><span class="sxs-lookup"><span data-stu-id="8eec2-703">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="8eec2-704">Det här är användbart när du distribuerar ApiManagement-tjänsten i ett virtuellt nätverk och validerar om något beroende är brutet.</span><span class="sxs-lookup"><span data-stu-id="8eec2-704">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="8eec2-705">Uppdaterade cmdlet **New-AzApiManagement** för att hantera ApiManagement-tjänsten</span><span class="sxs-lookup"><span data-stu-id="8eec2-705">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="8eec2-706">Lade till stöd för den nya SKU:n Consumption</span><span class="sxs-lookup"><span data-stu-id="8eec2-706">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="8eec2-707">Aktiverade stöd för att slå på flaggan EnableClientCertificate för SKU:n Consumption</span><span class="sxs-lookup"><span data-stu-id="8eec2-707">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="8eec2-708">Den nya cmdleten **New-AzApiManagementSslSetting** gör det möjligt att ställa in TLS/SSL-inställningen på ”Backend” och ”Frontend” (serverdel och klientdel).</span><span class="sxs-lookup"><span data-stu-id="8eec2-708">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="8eec2-709">Det här kan också användas till att konfigurera chiffer som 3DES och ServerProtocols som Http2 för Frontend för en ApiManagement-tjänst.</span><span class="sxs-lookup"><span data-stu-id="8eec2-709">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="8eec2-710">Stöd har lagts till för att konfigurera värdnamnet DeveloperPortal på ApiManagement-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="8eec2-710">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="8eec2-711">Uppdaterade cmdletar **Get-AzApiManagementSsoToken** för att ta PsApiManagement-objekt som indata</span><span class="sxs-lookup"><span data-stu-id="8eec2-711">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="8eec2-712">Uppdaterad cmdleten för att visa infogade felmeddelanden</span><span class="sxs-lookup"><span data-stu-id="8eec2-712">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="8eec2-713">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Felkod: Felmeddelande av typen ValidationError: Ett eller flera fält innehåller felaktiga värden: Felinformation:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="8eec2-713">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="8eec2-714">Uppdaterade cmdlet **Export-AzApiManagementApi** för att exportera API:er i OpenApi 3.0-format</span><span class="sxs-lookup"><span data-stu-id="8eec2-714">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="8eec2-715">Uppdaterade cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="8eec2-715">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="8eec2-716">Importera API från dokumentspecifikationen OpenApi 3.0</span><span class="sxs-lookup"><span data-stu-id="8eec2-716">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="8eec2-717">Om du vill åsidosätta egenskapen PsApiManagementSchema specificerad i ett dokument (Swagger, Wadl, Wsdl, OpenApi).</span><span class="sxs-lookup"><span data-stu-id="8eec2-717">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="8eec2-718">Åsidosätta egenskapen ServiceUrl som specificeras i ett dokument.</span><span class="sxs-lookup"><span data-stu-id="8eec2-718">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="8eec2-719">Uppdaterade cmdlet **Get-AzApiManagementPolicy** för att returnera policy i undantaget format av typen icke-XML med rawxml</span><span class="sxs-lookup"><span data-stu-id="8eec2-719">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="8eec2-720">Uppdaterade cmdlet **Set-AzApiManagementPolicy** för att godkänna policy i undantaget format av typen icke-XML med rawxml och XML undantaget med xml</span><span class="sxs-lookup"><span data-stu-id="8eec2-720">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="8eec2-721">Uppdaterad cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="8eec2-721">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="8eec2-722">Konfigurera API med OpenId auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="8eec2-722">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="8eec2-723">Skapa ett API i ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="8eec2-723">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="8eec2-724">Klona ett API med SourceApiId och SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="8eec2-724">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="8eec2-725">Möjlighet att konfigurera SubscriptionRequired i API-omfattningen.</span><span class="sxs-lookup"><span data-stu-id="8eec2-725">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="8eec2-726">Uppdaterad cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="8eec2-726">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="8eec2-727">Konfigurera API med OpenId auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="8eec2-727">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="8eec2-728">Uppdatera ett API till ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="8eec2-728">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="8eec2-729">Möjlighet att konfigurera SubscriptionRequired i API-omfattningen.</span><span class="sxs-lookup"><span data-stu-id="8eec2-729">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="8eec2-730">Uppdaterad cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="8eec2-730">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="8eec2-731">Klona en befintlig version med hjälp av SourceApiRevision (kopiera taggar, produkter, åtgärder och principer).</span><span class="sxs-lookup"><span data-stu-id="8eec2-731">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="8eec2-732">Den nya revisionen antar ApiId från den överordnade instansen.</span><span class="sxs-lookup"><span data-stu-id="8eec2-732">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="8eec2-733">Tillhandahålla ApiRevisionDescription</span><span class="sxs-lookup"><span data-stu-id="8eec2-733">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="8eec2-734">Åsidosätta ServiceUrl vid kloning av ett API.</span><span class="sxs-lookup"><span data-stu-id="8eec2-734">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="8eec2-735">Uppdaterad cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="8eec2-735">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="8eec2-736">Konfigurera AAD eller AADB2C med en Authority</span><span class="sxs-lookup"><span data-stu-id="8eec2-736">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="8eec2-737">Konfigurera SignupPolicy, SigninPolicy, ProfileEditingPolicy och PasswordResetPolicy</span><span class="sxs-lookup"><span data-stu-id="8eec2-737">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="8eec2-738">Uppdaterad cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="8eec2-738">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="8eec2-739">Kompensera för ny SubscriptonModel med Scope och UserId</span><span class="sxs-lookup"><span data-stu-id="8eec2-739">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="8eec2-740">Kompensera för gammal prenumerationsmodell med ProductId och UserId</span><span class="sxs-lookup"><span data-stu-id="8eec2-740">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="8eec2-741">Lägg till funktion för att aktivera AllowTracing på prenumerationsnivå.</span><span class="sxs-lookup"><span data-stu-id="8eec2-741">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="8eec2-742">Uppdaterad cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="8eec2-742">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="8eec2-743">Kompensera för ny SubscriptonModel med Scope och UserId</span><span class="sxs-lookup"><span data-stu-id="8eec2-743">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="8eec2-744">Kompensera för gammal prenumerationsmodell med ProductId och UserId</span><span class="sxs-lookup"><span data-stu-id="8eec2-744">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="8eec2-745">Lägg till funktion för att aktivera AllowTracing på prenumerationsnivå.</span><span class="sxs-lookup"><span data-stu-id="8eec2-745">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="8eec2-746">Uppdaterade följande cmdletar för att acceptera ResourceId som indata</span><span class="sxs-lookup"><span data-stu-id="8eec2-746">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="8eec2-747">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="8eec2-747">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="8eec2-748">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="8eec2-748">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="8eec2-749">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="8eec2-749">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="8eec2-750">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="8eec2-750">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="8eec2-751">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="8eec2-751">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="8eec2-752">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="8eec2-752">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="8eec2-753">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="8eec2-753">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="8eec2-754">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="8eec2-754">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="8eec2-755">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="8eec2-755">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="8eec2-756">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="8eec2-756">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="8eec2-757">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="8eec2-757">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="8eec2-758">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="8eec2-758">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8eec2-759">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8eec2-759">Az.Automation</span></span>
* <span data-ttu-id="8eec2-760">Uppdaterade Get-AzAutomationJobOutputRecord för att hantera postvärden av typen JSON och Text.</span><span class="sxs-lookup"><span data-stu-id="8eec2-760">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="8eec2-761">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="8eec2-761">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="8eec2-762">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="8eec2-762">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="8eec2-763">Ändrade beteende för Start-AzAutomationDscCompilationJob till att bara starta jobbet istället för att vänta på slutförandet.</span><span class="sxs-lookup"><span data-stu-id="8eec2-763">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="8eec2-764">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="8eec2-764">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="8eec2-765">Korrigering för Get-AzAutomationDscNode när using -Name returnerar alla noder.</span><span class="sxs-lookup"><span data-stu-id="8eec2-765">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="8eec2-766">Nu returnerar den endast den matchande noden.</span><span class="sxs-lookup"><span data-stu-id="8eec2-766">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8eec2-767">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8eec2-767">Az.Compute</span></span>
* <span data-ttu-id="8eec2-768">Lägg till parametrarna ProtectFromScaleIn och ProtectFromScaleSetAction i cmdleten Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="8eec2-768">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="8eec2-769">Nu är standardinställningen att vimpelparametern New-AzVM använder en tillgänglig plats om USA, östra inte stöds</span><span class="sxs-lookup"><span data-stu-id="8eec2-769">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8eec2-770">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8eec2-770">Az.DataLakeStore</span></span>
* <span data-ttu-id="8eec2-771">Uppdatera ADLS-sdk för att använda httpclient, integrera dataplanstestning med Azure-ramverk</span><span class="sxs-lookup"><span data-stu-id="8eec2-771">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8eec2-772">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8eec2-772">Az.Monitor</span></span>
* <span data-ttu-id="8eec2-773">Korrigera felaktiga parameternamn i hjälpexempel</span><span class="sxs-lookup"><span data-stu-id="8eec2-773">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8eec2-774">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8eec2-774">Az.Network</span></span>
* <span data-ttu-id="8eec2-775">Lägg till flaggan DisableBgpRoutePropagation i utdata för effektiv routningstabell</span><span class="sxs-lookup"><span data-stu-id="8eec2-775">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="8eec2-776">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="8eec2-776">Updated cmdlet:</span></span>
        - <span data-ttu-id="8eec2-777">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="8eec2-777">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="8eec2-778">Åtgärda dubbelstreck i dokumentationen New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="8eec2-778">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="8eec2-779">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8eec2-779">Az.Resources</span></span>
* <span data-ttu-id="8eec2-780">Lägg till ny cmdlet Get-AzureRmDenyAssignment för att hämta tilldelningsnekanden</span><span class="sxs-lookup"><span data-stu-id="8eec2-780">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="8eec2-781">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8eec2-781">Az.Sql</span></span>
* <span data-ttu-id="8eec2-782">Döp om Advanced Threat Protection-cmdletar för Advanced Data Security och aktivera Vulnerability Assessment som standard</span><span class="sxs-lookup"><span data-stu-id="8eec2-782">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="8eec2-783">2.0.0 – maj 2019</span><span class="sxs-lookup"><span data-stu-id="8eec2-783">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8eec2-784">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8eec2-784">Az.Accounts</span></span>
* <span data-ttu-id="8eec2-785">Uppdatera autentiseringsbiblioteket för att åtgärda ADFS-problem med autentisering av användarnamn/lösenord</span><span class="sxs-lookup"><span data-stu-id="8eec2-785">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="8eec2-786">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8eec2-786">Az.CognitiveServices</span></span>
* <span data-ttu-id="8eec2-787">Visa endast Bing-ansvarsfriskrivning för Bing-sökningstjänster.</span><span class="sxs-lookup"><span data-stu-id="8eec2-787">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="8eec2-788">Förbättra felmeddelande när det inte går att skapa konton.</span><span class="sxs-lookup"><span data-stu-id="8eec2-788">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8eec2-789">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8eec2-789">Az.Compute</span></span>
* <span data-ttu-id="8eec2-790">Funktion för närhetsplaceringsgrupper.</span><span class="sxs-lookup"><span data-stu-id="8eec2-790">Proximity placement group feature.</span></span>
    - <span data-ttu-id="8eec2-791">Följande nya cmdletar har lagts till:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="8eec2-791">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="8eec2-792">Den nya parametern ProximityPlacementGroupId har lagts till i följande cmdletar:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="8eec2-792">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="8eec2-793">Parametern StorageAccountType har lagts till i New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="8eec2-793">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="8eec2-794">TargetRegion för New-AzGalleryImageVersion kan innehålla StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="8eec2-794">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="8eec2-795">Växlingsparametern SkipShutdown har lagts till i Stop-AzVM och Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="8eec2-795">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="8eec2-796">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="8eec2-796">Breaking changes</span></span>
    - <span data-ttu-id="8eec2-797">Set-AzVMBootDiagnostics har ändrats till Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="8eec2-797">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="8eec2-798">Export-AzLogAnalyticThrottledRequests har ändrats till Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="8eec2-798">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="8eec2-799">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="8eec2-799">Az.DeploymentManager</span></span>
* <span data-ttu-id="8eec2-800">De första allmänt tillgängliga versionerna av cmdletar för Distributionshanteraren i Azure</span><span class="sxs-lookup"><span data-stu-id="8eec2-800">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="8eec2-801">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="8eec2-801">Az.Dns</span></span>
* <span data-ttu-id="8eec2-802">Automatisk delegering av DNS för NameServer</span><span class="sxs-lookup"><span data-stu-id="8eec2-802">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="8eec2-803">Det överordnade zonnamnet kan användas som ytterligare valfri parameter i cmdleten för att skapa DNS-zoner.</span><span class="sxs-lookup"><span data-stu-id="8eec2-803">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="8eec2-804">Lägger till NS-poster för en nyligen skapad underordnad zon i den överordnade zonen.</span><span class="sxs-lookup"><span data-stu-id="8eec2-804">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="8eec2-805">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="8eec2-805">Az.FrontDoor</span></span>
* <span data-ttu-id="8eec2-806">De första allmänt tillgängliga versionerna av cmdletar för Azure FrontDoor</span><span class="sxs-lookup"><span data-stu-id="8eec2-806">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="8eec2-807">Byt namn på WAF-cmdletar så att de omfattar ”Waf”</span><span class="sxs-lookup"><span data-stu-id="8eec2-807">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="8eec2-808">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="8eec2-808">Az.HDInsight</span></span>
* <span data-ttu-id="8eec2-809">Två cmdletar har tagits bort:</span><span class="sxs-lookup"><span data-stu-id="8eec2-809">Removed two cmdlets:</span></span>
    - <span data-ttu-id="8eec2-810">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="8eec2-810">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="8eec2-811">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="8eec2-811">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="8eec2-812">En ny cmdlet har lagts till, Set-AzHDInsightGatewayCredential, som ersätter Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="8eec2-812">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="8eec2-813">Uppdatera cmdleten Get-AzHDInsightJobOutput för att skilja mellan läsarrollen och HDInsight-operatörsrollen:</span><span class="sxs-lookup"><span data-stu-id="8eec2-813">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="8eec2-814">Användare med läsarrollen måste uttryckligen ange parametern ”DefaultStorageAccountKey”, annars uppstår fel.</span><span class="sxs-lookup"><span data-stu-id="8eec2-814">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="8eec2-815">Användare med HDInsight-operatörsrollen påverkas inte.</span><span class="sxs-lookup"><span data-stu-id="8eec2-815">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8eec2-816">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8eec2-816">Az.Monitor</span></span>
* <span data-ttu-id="8eec2-817">Nya cmdletar för SQR API (schemalagd frågeregel)</span><span class="sxs-lookup"><span data-stu-id="8eec2-817">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="8eec2-818">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="8eec2-818">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="8eec2-819">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="8eec2-819">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="8eec2-820">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="8eec2-820">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="8eec2-821">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="8eec2-821">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="8eec2-822">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="8eec2-822">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="8eec2-823">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="8eec2-823">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="8eec2-824">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="8eec2-824">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="8eec2-825">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="8eec2-825">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="8eec2-826">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="8eec2-826">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="8eec2-827">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="8eec2-827">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="8eec2-828">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="8eec2-828">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="8eec2-829">[Mer](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information om SQR API</span><span class="sxs-lookup"><span data-stu-id="8eec2-829">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="8eec2-830">Az.Monitor.md har uppdaterats för att omfatta cmdletar för måttbaserade aviseringsregler i GenV2 (inte klassiska)</span><span class="sxs-lookup"><span data-stu-id="8eec2-830">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8eec2-831">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8eec2-831">Az.Network</span></span>
* <span data-ttu-id="8eec2-832">Lägg till stöd för NAT Gateway-resurs</span><span class="sxs-lookup"><span data-stu-id="8eec2-832">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="8eec2-833">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="8eec2-833">New cmdlets</span></span>
        - <span data-ttu-id="8eec2-834">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="8eec2-834">New-AzNatGateway</span></span>
        - <span data-ttu-id="8eec2-835">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="8eec2-835">Get-AzNatGateway</span></span>
        - <span data-ttu-id="8eec2-836">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="8eec2-836">Set-AzNatGateway</span></span>
        - <span data-ttu-id="8eec2-837">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="8eec2-837">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="8eec2-838">Uppdaterade cmdletar</span><span class="sxs-lookup"><span data-stu-id="8eec2-838">Updated cmdlets</span></span>
        - <span data-ttu-id="8eec2-839">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="8eec2-839">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="8eec2-840">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="8eec2-840">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="8eec2-841">Nedanstående kommandon för funktionen har uppdaterats: Ange/ta bort anpassade vägar på Brooklyn Gateway.</span><span class="sxs-lookup"><span data-stu-id="8eec2-841">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="8eec2-842">New-AzVirtualNetworkGateway har uppdaterats: Den valfria parametern -CustomRoute har lagts till för att ställa in adressprefix som anpassade vägar för att ange gateway.</span><span class="sxs-lookup"><span data-stu-id="8eec2-842">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="8eec2-843">Set-AzVirtualNetworkGateway har uppdaterats: Den valfria parametern -CustomRoute har lagts till för att ange adressprefix som anpassade vägar för att ange gateway.</span><span class="sxs-lookup"><span data-stu-id="8eec2-843">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="8eec2-844">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="8eec2-844">Az.PolicyInsights</span></span>
* <span data-ttu-id="8eec2-845">Stöd för att fråga efter information om principutvärdering.</span><span class="sxs-lookup"><span data-stu-id="8eec2-845">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="8eec2-846">Lägg till parametern ”-Expand” för Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="8eec2-846">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="8eec2-847">Stöd för -Expand PolicyEvaluationDetails.</span><span class="sxs-lookup"><span data-stu-id="8eec2-847">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8eec2-848">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8eec2-848">Az.RecoveryServices</span></span>
* <span data-ttu-id="8eec2-849">Stöd för att dela prenumeration mellan Azure och Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="8eec2-849">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="8eec2-850">Markering av kommande icke-bakåtkompatibla ändringar för Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="8eec2-850">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="8eec2-851">Korrigering för återställningsplan och åtgärdsplan i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="8eec2-851">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="8eec2-852">Korrigering för mappning av uppdateringsnätverk i Azure Site Recovery för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="8eec2-852">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="8eec2-853">Korrigering för instruktioner för uppdateringsskydd i Azure Site Recovery för Azure till Azure för hanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="8eec2-853">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="8eec2-854">Andra mindre korrigeringar.</span><span class="sxs-lookup"><span data-stu-id="8eec2-854">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="8eec2-855">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="8eec2-855">Az.Relay</span></span>
* <span data-ttu-id="8eec2-856">Korrigera stavfel i kundriktade meddelanden</span><span class="sxs-lookup"><span data-stu-id="8eec2-856">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="8eec2-857">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8eec2-857">Az.ServiceBus</span></span>
* <span data-ttu-id="8eec2-858">Nya cmdletar har lagts till för NetworkRuleSet för namnområden</span><span class="sxs-lookup"><span data-stu-id="8eec2-858">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8eec2-859">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8eec2-859">Az.Storage</span></span>
* <span data-ttu-id="8eec2-860">Uppgradera till lagringsklientbiblioteket 10.0.1 (namnområdet för alla objekt från detta SDK ändras från ”Microsoft.WindowsAzure.Storage. *till ”Microsoft.Azure.Storage.* ”)</span><span class="sxs-lookup"><span data-stu-id="8eec2-860">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="8eec2-861">Uppgradera till Microsoft.Azure.Management.Storage 11.0.0 för att stödja den nya API-versionen 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="8eec2-861">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="8eec2-862">Standardlagringskontot i Skapa lagringskonto ändras från ”Storage” till ”StorageV2”</span><span class="sxs-lookup"><span data-stu-id="8eec2-862">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="8eec2-863">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8eec2-863">New-AzStorageAccount</span></span>
* <span data-ttu-id="8eec2-864">Ändra lagringskontots cmdlet-utdata Sku.Name för att passa med indata-SkuName genom att lägga till ”-”. Till exempel ändras ”StandardLRS” till ”Standard_LRS”</span><span class="sxs-lookup"><span data-stu-id="8eec2-864">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="8eec2-865">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8eec2-865">New-AzStorageAccount</span></span>
    - <span data-ttu-id="8eec2-866">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8eec2-866">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="8eec2-867">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8eec2-867">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8eec2-868">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8eec2-868">Az.Websites</span></span>
* <span data-ttu-id="8eec2-869">Egenskapen ”typ” konfigureras nu för PSSite-objekt som returneras av Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="8eec2-869">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="8eec2-870">Get-AzWebApp\*Metrics och Get-AzAppServicePlanMetrics markeras som inaktuella</span><span class="sxs-lookup"><span data-stu-id="8eec2-870">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="8eec2-871">1.8.0 – april 2019</span><span class="sxs-lookup"><span data-stu-id="8eec2-871">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="8eec2-872">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="8eec2-872">Highlights since the last major release</span></span>
* <span data-ttu-id="8eec2-873">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="8eec2-873">General availability of `Az` module</span></span>
* <span data-ttu-id="8eec2-874">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="8eec2-874">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="8eec2-875">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="8eec2-875">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="8eec2-876">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="8eec2-876">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="8eec2-877">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="8eec2-877">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="8eec2-878">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="8eec2-878">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="8eec2-879">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="8eec2-879">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="8eec2-880">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8eec2-880">Az.Accounts</span></span>
* <span data-ttu-id="8eec2-881">Uppdatera Uninstall-AzureRm för att ta bort moduler i Mac på ett korrekt sätt</span><span class="sxs-lookup"><span data-stu-id="8eec2-881">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="8eec2-882">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="8eec2-882">Az.Batch</span></span>
* <span data-ttu-id="8eec2-883">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8eec2-883">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="8eec2-884">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="8eec2-884">Az.Cdn</span></span>
* <span data-ttu-id="8eec2-885">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8eec2-885">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="8eec2-886">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8eec2-886">Az.CognitiveServices</span></span>
* <span data-ttu-id="8eec2-887">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8eec2-887">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8eec2-888">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8eec2-888">Az.Compute</span></span>
* <span data-ttu-id="8eec2-889">Åtgärda problem med AEM-installationen om resurs-ID:n för diskar innehåller resourcegroups i gemener i resurs-ID:n</span><span class="sxs-lookup"><span data-stu-id="8eec2-889">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="8eec2-890">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8eec2-890">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="8eec2-891">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="8eec2-891">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8eec2-892">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8eec2-892">Az.DataFactory</span></span>
* <span data-ttu-id="8eec2-893">Lägg till SsisProperties om NodeCount inte är null för hanterad integreringskörning.</span><span class="sxs-lookup"><span data-stu-id="8eec2-893">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8eec2-894">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8eec2-894">Az.DataLakeStore</span></span>
* <span data-ttu-id="8eec2-895">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8eec2-895">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="8eec2-896">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="8eec2-896">Az.EventGrid</span></span>
* <span data-ttu-id="8eec2-897">Hjälptexten för slutpunkten har uppdaterats för att visa att resurser ska skapas innan cmdletarna för att skapa/uppdatera händelseprenumerationer används.</span><span class="sxs-lookup"><span data-stu-id="8eec2-897">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="8eec2-898">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="8eec2-898">Az.EventHub</span></span>
* <span data-ttu-id="8eec2-899">Nya cmdletar har lagts till för NetworkRuleSet för namnområden</span><span class="sxs-lookup"><span data-stu-id="8eec2-899">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="8eec2-900">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="8eec2-900">Az.HDInsight</span></span>
* <span data-ttu-id="8eec2-901">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8eec2-901">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8eec2-902">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8eec2-902">Az.IotHub</span></span>
* <span data-ttu-id="8eec2-903">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8eec2-903">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8eec2-904">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8eec2-904">Az.KeyVault</span></span>
* <span data-ttu-id="8eec2-905">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8eec2-905">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="8eec2-906">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="8eec2-906">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="8eec2-907">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="8eec2-907">Az.MachineLearning</span></span>
* <span data-ttu-id="8eec2-908">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8eec2-908">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="8eec2-909">Az.Media</span><span class="sxs-lookup"><span data-stu-id="8eec2-909">Az.Media</span></span>
* <span data-ttu-id="8eec2-910">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8eec2-910">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8eec2-911">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8eec2-911">Az.Monitor</span></span>
  * <span data-ttu-id="8eec2-912">Nya cmdletar för måttbaserad aviseringsregel i GenV2 (inte klassisk)</span><span class="sxs-lookup"><span data-stu-id="8eec2-912">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="8eec2-913">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="8eec2-913">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="8eec2-914">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="8eec2-914">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="8eec2-915">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="8eec2-915">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="8eec2-916">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="8eec2-916">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="8eec2-917">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="8eec2-917">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="8eec2-918">Monitor SDK har uppdaterats till version 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="8eec2-918">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8eec2-919">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8eec2-919">Az.Network</span></span>
* <span data-ttu-id="8eec2-920">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8eec2-920">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="8eec2-921">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="8eec2-921">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="8eec2-922">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="8eec2-922">Az.NotificationHubs</span></span>
* <span data-ttu-id="8eec2-923">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8eec2-923">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="8eec2-924">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8eec2-924">Az.OperationalInsights</span></span>
* <span data-ttu-id="8eec2-925">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8eec2-925">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="8eec2-926">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="8eec2-926">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="8eec2-927">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8eec2-927">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8eec2-928">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8eec2-928">Az.RecoveryServices</span></span>
* <span data-ttu-id="8eec2-929">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8eec2-929">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="8eec2-930">Tabellformatet för SQL i virtuella Azure-datorer har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="8eec2-930">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="8eec2-931">En alternativ metod för att hämta platser i AzureFileShare har lagts till</span><span class="sxs-lookup"><span data-stu-id="8eec2-931">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="8eec2-932">ScheduleRunDays i SchedulePolicy-objekt har uppdaterats enligt tidszon</span><span class="sxs-lookup"><span data-stu-id="8eec2-932">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="8eec2-933">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="8eec2-933">Az.RedisCache</span></span>
* <span data-ttu-id="8eec2-934">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8eec2-934">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8eec2-935">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8eec2-935">Az.Resources</span></span>
* <span data-ttu-id="8eec2-936">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="8eec2-936">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="8eec2-937">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8eec2-937">Az.Sql</span></span>
* <span data-ttu-id="8eec2-938">Ersätt Monitor SDK-beroende med vanlig kod</span><span class="sxs-lookup"><span data-stu-id="8eec2-938">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="8eec2-939">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8eec2-939">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="8eec2-940">Förbättrad process för klassificering av flera kolumner.</span><span class="sxs-lookup"><span data-stu-id="8eec2-940">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="8eec2-941">Inkludera SKU-egenskaper (SKU-namn, serie, kapacitet) i svaret från Get-AzSqlServerServiceObjective och formatera som tabell som standard.</span><span class="sxs-lookup"><span data-stu-id="8eec2-941">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="8eec2-942">Möjlighet att använda Get-AzSqlServerServiceObjective efter plats utan att behöva en redan befintlig server i regionen.</span><span class="sxs-lookup"><span data-stu-id="8eec2-942">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="8eec2-943">Stöd för tidszonsparametern när hanterade instanser skapas.</span><span class="sxs-lookup"><span data-stu-id="8eec2-943">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="8eec2-944">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="8eec2-944">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8eec2-945">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8eec2-945">Az.Websites</span></span>
* <span data-ttu-id="8eec2-946">åtgärdar Set-AzWebApp och Set-AzWebAppSlot så att de inte tar bort taggar vid körning</span><span class="sxs-lookup"><span data-stu-id="8eec2-946">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="8eec2-947">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8eec2-947">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="8eec2-948">SDK för WebSites har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="8eec2-948">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="8eec2-949">Egenskapen AdminSiteName har tagits bort från PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="8eec2-949">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="8eec2-950">1.7.0 – april 2019</span><span class="sxs-lookup"><span data-stu-id="8eec2-950">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="8eec2-951">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="8eec2-951">Highlights since the last major release</span></span>
* <span data-ttu-id="8eec2-952">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="8eec2-952">General availability of `Az` module</span></span>
* <span data-ttu-id="8eec2-953">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="8eec2-953">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="8eec2-954">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="8eec2-954">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="8eec2-955">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="8eec2-955">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="8eec2-956">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="8eec2-956">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="8eec2-957">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="8eec2-957">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="8eec2-958">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="8eec2-958">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="8eec2-959">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8eec2-959">Az.Accounts</span></span>
* <span data-ttu-id="8eec2-960">Add-AzEnvironment och Set-AzEnvironment har uppdaterats för att godkänna parametern AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="8eec2-960">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="8eec2-961">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="8eec2-961">Az.AnalysisServices</span></span>
* <span data-ttu-id="8eec2-962">ServiceClient används i cmdletar för dataplan och den ursprungliga autentiseringslogiken har tagits bort</span><span class="sxs-lookup"><span data-stu-id="8eec2-962">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="8eec2-963">Add-AzureASAccount används för omslutning av Connect-AzAccount för att undvika en icke-bakåtkompatibel ändring</span><span class="sxs-lookup"><span data-stu-id="8eec2-963">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8eec2-964">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8eec2-964">Az.Automation</span></span>
* <span data-ttu-id="8eec2-965">Buggen för cmdleten New-AzAutomationSoftwareUpdateConfiguration för inkluderingar har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="8eec2-965">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="8eec2-966">Nu bör parametern IncludedKbNumber och IncludedPackageNameMask fungera.</span><span class="sxs-lookup"><span data-stu-id="8eec2-966">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="8eec2-967">Felkorrigering för dynamiska grupper i uppdateringshanteringen för azure automation</span><span class="sxs-lookup"><span data-stu-id="8eec2-967">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8eec2-968">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8eec2-968">Az.Compute</span></span>
* <span data-ttu-id="8eec2-969">Lägg till parametern HyperVGeneration i New-AzDiskConfig och New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="8eec2-969">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="8eec2-970">Tillåt att virtuella datorer skapas med galleribilder från andra klientorganisationer.</span><span class="sxs-lookup"><span data-stu-id="8eec2-970">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="8eec2-971">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="8eec2-971">Az.ContainerInstance</span></span>
* <span data-ttu-id="8eec2-972">Ett problem har åtgärdats i parametern -Command för New-AzContainerGroup som lade till ett avslutande tomt argument</span><span class="sxs-lookup"><span data-stu-id="8eec2-972">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8eec2-973">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8eec2-973">Az.DataFactory</span></span>
* <span data-ttu-id="8eec2-974">ADF .Net SDK-versionen har uppdaterats till 3.0.2</span><span class="sxs-lookup"><span data-stu-id="8eec2-974">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="8eec2-975">Cmdleten Set-AzDataFactoryV2 har uppdaterats med extra parametrar för inställningar som rör RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="8eec2-975">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8eec2-976">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8eec2-976">Az.Resources</span></span>
* <span data-ttu-id="8eec2-977">Förbättra hanteringen av providrar för Get-AzResource när parametrarna -ResourceId eller -ResourceGroupName, -Name och -ResourceType tillhandahålls</span><span class="sxs-lookup"><span data-stu-id="8eec2-977">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="8eec2-978">Förbättra felhanteringen för ”Test-AzDeployment” och ”Test-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="8eec2-978">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="8eec2-979">Hantera fel utanför distributionsvalideringen och ta med dem i kommandoutdata istället</span><span class="sxs-lookup"><span data-stu-id="8eec2-979">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="8eec2-980">Mer information här: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="8eec2-980">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="8eec2-981">Lägg till växlingsparametern -IgnoreDynamicParameters till en uppsättning av cmdletar för distribution för att hoppa över fråga i skript och jobbscenarier</span><span class="sxs-lookup"><span data-stu-id="8eec2-981">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="8eec2-982">Mer information här: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="8eec2-982">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="8eec2-983">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8eec2-983">Az.Sql</span></span>
* <span data-ttu-id="8eec2-984">Stöd för dataklassificering av databaser.</span><span class="sxs-lookup"><span data-stu-id="8eec2-984">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8eec2-985">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8eec2-985">Az.Storage</span></span>
* <span data-ttu-id="8eec2-986">Rapportera detaljfel när lagringskontext skapas med parametern -UseConnectedAccount, men utan inloggning på Azure-kontot</span><span class="sxs-lookup"><span data-stu-id="8eec2-986">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="8eec2-987">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="8eec2-987">New-AzStorageContext</span></span>
* <span data-ttu-id="8eec2-988">Stöd för att hantera Blob Service-egenskaper för ett angivet lagringskonto med API:et för hanteringsplan</span><span class="sxs-lookup"><span data-stu-id="8eec2-988">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="8eec2-989">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="8eec2-989">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="8eec2-990">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="8eec2-990">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="8eec2-991">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="8eec2-991">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="8eec2-992">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="8eec2-992">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="8eec2-993">Stöd för -AsJob-cmdletar för att ladda upp och ladda ned blobar och filer</span><span class="sxs-lookup"><span data-stu-id="8eec2-993">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="8eec2-994">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="8eec2-994">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="8eec2-995">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="8eec2-995">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="8eec2-996">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="8eec2-996">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="8eec2-997">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="8eec2-997">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="8eec2-998">1.6.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="8eec2-998">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="8eec2-999">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="8eec2-999">Highlights since the last major release</span></span>
* <span data-ttu-id="8eec2-1000">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="8eec2-1000">General availability of `Az` module</span></span>
* <span data-ttu-id="8eec2-1001">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="8eec2-1001">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="8eec2-1002">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="8eec2-1002">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="8eec2-1003">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="8eec2-1003">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="8eec2-1004">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="8eec2-1004">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="8eec2-1005">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="8eec2-1005">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="8eec2-1006">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="8eec2-1006">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8eec2-1007">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8eec2-1007">Az.Automation</span></span>
* <span data-ttu-id="8eec2-1008">Azure Automation – ändring av uppdateringshantering för stöd för de nya funktionerna:</span><span class="sxs-lookup"><span data-stu-id="8eec2-1008">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="8eec2-1009">Dynamisk gruppering</span><span class="sxs-lookup"><span data-stu-id="8eec2-1009">Dynamic grouping</span></span>
    * <span data-ttu-id="8eec2-1010">För-/efterskrift</span><span class="sxs-lookup"><span data-stu-id="8eec2-1010">Pre-Post script</span></span>
    * <span data-ttu-id="8eec2-1011">Inställning för omstart</span><span class="sxs-lookup"><span data-stu-id="8eec2-1011">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8eec2-1012">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8eec2-1012">Az.Compute</span></span>
* <span data-ttu-id="8eec2-1013">Åtgärda problem med sökvägsmatchning i Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="8eec2-1013">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="8eec2-1014">Uppdatera Compute-klientbibliotek till 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="8eec2-1014">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8eec2-1015">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8eec2-1015">Az.KeyVault</span></span>
* <span data-ttu-id="8eec2-1016">Stöd för jokertecken för KeyVault-cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="8eec2-1016">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8eec2-1017">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8eec2-1017">Az.Network</span></span>
* <span data-ttu-id="8eec2-1018">Lägg till stöd för Threat Intelligence för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="8eec2-1018">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="8eec2-1019">Lägg till resurs för brandväggsprincip på översta nivå och anpassade regler för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="8eec2-1019">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8eec2-1020">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8eec2-1020">Az.RecoveryServices</span></span>
* <span data-ttu-id="8eec2-1021">SnapshotRetentionInDays har lagts till i Azure-principen för virtuella datorer för stöd av Instant RP</span><span class="sxs-lookup"><span data-stu-id="8eec2-1021">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="8eec2-1022">Pipe-stöd för avregistrering av container har lagts till</span><span class="sxs-lookup"><span data-stu-id="8eec2-1022">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="8eec2-1023">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8eec2-1023">Az.Resources</span></span>
* <span data-ttu-id="8eec2-1024">Uppdatera stöd för jokertecken för Get-AzResource och Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8eec2-1024">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="8eec2-1025">Uppdatera autentiseringsuppgifter som används vid allmänna anrop till ARM</span><span class="sxs-lookup"><span data-stu-id="8eec2-1025">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="8eec2-1026">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8eec2-1026">Az.Sql</span></span>
* <span data-ttu-id="8eec2-1027">Cmdlet-parametern (ExcludeDetectionType) för Hotidentifiering ändrades från DetectionType till sträng[] för att framtidssäkra den när nya DetectionTypes läggs till, och även för att stödja automatisk ifyllning.</span><span class="sxs-lookup"><span data-stu-id="8eec2-1027">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8eec2-1028">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8eec2-1028">Az.Storage</span></span>
* <span data-ttu-id="8eec2-1029">Stöd för att hämta/ange/ta bort hanteringsprincip på ett lagringskonto</span><span class="sxs-lookup"><span data-stu-id="8eec2-1029">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="8eec2-1030">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="8eec2-1030">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="8eec2-1031">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="8eec2-1031">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="8eec2-1032">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="8eec2-1032">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="8eec2-1033">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="8eec2-1033">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="8eec2-1034">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="8eec2-1034">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="8eec2-1035">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="8eec2-1035">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8eec2-1036">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8eec2-1036">Az.Websites</span></span>
* <span data-ttu-id="8eec2-1037">Åtgärda fel med ARM-mall som avbryter kloning av alla platser med 'New-AzWebApp -IncludeSourceWebAppSlots'</span><span class="sxs-lookup"><span data-stu-id="8eec2-1037">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="8eec2-1038">1.5.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="8eec2-1038">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8eec2-1039">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8eec2-1039">Az.Accounts</span></span>
* <span data-ttu-id="8eec2-1040">Lägg till kommandot Register-AzModule för stöd för AutoRest-genererade cmdletar</span><span class="sxs-lookup"><span data-stu-id="8eec2-1040">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="8eec2-1041">Uppdatera exempel för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="8eec2-1041">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8eec2-1042">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8eec2-1042">Az.Automation</span></span>
* <span data-ttu-id="8eec2-1043">Problem med att hämta vissa månadsscheman i flera Azure Automation-cmdletar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8eec2-1043">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="8eec2-1044">Åtgärda problem med att Get-AzAutomationDscNode bara returnerar de 20 översta noderna.</span><span class="sxs-lookup"><span data-stu-id="8eec2-1044">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="8eec2-1045">Nu returneras alla noder</span><span class="sxs-lookup"><span data-stu-id="8eec2-1045">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="8eec2-1046">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="8eec2-1046">Az.Cdn</span></span>
* <span data-ttu-id="8eec2-1047">Nya Powershell-cmdletar för att aktivera/inaktivera anpassade domän-HTTPS har lagts till och de gamla har gjorts inaktuella</span><span class="sxs-lookup"><span data-stu-id="8eec2-1047">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8eec2-1048">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8eec2-1048">Az.Compute</span></span>
* <span data-ttu-id="8eec2-1049">Lägg till stöd för jokertecken för Get-cmdletar</span><span class="sxs-lookup"><span data-stu-id="8eec2-1049">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8eec2-1050">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8eec2-1050">Az.DataFactory</span></span>
* <span data-ttu-id="8eec2-1051">ADF .Net SDK-versionen har uppdaterats till 3.0.1</span><span class="sxs-lookup"><span data-stu-id="8eec2-1051">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="8eec2-1052">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="8eec2-1052">Az.LogicApp</span></span>
* <span data-ttu-id="8eec2-1053">Åtgärda problemet med att ListWorkflows endast hämtar den första sidan med resultat</span><span class="sxs-lookup"><span data-stu-id="8eec2-1053">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8eec2-1054">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8eec2-1054">Az.Network</span></span>
* <span data-ttu-id="8eec2-1055">Lägg till stöd för jokertecken för Network-cmdletar</span><span class="sxs-lookup"><span data-stu-id="8eec2-1055">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8eec2-1056">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8eec2-1056">Az.RecoveryServices</span></span>
* <span data-ttu-id="8eec2-1057">Stöd har lagts till för SQL Server i virtuella Azure-datorer</span><span class="sxs-lookup"><span data-stu-id="8eec2-1057">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="8eec2-1058">SDK-uppdatering</span><span class="sxs-lookup"><span data-stu-id="8eec2-1058">SDK Update</span></span>
* <span data-ttu-id="8eec2-1059">Get-ProtectableItem-incheckning i VMappContainer har tagits bort</span><span class="sxs-lookup"><span data-stu-id="8eec2-1059">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="8eec2-1060">Name och ServerName har lagts till som parametrar för Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="8eec2-1060">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="8eec2-1061">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8eec2-1061">Az.Resources</span></span>
* <span data-ttu-id="8eec2-1062">Lägg till parametern `-TemplateObject` i cmdletar för distribution</span><span class="sxs-lookup"><span data-stu-id="8eec2-1062">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="8eec2-1063">Mer information här: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="8eec2-1063">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="8eec2-1064">Åtgärda problem med piping av resultatet i `Get-AzResource` till `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="8eec2-1064">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="8eec2-1065">Mer information här: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="8eec2-1065">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="8eec2-1066">Åtgärda problem med ändring av JSON-datatyp när `Set-AzResource` körs</span><span class="sxs-lookup"><span data-stu-id="8eec2-1066">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="8eec2-1067">Mer information här: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="8eec2-1067">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="8eec2-1068">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8eec2-1068">Az.Sql</span></span>
* <span data-ttu-id="8eec2-1069">AuditingEndpointsCommunicator uppdateras.</span><span class="sxs-lookup"><span data-stu-id="8eec2-1069">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="8eec2-1070">Åtgärdar beteendet hos ett gränsscenario när nya diagnostikinställningar skapas.</span><span class="sxs-lookup"><span data-stu-id="8eec2-1070">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8eec2-1071">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8eec2-1071">Az.Storage</span></span>
* <span data-ttu-id="8eec2-1072">Stöd för BlockBlobStorage när Storage-konto skapas      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8eec2-1072">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="8eec2-1073">1.4.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="8eec2-1073">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="8eec2-1074">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="8eec2-1074">Az.AnalysisServices</span></span>
* <span data-ttu-id="8eec2-1075">Inaktuell AddAzureASAccount-cmdlet</span><span class="sxs-lookup"><span data-stu-id="8eec2-1075">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8eec2-1076">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8eec2-1076">Az.Automation</span></span>
* <span data-ttu-id="8eec2-1077">Hjälpen för Import-AzAutomationDscNodeConfiguration har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="8eec2-1077">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="8eec2-1078">Konfigurationsnamnsvalidering har lagts till i cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="8eec2-1078">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="8eec2-1079">Förbättrad felhantering för cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="8eec2-1079">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="8eec2-1080">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8eec2-1080">Az.CognitiveServices</span></span>
* <span data-ttu-id="8eec2-1081">CustomSubdomainName har lagts till som en ny valfri parameter för New-AzCognitiveServicesAccount, som används för att ange underdomän för resursen.</span><span class="sxs-lookup"><span data-stu-id="8eec2-1081">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8eec2-1082">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8eec2-1082">Az.Compute</span></span>
* <span data-ttu-id="8eec2-1083">Problemet med ID-parameteruppsättningar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8eec2-1083">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="8eec2-1084">Get-AzVMExtension har uppdaterats så att alla installerade tillägg visas om parametern Name inte har angetts</span><span class="sxs-lookup"><span data-stu-id="8eec2-1084">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="8eec2-1085">Parametrarna Tag och ResourceId har lagts till i cmdleten Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="8eec2-1085">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="8eec2-1086">Get-AzVmssVM utan instans-ID och med InstanceView kan visa virtuella VMSS-datorer med instansvyn.</span><span class="sxs-lookup"><span data-stu-id="8eec2-1086">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8eec2-1087">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8eec2-1087">Az.DataLakeStore</span></span>
* <span data-ttu-id="8eec2-1088">Cmdletar har lagts till för uppräkning och återställning av borttagna objekt i ADL</span><span class="sxs-lookup"><span data-stu-id="8eec2-1088">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="8eec2-1089">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="8eec2-1089">Az.EventHub</span></span>
* <span data-ttu-id="8eec2-1090">Ny boolesk egenskap SkipEmptyArchives har lagts till i Skip Empty Archives i CaptureDescription-klassen i Eventhub</span><span class="sxs-lookup"><span data-stu-id="8eec2-1090">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="8eec2-1091">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8eec2-1091">Az.KeyVault</span></span>
* <span data-ttu-id="8eec2-1092">Taggning i Set-AzKeyVaultSecret har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8eec2-1092">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="8eec2-1093">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="8eec2-1093">Az.LogicApp</span></span>
* <span data-ttu-id="8eec2-1094">Grundläggande SKU har lagts till för Integrationskonton</span><span class="sxs-lookup"><span data-stu-id="8eec2-1094">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="8eec2-1095">XSLT 2.0, XSLT 3.0 och Flytande mappningstyper har lagts till</span><span class="sxs-lookup"><span data-stu-id="8eec2-1095">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="8eec2-1096">Nya cmdletar för integrationskontosammansättningar</span><span class="sxs-lookup"><span data-stu-id="8eec2-1096">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="8eec2-1097">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="8eec2-1097">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="8eec2-1098">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="8eec2-1098">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="8eec2-1099">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="8eec2-1099">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="8eec2-1100">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="8eec2-1100">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="8eec2-1101">Nya cmdletar för batchkonfiguration för integrationskonto</span><span class="sxs-lookup"><span data-stu-id="8eec2-1101">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="8eec2-1102">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="8eec2-1102">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="8eec2-1103">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="8eec2-1103">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="8eec2-1104">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="8eec2-1104">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="8eec2-1105">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="8eec2-1105">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="8eec2-1106">Logic App-SDK har uppdaterats till version 4.1.0</span><span class="sxs-lookup"><span data-stu-id="8eec2-1106">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8eec2-1107">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8eec2-1107">Az.Monitor</span></span>
* <span data-ttu-id="8eec2-1108">Hjälpen för Get-AzMetric har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="8eec2-1108">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8eec2-1109">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8eec2-1109">Az.Network</span></span>
* <span data-ttu-id="8eec2-1110">Hjälpexempel för Add-AzApplicationGatewayCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="8eec2-1110">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="8eec2-1111">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8eec2-1111">Az.OperationalInsights</span></span>
* <span data-ttu-id="8eec2-1112">Ytterligare stöd för datakällorna New och Get ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="8eec2-1112">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="8eec2-1113">Ny ApplicationInsights-typ har lagts till för att ge stöd för ”Get specific” och ”Get all” för ApplicationInsights-datakällor för angiven arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="8eec2-1113">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="8eec2-1114">Cmdleten New-AzOperationalInsightsApplicationInsightsDataSource har lagts till för att skapa datakälla med angivna parametrar för Application Insights-resurs: subscription Id, resourceGroupName och name.</span><span class="sxs-lookup"><span data-stu-id="8eec2-1114">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="8eec2-1115">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8eec2-1115">Az.Resources</span></span>
* <span data-ttu-id="8eec2-1116">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="8eec2-1116">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="8eec2-1117">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="8eec2-1117">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="8eec2-1118">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="8eec2-1118">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="8eec2-1119">Fel som gör att KeyCredentials inte kan skapas upprepade gånger har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8eec2-1119">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="8eec2-1120">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8eec2-1120">Az.Sql</span></span>
* <span data-ttu-id="8eec2-1121">Lägg till stöd för hyperskalanivån för SQL DB</span><span class="sxs-lookup"><span data-stu-id="8eec2-1121">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="8eec2-1122">Ett fel har åtgärdats där återställningen kunde misslyckas på grund av onödiga inställningsegenskaper i restore-förfrågan</span><span class="sxs-lookup"><span data-stu-id="8eec2-1122">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8eec2-1123">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8eec2-1123">Az.Websites</span></span>
* <span data-ttu-id="8eec2-1124">Rätt exempel i Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="8eec2-1124">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="8eec2-1125">1.3.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="8eec2-1125">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8eec2-1126">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8eec2-1126">Az.Accounts</span></span>
* <span data-ttu-id="8eec2-1127">Uppdatera till den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="8eec2-1127">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="8eec2-1128">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="8eec2-1128">Az.AnalysisServices</span></span>
<span data-ttu-id="8eec2-1129">Allmän tillgänglighet för Az.AnalysisServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="8eec2-1129">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8eec2-1130">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8eec2-1130">Az.Compute</span></span>
* <span data-ttu-id="8eec2-1131">AEM-tillägg: Lägg till stöd för UltraSSD-, P60-, P70- och P80-diskar</span><span class="sxs-lookup"><span data-stu-id="8eec2-1131">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="8eec2-1132">Uppdatera hjälpbeskrivning för Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="8eec2-1132">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="8eec2-1133">Uppdatera hjälpbeskrivning och exempel för Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="8eec2-1133">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8eec2-1134">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8eec2-1134">Az.RecoveryServices</span></span>
<span data-ttu-id="8eec2-1135">Allmän tillgänglighet för Az.RecoveryServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="8eec2-1135">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8eec2-1136">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8eec2-1136">Az.Resources</span></span>
* <span data-ttu-id="8eec2-1137">Korrigera taggar för resursgrupper</span><span class="sxs-lookup"><span data-stu-id="8eec2-1137">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="8eec2-1138">Mer information här: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="8eec2-1138">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="8eec2-1139">Åtgärda problem där `Get-AzureRmRoleAssignment` inte respekterar -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="8eec2-1139">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="8eec2-1140">Mer information här: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="8eec2-1140">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="8eec2-1141">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8eec2-1141">Az.Sql</span></span>
* <span data-ttu-id="8eec2-1142">Lägga till Get/Set-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="8eec2-1142">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="8eec2-1143">Åtgärda problem där ett nullref-undantag uppstår när du kör SQL-cmdletar och inte är inloggad på ett Azure-konto</span><span class="sxs-lookup"><span data-stu-id="8eec2-1143">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="8eec2-1144">Åtgärda nullref-undantag i Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="8eec2-1144">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="8eec2-1145">1.2.1 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="8eec2-1145">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8eec2-1146">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8eec2-1146">Az.Accounts</span></span>
* <span data-ttu-id="8eec2-1147">Version med rätt version av autentisering</span><span class="sxs-lookup"><span data-stu-id="8eec2-1147">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="8eec2-1148">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="8eec2-1148">Az.AnalysisServices</span></span>
* <span data-ttu-id="8eec2-1149">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="8eec2-1149">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8eec2-1150">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8eec2-1150">Az.RecoveryServices</span></span>
* <span data-ttu-id="8eec2-1151">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="8eec2-1151">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="8eec2-1152">1.2.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="8eec2-1152">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8eec2-1153">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8eec2-1153">Az.Accounts</span></span>
* <span data-ttu-id="8eec2-1154">Lägga till interaktiv autentisering och autentisering med användarnamn/lösenord för endast Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="8eec2-1154">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="8eec2-1155">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="8eec2-1155">Update incorrect online help URLs</span></span>
* <span data-ttu-id="8eec2-1156">Lägga till varningsmeddelande i PS Core för Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="8eec2-1156">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="8eec2-1157">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="8eec2-1157">Az.Aks</span></span>
* <span data-ttu-id="8eec2-1158">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="8eec2-1158">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8eec2-1159">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8eec2-1159">Az.Automation</span></span>
* <span data-ttu-id="8eec2-1160">Stöd för Python 2-runbookflöden har lagts till</span><span class="sxs-lookup"><span data-stu-id="8eec2-1160">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="8eec2-1161">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="8eec2-1161">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="8eec2-1162">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="8eec2-1162">Az.Cdn</span></span>
* <span data-ttu-id="8eec2-1163">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="8eec2-1163">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8eec2-1164">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8eec2-1164">Az.Compute</span></span>
* <span data-ttu-id="8eec2-1165">Lägga till cmdleten Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="8eec2-1165">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="8eec2-1166">Lägga till TempDisk-parameter i Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="8eec2-1166">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="8eec2-1167">Korrigera varningsmeddelande för New-AzVM</span><span class="sxs-lookup"><span data-stu-id="8eec2-1167">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="8eec2-1168">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="8eec2-1168">Az.ContainerRegistry</span></span>
* <span data-ttu-id="8eec2-1169">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="8eec2-1169">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8eec2-1170">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8eec2-1170">Az.DataFactory</span></span>
* <span data-ttu-id="8eec2-1171">ADF .Net SDK-versionen har uppdaterats till 3.0.0</span><span class="sxs-lookup"><span data-stu-id="8eec2-1171">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8eec2-1172">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8eec2-1172">Az.DataLakeStore</span></span>
* <span data-ttu-id="8eec2-1173">Åtgärda problem med ADLS-slutpunkt vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="8eec2-1173">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="8eec2-1174">Mer information här: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="8eec2-1174">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="8eec2-1175">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="8eec2-1175">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8eec2-1176">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8eec2-1176">Az.IotHub</span></span>
* <span data-ttu-id="8eec2-1177">Lägga till kodningsformat i cmdleten Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="8eec2-1177">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8eec2-1178">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8eec2-1178">Az.KeyVault</span></span>
* <span data-ttu-id="8eec2-1179">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="8eec2-1179">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8eec2-1180">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8eec2-1180">Az.Network</span></span>
* <span data-ttu-id="8eec2-1181">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="8eec2-1181">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="8eec2-1182">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8eec2-1182">Az.Resources</span></span>
* <span data-ttu-id="8eec2-1183">Åtgärda felaktiga exempel i referensdokumentationen ”New-AzADAppCredential” och ”New-AzADSpCredential”</span><span class="sxs-lookup"><span data-stu-id="8eec2-1183">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="8eec2-1184">Åtgärda problem där sökvägen för parametern ”-TemplateFile” inte omvandlas innan cmdletarna för distribution i resursgruppen körs</span><span class="sxs-lookup"><span data-stu-id="8eec2-1184">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="8eec2-1185">Az.Resources: Korrigera dokumentationen om standardvärdet för New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="8eec2-1185">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="8eec2-1186">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="8eec2-1186">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="8eec2-1187">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="8eec2-1187">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="8eec2-1188">Åtgärda formateringsproblemet med objektet ”PSResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="8eec2-1188">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="8eec2-1189">Mer information här: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="8eec2-1189">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="8eec2-1190">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8eec2-1190">Az.ServiceFabric</span></span>
* <span data-ttu-id="8eec2-1191">Återställ när ett certifikat läggs till i en Virtual Machine Scale Sets-modell men ett undantag genereras. Detta har gjorts för att åtgärda följande fel: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="8eec2-1191">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="8eec2-1192">Korrigera några felmeddelanden.</span><span class="sxs-lookup"><span data-stu-id="8eec2-1192">Fix some error messages.</span></span>
* <span data-ttu-id="8eec2-1193">Korrigering av skapande av kluster med ARM-mall som är standard för New-AzServiceFabriCluster som inte fungerade med migrering till Az.</span><span class="sxs-lookup"><span data-stu-id="8eec2-1193">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="8eec2-1194">Korrigering av tilläggning av kluster/programcertifikat så att endast VM Scale Sets som motsvarar klustret läggs till genom att kontrollera ID för klustret i tillägget.</span><span class="sxs-lookup"><span data-stu-id="8eec2-1194">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="8eec2-1195">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="8eec2-1195">Az.SignalR</span></span>
* <span data-ttu-id="8eec2-1196">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="8eec2-1196">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="8eec2-1197">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8eec2-1197">Az.Sql</span></span>
* <span data-ttu-id="8eec2-1198">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="8eec2-1198">Update incorrect online help URLs</span></span>
* <span data-ttu-id="8eec2-1199">Uppdaterad parameterbeskrivning för LicenseType-parameter med möjliga värden</span><span class="sxs-lookup"><span data-stu-id="8eec2-1199">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="8eec2-1200">Korrigering för att uppdatera hanterad instansidentitet som inte fungerar när det är den enda uppdaterade egenskapen</span><span class="sxs-lookup"><span data-stu-id="8eec2-1200">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="8eec2-1201">Stöd för anpassad sortering på hanterad instans</span><span class="sxs-lookup"><span data-stu-id="8eec2-1201">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8eec2-1202">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8eec2-1202">Az.Storage</span></span>
* <span data-ttu-id="8eec2-1203">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="8eec2-1203">Update incorrect online help URLs</span></span>
* <span data-ttu-id="8eec2-1204">Tillhandahåll detaljerat felmeddelande när en användare försöker hämta/konfigurera klassisk loggning/mått på ett Premium Storage-konto eftersom Premium Storage-kontot inte har stöd för klassisk loggning/mått.</span><span class="sxs-lookup"><span data-stu-id="8eec2-1204">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="8eec2-1205">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="8eec2-1205">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="8eec2-1206">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="8eec2-1206">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="8eec2-1207">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="8eec2-1207">Az.TrafficManager</span></span>
* <span data-ttu-id="8eec2-1208">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="8eec2-1208">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8eec2-1209">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8eec2-1209">Az.Websites</span></span>
* <span data-ttu-id="8eec2-1210">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="8eec2-1210">Update incorrect online help URLs</span></span>
* <span data-ttu-id="8eec2-1211">Korrigerar ”New-AzWebAppSSLBinding” så att certifikatet laddas upp till rätt resursgrupp och plats om appen finns i en ASE.</span><span class="sxs-lookup"><span data-stu-id="8eec2-1211">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="8eec2-1212">Korrigerar ”New-AzWebAppSSLBinding” så att taggarna inte skrivs över på en bindning av ett SSL-certifikat till en app</span><span class="sxs-lookup"><span data-stu-id="8eec2-1212">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="8eec2-1213">1.1.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="8eec2-1213">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8eec2-1214">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8eec2-1214">Az.Accounts</span></span>
* <span data-ttu-id="8eec2-1215">Lade till omfattningen ”Lokal” till Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="8eec2-1215">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8eec2-1216">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8eec2-1216">Az.Compute</span></span>
* <span data-ttu-id="8eec2-1217">Namn är nu valfritt i ID-parametern för Restart/Start/Stop/Remove/Set-AzVM och Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="8eec2-1217">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="8eec2-1218">Uppdaterade beskrivningen av ID i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="8eec2-1218">Updated the description of ID in help files</span></span>
* <span data-ttu-id="8eec2-1219">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8eec2-1219">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8eec2-1220">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8eec2-1220">Az.DataLakeStore</span></span>
* <span data-ttu-id="8eec2-1221">Uppdatera sdk-versionen av dataplanet till 1.1.14 för SDK-korrigeringar.</span><span class="sxs-lookup"><span data-stu-id="8eec2-1221">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="8eec2-1222">Korrigerade hanteringen av negativ accesstime och modificationtime för getfilestatus och liststatus; korrigera asynkront annulleringstoken</span><span class="sxs-lookup"><span data-stu-id="8eec2-1222">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="8eec2-1223">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="8eec2-1223">Az.EventGrid</span></span>
* <span data-ttu-id="8eec2-1224">Uppdaterat för användning av API-versionen 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="8eec2-1224">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="8eec2-1225">Uppdaterade följande cmdletar för att stödja nytt scenario i API-versionen 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="8eec2-1225">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="8eec2-1226">New-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="8eec2-1226">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="8eec2-1227">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="8eec2-1227">Event Time-To-Live,</span></span>
        - <span data-ttu-id="8eec2-1228">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="8eec2-1228">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="8eec2-1229">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="8eec2-1229">Dead letter endpoint.</span></span>
    - <span data-ttu-id="8eec2-1230">Update-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="8eec2-1230">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="8eec2-1231">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="8eec2-1231">Event Time-To-Live,</span></span>
        - <span data-ttu-id="8eec2-1232">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="8eec2-1232">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="8eec2-1233">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="8eec2-1233">Dead letter endpoint.</span></span>
* <span data-ttu-id="8eec2-1234">Lade till nya enum-värden (storageQueue och hybridConnection) för alternativet EndpointType i cmdletarna New-AzureRmEventGridSubscription och Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="8eec2-1234">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="8eec2-1235">Visa varningsmeddelanden om skapande eller uppdatering av händelseprenumerationen förväntas medföra manuell åtgärd från användaren.</span><span class="sxs-lookup"><span data-stu-id="8eec2-1235">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8eec2-1236">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8eec2-1236">Az.IotHub</span></span>
* <span data-ttu-id="8eec2-1237">Har uppdaterats till den senaste versionen av SDK:n lotHub</span><span class="sxs-lookup"><span data-stu-id="8eec2-1237">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="8eec2-1238">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="8eec2-1238">Az.LogicApp</span></span>
* <span data-ttu-id="8eec2-1239">Get-AzLogicApp visar en lista över alla som inte har angivet namn</span><span class="sxs-lookup"><span data-stu-id="8eec2-1239">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="8eec2-1240">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8eec2-1240">Az.Resources</span></span>
* <span data-ttu-id="8eec2-1241">Åtgärdade problem med parameteruppsättningen när parametrarna -ODataQuery och -ResourceId anges för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="8eec2-1241">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="8eec2-1242">Mer information här: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="8eec2-1242">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="8eec2-1243">Åtgärdade hantering av parametern -Custom i New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8eec2-1243">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="8eec2-1244">Korrigerade stavfel i New-AzDeployment-dokumentationen</span><span class="sxs-lookup"><span data-stu-id="8eec2-1244">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="8eec2-1245">Gjorde parametern -MailNickname obligatorisk för New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="8eec2-1245">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="8eec2-1246">Mer information här: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="8eec2-1246">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="8eec2-1247">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="8eec2-1247">Az.SignalR</span></span>
* <span data-ttu-id="8eec2-1248">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8eec2-1248">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="8eec2-1249">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8eec2-1249">Az.Sql</span></span>
* <span data-ttu-id="8eec2-1250">Konverterade lagringshanteringsklientens beroende av den normala SDK-implementeringen.</span><span class="sxs-lookup"><span data-stu-id="8eec2-1250">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8eec2-1251">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8eec2-1251">Az.Storage</span></span>
* <span data-ttu-id="8eec2-1252">Angav StorageAccountName för lagringskontext som det verkliga namnet på lagringskontot när det skapas med Sas Token, OAuth eller Anonymous</span><span class="sxs-lookup"><span data-stu-id="8eec2-1252">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="8eec2-1253">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="8eec2-1253">New-AzStorageContext</span></span>
* <span data-ttu-id="8eec2-1254">Skapade Sas Token för Blob Snapshot-objekt med parametern -FullUri, åtgärdade den returnerade URI:n så att den blir URI för ögonblicksbild</span><span class="sxs-lookup"><span data-stu-id="8eec2-1254">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="8eec2-1255">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="8eec2-1255">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8eec2-1256">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8eec2-1256">Az.Websites</span></span>
* <span data-ttu-id="8eec2-1257">Åtgärdade en bugg i datumparsningen i Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="8eec2-1257">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="8eec2-1258">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8eec2-1258">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="8eec2-1259">1.0.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="8eec2-1259">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="8eec2-1260">Allmänt</span><span class="sxs-lookup"><span data-stu-id="8eec2-1260">General</span></span>

- <span data-ttu-id="8eec2-1261">Allmän tillgänglighet för Az-modulen</span><span class="sxs-lookup"><span data-stu-id="8eec2-1261">General Availability of Az Module</span></span>
- <span data-ttu-id="8eec2-1262">Onlinehjälp för varje modul</span><span class="sxs-lookup"><span data-stu-id="8eec2-1262">Online help for each module</span></span>
- <span data-ttu-id="8eec2-1263">Mer information och en översikt finns på [Az-informationssidan](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="8eec2-1263">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="8eec2-1264">Information om hur du migrerar från AzureRM finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8eec2-1264">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="8eec2-1265">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8eec2-1265">Az.Accounts</span></span>
- <span data-ttu-id="8eec2-1266">Har ändrats från Az.Profile</span><span class="sxs-lookup"><span data-stu-id="8eec2-1266">Changed from Az.Profile</span></span>
- <span data-ttu-id="8eec2-1267">Fasta tabellformat för profil- och kontexttyper</span><span class="sxs-lookup"><span data-stu-id="8eec2-1267">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="8eec2-1268">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8eec2-1268">Az.ApiManagement</span></span>
- <span data-ttu-id="8eec2-1269">Korrigeringar för #7002</span><span class="sxs-lookup"><span data-stu-id="8eec2-1269">Fixes for #7002</span></span>
- <span data-ttu-id="8eec2-1270">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8eec2-1270">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="8eec2-1271">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="8eec2-1271">Az.Batch</span></span>
- <span data-ttu-id="8eec2-1272">Lade till möjligheten att se vilken version av Azure Batch Node Agent som körs på var och en av de virtuella datorerna i en pool, via den nya egenskapen `NodeAgentInformation` på `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="8eec2-1272">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="8eec2-1273">Standarden `Caching` för `PSDataDisk` är nu `ReadWrite` i stället för `None`.</span><span class="sxs-lookup"><span data-stu-id="8eec2-1273">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="8eec2-1274">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8eec2-1274">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="8eec2-1275">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="8eec2-1275">Az.Billing</span></span>
- <span data-ttu-id="8eec2-1276">Kombinerar cmdletarna för fakturering, förbrukning och UsageAggregates. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8eec2-1276">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="8eec2-1277">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="8eec2-1277">Az.CognitivServices</span></span>
- <span data-ttu-id="8eec2-1278">Lade till kompletterare för SkuName och Typem som är tillgängliga i New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="8eec2-1278">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="8eec2-1279">Tog bort parameteruppsättningen GetSkusWithAccountParamSetName från Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="8eec2-1279">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="8eec2-1280">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="8eec2-1280">Az.ContainerInstance</span></span>
- <span data-ttu-id="8eec2-1281">Stöd för ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="8eec2-1281">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="8eec2-1282">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="8eec2-1282">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="8eec2-1283">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8eec2-1283">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="8eec2-1284">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8eec2-1284">Az.DataLakeStore</span></span>
- <span data-ttu-id="8eec2-1285">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8eec2-1285">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="8eec2-1286">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8eec2-1286">Az.Monitor</span></span>
- <span data-ttu-id="8eec2-1287">Döpte om Az.Insights till Az.Monitor och andra mindre icke-bakåtkompatibla ändringar. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8eec2-1287">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="8eec2-1288">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8eec2-1288">Az.KeyVault</span></span>
- <span data-ttu-id="8eec2-1289">Tog bort den inaktuella egenskapen PurgeDisabled från utdatatyper</span><span class="sxs-lookup"><span data-stu-id="8eec2-1289">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="8eec2-1290">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="8eec2-1290">Az.MachineLearning</span></span>
- <span data-ttu-id="8eec2-1291">Inkluderade cmdletarna från modulen Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="8eec2-1291">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="8eec2-1292">Az.Media</span><span class="sxs-lookup"><span data-stu-id="8eec2-1292">Az.Media</span></span>
- <span data-ttu-id="8eec2-1293">Tog bort inaktuella -Tags-alias från New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="8eec2-1293">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="8eec2-1294">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8eec2-1294">Az.Network</span></span>
<span data-ttu-id="8eec2-1295">Stöd har lagts till för konfiguration av RewriteRuleSets i Application Gateway</span><span class="sxs-lookup"><span data-stu-id="8eec2-1295">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="8eec2-1296">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="8eec2-1296">New cmdlets added:</span></span>
        - <span data-ttu-id="8eec2-1297">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8eec2-1297">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="8eec2-1298">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8eec2-1298">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="8eec2-1299">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8eec2-1299">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="8eec2-1300">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8eec2-1300">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="8eec2-1301">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8eec2-1301">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="8eec2-1302">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="8eec2-1302">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="8eec2-1303">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="8eec2-1303">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="8eec2-1304">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="8eec2-1304">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="8eec2-1305">Cmdletar har uppdaterats med den valfria parametern -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8eec2-1305">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="8eec2-1306">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8eec2-1306">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="8eec2-1307">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="8eec2-1307">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="8eec2-1308">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="8eec2-1308">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="8eec2-1309">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8eec2-1309">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="8eec2-1310">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="8eec2-1310">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="8eec2-1311">New-AzureRmApplicationGatewayUrlPathMapConfig har lagt till KeyVault-stöd för Application Gateway med Identity.</span><span class="sxs-lookup"><span data-stu-id="8eec2-1311">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="8eec2-1312">Cmdletar har uppdaterats med den valfria parametern -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="8eec2-1312">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="8eec2-1313">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8eec2-1313">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="8eec2-1314">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8eec2-1314">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="8eec2-1315">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8eec2-1315">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="8eec2-1316">Cmdleten New-AzApplicationGateway har uppdaterats med den valfria parametern -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="8eec2-1316">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="8eec2-1317">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8eec2-1317">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="8eec2-1318">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8eec2-1318">Az.OperationalInsights</span></span>
- <span data-ttu-id="8eec2-1319">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8eec2-1319">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="8eec2-1320">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="8eec2-1320">Az.Profile</span></span>
- <span data-ttu-id="8eec2-1321">Modulnamnet har ändrats till Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8eec2-1321">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="8eec2-1322">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8eec2-1322">Az.RecoveryServices</span></span>
- <span data-ttu-id="8eec2-1323">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8eec2-1323">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="8eec2-1324">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8eec2-1324">Az.Resources</span></span>
- <span data-ttu-id="8eec2-1325">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8eec2-1325">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="8eec2-1326">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8eec2-1326">Az.ServiceFabric</span></span>
- <span data-ttu-id="8eec2-1327">Stöd för specificering av certifikat efter eget namn och tumavtryck</span><span class="sxs-lookup"><span data-stu-id="8eec2-1327">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="8eec2-1328">Information om fler icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8eec2-1328">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="8eec2-1329">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="8eec2-1329">Az.SIgnalR</span></span>
- <span data-ttu-id="8eec2-1330">Allmän tillgänglighet för PowerShell-cmdletar för SIgnalR</span><span class="sxs-lookup"><span data-stu-id="8eec2-1330">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="8eec2-1331">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8eec2-1331">Az.Sql</span></span>
- <span data-ttu-id="8eec2-1332">Lade till de nya identifieringstyperna Data_Exfiltration och Unsafe_Action i Threat Detection-cmdletar</span><span class="sxs-lookup"><span data-stu-id="8eec2-1332">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="8eec2-1333">Uppdaterade dokumentationsexempel för Sql Auditing-cmdletar</span><span class="sxs-lookup"><span data-stu-id="8eec2-1333">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="8eec2-1334">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8eec2-1334">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="8eec2-1335">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8eec2-1335">Az.Storage</span></span>
- <span data-ttu-id="8eec2-1336">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8eec2-1336">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="8eec2-1337">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8eec2-1337">Az.Websites</span></span>
- <span data-ttu-id="8eec2-1338">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8eec2-1338">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="8eec2-1339">0.7.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="8eec2-1339">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="8eec2-1340">Allmänt</span><span class="sxs-lookup"><span data-stu-id="8eec2-1340">General</span></span>

* <span data-ttu-id="8eec2-1341">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="8eec2-1341">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="8eec2-1342">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8eec2-1342">Az.Compute</span></span>

* <span data-ttu-id="8eec2-1343">Lade till stöd för UltraSSD och Galleriavbildningar i de enkla parameteruppsättningarna för `New-AzVm(ss)`-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="8eec2-1343">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="8eec2-1344">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8eec2-1344">Az.DataLakeStore</span></span>

* <span data-ttu-id="8eec2-1345">Åtgärdade avslutande snedstreck i domänen för adls-konto</span><span class="sxs-lookup"><span data-stu-id="8eec2-1345">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="8eec2-1346">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="8eec2-1346">Az.FrontDoor</span></span>

* <span data-ttu-id="8eec2-1347">Brutna länkar korrigerades</span><span class="sxs-lookup"><span data-stu-id="8eec2-1347">Fixed some broken links</span></span>
    - <span data-ttu-id="8eec2-1348">I artiklarna New-AzureRmFrontDoor och Set-AzureRmFrontDoor artiklar korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="8eec2-1348">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="8eec2-1349">I artikeln New-AzureRmFrontDoorManagedRuleObject korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="8eec2-1349">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="8eec2-1350">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8eec2-1350">Az.RecoveryServices</span></span>

* <span data-ttu-id="8eec2-1351">Lade till valideringar på klientsidan för Azure-filresurs med återställningsåtgärder.</span><span class="sxs-lookup"><span data-stu-id="8eec2-1351">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="8eec2-1352">Gjorde storageAccountName och storageAccountResourceGroupName valfritt för afs-återställning.</span><span class="sxs-lookup"><span data-stu-id="8eec2-1352">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="8eec2-1353">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8eec2-1353">Az.Resources</span></span>

* <span data-ttu-id="8eec2-1354">Korrigering för https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="8eec2-1354">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="8eec2-1355">Uppdaterade Get-AzureRmRoleAssignment så att prenumerationsomfattningen används om den anges vid begäran om klassiska administratörer.</span><span class="sxs-lookup"><span data-stu-id="8eec2-1355">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="8eec2-1356">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8eec2-1356">Az.Sql</span></span>

* <span data-ttu-id="8eec2-1357">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="8eec2-1357">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="8eec2-1358">Korrigerade ett problem med Get-AzureRmSqlDatabaseVulnerabilityAssessment med DotNet-kärna</span><span class="sxs-lookup"><span data-stu-id="8eec2-1358">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="8eec2-1359">Ändrade dokumentationen för hjälpmeddelanden som rör SQL Auditing-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="8eec2-1359">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="8eec2-1360">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8eec2-1360">Az.Storage</span></span>

* <span data-ttu-id="8eec2-1361">Lade till -EnableHierarchicalNamespace i New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8eec2-1361">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="8eec2-1362">Åtgärdade problemet med att cmdleten Copy File inte kunde återanvända källkontexten på målet om inte -DestContext angetts</span><span class="sxs-lookup"><span data-stu-id="8eec2-1362">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="8eec2-1363">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="8eec2-1363">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="8eec2-1364">Stöd för statisk webbplatskonfiguration</span><span class="sxs-lookup"><span data-stu-id="8eec2-1364">Support Static Website configuration</span></span>
    - <span data-ttu-id="8eec2-1365">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="8eec2-1365">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="8eec2-1366">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="8eec2-1366">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="8eec2-1367">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8eec2-1367">Az.Websites</span></span>

* <span data-ttu-id="8eec2-1368">Set-AzureRmWebApp och Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8eec2-1368">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="8eec2-1369">Ny parameter (-AzureStoragePath) har lagts till för att ange att Azure Storage-sökvägar ska monteras i containerappar i Windows och Linux.</span><span class="sxs-lookup"><span data-stu-id="8eec2-1369">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="8eec2-1370">Använder utdata från den nya cmdleten New-AzureRmWebAppAzureStoragePath som en parameter för att ange sökvägar för Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="8eec2-1370">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="8eec2-1371">0.6.1 – november 2018</span><span class="sxs-lookup"><span data-stu-id="8eec2-1371">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="8eec2-1372">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8eec2-1372">Az.ApiManagement</span></span>
* <span data-ttu-id="8eec2-1373">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="8eec2-1373">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="8eec2-1374">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8eec2-1374">Az.Automation</span></span>
* <span data-ttu-id="8eec2-1375">Swagger baserade Azure Automation-cmdletar</span><span class="sxs-lookup"><span data-stu-id="8eec2-1375">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="8eec2-1376">Cmdletar för Uppdateringshantering har lagts till</span><span class="sxs-lookup"><span data-stu-id="8eec2-1376">Added Update Management cmdlets</span></span>
* <span data-ttu-id="8eec2-1377">Cmdletar för källkontroll har lagts till</span><span class="sxs-lookup"><span data-stu-id="8eec2-1377">Added Source Control cmdlets</span></span>
* <span data-ttu-id="8eec2-1378">Remove-AzureRmAutomationHybridWorkerGroup-cmdlet har lagts till</span><span class="sxs-lookup"><span data-stu-id="8eec2-1378">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="8eec2-1379">Kommandot för DSC-registreringsnod har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8eec2-1379">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="8eec2-1380">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8eec2-1380">Az.Compute</span></span>
* <span data-ttu-id="8eec2-1381">Problem med SystemAssigned-identitet har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8eec2-1381">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="8eec2-1382">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="8eec2-1382">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="8eec2-1383">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="8eec2-1383">Az.ContainerInstance</span></span>
* <span data-ttu-id="8eec2-1384">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="8eec2-1384">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="8eec2-1385">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="8eec2-1385">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="8eec2-1386">uppdatera exempelbeskrivningen för marketplace-cmdletar</span><span class="sxs-lookup"><span data-stu-id="8eec2-1386">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="8eec2-1387">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8eec2-1387">Az.Network</span></span>
* <span data-ttu-id="8eec2-1388">Cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomErreller Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="8eec2-1388">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="8eec2-1389">ICMP tillbaka till stöd för Azure Firewall-nätverksprotokoll har lagts till</span><span class="sxs-lookup"><span data-stu-id="8eec2-1389">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="8eec2-1390">Uppdatera cmdlet Test-AzureRmNetworkWatcherConnectivity, lägga till verifiering av mål-id, adress och port.</span><span class="sxs-lookup"><span data-stu-id="8eec2-1390">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="8eec2-1391">Åtgärda problem med minnesanvändning i VirtualNetwork-karta</span><span class="sxs-lookup"><span data-stu-id="8eec2-1391">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="8eec2-1392">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="8eec2-1392">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="8eec2-1393">Åtgärda för att ändra principen för en skyddad fildelning.</span><span class="sxs-lookup"><span data-stu-id="8eec2-1393">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="8eec2-1394">Tidszonsprincipen har konverterats till versaler.</span><span class="sxs-lookup"><span data-stu-id="8eec2-1394">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="8eec2-1395">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="8eec2-1395">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="8eec2-1396">Exempel i New-AzureRmRecoveryServicesAsrProtectableItem har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8eec2-1396">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="8eec2-1397">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="8eec2-1397">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="8eec2-1398">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="8eec2-1398">Az.Relay</span></span>
* <span data-ttu-id="8eec2-1399">Valfri parameter -KeyValue till New-AzureRmRelayKey cmdlet har lagts till, vilket gör det möjligt för användare att tillhandahålla KeyValue.</span><span class="sxs-lookup"><span data-stu-id="8eec2-1399">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="8eec2-1400">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8eec2-1400">Az.Resources</span></span>
* <span data-ttu-id="8eec2-1401">Uppdatera hjälpdokumentation för resursidentitet kopplad till parametrar i `New-AzureRmPolicyAssignment` och `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="8eec2-1401">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="8eec2-1402">Lägg till ett exempel för New-AzureRmPolicyDefinition som använder -Metadata</span><span class="sxs-lookup"><span data-stu-id="8eec2-1402">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="8eec2-1403">Korrigera så att skiftläge behålls i taggnycklar i NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="8eec2-1403">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="8eec2-1404">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8eec2-1404">Az.ServiceFabric</span></span>
* <span data-ttu-id="8eec2-1405">Lägg till utfasningsmeddelanden för kommande icke-kompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="8eec2-1405">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="8eec2-1406">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8eec2-1406">Az.Sql</span></span>
* <span data-ttu-id="8eec2-1407">Nya cmdletar för CRUD-åtgärder på Azure Sql Database-hanterad instans och Azure Sql-hanterad databas</span><span class="sxs-lookup"><span data-stu-id="8eec2-1407">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="8eec2-1408">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="8eec2-1408">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="8eec2-1409">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="8eec2-1409">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="8eec2-1410">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="8eec2-1410">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="8eec2-1411">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="8eec2-1411">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="8eec2-1412">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="8eec2-1412">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="8eec2-1413">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="8eec2-1413">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="8eec2-1414">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="8eec2-1414">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="8eec2-1415">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="8eec2-1415">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="8eec2-1416">Hantering av utökad granskningsprincip på en server eller en databas har aktiverats.</span><span class="sxs-lookup"><span data-stu-id="8eec2-1416">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="8eec2-1417">Ny parameter (PredicateExpression) har lagts till för att aktivera filtrering av granskningsloggar.</span><span class="sxs-lookup"><span data-stu-id="8eec2-1417">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="8eec2-1418">Cmdletar har ändrats så att de använder SQL-klienter i stället för äldre klienter.</span><span class="sxs-lookup"><span data-stu-id="8eec2-1418">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="8eec2-1419">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="8eec2-1419">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="8eec2-1420">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="8eec2-1420">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="8eec2-1421">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="8eec2-1421">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="8eec2-1422">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="8eec2-1422">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="8eec2-1423">Problem med att använda Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings med lagringskontots namnparameter har korrigerats</span><span class="sxs-lookup"><span data-stu-id="8eec2-1423">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="8eec2-1424">0.5.0 – november 2018</span><span class="sxs-lookup"><span data-stu-id="8eec2-1424">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="8eec2-1425">Allmänt</span><span class="sxs-lookup"><span data-stu-id="8eec2-1425">General</span></span>
* <span data-ttu-id="8eec2-1426">Lade till resurskompletterare till många kärn-cmdletar – dessa gör att du kan stega genom befintliga resursnamn med TABB vid interaktiva anrop till cmdletar</span><span class="sxs-lookup"><span data-stu-id="8eec2-1426">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="8eec2-1427">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="8eec2-1427">Az.Profile</span></span>
* <span data-ttu-id="8eec2-1428">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="8eec2-1428">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="8eec2-1429">Bytte namn på parametern TenantId i cmdleten Connect-AzAccount till Tenant och lade till ett alias för TenantId</span><span class="sxs-lookup"><span data-stu-id="8eec2-1429">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="8eec2-1430">Uppdaterade TenantId-beskrivningen för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="8eec2-1430">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="8eec2-1431">Åtgärda felmeddelande för misslyckad inloggning när du tillhandahåller klientdomän</span><span class="sxs-lookup"><span data-stu-id="8eec2-1431">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="8eec2-1432">Åtgärda problem med att kontextnamn hamnar i konflikt för konton utan prenumerationer i klientorganisationen</span><span class="sxs-lookup"><span data-stu-id="8eec2-1432">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="8eec2-1433">Åtgärda problem med DataLake-slutpunkter vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="8eec2-1433">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="8eec2-1434">Åtgärdade problem med att Disconnect-AzAccount kastades om den inte anslöts</span><span class="sxs-lookup"><span data-stu-id="8eec2-1434">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="8eec2-1435">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8eec2-1435">Az.CognitiveServices</span></span>
* <span data-ttu-id="8eec2-1436">Lade till åtgärden Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="8eec2-1436">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8eec2-1437">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8eec2-1437">Az.Compute</span></span>
* <span data-ttu-id="8eec2-1438">Lade till cmdletarna Add-AzVmssVMDataDisk och Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="8eec2-1438">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="8eec2-1439">Get-AzVMImage visar AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="8eec2-1439">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="8eec2-1440">Åtgärdade att värdena för alternativen SetAzVMChefExtension -BootstrapOptions och -JsonAttribute inte angavs i json-format.</span><span class="sxs-lookup"><span data-stu-id="8eec2-1440">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8eec2-1441">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8eec2-1441">Az.DataLakeStore</span></span>
* <span data-ttu-id="8eec2-1442">Uppdatera DataLake-paketet till 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="8eec2-1442">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="8eec2-1443">Lägg till standardsamtidighet för flertrådade åtgärder.</span><span class="sxs-lookup"><span data-stu-id="8eec2-1443">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="8eec2-1444">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="8eec2-1444">Az.Insights</span></span>
* <span data-ttu-id="8eec2-1445">Åtgärdade problem #7267 (autoskalningsområde)</span><span class="sxs-lookup"><span data-stu-id="8eec2-1445">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="8eec2-1446">Problem med att uppräknade parametrar inte ställdes in ordentligt när du skapade en ny autoskalningsregel (de ställdes alltid in med standardvärdet).</span><span class="sxs-lookup"><span data-stu-id="8eec2-1446">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="8eec2-1447">Åtgärdade problem #7513 [Insights] Set-AzDiagnosticSetting kräver uttrycklig specifikation av kategorier när inställningar skapas</span><span class="sxs-lookup"><span data-stu-id="8eec2-1447">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="8eec2-1448">Nu kräver inte cmdleten uttrycklig anvisning av kategorierna för att aktiveras under skapande, d.v.s. den fungerar enligt beskrivning</span><span class="sxs-lookup"><span data-stu-id="8eec2-1448">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8eec2-1449">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8eec2-1449">Az.Network</span></span>
* <span data-ttu-id="8eec2-1450">PeeringType ändrades till en obligatorisk parameter för följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="8eec2-1450">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="8eec2-1451">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="8eec2-1451">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="8eec2-1452">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="8eec2-1452">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="8eec2-1453">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="8eec2-1453">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="8eec2-1454">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="8eec2-1454">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="8eec2-1455">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="8eec2-1455">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="8eec2-1456">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="8eec2-1456">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="8eec2-1457">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="8eec2-1457">Az.PolicyInsights</span></span>
* <span data-ttu-id="8eec2-1458">Cmdletar för principreparation har lagts till</span><span class="sxs-lookup"><span data-stu-id="8eec2-1458">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="8eec2-1459">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8eec2-1459">Az.Resources</span></span>
* <span data-ttu-id="8eec2-1460">Korrigering för https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="8eec2-1460">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="8eec2-1461">Tillåt att resurser listas med parametern -ResourceId för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="8eec2-1461">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="8eec2-1462">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8eec2-1462">Az.ServiceBus</span></span>
* <span data-ttu-id="8eec2-1463">Skrivskyddad MigrationState-egenskap har lagts till i PSServiceBusMigrationConfigurationAttributes, som hjälper till att hålla koll på migreringstillståndet.</span><span class="sxs-lookup"><span data-stu-id="8eec2-1463">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="8eec2-1464">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8eec2-1464">Az.ServiceFabric</span></span>
* <span data-ttu-id="8eec2-1465">Åtgärda att lägga till certifikat till Linux-Vmss.</span><span class="sxs-lookup"><span data-stu-id="8eec2-1465">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="8eec2-1466">Åtgärdade Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="8eec2-1466">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="8eec2-1467">Använd rätt tumavtryck från nya certifikat (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="8eec2-1467">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="8eec2-1468">Visa undantag korrekt (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="8eec2-1468">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="8eec2-1469">Åtgärdade Update-AzServiceFabricDurability så att klusterkonfigurationen uppdateras innan Vmss-åtgärden CreateOrUpdate påbörjas.</span><span class="sxs-lookup"><span data-stu-id="8eec2-1469">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="8eec2-1470">0.4.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="8eec2-1470">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="8eec2-1471">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="8eec2-1471">Az.Profile</span></span>
* <span data-ttu-id="8eec2-1472">Åtgärdade problemet med Get-AzSubscription i CloudShell</span><span class="sxs-lookup"><span data-stu-id="8eec2-1472">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="8eec2-1473">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="8eec2-1473">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8eec2-1474">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8eec2-1474">Az.Compute</span></span>
* <span data-ttu-id="8eec2-1475">Nya storlekar lades till i listan över godkända VM-storlekar för vilka accelererat nätverk kommer att aktiveras vid användning av den enkla parameteruppsättningen för New-AzVm</span><span class="sxs-lookup"><span data-stu-id="8eec2-1475">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="8eec2-1476">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="8eec2-1476">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8eec2-1477">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8eec2-1477">Az.DataLakeStore</span></span>
* <span data-ttu-id="8eec2-1478">Lägger till stöd för regler för virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="8eec2-1478">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="8eec2-1479">Get-AzDataLakeStoreVirtualNetworkRule: Hämtar eller listar regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8eec2-1479">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="8eec2-1480">Add-AzDataLakeStoreVirtualNetworkRule: Lägger till en regel för virtuellt nätverk i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="8eec2-1480">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="8eec2-1481">Set-AzDataLakeStoreVirtualNetworkRule: Ändrar den angivna regeln för virtuellt nätverk i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="8eec2-1481">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="8eec2-1482">Remove-AzDataLakeStoreVirtualNetworkRule: Tar bort en regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8eec2-1482">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8eec2-1483">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8eec2-1483">Az.Network</span></span>
* <span data-ttu-id="8eec2-1484">Skicka protokollvärdet till serverdelen för att uppdatera cmdleten Test-AzNetworkWatcherConnectivity.</span><span class="sxs-lookup"><span data-stu-id="8eec2-1484">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="8eec2-1485">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="8eec2-1485">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8eec2-1486">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8eec2-1486">Az.Resources</span></span>
* <span data-ttu-id="8eec2-1487">Åtgärdade problem där Get-AzRoleDefinition genererar ett oläsligt undantag (när standardprofilen inte innehåller någon prenumeration och ingen omfattning har angetts) genom att lägga till ett beskrivande undantag i scenariot.</span><span class="sxs-lookup"><span data-stu-id="8eec2-1487">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="8eec2-1488">Ställ in ”RoleDefinitionNameParameterSet” som standardparameteruppsättning.</span><span class="sxs-lookup"><span data-stu-id="8eec2-1488">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="8eec2-1489">0.3.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="8eec2-1489">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="8eec2-1490">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="8eec2-1490">Azure.Storage</span></span>
* <span data-ttu-id="8eec2-1491">Åtgärda fel där Kopiera blob/fil inte kopierar metadata när målplatsen har ett problem med metadata</span><span class="sxs-lookup"><span data-stu-id="8eec2-1491">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="8eec2-1492">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="8eec2-1492">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="8eec2-1493">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="8eec2-1493">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="8eec2-1494">Stöd för att hämta användningsinformation om en Storage-resurs för en specifik plats och för att lägga till ett varningsmeddelande för att hämta användningsinformation om en global Storage-resurs är inaktuellt.</span><span class="sxs-lookup"><span data-stu-id="8eec2-1494">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="8eec2-1495">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="8eec2-1495">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="8eec2-1496">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8eec2-1496">Az.CognitiveServices</span></span>
* <span data-ttu-id="8eec2-1497">Stöd för Get-AzCognitiveServicesAccountSkus utan ett befintligt konto.</span><span class="sxs-lookup"><span data-stu-id="8eec2-1497">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8eec2-1498">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8eec2-1498">Az.Compute</span></span>
* <span data-ttu-id="8eec2-1499">Åtgärdade fel där Get-AzVM -ResourceGroupName <rg> returnerar fler än 50 resultat om det behövs</span><span class="sxs-lookup"><span data-stu-id="8eec2-1499">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="8eec2-1500">Lade till ett exempel för SimpleParameterSet i hjälpen för cmdleten New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="8eec2-1500">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="8eec2-1501">Ett stavfel i förloppsmeddelandet för Azure Disk Encryption har korrigerats</span><span class="sxs-lookup"><span data-stu-id="8eec2-1501">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="8eec2-1502">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="8eec2-1502">Az.DataFactoryV2</span></span>
* <span data-ttu-id="8eec2-1503">ADF .Net SDK-versionen har uppdaterats till 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="8eec2-1503">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8eec2-1504">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8eec2-1504">Az.Network</span></span>
* <span data-ttu-id="8eec2-1505">Funktionalitet för NetworkProfile har lagts till.</span><span class="sxs-lookup"><span data-stu-id="8eec2-1505">Added NetworkProfile functionality.</span></span> <span data-ttu-id="8eec2-1506">nya cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="8eec2-1506">new cmdlets added</span></span>
    - <span data-ttu-id="8eec2-1507">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="8eec2-1507">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="8eec2-1508">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="8eec2-1508">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="8eec2-1509">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="8eec2-1509">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="8eec2-1510">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="8eec2-1510">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="8eec2-1511">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="8eec2-1511">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="8eec2-1512">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="8eec2-1512">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="8eec2-1513">Länk för tjänstassociering på modell för undernät har lagts till</span><span class="sxs-lookup"><span data-stu-id="8eec2-1513">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="8eec2-1514">Cmdletarna New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap och Remove-AzVirtualNetworkTap har lagts till</span><span class="sxs-lookup"><span data-stu-id="8eec2-1514">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="8eec2-1515">Cmdletarna Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig och Remove-AzNEtworkInterfaceTapConfig har lagts till</span><span class="sxs-lookup"><span data-stu-id="8eec2-1515">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="8eec2-1516">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="8eec2-1516">Az.RedisCache</span></span>
* <span data-ttu-id="8eec2-1517">Tillåt att alla strängar används som storleksparametrar framöver.</span><span class="sxs-lookup"><span data-stu-id="8eec2-1517">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="8eec2-1518">Lägg till P5 i popup-fönstret PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="8eec2-1518">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="8eec2-1519">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8eec2-1519">Az.Resources</span></span>
* <span data-ttu-id="8eec2-1520">Parametern -Mode som saknades i Set-AzPolicyDefinition har lagts till</span><span class="sxs-lookup"><span data-stu-id="8eec2-1520">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="8eec2-1521">Åtgärdade buggen för cmdleten Get-AzProviderOperation för åtgärder med ursprung som innehåller användare</span><span class="sxs-lookup"><span data-stu-id="8eec2-1521">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="8eec2-1522">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8eec2-1522">Az.Sql</span></span>
* <span data-ttu-id="8eec2-1523">Ett problem där vissa cmdletar för säkerhetskopiering inte kunde identifiera den aktuella azure-prenumerationen har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8eec2-1523">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8eec2-1524">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8eec2-1524">Az.Websites</span></span>
* <span data-ttu-id="8eec2-1525">Ny cmdlet: Get-AzWebAppContainerContinuousDeploymentUrl – Hämtar webhook-URL:en för kontinuerlig distribution av container</span><span class="sxs-lookup"><span data-stu-id="8eec2-1525">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="8eec2-1526">Nya cmdletar: New-AzWebAppContainerPSSession och Enter-WebAppContainerPSSession – Startar en PowerShell-fjärrsession i en containerapp för windows</span><span class="sxs-lookup"><span data-stu-id="8eec2-1526">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="8eec2-1527">0.2.0 – september 2018</span><span class="sxs-lookup"><span data-stu-id="8eec2-1527">0.2.0 - September 2018</span></span>
 <span data-ttu-id="8eec2-1528">Första versionen</span><span class="sxs-lookup"><span data-stu-id="8eec2-1528">Initial Release</span></span>