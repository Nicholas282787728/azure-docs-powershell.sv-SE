---
title: Viktig information om Azure PowerShell
description: Lär dig mer om alla de senaste uppdateringarna för Azure PowerShell-modulerna.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.openlocfilehash: 9e60e76206127922902804112e0b3f837cf03d76
ms.sourcegitcommit: eeb720e053939a68873ae3973bc81d5826358c9f
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2020
ms.locfileid: "80440511"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="4f44c-103">Viktig information om Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="4f44c-103">Azure PowerShell release notes</span></span>
## <a name="370---march-2020"></a><span data-ttu-id="4f44c-104">3.7.0 – mars 2020</span><span class="sxs-lookup"><span data-stu-id="4f44c-104">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4f44c-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4f44c-105">Az.Accounts</span></span>
* <span data-ttu-id="4f44c-106">Åtgärdade ”Get-AzTenant”/”Get-AzDefault”/”Set-AzDefault”-utlösning av NullReferenceException när du inte är inloggad [#10292]</span><span class="sxs-lookup"><span data-stu-id="4f44c-106">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4f44c-107">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4f44c-107">Az.Compute</span></span>
* <span data-ttu-id="4f44c-108">Följande parametrar har lagts till i cmdleten ”New-AzDiskConfig”:</span><span class="sxs-lookup"><span data-stu-id="4f44c-108">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span> 
    - <span data-ttu-id="4f44c-109">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="4f44c-109">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="4f44c-110">Tillåten krypteringsegenskap till målparametern för cmdleten ”New-AzGalleryImageVersion”.</span><span class="sxs-lookup"><span data-stu-id="4f44c-110">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="4f44c-111">Åtgärdade tempDisk-problem för cmdletarna ”Set-AzVmss”-Reimage och ”Invoke-AzVMReimage”.</span><span class="sxs-lookup"><span data-stu-id="4f44c-111">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="4f44c-112">[#11354]</span><span class="sxs-lookup"><span data-stu-id="4f44c-112">[#11354]</span></span>
* <span data-ttu-id="4f44c-113">Stöd har lagts till i nedanstående cmdletar för nytt SAP-tillägg</span><span class="sxs-lookup"><span data-stu-id="4f44c-113">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="4f44c-114">”Set-AzVMAEMExtension”</span><span class="sxs-lookup"><span data-stu-id="4f44c-114">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="4f44c-115">”Get-AzVMAEMExtension”</span><span class="sxs-lookup"><span data-stu-id="4f44c-115">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="4f44c-116">”Remove-AzVMAEMExtension”</span><span class="sxs-lookup"><span data-stu-id="4f44c-116">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="4f44c-117">”Update-AzVMAEMExtension”</span><span class="sxs-lookup"><span data-stu-id="4f44c-117">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="4f44c-118">Åtgärdade fel i exempel på hjälpdokument</span><span class="sxs-lookup"><span data-stu-id="4f44c-118">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="4f44c-119">Visade det exakta strängvärdet för VM PowerState i tabellformat.</span><span class="sxs-lookup"><span data-stu-id="4f44c-119">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="4f44c-120">”New-AzVmssConfig”: den fasta serialiseringen av egenskapen AutomaticRepairs när SinglePlacementGroup är inaktiverad.</span><span class="sxs-lookup"><span data-stu-id="4f44c-120">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="4f44c-121">[#11257]</span><span class="sxs-lookup"><span data-stu-id="4f44c-121">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4f44c-122">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4f44c-122">Az.DataFactory</span></span>
* <span data-ttu-id="4f44c-123">ADF .Net SDK har uppdaterats till 4.8.0</span><span class="sxs-lookup"><span data-stu-id="4f44c-123">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="4f44c-124">Valfria parametrar har lagts till i kommandot ”Invoke-AzDataFactoryV2Pipeline” för att stödja omkörning</span><span class="sxs-lookup"><span data-stu-id="4f44c-124">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4f44c-125">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4f44c-125">Az.DataLakeStore</span></span>
* <span data-ttu-id="4f44c-126">Lade till beskrivning för icke-bakåtkompatibel ändring för ”Export-AzDataLakeStoreItem” och ”Import-AzDataLakeStoreItem”</span><span class="sxs-lookup"><span data-stu-id="4f44c-126">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="4f44c-127">Lade till alternativ för bytekodning för ”New-AzDataLakeStoreItem”, ”Add-AzDAtaLakeStoreItemContent” och ”Get-AzDAtaLakeStoreItemContent”</span><span class="sxs-lookup"><span data-stu-id="4f44c-127">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="4f44c-128">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="4f44c-128">Az.HDInsight</span></span>
* <span data-ttu-id="4f44c-129">Stöd för att ange en minimal TLS-version som stöds när klustret skapas.</span><span class="sxs-lookup"><span data-stu-id="4f44c-129">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="4f44c-130">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="4f44c-130">Az.IotHub</span></span>
* <span data-ttu-id="4f44c-131">Stöd har lagts till för att hantera distribuerade inställningar per enhet.</span><span class="sxs-lookup"><span data-stu-id="4f44c-131">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="4f44c-132">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="4f44c-132">New Cmdlets are:</span></span>
    - <span data-ttu-id="4f44c-133">”Get-AzIotHubDistributedTracing”</span><span class="sxs-lookup"><span data-stu-id="4f44c-133">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="4f44c-134">”Set-AzIotHubDistributedTracing”</span><span class="sxs-lookup"><span data-stu-id="4f44c-134">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="4f44c-135">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4f44c-135">Az.KeyVault</span></span>
* <span data-ttu-id="4f44c-136">Ändrade attribut för icke-bakåtkompatibel ändring lades till för ”New-AzKeyVault”</span><span class="sxs-lookup"><span data-stu-id="4f44c-136">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4f44c-137">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4f44c-137">Az.Monitor</span></span>
* <span data-ttu-id="4f44c-138">Uppdaterad dokumentation för ”New-AzScheduledQueryRuleLogMetricTrigger”</span><span class="sxs-lookup"><span data-stu-id="4f44c-138">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4f44c-139">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4f44c-139">Az.Network</span></span>
* <span data-ttu-id="4f44c-140">Uppdaterade cmdletar för att tillåta VirtualHubVnetConnections mellan klienter</span><span class="sxs-lookup"><span data-stu-id="4f44c-140">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="4f44c-141">”New-AzVirtualHubVnetConnection”</span><span class="sxs-lookup"><span data-stu-id="4f44c-141">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="4f44c-142">”Update-AzVirtualHubVnetConnection”</span><span class="sxs-lookup"><span data-stu-id="4f44c-142">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="4f44c-143">”New-AzVirtualHub”</span><span class="sxs-lookup"><span data-stu-id="4f44c-143">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="4f44c-144">”Update-AzVirtualHub”</span><span class="sxs-lookup"><span data-stu-id="4f44c-144">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="4f44c-145">SQL Management SDK-beroende har tagits bort</span><span class="sxs-lookup"><span data-stu-id="4f44c-145">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="4f44c-146">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="4f44c-146">Az.PolicyInsights</span></span>
* <span data-ttu-id="4f44c-147">Förbättrade felmeddelanden</span><span class="sxs-lookup"><span data-stu-id="4f44c-147">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4f44c-148">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4f44c-148">Az.RecoveryServices</span></span>
* <span data-ttu-id="4f44c-149">Azure Site Recovery har lagt till stöd för återaktivering av skydd och uppdaterade VM-egenskaper för virtuella Azure-datorer med krypterad disk.</span><span class="sxs-lookup"><span data-stu-id="4f44c-149">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="4f44c-150">Lade till Azure Site Recovery VmwareToAzure-egenskaper för DR-övervakning</span><span class="sxs-lookup"><span data-stu-id="4f44c-150">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="4f44c-151">Azure Backup har lagt till stöd för att försöka uppdatera principuppdateringen för misslyckade objekt på nytt.</span><span class="sxs-lookup"><span data-stu-id="4f44c-151">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="4f44c-152">Azure Backup lagt till stöd för diskundantagsinställningar under säkerhetskopiering och återställning.</span><span class="sxs-lookup"><span data-stu-id="4f44c-152">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="4f44c-153">Azure Backup lagt till stöd för att återställa flera filer/mappar i AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="4f44c-153">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="4f44c-154">Azure Backup lade till support för användardefinierad Resourcegroup-support vid uppdatering av IaasVM-princip</span><span class="sxs-lookup"><span data-stu-id="4f44c-154">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="4f44c-155">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4f44c-155">Az.Resources</span></span>
* <span data-ttu-id="4f44c-156">Åtgärdade ”Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType” så att den använder den faktisk apiVersion av resurser i stället för standard-apiVersion [#11267]</span><span class="sxs-lookup"><span data-stu-id="4f44c-156">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="4f44c-157">Lade till correlationId-loggning för felscenarier</span><span class="sxs-lookup"><span data-stu-id="4f44c-157">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="4f44c-158">Liten dokumentationsändring för ”Get-AzResourceLock”.</span><span class="sxs-lookup"><span data-stu-id="4f44c-158">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="4f44c-159">Lade till exempel.</span><span class="sxs-lookup"><span data-stu-id="4f44c-159">Added example.</span></span>
* <span data-ttu-id="4f44c-160">Undantaget enkelt citattecken i parametervärde för ”Get-AzADUser” [#11317]</span><span class="sxs-lookup"><span data-stu-id="4f44c-160">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="4f44c-161">Nya cmdletar har lagts till för distributionsskript (”Get-AzDeploymentScript”, ”Get-AzDeploymentScriptLog”, ”Save-AzDeploymentScriptLog”, ”Remove-AzDeploymentScript”)</span><span class="sxs-lookup"><span data-stu-id="4f44c-161">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="4f44c-162">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4f44c-162">Az.Sql</span></span>
* <span data-ttu-id="4f44c-163">En läsbar sekundär parameter har lagts till i Invoke-AzSqlDatabaseFailover</span><span class="sxs-lookup"><span data-stu-id="4f44c-163">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="4f44c-164">Cmdleten Disable-AzSqlServerActiveDirectoryOnlyAuthentication har lagts till</span><span class="sxs-lookup"><span data-stu-id="4f44c-164">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="4f44c-165">Den sparade känslighet rangordningen när kolumner klassificeras i databasen.</span><span class="sxs-lookup"><span data-stu-id="4f44c-165">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="4f44c-166">Az.Support</span><span class="sxs-lookup"><span data-stu-id="4f44c-166">Az.Support</span></span>
* <span data-ttu-id="4f44c-167">Allmän tillgänglighet för ”Az.Support”-modulen</span><span class="sxs-lookup"><span data-stu-id="4f44c-167">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4f44c-168">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4f44c-168">Az.Websites</span></span>
* <span data-ttu-id="4f44c-169">Stöd har lagts till för att arbeta med trafikdirigeringsregler för webbappar under nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="4f44c-169">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="4f44c-170">”Get-AzWebAppTrafficRouting”</span><span class="sxs-lookup"><span data-stu-id="4f44c-170">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="4f44c-171">”Update-AzWebAppTrafficRouting”</span><span class="sxs-lookup"><span data-stu-id="4f44c-171">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="4f44c-172">”Add-AzWebAppTrafficRouting”</span><span class="sxs-lookup"><span data-stu-id="4f44c-172">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="4f44c-173">”Remove-AzWebAppTrafficRouting”</span><span class="sxs-lookup"><span data-stu-id="4f44c-173">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="4f44c-174">3.6.1 – mars 2020</span><span class="sxs-lookup"><span data-stu-id="4f44c-174">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4f44c-175">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4f44c-175">Az.Accounts</span></span>
* <span data-ttu-id="4f44c-176">Öppna sidan med Azure PowerShell-enkäten i ”Send-Feedback” [#11020]</span><span class="sxs-lookup"><span data-stu-id="4f44c-176">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="4f44c-177">Visa URL:en för Azure PowerShell-enkäten i ”Resolve-Error” [#11021]</span><span class="sxs-lookup"><span data-stu-id="4f44c-177">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="4f44c-178">Az-version har lagts till i UserAgent</span><span class="sxs-lookup"><span data-stu-id="4f44c-178">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="4f44c-179">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4f44c-179">Az.ApiManagement</span></span>
* <span data-ttu-id="4f44c-180">Stöd har lagts till för att hämta och konfigurera en anpassad domän på DeveloperPortal-slutpunkten [#11007]</span><span class="sxs-lookup"><span data-stu-id="4f44c-180">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="4f44c-181">”Export-AzApiManagementApi” Stöd har lagts till för att ladda ned API-definition i Json-format [#9987]</span><span class="sxs-lookup"><span data-stu-id="4f44c-181">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="4f44c-182">”Import-AzApiManagementApi” Stöd har lagts till för att importera OpenApi 3.0-definition från Json-dokument</span><span class="sxs-lookup"><span data-stu-id="4f44c-182">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="4f44c-183">”New-AzApiManagementIdentityProvider” och ”Set-AzApiManagementIdentityProvider” Stöd har lagts till för att konfigurera ”Signin Tenant” för AAD B2C-provider [#9784]</span><span class="sxs-lookup"><span data-stu-id="4f44c-183">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4f44c-184">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4f44c-184">Az.DataLakeStore</span></span>
* <span data-ttu-id="4f44c-185">En referens har uttryckligen lagts till för System.Buffers i csproj och psd1.</span><span class="sxs-lookup"><span data-stu-id="4f44c-185">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="4f44c-186">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="4f44c-186">Az.IotHub</span></span>
* <span data-ttu-id="4f44c-187">Lade till stöd för att hantera enheter i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="4f44c-187">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="4f44c-188">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="4f44c-188">New Cmdlets are:</span></span>
    - <span data-ttu-id="4f44c-189">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="4f44c-189">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="4f44c-190">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="4f44c-190">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="4f44c-191">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="4f44c-191">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="4f44c-192">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="4f44c-192">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="4f44c-193">Stöd har lagts till för att hantera moduler på en mål-IoT-enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="4f44c-193">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="4f44c-194">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="4f44c-194">New Cmdlets are:</span></span>
    - <span data-ttu-id="4f44c-195">”Add-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="4f44c-195">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="4f44c-196">”Get-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="4f44c-196">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="4f44c-197">”Remove-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="4f44c-197">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="4f44c-198">”Set-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="4f44c-198">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="4f44c-199">Cmdlet har lagts till för att hämta anslutningssträngen för en mål-IoT-enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="4f44c-199">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="4f44c-200">Cmdlet har lagts till för att hämta anslutningssträngen för en modul på en mål-IoT-enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="4f44c-200">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="4f44c-201">Stöd har lagts till för att hämta/ange en överordnad enhet för en IoT-enhet.</span><span class="sxs-lookup"><span data-stu-id="4f44c-201">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="4f44c-202">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="4f44c-202">New Cmdlets are:</span></span>
    - <span data-ttu-id="4f44c-203">”Get-AzIotHubDeviceParent”</span><span class="sxs-lookup"><span data-stu-id="4f44c-203">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="4f44c-204">”Set-AzIotHubDeviceParent”</span><span class="sxs-lookup"><span data-stu-id="4f44c-204">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="4f44c-205">Stöd har lagts till för att hantera en enhets överordnade och underordnade relationer.</span><span class="sxs-lookup"><span data-stu-id="4f44c-205">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4f44c-206">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4f44c-206">Az.Monitor</span></span>
* <span data-ttu-id="4f44c-207">Utdatavärdet har åtgärdats för ”Get-AzMetricDefinition” [#9714]</span><span class="sxs-lookup"><span data-stu-id="4f44c-207">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4f44c-208">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4f44c-208">Az.Network</span></span>
* <span data-ttu-id="4f44c-209">SQL Management SDK har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="4f44c-209">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="4f44c-210">Ett problem har åtgärdats med namngivningsskillnader i klassen PrivateLinkServiceConnectionState.</span><span class="sxs-lookup"><span data-stu-id="4f44c-210">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="4f44c-211">Fältet ActionsRequired mappar till ActionRequired.</span><span class="sxs-lookup"><span data-stu-id="4f44c-211">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="4f44c-212">PublicNetworkAccess har lagts till i ”New-AzSqlServer” och ”Set-AzSqlServer”</span><span class="sxs-lookup"><span data-stu-id="4f44c-212">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="4f44c-213">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4f44c-213">Az.Resources</span></span>
* <span data-ttu-id="4f44c-214">Null-referensfel har åtgärdats i ”Get-AzRoleAssignment”</span><span class="sxs-lookup"><span data-stu-id="4f44c-214">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="4f44c-215">Växlarna ”-Force” och ”-PassThru” är valfria i ”Remove-AzADGroup” [#10849]</span><span class="sxs-lookup"><span data-stu-id="4f44c-215">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="4f44c-216">Ett problem har åtgärdats som gjorde att ”MailNickname” inte returnerades i ”Remove-AzADGroup” [#11167]</span><span class="sxs-lookup"><span data-stu-id="4f44c-216">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="4f44c-217">Ett problem har åtgärdats som gjorde att pipe-åtgärden ”Remove-AzADGroup” inte fungerar [#11171]</span><span class="sxs-lookup"><span data-stu-id="4f44c-217">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="4f44c-218">Ett null-referensfel har åtgärdats i GetAzureRoleAssignmentCommand</span><span class="sxs-lookup"><span data-stu-id="4f44c-218">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="4f44c-219">Attribut för icke-bakåtkompatibla ändringar har lagts till för kommande ändringar i cmdlets för principer</span><span class="sxs-lookup"><span data-stu-id="4f44c-219">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="4f44c-220">”Get-AzResourceGroup” har uppdaterats för att utföra taggfiltrering för resursgrupper på serversidan</span><span class="sxs-lookup"><span data-stu-id="4f44c-220">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="4f44c-221">Utökade Tag-cmdlets stöder -ResourceId</span><span class="sxs-lookup"><span data-stu-id="4f44c-221">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="4f44c-222">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="4f44c-222">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="4f44c-223">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="4f44c-223">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="4f44c-224">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="4f44c-224">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="4f44c-225">Ny Tag-cmdlet har lagts till</span><span class="sxs-lookup"><span data-stu-id="4f44c-225">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="4f44c-226">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="4f44c-226">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="4f44c-227">Flyttade ScopedDeployment från SDK 3.3.0</span><span class="sxs-lookup"><span data-stu-id="4f44c-227">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="4f44c-228">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4f44c-228">Az.Sql</span></span>
* <span data-ttu-id="4f44c-229">PublicNetworkAccess har lagts till i ”New-AzSqlServer” och ”Set-AzSqlServer”</span><span class="sxs-lookup"><span data-stu-id="4f44c-229">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="4f44c-230">Stöd har lagts till för konfiguration av säkerhetskopiering för långsiktig kvarhållning för hanterade databaser</span><span class="sxs-lookup"><span data-stu-id="4f44c-230">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="4f44c-231">Hämta/ange LTR-princip på en hanterad databas</span><span class="sxs-lookup"><span data-stu-id="4f44c-231">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="4f44c-232">Hämta LTR-säkerhetskopior efter hanterad databas, hanterad instans eller plats</span><span class="sxs-lookup"><span data-stu-id="4f44c-232">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="4f44c-233">Ta bort en LTR-säkerhetskopia</span><span class="sxs-lookup"><span data-stu-id="4f44c-233">Remove an LTR backup</span></span>
    - <span data-ttu-id="4f44c-234">Återställa en LTR-säkerhetskopia för att skapa en ny hanterad databas</span><span class="sxs-lookup"><span data-stu-id="4f44c-234">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="4f44c-235">MinimalTlsVersion har lagts till för New-AzSqlServer och Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="4f44c-235">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="4f44c-236">MinimalTlsVersion har lagts till för New-AzSqlInstance och Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="4f44c-236">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="4f44c-237">SQL SDK-versionen för Az.Network har ändrats</span><span class="sxs-lookup"><span data-stu-id="4f44c-237">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4f44c-238">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4f44c-238">Az.Storage</span></span>
* <span data-ttu-id="4f44c-239">AllowProtectedAppendWrite stöds i ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="4f44c-239">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="4f44c-240">”Set-AzRmStorageContainerImmutabilityPolicy”</span><span class="sxs-lookup"><span data-stu-id="4f44c-240">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="4f44c-241">Varningsmeddelande har lagts till om icke-bakåtkompatibel ändring för ändring av typen AzureStorageTable i en senare version</span><span class="sxs-lookup"><span data-stu-id="4f44c-241">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="4f44c-242">”New-AzStorageTable”</span><span class="sxs-lookup"><span data-stu-id="4f44c-242">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="4f44c-243">”Get-AzStorageTable”</span><span class="sxs-lookup"><span data-stu-id="4f44c-243">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4f44c-244">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4f44c-244">Az.Websites</span></span>
* <span data-ttu-id="4f44c-245">Tag-parametern har lagts till för ”New-AzAppServicePlan” och ”Set-AzAppServicePlan”</span><span class="sxs-lookup"><span data-stu-id="4f44c-245">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="4f44c-246">Stoppa cmdlet-körning om ett undantag uppstår när en anpassad domän läggs till på en webbplats</span><span class="sxs-lookup"><span data-stu-id="4f44c-246">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="4f44c-247">Stöd har lagts till för att utföra åtgärder för App Services som inte tillhör samma resursgrupp som App Services-planen</span><span class="sxs-lookup"><span data-stu-id="4f44c-247">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="4f44c-248">Åtkomstbegränsning har tillämpats på WebApp/Function i olika resursgrupper</span><span class="sxs-lookup"><span data-stu-id="4f44c-248">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="4f44c-249">Ett problem har åtgärdats för att ange anpassade värdnamn för WebAppSlots</span><span class="sxs-lookup"><span data-stu-id="4f44c-249">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="4f44c-250">3.5.0 – februari 2020</span><span class="sxs-lookup"><span data-stu-id="4f44c-250">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="4f44c-251">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="4f44c-251">Highlights since the last major release</span></span>
* <span data-ttu-id="4f44c-252">Uppdaterade telemetri på klientsidan.</span><span class="sxs-lookup"><span data-stu-id="4f44c-252">Updated client side telemetry.</span></span>
* <span data-ttu-id="4f44c-253">Az.IotHub lade till cmdletar som stöd för att hantera enheter.</span><span class="sxs-lookup"><span data-stu-id="4f44c-253">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="4f44c-254">Az.SqlVirtualMachine lade till cmdletar för lyssningsfunktion för tillgänglighetsgrupp.</span><span class="sxs-lookup"><span data-stu-id="4f44c-254">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="4f44c-255">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4f44c-255">Az.Accounts</span></span>
* <span data-ttu-id="4f44c-256">Lade till SubscriptionId, TenantId och körningstid i data för telemetri på klientsidan</span><span class="sxs-lookup"><span data-stu-id="4f44c-256">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4f44c-257">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4f44c-257">Az.Automation</span></span>
* <span data-ttu-id="4f44c-258">Åtgärdade skrivfel i exempel 1 i referensdokumentation för ”New-AzAutomationSoftwareUpdateConfiguration”</span><span class="sxs-lookup"><span data-stu-id="4f44c-258">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="4f44c-259">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="4f44c-259">Az.CognitiveServices</span></span>
* <span data-ttu-id="4f44c-260">Uppdaterade SDK till 7.0</span><span class="sxs-lookup"><span data-stu-id="4f44c-260">Updated SDK to 7.0</span></span>
* <span data-ttu-id="4f44c-261">Förbättrade felmeddelande vid serversvar om tom brödtext</span><span class="sxs-lookup"><span data-stu-id="4f44c-261">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4f44c-262">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4f44c-262">Az.Compute</span></span>
* <span data-ttu-id="4f44c-263">Tillät tomt värde för ProximityPlacementGroupId under uppdatering</span><span class="sxs-lookup"><span data-stu-id="4f44c-263">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="4f44c-264">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="4f44c-264">Az.FrontDoor</span></span>
* <span data-ttu-id="4f44c-265">Lade till cmdlet för att hämta hanterade regeldefinitioner som kan användas i WAF</span><span class="sxs-lookup"><span data-stu-id="4f44c-265">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="4f44c-266">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="4f44c-266">Az.IotHub</span></span>
* <span data-ttu-id="4f44c-267">Lade till stöd för att hantera enheter i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="4f44c-267">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="4f44c-268">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="4f44c-268">New Cmdlets are:</span></span>
    - <span data-ttu-id="4f44c-269">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="4f44c-269">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="4f44c-270">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="4f44c-270">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="4f44c-271">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="4f44c-271">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="4f44c-272">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="4f44c-272">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="4f44c-273">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4f44c-273">Az.KeyVault</span></span>
* <span data-ttu-id="4f44c-274">Åtgärdade duplicerad text för Add-AzKeyVaultKey.md</span><span class="sxs-lookup"><span data-stu-id="4f44c-274">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4f44c-275">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4f44c-275">Az.Monitor</span></span>
* <span data-ttu-id="4f44c-276">Åtgärdade beskrivning av cmdleten Get-AzLog.</span><span class="sxs-lookup"><span data-stu-id="4f44c-276">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="4f44c-277">En ny parameter med namnet ActionGroupId har lagts till i kommandot ”New-AzMetricAlertRuleV2”.</span><span class="sxs-lookup"><span data-stu-id="4f44c-277">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="4f44c-278">Användaren kan ange ActionGroupId(string) eller ActionGroup(ActivityLogAlertActionGroup).</span><span class="sxs-lookup"><span data-stu-id="4f44c-278">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4f44c-279">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4f44c-279">Az.Network</span></span>
* <span data-ttu-id="4f44c-280">Lade till en extra parameteranteckning för parametern ”-EnableProxyProtocol” för cmdleten ”New-AzPrivateLinkService”.</span><span class="sxs-lookup"><span data-stu-id="4f44c-280">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="4f44c-281">Åtgärdade FilterData-exempel i Start-AzVirtualNetworkGatewayConnectionPacketCapture.md och Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="4f44c-281">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="4f44c-282">Lade till paketinsamlingsexempel för att samla in alla inre och yttre paket i Start-AzVirtualNetworkGatewayConnectionPacketCapture.md och Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="4f44c-282">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="4f44c-283">Lade till stöd för Azure-brandväggsprincip på VNet-brandväggar</span><span class="sxs-lookup"><span data-stu-id="4f44c-283">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="4f44c-284">Inga nya cmdletar har lagts till.</span><span class="sxs-lookup"><span data-stu-id="4f44c-284">No new cmdlets are added.</span></span> <span data-ttu-id="4f44c-285">Lättar begränsningen för brandväggsprincip på VNet-brandväggar</span><span class="sxs-lookup"><span data-stu-id="4f44c-285">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4f44c-286">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4f44c-286">Az.RecoveryServices</span></span>
* <span data-ttu-id="4f44c-287">Lade till stöd för Restore-as-files för SQL-databaser.</span><span class="sxs-lookup"><span data-stu-id="4f44c-287">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="4f44c-288">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4f44c-288">Az.Resources</span></span>
* <span data-ttu-id="4f44c-289">Omstrukturerade cmdletar för malldistribution</span><span class="sxs-lookup"><span data-stu-id="4f44c-289">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="4f44c-290">Lade till nya cmdletar för att hantera distributioner i hanteringsgruppen: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4f44c-290">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="4f44c-291">Lade till nya cmdletar för att hantera distributioner i klientorganisationsområdet: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="4f44c-291">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="4f44c-292">Omstrukturerade \*-AzDeployment-cmdletar för att fungera specifikt i prenumerationsomfattningen</span><span class="sxs-lookup"><span data-stu-id="4f44c-292">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="4f44c-293">Skapade alias \*-AzSubscriptionDeployment för \*-AzDeployment-cmdletar</span><span class="sxs-lookup"><span data-stu-id="4f44c-293">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="4f44c-294">Åtgärdade ”Update-AzADApplication” när parametern ”AvailableToOtherTenants” inte har angetts</span><span class="sxs-lookup"><span data-stu-id="4f44c-294">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="4f44c-295">Tog bort ApplicationObjectWithoutCredentialParameterSet för att undvika AmbiguousParameterSetException.</span><span class="sxs-lookup"><span data-stu-id="4f44c-295">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="4f44c-296">Återskapade hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="4f44c-296">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="4f44c-297">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4f44c-297">Az.Sql</span></span>
* <span data-ttu-id="4f44c-298">Lade till stöd för återställning till tidpunkt mellan prenumerationer på hanterade instanser.</span><span class="sxs-lookup"><span data-stu-id="4f44c-298">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="4f44c-299">Lade till stöd för att ändra befintlig SQL Managed Instance-maskinvarugenerering</span><span class="sxs-lookup"><span data-stu-id="4f44c-299">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="4f44c-300">Åtgärdade ”Update-AzSqlServerVulnerabilityAssessmentSetting”-hjälpexempel: parameter/egenskapsutdata - EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="4f44c-300">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="4f44c-301">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="4f44c-301">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="4f44c-302">Lade till cmdletar för lyssningsfunktion för tillgänglighetsgrupp</span><span class="sxs-lookup"><span data-stu-id="4f44c-302">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="4f44c-303">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="4f44c-303">Az.StorageSync</span></span>
* <span data-ttu-id="4f44c-304">Uppdaterade teckenuppsättningar som stöds i ”Invoke-AzStorageSyncCompatibilityCheck”.</span><span class="sxs-lookup"><span data-stu-id="4f44c-304">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="4f44c-305">3.4.0 – februari 2020</span><span class="sxs-lookup"><span data-stu-id="4f44c-305">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="4f44c-306">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="4f44c-306">Highlights since the last major release</span></span>
* <span data-ttu-id="4f44c-307">Första Az.CosmosDB-versionen 0.1.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="4f44c-307">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="4f44c-308">Stöd för Az.Network ConnectionMonitor V2 har lagts till</span><span class="sxs-lookup"><span data-stu-id="4f44c-308">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="4f44c-309">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4f44c-309">Az.Accounts</span></span>
* <span data-ttu-id="4f44c-310">Inaktivera automatisk sparande av kontext när AzureRmContext.json inte är tillgängligt</span><span class="sxs-lookup"><span data-stu-id="4f44c-310">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="4f44c-311">Uppdatera referensen till Azure Powershell Common till 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="4f44c-311">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="4f44c-312">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4f44c-312">Az.ApiManagement</span></span>
* <span data-ttu-id="4f44c-313">**Get-AzApiManagementApiSchema** Hämtning av Open-Api-schema som är associerat med ett API har åtgärdats   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="4f44c-313">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="4f44c-314">**New-AzApiManagementProduct**\* och **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="4f44c-314">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="4f44c-315">Åtgärda dokumentation för https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="4f44c-315">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="4f44c-316">**Set-AzApiManagementApi** Exempel för att visa hur ServiceUrl uppdateras med hjälp av cmdleten har lagts till</span><span class="sxs-lookup"><span data-stu-id="4f44c-316">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4f44c-317">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4f44c-317">Az.Compute</span></span>
* <span data-ttu-id="4f44c-318">Begränsa antalet VM-status till 100 för att undvika begränsning när Get-AzVM -Status utförs utan VM-namn.</span><span class="sxs-lookup"><span data-stu-id="4f44c-318">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="4f44c-319">Lägg till cmdleten Update-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="4f44c-319">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="4f44c-320">Lägg till parametrarna EncryptionType och DiskEncryptionSetId i följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="4f44c-320">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="4f44c-321">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="4f44c-321">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="4f44c-322">Lägg till parametern ColocationStatus för cmdleten Get-AzProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="4f44c-322">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4f44c-323">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4f44c-323">Az.DataFactory</span></span>
* <span data-ttu-id="4f44c-324">Uppdatera ADF .Net SDK-versionen till 4.7.0</span><span class="sxs-lookup"><span data-stu-id="4f44c-324">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="4f44c-325">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="4f44c-325">Az.DeploymentManager</span></span>
* <span data-ttu-id="4f44c-326">Lägger till LIST-åtgärder för resurser</span><span class="sxs-lookup"><span data-stu-id="4f44c-326">Adds LIST operations for resources</span></span>
* <span data-ttu-id="4f44c-327">Lägger till funktion för att utföra åtgärder för hälsokontrollsteg</span><span class="sxs-lookup"><span data-stu-id="4f44c-327">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="4f44c-328">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="4f44c-328">Az.HDInsight</span></span>
* <span data-ttu-id="4f44c-329">Åtgärda dokumentfel för New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="4f44c-329">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="4f44c-330">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4f44c-330">Az.KeyVault</span></span>
* <span data-ttu-id="4f44c-331">Lägg till Name-alias för attributet VaultName så att Remove-AzureKeyVault stämmer överens med New-AzureKeyVault.</span><span class="sxs-lookup"><span data-stu-id="4f44c-331">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4f44c-332">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4f44c-332">Az.Network</span></span>
* <span data-ttu-id="4f44c-333">Nytt exempel har lagts till i Set-AzNetworkWatcherConfigFlowLog.md för att demonstrera ett inaktiveringsscenario för Trafikanalys.</span><span class="sxs-lookup"><span data-stu-id="4f44c-333">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="4f44c-334">Lägg till stöd för att tilldela konfiguration av hanterings-IP till Azure Firewall – ett dedikerat undernät och en offentlig IP som brandväggen använder för dess hanteringstrafik</span><span class="sxs-lookup"><span data-stu-id="4f44c-334">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="4f44c-335">Cmdleten New-AzFirewall har uppdaterats:</span><span class="sxs-lookup"><span data-stu-id="4f44c-335">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="4f44c-336">Parametern -ManagementPublicIpAddress (inte obligatorisk) som accepterar ett offentligt IP-adressobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="4f44c-336">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="4f44c-337">Metoden SetManagementIpConfiguration har lagts till för brandväggsobjekt – kräver ett undernät och en offentlig IP-adress som indata – undernätets namn måste vara ”AzureFirewallManagementSubnet”</span><span class="sxs-lookup"><span data-stu-id="4f44c-337">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="4f44c-338">Exempel för Get-AzNetworkSecurityGroup har korrigerats så att exempel visas för NSG:er i stället för nätverksgränssnitt.</span><span class="sxs-lookup"><span data-stu-id="4f44c-338">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="4f44c-339">Ett skrivfel har åtgärdats i kommandot New-AzVpnSite som hindrade kompletteraren för resurs-ID från att fylla i en parameter.</span><span class="sxs-lookup"><span data-stu-id="4f44c-339">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="4f44c-340">Stöd för Url-konfiguration i åtgärdsuppsättningen för omskrivningsregler i Application Gateway har lagts till</span><span class="sxs-lookup"><span data-stu-id="4f44c-340">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="4f44c-341">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="4f44c-341">New cmdlets added:</span></span>
        - <span data-ttu-id="4f44c-342">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="4f44c-342">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="4f44c-343">Cmdletar har uppdaterats med den valfria parametern -UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="4f44c-343">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="4f44c-344">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="4f44c-344">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="4f44c-345">Lägg till stöd för resurser för NetworkWatcher ConnectionMonitor version 2</span><span class="sxs-lookup"><span data-stu-id="4f44c-345">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="4f44c-346">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="4f44c-346">Az.PolicyInsights</span></span>
* <span data-ttu-id="4f44c-347">Stöd för utvärdering av efterlevnad innan fastställande av vilken resurs som ska åtgärdas</span><span class="sxs-lookup"><span data-stu-id="4f44c-347">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="4f44c-348">Lägg till parametern ”-ResourceDiscoverMode” för Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="4f44c-348">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="4f44c-349">Lägg till cmdleten Get-AzPolicyMetadata för att hämta resurser för principmetadata</span><span class="sxs-lookup"><span data-stu-id="4f44c-349">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="4f44c-350">Get-AzPolicyState och Get-AzPolicyStateSummary för API-versionen 2019-10-01 har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="4f44c-350">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4f44c-351">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4f44c-351">Az.RecoveryServices</span></span>
* <span data-ttu-id="4f44c-352">Azure Site Recovery-stöd för att ta bort en replikerad disk.</span><span class="sxs-lookup"><span data-stu-id="4f44c-352">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="4f44c-353">Tillagt Azure Backup-stöd för att lägga till taggar när ett Recovery Services-valv skapas.</span><span class="sxs-lookup"><span data-stu-id="4f44c-353">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="4f44c-354">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4f44c-354">Az.Resources</span></span>
* <span data-ttu-id="4f44c-355">Gör -Scope valfritt i cmdletarna \*-AzPolicyAssignment med standardinställning till kontextprenumeration</span><span class="sxs-lookup"><span data-stu-id="4f44c-355">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="4f44c-356">Lägg till exempel på att skapa ADServicePrincipal med lösenord och nyckelautentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="4f44c-356">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="4f44c-357">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4f44c-357">Az.Sql</span></span>
<span data-ttu-id="4f44c-358">Åtgärda cmdleten New-AzSqlDatabaseSecondary så att existensen PartnerDatabaseName kontrolleras i stället för existensen DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="4f44c-358">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4f44c-359">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4f44c-359">Az.Storage</span></span>
* <span data-ttu-id="4f44c-360">Stöd för angivning av krypteringsnyckeltyp för Tabell/kö i Skapa lagringskonto</span><span class="sxs-lookup"><span data-stu-id="4f44c-360">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="4f44c-361">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4f44c-361">New-AzStorageAccount</span></span>
* <span data-ttu-id="4f44c-362">Visa RequestId när StorageException inte har ExtendedErrorInformation</span><span class="sxs-lookup"><span data-stu-id="4f44c-362">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="4f44c-363">Åtgärda exempel 6 för cmdleten Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="4f44c-363">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4f44c-364">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4f44c-364">Az.Websites</span></span>
* <span data-ttu-id="4f44c-365">Set-AzWebapp och Set-AzWebappSlot stöder egenskaperna AlwaysOn, MinTls och FtpsState</span><span class="sxs-lookup"><span data-stu-id="4f44c-365">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="4f44c-366">Åtgärdar problemet där inställning av HttpsOnly samtidigt som AppservicePlan ändrades med det enskilda kommandot Set-AzWebApp återställde HttpsOnly till standardvärdet</span><span class="sxs-lookup"><span data-stu-id="4f44c-366">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="4f44c-367">3.3.0 – januari 2020</span><span class="sxs-lookup"><span data-stu-id="4f44c-367">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4f44c-368">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4f44c-368">Az.Accounts</span></span>
* <span data-ttu-id="4f44c-369">Nu stöder Add-AzEnvironment och Set-AzEnvironment parametrarna AzureAttestationServiceEndpointResourceId och AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="4f44c-369">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="4f44c-370">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="4f44c-370">Az.Cdn</span></span>
* <span data-ttu-id="4f44c-371">Information om felsvar visas i New-AzCdnEndpoint-cmdleten</span><span class="sxs-lookup"><span data-stu-id="4f44c-371">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4f44c-372">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4f44c-372">Az.Compute</span></span>
* <span data-ttu-id="4f44c-373">Set-AzVMCustomScriptExtension-cmdleten har åtgärdats för en virtuell dator med hanterad OD-disk som inte har någon operativsystemprofil.</span><span class="sxs-lookup"><span data-stu-id="4f44c-373">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="4f44c-374">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="4f44c-374">Az.ContainerInstance</span></span>
* <span data-ttu-id="4f44c-375">Parameternamn som används med New-AzContainerGroup-exempel har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="4f44c-375">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="4f44c-376">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="4f44c-376">Az.DataBoxEdge</span></span>
* <span data-ttu-id="4f44c-377">Cmdleten ”Get-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="4f44c-377">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="4f44c-378">Hämta gränslagringscontainern</span><span class="sxs-lookup"><span data-stu-id="4f44c-378">Get the Edge Storage Container</span></span>
* <span data-ttu-id="4f44c-379">Cmdleten ”New-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="4f44c-379">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="4f44c-380">Skapa en ny gränslagringscontainer</span><span class="sxs-lookup"><span data-stu-id="4f44c-380">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="4f44c-381">Cmdleten ”Remove-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="4f44c-381">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="4f44c-382">Ta bort gränslagringscontainern</span><span class="sxs-lookup"><span data-stu-id="4f44c-382">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="4f44c-383">Cmdleten ”Invoke-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="4f44c-383">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="4f44c-384">Anropa åtgärd för att uppdatera data i gränslagringscontainer</span><span class="sxs-lookup"><span data-stu-id="4f44c-384">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="4f44c-385">Cmdleten ”Get-AzDataBoxEdgeStorageAccount” har lagts till</span><span class="sxs-lookup"><span data-stu-id="4f44c-385">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="4f44c-386">Hämta gränslagringskontot</span><span class="sxs-lookup"><span data-stu-id="4f44c-386">Get the Edge Storage Account</span></span>
* <span data-ttu-id="4f44c-387">Cmdleten ”New-AzDataBoxEdgeStorageAccount” har lagts till</span><span class="sxs-lookup"><span data-stu-id="4f44c-387">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="4f44c-388">Skapa ett nytt gränslagringskonto</span><span class="sxs-lookup"><span data-stu-id="4f44c-388">Create new Edge Storage Account</span></span>
* <span data-ttu-id="4f44c-389">Cmdleten ”Remove-AzDataBoxEdgeStorageAccount” har lagts till</span><span class="sxs-lookup"><span data-stu-id="4f44c-389">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="4f44c-390">Ta bort gränslagringskontot</span><span class="sxs-lookup"><span data-stu-id="4f44c-390">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="4f44c-391">Anropa cmdleten ”Invoke-AzDataBoxEdgeShare”</span><span class="sxs-lookup"><span data-stu-id="4f44c-391">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="4f44c-392">Anropa åtgärd för att uppdatera resursdata</span><span class="sxs-lookup"><span data-stu-id="4f44c-392">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="4f44c-393">Cmdleten ”Set-AzDataBoxEdgeStorageAccountCredential” har lagts till</span><span class="sxs-lookup"><span data-stu-id="4f44c-393">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="4f44c-394">Ange autentiseringsuppgifter för az databoxedge-lagringskonto</span><span class="sxs-lookup"><span data-stu-id="4f44c-394">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4f44c-395">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4f44c-395">Az.DataFactory</span></span>
* <span data-ttu-id="4f44c-396">Lägg till AutoUpdateETA-, LatestVersion-, PushedVersion-, TaskQueueId- och VersionStatus-egenskaper för Get-AzDataFactoryV2IntegrationRuntime-cmd</span><span class="sxs-lookup"><span data-stu-id="4f44c-396">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="4f44c-397">Uppdatera ADF .Net SDK-versionen till 4.6.0</span><span class="sxs-lookup"><span data-stu-id="4f44c-397">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="4f44c-398">Lägg till parametern ”PublicIPs” för ”Set-AzureRmDataFactoryV2IntegrationRuntime”-cmd så att Azure-SSIS IR kan skapas med statiska offentliga IP-adresser.</span><span class="sxs-lookup"><span data-stu-id="4f44c-398">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="4f44c-399">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="4f44c-399">Az.DevTestLabs</span></span>
* <span data-ttu-id="4f44c-400">Ta bort den brutna länken i Get-AzDtlAllowedVMSizesPolicy.md</span><span class="sxs-lookup"><span data-stu-id="4f44c-400">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="4f44c-401">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="4f44c-401">Az.EventHub</span></span>
* <span data-ttu-id="4f44c-402">Korrigering av problem 10634: Åtgärda referensen till null-objekt för eventhubnamespace-borttagning</span><span class="sxs-lookup"><span data-stu-id="4f44c-402">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="4f44c-403">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="4f44c-403">Az.HDInsight</span></span>
* <span data-ttu-id="4f44c-404">Åtgärda Invoke-AzHDInsightHiveJob.md-fel.</span><span class="sxs-lookup"><span data-stu-id="4f44c-404">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="4f44c-405">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="4f44c-405">Az.MachineLearning</span></span>
* <span data-ttu-id="4f44c-406">Nedanstående cmdletar har tagits bort eftersom MachineLearningCompute inte längre är tillgängligt</span><span class="sxs-lookup"><span data-stu-id="4f44c-406">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="4f44c-407">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="4f44c-407">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="4f44c-408">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="4f44c-408">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="4f44c-409">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="4f44c-409">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="4f44c-410">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="4f44c-410">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="4f44c-411">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="4f44c-411">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="4f44c-412">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="4f44c-412">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="4f44c-413">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="4f44c-413">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4f44c-414">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4f44c-414">Az.Network</span></span>
* <span data-ttu-id="4f44c-415">Uppgradera beroende av Microsoft.Azure.Management.Sql från 1.36-preview till 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="4f44c-415">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4f44c-416">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4f44c-416">Az.RecoveryServices</span></span>
* <span data-ttu-id="4f44c-417">Ändrat Azure Site Recovery-stöd för krypterade vilande data på virtuella datorer med hanterade diskar med kundhanterade nycklar för Azure till Azure-providern.</span><span class="sxs-lookup"><span data-stu-id="4f44c-417">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="4f44c-418">Azure Site Recovery-stöd för att ange ID för diskkrypteringsuppsättning som valfri inmatning för aktivering av skydd för VMware till Azure.</span><span class="sxs-lookup"><span data-stu-id="4f44c-418">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="4f44c-419">Azure Site Recovery-stöd för att ange ID för diskkrypteringsuppsättning som valfri inmatning på disknivå för aktivering av skydd för VMware till Azure.</span><span class="sxs-lookup"><span data-stu-id="4f44c-419">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="4f44c-420">Azure Site Recovery-stöd för att uppdatera replikeringsskyddade objekt med mappning för diskkrypteringsuppsättning för HyperV till Azure.</span><span class="sxs-lookup"><span data-stu-id="4f44c-420">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="4f44c-421">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4f44c-421">Az.Resources</span></span>
* <span data-ttu-id="4f44c-422">Åtgärda ett fel i hjälpdokument för ”Remove-AzTag”.</span><span class="sxs-lookup"><span data-stu-id="4f44c-422">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="4f44c-423">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4f44c-423">Az.Sql</span></span>
* <span data-ttu-id="4f44c-424">Åtgärda funktioner i cmdletar för att ange baslinjen för sårbarhetsbedömning för arbete med huvuddatabasen för Azure-databasen och begränsa den för systemdatabaser på hanterade instanser.</span><span class="sxs-lookup"><span data-stu-id="4f44c-424">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="4f44c-425">Åtgärda ett fel när en redundansgrupp för en SQL-instans skapas</span><span class="sxs-lookup"><span data-stu-id="4f44c-425">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="4f44c-426">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="4f44c-426">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="4f44c-427">Lägg till DR som en ny giltig licenstyp</span><span class="sxs-lookup"><span data-stu-id="4f44c-427">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4f44c-428">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4f44c-428">Az.Storage</span></span>
* <span data-ttu-id="4f44c-429">Lägg till varningsmeddelande om icke-bakåtkompatibel ändring för DefaultAction-värdeändring i en framtida version</span><span class="sxs-lookup"><span data-stu-id="4f44c-429">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="4f44c-430">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="4f44c-430">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="4f44c-431">Stöd för att hämta lagringskontots senaste synkroniseringstid genom att köra get-AzureRMStorageAccount med parametern -IncludeGeoReplicationStats</span><span class="sxs-lookup"><span data-stu-id="4f44c-431">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="4f44c-432">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4f44c-432">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="4f44c-433">3.2.0 – December 2019</span><span class="sxs-lookup"><span data-stu-id="4f44c-433">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="4f44c-434">Allmänt</span><span class="sxs-lookup"><span data-stu-id="4f44c-434">General</span></span>
* <span data-ttu-id="4f44c-435">Uppdatera referenser i .psd1 för att använda relativa sökvägar för alla moduler</span><span class="sxs-lookup"><span data-stu-id="4f44c-435">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="4f44c-436">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4f44c-436">Az.Accounts</span></span>
* <span data-ttu-id="4f44c-437">Ange rätt UserAgent för telemetri på klientsidan för Az 4.0 preview</span><span class="sxs-lookup"><span data-stu-id="4f44c-437">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="4f44c-438">Visa användarvänligt felmeddelande när kontexten är null i Az 4.0 preview</span><span class="sxs-lookup"><span data-stu-id="4f44c-438">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="4f44c-439">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="4f44c-439">Az.Batch</span></span>
* <span data-ttu-id="4f44c-440">Korrigera problem [#10602](https://github.com/Azure/azure-powershell/issues/10602), där **New-AzBatchPool** skickade VirtualMachineConfiguration.ContainerConfiguration eller VirtualMachineConfiguration.DataDisks på ett felaktigt sätt till servern.</span><span class="sxs-lookup"><span data-stu-id="4f44c-440">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4f44c-441">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4f44c-441">Az.DataFactory</span></span>
* <span data-ttu-id="4f44c-442">Uppdatera ADF .Net SDK-versionen till 4.5.0</span><span class="sxs-lookup"><span data-stu-id="4f44c-442">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="4f44c-443">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="4f44c-443">Az.FrontDoor</span></span>
* <span data-ttu-id="4f44c-444">Stöd har lagts till för undantag för hanterade regler för brandväggen för webbaserade program</span><span class="sxs-lookup"><span data-stu-id="4f44c-444">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="4f44c-445">Lägg till SocketAddr för automatisk komplettering</span><span class="sxs-lookup"><span data-stu-id="4f44c-445">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="4f44c-446">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="4f44c-446">Az.HealthcareApis</span></span>
* <span data-ttu-id="4f44c-447">Undantagshantering</span><span class="sxs-lookup"><span data-stu-id="4f44c-447">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="4f44c-448">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4f44c-448">Az.KeyVault</span></span>
* <span data-ttu-id="4f44c-449">Åtgärdat fel vid åtkomst av värde som kanske inte har angetts</span><span class="sxs-lookup"><span data-stu-id="4f44c-449">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="4f44c-450">Hantering av ECC-certifikat (Elliptic Curve Cryptography)</span><span class="sxs-lookup"><span data-stu-id="4f44c-450">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="4f44c-451">Stöd har lagts till för att ange kurvan för certifikatprinciper</span><span class="sxs-lookup"><span data-stu-id="4f44c-451">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4f44c-452">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4f44c-452">Az.Monitor</span></span>
* <span data-ttu-id="4f44c-453">Lägger till valfritt argument i kommandot Lägg till diagnostikinställningar.</span><span class="sxs-lookup"><span data-stu-id="4f44c-453">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="4f44c-454">Ett växelargument som om det finns visar att exporten till Log Analytics måste ske till ett fast schema (kallas även</span><span class="sxs-lookup"><span data-stu-id="4f44c-454">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="4f44c-455">dedikerad, datatyp)</span><span class="sxs-lookup"><span data-stu-id="4f44c-455">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4f44c-456">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4f44c-456">Az.Network</span></span>
* <span data-ttu-id="4f44c-457">Stöd för IpGroups i program-, NAT- och nätverksregler för Azure Firewall.</span><span class="sxs-lookup"><span data-stu-id="4f44c-457">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="4f44c-458">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4f44c-458">Az.Resources</span></span>
* <span data-ttu-id="4f44c-459">Åtgärda ett problem där malldistributionen inte kan läsa en mallparameter om dess namn står i konflikt med ett inbyggt parameternamn.</span><span class="sxs-lookup"><span data-stu-id="4f44c-459">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="4f44c-460">Uppdaterade princip-cmdletar för att använda den nya API-versionen 2019-09-01 som introducerar grupperingsstöd inom principuppsättningsdefinitioner.</span><span class="sxs-lookup"><span data-stu-id="4f44c-460">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="4f44c-461">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4f44c-461">Az.Sql</span></span>
* <span data-ttu-id="4f44c-462">Uppgraderad funktion för att skapa lagring i automatisk aktivering av sårbarhetsbedömning till StorageV2</span><span class="sxs-lookup"><span data-stu-id="4f44c-462">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4f44c-463">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4f44c-463">Az.Storage</span></span>
* <span data-ttu-id="4f44c-464">Stöd för generering av blob/container-identitetsbaserad SAS-token med lagringskontextbaserad på OAuth-autentisering</span><span class="sxs-lookup"><span data-stu-id="4f44c-464">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="4f44c-465">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="4f44c-465">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="4f44c-466">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="4f44c-466">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="4f44c-467">Stöd för återkallning av användardelegeringsnycklar för lagringskonto för att återkalla alla SAS-token</span><span class="sxs-lookup"><span data-stu-id="4f44c-467">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="4f44c-468">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="4f44c-468">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="4f44c-469">Uppgradera till Microsoft.Azure.Management.Storage 14.2.0 för att stödja den nya API-versionen 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="4f44c-469">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="4f44c-470">Stöd för QuotaGiB (resurskvot i Gibibye) för värden över 5120 i hanteringsplanet för cmdletar för filresurser och parameteraliaset. Quota har också lagts till för parametern ”QuotaGiB”.</span><span class="sxs-lookup"><span data-stu-id="4f44c-470">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="4f44c-471">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="4f44c-471">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="4f44c-472">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="4f44c-472">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="4f44c-473">Lägg till parameteraliaset QuotaGiB i parametern Quota</span><span class="sxs-lookup"><span data-stu-id="4f44c-473">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="4f44c-474">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="4f44c-474">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="4f44c-475">Åtgärda problemet att Set-AzStorageContainerAcl kan rensa den lagrade åtkomstprincipen</span><span class="sxs-lookup"><span data-stu-id="4f44c-475">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="4f44c-476">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="4f44c-476">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="4f44c-477">3.1.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="4f44c-477">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="4f44c-478">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="4f44c-478">Highlights since the last major release</span></span>
* <span data-ttu-id="4f44c-479">Az.DataBoxEdge 1.0.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="4f44c-479">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="4f44c-480">Az.SqlVirtualMachine 1.0.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="4f44c-480">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4f44c-481">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4f44c-481">Az.Compute</span></span>
* <span data-ttu-id="4f44c-482">Funktion för att använda en virtuell dator igen</span><span class="sxs-lookup"><span data-stu-id="4f44c-482">VM Reapply feature</span></span>
    - <span data-ttu-id="4f44c-483">Lägg till parameter för att använda igen till cmdleten Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="4f44c-483">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="4f44c-484">Funktionen AutomaticRepairs i VM-skalningsuppsättningar:</span><span class="sxs-lookup"><span data-stu-id="4f44c-484">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="4f44c-485">Lägg till parametrarna EnableAutomaticRepair, AutomaticRepairGracePeriod och AutomaticRepairMaxInstanceRepairsPercent till följande cmdletar:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4f44c-485">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="4f44c-486">Stöd för galleriavbildningar i flera klientorganisationer för New-AzVM</span><span class="sxs-lookup"><span data-stu-id="4f44c-486">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="4f44c-487">Lägg till "Spot" till argumentslutföraren i prioritetsparametern i cmdletarna New-AzVM, New-AzVMConfig och New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4f44c-487">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="4f44c-488">Lägg till parametrarna DiskIOPSReadWrite och DiskMBpsReadWrite till cmdleten Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="4f44c-488">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="4f44c-489">Ändra parametern SourceImageId för cmdleten New-AzGalleryImageVersion till valfri</span><span class="sxs-lookup"><span data-stu-id="4f44c-489">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="4f44c-490">Lägg till parametrarna OSDiskImage och DataDiskImage till cmdleten New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="4f44c-490">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="4f44c-491">Lägg till parametern HyperVGeneration till cmdleten New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="4f44c-491">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="4f44c-492">Lägg till parametern SkipExtensionsOnOverprovisionedVMs till cmdletarna New-AzVmss, New-AzVmssConfig och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4f44c-492">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="4f44c-493">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="4f44c-493">Az.DataBoxEdge</span></span>
* <span data-ttu-id="4f44c-494">Cmdleten `Get-AzDataBoxEdgeOrder` har lagts till</span><span class="sxs-lookup"><span data-stu-id="4f44c-494">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="4f44c-495">Hämta ordning</span><span class="sxs-lookup"><span data-stu-id="4f44c-495">Get the Order</span></span>
* <span data-ttu-id="4f44c-496">Cmdleten `New-AzDataBoxEdgeOrder` har lagts till</span><span class="sxs-lookup"><span data-stu-id="4f44c-496">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="4f44c-497">Skapa ny ordning</span><span class="sxs-lookup"><span data-stu-id="4f44c-497">Create new Order</span></span>
* <span data-ttu-id="4f44c-498">Cmdleten `Remove-AzDataBoxEdgeOrder` har lagts till</span><span class="sxs-lookup"><span data-stu-id="4f44c-498">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="4f44c-499">Ta bort ordning</span><span class="sxs-lookup"><span data-stu-id="4f44c-499">Remove the Order</span></span>
* <span data-ttu-id="4f44c-500">Cmdleten `New-AzDataBoxEdgeShare` har ändrats</span><span class="sxs-lookup"><span data-stu-id="4f44c-500">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="4f44c-501">Nu skapas lokal filresurs</span><span class="sxs-lookup"><span data-stu-id="4f44c-501">Now creates Local Share</span></span>
* <span data-ttu-id="4f44c-502">Cmdleten `Set-AzDataBoxEdgeRole` har lagts till</span><span class="sxs-lookup"><span data-stu-id="4f44c-502">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="4f44c-503">Nu kan IotRole mappas till filresursen</span><span class="sxs-lookup"><span data-stu-id="4f44c-503">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="4f44c-504">Cmdleten `Invoke-AzDataBoxEdgeDevice` har lagts till</span><span class="sxs-lookup"><span data-stu-id="4f44c-504">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="4f44c-505">Anropa genomsökningsuppdatering, ladda ned uppdatering, installera uppdateringar på enheten</span><span class="sxs-lookup"><span data-stu-id="4f44c-505">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="4f44c-506">Cmdleten `Get-AzDataBoxEdgeTrigger` har lagts till</span><span class="sxs-lookup"><span data-stu-id="4f44c-506">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="4f44c-507">Hämtar information om utlösare</span><span class="sxs-lookup"><span data-stu-id="4f44c-507">Gets the information about Triggers</span></span>
* <span data-ttu-id="4f44c-508">Cmdleten `New-AzDataBoxEdgeTrigger` har lagts till</span><span class="sxs-lookup"><span data-stu-id="4f44c-508">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="4f44c-509">Skapa nya utlösare</span><span class="sxs-lookup"><span data-stu-id="4f44c-509">Create new Triggers</span></span>
* <span data-ttu-id="4f44c-510">Cmdleten `Remove-AzDataBoxEdgeTrigger` har lagts till</span><span class="sxs-lookup"><span data-stu-id="4f44c-510">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="4f44c-511">Ta bort utlösare</span><span class="sxs-lookup"><span data-stu-id="4f44c-511">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4f44c-512">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4f44c-512">Az.DataFactory</span></span>
* <span data-ttu-id="4f44c-513">Uppdatera ADF .Net SDK-versionen till 4.4.0</span><span class="sxs-lookup"><span data-stu-id="4f44c-513">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="4f44c-514">Lägg till parametern ExpressCustomSetup för kommandot Set-AzureRmDataFactoryV2IntegrationRuntime för att aktivera installationskonfigurationer och komponenter från tredje part utan anpassat konfigurationsskript.</span><span class="sxs-lookup"><span data-stu-id="4f44c-514">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4f44c-515">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4f44c-515">Az.DataLakeStore</span></span>
* <span data-ttu-id="4f44c-516">Uppdatera dokumentation för Get-AzDataLakeStoreDeletedItem och Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="4f44c-516">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="4f44c-517">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="4f44c-517">Az.EventHub</span></span>
* <span data-ttu-id="4f44c-518">Korrigering av problem #10301: Korrigera datumformat för SAS-token</span><span class="sxs-lookup"><span data-stu-id="4f44c-518">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="4f44c-519">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="4f44c-519">Az.FrontDoor</span></span>
* <span data-ttu-id="4f44c-520">Lägg till parametern MinimumTlsVersion till Enable-AzFrontDoorCustomDomainHttps och New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="4f44c-520">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="4f44c-521">Lägg till parametrarna HealthProbeMethod och EnabledState till New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="4f44c-521">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="4f44c-522">Lägg till en ny cmdlet för att skapa BackendPoolsSettings-objekt som passar i skapande/uppdatering av Front Door</span><span class="sxs-lookup"><span data-stu-id="4f44c-522">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="4f44c-523">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="4f44c-523">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4f44c-524">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4f44c-524">Az.Network</span></span>
* <span data-ttu-id="4f44c-525">Ändra alternativexemplen Start-AzVirtualNetworkGatewayConnectionPacketCapture.md och Start-AzVirtualnetworkGatewayPacketCapture.md för FilterData.</span><span class="sxs-lookup"><span data-stu-id="4f44c-525">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="4f44c-526">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="4f44c-526">Az.PrivateDns</span></span>
* <span data-ttu-id="4f44c-527">Uppdaterade PrivateDns .NET SDK till version 1.0.0</span><span class="sxs-lookup"><span data-stu-id="4f44c-527">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4f44c-528">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4f44c-528">Az.RecoveryServices</span></span>
* <span data-ttu-id="4f44c-529">Stöd för att välja disktyp vid aktivering av skydd i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="4f44c-529">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="4f44c-530">Korrigering av bugg för åtgärdsredigering av återställningsplan i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="4f44c-530">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="4f44c-531">Återställningsstöd för att godkänna filestream-databaser i Azure Backup SQL.</span><span class="sxs-lookup"><span data-stu-id="4f44c-531">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="4f44c-532">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="4f44c-532">Az.RedisCache</span></span>
* <span data-ttu-id="4f44c-533">Parametern MinimumTlsVersion har lagts till i cmdletarna New-AzRedisCache och Set-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="4f44c-533">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="4f44c-534">Dessutom har MinimumTlsVersion lagts till i utdata för cmdleten Get-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="4f44c-534">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="4f44c-535">Verifiering har lagts till på parametern -Size i cmdletarna Set-AzRedisCache och New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="4f44c-535">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="4f44c-536">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4f44c-536">Az.Resources</span></span>
- <span data-ttu-id="4f44c-537">Uppdaterade policy-cmdletar för att använda den nya API-versionen 2019-06-01 som har en ny EnforcementMode-egenskap i policytilldelningen.</span><span class="sxs-lookup"><span data-stu-id="4f44c-537">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="4f44c-538">Uppdaterade hjälpexempel för skapandet av policydefinition</span><span class="sxs-lookup"><span data-stu-id="4f44c-538">Updated create policy definition help example</span></span>
- <span data-ttu-id="4f44c-539">Åtgärda bugg i Remove-AZADServicePrincipal -ServicePrincipalName, utlös null-referens när tjänstens huvudnamn inte hittas.</span><span class="sxs-lookup"><span data-stu-id="4f44c-539">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="4f44c-540">Åtgärda bugg i New-AZADServicePrincipal, utlös null-referens när klientorganisationen inte har någon prenumeration.</span><span class="sxs-lookup"><span data-stu-id="4f44c-540">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="4f44c-541">Ändra New-AzAdServicePrincipal för att endast lägga till autentiseringsuppgifter för det associerade programmet.</span><span class="sxs-lookup"><span data-stu-id="4f44c-541">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="4f44c-542">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4f44c-542">Az.Sql</span></span>
* <span data-ttu-id="4f44c-543">Stöd har lagts till för databasen ReadReplicaCount.</span><span class="sxs-lookup"><span data-stu-id="4f44c-543">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="4f44c-544">Korrigerade Set-AzSqlDatabase när zonredundans inte har angetts</span><span class="sxs-lookup"><span data-stu-id="4f44c-544">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="4f44c-545">3.0.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="4f44c-545">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="4f44c-546">Allmänt</span><span class="sxs-lookup"><span data-stu-id="4f44c-546">General</span></span>
* <span data-ttu-id="4f44c-547">Az. PrivateDns 1.0.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="4f44c-547">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="4f44c-548">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4f44c-548">Az.Accounts</span></span>
* <span data-ttu-id="4f44c-549">Lägg till ett utfasningsmeddelande för aliaset Resolve-error.</span><span class="sxs-lookup"><span data-stu-id="4f44c-549">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="4f44c-550">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="4f44c-550">Az.Advisor</span></span>
* <span data-ttu-id="4f44c-551">Den nya kategorin Operational Excellence har lagts till i cmdleten Get-AzAdvisorRecommendation.</span><span class="sxs-lookup"><span data-stu-id="4f44c-551">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="4f44c-552">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="4f44c-552">Az.Batch</span></span>
* <span data-ttu-id="4f44c-553">`CoreQuota` på `BatchAccountContext` har bytt namn till `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="4f44c-553">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="4f44c-554">Det finns även en ny `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="4f44c-554">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="4f44c-555">Detta påverkar **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="4f44c-555">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="4f44c-556">**New-AzBatchTask** `-ResourceFile`-parametern tar nu en samling `PSResourceFile`-objekt som kan skapas med hjälp av den nya cmdleten **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="4f44c-556">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="4f44c-557">Ny **New-AzBatchResourceFile**-cmdlet för att skapa `PSResourceFile`-objekt.</span><span class="sxs-lookup"><span data-stu-id="4f44c-557">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="4f44c-558">Dessa kan tillhandahållas till **New-AzBatchTask** på `-ResourceFile`-parametern.</span><span class="sxs-lookup"><span data-stu-id="4f44c-558">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="4f44c-559">Detta stöder två nya typer av resursfiler förutom det befintliga sättet med `HttpUrl`:</span><span class="sxs-lookup"><span data-stu-id="4f44c-559">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="4f44c-560">`AutoStorageContainerName`-baserade resursfiler laddar ned en hel container för automatisk lagring till Batch-noden.</span><span class="sxs-lookup"><span data-stu-id="4f44c-560">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="4f44c-561">`StorageContainerUrl`-baserade resursfiler laddar ned containern som anges i webbadressen till Batch-noden.</span><span class="sxs-lookup"><span data-stu-id="4f44c-561">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="4f44c-562">Tog bort egenskapen `ApplicationPackages` för `PSApplication` som returnerades av **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="4f44c-562">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="4f44c-563">Specifika paket i ett program kan nu hämtas med hjälp av **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="4f44c-563">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="4f44c-564">Till exempel: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="4f44c-564">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="4f44c-565">Bytt namn på `ApplicationId` till `ApplicationName` på **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** och **Set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="4f44c-565">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="4f44c-566">`ApplicationId` är nu ett alias för `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="4f44c-566">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="4f44c-567">Ny `PSWindowsUserConfiguration`-egenskap till `PSUserAccount` lades till.</span><span class="sxs-lookup"><span data-stu-id="4f44c-567">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="4f44c-568">Bytte namn på `Version` till `Name` på `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="4f44c-568">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="4f44c-569">Bytte namn på `BlobSource` till `HttpUrl` på `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="4f44c-569">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="4f44c-570">Tog bort egenskapen `OSDisk` från `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="4f44c-570">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="4f44c-571">Tog bort **Set-AzBatchPoolOSVersion**.</span><span class="sxs-lookup"><span data-stu-id="4f44c-571">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="4f44c-572">Den här åtgärden stöds inte längre.</span><span class="sxs-lookup"><span data-stu-id="4f44c-572">This operation is no longer supported.</span></span>
* <span data-ttu-id="4f44c-573">`TargetOSVersion` har tagits bort från `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="4f44c-573">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="4f44c-574">Bytte namn på `CurrentOSVersion` till `OSVersion` på `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="4f44c-574">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="4f44c-575">`DataEgressGiB` och `DataIngressGiB` har tagits bort från `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="4f44c-575">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="4f44c-576">Tog bort **Get-AzBatchNodeAgentSku** och ersatte det med **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="4f44c-576">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="4f44c-577">**Get-AzBatchSupportedImage** returnerar samma data som **Get-AzBatchNodeAgentSku** men i ett mer användarvänligt format.</span><span class="sxs-lookup"><span data-stu-id="4f44c-577">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="4f44c-578">Nya icke-verifierade avbildningar returneras nu också.</span><span class="sxs-lookup"><span data-stu-id="4f44c-578">New non-verified images are also now returned.</span></span> <span data-ttu-id="4f44c-579">Ytterligare information om `Capabilities` och `BatchSupportEndOfLife` för varje avbildning inkluderas också.</span><span class="sxs-lookup"><span data-stu-id="4f44c-579">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="4f44c-580">Lade till möjlighet att montera fjärrfilsystem på varje nod i en pool via den nya parametern `MountConfiguration` för **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="4f44c-580">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="4f44c-581">Har nu stöd för nätverkssäkerhetsregler som blockerar nätverksåtkomst till en pool baserat på källportens trafik.</span><span class="sxs-lookup"><span data-stu-id="4f44c-581">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="4f44c-582">Detta görs via egenskapen `SourcePortRanges` på `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="4f44c-582">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="4f44c-583">När du kör en container stöder nu Batch körningen av uppgiften i arbetskatalogen för containern eller i arbetskatalogen för Batch-uppgiften.</span><span class="sxs-lookup"><span data-stu-id="4f44c-583">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="4f44c-584">Detta styrs av egenskapen `WorkingDirectory` på `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="4f44c-584">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="4f44c-585">Lade till en funktion för att ange en samling av offentliga IP-adresser på `PSNetworkConfiguration` via den nya egenskapen `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="4f44c-585">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="4f44c-586">Detta garanterar att noderna i poolen har en IP-adress från listan över IP-adresser som tillhandahållits av användare.</span><span class="sxs-lookup"><span data-stu-id="4f44c-586">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="4f44c-587">Om inget värde anges är standardvärdet för `WaitForSuccess` på `PSSTartTask` nu `$True` (var tidigare `$False`).</span><span class="sxs-lookup"><span data-stu-id="4f44c-587">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="4f44c-588">Om inget värde anges är standardvärdet för `Scope` på `PSAutoUserSpecification` nu `Pool` (var tidigare `Task` på Windows och `Pool` på Linux).</span><span class="sxs-lookup"><span data-stu-id="4f44c-588">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="4f44c-589">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="4f44c-589">Az.Cdn</span></span>
* <span data-ttu-id="4f44c-590">Introducerade UrlRewriteAction och CacheKeyQueryStringAction till RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="4f44c-590">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="4f44c-591">Åtgärdade flera buggar, som saknade indata för ”väljare” i cmdleten New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="4f44c-591">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4f44c-592">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4f44c-592">Az.Compute</span></span>
* <span data-ttu-id="4f44c-593">Funktion för diskkrypteringsuppsättning</span><span class="sxs-lookup"><span data-stu-id="4f44c-593">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="4f44c-594">Nya cmdletar:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="4f44c-594">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="4f44c-595">Parametern DiskEncryptionSetId har lagts till i följande cmdletar:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="4f44c-595">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="4f44c-596">Parametrarna DiskEncryptionSetId och EncryptionType har lagts till i följande cmdletar:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="4f44c-596">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="4f44c-597">Lägg till parametern PublicIPAddressVersion i New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="4f44c-597">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="4f44c-598">Flytta FileUris för anpassat skripttillägg från offentlig inställning till skyddad inställning</span><span class="sxs-lookup"><span data-stu-id="4f44c-598">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="4f44c-599">Lägg till ScaleInPolicy i cmdletarna New-AzVmss, New-AzVmssConfig och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4f44c-599">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="4f44c-600">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="4f44c-600">Breaking changes</span></span>
    - <span data-ttu-id="4f44c-601">Parametern UploadSizeInBytes används istället för DiskSizeGB för New-AzDiskConfig när CreateOption är Uppladdning</span><span class="sxs-lookup"><span data-stu-id="4f44c-601">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="4f44c-602">PublishingProfile.Source.ManagedImage.Id ersätts med StorageProfile.Source.Id i objektet GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="4f44c-602">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4f44c-603">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4f44c-603">Az.DataFactory</span></span>
* <span data-ttu-id="4f44c-604">Uppdatera ADF .Net SDK-versionen till 4.3.0</span><span class="sxs-lookup"><span data-stu-id="4f44c-604">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4f44c-605">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4f44c-605">Az.DataLakeStore</span></span>
* <span data-ttu-id="4f44c-606">Uppdatera ADLS SDK-version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) innehåller följande korrigeringar</span><span class="sxs-lookup"><span data-stu-id="4f44c-606">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="4f44c-607">Undvik att utlösa undantag när det inte går att deserialisera creationtime för inmatning av papperskorg eller katalog.</span><span class="sxs-lookup"><span data-stu-id="4f44c-607">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="4f44c-608">Gör inställning tillgänglig per tidsgräns för förfrågan i adlsclient</span><span class="sxs-lookup"><span data-stu-id="4f44c-608">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="4f44c-609">Korrigera överföringen av ursprunglig syncflag för badoffset-återställning</span><span class="sxs-lookup"><span data-stu-id="4f44c-609">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="4f44c-610">Korrigera EnumerateDirectory för att hämta fortsättningstoken när svar har kontrollerats</span><span class="sxs-lookup"><span data-stu-id="4f44c-610">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="4f44c-611">Korrigera bugg i Concat</span><span class="sxs-lookup"><span data-stu-id="4f44c-611">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="4f44c-612">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="4f44c-612">Az.FrontDoor</span></span>
* <span data-ttu-id="4f44c-613">Åtgärdade diverse stavfel i modul</span><span class="sxs-lookup"><span data-stu-id="4f44c-613">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="4f44c-614">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="4f44c-614">Az.HDInsight</span></span>
* <span data-ttu-id="4f44c-615">Korrigerade buggen att kunder får felet ”inte en giltig Base-64-sträng” vid användning av Get-AzHDInsightCluster för att hämta klustret med ADLSGen1-lagring.</span><span class="sxs-lookup"><span data-stu-id="4f44c-615">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="4f44c-616">Lägg till en parameter med namnet ”ApplicationId” i de tre cmdletarna Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig och New-AzHDInsightCluster så att kunden kan tillhandahålla tjänstens huvudnamn för program-ID för åtkomst till Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="4f44c-616">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="4f44c-617">Ändrade Microsoft.Azure.Management.HDInsight från 2.1.0 till 5.1.0</span><span class="sxs-lookup"><span data-stu-id="4f44c-617">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="4f44c-618">Fem cmdletar har tagits bort:</span><span class="sxs-lookup"><span data-stu-id="4f44c-618">Removed five cmdlets:</span></span>
    - <span data-ttu-id="4f44c-619">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="4f44c-619">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="4f44c-620">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="4f44c-620">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="4f44c-621">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="4f44c-621">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="4f44c-622">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="4f44c-622">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="4f44c-623">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="4f44c-623">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="4f44c-624">Tre cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="4f44c-624">Added three cmdlets:</span></span>
    - <span data-ttu-id="4f44c-625">Get-AzHDInsightMonitoring som ersätter Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="4f44c-625">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="4f44c-626">Enable-AzHDInsightMonitoring som ersätter Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="4f44c-626">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="4f44c-627">Disable-AzHDInsightMonitoring som ersätter Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="4f44c-627">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="4f44c-628">Korrigerade cmdleten Get-AzHDInsightProperties för att stödja hämtning av funktionsinformation från en viss plats.</span><span class="sxs-lookup"><span data-stu-id="4f44c-628">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="4f44c-629">Parameteruppsättningarna (Spark1 och Spark2) har tagits bort från Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="4f44c-629">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="4f44c-630">Lägg till exempel för cmdleten Add-AzHDInsightSecurityProfile till hjälpdokumenten.</span><span class="sxs-lookup"><span data-stu-id="4f44c-630">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="4f44c-631">Ändrade utdatatyp för följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="4f44c-631">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="4f44c-632">Ändrade utdatatyp för Get-AzHDInsightProperties från CapabilitiesResponse till AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="4f44c-632">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="4f44c-633">Ändrade utdatatyp för Remove-AzHDInsightCluster från ClusterGetResponse till bool.</span><span class="sxs-lookup"><span data-stu-id="4f44c-633">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="4f44c-634">Ändrade utdatatyp för Set-AzHDInsightGatewaySettings HttpConnectivitySettings till GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="4f44c-634">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="4f44c-635">Lade till testfall för vissa scenarier.</span><span class="sxs-lookup"><span data-stu-id="4f44c-635">Added some scenario test cases.</span></span>
* <span data-ttu-id="4f44c-636">Ta bort vissa alias: Add-AzHDInsightConfigValues, Get-AzHDInsightProperties.</span><span class="sxs-lookup"><span data-stu-id="4f44c-636">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="4f44c-637">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="4f44c-637">Az.IotHub</span></span>
* <span data-ttu-id="4f44c-638">Icke-bakåtkompatibla ändringar:</span><span class="sxs-lookup"><span data-stu-id="4f44c-638">Breaking changes:</span></span>
    - <span data-ttu-id="4f44c-639">Cmdleten Add-AzIotHubEventHubConsumerGroup har inte längre stöd för parametern EventHubEndpointName och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="4f44c-639">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="4f44c-640">Parameteruppsättningen __AllParameterSets för cmdleten Add-AzIotHubEventHubConsumerGroup har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="4f44c-640">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="4f44c-641">Cmdleten Get-AzIotHubEventHubConsumerGroup har inte längre stöd för parametern EventHubEndpointName och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="4f44c-641">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="4f44c-642">Parameteruppsättningen __AllParameterSets för cmdleten Get-AzIotHubEventHubConsumerGroup har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="4f44c-642">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="4f44c-643">Egenskapen OperationsMonitoringProperties av typen Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="4f44c-643">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="4f44c-644">Egenskapen OperationsMonitoringProperties av typen Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="4f44c-644">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="4f44c-645">Cmdleten New-AzIotHubExportDevice stöder inte längre aliaset New-AzIotHubExportDevices.</span><span class="sxs-lookup"><span data-stu-id="4f44c-645">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="4f44c-646">Cmdleten New-AzIotHubImportDevice stöder inte längre aliaset New-AzIotHubImportDevices.</span><span class="sxs-lookup"><span data-stu-id="4f44c-646">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="4f44c-647">Cmdleten Remove-AzIotHubEventHubConsumerGroup har inte längre stöd för parametern EventHubEndpointName och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="4f44c-647">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="4f44c-648">Parameteruppsättningen __AllParameterSets för cmdleten Remove-AzIotHubEventHubConsumerGroup har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="4f44c-648">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="4f44c-649">Cmdleten Set-AzIotHub har inte längre stöd för parametern OperationsMonitoringProperties och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="4f44c-649">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="4f44c-650">Parameteruppsättningen UpdateOperationsMonitoringProperties för cmdleten Set-AzIotHub har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="4f44c-650">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4f44c-651">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4f44c-651">Az.RecoveryServices</span></span>
* <span data-ttu-id="4f44c-652">Azure Site Recovery-stöd för att konfigurera nätverksresurser som NSG, offentliga IP-adresser och interna lastbalanserare för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="4f44c-652">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="4f44c-653">Azure Site Recovery-stöd för att skriva till hanterad disk för vMWare till Azure.</span><span class="sxs-lookup"><span data-stu-id="4f44c-653">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="4f44c-654">Azure Site Recovery-stöd för NIC-reduktion för vMWare till Azure.</span><span class="sxs-lookup"><span data-stu-id="4f44c-654">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="4f44c-655">Azure Site Recovery-stöd för accelererat nätverk för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="4f44c-655">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="4f44c-656">Azure Site Recovery-stöd för automatisk uppdatering av agent för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="4f44c-656">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="4f44c-657">Azure Site Recovery-stöd för Standard SSD för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="4f44c-657">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="4f44c-658">Azure Site Recovery-stöd för tvåstegskryptering i Azure Disk Encryption för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="4f44c-658">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="4f44c-659">Azure Site Recovery-stöd för att skydda nyligen tillagda diskar för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="4f44c-659">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="4f44c-660">En funktion för mjuk borttagning av virtuella datorer samt tester för mjuk borttagning har tagits bort</span><span class="sxs-lookup"><span data-stu-id="4f44c-660">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="4f44c-661">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4f44c-661">Az.Resources</span></span>
* <span data-ttu-id="4f44c-662">Uppdatera beroendesammansättning för Microsoft.Extensions.Caching.Memory från 1.1.1 till 2.2</span><span class="sxs-lookup"><span data-stu-id="4f44c-662">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4f44c-663">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4f44c-663">Az.Network</span></span>
* <span data-ttu-id="4f44c-664">Ändra alla cmdletar för PrivateEndpointConnection så att de stöder generiska tjänstleverantörer.</span><span class="sxs-lookup"><span data-stu-id="4f44c-664">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="4f44c-665">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="4f44c-665">Updated cmdlet:</span></span>
        - <span data-ttu-id="4f44c-666">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4f44c-666">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="4f44c-667">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4f44c-667">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="4f44c-668">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4f44c-668">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="4f44c-669">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4f44c-669">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="4f44c-670">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4f44c-670">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="4f44c-671">Lägg till ny cmdlet för PrivateLinkResource så att det också stöder generiska tjänstleverantörer.</span><span class="sxs-lookup"><span data-stu-id="4f44c-671">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="4f44c-672">Ny cmdlet:</span><span class="sxs-lookup"><span data-stu-id="4f44c-672">New cmdlet:</span></span>
        - <span data-ttu-id="4f44c-673">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="4f44c-673">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="4f44c-674">Lägg till nya fält och parametrar för funktionen Proxy Protocol V2.</span><span class="sxs-lookup"><span data-stu-id="4f44c-674">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="4f44c-675">Lägg till egenskapen EnableProxyProtocol i PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="4f44c-675">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="4f44c-676">Lägg till egenskapen LinkIdentifier i PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4f44c-676">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="4f44c-677">Uppdaterade New-AzPrivateLinkService för att lägga till den nya valfria parametern EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="4f44c-677">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="4f44c-678">Korrigera felaktig beskrivning av parameter i referensdokumentationen för New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="4f44c-678">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="4f44c-679">Nya cmdletar som stöder Azure-brandväggsprincipen</span><span class="sxs-lookup"><span data-stu-id="4f44c-679">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="4f44c-680">Lägg till stöd för den underordnade resursen RouteTables för VirtualHub</span><span class="sxs-lookup"><span data-stu-id="4f44c-680">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="4f44c-681">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="4f44c-681">New cmdlets added:</span></span>
        - <span data-ttu-id="4f44c-682">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="4f44c-682">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="4f44c-683">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="4f44c-683">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="4f44c-684">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="4f44c-684">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="4f44c-685">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="4f44c-685">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="4f44c-686">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="4f44c-686">Set-AzVirtualHub</span></span>
* <span data-ttu-id="4f44c-687">Lägg till stöd för ny egenskaps-SKU för VirtualHub och VirtualWANType för VirtualWan</span><span class="sxs-lookup"><span data-stu-id="4f44c-687">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="4f44c-688">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="4f44c-688">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="4f44c-689">New-AzVirtualHub: lade till parameter-SKU</span><span class="sxs-lookup"><span data-stu-id="4f44c-689">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="4f44c-690">Update-AzVirtualHub: lade till parameter-SKU</span><span class="sxs-lookup"><span data-stu-id="4f44c-690">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="4f44c-691">New-AzVirtualWan: lade till parametern VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="4f44c-691">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="4f44c-692">Update-AzVirtualWan: lade till parametern VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="4f44c-692">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="4f44c-693">Lägg till stöd för egenskapen EnableInternetSecurity för HubVnetConnection, VpnConnection och ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="4f44c-693">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="4f44c-694">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="4f44c-694">New cmdlets added:</span></span>
        - <span data-ttu-id="4f44c-695">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="4f44c-695">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="4f44c-696">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="4f44c-696">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="4f44c-697">New-AzureRmVirtualHubVnetConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="4f44c-697">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="4f44c-698">New-AzureRmVpnConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="4f44c-698">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="4f44c-699">Update-AzureRmVpnConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="4f44c-699">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="4f44c-700">New-AzureRmExpressRouteConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="4f44c-700">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="4f44c-701">Set-AzureRmExpressRouteConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="4f44c-701">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="4f44c-702">Lägg till stöd för att konfigurera TopLevel WebApplicationFirewall-princip</span><span class="sxs-lookup"><span data-stu-id="4f44c-702">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="4f44c-703">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="4f44c-703">New cmdlets added:</span></span>
        - <span data-ttu-id="4f44c-704">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="4f44c-704">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="4f44c-705">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="4f44c-705">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="4f44c-706">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="4f44c-706">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="4f44c-707">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="4f44c-707">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="4f44c-708">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="4f44c-708">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="4f44c-709">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="4f44c-709">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="4f44c-710">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="4f44c-710">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="4f44c-711">New-AzApplicationGatewayFirewallPolicy: parametrarna PolicySetting, ManagedRule har lagts till</span><span class="sxs-lookup"><span data-stu-id="4f44c-711">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="4f44c-712">Stöd för operator för geomatchning har lagts till på CustomRule</span><span class="sxs-lookup"><span data-stu-id="4f44c-712">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="4f44c-713">Geomatchning har lagts till i operatorn på FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="4f44c-713">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="4f44c-714">Stöd har lagts till för brandväggsprinciperna perListener och perSite</span><span class="sxs-lookup"><span data-stu-id="4f44c-714">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="4f44c-715">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="4f44c-715">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="4f44c-716">New-AzApplicationGatewayHttpListener: parametrarna FirewallPolicy, FirewallPolicyId har lagts till</span><span class="sxs-lookup"><span data-stu-id="4f44c-716">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="4f44c-717">New-AzApplicationGatewayPathRuleConfig: parametrarna FirewallPolicy, FirewallPolicyId har lagts till</span><span class="sxs-lookup"><span data-stu-id="4f44c-717">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="4f44c-718">Åtgärdat så att nödvändigt undernät med namnet AzureBastionSubnet i PSBastion kan vara skiftlägesokänsligt</span><span class="sxs-lookup"><span data-stu-id="4f44c-718">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="4f44c-719">Stöd för mål-FQDN:er i nätverksregler och översatt FQDN i NAT-regler för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="4f44c-719">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="4f44c-720">Lägg till stöd för resursen RouteTables för IpGroup på den högsta nivån</span><span class="sxs-lookup"><span data-stu-id="4f44c-720">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="4f44c-721">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="4f44c-721">New cmdlets added:</span></span>
        - <span data-ttu-id="4f44c-722">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="4f44c-722">New-AzIpGroup</span></span>
        - <span data-ttu-id="4f44c-723">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="4f44c-723">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="4f44c-724">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="4f44c-724">Get-AzIpGroup</span></span>
        - <span data-ttu-id="4f44c-725">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="4f44c-725">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="4f44c-726">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4f44c-726">Az.ServiceFabric</span></span>
* <span data-ttu-id="4f44c-727">Ta bort cmdleten Add-AzServiceFabricApplicationCertificate eftersom det här scenariot omfattas av Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="4f44c-727">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="4f44c-728">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4f44c-728">Az.Sql</span></span>
* <span data-ttu-id="4f44c-729">Stöd har lagts till för återställning av utelämnade databaser på hanterade instanser.</span><span class="sxs-lookup"><span data-stu-id="4f44c-729">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="4f44c-730">Inaktuella gamla cmdletar för granskning från kod.</span><span class="sxs-lookup"><span data-stu-id="4f44c-730">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="4f44c-731">Tog bort inaktuella alias:</span><span class="sxs-lookup"><span data-stu-id="4f44c-731">Removed deprecated aliases:</span></span>
* <span data-ttu-id="4f44c-732">Get-AzSqlDatabaseIndexRecommendations (använd Get-AzSqlDatabaseIndexRecommendation istället)</span><span class="sxs-lookup"><span data-stu-id="4f44c-732">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="4f44c-733">Get-AzSqlDatabaseRestorePoints (använd Get-AzSqlDatabaseRestorePoint istället)</span><span class="sxs-lookup"><span data-stu-id="4f44c-733">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="4f44c-734">Ta bort cmdleten Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="4f44c-734">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="4f44c-735">Ta bort alias för inaktuella cmdletar för inställningar för utvärdering av säkerhetsrisk</span><span class="sxs-lookup"><span data-stu-id="4f44c-735">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="4f44c-736">Inaktualisera cmdletar för inställningar för avancerad hotidentifiering</span><span class="sxs-lookup"><span data-stu-id="4f44c-736">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="4f44c-737">Lägga till cmdletar för att inaktivera och aktivera känslighetsrekommendationer på kolumner i en databas.</span><span class="sxs-lookup"><span data-stu-id="4f44c-737">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4f44c-738">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4f44c-738">Az.Storage</span></span>
* <span data-ttu-id="4f44c-739">Stöd för att aktivera stora filresurser vid skapande eller uppdatering av lagringskonto</span><span class="sxs-lookup"><span data-stu-id="4f44c-739">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="4f44c-740">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4f44c-740">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="4f44c-741">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4f44c-741">Set-AzStorageAccount</span></span>
* <span data-ttu-id="4f44c-742">När du stänger/hämtar en filreferens kan du hoppa över kontrollen av huruvida indatasökvägen är en filkatalog eller en fil för att undvika problem med objekt som har status DeletePending</span><span class="sxs-lookup"><span data-stu-id="4f44c-742">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="4f44c-743">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="4f44c-743">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="4f44c-744">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="4f44c-744">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="4f44c-745">2.8.0 – oktober 2019</span><span class="sxs-lookup"><span data-stu-id="4f44c-745">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="4f44c-746">Allmänt</span><span class="sxs-lookup"><span data-stu-id="4f44c-746">General</span></span>
* <span data-ttu-id="4f44c-747">AZ. HealthcareApis 1.0.0-version</span><span class="sxs-lookup"><span data-stu-id="4f44c-747">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="4f44c-748">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4f44c-748">Az.Accounts</span></span>
* <span data-ttu-id="4f44c-749">Uppdatera telemetri och URL-omskrivning för genererade moduler, korrigera Windows-enhetstester.</span><span class="sxs-lookup"><span data-stu-id="4f44c-749">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="4f44c-750">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4f44c-750">Az.ApiManagement</span></span>
* <span data-ttu-id="4f44c-751">**Set-AzApiManagementApi** – Tillagt stöd för att uppdatera Api till ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="4f44c-751">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="4f44c-752">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="4f44c-752">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4f44c-753">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4f44c-753">Az.Automation</span></span>
* <span data-ttu-id="4f44c-754">Åtgärdade cmdleten New-AzureAutomationSoftwareUpdateConfiguration för parametern för inställning av Linux-omstart.</span><span class="sxs-lookup"><span data-stu-id="4f44c-754">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="4f44c-755">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="4f44c-755">Az.Batch</span></span>
* <span data-ttu-id="4f44c-756">**Get-AzBatchNodeAgentSku** är inaktuell och ersätts av **Get-AzBatchSupportImage** i version 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="4f44c-756">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4f44c-757">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4f44c-757">Az.Compute</span></span>
* <span data-ttu-id="4f44c-758">Lägg till parametrarna Priority, EvictionPolicy och MaxPrice till cmdletarna New-AzVM och New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4f44c-758">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="4f44c-759">Korrigera varningsmeddelande och hjälpdokument för cmdletarna Add-AzVMAdditionalUnattendContent och Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="4f44c-759">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="4f44c-760">Åtgärda – skipVmBackup-undantag för virtuella Linux-datorer med hanterade diskar för Set-AzVMDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="4f44c-760">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="4f44c-761">Åtgärda fel i uppdatera krypteringsinställningarna i set-AzVMDiskEncryptionExtension, scenario i två steg.</span><span class="sxs-lookup"><span data-stu-id="4f44c-761">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4f44c-762">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4f44c-762">Az.DataFactory</span></span>
* <span data-ttu-id="4f44c-763">Lägga till CRUD-kommandon för ADF V2-dataflödet: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow och Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="4f44c-763">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="4f44c-764">Lägger till åtgärdskommandon för ADF V2-dataflödesfelsökningssession: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand och Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="4f44c-764">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="4f44c-765">Uppdatera ADF .Net SDK-versionen till 4.2.0</span><span class="sxs-lookup"><span data-stu-id="4f44c-765">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4f44c-766">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4f44c-766">Az.DataLakeStore</span></span>
* <span data-ttu-id="4f44c-767">Korrigera kontovalidering så att konton med ”-” kan skickas utan domän</span><span class="sxs-lookup"><span data-stu-id="4f44c-767">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="4f44c-768">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="4f44c-768">Az.HealthcareApis</span></span>
* <span data-ttu-id="4f44c-769">PowerShell-versionen har uppdaterats till 1.0.0</span><span class="sxs-lookup"><span data-stu-id="4f44c-769">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="4f44c-770">Uppdaterade SDK-versionen till 1.0.2</span><span class="sxs-lookup"><span data-stu-id="4f44c-770">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="4f44c-771">Uppdatera i tester för att referera till en ny SDK-version</span><span class="sxs-lookup"><span data-stu-id="4f44c-771">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="4f44c-772">Utdatastrukturen har uppdaterats från kapslad till förenklad.</span><span class="sxs-lookup"><span data-stu-id="4f44c-772">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="4f44c-773">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="4f44c-773">Az.IotHub</span></span>
* <span data-ttu-id="4f44c-774">Lägg till ny routningskälla: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="4f44c-774">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="4f44c-775">Mindre felkorrigering: Get-AzIothub returnerar inte subscriptionId</span><span class="sxs-lookup"><span data-stu-id="4f44c-775">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4f44c-776">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4f44c-776">Az.Monitor</span></span>
* <span data-ttu-id="4f44c-777">Nya åtgärdsgruppsmottagare har lagts till för åtgärdsgrupp   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="4f44c-777">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="4f44c-778">Använd vanligt aviseringsschema som är aktiverat för mottagarna.</span><span class="sxs-lookup"><span data-stu-id="4f44c-778">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="4f44c-779">Detta gäller inte för SMS, push för Azure-app, ITSM och röstmottagare</span><span class="sxs-lookup"><span data-stu-id="4f44c-779">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="4f44c-780">Webhooks har nu stöd för Azure Active Directory-autentisering.</span><span class="sxs-lookup"><span data-stu-id="4f44c-780">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4f44c-781">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4f44c-781">Az.Network</span></span>
* <span data-ttu-id="4f44c-782">Lägg till ny cmdlet Get-AzAvailableServiceAlias som kan anropas för att hämta de alias som kan användas för tjänstslutpunktsprinciper.</span><span class="sxs-lookup"><span data-stu-id="4f44c-782">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="4f44c-783">Stöd för tillägg av trafikväljare har lagts till i gatewayanslutningar för virtuella nätverk</span><span class="sxs-lookup"><span data-stu-id="4f44c-783">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="4f44c-784">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="4f44c-784">New cmdlets added:</span></span>
        - <span data-ttu-id="4f44c-785">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="4f44c-785">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="4f44c-786">Cmdletar har uppdaterats med valfri parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="4f44c-786">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="4f44c-787">Lägg till stöd för ESP- och AH-protokoll i konfiguration av nätverkssäkerhetsregler</span><span class="sxs-lookup"><span data-stu-id="4f44c-787">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="4f44c-788">Uppdaterade cmdletar:</span><span class="sxs-lookup"><span data-stu-id="4f44c-788">Updated cmdlets:</span></span>
        - <span data-ttu-id="4f44c-789">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4f44c-789">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="4f44c-790">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4f44c-790">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="4f44c-791">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4f44c-791">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="4f44c-792">Förbättra hanteringen av undantag i Cortex-cmdletar</span><span class="sxs-lookup"><span data-stu-id="4f44c-792">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="4f44c-793">Nya generationer och SKU:er för VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="4f44c-793">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="4f44c-794">Introducera nya generationer för VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="4f44c-794">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="4f44c-795">Introducera nya SKU:er med högt dataflöde för VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="4f44c-795">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="4f44c-796">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="4f44c-796">Az.RedisCache</span></span>
* <span data-ttu-id="4f44c-797">Uppdaterad referensdokumentation för ”set-AzRedisCache” för att inkludera saknade värden för parametern ”size”</span><span class="sxs-lookup"><span data-stu-id="4f44c-797">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="4f44c-798">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4f44c-798">Az.Sql</span></span>
* <span data-ttu-id="4f44c-799">Lägg till stöd för inställningen Active Directory administratör på den hanterade instansen</span><span class="sxs-lookup"><span data-stu-id="4f44c-799">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4f44c-800">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4f44c-800">Az.Storage</span></span>
* <span data-ttu-id="4f44c-801">Uppdatera Lagringsklientbibliotek till 11.1.0</span><span class="sxs-lookup"><span data-stu-id="4f44c-801">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="4f44c-802">Lista containrar med hanteringsplans-API, kommer att listas med NextPageLink</span><span class="sxs-lookup"><span data-stu-id="4f44c-802">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="4f44c-803">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="4f44c-803">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="4f44c-804">Lista lagringskonton från prenumerationen, kommer att listas med NextPageLink</span><span class="sxs-lookup"><span data-stu-id="4f44c-804">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="4f44c-805">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4f44c-805">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="4f44c-806">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="4f44c-806">Az.StorageSync</span></span>
* <span data-ttu-id="4f44c-807">Åtgärda problemet 9810 i Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="4f44c-807">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4f44c-808">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4f44c-808">Az.Websites</span></span>
* <span data-ttu-id="4f44c-809">Set-AzWebApp – uppdatering av ASP för en app misslyckades</span><span class="sxs-lookup"><span data-stu-id="4f44c-809">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="4f44c-810">2.7.0 – september 2019</span><span class="sxs-lookup"><span data-stu-id="4f44c-810">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="4f44c-811">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4f44c-811">Az.ApiManagement</span></span>
* <span data-ttu-id="4f44c-812">Uppdatera ”-Format”-parameterbeskrivningen i ”Set-AzApiManagementPolicy”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="4f44c-812">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="4f44c-813">Referenser för den föråldrade cmdleten ”Update-AzApiManagementDeployment” har tagits bort från referensdokumentationen.</span><span class="sxs-lookup"><span data-stu-id="4f44c-813">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="4f44c-814">Använd ”Set-AzApiManagement” i stället.</span><span class="sxs-lookup"><span data-stu-id="4f44c-814">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4f44c-815">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4f44c-815">Az.Automation</span></span>
* <span data-ttu-id="4f44c-816">Stavfel har korrigerats i exempel i referensdokumentationen för ”Register-AzAutomationDscNode”</span><span class="sxs-lookup"><span data-stu-id="4f44c-816">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="4f44c-817">Klargörande har lagts till om OS-begränsningar för Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="4f44c-817">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="4f44c-818">Null-referensundantag har korrigerats för -Wait-alternativet i Start-AzAutomationRunbook-cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4f44c-818">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4f44c-819">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4f44c-819">Az.Compute</span></span>
* <span data-ttu-id="4f44c-820">Lägg till UploadSizeInBytes-parameter till New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="4f44c-820">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="4f44c-821">Lägg till Incremental-parameter till New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="4f44c-821">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="4f44c-822">Lägg till en funktion för virtuella datorer med låg prioritet:</span><span class="sxs-lookup"><span data-stu-id="4f44c-822">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="4f44c-823">MaxPrice-, EvictionPolicy- och Priority-parametrar har lagts till i New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="4f44c-823">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="4f44c-824">MaxPrice-parametern har lagts till i New-AzVmssConfig-, Update-AzVM- och Update-AzVmss-cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="4f44c-824">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="4f44c-825">Åtgärda problem med VM-referenser för Get-AzAvailabilitySet-cmdleten när alla tillgänglighetsuppsättningar i prenumerationen visas.</span><span class="sxs-lookup"><span data-stu-id="4f44c-825">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="4f44c-826">Korrigera null-undantaget för Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="4f44c-826">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="4f44c-827">Korrigera VHD-metoden för sökning relativt till slut.</span><span class="sxs-lookup"><span data-stu-id="4f44c-827">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="4f44c-828">Åtgärda UltraSSD-problem för New-AzVM och Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="4f44c-828">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4f44c-829">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4f44c-829">Az.DataFactory</span></span>
* <span data-ttu-id="4f44c-830">Lägger till 3 nya kommandon för ADF V2 – Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription och Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="4f44c-830">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="4f44c-831">ADF .Net SDK har uppdaterats till 4.1.3</span><span class="sxs-lookup"><span data-stu-id="4f44c-831">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="4f44c-832">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="4f44c-832">Az.HDInsight</span></span>
* <span data-ttu-id="4f44c-833">Anrop för icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="4f44c-833">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="4f44c-834">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="4f44c-834">Az.IotHub</span></span>
* <span data-ttu-id="4f44c-835">Lägg till stöd för att anropa redundans för en IotHub till den geo-länkade katastrofåterställningsregionen.</span><span class="sxs-lookup"><span data-stu-id="4f44c-835">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="4f44c-836">Lägg till stöd för att hantera meddelandeberikning för en IotHub.</span><span class="sxs-lookup"><span data-stu-id="4f44c-836">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="4f44c-837">Nya cmdlet:ar är:</span><span class="sxs-lookup"><span data-stu-id="4f44c-837">New cmdlets are:</span></span>
    - <span data-ttu-id="4f44c-838">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="4f44c-838">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="4f44c-839">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="4f44c-839">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="4f44c-840">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="4f44c-840">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="4f44c-841">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="4f44c-841">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4f44c-842">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4f44c-842">Az.Monitor</span></span>
* <span data-ttu-id="4f44c-843">Pekar på den senaste Monitor SDK:n, dvs. 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="4f44c-843">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="4f44c-844">Lägger till bakåtkompatibla ändringar i Metrics-cmdletarna, dvs. enhetsuppräkningen stöder flera nya värden.</span><span class="sxs-lookup"><span data-stu-id="4f44c-844">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="4f44c-845">Detta är skrivskyddade cmdletar, så det förekommer inga ändringar i inmatningen för cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="4f44c-845">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="4f44c-846">API-versionen för **ActionGroups**-begäranden är nu **2019-06-01**. Tidigare var den **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="4f44c-846">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="4f44c-847">Test av scenarier har uppdaterats för att anpassas till den här ändringen.</span><span class="sxs-lookup"><span data-stu-id="4f44c-847">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="4f44c-848">Ett nytt obligatoriskt argument har lagts till för konstruktorerna för klasserna **EmailReceiver** och **WebhookReceiver** – ett booleskt värde med namnet **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="4f44c-848">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="4f44c-849">Värdet är för närvarande fast till **false** så att den här icke-bakåtkompatibla ändringen är dold från cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="4f44c-849">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="4f44c-850">**Obs!** Det här är en tillfällig ändring som måste verifieras av Alerts-teamet.</span><span class="sxs-lookup"><span data-stu-id="4f44c-850">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="4f44c-851">Ordningen på argumenten för konstruktorn för klassen **Source** (relaterad till klassen **ScheduledQueryRuleSource**) har ändrats från den tidigare SDK:n.</span><span class="sxs-lookup"><span data-stu-id="4f44c-851">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="4f44c-852">Den här ändringen krävde korrigering av två enhetstest: de kompilerades, men testerna skickades inte.</span><span class="sxs-lookup"><span data-stu-id="4f44c-852">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="4f44c-853">Ordningen på argumenten för konstruktorn för klassen **AlertingAction** (relaterad till klassen **ScheduledQueryRuleSource**) har ändrats från den tidigare SDK:n.</span><span class="sxs-lookup"><span data-stu-id="4f44c-853">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="4f44c-854">Den här ändringen krävde korrigering av två enhetstest: de kompilerades, men testerna skickades inte.</span><span class="sxs-lookup"><span data-stu-id="4f44c-854">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="4f44c-855">Stöd för kriterier för dynamiskt tröskelvärde för måttavisering v2</span><span class="sxs-lookup"><span data-stu-id="4f44c-855">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="4f44c-856">New-AzMetricAlertRuleV2Criteria: skapar nu även kriterier för dynamiskt tröskelvärde</span><span class="sxs-lookup"><span data-stu-id="4f44c-856">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="4f44c-857">Add-AzMetricAlertRuleV2: accepterar nu även kriterier för dynamiskt tröskelvärde</span><span class="sxs-lookup"><span data-stu-id="4f44c-857">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="4f44c-858">Förbättringar i schemalagd frågeregel (SQR)</span><span class="sxs-lookup"><span data-stu-id="4f44c-858">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="4f44c-859">Cmdletar accepterar ”Location”-parameter i båda formaten, antingen platsen (t.ex. eastus) eller platsens visningsnamn (t.ex. USA, östra)</span><span class="sxs-lookup"><span data-stu-id="4f44c-859">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="4f44c-860">”Enabled”-parametern illustreras korrekt i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="4f44c-860">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="4f44c-861">Exempel för den valfria parametern ”ActionGroup” har lagts till</span><span class="sxs-lookup"><span data-stu-id="4f44c-861">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="4f44c-862">Förbättrade hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="4f44c-862">Overall improved help files</span></span>
* <span data-ttu-id="4f44c-863">Åtgärda bugg då omfattningstypen fastställs för ”Set-AzActionRule”</span><span class="sxs-lookup"><span data-stu-id="4f44c-863">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4f44c-864">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4f44c-864">Az.Network</span></span>
* <span data-ttu-id="4f44c-865">Korrigera felaktigt exempel i referensdokumentationen för ”New-AzApplicationGateway”</span><span class="sxs-lookup"><span data-stu-id="4f44c-865">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="4f44c-866">Lägg till anmärkning i ”Get-AzNetworkWatcherPacketCapture”-referensdokumentationen om hämtning av alla egenskaper för en paketinsamling</span><span class="sxs-lookup"><span data-stu-id="4f44c-866">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="4f44c-867">Exempel har korrigerats i ”Test-AzNetworkWatcherIPFlow”-referensdokumentationen för korrekt uppräkning av nätverkskort</span><span class="sxs-lookup"><span data-stu-id="4f44c-867">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="4f44c-868">Förbättrad tolkning av molnundantag för att visa eventuell ytterligare information</span><span class="sxs-lookup"><span data-stu-id="4f44c-868">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="4f44c-869">Förbättrad tolkning av molnundantag för att hantera ytterligare en typ av SDK-undantag</span><span class="sxs-lookup"><span data-stu-id="4f44c-869">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="4f44c-870">Felaktig mappning av säkerhetsregelmodeller har korrigerats</span><span class="sxs-lookup"><span data-stu-id="4f44c-870">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="4f44c-871">Egenskaper har lagts till för nätverksgränssnittet för funktionen Privat IP</span><span class="sxs-lookup"><span data-stu-id="4f44c-871">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="4f44c-872">Egenskapen ”PrivateEndpoint” har lagts till som en typ av PSResourceId till PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="4f44c-872">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="4f44c-873">Egenskapen ”PrivateLinkConnectionProperties” har lagts till som en typ av PSIpConfigurationConnectivityInformation till PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="4f44c-873">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="4f44c-874">Modellklassen PSIpConfigurationConnectivityInformation har lagts till</span><span class="sxs-lookup"><span data-stu-id="4f44c-874">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="4f44c-875">ApplicationRuleProtocolType ”mssql” har lagts till för Azure Firewall-resurs</span><span class="sxs-lookup"><span data-stu-id="4f44c-875">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="4f44c-876">MultiLink-stöd i virtuellt WAN</span><span class="sxs-lookup"><span data-stu-id="4f44c-876">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="4f44c-877">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="4f44c-877">New cmdlets</span></span>
        - <span data-ttu-id="4f44c-878">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="4f44c-878">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="4f44c-879">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="4f44c-879">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="4f44c-880">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="4f44c-880">Updated cmdlet:</span></span>
        - <span data-ttu-id="4f44c-881">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="4f44c-881">New-VpnSite</span></span>
        - <span data-ttu-id="4f44c-882">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="4f44c-882">Update-VpnSite</span></span>
        - <span data-ttu-id="4f44c-883">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="4f44c-883">New-VpnConnection</span></span>
        - <span data-ttu-id="4f44c-884">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="4f44c-884">Update-VpnConnection</span></span>
* <span data-ttu-id="4f44c-885">Dokument för vissa PowerShell-exempel har korrigerats så att Az-cmdletar används i stället för AzureRM-cmdletar</span><span class="sxs-lookup"><span data-stu-id="4f44c-885">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4f44c-886">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4f44c-886">Az.RecoveryServices</span></span>
* <span data-ttu-id="4f44c-887">Uppdatera AzureVMpolicy-objekt med ProtectedItemsCount-attribut</span><span class="sxs-lookup"><span data-stu-id="4f44c-887">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="4f44c-888">Ytterligare tester har lagts till för VM-princip och återställning av ursprungligt lagringskonto</span><span class="sxs-lookup"><span data-stu-id="4f44c-888">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="4f44c-889">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4f44c-889">Az.Resources</span></span>
* <span data-ttu-id="4f44c-890">Åtgärda fel där det inte gick att anropa New-AzRoleAssignment utan parametern Scope.</span><span class="sxs-lookup"><span data-stu-id="4f44c-890">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="4f44c-891">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4f44c-891">Az.ServiceFabric</span></span>
* <span data-ttu-id="4f44c-892">Stavfel har korrigerats i exempel för ”Update-AzServiceFabricReliability”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="4f44c-892">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="4f44c-893">Lägger till nya cmdletar för att hantera program och tjänster:</span><span class="sxs-lookup"><span data-stu-id="4f44c-893">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="4f44c-894">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="4f44c-894">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="4f44c-895">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="4f44c-895">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="4f44c-896">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="4f44c-896">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="4f44c-897">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="4f44c-897">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="4f44c-898">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="4f44c-898">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="4f44c-899">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="4f44c-899">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="4f44c-900">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="4f44c-900">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="4f44c-901">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="4f44c-901">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="4f44c-902">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="4f44c-902">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="4f44c-903">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="4f44c-903">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="4f44c-904">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="4f44c-904">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="4f44c-905">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="4f44c-905">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="4f44c-906">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="4f44c-906">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="4f44c-907">Service Fabric SDK har uppgraderats till version 1.2.0 som använder Service Fabric-resursprovidern med API-version 2019-03-01.</span><span class="sxs-lookup"><span data-stu-id="4f44c-907">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="4f44c-908">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="4f44c-908">Az.SignalR</span></span>
* <span data-ttu-id="4f44c-909">Lägg till Update-, Restart-, CheckNameAvailability- och GetUsage-cmdletar</span><span class="sxs-lookup"><span data-stu-id="4f44c-909">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="4f44c-910">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4f44c-910">Az.Sql</span></span>
* <span data-ttu-id="4f44c-911">Uppdatera exempel i referensdokumentationen för ”Get-AzSqlElasticPool”</span><span class="sxs-lookup"><span data-stu-id="4f44c-911">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="4f44c-912">vCore-exempel för att skapa en elastisk pool (New-AzSqlElasticPool) har lagts till.</span><span class="sxs-lookup"><span data-stu-id="4f44c-912">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="4f44c-913">Ta bort verifieringen av EmailAddresses och kontrollen som bekräftar att EmailAdmins inte är falskt när EmailAddresses är tomt i Set-AzSqlServerAdvancedThreatProtectionPolicy och Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="4f44c-913">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="4f44c-914">Server-/databasgranskningsinställningar kan tas bort när det finns flera diagnostikinställningar som aktiverar granskningskategorin.</span><span class="sxs-lookup"><span data-stu-id="4f44c-914">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="4f44c-915">Åtgärda verifiering av e-postadresser i flera Sql Vulnerability Assessment-cmdletar (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting och Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="4f44c-915">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4f44c-916">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4f44c-916">Az.Storage</span></span>
* <span data-ttu-id="4f44c-917">Exempel i referensdokumentationen för ”Get-AzStorageAccountKey” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="4f44c-917">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="4f44c-918">Vid upp- och nedladdning av en Azure-fil kan SMB-egenskaperna för källfilen (t.ex. filattribut, tidpunkten då filen skapades och tidpunkten för den senaste skrivningen) sparas i målfilen</span><span class="sxs-lookup"><span data-stu-id="4f44c-918">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="4f44c-919">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="4f44c-919">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="4f44c-920">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="4f44c-920">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="4f44c-921">Korrigera problem med uppladdningen av blockblob med egenskaper/metadata för ImmutabilityPolicy i containrar.</span><span class="sxs-lookup"><span data-stu-id="4f44c-921">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="4f44c-922">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="4f44c-922">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="4f44c-923">Stöd för hantering av Azure-filresurser med API för hanteringsplan</span><span class="sxs-lookup"><span data-stu-id="4f44c-923">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="4f44c-924">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="4f44c-924">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="4f44c-925">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="4f44c-925">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="4f44c-926">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="4f44c-926">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="4f44c-927">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="4f44c-927">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4f44c-928">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4f44c-928">Az.Websites</span></span>
* <span data-ttu-id="4f44c-929">Åtgärdar problemet där webapp-taggar togs bort när appen migrerades till nya ASP</span><span class="sxs-lookup"><span data-stu-id="4f44c-929">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="4f44c-930">Åtgärda Publish-AzureWebapp så att det fungerar i Linux och Windows</span><span class="sxs-lookup"><span data-stu-id="4f44c-930">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="4f44c-931">Uppdatera exempel i ”Get-AzWebAppPublishingProfile”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="4f44c-931">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="4f44c-932">2.6.0 – augusti 2019</span><span class="sxs-lookup"><span data-stu-id="4f44c-932">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="4f44c-933">Allmänt</span><span class="sxs-lookup"><span data-stu-id="4f44c-933">General</span></span>
* <span data-ttu-id="4f44c-934">Åtgärdade diverse skrivfel i flera moduler</span><span class="sxs-lookup"><span data-stu-id="4f44c-934">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="4f44c-935">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4f44c-935">Az.Accounts</span></span>
* <span data-ttu-id="4f44c-936">Stöd för användartilldelat MSI i Azure Functions-autentisering (#9479)</span><span class="sxs-lookup"><span data-stu-id="4f44c-936">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="4f44c-937">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="4f44c-937">Az.Aks</span></span>
* <span data-ttu-id="4f44c-938">Åtgärda problem med utdata för "Get-AzAks"</span><span class="sxs-lookup"><span data-stu-id="4f44c-938">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="4f44c-939">Mer information här: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="4f44c-939">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="4f44c-940">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4f44c-940">Az.ApiManagement</span></span>
* <span data-ttu-id="4f44c-941">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="4f44c-941">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="4f44c-942">Uppdatera .net-NuGet-versionen, som inte tillämpar begränsningar för productId, apiId och userId</span><span class="sxs-lookup"><span data-stu-id="4f44c-942">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="4f44c-943">**Get-AzApiManagementProduct** – Lade till stöd för frågekörning mot produkter via API.</span><span class="sxs-lookup"><span data-stu-id="4f44c-943">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="4f44c-944">**New-AzApiManagementApiRevision** – Korrigering för problem där ApiRevisionDescription inte angavs vid skapande av ny API-revision https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="4f44c-944">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="4f44c-945">Åtgärdade skrivfel i modellen "PsApiManagementOAuth2AuthrozationServer" till "PsApiManagementOAuth2AuthorizationServer"</span><span class="sxs-lookup"><span data-stu-id="4f44c-945">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="4f44c-946">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="4f44c-946">Az.Batch</span></span>
* <span data-ttu-id="4f44c-947">Åtgärdade skrivfel i hjälpmeddelande och dokumentation till att skriva Windows med versaler</span><span class="sxs-lookup"><span data-stu-id="4f44c-947">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="4f44c-948">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="4f44c-948">Az.Cdn</span></span>
* <span data-ttu-id="4f44c-949">Åtgärdade skrivfel i CDN-modulens konverteringshjälp</span><span class="sxs-lookup"><span data-stu-id="4f44c-949">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4f44c-950">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4f44c-950">Az.Compute</span></span>
* <span data-ttu-id="4f44c-951">Lägg till VmssId i New-AzVMConfig-cmdleten</span><span class="sxs-lookup"><span data-stu-id="4f44c-951">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="4f44c-952">Lägg till parametrarna TerminateScheduledEvents och TerminateScheduledEventNotBeforeTimeoutInMinutes i New-AzVmssConfig och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4f44c-952">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="4f44c-953">Lägg till egenskapen HyperVGeneration till avbildningsobjekt för virtuell dator</span><span class="sxs-lookup"><span data-stu-id="4f44c-953">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="4f44c-954">Lägg till funktioner för Host och HostGroup</span><span class="sxs-lookup"><span data-stu-id="4f44c-954">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="4f44c-955">Nya cmdletar:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="4f44c-955">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="4f44c-956">HostId-parametern läggs till i New-AzVMConfig och New-AzVM</span><span class="sxs-lookup"><span data-stu-id="4f44c-956">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="4f44c-957">Uppdatera exempel i "Invoke-AzVMRunCommand"-dokumentationen till att använda rätt parameternamn</span><span class="sxs-lookup"><span data-stu-id="4f44c-957">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="4f44c-958">Uppdatera "-VolumeType"-beskrivningen i referensdokumentationen för "set-AzVMDiskEncryptionExtension" och "set-AzVmssDiskEncryptionExtension"</span><span class="sxs-lookup"><span data-stu-id="4f44c-958">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4f44c-959">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4f44c-959">Az.DataFactory</span></span>
* <span data-ttu-id="4f44c-960">Åtgärda skrivfel till att använda versaler för "Windows" i "New-AzDataFactoryEncryptValue"-dokumentationen</span><span class="sxs-lookup"><span data-stu-id="4f44c-960">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="4f44c-961">Uppdaterade ADF .Net SDK-versionen till 4.1.2</span><span class="sxs-lookup"><span data-stu-id="4f44c-961">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="4f44c-962">Lägg till parametrarna "DataProxyIntegrationRuntimeName", "DataProxyStagingLinkedServiceName" och "DataProxyStagingPath" för "Set-AzureRmDataFactoryV2IntegrationRuntime"-cmd för att aktivera konfiguration av lokalt installerad integrationskörning som en proxy för SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="4f44c-962">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="4f44c-963">Uppdaterade PSTriggerRun till att visa utlöst pipeline, meddelande och egenskaper samt PSActivityRun till att visa aktivitetstypen</span><span class="sxs-lookup"><span data-stu-id="4f44c-963">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4f44c-964">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4f44c-964">Az.DataLakeStore</span></span>
* <span data-ttu-id="4f44c-965">Korrigering av frysning av Get-DataLakeStoreDeletedItem för fel eller fjärrundantag.</span><span class="sxs-lookup"><span data-stu-id="4f44c-965">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="4f44c-966">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="4f44c-966">Az.EventHub</span></span>
* <span data-ttu-id="4f44c-967">Korrigering av problem #9658 : Skrivfel i parametern VirtualNteworkRule i Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="4f44c-967">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="4f44c-968">Korrigering av problem #9558 : Set-AzEventHubNamespace använder PATCH i stället för PUT</span><span class="sxs-lookup"><span data-stu-id="4f44c-968">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="4f44c-969">lade till parametern EnableKafka i Set-AzEventHubNamespace-cmdleten</span><span class="sxs-lookup"><span data-stu-id="4f44c-969">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="4f44c-970">Korrigering av problem #9786 : kan inte skapa en regel med Endast lyssna-behörighet</span><span class="sxs-lookup"><span data-stu-id="4f44c-970">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="4f44c-971">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="4f44c-971">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="4f44c-972">Åtgärdade skrivfel i dokumentation där "Azure" skrevs helt med gemener</span><span class="sxs-lookup"><span data-stu-id="4f44c-972">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4f44c-973">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4f44c-973">Az.Monitor</span></span>
* <span data-ttu-id="4f44c-974">Åtgärdade felaktigt parameternamn i hjälpdokumentationen</span><span class="sxs-lookup"><span data-stu-id="4f44c-974">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4f44c-975">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4f44c-975">Az.Network</span></span>
* <span data-ttu-id="4f44c-976">Uppdaterade New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="4f44c-976">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="4f44c-977">Gjorde parametern "PublicIpAddress" inaktuell eftersom den aldrig används på serversidan.</span><span class="sxs-lookup"><span data-stu-id="4f44c-977">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="4f44c-978">Lade till den valfria parametern "Primary", som anger huruvida den aktuella IP-konfigurationen är den primära.</span><span class="sxs-lookup"><span data-stu-id="4f44c-978">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="4f44c-979">Förbättrade hanteringen av felundantag för begärande från SDK – åtgärdar problemet att tidigare SDK-undantag inte hanteras på rätt sätt, vilket leder till att viktig felinformation inte visas</span><span class="sxs-lookup"><span data-stu-id="4f44c-979">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="4f44c-980">Justerade valideringslogiken för IPv6-IP-prefix till att kontrollera korrekt IPv6-prefixlängd.</span><span class="sxs-lookup"><span data-stu-id="4f44c-980">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="4f44c-981">Uppdaterade Get-AzVirtualNetworkSubnetConfig: Lade till parameter som anges till get av undernätets resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="4f44c-981">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="4f44c-982">Uppdaterade beskrivningen av parametern Location för AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="4f44c-982">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="4f44c-983">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="4f44c-983">Az.OperationalInsights</span></span>
* <span data-ttu-id="4f44c-984">Uppdaterade dokumentation för "New-AzOperationalInsightsLinuxSyslogDataSource"</span><span class="sxs-lookup"><span data-stu-id="4f44c-984">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="4f44c-985">Lade till exempel</span><span class="sxs-lookup"><span data-stu-id="4f44c-985">Added example</span></span>
    - <span data-ttu-id="4f44c-986">Uppdaterade beskrivningen av parametern "-Name"</span><span class="sxs-lookup"><span data-stu-id="4f44c-986">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="4f44c-987">Lade till ett exempel för New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="4f44c-987">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="4f44c-988">Ändrade beskrivningen av parametern -Name för New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="4f44c-988">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4f44c-989">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4f44c-989">Az.RecoveryServices</span></span>
* <span data-ttu-id="4f44c-990">Uppdatera "Get-AzRecoveryServicesBackupJobDetail.md"</span><span class="sxs-lookup"><span data-stu-id="4f44c-990">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="4f44c-991">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4f44c-991">Az.Resources</span></span>
* <span data-ttu-id="4f44c-992">Lägg till stöd för den nya API-versionen från 2019-05-10 för Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="4f44c-992">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="4f44c-993">Lägg till stöd för "copy.count = 0" för variabler, resurser och egenskaper</span><span class="sxs-lookup"><span data-stu-id="4f44c-993">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="4f44c-994">Resurser med "condition = false" eller "copy.count = 0" tas bort i complete-läget</span><span class="sxs-lookup"><span data-stu-id="4f44c-994">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="4f44c-995">Lägg till ett exempel på tilldelning av princip på prenumerationsnivå i hjälpdokumentationen</span><span class="sxs-lookup"><span data-stu-id="4f44c-995">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="4f44c-996">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="4f44c-996">Az.ServiceBus</span></span>
* <span data-ttu-id="4f44c-997">Korrigering av problem #9658 : Skrivfel i parametern VirtualNetworkRule i set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="4f44c-997">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="4f44c-998">Korrigering av problem #9786 : kan inte skapa en regel med Endast lyssna-behörighet</span><span class="sxs-lookup"><span data-stu-id="4f44c-998">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="4f44c-999">Lade till det nya kommandot "Test-AzServiceBusNameAvailability" för att kontrollera namntillgängligheten för kö och ämne</span><span class="sxs-lookup"><span data-stu-id="4f44c-999">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="4f44c-1000">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4f44c-1000">Az.ServiceFabric</span></span>
* <span data-ttu-id="4f44c-1001">Åtgärda buggar med tillägg av nodtyps-cmdlet:</span><span class="sxs-lookup"><span data-stu-id="4f44c-1001">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="4f44c-1002">NullReferenceException-bugg när resursgrupp hade annan vmss som inte är relaterad till Service Fabric-klustret.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1002">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="4f44c-1003">Åtgärdar problemet: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="4f44c-1003">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="4f44c-1004">Åtgärda bugg där cmdleten misslyckades om virtualNetwork var i en annan resursgrupp än klustret.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1004">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="4f44c-1005">Åtgärdar problemet: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="4f44c-1005">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="4f44c-1006">AzServiceFabricApplicationCertificate-cmdleten görs inaktuell</span><span class="sxs-lookup"><span data-stu-id="4f44c-1006">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="4f44c-1007">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4f44c-1007">Az.Sql</span></span>
* <span data-ttu-id="4f44c-1008">Uppdatera dokumentation om gamla gransknings-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1008">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4f44c-1009">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4f44c-1009">Az.Storage</span></span>
* <span data-ttu-id="4f44c-1010">Uppdatera hjälpen för Get/Close-AzStorageFileHandle genom att lägga till fler scenarier i cmdlet-exempel och uppdatera parameterbeskrivningar</span><span class="sxs-lookup"><span data-stu-id="4f44c-1010">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="4f44c-1011">Stöd för StandardBlobTier i uppladdningsblob och kopieringsblob</span><span class="sxs-lookup"><span data-stu-id="4f44c-1011">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="4f44c-1012">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="4f44c-1012">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="4f44c-1013">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="4f44c-1013">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="4f44c-1014">Stöd för rehydratiseringsprioritet i kopieringsblob</span><span class="sxs-lookup"><span data-stu-id="4f44c-1014">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="4f44c-1015">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="4f44c-1015">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4f44c-1016">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4f44c-1016">Az.Websites</span></span>
* <span data-ttu-id="4f44c-1017">Lägg till klargöranden gällande parametern -AppSettings i Set-AzWebApp och Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4f44c-1017">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="4f44c-1018">2.5.0 – July 2019</span><span class="sxs-lookup"><span data-stu-id="4f44c-1018">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4f44c-1019">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4f44c-1019">Az.Accounts</span></span>
* <span data-ttu-id="4f44c-1020">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="4f44c-1020">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="4f44c-1021">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="4f44c-1021">Az.ApplicationInsights</span></span>
* <span data-ttu-id="4f44c-1022">Korrigera skrivfel i exempel i dokumentationen för Remove-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="4f44c-1022">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4f44c-1023">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4f44c-1023">Az.Automation</span></span>
* <span data-ttu-id="4f44c-1024">Korrigera skrivfel i resurssträng</span><span class="sxs-lookup"><span data-stu-id="4f44c-1024">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="4f44c-1025">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="4f44c-1025">Az.CognitiveServices</span></span>
* <span data-ttu-id="4f44c-1026">Stöd för NetworkRuleSet har lagts till.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1026">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4f44c-1027">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4f44c-1027">Az.Compute</span></span>
* <span data-ttu-id="4f44c-1028">Lägg till saknade egenskaper (ComputerName, OsName, OsVersion och HyperVGeneration) för visningsobjekt i den virtuella datorinstansen.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1028">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="4f44c-1029">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="4f44c-1029">Az.ContainerRegistry</span></span>
* <span data-ttu-id="4f44c-1030">Åtgärda skrivfel i Remove-AzContainerRegistryReplication för parametern Replication</span><span class="sxs-lookup"><span data-stu-id="4f44c-1030">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="4f44c-1031">Mer information finns här: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="4f44c-1031">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4f44c-1032">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4f44c-1032">Az.DataFactory</span></span>
* <span data-ttu-id="4f44c-1033">ADF .Net SDK-versionen har uppdaterats till 4.1.0</span><span class="sxs-lookup"><span data-stu-id="4f44c-1033">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="4f44c-1034">Korrigera skrivfel i dokumentationen för Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="4f44c-1034">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="4f44c-1035">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="4f44c-1035">Az.EventHub</span></span>
* <span data-ttu-id="4f44c-1036">Ny cmmdlet har lagts till för att skapa SAS-token: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="4f44c-1036">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="4f44c-1037">verifierings- och felmeddelande har lagts till för authorizationrules-rättigheter om endast "hantera" har tilldelats</span><span class="sxs-lookup"><span data-stu-id="4f44c-1037">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="4f44c-1038">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4f44c-1038">Az.KeyVault</span></span>
* <span data-ttu-id="4f44c-1039">Stöd har lagts till för att ange KeySize för certifikatprinciper</span><span class="sxs-lookup"><span data-stu-id="4f44c-1039">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="4f44c-1040">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="4f44c-1040">Az.LogicApp</span></span>
* <span data-ttu-id="4f44c-1041">Korrigering för Get-AzIntegrationAccountMap för att lista alla mappningstyper</span><span class="sxs-lookup"><span data-stu-id="4f44c-1041">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="4f44c-1042">Ny MapType-parameter har lagts till för filtrering</span><span class="sxs-lookup"><span data-stu-id="4f44c-1042">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="4f44c-1043">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="4f44c-1043">Az.ManagedServices</span></span>
* <span data-ttu-id="4f44c-1044">Stöd för API-versionen 2019-06-01 (GA) har lagts till</span><span class="sxs-lookup"><span data-stu-id="4f44c-1044">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4f44c-1045">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4f44c-1045">Az.Network</span></span>
* <span data-ttu-id="4f44c-1046">Lägg till stöd för privat slutpunkt och privat länktjänst</span><span class="sxs-lookup"><span data-stu-id="4f44c-1046">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="4f44c-1047">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="4f44c-1047">New cmdlets</span></span>
        - <span data-ttu-id="4f44c-1048">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="4f44c-1048">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="4f44c-1049">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="4f44c-1049">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="4f44c-1050">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4f44c-1050">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="4f44c-1051">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4f44c-1051">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="4f44c-1052">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4f44c-1052">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="4f44c-1053">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4f44c-1053">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="4f44c-1054">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="4f44c-1054">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="4f44c-1055">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="4f44c-1055">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="4f44c-1056">Nedanstående kommandon för funktionen har uppdaterats: Flaggan PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies på undernätet i VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4f44c-1056">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="4f44c-1057">Uppdaterade New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="4f44c-1057">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="4f44c-1058">Valfri parameter har lagts till – PrivateEndpointNetworkPoliciesFlag som konfigurerar huruvida nätverksprinciper ska tillämpas på en privat slutpunkt i det här undernätet.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1058">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="4f44c-1059">Valfri parameter har lagts till – PrivateLinkServiceNetworkPoliciesFlag som konfigurerar huruvida nätverksprinciper ska tillämpas på en privat länktjänst i det här undernätet.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1059">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="4f44c-1060">AzPrivateLinkService för cmdlet-parametern ServiceName har bytt namn till Name med aliaset ServiceName för bakåtkompatibilitet</span><span class="sxs-lookup"><span data-stu-id="4f44c-1060">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="4f44c-1061">Aktivera ICMP-protokoll för konfiguration av nätverkssäkerhetsregler</span><span class="sxs-lookup"><span data-stu-id="4f44c-1061">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="4f44c-1062">Uppdaterade cmdletar</span><span class="sxs-lookup"><span data-stu-id="4f44c-1062">Updated cmdlets</span></span>
        - <span data-ttu-id="4f44c-1063">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4f44c-1063">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="4f44c-1064">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4f44c-1064">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="4f44c-1065">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4f44c-1065">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="4f44c-1066">Lägg till ConnectionProtocolType (Ikev1/Ikev2) som en konfigurerbar parameter för New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="4f44c-1066">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="4f44c-1067">Lägg till PrivateIpAddressVersion i LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="4f44c-1067">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="4f44c-1068">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="4f44c-1068">Updated cmdlet:</span></span>
        - <span data-ttu-id="4f44c-1069">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="4f44c-1069">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="4f44c-1070">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="4f44c-1070">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="4f44c-1071">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="4f44c-1071">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="4f44c-1072">Uppdatering av Application Gateway-kommandot New-AzApplicationGatewayProbeConfig för stöd av anpassad port i Probe</span><span class="sxs-lookup"><span data-stu-id="4f44c-1072">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="4f44c-1073">Uppdaterade New-AzApplicationGatewayProbeConfig: Den valfria parametern Port som används för avsökning i serverdelen har lagts till.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1073">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="4f44c-1074">Denna parameter gäller för SKU:erna Standard_V2 och WAF_V2.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1074">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="4f44c-1075">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="4f44c-1075">Az.OperationalInsights</span></span>
* <span data-ttu-id="4f44c-1076">Uppdaterade standardversionen för sparade sökningar till 1.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1076">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="4f44c-1077">Åtgärdade hantering av anpassad log null regex</span><span class="sxs-lookup"><span data-stu-id="4f44c-1077">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4f44c-1078">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4f44c-1078">Az.RecoveryServices</span></span>
* <span data-ttu-id="4f44c-1079">Uppdatera Get-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="4f44c-1079">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="4f44c-1080">Uppdatera Get-AzRecoveryServicesBackupContainer.md</span><span class="sxs-lookup"><span data-stu-id="4f44c-1080">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="4f44c-1081">Uppdatera Get-AzRecoveryServicesVault.md</span><span class="sxs-lookup"><span data-stu-id="4f44c-1081">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="4f44c-1082">Uppdatera Wait-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="4f44c-1082">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="4f44c-1083">Uppdatera Set-AzRecoveryServicesVaultContext.md</span><span class="sxs-lookup"><span data-stu-id="4f44c-1083">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="4f44c-1084">Uppdatera Get-AzRecoveryServicesBackupItem.md</span><span class="sxs-lookup"><span data-stu-id="4f44c-1084">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="4f44c-1085">Uppdatera Get-AzRecoveryServicesBackupRecoveryPoint.md</span><span class="sxs-lookup"><span data-stu-id="4f44c-1085">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="4f44c-1086">Uppdatera Restore-AzRecoveryServicesBackupItem.md</span><span class="sxs-lookup"><span data-stu-id="4f44c-1086">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="4f44c-1087">Uppdaterat tjänstanrop för avregistrering av container för Azure-filresurs</span><span class="sxs-lookup"><span data-stu-id="4f44c-1087">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="4f44c-1088">Uppdatera Set-AzRecoveryServicesAsrAlertSetting.md</span><span class="sxs-lookup"><span data-stu-id="4f44c-1088">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="4f44c-1089">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4f44c-1089">Az.Resources</span></span>
- <span data-ttu-id="4f44c-1090">Ta bort den cmdlet som saknas och som refereras i dokumentationen till New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4f44c-1090">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="4f44c-1091">Princip-cmdletar har uppdaterats så att de använder den nya API-versionen 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="4f44c-1091">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="4f44c-1092">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="4f44c-1092">Az.ServiceBus</span></span>
* <span data-ttu-id="4f44c-1093">Ny cmmdlet har lagts till för att skapa SAS-token: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="4f44c-1093">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="4f44c-1094">verifierings- och felmeddelande har lagts till för authorizationrules-rättigheter om endast "hantera" har tilldelats</span><span class="sxs-lookup"><span data-stu-id="4f44c-1094">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="4f44c-1095">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4f44c-1095">Az.Sql</span></span>
* <span data-ttu-id="4f44c-1096">Åtgärda saknade exempel för Set-AzSqlDatabaseSecondary cmdlet</span><span class="sxs-lookup"><span data-stu-id="4f44c-1096">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="4f44c-1097">Åtgärda angivna återkommande genomsökningar för bedömning av säkerhetsrisk utan angivna e-postadresser</span><span class="sxs-lookup"><span data-stu-id="4f44c-1097">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="4f44c-1098">Korrigera ett skrivfel i ett varningsmeddelande.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1098">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4f44c-1099">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4f44c-1099">Az.Storage</span></span>
* <span data-ttu-id="4f44c-1100">Uppdatera exempel i referensdokumentationen för Get-AzStorageAccount så att rätt parameternamn används</span><span class="sxs-lookup"><span data-stu-id="4f44c-1100">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="4f44c-1101">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="4f44c-1101">Az.StorageSync</span></span>
* <span data-ttu-id="4f44c-1102">Lägger till cmdleten Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1102">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="4f44c-1103">Åtgärda problem 9551 så att TierFilesOlderThanDays föredras</span><span class="sxs-lookup"><span data-stu-id="4f44c-1103">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4f44c-1104">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4f44c-1104">Az.Websites</span></span>
* <span data-ttu-id="4f44c-1105">Åtgärdar ett fel där vissa SiteConfig-egenskaper inte returnerades av Get-AzWebApp och Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="4f44c-1105">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="4f44c-1106">Lägger till en ny platsparameter för Get-AzDeletedWebApp och Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="4f44c-1106">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="4f44c-1107">Åtgärdar ett fel i kloning av webbapp-platser som använder New-AzWebApp-IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="4f44c-1107">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="4f44c-1108">2.4.0 – juli 2019</span><span class="sxs-lookup"><span data-stu-id="4f44c-1108">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4f44c-1109">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4f44c-1109">Az.Accounts</span></span>
* <span data-ttu-id="4f44c-1110">Lägg till stöd för profil-cmdletar</span><span class="sxs-lookup"><span data-stu-id="4f44c-1110">Add support for profile cmdlets</span></span>
* <span data-ttu-id="4f44c-1111">Lägg till stöd för miljöer och dataplaner i genererade cmdletar</span><span class="sxs-lookup"><span data-stu-id="4f44c-1111">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="4f44c-1112">Åtgärda bugg där fel slutpunkt i vissa fall användes för cmdletar för dataplaner i Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="4f44c-1112">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="4f44c-1113">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="4f44c-1113">Az.Advisor</span></span>
* <span data-ttu-id="4f44c-1114">GA-version av Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="4f44c-1114">GA release of Az.Advisor</span></span>
* <span data-ttu-id="4f44c-1115">Den här modulen ingår nu som en del av `Az`-sammanslagningsmodulen</span><span class="sxs-lookup"><span data-stu-id="4f44c-1115">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="4f44c-1116">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4f44c-1116">Az.ApiManagement</span></span>
* <span data-ttu-id="4f44c-1117">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="4f44c-1117">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="4f44c-1118">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="4f44c-1118">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="4f44c-1119">Stöd för att fråga prenumerationer efter användare och produkt har lagts till</span><span class="sxs-lookup"><span data-stu-id="4f44c-1119">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="4f44c-1120">Stöd för att fråga med hjälp av omfång ”/”, ”/apis”, ”/apis/echo-api” har lagts till</span><span class="sxs-lookup"><span data-stu-id="4f44c-1120">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="4f44c-1121">Korrigering av problem https://github.com/Azure/azure-powershell/issues/9307 och https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="4f44c-1121">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="4f44c-1122">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="4f44c-1122">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="4f44c-1123">Stöd för att ange ”ApiVersion” och ”ApiVersionSetId” när API:er importeras har lagts till</span><span class="sxs-lookup"><span data-stu-id="4f44c-1123">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4f44c-1124">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4f44c-1124">Az.Automation</span></span>
* <span data-ttu-id="4f44c-1125">Bugg med cmdleten Set-AzAutomationConnectionFieldValue för att hantera strängvärde har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1125">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4f44c-1126">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4f44c-1126">Az.Compute</span></span>
* <span data-ttu-id="4f44c-1127">Lägg till parametern HyperVGeneration i New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="4f44c-1127">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4f44c-1128">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4f44c-1128">Az.DataFactory</span></span>
* <span data-ttu-id="4f44c-1129">Uppdaterar utdata från ADF-cmdletar som hämtar aktivitetskörningar, hämtar pipelinekörningar och hämtar utlösarkörningar för stöd för Select-Object-pipe.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1129">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="4f44c-1130">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="4f44c-1130">Az.EventGrid</span></span>
* <span data-ttu-id="4f44c-1131">Korrigera stavfel i dokumentation om ”New-AzEventGridSubscription”</span><span class="sxs-lookup"><span data-stu-id="4f44c-1131">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="4f44c-1132">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="4f44c-1132">Az.IotHub</span></span>
* <span data-ttu-id="4f44c-1133">Lägg till stöd för att återskapa principnycklar för auktorisering.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1133">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4f44c-1134">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4f44c-1134">Az.Network</span></span>
* <span data-ttu-id="4f44c-1135">”RoutingPreference” har lagts till i offentliga IP-taggar</span><span class="sxs-lookup"><span data-stu-id="4f44c-1135">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="4f44c-1136">Förbättra exempel för referensdokumentation om ”Get-AzNetworkServiceTag”</span><span class="sxs-lookup"><span data-stu-id="4f44c-1136">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="4f44c-1137">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="4f44c-1137">Az.PolicyInsights</span></span>
* <span data-ttu-id="4f44c-1138">Åtgärda problem med null-referens i Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="4f44c-1138">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="4f44c-1139">Mer information här: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="4f44c-1139">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="4f44c-1140">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="4f44c-1140">Az.OperationalInsights</span></span>
* <span data-ttu-id="4f44c-1141">Modellen för CustomLog-datakälla som returneras i Get-AzOperationalInsightsDataSource har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="4f44c-1141">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4f44c-1142">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4f44c-1142">Az.RecoveryServices</span></span>
* <span data-ttu-id="4f44c-1143">Kommandot get-policy för IaaSVM:er har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="4f44c-1143">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="4f44c-1144">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4f44c-1144">Az.Resources</span></span>
    - <span data-ttu-id="4f44c-1145">Korrigera hjälptext för den översta parametern i Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="4f44c-1145">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="4f44c-1146">Lägg till växlingsstöd på klientsidan för Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="4f44c-1146">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="4f44c-1147">Lägg till nya parametrar för Set-AzPolicyAssignment, -PolicyParameters och -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="4f44c-1147">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="4f44c-1148">En mängd dokument- och exempeluppdateringar för Policy-cmdletar</span><span class="sxs-lookup"><span data-stu-id="4f44c-1148">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="4f44c-1149">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="4f44c-1149">Az.ServiceBus</span></span>
* <span data-ttu-id="4f44c-1150">Korrigering av problem #4938 – New-AzureRmServiceBusQueue returnerar BadRequest vid konfiguration av MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="4f44c-1150">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="4f44c-1151">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4f44c-1151">Az.Sql</span></span>
* <span data-ttu-id="4f44c-1152">Lägg till cmdletar för instansredundansgrupper från förhandsversion till offentlig version</span><span class="sxs-lookup"><span data-stu-id="4f44c-1152">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="4f44c-1153">Stöd för granskning för Azure SQL Server\Database med nya cmdletar.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1153">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="4f44c-1154">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="4f44c-1154">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="4f44c-1155">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="4f44c-1155">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="4f44c-1156">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="4f44c-1156">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="4f44c-1157">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="4f44c-1157">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="4f44c-1158">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="4f44c-1158">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="4f44c-1159">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="4f44c-1159">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="4f44c-1160">Ta bort begränsningar för e-post från inställningarna för sårbarhetsbedömning</span><span class="sxs-lookup"><span data-stu-id="4f44c-1160">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4f44c-1161">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4f44c-1161">Az.Storage</span></span>
* <span data-ttu-id="4f44c-1162">Ändra två parametrar ”-IndexDocument” och ”-ErrorDocument404Path” från ”krävs” till ”valfri” i cmdlet:</span><span class="sxs-lookup"><span data-stu-id="4f44c-1162">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="4f44c-1163">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="4f44c-1163">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="4f44c-1164">Uppdatera hjälpen för Get-AzStorageBlobContent genom att lägga till ett exempel</span><span class="sxs-lookup"><span data-stu-id="4f44c-1164">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="4f44c-1165">Visa mer felinformation när cmdleten misslyckas med StorageException</span><span class="sxs-lookup"><span data-stu-id="4f44c-1165">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="4f44c-1166">Stöd för att skapa eller uppdatera lagringskonto med Azure Files AAD DS-autentisering</span><span class="sxs-lookup"><span data-stu-id="4f44c-1166">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="4f44c-1167">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4f44c-1167">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="4f44c-1168">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4f44c-1168">Set-AzStorageAccount</span></span>
* <span data-ttu-id="4f44c-1169">Stöd för att lista eller stänga filreferenser för en filresurs, filkatalog eller en fil</span><span class="sxs-lookup"><span data-stu-id="4f44c-1169">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="4f44c-1170">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="4f44c-1170">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="4f44c-1171">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="4f44c-1171">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="4f44c-1172">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="4f44c-1172">Az.StorageSync</span></span>
* <span data-ttu-id="4f44c-1173">Den här modulen ingår nu som en del av `Az`-sammanslagningsmodulen</span><span class="sxs-lookup"><span data-stu-id="4f44c-1173">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="4f44c-1174">2.3.2 – juni 2019</span><span class="sxs-lookup"><span data-stu-id="4f44c-1174">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4f44c-1175">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4f44c-1175">Az.Accounts</span></span>
* <span data-ttu-id="4f44c-1176">Åtgärda bugg med felaktiga webbadresser som i vissa fall användes för Functions-anrop</span><span class="sxs-lookup"><span data-stu-id="4f44c-1176">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="4f44c-1177">Mer information här: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="4f44c-1177">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="4f44c-1178">Åtgärda problem med alias från AzureRM i Az-cmdletar</span><span class="sxs-lookup"><span data-stu-id="4f44c-1178">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="4f44c-1179">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="4f44c-1179">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="4f44c-1180">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="4f44c-1180">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4f44c-1181">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4f44c-1181">Az.Compute</span></span>
* <span data-ttu-id="4f44c-1182">Parameteruppsättningarna New-AzVm och New-AzVmss accepterar nu parametern ”ProximityPlacementGroup”.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1182">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="4f44c-1183">Stavfel i referensdokumentationen för ”New-AzVM” har korrigerats</span><span class="sxs-lookup"><span data-stu-id="4f44c-1183">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="4f44c-1184">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="4f44c-1184">Az.Dns</span></span>
* <span data-ttu-id="4f44c-1185">Stavfel i hjälpexempel för ”Set-AzDnsZone” har korrigerats.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1185">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="4f44c-1186">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="4f44c-1186">Az.EventGrid</span></span>
* <span data-ttu-id="4f44c-1187">Har uppdaterats för att använda API-versionen 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1187">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="4f44c-1188">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="4f44c-1188">New cmdlets:</span></span>
    - <span data-ttu-id="4f44c-1189">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="4f44c-1189">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="4f44c-1190">Skapar en ny Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1190">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="4f44c-1191">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="4f44c-1191">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="4f44c-1192">Hämtar information om en Event Grid-domän eller hämtar en lista med alla Event Grid-domäner i den aktuella Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1192">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="4f44c-1193">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="4f44c-1193">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="4f44c-1194">Tar bort en Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1194">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="4f44c-1195">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="4f44c-1195">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="4f44c-1196">Återskapar nyckeln för delad åtkomst för en Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1196">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="4f44c-1197">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="4f44c-1197">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="4f44c-1198">Hämtar de nycklar för delad åtkomst som används för att publicera händelser till en Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1198">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="4f44c-1199">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="4f44c-1199">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="4f44c-1200">Skapar ett nytt Azure Event Grid-domänämne.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1200">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="4f44c-1201">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="4f44c-1201">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="4f44c-1202">Hämtar information om ett Event Grid-domänämne eller hämtar en lista med alla Event Grid-domänämnen under en specifik Event Grid-domän i nuvarande Azure</span><span class="sxs-lookup"><span data-stu-id="4f44c-1202">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="4f44c-1203">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="4f44c-1203">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="4f44c-1204">Tar bort ett befintligt Azure Event Grid-domänämne.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1204">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="4f44c-1205">Uppdaterade cmdletar:</span><span class="sxs-lookup"><span data-stu-id="4f44c-1205">Updated cmdlets:</span></span>
    - <span data-ttu-id="4f44c-1206">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="4f44c-1206">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="4f44c-1207">Lägg till nya obligatoriska parametrar för att stödja piping för den nya Event Grid-domänen och Event Grid-domänämnet för att göra det möjligt att skapa nya händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1207">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="4f44c-1208">Lägg till nya obligatoriska parametrar för att ange det nya Event Grid-domännamnet och/eller namnet på Event Grid-domänämnet för att göra det möjligt att skapa nya händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1208">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="4f44c-1209">Lägg till ny parameteruppsättningar för domäner och domänämnen för att göra det möjligt att återanvända befintliga parametrar (t.ex. EndPointType, SubjectBeginsWith osv).</span><span class="sxs-lookup"><span data-stu-id="4f44c-1209">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="4f44c-1210">Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="4f44c-1210">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="4f44c-1211">Förfallodatum för händelseprenumeration</span><span class="sxs-lookup"><span data-stu-id="4f44c-1211">Event subscription expiration date,</span></span>
            - <span data-ttu-id="4f44c-1212">Avancerade filterparametrar.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1212">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="4f44c-1213">Lägg till ny uppräkning för servicebusqueue som mål.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1213">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="4f44c-1214">Tillåt inte användning av ”Alla” i alternativet -IncludedEventType och ersätt det med</span><span class="sxs-lookup"><span data-stu-id="4f44c-1214">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="4f44c-1215">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="4f44c-1215">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="4f44c-1216">Lägg till ny valfria parametrar (Top, ODataQuery och NextLink) för att stödja sidnumrering och filtrering av resultat.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1216">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="4f44c-1217">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="4f44c-1217">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="4f44c-1218">Lägg till nya obligatoriska parametrar för att stödja piping för en Event Grid-domän och Event Grid-domänämnen för att göra det möjligt att ta bort befintliga händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1218">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="4f44c-1219">Lägg till nya obligatoriska parametrar för att ange Event Grid-domännamnet och/eller namnet på Event Grid-domänämnet för att göra det möjligt att ta bort befintliga händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1219">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="4f44c-1220">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="4f44c-1220">Az.FrontDoor</span></span>
* <span data-ttu-id="4f44c-1221">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="4f44c-1221">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="4f44c-1222">Lägg till stöd för transformeringar och nytt värde för automatisk komplettering för operatorer (RegEx)</span><span class="sxs-lookup"><span data-stu-id="4f44c-1222">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="4f44c-1223">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="4f44c-1223">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="4f44c-1224">Lägg till nya värden för automatisk komplettering</span><span class="sxs-lookup"><span data-stu-id="4f44c-1224">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4f44c-1225">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4f44c-1225">Az.Network</span></span>
* <span data-ttu-id="4f44c-1226">Lägg till stöd för resurs för virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="4f44c-1226">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="4f44c-1227">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="4f44c-1227">New cmdlets</span></span>
        - <span data-ttu-id="4f44c-1228">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="4f44c-1228">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="4f44c-1229">Lägg till AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="4f44c-1229">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="4f44c-1230">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="4f44c-1230">New cmdlets</span></span>
        - <span data-ttu-id="4f44c-1231">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="4f44c-1231">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="4f44c-1232">Lägg till PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="4f44c-1232">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="4f44c-1233">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="4f44c-1233">New cmdlets</span></span>
        - <span data-ttu-id="4f44c-1234">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="4f44c-1234">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="4f44c-1235">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="4f44c-1235">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="4f44c-1236">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="4f44c-1236">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="4f44c-1237">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="4f44c-1237">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="4f44c-1238">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4f44c-1238">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="4f44c-1239">Lägg till PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="4f44c-1239">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="4f44c-1240">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="4f44c-1240">New cmdlets</span></span>
        - <span data-ttu-id="4f44c-1241">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="4f44c-1241">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="4f44c-1242">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="4f44c-1242">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="4f44c-1243">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="4f44c-1243">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="4f44c-1244">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="4f44c-1244">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="4f44c-1245">Nedanstående kommandon för funktionen har uppdaterats: Flaggan UseLocalAzureIpAddress på VpnConnection</span><span class="sxs-lookup"><span data-stu-id="4f44c-1245">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="4f44c-1246">New-AzVpnConnection har uppdaterats: Den valfria parametern -UseLocalAzureIpAddress har lagts till för att visa att en lokal IP-adress i Azure ska användas som källadress när anslutningen initieras.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1246">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="4f44c-1247">Set-AzVpnConnection har uppdaterats: Den valfria parametern -UseLocalAzureIpAddress har lagts till för att visa att en lokal IP-adress i Azure ska användas som källadress när anslutningen initieras.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1247">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="4f44c-1248">Det skrivskyddade fältet PeeredConnections har lagts till i ExpressRoute-peering.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1248">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="4f44c-1249">Det skrivskyddade fältet GlobalReachEnabled har lagts till i ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1249">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="4f44c-1250">Ett attribut för icke-bakåtkompatibla ändringar har lagts till för att lyfta fram utfasning av fältet AllowGlobalReach i modellen ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4f44c-1250">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="4f44c-1251">Problem 8756 har åtgärdats: Fel vid användning av TargetListenerID med AzApplicationGatewayRedirectConfiguration-cmdletar</span><span class="sxs-lookup"><span data-stu-id="4f44c-1251">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="4f44c-1252">En bugg i New-AzApplicationGatewayPathRuleConfig som gjorde att regeluppsättningen för att återskapa inte kunde anges har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1252">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="4f44c-1253">Visningen av VirtualNetworkTaps i NetworkInterfaceIpConfiguration har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="4f44c-1253">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="4f44c-1254">Cortex Get-cmdletar för att visa en lista med alla delar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="4f44c-1254">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="4f44c-1255">Funktionen för att skapa VirtualHub-referenser för ExpressRouteGateways och VpnGateway har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="4f44c-1255">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="4f44c-1256">Stöd för tillgänglighetszoner i AzureFirewall och NatGateway har lagts till</span><span class="sxs-lookup"><span data-stu-id="4f44c-1256">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="4f44c-1257">Cmdleten Get-AzNetworkServiceTag har lagts till</span><span class="sxs-lookup"><span data-stu-id="4f44c-1257">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="4f44c-1258">Lägg till stöd för flera offentliga IP-adresser för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="4f44c-1258">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="4f44c-1259">Cmdleten New-AzFirewall har uppdaterats:</span><span class="sxs-lookup"><span data-stu-id="4f44c-1259">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="4f44c-1260">Parametern -PublicIpAddress som accepterar ett eller flera offentliga IP-adressobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="4f44c-1260">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="4f44c-1261">Parametern -VirtualNetwork som accepterar ett virtuellt nätverksobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="4f44c-1261">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="4f44c-1262">Metoderna AddPublicIpAddress och RemovePublicIpAddress har lagts till på brandväggsobjekt – dessa accepterar ett offentligt IP-adressobjekt som indata</span><span class="sxs-lookup"><span data-stu-id="4f44c-1262">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="4f44c-1263">Inaktuella parametrar -PublicIpName och -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="4f44c-1263">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="4f44c-1264">Nedanstående kommandon för funktionen har uppdaterats: Ange autentiseringsalternativ för VpnClient AAD till resurser för virtuella nätverksgatewayer.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1264">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="4f44c-1265">New-AzVirtualNetworkGateway har uppdaterats: De valfria parametrarna AadTenantUri, AadAudienceId och AadIssuerUri för att ange VpnClient AAD-autentiseringsalternativ på en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1265">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="4f44c-1266">Set-AzVirtualNetworkGateway har uppdaterats: De valfria parametrarna AadTenantUri, AadAudienceId och AadIssuerUri för att ange VpnClient AAD-autentiseringsalternativ på en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1266">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="4f44c-1267">Set-AzVirtualNetworkGateway har uppdaterats: Den valfria växelparametern RemoveAadAuthentication som tar bort VpnClient AAD-autentiseringsalternativ från en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1267">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="4f44c-1268">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="4f44c-1268">Az.OperationalInsights</span></span>
* <span data-ttu-id="4f44c-1269">Aktivera prisnivån **pergb2018** i kommandot ”New-AzureRmOperationalInsightsWorkspace”</span><span class="sxs-lookup"><span data-stu-id="4f44c-1269">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="4f44c-1270">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4f44c-1270">Az.Resources</span></span>
* <span data-ttu-id="4f44c-1271">Stöd för ytterligare alternativ för att exportera en mall</span><span class="sxs-lookup"><span data-stu-id="4f44c-1271">Support for additional Template Export options</span></span>
    - <span data-ttu-id="4f44c-1272">Lägg till parametern ”-SkipResourceNameParameterization” till Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4f44c-1272">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="4f44c-1273">Lägg till parametern ”-SkipAllParameterization” till Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4f44c-1273">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="4f44c-1274">Lägg till parametern ”-Resource” till Export-AzResourceGroup för exporterad resursfiltrering</span><span class="sxs-lookup"><span data-stu-id="4f44c-1274">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="4f44c-1275">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4f44c-1275">Az.ServiceFabric</span></span>
* <span data-ttu-id="4f44c-1276">Åtgärda att fel tumavtryck används vid tilläggning av certifikat i ByExistingKeyVault i vissa fall</span><span class="sxs-lookup"><span data-stu-id="4f44c-1276">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="4f44c-1277">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4f44c-1277">Az.Sql</span></span>
* <span data-ttu-id="4f44c-1278">Åtgärda suffix för lagringsslutpunkt i Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="4f44c-1278">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="4f44c-1279">Åtgärda att aktivering av Advanced Data Security åsidosätter Advanced Threat Protection-princip</span><span class="sxs-lookup"><span data-stu-id="4f44c-1279">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="4f44c-1280">Nya cmdletar för Management.Sql som gör att kunderna kan lägga till nycklar för transparent datakryptering (TDE) och ange TDE-skydd för hanterade instanser</span><span class="sxs-lookup"><span data-stu-id="4f44c-1280">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="4f44c-1281">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="4f44c-1281">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="4f44c-1282">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="4f44c-1282">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="4f44c-1283">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="4f44c-1283">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="4f44c-1284">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="4f44c-1284">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="4f44c-1285">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="4f44c-1285">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4f44c-1286">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4f44c-1286">Az.Storage</span></span>
* <span data-ttu-id="4f44c-1287">Stöd för typerna FileStorage och SkuName Premium_ZRS när lagringskonton skapas</span><span class="sxs-lookup"><span data-stu-id="4f44c-1287">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="4f44c-1288">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4f44c-1288">New-AzStorageAccount</span></span>
* <span data-ttu-id="4f44c-1289">Beskrivningen av cmdleten för bloboföränderlighet har förtydligats</span><span class="sxs-lookup"><span data-stu-id="4f44c-1289">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="4f44c-1290">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="4f44c-1290">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4f44c-1291">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4f44c-1291">Az.Websites</span></span>
* <span data-ttu-id="4f44c-1292">Optimerar Get-AzWebAppCertificate för att filtrera efter resursgrupp på servern i stället för klienten</span><span class="sxs-lookup"><span data-stu-id="4f44c-1292">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="4f44c-1293">Lägger till växlingsparametern -UseDisasterRecovery till Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="4f44c-1293">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="4f44c-1294">2.2.0 – juni 2019</span><span class="sxs-lookup"><span data-stu-id="4f44c-1294">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="4f44c-1295">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="4f44c-1295">Az.Cdn</span></span>
* <span data-ttu-id="4f44c-1296">Uppdaterade cmdletar för att ge stöd för rulesEngine-funktion baserat på API-version 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1296">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4f44c-1297">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4f44c-1297">Az.Compute</span></span>
* <span data-ttu-id="4f44c-1298">Lade till parameter `NoWait` som startar åtgärden och returnerar omedelbart, innan åtgärden har slutförts.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1298">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="4f44c-1299">Uppdaterade cmdletar:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="4f44c-1299">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="4f44c-1300">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="4f44c-1300">Az.EventHub</span></span>
* <span data-ttu-id="4f44c-1301">Korrigering för #9231 – Get-AzEventHubNamespace returnerar inga taggar</span><span class="sxs-lookup"><span data-stu-id="4f44c-1301">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="4f44c-1302">Korrigering för #9230 – Get-AzEventHubNamespace returnerar ResourceGroup istället för ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f44c-1302">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4f44c-1303">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4f44c-1303">Az.Network</span></span>
* <span data-ttu-id="4f44c-1304">Uppdatera ResourceId och InputObject för NAT-gateway</span><span class="sxs-lookup"><span data-stu-id="4f44c-1304">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="4f44c-1305">Lägg till alias för ResourceId och InputObject</span><span class="sxs-lookup"><span data-stu-id="4f44c-1305">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="4f44c-1306">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="4f44c-1306">Az.PolicyInsights</span></span>
* <span data-ttu-id="4f44c-1307">Åtgärda Null-referensproblem i Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="4f44c-1307">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4f44c-1308">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4f44c-1308">Az.RecoveryServices</span></span>
* <span data-ttu-id="4f44c-1309">Minsta kvarhållning för IaaSVM-policy i dagar ändrat till 7 från 1</span><span class="sxs-lookup"><span data-stu-id="4f44c-1309">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="4f44c-1310">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="4f44c-1310">Az.ServiceBus</span></span>
* <span data-ttu-id="4f44c-1311">Korrigering för ärende #9182 – Get-AzServiceBusNamespace returnerar ResourceGroup istället för ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f44c-1311">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="4f44c-1312">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4f44c-1312">Az.ServiceFabric</span></span>
* <span data-ttu-id="4f44c-1313">Åtgärda stavfel i felmeddelandet för Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="4f44c-1313">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="4f44c-1314">Åtgärda saknat tecken i Service Fabric-kommandorader</span><span class="sxs-lookup"><span data-stu-id="4f44c-1314">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="4f44c-1315">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4f44c-1315">Az.Sql</span></span>
* <span data-ttu-id="4f44c-1316">Lägg till parametern DnsZonePartner för New-AzureSqlInstance-cmdlet för att ge stöd för AutoDr för hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1316">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="4f44c-1317">Avvecklar cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="4f44c-1317">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="4f44c-1318">Döp om cmdletar för hotidentifiering till Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="4f44c-1318">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="4f44c-1319">Parametrarna New-AzSqlInstance -StorageSizeInGB och -LicenseType är nu valfria.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1319">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4f44c-1320">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4f44c-1320">Az.Websites</span></span>
* <span data-ttu-id="4f44c-1321">åtgärdar problemet där användningen av Set-AzWebApp och Set-AzWebAppSlot med -WebApp-egenskap tog bort taggarna</span><span class="sxs-lookup"><span data-stu-id="4f44c-1321">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="4f44c-1322">2.1.0 – maj 2019</span><span class="sxs-lookup"><span data-stu-id="4f44c-1322">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="4f44c-1323">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4f44c-1323">Az.ApiManagement</span></span>
* <span data-ttu-id="4f44c-1324">Skapade nya cmdletar för att hantera diagnostik för global- och API-omfång</span><span class="sxs-lookup"><span data-stu-id="4f44c-1324">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="4f44c-1325">**Get-AzApiManagementDiagnostic** – Skaffa diagnostik konfigurerad för global- eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="4f44c-1325">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="4f44c-1326">**New-AzApiManagementDiagnostic** – Skapa ny diagnostik för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="4f44c-1326">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="4f44c-1327">**New-AzApiManagementHttpMessageDiagnostic** – Skapa diagnostikinställning om vilka rubriker som ska loggas och storleken på brödtextbyte</span><span class="sxs-lookup"><span data-stu-id="4f44c-1327">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="4f44c-1328">**New-AzApiManagementPipelineDiagnosticSetting** – Skapa diagnostikinställningar för inkommande/utgående HTTP-meddelanden till gatewayen.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1328">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="4f44c-1329">**New-AzApiManagementSamplingSetting** – Skapa samplinginställningar för begäranden/svar för en diagnostik</span><span class="sxs-lookup"><span data-stu-id="4f44c-1329">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="4f44c-1330">**Remove-AzApiManagementDiagnostic** – Ta bort en diagnostikenhet för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="4f44c-1330">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="4f44c-1331">**Set-AzApiManagementDiagnostic** – Uppdatera en diagnostikenhet för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="4f44c-1331">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="4f44c-1332">Skapade nya cmdletar för hantering av cacheminne i ApiManagement-tjänsten</span><span class="sxs-lookup"><span data-stu-id="4f44c-1332">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="4f44c-1333">**Get-AzApiManagementCache** – Hämta information om cacheminnet som anges av identifierare eller alla cacheminnen</span><span class="sxs-lookup"><span data-stu-id="4f44c-1333">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="4f44c-1334">**New-AzApiManagementCache** – Skapa ett nytt default-cacheminne eller cacheminne i en viss Azure-region</span><span class="sxs-lookup"><span data-stu-id="4f44c-1334">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="4f44c-1335">**Remove-AzApiManagementCache** – Ta bort ett cacheminne</span><span class="sxs-lookup"><span data-stu-id="4f44c-1335">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="4f44c-1336">**Remove-AzApiManagementCache** – Ta bort ett cacheminne</span><span class="sxs-lookup"><span data-stu-id="4f44c-1336">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="4f44c-1337">Skapade nya cmdletar för hantering av API-schema</span><span class="sxs-lookup"><span data-stu-id="4f44c-1337">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="4f44c-1338">**New-AzApiManagementSchema** – Skapa ett nytt schema för ett API</span><span class="sxs-lookup"><span data-stu-id="4f44c-1338">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="4f44c-1339">**Get-AzApiManagementSchema** – Hämta de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="4f44c-1339">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="4f44c-1340">**Remove-AzApiManagementSchema** – Ta bort de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="4f44c-1340">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="4f44c-1341">**Set-AzApiManagementSchema** – Uppdatera de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="4f44c-1341">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="4f44c-1342">Skapa ny cmdlet för att generera en användartoken.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1342">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="4f44c-1343">**New-AzApiManagementUserToken** – Skapa en ny användartoken som enligt standardinställning är giltig i 8 timmar. Token för GIT-användaren kan skapas med den här cmdleten./</span><span class="sxs-lookup"><span data-stu-id="4f44c-1343">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="4f44c-1344">Skapade en ny cmdlet för att hämta nätverksstatus</span><span class="sxs-lookup"><span data-stu-id="4f44c-1344">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="4f44c-1345">**Get-AzApiManagementNetworkStatus** – Hämta nätverksstatusanslutningen för resurserna som API Management-tjänsten är beroende av.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1345">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="4f44c-1346">Det här är användbart när du distribuerar ApiManagement-tjänsten i ett virtuellt nätverk och validerar om något beroende är brutet.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1346">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="4f44c-1347">Uppdaterade cmdlet **New-AzApiManagement** för att hantera ApiManagement-tjänsten</span><span class="sxs-lookup"><span data-stu-id="4f44c-1347">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="4f44c-1348">Lade till stöd för den nya SKU:n Consumption</span><span class="sxs-lookup"><span data-stu-id="4f44c-1348">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="4f44c-1349">Aktiverade stöd för att slå på flaggan EnableClientCertificate för SKU:n Consumption</span><span class="sxs-lookup"><span data-stu-id="4f44c-1349">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="4f44c-1350">Den nya cmdleten **New-AzApiManagementSslSetting** gör det möjligt att ställa in TLS/SSL-inställningen på ”Backend” och ”Frontend” (serverdel och klientdel).</span><span class="sxs-lookup"><span data-stu-id="4f44c-1350">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="4f44c-1351">Det här kan också användas till att konfigurera chiffer som 3DES och ServerProtocols som Http2 för Frontend för en ApiManagement-tjänst.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1351">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="4f44c-1352">Stöd har lagts till för att konfigurera värdnamnet DeveloperPortal på ApiManagement-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1352">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="4f44c-1353">Uppdaterade cmdletar **Get-AzApiManagementSsoToken** för att ta PsApiManagement-objekt som indata</span><span class="sxs-lookup"><span data-stu-id="4f44c-1353">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="4f44c-1354">Uppdaterad cmdleten för att visa infogade felmeddelanden</span><span class="sxs-lookup"><span data-stu-id="4f44c-1354">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="4f44c-1355">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Felkod: Felmeddelande av typen ValidationError: Ett eller flera fält innehåller felaktiga värden: Felinformation:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="4f44c-1355">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="4f44c-1356">Uppdaterade cmdlet **Export-AzApiManagementApi** för att exportera API:er i OpenApi 3.0-format</span><span class="sxs-lookup"><span data-stu-id="4f44c-1356">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="4f44c-1357">Uppdaterade cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="4f44c-1357">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="4f44c-1358">Importera API från dokumentspecifikationen OpenApi 3.0</span><span class="sxs-lookup"><span data-stu-id="4f44c-1358">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="4f44c-1359">Om du vill åsidosätta egenskapen PsApiManagementSchema specificerad i ett dokument (Swagger, Wadl, Wsdl, OpenApi).</span><span class="sxs-lookup"><span data-stu-id="4f44c-1359">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="4f44c-1360">Åsidosätta egenskapen ServiceUrl som specificeras i ett dokument.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1360">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="4f44c-1361">Uppdaterade cmdlet **Get-AzApiManagementPolicy** för att returnera policy i undantaget format av typen icke-XML med rawxml</span><span class="sxs-lookup"><span data-stu-id="4f44c-1361">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="4f44c-1362">Uppdaterade cmdlet **Set-AzApiManagementPolicy** för att godkänna policy i undantaget format av typen icke-XML med rawxml och XML undantaget med xml</span><span class="sxs-lookup"><span data-stu-id="4f44c-1362">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="4f44c-1363">Uppdaterad cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="4f44c-1363">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="4f44c-1364">Konfigurera API med OpenId auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1364">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="4f44c-1365">Skapa ett API i ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="4f44c-1365">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="4f44c-1366">Klona ett API med SourceApiId och SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1366">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="4f44c-1367">Möjlighet att konfigurera SubscriptionRequired i API-omfattningen.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1367">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="4f44c-1368">Uppdaterad cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="4f44c-1368">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="4f44c-1369">Konfigurera API med OpenId auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1369">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="4f44c-1370">Uppdatera ett API till ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="4f44c-1370">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="4f44c-1371">Möjlighet att konfigurera SubscriptionRequired i API-omfattningen.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1371">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="4f44c-1372">Uppdaterad cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="4f44c-1372">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="4f44c-1373">Klona en befintlig version med hjälp av SourceApiRevision (kopiera taggar, produkter, åtgärder och principer).</span><span class="sxs-lookup"><span data-stu-id="4f44c-1373">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="4f44c-1374">Den nya revisionen antar ApiId från den överordnade instansen.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1374">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="4f44c-1375">Tillhandahålla ApiRevisionDescription</span><span class="sxs-lookup"><span data-stu-id="4f44c-1375">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="4f44c-1376">Åsidosätta ServiceUrl vid kloning av ett API.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1376">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="4f44c-1377">Uppdaterad cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="4f44c-1377">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="4f44c-1378">Konfigurera AAD eller AADB2C med en Authority</span><span class="sxs-lookup"><span data-stu-id="4f44c-1378">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="4f44c-1379">Konfigurera SignupPolicy, SigninPolicy, ProfileEditingPolicy och PasswordResetPolicy</span><span class="sxs-lookup"><span data-stu-id="4f44c-1379">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="4f44c-1380">Uppdaterad cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="4f44c-1380">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="4f44c-1381">Kompensera för ny SubscriptonModel med Scope och UserId</span><span class="sxs-lookup"><span data-stu-id="4f44c-1381">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="4f44c-1382">Kompensera för gammal prenumerationsmodell med ProductId och UserId</span><span class="sxs-lookup"><span data-stu-id="4f44c-1382">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="4f44c-1383">Lägg till funktion för att aktivera AllowTracing på prenumerationsnivå.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1383">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="4f44c-1384">Uppdaterad cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="4f44c-1384">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="4f44c-1385">Kompensera för ny SubscriptonModel med Scope och UserId</span><span class="sxs-lookup"><span data-stu-id="4f44c-1385">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="4f44c-1386">Kompensera för gammal prenumerationsmodell med ProductId och UserId</span><span class="sxs-lookup"><span data-stu-id="4f44c-1386">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="4f44c-1387">Lägg till funktion för att aktivera AllowTracing på prenumerationsnivå.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1387">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="4f44c-1388">Uppdaterade följande cmdletar för att acceptera ResourceId som indata</span><span class="sxs-lookup"><span data-stu-id="4f44c-1388">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="4f44c-1389">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="4f44c-1389">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="4f44c-1390">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="4f44c-1390">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="4f44c-1391">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="4f44c-1391">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="4f44c-1392">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="4f44c-1392">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="4f44c-1393">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="4f44c-1393">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="4f44c-1394">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="4f44c-1394">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="4f44c-1395">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="4f44c-1395">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="4f44c-1396">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="4f44c-1396">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="4f44c-1397">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="4f44c-1397">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="4f44c-1398">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="4f44c-1398">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="4f44c-1399">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="4f44c-1399">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="4f44c-1400">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="4f44c-1400">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4f44c-1401">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4f44c-1401">Az.Automation</span></span>
* <span data-ttu-id="4f44c-1402">Uppdaterade Get-AzAutomationJobOutputRecord för att hantera postvärden av typen JSON och Text.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1402">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="4f44c-1403">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="4f44c-1403">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="4f44c-1404">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="4f44c-1404">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="4f44c-1405">Ändrade beteende för Start-AzAutomationDscCompilationJob till att bara starta jobbet istället för att vänta på slutförandet.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1405">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="4f44c-1406">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="4f44c-1406">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="4f44c-1407">Korrigering för Get-AzAutomationDscNode när using -Name returnerar alla noder.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1407">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="4f44c-1408">Nu returnerar den endast den matchande noden.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1408">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4f44c-1409">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4f44c-1409">Az.Compute</span></span>
* <span data-ttu-id="4f44c-1410">Lägg till parametrarna ProtectFromScaleIn och ProtectFromScaleSetAction i cmdleten Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1410">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="4f44c-1411">Nu är standardinställningen att vimpelparametern New-AzVM använder en tillgänglig plats om USA, östra inte stöds</span><span class="sxs-lookup"><span data-stu-id="4f44c-1411">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4f44c-1412">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4f44c-1412">Az.DataLakeStore</span></span>
* <span data-ttu-id="4f44c-1413">Uppdatera ADLS-sdk för att använda httpclient, integrera dataplanstestning med Azure-ramverk</span><span class="sxs-lookup"><span data-stu-id="4f44c-1413">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4f44c-1414">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4f44c-1414">Az.Monitor</span></span>
* <span data-ttu-id="4f44c-1415">Korrigera felaktiga parameternamn i hjälpexempel</span><span class="sxs-lookup"><span data-stu-id="4f44c-1415">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4f44c-1416">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4f44c-1416">Az.Network</span></span>
* <span data-ttu-id="4f44c-1417">Lägg till flaggan DisableBgpRoutePropagation i utdata för effektiv routningstabell</span><span class="sxs-lookup"><span data-stu-id="4f44c-1417">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="4f44c-1418">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="4f44c-1418">Updated cmdlet:</span></span>
        - <span data-ttu-id="4f44c-1419">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="4f44c-1419">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="4f44c-1420">Åtgärda dubbelstreck i dokumentationen New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="4f44c-1420">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="4f44c-1421">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4f44c-1421">Az.Resources</span></span>
* <span data-ttu-id="4f44c-1422">Lägg till ny cmdlet Get-AzureRmDenyAssignment för att hämta tilldelningsnekanden</span><span class="sxs-lookup"><span data-stu-id="4f44c-1422">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="4f44c-1423">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4f44c-1423">Az.Sql</span></span>
* <span data-ttu-id="4f44c-1424">Döp om Advanced Threat Protection-cmdletar för Advanced Data Security och aktivera Vulnerability Assessment som standard</span><span class="sxs-lookup"><span data-stu-id="4f44c-1424">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="4f44c-1425">2.0.0 – maj 2019</span><span class="sxs-lookup"><span data-stu-id="4f44c-1425">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4f44c-1426">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4f44c-1426">Az.Accounts</span></span>
* <span data-ttu-id="4f44c-1427">Uppdatera autentiseringsbiblioteket för att åtgärda ADFS-problem med autentisering av användarnamn/lösenord</span><span class="sxs-lookup"><span data-stu-id="4f44c-1427">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="4f44c-1428">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="4f44c-1428">Az.CognitiveServices</span></span>
* <span data-ttu-id="4f44c-1429">Visa endast Bing-ansvarsfriskrivning för Bing-sökningstjänster.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1429">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="4f44c-1430">Förbättra felmeddelande när det inte går att skapa konton.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1430">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4f44c-1431">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4f44c-1431">Az.Compute</span></span>
* <span data-ttu-id="4f44c-1432">Funktion för närhetsplaceringsgrupper.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1432">Proximity placement group feature.</span></span>
    - <span data-ttu-id="4f44c-1433">Följande nya cmdletar har lagts till:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="4f44c-1433">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="4f44c-1434">Den nya parametern ProximityPlacementGroupId har lagts till i följande cmdletar:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="4f44c-1434">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="4f44c-1435">Parametern StorageAccountType har lagts till i New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1435">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="4f44c-1436">TargetRegion för New-AzGalleryImageVersion kan innehålla StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1436">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="4f44c-1437">Växlingsparametern SkipShutdown har lagts till i Stop-AzVM och Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4f44c-1437">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="4f44c-1438">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="4f44c-1438">Breaking changes</span></span>
    - <span data-ttu-id="4f44c-1439">Set-AzVMBootDiagnostics har ändrats till Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1439">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="4f44c-1440">Export-AzLogAnalyticThrottledRequests har ändrats till Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1440">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="4f44c-1441">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="4f44c-1441">Az.DeploymentManager</span></span>
* <span data-ttu-id="4f44c-1442">De första allmänt tillgängliga versionerna av cmdletar för Distributionshanteraren i Azure</span><span class="sxs-lookup"><span data-stu-id="4f44c-1442">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="4f44c-1443">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="4f44c-1443">Az.Dns</span></span>
* <span data-ttu-id="4f44c-1444">Automatisk delegering av DNS för NameServer</span><span class="sxs-lookup"><span data-stu-id="4f44c-1444">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="4f44c-1445">Det överordnade zonnamnet kan användas som ytterligare valfri parameter i cmdleten för att skapa DNS-zoner.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1445">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="4f44c-1446">Lägger till NS-poster för en nyligen skapad underordnad zon i den överordnade zonen.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1446">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="4f44c-1447">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="4f44c-1447">Az.FrontDoor</span></span>
* <span data-ttu-id="4f44c-1448">De första allmänt tillgängliga versionerna av cmdletar för Azure FrontDoor</span><span class="sxs-lookup"><span data-stu-id="4f44c-1448">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="4f44c-1449">Byt namn på WAF-cmdletar så att de omfattar ”Waf”</span><span class="sxs-lookup"><span data-stu-id="4f44c-1449">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="4f44c-1450">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="4f44c-1450">Az.HDInsight</span></span>
* <span data-ttu-id="4f44c-1451">Två cmdletar har tagits bort:</span><span class="sxs-lookup"><span data-stu-id="4f44c-1451">Removed two cmdlets:</span></span>
    - <span data-ttu-id="4f44c-1452">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="4f44c-1452">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="4f44c-1453">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="4f44c-1453">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="4f44c-1454">En ny cmdlet har lagts till, Set-AzHDInsightGatewayCredential, som ersätter Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="4f44c-1454">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="4f44c-1455">Uppdatera cmdleten Get-AzHDInsightJobOutput för att skilja mellan läsarrollen och HDInsight-operatörsrollen:</span><span class="sxs-lookup"><span data-stu-id="4f44c-1455">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="4f44c-1456">Användare med läsarrollen måste uttryckligen ange parametern ”DefaultStorageAccountKey”, annars uppstår fel.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1456">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="4f44c-1457">Användare med HDInsight-operatörsrollen påverkas inte.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1457">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4f44c-1458">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4f44c-1458">Az.Monitor</span></span>
* <span data-ttu-id="4f44c-1459">Nya cmdletar för SQR API (schemalagd frågeregel)</span><span class="sxs-lookup"><span data-stu-id="4f44c-1459">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="4f44c-1460">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="4f44c-1460">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="4f44c-1461">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="4f44c-1461">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="4f44c-1462">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="4f44c-1462">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="4f44c-1463">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="4f44c-1463">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="4f44c-1464">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="4f44c-1464">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="4f44c-1465">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="4f44c-1465">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="4f44c-1466">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="4f44c-1466">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="4f44c-1467">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="4f44c-1467">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="4f44c-1468">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="4f44c-1468">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="4f44c-1469">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="4f44c-1469">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="4f44c-1470">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="4f44c-1470">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="4f44c-1471">[Mer](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information om SQR API</span><span class="sxs-lookup"><span data-stu-id="4f44c-1471">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="4f44c-1472">Az.Monitor.md har uppdaterats för att omfatta cmdletar för måttbaserade aviseringsregler i GenV2 (inte klassiska)</span><span class="sxs-lookup"><span data-stu-id="4f44c-1472">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4f44c-1473">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4f44c-1473">Az.Network</span></span>
* <span data-ttu-id="4f44c-1474">Lägg till stöd för NAT Gateway-resurs</span><span class="sxs-lookup"><span data-stu-id="4f44c-1474">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="4f44c-1475">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="4f44c-1475">New cmdlets</span></span>
        - <span data-ttu-id="4f44c-1476">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="4f44c-1476">New-AzNatGateway</span></span>
        - <span data-ttu-id="4f44c-1477">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="4f44c-1477">Get-AzNatGateway</span></span>
        - <span data-ttu-id="4f44c-1478">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="4f44c-1478">Set-AzNatGateway</span></span>
        - <span data-ttu-id="4f44c-1479">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="4f44c-1479">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="4f44c-1480">Uppdaterade cmdletar</span><span class="sxs-lookup"><span data-stu-id="4f44c-1480">Updated cmdlets</span></span>
        - <span data-ttu-id="4f44c-1481">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="4f44c-1481">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="4f44c-1482">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="4f44c-1482">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="4f44c-1483">Nedanstående kommandon för funktionen har uppdaterats: Ange/ta bort anpassade vägar på Brooklyn Gateway.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1483">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="4f44c-1484">New-AzVirtualNetworkGateway har uppdaterats: Den valfria parametern -CustomRoute har lagts till för att ställa in adressprefix som anpassade vägar för att ange gateway.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1484">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="4f44c-1485">Set-AzVirtualNetworkGateway har uppdaterats: Den valfria parametern -CustomRoute har lagts till för att ange adressprefix som anpassade vägar för att ange gateway.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1485">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="4f44c-1486">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="4f44c-1486">Az.PolicyInsights</span></span>
* <span data-ttu-id="4f44c-1487">Stöd för att fråga efter information om principutvärdering.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1487">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="4f44c-1488">Lägg till parametern ”-Expand” för Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1488">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="4f44c-1489">Stöd för -Expand PolicyEvaluationDetails.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1489">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4f44c-1490">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4f44c-1490">Az.RecoveryServices</span></span>
* <span data-ttu-id="4f44c-1491">Stöd för att dela prenumeration mellan Azure och Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1491">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="4f44c-1492">Markering av kommande icke-bakåtkompatibla ändringar för Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1492">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="4f44c-1493">Korrigering för återställningsplan och åtgärdsplan i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1493">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="4f44c-1494">Korrigering för mappning av uppdateringsnätverk i Azure Site Recovery för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1494">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="4f44c-1495">Korrigering för instruktioner för uppdateringsskydd i Azure Site Recovery för Azure till Azure för hanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1495">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="4f44c-1496">Andra mindre korrigeringar.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1496">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="4f44c-1497">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="4f44c-1497">Az.Relay</span></span>
* <span data-ttu-id="4f44c-1498">Korrigera stavfel i kundriktade meddelanden</span><span class="sxs-lookup"><span data-stu-id="4f44c-1498">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="4f44c-1499">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="4f44c-1499">Az.ServiceBus</span></span>
* <span data-ttu-id="4f44c-1500">Nya cmdletar har lagts till för NetworkRuleSet för namnområden</span><span class="sxs-lookup"><span data-stu-id="4f44c-1500">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4f44c-1501">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4f44c-1501">Az.Storage</span></span>
* <span data-ttu-id="4f44c-1502">Uppgradera till lagringsklientbiblioteket 10.0.1 (namnområdet för alla objekt från detta SDK ändras från ”Microsoft.WindowsAzure.Storage. *till ”Microsoft.Azure.Storage.* ”)</span><span class="sxs-lookup"><span data-stu-id="4f44c-1502">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="4f44c-1503">Uppgradera till Microsoft.Azure.Management.Storage 11.0.0 för att stödja den nya API-versionen 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1503">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="4f44c-1504">Standardlagringskontot i Skapa lagringskonto ändras från ”Storage” till ”StorageV2”</span><span class="sxs-lookup"><span data-stu-id="4f44c-1504">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="4f44c-1505">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4f44c-1505">New-AzStorageAccount</span></span>
* <span data-ttu-id="4f44c-1506">Ändra lagringskontots cmdlet-utdata Sku.Name för att passa med indata-SkuName genom att lägga till ”-”. Till exempel ändras ”StandardLRS” till ”Standard_LRS”</span><span class="sxs-lookup"><span data-stu-id="4f44c-1506">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="4f44c-1507">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4f44c-1507">New-AzStorageAccount</span></span>
    - <span data-ttu-id="4f44c-1508">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4f44c-1508">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="4f44c-1509">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4f44c-1509">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4f44c-1510">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4f44c-1510">Az.Websites</span></span>
* <span data-ttu-id="4f44c-1511">Egenskapen ”typ” konfigureras nu för PSSite-objekt som returneras av Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="4f44c-1511">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="4f44c-1512">Get-AzWebApp\*Metrics och Get-AzAppServicePlanMetrics markeras som inaktuella</span><span class="sxs-lookup"><span data-stu-id="4f44c-1512">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="4f44c-1513">1.8.0 – april 2019</span><span class="sxs-lookup"><span data-stu-id="4f44c-1513">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="4f44c-1514">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="4f44c-1514">Highlights since the last major release</span></span>
* <span data-ttu-id="4f44c-1515">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="4f44c-1515">General availability of `Az` module</span></span>
* <span data-ttu-id="4f44c-1516">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="4f44c-1516">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="4f44c-1517">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="4f44c-1517">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="4f44c-1518">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="4f44c-1518">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="4f44c-1519">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="4f44c-1519">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="4f44c-1520">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="4f44c-1520">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="4f44c-1521">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="4f44c-1521">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="4f44c-1522">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4f44c-1522">Az.Accounts</span></span>
* <span data-ttu-id="4f44c-1523">Uppdatera Uninstall-AzureRm för att ta bort moduler i Mac på ett korrekt sätt</span><span class="sxs-lookup"><span data-stu-id="4f44c-1523">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="4f44c-1524">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="4f44c-1524">Az.Batch</span></span>
* <span data-ttu-id="4f44c-1525">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1525">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="4f44c-1526">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="4f44c-1526">Az.Cdn</span></span>
* <span data-ttu-id="4f44c-1527">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1527">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="4f44c-1528">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="4f44c-1528">Az.CognitiveServices</span></span>
* <span data-ttu-id="4f44c-1529">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1529">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4f44c-1530">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4f44c-1530">Az.Compute</span></span>
* <span data-ttu-id="4f44c-1531">Åtgärda problem med AEM-installationen om resurs-ID:n för diskar innehåller resourcegroups i gemener i resurs-ID:n</span><span class="sxs-lookup"><span data-stu-id="4f44c-1531">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="4f44c-1532">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1532">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="4f44c-1533">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="4f44c-1533">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4f44c-1534">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4f44c-1534">Az.DataFactory</span></span>
* <span data-ttu-id="4f44c-1535">Lägg till SsisProperties om NodeCount inte är null för hanterad integreringskörning.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1535">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4f44c-1536">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4f44c-1536">Az.DataLakeStore</span></span>
* <span data-ttu-id="4f44c-1537">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1537">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="4f44c-1538">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="4f44c-1538">Az.EventGrid</span></span>
* <span data-ttu-id="4f44c-1539">Hjälptexten för slutpunkten har uppdaterats för att visa att resurser ska skapas innan cmdletarna för att skapa/uppdatera händelseprenumerationer används.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1539">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="4f44c-1540">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="4f44c-1540">Az.EventHub</span></span>
* <span data-ttu-id="4f44c-1541">Nya cmdletar har lagts till för NetworkRuleSet för namnområden</span><span class="sxs-lookup"><span data-stu-id="4f44c-1541">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="4f44c-1542">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="4f44c-1542">Az.HDInsight</span></span>
* <span data-ttu-id="4f44c-1543">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1543">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="4f44c-1544">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="4f44c-1544">Az.IotHub</span></span>
* <span data-ttu-id="4f44c-1545">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1545">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="4f44c-1546">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4f44c-1546">Az.KeyVault</span></span>
* <span data-ttu-id="4f44c-1547">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1547">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="4f44c-1548">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="4f44c-1548">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="4f44c-1549">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="4f44c-1549">Az.MachineLearning</span></span>
* <span data-ttu-id="4f44c-1550">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1550">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="4f44c-1551">Az.Media</span><span class="sxs-lookup"><span data-stu-id="4f44c-1551">Az.Media</span></span>
* <span data-ttu-id="4f44c-1552">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1552">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4f44c-1553">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4f44c-1553">Az.Monitor</span></span>
  * <span data-ttu-id="4f44c-1554">Nya cmdletar för måttbaserad aviseringsregel i GenV2 (inte klassisk)</span><span class="sxs-lookup"><span data-stu-id="4f44c-1554">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="4f44c-1555">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="4f44c-1555">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="4f44c-1556">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="4f44c-1556">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="4f44c-1557">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="4f44c-1557">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="4f44c-1558">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="4f44c-1558">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="4f44c-1559">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="4f44c-1559">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="4f44c-1560">Monitor SDK har uppdaterats till version 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="4f44c-1560">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4f44c-1561">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4f44c-1561">Az.Network</span></span>
* <span data-ttu-id="4f44c-1562">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1562">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="4f44c-1563">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="4f44c-1563">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="4f44c-1564">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="4f44c-1564">Az.NotificationHubs</span></span>
* <span data-ttu-id="4f44c-1565">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1565">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="4f44c-1566">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="4f44c-1566">Az.OperationalInsights</span></span>
* <span data-ttu-id="4f44c-1567">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1567">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="4f44c-1568">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="4f44c-1568">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="4f44c-1569">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1569">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4f44c-1570">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4f44c-1570">Az.RecoveryServices</span></span>
* <span data-ttu-id="4f44c-1571">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1571">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="4f44c-1572">Tabellformatet för SQL i virtuella Azure-datorer har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="4f44c-1572">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="4f44c-1573">En alternativ metod för att hämta platser i AzureFileShare har lagts till</span><span class="sxs-lookup"><span data-stu-id="4f44c-1573">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="4f44c-1574">ScheduleRunDays i SchedulePolicy-objekt har uppdaterats enligt tidszon</span><span class="sxs-lookup"><span data-stu-id="4f44c-1574">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="4f44c-1575">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="4f44c-1575">Az.RedisCache</span></span>
* <span data-ttu-id="4f44c-1576">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1576">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="4f44c-1577">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4f44c-1577">Az.Resources</span></span>
* <span data-ttu-id="4f44c-1578">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="4f44c-1578">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="4f44c-1579">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4f44c-1579">Az.Sql</span></span>
* <span data-ttu-id="4f44c-1580">Ersätt Monitor SDK-beroende med vanlig kod</span><span class="sxs-lookup"><span data-stu-id="4f44c-1580">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="4f44c-1581">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1581">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="4f44c-1582">Förbättrad process för klassificering av flera kolumner.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1582">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="4f44c-1583">Inkludera SKU-egenskaper (SKU-namn, serie, kapacitet) i svaret från Get-AzSqlServerServiceObjective och formatera som tabell som standard.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1583">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="4f44c-1584">Möjlighet att använda Get-AzSqlServerServiceObjective efter plats utan att behöva en redan befintlig server i regionen.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1584">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="4f44c-1585">Stöd för tidszonsparametern när hanterade instanser skapas.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1585">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="4f44c-1586">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="4f44c-1586">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4f44c-1587">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4f44c-1587">Az.Websites</span></span>
* <span data-ttu-id="4f44c-1588">åtgärdar Set-AzWebApp och Set-AzWebAppSlot så att de inte tar bort taggar vid körning</span><span class="sxs-lookup"><span data-stu-id="4f44c-1588">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="4f44c-1589">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1589">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="4f44c-1590">SDK för WebSites har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1590">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="4f44c-1591">Egenskapen AdminSiteName har tagits bort från PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1591">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="4f44c-1592">1.7.0 – april 2019</span><span class="sxs-lookup"><span data-stu-id="4f44c-1592">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="4f44c-1593">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="4f44c-1593">Highlights since the last major release</span></span>
* <span data-ttu-id="4f44c-1594">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="4f44c-1594">General availability of `Az` module</span></span>
* <span data-ttu-id="4f44c-1595">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="4f44c-1595">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="4f44c-1596">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="4f44c-1596">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="4f44c-1597">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="4f44c-1597">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="4f44c-1598">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="4f44c-1598">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="4f44c-1599">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="4f44c-1599">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="4f44c-1600">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="4f44c-1600">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="4f44c-1601">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4f44c-1601">Az.Accounts</span></span>
* <span data-ttu-id="4f44c-1602">Add-AzEnvironment och Set-AzEnvironment har uppdaterats för att godkänna parametern AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="4f44c-1602">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="4f44c-1603">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="4f44c-1603">Az.AnalysisServices</span></span>
* <span data-ttu-id="4f44c-1604">ServiceClient används i cmdletar för dataplan och den ursprungliga autentiseringslogiken har tagits bort</span><span class="sxs-lookup"><span data-stu-id="4f44c-1604">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="4f44c-1605">Add-AzureASAccount används för omslutning av Connect-AzAccount för att undvika en icke-bakåtkompatibel ändring</span><span class="sxs-lookup"><span data-stu-id="4f44c-1605">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4f44c-1606">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4f44c-1606">Az.Automation</span></span>
* <span data-ttu-id="4f44c-1607">Buggen för cmdleten New-AzAutomationSoftwareUpdateConfiguration för inkluderingar har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1607">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="4f44c-1608">Nu bör parametern IncludedKbNumber och IncludedPackageNameMask fungera.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1608">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="4f44c-1609">Felkorrigering för dynamiska grupper i uppdateringshanteringen för azure automation</span><span class="sxs-lookup"><span data-stu-id="4f44c-1609">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4f44c-1610">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4f44c-1610">Az.Compute</span></span>
* <span data-ttu-id="4f44c-1611">Lägg till parametern HyperVGeneration i New-AzDiskConfig och New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="4f44c-1611">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="4f44c-1612">Tillåt att virtuella datorer skapas med galleribilder från andra klientorganisationer.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1612">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="4f44c-1613">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="4f44c-1613">Az.ContainerInstance</span></span>
* <span data-ttu-id="4f44c-1614">Ett problem har åtgärdats i parametern -Command för New-AzContainerGroup som lade till ett avslutande tomt argument</span><span class="sxs-lookup"><span data-stu-id="4f44c-1614">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4f44c-1615">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4f44c-1615">Az.DataFactory</span></span>
* <span data-ttu-id="4f44c-1616">ADF .Net SDK-versionen har uppdaterats till 3.0.2</span><span class="sxs-lookup"><span data-stu-id="4f44c-1616">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="4f44c-1617">Cmdleten Set-AzDataFactoryV2 har uppdaterats med extra parametrar för inställningar som rör RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1617">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="4f44c-1618">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4f44c-1618">Az.Resources</span></span>
* <span data-ttu-id="4f44c-1619">Förbättra hanteringen av providrar för Get-AzResource när parametrarna -ResourceId eller -ResourceGroupName, -Name och -ResourceType tillhandahålls</span><span class="sxs-lookup"><span data-stu-id="4f44c-1619">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="4f44c-1620">Förbättra felhanteringen för ”Test-AzDeployment” och ”Test-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="4f44c-1620">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="4f44c-1621">Hantera fel utanför distributionsvalideringen och ta med dem i kommandoutdata istället</span><span class="sxs-lookup"><span data-stu-id="4f44c-1621">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="4f44c-1622">Mer information här: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="4f44c-1622">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="4f44c-1623">Lägg till växlingsparametern -IgnoreDynamicParameters till en uppsättning av cmdletar för distribution för att hoppa över fråga i skript och jobbscenarier</span><span class="sxs-lookup"><span data-stu-id="4f44c-1623">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="4f44c-1624">Mer information här: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="4f44c-1624">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="4f44c-1625">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4f44c-1625">Az.Sql</span></span>
* <span data-ttu-id="4f44c-1626">Stöd för dataklassificering av databaser.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1626">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4f44c-1627">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4f44c-1627">Az.Storage</span></span>
* <span data-ttu-id="4f44c-1628">Rapportera detaljfel när lagringskontext skapas med parametern -UseConnectedAccount, men utan inloggning på Azure-kontot</span><span class="sxs-lookup"><span data-stu-id="4f44c-1628">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="4f44c-1629">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="4f44c-1629">New-AzStorageContext</span></span>
* <span data-ttu-id="4f44c-1630">Stöd för att hantera Blob Service-egenskaper för ett angivet lagringskonto med API:et för hanteringsplan</span><span class="sxs-lookup"><span data-stu-id="4f44c-1630">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="4f44c-1631">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="4f44c-1631">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="4f44c-1632">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="4f44c-1632">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="4f44c-1633">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="4f44c-1633">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="4f44c-1634">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="4f44c-1634">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="4f44c-1635">Stöd för -AsJob-cmdletar för att ladda upp och ladda ned blobar och filer</span><span class="sxs-lookup"><span data-stu-id="4f44c-1635">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="4f44c-1636">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="4f44c-1636">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="4f44c-1637">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="4f44c-1637">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="4f44c-1638">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="4f44c-1638">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="4f44c-1639">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="4f44c-1639">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="4f44c-1640">1.6.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="4f44c-1640">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="4f44c-1641">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="4f44c-1641">Highlights since the last major release</span></span>
* <span data-ttu-id="4f44c-1642">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="4f44c-1642">General availability of `Az` module</span></span>
* <span data-ttu-id="4f44c-1643">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="4f44c-1643">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="4f44c-1644">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="4f44c-1644">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="4f44c-1645">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="4f44c-1645">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="4f44c-1646">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="4f44c-1646">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="4f44c-1647">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="4f44c-1647">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="4f44c-1648">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="4f44c-1648">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4f44c-1649">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4f44c-1649">Az.Automation</span></span>
* <span data-ttu-id="4f44c-1650">Azure Automation – ändring av uppdateringshantering för stöd för de nya funktionerna:</span><span class="sxs-lookup"><span data-stu-id="4f44c-1650">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="4f44c-1651">Dynamisk gruppering</span><span class="sxs-lookup"><span data-stu-id="4f44c-1651">Dynamic grouping</span></span>
    * <span data-ttu-id="4f44c-1652">För-/efterskrift</span><span class="sxs-lookup"><span data-stu-id="4f44c-1652">Pre-Post script</span></span>
    * <span data-ttu-id="4f44c-1653">Inställning för omstart</span><span class="sxs-lookup"><span data-stu-id="4f44c-1653">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4f44c-1654">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4f44c-1654">Az.Compute</span></span>
* <span data-ttu-id="4f44c-1655">Åtgärda problem med sökvägsmatchning i Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="4f44c-1655">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="4f44c-1656">Uppdatera Compute-klientbibliotek till 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1656">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="4f44c-1657">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4f44c-1657">Az.KeyVault</span></span>
* <span data-ttu-id="4f44c-1658">Stöd för jokertecken för KeyVault-cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="4f44c-1658">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4f44c-1659">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4f44c-1659">Az.Network</span></span>
* <span data-ttu-id="4f44c-1660">Lägg till stöd för Threat Intelligence för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="4f44c-1660">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="4f44c-1661">Lägg till resurs för brandväggsprincip på översta nivå och anpassade regler för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="4f44c-1661">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4f44c-1662">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4f44c-1662">Az.RecoveryServices</span></span>
* <span data-ttu-id="4f44c-1663">SnapshotRetentionInDays har lagts till i Azure-principen för virtuella datorer för stöd av Instant RP</span><span class="sxs-lookup"><span data-stu-id="4f44c-1663">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="4f44c-1664">Pipe-stöd för avregistrering av container har lagts till</span><span class="sxs-lookup"><span data-stu-id="4f44c-1664">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="4f44c-1665">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4f44c-1665">Az.Resources</span></span>
* <span data-ttu-id="4f44c-1666">Uppdatera stöd för jokertecken för Get-AzResource och Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4f44c-1666">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="4f44c-1667">Uppdatera autentiseringsuppgifter som används vid allmänna anrop till ARM</span><span class="sxs-lookup"><span data-stu-id="4f44c-1667">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="4f44c-1668">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4f44c-1668">Az.Sql</span></span>
* <span data-ttu-id="4f44c-1669">Cmdlet-parametern (ExcludeDetectionType) för Hotidentifiering ändrades från DetectionType till sträng[] för att framtidssäkra den när nya DetectionTypes läggs till, och även för att stödja automatisk ifyllning.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1669">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4f44c-1670">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4f44c-1670">Az.Storage</span></span>
* <span data-ttu-id="4f44c-1671">Stöd för att hämta/ange/ta bort hanteringsprincip på ett lagringskonto</span><span class="sxs-lookup"><span data-stu-id="4f44c-1671">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="4f44c-1672">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="4f44c-1672">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="4f44c-1673">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="4f44c-1673">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="4f44c-1674">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="4f44c-1674">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="4f44c-1675">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="4f44c-1675">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="4f44c-1676">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="4f44c-1676">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="4f44c-1677">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="4f44c-1677">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4f44c-1678">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4f44c-1678">Az.Websites</span></span>
* <span data-ttu-id="4f44c-1679">Åtgärda fel med ARM-mall som avbryter kloning av alla platser med 'New-AzWebApp -IncludeSourceWebAppSlots'</span><span class="sxs-lookup"><span data-stu-id="4f44c-1679">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="4f44c-1680">1.5.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="4f44c-1680">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4f44c-1681">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4f44c-1681">Az.Accounts</span></span>
* <span data-ttu-id="4f44c-1682">Lägg till kommandot Register-AzModule för stöd för AutoRest-genererade cmdletar</span><span class="sxs-lookup"><span data-stu-id="4f44c-1682">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="4f44c-1683">Uppdatera exempel för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="4f44c-1683">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4f44c-1684">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4f44c-1684">Az.Automation</span></span>
* <span data-ttu-id="4f44c-1685">Problem med att hämta vissa månadsscheman i flera Azure Automation-cmdletar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="4f44c-1685">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="4f44c-1686">Åtgärda problem med att Get-AzAutomationDscNode bara returnerar de 20 översta noderna.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1686">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="4f44c-1687">Nu returneras alla noder</span><span class="sxs-lookup"><span data-stu-id="4f44c-1687">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="4f44c-1688">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="4f44c-1688">Az.Cdn</span></span>
* <span data-ttu-id="4f44c-1689">Nya Powershell-cmdletar för att aktivera/inaktivera anpassade domän-HTTPS har lagts till och de gamla har gjorts inaktuella</span><span class="sxs-lookup"><span data-stu-id="4f44c-1689">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4f44c-1690">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4f44c-1690">Az.Compute</span></span>
* <span data-ttu-id="4f44c-1691">Lägg till stöd för jokertecken för Get-cmdletar</span><span class="sxs-lookup"><span data-stu-id="4f44c-1691">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4f44c-1692">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4f44c-1692">Az.DataFactory</span></span>
* <span data-ttu-id="4f44c-1693">ADF .Net SDK-versionen har uppdaterats till 3.0.1</span><span class="sxs-lookup"><span data-stu-id="4f44c-1693">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="4f44c-1694">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="4f44c-1694">Az.LogicApp</span></span>
* <span data-ttu-id="4f44c-1695">Åtgärda problemet med att ListWorkflows endast hämtar den första sidan med resultat</span><span class="sxs-lookup"><span data-stu-id="4f44c-1695">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4f44c-1696">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4f44c-1696">Az.Network</span></span>
* <span data-ttu-id="4f44c-1697">Lägg till stöd för jokertecken för Network-cmdletar</span><span class="sxs-lookup"><span data-stu-id="4f44c-1697">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4f44c-1698">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4f44c-1698">Az.RecoveryServices</span></span>
* <span data-ttu-id="4f44c-1699">Stöd har lagts till för SQL Server i virtuella Azure-datorer</span><span class="sxs-lookup"><span data-stu-id="4f44c-1699">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="4f44c-1700">SDK-uppdatering</span><span class="sxs-lookup"><span data-stu-id="4f44c-1700">SDK Update</span></span>
* <span data-ttu-id="4f44c-1701">Get-ProtectableItem-incheckning i VMappContainer har tagits bort</span><span class="sxs-lookup"><span data-stu-id="4f44c-1701">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="4f44c-1702">Name och ServerName har lagts till som parametrar för Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="4f44c-1702">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="4f44c-1703">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4f44c-1703">Az.Resources</span></span>
* <span data-ttu-id="4f44c-1704">Lägg till parametern `-TemplateObject` i cmdletar för distribution</span><span class="sxs-lookup"><span data-stu-id="4f44c-1704">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="4f44c-1705">Mer information här: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="4f44c-1705">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="4f44c-1706">Åtgärda problem med piping av resultatet i `Get-AzResource` till `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="4f44c-1706">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="4f44c-1707">Mer information här: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="4f44c-1707">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="4f44c-1708">Åtgärda problem med ändring av JSON-datatyp när `Set-AzResource` körs</span><span class="sxs-lookup"><span data-stu-id="4f44c-1708">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="4f44c-1709">Mer information här: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="4f44c-1709">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="4f44c-1710">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4f44c-1710">Az.Sql</span></span>
* <span data-ttu-id="4f44c-1711">AuditingEndpointsCommunicator uppdateras.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1711">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="4f44c-1712">Åtgärdar beteendet hos ett gränsscenario när nya diagnostikinställningar skapas.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1712">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4f44c-1713">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4f44c-1713">Az.Storage</span></span>
* <span data-ttu-id="4f44c-1714">Stöd för BlockBlobStorage när Storage-konto skapas      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4f44c-1714">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="4f44c-1715">1.4.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="4f44c-1715">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="4f44c-1716">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="4f44c-1716">Az.AnalysisServices</span></span>
* <span data-ttu-id="4f44c-1717">Inaktuell AddAzureASAccount-cmdlet</span><span class="sxs-lookup"><span data-stu-id="4f44c-1717">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4f44c-1718">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4f44c-1718">Az.Automation</span></span>
* <span data-ttu-id="4f44c-1719">Hjälpen för Import-AzAutomationDscNodeConfiguration har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="4f44c-1719">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="4f44c-1720">Konfigurationsnamnsvalidering har lagts till i cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="4f44c-1720">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="4f44c-1721">Förbättrad felhantering för cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="4f44c-1721">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="4f44c-1722">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="4f44c-1722">Az.CognitiveServices</span></span>
* <span data-ttu-id="4f44c-1723">CustomSubdomainName har lagts till som en ny valfri parameter för New-AzCognitiveServicesAccount, som används för att ange underdomän för resursen.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1723">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4f44c-1724">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4f44c-1724">Az.Compute</span></span>
* <span data-ttu-id="4f44c-1725">Problemet med ID-parameteruppsättningar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="4f44c-1725">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="4f44c-1726">Get-AzVMExtension har uppdaterats så att alla installerade tillägg visas om parametern Name inte har angetts</span><span class="sxs-lookup"><span data-stu-id="4f44c-1726">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="4f44c-1727">Parametrarna Tag och ResourceId har lagts till i cmdleten Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="4f44c-1727">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="4f44c-1728">Get-AzVmssVM utan instans-ID och med InstanceView kan visa virtuella VMSS-datorer med instansvyn.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1728">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4f44c-1729">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4f44c-1729">Az.DataLakeStore</span></span>
* <span data-ttu-id="4f44c-1730">Cmdletar har lagts till för uppräkning och återställning av borttagna objekt i ADL</span><span class="sxs-lookup"><span data-stu-id="4f44c-1730">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="4f44c-1731">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="4f44c-1731">Az.EventHub</span></span>
* <span data-ttu-id="4f44c-1732">Ny boolesk egenskap SkipEmptyArchives har lagts till i Skip Empty Archives i CaptureDescription-klassen i Eventhub</span><span class="sxs-lookup"><span data-stu-id="4f44c-1732">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="4f44c-1733">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4f44c-1733">Az.KeyVault</span></span>
* <span data-ttu-id="4f44c-1734">Taggning i Set-AzKeyVaultSecret har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="4f44c-1734">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="4f44c-1735">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="4f44c-1735">Az.LogicApp</span></span>
* <span data-ttu-id="4f44c-1736">Grundläggande SKU har lagts till för Integrationskonton</span><span class="sxs-lookup"><span data-stu-id="4f44c-1736">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="4f44c-1737">XSLT 2.0, XSLT 3.0 och Flytande mappningstyper har lagts till</span><span class="sxs-lookup"><span data-stu-id="4f44c-1737">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="4f44c-1738">Nya cmdletar för integrationskontosammansättningar</span><span class="sxs-lookup"><span data-stu-id="4f44c-1738">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="4f44c-1739">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="4f44c-1739">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="4f44c-1740">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="4f44c-1740">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="4f44c-1741">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="4f44c-1741">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="4f44c-1742">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="4f44c-1742">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="4f44c-1743">Nya cmdletar för batchkonfiguration för integrationskonto</span><span class="sxs-lookup"><span data-stu-id="4f44c-1743">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="4f44c-1744">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="4f44c-1744">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="4f44c-1745">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="4f44c-1745">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="4f44c-1746">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="4f44c-1746">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="4f44c-1747">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="4f44c-1747">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="4f44c-1748">Logic App-SDK har uppdaterats till version 4.1.0</span><span class="sxs-lookup"><span data-stu-id="4f44c-1748">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4f44c-1749">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4f44c-1749">Az.Monitor</span></span>
* <span data-ttu-id="4f44c-1750">Hjälpen för Get-AzMetric har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="4f44c-1750">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4f44c-1751">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4f44c-1751">Az.Network</span></span>
* <span data-ttu-id="4f44c-1752">Hjälpexempel för Add-AzApplicationGatewayCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="4f44c-1752">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="4f44c-1753">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="4f44c-1753">Az.OperationalInsights</span></span>
* <span data-ttu-id="4f44c-1754">Ytterligare stöd för datakällorna New och Get ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1754">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="4f44c-1755">Ny ApplicationInsights-typ har lagts till för att ge stöd för ”Get specific” och ”Get all” för ApplicationInsights-datakällor för angiven arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1755">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="4f44c-1756">Cmdleten New-AzOperationalInsightsApplicationInsightsDataSource har lagts till för att skapa datakälla med angivna parametrar för Application Insights-resurs: subscription Id, resourceGroupName och name.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1756">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="4f44c-1757">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4f44c-1757">Az.Resources</span></span>
* <span data-ttu-id="4f44c-1758">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="4f44c-1758">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="4f44c-1759">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="4f44c-1759">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="4f44c-1760">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="4f44c-1760">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="4f44c-1761">Fel som gör att KeyCredentials inte kan skapas upprepade gånger har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="4f44c-1761">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="4f44c-1762">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4f44c-1762">Az.Sql</span></span>
* <span data-ttu-id="4f44c-1763">Lägg till stöd för hyperskalanivån för SQL DB</span><span class="sxs-lookup"><span data-stu-id="4f44c-1763">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="4f44c-1764">Ett fel har åtgärdats där återställningen kunde misslyckas på grund av onödiga inställningsegenskaper i restore-förfrågan</span><span class="sxs-lookup"><span data-stu-id="4f44c-1764">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4f44c-1765">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4f44c-1765">Az.Websites</span></span>
* <span data-ttu-id="4f44c-1766">Rätt exempel i Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="4f44c-1766">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="4f44c-1767">1.3.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="4f44c-1767">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4f44c-1768">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4f44c-1768">Az.Accounts</span></span>
* <span data-ttu-id="4f44c-1769">Uppdatera till den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="4f44c-1769">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="4f44c-1770">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="4f44c-1770">Az.AnalysisServices</span></span>
<span data-ttu-id="4f44c-1771">Allmän tillgänglighet för Az.AnalysisServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1771">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4f44c-1772">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4f44c-1772">Az.Compute</span></span>
* <span data-ttu-id="4f44c-1773">AEM-tillägg: Lägg till stöd för UltraSSD-, P60-, P70- och P80-diskar</span><span class="sxs-lookup"><span data-stu-id="4f44c-1773">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="4f44c-1774">Uppdatera hjälpbeskrivning för Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="4f44c-1774">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="4f44c-1775">Uppdatera hjälpbeskrivning och exempel för Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="4f44c-1775">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4f44c-1776">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4f44c-1776">Az.RecoveryServices</span></span>
<span data-ttu-id="4f44c-1777">Allmän tillgänglighet för Az.RecoveryServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1777">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="4f44c-1778">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4f44c-1778">Az.Resources</span></span>
* <span data-ttu-id="4f44c-1779">Korrigera taggar för resursgrupper</span><span class="sxs-lookup"><span data-stu-id="4f44c-1779">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="4f44c-1780">Mer information här: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="4f44c-1780">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="4f44c-1781">Åtgärda problem där `Get-AzureRmRoleAssignment` inte respekterar -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="4f44c-1781">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="4f44c-1782">Mer information här: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="4f44c-1782">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="4f44c-1783">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4f44c-1783">Az.Sql</span></span>
* <span data-ttu-id="4f44c-1784">Lägga till Get/Set-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="4f44c-1784">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="4f44c-1785">Åtgärda problem där ett nullref-undantag uppstår när du kör SQL-cmdletar och inte är inloggad på ett Azure-konto</span><span class="sxs-lookup"><span data-stu-id="4f44c-1785">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="4f44c-1786">Åtgärda nullref-undantag i Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="4f44c-1786">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="4f44c-1787">1.2.1 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="4f44c-1787">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4f44c-1788">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4f44c-1788">Az.Accounts</span></span>
* <span data-ttu-id="4f44c-1789">Version med rätt version av autentisering</span><span class="sxs-lookup"><span data-stu-id="4f44c-1789">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="4f44c-1790">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="4f44c-1790">Az.AnalysisServices</span></span>
* <span data-ttu-id="4f44c-1791">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="4f44c-1791">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4f44c-1792">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4f44c-1792">Az.RecoveryServices</span></span>
* <span data-ttu-id="4f44c-1793">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="4f44c-1793">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="4f44c-1794">1.2.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="4f44c-1794">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4f44c-1795">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4f44c-1795">Az.Accounts</span></span>
* <span data-ttu-id="4f44c-1796">Lägga till interaktiv autentisering och autentisering med användarnamn/lösenord för endast Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="4f44c-1796">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="4f44c-1797">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="4f44c-1797">Update incorrect online help URLs</span></span>
* <span data-ttu-id="4f44c-1798">Lägga till varningsmeddelande i PS Core för Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="4f44c-1798">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="4f44c-1799">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="4f44c-1799">Az.Aks</span></span>
* <span data-ttu-id="4f44c-1800">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="4f44c-1800">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4f44c-1801">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4f44c-1801">Az.Automation</span></span>
* <span data-ttu-id="4f44c-1802">Stöd för Python 2-runbookflöden har lagts till</span><span class="sxs-lookup"><span data-stu-id="4f44c-1802">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="4f44c-1803">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="4f44c-1803">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="4f44c-1804">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="4f44c-1804">Az.Cdn</span></span>
* <span data-ttu-id="4f44c-1805">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="4f44c-1805">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4f44c-1806">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4f44c-1806">Az.Compute</span></span>
* <span data-ttu-id="4f44c-1807">Lägga till cmdleten Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="4f44c-1807">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="4f44c-1808">Lägga till TempDisk-parameter i Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4f44c-1808">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="4f44c-1809">Korrigera varningsmeddelande för New-AzVM</span><span class="sxs-lookup"><span data-stu-id="4f44c-1809">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="4f44c-1810">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="4f44c-1810">Az.ContainerRegistry</span></span>
* <span data-ttu-id="4f44c-1811">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="4f44c-1811">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4f44c-1812">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4f44c-1812">Az.DataFactory</span></span>
* <span data-ttu-id="4f44c-1813">ADF .Net SDK-versionen har uppdaterats till 3.0.0</span><span class="sxs-lookup"><span data-stu-id="4f44c-1813">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4f44c-1814">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4f44c-1814">Az.DataLakeStore</span></span>
* <span data-ttu-id="4f44c-1815">Åtgärda problem med ADLS-slutpunkt vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="4f44c-1815">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="4f44c-1816">Mer information här: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="4f44c-1816">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="4f44c-1817">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="4f44c-1817">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="4f44c-1818">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="4f44c-1818">Az.IotHub</span></span>
* <span data-ttu-id="4f44c-1819">Lägga till kodningsformat i cmdleten Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1819">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="4f44c-1820">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4f44c-1820">Az.KeyVault</span></span>
* <span data-ttu-id="4f44c-1821">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="4f44c-1821">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4f44c-1822">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4f44c-1822">Az.Network</span></span>
* <span data-ttu-id="4f44c-1823">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="4f44c-1823">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="4f44c-1824">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4f44c-1824">Az.Resources</span></span>
* <span data-ttu-id="4f44c-1825">Åtgärda felaktiga exempel i referensdokumentationen ”New-AzADAppCredential” och ”New-AzADSpCredential”</span><span class="sxs-lookup"><span data-stu-id="4f44c-1825">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="4f44c-1826">Åtgärda problem där sökvägen för parametern ”-TemplateFile” inte omvandlas innan cmdletarna för distribution i resursgruppen körs</span><span class="sxs-lookup"><span data-stu-id="4f44c-1826">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="4f44c-1827">Az.Resources: Korrigera dokumentationen om standardvärdet för New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="4f44c-1827">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="4f44c-1828">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="4f44c-1828">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="4f44c-1829">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="4f44c-1829">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="4f44c-1830">Åtgärda formateringsproblemet med objektet ”PSResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="4f44c-1830">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="4f44c-1831">Mer information här: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="4f44c-1831">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="4f44c-1832">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4f44c-1832">Az.ServiceFabric</span></span>
* <span data-ttu-id="4f44c-1833">Återställ när ett certifikat läggs till i en Virtual Machine Scale Sets-modell men ett undantag genereras. Detta har gjorts för att åtgärda följande fel: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="4f44c-1833">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="4f44c-1834">Korrigera några felmeddelanden.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1834">Fix some error messages.</span></span>
* <span data-ttu-id="4f44c-1835">Korrigering av skapande av kluster med ARM-mall som är standard för New-AzServiceFabriCluster som inte fungerade med migrering till Az.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1835">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="4f44c-1836">Korrigering av tilläggning av kluster/programcertifikat så att endast VM Scale Sets som motsvarar klustret läggs till genom att kontrollera ID för klustret i tillägget.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1836">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="4f44c-1837">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="4f44c-1837">Az.SignalR</span></span>
* <span data-ttu-id="4f44c-1838">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="4f44c-1838">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="4f44c-1839">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4f44c-1839">Az.Sql</span></span>
* <span data-ttu-id="4f44c-1840">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="4f44c-1840">Update incorrect online help URLs</span></span>
* <span data-ttu-id="4f44c-1841">Uppdaterad parameterbeskrivning för LicenseType-parameter med möjliga värden</span><span class="sxs-lookup"><span data-stu-id="4f44c-1841">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="4f44c-1842">Korrigering för att uppdatera hanterad instansidentitet som inte fungerar när det är den enda uppdaterade egenskapen</span><span class="sxs-lookup"><span data-stu-id="4f44c-1842">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="4f44c-1843">Stöd för anpassad sortering på hanterad instans</span><span class="sxs-lookup"><span data-stu-id="4f44c-1843">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4f44c-1844">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4f44c-1844">Az.Storage</span></span>
* <span data-ttu-id="4f44c-1845">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="4f44c-1845">Update incorrect online help URLs</span></span>
* <span data-ttu-id="4f44c-1846">Tillhandahåll detaljerat felmeddelande när en användare försöker hämta/konfigurera klassisk loggning/mått på ett Premium Storage-konto eftersom Premium Storage-kontot inte har stöd för klassisk loggning/mått.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1846">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="4f44c-1847">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="4f44c-1847">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="4f44c-1848">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="4f44c-1848">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="4f44c-1849">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="4f44c-1849">Az.TrafficManager</span></span>
* <span data-ttu-id="4f44c-1850">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="4f44c-1850">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4f44c-1851">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4f44c-1851">Az.Websites</span></span>
* <span data-ttu-id="4f44c-1852">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="4f44c-1852">Update incorrect online help URLs</span></span>
* <span data-ttu-id="4f44c-1853">Korrigerar ”New-AzWebAppSSLBinding” så att certifikatet laddas upp till rätt resursgrupp och plats om appen finns i en ASE.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1853">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="4f44c-1854">Korrigerar ”New-AzWebAppSSLBinding” så att taggarna inte skrivs över på en bindning av ett SSL-certifikat till en app</span><span class="sxs-lookup"><span data-stu-id="4f44c-1854">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="4f44c-1855">1.1.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="4f44c-1855">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4f44c-1856">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4f44c-1856">Az.Accounts</span></span>
* <span data-ttu-id="4f44c-1857">Lade till omfattningen ”Lokal” till Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="4f44c-1857">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4f44c-1858">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4f44c-1858">Az.Compute</span></span>
* <span data-ttu-id="4f44c-1859">Namn är nu valfritt i ID-parametern för Restart/Start/Stop/Remove/Set-AzVM och Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="4f44c-1859">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="4f44c-1860">Uppdaterade beskrivningen av ID i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="4f44c-1860">Updated the description of ID in help files</span></span>
* <span data-ttu-id="4f44c-1861">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4f44c-1861">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4f44c-1862">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4f44c-1862">Az.DataLakeStore</span></span>
* <span data-ttu-id="4f44c-1863">Uppdatera sdk-versionen av dataplanet till 1.1.14 för SDK-korrigeringar.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1863">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="4f44c-1864">Korrigerade hanteringen av negativ accesstime och modificationtime för getfilestatus och liststatus; korrigera asynkront annulleringstoken</span><span class="sxs-lookup"><span data-stu-id="4f44c-1864">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="4f44c-1865">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="4f44c-1865">Az.EventGrid</span></span>
* <span data-ttu-id="4f44c-1866">Uppdaterat för användning av API-versionen 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1866">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="4f44c-1867">Uppdaterade följande cmdletar för att stödja nytt scenario i API-versionen 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="4f44c-1867">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="4f44c-1868">New-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="4f44c-1868">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="4f44c-1869">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="4f44c-1869">Event Time-To-Live,</span></span>
        - <span data-ttu-id="4f44c-1870">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="4f44c-1870">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="4f44c-1871">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1871">Dead letter endpoint.</span></span>
    - <span data-ttu-id="4f44c-1872">Update-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="4f44c-1872">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="4f44c-1873">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="4f44c-1873">Event Time-To-Live,</span></span>
        - <span data-ttu-id="4f44c-1874">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="4f44c-1874">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="4f44c-1875">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1875">Dead letter endpoint.</span></span>
* <span data-ttu-id="4f44c-1876">Lade till nya enum-värden (storageQueue och hybridConnection) för alternativet EndpointType i cmdletarna New-AzureRmEventGridSubscription och Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1876">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="4f44c-1877">Visa varningsmeddelanden om skapande eller uppdatering av händelseprenumerationen förväntas medföra manuell åtgärd från användaren.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1877">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="4f44c-1878">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="4f44c-1878">Az.IotHub</span></span>
* <span data-ttu-id="4f44c-1879">Har uppdaterats till den senaste versionen av SDK:n lotHub</span><span class="sxs-lookup"><span data-stu-id="4f44c-1879">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="4f44c-1880">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="4f44c-1880">Az.LogicApp</span></span>
* <span data-ttu-id="4f44c-1881">Get-AzLogicApp visar en lista över alla som inte har angivet namn</span><span class="sxs-lookup"><span data-stu-id="4f44c-1881">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="4f44c-1882">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4f44c-1882">Az.Resources</span></span>
* <span data-ttu-id="4f44c-1883">Åtgärdade problem med parameteruppsättningen när parametrarna -ODataQuery och -ResourceId anges för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="4f44c-1883">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="4f44c-1884">Mer information här: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="4f44c-1884">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="4f44c-1885">Åtgärdade hantering av parametern -Custom i New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4f44c-1885">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="4f44c-1886">Korrigerade stavfel i New-AzDeployment-dokumentationen</span><span class="sxs-lookup"><span data-stu-id="4f44c-1886">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="4f44c-1887">Gjorde parametern -MailNickname obligatorisk för New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="4f44c-1887">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="4f44c-1888">Mer information här: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="4f44c-1888">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="4f44c-1889">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="4f44c-1889">Az.SignalR</span></span>
* <span data-ttu-id="4f44c-1890">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4f44c-1890">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="4f44c-1891">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4f44c-1891">Az.Sql</span></span>
* <span data-ttu-id="4f44c-1892">Konverterade lagringshanteringsklientens beroende av den normala SDK-implementeringen.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1892">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4f44c-1893">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4f44c-1893">Az.Storage</span></span>
* <span data-ttu-id="4f44c-1894">Angav StorageAccountName för lagringskontext som det verkliga namnet på lagringskontot när det skapas med Sas Token, OAuth eller Anonymous</span><span class="sxs-lookup"><span data-stu-id="4f44c-1894">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="4f44c-1895">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="4f44c-1895">New-AzStorageContext</span></span>
* <span data-ttu-id="4f44c-1896">Skapade Sas Token för Blob Snapshot-objekt med parametern -FullUri, åtgärdade den returnerade URI:n så att den blir URI för ögonblicksbild</span><span class="sxs-lookup"><span data-stu-id="4f44c-1896">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="4f44c-1897">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="4f44c-1897">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4f44c-1898">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4f44c-1898">Az.Websites</span></span>
* <span data-ttu-id="4f44c-1899">Åtgärdade en bugg i datumparsningen i Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="4f44c-1899">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="4f44c-1900">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4f44c-1900">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="4f44c-1901">1.0.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="4f44c-1901">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="4f44c-1902">Allmänt</span><span class="sxs-lookup"><span data-stu-id="4f44c-1902">General</span></span>

- <span data-ttu-id="4f44c-1903">Allmän tillgänglighet för Az-modulen</span><span class="sxs-lookup"><span data-stu-id="4f44c-1903">General Availability of Az Module</span></span>
- <span data-ttu-id="4f44c-1904">Onlinehjälp för varje modul</span><span class="sxs-lookup"><span data-stu-id="4f44c-1904">Online help for each module</span></span>
- <span data-ttu-id="4f44c-1905">Mer information och en översikt finns på [Az-informationssidan](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="4f44c-1905">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="4f44c-1906">Information om hur du migrerar från AzureRM finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="4f44c-1906">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="4f44c-1907">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4f44c-1907">Az.Accounts</span></span>
- <span data-ttu-id="4f44c-1908">Har ändrats från Az.Profile</span><span class="sxs-lookup"><span data-stu-id="4f44c-1908">Changed from Az.Profile</span></span>
- <span data-ttu-id="4f44c-1909">Fasta tabellformat för profil- och kontexttyper</span><span class="sxs-lookup"><span data-stu-id="4f44c-1909">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="4f44c-1910">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4f44c-1910">Az.ApiManagement</span></span>
- <span data-ttu-id="4f44c-1911">Korrigeringar för #7002</span><span class="sxs-lookup"><span data-stu-id="4f44c-1911">Fixes for #7002</span></span>
- <span data-ttu-id="4f44c-1912">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="4f44c-1912">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="4f44c-1913">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="4f44c-1913">Az.Batch</span></span>
- <span data-ttu-id="4f44c-1914">Lade till möjligheten att se vilken version av Azure Batch Node Agent som körs på var och en av de virtuella datorerna i en pool, via den nya egenskapen `NodeAgentInformation` på `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1914">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="4f44c-1915">Standarden `Caching` för `PSDataDisk` är nu `ReadWrite` i stället för `None`.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1915">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="4f44c-1916">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="4f44c-1916">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="4f44c-1917">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="4f44c-1917">Az.Billing</span></span>
- <span data-ttu-id="4f44c-1918">Kombinerar cmdletarna för fakturering, förbrukning och UsageAggregates. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="4f44c-1918">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="4f44c-1919">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="4f44c-1919">Az.CognitivServices</span></span>
- <span data-ttu-id="4f44c-1920">Lade till kompletterare för SkuName och Typem som är tillgängliga i New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="4f44c-1920">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="4f44c-1921">Tog bort parameteruppsättningen GetSkusWithAccountParamSetName från Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="4f44c-1921">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="4f44c-1922">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="4f44c-1922">Az.ContainerInstance</span></span>
- <span data-ttu-id="4f44c-1923">Stöd för ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="4f44c-1923">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="4f44c-1924">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="4f44c-1924">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="4f44c-1925">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="4f44c-1925">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="4f44c-1926">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4f44c-1926">Az.DataLakeStore</span></span>
- <span data-ttu-id="4f44c-1927">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="4f44c-1927">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="4f44c-1928">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4f44c-1928">Az.Monitor</span></span>
- <span data-ttu-id="4f44c-1929">Döpte om Az.Insights till Az.Monitor och andra mindre icke-bakåtkompatibla ändringar. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="4f44c-1929">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="4f44c-1930">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4f44c-1930">Az.KeyVault</span></span>
- <span data-ttu-id="4f44c-1931">Tog bort den inaktuella egenskapen PurgeDisabled från utdatatyper</span><span class="sxs-lookup"><span data-stu-id="4f44c-1931">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="4f44c-1932">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="4f44c-1932">Az.MachineLearning</span></span>
- <span data-ttu-id="4f44c-1933">Inkluderade cmdletarna från modulen Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="4f44c-1933">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="4f44c-1934">Az.Media</span><span class="sxs-lookup"><span data-stu-id="4f44c-1934">Az.Media</span></span>
- <span data-ttu-id="4f44c-1935">Tog bort inaktuella -Tags-alias från New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="4f44c-1935">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="4f44c-1936">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4f44c-1936">Az.Network</span></span>
<span data-ttu-id="4f44c-1937">Stöd har lagts till för konfiguration av RewriteRuleSets i Application Gateway</span><span class="sxs-lookup"><span data-stu-id="4f44c-1937">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="4f44c-1938">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="4f44c-1938">New cmdlets added:</span></span>
        - <span data-ttu-id="4f44c-1939">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4f44c-1939">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="4f44c-1940">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4f44c-1940">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="4f44c-1941">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4f44c-1941">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="4f44c-1942">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4f44c-1942">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="4f44c-1943">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4f44c-1943">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="4f44c-1944">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="4f44c-1944">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="4f44c-1945">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="4f44c-1945">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="4f44c-1946">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="4f44c-1946">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="4f44c-1947">Cmdletar har uppdaterats med den valfria parametern -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4f44c-1947">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="4f44c-1948">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4f44c-1948">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="4f44c-1949">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="4f44c-1949">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="4f44c-1950">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="4f44c-1950">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="4f44c-1951">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4f44c-1951">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="4f44c-1952">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4f44c-1952">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="4f44c-1953">New-AzureRmApplicationGatewayUrlPathMapConfig har lagt till KeyVault-stöd för Application Gateway med Identity.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1953">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="4f44c-1954">Cmdletar har uppdaterats med den valfria parametern -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="4f44c-1954">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="4f44c-1955">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="4f44c-1955">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="4f44c-1956">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="4f44c-1956">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="4f44c-1957">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="4f44c-1957">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="4f44c-1958">Cmdleten New-AzApplicationGateway har uppdaterats med den valfria parametern -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="4f44c-1958">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="4f44c-1959">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="4f44c-1959">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="4f44c-1960">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="4f44c-1960">Az.OperationalInsights</span></span>
- <span data-ttu-id="4f44c-1961">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="4f44c-1961">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="4f44c-1962">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="4f44c-1962">Az.Profile</span></span>
- <span data-ttu-id="4f44c-1963">Modulnamnet har ändrats till Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4f44c-1963">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="4f44c-1964">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4f44c-1964">Az.RecoveryServices</span></span>
- <span data-ttu-id="4f44c-1965">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="4f44c-1965">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="4f44c-1966">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4f44c-1966">Az.Resources</span></span>
- <span data-ttu-id="4f44c-1967">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="4f44c-1967">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="4f44c-1968">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4f44c-1968">Az.ServiceFabric</span></span>
- <span data-ttu-id="4f44c-1969">Stöd för specificering av certifikat efter eget namn och tumavtryck</span><span class="sxs-lookup"><span data-stu-id="4f44c-1969">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="4f44c-1970">Information om fler icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="4f44c-1970">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="4f44c-1971">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="4f44c-1971">Az.SIgnalR</span></span>
- <span data-ttu-id="4f44c-1972">Allmän tillgänglighet för PowerShell-cmdletar för SIgnalR</span><span class="sxs-lookup"><span data-stu-id="4f44c-1972">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="4f44c-1973">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4f44c-1973">Az.Sql</span></span>
- <span data-ttu-id="4f44c-1974">Lade till de nya identifieringstyperna Data_Exfiltration och Unsafe_Action i Threat Detection-cmdletar</span><span class="sxs-lookup"><span data-stu-id="4f44c-1974">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="4f44c-1975">Uppdaterade dokumentationsexempel för Sql Auditing-cmdletar</span><span class="sxs-lookup"><span data-stu-id="4f44c-1975">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="4f44c-1976">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="4f44c-1976">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="4f44c-1977">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4f44c-1977">Az.Storage</span></span>
- <span data-ttu-id="4f44c-1978">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="4f44c-1978">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="4f44c-1979">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4f44c-1979">Az.Websites</span></span>
- <span data-ttu-id="4f44c-1980">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="4f44c-1980">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="4f44c-1981">0.7.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="4f44c-1981">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="4f44c-1982">Allmänt</span><span class="sxs-lookup"><span data-stu-id="4f44c-1982">General</span></span>

* <span data-ttu-id="4f44c-1983">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="4f44c-1983">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="4f44c-1984">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4f44c-1984">Az.Compute</span></span>

* <span data-ttu-id="4f44c-1985">Lade till stöd för UltraSSD och Galleriavbildningar i de enkla parameteruppsättningarna för `New-AzVm(ss)`-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1985">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="4f44c-1986">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4f44c-1986">Az.DataLakeStore</span></span>

* <span data-ttu-id="4f44c-1987">Åtgärdade avslutande snedstreck i domänen för adls-konto</span><span class="sxs-lookup"><span data-stu-id="4f44c-1987">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="4f44c-1988">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="4f44c-1988">Az.FrontDoor</span></span>

* <span data-ttu-id="4f44c-1989">Brutna länkar korrigerades</span><span class="sxs-lookup"><span data-stu-id="4f44c-1989">Fixed some broken links</span></span>
    - <span data-ttu-id="4f44c-1990">I artiklarna New-AzureRmFrontDoor och Set-AzureRmFrontDoor artiklar korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1990">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="4f44c-1991">I artikeln New-AzureRmFrontDoorManagedRuleObject korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1991">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="4f44c-1992">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4f44c-1992">Az.RecoveryServices</span></span>

* <span data-ttu-id="4f44c-1993">Lade till valideringar på klientsidan för Azure-filresurs med återställningsåtgärder.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1993">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="4f44c-1994">Gjorde storageAccountName och storageAccountResourceGroupName valfritt för afs-återställning.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1994">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="4f44c-1995">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4f44c-1995">Az.Resources</span></span>

* <span data-ttu-id="4f44c-1996">Korrigering för https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="4f44c-1996">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="4f44c-1997">Uppdaterade Get-AzureRmRoleAssignment så att prenumerationsomfattningen används om den anges vid begäran om klassiska administratörer.</span><span class="sxs-lookup"><span data-stu-id="4f44c-1997">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="4f44c-1998">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4f44c-1998">Az.Sql</span></span>

* <span data-ttu-id="4f44c-1999">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="4f44c-1999">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="4f44c-2000">Korrigerade ett problem med Get-AzureRmSqlDatabaseVulnerabilityAssessment med DotNet-kärna</span><span class="sxs-lookup"><span data-stu-id="4f44c-2000">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="4f44c-2001">Ändrade dokumentationen för hjälpmeddelanden som rör SQL Auditing-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="4f44c-2001">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="4f44c-2002">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4f44c-2002">Az.Storage</span></span>

* <span data-ttu-id="4f44c-2003">Lade till -EnableHierarchicalNamespace i New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4f44c-2003">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="4f44c-2004">Åtgärdade problemet med att cmdleten Copy File inte kunde återanvända källkontexten på målet om inte -DestContext angetts</span><span class="sxs-lookup"><span data-stu-id="4f44c-2004">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="4f44c-2005">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="4f44c-2005">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="4f44c-2006">Stöd för statisk webbplatskonfiguration</span><span class="sxs-lookup"><span data-stu-id="4f44c-2006">Support Static Website configuration</span></span>
    - <span data-ttu-id="4f44c-2007">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="4f44c-2007">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="4f44c-2008">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="4f44c-2008">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="4f44c-2009">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4f44c-2009">Az.Websites</span></span>

* <span data-ttu-id="4f44c-2010">Set-AzureRmWebApp och Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4f44c-2010">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="4f44c-2011">Ny parameter (-AzureStoragePath) har lagts till för att ange att Azure Storage-sökvägar ska monteras i containerappar i Windows och Linux.</span><span class="sxs-lookup"><span data-stu-id="4f44c-2011">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="4f44c-2012">Använder utdata från den nya cmdleten New-AzureRmWebAppAzureStoragePath som en parameter för att ange sökvägar för Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="4f44c-2012">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="4f44c-2013">0.6.1 – november 2018</span><span class="sxs-lookup"><span data-stu-id="4f44c-2013">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="4f44c-2014">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4f44c-2014">Az.ApiManagement</span></span>
* <span data-ttu-id="4f44c-2015">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="4f44c-2015">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="4f44c-2016">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4f44c-2016">Az.Automation</span></span>
* <span data-ttu-id="4f44c-2017">Swagger baserade Azure Automation-cmdletar</span><span class="sxs-lookup"><span data-stu-id="4f44c-2017">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="4f44c-2018">Cmdletar för Uppdateringshantering har lagts till</span><span class="sxs-lookup"><span data-stu-id="4f44c-2018">Added Update Management cmdlets</span></span>
* <span data-ttu-id="4f44c-2019">Cmdletar för källkontroll har lagts till</span><span class="sxs-lookup"><span data-stu-id="4f44c-2019">Added Source Control cmdlets</span></span>
* <span data-ttu-id="4f44c-2020">Remove-AzureRmAutomationHybridWorkerGroup-cmdlet har lagts till</span><span class="sxs-lookup"><span data-stu-id="4f44c-2020">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="4f44c-2021">Kommandot för DSC-registreringsnod har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="4f44c-2021">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="4f44c-2022">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4f44c-2022">Az.Compute</span></span>
* <span data-ttu-id="4f44c-2023">Problem med SystemAssigned-identitet har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="4f44c-2023">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="4f44c-2024">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="4f44c-2024">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="4f44c-2025">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="4f44c-2025">Az.ContainerInstance</span></span>
* <span data-ttu-id="4f44c-2026">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="4f44c-2026">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="4f44c-2027">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="4f44c-2027">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="4f44c-2028">uppdatera exempelbeskrivningen för marketplace-cmdletar</span><span class="sxs-lookup"><span data-stu-id="4f44c-2028">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="4f44c-2029">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4f44c-2029">Az.Network</span></span>
* <span data-ttu-id="4f44c-2030">Cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomErreller Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="4f44c-2030">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="4f44c-2031">ICMP tillbaka till stöd för Azure Firewall-nätverksprotokoll har lagts till</span><span class="sxs-lookup"><span data-stu-id="4f44c-2031">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="4f44c-2032">Uppdatera cmdlet Test-AzureRmNetworkWatcherConnectivity, lägga till verifiering av mål-id, adress och port.</span><span class="sxs-lookup"><span data-stu-id="4f44c-2032">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="4f44c-2033">Åtgärda problem med minnesanvändning i VirtualNetwork-karta</span><span class="sxs-lookup"><span data-stu-id="4f44c-2033">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="4f44c-2034">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="4f44c-2034">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="4f44c-2035">Åtgärda för att ändra principen för en skyddad fildelning.</span><span class="sxs-lookup"><span data-stu-id="4f44c-2035">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="4f44c-2036">Tidszonsprincipen har konverterats till versaler.</span><span class="sxs-lookup"><span data-stu-id="4f44c-2036">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="4f44c-2037">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="4f44c-2037">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="4f44c-2038">Exempel i New-AzureRmRecoveryServicesAsrProtectableItem har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="4f44c-2038">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="4f44c-2039">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="4f44c-2039">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="4f44c-2040">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="4f44c-2040">Az.Relay</span></span>
* <span data-ttu-id="4f44c-2041">Valfri parameter -KeyValue till New-AzureRmRelayKey cmdlet har lagts till, vilket gör det möjligt för användare att tillhandahålla KeyValue.</span><span class="sxs-lookup"><span data-stu-id="4f44c-2041">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="4f44c-2042">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4f44c-2042">Az.Resources</span></span>
* <span data-ttu-id="4f44c-2043">Uppdatera hjälpdokumentation för resursidentitet kopplad till parametrar i `New-AzureRmPolicyAssignment` och `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="4f44c-2043">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="4f44c-2044">Lägg till ett exempel för New-AzureRmPolicyDefinition som använder -Metadata</span><span class="sxs-lookup"><span data-stu-id="4f44c-2044">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="4f44c-2045">Korrigera så att skiftläge behålls i taggnycklar i NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="4f44c-2045">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="4f44c-2046">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4f44c-2046">Az.ServiceFabric</span></span>
* <span data-ttu-id="4f44c-2047">Lägg till utfasningsmeddelanden för kommande icke-kompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="4f44c-2047">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="4f44c-2048">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4f44c-2048">Az.Sql</span></span>
* <span data-ttu-id="4f44c-2049">Nya cmdletar för CRUD-åtgärder på Azure Sql Database-hanterad instans och Azure Sql-hanterad databas</span><span class="sxs-lookup"><span data-stu-id="4f44c-2049">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="4f44c-2050">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="4f44c-2050">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="4f44c-2051">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="4f44c-2051">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="4f44c-2052">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="4f44c-2052">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="4f44c-2053">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="4f44c-2053">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="4f44c-2054">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="4f44c-2054">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="4f44c-2055">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="4f44c-2055">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="4f44c-2056">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="4f44c-2056">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="4f44c-2057">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="4f44c-2057">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="4f44c-2058">Hantering av utökad granskningsprincip på en server eller en databas har aktiverats.</span><span class="sxs-lookup"><span data-stu-id="4f44c-2058">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="4f44c-2059">Ny parameter (PredicateExpression) har lagts till för att aktivera filtrering av granskningsloggar.</span><span class="sxs-lookup"><span data-stu-id="4f44c-2059">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="4f44c-2060">Cmdletar har ändrats så att de använder SQL-klienter i stället för äldre klienter.</span><span class="sxs-lookup"><span data-stu-id="4f44c-2060">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="4f44c-2061">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="4f44c-2061">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="4f44c-2062">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="4f44c-2062">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="4f44c-2063">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="4f44c-2063">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="4f44c-2064">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="4f44c-2064">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="4f44c-2065">Problem med att använda Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings med lagringskontots namnparameter har korrigerats</span><span class="sxs-lookup"><span data-stu-id="4f44c-2065">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="4f44c-2066">0.5.0 – november 2018</span><span class="sxs-lookup"><span data-stu-id="4f44c-2066">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="4f44c-2067">Allmänt</span><span class="sxs-lookup"><span data-stu-id="4f44c-2067">General</span></span>
* <span data-ttu-id="4f44c-2068">Lade till resurskompletterare till många kärn-cmdletar – dessa gör att du kan stega genom befintliga resursnamn med TABB vid interaktiva anrop till cmdletar</span><span class="sxs-lookup"><span data-stu-id="4f44c-2068">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="4f44c-2069">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="4f44c-2069">Az.Profile</span></span>
* <span data-ttu-id="4f44c-2070">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="4f44c-2070">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="4f44c-2071">Bytte namn på parametern TenantId i cmdleten Connect-AzAccount till Tenant och lade till ett alias för TenantId</span><span class="sxs-lookup"><span data-stu-id="4f44c-2071">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="4f44c-2072">Uppdaterade TenantId-beskrivningen för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="4f44c-2072">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="4f44c-2073">Åtgärda felmeddelande för misslyckad inloggning när du tillhandahåller klientdomän</span><span class="sxs-lookup"><span data-stu-id="4f44c-2073">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="4f44c-2074">Åtgärda problem med att kontextnamn hamnar i konflikt för konton utan prenumerationer i klientorganisationen</span><span class="sxs-lookup"><span data-stu-id="4f44c-2074">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="4f44c-2075">Åtgärda problem med DataLake-slutpunkter vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="4f44c-2075">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="4f44c-2076">Åtgärdade problem med att Disconnect-AzAccount kastades om den inte anslöts</span><span class="sxs-lookup"><span data-stu-id="4f44c-2076">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="4f44c-2077">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="4f44c-2077">Az.CognitiveServices</span></span>
* <span data-ttu-id="4f44c-2078">Lade till åtgärden Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="4f44c-2078">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4f44c-2079">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4f44c-2079">Az.Compute</span></span>
* <span data-ttu-id="4f44c-2080">Lade till cmdletarna Add-AzVmssVMDataDisk och Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="4f44c-2080">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="4f44c-2081">Get-AzVMImage visar AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="4f44c-2081">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="4f44c-2082">Åtgärdade att värdena för alternativen SetAzVMChefExtension -BootstrapOptions och -JsonAttribute inte angavs i json-format.</span><span class="sxs-lookup"><span data-stu-id="4f44c-2082">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4f44c-2083">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4f44c-2083">Az.DataLakeStore</span></span>
* <span data-ttu-id="4f44c-2084">Uppdatera DataLake-paketet till 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="4f44c-2084">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="4f44c-2085">Lägg till standardsamtidighet för flertrådade åtgärder.</span><span class="sxs-lookup"><span data-stu-id="4f44c-2085">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="4f44c-2086">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="4f44c-2086">Az.Insights</span></span>
* <span data-ttu-id="4f44c-2087">Åtgärdade problem #7267 (autoskalningsområde)</span><span class="sxs-lookup"><span data-stu-id="4f44c-2087">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="4f44c-2088">Problem med att uppräknade parametrar inte ställdes in ordentligt när du skapade en ny autoskalningsregel (de ställdes alltid in med standardvärdet).</span><span class="sxs-lookup"><span data-stu-id="4f44c-2088">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="4f44c-2089">Åtgärdade problem #7513 [Insights] Set-AzDiagnosticSetting kräver uttrycklig specifikation av kategorier när inställningar skapas</span><span class="sxs-lookup"><span data-stu-id="4f44c-2089">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="4f44c-2090">Nu kräver inte cmdleten uttrycklig anvisning av kategorierna för att aktiveras under skapande, d.v.s. den fungerar enligt beskrivning</span><span class="sxs-lookup"><span data-stu-id="4f44c-2090">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4f44c-2091">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4f44c-2091">Az.Network</span></span>
* <span data-ttu-id="4f44c-2092">PeeringType ändrades till en obligatorisk parameter för följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="4f44c-2092">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="4f44c-2093">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="4f44c-2093">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="4f44c-2094">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="4f44c-2094">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="4f44c-2095">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="4f44c-2095">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="4f44c-2096">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="4f44c-2096">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="4f44c-2097">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="4f44c-2097">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="4f44c-2098">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="4f44c-2098">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="4f44c-2099">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="4f44c-2099">Az.PolicyInsights</span></span>
* <span data-ttu-id="4f44c-2100">Cmdletar för principreparation har lagts till</span><span class="sxs-lookup"><span data-stu-id="4f44c-2100">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="4f44c-2101">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4f44c-2101">Az.Resources</span></span>
* <span data-ttu-id="4f44c-2102">Korrigering för https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="4f44c-2102">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="4f44c-2103">Tillåt att resurser listas med parametern -ResourceId för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="4f44c-2103">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="4f44c-2104">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="4f44c-2104">Az.ServiceBus</span></span>
* <span data-ttu-id="4f44c-2105">Skrivskyddad MigrationState-egenskap har lagts till i PSServiceBusMigrationConfigurationAttributes, som hjälper till att hålla koll på migreringstillståndet.</span><span class="sxs-lookup"><span data-stu-id="4f44c-2105">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="4f44c-2106">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4f44c-2106">Az.ServiceFabric</span></span>
* <span data-ttu-id="4f44c-2107">Åtgärda att lägga till certifikat till Linux-Vmss.</span><span class="sxs-lookup"><span data-stu-id="4f44c-2107">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="4f44c-2108">Åtgärdade Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="4f44c-2108">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="4f44c-2109">Använd rätt tumavtryck från nya certifikat (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="4f44c-2109">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="4f44c-2110">Visa undantag korrekt (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="4f44c-2110">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="4f44c-2111">Åtgärdade Update-AzServiceFabricDurability så att klusterkonfigurationen uppdateras innan Vmss-åtgärden CreateOrUpdate påbörjas.</span><span class="sxs-lookup"><span data-stu-id="4f44c-2111">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="4f44c-2112">0.4.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="4f44c-2112">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="4f44c-2113">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="4f44c-2113">Az.Profile</span></span>
* <span data-ttu-id="4f44c-2114">Åtgärdade problemet med Get-AzSubscription i CloudShell</span><span class="sxs-lookup"><span data-stu-id="4f44c-2114">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="4f44c-2115">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="4f44c-2115">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4f44c-2116">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4f44c-2116">Az.Compute</span></span>
* <span data-ttu-id="4f44c-2117">Nya storlekar lades till i listan över godkända VM-storlekar för vilka accelererat nätverk kommer att aktiveras vid användning av den enkla parameteruppsättningen för New-AzVm</span><span class="sxs-lookup"><span data-stu-id="4f44c-2117">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="4f44c-2118">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="4f44c-2118">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4f44c-2119">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4f44c-2119">Az.DataLakeStore</span></span>
* <span data-ttu-id="4f44c-2120">Lägger till stöd för regler för virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="4f44c-2120">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="4f44c-2121">Get-AzDataLakeStoreVirtualNetworkRule: Hämtar eller listar regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="4f44c-2121">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="4f44c-2122">Add-AzDataLakeStoreVirtualNetworkRule: Lägger till en regel för virtuellt nätverk i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="4f44c-2122">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="4f44c-2123">Set-AzDataLakeStoreVirtualNetworkRule: Ändrar den angivna regeln för virtuellt nätverk i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="4f44c-2123">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="4f44c-2124">Remove-AzDataLakeStoreVirtualNetworkRule: Tar bort en regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="4f44c-2124">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4f44c-2125">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4f44c-2125">Az.Network</span></span>
* <span data-ttu-id="4f44c-2126">Skicka protokollvärdet till serverdelen för att uppdatera cmdleten Test-AzNetworkWatcherConnectivity.</span><span class="sxs-lookup"><span data-stu-id="4f44c-2126">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="4f44c-2127">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="4f44c-2127">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="4f44c-2128">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4f44c-2128">Az.Resources</span></span>
* <span data-ttu-id="4f44c-2129">Åtgärdade problem där Get-AzRoleDefinition genererar ett oläsligt undantag (när standardprofilen inte innehåller någon prenumeration och ingen omfattning har angetts) genom att lägga till ett beskrivande undantag i scenariot.</span><span class="sxs-lookup"><span data-stu-id="4f44c-2129">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="4f44c-2130">Ställ in ”RoleDefinitionNameParameterSet” som standardparameteruppsättning.</span><span class="sxs-lookup"><span data-stu-id="4f44c-2130">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="4f44c-2131">0.3.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="4f44c-2131">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="4f44c-2132">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="4f44c-2132">Azure.Storage</span></span>
* <span data-ttu-id="4f44c-2133">Åtgärda fel där Kopiera blob/fil inte kopierar metadata när målplatsen har ett problem med metadata</span><span class="sxs-lookup"><span data-stu-id="4f44c-2133">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="4f44c-2134">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="4f44c-2134">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="4f44c-2135">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="4f44c-2135">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="4f44c-2136">Stöd för att hämta användningsinformation om en Storage-resurs för en specifik plats och för att lägga till ett varningsmeddelande för att hämta användningsinformation om en global Storage-resurs är inaktuellt.</span><span class="sxs-lookup"><span data-stu-id="4f44c-2136">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="4f44c-2137">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="4f44c-2137">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="4f44c-2138">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="4f44c-2138">Az.CognitiveServices</span></span>
* <span data-ttu-id="4f44c-2139">Stöd för Get-AzCognitiveServicesAccountSkus utan ett befintligt konto.</span><span class="sxs-lookup"><span data-stu-id="4f44c-2139">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4f44c-2140">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4f44c-2140">Az.Compute</span></span>
* <span data-ttu-id="4f44c-2141">Åtgärdade fel där Get-AzVM -ResourceGroupName <rg> returnerar fler än 50 resultat om det behövs</span><span class="sxs-lookup"><span data-stu-id="4f44c-2141">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="4f44c-2142">Lade till ett exempel för SimpleParameterSet i hjälpen för cmdleten New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="4f44c-2142">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="4f44c-2143">Ett stavfel i förloppsmeddelandet för Azure Disk Encryption har korrigerats</span><span class="sxs-lookup"><span data-stu-id="4f44c-2143">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="4f44c-2144">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="4f44c-2144">Az.DataFactoryV2</span></span>
* <span data-ttu-id="4f44c-2145">ADF .Net SDK-versionen har uppdaterats till 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="4f44c-2145">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4f44c-2146">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4f44c-2146">Az.Network</span></span>
* <span data-ttu-id="4f44c-2147">Funktionalitet för NetworkProfile har lagts till.</span><span class="sxs-lookup"><span data-stu-id="4f44c-2147">Added NetworkProfile functionality.</span></span> <span data-ttu-id="4f44c-2148">nya cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="4f44c-2148">new cmdlets added</span></span>
    - <span data-ttu-id="4f44c-2149">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="4f44c-2149">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="4f44c-2150">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="4f44c-2150">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="4f44c-2151">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="4f44c-2151">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="4f44c-2152">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="4f44c-2152">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="4f44c-2153">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="4f44c-2153">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="4f44c-2154">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="4f44c-2154">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="4f44c-2155">Länk för tjänstassociering på modell för undernät har lagts till</span><span class="sxs-lookup"><span data-stu-id="4f44c-2155">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="4f44c-2156">Cmdletarna New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap och Remove-AzVirtualNetworkTap har lagts till</span><span class="sxs-lookup"><span data-stu-id="4f44c-2156">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="4f44c-2157">Cmdletarna Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig och Remove-AzNEtworkInterfaceTapConfig har lagts till</span><span class="sxs-lookup"><span data-stu-id="4f44c-2157">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="4f44c-2158">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="4f44c-2158">Az.RedisCache</span></span>
* <span data-ttu-id="4f44c-2159">Tillåt att alla strängar används som storleksparametrar framöver.</span><span class="sxs-lookup"><span data-stu-id="4f44c-2159">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="4f44c-2160">Lägg till P5 i popup-fönstret PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="4f44c-2160">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="4f44c-2161">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4f44c-2161">Az.Resources</span></span>
* <span data-ttu-id="4f44c-2162">Parametern -Mode som saknades i Set-AzPolicyDefinition har lagts till</span><span class="sxs-lookup"><span data-stu-id="4f44c-2162">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="4f44c-2163">Åtgärdade buggen för cmdleten Get-AzProviderOperation för åtgärder med ursprung som innehåller användare</span><span class="sxs-lookup"><span data-stu-id="4f44c-2163">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="4f44c-2164">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4f44c-2164">Az.Sql</span></span>
* <span data-ttu-id="4f44c-2165">Ett problem där vissa cmdletar för säkerhetskopiering inte kunde identifiera den aktuella azure-prenumerationen har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="4f44c-2165">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4f44c-2166">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4f44c-2166">Az.Websites</span></span>
* <span data-ttu-id="4f44c-2167">Ny cmdlet: Get-AzWebAppContainerContinuousDeploymentUrl – Hämtar webhook-URL:en för kontinuerlig distribution av container</span><span class="sxs-lookup"><span data-stu-id="4f44c-2167">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="4f44c-2168">Nya cmdletar: New-AzWebAppContainerPSSession och Enter-WebAppContainerPSSession – Startar en PowerShell-fjärrsession i en containerapp för windows</span><span class="sxs-lookup"><span data-stu-id="4f44c-2168">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="4f44c-2169">0.2.0 – september 2018</span><span class="sxs-lookup"><span data-stu-id="4f44c-2169">0.2.0 - September 2018</span></span>
 <span data-ttu-id="4f44c-2170">Första versionen</span><span class="sxs-lookup"><span data-stu-id="4f44c-2170">Initial Release</span></span>
