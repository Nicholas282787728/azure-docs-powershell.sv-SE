---
title: Viktig information om Azure PowerShell
description: Lär dig mer om alla de senaste uppdateringarna för Azure PowerShell-modulerna.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 01/09/2020
ms.openlocfilehash: 4c7ea19a225d63307ecf4a6fe5ebfa14ccd78d7e
ms.sourcegitcommit: f6fa6543be1e0f6330b1598f01528b2928cc426c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/10/2020
ms.locfileid: "79036169"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="20708-103">Viktig information om Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="20708-103">Azure PowerShell release notes</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="20708-104">3.6.1 – mars 2020</span><span class="sxs-lookup"><span data-stu-id="20708-104">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="20708-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="20708-105">Az.Accounts</span></span>
* <span data-ttu-id="20708-106">Öppna sidan med Azure PowerShell-enkäten i ”Send-Feedback” [#11020]</span><span class="sxs-lookup"><span data-stu-id="20708-106">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="20708-107">Visa URL:en för Azure PowerShell-enkäten i ”Resolve-Error” [#11021]</span><span class="sxs-lookup"><span data-stu-id="20708-107">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="20708-108">Az-version har lagts till i UserAgent</span><span class="sxs-lookup"><span data-stu-id="20708-108">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="20708-109">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="20708-109">Az.ApiManagement</span></span>
* <span data-ttu-id="20708-110">Stöd har lagts till för att hämta och konfigurera en anpassad domän på DeveloperPortal-slutpunkten [#11007]</span><span class="sxs-lookup"><span data-stu-id="20708-110">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="20708-111">”Export-AzApiManagementApi” Stöd har lagts till för att ladda ned API-definition i Json-format [#9987]</span><span class="sxs-lookup"><span data-stu-id="20708-111">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="20708-112">”Import-AzApiManagementApi” Stöd har lagts till för att importera OpenApi 3.0-definition från Json-dokument</span><span class="sxs-lookup"><span data-stu-id="20708-112">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="20708-113">”New-AzApiManagementIdentityProvider” och ”Set-AzApiManagementIdentityProvider” Stöd har lagts till för att konfigurera ”Signin Tenant” för AAD B2C-provider [#9784]</span><span class="sxs-lookup"><span data-stu-id="20708-113">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="20708-114">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="20708-114">Az.DataLakeStore</span></span>
* <span data-ttu-id="20708-115">En referens har uttryckligen lagts till för System.Buffers i csproj och psd1.</span><span class="sxs-lookup"><span data-stu-id="20708-115">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="20708-116">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="20708-116">Az.IotHub</span></span>
* <span data-ttu-id="20708-117">Lade till stöd för att hantera enheter i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="20708-117">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="20708-118">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="20708-118">New Cmdlets are:</span></span>
    - <span data-ttu-id="20708-119">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="20708-119">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="20708-120">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="20708-120">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="20708-121">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="20708-121">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="20708-122">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="20708-122">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="20708-123">Stöd har lagts till för att hantera moduler på en mål-IoT-enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="20708-123">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="20708-124">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="20708-124">New Cmdlets are:</span></span>
    - <span data-ttu-id="20708-125">”Add-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="20708-125">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="20708-126">”Get-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="20708-126">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="20708-127">”Remove-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="20708-127">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="20708-128">”Set-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="20708-128">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="20708-129">Cmdlet har lagts till för att hämta anslutningssträngen för en mål-IoT-enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="20708-129">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="20708-130">Cmdlet har lagts till för att hämta anslutningssträngen för en modul på en mål-IoT-enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="20708-130">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="20708-131">Stöd har lagts till för att hämta/ange en överordnad enhet för en IoT-enhet.</span><span class="sxs-lookup"><span data-stu-id="20708-131">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="20708-132">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="20708-132">New Cmdlets are:</span></span>
    - <span data-ttu-id="20708-133">”Get-AzIotHubDeviceParent”</span><span class="sxs-lookup"><span data-stu-id="20708-133">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="20708-134">”Set-AzIotHubDeviceParent”</span><span class="sxs-lookup"><span data-stu-id="20708-134">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="20708-135">Stöd har lagts till för att hantera en enhets överordnade och underordnade relationer.</span><span class="sxs-lookup"><span data-stu-id="20708-135">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="20708-136">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="20708-136">Az.Monitor</span></span>
* <span data-ttu-id="20708-137">Utdatavärdet har åtgärdats för ”Get-AzMetricDefinition” [#9714]</span><span class="sxs-lookup"><span data-stu-id="20708-137">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="20708-138">Az.Network</span><span class="sxs-lookup"><span data-stu-id="20708-138">Az.Network</span></span>
* <span data-ttu-id="20708-139">SQL Management SDK har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="20708-139">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="20708-140">Ett problem har åtgärdats med namngivningsskillnader i klassen PrivateLinkServiceConnectionState.</span><span class="sxs-lookup"><span data-stu-id="20708-140">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="20708-141">Fältet ActionsRequired mappar till ActionRequired.</span><span class="sxs-lookup"><span data-stu-id="20708-141">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="20708-142">PublicNetworkAccess har lagts till i ”New-AzSqlServer” och ”Set-AzSqlServer”</span><span class="sxs-lookup"><span data-stu-id="20708-142">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="20708-143">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="20708-143">Az.Resources</span></span>
* <span data-ttu-id="20708-144">Null-referensfel har åtgärdats i ”Get-AzRoleAssignment”</span><span class="sxs-lookup"><span data-stu-id="20708-144">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="20708-145">Växlarna ”-Force” och ”-PassThru” är valfria i ”Remove-AzADGroup” [#10849]</span><span class="sxs-lookup"><span data-stu-id="20708-145">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="20708-146">Ett problem har åtgärdats som gjorde att ”MailNickname” inte returnerades i ”Remove-AzADGroup” [#11167]</span><span class="sxs-lookup"><span data-stu-id="20708-146">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="20708-147">Ett problem har åtgärdats som gjorde att pipe-åtgärden ”Remove-AzADGroup” inte fungerar [#11171]</span><span class="sxs-lookup"><span data-stu-id="20708-147">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="20708-148">Ett null-referensfel har åtgärdats i GetAzureRoleAssignmentCommand</span><span class="sxs-lookup"><span data-stu-id="20708-148">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="20708-149">Attribut för icke-bakåtkompatibla ändringar har lagts till för kommande ändringar i cmdlets för principer</span><span class="sxs-lookup"><span data-stu-id="20708-149">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="20708-150">”Get-AzResourceGroup” har uppdaterats för att utföra taggfiltrering för resursgrupper på serversidan</span><span class="sxs-lookup"><span data-stu-id="20708-150">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="20708-151">Utökade Tag-cmdlets stöder -ResourceId</span><span class="sxs-lookup"><span data-stu-id="20708-151">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="20708-152">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="20708-152">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="20708-153">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="20708-153">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="20708-154">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="20708-154">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="20708-155">Ny Tag-cmdlet har lagts till</span><span class="sxs-lookup"><span data-stu-id="20708-155">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="20708-156">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="20708-156">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="20708-157">Flyttade ScopedDeployment från SDK 3.3.0</span><span class="sxs-lookup"><span data-stu-id="20708-157">Brought ScopedDeployment from SDK 3.3.0</span></span> 

#### <a name="azsql"></a><span data-ttu-id="20708-158">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="20708-158">Az.Sql</span></span>
* <span data-ttu-id="20708-159">PublicNetworkAccess har lagts till i ”New-AzSqlServer” och ”Set-AzSqlServer”</span><span class="sxs-lookup"><span data-stu-id="20708-159">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="20708-160">Stöd har lagts till för konfiguration av säkerhetskopiering för långsiktig kvarhållning för hanterade databaser</span><span class="sxs-lookup"><span data-stu-id="20708-160">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="20708-161">Hämta/ange LTR-princip på en hanterad databas</span><span class="sxs-lookup"><span data-stu-id="20708-161">Get/Set LTR policy on a managed database</span></span> 
    - <span data-ttu-id="20708-162">Hämta LTR-säkerhetskopior efter hanterad databas, hanterad instans eller plats</span><span class="sxs-lookup"><span data-stu-id="20708-162">Get LTR backup(s) by managed database, managed instance, or by location</span></span> 
    - <span data-ttu-id="20708-163">Ta bort en LTR-säkerhetskopia</span><span class="sxs-lookup"><span data-stu-id="20708-163">Remove an LTR backup</span></span> 
    - <span data-ttu-id="20708-164">Återställa en LTR-säkerhetskopia för att skapa en ny hanterad databas</span><span class="sxs-lookup"><span data-stu-id="20708-164">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="20708-165">MinimalTlsVersion har lagts till för New-AzSqlServer och Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="20708-165">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="20708-166">MinimalTlsVersion har lagts till för New-AzSqlInstance och Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="20708-166">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="20708-167">SQL SDK-versionen för Az.Network har ändrats</span><span class="sxs-lookup"><span data-stu-id="20708-167">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="20708-168">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="20708-168">Az.Storage</span></span>
* <span data-ttu-id="20708-169">AllowProtectedAppendWrite stöds i ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="20708-169">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="20708-170">”Set-AzRmStorageContainerImmutabilityPolicy”</span><span class="sxs-lookup"><span data-stu-id="20708-170">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="20708-171">Varningsmeddelande har lagts till om icke-bakåtkompatibel ändring för ändring av typen AzureStorageTable i en senare version</span><span class="sxs-lookup"><span data-stu-id="20708-171">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="20708-172">”New-AzStorageTable”</span><span class="sxs-lookup"><span data-stu-id="20708-172">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="20708-173">”Get-AzStorageTable”</span><span class="sxs-lookup"><span data-stu-id="20708-173">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="20708-174">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="20708-174">Az.Websites</span></span>
* <span data-ttu-id="20708-175">Tag-parametern har lagts till för ”New-AzAppServicePlan” och ”Set-AzAppServicePlan”</span><span class="sxs-lookup"><span data-stu-id="20708-175">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="20708-176">Stoppa cmdlet-körning om ett undantag uppstår när en anpassad domän läggs till på en webbplats</span><span class="sxs-lookup"><span data-stu-id="20708-176">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="20708-177">Stöd har lagts till för att utföra åtgärder för App Services som inte tillhör samma resursgrupp som App Services-planen</span><span class="sxs-lookup"><span data-stu-id="20708-177">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="20708-178">Åtkomstbegränsning har tillämpats på WebApp/Function i olika resursgrupper</span><span class="sxs-lookup"><span data-stu-id="20708-178">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="20708-179">Ett problem har åtgärdats för att ange anpassade värdnamn för WebAppSlots</span><span class="sxs-lookup"><span data-stu-id="20708-179">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="20708-180">3.5.0 – februari 2020</span><span class="sxs-lookup"><span data-stu-id="20708-180">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="20708-181">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="20708-181">Highlights since the last major release</span></span>
* <span data-ttu-id="20708-182">Uppdaterade telemetri på klientsidan.</span><span class="sxs-lookup"><span data-stu-id="20708-182">Updated client side telemetry.</span></span>
* <span data-ttu-id="20708-183">Az.IotHub lade till cmdletar som stöd för att hantera enheter.</span><span class="sxs-lookup"><span data-stu-id="20708-183">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="20708-184">Az.SqlVirtualMachine lade till cmdletar för lyssningsfunktion för tillgänglighetsgrupp.</span><span class="sxs-lookup"><span data-stu-id="20708-184">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="20708-185">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="20708-185">Az.Accounts</span></span>
* <span data-ttu-id="20708-186">Lade till SubscriptionId, TenantId och körningstid i data för telemetri på klientsidan</span><span class="sxs-lookup"><span data-stu-id="20708-186">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="20708-187">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="20708-187">Az.Automation</span></span>
* <span data-ttu-id="20708-188">Åtgärdade skrivfel i exempel 1 i referensdokumentation för ”New-AzAutomationSoftwareUpdateConfiguration”</span><span class="sxs-lookup"><span data-stu-id="20708-188">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="20708-189">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="20708-189">Az.CognitiveServices</span></span>
* <span data-ttu-id="20708-190">Uppdaterade SDK till 7.0</span><span class="sxs-lookup"><span data-stu-id="20708-190">Updated SDK to 7.0</span></span>
* <span data-ttu-id="20708-191">Förbättrade felmeddelande vid serversvar om tom brödtext</span><span class="sxs-lookup"><span data-stu-id="20708-191">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="20708-192">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="20708-192">Az.Compute</span></span>
* <span data-ttu-id="20708-193">Tillät tomt värde för ProximityPlacementGroupId under uppdatering</span><span class="sxs-lookup"><span data-stu-id="20708-193">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="20708-194">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="20708-194">Az.FrontDoor</span></span>
* <span data-ttu-id="20708-195">Lade till cmdlet för att hämta hanterade regeldefinitioner som kan användas i WAF</span><span class="sxs-lookup"><span data-stu-id="20708-195">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="20708-196">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="20708-196">Az.IotHub</span></span>
* <span data-ttu-id="20708-197">Lade till stöd för att hantera enheter i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="20708-197">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="20708-198">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="20708-198">New Cmdlets are:</span></span>
    - <span data-ttu-id="20708-199">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="20708-199">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="20708-200">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="20708-200">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="20708-201">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="20708-201">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="20708-202">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="20708-202">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="20708-203">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="20708-203">Az.KeyVault</span></span>
* <span data-ttu-id="20708-204">Åtgärdade duplicerad text för Add-AzKeyVaultKey.md</span><span class="sxs-lookup"><span data-stu-id="20708-204">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="20708-205">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="20708-205">Az.Monitor</span></span>
* <span data-ttu-id="20708-206">Åtgärdade beskrivning av cmdleten Get-AzLog.</span><span class="sxs-lookup"><span data-stu-id="20708-206">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="20708-207">En ny parameter med namnet ActionGroupId har lagts till i kommandot ”New-AzMetricAlertRuleV2”.</span><span class="sxs-lookup"><span data-stu-id="20708-207">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="20708-208">Användaren kan ange ActionGroupId(string) eller ActionGroup(ActivityLogAlertActionGroup).</span><span class="sxs-lookup"><span data-stu-id="20708-208">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="20708-209">Az.Network</span><span class="sxs-lookup"><span data-stu-id="20708-209">Az.Network</span></span>
* <span data-ttu-id="20708-210">Lade till en extra parameteranteckning för parametern ”-EnableProxyProtocol” för cmdleten ”New-AzPrivateLinkService”.</span><span class="sxs-lookup"><span data-stu-id="20708-210">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="20708-211">Åtgärdade FilterData-exempel i Start-AzVirtualNetworkGatewayConnectionPacketCapture.md och Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="20708-211">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="20708-212">Lade till paketinsamlingsexempel för att samla in alla inre och yttre paket i Start-AzVirtualNetworkGatewayConnectionPacketCapture.md och Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="20708-212">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="20708-213">Lade till stöd för Azure-brandväggsprincip på VNet-brandväggar</span><span class="sxs-lookup"><span data-stu-id="20708-213">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="20708-214">Inga nya cmdletar har lagts till.</span><span class="sxs-lookup"><span data-stu-id="20708-214">No new cmdlets are added.</span></span> <span data-ttu-id="20708-215">Lättar begränsningen för brandväggsprincip på VNet-brandväggar</span><span class="sxs-lookup"><span data-stu-id="20708-215">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="20708-216">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="20708-216">Az.RecoveryServices</span></span>
* <span data-ttu-id="20708-217">Lade till stöd för Restore-as-files för SQL-databaser.</span><span class="sxs-lookup"><span data-stu-id="20708-217">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="20708-218">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="20708-218">Az.Resources</span></span>
* <span data-ttu-id="20708-219">Omstrukturerade cmdletar för malldistribution</span><span class="sxs-lookup"><span data-stu-id="20708-219">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="20708-220">Lade till nya cmdletar för att hantera distributioner i hanteringsgruppen: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="20708-220">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="20708-221">Lade till nya cmdletar för att hantera distributioner i klientorganisationsområdet: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="20708-221">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="20708-222">Omstrukturerade \*-AzDeployment-cmdletar för att fungera specifikt i prenumerationsomfattningen</span><span class="sxs-lookup"><span data-stu-id="20708-222">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="20708-223">Skapade alias \*-AzSubscriptionDeployment för \*-AzDeployment-cmdletar</span><span class="sxs-lookup"><span data-stu-id="20708-223">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="20708-224">Åtgärdade ”Update-AzADApplication” när parametern ”AvailableToOtherTenants” inte har angetts</span><span class="sxs-lookup"><span data-stu-id="20708-224">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="20708-225">Tog bort ApplicationObjectWithoutCredentialParameterSet för att undvika AmbiguousParameterSetException.</span><span class="sxs-lookup"><span data-stu-id="20708-225">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="20708-226">Återskapade hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="20708-226">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="20708-227">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="20708-227">Az.Sql</span></span>
* <span data-ttu-id="20708-228">Lade till stöd för återställning till tidpunkt mellan prenumerationer på hanterade instanser.</span><span class="sxs-lookup"><span data-stu-id="20708-228">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="20708-229">Lade till stöd för att ändra befintlig SQL Managed Instance-maskinvarugenerering</span><span class="sxs-lookup"><span data-stu-id="20708-229">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="20708-230">Åtgärdade ”Update-AzSqlServerVulnerabilityAssessmentSetting”-hjälpexempel: parameter/egenskapsutdata - EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="20708-230">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="20708-231">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="20708-231">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="20708-232">Lade till cmdletar för lyssningsfunktion för tillgänglighetsgrupp</span><span class="sxs-lookup"><span data-stu-id="20708-232">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="20708-233">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="20708-233">Az.StorageSync</span></span>
* <span data-ttu-id="20708-234">Uppdaterade teckenuppsättningar som stöds i ”Invoke-AzStorageSyncCompatibilityCheck”.</span><span class="sxs-lookup"><span data-stu-id="20708-234">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="20708-235">3.4.0 – februari 2020</span><span class="sxs-lookup"><span data-stu-id="20708-235">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="20708-236">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="20708-236">Highlights since the last major release</span></span>
* <span data-ttu-id="20708-237">Första Az.CosmosDB-versionen 0.1.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="20708-237">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="20708-238">Stöd för Az.Network ConnectionMonitor V2 har lagts till</span><span class="sxs-lookup"><span data-stu-id="20708-238">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="20708-239">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="20708-239">Az.Accounts</span></span>
* <span data-ttu-id="20708-240">Inaktivera automatisk sparande av kontext när AzureRmContext.json inte är tillgängligt</span><span class="sxs-lookup"><span data-stu-id="20708-240">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="20708-241">Uppdatera referensen till Azure Powershell Common till 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="20708-241">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="20708-242">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="20708-242">Az.ApiManagement</span></span>
* <span data-ttu-id="20708-243">**Get-AzApiManagementApiSchema** Hämtning av Open-Api-schema som är associerat med ett API har åtgärdats   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="20708-243">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="20708-244">**New-AzApiManagementProduct**\* och **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="20708-244">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="20708-245">Åtgärda dokumentation för https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="20708-245">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="20708-246">**Set-AzApiManagementApi** Exempel för att visa hur ServiceUrl uppdateras med hjälp av cmdleten har lagts till</span><span class="sxs-lookup"><span data-stu-id="20708-246">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="20708-247">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="20708-247">Az.Compute</span></span>
* <span data-ttu-id="20708-248">Begränsa antalet VM-status till 100 för att undvika begränsning när Get-AzVM -Status utförs utan VM-namn.</span><span class="sxs-lookup"><span data-stu-id="20708-248">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="20708-249">Lägg till cmdleten Update-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="20708-249">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="20708-250">Lägg till parametrarna EncryptionType och DiskEncryptionSetId i följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="20708-250">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="20708-251">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="20708-251">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="20708-252">Lägg till parametern ColocationStatus för cmdleten Get-AzProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="20708-252">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="20708-253">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="20708-253">Az.DataFactory</span></span>
* <span data-ttu-id="20708-254">Uppdatera ADF .Net SDK-versionen till 4.7.0</span><span class="sxs-lookup"><span data-stu-id="20708-254">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="20708-255">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="20708-255">Az.DeploymentManager</span></span>
* <span data-ttu-id="20708-256">Lägger till LIST-åtgärder för resurser</span><span class="sxs-lookup"><span data-stu-id="20708-256">Adds LIST operations for resources</span></span>
* <span data-ttu-id="20708-257">Lägger till funktion för att utföra åtgärder för hälsokontrollsteg</span><span class="sxs-lookup"><span data-stu-id="20708-257">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="20708-258">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="20708-258">Az.HDInsight</span></span>
* <span data-ttu-id="20708-259">Åtgärda dokumentfel för New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="20708-259">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="20708-260">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="20708-260">Az.KeyVault</span></span>
* <span data-ttu-id="20708-261">Lägg till Name-alias för attributet VaultName så att Remove-AzureKeyVault stämmer överens med New-AzureKeyVault.</span><span class="sxs-lookup"><span data-stu-id="20708-261">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="20708-262">Az.Network</span><span class="sxs-lookup"><span data-stu-id="20708-262">Az.Network</span></span>
* <span data-ttu-id="20708-263">Nytt exempel har lagts till i Set-AzNetworkWatcherConfigFlowLog.md för att demonstrera ett inaktiveringsscenario för Trafikanalys.</span><span class="sxs-lookup"><span data-stu-id="20708-263">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="20708-264">Lägg till stöd för att tilldela konfiguration av hanterings-IP till Azure Firewall – ett dedikerat undernät och en offentlig IP som brandväggen använder för dess hanteringstrafik</span><span class="sxs-lookup"><span data-stu-id="20708-264">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="20708-265">Cmdleten New-AzFirewall har uppdaterats:</span><span class="sxs-lookup"><span data-stu-id="20708-265">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="20708-266">Parametern -ManagementPublicIpAddress (inte obligatorisk) som accepterar ett offentligt IP-adressobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="20708-266">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="20708-267">Metoden SetManagementIpConfiguration har lagts till för brandväggsobjekt – kräver ett undernät och en offentlig IP-adress som indata – undernätets namn måste vara ”AzureFirewallManagementSubnet”</span><span class="sxs-lookup"><span data-stu-id="20708-267">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="20708-268">Exempel för Get-AzNetworkSecurityGroup har korrigerats så att exempel visas för NSG:er i stället för nätverksgränssnitt.</span><span class="sxs-lookup"><span data-stu-id="20708-268">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="20708-269">Ett skrivfel har åtgärdats i kommandot New-AzVpnSite som hindrade kompletteraren för resurs-ID från att fylla i en parameter.</span><span class="sxs-lookup"><span data-stu-id="20708-269">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="20708-270">Stöd för Url-konfiguration i åtgärdsuppsättningen för omskrivningsregler i Application Gateway har lagts till</span><span class="sxs-lookup"><span data-stu-id="20708-270">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="20708-271">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="20708-271">New cmdlets added:</span></span>
        - <span data-ttu-id="20708-272">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="20708-272">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="20708-273">Cmdletar har uppdaterats med den valfria parametern -UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="20708-273">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="20708-274">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="20708-274">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="20708-275">Lägg till stöd för resurser för NetworkWatcher ConnectionMonitor version 2</span><span class="sxs-lookup"><span data-stu-id="20708-275">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="20708-276">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="20708-276">Az.PolicyInsights</span></span>
* <span data-ttu-id="20708-277">Stöd för utvärdering av efterlevnad innan fastställande av vilken resurs som ska åtgärdas</span><span class="sxs-lookup"><span data-stu-id="20708-277">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="20708-278">Lägg till parametern ”-ResourceDiscoverMode” för Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="20708-278">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="20708-279">Lägg till cmdleten Get-AzPolicyMetadata för att hämta resurser för principmetadata</span><span class="sxs-lookup"><span data-stu-id="20708-279">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="20708-280">Get-AzPolicyState och Get-AzPolicyStateSummary för API-versionen 2019-10-01 har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="20708-280">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="20708-281">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="20708-281">Az.RecoveryServices</span></span>
* <span data-ttu-id="20708-282">Azure Site Recovery-stöd för att ta bort en replikerad disk.</span><span class="sxs-lookup"><span data-stu-id="20708-282">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="20708-283">Tillagt Azure Backup-stöd för att lägga till taggar när ett Recovery Services-valv skapas.</span><span class="sxs-lookup"><span data-stu-id="20708-283">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="20708-284">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="20708-284">Az.Resources</span></span>
* <span data-ttu-id="20708-285">Gör -Scope valfritt i cmdletarna \*-AzPolicyAssignment med standardinställning till kontextprenumeration</span><span class="sxs-lookup"><span data-stu-id="20708-285">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="20708-286">Lägg till exempel på att skapa ADServicePrincipal med lösenord och nyckelautentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="20708-286">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="20708-287">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="20708-287">Az.Sql</span></span>
<span data-ttu-id="20708-288">Åtgärda cmdleten New-AzSqlDatabaseSecondary så att existensen PartnerDatabaseName kontrolleras i stället för existensen DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="20708-288">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="20708-289">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="20708-289">Az.Storage</span></span>
* <span data-ttu-id="20708-290">Stöd för angivning av krypteringsnyckeltyp för Tabell/kö i Skapa lagringskonto</span><span class="sxs-lookup"><span data-stu-id="20708-290">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="20708-291">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="20708-291">New-AzStorageAccount</span></span>
* <span data-ttu-id="20708-292">Visa RequestId när StorageException inte har ExtendedErrorInformation</span><span class="sxs-lookup"><span data-stu-id="20708-292">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="20708-293">Åtgärda exempel 6 för cmdleten Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="20708-293">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="20708-294">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="20708-294">Az.Websites</span></span>
* <span data-ttu-id="20708-295">Set-AzWebapp och Set-AzWebappSlot stöder egenskaperna AlwaysOn, MinTls och FtpsState</span><span class="sxs-lookup"><span data-stu-id="20708-295">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="20708-296">Åtgärdar problemet där inställning av HttpsOnly samtidigt som AppservicePlan ändrades med det enskilda kommandot Set-AzWebApp återställde HttpsOnly till standardvärdet</span><span class="sxs-lookup"><span data-stu-id="20708-296">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="20708-297">3.3.0 – januari 2020</span><span class="sxs-lookup"><span data-stu-id="20708-297">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="20708-298">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="20708-298">Az.Accounts</span></span>
* <span data-ttu-id="20708-299">Nu stöder Add-AzEnvironment och Set-AzEnvironment parametrarna AzureAttestationServiceEndpointResourceId och AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="20708-299">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="20708-300">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="20708-300">Az.Cdn</span></span>
* <span data-ttu-id="20708-301">Information om felsvar visas i New-AzCdnEndpoint-cmdleten</span><span class="sxs-lookup"><span data-stu-id="20708-301">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="20708-302">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="20708-302">Az.Compute</span></span>
* <span data-ttu-id="20708-303">Set-AzVMCustomScriptExtension-cmdleten har åtgärdats för en virtuell dator med hanterad OD-disk som inte har någon operativsystemprofil.</span><span class="sxs-lookup"><span data-stu-id="20708-303">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="20708-304">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="20708-304">Az.ContainerInstance</span></span>
* <span data-ttu-id="20708-305">Parameternamn som används med New-AzContainerGroup-exempel har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="20708-305">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="20708-306">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="20708-306">Az.DataBoxEdge</span></span>
* <span data-ttu-id="20708-307">Cmdleten ”Get-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="20708-307">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="20708-308">Hämta gränslagringscontainern</span><span class="sxs-lookup"><span data-stu-id="20708-308">Get the Edge Storage Container</span></span>
* <span data-ttu-id="20708-309">Cmdleten ”New-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="20708-309">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="20708-310">Skapa en ny gränslagringscontainer</span><span class="sxs-lookup"><span data-stu-id="20708-310">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="20708-311">Cmdleten ”Remove-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="20708-311">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="20708-312">Ta bort gränslagringscontainern</span><span class="sxs-lookup"><span data-stu-id="20708-312">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="20708-313">Cmdleten ”Invoke-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="20708-313">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="20708-314">Anropa åtgärd för att uppdatera data i gränslagringscontainer</span><span class="sxs-lookup"><span data-stu-id="20708-314">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="20708-315">Cmdleten ”Get-AzDataBoxEdgeStorageAccount” har lagts till</span><span class="sxs-lookup"><span data-stu-id="20708-315">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="20708-316">Hämta gränslagringskontot</span><span class="sxs-lookup"><span data-stu-id="20708-316">Get the Edge Storage Account</span></span>
* <span data-ttu-id="20708-317">Cmdleten ”New-AzDataBoxEdgeStorageAccount” har lagts till</span><span class="sxs-lookup"><span data-stu-id="20708-317">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="20708-318">Skapa ett nytt gränslagringskonto</span><span class="sxs-lookup"><span data-stu-id="20708-318">Create new Edge Storage Account</span></span>
* <span data-ttu-id="20708-319">Cmdleten ”Remove-AzDataBoxEdgeStorageAccount” har lagts till</span><span class="sxs-lookup"><span data-stu-id="20708-319">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="20708-320">Ta bort gränslagringskontot</span><span class="sxs-lookup"><span data-stu-id="20708-320">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="20708-321">Anropa cmdleten ”Invoke-AzDataBoxEdgeShare”</span><span class="sxs-lookup"><span data-stu-id="20708-321">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="20708-322">Anropa åtgärd för att uppdatera resursdata</span><span class="sxs-lookup"><span data-stu-id="20708-322">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="20708-323">Cmdleten ”Set-AzDataBoxEdgeStorageAccountCredential” har lagts till</span><span class="sxs-lookup"><span data-stu-id="20708-323">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="20708-324">Ange autentiseringsuppgifter för az databoxedge-lagringskonto</span><span class="sxs-lookup"><span data-stu-id="20708-324">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="20708-325">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="20708-325">Az.DataFactory</span></span>
* <span data-ttu-id="20708-326">Lägg till AutoUpdateETA-, LatestVersion-, PushedVersion-, TaskQueueId- och VersionStatus-egenskaper för Get-AzDataFactoryV2IntegrationRuntime-cmd</span><span class="sxs-lookup"><span data-stu-id="20708-326">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="20708-327">Uppdatera ADF .Net SDK-versionen till 4.6.0</span><span class="sxs-lookup"><span data-stu-id="20708-327">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="20708-328">Lägg till parametern ”PublicIPs” för ”Set-AzureRmDataFactoryV2IntegrationRuntime”-cmd så att Azure-SSIS IR kan skapas med statiska offentliga IP-adresser.</span><span class="sxs-lookup"><span data-stu-id="20708-328">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="20708-329">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="20708-329">Az.DevTestLabs</span></span>
* <span data-ttu-id="20708-330">Ta bort den brutna länken i Get-AzDtlAllowedVMSizesPolicy.md</span><span class="sxs-lookup"><span data-stu-id="20708-330">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="20708-331">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="20708-331">Az.EventHub</span></span>
* <span data-ttu-id="20708-332">Korrigering av problem 10634: Åtgärda referensen till null-objekt för eventhubnamespace-borttagning</span><span class="sxs-lookup"><span data-stu-id="20708-332">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="20708-333">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="20708-333">Az.HDInsight</span></span>
* <span data-ttu-id="20708-334">Åtgärda Invoke-AzHDInsightHiveJob.md-fel.</span><span class="sxs-lookup"><span data-stu-id="20708-334">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="20708-335">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="20708-335">Az.MachineLearning</span></span>
* <span data-ttu-id="20708-336">Nedanstående cmdletar har tagits bort eftersom MachineLearningCompute inte längre är tillgängligt</span><span class="sxs-lookup"><span data-stu-id="20708-336">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="20708-337">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="20708-337">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="20708-338">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="20708-338">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="20708-339">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="20708-339">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="20708-340">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="20708-340">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="20708-341">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="20708-341">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="20708-342">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="20708-342">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="20708-343">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="20708-343">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="20708-344">Az.Network</span><span class="sxs-lookup"><span data-stu-id="20708-344">Az.Network</span></span>
* <span data-ttu-id="20708-345">Uppgradera beroende av Microsoft.Azure.Management.Sql från 1.36-preview till 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="20708-345">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="20708-346">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="20708-346">Az.RecoveryServices</span></span>
* <span data-ttu-id="20708-347">Ändrat Azure Site Recovery-stöd för krypterade vilande data på virtuella datorer med hanterade diskar med kundhanterade nycklar för Azure till Azure-providern.</span><span class="sxs-lookup"><span data-stu-id="20708-347">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="20708-348">Azure Site Recovery-stöd för att ange ID för diskkrypteringsuppsättning som valfri inmatning för aktivering av skydd för VMware till Azure.</span><span class="sxs-lookup"><span data-stu-id="20708-348">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="20708-349">Azure Site Recovery-stöd för att ange ID för diskkrypteringsuppsättning som valfri inmatning på disknivå för aktivering av skydd för VMware till Azure.</span><span class="sxs-lookup"><span data-stu-id="20708-349">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="20708-350">Azure Site Recovery-stöd för att uppdatera replikeringsskyddade objekt med mappning för diskkrypteringsuppsättning för HyperV till Azure.</span><span class="sxs-lookup"><span data-stu-id="20708-350">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="20708-351">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="20708-351">Az.Resources</span></span>
* <span data-ttu-id="20708-352">Åtgärda ett fel i hjälpdokument för ”Remove-AzTag”.</span><span class="sxs-lookup"><span data-stu-id="20708-352">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="20708-353">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="20708-353">Az.Sql</span></span>
* <span data-ttu-id="20708-354">Åtgärda funktioner i cmdletar för att ange baslinjen för sårbarhetsbedömning för arbete med huvuddatabasen för Azure-databasen och begränsa den för systemdatabaser på hanterade instanser.</span><span class="sxs-lookup"><span data-stu-id="20708-354">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="20708-355">Åtgärda ett fel när en redundansgrupp för en SQL-instans skapas</span><span class="sxs-lookup"><span data-stu-id="20708-355">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="20708-356">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="20708-356">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="20708-357">Lägg till DR som en ny giltig licenstyp</span><span class="sxs-lookup"><span data-stu-id="20708-357">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="20708-358">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="20708-358">Az.Storage</span></span>
* <span data-ttu-id="20708-359">Lägg till varningsmeddelande om icke-bakåtkompatibel ändring för DefaultAction-värdeändring i en framtida version</span><span class="sxs-lookup"><span data-stu-id="20708-359">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="20708-360">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="20708-360">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="20708-361">Stöd för att hämta lagringskontots senaste synkroniseringstid genom att köra get-AzureRMStorageAccount med parametern -IncludeGeoReplicationStats</span><span class="sxs-lookup"><span data-stu-id="20708-361">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span> 
    - <span data-ttu-id="20708-362">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="20708-362">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="20708-363">3.2.0 – December 2019</span><span class="sxs-lookup"><span data-stu-id="20708-363">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="20708-364">Allmänt</span><span class="sxs-lookup"><span data-stu-id="20708-364">General</span></span>
* <span data-ttu-id="20708-365">Uppdatera referenser i .psd1 för att använda relativa sökvägar för alla moduler</span><span class="sxs-lookup"><span data-stu-id="20708-365">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="20708-366">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="20708-366">Az.Accounts</span></span>
* <span data-ttu-id="20708-367">Ange rätt UserAgent för telemetri på klientsidan för Az 4.0 preview</span><span class="sxs-lookup"><span data-stu-id="20708-367">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="20708-368">Visa användarvänligt felmeddelande när kontexten är null i Az 4.0 preview</span><span class="sxs-lookup"><span data-stu-id="20708-368">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="20708-369">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="20708-369">Az.Batch</span></span>
* <span data-ttu-id="20708-370">Korrigera problem [#10602](https://github.com/Azure/azure-powershell/issues/10602), där **New-AzBatchPool** skickade VirtualMachineConfiguration.ContainerConfiguration eller VirtualMachineConfiguration.DataDisks på ett felaktigt sätt till servern.</span><span class="sxs-lookup"><span data-stu-id="20708-370">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="20708-371">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="20708-371">Az.DataFactory</span></span>
* <span data-ttu-id="20708-372">Uppdatera ADF .Net SDK-versionen till 4.5.0</span><span class="sxs-lookup"><span data-stu-id="20708-372">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="20708-373">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="20708-373">Az.FrontDoor</span></span>
* <span data-ttu-id="20708-374">Stöd har lagts till för undantag för hanterade regler för brandväggen för webbaserade program</span><span class="sxs-lookup"><span data-stu-id="20708-374">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="20708-375">Lägg till SocketAddr för automatisk komplettering</span><span class="sxs-lookup"><span data-stu-id="20708-375">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="20708-376">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="20708-376">Az.HealthcareApis</span></span>
* <span data-ttu-id="20708-377">Undantagshantering</span><span class="sxs-lookup"><span data-stu-id="20708-377">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="20708-378">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="20708-378">Az.KeyVault</span></span>
* <span data-ttu-id="20708-379">Åtgärdat fel vid åtkomst av värde som kanske inte har angetts</span><span class="sxs-lookup"><span data-stu-id="20708-379">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="20708-380">Hantering av ECC-certifikat (Elliptic Curve Cryptography)</span><span class="sxs-lookup"><span data-stu-id="20708-380">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="20708-381">Stöd har lagts till för att ange kurvan för certifikatprinciper</span><span class="sxs-lookup"><span data-stu-id="20708-381">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="20708-382">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="20708-382">Az.Monitor</span></span>
* <span data-ttu-id="20708-383">Lägger till valfritt argument i kommandot Lägg till diagnostikinställningar.</span><span class="sxs-lookup"><span data-stu-id="20708-383">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="20708-384">Ett växelargument som om det finns visar att exporten till Log Analytics måste ske till ett fast schema (kallas även</span><span class="sxs-lookup"><span data-stu-id="20708-384">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="20708-385">dedikerad, datatyp)</span><span class="sxs-lookup"><span data-stu-id="20708-385">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="20708-386">Az.Network</span><span class="sxs-lookup"><span data-stu-id="20708-386">Az.Network</span></span>
* <span data-ttu-id="20708-387">Stöd för IpGroups i program-, NAT- och nätverksregler för Azure Firewall.</span><span class="sxs-lookup"><span data-stu-id="20708-387">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="20708-388">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="20708-388">Az.Resources</span></span>
* <span data-ttu-id="20708-389">Åtgärda ett problem där malldistributionen inte kan läsa en mallparameter om dess namn står i konflikt med ett inbyggt parameternamn.</span><span class="sxs-lookup"><span data-stu-id="20708-389">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="20708-390">Uppdaterade princip-cmdletar för att använda den nya API-versionen 2019-09-01 som introducerar grupperingsstöd inom principuppsättningsdefinitioner.</span><span class="sxs-lookup"><span data-stu-id="20708-390">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="20708-391">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="20708-391">Az.Sql</span></span>
* <span data-ttu-id="20708-392">Uppgraderad funktion för att skapa lagring i automatisk aktivering av sårbarhetsbedömning till StorageV2</span><span class="sxs-lookup"><span data-stu-id="20708-392">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="20708-393">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="20708-393">Az.Storage</span></span>
* <span data-ttu-id="20708-394">Stöd för generering av blob/container-identitetsbaserad SAS-token med lagringskontextbaserad på OAuth-autentisering</span><span class="sxs-lookup"><span data-stu-id="20708-394">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="20708-395">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="20708-395">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="20708-396">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="20708-396">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="20708-397">Stöd för återkallning av användardelegeringsnycklar för lagringskonto för att återkalla alla SAS-token</span><span class="sxs-lookup"><span data-stu-id="20708-397">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="20708-398">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="20708-398">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="20708-399">Uppgradera till Microsoft.Azure.Management.Storage 14.2.0 för att stödja den nya API-versionen 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="20708-399">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="20708-400">Stöd för QuotaGiB (resurskvot i Gibibye) för värden över 5120 i hanteringsplanet för cmdletar för filresurser och parameteraliaset. Quota har också lagts till för parametern ”QuotaGiB”.</span><span class="sxs-lookup"><span data-stu-id="20708-400">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span> 
    - <span data-ttu-id="20708-401">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="20708-401">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="20708-402">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="20708-402">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="20708-403">Lägg till parameteraliaset QuotaGiB i parametern Quota</span><span class="sxs-lookup"><span data-stu-id="20708-403">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="20708-404">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="20708-404">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="20708-405">Åtgärda problemet att Set-AzStorageContainerAcl kan rensa den lagrade åtkomstprincipen</span><span class="sxs-lookup"><span data-stu-id="20708-405">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="20708-406">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="20708-406">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="20708-407">3.1.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="20708-407">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="20708-408">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="20708-408">Highlights since the last major release</span></span>
* <span data-ttu-id="20708-409">Az.DataBoxEdge 1.0.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="20708-409">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="20708-410">Az.SqlVirtualMachine 1.0.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="20708-410">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="20708-411">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="20708-411">Az.Compute</span></span>
* <span data-ttu-id="20708-412">Funktion för att använda en virtuell dator igen</span><span class="sxs-lookup"><span data-stu-id="20708-412">VM Reapply feature</span></span>
    - <span data-ttu-id="20708-413">Lägg till parameter för att använda igen till cmdleten Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="20708-413">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="20708-414">Funktionen AutomaticRepairs i VM-skalningsuppsättningar:</span><span class="sxs-lookup"><span data-stu-id="20708-414">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="20708-415">Lägg till parametrarna EnableAutomaticRepair, AutomaticRepairGracePeriod och AutomaticRepairMaxInstanceRepairsPercent till följande cmdletar:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="20708-415">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="20708-416">Stöd för galleriavbildningar i flera klientorganisationer för New-AzVM</span><span class="sxs-lookup"><span data-stu-id="20708-416">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="20708-417">Lägg till "Spot" till argumentslutföraren i prioritetsparametern i cmdletarna New-AzVM, New-AzVMConfig och New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="20708-417">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="20708-418">Lägg till parametrarna DiskIOPSReadWrite och DiskMBpsReadWrite till cmdleten Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="20708-418">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="20708-419">Ändra parametern SourceImageId för cmdleten New-AzGalleryImageVersion till valfri</span><span class="sxs-lookup"><span data-stu-id="20708-419">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="20708-420">Lägg till parametrarna OSDiskImage och DataDiskImage till cmdleten New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="20708-420">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="20708-421">Lägg till parametern HyperVGeneration till cmdleten New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="20708-421">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="20708-422">Lägg till parametern SkipExtensionsOnOverprovisionedVMs till cmdletarna New-AzVmss, New-AzVmssConfig och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="20708-422">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="20708-423">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="20708-423">Az.DataBoxEdge</span></span>
* <span data-ttu-id="20708-424">Cmdleten `Get-AzDataBoxEdgeOrder` har lagts till</span><span class="sxs-lookup"><span data-stu-id="20708-424">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="20708-425">Hämta ordning</span><span class="sxs-lookup"><span data-stu-id="20708-425">Get the Order</span></span>
* <span data-ttu-id="20708-426">Cmdleten `New-AzDataBoxEdgeOrder` har lagts till</span><span class="sxs-lookup"><span data-stu-id="20708-426">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="20708-427">Skapa ny ordning</span><span class="sxs-lookup"><span data-stu-id="20708-427">Create new Order</span></span>
* <span data-ttu-id="20708-428">Cmdleten `Remove-AzDataBoxEdgeOrder` har lagts till</span><span class="sxs-lookup"><span data-stu-id="20708-428">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="20708-429">Ta bort ordning</span><span class="sxs-lookup"><span data-stu-id="20708-429">Remove the Order</span></span>
* <span data-ttu-id="20708-430">Cmdleten `New-AzDataBoxEdgeShare` har ändrats</span><span class="sxs-lookup"><span data-stu-id="20708-430">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="20708-431">Nu skapas lokal filresurs</span><span class="sxs-lookup"><span data-stu-id="20708-431">Now creates Local Share</span></span>
* <span data-ttu-id="20708-432">Cmdleten `Set-AzDataBoxEdgeRole` har lagts till</span><span class="sxs-lookup"><span data-stu-id="20708-432">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="20708-433">Nu kan IotRole mappas till filresursen</span><span class="sxs-lookup"><span data-stu-id="20708-433">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="20708-434">Cmdleten `Invoke-AzDataBoxEdgeDevice` har lagts till</span><span class="sxs-lookup"><span data-stu-id="20708-434">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="20708-435">Anropa genomsökningsuppdatering, ladda ned uppdatering, installera uppdateringar på enheten</span><span class="sxs-lookup"><span data-stu-id="20708-435">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="20708-436">Cmdleten `Get-AzDataBoxEdgeTrigger` har lagts till</span><span class="sxs-lookup"><span data-stu-id="20708-436">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="20708-437">Hämtar information om utlösare</span><span class="sxs-lookup"><span data-stu-id="20708-437">Gets the information about Triggers</span></span>
* <span data-ttu-id="20708-438">Cmdleten `New-AzDataBoxEdgeTrigger` har lagts till</span><span class="sxs-lookup"><span data-stu-id="20708-438">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="20708-439">Skapa nya utlösare</span><span class="sxs-lookup"><span data-stu-id="20708-439">Create new Triggers</span></span>
* <span data-ttu-id="20708-440">Cmdleten `Remove-AzDataBoxEdgeTrigger` har lagts till</span><span class="sxs-lookup"><span data-stu-id="20708-440">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="20708-441">Ta bort utlösare</span><span class="sxs-lookup"><span data-stu-id="20708-441">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="20708-442">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="20708-442">Az.DataFactory</span></span>
* <span data-ttu-id="20708-443">Uppdatera ADF .Net SDK-versionen till 4.4.0</span><span class="sxs-lookup"><span data-stu-id="20708-443">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="20708-444">Lägg till parametern ExpressCustomSetup för kommandot Set-AzureRmDataFactoryV2IntegrationRuntime för att aktivera installationskonfigurationer och komponenter från tredje part utan anpassat konfigurationsskript.</span><span class="sxs-lookup"><span data-stu-id="20708-444">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="20708-445">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="20708-445">Az.DataLakeStore</span></span>
* <span data-ttu-id="20708-446">Uppdatera dokumentation för Get-AzDataLakeStoreDeletedItem och Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="20708-446">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="20708-447">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="20708-447">Az.EventHub</span></span>
* <span data-ttu-id="20708-448">Korrigering av problem #10301: Korrigera datumformat för SAS-token</span><span class="sxs-lookup"><span data-stu-id="20708-448">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="20708-449">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="20708-449">Az.FrontDoor</span></span>
* <span data-ttu-id="20708-450">Lägg till parametern MinimumTlsVersion till Enable-AzFrontDoorCustomDomainHttps och New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="20708-450">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="20708-451">Lägg till parametrarna HealthProbeMethod och EnabledState till New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="20708-451">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="20708-452">Lägg till en ny cmdlet för att skapa BackendPoolsSettings-objekt som passar i skapande/uppdatering av Front Door</span><span class="sxs-lookup"><span data-stu-id="20708-452">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="20708-453">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="20708-453">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="20708-454">Az.Network</span><span class="sxs-lookup"><span data-stu-id="20708-454">Az.Network</span></span>
* <span data-ttu-id="20708-455">Ändra alternativexemplen Start-AzVirtualNetworkGatewayConnectionPacketCapture.md och Start-AzVirtualnetworkGatewayPacketCapture.md för FilterData.</span><span class="sxs-lookup"><span data-stu-id="20708-455">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="20708-456">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="20708-456">Az.PrivateDns</span></span>
* <span data-ttu-id="20708-457">Uppdaterade PrivateDns .NET SDK till version 1.0.0</span><span class="sxs-lookup"><span data-stu-id="20708-457">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="20708-458">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="20708-458">Az.RecoveryServices</span></span>
* <span data-ttu-id="20708-459">Stöd för att välja disktyp vid aktivering av skydd i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="20708-459">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="20708-460">Korrigering av bugg för åtgärdsredigering av återställningsplan i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="20708-460">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="20708-461">Återställningsstöd för att godkänna filestream-databaser i Azure Backup SQL.</span><span class="sxs-lookup"><span data-stu-id="20708-461">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="20708-462">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="20708-462">Az.RedisCache</span></span>
* <span data-ttu-id="20708-463">Parametern MinimumTlsVersion har lagts till i cmdletarna New-AzRedisCache och Set-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="20708-463">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="20708-464">Dessutom har MinimumTlsVersion lagts till i utdata för cmdleten Get-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="20708-464">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="20708-465">Verifiering har lagts till på parametern -Size i cmdletarna Set-AzRedisCache och New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="20708-465">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="20708-466">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="20708-466">Az.Resources</span></span>
- <span data-ttu-id="20708-467">Uppdaterade policy-cmdletar för att använda den nya API-versionen 2019-06-01 som har en ny EnforcementMode-egenskap i policytilldelningen.</span><span class="sxs-lookup"><span data-stu-id="20708-467">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="20708-468">Uppdaterade hjälpexempel för skapandet av policydefinition</span><span class="sxs-lookup"><span data-stu-id="20708-468">Updated create policy definition help example</span></span>
- <span data-ttu-id="20708-469">Åtgärda bugg i Remove-AZADServicePrincipal -ServicePrincipalName, utlös null-referens när tjänstens huvudnamn inte hittas.</span><span class="sxs-lookup"><span data-stu-id="20708-469">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="20708-470">Åtgärda bugg i New-AZADServicePrincipal, utlös null-referens när klientorganisationen inte har någon prenumeration.</span><span class="sxs-lookup"><span data-stu-id="20708-470">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="20708-471">Ändra New-AzAdServicePrincipal för att endast lägga till autentiseringsuppgifter för det associerade programmet.</span><span class="sxs-lookup"><span data-stu-id="20708-471">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="20708-472">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="20708-472">Az.Sql</span></span>
* <span data-ttu-id="20708-473">Stöd har lagts till för databasen ReadReplicaCount.</span><span class="sxs-lookup"><span data-stu-id="20708-473">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="20708-474">Korrigerade Set-AzSqlDatabase när zonredundans inte har angetts</span><span class="sxs-lookup"><span data-stu-id="20708-474">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="20708-475">3.0.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="20708-475">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="20708-476">Allmänt</span><span class="sxs-lookup"><span data-stu-id="20708-476">General</span></span>
* <span data-ttu-id="20708-477">Az. PrivateDns 1.0.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="20708-477">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="20708-478">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="20708-478">Az.Accounts</span></span>
* <span data-ttu-id="20708-479">Lägg till ett utfasningsmeddelande för aliaset Resolve-error.</span><span class="sxs-lookup"><span data-stu-id="20708-479">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="20708-480">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="20708-480">Az.Advisor</span></span>
* <span data-ttu-id="20708-481">Den nya kategorin Operational Excellence har lagts till i cmdleten Get-AzAdvisorRecommendation.</span><span class="sxs-lookup"><span data-stu-id="20708-481">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="20708-482">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="20708-482">Az.Batch</span></span>
* <span data-ttu-id="20708-483">`CoreQuota` på `BatchAccountContext` har bytt namn till `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="20708-483">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="20708-484">Det finns även en ny `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="20708-484">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="20708-485">Detta påverkar **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="20708-485">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="20708-486">**New-AzBatchTask** `-ResourceFile`-parametern tar nu en samling `PSResourceFile`-objekt som kan skapas med hjälp av den nya cmdleten **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="20708-486">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="20708-487">Ny **New-AzBatchResourceFile**-cmdlet för att skapa `PSResourceFile`-objekt.</span><span class="sxs-lookup"><span data-stu-id="20708-487">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="20708-488">Dessa kan tillhandahållas till **New-AzBatchTask** på `-ResourceFile`-parametern.</span><span class="sxs-lookup"><span data-stu-id="20708-488">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="20708-489">Detta stöder två nya typer av resursfiler förutom det befintliga sättet med `HttpUrl`:</span><span class="sxs-lookup"><span data-stu-id="20708-489">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="20708-490">`AutoStorageContainerName`-baserade resursfiler laddar ned en hel container för automatisk lagring till Batch-noden.</span><span class="sxs-lookup"><span data-stu-id="20708-490">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="20708-491">`StorageContainerUrl`-baserade resursfiler laddar ned containern som anges i webbadressen till Batch-noden.</span><span class="sxs-lookup"><span data-stu-id="20708-491">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="20708-492">Tog bort egenskapen `ApplicationPackages` för `PSApplication` som returnerades av **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="20708-492">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="20708-493">Specifika paket i ett program kan nu hämtas med hjälp av **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="20708-493">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="20708-494">Till exempel: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="20708-494">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="20708-495">Bytt namn på `ApplicationId` till `ApplicationName` på **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** och **Set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="20708-495">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="20708-496">`ApplicationId` är nu ett alias för `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="20708-496">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="20708-497">Ny `PSWindowsUserConfiguration`-egenskap till `PSUserAccount` lades till.</span><span class="sxs-lookup"><span data-stu-id="20708-497">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="20708-498">Bytte namn på `Version` till `Name` på `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="20708-498">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="20708-499">Bytte namn på `BlobSource` till `HttpUrl` på `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="20708-499">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="20708-500">Tog bort egenskapen `OSDisk` från `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="20708-500">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="20708-501">Tog bort **Set-AzBatchPoolOSVersion**.</span><span class="sxs-lookup"><span data-stu-id="20708-501">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="20708-502">Den här åtgärden stöds inte längre.</span><span class="sxs-lookup"><span data-stu-id="20708-502">This operation is no longer supported.</span></span>
* <span data-ttu-id="20708-503">`TargetOSVersion` har tagits bort från `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="20708-503">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="20708-504">Bytte namn på `CurrentOSVersion` till `OSVersion` på `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="20708-504">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="20708-505">`DataEgressGiB` och `DataIngressGiB` har tagits bort från `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="20708-505">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="20708-506">Tog bort **Get-AzBatchNodeAgentSku** och ersatte det med **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="20708-506">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span> 
  - <span data-ttu-id="20708-507">**Get-AzBatchSupportedImage** returnerar samma data som **Get-AzBatchNodeAgentSku** men i ett mer användarvänligt format.</span><span class="sxs-lookup"><span data-stu-id="20708-507">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="20708-508">Nya icke-verifierade avbildningar returneras nu också.</span><span class="sxs-lookup"><span data-stu-id="20708-508">New non-verified images are also now returned.</span></span> <span data-ttu-id="20708-509">Ytterligare information om `Capabilities` och `BatchSupportEndOfLife` för varje avbildning inkluderas också.</span><span class="sxs-lookup"><span data-stu-id="20708-509">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="20708-510">Lade till möjlighet att montera fjärrfilsystem på varje nod i en pool via den nya parametern `MountConfiguration` för **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="20708-510">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="20708-511">Har nu stöd för nätverkssäkerhetsregler som blockerar nätverksåtkomst till en pool baserat på källportens trafik.</span><span class="sxs-lookup"><span data-stu-id="20708-511">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="20708-512">Detta görs via egenskapen `SourcePortRanges` på `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="20708-512">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="20708-513">När du kör en container stöder nu Batch körningen av uppgiften i arbetskatalogen för containern eller i arbetskatalogen för Batch-uppgiften.</span><span class="sxs-lookup"><span data-stu-id="20708-513">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="20708-514">Detta styrs av egenskapen `WorkingDirectory` på `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="20708-514">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="20708-515">Lade till en funktion för att ange en samling av offentliga IP-adresser på `PSNetworkConfiguration` via den nya egenskapen `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="20708-515">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="20708-516">Detta garanterar att noderna i poolen har en IP-adress från listan över IP-adresser som tillhandahållits av användare.</span><span class="sxs-lookup"><span data-stu-id="20708-516">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="20708-517">Om inget värde anges är standardvärdet för `WaitForSuccess` på `PSSTartTask` nu `$True` (var tidigare `$False`).</span><span class="sxs-lookup"><span data-stu-id="20708-517">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="20708-518">Om inget värde anges är standardvärdet för `Scope` på `PSAutoUserSpecification` nu `Pool` (var tidigare `Task` på Windows och `Pool` på Linux).</span><span class="sxs-lookup"><span data-stu-id="20708-518">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="20708-519">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="20708-519">Az.Cdn</span></span>
* <span data-ttu-id="20708-520">Introducerade UrlRewriteAction och CacheKeyQueryStringAction till RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="20708-520">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="20708-521">Åtgärdade flera buggar, som saknade indata för ”väljare” i cmdleten New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="20708-521">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="20708-522">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="20708-522">Az.Compute</span></span>
* <span data-ttu-id="20708-523">Funktion för diskkrypteringsuppsättning</span><span class="sxs-lookup"><span data-stu-id="20708-523">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="20708-524">Nya cmdletar:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="20708-524">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="20708-525">Parametern DiskEncryptionSetId har lagts till i följande cmdletar: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="20708-525">DiskEncryptionSetId parameter is added to the following cmdlets: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span></span>        
        <span data-ttu-id="20708-526">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="20708-526">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="20708-527">Parametrarna DiskEncryptionSetId och EncryptionType har lagts till i följande cmdletar:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="20708-527">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="20708-528">Lägg till parametern PublicIPAddressVersion i New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="20708-528">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="20708-529">Flytta FileUris för anpassat skripttillägg från offentlig inställning till skyddad inställning</span><span class="sxs-lookup"><span data-stu-id="20708-529">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="20708-530">Lägg till ScaleInPolicy i cmdletarna New-AzVmss, New-AzVmssConfig och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="20708-530">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="20708-531">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="20708-531">Breaking changes</span></span>
    - <span data-ttu-id="20708-532">Parametern UploadSizeInBytes används istället för DiskSizeGB för New-AzDiskConfig när CreateOption är Uppladdning</span><span class="sxs-lookup"><span data-stu-id="20708-532">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="20708-533">PublishingProfile.Source.ManagedImage.Id ersätts med StorageProfile.Source.Id i objektet GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="20708-533">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="20708-534">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="20708-534">Az.DataFactory</span></span>
* <span data-ttu-id="20708-535">Uppdatera ADF .Net SDK-versionen till 4.3.0</span><span class="sxs-lookup"><span data-stu-id="20708-535">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="20708-536">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="20708-536">Az.DataLakeStore</span></span>
* <span data-ttu-id="20708-537">Uppdatera ADLS SDK-version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) innehåller följande korrigeringar</span><span class="sxs-lookup"><span data-stu-id="20708-537">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="20708-538">Undvik att utlösa undantag när det inte går att deserialisera creationtime för inmatning av papperskorg eller katalog.</span><span class="sxs-lookup"><span data-stu-id="20708-538">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="20708-539">Gör inställning tillgänglig per tidsgräns för förfrågan i adlsclient</span><span class="sxs-lookup"><span data-stu-id="20708-539">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="20708-540">Korrigera överföringen av ursprunglig syncflag för badoffset-återställning</span><span class="sxs-lookup"><span data-stu-id="20708-540">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="20708-541">Korrigera EnumerateDirectory för att hämta fortsättningstoken när svar har kontrollerats</span><span class="sxs-lookup"><span data-stu-id="20708-541">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="20708-542">Korrigera bugg i Concat</span><span class="sxs-lookup"><span data-stu-id="20708-542">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="20708-543">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="20708-543">Az.FrontDoor</span></span>
* <span data-ttu-id="20708-544">Åtgärdade diverse stavfel i modul</span><span class="sxs-lookup"><span data-stu-id="20708-544">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="20708-545">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="20708-545">Az.HDInsight</span></span>
* <span data-ttu-id="20708-546">Korrigerade buggen att kunder får felet ”inte en giltig Base-64-sträng” vid användning av Get-AzHDInsightCluster för att hämta klustret med ADLSGen1-lagring.</span><span class="sxs-lookup"><span data-stu-id="20708-546">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="20708-547">Lägg till en parameter med namnet ”ApplicationId” i de tre cmdletarna Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig och New-AzHDInsightCluster så att kunden kan tillhandahålla tjänstens huvudnamn för program-ID för åtkomst till Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="20708-547">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="20708-548">Ändrade Microsoft.Azure.Management.HDInsight från 2.1.0 till 5.1.0</span><span class="sxs-lookup"><span data-stu-id="20708-548">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="20708-549">Fem cmdletar har tagits bort:</span><span class="sxs-lookup"><span data-stu-id="20708-549">Removed five cmdlets:</span></span>
    - <span data-ttu-id="20708-550">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="20708-550">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="20708-551">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="20708-551">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="20708-552">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="20708-552">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="20708-553">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="20708-553">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="20708-554">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="20708-554">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="20708-555">Tre cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="20708-555">Added three cmdlets:</span></span>
    - <span data-ttu-id="20708-556">Get-AzHDInsightMonitoring som ersätter Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="20708-556">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="20708-557">Enable-AzHDInsightMonitoring som ersätter Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="20708-557">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="20708-558">Disable-AzHDInsightMonitoring som ersätter Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="20708-558">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="20708-559">Korrigerade cmdleten Get-AzHDInsightProperties för att stödja hämtning av funktionsinformation från en viss plats.</span><span class="sxs-lookup"><span data-stu-id="20708-559">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="20708-560">Parameteruppsättningarna (Spark1 och Spark2) har tagits bort från Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="20708-560">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="20708-561">Lägg till exempel för cmdleten Add-AzHDInsightSecurityProfile till hjälpdokumenten.</span><span class="sxs-lookup"><span data-stu-id="20708-561">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="20708-562">Ändrade utdatatyp för följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="20708-562">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="20708-563">Ändrade utdatatyp för Get-AzHDInsightProperties från CapabilitiesResponse till AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="20708-563">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="20708-564">Ändrade utdatatyp för Remove-AzHDInsightCluster från ClusterGetResponse till bool.</span><span class="sxs-lookup"><span data-stu-id="20708-564">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="20708-565">Ändrade utdatatyp för Set-AzHDInsightGatewaySettings HttpConnectivitySettings till GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="20708-565">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="20708-566">Lade till testfall för vissa scenarier.</span><span class="sxs-lookup"><span data-stu-id="20708-566">Added some scenario test cases.</span></span>
* <span data-ttu-id="20708-567">Ta bort vissa alias: Add-AzHDInsightConfigValues, Get-AzHDInsightProperties.</span><span class="sxs-lookup"><span data-stu-id="20708-567">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="20708-568">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="20708-568">Az.IotHub</span></span>
* <span data-ttu-id="20708-569">Icke-bakåtkompatibla ändringar:</span><span class="sxs-lookup"><span data-stu-id="20708-569">Breaking changes:</span></span>
    - <span data-ttu-id="20708-570">Cmdleten Add-AzIotHubEventHubConsumerGroup har inte längre stöd för parametern EventHubEndpointName och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="20708-570">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="20708-571">Parameteruppsättningen __AllParameterSets för cmdleten Add-AzIotHubEventHubConsumerGroup har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="20708-571">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="20708-572">Cmdleten Get-AzIotHubEventHubConsumerGroup har inte längre stöd för parametern EventHubEndpointName och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="20708-572">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="20708-573">Parameteruppsättningen __AllParameterSets för cmdleten Get-AzIotHubEventHubConsumerGroup har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="20708-573">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="20708-574">Egenskapen OperationsMonitoringProperties av typen Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="20708-574">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="20708-575">Egenskapen OperationsMonitoringProperties av typen Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="20708-575">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="20708-576">Cmdleten New-AzIotHubExportDevice stöder inte längre aliaset New-AzIotHubExportDevices.</span><span class="sxs-lookup"><span data-stu-id="20708-576">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="20708-577">Cmdleten New-AzIotHubImportDevice stöder inte längre aliaset New-AzIotHubImportDevices.</span><span class="sxs-lookup"><span data-stu-id="20708-577">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="20708-578">Cmdleten Remove-AzIotHubEventHubConsumerGroup har inte längre stöd för parametern EventHubEndpointName och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="20708-578">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="20708-579">Parameteruppsättningen __AllParameterSets för cmdleten Remove-AzIotHubEventHubConsumerGroup har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="20708-579">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="20708-580">Cmdleten Set-AzIotHub har inte längre stöd för parametern OperationsMonitoringProperties och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="20708-580">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="20708-581">Parameteruppsättningen UpdateOperationsMonitoringProperties för cmdleten Set-AzIotHub har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="20708-581">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="20708-582">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="20708-582">Az.RecoveryServices</span></span>
* <span data-ttu-id="20708-583">Azure Site Recovery-stöd för att konfigurera nätverksresurser som NSG, offentliga IP-adresser och interna lastbalanserare för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="20708-583">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="20708-584">Azure Site Recovery-stöd för att skriva till hanterad disk för vMWare till Azure.</span><span class="sxs-lookup"><span data-stu-id="20708-584">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="20708-585">Azure Site Recovery-stöd för NIC-reduktion för vMWare till Azure.</span><span class="sxs-lookup"><span data-stu-id="20708-585">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="20708-586">Azure Site Recovery-stöd för accelererat nätverk för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="20708-586">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="20708-587">Azure Site Recovery-stöd för automatisk uppdatering av agent för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="20708-587">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="20708-588">Azure Site Recovery-stöd för Standard SSD för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="20708-588">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="20708-589">Azure Site Recovery-stöd för tvåstegskryptering i Azure Disk Encryption för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="20708-589">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="20708-590">Azure Site Recovery-stöd för att skydda nyligen tillagda diskar för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="20708-590">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="20708-591">En funktion för mjuk borttagning av virtuella datorer samt tester för mjuk borttagning har tagits bort</span><span class="sxs-lookup"><span data-stu-id="20708-591">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="20708-592">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="20708-592">Az.Resources</span></span>
* <span data-ttu-id="20708-593">Uppdatera beroendesammansättning för Microsoft.Extensions.Caching.Memory från 1.1.1 till 2.2</span><span class="sxs-lookup"><span data-stu-id="20708-593">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="20708-594">Az.Network</span><span class="sxs-lookup"><span data-stu-id="20708-594">Az.Network</span></span>
* <span data-ttu-id="20708-595">Ändra alla cmdletar för PrivateEndpointConnection så att de stöder generiska tjänstleverantörer.</span><span class="sxs-lookup"><span data-stu-id="20708-595">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="20708-596">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="20708-596">Updated cmdlet:</span></span>
        - <span data-ttu-id="20708-597">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="20708-597">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="20708-598">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="20708-598">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="20708-599">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="20708-599">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="20708-600">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="20708-600">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="20708-601">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="20708-601">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="20708-602">Lägg till ny cmdlet för PrivateLinkResource så att det också stöder generiska tjänstleverantörer.</span><span class="sxs-lookup"><span data-stu-id="20708-602">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="20708-603">Ny cmdlet:</span><span class="sxs-lookup"><span data-stu-id="20708-603">New cmdlet:</span></span>
        - <span data-ttu-id="20708-604">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="20708-604">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="20708-605">Lägg till nya fält och parametrar för funktionen Proxy Protocol V2.</span><span class="sxs-lookup"><span data-stu-id="20708-605">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="20708-606">Lägg till egenskapen EnableProxyProtocol i PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="20708-606">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="20708-607">Lägg till egenskapen LinkIdentifier i PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="20708-607">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="20708-608">Uppdaterade New-AzPrivateLinkService för att lägga till den nya valfria parametern EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="20708-608">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="20708-609">Korrigera felaktig beskrivning av parameter i referensdokumentationen för New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="20708-609">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="20708-610">Nya cmdletar som stöder Azure-brandväggsprincipen</span><span class="sxs-lookup"><span data-stu-id="20708-610">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="20708-611">Lägg till stöd för den underordnade resursen RouteTables för VirtualHub</span><span class="sxs-lookup"><span data-stu-id="20708-611">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="20708-612">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="20708-612">New cmdlets added:</span></span>
        - <span data-ttu-id="20708-613">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="20708-613">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="20708-614">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="20708-614">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="20708-615">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="20708-615">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="20708-616">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="20708-616">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="20708-617">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="20708-617">Set-AzVirtualHub</span></span>
* <span data-ttu-id="20708-618">Lägg till stöd för ny egenskaps-SKU för VirtualHub och VirtualWANType för VirtualWan</span><span class="sxs-lookup"><span data-stu-id="20708-618">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="20708-619">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="20708-619">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="20708-620">New-AzVirtualHub: lade till parameter-SKU</span><span class="sxs-lookup"><span data-stu-id="20708-620">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="20708-621">Update-AzVirtualHub: lade till parameter-SKU</span><span class="sxs-lookup"><span data-stu-id="20708-621">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="20708-622">New-AzVirtualWan: lade till parametern VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="20708-622">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="20708-623">Update-AzVirtualWan: lade till parametern VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="20708-623">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="20708-624">Lägg till stöd för egenskapen EnableInternetSecurity för HubVnetConnection, VpnConnection och ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="20708-624">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="20708-625">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="20708-625">New cmdlets added:</span></span>
        - <span data-ttu-id="20708-626">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="20708-626">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="20708-627">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="20708-627">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="20708-628">New-AzureRmVirtualHubVnetConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="20708-628">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="20708-629">New-AzureRmVpnConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="20708-629">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="20708-630">Update-AzureRmVpnConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="20708-630">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="20708-631">New-AzureRmExpressRouteConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="20708-631">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="20708-632">Set-AzureRmExpressRouteConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="20708-632">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="20708-633">Lägg till stöd för att konfigurera TopLevel WebApplicationFirewall-princip</span><span class="sxs-lookup"><span data-stu-id="20708-633">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="20708-634">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="20708-634">New cmdlets added:</span></span>
        - <span data-ttu-id="20708-635">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="20708-635">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="20708-636">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="20708-636">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="20708-637">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="20708-637">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="20708-638">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="20708-638">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="20708-639">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="20708-639">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="20708-640">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="20708-640">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="20708-641">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="20708-641">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="20708-642">New-AzApplicationGatewayFirewallPolicy: parametrarna PolicySetting, ManagedRule har lagts till</span><span class="sxs-lookup"><span data-stu-id="20708-642">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="20708-643">Stöd för operator för geomatchning har lagts till på CustomRule</span><span class="sxs-lookup"><span data-stu-id="20708-643">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="20708-644">Geomatchning har lagts till i operatorn på FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="20708-644">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="20708-645">Stöd har lagts till för brandväggsprinciperna perListener och perSite</span><span class="sxs-lookup"><span data-stu-id="20708-645">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="20708-646">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="20708-646">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="20708-647">New-AzApplicationGatewayHttpListener: parametrarna FirewallPolicy, FirewallPolicyId har lagts till</span><span class="sxs-lookup"><span data-stu-id="20708-647">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="20708-648">New-AzApplicationGatewayPathRuleConfig: parametrarna FirewallPolicy, FirewallPolicyId har lagts till</span><span class="sxs-lookup"><span data-stu-id="20708-648">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="20708-649">Åtgärdat så att nödvändigt undernät med namnet AzureBastionSubnet i PSBastion kan vara skiftlägesokänsligt</span><span class="sxs-lookup"><span data-stu-id="20708-649">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="20708-650">Stöd för mål-FQDN:er i nätverksregler och översatt FQDN i NAT-regler för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="20708-650">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="20708-651">Lägg till stöd för resursen RouteTables för IpGroup på den högsta nivån</span><span class="sxs-lookup"><span data-stu-id="20708-651">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="20708-652">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="20708-652">New cmdlets added:</span></span>
        - <span data-ttu-id="20708-653">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="20708-653">New-AzIpGroup</span></span>
        - <span data-ttu-id="20708-654">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="20708-654">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="20708-655">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="20708-655">Get-AzIpGroup</span></span>
        - <span data-ttu-id="20708-656">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="20708-656">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="20708-657">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="20708-657">Az.ServiceFabric</span></span>
* <span data-ttu-id="20708-658">Ta bort cmdleten Add-AzServiceFabricApplicationCertificate eftersom det här scenariot omfattas av Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="20708-658">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="20708-659">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="20708-659">Az.Sql</span></span>
* <span data-ttu-id="20708-660">Stöd har lagts till för återställning av utelämnade databaser på hanterade instanser.</span><span class="sxs-lookup"><span data-stu-id="20708-660">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="20708-661">Inaktuella gamla cmdletar för granskning från kod.</span><span class="sxs-lookup"><span data-stu-id="20708-661">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="20708-662">Tog bort inaktuella alias:</span><span class="sxs-lookup"><span data-stu-id="20708-662">Removed deprecated aliases:</span></span>
* <span data-ttu-id="20708-663">Get-AzSqlDatabaseIndexRecommendations (använd Get-AzSqlDatabaseIndexRecommendation istället)</span><span class="sxs-lookup"><span data-stu-id="20708-663">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="20708-664">Get-AzSqlDatabaseRestorePoints (använd Get-AzSqlDatabaseRestorePoint istället)</span><span class="sxs-lookup"><span data-stu-id="20708-664">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="20708-665">Ta bort cmdleten Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="20708-665">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="20708-666">Ta bort alias för inaktuella cmdletar för inställningar för utvärdering av säkerhetsrisk</span><span class="sxs-lookup"><span data-stu-id="20708-666">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="20708-667">Inaktualisera cmdletar för inställningar för avancerad hotidentifiering</span><span class="sxs-lookup"><span data-stu-id="20708-667">Deprecate Advanced Threat Detection Settings cmdlets</span></span> 
* <span data-ttu-id="20708-668">Lägga till cmdletar för att inaktivera och aktivera känslighetsrekommendationer på kolumner i en databas.</span><span class="sxs-lookup"><span data-stu-id="20708-668">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="20708-669">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="20708-669">Az.Storage</span></span>
* <span data-ttu-id="20708-670">Stöd för att aktivera stora filresurser vid skapande eller uppdatering av lagringskonto</span><span class="sxs-lookup"><span data-stu-id="20708-670">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="20708-671">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="20708-671">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="20708-672">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="20708-672">Set-AzStorageAccount</span></span>
* <span data-ttu-id="20708-673">När du stänger/hämtar en filreferens kan du hoppa över kontrollen av huruvida indatasökvägen är en filkatalog eller en fil för att undvika problem med objekt som har status DeletePending</span><span class="sxs-lookup"><span data-stu-id="20708-673">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="20708-674">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="20708-674">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="20708-675">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="20708-675">Close-AzStorageFileHandle</span></span>
    
## <a name="280---october-2019"></a><span data-ttu-id="20708-676">2.8.0 – oktober 2019</span><span class="sxs-lookup"><span data-stu-id="20708-676">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="20708-677">Allmänt</span><span class="sxs-lookup"><span data-stu-id="20708-677">General</span></span>
* <span data-ttu-id="20708-678">AZ. HealthcareApis 1.0.0-version</span><span class="sxs-lookup"><span data-stu-id="20708-678">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="20708-679">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="20708-679">Az.Accounts</span></span>
* <span data-ttu-id="20708-680">Uppdatera telemetri och URL-omskrivning för genererade moduler, korrigera Windows-enhetstester.</span><span class="sxs-lookup"><span data-stu-id="20708-680">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="20708-681">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="20708-681">Az.ApiManagement</span></span>
* <span data-ttu-id="20708-682">**Set-AzApiManagementApi** – Tillagt stöd för att uppdatera Api till ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="20708-682">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="20708-683">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="20708-683">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="20708-684">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="20708-684">Az.Automation</span></span>
* <span data-ttu-id="20708-685">Åtgärdade cmdleten New-AzureAutomationSoftwareUpdateConfiguration för parametern för inställning av Linux-omstart.</span><span class="sxs-lookup"><span data-stu-id="20708-685">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span> 

#### <a name="azbatch"></a><span data-ttu-id="20708-686">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="20708-686">Az.Batch</span></span>
* <span data-ttu-id="20708-687">**Get-AzBatchNodeAgentSku** är inaktuell och ersätts av **Get-AzBatchSupportImage** i version 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="20708-687">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="20708-688">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="20708-688">Az.Compute</span></span>
* <span data-ttu-id="20708-689">Lägg till parametrarna Priority, EvictionPolicy och MaxPrice till cmdletarna New-AzVM och New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="20708-689">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="20708-690">Korrigera varningsmeddelande och hjälpdokument för cmdletarna Add-AzVMAdditionalUnattendContent och Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="20708-690">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="20708-691">Åtgärda – skipVmBackup-undantag för virtuella Linux-datorer med hanterade diskar för Set-AzVMDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="20708-691">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span> 
* <span data-ttu-id="20708-692">Åtgärda fel i uppdatera krypteringsinställningarna i set-AzVMDiskEncryptionExtension, scenario i två steg.</span><span class="sxs-lookup"><span data-stu-id="20708-692">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="20708-693">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="20708-693">Az.DataFactory</span></span>
* <span data-ttu-id="20708-694">Lägga till CRUD-kommandon för ADF V2-dataflödet: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow och Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="20708-694">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="20708-695">Lägger till åtgärdskommandon för ADF V2-dataflödesfelsökningssession: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand och Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="20708-695">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="20708-696">Uppdatera ADF .Net SDK-versionen till 4.2.0</span><span class="sxs-lookup"><span data-stu-id="20708-696">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="20708-697">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="20708-697">Az.DataLakeStore</span></span>
* <span data-ttu-id="20708-698">Korrigera kontovalidering så att konton med ”-” kan skickas utan domän</span><span class="sxs-lookup"><span data-stu-id="20708-698">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="20708-699">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="20708-699">Az.HealthcareApis</span></span>
* <span data-ttu-id="20708-700">PowerShell-versionen har uppdaterats till 1.0.0</span><span class="sxs-lookup"><span data-stu-id="20708-700">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="20708-701">Uppdaterade SDK-versionen till 1.0.2</span><span class="sxs-lookup"><span data-stu-id="20708-701">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="20708-702">Uppdatera i tester för att referera till en ny SDK-version</span><span class="sxs-lookup"><span data-stu-id="20708-702">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="20708-703">Utdatastrukturen har uppdaterats från kapslad till förenklad.</span><span class="sxs-lookup"><span data-stu-id="20708-703">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="20708-704">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="20708-704">Az.IotHub</span></span>
* <span data-ttu-id="20708-705">Lägg till ny routningskälla: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="20708-705">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="20708-706">Mindre felkorrigering: Get-AzIothub returnerar inte subscriptionId</span><span class="sxs-lookup"><span data-stu-id="20708-706">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span> 

#### <a name="azmonitor"></a><span data-ttu-id="20708-707">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="20708-707">Az.Monitor</span></span>
* <span data-ttu-id="20708-708">Nya åtgärdsgruppsmottagare har lagts till för åtgärdsgrupp   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="20708-708">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="20708-709">Använd vanligt aviseringsschema som är aktiverat för mottagarna.</span><span class="sxs-lookup"><span data-stu-id="20708-709">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="20708-710">Detta gäller inte för SMS, push för Azure-app, ITSM och röstmottagare</span><span class="sxs-lookup"><span data-stu-id="20708-710">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="20708-711">Webhooks har nu stöd för Azure Active Directory-autentisering.</span><span class="sxs-lookup"><span data-stu-id="20708-711">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="20708-712">Az.Network</span><span class="sxs-lookup"><span data-stu-id="20708-712">Az.Network</span></span>
* <span data-ttu-id="20708-713">Lägg till ny cmdlet Get-AzAvailableServiceAlias som kan anropas för att hämta de alias som kan användas för tjänstslutpunktsprinciper.</span><span class="sxs-lookup"><span data-stu-id="20708-713">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="20708-714">Stöd för tillägg av trafikväljare har lagts till i gatewayanslutningar för virtuella nätverk</span><span class="sxs-lookup"><span data-stu-id="20708-714">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="20708-715">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="20708-715">New cmdlets added:</span></span>
        - <span data-ttu-id="20708-716">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="20708-716">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="20708-717">Cmdletar har uppdaterats med valfri parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="20708-717">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="20708-718">Lägg till stöd för ESP- och AH-protokoll i konfiguration av nätverkssäkerhetsregler</span><span class="sxs-lookup"><span data-stu-id="20708-718">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="20708-719">Uppdaterade cmdletar:</span><span class="sxs-lookup"><span data-stu-id="20708-719">Updated cmdlets:</span></span>
        - <span data-ttu-id="20708-720">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="20708-720">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="20708-721">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="20708-721">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="20708-722">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="20708-722">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="20708-723">Förbättra hanteringen av undantag i Cortex-cmdletar</span><span class="sxs-lookup"><span data-stu-id="20708-723">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="20708-724">Nya generationer och SKU:er för VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="20708-724">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="20708-725">Introducera nya generationer för VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="20708-725">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="20708-726">Introducera nya SKU:er med högt dataflöde för VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="20708-726">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="20708-727">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="20708-727">Az.RedisCache</span></span>
* <span data-ttu-id="20708-728">Uppdaterad referensdokumentation för ”set-AzRedisCache” för att inkludera saknade värden för parametern ”size”</span><span class="sxs-lookup"><span data-stu-id="20708-728">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="20708-729">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="20708-729">Az.Sql</span></span>
* <span data-ttu-id="20708-730">Lägg till stöd för inställningen Active Directory administratör på den hanterade instansen</span><span class="sxs-lookup"><span data-stu-id="20708-730">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="20708-731">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="20708-731">Az.Storage</span></span>
* <span data-ttu-id="20708-732">Uppdatera Lagringsklientbibliotek till 11.1.0</span><span class="sxs-lookup"><span data-stu-id="20708-732">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="20708-733">Lista containrar med hanteringsplans-API, kommer att listas med NextPageLink</span><span class="sxs-lookup"><span data-stu-id="20708-733">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="20708-734">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="20708-734">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="20708-735">Lista lagringskonton från prenumerationen, kommer att listas med NextPageLink</span><span class="sxs-lookup"><span data-stu-id="20708-735">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="20708-736">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="20708-736">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="20708-737">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="20708-737">Az.StorageSync</span></span>
* <span data-ttu-id="20708-738">Åtgärda problemet 9810 i Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="20708-738">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="20708-739">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="20708-739">Az.Websites</span></span>
* <span data-ttu-id="20708-740">Set-AzWebApp – uppdatering av ASP för en app misslyckades</span><span class="sxs-lookup"><span data-stu-id="20708-740">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="20708-741">2.7.0 – september 2019</span><span class="sxs-lookup"><span data-stu-id="20708-741">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="20708-742">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="20708-742">Az.ApiManagement</span></span>
* <span data-ttu-id="20708-743">Uppdatera ”-Format”-parameterbeskrivningen i ”Set-AzApiManagementPolicy”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="20708-743">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="20708-744">Referenser för den föråldrade cmdleten ”Update-AzApiManagementDeployment” har tagits bort från referensdokumentationen.</span><span class="sxs-lookup"><span data-stu-id="20708-744">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="20708-745">Använd ”Set-AzApiManagement” i stället.</span><span class="sxs-lookup"><span data-stu-id="20708-745">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="20708-746">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="20708-746">Az.Automation</span></span>
* <span data-ttu-id="20708-747">Stavfel har korrigerats i exempel i referensdokumentationen för ”Register-AzAutomationDscNode”</span><span class="sxs-lookup"><span data-stu-id="20708-747">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="20708-748">Klargörande har lagts till om OS-begränsningar för Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="20708-748">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="20708-749">Null-referensundantag har korrigerats för -Wait-alternativet i Start-AzAutomationRunbook-cmdleten.</span><span class="sxs-lookup"><span data-stu-id="20708-749">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="20708-750">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="20708-750">Az.Compute</span></span>
* <span data-ttu-id="20708-751">Lägg till UploadSizeInBytes-parameter till New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="20708-751">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="20708-752">Lägg till Incremental-parameter till New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="20708-752">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="20708-753">Lägg till en funktion för virtuella datorer med låg prioritet:</span><span class="sxs-lookup"><span data-stu-id="20708-753">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="20708-754">MaxPrice-, EvictionPolicy- och Priority-parametrar har lagts till i New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="20708-754">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="20708-755">MaxPrice-parametern har lagts till i New-AzVmssConfig-, Update-AzVM- och Update-AzVmss-cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="20708-755">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="20708-756">Åtgärda problem med VM-referenser för Get-AzAvailabilitySet-cmdleten när alla tillgänglighetsuppsättningar i prenumerationen visas.</span><span class="sxs-lookup"><span data-stu-id="20708-756">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="20708-757">Korrigera null-undantaget för Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="20708-757">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="20708-758">Korrigera VHD-metoden för sökning relativt till slut.</span><span class="sxs-lookup"><span data-stu-id="20708-758">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="20708-759">Åtgärda UltraSSD-problem för New-AzVM och Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="20708-759">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="20708-760">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="20708-760">Az.DataFactory</span></span>
* <span data-ttu-id="20708-761">Lägger till 3 nya kommandon för ADF V2 – Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription och Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="20708-761">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="20708-762">ADF .Net SDK har uppdaterats till 4.1.3</span><span class="sxs-lookup"><span data-stu-id="20708-762">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="20708-763">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="20708-763">Az.HDInsight</span></span>
* <span data-ttu-id="20708-764">Anrop för icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="20708-764">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="20708-765">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="20708-765">Az.IotHub</span></span>
* <span data-ttu-id="20708-766">Lägg till stöd för att anropa redundans för en IotHub till den geo-länkade katastrofåterställningsregionen.</span><span class="sxs-lookup"><span data-stu-id="20708-766">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="20708-767">Lägg till stöd för att hantera meddelandeberikning för en IotHub.</span><span class="sxs-lookup"><span data-stu-id="20708-767">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="20708-768">Nya cmdlet:ar är:</span><span class="sxs-lookup"><span data-stu-id="20708-768">New cmdlets are:</span></span>
    - <span data-ttu-id="20708-769">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="20708-769">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="20708-770">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="20708-770">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="20708-771">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="20708-771">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="20708-772">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="20708-772">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="20708-773">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="20708-773">Az.Monitor</span></span>
* <span data-ttu-id="20708-774">Pekar på den senaste Monitor SDK:n, dvs. 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="20708-774">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="20708-775">Lägger till bakåtkompatibla ändringar i Metrics-cmdletarna, dvs. enhetsuppräkningen stöder flera nya värden.</span><span class="sxs-lookup"><span data-stu-id="20708-775">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="20708-776">Detta är skrivskyddade cmdletar, så det förekommer inga ändringar i inmatningen för cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="20708-776">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="20708-777">API-versionen för **ActionGroups**-begäranden är nu **2019-06-01**. Tidigare var den **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="20708-777">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="20708-778">Test av scenarier har uppdaterats för att anpassas till den här ändringen.</span><span class="sxs-lookup"><span data-stu-id="20708-778">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="20708-779">Ett nytt obligatoriskt argument har lagts till för konstruktorerna för klasserna **EmailReceiver** och **WebhookReceiver** – ett booleskt värde med namnet **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="20708-779">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="20708-780">Värdet är för närvarande fast till **false** så att den här icke-bakåtkompatibla ändringen är dold från cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="20708-780">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="20708-781">**Obs!** Det här är en tillfällig ändring som måste verifieras av Alerts-teamet.</span><span class="sxs-lookup"><span data-stu-id="20708-781">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="20708-782">Ordningen på argumenten för konstruktorn för klassen **Source** (relaterad till klassen **ScheduledQueryRuleSource**) har ändrats från den tidigare SDK:n.</span><span class="sxs-lookup"><span data-stu-id="20708-782">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="20708-783">Den här ändringen krävde korrigering av två enhetstest: de kompilerades, men testerna skickades inte.</span><span class="sxs-lookup"><span data-stu-id="20708-783">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="20708-784">Ordningen på argumenten för konstruktorn för klassen **AlertingAction** (relaterad till klassen **ScheduledQueryRuleSource**) har ändrats från den tidigare SDK:n.</span><span class="sxs-lookup"><span data-stu-id="20708-784">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="20708-785">Den här ändringen krävde korrigering av två enhetstest: de kompilerades, men testerna skickades inte.</span><span class="sxs-lookup"><span data-stu-id="20708-785">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="20708-786">Stöd för kriterier för dynamiskt tröskelvärde för måttavisering v2</span><span class="sxs-lookup"><span data-stu-id="20708-786">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="20708-787">New-AzMetricAlertRuleV2Criteria: skapar nu även kriterier för dynamiskt tröskelvärde</span><span class="sxs-lookup"><span data-stu-id="20708-787">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="20708-788">Add-AzMetricAlertRuleV2: accepterar nu även kriterier för dynamiskt tröskelvärde</span><span class="sxs-lookup"><span data-stu-id="20708-788">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="20708-789">Förbättringar i schemalagd frågeregel (SQR)</span><span class="sxs-lookup"><span data-stu-id="20708-789">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="20708-790">Cmdletar accepterar ”Location”-parameter i båda formaten, antingen platsen (t.ex. eastus) eller platsens visningsnamn (t.ex. USA, östra)</span><span class="sxs-lookup"><span data-stu-id="20708-790">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="20708-791">”Enabled”-parametern illustreras korrekt i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="20708-791">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="20708-792">Exempel för den valfria parametern ”ActionGroup” har lagts till</span><span class="sxs-lookup"><span data-stu-id="20708-792">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="20708-793">Förbättrade hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="20708-793">Overall improved help files</span></span>
* <span data-ttu-id="20708-794">Åtgärda bugg då omfattningstypen fastställs för ”Set-AzActionRule”</span><span class="sxs-lookup"><span data-stu-id="20708-794">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="20708-795">Az.Network</span><span class="sxs-lookup"><span data-stu-id="20708-795">Az.Network</span></span>
* <span data-ttu-id="20708-796">Korrigera felaktigt exempel i referensdokumentationen för ”New-AzApplicationGateway”</span><span class="sxs-lookup"><span data-stu-id="20708-796">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="20708-797">Lägg till anmärkning i ”Get-AzNetworkWatcherPacketCapture”-referensdokumentationen om hämtning av alla egenskaper för en paketinsamling</span><span class="sxs-lookup"><span data-stu-id="20708-797">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="20708-798">Exempel har korrigerats i ”Test-AzNetworkWatcherIPFlow”-referensdokumentationen för korrekt uppräkning av nätverkskort</span><span class="sxs-lookup"><span data-stu-id="20708-798">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="20708-799">Förbättrad tolkning av molnundantag för att visa eventuell ytterligare information</span><span class="sxs-lookup"><span data-stu-id="20708-799">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="20708-800">Förbättrad tolkning av molnundantag för att hantera ytterligare en typ av SDK-undantag</span><span class="sxs-lookup"><span data-stu-id="20708-800">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="20708-801">Felaktig mappning av säkerhetsregelmodeller har korrigerats</span><span class="sxs-lookup"><span data-stu-id="20708-801">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="20708-802">Egenskaper har lagts till för nätverksgränssnittet för funktionen Privat IP</span><span class="sxs-lookup"><span data-stu-id="20708-802">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="20708-803">Egenskapen ”PrivateEndpoint” har lagts till som en typ av PSResourceId till PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="20708-803">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="20708-804">Egenskapen ”PrivateLinkConnectionProperties” har lagts till som en typ av PSIpConfigurationConnectivityInformation till PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="20708-804">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="20708-805">Modellklassen PSIpConfigurationConnectivityInformation har lagts till</span><span class="sxs-lookup"><span data-stu-id="20708-805">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="20708-806">ApplicationRuleProtocolType ”mssql” har lagts till för Azure Firewall-resurs</span><span class="sxs-lookup"><span data-stu-id="20708-806">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="20708-807">MultiLink-stöd i virtuellt WAN</span><span class="sxs-lookup"><span data-stu-id="20708-807">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="20708-808">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="20708-808">New cmdlets</span></span>
        - <span data-ttu-id="20708-809">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="20708-809">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="20708-810">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="20708-810">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="20708-811">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="20708-811">Updated cmdlet:</span></span>
        - <span data-ttu-id="20708-812">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="20708-812">New-VpnSite</span></span>
        - <span data-ttu-id="20708-813">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="20708-813">Update-VpnSite</span></span>
        - <span data-ttu-id="20708-814">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="20708-814">New-VpnConnection</span></span>
        - <span data-ttu-id="20708-815">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="20708-815">Update-VpnConnection</span></span>
* <span data-ttu-id="20708-816">Dokument för vissa PowerShell-exempel har korrigerats så att Az-cmdletar används i stället för AzureRM-cmdletar</span><span class="sxs-lookup"><span data-stu-id="20708-816">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="20708-817">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="20708-817">Az.RecoveryServices</span></span>
* <span data-ttu-id="20708-818">Uppdatera AzureVMpolicy-objekt med ProtectedItemsCount-attribut</span><span class="sxs-lookup"><span data-stu-id="20708-818">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="20708-819">Ytterligare tester har lagts till för VM-princip och återställning av ursprungligt lagringskonto</span><span class="sxs-lookup"><span data-stu-id="20708-819">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="20708-820">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="20708-820">Az.Resources</span></span>
* <span data-ttu-id="20708-821">Åtgärda fel där det inte gick att anropa New-AzRoleAssignment utan parametern Scope.</span><span class="sxs-lookup"><span data-stu-id="20708-821">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="20708-822">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="20708-822">Az.ServiceFabric</span></span>
* <span data-ttu-id="20708-823">Stavfel har korrigerats i exempel för ”Update-AzServiceFabricReliability”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="20708-823">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="20708-824">Lägger till nya cmdletar för att hantera program och tjänster:</span><span class="sxs-lookup"><span data-stu-id="20708-824">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="20708-825">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="20708-825">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="20708-826">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="20708-826">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="20708-827">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="20708-827">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="20708-828">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="20708-828">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="20708-829">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="20708-829">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="20708-830">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="20708-830">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="20708-831">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="20708-831">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="20708-832">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="20708-832">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="20708-833">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="20708-833">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="20708-834">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="20708-834">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="20708-835">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="20708-835">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="20708-836">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="20708-836">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="20708-837">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="20708-837">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="20708-838">Service Fabric SDK har uppgraderats till version 1.2.0 som använder Service Fabric-resursprovidern med API-version 2019-03-01.</span><span class="sxs-lookup"><span data-stu-id="20708-838">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="20708-839">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="20708-839">Az.SignalR</span></span>
* <span data-ttu-id="20708-840">Lägg till Update-, Restart-, CheckNameAvailability- och GetUsage-cmdletar</span><span class="sxs-lookup"><span data-stu-id="20708-840">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="20708-841">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="20708-841">Az.Sql</span></span>
* <span data-ttu-id="20708-842">Uppdatera exempel i referensdokumentationen för ”Get-AzSqlElasticPool”</span><span class="sxs-lookup"><span data-stu-id="20708-842">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="20708-843">vCore-exempel för att skapa en elastisk pool (New-AzSqlElasticPool) har lagts till.</span><span class="sxs-lookup"><span data-stu-id="20708-843">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="20708-844">Ta bort verifieringen av EmailAddresses och kontrollen som bekräftar att EmailAdmins inte är falskt när EmailAddresses är tomt i Set-AzSqlServerAdvancedThreatProtectionPolicy och Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="20708-844">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="20708-845">Server-/databasgranskningsinställningar kan tas bort när det finns flera diagnostikinställningar som aktiverar granskningskategorin.</span><span class="sxs-lookup"><span data-stu-id="20708-845">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="20708-846">Åtgärda verifiering av e-postadresser i flera Sql Vulnerability Assessment-cmdletar (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting och Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="20708-846">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="20708-847">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="20708-847">Az.Storage</span></span>
* <span data-ttu-id="20708-848">Exempel i referensdokumentationen för ”Get-AzStorageAccountKey” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="20708-848">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="20708-849">Vid upp- och nedladdning av en Azure-fil kan SMB-egenskaperna för källfilen (t.ex. filattribut, tidpunkten då filen skapades och tidpunkten för den senaste skrivningen) sparas i målfilen</span><span class="sxs-lookup"><span data-stu-id="20708-849">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="20708-850">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="20708-850">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="20708-851">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="20708-851">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="20708-852">Korrigera problem med uppladdningen av blockblob med egenskaper/metadata för ImmutabilityPolicy i containrar.</span><span class="sxs-lookup"><span data-stu-id="20708-852">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="20708-853">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="20708-853">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="20708-854">Stöd för hantering av Azure-filresurser med API för hanteringsplan</span><span class="sxs-lookup"><span data-stu-id="20708-854">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="20708-855">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="20708-855">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="20708-856">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="20708-856">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="20708-857">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="20708-857">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="20708-858">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="20708-858">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="20708-859">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="20708-859">Az.Websites</span></span>
* <span data-ttu-id="20708-860">Åtgärdar problemet där webapp-taggar togs bort när appen migrerades till nya ASP</span><span class="sxs-lookup"><span data-stu-id="20708-860">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="20708-861">Åtgärda Publish-AzureWebapp så att det fungerar i Linux och Windows</span><span class="sxs-lookup"><span data-stu-id="20708-861">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="20708-862">Uppdatera exempel i ”Get-AzWebAppPublishingProfile”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="20708-862">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="20708-863">2.6.0 – augusti 2019</span><span class="sxs-lookup"><span data-stu-id="20708-863">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="20708-864">Allmänt</span><span class="sxs-lookup"><span data-stu-id="20708-864">General</span></span>
* <span data-ttu-id="20708-865">Åtgärdade diverse skrivfel i flera moduler</span><span class="sxs-lookup"><span data-stu-id="20708-865">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="20708-866">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="20708-866">Az.Accounts</span></span>
* <span data-ttu-id="20708-867">Stöd för användartilldelat MSI i Azure Functions-autentisering (#9479)</span><span class="sxs-lookup"><span data-stu-id="20708-867">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="20708-868">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="20708-868">Az.Aks</span></span>
* <span data-ttu-id="20708-869">Åtgärda problem med utdata för "Get-AzAks"</span><span class="sxs-lookup"><span data-stu-id="20708-869">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="20708-870">Mer information här: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="20708-870">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="20708-871">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="20708-871">Az.ApiManagement</span></span>
* <span data-ttu-id="20708-872">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="20708-872">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="20708-873">Uppdatera .net-NuGet-versionen, som inte tillämpar begränsningar för productId, apiId och userId</span><span class="sxs-lookup"><span data-stu-id="20708-873">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="20708-874">**Get-AzApiManagementProduct** – Lade till stöd för frågekörning mot produkter via API.</span><span class="sxs-lookup"><span data-stu-id="20708-874">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="20708-875">**New-AzApiManagementApiRevision** – Korrigering för problem där ApiRevisionDescription inte angavs vid skapande av ny API-revision https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="20708-875">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="20708-876">Åtgärdade skrivfel i modellen "PsApiManagementOAuth2AuthrozationServer" till "PsApiManagementOAuth2AuthorizationServer"</span><span class="sxs-lookup"><span data-stu-id="20708-876">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="20708-877">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="20708-877">Az.Batch</span></span>
* <span data-ttu-id="20708-878">Åtgärdade skrivfel i hjälpmeddelande och dokumentation till att skriva Windows med versaler</span><span class="sxs-lookup"><span data-stu-id="20708-878">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="20708-879">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="20708-879">Az.Cdn</span></span>
* <span data-ttu-id="20708-880">Åtgärdade skrivfel i CDN-modulens konverteringshjälp</span><span class="sxs-lookup"><span data-stu-id="20708-880">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="20708-881">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="20708-881">Az.Compute</span></span>
* <span data-ttu-id="20708-882">Lägg till VmssId i New-AzVMConfig-cmdleten</span><span class="sxs-lookup"><span data-stu-id="20708-882">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="20708-883">Lägg till parametrarna TerminateScheduledEvents och TerminateScheduledEventNotBeforeTimeoutInMinutes i New-AzVmssConfig och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="20708-883">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="20708-884">Lägg till egenskapen HyperVGeneration till avbildningsobjekt för virtuell dator</span><span class="sxs-lookup"><span data-stu-id="20708-884">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="20708-885">Lägg till funktioner för Host och HostGroup</span><span class="sxs-lookup"><span data-stu-id="20708-885">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="20708-886">Nya cmdletar:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="20708-886">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="20708-887">HostId-parametern läggs till i New-AzVMConfig och New-AzVM</span><span class="sxs-lookup"><span data-stu-id="20708-887">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="20708-888">Uppdatera exempel i "Invoke-AzVMRunCommand"-dokumentationen till att använda rätt parameternamn</span><span class="sxs-lookup"><span data-stu-id="20708-888">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="20708-889">Uppdatera "-VolumeType"-beskrivningen i referensdokumentationen för "set-AzVMDiskEncryptionExtension" och "set-AzVmssDiskEncryptionExtension"</span><span class="sxs-lookup"><span data-stu-id="20708-889">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="20708-890">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="20708-890">Az.DataFactory</span></span>
* <span data-ttu-id="20708-891">Åtgärda skrivfel till att använda versaler för "Windows" i "New-AzDataFactoryEncryptValue"-dokumentationen</span><span class="sxs-lookup"><span data-stu-id="20708-891">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="20708-892">Uppdaterade ADF .Net SDK-versionen till 4.1.2</span><span class="sxs-lookup"><span data-stu-id="20708-892">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="20708-893">Lägg till parametrarna "DataProxyIntegrationRuntimeName", "DataProxyStagingLinkedServiceName" och "DataProxyStagingPath" för "Set-AzureRmDataFactoryV2IntegrationRuntime"-cmd för att aktivera konfiguration av lokalt installerad integrationskörning som en proxy för SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="20708-893">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="20708-894">Uppdaterade PSTriggerRun till att visa utlöst pipeline, meddelande och egenskaper samt PSActivityRun till att visa aktivitetstypen</span><span class="sxs-lookup"><span data-stu-id="20708-894">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="20708-895">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="20708-895">Az.DataLakeStore</span></span>
* <span data-ttu-id="20708-896">Korrigering av frysning av Get-DataLakeStoreDeletedItem för fel eller fjärrundantag.</span><span class="sxs-lookup"><span data-stu-id="20708-896">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="20708-897">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="20708-897">Az.EventHub</span></span>
* <span data-ttu-id="20708-898">Korrigering av problem #9658 : Skrivfel i parametern VirtualNteworkRule i Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="20708-898">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="20708-899">Korrigering av problem #9558 : Set-AzEventHubNamespace använder PATCH i stället för PUT</span><span class="sxs-lookup"><span data-stu-id="20708-899">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="20708-900">lade till parametern EnableKafka i Set-AzEventHubNamespace-cmdleten</span><span class="sxs-lookup"><span data-stu-id="20708-900">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="20708-901">Korrigering av problem #9786 : kan inte skapa en regel med Endast lyssna-behörighet</span><span class="sxs-lookup"><span data-stu-id="20708-901">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="20708-902">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="20708-902">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="20708-903">Åtgärdade skrivfel i dokumentation där "Azure" skrevs helt med gemener</span><span class="sxs-lookup"><span data-stu-id="20708-903">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="20708-904">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="20708-904">Az.Monitor</span></span>
* <span data-ttu-id="20708-905">Åtgärdade felaktigt parameternamn i hjälpdokumentationen</span><span class="sxs-lookup"><span data-stu-id="20708-905">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="20708-906">Az.Network</span><span class="sxs-lookup"><span data-stu-id="20708-906">Az.Network</span></span>
* <span data-ttu-id="20708-907">Uppdaterade New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="20708-907">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="20708-908">Gjorde parametern "PublicIpAddress" inaktuell eftersom den aldrig används på serversidan.</span><span class="sxs-lookup"><span data-stu-id="20708-908">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="20708-909">Lade till den valfria parametern "Primary", som anger huruvida den aktuella IP-konfigurationen är den primära.</span><span class="sxs-lookup"><span data-stu-id="20708-909">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="20708-910">Förbättrade hanteringen av felundantag för begärande från SDK – åtgärdar problemet att tidigare SDK-undantag inte hanteras på rätt sätt, vilket leder till att viktig felinformation inte visas</span><span class="sxs-lookup"><span data-stu-id="20708-910">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="20708-911">Justerade valideringslogiken för IPv6-IP-prefix till att kontrollera korrekt IPv6-prefixlängd.</span><span class="sxs-lookup"><span data-stu-id="20708-911">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="20708-912">Uppdaterade Get-AzVirtualNetworkSubnetConfig: Lade till parameter som anges till get av undernätets resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="20708-912">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="20708-913">Uppdaterade beskrivningen av parametern Location för AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="20708-913">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="20708-914">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="20708-914">Az.OperationalInsights</span></span>
* <span data-ttu-id="20708-915">Uppdaterade dokumentation för "New-AzOperationalInsightsLinuxSyslogDataSource"</span><span class="sxs-lookup"><span data-stu-id="20708-915">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="20708-916">Lade till exempel</span><span class="sxs-lookup"><span data-stu-id="20708-916">Added example</span></span>
    - <span data-ttu-id="20708-917">Uppdaterade beskrivningen av parametern "-Name"</span><span class="sxs-lookup"><span data-stu-id="20708-917">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="20708-918">Lade till ett exempel för New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="20708-918">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="20708-919">Ändrade beskrivningen av parametern -Name för New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="20708-919">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="20708-920">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="20708-920">Az.RecoveryServices</span></span>
* <span data-ttu-id="20708-921">Uppdatera "Get-AzRecoveryServicesBackupJobDetail.md"</span><span class="sxs-lookup"><span data-stu-id="20708-921">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="20708-922">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="20708-922">Az.Resources</span></span>
* <span data-ttu-id="20708-923">Lägg till stöd för den nya API-versionen från 2019-05-10 för Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="20708-923">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="20708-924">Lägg till stöd för "copy.count = 0" för variabler, resurser och egenskaper</span><span class="sxs-lookup"><span data-stu-id="20708-924">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="20708-925">Resurser med "condition = false" eller "copy.count = 0" tas bort i complete-läget</span><span class="sxs-lookup"><span data-stu-id="20708-925">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="20708-926">Lägg till ett exempel på tilldelning av princip på prenumerationsnivå i hjälpdokumentationen</span><span class="sxs-lookup"><span data-stu-id="20708-926">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="20708-927">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="20708-927">Az.ServiceBus</span></span>
* <span data-ttu-id="20708-928">Korrigering av problem #9658 : Skrivfel i parametern VirtualNetworkRule i set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="20708-928">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="20708-929">Korrigering av problem #9786 : kan inte skapa en regel med Endast lyssna-behörighet</span><span class="sxs-lookup"><span data-stu-id="20708-929">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="20708-930">Lade till det nya kommandot "Test-AzServiceBusNameAvailability" för att kontrollera namntillgängligheten för kö och ämne</span><span class="sxs-lookup"><span data-stu-id="20708-930">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="20708-931">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="20708-931">Az.ServiceFabric</span></span>
* <span data-ttu-id="20708-932">Åtgärda buggar med tillägg av nodtyps-cmdlet:</span><span class="sxs-lookup"><span data-stu-id="20708-932">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="20708-933">NullReferenceException-bugg när resursgrupp hade annan vmss som inte är relaterad till Service Fabric-klustret.</span><span class="sxs-lookup"><span data-stu-id="20708-933">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="20708-934">Åtgärdar problemet: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="20708-934">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="20708-935">Åtgärda bugg där cmdleten misslyckades om virtualNetwork var i en annan resursgrupp än klustret.</span><span class="sxs-lookup"><span data-stu-id="20708-935">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="20708-936">Åtgärdar problemet: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="20708-936">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="20708-937">AzServiceFabricApplicationCertificate-cmdleten görs inaktuell</span><span class="sxs-lookup"><span data-stu-id="20708-937">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="20708-938">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="20708-938">Az.Sql</span></span>
* <span data-ttu-id="20708-939">Uppdatera dokumentation om gamla gransknings-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="20708-939">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="20708-940">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="20708-940">Az.Storage</span></span>
* <span data-ttu-id="20708-941">Uppdatera hjälpen för Get/Close-AzStorageFileHandle genom att lägga till fler scenarier i cmdlet-exempel och uppdatera parameterbeskrivningar</span><span class="sxs-lookup"><span data-stu-id="20708-941">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="20708-942">Stöd för StandardBlobTier i uppladdningsblob och kopieringsblob</span><span class="sxs-lookup"><span data-stu-id="20708-942">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="20708-943">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="20708-943">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="20708-944">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="20708-944">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="20708-945">Stöd för rehydratiseringsprioritet i kopieringsblob</span><span class="sxs-lookup"><span data-stu-id="20708-945">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="20708-946">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="20708-946">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="20708-947">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="20708-947">Az.Websites</span></span>
* <span data-ttu-id="20708-948">Lägg till klargöranden gällande parametern -AppSettings i Set-AzWebApp och Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="20708-948">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="20708-949">2.5.0 – July 2019</span><span class="sxs-lookup"><span data-stu-id="20708-949">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="20708-950">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="20708-950">Az.Accounts</span></span>
* <span data-ttu-id="20708-951">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="20708-951">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="20708-952">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="20708-952">Az.ApplicationInsights</span></span>
* <span data-ttu-id="20708-953">Korrigera skrivfel i exempel i dokumentationen för Remove-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="20708-953">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="20708-954">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="20708-954">Az.Automation</span></span>
* <span data-ttu-id="20708-955">Korrigera skrivfel i resurssträng</span><span class="sxs-lookup"><span data-stu-id="20708-955">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="20708-956">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="20708-956">Az.CognitiveServices</span></span>
* <span data-ttu-id="20708-957">Stöd för NetworkRuleSet har lagts till.</span><span class="sxs-lookup"><span data-stu-id="20708-957">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="20708-958">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="20708-958">Az.Compute</span></span>
* <span data-ttu-id="20708-959">Lägg till saknade egenskaper (ComputerName, OsName, OsVersion och HyperVGeneration) för visningsobjekt i den virtuella datorinstansen.</span><span class="sxs-lookup"><span data-stu-id="20708-959">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="20708-960">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="20708-960">Az.ContainerRegistry</span></span>
* <span data-ttu-id="20708-961">Åtgärda skrivfel i Remove-AzContainerRegistryReplication för parametern Replication</span><span class="sxs-lookup"><span data-stu-id="20708-961">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="20708-962">Mer information finns här: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="20708-962">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="20708-963">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="20708-963">Az.DataFactory</span></span>
* <span data-ttu-id="20708-964">ADF .Net SDK-versionen har uppdaterats till 4.1.0</span><span class="sxs-lookup"><span data-stu-id="20708-964">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="20708-965">Korrigera skrivfel i dokumentationen för Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="20708-965">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="20708-966">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="20708-966">Az.EventHub</span></span>
* <span data-ttu-id="20708-967">Ny cmmdlet har lagts till för att skapa SAS-token: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="20708-967">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="20708-968">verifierings- och felmeddelande har lagts till för authorizationrules-rättigheter om endast "hantera" har tilldelats</span><span class="sxs-lookup"><span data-stu-id="20708-968">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="20708-969">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="20708-969">Az.KeyVault</span></span>
* <span data-ttu-id="20708-970">Stöd har lagts till för att ange KeySize för certifikatprinciper</span><span class="sxs-lookup"><span data-stu-id="20708-970">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="20708-971">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="20708-971">Az.LogicApp</span></span>
* <span data-ttu-id="20708-972">Korrigering för Get-AzIntegrationAccountMap för att lista alla mappningstyper</span><span class="sxs-lookup"><span data-stu-id="20708-972">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="20708-973">Ny MapType-parameter har lagts till för filtrering</span><span class="sxs-lookup"><span data-stu-id="20708-973">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="20708-974">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="20708-974">Az.ManagedServices</span></span>
* <span data-ttu-id="20708-975">Stöd för API-versionen 2019-06-01 (GA) har lagts till</span><span class="sxs-lookup"><span data-stu-id="20708-975">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="20708-976">Az.Network</span><span class="sxs-lookup"><span data-stu-id="20708-976">Az.Network</span></span>
* <span data-ttu-id="20708-977">Lägg till stöd för privat slutpunkt och privat länktjänst</span><span class="sxs-lookup"><span data-stu-id="20708-977">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="20708-978">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="20708-978">New cmdlets</span></span>
        - <span data-ttu-id="20708-979">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="20708-979">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="20708-980">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="20708-980">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="20708-981">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="20708-981">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="20708-982">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="20708-982">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="20708-983">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="20708-983">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="20708-984">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="20708-984">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="20708-985">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="20708-985">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="20708-986">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="20708-986">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="20708-987">Nedanstående kommandon för funktionen har uppdaterats: Flaggan PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies på undernätet i VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="20708-987">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="20708-988">Uppdaterade New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="20708-988">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="20708-989">Valfri parameter har lagts till – PrivateEndpointNetworkPoliciesFlag som konfigurerar huruvida nätverksprinciper ska tillämpas på en privat slutpunkt i det här undernätet.</span><span class="sxs-lookup"><span data-stu-id="20708-989">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="20708-990">Valfri parameter har lagts till – PrivateLinkServiceNetworkPoliciesFlag som konfigurerar huruvida nätverksprinciper ska tillämpas på en privat länktjänst i det här undernätet.</span><span class="sxs-lookup"><span data-stu-id="20708-990">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="20708-991">AzPrivateLinkService för cmdlet-parametern ServiceName har bytt namn till Name med aliaset ServiceName för bakåtkompatibilitet</span><span class="sxs-lookup"><span data-stu-id="20708-991">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="20708-992">Aktivera ICMP-protokoll för konfiguration av nätverkssäkerhetsregler</span><span class="sxs-lookup"><span data-stu-id="20708-992">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="20708-993">Uppdaterade cmdletar</span><span class="sxs-lookup"><span data-stu-id="20708-993">Updated cmdlets</span></span>
        - <span data-ttu-id="20708-994">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="20708-994">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="20708-995">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="20708-995">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="20708-996">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="20708-996">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="20708-997">Lägg till ConnectionProtocolType (Ikev1/Ikev2) som en konfigurerbar parameter för New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="20708-997">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="20708-998">Lägg till PrivateIpAddressVersion i LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="20708-998">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="20708-999">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="20708-999">Updated cmdlet:</span></span>
        - <span data-ttu-id="20708-1000">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="20708-1000">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="20708-1001">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="20708-1001">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="20708-1002">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="20708-1002">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="20708-1003">Uppdatering av Application Gateway-kommandot New-AzApplicationGatewayProbeConfig för stöd av anpassad port i Probe</span><span class="sxs-lookup"><span data-stu-id="20708-1003">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="20708-1004">Uppdaterade New-AzApplicationGatewayProbeConfig: Den valfria parametern Port som används för avsökning i serverdelen har lagts till.</span><span class="sxs-lookup"><span data-stu-id="20708-1004">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="20708-1005">Denna parameter gäller för SKU:erna Standard_V2 och WAF_V2.</span><span class="sxs-lookup"><span data-stu-id="20708-1005">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="20708-1006">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="20708-1006">Az.OperationalInsights</span></span>
* <span data-ttu-id="20708-1007">Uppdaterade standardversionen för sparade sökningar till 1.</span><span class="sxs-lookup"><span data-stu-id="20708-1007">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="20708-1008">Åtgärdade hantering av anpassad log null regex</span><span class="sxs-lookup"><span data-stu-id="20708-1008">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="20708-1009">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="20708-1009">Az.RecoveryServices</span></span>
* <span data-ttu-id="20708-1010">Uppdatera Get-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="20708-1010">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="20708-1011">Uppdatera Get-AzRecoveryServicesBackupContainer.md</span><span class="sxs-lookup"><span data-stu-id="20708-1011">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="20708-1012">Uppdatera Get-AzRecoveryServicesVault.md</span><span class="sxs-lookup"><span data-stu-id="20708-1012">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="20708-1013">Uppdatera Wait-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="20708-1013">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="20708-1014">Uppdatera Set-AzRecoveryServicesVaultContext.md</span><span class="sxs-lookup"><span data-stu-id="20708-1014">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="20708-1015">Uppdatera Get-AzRecoveryServicesBackupItem.md</span><span class="sxs-lookup"><span data-stu-id="20708-1015">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="20708-1016">Uppdatera Get-AzRecoveryServicesBackupRecoveryPoint.md</span><span class="sxs-lookup"><span data-stu-id="20708-1016">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="20708-1017">Uppdatera Restore-AzRecoveryServicesBackupItem.md</span><span class="sxs-lookup"><span data-stu-id="20708-1017">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="20708-1018">Uppdaterat tjänstanrop för avregistrering av container för Azure-filresurs</span><span class="sxs-lookup"><span data-stu-id="20708-1018">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="20708-1019">Uppdatera Set-AzRecoveryServicesAsrAlertSetting.md</span><span class="sxs-lookup"><span data-stu-id="20708-1019">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="20708-1020">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="20708-1020">Az.Resources</span></span>
- <span data-ttu-id="20708-1021">Ta bort den cmdlet som saknas och som refereras i dokumentationen till New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="20708-1021">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="20708-1022">Princip-cmdletar har uppdaterats så att de använder den nya API-versionen 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="20708-1022">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="20708-1023">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="20708-1023">Az.ServiceBus</span></span>
* <span data-ttu-id="20708-1024">Ny cmmdlet har lagts till för att skapa SAS-token: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="20708-1024">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="20708-1025">verifierings- och felmeddelande har lagts till för authorizationrules-rättigheter om endast "hantera" har tilldelats</span><span class="sxs-lookup"><span data-stu-id="20708-1025">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="20708-1026">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="20708-1026">Az.Sql</span></span>
* <span data-ttu-id="20708-1027">Åtgärda saknade exempel för Set-AzSqlDatabaseSecondary cmdlet</span><span class="sxs-lookup"><span data-stu-id="20708-1027">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="20708-1028">Åtgärda angivna återkommande genomsökningar för bedömning av säkerhetsrisk utan angivna e-postadresser</span><span class="sxs-lookup"><span data-stu-id="20708-1028">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="20708-1029">Korrigera ett skrivfel i ett varningsmeddelande.</span><span class="sxs-lookup"><span data-stu-id="20708-1029">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="20708-1030">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="20708-1030">Az.Storage</span></span>
* <span data-ttu-id="20708-1031">Uppdatera exempel i referensdokumentationen för Get-AzStorageAccount så att rätt parameternamn används</span><span class="sxs-lookup"><span data-stu-id="20708-1031">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="20708-1032">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="20708-1032">Az.StorageSync</span></span>
* <span data-ttu-id="20708-1033">Lägger till cmdleten Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="20708-1033">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="20708-1034">Åtgärda problem 9551 så att TierFilesOlderThanDays föredras</span><span class="sxs-lookup"><span data-stu-id="20708-1034">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="20708-1035">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="20708-1035">Az.Websites</span></span>
* <span data-ttu-id="20708-1036">Åtgärdar ett fel där vissa SiteConfig-egenskaper inte returnerades av Get-AzWebApp och Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="20708-1036">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="20708-1037">Lägger till en ny platsparameter för Get-AzDeletedWebApp och Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="20708-1037">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="20708-1038">Åtgärdar ett fel i kloning av webbapp-platser som använder New-AzWebApp-IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="20708-1038">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="20708-1039">2.4.0 – juli 2019</span><span class="sxs-lookup"><span data-stu-id="20708-1039">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="20708-1040">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="20708-1040">Az.Accounts</span></span>
* <span data-ttu-id="20708-1041">Lägg till stöd för profil-cmdletar</span><span class="sxs-lookup"><span data-stu-id="20708-1041">Add support for profile cmdlets</span></span>
* <span data-ttu-id="20708-1042">Lägg till stöd för miljöer och dataplaner i genererade cmdletar</span><span class="sxs-lookup"><span data-stu-id="20708-1042">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="20708-1043">Åtgärda bugg där fel slutpunkt i vissa fall användes för cmdletar för dataplaner i Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="20708-1043">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="20708-1044">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="20708-1044">Az.Advisor</span></span>
* <span data-ttu-id="20708-1045">GA-version av Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="20708-1045">GA release of Az.Advisor</span></span>
* <span data-ttu-id="20708-1046">Den här modulen ingår nu som en del av `Az`-sammanslagningsmodulen</span><span class="sxs-lookup"><span data-stu-id="20708-1046">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="20708-1047">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="20708-1047">Az.ApiManagement</span></span>
* <span data-ttu-id="20708-1048">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="20708-1048">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="20708-1049">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="20708-1049">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="20708-1050">Stöd för att fråga prenumerationer efter användare och produkt har lagts till</span><span class="sxs-lookup"><span data-stu-id="20708-1050">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="20708-1051">Stöd för att fråga med hjälp av omfång ”/”, ”/apis”, ”/apis/echo-api” har lagts till</span><span class="sxs-lookup"><span data-stu-id="20708-1051">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="20708-1052">Korrigering av problem https://github.com/Azure/azure-powershell/issues/9307 och https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="20708-1052">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="20708-1053">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="20708-1053">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="20708-1054">Stöd för att ange ”ApiVersion” och ”ApiVersionSetId” när API:er importeras har lagts till</span><span class="sxs-lookup"><span data-stu-id="20708-1054">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="20708-1055">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="20708-1055">Az.Automation</span></span>
* <span data-ttu-id="20708-1056">Bugg med cmdleten Set-AzAutomationConnectionFieldValue för att hantera strängvärde har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="20708-1056">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="20708-1057">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="20708-1057">Az.Compute</span></span>
* <span data-ttu-id="20708-1058">Lägg till parametern HyperVGeneration i New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="20708-1058">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="20708-1059">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="20708-1059">Az.DataFactory</span></span>
* <span data-ttu-id="20708-1060">Uppdaterar utdata från ADF-cmdletar som hämtar aktivitetskörningar, hämtar pipelinekörningar och hämtar utlösarkörningar för stöd för Select-Object-pipe.</span><span class="sxs-lookup"><span data-stu-id="20708-1060">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="20708-1061">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="20708-1061">Az.EventGrid</span></span>
* <span data-ttu-id="20708-1062">Korrigera stavfel i dokumentation om ”New-AzEventGridSubscription”</span><span class="sxs-lookup"><span data-stu-id="20708-1062">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="20708-1063">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="20708-1063">Az.IotHub</span></span>
* <span data-ttu-id="20708-1064">Lägg till stöd för att återskapa principnycklar för auktorisering.</span><span class="sxs-lookup"><span data-stu-id="20708-1064">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="20708-1065">Az.Network</span><span class="sxs-lookup"><span data-stu-id="20708-1065">Az.Network</span></span>
* <span data-ttu-id="20708-1066">”RoutingPreference” har lagts till i offentliga IP-taggar</span><span class="sxs-lookup"><span data-stu-id="20708-1066">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="20708-1067">Förbättra exempel för referensdokumentation om ”Get-AzNetworkServiceTag”</span><span class="sxs-lookup"><span data-stu-id="20708-1067">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="20708-1068">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="20708-1068">Az.PolicyInsights</span></span>
* <span data-ttu-id="20708-1069">Åtgärda problem med null-referens i Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="20708-1069">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="20708-1070">Mer information här: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="20708-1070">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="20708-1071">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="20708-1071">Az.OperationalInsights</span></span>
* <span data-ttu-id="20708-1072">Modellen för CustomLog-datakälla som returneras i Get-AzOperationalInsightsDataSource har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="20708-1072">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="20708-1073">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="20708-1073">Az.RecoveryServices</span></span>
* <span data-ttu-id="20708-1074">Kommandot get-policy för IaaSVM:er har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="20708-1074">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="20708-1075">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="20708-1075">Az.Resources</span></span>
    - <span data-ttu-id="20708-1076">Korrigera hjälptext för den översta parametern i Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="20708-1076">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="20708-1077">Lägg till växlingsstöd på klientsidan för Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="20708-1077">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="20708-1078">Lägg till nya parametrar för Set-AzPolicyAssignment, -PolicyParameters och -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="20708-1078">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="20708-1079">En mängd dokument- och exempeluppdateringar för Policy-cmdletar</span><span class="sxs-lookup"><span data-stu-id="20708-1079">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="20708-1080">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="20708-1080">Az.ServiceBus</span></span>
* <span data-ttu-id="20708-1081">Korrigering av problem #4938 – New-AzureRmServiceBusQueue returnerar BadRequest vid konfiguration av MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="20708-1081">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="20708-1082">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="20708-1082">Az.Sql</span></span>
* <span data-ttu-id="20708-1083">Lägg till cmdletar för instansredundansgrupper från förhandsversion till offentlig version</span><span class="sxs-lookup"><span data-stu-id="20708-1083">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="20708-1084">Stöd för granskning för Azure SQL Server\Database med nya cmdletar.</span><span class="sxs-lookup"><span data-stu-id="20708-1084">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="20708-1085">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="20708-1085">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="20708-1086">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="20708-1086">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="20708-1087">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="20708-1087">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="20708-1088">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="20708-1088">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="20708-1089">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="20708-1089">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="20708-1090">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="20708-1090">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="20708-1091">Ta bort begränsningar för e-post från inställningarna för sårbarhetsbedömning</span><span class="sxs-lookup"><span data-stu-id="20708-1091">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="20708-1092">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="20708-1092">Az.Storage</span></span>
* <span data-ttu-id="20708-1093">Ändra två parametrar ”-IndexDocument” och ”-ErrorDocument404Path” från ”krävs” till ”valfri” i cmdlet:</span><span class="sxs-lookup"><span data-stu-id="20708-1093">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="20708-1094">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="20708-1094">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="20708-1095">Uppdatera hjälpen för Get-AzStorageBlobContent genom att lägga till ett exempel</span><span class="sxs-lookup"><span data-stu-id="20708-1095">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="20708-1096">Visa mer felinformation när cmdleten misslyckas med StorageException</span><span class="sxs-lookup"><span data-stu-id="20708-1096">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="20708-1097">Stöd för att skapa eller uppdatera lagringskonto med Azure Files AAD DS-autentisering</span><span class="sxs-lookup"><span data-stu-id="20708-1097">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="20708-1098">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="20708-1098">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="20708-1099">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="20708-1099">Set-AzStorageAccount</span></span>
* <span data-ttu-id="20708-1100">Stöd för att lista eller stänga filreferenser för en filresurs, filkatalog eller en fil</span><span class="sxs-lookup"><span data-stu-id="20708-1100">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="20708-1101">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="20708-1101">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="20708-1102">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="20708-1102">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="20708-1103">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="20708-1103">Az.StorageSync</span></span>
* <span data-ttu-id="20708-1104">Den här modulen ingår nu som en del av `Az`-sammanslagningsmodulen</span><span class="sxs-lookup"><span data-stu-id="20708-1104">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="20708-1105">2.3.2 – juni 2019</span><span class="sxs-lookup"><span data-stu-id="20708-1105">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="20708-1106">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="20708-1106">Az.Accounts</span></span>
* <span data-ttu-id="20708-1107">Åtgärda bugg med felaktiga webbadresser som i vissa fall användes för Functions-anrop</span><span class="sxs-lookup"><span data-stu-id="20708-1107">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="20708-1108">Mer information här: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="20708-1108">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="20708-1109">Åtgärda problem med alias från AzureRM i Az-cmdletar</span><span class="sxs-lookup"><span data-stu-id="20708-1109">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="20708-1110">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="20708-1110">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="20708-1111">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="20708-1111">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="20708-1112">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="20708-1112">Az.Compute</span></span>
* <span data-ttu-id="20708-1113">Parameteruppsättningarna New-AzVm och New-AzVmss accepterar nu parametern ”ProximityPlacementGroup”.</span><span class="sxs-lookup"><span data-stu-id="20708-1113">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="20708-1114">Stavfel i referensdokumentationen för ”New-AzVM” har korrigerats</span><span class="sxs-lookup"><span data-stu-id="20708-1114">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="20708-1115">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="20708-1115">Az.Dns</span></span>
* <span data-ttu-id="20708-1116">Stavfel i hjälpexempel för ”Set-AzDnsZone” har korrigerats.</span><span class="sxs-lookup"><span data-stu-id="20708-1116">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="20708-1117">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="20708-1117">Az.EventGrid</span></span>
* <span data-ttu-id="20708-1118">Har uppdaterats för att använda API-versionen 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="20708-1118">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="20708-1119">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="20708-1119">New cmdlets:</span></span>
    - <span data-ttu-id="20708-1120">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="20708-1120">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="20708-1121">Skapar en ny Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="20708-1121">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="20708-1122">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="20708-1122">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="20708-1123">Hämtar information om en Event Grid-domän eller hämtar en lista med alla Event Grid-domäner i den aktuella Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="20708-1123">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="20708-1124">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="20708-1124">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="20708-1125">Tar bort en Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="20708-1125">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="20708-1126">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="20708-1126">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="20708-1127">Återskapar nyckeln för delad åtkomst för en Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="20708-1127">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="20708-1128">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="20708-1128">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="20708-1129">Hämtar de nycklar för delad åtkomst som används för att publicera händelser till en Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="20708-1129">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="20708-1130">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="20708-1130">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="20708-1131">Skapar ett nytt Azure Event Grid-domänämne.</span><span class="sxs-lookup"><span data-stu-id="20708-1131">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="20708-1132">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="20708-1132">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="20708-1133">Hämtar information om ett Event Grid-domänämne eller hämtar en lista med alla Event Grid-domänämnen under en specifik Event Grid-domän i nuvarande Azure</span><span class="sxs-lookup"><span data-stu-id="20708-1133">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="20708-1134">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="20708-1134">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="20708-1135">Tar bort ett befintligt Azure Event Grid-domänämne.</span><span class="sxs-lookup"><span data-stu-id="20708-1135">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="20708-1136">Uppdaterade cmdletar:</span><span class="sxs-lookup"><span data-stu-id="20708-1136">Updated cmdlets:</span></span>
    - <span data-ttu-id="20708-1137">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="20708-1137">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="20708-1138">Lägg till nya obligatoriska parametrar för att stödja piping för den nya Event Grid-domänen och Event Grid-domänämnet för att göra det möjligt att skapa nya händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="20708-1138">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="20708-1139">Lägg till nya obligatoriska parametrar för att ange det nya Event Grid-domännamnet och/eller namnet på Event Grid-domänämnet för att göra det möjligt att skapa nya händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="20708-1139">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="20708-1140">Lägg till ny parameteruppsättningar för domäner och domänämnen för att göra det möjligt att återanvända befintliga parametrar (t.ex. EndPointType, SubjectBeginsWith osv).</span><span class="sxs-lookup"><span data-stu-id="20708-1140">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="20708-1141">Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="20708-1141">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="20708-1142">Förfallodatum för händelseprenumeration</span><span class="sxs-lookup"><span data-stu-id="20708-1142">Event subscription expiration date,</span></span>
            - <span data-ttu-id="20708-1143">Avancerade filterparametrar.</span><span class="sxs-lookup"><span data-stu-id="20708-1143">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="20708-1144">Lägg till ny uppräkning för servicebusqueue som mål.</span><span class="sxs-lookup"><span data-stu-id="20708-1144">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="20708-1145">Tillåt inte användning av ”Alla” i alternativet -IncludedEventType och ersätt det med</span><span class="sxs-lookup"><span data-stu-id="20708-1145">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="20708-1146">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="20708-1146">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="20708-1147">Lägg till ny valfria parametrar (Top, ODataQuery och NextLink) för att stödja sidnumrering och filtrering av resultat.</span><span class="sxs-lookup"><span data-stu-id="20708-1147">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="20708-1148">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="20708-1148">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="20708-1149">Lägg till nya obligatoriska parametrar för att stödja piping för en Event Grid-domän och Event Grid-domänämnen för att göra det möjligt att ta bort befintliga händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="20708-1149">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="20708-1150">Lägg till nya obligatoriska parametrar för att ange Event Grid-domännamnet och/eller namnet på Event Grid-domänämnet för att göra det möjligt att ta bort befintliga händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="20708-1150">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="20708-1151">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="20708-1151">Az.FrontDoor</span></span>
* <span data-ttu-id="20708-1152">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="20708-1152">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="20708-1153">Lägg till stöd för transformeringar och nytt värde för automatisk komplettering för operatorer (RegEx)</span><span class="sxs-lookup"><span data-stu-id="20708-1153">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="20708-1154">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="20708-1154">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="20708-1155">Lägg till nya värden för automatisk komplettering</span><span class="sxs-lookup"><span data-stu-id="20708-1155">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="20708-1156">Az.Network</span><span class="sxs-lookup"><span data-stu-id="20708-1156">Az.Network</span></span>
* <span data-ttu-id="20708-1157">Lägg till stöd för resurs för virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="20708-1157">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="20708-1158">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="20708-1158">New cmdlets</span></span>
        - <span data-ttu-id="20708-1159">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="20708-1159">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="20708-1160">Lägg till AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="20708-1160">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="20708-1161">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="20708-1161">New cmdlets</span></span> 
        - <span data-ttu-id="20708-1162">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="20708-1162">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="20708-1163">Lägg till PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="20708-1163">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="20708-1164">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="20708-1164">New cmdlets</span></span> 
        - <span data-ttu-id="20708-1165">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="20708-1165">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="20708-1166">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="20708-1166">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="20708-1167">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="20708-1167">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="20708-1168">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="20708-1168">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="20708-1169">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="20708-1169">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="20708-1170">Lägg till PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="20708-1170">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="20708-1171">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="20708-1171">New cmdlets</span></span>
        - <span data-ttu-id="20708-1172">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="20708-1172">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="20708-1173">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="20708-1173">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="20708-1174">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="20708-1174">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="20708-1175">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="20708-1175">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="20708-1176">Nedanstående kommandon för funktionen har uppdaterats: Flaggan UseLocalAzureIpAddress på VpnConnection</span><span class="sxs-lookup"><span data-stu-id="20708-1176">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="20708-1177">New-AzVpnConnection har uppdaterats: Den valfria parametern -UseLocalAzureIpAddress har lagts till för att visa att en lokal IP-adress i Azure ska användas som källadress när anslutningen initieras.</span><span class="sxs-lookup"><span data-stu-id="20708-1177">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="20708-1178">Set-AzVpnConnection har uppdaterats: Den valfria parametern -UseLocalAzureIpAddress har lagts till för att visa att en lokal IP-adress i Azure ska användas som källadress när anslutningen initieras.</span><span class="sxs-lookup"><span data-stu-id="20708-1178">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="20708-1179">Det skrivskyddade fältet PeeredConnections har lagts till i ExpressRoute-peering.</span><span class="sxs-lookup"><span data-stu-id="20708-1179">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="20708-1180">Det skrivskyddade fältet GlobalReachEnabled har lagts till i ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="20708-1180">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="20708-1181">Ett attribut för icke-bakåtkompatibla ändringar har lagts till för att lyfta fram utfasning av fältet AllowGlobalReach i modellen ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="20708-1181">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="20708-1182">Problem 8756 har åtgärdats: Fel vid användning av TargetListenerID med AzApplicationGatewayRedirectConfiguration-cmdletar</span><span class="sxs-lookup"><span data-stu-id="20708-1182">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="20708-1183">En bugg i New-AzApplicationGatewayPathRuleConfig som gjorde att regeluppsättningen för att återskapa inte kunde anges har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="20708-1183">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="20708-1184">Visningen av VirtualNetworkTaps i NetworkInterfaceIpConfiguration har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="20708-1184">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="20708-1185">Cortex Get-cmdletar för att visa en lista med alla delar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="20708-1185">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="20708-1186">Funktionen för att skapa VirtualHub-referenser för ExpressRouteGateways och VpnGateway har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="20708-1186">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="20708-1187">Stöd för tillgänglighetszoner i AzureFirewall och NatGateway har lagts till</span><span class="sxs-lookup"><span data-stu-id="20708-1187">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="20708-1188">Cmdleten Get-AzNetworkServiceTag har lagts till</span><span class="sxs-lookup"><span data-stu-id="20708-1188">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="20708-1189">Lägg till stöd för flera offentliga IP-adresser för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="20708-1189">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="20708-1190">Cmdleten New-AzFirewall har uppdaterats:</span><span class="sxs-lookup"><span data-stu-id="20708-1190">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="20708-1191">Parametern -PublicIpAddress som accepterar ett eller flera offentliga IP-adressobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="20708-1191">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="20708-1192">Parametern -VirtualNetwork som accepterar ett virtuellt nätverksobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="20708-1192">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="20708-1193">Metoderna AddPublicIpAddress och RemovePublicIpAddress har lagts till på brandväggsobjekt – dessa accepterar ett offentligt IP-adressobjekt som indata</span><span class="sxs-lookup"><span data-stu-id="20708-1193">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="20708-1194">Inaktuella parametrar -PublicIpName och -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="20708-1194">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="20708-1195">Nedanstående kommandon för funktionen har uppdaterats: Ange autentiseringsalternativ för VpnClient AAD till resurser för virtuella nätverksgatewayer.</span><span class="sxs-lookup"><span data-stu-id="20708-1195">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="20708-1196">New-AzVirtualNetworkGateway har uppdaterats: De valfria parametrarna AadTenantUri, AadAudienceId och AadIssuerUri för att ange VpnClient AAD-autentiseringsalternativ på en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="20708-1196">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="20708-1197">Set-AzVirtualNetworkGateway har uppdaterats: De valfria parametrarna AadTenantUri, AadAudienceId och AadIssuerUri för att ange VpnClient AAD-autentiseringsalternativ på en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="20708-1197">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="20708-1198">Set-AzVirtualNetworkGateway har uppdaterats: Den valfria växelparametern RemoveAadAuthentication som tar bort VpnClient AAD-autentiseringsalternativ från en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="20708-1198">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="20708-1199">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="20708-1199">Az.OperationalInsights</span></span>
* <span data-ttu-id="20708-1200">Aktivera prisnivån **pergb2018** i kommandot ”New-AzureRmOperationalInsightsWorkspace”</span><span class="sxs-lookup"><span data-stu-id="20708-1200">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="20708-1201">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="20708-1201">Az.Resources</span></span>
* <span data-ttu-id="20708-1202">Stöd för ytterligare alternativ för att exportera en mall</span><span class="sxs-lookup"><span data-stu-id="20708-1202">Support for additional Template Export options</span></span>
    - <span data-ttu-id="20708-1203">Lägg till parametern ”-SkipResourceNameParameterization” till Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="20708-1203">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="20708-1204">Lägg till parametern ”-SkipAllParameterization” till Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="20708-1204">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="20708-1205">Lägg till parametern ”-Resource” till Export-AzResourceGroup för exporterad resursfiltrering</span><span class="sxs-lookup"><span data-stu-id="20708-1205">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="20708-1206">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="20708-1206">Az.ServiceFabric</span></span>
* <span data-ttu-id="20708-1207">Åtgärda att fel tumavtryck används vid tilläggning av certifikat i ByExistingKeyVault i vissa fall</span><span class="sxs-lookup"><span data-stu-id="20708-1207">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="20708-1208">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="20708-1208">Az.Sql</span></span>
* <span data-ttu-id="20708-1209">Åtgärda suffix för lagringsslutpunkt i Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="20708-1209">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="20708-1210">Åtgärda att aktivering av Advanced Data Security åsidosätter Advanced Threat Protection-princip</span><span class="sxs-lookup"><span data-stu-id="20708-1210">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="20708-1211">Nya cmdletar för Management.Sql som gör att kunderna kan lägga till nycklar för transparent datakryptering (TDE) och ange TDE-skydd för hanterade instanser</span><span class="sxs-lookup"><span data-stu-id="20708-1211">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="20708-1212">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="20708-1212">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="20708-1213">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="20708-1213">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="20708-1214">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="20708-1214">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="20708-1215">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="20708-1215">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="20708-1216">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="20708-1216">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="20708-1217">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="20708-1217">Az.Storage</span></span>
* <span data-ttu-id="20708-1218">Stöd för typerna FileStorage och SkuName Premium_ZRS när lagringskonton skapas</span><span class="sxs-lookup"><span data-stu-id="20708-1218">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="20708-1219">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="20708-1219">New-AzStorageAccount</span></span>
* <span data-ttu-id="20708-1220">Beskrivningen av cmdleten för bloboföränderlighet har förtydligats</span><span class="sxs-lookup"><span data-stu-id="20708-1220">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="20708-1221">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="20708-1221">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="20708-1222">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="20708-1222">Az.Websites</span></span>
* <span data-ttu-id="20708-1223">Optimerar Get-AzWebAppCertificate för att filtrera efter resursgrupp på servern i stället för klienten</span><span class="sxs-lookup"><span data-stu-id="20708-1223">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="20708-1224">Lägger till växlingsparametern -UseDisasterRecovery till Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="20708-1224">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="20708-1225">2.2.0 – juni 2019</span><span class="sxs-lookup"><span data-stu-id="20708-1225">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="20708-1226">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="20708-1226">Az.Cdn</span></span>
* <span data-ttu-id="20708-1227">Uppdaterade cmdletar för att ge stöd för rulesEngine-funktion baserat på API-version 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="20708-1227">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="20708-1228">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="20708-1228">Az.Compute</span></span>
* <span data-ttu-id="20708-1229">Lade till parameter `NoWait` som startar åtgärden och returnerar omedelbart, innan åtgärden har slutförts.</span><span class="sxs-lookup"><span data-stu-id="20708-1229">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="20708-1230">Uppdaterade cmdletar:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="20708-1230">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="20708-1231">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="20708-1231">Az.EventHub</span></span>
* <span data-ttu-id="20708-1232">Korrigering för #9231 – Get-AzEventHubNamespace returnerar inga taggar</span><span class="sxs-lookup"><span data-stu-id="20708-1232">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="20708-1233">Korrigering för #9230 – Get-AzEventHubNamespace returnerar ResourceGroup istället för ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20708-1233">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="20708-1234">Az.Network</span><span class="sxs-lookup"><span data-stu-id="20708-1234">Az.Network</span></span>
* <span data-ttu-id="20708-1235">Uppdatera ResourceId och InputObject för NAT-gateway</span><span class="sxs-lookup"><span data-stu-id="20708-1235">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="20708-1236">Lägg till alias för ResourceId och InputObject</span><span class="sxs-lookup"><span data-stu-id="20708-1236">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="20708-1237">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="20708-1237">Az.PolicyInsights</span></span>
* <span data-ttu-id="20708-1238">Åtgärda Null-referensproblem i Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="20708-1238">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="20708-1239">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="20708-1239">Az.RecoveryServices</span></span>
* <span data-ttu-id="20708-1240">Minsta kvarhållning för IaaSVM-policy i dagar ändrat till 7 från 1</span><span class="sxs-lookup"><span data-stu-id="20708-1240">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="20708-1241">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="20708-1241">Az.ServiceBus</span></span>
* <span data-ttu-id="20708-1242">Korrigering för ärende #9182 – Get-AzServiceBusNamespace returnerar ResourceGroup istället för ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20708-1242">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="20708-1243">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="20708-1243">Az.ServiceFabric</span></span>
* <span data-ttu-id="20708-1244">Åtgärda stavfel i felmeddelandet för Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="20708-1244">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="20708-1245">Åtgärda saknat tecken i Service Fabric-kommandorader</span><span class="sxs-lookup"><span data-stu-id="20708-1245">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="20708-1246">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="20708-1246">Az.Sql</span></span>
* <span data-ttu-id="20708-1247">Lägg till parametern DnsZonePartner för New-AzureSqlInstance-cmdlet för att ge stöd för AutoDr för hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="20708-1247">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="20708-1248">Avvecklar cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="20708-1248">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="20708-1249">Döp om cmdletar för hotidentifiering till Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="20708-1249">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="20708-1250">Parametrarna New-AzSqlInstance -StorageSizeInGB och -LicenseType är nu valfria.</span><span class="sxs-lookup"><span data-stu-id="20708-1250">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="20708-1251">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="20708-1251">Az.Websites</span></span>
* <span data-ttu-id="20708-1252">åtgärdar problemet där användningen av Set-AzWebApp och Set-AzWebAppSlot med -WebApp-egenskap tog bort taggarna</span><span class="sxs-lookup"><span data-stu-id="20708-1252">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="20708-1253">2.1.0 – maj 2019</span><span class="sxs-lookup"><span data-stu-id="20708-1253">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="20708-1254">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="20708-1254">Az.ApiManagement</span></span>
* <span data-ttu-id="20708-1255">Skapade nya cmdletar för att hantera diagnostik för global- och API-omfång</span><span class="sxs-lookup"><span data-stu-id="20708-1255">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="20708-1256">**Get-AzApiManagementDiagnostic** – Skaffa diagnostik konfigurerad för global- eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="20708-1256">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="20708-1257">**New-AzApiManagementDiagnostic** – Skapa ny diagnostik för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="20708-1257">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="20708-1258">**New-AzApiManagementHttpMessageDiagnostic** – Skapa diagnostikinställning om vilka rubriker som ska loggas och storleken på brödtextbyte</span><span class="sxs-lookup"><span data-stu-id="20708-1258">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="20708-1259">**New-AzApiManagementPipelineDiagnosticSetting** – Skapa diagnostikinställningar för inkommande/utgående HTTP-meddelanden till gatewayen.</span><span class="sxs-lookup"><span data-stu-id="20708-1259">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="20708-1260">**New-AzApiManagementSamplingSetting** – Skapa samplinginställningar för begäranden/svar för en diagnostik</span><span class="sxs-lookup"><span data-stu-id="20708-1260">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="20708-1261">**Remove-AzApiManagementDiagnostic** – Ta bort en diagnostikenhet för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="20708-1261">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="20708-1262">**Set-AzApiManagementDiagnostic** – Uppdatera en diagnostikenhet för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="20708-1262">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="20708-1263">Skapade nya cmdletar för hantering av cacheminne i ApiManagement-tjänsten</span><span class="sxs-lookup"><span data-stu-id="20708-1263">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="20708-1264">**Get-AzApiManagementCache** – Hämta information om cacheminnet som anges av identifierare eller alla cacheminnen</span><span class="sxs-lookup"><span data-stu-id="20708-1264">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="20708-1265">**New-AzApiManagementCache** – Skapa ett nytt default-cacheminne eller cacheminne i en viss Azure-region</span><span class="sxs-lookup"><span data-stu-id="20708-1265">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="20708-1266">**Remove-AzApiManagementCache** – Ta bort ett cacheminne</span><span class="sxs-lookup"><span data-stu-id="20708-1266">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="20708-1267">**Remove-AzApiManagementCache** – Ta bort ett cacheminne</span><span class="sxs-lookup"><span data-stu-id="20708-1267">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="20708-1268">Skapade nya cmdletar för hantering av API-schema</span><span class="sxs-lookup"><span data-stu-id="20708-1268">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="20708-1269">**New-AzApiManagementSchema** – Skapa ett nytt schema för ett API</span><span class="sxs-lookup"><span data-stu-id="20708-1269">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="20708-1270">**Get-AzApiManagementSchema** – Hämta de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="20708-1270">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="20708-1271">**Remove-AzApiManagementSchema** – Ta bort de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="20708-1271">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="20708-1272">**Set-AzApiManagementSchema** – Uppdatera de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="20708-1272">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="20708-1273">Skapa ny cmdlet för att generera en användartoken.</span><span class="sxs-lookup"><span data-stu-id="20708-1273">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="20708-1274">**New-AzApiManagementUserToken** – Skapa en ny användartoken som enligt standardinställning är giltig i 8 timmar. Token för GIT-användaren kan skapas med den här cmdleten./</span><span class="sxs-lookup"><span data-stu-id="20708-1274">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="20708-1275">Skapade en ny cmdlet för att hämta nätverksstatus</span><span class="sxs-lookup"><span data-stu-id="20708-1275">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="20708-1276">**Get-AzApiManagementNetworkStatus** – Hämta nätverksstatusanslutningen för resurserna som API Management-tjänsten är beroende av.</span><span class="sxs-lookup"><span data-stu-id="20708-1276">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="20708-1277">Det här är användbart när du distribuerar ApiManagement-tjänsten i ett virtuellt nätverk och validerar om något beroende är brutet.</span><span class="sxs-lookup"><span data-stu-id="20708-1277">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="20708-1278">Uppdaterade cmdlet **New-AzApiManagement** för att hantera ApiManagement-tjänsten</span><span class="sxs-lookup"><span data-stu-id="20708-1278">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="20708-1279">Lade till stöd för den nya SKU:n Consumption</span><span class="sxs-lookup"><span data-stu-id="20708-1279">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="20708-1280">Aktiverade stöd för att slå på flaggan EnableClientCertificate för SKU:n Consumption</span><span class="sxs-lookup"><span data-stu-id="20708-1280">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="20708-1281">Den nya cmdleten **New-AzApiManagementSslSetting** gör det möjligt att ställa in TLS/SSL-inställningen på ”Backend” och ”Frontend” (serverdel och klientdel).</span><span class="sxs-lookup"><span data-stu-id="20708-1281">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="20708-1282">Det här kan också användas till att konfigurera chiffer som 3DES och ServerProtocols som Http2 för Frontend för en ApiManagement-tjänst.</span><span class="sxs-lookup"><span data-stu-id="20708-1282">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="20708-1283">Stöd har lagts till för att konfigurera värdnamnet DeveloperPortal på ApiManagement-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="20708-1283">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="20708-1284">Uppdaterade cmdletar **Get-AzApiManagementSsoToken** för att ta PsApiManagement-objekt som indata</span><span class="sxs-lookup"><span data-stu-id="20708-1284">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="20708-1285">Uppdaterad cmdleten för att visa infogade felmeddelanden</span><span class="sxs-lookup"><span data-stu-id="20708-1285">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="20708-1286">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Felkod: Felmeddelande av typen ValidationError: Ett eller flera fält innehåller felaktiga värden: Felinformation:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="20708-1286">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="20708-1287">Uppdaterade cmdlet **Export-AzApiManagementApi** för att exportera API:er i OpenApi 3.0-format</span><span class="sxs-lookup"><span data-stu-id="20708-1287">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="20708-1288">Uppdaterade cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="20708-1288">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="20708-1289">Importera API från dokumentspecifikationen OpenApi 3.0</span><span class="sxs-lookup"><span data-stu-id="20708-1289">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="20708-1290">Om du vill åsidosätta egenskapen PsApiManagementSchema specificerad i ett dokument (Swagger, Wadl, Wsdl, OpenApi).</span><span class="sxs-lookup"><span data-stu-id="20708-1290">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="20708-1291">Åsidosätta egenskapen ServiceUrl som specificeras i ett dokument.</span><span class="sxs-lookup"><span data-stu-id="20708-1291">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="20708-1292">Uppdaterade cmdlet **Get-AzApiManagementPolicy** för att returnera policy i undantaget format av typen icke-XML med rawxml</span><span class="sxs-lookup"><span data-stu-id="20708-1292">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="20708-1293">Uppdaterade cmdlet **Set-AzApiManagementPolicy** för att godkänna policy i undantaget format av typen icke-XML med rawxml och XML undantaget med xml</span><span class="sxs-lookup"><span data-stu-id="20708-1293">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="20708-1294">Uppdaterad cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="20708-1294">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="20708-1295">Konfigurera API med OpenId auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="20708-1295">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="20708-1296">Skapa ett API i ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="20708-1296">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="20708-1297">Klona ett API med SourceApiId och SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="20708-1297">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="20708-1298">Möjlighet att konfigurera SubscriptionRequired i API-omfattningen.</span><span class="sxs-lookup"><span data-stu-id="20708-1298">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="20708-1299">Uppdaterad cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="20708-1299">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="20708-1300">Konfigurera API med OpenId auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="20708-1300">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="20708-1301">Uppdatera ett API till ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="20708-1301">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="20708-1302">Möjlighet att konfigurera SubscriptionRequired i API-omfattningen.</span><span class="sxs-lookup"><span data-stu-id="20708-1302">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="20708-1303">Uppdaterad cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="20708-1303">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="20708-1304">Klona en befintlig version med hjälp av SourceApiRevision (kopiera taggar, produkter, åtgärder och principer).</span><span class="sxs-lookup"><span data-stu-id="20708-1304">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="20708-1305">Den nya revisionen antar ApiId från den överordnade instansen.</span><span class="sxs-lookup"><span data-stu-id="20708-1305">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="20708-1306">Tillhandahålla ApiRevisionDescription</span><span class="sxs-lookup"><span data-stu-id="20708-1306">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="20708-1307">Åsidosätta ServiceUrl vid kloning av ett API.</span><span class="sxs-lookup"><span data-stu-id="20708-1307">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="20708-1308">Uppdaterad cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="20708-1308">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="20708-1309">Konfigurera AAD eller AADB2C med en Authority</span><span class="sxs-lookup"><span data-stu-id="20708-1309">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="20708-1310">Konfigurera SignupPolicy, SigninPolicy, ProfileEditingPolicy och PasswordResetPolicy</span><span class="sxs-lookup"><span data-stu-id="20708-1310">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="20708-1311">Uppdaterad cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="20708-1311">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="20708-1312">Kompensera för ny SubscriptonModel med Scope och UserId</span><span class="sxs-lookup"><span data-stu-id="20708-1312">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="20708-1313">Kompensera för gammal prenumerationsmodell med ProductId och UserId</span><span class="sxs-lookup"><span data-stu-id="20708-1313">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="20708-1314">Lägg till funktion för att aktivera AllowTracing på prenumerationsnivå.</span><span class="sxs-lookup"><span data-stu-id="20708-1314">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="20708-1315">Uppdaterad cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="20708-1315">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="20708-1316">Kompensera för ny SubscriptonModel med Scope och UserId</span><span class="sxs-lookup"><span data-stu-id="20708-1316">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="20708-1317">Kompensera för gammal prenumerationsmodell med ProductId och UserId</span><span class="sxs-lookup"><span data-stu-id="20708-1317">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="20708-1318">Lägg till funktion för att aktivera AllowTracing på prenumerationsnivå.</span><span class="sxs-lookup"><span data-stu-id="20708-1318">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="20708-1319">Uppdaterade följande cmdletar för att acceptera ResourceId som indata</span><span class="sxs-lookup"><span data-stu-id="20708-1319">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="20708-1320">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="20708-1320">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="20708-1321">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="20708-1321">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="20708-1322">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="20708-1322">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="20708-1323">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="20708-1323">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="20708-1324">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="20708-1324">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="20708-1325">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="20708-1325">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="20708-1326">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="20708-1326">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="20708-1327">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="20708-1327">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="20708-1328">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="20708-1328">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="20708-1329">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="20708-1329">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="20708-1330">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="20708-1330">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="20708-1331">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="20708-1331">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="20708-1332">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="20708-1332">Az.Automation</span></span>
* <span data-ttu-id="20708-1333">Uppdaterade Get-AzAutomationJobOutputRecord för att hantera postvärden av typen JSON och Text.</span><span class="sxs-lookup"><span data-stu-id="20708-1333">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="20708-1334">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="20708-1334">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="20708-1335">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="20708-1335">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="20708-1336">Ändrade beteende för Start-AzAutomationDscCompilationJob till att bara starta jobbet istället för att vänta på slutförandet.</span><span class="sxs-lookup"><span data-stu-id="20708-1336">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="20708-1337">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="20708-1337">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="20708-1338">Korrigering för Get-AzAutomationDscNode när using -Name returnerar alla noder.</span><span class="sxs-lookup"><span data-stu-id="20708-1338">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="20708-1339">Nu returnerar den endast den matchande noden.</span><span class="sxs-lookup"><span data-stu-id="20708-1339">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="20708-1340">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="20708-1340">Az.Compute</span></span>
* <span data-ttu-id="20708-1341">Lägg till parametrarna ProtectFromScaleIn och ProtectFromScaleSetAction i cmdleten Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="20708-1341">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="20708-1342">Nu är standardinställningen att vimpelparametern New-AzVM använder en tillgänglig plats om USA, östra inte stöds</span><span class="sxs-lookup"><span data-stu-id="20708-1342">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="20708-1343">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="20708-1343">Az.DataLakeStore</span></span>
* <span data-ttu-id="20708-1344">Uppdatera ADLS-sdk för att använda httpclient, integrera dataplanstestning med Azure-ramverk</span><span class="sxs-lookup"><span data-stu-id="20708-1344">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="20708-1345">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="20708-1345">Az.Monitor</span></span>
* <span data-ttu-id="20708-1346">Korrigera felaktiga parameternamn i hjälpexempel</span><span class="sxs-lookup"><span data-stu-id="20708-1346">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="20708-1347">Az.Network</span><span class="sxs-lookup"><span data-stu-id="20708-1347">Az.Network</span></span>
* <span data-ttu-id="20708-1348">Lägg till flaggan DisableBgpRoutePropagation i utdata för effektiv routningstabell</span><span class="sxs-lookup"><span data-stu-id="20708-1348">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="20708-1349">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="20708-1349">Updated cmdlet:</span></span>
        - <span data-ttu-id="20708-1350">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="20708-1350">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="20708-1351">Åtgärda dubbelstreck i dokumentationen New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="20708-1351">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="20708-1352">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="20708-1352">Az.Resources</span></span>
* <span data-ttu-id="20708-1353">Lägg till ny cmdlet Get-AzureRmDenyAssignment för att hämta tilldelningsnekanden</span><span class="sxs-lookup"><span data-stu-id="20708-1353">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="20708-1354">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="20708-1354">Az.Sql</span></span>
* <span data-ttu-id="20708-1355">Döp om Advanced Threat Protection-cmdletar för Advanced Data Security och aktivera Vulnerability Assessment som standard</span><span class="sxs-lookup"><span data-stu-id="20708-1355">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="20708-1356">2.0.0 – maj 2019</span><span class="sxs-lookup"><span data-stu-id="20708-1356">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="20708-1357">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="20708-1357">Az.Accounts</span></span>
* <span data-ttu-id="20708-1358">Uppdatera autentiseringsbiblioteket för att åtgärda ADFS-problem med autentisering av användarnamn/lösenord</span><span class="sxs-lookup"><span data-stu-id="20708-1358">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="20708-1359">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="20708-1359">Az.CognitiveServices</span></span>
* <span data-ttu-id="20708-1360">Visa endast Bing-ansvarsfriskrivning för Bing-sökningstjänster.</span><span class="sxs-lookup"><span data-stu-id="20708-1360">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="20708-1361">Förbättra felmeddelande när det inte går att skapa konton.</span><span class="sxs-lookup"><span data-stu-id="20708-1361">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="20708-1362">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="20708-1362">Az.Compute</span></span>
* <span data-ttu-id="20708-1363">Funktion för närhetsplaceringsgrupper.</span><span class="sxs-lookup"><span data-stu-id="20708-1363">Proximity placement group feature.</span></span>
    - <span data-ttu-id="20708-1364">Följande nya cmdletar har lagts till:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="20708-1364">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="20708-1365">Den nya parametern ProximityPlacementGroupId har lagts till i följande cmdletar:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="20708-1365">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="20708-1366">Parametern StorageAccountType har lagts till i New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="20708-1366">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="20708-1367">TargetRegion för New-AzGalleryImageVersion kan innehålla StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="20708-1367">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="20708-1368">Växlingsparametern SkipShutdown har lagts till i Stop-AzVM och Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="20708-1368">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="20708-1369">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="20708-1369">Breaking changes</span></span>
    - <span data-ttu-id="20708-1370">Set-AzVMBootDiagnostics har ändrats till Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="20708-1370">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="20708-1371">Export-AzLogAnalyticThrottledRequests har ändrats till Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="20708-1371">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="20708-1372">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="20708-1372">Az.DeploymentManager</span></span>
* <span data-ttu-id="20708-1373">De första allmänt tillgängliga versionerna av cmdletar för Distributionshanteraren i Azure</span><span class="sxs-lookup"><span data-stu-id="20708-1373">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="20708-1374">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="20708-1374">Az.Dns</span></span>
* <span data-ttu-id="20708-1375">Automatisk delegering av DNS för NameServer</span><span class="sxs-lookup"><span data-stu-id="20708-1375">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="20708-1376">Det överordnade zonnamnet kan användas som ytterligare valfri parameter i cmdleten för att skapa DNS-zoner.</span><span class="sxs-lookup"><span data-stu-id="20708-1376">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="20708-1377">Lägger till NS-poster för en nyligen skapad underordnad zon i den överordnade zonen.</span><span class="sxs-lookup"><span data-stu-id="20708-1377">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="20708-1378">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="20708-1378">Az.FrontDoor</span></span>
* <span data-ttu-id="20708-1379">De första allmänt tillgängliga versionerna av cmdletar för Azure FrontDoor</span><span class="sxs-lookup"><span data-stu-id="20708-1379">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="20708-1380">Byt namn på WAF-cmdletar så att de omfattar ”Waf”</span><span class="sxs-lookup"><span data-stu-id="20708-1380">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="20708-1381">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="20708-1381">Az.HDInsight</span></span>
* <span data-ttu-id="20708-1382">Två cmdletar har tagits bort:</span><span class="sxs-lookup"><span data-stu-id="20708-1382">Removed two cmdlets:</span></span>
    - <span data-ttu-id="20708-1383">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="20708-1383">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="20708-1384">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="20708-1384">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="20708-1385">En ny cmdlet har lagts till, Set-AzHDInsightGatewayCredential, som ersätter Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="20708-1385">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="20708-1386">Uppdatera cmdleten Get-AzHDInsightJobOutput för att skilja mellan läsarrollen och HDInsight-operatörsrollen:</span><span class="sxs-lookup"><span data-stu-id="20708-1386">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="20708-1387">Användare med läsarrollen måste uttryckligen ange parametern ”DefaultStorageAccountKey”, annars uppstår fel.</span><span class="sxs-lookup"><span data-stu-id="20708-1387">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="20708-1388">Användare med HDInsight-operatörsrollen påverkas inte.</span><span class="sxs-lookup"><span data-stu-id="20708-1388">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="20708-1389">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="20708-1389">Az.Monitor</span></span>
* <span data-ttu-id="20708-1390">Nya cmdletar för SQR API (schemalagd frågeregel)</span><span class="sxs-lookup"><span data-stu-id="20708-1390">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="20708-1391">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="20708-1391">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="20708-1392">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="20708-1392">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="20708-1393">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="20708-1393">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="20708-1394">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="20708-1394">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="20708-1395">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="20708-1395">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="20708-1396">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="20708-1396">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="20708-1397">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="20708-1397">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="20708-1398">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="20708-1398">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="20708-1399">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="20708-1399">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="20708-1400">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="20708-1400">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="20708-1401">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="20708-1401">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="20708-1402">[Mer](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information om SQR API</span><span class="sxs-lookup"><span data-stu-id="20708-1402">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="20708-1403">Az.Monitor.md har uppdaterats för att omfatta cmdletar för måttbaserade aviseringsregler i GenV2 (inte klassiska)</span><span class="sxs-lookup"><span data-stu-id="20708-1403">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="20708-1404">Az.Network</span><span class="sxs-lookup"><span data-stu-id="20708-1404">Az.Network</span></span>
* <span data-ttu-id="20708-1405">Lägg till stöd för NAT Gateway-resurs</span><span class="sxs-lookup"><span data-stu-id="20708-1405">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="20708-1406">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="20708-1406">New cmdlets</span></span>
        - <span data-ttu-id="20708-1407">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="20708-1407">New-AzNatGateway</span></span>
        - <span data-ttu-id="20708-1408">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="20708-1408">Get-AzNatGateway</span></span>
        - <span data-ttu-id="20708-1409">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="20708-1409">Set-AzNatGateway</span></span>
        - <span data-ttu-id="20708-1410">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="20708-1410">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="20708-1411">Uppdaterade cmdletar</span><span class="sxs-lookup"><span data-stu-id="20708-1411">Updated cmdlets</span></span>
        - <span data-ttu-id="20708-1412">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="20708-1412">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="20708-1413">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="20708-1413">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="20708-1414">Nedanstående kommandon för funktionen har uppdaterats: Ange/ta bort anpassade vägar på Brooklyn Gateway.</span><span class="sxs-lookup"><span data-stu-id="20708-1414">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="20708-1415">New-AzVirtualNetworkGateway har uppdaterats: Den valfria parametern -CustomRoute har lagts till för att ställa in adressprefix som anpassade vägar för att ange gateway.</span><span class="sxs-lookup"><span data-stu-id="20708-1415">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="20708-1416">Set-AzVirtualNetworkGateway har uppdaterats: Den valfria parametern -CustomRoute har lagts till för att ange adressprefix som anpassade vägar för att ange gateway.</span><span class="sxs-lookup"><span data-stu-id="20708-1416">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="20708-1417">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="20708-1417">Az.PolicyInsights</span></span>
* <span data-ttu-id="20708-1418">Stöd för att fråga efter information om principutvärdering.</span><span class="sxs-lookup"><span data-stu-id="20708-1418">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="20708-1419">Lägg till parametern ”-Expand” för Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="20708-1419">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="20708-1420">Stöd för -Expand PolicyEvaluationDetails.</span><span class="sxs-lookup"><span data-stu-id="20708-1420">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="20708-1421">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="20708-1421">Az.RecoveryServices</span></span>
* <span data-ttu-id="20708-1422">Stöd för att dela prenumeration mellan Azure och Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="20708-1422">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="20708-1423">Markering av kommande icke-bakåtkompatibla ändringar för Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="20708-1423">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="20708-1424">Korrigering för återställningsplan och åtgärdsplan i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="20708-1424">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="20708-1425">Korrigering för mappning av uppdateringsnätverk i Azure Site Recovery för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="20708-1425">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="20708-1426">Korrigering för instruktioner för uppdateringsskydd i Azure Site Recovery för Azure till Azure för hanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="20708-1426">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="20708-1427">Andra mindre korrigeringar.</span><span class="sxs-lookup"><span data-stu-id="20708-1427">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="20708-1428">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="20708-1428">Az.Relay</span></span>
* <span data-ttu-id="20708-1429">Korrigera stavfel i kundriktade meddelanden</span><span class="sxs-lookup"><span data-stu-id="20708-1429">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="20708-1430">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="20708-1430">Az.ServiceBus</span></span>
* <span data-ttu-id="20708-1431">Nya cmdletar har lagts till för NetworkRuleSet för namnområden</span><span class="sxs-lookup"><span data-stu-id="20708-1431">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="20708-1432">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="20708-1432">Az.Storage</span></span>
* <span data-ttu-id="20708-1433">Uppgradera till lagringsklientbiblioteket 10.0.1 (namnområdet för alla objekt från detta SDK ändras från ”Microsoft.WindowsAzure.Storage. *till ”Microsoft.Azure.Storage.* ”)</span><span class="sxs-lookup"><span data-stu-id="20708-1433">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="20708-1434">Uppgradera till Microsoft.Azure.Management.Storage 11.0.0 för att stödja den nya API-versionen 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="20708-1434">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="20708-1435">Standardlagringskontot i Skapa lagringskonto ändras från ”Storage” till ”StorageV2”</span><span class="sxs-lookup"><span data-stu-id="20708-1435">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="20708-1436">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="20708-1436">New-AzStorageAccount</span></span>
* <span data-ttu-id="20708-1437">Ändra lagringskontots cmdlet-utdata Sku.Name för att passa med indata-SkuName genom att lägga till ”-”. Till exempel ändras ”StandardLRS” till ”Standard_LRS”</span><span class="sxs-lookup"><span data-stu-id="20708-1437">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="20708-1438">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="20708-1438">New-AzStorageAccount</span></span>
    - <span data-ttu-id="20708-1439">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="20708-1439">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="20708-1440">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="20708-1440">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="20708-1441">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="20708-1441">Az.Websites</span></span>
* <span data-ttu-id="20708-1442">Egenskapen ”typ” konfigureras nu för PSSite-objekt som returneras av Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="20708-1442">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="20708-1443">Get-AzWebApp\*Metrics och Get-AzAppServicePlanMetrics markeras som inaktuella</span><span class="sxs-lookup"><span data-stu-id="20708-1443">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="20708-1444">1.8.0 – april 2019</span><span class="sxs-lookup"><span data-stu-id="20708-1444">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="20708-1445">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="20708-1445">Highlights since the last major release</span></span>
* <span data-ttu-id="20708-1446">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="20708-1446">General availability of `Az` module</span></span>
* <span data-ttu-id="20708-1447">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="20708-1447">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="20708-1448">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="20708-1448">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="20708-1449">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="20708-1449">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="20708-1450">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="20708-1450">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="20708-1451">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="20708-1451">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="20708-1452">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="20708-1452">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="20708-1453">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="20708-1453">Az.Accounts</span></span>
* <span data-ttu-id="20708-1454">Uppdatera Uninstall-AzureRm för att ta bort moduler i Mac på ett korrekt sätt</span><span class="sxs-lookup"><span data-stu-id="20708-1454">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="20708-1455">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="20708-1455">Az.Batch</span></span>
* <span data-ttu-id="20708-1456">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="20708-1456">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="20708-1457">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="20708-1457">Az.Cdn</span></span>
* <span data-ttu-id="20708-1458">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="20708-1458">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="20708-1459">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="20708-1459">Az.CognitiveServices</span></span>
* <span data-ttu-id="20708-1460">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="20708-1460">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="20708-1461">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="20708-1461">Az.Compute</span></span>
* <span data-ttu-id="20708-1462">Åtgärda problem med AEM-installationen om resurs-ID:n för diskar innehåller resourcegroups i gemener i resurs-ID:n</span><span class="sxs-lookup"><span data-stu-id="20708-1462">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="20708-1463">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="20708-1463">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="20708-1464">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="20708-1464">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="20708-1465">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="20708-1465">Az.DataFactory</span></span>
* <span data-ttu-id="20708-1466">Lägg till SsisProperties om NodeCount inte är null för hanterad integreringskörning.</span><span class="sxs-lookup"><span data-stu-id="20708-1466">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="20708-1467">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="20708-1467">Az.DataLakeStore</span></span>
* <span data-ttu-id="20708-1468">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="20708-1468">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="20708-1469">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="20708-1469">Az.EventGrid</span></span>
* <span data-ttu-id="20708-1470">Hjälptexten för slutpunkten har uppdaterats för att visa att resurser ska skapas innan cmdletarna för att skapa/uppdatera händelseprenumerationer används.</span><span class="sxs-lookup"><span data-stu-id="20708-1470">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="20708-1471">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="20708-1471">Az.EventHub</span></span>
* <span data-ttu-id="20708-1472">Nya cmdletar har lagts till för NetworkRuleSet för namnområden</span><span class="sxs-lookup"><span data-stu-id="20708-1472">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="20708-1473">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="20708-1473">Az.HDInsight</span></span>
* <span data-ttu-id="20708-1474">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="20708-1474">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="20708-1475">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="20708-1475">Az.IotHub</span></span>
* <span data-ttu-id="20708-1476">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="20708-1476">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="20708-1477">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="20708-1477">Az.KeyVault</span></span>
* <span data-ttu-id="20708-1478">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="20708-1478">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="20708-1479">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="20708-1479">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="20708-1480">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="20708-1480">Az.MachineLearning</span></span>
* <span data-ttu-id="20708-1481">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="20708-1481">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="20708-1482">Az.Media</span><span class="sxs-lookup"><span data-stu-id="20708-1482">Az.Media</span></span>
* <span data-ttu-id="20708-1483">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="20708-1483">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="20708-1484">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="20708-1484">Az.Monitor</span></span>
  * <span data-ttu-id="20708-1485">Nya cmdletar för måttbaserad aviseringsregel i GenV2 (inte klassisk)</span><span class="sxs-lookup"><span data-stu-id="20708-1485">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="20708-1486">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="20708-1486">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="20708-1487">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="20708-1487">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="20708-1488">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="20708-1488">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="20708-1489">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="20708-1489">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="20708-1490">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="20708-1490">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="20708-1491">Monitor SDK har uppdaterats till version 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="20708-1491">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="20708-1492">Az.Network</span><span class="sxs-lookup"><span data-stu-id="20708-1492">Az.Network</span></span>
* <span data-ttu-id="20708-1493">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="20708-1493">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="20708-1494">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="20708-1494">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="20708-1495">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="20708-1495">Az.NotificationHubs</span></span>
* <span data-ttu-id="20708-1496">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="20708-1496">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="20708-1497">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="20708-1497">Az.OperationalInsights</span></span>
* <span data-ttu-id="20708-1498">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="20708-1498">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="20708-1499">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="20708-1499">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="20708-1500">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="20708-1500">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="20708-1501">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="20708-1501">Az.RecoveryServices</span></span>
* <span data-ttu-id="20708-1502">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="20708-1502">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="20708-1503">Tabellformatet för SQL i virtuella Azure-datorer har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="20708-1503">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="20708-1504">En alternativ metod för att hämta platser i AzureFileShare har lagts till</span><span class="sxs-lookup"><span data-stu-id="20708-1504">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="20708-1505">ScheduleRunDays i SchedulePolicy-objekt har uppdaterats enligt tidszon</span><span class="sxs-lookup"><span data-stu-id="20708-1505">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="20708-1506">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="20708-1506">Az.RedisCache</span></span>
* <span data-ttu-id="20708-1507">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="20708-1507">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="20708-1508">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="20708-1508">Az.Resources</span></span>
* <span data-ttu-id="20708-1509">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="20708-1509">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="20708-1510">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="20708-1510">Az.Sql</span></span>
* <span data-ttu-id="20708-1511">Ersätt Monitor SDK-beroende med vanlig kod</span><span class="sxs-lookup"><span data-stu-id="20708-1511">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="20708-1512">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="20708-1512">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="20708-1513">Förbättrad process för klassificering av flera kolumner.</span><span class="sxs-lookup"><span data-stu-id="20708-1513">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="20708-1514">Inkludera SKU-egenskaper (SKU-namn, serie, kapacitet) i svaret från Get-AzSqlServerServiceObjective och formatera som tabell som standard.</span><span class="sxs-lookup"><span data-stu-id="20708-1514">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="20708-1515">Möjlighet att använda Get-AzSqlServerServiceObjective efter plats utan att behöva en redan befintlig server i regionen.</span><span class="sxs-lookup"><span data-stu-id="20708-1515">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="20708-1516">Stöd för tidszonsparametern när hanterade instanser skapas.</span><span class="sxs-lookup"><span data-stu-id="20708-1516">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="20708-1517">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="20708-1517">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="20708-1518">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="20708-1518">Az.Websites</span></span>
* <span data-ttu-id="20708-1519">åtgärdar Set-AzWebApp och Set-AzWebAppSlot så att de inte tar bort taggar vid körning</span><span class="sxs-lookup"><span data-stu-id="20708-1519">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="20708-1520">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="20708-1520">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="20708-1521">SDK för WebSites har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="20708-1521">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="20708-1522">Egenskapen AdminSiteName har tagits bort från PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="20708-1522">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="20708-1523">1.7.0 – april 2019</span><span class="sxs-lookup"><span data-stu-id="20708-1523">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="20708-1524">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="20708-1524">Highlights since the last major release</span></span>
* <span data-ttu-id="20708-1525">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="20708-1525">General availability of `Az` module</span></span>
* <span data-ttu-id="20708-1526">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="20708-1526">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="20708-1527">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="20708-1527">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="20708-1528">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="20708-1528">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="20708-1529">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="20708-1529">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="20708-1530">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="20708-1530">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="20708-1531">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="20708-1531">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="20708-1532">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="20708-1532">Az.Accounts</span></span>
* <span data-ttu-id="20708-1533">Add-AzEnvironment och Set-AzEnvironment har uppdaterats för att godkänna parametern AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="20708-1533">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="20708-1534">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="20708-1534">Az.AnalysisServices</span></span>
* <span data-ttu-id="20708-1535">ServiceClient används i cmdletar för dataplan och den ursprungliga autentiseringslogiken har tagits bort</span><span class="sxs-lookup"><span data-stu-id="20708-1535">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="20708-1536">Add-AzureASAccount används för omslutning av Connect-AzAccount för att undvika en icke-bakåtkompatibel ändring</span><span class="sxs-lookup"><span data-stu-id="20708-1536">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="20708-1537">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="20708-1537">Az.Automation</span></span>
* <span data-ttu-id="20708-1538">Buggen för cmdleten New-AzAutomationSoftwareUpdateConfiguration för inkluderingar har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="20708-1538">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="20708-1539">Nu bör parametern IncludedKbNumber och IncludedPackageNameMask fungera.</span><span class="sxs-lookup"><span data-stu-id="20708-1539">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="20708-1540">Felkorrigering för dynamiska grupper i uppdateringshanteringen för azure automation</span><span class="sxs-lookup"><span data-stu-id="20708-1540">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="20708-1541">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="20708-1541">Az.Compute</span></span>
* <span data-ttu-id="20708-1542">Lägg till parametern HyperVGeneration i New-AzDiskConfig och New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="20708-1542">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="20708-1543">Tillåt att virtuella datorer skapas med galleribilder från andra klientorganisationer.</span><span class="sxs-lookup"><span data-stu-id="20708-1543">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="20708-1544">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="20708-1544">Az.ContainerInstance</span></span>
* <span data-ttu-id="20708-1545">Ett problem har åtgärdats i parametern -Command för New-AzContainerGroup som lade till ett avslutande tomt argument</span><span class="sxs-lookup"><span data-stu-id="20708-1545">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="20708-1546">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="20708-1546">Az.DataFactory</span></span>
* <span data-ttu-id="20708-1547">ADF .Net SDK-versionen har uppdaterats till 3.0.2</span><span class="sxs-lookup"><span data-stu-id="20708-1547">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="20708-1548">Cmdleten Set-AzDataFactoryV2 har uppdaterats med extra parametrar för inställningar som rör RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="20708-1548">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="20708-1549">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="20708-1549">Az.Resources</span></span>
* <span data-ttu-id="20708-1550">Förbättra hanteringen av providrar för Get-AzResource när parametrarna -ResourceId eller -ResourceGroupName, -Name och -ResourceType tillhandahålls</span><span class="sxs-lookup"><span data-stu-id="20708-1550">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="20708-1551">Förbättra felhanteringen för ”Test-AzDeployment” och ”Test-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="20708-1551">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="20708-1552">Hantera fel utanför distributionsvalideringen och ta med dem i kommandoutdata istället</span><span class="sxs-lookup"><span data-stu-id="20708-1552">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="20708-1553">Mer information här: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="20708-1553">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="20708-1554">Lägg till växlingsparametern -IgnoreDynamicParameters till en uppsättning av cmdletar för distribution för att hoppa över fråga i skript och jobbscenarier</span><span class="sxs-lookup"><span data-stu-id="20708-1554">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="20708-1555">Mer information här: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="20708-1555">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="20708-1556">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="20708-1556">Az.Sql</span></span>
* <span data-ttu-id="20708-1557">Stöd för dataklassificering av databaser.</span><span class="sxs-lookup"><span data-stu-id="20708-1557">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="20708-1558">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="20708-1558">Az.Storage</span></span>
* <span data-ttu-id="20708-1559">Rapportera detaljfel när lagringskontext skapas med parametern -UseConnectedAccount, men utan inloggning på Azure-kontot</span><span class="sxs-lookup"><span data-stu-id="20708-1559">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="20708-1560">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="20708-1560">New-AzStorageContext</span></span>
* <span data-ttu-id="20708-1561">Stöd för att hantera Blob Service-egenskaper för ett angivet lagringskonto med API:et för hanteringsplan</span><span class="sxs-lookup"><span data-stu-id="20708-1561">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="20708-1562">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="20708-1562">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="20708-1563">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="20708-1563">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="20708-1564">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="20708-1564">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="20708-1565">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="20708-1565">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="20708-1566">Stöd för -AsJob-cmdletar för att ladda upp och ladda ned blobar och filer</span><span class="sxs-lookup"><span data-stu-id="20708-1566">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="20708-1567">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="20708-1567">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="20708-1568">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="20708-1568">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="20708-1569">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="20708-1569">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="20708-1570">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="20708-1570">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="20708-1571">1.6.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="20708-1571">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="20708-1572">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="20708-1572">Highlights since the last major release</span></span>
* <span data-ttu-id="20708-1573">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="20708-1573">General availability of `Az` module</span></span>
* <span data-ttu-id="20708-1574">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="20708-1574">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="20708-1575">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="20708-1575">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="20708-1576">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="20708-1576">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="20708-1577">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="20708-1577">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="20708-1578">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="20708-1578">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="20708-1579">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="20708-1579">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="20708-1580">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="20708-1580">Az.Automation</span></span>
* <span data-ttu-id="20708-1581">Azure Automation – ändring av uppdateringshantering för stöd för de nya funktionerna:</span><span class="sxs-lookup"><span data-stu-id="20708-1581">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="20708-1582">Dynamisk gruppering</span><span class="sxs-lookup"><span data-stu-id="20708-1582">Dynamic grouping</span></span>
    * <span data-ttu-id="20708-1583">För-/efterskrift</span><span class="sxs-lookup"><span data-stu-id="20708-1583">Pre-Post script</span></span>
    * <span data-ttu-id="20708-1584">Inställning för omstart</span><span class="sxs-lookup"><span data-stu-id="20708-1584">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="20708-1585">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="20708-1585">Az.Compute</span></span>
* <span data-ttu-id="20708-1586">Åtgärda problem med sökvägsmatchning i Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="20708-1586">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="20708-1587">Uppdatera Compute-klientbibliotek till 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="20708-1587">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="20708-1588">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="20708-1588">Az.KeyVault</span></span>
* <span data-ttu-id="20708-1589">Stöd för jokertecken för KeyVault-cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="20708-1589">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="20708-1590">Az.Network</span><span class="sxs-lookup"><span data-stu-id="20708-1590">Az.Network</span></span>
* <span data-ttu-id="20708-1591">Lägg till stöd för Threat Intelligence för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="20708-1591">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="20708-1592">Lägg till resurs för brandväggsprincip på översta nivå och anpassade regler för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="20708-1592">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="20708-1593">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="20708-1593">Az.RecoveryServices</span></span>
* <span data-ttu-id="20708-1594">SnapshotRetentionInDays har lagts till i Azure-principen för virtuella datorer för stöd av Instant RP</span><span class="sxs-lookup"><span data-stu-id="20708-1594">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="20708-1595">Pipe-stöd för avregistrering av container har lagts till</span><span class="sxs-lookup"><span data-stu-id="20708-1595">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="20708-1596">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="20708-1596">Az.Resources</span></span>
* <span data-ttu-id="20708-1597">Uppdatera stöd för jokertecken för Get-AzResource och Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="20708-1597">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="20708-1598">Uppdatera autentiseringsuppgifter som används vid allmänna anrop till ARM</span><span class="sxs-lookup"><span data-stu-id="20708-1598">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="20708-1599">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="20708-1599">Az.Sql</span></span>
* <span data-ttu-id="20708-1600">Cmdlet-parametern (ExcludeDetectionType) för Hotidentifiering ändrades från DetectionType till sträng[] för att framtidssäkra den när nya DetectionTypes läggs till, och även för att stödja automatisk ifyllning.</span><span class="sxs-lookup"><span data-stu-id="20708-1600">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="20708-1601">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="20708-1601">Az.Storage</span></span>
* <span data-ttu-id="20708-1602">Stöd för att hämta/ange/ta bort hanteringsprincip på ett lagringskonto</span><span class="sxs-lookup"><span data-stu-id="20708-1602">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="20708-1603">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="20708-1603">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="20708-1604">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="20708-1604">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="20708-1605">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="20708-1605">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="20708-1606">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="20708-1606">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="20708-1607">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="20708-1607">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="20708-1608">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="20708-1608">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="20708-1609">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="20708-1609">Az.Websites</span></span>
* <span data-ttu-id="20708-1610">Åtgärda fel med ARM-mall som avbryter kloning av alla platser med 'New-AzWebApp -IncludeSourceWebAppSlots'</span><span class="sxs-lookup"><span data-stu-id="20708-1610">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="20708-1611">1.5.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="20708-1611">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="20708-1612">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="20708-1612">Az.Accounts</span></span>
* <span data-ttu-id="20708-1613">Lägg till kommandot Register-AzModule för stöd för AutoRest-genererade cmdletar</span><span class="sxs-lookup"><span data-stu-id="20708-1613">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="20708-1614">Uppdatera exempel för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="20708-1614">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="20708-1615">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="20708-1615">Az.Automation</span></span>
* <span data-ttu-id="20708-1616">Problem med att hämta vissa månadsscheman i flera Azure Automation-cmdletar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="20708-1616">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="20708-1617">Åtgärda problem med att Get-AzAutomationDscNode bara returnerar de 20 översta noderna.</span><span class="sxs-lookup"><span data-stu-id="20708-1617">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="20708-1618">Nu returneras alla noder</span><span class="sxs-lookup"><span data-stu-id="20708-1618">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="20708-1619">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="20708-1619">Az.Cdn</span></span>
* <span data-ttu-id="20708-1620">Nya Powershell-cmdletar för att aktivera/inaktivera anpassade domän-HTTPS har lagts till och de gamla har gjorts inaktuella</span><span class="sxs-lookup"><span data-stu-id="20708-1620">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="20708-1621">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="20708-1621">Az.Compute</span></span>
* <span data-ttu-id="20708-1622">Lägg till stöd för jokertecken för Get-cmdletar</span><span class="sxs-lookup"><span data-stu-id="20708-1622">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="20708-1623">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="20708-1623">Az.DataFactory</span></span>
* <span data-ttu-id="20708-1624">ADF .Net SDK-versionen har uppdaterats till 3.0.1</span><span class="sxs-lookup"><span data-stu-id="20708-1624">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="20708-1625">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="20708-1625">Az.LogicApp</span></span>
* <span data-ttu-id="20708-1626">Åtgärda problemet med att ListWorkflows endast hämtar den första sidan med resultat</span><span class="sxs-lookup"><span data-stu-id="20708-1626">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="20708-1627">Az.Network</span><span class="sxs-lookup"><span data-stu-id="20708-1627">Az.Network</span></span>
* <span data-ttu-id="20708-1628">Lägg till stöd för jokertecken för Network-cmdletar</span><span class="sxs-lookup"><span data-stu-id="20708-1628">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="20708-1629">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="20708-1629">Az.RecoveryServices</span></span>
* <span data-ttu-id="20708-1630">Stöd har lagts till för SQL Server i virtuella Azure-datorer</span><span class="sxs-lookup"><span data-stu-id="20708-1630">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="20708-1631">SDK-uppdatering</span><span class="sxs-lookup"><span data-stu-id="20708-1631">SDK Update</span></span>
* <span data-ttu-id="20708-1632">Get-ProtectableItem-incheckning i VMappContainer har tagits bort</span><span class="sxs-lookup"><span data-stu-id="20708-1632">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="20708-1633">Name och ServerName har lagts till som parametrar för Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="20708-1633">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="20708-1634">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="20708-1634">Az.Resources</span></span>
* <span data-ttu-id="20708-1635">Lägg till parametern `-TemplateObject` i cmdletar för distribution</span><span class="sxs-lookup"><span data-stu-id="20708-1635">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="20708-1636">Mer information här: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="20708-1636">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="20708-1637">Åtgärda problem med piping av resultatet i `Get-AzResource` till `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="20708-1637">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="20708-1638">Mer information här: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="20708-1638">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="20708-1639">Åtgärda problem med ändring av JSON-datatyp när `Set-AzResource` körs</span><span class="sxs-lookup"><span data-stu-id="20708-1639">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="20708-1640">Mer information här: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="20708-1640">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="20708-1641">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="20708-1641">Az.Sql</span></span>
* <span data-ttu-id="20708-1642">AuditingEndpointsCommunicator uppdateras.</span><span class="sxs-lookup"><span data-stu-id="20708-1642">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="20708-1643">Åtgärdar beteendet hos ett gränsscenario när nya diagnostikinställningar skapas.</span><span class="sxs-lookup"><span data-stu-id="20708-1643">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="20708-1644">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="20708-1644">Az.Storage</span></span>
* <span data-ttu-id="20708-1645">Stöd för BlockBlobStorage när Storage-konto skapas      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="20708-1645">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="20708-1646">1.4.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="20708-1646">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="20708-1647">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="20708-1647">Az.AnalysisServices</span></span>
* <span data-ttu-id="20708-1648">Inaktuell AddAzureASAccount-cmdlet</span><span class="sxs-lookup"><span data-stu-id="20708-1648">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="20708-1649">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="20708-1649">Az.Automation</span></span>
* <span data-ttu-id="20708-1650">Hjälpen för Import-AzAutomationDscNodeConfiguration har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="20708-1650">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="20708-1651">Konfigurationsnamnsvalidering har lagts till i cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="20708-1651">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="20708-1652">Förbättrad felhantering för cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="20708-1652">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="20708-1653">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="20708-1653">Az.CognitiveServices</span></span>
* <span data-ttu-id="20708-1654">CustomSubdomainName har lagts till som en ny valfri parameter för New-AzCognitiveServicesAccount, som används för att ange underdomän för resursen.</span><span class="sxs-lookup"><span data-stu-id="20708-1654">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="20708-1655">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="20708-1655">Az.Compute</span></span>
* <span data-ttu-id="20708-1656">Problemet med ID-parameteruppsättningar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="20708-1656">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="20708-1657">Get-AzVMExtension har uppdaterats så att alla installerade tillägg visas om parametern Name inte har angetts</span><span class="sxs-lookup"><span data-stu-id="20708-1657">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="20708-1658">Parametrarna Tag och ResourceId har lagts till i cmdleten Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="20708-1658">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="20708-1659">Get-AzVmssVM utan instans-ID och med InstanceView kan visa virtuella VMSS-datorer med instansvyn.</span><span class="sxs-lookup"><span data-stu-id="20708-1659">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="20708-1660">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="20708-1660">Az.DataLakeStore</span></span>
* <span data-ttu-id="20708-1661">Cmdletar har lagts till för uppräkning och återställning av borttagna objekt i ADL</span><span class="sxs-lookup"><span data-stu-id="20708-1661">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="20708-1662">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="20708-1662">Az.EventHub</span></span>
* <span data-ttu-id="20708-1663">Ny boolesk egenskap SkipEmptyArchives har lagts till i Skip Empty Archives i CaptureDescription-klassen i Eventhub</span><span class="sxs-lookup"><span data-stu-id="20708-1663">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="20708-1664">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="20708-1664">Az.KeyVault</span></span>
* <span data-ttu-id="20708-1665">Taggning i Set-AzKeyVaultSecret har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="20708-1665">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="20708-1666">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="20708-1666">Az.LogicApp</span></span>
* <span data-ttu-id="20708-1667">Grundläggande SKU har lagts till för Integrationskonton</span><span class="sxs-lookup"><span data-stu-id="20708-1667">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="20708-1668">XSLT 2.0, XSLT 3.0 och Flytande mappningstyper har lagts till</span><span class="sxs-lookup"><span data-stu-id="20708-1668">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="20708-1669">Nya cmdletar för integrationskontosammansättningar</span><span class="sxs-lookup"><span data-stu-id="20708-1669">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="20708-1670">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="20708-1670">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="20708-1671">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="20708-1671">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="20708-1672">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="20708-1672">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="20708-1673">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="20708-1673">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="20708-1674">Nya cmdletar för batchkonfiguration för integrationskonto</span><span class="sxs-lookup"><span data-stu-id="20708-1674">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="20708-1675">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="20708-1675">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="20708-1676">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="20708-1676">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="20708-1677">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="20708-1677">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="20708-1678">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="20708-1678">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="20708-1679">Logic App-SDK har uppdaterats till version 4.1.0</span><span class="sxs-lookup"><span data-stu-id="20708-1679">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="20708-1680">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="20708-1680">Az.Monitor</span></span>
* <span data-ttu-id="20708-1681">Hjälpen för Get-AzMetric har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="20708-1681">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="20708-1682">Az.Network</span><span class="sxs-lookup"><span data-stu-id="20708-1682">Az.Network</span></span>
* <span data-ttu-id="20708-1683">Hjälpexempel för Add-AzApplicationGatewayCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="20708-1683">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="20708-1684">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="20708-1684">Az.OperationalInsights</span></span>
* <span data-ttu-id="20708-1685">Ytterligare stöd för datakällorna New och Get ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="20708-1685">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="20708-1686">Ny ApplicationInsights-typ har lagts till för att ge stöd för ”Get specific” och ”Get all” för ApplicationInsights-datakällor för angiven arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="20708-1686">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="20708-1687">Cmdleten New-AzOperationalInsightsApplicationInsightsDataSource har lagts till för att skapa datakälla med angivna parametrar för Application Insights-resurs: subscription Id, resourceGroupName och name.</span><span class="sxs-lookup"><span data-stu-id="20708-1687">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="20708-1688">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="20708-1688">Az.Resources</span></span>
* <span data-ttu-id="20708-1689">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="20708-1689">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="20708-1690">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="20708-1690">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="20708-1691">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="20708-1691">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="20708-1692">Fel som gör att KeyCredentials inte kan skapas upprepade gånger har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="20708-1692">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="20708-1693">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="20708-1693">Az.Sql</span></span>
* <span data-ttu-id="20708-1694">Lägg till stöd för hyperskalanivån för SQL DB</span><span class="sxs-lookup"><span data-stu-id="20708-1694">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="20708-1695">Ett fel har åtgärdats där återställningen kunde misslyckas på grund av onödiga inställningsegenskaper i restore-förfrågan</span><span class="sxs-lookup"><span data-stu-id="20708-1695">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="20708-1696">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="20708-1696">Az.Websites</span></span>
* <span data-ttu-id="20708-1697">Rätt exempel i Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="20708-1697">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="20708-1698">1.3.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="20708-1698">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="20708-1699">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="20708-1699">Az.Accounts</span></span>
* <span data-ttu-id="20708-1700">Uppdatera till den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="20708-1700">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="20708-1701">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="20708-1701">Az.AnalysisServices</span></span>
<span data-ttu-id="20708-1702">Allmän tillgänglighet för Az.AnalysisServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="20708-1702">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="20708-1703">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="20708-1703">Az.Compute</span></span>
* <span data-ttu-id="20708-1704">AEM-tillägg: Lägg till stöd för UltraSSD-, P60-, P70- och P80-diskar</span><span class="sxs-lookup"><span data-stu-id="20708-1704">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="20708-1705">Uppdatera hjälpbeskrivning för Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="20708-1705">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="20708-1706">Uppdatera hjälpbeskrivning och exempel för Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="20708-1706">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="20708-1707">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="20708-1707">Az.RecoveryServices</span></span>
<span data-ttu-id="20708-1708">Allmän tillgänglighet för Az.RecoveryServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="20708-1708">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="20708-1709">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="20708-1709">Az.Resources</span></span>
* <span data-ttu-id="20708-1710">Korrigera taggar för resursgrupper</span><span class="sxs-lookup"><span data-stu-id="20708-1710">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="20708-1711">Mer information här: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="20708-1711">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="20708-1712">Åtgärda problem där `Get-AzureRmRoleAssignment` inte respekterar -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="20708-1712">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="20708-1713">Mer information här: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="20708-1713">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="20708-1714">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="20708-1714">Az.Sql</span></span>
* <span data-ttu-id="20708-1715">Lägga till Get/Set-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="20708-1715">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="20708-1716">Åtgärda problem där ett nullref-undantag uppstår när du kör SQL-cmdletar och inte är inloggad på ett Azure-konto</span><span class="sxs-lookup"><span data-stu-id="20708-1716">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="20708-1717">Åtgärda nullref-undantag i Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="20708-1717">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="20708-1718">1.2.1 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="20708-1718">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="20708-1719">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="20708-1719">Az.Accounts</span></span>
* <span data-ttu-id="20708-1720">Version med rätt version av autentisering</span><span class="sxs-lookup"><span data-stu-id="20708-1720">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="20708-1721">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="20708-1721">Az.AnalysisServices</span></span>
* <span data-ttu-id="20708-1722">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="20708-1722">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="20708-1723">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="20708-1723">Az.RecoveryServices</span></span>
* <span data-ttu-id="20708-1724">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="20708-1724">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="20708-1725">1.2.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="20708-1725">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="20708-1726">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="20708-1726">Az.Accounts</span></span>
* <span data-ttu-id="20708-1727">Lägga till interaktiv autentisering och autentisering med användarnamn/lösenord för endast Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="20708-1727">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="20708-1728">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="20708-1728">Update incorrect online help URLs</span></span>
* <span data-ttu-id="20708-1729">Lägga till varningsmeddelande i PS Core för Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="20708-1729">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="20708-1730">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="20708-1730">Az.Aks</span></span>
* <span data-ttu-id="20708-1731">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="20708-1731">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="20708-1732">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="20708-1732">Az.Automation</span></span>
* <span data-ttu-id="20708-1733">Stöd för Python 2-runbookflöden har lagts till</span><span class="sxs-lookup"><span data-stu-id="20708-1733">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="20708-1734">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="20708-1734">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="20708-1735">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="20708-1735">Az.Cdn</span></span>
* <span data-ttu-id="20708-1736">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="20708-1736">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="20708-1737">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="20708-1737">Az.Compute</span></span>
* <span data-ttu-id="20708-1738">Lägga till cmdleten Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="20708-1738">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="20708-1739">Lägga till TempDisk-parameter i Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="20708-1739">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="20708-1740">Korrigera varningsmeddelande för New-AzVM</span><span class="sxs-lookup"><span data-stu-id="20708-1740">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="20708-1741">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="20708-1741">Az.ContainerRegistry</span></span>
* <span data-ttu-id="20708-1742">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="20708-1742">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="20708-1743">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="20708-1743">Az.DataFactory</span></span>
* <span data-ttu-id="20708-1744">ADF .Net SDK-versionen har uppdaterats till 3.0.0</span><span class="sxs-lookup"><span data-stu-id="20708-1744">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="20708-1745">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="20708-1745">Az.DataLakeStore</span></span>
* <span data-ttu-id="20708-1746">Åtgärda problem med ADLS-slutpunkt vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="20708-1746">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="20708-1747">Mer information här: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="20708-1747">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="20708-1748">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="20708-1748">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="20708-1749">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="20708-1749">Az.IotHub</span></span>
* <span data-ttu-id="20708-1750">Lägga till kodningsformat i cmdleten Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="20708-1750">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="20708-1751">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="20708-1751">Az.KeyVault</span></span>
* <span data-ttu-id="20708-1752">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="20708-1752">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="20708-1753">Az.Network</span><span class="sxs-lookup"><span data-stu-id="20708-1753">Az.Network</span></span>
* <span data-ttu-id="20708-1754">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="20708-1754">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="20708-1755">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="20708-1755">Az.Resources</span></span>
* <span data-ttu-id="20708-1756">Åtgärda felaktiga exempel i referensdokumentationen ”New-AzADAppCredential” och ”New-AzADSpCredential”</span><span class="sxs-lookup"><span data-stu-id="20708-1756">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="20708-1757">Åtgärda problem där sökvägen för parametern ”-TemplateFile” inte omvandlas innan cmdletarna för distribution i resursgruppen körs</span><span class="sxs-lookup"><span data-stu-id="20708-1757">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="20708-1758">Az.Resources: Korrigera dokumentationen om standardvärdet för New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="20708-1758">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="20708-1759">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="20708-1759">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="20708-1760">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="20708-1760">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="20708-1761">Åtgärda formateringsproblemet med objektet ”PSResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="20708-1761">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="20708-1762">Mer information här: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="20708-1762">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="20708-1763">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="20708-1763">Az.ServiceFabric</span></span>
* <span data-ttu-id="20708-1764">Återställ när ett certifikat läggs till i en Virtual Machine Scale Sets-modell men ett undantag genereras. Detta har gjorts för att åtgärda följande fel: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="20708-1764">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="20708-1765">Korrigera några felmeddelanden.</span><span class="sxs-lookup"><span data-stu-id="20708-1765">Fix some error messages.</span></span>
* <span data-ttu-id="20708-1766">Korrigering av skapande av kluster med ARM-mall som är standard för New-AzServiceFabriCluster som inte fungerade med migrering till Az.</span><span class="sxs-lookup"><span data-stu-id="20708-1766">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="20708-1767">Korrigering av tilläggning av kluster/programcertifikat så att endast VM Scale Sets som motsvarar klustret läggs till genom att kontrollera ID för klustret i tillägget.</span><span class="sxs-lookup"><span data-stu-id="20708-1767">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="20708-1768">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="20708-1768">Az.SignalR</span></span>
* <span data-ttu-id="20708-1769">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="20708-1769">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="20708-1770">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="20708-1770">Az.Sql</span></span>
* <span data-ttu-id="20708-1771">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="20708-1771">Update incorrect online help URLs</span></span>
* <span data-ttu-id="20708-1772">Uppdaterad parameterbeskrivning för LicenseType-parameter med möjliga värden</span><span class="sxs-lookup"><span data-stu-id="20708-1772">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="20708-1773">Korrigering för att uppdatera hanterad instansidentitet som inte fungerar när det är den enda uppdaterade egenskapen</span><span class="sxs-lookup"><span data-stu-id="20708-1773">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="20708-1774">Stöd för anpassad sortering på hanterad instans</span><span class="sxs-lookup"><span data-stu-id="20708-1774">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="20708-1775">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="20708-1775">Az.Storage</span></span>
* <span data-ttu-id="20708-1776">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="20708-1776">Update incorrect online help URLs</span></span>
* <span data-ttu-id="20708-1777">Tillhandahåll detaljerat felmeddelande när en användare försöker hämta/konfigurera klassisk loggning/mått på ett Premium Storage-konto eftersom Premium Storage-kontot inte har stöd för klassisk loggning/mått.</span><span class="sxs-lookup"><span data-stu-id="20708-1777">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="20708-1778">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="20708-1778">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="20708-1779">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="20708-1779">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="20708-1780">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="20708-1780">Az.TrafficManager</span></span>
* <span data-ttu-id="20708-1781">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="20708-1781">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="20708-1782">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="20708-1782">Az.Websites</span></span>
* <span data-ttu-id="20708-1783">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="20708-1783">Update incorrect online help URLs</span></span>
* <span data-ttu-id="20708-1784">Korrigerar ”New-AzWebAppSSLBinding” så att certifikatet laddas upp till rätt resursgrupp och plats om appen finns i en ASE.</span><span class="sxs-lookup"><span data-stu-id="20708-1784">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="20708-1785">Korrigerar ”New-AzWebAppSSLBinding” så att taggarna inte skrivs över på en bindning av ett SSL-certifikat till en app</span><span class="sxs-lookup"><span data-stu-id="20708-1785">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="20708-1786">1.1.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="20708-1786">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="20708-1787">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="20708-1787">Az.Accounts</span></span>
* <span data-ttu-id="20708-1788">Lade till omfattningen ”Lokal” till Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="20708-1788">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="20708-1789">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="20708-1789">Az.Compute</span></span>
* <span data-ttu-id="20708-1790">Namn är nu valfritt i ID-parametern för Restart/Start/Stop/Remove/Set-AzVM och Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="20708-1790">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="20708-1791">Uppdaterade beskrivningen av ID i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="20708-1791">Updated the description of ID in help files</span></span>
* <span data-ttu-id="20708-1792">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="20708-1792">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="20708-1793">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="20708-1793">Az.DataLakeStore</span></span>
* <span data-ttu-id="20708-1794">Uppdatera sdk-versionen av dataplanet till 1.1.14 för SDK-korrigeringar.</span><span class="sxs-lookup"><span data-stu-id="20708-1794">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="20708-1795">Korrigerade hanteringen av negativ accesstime och modificationtime för getfilestatus och liststatus; korrigera asynkront annulleringstoken</span><span class="sxs-lookup"><span data-stu-id="20708-1795">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="20708-1796">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="20708-1796">Az.EventGrid</span></span>
* <span data-ttu-id="20708-1797">Uppdaterat för användning av API-versionen 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="20708-1797">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="20708-1798">Uppdaterade följande cmdletar för att stödja nytt scenario i API-versionen 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="20708-1798">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="20708-1799">New-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="20708-1799">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="20708-1800">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="20708-1800">Event Time-To-Live,</span></span>
        - <span data-ttu-id="20708-1801">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="20708-1801">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="20708-1802">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="20708-1802">Dead letter endpoint.</span></span>
    - <span data-ttu-id="20708-1803">Update-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="20708-1803">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="20708-1804">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="20708-1804">Event Time-To-Live,</span></span>
        - <span data-ttu-id="20708-1805">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="20708-1805">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="20708-1806">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="20708-1806">Dead letter endpoint.</span></span>
* <span data-ttu-id="20708-1807">Lade till nya enum-värden (storageQueue och hybridConnection) för alternativet EndpointType i cmdletarna New-AzureRmEventGridSubscription och Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="20708-1807">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="20708-1808">Visa varningsmeddelanden om skapande eller uppdatering av händelseprenumerationen förväntas medföra manuell åtgärd från användaren.</span><span class="sxs-lookup"><span data-stu-id="20708-1808">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="20708-1809">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="20708-1809">Az.IotHub</span></span>
* <span data-ttu-id="20708-1810">Har uppdaterats till den senaste versionen av SDK:n lotHub</span><span class="sxs-lookup"><span data-stu-id="20708-1810">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="20708-1811">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="20708-1811">Az.LogicApp</span></span>
* <span data-ttu-id="20708-1812">Get-AzLogicApp visar en lista över alla som inte har angivet namn</span><span class="sxs-lookup"><span data-stu-id="20708-1812">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="20708-1813">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="20708-1813">Az.Resources</span></span>
* <span data-ttu-id="20708-1814">Åtgärdade problem med parameteruppsättningen när parametrarna -ODataQuery och -ResourceId anges för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="20708-1814">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="20708-1815">Mer information här: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="20708-1815">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="20708-1816">Åtgärdade hantering av parametern -Custom i New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="20708-1816">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="20708-1817">Korrigerade stavfel i New-AzDeployment-dokumentationen</span><span class="sxs-lookup"><span data-stu-id="20708-1817">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="20708-1818">Gjorde parametern -MailNickname obligatorisk för New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="20708-1818">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="20708-1819">Mer information här: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="20708-1819">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="20708-1820">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="20708-1820">Az.SignalR</span></span>
* <span data-ttu-id="20708-1821">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="20708-1821">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="20708-1822">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="20708-1822">Az.Sql</span></span>
* <span data-ttu-id="20708-1823">Konverterade lagringshanteringsklientens beroende av den normala SDK-implementeringen.</span><span class="sxs-lookup"><span data-stu-id="20708-1823">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="20708-1824">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="20708-1824">Az.Storage</span></span>
* <span data-ttu-id="20708-1825">Angav StorageAccountName för lagringskontext som det verkliga namnet på lagringskontot när det skapas med Sas Token, OAuth eller Anonymous</span><span class="sxs-lookup"><span data-stu-id="20708-1825">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="20708-1826">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="20708-1826">New-AzStorageContext</span></span>
* <span data-ttu-id="20708-1827">Skapade Sas Token för Blob Snapshot-objekt med parametern -FullUri, åtgärdade den returnerade URI:n så att den blir URI för ögonblicksbild</span><span class="sxs-lookup"><span data-stu-id="20708-1827">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="20708-1828">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="20708-1828">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="20708-1829">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="20708-1829">Az.Websites</span></span>
* <span data-ttu-id="20708-1830">Åtgärdade en bugg i datumparsningen i Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="20708-1830">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="20708-1831">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="20708-1831">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="20708-1832">1.0.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="20708-1832">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="20708-1833">Allmänt</span><span class="sxs-lookup"><span data-stu-id="20708-1833">General</span></span>

- <span data-ttu-id="20708-1834">Allmän tillgänglighet för Az-modulen</span><span class="sxs-lookup"><span data-stu-id="20708-1834">General Availability of Az Module</span></span>
- <span data-ttu-id="20708-1835">Onlinehjälp för varje modul</span><span class="sxs-lookup"><span data-stu-id="20708-1835">Online help for each module</span></span>
- <span data-ttu-id="20708-1836">Mer information och en översikt finns på [Az-informationssidan](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="20708-1836">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="20708-1837">Information om hur du migrerar från AzureRM finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="20708-1837">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="20708-1838">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="20708-1838">Az.Accounts</span></span>
- <span data-ttu-id="20708-1839">Har ändrats från Az.Profile</span><span class="sxs-lookup"><span data-stu-id="20708-1839">Changed from Az.Profile</span></span>
- <span data-ttu-id="20708-1840">Fasta tabellformat för profil- och kontexttyper</span><span class="sxs-lookup"><span data-stu-id="20708-1840">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="20708-1841">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="20708-1841">Az.ApiManagement</span></span>
- <span data-ttu-id="20708-1842">Korrigeringar för #7002</span><span class="sxs-lookup"><span data-stu-id="20708-1842">Fixes for #7002</span></span>
- <span data-ttu-id="20708-1843">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="20708-1843">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="20708-1844">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="20708-1844">Az.Batch</span></span>
- <span data-ttu-id="20708-1845">Lade till möjligheten att se vilken version av Azure Batch Node Agent som körs på var och en av de virtuella datorerna i en pool, via den nya egenskapen `NodeAgentInformation` på `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="20708-1845">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="20708-1846">Standarden `Caching` för `PSDataDisk` är nu `ReadWrite` i stället för `None`.</span><span class="sxs-lookup"><span data-stu-id="20708-1846">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="20708-1847">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="20708-1847">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="20708-1848">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="20708-1848">Az.Billing</span></span>
- <span data-ttu-id="20708-1849">Kombinerar cmdletarna för fakturering, förbrukning och UsageAggregates. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="20708-1849">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="20708-1850">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="20708-1850">Az.CognitivServices</span></span>
- <span data-ttu-id="20708-1851">Lade till kompletterare för SkuName och Typem som är tillgängliga i New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="20708-1851">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="20708-1852">Tog bort parameteruppsättningen GetSkusWithAccountParamSetName från Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="20708-1852">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="20708-1853">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="20708-1853">Az.ContainerInstance</span></span>
- <span data-ttu-id="20708-1854">Stöd för ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="20708-1854">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="20708-1855">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="20708-1855">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="20708-1856">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="20708-1856">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="20708-1857">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="20708-1857">Az.DataLakeStore</span></span>
- <span data-ttu-id="20708-1858">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="20708-1858">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="20708-1859">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="20708-1859">Az.Monitor</span></span>
- <span data-ttu-id="20708-1860">Döpte om Az.Insights till Az.Monitor och andra mindre icke-bakåtkompatibla ändringar. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="20708-1860">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="20708-1861">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="20708-1861">Az.KeyVault</span></span>
- <span data-ttu-id="20708-1862">Tog bort den inaktuella egenskapen PurgeDisabled från utdatatyper</span><span class="sxs-lookup"><span data-stu-id="20708-1862">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="20708-1863">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="20708-1863">Az.MachineLearning</span></span>
- <span data-ttu-id="20708-1864">Inkluderade cmdletarna från modulen Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="20708-1864">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="20708-1865">Az.Media</span><span class="sxs-lookup"><span data-stu-id="20708-1865">Az.Media</span></span>
- <span data-ttu-id="20708-1866">Tog bort inaktuella -Tags-alias från New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="20708-1866">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="20708-1867">Az.Network</span><span class="sxs-lookup"><span data-stu-id="20708-1867">Az.Network</span></span>
<span data-ttu-id="20708-1868">Stöd har lagts till för konfiguration av RewriteRuleSets i Application Gateway</span><span class="sxs-lookup"><span data-stu-id="20708-1868">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="20708-1869">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="20708-1869">New cmdlets added:</span></span>
        - <span data-ttu-id="20708-1870">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="20708-1870">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="20708-1871">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="20708-1871">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="20708-1872">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="20708-1872">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="20708-1873">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="20708-1873">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="20708-1874">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="20708-1874">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="20708-1875">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="20708-1875">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="20708-1876">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="20708-1876">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="20708-1877">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="20708-1877">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="20708-1878">Cmdletar har uppdaterats med den valfria parametern -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="20708-1878">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="20708-1879">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="20708-1879">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="20708-1880">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="20708-1880">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="20708-1881">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="20708-1881">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="20708-1882">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="20708-1882">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="20708-1883">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="20708-1883">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="20708-1884">New-AzureRmApplicationGatewayUrlPathMapConfig har lagt till KeyVault-stöd för Application Gateway med Identity.</span><span class="sxs-lookup"><span data-stu-id="20708-1884">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="20708-1885">Cmdletar har uppdaterats med den valfria parametern -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="20708-1885">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="20708-1886">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="20708-1886">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="20708-1887">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="20708-1887">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="20708-1888">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="20708-1888">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="20708-1889">Cmdleten New-AzApplicationGateway har uppdaterats med den valfria parametern -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="20708-1889">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="20708-1890">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="20708-1890">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="20708-1891">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="20708-1891">Az.OperationalInsights</span></span>
- <span data-ttu-id="20708-1892">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="20708-1892">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="20708-1893">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="20708-1893">Az.Profile</span></span>
- <span data-ttu-id="20708-1894">Modulnamnet har ändrats till Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="20708-1894">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="20708-1895">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="20708-1895">Az.RecoveryServices</span></span>
- <span data-ttu-id="20708-1896">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="20708-1896">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="20708-1897">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="20708-1897">Az.Resources</span></span>
- <span data-ttu-id="20708-1898">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="20708-1898">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="20708-1899">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="20708-1899">Az.ServiceFabric</span></span>
- <span data-ttu-id="20708-1900">Stöd för specificering av certifikat efter eget namn och tumavtryck</span><span class="sxs-lookup"><span data-stu-id="20708-1900">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="20708-1901">Information om fler icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="20708-1901">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="20708-1902">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="20708-1902">Az.SIgnalR</span></span>
- <span data-ttu-id="20708-1903">Allmän tillgänglighet för PowerShell-cmdletar för SIgnalR</span><span class="sxs-lookup"><span data-stu-id="20708-1903">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="20708-1904">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="20708-1904">Az.Sql</span></span>
- <span data-ttu-id="20708-1905">Lade till de nya identifieringstyperna Data_Exfiltration och Unsafe_Action i Threat Detection-cmdletar</span><span class="sxs-lookup"><span data-stu-id="20708-1905">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="20708-1906">Uppdaterade dokumentationsexempel för Sql Auditing-cmdletar</span><span class="sxs-lookup"><span data-stu-id="20708-1906">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="20708-1907">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="20708-1907">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="20708-1908">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="20708-1908">Az.Storage</span></span>
- <span data-ttu-id="20708-1909">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="20708-1909">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="20708-1910">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="20708-1910">Az.Websites</span></span>
- <span data-ttu-id="20708-1911">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="20708-1911">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="20708-1912">0.7.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="20708-1912">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="20708-1913">Allmänt</span><span class="sxs-lookup"><span data-stu-id="20708-1913">General</span></span>

* <span data-ttu-id="20708-1914">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="20708-1914">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="20708-1915">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="20708-1915">Az.Compute</span></span>

* <span data-ttu-id="20708-1916">Lade till stöd för UltraSSD och Galleriavbildningar i de enkla parameteruppsättningarna för `New-AzVm(ss)`-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="20708-1916">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="20708-1917">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="20708-1917">Az.DataLakeStore</span></span>

* <span data-ttu-id="20708-1918">Åtgärdade avslutande snedstreck i domänen för adls-konto</span><span class="sxs-lookup"><span data-stu-id="20708-1918">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="20708-1919">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="20708-1919">Az.FrontDoor</span></span>

* <span data-ttu-id="20708-1920">Brutna länkar korrigerades</span><span class="sxs-lookup"><span data-stu-id="20708-1920">Fixed some broken links</span></span>
    - <span data-ttu-id="20708-1921">I artiklarna New-AzureRmFrontDoor och Set-AzureRmFrontDoor artiklar korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="20708-1921">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="20708-1922">I artikeln New-AzureRmFrontDoorManagedRuleObject korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="20708-1922">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="20708-1923">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="20708-1923">Az.RecoveryServices</span></span>

* <span data-ttu-id="20708-1924">Lade till valideringar på klientsidan för Azure-filresurs med återställningsåtgärder.</span><span class="sxs-lookup"><span data-stu-id="20708-1924">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="20708-1925">Gjorde storageAccountName och storageAccountResourceGroupName valfritt för afs-återställning.</span><span class="sxs-lookup"><span data-stu-id="20708-1925">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="20708-1926">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="20708-1926">Az.Resources</span></span>

* <span data-ttu-id="20708-1927">Korrigering för https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="20708-1927">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="20708-1928">Uppdaterade Get-AzureRmRoleAssignment så att prenumerationsomfattningen används om den anges vid begäran om klassiska administratörer.</span><span class="sxs-lookup"><span data-stu-id="20708-1928">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="20708-1929">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="20708-1929">Az.Sql</span></span>

* <span data-ttu-id="20708-1930">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="20708-1930">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="20708-1931">Korrigerade ett problem med Get-AzureRmSqlDatabaseVulnerabilityAssessment med DotNet-kärna</span><span class="sxs-lookup"><span data-stu-id="20708-1931">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="20708-1932">Ändrade dokumentationen för hjälpmeddelanden som rör SQL Auditing-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="20708-1932">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="20708-1933">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="20708-1933">Az.Storage</span></span>

* <span data-ttu-id="20708-1934">Lade till -EnableHierarchicalNamespace i New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="20708-1934">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="20708-1935">Åtgärdade problemet med att cmdleten Copy File inte kunde återanvända källkontexten på målet om inte -DestContext angetts</span><span class="sxs-lookup"><span data-stu-id="20708-1935">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="20708-1936">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="20708-1936">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="20708-1937">Stöd för statisk webbplatskonfiguration</span><span class="sxs-lookup"><span data-stu-id="20708-1937">Support Static Website configuration</span></span>
    - <span data-ttu-id="20708-1938">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="20708-1938">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="20708-1939">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="20708-1939">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="20708-1940">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="20708-1940">Az.Websites</span></span>

* <span data-ttu-id="20708-1941">Set-AzureRmWebApp och Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="20708-1941">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="20708-1942">Ny parameter (-AzureStoragePath) har lagts till för att ange att Azure Storage-sökvägar ska monteras i containerappar i Windows och Linux.</span><span class="sxs-lookup"><span data-stu-id="20708-1942">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="20708-1943">Använder utdata från den nya cmdleten New-AzureRmWebAppAzureStoragePath som en parameter för att ange sökvägar för Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="20708-1943">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="20708-1944">0.6.1 – november 2018</span><span class="sxs-lookup"><span data-stu-id="20708-1944">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="20708-1945">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="20708-1945">Az.ApiManagement</span></span>
* <span data-ttu-id="20708-1946">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="20708-1946">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="20708-1947">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="20708-1947">Az.Automation</span></span>
* <span data-ttu-id="20708-1948">Swagger baserade Azure Automation-cmdletar</span><span class="sxs-lookup"><span data-stu-id="20708-1948">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="20708-1949">Cmdletar för Uppdateringshantering har lagts till</span><span class="sxs-lookup"><span data-stu-id="20708-1949">Added Update Management cmdlets</span></span>
* <span data-ttu-id="20708-1950">Cmdletar för källkontroll har lagts till</span><span class="sxs-lookup"><span data-stu-id="20708-1950">Added Source Control cmdlets</span></span>
* <span data-ttu-id="20708-1951">Remove-AzureRmAutomationHybridWorkerGroup-cmdlet har lagts till</span><span class="sxs-lookup"><span data-stu-id="20708-1951">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="20708-1952">Kommandot för DSC-registreringsnod har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="20708-1952">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="20708-1953">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="20708-1953">Az.Compute</span></span>
* <span data-ttu-id="20708-1954">Problem med SystemAssigned-identitet har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="20708-1954">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="20708-1955">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="20708-1955">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="20708-1956">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="20708-1956">Az.ContainerInstance</span></span>
* <span data-ttu-id="20708-1957">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="20708-1957">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="20708-1958">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="20708-1958">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="20708-1959">uppdatera exempelbeskrivningen för marketplace-cmdletar</span><span class="sxs-lookup"><span data-stu-id="20708-1959">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="20708-1960">Az.Network</span><span class="sxs-lookup"><span data-stu-id="20708-1960">Az.Network</span></span>
* <span data-ttu-id="20708-1961">Cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomErreller Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="20708-1961">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="20708-1962">ICMP tillbaka till stöd för Azure Firewall-nätverksprotokoll har lagts till</span><span class="sxs-lookup"><span data-stu-id="20708-1962">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="20708-1963">Uppdatera cmdlet Test-AzureRmNetworkWatcherConnectivity, lägga till verifiering av mål-id, adress och port.</span><span class="sxs-lookup"><span data-stu-id="20708-1963">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="20708-1964">Åtgärda problem med minnesanvändning i VirtualNetwork-karta</span><span class="sxs-lookup"><span data-stu-id="20708-1964">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="20708-1965">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="20708-1965">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="20708-1966">Åtgärda för att ändra principen för en skyddad fildelning.</span><span class="sxs-lookup"><span data-stu-id="20708-1966">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="20708-1967">Tidszonsprincipen har konverterats till versaler.</span><span class="sxs-lookup"><span data-stu-id="20708-1967">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="20708-1968">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="20708-1968">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="20708-1969">Exempel i New-AzureRmRecoveryServicesAsrProtectableItem har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="20708-1969">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="20708-1970">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="20708-1970">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="20708-1971">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="20708-1971">Az.Relay</span></span>
* <span data-ttu-id="20708-1972">Valfri parameter -KeyValue till New-AzureRmRelayKey cmdlet har lagts till, vilket gör det möjligt för användare att tillhandahålla KeyValue.</span><span class="sxs-lookup"><span data-stu-id="20708-1972">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="20708-1973">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="20708-1973">Az.Resources</span></span>
* <span data-ttu-id="20708-1974">Uppdatera hjälpdokumentation för resursidentitet kopplad till parametrar i `New-AzureRmPolicyAssignment` och `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="20708-1974">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="20708-1975">Lägg till ett exempel för New-AzureRmPolicyDefinition som använder -Metadata</span><span class="sxs-lookup"><span data-stu-id="20708-1975">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="20708-1976">Korrigera så att skiftläge behålls i taggnycklar i NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="20708-1976">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="20708-1977">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="20708-1977">Az.ServiceFabric</span></span>
* <span data-ttu-id="20708-1978">Lägg till utfasningsmeddelanden för kommande icke-kompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="20708-1978">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="20708-1979">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="20708-1979">Az.Sql</span></span>
* <span data-ttu-id="20708-1980">Nya cmdletar för CRUD-åtgärder på Azure Sql Database-hanterad instans och Azure Sql-hanterad databas</span><span class="sxs-lookup"><span data-stu-id="20708-1980">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="20708-1981">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="20708-1981">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="20708-1982">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="20708-1982">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="20708-1983">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="20708-1983">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="20708-1984">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="20708-1984">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="20708-1985">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="20708-1985">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="20708-1986">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="20708-1986">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="20708-1987">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="20708-1987">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="20708-1988">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="20708-1988">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="20708-1989">Hantering av utökad granskningsprincip på en server eller en databas har aktiverats.</span><span class="sxs-lookup"><span data-stu-id="20708-1989">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="20708-1990">Ny parameter (PredicateExpression) har lagts till för att aktivera filtrering av granskningsloggar.</span><span class="sxs-lookup"><span data-stu-id="20708-1990">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="20708-1991">Cmdletar har ändrats så att de använder SQL-klienter i stället för äldre klienter.</span><span class="sxs-lookup"><span data-stu-id="20708-1991">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="20708-1992">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="20708-1992">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="20708-1993">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="20708-1993">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="20708-1994">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="20708-1994">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="20708-1995">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="20708-1995">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="20708-1996">Problem med att använda Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings med lagringskontots namnparameter har korrigerats</span><span class="sxs-lookup"><span data-stu-id="20708-1996">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="20708-1997">0.5.0 – november 2018</span><span class="sxs-lookup"><span data-stu-id="20708-1997">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="20708-1998">Allmänt</span><span class="sxs-lookup"><span data-stu-id="20708-1998">General</span></span>
* <span data-ttu-id="20708-1999">Lade till resurskompletterare till många kärn-cmdletar – dessa gör att du kan stega genom befintliga resursnamn med TABB vid interaktiva anrop till cmdletar</span><span class="sxs-lookup"><span data-stu-id="20708-1999">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="20708-2000">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="20708-2000">Az.Profile</span></span>
* <span data-ttu-id="20708-2001">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="20708-2001">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="20708-2002">Bytte namn på parametern TenantId i cmdleten Connect-AzAccount till Tenant och lade till ett alias för TenantId</span><span class="sxs-lookup"><span data-stu-id="20708-2002">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="20708-2003">Uppdaterade TenantId-beskrivningen för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="20708-2003">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="20708-2004">Åtgärda felmeddelande för misslyckad inloggning när du tillhandahåller klientdomän</span><span class="sxs-lookup"><span data-stu-id="20708-2004">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="20708-2005">Åtgärda problem med att kontextnamn hamnar i konflikt för konton utan prenumerationer i klientorganisationen</span><span class="sxs-lookup"><span data-stu-id="20708-2005">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="20708-2006">Åtgärda problem med DataLake-slutpunkter vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="20708-2006">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="20708-2007">Åtgärdade problem med att Disconnect-AzAccount kastades om den inte anslöts</span><span class="sxs-lookup"><span data-stu-id="20708-2007">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="20708-2008">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="20708-2008">Az.CognitiveServices</span></span>
* <span data-ttu-id="20708-2009">Lade till åtgärden Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="20708-2009">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="20708-2010">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="20708-2010">Az.Compute</span></span>
* <span data-ttu-id="20708-2011">Lade till cmdletarna Add-AzVmssVMDataDisk och Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="20708-2011">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="20708-2012">Get-AzVMImage visar AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="20708-2012">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="20708-2013">Åtgärdade att värdena för alternativen SetAzVMChefExtension -BootstrapOptions och -JsonAttribute inte angavs i json-format.</span><span class="sxs-lookup"><span data-stu-id="20708-2013">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="20708-2014">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="20708-2014">Az.DataLakeStore</span></span>
* <span data-ttu-id="20708-2015">Uppdatera DataLake-paketet till 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="20708-2015">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="20708-2016">Lägg till standardsamtidighet för flertrådade åtgärder.</span><span class="sxs-lookup"><span data-stu-id="20708-2016">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="20708-2017">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="20708-2017">Az.Insights</span></span>
* <span data-ttu-id="20708-2018">Åtgärdade problem #7267 (autoskalningsområde)</span><span class="sxs-lookup"><span data-stu-id="20708-2018">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="20708-2019">Problem med att uppräknade parametrar inte ställdes in ordentligt när du skapade en ny autoskalningsregel (de ställdes alltid in med standardvärdet).</span><span class="sxs-lookup"><span data-stu-id="20708-2019">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="20708-2020">Åtgärdade problem #7513 [Insights] Set-AzDiagnosticSetting kräver uttrycklig specifikation av kategorier när inställningar skapas</span><span class="sxs-lookup"><span data-stu-id="20708-2020">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="20708-2021">Nu kräver inte cmdleten uttrycklig anvisning av kategorierna för att aktiveras under skapande, d.v.s. den fungerar enligt beskrivning</span><span class="sxs-lookup"><span data-stu-id="20708-2021">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="20708-2022">Az.Network</span><span class="sxs-lookup"><span data-stu-id="20708-2022">Az.Network</span></span>
* <span data-ttu-id="20708-2023">PeeringType ändrades till en obligatorisk parameter för följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="20708-2023">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="20708-2024">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="20708-2024">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="20708-2025">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="20708-2025">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="20708-2026">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="20708-2026">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="20708-2027">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="20708-2027">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="20708-2028">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="20708-2028">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="20708-2029">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="20708-2029">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="20708-2030">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="20708-2030">Az.PolicyInsights</span></span>
* <span data-ttu-id="20708-2031">Cmdletar för principreparation har lagts till</span><span class="sxs-lookup"><span data-stu-id="20708-2031">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="20708-2032">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="20708-2032">Az.Resources</span></span>
* <span data-ttu-id="20708-2033">Korrigering för https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="20708-2033">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="20708-2034">Tillåt att resurser listas med parametern -ResourceId för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="20708-2034">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="20708-2035">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="20708-2035">Az.ServiceBus</span></span>
* <span data-ttu-id="20708-2036">Skrivskyddad MigrationState-egenskap har lagts till i PSServiceBusMigrationConfigurationAttributes, som hjälper till att hålla koll på migreringstillståndet.</span><span class="sxs-lookup"><span data-stu-id="20708-2036">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="20708-2037">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="20708-2037">Az.ServiceFabric</span></span>
* <span data-ttu-id="20708-2038">Åtgärda att lägga till certifikat till Linux-Vmss.</span><span class="sxs-lookup"><span data-stu-id="20708-2038">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="20708-2039">Åtgärdade Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="20708-2039">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="20708-2040">Använd rätt tumavtryck från nya certifikat (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="20708-2040">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="20708-2041">Visa undantag korrekt (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="20708-2041">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="20708-2042">Åtgärdade Update-AzServiceFabricDurability så att klusterkonfigurationen uppdateras innan Vmss-åtgärden CreateOrUpdate påbörjas.</span><span class="sxs-lookup"><span data-stu-id="20708-2042">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="20708-2043">0.4.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="20708-2043">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="20708-2044">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="20708-2044">Az.Profile</span></span>
* <span data-ttu-id="20708-2045">Åtgärdade problemet med Get-AzSubscription i CloudShell</span><span class="sxs-lookup"><span data-stu-id="20708-2045">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="20708-2046">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="20708-2046">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="20708-2047">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="20708-2047">Az.Compute</span></span>
* <span data-ttu-id="20708-2048">Nya storlekar lades till i listan över godkända VM-storlekar för vilka accelererat nätverk kommer att aktiveras vid användning av den enkla parameteruppsättningen för New-AzVm</span><span class="sxs-lookup"><span data-stu-id="20708-2048">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="20708-2049">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="20708-2049">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="20708-2050">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="20708-2050">Az.DataLakeStore</span></span>
* <span data-ttu-id="20708-2051">Lägger till stöd för regler för virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="20708-2051">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="20708-2052">Get-AzDataLakeStoreVirtualNetworkRule: Hämtar eller listar regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="20708-2052">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="20708-2053">Add-AzDataLakeStoreVirtualNetworkRule: Lägger till en regel för virtuellt nätverk i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="20708-2053">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="20708-2054">Set-AzDataLakeStoreVirtualNetworkRule: Ändrar den angivna regeln för virtuellt nätverk i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="20708-2054">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="20708-2055">Remove-AzDataLakeStoreVirtualNetworkRule: Tar bort en regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="20708-2055">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="20708-2056">Az.Network</span><span class="sxs-lookup"><span data-stu-id="20708-2056">Az.Network</span></span>
* <span data-ttu-id="20708-2057">Skicka protokollvärdet till serverdelen för att uppdatera cmdleten Test-AzNetworkWatcherConnectivity.</span><span class="sxs-lookup"><span data-stu-id="20708-2057">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="20708-2058">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="20708-2058">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="20708-2059">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="20708-2059">Az.Resources</span></span>
* <span data-ttu-id="20708-2060">Åtgärdade problem där Get-AzRoleDefinition genererar ett oläsligt undantag (när standardprofilen inte innehåller någon prenumeration och ingen omfattning har angetts) genom att lägga till ett beskrivande undantag i scenariot.</span><span class="sxs-lookup"><span data-stu-id="20708-2060">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="20708-2061">Ställ in ”RoleDefinitionNameParameterSet” som standardparameteruppsättning.</span><span class="sxs-lookup"><span data-stu-id="20708-2061">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="20708-2062">0.3.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="20708-2062">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="20708-2063">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="20708-2063">Azure.Storage</span></span>
* <span data-ttu-id="20708-2064">Åtgärda fel där Kopiera blob/fil inte kopierar metadata när målplatsen har ett problem med metadata</span><span class="sxs-lookup"><span data-stu-id="20708-2064">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="20708-2065">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="20708-2065">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="20708-2066">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="20708-2066">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="20708-2067">Stöd för att hämta användningsinformation om en Storage-resurs för en specifik plats och för att lägga till ett varningsmeddelande för att hämta användningsinformation om en global Storage-resurs är inaktuellt.</span><span class="sxs-lookup"><span data-stu-id="20708-2067">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="20708-2068">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="20708-2068">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="20708-2069">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="20708-2069">Az.CognitiveServices</span></span>
* <span data-ttu-id="20708-2070">Stöd för Get-AzCognitiveServicesAccountSkus utan ett befintligt konto.</span><span class="sxs-lookup"><span data-stu-id="20708-2070">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="20708-2071">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="20708-2071">Az.Compute</span></span>
* <span data-ttu-id="20708-2072">Åtgärdade fel där Get-AzVM -ResourceGroupName <rg> returnerar fler än 50 resultat om det behövs</span><span class="sxs-lookup"><span data-stu-id="20708-2072">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="20708-2073">Lade till ett exempel för SimpleParameterSet i hjälpen för cmdleten New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="20708-2073">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="20708-2074">Ett stavfel i förloppsmeddelandet för Azure Disk Encryption har korrigerats</span><span class="sxs-lookup"><span data-stu-id="20708-2074">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="20708-2075">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="20708-2075">Az.DataFactoryV2</span></span>
* <span data-ttu-id="20708-2076">ADF .Net SDK-versionen har uppdaterats till 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="20708-2076">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="20708-2077">Az.Network</span><span class="sxs-lookup"><span data-stu-id="20708-2077">Az.Network</span></span>
* <span data-ttu-id="20708-2078">Funktionalitet för NetworkProfile har lagts till.</span><span class="sxs-lookup"><span data-stu-id="20708-2078">Added NetworkProfile functionality.</span></span> <span data-ttu-id="20708-2079">nya cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="20708-2079">new cmdlets added</span></span>
    - <span data-ttu-id="20708-2080">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="20708-2080">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="20708-2081">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="20708-2081">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="20708-2082">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="20708-2082">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="20708-2083">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="20708-2083">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="20708-2084">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="20708-2084">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="20708-2085">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="20708-2085">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="20708-2086">Länk för tjänstassociering på modell för undernät har lagts till</span><span class="sxs-lookup"><span data-stu-id="20708-2086">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="20708-2087">Cmdletarna New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap och Remove-AzVirtualNetworkTap har lagts till</span><span class="sxs-lookup"><span data-stu-id="20708-2087">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="20708-2088">Cmdletarna Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig och Remove-AzNEtworkInterfaceTapConfig har lagts till</span><span class="sxs-lookup"><span data-stu-id="20708-2088">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="20708-2089">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="20708-2089">Az.RedisCache</span></span>
* <span data-ttu-id="20708-2090">Tillåt att alla strängar används som storleksparametrar framöver.</span><span class="sxs-lookup"><span data-stu-id="20708-2090">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="20708-2091">Lägg till P5 i popup-fönstret PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="20708-2091">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="20708-2092">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="20708-2092">Az.Resources</span></span>
* <span data-ttu-id="20708-2093">Parametern -Mode som saknades i Set-AzPolicyDefinition har lagts till</span><span class="sxs-lookup"><span data-stu-id="20708-2093">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="20708-2094">Åtgärdade buggen för cmdleten Get-AzProviderOperation för åtgärder med ursprung som innehåller användare</span><span class="sxs-lookup"><span data-stu-id="20708-2094">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="20708-2095">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="20708-2095">Az.Sql</span></span>
* <span data-ttu-id="20708-2096">Ett problem där vissa cmdletar för säkerhetskopiering inte kunde identifiera den aktuella azure-prenumerationen har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="20708-2096">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="20708-2097">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="20708-2097">Az.Websites</span></span>
* <span data-ttu-id="20708-2098">Ny cmdlet: Get-AzWebAppContainerContinuousDeploymentUrl – Hämtar webhook-URL:en för kontinuerlig distribution av container</span><span class="sxs-lookup"><span data-stu-id="20708-2098">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="20708-2099">Nya cmdletar: New-AzWebAppContainerPSSession och Enter-WebAppContainerPSSession – Startar en PowerShell-fjärrsession i en containerapp för windows</span><span class="sxs-lookup"><span data-stu-id="20708-2099">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="20708-2100">0.2.0 – september 2018</span><span class="sxs-lookup"><span data-stu-id="20708-2100">0.2.0 - September 2018</span></span>
 <span data-ttu-id="20708-2101">Första versionen</span><span class="sxs-lookup"><span data-stu-id="20708-2101">Initial Release</span></span>
