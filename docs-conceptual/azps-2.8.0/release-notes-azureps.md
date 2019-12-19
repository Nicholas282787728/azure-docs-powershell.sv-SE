---
title: Viktig information om Azure PowerShell
description: Lär dig mer om alla de senaste uppdateringarna för Azure PowerShell-modulerna.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/15/2019
ms.openlocfilehash: 98a24c805fbf43dd899119d43301b4261c1f60dc
ms.sourcegitcommit: f9445d1525eac8c165637e1a80fbc92b1ab005c2
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/16/2019
ms.locfileid: "75035769"
---
## <a name="280---october-2019"></a><span data-ttu-id="f8a4a-103">2.8.0 – oktober 2019</span><span class="sxs-lookup"><span data-stu-id="f8a4a-103">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="f8a4a-104">Allmänt</span><span class="sxs-lookup"><span data-stu-id="f8a4a-104">General</span></span>
* <span data-ttu-id="f8a4a-105">AZ. HealthcareApis 1.0.0-version</span><span class="sxs-lookup"><span data-stu-id="f8a4a-105">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f8a4a-106">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f8a4a-106">Az.Accounts</span></span>
* <span data-ttu-id="f8a4a-107">Uppdatera telemetri och URL-omskrivning för genererade moduler, korrigera Windows-enhetstester.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-107">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="f8a4a-108">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f8a4a-108">Az.ApiManagement</span></span>
* <span data-ttu-id="f8a4a-109">**Set-AzApiManagementApi** – Tillagt stöd för att uppdatera Api till ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="f8a4a-109">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="f8a4a-110">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="f8a4a-110">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f8a4a-111">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f8a4a-111">Az.Automation</span></span>
* <span data-ttu-id="f8a4a-112">Åtgärdade cmdleten New-AzureAutomationSoftwareUpdateConfiguration för parametern för inställning av Linux-omstart.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-112">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span> 

#### <a name="azbatch"></a><span data-ttu-id="f8a4a-113">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="f8a4a-113">Az.Batch</span></span>
* <span data-ttu-id="f8a4a-114">**Get-AzBatchNodeAgentSku** är inaktuell och ersätts av **Get-AzBatchSupportImage** i version 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-114">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f8a4a-115">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f8a4a-115">Az.Compute</span></span>
* <span data-ttu-id="f8a4a-116">Lägg till parametrarna Priority, EvictionPolicy och MaxPrice till cmdletarna New-AzVM och New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f8a4a-116">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="f8a4a-117">Korrigera varningsmeddelande och hjälpdokument för cmdletarna Add-AzVMAdditionalUnattendContent och Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="f8a4a-117">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="f8a4a-118">Åtgärda – skipVmBackup-undantag för virtuella Linux-datorer med hanterade diskar för Set-AzVMDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-118">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span> 
* <span data-ttu-id="f8a4a-119">Åtgärda fel i uppdatera krypteringsinställningarna i set-AzVMDiskEncryptionExtension, scenario i två steg.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-119">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f8a4a-120">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f8a4a-120">Az.DataFactory</span></span>
* <span data-ttu-id="f8a4a-121">Lägga till CRUD-kommandon för ADF V2-dataflödet: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow och Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-121">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="f8a4a-122">Lägger till åtgärdskommandon för ADF V2-dataflödesfelsökningssession: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand och Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-122">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="f8a4a-123">Uppdatera ADF .Net SDK-versionen till 4.2.0</span><span class="sxs-lookup"><span data-stu-id="f8a4a-123">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f8a4a-124">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f8a4a-124">Az.DataLakeStore</span></span>
* <span data-ttu-id="f8a4a-125">Korrigera kontovalidering så att konton med ”-” kan skickas utan domän</span><span class="sxs-lookup"><span data-stu-id="f8a4a-125">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="f8a4a-126">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="f8a4a-126">Az.HealthcareApis</span></span>
* <span data-ttu-id="f8a4a-127">PowerShell-versionen har uppdaterats till 1.0.0</span><span class="sxs-lookup"><span data-stu-id="f8a4a-127">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="f8a4a-128">Uppdaterade SDK-versionen till 1.0.2</span><span class="sxs-lookup"><span data-stu-id="f8a4a-128">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="f8a4a-129">Uppdatera i tester för att referera till en ny SDK-version</span><span class="sxs-lookup"><span data-stu-id="f8a4a-129">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="f8a4a-130">Utdatastrukturen har uppdaterats från kapslad till förenklad.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-130">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f8a4a-131">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f8a4a-131">Az.IotHub</span></span>
* <span data-ttu-id="f8a4a-132">Lägg till ny routningskälla: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="f8a4a-132">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="f8a4a-133">Mindre felkorrigering: Get-AzIothub returnerar inte subscriptionId</span><span class="sxs-lookup"><span data-stu-id="f8a4a-133">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span> 

#### <a name="azmonitor"></a><span data-ttu-id="f8a4a-134">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f8a4a-134">Az.Monitor</span></span>
* <span data-ttu-id="f8a4a-135">Nya åtgärdsgruppsmottagare har lagts till för New-AzActionGroupReceiver:   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="f8a4a-135">New action group receivers added for New-AzActionGroupReceiver:   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="f8a4a-136">Använd vanligt aviseringsschema som är aktiverat för mottagarna.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-136">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="f8a4a-137">Detta gäller inte för SMS, push för Azure-app, ITSM och röstmottagare</span><span class="sxs-lookup"><span data-stu-id="f8a4a-137">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="f8a4a-138">Webhooks har nu stöd för Azure Active Directory-autentisering.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-138">Webhooks now supports Azure active directory authentication.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f8a4a-139">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f8a4a-139">Az.Network</span></span>
* <span data-ttu-id="f8a4a-140">Lägg till ny cmdlet Get-AzAvailableServiceAlias som kan anropas för att hämta de alias som kan användas för tjänstslutpunktsprinciper.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-140">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="f8a4a-141">Stöd för tillägg av trafikväljare har lagts till i gatewayanslutningar för virtuella nätverk</span><span class="sxs-lookup"><span data-stu-id="f8a4a-141">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="f8a4a-142">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="f8a4a-142">New cmdlets added:</span></span>
        - <span data-ttu-id="f8a4a-143">New-AzIpsecTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="f8a4a-143">New-AzIpsecTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="f8a4a-144">Cmdletar har uppdaterats med den valfria parametern -TrafficSelectorPolicies</span><span class="sxs-lookup"><span data-stu-id="f8a4a-144">Cmdlets updated with optional parameter -TrafficSelectorPolicies</span></span>
        - <span data-ttu-id="f8a4a-145">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f8a4a-145">New-AzVirtualNetworkGatewayConnection</span></span>
        - <span data-ttu-id="f8a4a-146">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f8a4a-146">Set-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="f8a4a-147">Lägg till stöd för ESP- och AH-protokoll i konfiguration av nätverkssäkerhetsregler</span><span class="sxs-lookup"><span data-stu-id="f8a4a-147">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="f8a4a-148">Uppdaterade cmdletar:</span><span class="sxs-lookup"><span data-stu-id="f8a4a-148">Updated cmdlets:</span></span>
        - <span data-ttu-id="f8a4a-149">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f8a4a-149">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="f8a4a-150">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f8a4a-150">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="f8a4a-151">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f8a4a-151">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="f8a4a-152">Förbättra hanteringen av undantag i Cortex-cmdletar</span><span class="sxs-lookup"><span data-stu-id="f8a4a-152">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="f8a4a-153">Nya generationer och SKU:er för VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="f8a4a-153">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="f8a4a-154">Introducera nya generationer för VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-154">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="f8a4a-155">Introducera nya SKU:er med högt dataflöde för VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-155">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="f8a4a-156">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="f8a4a-156">Az.RedisCache</span></span>
* <span data-ttu-id="f8a4a-157">Uppdaterad referensdokumentation för ”set-AzRedisCache” för att inkludera saknade värden för parametern ”size”</span><span class="sxs-lookup"><span data-stu-id="f8a4a-157">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="f8a4a-158">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f8a4a-158">Az.Sql</span></span>
* <span data-ttu-id="f8a4a-159">Lägg till stöd för inställningen Active Directory administratör på den hanterade instansen</span><span class="sxs-lookup"><span data-stu-id="f8a4a-159">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f8a4a-160">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f8a4a-160">Az.Storage</span></span>
* <span data-ttu-id="f8a4a-161">Uppdatera Lagringsklientbibliotek till 11.1.0</span><span class="sxs-lookup"><span data-stu-id="f8a4a-161">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="f8a4a-162">Lista containrar med hanteringsplans-API, kommer att listas med NextPageLink</span><span class="sxs-lookup"><span data-stu-id="f8a4a-162">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="f8a4a-163">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="f8a4a-163">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="f8a4a-164">Lista lagringskonton från prenumerationen, kommer att listas med NextPageLink</span><span class="sxs-lookup"><span data-stu-id="f8a4a-164">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="f8a4a-165">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f8a4a-165">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="f8a4a-166">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="f8a4a-166">Az.StorageSync</span></span>
* <span data-ttu-id="f8a4a-167">Åtgärda problemet 9810 i Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-167">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f8a4a-168">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f8a4a-168">Az.Websites</span></span>
* <span data-ttu-id="f8a4a-169">Set-AzWebApp – uppdatering av ASP för en app misslyckades</span><span class="sxs-lookup"><span data-stu-id="f8a4a-169">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="f8a4a-170">2.7.0 – september 2019</span><span class="sxs-lookup"><span data-stu-id="f8a4a-170">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="f8a4a-171">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f8a4a-171">Az.ApiManagement</span></span>
* <span data-ttu-id="f8a4a-172">Uppdatera ”-Format”-parameterbeskrivningen i ”Set-AzApiManagementPolicy”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="f8a4a-172">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="f8a4a-173">Referenser för den föråldrade cmdleten ”Update-AzApiManagementDeployment” har tagits bort från referensdokumentationen.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-173">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="f8a4a-174">Använd ”Set-AzApiManagement” i stället.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-174">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f8a4a-175">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f8a4a-175">Az.Automation</span></span>
* <span data-ttu-id="f8a4a-176">Stavfel har korrigerats i exempel i referensdokumentationen för ”Register-AzAutomationDscNode”</span><span class="sxs-lookup"><span data-stu-id="f8a4a-176">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="f8a4a-177">Klargörande har lagts till om OS-begränsningar för Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="f8a4a-177">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="f8a4a-178">Null-referensundantag har korrigerats för -Wait-alternativet i Start-AzAutomationRunbook-cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-178">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f8a4a-179">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f8a4a-179">Az.Compute</span></span>
* <span data-ttu-id="f8a4a-180">Lägg till UploadSizeInBytes-parameter till New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="f8a4a-180">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="f8a4a-181">Lägg till Incremental-parameter till New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="f8a4a-181">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="f8a4a-182">Lägg till en funktion för virtuella datorer med låg prioritet:</span><span class="sxs-lookup"><span data-stu-id="f8a4a-182">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="f8a4a-183">MaxPrice-, EvictionPolicy- och Priority-parametrar har lagts till i New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-183">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="f8a4a-184">MaxPrice-parametern har lagts till i New-AzVmssConfig-, Update-AzVM- och Update-AzVmss-cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-184">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="f8a4a-185">Åtgärda problem med VM-referenser för Get-AzAvailabilitySet-cmdleten när alla tillgänglighetsuppsättningar i prenumerationen visas.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-185">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="f8a4a-186">Korrigera null-undantaget för Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-186">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="f8a4a-187">Korrigera VHD-metoden för sökning relativt till slut.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-187">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="f8a4a-188">Åtgärda UltraSSD-problem för New-AzVM och Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-188">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f8a4a-189">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f8a4a-189">Az.DataFactory</span></span>
* <span data-ttu-id="f8a4a-190">Lägger till 3 nya kommandon för ADF V2 – Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription och Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="f8a4a-190">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="f8a4a-191">ADF .Net SDK har uppdaterats till 4.1.3</span><span class="sxs-lookup"><span data-stu-id="f8a4a-191">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="f8a4a-192">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f8a4a-192">Az.HDInsight</span></span>
* <span data-ttu-id="f8a4a-193">Anrop för icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="f8a4a-193">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f8a4a-194">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f8a4a-194">Az.IotHub</span></span>
* <span data-ttu-id="f8a4a-195">Lägg till stöd för att anropa redundans för en IotHub till den geo-länkade katastrofåterställningsregionen.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-195">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="f8a4a-196">Lägg till stöd för att hantera meddelandeberikning för en IotHub.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-196">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="f8a4a-197">Nya cmdlet:ar är:</span><span class="sxs-lookup"><span data-stu-id="f8a4a-197">New cmdlets are:</span></span>
    - <span data-ttu-id="f8a4a-198">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="f8a4a-198">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="f8a4a-199">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="f8a4a-199">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="f8a4a-200">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="f8a4a-200">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="f8a4a-201">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="f8a4a-201">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f8a4a-202">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f8a4a-202">Az.Monitor</span></span>
* <span data-ttu-id="f8a4a-203">Pekar på den senaste Monitor SDK:n, dvs. 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="f8a4a-203">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="f8a4a-204">Lägger till bakåtkompatibla ändringar i Metrics-cmdletarna, dvs. enhetsuppräkningen stöder flera nya värden.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-204">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="f8a4a-205">Detta är skrivskyddade cmdletar, så det förekommer inga ändringar i inmatningen för cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-205">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="f8a4a-206">API-versionen för **ActionGroups**-begäranden är nu **2019-06-01**. Tidigare var den **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-206">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="f8a4a-207">Test av scenarier har uppdaterats för att anpassas till den här ändringen.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-207">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="f8a4a-208">Ett nytt obligatoriskt argument har lagts till för konstruktorerna för klasserna **EmailReceiver** och **WebhookReceiver** – ett booleskt värde med namnet **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-208">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="f8a4a-209">Värdet är för närvarande fast till **false** så att den här icke-bakåtkompatibla ändringen är dold från cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-209">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="f8a4a-210">**Obs!** Det här är en tillfällig ändring som måste verifieras av Alerts-teamet.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-210">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="f8a4a-211">Ordningen på argumenten för konstruktorn för klassen **Source** (relaterad till klassen **ScheduledQueryRuleSource**) har ändrats från den tidigare SDK:n.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-211">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="f8a4a-212">Den här ändringen krävde korrigering av två enhetstest: de kompilerades, men testerna skickades inte.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-212">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="f8a4a-213">Ordningen på argumenten för konstruktorn för klassen **AlertingAction** (relaterad till klassen **ScheduledQueryRuleSource**) har ändrats från den tidigare SDK:n.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-213">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="f8a4a-214">Den här ändringen krävde korrigering av två enhetstest: de kompilerades, men testerna skickades inte.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-214">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="f8a4a-215">Stöd för kriterier för dynamiskt tröskelvärde för måttavisering v2</span><span class="sxs-lookup"><span data-stu-id="f8a4a-215">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="f8a4a-216">New-AzMetricAlertRuleV2Criteria: skapar nu även kriterier för dynamiskt tröskelvärde</span><span class="sxs-lookup"><span data-stu-id="f8a4a-216">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="f8a4a-217">Add-AzMetricAlertRuleV2: accepterar nu även kriterier för dynamiskt tröskelvärde</span><span class="sxs-lookup"><span data-stu-id="f8a4a-217">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="f8a4a-218">Förbättringar i schemalagd frågeregel (SQR)</span><span class="sxs-lookup"><span data-stu-id="f8a4a-218">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="f8a4a-219">Cmdletar accepterar ”Location”-parameter i båda formaten, antingen platsen (t.ex. eastus) eller platsens visningsnamn (t.ex. USA, östra)</span><span class="sxs-lookup"><span data-stu-id="f8a4a-219">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="f8a4a-220">”Enabled”-parametern illustreras korrekt i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="f8a4a-220">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="f8a4a-221">Exempel för den valfria parametern ”ActionGroup” har lagts till</span><span class="sxs-lookup"><span data-stu-id="f8a4a-221">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="f8a4a-222">Förbättrade hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="f8a4a-222">Overall improved help files</span></span>
* <span data-ttu-id="f8a4a-223">Åtgärda bugg då omfattningstypen fastställs för ”Set-AzActionRule”</span><span class="sxs-lookup"><span data-stu-id="f8a4a-223">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f8a4a-224">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f8a4a-224">Az.Network</span></span>
* <span data-ttu-id="f8a4a-225">Korrigera felaktigt exempel i referensdokumentationen för ”New-AzApplicationGateway”</span><span class="sxs-lookup"><span data-stu-id="f8a4a-225">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="f8a4a-226">Lägg till anmärkning i ”Get-AzNetworkWatcherPacketCapture”-referensdokumentationen om hämtning av alla egenskaper för en paketinsamling</span><span class="sxs-lookup"><span data-stu-id="f8a4a-226">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="f8a4a-227">Exempel har korrigerats i ”Test-AzNetworkWatcherIPFlow”-referensdokumentationen för korrekt uppräkning av nätverkskort</span><span class="sxs-lookup"><span data-stu-id="f8a4a-227">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="f8a4a-228">Förbättrad tolkning av molnundantag för att visa eventuell ytterligare information</span><span class="sxs-lookup"><span data-stu-id="f8a4a-228">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="f8a4a-229">Förbättrad tolkning av molnundantag för att hantera ytterligare en typ av SDK-undantag</span><span class="sxs-lookup"><span data-stu-id="f8a4a-229">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="f8a4a-230">Felaktig mappning av säkerhetsregelmodeller har korrigerats</span><span class="sxs-lookup"><span data-stu-id="f8a4a-230">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="f8a4a-231">Egenskaper har lagts till för nätverksgränssnittet för funktionen Privat IP</span><span class="sxs-lookup"><span data-stu-id="f8a4a-231">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="f8a4a-232">Egenskapen ”PrivateEndpoint” har lagts till som en typ av PSResourceId till PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="f8a4a-232">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="f8a4a-233">Egenskapen ”PrivateLinkConnectionProperties” har lagts till som en typ av PSIpConfigurationConnectivityInformation till PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="f8a4a-233">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="f8a4a-234">Modellklassen PSIpConfigurationConnectivityInformation har lagts till</span><span class="sxs-lookup"><span data-stu-id="f8a4a-234">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="f8a4a-235">ApplicationRuleProtocolType ”mssql” har lagts till för Azure Firewall-resurs</span><span class="sxs-lookup"><span data-stu-id="f8a4a-235">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="f8a4a-236">MultiLink-stöd i virtuellt WAN</span><span class="sxs-lookup"><span data-stu-id="f8a4a-236">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="f8a4a-237">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="f8a4a-237">New cmdlets</span></span>
        - <span data-ttu-id="f8a4a-238">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="f8a4a-238">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="f8a4a-239">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="f8a4a-239">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="f8a4a-240">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="f8a4a-240">Updated cmdlet:</span></span>
        - <span data-ttu-id="f8a4a-241">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="f8a4a-241">New-VpnSite</span></span>
        - <span data-ttu-id="f8a4a-242">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="f8a4a-242">Update-VpnSite</span></span>
        - <span data-ttu-id="f8a4a-243">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="f8a4a-243">New-VpnConnection</span></span>
        - <span data-ttu-id="f8a4a-244">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="f8a4a-244">Update-VpnConnection</span></span>
* <span data-ttu-id="f8a4a-245">Dokument för vissa PowerShell-exempel har korrigerats så att Az-cmdletar används i stället för AzureRM-cmdletar</span><span class="sxs-lookup"><span data-stu-id="f8a4a-245">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f8a4a-246">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f8a4a-246">Az.RecoveryServices</span></span>
* <span data-ttu-id="f8a4a-247">Uppdatera AzureVMpolicy-objekt med ProtectedItemsCount-attribut</span><span class="sxs-lookup"><span data-stu-id="f8a4a-247">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="f8a4a-248">Ytterligare tester har lagts till för VM-princip och återställning av ursprungligt lagringskonto</span><span class="sxs-lookup"><span data-stu-id="f8a4a-248">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="f8a4a-249">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f8a4a-249">Az.Resources</span></span>
* <span data-ttu-id="f8a4a-250">Åtgärda fel där det inte gick att anropa New-AzRoleAssignment utan parametern Scope.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-250">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f8a4a-251">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f8a4a-251">Az.ServiceFabric</span></span>
* <span data-ttu-id="f8a4a-252">Stavfel har korrigerats i exempel för ”Update-AzServiceFabricReliability”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="f8a4a-252">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="f8a4a-253">Lägger till nya cmdletar för att hantera program och tjänster:</span><span class="sxs-lookup"><span data-stu-id="f8a4a-253">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="f8a4a-254">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="f8a4a-254">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="f8a4a-255">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="f8a4a-255">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="f8a4a-256">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="f8a4a-256">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="f8a4a-257">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="f8a4a-257">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="f8a4a-258">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="f8a4a-258">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="f8a4a-259">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="f8a4a-259">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="f8a4a-260">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="f8a4a-260">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="f8a4a-261">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="f8a4a-261">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="f8a4a-262">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="f8a4a-262">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="f8a4a-263">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="f8a4a-263">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="f8a4a-264">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="f8a4a-264">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="f8a4a-265">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="f8a4a-265">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="f8a4a-266">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="f8a4a-266">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="f8a4a-267">Service Fabric SDK har uppgraderats till version 1.2.0 som använder Service Fabric-resursprovidern med API-version 2019-03-01.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-267">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="f8a4a-268">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="f8a4a-268">Az.SignalR</span></span>
* <span data-ttu-id="f8a4a-269">Lägg till Update-, Restart-, CheckNameAvailability- och GetUsage-cmdletar</span><span class="sxs-lookup"><span data-stu-id="f8a4a-269">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="f8a4a-270">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f8a4a-270">Az.Sql</span></span>
* <span data-ttu-id="f8a4a-271">Uppdatera exempel i referensdokumentationen för ”Get-AzSqlElasticPool”</span><span class="sxs-lookup"><span data-stu-id="f8a4a-271">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="f8a4a-272">vCore-exempel för att skapa en elastisk pool (New-AzSqlElasticPool) har lagts till.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-272">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="f8a4a-273">Ta bort verifieringen av EmailAddresses och kontrollen som bekräftar att EmailAdmins inte är falskt när EmailAddresses är tomt i Set-AzSqlServerAdvancedThreatProtectionPolicy och Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="f8a4a-273">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="f8a4a-274">Server-/databasgranskningsinställningar kan tas bort när det finns flera diagnostikinställningar som aktiverar granskningskategorin.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-274">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="f8a4a-275">Åtgärda verifiering av e-postadresser i flera Sql Vulnerability Assessment-cmdletar (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting och Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="f8a4a-275">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f8a4a-276">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f8a4a-276">Az.Storage</span></span>
* <span data-ttu-id="f8a4a-277">Exempel i referensdokumentationen för ”Get-AzStorageAccountKey” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="f8a4a-277">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="f8a4a-278">Vid upp- och nedladdning av en Azure-fil kan SMB-egenskaperna för källfilen (t.ex. filattribut, tidpunkten då filen skapades och tidpunkten för den senaste skrivningen) sparas i målfilen</span><span class="sxs-lookup"><span data-stu-id="f8a4a-278">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="f8a4a-279">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="f8a4a-279">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="f8a4a-280">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="f8a4a-280">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="f8a4a-281">Korrigera problem med uppladdningen av blockblob med egenskaper/metadata för ImmutabilityPolicy i containrar.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-281">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="f8a4a-282">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="f8a4a-282">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="f8a4a-283">Stöd för hantering av Azure-filresurser med API för hanteringsplan</span><span class="sxs-lookup"><span data-stu-id="f8a4a-283">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="f8a4a-284">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="f8a4a-284">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="f8a4a-285">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="f8a4a-285">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="f8a4a-286">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="f8a4a-286">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="f8a4a-287">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="f8a4a-287">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f8a4a-288">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f8a4a-288">Az.Websites</span></span>
* <span data-ttu-id="f8a4a-289">Åtgärda problemet där webbapp-taggar togs bort när appen migrerades till en ny ASP</span><span class="sxs-lookup"><span data-stu-id="f8a4a-289">Fixing issue where webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="f8a4a-290">Åtgärda Publish-AzureWebapp så att det fungerar i Linux och Windows</span><span class="sxs-lookup"><span data-stu-id="f8a4a-290">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="f8a4a-291">Uppdatera exempel i ”Get-AzWebAppPublishingProfile”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="f8a4a-291">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="f8a4a-292">2.6.0 – augusti 2019</span><span class="sxs-lookup"><span data-stu-id="f8a4a-292">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="f8a4a-293">Allmänt</span><span class="sxs-lookup"><span data-stu-id="f8a4a-293">General</span></span>
* <span data-ttu-id="f8a4a-294">Åtgärdade diverse skrivfel i flera moduler</span><span class="sxs-lookup"><span data-stu-id="f8a4a-294">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f8a4a-295">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f8a4a-295">Az.Accounts</span></span>
* <span data-ttu-id="f8a4a-296">Stöd för användartilldelat MSI i Azure Functions-autentisering (#9479)</span><span class="sxs-lookup"><span data-stu-id="f8a4a-296">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="f8a4a-297">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="f8a4a-297">Az.Aks</span></span>
* <span data-ttu-id="f8a4a-298">Åtgärda problem med utdata för "Get-AzAks"</span><span class="sxs-lookup"><span data-stu-id="f8a4a-298">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="f8a4a-299">Mer information här: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="f8a4a-299">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="f8a4a-300">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f8a4a-300">Az.ApiManagement</span></span>
* <span data-ttu-id="f8a4a-301">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="f8a4a-301">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="f8a4a-302">Uppdatera .net-NuGet-versionen, som inte tillämpar begränsningar för productId, apiId och userId</span><span class="sxs-lookup"><span data-stu-id="f8a4a-302">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="f8a4a-303">**Get-AzApiManagementProduct** – Lade till stöd för frågekörning mot produkter via API.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-303">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="f8a4a-304">**New-AzApiManagementApiRevision** – Korrigering för problem där ApiRevisionDescription inte angavs vid skapande av ny API-revision https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="f8a4a-304">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="f8a4a-305">Åtgärdade skrivfel i modellen "PsApiManagementOAuth2AuthrozationServer" till "PsApiManagementOAuth2AuthorizationServer"</span><span class="sxs-lookup"><span data-stu-id="f8a4a-305">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="f8a4a-306">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="f8a4a-306">Az.Batch</span></span>
* <span data-ttu-id="f8a4a-307">Åtgärdade skrivfel i hjälpmeddelande och dokumentation till att skriva Windows med versaler</span><span class="sxs-lookup"><span data-stu-id="f8a4a-307">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="f8a4a-308">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f8a4a-308">Az.Cdn</span></span>
* <span data-ttu-id="f8a4a-309">Åtgärdade skrivfel i CDN-modulens konverteringshjälp</span><span class="sxs-lookup"><span data-stu-id="f8a4a-309">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f8a4a-310">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f8a4a-310">Az.Compute</span></span>
* <span data-ttu-id="f8a4a-311">Lägg till VmssId i New-AzVMConfig-cmdleten</span><span class="sxs-lookup"><span data-stu-id="f8a4a-311">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="f8a4a-312">Lägg till parametrarna TerminateScheduledEvents och TerminateScheduledEventNotBeforeTimeoutInMinutes i New-AzVmssConfig och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f8a4a-312">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="f8a4a-313">Lägg till egenskapen HyperVGeneration till avbildningsobjekt för virtuell dator</span><span class="sxs-lookup"><span data-stu-id="f8a4a-313">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="f8a4a-314">Lägg till funktioner för Host och HostGroup</span><span class="sxs-lookup"><span data-stu-id="f8a4a-314">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="f8a4a-315">Nya cmdletar:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="f8a4a-315">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="f8a4a-316">HostId-parametern läggs till i New-AzVMConfig och New-AzVM</span><span class="sxs-lookup"><span data-stu-id="f8a4a-316">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="f8a4a-317">Uppdatera exempel i "Invoke-AzVMRunCommand"-dokumentationen till att använda rätt parameternamn</span><span class="sxs-lookup"><span data-stu-id="f8a4a-317">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="f8a4a-318">Uppdatera "-VolumeType"-beskrivningen i referensdokumentationen för "set-AzVMDiskEncryptionExtension" och "set-AzVmssDiskEncryptionExtension"</span><span class="sxs-lookup"><span data-stu-id="f8a4a-318">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f8a4a-319">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f8a4a-319">Az.DataFactory</span></span>
* <span data-ttu-id="f8a4a-320">Åtgärda skrivfel till att använda versaler för "Windows" i "New-AzDataFactoryEncryptValue"-dokumentationen</span><span class="sxs-lookup"><span data-stu-id="f8a4a-320">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="f8a4a-321">Uppdaterade ADF .Net SDK-versionen till 4.1.2</span><span class="sxs-lookup"><span data-stu-id="f8a4a-321">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="f8a4a-322">Lägg till parametrarna "DataProxyIntegrationRuntimeName", "DataProxyStagingLinkedServiceName" och "DataProxyStagingPath" för "Set-AzureRmDataFactoryV2IntegrationRuntime"-cmd för att aktivera konfiguration av lokalt installerad integrationskörning som en proxy för SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="f8a4a-322">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="f8a4a-323">Uppdaterade PSTriggerRun till att visa utlöst pipeline, meddelande och egenskaper samt PSActivityRun till att visa aktivitetstypen</span><span class="sxs-lookup"><span data-stu-id="f8a4a-323">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f8a4a-324">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f8a4a-324">Az.DataLakeStore</span></span>
* <span data-ttu-id="f8a4a-325">Korrigering av frysning av Get-DataLakeStoreDeletedItem för fel eller fjärrundantag.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-325">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f8a4a-326">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f8a4a-326">Az.EventHub</span></span>
* <span data-ttu-id="f8a4a-327">Korrigering av problem #9658 : Skrivfel i parametern VirtualNteworkRule i Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="f8a4a-327">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="f8a4a-328">Korrigering av problem #9558 : Set-AzEventHubNamespace använder PATCH i stället för PUT</span><span class="sxs-lookup"><span data-stu-id="f8a4a-328">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="f8a4a-329">lade till parametern EnableKafka i Set-AzEventHubNamespace-cmdleten</span><span class="sxs-lookup"><span data-stu-id="f8a4a-329">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="f8a4a-330">Korrigering av problem #9786 : kan inte skapa en regel med Endast lyssna-behörighet</span><span class="sxs-lookup"><span data-stu-id="f8a4a-330">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="f8a4a-331">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="f8a4a-331">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="f8a4a-332">Åtgärdade skrivfel i dokumentation där "Azure" skrevs helt med gemener</span><span class="sxs-lookup"><span data-stu-id="f8a4a-332">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f8a4a-333">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f8a4a-333">Az.Monitor</span></span>
* <span data-ttu-id="f8a4a-334">Åtgärdade felaktigt parameternamn i hjälpdokumentationen</span><span class="sxs-lookup"><span data-stu-id="f8a4a-334">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f8a4a-335">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f8a4a-335">Az.Network</span></span>
* <span data-ttu-id="f8a4a-336">Uppdaterade New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="f8a4a-336">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="f8a4a-337">Gjorde parametern "PublicIpAddress" inaktuell eftersom den aldrig används på serversidan.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-337">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="f8a4a-338">Lade till den valfria parametern "Primary", som anger huruvida den aktuella IP-konfigurationen är den primära.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-338">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="f8a4a-339">Förbättrade hanteringen av felundantag för begärande från SDK – åtgärdar problemet att tidigare SDK-undantag inte hanteras på rätt sätt, vilket leder till att viktig felinformation inte visas</span><span class="sxs-lookup"><span data-stu-id="f8a4a-339">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="f8a4a-340">Justerade valideringslogiken för IPv6-IP-prefix till att kontrollera korrekt IPv6-prefixlängd.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-340">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="f8a4a-341">Uppdaterade Get-AzVirtualNetworkSubnetConfig: Lade till parameter som anges till get av undernätets resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-341">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="f8a4a-342">Uppdaterade beskrivningen av parametern Location för AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="f8a4a-342">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f8a4a-343">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f8a4a-343">Az.OperationalInsights</span></span>
* <span data-ttu-id="f8a4a-344">Uppdaterade dokumentation för "New-AzOperationalInsightsLinuxSyslogDataSource"</span><span class="sxs-lookup"><span data-stu-id="f8a4a-344">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="f8a4a-345">Lade till exempel</span><span class="sxs-lookup"><span data-stu-id="f8a4a-345">Added example</span></span>
    - <span data-ttu-id="f8a4a-346">Uppdaterade beskrivningen av parametern "-Name"</span><span class="sxs-lookup"><span data-stu-id="f8a4a-346">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="f8a4a-347">Lade till ett exempel för New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="f8a4a-347">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="f8a4a-348">Ändrade beskrivningen av parametern -Name för New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="f8a4a-348">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f8a4a-349">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f8a4a-349">Az.RecoveryServices</span></span>
* <span data-ttu-id="f8a4a-350">Uppdatera "Get-AzRecoveryServicesBackupJobDetail.md"</span><span class="sxs-lookup"><span data-stu-id="f8a4a-350">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="f8a4a-351">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f8a4a-351">Az.Resources</span></span>
* <span data-ttu-id="f8a4a-352">Lägg till stöd för den nya API-versionen från 2019-05-10 för Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="f8a4a-352">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="f8a4a-353">Lägg till stöd för "copy.count = 0" för variabler, resurser och egenskaper</span><span class="sxs-lookup"><span data-stu-id="f8a4a-353">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="f8a4a-354">Resurser med "condition = false" eller "copy.count = 0" tas bort i complete-läget</span><span class="sxs-lookup"><span data-stu-id="f8a4a-354">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="f8a4a-355">Lägg till ett exempel på tilldelning av princip på prenumerationsnivå i hjälpdokumentationen</span><span class="sxs-lookup"><span data-stu-id="f8a4a-355">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="f8a4a-356">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f8a4a-356">Az.ServiceBus</span></span>
* <span data-ttu-id="f8a4a-357">Korrigering av problem #9658 : Skrivfel i parametern VirtualNetworkRule i set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="f8a4a-357">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="f8a4a-358">Korrigering av problem #9786 : kan inte skapa en regel med Endast lyssna-behörighet</span><span class="sxs-lookup"><span data-stu-id="f8a4a-358">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="f8a4a-359">Lade till det nya kommandot "Test-AzServiceBusNameAvailability" för att kontrollera namntillgängligheten för kö och ämne</span><span class="sxs-lookup"><span data-stu-id="f8a4a-359">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="f8a4a-360">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f8a4a-360">Az.ServiceFabric</span></span>
* <span data-ttu-id="f8a4a-361">Åtgärda buggar med tillägg av nodtyps-cmdlet:</span><span class="sxs-lookup"><span data-stu-id="f8a4a-361">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="f8a4a-362">NullReferenceException-bugg när resursgrupp hade annan vmss som inte är relaterad till Service Fabric-klustret.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-362">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="f8a4a-363">Åtgärdar problemet: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="f8a4a-363">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="f8a4a-364">Åtgärda bugg där cmdleten misslyckades om virtualNetwork var i en annan resursgrupp än klustret.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-364">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="f8a4a-365">Åtgärdar problemet: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="f8a4a-365">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="f8a4a-366">AzServiceFabricApplicationCertificate-cmdleten görs inaktuell</span><span class="sxs-lookup"><span data-stu-id="f8a4a-366">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="f8a4a-367">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f8a4a-367">Az.Sql</span></span>
* <span data-ttu-id="f8a4a-368">Uppdatera dokumentation om gamla gransknings-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-368">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f8a4a-369">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f8a4a-369">Az.Storage</span></span>
* <span data-ttu-id="f8a4a-370">Uppdatera hjälpen för Get/Close-AzStorageFileHandle genom att lägga till fler scenarier i cmdlet-exempel och uppdatera parameterbeskrivningar</span><span class="sxs-lookup"><span data-stu-id="f8a4a-370">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="f8a4a-371">Stöd för StandardBlobTier i uppladdningsblob och kopieringsblob</span><span class="sxs-lookup"><span data-stu-id="f8a4a-371">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="f8a4a-372">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="f8a4a-372">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="f8a4a-373">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="f8a4a-373">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="f8a4a-374">Stöd för rehydratiseringsprioritet i kopieringsblob</span><span class="sxs-lookup"><span data-stu-id="f8a4a-374">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="f8a4a-375">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="f8a4a-375">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f8a4a-376">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f8a4a-376">Az.Websites</span></span>
* <span data-ttu-id="f8a4a-377">Lägg till klargöranden gällande parametern -AppSettings i Set-AzWebApp och Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f8a4a-377">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="f8a4a-378">2.5.0 – July 2019</span><span class="sxs-lookup"><span data-stu-id="f8a4a-378">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f8a4a-379">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f8a4a-379">Az.Accounts</span></span>
* <span data-ttu-id="f8a4a-380">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="f8a4a-380">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="f8a4a-381">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="f8a4a-381">Az.ApplicationInsights</span></span>
* <span data-ttu-id="f8a4a-382">Korrigera skrivfel i exempel i dokumentationen för Remove-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="f8a4a-382">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="f8a4a-383">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f8a4a-383">Az.Automation</span></span>
* <span data-ttu-id="f8a4a-384">Korrigera skrivfel i resurssträng</span><span class="sxs-lookup"><span data-stu-id="f8a4a-384">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="f8a4a-385">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f8a4a-385">Az.CognitiveServices</span></span>
* <span data-ttu-id="f8a4a-386">Stöd för NetworkRuleSet har lagts till.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-386">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f8a4a-387">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f8a4a-387">Az.Compute</span></span>
* <span data-ttu-id="f8a4a-388">Lägg till saknade egenskaper (ComputerName, OsName, OsVersion och HyperVGeneration) för visningsobjekt i den virtuella datorinstansen.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-388">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="f8a4a-389">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f8a4a-389">Az.ContainerRegistry</span></span>
* <span data-ttu-id="f8a4a-390">Åtgärda skrivfel i Remove-AzContainerRegistryReplication för parametern Replication</span><span class="sxs-lookup"><span data-stu-id="f8a4a-390">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="f8a4a-391">Mer information finns här: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="f8a4a-391">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f8a4a-392">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f8a4a-392">Az.DataFactory</span></span>
* <span data-ttu-id="f8a4a-393">ADF .Net SDK-versionen har uppdaterats till 4.1.0</span><span class="sxs-lookup"><span data-stu-id="f8a4a-393">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="f8a4a-394">Korrigera skrivfel i dokumentationen för Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="f8a4a-394">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f8a4a-395">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f8a4a-395">Az.EventHub</span></span>
* <span data-ttu-id="f8a4a-396">Ny cmmdlet har lagts till för att skapa SAS-token: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="f8a4a-396">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="f8a4a-397">verifierings- och felmeddelande har lagts till för authorizationrules-rättigheter om endast "hantera" har tilldelats</span><span class="sxs-lookup"><span data-stu-id="f8a4a-397">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f8a4a-398">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f8a4a-398">Az.KeyVault</span></span>
* <span data-ttu-id="f8a4a-399">Stöd har lagts till för att ange KeySize för certifikatprinciper</span><span class="sxs-lookup"><span data-stu-id="f8a4a-399">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="f8a4a-400">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="f8a4a-400">Az.LogicApp</span></span>
* <span data-ttu-id="f8a4a-401">Korrigering för Get-AzIntegrationAccountMap för att lista alla mappningstyper</span><span class="sxs-lookup"><span data-stu-id="f8a4a-401">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="f8a4a-402">Ny MapType-parameter har lagts till för filtrering</span><span class="sxs-lookup"><span data-stu-id="f8a4a-402">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="f8a4a-403">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="f8a4a-403">Az.ManagedServices</span></span>
* <span data-ttu-id="f8a4a-404">Stöd för API-versionen 2019-06-01 (GA) har lagts till</span><span class="sxs-lookup"><span data-stu-id="f8a4a-404">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f8a4a-405">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f8a4a-405">Az.Network</span></span>
* <span data-ttu-id="f8a4a-406">Lägg till stöd för privat slutpunkt och privat länktjänst</span><span class="sxs-lookup"><span data-stu-id="f8a4a-406">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="f8a4a-407">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="f8a4a-407">New cmdlets</span></span>
        - <span data-ttu-id="f8a4a-408">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f8a4a-408">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="f8a4a-409">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f8a4a-409">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="f8a4a-410">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f8a4a-410">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="f8a4a-411">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f8a4a-411">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="f8a4a-412">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f8a4a-412">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="f8a4a-413">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f8a4a-413">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="f8a4a-414">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="f8a4a-414">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="f8a4a-415">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f8a4a-415">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="f8a4a-416">Nedanstående kommandon för funktionen har uppdaterats: Flaggan PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies på undernätet i VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f8a4a-416">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="f8a4a-417">Uppdaterade New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="f8a4a-417">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="f8a4a-418">Valfri parameter har lagts till – PrivateEndpointNetworkPoliciesFlag som konfigurerar huruvida nätverksprinciper ska tillämpas på en privat slutpunkt i det här undernätet.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-418">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="f8a4a-419">Valfri parameter har lagts till – PrivateLinkServiceNetworkPoliciesFlag som konfigurerar huruvida nätverksprinciper ska tillämpas på en privat länktjänst i det här undernätet.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-419">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="f8a4a-420">AzPrivateLinkService för cmdlet-parametern ServiceName har bytt namn till Name med aliaset ServiceName för bakåtkompatibilitet</span><span class="sxs-lookup"><span data-stu-id="f8a4a-420">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="f8a4a-421">Aktivera ICMP-protokoll för konfiguration av nätverkssäkerhetsregler</span><span class="sxs-lookup"><span data-stu-id="f8a4a-421">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="f8a4a-422">Uppdaterade cmdletar</span><span class="sxs-lookup"><span data-stu-id="f8a4a-422">Updated cmdlets</span></span>
        - <span data-ttu-id="f8a4a-423">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f8a4a-423">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="f8a4a-424">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f8a4a-424">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="f8a4a-425">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f8a4a-425">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="f8a4a-426">Lägg till ConnectionProtocolType (Ikev1/Ikev2) som en konfigurerbar parameter för New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f8a4a-426">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="f8a4a-427">Lägg till PrivateIpAddressVersion i LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="f8a4a-427">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="f8a4a-428">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="f8a4a-428">Updated cmdlet:</span></span>
        - <span data-ttu-id="f8a4a-429">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f8a4a-429">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="f8a4a-430">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f8a4a-430">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="f8a4a-431">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f8a4a-431">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="f8a4a-432">Uppdatering av Application Gateway-kommandot New-AzApplicationGatewayProbeConfig för stöd av anpassad port i Probe</span><span class="sxs-lookup"><span data-stu-id="f8a4a-432">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="f8a4a-433">Uppdaterade New-AzApplicationGatewayProbeConfig: Den valfria parametern Port som används för avsökning i serverdelen har lagts till.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-433">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="f8a4a-434">Denna parameter gäller för SKU:erna Standard_V2 och WAF_V2.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-434">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f8a4a-435">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f8a4a-435">Az.OperationalInsights</span></span>
* <span data-ttu-id="f8a4a-436">Uppdaterade standardversionen för sparade sökningar till 1.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-436">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="f8a4a-437">Åtgärdade hantering av anpassad log null regex</span><span class="sxs-lookup"><span data-stu-id="f8a4a-437">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f8a4a-438">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f8a4a-438">Az.RecoveryServices</span></span>
* <span data-ttu-id="f8a4a-439">Uppdatera Get-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="f8a4a-439">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="f8a4a-440">Uppdatera Get-AzRecoveryServicesBackupContainer.md</span><span class="sxs-lookup"><span data-stu-id="f8a4a-440">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="f8a4a-441">Uppdatera Get-AzRecoveryServicesVault.md</span><span class="sxs-lookup"><span data-stu-id="f8a4a-441">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="f8a4a-442">Uppdatera Wait-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="f8a4a-442">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="f8a4a-443">Uppdatera Set-AzRecoveryServicesVaultContext.md</span><span class="sxs-lookup"><span data-stu-id="f8a4a-443">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="f8a4a-444">Uppdatera Get-AzRecoveryServicesBackupItem.md</span><span class="sxs-lookup"><span data-stu-id="f8a4a-444">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="f8a4a-445">Uppdatera Get-AzRecoveryServicesBackupRecoveryPoint.md</span><span class="sxs-lookup"><span data-stu-id="f8a4a-445">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="f8a4a-446">Uppdatera Restore-AzRecoveryServicesBackupItem.md</span><span class="sxs-lookup"><span data-stu-id="f8a4a-446">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="f8a4a-447">Uppdaterat tjänstanrop för avregistrering av container för Azure-filresurs</span><span class="sxs-lookup"><span data-stu-id="f8a4a-447">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="f8a4a-448">Uppdatera Set-AzRecoveryServicesAsrAlertSetting.md</span><span class="sxs-lookup"><span data-stu-id="f8a4a-448">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="f8a4a-449">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f8a4a-449">Az.Resources</span></span>
- <span data-ttu-id="f8a4a-450">Ta bort den cmdlet som saknas och som refereras i dokumentationen till New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f8a4a-450">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="f8a4a-451">Princip-cmdletar har uppdaterats så att de använder den nya API-versionen 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="f8a4a-451">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="f8a4a-452">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f8a4a-452">Az.ServiceBus</span></span>
* <span data-ttu-id="f8a4a-453">Ny cmmdlet har lagts till för att skapa SAS-token: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="f8a4a-453">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="f8a4a-454">verifierings- och felmeddelande har lagts till för authorizationrules-rättigheter om endast "hantera" har tilldelats</span><span class="sxs-lookup"><span data-stu-id="f8a4a-454">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="f8a4a-455">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f8a4a-455">Az.Sql</span></span>
* <span data-ttu-id="f8a4a-456">Åtgärda saknade exempel för Set-AzSqlDatabaseSecondary cmdlet</span><span class="sxs-lookup"><span data-stu-id="f8a4a-456">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="f8a4a-457">Åtgärda angivna återkommande genomsökningar för bedömning av säkerhetsrisk utan angivna e-postadresser</span><span class="sxs-lookup"><span data-stu-id="f8a4a-457">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="f8a4a-458">Korrigera ett skrivfel i ett varningsmeddelande.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-458">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f8a4a-459">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f8a4a-459">Az.Storage</span></span>
* <span data-ttu-id="f8a4a-460">Uppdatera exempel i referensdokumentationen för Get-AzStorageAccount så att rätt parameternamn används</span><span class="sxs-lookup"><span data-stu-id="f8a4a-460">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="f8a4a-461">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="f8a4a-461">Az.StorageSync</span></span>
* <span data-ttu-id="f8a4a-462">Lägger till cmdleten Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-462">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="f8a4a-463">Åtgärda problem 9551 så att TierFilesOlderThanDays föredras</span><span class="sxs-lookup"><span data-stu-id="f8a4a-463">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f8a4a-464">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f8a4a-464">Az.Websites</span></span>
* <span data-ttu-id="f8a4a-465">Åtgärdar ett fel där vissa SiteConfig-egenskaper inte returnerades av Get-AzWebApp och Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="f8a4a-465">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="f8a4a-466">Lägger till en ny platsparameter för Get-AzDeletedWebApp och Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="f8a4a-466">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="f8a4a-467">Åtgärdar ett fel i kloning av webbapp-platser som använder New-AzWebApp-IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="f8a4a-467">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="f8a4a-468">2.4.0 – juli 2019</span><span class="sxs-lookup"><span data-stu-id="f8a4a-468">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f8a4a-469">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f8a4a-469">Az.Accounts</span></span>
* <span data-ttu-id="f8a4a-470">Lägg till stöd för profil-cmdletar</span><span class="sxs-lookup"><span data-stu-id="f8a4a-470">Add support for profile cmdlets</span></span>
* <span data-ttu-id="f8a4a-471">Lägg till stöd för miljöer och dataplaner i genererade cmdletar</span><span class="sxs-lookup"><span data-stu-id="f8a4a-471">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="f8a4a-472">Åtgärda bugg där fel slutpunkt i vissa fall användes för cmdletar för dataplaner i Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="f8a4a-472">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="f8a4a-473">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="f8a4a-473">Az.Advisor</span></span>
* <span data-ttu-id="f8a4a-474">GA-version av Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="f8a4a-474">GA release of Az.Advisor</span></span>
* <span data-ttu-id="f8a4a-475">Den här modulen ingår nu som en del av `Az`-sammanslagningsmodulen</span><span class="sxs-lookup"><span data-stu-id="f8a4a-475">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="f8a4a-476">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f8a4a-476">Az.ApiManagement</span></span>
* <span data-ttu-id="f8a4a-477">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="f8a4a-477">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="f8a4a-478">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="f8a4a-478">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="f8a4a-479">Stöd för att fråga prenumerationer efter användare och produkt har lagts till</span><span class="sxs-lookup"><span data-stu-id="f8a4a-479">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="f8a4a-480">Stöd för att fråga med hjälp av omfång ”/”, ”/apis”, ”/apis/echo-api” har lagts till</span><span class="sxs-lookup"><span data-stu-id="f8a4a-480">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="f8a4a-481">Korrigering av problem https://github.com/Azure/azure-powershell/issues/9307 och https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="f8a4a-481">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="f8a4a-482">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="f8a4a-482">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="f8a4a-483">Stöd för att ange ”ApiVersion” och ”ApiVersionSetId” när API:er importeras har lagts till</span><span class="sxs-lookup"><span data-stu-id="f8a4a-483">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f8a4a-484">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f8a4a-484">Az.Automation</span></span>
* <span data-ttu-id="f8a4a-485">Bugg med cmdleten Set-AzAutomationConnectionFieldValue för att hantera strängvärde har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-485">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f8a4a-486">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f8a4a-486">Az.Compute</span></span>
* <span data-ttu-id="f8a4a-487">Lägg till parametern HyperVGeneration i New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="f8a4a-487">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f8a4a-488">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f8a4a-488">Az.DataFactory</span></span>
* <span data-ttu-id="f8a4a-489">Uppdaterar utdata från ADF-cmdletar som hämtar aktivitetskörningar, hämtar pipelinekörningar och hämtar utlösarkörningar för stöd för Select-Object-pipe.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-489">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="f8a4a-490">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="f8a4a-490">Az.EventGrid</span></span>
* <span data-ttu-id="f8a4a-491">Korrigera stavfel i dokumentation om ”New-AzEventGridSubscription”</span><span class="sxs-lookup"><span data-stu-id="f8a4a-491">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f8a4a-492">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f8a4a-492">Az.IotHub</span></span>
* <span data-ttu-id="f8a4a-493">Lägg till stöd för att återskapa principnycklar för auktorisering.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-493">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f8a4a-494">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f8a4a-494">Az.Network</span></span>
* <span data-ttu-id="f8a4a-495">”RoutingPreference” har lagts till i offentliga IP-taggar</span><span class="sxs-lookup"><span data-stu-id="f8a4a-495">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="f8a4a-496">Förbättra exempel för referensdokumentation om ”Get-AzNetworkServiceTag”</span><span class="sxs-lookup"><span data-stu-id="f8a4a-496">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f8a4a-497">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f8a4a-497">Az.PolicyInsights</span></span>
* <span data-ttu-id="f8a4a-498">Åtgärda problem med null-referens i Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="f8a4a-498">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="f8a4a-499">Mer information här: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="f8a4a-499">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f8a4a-500">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f8a4a-500">Az.OperationalInsights</span></span>
* <span data-ttu-id="f8a4a-501">Modellen för CustomLog-datakälla som returneras i Get-AzOperationalInsightsDataSource har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="f8a4a-501">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f8a4a-502">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f8a4a-502">Az.RecoveryServices</span></span>
* <span data-ttu-id="f8a4a-503">Kommandot get-policy för IaaSVM:er har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="f8a4a-503">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="f8a4a-504">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f8a4a-504">Az.Resources</span></span>
    - <span data-ttu-id="f8a4a-505">Korrigera hjälptext för den översta parametern i Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="f8a4a-505">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="f8a4a-506">Lägg till växlingsstöd på klientsidan för Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="f8a4a-506">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="f8a4a-507">Lägg till nya parametrar för Set-AzPolicyAssignment, -PolicyParameters och -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="f8a4a-507">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="f8a4a-508">En mängd dokument- och exempeluppdateringar för Policy-cmdletar</span><span class="sxs-lookup"><span data-stu-id="f8a4a-508">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="f8a4a-509">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f8a4a-509">Az.ServiceBus</span></span>
* <span data-ttu-id="f8a4a-510">Korrigering av problem #4938 – New-AzureRmServiceBusQueue returnerar BadRequest vid konfiguration av MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="f8a4a-510">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="f8a4a-511">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f8a4a-511">Az.Sql</span></span>
* <span data-ttu-id="f8a4a-512">Lägg till cmdletar för instansredundansgrupper från förhandsversion till offentlig version</span><span class="sxs-lookup"><span data-stu-id="f8a4a-512">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="f8a4a-513">Stöd för granskning för Azure SQL Server\Database med nya cmdletar.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-513">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="f8a4a-514">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="f8a4a-514">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="f8a4a-515">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="f8a4a-515">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="f8a4a-516">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="f8a4a-516">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="f8a4a-517">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="f8a4a-517">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="f8a4a-518">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="f8a4a-518">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="f8a4a-519">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="f8a4a-519">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="f8a4a-520">Ta bort begränsningar för e-post från inställningarna för sårbarhetsbedömning</span><span class="sxs-lookup"><span data-stu-id="f8a4a-520">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f8a4a-521">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f8a4a-521">Az.Storage</span></span>
* <span data-ttu-id="f8a4a-522">Ändra två parametrar ”-IndexDocument” och ”-ErrorDocument404Path” från ”krävs” till ”valfri” i cmdlet:</span><span class="sxs-lookup"><span data-stu-id="f8a4a-522">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="f8a4a-523">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="f8a4a-523">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="f8a4a-524">Uppdatera hjälpen för Get-AzStorageBlobContent genom att lägga till ett exempel</span><span class="sxs-lookup"><span data-stu-id="f8a4a-524">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="f8a4a-525">Visa mer felinformation när cmdleten misslyckas med StorageException</span><span class="sxs-lookup"><span data-stu-id="f8a4a-525">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="f8a4a-526">Stöd för att skapa eller uppdatera lagringskonto med Azure Files AAD DS-autentisering</span><span class="sxs-lookup"><span data-stu-id="f8a4a-526">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="f8a4a-527">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f8a4a-527">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="f8a4a-528">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f8a4a-528">Set-AzStorageAccount</span></span>
* <span data-ttu-id="f8a4a-529">Stöd för att lista eller stänga filreferenser för en filresurs, filkatalog eller en fil</span><span class="sxs-lookup"><span data-stu-id="f8a4a-529">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="f8a4a-530">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="f8a4a-530">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="f8a4a-531">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="f8a4a-531">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="f8a4a-532">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="f8a4a-532">Az.StorageSync</span></span>
* <span data-ttu-id="f8a4a-533">Den här modulen ingår nu som en del av `Az`-sammanslagningsmodulen</span><span class="sxs-lookup"><span data-stu-id="f8a4a-533">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="f8a4a-534">2.3.2 – juni 2019</span><span class="sxs-lookup"><span data-stu-id="f8a4a-534">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f8a4a-535">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f8a4a-535">Az.Accounts</span></span>
* <span data-ttu-id="f8a4a-536">Åtgärda bugg med felaktiga webbadresser som i vissa fall användes för Functions-anrop</span><span class="sxs-lookup"><span data-stu-id="f8a4a-536">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="f8a4a-537">Mer information här: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="f8a4a-537">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="f8a4a-538">Åtgärda problem med alias från AzureRM i Az-cmdletar</span><span class="sxs-lookup"><span data-stu-id="f8a4a-538">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="f8a4a-539">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="f8a4a-539">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="f8a4a-540">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="f8a4a-540">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f8a4a-541">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f8a4a-541">Az.Compute</span></span>
* <span data-ttu-id="f8a4a-542">Parameteruppsättningarna New-AzVm och New-AzVmss accepterar nu parametern ”ProximityPlacementGroup”.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-542">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="f8a4a-543">Stavfel i referensdokumentationen för ”New-AzVM” har korrigerats</span><span class="sxs-lookup"><span data-stu-id="f8a4a-543">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="f8a4a-544">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="f8a4a-544">Az.Dns</span></span>
* <span data-ttu-id="f8a4a-545">Stavfel i hjälpexempel för ”Set-AzDnsZone” har korrigerats.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-545">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="f8a4a-546">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="f8a4a-546">Az.EventGrid</span></span>
* <span data-ttu-id="f8a4a-547">Har uppdaterats för att använda API-versionen 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-547">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="f8a4a-548">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="f8a4a-548">New cmdlets:</span></span>
    - <span data-ttu-id="f8a4a-549">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="f8a4a-549">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="f8a4a-550">Skapar en ny Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-550">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="f8a4a-551">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="f8a4a-551">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="f8a4a-552">Hämtar information om en Event Grid-domän eller hämtar en lista med alla Event Grid-domäner i den aktuella Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-552">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="f8a4a-553">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="f8a4a-553">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="f8a4a-554">Tar bort en Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-554">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="f8a4a-555">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="f8a4a-555">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="f8a4a-556">Återskapar nyckeln för delad åtkomst för en Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-556">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="f8a4a-557">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="f8a4a-557">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="f8a4a-558">Hämtar de nycklar för delad åtkomst som används för att publicera händelser till en Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-558">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="f8a4a-559">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="f8a4a-559">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="f8a4a-560">Skapar ett nytt Azure Event Grid-domänämne.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-560">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="f8a4a-561">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="f8a4a-561">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="f8a4a-562">Hämtar information om ett Event Grid-domänämne eller hämtar en lista med alla Event Grid-domänämnen under en specifik Event Grid-domän i nuvarande Azure</span><span class="sxs-lookup"><span data-stu-id="f8a4a-562">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="f8a4a-563">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="f8a4a-563">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="f8a4a-564">Tar bort ett befintligt Azure Event Grid-domänämne.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-564">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="f8a4a-565">Uppdaterade cmdletar:</span><span class="sxs-lookup"><span data-stu-id="f8a4a-565">Updated cmdlets:</span></span>
    - <span data-ttu-id="f8a4a-566">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="f8a4a-566">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="f8a4a-567">Lägg till nya obligatoriska parametrar för att stödja piping för den nya Event Grid-domänen och Event Grid-domänämnet för att göra det möjligt att skapa nya händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-567">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="f8a4a-568">Lägg till nya obligatoriska parametrar för att ange det nya Event Grid-domännamnet och/eller namnet på Event Grid-domänämnet för att göra det möjligt att skapa nya händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-568">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="f8a4a-569">Lägg till ny parameteruppsättningar för domäner och domänämnen för att göra det möjligt att återanvända befintliga parametrar (t.ex. EndPointType, SubjectBeginsWith osv).</span><span class="sxs-lookup"><span data-stu-id="f8a4a-569">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="f8a4a-570">Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="f8a4a-570">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="f8a4a-571">Förfallodatum för händelseprenumeration</span><span class="sxs-lookup"><span data-stu-id="f8a4a-571">Event subscription expiration date,</span></span>
            - <span data-ttu-id="f8a4a-572">Avancerade filterparametrar.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-572">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="f8a4a-573">Lägg till ny uppräkning för servicebusqueue som mål.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-573">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="f8a4a-574">Tillåt inte användning av ”Alla” i alternativet -IncludedEventType och ersätt det med</span><span class="sxs-lookup"><span data-stu-id="f8a4a-574">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="f8a4a-575">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="f8a4a-575">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="f8a4a-576">Lägg till ny valfria parametrar (Top, ODataQuery och NextLink) för att stödja sidnumrering och filtrering av resultat.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-576">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="f8a4a-577">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="f8a4a-577">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="f8a4a-578">Lägg till nya obligatoriska parametrar för att stödja piping för en Event Grid-domän och Event Grid-domänämnen för att göra det möjligt att ta bort befintliga händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-578">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="f8a4a-579">Lägg till nya obligatoriska parametrar för att ange Event Grid-domännamnet och/eller namnet på Event Grid-domänämnet för att göra det möjligt att ta bort befintliga händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-579">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="f8a4a-580">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f8a4a-580">Az.FrontDoor</span></span>
* <span data-ttu-id="f8a4a-581">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="f8a4a-581">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="f8a4a-582">Lägg till stöd för transformeringar och nytt värde för automatisk komplettering för operatorer (RegEx)</span><span class="sxs-lookup"><span data-stu-id="f8a4a-582">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="f8a4a-583">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="f8a4a-583">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="f8a4a-584">Lägg till nya värden för automatisk komplettering</span><span class="sxs-lookup"><span data-stu-id="f8a4a-584">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f8a4a-585">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f8a4a-585">Az.Network</span></span>
* <span data-ttu-id="f8a4a-586">Lägg till stöd för resurs för virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="f8a4a-586">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="f8a4a-587">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="f8a4a-587">New cmdlets</span></span>
        - <span data-ttu-id="f8a4a-588">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="f8a4a-588">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="f8a4a-589">Lägg till AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="f8a4a-589">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="f8a4a-590">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="f8a4a-590">New cmdlets</span></span> 
        - <span data-ttu-id="f8a4a-591">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="f8a4a-591">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="f8a4a-592">Lägg till PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f8a4a-592">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="f8a4a-593">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="f8a4a-593">New cmdlets</span></span> 
        - <span data-ttu-id="f8a4a-594">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f8a4a-594">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="f8a4a-595">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f8a4a-595">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="f8a4a-596">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f8a4a-596">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="f8a4a-597">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="f8a4a-597">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="f8a4a-598">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f8a4a-598">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="f8a4a-599">Lägg till PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f8a4a-599">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="f8a4a-600">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="f8a4a-600">New cmdlets</span></span>
        - <span data-ttu-id="f8a4a-601">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f8a4a-601">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="f8a4a-602">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f8a4a-602">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="f8a4a-603">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f8a4a-603">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="f8a4a-604">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="f8a4a-604">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="f8a4a-605">Nedanstående kommandon för funktionen har uppdaterats: Flaggan UseLocalAzureIpAddress på VpnConnection</span><span class="sxs-lookup"><span data-stu-id="f8a4a-605">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="f8a4a-606">New-AzVpnConnection har uppdaterats: Den valfria parametern -UseLocalAzureIpAddress har lagts till för att visa att en lokal IP-adress i Azure ska användas som källadress när anslutningen initieras.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-606">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="f8a4a-607">Set-AzVpnConnection har uppdaterats: Den valfria parametern -UseLocalAzureIpAddress har lagts till för att visa att en lokal IP-adress i Azure ska användas som källadress när anslutningen initieras.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-607">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="f8a4a-608">Det skrivskyddade fältet PeeredConnections har lagts till i ExpressRoute-peering.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-608">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="f8a4a-609">Det skrivskyddade fältet GlobalReachEnabled har lagts till i ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-609">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="f8a4a-610">Ett attribut för icke-bakåtkompatibla ändringar har lagts till för att lyfta fram utfasning av fältet AllowGlobalReach i modellen ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f8a4a-610">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="f8a4a-611">Problem 8756 har åtgärdats: Fel vid användning av TargetListenerID med AzApplicationGatewayRedirectConfiguration-cmdletar</span><span class="sxs-lookup"><span data-stu-id="f8a4a-611">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="f8a4a-612">En bugg i New-AzApplicationGatewayPathRuleConfig som gjorde att regeluppsättningen för att återskapa inte kunde anges har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-612">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="f8a4a-613">Visningen av VirtualNetworkTaps i NetworkInterfaceIpConfiguration har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="f8a4a-613">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="f8a4a-614">Cortex Get-cmdletar för att visa en lista med alla delar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="f8a4a-614">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="f8a4a-615">Funktionen för att skapa VirtualHub-referenser för ExpressRouteGateways och VpnGateway har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="f8a4a-615">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="f8a4a-616">Stöd för tillgänglighetszoner i AzureFirewall och NatGateway har lagts till</span><span class="sxs-lookup"><span data-stu-id="f8a4a-616">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="f8a4a-617">Cmdleten Get-AzNetworkServiceTag har lagts till</span><span class="sxs-lookup"><span data-stu-id="f8a4a-617">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="f8a4a-618">Lägg till stöd för flera offentliga IP-adresser för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="f8a4a-618">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="f8a4a-619">Cmdleten New-AzFirewall har uppdaterats:</span><span class="sxs-lookup"><span data-stu-id="f8a4a-619">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="f8a4a-620">Parametern -PublicIpAddress som accepterar ett eller flera offentliga IP-adressobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="f8a4a-620">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="f8a4a-621">Parametern -VirtualNetwork som accepterar ett virtuellt nätverksobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="f8a4a-621">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="f8a4a-622">Metoderna AddPublicIpAddress och RemovePublicIpAddress har lagts till på brandväggsobjekt – dessa accepterar ett offentligt IP-adressobjekt som indata</span><span class="sxs-lookup"><span data-stu-id="f8a4a-622">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="f8a4a-623">Inaktuella parametrar -PublicIpName och -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="f8a4a-623">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="f8a4a-624">Nedanstående kommandon för funktionen har uppdaterats: Ange autentiseringsalternativ för VpnClient AAD till resurser för virtuella nätverksgatewayer.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-624">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="f8a4a-625">New-AzVirtualNetworkGateway har uppdaterats: De valfria parametrarna AadTenantUri, AadAudienceId och AadIssuerUri för att ange VpnClient AAD-autentiseringsalternativ på en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-625">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="f8a4a-626">Set-AzVirtualNetworkGateway har uppdaterats: De valfria parametrarna AadTenantUri, AadAudienceId och AadIssuerUri för att ange VpnClient AAD-autentiseringsalternativ på en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-626">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="f8a4a-627">Set-AzVirtualNetworkGateway har uppdaterats: Den valfria växelparametern RemoveAadAuthentication som tar bort VpnClient AAD-autentiseringsalternativ från en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-627">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f8a4a-628">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f8a4a-628">Az.OperationalInsights</span></span>
* <span data-ttu-id="f8a4a-629">Aktivera prisnivån **pergb2018** i kommandot ”New-AzureRmOperationalInsightsWorkspace”</span><span class="sxs-lookup"><span data-stu-id="f8a4a-629">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="f8a4a-630">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f8a4a-630">Az.Resources</span></span>
* <span data-ttu-id="f8a4a-631">Stöd för ytterligare alternativ för att exportera en mall</span><span class="sxs-lookup"><span data-stu-id="f8a4a-631">Support for additional Template Export options</span></span>
    - <span data-ttu-id="f8a4a-632">Lägg till parametern ”-SkipResourceNameParameterization” till Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f8a4a-632">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="f8a4a-633">Lägg till parametern ”-SkipAllParameterization” till Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f8a4a-633">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="f8a4a-634">Lägg till parametern ”-Resource” till Export-AzResourceGroup för exporterad resursfiltrering</span><span class="sxs-lookup"><span data-stu-id="f8a4a-634">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f8a4a-635">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f8a4a-635">Az.ServiceFabric</span></span>
* <span data-ttu-id="f8a4a-636">Åtgärda att fel tumavtryck används vid tilläggning av certifikat i ByExistingKeyVault i vissa fall</span><span class="sxs-lookup"><span data-stu-id="f8a4a-636">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="f8a4a-637">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f8a4a-637">Az.Sql</span></span>
* <span data-ttu-id="f8a4a-638">Åtgärda suffix för lagringsslutpunkt i Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="f8a4a-638">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="f8a4a-639">Åtgärda att aktivering av Advanced Data Security åsidosätter Advanced Threat Protection-princip</span><span class="sxs-lookup"><span data-stu-id="f8a4a-639">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="f8a4a-640">Nya cmdletar för Management.Sql som gör att kunderna kan lägga till nycklar för transparent datakryptering (TDE) och ange TDE-skydd för hanterade instanser</span><span class="sxs-lookup"><span data-stu-id="f8a4a-640">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="f8a4a-641">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="f8a4a-641">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="f8a4a-642">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="f8a4a-642">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="f8a4a-643">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="f8a4a-643">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="f8a4a-644">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="f8a4a-644">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="f8a4a-645">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="f8a4a-645">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f8a4a-646">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f8a4a-646">Az.Storage</span></span>
* <span data-ttu-id="f8a4a-647">Stöd för typerna FileStorage och SkuName Premium_ZRS när lagringskonton skapas</span><span class="sxs-lookup"><span data-stu-id="f8a4a-647">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="f8a4a-648">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f8a4a-648">New-AzStorageAccount</span></span>
* <span data-ttu-id="f8a4a-649">Beskrivningen av cmdleten för bloboföränderlighet har förtydligats</span><span class="sxs-lookup"><span data-stu-id="f8a4a-649">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="f8a4a-650">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="f8a4a-650">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f8a4a-651">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f8a4a-651">Az.Websites</span></span>
* <span data-ttu-id="f8a4a-652">Optimerar Get-AzWebAppCertificate för att filtrera efter resursgrupp på servern i stället för klienten</span><span class="sxs-lookup"><span data-stu-id="f8a4a-652">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="f8a4a-653">Lägger till växlingsparametern -UseDisasterRecovery till Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="f8a4a-653">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="f8a4a-654">2.2.0 – juni 2019</span><span class="sxs-lookup"><span data-stu-id="f8a4a-654">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="f8a4a-655">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f8a4a-655">Az.Cdn</span></span>
* <span data-ttu-id="f8a4a-656">Uppdaterade cmdletar för att ge stöd för rulesEngine-funktion baserat på API-version 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-656">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f8a4a-657">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f8a4a-657">Az.Compute</span></span>
* <span data-ttu-id="f8a4a-658">Lade till parameter `NoWait` som startar åtgärden och returnerar omedelbart, innan åtgärden har slutförts.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-658">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="f8a4a-659">Uppdaterade cmdletar:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="f8a4a-659">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f8a4a-660">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f8a4a-660">Az.EventHub</span></span>
* <span data-ttu-id="f8a4a-661">Korrigering för #9231 – Get-AzEventHubNamespace returnerar inga taggar</span><span class="sxs-lookup"><span data-stu-id="f8a4a-661">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="f8a4a-662">Korrigering för #9230 – Get-AzEventHubNamespace returnerar ResourceGroup istället för ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8a4a-662">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f8a4a-663">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f8a4a-663">Az.Network</span></span>
* <span data-ttu-id="f8a4a-664">Uppdatera ResourceId och InputObject för NAT-gateway</span><span class="sxs-lookup"><span data-stu-id="f8a4a-664">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="f8a4a-665">Lägg till alias för ResourceId och InputObject</span><span class="sxs-lookup"><span data-stu-id="f8a4a-665">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f8a4a-666">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f8a4a-666">Az.PolicyInsights</span></span>
* <span data-ttu-id="f8a4a-667">Åtgärda Null-referensproblem i Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="f8a4a-667">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f8a4a-668">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f8a4a-668">Az.RecoveryServices</span></span>
* <span data-ttu-id="f8a4a-669">Minsta kvarhållning för IaaSVM-policy i dagar ändrat till 7 från 1</span><span class="sxs-lookup"><span data-stu-id="f8a4a-669">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="f8a4a-670">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f8a4a-670">Az.ServiceBus</span></span>
* <span data-ttu-id="f8a4a-671">Korrigering för ärende #9182 – Get-AzServiceBusNamespace returnerar ResourceGroup istället för ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8a4a-671">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f8a4a-672">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f8a4a-672">Az.ServiceFabric</span></span>
* <span data-ttu-id="f8a4a-673">Åtgärda stavfel i felmeddelandet för Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="f8a4a-673">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="f8a4a-674">Åtgärda saknat tecken i Service Fabric-kommandorader</span><span class="sxs-lookup"><span data-stu-id="f8a4a-674">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="f8a4a-675">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f8a4a-675">Az.Sql</span></span>
* <span data-ttu-id="f8a4a-676">Lägg till parametern DnsZonePartner för New-AzureSqlInstance-cmdlet för att ge stöd för AutoDr för hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-676">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="f8a4a-677">Avvecklar cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="f8a4a-677">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="f8a4a-678">Döp om cmdletar för hotidentifiering till Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="f8a4a-678">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="f8a4a-679">Parametrarna New-AzSqlInstance -StorageSizeInGB och -LicenseType är nu valfria.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-679">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f8a4a-680">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f8a4a-680">Az.Websites</span></span>
* <span data-ttu-id="f8a4a-681">åtgärdar problemet där användningen av Set-AzWebApp och Set-AzWebAppSlot med -WebApp-egenskap tog bort taggarna</span><span class="sxs-lookup"><span data-stu-id="f8a4a-681">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="f8a4a-682">2.1.0 – maj 2019</span><span class="sxs-lookup"><span data-stu-id="f8a4a-682">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="f8a4a-683">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f8a4a-683">Az.ApiManagement</span></span>
* <span data-ttu-id="f8a4a-684">Skapade nya cmdletar för att hantera diagnostik för global- och API-omfång</span><span class="sxs-lookup"><span data-stu-id="f8a4a-684">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="f8a4a-685">**Get-AzApiManagementDiagnostic** – Skaffa diagnostik konfigurerad för global- eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="f8a4a-685">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="f8a4a-686">**New-AzApiManagementDiagnostic** – Skapa ny diagnostik för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="f8a4a-686">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="f8a4a-687">**New-AzApiManagementHttpMessageDiagnostic** – Skapa diagnostikinställning om vilka rubriker som ska loggas och storleken på brödtextbyte</span><span class="sxs-lookup"><span data-stu-id="f8a4a-687">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="f8a4a-688">**New-AzApiManagementPipelineDiagnosticSetting** – Skapa diagnostikinställningar för inkommande/utgående HTTP-meddelanden till gatewayen.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-688">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="f8a4a-689">**New-AzApiManagementSamplingSetting** – Skapa samplinginställningar för begäranden/svar för en diagnostik</span><span class="sxs-lookup"><span data-stu-id="f8a4a-689">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="f8a4a-690">**Remove-AzApiManagementDiagnostic** – Ta bort en diagnostikenhet för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="f8a4a-690">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="f8a4a-691">**Set-AzApiManagementDiagnostic** – Uppdatera en diagnostikenhet för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="f8a4a-691">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="f8a4a-692">Skapade nya cmdletar för hantering av cacheminne i ApiManagement-tjänsten</span><span class="sxs-lookup"><span data-stu-id="f8a4a-692">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="f8a4a-693">**Get-AzApiManagementCache** – Hämta information om cacheminnet som anges av identifierare eller alla cacheminnen</span><span class="sxs-lookup"><span data-stu-id="f8a4a-693">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="f8a4a-694">**New-AzApiManagementCache** – Skapa ett nytt default-cacheminne eller cacheminne i en viss Azure-region</span><span class="sxs-lookup"><span data-stu-id="f8a4a-694">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="f8a4a-695">**Remove-AzApiManagementCache** – Ta bort ett cacheminne</span><span class="sxs-lookup"><span data-stu-id="f8a4a-695">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="f8a4a-696">**Remove-AzApiManagementCache** – Ta bort ett cacheminne</span><span class="sxs-lookup"><span data-stu-id="f8a4a-696">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="f8a4a-697">Skapade nya cmdletar för hantering av API-schema</span><span class="sxs-lookup"><span data-stu-id="f8a4a-697">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="f8a4a-698">**New-AzApiManagementSchema** – Skapa ett nytt schema för ett API</span><span class="sxs-lookup"><span data-stu-id="f8a4a-698">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="f8a4a-699">**Get-AzApiManagementSchema** – Hämta de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="f8a4a-699">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="f8a4a-700">**Remove-AzApiManagementSchema** – Ta bort de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="f8a4a-700">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="f8a4a-701">**Set-AzApiManagementSchema** – Uppdatera de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="f8a4a-701">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="f8a4a-702">Skapa ny cmdlet för att generera en användartoken.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-702">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="f8a4a-703">**New-AzApiManagementUserToken** – Skapa en ny användartoken som enligt standardinställning är giltig i 8 timmar. Token för GIT-användaren kan skapas med den här cmdleten./</span><span class="sxs-lookup"><span data-stu-id="f8a4a-703">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="f8a4a-704">Skapade en ny cmdlet för att hämta nätverksstatus</span><span class="sxs-lookup"><span data-stu-id="f8a4a-704">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="f8a4a-705">**Get-AzApiManagementNetworkStatus** – Hämta nätverksstatusanslutningen för resurserna som API Management-tjänsten är beroende av.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-705">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="f8a4a-706">Det här är användbart när du distribuerar ApiManagement-tjänsten i ett virtuellt nätverk och validerar om något beroende är brutet.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-706">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="f8a4a-707">Uppdaterade cmdlet **New-AzApiManagement** för att hantera ApiManagement-tjänsten</span><span class="sxs-lookup"><span data-stu-id="f8a4a-707">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="f8a4a-708">Lade till stöd för den nya SKU:n Consumption</span><span class="sxs-lookup"><span data-stu-id="f8a4a-708">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="f8a4a-709">Aktiverade stöd för att slå på flaggan EnableClientCertificate för SKU:n Consumption</span><span class="sxs-lookup"><span data-stu-id="f8a4a-709">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="f8a4a-710">Den nya cmdleten **New-AzApiManagementSslSetting** gör det möjligt att ställa in TLS/SSL-inställningen på ”Backend” och ”Frontend” (serverdel och klientdel).</span><span class="sxs-lookup"><span data-stu-id="f8a4a-710">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="f8a4a-711">Det här kan också användas till att konfigurera chiffer som 3DES och ServerProtocols som Http2 för Frontend för en ApiManagement-tjänst.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-711">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="f8a4a-712">Stöd har lagts till för att konfigurera värdnamnet DeveloperPortal på ApiManagement-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-712">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="f8a4a-713">Uppdaterade cmdletar **Get-AzApiManagementSsoToken** för att ta PsApiManagement-objekt som indata</span><span class="sxs-lookup"><span data-stu-id="f8a4a-713">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="f8a4a-714">Uppdaterad cmdleten för att visa infogade felmeddelanden</span><span class="sxs-lookup"><span data-stu-id="f8a4a-714">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="f8a4a-715">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Felkod: Felmeddelande av typen ValidationError: Ett eller flera fält innehåller felaktiga värden: Felinformation:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="f8a4a-715">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="f8a4a-716">Uppdaterade cmdlet **Export-AzApiManagementApi** för att exportera API:er i OpenApi 3.0-format</span><span class="sxs-lookup"><span data-stu-id="f8a4a-716">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="f8a4a-717">Uppdaterade cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="f8a4a-717">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="f8a4a-718">Importera API från dokumentspecifikationen OpenApi 3.0</span><span class="sxs-lookup"><span data-stu-id="f8a4a-718">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="f8a4a-719">Om du vill åsidosätta egenskapen PsApiManagementSchema specificerad i ett dokument (Swagger, Wadl, Wsdl, OpenApi).</span><span class="sxs-lookup"><span data-stu-id="f8a4a-719">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="f8a4a-720">Åsidosätta egenskapen ServiceUrl som specificeras i ett dokument.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-720">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="f8a4a-721">Uppdaterade cmdlet **Get-AzApiManagementPolicy** för att returnera policy i undantaget format av typen icke-XML med rawxml</span><span class="sxs-lookup"><span data-stu-id="f8a4a-721">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="f8a4a-722">Uppdaterade cmdlet **Set-AzApiManagementPolicy** för att godkänna policy i undantaget format av typen icke-XML med rawxml och XML undantaget med xml</span><span class="sxs-lookup"><span data-stu-id="f8a4a-722">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="f8a4a-723">Uppdaterad cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="f8a4a-723">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="f8a4a-724">Konfigurera API med OpenId auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-724">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="f8a4a-725">Skapa ett API i ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="f8a4a-725">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="f8a4a-726">Klona ett API med SourceApiId och SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-726">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="f8a4a-727">Möjlighet att konfigurera SubscriptionRequired i API-omfattningen.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-727">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="f8a4a-728">Uppdaterad cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="f8a4a-728">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="f8a4a-729">Konfigurera API med OpenId auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-729">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="f8a4a-730">Uppdatera ett API till ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="f8a4a-730">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="f8a4a-731">Möjlighet att konfigurera SubscriptionRequired i API-omfattningen.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-731">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="f8a4a-732">Uppdaterad cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="f8a4a-732">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="f8a4a-733">Klona en befintlig version med hjälp av SourceApiRevision (kopiera taggar, produkter, åtgärder och principer).</span><span class="sxs-lookup"><span data-stu-id="f8a4a-733">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="f8a4a-734">Den nya revisionen antar ApiId från den överordnade instansen.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-734">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="f8a4a-735">Tillhandahålla ApiRevisionDescription</span><span class="sxs-lookup"><span data-stu-id="f8a4a-735">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="f8a4a-736">Åsidosätta ServiceUrl vid kloning av ett API.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-736">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="f8a4a-737">Uppdaterad cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="f8a4a-737">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="f8a4a-738">Konfigurera AAD eller AADB2C med en Authority</span><span class="sxs-lookup"><span data-stu-id="f8a4a-738">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="f8a4a-739">Konfigurera SignupPolicy, SigninPolicy, ProfileEditingPolicy och PasswordResetPolicy</span><span class="sxs-lookup"><span data-stu-id="f8a4a-739">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="f8a4a-740">Uppdaterad cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="f8a4a-740">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="f8a4a-741">Kompensera för ny SubscriptonModel med Scope och UserId</span><span class="sxs-lookup"><span data-stu-id="f8a4a-741">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="f8a4a-742">Kompensera för gammal prenumerationsmodell med ProductId och UserId</span><span class="sxs-lookup"><span data-stu-id="f8a4a-742">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="f8a4a-743">Lägg till funktion för att aktivera AllowTracing på prenumerationsnivå.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-743">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="f8a4a-744">Uppdaterad cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="f8a4a-744">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="f8a4a-745">Kompensera för ny SubscriptonModel med Scope och UserId</span><span class="sxs-lookup"><span data-stu-id="f8a4a-745">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="f8a4a-746">Kompensera för gammal prenumerationsmodell med ProductId och UserId</span><span class="sxs-lookup"><span data-stu-id="f8a4a-746">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="f8a4a-747">Lägg till funktion för att aktivera AllowTracing på prenumerationsnivå.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-747">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="f8a4a-748">Uppdaterade följande cmdletar för att acceptera ResourceId som indata</span><span class="sxs-lookup"><span data-stu-id="f8a4a-748">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="f8a4a-749">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f8a4a-749">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="f8a4a-750">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="f8a4a-750">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="f8a4a-751">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="f8a4a-751">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="f8a4a-752">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="f8a4a-752">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="f8a4a-753">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="f8a4a-753">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="f8a4a-754">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="f8a4a-754">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="f8a4a-755">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="f8a4a-755">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="f8a4a-756">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="f8a4a-756">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="f8a4a-757">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="f8a4a-757">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="f8a4a-758">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="f8a4a-758">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="f8a4a-759">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="f8a4a-759">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="f8a4a-760">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="f8a4a-760">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f8a4a-761">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f8a4a-761">Az.Automation</span></span>
* <span data-ttu-id="f8a4a-762">Uppdaterade Get-AzAutomationJobOutputRecord för att hantera postvärden av typen JSON och Text.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-762">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="f8a4a-763">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="f8a4a-763">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="f8a4a-764">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="f8a4a-764">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="f8a4a-765">Ändrade beteende för Start-AzAutomationDscCompilationJob till att bara starta jobbet istället för att vänta på slutförandet.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-765">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="f8a4a-766">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="f8a4a-766">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="f8a4a-767">Korrigering för Get-AzAutomationDscNode när using -Name returnerar alla noder.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-767">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="f8a4a-768">Nu returnerar den endast den matchande noden.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-768">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f8a4a-769">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f8a4a-769">Az.Compute</span></span>
* <span data-ttu-id="f8a4a-770">Lägg till parametrarna ProtectFromScaleIn och ProtectFromScaleSetAction i cmdleten Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-770">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="f8a4a-771">Nu är standardinställningen att vimpelparametern New-AzVM använder en tillgänglig plats om USA, östra inte stöds</span><span class="sxs-lookup"><span data-stu-id="f8a4a-771">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f8a4a-772">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f8a4a-772">Az.DataLakeStore</span></span>
* <span data-ttu-id="f8a4a-773">Uppdatera ADLS-sdk för att använda httpclient, integrera dataplanstestning med Azure-ramverk</span><span class="sxs-lookup"><span data-stu-id="f8a4a-773">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f8a4a-774">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f8a4a-774">Az.Monitor</span></span>
* <span data-ttu-id="f8a4a-775">Korrigera felaktiga parameternamn i hjälpexempel</span><span class="sxs-lookup"><span data-stu-id="f8a4a-775">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f8a4a-776">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f8a4a-776">Az.Network</span></span>
* <span data-ttu-id="f8a4a-777">Lägg till flaggan DisableBgpRoutePropagation i utdata för effektiv routningstabell</span><span class="sxs-lookup"><span data-stu-id="f8a4a-777">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="f8a4a-778">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="f8a4a-778">Updated cmdlet:</span></span>
        - <span data-ttu-id="f8a4a-779">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="f8a4a-779">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="f8a4a-780">Åtgärda dubbelstreck i dokumentationen New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f8a4a-780">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="f8a4a-781">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f8a4a-781">Az.Resources</span></span>
* <span data-ttu-id="f8a4a-782">Lägg till ny cmdlet Get-AzureRmDenyAssignment för att hämta tilldelningsnekanden</span><span class="sxs-lookup"><span data-stu-id="f8a4a-782">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="f8a4a-783">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f8a4a-783">Az.Sql</span></span>
* <span data-ttu-id="f8a4a-784">Döp om Advanced Threat Protection-cmdletar för Advanced Data Security och aktivera Vulnerability Assessment som standard</span><span class="sxs-lookup"><span data-stu-id="f8a4a-784">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="f8a4a-785">2.0.0 – maj 2019</span><span class="sxs-lookup"><span data-stu-id="f8a4a-785">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f8a4a-786">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f8a4a-786">Az.Accounts</span></span>
* <span data-ttu-id="f8a4a-787">Uppdatera autentiseringsbiblioteket för att åtgärda ADFS-problem med autentisering av användarnamn/lösenord</span><span class="sxs-lookup"><span data-stu-id="f8a4a-787">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f8a4a-788">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f8a4a-788">Az.CognitiveServices</span></span>
* <span data-ttu-id="f8a4a-789">Visa endast Bing-ansvarsfriskrivning för Bing-sökningstjänster.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-789">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="f8a4a-790">Förbättra felmeddelande när det inte går att skapa konton.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-790">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f8a4a-791">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f8a4a-791">Az.Compute</span></span>
* <span data-ttu-id="f8a4a-792">Funktion för närhetsplaceringsgrupper.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-792">Proximity placement group feature.</span></span>
    - <span data-ttu-id="f8a4a-793">Följande nya cmdletar har lagts till:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="f8a4a-793">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="f8a4a-794">Den nya parametern ProximityPlacementGroupId har lagts till i följande cmdletar:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="f8a4a-794">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="f8a4a-795">Parametern StorageAccountType har lagts till i New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-795">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="f8a4a-796">TargetRegion för New-AzGalleryImageVersion kan innehålla StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-796">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="f8a4a-797">Växlingsparametern SkipShutdown har lagts till i Stop-AzVM och Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f8a4a-797">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="f8a4a-798">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="f8a4a-798">Breaking changes</span></span>
    - <span data-ttu-id="f8a4a-799">Set-AzVMBootDiagnostics har ändrats till Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-799">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="f8a4a-800">Export-AzLogAnalyticThrottledRequests har ändrats till Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-800">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="f8a4a-801">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="f8a4a-801">Az.DeploymentManager</span></span>
* <span data-ttu-id="f8a4a-802">De första allmänt tillgängliga versionerna av cmdletar för Distributionshanteraren i Azure</span><span class="sxs-lookup"><span data-stu-id="f8a4a-802">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="f8a4a-803">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="f8a4a-803">Az.Dns</span></span>
* <span data-ttu-id="f8a4a-804">Automatisk delegering av DNS för NameServer</span><span class="sxs-lookup"><span data-stu-id="f8a4a-804">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="f8a4a-805">Det överordnade zonnamnet kan användas som ytterligare valfri parameter i cmdleten för att skapa DNS-zoner.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-805">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="f8a4a-806">Lägger till NS-poster för en nyligen skapad underordnad zon i den överordnade zonen.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-806">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="f8a4a-807">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f8a4a-807">Az.FrontDoor</span></span>
* <span data-ttu-id="f8a4a-808">De första allmänt tillgängliga versionerna av cmdletar för Azure FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f8a4a-808">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="f8a4a-809">Byt namn på WAF-cmdletar så att de omfattar ”Waf”</span><span class="sxs-lookup"><span data-stu-id="f8a4a-809">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="f8a4a-810">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f8a4a-810">Az.HDInsight</span></span>
* <span data-ttu-id="f8a4a-811">Två cmdletar har tagits bort:</span><span class="sxs-lookup"><span data-stu-id="f8a4a-811">Removed two cmdlets:</span></span>
    - <span data-ttu-id="f8a4a-812">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="f8a4a-812">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="f8a4a-813">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="f8a4a-813">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="f8a4a-814">En ny cmdlet har lagts till, Set-AzHDInsightGatewayCredential, som ersätter Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="f8a4a-814">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="f8a4a-815">Uppdatera cmdleten Get-AzHDInsightJobOutput för att skilja mellan läsarrollen och HDInsight-operatörsrollen:</span><span class="sxs-lookup"><span data-stu-id="f8a4a-815">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="f8a4a-816">Användare med läsarrollen måste uttryckligen ange parametern ”DefaultStorageAccountKey”, annars uppstår fel.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-816">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="f8a4a-817">Användare med HDInsight-operatörsrollen påverkas inte.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-817">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f8a4a-818">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f8a4a-818">Az.Monitor</span></span>
* <span data-ttu-id="f8a4a-819">Nya cmdletar för SQR API (schemalagd frågeregel)</span><span class="sxs-lookup"><span data-stu-id="f8a4a-819">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="f8a4a-820">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="f8a4a-820">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="f8a4a-821">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="f8a4a-821">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="f8a4a-822">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="f8a4a-822">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="f8a4a-823">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="f8a4a-823">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="f8a4a-824">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="f8a4a-824">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="f8a4a-825">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="f8a4a-825">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="f8a4a-826">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="f8a4a-826">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="f8a4a-827">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="f8a4a-827">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="f8a4a-828">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="f8a4a-828">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="f8a4a-829">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="f8a4a-829">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="f8a4a-830">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="f8a4a-830">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="f8a4a-831">[Mer](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information om SQR API</span><span class="sxs-lookup"><span data-stu-id="f8a4a-831">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="f8a4a-832">Az.Monitor.md har uppdaterats för att omfatta cmdletar för måttbaserade aviseringsregler i GenV2 (inte klassiska)</span><span class="sxs-lookup"><span data-stu-id="f8a4a-832">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f8a4a-833">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f8a4a-833">Az.Network</span></span>
* <span data-ttu-id="f8a4a-834">Lägg till stöd för NAT Gateway-resurs</span><span class="sxs-lookup"><span data-stu-id="f8a4a-834">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="f8a4a-835">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="f8a4a-835">New cmdlets</span></span>
        - <span data-ttu-id="f8a4a-836">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="f8a4a-836">New-AzNatGateway</span></span>
        - <span data-ttu-id="f8a4a-837">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="f8a4a-837">Get-AzNatGateway</span></span>
        - <span data-ttu-id="f8a4a-838">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="f8a4a-838">Set-AzNatGateway</span></span>
        - <span data-ttu-id="f8a4a-839">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="f8a4a-839">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="f8a4a-840">Uppdaterade cmdletar</span><span class="sxs-lookup"><span data-stu-id="f8a4a-840">Updated cmdlets</span></span>
        - <span data-ttu-id="f8a4a-841">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="f8a4a-841">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="f8a4a-842">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="f8a4a-842">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="f8a4a-843">Nedanstående kommandon för funktionen har uppdaterats: Ange/ta bort anpassade vägar på Brooklyn Gateway.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-843">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="f8a4a-844">New-AzVirtualNetworkGateway har uppdaterats: Den valfria parametern -CustomRoute har lagts till för att ställa in adressprefix som anpassade vägar för att ange gateway.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-844">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="f8a4a-845">Set-AzVirtualNetworkGateway har uppdaterats: Den valfria parametern -CustomRoute har lagts till för att ange adressprefix som anpassade vägar för att ange gateway.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-845">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f8a4a-846">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f8a4a-846">Az.PolicyInsights</span></span>
* <span data-ttu-id="f8a4a-847">Stöd för att fråga efter information om principutvärdering.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-847">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="f8a4a-848">Lägg till parametern ”-Expand” för Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-848">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="f8a4a-849">Stöd för -Expand PolicyEvaluationDetails.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-849">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f8a4a-850">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f8a4a-850">Az.RecoveryServices</span></span>
* <span data-ttu-id="f8a4a-851">Stöd för att dela prenumeration mellan Azure och Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-851">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="f8a4a-852">Markering av kommande icke-bakåtkompatibla ändringar för Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-852">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="f8a4a-853">Korrigering för återställningsplan och åtgärdsplan i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-853">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="f8a4a-854">Korrigering för mappning av uppdateringsnätverk i Azure Site Recovery för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-854">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="f8a4a-855">Korrigering för instruktioner för uppdateringsskydd i Azure Site Recovery för Azure till Azure för hanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-855">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="f8a4a-856">Andra mindre korrigeringar.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-856">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="f8a4a-857">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="f8a4a-857">Az.Relay</span></span>
* <span data-ttu-id="f8a4a-858">Korrigera stavfel i kundriktade meddelanden</span><span class="sxs-lookup"><span data-stu-id="f8a4a-858">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="f8a4a-859">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f8a4a-859">Az.ServiceBus</span></span>
* <span data-ttu-id="f8a4a-860">Nya cmdletar har lagts till för NetworkRuleSet för namnområden</span><span class="sxs-lookup"><span data-stu-id="f8a4a-860">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f8a4a-861">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f8a4a-861">Az.Storage</span></span>
* <span data-ttu-id="f8a4a-862">Uppgradera till lagringsklientbiblioteket 10.0.1 (namnområdet för alla objekt från detta SDK ändras från ”Microsoft.WindowsAzure.Storage. *till ”Microsoft.Azure.Storage.* ”)</span><span class="sxs-lookup"><span data-stu-id="f8a4a-862">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="f8a4a-863">Uppgradera till Microsoft.Azure.Management.Storage 11.0.0 för att stödja den nya API-versionen 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-863">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="f8a4a-864">Standardlagringskontot i Skapa lagringskonto ändras från ”Storage” till ”StorageV2”</span><span class="sxs-lookup"><span data-stu-id="f8a4a-864">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="f8a4a-865">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f8a4a-865">New-AzStorageAccount</span></span>
* <span data-ttu-id="f8a4a-866">Ändra lagringskontots cmdlet-utdata Sku.Name för att passa med indata-SkuName genom att lägga till ”-”. Till exempel ändras ”StandardLRS” till ”Standard_LRS”</span><span class="sxs-lookup"><span data-stu-id="f8a4a-866">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="f8a4a-867">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f8a4a-867">New-AzStorageAccount</span></span>
    - <span data-ttu-id="f8a4a-868">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f8a4a-868">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="f8a4a-869">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f8a4a-869">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f8a4a-870">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f8a4a-870">Az.Websites</span></span>
* <span data-ttu-id="f8a4a-871">Egenskapen ”typ” konfigureras nu för PSSite-objekt som returneras av Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="f8a4a-871">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="f8a4a-872">Get-AzWebApp\*Metrics och Get-AzAppServicePlanMetrics markeras som inaktuella</span><span class="sxs-lookup"><span data-stu-id="f8a4a-872">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="f8a4a-873">1.8.0 – april 2019</span><span class="sxs-lookup"><span data-stu-id="f8a4a-873">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="f8a4a-874">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="f8a4a-874">Highlights since the last major release</span></span>
* <span data-ttu-id="f8a4a-875">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="f8a4a-875">General availability of `Az` module</span></span>
* <span data-ttu-id="f8a4a-876">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="f8a4a-876">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="f8a4a-877">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="f8a4a-877">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="f8a4a-878">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="f8a4a-878">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="f8a4a-879">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="f8a4a-879">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="f8a4a-880">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="f8a4a-880">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="f8a4a-881">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="f8a4a-881">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f8a4a-882">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f8a4a-882">Az.Accounts</span></span>
* <span data-ttu-id="f8a4a-883">Uppdatera Uninstall-AzureRm för att ta bort moduler i Mac på ett korrekt sätt</span><span class="sxs-lookup"><span data-stu-id="f8a4a-883">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="f8a4a-884">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="f8a4a-884">Az.Batch</span></span>
* <span data-ttu-id="f8a4a-885">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-885">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="f8a4a-886">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f8a4a-886">Az.Cdn</span></span>
* <span data-ttu-id="f8a4a-887">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-887">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f8a4a-888">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f8a4a-888">Az.CognitiveServices</span></span>
* <span data-ttu-id="f8a4a-889">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-889">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f8a4a-890">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f8a4a-890">Az.Compute</span></span>
* <span data-ttu-id="f8a4a-891">Åtgärda problem med AEM-installationen om resurs-ID:n för diskar innehåller resourcegroups i gemener i resurs-ID:n</span><span class="sxs-lookup"><span data-stu-id="f8a4a-891">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="f8a4a-892">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-892">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f8a4a-893">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="f8a4a-893">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f8a4a-894">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f8a4a-894">Az.DataFactory</span></span>
* <span data-ttu-id="f8a4a-895">Lägg till SsisProperties om NodeCount inte är null för hanterad integreringskörning.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-895">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f8a4a-896">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f8a4a-896">Az.DataLakeStore</span></span>
* <span data-ttu-id="f8a4a-897">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-897">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="f8a4a-898">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="f8a4a-898">Az.EventGrid</span></span>
* <span data-ttu-id="f8a4a-899">Hjälptexten för slutpunkten har uppdaterats för att visa att resurser ska skapas innan cmdletarna för att skapa/uppdatera händelseprenumerationer används.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-899">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f8a4a-900">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f8a4a-900">Az.EventHub</span></span>
* <span data-ttu-id="f8a4a-901">Nya cmdletar har lagts till för NetworkRuleSet för namnområden</span><span class="sxs-lookup"><span data-stu-id="f8a4a-901">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="f8a4a-902">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f8a4a-902">Az.HDInsight</span></span>
* <span data-ttu-id="f8a4a-903">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-903">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f8a4a-904">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f8a4a-904">Az.IotHub</span></span>
* <span data-ttu-id="f8a4a-905">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-905">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f8a4a-906">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f8a4a-906">Az.KeyVault</span></span>
* <span data-ttu-id="f8a4a-907">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-907">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f8a4a-908">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="f8a4a-908">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="f8a4a-909">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="f8a4a-909">Az.MachineLearning</span></span>
* <span data-ttu-id="f8a4a-910">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-910">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="f8a4a-911">Az.Media</span><span class="sxs-lookup"><span data-stu-id="f8a4a-911">Az.Media</span></span>
* <span data-ttu-id="f8a4a-912">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-912">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f8a4a-913">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f8a4a-913">Az.Monitor</span></span>
  * <span data-ttu-id="f8a4a-914">Nya cmdletar för måttbaserad aviseringsregel i GenV2 (inte klassisk)</span><span class="sxs-lookup"><span data-stu-id="f8a4a-914">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="f8a4a-915">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="f8a4a-915">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="f8a4a-916">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="f8a4a-916">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="f8a4a-917">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="f8a4a-917">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="f8a4a-918">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="f8a4a-918">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="f8a4a-919">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="f8a4a-919">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="f8a4a-920">Monitor SDK har uppdaterats till version 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="f8a4a-920">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f8a4a-921">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f8a4a-921">Az.Network</span></span>
* <span data-ttu-id="f8a4a-922">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-922">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f8a4a-923">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="f8a4a-923">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="f8a4a-924">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="f8a4a-924">Az.NotificationHubs</span></span>
* <span data-ttu-id="f8a4a-925">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-925">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f8a4a-926">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f8a4a-926">Az.OperationalInsights</span></span>
* <span data-ttu-id="f8a4a-927">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-927">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="f8a4a-928">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="f8a4a-928">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="f8a4a-929">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-929">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f8a4a-930">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f8a4a-930">Az.RecoveryServices</span></span>
* <span data-ttu-id="f8a4a-931">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-931">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f8a4a-932">Tabellformatet för SQL i virtuella Azure-datorer har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="f8a4a-932">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="f8a4a-933">En alternativ metod för att hämta platser i AzureFileShare har lagts till</span><span class="sxs-lookup"><span data-stu-id="f8a4a-933">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="f8a4a-934">ScheduleRunDays i SchedulePolicy-objekt har uppdaterats enligt tidszon</span><span class="sxs-lookup"><span data-stu-id="f8a4a-934">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="f8a4a-935">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="f8a4a-935">Az.RedisCache</span></span>
* <span data-ttu-id="f8a4a-936">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-936">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f8a4a-937">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f8a4a-937">Az.Resources</span></span>
* <span data-ttu-id="f8a4a-938">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="f8a4a-938">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="f8a4a-939">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f8a4a-939">Az.Sql</span></span>
* <span data-ttu-id="f8a4a-940">Ersätt Monitor SDK-beroende med vanlig kod</span><span class="sxs-lookup"><span data-stu-id="f8a4a-940">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="f8a4a-941">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-941">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f8a4a-942">Förbättrad process för klassificering av flera kolumner.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-942">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="f8a4a-943">Inkludera SKU-egenskaper (SKU-namn, serie, kapacitet) i svaret från Get-AzSqlServerServiceObjective och formatera som tabell som standard.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-943">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="f8a4a-944">Möjlighet att använda Get-AzSqlServerServiceObjective efter plats utan att behöva en redan befintlig server i regionen.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-944">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="f8a4a-945">Stöd för tidszonsparametern när hanterade instanser skapas.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-945">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="f8a4a-946">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="f8a4a-946">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f8a4a-947">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f8a4a-947">Az.Websites</span></span>
* <span data-ttu-id="f8a4a-948">åtgärdar Set-AzWebApp och Set-AzWebAppSlot så att de inte tar bort taggar vid körning</span><span class="sxs-lookup"><span data-stu-id="f8a4a-948">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="f8a4a-949">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-949">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f8a4a-950">SDK för WebSites har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-950">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="f8a4a-951">Egenskapen AdminSiteName har tagits bort från PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-951">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="f8a4a-952">1.7.0 – april 2019</span><span class="sxs-lookup"><span data-stu-id="f8a4a-952">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="f8a4a-953">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="f8a4a-953">Highlights since the last major release</span></span>
* <span data-ttu-id="f8a4a-954">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="f8a4a-954">General availability of `Az` module</span></span>
* <span data-ttu-id="f8a4a-955">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="f8a4a-955">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="f8a4a-956">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="f8a4a-956">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="f8a4a-957">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="f8a4a-957">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="f8a4a-958">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="f8a4a-958">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="f8a4a-959">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="f8a4a-959">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="f8a4a-960">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="f8a4a-960">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f8a4a-961">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f8a4a-961">Az.Accounts</span></span>
* <span data-ttu-id="f8a4a-962">Add-AzEnvironment och Set-AzEnvironment har uppdaterats för att godkänna parametern AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="f8a4a-962">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="f8a4a-963">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f8a4a-963">Az.AnalysisServices</span></span>
* <span data-ttu-id="f8a4a-964">ServiceClient används i cmdletar för dataplan och den ursprungliga autentiseringslogiken har tagits bort</span><span class="sxs-lookup"><span data-stu-id="f8a4a-964">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="f8a4a-965">Add-AzureASAccount används för omslutning av Connect-AzAccount för att undvika en icke-bakåtkompatibel ändring</span><span class="sxs-lookup"><span data-stu-id="f8a4a-965">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f8a4a-966">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f8a4a-966">Az.Automation</span></span>
* <span data-ttu-id="f8a4a-967">Buggen för cmdleten New-AzAutomationSoftwareUpdateConfiguration för inkluderingar har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-967">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="f8a4a-968">Nu bör parametern IncludedKbNumber och IncludedPackageNameMask fungera.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-968">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="f8a4a-969">Felkorrigering för dynamiska grupper i uppdateringshanteringen för azure automation</span><span class="sxs-lookup"><span data-stu-id="f8a4a-969">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f8a4a-970">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f8a4a-970">Az.Compute</span></span>
* <span data-ttu-id="f8a4a-971">Lägg till parametern HyperVGeneration i New-AzDiskConfig och New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="f8a4a-971">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="f8a4a-972">Tillåt att virtuella datorer skapas med galleribilder från andra klientorganisationer.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-972">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="f8a4a-973">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="f8a4a-973">Az.ContainerInstance</span></span>
* <span data-ttu-id="f8a4a-974">Ett problem har åtgärdats i parametern -Command för New-AzContainerGroup som lade till ett avslutande tomt argument</span><span class="sxs-lookup"><span data-stu-id="f8a4a-974">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f8a4a-975">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f8a4a-975">Az.DataFactory</span></span>
* <span data-ttu-id="f8a4a-976">ADF .Net SDK-versionen har uppdaterats till 3.0.2</span><span class="sxs-lookup"><span data-stu-id="f8a4a-976">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="f8a4a-977">Cmdleten Set-AzDataFactoryV2 har uppdaterats med extra parametrar för inställningar som rör RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-977">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f8a4a-978">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f8a4a-978">Az.Resources</span></span>
* <span data-ttu-id="f8a4a-979">Förbättra hanteringen av providrar för Get-AzResource när parametrarna -ResourceId eller -ResourceGroupName, -Name och -ResourceType tillhandahålls</span><span class="sxs-lookup"><span data-stu-id="f8a4a-979">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="f8a4a-980">Förbättra felhanteringen för ”Test-AzDeployment” och ”Test-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="f8a4a-980">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="f8a4a-981">Hantera fel utanför distributionsvalideringen och ta med dem i kommandoutdata istället</span><span class="sxs-lookup"><span data-stu-id="f8a4a-981">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="f8a4a-982">Mer information här: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="f8a4a-982">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="f8a4a-983">Lägg till växlingsparametern -IgnoreDynamicParameters till en uppsättning av cmdletar för distribution för att hoppa över fråga i skript och jobbscenarier</span><span class="sxs-lookup"><span data-stu-id="f8a4a-983">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="f8a4a-984">Mer information här: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="f8a4a-984">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="f8a4a-985">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f8a4a-985">Az.Sql</span></span>
* <span data-ttu-id="f8a4a-986">Stöd för dataklassificering av databaser.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-986">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f8a4a-987">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f8a4a-987">Az.Storage</span></span>
* <span data-ttu-id="f8a4a-988">Rapportera detaljfel när lagringskontext skapas med parametern -UseConnectedAccount, men utan inloggning på Azure-kontot</span><span class="sxs-lookup"><span data-stu-id="f8a4a-988">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="f8a4a-989">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="f8a4a-989">New-AzStorageContext</span></span>
* <span data-ttu-id="f8a4a-990">Stöd för att hantera Blob Service-egenskaper för ett angivet lagringskonto med API:et för hanteringsplan</span><span class="sxs-lookup"><span data-stu-id="f8a4a-990">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="f8a4a-991">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="f8a4a-991">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="f8a4a-992">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="f8a4a-992">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="f8a4a-993">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="f8a4a-993">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="f8a4a-994">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="f8a4a-994">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="f8a4a-995">Stöd för -AsJob-cmdletar för att ladda upp och ladda ned blobar och filer</span><span class="sxs-lookup"><span data-stu-id="f8a4a-995">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="f8a4a-996">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="f8a4a-996">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="f8a4a-997">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="f8a4a-997">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="f8a4a-998">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="f8a4a-998">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="f8a4a-999">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="f8a4a-999">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="f8a4a-1000">1.6.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1000">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="f8a4a-1001">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1001">Highlights since the last major release</span></span>
* <span data-ttu-id="f8a4a-1002">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1002">General availability of `Az` module</span></span>
* <span data-ttu-id="f8a4a-1003">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1003">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="f8a4a-1004">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1004">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="f8a4a-1005">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1005">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="f8a4a-1006">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1006">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="f8a4a-1007">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1007">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="f8a4a-1008">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1008">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f8a4a-1009">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1009">Az.Automation</span></span>
* <span data-ttu-id="f8a4a-1010">Azure Automation – ändring av uppdateringshantering för stöd för de nya funktionerna:</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1010">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="f8a4a-1011">Dynamisk gruppering</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1011">Dynamic grouping</span></span>
    * <span data-ttu-id="f8a4a-1012">För-/efterskrift</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1012">Pre-Post script</span></span>
    * <span data-ttu-id="f8a4a-1013">Inställning för omstart</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1013">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f8a4a-1014">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1014">Az.Compute</span></span>
* <span data-ttu-id="f8a4a-1015">Åtgärda problem med sökvägsmatchning i Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1015">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="f8a4a-1016">Uppdatera Compute-klientbibliotek till 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1016">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f8a4a-1017">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1017">Az.KeyVault</span></span>
* <span data-ttu-id="f8a4a-1018">Stöd för jokertecken för KeyVault-cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1018">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f8a4a-1019">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1019">Az.Network</span></span>
* <span data-ttu-id="f8a4a-1020">Lägg till stöd för Threat Intelligence för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1020">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="f8a4a-1021">Lägg till resurs för brandväggsprincip på översta nivå och anpassade regler för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1021">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f8a4a-1022">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1022">Az.RecoveryServices</span></span>
* <span data-ttu-id="f8a4a-1023">SnapshotRetentionInDays har lagts till i Azure-principen för virtuella datorer för stöd av Instant RP</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1023">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="f8a4a-1024">Pipe-stöd för avregistrering av container har lagts till</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1024">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="f8a4a-1025">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1025">Az.Resources</span></span>
* <span data-ttu-id="f8a4a-1026">Uppdatera stöd för jokertecken för Get-AzResource och Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1026">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="f8a4a-1027">Uppdatera autentiseringsuppgifter som används vid allmänna anrop till ARM</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1027">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="f8a4a-1028">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1028">Az.Sql</span></span>
* <span data-ttu-id="f8a4a-1029">Cmdlet-parametern (ExcludeDetectionType) för Hotidentifiering ändrades från DetectionType till sträng[] för att framtidssäkra den när nya DetectionTypes läggs till, och även för att stödja automatisk ifyllning.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1029">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f8a4a-1030">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1030">Az.Storage</span></span>
* <span data-ttu-id="f8a4a-1031">Stöd för att hämta/ange/ta bort hanteringsprincip på ett lagringskonto</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1031">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="f8a4a-1032">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1032">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="f8a4a-1033">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1033">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="f8a4a-1034">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1034">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="f8a4a-1035">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1035">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="f8a4a-1036">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1036">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="f8a4a-1037">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1037">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f8a4a-1038">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1038">Az.Websites</span></span>
* <span data-ttu-id="f8a4a-1039">Åtgärda fel med ARM-mall som avbryter kloning av alla platser med 'New-AzWebApp -IncludeSourceWebAppSlots'</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1039">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="f8a4a-1040">1.5.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1040">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f8a4a-1041">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1041">Az.Accounts</span></span>
* <span data-ttu-id="f8a4a-1042">Lägg till kommandot Register-AzModule för stöd för AutoRest-genererade cmdletar</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1042">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="f8a4a-1043">Uppdatera exempel för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1043">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f8a4a-1044">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1044">Az.Automation</span></span>
* <span data-ttu-id="f8a4a-1045">Problem med att hämta vissa månadsscheman i flera Azure Automation-cmdletar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1045">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="f8a4a-1046">Åtgärda problem med att Get-AzAutomationDscNode bara returnerar de 20 översta noderna.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1046">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="f8a4a-1047">Nu returneras alla noder</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1047">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="f8a4a-1048">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1048">Az.Cdn</span></span>
* <span data-ttu-id="f8a4a-1049">Nya Powershell-cmdletar för att aktivera/inaktivera anpassade domän-HTTPS har lagts till och de gamla har gjorts inaktuella</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1049">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f8a4a-1050">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1050">Az.Compute</span></span>
* <span data-ttu-id="f8a4a-1051">Lägg till stöd för jokertecken för Get-cmdletar</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1051">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f8a4a-1052">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1052">Az.DataFactory</span></span>
* <span data-ttu-id="f8a4a-1053">ADF .Net SDK-versionen har uppdaterats till 3.0.1</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1053">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="f8a4a-1054">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1054">Az.LogicApp</span></span>
* <span data-ttu-id="f8a4a-1055">Åtgärda problemet med att ListWorkflows endast hämtar den första sidan med resultat</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1055">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f8a4a-1056">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1056">Az.Network</span></span>
* <span data-ttu-id="f8a4a-1057">Lägg till stöd för jokertecken för Network-cmdletar</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1057">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f8a4a-1058">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1058">Az.RecoveryServices</span></span>
* <span data-ttu-id="f8a4a-1059">Stöd har lagts till för SQL Server i virtuella Azure-datorer</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1059">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="f8a4a-1060">SDK-uppdatering</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1060">SDK Update</span></span>
* <span data-ttu-id="f8a4a-1061">Get-ProtectableItem-incheckning i VMappContainer har tagits bort</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1061">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="f8a4a-1062">Name och ServerName har lagts till som parametrar för Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1062">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="f8a4a-1063">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1063">Az.Resources</span></span>
* <span data-ttu-id="f8a4a-1064">Lägg till parametern `-TemplateObject` i cmdletar för distribution</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1064">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="f8a4a-1065">Mer information här: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1065">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="f8a4a-1066">Åtgärda problem med piping av resultatet i `Get-AzResource` till `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1066">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="f8a4a-1067">Mer information här: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1067">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="f8a4a-1068">Åtgärda problem med ändring av JSON-datatyp när `Set-AzResource` körs</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1068">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="f8a4a-1069">Mer information här: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1069">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="f8a4a-1070">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1070">Az.Sql</span></span>
* <span data-ttu-id="f8a4a-1071">AuditingEndpointsCommunicator uppdateras.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1071">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="f8a4a-1072">Åtgärdar beteendet hos ett gränsscenario när nya diagnostikinställningar skapas.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1072">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f8a4a-1073">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1073">Az.Storage</span></span>
* <span data-ttu-id="f8a4a-1074">Stöd för BlockBlobStorage när Storage-konto skapas      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1074">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="f8a4a-1075">1.4.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1075">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="f8a4a-1076">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1076">Az.AnalysisServices</span></span>
* <span data-ttu-id="f8a4a-1077">Inaktuell AddAzureASAccount-cmdlet</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1077">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f8a4a-1078">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1078">Az.Automation</span></span>
* <span data-ttu-id="f8a4a-1079">Hjälpen för Import-AzAutomationDscNodeConfiguration har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1079">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="f8a4a-1080">Konfigurationsnamnsvalidering har lagts till i cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1080">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="f8a4a-1081">Förbättrad felhantering för cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1081">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f8a4a-1082">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1082">Az.CognitiveServices</span></span>
* <span data-ttu-id="f8a4a-1083">CustomSubdomainName har lagts till som en ny valfri parameter för New-AzCognitiveServicesAccount, som används för att ange underdomän för resursen.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1083">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f8a4a-1084">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1084">Az.Compute</span></span>
* <span data-ttu-id="f8a4a-1085">Problemet med ID-parameteruppsättningar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1085">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="f8a4a-1086">Get-AzVMExtension har uppdaterats så att alla installerade tillägg visas om parametern Name inte har angetts</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1086">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="f8a4a-1087">Parametrarna Tag och ResourceId har lagts till i cmdleten Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1087">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="f8a4a-1088">Get-AzVmssVM utan instans-ID och med InstanceView kan visa virtuella VMSS-datorer med instansvyn.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1088">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f8a4a-1089">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1089">Az.DataLakeStore</span></span>
* <span data-ttu-id="f8a4a-1090">Cmdletar har lagts till för uppräkning och återställning av borttagna objekt i ADL</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1090">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f8a4a-1091">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1091">Az.EventHub</span></span>
* <span data-ttu-id="f8a4a-1092">Ny boolesk egenskap SkipEmptyArchives har lagts till i Skip Empty Archives i CaptureDescription-klassen i Eventhub</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1092">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="f8a4a-1093">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1093">Az.KeyVault</span></span>
* <span data-ttu-id="f8a4a-1094">Taggning i Set-AzKeyVaultSecret har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1094">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="f8a4a-1095">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1095">Az.LogicApp</span></span>
* <span data-ttu-id="f8a4a-1096">Grundläggande SKU har lagts till för Integrationskonton</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1096">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="f8a4a-1097">XSLT 2.0, XSLT 3.0 och Flytande mappningstyper har lagts till</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1097">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="f8a4a-1098">Nya cmdletar för integrationskontosammansättningar</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1098">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="f8a4a-1099">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1099">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="f8a4a-1100">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1100">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="f8a4a-1101">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1101">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="f8a4a-1102">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1102">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="f8a4a-1103">Nya cmdletar för batchkonfiguration för integrationskonto</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1103">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="f8a4a-1104">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1104">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="f8a4a-1105">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1105">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="f8a4a-1106">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1106">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="f8a4a-1107">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1107">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="f8a4a-1108">Logic App-SDK har uppdaterats till version 4.1.0</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1108">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f8a4a-1109">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1109">Az.Monitor</span></span>
* <span data-ttu-id="f8a4a-1110">Hjälpen för Get-AzMetric har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1110">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f8a4a-1111">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1111">Az.Network</span></span>
* <span data-ttu-id="f8a4a-1112">Hjälpexempel för Add-AzApplicationGatewayCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1112">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f8a4a-1113">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1113">Az.OperationalInsights</span></span>
* <span data-ttu-id="f8a4a-1114">Ytterligare stöd för datakällorna New och Get ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1114">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="f8a4a-1115">Ny ApplicationInsights-typ har lagts till för att ge stöd för ”Get specific” och ”Get all” för ApplicationInsights-datakällor för angiven arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1115">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="f8a4a-1116">Cmdleten New-AzOperationalInsightsApplicationInsightsDataSource har lagts till för att skapa datakälla med angivna parametrar för Application Insights-resurs: subscription Id, resourceGroupName och name.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1116">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="f8a4a-1117">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1117">Az.Resources</span></span>
* <span data-ttu-id="f8a4a-1118">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1118">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="f8a4a-1119">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1119">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="f8a4a-1120">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1120">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="f8a4a-1121">Fel som gör att KeyCredentials inte kan skapas upprepade gånger har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1121">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="f8a4a-1122">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1122">Az.Sql</span></span>
* <span data-ttu-id="f8a4a-1123">Lägg till stöd för hyperskalanivån för SQL DB</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1123">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="f8a4a-1124">Ett fel har åtgärdats där återställningen kunde misslyckas på grund av onödiga inställningsegenskaper i restore-förfrågan</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1124">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f8a4a-1125">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1125">Az.Websites</span></span>
* <span data-ttu-id="f8a4a-1126">Rätt exempel i Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1126">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="f8a4a-1127">1.3.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1127">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f8a4a-1128">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1128">Az.Accounts</span></span>
* <span data-ttu-id="f8a4a-1129">Uppdatera till den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1129">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="f8a4a-1130">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1130">Az.AnalysisServices</span></span>
<span data-ttu-id="f8a4a-1131">Allmän tillgänglighet för Az.AnalysisServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1131">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f8a4a-1132">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1132">Az.Compute</span></span>
* <span data-ttu-id="f8a4a-1133">AEM-tillägg: Lägg till stöd för UltraSSD-, P60-, P70- och P80-diskar</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1133">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="f8a4a-1134">Uppdatera hjälpbeskrivning för Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1134">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="f8a4a-1135">Uppdatera hjälpbeskrivning och exempel för Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1135">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f8a4a-1136">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1136">Az.RecoveryServices</span></span>
<span data-ttu-id="f8a4a-1137">Allmän tillgänglighet för Az.RecoveryServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1137">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f8a4a-1138">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1138">Az.Resources</span></span>
* <span data-ttu-id="f8a4a-1139">Korrigera taggar för resursgrupper</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1139">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="f8a4a-1140">Mer information här: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1140">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="f8a4a-1141">Åtgärda problem där `Get-AzureRmRoleAssignment` inte respekterar -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1141">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="f8a4a-1142">Mer information här: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1142">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="f8a4a-1143">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1143">Az.Sql</span></span>
* <span data-ttu-id="f8a4a-1144">Lägga till Get/Set-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1144">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="f8a4a-1145">Åtgärda problem där ett nullref-undantag uppstår när du kör SQL-cmdletar och inte är inloggad på ett Azure-konto</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1145">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="f8a4a-1146">Åtgärda nullref-undantag i Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1146">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="f8a4a-1147">1.2.1 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1147">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f8a4a-1148">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1148">Az.Accounts</span></span>
* <span data-ttu-id="f8a4a-1149">Version med rätt version av autentisering</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1149">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="f8a4a-1150">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1150">Az.AnalysisServices</span></span>
* <span data-ttu-id="f8a4a-1151">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1151">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f8a4a-1152">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1152">Az.RecoveryServices</span></span>
* <span data-ttu-id="f8a4a-1153">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1153">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="f8a4a-1154">1.2.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1154">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f8a4a-1155">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1155">Az.Accounts</span></span>
* <span data-ttu-id="f8a4a-1156">Lägga till interaktiv autentisering och autentisering med användarnamn/lösenord för endast Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1156">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="f8a4a-1157">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1157">Update incorrect online help URLs</span></span>
* <span data-ttu-id="f8a4a-1158">Lägga till varningsmeddelande i PS Core för Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1158">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="f8a4a-1159">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1159">Az.Aks</span></span>
* <span data-ttu-id="f8a4a-1160">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1160">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f8a4a-1161">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1161">Az.Automation</span></span>
* <span data-ttu-id="f8a4a-1162">Stöd för Python 2-runbookflöden har lagts till</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1162">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="f8a4a-1163">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1163">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="f8a4a-1164">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1164">Az.Cdn</span></span>
* <span data-ttu-id="f8a4a-1165">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1165">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f8a4a-1166">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1166">Az.Compute</span></span>
* <span data-ttu-id="f8a4a-1167">Lägga till cmdleten Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1167">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="f8a4a-1168">Lägga till TempDisk-parameter i Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1168">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="f8a4a-1169">Korrigera varningsmeddelande för New-AzVM</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1169">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="f8a4a-1170">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1170">Az.ContainerRegistry</span></span>
* <span data-ttu-id="f8a4a-1171">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1171">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f8a4a-1172">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1172">Az.DataFactory</span></span>
* <span data-ttu-id="f8a4a-1173">ADF .Net SDK-versionen har uppdaterats till 3.0.0</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1173">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f8a4a-1174">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1174">Az.DataLakeStore</span></span>
* <span data-ttu-id="f8a4a-1175">Åtgärda problem med ADLS-slutpunkt vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1175">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="f8a4a-1176">Mer information här: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1176">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="f8a4a-1177">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1177">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f8a4a-1178">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1178">Az.IotHub</span></span>
* <span data-ttu-id="f8a4a-1179">Lägga till kodningsformat i cmdleten Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1179">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f8a4a-1180">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1180">Az.KeyVault</span></span>
* <span data-ttu-id="f8a4a-1181">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1181">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f8a4a-1182">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1182">Az.Network</span></span>
* <span data-ttu-id="f8a4a-1183">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1183">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="f8a4a-1184">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1184">Az.Resources</span></span>
* <span data-ttu-id="f8a4a-1185">Åtgärda felaktiga exempel i referensdokumentationen ”New-AzADAppCredential” och ”New-AzADSpCredential”</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1185">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="f8a4a-1186">Åtgärda problem där sökvägen för parametern ”-TemplateFile” inte omvandlas innan cmdletarna för distribution i resursgruppen körs</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1186">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="f8a4a-1187">Az.Resources: Korrigera dokumentationen om standardvärdet för New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1187">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="f8a4a-1188">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1188">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="f8a4a-1189">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1189">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="f8a4a-1190">Åtgärda formateringsproblemet med objektet ”PSResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1190">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="f8a4a-1191">Mer information här: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1191">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f8a4a-1192">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1192">Az.ServiceFabric</span></span>
* <span data-ttu-id="f8a4a-1193">Återställ när ett certifikat läggs till i en Virtual Machine Scale Sets-modell men ett undantag genereras. Detta har gjorts för att åtgärda följande fel: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1193">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="f8a4a-1194">Korrigera några felmeddelanden.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1194">Fix some error messages.</span></span>
* <span data-ttu-id="f8a4a-1195">Korrigering av skapande av kluster med ARM-mall som är standard för New-AzServiceFabriCluster som inte fungerade med migrering till Az.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1195">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="f8a4a-1196">Korrigering av tilläggning av kluster/programcertifikat så att endast VM Scale Sets som motsvarar klustret läggs till genom att kontrollera ID för klustret i tillägget.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1196">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="f8a4a-1197">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1197">Az.SignalR</span></span>
* <span data-ttu-id="f8a4a-1198">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1198">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="f8a4a-1199">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1199">Az.Sql</span></span>
* <span data-ttu-id="f8a4a-1200">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1200">Update incorrect online help URLs</span></span>
* <span data-ttu-id="f8a4a-1201">Uppdaterad parameterbeskrivning för LicenseType-parameter med möjliga värden</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1201">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="f8a4a-1202">Korrigering för att uppdatera hanterad instansidentitet som inte fungerar när det är den enda uppdaterade egenskapen</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1202">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="f8a4a-1203">Stöd för anpassad sortering på hanterad instans</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1203">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f8a4a-1204">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1204">Az.Storage</span></span>
* <span data-ttu-id="f8a4a-1205">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1205">Update incorrect online help URLs</span></span>
* <span data-ttu-id="f8a4a-1206">Tillhandahåll detaljerat felmeddelande när en användare försöker hämta/konfigurera klassisk loggning/mått på ett Premium Storage-konto eftersom Premium Storage-kontot inte har stöd för klassisk loggning/mått.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1206">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="f8a4a-1207">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1207">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="f8a4a-1208">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1208">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="f8a4a-1209">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1209">Az.TrafficManager</span></span>
* <span data-ttu-id="f8a4a-1210">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1210">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f8a4a-1211">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1211">Az.Websites</span></span>
* <span data-ttu-id="f8a4a-1212">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1212">Update incorrect online help URLs</span></span>
* <span data-ttu-id="f8a4a-1213">Korrigerar ”New-AzWebAppSSLBinding” så att certifikatet laddas upp till rätt resursgrupp och plats om appen finns i en ASE.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1213">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="f8a4a-1214">Korrigerar ”New-AzWebAppSSLBinding” så att taggarna inte skrivs över på en bindning av ett SSL-certifikat till en app</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1214">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="f8a4a-1215">1.1.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1215">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f8a4a-1216">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1216">Az.Accounts</span></span>
* <span data-ttu-id="f8a4a-1217">Lade till omfattningen ”Lokal” till Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1217">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f8a4a-1218">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1218">Az.Compute</span></span>
* <span data-ttu-id="f8a4a-1219">Namn är nu valfritt i ID-parametern för Restart/Start/Stop/Remove/Set-AzVM och Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1219">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="f8a4a-1220">Uppdaterade beskrivningen av ID i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1220">Updated the description of ID in help files</span></span>
* <span data-ttu-id="f8a4a-1221">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1221">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f8a4a-1222">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1222">Az.DataLakeStore</span></span>
* <span data-ttu-id="f8a4a-1223">Uppdatera sdk-versionen av dataplanet till 1.1.14 för SDK-korrigeringar.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1223">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="f8a4a-1224">Korrigerade hanteringen av negativ accesstime och modificationtime för getfilestatus och liststatus; korrigera asynkront annulleringstoken</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1224">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="f8a4a-1225">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1225">Az.EventGrid</span></span>
* <span data-ttu-id="f8a4a-1226">Uppdaterat för användning av API-versionen 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1226">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="f8a4a-1227">Uppdaterade följande cmdletar för att stödja nytt scenario i API-versionen 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1227">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="f8a4a-1228">New-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1228">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="f8a4a-1229">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1229">Event Time-To-Live,</span></span>
        - <span data-ttu-id="f8a4a-1230">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1230">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="f8a4a-1231">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1231">Dead letter endpoint.</span></span>
    - <span data-ttu-id="f8a4a-1232">Update-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1232">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="f8a4a-1233">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1233">Event Time-To-Live,</span></span>
        - <span data-ttu-id="f8a4a-1234">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1234">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="f8a4a-1235">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1235">Dead letter endpoint.</span></span>
* <span data-ttu-id="f8a4a-1236">Lade till nya enum-värden (storageQueue och hybridConnection) för alternativet EndpointType i cmdletarna New-AzureRmEventGridSubscription och Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1236">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="f8a4a-1237">Visa varningsmeddelanden om skapande eller uppdatering av händelseprenumerationen förväntas medföra manuell åtgärd från användaren.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1237">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f8a4a-1238">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1238">Az.IotHub</span></span>
* <span data-ttu-id="f8a4a-1239">Har uppdaterats till den senaste versionen av SDK:n lotHub</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1239">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="f8a4a-1240">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1240">Az.LogicApp</span></span>
* <span data-ttu-id="f8a4a-1241">Get-AzLogicApp visar en lista över alla som inte har angivet namn</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1241">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="f8a4a-1242">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1242">Az.Resources</span></span>
* <span data-ttu-id="f8a4a-1243">Åtgärdade problem med parameteruppsättningen när parametrarna -ODataQuery och -ResourceId anges för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1243">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="f8a4a-1244">Mer information här: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1244">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="f8a4a-1245">Åtgärdade hantering av parametern -Custom i New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1245">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="f8a4a-1246">Korrigerade stavfel i New-AzDeployment-dokumentationen</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1246">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="f8a4a-1247">Gjorde parametern -MailNickname obligatorisk för New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1247">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="f8a4a-1248">Mer information här: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1248">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="f8a4a-1249">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1249">Az.SignalR</span></span>
* <span data-ttu-id="f8a4a-1250">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1250">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="f8a4a-1251">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1251">Az.Sql</span></span>
* <span data-ttu-id="f8a4a-1252">Konverterade lagringshanteringsklientens beroende av den normala SDK-implementeringen.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1252">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f8a4a-1253">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1253">Az.Storage</span></span>
* <span data-ttu-id="f8a4a-1254">Angav StorageAccountName för lagringskontext som det verkliga namnet på lagringskontot när det skapas med Sas Token, OAuth eller Anonymous</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1254">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="f8a4a-1255">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1255">New-AzStorageContext</span></span>
* <span data-ttu-id="f8a4a-1256">Skapade Sas Token för Blob Snapshot-objekt med parametern -FullUri, åtgärdade den returnerade URI:n så att den blir URI för ögonblicksbild</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1256">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="f8a4a-1257">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1257">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f8a4a-1258">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1258">Az.Websites</span></span>
* <span data-ttu-id="f8a4a-1259">Åtgärdade en bugg i datumparsningen i Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1259">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="f8a4a-1260">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1260">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="f8a4a-1261">1.0.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1261">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="f8a4a-1262">Allmänt</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1262">General</span></span>

- <span data-ttu-id="f8a4a-1263">Allmän tillgänglighet för Az-modulen</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1263">General Availability of Az Module</span></span>
- <span data-ttu-id="f8a4a-1264">Onlinehjälp för varje modul</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1264">Online help for each module</span></span>
- <span data-ttu-id="f8a4a-1265">Mer information och en översikt finns på [Az-informationssidan](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1265">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="f8a4a-1266">Information om hur du migrerar från AzureRM finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1266">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="f8a4a-1267">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1267">Az.Accounts</span></span>
- <span data-ttu-id="f8a4a-1268">Har ändrats från Az.Profile</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1268">Changed from Az.Profile</span></span>
- <span data-ttu-id="f8a4a-1269">Fasta tabellformat för profil- och kontexttyper</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1269">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="f8a4a-1270">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1270">Az.ApiManagement</span></span>
- <span data-ttu-id="f8a4a-1271">Korrigeringar för #7002</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1271">Fixes for #7002</span></span>
- <span data-ttu-id="f8a4a-1272">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1272">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="f8a4a-1273">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1273">Az.Batch</span></span>
- <span data-ttu-id="f8a4a-1274">Lade till möjligheten att se vilken version av Azure Batch Node Agent som körs på var och en av de virtuella datorerna i en pool, via den nya egenskapen `NodeAgentInformation` på `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1274">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="f8a4a-1275">Standarden `Caching` för `PSDataDisk` är nu `ReadWrite` i stället för `None`.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1275">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="f8a4a-1276">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1276">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="f8a4a-1277">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1277">Az.Billing</span></span>
- <span data-ttu-id="f8a4a-1278">Kombinerar cmdletarna för fakturering, förbrukning och UsageAggregates. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1278">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="f8a4a-1279">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1279">Az.CognitivServices</span></span>
- <span data-ttu-id="f8a4a-1280">Lade till kompletterare för SkuName och Typem som är tillgängliga i New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1280">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="f8a4a-1281">Tog bort parameteruppsättningen GetSkusWithAccountParamSetName från Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1281">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="f8a4a-1282">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1282">Az.ContainerInstance</span></span>
- <span data-ttu-id="f8a4a-1283">Stöd för ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1283">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="f8a4a-1284">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1284">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="f8a4a-1285">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1285">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="f8a4a-1286">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1286">Az.DataLakeStore</span></span>
- <span data-ttu-id="f8a4a-1287">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1287">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="f8a4a-1288">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1288">Az.Monitor</span></span>
- <span data-ttu-id="f8a4a-1289">Döpte om Az.Insights till Az.Monitor och andra mindre icke-bakåtkompatibla ändringar. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1289">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="f8a4a-1290">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1290">Az.KeyVault</span></span>
- <span data-ttu-id="f8a4a-1291">Tog bort den inaktuella egenskapen PurgeDisabled från utdatatyper</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1291">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="f8a4a-1292">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1292">Az.MachineLearning</span></span>
- <span data-ttu-id="f8a4a-1293">Inkluderade cmdletarna från modulen Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1293">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="f8a4a-1294">Az.Media</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1294">Az.Media</span></span>
- <span data-ttu-id="f8a4a-1295">Tog bort inaktuella -Tags-alias från New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1295">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="f8a4a-1296">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1296">Az.Network</span></span>
<span data-ttu-id="f8a4a-1297">Stöd har lagts till för konfiguration av RewriteRuleSets i Application Gateway</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1297">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="f8a4a-1298">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1298">New cmdlets added:</span></span>
        - <span data-ttu-id="f8a4a-1299">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1299">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="f8a4a-1300">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1300">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="f8a4a-1301">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1301">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="f8a4a-1302">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1302">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="f8a4a-1303">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1303">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="f8a4a-1304">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1304">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="f8a4a-1305">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1305">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="f8a4a-1306">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1306">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="f8a4a-1307">Cmdletar har uppdaterats med den valfria parametern -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1307">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="f8a4a-1308">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1308">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="f8a4a-1309">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1309">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="f8a4a-1310">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1310">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="f8a4a-1311">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1311">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="f8a4a-1312">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1312">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="f8a4a-1313">New-AzureRmApplicationGatewayUrlPathMapConfig har lagt till KeyVault-stöd för Application Gateway med Identity.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1313">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="f8a4a-1314">Cmdletar har uppdaterats med den valfria parametern -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1314">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="f8a4a-1315">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1315">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="f8a4a-1316">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1316">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="f8a4a-1317">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1317">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="f8a4a-1318">Cmdleten New-AzApplicationGateway har uppdaterats med den valfria parametern -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1318">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="f8a4a-1319">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1319">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="f8a4a-1320">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1320">Az.OperationalInsights</span></span>
- <span data-ttu-id="f8a4a-1321">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1321">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="f8a4a-1322">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1322">Az.Profile</span></span>
- <span data-ttu-id="f8a4a-1323">Modulnamnet har ändrats till Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1323">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="f8a4a-1324">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1324">Az.RecoveryServices</span></span>
- <span data-ttu-id="f8a4a-1325">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1325">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="f8a4a-1326">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1326">Az.Resources</span></span>
- <span data-ttu-id="f8a4a-1327">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1327">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="f8a4a-1328">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1328">Az.ServiceFabric</span></span>
- <span data-ttu-id="f8a4a-1329">Stöd för specificering av certifikat efter eget namn och tumavtryck</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1329">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="f8a4a-1330">Information om fler icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1330">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="f8a4a-1331">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1331">Az.SIgnalR</span></span>
- <span data-ttu-id="f8a4a-1332">Allmän tillgänglighet för PowerShell-cmdletar för SIgnalR</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1332">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="f8a4a-1333">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1333">Az.Sql</span></span>
- <span data-ttu-id="f8a4a-1334">Lade till de nya identifieringstyperna Data_Exfiltration och Unsafe_Action i Threat Detection-cmdletar</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1334">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="f8a4a-1335">Uppdaterade dokumentationsexempel för Sql Auditing-cmdletar</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1335">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="f8a4a-1336">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1336">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="f8a4a-1337">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1337">Az.Storage</span></span>
- <span data-ttu-id="f8a4a-1338">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1338">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="f8a4a-1339">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1339">Az.Websites</span></span>
- <span data-ttu-id="f8a4a-1340">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1340">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="f8a4a-1341">0.7.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1341">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="f8a4a-1342">Allmänt</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1342">General</span></span>

* <span data-ttu-id="f8a4a-1343">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1343">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="f8a4a-1344">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1344">Az.Compute</span></span>

* <span data-ttu-id="f8a4a-1345">Lade till stöd för UltraSSD och Galleriavbildningar i de enkla parameteruppsättningarna för `New-AzVm(ss)`-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1345">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="f8a4a-1346">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1346">Az.DataLakeStore</span></span>

* <span data-ttu-id="f8a4a-1347">Åtgärdade avslutande snedstreck i domänen för adls-konto</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1347">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="f8a4a-1348">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1348">Az.FrontDoor</span></span>

* <span data-ttu-id="f8a4a-1349">Brutna länkar korrigerades</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1349">Fixed some broken links</span></span>
    - <span data-ttu-id="f8a4a-1350">I artiklarna New-AzureRmFrontDoor och Set-AzureRmFrontDoor artiklar korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1350">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="f8a4a-1351">I artikeln New-AzureRmFrontDoorManagedRuleObject korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1351">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="f8a4a-1352">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1352">Az.RecoveryServices</span></span>

* <span data-ttu-id="f8a4a-1353">Lade till valideringar på klientsidan för Azure-filresurs med återställningsåtgärder.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1353">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="f8a4a-1354">Gjorde storageAccountName och storageAccountResourceGroupName valfritt för afs-återställning.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1354">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="f8a4a-1355">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1355">Az.Resources</span></span>

* <span data-ttu-id="f8a4a-1356">Korrigering för https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1356">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="f8a4a-1357">Uppdaterade Get-AzureRmRoleAssignment så att prenumerationsomfattningen används om den anges vid begäran om klassiska administratörer.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1357">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="f8a4a-1358">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1358">Az.Sql</span></span>

* <span data-ttu-id="f8a4a-1359">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1359">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="f8a4a-1360">Korrigerade ett problem med Get-AzureRmSqlDatabaseVulnerabilityAssessment med DotNet-kärna</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1360">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="f8a4a-1361">Ändrade dokumentationen för hjälpmeddelanden som rör SQL Auditing-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1361">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="f8a4a-1362">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1362">Az.Storage</span></span>

* <span data-ttu-id="f8a4a-1363">Lade till -EnableHierarchicalNamespace i New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1363">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="f8a4a-1364">Åtgärdade problemet med att cmdleten Copy File inte kunde återanvända källkontexten på målet om inte -DestContext angetts</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1364">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="f8a4a-1365">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1365">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="f8a4a-1366">Stöd för statisk webbplatskonfiguration</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1366">Support Static Website configuration</span></span>
    - <span data-ttu-id="f8a4a-1367">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1367">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="f8a4a-1368">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1368">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="f8a4a-1369">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1369">Az.Websites</span></span>

* <span data-ttu-id="f8a4a-1370">Set-AzureRmWebApp och Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1370">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="f8a4a-1371">Ny parameter (-AzureStoragePath) har lagts till för att ange att Azure Storage-sökvägar ska monteras i containerappar i Windows och Linux.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1371">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="f8a4a-1372">Använder utdata från den nya cmdleten New-AzureRmWebAppAzureStoragePath som en parameter för att ange sökvägar för Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1372">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="f8a4a-1373">0.6.1 – november 2018</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1373">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="f8a4a-1374">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1374">Az.ApiManagement</span></span>
* <span data-ttu-id="f8a4a-1375">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1375">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="f8a4a-1376">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1376">Az.Automation</span></span>
* <span data-ttu-id="f8a4a-1377">Swagger baserade Azure Automation-cmdletar</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1377">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="f8a4a-1378">Cmdletar för Uppdateringshantering har lagts till</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1378">Added Update Management cmdlets</span></span>
* <span data-ttu-id="f8a4a-1379">Cmdletar för källkontroll har lagts till</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1379">Added Source Control cmdlets</span></span>
* <span data-ttu-id="f8a4a-1380">Remove-AzureRmAutomationHybridWorkerGroup-cmdlet har lagts till</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1380">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="f8a4a-1381">Kommandot för DSC-registreringsnod har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1381">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="f8a4a-1382">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1382">Az.Compute</span></span>
* <span data-ttu-id="f8a4a-1383">Problem med SystemAssigned-identitet har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1383">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="f8a4a-1384">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1384">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="f8a4a-1385">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1385">Az.ContainerInstance</span></span>
* <span data-ttu-id="f8a4a-1386">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1386">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="f8a4a-1387">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1387">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="f8a4a-1388">uppdatera exempelbeskrivningen för marketplace-cmdletar</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1388">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="f8a4a-1389">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1389">Az.Network</span></span>
* <span data-ttu-id="f8a4a-1390">Cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomErreller Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1390">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="f8a4a-1391">ICMP tillbaka till stöd för Azure Firewall-nätverksprotokoll har lagts till</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1391">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="f8a4a-1392">Uppdatera cmdlet Test-AzureRmNetworkWatcherConnectivity, lägga till verifiering av mål-id, adress och port.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1392">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="f8a4a-1393">Åtgärda problem med minnesanvändning i VirtualNetwork-karta</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1393">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="f8a4a-1394">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1394">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="f8a4a-1395">Åtgärda för att ändra principen för en skyddad fildelning.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1395">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="f8a4a-1396">Tidszonsprincipen har konverterats till versaler.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1396">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="f8a4a-1397">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1397">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="f8a4a-1398">Exempel i New-AzureRmRecoveryServicesAsrProtectableItem har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1398">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="f8a4a-1399">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1399">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="f8a4a-1400">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1400">Az.Relay</span></span>
* <span data-ttu-id="f8a4a-1401">Valfri parameter -KeyValue till New-AzureRmRelayKey cmdlet har lagts till, vilket gör det möjligt för användare att tillhandahålla KeyValue.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1401">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="f8a4a-1402">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1402">Az.Resources</span></span>
* <span data-ttu-id="f8a4a-1403">Uppdatera hjälpdokumentation för resursidentitet kopplad till parametrar i `New-AzureRmPolicyAssignment` och `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1403">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="f8a4a-1404">Lägg till ett exempel för New-AzureRmPolicyDefinition som använder -Metadata</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1404">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="f8a4a-1405">Korrigera så att skiftläge behålls i taggnycklar i NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1405">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="f8a4a-1406">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1406">Az.ServiceFabric</span></span>
* <span data-ttu-id="f8a4a-1407">Lägg till utfasningsmeddelanden för kommande icke-kompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1407">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="f8a4a-1408">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1408">Az.Sql</span></span>
* <span data-ttu-id="f8a4a-1409">Nya cmdletar för CRUD-åtgärder på Azure Sql Database-hanterad instans och Azure Sql-hanterad databas</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1409">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="f8a4a-1410">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1410">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="f8a4a-1411">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1411">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="f8a4a-1412">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1412">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="f8a4a-1413">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1413">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="f8a4a-1414">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1414">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="f8a4a-1415">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1415">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="f8a4a-1416">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1416">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="f8a4a-1417">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1417">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="f8a4a-1418">Hantering av utökad granskningsprincip på en server eller en databas har aktiverats.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1418">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="f8a4a-1419">Ny parameter (PredicateExpression) har lagts till för att aktivera filtrering av granskningsloggar.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1419">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="f8a4a-1420">Cmdletar har ändrats så att de använder SQL-klienter i stället för äldre klienter.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1420">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="f8a4a-1421">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1421">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="f8a4a-1422">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1422">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="f8a4a-1423">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1423">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="f8a4a-1424">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1424">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="f8a4a-1425">Problem med att använda Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings med lagringskontots namnparameter har korrigerats</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1425">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="f8a4a-1426">0.5.0 – november 2018</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1426">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="f8a4a-1427">Allmänt</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1427">General</span></span>
* <span data-ttu-id="f8a4a-1428">Lade till resurskompletterare till många kärn-cmdletar – dessa gör att du kan stega genom befintliga resursnamn med TABB vid interaktiva anrop till cmdletar</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1428">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="f8a4a-1429">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1429">Az.Profile</span></span>
* <span data-ttu-id="f8a4a-1430">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1430">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="f8a4a-1431">Bytte namn på parametern TenantId i cmdleten Connect-AzAccount till Tenant och lade till ett alias för TenantId</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1431">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="f8a4a-1432">Uppdaterade TenantId-beskrivningen för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1432">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="f8a4a-1433">Åtgärda felmeddelande för misslyckad inloggning när du tillhandahåller klientdomän</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1433">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="f8a4a-1434">Åtgärda problem med att kontextnamn hamnar i konflikt för konton utan prenumerationer i klientorganisationen</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1434">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="f8a4a-1435">Åtgärda problem med DataLake-slutpunkter vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1435">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="f8a4a-1436">Åtgärdade problem med att Disconnect-AzAccount kastades om den inte anslöts</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1436">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="f8a4a-1437">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1437">Az.CognitiveServices</span></span>
* <span data-ttu-id="f8a4a-1438">Lade till åtgärden Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1438">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f8a4a-1439">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1439">Az.Compute</span></span>
* <span data-ttu-id="f8a4a-1440">Lade till cmdletarna Add-AzVmssVMDataDisk och Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1440">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="f8a4a-1441">Get-AzVMImage visar AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1441">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="f8a4a-1442">Åtgärdade att värdena för alternativen SetAzVMChefExtension -BootstrapOptions och -JsonAttribute inte angavs i json-format.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1442">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f8a4a-1443">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1443">Az.DataLakeStore</span></span>
* <span data-ttu-id="f8a4a-1444">Uppdatera DataLake-paketet till 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1444">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="f8a4a-1445">Lägg till standardsamtidighet för flertrådade åtgärder.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1445">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="f8a4a-1446">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1446">Az.Insights</span></span>
* <span data-ttu-id="f8a4a-1447">Åtgärdade problem #7267 (autoskalningsområde)</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1447">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="f8a4a-1448">Problem med att uppräknade parametrar inte ställdes in ordentligt när du skapade en ny autoskalningsregel (de ställdes alltid in med standardvärdet).</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1448">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="f8a4a-1449">Åtgärdade problem #7513 [Insights] Set-AzDiagnosticSetting kräver uttrycklig specifikation av kategorier när inställningar skapas</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1449">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="f8a4a-1450">Nu kräver inte cmdleten uttrycklig anvisning av kategorierna för att aktiveras under skapande, d.v.s. den fungerar enligt beskrivning</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1450">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f8a4a-1451">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1451">Az.Network</span></span>
* <span data-ttu-id="f8a4a-1452">PeeringType ändrades till en obligatorisk parameter för följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1452">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="f8a4a-1453">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1453">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="f8a4a-1454">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1454">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="f8a4a-1455">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1455">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="f8a4a-1456">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1456">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="f8a4a-1457">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1457">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="f8a4a-1458">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1458">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f8a4a-1459">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1459">Az.PolicyInsights</span></span>
* <span data-ttu-id="f8a4a-1460">Cmdletar för principreparation har lagts till</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1460">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="f8a4a-1461">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1461">Az.Resources</span></span>
* <span data-ttu-id="f8a4a-1462">Korrigering för https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1462">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="f8a4a-1463">Tillåt att resurser listas med parametern -ResourceId för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1463">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="f8a4a-1464">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1464">Az.ServiceBus</span></span>
* <span data-ttu-id="f8a4a-1465">Skrivskyddad MigrationState-egenskap har lagts till i PSServiceBusMigrationConfigurationAttributes, som hjälper till att hålla koll på migreringstillståndet.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1465">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f8a4a-1466">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1466">Az.ServiceFabric</span></span>
* <span data-ttu-id="f8a4a-1467">Åtgärda att lägga till certifikat till Linux-Vmss.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1467">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="f8a4a-1468">Åtgärdade Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1468">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="f8a4a-1469">Använd rätt tumavtryck från nya certifikat (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1469">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="f8a4a-1470">Visa undantag korrekt (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1470">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="f8a4a-1471">Åtgärdade Update-AzServiceFabricDurability så att klusterkonfigurationen uppdateras innan Vmss-åtgärden CreateOrUpdate påbörjas.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1471">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="f8a4a-1472">0.4.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1472">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="f8a4a-1473">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1473">Az.Profile</span></span>
* <span data-ttu-id="f8a4a-1474">Åtgärdade problemet med Get-AzSubscription i CloudShell</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1474">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="f8a4a-1475">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1475">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f8a4a-1476">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1476">Az.Compute</span></span>
* <span data-ttu-id="f8a4a-1477">Nya storlekar lades till i listan över godkända VM-storlekar för vilka accelererat nätverk kommer att aktiveras vid användning av den enkla parameteruppsättningen för New-AzVm</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1477">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="f8a4a-1478">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1478">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f8a4a-1479">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1479">Az.DataLakeStore</span></span>
* <span data-ttu-id="f8a4a-1480">Lägger till stöd för regler för virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1480">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="f8a4a-1481">Get-AzDataLakeStoreVirtualNetworkRule: Hämtar eller listar regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1481">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="f8a4a-1482">Add-AzDataLakeStoreVirtualNetworkRule: Lägger till en regel för virtuellt nätverk i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1482">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="f8a4a-1483">Set-AzDataLakeStoreVirtualNetworkRule: Ändrar den angivna regeln för virtuellt nätverk i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1483">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="f8a4a-1484">Remove-AzDataLakeStoreVirtualNetworkRule: Tar bort en regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1484">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f8a4a-1485">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1485">Az.Network</span></span>
* <span data-ttu-id="f8a4a-1486">Skicka protokollvärdet till serverdelen för att uppdatera cmdleten Test-AzNetworkWatcherConnectivity.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1486">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="f8a4a-1487">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1487">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f8a4a-1488">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1488">Az.Resources</span></span>
* <span data-ttu-id="f8a4a-1489">Åtgärdade problem där Get-AzRoleDefinition genererar ett oläsligt undantag (när standardprofilen inte innehåller någon prenumeration och ingen omfattning har angetts) genom att lägga till ett beskrivande undantag i scenariot.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1489">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="f8a4a-1490">Ställ in ”RoleDefinitionNameParameterSet” som standardparameteruppsättning.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1490">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="f8a4a-1491">0.3.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1491">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="f8a4a-1492">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1492">Azure.Storage</span></span>
* <span data-ttu-id="f8a4a-1493">Åtgärda fel där Kopiera blob/fil inte kopierar metadata när målplatsen har ett problem med metadata</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1493">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="f8a4a-1494">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1494">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="f8a4a-1495">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1495">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="f8a4a-1496">Stöd för att hämta användningsinformation om en Storage-resurs för en specifik plats och för att lägga till ett varningsmeddelande för att hämta användningsinformation om en global Storage-resurs är inaktuellt.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1496">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="f8a4a-1497">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1497">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="f8a4a-1498">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1498">Az.CognitiveServices</span></span>
* <span data-ttu-id="f8a4a-1499">Stöd för Get-AzCognitiveServicesAccountSkus utan ett befintligt konto.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1499">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f8a4a-1500">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1500">Az.Compute</span></span>
* <span data-ttu-id="f8a4a-1501">Åtgärdade fel där Get-AzVM -ResourceGroupName <rg> returnerar fler än 50 resultat om det behövs</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1501">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="f8a4a-1502">Lade till ett exempel för SimpleParameterSet i hjälpen för cmdleten New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1502">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="f8a4a-1503">Ett stavfel i förloppsmeddelandet för Azure Disk Encryption har korrigerats</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1503">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="f8a4a-1504">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1504">Az.DataFactoryV2</span></span>
* <span data-ttu-id="f8a4a-1505">ADF .Net SDK-versionen har uppdaterats till 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1505">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f8a4a-1506">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1506">Az.Network</span></span>
* <span data-ttu-id="f8a4a-1507">Funktionalitet för NetworkProfile har lagts till.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1507">Added NetworkProfile functionality.</span></span> <span data-ttu-id="f8a4a-1508">nya cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1508">new cmdlets added</span></span>
    - <span data-ttu-id="f8a4a-1509">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1509">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="f8a4a-1510">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1510">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="f8a4a-1511">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1511">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="f8a4a-1512">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1512">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="f8a4a-1513">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1513">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="f8a4a-1514">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1514">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="f8a4a-1515">Länk för tjänstassociering på modell för undernät har lagts till</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1515">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="f8a4a-1516">Cmdletarna New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap och Remove-AzVirtualNetworkTap har lagts till</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1516">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="f8a4a-1517">Cmdletarna Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig och Remove-AzNEtworkInterfaceTapConfig har lagts till</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1517">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="f8a4a-1518">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1518">Az.RedisCache</span></span>
* <span data-ttu-id="f8a4a-1519">Tillåt att alla strängar används som storleksparametrar framöver.</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1519">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="f8a4a-1520">Lägg till P5 i popup-fönstret PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1520">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="f8a4a-1521">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1521">Az.Resources</span></span>
* <span data-ttu-id="f8a4a-1522">Parametern -Mode som saknades i Set-AzPolicyDefinition har lagts till</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1522">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="f8a4a-1523">Åtgärdade buggen för cmdleten Get-AzProviderOperation för åtgärder med ursprung som innehåller användare</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1523">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="f8a4a-1524">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1524">Az.Sql</span></span>
* <span data-ttu-id="f8a4a-1525">Ett problem där vissa cmdletar för säkerhetskopiering inte kunde identifiera den aktuella azure-prenumerationen har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1525">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f8a4a-1526">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1526">Az.Websites</span></span>
* <span data-ttu-id="f8a4a-1527">Ny cmdlet: Get-AzWebAppContainerContinuousDeploymentUrl – Hämtar webhook-URL:en för kontinuerlig distribution av container</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1527">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="f8a4a-1528">Nya cmdletar: New-AzWebAppContainerPSSession och Enter-WebAppContainerPSSession – Startar en PowerShell-fjärrsession i en containerapp för windows</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1528">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="f8a4a-1529">0.2.0 – september 2018</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1529">0.2.0 - September 2018</span></span>
 <span data-ttu-id="f8a4a-1530">Första versionen</span><span class="sxs-lookup"><span data-stu-id="f8a4a-1530">Initial Release</span></span>
