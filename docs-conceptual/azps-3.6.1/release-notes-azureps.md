---
title: Viktig information om Azure PowerShell
description: Lär dig mer om alla de senaste uppdateringarna för Azure PowerShell-modulerna.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.openlocfilehash: f24e5ef66f9c49976c550c9847903bd0608c5123
ms.sourcegitcommit: f6fa6543be1e0f6330b1598f01528b2928cc426c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/11/2020
ms.locfileid: "79111041"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="2d45d-103">Viktig information om Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="2d45d-103">Azure PowerShell release notes</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="2d45d-104">3.6.1 – mars 2020</span><span class="sxs-lookup"><span data-stu-id="2d45d-104">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2d45d-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d45d-105">Az.Accounts</span></span>
* <span data-ttu-id="2d45d-106">Öppna sidan med Azure PowerShell-enkäten i ”Send-Feedback” [#11020]</span><span class="sxs-lookup"><span data-stu-id="2d45d-106">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="2d45d-107">Visa URL:en för Azure PowerShell-enkäten i ”Resolve-Error” [#11021]</span><span class="sxs-lookup"><span data-stu-id="2d45d-107">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="2d45d-108">Az-version har lagts till i UserAgent</span><span class="sxs-lookup"><span data-stu-id="2d45d-108">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="2d45d-109">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2d45d-109">Az.ApiManagement</span></span>
* <span data-ttu-id="2d45d-110">Stöd har lagts till för att hämta och konfigurera en anpassad domän på DeveloperPortal-slutpunkten [#11007]</span><span class="sxs-lookup"><span data-stu-id="2d45d-110">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="2d45d-111">”Export-AzApiManagementApi” Stöd har lagts till för att ladda ned API-definition i Json-format [#9987]</span><span class="sxs-lookup"><span data-stu-id="2d45d-111">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="2d45d-112">”Import-AzApiManagementApi” Stöd har lagts till för att importera OpenApi 3.0-definition från Json-dokument</span><span class="sxs-lookup"><span data-stu-id="2d45d-112">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="2d45d-113">”New-AzApiManagementIdentityProvider” och ”Set-AzApiManagementIdentityProvider” Stöd har lagts till för att konfigurera ”Signin Tenant” för AAD B2C-provider [#9784]</span><span class="sxs-lookup"><span data-stu-id="2d45d-113">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2d45d-114">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2d45d-114">Az.DataLakeStore</span></span>
* <span data-ttu-id="2d45d-115">En referens har uttryckligen lagts till för System.Buffers i csproj och psd1.</span><span class="sxs-lookup"><span data-stu-id="2d45d-115">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="2d45d-116">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="2d45d-116">Az.IotHub</span></span>
* <span data-ttu-id="2d45d-117">Lade till stöd för att hantera enheter i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="2d45d-117">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="2d45d-118">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="2d45d-118">New Cmdlets are:</span></span>
    - <span data-ttu-id="2d45d-119">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="2d45d-119">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="2d45d-120">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="2d45d-120">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="2d45d-121">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="2d45d-121">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="2d45d-122">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="2d45d-122">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="2d45d-123">Stöd har lagts till för att hantera moduler på en mål-IoT-enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="2d45d-123">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="2d45d-124">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="2d45d-124">New Cmdlets are:</span></span>
    - <span data-ttu-id="2d45d-125">”Add-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="2d45d-125">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="2d45d-126">”Get-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="2d45d-126">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="2d45d-127">”Remove-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="2d45d-127">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="2d45d-128">”Set-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="2d45d-128">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="2d45d-129">Cmdlet har lagts till för att hämta anslutningssträngen för en mål-IoT-enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="2d45d-129">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="2d45d-130">Cmdlet har lagts till för att hämta anslutningssträngen för en modul på en mål-IoT-enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="2d45d-130">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="2d45d-131">Stöd har lagts till för att hämta/ange en överordnad enhet för en IoT-enhet.</span><span class="sxs-lookup"><span data-stu-id="2d45d-131">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="2d45d-132">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="2d45d-132">New Cmdlets are:</span></span>
    - <span data-ttu-id="2d45d-133">”Get-AzIotHubDeviceParent”</span><span class="sxs-lookup"><span data-stu-id="2d45d-133">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="2d45d-134">”Set-AzIotHubDeviceParent”</span><span class="sxs-lookup"><span data-stu-id="2d45d-134">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="2d45d-135">Stöd har lagts till för att hantera en enhets överordnade och underordnade relationer.</span><span class="sxs-lookup"><span data-stu-id="2d45d-135">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2d45d-136">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2d45d-136">Az.Monitor</span></span>
* <span data-ttu-id="2d45d-137">Utdatavärdet har åtgärdats för ”Get-AzMetricDefinition” [#9714]</span><span class="sxs-lookup"><span data-stu-id="2d45d-137">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d45d-138">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d45d-138">Az.Network</span></span>
* <span data-ttu-id="2d45d-139">SQL Management SDK har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="2d45d-139">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="2d45d-140">Ett problem har åtgärdats med namngivningsskillnader i klassen PrivateLinkServiceConnectionState.</span><span class="sxs-lookup"><span data-stu-id="2d45d-140">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="2d45d-141">Fältet ActionsRequired mappar till ActionRequired.</span><span class="sxs-lookup"><span data-stu-id="2d45d-141">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="2d45d-142">PublicNetworkAccess har lagts till i ”New-AzSqlServer” och ”Set-AzSqlServer”</span><span class="sxs-lookup"><span data-stu-id="2d45d-142">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d45d-143">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d45d-143">Az.Resources</span></span>
* <span data-ttu-id="2d45d-144">Null-referensfel har åtgärdats i ”Get-AzRoleAssignment”</span><span class="sxs-lookup"><span data-stu-id="2d45d-144">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="2d45d-145">Växlarna ”-Force” och ”-PassThru” är valfria i ”Remove-AzADGroup” [#10849]</span><span class="sxs-lookup"><span data-stu-id="2d45d-145">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="2d45d-146">Ett problem har åtgärdats som gjorde att ”MailNickname” inte returnerades i ”Remove-AzADGroup” [#11167]</span><span class="sxs-lookup"><span data-stu-id="2d45d-146">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="2d45d-147">Ett problem har åtgärdats som gjorde att pipe-åtgärden ”Remove-AzADGroup” inte fungerar [#11171]</span><span class="sxs-lookup"><span data-stu-id="2d45d-147">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="2d45d-148">Ett null-referensfel har åtgärdats i GetAzureRoleAssignmentCommand</span><span class="sxs-lookup"><span data-stu-id="2d45d-148">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="2d45d-149">Attribut för icke-bakåtkompatibla ändringar har lagts till för kommande ändringar i cmdlets för principer</span><span class="sxs-lookup"><span data-stu-id="2d45d-149">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="2d45d-150">”Get-AzResourceGroup” har uppdaterats för att utföra taggfiltrering för resursgrupper på serversidan</span><span class="sxs-lookup"><span data-stu-id="2d45d-150">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="2d45d-151">Utökade Tag-cmdlets stöder -ResourceId</span><span class="sxs-lookup"><span data-stu-id="2d45d-151">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="2d45d-152">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="2d45d-152">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="2d45d-153">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="2d45d-153">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="2d45d-154">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="2d45d-154">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="2d45d-155">Ny Tag-cmdlet har lagts till</span><span class="sxs-lookup"><span data-stu-id="2d45d-155">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="2d45d-156">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="2d45d-156">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="2d45d-157">Flyttade ScopedDeployment från SDK 3.3.0</span><span class="sxs-lookup"><span data-stu-id="2d45d-157">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d45d-158">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d45d-158">Az.Sql</span></span>
* <span data-ttu-id="2d45d-159">PublicNetworkAccess har lagts till i ”New-AzSqlServer” och ”Set-AzSqlServer”</span><span class="sxs-lookup"><span data-stu-id="2d45d-159">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="2d45d-160">Stöd har lagts till för konfiguration av säkerhetskopiering för långsiktig kvarhållning för hanterade databaser</span><span class="sxs-lookup"><span data-stu-id="2d45d-160">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="2d45d-161">Hämta/ange LTR-princip på en hanterad databas</span><span class="sxs-lookup"><span data-stu-id="2d45d-161">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="2d45d-162">Hämta LTR-säkerhetskopior efter hanterad databas, hanterad instans eller plats</span><span class="sxs-lookup"><span data-stu-id="2d45d-162">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="2d45d-163">Ta bort en LTR-säkerhetskopia</span><span class="sxs-lookup"><span data-stu-id="2d45d-163">Remove an LTR backup</span></span>
    - <span data-ttu-id="2d45d-164">Återställa en LTR-säkerhetskopia för att skapa en ny hanterad databas</span><span class="sxs-lookup"><span data-stu-id="2d45d-164">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="2d45d-165">MinimalTlsVersion har lagts till för New-AzSqlServer och Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="2d45d-165">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="2d45d-166">MinimalTlsVersion har lagts till för New-AzSqlInstance och Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="2d45d-166">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="2d45d-167">SQL SDK-versionen för Az.Network har ändrats</span><span class="sxs-lookup"><span data-stu-id="2d45d-167">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2d45d-168">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d45d-168">Az.Storage</span></span>
* <span data-ttu-id="2d45d-169">AllowProtectedAppendWrite stöds i ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="2d45d-169">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="2d45d-170">”Set-AzRmStorageContainerImmutabilityPolicy”</span><span class="sxs-lookup"><span data-stu-id="2d45d-170">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="2d45d-171">Varningsmeddelande har lagts till om icke-bakåtkompatibel ändring för ändring av typen AzureStorageTable i en senare version</span><span class="sxs-lookup"><span data-stu-id="2d45d-171">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="2d45d-172">”New-AzStorageTable”</span><span class="sxs-lookup"><span data-stu-id="2d45d-172">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="2d45d-173">”Get-AzStorageTable”</span><span class="sxs-lookup"><span data-stu-id="2d45d-173">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2d45d-174">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2d45d-174">Az.Websites</span></span>
* <span data-ttu-id="2d45d-175">Tag-parametern har lagts till för ”New-AzAppServicePlan” och ”Set-AzAppServicePlan”</span><span class="sxs-lookup"><span data-stu-id="2d45d-175">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="2d45d-176">Stoppa cmdlet-körning om ett undantag uppstår när en anpassad domän läggs till på en webbplats</span><span class="sxs-lookup"><span data-stu-id="2d45d-176">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="2d45d-177">Stöd har lagts till för att utföra åtgärder för App Services som inte tillhör samma resursgrupp som App Services-planen</span><span class="sxs-lookup"><span data-stu-id="2d45d-177">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="2d45d-178">Åtkomstbegränsning har tillämpats på WebApp/Function i olika resursgrupper</span><span class="sxs-lookup"><span data-stu-id="2d45d-178">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="2d45d-179">Ett problem har åtgärdats för att ange anpassade värdnamn för WebAppSlots</span><span class="sxs-lookup"><span data-stu-id="2d45d-179">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="2d45d-180">3.5.0 – februari 2020</span><span class="sxs-lookup"><span data-stu-id="2d45d-180">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="2d45d-181">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="2d45d-181">Highlights since the last major release</span></span>
* <span data-ttu-id="2d45d-182">Uppdaterade telemetri på klientsidan.</span><span class="sxs-lookup"><span data-stu-id="2d45d-182">Updated client side telemetry.</span></span>
* <span data-ttu-id="2d45d-183">Az.IotHub lade till cmdletar som stöd för att hantera enheter.</span><span class="sxs-lookup"><span data-stu-id="2d45d-183">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="2d45d-184">Az.SqlVirtualMachine lade till cmdletar för lyssningsfunktion för tillgänglighetsgrupp.</span><span class="sxs-lookup"><span data-stu-id="2d45d-184">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="2d45d-185">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d45d-185">Az.Accounts</span></span>
* <span data-ttu-id="2d45d-186">Lade till SubscriptionId, TenantId och körningstid i data för telemetri på klientsidan</span><span class="sxs-lookup"><span data-stu-id="2d45d-186">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2d45d-187">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2d45d-187">Az.Automation</span></span>
* <span data-ttu-id="2d45d-188">Åtgärdade skrivfel i exempel 1 i referensdokumentation för ”New-AzAutomationSoftwareUpdateConfiguration”</span><span class="sxs-lookup"><span data-stu-id="2d45d-188">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="2d45d-189">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="2d45d-189">Az.CognitiveServices</span></span>
* <span data-ttu-id="2d45d-190">Uppdaterade SDK till 7.0</span><span class="sxs-lookup"><span data-stu-id="2d45d-190">Updated SDK to 7.0</span></span>
* <span data-ttu-id="2d45d-191">Förbättrade felmeddelande vid serversvar om tom brödtext</span><span class="sxs-lookup"><span data-stu-id="2d45d-191">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d45d-192">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d45d-192">Az.Compute</span></span>
* <span data-ttu-id="2d45d-193">Tillät tomt värde för ProximityPlacementGroupId under uppdatering</span><span class="sxs-lookup"><span data-stu-id="2d45d-193">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="2d45d-194">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="2d45d-194">Az.FrontDoor</span></span>
* <span data-ttu-id="2d45d-195">Lade till cmdlet för att hämta hanterade regeldefinitioner som kan användas i WAF</span><span class="sxs-lookup"><span data-stu-id="2d45d-195">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="2d45d-196">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="2d45d-196">Az.IotHub</span></span>
* <span data-ttu-id="2d45d-197">Lade till stöd för att hantera enheter i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="2d45d-197">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="2d45d-198">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="2d45d-198">New Cmdlets are:</span></span>
    - <span data-ttu-id="2d45d-199">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="2d45d-199">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="2d45d-200">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="2d45d-200">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="2d45d-201">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="2d45d-201">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="2d45d-202">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="2d45d-202">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="2d45d-203">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2d45d-203">Az.KeyVault</span></span>
* <span data-ttu-id="2d45d-204">Åtgärdade duplicerad text för Add-AzKeyVaultKey.md</span><span class="sxs-lookup"><span data-stu-id="2d45d-204">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2d45d-205">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2d45d-205">Az.Monitor</span></span>
* <span data-ttu-id="2d45d-206">Åtgärdade beskrivning av cmdleten Get-AzLog.</span><span class="sxs-lookup"><span data-stu-id="2d45d-206">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="2d45d-207">En ny parameter med namnet ActionGroupId har lagts till i kommandot ”New-AzMetricAlertRuleV2”.</span><span class="sxs-lookup"><span data-stu-id="2d45d-207">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="2d45d-208">Användaren kan ange ActionGroupId(string) eller ActionGroup(ActivityLogAlertActionGroup).</span><span class="sxs-lookup"><span data-stu-id="2d45d-208">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d45d-209">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d45d-209">Az.Network</span></span>
* <span data-ttu-id="2d45d-210">Lade till en extra parameteranteckning för parametern ”-EnableProxyProtocol” för cmdleten ”New-AzPrivateLinkService”.</span><span class="sxs-lookup"><span data-stu-id="2d45d-210">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="2d45d-211">Åtgärdade FilterData-exempel i Start-AzVirtualNetworkGatewayConnectionPacketCapture.md och Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="2d45d-211">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="2d45d-212">Lade till paketinsamlingsexempel för att samla in alla inre och yttre paket i Start-AzVirtualNetworkGatewayConnectionPacketCapture.md och Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="2d45d-212">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="2d45d-213">Lade till stöd för Azure-brandväggsprincip på VNet-brandväggar</span><span class="sxs-lookup"><span data-stu-id="2d45d-213">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="2d45d-214">Inga nya cmdletar har lagts till.</span><span class="sxs-lookup"><span data-stu-id="2d45d-214">No new cmdlets are added.</span></span> <span data-ttu-id="2d45d-215">Lättar begränsningen för brandväggsprincip på VNet-brandväggar</span><span class="sxs-lookup"><span data-stu-id="2d45d-215">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2d45d-216">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d45d-216">Az.RecoveryServices</span></span>
* <span data-ttu-id="2d45d-217">Lade till stöd för Restore-as-files för SQL-databaser.</span><span class="sxs-lookup"><span data-stu-id="2d45d-217">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d45d-218">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d45d-218">Az.Resources</span></span>
* <span data-ttu-id="2d45d-219">Omstrukturerade cmdletar för malldistribution</span><span class="sxs-lookup"><span data-stu-id="2d45d-219">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="2d45d-220">Lade till nya cmdletar för att hantera distributioner i hanteringsgruppen: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="2d45d-220">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="2d45d-221">Lade till nya cmdletar för att hantera distributioner i klientorganisationsområdet: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="2d45d-221">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="2d45d-222">Omstrukturerade \*-AzDeployment-cmdletar för att fungera specifikt i prenumerationsomfattningen</span><span class="sxs-lookup"><span data-stu-id="2d45d-222">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="2d45d-223">Skapade alias \*-AzSubscriptionDeployment för \*-AzDeployment-cmdletar</span><span class="sxs-lookup"><span data-stu-id="2d45d-223">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="2d45d-224">Åtgärdade ”Update-AzADApplication” när parametern ”AvailableToOtherTenants” inte har angetts</span><span class="sxs-lookup"><span data-stu-id="2d45d-224">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="2d45d-225">Tog bort ApplicationObjectWithoutCredentialParameterSet för att undvika AmbiguousParameterSetException.</span><span class="sxs-lookup"><span data-stu-id="2d45d-225">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="2d45d-226">Återskapade hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="2d45d-226">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d45d-227">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d45d-227">Az.Sql</span></span>
* <span data-ttu-id="2d45d-228">Lade till stöd för återställning till tidpunkt mellan prenumerationer på hanterade instanser.</span><span class="sxs-lookup"><span data-stu-id="2d45d-228">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="2d45d-229">Lade till stöd för att ändra befintlig SQL Managed Instance-maskinvarugenerering</span><span class="sxs-lookup"><span data-stu-id="2d45d-229">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="2d45d-230">Åtgärdade ”Update-AzSqlServerVulnerabilityAssessmentSetting”-hjälpexempel: parameter/egenskapsutdata - EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="2d45d-230">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="2d45d-231">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="2d45d-231">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="2d45d-232">Lade till cmdletar för lyssningsfunktion för tillgänglighetsgrupp</span><span class="sxs-lookup"><span data-stu-id="2d45d-232">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="2d45d-233">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="2d45d-233">Az.StorageSync</span></span>
* <span data-ttu-id="2d45d-234">Uppdaterade teckenuppsättningar som stöds i ”Invoke-AzStorageSyncCompatibilityCheck”.</span><span class="sxs-lookup"><span data-stu-id="2d45d-234">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="2d45d-235">3.4.0 – februari 2020</span><span class="sxs-lookup"><span data-stu-id="2d45d-235">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="2d45d-236">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="2d45d-236">Highlights since the last major release</span></span>
* <span data-ttu-id="2d45d-237">Första Az.CosmosDB-versionen 0.1.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="2d45d-237">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="2d45d-238">Stöd för Az.Network ConnectionMonitor V2 har lagts till</span><span class="sxs-lookup"><span data-stu-id="2d45d-238">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="2d45d-239">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d45d-239">Az.Accounts</span></span>
* <span data-ttu-id="2d45d-240">Inaktivera automatisk sparande av kontext när AzureRmContext.json inte är tillgängligt</span><span class="sxs-lookup"><span data-stu-id="2d45d-240">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="2d45d-241">Uppdatera referensen till Azure Powershell Common till 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="2d45d-241">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="2d45d-242">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2d45d-242">Az.ApiManagement</span></span>
* <span data-ttu-id="2d45d-243">**Get-AzApiManagementApiSchema** Hämtning av Open-Api-schema som är associerat med ett API har åtgärdats   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="2d45d-243">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="2d45d-244">**New-AzApiManagementProduct**\* och **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="2d45d-244">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="2d45d-245">Åtgärda dokumentation för https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="2d45d-245">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="2d45d-246">**Set-AzApiManagementApi** Exempel för att visa hur ServiceUrl uppdateras med hjälp av cmdleten har lagts till</span><span class="sxs-lookup"><span data-stu-id="2d45d-246">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d45d-247">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d45d-247">Az.Compute</span></span>
* <span data-ttu-id="2d45d-248">Begränsa antalet VM-status till 100 för att undvika begränsning när Get-AzVM -Status utförs utan VM-namn.</span><span class="sxs-lookup"><span data-stu-id="2d45d-248">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="2d45d-249">Lägg till cmdleten Update-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="2d45d-249">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="2d45d-250">Lägg till parametrarna EncryptionType och DiskEncryptionSetId i följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="2d45d-250">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="2d45d-251">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="2d45d-251">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="2d45d-252">Lägg till parametern ColocationStatus för cmdleten Get-AzProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="2d45d-252">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2d45d-253">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2d45d-253">Az.DataFactory</span></span>
* <span data-ttu-id="2d45d-254">Uppdatera ADF .Net SDK-versionen till 4.7.0</span><span class="sxs-lookup"><span data-stu-id="2d45d-254">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="2d45d-255">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="2d45d-255">Az.DeploymentManager</span></span>
* <span data-ttu-id="2d45d-256">Lägger till LIST-åtgärder för resurser</span><span class="sxs-lookup"><span data-stu-id="2d45d-256">Adds LIST operations for resources</span></span>
* <span data-ttu-id="2d45d-257">Lägger till funktion för att utföra åtgärder för hälsokontrollsteg</span><span class="sxs-lookup"><span data-stu-id="2d45d-257">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="2d45d-258">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="2d45d-258">Az.HDInsight</span></span>
* <span data-ttu-id="2d45d-259">Åtgärda dokumentfel för New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="2d45d-259">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="2d45d-260">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2d45d-260">Az.KeyVault</span></span>
* <span data-ttu-id="2d45d-261">Lägg till Name-alias för attributet VaultName så att Remove-AzureKeyVault stämmer överens med New-AzureKeyVault.</span><span class="sxs-lookup"><span data-stu-id="2d45d-261">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d45d-262">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d45d-262">Az.Network</span></span>
* <span data-ttu-id="2d45d-263">Nytt exempel har lagts till i Set-AzNetworkWatcherConfigFlowLog.md för att demonstrera ett inaktiveringsscenario för Trafikanalys.</span><span class="sxs-lookup"><span data-stu-id="2d45d-263">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="2d45d-264">Lägg till stöd för att tilldela konfiguration av hanterings-IP till Azure Firewall – ett dedikerat undernät och en offentlig IP som brandväggen använder för dess hanteringstrafik</span><span class="sxs-lookup"><span data-stu-id="2d45d-264">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="2d45d-265">Cmdleten New-AzFirewall har uppdaterats:</span><span class="sxs-lookup"><span data-stu-id="2d45d-265">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="2d45d-266">Parametern -ManagementPublicIpAddress (inte obligatorisk) som accepterar ett offentligt IP-adressobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="2d45d-266">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="2d45d-267">Metoden SetManagementIpConfiguration har lagts till för brandväggsobjekt – kräver ett undernät och en offentlig IP-adress som indata – undernätets namn måste vara ”AzureFirewallManagementSubnet”</span><span class="sxs-lookup"><span data-stu-id="2d45d-267">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="2d45d-268">Exempel för Get-AzNetworkSecurityGroup har korrigerats så att exempel visas för NSG:er i stället för nätverksgränssnitt.</span><span class="sxs-lookup"><span data-stu-id="2d45d-268">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="2d45d-269">Ett skrivfel har åtgärdats i kommandot New-AzVpnSite som hindrade kompletteraren för resurs-ID från att fylla i en parameter.</span><span class="sxs-lookup"><span data-stu-id="2d45d-269">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="2d45d-270">Stöd för Url-konfiguration i åtgärdsuppsättningen för omskrivningsregler i Application Gateway har lagts till</span><span class="sxs-lookup"><span data-stu-id="2d45d-270">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="2d45d-271">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="2d45d-271">New cmdlets added:</span></span>
        - <span data-ttu-id="2d45d-272">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="2d45d-272">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="2d45d-273">Cmdletar har uppdaterats med den valfria parametern -UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="2d45d-273">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="2d45d-274">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="2d45d-274">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="2d45d-275">Lägg till stöd för resurser för NetworkWatcher ConnectionMonitor version 2</span><span class="sxs-lookup"><span data-stu-id="2d45d-275">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="2d45d-276">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="2d45d-276">Az.PolicyInsights</span></span>
* <span data-ttu-id="2d45d-277">Stöd för utvärdering av efterlevnad innan fastställande av vilken resurs som ska åtgärdas</span><span class="sxs-lookup"><span data-stu-id="2d45d-277">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="2d45d-278">Lägg till parametern ”-ResourceDiscoverMode” för Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="2d45d-278">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="2d45d-279">Lägg till cmdleten Get-AzPolicyMetadata för att hämta resurser för principmetadata</span><span class="sxs-lookup"><span data-stu-id="2d45d-279">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="2d45d-280">Get-AzPolicyState och Get-AzPolicyStateSummary för API-versionen 2019-10-01 har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="2d45d-280">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2d45d-281">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d45d-281">Az.RecoveryServices</span></span>
* <span data-ttu-id="2d45d-282">Azure Site Recovery-stöd för att ta bort en replikerad disk.</span><span class="sxs-lookup"><span data-stu-id="2d45d-282">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="2d45d-283">Tillagt Azure Backup-stöd för att lägga till taggar när ett Recovery Services-valv skapas.</span><span class="sxs-lookup"><span data-stu-id="2d45d-283">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d45d-284">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d45d-284">Az.Resources</span></span>
* <span data-ttu-id="2d45d-285">Gör -Scope valfritt i cmdletarna \*-AzPolicyAssignment med standardinställning till kontextprenumeration</span><span class="sxs-lookup"><span data-stu-id="2d45d-285">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="2d45d-286">Lägg till exempel på att skapa ADServicePrincipal med lösenord och nyckelautentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="2d45d-286">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d45d-287">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d45d-287">Az.Sql</span></span>
<span data-ttu-id="2d45d-288">Åtgärda cmdleten New-AzSqlDatabaseSecondary så att existensen PartnerDatabaseName kontrolleras i stället för existensen DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="2d45d-288">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2d45d-289">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d45d-289">Az.Storage</span></span>
* <span data-ttu-id="2d45d-290">Stöd för angivning av krypteringsnyckeltyp för Tabell/kö i Skapa lagringskonto</span><span class="sxs-lookup"><span data-stu-id="2d45d-290">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="2d45d-291">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2d45d-291">New-AzStorageAccount</span></span>
* <span data-ttu-id="2d45d-292">Visa RequestId när StorageException inte har ExtendedErrorInformation</span><span class="sxs-lookup"><span data-stu-id="2d45d-292">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="2d45d-293">Åtgärda exempel 6 för cmdleten Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="2d45d-293">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2d45d-294">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2d45d-294">Az.Websites</span></span>
* <span data-ttu-id="2d45d-295">Set-AzWebapp och Set-AzWebappSlot stöder egenskaperna AlwaysOn, MinTls och FtpsState</span><span class="sxs-lookup"><span data-stu-id="2d45d-295">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="2d45d-296">Åtgärdar problemet där inställning av HttpsOnly samtidigt som AppservicePlan ändrades med det enskilda kommandot Set-AzWebApp återställde HttpsOnly till standardvärdet</span><span class="sxs-lookup"><span data-stu-id="2d45d-296">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="2d45d-297">3.3.0 – januari 2020</span><span class="sxs-lookup"><span data-stu-id="2d45d-297">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2d45d-298">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d45d-298">Az.Accounts</span></span>
* <span data-ttu-id="2d45d-299">Nu stöder Add-AzEnvironment och Set-AzEnvironment parametrarna AzureAttestationServiceEndpointResourceId och AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="2d45d-299">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="2d45d-300">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="2d45d-300">Az.Cdn</span></span>
* <span data-ttu-id="2d45d-301">Information om felsvar visas i New-AzCdnEndpoint-cmdleten</span><span class="sxs-lookup"><span data-stu-id="2d45d-301">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d45d-302">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d45d-302">Az.Compute</span></span>
* <span data-ttu-id="2d45d-303">Set-AzVMCustomScriptExtension-cmdleten har åtgärdats för en virtuell dator med hanterad OD-disk som inte har någon operativsystemprofil.</span><span class="sxs-lookup"><span data-stu-id="2d45d-303">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="2d45d-304">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="2d45d-304">Az.ContainerInstance</span></span>
* <span data-ttu-id="2d45d-305">Parameternamn som används med New-AzContainerGroup-exempel har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="2d45d-305">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="2d45d-306">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="2d45d-306">Az.DataBoxEdge</span></span>
* <span data-ttu-id="2d45d-307">Cmdleten ”Get-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="2d45d-307">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="2d45d-308">Hämta gränslagringscontainern</span><span class="sxs-lookup"><span data-stu-id="2d45d-308">Get the Edge Storage Container</span></span>
* <span data-ttu-id="2d45d-309">Cmdleten ”New-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="2d45d-309">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="2d45d-310">Skapa en ny gränslagringscontainer</span><span class="sxs-lookup"><span data-stu-id="2d45d-310">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="2d45d-311">Cmdleten ”Remove-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="2d45d-311">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="2d45d-312">Ta bort gränslagringscontainern</span><span class="sxs-lookup"><span data-stu-id="2d45d-312">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="2d45d-313">Cmdleten ”Invoke-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="2d45d-313">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="2d45d-314">Anropa åtgärd för att uppdatera data i gränslagringscontainer</span><span class="sxs-lookup"><span data-stu-id="2d45d-314">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="2d45d-315">Cmdleten ”Get-AzDataBoxEdgeStorageAccount” har lagts till</span><span class="sxs-lookup"><span data-stu-id="2d45d-315">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="2d45d-316">Hämta gränslagringskontot</span><span class="sxs-lookup"><span data-stu-id="2d45d-316">Get the Edge Storage Account</span></span>
* <span data-ttu-id="2d45d-317">Cmdleten ”New-AzDataBoxEdgeStorageAccount” har lagts till</span><span class="sxs-lookup"><span data-stu-id="2d45d-317">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="2d45d-318">Skapa ett nytt gränslagringskonto</span><span class="sxs-lookup"><span data-stu-id="2d45d-318">Create new Edge Storage Account</span></span>
* <span data-ttu-id="2d45d-319">Cmdleten ”Remove-AzDataBoxEdgeStorageAccount” har lagts till</span><span class="sxs-lookup"><span data-stu-id="2d45d-319">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="2d45d-320">Ta bort gränslagringskontot</span><span class="sxs-lookup"><span data-stu-id="2d45d-320">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="2d45d-321">Anropa cmdleten ”Invoke-AzDataBoxEdgeShare”</span><span class="sxs-lookup"><span data-stu-id="2d45d-321">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="2d45d-322">Anropa åtgärd för att uppdatera resursdata</span><span class="sxs-lookup"><span data-stu-id="2d45d-322">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="2d45d-323">Cmdleten ”Set-AzDataBoxEdgeStorageAccountCredential” har lagts till</span><span class="sxs-lookup"><span data-stu-id="2d45d-323">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="2d45d-324">Ange autentiseringsuppgifter för az databoxedge-lagringskonto</span><span class="sxs-lookup"><span data-stu-id="2d45d-324">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2d45d-325">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2d45d-325">Az.DataFactory</span></span>
* <span data-ttu-id="2d45d-326">Lägg till AutoUpdateETA-, LatestVersion-, PushedVersion-, TaskQueueId- och VersionStatus-egenskaper för Get-AzDataFactoryV2IntegrationRuntime-cmd</span><span class="sxs-lookup"><span data-stu-id="2d45d-326">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="2d45d-327">Uppdatera ADF .Net SDK-versionen till 4.6.0</span><span class="sxs-lookup"><span data-stu-id="2d45d-327">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="2d45d-328">Lägg till parametern ”PublicIPs” för ”Set-AzureRmDataFactoryV2IntegrationRuntime”-cmd så att Azure-SSIS IR kan skapas med statiska offentliga IP-adresser.</span><span class="sxs-lookup"><span data-stu-id="2d45d-328">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="2d45d-329">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="2d45d-329">Az.DevTestLabs</span></span>
* <span data-ttu-id="2d45d-330">Ta bort den brutna länken i Get-AzDtlAllowedVMSizesPolicy.md</span><span class="sxs-lookup"><span data-stu-id="2d45d-330">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="2d45d-331">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="2d45d-331">Az.EventHub</span></span>
* <span data-ttu-id="2d45d-332">Korrigering av problem 10634: Åtgärda referensen till null-objekt för eventhubnamespace-borttagning</span><span class="sxs-lookup"><span data-stu-id="2d45d-332">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="2d45d-333">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="2d45d-333">Az.HDInsight</span></span>
* <span data-ttu-id="2d45d-334">Åtgärda Invoke-AzHDInsightHiveJob.md-fel.</span><span class="sxs-lookup"><span data-stu-id="2d45d-334">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="2d45d-335">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="2d45d-335">Az.MachineLearning</span></span>
* <span data-ttu-id="2d45d-336">Nedanstående cmdletar har tagits bort eftersom MachineLearningCompute inte längre är tillgängligt</span><span class="sxs-lookup"><span data-stu-id="2d45d-336">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="2d45d-337">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="2d45d-337">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="2d45d-338">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="2d45d-338">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="2d45d-339">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="2d45d-339">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="2d45d-340">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="2d45d-340">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="2d45d-341">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="2d45d-341">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="2d45d-342">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="2d45d-342">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="2d45d-343">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="2d45d-343">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d45d-344">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d45d-344">Az.Network</span></span>
* <span data-ttu-id="2d45d-345">Uppgradera beroende av Microsoft.Azure.Management.Sql från 1.36-preview till 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="2d45d-345">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2d45d-346">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d45d-346">Az.RecoveryServices</span></span>
* <span data-ttu-id="2d45d-347">Ändrat Azure Site Recovery-stöd för krypterade vilande data på virtuella datorer med hanterade diskar med kundhanterade nycklar för Azure till Azure-providern.</span><span class="sxs-lookup"><span data-stu-id="2d45d-347">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="2d45d-348">Azure Site Recovery-stöd för att ange ID för diskkrypteringsuppsättning som valfri inmatning för aktivering av skydd för VMware till Azure.</span><span class="sxs-lookup"><span data-stu-id="2d45d-348">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="2d45d-349">Azure Site Recovery-stöd för att ange ID för diskkrypteringsuppsättning som valfri inmatning på disknivå för aktivering av skydd för VMware till Azure.</span><span class="sxs-lookup"><span data-stu-id="2d45d-349">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="2d45d-350">Azure Site Recovery-stöd för att uppdatera replikeringsskyddade objekt med mappning för diskkrypteringsuppsättning för HyperV till Azure.</span><span class="sxs-lookup"><span data-stu-id="2d45d-350">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d45d-351">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d45d-351">Az.Resources</span></span>
* <span data-ttu-id="2d45d-352">Åtgärda ett fel i hjälpdokument för ”Remove-AzTag”.</span><span class="sxs-lookup"><span data-stu-id="2d45d-352">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d45d-353">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d45d-353">Az.Sql</span></span>
* <span data-ttu-id="2d45d-354">Åtgärda funktioner i cmdletar för att ange baslinjen för sårbarhetsbedömning för arbete med huvuddatabasen för Azure-databasen och begränsa den för systemdatabaser på hanterade instanser.</span><span class="sxs-lookup"><span data-stu-id="2d45d-354">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="2d45d-355">Åtgärda ett fel när en redundansgrupp för en SQL-instans skapas</span><span class="sxs-lookup"><span data-stu-id="2d45d-355">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="2d45d-356">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="2d45d-356">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="2d45d-357">Lägg till DR som en ny giltig licenstyp</span><span class="sxs-lookup"><span data-stu-id="2d45d-357">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2d45d-358">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d45d-358">Az.Storage</span></span>
* <span data-ttu-id="2d45d-359">Lägg till varningsmeddelande om icke-bakåtkompatibel ändring för DefaultAction-värdeändring i en framtida version</span><span class="sxs-lookup"><span data-stu-id="2d45d-359">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="2d45d-360">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="2d45d-360">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="2d45d-361">Stöd för att hämta lagringskontots senaste synkroniseringstid genom att köra get-AzureRMStorageAccount med parametern -IncludeGeoReplicationStats</span><span class="sxs-lookup"><span data-stu-id="2d45d-361">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="2d45d-362">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2d45d-362">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="2d45d-363">3.2.0 – December 2019</span><span class="sxs-lookup"><span data-stu-id="2d45d-363">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="2d45d-364">Allmänt</span><span class="sxs-lookup"><span data-stu-id="2d45d-364">General</span></span>
* <span data-ttu-id="2d45d-365">Uppdatera referenser i .psd1 för att använda relativa sökvägar för alla moduler</span><span class="sxs-lookup"><span data-stu-id="2d45d-365">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="2d45d-366">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d45d-366">Az.Accounts</span></span>
* <span data-ttu-id="2d45d-367">Ange rätt UserAgent för telemetri på klientsidan för Az 4.0 preview</span><span class="sxs-lookup"><span data-stu-id="2d45d-367">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="2d45d-368">Visa användarvänligt felmeddelande när kontexten är null i Az 4.0 preview</span><span class="sxs-lookup"><span data-stu-id="2d45d-368">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="2d45d-369">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="2d45d-369">Az.Batch</span></span>
* <span data-ttu-id="2d45d-370">Korrigera problem [#10602](https://github.com/Azure/azure-powershell/issues/10602), där **New-AzBatchPool** skickade VirtualMachineConfiguration.ContainerConfiguration eller VirtualMachineConfiguration.DataDisks på ett felaktigt sätt till servern.</span><span class="sxs-lookup"><span data-stu-id="2d45d-370">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2d45d-371">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2d45d-371">Az.DataFactory</span></span>
* <span data-ttu-id="2d45d-372">Uppdatera ADF .Net SDK-versionen till 4.5.0</span><span class="sxs-lookup"><span data-stu-id="2d45d-372">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="2d45d-373">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="2d45d-373">Az.FrontDoor</span></span>
* <span data-ttu-id="2d45d-374">Stöd har lagts till för undantag för hanterade regler för brandväggen för webbaserade program</span><span class="sxs-lookup"><span data-stu-id="2d45d-374">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="2d45d-375">Lägg till SocketAddr för automatisk komplettering</span><span class="sxs-lookup"><span data-stu-id="2d45d-375">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="2d45d-376">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="2d45d-376">Az.HealthcareApis</span></span>
* <span data-ttu-id="2d45d-377">Undantagshantering</span><span class="sxs-lookup"><span data-stu-id="2d45d-377">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="2d45d-378">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2d45d-378">Az.KeyVault</span></span>
* <span data-ttu-id="2d45d-379">Åtgärdat fel vid åtkomst av värde som kanske inte har angetts</span><span class="sxs-lookup"><span data-stu-id="2d45d-379">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="2d45d-380">Hantering av ECC-certifikat (Elliptic Curve Cryptography)</span><span class="sxs-lookup"><span data-stu-id="2d45d-380">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="2d45d-381">Stöd har lagts till för att ange kurvan för certifikatprinciper</span><span class="sxs-lookup"><span data-stu-id="2d45d-381">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2d45d-382">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2d45d-382">Az.Monitor</span></span>
* <span data-ttu-id="2d45d-383">Lägger till valfritt argument i kommandot Lägg till diagnostikinställningar.</span><span class="sxs-lookup"><span data-stu-id="2d45d-383">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="2d45d-384">Ett växelargument som om det finns visar att exporten till Log Analytics måste ske till ett fast schema (kallas även</span><span class="sxs-lookup"><span data-stu-id="2d45d-384">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="2d45d-385">dedikerad, datatyp)</span><span class="sxs-lookup"><span data-stu-id="2d45d-385">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d45d-386">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d45d-386">Az.Network</span></span>
* <span data-ttu-id="2d45d-387">Stöd för IpGroups i program-, NAT- och nätverksregler för Azure Firewall.</span><span class="sxs-lookup"><span data-stu-id="2d45d-387">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d45d-388">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d45d-388">Az.Resources</span></span>
* <span data-ttu-id="2d45d-389">Åtgärda ett problem där malldistributionen inte kan läsa en mallparameter om dess namn står i konflikt med ett inbyggt parameternamn.</span><span class="sxs-lookup"><span data-stu-id="2d45d-389">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="2d45d-390">Uppdaterade princip-cmdletar för att använda den nya API-versionen 2019-09-01 som introducerar grupperingsstöd inom principuppsättningsdefinitioner.</span><span class="sxs-lookup"><span data-stu-id="2d45d-390">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d45d-391">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d45d-391">Az.Sql</span></span>
* <span data-ttu-id="2d45d-392">Uppgraderad funktion för att skapa lagring i automatisk aktivering av sårbarhetsbedömning till StorageV2</span><span class="sxs-lookup"><span data-stu-id="2d45d-392">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2d45d-393">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d45d-393">Az.Storage</span></span>
* <span data-ttu-id="2d45d-394">Stöd för generering av blob/container-identitetsbaserad SAS-token med lagringskontextbaserad på OAuth-autentisering</span><span class="sxs-lookup"><span data-stu-id="2d45d-394">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="2d45d-395">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="2d45d-395">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="2d45d-396">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="2d45d-396">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="2d45d-397">Stöd för återkallning av användardelegeringsnycklar för lagringskonto för att återkalla alla SAS-token</span><span class="sxs-lookup"><span data-stu-id="2d45d-397">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="2d45d-398">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="2d45d-398">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="2d45d-399">Uppgradera till Microsoft.Azure.Management.Storage 14.2.0 för att stödja den nya API-versionen 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="2d45d-399">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="2d45d-400">Stöd för QuotaGiB (resurskvot i Gibibye) för värden över 5120 i hanteringsplanet för cmdletar för filresurser och parameteraliaset. Quota har också lagts till för parametern ”QuotaGiB”.</span><span class="sxs-lookup"><span data-stu-id="2d45d-400">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="2d45d-401">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="2d45d-401">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="2d45d-402">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="2d45d-402">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="2d45d-403">Lägg till parameteraliaset QuotaGiB i parametern Quota</span><span class="sxs-lookup"><span data-stu-id="2d45d-403">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="2d45d-404">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="2d45d-404">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="2d45d-405">Åtgärda problemet att Set-AzStorageContainerAcl kan rensa den lagrade åtkomstprincipen</span><span class="sxs-lookup"><span data-stu-id="2d45d-405">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="2d45d-406">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="2d45d-406">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="2d45d-407">3.1.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="2d45d-407">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="2d45d-408">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="2d45d-408">Highlights since the last major release</span></span>
* <span data-ttu-id="2d45d-409">Az.DataBoxEdge 1.0.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="2d45d-409">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="2d45d-410">Az.SqlVirtualMachine 1.0.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="2d45d-410">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d45d-411">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d45d-411">Az.Compute</span></span>
* <span data-ttu-id="2d45d-412">Funktion för att använda en virtuell dator igen</span><span class="sxs-lookup"><span data-stu-id="2d45d-412">VM Reapply feature</span></span>
    - <span data-ttu-id="2d45d-413">Lägg till parameter för att använda igen till cmdleten Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="2d45d-413">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="2d45d-414">Funktionen AutomaticRepairs i VM-skalningsuppsättningar:</span><span class="sxs-lookup"><span data-stu-id="2d45d-414">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="2d45d-415">Lägg till parametrarna EnableAutomaticRepair, AutomaticRepairGracePeriod och AutomaticRepairMaxInstanceRepairsPercent till följande cmdletar:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="2d45d-415">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="2d45d-416">Stöd för galleriavbildningar i flera klientorganisationer för New-AzVM</span><span class="sxs-lookup"><span data-stu-id="2d45d-416">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="2d45d-417">Lägg till "Spot" till argumentslutföraren i prioritetsparametern i cmdletarna New-AzVM, New-AzVMConfig och New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="2d45d-417">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="2d45d-418">Lägg till parametrarna DiskIOPSReadWrite och DiskMBpsReadWrite till cmdleten Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="2d45d-418">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="2d45d-419">Ändra parametern SourceImageId för cmdleten New-AzGalleryImageVersion till valfri</span><span class="sxs-lookup"><span data-stu-id="2d45d-419">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="2d45d-420">Lägg till parametrarna OSDiskImage och DataDiskImage till cmdleten New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="2d45d-420">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="2d45d-421">Lägg till parametern HyperVGeneration till cmdleten New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="2d45d-421">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="2d45d-422">Lägg till parametern SkipExtensionsOnOverprovisionedVMs till cmdletarna New-AzVmss, New-AzVmssConfig och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="2d45d-422">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="2d45d-423">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="2d45d-423">Az.DataBoxEdge</span></span>
* <span data-ttu-id="2d45d-424">Cmdleten `Get-AzDataBoxEdgeOrder` har lagts till</span><span class="sxs-lookup"><span data-stu-id="2d45d-424">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="2d45d-425">Hämta ordning</span><span class="sxs-lookup"><span data-stu-id="2d45d-425">Get the Order</span></span>
* <span data-ttu-id="2d45d-426">Cmdleten `New-AzDataBoxEdgeOrder` har lagts till</span><span class="sxs-lookup"><span data-stu-id="2d45d-426">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="2d45d-427">Skapa ny ordning</span><span class="sxs-lookup"><span data-stu-id="2d45d-427">Create new Order</span></span>
* <span data-ttu-id="2d45d-428">Cmdleten `Remove-AzDataBoxEdgeOrder` har lagts till</span><span class="sxs-lookup"><span data-stu-id="2d45d-428">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="2d45d-429">Ta bort ordning</span><span class="sxs-lookup"><span data-stu-id="2d45d-429">Remove the Order</span></span>
* <span data-ttu-id="2d45d-430">Cmdleten `New-AzDataBoxEdgeShare` har ändrats</span><span class="sxs-lookup"><span data-stu-id="2d45d-430">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="2d45d-431">Nu skapas lokal filresurs</span><span class="sxs-lookup"><span data-stu-id="2d45d-431">Now creates Local Share</span></span>
* <span data-ttu-id="2d45d-432">Cmdleten `Set-AzDataBoxEdgeRole` har lagts till</span><span class="sxs-lookup"><span data-stu-id="2d45d-432">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="2d45d-433">Nu kan IotRole mappas till filresursen</span><span class="sxs-lookup"><span data-stu-id="2d45d-433">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="2d45d-434">Cmdleten `Invoke-AzDataBoxEdgeDevice` har lagts till</span><span class="sxs-lookup"><span data-stu-id="2d45d-434">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="2d45d-435">Anropa genomsökningsuppdatering, ladda ned uppdatering, installera uppdateringar på enheten</span><span class="sxs-lookup"><span data-stu-id="2d45d-435">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="2d45d-436">Cmdleten `Get-AzDataBoxEdgeTrigger` har lagts till</span><span class="sxs-lookup"><span data-stu-id="2d45d-436">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="2d45d-437">Hämtar information om utlösare</span><span class="sxs-lookup"><span data-stu-id="2d45d-437">Gets the information about Triggers</span></span>
* <span data-ttu-id="2d45d-438">Cmdleten `New-AzDataBoxEdgeTrigger` har lagts till</span><span class="sxs-lookup"><span data-stu-id="2d45d-438">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="2d45d-439">Skapa nya utlösare</span><span class="sxs-lookup"><span data-stu-id="2d45d-439">Create new Triggers</span></span>
* <span data-ttu-id="2d45d-440">Cmdleten `Remove-AzDataBoxEdgeTrigger` har lagts till</span><span class="sxs-lookup"><span data-stu-id="2d45d-440">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="2d45d-441">Ta bort utlösare</span><span class="sxs-lookup"><span data-stu-id="2d45d-441">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2d45d-442">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2d45d-442">Az.DataFactory</span></span>
* <span data-ttu-id="2d45d-443">Uppdatera ADF .Net SDK-versionen till 4.4.0</span><span class="sxs-lookup"><span data-stu-id="2d45d-443">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="2d45d-444">Lägg till parametern ExpressCustomSetup för kommandot Set-AzureRmDataFactoryV2IntegrationRuntime för att aktivera installationskonfigurationer och komponenter från tredje part utan anpassat konfigurationsskript.</span><span class="sxs-lookup"><span data-stu-id="2d45d-444">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2d45d-445">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2d45d-445">Az.DataLakeStore</span></span>
* <span data-ttu-id="2d45d-446">Uppdatera dokumentation för Get-AzDataLakeStoreDeletedItem och Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="2d45d-446">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="2d45d-447">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="2d45d-447">Az.EventHub</span></span>
* <span data-ttu-id="2d45d-448">Korrigering av problem #10301: Korrigera datumformat för SAS-token</span><span class="sxs-lookup"><span data-stu-id="2d45d-448">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="2d45d-449">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="2d45d-449">Az.FrontDoor</span></span>
* <span data-ttu-id="2d45d-450">Lägg till parametern MinimumTlsVersion till Enable-AzFrontDoorCustomDomainHttps och New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="2d45d-450">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="2d45d-451">Lägg till parametrarna HealthProbeMethod och EnabledState till New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="2d45d-451">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="2d45d-452">Lägg till en ny cmdlet för att skapa BackendPoolsSettings-objekt som passar i skapande/uppdatering av Front Door</span><span class="sxs-lookup"><span data-stu-id="2d45d-452">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="2d45d-453">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="2d45d-453">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d45d-454">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d45d-454">Az.Network</span></span>
* <span data-ttu-id="2d45d-455">Ändra alternativexemplen Start-AzVirtualNetworkGatewayConnectionPacketCapture.md och Start-AzVirtualnetworkGatewayPacketCapture.md för FilterData.</span><span class="sxs-lookup"><span data-stu-id="2d45d-455">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="2d45d-456">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="2d45d-456">Az.PrivateDns</span></span>
* <span data-ttu-id="2d45d-457">Uppdaterade PrivateDns .NET SDK till version 1.0.0</span><span class="sxs-lookup"><span data-stu-id="2d45d-457">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2d45d-458">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d45d-458">Az.RecoveryServices</span></span>
* <span data-ttu-id="2d45d-459">Stöd för att välja disktyp vid aktivering av skydd i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="2d45d-459">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="2d45d-460">Korrigering av bugg för åtgärdsredigering av återställningsplan i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="2d45d-460">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="2d45d-461">Återställningsstöd för att godkänna filestream-databaser i Azure Backup SQL.</span><span class="sxs-lookup"><span data-stu-id="2d45d-461">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="2d45d-462">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="2d45d-462">Az.RedisCache</span></span>
* <span data-ttu-id="2d45d-463">Parametern MinimumTlsVersion har lagts till i cmdletarna New-AzRedisCache och Set-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="2d45d-463">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="2d45d-464">Dessutom har MinimumTlsVersion lagts till i utdata för cmdleten Get-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="2d45d-464">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="2d45d-465">Verifiering har lagts till på parametern -Size i cmdletarna Set-AzRedisCache och New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="2d45d-465">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d45d-466">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d45d-466">Az.Resources</span></span>
- <span data-ttu-id="2d45d-467">Uppdaterade policy-cmdletar för att använda den nya API-versionen 2019-06-01 som har en ny EnforcementMode-egenskap i policytilldelningen.</span><span class="sxs-lookup"><span data-stu-id="2d45d-467">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="2d45d-468">Uppdaterade hjälpexempel för skapandet av policydefinition</span><span class="sxs-lookup"><span data-stu-id="2d45d-468">Updated create policy definition help example</span></span>
- <span data-ttu-id="2d45d-469">Åtgärda bugg i Remove-AZADServicePrincipal -ServicePrincipalName, utlös null-referens när tjänstens huvudnamn inte hittas.</span><span class="sxs-lookup"><span data-stu-id="2d45d-469">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="2d45d-470">Åtgärda bugg i New-AZADServicePrincipal, utlös null-referens när klientorganisationen inte har någon prenumeration.</span><span class="sxs-lookup"><span data-stu-id="2d45d-470">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="2d45d-471">Ändra New-AzAdServicePrincipal för att endast lägga till autentiseringsuppgifter för det associerade programmet.</span><span class="sxs-lookup"><span data-stu-id="2d45d-471">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d45d-472">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d45d-472">Az.Sql</span></span>
* <span data-ttu-id="2d45d-473">Stöd har lagts till för databasen ReadReplicaCount.</span><span class="sxs-lookup"><span data-stu-id="2d45d-473">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="2d45d-474">Korrigerade Set-AzSqlDatabase när zonredundans inte har angetts</span><span class="sxs-lookup"><span data-stu-id="2d45d-474">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="2d45d-475">3.0.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="2d45d-475">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="2d45d-476">Allmänt</span><span class="sxs-lookup"><span data-stu-id="2d45d-476">General</span></span>
* <span data-ttu-id="2d45d-477">Az. PrivateDns 1.0.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="2d45d-477">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="2d45d-478">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d45d-478">Az.Accounts</span></span>
* <span data-ttu-id="2d45d-479">Lägg till ett utfasningsmeddelande för aliaset Resolve-error.</span><span class="sxs-lookup"><span data-stu-id="2d45d-479">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="2d45d-480">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="2d45d-480">Az.Advisor</span></span>
* <span data-ttu-id="2d45d-481">Den nya kategorin Operational Excellence har lagts till i cmdleten Get-AzAdvisorRecommendation.</span><span class="sxs-lookup"><span data-stu-id="2d45d-481">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="2d45d-482">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="2d45d-482">Az.Batch</span></span>
* <span data-ttu-id="2d45d-483">`CoreQuota` på `BatchAccountContext` har bytt namn till `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="2d45d-483">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="2d45d-484">Det finns även en ny `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="2d45d-484">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="2d45d-485">Detta påverkar **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="2d45d-485">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="2d45d-486">**New-AzBatchTask** `-ResourceFile`-parametern tar nu en samling `PSResourceFile`-objekt som kan skapas med hjälp av den nya cmdleten **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="2d45d-486">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="2d45d-487">Ny **New-AzBatchResourceFile**-cmdlet för att skapa `PSResourceFile`-objekt.</span><span class="sxs-lookup"><span data-stu-id="2d45d-487">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="2d45d-488">Dessa kan tillhandahållas till **New-AzBatchTask** på `-ResourceFile`-parametern.</span><span class="sxs-lookup"><span data-stu-id="2d45d-488">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="2d45d-489">Detta stöder två nya typer av resursfiler förutom det befintliga sättet med `HttpUrl`:</span><span class="sxs-lookup"><span data-stu-id="2d45d-489">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="2d45d-490">`AutoStorageContainerName`-baserade resursfiler laddar ned en hel container för automatisk lagring till Batch-noden.</span><span class="sxs-lookup"><span data-stu-id="2d45d-490">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="2d45d-491">`StorageContainerUrl`-baserade resursfiler laddar ned containern som anges i webbadressen till Batch-noden.</span><span class="sxs-lookup"><span data-stu-id="2d45d-491">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="2d45d-492">Tog bort egenskapen `ApplicationPackages` för `PSApplication` som returnerades av **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="2d45d-492">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="2d45d-493">Specifika paket i ett program kan nu hämtas med hjälp av **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="2d45d-493">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="2d45d-494">Till exempel: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="2d45d-494">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="2d45d-495">Bytt namn på `ApplicationId` till `ApplicationName` på **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** och **Set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="2d45d-495">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="2d45d-496">`ApplicationId` är nu ett alias för `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="2d45d-496">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="2d45d-497">Ny `PSWindowsUserConfiguration`-egenskap till `PSUserAccount` lades till.</span><span class="sxs-lookup"><span data-stu-id="2d45d-497">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="2d45d-498">Bytte namn på `Version` till `Name` på `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="2d45d-498">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="2d45d-499">Bytte namn på `BlobSource` till `HttpUrl` på `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="2d45d-499">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="2d45d-500">Tog bort egenskapen `OSDisk` från `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="2d45d-500">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="2d45d-501">Tog bort **Set-AzBatchPoolOSVersion**.</span><span class="sxs-lookup"><span data-stu-id="2d45d-501">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="2d45d-502">Den här åtgärden stöds inte längre.</span><span class="sxs-lookup"><span data-stu-id="2d45d-502">This operation is no longer supported.</span></span>
* <span data-ttu-id="2d45d-503">`TargetOSVersion` har tagits bort från `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="2d45d-503">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="2d45d-504">Bytte namn på `CurrentOSVersion` till `OSVersion` på `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="2d45d-504">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="2d45d-505">`DataEgressGiB` och `DataIngressGiB` har tagits bort från `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="2d45d-505">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="2d45d-506">Tog bort **Get-AzBatchNodeAgentSku** och ersatte det med **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="2d45d-506">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="2d45d-507">**Get-AzBatchSupportedImage** returnerar samma data som **Get-AzBatchNodeAgentSku** men i ett mer användarvänligt format.</span><span class="sxs-lookup"><span data-stu-id="2d45d-507">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="2d45d-508">Nya icke-verifierade avbildningar returneras nu också.</span><span class="sxs-lookup"><span data-stu-id="2d45d-508">New non-verified images are also now returned.</span></span> <span data-ttu-id="2d45d-509">Ytterligare information om `Capabilities` och `BatchSupportEndOfLife` för varje avbildning inkluderas också.</span><span class="sxs-lookup"><span data-stu-id="2d45d-509">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="2d45d-510">Lade till möjlighet att montera fjärrfilsystem på varje nod i en pool via den nya parametern `MountConfiguration` för **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="2d45d-510">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="2d45d-511">Har nu stöd för nätverkssäkerhetsregler som blockerar nätverksåtkomst till en pool baserat på källportens trafik.</span><span class="sxs-lookup"><span data-stu-id="2d45d-511">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="2d45d-512">Detta görs via egenskapen `SourcePortRanges` på `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="2d45d-512">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="2d45d-513">När du kör en container stöder nu Batch körningen av uppgiften i arbetskatalogen för containern eller i arbetskatalogen för Batch-uppgiften.</span><span class="sxs-lookup"><span data-stu-id="2d45d-513">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="2d45d-514">Detta styrs av egenskapen `WorkingDirectory` på `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="2d45d-514">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="2d45d-515">Lade till en funktion för att ange en samling av offentliga IP-adresser på `PSNetworkConfiguration` via den nya egenskapen `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="2d45d-515">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="2d45d-516">Detta garanterar att noderna i poolen har en IP-adress från listan över IP-adresser som tillhandahållits av användare.</span><span class="sxs-lookup"><span data-stu-id="2d45d-516">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="2d45d-517">Om inget värde anges är standardvärdet för `WaitForSuccess` på `PSSTartTask` nu `$True` (var tidigare `$False`).</span><span class="sxs-lookup"><span data-stu-id="2d45d-517">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="2d45d-518">Om inget värde anges är standardvärdet för `Scope` på `PSAutoUserSpecification` nu `Pool` (var tidigare `Task` på Windows och `Pool` på Linux).</span><span class="sxs-lookup"><span data-stu-id="2d45d-518">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="2d45d-519">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="2d45d-519">Az.Cdn</span></span>
* <span data-ttu-id="2d45d-520">Introducerade UrlRewriteAction och CacheKeyQueryStringAction till RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="2d45d-520">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="2d45d-521">Åtgärdade flera buggar, som saknade indata för ”väljare” i cmdleten New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="2d45d-521">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d45d-522">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d45d-522">Az.Compute</span></span>
* <span data-ttu-id="2d45d-523">Funktion för diskkrypteringsuppsättning</span><span class="sxs-lookup"><span data-stu-id="2d45d-523">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="2d45d-524">Nya cmdletar:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="2d45d-524">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="2d45d-525">Parametern DiskEncryptionSetId har lagts till i följande cmdletar:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="2d45d-525">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="2d45d-526">Parametrarna DiskEncryptionSetId och EncryptionType har lagts till i följande cmdletar:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="2d45d-526">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="2d45d-527">Lägg till parametern PublicIPAddressVersion i New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="2d45d-527">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="2d45d-528">Flytta FileUris för anpassat skripttillägg från offentlig inställning till skyddad inställning</span><span class="sxs-lookup"><span data-stu-id="2d45d-528">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="2d45d-529">Lägg till ScaleInPolicy i cmdletarna New-AzVmss, New-AzVmssConfig och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="2d45d-529">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="2d45d-530">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="2d45d-530">Breaking changes</span></span>
    - <span data-ttu-id="2d45d-531">Parametern UploadSizeInBytes används istället för DiskSizeGB för New-AzDiskConfig när CreateOption är Uppladdning</span><span class="sxs-lookup"><span data-stu-id="2d45d-531">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="2d45d-532">PublishingProfile.Source.ManagedImage.Id ersätts med StorageProfile.Source.Id i objektet GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="2d45d-532">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2d45d-533">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2d45d-533">Az.DataFactory</span></span>
* <span data-ttu-id="2d45d-534">Uppdatera ADF .Net SDK-versionen till 4.3.0</span><span class="sxs-lookup"><span data-stu-id="2d45d-534">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2d45d-535">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2d45d-535">Az.DataLakeStore</span></span>
* <span data-ttu-id="2d45d-536">Uppdatera ADLS SDK-version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) innehåller följande korrigeringar</span><span class="sxs-lookup"><span data-stu-id="2d45d-536">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="2d45d-537">Undvik att utlösa undantag när det inte går att deserialisera creationtime för inmatning av papperskorg eller katalog.</span><span class="sxs-lookup"><span data-stu-id="2d45d-537">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="2d45d-538">Gör inställning tillgänglig per tidsgräns för förfrågan i adlsclient</span><span class="sxs-lookup"><span data-stu-id="2d45d-538">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="2d45d-539">Korrigera överföringen av ursprunglig syncflag för badoffset-återställning</span><span class="sxs-lookup"><span data-stu-id="2d45d-539">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="2d45d-540">Korrigera EnumerateDirectory för att hämta fortsättningstoken när svar har kontrollerats</span><span class="sxs-lookup"><span data-stu-id="2d45d-540">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="2d45d-541">Korrigera bugg i Concat</span><span class="sxs-lookup"><span data-stu-id="2d45d-541">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="2d45d-542">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="2d45d-542">Az.FrontDoor</span></span>
* <span data-ttu-id="2d45d-543">Åtgärdade diverse stavfel i modul</span><span class="sxs-lookup"><span data-stu-id="2d45d-543">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="2d45d-544">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="2d45d-544">Az.HDInsight</span></span>
* <span data-ttu-id="2d45d-545">Korrigerade buggen att kunder får felet ”inte en giltig Base-64-sträng” vid användning av Get-AzHDInsightCluster för att hämta klustret med ADLSGen1-lagring.</span><span class="sxs-lookup"><span data-stu-id="2d45d-545">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="2d45d-546">Lägg till en parameter med namnet ”ApplicationId” i de tre cmdletarna Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig och New-AzHDInsightCluster så att kunden kan tillhandahålla tjänstens huvudnamn för program-ID för åtkomst till Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="2d45d-546">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="2d45d-547">Ändrade Microsoft.Azure.Management.HDInsight från 2.1.0 till 5.1.0</span><span class="sxs-lookup"><span data-stu-id="2d45d-547">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="2d45d-548">Fem cmdletar har tagits bort:</span><span class="sxs-lookup"><span data-stu-id="2d45d-548">Removed five cmdlets:</span></span>
    - <span data-ttu-id="2d45d-549">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="2d45d-549">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="2d45d-550">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="2d45d-550">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="2d45d-551">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="2d45d-551">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="2d45d-552">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="2d45d-552">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="2d45d-553">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="2d45d-553">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="2d45d-554">Tre cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="2d45d-554">Added three cmdlets:</span></span>
    - <span data-ttu-id="2d45d-555">Get-AzHDInsightMonitoring som ersätter Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="2d45d-555">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="2d45d-556">Enable-AzHDInsightMonitoring som ersätter Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="2d45d-556">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="2d45d-557">Disable-AzHDInsightMonitoring som ersätter Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="2d45d-557">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="2d45d-558">Korrigerade cmdleten Get-AzHDInsightProperties för att stödja hämtning av funktionsinformation från en viss plats.</span><span class="sxs-lookup"><span data-stu-id="2d45d-558">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="2d45d-559">Parameteruppsättningarna (Spark1 och Spark2) har tagits bort från Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="2d45d-559">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="2d45d-560">Lägg till exempel för cmdleten Add-AzHDInsightSecurityProfile till hjälpdokumenten.</span><span class="sxs-lookup"><span data-stu-id="2d45d-560">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="2d45d-561">Ändrade utdatatyp för följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="2d45d-561">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="2d45d-562">Ändrade utdatatyp för Get-AzHDInsightProperties från CapabilitiesResponse till AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="2d45d-562">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="2d45d-563">Ändrade utdatatyp för Remove-AzHDInsightCluster från ClusterGetResponse till bool.</span><span class="sxs-lookup"><span data-stu-id="2d45d-563">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="2d45d-564">Ändrade utdatatyp för Set-AzHDInsightGatewaySettings HttpConnectivitySettings till GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="2d45d-564">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="2d45d-565">Lade till testfall för vissa scenarier.</span><span class="sxs-lookup"><span data-stu-id="2d45d-565">Added some scenario test cases.</span></span>
* <span data-ttu-id="2d45d-566">Ta bort vissa alias: Add-AzHDInsightConfigValues, Get-AzHDInsightProperties.</span><span class="sxs-lookup"><span data-stu-id="2d45d-566">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="2d45d-567">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="2d45d-567">Az.IotHub</span></span>
* <span data-ttu-id="2d45d-568">Icke-bakåtkompatibla ändringar:</span><span class="sxs-lookup"><span data-stu-id="2d45d-568">Breaking changes:</span></span>
    - <span data-ttu-id="2d45d-569">Cmdleten Add-AzIotHubEventHubConsumerGroup har inte längre stöd för parametern EventHubEndpointName och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="2d45d-569">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="2d45d-570">Parameteruppsättningen __AllParameterSets för cmdleten Add-AzIotHubEventHubConsumerGroup har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="2d45d-570">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="2d45d-571">Cmdleten Get-AzIotHubEventHubConsumerGroup har inte längre stöd för parametern EventHubEndpointName och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="2d45d-571">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="2d45d-572">Parameteruppsättningen __AllParameterSets för cmdleten Get-AzIotHubEventHubConsumerGroup har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="2d45d-572">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="2d45d-573">Egenskapen OperationsMonitoringProperties av typen Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="2d45d-573">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="2d45d-574">Egenskapen OperationsMonitoringProperties av typen Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="2d45d-574">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="2d45d-575">Cmdleten New-AzIotHubExportDevice stöder inte längre aliaset New-AzIotHubExportDevices.</span><span class="sxs-lookup"><span data-stu-id="2d45d-575">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="2d45d-576">Cmdleten New-AzIotHubImportDevice stöder inte längre aliaset New-AzIotHubImportDevices.</span><span class="sxs-lookup"><span data-stu-id="2d45d-576">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="2d45d-577">Cmdleten Remove-AzIotHubEventHubConsumerGroup har inte längre stöd för parametern EventHubEndpointName och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="2d45d-577">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="2d45d-578">Parameteruppsättningen __AllParameterSets för cmdleten Remove-AzIotHubEventHubConsumerGroup har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="2d45d-578">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="2d45d-579">Cmdleten Set-AzIotHub har inte längre stöd för parametern OperationsMonitoringProperties och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="2d45d-579">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="2d45d-580">Parameteruppsättningen UpdateOperationsMonitoringProperties för cmdleten Set-AzIotHub har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="2d45d-580">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2d45d-581">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d45d-581">Az.RecoveryServices</span></span>
* <span data-ttu-id="2d45d-582">Azure Site Recovery-stöd för att konfigurera nätverksresurser som NSG, offentliga IP-adresser och interna lastbalanserare för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="2d45d-582">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="2d45d-583">Azure Site Recovery-stöd för att skriva till hanterad disk för vMWare till Azure.</span><span class="sxs-lookup"><span data-stu-id="2d45d-583">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="2d45d-584">Azure Site Recovery-stöd för NIC-reduktion för vMWare till Azure.</span><span class="sxs-lookup"><span data-stu-id="2d45d-584">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="2d45d-585">Azure Site Recovery-stöd för accelererat nätverk för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="2d45d-585">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="2d45d-586">Azure Site Recovery-stöd för automatisk uppdatering av agent för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="2d45d-586">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="2d45d-587">Azure Site Recovery-stöd för Standard SSD för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="2d45d-587">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="2d45d-588">Azure Site Recovery-stöd för tvåstegskryptering i Azure Disk Encryption för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="2d45d-588">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="2d45d-589">Azure Site Recovery-stöd för att skydda nyligen tillagda diskar för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="2d45d-589">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="2d45d-590">En funktion för mjuk borttagning av virtuella datorer samt tester för mjuk borttagning har tagits bort</span><span class="sxs-lookup"><span data-stu-id="2d45d-590">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d45d-591">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d45d-591">Az.Resources</span></span>
* <span data-ttu-id="2d45d-592">Uppdatera beroendesammansättning för Microsoft.Extensions.Caching.Memory från 1.1.1 till 2.2</span><span class="sxs-lookup"><span data-stu-id="2d45d-592">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d45d-593">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d45d-593">Az.Network</span></span>
* <span data-ttu-id="2d45d-594">Ändra alla cmdletar för PrivateEndpointConnection så att de stöder generiska tjänstleverantörer.</span><span class="sxs-lookup"><span data-stu-id="2d45d-594">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="2d45d-595">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="2d45d-595">Updated cmdlet:</span></span>
        - <span data-ttu-id="2d45d-596">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2d45d-596">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="2d45d-597">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2d45d-597">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="2d45d-598">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2d45d-598">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="2d45d-599">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2d45d-599">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="2d45d-600">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2d45d-600">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="2d45d-601">Lägg till ny cmdlet för PrivateLinkResource så att det också stöder generiska tjänstleverantörer.</span><span class="sxs-lookup"><span data-stu-id="2d45d-601">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="2d45d-602">Ny cmdlet:</span><span class="sxs-lookup"><span data-stu-id="2d45d-602">New cmdlet:</span></span>
        - <span data-ttu-id="2d45d-603">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="2d45d-603">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="2d45d-604">Lägg till nya fält och parametrar för funktionen Proxy Protocol V2.</span><span class="sxs-lookup"><span data-stu-id="2d45d-604">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="2d45d-605">Lägg till egenskapen EnableProxyProtocol i PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="2d45d-605">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="2d45d-606">Lägg till egenskapen LinkIdentifier i PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2d45d-606">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="2d45d-607">Uppdaterade New-AzPrivateLinkService för att lägga till den nya valfria parametern EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="2d45d-607">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="2d45d-608">Korrigera felaktig beskrivning av parameter i referensdokumentationen för New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="2d45d-608">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="2d45d-609">Nya cmdletar som stöder Azure-brandväggsprincipen</span><span class="sxs-lookup"><span data-stu-id="2d45d-609">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="2d45d-610">Lägg till stöd för den underordnade resursen RouteTables för VirtualHub</span><span class="sxs-lookup"><span data-stu-id="2d45d-610">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="2d45d-611">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="2d45d-611">New cmdlets added:</span></span>
        - <span data-ttu-id="2d45d-612">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="2d45d-612">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="2d45d-613">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="2d45d-613">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="2d45d-614">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="2d45d-614">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="2d45d-615">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="2d45d-615">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="2d45d-616">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="2d45d-616">Set-AzVirtualHub</span></span>
* <span data-ttu-id="2d45d-617">Lägg till stöd för ny egenskaps-SKU för VirtualHub och VirtualWANType för VirtualWan</span><span class="sxs-lookup"><span data-stu-id="2d45d-617">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="2d45d-618">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="2d45d-618">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="2d45d-619">New-AzVirtualHub: lade till parameter-SKU</span><span class="sxs-lookup"><span data-stu-id="2d45d-619">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="2d45d-620">Update-AzVirtualHub: lade till parameter-SKU</span><span class="sxs-lookup"><span data-stu-id="2d45d-620">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="2d45d-621">New-AzVirtualWan: lade till parametern VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="2d45d-621">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="2d45d-622">Update-AzVirtualWan: lade till parametern VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="2d45d-622">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="2d45d-623">Lägg till stöd för egenskapen EnableInternetSecurity för HubVnetConnection, VpnConnection och ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="2d45d-623">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="2d45d-624">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="2d45d-624">New cmdlets added:</span></span>
        - <span data-ttu-id="2d45d-625">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="2d45d-625">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="2d45d-626">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="2d45d-626">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="2d45d-627">New-AzureRmVirtualHubVnetConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="2d45d-627">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="2d45d-628">New-AzureRmVpnConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="2d45d-628">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="2d45d-629">Update-AzureRmVpnConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="2d45d-629">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="2d45d-630">New-AzureRmExpressRouteConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="2d45d-630">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="2d45d-631">Set-AzureRmExpressRouteConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="2d45d-631">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="2d45d-632">Lägg till stöd för att konfigurera TopLevel WebApplicationFirewall-princip</span><span class="sxs-lookup"><span data-stu-id="2d45d-632">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="2d45d-633">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="2d45d-633">New cmdlets added:</span></span>
        - <span data-ttu-id="2d45d-634">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="2d45d-634">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="2d45d-635">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="2d45d-635">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="2d45d-636">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="2d45d-636">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="2d45d-637">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="2d45d-637">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="2d45d-638">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="2d45d-638">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="2d45d-639">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="2d45d-639">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="2d45d-640">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="2d45d-640">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="2d45d-641">New-AzApplicationGatewayFirewallPolicy: parametrarna PolicySetting, ManagedRule har lagts till</span><span class="sxs-lookup"><span data-stu-id="2d45d-641">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="2d45d-642">Stöd för operator för geomatchning har lagts till på CustomRule</span><span class="sxs-lookup"><span data-stu-id="2d45d-642">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="2d45d-643">Geomatchning har lagts till i operatorn på FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="2d45d-643">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="2d45d-644">Stöd har lagts till för brandväggsprinciperna perListener och perSite</span><span class="sxs-lookup"><span data-stu-id="2d45d-644">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="2d45d-645">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="2d45d-645">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="2d45d-646">New-AzApplicationGatewayHttpListener: parametrarna FirewallPolicy, FirewallPolicyId har lagts till</span><span class="sxs-lookup"><span data-stu-id="2d45d-646">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="2d45d-647">New-AzApplicationGatewayPathRuleConfig: parametrarna FirewallPolicy, FirewallPolicyId har lagts till</span><span class="sxs-lookup"><span data-stu-id="2d45d-647">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="2d45d-648">Åtgärdat så att nödvändigt undernät med namnet AzureBastionSubnet i PSBastion kan vara skiftlägesokänsligt</span><span class="sxs-lookup"><span data-stu-id="2d45d-648">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="2d45d-649">Stöd för mål-FQDN:er i nätverksregler och översatt FQDN i NAT-regler för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="2d45d-649">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="2d45d-650">Lägg till stöd för resursen RouteTables för IpGroup på den högsta nivån</span><span class="sxs-lookup"><span data-stu-id="2d45d-650">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="2d45d-651">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="2d45d-651">New cmdlets added:</span></span>
        - <span data-ttu-id="2d45d-652">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="2d45d-652">New-AzIpGroup</span></span>
        - <span data-ttu-id="2d45d-653">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="2d45d-653">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="2d45d-654">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="2d45d-654">Get-AzIpGroup</span></span>
        - <span data-ttu-id="2d45d-655">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="2d45d-655">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="2d45d-656">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2d45d-656">Az.ServiceFabric</span></span>
* <span data-ttu-id="2d45d-657">Ta bort cmdleten Add-AzServiceFabricApplicationCertificate eftersom det här scenariot omfattas av Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="2d45d-657">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d45d-658">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d45d-658">Az.Sql</span></span>
* <span data-ttu-id="2d45d-659">Stöd har lagts till för återställning av utelämnade databaser på hanterade instanser.</span><span class="sxs-lookup"><span data-stu-id="2d45d-659">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="2d45d-660">Inaktuella gamla cmdletar för granskning från kod.</span><span class="sxs-lookup"><span data-stu-id="2d45d-660">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="2d45d-661">Tog bort inaktuella alias:</span><span class="sxs-lookup"><span data-stu-id="2d45d-661">Removed deprecated aliases:</span></span>
* <span data-ttu-id="2d45d-662">Get-AzSqlDatabaseIndexRecommendations (använd Get-AzSqlDatabaseIndexRecommendation istället)</span><span class="sxs-lookup"><span data-stu-id="2d45d-662">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="2d45d-663">Get-AzSqlDatabaseRestorePoints (använd Get-AzSqlDatabaseRestorePoint istället)</span><span class="sxs-lookup"><span data-stu-id="2d45d-663">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="2d45d-664">Ta bort cmdleten Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="2d45d-664">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="2d45d-665">Ta bort alias för inaktuella cmdletar för inställningar för utvärdering av säkerhetsrisk</span><span class="sxs-lookup"><span data-stu-id="2d45d-665">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="2d45d-666">Inaktualisera cmdletar för inställningar för avancerad hotidentifiering</span><span class="sxs-lookup"><span data-stu-id="2d45d-666">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="2d45d-667">Lägga till cmdletar för att inaktivera och aktivera känslighetsrekommendationer på kolumner i en databas.</span><span class="sxs-lookup"><span data-stu-id="2d45d-667">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2d45d-668">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d45d-668">Az.Storage</span></span>
* <span data-ttu-id="2d45d-669">Stöd för att aktivera stora filresurser vid skapande eller uppdatering av lagringskonto</span><span class="sxs-lookup"><span data-stu-id="2d45d-669">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="2d45d-670">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2d45d-670">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="2d45d-671">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2d45d-671">Set-AzStorageAccount</span></span>
* <span data-ttu-id="2d45d-672">När du stänger/hämtar en filreferens kan du hoppa över kontrollen av huruvida indatasökvägen är en filkatalog eller en fil för att undvika problem med objekt som har status DeletePending</span><span class="sxs-lookup"><span data-stu-id="2d45d-672">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="2d45d-673">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="2d45d-673">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="2d45d-674">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="2d45d-674">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="2d45d-675">2.8.0 – oktober 2019</span><span class="sxs-lookup"><span data-stu-id="2d45d-675">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="2d45d-676">Allmänt</span><span class="sxs-lookup"><span data-stu-id="2d45d-676">General</span></span>
* <span data-ttu-id="2d45d-677">AZ. HealthcareApis 1.0.0-version</span><span class="sxs-lookup"><span data-stu-id="2d45d-677">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="2d45d-678">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d45d-678">Az.Accounts</span></span>
* <span data-ttu-id="2d45d-679">Uppdatera telemetri och URL-omskrivning för genererade moduler, korrigera Windows-enhetstester.</span><span class="sxs-lookup"><span data-stu-id="2d45d-679">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="2d45d-680">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2d45d-680">Az.ApiManagement</span></span>
* <span data-ttu-id="2d45d-681">**Set-AzApiManagementApi** – Tillagt stöd för att uppdatera Api till ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="2d45d-681">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="2d45d-682">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="2d45d-682">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2d45d-683">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2d45d-683">Az.Automation</span></span>
* <span data-ttu-id="2d45d-684">Åtgärdade cmdleten New-AzureAutomationSoftwareUpdateConfiguration för parametern för inställning av Linux-omstart.</span><span class="sxs-lookup"><span data-stu-id="2d45d-684">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="2d45d-685">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="2d45d-685">Az.Batch</span></span>
* <span data-ttu-id="2d45d-686">**Get-AzBatchNodeAgentSku** är inaktuell och ersätts av **Get-AzBatchSupportImage** i version 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="2d45d-686">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d45d-687">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d45d-687">Az.Compute</span></span>
* <span data-ttu-id="2d45d-688">Lägg till parametrarna Priority, EvictionPolicy och MaxPrice till cmdletarna New-AzVM och New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="2d45d-688">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="2d45d-689">Korrigera varningsmeddelande och hjälpdokument för cmdletarna Add-AzVMAdditionalUnattendContent och Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="2d45d-689">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="2d45d-690">Åtgärda – skipVmBackup-undantag för virtuella Linux-datorer med hanterade diskar för Set-AzVMDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="2d45d-690">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="2d45d-691">Åtgärda fel i uppdatera krypteringsinställningarna i set-AzVMDiskEncryptionExtension, scenario i två steg.</span><span class="sxs-lookup"><span data-stu-id="2d45d-691">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2d45d-692">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2d45d-692">Az.DataFactory</span></span>
* <span data-ttu-id="2d45d-693">Lägga till CRUD-kommandon för ADF V2-dataflödet: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow och Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="2d45d-693">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="2d45d-694">Lägger till åtgärdskommandon för ADF V2-dataflödesfelsökningssession: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand och Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="2d45d-694">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="2d45d-695">Uppdatera ADF .Net SDK-versionen till 4.2.0</span><span class="sxs-lookup"><span data-stu-id="2d45d-695">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2d45d-696">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2d45d-696">Az.DataLakeStore</span></span>
* <span data-ttu-id="2d45d-697">Korrigera kontovalidering så att konton med ”-” kan skickas utan domän</span><span class="sxs-lookup"><span data-stu-id="2d45d-697">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="2d45d-698">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="2d45d-698">Az.HealthcareApis</span></span>
* <span data-ttu-id="2d45d-699">PowerShell-versionen har uppdaterats till 1.0.0</span><span class="sxs-lookup"><span data-stu-id="2d45d-699">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="2d45d-700">Uppdaterade SDK-versionen till 1.0.2</span><span class="sxs-lookup"><span data-stu-id="2d45d-700">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="2d45d-701">Uppdatera i tester för att referera till en ny SDK-version</span><span class="sxs-lookup"><span data-stu-id="2d45d-701">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="2d45d-702">Utdatastrukturen har uppdaterats från kapslad till förenklad.</span><span class="sxs-lookup"><span data-stu-id="2d45d-702">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="2d45d-703">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="2d45d-703">Az.IotHub</span></span>
* <span data-ttu-id="2d45d-704">Lägg till ny routningskälla: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="2d45d-704">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="2d45d-705">Mindre felkorrigering: Get-AzIothub returnerar inte subscriptionId</span><span class="sxs-lookup"><span data-stu-id="2d45d-705">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2d45d-706">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2d45d-706">Az.Monitor</span></span>
* <span data-ttu-id="2d45d-707">Nya åtgärdsgruppsmottagare har lagts till för åtgärdsgrupp   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="2d45d-707">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="2d45d-708">Använd vanligt aviseringsschema som är aktiverat för mottagarna.</span><span class="sxs-lookup"><span data-stu-id="2d45d-708">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="2d45d-709">Detta gäller inte för SMS, push för Azure-app, ITSM och röstmottagare</span><span class="sxs-lookup"><span data-stu-id="2d45d-709">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="2d45d-710">Webhooks har nu stöd för Azure Active Directory-autentisering.</span><span class="sxs-lookup"><span data-stu-id="2d45d-710">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d45d-711">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d45d-711">Az.Network</span></span>
* <span data-ttu-id="2d45d-712">Lägg till ny cmdlet Get-AzAvailableServiceAlias som kan anropas för att hämta de alias som kan användas för tjänstslutpunktsprinciper.</span><span class="sxs-lookup"><span data-stu-id="2d45d-712">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="2d45d-713">Stöd för tillägg av trafikväljare har lagts till i gatewayanslutningar för virtuella nätverk</span><span class="sxs-lookup"><span data-stu-id="2d45d-713">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="2d45d-714">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="2d45d-714">New cmdlets added:</span></span>
        - <span data-ttu-id="2d45d-715">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="2d45d-715">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="2d45d-716">Cmdletar har uppdaterats med valfri parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="2d45d-716">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="2d45d-717">Lägg till stöd för ESP- och AH-protokoll i konfiguration av nätverkssäkerhetsregler</span><span class="sxs-lookup"><span data-stu-id="2d45d-717">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="2d45d-718">Uppdaterade cmdletar:</span><span class="sxs-lookup"><span data-stu-id="2d45d-718">Updated cmdlets:</span></span>
        - <span data-ttu-id="2d45d-719">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2d45d-719">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="2d45d-720">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2d45d-720">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="2d45d-721">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2d45d-721">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="2d45d-722">Förbättra hanteringen av undantag i Cortex-cmdletar</span><span class="sxs-lookup"><span data-stu-id="2d45d-722">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="2d45d-723">Nya generationer och SKU:er för VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="2d45d-723">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="2d45d-724">Introducera nya generationer för VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="2d45d-724">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="2d45d-725">Introducera nya SKU:er med högt dataflöde för VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="2d45d-725">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="2d45d-726">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="2d45d-726">Az.RedisCache</span></span>
* <span data-ttu-id="2d45d-727">Uppdaterad referensdokumentation för ”set-AzRedisCache” för att inkludera saknade värden för parametern ”size”</span><span class="sxs-lookup"><span data-stu-id="2d45d-727">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d45d-728">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d45d-728">Az.Sql</span></span>
* <span data-ttu-id="2d45d-729">Lägg till stöd för inställningen Active Directory administratör på den hanterade instansen</span><span class="sxs-lookup"><span data-stu-id="2d45d-729">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2d45d-730">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d45d-730">Az.Storage</span></span>
* <span data-ttu-id="2d45d-731">Uppdatera Lagringsklientbibliotek till 11.1.0</span><span class="sxs-lookup"><span data-stu-id="2d45d-731">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="2d45d-732">Lista containrar med hanteringsplans-API, kommer att listas med NextPageLink</span><span class="sxs-lookup"><span data-stu-id="2d45d-732">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="2d45d-733">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="2d45d-733">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="2d45d-734">Lista lagringskonton från prenumerationen, kommer att listas med NextPageLink</span><span class="sxs-lookup"><span data-stu-id="2d45d-734">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="2d45d-735">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2d45d-735">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="2d45d-736">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="2d45d-736">Az.StorageSync</span></span>
* <span data-ttu-id="2d45d-737">Åtgärda problemet 9810 i Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="2d45d-737">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2d45d-738">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2d45d-738">Az.Websites</span></span>
* <span data-ttu-id="2d45d-739">Set-AzWebApp – uppdatering av ASP för en app misslyckades</span><span class="sxs-lookup"><span data-stu-id="2d45d-739">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="2d45d-740">2.7.0 – september 2019</span><span class="sxs-lookup"><span data-stu-id="2d45d-740">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="2d45d-741">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2d45d-741">Az.ApiManagement</span></span>
* <span data-ttu-id="2d45d-742">Uppdatera ”-Format”-parameterbeskrivningen i ”Set-AzApiManagementPolicy”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="2d45d-742">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="2d45d-743">Referenser för den föråldrade cmdleten ”Update-AzApiManagementDeployment” har tagits bort från referensdokumentationen.</span><span class="sxs-lookup"><span data-stu-id="2d45d-743">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="2d45d-744">Använd ”Set-AzApiManagement” i stället.</span><span class="sxs-lookup"><span data-stu-id="2d45d-744">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2d45d-745">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2d45d-745">Az.Automation</span></span>
* <span data-ttu-id="2d45d-746">Stavfel har korrigerats i exempel i referensdokumentationen för ”Register-AzAutomationDscNode”</span><span class="sxs-lookup"><span data-stu-id="2d45d-746">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="2d45d-747">Klargörande har lagts till om OS-begränsningar för Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="2d45d-747">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="2d45d-748">Null-referensundantag har korrigerats för -Wait-alternativet i Start-AzAutomationRunbook-cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2d45d-748">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d45d-749">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d45d-749">Az.Compute</span></span>
* <span data-ttu-id="2d45d-750">Lägg till UploadSizeInBytes-parameter till New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="2d45d-750">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="2d45d-751">Lägg till Incremental-parameter till New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="2d45d-751">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="2d45d-752">Lägg till en funktion för virtuella datorer med låg prioritet:</span><span class="sxs-lookup"><span data-stu-id="2d45d-752">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="2d45d-753">MaxPrice-, EvictionPolicy- och Priority-parametrar har lagts till i New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="2d45d-753">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="2d45d-754">MaxPrice-parametern har lagts till i New-AzVmssConfig-, Update-AzVM- och Update-AzVmss-cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="2d45d-754">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="2d45d-755">Åtgärda problem med VM-referenser för Get-AzAvailabilitySet-cmdleten när alla tillgänglighetsuppsättningar i prenumerationen visas.</span><span class="sxs-lookup"><span data-stu-id="2d45d-755">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="2d45d-756">Korrigera null-undantaget för Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="2d45d-756">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="2d45d-757">Korrigera VHD-metoden för sökning relativt till slut.</span><span class="sxs-lookup"><span data-stu-id="2d45d-757">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="2d45d-758">Åtgärda UltraSSD-problem för New-AzVM och Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="2d45d-758">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2d45d-759">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2d45d-759">Az.DataFactory</span></span>
* <span data-ttu-id="2d45d-760">Lägger till 3 nya kommandon för ADF V2 – Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription och Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="2d45d-760">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="2d45d-761">ADF .Net SDK har uppdaterats till 4.1.3</span><span class="sxs-lookup"><span data-stu-id="2d45d-761">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="2d45d-762">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="2d45d-762">Az.HDInsight</span></span>
* <span data-ttu-id="2d45d-763">Anrop för icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="2d45d-763">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="2d45d-764">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="2d45d-764">Az.IotHub</span></span>
* <span data-ttu-id="2d45d-765">Lägg till stöd för att anropa redundans för en IotHub till den geo-länkade katastrofåterställningsregionen.</span><span class="sxs-lookup"><span data-stu-id="2d45d-765">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="2d45d-766">Lägg till stöd för att hantera meddelandeberikning för en IotHub.</span><span class="sxs-lookup"><span data-stu-id="2d45d-766">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="2d45d-767">Nya cmdlet:ar är:</span><span class="sxs-lookup"><span data-stu-id="2d45d-767">New cmdlets are:</span></span>
    - <span data-ttu-id="2d45d-768">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="2d45d-768">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="2d45d-769">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="2d45d-769">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="2d45d-770">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="2d45d-770">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="2d45d-771">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="2d45d-771">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2d45d-772">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2d45d-772">Az.Monitor</span></span>
* <span data-ttu-id="2d45d-773">Pekar på den senaste Monitor SDK:n, dvs. 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="2d45d-773">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="2d45d-774">Lägger till bakåtkompatibla ändringar i Metrics-cmdletarna, dvs. enhetsuppräkningen stöder flera nya värden.</span><span class="sxs-lookup"><span data-stu-id="2d45d-774">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="2d45d-775">Detta är skrivskyddade cmdletar, så det förekommer inga ändringar i inmatningen för cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="2d45d-775">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="2d45d-776">API-versionen för **ActionGroups**-begäranden är nu **2019-06-01**. Tidigare var den **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="2d45d-776">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="2d45d-777">Test av scenarier har uppdaterats för att anpassas till den här ändringen.</span><span class="sxs-lookup"><span data-stu-id="2d45d-777">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="2d45d-778">Ett nytt obligatoriskt argument har lagts till för konstruktorerna för klasserna **EmailReceiver** och **WebhookReceiver** – ett booleskt värde med namnet **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="2d45d-778">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="2d45d-779">Värdet är för närvarande fast till **false** så att den här icke-bakåtkompatibla ändringen är dold från cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="2d45d-779">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="2d45d-780">**Obs!** Det här är en tillfällig ändring som måste verifieras av Alerts-teamet.</span><span class="sxs-lookup"><span data-stu-id="2d45d-780">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="2d45d-781">Ordningen på argumenten för konstruktorn för klassen **Source** (relaterad till klassen **ScheduledQueryRuleSource**) har ändrats från den tidigare SDK:n.</span><span class="sxs-lookup"><span data-stu-id="2d45d-781">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="2d45d-782">Den här ändringen krävde korrigering av två enhetstest: de kompilerades, men testerna skickades inte.</span><span class="sxs-lookup"><span data-stu-id="2d45d-782">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="2d45d-783">Ordningen på argumenten för konstruktorn för klassen **AlertingAction** (relaterad till klassen **ScheduledQueryRuleSource**) har ändrats från den tidigare SDK:n.</span><span class="sxs-lookup"><span data-stu-id="2d45d-783">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="2d45d-784">Den här ändringen krävde korrigering av två enhetstest: de kompilerades, men testerna skickades inte.</span><span class="sxs-lookup"><span data-stu-id="2d45d-784">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="2d45d-785">Stöd för kriterier för dynamiskt tröskelvärde för måttavisering v2</span><span class="sxs-lookup"><span data-stu-id="2d45d-785">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="2d45d-786">New-AzMetricAlertRuleV2Criteria: skapar nu även kriterier för dynamiskt tröskelvärde</span><span class="sxs-lookup"><span data-stu-id="2d45d-786">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="2d45d-787">Add-AzMetricAlertRuleV2: accepterar nu även kriterier för dynamiskt tröskelvärde</span><span class="sxs-lookup"><span data-stu-id="2d45d-787">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="2d45d-788">Förbättringar i schemalagd frågeregel (SQR)</span><span class="sxs-lookup"><span data-stu-id="2d45d-788">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="2d45d-789">Cmdletar accepterar ”Location”-parameter i båda formaten, antingen platsen (t.ex. eastus) eller platsens visningsnamn (t.ex. USA, östra)</span><span class="sxs-lookup"><span data-stu-id="2d45d-789">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="2d45d-790">”Enabled”-parametern illustreras korrekt i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="2d45d-790">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="2d45d-791">Exempel för den valfria parametern ”ActionGroup” har lagts till</span><span class="sxs-lookup"><span data-stu-id="2d45d-791">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="2d45d-792">Förbättrade hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="2d45d-792">Overall improved help files</span></span>
* <span data-ttu-id="2d45d-793">Åtgärda bugg då omfattningstypen fastställs för ”Set-AzActionRule”</span><span class="sxs-lookup"><span data-stu-id="2d45d-793">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d45d-794">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d45d-794">Az.Network</span></span>
* <span data-ttu-id="2d45d-795">Korrigera felaktigt exempel i referensdokumentationen för ”New-AzApplicationGateway”</span><span class="sxs-lookup"><span data-stu-id="2d45d-795">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="2d45d-796">Lägg till anmärkning i ”Get-AzNetworkWatcherPacketCapture”-referensdokumentationen om hämtning av alla egenskaper för en paketinsamling</span><span class="sxs-lookup"><span data-stu-id="2d45d-796">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="2d45d-797">Exempel har korrigerats i ”Test-AzNetworkWatcherIPFlow”-referensdokumentationen för korrekt uppräkning av nätverkskort</span><span class="sxs-lookup"><span data-stu-id="2d45d-797">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="2d45d-798">Förbättrad tolkning av molnundantag för att visa eventuell ytterligare information</span><span class="sxs-lookup"><span data-stu-id="2d45d-798">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="2d45d-799">Förbättrad tolkning av molnundantag för att hantera ytterligare en typ av SDK-undantag</span><span class="sxs-lookup"><span data-stu-id="2d45d-799">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="2d45d-800">Felaktig mappning av säkerhetsregelmodeller har korrigerats</span><span class="sxs-lookup"><span data-stu-id="2d45d-800">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="2d45d-801">Egenskaper har lagts till för nätverksgränssnittet för funktionen Privat IP</span><span class="sxs-lookup"><span data-stu-id="2d45d-801">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="2d45d-802">Egenskapen ”PrivateEndpoint” har lagts till som en typ av PSResourceId till PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="2d45d-802">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="2d45d-803">Egenskapen ”PrivateLinkConnectionProperties” har lagts till som en typ av PSIpConfigurationConnectivityInformation till PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="2d45d-803">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="2d45d-804">Modellklassen PSIpConfigurationConnectivityInformation har lagts till</span><span class="sxs-lookup"><span data-stu-id="2d45d-804">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="2d45d-805">ApplicationRuleProtocolType ”mssql” har lagts till för Azure Firewall-resurs</span><span class="sxs-lookup"><span data-stu-id="2d45d-805">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="2d45d-806">MultiLink-stöd i virtuellt WAN</span><span class="sxs-lookup"><span data-stu-id="2d45d-806">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="2d45d-807">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="2d45d-807">New cmdlets</span></span>
        - <span data-ttu-id="2d45d-808">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="2d45d-808">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="2d45d-809">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="2d45d-809">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="2d45d-810">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="2d45d-810">Updated cmdlet:</span></span>
        - <span data-ttu-id="2d45d-811">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="2d45d-811">New-VpnSite</span></span>
        - <span data-ttu-id="2d45d-812">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="2d45d-812">Update-VpnSite</span></span>
        - <span data-ttu-id="2d45d-813">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="2d45d-813">New-VpnConnection</span></span>
        - <span data-ttu-id="2d45d-814">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="2d45d-814">Update-VpnConnection</span></span>
* <span data-ttu-id="2d45d-815">Dokument för vissa PowerShell-exempel har korrigerats så att Az-cmdletar används i stället för AzureRM-cmdletar</span><span class="sxs-lookup"><span data-stu-id="2d45d-815">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2d45d-816">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d45d-816">Az.RecoveryServices</span></span>
* <span data-ttu-id="2d45d-817">Uppdatera AzureVMpolicy-objekt med ProtectedItemsCount-attribut</span><span class="sxs-lookup"><span data-stu-id="2d45d-817">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="2d45d-818">Ytterligare tester har lagts till för VM-princip och återställning av ursprungligt lagringskonto</span><span class="sxs-lookup"><span data-stu-id="2d45d-818">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d45d-819">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d45d-819">Az.Resources</span></span>
* <span data-ttu-id="2d45d-820">Åtgärda fel där det inte gick att anropa New-AzRoleAssignment utan parametern Scope.</span><span class="sxs-lookup"><span data-stu-id="2d45d-820">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="2d45d-821">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2d45d-821">Az.ServiceFabric</span></span>
* <span data-ttu-id="2d45d-822">Stavfel har korrigerats i exempel för ”Update-AzServiceFabricReliability”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="2d45d-822">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="2d45d-823">Lägger till nya cmdletar för att hantera program och tjänster:</span><span class="sxs-lookup"><span data-stu-id="2d45d-823">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="2d45d-824">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="2d45d-824">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="2d45d-825">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="2d45d-825">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="2d45d-826">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="2d45d-826">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="2d45d-827">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="2d45d-827">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="2d45d-828">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="2d45d-828">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="2d45d-829">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="2d45d-829">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="2d45d-830">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="2d45d-830">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="2d45d-831">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="2d45d-831">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="2d45d-832">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="2d45d-832">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="2d45d-833">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="2d45d-833">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="2d45d-834">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="2d45d-834">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="2d45d-835">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="2d45d-835">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="2d45d-836">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="2d45d-836">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="2d45d-837">Service Fabric SDK har uppgraderats till version 1.2.0 som använder Service Fabric-resursprovidern med API-version 2019-03-01.</span><span class="sxs-lookup"><span data-stu-id="2d45d-837">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="2d45d-838">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="2d45d-838">Az.SignalR</span></span>
* <span data-ttu-id="2d45d-839">Lägg till Update-, Restart-, CheckNameAvailability- och GetUsage-cmdletar</span><span class="sxs-lookup"><span data-stu-id="2d45d-839">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d45d-840">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d45d-840">Az.Sql</span></span>
* <span data-ttu-id="2d45d-841">Uppdatera exempel i referensdokumentationen för ”Get-AzSqlElasticPool”</span><span class="sxs-lookup"><span data-stu-id="2d45d-841">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="2d45d-842">vCore-exempel för att skapa en elastisk pool (New-AzSqlElasticPool) har lagts till.</span><span class="sxs-lookup"><span data-stu-id="2d45d-842">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="2d45d-843">Ta bort verifieringen av EmailAddresses och kontrollen som bekräftar att EmailAdmins inte är falskt när EmailAddresses är tomt i Set-AzSqlServerAdvancedThreatProtectionPolicy och Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="2d45d-843">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="2d45d-844">Server-/databasgranskningsinställningar kan tas bort när det finns flera diagnostikinställningar som aktiverar granskningskategorin.</span><span class="sxs-lookup"><span data-stu-id="2d45d-844">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="2d45d-845">Åtgärda verifiering av e-postadresser i flera Sql Vulnerability Assessment-cmdletar (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting och Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="2d45d-845">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2d45d-846">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d45d-846">Az.Storage</span></span>
* <span data-ttu-id="2d45d-847">Exempel i referensdokumentationen för ”Get-AzStorageAccountKey” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="2d45d-847">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="2d45d-848">Vid upp- och nedladdning av en Azure-fil kan SMB-egenskaperna för källfilen (t.ex. filattribut, tidpunkten då filen skapades och tidpunkten för den senaste skrivningen) sparas i målfilen</span><span class="sxs-lookup"><span data-stu-id="2d45d-848">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="2d45d-849">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="2d45d-849">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="2d45d-850">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="2d45d-850">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="2d45d-851">Korrigera problem med uppladdningen av blockblob med egenskaper/metadata för ImmutabilityPolicy i containrar.</span><span class="sxs-lookup"><span data-stu-id="2d45d-851">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="2d45d-852">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="2d45d-852">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="2d45d-853">Stöd för hantering av Azure-filresurser med API för hanteringsplan</span><span class="sxs-lookup"><span data-stu-id="2d45d-853">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="2d45d-854">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="2d45d-854">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="2d45d-855">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="2d45d-855">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="2d45d-856">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="2d45d-856">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="2d45d-857">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="2d45d-857">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2d45d-858">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2d45d-858">Az.Websites</span></span>
* <span data-ttu-id="2d45d-859">Åtgärdar problemet där webapp-taggar togs bort när appen migrerades till nya ASP</span><span class="sxs-lookup"><span data-stu-id="2d45d-859">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="2d45d-860">Åtgärda Publish-AzureWebapp så att det fungerar i Linux och Windows</span><span class="sxs-lookup"><span data-stu-id="2d45d-860">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="2d45d-861">Uppdatera exempel i ”Get-AzWebAppPublishingProfile”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="2d45d-861">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="2d45d-862">2.6.0 – augusti 2019</span><span class="sxs-lookup"><span data-stu-id="2d45d-862">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="2d45d-863">Allmänt</span><span class="sxs-lookup"><span data-stu-id="2d45d-863">General</span></span>
* <span data-ttu-id="2d45d-864">Åtgärdade diverse skrivfel i flera moduler</span><span class="sxs-lookup"><span data-stu-id="2d45d-864">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="2d45d-865">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d45d-865">Az.Accounts</span></span>
* <span data-ttu-id="2d45d-866">Stöd för användartilldelat MSI i Azure Functions-autentisering (#9479)</span><span class="sxs-lookup"><span data-stu-id="2d45d-866">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="2d45d-867">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="2d45d-867">Az.Aks</span></span>
* <span data-ttu-id="2d45d-868">Åtgärda problem med utdata för "Get-AzAks"</span><span class="sxs-lookup"><span data-stu-id="2d45d-868">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="2d45d-869">Mer information här: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="2d45d-869">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="2d45d-870">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2d45d-870">Az.ApiManagement</span></span>
* <span data-ttu-id="2d45d-871">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="2d45d-871">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="2d45d-872">Uppdatera .net-NuGet-versionen, som inte tillämpar begränsningar för productId, apiId och userId</span><span class="sxs-lookup"><span data-stu-id="2d45d-872">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="2d45d-873">**Get-AzApiManagementProduct** – Lade till stöd för frågekörning mot produkter via API.</span><span class="sxs-lookup"><span data-stu-id="2d45d-873">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="2d45d-874">**New-AzApiManagementApiRevision** – Korrigering för problem där ApiRevisionDescription inte angavs vid skapande av ny API-revision https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="2d45d-874">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="2d45d-875">Åtgärdade skrivfel i modellen "PsApiManagementOAuth2AuthrozationServer" till "PsApiManagementOAuth2AuthorizationServer"</span><span class="sxs-lookup"><span data-stu-id="2d45d-875">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="2d45d-876">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="2d45d-876">Az.Batch</span></span>
* <span data-ttu-id="2d45d-877">Åtgärdade skrivfel i hjälpmeddelande och dokumentation till att skriva Windows med versaler</span><span class="sxs-lookup"><span data-stu-id="2d45d-877">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="2d45d-878">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="2d45d-878">Az.Cdn</span></span>
* <span data-ttu-id="2d45d-879">Åtgärdade skrivfel i CDN-modulens konverteringshjälp</span><span class="sxs-lookup"><span data-stu-id="2d45d-879">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d45d-880">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d45d-880">Az.Compute</span></span>
* <span data-ttu-id="2d45d-881">Lägg till VmssId i New-AzVMConfig-cmdleten</span><span class="sxs-lookup"><span data-stu-id="2d45d-881">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="2d45d-882">Lägg till parametrarna TerminateScheduledEvents och TerminateScheduledEventNotBeforeTimeoutInMinutes i New-AzVmssConfig och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="2d45d-882">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="2d45d-883">Lägg till egenskapen HyperVGeneration till avbildningsobjekt för virtuell dator</span><span class="sxs-lookup"><span data-stu-id="2d45d-883">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="2d45d-884">Lägg till funktioner för Host och HostGroup</span><span class="sxs-lookup"><span data-stu-id="2d45d-884">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="2d45d-885">Nya cmdletar:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="2d45d-885">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="2d45d-886">HostId-parametern läggs till i New-AzVMConfig och New-AzVM</span><span class="sxs-lookup"><span data-stu-id="2d45d-886">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="2d45d-887">Uppdatera exempel i "Invoke-AzVMRunCommand"-dokumentationen till att använda rätt parameternamn</span><span class="sxs-lookup"><span data-stu-id="2d45d-887">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="2d45d-888">Uppdatera "-VolumeType"-beskrivningen i referensdokumentationen för "set-AzVMDiskEncryptionExtension" och "set-AzVmssDiskEncryptionExtension"</span><span class="sxs-lookup"><span data-stu-id="2d45d-888">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2d45d-889">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2d45d-889">Az.DataFactory</span></span>
* <span data-ttu-id="2d45d-890">Åtgärda skrivfel till att använda versaler för "Windows" i "New-AzDataFactoryEncryptValue"-dokumentationen</span><span class="sxs-lookup"><span data-stu-id="2d45d-890">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="2d45d-891">Uppdaterade ADF .Net SDK-versionen till 4.1.2</span><span class="sxs-lookup"><span data-stu-id="2d45d-891">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="2d45d-892">Lägg till parametrarna "DataProxyIntegrationRuntimeName", "DataProxyStagingLinkedServiceName" och "DataProxyStagingPath" för "Set-AzureRmDataFactoryV2IntegrationRuntime"-cmd för att aktivera konfiguration av lokalt installerad integrationskörning som en proxy för SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="2d45d-892">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="2d45d-893">Uppdaterade PSTriggerRun till att visa utlöst pipeline, meddelande och egenskaper samt PSActivityRun till att visa aktivitetstypen</span><span class="sxs-lookup"><span data-stu-id="2d45d-893">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2d45d-894">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2d45d-894">Az.DataLakeStore</span></span>
* <span data-ttu-id="2d45d-895">Korrigering av frysning av Get-DataLakeStoreDeletedItem för fel eller fjärrundantag.</span><span class="sxs-lookup"><span data-stu-id="2d45d-895">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="2d45d-896">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="2d45d-896">Az.EventHub</span></span>
* <span data-ttu-id="2d45d-897">Korrigering av problem #9658 : Skrivfel i parametern VirtualNteworkRule i Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="2d45d-897">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="2d45d-898">Korrigering av problem #9558 : Set-AzEventHubNamespace använder PATCH i stället för PUT</span><span class="sxs-lookup"><span data-stu-id="2d45d-898">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="2d45d-899">lade till parametern EnableKafka i Set-AzEventHubNamespace-cmdleten</span><span class="sxs-lookup"><span data-stu-id="2d45d-899">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="2d45d-900">Korrigering av problem #9786 : kan inte skapa en regel med Endast lyssna-behörighet</span><span class="sxs-lookup"><span data-stu-id="2d45d-900">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="2d45d-901">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="2d45d-901">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="2d45d-902">Åtgärdade skrivfel i dokumentation där "Azure" skrevs helt med gemener</span><span class="sxs-lookup"><span data-stu-id="2d45d-902">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2d45d-903">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2d45d-903">Az.Monitor</span></span>
* <span data-ttu-id="2d45d-904">Åtgärdade felaktigt parameternamn i hjälpdokumentationen</span><span class="sxs-lookup"><span data-stu-id="2d45d-904">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d45d-905">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d45d-905">Az.Network</span></span>
* <span data-ttu-id="2d45d-906">Uppdaterade New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="2d45d-906">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="2d45d-907">Gjorde parametern "PublicIpAddress" inaktuell eftersom den aldrig används på serversidan.</span><span class="sxs-lookup"><span data-stu-id="2d45d-907">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="2d45d-908">Lade till den valfria parametern "Primary", som anger huruvida den aktuella IP-konfigurationen är den primära.</span><span class="sxs-lookup"><span data-stu-id="2d45d-908">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="2d45d-909">Förbättrade hanteringen av felundantag för begärande från SDK – åtgärdar problemet att tidigare SDK-undantag inte hanteras på rätt sätt, vilket leder till att viktig felinformation inte visas</span><span class="sxs-lookup"><span data-stu-id="2d45d-909">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="2d45d-910">Justerade valideringslogiken för IPv6-IP-prefix till att kontrollera korrekt IPv6-prefixlängd.</span><span class="sxs-lookup"><span data-stu-id="2d45d-910">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="2d45d-911">Uppdaterade Get-AzVirtualNetworkSubnetConfig: Lade till parameter som anges till get av undernätets resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="2d45d-911">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="2d45d-912">Uppdaterade beskrivningen av parametern Location för AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="2d45d-912">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="2d45d-913">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2d45d-913">Az.OperationalInsights</span></span>
* <span data-ttu-id="2d45d-914">Uppdaterade dokumentation för "New-AzOperationalInsightsLinuxSyslogDataSource"</span><span class="sxs-lookup"><span data-stu-id="2d45d-914">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="2d45d-915">Lade till exempel</span><span class="sxs-lookup"><span data-stu-id="2d45d-915">Added example</span></span>
    - <span data-ttu-id="2d45d-916">Uppdaterade beskrivningen av parametern "-Name"</span><span class="sxs-lookup"><span data-stu-id="2d45d-916">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="2d45d-917">Lade till ett exempel för New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="2d45d-917">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="2d45d-918">Ändrade beskrivningen av parametern -Name för New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="2d45d-918">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2d45d-919">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d45d-919">Az.RecoveryServices</span></span>
* <span data-ttu-id="2d45d-920">Uppdatera "Get-AzRecoveryServicesBackupJobDetail.md"</span><span class="sxs-lookup"><span data-stu-id="2d45d-920">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d45d-921">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d45d-921">Az.Resources</span></span>
* <span data-ttu-id="2d45d-922">Lägg till stöd för den nya API-versionen från 2019-05-10 för Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="2d45d-922">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="2d45d-923">Lägg till stöd för "copy.count = 0" för variabler, resurser och egenskaper</span><span class="sxs-lookup"><span data-stu-id="2d45d-923">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="2d45d-924">Resurser med "condition = false" eller "copy.count = 0" tas bort i complete-läget</span><span class="sxs-lookup"><span data-stu-id="2d45d-924">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="2d45d-925">Lägg till ett exempel på tilldelning av princip på prenumerationsnivå i hjälpdokumentationen</span><span class="sxs-lookup"><span data-stu-id="2d45d-925">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="2d45d-926">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="2d45d-926">Az.ServiceBus</span></span>
* <span data-ttu-id="2d45d-927">Korrigering av problem #9658 : Skrivfel i parametern VirtualNetworkRule i set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="2d45d-927">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="2d45d-928">Korrigering av problem #9786 : kan inte skapa en regel med Endast lyssna-behörighet</span><span class="sxs-lookup"><span data-stu-id="2d45d-928">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="2d45d-929">Lade till det nya kommandot "Test-AzServiceBusNameAvailability" för att kontrollera namntillgängligheten för kö och ämne</span><span class="sxs-lookup"><span data-stu-id="2d45d-929">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="2d45d-930">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2d45d-930">Az.ServiceFabric</span></span>
* <span data-ttu-id="2d45d-931">Åtgärda buggar med tillägg av nodtyps-cmdlet:</span><span class="sxs-lookup"><span data-stu-id="2d45d-931">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="2d45d-932">NullReferenceException-bugg när resursgrupp hade annan vmss som inte är relaterad till Service Fabric-klustret.</span><span class="sxs-lookup"><span data-stu-id="2d45d-932">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="2d45d-933">Åtgärdar problemet: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="2d45d-933">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="2d45d-934">Åtgärda bugg där cmdleten misslyckades om virtualNetwork var i en annan resursgrupp än klustret.</span><span class="sxs-lookup"><span data-stu-id="2d45d-934">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="2d45d-935">Åtgärdar problemet: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="2d45d-935">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="2d45d-936">AzServiceFabricApplicationCertificate-cmdleten görs inaktuell</span><span class="sxs-lookup"><span data-stu-id="2d45d-936">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d45d-937">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d45d-937">Az.Sql</span></span>
* <span data-ttu-id="2d45d-938">Uppdatera dokumentation om gamla gransknings-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="2d45d-938">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2d45d-939">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d45d-939">Az.Storage</span></span>
* <span data-ttu-id="2d45d-940">Uppdatera hjälpen för Get/Close-AzStorageFileHandle genom att lägga till fler scenarier i cmdlet-exempel och uppdatera parameterbeskrivningar</span><span class="sxs-lookup"><span data-stu-id="2d45d-940">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="2d45d-941">Stöd för StandardBlobTier i uppladdningsblob och kopieringsblob</span><span class="sxs-lookup"><span data-stu-id="2d45d-941">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="2d45d-942">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="2d45d-942">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="2d45d-943">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="2d45d-943">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="2d45d-944">Stöd för rehydratiseringsprioritet i kopieringsblob</span><span class="sxs-lookup"><span data-stu-id="2d45d-944">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="2d45d-945">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="2d45d-945">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2d45d-946">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2d45d-946">Az.Websites</span></span>
* <span data-ttu-id="2d45d-947">Lägg till klargöranden gällande parametern -AppSettings i Set-AzWebApp och Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2d45d-947">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="2d45d-948">2.5.0 – July 2019</span><span class="sxs-lookup"><span data-stu-id="2d45d-948">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2d45d-949">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d45d-949">Az.Accounts</span></span>
* <span data-ttu-id="2d45d-950">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="2d45d-950">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="2d45d-951">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="2d45d-951">Az.ApplicationInsights</span></span>
* <span data-ttu-id="2d45d-952">Korrigera skrivfel i exempel i dokumentationen för Remove-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="2d45d-952">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2d45d-953">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2d45d-953">Az.Automation</span></span>
* <span data-ttu-id="2d45d-954">Korrigera skrivfel i resurssträng</span><span class="sxs-lookup"><span data-stu-id="2d45d-954">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="2d45d-955">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="2d45d-955">Az.CognitiveServices</span></span>
* <span data-ttu-id="2d45d-956">Stöd för NetworkRuleSet har lagts till.</span><span class="sxs-lookup"><span data-stu-id="2d45d-956">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d45d-957">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d45d-957">Az.Compute</span></span>
* <span data-ttu-id="2d45d-958">Lägg till saknade egenskaper (ComputerName, OsName, OsVersion och HyperVGeneration) för visningsobjekt i den virtuella datorinstansen.</span><span class="sxs-lookup"><span data-stu-id="2d45d-958">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="2d45d-959">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="2d45d-959">Az.ContainerRegistry</span></span>
* <span data-ttu-id="2d45d-960">Åtgärda skrivfel i Remove-AzContainerRegistryReplication för parametern Replication</span><span class="sxs-lookup"><span data-stu-id="2d45d-960">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="2d45d-961">Mer information finns här: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="2d45d-961">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2d45d-962">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2d45d-962">Az.DataFactory</span></span>
* <span data-ttu-id="2d45d-963">ADF .Net SDK-versionen har uppdaterats till 4.1.0</span><span class="sxs-lookup"><span data-stu-id="2d45d-963">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="2d45d-964">Korrigera skrivfel i dokumentationen för Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="2d45d-964">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="2d45d-965">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="2d45d-965">Az.EventHub</span></span>
* <span data-ttu-id="2d45d-966">Ny cmmdlet har lagts till för att skapa SAS-token: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="2d45d-966">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="2d45d-967">verifierings- och felmeddelande har lagts till för authorizationrules-rättigheter om endast "hantera" har tilldelats</span><span class="sxs-lookup"><span data-stu-id="2d45d-967">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="2d45d-968">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2d45d-968">Az.KeyVault</span></span>
* <span data-ttu-id="2d45d-969">Stöd har lagts till för att ange KeySize för certifikatprinciper</span><span class="sxs-lookup"><span data-stu-id="2d45d-969">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="2d45d-970">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="2d45d-970">Az.LogicApp</span></span>
* <span data-ttu-id="2d45d-971">Korrigering för Get-AzIntegrationAccountMap för att lista alla mappningstyper</span><span class="sxs-lookup"><span data-stu-id="2d45d-971">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="2d45d-972">Ny MapType-parameter har lagts till för filtrering</span><span class="sxs-lookup"><span data-stu-id="2d45d-972">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="2d45d-973">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="2d45d-973">Az.ManagedServices</span></span>
* <span data-ttu-id="2d45d-974">Stöd för API-versionen 2019-06-01 (GA) har lagts till</span><span class="sxs-lookup"><span data-stu-id="2d45d-974">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d45d-975">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d45d-975">Az.Network</span></span>
* <span data-ttu-id="2d45d-976">Lägg till stöd för privat slutpunkt och privat länktjänst</span><span class="sxs-lookup"><span data-stu-id="2d45d-976">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="2d45d-977">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="2d45d-977">New cmdlets</span></span>
        - <span data-ttu-id="2d45d-978">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="2d45d-978">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="2d45d-979">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="2d45d-979">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="2d45d-980">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2d45d-980">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="2d45d-981">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2d45d-981">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="2d45d-982">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2d45d-982">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="2d45d-983">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2d45d-983">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="2d45d-984">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="2d45d-984">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="2d45d-985">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="2d45d-985">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="2d45d-986">Nedanstående kommandon för funktionen har uppdaterats: Flaggan PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies på undernätet i VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2d45d-986">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="2d45d-987">Uppdaterade New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="2d45d-987">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="2d45d-988">Valfri parameter har lagts till – PrivateEndpointNetworkPoliciesFlag som konfigurerar huruvida nätverksprinciper ska tillämpas på en privat slutpunkt i det här undernätet.</span><span class="sxs-lookup"><span data-stu-id="2d45d-988">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="2d45d-989">Valfri parameter har lagts till – PrivateLinkServiceNetworkPoliciesFlag som konfigurerar huruvida nätverksprinciper ska tillämpas på en privat länktjänst i det här undernätet.</span><span class="sxs-lookup"><span data-stu-id="2d45d-989">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="2d45d-990">AzPrivateLinkService för cmdlet-parametern ServiceName har bytt namn till Name med aliaset ServiceName för bakåtkompatibilitet</span><span class="sxs-lookup"><span data-stu-id="2d45d-990">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="2d45d-991">Aktivera ICMP-protokoll för konfiguration av nätverkssäkerhetsregler</span><span class="sxs-lookup"><span data-stu-id="2d45d-991">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="2d45d-992">Uppdaterade cmdletar</span><span class="sxs-lookup"><span data-stu-id="2d45d-992">Updated cmdlets</span></span>
        - <span data-ttu-id="2d45d-993">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2d45d-993">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="2d45d-994">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2d45d-994">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="2d45d-995">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2d45d-995">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="2d45d-996">Lägg till ConnectionProtocolType (Ikev1/Ikev2) som en konfigurerbar parameter för New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="2d45d-996">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="2d45d-997">Lägg till PrivateIpAddressVersion i LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="2d45d-997">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="2d45d-998">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="2d45d-998">Updated cmdlet:</span></span>
        - <span data-ttu-id="2d45d-999">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="2d45d-999">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="2d45d-1000">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="2d45d-1000">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="2d45d-1001">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="2d45d-1001">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="2d45d-1002">Uppdatering av Application Gateway-kommandot New-AzApplicationGatewayProbeConfig för stöd av anpassad port i Probe</span><span class="sxs-lookup"><span data-stu-id="2d45d-1002">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="2d45d-1003">Uppdaterade New-AzApplicationGatewayProbeConfig: Den valfria parametern Port som används för avsökning i serverdelen har lagts till.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1003">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="2d45d-1004">Denna parameter gäller för SKU:erna Standard_V2 och WAF_V2.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1004">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="2d45d-1005">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2d45d-1005">Az.OperationalInsights</span></span>
* <span data-ttu-id="2d45d-1006">Uppdaterade standardversionen för sparade sökningar till 1.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1006">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="2d45d-1007">Åtgärdade hantering av anpassad log null regex</span><span class="sxs-lookup"><span data-stu-id="2d45d-1007">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2d45d-1008">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d45d-1008">Az.RecoveryServices</span></span>
* <span data-ttu-id="2d45d-1009">Uppdatera Get-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="2d45d-1009">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="2d45d-1010">Uppdatera Get-AzRecoveryServicesBackupContainer.md</span><span class="sxs-lookup"><span data-stu-id="2d45d-1010">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="2d45d-1011">Uppdatera Get-AzRecoveryServicesVault.md</span><span class="sxs-lookup"><span data-stu-id="2d45d-1011">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="2d45d-1012">Uppdatera Wait-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="2d45d-1012">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="2d45d-1013">Uppdatera Set-AzRecoveryServicesVaultContext.md</span><span class="sxs-lookup"><span data-stu-id="2d45d-1013">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="2d45d-1014">Uppdatera Get-AzRecoveryServicesBackupItem.md</span><span class="sxs-lookup"><span data-stu-id="2d45d-1014">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="2d45d-1015">Uppdatera Get-AzRecoveryServicesBackupRecoveryPoint.md</span><span class="sxs-lookup"><span data-stu-id="2d45d-1015">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="2d45d-1016">Uppdatera Restore-AzRecoveryServicesBackupItem.md</span><span class="sxs-lookup"><span data-stu-id="2d45d-1016">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="2d45d-1017">Uppdaterat tjänstanrop för avregistrering av container för Azure-filresurs</span><span class="sxs-lookup"><span data-stu-id="2d45d-1017">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="2d45d-1018">Uppdatera Set-AzRecoveryServicesAsrAlertSetting.md</span><span class="sxs-lookup"><span data-stu-id="2d45d-1018">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d45d-1019">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d45d-1019">Az.Resources</span></span>
- <span data-ttu-id="2d45d-1020">Ta bort den cmdlet som saknas och som refereras i dokumentationen till New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="2d45d-1020">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="2d45d-1021">Princip-cmdletar har uppdaterats så att de använder den nya API-versionen 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="2d45d-1021">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="2d45d-1022">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="2d45d-1022">Az.ServiceBus</span></span>
* <span data-ttu-id="2d45d-1023">Ny cmmdlet har lagts till för att skapa SAS-token: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="2d45d-1023">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="2d45d-1024">verifierings- och felmeddelande har lagts till för authorizationrules-rättigheter om endast "hantera" har tilldelats</span><span class="sxs-lookup"><span data-stu-id="2d45d-1024">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d45d-1025">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d45d-1025">Az.Sql</span></span>
* <span data-ttu-id="2d45d-1026">Åtgärda saknade exempel för Set-AzSqlDatabaseSecondary cmdlet</span><span class="sxs-lookup"><span data-stu-id="2d45d-1026">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="2d45d-1027">Åtgärda angivna återkommande genomsökningar för bedömning av säkerhetsrisk utan angivna e-postadresser</span><span class="sxs-lookup"><span data-stu-id="2d45d-1027">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="2d45d-1028">Korrigera ett skrivfel i ett varningsmeddelande.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1028">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2d45d-1029">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d45d-1029">Az.Storage</span></span>
* <span data-ttu-id="2d45d-1030">Uppdatera exempel i referensdokumentationen för Get-AzStorageAccount så att rätt parameternamn används</span><span class="sxs-lookup"><span data-stu-id="2d45d-1030">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="2d45d-1031">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="2d45d-1031">Az.StorageSync</span></span>
* <span data-ttu-id="2d45d-1032">Lägger till cmdleten Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1032">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="2d45d-1033">Åtgärda problem 9551 så att TierFilesOlderThanDays föredras</span><span class="sxs-lookup"><span data-stu-id="2d45d-1033">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2d45d-1034">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2d45d-1034">Az.Websites</span></span>
* <span data-ttu-id="2d45d-1035">Åtgärdar ett fel där vissa SiteConfig-egenskaper inte returnerades av Get-AzWebApp och Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="2d45d-1035">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="2d45d-1036">Lägger till en ny platsparameter för Get-AzDeletedWebApp och Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="2d45d-1036">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="2d45d-1037">Åtgärdar ett fel i kloning av webbapp-platser som använder New-AzWebApp-IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="2d45d-1037">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="2d45d-1038">2.4.0 – juli 2019</span><span class="sxs-lookup"><span data-stu-id="2d45d-1038">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2d45d-1039">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d45d-1039">Az.Accounts</span></span>
* <span data-ttu-id="2d45d-1040">Lägg till stöd för profil-cmdletar</span><span class="sxs-lookup"><span data-stu-id="2d45d-1040">Add support for profile cmdlets</span></span>
* <span data-ttu-id="2d45d-1041">Lägg till stöd för miljöer och dataplaner i genererade cmdletar</span><span class="sxs-lookup"><span data-stu-id="2d45d-1041">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="2d45d-1042">Åtgärda bugg där fel slutpunkt i vissa fall användes för cmdletar för dataplaner i Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="2d45d-1042">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="2d45d-1043">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="2d45d-1043">Az.Advisor</span></span>
* <span data-ttu-id="2d45d-1044">GA-version av Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="2d45d-1044">GA release of Az.Advisor</span></span>
* <span data-ttu-id="2d45d-1045">Den här modulen ingår nu som en del av `Az`-sammanslagningsmodulen</span><span class="sxs-lookup"><span data-stu-id="2d45d-1045">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="2d45d-1046">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2d45d-1046">Az.ApiManagement</span></span>
* <span data-ttu-id="2d45d-1047">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="2d45d-1047">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="2d45d-1048">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="2d45d-1048">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="2d45d-1049">Stöd för att fråga prenumerationer efter användare och produkt har lagts till</span><span class="sxs-lookup"><span data-stu-id="2d45d-1049">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="2d45d-1050">Stöd för att fråga med hjälp av omfång ”/”, ”/apis”, ”/apis/echo-api” har lagts till</span><span class="sxs-lookup"><span data-stu-id="2d45d-1050">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="2d45d-1051">Korrigering av problem https://github.com/Azure/azure-powershell/issues/9307 och https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="2d45d-1051">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="2d45d-1052">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="2d45d-1052">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="2d45d-1053">Stöd för att ange ”ApiVersion” och ”ApiVersionSetId” när API:er importeras har lagts till</span><span class="sxs-lookup"><span data-stu-id="2d45d-1053">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2d45d-1054">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2d45d-1054">Az.Automation</span></span>
* <span data-ttu-id="2d45d-1055">Bugg med cmdleten Set-AzAutomationConnectionFieldValue för att hantera strängvärde har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1055">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d45d-1056">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d45d-1056">Az.Compute</span></span>
* <span data-ttu-id="2d45d-1057">Lägg till parametern HyperVGeneration i New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="2d45d-1057">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2d45d-1058">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2d45d-1058">Az.DataFactory</span></span>
* <span data-ttu-id="2d45d-1059">Uppdaterar utdata från ADF-cmdletar som hämtar aktivitetskörningar, hämtar pipelinekörningar och hämtar utlösarkörningar för stöd för Select-Object-pipe.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1059">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="2d45d-1060">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="2d45d-1060">Az.EventGrid</span></span>
* <span data-ttu-id="2d45d-1061">Korrigera stavfel i dokumentation om ”New-AzEventGridSubscription”</span><span class="sxs-lookup"><span data-stu-id="2d45d-1061">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="2d45d-1062">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="2d45d-1062">Az.IotHub</span></span>
* <span data-ttu-id="2d45d-1063">Lägg till stöd för att återskapa principnycklar för auktorisering.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1063">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d45d-1064">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d45d-1064">Az.Network</span></span>
* <span data-ttu-id="2d45d-1065">”RoutingPreference” har lagts till i offentliga IP-taggar</span><span class="sxs-lookup"><span data-stu-id="2d45d-1065">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="2d45d-1066">Förbättra exempel för referensdokumentation om ”Get-AzNetworkServiceTag”</span><span class="sxs-lookup"><span data-stu-id="2d45d-1066">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="2d45d-1067">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="2d45d-1067">Az.PolicyInsights</span></span>
* <span data-ttu-id="2d45d-1068">Åtgärda problem med null-referens i Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="2d45d-1068">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="2d45d-1069">Mer information här: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="2d45d-1069">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="2d45d-1070">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2d45d-1070">Az.OperationalInsights</span></span>
* <span data-ttu-id="2d45d-1071">Modellen för CustomLog-datakälla som returneras i Get-AzOperationalInsightsDataSource har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="2d45d-1071">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2d45d-1072">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d45d-1072">Az.RecoveryServices</span></span>
* <span data-ttu-id="2d45d-1073">Kommandot get-policy för IaaSVM:er har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="2d45d-1073">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d45d-1074">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d45d-1074">Az.Resources</span></span>
    - <span data-ttu-id="2d45d-1075">Korrigera hjälptext för den översta parametern i Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="2d45d-1075">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="2d45d-1076">Lägg till växlingsstöd på klientsidan för Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="2d45d-1076">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="2d45d-1077">Lägg till nya parametrar för Set-AzPolicyAssignment, -PolicyParameters och -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="2d45d-1077">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="2d45d-1078">En mängd dokument- och exempeluppdateringar för Policy-cmdletar</span><span class="sxs-lookup"><span data-stu-id="2d45d-1078">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="2d45d-1079">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="2d45d-1079">Az.ServiceBus</span></span>
* <span data-ttu-id="2d45d-1080">Korrigering av problem #4938 – New-AzureRmServiceBusQueue returnerar BadRequest vid konfiguration av MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="2d45d-1080">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d45d-1081">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d45d-1081">Az.Sql</span></span>
* <span data-ttu-id="2d45d-1082">Lägg till cmdletar för instansredundansgrupper från förhandsversion till offentlig version</span><span class="sxs-lookup"><span data-stu-id="2d45d-1082">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="2d45d-1083">Stöd för granskning för Azure SQL Server\Database med nya cmdletar.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1083">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="2d45d-1084">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="2d45d-1084">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="2d45d-1085">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="2d45d-1085">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="2d45d-1086">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="2d45d-1086">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="2d45d-1087">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="2d45d-1087">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="2d45d-1088">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="2d45d-1088">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="2d45d-1089">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="2d45d-1089">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="2d45d-1090">Ta bort begränsningar för e-post från inställningarna för sårbarhetsbedömning</span><span class="sxs-lookup"><span data-stu-id="2d45d-1090">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2d45d-1091">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d45d-1091">Az.Storage</span></span>
* <span data-ttu-id="2d45d-1092">Ändra två parametrar ”-IndexDocument” och ”-ErrorDocument404Path” från ”krävs” till ”valfri” i cmdlet:</span><span class="sxs-lookup"><span data-stu-id="2d45d-1092">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="2d45d-1093">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="2d45d-1093">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="2d45d-1094">Uppdatera hjälpen för Get-AzStorageBlobContent genom att lägga till ett exempel</span><span class="sxs-lookup"><span data-stu-id="2d45d-1094">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="2d45d-1095">Visa mer felinformation när cmdleten misslyckas med StorageException</span><span class="sxs-lookup"><span data-stu-id="2d45d-1095">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="2d45d-1096">Stöd för att skapa eller uppdatera lagringskonto med Azure Files AAD DS-autentisering</span><span class="sxs-lookup"><span data-stu-id="2d45d-1096">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="2d45d-1097">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2d45d-1097">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="2d45d-1098">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2d45d-1098">Set-AzStorageAccount</span></span>
* <span data-ttu-id="2d45d-1099">Stöd för att lista eller stänga filreferenser för en filresurs, filkatalog eller en fil</span><span class="sxs-lookup"><span data-stu-id="2d45d-1099">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="2d45d-1100">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="2d45d-1100">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="2d45d-1101">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="2d45d-1101">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="2d45d-1102">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="2d45d-1102">Az.StorageSync</span></span>
* <span data-ttu-id="2d45d-1103">Den här modulen ingår nu som en del av `Az`-sammanslagningsmodulen</span><span class="sxs-lookup"><span data-stu-id="2d45d-1103">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="2d45d-1104">2.3.2 – juni 2019</span><span class="sxs-lookup"><span data-stu-id="2d45d-1104">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2d45d-1105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d45d-1105">Az.Accounts</span></span>
* <span data-ttu-id="2d45d-1106">Åtgärda bugg med felaktiga webbadresser som i vissa fall användes för Functions-anrop</span><span class="sxs-lookup"><span data-stu-id="2d45d-1106">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="2d45d-1107">Mer information här: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="2d45d-1107">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="2d45d-1108">Åtgärda problem med alias från AzureRM i Az-cmdletar</span><span class="sxs-lookup"><span data-stu-id="2d45d-1108">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="2d45d-1109">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="2d45d-1109">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="2d45d-1110">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="2d45d-1110">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d45d-1111">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d45d-1111">Az.Compute</span></span>
* <span data-ttu-id="2d45d-1112">Parameteruppsättningarna New-AzVm och New-AzVmss accepterar nu parametern ”ProximityPlacementGroup”.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1112">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="2d45d-1113">Stavfel i referensdokumentationen för ”New-AzVM” har korrigerats</span><span class="sxs-lookup"><span data-stu-id="2d45d-1113">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="2d45d-1114">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="2d45d-1114">Az.Dns</span></span>
* <span data-ttu-id="2d45d-1115">Stavfel i hjälpexempel för ”Set-AzDnsZone” har korrigerats.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1115">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="2d45d-1116">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="2d45d-1116">Az.EventGrid</span></span>
* <span data-ttu-id="2d45d-1117">Har uppdaterats för att använda API-versionen 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1117">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="2d45d-1118">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="2d45d-1118">New cmdlets:</span></span>
    - <span data-ttu-id="2d45d-1119">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="2d45d-1119">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="2d45d-1120">Skapar en ny Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1120">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="2d45d-1121">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="2d45d-1121">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="2d45d-1122">Hämtar information om en Event Grid-domän eller hämtar en lista med alla Event Grid-domäner i den aktuella Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1122">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="2d45d-1123">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="2d45d-1123">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="2d45d-1124">Tar bort en Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1124">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="2d45d-1125">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="2d45d-1125">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="2d45d-1126">Återskapar nyckeln för delad åtkomst för en Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1126">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="2d45d-1127">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="2d45d-1127">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="2d45d-1128">Hämtar de nycklar för delad åtkomst som används för att publicera händelser till en Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1128">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="2d45d-1129">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="2d45d-1129">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="2d45d-1130">Skapar ett nytt Azure Event Grid-domänämne.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1130">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="2d45d-1131">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="2d45d-1131">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="2d45d-1132">Hämtar information om ett Event Grid-domänämne eller hämtar en lista med alla Event Grid-domänämnen under en specifik Event Grid-domän i nuvarande Azure</span><span class="sxs-lookup"><span data-stu-id="2d45d-1132">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="2d45d-1133">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="2d45d-1133">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="2d45d-1134">Tar bort ett befintligt Azure Event Grid-domänämne.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1134">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="2d45d-1135">Uppdaterade cmdletar:</span><span class="sxs-lookup"><span data-stu-id="2d45d-1135">Updated cmdlets:</span></span>
    - <span data-ttu-id="2d45d-1136">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="2d45d-1136">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="2d45d-1137">Lägg till nya obligatoriska parametrar för att stödja piping för den nya Event Grid-domänen och Event Grid-domänämnet för att göra det möjligt att skapa nya händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1137">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="2d45d-1138">Lägg till nya obligatoriska parametrar för att ange det nya Event Grid-domännamnet och/eller namnet på Event Grid-domänämnet för att göra det möjligt att skapa nya händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1138">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="2d45d-1139">Lägg till ny parameteruppsättningar för domäner och domänämnen för att göra det möjligt att återanvända befintliga parametrar (t.ex. EndPointType, SubjectBeginsWith osv).</span><span class="sxs-lookup"><span data-stu-id="2d45d-1139">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="2d45d-1140">Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="2d45d-1140">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="2d45d-1141">Förfallodatum för händelseprenumeration</span><span class="sxs-lookup"><span data-stu-id="2d45d-1141">Event subscription expiration date,</span></span>
            - <span data-ttu-id="2d45d-1142">Avancerade filterparametrar.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1142">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="2d45d-1143">Lägg till ny uppräkning för servicebusqueue som mål.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1143">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="2d45d-1144">Tillåt inte användning av ”Alla” i alternativet -IncludedEventType och ersätt det med</span><span class="sxs-lookup"><span data-stu-id="2d45d-1144">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="2d45d-1145">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="2d45d-1145">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="2d45d-1146">Lägg till ny valfria parametrar (Top, ODataQuery och NextLink) för att stödja sidnumrering och filtrering av resultat.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1146">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="2d45d-1147">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="2d45d-1147">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="2d45d-1148">Lägg till nya obligatoriska parametrar för att stödja piping för en Event Grid-domän och Event Grid-domänämnen för att göra det möjligt att ta bort befintliga händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1148">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="2d45d-1149">Lägg till nya obligatoriska parametrar för att ange Event Grid-domännamnet och/eller namnet på Event Grid-domänämnet för att göra det möjligt att ta bort befintliga händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1149">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="2d45d-1150">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="2d45d-1150">Az.FrontDoor</span></span>
* <span data-ttu-id="2d45d-1151">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="2d45d-1151">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="2d45d-1152">Lägg till stöd för transformeringar och nytt värde för automatisk komplettering för operatorer (RegEx)</span><span class="sxs-lookup"><span data-stu-id="2d45d-1152">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="2d45d-1153">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="2d45d-1153">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="2d45d-1154">Lägg till nya värden för automatisk komplettering</span><span class="sxs-lookup"><span data-stu-id="2d45d-1154">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d45d-1155">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d45d-1155">Az.Network</span></span>
* <span data-ttu-id="2d45d-1156">Lägg till stöd för resurs för virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="2d45d-1156">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="2d45d-1157">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="2d45d-1157">New cmdlets</span></span>
        - <span data-ttu-id="2d45d-1158">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="2d45d-1158">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="2d45d-1159">Lägg till AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="2d45d-1159">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="2d45d-1160">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="2d45d-1160">New cmdlets</span></span>
        - <span data-ttu-id="2d45d-1161">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="2d45d-1161">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="2d45d-1162">Lägg till PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="2d45d-1162">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="2d45d-1163">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="2d45d-1163">New cmdlets</span></span>
        - <span data-ttu-id="2d45d-1164">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="2d45d-1164">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="2d45d-1165">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="2d45d-1165">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="2d45d-1166">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="2d45d-1166">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="2d45d-1167">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="2d45d-1167">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="2d45d-1168">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2d45d-1168">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="2d45d-1169">Lägg till PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="2d45d-1169">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="2d45d-1170">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="2d45d-1170">New cmdlets</span></span>
        - <span data-ttu-id="2d45d-1171">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="2d45d-1171">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="2d45d-1172">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="2d45d-1172">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="2d45d-1173">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="2d45d-1173">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="2d45d-1174">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="2d45d-1174">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="2d45d-1175">Nedanstående kommandon för funktionen har uppdaterats: Flaggan UseLocalAzureIpAddress på VpnConnection</span><span class="sxs-lookup"><span data-stu-id="2d45d-1175">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="2d45d-1176">New-AzVpnConnection har uppdaterats: Den valfria parametern -UseLocalAzureIpAddress har lagts till för att visa att en lokal IP-adress i Azure ska användas som källadress när anslutningen initieras.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1176">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="2d45d-1177">Set-AzVpnConnection har uppdaterats: Den valfria parametern -UseLocalAzureIpAddress har lagts till för att visa att en lokal IP-adress i Azure ska användas som källadress när anslutningen initieras.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1177">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="2d45d-1178">Det skrivskyddade fältet PeeredConnections har lagts till i ExpressRoute-peering.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1178">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="2d45d-1179">Det skrivskyddade fältet GlobalReachEnabled har lagts till i ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1179">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="2d45d-1180">Ett attribut för icke-bakåtkompatibla ändringar har lagts till för att lyfta fram utfasning av fältet AllowGlobalReach i modellen ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2d45d-1180">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="2d45d-1181">Problem 8756 har åtgärdats: Fel vid användning av TargetListenerID med AzApplicationGatewayRedirectConfiguration-cmdletar</span><span class="sxs-lookup"><span data-stu-id="2d45d-1181">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="2d45d-1182">En bugg i New-AzApplicationGatewayPathRuleConfig som gjorde att regeluppsättningen för att återskapa inte kunde anges har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1182">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="2d45d-1183">Visningen av VirtualNetworkTaps i NetworkInterfaceIpConfiguration har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="2d45d-1183">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="2d45d-1184">Cortex Get-cmdletar för att visa en lista med alla delar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="2d45d-1184">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="2d45d-1185">Funktionen för att skapa VirtualHub-referenser för ExpressRouteGateways och VpnGateway har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="2d45d-1185">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="2d45d-1186">Stöd för tillgänglighetszoner i AzureFirewall och NatGateway har lagts till</span><span class="sxs-lookup"><span data-stu-id="2d45d-1186">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="2d45d-1187">Cmdleten Get-AzNetworkServiceTag har lagts till</span><span class="sxs-lookup"><span data-stu-id="2d45d-1187">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="2d45d-1188">Lägg till stöd för flera offentliga IP-adresser för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="2d45d-1188">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="2d45d-1189">Cmdleten New-AzFirewall har uppdaterats:</span><span class="sxs-lookup"><span data-stu-id="2d45d-1189">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="2d45d-1190">Parametern -PublicIpAddress som accepterar ett eller flera offentliga IP-adressobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="2d45d-1190">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="2d45d-1191">Parametern -VirtualNetwork som accepterar ett virtuellt nätverksobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="2d45d-1191">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="2d45d-1192">Metoderna AddPublicIpAddress och RemovePublicIpAddress har lagts till på brandväggsobjekt – dessa accepterar ett offentligt IP-adressobjekt som indata</span><span class="sxs-lookup"><span data-stu-id="2d45d-1192">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="2d45d-1193">Inaktuella parametrar -PublicIpName och -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="2d45d-1193">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="2d45d-1194">Nedanstående kommandon för funktionen har uppdaterats: Ange autentiseringsalternativ för VpnClient AAD till resurser för virtuella nätverksgatewayer.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1194">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="2d45d-1195">New-AzVirtualNetworkGateway har uppdaterats: De valfria parametrarna AadTenantUri, AadAudienceId och AadIssuerUri för att ange VpnClient AAD-autentiseringsalternativ på en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1195">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="2d45d-1196">Set-AzVirtualNetworkGateway har uppdaterats: De valfria parametrarna AadTenantUri, AadAudienceId och AadIssuerUri för att ange VpnClient AAD-autentiseringsalternativ på en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1196">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="2d45d-1197">Set-AzVirtualNetworkGateway har uppdaterats: Den valfria växelparametern RemoveAadAuthentication som tar bort VpnClient AAD-autentiseringsalternativ från en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1197">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="2d45d-1198">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2d45d-1198">Az.OperationalInsights</span></span>
* <span data-ttu-id="2d45d-1199">Aktivera prisnivån **pergb2018** i kommandot ”New-AzureRmOperationalInsightsWorkspace”</span><span class="sxs-lookup"><span data-stu-id="2d45d-1199">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d45d-1200">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d45d-1200">Az.Resources</span></span>
* <span data-ttu-id="2d45d-1201">Stöd för ytterligare alternativ för att exportera en mall</span><span class="sxs-lookup"><span data-stu-id="2d45d-1201">Support for additional Template Export options</span></span>
    - <span data-ttu-id="2d45d-1202">Lägg till parametern ”-SkipResourceNameParameterization” till Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2d45d-1202">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="2d45d-1203">Lägg till parametern ”-SkipAllParameterization” till Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2d45d-1203">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="2d45d-1204">Lägg till parametern ”-Resource” till Export-AzResourceGroup för exporterad resursfiltrering</span><span class="sxs-lookup"><span data-stu-id="2d45d-1204">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="2d45d-1205">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2d45d-1205">Az.ServiceFabric</span></span>
* <span data-ttu-id="2d45d-1206">Åtgärda att fel tumavtryck används vid tilläggning av certifikat i ByExistingKeyVault i vissa fall</span><span class="sxs-lookup"><span data-stu-id="2d45d-1206">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d45d-1207">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d45d-1207">Az.Sql</span></span>
* <span data-ttu-id="2d45d-1208">Åtgärda suffix för lagringsslutpunkt i Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="2d45d-1208">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="2d45d-1209">Åtgärda att aktivering av Advanced Data Security åsidosätter Advanced Threat Protection-princip</span><span class="sxs-lookup"><span data-stu-id="2d45d-1209">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="2d45d-1210">Nya cmdletar för Management.Sql som gör att kunderna kan lägga till nycklar för transparent datakryptering (TDE) och ange TDE-skydd för hanterade instanser</span><span class="sxs-lookup"><span data-stu-id="2d45d-1210">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="2d45d-1211">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="2d45d-1211">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="2d45d-1212">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="2d45d-1212">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="2d45d-1213">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="2d45d-1213">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="2d45d-1214">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="2d45d-1214">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="2d45d-1215">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="2d45d-1215">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2d45d-1216">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d45d-1216">Az.Storage</span></span>
* <span data-ttu-id="2d45d-1217">Stöd för typerna FileStorage och SkuName Premium_ZRS när lagringskonton skapas</span><span class="sxs-lookup"><span data-stu-id="2d45d-1217">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="2d45d-1218">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2d45d-1218">New-AzStorageAccount</span></span>
* <span data-ttu-id="2d45d-1219">Beskrivningen av cmdleten för bloboföränderlighet har förtydligats</span><span class="sxs-lookup"><span data-stu-id="2d45d-1219">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="2d45d-1220">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="2d45d-1220">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2d45d-1221">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2d45d-1221">Az.Websites</span></span>
* <span data-ttu-id="2d45d-1222">Optimerar Get-AzWebAppCertificate för att filtrera efter resursgrupp på servern i stället för klienten</span><span class="sxs-lookup"><span data-stu-id="2d45d-1222">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="2d45d-1223">Lägger till växlingsparametern -UseDisasterRecovery till Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="2d45d-1223">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="2d45d-1224">2.2.0 – juni 2019</span><span class="sxs-lookup"><span data-stu-id="2d45d-1224">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="2d45d-1225">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="2d45d-1225">Az.Cdn</span></span>
* <span data-ttu-id="2d45d-1226">Uppdaterade cmdletar för att ge stöd för rulesEngine-funktion baserat på API-version 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1226">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d45d-1227">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d45d-1227">Az.Compute</span></span>
* <span data-ttu-id="2d45d-1228">Lade till parameter `NoWait` som startar åtgärden och returnerar omedelbart, innan åtgärden har slutförts.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1228">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="2d45d-1229">Uppdaterade cmdletar:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="2d45d-1229">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="2d45d-1230">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="2d45d-1230">Az.EventHub</span></span>
* <span data-ttu-id="2d45d-1231">Korrigering för #9231 – Get-AzEventHubNamespace returnerar inga taggar</span><span class="sxs-lookup"><span data-stu-id="2d45d-1231">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="2d45d-1232">Korrigering för #9230 – Get-AzEventHubNamespace returnerar ResourceGroup istället för ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d45d-1232">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d45d-1233">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d45d-1233">Az.Network</span></span>
* <span data-ttu-id="2d45d-1234">Uppdatera ResourceId och InputObject för NAT-gateway</span><span class="sxs-lookup"><span data-stu-id="2d45d-1234">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="2d45d-1235">Lägg till alias för ResourceId och InputObject</span><span class="sxs-lookup"><span data-stu-id="2d45d-1235">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="2d45d-1236">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="2d45d-1236">Az.PolicyInsights</span></span>
* <span data-ttu-id="2d45d-1237">Åtgärda Null-referensproblem i Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="2d45d-1237">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2d45d-1238">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d45d-1238">Az.RecoveryServices</span></span>
* <span data-ttu-id="2d45d-1239">Minsta kvarhållning för IaaSVM-policy i dagar ändrat till 7 från 1</span><span class="sxs-lookup"><span data-stu-id="2d45d-1239">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="2d45d-1240">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="2d45d-1240">Az.ServiceBus</span></span>
* <span data-ttu-id="2d45d-1241">Korrigering för ärende #9182 – Get-AzServiceBusNamespace returnerar ResourceGroup istället för ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d45d-1241">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="2d45d-1242">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2d45d-1242">Az.ServiceFabric</span></span>
* <span data-ttu-id="2d45d-1243">Åtgärda stavfel i felmeddelandet för Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="2d45d-1243">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="2d45d-1244">Åtgärda saknat tecken i Service Fabric-kommandorader</span><span class="sxs-lookup"><span data-stu-id="2d45d-1244">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d45d-1245">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d45d-1245">Az.Sql</span></span>
* <span data-ttu-id="2d45d-1246">Lägg till parametern DnsZonePartner för New-AzureSqlInstance-cmdlet för att ge stöd för AutoDr för hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1246">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="2d45d-1247">Avvecklar cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="2d45d-1247">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="2d45d-1248">Döp om cmdletar för hotidentifiering till Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="2d45d-1248">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="2d45d-1249">Parametrarna New-AzSqlInstance -StorageSizeInGB och -LicenseType är nu valfria.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1249">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2d45d-1250">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2d45d-1250">Az.Websites</span></span>
* <span data-ttu-id="2d45d-1251">åtgärdar problemet där användningen av Set-AzWebApp och Set-AzWebAppSlot med -WebApp-egenskap tog bort taggarna</span><span class="sxs-lookup"><span data-stu-id="2d45d-1251">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="2d45d-1252">2.1.0 – maj 2019</span><span class="sxs-lookup"><span data-stu-id="2d45d-1252">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="2d45d-1253">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2d45d-1253">Az.ApiManagement</span></span>
* <span data-ttu-id="2d45d-1254">Skapade nya cmdletar för att hantera diagnostik för global- och API-omfång</span><span class="sxs-lookup"><span data-stu-id="2d45d-1254">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="2d45d-1255">**Get-AzApiManagementDiagnostic** – Skaffa diagnostik konfigurerad för global- eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="2d45d-1255">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="2d45d-1256">**New-AzApiManagementDiagnostic** – Skapa ny diagnostik för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="2d45d-1256">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="2d45d-1257">**New-AzApiManagementHttpMessageDiagnostic** – Skapa diagnostikinställning om vilka rubriker som ska loggas och storleken på brödtextbyte</span><span class="sxs-lookup"><span data-stu-id="2d45d-1257">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="2d45d-1258">**New-AzApiManagementPipelineDiagnosticSetting** – Skapa diagnostikinställningar för inkommande/utgående HTTP-meddelanden till gatewayen.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1258">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="2d45d-1259">**New-AzApiManagementSamplingSetting** – Skapa samplinginställningar för begäranden/svar för en diagnostik</span><span class="sxs-lookup"><span data-stu-id="2d45d-1259">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="2d45d-1260">**Remove-AzApiManagementDiagnostic** – Ta bort en diagnostikenhet för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="2d45d-1260">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="2d45d-1261">**Set-AzApiManagementDiagnostic** – Uppdatera en diagnostikenhet för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="2d45d-1261">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="2d45d-1262">Skapade nya cmdletar för hantering av cacheminne i ApiManagement-tjänsten</span><span class="sxs-lookup"><span data-stu-id="2d45d-1262">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="2d45d-1263">**Get-AzApiManagementCache** – Hämta information om cacheminnet som anges av identifierare eller alla cacheminnen</span><span class="sxs-lookup"><span data-stu-id="2d45d-1263">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="2d45d-1264">**New-AzApiManagementCache** – Skapa ett nytt default-cacheminne eller cacheminne i en viss Azure-region</span><span class="sxs-lookup"><span data-stu-id="2d45d-1264">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="2d45d-1265">**Remove-AzApiManagementCache** – Ta bort ett cacheminne</span><span class="sxs-lookup"><span data-stu-id="2d45d-1265">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="2d45d-1266">**Remove-AzApiManagementCache** – Ta bort ett cacheminne</span><span class="sxs-lookup"><span data-stu-id="2d45d-1266">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="2d45d-1267">Skapade nya cmdletar för hantering av API-schema</span><span class="sxs-lookup"><span data-stu-id="2d45d-1267">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="2d45d-1268">**New-AzApiManagementSchema** – Skapa ett nytt schema för ett API</span><span class="sxs-lookup"><span data-stu-id="2d45d-1268">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="2d45d-1269">**Get-AzApiManagementSchema** – Hämta de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="2d45d-1269">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="2d45d-1270">**Remove-AzApiManagementSchema** – Ta bort de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="2d45d-1270">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="2d45d-1271">**Set-AzApiManagementSchema** – Uppdatera de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="2d45d-1271">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="2d45d-1272">Skapa ny cmdlet för att generera en användartoken.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1272">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="2d45d-1273">**New-AzApiManagementUserToken** – Skapa en ny användartoken som enligt standardinställning är giltig i 8 timmar. Token för GIT-användaren kan skapas med den här cmdleten./</span><span class="sxs-lookup"><span data-stu-id="2d45d-1273">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="2d45d-1274">Skapade en ny cmdlet för att hämta nätverksstatus</span><span class="sxs-lookup"><span data-stu-id="2d45d-1274">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="2d45d-1275">**Get-AzApiManagementNetworkStatus** – Hämta nätverksstatusanslutningen för resurserna som API Management-tjänsten är beroende av.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1275">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="2d45d-1276">Det här är användbart när du distribuerar ApiManagement-tjänsten i ett virtuellt nätverk och validerar om något beroende är brutet.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1276">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="2d45d-1277">Uppdaterade cmdlet **New-AzApiManagement** för att hantera ApiManagement-tjänsten</span><span class="sxs-lookup"><span data-stu-id="2d45d-1277">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="2d45d-1278">Lade till stöd för den nya SKU:n Consumption</span><span class="sxs-lookup"><span data-stu-id="2d45d-1278">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="2d45d-1279">Aktiverade stöd för att slå på flaggan EnableClientCertificate för SKU:n Consumption</span><span class="sxs-lookup"><span data-stu-id="2d45d-1279">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="2d45d-1280">Den nya cmdleten **New-AzApiManagementSslSetting** gör det möjligt att ställa in TLS/SSL-inställningen på ”Backend” och ”Frontend” (serverdel och klientdel).</span><span class="sxs-lookup"><span data-stu-id="2d45d-1280">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="2d45d-1281">Det här kan också användas till att konfigurera chiffer som 3DES och ServerProtocols som Http2 för Frontend för en ApiManagement-tjänst.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1281">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="2d45d-1282">Stöd har lagts till för att konfigurera värdnamnet DeveloperPortal på ApiManagement-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1282">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="2d45d-1283">Uppdaterade cmdletar **Get-AzApiManagementSsoToken** för att ta PsApiManagement-objekt som indata</span><span class="sxs-lookup"><span data-stu-id="2d45d-1283">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="2d45d-1284">Uppdaterad cmdleten för att visa infogade felmeddelanden</span><span class="sxs-lookup"><span data-stu-id="2d45d-1284">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="2d45d-1285">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Felkod: Felmeddelande av typen ValidationError: Ett eller flera fält innehåller felaktiga värden: Felinformation:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="2d45d-1285">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="2d45d-1286">Uppdaterade cmdlet **Export-AzApiManagementApi** för att exportera API:er i OpenApi 3.0-format</span><span class="sxs-lookup"><span data-stu-id="2d45d-1286">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="2d45d-1287">Uppdaterade cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="2d45d-1287">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="2d45d-1288">Importera API från dokumentspecifikationen OpenApi 3.0</span><span class="sxs-lookup"><span data-stu-id="2d45d-1288">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="2d45d-1289">Om du vill åsidosätta egenskapen PsApiManagementSchema specificerad i ett dokument (Swagger, Wadl, Wsdl, OpenApi).</span><span class="sxs-lookup"><span data-stu-id="2d45d-1289">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="2d45d-1290">Åsidosätta egenskapen ServiceUrl som specificeras i ett dokument.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1290">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="2d45d-1291">Uppdaterade cmdlet **Get-AzApiManagementPolicy** för att returnera policy i undantaget format av typen icke-XML med rawxml</span><span class="sxs-lookup"><span data-stu-id="2d45d-1291">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="2d45d-1292">Uppdaterade cmdlet **Set-AzApiManagementPolicy** för att godkänna policy i undantaget format av typen icke-XML med rawxml och XML undantaget med xml</span><span class="sxs-lookup"><span data-stu-id="2d45d-1292">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="2d45d-1293">Uppdaterad cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="2d45d-1293">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="2d45d-1294">Konfigurera API med OpenId auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1294">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="2d45d-1295">Skapa ett API i ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="2d45d-1295">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="2d45d-1296">Klona ett API med SourceApiId och SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1296">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="2d45d-1297">Möjlighet att konfigurera SubscriptionRequired i API-omfattningen.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1297">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="2d45d-1298">Uppdaterad cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="2d45d-1298">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="2d45d-1299">Konfigurera API med OpenId auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1299">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="2d45d-1300">Uppdatera ett API till ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="2d45d-1300">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="2d45d-1301">Möjlighet att konfigurera SubscriptionRequired i API-omfattningen.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1301">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="2d45d-1302">Uppdaterad cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="2d45d-1302">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="2d45d-1303">Klona en befintlig version med hjälp av SourceApiRevision (kopiera taggar, produkter, åtgärder och principer).</span><span class="sxs-lookup"><span data-stu-id="2d45d-1303">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="2d45d-1304">Den nya revisionen antar ApiId från den överordnade instansen.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1304">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="2d45d-1305">Tillhandahålla ApiRevisionDescription</span><span class="sxs-lookup"><span data-stu-id="2d45d-1305">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="2d45d-1306">Åsidosätta ServiceUrl vid kloning av ett API.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1306">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="2d45d-1307">Uppdaterad cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="2d45d-1307">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="2d45d-1308">Konfigurera AAD eller AADB2C med en Authority</span><span class="sxs-lookup"><span data-stu-id="2d45d-1308">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="2d45d-1309">Konfigurera SignupPolicy, SigninPolicy, ProfileEditingPolicy och PasswordResetPolicy</span><span class="sxs-lookup"><span data-stu-id="2d45d-1309">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="2d45d-1310">Uppdaterad cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="2d45d-1310">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="2d45d-1311">Kompensera för ny SubscriptonModel med Scope och UserId</span><span class="sxs-lookup"><span data-stu-id="2d45d-1311">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="2d45d-1312">Kompensera för gammal prenumerationsmodell med ProductId och UserId</span><span class="sxs-lookup"><span data-stu-id="2d45d-1312">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="2d45d-1313">Lägg till funktion för att aktivera AllowTracing på prenumerationsnivå.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1313">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="2d45d-1314">Uppdaterad cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="2d45d-1314">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="2d45d-1315">Kompensera för ny SubscriptonModel med Scope och UserId</span><span class="sxs-lookup"><span data-stu-id="2d45d-1315">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="2d45d-1316">Kompensera för gammal prenumerationsmodell med ProductId och UserId</span><span class="sxs-lookup"><span data-stu-id="2d45d-1316">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="2d45d-1317">Lägg till funktion för att aktivera AllowTracing på prenumerationsnivå.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1317">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="2d45d-1318">Uppdaterade följande cmdletar för att acceptera ResourceId som indata</span><span class="sxs-lookup"><span data-stu-id="2d45d-1318">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="2d45d-1319">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2d45d-1319">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="2d45d-1320">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="2d45d-1320">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="2d45d-1321">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="2d45d-1321">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="2d45d-1322">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="2d45d-1322">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="2d45d-1323">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="2d45d-1323">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="2d45d-1324">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="2d45d-1324">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="2d45d-1325">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="2d45d-1325">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="2d45d-1326">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="2d45d-1326">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="2d45d-1327">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="2d45d-1327">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="2d45d-1328">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="2d45d-1328">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="2d45d-1329">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="2d45d-1329">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="2d45d-1330">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="2d45d-1330">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2d45d-1331">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2d45d-1331">Az.Automation</span></span>
* <span data-ttu-id="2d45d-1332">Uppdaterade Get-AzAutomationJobOutputRecord för att hantera postvärden av typen JSON och Text.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1332">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="2d45d-1333">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="2d45d-1333">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="2d45d-1334">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="2d45d-1334">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="2d45d-1335">Ändrade beteende för Start-AzAutomationDscCompilationJob till att bara starta jobbet istället för att vänta på slutförandet.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1335">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="2d45d-1336">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="2d45d-1336">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="2d45d-1337">Korrigering för Get-AzAutomationDscNode när using -Name returnerar alla noder.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1337">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="2d45d-1338">Nu returnerar den endast den matchande noden.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1338">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d45d-1339">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d45d-1339">Az.Compute</span></span>
* <span data-ttu-id="2d45d-1340">Lägg till parametrarna ProtectFromScaleIn och ProtectFromScaleSetAction i cmdleten Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1340">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="2d45d-1341">Nu är standardinställningen att vimpelparametern New-AzVM använder en tillgänglig plats om USA, östra inte stöds</span><span class="sxs-lookup"><span data-stu-id="2d45d-1341">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2d45d-1342">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2d45d-1342">Az.DataLakeStore</span></span>
* <span data-ttu-id="2d45d-1343">Uppdatera ADLS-sdk för att använda httpclient, integrera dataplanstestning med Azure-ramverk</span><span class="sxs-lookup"><span data-stu-id="2d45d-1343">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2d45d-1344">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2d45d-1344">Az.Monitor</span></span>
* <span data-ttu-id="2d45d-1345">Korrigera felaktiga parameternamn i hjälpexempel</span><span class="sxs-lookup"><span data-stu-id="2d45d-1345">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d45d-1346">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d45d-1346">Az.Network</span></span>
* <span data-ttu-id="2d45d-1347">Lägg till flaggan DisableBgpRoutePropagation i utdata för effektiv routningstabell</span><span class="sxs-lookup"><span data-stu-id="2d45d-1347">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="2d45d-1348">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="2d45d-1348">Updated cmdlet:</span></span>
        - <span data-ttu-id="2d45d-1349">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="2d45d-1349">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="2d45d-1350">Åtgärda dubbelstreck i dokumentationen New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="2d45d-1350">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d45d-1351">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d45d-1351">Az.Resources</span></span>
* <span data-ttu-id="2d45d-1352">Lägg till ny cmdlet Get-AzureRmDenyAssignment för att hämta tilldelningsnekanden</span><span class="sxs-lookup"><span data-stu-id="2d45d-1352">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d45d-1353">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d45d-1353">Az.Sql</span></span>
* <span data-ttu-id="2d45d-1354">Döp om Advanced Threat Protection-cmdletar för Advanced Data Security och aktivera Vulnerability Assessment som standard</span><span class="sxs-lookup"><span data-stu-id="2d45d-1354">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="2d45d-1355">2.0.0 – maj 2019</span><span class="sxs-lookup"><span data-stu-id="2d45d-1355">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2d45d-1356">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d45d-1356">Az.Accounts</span></span>
* <span data-ttu-id="2d45d-1357">Uppdatera autentiseringsbiblioteket för att åtgärda ADFS-problem med autentisering av användarnamn/lösenord</span><span class="sxs-lookup"><span data-stu-id="2d45d-1357">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="2d45d-1358">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="2d45d-1358">Az.CognitiveServices</span></span>
* <span data-ttu-id="2d45d-1359">Visa endast Bing-ansvarsfriskrivning för Bing-sökningstjänster.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1359">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="2d45d-1360">Förbättra felmeddelande när det inte går att skapa konton.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1360">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d45d-1361">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d45d-1361">Az.Compute</span></span>
* <span data-ttu-id="2d45d-1362">Funktion för närhetsplaceringsgrupper.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1362">Proximity placement group feature.</span></span>
    - <span data-ttu-id="2d45d-1363">Följande nya cmdletar har lagts till:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="2d45d-1363">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="2d45d-1364">Den nya parametern ProximityPlacementGroupId har lagts till i följande cmdletar:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="2d45d-1364">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="2d45d-1365">Parametern StorageAccountType har lagts till i New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1365">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="2d45d-1366">TargetRegion för New-AzGalleryImageVersion kan innehålla StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1366">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="2d45d-1367">Växlingsparametern SkipShutdown har lagts till i Stop-AzVM och Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="2d45d-1367">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="2d45d-1368">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="2d45d-1368">Breaking changes</span></span>
    - <span data-ttu-id="2d45d-1369">Set-AzVMBootDiagnostics har ändrats till Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1369">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="2d45d-1370">Export-AzLogAnalyticThrottledRequests har ändrats till Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1370">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="2d45d-1371">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="2d45d-1371">Az.DeploymentManager</span></span>
* <span data-ttu-id="2d45d-1372">De första allmänt tillgängliga versionerna av cmdletar för Distributionshanteraren i Azure</span><span class="sxs-lookup"><span data-stu-id="2d45d-1372">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="2d45d-1373">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="2d45d-1373">Az.Dns</span></span>
* <span data-ttu-id="2d45d-1374">Automatisk delegering av DNS för NameServer</span><span class="sxs-lookup"><span data-stu-id="2d45d-1374">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="2d45d-1375">Det överordnade zonnamnet kan användas som ytterligare valfri parameter i cmdleten för att skapa DNS-zoner.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1375">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="2d45d-1376">Lägger till NS-poster för en nyligen skapad underordnad zon i den överordnade zonen.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1376">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="2d45d-1377">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="2d45d-1377">Az.FrontDoor</span></span>
* <span data-ttu-id="2d45d-1378">De första allmänt tillgängliga versionerna av cmdletar för Azure FrontDoor</span><span class="sxs-lookup"><span data-stu-id="2d45d-1378">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="2d45d-1379">Byt namn på WAF-cmdletar så att de omfattar ”Waf”</span><span class="sxs-lookup"><span data-stu-id="2d45d-1379">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="2d45d-1380">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="2d45d-1380">Az.HDInsight</span></span>
* <span data-ttu-id="2d45d-1381">Två cmdletar har tagits bort:</span><span class="sxs-lookup"><span data-stu-id="2d45d-1381">Removed two cmdlets:</span></span>
    - <span data-ttu-id="2d45d-1382">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="2d45d-1382">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="2d45d-1383">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="2d45d-1383">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="2d45d-1384">En ny cmdlet har lagts till, Set-AzHDInsightGatewayCredential, som ersätter Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="2d45d-1384">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="2d45d-1385">Uppdatera cmdleten Get-AzHDInsightJobOutput för att skilja mellan läsarrollen och HDInsight-operatörsrollen:</span><span class="sxs-lookup"><span data-stu-id="2d45d-1385">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="2d45d-1386">Användare med läsarrollen måste uttryckligen ange parametern ”DefaultStorageAccountKey”, annars uppstår fel.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1386">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="2d45d-1387">Användare med HDInsight-operatörsrollen påverkas inte.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1387">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2d45d-1388">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2d45d-1388">Az.Monitor</span></span>
* <span data-ttu-id="2d45d-1389">Nya cmdletar för SQR API (schemalagd frågeregel)</span><span class="sxs-lookup"><span data-stu-id="2d45d-1389">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="2d45d-1390">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="2d45d-1390">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="2d45d-1391">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="2d45d-1391">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="2d45d-1392">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="2d45d-1392">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="2d45d-1393">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="2d45d-1393">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="2d45d-1394">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="2d45d-1394">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="2d45d-1395">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="2d45d-1395">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="2d45d-1396">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="2d45d-1396">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="2d45d-1397">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="2d45d-1397">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="2d45d-1398">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="2d45d-1398">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="2d45d-1399">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="2d45d-1399">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="2d45d-1400">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="2d45d-1400">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="2d45d-1401">[Mer](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information om SQR API</span><span class="sxs-lookup"><span data-stu-id="2d45d-1401">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="2d45d-1402">Az.Monitor.md har uppdaterats för att omfatta cmdletar för måttbaserade aviseringsregler i GenV2 (inte klassiska)</span><span class="sxs-lookup"><span data-stu-id="2d45d-1402">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d45d-1403">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d45d-1403">Az.Network</span></span>
* <span data-ttu-id="2d45d-1404">Lägg till stöd för NAT Gateway-resurs</span><span class="sxs-lookup"><span data-stu-id="2d45d-1404">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="2d45d-1405">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="2d45d-1405">New cmdlets</span></span>
        - <span data-ttu-id="2d45d-1406">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="2d45d-1406">New-AzNatGateway</span></span>
        - <span data-ttu-id="2d45d-1407">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="2d45d-1407">Get-AzNatGateway</span></span>
        - <span data-ttu-id="2d45d-1408">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="2d45d-1408">Set-AzNatGateway</span></span>
        - <span data-ttu-id="2d45d-1409">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="2d45d-1409">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="2d45d-1410">Uppdaterade cmdletar</span><span class="sxs-lookup"><span data-stu-id="2d45d-1410">Updated cmdlets</span></span>
        - <span data-ttu-id="2d45d-1411">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="2d45d-1411">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="2d45d-1412">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="2d45d-1412">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="2d45d-1413">Nedanstående kommandon för funktionen har uppdaterats: Ange/ta bort anpassade vägar på Brooklyn Gateway.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1413">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="2d45d-1414">New-AzVirtualNetworkGateway har uppdaterats: Den valfria parametern -CustomRoute har lagts till för att ställa in adressprefix som anpassade vägar för att ange gateway.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1414">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="2d45d-1415">Set-AzVirtualNetworkGateway har uppdaterats: Den valfria parametern -CustomRoute har lagts till för att ange adressprefix som anpassade vägar för att ange gateway.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1415">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="2d45d-1416">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="2d45d-1416">Az.PolicyInsights</span></span>
* <span data-ttu-id="2d45d-1417">Stöd för att fråga efter information om principutvärdering.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1417">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="2d45d-1418">Lägg till parametern ”-Expand” för Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1418">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="2d45d-1419">Stöd för -Expand PolicyEvaluationDetails.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1419">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2d45d-1420">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d45d-1420">Az.RecoveryServices</span></span>
* <span data-ttu-id="2d45d-1421">Stöd för att dela prenumeration mellan Azure och Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1421">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="2d45d-1422">Markering av kommande icke-bakåtkompatibla ändringar för Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1422">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="2d45d-1423">Korrigering för återställningsplan och åtgärdsplan i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1423">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="2d45d-1424">Korrigering för mappning av uppdateringsnätverk i Azure Site Recovery för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1424">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="2d45d-1425">Korrigering för instruktioner för uppdateringsskydd i Azure Site Recovery för Azure till Azure för hanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1425">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="2d45d-1426">Andra mindre korrigeringar.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1426">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="2d45d-1427">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="2d45d-1427">Az.Relay</span></span>
* <span data-ttu-id="2d45d-1428">Korrigera stavfel i kundriktade meddelanden</span><span class="sxs-lookup"><span data-stu-id="2d45d-1428">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="2d45d-1429">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="2d45d-1429">Az.ServiceBus</span></span>
* <span data-ttu-id="2d45d-1430">Nya cmdletar har lagts till för NetworkRuleSet för namnområden</span><span class="sxs-lookup"><span data-stu-id="2d45d-1430">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2d45d-1431">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d45d-1431">Az.Storage</span></span>
* <span data-ttu-id="2d45d-1432">Uppgradera till lagringsklientbiblioteket 10.0.1 (namnområdet för alla objekt från detta SDK ändras från ”Microsoft.WindowsAzure.Storage. *till ”Microsoft.Azure.Storage.* ”)</span><span class="sxs-lookup"><span data-stu-id="2d45d-1432">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="2d45d-1433">Uppgradera till Microsoft.Azure.Management.Storage 11.0.0 för att stödja den nya API-versionen 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1433">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="2d45d-1434">Standardlagringskontot i Skapa lagringskonto ändras från ”Storage” till ”StorageV2”</span><span class="sxs-lookup"><span data-stu-id="2d45d-1434">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="2d45d-1435">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2d45d-1435">New-AzStorageAccount</span></span>
* <span data-ttu-id="2d45d-1436">Ändra lagringskontots cmdlet-utdata Sku.Name för att passa med indata-SkuName genom att lägga till ”-”. Till exempel ändras ”StandardLRS” till ”Standard_LRS”</span><span class="sxs-lookup"><span data-stu-id="2d45d-1436">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="2d45d-1437">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2d45d-1437">New-AzStorageAccount</span></span>
    - <span data-ttu-id="2d45d-1438">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2d45d-1438">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="2d45d-1439">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2d45d-1439">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2d45d-1440">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2d45d-1440">Az.Websites</span></span>
* <span data-ttu-id="2d45d-1441">Egenskapen ”typ” konfigureras nu för PSSite-objekt som returneras av Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="2d45d-1441">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="2d45d-1442">Get-AzWebApp\*Metrics och Get-AzAppServicePlanMetrics markeras som inaktuella</span><span class="sxs-lookup"><span data-stu-id="2d45d-1442">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="2d45d-1443">1.8.0 – april 2019</span><span class="sxs-lookup"><span data-stu-id="2d45d-1443">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="2d45d-1444">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="2d45d-1444">Highlights since the last major release</span></span>
* <span data-ttu-id="2d45d-1445">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="2d45d-1445">General availability of `Az` module</span></span>
* <span data-ttu-id="2d45d-1446">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="2d45d-1446">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="2d45d-1447">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="2d45d-1447">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="2d45d-1448">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="2d45d-1448">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="2d45d-1449">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="2d45d-1449">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="2d45d-1450">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="2d45d-1450">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="2d45d-1451">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="2d45d-1451">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="2d45d-1452">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d45d-1452">Az.Accounts</span></span>
* <span data-ttu-id="2d45d-1453">Uppdatera Uninstall-AzureRm för att ta bort moduler i Mac på ett korrekt sätt</span><span class="sxs-lookup"><span data-stu-id="2d45d-1453">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="2d45d-1454">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="2d45d-1454">Az.Batch</span></span>
* <span data-ttu-id="2d45d-1455">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1455">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="2d45d-1456">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="2d45d-1456">Az.Cdn</span></span>
* <span data-ttu-id="2d45d-1457">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1457">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="2d45d-1458">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="2d45d-1458">Az.CognitiveServices</span></span>
* <span data-ttu-id="2d45d-1459">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1459">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d45d-1460">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d45d-1460">Az.Compute</span></span>
* <span data-ttu-id="2d45d-1461">Åtgärda problem med AEM-installationen om resurs-ID:n för diskar innehåller resourcegroups i gemener i resurs-ID:n</span><span class="sxs-lookup"><span data-stu-id="2d45d-1461">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="2d45d-1462">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1462">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="2d45d-1463">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="2d45d-1463">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2d45d-1464">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2d45d-1464">Az.DataFactory</span></span>
* <span data-ttu-id="2d45d-1465">Lägg till SsisProperties om NodeCount inte är null för hanterad integreringskörning.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1465">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2d45d-1466">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2d45d-1466">Az.DataLakeStore</span></span>
* <span data-ttu-id="2d45d-1467">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1467">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="2d45d-1468">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="2d45d-1468">Az.EventGrid</span></span>
* <span data-ttu-id="2d45d-1469">Hjälptexten för slutpunkten har uppdaterats för att visa att resurser ska skapas innan cmdletarna för att skapa/uppdatera händelseprenumerationer används.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1469">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="2d45d-1470">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="2d45d-1470">Az.EventHub</span></span>
* <span data-ttu-id="2d45d-1471">Nya cmdletar har lagts till för NetworkRuleSet för namnområden</span><span class="sxs-lookup"><span data-stu-id="2d45d-1471">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="2d45d-1472">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="2d45d-1472">Az.HDInsight</span></span>
* <span data-ttu-id="2d45d-1473">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1473">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="2d45d-1474">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="2d45d-1474">Az.IotHub</span></span>
* <span data-ttu-id="2d45d-1475">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1475">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="2d45d-1476">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2d45d-1476">Az.KeyVault</span></span>
* <span data-ttu-id="2d45d-1477">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1477">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="2d45d-1478">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="2d45d-1478">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="2d45d-1479">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="2d45d-1479">Az.MachineLearning</span></span>
* <span data-ttu-id="2d45d-1480">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1480">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="2d45d-1481">Az.Media</span><span class="sxs-lookup"><span data-stu-id="2d45d-1481">Az.Media</span></span>
* <span data-ttu-id="2d45d-1482">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1482">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2d45d-1483">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2d45d-1483">Az.Monitor</span></span>
  * <span data-ttu-id="2d45d-1484">Nya cmdletar för måttbaserad aviseringsregel i GenV2 (inte klassisk)</span><span class="sxs-lookup"><span data-stu-id="2d45d-1484">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="2d45d-1485">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="2d45d-1485">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="2d45d-1486">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="2d45d-1486">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="2d45d-1487">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="2d45d-1487">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="2d45d-1488">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="2d45d-1488">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="2d45d-1489">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="2d45d-1489">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="2d45d-1490">Monitor SDK har uppdaterats till version 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="2d45d-1490">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d45d-1491">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d45d-1491">Az.Network</span></span>
* <span data-ttu-id="2d45d-1492">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1492">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="2d45d-1493">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="2d45d-1493">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="2d45d-1494">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="2d45d-1494">Az.NotificationHubs</span></span>
* <span data-ttu-id="2d45d-1495">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1495">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="2d45d-1496">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2d45d-1496">Az.OperationalInsights</span></span>
* <span data-ttu-id="2d45d-1497">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1497">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="2d45d-1498">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="2d45d-1498">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="2d45d-1499">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1499">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2d45d-1500">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d45d-1500">Az.RecoveryServices</span></span>
* <span data-ttu-id="2d45d-1501">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1501">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="2d45d-1502">Tabellformatet för SQL i virtuella Azure-datorer har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="2d45d-1502">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="2d45d-1503">En alternativ metod för att hämta platser i AzureFileShare har lagts till</span><span class="sxs-lookup"><span data-stu-id="2d45d-1503">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="2d45d-1504">ScheduleRunDays i SchedulePolicy-objekt har uppdaterats enligt tidszon</span><span class="sxs-lookup"><span data-stu-id="2d45d-1504">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="2d45d-1505">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="2d45d-1505">Az.RedisCache</span></span>
* <span data-ttu-id="2d45d-1506">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1506">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d45d-1507">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d45d-1507">Az.Resources</span></span>
* <span data-ttu-id="2d45d-1508">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="2d45d-1508">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d45d-1509">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d45d-1509">Az.Sql</span></span>
* <span data-ttu-id="2d45d-1510">Ersätt Monitor SDK-beroende med vanlig kod</span><span class="sxs-lookup"><span data-stu-id="2d45d-1510">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="2d45d-1511">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1511">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="2d45d-1512">Förbättrad process för klassificering av flera kolumner.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1512">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="2d45d-1513">Inkludera SKU-egenskaper (SKU-namn, serie, kapacitet) i svaret från Get-AzSqlServerServiceObjective och formatera som tabell som standard.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1513">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="2d45d-1514">Möjlighet att använda Get-AzSqlServerServiceObjective efter plats utan att behöva en redan befintlig server i regionen.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1514">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="2d45d-1515">Stöd för tidszonsparametern när hanterade instanser skapas.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1515">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="2d45d-1516">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="2d45d-1516">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2d45d-1517">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2d45d-1517">Az.Websites</span></span>
* <span data-ttu-id="2d45d-1518">åtgärdar Set-AzWebApp och Set-AzWebAppSlot så att de inte tar bort taggar vid körning</span><span class="sxs-lookup"><span data-stu-id="2d45d-1518">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="2d45d-1519">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1519">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="2d45d-1520">SDK för WebSites har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1520">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="2d45d-1521">Egenskapen AdminSiteName har tagits bort från PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1521">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="2d45d-1522">1.7.0 – april 2019</span><span class="sxs-lookup"><span data-stu-id="2d45d-1522">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="2d45d-1523">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="2d45d-1523">Highlights since the last major release</span></span>
* <span data-ttu-id="2d45d-1524">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="2d45d-1524">General availability of `Az` module</span></span>
* <span data-ttu-id="2d45d-1525">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="2d45d-1525">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="2d45d-1526">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="2d45d-1526">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="2d45d-1527">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="2d45d-1527">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="2d45d-1528">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="2d45d-1528">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="2d45d-1529">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="2d45d-1529">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="2d45d-1530">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="2d45d-1530">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="2d45d-1531">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d45d-1531">Az.Accounts</span></span>
* <span data-ttu-id="2d45d-1532">Add-AzEnvironment och Set-AzEnvironment har uppdaterats för att godkänna parametern AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="2d45d-1532">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="2d45d-1533">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="2d45d-1533">Az.AnalysisServices</span></span>
* <span data-ttu-id="2d45d-1534">ServiceClient används i cmdletar för dataplan och den ursprungliga autentiseringslogiken har tagits bort</span><span class="sxs-lookup"><span data-stu-id="2d45d-1534">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="2d45d-1535">Add-AzureASAccount används för omslutning av Connect-AzAccount för att undvika en icke-bakåtkompatibel ändring</span><span class="sxs-lookup"><span data-stu-id="2d45d-1535">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2d45d-1536">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2d45d-1536">Az.Automation</span></span>
* <span data-ttu-id="2d45d-1537">Buggen för cmdleten New-AzAutomationSoftwareUpdateConfiguration för inkluderingar har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1537">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="2d45d-1538">Nu bör parametern IncludedKbNumber och IncludedPackageNameMask fungera.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1538">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="2d45d-1539">Felkorrigering för dynamiska grupper i uppdateringshanteringen för azure automation</span><span class="sxs-lookup"><span data-stu-id="2d45d-1539">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d45d-1540">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d45d-1540">Az.Compute</span></span>
* <span data-ttu-id="2d45d-1541">Lägg till parametern HyperVGeneration i New-AzDiskConfig och New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="2d45d-1541">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="2d45d-1542">Tillåt att virtuella datorer skapas med galleribilder från andra klientorganisationer.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1542">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="2d45d-1543">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="2d45d-1543">Az.ContainerInstance</span></span>
* <span data-ttu-id="2d45d-1544">Ett problem har åtgärdats i parametern -Command för New-AzContainerGroup som lade till ett avslutande tomt argument</span><span class="sxs-lookup"><span data-stu-id="2d45d-1544">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2d45d-1545">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2d45d-1545">Az.DataFactory</span></span>
* <span data-ttu-id="2d45d-1546">ADF .Net SDK-versionen har uppdaterats till 3.0.2</span><span class="sxs-lookup"><span data-stu-id="2d45d-1546">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="2d45d-1547">Cmdleten Set-AzDataFactoryV2 har uppdaterats med extra parametrar för inställningar som rör RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1547">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d45d-1548">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d45d-1548">Az.Resources</span></span>
* <span data-ttu-id="2d45d-1549">Förbättra hanteringen av providrar för Get-AzResource när parametrarna -ResourceId eller -ResourceGroupName, -Name och -ResourceType tillhandahålls</span><span class="sxs-lookup"><span data-stu-id="2d45d-1549">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="2d45d-1550">Förbättra felhanteringen för ”Test-AzDeployment” och ”Test-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="2d45d-1550">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="2d45d-1551">Hantera fel utanför distributionsvalideringen och ta med dem i kommandoutdata istället</span><span class="sxs-lookup"><span data-stu-id="2d45d-1551">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="2d45d-1552">Mer information här: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="2d45d-1552">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="2d45d-1553">Lägg till växlingsparametern -IgnoreDynamicParameters till en uppsättning av cmdletar för distribution för att hoppa över fråga i skript och jobbscenarier</span><span class="sxs-lookup"><span data-stu-id="2d45d-1553">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="2d45d-1554">Mer information här: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="2d45d-1554">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d45d-1555">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d45d-1555">Az.Sql</span></span>
* <span data-ttu-id="2d45d-1556">Stöd för dataklassificering av databaser.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1556">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2d45d-1557">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d45d-1557">Az.Storage</span></span>
* <span data-ttu-id="2d45d-1558">Rapportera detaljfel när lagringskontext skapas med parametern -UseConnectedAccount, men utan inloggning på Azure-kontot</span><span class="sxs-lookup"><span data-stu-id="2d45d-1558">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="2d45d-1559">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="2d45d-1559">New-AzStorageContext</span></span>
* <span data-ttu-id="2d45d-1560">Stöd för att hantera Blob Service-egenskaper för ett angivet lagringskonto med API:et för hanteringsplan</span><span class="sxs-lookup"><span data-stu-id="2d45d-1560">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="2d45d-1561">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="2d45d-1561">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="2d45d-1562">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="2d45d-1562">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="2d45d-1563">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="2d45d-1563">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="2d45d-1564">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="2d45d-1564">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="2d45d-1565">Stöd för -AsJob-cmdletar för att ladda upp och ladda ned blobar och filer</span><span class="sxs-lookup"><span data-stu-id="2d45d-1565">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="2d45d-1566">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="2d45d-1566">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="2d45d-1567">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="2d45d-1567">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="2d45d-1568">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="2d45d-1568">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="2d45d-1569">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="2d45d-1569">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="2d45d-1570">1.6.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="2d45d-1570">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="2d45d-1571">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="2d45d-1571">Highlights since the last major release</span></span>
* <span data-ttu-id="2d45d-1572">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="2d45d-1572">General availability of `Az` module</span></span>
* <span data-ttu-id="2d45d-1573">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="2d45d-1573">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="2d45d-1574">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="2d45d-1574">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="2d45d-1575">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="2d45d-1575">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="2d45d-1576">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="2d45d-1576">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="2d45d-1577">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="2d45d-1577">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="2d45d-1578">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="2d45d-1578">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2d45d-1579">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2d45d-1579">Az.Automation</span></span>
* <span data-ttu-id="2d45d-1580">Azure Automation – ändring av uppdateringshantering för stöd för de nya funktionerna:</span><span class="sxs-lookup"><span data-stu-id="2d45d-1580">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="2d45d-1581">Dynamisk gruppering</span><span class="sxs-lookup"><span data-stu-id="2d45d-1581">Dynamic grouping</span></span>
    * <span data-ttu-id="2d45d-1582">För-/efterskrift</span><span class="sxs-lookup"><span data-stu-id="2d45d-1582">Pre-Post script</span></span>
    * <span data-ttu-id="2d45d-1583">Inställning för omstart</span><span class="sxs-lookup"><span data-stu-id="2d45d-1583">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d45d-1584">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d45d-1584">Az.Compute</span></span>
* <span data-ttu-id="2d45d-1585">Åtgärda problem med sökvägsmatchning i Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="2d45d-1585">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="2d45d-1586">Uppdatera Compute-klientbibliotek till 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1586">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="2d45d-1587">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2d45d-1587">Az.KeyVault</span></span>
* <span data-ttu-id="2d45d-1588">Stöd för jokertecken för KeyVault-cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="2d45d-1588">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d45d-1589">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d45d-1589">Az.Network</span></span>
* <span data-ttu-id="2d45d-1590">Lägg till stöd för Threat Intelligence för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="2d45d-1590">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="2d45d-1591">Lägg till resurs för brandväggsprincip på översta nivå och anpassade regler för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="2d45d-1591">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2d45d-1592">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d45d-1592">Az.RecoveryServices</span></span>
* <span data-ttu-id="2d45d-1593">SnapshotRetentionInDays har lagts till i Azure-principen för virtuella datorer för stöd av Instant RP</span><span class="sxs-lookup"><span data-stu-id="2d45d-1593">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="2d45d-1594">Pipe-stöd för avregistrering av container har lagts till</span><span class="sxs-lookup"><span data-stu-id="2d45d-1594">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d45d-1595">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d45d-1595">Az.Resources</span></span>
* <span data-ttu-id="2d45d-1596">Uppdatera stöd för jokertecken för Get-AzResource och Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2d45d-1596">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="2d45d-1597">Uppdatera autentiseringsuppgifter som används vid allmänna anrop till ARM</span><span class="sxs-lookup"><span data-stu-id="2d45d-1597">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d45d-1598">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d45d-1598">Az.Sql</span></span>
* <span data-ttu-id="2d45d-1599">Cmdlet-parametern (ExcludeDetectionType) för Hotidentifiering ändrades från DetectionType till sträng[] för att framtidssäkra den när nya DetectionTypes läggs till, och även för att stödja automatisk ifyllning.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1599">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2d45d-1600">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d45d-1600">Az.Storage</span></span>
* <span data-ttu-id="2d45d-1601">Stöd för att hämta/ange/ta bort hanteringsprincip på ett lagringskonto</span><span class="sxs-lookup"><span data-stu-id="2d45d-1601">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="2d45d-1602">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="2d45d-1602">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="2d45d-1603">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="2d45d-1603">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="2d45d-1604">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="2d45d-1604">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="2d45d-1605">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="2d45d-1605">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="2d45d-1606">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="2d45d-1606">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="2d45d-1607">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="2d45d-1607">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2d45d-1608">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2d45d-1608">Az.Websites</span></span>
* <span data-ttu-id="2d45d-1609">Åtgärda fel med ARM-mall som avbryter kloning av alla platser med 'New-AzWebApp -IncludeSourceWebAppSlots'</span><span class="sxs-lookup"><span data-stu-id="2d45d-1609">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="2d45d-1610">1.5.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="2d45d-1610">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2d45d-1611">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d45d-1611">Az.Accounts</span></span>
* <span data-ttu-id="2d45d-1612">Lägg till kommandot Register-AzModule för stöd för AutoRest-genererade cmdletar</span><span class="sxs-lookup"><span data-stu-id="2d45d-1612">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="2d45d-1613">Uppdatera exempel för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="2d45d-1613">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2d45d-1614">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2d45d-1614">Az.Automation</span></span>
* <span data-ttu-id="2d45d-1615">Problem med att hämta vissa månadsscheman i flera Azure Automation-cmdletar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="2d45d-1615">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="2d45d-1616">Åtgärda problem med att Get-AzAutomationDscNode bara returnerar de 20 översta noderna.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1616">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="2d45d-1617">Nu returneras alla noder</span><span class="sxs-lookup"><span data-stu-id="2d45d-1617">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="2d45d-1618">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="2d45d-1618">Az.Cdn</span></span>
* <span data-ttu-id="2d45d-1619">Nya Powershell-cmdletar för att aktivera/inaktivera anpassade domän-HTTPS har lagts till och de gamla har gjorts inaktuella</span><span class="sxs-lookup"><span data-stu-id="2d45d-1619">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d45d-1620">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d45d-1620">Az.Compute</span></span>
* <span data-ttu-id="2d45d-1621">Lägg till stöd för jokertecken för Get-cmdletar</span><span class="sxs-lookup"><span data-stu-id="2d45d-1621">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2d45d-1622">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2d45d-1622">Az.DataFactory</span></span>
* <span data-ttu-id="2d45d-1623">ADF .Net SDK-versionen har uppdaterats till 3.0.1</span><span class="sxs-lookup"><span data-stu-id="2d45d-1623">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="2d45d-1624">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="2d45d-1624">Az.LogicApp</span></span>
* <span data-ttu-id="2d45d-1625">Åtgärda problemet med att ListWorkflows endast hämtar den första sidan med resultat</span><span class="sxs-lookup"><span data-stu-id="2d45d-1625">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d45d-1626">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d45d-1626">Az.Network</span></span>
* <span data-ttu-id="2d45d-1627">Lägg till stöd för jokertecken för Network-cmdletar</span><span class="sxs-lookup"><span data-stu-id="2d45d-1627">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2d45d-1628">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d45d-1628">Az.RecoveryServices</span></span>
* <span data-ttu-id="2d45d-1629">Stöd har lagts till för SQL Server i virtuella Azure-datorer</span><span class="sxs-lookup"><span data-stu-id="2d45d-1629">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="2d45d-1630">SDK-uppdatering</span><span class="sxs-lookup"><span data-stu-id="2d45d-1630">SDK Update</span></span>
* <span data-ttu-id="2d45d-1631">Get-ProtectableItem-incheckning i VMappContainer har tagits bort</span><span class="sxs-lookup"><span data-stu-id="2d45d-1631">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="2d45d-1632">Name och ServerName har lagts till som parametrar för Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="2d45d-1632">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d45d-1633">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d45d-1633">Az.Resources</span></span>
* <span data-ttu-id="2d45d-1634">Lägg till parametern `-TemplateObject` i cmdletar för distribution</span><span class="sxs-lookup"><span data-stu-id="2d45d-1634">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="2d45d-1635">Mer information här: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="2d45d-1635">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="2d45d-1636">Åtgärda problem med piping av resultatet i `Get-AzResource` till `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="2d45d-1636">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="2d45d-1637">Mer information här: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="2d45d-1637">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="2d45d-1638">Åtgärda problem med ändring av JSON-datatyp när `Set-AzResource` körs</span><span class="sxs-lookup"><span data-stu-id="2d45d-1638">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="2d45d-1639">Mer information här: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="2d45d-1639">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d45d-1640">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d45d-1640">Az.Sql</span></span>
* <span data-ttu-id="2d45d-1641">AuditingEndpointsCommunicator uppdateras.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1641">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="2d45d-1642">Åtgärdar beteendet hos ett gränsscenario när nya diagnostikinställningar skapas.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1642">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2d45d-1643">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d45d-1643">Az.Storage</span></span>
* <span data-ttu-id="2d45d-1644">Stöd för BlockBlobStorage när Storage-konto skapas      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2d45d-1644">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="2d45d-1645">1.4.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="2d45d-1645">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="2d45d-1646">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="2d45d-1646">Az.AnalysisServices</span></span>
* <span data-ttu-id="2d45d-1647">Inaktuell AddAzureASAccount-cmdlet</span><span class="sxs-lookup"><span data-stu-id="2d45d-1647">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2d45d-1648">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2d45d-1648">Az.Automation</span></span>
* <span data-ttu-id="2d45d-1649">Hjälpen för Import-AzAutomationDscNodeConfiguration har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="2d45d-1649">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="2d45d-1650">Konfigurationsnamnsvalidering har lagts till i cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="2d45d-1650">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="2d45d-1651">Förbättrad felhantering för cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="2d45d-1651">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="2d45d-1652">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="2d45d-1652">Az.CognitiveServices</span></span>
* <span data-ttu-id="2d45d-1653">CustomSubdomainName har lagts till som en ny valfri parameter för New-AzCognitiveServicesAccount, som används för att ange underdomän för resursen.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1653">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d45d-1654">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d45d-1654">Az.Compute</span></span>
* <span data-ttu-id="2d45d-1655">Problemet med ID-parameteruppsättningar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="2d45d-1655">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="2d45d-1656">Get-AzVMExtension har uppdaterats så att alla installerade tillägg visas om parametern Name inte har angetts</span><span class="sxs-lookup"><span data-stu-id="2d45d-1656">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="2d45d-1657">Parametrarna Tag och ResourceId har lagts till i cmdleten Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="2d45d-1657">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="2d45d-1658">Get-AzVmssVM utan instans-ID och med InstanceView kan visa virtuella VMSS-datorer med instansvyn.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1658">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2d45d-1659">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2d45d-1659">Az.DataLakeStore</span></span>
* <span data-ttu-id="2d45d-1660">Cmdletar har lagts till för uppräkning och återställning av borttagna objekt i ADL</span><span class="sxs-lookup"><span data-stu-id="2d45d-1660">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="2d45d-1661">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="2d45d-1661">Az.EventHub</span></span>
* <span data-ttu-id="2d45d-1662">Ny boolesk egenskap SkipEmptyArchives har lagts till i Skip Empty Archives i CaptureDescription-klassen i Eventhub</span><span class="sxs-lookup"><span data-stu-id="2d45d-1662">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="2d45d-1663">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2d45d-1663">Az.KeyVault</span></span>
* <span data-ttu-id="2d45d-1664">Taggning i Set-AzKeyVaultSecret har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="2d45d-1664">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="2d45d-1665">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="2d45d-1665">Az.LogicApp</span></span>
* <span data-ttu-id="2d45d-1666">Grundläggande SKU har lagts till för Integrationskonton</span><span class="sxs-lookup"><span data-stu-id="2d45d-1666">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="2d45d-1667">XSLT 2.0, XSLT 3.0 och Flytande mappningstyper har lagts till</span><span class="sxs-lookup"><span data-stu-id="2d45d-1667">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="2d45d-1668">Nya cmdletar för integrationskontosammansättningar</span><span class="sxs-lookup"><span data-stu-id="2d45d-1668">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="2d45d-1669">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="2d45d-1669">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="2d45d-1670">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="2d45d-1670">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="2d45d-1671">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="2d45d-1671">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="2d45d-1672">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="2d45d-1672">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="2d45d-1673">Nya cmdletar för batchkonfiguration för integrationskonto</span><span class="sxs-lookup"><span data-stu-id="2d45d-1673">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="2d45d-1674">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="2d45d-1674">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="2d45d-1675">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="2d45d-1675">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="2d45d-1676">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="2d45d-1676">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="2d45d-1677">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="2d45d-1677">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="2d45d-1678">Logic App-SDK har uppdaterats till version 4.1.0</span><span class="sxs-lookup"><span data-stu-id="2d45d-1678">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2d45d-1679">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2d45d-1679">Az.Monitor</span></span>
* <span data-ttu-id="2d45d-1680">Hjälpen för Get-AzMetric har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="2d45d-1680">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d45d-1681">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d45d-1681">Az.Network</span></span>
* <span data-ttu-id="2d45d-1682">Hjälpexempel för Add-AzApplicationGatewayCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="2d45d-1682">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="2d45d-1683">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2d45d-1683">Az.OperationalInsights</span></span>
* <span data-ttu-id="2d45d-1684">Ytterligare stöd för datakällorna New och Get ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1684">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="2d45d-1685">Ny ApplicationInsights-typ har lagts till för att ge stöd för ”Get specific” och ”Get all” för ApplicationInsights-datakällor för angiven arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1685">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="2d45d-1686">Cmdleten New-AzOperationalInsightsApplicationInsightsDataSource har lagts till för att skapa datakälla med angivna parametrar för Application Insights-resurs: subscription Id, resourceGroupName och name.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1686">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d45d-1687">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d45d-1687">Az.Resources</span></span>
* <span data-ttu-id="2d45d-1688">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="2d45d-1688">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="2d45d-1689">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="2d45d-1689">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="2d45d-1690">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="2d45d-1690">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="2d45d-1691">Fel som gör att KeyCredentials inte kan skapas upprepade gånger har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="2d45d-1691">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d45d-1692">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d45d-1692">Az.Sql</span></span>
* <span data-ttu-id="2d45d-1693">Lägg till stöd för hyperskalanivån för SQL DB</span><span class="sxs-lookup"><span data-stu-id="2d45d-1693">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="2d45d-1694">Ett fel har åtgärdats där återställningen kunde misslyckas på grund av onödiga inställningsegenskaper i restore-förfrågan</span><span class="sxs-lookup"><span data-stu-id="2d45d-1694">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2d45d-1695">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2d45d-1695">Az.Websites</span></span>
* <span data-ttu-id="2d45d-1696">Rätt exempel i Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="2d45d-1696">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="2d45d-1697">1.3.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="2d45d-1697">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2d45d-1698">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d45d-1698">Az.Accounts</span></span>
* <span data-ttu-id="2d45d-1699">Uppdatera till den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="2d45d-1699">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="2d45d-1700">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="2d45d-1700">Az.AnalysisServices</span></span>
<span data-ttu-id="2d45d-1701">Allmän tillgänglighet för Az.AnalysisServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1701">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d45d-1702">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d45d-1702">Az.Compute</span></span>
* <span data-ttu-id="2d45d-1703">AEM-tillägg: Lägg till stöd för UltraSSD-, P60-, P70- och P80-diskar</span><span class="sxs-lookup"><span data-stu-id="2d45d-1703">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="2d45d-1704">Uppdatera hjälpbeskrivning för Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="2d45d-1704">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="2d45d-1705">Uppdatera hjälpbeskrivning och exempel för Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="2d45d-1705">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2d45d-1706">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d45d-1706">Az.RecoveryServices</span></span>
<span data-ttu-id="2d45d-1707">Allmän tillgänglighet för Az.RecoveryServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1707">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d45d-1708">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d45d-1708">Az.Resources</span></span>
* <span data-ttu-id="2d45d-1709">Korrigera taggar för resursgrupper</span><span class="sxs-lookup"><span data-stu-id="2d45d-1709">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="2d45d-1710">Mer information här: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="2d45d-1710">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="2d45d-1711">Åtgärda problem där `Get-AzureRmRoleAssignment` inte respekterar -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="2d45d-1711">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="2d45d-1712">Mer information här: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="2d45d-1712">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d45d-1713">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d45d-1713">Az.Sql</span></span>
* <span data-ttu-id="2d45d-1714">Lägga till Get/Set-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="2d45d-1714">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="2d45d-1715">Åtgärda problem där ett nullref-undantag uppstår när du kör SQL-cmdletar och inte är inloggad på ett Azure-konto</span><span class="sxs-lookup"><span data-stu-id="2d45d-1715">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="2d45d-1716">Åtgärda nullref-undantag i Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="2d45d-1716">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="2d45d-1717">1.2.1 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="2d45d-1717">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2d45d-1718">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d45d-1718">Az.Accounts</span></span>
* <span data-ttu-id="2d45d-1719">Version med rätt version av autentisering</span><span class="sxs-lookup"><span data-stu-id="2d45d-1719">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="2d45d-1720">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="2d45d-1720">Az.AnalysisServices</span></span>
* <span data-ttu-id="2d45d-1721">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="2d45d-1721">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2d45d-1722">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d45d-1722">Az.RecoveryServices</span></span>
* <span data-ttu-id="2d45d-1723">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="2d45d-1723">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="2d45d-1724">1.2.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="2d45d-1724">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2d45d-1725">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d45d-1725">Az.Accounts</span></span>
* <span data-ttu-id="2d45d-1726">Lägga till interaktiv autentisering och autentisering med användarnamn/lösenord för endast Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="2d45d-1726">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="2d45d-1727">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="2d45d-1727">Update incorrect online help URLs</span></span>
* <span data-ttu-id="2d45d-1728">Lägga till varningsmeddelande i PS Core för Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="2d45d-1728">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="2d45d-1729">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="2d45d-1729">Az.Aks</span></span>
* <span data-ttu-id="2d45d-1730">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="2d45d-1730">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2d45d-1731">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2d45d-1731">Az.Automation</span></span>
* <span data-ttu-id="2d45d-1732">Stöd för Python 2-runbookflöden har lagts till</span><span class="sxs-lookup"><span data-stu-id="2d45d-1732">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="2d45d-1733">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="2d45d-1733">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="2d45d-1734">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="2d45d-1734">Az.Cdn</span></span>
* <span data-ttu-id="2d45d-1735">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="2d45d-1735">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d45d-1736">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d45d-1736">Az.Compute</span></span>
* <span data-ttu-id="2d45d-1737">Lägga till cmdleten Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="2d45d-1737">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="2d45d-1738">Lägga till TempDisk-parameter i Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="2d45d-1738">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="2d45d-1739">Korrigera varningsmeddelande för New-AzVM</span><span class="sxs-lookup"><span data-stu-id="2d45d-1739">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="2d45d-1740">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="2d45d-1740">Az.ContainerRegistry</span></span>
* <span data-ttu-id="2d45d-1741">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="2d45d-1741">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2d45d-1742">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2d45d-1742">Az.DataFactory</span></span>
* <span data-ttu-id="2d45d-1743">ADF .Net SDK-versionen har uppdaterats till 3.0.0</span><span class="sxs-lookup"><span data-stu-id="2d45d-1743">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2d45d-1744">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2d45d-1744">Az.DataLakeStore</span></span>
* <span data-ttu-id="2d45d-1745">Åtgärda problem med ADLS-slutpunkt vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="2d45d-1745">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="2d45d-1746">Mer information här: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="2d45d-1746">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="2d45d-1747">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="2d45d-1747">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="2d45d-1748">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="2d45d-1748">Az.IotHub</span></span>
* <span data-ttu-id="2d45d-1749">Lägga till kodningsformat i cmdleten Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1749">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="2d45d-1750">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2d45d-1750">Az.KeyVault</span></span>
* <span data-ttu-id="2d45d-1751">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="2d45d-1751">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d45d-1752">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d45d-1752">Az.Network</span></span>
* <span data-ttu-id="2d45d-1753">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="2d45d-1753">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d45d-1754">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d45d-1754">Az.Resources</span></span>
* <span data-ttu-id="2d45d-1755">Åtgärda felaktiga exempel i referensdokumentationen ”New-AzADAppCredential” och ”New-AzADSpCredential”</span><span class="sxs-lookup"><span data-stu-id="2d45d-1755">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="2d45d-1756">Åtgärda problem där sökvägen för parametern ”-TemplateFile” inte omvandlas innan cmdletarna för distribution i resursgruppen körs</span><span class="sxs-lookup"><span data-stu-id="2d45d-1756">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="2d45d-1757">Az.Resources: Korrigera dokumentationen om standardvärdet för New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="2d45d-1757">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="2d45d-1758">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="2d45d-1758">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="2d45d-1759">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="2d45d-1759">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="2d45d-1760">Åtgärda formateringsproblemet med objektet ”PSResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="2d45d-1760">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="2d45d-1761">Mer information här: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="2d45d-1761">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="2d45d-1762">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2d45d-1762">Az.ServiceFabric</span></span>
* <span data-ttu-id="2d45d-1763">Återställ när ett certifikat läggs till i en Virtual Machine Scale Sets-modell men ett undantag genereras. Detta har gjorts för att åtgärda följande fel: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="2d45d-1763">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="2d45d-1764">Korrigera några felmeddelanden.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1764">Fix some error messages.</span></span>
* <span data-ttu-id="2d45d-1765">Korrigering av skapande av kluster med ARM-mall som är standard för New-AzServiceFabriCluster som inte fungerade med migrering till Az.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1765">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="2d45d-1766">Korrigering av tilläggning av kluster/programcertifikat så att endast VM Scale Sets som motsvarar klustret läggs till genom att kontrollera ID för klustret i tillägget.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1766">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="2d45d-1767">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="2d45d-1767">Az.SignalR</span></span>
* <span data-ttu-id="2d45d-1768">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="2d45d-1768">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d45d-1769">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d45d-1769">Az.Sql</span></span>
* <span data-ttu-id="2d45d-1770">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="2d45d-1770">Update incorrect online help URLs</span></span>
* <span data-ttu-id="2d45d-1771">Uppdaterad parameterbeskrivning för LicenseType-parameter med möjliga värden</span><span class="sxs-lookup"><span data-stu-id="2d45d-1771">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="2d45d-1772">Korrigering för att uppdatera hanterad instansidentitet som inte fungerar när det är den enda uppdaterade egenskapen</span><span class="sxs-lookup"><span data-stu-id="2d45d-1772">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="2d45d-1773">Stöd för anpassad sortering på hanterad instans</span><span class="sxs-lookup"><span data-stu-id="2d45d-1773">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2d45d-1774">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d45d-1774">Az.Storage</span></span>
* <span data-ttu-id="2d45d-1775">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="2d45d-1775">Update incorrect online help URLs</span></span>
* <span data-ttu-id="2d45d-1776">Tillhandahåll detaljerat felmeddelande när en användare försöker hämta/konfigurera klassisk loggning/mått på ett Premium Storage-konto eftersom Premium Storage-kontot inte har stöd för klassisk loggning/mått.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1776">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="2d45d-1777">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="2d45d-1777">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="2d45d-1778">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="2d45d-1778">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="2d45d-1779">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="2d45d-1779">Az.TrafficManager</span></span>
* <span data-ttu-id="2d45d-1780">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="2d45d-1780">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2d45d-1781">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2d45d-1781">Az.Websites</span></span>
* <span data-ttu-id="2d45d-1782">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="2d45d-1782">Update incorrect online help URLs</span></span>
* <span data-ttu-id="2d45d-1783">Korrigerar ”New-AzWebAppSSLBinding” så att certifikatet laddas upp till rätt resursgrupp och plats om appen finns i en ASE.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1783">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="2d45d-1784">Korrigerar ”New-AzWebAppSSLBinding” så att taggarna inte skrivs över på en bindning av ett SSL-certifikat till en app</span><span class="sxs-lookup"><span data-stu-id="2d45d-1784">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="2d45d-1785">1.1.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="2d45d-1785">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2d45d-1786">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d45d-1786">Az.Accounts</span></span>
* <span data-ttu-id="2d45d-1787">Lade till omfattningen ”Lokal” till Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="2d45d-1787">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d45d-1788">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d45d-1788">Az.Compute</span></span>
* <span data-ttu-id="2d45d-1789">Namn är nu valfritt i ID-parametern för Restart/Start/Stop/Remove/Set-AzVM och Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="2d45d-1789">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="2d45d-1790">Uppdaterade beskrivningen av ID i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="2d45d-1790">Updated the description of ID in help files</span></span>
* <span data-ttu-id="2d45d-1791">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d45d-1791">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2d45d-1792">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2d45d-1792">Az.DataLakeStore</span></span>
* <span data-ttu-id="2d45d-1793">Uppdatera sdk-versionen av dataplanet till 1.1.14 för SDK-korrigeringar.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1793">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="2d45d-1794">Korrigerade hanteringen av negativ accesstime och modificationtime för getfilestatus och liststatus; korrigera asynkront annulleringstoken</span><span class="sxs-lookup"><span data-stu-id="2d45d-1794">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="2d45d-1795">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="2d45d-1795">Az.EventGrid</span></span>
* <span data-ttu-id="2d45d-1796">Uppdaterat för användning av API-versionen 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1796">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="2d45d-1797">Uppdaterade följande cmdletar för att stödja nytt scenario i API-versionen 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="2d45d-1797">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="2d45d-1798">New-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="2d45d-1798">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="2d45d-1799">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="2d45d-1799">Event Time-To-Live,</span></span>
        - <span data-ttu-id="2d45d-1800">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="2d45d-1800">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="2d45d-1801">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1801">Dead letter endpoint.</span></span>
    - <span data-ttu-id="2d45d-1802">Update-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="2d45d-1802">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="2d45d-1803">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="2d45d-1803">Event Time-To-Live,</span></span>
        - <span data-ttu-id="2d45d-1804">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="2d45d-1804">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="2d45d-1805">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1805">Dead letter endpoint.</span></span>
* <span data-ttu-id="2d45d-1806">Lade till nya enum-värden (storageQueue och hybridConnection) för alternativet EndpointType i cmdletarna New-AzureRmEventGridSubscription och Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1806">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="2d45d-1807">Visa varningsmeddelanden om skapande eller uppdatering av händelseprenumerationen förväntas medföra manuell åtgärd från användaren.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1807">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="2d45d-1808">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="2d45d-1808">Az.IotHub</span></span>
* <span data-ttu-id="2d45d-1809">Har uppdaterats till den senaste versionen av SDK:n lotHub</span><span class="sxs-lookup"><span data-stu-id="2d45d-1809">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="2d45d-1810">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="2d45d-1810">Az.LogicApp</span></span>
* <span data-ttu-id="2d45d-1811">Get-AzLogicApp visar en lista över alla som inte har angivet namn</span><span class="sxs-lookup"><span data-stu-id="2d45d-1811">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d45d-1812">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d45d-1812">Az.Resources</span></span>
* <span data-ttu-id="2d45d-1813">Åtgärdade problem med parameteruppsättningen när parametrarna -ODataQuery och -ResourceId anges för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="2d45d-1813">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="2d45d-1814">Mer information här: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="2d45d-1814">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="2d45d-1815">Åtgärdade hantering av parametern -Custom i New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="2d45d-1815">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="2d45d-1816">Korrigerade stavfel i New-AzDeployment-dokumentationen</span><span class="sxs-lookup"><span data-stu-id="2d45d-1816">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="2d45d-1817">Gjorde parametern -MailNickname obligatorisk för New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="2d45d-1817">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="2d45d-1818">Mer information här: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="2d45d-1818">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="2d45d-1819">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="2d45d-1819">Az.SignalR</span></span>
* <span data-ttu-id="2d45d-1820">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d45d-1820">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d45d-1821">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d45d-1821">Az.Sql</span></span>
* <span data-ttu-id="2d45d-1822">Konverterade lagringshanteringsklientens beroende av den normala SDK-implementeringen.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1822">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2d45d-1823">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d45d-1823">Az.Storage</span></span>
* <span data-ttu-id="2d45d-1824">Angav StorageAccountName för lagringskontext som det verkliga namnet på lagringskontot när det skapas med Sas Token, OAuth eller Anonymous</span><span class="sxs-lookup"><span data-stu-id="2d45d-1824">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="2d45d-1825">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="2d45d-1825">New-AzStorageContext</span></span>
* <span data-ttu-id="2d45d-1826">Skapade Sas Token för Blob Snapshot-objekt med parametern -FullUri, åtgärdade den returnerade URI:n så att den blir URI för ögonblicksbild</span><span class="sxs-lookup"><span data-stu-id="2d45d-1826">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="2d45d-1827">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="2d45d-1827">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2d45d-1828">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2d45d-1828">Az.Websites</span></span>
* <span data-ttu-id="2d45d-1829">Åtgärdade en bugg i datumparsningen i Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="2d45d-1829">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="2d45d-1830">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d45d-1830">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="2d45d-1831">1.0.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="2d45d-1831">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="2d45d-1832">Allmänt</span><span class="sxs-lookup"><span data-stu-id="2d45d-1832">General</span></span>

- <span data-ttu-id="2d45d-1833">Allmän tillgänglighet för Az-modulen</span><span class="sxs-lookup"><span data-stu-id="2d45d-1833">General Availability of Az Module</span></span>
- <span data-ttu-id="2d45d-1834">Onlinehjälp för varje modul</span><span class="sxs-lookup"><span data-stu-id="2d45d-1834">Online help for each module</span></span>
- <span data-ttu-id="2d45d-1835">Mer information och en översikt finns på [Az-informationssidan](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="2d45d-1835">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="2d45d-1836">Information om hur du migrerar från AzureRM finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="2d45d-1836">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="2d45d-1837">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d45d-1837">Az.Accounts</span></span>
- <span data-ttu-id="2d45d-1838">Har ändrats från Az.Profile</span><span class="sxs-lookup"><span data-stu-id="2d45d-1838">Changed from Az.Profile</span></span>
- <span data-ttu-id="2d45d-1839">Fasta tabellformat för profil- och kontexttyper</span><span class="sxs-lookup"><span data-stu-id="2d45d-1839">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="2d45d-1840">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2d45d-1840">Az.ApiManagement</span></span>
- <span data-ttu-id="2d45d-1841">Korrigeringar för #7002</span><span class="sxs-lookup"><span data-stu-id="2d45d-1841">Fixes for #7002</span></span>
- <span data-ttu-id="2d45d-1842">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="2d45d-1842">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="2d45d-1843">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="2d45d-1843">Az.Batch</span></span>
- <span data-ttu-id="2d45d-1844">Lade till möjligheten att se vilken version av Azure Batch Node Agent som körs på var och en av de virtuella datorerna i en pool, via den nya egenskapen `NodeAgentInformation` på `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1844">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="2d45d-1845">Standarden `Caching` för `PSDataDisk` är nu `ReadWrite` i stället för `None`.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1845">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="2d45d-1846">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="2d45d-1846">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="2d45d-1847">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="2d45d-1847">Az.Billing</span></span>
- <span data-ttu-id="2d45d-1848">Kombinerar cmdletarna för fakturering, förbrukning och UsageAggregates. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="2d45d-1848">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="2d45d-1849">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="2d45d-1849">Az.CognitivServices</span></span>
- <span data-ttu-id="2d45d-1850">Lade till kompletterare för SkuName och Typem som är tillgängliga i New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="2d45d-1850">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="2d45d-1851">Tog bort parameteruppsättningen GetSkusWithAccountParamSetName från Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="2d45d-1851">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="2d45d-1852">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="2d45d-1852">Az.ContainerInstance</span></span>
- <span data-ttu-id="2d45d-1853">Stöd för ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="2d45d-1853">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="2d45d-1854">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="2d45d-1854">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="2d45d-1855">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="2d45d-1855">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="2d45d-1856">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2d45d-1856">Az.DataLakeStore</span></span>
- <span data-ttu-id="2d45d-1857">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="2d45d-1857">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="2d45d-1858">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2d45d-1858">Az.Monitor</span></span>
- <span data-ttu-id="2d45d-1859">Döpte om Az.Insights till Az.Monitor och andra mindre icke-bakåtkompatibla ändringar. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="2d45d-1859">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="2d45d-1860">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2d45d-1860">Az.KeyVault</span></span>
- <span data-ttu-id="2d45d-1861">Tog bort den inaktuella egenskapen PurgeDisabled från utdatatyper</span><span class="sxs-lookup"><span data-stu-id="2d45d-1861">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="2d45d-1862">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="2d45d-1862">Az.MachineLearning</span></span>
- <span data-ttu-id="2d45d-1863">Inkluderade cmdletarna från modulen Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="2d45d-1863">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="2d45d-1864">Az.Media</span><span class="sxs-lookup"><span data-stu-id="2d45d-1864">Az.Media</span></span>
- <span data-ttu-id="2d45d-1865">Tog bort inaktuella -Tags-alias från New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="2d45d-1865">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="2d45d-1866">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d45d-1866">Az.Network</span></span>
<span data-ttu-id="2d45d-1867">Stöd har lagts till för konfiguration av RewriteRuleSets i Application Gateway</span><span class="sxs-lookup"><span data-stu-id="2d45d-1867">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="2d45d-1868">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="2d45d-1868">New cmdlets added:</span></span>
        - <span data-ttu-id="2d45d-1869">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2d45d-1869">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="2d45d-1870">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2d45d-1870">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="2d45d-1871">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2d45d-1871">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="2d45d-1872">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2d45d-1872">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="2d45d-1873">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2d45d-1873">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="2d45d-1874">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="2d45d-1874">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="2d45d-1875">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="2d45d-1875">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="2d45d-1876">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="2d45d-1876">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="2d45d-1877">Cmdletar har uppdaterats med den valfria parametern -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2d45d-1877">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="2d45d-1878">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2d45d-1878">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="2d45d-1879">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="2d45d-1879">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="2d45d-1880">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="2d45d-1880">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="2d45d-1881">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2d45d-1881">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="2d45d-1882">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="2d45d-1882">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="2d45d-1883">New-AzureRmApplicationGatewayUrlPathMapConfig har lagt till KeyVault-stöd för Application Gateway med Identity.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1883">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="2d45d-1884">Cmdletar har uppdaterats med den valfria parametern -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="2d45d-1884">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="2d45d-1885">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="2d45d-1885">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="2d45d-1886">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="2d45d-1886">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="2d45d-1887">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="2d45d-1887">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="2d45d-1888">Cmdleten New-AzApplicationGateway har uppdaterats med den valfria parametern -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="2d45d-1888">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="2d45d-1889">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="2d45d-1889">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="2d45d-1890">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2d45d-1890">Az.OperationalInsights</span></span>
- <span data-ttu-id="2d45d-1891">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="2d45d-1891">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="2d45d-1892">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="2d45d-1892">Az.Profile</span></span>
- <span data-ttu-id="2d45d-1893">Modulnamnet har ändrats till Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d45d-1893">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="2d45d-1894">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d45d-1894">Az.RecoveryServices</span></span>
- <span data-ttu-id="2d45d-1895">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="2d45d-1895">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="2d45d-1896">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d45d-1896">Az.Resources</span></span>
- <span data-ttu-id="2d45d-1897">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="2d45d-1897">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="2d45d-1898">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2d45d-1898">Az.ServiceFabric</span></span>
- <span data-ttu-id="2d45d-1899">Stöd för specificering av certifikat efter eget namn och tumavtryck</span><span class="sxs-lookup"><span data-stu-id="2d45d-1899">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="2d45d-1900">Information om fler icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="2d45d-1900">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="2d45d-1901">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="2d45d-1901">Az.SIgnalR</span></span>
- <span data-ttu-id="2d45d-1902">Allmän tillgänglighet för PowerShell-cmdletar för SIgnalR</span><span class="sxs-lookup"><span data-stu-id="2d45d-1902">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="2d45d-1903">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d45d-1903">Az.Sql</span></span>
- <span data-ttu-id="2d45d-1904">Lade till de nya identifieringstyperna Data_Exfiltration och Unsafe_Action i Threat Detection-cmdletar</span><span class="sxs-lookup"><span data-stu-id="2d45d-1904">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="2d45d-1905">Uppdaterade dokumentationsexempel för Sql Auditing-cmdletar</span><span class="sxs-lookup"><span data-stu-id="2d45d-1905">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="2d45d-1906">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="2d45d-1906">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="2d45d-1907">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d45d-1907">Az.Storage</span></span>
- <span data-ttu-id="2d45d-1908">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="2d45d-1908">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="2d45d-1909">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2d45d-1909">Az.Websites</span></span>
- <span data-ttu-id="2d45d-1910">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="2d45d-1910">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="2d45d-1911">0.7.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="2d45d-1911">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="2d45d-1912">Allmänt</span><span class="sxs-lookup"><span data-stu-id="2d45d-1912">General</span></span>

* <span data-ttu-id="2d45d-1913">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="2d45d-1913">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="2d45d-1914">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d45d-1914">Az.Compute</span></span>

* <span data-ttu-id="2d45d-1915">Lade till stöd för UltraSSD och Galleriavbildningar i de enkla parameteruppsättningarna för `New-AzVm(ss)`-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1915">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="2d45d-1916">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2d45d-1916">Az.DataLakeStore</span></span>

* <span data-ttu-id="2d45d-1917">Åtgärdade avslutande snedstreck i domänen för adls-konto</span><span class="sxs-lookup"><span data-stu-id="2d45d-1917">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="2d45d-1918">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="2d45d-1918">Az.FrontDoor</span></span>

* <span data-ttu-id="2d45d-1919">Brutna länkar korrigerades</span><span class="sxs-lookup"><span data-stu-id="2d45d-1919">Fixed some broken links</span></span>
    - <span data-ttu-id="2d45d-1920">I artiklarna New-AzureRmFrontDoor och Set-AzureRmFrontDoor artiklar korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1920">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="2d45d-1921">I artikeln New-AzureRmFrontDoorManagedRuleObject korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1921">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="2d45d-1922">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d45d-1922">Az.RecoveryServices</span></span>

* <span data-ttu-id="2d45d-1923">Lade till valideringar på klientsidan för Azure-filresurs med återställningsåtgärder.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1923">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="2d45d-1924">Gjorde storageAccountName och storageAccountResourceGroupName valfritt för afs-återställning.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1924">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="2d45d-1925">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d45d-1925">Az.Resources</span></span>

* <span data-ttu-id="2d45d-1926">Korrigering för https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="2d45d-1926">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="2d45d-1927">Uppdaterade Get-AzureRmRoleAssignment så att prenumerationsomfattningen används om den anges vid begäran om klassiska administratörer.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1927">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="2d45d-1928">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d45d-1928">Az.Sql</span></span>

* <span data-ttu-id="2d45d-1929">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="2d45d-1929">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="2d45d-1930">Korrigerade ett problem med Get-AzureRmSqlDatabaseVulnerabilityAssessment med DotNet-kärna</span><span class="sxs-lookup"><span data-stu-id="2d45d-1930">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="2d45d-1931">Ändrade dokumentationen för hjälpmeddelanden som rör SQL Auditing-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1931">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="2d45d-1932">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d45d-1932">Az.Storage</span></span>

* <span data-ttu-id="2d45d-1933">Lade till -EnableHierarchicalNamespace i New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2d45d-1933">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="2d45d-1934">Åtgärdade problemet med att cmdleten Copy File inte kunde återanvända källkontexten på målet om inte -DestContext angetts</span><span class="sxs-lookup"><span data-stu-id="2d45d-1934">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="2d45d-1935">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="2d45d-1935">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="2d45d-1936">Stöd för statisk webbplatskonfiguration</span><span class="sxs-lookup"><span data-stu-id="2d45d-1936">Support Static Website configuration</span></span>
    - <span data-ttu-id="2d45d-1937">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="2d45d-1937">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="2d45d-1938">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="2d45d-1938">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="2d45d-1939">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2d45d-1939">Az.Websites</span></span>

* <span data-ttu-id="2d45d-1940">Set-AzureRmWebApp och Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2d45d-1940">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="2d45d-1941">Ny parameter (-AzureStoragePath) har lagts till för att ange att Azure Storage-sökvägar ska monteras i containerappar i Windows och Linux.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1941">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="2d45d-1942">Använder utdata från den nya cmdleten New-AzureRmWebAppAzureStoragePath som en parameter för att ange sökvägar för Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1942">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="2d45d-1943">0.6.1 – november 2018</span><span class="sxs-lookup"><span data-stu-id="2d45d-1943">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="2d45d-1944">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2d45d-1944">Az.ApiManagement</span></span>
* <span data-ttu-id="2d45d-1945">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="2d45d-1945">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="2d45d-1946">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2d45d-1946">Az.Automation</span></span>
* <span data-ttu-id="2d45d-1947">Swagger baserade Azure Automation-cmdletar</span><span class="sxs-lookup"><span data-stu-id="2d45d-1947">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="2d45d-1948">Cmdletar för Uppdateringshantering har lagts till</span><span class="sxs-lookup"><span data-stu-id="2d45d-1948">Added Update Management cmdlets</span></span>
* <span data-ttu-id="2d45d-1949">Cmdletar för källkontroll har lagts till</span><span class="sxs-lookup"><span data-stu-id="2d45d-1949">Added Source Control cmdlets</span></span>
* <span data-ttu-id="2d45d-1950">Remove-AzureRmAutomationHybridWorkerGroup-cmdlet har lagts till</span><span class="sxs-lookup"><span data-stu-id="2d45d-1950">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="2d45d-1951">Kommandot för DSC-registreringsnod har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="2d45d-1951">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="2d45d-1952">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d45d-1952">Az.Compute</span></span>
* <span data-ttu-id="2d45d-1953">Problem med SystemAssigned-identitet har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="2d45d-1953">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="2d45d-1954">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="2d45d-1954">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="2d45d-1955">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="2d45d-1955">Az.ContainerInstance</span></span>
* <span data-ttu-id="2d45d-1956">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="2d45d-1956">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="2d45d-1957">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="2d45d-1957">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="2d45d-1958">uppdatera exempelbeskrivningen för marketplace-cmdletar</span><span class="sxs-lookup"><span data-stu-id="2d45d-1958">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="2d45d-1959">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d45d-1959">Az.Network</span></span>
* <span data-ttu-id="2d45d-1960">Cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomErreller Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="2d45d-1960">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="2d45d-1961">ICMP tillbaka till stöd för Azure Firewall-nätverksprotokoll har lagts till</span><span class="sxs-lookup"><span data-stu-id="2d45d-1961">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="2d45d-1962">Uppdatera cmdlet Test-AzureRmNetworkWatcherConnectivity, lägga till verifiering av mål-id, adress och port.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1962">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="2d45d-1963">Åtgärda problem med minnesanvändning i VirtualNetwork-karta</span><span class="sxs-lookup"><span data-stu-id="2d45d-1963">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="2d45d-1964">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="2d45d-1964">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="2d45d-1965">Åtgärda för att ändra principen för en skyddad fildelning.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1965">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="2d45d-1966">Tidszonsprincipen har konverterats till versaler.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1966">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="2d45d-1967">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="2d45d-1967">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="2d45d-1968">Exempel i New-AzureRmRecoveryServicesAsrProtectableItem har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="2d45d-1968">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="2d45d-1969">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="2d45d-1969">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="2d45d-1970">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="2d45d-1970">Az.Relay</span></span>
* <span data-ttu-id="2d45d-1971">Valfri parameter -KeyValue till New-AzureRmRelayKey cmdlet har lagts till, vilket gör det möjligt för användare att tillhandahålla KeyValue.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1971">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="2d45d-1972">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d45d-1972">Az.Resources</span></span>
* <span data-ttu-id="2d45d-1973">Uppdatera hjälpdokumentation för resursidentitet kopplad till parametrar i `New-AzureRmPolicyAssignment` och `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="2d45d-1973">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="2d45d-1974">Lägg till ett exempel för New-AzureRmPolicyDefinition som använder -Metadata</span><span class="sxs-lookup"><span data-stu-id="2d45d-1974">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="2d45d-1975">Korrigera så att skiftläge behålls i taggnycklar i NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="2d45d-1975">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="2d45d-1976">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2d45d-1976">Az.ServiceFabric</span></span>
* <span data-ttu-id="2d45d-1977">Lägg till utfasningsmeddelanden för kommande icke-kompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="2d45d-1977">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="2d45d-1978">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d45d-1978">Az.Sql</span></span>
* <span data-ttu-id="2d45d-1979">Nya cmdletar för CRUD-åtgärder på Azure Sql Database-hanterad instans och Azure Sql-hanterad databas</span><span class="sxs-lookup"><span data-stu-id="2d45d-1979">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="2d45d-1980">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="2d45d-1980">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="2d45d-1981">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="2d45d-1981">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="2d45d-1982">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="2d45d-1982">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="2d45d-1983">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="2d45d-1983">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="2d45d-1984">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="2d45d-1984">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="2d45d-1985">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="2d45d-1985">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="2d45d-1986">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="2d45d-1986">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="2d45d-1987">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="2d45d-1987">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="2d45d-1988">Hantering av utökad granskningsprincip på en server eller en databas har aktiverats.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1988">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="2d45d-1989">Ny parameter (PredicateExpression) har lagts till för att aktivera filtrering av granskningsloggar.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1989">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="2d45d-1990">Cmdletar har ändrats så att de använder SQL-klienter i stället för äldre klienter.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1990">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="2d45d-1991">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1991">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="2d45d-1992">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1992">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="2d45d-1993">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1993">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="2d45d-1994">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="2d45d-1994">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="2d45d-1995">Problem med att använda Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings med lagringskontots namnparameter har korrigerats</span><span class="sxs-lookup"><span data-stu-id="2d45d-1995">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="2d45d-1996">0.5.0 – november 2018</span><span class="sxs-lookup"><span data-stu-id="2d45d-1996">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="2d45d-1997">Allmänt</span><span class="sxs-lookup"><span data-stu-id="2d45d-1997">General</span></span>
* <span data-ttu-id="2d45d-1998">Lade till resurskompletterare till många kärn-cmdletar – dessa gör att du kan stega genom befintliga resursnamn med TABB vid interaktiva anrop till cmdletar</span><span class="sxs-lookup"><span data-stu-id="2d45d-1998">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="2d45d-1999">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="2d45d-1999">Az.Profile</span></span>
* <span data-ttu-id="2d45d-2000">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="2d45d-2000">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="2d45d-2001">Bytte namn på parametern TenantId i cmdleten Connect-AzAccount till Tenant och lade till ett alias för TenantId</span><span class="sxs-lookup"><span data-stu-id="2d45d-2001">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="2d45d-2002">Uppdaterade TenantId-beskrivningen för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="2d45d-2002">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="2d45d-2003">Åtgärda felmeddelande för misslyckad inloggning när du tillhandahåller klientdomän</span><span class="sxs-lookup"><span data-stu-id="2d45d-2003">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="2d45d-2004">Åtgärda problem med att kontextnamn hamnar i konflikt för konton utan prenumerationer i klientorganisationen</span><span class="sxs-lookup"><span data-stu-id="2d45d-2004">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="2d45d-2005">Åtgärda problem med DataLake-slutpunkter vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="2d45d-2005">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="2d45d-2006">Åtgärdade problem med att Disconnect-AzAccount kastades om den inte anslöts</span><span class="sxs-lookup"><span data-stu-id="2d45d-2006">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="2d45d-2007">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="2d45d-2007">Az.CognitiveServices</span></span>
* <span data-ttu-id="2d45d-2008">Lade till åtgärden Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="2d45d-2008">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d45d-2009">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d45d-2009">Az.Compute</span></span>
* <span data-ttu-id="2d45d-2010">Lade till cmdletarna Add-AzVmssVMDataDisk och Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="2d45d-2010">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="2d45d-2011">Get-AzVMImage visar AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="2d45d-2011">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="2d45d-2012">Åtgärdade att värdena för alternativen SetAzVMChefExtension -BootstrapOptions och -JsonAttribute inte angavs i json-format.</span><span class="sxs-lookup"><span data-stu-id="2d45d-2012">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2d45d-2013">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2d45d-2013">Az.DataLakeStore</span></span>
* <span data-ttu-id="2d45d-2014">Uppdatera DataLake-paketet till 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="2d45d-2014">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="2d45d-2015">Lägg till standardsamtidighet för flertrådade åtgärder.</span><span class="sxs-lookup"><span data-stu-id="2d45d-2015">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="2d45d-2016">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="2d45d-2016">Az.Insights</span></span>
* <span data-ttu-id="2d45d-2017">Åtgärdade problem #7267 (autoskalningsområde)</span><span class="sxs-lookup"><span data-stu-id="2d45d-2017">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="2d45d-2018">Problem med att uppräknade parametrar inte ställdes in ordentligt när du skapade en ny autoskalningsregel (de ställdes alltid in med standardvärdet).</span><span class="sxs-lookup"><span data-stu-id="2d45d-2018">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="2d45d-2019">Åtgärdade problem #7513 [Insights] Set-AzDiagnosticSetting kräver uttrycklig specifikation av kategorier när inställningar skapas</span><span class="sxs-lookup"><span data-stu-id="2d45d-2019">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="2d45d-2020">Nu kräver inte cmdleten uttrycklig anvisning av kategorierna för att aktiveras under skapande, d.v.s. den fungerar enligt beskrivning</span><span class="sxs-lookup"><span data-stu-id="2d45d-2020">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d45d-2021">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d45d-2021">Az.Network</span></span>
* <span data-ttu-id="2d45d-2022">PeeringType ändrades till en obligatorisk parameter för följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="2d45d-2022">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="2d45d-2023">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="2d45d-2023">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="2d45d-2024">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="2d45d-2024">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="2d45d-2025">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="2d45d-2025">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="2d45d-2026">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="2d45d-2026">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="2d45d-2027">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="2d45d-2027">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="2d45d-2028">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="2d45d-2028">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="2d45d-2029">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="2d45d-2029">Az.PolicyInsights</span></span>
* <span data-ttu-id="2d45d-2030">Cmdletar för principreparation har lagts till</span><span class="sxs-lookup"><span data-stu-id="2d45d-2030">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d45d-2031">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d45d-2031">Az.Resources</span></span>
* <span data-ttu-id="2d45d-2032">Korrigering för https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="2d45d-2032">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="2d45d-2033">Tillåt att resurser listas med parametern -ResourceId för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="2d45d-2033">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="2d45d-2034">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="2d45d-2034">Az.ServiceBus</span></span>
* <span data-ttu-id="2d45d-2035">Skrivskyddad MigrationState-egenskap har lagts till i PSServiceBusMigrationConfigurationAttributes, som hjälper till att hålla koll på migreringstillståndet.</span><span class="sxs-lookup"><span data-stu-id="2d45d-2035">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="2d45d-2036">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2d45d-2036">Az.ServiceFabric</span></span>
* <span data-ttu-id="2d45d-2037">Åtgärda att lägga till certifikat till Linux-Vmss.</span><span class="sxs-lookup"><span data-stu-id="2d45d-2037">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="2d45d-2038">Åtgärdade Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="2d45d-2038">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="2d45d-2039">Använd rätt tumavtryck från nya certifikat (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="2d45d-2039">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="2d45d-2040">Visa undantag korrekt (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="2d45d-2040">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="2d45d-2041">Åtgärdade Update-AzServiceFabricDurability så att klusterkonfigurationen uppdateras innan Vmss-åtgärden CreateOrUpdate påbörjas.</span><span class="sxs-lookup"><span data-stu-id="2d45d-2041">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="2d45d-2042">0.4.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="2d45d-2042">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="2d45d-2043">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="2d45d-2043">Az.Profile</span></span>
* <span data-ttu-id="2d45d-2044">Åtgärdade problemet med Get-AzSubscription i CloudShell</span><span class="sxs-lookup"><span data-stu-id="2d45d-2044">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="2d45d-2045">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="2d45d-2045">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d45d-2046">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d45d-2046">Az.Compute</span></span>
* <span data-ttu-id="2d45d-2047">Nya storlekar lades till i listan över godkända VM-storlekar för vilka accelererat nätverk kommer att aktiveras vid användning av den enkla parameteruppsättningen för New-AzVm</span><span class="sxs-lookup"><span data-stu-id="2d45d-2047">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="2d45d-2048">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="2d45d-2048">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2d45d-2049">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2d45d-2049">Az.DataLakeStore</span></span>
* <span data-ttu-id="2d45d-2050">Lägger till stöd för regler för virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="2d45d-2050">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="2d45d-2051">Get-AzDataLakeStoreVirtualNetworkRule: Hämtar eller listar regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2d45d-2051">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="2d45d-2052">Add-AzDataLakeStoreVirtualNetworkRule: Lägger till en regel för virtuellt nätverk i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="2d45d-2052">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="2d45d-2053">Set-AzDataLakeStoreVirtualNetworkRule: Ändrar den angivna regeln för virtuellt nätverk i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="2d45d-2053">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="2d45d-2054">Remove-AzDataLakeStoreVirtualNetworkRule: Tar bort en regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2d45d-2054">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d45d-2055">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d45d-2055">Az.Network</span></span>
* <span data-ttu-id="2d45d-2056">Skicka protokollvärdet till serverdelen för att uppdatera cmdleten Test-AzNetworkWatcherConnectivity.</span><span class="sxs-lookup"><span data-stu-id="2d45d-2056">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="2d45d-2057">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="2d45d-2057">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d45d-2058">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d45d-2058">Az.Resources</span></span>
* <span data-ttu-id="2d45d-2059">Åtgärdade problem där Get-AzRoleDefinition genererar ett oläsligt undantag (när standardprofilen inte innehåller någon prenumeration och ingen omfattning har angetts) genom att lägga till ett beskrivande undantag i scenariot.</span><span class="sxs-lookup"><span data-stu-id="2d45d-2059">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="2d45d-2060">Ställ in ”RoleDefinitionNameParameterSet” som standardparameteruppsättning.</span><span class="sxs-lookup"><span data-stu-id="2d45d-2060">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="2d45d-2061">0.3.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="2d45d-2061">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="2d45d-2062">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="2d45d-2062">Azure.Storage</span></span>
* <span data-ttu-id="2d45d-2063">Åtgärda fel där Kopiera blob/fil inte kopierar metadata när målplatsen har ett problem med metadata</span><span class="sxs-lookup"><span data-stu-id="2d45d-2063">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="2d45d-2064">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="2d45d-2064">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="2d45d-2065">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="2d45d-2065">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="2d45d-2066">Stöd för att hämta användningsinformation om en Storage-resurs för en specifik plats och för att lägga till ett varningsmeddelande för att hämta användningsinformation om en global Storage-resurs är inaktuellt.</span><span class="sxs-lookup"><span data-stu-id="2d45d-2066">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="2d45d-2067">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="2d45d-2067">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="2d45d-2068">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="2d45d-2068">Az.CognitiveServices</span></span>
* <span data-ttu-id="2d45d-2069">Stöd för Get-AzCognitiveServicesAccountSkus utan ett befintligt konto.</span><span class="sxs-lookup"><span data-stu-id="2d45d-2069">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d45d-2070">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d45d-2070">Az.Compute</span></span>
* <span data-ttu-id="2d45d-2071">Åtgärdade fel där Get-AzVM -ResourceGroupName <rg> returnerar fler än 50 resultat om det behövs</span><span class="sxs-lookup"><span data-stu-id="2d45d-2071">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="2d45d-2072">Lade till ett exempel för SimpleParameterSet i hjälpen för cmdleten New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="2d45d-2072">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="2d45d-2073">Ett stavfel i förloppsmeddelandet för Azure Disk Encryption har korrigerats</span><span class="sxs-lookup"><span data-stu-id="2d45d-2073">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="2d45d-2074">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="2d45d-2074">Az.DataFactoryV2</span></span>
* <span data-ttu-id="2d45d-2075">ADF .Net SDK-versionen har uppdaterats till 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="2d45d-2075">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d45d-2076">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d45d-2076">Az.Network</span></span>
* <span data-ttu-id="2d45d-2077">Funktionalitet för NetworkProfile har lagts till.</span><span class="sxs-lookup"><span data-stu-id="2d45d-2077">Added NetworkProfile functionality.</span></span> <span data-ttu-id="2d45d-2078">nya cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="2d45d-2078">new cmdlets added</span></span>
    - <span data-ttu-id="2d45d-2079">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="2d45d-2079">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="2d45d-2080">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="2d45d-2080">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="2d45d-2081">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="2d45d-2081">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="2d45d-2082">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="2d45d-2082">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="2d45d-2083">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="2d45d-2083">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="2d45d-2084">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="2d45d-2084">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="2d45d-2085">Länk för tjänstassociering på modell för undernät har lagts till</span><span class="sxs-lookup"><span data-stu-id="2d45d-2085">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="2d45d-2086">Cmdletarna New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap och Remove-AzVirtualNetworkTap har lagts till</span><span class="sxs-lookup"><span data-stu-id="2d45d-2086">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="2d45d-2087">Cmdletarna Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig och Remove-AzNEtworkInterfaceTapConfig har lagts till</span><span class="sxs-lookup"><span data-stu-id="2d45d-2087">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="2d45d-2088">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="2d45d-2088">Az.RedisCache</span></span>
* <span data-ttu-id="2d45d-2089">Tillåt att alla strängar används som storleksparametrar framöver.</span><span class="sxs-lookup"><span data-stu-id="2d45d-2089">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="2d45d-2090">Lägg till P5 i popup-fönstret PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="2d45d-2090">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d45d-2091">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d45d-2091">Az.Resources</span></span>
* <span data-ttu-id="2d45d-2092">Parametern -Mode som saknades i Set-AzPolicyDefinition har lagts till</span><span class="sxs-lookup"><span data-stu-id="2d45d-2092">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="2d45d-2093">Åtgärdade buggen för cmdleten Get-AzProviderOperation för åtgärder med ursprung som innehåller användare</span><span class="sxs-lookup"><span data-stu-id="2d45d-2093">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d45d-2094">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d45d-2094">Az.Sql</span></span>
* <span data-ttu-id="2d45d-2095">Ett problem där vissa cmdletar för säkerhetskopiering inte kunde identifiera den aktuella azure-prenumerationen har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="2d45d-2095">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2d45d-2096">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2d45d-2096">Az.Websites</span></span>
* <span data-ttu-id="2d45d-2097">Ny cmdlet: Get-AzWebAppContainerContinuousDeploymentUrl – Hämtar webhook-URL:en för kontinuerlig distribution av container</span><span class="sxs-lookup"><span data-stu-id="2d45d-2097">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="2d45d-2098">Nya cmdletar: New-AzWebAppContainerPSSession och Enter-WebAppContainerPSSession – Startar en PowerShell-fjärrsession i en containerapp för windows</span><span class="sxs-lookup"><span data-stu-id="2d45d-2098">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="2d45d-2099">0.2.0 – september 2018</span><span class="sxs-lookup"><span data-stu-id="2d45d-2099">0.2.0 - September 2018</span></span>
 <span data-ttu-id="2d45d-2100">Första versionen</span><span class="sxs-lookup"><span data-stu-id="2d45d-2100">Initial Release</span></span>
