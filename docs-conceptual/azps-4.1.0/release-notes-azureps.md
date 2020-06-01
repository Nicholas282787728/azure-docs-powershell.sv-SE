---
title: Viktig information om Azure PowerShell
description: Lär dig mer om alla de senaste uppdateringarna för Azure PowerShell-modulerna.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.openlocfilehash: 60827fe7b4f8c351655046e3711660cdf7ce0513
ms.sourcegitcommit: 10ec909100a70acec94d42f6084e7bf0342c6854
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/19/2020
ms.locfileid: "83631072"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="b6b44-103">Viktig information om Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="b6b44-103">Azure PowerShell release notes</span></span>

## <a name="410---may-2020"></a><span data-ttu-id="b6b44-104">4.1.0 – maj 2020</span><span class="sxs-lookup"><span data-stu-id="b6b44-104">4.1.0 - May 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="b6b44-105">Höjdpunkter sedan den senaste uppdateringen</span><span class="sxs-lookup"><span data-stu-id="b6b44-105">Highlights since the last release</span></span>
* <span data-ttu-id="b6b44-106">PowerShell-versioner som stöds: Windows PowerShell 5.1, PowerShell Core 6.2.4+ och PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="b6b44-106">Supported PowerShell versions: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>
* <span data-ttu-id="b6b44-107">Allmän tillgänglighet för Az.Functions</span><span class="sxs-lookup"><span data-stu-id="b6b44-107">General availability of Az.Functions</span></span> 
* <span data-ttu-id="b6b44-108">Nya stora uppdateringar har gjorts för Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources och Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b6b44-108">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources, and Az.Storage have major release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="b6b44-109">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b6b44-109">Az.Accounts</span></span>
* <span data-ttu-id="b6b44-110">”Add-AzEnvironment” och ”Set-AzEnvironment” har uppdaterats med stöd för parametrarna ”AzureSynapseAnalyticsEndpointResourceId” och ”AzureSynapseAnalyticsEndpointSuffix”</span><span class="sxs-lookup"><span data-stu-id="b6b44-110">Updated 'Add-AzEnvironment' and 'Set-AzEnvironment' to accept parameters 'AzureSynapseAnalyticsEndpointResourceId' and 'AzureSynapseAnalyticsEndpointSuffix'</span></span>
* <span data-ttu-id="b6b44-111">Azure.Core-relaterade sammansättningar har lagts till i Az.Accounts; PowerShell-plattformar som stöds är Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span><span class="sxs-lookup"><span data-stu-id="b6b44-111">Added Azure.Core related assemblies into Az.Accounts, supported PowerShell platforms include Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span></span>

#### <a name="azaks"></a><span data-ttu-id="b6b44-112">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="b6b44-112">Az.Aks</span></span>
* <span data-ttu-id="b6b44-113">API-versionen har uppgraderats till 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="b6b44-113">Upgraded API Version to 2019-10-01</span></span>
* <span data-ttu-id="b6b44-114">Stöds för att skapa AKS med hjälp av Windows-container</span><span class="sxs-lookup"><span data-stu-id="b6b44-114">Supported to create AKS using Windows container</span></span>
* <span data-ttu-id="b6b44-115">Nya cmdletar är tillgängliga: ”New-AzAksNodePool”, ”Update-AzAksNodePool”, ”Remove-AzAksNodePool”,        ”Get-AzAksNodePool”, ”Install-AzAksKubectl”, ”Get-AzAksVersion”</span><span class="sxs-lookup"><span data-stu-id="b6b44-115">Provided new cmdlets: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="b6b44-116">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b6b44-116">Az.ApiManagement</span></span>
* <span data-ttu-id="b6b44-117">Parametrarna ”New-AzApiManagement” och ”Set-AzApiManagement”: [-AssignIdentity] har bytt namn till [-SystemAssignedIdentity]</span><span class="sxs-lookup"><span data-stu-id="b6b44-117">'New-AzApiManagement' and 'Set-AzApiManagement': [-AssignIdentity] parameter renamed as [-SystemAssignedIdentity]</span></span>
* <span data-ttu-id="b6b44-118">”New-AzApiManagement” och ”Set-AzApiManagement”: En ny parameter har lagts till: [-UserAssignedIdentity <String[]>]</span><span class="sxs-lookup"><span data-stu-id="b6b44-118">'New-AzApiManagement' and 'Set-AzApiManagement': New parameter added: [-UserAssignedIdentity <String[]>]</span></span>
* <span data-ttu-id="b6b44-119">”Get-AzApiManagementProperty” har bytt namn till ”Get-AzApiManagementNamedValue”.</span><span class="sxs-lookup"><span data-stu-id="b6b44-119">'Get-AzApiManagementProperty': renamed as 'Get-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="b6b44-120">PropertyId-parametern har bytt namn till NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="b6b44-120">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="b6b44-121">”New-AzApiManagementProperty” har bytt namn till ”New-AzApiManagementNamedValue”.</span><span class="sxs-lookup"><span data-stu-id="b6b44-121">'New-AzApiManagementProperty': renamed as 'New-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="b6b44-122">PropertyId-parametern har bytt namn till NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="b6b44-122">PropertyId parameter renamed as NamedValueId.</span></span> 
* <span data-ttu-id="b6b44-123">”Set-AzApiManagementProperty” har bytt namn till ”Set-AzApiManagementNamedValue”.</span><span class="sxs-lookup"><span data-stu-id="b6b44-123">'Set-AzApiManagementProperty': renamed as 'Set-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="b6b44-124">PropertyId-parametern har bytt namn till NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="b6b44-124">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="b6b44-125">”Remove-AzApiManagementProperty” har bytt namn till ”Remove-AzApiManagementNamedValue”.</span><span class="sxs-lookup"><span data-stu-id="b6b44-125">'Remove-AzApiManagementProperty': renamed as 'Remove-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="b6b44-126">PropertyId-parametern har bytt namn till NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="b6b44-126">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="b6b44-127">Den nya cmdleten Get-AzApiManagementAuthorizationServerClientSecret gör att ”Get-AzApiManagementAuthorizationServer” inte längre returnerar klienthemligheter.</span><span class="sxs-lookup"><span data-stu-id="b6b44-127">Added new 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet and 'Get-AzApiManagementAuthorizationServer' will not return client secret anymore.</span></span>
* <span data-ttu-id="b6b44-128">Den nya cmdleten ”Get-AzApiManagementNamedValueSecretValue” gör att ”Get-AzApiManagementNamedValue” inte returnerar värdet för en hemlighet.</span><span class="sxs-lookup"><span data-stu-id="b6b44-128">Added new 'Get-AzApiManagementNamedValueSecretValue' cmdlet and 'Get-AzApiManagementNamedValue' will not return secret value.</span></span>
* <span data-ttu-id="b6b44-129">Den nya cmdleten ”Get-AzApiManagementOpenIdConnectProviderClientSecret” gör att ”Get-AzApiManagementOpenIdConnectProvider” inte längre returnerar klienthemligheter.</span><span class="sxs-lookup"><span data-stu-id="b6b44-129">Added new 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet and 'Get-AzApiManagementOpenIdConnectProvider' will not return client secret anymore.</span></span>
* <span data-ttu-id="b6b44-130">Den nya cmdleten ”Get-AzApiManagementSubscriptionKey” gör att ”Get-AzApiManagementSubscription” inte längre returnerar prenumerationsnycklar.</span><span class="sxs-lookup"><span data-stu-id="b6b44-130">Added new 'Get-AzApiManagementSubscriptionKey' cmdlet and 'Get-AzApiManagementSubscription' will not return subscription keys anymore.</span></span>
* <span data-ttu-id="b6b44-131">Den nya cmdleten ”Get-AzApiManagementTenantAccessSecret” gör att ”Get-AzApiManagementTenantAccess” inte längre returnerar nycklar.</span><span class="sxs-lookup"><span data-stu-id="b6b44-131">Added new 'Get-AzApiManagementTenantAccessSecret' cmdlet and 'Get-AzApiManagementTenantAccess' will not return keys anymore.</span></span>
* <span data-ttu-id="b6b44-132">Den nya cmdleten ”Get-AzApiManagementTenantGitAccessSecret” gör att ”Get-AzApiManagementTenantGitAccess” inte längre returnerar nycklar.</span><span class="sxs-lookup"><span data-stu-id="b6b44-132">Added new 'Get-AzApiManagementTenantGitAccessSecret' cmdlet and 'Get-AzApiManagementTenantGitAccess' will not return keys anymore.</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="b6b44-133">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="b6b44-133">Az.ApplicationInsights</span></span>
* <span data-ttu-id="b6b44-134">Tillagda parametrar: ”RetentionInDays” ”PublicNetworkAccessForIngestion” ”PublicNetworkAccessForQuery” för ”New-AzApplicationInsights”</span><span class="sxs-lookup"><span data-stu-id="b6b44-134">Added Parameters: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span></span>
* <span data-ttu-id="b6b44-135">Cmdleten ”Update-AzApplicationInsights” har skapats</span><span class="sxs-lookup"><span data-stu-id="b6b44-135">Created cmdlet 'Update-AzApplicationInsights'</span></span>
* <span data-ttu-id="b6b44-136">Cmdletar har skapats för länkat lagringskonto</span><span class="sxs-lookup"><span data-stu-id="b6b44-136">Created cmdlets for Linked Storage Account</span></span>

#### <a name="azbatch"></a><span data-ttu-id="b6b44-137">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="b6b44-137">Az.Batch</span></span>
* <span data-ttu-id="b6b44-138">Az.Batch har uppdaterats att använda ”Microsoft.Azure.Batch” SDK version 13.0.0 och ”Microsoft.Azure.Management.Batch” SDK version 9.0.0.</span><span class="sxs-lookup"><span data-stu-id="b6b44-138">Updated Az.Batch to use 'Microsoft.Azure.Batch' SDK version 13.0.0 and 'Microsoft.Azure.Management.Batch' SDK version 9.0.0.</span></span>
* <span data-ttu-id="b6b44-139">Nu kan du välja vilken typ av certifikat du lägger till genom att använda den nya parametern ”-CertificateKind” med ”New-AzBatchCertificate”.</span><span class="sxs-lookup"><span data-stu-id="b6b44-139">Added the ability to select the kind of certificate being added using the new '-CertificateKind' parameter to 'New-AzBatchCertificate'.</span></span>
* <span data-ttu-id="b6b44-140">Egenskapen ”ApplicationPackages” har tagits bort från ”PSApplication”, som tidigare alltid var ''.</span><span class="sxs-lookup"><span data-stu-id="b6b44-140">Removed 'ApplicationPackages' property from 'PSApplication' which was previously always ''.</span></span>
  - <span data-ttu-id="b6b44-141">Specifika paket i ett program kan nu hämtas med hjälp av ”Get-AzBatchApplicationPackage”.</span><span class="sxs-lookup"><span data-stu-id="b6b44-141">The specific packages inside of an application now can be retrieved using 'Get-AzBatchApplicationPackage'.</span></span> <span data-ttu-id="b6b44-142">Ett exempel: ”Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication”.</span><span class="sxs-lookup"><span data-stu-id="b6b44-142">For example: 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span></span>
* <span data-ttu-id="b6b44-143">Nu när du skapar en pool med hjälp av ”New-AzBatchPool” kan egenskapen ”VirtualMachineImageId” för ”PSImageReference” endast referera till en Shared Image Gallery-avbildning.</span><span class="sxs-lookup"><span data-stu-id="b6b44-143">When creating a pool using 'New-AzBatchPool', the 'VirtualMachineImageId' property of 'PSImageReference' can now only refer to a Shared Image Gallery image.</span></span>
* <span data-ttu-id="b6b44-144">När du skapar en pool med hjälp av ”New-AzBatchPool” kan poolen etableras utan en offentlig IP-adress med hjälp av den nya egenskapen ”PublicIPAddressConfiguration” för ”PSNetworkConfiguration”.</span><span class="sxs-lookup"><span data-stu-id="b6b44-144">When creating a pool using 'New-AzBatchPool', the pool can be provisioned without a public IP using the new 'PublicIPAddressConfiguration' property of 'PSNetworkConfiguration'.</span></span>
  - <span data-ttu-id="b6b44-145">Egenskapen ”PublicIPs” för ”PSNetworkConfiguration” har också flyttats till ”PSPublicIPAddressConfiguration”.</span><span class="sxs-lookup"><span data-stu-id="b6b44-145">The 'PublicIPs' property of 'PSNetworkConfiguration' has moved in to 'PSPublicIPAddressConfiguration' as well.</span></span> <span data-ttu-id="b6b44-146">Den här egenskapen kan bara anges om ”IPAddressProvisioningType” är ”UserManaged”.</span><span class="sxs-lookup"><span data-stu-id="b6b44-146">This property can only be specified if 'IPAddressProvisioningType' is 'UserManaged'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b6b44-147">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b6b44-147">Az.Compute</span></span>
* <span data-ttu-id="b6b44-148">Parametern HostId har lagts till för cmdleten ”Update-AzVM”t</span><span class="sxs-lookup"><span data-stu-id="b6b44-148">Added HostId parameter to 'Update-AzVM' cmdlet</span></span>
* <span data-ttu-id="b6b44-149">Hjälpdokumenten har uppdaterats för cmdletarna ”New-AzVMConfig”, ”New-AzVmssConfig”, ”Update-AzVmss”, ”Set-AzVMOperatingSystem” och ”Set-AzVmssOsProfile”.</span><span class="sxs-lookup"><span data-stu-id="b6b44-149">Updated Help documents for 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' and 'Set-AzVmssOsProfile' cmdlets.</span></span>
* <span data-ttu-id="b6b44-150">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="b6b44-150">Breaking changes</span></span>
    - <span data-ttu-id="b6b44-151">Parametern FilterExpression tas bort från cmdleten ”Get-AzVMImage”.</span><span class="sxs-lookup"><span data-stu-id="b6b44-151">FilterExpression parameter is removed from 'Get-AzVMImage' cmdlet.</span></span>
    - <span data-ttu-id="b6b44-152">Parametern AssignIdentity tas bort från cmdletarna ”New-AzVmssConfig”, ”New-AzVMConfig” och ”Update-AzVM”.</span><span class="sxs-lookup"><span data-stu-id="b6b44-152">AssignIdentity parameter is removed from 'New-AzVmssConfig', 'New-AzVMConfig' and 'Update-AzVM' cmdlets.</span></span>
    - <span data-ttu-id="b6b44-153">AutomaticRepairMaxInstanceRepairsPercent tas bort från cmdletarna ”New-AzVmssConfig” och ”Update-AzVmss”.</span><span class="sxs-lookup"><span data-stu-id="b6b44-153">AutomaticRepairMaxInstanceRepairsPercent is removed from 'New-AzVmssConfig' and 'Update-AzVmss' cmdlets.</span></span>
    - <span data-ttu-id="b6b44-154">Egenskaperna AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus och VirtualMachineScaleSetsColocationStatus tas bort från ProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="b6b44-154">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus and VirtualMachineScaleSetsColocationStatus properties are removed from ProximityPlacementGroup.</span></span>
    - <span data-ttu-id="b6b44-155">Egenskapen MaxInstanceRepairsPercent tas bort från AutomaticRepairsPolicy.</span><span class="sxs-lookup"><span data-stu-id="b6b44-155">MaxInstanceRepairsPercent property is removed from AutomaticRepairsPolicy.</span></span>
    - <span data-ttu-id="b6b44-156">Typerna AvailabilitySets, VirtualMachines och VirtualMachineScaleSets ändras från IList<SubResource> till IList<SubResourceWithColocationStatus>.</span><span class="sxs-lookup"><span data-stu-id="b6b44-156">The types of AvailabilitySets, VirtualMachines and VirtualMachineScaleSets are changed from IList<SubResource> to IList<SubResourceWithColocationStatus>.</span></span>
* <span data-ttu-id="b6b44-157">Beskrivningen för cmdleten ”Get-AzVM” har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="b6b44-157">Description for 'Get-AzVM' cmdlet has been updated to better describe it.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="b6b44-158">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b6b44-158">Az.DataFactory</span></span>
* <span data-ttu-id="b6b44-159">CRUD-stöd för egenskaper för dataflödeskörning  i hanterad IR.</span><span class="sxs-lookup"><span data-stu-id="b6b44-159">Supported CRUD of data flow runtime properties in Managed IR.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="b6b44-160">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="b6b44-160">Az.FrontDoor</span></span>
* <span data-ttu-id="b6b44-161">Nya cmdletar har lagts till för att skapa, uppdatera, hämta och ta bort (CRUD) Front Door-regelmotorobjekt</span><span class="sxs-lookup"><span data-stu-id="b6b44-161">Added new cmdlets for creation, update, retreival, and deletion of Front Door Rules Engine object</span></span>
* <span data-ttu-id="b6b44-162">Hjälp-cmdletar har lagts till för konstruktion av Front Door-regelmotorobjekt</span><span class="sxs-lookup"><span data-stu-id="b6b44-162">Added helper cmdlets for construction of Front Door Rules Engine object</span></span>
* <span data-ttu-id="b6b44-163">Regelmotorreferens har lagts till för Front Door-hanteringsregelobjekt.</span><span class="sxs-lookup"><span data-stu-id="b6b44-163">Added Rules Engine reference to Front Door Routing Rule object.</span></span>
* <span data-ttu-id="b6b44-164">Parametrar för Private Link har lagts till för Front Door-serverdelsobjekt</span><span class="sxs-lookup"><span data-stu-id="b6b44-164">Added Private Link parameters to Front Door Backend object</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="b6b44-165">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="b6b44-165">Az.Functions</span></span>
* <span data-ttu-id="b6b44-166">Allmän tillgänglighet för ”Az.Functions”-modulen</span><span class="sxs-lookup"><span data-stu-id="b6b44-166">General availability of ''Az.Functions'' module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="b6b44-167">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="b6b44-167">Az.HDInsight</span></span>
* <span data-ttu-id="b6b44-168">Stöd för diskkryptering med kundhanterad nyckel.</span><span class="sxs-lookup"><span data-stu-id="b6b44-168">Supported Customer-managed key disk encryption.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="b6b44-169">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="b6b44-169">Az.HealthcareApis</span></span>
* <span data-ttu-id="b6b44-170">Åtkomstprinciper använder inte längre det aktiva huvudkontot som standard</span><span class="sxs-lookup"><span data-stu-id="b6b44-170">Access policies are no longer defaulted to the current principal</span></span>

#### <a name="aziothub"></a><span data-ttu-id="b6b44-171">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="b6b44-171">Az.IotHub</span></span>
* <span data-ttu-id="b6b44-172">En cmdlet har lagts till som anropar en fråga i en IoT-hubb för att hämta information med ett SQL-liknande språk.</span><span class="sxs-lookup"><span data-stu-id="b6b44-172">Added cmdlet to invoke a query in an IoT hub to retrieve information using a SQL-like language.</span></span>
* <span data-ttu-id="b6b44-173">Problemet som gjorde att ”Add-AzIotHubDevice” inte skapade en Edge-aktiverad enhet utan underordnade enheter har åtgärdats [#11597]</span><span class="sxs-lookup"><span data-stu-id="b6b44-173">Fix issue that 'Add-AzIotHubDevice' fails to create Edge Enabled Device without child devices [#11597]</span></span>
* <span data-ttu-id="b6b44-174">En cmdlet har lagts till för att generera SAS-token för en Iot-hubb, enhet eller modul.</span><span class="sxs-lookup"><span data-stu-id="b6b44-174">Added cmdlet to generate SAS token for Iot Hub, device or module.</span></span>
* <span data-ttu-id="b6b44-175">En cmdlet har lagts till för att anropa en måttfråga om konfiguration.</span><span class="sxs-lookup"><span data-stu-id="b6b44-175">Added cmdlet to invoke configuration metrics query.</span></span>
* <span data-ttu-id="b6b44-176">Hantera automatisk distribution av IoT Edge i stor skala.</span><span class="sxs-lookup"><span data-stu-id="b6b44-176">Manage IoT Edge automatic deployment at scale.</span></span> <span data-ttu-id="b6b44-177">Nya cmdlet:ar är:</span><span class="sxs-lookup"><span data-stu-id="b6b44-177">New cmdlets are:</span></span>
    - <span data-ttu-id="b6b44-178">”Add-AzIotHubDeployment”</span><span class="sxs-lookup"><span data-stu-id="b6b44-178">'Add-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="b6b44-179">”Get-AzIotHubDeployment”</span><span class="sxs-lookup"><span data-stu-id="b6b44-179">'Get-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="b6b44-180">”Remove-AzIotHubDeployment”</span><span class="sxs-lookup"><span data-stu-id="b6b44-180">'Remove-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="b6b44-181">”Set-AzIotHubDeployment”</span><span class="sxs-lookup"><span data-stu-id="b6b44-181">'Set-AzIotHubDeployment'</span></span>
* <span data-ttu-id="b6b44-182">En cmdlet har lagts till för att anropa en måttfråga om IoT Edge-distribution.</span><span class="sxs-lookup"><span data-stu-id="b6b44-182">Added cmdlet to invoke an IoT Edge deployment metrics query.</span></span>
* <span data-ttu-id="b6b44-183">En cmdlet har lagts till för att tillämpa konfigurationsinnehåll på den angivna gränsenheten.</span><span class="sxs-lookup"><span data-stu-id="b6b44-183">Added cmdlet to apply the configuration content to the specified edge device.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="b6b44-184">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b6b44-184">Az.KeyVault</span></span>
* <span data-ttu-id="b6b44-185">Två alias har tagits bort: ”New-AzKeyVaultCertificateAdministratorDetails” och ”New-AzKeyVaultCertificateOrganizationDetails”</span><span class="sxs-lookup"><span data-stu-id="b6b44-185">Removed two aliases: 'New-AzKeyVaultCertificateAdministratorDetails' and 'New-AzKeyVaultCertificateOrganizationDetails'</span></span>
* <span data-ttu-id="b6b44-186">Nu är mjuk borttagning aktiverat som standard när ett nyckelvalv skapas</span><span class="sxs-lookup"><span data-stu-id="b6b44-186">Enabled soft delete by default when creating a key vault</span></span>
* <span data-ttu-id="b6b44-187">Nätverksregler kan ställas in för att styra åtkomsten från särskilda nätverksplatser när du skapar ett nyckelvalv</span><span class="sxs-lookup"><span data-stu-id="b6b44-187">Network rules can be set to govern the accessibility from specific network locations when creating a key vault</span></span>
* <span data-ttu-id="b6b44-188">Stöd för BYOK (Bring Your Own Key) har lagts till</span><span class="sxs-lookup"><span data-stu-id="b6b44-188">Added support to bring your own key (BYOK)</span></span>
    - <span data-ttu-id="b6b44-189">”Add-AzKeyVaultKey” stöder generering av en KeyExchange-nyckel</span><span class="sxs-lookup"><span data-stu-id="b6b44-189">'Add-AzKeyVaultKey' supports generating a key exchange key</span></span>
    - <span data-ttu-id="b6b44-190">”Get-AzKeyVaultKey” stöder nedladdning av en offentlig nyckel i PEM-format</span><span class="sxs-lookup"><span data-stu-id="b6b44-190">'Get-AzKeyVaultKey' supports downloading a public key in PEM format</span></span>
* <span data-ttu-id="b6b44-191">”KeyOps”-delen av hjälpdokumentet för ”Add-AzKeyVaultKey” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="b6b44-191">Updated the 'KeyOps' part of the help document of 'Add-AzKeyVaultKey'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="b6b44-192">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b6b44-192">Az.Monitor</span></span>
* <span data-ttu-id="b6b44-193">Bugg för ”Set-AzDiagnosticSettings” har åtgärdats; kvarhållningsprincipen tillämpas inte på alla kategorier [#11589]</span><span class="sxs-lookup"><span data-stu-id="b6b44-193">Fixed bug for 'Set-AzDiagnosticSettings', retention policy won't apply to all categories [#11589]</span></span>
* <span data-ttu-id="b6b44-194">Stöd för WebTest-tillgänglighetskriterier för måttavisering V2</span><span class="sxs-lookup"><span data-stu-id="b6b44-194">Supported WebTest availability criteria for metric alert V2</span></span>
    - <span data-ttu-id="b6b44-195">”New-AzMetricAlertRuleV2Criteria”: ett alternativ för att skapa tillgänglighetskriterier för webbtest har lagts till</span><span class="sxs-lookup"><span data-stu-id="b6b44-195">'New-AzMetricAlertRuleV2Criteria': an option to create webtest availability criteria was added</span></span>
    - <span data-ttu-id="b6b44-196">”Add-AzMetricAlertRuleV2”: stöd för de nya tillgänglighetskriterierna för webbtest</span><span class="sxs-lookup"><span data-stu-id="b6b44-196">'Add-AzMetricAlertRuleV2': supports the new webtest availability criteria</span></span>
* <span data-ttu-id="b6b44-197">Redundant definition har tagits bort för RetentionPolicy i PSLogProfile [#7608]</span><span class="sxs-lookup"><span data-stu-id="b6b44-197">Removed redundant definition for RetentionPolicy in PSLogProfile [#7608]</span></span>
* <span data-ttu-id="b6b44-198">Redundanta egenskaper som definierats i PSEventData har tagits bort [#11353]</span><span class="sxs-lookup"><span data-stu-id="b6b44-198">Removed redundant properties difined in PSEventData [#11353]</span></span>
* <span data-ttu-id="b6b44-199">”Get-AzLog” har bytt namn till ”Get-AzActivityLog”</span><span class="sxs-lookup"><span data-stu-id="b6b44-199">Renamed 'Get-AzLog' to 'Get-AzActivityLog'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b6b44-200">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b6b44-200">Az.Network</span></span>
* <span data-ttu-id="b6b44-201">Attribut för icke-bakåtkompatibel ändring har lagts till för att meddela att standardbeteendet för zoner kommer att ändras</span><span class="sxs-lookup"><span data-stu-id="b6b44-201">Added breaking change attribute to notify that Zone default behaviour will be changed</span></span>
    - <span data-ttu-id="b6b44-202">”New-AzPublicIpAddress”</span><span class="sxs-lookup"><span data-stu-id="b6b44-202">'New-AzPublicIpAddress'</span></span>
    - <span data-ttu-id="b6b44-203">”New-AzPublicIpPrefix”</span><span class="sxs-lookup"><span data-stu-id="b6b44-203">'New-AzPublicIpPrefix'</span></span>
    - <span data-ttu-id="b6b44-204">”New-AzLoadBalancerFrontendIpConfig”</span><span class="sxs-lookup"><span data-stu-id="b6b44-204">'New-AzLoadBalancerFrontendIpConfig'</span></span>
* <span data-ttu-id="b6b44-205">Stöd har lagts till för en ny resurs på den översta nivån, SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="b6b44-205">Added support for a new top level resource SecurityPartnerProvider</span></span>
    - <span data-ttu-id="b6b44-206">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="b6b44-206">New cmdlets added:</span></span>
        - <span data-ttu-id="b6b44-207">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="b6b44-207">New-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="b6b44-208">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="b6b44-208">Remove-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="b6b44-209">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="b6b44-209">Get-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="b6b44-210">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="b6b44-210">Set-AzSecurityPartnerProvider</span></span>
* <span data-ttu-id="b6b44-211">”RequiredZoneNames” har lagts till för ”PSPrivateLinkResource” och ”GroupId” för ”PSPrivateEndpointConnection”</span><span class="sxs-lookup"><span data-stu-id="b6b44-211">Added 'RequiredZoneNames' on 'PSPrivateLinkResource' and 'GroupId' on 'PSPrivateEndpointConnection'</span></span>
* <span data-ttu-id="b6b44-212">Fel parametertyp för SuccessThresholdRoundTripTimeMs-parametern för New-AzNetworkWatcherConnectionMonitorTestConfigurationObject har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="b6b44-212">Fixed incorrect type of SuccessThresholdRoundTripTimeMs parameter for New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>
* <span data-ttu-id="b6b44-213">VirtualWan-cmdletar har uppdaterats för att ange AllowVnetToVnetTraffic-argumentets standardvärde till True.</span><span class="sxs-lookup"><span data-stu-id="b6b44-213">Updated VirtualWan cmdlets to set default value of AllowVnetToVnetTraffic argument to True.</span></span>
    - <span data-ttu-id="b6b44-214">”New-AzVirtualWan”</span><span class="sxs-lookup"><span data-stu-id="b6b44-214">'New-AzVirtualWan'</span></span>
    - <span data-ttu-id="b6b44-215">”Update-AzVirtualWan”</span><span class="sxs-lookup"><span data-stu-id="b6b44-215">'Update-AzVirtualWan'</span></span>
* <span data-ttu-id="b6b44-216">Nya cmdletar har lagts till för att stödja DNS-zongrupp för privat slutpunkt</span><span class="sxs-lookup"><span data-stu-id="b6b44-216">Added new cmdlets to support DNS zone group for private endpoint</span></span>
    - <span data-ttu-id="b6b44-217">”New-AzPrivateDnsZoneConfig”</span><span class="sxs-lookup"><span data-stu-id="b6b44-217">'New-AzPrivateDnsZoneConfig'</span></span>
    - <span data-ttu-id="b6b44-218">”Get-AzPrivateDnsZoneGroup”</span><span class="sxs-lookup"><span data-stu-id="b6b44-218">'Get-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="b6b44-219">”New-AzPrivateDnsZoneGroup”</span><span class="sxs-lookup"><span data-stu-id="b6b44-219">'New-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="b6b44-220">”Set-AzPrivateDnsZoneGroup”</span><span class="sxs-lookup"><span data-stu-id="b6b44-220">'Set-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="b6b44-221">”Remove-AzPrivateDnsZoneGroup”</span><span class="sxs-lookup"><span data-stu-id="b6b44-221">'Remove-AzPrivateDnsZoneGroup'</span></span>
* <span data-ttu-id="b6b44-222">Parametrarna ”DNSEnableProxy”, ”DNSRequireProxyForNetworkRules” och ”DNSServers” har lagts till för ”AzureFirewall”</span><span class="sxs-lookup"><span data-stu-id="b6b44-222">Added 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' and 'DNSServers' parameters to 'AzureFirewall'</span></span>
* <span data-ttu-id="b6b44-223">Parametrarna ”EnableDnsProxy”, ”DnsProxyNotRequiredForNetworkRule” och ”DnsServer” har lagts till för ”AzureFirewall”</span><span class="sxs-lookup"><span data-stu-id="b6b44-223">Added 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' and 'DnsServer' parameters to 'AzureFirewall'</span></span>
    - <span data-ttu-id="b6b44-224">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="b6b44-224">Updated cmdlet:</span></span>
        - <span data-ttu-id="b6b44-225">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="b6b44-225">New-AzFirewall</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="b6b44-226">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="b6b44-226">Az.OperationalInsights</span></span>
* <span data-ttu-id="b6b44-227">Äldre kod har uppdaterats för att tillämpa ny genererad SDK</span><span class="sxs-lookup"><span data-stu-id="b6b44-227">Updated legacy code to apply new generated SDK</span></span>
* <span data-ttu-id="b6b44-228">Cmdletar har tagits bort på grund av föråldrade API:er</span><span class="sxs-lookup"><span data-stu-id="b6b44-228">Deleted cmdlets due to deprecated APIs</span></span>
    - <span data-ttu-id="b6b44-229">”Get-AzOperationalInsightsSavedSearchResult” (alias ”Get-AzOperationalInsightsSavedSearchResults”)</span><span class="sxs-lookup"><span data-stu-id="b6b44-229">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span></span>
    - <span data-ttu-id="b6b44-230">”Get-AzOperationalInsightsSearchResult” (alias ”Get-AzOperationalInsightsSearchResults”)</span><span class="sxs-lookup"><span data-stu-id="b6b44-230">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span></span>
    - <span data-ttu-id="b6b44-231">”Get-AzOperationalInsightsLinkTarget” (alias ”Get-AzOperationalInsightsLinkTargets”)</span><span class="sxs-lookup"><span data-stu-id="b6b44-231">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span></span>
* <span data-ttu-id="b6b44-232">Parametrar har lagts till för ”Set-AzOperationalInsightsWorkspace” och ”New-AzOperationalInsightsWorkspace”</span><span class="sxs-lookup"><span data-stu-id="b6b44-232">Added parameters for 'Set-AzOperationalInsightsWorkspace' and 'New-AzOperationalInsightsWorkspace'</span></span>
* <span data-ttu-id="b6b44-233">Cmdletar har skapats för länkat lagringskonto</span><span class="sxs-lookup"><span data-stu-id="b6b44-233">Created cmdlets for Linked Stoarge Account</span></span>
* <span data-ttu-id="b6b44-234">Cmdletar har skapats för kluster och länkad tjänst</span><span class="sxs-lookup"><span data-stu-id="b6b44-234">Created cmdlets for Clusters and Linked Service</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b6b44-235">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b6b44-235">Az.RecoveryServices</span></span>
* <span data-ttu-id="b6b44-236">Azure Site Recovery: Stöd har lagts till för att skydda VM-närhetsplaceringsgrupper för Azure till Azure-provider.</span><span class="sxs-lookup"><span data-stu-id="b6b44-236">Azure Site Recovery added support for protecting proximity placement group virtual machines for Azure to Azure provider.</span></span>
* <span data-ttu-id="b6b44-237">Azure Site Recovery: Stöd har lagts till för replikering mellan zoner.</span><span class="sxs-lookup"><span data-stu-id="b6b44-237">Azure Site Recovery added support for zone to zone replication.</span></span>
* <span data-ttu-id="b6b44-238">Azure Backup: Stöd har lagts till för långsiktig kvarhållning för Azure FileShare-återställningspunkter.</span><span class="sxs-lookup"><span data-stu-id="b6b44-238">Azure Backup Added Long term retention support for Azure FileShare Recovery Points.</span></span>
* <span data-ttu-id="b6b44-239">Azure Backup: Egenskaper för diskexkludering har lagts till för cmdlet-utdata från ”Get-AzRecoveryServicesBackupItem”.</span><span class="sxs-lookup"><span data-stu-id="b6b44-239">Azure Backup Added disk exclusion properties to 'Get-AzRecoveryServicesBackupItem' cmdlet output.</span></span>
* <span data-ttu-id="b6b44-240">En privat slutpunkt har lagts till för filen med valvets autentiseringsuppgifter för Site Recovery-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="b6b44-240">Added private endpoint for Vault credential file for site recovery service.</span></span>

#### <a name="azresources"></a><span data-ttu-id="b6b44-241">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b6b44-241">Az.Resources</span></span>
* <span data-ttu-id="b6b44-242">En varning har lagts till om visningsfördröjning när en ny rolldefinition skapas</span><span class="sxs-lookup"><span data-stu-id="b6b44-242">Added message warning about view delay when creating a new Role Definition</span></span>
* <span data-ttu-id="b6b44-243">Princip-cmdletar har ändrats för utmatning av starkt typifierade objekt</span><span class="sxs-lookup"><span data-stu-id="b6b44-243">Changed policy cmdlets to output strongly-typed objects</span></span>
* <span data-ttu-id="b6b44-244">Parametern ”-TenantLevel” har tagits bort för användning med ”Get-AzResourceLock” [#11335]</span><span class="sxs-lookup"><span data-stu-id="b6b44-244">Removed '-TenantLevel' parameter used for on the 'Get-AzResourceLock' cmdlet [#11335]</span></span>
* <span data-ttu-id="b6b44-245">”Remove-AzResourceGroup -Id ResourceId” har åtgärdats [#9882]</span><span class="sxs-lookup"><span data-stu-id="b6b44-245">Fixed 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span></span>
* <span data-ttu-id="b6b44-246">En ny cmdlet har lagts till för att hämta What-If-resultat för ARM-mallar i omfånget för resursgrupper: ”Get-AzDeploymentResourceGroupWhatIfResult”</span><span class="sxs-lookup"><span data-stu-id="b6b44-246">Added new cmdlet for getting ARM template What-If results at resource group scope: 'Get-AzDeploymentResourceGroupWhatIfResult'</span></span>
* <span data-ttu-id="b6b44-247">En ny cmdlet har lagts till för att hämta What-If-resultat för ARM-mallar i prenumerationsomfånget: ”Get-AzDeploymentWhatIfResult”</span><span class="sxs-lookup"><span data-stu-id="b6b44-247">Added new cmdlet for getting ARM template What-If results at subscription scope: 'Get-AzDeploymentWhatIfResult'</span></span>
   - <span data-ttu-id="b6b44-248">Alias: ”Get-AzSubscriptionDeploymentWhatIf”</span><span class="sxs-lookup"><span data-stu-id="b6b44-248">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span></span>
* <span data-ttu-id="b6b44-249">Parametrarna ”-WhatIf” och ”-Confirm” har åsidosatts för ”New-AzDeployment” och ”New-AzResourceGroupDeployment” för att använda What-If-resultat för ARM-mallar</span><span class="sxs-lookup"><span data-stu-id="b6b44-249">Overrode '-WhatIf' and '-Confirm' parameters for 'New-AzDeployment' and 'New-AzResourceGroupDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="b6b44-250">Ett utfasningsmeddelande har lagts till för parametern ”ApiVersion” i distributions-cmdletar</span><span class="sxs-lookup"><span data-stu-id="b6b44-250">Added deprecation message for 'ApiVersion' parameter in deployment cmdlets</span></span>
* <span data-ttu-id="b6b44-251">En funktion har lagts till för att visa förbättrade felmeddelanden för distributionsfel</span><span class="sxs-lookup"><span data-stu-id="b6b44-251">Added capability to show improved error messages for deployment failures</span></span>
* <span data-ttu-id="b6b44-252">CorrelationId-loggning har lagts till för distributionsfel</span><span class="sxs-lookup"><span data-stu-id="b6b44-252">Added correlationId logging for deployment failures</span></span>
* <span data-ttu-id="b6b44-253">Egenskapen ”error” har lagts till i utdata från distributionsskript</span><span class="sxs-lookup"><span data-stu-id="b6b44-253">Added 'error' property to the deployment script output</span></span>
* <span data-ttu-id="b6b44-254">Nuget Microsoft.Azure.Management.ResourceManager har uppdaterats till ”3.7.1-preview”</span><span class="sxs-lookup"><span data-stu-id="b6b44-254">Updated nuget Microsoft.Azure.Management.ResourceManager to '3.7.1-preview'</span></span>
* <span data-ttu-id="b6b44-255">Specifika testfall har tagits bort då egenskapen Error i DeploymentValidateResult har ändrats till lässkyddad från nuget 3.7.1-preview</span><span class="sxs-lookup"><span data-stu-id="b6b44-255">Removed specific test cases as Error property in DeploymentValidateResult has changed to readonly from nuget 3.7.1-preview</span></span>
* <span data-ttu-id="b6b44-256">GenericResourceExpanded har flyttats från SDK ResourceManager 3.7.1-preview</span><span class="sxs-lookup"><span data-stu-id="b6b44-256">Brought GenericResourceExpanded from SDK ResourceManager 3.7.1-preview</span></span>
* <span data-ttu-id="b6b44-257">Stöd för taggar har lagts till för alla Get-cmdletar för distribution, samt</span><span class="sxs-lookup"><span data-stu-id="b6b44-257">Added tag support for all Get cmdlets for deployment, as well as</span></span>
    - <span data-ttu-id="b6b44-258">”New-AzDeployment”</span><span class="sxs-lookup"><span data-stu-id="b6b44-258">'New-AzDeployment'</span></span>
    - <span data-ttu-id="b6b44-259">”New-AzManagementGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="b6b44-259">'New-AzManagementGroupDeployment'</span></span>
    - <span data-ttu-id="b6b44-260">”New-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="b6b44-260">'New-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="b6b44-261">”New-AzTenantDeployment”</span><span class="sxs-lookup"><span data-stu-id="b6b44-261">'New-AzTenantDeployment'</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="b6b44-262">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b6b44-262">Az.ServiceFabric</span></span>
* <span data-ttu-id="b6b44-263">En bugg har åtgärdats som gjorde att --SecretIdentifier fick fel tumavtryck för certifikat när ett certifikat lades till</span><span class="sxs-lookup"><span data-stu-id="b6b44-263">Fixed bug in add certificate using --SecretIdentifier that was getting the wrong certificate thumbprint</span></span>

#### <a name="azsql"></a><span data-ttu-id="b6b44-264">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b6b44-264">Az.Sql</span></span>
* <span data-ttu-id="b6b44-265">Förbättrade prestanda för:</span><span class="sxs-lookup"><span data-stu-id="b6b44-265">Enhance performance of:</span></span>
    - <span data-ttu-id="b6b44-266">”Set-AzSqlDatabaseSensitivityClassification”</span><span class="sxs-lookup"><span data-stu-id="b6b44-266">'Set-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="b6b44-267">”Set-AzSqlInstanceDatabaseSensitivityClassification”</span><span class="sxs-lookup"><span data-stu-id="b6b44-267">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="b6b44-268">”Remove-AzSqlDatabaseSensitivityClassification”</span><span class="sxs-lookup"><span data-stu-id="b6b44-268">'Remove-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="b6b44-269">”Remove-AzSqlInstanceDatabaseSensitivityClassification”</span><span class="sxs-lookup"><span data-stu-id="b6b44-269">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="b6b44-270">”Enable-AzSqlDatabaseSensitivityRecommendation”</span><span class="sxs-lookup"><span data-stu-id="b6b44-270">'Enable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="b6b44-271">”Enable-AzSqlInstanceDatabaseSensitivityRecommendation”</span><span class="sxs-lookup"><span data-stu-id="b6b44-271">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="b6b44-272">”Disable-AzSqlDatabaseSensitivityRecommendation”</span><span class="sxs-lookup"><span data-stu-id="b6b44-272">'Disable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="b6b44-273">”Disable-AzSqlInstanceDatabaseSensitivityRecommendation”</span><span class="sxs-lookup"><span data-stu-id="b6b44-273">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
* <span data-ttu-id="b6b44-274">Validering på klientsidan har tagits bort för parametern ”RetentionDays” från cmdleten ”Set-AzSqlDatabaseBackupShortTermRetentionPolicy”</span><span class="sxs-lookup"><span data-stu-id="b6b44-274">Removed client-side validation of 'RetentionDays' parameter from cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span>
* <span data-ttu-id="b6b44-275">Granskning av ett lagringskonto i Vnet; en bugg har åtgärdats som orsakade fel när en Storage Blob Data-deltagarroll skapades.</span><span class="sxs-lookup"><span data-stu-id="b6b44-275">Auditing to a storage account in Vnet, fixing a bug when creating a Storage Blob Data Contributor role.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b6b44-276">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b6b44-276">Az.Storage</span></span>
* <span data-ttu-id="b6b44-277">”-AsJob” har lagts till för att hämta/lista konto med cmdleten ”Get-AzStorageAccount”</span><span class="sxs-lookup"><span data-stu-id="b6b44-277">Added '-AsJob' to get/list account cmdlet 'Get-AzStorageAccount'</span></span>
* <span data-ttu-id="b6b44-278">Gör KeyVersion valfri när lagringskontot uppdateras med KeyvaultEncryption, för att ge stöd för automatisk nyckelrotation</span><span class="sxs-lookup"><span data-stu-id="b6b44-278">Make KeyVersion to optional when update Storage account with KeyvaultEncryption, to support key auto-rotation</span></span>
    - <span data-ttu-id="b6b44-279">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="b6b44-279">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="b6b44-280">Problemet med borttagning av Azure-filkatalog i pipeline har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="b6b44-280">Fixed remove Azure File Directory fail with pipeline</span></span>
    - <span data-ttu-id="b6b44-281">”Remove-AzStorageDirectory”</span><span class="sxs-lookup"><span data-stu-id="b6b44-281">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="b6b44-282">Åtgärdat [#9880]: Definitionen av DefaultAction-värdet för NetWorkRule har ändrats för konsekvens med Swagger.</span><span class="sxs-lookup"><span data-stu-id="b6b44-282">Fixed [#9880]: Change NetWorkRule DefaultAction value defination to align with swagger.</span></span>
    - <span data-ttu-id="b6b44-283">”Update-AzStorageAccountNetworkRuleSet”</span><span class="sxs-lookup"><span data-stu-id="b6b44-283">'Update-AzStorageAccountNetworkRuleSet'</span></span>
    - <span data-ttu-id="b6b44-284">”Get-AzStorageAccountNetworkRuleSet”</span><span class="sxs-lookup"><span data-stu-id="b6b44-284">'Get-AzStorageAccountNetworkRuleSet'</span></span>
* <span data-ttu-id="b6b44-285">Åtgärdat [#11624]: Hoppa över dubblettregler när NetworkRules läggs till, för att undvika serverfel</span><span class="sxs-lookup"><span data-stu-id="b6b44-285">Fixed [#11624]: Skip duplicated rules when add NetworkRules, to avoid server failure</span></span>
    - <span data-ttu-id="b6b44-286">”Add-AzStorageAccountNetworkRule”</span><span class="sxs-lookup"><span data-stu-id="b6b44-286">'Add-AzStorageAccountNetworkRule'</span></span>
* <span data-ttu-id="b6b44-287">Microsoft.Azure.Cosmos.Table SDK har uppgraderats till 1.0.7</span><span class="sxs-lookup"><span data-stu-id="b6b44-287">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.7</span></span>
* <span data-ttu-id="b6b44-288">Ett varningsmeddelande har lagts till för att påminna användaren om att lista igen med ContinuationToken när endast delobjekt returneras i listan med DataLake Gen2-objekt,</span><span class="sxs-lookup"><span data-stu-id="b6b44-288">Added a warning message to remind user to list again with ContinuationToken when only part items are returned in list DataLake Gen2 Items,</span></span>
    - <span data-ttu-id="b6b44-289">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="b6b44-289">'Get-AzDataLakeGen2ChildItem'</span></span>
* <span data-ttu-id="b6b44-290">Stöd för att skapa eller uppdatera lagringskonto med Azure Files Active Directory Domain Service-autentisering</span><span class="sxs-lookup"><span data-stu-id="b6b44-290">Supported to create or update Storage account with Azure Files Active Directory Domain Service Authentication</span></span>
    -  <span data-ttu-id="b6b44-291">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="b6b44-291">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="b6b44-292">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="b6b44-292">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="b6b44-293">Stöd för nya eller listade Kerberos-nycklar för lagringskontot</span><span class="sxs-lookup"><span data-stu-id="b6b44-293">Supported to new or list Kerberos keys of Storage account</span></span>
    -  <span data-ttu-id="b6b44-294">”New-AzStorageAccountKey”</span><span class="sxs-lookup"><span data-stu-id="b6b44-294">'New-AzStorageAccountKey'</span></span>
    -  <span data-ttu-id="b6b44-295">”Get-AzStorageAccountKey”</span><span class="sxs-lookup"><span data-stu-id="b6b44-295">'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="b6b44-296">Stöd för redundans med lagringskonto</span><span class="sxs-lookup"><span data-stu-id="b6b44-296">Supported failover Storage account</span></span>
    - <span data-ttu-id="b6b44-297">”Invoke-AzStorageAccountFailover”</span><span class="sxs-lookup"><span data-stu-id="b6b44-297">'Invoke-AzStorageAccountFailover'</span></span>
* <span data-ttu-id="b6b44-298">Hjälpen för ”Get-AzStorageBlobCopyState” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="b6b44-298">Updated help of 'Get-AzStorageBlobCopyState'</span></span>
* <span data-ttu-id="b6b44-299">Hjälpen för ”Get-AzStorageFileCopyState” och ”Start-AzStorageBlobCopy” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="b6b44-299">Updated help of 'Get-AzStorageFileCopyState' and 'Start-AzStorageBlobCopy'</span></span>
* <span data-ttu-id="b6b44-300">Lagringsklientbibliotek v12 har integrerats med Queue- och File-cmdletar</span><span class="sxs-lookup"><span data-stu-id="b6b44-300">Integrated Storage client library v12 to Queue and File cmdlets</span></span>
* <span data-ttu-id="b6b44-301">Utdatatypen har ändrats från CloudFile till AzureStorageFile; ursprungliga utdata blir en underordnad egenskap i den nya utmatningen</span><span class="sxs-lookup"><span data-stu-id="b6b44-301">Changed output type from CloudFile to AzureStorageFile, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="b6b44-302">”Get-AzStorageFile”</span><span class="sxs-lookup"><span data-stu-id="b6b44-302">'Get-AzStorageFile'</span></span>
    - <span data-ttu-id="b6b44-303">”Remove-AzStorageFile”</span><span class="sxs-lookup"><span data-stu-id="b6b44-303">'Remove-AzStorageFile'</span></span>
    - <span data-ttu-id="b6b44-304">”Get-AzStorageFileContent”</span><span class="sxs-lookup"><span data-stu-id="b6b44-304">'Get-AzStorageFileContent'</span></span>
    - <span data-ttu-id="b6b44-305">”Set-AzStorageFileContent”</span><span class="sxs-lookup"><span data-stu-id="b6b44-305">'Set-AzStorageFileContent'</span></span>
    - <span data-ttu-id="b6b44-306">”Start-AzStorageFileCopy”</span><span class="sxs-lookup"><span data-stu-id="b6b44-306">'Start-AzStorageFileCopy'</span></span>
* <span data-ttu-id="b6b44-307">Utdatatypen har ändrats från CloudFileDirectory till AzureStorageFileDirectory; ursprungliga utdata blir en underordnad egenskap i den nya utmatningen</span><span class="sxs-lookup"><span data-stu-id="b6b44-307">Changed output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="b6b44-308">”New-AzStorageDirectory”</span><span class="sxs-lookup"><span data-stu-id="b6b44-308">'New-AzStorageDirectory'</span></span>
    - <span data-ttu-id="b6b44-309">”Remove-AzStorageDirectory”</span><span class="sxs-lookup"><span data-stu-id="b6b44-309">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="b6b44-310">Utdatatypen har ändrats från CloudFileShare till AzureStorageFileShare; ursprungliga utdata blir en underordnad egenskap i den nya utmatningen</span><span class="sxs-lookup"><span data-stu-id="b6b44-310">Changed output type from CloudFileShare to AzureStorageFileShare, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="b6b44-311">”Get-AzStorageShare”</span><span class="sxs-lookup"><span data-stu-id="b6b44-311">'Get-AzStorageShare'</span></span>
    - <span data-ttu-id="b6b44-312">”New-AzStorageShare”</span><span class="sxs-lookup"><span data-stu-id="b6b44-312">'New-AzStorageShare'</span></span>
    - <span data-ttu-id="b6b44-313">”Remove-AzStorageShare”</span><span class="sxs-lookup"><span data-stu-id="b6b44-313">'Remove-AzStorageShare'</span></span>
* <span data-ttu-id="b6b44-314">Utdatatypen har ändrats från FileShareProperties till AzureStorageFileShare; ursprungliga utdata blir en underordnad egenskap i den nya utmatningen</span><span class="sxs-lookup"><span data-stu-id="b6b44-314">Changed output type from FileShareProperties to AzureStorageFileShare, the original output will become a sub child property of the new output</span></span>
    - <span data-ttu-id="b6b44-315">”Set-AzStorageShareQuota”</span><span class="sxs-lookup"><span data-stu-id="b6b44-315">'Set-AzStorageShareQuota'</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="b6b44-316">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="b6b44-316">Az.TrafficManager</span></span>
* <span data-ttu-id="b6b44-317">Felaktigt profilnamn har åtgärdats i utförliga utdata för ”DisableAzureTrafficManagerEndpoint”</span><span class="sxs-lookup"><span data-stu-id="b6b44-317">Fixed incorrect profile name in 'DisableAzureTrafficManagerEndpoint' verbose output</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b6b44-318">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b6b44-318">Az.Websites</span></span>
* <span data-ttu-id="b6b44-319">Stavfel har åtgärdats i hjälpen för ”Update-AzWebAppAccessRestrictionConfig”.</span><span class="sxs-lookup"><span data-stu-id="b6b44-319">Fixed typo on help of 'Update-AzWebAppAccessRestrictionConfig'.</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="b6b44-320">3.8.0 – April 2020</span><span class="sxs-lookup"><span data-stu-id="b6b44-320">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="b6b44-321">Höjdpunkter sedan den senaste uppdateringen</span><span class="sxs-lookup"><span data-stu-id="b6b44-321">Highlights since the last release</span></span>
* <span data-ttu-id="b6b44-322">PowerShell-versioner som Az.Storage stöder: Windows PowerShell 5.1, PowerShell Core 6.2.4+ och PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="b6b44-322">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="b6b44-323">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b6b44-323">Az.Accounts</span></span>
* <span data-ttu-id="b6b44-324">Uppdaterade URL:en för Azure PowerShell-enkäten i ”Resolve-AzError” [#11507]</span><span class="sxs-lookup"><span data-stu-id="b6b44-324">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="b6b44-325">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b6b44-325">Az.ApiManagement</span></span>
* <span data-ttu-id="b6b44-326">Lade till meddelande om icke-bakåtkompatibel ändring vid ändring i utdata för Azure File-cmdletar i en framtida version</span><span class="sxs-lookup"><span data-stu-id="b6b44-326">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="b6b44-327">"Set-AzApiManagementGroup" Uppdaterad dokumentation för att ange GroupId-parametern</span><span class="sxs-lookup"><span data-stu-id="b6b44-327">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="b6b44-328">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="b6b44-328">Az.Cdn</span></span>
* <span data-ttu-id="b6b44-329">Fast ChinaCDN-relaterad prissättning för SKU-visning</span><span class="sxs-lookup"><span data-stu-id="b6b44-329">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="b6b44-330">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="b6b44-330">Az.CognitiveServices</span></span>
* <span data-ttu-id="b6b44-331">Identitet som stöds, kryptering, UserOwnedStorage</span><span class="sxs-lookup"><span data-stu-id="b6b44-331">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b6b44-332">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b6b44-332">Az.Compute</span></span>
* <span data-ttu-id="b6b44-333">Cmdleten ”Set-AzVmssOrchestrationServiceState” har lagts till.</span><span class="sxs-lookup"><span data-stu-id="b6b44-333">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="b6b44-334">”Get-AzVmss” med -InstanceView visar OrchestrationService-tillstånd.</span><span class="sxs-lookup"><span data-stu-id="b6b44-334">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="b6b44-335">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="b6b44-335">Az.IotHub</span></span>
* <span data-ttu-id="b6b44-336">Hantera den dubbla konfigurationen för IoT-enheter, nya cmdletar är:</span><span class="sxs-lookup"><span data-stu-id="b6b44-336">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="b6b44-337">'Get-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="b6b44-337">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="b6b44-338">'Update-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="b6b44-338">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="b6b44-339">En cmdlet har lagts till för att anropa direkt metod på en enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="b6b44-339">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="b6b44-340">Hantera dubbel konfiguration för IoT-enhetsmodul, nya cmdletar är:</span><span class="sxs-lookup"><span data-stu-id="b6b44-340">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="b6b44-341">'Get-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="b6b44-341">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="b6b44-342">'Update-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="b6b44-342">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="b6b44-343">Hantera IoT-automatisk konfiguration av enhetshantering i stor skala.</span><span class="sxs-lookup"><span data-stu-id="b6b44-343">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="b6b44-344">Nya cmdlet:ar är:</span><span class="sxs-lookup"><span data-stu-id="b6b44-344">New cmdlets are:</span></span>
    - <span data-ttu-id="b6b44-345">'Add-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="b6b44-345">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="b6b44-346">'Get-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="b6b44-346">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="b6b44-347">'Remove-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="b6b44-347">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="b6b44-348">'Set-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="b6b44-348">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="b6b44-349">En cmdlet har lagts till för att anropa en edge-modulmetod i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="b6b44-349">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="b6b44-350">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b6b44-350">Az.KeyVault</span></span>
* <span data-ttu-id="b6b44-351">Har lagt till en ny cmdlet, "Update-AzKeyVault", som kan aktivera mjuk borttagning och rensning av skydd i ett valv</span><span class="sxs-lookup"><span data-stu-id="b6b44-351">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="b6b44-352">Har lagt till stöd i Microsoft.PowerShell.SecretManagement [#11178]</span><span class="sxs-lookup"><span data-stu-id="b6b44-352">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="b6b44-353">Åtgärdat fel i exemplen i 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span><span class="sxs-lookup"><span data-stu-id="b6b44-353">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="b6b44-354">Har lagt till stöd för privat slutpunkt</span><span class="sxs-lookup"><span data-stu-id="b6b44-354">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="b6b44-355">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="b6b44-355">Az.Maintenance</span></span>
* <span data-ttu-id="b6b44-356">Publicerar slutversion av underhålls-cmdletar för GA</span><span class="sxs-lookup"><span data-stu-id="b6b44-356">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="b6b44-357">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b6b44-357">Az.Monitor</span></span>
* <span data-ttu-id="b6b44-358">Har lagt till cmdletar för privat länkomfång</span><span class="sxs-lookup"><span data-stu-id="b6b44-358">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="b6b44-359">'Get-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="b6b44-359">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="b6b44-360">'Remove-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="b6b44-360">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="b6b44-361">'New-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="b6b44-361">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="b6b44-362">'Update-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="b6b44-362">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="b6b44-363">'Get-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="b6b44-363">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="b6b44-364">'New-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="b6b44-364">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="b6b44-365">'Remove-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="b6b44-365">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b6b44-366">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b6b44-366">Az.Network</span></span>
* <span data-ttu-id="b6b44-367">Uppdaterade cmdletar för att aktivera anslutning på privat IP för Virtual Network Gateway.</span><span class="sxs-lookup"><span data-stu-id="b6b44-367">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="b6b44-368">'New-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="b6b44-368">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="b6b44-369">'Set-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="b6b44-369">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="b6b44-370">'New-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="b6b44-370">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="b6b44-371">'Set-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="b6b44-371">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="b6b44-372">Uppdaterade cmdletar för att aktivera FQDN-baserade LocalNetworkGateways och VpnSites</span><span class="sxs-lookup"><span data-stu-id="b6b44-372">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="b6b44-373">'New-AzLocalNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="b6b44-373">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="b6b44-374">'New-AzVpnSiteLink'</span><span class="sxs-lookup"><span data-stu-id="b6b44-374">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="b6b44-375">Stöd har lagts till för IPv6-adresstypen i ExpressRouteCircuitConnectionConfig (Global Reach)</span><span class="sxs-lookup"><span data-stu-id="b6b44-375">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="b6b44-376">Lade till 'Set-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="b6b44-376">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="b6b44-377">tillåter inställning av alla befintliga egenskaper inklusive IPv6CircuitConnectionProperties</span><span class="sxs-lookup"><span data-stu-id="b6b44-377">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="b6b44-378">Uppdaterade 'Add-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="b6b44-378">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="b6b44-379">Lade till en ytterligare valfri parameter, AddressPrefixType, för att specificera adresstypen för adressprefix</span><span class="sxs-lookup"><span data-stu-id="b6b44-379">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="b6b44-380">Uppdaterade cmdletar för att aktivera inställningen för DPD-timeout på Virtual Network Gateway-anslutningar.</span><span class="sxs-lookup"><span data-stu-id="b6b44-380">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="b6b44-381">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="b6b44-381">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="b6b44-382">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="b6b44-382">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="b6b44-383">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="b6b44-383">Az.PolicyInsights</span></span>
* <span data-ttu-id="b6b44-384">Cmdleten "Start-AzPolicyComplianceScan" har lagts till för att utlösa genomsökningar av principefterlevnad</span><span class="sxs-lookup"><span data-stu-id="b6b44-384">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="b6b44-385">Principdefinition, uppsättningsdefinition och tilldelningsversioner har lagts till i "Get-AzPolicyState"-utdata</span><span class="sxs-lookup"><span data-stu-id="b6b44-385">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="b6b44-386">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b6b44-386">Az.ServiceFabric</span></span>
* <span data-ttu-id="b6b44-387">Förbättrad kodformatering och användbarhet för "New-AzServiceFabricCluster"-exempel</span><span class="sxs-lookup"><span data-stu-id="b6b44-387">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="b6b44-388">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b6b44-388">Az.Sql</span></span>
* <span data-ttu-id="b6b44-389">Lade till cmdletarna "Get-AzSqlInstanceOperation" och "Stop-AzSqlInstanceOperation"</span><span class="sxs-lookup"><span data-stu-id="b6b44-389">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="b6b44-390">Stöd för granskning för ett lagringskonto i VNet.</span><span class="sxs-lookup"><span data-stu-id="b6b44-390">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b6b44-391">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b6b44-391">Az.Storage</span></span>
* <span data-ttu-id="b6b44-392">Lade till meddelande om icke-bakåtkompatibel ändring vid ändring i utdata för Azure File-cmdletar i en framtida version</span><span class="sxs-lookup"><span data-stu-id="b6b44-392">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="b6b44-393">Stöd för nya SkuName StandardGZRS, StandardRAGZRS när ett lagringskonto skapas/uppdateras</span><span class="sxs-lookup"><span data-stu-id="b6b44-393">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="b6b44-394">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="b6b44-394">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="b6b44-395">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="b6b44-395">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="b6b44-396">Stöd för DataLake Gen2</span><span class="sxs-lookup"><span data-stu-id="b6b44-396">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="b6b44-397">'New-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="b6b44-397">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="b6b44-398">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="b6b44-398">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="b6b44-399">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="b6b44-399">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="b6b44-400">'Move-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="b6b44-400">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="b6b44-401">'Set-AzDataLakeGen2ItemAclObject'</span><span class="sxs-lookup"><span data-stu-id="b6b44-401">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="b6b44-402">'Update-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="b6b44-402">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="b6b44-403">'Get-AzDataLakeGen2ItemContent'</span><span class="sxs-lookup"><span data-stu-id="b6b44-403">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="b6b44-404">'Remove-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="b6b44-404">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="b6b44-405">0.10.0-förhandsversion – April 2020</span><span class="sxs-lookup"><span data-stu-id="b6b44-405">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="b6b44-406">Allmänt</span><span class="sxs-lookup"><span data-stu-id="b6b44-406">General</span></span>
* <span data-ttu-id="b6b44-407">Az-moduler är nu tillgängliga i förhandsversion på Azure Stack Hub.</span><span class="sxs-lookup"><span data-stu-id="b6b44-407">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="b6b44-408">Därmed möjliggörs kompatibilitet för flera plattformar med Linux och macOs.</span><span class="sxs-lookup"><span data-stu-id="b6b44-408">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="b6b44-409">Azure Stack Hub stöder nu PowerShell Core med AZ-moduler. Mer information finns [här](https://aka.ms/az4AzureStack)</span><span class="sxs-lookup"><span data-stu-id="b6b44-409">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](https://aka.ms/az4AzureStack)</span></span>
* <span data-ttu-id="b6b44-410">Supportprofil för AZ-moduler 2019-03-01-hybrid:</span><span class="sxs-lookup"><span data-stu-id="b6b44-410">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="b6b44-411">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="b6b44-411">Az.Billing</span></span>
  - <span data-ttu-id="b6b44-412">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b6b44-412">Az.Compute</span></span>
  - <span data-ttu-id="b6b44-413">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="b6b44-413">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="b6b44-414">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="b6b44-414">Az.EventHub</span></span>
  - <span data-ttu-id="b6b44-415">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="b6b44-415">Az.IotHub</span></span>
  - <span data-ttu-id="b6b44-416">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b6b44-416">Az.KeyVault</span></span>
  - <span data-ttu-id="b6b44-417">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b6b44-417">Az.Monitor</span></span>
  - <span data-ttu-id="b6b44-418">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b6b44-418">Az.Network</span></span>
  - <span data-ttu-id="b6b44-419">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b6b44-419">Az.Resources</span></span>
  - <span data-ttu-id="b6b44-420">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b6b44-420">Az.Storage</span></span>
  - <span data-ttu-id="b6b44-421">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b6b44-421">Az.Websites</span></span>
* <span data-ttu-id="b6b44-422">Tre nya PowerShell-moduler för AZ har introducerats som fungerar med Azure Stack Hub, och de är Az.Databox, Az.IotHub och Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="b6b44-422">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="b6b44-423">Kommandona är i princip oförändrade, med endast mindre ändringar som att AzureRM ändras till AZ</span><span class="sxs-lookup"><span data-stu-id="b6b44-423">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="b6b44-424">En uppdaterad länk till PowerShell-dokumentationen för Azure Stack Hub finns [här](https://aka.ms/InstallASHPowerShell)</span><span class="sxs-lookup"><span data-stu-id="b6b44-424">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](https://aka.ms/InstallASHPowerShell)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="b6b44-425">3.7.0 – mars 2020</span><span class="sxs-lookup"><span data-stu-id="b6b44-425">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b6b44-426">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b6b44-426">Az.Accounts</span></span>
* <span data-ttu-id="b6b44-427">Åtgärdade ”Get-AzTenant”/”Get-AzDefault”/”Set-AzDefault”-utlösning av NullReferenceException när du inte är inloggad [#10292]</span><span class="sxs-lookup"><span data-stu-id="b6b44-427">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b6b44-428">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b6b44-428">Az.Compute</span></span>
* <span data-ttu-id="b6b44-429">Följande parametrar har lagts till i cmdleten ”New-AzDiskConfig”:</span><span class="sxs-lookup"><span data-stu-id="b6b44-429">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="b6b44-430">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="b6b44-430">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="b6b44-431">Tillåten krypteringsegenskap till målparametern för cmdleten ”New-AzGalleryImageVersion”.</span><span class="sxs-lookup"><span data-stu-id="b6b44-431">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="b6b44-432">Åtgärdade tempDisk-problem för cmdletarna ”Set-AzVmss”-Reimage och ”Invoke-AzVMReimage”.</span><span class="sxs-lookup"><span data-stu-id="b6b44-432">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="b6b44-433">[#11354]</span><span class="sxs-lookup"><span data-stu-id="b6b44-433">[#11354]</span></span>
* <span data-ttu-id="b6b44-434">Stöd har lagts till i nedanstående cmdletar för nytt SAP-tillägg</span><span class="sxs-lookup"><span data-stu-id="b6b44-434">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="b6b44-435">”Set-AzVMAEMExtension”</span><span class="sxs-lookup"><span data-stu-id="b6b44-435">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="b6b44-436">”Get-AzVMAEMExtension”</span><span class="sxs-lookup"><span data-stu-id="b6b44-436">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="b6b44-437">”Remove-AzVMAEMExtension”</span><span class="sxs-lookup"><span data-stu-id="b6b44-437">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="b6b44-438">”Update-AzVMAEMExtension”</span><span class="sxs-lookup"><span data-stu-id="b6b44-438">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="b6b44-439">Åtgärdade fel i exempel på hjälpdokument</span><span class="sxs-lookup"><span data-stu-id="b6b44-439">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="b6b44-440">Visade det exakta strängvärdet för VM PowerState i tabellformat.</span><span class="sxs-lookup"><span data-stu-id="b6b44-440">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="b6b44-441">”New-AzVmssConfig”: den fasta serialiseringen av egenskapen AutomaticRepairs när SinglePlacementGroup är inaktiverad.</span><span class="sxs-lookup"><span data-stu-id="b6b44-441">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="b6b44-442">[#11257]</span><span class="sxs-lookup"><span data-stu-id="b6b44-442">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b6b44-443">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b6b44-443">Az.DataFactory</span></span>
* <span data-ttu-id="b6b44-444">ADF .Net SDK har uppdaterats till 4.8.0</span><span class="sxs-lookup"><span data-stu-id="b6b44-444">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="b6b44-445">Valfria parametrar har lagts till i kommandot ”Invoke-AzDataFactoryV2Pipeline” för att stödja omkörning</span><span class="sxs-lookup"><span data-stu-id="b6b44-445">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b6b44-446">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b6b44-446">Az.DataLakeStore</span></span>
* <span data-ttu-id="b6b44-447">Lade till beskrivning för icke-bakåtkompatibel ändring för ”Export-AzDataLakeStoreItem” och ”Import-AzDataLakeStoreItem”</span><span class="sxs-lookup"><span data-stu-id="b6b44-447">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="b6b44-448">Lade till alternativ för bytekodning för ”New-AzDataLakeStoreItem”, ”Add-AzDAtaLakeStoreItemContent” och ”Get-AzDAtaLakeStoreItemContent”</span><span class="sxs-lookup"><span data-stu-id="b6b44-448">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="b6b44-449">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="b6b44-449">Az.HDInsight</span></span>
* <span data-ttu-id="b6b44-450">Stöd för att ange en minimal TLS-version som stöds när klustret skapas.</span><span class="sxs-lookup"><span data-stu-id="b6b44-450">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="b6b44-451">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="b6b44-451">Az.IotHub</span></span>
* <span data-ttu-id="b6b44-452">Stöd har lagts till för att hantera distribuerade inställningar per enhet.</span><span class="sxs-lookup"><span data-stu-id="b6b44-452">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="b6b44-453">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="b6b44-453">New Cmdlets are:</span></span>
    - <span data-ttu-id="b6b44-454">”Get-AzIotHubDistributedTracing”</span><span class="sxs-lookup"><span data-stu-id="b6b44-454">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="b6b44-455">”Set-AzIotHubDistributedTracing”</span><span class="sxs-lookup"><span data-stu-id="b6b44-455">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="b6b44-456">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b6b44-456">Az.KeyVault</span></span>
* <span data-ttu-id="b6b44-457">Ändrade attribut för icke-bakåtkompatibel ändring lades till för ”New-AzKeyVault”</span><span class="sxs-lookup"><span data-stu-id="b6b44-457">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="b6b44-458">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b6b44-458">Az.Monitor</span></span>
* <span data-ttu-id="b6b44-459">Uppdaterad dokumentation för ”New-AzScheduledQueryRuleLogMetricTrigger”</span><span class="sxs-lookup"><span data-stu-id="b6b44-459">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b6b44-460">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b6b44-460">Az.Network</span></span>
* <span data-ttu-id="b6b44-461">Uppdaterade cmdletar för att tillåta VirtualHubVnetConnections mellan klienter</span><span class="sxs-lookup"><span data-stu-id="b6b44-461">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="b6b44-462">”New-AzVirtualHubVnetConnection”</span><span class="sxs-lookup"><span data-stu-id="b6b44-462">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="b6b44-463">”Update-AzVirtualHubVnetConnection”</span><span class="sxs-lookup"><span data-stu-id="b6b44-463">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="b6b44-464">”New-AzVirtualHub”</span><span class="sxs-lookup"><span data-stu-id="b6b44-464">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="b6b44-465">”Update-AzVirtualHub”</span><span class="sxs-lookup"><span data-stu-id="b6b44-465">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="b6b44-466">SQL Management SDK-beroende har tagits bort</span><span class="sxs-lookup"><span data-stu-id="b6b44-466">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="b6b44-467">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="b6b44-467">Az.PolicyInsights</span></span>
* <span data-ttu-id="b6b44-468">Förbättrade felmeddelanden</span><span class="sxs-lookup"><span data-stu-id="b6b44-468">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b6b44-469">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b6b44-469">Az.RecoveryServices</span></span>
* <span data-ttu-id="b6b44-470">Azure Site Recovery har lagt till stöd för återaktivering av skydd och uppdaterade VM-egenskaper för virtuella Azure-datorer med krypterad disk.</span><span class="sxs-lookup"><span data-stu-id="b6b44-470">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="b6b44-471">Lade till Azure Site Recovery VmwareToAzure-egenskaper för DR-övervakning</span><span class="sxs-lookup"><span data-stu-id="b6b44-471">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="b6b44-472">Azure Backup har lagt till stöd för att försöka uppdatera principuppdateringen för misslyckade objekt på nytt.</span><span class="sxs-lookup"><span data-stu-id="b6b44-472">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="b6b44-473">Azure Backup lagt till stöd för diskundantagsinställningar under säkerhetskopiering och återställning.</span><span class="sxs-lookup"><span data-stu-id="b6b44-473">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="b6b44-474">Azure Backup lagt till stöd för att återställa flera filer/mappar i AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="b6b44-474">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="b6b44-475">Azure Backup lade till support för användardefinierad Resourcegroup-support vid uppdatering av IaasVM-princip</span><span class="sxs-lookup"><span data-stu-id="b6b44-475">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="b6b44-476">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b6b44-476">Az.Resources</span></span>
* <span data-ttu-id="b6b44-477">Åtgärdade ”Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType” så att den använder den faktisk apiVersion av resurser i stället för standard-apiVersion [#11267]</span><span class="sxs-lookup"><span data-stu-id="b6b44-477">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="b6b44-478">Lade till correlationId-loggning för felscenarier</span><span class="sxs-lookup"><span data-stu-id="b6b44-478">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="b6b44-479">Liten dokumentationsändring för ”Get-AzResourceLock”.</span><span class="sxs-lookup"><span data-stu-id="b6b44-479">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="b6b44-480">Lade till exempel.</span><span class="sxs-lookup"><span data-stu-id="b6b44-480">Added example.</span></span>
* <span data-ttu-id="b6b44-481">Undantaget enkelt citattecken i parametervärde för ”Get-AzADUser” [#11317]</span><span class="sxs-lookup"><span data-stu-id="b6b44-481">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="b6b44-482">Nya cmdletar har lagts till för distributionsskript (”Get-AzDeploymentScript”, ”Get-AzDeploymentScriptLog”, ”Save-AzDeploymentScriptLog”, ”Remove-AzDeploymentScript”)</span><span class="sxs-lookup"><span data-stu-id="b6b44-482">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="b6b44-483">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b6b44-483">Az.Sql</span></span>
* <span data-ttu-id="b6b44-484">En läsbar sekundär parameter har lagts till i Invoke-AzSqlDatabaseFailover</span><span class="sxs-lookup"><span data-stu-id="b6b44-484">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="b6b44-485">Cmdleten Disable-AzSqlServerActiveDirectoryOnlyAuthentication har lagts till</span><span class="sxs-lookup"><span data-stu-id="b6b44-485">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="b6b44-486">Den sparade känslighet rangordningen när kolumner klassificeras i databasen.</span><span class="sxs-lookup"><span data-stu-id="b6b44-486">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="b6b44-487">Az.Support</span><span class="sxs-lookup"><span data-stu-id="b6b44-487">Az.Support</span></span>
* <span data-ttu-id="b6b44-488">Allmän tillgänglighet för ”Az.Support”-modulen</span><span class="sxs-lookup"><span data-stu-id="b6b44-488">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b6b44-489">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b6b44-489">Az.Websites</span></span>
* <span data-ttu-id="b6b44-490">Stöd har lagts till för att arbeta med trafikdirigeringsregler för webbappar under nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="b6b44-490">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="b6b44-491">”Get-AzWebAppTrafficRouting”</span><span class="sxs-lookup"><span data-stu-id="b6b44-491">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="b6b44-492">”Update-AzWebAppTrafficRouting”</span><span class="sxs-lookup"><span data-stu-id="b6b44-492">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="b6b44-493">”Add-AzWebAppTrafficRouting”</span><span class="sxs-lookup"><span data-stu-id="b6b44-493">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="b6b44-494">”Remove-AzWebAppTrafficRouting”</span><span class="sxs-lookup"><span data-stu-id="b6b44-494">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="b6b44-495">3.6.1 – mars 2020</span><span class="sxs-lookup"><span data-stu-id="b6b44-495">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b6b44-496">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b6b44-496">Az.Accounts</span></span>
* <span data-ttu-id="b6b44-497">Öppna sidan med Azure PowerShell-enkäten i ”Send-Feedback” [#11020]</span><span class="sxs-lookup"><span data-stu-id="b6b44-497">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="b6b44-498">Visa URL:en för Azure PowerShell-enkäten i ”Resolve-Error” [#11021]</span><span class="sxs-lookup"><span data-stu-id="b6b44-498">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="b6b44-499">Az-version har lagts till i UserAgent</span><span class="sxs-lookup"><span data-stu-id="b6b44-499">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="b6b44-500">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b6b44-500">Az.ApiManagement</span></span>
* <span data-ttu-id="b6b44-501">Stöd har lagts till för att hämta och konfigurera en anpassad domän på DeveloperPortal-slutpunkten [#11007]</span><span class="sxs-lookup"><span data-stu-id="b6b44-501">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="b6b44-502">”Export-AzApiManagementApi” Stöd har lagts till för att ladda ned API-definition i Json-format [#9987]</span><span class="sxs-lookup"><span data-stu-id="b6b44-502">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="b6b44-503">”Import-AzApiManagementApi” Stöd har lagts till för att importera OpenApi 3.0-definition från Json-dokument</span><span class="sxs-lookup"><span data-stu-id="b6b44-503">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="b6b44-504">”New-AzApiManagementIdentityProvider” och ”Set-AzApiManagementIdentityProvider” Stöd har lagts till för att konfigurera ”Signin Tenant” för AAD B2C-provider [#9784]</span><span class="sxs-lookup"><span data-stu-id="b6b44-504">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b6b44-505">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b6b44-505">Az.DataLakeStore</span></span>
* <span data-ttu-id="b6b44-506">En referens har uttryckligen lagts till för System.Buffers i csproj och psd1.</span><span class="sxs-lookup"><span data-stu-id="b6b44-506">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="b6b44-507">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="b6b44-507">Az.IotHub</span></span>
* <span data-ttu-id="b6b44-508">Lade till stöd för att hantera enheter i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="b6b44-508">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="b6b44-509">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="b6b44-509">New Cmdlets are:</span></span>
    - <span data-ttu-id="b6b44-510">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="b6b44-510">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="b6b44-511">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="b6b44-511">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="b6b44-512">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="b6b44-512">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="b6b44-513">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="b6b44-513">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="b6b44-514">Stöd har lagts till för att hantera moduler på en mål-IoT-enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="b6b44-514">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="b6b44-515">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="b6b44-515">New Cmdlets are:</span></span>
    - <span data-ttu-id="b6b44-516">”Add-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="b6b44-516">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="b6b44-517">”Get-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="b6b44-517">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="b6b44-518">”Remove-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="b6b44-518">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="b6b44-519">”Set-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="b6b44-519">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="b6b44-520">Cmdlet har lagts till för att hämta anslutningssträngen för en mål-IoT-enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="b6b44-520">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="b6b44-521">Cmdlet har lagts till för att hämta anslutningssträngen för en modul på en mål-IoT-enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="b6b44-521">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="b6b44-522">Stöd har lagts till för att hämta/ange en överordnad enhet för en IoT-enhet.</span><span class="sxs-lookup"><span data-stu-id="b6b44-522">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="b6b44-523">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="b6b44-523">New Cmdlets are:</span></span>
    - <span data-ttu-id="b6b44-524">”Get-AzIotHubDeviceParent”</span><span class="sxs-lookup"><span data-stu-id="b6b44-524">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="b6b44-525">”Set-AzIotHubDeviceParent”</span><span class="sxs-lookup"><span data-stu-id="b6b44-525">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="b6b44-526">Stöd har lagts till för att hantera en enhets överordnade och underordnade relationer.</span><span class="sxs-lookup"><span data-stu-id="b6b44-526">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="b6b44-527">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b6b44-527">Az.Monitor</span></span>
* <span data-ttu-id="b6b44-528">Utdatavärdet har åtgärdats för ”Get-AzMetricDefinition” [#9714]</span><span class="sxs-lookup"><span data-stu-id="b6b44-528">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b6b44-529">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b6b44-529">Az.Network</span></span>
* <span data-ttu-id="b6b44-530">SQL Management SDK har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="b6b44-530">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="b6b44-531">Ett problem har åtgärdats med namngivningsskillnader i klassen PrivateLinkServiceConnectionState.</span><span class="sxs-lookup"><span data-stu-id="b6b44-531">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="b6b44-532">Fältet ActionsRequired mappar till ActionRequired.</span><span class="sxs-lookup"><span data-stu-id="b6b44-532">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="b6b44-533">PublicNetworkAccess har lagts till i ”New-AzSqlServer” och ”Set-AzSqlServer”</span><span class="sxs-lookup"><span data-stu-id="b6b44-533">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="b6b44-534">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b6b44-534">Az.Resources</span></span>
* <span data-ttu-id="b6b44-535">Null-referensfel har åtgärdats i ”Get-AzRoleAssignment”</span><span class="sxs-lookup"><span data-stu-id="b6b44-535">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="b6b44-536">Växlarna ”-Force” och ”-PassThru” är valfria i ”Remove-AzADGroup” [#10849]</span><span class="sxs-lookup"><span data-stu-id="b6b44-536">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="b6b44-537">Ett problem har åtgärdats som gjorde att ”MailNickname” inte returnerades i ”Remove-AzADGroup” [#11167]</span><span class="sxs-lookup"><span data-stu-id="b6b44-537">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="b6b44-538">Ett problem har åtgärdats som gjorde att pipe-åtgärden ”Remove-AzADGroup” inte fungerar [#11171]</span><span class="sxs-lookup"><span data-stu-id="b6b44-538">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="b6b44-539">Ett null-referensfel har åtgärdats i GetAzureRoleAssignmentCommand</span><span class="sxs-lookup"><span data-stu-id="b6b44-539">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="b6b44-540">Attribut för icke-bakåtkompatibla ändringar har lagts till för kommande ändringar i cmdlets för principer</span><span class="sxs-lookup"><span data-stu-id="b6b44-540">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="b6b44-541">”Get-AzResourceGroup” har uppdaterats för att utföra taggfiltrering för resursgrupper på serversidan</span><span class="sxs-lookup"><span data-stu-id="b6b44-541">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="b6b44-542">Utökade Tag-cmdlets stöder -ResourceId</span><span class="sxs-lookup"><span data-stu-id="b6b44-542">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="b6b44-543">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="b6b44-543">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="b6b44-544">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="b6b44-544">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="b6b44-545">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="b6b44-545">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="b6b44-546">Ny Tag-cmdlet har lagts till</span><span class="sxs-lookup"><span data-stu-id="b6b44-546">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="b6b44-547">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="b6b44-547">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="b6b44-548">Flyttade ScopedDeployment från SDK 3.3.0</span><span class="sxs-lookup"><span data-stu-id="b6b44-548">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="b6b44-549">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b6b44-549">Az.Sql</span></span>
* <span data-ttu-id="b6b44-550">PublicNetworkAccess har lagts till i ”New-AzSqlServer” och ”Set-AzSqlServer”</span><span class="sxs-lookup"><span data-stu-id="b6b44-550">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="b6b44-551">Stöd har lagts till för konfiguration av säkerhetskopiering för långsiktig kvarhållning för hanterade databaser</span><span class="sxs-lookup"><span data-stu-id="b6b44-551">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="b6b44-552">Hämta/ange LTR-princip på en hanterad databas</span><span class="sxs-lookup"><span data-stu-id="b6b44-552">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="b6b44-553">Hämta LTR-säkerhetskopior efter hanterad databas, hanterad instans eller plats</span><span class="sxs-lookup"><span data-stu-id="b6b44-553">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="b6b44-554">Ta bort en LTR-säkerhetskopia</span><span class="sxs-lookup"><span data-stu-id="b6b44-554">Remove an LTR backup</span></span>
    - <span data-ttu-id="b6b44-555">Återställa en LTR-säkerhetskopia för att skapa en ny hanterad databas</span><span class="sxs-lookup"><span data-stu-id="b6b44-555">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="b6b44-556">MinimalTlsVersion har lagts till för New-AzSqlServer och Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="b6b44-556">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="b6b44-557">MinimalTlsVersion har lagts till för New-AzSqlInstance och Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="b6b44-557">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="b6b44-558">SQL SDK-versionen för Az.Network har ändrats</span><span class="sxs-lookup"><span data-stu-id="b6b44-558">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b6b44-559">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b6b44-559">Az.Storage</span></span>
* <span data-ttu-id="b6b44-560">AllowProtectedAppendWrite stöds i ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="b6b44-560">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="b6b44-561">”Set-AzRmStorageContainerImmutabilityPolicy”</span><span class="sxs-lookup"><span data-stu-id="b6b44-561">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="b6b44-562">Varningsmeddelande har lagts till om icke-bakåtkompatibel ändring för ändring av typen AzureStorageTable i en senare version</span><span class="sxs-lookup"><span data-stu-id="b6b44-562">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="b6b44-563">”New-AzStorageTable”</span><span class="sxs-lookup"><span data-stu-id="b6b44-563">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="b6b44-564">”Get-AzStorageTable”</span><span class="sxs-lookup"><span data-stu-id="b6b44-564">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b6b44-565">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b6b44-565">Az.Websites</span></span>
* <span data-ttu-id="b6b44-566">Tag-parametern har lagts till för ”New-AzAppServicePlan” och ”Set-AzAppServicePlan”</span><span class="sxs-lookup"><span data-stu-id="b6b44-566">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="b6b44-567">Stoppa cmdlet-körning om ett undantag uppstår när en anpassad domän läggs till på en webbplats</span><span class="sxs-lookup"><span data-stu-id="b6b44-567">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="b6b44-568">Stöd har lagts till för att utföra åtgärder för App Services som inte tillhör samma resursgrupp som App Services-planen</span><span class="sxs-lookup"><span data-stu-id="b6b44-568">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="b6b44-569">Åtkomstbegränsning har tillämpats på WebApp/Function i olika resursgrupper</span><span class="sxs-lookup"><span data-stu-id="b6b44-569">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="b6b44-570">Ett problem har åtgärdats för att ange anpassade värdnamn för WebAppSlots</span><span class="sxs-lookup"><span data-stu-id="b6b44-570">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="b6b44-571">3.5.0 – februari 2020</span><span class="sxs-lookup"><span data-stu-id="b6b44-571">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="b6b44-572">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="b6b44-572">Highlights since the last major release</span></span>
* <span data-ttu-id="b6b44-573">Uppdaterade telemetri på klientsidan.</span><span class="sxs-lookup"><span data-stu-id="b6b44-573">Updated client side telemetry.</span></span>
* <span data-ttu-id="b6b44-574">Az.IotHub lade till cmdletar som stöd för att hantera enheter.</span><span class="sxs-lookup"><span data-stu-id="b6b44-574">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="b6b44-575">Az.SqlVirtualMachine lade till cmdletar för lyssningsfunktion för tillgänglighetsgrupp.</span><span class="sxs-lookup"><span data-stu-id="b6b44-575">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="b6b44-576">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b6b44-576">Az.Accounts</span></span>
* <span data-ttu-id="b6b44-577">Lade till SubscriptionId, TenantId och körningstid i data för telemetri på klientsidan</span><span class="sxs-lookup"><span data-stu-id="b6b44-577">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="b6b44-578">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b6b44-578">Az.Automation</span></span>
* <span data-ttu-id="b6b44-579">Åtgärdade skrivfel i exempel 1 i referensdokumentation för ”New-AzAutomationSoftwareUpdateConfiguration”</span><span class="sxs-lookup"><span data-stu-id="b6b44-579">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="b6b44-580">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="b6b44-580">Az.CognitiveServices</span></span>
* <span data-ttu-id="b6b44-581">Uppdaterade SDK till 7.0</span><span class="sxs-lookup"><span data-stu-id="b6b44-581">Updated SDK to 7.0</span></span>
* <span data-ttu-id="b6b44-582">Förbättrade felmeddelande vid serversvar om tom brödtext</span><span class="sxs-lookup"><span data-stu-id="b6b44-582">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b6b44-583">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b6b44-583">Az.Compute</span></span>
* <span data-ttu-id="b6b44-584">Tillät tomt värde för ProximityPlacementGroupId under uppdatering</span><span class="sxs-lookup"><span data-stu-id="b6b44-584">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="b6b44-585">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="b6b44-585">Az.FrontDoor</span></span>
* <span data-ttu-id="b6b44-586">Lade till cmdlet för att hämta hanterade regeldefinitioner som kan användas i WAF</span><span class="sxs-lookup"><span data-stu-id="b6b44-586">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="b6b44-587">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="b6b44-587">Az.IotHub</span></span>
* <span data-ttu-id="b6b44-588">Lade till stöd för att hantera enheter i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="b6b44-588">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="b6b44-589">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="b6b44-589">New Cmdlets are:</span></span>
    - <span data-ttu-id="b6b44-590">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="b6b44-590">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="b6b44-591">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="b6b44-591">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="b6b44-592">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="b6b44-592">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="b6b44-593">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="b6b44-593">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="b6b44-594">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b6b44-594">Az.KeyVault</span></span>
* <span data-ttu-id="b6b44-595">Åtgärdade duplicerad text för Add-AzKeyVaultKey.md</span><span class="sxs-lookup"><span data-stu-id="b6b44-595">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="b6b44-596">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b6b44-596">Az.Monitor</span></span>
* <span data-ttu-id="b6b44-597">Åtgärdade beskrivning av cmdleten Get-AzLog.</span><span class="sxs-lookup"><span data-stu-id="b6b44-597">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="b6b44-598">En ny parameter med namnet ActionGroupId har lagts till i kommandot ”New-AzMetricAlertRuleV2”.</span><span class="sxs-lookup"><span data-stu-id="b6b44-598">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="b6b44-599">Användaren kan ange ActionGroupId(string) eller ActionGroup(ActivityLogAlertActionGroup).</span><span class="sxs-lookup"><span data-stu-id="b6b44-599">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b6b44-600">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b6b44-600">Az.Network</span></span>
* <span data-ttu-id="b6b44-601">Lade till en extra parameteranteckning för parametern ”-EnableProxyProtocol” för cmdleten ”New-AzPrivateLinkService”.</span><span class="sxs-lookup"><span data-stu-id="b6b44-601">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="b6b44-602">Åtgärdade FilterData-exempel i Start-AzVirtualNetworkGatewayConnectionPacketCapture.md och Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="b6b44-602">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="b6b44-603">Lade till paketinsamlingsexempel för att samla in alla inre och yttre paket i Start-AzVirtualNetworkGatewayConnectionPacketCapture.md och Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="b6b44-603">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="b6b44-604">Lade till stöd för Azure-brandväggsprincip på VNet-brandväggar</span><span class="sxs-lookup"><span data-stu-id="b6b44-604">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="b6b44-605">Inga nya cmdletar har lagts till.</span><span class="sxs-lookup"><span data-stu-id="b6b44-605">No new cmdlets are added.</span></span> <span data-ttu-id="b6b44-606">Lättar begränsningen för brandväggsprincip på VNet-brandväggar</span><span class="sxs-lookup"><span data-stu-id="b6b44-606">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b6b44-607">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b6b44-607">Az.RecoveryServices</span></span>
* <span data-ttu-id="b6b44-608">Lade till stöd för Restore-as-files för SQL-databaser.</span><span class="sxs-lookup"><span data-stu-id="b6b44-608">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="b6b44-609">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b6b44-609">Az.Resources</span></span>
* <span data-ttu-id="b6b44-610">Omstrukturerade cmdletar för malldistribution</span><span class="sxs-lookup"><span data-stu-id="b6b44-610">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="b6b44-611">Lade till nya cmdletar för att hantera distributioner i hanteringsgruppen: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b6b44-611">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="b6b44-612">Lade till nya cmdletar för att hantera distributioner i klientorganisationsområdet: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="b6b44-612">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="b6b44-613">Omstrukturerade \*-AzDeployment-cmdletar för att fungera specifikt i prenumerationsomfattningen</span><span class="sxs-lookup"><span data-stu-id="b6b44-613">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="b6b44-614">Skapade alias \*-AzSubscriptionDeployment för \*-AzDeployment-cmdletar</span><span class="sxs-lookup"><span data-stu-id="b6b44-614">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="b6b44-615">Åtgärdade ”Update-AzADApplication” när parametern ”AvailableToOtherTenants” inte har angetts</span><span class="sxs-lookup"><span data-stu-id="b6b44-615">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="b6b44-616">Tog bort ApplicationObjectWithoutCredentialParameterSet för att undvika AmbiguousParameterSetException.</span><span class="sxs-lookup"><span data-stu-id="b6b44-616">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="b6b44-617">Återskapade hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="b6b44-617">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="b6b44-618">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b6b44-618">Az.Sql</span></span>
* <span data-ttu-id="b6b44-619">Lade till stöd för återställning till tidpunkt mellan prenumerationer på hanterade instanser.</span><span class="sxs-lookup"><span data-stu-id="b6b44-619">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="b6b44-620">Lade till stöd för att ändra befintlig SQL Managed Instance-maskinvarugenerering</span><span class="sxs-lookup"><span data-stu-id="b6b44-620">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="b6b44-621">Åtgärdade ”Update-AzSqlServerVulnerabilityAssessmentSetting”-hjälpexempel: parameter/egenskapsutdata - EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="b6b44-621">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="b6b44-622">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="b6b44-622">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="b6b44-623">Lade till cmdletar för lyssningsfunktion för tillgänglighetsgrupp</span><span class="sxs-lookup"><span data-stu-id="b6b44-623">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="b6b44-624">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="b6b44-624">Az.StorageSync</span></span>
* <span data-ttu-id="b6b44-625">Uppdaterade teckenuppsättningar som stöds i ”Invoke-AzStorageSyncCompatibilityCheck”.</span><span class="sxs-lookup"><span data-stu-id="b6b44-625">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="b6b44-626">3.4.0 – februari 2020</span><span class="sxs-lookup"><span data-stu-id="b6b44-626">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="b6b44-627">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="b6b44-627">Highlights since the last major release</span></span>
* <span data-ttu-id="b6b44-628">Första Az.CosmosDB-versionen 0.1.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="b6b44-628">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="b6b44-629">Stöd för Az.Network ConnectionMonitor V2 har lagts till</span><span class="sxs-lookup"><span data-stu-id="b6b44-629">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="b6b44-630">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b6b44-630">Az.Accounts</span></span>
* <span data-ttu-id="b6b44-631">Inaktivera automatisk sparande av kontext när AzureRmContext.json inte är tillgängligt</span><span class="sxs-lookup"><span data-stu-id="b6b44-631">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="b6b44-632">Uppdatera referensen till Azure Powershell Common till 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="b6b44-632">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="b6b44-633">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b6b44-633">Az.ApiManagement</span></span>
* <span data-ttu-id="b6b44-634">**Get-AzApiManagementApiSchema** Hämtning av Open-Api-schema som är associerat med ett API har åtgärdats   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="b6b44-634">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="b6b44-635">**New-AzApiManagementProduct**\* och **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="b6b44-635">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="b6b44-636">Åtgärda dokumentation för https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="b6b44-636">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="b6b44-637">**Set-AzApiManagementApi** Exempel för att visa hur ServiceUrl uppdateras med hjälp av cmdleten har lagts till</span><span class="sxs-lookup"><span data-stu-id="b6b44-637">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b6b44-638">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b6b44-638">Az.Compute</span></span>
* <span data-ttu-id="b6b44-639">Begränsa antalet VM-status till 100 för att undvika begränsning när Get-AzVM -Status utförs utan VM-namn.</span><span class="sxs-lookup"><span data-stu-id="b6b44-639">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="b6b44-640">Lägg till cmdleten Update-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="b6b44-640">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="b6b44-641">Lägg till parametrarna EncryptionType och DiskEncryptionSetId i följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="b6b44-641">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="b6b44-642">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="b6b44-642">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="b6b44-643">Lägg till parametern ColocationStatus för cmdleten Get-AzProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="b6b44-643">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b6b44-644">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b6b44-644">Az.DataFactory</span></span>
* <span data-ttu-id="b6b44-645">Uppdatera ADF .Net SDK-versionen till 4.7.0</span><span class="sxs-lookup"><span data-stu-id="b6b44-645">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="b6b44-646">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="b6b44-646">Az.DeploymentManager</span></span>
* <span data-ttu-id="b6b44-647">Lägger till LIST-åtgärder för resurser</span><span class="sxs-lookup"><span data-stu-id="b6b44-647">Adds LIST operations for resources</span></span>
* <span data-ttu-id="b6b44-648">Lägger till funktion för att utföra åtgärder för hälsokontrollsteg</span><span class="sxs-lookup"><span data-stu-id="b6b44-648">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="b6b44-649">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="b6b44-649">Az.HDInsight</span></span>
* <span data-ttu-id="b6b44-650">Åtgärda dokumentfel för New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="b6b44-650">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="b6b44-651">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b6b44-651">Az.KeyVault</span></span>
* <span data-ttu-id="b6b44-652">Lägg till Name-alias för attributet VaultName så att Remove-AzureKeyVault stämmer överens med New-AzureKeyVault.</span><span class="sxs-lookup"><span data-stu-id="b6b44-652">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b6b44-653">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b6b44-653">Az.Network</span></span>
* <span data-ttu-id="b6b44-654">Nytt exempel har lagts till i Set-AzNetworkWatcherConfigFlowLog.md för att demonstrera ett inaktiveringsscenario för Trafikanalys.</span><span class="sxs-lookup"><span data-stu-id="b6b44-654">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="b6b44-655">Lägg till stöd för att tilldela konfiguration av hanterings-IP till Azure Firewall – ett dedikerat undernät och en offentlig IP som brandväggen använder för dess hanteringstrafik</span><span class="sxs-lookup"><span data-stu-id="b6b44-655">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="b6b44-656">Cmdleten New-AzFirewall har uppdaterats:</span><span class="sxs-lookup"><span data-stu-id="b6b44-656">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="b6b44-657">Parametern -ManagementPublicIpAddress (inte obligatorisk) som accepterar ett offentligt IP-adressobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="b6b44-657">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="b6b44-658">Metoden SetManagementIpConfiguration har lagts till för brandväggsobjekt – kräver ett undernät och en offentlig IP-adress som indata – undernätets namn måste vara ”AzureFirewallManagementSubnet”</span><span class="sxs-lookup"><span data-stu-id="b6b44-658">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="b6b44-659">Exempel för Get-AzNetworkSecurityGroup har korrigerats så att exempel visas för NSG:er i stället för nätverksgränssnitt.</span><span class="sxs-lookup"><span data-stu-id="b6b44-659">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="b6b44-660">Ett skrivfel har åtgärdats i kommandot New-AzVpnSite som hindrade kompletteraren för resurs-ID från att fylla i en parameter.</span><span class="sxs-lookup"><span data-stu-id="b6b44-660">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="b6b44-661">Stöd för Url-konfiguration i åtgärdsuppsättningen för omskrivningsregler i Application Gateway har lagts till</span><span class="sxs-lookup"><span data-stu-id="b6b44-661">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="b6b44-662">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="b6b44-662">New cmdlets added:</span></span>
        - <span data-ttu-id="b6b44-663">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="b6b44-663">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="b6b44-664">Cmdletar har uppdaterats med den valfria parametern -UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="b6b44-664">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="b6b44-665">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="b6b44-665">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="b6b44-666">Lägg till stöd för resurser för NetworkWatcher ConnectionMonitor version 2</span><span class="sxs-lookup"><span data-stu-id="b6b44-666">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="b6b44-667">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="b6b44-667">Az.PolicyInsights</span></span>
* <span data-ttu-id="b6b44-668">Stöd för utvärdering av efterlevnad innan fastställande av vilken resurs som ska åtgärdas</span><span class="sxs-lookup"><span data-stu-id="b6b44-668">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="b6b44-669">Lägg till parametern ”-ResourceDiscoverMode” för Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="b6b44-669">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="b6b44-670">Lägg till cmdleten Get-AzPolicyMetadata för att hämta resurser för principmetadata</span><span class="sxs-lookup"><span data-stu-id="b6b44-670">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="b6b44-671">Get-AzPolicyState och Get-AzPolicyStateSummary för API-versionen 2019-10-01 har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="b6b44-671">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b6b44-672">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b6b44-672">Az.RecoveryServices</span></span>
* <span data-ttu-id="b6b44-673">Azure Site Recovery-stöd för att ta bort en replikerad disk.</span><span class="sxs-lookup"><span data-stu-id="b6b44-673">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="b6b44-674">Tillagt Azure Backup-stöd för att lägga till taggar när ett Recovery Services-valv skapas.</span><span class="sxs-lookup"><span data-stu-id="b6b44-674">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="b6b44-675">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b6b44-675">Az.Resources</span></span>
* <span data-ttu-id="b6b44-676">Gör -Scope valfritt i cmdletarna \*-AzPolicyAssignment med standardinställning till kontextprenumeration</span><span class="sxs-lookup"><span data-stu-id="b6b44-676">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="b6b44-677">Lägg till exempel på att skapa ADServicePrincipal med lösenord och nyckelautentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="b6b44-677">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="b6b44-678">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b6b44-678">Az.Sql</span></span>
<span data-ttu-id="b6b44-679">Åtgärda cmdleten New-AzSqlDatabaseSecondary så att existensen PartnerDatabaseName kontrolleras i stället för existensen DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="b6b44-679">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b6b44-680">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b6b44-680">Az.Storage</span></span>
* <span data-ttu-id="b6b44-681">Stöd för angivning av krypteringsnyckeltyp för Tabell/kö i Skapa lagringskonto</span><span class="sxs-lookup"><span data-stu-id="b6b44-681">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="b6b44-682">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b6b44-682">New-AzStorageAccount</span></span>
* <span data-ttu-id="b6b44-683">Visa RequestId när StorageException inte har ExtendedErrorInformation</span><span class="sxs-lookup"><span data-stu-id="b6b44-683">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="b6b44-684">Åtgärda exempel 6 för cmdleten Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="b6b44-684">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b6b44-685">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b6b44-685">Az.Websites</span></span>
* <span data-ttu-id="b6b44-686">Set-AzWebapp och Set-AzWebappSlot stöder egenskaperna AlwaysOn, MinTls och FtpsState</span><span class="sxs-lookup"><span data-stu-id="b6b44-686">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="b6b44-687">Åtgärdar problemet där inställning av HttpsOnly samtidigt som AppservicePlan ändrades med det enskilda kommandot Set-AzWebApp återställde HttpsOnly till standardvärdet</span><span class="sxs-lookup"><span data-stu-id="b6b44-687">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="b6b44-688">3.3.0 – januari 2020</span><span class="sxs-lookup"><span data-stu-id="b6b44-688">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b6b44-689">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b6b44-689">Az.Accounts</span></span>
* <span data-ttu-id="b6b44-690">Nu stöder Add-AzEnvironment och Set-AzEnvironment parametrarna AzureAttestationServiceEndpointResourceId och AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="b6b44-690">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="b6b44-691">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="b6b44-691">Az.Cdn</span></span>
* <span data-ttu-id="b6b44-692">Information om felsvar visas i New-AzCdnEndpoint-cmdleten</span><span class="sxs-lookup"><span data-stu-id="b6b44-692">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b6b44-693">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b6b44-693">Az.Compute</span></span>
* <span data-ttu-id="b6b44-694">Set-AzVMCustomScriptExtension-cmdleten har åtgärdats för en virtuell dator med hanterad OD-disk som inte har någon operativsystemprofil.</span><span class="sxs-lookup"><span data-stu-id="b6b44-694">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="b6b44-695">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="b6b44-695">Az.ContainerInstance</span></span>
* <span data-ttu-id="b6b44-696">Parameternamn som används med New-AzContainerGroup-exempel har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="b6b44-696">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="b6b44-697">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="b6b44-697">Az.DataBoxEdge</span></span>
* <span data-ttu-id="b6b44-698">Cmdleten ”Get-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="b6b44-698">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="b6b44-699">Hämta gränslagringscontainern</span><span class="sxs-lookup"><span data-stu-id="b6b44-699">Get the Edge Storage Container</span></span>
* <span data-ttu-id="b6b44-700">Cmdleten ”New-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="b6b44-700">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="b6b44-701">Skapa en ny gränslagringscontainer</span><span class="sxs-lookup"><span data-stu-id="b6b44-701">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="b6b44-702">Cmdleten ”Remove-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="b6b44-702">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="b6b44-703">Ta bort gränslagringscontainern</span><span class="sxs-lookup"><span data-stu-id="b6b44-703">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="b6b44-704">Cmdleten ”Invoke-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="b6b44-704">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="b6b44-705">Anropa åtgärd för att uppdatera data i gränslagringscontainer</span><span class="sxs-lookup"><span data-stu-id="b6b44-705">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="b6b44-706">Cmdleten ”Get-AzDataBoxEdgeStorageAccount” har lagts till</span><span class="sxs-lookup"><span data-stu-id="b6b44-706">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="b6b44-707">Hämta gränslagringskontot</span><span class="sxs-lookup"><span data-stu-id="b6b44-707">Get the Edge Storage Account</span></span>
* <span data-ttu-id="b6b44-708">Cmdleten ”New-AzDataBoxEdgeStorageAccount” har lagts till</span><span class="sxs-lookup"><span data-stu-id="b6b44-708">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="b6b44-709">Skapa ett nytt gränslagringskonto</span><span class="sxs-lookup"><span data-stu-id="b6b44-709">Create new Edge Storage Account</span></span>
* <span data-ttu-id="b6b44-710">Cmdleten ”Remove-AzDataBoxEdgeStorageAccount” har lagts till</span><span class="sxs-lookup"><span data-stu-id="b6b44-710">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="b6b44-711">Ta bort gränslagringskontot</span><span class="sxs-lookup"><span data-stu-id="b6b44-711">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="b6b44-712">Anropa cmdleten ”Invoke-AzDataBoxEdgeShare”</span><span class="sxs-lookup"><span data-stu-id="b6b44-712">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="b6b44-713">Anropa åtgärd för att uppdatera resursdata</span><span class="sxs-lookup"><span data-stu-id="b6b44-713">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="b6b44-714">Cmdleten ”Set-AzDataBoxEdgeStorageAccountCredential” har lagts till</span><span class="sxs-lookup"><span data-stu-id="b6b44-714">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="b6b44-715">Ange autentiseringsuppgifter för az databoxedge-lagringskonto</span><span class="sxs-lookup"><span data-stu-id="b6b44-715">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b6b44-716">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b6b44-716">Az.DataFactory</span></span>
* <span data-ttu-id="b6b44-717">Lägg till AutoUpdateETA-, LatestVersion-, PushedVersion-, TaskQueueId- och VersionStatus-egenskaper för Get-AzDataFactoryV2IntegrationRuntime-cmd</span><span class="sxs-lookup"><span data-stu-id="b6b44-717">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="b6b44-718">Uppdatera ADF .Net SDK-versionen till 4.6.0</span><span class="sxs-lookup"><span data-stu-id="b6b44-718">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="b6b44-719">Lägg till parametern ”PublicIPs” för ”Set-AzureRmDataFactoryV2IntegrationRuntime”-cmd så att Azure-SSIS IR kan skapas med statiska offentliga IP-adresser.</span><span class="sxs-lookup"><span data-stu-id="b6b44-719">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="b6b44-720">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="b6b44-720">Az.DevTestLabs</span></span>
* <span data-ttu-id="b6b44-721">Ta bort den brutna länken i Get-AzDtlAllowedVMSizesPolicy.md</span><span class="sxs-lookup"><span data-stu-id="b6b44-721">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="b6b44-722">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="b6b44-722">Az.EventHub</span></span>
* <span data-ttu-id="b6b44-723">Korrigering av problem 10634: Åtgärda referensen till null-objekt för eventhubnamespace-borttagning</span><span class="sxs-lookup"><span data-stu-id="b6b44-723">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="b6b44-724">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="b6b44-724">Az.HDInsight</span></span>
* <span data-ttu-id="b6b44-725">Åtgärda Invoke-AzHDInsightHiveJob.md-fel.</span><span class="sxs-lookup"><span data-stu-id="b6b44-725">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="b6b44-726">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="b6b44-726">Az.MachineLearning</span></span>
* <span data-ttu-id="b6b44-727">Nedanstående cmdletar har tagits bort eftersom MachineLearningCompute inte längre är tillgängligt</span><span class="sxs-lookup"><span data-stu-id="b6b44-727">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="b6b44-728">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="b6b44-728">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="b6b44-729">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="b6b44-729">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="b6b44-730">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="b6b44-730">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="b6b44-731">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="b6b44-731">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="b6b44-732">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="b6b44-732">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="b6b44-733">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="b6b44-733">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="b6b44-734">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="b6b44-734">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b6b44-735">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b6b44-735">Az.Network</span></span>
* <span data-ttu-id="b6b44-736">Uppgradera beroende av Microsoft.Azure.Management.Sql från 1.36-preview till 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="b6b44-736">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b6b44-737">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b6b44-737">Az.RecoveryServices</span></span>
* <span data-ttu-id="b6b44-738">Ändrat Azure Site Recovery-stöd för krypterade vilande data på virtuella datorer med hanterade diskar med kundhanterade nycklar för Azure till Azure-providern.</span><span class="sxs-lookup"><span data-stu-id="b6b44-738">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="b6b44-739">Azure Site Recovery-stöd för att ange ID för diskkrypteringsuppsättning som valfri inmatning för aktivering av skydd för VMware till Azure.</span><span class="sxs-lookup"><span data-stu-id="b6b44-739">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="b6b44-740">Azure Site Recovery-stöd för att ange ID för diskkrypteringsuppsättning som valfri inmatning på disknivå för aktivering av skydd för VMware till Azure.</span><span class="sxs-lookup"><span data-stu-id="b6b44-740">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="b6b44-741">Azure Site Recovery-stöd för att uppdatera replikeringsskyddade objekt med mappning för diskkrypteringsuppsättning för HyperV till Azure.</span><span class="sxs-lookup"><span data-stu-id="b6b44-741">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="b6b44-742">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b6b44-742">Az.Resources</span></span>
* <span data-ttu-id="b6b44-743">Åtgärda ett fel i hjälpdokument för ”Remove-AzTag”.</span><span class="sxs-lookup"><span data-stu-id="b6b44-743">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="b6b44-744">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b6b44-744">Az.Sql</span></span>
* <span data-ttu-id="b6b44-745">Åtgärda funktioner i cmdletar för att ange baslinjen för sårbarhetsbedömning för arbete med huvuddatabasen för Azure-databasen och begränsa den för systemdatabaser på hanterade instanser.</span><span class="sxs-lookup"><span data-stu-id="b6b44-745">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="b6b44-746">Åtgärda ett fel när en redundansgrupp för en SQL-instans skapas</span><span class="sxs-lookup"><span data-stu-id="b6b44-746">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="b6b44-747">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="b6b44-747">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="b6b44-748">Lägg till DR som en ny giltig licenstyp</span><span class="sxs-lookup"><span data-stu-id="b6b44-748">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b6b44-749">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b6b44-749">Az.Storage</span></span>
* <span data-ttu-id="b6b44-750">Lägg till varningsmeddelande om icke-bakåtkompatibel ändring för DefaultAction-värdeändring i en framtida version</span><span class="sxs-lookup"><span data-stu-id="b6b44-750">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="b6b44-751">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="b6b44-751">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="b6b44-752">Stöd för att hämta lagringskontots senaste synkroniseringstid genom att köra get-AzureRMStorageAccount med parametern -IncludeGeoReplicationStats</span><span class="sxs-lookup"><span data-stu-id="b6b44-752">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="b6b44-753">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b6b44-753">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="b6b44-754">3.2.0 – December 2019</span><span class="sxs-lookup"><span data-stu-id="b6b44-754">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="b6b44-755">Allmänt</span><span class="sxs-lookup"><span data-stu-id="b6b44-755">General</span></span>
* <span data-ttu-id="b6b44-756">Uppdatera referenser i .psd1 för att använda relativa sökvägar för alla moduler</span><span class="sxs-lookup"><span data-stu-id="b6b44-756">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="b6b44-757">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b6b44-757">Az.Accounts</span></span>
* <span data-ttu-id="b6b44-758">Ange rätt UserAgent för telemetri på klientsidan för Az 4.0 preview</span><span class="sxs-lookup"><span data-stu-id="b6b44-758">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="b6b44-759">Visa användarvänligt felmeddelande när kontexten är null i Az 4.0 preview</span><span class="sxs-lookup"><span data-stu-id="b6b44-759">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="b6b44-760">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="b6b44-760">Az.Batch</span></span>
* <span data-ttu-id="b6b44-761">Korrigera problem [#10602](https://github.com/Azure/azure-powershell/issues/10602), där **New-AzBatchPool** skickade VirtualMachineConfiguration.ContainerConfiguration eller VirtualMachineConfiguration.DataDisks på ett felaktigt sätt till servern.</span><span class="sxs-lookup"><span data-stu-id="b6b44-761">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b6b44-762">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b6b44-762">Az.DataFactory</span></span>
* <span data-ttu-id="b6b44-763">Uppdatera ADF .Net SDK-versionen till 4.5.0</span><span class="sxs-lookup"><span data-stu-id="b6b44-763">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="b6b44-764">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="b6b44-764">Az.FrontDoor</span></span>
* <span data-ttu-id="b6b44-765">Stöd har lagts till för undantag för hanterade regler för brandväggen för webbaserade program</span><span class="sxs-lookup"><span data-stu-id="b6b44-765">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="b6b44-766">Lägg till SocketAddr för automatisk komplettering</span><span class="sxs-lookup"><span data-stu-id="b6b44-766">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="b6b44-767">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="b6b44-767">Az.HealthcareApis</span></span>
* <span data-ttu-id="b6b44-768">Undantagshantering</span><span class="sxs-lookup"><span data-stu-id="b6b44-768">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="b6b44-769">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b6b44-769">Az.KeyVault</span></span>
* <span data-ttu-id="b6b44-770">Åtgärdat fel vid åtkomst av värde som kanske inte har angetts</span><span class="sxs-lookup"><span data-stu-id="b6b44-770">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="b6b44-771">Hantering av ECC-certifikat (Elliptic Curve Cryptography)</span><span class="sxs-lookup"><span data-stu-id="b6b44-771">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="b6b44-772">Stöd har lagts till för att ange kurvan för certifikatprinciper</span><span class="sxs-lookup"><span data-stu-id="b6b44-772">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="b6b44-773">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b6b44-773">Az.Monitor</span></span>
* <span data-ttu-id="b6b44-774">Lägger till valfritt argument i kommandot Lägg till diagnostikinställningar.</span><span class="sxs-lookup"><span data-stu-id="b6b44-774">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="b6b44-775">Ett växelargument som om det finns visar att exporten till Log Analytics måste ske till ett fast schema (kallas även</span><span class="sxs-lookup"><span data-stu-id="b6b44-775">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="b6b44-776">dedikerad, datatyp)</span><span class="sxs-lookup"><span data-stu-id="b6b44-776">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b6b44-777">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b6b44-777">Az.Network</span></span>
* <span data-ttu-id="b6b44-778">Stöd för IpGroups i program-, NAT- och nätverksregler för Azure Firewall.</span><span class="sxs-lookup"><span data-stu-id="b6b44-778">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="b6b44-779">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b6b44-779">Az.Resources</span></span>
* <span data-ttu-id="b6b44-780">Åtgärda ett problem där malldistributionen inte kan läsa en mallparameter om dess namn står i konflikt med ett inbyggt parameternamn.</span><span class="sxs-lookup"><span data-stu-id="b6b44-780">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="b6b44-781">Uppdaterade princip-cmdletar för att använda den nya API-versionen 2019-09-01 som introducerar grupperingsstöd inom principuppsättningsdefinitioner.</span><span class="sxs-lookup"><span data-stu-id="b6b44-781">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="b6b44-782">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b6b44-782">Az.Sql</span></span>
* <span data-ttu-id="b6b44-783">Uppgraderad funktion för att skapa lagring i automatisk aktivering av sårbarhetsbedömning till StorageV2</span><span class="sxs-lookup"><span data-stu-id="b6b44-783">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b6b44-784">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b6b44-784">Az.Storage</span></span>
* <span data-ttu-id="b6b44-785">Stöd för generering av blob/container-identitetsbaserad SAS-token med lagringskontextbaserad på OAuth-autentisering</span><span class="sxs-lookup"><span data-stu-id="b6b44-785">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="b6b44-786">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="b6b44-786">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="b6b44-787">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="b6b44-787">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="b6b44-788">Stöd för återkallning av användardelegeringsnycklar för lagringskonto för att återkalla alla SAS-token</span><span class="sxs-lookup"><span data-stu-id="b6b44-788">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="b6b44-789">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="b6b44-789">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="b6b44-790">Uppgradera till Microsoft.Azure.Management.Storage 14.2.0 för att stödja den nya API-versionen 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="b6b44-790">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="b6b44-791">Stöd för QuotaGiB (resurskvot i Gibibye) för värden över 5120 i hanteringsplanet för cmdletar för filresurser och parameteraliaset. Quota har också lagts till för parametern ”QuotaGiB”.</span><span class="sxs-lookup"><span data-stu-id="b6b44-791">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="b6b44-792">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="b6b44-792">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="b6b44-793">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="b6b44-793">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="b6b44-794">Lägg till parameteraliaset QuotaGiB i parametern Quota</span><span class="sxs-lookup"><span data-stu-id="b6b44-794">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="b6b44-795">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="b6b44-795">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="b6b44-796">Åtgärda problemet att Set-AzStorageContainerAcl kan rensa den lagrade åtkomstprincipen</span><span class="sxs-lookup"><span data-stu-id="b6b44-796">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="b6b44-797">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="b6b44-797">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="b6b44-798">3.1.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="b6b44-798">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="b6b44-799">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="b6b44-799">Highlights since the last major release</span></span>
* <span data-ttu-id="b6b44-800">Az.DataBoxEdge 1.0.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="b6b44-800">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="b6b44-801">Az.SqlVirtualMachine 1.0.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="b6b44-801">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b6b44-802">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b6b44-802">Az.Compute</span></span>
* <span data-ttu-id="b6b44-803">Funktion för att använda en virtuell dator igen</span><span class="sxs-lookup"><span data-stu-id="b6b44-803">VM Reapply feature</span></span>
    - <span data-ttu-id="b6b44-804">Lägg till parameter för att använda igen till cmdleten Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="b6b44-804">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="b6b44-805">Funktionen AutomaticRepairs i VM-skalningsuppsättningar:</span><span class="sxs-lookup"><span data-stu-id="b6b44-805">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="b6b44-806">Lägg till parametrarna EnableAutomaticRepair, AutomaticRepairGracePeriod och AutomaticRepairMaxInstanceRepairsPercent till följande cmdletar:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b6b44-806">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="b6b44-807">Stöd för galleriavbildningar i flera klientorganisationer för New-AzVM</span><span class="sxs-lookup"><span data-stu-id="b6b44-807">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="b6b44-808">Lägg till "Spot" till argumentslutföraren i prioritetsparametern i cmdletarna New-AzVM, New-AzVMConfig och New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b6b44-808">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="b6b44-809">Lägg till parametrarna DiskIOPSReadWrite och DiskMBpsReadWrite till cmdleten Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="b6b44-809">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="b6b44-810">Ändra parametern SourceImageId för cmdleten New-AzGalleryImageVersion till valfri</span><span class="sxs-lookup"><span data-stu-id="b6b44-810">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="b6b44-811">Lägg till parametrarna OSDiskImage och DataDiskImage till cmdleten New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="b6b44-811">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="b6b44-812">Lägg till parametern HyperVGeneration till cmdleten New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="b6b44-812">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="b6b44-813">Lägg till parametern SkipExtensionsOnOverprovisionedVMs till cmdletarna New-AzVmss, New-AzVmssConfig och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b6b44-813">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="b6b44-814">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="b6b44-814">Az.DataBoxEdge</span></span>
* <span data-ttu-id="b6b44-815">Cmdleten `Get-AzDataBoxEdgeOrder` har lagts till</span><span class="sxs-lookup"><span data-stu-id="b6b44-815">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="b6b44-816">Hämta ordning</span><span class="sxs-lookup"><span data-stu-id="b6b44-816">Get the Order</span></span>
* <span data-ttu-id="b6b44-817">Cmdleten `New-AzDataBoxEdgeOrder` har lagts till</span><span class="sxs-lookup"><span data-stu-id="b6b44-817">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="b6b44-818">Skapa ny ordning</span><span class="sxs-lookup"><span data-stu-id="b6b44-818">Create new Order</span></span>
* <span data-ttu-id="b6b44-819">Cmdleten `Remove-AzDataBoxEdgeOrder` har lagts till</span><span class="sxs-lookup"><span data-stu-id="b6b44-819">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="b6b44-820">Ta bort ordning</span><span class="sxs-lookup"><span data-stu-id="b6b44-820">Remove the Order</span></span>
* <span data-ttu-id="b6b44-821">Cmdleten `New-AzDataBoxEdgeShare` har ändrats</span><span class="sxs-lookup"><span data-stu-id="b6b44-821">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="b6b44-822">Nu skapas lokal filresurs</span><span class="sxs-lookup"><span data-stu-id="b6b44-822">Now creates Local Share</span></span>
* <span data-ttu-id="b6b44-823">Cmdleten `Set-AzDataBoxEdgeRole` har lagts till</span><span class="sxs-lookup"><span data-stu-id="b6b44-823">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="b6b44-824">Nu kan IotRole mappas till filresursen</span><span class="sxs-lookup"><span data-stu-id="b6b44-824">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="b6b44-825">Cmdleten `Invoke-AzDataBoxEdgeDevice` har lagts till</span><span class="sxs-lookup"><span data-stu-id="b6b44-825">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="b6b44-826">Anropa genomsökningsuppdatering, ladda ned uppdatering, installera uppdateringar på enheten</span><span class="sxs-lookup"><span data-stu-id="b6b44-826">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="b6b44-827">Cmdleten `Get-AzDataBoxEdgeTrigger` har lagts till</span><span class="sxs-lookup"><span data-stu-id="b6b44-827">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="b6b44-828">Hämtar information om utlösare</span><span class="sxs-lookup"><span data-stu-id="b6b44-828">Gets the information about Triggers</span></span>
* <span data-ttu-id="b6b44-829">Cmdleten `New-AzDataBoxEdgeTrigger` har lagts till</span><span class="sxs-lookup"><span data-stu-id="b6b44-829">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="b6b44-830">Skapa nya utlösare</span><span class="sxs-lookup"><span data-stu-id="b6b44-830">Create new Triggers</span></span>
* <span data-ttu-id="b6b44-831">Cmdleten `Remove-AzDataBoxEdgeTrigger` har lagts till</span><span class="sxs-lookup"><span data-stu-id="b6b44-831">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="b6b44-832">Ta bort utlösare</span><span class="sxs-lookup"><span data-stu-id="b6b44-832">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b6b44-833">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b6b44-833">Az.DataFactory</span></span>
* <span data-ttu-id="b6b44-834">Uppdatera ADF .Net SDK-versionen till 4.4.0</span><span class="sxs-lookup"><span data-stu-id="b6b44-834">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="b6b44-835">Lägg till parametern ExpressCustomSetup för kommandot Set-AzureRmDataFactoryV2IntegrationRuntime för att aktivera installationskonfigurationer och komponenter från tredje part utan anpassat konfigurationsskript.</span><span class="sxs-lookup"><span data-stu-id="b6b44-835">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b6b44-836">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b6b44-836">Az.DataLakeStore</span></span>
* <span data-ttu-id="b6b44-837">Uppdatera dokumentation för Get-AzDataLakeStoreDeletedItem och Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="b6b44-837">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="b6b44-838">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="b6b44-838">Az.EventHub</span></span>
* <span data-ttu-id="b6b44-839">Korrigering av problem #10301: Korrigera datumformat för SAS-token</span><span class="sxs-lookup"><span data-stu-id="b6b44-839">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="b6b44-840">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="b6b44-840">Az.FrontDoor</span></span>
* <span data-ttu-id="b6b44-841">Lägg till parametern MinimumTlsVersion till Enable-AzFrontDoorCustomDomainHttps och New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="b6b44-841">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="b6b44-842">Lägg till parametrarna HealthProbeMethod och EnabledState till New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="b6b44-842">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="b6b44-843">Lägg till en ny cmdlet för att skapa BackendPoolsSettings-objekt som passar i skapande/uppdatering av Front Door</span><span class="sxs-lookup"><span data-stu-id="b6b44-843">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="b6b44-844">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="b6b44-844">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b6b44-845">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b6b44-845">Az.Network</span></span>
* <span data-ttu-id="b6b44-846">Ändra alternativexemplen Start-AzVirtualNetworkGatewayConnectionPacketCapture.md och Start-AzVirtualnetworkGatewayPacketCapture.md för FilterData.</span><span class="sxs-lookup"><span data-stu-id="b6b44-846">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="b6b44-847">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="b6b44-847">Az.PrivateDns</span></span>
* <span data-ttu-id="b6b44-848">Uppdaterade PrivateDns .NET SDK till version 1.0.0</span><span class="sxs-lookup"><span data-stu-id="b6b44-848">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b6b44-849">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b6b44-849">Az.RecoveryServices</span></span>
* <span data-ttu-id="b6b44-850">Stöd för att välja disktyp vid aktivering av skydd i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="b6b44-850">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="b6b44-851">Korrigering av bugg för åtgärdsredigering av återställningsplan i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="b6b44-851">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="b6b44-852">Återställningsstöd för att godkänna filestream-databaser i Azure Backup SQL.</span><span class="sxs-lookup"><span data-stu-id="b6b44-852">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="b6b44-853">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="b6b44-853">Az.RedisCache</span></span>
* <span data-ttu-id="b6b44-854">Parametern MinimumTlsVersion har lagts till i cmdletarna New-AzRedisCache och Set-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="b6b44-854">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="b6b44-855">Dessutom har MinimumTlsVersion lagts till i utdata för cmdleten Get-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="b6b44-855">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="b6b44-856">Verifiering har lagts till på parametern -Size i cmdletarna Set-AzRedisCache och New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="b6b44-856">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="b6b44-857">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b6b44-857">Az.Resources</span></span>
- <span data-ttu-id="b6b44-858">Uppdaterade policy-cmdletar för att använda den nya API-versionen 2019-06-01 som har en ny EnforcementMode-egenskap i policytilldelningen.</span><span class="sxs-lookup"><span data-stu-id="b6b44-858">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="b6b44-859">Uppdaterade hjälpexempel för skapandet av policydefinition</span><span class="sxs-lookup"><span data-stu-id="b6b44-859">Updated create policy definition help example</span></span>
- <span data-ttu-id="b6b44-860">Åtgärda bugg i Remove-AZADServicePrincipal -ServicePrincipalName, utlös null-referens när tjänstens huvudnamn inte hittas.</span><span class="sxs-lookup"><span data-stu-id="b6b44-860">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="b6b44-861">Åtgärda bugg i New-AZADServicePrincipal, utlös null-referens när klientorganisationen inte har någon prenumeration.</span><span class="sxs-lookup"><span data-stu-id="b6b44-861">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="b6b44-862">Ändra New-AzAdServicePrincipal för att endast lägga till autentiseringsuppgifter för det associerade programmet.</span><span class="sxs-lookup"><span data-stu-id="b6b44-862">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="b6b44-863">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b6b44-863">Az.Sql</span></span>
* <span data-ttu-id="b6b44-864">Stöd har lagts till för databasen ReadReplicaCount.</span><span class="sxs-lookup"><span data-stu-id="b6b44-864">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="b6b44-865">Korrigerade Set-AzSqlDatabase när zonredundans inte har angetts</span><span class="sxs-lookup"><span data-stu-id="b6b44-865">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="b6b44-866">3.0.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="b6b44-866">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="b6b44-867">Allmänt</span><span class="sxs-lookup"><span data-stu-id="b6b44-867">General</span></span>
* <span data-ttu-id="b6b44-868">Az. PrivateDns 1.0.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="b6b44-868">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="b6b44-869">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b6b44-869">Az.Accounts</span></span>
* <span data-ttu-id="b6b44-870">Lägg till ett utfasningsmeddelande för aliaset Resolve-error.</span><span class="sxs-lookup"><span data-stu-id="b6b44-870">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="b6b44-871">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="b6b44-871">Az.Advisor</span></span>
* <span data-ttu-id="b6b44-872">Den nya kategorin Operational Excellence har lagts till i cmdleten Get-AzAdvisorRecommendation.</span><span class="sxs-lookup"><span data-stu-id="b6b44-872">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="b6b44-873">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="b6b44-873">Az.Batch</span></span>
* <span data-ttu-id="b6b44-874">`CoreQuota` på `BatchAccountContext` har bytt namn till `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="b6b44-874">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="b6b44-875">Det finns även en ny `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="b6b44-875">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="b6b44-876">Detta påverkar **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="b6b44-876">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="b6b44-877">**New-AzBatchTask** `-ResourceFile`-parametern tar nu en samling `PSResourceFile`-objekt som kan skapas med hjälp av den nya cmdleten **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="b6b44-877">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="b6b44-878">Ny **New-AzBatchResourceFile**-cmdlet för att skapa `PSResourceFile`-objekt.</span><span class="sxs-lookup"><span data-stu-id="b6b44-878">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="b6b44-879">Dessa kan tillhandahållas till **New-AzBatchTask** på `-ResourceFile`-parametern.</span><span class="sxs-lookup"><span data-stu-id="b6b44-879">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="b6b44-880">Detta stöder två nya typer av resursfiler förutom det befintliga sättet med `HttpUrl`:</span><span class="sxs-lookup"><span data-stu-id="b6b44-880">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="b6b44-881">`AutoStorageContainerName`-baserade resursfiler laddar ned en hel container för automatisk lagring till Batch-noden.</span><span class="sxs-lookup"><span data-stu-id="b6b44-881">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="b6b44-882">`StorageContainerUrl`-baserade resursfiler laddar ned containern som anges i webbadressen till Batch-noden.</span><span class="sxs-lookup"><span data-stu-id="b6b44-882">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="b6b44-883">Tog bort egenskapen `ApplicationPackages` för `PSApplication` som returnerades av **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="b6b44-883">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="b6b44-884">Specifika paket i ett program kan nu hämtas med hjälp av **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="b6b44-884">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="b6b44-885">Till exempel: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="b6b44-885">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="b6b44-886">Bytt namn på `ApplicationId` till `ApplicationName` på **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** och **Set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="b6b44-886">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="b6b44-887">`ApplicationId` är nu ett alias för `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="b6b44-887">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="b6b44-888">Ny `PSWindowsUserConfiguration`-egenskap till `PSUserAccount` lades till.</span><span class="sxs-lookup"><span data-stu-id="b6b44-888">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="b6b44-889">Bytte namn på `Version` till `Name` på `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="b6b44-889">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="b6b44-890">Bytte namn på `BlobSource` till `HttpUrl` på `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="b6b44-890">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="b6b44-891">Tog bort egenskapen `OSDisk` från `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="b6b44-891">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="b6b44-892">Tog bort **Set-AzBatchPoolOSVersion**.</span><span class="sxs-lookup"><span data-stu-id="b6b44-892">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="b6b44-893">Den här åtgärden stöds inte längre.</span><span class="sxs-lookup"><span data-stu-id="b6b44-893">This operation is no longer supported.</span></span>
* <span data-ttu-id="b6b44-894">`TargetOSVersion` har tagits bort från `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="b6b44-894">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="b6b44-895">Bytte namn på `CurrentOSVersion` till `OSVersion` på `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="b6b44-895">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="b6b44-896">`DataEgressGiB` och `DataIngressGiB` har tagits bort från `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="b6b44-896">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="b6b44-897">Tog bort **Get-AzBatchNodeAgentSku** och ersatte det med **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="b6b44-897">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="b6b44-898">**Get-AzBatchSupportedImage** returnerar samma data som **Get-AzBatchNodeAgentSku** men i ett mer användarvänligt format.</span><span class="sxs-lookup"><span data-stu-id="b6b44-898">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="b6b44-899">Nya icke-verifierade avbildningar returneras nu också.</span><span class="sxs-lookup"><span data-stu-id="b6b44-899">New non-verified images are also now returned.</span></span> <span data-ttu-id="b6b44-900">Ytterligare information om `Capabilities` och `BatchSupportEndOfLife` för varje avbildning inkluderas också.</span><span class="sxs-lookup"><span data-stu-id="b6b44-900">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="b6b44-901">Lade till möjlighet att montera fjärrfilsystem på varje nod i en pool via den nya parametern `MountConfiguration` för **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="b6b44-901">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="b6b44-902">Har nu stöd för nätverkssäkerhetsregler som blockerar nätverksåtkomst till en pool baserat på källportens trafik.</span><span class="sxs-lookup"><span data-stu-id="b6b44-902">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="b6b44-903">Detta görs via egenskapen `SourcePortRanges` på `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="b6b44-903">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="b6b44-904">När du kör en container stöder nu Batch körningen av uppgiften i arbetskatalogen för containern eller i arbetskatalogen för Batch-uppgiften.</span><span class="sxs-lookup"><span data-stu-id="b6b44-904">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="b6b44-905">Detta styrs av egenskapen `WorkingDirectory` på `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="b6b44-905">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="b6b44-906">Lade till en funktion för att ange en samling av offentliga IP-adresser på `PSNetworkConfiguration` via den nya egenskapen `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="b6b44-906">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="b6b44-907">Detta garanterar att noderna i poolen har en IP-adress från listan över IP-adresser som tillhandahållits av användare.</span><span class="sxs-lookup"><span data-stu-id="b6b44-907">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="b6b44-908">Om inget värde anges är standardvärdet för `WaitForSuccess` på `PSSTartTask` nu `$True` (var tidigare `$False`).</span><span class="sxs-lookup"><span data-stu-id="b6b44-908">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="b6b44-909">Om inget värde anges är standardvärdet för `Scope` på `PSAutoUserSpecification` nu `Pool` (var tidigare `Task` på Windows och `Pool` på Linux).</span><span class="sxs-lookup"><span data-stu-id="b6b44-909">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="b6b44-910">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="b6b44-910">Az.Cdn</span></span>
* <span data-ttu-id="b6b44-911">Introducerade UrlRewriteAction och CacheKeyQueryStringAction till RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="b6b44-911">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="b6b44-912">Åtgärdade flera buggar, som saknade indata för ”väljare” i cmdleten New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="b6b44-912">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b6b44-913">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b6b44-913">Az.Compute</span></span>
* <span data-ttu-id="b6b44-914">Funktion för diskkrypteringsuppsättning</span><span class="sxs-lookup"><span data-stu-id="b6b44-914">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="b6b44-915">Nya cmdletar:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="b6b44-915">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="b6b44-916">Parametern DiskEncryptionSetId har lagts till i följande cmdletar:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="b6b44-916">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="b6b44-917">Parametrarna DiskEncryptionSetId och EncryptionType har lagts till i följande cmdletar:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="b6b44-917">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="b6b44-918">Lägg till parametern PublicIPAddressVersion i New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="b6b44-918">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="b6b44-919">Flytta FileUris för anpassat skripttillägg från offentlig inställning till skyddad inställning</span><span class="sxs-lookup"><span data-stu-id="b6b44-919">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="b6b44-920">Lägg till ScaleInPolicy i cmdletarna New-AzVmss, New-AzVmssConfig och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b6b44-920">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="b6b44-921">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="b6b44-921">Breaking changes</span></span>
    - <span data-ttu-id="b6b44-922">Parametern UploadSizeInBytes används istället för DiskSizeGB för New-AzDiskConfig när CreateOption är Uppladdning</span><span class="sxs-lookup"><span data-stu-id="b6b44-922">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="b6b44-923">PublishingProfile.Source.ManagedImage.Id ersätts med StorageProfile.Source.Id i objektet GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="b6b44-923">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b6b44-924">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b6b44-924">Az.DataFactory</span></span>
* <span data-ttu-id="b6b44-925">Uppdatera ADF .Net SDK-versionen till 4.3.0</span><span class="sxs-lookup"><span data-stu-id="b6b44-925">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b6b44-926">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b6b44-926">Az.DataLakeStore</span></span>
* <span data-ttu-id="b6b44-927">Uppdatera ADLS SDK-version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) innehåller följande korrigeringar</span><span class="sxs-lookup"><span data-stu-id="b6b44-927">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="b6b44-928">Undvik att utlösa undantag när det inte går att deserialisera creationtime för inmatning av papperskorg eller katalog.</span><span class="sxs-lookup"><span data-stu-id="b6b44-928">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="b6b44-929">Gör inställning tillgänglig per tidsgräns för förfrågan i adlsclient</span><span class="sxs-lookup"><span data-stu-id="b6b44-929">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="b6b44-930">Korrigera överföringen av ursprunglig syncflag för badoffset-återställning</span><span class="sxs-lookup"><span data-stu-id="b6b44-930">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="b6b44-931">Korrigera EnumerateDirectory för att hämta fortsättningstoken när svar har kontrollerats</span><span class="sxs-lookup"><span data-stu-id="b6b44-931">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="b6b44-932">Korrigera bugg i Concat</span><span class="sxs-lookup"><span data-stu-id="b6b44-932">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="b6b44-933">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="b6b44-933">Az.FrontDoor</span></span>
* <span data-ttu-id="b6b44-934">Åtgärdade diverse stavfel i modul</span><span class="sxs-lookup"><span data-stu-id="b6b44-934">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="b6b44-935">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="b6b44-935">Az.HDInsight</span></span>
* <span data-ttu-id="b6b44-936">Korrigerade buggen att kunder får felet ”inte en giltig Base-64-sträng” vid användning av Get-AzHDInsightCluster för att hämta klustret med ADLSGen1-lagring.</span><span class="sxs-lookup"><span data-stu-id="b6b44-936">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="b6b44-937">Lägg till en parameter med namnet ”ApplicationId” i de tre cmdletarna Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig och New-AzHDInsightCluster så att kunden kan tillhandahålla tjänstens huvudnamn för program-ID för åtkomst till Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="b6b44-937">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="b6b44-938">Ändrade Microsoft.Azure.Management.HDInsight från 2.1.0 till 5.1.0</span><span class="sxs-lookup"><span data-stu-id="b6b44-938">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="b6b44-939">Fem cmdletar har tagits bort:</span><span class="sxs-lookup"><span data-stu-id="b6b44-939">Removed five cmdlets:</span></span>
    - <span data-ttu-id="b6b44-940">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="b6b44-940">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="b6b44-941">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="b6b44-941">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="b6b44-942">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="b6b44-942">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="b6b44-943">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="b6b44-943">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="b6b44-944">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="b6b44-944">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="b6b44-945">Tre cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="b6b44-945">Added three cmdlets:</span></span>
    - <span data-ttu-id="b6b44-946">Get-AzHDInsightMonitoring som ersätter Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="b6b44-946">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="b6b44-947">Enable-AzHDInsightMonitoring som ersätter Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="b6b44-947">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="b6b44-948">Disable-AzHDInsightMonitoring som ersätter Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="b6b44-948">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="b6b44-949">Korrigerade cmdleten Get-AzHDInsightProperties för att stödja hämtning av funktionsinformation från en viss plats.</span><span class="sxs-lookup"><span data-stu-id="b6b44-949">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="b6b44-950">Parameteruppsättningarna (Spark1 och Spark2) har tagits bort från Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="b6b44-950">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="b6b44-951">Lägg till exempel för cmdleten Add-AzHDInsightSecurityProfile till hjälpdokumenten.</span><span class="sxs-lookup"><span data-stu-id="b6b44-951">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="b6b44-952">Ändrade utdatatyp för följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="b6b44-952">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="b6b44-953">Ändrade utdatatyp för Get-AzHDInsightProperties från CapabilitiesResponse till AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="b6b44-953">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="b6b44-954">Ändrade utdatatyp för Remove-AzHDInsightCluster från ClusterGetResponse till bool.</span><span class="sxs-lookup"><span data-stu-id="b6b44-954">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="b6b44-955">Ändrade utdatatyp för Set-AzHDInsightGatewaySettings HttpConnectivitySettings till GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="b6b44-955">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="b6b44-956">Lade till testfall för vissa scenarier.</span><span class="sxs-lookup"><span data-stu-id="b6b44-956">Added some scenario test cases.</span></span>
* <span data-ttu-id="b6b44-957">Ta bort vissa alias: Add-AzHDInsightConfigValues, Get-AzHDInsightProperties.</span><span class="sxs-lookup"><span data-stu-id="b6b44-957">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="b6b44-958">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="b6b44-958">Az.IotHub</span></span>
* <span data-ttu-id="b6b44-959">Icke-bakåtkompatibla ändringar:</span><span class="sxs-lookup"><span data-stu-id="b6b44-959">Breaking changes:</span></span>
    - <span data-ttu-id="b6b44-960">Cmdleten Add-AzIotHubEventHubConsumerGroup har inte längre stöd för parametern EventHubEndpointName och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="b6b44-960">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="b6b44-961">Parameteruppsättningen __AllParameterSets för cmdleten Add-AzIotHubEventHubConsumerGroup har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="b6b44-961">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="b6b44-962">Cmdleten Get-AzIotHubEventHubConsumerGroup har inte längre stöd för parametern EventHubEndpointName och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="b6b44-962">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="b6b44-963">Parameteruppsättningen __AllParameterSets för cmdleten Get-AzIotHubEventHubConsumerGroup har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="b6b44-963">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="b6b44-964">Egenskapen OperationsMonitoringProperties av typen Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="b6b44-964">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="b6b44-965">Egenskapen OperationsMonitoringProperties av typen Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="b6b44-965">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="b6b44-966">Cmdleten New-AzIotHubExportDevice stöder inte längre aliaset New-AzIotHubExportDevices.</span><span class="sxs-lookup"><span data-stu-id="b6b44-966">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="b6b44-967">Cmdleten New-AzIotHubImportDevice stöder inte längre aliaset New-AzIotHubImportDevices.</span><span class="sxs-lookup"><span data-stu-id="b6b44-967">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="b6b44-968">Cmdleten Remove-AzIotHubEventHubConsumerGroup har inte längre stöd för parametern EventHubEndpointName och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="b6b44-968">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="b6b44-969">Parameteruppsättningen __AllParameterSets för cmdleten Remove-AzIotHubEventHubConsumerGroup har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="b6b44-969">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="b6b44-970">Cmdleten Set-AzIotHub har inte längre stöd för parametern OperationsMonitoringProperties och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="b6b44-970">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="b6b44-971">Parameteruppsättningen UpdateOperationsMonitoringProperties för cmdleten Set-AzIotHub har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="b6b44-971">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b6b44-972">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b6b44-972">Az.RecoveryServices</span></span>
* <span data-ttu-id="b6b44-973">Azure Site Recovery-stöd för att konfigurera nätverksresurser som NSG, offentliga IP-adresser och interna lastbalanserare för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="b6b44-973">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="b6b44-974">Azure Site Recovery-stöd för att skriva till hanterad disk för vMWare till Azure.</span><span class="sxs-lookup"><span data-stu-id="b6b44-974">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="b6b44-975">Azure Site Recovery-stöd för NIC-reduktion för vMWare till Azure.</span><span class="sxs-lookup"><span data-stu-id="b6b44-975">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="b6b44-976">Azure Site Recovery-stöd för accelererat nätverk för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="b6b44-976">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="b6b44-977">Azure Site Recovery-stöd för automatisk uppdatering av agent för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="b6b44-977">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="b6b44-978">Azure Site Recovery-stöd för Standard SSD för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="b6b44-978">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="b6b44-979">Azure Site Recovery-stöd för tvåstegskryptering i Azure Disk Encryption för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="b6b44-979">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="b6b44-980">Azure Site Recovery-stöd för att skydda nyligen tillagda diskar för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="b6b44-980">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="b6b44-981">En funktion för mjuk borttagning av virtuella datorer samt tester för mjuk borttagning har tagits bort</span><span class="sxs-lookup"><span data-stu-id="b6b44-981">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="b6b44-982">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b6b44-982">Az.Resources</span></span>
* <span data-ttu-id="b6b44-983">Uppdatera beroendesammansättning för Microsoft.Extensions.Caching.Memory från 1.1.1 till 2.2</span><span class="sxs-lookup"><span data-stu-id="b6b44-983">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b6b44-984">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b6b44-984">Az.Network</span></span>
* <span data-ttu-id="b6b44-985">Ändra alla cmdletar för PrivateEndpointConnection så att de stöder generiska tjänstleverantörer.</span><span class="sxs-lookup"><span data-stu-id="b6b44-985">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="b6b44-986">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="b6b44-986">Updated cmdlet:</span></span>
        - <span data-ttu-id="b6b44-987">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="b6b44-987">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="b6b44-988">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="b6b44-988">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="b6b44-989">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="b6b44-989">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="b6b44-990">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="b6b44-990">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="b6b44-991">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="b6b44-991">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="b6b44-992">Lägg till ny cmdlet för PrivateLinkResource så att det också stöder generiska tjänstleverantörer.</span><span class="sxs-lookup"><span data-stu-id="b6b44-992">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="b6b44-993">Ny cmdlet:</span><span class="sxs-lookup"><span data-stu-id="b6b44-993">New cmdlet:</span></span>
        - <span data-ttu-id="b6b44-994">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="b6b44-994">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="b6b44-995">Lägg till nya fält och parametrar för funktionen Proxy Protocol V2.</span><span class="sxs-lookup"><span data-stu-id="b6b44-995">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="b6b44-996">Lägg till egenskapen EnableProxyProtocol i PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="b6b44-996">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="b6b44-997">Lägg till egenskapen LinkIdentifier i PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="b6b44-997">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="b6b44-998">Uppdaterade New-AzPrivateLinkService för att lägga till den nya valfria parametern EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="b6b44-998">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="b6b44-999">Korrigera felaktig beskrivning av parameter i referensdokumentationen för New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="b6b44-999">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="b6b44-1000">Nya cmdletar som stöder Azure-brandväggsprincipen</span><span class="sxs-lookup"><span data-stu-id="b6b44-1000">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="b6b44-1001">Lägg till stöd för den underordnade resursen RouteTables för VirtualHub</span><span class="sxs-lookup"><span data-stu-id="b6b44-1001">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="b6b44-1002">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="b6b44-1002">New cmdlets added:</span></span>
        - <span data-ttu-id="b6b44-1003">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="b6b44-1003">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="b6b44-1004">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="b6b44-1004">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="b6b44-1005">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="b6b44-1005">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="b6b44-1006">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="b6b44-1006">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="b6b44-1007">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="b6b44-1007">Set-AzVirtualHub</span></span>
* <span data-ttu-id="b6b44-1008">Lägg till stöd för ny egenskaps-SKU för VirtualHub och VirtualWANType för VirtualWan</span><span class="sxs-lookup"><span data-stu-id="b6b44-1008">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="b6b44-1009">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="b6b44-1009">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="b6b44-1010">New-AzVirtualHub: lade till parameter-SKU</span><span class="sxs-lookup"><span data-stu-id="b6b44-1010">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="b6b44-1011">Update-AzVirtualHub: lade till parameter-SKU</span><span class="sxs-lookup"><span data-stu-id="b6b44-1011">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="b6b44-1012">New-AzVirtualWan: lade till parametern VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="b6b44-1012">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="b6b44-1013">Update-AzVirtualWan: lade till parametern VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="b6b44-1013">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="b6b44-1014">Lägg till stöd för egenskapen EnableInternetSecurity för HubVnetConnection, VpnConnection och ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="b6b44-1014">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="b6b44-1015">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="b6b44-1015">New cmdlets added:</span></span>
        - <span data-ttu-id="b6b44-1016">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="b6b44-1016">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="b6b44-1017">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="b6b44-1017">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="b6b44-1018">New-AzureRmVirtualHubVnetConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="b6b44-1018">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="b6b44-1019">New-AzureRmVpnConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="b6b44-1019">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="b6b44-1020">Update-AzureRmVpnConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="b6b44-1020">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="b6b44-1021">New-AzureRmExpressRouteConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="b6b44-1021">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="b6b44-1022">Set-AzureRmExpressRouteConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="b6b44-1022">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="b6b44-1023">Lägg till stöd för att konfigurera TopLevel WebApplicationFirewall-princip</span><span class="sxs-lookup"><span data-stu-id="b6b44-1023">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="b6b44-1024">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="b6b44-1024">New cmdlets added:</span></span>
        - <span data-ttu-id="b6b44-1025">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="b6b44-1025">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="b6b44-1026">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="b6b44-1026">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="b6b44-1027">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="b6b44-1027">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="b6b44-1028">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="b6b44-1028">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="b6b44-1029">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="b6b44-1029">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="b6b44-1030">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="b6b44-1030">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="b6b44-1031">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="b6b44-1031">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="b6b44-1032">New-AzApplicationGatewayFirewallPolicy: parametrarna PolicySetting, ManagedRule har lagts till</span><span class="sxs-lookup"><span data-stu-id="b6b44-1032">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="b6b44-1033">Stöd för operator för geomatchning har lagts till på CustomRule</span><span class="sxs-lookup"><span data-stu-id="b6b44-1033">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="b6b44-1034">Geomatchning har lagts till i operatorn på FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="b6b44-1034">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="b6b44-1035">Stöd har lagts till för brandväggsprinciperna perListener och perSite</span><span class="sxs-lookup"><span data-stu-id="b6b44-1035">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="b6b44-1036">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="b6b44-1036">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="b6b44-1037">New-AzApplicationGatewayHttpListener: parametrarna FirewallPolicy, FirewallPolicyId har lagts till</span><span class="sxs-lookup"><span data-stu-id="b6b44-1037">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="b6b44-1038">New-AzApplicationGatewayPathRuleConfig: parametrarna FirewallPolicy, FirewallPolicyId har lagts till</span><span class="sxs-lookup"><span data-stu-id="b6b44-1038">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="b6b44-1039">Åtgärdat så att nödvändigt undernät med namnet AzureBastionSubnet i PSBastion kan vara skiftlägesokänsligt</span><span class="sxs-lookup"><span data-stu-id="b6b44-1039">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="b6b44-1040">Stöd för mål-FQDN:er i nätverksregler och översatt FQDN i NAT-regler för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="b6b44-1040">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="b6b44-1041">Lägg till stöd för resursen RouteTables för IpGroup på den högsta nivån</span><span class="sxs-lookup"><span data-stu-id="b6b44-1041">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="b6b44-1042">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="b6b44-1042">New cmdlets added:</span></span>
        - <span data-ttu-id="b6b44-1043">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="b6b44-1043">New-AzIpGroup</span></span>
        - <span data-ttu-id="b6b44-1044">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="b6b44-1044">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="b6b44-1045">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="b6b44-1045">Get-AzIpGroup</span></span>
        - <span data-ttu-id="b6b44-1046">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="b6b44-1046">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="b6b44-1047">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b6b44-1047">Az.ServiceFabric</span></span>
* <span data-ttu-id="b6b44-1048">Ta bort cmdleten Add-AzServiceFabricApplicationCertificate eftersom det här scenariot omfattas av Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1048">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="b6b44-1049">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b6b44-1049">Az.Sql</span></span>
* <span data-ttu-id="b6b44-1050">Stöd har lagts till för återställning av utelämnade databaser på hanterade instanser.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1050">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="b6b44-1051">Inaktuella gamla cmdletar för granskning från kod.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1051">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="b6b44-1052">Tog bort inaktuella alias:</span><span class="sxs-lookup"><span data-stu-id="b6b44-1052">Removed deprecated aliases:</span></span>
* <span data-ttu-id="b6b44-1053">Get-AzSqlDatabaseIndexRecommendations (använd Get-AzSqlDatabaseIndexRecommendation istället)</span><span class="sxs-lookup"><span data-stu-id="b6b44-1053">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="b6b44-1054">Get-AzSqlDatabaseRestorePoints (använd Get-AzSqlDatabaseRestorePoint istället)</span><span class="sxs-lookup"><span data-stu-id="b6b44-1054">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="b6b44-1055">Ta bort cmdleten Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b6b44-1055">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="b6b44-1056">Ta bort alias för inaktuella cmdletar för inställningar för utvärdering av säkerhetsrisk</span><span class="sxs-lookup"><span data-stu-id="b6b44-1056">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="b6b44-1057">Inaktualisera cmdletar för inställningar för avancerad hotidentifiering</span><span class="sxs-lookup"><span data-stu-id="b6b44-1057">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="b6b44-1058">Lägga till cmdletar för att inaktivera och aktivera känslighetsrekommendationer på kolumner i en databas.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1058">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b6b44-1059">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b6b44-1059">Az.Storage</span></span>
* <span data-ttu-id="b6b44-1060">Stöd för att aktivera stora filresurser vid skapande eller uppdatering av lagringskonto</span><span class="sxs-lookup"><span data-stu-id="b6b44-1060">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="b6b44-1061">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b6b44-1061">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="b6b44-1062">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b6b44-1062">Set-AzStorageAccount</span></span>
* <span data-ttu-id="b6b44-1063">När du stänger/hämtar en filreferens kan du hoppa över kontrollen av huruvida indatasökvägen är en filkatalog eller en fil för att undvika problem med objekt som har status DeletePending</span><span class="sxs-lookup"><span data-stu-id="b6b44-1063">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="b6b44-1064">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="b6b44-1064">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="b6b44-1065">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="b6b44-1065">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="b6b44-1066">2.8.0 – oktober 2019</span><span class="sxs-lookup"><span data-stu-id="b6b44-1066">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="b6b44-1067">Allmänt</span><span class="sxs-lookup"><span data-stu-id="b6b44-1067">General</span></span>
* <span data-ttu-id="b6b44-1068">AZ. HealthcareApis 1.0.0-version</span><span class="sxs-lookup"><span data-stu-id="b6b44-1068">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="b6b44-1069">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b6b44-1069">Az.Accounts</span></span>
* <span data-ttu-id="b6b44-1070">Uppdatera telemetri och URL-omskrivning för genererade moduler, korrigera Windows-enhetstester.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1070">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="b6b44-1071">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b6b44-1071">Az.ApiManagement</span></span>
* <span data-ttu-id="b6b44-1072">**Set-AzApiManagementApi** – Tillagt stöd för att uppdatera Api till ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="b6b44-1072">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="b6b44-1073">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="b6b44-1073">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="b6b44-1074">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b6b44-1074">Az.Automation</span></span>
* <span data-ttu-id="b6b44-1075">Åtgärdade cmdleten New-AzureAutomationSoftwareUpdateConfiguration för parametern för inställning av Linux-omstart.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1075">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="b6b44-1076">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="b6b44-1076">Az.Batch</span></span>
* <span data-ttu-id="b6b44-1077">**Get-AzBatchNodeAgentSku** är inaktuell och ersätts av **Get-AzBatchSupportImage** i version 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1077">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b6b44-1078">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b6b44-1078">Az.Compute</span></span>
* <span data-ttu-id="b6b44-1079">Lägg till parametrarna Priority, EvictionPolicy och MaxPrice till cmdletarna New-AzVM och New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b6b44-1079">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="b6b44-1080">Korrigera varningsmeddelande och hjälpdokument för cmdletarna Add-AzVMAdditionalUnattendContent och Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="b6b44-1080">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="b6b44-1081">Åtgärda – skipVmBackup-undantag för virtuella Linux-datorer med hanterade diskar för Set-AzVMDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1081">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="b6b44-1082">Åtgärda fel i uppdatera krypteringsinställningarna i set-AzVMDiskEncryptionExtension, scenario i två steg.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1082">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b6b44-1083">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b6b44-1083">Az.DataFactory</span></span>
* <span data-ttu-id="b6b44-1084">Lägga till CRUD-kommandon för ADF V2-dataflödet: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow och Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1084">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="b6b44-1085">Lägger till åtgärdskommandon för ADF V2-dataflödesfelsökningssession: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand och Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1085">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="b6b44-1086">Uppdatera ADF .Net SDK-versionen till 4.2.0</span><span class="sxs-lookup"><span data-stu-id="b6b44-1086">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b6b44-1087">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b6b44-1087">Az.DataLakeStore</span></span>
* <span data-ttu-id="b6b44-1088">Korrigera kontovalidering så att konton med ”-” kan skickas utan domän</span><span class="sxs-lookup"><span data-stu-id="b6b44-1088">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="b6b44-1089">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="b6b44-1089">Az.HealthcareApis</span></span>
* <span data-ttu-id="b6b44-1090">PowerShell-versionen har uppdaterats till 1.0.0</span><span class="sxs-lookup"><span data-stu-id="b6b44-1090">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="b6b44-1091">Uppdaterade SDK-versionen till 1.0.2</span><span class="sxs-lookup"><span data-stu-id="b6b44-1091">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="b6b44-1092">Uppdatera i tester för att referera till en ny SDK-version</span><span class="sxs-lookup"><span data-stu-id="b6b44-1092">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="b6b44-1093">Utdatastrukturen har uppdaterats från kapslad till förenklad.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1093">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="b6b44-1094">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="b6b44-1094">Az.IotHub</span></span>
* <span data-ttu-id="b6b44-1095">Lägg till ny routningskälla: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="b6b44-1095">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="b6b44-1096">Mindre felkorrigering: Get-AzIothub returnerar inte subscriptionId</span><span class="sxs-lookup"><span data-stu-id="b6b44-1096">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="b6b44-1097">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b6b44-1097">Az.Monitor</span></span>
* <span data-ttu-id="b6b44-1098">Nya åtgärdsgruppsmottagare har lagts till för åtgärdsgrupp   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="b6b44-1098">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="b6b44-1099">Använd vanligt aviseringsschema som är aktiverat för mottagarna.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1099">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="b6b44-1100">Detta gäller inte för SMS, push för Azure-app, ITSM och röstmottagare</span><span class="sxs-lookup"><span data-stu-id="b6b44-1100">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="b6b44-1101">Webhooks har nu stöd för Azure Active Directory-autentisering.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1101">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b6b44-1102">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b6b44-1102">Az.Network</span></span>
* <span data-ttu-id="b6b44-1103">Lägg till ny cmdlet Get-AzAvailableServiceAlias som kan anropas för att hämta de alias som kan användas för tjänstslutpunktsprinciper.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1103">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="b6b44-1104">Stöd för tillägg av trafikväljare har lagts till i gatewayanslutningar för virtuella nätverk</span><span class="sxs-lookup"><span data-stu-id="b6b44-1104">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="b6b44-1105">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="b6b44-1105">New cmdlets added:</span></span>
        - <span data-ttu-id="b6b44-1106">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="b6b44-1106">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="b6b44-1107">Cmdletar har uppdaterats med valfri parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="b6b44-1107">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="b6b44-1108">Lägg till stöd för ESP- och AH-protokoll i konfiguration av nätverkssäkerhetsregler</span><span class="sxs-lookup"><span data-stu-id="b6b44-1108">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="b6b44-1109">Uppdaterade cmdletar:</span><span class="sxs-lookup"><span data-stu-id="b6b44-1109">Updated cmdlets:</span></span>
        - <span data-ttu-id="b6b44-1110">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b6b44-1110">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="b6b44-1111">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b6b44-1111">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="b6b44-1112">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b6b44-1112">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="b6b44-1113">Förbättra hanteringen av undantag i Cortex-cmdletar</span><span class="sxs-lookup"><span data-stu-id="b6b44-1113">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="b6b44-1114">Nya generationer och SKU:er för VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="b6b44-1114">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="b6b44-1115">Introducera nya generationer för VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1115">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="b6b44-1116">Introducera nya SKU:er med högt dataflöde för VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1116">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="b6b44-1117">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="b6b44-1117">Az.RedisCache</span></span>
* <span data-ttu-id="b6b44-1118">Uppdaterad referensdokumentation för ”set-AzRedisCache” för att inkludera saknade värden för parametern ”size”</span><span class="sxs-lookup"><span data-stu-id="b6b44-1118">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="b6b44-1119">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b6b44-1119">Az.Sql</span></span>
* <span data-ttu-id="b6b44-1120">Lägg till stöd för inställningen Active Directory administratör på den hanterade instansen</span><span class="sxs-lookup"><span data-stu-id="b6b44-1120">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b6b44-1121">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b6b44-1121">Az.Storage</span></span>
* <span data-ttu-id="b6b44-1122">Uppdatera Lagringsklientbibliotek till 11.1.0</span><span class="sxs-lookup"><span data-stu-id="b6b44-1122">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="b6b44-1123">Lista containrar med hanteringsplans-API, kommer att listas med NextPageLink</span><span class="sxs-lookup"><span data-stu-id="b6b44-1123">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="b6b44-1124">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="b6b44-1124">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="b6b44-1125">Lista lagringskonton från prenumerationen, kommer att listas med NextPageLink</span><span class="sxs-lookup"><span data-stu-id="b6b44-1125">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="b6b44-1126">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b6b44-1126">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="b6b44-1127">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="b6b44-1127">Az.StorageSync</span></span>
* <span data-ttu-id="b6b44-1128">Åtgärda problemet 9810 i Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1128">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b6b44-1129">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b6b44-1129">Az.Websites</span></span>
* <span data-ttu-id="b6b44-1130">Set-AzWebApp – uppdatering av ASP för en app misslyckades</span><span class="sxs-lookup"><span data-stu-id="b6b44-1130">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="b6b44-1131">2.7.0 – september 2019</span><span class="sxs-lookup"><span data-stu-id="b6b44-1131">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="b6b44-1132">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b6b44-1132">Az.ApiManagement</span></span>
* <span data-ttu-id="b6b44-1133">Uppdatera ”-Format”-parameterbeskrivningen i ”Set-AzApiManagementPolicy”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="b6b44-1133">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="b6b44-1134">Referenser för den föråldrade cmdleten ”Update-AzApiManagementDeployment” har tagits bort från referensdokumentationen.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1134">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="b6b44-1135">Använd ”Set-AzApiManagement” i stället.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1135">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="b6b44-1136">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b6b44-1136">Az.Automation</span></span>
* <span data-ttu-id="b6b44-1137">Stavfel har korrigerats i exempel i referensdokumentationen för ”Register-AzAutomationDscNode”</span><span class="sxs-lookup"><span data-stu-id="b6b44-1137">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="b6b44-1138">Klargörande har lagts till om OS-begränsningar för Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="b6b44-1138">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="b6b44-1139">Null-referensundantag har korrigerats för -Wait-alternativet i Start-AzAutomationRunbook-cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1139">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b6b44-1140">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b6b44-1140">Az.Compute</span></span>
* <span data-ttu-id="b6b44-1141">Lägg till UploadSizeInBytes-parameter till New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="b6b44-1141">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="b6b44-1142">Lägg till Incremental-parameter till New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="b6b44-1142">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="b6b44-1143">Lägg till en funktion för virtuella datorer med låg prioritet:</span><span class="sxs-lookup"><span data-stu-id="b6b44-1143">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="b6b44-1144">MaxPrice-, EvictionPolicy- och Priority-parametrar har lagts till i New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1144">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="b6b44-1145">MaxPrice-parametern har lagts till i New-AzVmssConfig-, Update-AzVM- och Update-AzVmss-cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1145">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="b6b44-1146">Åtgärda problem med VM-referenser för Get-AzAvailabilitySet-cmdleten när alla tillgänglighetsuppsättningar i prenumerationen visas.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1146">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="b6b44-1147">Korrigera null-undantaget för Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1147">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="b6b44-1148">Korrigera VHD-metoden för sökning relativt till slut.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1148">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="b6b44-1149">Åtgärda UltraSSD-problem för New-AzVM och Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1149">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b6b44-1150">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b6b44-1150">Az.DataFactory</span></span>
* <span data-ttu-id="b6b44-1151">Lägger till 3 nya kommandon för ADF V2 – Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription och Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="b6b44-1151">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="b6b44-1152">ADF .Net SDK har uppdaterats till 4.1.3</span><span class="sxs-lookup"><span data-stu-id="b6b44-1152">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="b6b44-1153">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="b6b44-1153">Az.HDInsight</span></span>
* <span data-ttu-id="b6b44-1154">Anrop för icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="b6b44-1154">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="b6b44-1155">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="b6b44-1155">Az.IotHub</span></span>
* <span data-ttu-id="b6b44-1156">Lägg till stöd för att anropa redundans för en IotHub till den geo-länkade katastrofåterställningsregionen.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1156">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="b6b44-1157">Lägg till stöd för att hantera meddelandeberikning för en IotHub.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1157">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="b6b44-1158">Nya cmdlet:ar är:</span><span class="sxs-lookup"><span data-stu-id="b6b44-1158">New cmdlets are:</span></span>
    - <span data-ttu-id="b6b44-1159">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="b6b44-1159">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="b6b44-1160">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="b6b44-1160">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="b6b44-1161">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="b6b44-1161">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="b6b44-1162">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="b6b44-1162">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="b6b44-1163">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b6b44-1163">Az.Monitor</span></span>
* <span data-ttu-id="b6b44-1164">Pekar på den senaste Monitor SDK:n, dvs. 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="b6b44-1164">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="b6b44-1165">Lägger till bakåtkompatibla ändringar i Metrics-cmdletarna, dvs. enhetsuppräkningen stöder flera nya värden.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1165">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="b6b44-1166">Detta är skrivskyddade cmdletar, så det förekommer inga ändringar i inmatningen för cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1166">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="b6b44-1167">API-versionen för **ActionGroups**-begäranden är nu **2019-06-01**. Tidigare var den **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1167">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="b6b44-1168">Test av scenarier har uppdaterats för att anpassas till den här ändringen.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1168">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="b6b44-1169">Ett nytt obligatoriskt argument har lagts till för konstruktorerna för klasserna **EmailReceiver** och **WebhookReceiver** – ett booleskt värde med namnet **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1169">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="b6b44-1170">Värdet är för närvarande fast till **false** så att den här icke-bakåtkompatibla ändringen är dold från cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1170">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="b6b44-1171">**Obs!** Det här är en tillfällig ändring som måste verifieras av Alerts-teamet.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1171">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="b6b44-1172">Ordningen på argumenten för konstruktorn för klassen **Source** (relaterad till klassen **ScheduledQueryRuleSource**) har ändrats från den tidigare SDK:n.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1172">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="b6b44-1173">Den här ändringen krävde korrigering av två enhetstest: de kompilerades, men testerna skickades inte.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1173">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="b6b44-1174">Ordningen på argumenten för konstruktorn för klassen **AlertingAction** (relaterad till klassen **ScheduledQueryRuleSource**) har ändrats från den tidigare SDK:n.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1174">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="b6b44-1175">Den här ändringen krävde korrigering av två enhetstest: de kompilerades, men testerna skickades inte.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1175">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="b6b44-1176">Stöd för kriterier för dynamiskt tröskelvärde för måttavisering v2</span><span class="sxs-lookup"><span data-stu-id="b6b44-1176">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="b6b44-1177">New-AzMetricAlertRuleV2Criteria: skapar nu även kriterier för dynamiskt tröskelvärde</span><span class="sxs-lookup"><span data-stu-id="b6b44-1177">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="b6b44-1178">Add-AzMetricAlertRuleV2: accepterar nu även kriterier för dynamiskt tröskelvärde</span><span class="sxs-lookup"><span data-stu-id="b6b44-1178">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="b6b44-1179">Förbättringar i schemalagd frågeregel (SQR)</span><span class="sxs-lookup"><span data-stu-id="b6b44-1179">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="b6b44-1180">Cmdletar accepterar ”Location”-parameter i båda formaten, antingen platsen (t.ex. eastus) eller platsens visningsnamn (t.ex. USA, östra)</span><span class="sxs-lookup"><span data-stu-id="b6b44-1180">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="b6b44-1181">”Enabled”-parametern illustreras korrekt i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="b6b44-1181">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="b6b44-1182">Exempel för den valfria parametern ”ActionGroup” har lagts till</span><span class="sxs-lookup"><span data-stu-id="b6b44-1182">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="b6b44-1183">Förbättrade hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="b6b44-1183">Overall improved help files</span></span>
* <span data-ttu-id="b6b44-1184">Åtgärda bugg då omfattningstypen fastställs för ”Set-AzActionRule”</span><span class="sxs-lookup"><span data-stu-id="b6b44-1184">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b6b44-1185">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b6b44-1185">Az.Network</span></span>
* <span data-ttu-id="b6b44-1186">Korrigera felaktigt exempel i referensdokumentationen för ”New-AzApplicationGateway”</span><span class="sxs-lookup"><span data-stu-id="b6b44-1186">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="b6b44-1187">Lägg till anmärkning i ”Get-AzNetworkWatcherPacketCapture”-referensdokumentationen om hämtning av alla egenskaper för en paketinsamling</span><span class="sxs-lookup"><span data-stu-id="b6b44-1187">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="b6b44-1188">Exempel har korrigerats i ”Test-AzNetworkWatcherIPFlow”-referensdokumentationen för korrekt uppräkning av nätverkskort</span><span class="sxs-lookup"><span data-stu-id="b6b44-1188">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="b6b44-1189">Förbättrad tolkning av molnundantag för att visa eventuell ytterligare information</span><span class="sxs-lookup"><span data-stu-id="b6b44-1189">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="b6b44-1190">Förbättrad tolkning av molnundantag för att hantera ytterligare en typ av SDK-undantag</span><span class="sxs-lookup"><span data-stu-id="b6b44-1190">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="b6b44-1191">Felaktig mappning av säkerhetsregelmodeller har korrigerats</span><span class="sxs-lookup"><span data-stu-id="b6b44-1191">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="b6b44-1192">Egenskaper har lagts till för nätverksgränssnittet för funktionen Privat IP</span><span class="sxs-lookup"><span data-stu-id="b6b44-1192">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="b6b44-1193">Egenskapen ”PrivateEndpoint” har lagts till som en typ av PSResourceId till PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="b6b44-1193">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="b6b44-1194">Egenskapen ”PrivateLinkConnectionProperties” har lagts till som en typ av PSIpConfigurationConnectivityInformation till PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b6b44-1194">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="b6b44-1195">Modellklassen PSIpConfigurationConnectivityInformation har lagts till</span><span class="sxs-lookup"><span data-stu-id="b6b44-1195">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="b6b44-1196">ApplicationRuleProtocolType ”mssql” har lagts till för Azure Firewall-resurs</span><span class="sxs-lookup"><span data-stu-id="b6b44-1196">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="b6b44-1197">MultiLink-stöd i virtuellt WAN</span><span class="sxs-lookup"><span data-stu-id="b6b44-1197">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="b6b44-1198">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="b6b44-1198">New cmdlets</span></span>
        - <span data-ttu-id="b6b44-1199">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="b6b44-1199">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="b6b44-1200">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="b6b44-1200">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="b6b44-1201">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="b6b44-1201">Updated cmdlet:</span></span>
        - <span data-ttu-id="b6b44-1202">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="b6b44-1202">New-VpnSite</span></span>
        - <span data-ttu-id="b6b44-1203">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="b6b44-1203">Update-VpnSite</span></span>
        - <span data-ttu-id="b6b44-1204">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="b6b44-1204">New-VpnConnection</span></span>
        - <span data-ttu-id="b6b44-1205">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="b6b44-1205">Update-VpnConnection</span></span>
* <span data-ttu-id="b6b44-1206">Dokument för vissa PowerShell-exempel har korrigerats så att Az-cmdletar används i stället för AzureRM-cmdletar</span><span class="sxs-lookup"><span data-stu-id="b6b44-1206">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b6b44-1207">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b6b44-1207">Az.RecoveryServices</span></span>
* <span data-ttu-id="b6b44-1208">Uppdatera AzureVMpolicy-objekt med ProtectedItemsCount-attribut</span><span class="sxs-lookup"><span data-stu-id="b6b44-1208">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="b6b44-1209">Ytterligare tester har lagts till för VM-princip och återställning av ursprungligt lagringskonto</span><span class="sxs-lookup"><span data-stu-id="b6b44-1209">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="b6b44-1210">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b6b44-1210">Az.Resources</span></span>
* <span data-ttu-id="b6b44-1211">Åtgärda fel där det inte gick att anropa New-AzRoleAssignment utan parametern Scope.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1211">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="b6b44-1212">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b6b44-1212">Az.ServiceFabric</span></span>
* <span data-ttu-id="b6b44-1213">Stavfel har korrigerats i exempel för ”Update-AzServiceFabricReliability”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="b6b44-1213">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="b6b44-1214">Lägger till nya cmdletar för att hantera program och tjänster:</span><span class="sxs-lookup"><span data-stu-id="b6b44-1214">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="b6b44-1215">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="b6b44-1215">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="b6b44-1216">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="b6b44-1216">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="b6b44-1217">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="b6b44-1217">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="b6b44-1218">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="b6b44-1218">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="b6b44-1219">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="b6b44-1219">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="b6b44-1220">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="b6b44-1220">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="b6b44-1221">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="b6b44-1221">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="b6b44-1222">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="b6b44-1222">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="b6b44-1223">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="b6b44-1223">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="b6b44-1224">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="b6b44-1224">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="b6b44-1225">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="b6b44-1225">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="b6b44-1226">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="b6b44-1226">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="b6b44-1227">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="b6b44-1227">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="b6b44-1228">Service Fabric SDK har uppgraderats till version 1.2.0 som använder Service Fabric-resursprovidern med API-version 2019-03-01.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1228">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="b6b44-1229">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="b6b44-1229">Az.SignalR</span></span>
* <span data-ttu-id="b6b44-1230">Lägg till Update-, Restart-, CheckNameAvailability- och GetUsage-cmdletar</span><span class="sxs-lookup"><span data-stu-id="b6b44-1230">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="b6b44-1231">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b6b44-1231">Az.Sql</span></span>
* <span data-ttu-id="b6b44-1232">Uppdatera exempel i referensdokumentationen för ”Get-AzSqlElasticPool”</span><span class="sxs-lookup"><span data-stu-id="b6b44-1232">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="b6b44-1233">vCore-exempel för att skapa en elastisk pool (New-AzSqlElasticPool) har lagts till.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1233">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="b6b44-1234">Ta bort verifieringen av EmailAddresses och kontrollen som bekräftar att EmailAdmins inte är falskt när EmailAddresses är tomt i Set-AzSqlServerAdvancedThreatProtectionPolicy och Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b6b44-1234">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="b6b44-1235">Server-/databasgranskningsinställningar kan tas bort när det finns flera diagnostikinställningar som aktiverar granskningskategorin.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1235">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="b6b44-1236">Åtgärda verifiering av e-postadresser i flera Sql Vulnerability Assessment-cmdletar (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting och Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="b6b44-1236">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b6b44-1237">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b6b44-1237">Az.Storage</span></span>
* <span data-ttu-id="b6b44-1238">Exempel i referensdokumentationen för ”Get-AzStorageAccountKey” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="b6b44-1238">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="b6b44-1239">Vid upp- och nedladdning av en Azure-fil kan SMB-egenskaperna för källfilen (t.ex. filattribut, tidpunkten då filen skapades och tidpunkten för den senaste skrivningen) sparas i målfilen</span><span class="sxs-lookup"><span data-stu-id="b6b44-1239">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="b6b44-1240">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="b6b44-1240">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="b6b44-1241">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="b6b44-1241">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="b6b44-1242">Korrigera problem med uppladdningen av blockblob med egenskaper/metadata för ImmutabilityPolicy i containrar.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1242">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="b6b44-1243">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="b6b44-1243">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="b6b44-1244">Stöd för hantering av Azure-filresurser med API för hanteringsplan</span><span class="sxs-lookup"><span data-stu-id="b6b44-1244">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="b6b44-1245">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="b6b44-1245">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="b6b44-1246">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="b6b44-1246">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="b6b44-1247">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="b6b44-1247">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="b6b44-1248">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="b6b44-1248">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b6b44-1249">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b6b44-1249">Az.Websites</span></span>
* <span data-ttu-id="b6b44-1250">Åtgärdar problemet där webapp-taggar togs bort när appen migrerades till nya ASP</span><span class="sxs-lookup"><span data-stu-id="b6b44-1250">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="b6b44-1251">Åtgärda Publish-AzureWebapp så att det fungerar i Linux och Windows</span><span class="sxs-lookup"><span data-stu-id="b6b44-1251">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="b6b44-1252">Uppdatera exempel i ”Get-AzWebAppPublishingProfile”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="b6b44-1252">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="b6b44-1253">2.6.0 – augusti 2019</span><span class="sxs-lookup"><span data-stu-id="b6b44-1253">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="b6b44-1254">Allmänt</span><span class="sxs-lookup"><span data-stu-id="b6b44-1254">General</span></span>
* <span data-ttu-id="b6b44-1255">Åtgärdade diverse skrivfel i flera moduler</span><span class="sxs-lookup"><span data-stu-id="b6b44-1255">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="b6b44-1256">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b6b44-1256">Az.Accounts</span></span>
* <span data-ttu-id="b6b44-1257">Stöd för användartilldelat MSI i Azure Functions-autentisering (#9479)</span><span class="sxs-lookup"><span data-stu-id="b6b44-1257">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="b6b44-1258">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="b6b44-1258">Az.Aks</span></span>
* <span data-ttu-id="b6b44-1259">Åtgärda problem med utdata för "Get-AzAks"</span><span class="sxs-lookup"><span data-stu-id="b6b44-1259">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="b6b44-1260">Mer information här: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="b6b44-1260">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="b6b44-1261">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b6b44-1261">Az.ApiManagement</span></span>
* <span data-ttu-id="b6b44-1262">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="b6b44-1262">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="b6b44-1263">Uppdatera .net-NuGet-versionen, som inte tillämpar begränsningar för productId, apiId och userId</span><span class="sxs-lookup"><span data-stu-id="b6b44-1263">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="b6b44-1264">**Get-AzApiManagementProduct** – Lade till stöd för frågekörning mot produkter via API.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1264">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="b6b44-1265">**New-AzApiManagementApiRevision** – Korrigering för problem där ApiRevisionDescription inte angavs vid skapande av ny API-revision https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="b6b44-1265">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="b6b44-1266">Åtgärdade skrivfel i modellen "PsApiManagementOAuth2AuthrozationServer" till "PsApiManagementOAuth2AuthorizationServer"</span><span class="sxs-lookup"><span data-stu-id="b6b44-1266">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="b6b44-1267">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="b6b44-1267">Az.Batch</span></span>
* <span data-ttu-id="b6b44-1268">Åtgärdade skrivfel i hjälpmeddelande och dokumentation till att skriva Windows med versaler</span><span class="sxs-lookup"><span data-stu-id="b6b44-1268">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="b6b44-1269">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="b6b44-1269">Az.Cdn</span></span>
* <span data-ttu-id="b6b44-1270">Åtgärdade skrivfel i CDN-modulens konverteringshjälp</span><span class="sxs-lookup"><span data-stu-id="b6b44-1270">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b6b44-1271">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b6b44-1271">Az.Compute</span></span>
* <span data-ttu-id="b6b44-1272">Lägg till VmssId i New-AzVMConfig-cmdleten</span><span class="sxs-lookup"><span data-stu-id="b6b44-1272">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="b6b44-1273">Lägg till parametrarna TerminateScheduledEvents och TerminateScheduledEventNotBeforeTimeoutInMinutes i New-AzVmssConfig och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b6b44-1273">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="b6b44-1274">Lägg till egenskapen HyperVGeneration till avbildningsobjekt för virtuell dator</span><span class="sxs-lookup"><span data-stu-id="b6b44-1274">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="b6b44-1275">Lägg till funktioner för Host och HostGroup</span><span class="sxs-lookup"><span data-stu-id="b6b44-1275">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="b6b44-1276">Nya cmdletar:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="b6b44-1276">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="b6b44-1277">HostId-parametern läggs till i New-AzVMConfig och New-AzVM</span><span class="sxs-lookup"><span data-stu-id="b6b44-1277">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="b6b44-1278">Uppdatera exempel i "Invoke-AzVMRunCommand"-dokumentationen till att använda rätt parameternamn</span><span class="sxs-lookup"><span data-stu-id="b6b44-1278">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="b6b44-1279">Uppdatera "-VolumeType"-beskrivningen i referensdokumentationen för "set-AzVMDiskEncryptionExtension" och "set-AzVmssDiskEncryptionExtension"</span><span class="sxs-lookup"><span data-stu-id="b6b44-1279">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b6b44-1280">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b6b44-1280">Az.DataFactory</span></span>
* <span data-ttu-id="b6b44-1281">Åtgärda skrivfel till att använda versaler för "Windows" i "New-AzDataFactoryEncryptValue"-dokumentationen</span><span class="sxs-lookup"><span data-stu-id="b6b44-1281">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="b6b44-1282">Uppdaterade ADF .Net SDK-versionen till 4.1.2</span><span class="sxs-lookup"><span data-stu-id="b6b44-1282">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="b6b44-1283">Lägg till parametrarna "DataProxyIntegrationRuntimeName", "DataProxyStagingLinkedServiceName" och "DataProxyStagingPath" för "Set-AzureRmDataFactoryV2IntegrationRuntime"-cmd för att aktivera konfiguration av lokalt installerad integrationskörning som en proxy för SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="b6b44-1283">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="b6b44-1284">Uppdaterade PSTriggerRun till att visa utlöst pipeline, meddelande och egenskaper samt PSActivityRun till att visa aktivitetstypen</span><span class="sxs-lookup"><span data-stu-id="b6b44-1284">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b6b44-1285">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b6b44-1285">Az.DataLakeStore</span></span>
* <span data-ttu-id="b6b44-1286">Korrigering av frysning av Get-DataLakeStoreDeletedItem för fel eller fjärrundantag.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1286">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="b6b44-1287">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="b6b44-1287">Az.EventHub</span></span>
* <span data-ttu-id="b6b44-1288">Korrigering av problem #9658 : Skrivfel i parametern VirtualNteworkRule i Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="b6b44-1288">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="b6b44-1289">Korrigering av problem #9558 : Set-AzEventHubNamespace använder PATCH i stället för PUT</span><span class="sxs-lookup"><span data-stu-id="b6b44-1289">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="b6b44-1290">lade till parametern EnableKafka i Set-AzEventHubNamespace-cmdleten</span><span class="sxs-lookup"><span data-stu-id="b6b44-1290">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="b6b44-1291">Korrigering av problem #9786 : kan inte skapa en regel med Endast lyssna-behörighet</span><span class="sxs-lookup"><span data-stu-id="b6b44-1291">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="b6b44-1292">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="b6b44-1292">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="b6b44-1293">Åtgärdade skrivfel i dokumentation där "Azure" skrevs helt med gemener</span><span class="sxs-lookup"><span data-stu-id="b6b44-1293">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="b6b44-1294">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b6b44-1294">Az.Monitor</span></span>
* <span data-ttu-id="b6b44-1295">Åtgärdade felaktigt parameternamn i hjälpdokumentationen</span><span class="sxs-lookup"><span data-stu-id="b6b44-1295">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b6b44-1296">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b6b44-1296">Az.Network</span></span>
* <span data-ttu-id="b6b44-1297">Uppdaterade New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="b6b44-1297">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="b6b44-1298">Gjorde parametern "PublicIpAddress" inaktuell eftersom den aldrig används på serversidan.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1298">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="b6b44-1299">Lade till den valfria parametern "Primary", som anger huruvida den aktuella IP-konfigurationen är den primära.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1299">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="b6b44-1300">Förbättrade hanteringen av felundantag för begärande från SDK – åtgärdar problemet att tidigare SDK-undantag inte hanteras på rätt sätt, vilket leder till att viktig felinformation inte visas</span><span class="sxs-lookup"><span data-stu-id="b6b44-1300">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="b6b44-1301">Justerade valideringslogiken för IPv6-IP-prefix till att kontrollera korrekt IPv6-prefixlängd.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1301">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="b6b44-1302">Uppdaterade Get-AzVirtualNetworkSubnetConfig: Lade till parameter som anges till get av undernätets resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1302">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="b6b44-1303">Uppdaterade beskrivningen av parametern Location för AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="b6b44-1303">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="b6b44-1304">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="b6b44-1304">Az.OperationalInsights</span></span>
* <span data-ttu-id="b6b44-1305">Uppdaterade dokumentation för "New-AzOperationalInsightsLinuxSyslogDataSource"</span><span class="sxs-lookup"><span data-stu-id="b6b44-1305">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="b6b44-1306">Lade till exempel</span><span class="sxs-lookup"><span data-stu-id="b6b44-1306">Added example</span></span>
    - <span data-ttu-id="b6b44-1307">Uppdaterade beskrivningen av parametern "-Name"</span><span class="sxs-lookup"><span data-stu-id="b6b44-1307">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="b6b44-1308">Lade till ett exempel för New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="b6b44-1308">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="b6b44-1309">Ändrade beskrivningen av parametern -Name för New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="b6b44-1309">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b6b44-1310">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b6b44-1310">Az.RecoveryServices</span></span>
* <span data-ttu-id="b6b44-1311">Uppdatera "Get-AzRecoveryServicesBackupJobDetail.md"</span><span class="sxs-lookup"><span data-stu-id="b6b44-1311">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="b6b44-1312">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b6b44-1312">Az.Resources</span></span>
* <span data-ttu-id="b6b44-1313">Lägg till stöd för den nya API-versionen från 2019-05-10 för Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="b6b44-1313">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="b6b44-1314">Lägg till stöd för "copy.count = 0" för variabler, resurser och egenskaper</span><span class="sxs-lookup"><span data-stu-id="b6b44-1314">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="b6b44-1315">Resurser med "condition = false" eller "copy.count = 0" tas bort i complete-läget</span><span class="sxs-lookup"><span data-stu-id="b6b44-1315">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="b6b44-1316">Lägg till ett exempel på tilldelning av princip på prenumerationsnivå i hjälpdokumentationen</span><span class="sxs-lookup"><span data-stu-id="b6b44-1316">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="b6b44-1317">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="b6b44-1317">Az.ServiceBus</span></span>
* <span data-ttu-id="b6b44-1318">Korrigering av problem #9658 : Skrivfel i parametern VirtualNetworkRule i set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="b6b44-1318">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="b6b44-1319">Korrigering av problem #9786 : kan inte skapa en regel med Endast lyssna-behörighet</span><span class="sxs-lookup"><span data-stu-id="b6b44-1319">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="b6b44-1320">Lade till det nya kommandot "Test-AzServiceBusNameAvailability" för att kontrollera namntillgängligheten för kö och ämne</span><span class="sxs-lookup"><span data-stu-id="b6b44-1320">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="b6b44-1321">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b6b44-1321">Az.ServiceFabric</span></span>
* <span data-ttu-id="b6b44-1322">Åtgärda buggar med tillägg av nodtyps-cmdlet:</span><span class="sxs-lookup"><span data-stu-id="b6b44-1322">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="b6b44-1323">NullReferenceException-bugg när resursgrupp hade annan vmss som inte är relaterad till Service Fabric-klustret.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1323">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="b6b44-1324">Åtgärdar problemet: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="b6b44-1324">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="b6b44-1325">Åtgärda bugg där cmdleten misslyckades om virtualNetwork var i en annan resursgrupp än klustret.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1325">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="b6b44-1326">Åtgärdar problemet: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="b6b44-1326">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="b6b44-1327">AzServiceFabricApplicationCertificate-cmdleten görs inaktuell</span><span class="sxs-lookup"><span data-stu-id="b6b44-1327">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="b6b44-1328">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b6b44-1328">Az.Sql</span></span>
* <span data-ttu-id="b6b44-1329">Uppdatera dokumentation om gamla gransknings-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1329">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b6b44-1330">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b6b44-1330">Az.Storage</span></span>
* <span data-ttu-id="b6b44-1331">Uppdatera hjälpen för Get/Close-AzStorageFileHandle genom att lägga till fler scenarier i cmdlet-exempel och uppdatera parameterbeskrivningar</span><span class="sxs-lookup"><span data-stu-id="b6b44-1331">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="b6b44-1332">Stöd för StandardBlobTier i uppladdningsblob och kopieringsblob</span><span class="sxs-lookup"><span data-stu-id="b6b44-1332">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="b6b44-1333">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="b6b44-1333">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="b6b44-1334">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="b6b44-1334">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="b6b44-1335">Stöd för rehydratiseringsprioritet i kopieringsblob</span><span class="sxs-lookup"><span data-stu-id="b6b44-1335">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="b6b44-1336">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="b6b44-1336">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b6b44-1337">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b6b44-1337">Az.Websites</span></span>
* <span data-ttu-id="b6b44-1338">Lägg till klargöranden gällande parametern -AppSettings i Set-AzWebApp och Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b6b44-1338">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="b6b44-1339">2.5.0 – July 2019</span><span class="sxs-lookup"><span data-stu-id="b6b44-1339">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b6b44-1340">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b6b44-1340">Az.Accounts</span></span>
* <span data-ttu-id="b6b44-1341">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="b6b44-1341">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="b6b44-1342">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="b6b44-1342">Az.ApplicationInsights</span></span>
* <span data-ttu-id="b6b44-1343">Korrigera skrivfel i exempel i dokumentationen för Remove-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="b6b44-1343">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="b6b44-1344">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b6b44-1344">Az.Automation</span></span>
* <span data-ttu-id="b6b44-1345">Korrigera skrivfel i resurssträng</span><span class="sxs-lookup"><span data-stu-id="b6b44-1345">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="b6b44-1346">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="b6b44-1346">Az.CognitiveServices</span></span>
* <span data-ttu-id="b6b44-1347">Stöd för NetworkRuleSet har lagts till.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1347">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b6b44-1348">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b6b44-1348">Az.Compute</span></span>
* <span data-ttu-id="b6b44-1349">Lägg till saknade egenskaper (ComputerName, OsName, OsVersion och HyperVGeneration) för visningsobjekt i den virtuella datorinstansen.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1349">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="b6b44-1350">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="b6b44-1350">Az.ContainerRegistry</span></span>
* <span data-ttu-id="b6b44-1351">Åtgärda skrivfel i Remove-AzContainerRegistryReplication för parametern Replication</span><span class="sxs-lookup"><span data-stu-id="b6b44-1351">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="b6b44-1352">Mer information finns här: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="b6b44-1352">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b6b44-1353">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b6b44-1353">Az.DataFactory</span></span>
* <span data-ttu-id="b6b44-1354">ADF .Net SDK-versionen har uppdaterats till 4.1.0</span><span class="sxs-lookup"><span data-stu-id="b6b44-1354">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="b6b44-1355">Korrigera skrivfel i dokumentationen för Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="b6b44-1355">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="b6b44-1356">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="b6b44-1356">Az.EventHub</span></span>
* <span data-ttu-id="b6b44-1357">Ny cmmdlet har lagts till för att skapa SAS-token: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="b6b44-1357">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="b6b44-1358">verifierings- och felmeddelande har lagts till för authorizationrules-rättigheter om endast "hantera" har tilldelats</span><span class="sxs-lookup"><span data-stu-id="b6b44-1358">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="b6b44-1359">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b6b44-1359">Az.KeyVault</span></span>
* <span data-ttu-id="b6b44-1360">Stöd har lagts till för att ange KeySize för certifikatprinciper</span><span class="sxs-lookup"><span data-stu-id="b6b44-1360">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="b6b44-1361">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="b6b44-1361">Az.LogicApp</span></span>
* <span data-ttu-id="b6b44-1362">Korrigering för Get-AzIntegrationAccountMap för att lista alla mappningstyper</span><span class="sxs-lookup"><span data-stu-id="b6b44-1362">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="b6b44-1363">Ny MapType-parameter har lagts till för filtrering</span><span class="sxs-lookup"><span data-stu-id="b6b44-1363">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="b6b44-1364">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="b6b44-1364">Az.ManagedServices</span></span>
* <span data-ttu-id="b6b44-1365">Stöd för API-versionen 2019-06-01 (GA) har lagts till</span><span class="sxs-lookup"><span data-stu-id="b6b44-1365">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b6b44-1366">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b6b44-1366">Az.Network</span></span>
* <span data-ttu-id="b6b44-1367">Lägg till stöd för privat slutpunkt och privat länktjänst</span><span class="sxs-lookup"><span data-stu-id="b6b44-1367">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="b6b44-1368">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="b6b44-1368">New cmdlets</span></span>
        - <span data-ttu-id="b6b44-1369">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="b6b44-1369">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="b6b44-1370">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="b6b44-1370">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="b6b44-1371">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="b6b44-1371">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="b6b44-1372">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="b6b44-1372">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="b6b44-1373">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="b6b44-1373">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="b6b44-1374">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="b6b44-1374">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="b6b44-1375">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="b6b44-1375">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="b6b44-1376">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="b6b44-1376">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="b6b44-1377">Nedanstående kommandon för funktionen har uppdaterats: Flaggan PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies på undernätet i VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b6b44-1377">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="b6b44-1378">Uppdaterade New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="b6b44-1378">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="b6b44-1379">Valfri parameter har lagts till – PrivateEndpointNetworkPoliciesFlag som konfigurerar huruvida nätverksprinciper ska tillämpas på en privat slutpunkt i det här undernätet.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1379">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="b6b44-1380">Valfri parameter har lagts till – PrivateLinkServiceNetworkPoliciesFlag som konfigurerar huruvida nätverksprinciper ska tillämpas på en privat länktjänst i det här undernätet.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1380">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="b6b44-1381">AzPrivateLinkService för cmdlet-parametern ServiceName har bytt namn till Name med aliaset ServiceName för bakåtkompatibilitet</span><span class="sxs-lookup"><span data-stu-id="b6b44-1381">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="b6b44-1382">Aktivera ICMP-protokoll för konfiguration av nätverkssäkerhetsregler</span><span class="sxs-lookup"><span data-stu-id="b6b44-1382">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="b6b44-1383">Uppdaterade cmdletar</span><span class="sxs-lookup"><span data-stu-id="b6b44-1383">Updated cmdlets</span></span>
        - <span data-ttu-id="b6b44-1384">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b6b44-1384">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="b6b44-1385">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b6b44-1385">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="b6b44-1386">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b6b44-1386">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="b6b44-1387">Lägg till ConnectionProtocolType (Ikev1/Ikev2) som en konfigurerbar parameter för New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="b6b44-1387">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="b6b44-1388">Lägg till PrivateIpAddressVersion i LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="b6b44-1388">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="b6b44-1389">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="b6b44-1389">Updated cmdlet:</span></span>
        - <span data-ttu-id="b6b44-1390">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b6b44-1390">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="b6b44-1391">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b6b44-1391">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="b6b44-1392">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b6b44-1392">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="b6b44-1393">Uppdatering av Application Gateway-kommandot New-AzApplicationGatewayProbeConfig för stöd av anpassad port i Probe</span><span class="sxs-lookup"><span data-stu-id="b6b44-1393">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="b6b44-1394">Uppdaterade New-AzApplicationGatewayProbeConfig: Den valfria parametern Port som används för avsökning i serverdelen har lagts till.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1394">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="b6b44-1395">Denna parameter gäller för SKU:erna Standard_V2 och WAF_V2.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1395">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="b6b44-1396">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="b6b44-1396">Az.OperationalInsights</span></span>
* <span data-ttu-id="b6b44-1397">Uppdaterade standardversionen för sparade sökningar till 1.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1397">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="b6b44-1398">Åtgärdade hantering av anpassad log null regex</span><span class="sxs-lookup"><span data-stu-id="b6b44-1398">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b6b44-1399">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b6b44-1399">Az.RecoveryServices</span></span>
* <span data-ttu-id="b6b44-1400">Uppdatera Get-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="b6b44-1400">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="b6b44-1401">Uppdatera Get-AzRecoveryServicesBackupContainer.md</span><span class="sxs-lookup"><span data-stu-id="b6b44-1401">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="b6b44-1402">Uppdatera Get-AzRecoveryServicesVault.md</span><span class="sxs-lookup"><span data-stu-id="b6b44-1402">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="b6b44-1403">Uppdatera Wait-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="b6b44-1403">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="b6b44-1404">Uppdatera Set-AzRecoveryServicesVaultContext.md</span><span class="sxs-lookup"><span data-stu-id="b6b44-1404">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="b6b44-1405">Uppdatera Get-AzRecoveryServicesBackupItem.md</span><span class="sxs-lookup"><span data-stu-id="b6b44-1405">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="b6b44-1406">Uppdatera Get-AzRecoveryServicesBackupRecoveryPoint.md</span><span class="sxs-lookup"><span data-stu-id="b6b44-1406">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="b6b44-1407">Uppdatera Restore-AzRecoveryServicesBackupItem.md</span><span class="sxs-lookup"><span data-stu-id="b6b44-1407">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="b6b44-1408">Uppdaterat tjänstanrop för avregistrering av container för Azure-filresurs</span><span class="sxs-lookup"><span data-stu-id="b6b44-1408">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="b6b44-1409">Uppdatera Set-AzRecoveryServicesAsrAlertSetting.md</span><span class="sxs-lookup"><span data-stu-id="b6b44-1409">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="b6b44-1410">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b6b44-1410">Az.Resources</span></span>
- <span data-ttu-id="b6b44-1411">Ta bort den cmdlet som saknas och som refereras i dokumentationen till New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b6b44-1411">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="b6b44-1412">Princip-cmdletar har uppdaterats så att de använder den nya API-versionen 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="b6b44-1412">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="b6b44-1413">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="b6b44-1413">Az.ServiceBus</span></span>
* <span data-ttu-id="b6b44-1414">Ny cmmdlet har lagts till för att skapa SAS-token: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="b6b44-1414">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="b6b44-1415">verifierings- och felmeddelande har lagts till för authorizationrules-rättigheter om endast "hantera" har tilldelats</span><span class="sxs-lookup"><span data-stu-id="b6b44-1415">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="b6b44-1416">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b6b44-1416">Az.Sql</span></span>
* <span data-ttu-id="b6b44-1417">Åtgärda saknade exempel för Set-AzSqlDatabaseSecondary cmdlet</span><span class="sxs-lookup"><span data-stu-id="b6b44-1417">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="b6b44-1418">Åtgärda angivna återkommande genomsökningar för bedömning av säkerhetsrisk utan angivna e-postadresser</span><span class="sxs-lookup"><span data-stu-id="b6b44-1418">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="b6b44-1419">Korrigera ett skrivfel i ett varningsmeddelande.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1419">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b6b44-1420">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b6b44-1420">Az.Storage</span></span>
* <span data-ttu-id="b6b44-1421">Uppdatera exempel i referensdokumentationen för Get-AzStorageAccount så att rätt parameternamn används</span><span class="sxs-lookup"><span data-stu-id="b6b44-1421">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="b6b44-1422">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="b6b44-1422">Az.StorageSync</span></span>
* <span data-ttu-id="b6b44-1423">Lägger till cmdleten Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1423">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="b6b44-1424">Åtgärda problem 9551 så att TierFilesOlderThanDays föredras</span><span class="sxs-lookup"><span data-stu-id="b6b44-1424">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b6b44-1425">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b6b44-1425">Az.Websites</span></span>
* <span data-ttu-id="b6b44-1426">Åtgärdar ett fel där vissa SiteConfig-egenskaper inte returnerades av Get-AzWebApp och Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="b6b44-1426">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="b6b44-1427">Lägger till en ny platsparameter för Get-AzDeletedWebApp och Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="b6b44-1427">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="b6b44-1428">Åtgärdar ett fel i kloning av webbapp-platser som använder New-AzWebApp-IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="b6b44-1428">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="b6b44-1429">2.4.0 – juli 2019</span><span class="sxs-lookup"><span data-stu-id="b6b44-1429">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b6b44-1430">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b6b44-1430">Az.Accounts</span></span>
* <span data-ttu-id="b6b44-1431">Lägg till stöd för profil-cmdletar</span><span class="sxs-lookup"><span data-stu-id="b6b44-1431">Add support for profile cmdlets</span></span>
* <span data-ttu-id="b6b44-1432">Lägg till stöd för miljöer och dataplaner i genererade cmdletar</span><span class="sxs-lookup"><span data-stu-id="b6b44-1432">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="b6b44-1433">Åtgärda bugg där fel slutpunkt i vissa fall användes för cmdletar för dataplaner i Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="b6b44-1433">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="b6b44-1434">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="b6b44-1434">Az.Advisor</span></span>
* <span data-ttu-id="b6b44-1435">GA-version av Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="b6b44-1435">GA release of Az.Advisor</span></span>
* <span data-ttu-id="b6b44-1436">Den här modulen ingår nu som en del av `Az`-sammanslagningsmodulen</span><span class="sxs-lookup"><span data-stu-id="b6b44-1436">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="b6b44-1437">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b6b44-1437">Az.ApiManagement</span></span>
* <span data-ttu-id="b6b44-1438">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="b6b44-1438">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="b6b44-1439">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="b6b44-1439">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="b6b44-1440">Stöd för att fråga prenumerationer efter användare och produkt har lagts till</span><span class="sxs-lookup"><span data-stu-id="b6b44-1440">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="b6b44-1441">Stöd för att fråga med hjälp av omfång ”/”, ”/apis”, ”/apis/echo-api” har lagts till</span><span class="sxs-lookup"><span data-stu-id="b6b44-1441">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="b6b44-1442">Korrigering av problem https://github.com/Azure/azure-powershell/issues/9307 och https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="b6b44-1442">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="b6b44-1443">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="b6b44-1443">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="b6b44-1444">Stöd för att ange ”ApiVersion” och ”ApiVersionSetId” när API:er importeras har lagts till</span><span class="sxs-lookup"><span data-stu-id="b6b44-1444">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="b6b44-1445">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b6b44-1445">Az.Automation</span></span>
* <span data-ttu-id="b6b44-1446">Bugg med cmdleten Set-AzAutomationConnectionFieldValue för att hantera strängvärde har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1446">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b6b44-1447">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b6b44-1447">Az.Compute</span></span>
* <span data-ttu-id="b6b44-1448">Lägg till parametern HyperVGeneration i New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="b6b44-1448">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b6b44-1449">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b6b44-1449">Az.DataFactory</span></span>
* <span data-ttu-id="b6b44-1450">Uppdaterar utdata från ADF-cmdletar som hämtar aktivitetskörningar, hämtar pipelinekörningar och hämtar utlösarkörningar för stöd för Select-Object-pipe.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1450">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="b6b44-1451">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="b6b44-1451">Az.EventGrid</span></span>
* <span data-ttu-id="b6b44-1452">Korrigera stavfel i dokumentation om ”New-AzEventGridSubscription”</span><span class="sxs-lookup"><span data-stu-id="b6b44-1452">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="b6b44-1453">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="b6b44-1453">Az.IotHub</span></span>
* <span data-ttu-id="b6b44-1454">Lägg till stöd för att återskapa principnycklar för auktorisering.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1454">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b6b44-1455">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b6b44-1455">Az.Network</span></span>
* <span data-ttu-id="b6b44-1456">”RoutingPreference” har lagts till i offentliga IP-taggar</span><span class="sxs-lookup"><span data-stu-id="b6b44-1456">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="b6b44-1457">Förbättra exempel för referensdokumentation om ”Get-AzNetworkServiceTag”</span><span class="sxs-lookup"><span data-stu-id="b6b44-1457">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="b6b44-1458">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="b6b44-1458">Az.PolicyInsights</span></span>
* <span data-ttu-id="b6b44-1459">Åtgärda problem med null-referens i Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="b6b44-1459">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="b6b44-1460">Mer information här: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="b6b44-1460">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="b6b44-1461">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="b6b44-1461">Az.OperationalInsights</span></span>
* <span data-ttu-id="b6b44-1462">Modellen för CustomLog-datakälla som returneras i Get-AzOperationalInsightsDataSource har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="b6b44-1462">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b6b44-1463">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b6b44-1463">Az.RecoveryServices</span></span>
* <span data-ttu-id="b6b44-1464">Kommandot get-policy för IaaSVM:er har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="b6b44-1464">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="b6b44-1465">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b6b44-1465">Az.Resources</span></span>
    - <span data-ttu-id="b6b44-1466">Korrigera hjälptext för den översta parametern i Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="b6b44-1466">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="b6b44-1467">Lägg till växlingsstöd på klientsidan för Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="b6b44-1467">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="b6b44-1468">Lägg till nya parametrar för Set-AzPolicyAssignment, -PolicyParameters och -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="b6b44-1468">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="b6b44-1469">En mängd dokument- och exempeluppdateringar för Policy-cmdletar</span><span class="sxs-lookup"><span data-stu-id="b6b44-1469">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="b6b44-1470">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="b6b44-1470">Az.ServiceBus</span></span>
* <span data-ttu-id="b6b44-1471">Korrigering av problem #4938 – New-AzureRmServiceBusQueue returnerar BadRequest vid konfiguration av MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="b6b44-1471">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="b6b44-1472">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b6b44-1472">Az.Sql</span></span>
* <span data-ttu-id="b6b44-1473">Lägg till cmdletar för instansredundansgrupper från förhandsversion till offentlig version</span><span class="sxs-lookup"><span data-stu-id="b6b44-1473">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="b6b44-1474">Stöd för granskning för Azure SQL Server\Database med nya cmdletar.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1474">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="b6b44-1475">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="b6b44-1475">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="b6b44-1476">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="b6b44-1476">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="b6b44-1477">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="b6b44-1477">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="b6b44-1478">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="b6b44-1478">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="b6b44-1479">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="b6b44-1479">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="b6b44-1480">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="b6b44-1480">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="b6b44-1481">Ta bort begränsningar för e-post från inställningarna för sårbarhetsbedömning</span><span class="sxs-lookup"><span data-stu-id="b6b44-1481">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b6b44-1482">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b6b44-1482">Az.Storage</span></span>
* <span data-ttu-id="b6b44-1483">Ändra två parametrar ”-IndexDocument” och ”-ErrorDocument404Path” från ”krävs” till ”valfri” i cmdlet:</span><span class="sxs-lookup"><span data-stu-id="b6b44-1483">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="b6b44-1484">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="b6b44-1484">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="b6b44-1485">Uppdatera hjälpen för Get-AzStorageBlobContent genom att lägga till ett exempel</span><span class="sxs-lookup"><span data-stu-id="b6b44-1485">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="b6b44-1486">Visa mer felinformation när cmdleten misslyckas med StorageException</span><span class="sxs-lookup"><span data-stu-id="b6b44-1486">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="b6b44-1487">Stöd för att skapa eller uppdatera lagringskonto med Azure Files AAD DS-autentisering</span><span class="sxs-lookup"><span data-stu-id="b6b44-1487">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="b6b44-1488">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b6b44-1488">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="b6b44-1489">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b6b44-1489">Set-AzStorageAccount</span></span>
* <span data-ttu-id="b6b44-1490">Stöd för att lista eller stänga filreferenser för en filresurs, filkatalog eller en fil</span><span class="sxs-lookup"><span data-stu-id="b6b44-1490">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="b6b44-1491">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="b6b44-1491">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="b6b44-1492">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="b6b44-1492">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="b6b44-1493">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="b6b44-1493">Az.StorageSync</span></span>
* <span data-ttu-id="b6b44-1494">Den här modulen ingår nu som en del av `Az`-sammanslagningsmodulen</span><span class="sxs-lookup"><span data-stu-id="b6b44-1494">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="b6b44-1495">2.3.2 – juni 2019</span><span class="sxs-lookup"><span data-stu-id="b6b44-1495">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b6b44-1496">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b6b44-1496">Az.Accounts</span></span>
* <span data-ttu-id="b6b44-1497">Åtgärda bugg med felaktiga webbadresser som i vissa fall användes för Functions-anrop</span><span class="sxs-lookup"><span data-stu-id="b6b44-1497">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="b6b44-1498">Mer information här: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="b6b44-1498">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="b6b44-1499">Åtgärda problem med alias från AzureRM i Az-cmdletar</span><span class="sxs-lookup"><span data-stu-id="b6b44-1499">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="b6b44-1500">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="b6b44-1500">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="b6b44-1501">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="b6b44-1501">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b6b44-1502">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b6b44-1502">Az.Compute</span></span>
* <span data-ttu-id="b6b44-1503">Parameteruppsättningarna New-AzVm och New-AzVmss accepterar nu parametern ”ProximityPlacementGroup”.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1503">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="b6b44-1504">Stavfel i referensdokumentationen för ”New-AzVM” har korrigerats</span><span class="sxs-lookup"><span data-stu-id="b6b44-1504">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="b6b44-1505">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="b6b44-1505">Az.Dns</span></span>
* <span data-ttu-id="b6b44-1506">Stavfel i hjälpexempel för ”Set-AzDnsZone” har korrigerats.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1506">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="b6b44-1507">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="b6b44-1507">Az.EventGrid</span></span>
* <span data-ttu-id="b6b44-1508">Har uppdaterats för att använda API-versionen 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1508">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="b6b44-1509">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="b6b44-1509">New cmdlets:</span></span>
    - <span data-ttu-id="b6b44-1510">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="b6b44-1510">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="b6b44-1511">Skapar en ny Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1511">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="b6b44-1512">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="b6b44-1512">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="b6b44-1513">Hämtar information om en Event Grid-domän eller hämtar en lista med alla Event Grid-domäner i den aktuella Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1513">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="b6b44-1514">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="b6b44-1514">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="b6b44-1515">Tar bort en Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1515">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="b6b44-1516">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="b6b44-1516">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="b6b44-1517">Återskapar nyckeln för delad åtkomst för en Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1517">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="b6b44-1518">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="b6b44-1518">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="b6b44-1519">Hämtar de nycklar för delad åtkomst som används för att publicera händelser till en Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1519">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="b6b44-1520">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="b6b44-1520">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="b6b44-1521">Skapar ett nytt Azure Event Grid-domänämne.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1521">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="b6b44-1522">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="b6b44-1522">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="b6b44-1523">Hämtar information om ett Event Grid-domänämne eller hämtar en lista med alla Event Grid-domänämnen under en specifik Event Grid-domän i nuvarande Azure</span><span class="sxs-lookup"><span data-stu-id="b6b44-1523">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="b6b44-1524">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="b6b44-1524">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="b6b44-1525">Tar bort ett befintligt Azure Event Grid-domänämne.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1525">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="b6b44-1526">Uppdaterade cmdletar:</span><span class="sxs-lookup"><span data-stu-id="b6b44-1526">Updated cmdlets:</span></span>
    - <span data-ttu-id="b6b44-1527">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="b6b44-1527">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="b6b44-1528">Lägg till nya obligatoriska parametrar för att stödja piping för den nya Event Grid-domänen och Event Grid-domänämnet för att göra det möjligt att skapa nya händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1528">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="b6b44-1529">Lägg till nya obligatoriska parametrar för att ange det nya Event Grid-domännamnet och/eller namnet på Event Grid-domänämnet för att göra det möjligt att skapa nya händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1529">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="b6b44-1530">Lägg till ny parameteruppsättningar för domäner och domänämnen för att göra det möjligt att återanvända befintliga parametrar (t.ex. EndPointType, SubjectBeginsWith osv).</span><span class="sxs-lookup"><span data-stu-id="b6b44-1530">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="b6b44-1531">Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="b6b44-1531">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="b6b44-1532">Förfallodatum för händelseprenumeration</span><span class="sxs-lookup"><span data-stu-id="b6b44-1532">Event subscription expiration date,</span></span>
            - <span data-ttu-id="b6b44-1533">Avancerade filterparametrar.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1533">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="b6b44-1534">Lägg till ny uppräkning för servicebusqueue som mål.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1534">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="b6b44-1535">Tillåt inte användning av ”Alla” i alternativet -IncludedEventType och ersätt det med</span><span class="sxs-lookup"><span data-stu-id="b6b44-1535">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="b6b44-1536">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="b6b44-1536">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="b6b44-1537">Lägg till ny valfria parametrar (Top, ODataQuery och NextLink) för att stödja sidnumrering och filtrering av resultat.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1537">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="b6b44-1538">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="b6b44-1538">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="b6b44-1539">Lägg till nya obligatoriska parametrar för att stödja piping för en Event Grid-domän och Event Grid-domänämnen för att göra det möjligt att ta bort befintliga händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1539">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="b6b44-1540">Lägg till nya obligatoriska parametrar för att ange Event Grid-domännamnet och/eller namnet på Event Grid-domänämnet för att göra det möjligt att ta bort befintliga händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1540">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="b6b44-1541">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="b6b44-1541">Az.FrontDoor</span></span>
* <span data-ttu-id="b6b44-1542">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="b6b44-1542">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="b6b44-1543">Lägg till stöd för transformeringar och nytt värde för automatisk komplettering för operatorer (RegEx)</span><span class="sxs-lookup"><span data-stu-id="b6b44-1543">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="b6b44-1544">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="b6b44-1544">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="b6b44-1545">Lägg till nya värden för automatisk komplettering</span><span class="sxs-lookup"><span data-stu-id="b6b44-1545">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b6b44-1546">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b6b44-1546">Az.Network</span></span>
* <span data-ttu-id="b6b44-1547">Lägg till stöd för resurs för virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="b6b44-1547">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="b6b44-1548">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="b6b44-1548">New cmdlets</span></span>
        - <span data-ttu-id="b6b44-1549">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="b6b44-1549">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="b6b44-1550">Lägg till AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="b6b44-1550">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="b6b44-1551">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="b6b44-1551">New cmdlets</span></span>
        - <span data-ttu-id="b6b44-1552">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="b6b44-1552">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="b6b44-1553">Lägg till PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="b6b44-1553">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="b6b44-1554">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="b6b44-1554">New cmdlets</span></span>
        - <span data-ttu-id="b6b44-1555">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="b6b44-1555">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="b6b44-1556">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="b6b44-1556">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="b6b44-1557">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="b6b44-1557">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="b6b44-1558">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="b6b44-1558">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="b6b44-1559">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="b6b44-1559">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="b6b44-1560">Lägg till PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="b6b44-1560">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="b6b44-1561">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="b6b44-1561">New cmdlets</span></span>
        - <span data-ttu-id="b6b44-1562">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="b6b44-1562">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="b6b44-1563">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="b6b44-1563">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="b6b44-1564">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="b6b44-1564">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="b6b44-1565">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="b6b44-1565">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="b6b44-1566">Nedanstående kommandon för funktionen har uppdaterats: Flaggan UseLocalAzureIpAddress på VpnConnection</span><span class="sxs-lookup"><span data-stu-id="b6b44-1566">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="b6b44-1567">New-AzVpnConnection har uppdaterats: Den valfria parametern -UseLocalAzureIpAddress har lagts till för att visa att en lokal IP-adress i Azure ska användas som källadress när anslutningen initieras.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1567">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="b6b44-1568">Set-AzVpnConnection har uppdaterats: Den valfria parametern -UseLocalAzureIpAddress har lagts till för att visa att en lokal IP-adress i Azure ska användas som källadress när anslutningen initieras.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1568">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="b6b44-1569">Det skrivskyddade fältet PeeredConnections har lagts till i ExpressRoute-peering.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1569">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="b6b44-1570">Det skrivskyddade fältet GlobalReachEnabled har lagts till i ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1570">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="b6b44-1571">Ett attribut för icke-bakåtkompatibla ändringar har lagts till för att lyfta fram utfasning av fältet AllowGlobalReach i modellen ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b6b44-1571">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="b6b44-1572">Problem 8756 har åtgärdats: Fel vid användning av TargetListenerID med AzApplicationGatewayRedirectConfiguration-cmdletar</span><span class="sxs-lookup"><span data-stu-id="b6b44-1572">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="b6b44-1573">En bugg i New-AzApplicationGatewayPathRuleConfig som gjorde att regeluppsättningen för att återskapa inte kunde anges har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1573">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="b6b44-1574">Visningen av VirtualNetworkTaps i NetworkInterfaceIpConfiguration har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="b6b44-1574">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="b6b44-1575">Cortex Get-cmdletar för att visa en lista med alla delar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="b6b44-1575">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="b6b44-1576">Funktionen för att skapa VirtualHub-referenser för ExpressRouteGateways och VpnGateway har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="b6b44-1576">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="b6b44-1577">Stöd för tillgänglighetszoner i AzureFirewall och NatGateway har lagts till</span><span class="sxs-lookup"><span data-stu-id="b6b44-1577">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="b6b44-1578">Cmdleten Get-AzNetworkServiceTag har lagts till</span><span class="sxs-lookup"><span data-stu-id="b6b44-1578">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="b6b44-1579">Lägg till stöd för flera offentliga IP-adresser för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="b6b44-1579">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="b6b44-1580">Cmdleten New-AzFirewall har uppdaterats:</span><span class="sxs-lookup"><span data-stu-id="b6b44-1580">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="b6b44-1581">Parametern -PublicIpAddress som accepterar ett eller flera offentliga IP-adressobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="b6b44-1581">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="b6b44-1582">Parametern -VirtualNetwork som accepterar ett virtuellt nätverksobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="b6b44-1582">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="b6b44-1583">Metoderna AddPublicIpAddress och RemovePublicIpAddress har lagts till på brandväggsobjekt – dessa accepterar ett offentligt IP-adressobjekt som indata</span><span class="sxs-lookup"><span data-stu-id="b6b44-1583">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="b6b44-1584">Inaktuella parametrar -PublicIpName och -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="b6b44-1584">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="b6b44-1585">Nedanstående kommandon för funktionen har uppdaterats: Ange autentiseringsalternativ för VpnClient AAD till resurser för virtuella nätverksgatewayer.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1585">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="b6b44-1586">New-AzVirtualNetworkGateway har uppdaterats: De valfria parametrarna AadTenantUri, AadAudienceId och AadIssuerUri för att ange VpnClient AAD-autentiseringsalternativ på en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1586">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="b6b44-1587">Set-AzVirtualNetworkGateway har uppdaterats: De valfria parametrarna AadTenantUri, AadAudienceId och AadIssuerUri för att ange VpnClient AAD-autentiseringsalternativ på en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1587">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="b6b44-1588">Set-AzVirtualNetworkGateway har uppdaterats: Den valfria växelparametern RemoveAadAuthentication som tar bort VpnClient AAD-autentiseringsalternativ från en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1588">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="b6b44-1589">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="b6b44-1589">Az.OperationalInsights</span></span>
* <span data-ttu-id="b6b44-1590">Aktivera prisnivån **pergb2018** i kommandot ”New-AzureRmOperationalInsightsWorkspace”</span><span class="sxs-lookup"><span data-stu-id="b6b44-1590">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="b6b44-1591">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b6b44-1591">Az.Resources</span></span>
* <span data-ttu-id="b6b44-1592">Stöd för ytterligare alternativ för att exportera en mall</span><span class="sxs-lookup"><span data-stu-id="b6b44-1592">Support for additional Template Export options</span></span>
    - <span data-ttu-id="b6b44-1593">Lägg till parametern ”-SkipResourceNameParameterization” till Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b6b44-1593">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="b6b44-1594">Lägg till parametern ”-SkipAllParameterization” till Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b6b44-1594">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="b6b44-1595">Lägg till parametern ”-Resource” till Export-AzResourceGroup för exporterad resursfiltrering</span><span class="sxs-lookup"><span data-stu-id="b6b44-1595">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="b6b44-1596">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b6b44-1596">Az.ServiceFabric</span></span>
* <span data-ttu-id="b6b44-1597">Åtgärda att fel tumavtryck används vid tilläggning av certifikat i ByExistingKeyVault i vissa fall</span><span class="sxs-lookup"><span data-stu-id="b6b44-1597">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="b6b44-1598">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b6b44-1598">Az.Sql</span></span>
* <span data-ttu-id="b6b44-1599">Åtgärda suffix för lagringsslutpunkt i Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="b6b44-1599">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="b6b44-1600">Åtgärda att aktivering av Advanced Data Security åsidosätter Advanced Threat Protection-princip</span><span class="sxs-lookup"><span data-stu-id="b6b44-1600">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="b6b44-1601">Nya cmdletar för Management.Sql som gör att kunderna kan lägga till nycklar för transparent datakryptering (TDE) och ange TDE-skydd för hanterade instanser</span><span class="sxs-lookup"><span data-stu-id="b6b44-1601">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="b6b44-1602">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b6b44-1602">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="b6b44-1603">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b6b44-1603">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="b6b44-1604">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b6b44-1604">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="b6b44-1605">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="b6b44-1605">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="b6b44-1606">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="b6b44-1606">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b6b44-1607">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b6b44-1607">Az.Storage</span></span>
* <span data-ttu-id="b6b44-1608">Stöd för typerna FileStorage och SkuName Premium_ZRS när lagringskonton skapas</span><span class="sxs-lookup"><span data-stu-id="b6b44-1608">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="b6b44-1609">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b6b44-1609">New-AzStorageAccount</span></span>
* <span data-ttu-id="b6b44-1610">Beskrivningen av cmdleten för bloboföränderlighet har förtydligats</span><span class="sxs-lookup"><span data-stu-id="b6b44-1610">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="b6b44-1611">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="b6b44-1611">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b6b44-1612">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b6b44-1612">Az.Websites</span></span>
* <span data-ttu-id="b6b44-1613">Optimerar Get-AzWebAppCertificate för att filtrera efter resursgrupp på servern i stället för klienten</span><span class="sxs-lookup"><span data-stu-id="b6b44-1613">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="b6b44-1614">Lägger till växlingsparametern -UseDisasterRecovery till Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="b6b44-1614">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="b6b44-1615">2.2.0 – juni 2019</span><span class="sxs-lookup"><span data-stu-id="b6b44-1615">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="b6b44-1616">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="b6b44-1616">Az.Cdn</span></span>
* <span data-ttu-id="b6b44-1617">Uppdaterade cmdletar för att ge stöd för rulesEngine-funktion baserat på API-version 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1617">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b6b44-1618">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b6b44-1618">Az.Compute</span></span>
* <span data-ttu-id="b6b44-1619">Lade till parameter `NoWait` som startar åtgärden och returnerar omedelbart, innan åtgärden har slutförts.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1619">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="b6b44-1620">Uppdaterade cmdletar:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="b6b44-1620">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="b6b44-1621">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="b6b44-1621">Az.EventHub</span></span>
* <span data-ttu-id="b6b44-1622">Korrigering för #9231 – Get-AzEventHubNamespace returnerar inga taggar</span><span class="sxs-lookup"><span data-stu-id="b6b44-1622">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="b6b44-1623">Korrigering för #9230 – Get-AzEventHubNamespace returnerar ResourceGroup istället för ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6b44-1623">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b6b44-1624">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b6b44-1624">Az.Network</span></span>
* <span data-ttu-id="b6b44-1625">Uppdatera ResourceId och InputObject för NAT-gateway</span><span class="sxs-lookup"><span data-stu-id="b6b44-1625">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="b6b44-1626">Lägg till alias för ResourceId och InputObject</span><span class="sxs-lookup"><span data-stu-id="b6b44-1626">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="b6b44-1627">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="b6b44-1627">Az.PolicyInsights</span></span>
* <span data-ttu-id="b6b44-1628">Åtgärda Null-referensproblem i Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="b6b44-1628">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b6b44-1629">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b6b44-1629">Az.RecoveryServices</span></span>
* <span data-ttu-id="b6b44-1630">Minsta kvarhållning för IaaSVM-policy i dagar ändrat till 7 från 1</span><span class="sxs-lookup"><span data-stu-id="b6b44-1630">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="b6b44-1631">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="b6b44-1631">Az.ServiceBus</span></span>
* <span data-ttu-id="b6b44-1632">Korrigering för ärende #9182 – Get-AzServiceBusNamespace returnerar ResourceGroup istället för ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6b44-1632">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="b6b44-1633">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b6b44-1633">Az.ServiceFabric</span></span>
* <span data-ttu-id="b6b44-1634">Åtgärda stavfel i felmeddelandet för Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="b6b44-1634">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="b6b44-1635">Åtgärda saknat tecken i Service Fabric-kommandorader</span><span class="sxs-lookup"><span data-stu-id="b6b44-1635">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="b6b44-1636">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b6b44-1636">Az.Sql</span></span>
* <span data-ttu-id="b6b44-1637">Lägg till parametern DnsZonePartner för New-AzureSqlInstance-cmdlet för att ge stöd för AutoDr för hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1637">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="b6b44-1638">Avvecklar cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b6b44-1638">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="b6b44-1639">Döp om cmdletar för hotidentifiering till Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="b6b44-1639">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="b6b44-1640">Parametrarna New-AzSqlInstance -StorageSizeInGB och -LicenseType är nu valfria.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1640">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b6b44-1641">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b6b44-1641">Az.Websites</span></span>
* <span data-ttu-id="b6b44-1642">åtgärdar problemet där användningen av Set-AzWebApp och Set-AzWebAppSlot med -WebApp-egenskap tog bort taggarna</span><span class="sxs-lookup"><span data-stu-id="b6b44-1642">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="b6b44-1643">2.1.0 – maj 2019</span><span class="sxs-lookup"><span data-stu-id="b6b44-1643">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="b6b44-1644">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b6b44-1644">Az.ApiManagement</span></span>
* <span data-ttu-id="b6b44-1645">Skapade nya cmdletar för att hantera diagnostik för global- och API-omfång</span><span class="sxs-lookup"><span data-stu-id="b6b44-1645">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="b6b44-1646">**Get-AzApiManagementDiagnostic** – Skaffa diagnostik konfigurerad för global- eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="b6b44-1646">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="b6b44-1647">**New-AzApiManagementDiagnostic** – Skapa ny diagnostik för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="b6b44-1647">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="b6b44-1648">**New-AzApiManagementHttpMessageDiagnostic** – Skapa diagnostikinställning om vilka rubriker som ska loggas och storleken på brödtextbyte</span><span class="sxs-lookup"><span data-stu-id="b6b44-1648">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="b6b44-1649">**New-AzApiManagementPipelineDiagnosticSetting** – Skapa diagnostikinställningar för inkommande/utgående HTTP-meddelanden till gatewayen.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1649">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="b6b44-1650">**New-AzApiManagementSamplingSetting** – Skapa samplinginställningar för begäranden/svar för en diagnostik</span><span class="sxs-lookup"><span data-stu-id="b6b44-1650">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="b6b44-1651">**Remove-AzApiManagementDiagnostic** – Ta bort en diagnostikenhet för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="b6b44-1651">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="b6b44-1652">**Set-AzApiManagementDiagnostic** – Uppdatera en diagnostikenhet för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="b6b44-1652">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="b6b44-1653">Skapade nya cmdletar för hantering av cacheminne i ApiManagement-tjänsten</span><span class="sxs-lookup"><span data-stu-id="b6b44-1653">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="b6b44-1654">**Get-AzApiManagementCache** – Hämta information om cacheminnet som anges av identifierare eller alla cacheminnen</span><span class="sxs-lookup"><span data-stu-id="b6b44-1654">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="b6b44-1655">**New-AzApiManagementCache** – Skapa ett nytt default-cacheminne eller cacheminne i en viss Azure-region</span><span class="sxs-lookup"><span data-stu-id="b6b44-1655">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="b6b44-1656">**Remove-AzApiManagementCache** – Ta bort ett cacheminne</span><span class="sxs-lookup"><span data-stu-id="b6b44-1656">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="b6b44-1657">**Remove-AzApiManagementCache** – Ta bort ett cacheminne</span><span class="sxs-lookup"><span data-stu-id="b6b44-1657">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="b6b44-1658">Skapade nya cmdletar för hantering av API-schema</span><span class="sxs-lookup"><span data-stu-id="b6b44-1658">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="b6b44-1659">**New-AzApiManagementSchema** – Skapa ett nytt schema för ett API</span><span class="sxs-lookup"><span data-stu-id="b6b44-1659">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="b6b44-1660">**Get-AzApiManagementSchema** – Hämta de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="b6b44-1660">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="b6b44-1661">**Remove-AzApiManagementSchema** – Ta bort de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="b6b44-1661">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="b6b44-1662">**Set-AzApiManagementSchema** – Uppdatera de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="b6b44-1662">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="b6b44-1663">Skapa ny cmdlet för att generera en användartoken.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1663">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="b6b44-1664">**New-AzApiManagementUserToken** – Skapa en ny användartoken som enligt standardinställning är giltig i 8 timmar. Token för GIT-användaren kan skapas med den här cmdleten./</span><span class="sxs-lookup"><span data-stu-id="b6b44-1664">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="b6b44-1665">Skapade en ny cmdlet för att hämta nätverksstatus</span><span class="sxs-lookup"><span data-stu-id="b6b44-1665">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="b6b44-1666">**Get-AzApiManagementNetworkStatus** – Hämta nätverksstatusanslutningen för resurserna som API Management-tjänsten är beroende av.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1666">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="b6b44-1667">Det här är användbart när du distribuerar ApiManagement-tjänsten i ett virtuellt nätverk och validerar om något beroende är brutet.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1667">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="b6b44-1668">Uppdaterade cmdlet **New-AzApiManagement** för att hantera ApiManagement-tjänsten</span><span class="sxs-lookup"><span data-stu-id="b6b44-1668">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="b6b44-1669">Lade till stöd för den nya SKU:n Consumption</span><span class="sxs-lookup"><span data-stu-id="b6b44-1669">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="b6b44-1670">Aktiverade stöd för att slå på flaggan EnableClientCertificate för SKU:n Consumption</span><span class="sxs-lookup"><span data-stu-id="b6b44-1670">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="b6b44-1671">Den nya cmdleten **New-AzApiManagementSslSetting** gör det möjligt att ställa in TLS/SSL-inställningen på ”Backend” och ”Frontend” (serverdel och klientdel).</span><span class="sxs-lookup"><span data-stu-id="b6b44-1671">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="b6b44-1672">Det här kan också användas till att konfigurera chiffer som 3DES och ServerProtocols som Http2 för Frontend för en ApiManagement-tjänst.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1672">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="b6b44-1673">Stöd har lagts till för att konfigurera värdnamnet DeveloperPortal på ApiManagement-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1673">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="b6b44-1674">Uppdaterade cmdletar **Get-AzApiManagementSsoToken** för att ta PsApiManagement-objekt som indata</span><span class="sxs-lookup"><span data-stu-id="b6b44-1674">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="b6b44-1675">Uppdaterad cmdleten för att visa infogade felmeddelanden</span><span class="sxs-lookup"><span data-stu-id="b6b44-1675">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="b6b44-1676">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Felkod: Felmeddelande av typen ValidationError: Ett eller flera fält innehåller felaktiga värden: Felinformation:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="b6b44-1676">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="b6b44-1677">Uppdaterade cmdlet **Export-AzApiManagementApi** för att exportera API:er i OpenApi 3.0-format</span><span class="sxs-lookup"><span data-stu-id="b6b44-1677">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="b6b44-1678">Uppdaterade cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="b6b44-1678">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="b6b44-1679">Importera API från dokumentspecifikationen OpenApi 3.0</span><span class="sxs-lookup"><span data-stu-id="b6b44-1679">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="b6b44-1680">Om du vill åsidosätta egenskapen PsApiManagementSchema specificerad i ett dokument (Swagger, Wadl, Wsdl, OpenApi).</span><span class="sxs-lookup"><span data-stu-id="b6b44-1680">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="b6b44-1681">Åsidosätta egenskapen ServiceUrl som specificeras i ett dokument.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1681">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="b6b44-1682">Uppdaterade cmdlet **Get-AzApiManagementPolicy** för att returnera policy i undantaget format av typen icke-XML med rawxml</span><span class="sxs-lookup"><span data-stu-id="b6b44-1682">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="b6b44-1683">Uppdaterade cmdlet **Set-AzApiManagementPolicy** för att godkänna policy i undantaget format av typen icke-XML med rawxml och XML undantaget med xml</span><span class="sxs-lookup"><span data-stu-id="b6b44-1683">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="b6b44-1684">Uppdaterad cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="b6b44-1684">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="b6b44-1685">Konfigurera API med OpenId auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1685">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="b6b44-1686">Skapa ett API i ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="b6b44-1686">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="b6b44-1687">Klona ett API med SourceApiId och SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1687">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="b6b44-1688">Möjlighet att konfigurera SubscriptionRequired i API-omfattningen.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1688">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="b6b44-1689">Uppdaterad cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="b6b44-1689">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="b6b44-1690">Konfigurera API med OpenId auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1690">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="b6b44-1691">Uppdatera ett API till ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="b6b44-1691">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="b6b44-1692">Möjlighet att konfigurera SubscriptionRequired i API-omfattningen.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1692">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="b6b44-1693">Uppdaterad cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="b6b44-1693">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="b6b44-1694">Klona en befintlig version med hjälp av SourceApiRevision (kopiera taggar, produkter, åtgärder och principer).</span><span class="sxs-lookup"><span data-stu-id="b6b44-1694">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="b6b44-1695">Den nya revisionen antar ApiId från den överordnade instansen.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1695">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="b6b44-1696">Tillhandahålla ApiRevisionDescription</span><span class="sxs-lookup"><span data-stu-id="b6b44-1696">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="b6b44-1697">Åsidosätta ServiceUrl vid kloning av ett API.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1697">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="b6b44-1698">Uppdaterad cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="b6b44-1698">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="b6b44-1699">Konfigurera AAD eller AADB2C med en Authority</span><span class="sxs-lookup"><span data-stu-id="b6b44-1699">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="b6b44-1700">Konfigurera SignupPolicy, SigninPolicy, ProfileEditingPolicy och PasswordResetPolicy</span><span class="sxs-lookup"><span data-stu-id="b6b44-1700">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="b6b44-1701">Uppdaterad cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="b6b44-1701">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="b6b44-1702">Kompensera för ny SubscriptonModel med Scope och UserId</span><span class="sxs-lookup"><span data-stu-id="b6b44-1702">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="b6b44-1703">Kompensera för gammal prenumerationsmodell med ProductId och UserId</span><span class="sxs-lookup"><span data-stu-id="b6b44-1703">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="b6b44-1704">Lägg till funktion för att aktivera AllowTracing på prenumerationsnivå.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1704">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="b6b44-1705">Uppdaterad cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="b6b44-1705">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="b6b44-1706">Kompensera för ny SubscriptonModel med Scope och UserId</span><span class="sxs-lookup"><span data-stu-id="b6b44-1706">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="b6b44-1707">Kompensera för gammal prenumerationsmodell med ProductId och UserId</span><span class="sxs-lookup"><span data-stu-id="b6b44-1707">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="b6b44-1708">Lägg till funktion för att aktivera AllowTracing på prenumerationsnivå.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1708">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="b6b44-1709">Uppdaterade följande cmdletar för att acceptera ResourceId som indata</span><span class="sxs-lookup"><span data-stu-id="b6b44-1709">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="b6b44-1710">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b6b44-1710">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="b6b44-1711">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="b6b44-1711">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="b6b44-1712">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="b6b44-1712">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="b6b44-1713">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="b6b44-1713">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="b6b44-1714">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="b6b44-1714">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="b6b44-1715">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="b6b44-1715">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="b6b44-1716">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="b6b44-1716">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="b6b44-1717">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="b6b44-1717">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="b6b44-1718">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="b6b44-1718">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="b6b44-1719">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="b6b44-1719">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="b6b44-1720">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="b6b44-1720">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="b6b44-1721">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="b6b44-1721">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="b6b44-1722">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b6b44-1722">Az.Automation</span></span>
* <span data-ttu-id="b6b44-1723">Uppdaterade Get-AzAutomationJobOutputRecord för att hantera postvärden av typen JSON och Text.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1723">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="b6b44-1724">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="b6b44-1724">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="b6b44-1725">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="b6b44-1725">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="b6b44-1726">Ändrade beteende för Start-AzAutomationDscCompilationJob till att bara starta jobbet istället för att vänta på slutförandet.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1726">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="b6b44-1727">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="b6b44-1727">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="b6b44-1728">Korrigering för Get-AzAutomationDscNode när using -Name returnerar alla noder.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1728">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="b6b44-1729">Nu returnerar den endast den matchande noden.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1729">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b6b44-1730">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b6b44-1730">Az.Compute</span></span>
* <span data-ttu-id="b6b44-1731">Lägg till parametrarna ProtectFromScaleIn och ProtectFromScaleSetAction i cmdleten Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1731">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="b6b44-1732">Nu är standardinställningen att vimpelparametern New-AzVM använder en tillgänglig plats om USA, östra inte stöds</span><span class="sxs-lookup"><span data-stu-id="b6b44-1732">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b6b44-1733">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b6b44-1733">Az.DataLakeStore</span></span>
* <span data-ttu-id="b6b44-1734">Uppdatera ADLS-sdk för att använda httpclient, integrera dataplanstestning med Azure-ramverk</span><span class="sxs-lookup"><span data-stu-id="b6b44-1734">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="b6b44-1735">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b6b44-1735">Az.Monitor</span></span>
* <span data-ttu-id="b6b44-1736">Korrigera felaktiga parameternamn i hjälpexempel</span><span class="sxs-lookup"><span data-stu-id="b6b44-1736">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b6b44-1737">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b6b44-1737">Az.Network</span></span>
* <span data-ttu-id="b6b44-1738">Lägg till flaggan DisableBgpRoutePropagation i utdata för effektiv routningstabell</span><span class="sxs-lookup"><span data-stu-id="b6b44-1738">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="b6b44-1739">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="b6b44-1739">Updated cmdlet:</span></span>
        - <span data-ttu-id="b6b44-1740">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="b6b44-1740">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="b6b44-1741">Åtgärda dubbelstreck i dokumentationen New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="b6b44-1741">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="b6b44-1742">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b6b44-1742">Az.Resources</span></span>
* <span data-ttu-id="b6b44-1743">Lägg till ny cmdlet Get-AzureRmDenyAssignment för att hämta tilldelningsnekanden</span><span class="sxs-lookup"><span data-stu-id="b6b44-1743">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="b6b44-1744">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b6b44-1744">Az.Sql</span></span>
* <span data-ttu-id="b6b44-1745">Döp om Advanced Threat Protection-cmdletar för Advanced Data Security och aktivera Vulnerability Assessment som standard</span><span class="sxs-lookup"><span data-stu-id="b6b44-1745">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="b6b44-1746">2.0.0 – maj 2019</span><span class="sxs-lookup"><span data-stu-id="b6b44-1746">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b6b44-1747">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b6b44-1747">Az.Accounts</span></span>
* <span data-ttu-id="b6b44-1748">Uppdatera autentiseringsbiblioteket för att åtgärda ADFS-problem med autentisering av användarnamn/lösenord</span><span class="sxs-lookup"><span data-stu-id="b6b44-1748">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="b6b44-1749">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="b6b44-1749">Az.CognitiveServices</span></span>
* <span data-ttu-id="b6b44-1750">Visa endast Bing-ansvarsfriskrivning för Bing-sökningstjänster.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1750">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="b6b44-1751">Förbättra felmeddelande när det inte går att skapa konton.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1751">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b6b44-1752">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b6b44-1752">Az.Compute</span></span>
* <span data-ttu-id="b6b44-1753">Funktion för närhetsplaceringsgrupper.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1753">Proximity placement group feature.</span></span>
    - <span data-ttu-id="b6b44-1754">Följande nya cmdletar har lagts till:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="b6b44-1754">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="b6b44-1755">Den nya parametern ProximityPlacementGroupId har lagts till i följande cmdletar:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="b6b44-1755">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="b6b44-1756">Parametern StorageAccountType har lagts till i New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1756">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="b6b44-1757">TargetRegion för New-AzGalleryImageVersion kan innehålla StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1757">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="b6b44-1758">Växlingsparametern SkipShutdown har lagts till i Stop-AzVM och Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b6b44-1758">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="b6b44-1759">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="b6b44-1759">Breaking changes</span></span>
    - <span data-ttu-id="b6b44-1760">Set-AzVMBootDiagnostics har ändrats till Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1760">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="b6b44-1761">Export-AzLogAnalyticThrottledRequests har ändrats till Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1761">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="b6b44-1762">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="b6b44-1762">Az.DeploymentManager</span></span>
* <span data-ttu-id="b6b44-1763">De första allmänt tillgängliga versionerna av cmdletar för Distributionshanteraren i Azure</span><span class="sxs-lookup"><span data-stu-id="b6b44-1763">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="b6b44-1764">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="b6b44-1764">Az.Dns</span></span>
* <span data-ttu-id="b6b44-1765">Automatisk delegering av DNS för NameServer</span><span class="sxs-lookup"><span data-stu-id="b6b44-1765">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="b6b44-1766">Det överordnade zonnamnet kan användas som ytterligare valfri parameter i cmdleten för att skapa DNS-zoner.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1766">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="b6b44-1767">Lägger till NS-poster för en nyligen skapad underordnad zon i den överordnade zonen.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1767">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="b6b44-1768">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="b6b44-1768">Az.FrontDoor</span></span>
* <span data-ttu-id="b6b44-1769">De första allmänt tillgängliga versionerna av cmdletar för Azure FrontDoor</span><span class="sxs-lookup"><span data-stu-id="b6b44-1769">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="b6b44-1770">Byt namn på WAF-cmdletar så att de omfattar ”Waf”</span><span class="sxs-lookup"><span data-stu-id="b6b44-1770">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="b6b44-1771">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="b6b44-1771">Az.HDInsight</span></span>
* <span data-ttu-id="b6b44-1772">Två cmdletar har tagits bort:</span><span class="sxs-lookup"><span data-stu-id="b6b44-1772">Removed two cmdlets:</span></span>
    - <span data-ttu-id="b6b44-1773">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="b6b44-1773">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="b6b44-1774">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="b6b44-1774">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="b6b44-1775">En ny cmdlet har lagts till, Set-AzHDInsightGatewayCredential, som ersätter Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="b6b44-1775">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="b6b44-1776">Uppdatera cmdleten Get-AzHDInsightJobOutput för att skilja mellan läsarrollen och HDInsight-operatörsrollen:</span><span class="sxs-lookup"><span data-stu-id="b6b44-1776">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="b6b44-1777">Användare med läsarrollen måste uttryckligen ange parametern ”DefaultStorageAccountKey”, annars uppstår fel.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1777">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="b6b44-1778">Användare med HDInsight-operatörsrollen påverkas inte.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1778">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="b6b44-1779">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b6b44-1779">Az.Monitor</span></span>
* <span data-ttu-id="b6b44-1780">Nya cmdletar för SQR API (schemalagd frågeregel)</span><span class="sxs-lookup"><span data-stu-id="b6b44-1780">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="b6b44-1781">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="b6b44-1781">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="b6b44-1782">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="b6b44-1782">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="b6b44-1783">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="b6b44-1783">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="b6b44-1784">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="b6b44-1784">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="b6b44-1785">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="b6b44-1785">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="b6b44-1786">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="b6b44-1786">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="b6b44-1787">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="b6b44-1787">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="b6b44-1788">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="b6b44-1788">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="b6b44-1789">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="b6b44-1789">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="b6b44-1790">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="b6b44-1790">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="b6b44-1791">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="b6b44-1791">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="b6b44-1792">[Mer](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information om SQR API</span><span class="sxs-lookup"><span data-stu-id="b6b44-1792">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="b6b44-1793">Az.Monitor.md har uppdaterats för att omfatta cmdletar för måttbaserade aviseringsregler i GenV2 (inte klassiska)</span><span class="sxs-lookup"><span data-stu-id="b6b44-1793">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b6b44-1794">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b6b44-1794">Az.Network</span></span>
* <span data-ttu-id="b6b44-1795">Lägg till stöd för NAT Gateway-resurs</span><span class="sxs-lookup"><span data-stu-id="b6b44-1795">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="b6b44-1796">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="b6b44-1796">New cmdlets</span></span>
        - <span data-ttu-id="b6b44-1797">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="b6b44-1797">New-AzNatGateway</span></span>
        - <span data-ttu-id="b6b44-1798">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="b6b44-1798">Get-AzNatGateway</span></span>
        - <span data-ttu-id="b6b44-1799">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="b6b44-1799">Set-AzNatGateway</span></span>
        - <span data-ttu-id="b6b44-1800">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="b6b44-1800">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="b6b44-1801">Uppdaterade cmdletar</span><span class="sxs-lookup"><span data-stu-id="b6b44-1801">Updated cmdlets</span></span>
        - <span data-ttu-id="b6b44-1802">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="b6b44-1802">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="b6b44-1803">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="b6b44-1803">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="b6b44-1804">Nedanstående kommandon för funktionen har uppdaterats: Ange/ta bort anpassade vägar på Brooklyn Gateway.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1804">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="b6b44-1805">New-AzVirtualNetworkGateway har uppdaterats: Den valfria parametern -CustomRoute har lagts till för att ställa in adressprefix som anpassade vägar för att ange gateway.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1805">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="b6b44-1806">Set-AzVirtualNetworkGateway har uppdaterats: Den valfria parametern -CustomRoute har lagts till för att ange adressprefix som anpassade vägar för att ange gateway.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1806">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="b6b44-1807">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="b6b44-1807">Az.PolicyInsights</span></span>
* <span data-ttu-id="b6b44-1808">Stöd för att fråga efter information om principutvärdering.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1808">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="b6b44-1809">Lägg till parametern ”-Expand” för Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1809">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="b6b44-1810">Stöd för -Expand PolicyEvaluationDetails.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1810">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b6b44-1811">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b6b44-1811">Az.RecoveryServices</span></span>
* <span data-ttu-id="b6b44-1812">Stöd för att dela prenumeration mellan Azure och Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1812">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="b6b44-1813">Markering av kommande icke-bakåtkompatibla ändringar för Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1813">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="b6b44-1814">Korrigering för återställningsplan och åtgärdsplan i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1814">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="b6b44-1815">Korrigering för mappning av uppdateringsnätverk i Azure Site Recovery för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1815">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="b6b44-1816">Korrigering för instruktioner för uppdateringsskydd i Azure Site Recovery för Azure till Azure för hanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1816">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="b6b44-1817">Andra mindre korrigeringar.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1817">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="b6b44-1818">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="b6b44-1818">Az.Relay</span></span>
* <span data-ttu-id="b6b44-1819">Korrigera stavfel i kundriktade meddelanden</span><span class="sxs-lookup"><span data-stu-id="b6b44-1819">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="b6b44-1820">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="b6b44-1820">Az.ServiceBus</span></span>
* <span data-ttu-id="b6b44-1821">Nya cmdletar har lagts till för NetworkRuleSet för namnområden</span><span class="sxs-lookup"><span data-stu-id="b6b44-1821">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b6b44-1822">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b6b44-1822">Az.Storage</span></span>
* <span data-ttu-id="b6b44-1823">Uppgradera till lagringsklientbiblioteket 10.0.1 (namnområdet för alla objekt från detta SDK ändras från ”Microsoft.WindowsAzure.Storage. *till ”Microsoft.Azure.Storage.* ”)</span><span class="sxs-lookup"><span data-stu-id="b6b44-1823">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="b6b44-1824">Uppgradera till Microsoft.Azure.Management.Storage 11.0.0 för att stödja den nya API-versionen 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1824">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="b6b44-1825">Standardlagringskontot i Skapa lagringskonto ändras från ”Storage” till ”StorageV2”</span><span class="sxs-lookup"><span data-stu-id="b6b44-1825">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="b6b44-1826">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b6b44-1826">New-AzStorageAccount</span></span>
* <span data-ttu-id="b6b44-1827">Ändra lagringskontots cmdlet-utdata Sku.Name för att passa med indata-SkuName genom att lägga till ”-”. Till exempel ändras ”StandardLRS” till ”Standard_LRS”</span><span class="sxs-lookup"><span data-stu-id="b6b44-1827">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="b6b44-1828">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b6b44-1828">New-AzStorageAccount</span></span>
    - <span data-ttu-id="b6b44-1829">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b6b44-1829">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="b6b44-1830">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b6b44-1830">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b6b44-1831">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b6b44-1831">Az.Websites</span></span>
* <span data-ttu-id="b6b44-1832">Egenskapen ”typ” konfigureras nu för PSSite-objekt som returneras av Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="b6b44-1832">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="b6b44-1833">Get-AzWebApp\*Metrics och Get-AzAppServicePlanMetrics markeras som inaktuella</span><span class="sxs-lookup"><span data-stu-id="b6b44-1833">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="b6b44-1834">1.8.0 – april 2019</span><span class="sxs-lookup"><span data-stu-id="b6b44-1834">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="b6b44-1835">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="b6b44-1835">Highlights since the last major release</span></span>
* <span data-ttu-id="b6b44-1836">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="b6b44-1836">General availability of `Az` module</span></span>
* <span data-ttu-id="b6b44-1837">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="b6b44-1837">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="b6b44-1838">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="b6b44-1838">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="b6b44-1839">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="b6b44-1839">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="b6b44-1840">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="b6b44-1840">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="b6b44-1841">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="b6b44-1841">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="b6b44-1842">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="b6b44-1842">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="b6b44-1843">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b6b44-1843">Az.Accounts</span></span>
* <span data-ttu-id="b6b44-1844">Uppdatera Uninstall-AzureRm för att ta bort moduler i Mac på ett korrekt sätt</span><span class="sxs-lookup"><span data-stu-id="b6b44-1844">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="b6b44-1845">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="b6b44-1845">Az.Batch</span></span>
* <span data-ttu-id="b6b44-1846">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1846">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="b6b44-1847">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="b6b44-1847">Az.Cdn</span></span>
* <span data-ttu-id="b6b44-1848">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1848">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="b6b44-1849">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="b6b44-1849">Az.CognitiveServices</span></span>
* <span data-ttu-id="b6b44-1850">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1850">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b6b44-1851">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b6b44-1851">Az.Compute</span></span>
* <span data-ttu-id="b6b44-1852">Åtgärda problem med AEM-installationen om resurs-ID:n för diskar innehåller resourcegroups i gemener i resurs-ID:n</span><span class="sxs-lookup"><span data-stu-id="b6b44-1852">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="b6b44-1853">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1853">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="b6b44-1854">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="b6b44-1854">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b6b44-1855">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b6b44-1855">Az.DataFactory</span></span>
* <span data-ttu-id="b6b44-1856">Lägg till SsisProperties om NodeCount inte är null för hanterad integreringskörning.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1856">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b6b44-1857">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b6b44-1857">Az.DataLakeStore</span></span>
* <span data-ttu-id="b6b44-1858">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1858">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="b6b44-1859">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="b6b44-1859">Az.EventGrid</span></span>
* <span data-ttu-id="b6b44-1860">Hjälptexten för slutpunkten har uppdaterats för att visa att resurser ska skapas innan cmdletarna för att skapa/uppdatera händelseprenumerationer används.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1860">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="b6b44-1861">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="b6b44-1861">Az.EventHub</span></span>
* <span data-ttu-id="b6b44-1862">Nya cmdletar har lagts till för NetworkRuleSet för namnområden</span><span class="sxs-lookup"><span data-stu-id="b6b44-1862">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="b6b44-1863">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="b6b44-1863">Az.HDInsight</span></span>
* <span data-ttu-id="b6b44-1864">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1864">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="b6b44-1865">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="b6b44-1865">Az.IotHub</span></span>
* <span data-ttu-id="b6b44-1866">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1866">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="b6b44-1867">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b6b44-1867">Az.KeyVault</span></span>
* <span data-ttu-id="b6b44-1868">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1868">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="b6b44-1869">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="b6b44-1869">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="b6b44-1870">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="b6b44-1870">Az.MachineLearning</span></span>
* <span data-ttu-id="b6b44-1871">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1871">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="b6b44-1872">Az.Media</span><span class="sxs-lookup"><span data-stu-id="b6b44-1872">Az.Media</span></span>
* <span data-ttu-id="b6b44-1873">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1873">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="b6b44-1874">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b6b44-1874">Az.Monitor</span></span>
  * <span data-ttu-id="b6b44-1875">Nya cmdletar för måttbaserad aviseringsregel i GenV2 (inte klassisk)</span><span class="sxs-lookup"><span data-stu-id="b6b44-1875">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="b6b44-1876">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="b6b44-1876">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="b6b44-1877">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="b6b44-1877">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="b6b44-1878">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="b6b44-1878">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="b6b44-1879">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="b6b44-1879">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="b6b44-1880">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="b6b44-1880">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="b6b44-1881">Monitor SDK har uppdaterats till version 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="b6b44-1881">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b6b44-1882">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b6b44-1882">Az.Network</span></span>
* <span data-ttu-id="b6b44-1883">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1883">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="b6b44-1884">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="b6b44-1884">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="b6b44-1885">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="b6b44-1885">Az.NotificationHubs</span></span>
* <span data-ttu-id="b6b44-1886">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1886">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="b6b44-1887">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="b6b44-1887">Az.OperationalInsights</span></span>
* <span data-ttu-id="b6b44-1888">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1888">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="b6b44-1889">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="b6b44-1889">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="b6b44-1890">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1890">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b6b44-1891">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b6b44-1891">Az.RecoveryServices</span></span>
* <span data-ttu-id="b6b44-1892">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1892">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="b6b44-1893">Tabellformatet för SQL i virtuella Azure-datorer har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="b6b44-1893">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="b6b44-1894">En alternativ metod för att hämta platser i AzureFileShare har lagts till</span><span class="sxs-lookup"><span data-stu-id="b6b44-1894">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="b6b44-1895">ScheduleRunDays i SchedulePolicy-objekt har uppdaterats enligt tidszon</span><span class="sxs-lookup"><span data-stu-id="b6b44-1895">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="b6b44-1896">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="b6b44-1896">Az.RedisCache</span></span>
* <span data-ttu-id="b6b44-1897">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1897">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="b6b44-1898">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b6b44-1898">Az.Resources</span></span>
* <span data-ttu-id="b6b44-1899">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="b6b44-1899">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="b6b44-1900">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b6b44-1900">Az.Sql</span></span>
* <span data-ttu-id="b6b44-1901">Ersätt Monitor SDK-beroende med vanlig kod</span><span class="sxs-lookup"><span data-stu-id="b6b44-1901">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="b6b44-1902">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1902">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="b6b44-1903">Förbättrad process för klassificering av flera kolumner.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1903">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="b6b44-1904">Inkludera SKU-egenskaper (SKU-namn, serie, kapacitet) i svaret från Get-AzSqlServerServiceObjective och formatera som tabell som standard.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1904">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="b6b44-1905">Möjlighet att använda Get-AzSqlServerServiceObjective efter plats utan att behöva en redan befintlig server i regionen.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1905">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="b6b44-1906">Stöd för tidszonsparametern när hanterade instanser skapas.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1906">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="b6b44-1907">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="b6b44-1907">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b6b44-1908">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b6b44-1908">Az.Websites</span></span>
* <span data-ttu-id="b6b44-1909">åtgärdar Set-AzWebApp och Set-AzWebAppSlot så att de inte tar bort taggar vid körning</span><span class="sxs-lookup"><span data-stu-id="b6b44-1909">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="b6b44-1910">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1910">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="b6b44-1911">SDK för WebSites har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1911">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="b6b44-1912">Egenskapen AdminSiteName har tagits bort från PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1912">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="b6b44-1913">1.7.0 – april 2019</span><span class="sxs-lookup"><span data-stu-id="b6b44-1913">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="b6b44-1914">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="b6b44-1914">Highlights since the last major release</span></span>
* <span data-ttu-id="b6b44-1915">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="b6b44-1915">General availability of `Az` module</span></span>
* <span data-ttu-id="b6b44-1916">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="b6b44-1916">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="b6b44-1917">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="b6b44-1917">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="b6b44-1918">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="b6b44-1918">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="b6b44-1919">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="b6b44-1919">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="b6b44-1920">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="b6b44-1920">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="b6b44-1921">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="b6b44-1921">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="b6b44-1922">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b6b44-1922">Az.Accounts</span></span>
* <span data-ttu-id="b6b44-1923">Add-AzEnvironment och Set-AzEnvironment har uppdaterats för att godkänna parametern AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="b6b44-1923">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="b6b44-1924">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="b6b44-1924">Az.AnalysisServices</span></span>
* <span data-ttu-id="b6b44-1925">ServiceClient används i cmdletar för dataplan och den ursprungliga autentiseringslogiken har tagits bort</span><span class="sxs-lookup"><span data-stu-id="b6b44-1925">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="b6b44-1926">Add-AzureASAccount används för omslutning av Connect-AzAccount för att undvika en icke-bakåtkompatibel ändring</span><span class="sxs-lookup"><span data-stu-id="b6b44-1926">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="b6b44-1927">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b6b44-1927">Az.Automation</span></span>
* <span data-ttu-id="b6b44-1928">Buggen för cmdleten New-AzAutomationSoftwareUpdateConfiguration för inkluderingar har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1928">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="b6b44-1929">Nu bör parametern IncludedKbNumber och IncludedPackageNameMask fungera.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1929">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="b6b44-1930">Felkorrigering för dynamiska grupper i uppdateringshanteringen för azure automation</span><span class="sxs-lookup"><span data-stu-id="b6b44-1930">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b6b44-1931">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b6b44-1931">Az.Compute</span></span>
* <span data-ttu-id="b6b44-1932">Lägg till parametern HyperVGeneration i New-AzDiskConfig och New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="b6b44-1932">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="b6b44-1933">Tillåt att virtuella datorer skapas med galleribilder från andra klientorganisationer.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1933">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="b6b44-1934">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="b6b44-1934">Az.ContainerInstance</span></span>
* <span data-ttu-id="b6b44-1935">Ett problem har åtgärdats i parametern -Command för New-AzContainerGroup som lade till ett avslutande tomt argument</span><span class="sxs-lookup"><span data-stu-id="b6b44-1935">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b6b44-1936">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b6b44-1936">Az.DataFactory</span></span>
* <span data-ttu-id="b6b44-1937">ADF .Net SDK-versionen har uppdaterats till 3.0.2</span><span class="sxs-lookup"><span data-stu-id="b6b44-1937">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="b6b44-1938">Cmdleten Set-AzDataFactoryV2 har uppdaterats med extra parametrar för inställningar som rör RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1938">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="b6b44-1939">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b6b44-1939">Az.Resources</span></span>
* <span data-ttu-id="b6b44-1940">Förbättra hanteringen av providrar för Get-AzResource när parametrarna -ResourceId eller -ResourceGroupName, -Name och -ResourceType tillhandahålls</span><span class="sxs-lookup"><span data-stu-id="b6b44-1940">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="b6b44-1941">Förbättra felhanteringen för ”Test-AzDeployment” och ”Test-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="b6b44-1941">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="b6b44-1942">Hantera fel utanför distributionsvalideringen och ta med dem i kommandoutdata istället</span><span class="sxs-lookup"><span data-stu-id="b6b44-1942">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="b6b44-1943">Mer information här: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="b6b44-1943">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="b6b44-1944">Lägg till växlingsparametern -IgnoreDynamicParameters till en uppsättning av cmdletar för distribution för att hoppa över fråga i skript och jobbscenarier</span><span class="sxs-lookup"><span data-stu-id="b6b44-1944">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="b6b44-1945">Mer information här: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="b6b44-1945">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="b6b44-1946">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b6b44-1946">Az.Sql</span></span>
* <span data-ttu-id="b6b44-1947">Stöd för dataklassificering av databaser.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1947">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b6b44-1948">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b6b44-1948">Az.Storage</span></span>
* <span data-ttu-id="b6b44-1949">Rapportera detaljfel när lagringskontext skapas med parametern -UseConnectedAccount, men utan inloggning på Azure-kontot</span><span class="sxs-lookup"><span data-stu-id="b6b44-1949">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="b6b44-1950">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="b6b44-1950">New-AzStorageContext</span></span>
* <span data-ttu-id="b6b44-1951">Stöd för att hantera Blob Service-egenskaper för ett angivet lagringskonto med API:et för hanteringsplan</span><span class="sxs-lookup"><span data-stu-id="b6b44-1951">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="b6b44-1952">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="b6b44-1952">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="b6b44-1953">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="b6b44-1953">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="b6b44-1954">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="b6b44-1954">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="b6b44-1955">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="b6b44-1955">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="b6b44-1956">Stöd för -AsJob-cmdletar för att ladda upp och ladda ned blobar och filer</span><span class="sxs-lookup"><span data-stu-id="b6b44-1956">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="b6b44-1957">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="b6b44-1957">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="b6b44-1958">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="b6b44-1958">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="b6b44-1959">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="b6b44-1959">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="b6b44-1960">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="b6b44-1960">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="b6b44-1961">1.6.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="b6b44-1961">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="b6b44-1962">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="b6b44-1962">Highlights since the last major release</span></span>
* <span data-ttu-id="b6b44-1963">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="b6b44-1963">General availability of `Az` module</span></span>
* <span data-ttu-id="b6b44-1964">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="b6b44-1964">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="b6b44-1965">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="b6b44-1965">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="b6b44-1966">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="b6b44-1966">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="b6b44-1967">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="b6b44-1967">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="b6b44-1968">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="b6b44-1968">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="b6b44-1969">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="b6b44-1969">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="b6b44-1970">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b6b44-1970">Az.Automation</span></span>
* <span data-ttu-id="b6b44-1971">Azure Automation – ändring av uppdateringshantering för stöd för de nya funktionerna:</span><span class="sxs-lookup"><span data-stu-id="b6b44-1971">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="b6b44-1972">Dynamisk gruppering</span><span class="sxs-lookup"><span data-stu-id="b6b44-1972">Dynamic grouping</span></span>
    * <span data-ttu-id="b6b44-1973">För-/efterskrift</span><span class="sxs-lookup"><span data-stu-id="b6b44-1973">Pre-Post script</span></span>
    * <span data-ttu-id="b6b44-1974">Inställning för omstart</span><span class="sxs-lookup"><span data-stu-id="b6b44-1974">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b6b44-1975">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b6b44-1975">Az.Compute</span></span>
* <span data-ttu-id="b6b44-1976">Åtgärda problem med sökvägsmatchning i Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="b6b44-1976">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="b6b44-1977">Uppdatera Compute-klientbibliotek till 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1977">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="b6b44-1978">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b6b44-1978">Az.KeyVault</span></span>
* <span data-ttu-id="b6b44-1979">Stöd för jokertecken för KeyVault-cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="b6b44-1979">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b6b44-1980">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b6b44-1980">Az.Network</span></span>
* <span data-ttu-id="b6b44-1981">Lägg till stöd för Threat Intelligence för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="b6b44-1981">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="b6b44-1982">Lägg till resurs för brandväggsprincip på översta nivå och anpassade regler för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="b6b44-1982">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b6b44-1983">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b6b44-1983">Az.RecoveryServices</span></span>
* <span data-ttu-id="b6b44-1984">SnapshotRetentionInDays har lagts till i Azure-principen för virtuella datorer för stöd av Instant RP</span><span class="sxs-lookup"><span data-stu-id="b6b44-1984">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="b6b44-1985">Pipe-stöd för avregistrering av container har lagts till</span><span class="sxs-lookup"><span data-stu-id="b6b44-1985">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="b6b44-1986">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b6b44-1986">Az.Resources</span></span>
* <span data-ttu-id="b6b44-1987">Uppdatera stöd för jokertecken för Get-AzResource och Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b6b44-1987">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="b6b44-1988">Uppdatera autentiseringsuppgifter som används vid allmänna anrop till ARM</span><span class="sxs-lookup"><span data-stu-id="b6b44-1988">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="b6b44-1989">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b6b44-1989">Az.Sql</span></span>
* <span data-ttu-id="b6b44-1990">Cmdlet-parametern (ExcludeDetectionType) för Hotidentifiering ändrades från DetectionType till sträng[] för att framtidssäkra den när nya DetectionTypes läggs till, och även för att stödja automatisk ifyllning.</span><span class="sxs-lookup"><span data-stu-id="b6b44-1990">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b6b44-1991">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b6b44-1991">Az.Storage</span></span>
* <span data-ttu-id="b6b44-1992">Stöd för att hämta/ange/ta bort hanteringsprincip på ett lagringskonto</span><span class="sxs-lookup"><span data-stu-id="b6b44-1992">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="b6b44-1993">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="b6b44-1993">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="b6b44-1994">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="b6b44-1994">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="b6b44-1995">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="b6b44-1995">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="b6b44-1996">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="b6b44-1996">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="b6b44-1997">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="b6b44-1997">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="b6b44-1998">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="b6b44-1998">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b6b44-1999">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b6b44-1999">Az.Websites</span></span>
* <span data-ttu-id="b6b44-2000">Åtgärda fel med ARM-mall som avbryter kloning av alla platser med 'New-AzWebApp -IncludeSourceWebAppSlots'</span><span class="sxs-lookup"><span data-stu-id="b6b44-2000">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="b6b44-2001">1.5.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="b6b44-2001">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b6b44-2002">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b6b44-2002">Az.Accounts</span></span>
* <span data-ttu-id="b6b44-2003">Lägg till kommandot Register-AzModule för stöd för AutoRest-genererade cmdletar</span><span class="sxs-lookup"><span data-stu-id="b6b44-2003">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="b6b44-2004">Uppdatera exempel för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="b6b44-2004">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="b6b44-2005">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b6b44-2005">Az.Automation</span></span>
* <span data-ttu-id="b6b44-2006">Problem med att hämta vissa månadsscheman i flera Azure Automation-cmdletar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="b6b44-2006">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="b6b44-2007">Åtgärda problem med att Get-AzAutomationDscNode bara returnerar de 20 översta noderna.</span><span class="sxs-lookup"><span data-stu-id="b6b44-2007">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="b6b44-2008">Nu returneras alla noder</span><span class="sxs-lookup"><span data-stu-id="b6b44-2008">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="b6b44-2009">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="b6b44-2009">Az.Cdn</span></span>
* <span data-ttu-id="b6b44-2010">Nya Powershell-cmdletar för att aktivera/inaktivera anpassade domän-HTTPS har lagts till och de gamla har gjorts inaktuella</span><span class="sxs-lookup"><span data-stu-id="b6b44-2010">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b6b44-2011">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b6b44-2011">Az.Compute</span></span>
* <span data-ttu-id="b6b44-2012">Lägg till stöd för jokertecken för Get-cmdletar</span><span class="sxs-lookup"><span data-stu-id="b6b44-2012">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b6b44-2013">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b6b44-2013">Az.DataFactory</span></span>
* <span data-ttu-id="b6b44-2014">ADF .Net SDK-versionen har uppdaterats till 3.0.1</span><span class="sxs-lookup"><span data-stu-id="b6b44-2014">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="b6b44-2015">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="b6b44-2015">Az.LogicApp</span></span>
* <span data-ttu-id="b6b44-2016">Åtgärda problemet med att ListWorkflows endast hämtar den första sidan med resultat</span><span class="sxs-lookup"><span data-stu-id="b6b44-2016">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b6b44-2017">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b6b44-2017">Az.Network</span></span>
* <span data-ttu-id="b6b44-2018">Lägg till stöd för jokertecken för Network-cmdletar</span><span class="sxs-lookup"><span data-stu-id="b6b44-2018">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b6b44-2019">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b6b44-2019">Az.RecoveryServices</span></span>
* <span data-ttu-id="b6b44-2020">Stöd har lagts till för SQL Server i virtuella Azure-datorer</span><span class="sxs-lookup"><span data-stu-id="b6b44-2020">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="b6b44-2021">SDK-uppdatering</span><span class="sxs-lookup"><span data-stu-id="b6b44-2021">SDK Update</span></span>
* <span data-ttu-id="b6b44-2022">Get-ProtectableItem-incheckning i VMappContainer har tagits bort</span><span class="sxs-lookup"><span data-stu-id="b6b44-2022">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="b6b44-2023">Name och ServerName har lagts till som parametrar för Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="b6b44-2023">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="b6b44-2024">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b6b44-2024">Az.Resources</span></span>
* <span data-ttu-id="b6b44-2025">Lägg till parametern `-TemplateObject` i cmdletar för distribution</span><span class="sxs-lookup"><span data-stu-id="b6b44-2025">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="b6b44-2026">Mer information här: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="b6b44-2026">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="b6b44-2027">Åtgärda problem med piping av resultatet i `Get-AzResource` till `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="b6b44-2027">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="b6b44-2028">Mer information här: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="b6b44-2028">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="b6b44-2029">Åtgärda problem med ändring av JSON-datatyp när `Set-AzResource` körs</span><span class="sxs-lookup"><span data-stu-id="b6b44-2029">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="b6b44-2030">Mer information här: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="b6b44-2030">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="b6b44-2031">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b6b44-2031">Az.Sql</span></span>
* <span data-ttu-id="b6b44-2032">AuditingEndpointsCommunicator uppdateras.</span><span class="sxs-lookup"><span data-stu-id="b6b44-2032">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="b6b44-2033">Åtgärdar beteendet hos ett gränsscenario när nya diagnostikinställningar skapas.</span><span class="sxs-lookup"><span data-stu-id="b6b44-2033">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b6b44-2034">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b6b44-2034">Az.Storage</span></span>
* <span data-ttu-id="b6b44-2035">Stöd för BlockBlobStorage när Storage-konto skapas      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b6b44-2035">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="b6b44-2036">1.4.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="b6b44-2036">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="b6b44-2037">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="b6b44-2037">Az.AnalysisServices</span></span>
* <span data-ttu-id="b6b44-2038">Inaktuell AddAzureASAccount-cmdlet</span><span class="sxs-lookup"><span data-stu-id="b6b44-2038">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="b6b44-2039">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b6b44-2039">Az.Automation</span></span>
* <span data-ttu-id="b6b44-2040">Hjälpen för Import-AzAutomationDscNodeConfiguration har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="b6b44-2040">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="b6b44-2041">Konfigurationsnamnsvalidering har lagts till i cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="b6b44-2041">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="b6b44-2042">Förbättrad felhantering för cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="b6b44-2042">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="b6b44-2043">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="b6b44-2043">Az.CognitiveServices</span></span>
* <span data-ttu-id="b6b44-2044">CustomSubdomainName har lagts till som en ny valfri parameter för New-AzCognitiveServicesAccount, som används för att ange underdomän för resursen.</span><span class="sxs-lookup"><span data-stu-id="b6b44-2044">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b6b44-2045">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b6b44-2045">Az.Compute</span></span>
* <span data-ttu-id="b6b44-2046">Problemet med ID-parameteruppsättningar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="b6b44-2046">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="b6b44-2047">Get-AzVMExtension har uppdaterats så att alla installerade tillägg visas om parametern Name inte har angetts</span><span class="sxs-lookup"><span data-stu-id="b6b44-2047">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="b6b44-2048">Parametrarna Tag och ResourceId har lagts till i cmdleten Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="b6b44-2048">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="b6b44-2049">Get-AzVmssVM utan instans-ID och med InstanceView kan visa virtuella VMSS-datorer med instansvyn.</span><span class="sxs-lookup"><span data-stu-id="b6b44-2049">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b6b44-2050">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b6b44-2050">Az.DataLakeStore</span></span>
* <span data-ttu-id="b6b44-2051">Cmdletar har lagts till för uppräkning och återställning av borttagna objekt i ADL</span><span class="sxs-lookup"><span data-stu-id="b6b44-2051">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="b6b44-2052">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="b6b44-2052">Az.EventHub</span></span>
* <span data-ttu-id="b6b44-2053">Ny boolesk egenskap SkipEmptyArchives har lagts till i Skip Empty Archives i CaptureDescription-klassen i Eventhub</span><span class="sxs-lookup"><span data-stu-id="b6b44-2053">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="b6b44-2054">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b6b44-2054">Az.KeyVault</span></span>
* <span data-ttu-id="b6b44-2055">Taggning i Set-AzKeyVaultSecret har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="b6b44-2055">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="b6b44-2056">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="b6b44-2056">Az.LogicApp</span></span>
* <span data-ttu-id="b6b44-2057">Grundläggande SKU har lagts till för Integrationskonton</span><span class="sxs-lookup"><span data-stu-id="b6b44-2057">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="b6b44-2058">XSLT 2.0, XSLT 3.0 och Flytande mappningstyper har lagts till</span><span class="sxs-lookup"><span data-stu-id="b6b44-2058">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="b6b44-2059">Nya cmdletar för integrationskontosammansättningar</span><span class="sxs-lookup"><span data-stu-id="b6b44-2059">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="b6b44-2060">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="b6b44-2060">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="b6b44-2061">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="b6b44-2061">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="b6b44-2062">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="b6b44-2062">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="b6b44-2063">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="b6b44-2063">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="b6b44-2064">Nya cmdletar för batchkonfiguration för integrationskonto</span><span class="sxs-lookup"><span data-stu-id="b6b44-2064">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="b6b44-2065">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="b6b44-2065">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="b6b44-2066">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="b6b44-2066">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="b6b44-2067">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="b6b44-2067">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="b6b44-2068">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="b6b44-2068">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="b6b44-2069">Logic App-SDK har uppdaterats till version 4.1.0</span><span class="sxs-lookup"><span data-stu-id="b6b44-2069">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="b6b44-2070">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b6b44-2070">Az.Monitor</span></span>
* <span data-ttu-id="b6b44-2071">Hjälpen för Get-AzMetric har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="b6b44-2071">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b6b44-2072">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b6b44-2072">Az.Network</span></span>
* <span data-ttu-id="b6b44-2073">Hjälpexempel för Add-AzApplicationGatewayCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="b6b44-2073">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="b6b44-2074">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="b6b44-2074">Az.OperationalInsights</span></span>
* <span data-ttu-id="b6b44-2075">Ytterligare stöd för datakällorna New och Get ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="b6b44-2075">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="b6b44-2076">Ny ApplicationInsights-typ har lagts till för att ge stöd för ”Get specific” och ”Get all” för ApplicationInsights-datakällor för angiven arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="b6b44-2076">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="b6b44-2077">Cmdleten New-AzOperationalInsightsApplicationInsightsDataSource har lagts till för att skapa datakälla med angivna parametrar för Application Insights-resurs: subscription Id, resourceGroupName och name.</span><span class="sxs-lookup"><span data-stu-id="b6b44-2077">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="b6b44-2078">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b6b44-2078">Az.Resources</span></span>
* <span data-ttu-id="b6b44-2079">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="b6b44-2079">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="b6b44-2080">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="b6b44-2080">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="b6b44-2081">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="b6b44-2081">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="b6b44-2082">Fel som gör att KeyCredentials inte kan skapas upprepade gånger har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="b6b44-2082">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="b6b44-2083">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b6b44-2083">Az.Sql</span></span>
* <span data-ttu-id="b6b44-2084">Lägg till stöd för hyperskalanivån för SQL DB</span><span class="sxs-lookup"><span data-stu-id="b6b44-2084">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="b6b44-2085">Ett fel har åtgärdats där återställningen kunde misslyckas på grund av onödiga inställningsegenskaper i restore-förfrågan</span><span class="sxs-lookup"><span data-stu-id="b6b44-2085">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b6b44-2086">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b6b44-2086">Az.Websites</span></span>
* <span data-ttu-id="b6b44-2087">Rätt exempel i Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="b6b44-2087">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="b6b44-2088">1.3.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="b6b44-2088">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b6b44-2089">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b6b44-2089">Az.Accounts</span></span>
* <span data-ttu-id="b6b44-2090">Uppdatera till den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="b6b44-2090">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="b6b44-2091">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="b6b44-2091">Az.AnalysisServices</span></span>
<span data-ttu-id="b6b44-2092">Allmän tillgänglighet för Az.AnalysisServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="b6b44-2092">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b6b44-2093">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b6b44-2093">Az.Compute</span></span>
* <span data-ttu-id="b6b44-2094">AEM-tillägg: Lägg till stöd för UltraSSD-, P60-, P70- och P80-diskar</span><span class="sxs-lookup"><span data-stu-id="b6b44-2094">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="b6b44-2095">Uppdatera hjälpbeskrivning för Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="b6b44-2095">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="b6b44-2096">Uppdatera hjälpbeskrivning och exempel för Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="b6b44-2096">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b6b44-2097">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b6b44-2097">Az.RecoveryServices</span></span>
<span data-ttu-id="b6b44-2098">Allmän tillgänglighet för Az.RecoveryServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="b6b44-2098">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="b6b44-2099">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b6b44-2099">Az.Resources</span></span>
* <span data-ttu-id="b6b44-2100">Korrigera taggar för resursgrupper</span><span class="sxs-lookup"><span data-stu-id="b6b44-2100">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="b6b44-2101">Mer information här: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="b6b44-2101">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="b6b44-2102">Åtgärda problem där `Get-AzureRmRoleAssignment` inte respekterar -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="b6b44-2102">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="b6b44-2103">Mer information här: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="b6b44-2103">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="b6b44-2104">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b6b44-2104">Az.Sql</span></span>
* <span data-ttu-id="b6b44-2105">Lägga till Get/Set-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="b6b44-2105">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="b6b44-2106">Åtgärda problem där ett nullref-undantag uppstår när du kör SQL-cmdletar och inte är inloggad på ett Azure-konto</span><span class="sxs-lookup"><span data-stu-id="b6b44-2106">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="b6b44-2107">Åtgärda nullref-undantag i Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="b6b44-2107">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="b6b44-2108">1.2.1 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="b6b44-2108">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b6b44-2109">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b6b44-2109">Az.Accounts</span></span>
* <span data-ttu-id="b6b44-2110">Version med rätt version av autentisering</span><span class="sxs-lookup"><span data-stu-id="b6b44-2110">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="b6b44-2111">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="b6b44-2111">Az.AnalysisServices</span></span>
* <span data-ttu-id="b6b44-2112">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="b6b44-2112">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b6b44-2113">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b6b44-2113">Az.RecoveryServices</span></span>
* <span data-ttu-id="b6b44-2114">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="b6b44-2114">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="b6b44-2115">1.2.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="b6b44-2115">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b6b44-2116">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b6b44-2116">Az.Accounts</span></span>
* <span data-ttu-id="b6b44-2117">Lägga till interaktiv autentisering och autentisering med användarnamn/lösenord för endast Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="b6b44-2117">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="b6b44-2118">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="b6b44-2118">Update incorrect online help URLs</span></span>
* <span data-ttu-id="b6b44-2119">Lägga till varningsmeddelande i PS Core för Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="b6b44-2119">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="b6b44-2120">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="b6b44-2120">Az.Aks</span></span>
* <span data-ttu-id="b6b44-2121">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="b6b44-2121">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="b6b44-2122">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b6b44-2122">Az.Automation</span></span>
* <span data-ttu-id="b6b44-2123">Stöd för Python 2-runbookflöden har lagts till</span><span class="sxs-lookup"><span data-stu-id="b6b44-2123">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="b6b44-2124">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="b6b44-2124">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="b6b44-2125">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="b6b44-2125">Az.Cdn</span></span>
* <span data-ttu-id="b6b44-2126">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="b6b44-2126">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b6b44-2127">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b6b44-2127">Az.Compute</span></span>
* <span data-ttu-id="b6b44-2128">Lägga till cmdleten Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="b6b44-2128">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="b6b44-2129">Lägga till TempDisk-parameter i Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b6b44-2129">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="b6b44-2130">Korrigera varningsmeddelande för New-AzVM</span><span class="sxs-lookup"><span data-stu-id="b6b44-2130">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="b6b44-2131">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="b6b44-2131">Az.ContainerRegistry</span></span>
* <span data-ttu-id="b6b44-2132">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="b6b44-2132">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b6b44-2133">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b6b44-2133">Az.DataFactory</span></span>
* <span data-ttu-id="b6b44-2134">ADF .Net SDK-versionen har uppdaterats till 3.0.0</span><span class="sxs-lookup"><span data-stu-id="b6b44-2134">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b6b44-2135">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b6b44-2135">Az.DataLakeStore</span></span>
* <span data-ttu-id="b6b44-2136">Åtgärda problem med ADLS-slutpunkt vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="b6b44-2136">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="b6b44-2137">Mer information här: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="b6b44-2137">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="b6b44-2138">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="b6b44-2138">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="b6b44-2139">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="b6b44-2139">Az.IotHub</span></span>
* <span data-ttu-id="b6b44-2140">Lägga till kodningsformat i cmdleten Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="b6b44-2140">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="b6b44-2141">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b6b44-2141">Az.KeyVault</span></span>
* <span data-ttu-id="b6b44-2142">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="b6b44-2142">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b6b44-2143">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b6b44-2143">Az.Network</span></span>
* <span data-ttu-id="b6b44-2144">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="b6b44-2144">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="b6b44-2145">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b6b44-2145">Az.Resources</span></span>
* <span data-ttu-id="b6b44-2146">Åtgärda felaktiga exempel i referensdokumentationen ”New-AzADAppCredential” och ”New-AzADSpCredential”</span><span class="sxs-lookup"><span data-stu-id="b6b44-2146">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="b6b44-2147">Åtgärda problem där sökvägen för parametern ”-TemplateFile” inte omvandlas innan cmdletarna för distribution i resursgruppen körs</span><span class="sxs-lookup"><span data-stu-id="b6b44-2147">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="b6b44-2148">Az.Resources: Korrigera dokumentationen om standardvärdet för New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="b6b44-2148">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="b6b44-2149">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="b6b44-2149">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="b6b44-2150">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="b6b44-2150">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="b6b44-2151">Åtgärda formateringsproblemet med objektet ”PSResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="b6b44-2151">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="b6b44-2152">Mer information här: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="b6b44-2152">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="b6b44-2153">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b6b44-2153">Az.ServiceFabric</span></span>
* <span data-ttu-id="b6b44-2154">Återställ när ett certifikat läggs till i en Virtual Machine Scale Sets-modell men ett undantag genereras. Detta har gjorts för att åtgärda följande fel: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="b6b44-2154">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="b6b44-2155">Korrigera några felmeddelanden.</span><span class="sxs-lookup"><span data-stu-id="b6b44-2155">Fix some error messages.</span></span>
* <span data-ttu-id="b6b44-2156">Korrigering av skapande av kluster med ARM-mall som är standard för New-AzServiceFabriCluster som inte fungerade med migrering till Az.</span><span class="sxs-lookup"><span data-stu-id="b6b44-2156">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="b6b44-2157">Korrigering av tilläggning av kluster/programcertifikat så att endast VM Scale Sets som motsvarar klustret läggs till genom att kontrollera ID för klustret i tillägget.</span><span class="sxs-lookup"><span data-stu-id="b6b44-2157">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="b6b44-2158">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="b6b44-2158">Az.SignalR</span></span>
* <span data-ttu-id="b6b44-2159">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="b6b44-2159">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="b6b44-2160">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b6b44-2160">Az.Sql</span></span>
* <span data-ttu-id="b6b44-2161">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="b6b44-2161">Update incorrect online help URLs</span></span>
* <span data-ttu-id="b6b44-2162">Uppdaterad parameterbeskrivning för LicenseType-parameter med möjliga värden</span><span class="sxs-lookup"><span data-stu-id="b6b44-2162">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="b6b44-2163">Korrigering för att uppdatera hanterad instansidentitet som inte fungerar när det är den enda uppdaterade egenskapen</span><span class="sxs-lookup"><span data-stu-id="b6b44-2163">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="b6b44-2164">Stöd för anpassad sortering på hanterad instans</span><span class="sxs-lookup"><span data-stu-id="b6b44-2164">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b6b44-2165">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b6b44-2165">Az.Storage</span></span>
* <span data-ttu-id="b6b44-2166">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="b6b44-2166">Update incorrect online help URLs</span></span>
* <span data-ttu-id="b6b44-2167">Tillhandahåll detaljerat felmeddelande när en användare försöker hämta/konfigurera klassisk loggning/mått på ett Premium Storage-konto eftersom Premium Storage-kontot inte har stöd för klassisk loggning/mått.</span><span class="sxs-lookup"><span data-stu-id="b6b44-2167">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="b6b44-2168">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="b6b44-2168">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="b6b44-2169">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="b6b44-2169">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="b6b44-2170">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="b6b44-2170">Az.TrafficManager</span></span>
* <span data-ttu-id="b6b44-2171">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="b6b44-2171">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b6b44-2172">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b6b44-2172">Az.Websites</span></span>
* <span data-ttu-id="b6b44-2173">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="b6b44-2173">Update incorrect online help URLs</span></span>
* <span data-ttu-id="b6b44-2174">Korrigerar ”New-AzWebAppSSLBinding” så att certifikatet laddas upp till rätt resursgrupp och plats om appen finns i en ASE.</span><span class="sxs-lookup"><span data-stu-id="b6b44-2174">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="b6b44-2175">Korrigerar ”New-AzWebAppSSLBinding” så att taggarna inte skrivs över på en bindning av ett SSL-certifikat till en app</span><span class="sxs-lookup"><span data-stu-id="b6b44-2175">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="b6b44-2176">1.1.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="b6b44-2176">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b6b44-2177">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b6b44-2177">Az.Accounts</span></span>
* <span data-ttu-id="b6b44-2178">Lade till omfattningen ”Lokal” till Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="b6b44-2178">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b6b44-2179">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b6b44-2179">Az.Compute</span></span>
* <span data-ttu-id="b6b44-2180">Namn är nu valfritt i ID-parametern för Restart/Start/Stop/Remove/Set-AzVM och Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="b6b44-2180">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="b6b44-2181">Uppdaterade beskrivningen av ID i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="b6b44-2181">Updated the description of ID in help files</span></span>
* <span data-ttu-id="b6b44-2182">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b6b44-2182">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b6b44-2183">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b6b44-2183">Az.DataLakeStore</span></span>
* <span data-ttu-id="b6b44-2184">Uppdatera sdk-versionen av dataplanet till 1.1.14 för SDK-korrigeringar.</span><span class="sxs-lookup"><span data-stu-id="b6b44-2184">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="b6b44-2185">Korrigerade hanteringen av negativ accesstime och modificationtime för getfilestatus och liststatus; korrigera asynkront annulleringstoken</span><span class="sxs-lookup"><span data-stu-id="b6b44-2185">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="b6b44-2186">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="b6b44-2186">Az.EventGrid</span></span>
* <span data-ttu-id="b6b44-2187">Uppdaterat för användning av API-versionen 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="b6b44-2187">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="b6b44-2188">Uppdaterade följande cmdletar för att stödja nytt scenario i API-versionen 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="b6b44-2188">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="b6b44-2189">New-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="b6b44-2189">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="b6b44-2190">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="b6b44-2190">Event Time-To-Live,</span></span>
        - <span data-ttu-id="b6b44-2191">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="b6b44-2191">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="b6b44-2192">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="b6b44-2192">Dead letter endpoint.</span></span>
    - <span data-ttu-id="b6b44-2193">Update-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="b6b44-2193">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="b6b44-2194">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="b6b44-2194">Event Time-To-Live,</span></span>
        - <span data-ttu-id="b6b44-2195">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="b6b44-2195">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="b6b44-2196">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="b6b44-2196">Dead letter endpoint.</span></span>
* <span data-ttu-id="b6b44-2197">Lade till nya enum-värden (storageQueue och hybridConnection) för alternativet EndpointType i cmdletarna New-AzureRmEventGridSubscription och Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="b6b44-2197">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="b6b44-2198">Visa varningsmeddelanden om skapande eller uppdatering av händelseprenumerationen förväntas medföra manuell åtgärd från användaren.</span><span class="sxs-lookup"><span data-stu-id="b6b44-2198">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="b6b44-2199">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="b6b44-2199">Az.IotHub</span></span>
* <span data-ttu-id="b6b44-2200">Har uppdaterats till den senaste versionen av SDK:n lotHub</span><span class="sxs-lookup"><span data-stu-id="b6b44-2200">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="b6b44-2201">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="b6b44-2201">Az.LogicApp</span></span>
* <span data-ttu-id="b6b44-2202">Get-AzLogicApp visar en lista över alla som inte har angivet namn</span><span class="sxs-lookup"><span data-stu-id="b6b44-2202">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="b6b44-2203">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b6b44-2203">Az.Resources</span></span>
* <span data-ttu-id="b6b44-2204">Åtgärdade problem med parameteruppsättningen när parametrarna -ODataQuery och -ResourceId anges för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="b6b44-2204">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="b6b44-2205">Mer information här: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="b6b44-2205">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="b6b44-2206">Åtgärdade hantering av parametern -Custom i New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b6b44-2206">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="b6b44-2207">Korrigerade stavfel i New-AzDeployment-dokumentationen</span><span class="sxs-lookup"><span data-stu-id="b6b44-2207">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="b6b44-2208">Gjorde parametern -MailNickname obligatorisk för New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="b6b44-2208">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="b6b44-2209">Mer information här: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="b6b44-2209">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="b6b44-2210">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="b6b44-2210">Az.SignalR</span></span>
* <span data-ttu-id="b6b44-2211">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b6b44-2211">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="b6b44-2212">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b6b44-2212">Az.Sql</span></span>
* <span data-ttu-id="b6b44-2213">Konverterade lagringshanteringsklientens beroende av den normala SDK-implementeringen.</span><span class="sxs-lookup"><span data-stu-id="b6b44-2213">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b6b44-2214">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b6b44-2214">Az.Storage</span></span>
* <span data-ttu-id="b6b44-2215">Angav StorageAccountName för lagringskontext som det verkliga namnet på lagringskontot när det skapas med Sas Token, OAuth eller Anonymous</span><span class="sxs-lookup"><span data-stu-id="b6b44-2215">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="b6b44-2216">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="b6b44-2216">New-AzStorageContext</span></span>
* <span data-ttu-id="b6b44-2217">Skapade Sas Token för Blob Snapshot-objekt med parametern -FullUri, åtgärdade den returnerade URI:n så att den blir URI för ögonblicksbild</span><span class="sxs-lookup"><span data-stu-id="b6b44-2217">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="b6b44-2218">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="b6b44-2218">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b6b44-2219">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b6b44-2219">Az.Websites</span></span>
* <span data-ttu-id="b6b44-2220">Åtgärdade en bugg i datumparsningen i Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="b6b44-2220">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="b6b44-2221">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b6b44-2221">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="b6b44-2222">1.0.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="b6b44-2222">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="b6b44-2223">Allmänt</span><span class="sxs-lookup"><span data-stu-id="b6b44-2223">General</span></span>

- <span data-ttu-id="b6b44-2224">Allmän tillgänglighet för Az-modulen</span><span class="sxs-lookup"><span data-stu-id="b6b44-2224">General Availability of Az Module</span></span>
- <span data-ttu-id="b6b44-2225">Onlinehjälp för varje modul</span><span class="sxs-lookup"><span data-stu-id="b6b44-2225">Online help for each module</span></span>
- <span data-ttu-id="b6b44-2226">Mer information och en översikt finns på [Az-informationssidan](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="b6b44-2226">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="b6b44-2227">Information om hur du migrerar från AzureRM finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="b6b44-2227">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="b6b44-2228">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b6b44-2228">Az.Accounts</span></span>
- <span data-ttu-id="b6b44-2229">Har ändrats från Az.Profile</span><span class="sxs-lookup"><span data-stu-id="b6b44-2229">Changed from Az.Profile</span></span>
- <span data-ttu-id="b6b44-2230">Fasta tabellformat för profil- och kontexttyper</span><span class="sxs-lookup"><span data-stu-id="b6b44-2230">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="b6b44-2231">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b6b44-2231">Az.ApiManagement</span></span>
- <span data-ttu-id="b6b44-2232">Korrigeringar för #7002</span><span class="sxs-lookup"><span data-stu-id="b6b44-2232">Fixes for #7002</span></span>
- <span data-ttu-id="b6b44-2233">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="b6b44-2233">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="b6b44-2234">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="b6b44-2234">Az.Batch</span></span>
- <span data-ttu-id="b6b44-2235">Lade till möjligheten att se vilken version av Azure Batch Node Agent som körs på var och en av de virtuella datorerna i en pool, via den nya egenskapen `NodeAgentInformation` på `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="b6b44-2235">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="b6b44-2236">Standarden `Caching` för `PSDataDisk` är nu `ReadWrite` i stället för `None`.</span><span class="sxs-lookup"><span data-stu-id="b6b44-2236">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="b6b44-2237">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="b6b44-2237">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="b6b44-2238">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="b6b44-2238">Az.Billing</span></span>
- <span data-ttu-id="b6b44-2239">Kombinerar cmdletarna för fakturering, förbrukning och UsageAggregates. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="b6b44-2239">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="b6b44-2240">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="b6b44-2240">Az.CognitivServices</span></span>
- <span data-ttu-id="b6b44-2241">Lade till kompletterare för SkuName och Typem som är tillgängliga i New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="b6b44-2241">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="b6b44-2242">Tog bort parameteruppsättningen GetSkusWithAccountParamSetName från Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="b6b44-2242">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="b6b44-2243">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="b6b44-2243">Az.ContainerInstance</span></span>
- <span data-ttu-id="b6b44-2244">Stöd för ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="b6b44-2244">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="b6b44-2245">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="b6b44-2245">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="b6b44-2246">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="b6b44-2246">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="b6b44-2247">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b6b44-2247">Az.DataLakeStore</span></span>
- <span data-ttu-id="b6b44-2248">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="b6b44-2248">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="b6b44-2249">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b6b44-2249">Az.Monitor</span></span>
- <span data-ttu-id="b6b44-2250">Döpte om Az.Insights till Az.Monitor och andra mindre icke-bakåtkompatibla ändringar. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="b6b44-2250">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="b6b44-2251">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b6b44-2251">Az.KeyVault</span></span>
- <span data-ttu-id="b6b44-2252">Tog bort den inaktuella egenskapen PurgeDisabled från utdatatyper</span><span class="sxs-lookup"><span data-stu-id="b6b44-2252">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="b6b44-2253">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="b6b44-2253">Az.MachineLearning</span></span>
- <span data-ttu-id="b6b44-2254">Inkluderade cmdletarna från modulen Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="b6b44-2254">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="b6b44-2255">Az.Media</span><span class="sxs-lookup"><span data-stu-id="b6b44-2255">Az.Media</span></span>
- <span data-ttu-id="b6b44-2256">Tog bort inaktuella -Tags-alias från New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="b6b44-2256">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="b6b44-2257">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b6b44-2257">Az.Network</span></span>
<span data-ttu-id="b6b44-2258">Stöd har lagts till för konfiguration av RewriteRuleSets i Application Gateway</span><span class="sxs-lookup"><span data-stu-id="b6b44-2258">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="b6b44-2259">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="b6b44-2259">New cmdlets added:</span></span>
        - <span data-ttu-id="b6b44-2260">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b6b44-2260">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="b6b44-2261">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b6b44-2261">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="b6b44-2262">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b6b44-2262">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="b6b44-2263">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b6b44-2263">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="b6b44-2264">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b6b44-2264">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="b6b44-2265">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="b6b44-2265">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="b6b44-2266">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="b6b44-2266">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="b6b44-2267">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="b6b44-2267">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="b6b44-2268">Cmdletar har uppdaterats med den valfria parametern -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b6b44-2268">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="b6b44-2269">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b6b44-2269">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="b6b44-2270">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="b6b44-2270">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="b6b44-2271">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="b6b44-2271">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="b6b44-2272">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b6b44-2272">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="b6b44-2273">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="b6b44-2273">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="b6b44-2274">New-AzureRmApplicationGatewayUrlPathMapConfig har lagt till KeyVault-stöd för Application Gateway med Identity.</span><span class="sxs-lookup"><span data-stu-id="b6b44-2274">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="b6b44-2275">Cmdletar har uppdaterats med den valfria parametern -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="b6b44-2275">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="b6b44-2276">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b6b44-2276">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="b6b44-2277">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b6b44-2277">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="b6b44-2278">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b6b44-2278">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="b6b44-2279">Cmdleten New-AzApplicationGateway har uppdaterats med den valfria parametern -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="b6b44-2279">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="b6b44-2280">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="b6b44-2280">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="b6b44-2281">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="b6b44-2281">Az.OperationalInsights</span></span>
- <span data-ttu-id="b6b44-2282">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="b6b44-2282">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="b6b44-2283">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="b6b44-2283">Az.Profile</span></span>
- <span data-ttu-id="b6b44-2284">Modulnamnet har ändrats till Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b6b44-2284">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="b6b44-2285">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b6b44-2285">Az.RecoveryServices</span></span>
- <span data-ttu-id="b6b44-2286">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="b6b44-2286">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="b6b44-2287">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b6b44-2287">Az.Resources</span></span>
- <span data-ttu-id="b6b44-2288">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="b6b44-2288">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="b6b44-2289">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b6b44-2289">Az.ServiceFabric</span></span>
- <span data-ttu-id="b6b44-2290">Stöd för specificering av certifikat efter eget namn och tumavtryck</span><span class="sxs-lookup"><span data-stu-id="b6b44-2290">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="b6b44-2291">Information om fler icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="b6b44-2291">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="b6b44-2292">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="b6b44-2292">Az.SIgnalR</span></span>
- <span data-ttu-id="b6b44-2293">Allmän tillgänglighet för PowerShell-cmdletar för SIgnalR</span><span class="sxs-lookup"><span data-stu-id="b6b44-2293">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="b6b44-2294">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b6b44-2294">Az.Sql</span></span>
- <span data-ttu-id="b6b44-2295">Lade till de nya identifieringstyperna Data_Exfiltration och Unsafe_Action i Threat Detection-cmdletar</span><span class="sxs-lookup"><span data-stu-id="b6b44-2295">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="b6b44-2296">Uppdaterade dokumentationsexempel för Sql Auditing-cmdletar</span><span class="sxs-lookup"><span data-stu-id="b6b44-2296">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="b6b44-2297">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="b6b44-2297">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="b6b44-2298">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b6b44-2298">Az.Storage</span></span>
- <span data-ttu-id="b6b44-2299">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="b6b44-2299">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="b6b44-2300">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b6b44-2300">Az.Websites</span></span>
- <span data-ttu-id="b6b44-2301">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="b6b44-2301">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="b6b44-2302">0.7.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="b6b44-2302">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="b6b44-2303">Allmänt</span><span class="sxs-lookup"><span data-stu-id="b6b44-2303">General</span></span>

* <span data-ttu-id="b6b44-2304">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="b6b44-2304">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="b6b44-2305">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b6b44-2305">Az.Compute</span></span>

* <span data-ttu-id="b6b44-2306">Lade till stöd för UltraSSD och Galleriavbildningar i de enkla parameteruppsättningarna för `New-AzVm(ss)`-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="b6b44-2306">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="b6b44-2307">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b6b44-2307">Az.DataLakeStore</span></span>

* <span data-ttu-id="b6b44-2308">Åtgärdade avslutande snedstreck i domänen för adls-konto</span><span class="sxs-lookup"><span data-stu-id="b6b44-2308">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="b6b44-2309">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="b6b44-2309">Az.FrontDoor</span></span>

* <span data-ttu-id="b6b44-2310">Brutna länkar korrigerades</span><span class="sxs-lookup"><span data-stu-id="b6b44-2310">Fixed some broken links</span></span>
    - <span data-ttu-id="b6b44-2311">I artiklarna New-AzureRmFrontDoor och Set-AzureRmFrontDoor artiklar korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="b6b44-2311">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="b6b44-2312">I artikeln New-AzureRmFrontDoorManagedRuleObject korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="b6b44-2312">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="b6b44-2313">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b6b44-2313">Az.RecoveryServices</span></span>

* <span data-ttu-id="b6b44-2314">Lade till valideringar på klientsidan för Azure-filresurs med återställningsåtgärder.</span><span class="sxs-lookup"><span data-stu-id="b6b44-2314">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="b6b44-2315">Gjorde storageAccountName och storageAccountResourceGroupName valfritt för afs-återställning.</span><span class="sxs-lookup"><span data-stu-id="b6b44-2315">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="b6b44-2316">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b6b44-2316">Az.Resources</span></span>

* <span data-ttu-id="b6b44-2317">Korrigering för https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="b6b44-2317">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="b6b44-2318">Uppdaterade Get-AzureRmRoleAssignment så att prenumerationsomfattningen används om den anges vid begäran om klassiska administratörer.</span><span class="sxs-lookup"><span data-stu-id="b6b44-2318">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="b6b44-2319">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b6b44-2319">Az.Sql</span></span>

* <span data-ttu-id="b6b44-2320">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="b6b44-2320">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="b6b44-2321">Korrigerade ett problem med Get-AzureRmSqlDatabaseVulnerabilityAssessment med DotNet-kärna</span><span class="sxs-lookup"><span data-stu-id="b6b44-2321">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="b6b44-2322">Ändrade dokumentationen för hjälpmeddelanden som rör SQL Auditing-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="b6b44-2322">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="b6b44-2323">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b6b44-2323">Az.Storage</span></span>

* <span data-ttu-id="b6b44-2324">Lade till -EnableHierarchicalNamespace i New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b6b44-2324">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="b6b44-2325">Åtgärdade problemet med att cmdleten Copy File inte kunde återanvända källkontexten på målet om inte -DestContext angetts</span><span class="sxs-lookup"><span data-stu-id="b6b44-2325">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="b6b44-2326">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="b6b44-2326">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="b6b44-2327">Stöd för statisk webbplatskonfiguration</span><span class="sxs-lookup"><span data-stu-id="b6b44-2327">Support Static Website configuration</span></span>
    - <span data-ttu-id="b6b44-2328">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="b6b44-2328">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="b6b44-2329">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="b6b44-2329">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="b6b44-2330">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b6b44-2330">Az.Websites</span></span>

* <span data-ttu-id="b6b44-2331">Set-AzureRmWebApp och Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b6b44-2331">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="b6b44-2332">Ny parameter (-AzureStoragePath) har lagts till för att ange att Azure Storage-sökvägar ska monteras i containerappar i Windows och Linux.</span><span class="sxs-lookup"><span data-stu-id="b6b44-2332">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="b6b44-2333">Använder utdata från den nya cmdleten New-AzureRmWebAppAzureStoragePath som en parameter för att ange sökvägar för Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="b6b44-2333">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="b6b44-2334">0.6.1 – november 2018</span><span class="sxs-lookup"><span data-stu-id="b6b44-2334">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="b6b44-2335">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b6b44-2335">Az.ApiManagement</span></span>
* <span data-ttu-id="b6b44-2336">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="b6b44-2336">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="b6b44-2337">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b6b44-2337">Az.Automation</span></span>
* <span data-ttu-id="b6b44-2338">Swagger baserade Azure Automation-cmdletar</span><span class="sxs-lookup"><span data-stu-id="b6b44-2338">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="b6b44-2339">Cmdletar för Uppdateringshantering har lagts till</span><span class="sxs-lookup"><span data-stu-id="b6b44-2339">Added Update Management cmdlets</span></span>
* <span data-ttu-id="b6b44-2340">Cmdletar för källkontroll har lagts till</span><span class="sxs-lookup"><span data-stu-id="b6b44-2340">Added Source Control cmdlets</span></span>
* <span data-ttu-id="b6b44-2341">Remove-AzureRmAutomationHybridWorkerGroup-cmdlet har lagts till</span><span class="sxs-lookup"><span data-stu-id="b6b44-2341">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="b6b44-2342">Kommandot för DSC-registreringsnod har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="b6b44-2342">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="b6b44-2343">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b6b44-2343">Az.Compute</span></span>
* <span data-ttu-id="b6b44-2344">Problem med SystemAssigned-identitet har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="b6b44-2344">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="b6b44-2345">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="b6b44-2345">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="b6b44-2346">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="b6b44-2346">Az.ContainerInstance</span></span>
* <span data-ttu-id="b6b44-2347">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="b6b44-2347">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="b6b44-2348">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="b6b44-2348">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="b6b44-2349">uppdatera exempelbeskrivningen för marketplace-cmdletar</span><span class="sxs-lookup"><span data-stu-id="b6b44-2349">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="b6b44-2350">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b6b44-2350">Az.Network</span></span>
* <span data-ttu-id="b6b44-2351">Cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomErreller Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="b6b44-2351">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="b6b44-2352">ICMP tillbaka till stöd för Azure Firewall-nätverksprotokoll har lagts till</span><span class="sxs-lookup"><span data-stu-id="b6b44-2352">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="b6b44-2353">Uppdatera cmdlet Test-AzureRmNetworkWatcherConnectivity, lägga till verifiering av mål-id, adress och port.</span><span class="sxs-lookup"><span data-stu-id="b6b44-2353">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="b6b44-2354">Åtgärda problem med minnesanvändning i VirtualNetwork-karta</span><span class="sxs-lookup"><span data-stu-id="b6b44-2354">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="b6b44-2355">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="b6b44-2355">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="b6b44-2356">Åtgärda för att ändra principen för en skyddad fildelning.</span><span class="sxs-lookup"><span data-stu-id="b6b44-2356">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="b6b44-2357">Tidszonsprincipen har konverterats till versaler.</span><span class="sxs-lookup"><span data-stu-id="b6b44-2357">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="b6b44-2358">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="b6b44-2358">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="b6b44-2359">Exempel i New-AzureRmRecoveryServicesAsrProtectableItem har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="b6b44-2359">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="b6b44-2360">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="b6b44-2360">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="b6b44-2361">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="b6b44-2361">Az.Relay</span></span>
* <span data-ttu-id="b6b44-2362">Valfri parameter -KeyValue till New-AzureRmRelayKey cmdlet har lagts till, vilket gör det möjligt för användare att tillhandahålla KeyValue.</span><span class="sxs-lookup"><span data-stu-id="b6b44-2362">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="b6b44-2363">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b6b44-2363">Az.Resources</span></span>
* <span data-ttu-id="b6b44-2364">Uppdatera hjälpdokumentation för resursidentitet kopplad till parametrar i `New-AzureRmPolicyAssignment` och `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="b6b44-2364">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="b6b44-2365">Lägg till ett exempel för New-AzureRmPolicyDefinition som använder -Metadata</span><span class="sxs-lookup"><span data-stu-id="b6b44-2365">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="b6b44-2366">Korrigera så att skiftläge behålls i taggnycklar i NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="b6b44-2366">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="b6b44-2367">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b6b44-2367">Az.ServiceFabric</span></span>
* <span data-ttu-id="b6b44-2368">Lägg till utfasningsmeddelanden för kommande icke-kompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="b6b44-2368">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="b6b44-2369">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b6b44-2369">Az.Sql</span></span>
* <span data-ttu-id="b6b44-2370">Nya cmdletar för CRUD-åtgärder på Azure Sql Database-hanterad instans och Azure Sql-hanterad databas</span><span class="sxs-lookup"><span data-stu-id="b6b44-2370">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="b6b44-2371">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="b6b44-2371">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="b6b44-2372">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="b6b44-2372">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="b6b44-2373">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="b6b44-2373">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="b6b44-2374">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="b6b44-2374">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="b6b44-2375">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="b6b44-2375">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="b6b44-2376">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="b6b44-2376">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="b6b44-2377">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="b6b44-2377">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="b6b44-2378">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="b6b44-2378">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="b6b44-2379">Hantering av utökad granskningsprincip på en server eller en databas har aktiverats.</span><span class="sxs-lookup"><span data-stu-id="b6b44-2379">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="b6b44-2380">Ny parameter (PredicateExpression) har lagts till för att aktivera filtrering av granskningsloggar.</span><span class="sxs-lookup"><span data-stu-id="b6b44-2380">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="b6b44-2381">Cmdletar har ändrats så att de använder SQL-klienter i stället för äldre klienter.</span><span class="sxs-lookup"><span data-stu-id="b6b44-2381">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="b6b44-2382">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="b6b44-2382">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="b6b44-2383">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="b6b44-2383">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="b6b44-2384">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="b6b44-2384">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="b6b44-2385">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="b6b44-2385">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="b6b44-2386">Problem med att använda Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings med lagringskontots namnparameter har korrigerats</span><span class="sxs-lookup"><span data-stu-id="b6b44-2386">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="b6b44-2387">0.5.0 – november 2018</span><span class="sxs-lookup"><span data-stu-id="b6b44-2387">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="b6b44-2388">Allmänt</span><span class="sxs-lookup"><span data-stu-id="b6b44-2388">General</span></span>
* <span data-ttu-id="b6b44-2389">Lade till resurskompletterare till många kärn-cmdletar – dessa gör att du kan stega genom befintliga resursnamn med TABB vid interaktiva anrop till cmdletar</span><span class="sxs-lookup"><span data-stu-id="b6b44-2389">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="b6b44-2390">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="b6b44-2390">Az.Profile</span></span>
* <span data-ttu-id="b6b44-2391">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="b6b44-2391">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="b6b44-2392">Bytte namn på parametern TenantId i cmdleten Connect-AzAccount till Tenant och lade till ett alias för TenantId</span><span class="sxs-lookup"><span data-stu-id="b6b44-2392">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="b6b44-2393">Uppdaterade TenantId-beskrivningen för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="b6b44-2393">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="b6b44-2394">Åtgärda felmeddelande för misslyckad inloggning när du tillhandahåller klientdomän</span><span class="sxs-lookup"><span data-stu-id="b6b44-2394">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="b6b44-2395">Åtgärda problem med att kontextnamn hamnar i konflikt för konton utan prenumerationer i klientorganisationen</span><span class="sxs-lookup"><span data-stu-id="b6b44-2395">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="b6b44-2396">Åtgärda problem med DataLake-slutpunkter vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="b6b44-2396">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="b6b44-2397">Åtgärdade problem med att Disconnect-AzAccount kastades om den inte anslöts</span><span class="sxs-lookup"><span data-stu-id="b6b44-2397">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="b6b44-2398">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="b6b44-2398">Az.CognitiveServices</span></span>
* <span data-ttu-id="b6b44-2399">Lade till åtgärden Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="b6b44-2399">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b6b44-2400">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b6b44-2400">Az.Compute</span></span>
* <span data-ttu-id="b6b44-2401">Lade till cmdletarna Add-AzVmssVMDataDisk och Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="b6b44-2401">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="b6b44-2402">Get-AzVMImage visar AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="b6b44-2402">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="b6b44-2403">Åtgärdade att värdena för alternativen SetAzVMChefExtension -BootstrapOptions och -JsonAttribute inte angavs i json-format.</span><span class="sxs-lookup"><span data-stu-id="b6b44-2403">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b6b44-2404">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b6b44-2404">Az.DataLakeStore</span></span>
* <span data-ttu-id="b6b44-2405">Uppdatera DataLake-paketet till 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="b6b44-2405">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="b6b44-2406">Lägg till standardsamtidighet för flertrådade åtgärder.</span><span class="sxs-lookup"><span data-stu-id="b6b44-2406">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="b6b44-2407">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="b6b44-2407">Az.Insights</span></span>
* <span data-ttu-id="b6b44-2408">Åtgärdade problem #7267 (autoskalningsområde)</span><span class="sxs-lookup"><span data-stu-id="b6b44-2408">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="b6b44-2409">Problem med att uppräknade parametrar inte ställdes in ordentligt när du skapade en ny autoskalningsregel (de ställdes alltid in med standardvärdet).</span><span class="sxs-lookup"><span data-stu-id="b6b44-2409">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="b6b44-2410">Åtgärdade problem #7513 [Insights] Set-AzDiagnosticSetting kräver uttrycklig specifikation av kategorier när inställningar skapas</span><span class="sxs-lookup"><span data-stu-id="b6b44-2410">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="b6b44-2411">Nu kräver inte cmdleten uttrycklig anvisning av kategorierna för att aktiveras under skapande, d.v.s. den fungerar enligt beskrivning</span><span class="sxs-lookup"><span data-stu-id="b6b44-2411">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b6b44-2412">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b6b44-2412">Az.Network</span></span>
* <span data-ttu-id="b6b44-2413">PeeringType ändrades till en obligatorisk parameter för följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="b6b44-2413">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="b6b44-2414">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="b6b44-2414">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="b6b44-2415">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="b6b44-2415">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="b6b44-2416">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="b6b44-2416">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="b6b44-2417">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="b6b44-2417">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="b6b44-2418">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="b6b44-2418">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="b6b44-2419">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="b6b44-2419">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="b6b44-2420">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="b6b44-2420">Az.PolicyInsights</span></span>
* <span data-ttu-id="b6b44-2421">Cmdletar för principreparation har lagts till</span><span class="sxs-lookup"><span data-stu-id="b6b44-2421">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="b6b44-2422">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b6b44-2422">Az.Resources</span></span>
* <span data-ttu-id="b6b44-2423">Korrigering för https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="b6b44-2423">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="b6b44-2424">Tillåt att resurser listas med parametern -ResourceId för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="b6b44-2424">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="b6b44-2425">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="b6b44-2425">Az.ServiceBus</span></span>
* <span data-ttu-id="b6b44-2426">Skrivskyddad MigrationState-egenskap har lagts till i PSServiceBusMigrationConfigurationAttributes, som hjälper till att hålla koll på migreringstillståndet.</span><span class="sxs-lookup"><span data-stu-id="b6b44-2426">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="b6b44-2427">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b6b44-2427">Az.ServiceFabric</span></span>
* <span data-ttu-id="b6b44-2428">Åtgärda att lägga till certifikat till Linux-Vmss.</span><span class="sxs-lookup"><span data-stu-id="b6b44-2428">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="b6b44-2429">Åtgärdade Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="b6b44-2429">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="b6b44-2430">Använd rätt tumavtryck från nya certifikat (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="b6b44-2430">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="b6b44-2431">Visa undantag korrekt (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="b6b44-2431">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="b6b44-2432">Åtgärdade Update-AzServiceFabricDurability så att klusterkonfigurationen uppdateras innan Vmss-åtgärden CreateOrUpdate påbörjas.</span><span class="sxs-lookup"><span data-stu-id="b6b44-2432">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="b6b44-2433">0.4.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="b6b44-2433">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="b6b44-2434">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="b6b44-2434">Az.Profile</span></span>
* <span data-ttu-id="b6b44-2435">Åtgärdade problemet med Get-AzSubscription i CloudShell</span><span class="sxs-lookup"><span data-stu-id="b6b44-2435">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="b6b44-2436">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="b6b44-2436">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b6b44-2437">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b6b44-2437">Az.Compute</span></span>
* <span data-ttu-id="b6b44-2438">Nya storlekar lades till i listan över godkända VM-storlekar för vilka accelererat nätverk kommer att aktiveras vid användning av den enkla parameteruppsättningen för New-AzVm</span><span class="sxs-lookup"><span data-stu-id="b6b44-2438">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="b6b44-2439">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="b6b44-2439">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b6b44-2440">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b6b44-2440">Az.DataLakeStore</span></span>
* <span data-ttu-id="b6b44-2441">Lägger till stöd för regler för virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="b6b44-2441">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="b6b44-2442">Get-AzDataLakeStoreVirtualNetworkRule: Hämtar eller listar regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="b6b44-2442">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="b6b44-2443">Add-AzDataLakeStoreVirtualNetworkRule: Lägger till en regel för virtuellt nätverk i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="b6b44-2443">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="b6b44-2444">Set-AzDataLakeStoreVirtualNetworkRule: Ändrar den angivna regeln för virtuellt nätverk i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="b6b44-2444">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="b6b44-2445">Remove-AzDataLakeStoreVirtualNetworkRule: Tar bort en regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="b6b44-2445">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b6b44-2446">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b6b44-2446">Az.Network</span></span>
* <span data-ttu-id="b6b44-2447">Skicka protokollvärdet till serverdelen för att uppdatera cmdleten Test-AzNetworkWatcherConnectivity.</span><span class="sxs-lookup"><span data-stu-id="b6b44-2447">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="b6b44-2448">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="b6b44-2448">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="b6b44-2449">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b6b44-2449">Az.Resources</span></span>
* <span data-ttu-id="b6b44-2450">Åtgärdade problem där Get-AzRoleDefinition genererar ett oläsligt undantag (när standardprofilen inte innehåller någon prenumeration och ingen omfattning har angetts) genom att lägga till ett beskrivande undantag i scenariot.</span><span class="sxs-lookup"><span data-stu-id="b6b44-2450">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="b6b44-2451">Ställ in ”RoleDefinitionNameParameterSet” som standardparameteruppsättning.</span><span class="sxs-lookup"><span data-stu-id="b6b44-2451">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="b6b44-2452">0.3.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="b6b44-2452">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="b6b44-2453">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="b6b44-2453">Azure.Storage</span></span>
* <span data-ttu-id="b6b44-2454">Åtgärda fel där Kopiera blob/fil inte kopierar metadata när målplatsen har ett problem med metadata</span><span class="sxs-lookup"><span data-stu-id="b6b44-2454">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="b6b44-2455">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="b6b44-2455">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="b6b44-2456">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="b6b44-2456">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="b6b44-2457">Stöd för att hämta användningsinformation om en Storage-resurs för en specifik plats och för att lägga till ett varningsmeddelande för att hämta användningsinformation om en global Storage-resurs är inaktuellt.</span><span class="sxs-lookup"><span data-stu-id="b6b44-2457">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="b6b44-2458">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="b6b44-2458">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="b6b44-2459">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="b6b44-2459">Az.CognitiveServices</span></span>
* <span data-ttu-id="b6b44-2460">Stöd för Get-AzCognitiveServicesAccountSkus utan ett befintligt konto.</span><span class="sxs-lookup"><span data-stu-id="b6b44-2460">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b6b44-2461">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b6b44-2461">Az.Compute</span></span>
* <span data-ttu-id="b6b44-2462">Åtgärdade fel där Get-AzVM -ResourceGroupName <rg> returnerar fler än 50 resultat om det behövs</span><span class="sxs-lookup"><span data-stu-id="b6b44-2462">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="b6b44-2463">Lade till ett exempel för SimpleParameterSet i hjälpen för cmdleten New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="b6b44-2463">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="b6b44-2464">Ett stavfel i förloppsmeddelandet för Azure Disk Encryption har korrigerats</span><span class="sxs-lookup"><span data-stu-id="b6b44-2464">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="b6b44-2465">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="b6b44-2465">Az.DataFactoryV2</span></span>
* <span data-ttu-id="b6b44-2466">ADF .Net SDK-versionen har uppdaterats till 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="b6b44-2466">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b6b44-2467">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b6b44-2467">Az.Network</span></span>
* <span data-ttu-id="b6b44-2468">Funktionalitet för NetworkProfile har lagts till.</span><span class="sxs-lookup"><span data-stu-id="b6b44-2468">Added NetworkProfile functionality.</span></span> <span data-ttu-id="b6b44-2469">nya cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="b6b44-2469">new cmdlets added</span></span>
    - <span data-ttu-id="b6b44-2470">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b6b44-2470">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="b6b44-2471">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b6b44-2471">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="b6b44-2472">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b6b44-2472">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="b6b44-2473">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b6b44-2473">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="b6b44-2474">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="b6b44-2474">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="b6b44-2475">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="b6b44-2475">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="b6b44-2476">Länk för tjänstassociering på modell för undernät har lagts till</span><span class="sxs-lookup"><span data-stu-id="b6b44-2476">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="b6b44-2477">Cmdletarna New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap och Remove-AzVirtualNetworkTap har lagts till</span><span class="sxs-lookup"><span data-stu-id="b6b44-2477">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="b6b44-2478">Cmdletarna Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig och Remove-AzNEtworkInterfaceTapConfig har lagts till</span><span class="sxs-lookup"><span data-stu-id="b6b44-2478">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="b6b44-2479">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="b6b44-2479">Az.RedisCache</span></span>
* <span data-ttu-id="b6b44-2480">Tillåt att alla strängar används som storleksparametrar framöver.</span><span class="sxs-lookup"><span data-stu-id="b6b44-2480">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="b6b44-2481">Lägg till P5 i popup-fönstret PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="b6b44-2481">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="b6b44-2482">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b6b44-2482">Az.Resources</span></span>
* <span data-ttu-id="b6b44-2483">Parametern -Mode som saknades i Set-AzPolicyDefinition har lagts till</span><span class="sxs-lookup"><span data-stu-id="b6b44-2483">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="b6b44-2484">Åtgärdade buggen för cmdleten Get-AzProviderOperation för åtgärder med ursprung som innehåller användare</span><span class="sxs-lookup"><span data-stu-id="b6b44-2484">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="b6b44-2485">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b6b44-2485">Az.Sql</span></span>
* <span data-ttu-id="b6b44-2486">Ett problem där vissa cmdletar för säkerhetskopiering inte kunde identifiera den aktuella azure-prenumerationen har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="b6b44-2486">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b6b44-2487">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b6b44-2487">Az.Websites</span></span>
* <span data-ttu-id="b6b44-2488">Ny cmdlet: Get-AzWebAppContainerContinuousDeploymentUrl – Hämtar webhook-URL:en för kontinuerlig distribution av container</span><span class="sxs-lookup"><span data-stu-id="b6b44-2488">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="b6b44-2489">Nya cmdletar: New-AzWebAppContainerPSSession och Enter-WebAppContainerPSSession – Startar en PowerShell-fjärrsession i en containerapp för windows</span><span class="sxs-lookup"><span data-stu-id="b6b44-2489">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="b6b44-2490">0.2.0 – september 2018</span><span class="sxs-lookup"><span data-stu-id="b6b44-2490">0.2.0 - September 2018</span></span>
 <span data-ttu-id="b6b44-2491">Första versionen</span><span class="sxs-lookup"><span data-stu-id="b6b44-2491">Initial Release</span></span>
