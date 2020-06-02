---
title: Viktig information om Azure PowerShell
description: Lär dig mer om alla de senaste uppdateringarna för Azure PowerShell-modulerna.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.openlocfilehash: c02cfaa7f7f39393f21cec31c5115f009381b19c
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/05/2020
ms.locfileid: "81446061"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="ed124-103">Viktig information om Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="ed124-103">Azure PowerShell release notes</span></span>
## <a name="0100-preview---april-2020"></a><span data-ttu-id="ed124-104">0.10.0-förhandsversion – April 2020</span><span class="sxs-lookup"><span data-stu-id="ed124-104">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="ed124-105">Allmänt</span><span class="sxs-lookup"><span data-stu-id="ed124-105">General</span></span>
* <span data-ttu-id="ed124-106">Az-moduler är nu tillgängliga i förhandsversion på Azure Stack Hub.</span><span class="sxs-lookup"><span data-stu-id="ed124-106">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="ed124-107">Därmed möjliggörs kompatibilitet för flera plattformar med Linux och macOs.</span><span class="sxs-lookup"><span data-stu-id="ed124-107">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="ed124-108">Azure Stack Hub stöder nu PowerShell Core med AZ-moduler. Mer information finns [här](https://aka.ms/az4AzureStack)</span><span class="sxs-lookup"><span data-stu-id="ed124-108">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](https://aka.ms/az4AzureStack)</span></span>
* <span data-ttu-id="ed124-109">Supportprofil för AZ-moduler 2019-03-01-hybrid:</span><span class="sxs-lookup"><span data-stu-id="ed124-109">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="ed124-110">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="ed124-110">Az.Billing</span></span>
  - <span data-ttu-id="ed124-111">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ed124-111">Az.Compute</span></span>
  - <span data-ttu-id="ed124-112">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="ed124-112">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="ed124-113">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="ed124-113">Az.EventHub</span></span>
  - <span data-ttu-id="ed124-114">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ed124-114">Az.IotHub</span></span>
  - <span data-ttu-id="ed124-115">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ed124-115">Az.KeyVault</span></span>
  - <span data-ttu-id="ed124-116">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ed124-116">Az.Monitor</span></span>
  - <span data-ttu-id="ed124-117">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ed124-117">Az.Network</span></span>
  - <span data-ttu-id="ed124-118">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ed124-118">Az.Resources</span></span>
  - <span data-ttu-id="ed124-119">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ed124-119">Az.Storage</span></span>
  - <span data-ttu-id="ed124-120">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ed124-120">Az.Websites</span></span>
* <span data-ttu-id="ed124-121">Tre nya PowerShell-moduler för AZ har introducerats som fungerar med Azure Stack Hub, och de är Az.Databox, Az.IotHub och Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="ed124-121">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="ed124-122">Kommandona är i princip oförändrade, med endast mindre ändringar som att AzureRM ändras till AZ</span><span class="sxs-lookup"><span data-stu-id="ed124-122">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="ed124-123">En uppdaterad länk till PowerShell-dokumentationen för Azure Stack Hub finns [här](aka.ms/InstallASHPowerShell)</span><span class="sxs-lookup"><span data-stu-id="ed124-123">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](aka.ms/InstallASHPowerShell)</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="ed124-124">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ed124-124">Az.Accounts</span></span>
* <span data-ttu-id="ed124-125">Uppgradera från ADAL till MSAL</span><span class="sxs-lookup"><span data-stu-id="ed124-125">Upgrade from ADAL to MSAL</span></span>


## <a name="370---march-2020"></a><span data-ttu-id="ed124-126">3.7.0 – mars 2020</span><span class="sxs-lookup"><span data-stu-id="ed124-126">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ed124-127">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ed124-127">Az.Accounts</span></span>
* <span data-ttu-id="ed124-128">Åtgärdade ”Get-AzTenant”/”Get-AzDefault”/”Set-AzDefault”-utlösning av NullReferenceException när du inte är inloggad [#10292]</span><span class="sxs-lookup"><span data-stu-id="ed124-128">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ed124-129">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ed124-129">Az.Compute</span></span>
* <span data-ttu-id="ed124-130">Följande parametrar har lagts till i cmdleten ”New-AzDiskConfig”:</span><span class="sxs-lookup"><span data-stu-id="ed124-130">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span> 
    - <span data-ttu-id="ed124-131">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="ed124-131">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="ed124-132">Tillåten krypteringsegenskap till målparametern för cmdleten ”New-AzGalleryImageVersion”.</span><span class="sxs-lookup"><span data-stu-id="ed124-132">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="ed124-133">Åtgärdade tempDisk-problem för cmdletarna ”Set-AzVmss”-Reimage och ”Invoke-AzVMReimage”.</span><span class="sxs-lookup"><span data-stu-id="ed124-133">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="ed124-134">[#11354]</span><span class="sxs-lookup"><span data-stu-id="ed124-134">[#11354]</span></span>
* <span data-ttu-id="ed124-135">Stöd har lagts till i nedanstående cmdletar för nytt SAP-tillägg</span><span class="sxs-lookup"><span data-stu-id="ed124-135">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="ed124-136">”Set-AzVMAEMExtension”</span><span class="sxs-lookup"><span data-stu-id="ed124-136">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="ed124-137">”Get-AzVMAEMExtension”</span><span class="sxs-lookup"><span data-stu-id="ed124-137">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="ed124-138">”Remove-AzVMAEMExtension”</span><span class="sxs-lookup"><span data-stu-id="ed124-138">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="ed124-139">”Update-AzVMAEMExtension”</span><span class="sxs-lookup"><span data-stu-id="ed124-139">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="ed124-140">Åtgärdade fel i exempel på hjälpdokument</span><span class="sxs-lookup"><span data-stu-id="ed124-140">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="ed124-141">Visade det exakta strängvärdet för VM PowerState i tabellformat.</span><span class="sxs-lookup"><span data-stu-id="ed124-141">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="ed124-142">”New-AzVmssConfig”: den fasta serialiseringen av egenskapen AutomaticRepairs när SinglePlacementGroup är inaktiverad.</span><span class="sxs-lookup"><span data-stu-id="ed124-142">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="ed124-143">[#11257]</span><span class="sxs-lookup"><span data-stu-id="ed124-143">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ed124-144">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ed124-144">Az.DataFactory</span></span>
* <span data-ttu-id="ed124-145">ADF .Net SDK har uppdaterats till 4.8.0</span><span class="sxs-lookup"><span data-stu-id="ed124-145">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="ed124-146">Valfria parametrar har lagts till i kommandot ”Invoke-AzDataFactoryV2Pipeline” för att stödja omkörning</span><span class="sxs-lookup"><span data-stu-id="ed124-146">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ed124-147">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ed124-147">Az.DataLakeStore</span></span>
* <span data-ttu-id="ed124-148">Lade till beskrivning för icke-bakåtkompatibel ändring för ”Export-AzDataLakeStoreItem” och ”Import-AzDataLakeStoreItem”</span><span class="sxs-lookup"><span data-stu-id="ed124-148">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="ed124-149">Lade till alternativ för bytekodning för ”New-AzDataLakeStoreItem”, ”Add-AzDAtaLakeStoreItemContent” och ”Get-AzDAtaLakeStoreItemContent”</span><span class="sxs-lookup"><span data-stu-id="ed124-149">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="ed124-150">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="ed124-150">Az.HDInsight</span></span>
* <span data-ttu-id="ed124-151">Stöd för att ange en minimal TLS-version som stöds när klustret skapas.</span><span class="sxs-lookup"><span data-stu-id="ed124-151">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ed124-152">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ed124-152">Az.IotHub</span></span>
* <span data-ttu-id="ed124-153">Stöd har lagts till för att hantera distribuerade inställningar per enhet.</span><span class="sxs-lookup"><span data-stu-id="ed124-153">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="ed124-154">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="ed124-154">New Cmdlets are:</span></span>
    - <span data-ttu-id="ed124-155">”Get-AzIotHubDistributedTracing”</span><span class="sxs-lookup"><span data-stu-id="ed124-155">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="ed124-156">”Set-AzIotHubDistributedTracing”</span><span class="sxs-lookup"><span data-stu-id="ed124-156">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="ed124-157">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ed124-157">Az.KeyVault</span></span>
* <span data-ttu-id="ed124-158">Ändrade attribut för icke-bakåtkompatibel ändring lades till för ”New-AzKeyVault”</span><span class="sxs-lookup"><span data-stu-id="ed124-158">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ed124-159">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ed124-159">Az.Monitor</span></span>
* <span data-ttu-id="ed124-160">Uppdaterad dokumentation för ”New-AzScheduledQueryRuleLogMetricTrigger”</span><span class="sxs-lookup"><span data-stu-id="ed124-160">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ed124-161">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ed124-161">Az.Network</span></span>
* <span data-ttu-id="ed124-162">Uppdaterade cmdletar för att tillåta VirtualHubVnetConnections mellan klienter</span><span class="sxs-lookup"><span data-stu-id="ed124-162">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="ed124-163">”New-AzVirtualHubVnetConnection”</span><span class="sxs-lookup"><span data-stu-id="ed124-163">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="ed124-164">”Update-AzVirtualHubVnetConnection”</span><span class="sxs-lookup"><span data-stu-id="ed124-164">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="ed124-165">”New-AzVirtualHub”</span><span class="sxs-lookup"><span data-stu-id="ed124-165">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="ed124-166">”Update-AzVirtualHub”</span><span class="sxs-lookup"><span data-stu-id="ed124-166">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="ed124-167">SQL Management SDK-beroende har tagits bort</span><span class="sxs-lookup"><span data-stu-id="ed124-167">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="ed124-168">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="ed124-168">Az.PolicyInsights</span></span>
* <span data-ttu-id="ed124-169">Förbättrade felmeddelanden</span><span class="sxs-lookup"><span data-stu-id="ed124-169">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ed124-170">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ed124-170">Az.RecoveryServices</span></span>
* <span data-ttu-id="ed124-171">Azure Site Recovery har lagt till stöd för återaktivering av skydd och uppdaterade VM-egenskaper för virtuella Azure-datorer med krypterad disk.</span><span class="sxs-lookup"><span data-stu-id="ed124-171">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="ed124-172">Lade till Azure Site Recovery VmwareToAzure-egenskaper för DR-övervakning</span><span class="sxs-lookup"><span data-stu-id="ed124-172">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="ed124-173">Azure Backup har lagt till stöd för att försöka uppdatera principuppdateringen för misslyckade objekt på nytt.</span><span class="sxs-lookup"><span data-stu-id="ed124-173">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="ed124-174">Azure Backup lagt till stöd för diskundantagsinställningar under säkerhetskopiering och återställning.</span><span class="sxs-lookup"><span data-stu-id="ed124-174">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="ed124-175">Azure Backup lagt till stöd för att återställa flera filer/mappar i AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="ed124-175">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="ed124-176">Azure Backup lade till support för användardefinierad Resourcegroup-support vid uppdatering av IaasVM-princip</span><span class="sxs-lookup"><span data-stu-id="ed124-176">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="ed124-177">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ed124-177">Az.Resources</span></span>
* <span data-ttu-id="ed124-178">Åtgärdade ”Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType” så att den använder den faktisk apiVersion av resurser i stället för standard-apiVersion [#11267]</span><span class="sxs-lookup"><span data-stu-id="ed124-178">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="ed124-179">Lade till correlationId-loggning för felscenarier</span><span class="sxs-lookup"><span data-stu-id="ed124-179">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="ed124-180">Liten dokumentationsändring för ”Get-AzResourceLock”.</span><span class="sxs-lookup"><span data-stu-id="ed124-180">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="ed124-181">Lade till exempel.</span><span class="sxs-lookup"><span data-stu-id="ed124-181">Added example.</span></span>
* <span data-ttu-id="ed124-182">Undantaget enkelt citattecken i parametervärde för ”Get-AzADUser” [#11317]</span><span class="sxs-lookup"><span data-stu-id="ed124-182">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="ed124-183">Nya cmdletar har lagts till för distributionsskript (”Get-AzDeploymentScript”, ”Get-AzDeploymentScriptLog”, ”Save-AzDeploymentScriptLog”, ”Remove-AzDeploymentScript”)</span><span class="sxs-lookup"><span data-stu-id="ed124-183">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="ed124-184">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ed124-184">Az.Sql</span></span>
* <span data-ttu-id="ed124-185">En läsbar sekundär parameter har lagts till i Invoke-AzSqlDatabaseFailover</span><span class="sxs-lookup"><span data-stu-id="ed124-185">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="ed124-186">Cmdleten Disable-AzSqlServerActiveDirectoryOnlyAuthentication har lagts till</span><span class="sxs-lookup"><span data-stu-id="ed124-186">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="ed124-187">Den sparade känslighet rangordningen när kolumner klassificeras i databasen.</span><span class="sxs-lookup"><span data-stu-id="ed124-187">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="ed124-188">Az.Support</span><span class="sxs-lookup"><span data-stu-id="ed124-188">Az.Support</span></span>
* <span data-ttu-id="ed124-189">Allmän tillgänglighet för ”Az.Support”-modulen</span><span class="sxs-lookup"><span data-stu-id="ed124-189">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ed124-190">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ed124-190">Az.Websites</span></span>
* <span data-ttu-id="ed124-191">Stöd har lagts till för att arbeta med trafikdirigeringsregler för webbappar under nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="ed124-191">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="ed124-192">”Get-AzWebAppTrafficRouting”</span><span class="sxs-lookup"><span data-stu-id="ed124-192">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="ed124-193">”Update-AzWebAppTrafficRouting”</span><span class="sxs-lookup"><span data-stu-id="ed124-193">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="ed124-194">”Add-AzWebAppTrafficRouting”</span><span class="sxs-lookup"><span data-stu-id="ed124-194">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="ed124-195">”Remove-AzWebAppTrafficRouting”</span><span class="sxs-lookup"><span data-stu-id="ed124-195">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="ed124-196">3.6.1 – mars 2020</span><span class="sxs-lookup"><span data-stu-id="ed124-196">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ed124-197">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ed124-197">Az.Accounts</span></span>
* <span data-ttu-id="ed124-198">Öppna sidan med Azure PowerShell-enkäten i ”Send-Feedback” [#11020]</span><span class="sxs-lookup"><span data-stu-id="ed124-198">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="ed124-199">Visa URL:en för Azure PowerShell-enkäten i ”Resolve-Error” [#11021]</span><span class="sxs-lookup"><span data-stu-id="ed124-199">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="ed124-200">Az-version har lagts till i UserAgent</span><span class="sxs-lookup"><span data-stu-id="ed124-200">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="ed124-201">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ed124-201">Az.ApiManagement</span></span>
* <span data-ttu-id="ed124-202">Stöd har lagts till för att hämta och konfigurera en anpassad domän på DeveloperPortal-slutpunkten [#11007]</span><span class="sxs-lookup"><span data-stu-id="ed124-202">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="ed124-203">”Export-AzApiManagementApi” Stöd har lagts till för att ladda ned API-definition i Json-format [#9987]</span><span class="sxs-lookup"><span data-stu-id="ed124-203">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="ed124-204">”Import-AzApiManagementApi” Stöd har lagts till för att importera OpenApi 3.0-definition från Json-dokument</span><span class="sxs-lookup"><span data-stu-id="ed124-204">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="ed124-205">”New-AzApiManagementIdentityProvider” och ”Set-AzApiManagementIdentityProvider” Stöd har lagts till för att konfigurera ”Signin Tenant” för AAD B2C-provider [#9784]</span><span class="sxs-lookup"><span data-stu-id="ed124-205">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ed124-206">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ed124-206">Az.DataLakeStore</span></span>
* <span data-ttu-id="ed124-207">En referens har uttryckligen lagts till för System.Buffers i csproj och psd1.</span><span class="sxs-lookup"><span data-stu-id="ed124-207">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ed124-208">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ed124-208">Az.IotHub</span></span>
* <span data-ttu-id="ed124-209">Lade till stöd för att hantera enheter i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="ed124-209">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="ed124-210">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="ed124-210">New Cmdlets are:</span></span>
    - <span data-ttu-id="ed124-211">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="ed124-211">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="ed124-212">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="ed124-212">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="ed124-213">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="ed124-213">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="ed124-214">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="ed124-214">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="ed124-215">Stöd har lagts till för att hantera moduler på en mål-IoT-enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="ed124-215">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="ed124-216">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="ed124-216">New Cmdlets are:</span></span>
    - <span data-ttu-id="ed124-217">”Add-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="ed124-217">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="ed124-218">”Get-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="ed124-218">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="ed124-219">”Remove-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="ed124-219">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="ed124-220">”Set-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="ed124-220">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="ed124-221">Cmdlet har lagts till för att hämta anslutningssträngen för en mål-IoT-enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="ed124-221">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="ed124-222">Cmdlet har lagts till för att hämta anslutningssträngen för en modul på en mål-IoT-enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="ed124-222">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="ed124-223">Stöd har lagts till för att hämta/ange en överordnad enhet för en IoT-enhet.</span><span class="sxs-lookup"><span data-stu-id="ed124-223">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="ed124-224">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="ed124-224">New Cmdlets are:</span></span>
    - <span data-ttu-id="ed124-225">”Get-AzIotHubDeviceParent”</span><span class="sxs-lookup"><span data-stu-id="ed124-225">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="ed124-226">”Set-AzIotHubDeviceParent”</span><span class="sxs-lookup"><span data-stu-id="ed124-226">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="ed124-227">Stöd har lagts till för att hantera en enhets överordnade och underordnade relationer.</span><span class="sxs-lookup"><span data-stu-id="ed124-227">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ed124-228">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ed124-228">Az.Monitor</span></span>
* <span data-ttu-id="ed124-229">Utdatavärdet har åtgärdats för ”Get-AzMetricDefinition” [#9714]</span><span class="sxs-lookup"><span data-stu-id="ed124-229">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ed124-230">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ed124-230">Az.Network</span></span>
* <span data-ttu-id="ed124-231">SQL Management SDK har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="ed124-231">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="ed124-232">Ett problem har åtgärdats med namngivningsskillnader i klassen PrivateLinkServiceConnectionState.</span><span class="sxs-lookup"><span data-stu-id="ed124-232">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="ed124-233">Fältet ActionsRequired mappar till ActionRequired.</span><span class="sxs-lookup"><span data-stu-id="ed124-233">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="ed124-234">PublicNetworkAccess har lagts till i ”New-AzSqlServer” och ”Set-AzSqlServer”</span><span class="sxs-lookup"><span data-stu-id="ed124-234">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="ed124-235">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ed124-235">Az.Resources</span></span>
* <span data-ttu-id="ed124-236">Null-referensfel har åtgärdats i ”Get-AzRoleAssignment”</span><span class="sxs-lookup"><span data-stu-id="ed124-236">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="ed124-237">Växlarna ”-Force” och ”-PassThru” är valfria i ”Remove-AzADGroup” [#10849]</span><span class="sxs-lookup"><span data-stu-id="ed124-237">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="ed124-238">Ett problem har åtgärdats som gjorde att ”MailNickname” inte returnerades i ”Remove-AzADGroup” [#11167]</span><span class="sxs-lookup"><span data-stu-id="ed124-238">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="ed124-239">Ett problem har åtgärdats som gjorde att pipe-åtgärden ”Remove-AzADGroup” inte fungerar [#11171]</span><span class="sxs-lookup"><span data-stu-id="ed124-239">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="ed124-240">Ett null-referensfel har åtgärdats i GetAzureRoleAssignmentCommand</span><span class="sxs-lookup"><span data-stu-id="ed124-240">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="ed124-241">Attribut för icke-bakåtkompatibla ändringar har lagts till för kommande ändringar i cmdlets för principer</span><span class="sxs-lookup"><span data-stu-id="ed124-241">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="ed124-242">”Get-AzResourceGroup” har uppdaterats för att utföra taggfiltrering för resursgrupper på serversidan</span><span class="sxs-lookup"><span data-stu-id="ed124-242">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="ed124-243">Utökade Tag-cmdlets stöder -ResourceId</span><span class="sxs-lookup"><span data-stu-id="ed124-243">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="ed124-244">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="ed124-244">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="ed124-245">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="ed124-245">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="ed124-246">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="ed124-246">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="ed124-247">Ny Tag-cmdlet har lagts till</span><span class="sxs-lookup"><span data-stu-id="ed124-247">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="ed124-248">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="ed124-248">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="ed124-249">Flyttade ScopedDeployment från SDK 3.3.0</span><span class="sxs-lookup"><span data-stu-id="ed124-249">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="ed124-250">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ed124-250">Az.Sql</span></span>
* <span data-ttu-id="ed124-251">PublicNetworkAccess har lagts till i ”New-AzSqlServer” och ”Set-AzSqlServer”</span><span class="sxs-lookup"><span data-stu-id="ed124-251">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="ed124-252">Stöd har lagts till för konfiguration av säkerhetskopiering för långsiktig kvarhållning för hanterade databaser</span><span class="sxs-lookup"><span data-stu-id="ed124-252">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="ed124-253">Hämta/ange LTR-princip på en hanterad databas</span><span class="sxs-lookup"><span data-stu-id="ed124-253">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="ed124-254">Hämta LTR-säkerhetskopior efter hanterad databas, hanterad instans eller plats</span><span class="sxs-lookup"><span data-stu-id="ed124-254">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="ed124-255">Ta bort en LTR-säkerhetskopia</span><span class="sxs-lookup"><span data-stu-id="ed124-255">Remove an LTR backup</span></span>
    - <span data-ttu-id="ed124-256">Återställa en LTR-säkerhetskopia för att skapa en ny hanterad databas</span><span class="sxs-lookup"><span data-stu-id="ed124-256">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="ed124-257">MinimalTlsVersion har lagts till för New-AzSqlServer och Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="ed124-257">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="ed124-258">MinimalTlsVersion har lagts till för New-AzSqlInstance och Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="ed124-258">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="ed124-259">SQL SDK-versionen för Az.Network har ändrats</span><span class="sxs-lookup"><span data-stu-id="ed124-259">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ed124-260">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ed124-260">Az.Storage</span></span>
* <span data-ttu-id="ed124-261">AllowProtectedAppendWrite stöds i ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="ed124-261">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="ed124-262">”Set-AzRmStorageContainerImmutabilityPolicy”</span><span class="sxs-lookup"><span data-stu-id="ed124-262">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="ed124-263">Varningsmeddelande har lagts till om icke-bakåtkompatibel ändring för ändring av typen AzureStorageTable i en senare version</span><span class="sxs-lookup"><span data-stu-id="ed124-263">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="ed124-264">”New-AzStorageTable”</span><span class="sxs-lookup"><span data-stu-id="ed124-264">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="ed124-265">”Get-AzStorageTable”</span><span class="sxs-lookup"><span data-stu-id="ed124-265">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ed124-266">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ed124-266">Az.Websites</span></span>
* <span data-ttu-id="ed124-267">Tag-parametern har lagts till för ”New-AzAppServicePlan” och ”Set-AzAppServicePlan”</span><span class="sxs-lookup"><span data-stu-id="ed124-267">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="ed124-268">Stoppa cmdlet-körning om ett undantag uppstår när en anpassad domän läggs till på en webbplats</span><span class="sxs-lookup"><span data-stu-id="ed124-268">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="ed124-269">Stöd har lagts till för att utföra åtgärder för App Services som inte tillhör samma resursgrupp som App Services-planen</span><span class="sxs-lookup"><span data-stu-id="ed124-269">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="ed124-270">Åtkomstbegränsning har tillämpats på WebApp/Function i olika resursgrupper</span><span class="sxs-lookup"><span data-stu-id="ed124-270">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="ed124-271">Ett problem har åtgärdats för att ange anpassade värdnamn för WebAppSlots</span><span class="sxs-lookup"><span data-stu-id="ed124-271">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="ed124-272">3.5.0 – februari 2020</span><span class="sxs-lookup"><span data-stu-id="ed124-272">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="ed124-273">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="ed124-273">Highlights since the last major release</span></span>
* <span data-ttu-id="ed124-274">Uppdaterade telemetri på klientsidan.</span><span class="sxs-lookup"><span data-stu-id="ed124-274">Updated client side telemetry.</span></span>
* <span data-ttu-id="ed124-275">Az.IotHub lade till cmdletar som stöd för att hantera enheter.</span><span class="sxs-lookup"><span data-stu-id="ed124-275">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="ed124-276">Az.SqlVirtualMachine lade till cmdletar för lyssningsfunktion för tillgänglighetsgrupp.</span><span class="sxs-lookup"><span data-stu-id="ed124-276">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="ed124-277">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ed124-277">Az.Accounts</span></span>
* <span data-ttu-id="ed124-278">Lade till SubscriptionId, TenantId och körningstid i data för telemetri på klientsidan</span><span class="sxs-lookup"><span data-stu-id="ed124-278">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ed124-279">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ed124-279">Az.Automation</span></span>
* <span data-ttu-id="ed124-280">Åtgärdade skrivfel i exempel 1 i referensdokumentation för ”New-AzAutomationSoftwareUpdateConfiguration”</span><span class="sxs-lookup"><span data-stu-id="ed124-280">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="ed124-281">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ed124-281">Az.CognitiveServices</span></span>
* <span data-ttu-id="ed124-282">Uppdaterade SDK till 7.0</span><span class="sxs-lookup"><span data-stu-id="ed124-282">Updated SDK to 7.0</span></span>
* <span data-ttu-id="ed124-283">Förbättrade felmeddelande vid serversvar om tom brödtext</span><span class="sxs-lookup"><span data-stu-id="ed124-283">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ed124-284">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ed124-284">Az.Compute</span></span>
* <span data-ttu-id="ed124-285">Tillät tomt värde för ProximityPlacementGroupId under uppdatering</span><span class="sxs-lookup"><span data-stu-id="ed124-285">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="ed124-286">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="ed124-286">Az.FrontDoor</span></span>
* <span data-ttu-id="ed124-287">Lade till cmdlet för att hämta hanterade regeldefinitioner som kan användas i WAF</span><span class="sxs-lookup"><span data-stu-id="ed124-287">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ed124-288">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ed124-288">Az.IotHub</span></span>
* <span data-ttu-id="ed124-289">Lade till stöd för att hantera enheter i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="ed124-289">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="ed124-290">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="ed124-290">New Cmdlets are:</span></span>
    - <span data-ttu-id="ed124-291">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="ed124-291">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="ed124-292">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="ed124-292">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="ed124-293">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="ed124-293">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="ed124-294">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="ed124-294">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="ed124-295">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ed124-295">Az.KeyVault</span></span>
* <span data-ttu-id="ed124-296">Åtgärdade duplicerad text för Add-AzKeyVaultKey.md</span><span class="sxs-lookup"><span data-stu-id="ed124-296">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ed124-297">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ed124-297">Az.Monitor</span></span>
* <span data-ttu-id="ed124-298">Åtgärdade beskrivning av cmdleten Get-AzLog.</span><span class="sxs-lookup"><span data-stu-id="ed124-298">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="ed124-299">En ny parameter med namnet ActionGroupId har lagts till i kommandot ”New-AzMetricAlertRuleV2”.</span><span class="sxs-lookup"><span data-stu-id="ed124-299">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="ed124-300">Användaren kan ange ActionGroupId(string) eller ActionGroup(ActivityLogAlertActionGroup).</span><span class="sxs-lookup"><span data-stu-id="ed124-300">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ed124-301">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ed124-301">Az.Network</span></span>
* <span data-ttu-id="ed124-302">Lade till en extra parameteranteckning för parametern ”-EnableProxyProtocol” för cmdleten ”New-AzPrivateLinkService”.</span><span class="sxs-lookup"><span data-stu-id="ed124-302">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="ed124-303">Åtgärdade FilterData-exempel i Start-AzVirtualNetworkGatewayConnectionPacketCapture.md och Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="ed124-303">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="ed124-304">Lade till paketinsamlingsexempel för att samla in alla inre och yttre paket i Start-AzVirtualNetworkGatewayConnectionPacketCapture.md och Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="ed124-304">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="ed124-305">Lade till stöd för Azure-brandväggsprincip på VNet-brandväggar</span><span class="sxs-lookup"><span data-stu-id="ed124-305">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="ed124-306">Inga nya cmdletar har lagts till.</span><span class="sxs-lookup"><span data-stu-id="ed124-306">No new cmdlets are added.</span></span> <span data-ttu-id="ed124-307">Lättar begränsningen för brandväggsprincip på VNet-brandväggar</span><span class="sxs-lookup"><span data-stu-id="ed124-307">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ed124-308">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ed124-308">Az.RecoveryServices</span></span>
* <span data-ttu-id="ed124-309">Lade till stöd för Restore-as-files för SQL-databaser.</span><span class="sxs-lookup"><span data-stu-id="ed124-309">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="ed124-310">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ed124-310">Az.Resources</span></span>
* <span data-ttu-id="ed124-311">Omstrukturerade cmdletar för malldistribution</span><span class="sxs-lookup"><span data-stu-id="ed124-311">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="ed124-312">Lade till nya cmdletar för att hantera distributioner i hanteringsgruppen: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ed124-312">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="ed124-313">Lade till nya cmdletar för att hantera distributioner i klientorganisationsområdet: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="ed124-313">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="ed124-314">Omstrukturerade \*-AzDeployment-cmdletar för att fungera specifikt i prenumerationsomfattningen</span><span class="sxs-lookup"><span data-stu-id="ed124-314">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="ed124-315">Skapade alias \*-AzSubscriptionDeployment för \*-AzDeployment-cmdletar</span><span class="sxs-lookup"><span data-stu-id="ed124-315">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="ed124-316">Åtgärdade ”Update-AzADApplication” när parametern ”AvailableToOtherTenants” inte har angetts</span><span class="sxs-lookup"><span data-stu-id="ed124-316">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="ed124-317">Tog bort ApplicationObjectWithoutCredentialParameterSet för att undvika AmbiguousParameterSetException.</span><span class="sxs-lookup"><span data-stu-id="ed124-317">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="ed124-318">Återskapade hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="ed124-318">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="ed124-319">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ed124-319">Az.Sql</span></span>
* <span data-ttu-id="ed124-320">Lade till stöd för återställning till tidpunkt mellan prenumerationer på hanterade instanser.</span><span class="sxs-lookup"><span data-stu-id="ed124-320">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="ed124-321">Lade till stöd för att ändra befintlig SQL Managed Instance-maskinvarugenerering</span><span class="sxs-lookup"><span data-stu-id="ed124-321">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="ed124-322">Åtgärdade ”Update-AzSqlServerVulnerabilityAssessmentSetting”-hjälpexempel: parameter/egenskapsutdata - EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="ed124-322">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="ed124-323">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="ed124-323">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="ed124-324">Lade till cmdletar för lyssningsfunktion för tillgänglighetsgrupp</span><span class="sxs-lookup"><span data-stu-id="ed124-324">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="ed124-325">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="ed124-325">Az.StorageSync</span></span>
* <span data-ttu-id="ed124-326">Uppdaterade teckenuppsättningar som stöds i ”Invoke-AzStorageSyncCompatibilityCheck”.</span><span class="sxs-lookup"><span data-stu-id="ed124-326">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="ed124-327">3.4.0 – februari 2020</span><span class="sxs-lookup"><span data-stu-id="ed124-327">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="ed124-328">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="ed124-328">Highlights since the last major release</span></span>
* <span data-ttu-id="ed124-329">Första Az.CosmosDB-versionen 0.1.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="ed124-329">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="ed124-330">Stöd för Az.Network ConnectionMonitor V2 har lagts till</span><span class="sxs-lookup"><span data-stu-id="ed124-330">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="ed124-331">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ed124-331">Az.Accounts</span></span>
* <span data-ttu-id="ed124-332">Inaktivera automatisk sparande av kontext när AzureRmContext.json inte är tillgängligt</span><span class="sxs-lookup"><span data-stu-id="ed124-332">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="ed124-333">Uppdatera referensen till Azure Powershell Common till 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="ed124-333">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="ed124-334">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ed124-334">Az.ApiManagement</span></span>
* <span data-ttu-id="ed124-335">**Get-AzApiManagementApiSchema** Hämtning av Open-Api-schema som är associerat med ett API har åtgärdats   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="ed124-335">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="ed124-336">**New-AzApiManagementProduct**\* och **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="ed124-336">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="ed124-337">Åtgärda dokumentation för https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="ed124-337">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="ed124-338">**Set-AzApiManagementApi** Exempel för att visa hur ServiceUrl uppdateras med hjälp av cmdleten har lagts till</span><span class="sxs-lookup"><span data-stu-id="ed124-338">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ed124-339">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ed124-339">Az.Compute</span></span>
* <span data-ttu-id="ed124-340">Begränsa antalet VM-status till 100 för att undvika begränsning när Get-AzVM -Status utförs utan VM-namn.</span><span class="sxs-lookup"><span data-stu-id="ed124-340">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="ed124-341">Lägg till cmdleten Update-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="ed124-341">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="ed124-342">Lägg till parametrarna EncryptionType och DiskEncryptionSetId i följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="ed124-342">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="ed124-343">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="ed124-343">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="ed124-344">Lägg till parametern ColocationStatus för cmdleten Get-AzProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="ed124-344">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ed124-345">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ed124-345">Az.DataFactory</span></span>
* <span data-ttu-id="ed124-346">Uppdatera ADF .Net SDK-versionen till 4.7.0</span><span class="sxs-lookup"><span data-stu-id="ed124-346">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="ed124-347">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="ed124-347">Az.DeploymentManager</span></span>
* <span data-ttu-id="ed124-348">Lägger till LIST-åtgärder för resurser</span><span class="sxs-lookup"><span data-stu-id="ed124-348">Adds LIST operations for resources</span></span>
* <span data-ttu-id="ed124-349">Lägger till funktion för att utföra åtgärder för hälsokontrollsteg</span><span class="sxs-lookup"><span data-stu-id="ed124-349">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="ed124-350">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="ed124-350">Az.HDInsight</span></span>
* <span data-ttu-id="ed124-351">Åtgärda dokumentfel för New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="ed124-351">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="ed124-352">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ed124-352">Az.KeyVault</span></span>
* <span data-ttu-id="ed124-353">Lägg till Name-alias för attributet VaultName så att Remove-AzureKeyVault stämmer överens med New-AzureKeyVault.</span><span class="sxs-lookup"><span data-stu-id="ed124-353">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ed124-354">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ed124-354">Az.Network</span></span>
* <span data-ttu-id="ed124-355">Nytt exempel har lagts till i Set-AzNetworkWatcherConfigFlowLog.md för att demonstrera ett inaktiveringsscenario för Trafikanalys.</span><span class="sxs-lookup"><span data-stu-id="ed124-355">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="ed124-356">Lägg till stöd för att tilldela konfiguration av hanterings-IP till Azure Firewall – ett dedikerat undernät och en offentlig IP som brandväggen använder för dess hanteringstrafik</span><span class="sxs-lookup"><span data-stu-id="ed124-356">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="ed124-357">Cmdleten New-AzFirewall har uppdaterats:</span><span class="sxs-lookup"><span data-stu-id="ed124-357">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="ed124-358">Parametern -ManagementPublicIpAddress (inte obligatorisk) som accepterar ett offentligt IP-adressobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="ed124-358">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="ed124-359">Metoden SetManagementIpConfiguration har lagts till för brandväggsobjekt – kräver ett undernät och en offentlig IP-adress som indata – undernätets namn måste vara ”AzureFirewallManagementSubnet”</span><span class="sxs-lookup"><span data-stu-id="ed124-359">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="ed124-360">Exempel för Get-AzNetworkSecurityGroup har korrigerats så att exempel visas för NSG:er i stället för nätverksgränssnitt.</span><span class="sxs-lookup"><span data-stu-id="ed124-360">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="ed124-361">Ett skrivfel har åtgärdats i kommandot New-AzVpnSite som hindrade kompletteraren för resurs-ID från att fylla i en parameter.</span><span class="sxs-lookup"><span data-stu-id="ed124-361">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="ed124-362">Stöd för Url-konfiguration i åtgärdsuppsättningen för omskrivningsregler i Application Gateway har lagts till</span><span class="sxs-lookup"><span data-stu-id="ed124-362">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="ed124-363">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="ed124-363">New cmdlets added:</span></span>
        - <span data-ttu-id="ed124-364">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="ed124-364">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="ed124-365">Cmdletar har uppdaterats med den valfria parametern -UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="ed124-365">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="ed124-366">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="ed124-366">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="ed124-367">Lägg till stöd för resurser för NetworkWatcher ConnectionMonitor version 2</span><span class="sxs-lookup"><span data-stu-id="ed124-367">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="ed124-368">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="ed124-368">Az.PolicyInsights</span></span>
* <span data-ttu-id="ed124-369">Stöd för utvärdering av efterlevnad innan fastställande av vilken resurs som ska åtgärdas</span><span class="sxs-lookup"><span data-stu-id="ed124-369">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="ed124-370">Lägg till parametern ”-ResourceDiscoverMode” för Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="ed124-370">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="ed124-371">Lägg till cmdleten Get-AzPolicyMetadata för att hämta resurser för principmetadata</span><span class="sxs-lookup"><span data-stu-id="ed124-371">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="ed124-372">Get-AzPolicyState och Get-AzPolicyStateSummary för API-versionen 2019-10-01 har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="ed124-372">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ed124-373">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ed124-373">Az.RecoveryServices</span></span>
* <span data-ttu-id="ed124-374">Azure Site Recovery-stöd för att ta bort en replikerad disk.</span><span class="sxs-lookup"><span data-stu-id="ed124-374">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="ed124-375">Tillagt Azure Backup-stöd för att lägga till taggar när ett Recovery Services-valv skapas.</span><span class="sxs-lookup"><span data-stu-id="ed124-375">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="ed124-376">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ed124-376">Az.Resources</span></span>
* <span data-ttu-id="ed124-377">Gör -Scope valfritt i cmdletarna \*-AzPolicyAssignment med standardinställning till kontextprenumeration</span><span class="sxs-lookup"><span data-stu-id="ed124-377">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="ed124-378">Lägg till exempel på att skapa ADServicePrincipal med lösenord och nyckelautentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="ed124-378">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="ed124-379">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ed124-379">Az.Sql</span></span>
<span data-ttu-id="ed124-380">Åtgärda cmdleten New-AzSqlDatabaseSecondary så att existensen PartnerDatabaseName kontrolleras i stället för existensen DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="ed124-380">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ed124-381">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ed124-381">Az.Storage</span></span>
* <span data-ttu-id="ed124-382">Stöd för angivning av krypteringsnyckeltyp för Tabell/kö i Skapa lagringskonto</span><span class="sxs-lookup"><span data-stu-id="ed124-382">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="ed124-383">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ed124-383">New-AzStorageAccount</span></span>
* <span data-ttu-id="ed124-384">Visa RequestId när StorageException inte har ExtendedErrorInformation</span><span class="sxs-lookup"><span data-stu-id="ed124-384">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="ed124-385">Åtgärda exempel 6 för cmdleten Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="ed124-385">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ed124-386">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ed124-386">Az.Websites</span></span>
* <span data-ttu-id="ed124-387">Set-AzWebapp och Set-AzWebappSlot stöder egenskaperna AlwaysOn, MinTls och FtpsState</span><span class="sxs-lookup"><span data-stu-id="ed124-387">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="ed124-388">Åtgärdar problemet där inställning av HttpsOnly samtidigt som AppservicePlan ändrades med det enskilda kommandot Set-AzWebApp återställde HttpsOnly till standardvärdet</span><span class="sxs-lookup"><span data-stu-id="ed124-388">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="ed124-389">3.3.0 – januari 2020</span><span class="sxs-lookup"><span data-stu-id="ed124-389">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ed124-390">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ed124-390">Az.Accounts</span></span>
* <span data-ttu-id="ed124-391">Nu stöder Add-AzEnvironment och Set-AzEnvironment parametrarna AzureAttestationServiceEndpointResourceId och AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="ed124-391">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="ed124-392">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="ed124-392">Az.Cdn</span></span>
* <span data-ttu-id="ed124-393">Information om felsvar visas i New-AzCdnEndpoint-cmdleten</span><span class="sxs-lookup"><span data-stu-id="ed124-393">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ed124-394">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ed124-394">Az.Compute</span></span>
* <span data-ttu-id="ed124-395">Set-AzVMCustomScriptExtension-cmdleten har åtgärdats för en virtuell dator med hanterad OD-disk som inte har någon operativsystemprofil.</span><span class="sxs-lookup"><span data-stu-id="ed124-395">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="ed124-396">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="ed124-396">Az.ContainerInstance</span></span>
* <span data-ttu-id="ed124-397">Parameternamn som används med New-AzContainerGroup-exempel har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="ed124-397">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="ed124-398">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="ed124-398">Az.DataBoxEdge</span></span>
* <span data-ttu-id="ed124-399">Cmdleten ”Get-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="ed124-399">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="ed124-400">Hämta gränslagringscontainern</span><span class="sxs-lookup"><span data-stu-id="ed124-400">Get the Edge Storage Container</span></span>
* <span data-ttu-id="ed124-401">Cmdleten ”New-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="ed124-401">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="ed124-402">Skapa en ny gränslagringscontainer</span><span class="sxs-lookup"><span data-stu-id="ed124-402">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="ed124-403">Cmdleten ”Remove-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="ed124-403">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="ed124-404">Ta bort gränslagringscontainern</span><span class="sxs-lookup"><span data-stu-id="ed124-404">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="ed124-405">Cmdleten ”Invoke-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="ed124-405">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="ed124-406">Anropa åtgärd för att uppdatera data i gränslagringscontainer</span><span class="sxs-lookup"><span data-stu-id="ed124-406">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="ed124-407">Cmdleten ”Get-AzDataBoxEdgeStorageAccount” har lagts till</span><span class="sxs-lookup"><span data-stu-id="ed124-407">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="ed124-408">Hämta gränslagringskontot</span><span class="sxs-lookup"><span data-stu-id="ed124-408">Get the Edge Storage Account</span></span>
* <span data-ttu-id="ed124-409">Cmdleten ”New-AzDataBoxEdgeStorageAccount” har lagts till</span><span class="sxs-lookup"><span data-stu-id="ed124-409">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="ed124-410">Skapa ett nytt gränslagringskonto</span><span class="sxs-lookup"><span data-stu-id="ed124-410">Create new Edge Storage Account</span></span>
* <span data-ttu-id="ed124-411">Cmdleten ”Remove-AzDataBoxEdgeStorageAccount” har lagts till</span><span class="sxs-lookup"><span data-stu-id="ed124-411">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="ed124-412">Ta bort gränslagringskontot</span><span class="sxs-lookup"><span data-stu-id="ed124-412">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="ed124-413">Anropa cmdleten ”Invoke-AzDataBoxEdgeShare”</span><span class="sxs-lookup"><span data-stu-id="ed124-413">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="ed124-414">Anropa åtgärd för att uppdatera resursdata</span><span class="sxs-lookup"><span data-stu-id="ed124-414">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="ed124-415">Cmdleten ”Set-AzDataBoxEdgeStorageAccountCredential” har lagts till</span><span class="sxs-lookup"><span data-stu-id="ed124-415">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="ed124-416">Ange autentiseringsuppgifter för az databoxedge-lagringskonto</span><span class="sxs-lookup"><span data-stu-id="ed124-416">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ed124-417">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ed124-417">Az.DataFactory</span></span>
* <span data-ttu-id="ed124-418">Lägg till AutoUpdateETA-, LatestVersion-, PushedVersion-, TaskQueueId- och VersionStatus-egenskaper för Get-AzDataFactoryV2IntegrationRuntime-cmd</span><span class="sxs-lookup"><span data-stu-id="ed124-418">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="ed124-419">Uppdatera ADF .Net SDK-versionen till 4.6.0</span><span class="sxs-lookup"><span data-stu-id="ed124-419">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="ed124-420">Lägg till parametern ”PublicIPs” för ”Set-AzureRmDataFactoryV2IntegrationRuntime”-cmd så att Azure-SSIS IR kan skapas med statiska offentliga IP-adresser.</span><span class="sxs-lookup"><span data-stu-id="ed124-420">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="ed124-421">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="ed124-421">Az.DevTestLabs</span></span>
* <span data-ttu-id="ed124-422">Ta bort den brutna länken i Get-AzDtlAllowedVMSizesPolicy.md</span><span class="sxs-lookup"><span data-stu-id="ed124-422">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="ed124-423">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="ed124-423">Az.EventHub</span></span>
* <span data-ttu-id="ed124-424">Korrigering av problem 10634: Åtgärda referensen till null-objekt för eventhubnamespace-borttagning</span><span class="sxs-lookup"><span data-stu-id="ed124-424">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="ed124-425">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="ed124-425">Az.HDInsight</span></span>
* <span data-ttu-id="ed124-426">Åtgärda Invoke-AzHDInsightHiveJob.md-fel.</span><span class="sxs-lookup"><span data-stu-id="ed124-426">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="ed124-427">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="ed124-427">Az.MachineLearning</span></span>
* <span data-ttu-id="ed124-428">Nedanstående cmdletar har tagits bort eftersom MachineLearningCompute inte längre är tillgängligt</span><span class="sxs-lookup"><span data-stu-id="ed124-428">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="ed124-429">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="ed124-429">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="ed124-430">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="ed124-430">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="ed124-431">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="ed124-431">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="ed124-432">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="ed124-432">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="ed124-433">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="ed124-433">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="ed124-434">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="ed124-434">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="ed124-435">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="ed124-435">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ed124-436">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ed124-436">Az.Network</span></span>
* <span data-ttu-id="ed124-437">Uppgradera beroende av Microsoft.Azure.Management.Sql från 1.36-preview till 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="ed124-437">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ed124-438">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ed124-438">Az.RecoveryServices</span></span>
* <span data-ttu-id="ed124-439">Ändrat Azure Site Recovery-stöd för krypterade vilande data på virtuella datorer med hanterade diskar med kundhanterade nycklar för Azure till Azure-providern.</span><span class="sxs-lookup"><span data-stu-id="ed124-439">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="ed124-440">Azure Site Recovery-stöd för att ange ID för diskkrypteringsuppsättning som valfri inmatning för aktivering av skydd för VMware till Azure.</span><span class="sxs-lookup"><span data-stu-id="ed124-440">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="ed124-441">Azure Site Recovery-stöd för att ange ID för diskkrypteringsuppsättning som valfri inmatning på disknivå för aktivering av skydd för VMware till Azure.</span><span class="sxs-lookup"><span data-stu-id="ed124-441">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="ed124-442">Azure Site Recovery-stöd för att uppdatera replikeringsskyddade objekt med mappning för diskkrypteringsuppsättning för HyperV till Azure.</span><span class="sxs-lookup"><span data-stu-id="ed124-442">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="ed124-443">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ed124-443">Az.Resources</span></span>
* <span data-ttu-id="ed124-444">Åtgärda ett fel i hjälpdokument för ”Remove-AzTag”.</span><span class="sxs-lookup"><span data-stu-id="ed124-444">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="ed124-445">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ed124-445">Az.Sql</span></span>
* <span data-ttu-id="ed124-446">Åtgärda funktioner i cmdletar för att ange baslinjen för sårbarhetsbedömning för arbete med huvuddatabasen för Azure-databasen och begränsa den för systemdatabaser på hanterade instanser.</span><span class="sxs-lookup"><span data-stu-id="ed124-446">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="ed124-447">Åtgärda ett fel när en redundansgrupp för en SQL-instans skapas</span><span class="sxs-lookup"><span data-stu-id="ed124-447">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="ed124-448">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="ed124-448">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="ed124-449">Lägg till DR som en ny giltig licenstyp</span><span class="sxs-lookup"><span data-stu-id="ed124-449">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ed124-450">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ed124-450">Az.Storage</span></span>
* <span data-ttu-id="ed124-451">Lägg till varningsmeddelande om icke-bakåtkompatibel ändring för DefaultAction-värdeändring i en framtida version</span><span class="sxs-lookup"><span data-stu-id="ed124-451">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="ed124-452">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="ed124-452">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="ed124-453">Stöd för att hämta lagringskontots senaste synkroniseringstid genom att köra get-AzureRMStorageAccount med parametern -IncludeGeoReplicationStats</span><span class="sxs-lookup"><span data-stu-id="ed124-453">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="ed124-454">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ed124-454">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="ed124-455">3.2.0 – December 2019</span><span class="sxs-lookup"><span data-stu-id="ed124-455">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="ed124-456">Allmänt</span><span class="sxs-lookup"><span data-stu-id="ed124-456">General</span></span>
* <span data-ttu-id="ed124-457">Uppdatera referenser i .psd1 för att använda relativa sökvägar för alla moduler</span><span class="sxs-lookup"><span data-stu-id="ed124-457">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="ed124-458">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ed124-458">Az.Accounts</span></span>
* <span data-ttu-id="ed124-459">Ange rätt UserAgent för telemetri på klientsidan för Az 4.0 preview</span><span class="sxs-lookup"><span data-stu-id="ed124-459">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="ed124-460">Visa användarvänligt felmeddelande när kontexten är null i Az 4.0 preview</span><span class="sxs-lookup"><span data-stu-id="ed124-460">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="ed124-461">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="ed124-461">Az.Batch</span></span>
* <span data-ttu-id="ed124-462">Korrigera problem [#10602](https://github.com/Azure/azure-powershell/issues/10602), där **New-AzBatchPool** skickade VirtualMachineConfiguration.ContainerConfiguration eller VirtualMachineConfiguration.DataDisks på ett felaktigt sätt till servern.</span><span class="sxs-lookup"><span data-stu-id="ed124-462">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ed124-463">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ed124-463">Az.DataFactory</span></span>
* <span data-ttu-id="ed124-464">Uppdatera ADF .Net SDK-versionen till 4.5.0</span><span class="sxs-lookup"><span data-stu-id="ed124-464">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="ed124-465">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="ed124-465">Az.FrontDoor</span></span>
* <span data-ttu-id="ed124-466">Stöd har lagts till för undantag för hanterade regler för brandväggen för webbaserade program</span><span class="sxs-lookup"><span data-stu-id="ed124-466">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="ed124-467">Lägg till SocketAddr för automatisk komplettering</span><span class="sxs-lookup"><span data-stu-id="ed124-467">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="ed124-468">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="ed124-468">Az.HealthcareApis</span></span>
* <span data-ttu-id="ed124-469">Undantagshantering</span><span class="sxs-lookup"><span data-stu-id="ed124-469">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="ed124-470">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ed124-470">Az.KeyVault</span></span>
* <span data-ttu-id="ed124-471">Åtgärdat fel vid åtkomst av värde som kanske inte har angetts</span><span class="sxs-lookup"><span data-stu-id="ed124-471">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="ed124-472">Hantering av ECC-certifikat (Elliptic Curve Cryptography)</span><span class="sxs-lookup"><span data-stu-id="ed124-472">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="ed124-473">Stöd har lagts till för att ange kurvan för certifikatprinciper</span><span class="sxs-lookup"><span data-stu-id="ed124-473">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ed124-474">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ed124-474">Az.Monitor</span></span>
* <span data-ttu-id="ed124-475">Lägger till valfritt argument i kommandot Lägg till diagnostikinställningar.</span><span class="sxs-lookup"><span data-stu-id="ed124-475">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="ed124-476">Ett växelargument som om det finns visar att exporten till Log Analytics måste ske till ett fast schema (kallas även</span><span class="sxs-lookup"><span data-stu-id="ed124-476">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="ed124-477">dedikerad, datatyp)</span><span class="sxs-lookup"><span data-stu-id="ed124-477">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ed124-478">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ed124-478">Az.Network</span></span>
* <span data-ttu-id="ed124-479">Stöd för IpGroups i program-, NAT- och nätverksregler för Azure Firewall.</span><span class="sxs-lookup"><span data-stu-id="ed124-479">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="ed124-480">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ed124-480">Az.Resources</span></span>
* <span data-ttu-id="ed124-481">Åtgärda ett problem där malldistributionen inte kan läsa en mallparameter om dess namn står i konflikt med ett inbyggt parameternamn.</span><span class="sxs-lookup"><span data-stu-id="ed124-481">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="ed124-482">Uppdaterade princip-cmdletar för att använda den nya API-versionen 2019-09-01 som introducerar grupperingsstöd inom principuppsättningsdefinitioner.</span><span class="sxs-lookup"><span data-stu-id="ed124-482">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="ed124-483">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ed124-483">Az.Sql</span></span>
* <span data-ttu-id="ed124-484">Uppgraderad funktion för att skapa lagring i automatisk aktivering av sårbarhetsbedömning till StorageV2</span><span class="sxs-lookup"><span data-stu-id="ed124-484">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ed124-485">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ed124-485">Az.Storage</span></span>
* <span data-ttu-id="ed124-486">Stöd för generering av blob/container-identitetsbaserad SAS-token med lagringskontextbaserad på OAuth-autentisering</span><span class="sxs-lookup"><span data-stu-id="ed124-486">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="ed124-487">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="ed124-487">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="ed124-488">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="ed124-488">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="ed124-489">Stöd för återkallning av användardelegeringsnycklar för lagringskonto för att återkalla alla SAS-token</span><span class="sxs-lookup"><span data-stu-id="ed124-489">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="ed124-490">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="ed124-490">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="ed124-491">Uppgradera till Microsoft.Azure.Management.Storage 14.2.0 för att stödja den nya API-versionen 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="ed124-491">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="ed124-492">Stöd för QuotaGiB (resurskvot i Gibibye) för värden över 5120 i hanteringsplanet för cmdletar för filresurser och parameteraliaset. Quota har också lagts till för parametern ”QuotaGiB”.</span><span class="sxs-lookup"><span data-stu-id="ed124-492">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="ed124-493">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="ed124-493">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="ed124-494">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="ed124-494">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="ed124-495">Lägg till parameteraliaset QuotaGiB i parametern Quota</span><span class="sxs-lookup"><span data-stu-id="ed124-495">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="ed124-496">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="ed124-496">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="ed124-497">Åtgärda problemet att Set-AzStorageContainerAcl kan rensa den lagrade åtkomstprincipen</span><span class="sxs-lookup"><span data-stu-id="ed124-497">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="ed124-498">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="ed124-498">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="ed124-499">3.1.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="ed124-499">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="ed124-500">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="ed124-500">Highlights since the last major release</span></span>
* <span data-ttu-id="ed124-501">Az.DataBoxEdge 1.0.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="ed124-501">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="ed124-502">Az.SqlVirtualMachine 1.0.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="ed124-502">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ed124-503">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ed124-503">Az.Compute</span></span>
* <span data-ttu-id="ed124-504">Funktion för att använda en virtuell dator igen</span><span class="sxs-lookup"><span data-stu-id="ed124-504">VM Reapply feature</span></span>
    - <span data-ttu-id="ed124-505">Lägg till parameter för att använda igen till cmdleten Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="ed124-505">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="ed124-506">Funktionen AutomaticRepairs i VM-skalningsuppsättningar:</span><span class="sxs-lookup"><span data-stu-id="ed124-506">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="ed124-507">Lägg till parametrarna EnableAutomaticRepair, AutomaticRepairGracePeriod och AutomaticRepairMaxInstanceRepairsPercent till följande cmdletar:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ed124-507">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="ed124-508">Stöd för galleriavbildningar i flera klientorganisationer för New-AzVM</span><span class="sxs-lookup"><span data-stu-id="ed124-508">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="ed124-509">Lägg till "Spot" till argumentslutföraren i prioritetsparametern i cmdletarna New-AzVM, New-AzVMConfig och New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ed124-509">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="ed124-510">Lägg till parametrarna DiskIOPSReadWrite och DiskMBpsReadWrite till cmdleten Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="ed124-510">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="ed124-511">Ändra parametern SourceImageId för cmdleten New-AzGalleryImageVersion till valfri</span><span class="sxs-lookup"><span data-stu-id="ed124-511">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="ed124-512">Lägg till parametrarna OSDiskImage och DataDiskImage till cmdleten New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="ed124-512">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="ed124-513">Lägg till parametern HyperVGeneration till cmdleten New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="ed124-513">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="ed124-514">Lägg till parametern SkipExtensionsOnOverprovisionedVMs till cmdletarna New-AzVmss, New-AzVmssConfig och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ed124-514">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="ed124-515">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="ed124-515">Az.DataBoxEdge</span></span>
* <span data-ttu-id="ed124-516">Cmdleten `Get-AzDataBoxEdgeOrder` har lagts till</span><span class="sxs-lookup"><span data-stu-id="ed124-516">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="ed124-517">Hämta ordning</span><span class="sxs-lookup"><span data-stu-id="ed124-517">Get the Order</span></span>
* <span data-ttu-id="ed124-518">Cmdleten `New-AzDataBoxEdgeOrder` har lagts till</span><span class="sxs-lookup"><span data-stu-id="ed124-518">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="ed124-519">Skapa ny ordning</span><span class="sxs-lookup"><span data-stu-id="ed124-519">Create new Order</span></span>
* <span data-ttu-id="ed124-520">Cmdleten `Remove-AzDataBoxEdgeOrder` har lagts till</span><span class="sxs-lookup"><span data-stu-id="ed124-520">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="ed124-521">Ta bort ordning</span><span class="sxs-lookup"><span data-stu-id="ed124-521">Remove the Order</span></span>
* <span data-ttu-id="ed124-522">Cmdleten `New-AzDataBoxEdgeShare` har ändrats</span><span class="sxs-lookup"><span data-stu-id="ed124-522">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="ed124-523">Nu skapas lokal filresurs</span><span class="sxs-lookup"><span data-stu-id="ed124-523">Now creates Local Share</span></span>
* <span data-ttu-id="ed124-524">Cmdleten `Set-AzDataBoxEdgeRole` har lagts till</span><span class="sxs-lookup"><span data-stu-id="ed124-524">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="ed124-525">Nu kan IotRole mappas till filresursen</span><span class="sxs-lookup"><span data-stu-id="ed124-525">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="ed124-526">Cmdleten `Invoke-AzDataBoxEdgeDevice` har lagts till</span><span class="sxs-lookup"><span data-stu-id="ed124-526">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="ed124-527">Anropa genomsökningsuppdatering, ladda ned uppdatering, installera uppdateringar på enheten</span><span class="sxs-lookup"><span data-stu-id="ed124-527">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="ed124-528">Cmdleten `Get-AzDataBoxEdgeTrigger` har lagts till</span><span class="sxs-lookup"><span data-stu-id="ed124-528">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="ed124-529">Hämtar information om utlösare</span><span class="sxs-lookup"><span data-stu-id="ed124-529">Gets the information about Triggers</span></span>
* <span data-ttu-id="ed124-530">Cmdleten `New-AzDataBoxEdgeTrigger` har lagts till</span><span class="sxs-lookup"><span data-stu-id="ed124-530">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="ed124-531">Skapa nya utlösare</span><span class="sxs-lookup"><span data-stu-id="ed124-531">Create new Triggers</span></span>
* <span data-ttu-id="ed124-532">Cmdleten `Remove-AzDataBoxEdgeTrigger` har lagts till</span><span class="sxs-lookup"><span data-stu-id="ed124-532">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="ed124-533">Ta bort utlösare</span><span class="sxs-lookup"><span data-stu-id="ed124-533">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ed124-534">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ed124-534">Az.DataFactory</span></span>
* <span data-ttu-id="ed124-535">Uppdatera ADF .Net SDK-versionen till 4.4.0</span><span class="sxs-lookup"><span data-stu-id="ed124-535">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="ed124-536">Lägg till parametern ExpressCustomSetup för kommandot Set-AzureRmDataFactoryV2IntegrationRuntime för att aktivera installationskonfigurationer och komponenter från tredje part utan anpassat konfigurationsskript.</span><span class="sxs-lookup"><span data-stu-id="ed124-536">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ed124-537">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ed124-537">Az.DataLakeStore</span></span>
* <span data-ttu-id="ed124-538">Uppdatera dokumentation för Get-AzDataLakeStoreDeletedItem och Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="ed124-538">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="ed124-539">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="ed124-539">Az.EventHub</span></span>
* <span data-ttu-id="ed124-540">Korrigering av problem #10301: Korrigera datumformat för SAS-token</span><span class="sxs-lookup"><span data-stu-id="ed124-540">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="ed124-541">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="ed124-541">Az.FrontDoor</span></span>
* <span data-ttu-id="ed124-542">Lägg till parametern MinimumTlsVersion till Enable-AzFrontDoorCustomDomainHttps och New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="ed124-542">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="ed124-543">Lägg till parametrarna HealthProbeMethod och EnabledState till New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="ed124-543">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="ed124-544">Lägg till en ny cmdlet för att skapa BackendPoolsSettings-objekt som passar i skapande/uppdatering av Front Door</span><span class="sxs-lookup"><span data-stu-id="ed124-544">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="ed124-545">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="ed124-545">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ed124-546">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ed124-546">Az.Network</span></span>
* <span data-ttu-id="ed124-547">Ändra alternativexemplen Start-AzVirtualNetworkGatewayConnectionPacketCapture.md och Start-AzVirtualnetworkGatewayPacketCapture.md för FilterData.</span><span class="sxs-lookup"><span data-stu-id="ed124-547">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="ed124-548">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="ed124-548">Az.PrivateDns</span></span>
* <span data-ttu-id="ed124-549">Uppdaterade PrivateDns .NET SDK till version 1.0.0</span><span class="sxs-lookup"><span data-stu-id="ed124-549">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ed124-550">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ed124-550">Az.RecoveryServices</span></span>
* <span data-ttu-id="ed124-551">Stöd för att välja disktyp vid aktivering av skydd i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="ed124-551">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="ed124-552">Korrigering av bugg för åtgärdsredigering av återställningsplan i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="ed124-552">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="ed124-553">Återställningsstöd för att godkänna filestream-databaser i Azure Backup SQL.</span><span class="sxs-lookup"><span data-stu-id="ed124-553">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="ed124-554">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="ed124-554">Az.RedisCache</span></span>
* <span data-ttu-id="ed124-555">Parametern MinimumTlsVersion har lagts till i cmdletarna New-AzRedisCache och Set-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="ed124-555">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="ed124-556">Dessutom har MinimumTlsVersion lagts till i utdata för cmdleten Get-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="ed124-556">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="ed124-557">Verifiering har lagts till på parametern -Size i cmdletarna Set-AzRedisCache och New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="ed124-557">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="ed124-558">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ed124-558">Az.Resources</span></span>
- <span data-ttu-id="ed124-559">Uppdaterade policy-cmdletar för att använda den nya API-versionen 2019-06-01 som har en ny EnforcementMode-egenskap i policytilldelningen.</span><span class="sxs-lookup"><span data-stu-id="ed124-559">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="ed124-560">Uppdaterade hjälpexempel för skapandet av policydefinition</span><span class="sxs-lookup"><span data-stu-id="ed124-560">Updated create policy definition help example</span></span>
- <span data-ttu-id="ed124-561">Åtgärda bugg i Remove-AZADServicePrincipal -ServicePrincipalName, utlös null-referens när tjänstens huvudnamn inte hittas.</span><span class="sxs-lookup"><span data-stu-id="ed124-561">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="ed124-562">Åtgärda bugg i New-AZADServicePrincipal, utlös null-referens när klientorganisationen inte har någon prenumeration.</span><span class="sxs-lookup"><span data-stu-id="ed124-562">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="ed124-563">Ändra New-AzAdServicePrincipal för att endast lägga till autentiseringsuppgifter för det associerade programmet.</span><span class="sxs-lookup"><span data-stu-id="ed124-563">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="ed124-564">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ed124-564">Az.Sql</span></span>
* <span data-ttu-id="ed124-565">Stöd har lagts till för databasen ReadReplicaCount.</span><span class="sxs-lookup"><span data-stu-id="ed124-565">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="ed124-566">Korrigerade Set-AzSqlDatabase när zonredundans inte har angetts</span><span class="sxs-lookup"><span data-stu-id="ed124-566">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="ed124-567">3.0.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="ed124-567">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="ed124-568">Allmänt</span><span class="sxs-lookup"><span data-stu-id="ed124-568">General</span></span>
* <span data-ttu-id="ed124-569">Az. PrivateDns 1.0.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="ed124-569">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="ed124-570">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ed124-570">Az.Accounts</span></span>
* <span data-ttu-id="ed124-571">Lägg till ett utfasningsmeddelande för aliaset Resolve-error.</span><span class="sxs-lookup"><span data-stu-id="ed124-571">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="ed124-572">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="ed124-572">Az.Advisor</span></span>
* <span data-ttu-id="ed124-573">Den nya kategorin Operational Excellence har lagts till i cmdleten Get-AzAdvisorRecommendation.</span><span class="sxs-lookup"><span data-stu-id="ed124-573">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="ed124-574">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="ed124-574">Az.Batch</span></span>
* <span data-ttu-id="ed124-575">`CoreQuota` på `BatchAccountContext` har bytt namn till `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="ed124-575">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="ed124-576">Det finns även en ny `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="ed124-576">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="ed124-577">Detta påverkar **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="ed124-577">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="ed124-578">**New-AzBatchTask** `-ResourceFile`-parametern tar nu en samling `PSResourceFile`-objekt som kan skapas med hjälp av den nya cmdleten **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="ed124-578">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="ed124-579">Ny **New-AzBatchResourceFile**-cmdlet för att skapa `PSResourceFile`-objekt.</span><span class="sxs-lookup"><span data-stu-id="ed124-579">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="ed124-580">Dessa kan tillhandahållas till **New-AzBatchTask** på `-ResourceFile`-parametern.</span><span class="sxs-lookup"><span data-stu-id="ed124-580">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="ed124-581">Detta stöder två nya typer av resursfiler förutom det befintliga sättet med `HttpUrl`:</span><span class="sxs-lookup"><span data-stu-id="ed124-581">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="ed124-582">`AutoStorageContainerName`-baserade resursfiler laddar ned en hel container för automatisk lagring till Batch-noden.</span><span class="sxs-lookup"><span data-stu-id="ed124-582">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="ed124-583">`StorageContainerUrl`-baserade resursfiler laddar ned containern som anges i webbadressen till Batch-noden.</span><span class="sxs-lookup"><span data-stu-id="ed124-583">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="ed124-584">Tog bort egenskapen `ApplicationPackages` för `PSApplication` som returnerades av **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="ed124-584">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="ed124-585">Specifika paket i ett program kan nu hämtas med hjälp av **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="ed124-585">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="ed124-586">Till exempel: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="ed124-586">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="ed124-587">Bytt namn på `ApplicationId` till `ApplicationName` på **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** och **Set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="ed124-587">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="ed124-588">`ApplicationId` är nu ett alias för `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="ed124-588">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="ed124-589">Ny `PSWindowsUserConfiguration`-egenskap till `PSUserAccount` lades till.</span><span class="sxs-lookup"><span data-stu-id="ed124-589">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="ed124-590">Bytte namn på `Version` till `Name` på `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="ed124-590">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="ed124-591">Bytte namn på `BlobSource` till `HttpUrl` på `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="ed124-591">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="ed124-592">Tog bort egenskapen `OSDisk` från `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="ed124-592">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="ed124-593">Tog bort **Set-AzBatchPoolOSVersion**.</span><span class="sxs-lookup"><span data-stu-id="ed124-593">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="ed124-594">Den här åtgärden stöds inte längre.</span><span class="sxs-lookup"><span data-stu-id="ed124-594">This operation is no longer supported.</span></span>
* <span data-ttu-id="ed124-595">`TargetOSVersion` har tagits bort från `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="ed124-595">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="ed124-596">Bytte namn på `CurrentOSVersion` till `OSVersion` på `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="ed124-596">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="ed124-597">`DataEgressGiB` och `DataIngressGiB` har tagits bort från `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="ed124-597">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="ed124-598">Tog bort **Get-AzBatchNodeAgentSku** och ersatte det med **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="ed124-598">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="ed124-599">**Get-AzBatchSupportedImage** returnerar samma data som **Get-AzBatchNodeAgentSku** men i ett mer användarvänligt format.</span><span class="sxs-lookup"><span data-stu-id="ed124-599">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="ed124-600">Nya icke-verifierade avbildningar returneras nu också.</span><span class="sxs-lookup"><span data-stu-id="ed124-600">New non-verified images are also now returned.</span></span> <span data-ttu-id="ed124-601">Ytterligare information om `Capabilities` och `BatchSupportEndOfLife` för varje avbildning inkluderas också.</span><span class="sxs-lookup"><span data-stu-id="ed124-601">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="ed124-602">Lade till möjlighet att montera fjärrfilsystem på varje nod i en pool via den nya parametern `MountConfiguration` för **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="ed124-602">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="ed124-603">Har nu stöd för nätverkssäkerhetsregler som blockerar nätverksåtkomst till en pool baserat på källportens trafik.</span><span class="sxs-lookup"><span data-stu-id="ed124-603">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="ed124-604">Detta görs via egenskapen `SourcePortRanges` på `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="ed124-604">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="ed124-605">När du kör en container stöder nu Batch körningen av uppgiften i arbetskatalogen för containern eller i arbetskatalogen för Batch-uppgiften.</span><span class="sxs-lookup"><span data-stu-id="ed124-605">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="ed124-606">Detta styrs av egenskapen `WorkingDirectory` på `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="ed124-606">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="ed124-607">Lade till en funktion för att ange en samling av offentliga IP-adresser på `PSNetworkConfiguration` via den nya egenskapen `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="ed124-607">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="ed124-608">Detta garanterar att noderna i poolen har en IP-adress från listan över IP-adresser som tillhandahållits av användare.</span><span class="sxs-lookup"><span data-stu-id="ed124-608">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="ed124-609">Om inget värde anges är standardvärdet för `WaitForSuccess` på `PSSTartTask` nu `$True` (var tidigare `$False`).</span><span class="sxs-lookup"><span data-stu-id="ed124-609">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="ed124-610">Om inget värde anges är standardvärdet för `Scope` på `PSAutoUserSpecification` nu `Pool` (var tidigare `Task` på Windows och `Pool` på Linux).</span><span class="sxs-lookup"><span data-stu-id="ed124-610">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="ed124-611">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="ed124-611">Az.Cdn</span></span>
* <span data-ttu-id="ed124-612">Introducerade UrlRewriteAction och CacheKeyQueryStringAction till RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="ed124-612">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="ed124-613">Åtgärdade flera buggar, som saknade indata för ”väljare” i cmdleten New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="ed124-613">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ed124-614">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ed124-614">Az.Compute</span></span>
* <span data-ttu-id="ed124-615">Funktion för diskkrypteringsuppsättning</span><span class="sxs-lookup"><span data-stu-id="ed124-615">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="ed124-616">Nya cmdletar:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="ed124-616">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="ed124-617">Parametern DiskEncryptionSetId har lagts till i följande cmdletar:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="ed124-617">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="ed124-618">Parametrarna DiskEncryptionSetId och EncryptionType har lagts till i följande cmdletar:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="ed124-618">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="ed124-619">Lägg till parametern PublicIPAddressVersion i New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="ed124-619">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="ed124-620">Flytta FileUris för anpassat skripttillägg från offentlig inställning till skyddad inställning</span><span class="sxs-lookup"><span data-stu-id="ed124-620">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="ed124-621">Lägg till ScaleInPolicy i cmdletarna New-AzVmss, New-AzVmssConfig och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ed124-621">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="ed124-622">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="ed124-622">Breaking changes</span></span>
    - <span data-ttu-id="ed124-623">Parametern UploadSizeInBytes används istället för DiskSizeGB för New-AzDiskConfig när CreateOption är Uppladdning</span><span class="sxs-lookup"><span data-stu-id="ed124-623">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="ed124-624">PublishingProfile.Source.ManagedImage.Id ersätts med StorageProfile.Source.Id i objektet GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="ed124-624">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ed124-625">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ed124-625">Az.DataFactory</span></span>
* <span data-ttu-id="ed124-626">Uppdatera ADF .Net SDK-versionen till 4.3.0</span><span class="sxs-lookup"><span data-stu-id="ed124-626">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ed124-627">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ed124-627">Az.DataLakeStore</span></span>
* <span data-ttu-id="ed124-628">Uppdatera ADLS SDK-version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) innehåller följande korrigeringar</span><span class="sxs-lookup"><span data-stu-id="ed124-628">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="ed124-629">Undvik att utlösa undantag när det inte går att deserialisera creationtime för inmatning av papperskorg eller katalog.</span><span class="sxs-lookup"><span data-stu-id="ed124-629">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="ed124-630">Gör inställning tillgänglig per tidsgräns för förfrågan i adlsclient</span><span class="sxs-lookup"><span data-stu-id="ed124-630">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="ed124-631">Korrigera överföringen av ursprunglig syncflag för badoffset-återställning</span><span class="sxs-lookup"><span data-stu-id="ed124-631">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="ed124-632">Korrigera EnumerateDirectory för att hämta fortsättningstoken när svar har kontrollerats</span><span class="sxs-lookup"><span data-stu-id="ed124-632">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="ed124-633">Korrigera bugg i Concat</span><span class="sxs-lookup"><span data-stu-id="ed124-633">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="ed124-634">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="ed124-634">Az.FrontDoor</span></span>
* <span data-ttu-id="ed124-635">Åtgärdade diverse stavfel i modul</span><span class="sxs-lookup"><span data-stu-id="ed124-635">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="ed124-636">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="ed124-636">Az.HDInsight</span></span>
* <span data-ttu-id="ed124-637">Korrigerade buggen att kunder får felet ”inte en giltig Base-64-sträng” vid användning av Get-AzHDInsightCluster för att hämta klustret med ADLSGen1-lagring.</span><span class="sxs-lookup"><span data-stu-id="ed124-637">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="ed124-638">Lägg till en parameter med namnet ”ApplicationId” i de tre cmdletarna Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig och New-AzHDInsightCluster så att kunden kan tillhandahålla tjänstens huvudnamn för program-ID för åtkomst till Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="ed124-638">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="ed124-639">Ändrade Microsoft.Azure.Management.HDInsight från 2.1.0 till 5.1.0</span><span class="sxs-lookup"><span data-stu-id="ed124-639">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="ed124-640">Fem cmdletar har tagits bort:</span><span class="sxs-lookup"><span data-stu-id="ed124-640">Removed five cmdlets:</span></span>
    - <span data-ttu-id="ed124-641">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="ed124-641">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="ed124-642">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="ed124-642">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="ed124-643">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="ed124-643">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="ed124-644">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="ed124-644">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="ed124-645">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="ed124-645">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="ed124-646">Tre cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="ed124-646">Added three cmdlets:</span></span>
    - <span data-ttu-id="ed124-647">Get-AzHDInsightMonitoring som ersätter Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="ed124-647">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="ed124-648">Enable-AzHDInsightMonitoring som ersätter Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="ed124-648">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="ed124-649">Disable-AzHDInsightMonitoring som ersätter Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="ed124-649">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="ed124-650">Korrigerade cmdleten Get-AzHDInsightProperties för att stödja hämtning av funktionsinformation från en viss plats.</span><span class="sxs-lookup"><span data-stu-id="ed124-650">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="ed124-651">Parameteruppsättningarna (Spark1 och Spark2) har tagits bort från Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="ed124-651">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="ed124-652">Lägg till exempel för cmdleten Add-AzHDInsightSecurityProfile till hjälpdokumenten.</span><span class="sxs-lookup"><span data-stu-id="ed124-652">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="ed124-653">Ändrade utdatatyp för följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="ed124-653">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="ed124-654">Ändrade utdatatyp för Get-AzHDInsightProperties från CapabilitiesResponse till AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="ed124-654">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="ed124-655">Ändrade utdatatyp för Remove-AzHDInsightCluster från ClusterGetResponse till bool.</span><span class="sxs-lookup"><span data-stu-id="ed124-655">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="ed124-656">Ändrade utdatatyp för Set-AzHDInsightGatewaySettings HttpConnectivitySettings till GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="ed124-656">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="ed124-657">Lade till testfall för vissa scenarier.</span><span class="sxs-lookup"><span data-stu-id="ed124-657">Added some scenario test cases.</span></span>
* <span data-ttu-id="ed124-658">Ta bort vissa alias: Add-AzHDInsightConfigValues, Get-AzHDInsightProperties.</span><span class="sxs-lookup"><span data-stu-id="ed124-658">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ed124-659">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ed124-659">Az.IotHub</span></span>
* <span data-ttu-id="ed124-660">Icke-bakåtkompatibla ändringar:</span><span class="sxs-lookup"><span data-stu-id="ed124-660">Breaking changes:</span></span>
    - <span data-ttu-id="ed124-661">Cmdleten Add-AzIotHubEventHubConsumerGroup har inte längre stöd för parametern EventHubEndpointName och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="ed124-661">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="ed124-662">Parameteruppsättningen __AllParameterSets för cmdleten Add-AzIotHubEventHubConsumerGroup har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="ed124-662">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="ed124-663">Cmdleten Get-AzIotHubEventHubConsumerGroup har inte längre stöd för parametern EventHubEndpointName och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="ed124-663">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="ed124-664">Parameteruppsättningen __AllParameterSets för cmdleten Get-AzIotHubEventHubConsumerGroup har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="ed124-664">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="ed124-665">Egenskapen OperationsMonitoringProperties av typen Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="ed124-665">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="ed124-666">Egenskapen OperationsMonitoringProperties av typen Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="ed124-666">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="ed124-667">Cmdleten New-AzIotHubExportDevice stöder inte längre aliaset New-AzIotHubExportDevices.</span><span class="sxs-lookup"><span data-stu-id="ed124-667">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="ed124-668">Cmdleten New-AzIotHubImportDevice stöder inte längre aliaset New-AzIotHubImportDevices.</span><span class="sxs-lookup"><span data-stu-id="ed124-668">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="ed124-669">Cmdleten Remove-AzIotHubEventHubConsumerGroup har inte längre stöd för parametern EventHubEndpointName och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="ed124-669">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="ed124-670">Parameteruppsättningen __AllParameterSets för cmdleten Remove-AzIotHubEventHubConsumerGroup har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="ed124-670">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="ed124-671">Cmdleten Set-AzIotHub har inte längre stöd för parametern OperationsMonitoringProperties och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="ed124-671">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="ed124-672">Parameteruppsättningen UpdateOperationsMonitoringProperties för cmdleten Set-AzIotHub har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="ed124-672">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ed124-673">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ed124-673">Az.RecoveryServices</span></span>
* <span data-ttu-id="ed124-674">Azure Site Recovery-stöd för att konfigurera nätverksresurser som NSG, offentliga IP-adresser och interna lastbalanserare för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="ed124-674">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="ed124-675">Azure Site Recovery-stöd för att skriva till hanterad disk för vMWare till Azure.</span><span class="sxs-lookup"><span data-stu-id="ed124-675">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="ed124-676">Azure Site Recovery-stöd för NIC-reduktion för vMWare till Azure.</span><span class="sxs-lookup"><span data-stu-id="ed124-676">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="ed124-677">Azure Site Recovery-stöd för accelererat nätverk för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="ed124-677">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="ed124-678">Azure Site Recovery-stöd för automatisk uppdatering av agent för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="ed124-678">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="ed124-679">Azure Site Recovery-stöd för Standard SSD för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="ed124-679">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="ed124-680">Azure Site Recovery-stöd för tvåstegskryptering i Azure Disk Encryption för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="ed124-680">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="ed124-681">Azure Site Recovery-stöd för att skydda nyligen tillagda diskar för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="ed124-681">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="ed124-682">En funktion för mjuk borttagning av virtuella datorer samt tester för mjuk borttagning har tagits bort</span><span class="sxs-lookup"><span data-stu-id="ed124-682">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="ed124-683">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ed124-683">Az.Resources</span></span>
* <span data-ttu-id="ed124-684">Uppdatera beroendesammansättning för Microsoft.Extensions.Caching.Memory från 1.1.1 till 2.2</span><span class="sxs-lookup"><span data-stu-id="ed124-684">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ed124-685">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ed124-685">Az.Network</span></span>
* <span data-ttu-id="ed124-686">Ändra alla cmdletar för PrivateEndpointConnection så att de stöder generiska tjänstleverantörer.</span><span class="sxs-lookup"><span data-stu-id="ed124-686">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="ed124-687">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="ed124-687">Updated cmdlet:</span></span>
        - <span data-ttu-id="ed124-688">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ed124-688">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="ed124-689">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ed124-689">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="ed124-690">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ed124-690">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="ed124-691">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ed124-691">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="ed124-692">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ed124-692">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="ed124-693">Lägg till ny cmdlet för PrivateLinkResource så att det också stöder generiska tjänstleverantörer.</span><span class="sxs-lookup"><span data-stu-id="ed124-693">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="ed124-694">Ny cmdlet:</span><span class="sxs-lookup"><span data-stu-id="ed124-694">New cmdlet:</span></span>
        - <span data-ttu-id="ed124-695">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="ed124-695">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="ed124-696">Lägg till nya fält och parametrar för funktionen Proxy Protocol V2.</span><span class="sxs-lookup"><span data-stu-id="ed124-696">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="ed124-697">Lägg till egenskapen EnableProxyProtocol i PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ed124-697">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="ed124-698">Lägg till egenskapen LinkIdentifier i PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ed124-698">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="ed124-699">Uppdaterade New-AzPrivateLinkService för att lägga till den nya valfria parametern EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="ed124-699">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="ed124-700">Korrigera felaktig beskrivning av parameter i referensdokumentationen för New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="ed124-700">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="ed124-701">Nya cmdletar som stöder Azure-brandväggsprincipen</span><span class="sxs-lookup"><span data-stu-id="ed124-701">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="ed124-702">Lägg till stöd för den underordnade resursen RouteTables för VirtualHub</span><span class="sxs-lookup"><span data-stu-id="ed124-702">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="ed124-703">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="ed124-703">New cmdlets added:</span></span>
        - <span data-ttu-id="ed124-704">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="ed124-704">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="ed124-705">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="ed124-705">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="ed124-706">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="ed124-706">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="ed124-707">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="ed124-707">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="ed124-708">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="ed124-708">Set-AzVirtualHub</span></span>
* <span data-ttu-id="ed124-709">Lägg till stöd för ny egenskaps-SKU för VirtualHub och VirtualWANType för VirtualWan</span><span class="sxs-lookup"><span data-stu-id="ed124-709">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="ed124-710">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="ed124-710">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="ed124-711">New-AzVirtualHub: lade till parameter-SKU</span><span class="sxs-lookup"><span data-stu-id="ed124-711">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="ed124-712">Update-AzVirtualHub: lade till parameter-SKU</span><span class="sxs-lookup"><span data-stu-id="ed124-712">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="ed124-713">New-AzVirtualWan: lade till parametern VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="ed124-713">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="ed124-714">Update-AzVirtualWan: lade till parametern VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="ed124-714">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="ed124-715">Lägg till stöd för egenskapen EnableInternetSecurity för HubVnetConnection, VpnConnection och ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="ed124-715">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="ed124-716">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="ed124-716">New cmdlets added:</span></span>
        - <span data-ttu-id="ed124-717">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="ed124-717">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="ed124-718">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="ed124-718">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="ed124-719">New-AzureRmVirtualHubVnetConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="ed124-719">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="ed124-720">New-AzureRmVpnConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="ed124-720">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="ed124-721">Update-AzureRmVpnConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="ed124-721">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="ed124-722">New-AzureRmExpressRouteConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="ed124-722">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="ed124-723">Set-AzureRmExpressRouteConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="ed124-723">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="ed124-724">Lägg till stöd för att konfigurera TopLevel WebApplicationFirewall-princip</span><span class="sxs-lookup"><span data-stu-id="ed124-724">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="ed124-725">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="ed124-725">New cmdlets added:</span></span>
        - <span data-ttu-id="ed124-726">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="ed124-726">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="ed124-727">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="ed124-727">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="ed124-728">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="ed124-728">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="ed124-729">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="ed124-729">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="ed124-730">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="ed124-730">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="ed124-731">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="ed124-731">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="ed124-732">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="ed124-732">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="ed124-733">New-AzApplicationGatewayFirewallPolicy: parametrarna PolicySetting, ManagedRule har lagts till</span><span class="sxs-lookup"><span data-stu-id="ed124-733">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="ed124-734">Stöd för operator för geomatchning har lagts till på CustomRule</span><span class="sxs-lookup"><span data-stu-id="ed124-734">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="ed124-735">Geomatchning har lagts till i operatorn på FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="ed124-735">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="ed124-736">Stöd har lagts till för brandväggsprinciperna perListener och perSite</span><span class="sxs-lookup"><span data-stu-id="ed124-736">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="ed124-737">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="ed124-737">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="ed124-738">New-AzApplicationGatewayHttpListener: parametrarna FirewallPolicy, FirewallPolicyId har lagts till</span><span class="sxs-lookup"><span data-stu-id="ed124-738">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="ed124-739">New-AzApplicationGatewayPathRuleConfig: parametrarna FirewallPolicy, FirewallPolicyId har lagts till</span><span class="sxs-lookup"><span data-stu-id="ed124-739">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="ed124-740">Åtgärdat så att nödvändigt undernät med namnet AzureBastionSubnet i PSBastion kan vara skiftlägesokänsligt</span><span class="sxs-lookup"><span data-stu-id="ed124-740">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="ed124-741">Stöd för mål-FQDN:er i nätverksregler och översatt FQDN i NAT-regler för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="ed124-741">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="ed124-742">Lägg till stöd för resursen RouteTables för IpGroup på den högsta nivån</span><span class="sxs-lookup"><span data-stu-id="ed124-742">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="ed124-743">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="ed124-743">New cmdlets added:</span></span>
        - <span data-ttu-id="ed124-744">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="ed124-744">New-AzIpGroup</span></span>
        - <span data-ttu-id="ed124-745">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="ed124-745">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="ed124-746">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="ed124-746">Get-AzIpGroup</span></span>
        - <span data-ttu-id="ed124-747">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="ed124-747">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="ed124-748">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ed124-748">Az.ServiceFabric</span></span>
* <span data-ttu-id="ed124-749">Ta bort cmdleten Add-AzServiceFabricApplicationCertificate eftersom det här scenariot omfattas av Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="ed124-749">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="ed124-750">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ed124-750">Az.Sql</span></span>
* <span data-ttu-id="ed124-751">Stöd har lagts till för återställning av utelämnade databaser på hanterade instanser.</span><span class="sxs-lookup"><span data-stu-id="ed124-751">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="ed124-752">Inaktuella gamla cmdletar för granskning från kod.</span><span class="sxs-lookup"><span data-stu-id="ed124-752">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="ed124-753">Tog bort inaktuella alias:</span><span class="sxs-lookup"><span data-stu-id="ed124-753">Removed deprecated aliases:</span></span>
* <span data-ttu-id="ed124-754">Get-AzSqlDatabaseIndexRecommendations (använd Get-AzSqlDatabaseIndexRecommendation istället)</span><span class="sxs-lookup"><span data-stu-id="ed124-754">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="ed124-755">Get-AzSqlDatabaseRestorePoints (använd Get-AzSqlDatabaseRestorePoint istället)</span><span class="sxs-lookup"><span data-stu-id="ed124-755">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="ed124-756">Ta bort cmdleten Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="ed124-756">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="ed124-757">Ta bort alias för inaktuella cmdletar för inställningar för utvärdering av säkerhetsrisk</span><span class="sxs-lookup"><span data-stu-id="ed124-757">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="ed124-758">Inaktualisera cmdletar för inställningar för avancerad hotidentifiering</span><span class="sxs-lookup"><span data-stu-id="ed124-758">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="ed124-759">Lägga till cmdletar för att inaktivera och aktivera känslighetsrekommendationer på kolumner i en databas.</span><span class="sxs-lookup"><span data-stu-id="ed124-759">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ed124-760">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ed124-760">Az.Storage</span></span>
* <span data-ttu-id="ed124-761">Stöd för att aktivera stora filresurser vid skapande eller uppdatering av lagringskonto</span><span class="sxs-lookup"><span data-stu-id="ed124-761">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="ed124-762">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ed124-762">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="ed124-763">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ed124-763">Set-AzStorageAccount</span></span>
* <span data-ttu-id="ed124-764">När du stänger/hämtar en filreferens kan du hoppa över kontrollen av huruvida indatasökvägen är en filkatalog eller en fil för att undvika problem med objekt som har status DeletePending</span><span class="sxs-lookup"><span data-stu-id="ed124-764">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="ed124-765">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="ed124-765">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="ed124-766">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="ed124-766">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="ed124-767">2.8.0 – oktober 2019</span><span class="sxs-lookup"><span data-stu-id="ed124-767">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="ed124-768">Allmänt</span><span class="sxs-lookup"><span data-stu-id="ed124-768">General</span></span>
* <span data-ttu-id="ed124-769">AZ. HealthcareApis 1.0.0-version</span><span class="sxs-lookup"><span data-stu-id="ed124-769">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="ed124-770">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ed124-770">Az.Accounts</span></span>
* <span data-ttu-id="ed124-771">Uppdatera telemetri och URL-omskrivning för genererade moduler, korrigera Windows-enhetstester.</span><span class="sxs-lookup"><span data-stu-id="ed124-771">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="ed124-772">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ed124-772">Az.ApiManagement</span></span>
* <span data-ttu-id="ed124-773">**Set-AzApiManagementApi** – Tillagt stöd för att uppdatera Api till ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="ed124-773">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="ed124-774">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="ed124-774">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ed124-775">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ed124-775">Az.Automation</span></span>
* <span data-ttu-id="ed124-776">Åtgärdade cmdleten New-AzureAutomationSoftwareUpdateConfiguration för parametern för inställning av Linux-omstart.</span><span class="sxs-lookup"><span data-stu-id="ed124-776">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="ed124-777">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="ed124-777">Az.Batch</span></span>
* <span data-ttu-id="ed124-778">**Get-AzBatchNodeAgentSku** är inaktuell och ersätts av **Get-AzBatchSupportImage** i version 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="ed124-778">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ed124-779">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ed124-779">Az.Compute</span></span>
* <span data-ttu-id="ed124-780">Lägg till parametrarna Priority, EvictionPolicy och MaxPrice till cmdletarna New-AzVM och New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ed124-780">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="ed124-781">Korrigera varningsmeddelande och hjälpdokument för cmdletarna Add-AzVMAdditionalUnattendContent och Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="ed124-781">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="ed124-782">Åtgärda – skipVmBackup-undantag för virtuella Linux-datorer med hanterade diskar för Set-AzVMDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="ed124-782">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="ed124-783">Åtgärda fel i uppdatera krypteringsinställningarna i set-AzVMDiskEncryptionExtension, scenario i två steg.</span><span class="sxs-lookup"><span data-stu-id="ed124-783">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ed124-784">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ed124-784">Az.DataFactory</span></span>
* <span data-ttu-id="ed124-785">Lägga till CRUD-kommandon för ADF V2-dataflödet: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow och Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="ed124-785">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="ed124-786">Lägger till åtgärdskommandon för ADF V2-dataflödesfelsökningssession: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand och Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="ed124-786">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="ed124-787">Uppdatera ADF .Net SDK-versionen till 4.2.0</span><span class="sxs-lookup"><span data-stu-id="ed124-787">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ed124-788">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ed124-788">Az.DataLakeStore</span></span>
* <span data-ttu-id="ed124-789">Korrigera kontovalidering så att konton med ”-” kan skickas utan domän</span><span class="sxs-lookup"><span data-stu-id="ed124-789">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="ed124-790">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="ed124-790">Az.HealthcareApis</span></span>
* <span data-ttu-id="ed124-791">PowerShell-versionen har uppdaterats till 1.0.0</span><span class="sxs-lookup"><span data-stu-id="ed124-791">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="ed124-792">Uppdaterade SDK-versionen till 1.0.2</span><span class="sxs-lookup"><span data-stu-id="ed124-792">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="ed124-793">Uppdatera i tester för att referera till en ny SDK-version</span><span class="sxs-lookup"><span data-stu-id="ed124-793">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="ed124-794">Utdatastrukturen har uppdaterats från kapslad till förenklad.</span><span class="sxs-lookup"><span data-stu-id="ed124-794">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ed124-795">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ed124-795">Az.IotHub</span></span>
* <span data-ttu-id="ed124-796">Lägg till ny routningskälla: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="ed124-796">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="ed124-797">Mindre felkorrigering: Get-AzIothub returnerar inte subscriptionId</span><span class="sxs-lookup"><span data-stu-id="ed124-797">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ed124-798">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ed124-798">Az.Monitor</span></span>
* <span data-ttu-id="ed124-799">Nya åtgärdsgruppsmottagare har lagts till för åtgärdsgrupp   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="ed124-799">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="ed124-800">Använd vanligt aviseringsschema som är aktiverat för mottagarna.</span><span class="sxs-lookup"><span data-stu-id="ed124-800">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="ed124-801">Detta gäller inte för SMS, push för Azure-app, ITSM och röstmottagare</span><span class="sxs-lookup"><span data-stu-id="ed124-801">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="ed124-802">Webhooks har nu stöd för Azure Active Directory-autentisering.</span><span class="sxs-lookup"><span data-stu-id="ed124-802">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ed124-803">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ed124-803">Az.Network</span></span>
* <span data-ttu-id="ed124-804">Lägg till ny cmdlet Get-AzAvailableServiceAlias som kan anropas för att hämta de alias som kan användas för tjänstslutpunktsprinciper.</span><span class="sxs-lookup"><span data-stu-id="ed124-804">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="ed124-805">Stöd för tillägg av trafikväljare har lagts till i gatewayanslutningar för virtuella nätverk</span><span class="sxs-lookup"><span data-stu-id="ed124-805">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="ed124-806">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="ed124-806">New cmdlets added:</span></span>
        - <span data-ttu-id="ed124-807">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="ed124-807">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="ed124-808">Cmdletar har uppdaterats med valfri parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ed124-808">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="ed124-809">Lägg till stöd för ESP- och AH-protokoll i konfiguration av nätverkssäkerhetsregler</span><span class="sxs-lookup"><span data-stu-id="ed124-809">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="ed124-810">Uppdaterade cmdletar:</span><span class="sxs-lookup"><span data-stu-id="ed124-810">Updated cmdlets:</span></span>
        - <span data-ttu-id="ed124-811">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ed124-811">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="ed124-812">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ed124-812">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="ed124-813">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ed124-813">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="ed124-814">Förbättra hanteringen av undantag i Cortex-cmdletar</span><span class="sxs-lookup"><span data-stu-id="ed124-814">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="ed124-815">Nya generationer och SKU:er för VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="ed124-815">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="ed124-816">Introducera nya generationer för VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="ed124-816">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="ed124-817">Introducera nya SKU:er med högt dataflöde för VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="ed124-817">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="ed124-818">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="ed124-818">Az.RedisCache</span></span>
* <span data-ttu-id="ed124-819">Uppdaterad referensdokumentation för ”set-AzRedisCache” för att inkludera saknade värden för parametern ”size”</span><span class="sxs-lookup"><span data-stu-id="ed124-819">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="ed124-820">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ed124-820">Az.Sql</span></span>
* <span data-ttu-id="ed124-821">Lägg till stöd för inställningen Active Directory administratör på den hanterade instansen</span><span class="sxs-lookup"><span data-stu-id="ed124-821">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ed124-822">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ed124-822">Az.Storage</span></span>
* <span data-ttu-id="ed124-823">Uppdatera Lagringsklientbibliotek till 11.1.0</span><span class="sxs-lookup"><span data-stu-id="ed124-823">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="ed124-824">Lista containrar med hanteringsplans-API, kommer att listas med NextPageLink</span><span class="sxs-lookup"><span data-stu-id="ed124-824">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="ed124-825">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ed124-825">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="ed124-826">Lista lagringskonton från prenumerationen, kommer att listas med NextPageLink</span><span class="sxs-lookup"><span data-stu-id="ed124-826">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="ed124-827">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ed124-827">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="ed124-828">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="ed124-828">Az.StorageSync</span></span>
* <span data-ttu-id="ed124-829">Åtgärda problemet 9810 i Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="ed124-829">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ed124-830">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ed124-830">Az.Websites</span></span>
* <span data-ttu-id="ed124-831">Set-AzWebApp – uppdatering av ASP för en app misslyckades</span><span class="sxs-lookup"><span data-stu-id="ed124-831">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="ed124-832">2.7.0 – september 2019</span><span class="sxs-lookup"><span data-stu-id="ed124-832">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="ed124-833">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ed124-833">Az.ApiManagement</span></span>
* <span data-ttu-id="ed124-834">Uppdatera ”-Format”-parameterbeskrivningen i ”Set-AzApiManagementPolicy”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="ed124-834">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="ed124-835">Referenser för den föråldrade cmdleten ”Update-AzApiManagementDeployment” har tagits bort från referensdokumentationen.</span><span class="sxs-lookup"><span data-stu-id="ed124-835">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="ed124-836">Använd ”Set-AzApiManagement” i stället.</span><span class="sxs-lookup"><span data-stu-id="ed124-836">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ed124-837">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ed124-837">Az.Automation</span></span>
* <span data-ttu-id="ed124-838">Stavfel har korrigerats i exempel i referensdokumentationen för ”Register-AzAutomationDscNode”</span><span class="sxs-lookup"><span data-stu-id="ed124-838">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="ed124-839">Klargörande har lagts till om OS-begränsningar för Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="ed124-839">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="ed124-840">Null-referensundantag har korrigerats för -Wait-alternativet i Start-AzAutomationRunbook-cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ed124-840">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ed124-841">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ed124-841">Az.Compute</span></span>
* <span data-ttu-id="ed124-842">Lägg till UploadSizeInBytes-parameter till New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="ed124-842">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="ed124-843">Lägg till Incremental-parameter till New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="ed124-843">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="ed124-844">Lägg till en funktion för virtuella datorer med låg prioritet:</span><span class="sxs-lookup"><span data-stu-id="ed124-844">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="ed124-845">MaxPrice-, EvictionPolicy- och Priority-parametrar har lagts till i New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="ed124-845">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="ed124-846">MaxPrice-parametern har lagts till i New-AzVmssConfig-, Update-AzVM- och Update-AzVmss-cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="ed124-846">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="ed124-847">Åtgärda problem med VM-referenser för Get-AzAvailabilitySet-cmdleten när alla tillgänglighetsuppsättningar i prenumerationen visas.</span><span class="sxs-lookup"><span data-stu-id="ed124-847">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="ed124-848">Korrigera null-undantaget för Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="ed124-848">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="ed124-849">Korrigera VHD-metoden för sökning relativt till slut.</span><span class="sxs-lookup"><span data-stu-id="ed124-849">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="ed124-850">Åtgärda UltraSSD-problem för New-AzVM och Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="ed124-850">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ed124-851">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ed124-851">Az.DataFactory</span></span>
* <span data-ttu-id="ed124-852">Lägger till 3 nya kommandon för ADF V2 – Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription och Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="ed124-852">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="ed124-853">ADF .Net SDK har uppdaterats till 4.1.3</span><span class="sxs-lookup"><span data-stu-id="ed124-853">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="ed124-854">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="ed124-854">Az.HDInsight</span></span>
* <span data-ttu-id="ed124-855">Anrop för icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="ed124-855">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ed124-856">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ed124-856">Az.IotHub</span></span>
* <span data-ttu-id="ed124-857">Lägg till stöd för att anropa redundans för en IotHub till den geo-länkade katastrofåterställningsregionen.</span><span class="sxs-lookup"><span data-stu-id="ed124-857">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="ed124-858">Lägg till stöd för att hantera meddelandeberikning för en IotHub.</span><span class="sxs-lookup"><span data-stu-id="ed124-858">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="ed124-859">Nya cmdlet:ar är:</span><span class="sxs-lookup"><span data-stu-id="ed124-859">New cmdlets are:</span></span>
    - <span data-ttu-id="ed124-860">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="ed124-860">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="ed124-861">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="ed124-861">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="ed124-862">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="ed124-862">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="ed124-863">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="ed124-863">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ed124-864">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ed124-864">Az.Monitor</span></span>
* <span data-ttu-id="ed124-865">Pekar på den senaste Monitor SDK:n, dvs. 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="ed124-865">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="ed124-866">Lägger till bakåtkompatibla ändringar i Metrics-cmdletarna, dvs. enhetsuppräkningen stöder flera nya värden.</span><span class="sxs-lookup"><span data-stu-id="ed124-866">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="ed124-867">Detta är skrivskyddade cmdletar, så det förekommer inga ändringar i inmatningen för cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="ed124-867">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="ed124-868">API-versionen för **ActionGroups**-begäranden är nu **2019-06-01**. Tidigare var den **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="ed124-868">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="ed124-869">Test av scenarier har uppdaterats för att anpassas till den här ändringen.</span><span class="sxs-lookup"><span data-stu-id="ed124-869">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="ed124-870">Ett nytt obligatoriskt argument har lagts till för konstruktorerna för klasserna **EmailReceiver** och **WebhookReceiver** – ett booleskt värde med namnet **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="ed124-870">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="ed124-871">Värdet är för närvarande fast till **false** så att den här icke-bakåtkompatibla ändringen är dold från cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="ed124-871">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="ed124-872">**Obs!** Det här är en tillfällig ändring som måste verifieras av Alerts-teamet.</span><span class="sxs-lookup"><span data-stu-id="ed124-872">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="ed124-873">Ordningen på argumenten för konstruktorn för klassen **Source** (relaterad till klassen **ScheduledQueryRuleSource**) har ändrats från den tidigare SDK:n.</span><span class="sxs-lookup"><span data-stu-id="ed124-873">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="ed124-874">Den här ändringen krävde korrigering av två enhetstest: de kompilerades, men testerna skickades inte.</span><span class="sxs-lookup"><span data-stu-id="ed124-874">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="ed124-875">Ordningen på argumenten för konstruktorn för klassen **AlertingAction** (relaterad till klassen **ScheduledQueryRuleSource**) har ändrats från den tidigare SDK:n.</span><span class="sxs-lookup"><span data-stu-id="ed124-875">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="ed124-876">Den här ändringen krävde korrigering av två enhetstest: de kompilerades, men testerna skickades inte.</span><span class="sxs-lookup"><span data-stu-id="ed124-876">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="ed124-877">Stöd för kriterier för dynamiskt tröskelvärde för måttavisering v2</span><span class="sxs-lookup"><span data-stu-id="ed124-877">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="ed124-878">New-AzMetricAlertRuleV2Criteria: skapar nu även kriterier för dynamiskt tröskelvärde</span><span class="sxs-lookup"><span data-stu-id="ed124-878">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="ed124-879">Add-AzMetricAlertRuleV2: accepterar nu även kriterier för dynamiskt tröskelvärde</span><span class="sxs-lookup"><span data-stu-id="ed124-879">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="ed124-880">Förbättringar i schemalagd frågeregel (SQR)</span><span class="sxs-lookup"><span data-stu-id="ed124-880">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="ed124-881">Cmdletar accepterar ”Location”-parameter i båda formaten, antingen platsen (t.ex. eastus) eller platsens visningsnamn (t.ex. USA, östra)</span><span class="sxs-lookup"><span data-stu-id="ed124-881">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="ed124-882">”Enabled”-parametern illustreras korrekt i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="ed124-882">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="ed124-883">Exempel för den valfria parametern ”ActionGroup” har lagts till</span><span class="sxs-lookup"><span data-stu-id="ed124-883">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="ed124-884">Förbättrade hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="ed124-884">Overall improved help files</span></span>
* <span data-ttu-id="ed124-885">Åtgärda bugg då omfattningstypen fastställs för ”Set-AzActionRule”</span><span class="sxs-lookup"><span data-stu-id="ed124-885">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ed124-886">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ed124-886">Az.Network</span></span>
* <span data-ttu-id="ed124-887">Korrigera felaktigt exempel i referensdokumentationen för ”New-AzApplicationGateway”</span><span class="sxs-lookup"><span data-stu-id="ed124-887">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="ed124-888">Lägg till anmärkning i ”Get-AzNetworkWatcherPacketCapture”-referensdokumentationen om hämtning av alla egenskaper för en paketinsamling</span><span class="sxs-lookup"><span data-stu-id="ed124-888">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="ed124-889">Exempel har korrigerats i ”Test-AzNetworkWatcherIPFlow”-referensdokumentationen för korrekt uppräkning av nätverkskort</span><span class="sxs-lookup"><span data-stu-id="ed124-889">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="ed124-890">Förbättrad tolkning av molnundantag för att visa eventuell ytterligare information</span><span class="sxs-lookup"><span data-stu-id="ed124-890">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="ed124-891">Förbättrad tolkning av molnundantag för att hantera ytterligare en typ av SDK-undantag</span><span class="sxs-lookup"><span data-stu-id="ed124-891">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="ed124-892">Felaktig mappning av säkerhetsregelmodeller har korrigerats</span><span class="sxs-lookup"><span data-stu-id="ed124-892">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="ed124-893">Egenskaper har lagts till för nätverksgränssnittet för funktionen Privat IP</span><span class="sxs-lookup"><span data-stu-id="ed124-893">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="ed124-894">Egenskapen ”PrivateEndpoint” har lagts till som en typ av PSResourceId till PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="ed124-894">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="ed124-895">Egenskapen ”PrivateLinkConnectionProperties” har lagts till som en typ av PSIpConfigurationConnectivityInformation till PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ed124-895">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="ed124-896">Modellklassen PSIpConfigurationConnectivityInformation har lagts till</span><span class="sxs-lookup"><span data-stu-id="ed124-896">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="ed124-897">ApplicationRuleProtocolType ”mssql” har lagts till för Azure Firewall-resurs</span><span class="sxs-lookup"><span data-stu-id="ed124-897">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="ed124-898">MultiLink-stöd i virtuellt WAN</span><span class="sxs-lookup"><span data-stu-id="ed124-898">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="ed124-899">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="ed124-899">New cmdlets</span></span>
        - <span data-ttu-id="ed124-900">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="ed124-900">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="ed124-901">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="ed124-901">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="ed124-902">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="ed124-902">Updated cmdlet:</span></span>
        - <span data-ttu-id="ed124-903">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="ed124-903">New-VpnSite</span></span>
        - <span data-ttu-id="ed124-904">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="ed124-904">Update-VpnSite</span></span>
        - <span data-ttu-id="ed124-905">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="ed124-905">New-VpnConnection</span></span>
        - <span data-ttu-id="ed124-906">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="ed124-906">Update-VpnConnection</span></span>
* <span data-ttu-id="ed124-907">Dokument för vissa PowerShell-exempel har korrigerats så att Az-cmdletar används i stället för AzureRM-cmdletar</span><span class="sxs-lookup"><span data-stu-id="ed124-907">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ed124-908">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ed124-908">Az.RecoveryServices</span></span>
* <span data-ttu-id="ed124-909">Uppdatera AzureVMpolicy-objekt med ProtectedItemsCount-attribut</span><span class="sxs-lookup"><span data-stu-id="ed124-909">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="ed124-910">Ytterligare tester har lagts till för VM-princip och återställning av ursprungligt lagringskonto</span><span class="sxs-lookup"><span data-stu-id="ed124-910">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="ed124-911">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ed124-911">Az.Resources</span></span>
* <span data-ttu-id="ed124-912">Åtgärda fel där det inte gick att anropa New-AzRoleAssignment utan parametern Scope.</span><span class="sxs-lookup"><span data-stu-id="ed124-912">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="ed124-913">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ed124-913">Az.ServiceFabric</span></span>
* <span data-ttu-id="ed124-914">Stavfel har korrigerats i exempel för ”Update-AzServiceFabricReliability”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="ed124-914">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="ed124-915">Lägger till nya cmdletar för att hantera program och tjänster:</span><span class="sxs-lookup"><span data-stu-id="ed124-915">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="ed124-916">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="ed124-916">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="ed124-917">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="ed124-917">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="ed124-918">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="ed124-918">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="ed124-919">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="ed124-919">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="ed124-920">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="ed124-920">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="ed124-921">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="ed124-921">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="ed124-922">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="ed124-922">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="ed124-923">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="ed124-923">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="ed124-924">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="ed124-924">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="ed124-925">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="ed124-925">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="ed124-926">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="ed124-926">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="ed124-927">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="ed124-927">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="ed124-928">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="ed124-928">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="ed124-929">Service Fabric SDK har uppgraderats till version 1.2.0 som använder Service Fabric-resursprovidern med API-version 2019-03-01.</span><span class="sxs-lookup"><span data-stu-id="ed124-929">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="ed124-930">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="ed124-930">Az.SignalR</span></span>
* <span data-ttu-id="ed124-931">Lägg till Update-, Restart-, CheckNameAvailability- och GetUsage-cmdletar</span><span class="sxs-lookup"><span data-stu-id="ed124-931">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="ed124-932">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ed124-932">Az.Sql</span></span>
* <span data-ttu-id="ed124-933">Uppdatera exempel i referensdokumentationen för ”Get-AzSqlElasticPool”</span><span class="sxs-lookup"><span data-stu-id="ed124-933">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="ed124-934">vCore-exempel för att skapa en elastisk pool (New-AzSqlElasticPool) har lagts till.</span><span class="sxs-lookup"><span data-stu-id="ed124-934">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="ed124-935">Ta bort verifieringen av EmailAddresses och kontrollen som bekräftar att EmailAdmins inte är falskt när EmailAddresses är tomt i Set-AzSqlServerAdvancedThreatProtectionPolicy och Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="ed124-935">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="ed124-936">Server-/databasgranskningsinställningar kan tas bort när det finns flera diagnostikinställningar som aktiverar granskningskategorin.</span><span class="sxs-lookup"><span data-stu-id="ed124-936">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="ed124-937">Åtgärda verifiering av e-postadresser i flera Sql Vulnerability Assessment-cmdletar (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting och Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="ed124-937">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ed124-938">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ed124-938">Az.Storage</span></span>
* <span data-ttu-id="ed124-939">Exempel i referensdokumentationen för ”Get-AzStorageAccountKey” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="ed124-939">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="ed124-940">Vid upp- och nedladdning av en Azure-fil kan SMB-egenskaperna för källfilen (t.ex. filattribut, tidpunkten då filen skapades och tidpunkten för den senaste skrivningen) sparas i målfilen</span><span class="sxs-lookup"><span data-stu-id="ed124-940">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="ed124-941">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="ed124-941">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="ed124-942">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="ed124-942">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="ed124-943">Korrigera problem med uppladdningen av blockblob med egenskaper/metadata för ImmutabilityPolicy i containrar.</span><span class="sxs-lookup"><span data-stu-id="ed124-943">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="ed124-944">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="ed124-944">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="ed124-945">Stöd för hantering av Azure-filresurser med API för hanteringsplan</span><span class="sxs-lookup"><span data-stu-id="ed124-945">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="ed124-946">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="ed124-946">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="ed124-947">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="ed124-947">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="ed124-948">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="ed124-948">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="ed124-949">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="ed124-949">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ed124-950">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ed124-950">Az.Websites</span></span>
* <span data-ttu-id="ed124-951">Åtgärdar problemet där webapp-taggar togs bort när appen migrerades till nya ASP</span><span class="sxs-lookup"><span data-stu-id="ed124-951">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="ed124-952">Åtgärda Publish-AzureWebapp så att det fungerar i Linux och Windows</span><span class="sxs-lookup"><span data-stu-id="ed124-952">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="ed124-953">Uppdatera exempel i ”Get-AzWebAppPublishingProfile”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="ed124-953">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="ed124-954">2.6.0 – augusti 2019</span><span class="sxs-lookup"><span data-stu-id="ed124-954">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="ed124-955">Allmänt</span><span class="sxs-lookup"><span data-stu-id="ed124-955">General</span></span>
* <span data-ttu-id="ed124-956">Åtgärdade diverse skrivfel i flera moduler</span><span class="sxs-lookup"><span data-stu-id="ed124-956">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="ed124-957">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ed124-957">Az.Accounts</span></span>
* <span data-ttu-id="ed124-958">Stöd för användartilldelat MSI i Azure Functions-autentisering (#9479)</span><span class="sxs-lookup"><span data-stu-id="ed124-958">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="ed124-959">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="ed124-959">Az.Aks</span></span>
* <span data-ttu-id="ed124-960">Åtgärda problem med utdata för "Get-AzAks"</span><span class="sxs-lookup"><span data-stu-id="ed124-960">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="ed124-961">Mer information här: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="ed124-961">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="ed124-962">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ed124-962">Az.ApiManagement</span></span>
* <span data-ttu-id="ed124-963">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="ed124-963">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="ed124-964">Uppdatera .net-NuGet-versionen, som inte tillämpar begränsningar för productId, apiId och userId</span><span class="sxs-lookup"><span data-stu-id="ed124-964">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="ed124-965">**Get-AzApiManagementProduct** – Lade till stöd för frågekörning mot produkter via API.</span><span class="sxs-lookup"><span data-stu-id="ed124-965">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="ed124-966">**New-AzApiManagementApiRevision** – Korrigering för problem där ApiRevisionDescription inte angavs vid skapande av ny API-revision https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="ed124-966">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="ed124-967">Åtgärdade skrivfel i modellen "PsApiManagementOAuth2AuthrozationServer" till "PsApiManagementOAuth2AuthorizationServer"</span><span class="sxs-lookup"><span data-stu-id="ed124-967">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="ed124-968">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="ed124-968">Az.Batch</span></span>
* <span data-ttu-id="ed124-969">Åtgärdade skrivfel i hjälpmeddelande och dokumentation till att skriva Windows med versaler</span><span class="sxs-lookup"><span data-stu-id="ed124-969">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="ed124-970">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="ed124-970">Az.Cdn</span></span>
* <span data-ttu-id="ed124-971">Åtgärdade skrivfel i CDN-modulens konverteringshjälp</span><span class="sxs-lookup"><span data-stu-id="ed124-971">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ed124-972">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ed124-972">Az.Compute</span></span>
* <span data-ttu-id="ed124-973">Lägg till VmssId i New-AzVMConfig-cmdleten</span><span class="sxs-lookup"><span data-stu-id="ed124-973">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="ed124-974">Lägg till parametrarna TerminateScheduledEvents och TerminateScheduledEventNotBeforeTimeoutInMinutes i New-AzVmssConfig och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ed124-974">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="ed124-975">Lägg till egenskapen HyperVGeneration till avbildningsobjekt för virtuell dator</span><span class="sxs-lookup"><span data-stu-id="ed124-975">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="ed124-976">Lägg till funktioner för Host och HostGroup</span><span class="sxs-lookup"><span data-stu-id="ed124-976">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="ed124-977">Nya cmdletar:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="ed124-977">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="ed124-978">HostId-parametern läggs till i New-AzVMConfig och New-AzVM</span><span class="sxs-lookup"><span data-stu-id="ed124-978">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="ed124-979">Uppdatera exempel i "Invoke-AzVMRunCommand"-dokumentationen till att använda rätt parameternamn</span><span class="sxs-lookup"><span data-stu-id="ed124-979">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="ed124-980">Uppdatera "-VolumeType"-beskrivningen i referensdokumentationen för "set-AzVMDiskEncryptionExtension" och "set-AzVmssDiskEncryptionExtension"</span><span class="sxs-lookup"><span data-stu-id="ed124-980">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ed124-981">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ed124-981">Az.DataFactory</span></span>
* <span data-ttu-id="ed124-982">Åtgärda skrivfel till att använda versaler för "Windows" i "New-AzDataFactoryEncryptValue"-dokumentationen</span><span class="sxs-lookup"><span data-stu-id="ed124-982">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="ed124-983">Uppdaterade ADF .Net SDK-versionen till 4.1.2</span><span class="sxs-lookup"><span data-stu-id="ed124-983">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="ed124-984">Lägg till parametrarna "DataProxyIntegrationRuntimeName", "DataProxyStagingLinkedServiceName" och "DataProxyStagingPath" för "Set-AzureRmDataFactoryV2IntegrationRuntime"-cmd för att aktivera konfiguration av lokalt installerad integrationskörning som en proxy för SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="ed124-984">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="ed124-985">Uppdaterade PSTriggerRun till att visa utlöst pipeline, meddelande och egenskaper samt PSActivityRun till att visa aktivitetstypen</span><span class="sxs-lookup"><span data-stu-id="ed124-985">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ed124-986">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ed124-986">Az.DataLakeStore</span></span>
* <span data-ttu-id="ed124-987">Korrigering av frysning av Get-DataLakeStoreDeletedItem för fel eller fjärrundantag.</span><span class="sxs-lookup"><span data-stu-id="ed124-987">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="ed124-988">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="ed124-988">Az.EventHub</span></span>
* <span data-ttu-id="ed124-989">Korrigering av problem #9658 : Skrivfel i parametern VirtualNteworkRule i Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="ed124-989">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="ed124-990">Korrigering av problem #9558 : Set-AzEventHubNamespace använder PATCH i stället för PUT</span><span class="sxs-lookup"><span data-stu-id="ed124-990">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="ed124-991">lade till parametern EnableKafka i Set-AzEventHubNamespace-cmdleten</span><span class="sxs-lookup"><span data-stu-id="ed124-991">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="ed124-992">Korrigering av problem #9786 : kan inte skapa en regel med Endast lyssna-behörighet</span><span class="sxs-lookup"><span data-stu-id="ed124-992">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="ed124-993">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="ed124-993">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="ed124-994">Åtgärdade skrivfel i dokumentation där "Azure" skrevs helt med gemener</span><span class="sxs-lookup"><span data-stu-id="ed124-994">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ed124-995">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ed124-995">Az.Monitor</span></span>
* <span data-ttu-id="ed124-996">Åtgärdade felaktigt parameternamn i hjälpdokumentationen</span><span class="sxs-lookup"><span data-stu-id="ed124-996">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ed124-997">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ed124-997">Az.Network</span></span>
* <span data-ttu-id="ed124-998">Uppdaterade New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="ed124-998">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="ed124-999">Gjorde parametern "PublicIpAddress" inaktuell eftersom den aldrig används på serversidan.</span><span class="sxs-lookup"><span data-stu-id="ed124-999">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="ed124-1000">Lade till den valfria parametern "Primary", som anger huruvida den aktuella IP-konfigurationen är den primära.</span><span class="sxs-lookup"><span data-stu-id="ed124-1000">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="ed124-1001">Förbättrade hanteringen av felundantag för begärande från SDK – åtgärdar problemet att tidigare SDK-undantag inte hanteras på rätt sätt, vilket leder till att viktig felinformation inte visas</span><span class="sxs-lookup"><span data-stu-id="ed124-1001">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="ed124-1002">Justerade valideringslogiken för IPv6-IP-prefix till att kontrollera korrekt IPv6-prefixlängd.</span><span class="sxs-lookup"><span data-stu-id="ed124-1002">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="ed124-1003">Uppdaterade Get-AzVirtualNetworkSubnetConfig: Lade till parameter som anges till get av undernätets resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="ed124-1003">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="ed124-1004">Uppdaterade beskrivningen av parametern Location för AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="ed124-1004">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="ed124-1005">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ed124-1005">Az.OperationalInsights</span></span>
* <span data-ttu-id="ed124-1006">Uppdaterade dokumentation för "New-AzOperationalInsightsLinuxSyslogDataSource"</span><span class="sxs-lookup"><span data-stu-id="ed124-1006">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="ed124-1007">Lade till exempel</span><span class="sxs-lookup"><span data-stu-id="ed124-1007">Added example</span></span>
    - <span data-ttu-id="ed124-1008">Uppdaterade beskrivningen av parametern "-Name"</span><span class="sxs-lookup"><span data-stu-id="ed124-1008">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="ed124-1009">Lade till ett exempel för New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="ed124-1009">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="ed124-1010">Ändrade beskrivningen av parametern -Name för New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="ed124-1010">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ed124-1011">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ed124-1011">Az.RecoveryServices</span></span>
* <span data-ttu-id="ed124-1012">Uppdatera "Get-AzRecoveryServicesBackupJobDetail.md"</span><span class="sxs-lookup"><span data-stu-id="ed124-1012">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="ed124-1013">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ed124-1013">Az.Resources</span></span>
* <span data-ttu-id="ed124-1014">Lägg till stöd för den nya API-versionen från 2019-05-10 för Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="ed124-1014">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="ed124-1015">Lägg till stöd för "copy.count = 0" för variabler, resurser och egenskaper</span><span class="sxs-lookup"><span data-stu-id="ed124-1015">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="ed124-1016">Resurser med "condition = false" eller "copy.count = 0" tas bort i complete-läget</span><span class="sxs-lookup"><span data-stu-id="ed124-1016">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="ed124-1017">Lägg till ett exempel på tilldelning av princip på prenumerationsnivå i hjälpdokumentationen</span><span class="sxs-lookup"><span data-stu-id="ed124-1017">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="ed124-1018">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ed124-1018">Az.ServiceBus</span></span>
* <span data-ttu-id="ed124-1019">Korrigering av problem #9658 : Skrivfel i parametern VirtualNetworkRule i set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="ed124-1019">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="ed124-1020">Korrigering av problem #9786 : kan inte skapa en regel med Endast lyssna-behörighet</span><span class="sxs-lookup"><span data-stu-id="ed124-1020">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="ed124-1021">Lade till det nya kommandot "Test-AzServiceBusNameAvailability" för att kontrollera namntillgängligheten för kö och ämne</span><span class="sxs-lookup"><span data-stu-id="ed124-1021">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="ed124-1022">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ed124-1022">Az.ServiceFabric</span></span>
* <span data-ttu-id="ed124-1023">Åtgärda buggar med tillägg av nodtyps-cmdlet:</span><span class="sxs-lookup"><span data-stu-id="ed124-1023">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="ed124-1024">NullReferenceException-bugg när resursgrupp hade annan vmss som inte är relaterad till Service Fabric-klustret.</span><span class="sxs-lookup"><span data-stu-id="ed124-1024">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="ed124-1025">Åtgärdar problemet: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="ed124-1025">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="ed124-1026">Åtgärda bugg där cmdleten misslyckades om virtualNetwork var i en annan resursgrupp än klustret.</span><span class="sxs-lookup"><span data-stu-id="ed124-1026">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="ed124-1027">Åtgärdar problemet: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="ed124-1027">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="ed124-1028">AzServiceFabricApplicationCertificate-cmdleten görs inaktuell</span><span class="sxs-lookup"><span data-stu-id="ed124-1028">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="ed124-1029">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ed124-1029">Az.Sql</span></span>
* <span data-ttu-id="ed124-1030">Uppdatera dokumentation om gamla gransknings-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="ed124-1030">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ed124-1031">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ed124-1031">Az.Storage</span></span>
* <span data-ttu-id="ed124-1032">Uppdatera hjälpen för Get/Close-AzStorageFileHandle genom att lägga till fler scenarier i cmdlet-exempel och uppdatera parameterbeskrivningar</span><span class="sxs-lookup"><span data-stu-id="ed124-1032">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="ed124-1033">Stöd för StandardBlobTier i uppladdningsblob och kopieringsblob</span><span class="sxs-lookup"><span data-stu-id="ed124-1033">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="ed124-1034">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="ed124-1034">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="ed124-1035">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="ed124-1035">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="ed124-1036">Stöd för rehydratiseringsprioritet i kopieringsblob</span><span class="sxs-lookup"><span data-stu-id="ed124-1036">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="ed124-1037">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="ed124-1037">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ed124-1038">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ed124-1038">Az.Websites</span></span>
* <span data-ttu-id="ed124-1039">Lägg till klargöranden gällande parametern -AppSettings i Set-AzWebApp och Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ed124-1039">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="ed124-1040">2.5.0 – July 2019</span><span class="sxs-lookup"><span data-stu-id="ed124-1040">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ed124-1041">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ed124-1041">Az.Accounts</span></span>
* <span data-ttu-id="ed124-1042">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="ed124-1042">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="ed124-1043">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="ed124-1043">Az.ApplicationInsights</span></span>
* <span data-ttu-id="ed124-1044">Korrigera skrivfel i exempel i dokumentationen för Remove-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="ed124-1044">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ed124-1045">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ed124-1045">Az.Automation</span></span>
* <span data-ttu-id="ed124-1046">Korrigera skrivfel i resurssträng</span><span class="sxs-lookup"><span data-stu-id="ed124-1046">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="ed124-1047">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ed124-1047">Az.CognitiveServices</span></span>
* <span data-ttu-id="ed124-1048">Stöd för NetworkRuleSet har lagts till.</span><span class="sxs-lookup"><span data-stu-id="ed124-1048">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ed124-1049">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ed124-1049">Az.Compute</span></span>
* <span data-ttu-id="ed124-1050">Lägg till saknade egenskaper (ComputerName, OsName, OsVersion och HyperVGeneration) för visningsobjekt i den virtuella datorinstansen.</span><span class="sxs-lookup"><span data-stu-id="ed124-1050">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="ed124-1051">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ed124-1051">Az.ContainerRegistry</span></span>
* <span data-ttu-id="ed124-1052">Åtgärda skrivfel i Remove-AzContainerRegistryReplication för parametern Replication</span><span class="sxs-lookup"><span data-stu-id="ed124-1052">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="ed124-1053">Mer information finns här: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="ed124-1053">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ed124-1054">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ed124-1054">Az.DataFactory</span></span>
* <span data-ttu-id="ed124-1055">ADF .Net SDK-versionen har uppdaterats till 4.1.0</span><span class="sxs-lookup"><span data-stu-id="ed124-1055">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="ed124-1056">Korrigera skrivfel i dokumentationen för Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="ed124-1056">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="ed124-1057">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="ed124-1057">Az.EventHub</span></span>
* <span data-ttu-id="ed124-1058">Ny cmmdlet har lagts till för att skapa SAS-token: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="ed124-1058">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="ed124-1059">verifierings- och felmeddelande har lagts till för authorizationrules-rättigheter om endast "hantera" har tilldelats</span><span class="sxs-lookup"><span data-stu-id="ed124-1059">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="ed124-1060">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ed124-1060">Az.KeyVault</span></span>
* <span data-ttu-id="ed124-1061">Stöd har lagts till för att ange KeySize för certifikatprinciper</span><span class="sxs-lookup"><span data-stu-id="ed124-1061">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="ed124-1062">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="ed124-1062">Az.LogicApp</span></span>
* <span data-ttu-id="ed124-1063">Korrigering för Get-AzIntegrationAccountMap för att lista alla mappningstyper</span><span class="sxs-lookup"><span data-stu-id="ed124-1063">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="ed124-1064">Ny MapType-parameter har lagts till för filtrering</span><span class="sxs-lookup"><span data-stu-id="ed124-1064">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="ed124-1065">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="ed124-1065">Az.ManagedServices</span></span>
* <span data-ttu-id="ed124-1066">Stöd för API-versionen 2019-06-01 (GA) har lagts till</span><span class="sxs-lookup"><span data-stu-id="ed124-1066">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ed124-1067">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ed124-1067">Az.Network</span></span>
* <span data-ttu-id="ed124-1068">Lägg till stöd för privat slutpunkt och privat länktjänst</span><span class="sxs-lookup"><span data-stu-id="ed124-1068">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="ed124-1069">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="ed124-1069">New cmdlets</span></span>
        - <span data-ttu-id="ed124-1070">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="ed124-1070">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="ed124-1071">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ed124-1071">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="ed124-1072">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ed124-1072">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="ed124-1073">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ed124-1073">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="ed124-1074">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ed124-1074">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="ed124-1075">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ed124-1075">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="ed124-1076">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="ed124-1076">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="ed124-1077">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ed124-1077">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="ed124-1078">Nedanstående kommandon för funktionen har uppdaterats: Flaggan PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies på undernätet i VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ed124-1078">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="ed124-1079">Uppdaterade New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="ed124-1079">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="ed124-1080">Valfri parameter har lagts till – PrivateEndpointNetworkPoliciesFlag som konfigurerar huruvida nätverksprinciper ska tillämpas på en privat slutpunkt i det här undernätet.</span><span class="sxs-lookup"><span data-stu-id="ed124-1080">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="ed124-1081">Valfri parameter har lagts till – PrivateLinkServiceNetworkPoliciesFlag som konfigurerar huruvida nätverksprinciper ska tillämpas på en privat länktjänst i det här undernätet.</span><span class="sxs-lookup"><span data-stu-id="ed124-1081">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="ed124-1082">AzPrivateLinkService för cmdlet-parametern ServiceName har bytt namn till Name med aliaset ServiceName för bakåtkompatibilitet</span><span class="sxs-lookup"><span data-stu-id="ed124-1082">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="ed124-1083">Aktivera ICMP-protokoll för konfiguration av nätverkssäkerhetsregler</span><span class="sxs-lookup"><span data-stu-id="ed124-1083">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="ed124-1084">Uppdaterade cmdletar</span><span class="sxs-lookup"><span data-stu-id="ed124-1084">Updated cmdlets</span></span>
        - <span data-ttu-id="ed124-1085">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ed124-1085">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="ed124-1086">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ed124-1086">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="ed124-1087">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ed124-1087">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="ed124-1088">Lägg till ConnectionProtocolType (Ikev1/Ikev2) som en konfigurerbar parameter för New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ed124-1088">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="ed124-1089">Lägg till PrivateIpAddressVersion i LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="ed124-1089">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="ed124-1090">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="ed124-1090">Updated cmdlet:</span></span>
        - <span data-ttu-id="ed124-1091">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ed124-1091">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="ed124-1092">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ed124-1092">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="ed124-1093">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ed124-1093">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="ed124-1094">Uppdatering av Application Gateway-kommandot New-AzApplicationGatewayProbeConfig för stöd av anpassad port i Probe</span><span class="sxs-lookup"><span data-stu-id="ed124-1094">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="ed124-1095">Uppdaterade New-AzApplicationGatewayProbeConfig: Den valfria parametern Port som används för avsökning i serverdelen har lagts till.</span><span class="sxs-lookup"><span data-stu-id="ed124-1095">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="ed124-1096">Denna parameter gäller för SKU:erna Standard_V2 och WAF_V2.</span><span class="sxs-lookup"><span data-stu-id="ed124-1096">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="ed124-1097">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ed124-1097">Az.OperationalInsights</span></span>
* <span data-ttu-id="ed124-1098">Uppdaterade standardversionen för sparade sökningar till 1.</span><span class="sxs-lookup"><span data-stu-id="ed124-1098">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="ed124-1099">Åtgärdade hantering av anpassad log null regex</span><span class="sxs-lookup"><span data-stu-id="ed124-1099">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ed124-1100">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ed124-1100">Az.RecoveryServices</span></span>
* <span data-ttu-id="ed124-1101">Uppdatera Get-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="ed124-1101">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="ed124-1102">Uppdatera Get-AzRecoveryServicesBackupContainer.md</span><span class="sxs-lookup"><span data-stu-id="ed124-1102">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="ed124-1103">Uppdatera Get-AzRecoveryServicesVault.md</span><span class="sxs-lookup"><span data-stu-id="ed124-1103">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="ed124-1104">Uppdatera Wait-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="ed124-1104">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="ed124-1105">Uppdatera Set-AzRecoveryServicesVaultContext.md</span><span class="sxs-lookup"><span data-stu-id="ed124-1105">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="ed124-1106">Uppdatera Get-AzRecoveryServicesBackupItem.md</span><span class="sxs-lookup"><span data-stu-id="ed124-1106">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="ed124-1107">Uppdatera Get-AzRecoveryServicesBackupRecoveryPoint.md</span><span class="sxs-lookup"><span data-stu-id="ed124-1107">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="ed124-1108">Uppdatera Restore-AzRecoveryServicesBackupItem.md</span><span class="sxs-lookup"><span data-stu-id="ed124-1108">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="ed124-1109">Uppdaterat tjänstanrop för avregistrering av container för Azure-filresurs</span><span class="sxs-lookup"><span data-stu-id="ed124-1109">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="ed124-1110">Uppdatera Set-AzRecoveryServicesAsrAlertSetting.md</span><span class="sxs-lookup"><span data-stu-id="ed124-1110">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="ed124-1111">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ed124-1111">Az.Resources</span></span>
- <span data-ttu-id="ed124-1112">Ta bort den cmdlet som saknas och som refereras i dokumentationen till New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ed124-1112">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="ed124-1113">Princip-cmdletar har uppdaterats så att de använder den nya API-versionen 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="ed124-1113">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="ed124-1114">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ed124-1114">Az.ServiceBus</span></span>
* <span data-ttu-id="ed124-1115">Ny cmmdlet har lagts till för att skapa SAS-token: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="ed124-1115">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="ed124-1116">verifierings- och felmeddelande har lagts till för authorizationrules-rättigheter om endast "hantera" har tilldelats</span><span class="sxs-lookup"><span data-stu-id="ed124-1116">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="ed124-1117">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ed124-1117">Az.Sql</span></span>
* <span data-ttu-id="ed124-1118">Åtgärda saknade exempel för Set-AzSqlDatabaseSecondary cmdlet</span><span class="sxs-lookup"><span data-stu-id="ed124-1118">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="ed124-1119">Åtgärda angivna återkommande genomsökningar för bedömning av säkerhetsrisk utan angivna e-postadresser</span><span class="sxs-lookup"><span data-stu-id="ed124-1119">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="ed124-1120">Korrigera ett skrivfel i ett varningsmeddelande.</span><span class="sxs-lookup"><span data-stu-id="ed124-1120">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ed124-1121">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ed124-1121">Az.Storage</span></span>
* <span data-ttu-id="ed124-1122">Uppdatera exempel i referensdokumentationen för Get-AzStorageAccount så att rätt parameternamn används</span><span class="sxs-lookup"><span data-stu-id="ed124-1122">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="ed124-1123">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="ed124-1123">Az.StorageSync</span></span>
* <span data-ttu-id="ed124-1124">Lägger till cmdleten Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="ed124-1124">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="ed124-1125">Åtgärda problem 9551 så att TierFilesOlderThanDays föredras</span><span class="sxs-lookup"><span data-stu-id="ed124-1125">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ed124-1126">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ed124-1126">Az.Websites</span></span>
* <span data-ttu-id="ed124-1127">Åtgärdar ett fel där vissa SiteConfig-egenskaper inte returnerades av Get-AzWebApp och Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ed124-1127">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="ed124-1128">Lägger till en ny platsparameter för Get-AzDeletedWebApp och Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="ed124-1128">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="ed124-1129">Åtgärdar ett fel i kloning av webbapp-platser som använder New-AzWebApp-IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="ed124-1129">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="ed124-1130">2.4.0 – juli 2019</span><span class="sxs-lookup"><span data-stu-id="ed124-1130">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ed124-1131">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ed124-1131">Az.Accounts</span></span>
* <span data-ttu-id="ed124-1132">Lägg till stöd för profil-cmdletar</span><span class="sxs-lookup"><span data-stu-id="ed124-1132">Add support for profile cmdlets</span></span>
* <span data-ttu-id="ed124-1133">Lägg till stöd för miljöer och dataplaner i genererade cmdletar</span><span class="sxs-lookup"><span data-stu-id="ed124-1133">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="ed124-1134">Åtgärda bugg där fel slutpunkt i vissa fall användes för cmdletar för dataplaner i Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="ed124-1134">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="ed124-1135">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="ed124-1135">Az.Advisor</span></span>
* <span data-ttu-id="ed124-1136">GA-version av Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="ed124-1136">GA release of Az.Advisor</span></span>
* <span data-ttu-id="ed124-1137">Den här modulen ingår nu som en del av `Az`-sammanslagningsmodulen</span><span class="sxs-lookup"><span data-stu-id="ed124-1137">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="ed124-1138">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ed124-1138">Az.ApiManagement</span></span>
* <span data-ttu-id="ed124-1139">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="ed124-1139">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="ed124-1140">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="ed124-1140">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="ed124-1141">Stöd för att fråga prenumerationer efter användare och produkt har lagts till</span><span class="sxs-lookup"><span data-stu-id="ed124-1141">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="ed124-1142">Stöd för att fråga med hjälp av omfång ”/”, ”/apis”, ”/apis/echo-api” har lagts till</span><span class="sxs-lookup"><span data-stu-id="ed124-1142">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="ed124-1143">Korrigering av problem https://github.com/Azure/azure-powershell/issues/9307 och https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="ed124-1143">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="ed124-1144">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="ed124-1144">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="ed124-1145">Stöd för att ange ”ApiVersion” och ”ApiVersionSetId” när API:er importeras har lagts till</span><span class="sxs-lookup"><span data-stu-id="ed124-1145">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ed124-1146">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ed124-1146">Az.Automation</span></span>
* <span data-ttu-id="ed124-1147">Bugg med cmdleten Set-AzAutomationConnectionFieldValue för att hantera strängvärde har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="ed124-1147">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ed124-1148">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ed124-1148">Az.Compute</span></span>
* <span data-ttu-id="ed124-1149">Lägg till parametern HyperVGeneration i New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="ed124-1149">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ed124-1150">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ed124-1150">Az.DataFactory</span></span>
* <span data-ttu-id="ed124-1151">Uppdaterar utdata från ADF-cmdletar som hämtar aktivitetskörningar, hämtar pipelinekörningar och hämtar utlösarkörningar för stöd för Select-Object-pipe.</span><span class="sxs-lookup"><span data-stu-id="ed124-1151">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="ed124-1152">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="ed124-1152">Az.EventGrid</span></span>
* <span data-ttu-id="ed124-1153">Korrigera stavfel i dokumentation om ”New-AzEventGridSubscription”</span><span class="sxs-lookup"><span data-stu-id="ed124-1153">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ed124-1154">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ed124-1154">Az.IotHub</span></span>
* <span data-ttu-id="ed124-1155">Lägg till stöd för att återskapa principnycklar för auktorisering.</span><span class="sxs-lookup"><span data-stu-id="ed124-1155">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ed124-1156">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ed124-1156">Az.Network</span></span>
* <span data-ttu-id="ed124-1157">”RoutingPreference” har lagts till i offentliga IP-taggar</span><span class="sxs-lookup"><span data-stu-id="ed124-1157">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="ed124-1158">Förbättra exempel för referensdokumentation om ”Get-AzNetworkServiceTag”</span><span class="sxs-lookup"><span data-stu-id="ed124-1158">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="ed124-1159">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="ed124-1159">Az.PolicyInsights</span></span>
* <span data-ttu-id="ed124-1160">Åtgärda problem med null-referens i Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="ed124-1160">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="ed124-1161">Mer information här: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="ed124-1161">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="ed124-1162">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ed124-1162">Az.OperationalInsights</span></span>
* <span data-ttu-id="ed124-1163">Modellen för CustomLog-datakälla som returneras i Get-AzOperationalInsightsDataSource har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="ed124-1163">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ed124-1164">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ed124-1164">Az.RecoveryServices</span></span>
* <span data-ttu-id="ed124-1165">Kommandot get-policy för IaaSVM:er har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="ed124-1165">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="ed124-1166">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ed124-1166">Az.Resources</span></span>
    - <span data-ttu-id="ed124-1167">Korrigera hjälptext för den översta parametern i Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="ed124-1167">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="ed124-1168">Lägg till växlingsstöd på klientsidan för Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="ed124-1168">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="ed124-1169">Lägg till nya parametrar för Set-AzPolicyAssignment, -PolicyParameters och -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="ed124-1169">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="ed124-1170">En mängd dokument- och exempeluppdateringar för Policy-cmdletar</span><span class="sxs-lookup"><span data-stu-id="ed124-1170">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="ed124-1171">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ed124-1171">Az.ServiceBus</span></span>
* <span data-ttu-id="ed124-1172">Korrigering av problem #4938 – New-AzureRmServiceBusQueue returnerar BadRequest vid konfiguration av MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="ed124-1172">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="ed124-1173">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ed124-1173">Az.Sql</span></span>
* <span data-ttu-id="ed124-1174">Lägg till cmdletar för instansredundansgrupper från förhandsversion till offentlig version</span><span class="sxs-lookup"><span data-stu-id="ed124-1174">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="ed124-1175">Stöd för granskning för Azure SQL Server\Database med nya cmdletar.</span><span class="sxs-lookup"><span data-stu-id="ed124-1175">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="ed124-1176">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="ed124-1176">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="ed124-1177">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="ed124-1177">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="ed124-1178">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="ed124-1178">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="ed124-1179">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="ed124-1179">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="ed124-1180">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="ed124-1180">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="ed124-1181">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="ed124-1181">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="ed124-1182">Ta bort begränsningar för e-post från inställningarna för sårbarhetsbedömning</span><span class="sxs-lookup"><span data-stu-id="ed124-1182">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ed124-1183">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ed124-1183">Az.Storage</span></span>
* <span data-ttu-id="ed124-1184">Ändra två parametrar ”-IndexDocument” och ”-ErrorDocument404Path” från ”krävs” till ”valfri” i cmdlet:</span><span class="sxs-lookup"><span data-stu-id="ed124-1184">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="ed124-1185">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="ed124-1185">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="ed124-1186">Uppdatera hjälpen för Get-AzStorageBlobContent genom att lägga till ett exempel</span><span class="sxs-lookup"><span data-stu-id="ed124-1186">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="ed124-1187">Visa mer felinformation när cmdleten misslyckas med StorageException</span><span class="sxs-lookup"><span data-stu-id="ed124-1187">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="ed124-1188">Stöd för att skapa eller uppdatera lagringskonto med Azure Files AAD DS-autentisering</span><span class="sxs-lookup"><span data-stu-id="ed124-1188">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="ed124-1189">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ed124-1189">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="ed124-1190">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ed124-1190">Set-AzStorageAccount</span></span>
* <span data-ttu-id="ed124-1191">Stöd för att lista eller stänga filreferenser för en filresurs, filkatalog eller en fil</span><span class="sxs-lookup"><span data-stu-id="ed124-1191">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="ed124-1192">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="ed124-1192">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="ed124-1193">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="ed124-1193">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="ed124-1194">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="ed124-1194">Az.StorageSync</span></span>
* <span data-ttu-id="ed124-1195">Den här modulen ingår nu som en del av `Az`-sammanslagningsmodulen</span><span class="sxs-lookup"><span data-stu-id="ed124-1195">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="ed124-1196">2.3.2 – juni 2019</span><span class="sxs-lookup"><span data-stu-id="ed124-1196">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ed124-1197">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ed124-1197">Az.Accounts</span></span>
* <span data-ttu-id="ed124-1198">Åtgärda bugg med felaktiga webbadresser som i vissa fall användes för Functions-anrop</span><span class="sxs-lookup"><span data-stu-id="ed124-1198">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="ed124-1199">Mer information här: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="ed124-1199">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="ed124-1200">Åtgärda problem med alias från AzureRM i Az-cmdletar</span><span class="sxs-lookup"><span data-stu-id="ed124-1200">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="ed124-1201">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="ed124-1201">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="ed124-1202">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="ed124-1202">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ed124-1203">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ed124-1203">Az.Compute</span></span>
* <span data-ttu-id="ed124-1204">Parameteruppsättningarna New-AzVm och New-AzVmss accepterar nu parametern ”ProximityPlacementGroup”.</span><span class="sxs-lookup"><span data-stu-id="ed124-1204">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="ed124-1205">Stavfel i referensdokumentationen för ”New-AzVM” har korrigerats</span><span class="sxs-lookup"><span data-stu-id="ed124-1205">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="ed124-1206">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="ed124-1206">Az.Dns</span></span>
* <span data-ttu-id="ed124-1207">Stavfel i hjälpexempel för ”Set-AzDnsZone” har korrigerats.</span><span class="sxs-lookup"><span data-stu-id="ed124-1207">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="ed124-1208">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="ed124-1208">Az.EventGrid</span></span>
* <span data-ttu-id="ed124-1209">Har uppdaterats för att använda API-versionen 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="ed124-1209">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="ed124-1210">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="ed124-1210">New cmdlets:</span></span>
    - <span data-ttu-id="ed124-1211">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="ed124-1211">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="ed124-1212">Skapar en ny Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="ed124-1212">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="ed124-1213">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="ed124-1213">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="ed124-1214">Hämtar information om en Event Grid-domän eller hämtar en lista med alla Event Grid-domäner i den aktuella Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="ed124-1214">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="ed124-1215">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="ed124-1215">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="ed124-1216">Tar bort en Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="ed124-1216">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="ed124-1217">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="ed124-1217">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="ed124-1218">Återskapar nyckeln för delad åtkomst för en Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="ed124-1218">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="ed124-1219">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="ed124-1219">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="ed124-1220">Hämtar de nycklar för delad åtkomst som används för att publicera händelser till en Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="ed124-1220">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="ed124-1221">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="ed124-1221">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="ed124-1222">Skapar ett nytt Azure Event Grid-domänämne.</span><span class="sxs-lookup"><span data-stu-id="ed124-1222">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="ed124-1223">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="ed124-1223">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="ed124-1224">Hämtar information om ett Event Grid-domänämne eller hämtar en lista med alla Event Grid-domänämnen under en specifik Event Grid-domän i nuvarande Azure</span><span class="sxs-lookup"><span data-stu-id="ed124-1224">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="ed124-1225">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="ed124-1225">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="ed124-1226">Tar bort ett befintligt Azure Event Grid-domänämne.</span><span class="sxs-lookup"><span data-stu-id="ed124-1226">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="ed124-1227">Uppdaterade cmdletar:</span><span class="sxs-lookup"><span data-stu-id="ed124-1227">Updated cmdlets:</span></span>
    - <span data-ttu-id="ed124-1228">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="ed124-1228">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="ed124-1229">Lägg till nya obligatoriska parametrar för att stödja piping för den nya Event Grid-domänen och Event Grid-domänämnet för att göra det möjligt att skapa nya händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="ed124-1229">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="ed124-1230">Lägg till nya obligatoriska parametrar för att ange det nya Event Grid-domännamnet och/eller namnet på Event Grid-domänämnet för att göra det möjligt att skapa nya händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="ed124-1230">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="ed124-1231">Lägg till ny parameteruppsättningar för domäner och domänämnen för att göra det möjligt att återanvända befintliga parametrar (t.ex. EndPointType, SubjectBeginsWith osv).</span><span class="sxs-lookup"><span data-stu-id="ed124-1231">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="ed124-1232">Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="ed124-1232">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="ed124-1233">Förfallodatum för händelseprenumeration</span><span class="sxs-lookup"><span data-stu-id="ed124-1233">Event subscription expiration date,</span></span>
            - <span data-ttu-id="ed124-1234">Avancerade filterparametrar.</span><span class="sxs-lookup"><span data-stu-id="ed124-1234">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="ed124-1235">Lägg till ny uppräkning för servicebusqueue som mål.</span><span class="sxs-lookup"><span data-stu-id="ed124-1235">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="ed124-1236">Tillåt inte användning av ”Alla” i alternativet -IncludedEventType och ersätt det med</span><span class="sxs-lookup"><span data-stu-id="ed124-1236">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="ed124-1237">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="ed124-1237">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="ed124-1238">Lägg till ny valfria parametrar (Top, ODataQuery och NextLink) för att stödja sidnumrering och filtrering av resultat.</span><span class="sxs-lookup"><span data-stu-id="ed124-1238">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="ed124-1239">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="ed124-1239">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="ed124-1240">Lägg till nya obligatoriska parametrar för att stödja piping för en Event Grid-domän och Event Grid-domänämnen för att göra det möjligt att ta bort befintliga händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="ed124-1240">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="ed124-1241">Lägg till nya obligatoriska parametrar för att ange Event Grid-domännamnet och/eller namnet på Event Grid-domänämnet för att göra det möjligt att ta bort befintliga händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="ed124-1241">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="ed124-1242">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="ed124-1242">Az.FrontDoor</span></span>
* <span data-ttu-id="ed124-1243">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="ed124-1243">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="ed124-1244">Lägg till stöd för transformeringar och nytt värde för automatisk komplettering för operatorer (RegEx)</span><span class="sxs-lookup"><span data-stu-id="ed124-1244">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="ed124-1245">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="ed124-1245">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="ed124-1246">Lägg till nya värden för automatisk komplettering</span><span class="sxs-lookup"><span data-stu-id="ed124-1246">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ed124-1247">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ed124-1247">Az.Network</span></span>
* <span data-ttu-id="ed124-1248">Lägg till stöd för resurs för virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="ed124-1248">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="ed124-1249">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="ed124-1249">New cmdlets</span></span>
        - <span data-ttu-id="ed124-1250">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="ed124-1250">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="ed124-1251">Lägg till AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="ed124-1251">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="ed124-1252">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="ed124-1252">New cmdlets</span></span>
        - <span data-ttu-id="ed124-1253">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="ed124-1253">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="ed124-1254">Lägg till PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ed124-1254">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="ed124-1255">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="ed124-1255">New cmdlets</span></span>
        - <span data-ttu-id="ed124-1256">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ed124-1256">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="ed124-1257">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ed124-1257">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="ed124-1258">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ed124-1258">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="ed124-1259">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="ed124-1259">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="ed124-1260">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ed124-1260">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="ed124-1261">Lägg till PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="ed124-1261">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="ed124-1262">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="ed124-1262">New cmdlets</span></span>
        - <span data-ttu-id="ed124-1263">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="ed124-1263">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="ed124-1264">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="ed124-1264">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="ed124-1265">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="ed124-1265">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="ed124-1266">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="ed124-1266">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="ed124-1267">Nedanstående kommandon för funktionen har uppdaterats: Flaggan UseLocalAzureIpAddress på VpnConnection</span><span class="sxs-lookup"><span data-stu-id="ed124-1267">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="ed124-1268">New-AzVpnConnection har uppdaterats: Den valfria parametern -UseLocalAzureIpAddress har lagts till för att visa att en lokal IP-adress i Azure ska användas som källadress när anslutningen initieras.</span><span class="sxs-lookup"><span data-stu-id="ed124-1268">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="ed124-1269">Set-AzVpnConnection har uppdaterats: Den valfria parametern -UseLocalAzureIpAddress har lagts till för att visa att en lokal IP-adress i Azure ska användas som källadress när anslutningen initieras.</span><span class="sxs-lookup"><span data-stu-id="ed124-1269">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="ed124-1270">Det skrivskyddade fältet PeeredConnections har lagts till i ExpressRoute-peering.</span><span class="sxs-lookup"><span data-stu-id="ed124-1270">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="ed124-1271">Det skrivskyddade fältet GlobalReachEnabled har lagts till i ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="ed124-1271">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="ed124-1272">Ett attribut för icke-bakåtkompatibla ändringar har lagts till för att lyfta fram utfasning av fältet AllowGlobalReach i modellen ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ed124-1272">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="ed124-1273">Problem 8756 har åtgärdats: Fel vid användning av TargetListenerID med AzApplicationGatewayRedirectConfiguration-cmdletar</span><span class="sxs-lookup"><span data-stu-id="ed124-1273">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="ed124-1274">En bugg i New-AzApplicationGatewayPathRuleConfig som gjorde att regeluppsättningen för att återskapa inte kunde anges har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="ed124-1274">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="ed124-1275">Visningen av VirtualNetworkTaps i NetworkInterfaceIpConfiguration har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="ed124-1275">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="ed124-1276">Cortex Get-cmdletar för att visa en lista med alla delar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="ed124-1276">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="ed124-1277">Funktionen för att skapa VirtualHub-referenser för ExpressRouteGateways och VpnGateway har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="ed124-1277">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="ed124-1278">Stöd för tillgänglighetszoner i AzureFirewall och NatGateway har lagts till</span><span class="sxs-lookup"><span data-stu-id="ed124-1278">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="ed124-1279">Cmdleten Get-AzNetworkServiceTag har lagts till</span><span class="sxs-lookup"><span data-stu-id="ed124-1279">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="ed124-1280">Lägg till stöd för flera offentliga IP-adresser för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="ed124-1280">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="ed124-1281">Cmdleten New-AzFirewall har uppdaterats:</span><span class="sxs-lookup"><span data-stu-id="ed124-1281">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="ed124-1282">Parametern -PublicIpAddress som accepterar ett eller flera offentliga IP-adressobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="ed124-1282">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="ed124-1283">Parametern -VirtualNetwork som accepterar ett virtuellt nätverksobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="ed124-1283">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="ed124-1284">Metoderna AddPublicIpAddress och RemovePublicIpAddress har lagts till på brandväggsobjekt – dessa accepterar ett offentligt IP-adressobjekt som indata</span><span class="sxs-lookup"><span data-stu-id="ed124-1284">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="ed124-1285">Inaktuella parametrar -PublicIpName och -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="ed124-1285">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="ed124-1286">Nedanstående kommandon för funktionen har uppdaterats: Ange autentiseringsalternativ för VpnClient AAD till resurser för virtuella nätverksgatewayer.</span><span class="sxs-lookup"><span data-stu-id="ed124-1286">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="ed124-1287">New-AzVirtualNetworkGateway har uppdaterats: De valfria parametrarna AadTenantUri, AadAudienceId och AadIssuerUri för att ange VpnClient AAD-autentiseringsalternativ på en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="ed124-1287">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="ed124-1288">Set-AzVirtualNetworkGateway har uppdaterats: De valfria parametrarna AadTenantUri, AadAudienceId och AadIssuerUri för att ange VpnClient AAD-autentiseringsalternativ på en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="ed124-1288">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="ed124-1289">Set-AzVirtualNetworkGateway har uppdaterats: Den valfria växelparametern RemoveAadAuthentication som tar bort VpnClient AAD-autentiseringsalternativ från en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="ed124-1289">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="ed124-1290">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ed124-1290">Az.OperationalInsights</span></span>
* <span data-ttu-id="ed124-1291">Aktivera prisnivån **pergb2018** i kommandot ”New-AzureRmOperationalInsightsWorkspace”</span><span class="sxs-lookup"><span data-stu-id="ed124-1291">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="ed124-1292">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ed124-1292">Az.Resources</span></span>
* <span data-ttu-id="ed124-1293">Stöd för ytterligare alternativ för att exportera en mall</span><span class="sxs-lookup"><span data-stu-id="ed124-1293">Support for additional Template Export options</span></span>
    - <span data-ttu-id="ed124-1294">Lägg till parametern ”-SkipResourceNameParameterization” till Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ed124-1294">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="ed124-1295">Lägg till parametern ”-SkipAllParameterization” till Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ed124-1295">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="ed124-1296">Lägg till parametern ”-Resource” till Export-AzResourceGroup för exporterad resursfiltrering</span><span class="sxs-lookup"><span data-stu-id="ed124-1296">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="ed124-1297">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ed124-1297">Az.ServiceFabric</span></span>
* <span data-ttu-id="ed124-1298">Åtgärda att fel tumavtryck används vid tilläggning av certifikat i ByExistingKeyVault i vissa fall</span><span class="sxs-lookup"><span data-stu-id="ed124-1298">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="ed124-1299">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ed124-1299">Az.Sql</span></span>
* <span data-ttu-id="ed124-1300">Åtgärda suffix för lagringsslutpunkt i Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="ed124-1300">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="ed124-1301">Åtgärda att aktivering av Advanced Data Security åsidosätter Advanced Threat Protection-princip</span><span class="sxs-lookup"><span data-stu-id="ed124-1301">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="ed124-1302">Nya cmdletar för Management.Sql som gör att kunderna kan lägga till nycklar för transparent datakryptering (TDE) och ange TDE-skydd för hanterade instanser</span><span class="sxs-lookup"><span data-stu-id="ed124-1302">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="ed124-1303">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ed124-1303">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="ed124-1304">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ed124-1304">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="ed124-1305">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ed124-1305">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="ed124-1306">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="ed124-1306">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="ed124-1307">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="ed124-1307">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ed124-1308">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ed124-1308">Az.Storage</span></span>
* <span data-ttu-id="ed124-1309">Stöd för typerna FileStorage och SkuName Premium_ZRS när lagringskonton skapas</span><span class="sxs-lookup"><span data-stu-id="ed124-1309">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="ed124-1310">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ed124-1310">New-AzStorageAccount</span></span>
* <span data-ttu-id="ed124-1311">Beskrivningen av cmdleten för bloboföränderlighet har förtydligats</span><span class="sxs-lookup"><span data-stu-id="ed124-1311">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="ed124-1312">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="ed124-1312">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ed124-1313">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ed124-1313">Az.Websites</span></span>
* <span data-ttu-id="ed124-1314">Optimerar Get-AzWebAppCertificate för att filtrera efter resursgrupp på servern i stället för klienten</span><span class="sxs-lookup"><span data-stu-id="ed124-1314">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="ed124-1315">Lägger till växlingsparametern -UseDisasterRecovery till Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="ed124-1315">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="ed124-1316">2.2.0 – juni 2019</span><span class="sxs-lookup"><span data-stu-id="ed124-1316">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="ed124-1317">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="ed124-1317">Az.Cdn</span></span>
* <span data-ttu-id="ed124-1318">Uppdaterade cmdletar för att ge stöd för rulesEngine-funktion baserat på API-version 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="ed124-1318">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ed124-1319">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ed124-1319">Az.Compute</span></span>
* <span data-ttu-id="ed124-1320">Lade till parameter `NoWait` som startar åtgärden och returnerar omedelbart, innan åtgärden har slutförts.</span><span class="sxs-lookup"><span data-stu-id="ed124-1320">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="ed124-1321">Uppdaterade cmdletar:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="ed124-1321">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="ed124-1322">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="ed124-1322">Az.EventHub</span></span>
* <span data-ttu-id="ed124-1323">Korrigering för #9231 – Get-AzEventHubNamespace returnerar inga taggar</span><span class="sxs-lookup"><span data-stu-id="ed124-1323">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="ed124-1324">Korrigering för #9230 – Get-AzEventHubNamespace returnerar ResourceGroup istället för ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed124-1324">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ed124-1325">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ed124-1325">Az.Network</span></span>
* <span data-ttu-id="ed124-1326">Uppdatera ResourceId och InputObject för NAT-gateway</span><span class="sxs-lookup"><span data-stu-id="ed124-1326">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="ed124-1327">Lägg till alias för ResourceId och InputObject</span><span class="sxs-lookup"><span data-stu-id="ed124-1327">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="ed124-1328">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="ed124-1328">Az.PolicyInsights</span></span>
* <span data-ttu-id="ed124-1329">Åtgärda Null-referensproblem i Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="ed124-1329">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ed124-1330">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ed124-1330">Az.RecoveryServices</span></span>
* <span data-ttu-id="ed124-1331">Minsta kvarhållning för IaaSVM-policy i dagar ändrat till 7 från 1</span><span class="sxs-lookup"><span data-stu-id="ed124-1331">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="ed124-1332">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ed124-1332">Az.ServiceBus</span></span>
* <span data-ttu-id="ed124-1333">Korrigering för ärende #9182 – Get-AzServiceBusNamespace returnerar ResourceGroup istället för ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed124-1333">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="ed124-1334">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ed124-1334">Az.ServiceFabric</span></span>
* <span data-ttu-id="ed124-1335">Åtgärda stavfel i felmeddelandet för Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="ed124-1335">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="ed124-1336">Åtgärda saknat tecken i Service Fabric-kommandorader</span><span class="sxs-lookup"><span data-stu-id="ed124-1336">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="ed124-1337">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ed124-1337">Az.Sql</span></span>
* <span data-ttu-id="ed124-1338">Lägg till parametern DnsZonePartner för New-AzureSqlInstance-cmdlet för att ge stöd för AutoDr för hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="ed124-1338">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="ed124-1339">Avvecklar cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="ed124-1339">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="ed124-1340">Döp om cmdletar för hotidentifiering till Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="ed124-1340">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="ed124-1341">Parametrarna New-AzSqlInstance -StorageSizeInGB och -LicenseType är nu valfria.</span><span class="sxs-lookup"><span data-stu-id="ed124-1341">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ed124-1342">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ed124-1342">Az.Websites</span></span>
* <span data-ttu-id="ed124-1343">åtgärdar problemet där användningen av Set-AzWebApp och Set-AzWebAppSlot med -WebApp-egenskap tog bort taggarna</span><span class="sxs-lookup"><span data-stu-id="ed124-1343">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="ed124-1344">2.1.0 – maj 2019</span><span class="sxs-lookup"><span data-stu-id="ed124-1344">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="ed124-1345">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ed124-1345">Az.ApiManagement</span></span>
* <span data-ttu-id="ed124-1346">Skapade nya cmdletar för att hantera diagnostik för global- och API-omfång</span><span class="sxs-lookup"><span data-stu-id="ed124-1346">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="ed124-1347">**Get-AzApiManagementDiagnostic** – Skaffa diagnostik konfigurerad för global- eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="ed124-1347">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="ed124-1348">**New-AzApiManagementDiagnostic** – Skapa ny diagnostik för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="ed124-1348">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="ed124-1349">**New-AzApiManagementHttpMessageDiagnostic** – Skapa diagnostikinställning om vilka rubriker som ska loggas och storleken på brödtextbyte</span><span class="sxs-lookup"><span data-stu-id="ed124-1349">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="ed124-1350">**New-AzApiManagementPipelineDiagnosticSetting** – Skapa diagnostikinställningar för inkommande/utgående HTTP-meddelanden till gatewayen.</span><span class="sxs-lookup"><span data-stu-id="ed124-1350">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="ed124-1351">**New-AzApiManagementSamplingSetting** – Skapa samplinginställningar för begäranden/svar för en diagnostik</span><span class="sxs-lookup"><span data-stu-id="ed124-1351">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="ed124-1352">**Remove-AzApiManagementDiagnostic** – Ta bort en diagnostikenhet för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="ed124-1352">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="ed124-1353">**Set-AzApiManagementDiagnostic** – Uppdatera en diagnostikenhet för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="ed124-1353">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="ed124-1354">Skapade nya cmdletar för hantering av cacheminne i ApiManagement-tjänsten</span><span class="sxs-lookup"><span data-stu-id="ed124-1354">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="ed124-1355">**Get-AzApiManagementCache** – Hämta information om cacheminnet som anges av identifierare eller alla cacheminnen</span><span class="sxs-lookup"><span data-stu-id="ed124-1355">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="ed124-1356">**New-AzApiManagementCache** – Skapa ett nytt default-cacheminne eller cacheminne i en viss Azure-region</span><span class="sxs-lookup"><span data-stu-id="ed124-1356">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="ed124-1357">**Remove-AzApiManagementCache** – Ta bort ett cacheminne</span><span class="sxs-lookup"><span data-stu-id="ed124-1357">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="ed124-1358">**Remove-AzApiManagementCache** – Ta bort ett cacheminne</span><span class="sxs-lookup"><span data-stu-id="ed124-1358">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="ed124-1359">Skapade nya cmdletar för hantering av API-schema</span><span class="sxs-lookup"><span data-stu-id="ed124-1359">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="ed124-1360">**New-AzApiManagementSchema** – Skapa ett nytt schema för ett API</span><span class="sxs-lookup"><span data-stu-id="ed124-1360">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="ed124-1361">**Get-AzApiManagementSchema** – Hämta de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="ed124-1361">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="ed124-1362">**Remove-AzApiManagementSchema** – Ta bort de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="ed124-1362">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="ed124-1363">**Set-AzApiManagementSchema** – Uppdatera de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="ed124-1363">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="ed124-1364">Skapa ny cmdlet för att generera en användartoken.</span><span class="sxs-lookup"><span data-stu-id="ed124-1364">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="ed124-1365">**New-AzApiManagementUserToken** – Skapa en ny användartoken som enligt standardinställning är giltig i 8 timmar. Token för GIT-användaren kan skapas med den här cmdleten./</span><span class="sxs-lookup"><span data-stu-id="ed124-1365">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="ed124-1366">Skapade en ny cmdlet för att hämta nätverksstatus</span><span class="sxs-lookup"><span data-stu-id="ed124-1366">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="ed124-1367">**Get-AzApiManagementNetworkStatus** – Hämta nätverksstatusanslutningen för resurserna som API Management-tjänsten är beroende av.</span><span class="sxs-lookup"><span data-stu-id="ed124-1367">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="ed124-1368">Det här är användbart när du distribuerar ApiManagement-tjänsten i ett virtuellt nätverk och validerar om något beroende är brutet.</span><span class="sxs-lookup"><span data-stu-id="ed124-1368">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="ed124-1369">Uppdaterade cmdlet **New-AzApiManagement** för att hantera ApiManagement-tjänsten</span><span class="sxs-lookup"><span data-stu-id="ed124-1369">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="ed124-1370">Lade till stöd för den nya SKU:n Consumption</span><span class="sxs-lookup"><span data-stu-id="ed124-1370">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="ed124-1371">Aktiverade stöd för att slå på flaggan EnableClientCertificate för SKU:n Consumption</span><span class="sxs-lookup"><span data-stu-id="ed124-1371">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="ed124-1372">Den nya cmdleten **New-AzApiManagementSslSetting** gör det möjligt att ställa in TLS/SSL-inställningen på ”Backend” och ”Frontend” (serverdel och klientdel).</span><span class="sxs-lookup"><span data-stu-id="ed124-1372">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="ed124-1373">Det här kan också användas till att konfigurera chiffer som 3DES och ServerProtocols som Http2 för Frontend för en ApiManagement-tjänst.</span><span class="sxs-lookup"><span data-stu-id="ed124-1373">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="ed124-1374">Stöd har lagts till för att konfigurera värdnamnet DeveloperPortal på ApiManagement-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="ed124-1374">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="ed124-1375">Uppdaterade cmdletar **Get-AzApiManagementSsoToken** för att ta PsApiManagement-objekt som indata</span><span class="sxs-lookup"><span data-stu-id="ed124-1375">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="ed124-1376">Uppdaterad cmdleten för att visa infogade felmeddelanden</span><span class="sxs-lookup"><span data-stu-id="ed124-1376">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="ed124-1377">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Felkod: Felmeddelande av typen ValidationError: Ett eller flera fält innehåller felaktiga värden: Felinformation:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="ed124-1377">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="ed124-1378">Uppdaterade cmdlet **Export-AzApiManagementApi** för att exportera API:er i OpenApi 3.0-format</span><span class="sxs-lookup"><span data-stu-id="ed124-1378">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="ed124-1379">Uppdaterade cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="ed124-1379">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="ed124-1380">Importera API från dokumentspecifikationen OpenApi 3.0</span><span class="sxs-lookup"><span data-stu-id="ed124-1380">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="ed124-1381">Om du vill åsidosätta egenskapen PsApiManagementSchema specificerad i ett dokument (Swagger, Wadl, Wsdl, OpenApi).</span><span class="sxs-lookup"><span data-stu-id="ed124-1381">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="ed124-1382">Åsidosätta egenskapen ServiceUrl som specificeras i ett dokument.</span><span class="sxs-lookup"><span data-stu-id="ed124-1382">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="ed124-1383">Uppdaterade cmdlet **Get-AzApiManagementPolicy** för att returnera policy i undantaget format av typen icke-XML med rawxml</span><span class="sxs-lookup"><span data-stu-id="ed124-1383">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="ed124-1384">Uppdaterade cmdlet **Set-AzApiManagementPolicy** för att godkänna policy i undantaget format av typen icke-XML med rawxml och XML undantaget med xml</span><span class="sxs-lookup"><span data-stu-id="ed124-1384">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="ed124-1385">Uppdaterad cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="ed124-1385">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="ed124-1386">Konfigurera API med OpenId auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="ed124-1386">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="ed124-1387">Skapa ett API i ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="ed124-1387">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="ed124-1388">Klona ett API med SourceApiId och SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="ed124-1388">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="ed124-1389">Möjlighet att konfigurera SubscriptionRequired i API-omfattningen.</span><span class="sxs-lookup"><span data-stu-id="ed124-1389">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="ed124-1390">Uppdaterad cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="ed124-1390">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="ed124-1391">Konfigurera API med OpenId auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="ed124-1391">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="ed124-1392">Uppdatera ett API till ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="ed124-1392">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="ed124-1393">Möjlighet att konfigurera SubscriptionRequired i API-omfattningen.</span><span class="sxs-lookup"><span data-stu-id="ed124-1393">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="ed124-1394">Uppdaterad cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="ed124-1394">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="ed124-1395">Klona en befintlig version med hjälp av SourceApiRevision (kopiera taggar, produkter, åtgärder och principer).</span><span class="sxs-lookup"><span data-stu-id="ed124-1395">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="ed124-1396">Den nya revisionen antar ApiId från den överordnade instansen.</span><span class="sxs-lookup"><span data-stu-id="ed124-1396">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="ed124-1397">Tillhandahålla ApiRevisionDescription</span><span class="sxs-lookup"><span data-stu-id="ed124-1397">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="ed124-1398">Åsidosätta ServiceUrl vid kloning av ett API.</span><span class="sxs-lookup"><span data-stu-id="ed124-1398">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="ed124-1399">Uppdaterad cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="ed124-1399">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="ed124-1400">Konfigurera AAD eller AADB2C med en Authority</span><span class="sxs-lookup"><span data-stu-id="ed124-1400">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="ed124-1401">Konfigurera SignupPolicy, SigninPolicy, ProfileEditingPolicy och PasswordResetPolicy</span><span class="sxs-lookup"><span data-stu-id="ed124-1401">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="ed124-1402">Uppdaterad cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="ed124-1402">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="ed124-1403">Kompensera för ny SubscriptonModel med Scope och UserId</span><span class="sxs-lookup"><span data-stu-id="ed124-1403">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="ed124-1404">Kompensera för gammal prenumerationsmodell med ProductId och UserId</span><span class="sxs-lookup"><span data-stu-id="ed124-1404">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="ed124-1405">Lägg till funktion för att aktivera AllowTracing på prenumerationsnivå.</span><span class="sxs-lookup"><span data-stu-id="ed124-1405">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="ed124-1406">Uppdaterad cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="ed124-1406">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="ed124-1407">Kompensera för ny SubscriptonModel med Scope och UserId</span><span class="sxs-lookup"><span data-stu-id="ed124-1407">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="ed124-1408">Kompensera för gammal prenumerationsmodell med ProductId och UserId</span><span class="sxs-lookup"><span data-stu-id="ed124-1408">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="ed124-1409">Lägg till funktion för att aktivera AllowTracing på prenumerationsnivå.</span><span class="sxs-lookup"><span data-stu-id="ed124-1409">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="ed124-1410">Uppdaterade följande cmdletar för att acceptera ResourceId som indata</span><span class="sxs-lookup"><span data-stu-id="ed124-1410">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="ed124-1411">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ed124-1411">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="ed124-1412">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="ed124-1412">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="ed124-1413">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="ed124-1413">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="ed124-1414">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="ed124-1414">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="ed124-1415">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="ed124-1415">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="ed124-1416">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="ed124-1416">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="ed124-1417">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="ed124-1417">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="ed124-1418">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="ed124-1418">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="ed124-1419">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="ed124-1419">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="ed124-1420">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="ed124-1420">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="ed124-1421">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="ed124-1421">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="ed124-1422">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="ed124-1422">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ed124-1423">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ed124-1423">Az.Automation</span></span>
* <span data-ttu-id="ed124-1424">Uppdaterade Get-AzAutomationJobOutputRecord för att hantera postvärden av typen JSON och Text.</span><span class="sxs-lookup"><span data-stu-id="ed124-1424">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="ed124-1425">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="ed124-1425">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="ed124-1426">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="ed124-1426">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="ed124-1427">Ändrade beteende för Start-AzAutomationDscCompilationJob till att bara starta jobbet istället för att vänta på slutförandet.</span><span class="sxs-lookup"><span data-stu-id="ed124-1427">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="ed124-1428">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="ed124-1428">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="ed124-1429">Korrigering för Get-AzAutomationDscNode när using -Name returnerar alla noder.</span><span class="sxs-lookup"><span data-stu-id="ed124-1429">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="ed124-1430">Nu returnerar den endast den matchande noden.</span><span class="sxs-lookup"><span data-stu-id="ed124-1430">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ed124-1431">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ed124-1431">Az.Compute</span></span>
* <span data-ttu-id="ed124-1432">Lägg till parametrarna ProtectFromScaleIn och ProtectFromScaleSetAction i cmdleten Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="ed124-1432">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="ed124-1433">Nu är standardinställningen att vimpelparametern New-AzVM använder en tillgänglig plats om USA, östra inte stöds</span><span class="sxs-lookup"><span data-stu-id="ed124-1433">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ed124-1434">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ed124-1434">Az.DataLakeStore</span></span>
* <span data-ttu-id="ed124-1435">Uppdatera ADLS-sdk för att använda httpclient, integrera dataplanstestning med Azure-ramverk</span><span class="sxs-lookup"><span data-stu-id="ed124-1435">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ed124-1436">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ed124-1436">Az.Monitor</span></span>
* <span data-ttu-id="ed124-1437">Korrigera felaktiga parameternamn i hjälpexempel</span><span class="sxs-lookup"><span data-stu-id="ed124-1437">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ed124-1438">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ed124-1438">Az.Network</span></span>
* <span data-ttu-id="ed124-1439">Lägg till flaggan DisableBgpRoutePropagation i utdata för effektiv routningstabell</span><span class="sxs-lookup"><span data-stu-id="ed124-1439">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="ed124-1440">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="ed124-1440">Updated cmdlet:</span></span>
        - <span data-ttu-id="ed124-1441">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="ed124-1441">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="ed124-1442">Åtgärda dubbelstreck i dokumentationen New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="ed124-1442">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="ed124-1443">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ed124-1443">Az.Resources</span></span>
* <span data-ttu-id="ed124-1444">Lägg till ny cmdlet Get-AzureRmDenyAssignment för att hämta tilldelningsnekanden</span><span class="sxs-lookup"><span data-stu-id="ed124-1444">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="ed124-1445">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ed124-1445">Az.Sql</span></span>
* <span data-ttu-id="ed124-1446">Döp om Advanced Threat Protection-cmdletar för Advanced Data Security och aktivera Vulnerability Assessment som standard</span><span class="sxs-lookup"><span data-stu-id="ed124-1446">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="ed124-1447">2.0.0 – maj 2019</span><span class="sxs-lookup"><span data-stu-id="ed124-1447">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ed124-1448">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ed124-1448">Az.Accounts</span></span>
* <span data-ttu-id="ed124-1449">Uppdatera autentiseringsbiblioteket för att åtgärda ADFS-problem med autentisering av användarnamn/lösenord</span><span class="sxs-lookup"><span data-stu-id="ed124-1449">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="ed124-1450">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ed124-1450">Az.CognitiveServices</span></span>
* <span data-ttu-id="ed124-1451">Visa endast Bing-ansvarsfriskrivning för Bing-sökningstjänster.</span><span class="sxs-lookup"><span data-stu-id="ed124-1451">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="ed124-1452">Förbättra felmeddelande när det inte går att skapa konton.</span><span class="sxs-lookup"><span data-stu-id="ed124-1452">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ed124-1453">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ed124-1453">Az.Compute</span></span>
* <span data-ttu-id="ed124-1454">Funktion för närhetsplaceringsgrupper.</span><span class="sxs-lookup"><span data-stu-id="ed124-1454">Proximity placement group feature.</span></span>
    - <span data-ttu-id="ed124-1455">Följande nya cmdletar har lagts till:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="ed124-1455">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="ed124-1456">Den nya parametern ProximityPlacementGroupId har lagts till i följande cmdletar:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="ed124-1456">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="ed124-1457">Parametern StorageAccountType har lagts till i New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="ed124-1457">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="ed124-1458">TargetRegion för New-AzGalleryImageVersion kan innehålla StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="ed124-1458">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="ed124-1459">Växlingsparametern SkipShutdown har lagts till i Stop-AzVM och Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ed124-1459">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="ed124-1460">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="ed124-1460">Breaking changes</span></span>
    - <span data-ttu-id="ed124-1461">Set-AzVMBootDiagnostics har ändrats till Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="ed124-1461">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="ed124-1462">Export-AzLogAnalyticThrottledRequests har ändrats till Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="ed124-1462">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="ed124-1463">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="ed124-1463">Az.DeploymentManager</span></span>
* <span data-ttu-id="ed124-1464">De första allmänt tillgängliga versionerna av cmdletar för Distributionshanteraren i Azure</span><span class="sxs-lookup"><span data-stu-id="ed124-1464">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="ed124-1465">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="ed124-1465">Az.Dns</span></span>
* <span data-ttu-id="ed124-1466">Automatisk delegering av DNS för NameServer</span><span class="sxs-lookup"><span data-stu-id="ed124-1466">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="ed124-1467">Det överordnade zonnamnet kan användas som ytterligare valfri parameter i cmdleten för att skapa DNS-zoner.</span><span class="sxs-lookup"><span data-stu-id="ed124-1467">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="ed124-1468">Lägger till NS-poster för en nyligen skapad underordnad zon i den överordnade zonen.</span><span class="sxs-lookup"><span data-stu-id="ed124-1468">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="ed124-1469">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="ed124-1469">Az.FrontDoor</span></span>
* <span data-ttu-id="ed124-1470">De första allmänt tillgängliga versionerna av cmdletar för Azure FrontDoor</span><span class="sxs-lookup"><span data-stu-id="ed124-1470">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="ed124-1471">Byt namn på WAF-cmdletar så att de omfattar ”Waf”</span><span class="sxs-lookup"><span data-stu-id="ed124-1471">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="ed124-1472">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="ed124-1472">Az.HDInsight</span></span>
* <span data-ttu-id="ed124-1473">Två cmdletar har tagits bort:</span><span class="sxs-lookup"><span data-stu-id="ed124-1473">Removed two cmdlets:</span></span>
    - <span data-ttu-id="ed124-1474">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="ed124-1474">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="ed124-1475">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="ed124-1475">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="ed124-1476">En ny cmdlet har lagts till, Set-AzHDInsightGatewayCredential, som ersätter Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="ed124-1476">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="ed124-1477">Uppdatera cmdleten Get-AzHDInsightJobOutput för att skilja mellan läsarrollen och HDInsight-operatörsrollen:</span><span class="sxs-lookup"><span data-stu-id="ed124-1477">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="ed124-1478">Användare med läsarrollen måste uttryckligen ange parametern ”DefaultStorageAccountKey”, annars uppstår fel.</span><span class="sxs-lookup"><span data-stu-id="ed124-1478">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="ed124-1479">Användare med HDInsight-operatörsrollen påverkas inte.</span><span class="sxs-lookup"><span data-stu-id="ed124-1479">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ed124-1480">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ed124-1480">Az.Monitor</span></span>
* <span data-ttu-id="ed124-1481">Nya cmdletar för SQR API (schemalagd frågeregel)</span><span class="sxs-lookup"><span data-stu-id="ed124-1481">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="ed124-1482">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="ed124-1482">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="ed124-1483">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="ed124-1483">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="ed124-1484">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="ed124-1484">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="ed124-1485">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="ed124-1485">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="ed124-1486">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="ed124-1486">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="ed124-1487">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="ed124-1487">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="ed124-1488">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="ed124-1488">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="ed124-1489">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="ed124-1489">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="ed124-1490">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="ed124-1490">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="ed124-1491">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="ed124-1491">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="ed124-1492">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="ed124-1492">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="ed124-1493">[Mer](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information om SQR API</span><span class="sxs-lookup"><span data-stu-id="ed124-1493">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="ed124-1494">Az.Monitor.md har uppdaterats för att omfatta cmdletar för måttbaserade aviseringsregler i GenV2 (inte klassiska)</span><span class="sxs-lookup"><span data-stu-id="ed124-1494">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ed124-1495">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ed124-1495">Az.Network</span></span>
* <span data-ttu-id="ed124-1496">Lägg till stöd för NAT Gateway-resurs</span><span class="sxs-lookup"><span data-stu-id="ed124-1496">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="ed124-1497">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="ed124-1497">New cmdlets</span></span>
        - <span data-ttu-id="ed124-1498">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="ed124-1498">New-AzNatGateway</span></span>
        - <span data-ttu-id="ed124-1499">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="ed124-1499">Get-AzNatGateway</span></span>
        - <span data-ttu-id="ed124-1500">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="ed124-1500">Set-AzNatGateway</span></span>
        - <span data-ttu-id="ed124-1501">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="ed124-1501">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="ed124-1502">Uppdaterade cmdletar</span><span class="sxs-lookup"><span data-stu-id="ed124-1502">Updated cmdlets</span></span>
        - <span data-ttu-id="ed124-1503">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="ed124-1503">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="ed124-1504">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="ed124-1504">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="ed124-1505">Nedanstående kommandon för funktionen har uppdaterats: Ange/ta bort anpassade vägar på Brooklyn Gateway.</span><span class="sxs-lookup"><span data-stu-id="ed124-1505">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="ed124-1506">New-AzVirtualNetworkGateway har uppdaterats: Den valfria parametern -CustomRoute har lagts till för att ställa in adressprefix som anpassade vägar för att ange gateway.</span><span class="sxs-lookup"><span data-stu-id="ed124-1506">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="ed124-1507">Set-AzVirtualNetworkGateway har uppdaterats: Den valfria parametern -CustomRoute har lagts till för att ange adressprefix som anpassade vägar för att ange gateway.</span><span class="sxs-lookup"><span data-stu-id="ed124-1507">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="ed124-1508">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="ed124-1508">Az.PolicyInsights</span></span>
* <span data-ttu-id="ed124-1509">Stöd för att fråga efter information om principutvärdering.</span><span class="sxs-lookup"><span data-stu-id="ed124-1509">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="ed124-1510">Lägg till parametern ”-Expand” för Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="ed124-1510">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="ed124-1511">Stöd för -Expand PolicyEvaluationDetails.</span><span class="sxs-lookup"><span data-stu-id="ed124-1511">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ed124-1512">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ed124-1512">Az.RecoveryServices</span></span>
* <span data-ttu-id="ed124-1513">Stöd för att dela prenumeration mellan Azure och Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="ed124-1513">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="ed124-1514">Markering av kommande icke-bakåtkompatibla ändringar för Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="ed124-1514">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="ed124-1515">Korrigering för återställningsplan och åtgärdsplan i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="ed124-1515">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="ed124-1516">Korrigering för mappning av uppdateringsnätverk i Azure Site Recovery för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="ed124-1516">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="ed124-1517">Korrigering för instruktioner för uppdateringsskydd i Azure Site Recovery för Azure till Azure för hanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="ed124-1517">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="ed124-1518">Andra mindre korrigeringar.</span><span class="sxs-lookup"><span data-stu-id="ed124-1518">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="ed124-1519">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="ed124-1519">Az.Relay</span></span>
* <span data-ttu-id="ed124-1520">Korrigera stavfel i kundriktade meddelanden</span><span class="sxs-lookup"><span data-stu-id="ed124-1520">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="ed124-1521">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ed124-1521">Az.ServiceBus</span></span>
* <span data-ttu-id="ed124-1522">Nya cmdletar har lagts till för NetworkRuleSet för namnområden</span><span class="sxs-lookup"><span data-stu-id="ed124-1522">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ed124-1523">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ed124-1523">Az.Storage</span></span>
* <span data-ttu-id="ed124-1524">Uppgradera till lagringsklientbiblioteket 10.0.1 (namnområdet för alla objekt från detta SDK ändras från ”Microsoft.WindowsAzure.Storage. *till ”Microsoft.Azure.Storage.* ”)</span><span class="sxs-lookup"><span data-stu-id="ed124-1524">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="ed124-1525">Uppgradera till Microsoft.Azure.Management.Storage 11.0.0 för att stödja den nya API-versionen 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="ed124-1525">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="ed124-1526">Standardlagringskontot i Skapa lagringskonto ändras från ”Storage” till ”StorageV2”</span><span class="sxs-lookup"><span data-stu-id="ed124-1526">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="ed124-1527">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ed124-1527">New-AzStorageAccount</span></span>
* <span data-ttu-id="ed124-1528">Ändra lagringskontots cmdlet-utdata Sku.Name för att passa med indata-SkuName genom att lägga till ”-”. Till exempel ändras ”StandardLRS” till ”Standard_LRS”</span><span class="sxs-lookup"><span data-stu-id="ed124-1528">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="ed124-1529">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ed124-1529">New-AzStorageAccount</span></span>
    - <span data-ttu-id="ed124-1530">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ed124-1530">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="ed124-1531">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ed124-1531">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ed124-1532">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ed124-1532">Az.Websites</span></span>
* <span data-ttu-id="ed124-1533">Egenskapen ”typ” konfigureras nu för PSSite-objekt som returneras av Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ed124-1533">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="ed124-1534">Get-AzWebApp\*Metrics och Get-AzAppServicePlanMetrics markeras som inaktuella</span><span class="sxs-lookup"><span data-stu-id="ed124-1534">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="ed124-1535">1.8.0 – april 2019</span><span class="sxs-lookup"><span data-stu-id="ed124-1535">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="ed124-1536">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="ed124-1536">Highlights since the last major release</span></span>
* <span data-ttu-id="ed124-1537">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="ed124-1537">General availability of `Az` module</span></span>
* <span data-ttu-id="ed124-1538">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="ed124-1538">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="ed124-1539">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="ed124-1539">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="ed124-1540">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="ed124-1540">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="ed124-1541">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="ed124-1541">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="ed124-1542">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="ed124-1542">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="ed124-1543">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="ed124-1543">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="ed124-1544">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ed124-1544">Az.Accounts</span></span>
* <span data-ttu-id="ed124-1545">Uppdatera Uninstall-AzureRm för att ta bort moduler i Mac på ett korrekt sätt</span><span class="sxs-lookup"><span data-stu-id="ed124-1545">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="ed124-1546">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="ed124-1546">Az.Batch</span></span>
* <span data-ttu-id="ed124-1547">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="ed124-1547">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="ed124-1548">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="ed124-1548">Az.Cdn</span></span>
* <span data-ttu-id="ed124-1549">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="ed124-1549">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="ed124-1550">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ed124-1550">Az.CognitiveServices</span></span>
* <span data-ttu-id="ed124-1551">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="ed124-1551">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ed124-1552">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ed124-1552">Az.Compute</span></span>
* <span data-ttu-id="ed124-1553">Åtgärda problem med AEM-installationen om resurs-ID:n för diskar innehåller resourcegroups i gemener i resurs-ID:n</span><span class="sxs-lookup"><span data-stu-id="ed124-1553">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="ed124-1554">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="ed124-1554">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="ed124-1555">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="ed124-1555">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ed124-1556">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ed124-1556">Az.DataFactory</span></span>
* <span data-ttu-id="ed124-1557">Lägg till SsisProperties om NodeCount inte är null för hanterad integreringskörning.</span><span class="sxs-lookup"><span data-stu-id="ed124-1557">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ed124-1558">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ed124-1558">Az.DataLakeStore</span></span>
* <span data-ttu-id="ed124-1559">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="ed124-1559">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="ed124-1560">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="ed124-1560">Az.EventGrid</span></span>
* <span data-ttu-id="ed124-1561">Hjälptexten för slutpunkten har uppdaterats för att visa att resurser ska skapas innan cmdletarna för att skapa/uppdatera händelseprenumerationer används.</span><span class="sxs-lookup"><span data-stu-id="ed124-1561">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="ed124-1562">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="ed124-1562">Az.EventHub</span></span>
* <span data-ttu-id="ed124-1563">Nya cmdletar har lagts till för NetworkRuleSet för namnområden</span><span class="sxs-lookup"><span data-stu-id="ed124-1563">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="ed124-1564">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="ed124-1564">Az.HDInsight</span></span>
* <span data-ttu-id="ed124-1565">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="ed124-1565">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ed124-1566">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ed124-1566">Az.IotHub</span></span>
* <span data-ttu-id="ed124-1567">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="ed124-1567">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="ed124-1568">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ed124-1568">Az.KeyVault</span></span>
* <span data-ttu-id="ed124-1569">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="ed124-1569">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="ed124-1570">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="ed124-1570">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="ed124-1571">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="ed124-1571">Az.MachineLearning</span></span>
* <span data-ttu-id="ed124-1572">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="ed124-1572">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="ed124-1573">Az.Media</span><span class="sxs-lookup"><span data-stu-id="ed124-1573">Az.Media</span></span>
* <span data-ttu-id="ed124-1574">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="ed124-1574">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ed124-1575">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ed124-1575">Az.Monitor</span></span>
  * <span data-ttu-id="ed124-1576">Nya cmdletar för måttbaserad aviseringsregel i GenV2 (inte klassisk)</span><span class="sxs-lookup"><span data-stu-id="ed124-1576">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="ed124-1577">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="ed124-1577">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="ed124-1578">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="ed124-1578">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="ed124-1579">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="ed124-1579">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="ed124-1580">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="ed124-1580">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="ed124-1581">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="ed124-1581">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="ed124-1582">Monitor SDK har uppdaterats till version 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="ed124-1582">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ed124-1583">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ed124-1583">Az.Network</span></span>
* <span data-ttu-id="ed124-1584">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="ed124-1584">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="ed124-1585">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="ed124-1585">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="ed124-1586">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="ed124-1586">Az.NotificationHubs</span></span>
* <span data-ttu-id="ed124-1587">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="ed124-1587">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="ed124-1588">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ed124-1588">Az.OperationalInsights</span></span>
* <span data-ttu-id="ed124-1589">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="ed124-1589">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="ed124-1590">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="ed124-1590">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="ed124-1591">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="ed124-1591">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ed124-1592">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ed124-1592">Az.RecoveryServices</span></span>
* <span data-ttu-id="ed124-1593">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="ed124-1593">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="ed124-1594">Tabellformatet för SQL i virtuella Azure-datorer har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="ed124-1594">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="ed124-1595">En alternativ metod för att hämta platser i AzureFileShare har lagts till</span><span class="sxs-lookup"><span data-stu-id="ed124-1595">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="ed124-1596">ScheduleRunDays i SchedulePolicy-objekt har uppdaterats enligt tidszon</span><span class="sxs-lookup"><span data-stu-id="ed124-1596">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="ed124-1597">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="ed124-1597">Az.RedisCache</span></span>
* <span data-ttu-id="ed124-1598">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="ed124-1598">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="ed124-1599">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ed124-1599">Az.Resources</span></span>
* <span data-ttu-id="ed124-1600">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="ed124-1600">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="ed124-1601">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ed124-1601">Az.Sql</span></span>
* <span data-ttu-id="ed124-1602">Ersätt Monitor SDK-beroende med vanlig kod</span><span class="sxs-lookup"><span data-stu-id="ed124-1602">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="ed124-1603">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="ed124-1603">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="ed124-1604">Förbättrad process för klassificering av flera kolumner.</span><span class="sxs-lookup"><span data-stu-id="ed124-1604">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="ed124-1605">Inkludera SKU-egenskaper (SKU-namn, serie, kapacitet) i svaret från Get-AzSqlServerServiceObjective och formatera som tabell som standard.</span><span class="sxs-lookup"><span data-stu-id="ed124-1605">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="ed124-1606">Möjlighet att använda Get-AzSqlServerServiceObjective efter plats utan att behöva en redan befintlig server i regionen.</span><span class="sxs-lookup"><span data-stu-id="ed124-1606">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="ed124-1607">Stöd för tidszonsparametern när hanterade instanser skapas.</span><span class="sxs-lookup"><span data-stu-id="ed124-1607">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="ed124-1608">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="ed124-1608">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ed124-1609">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ed124-1609">Az.Websites</span></span>
* <span data-ttu-id="ed124-1610">åtgärdar Set-AzWebApp och Set-AzWebAppSlot så att de inte tar bort taggar vid körning</span><span class="sxs-lookup"><span data-stu-id="ed124-1610">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="ed124-1611">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="ed124-1611">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="ed124-1612">SDK för WebSites har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="ed124-1612">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="ed124-1613">Egenskapen AdminSiteName har tagits bort från PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="ed124-1613">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="ed124-1614">1.7.0 – april 2019</span><span class="sxs-lookup"><span data-stu-id="ed124-1614">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="ed124-1615">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="ed124-1615">Highlights since the last major release</span></span>
* <span data-ttu-id="ed124-1616">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="ed124-1616">General availability of `Az` module</span></span>
* <span data-ttu-id="ed124-1617">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="ed124-1617">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="ed124-1618">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="ed124-1618">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="ed124-1619">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="ed124-1619">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="ed124-1620">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="ed124-1620">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="ed124-1621">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="ed124-1621">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="ed124-1622">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="ed124-1622">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="ed124-1623">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ed124-1623">Az.Accounts</span></span>
* <span data-ttu-id="ed124-1624">Add-AzEnvironment och Set-AzEnvironment har uppdaterats för att godkänna parametern AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="ed124-1624">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="ed124-1625">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ed124-1625">Az.AnalysisServices</span></span>
* <span data-ttu-id="ed124-1626">ServiceClient används i cmdletar för dataplan och den ursprungliga autentiseringslogiken har tagits bort</span><span class="sxs-lookup"><span data-stu-id="ed124-1626">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="ed124-1627">Add-AzureASAccount används för omslutning av Connect-AzAccount för att undvika en icke-bakåtkompatibel ändring</span><span class="sxs-lookup"><span data-stu-id="ed124-1627">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ed124-1628">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ed124-1628">Az.Automation</span></span>
* <span data-ttu-id="ed124-1629">Buggen för cmdleten New-AzAutomationSoftwareUpdateConfiguration för inkluderingar har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="ed124-1629">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="ed124-1630">Nu bör parametern IncludedKbNumber och IncludedPackageNameMask fungera.</span><span class="sxs-lookup"><span data-stu-id="ed124-1630">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="ed124-1631">Felkorrigering för dynamiska grupper i uppdateringshanteringen för azure automation</span><span class="sxs-lookup"><span data-stu-id="ed124-1631">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ed124-1632">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ed124-1632">Az.Compute</span></span>
* <span data-ttu-id="ed124-1633">Lägg till parametern HyperVGeneration i New-AzDiskConfig och New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="ed124-1633">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="ed124-1634">Tillåt att virtuella datorer skapas med galleribilder från andra klientorganisationer.</span><span class="sxs-lookup"><span data-stu-id="ed124-1634">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="ed124-1635">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="ed124-1635">Az.ContainerInstance</span></span>
* <span data-ttu-id="ed124-1636">Ett problem har åtgärdats i parametern -Command för New-AzContainerGroup som lade till ett avslutande tomt argument</span><span class="sxs-lookup"><span data-stu-id="ed124-1636">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ed124-1637">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ed124-1637">Az.DataFactory</span></span>
* <span data-ttu-id="ed124-1638">ADF .Net SDK-versionen har uppdaterats till 3.0.2</span><span class="sxs-lookup"><span data-stu-id="ed124-1638">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="ed124-1639">Cmdleten Set-AzDataFactoryV2 har uppdaterats med extra parametrar för inställningar som rör RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="ed124-1639">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="ed124-1640">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ed124-1640">Az.Resources</span></span>
* <span data-ttu-id="ed124-1641">Förbättra hanteringen av providrar för Get-AzResource när parametrarna -ResourceId eller -ResourceGroupName, -Name och -ResourceType tillhandahålls</span><span class="sxs-lookup"><span data-stu-id="ed124-1641">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="ed124-1642">Förbättra felhanteringen för ”Test-AzDeployment” och ”Test-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="ed124-1642">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="ed124-1643">Hantera fel utanför distributionsvalideringen och ta med dem i kommandoutdata istället</span><span class="sxs-lookup"><span data-stu-id="ed124-1643">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="ed124-1644">Mer information här: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="ed124-1644">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="ed124-1645">Lägg till växlingsparametern -IgnoreDynamicParameters till en uppsättning av cmdletar för distribution för att hoppa över fråga i skript och jobbscenarier</span><span class="sxs-lookup"><span data-stu-id="ed124-1645">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="ed124-1646">Mer information här: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="ed124-1646">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="ed124-1647">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ed124-1647">Az.Sql</span></span>
* <span data-ttu-id="ed124-1648">Stöd för dataklassificering av databaser.</span><span class="sxs-lookup"><span data-stu-id="ed124-1648">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ed124-1649">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ed124-1649">Az.Storage</span></span>
* <span data-ttu-id="ed124-1650">Rapportera detaljfel när lagringskontext skapas med parametern -UseConnectedAccount, men utan inloggning på Azure-kontot</span><span class="sxs-lookup"><span data-stu-id="ed124-1650">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="ed124-1651">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="ed124-1651">New-AzStorageContext</span></span>
* <span data-ttu-id="ed124-1652">Stöd för att hantera Blob Service-egenskaper för ett angivet lagringskonto med API:et för hanteringsplan</span><span class="sxs-lookup"><span data-stu-id="ed124-1652">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="ed124-1653">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="ed124-1653">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="ed124-1654">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="ed124-1654">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="ed124-1655">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="ed124-1655">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="ed124-1656">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="ed124-1656">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="ed124-1657">Stöd för -AsJob-cmdletar för att ladda upp och ladda ned blobar och filer</span><span class="sxs-lookup"><span data-stu-id="ed124-1657">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="ed124-1658">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="ed124-1658">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="ed124-1659">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="ed124-1659">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="ed124-1660">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="ed124-1660">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="ed124-1661">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="ed124-1661">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="ed124-1662">1.6.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="ed124-1662">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="ed124-1663">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="ed124-1663">Highlights since the last major release</span></span>
* <span data-ttu-id="ed124-1664">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="ed124-1664">General availability of `Az` module</span></span>
* <span data-ttu-id="ed124-1665">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="ed124-1665">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="ed124-1666">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="ed124-1666">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="ed124-1667">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="ed124-1667">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="ed124-1668">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="ed124-1668">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="ed124-1669">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="ed124-1669">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="ed124-1670">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="ed124-1670">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ed124-1671">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ed124-1671">Az.Automation</span></span>
* <span data-ttu-id="ed124-1672">Azure Automation – ändring av uppdateringshantering för stöd för de nya funktionerna:</span><span class="sxs-lookup"><span data-stu-id="ed124-1672">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="ed124-1673">Dynamisk gruppering</span><span class="sxs-lookup"><span data-stu-id="ed124-1673">Dynamic grouping</span></span>
    * <span data-ttu-id="ed124-1674">För-/efterskrift</span><span class="sxs-lookup"><span data-stu-id="ed124-1674">Pre-Post script</span></span>
    * <span data-ttu-id="ed124-1675">Inställning för omstart</span><span class="sxs-lookup"><span data-stu-id="ed124-1675">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ed124-1676">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ed124-1676">Az.Compute</span></span>
* <span data-ttu-id="ed124-1677">Åtgärda problem med sökvägsmatchning i Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="ed124-1677">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="ed124-1678">Uppdatera Compute-klientbibliotek till 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="ed124-1678">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="ed124-1679">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ed124-1679">Az.KeyVault</span></span>
* <span data-ttu-id="ed124-1680">Stöd för jokertecken för KeyVault-cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="ed124-1680">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ed124-1681">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ed124-1681">Az.Network</span></span>
* <span data-ttu-id="ed124-1682">Lägg till stöd för Threat Intelligence för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="ed124-1682">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="ed124-1683">Lägg till resurs för brandväggsprincip på översta nivå och anpassade regler för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="ed124-1683">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ed124-1684">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ed124-1684">Az.RecoveryServices</span></span>
* <span data-ttu-id="ed124-1685">SnapshotRetentionInDays har lagts till i Azure-principen för virtuella datorer för stöd av Instant RP</span><span class="sxs-lookup"><span data-stu-id="ed124-1685">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="ed124-1686">Pipe-stöd för avregistrering av container har lagts till</span><span class="sxs-lookup"><span data-stu-id="ed124-1686">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="ed124-1687">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ed124-1687">Az.Resources</span></span>
* <span data-ttu-id="ed124-1688">Uppdatera stöd för jokertecken för Get-AzResource och Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ed124-1688">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="ed124-1689">Uppdatera autentiseringsuppgifter som används vid allmänna anrop till ARM</span><span class="sxs-lookup"><span data-stu-id="ed124-1689">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="ed124-1690">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ed124-1690">Az.Sql</span></span>
* <span data-ttu-id="ed124-1691">Cmdlet-parametern (ExcludeDetectionType) för Hotidentifiering ändrades från DetectionType till sträng[] för att framtidssäkra den när nya DetectionTypes läggs till, och även för att stödja automatisk ifyllning.</span><span class="sxs-lookup"><span data-stu-id="ed124-1691">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ed124-1692">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ed124-1692">Az.Storage</span></span>
* <span data-ttu-id="ed124-1693">Stöd för att hämta/ange/ta bort hanteringsprincip på ett lagringskonto</span><span class="sxs-lookup"><span data-stu-id="ed124-1693">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="ed124-1694">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="ed124-1694">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="ed124-1695">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="ed124-1695">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="ed124-1696">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="ed124-1696">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="ed124-1697">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="ed124-1697">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="ed124-1698">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="ed124-1698">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="ed124-1699">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="ed124-1699">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ed124-1700">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ed124-1700">Az.Websites</span></span>
* <span data-ttu-id="ed124-1701">Åtgärda fel med ARM-mall som avbryter kloning av alla platser med 'New-AzWebApp -IncludeSourceWebAppSlots'</span><span class="sxs-lookup"><span data-stu-id="ed124-1701">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="ed124-1702">1.5.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="ed124-1702">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ed124-1703">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ed124-1703">Az.Accounts</span></span>
* <span data-ttu-id="ed124-1704">Lägg till kommandot Register-AzModule för stöd för AutoRest-genererade cmdletar</span><span class="sxs-lookup"><span data-stu-id="ed124-1704">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="ed124-1705">Uppdatera exempel för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="ed124-1705">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ed124-1706">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ed124-1706">Az.Automation</span></span>
* <span data-ttu-id="ed124-1707">Problem med att hämta vissa månadsscheman i flera Azure Automation-cmdletar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="ed124-1707">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="ed124-1708">Åtgärda problem med att Get-AzAutomationDscNode bara returnerar de 20 översta noderna.</span><span class="sxs-lookup"><span data-stu-id="ed124-1708">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="ed124-1709">Nu returneras alla noder</span><span class="sxs-lookup"><span data-stu-id="ed124-1709">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="ed124-1710">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="ed124-1710">Az.Cdn</span></span>
* <span data-ttu-id="ed124-1711">Nya Powershell-cmdletar för att aktivera/inaktivera anpassade domän-HTTPS har lagts till och de gamla har gjorts inaktuella</span><span class="sxs-lookup"><span data-stu-id="ed124-1711">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ed124-1712">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ed124-1712">Az.Compute</span></span>
* <span data-ttu-id="ed124-1713">Lägg till stöd för jokertecken för Get-cmdletar</span><span class="sxs-lookup"><span data-stu-id="ed124-1713">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ed124-1714">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ed124-1714">Az.DataFactory</span></span>
* <span data-ttu-id="ed124-1715">ADF .Net SDK-versionen har uppdaterats till 3.0.1</span><span class="sxs-lookup"><span data-stu-id="ed124-1715">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="ed124-1716">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="ed124-1716">Az.LogicApp</span></span>
* <span data-ttu-id="ed124-1717">Åtgärda problemet med att ListWorkflows endast hämtar den första sidan med resultat</span><span class="sxs-lookup"><span data-stu-id="ed124-1717">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ed124-1718">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ed124-1718">Az.Network</span></span>
* <span data-ttu-id="ed124-1719">Lägg till stöd för jokertecken för Network-cmdletar</span><span class="sxs-lookup"><span data-stu-id="ed124-1719">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ed124-1720">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ed124-1720">Az.RecoveryServices</span></span>
* <span data-ttu-id="ed124-1721">Stöd har lagts till för SQL Server i virtuella Azure-datorer</span><span class="sxs-lookup"><span data-stu-id="ed124-1721">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="ed124-1722">SDK-uppdatering</span><span class="sxs-lookup"><span data-stu-id="ed124-1722">SDK Update</span></span>
* <span data-ttu-id="ed124-1723">Get-ProtectableItem-incheckning i VMappContainer har tagits bort</span><span class="sxs-lookup"><span data-stu-id="ed124-1723">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="ed124-1724">Name och ServerName har lagts till som parametrar för Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="ed124-1724">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="ed124-1725">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ed124-1725">Az.Resources</span></span>
* <span data-ttu-id="ed124-1726">Lägg till parametern `-TemplateObject` i cmdletar för distribution</span><span class="sxs-lookup"><span data-stu-id="ed124-1726">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="ed124-1727">Mer information här: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="ed124-1727">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="ed124-1728">Åtgärda problem med piping av resultatet i `Get-AzResource` till `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="ed124-1728">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="ed124-1729">Mer information här: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="ed124-1729">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="ed124-1730">Åtgärda problem med ändring av JSON-datatyp när `Set-AzResource` körs</span><span class="sxs-lookup"><span data-stu-id="ed124-1730">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="ed124-1731">Mer information här: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="ed124-1731">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="ed124-1732">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ed124-1732">Az.Sql</span></span>
* <span data-ttu-id="ed124-1733">AuditingEndpointsCommunicator uppdateras.</span><span class="sxs-lookup"><span data-stu-id="ed124-1733">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="ed124-1734">Åtgärdar beteendet hos ett gränsscenario när nya diagnostikinställningar skapas.</span><span class="sxs-lookup"><span data-stu-id="ed124-1734">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ed124-1735">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ed124-1735">Az.Storage</span></span>
* <span data-ttu-id="ed124-1736">Stöd för BlockBlobStorage när Storage-konto skapas      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ed124-1736">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="ed124-1737">1.4.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="ed124-1737">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="ed124-1738">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ed124-1738">Az.AnalysisServices</span></span>
* <span data-ttu-id="ed124-1739">Inaktuell AddAzureASAccount-cmdlet</span><span class="sxs-lookup"><span data-stu-id="ed124-1739">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ed124-1740">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ed124-1740">Az.Automation</span></span>
* <span data-ttu-id="ed124-1741">Hjälpen för Import-AzAutomationDscNodeConfiguration har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="ed124-1741">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="ed124-1742">Konfigurationsnamnsvalidering har lagts till i cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="ed124-1742">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="ed124-1743">Förbättrad felhantering för cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="ed124-1743">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="ed124-1744">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ed124-1744">Az.CognitiveServices</span></span>
* <span data-ttu-id="ed124-1745">CustomSubdomainName har lagts till som en ny valfri parameter för New-AzCognitiveServicesAccount, som används för att ange underdomän för resursen.</span><span class="sxs-lookup"><span data-stu-id="ed124-1745">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ed124-1746">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ed124-1746">Az.Compute</span></span>
* <span data-ttu-id="ed124-1747">Problemet med ID-parameteruppsättningar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="ed124-1747">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="ed124-1748">Get-AzVMExtension har uppdaterats så att alla installerade tillägg visas om parametern Name inte har angetts</span><span class="sxs-lookup"><span data-stu-id="ed124-1748">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="ed124-1749">Parametrarna Tag och ResourceId har lagts till i cmdleten Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="ed124-1749">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="ed124-1750">Get-AzVmssVM utan instans-ID och med InstanceView kan visa virtuella VMSS-datorer med instansvyn.</span><span class="sxs-lookup"><span data-stu-id="ed124-1750">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ed124-1751">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ed124-1751">Az.DataLakeStore</span></span>
* <span data-ttu-id="ed124-1752">Cmdletar har lagts till för uppräkning och återställning av borttagna objekt i ADL</span><span class="sxs-lookup"><span data-stu-id="ed124-1752">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="ed124-1753">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="ed124-1753">Az.EventHub</span></span>
* <span data-ttu-id="ed124-1754">Ny boolesk egenskap SkipEmptyArchives har lagts till i Skip Empty Archives i CaptureDescription-klassen i Eventhub</span><span class="sxs-lookup"><span data-stu-id="ed124-1754">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="ed124-1755">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ed124-1755">Az.KeyVault</span></span>
* <span data-ttu-id="ed124-1756">Taggning i Set-AzKeyVaultSecret har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="ed124-1756">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="ed124-1757">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="ed124-1757">Az.LogicApp</span></span>
* <span data-ttu-id="ed124-1758">Grundläggande SKU har lagts till för Integrationskonton</span><span class="sxs-lookup"><span data-stu-id="ed124-1758">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="ed124-1759">XSLT 2.0, XSLT 3.0 och Flytande mappningstyper har lagts till</span><span class="sxs-lookup"><span data-stu-id="ed124-1759">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="ed124-1760">Nya cmdletar för integrationskontosammansättningar</span><span class="sxs-lookup"><span data-stu-id="ed124-1760">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="ed124-1761">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="ed124-1761">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="ed124-1762">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="ed124-1762">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="ed124-1763">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="ed124-1763">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="ed124-1764">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="ed124-1764">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="ed124-1765">Nya cmdletar för batchkonfiguration för integrationskonto</span><span class="sxs-lookup"><span data-stu-id="ed124-1765">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="ed124-1766">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="ed124-1766">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="ed124-1767">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="ed124-1767">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="ed124-1768">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="ed124-1768">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="ed124-1769">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="ed124-1769">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="ed124-1770">Logic App-SDK har uppdaterats till version 4.1.0</span><span class="sxs-lookup"><span data-stu-id="ed124-1770">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ed124-1771">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ed124-1771">Az.Monitor</span></span>
* <span data-ttu-id="ed124-1772">Hjälpen för Get-AzMetric har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="ed124-1772">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ed124-1773">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ed124-1773">Az.Network</span></span>
* <span data-ttu-id="ed124-1774">Hjälpexempel för Add-AzApplicationGatewayCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="ed124-1774">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="ed124-1775">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ed124-1775">Az.OperationalInsights</span></span>
* <span data-ttu-id="ed124-1776">Ytterligare stöd för datakällorna New och Get ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="ed124-1776">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="ed124-1777">Ny ApplicationInsights-typ har lagts till för att ge stöd för ”Get specific” och ”Get all” för ApplicationInsights-datakällor för angiven arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="ed124-1777">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="ed124-1778">Cmdleten New-AzOperationalInsightsApplicationInsightsDataSource har lagts till för att skapa datakälla med angivna parametrar för Application Insights-resurs: subscription Id, resourceGroupName och name.</span><span class="sxs-lookup"><span data-stu-id="ed124-1778">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="ed124-1779">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ed124-1779">Az.Resources</span></span>
* <span data-ttu-id="ed124-1780">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="ed124-1780">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="ed124-1781">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="ed124-1781">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="ed124-1782">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="ed124-1782">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="ed124-1783">Fel som gör att KeyCredentials inte kan skapas upprepade gånger har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="ed124-1783">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="ed124-1784">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ed124-1784">Az.Sql</span></span>
* <span data-ttu-id="ed124-1785">Lägg till stöd för hyperskalanivån för SQL DB</span><span class="sxs-lookup"><span data-stu-id="ed124-1785">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="ed124-1786">Ett fel har åtgärdats där återställningen kunde misslyckas på grund av onödiga inställningsegenskaper i restore-förfrågan</span><span class="sxs-lookup"><span data-stu-id="ed124-1786">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ed124-1787">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ed124-1787">Az.Websites</span></span>
* <span data-ttu-id="ed124-1788">Rätt exempel i Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="ed124-1788">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="ed124-1789">1.3.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="ed124-1789">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ed124-1790">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ed124-1790">Az.Accounts</span></span>
* <span data-ttu-id="ed124-1791">Uppdatera till den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="ed124-1791">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="ed124-1792">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ed124-1792">Az.AnalysisServices</span></span>
<span data-ttu-id="ed124-1793">Allmän tillgänglighet för Az.AnalysisServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="ed124-1793">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ed124-1794">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ed124-1794">Az.Compute</span></span>
* <span data-ttu-id="ed124-1795">AEM-tillägg: Lägg till stöd för UltraSSD-, P60-, P70- och P80-diskar</span><span class="sxs-lookup"><span data-stu-id="ed124-1795">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="ed124-1796">Uppdatera hjälpbeskrivning för Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="ed124-1796">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="ed124-1797">Uppdatera hjälpbeskrivning och exempel för Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="ed124-1797">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ed124-1798">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ed124-1798">Az.RecoveryServices</span></span>
<span data-ttu-id="ed124-1799">Allmän tillgänglighet för Az.RecoveryServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="ed124-1799">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="ed124-1800">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ed124-1800">Az.Resources</span></span>
* <span data-ttu-id="ed124-1801">Korrigera taggar för resursgrupper</span><span class="sxs-lookup"><span data-stu-id="ed124-1801">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="ed124-1802">Mer information här: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="ed124-1802">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="ed124-1803">Åtgärda problem där `Get-AzureRmRoleAssignment` inte respekterar -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="ed124-1803">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="ed124-1804">Mer information här: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="ed124-1804">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="ed124-1805">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ed124-1805">Az.Sql</span></span>
* <span data-ttu-id="ed124-1806">Lägga till Get/Set-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="ed124-1806">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="ed124-1807">Åtgärda problem där ett nullref-undantag uppstår när du kör SQL-cmdletar och inte är inloggad på ett Azure-konto</span><span class="sxs-lookup"><span data-stu-id="ed124-1807">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="ed124-1808">Åtgärda nullref-undantag i Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="ed124-1808">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="ed124-1809">1.2.1 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="ed124-1809">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ed124-1810">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ed124-1810">Az.Accounts</span></span>
* <span data-ttu-id="ed124-1811">Version med rätt version av autentisering</span><span class="sxs-lookup"><span data-stu-id="ed124-1811">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="ed124-1812">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ed124-1812">Az.AnalysisServices</span></span>
* <span data-ttu-id="ed124-1813">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="ed124-1813">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ed124-1814">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ed124-1814">Az.RecoveryServices</span></span>
* <span data-ttu-id="ed124-1815">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="ed124-1815">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="ed124-1816">1.2.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="ed124-1816">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ed124-1817">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ed124-1817">Az.Accounts</span></span>
* <span data-ttu-id="ed124-1818">Lägga till interaktiv autentisering och autentisering med användarnamn/lösenord för endast Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="ed124-1818">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="ed124-1819">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="ed124-1819">Update incorrect online help URLs</span></span>
* <span data-ttu-id="ed124-1820">Lägga till varningsmeddelande i PS Core för Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="ed124-1820">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="ed124-1821">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="ed124-1821">Az.Aks</span></span>
* <span data-ttu-id="ed124-1822">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="ed124-1822">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ed124-1823">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ed124-1823">Az.Automation</span></span>
* <span data-ttu-id="ed124-1824">Stöd för Python 2-runbookflöden har lagts till</span><span class="sxs-lookup"><span data-stu-id="ed124-1824">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="ed124-1825">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="ed124-1825">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="ed124-1826">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="ed124-1826">Az.Cdn</span></span>
* <span data-ttu-id="ed124-1827">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="ed124-1827">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ed124-1828">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ed124-1828">Az.Compute</span></span>
* <span data-ttu-id="ed124-1829">Lägga till cmdleten Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="ed124-1829">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="ed124-1830">Lägga till TempDisk-parameter i Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ed124-1830">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="ed124-1831">Korrigera varningsmeddelande för New-AzVM</span><span class="sxs-lookup"><span data-stu-id="ed124-1831">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="ed124-1832">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ed124-1832">Az.ContainerRegistry</span></span>
* <span data-ttu-id="ed124-1833">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="ed124-1833">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ed124-1834">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ed124-1834">Az.DataFactory</span></span>
* <span data-ttu-id="ed124-1835">ADF .Net SDK-versionen har uppdaterats till 3.0.0</span><span class="sxs-lookup"><span data-stu-id="ed124-1835">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ed124-1836">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ed124-1836">Az.DataLakeStore</span></span>
* <span data-ttu-id="ed124-1837">Åtgärda problem med ADLS-slutpunkt vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="ed124-1837">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="ed124-1838">Mer information här: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="ed124-1838">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="ed124-1839">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="ed124-1839">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ed124-1840">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ed124-1840">Az.IotHub</span></span>
* <span data-ttu-id="ed124-1841">Lägga till kodningsformat i cmdleten Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="ed124-1841">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="ed124-1842">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ed124-1842">Az.KeyVault</span></span>
* <span data-ttu-id="ed124-1843">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="ed124-1843">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ed124-1844">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ed124-1844">Az.Network</span></span>
* <span data-ttu-id="ed124-1845">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="ed124-1845">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="ed124-1846">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ed124-1846">Az.Resources</span></span>
* <span data-ttu-id="ed124-1847">Åtgärda felaktiga exempel i referensdokumentationen ”New-AzADAppCredential” och ”New-AzADSpCredential”</span><span class="sxs-lookup"><span data-stu-id="ed124-1847">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="ed124-1848">Åtgärda problem där sökvägen för parametern ”-TemplateFile” inte omvandlas innan cmdletarna för distribution i resursgruppen körs</span><span class="sxs-lookup"><span data-stu-id="ed124-1848">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="ed124-1849">Az.Resources: Korrigera dokumentationen om standardvärdet för New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="ed124-1849">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="ed124-1850">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="ed124-1850">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="ed124-1851">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="ed124-1851">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="ed124-1852">Åtgärda formateringsproblemet med objektet ”PSResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="ed124-1852">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="ed124-1853">Mer information här: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="ed124-1853">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="ed124-1854">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ed124-1854">Az.ServiceFabric</span></span>
* <span data-ttu-id="ed124-1855">Återställ när ett certifikat läggs till i en Virtual Machine Scale Sets-modell men ett undantag genereras. Detta har gjorts för att åtgärda följande fel: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="ed124-1855">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="ed124-1856">Korrigera några felmeddelanden.</span><span class="sxs-lookup"><span data-stu-id="ed124-1856">Fix some error messages.</span></span>
* <span data-ttu-id="ed124-1857">Korrigering av skapande av kluster med ARM-mall som är standard för New-AzServiceFabriCluster som inte fungerade med migrering till Az.</span><span class="sxs-lookup"><span data-stu-id="ed124-1857">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="ed124-1858">Korrigering av tilläggning av kluster/programcertifikat så att endast VM Scale Sets som motsvarar klustret läggs till genom att kontrollera ID för klustret i tillägget.</span><span class="sxs-lookup"><span data-stu-id="ed124-1858">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="ed124-1859">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="ed124-1859">Az.SignalR</span></span>
* <span data-ttu-id="ed124-1860">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="ed124-1860">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="ed124-1861">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ed124-1861">Az.Sql</span></span>
* <span data-ttu-id="ed124-1862">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="ed124-1862">Update incorrect online help URLs</span></span>
* <span data-ttu-id="ed124-1863">Uppdaterad parameterbeskrivning för LicenseType-parameter med möjliga värden</span><span class="sxs-lookup"><span data-stu-id="ed124-1863">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="ed124-1864">Korrigering för att uppdatera hanterad instansidentitet som inte fungerar när det är den enda uppdaterade egenskapen</span><span class="sxs-lookup"><span data-stu-id="ed124-1864">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="ed124-1865">Stöd för anpassad sortering på hanterad instans</span><span class="sxs-lookup"><span data-stu-id="ed124-1865">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ed124-1866">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ed124-1866">Az.Storage</span></span>
* <span data-ttu-id="ed124-1867">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="ed124-1867">Update incorrect online help URLs</span></span>
* <span data-ttu-id="ed124-1868">Tillhandahåll detaljerat felmeddelande när en användare försöker hämta/konfigurera klassisk loggning/mått på ett Premium Storage-konto eftersom Premium Storage-kontot inte har stöd för klassisk loggning/mått.</span><span class="sxs-lookup"><span data-stu-id="ed124-1868">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="ed124-1869">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="ed124-1869">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="ed124-1870">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="ed124-1870">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="ed124-1871">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="ed124-1871">Az.TrafficManager</span></span>
* <span data-ttu-id="ed124-1872">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="ed124-1872">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ed124-1873">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ed124-1873">Az.Websites</span></span>
* <span data-ttu-id="ed124-1874">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="ed124-1874">Update incorrect online help URLs</span></span>
* <span data-ttu-id="ed124-1875">Korrigerar ”New-AzWebAppSSLBinding” så att certifikatet laddas upp till rätt resursgrupp och plats om appen finns i en ASE.</span><span class="sxs-lookup"><span data-stu-id="ed124-1875">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="ed124-1876">Korrigerar ”New-AzWebAppSSLBinding” så att taggarna inte skrivs över på en bindning av ett SSL-certifikat till en app</span><span class="sxs-lookup"><span data-stu-id="ed124-1876">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="ed124-1877">1.1.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="ed124-1877">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ed124-1878">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ed124-1878">Az.Accounts</span></span>
* <span data-ttu-id="ed124-1879">Lade till omfattningen ”Lokal” till Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="ed124-1879">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ed124-1880">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ed124-1880">Az.Compute</span></span>
* <span data-ttu-id="ed124-1881">Namn är nu valfritt i ID-parametern för Restart/Start/Stop/Remove/Set-AzVM och Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="ed124-1881">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="ed124-1882">Uppdaterade beskrivningen av ID i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="ed124-1882">Updated the description of ID in help files</span></span>
* <span data-ttu-id="ed124-1883">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ed124-1883">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ed124-1884">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ed124-1884">Az.DataLakeStore</span></span>
* <span data-ttu-id="ed124-1885">Uppdatera sdk-versionen av dataplanet till 1.1.14 för SDK-korrigeringar.</span><span class="sxs-lookup"><span data-stu-id="ed124-1885">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="ed124-1886">Korrigerade hanteringen av negativ accesstime och modificationtime för getfilestatus och liststatus; korrigera asynkront annulleringstoken</span><span class="sxs-lookup"><span data-stu-id="ed124-1886">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="ed124-1887">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="ed124-1887">Az.EventGrid</span></span>
* <span data-ttu-id="ed124-1888">Uppdaterat för användning av API-versionen 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="ed124-1888">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="ed124-1889">Uppdaterade följande cmdletar för att stödja nytt scenario i API-versionen 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="ed124-1889">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="ed124-1890">New-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="ed124-1890">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="ed124-1891">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="ed124-1891">Event Time-To-Live,</span></span>
        - <span data-ttu-id="ed124-1892">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="ed124-1892">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="ed124-1893">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="ed124-1893">Dead letter endpoint.</span></span>
    - <span data-ttu-id="ed124-1894">Update-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="ed124-1894">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="ed124-1895">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="ed124-1895">Event Time-To-Live,</span></span>
        - <span data-ttu-id="ed124-1896">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="ed124-1896">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="ed124-1897">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="ed124-1897">Dead letter endpoint.</span></span>
* <span data-ttu-id="ed124-1898">Lade till nya enum-värden (storageQueue och hybridConnection) för alternativet EndpointType i cmdletarna New-AzureRmEventGridSubscription och Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="ed124-1898">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="ed124-1899">Visa varningsmeddelanden om skapande eller uppdatering av händelseprenumerationen förväntas medföra manuell åtgärd från användaren.</span><span class="sxs-lookup"><span data-stu-id="ed124-1899">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ed124-1900">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ed124-1900">Az.IotHub</span></span>
* <span data-ttu-id="ed124-1901">Har uppdaterats till den senaste versionen av SDK:n lotHub</span><span class="sxs-lookup"><span data-stu-id="ed124-1901">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="ed124-1902">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="ed124-1902">Az.LogicApp</span></span>
* <span data-ttu-id="ed124-1903">Get-AzLogicApp visar en lista över alla som inte har angivet namn</span><span class="sxs-lookup"><span data-stu-id="ed124-1903">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="ed124-1904">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ed124-1904">Az.Resources</span></span>
* <span data-ttu-id="ed124-1905">Åtgärdade problem med parameteruppsättningen när parametrarna -ODataQuery och -ResourceId anges för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="ed124-1905">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="ed124-1906">Mer information här: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="ed124-1906">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="ed124-1907">Åtgärdade hantering av parametern -Custom i New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ed124-1907">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="ed124-1908">Korrigerade stavfel i New-AzDeployment-dokumentationen</span><span class="sxs-lookup"><span data-stu-id="ed124-1908">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="ed124-1909">Gjorde parametern -MailNickname obligatorisk för New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="ed124-1909">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="ed124-1910">Mer information här: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="ed124-1910">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="ed124-1911">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="ed124-1911">Az.SignalR</span></span>
* <span data-ttu-id="ed124-1912">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ed124-1912">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="ed124-1913">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ed124-1913">Az.Sql</span></span>
* <span data-ttu-id="ed124-1914">Konverterade lagringshanteringsklientens beroende av den normala SDK-implementeringen.</span><span class="sxs-lookup"><span data-stu-id="ed124-1914">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ed124-1915">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ed124-1915">Az.Storage</span></span>
* <span data-ttu-id="ed124-1916">Angav StorageAccountName för lagringskontext som det verkliga namnet på lagringskontot när det skapas med Sas Token, OAuth eller Anonymous</span><span class="sxs-lookup"><span data-stu-id="ed124-1916">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="ed124-1917">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="ed124-1917">New-AzStorageContext</span></span>
* <span data-ttu-id="ed124-1918">Skapade Sas Token för Blob Snapshot-objekt med parametern -FullUri, åtgärdade den returnerade URI:n så att den blir URI för ögonblicksbild</span><span class="sxs-lookup"><span data-stu-id="ed124-1918">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="ed124-1919">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="ed124-1919">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ed124-1920">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ed124-1920">Az.Websites</span></span>
* <span data-ttu-id="ed124-1921">Åtgärdade en bugg i datumparsningen i Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="ed124-1921">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="ed124-1922">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ed124-1922">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="ed124-1923">1.0.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="ed124-1923">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="ed124-1924">Allmänt</span><span class="sxs-lookup"><span data-stu-id="ed124-1924">General</span></span>

- <span data-ttu-id="ed124-1925">Allmän tillgänglighet för Az-modulen</span><span class="sxs-lookup"><span data-stu-id="ed124-1925">General Availability of Az Module</span></span>
- <span data-ttu-id="ed124-1926">Onlinehjälp för varje modul</span><span class="sxs-lookup"><span data-stu-id="ed124-1926">Online help for each module</span></span>
- <span data-ttu-id="ed124-1927">Mer information och en översikt finns på [Az-informationssidan](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="ed124-1927">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="ed124-1928">Information om hur du migrerar från AzureRM finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ed124-1928">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="ed124-1929">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ed124-1929">Az.Accounts</span></span>
- <span data-ttu-id="ed124-1930">Har ändrats från Az.Profile</span><span class="sxs-lookup"><span data-stu-id="ed124-1930">Changed from Az.Profile</span></span>
- <span data-ttu-id="ed124-1931">Fasta tabellformat för profil- och kontexttyper</span><span class="sxs-lookup"><span data-stu-id="ed124-1931">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="ed124-1932">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ed124-1932">Az.ApiManagement</span></span>
- <span data-ttu-id="ed124-1933">Korrigeringar för #7002</span><span class="sxs-lookup"><span data-stu-id="ed124-1933">Fixes for #7002</span></span>
- <span data-ttu-id="ed124-1934">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ed124-1934">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="ed124-1935">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="ed124-1935">Az.Batch</span></span>
- <span data-ttu-id="ed124-1936">Lade till möjligheten att se vilken version av Azure Batch Node Agent som körs på var och en av de virtuella datorerna i en pool, via den nya egenskapen `NodeAgentInformation` på `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="ed124-1936">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="ed124-1937">Standarden `Caching` för `PSDataDisk` är nu `ReadWrite` i stället för `None`.</span><span class="sxs-lookup"><span data-stu-id="ed124-1937">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="ed124-1938">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ed124-1938">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="ed124-1939">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="ed124-1939">Az.Billing</span></span>
- <span data-ttu-id="ed124-1940">Kombinerar cmdletarna för fakturering, förbrukning och UsageAggregates. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ed124-1940">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="ed124-1941">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="ed124-1941">Az.CognitivServices</span></span>
- <span data-ttu-id="ed124-1942">Lade till kompletterare för SkuName och Typem som är tillgängliga i New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="ed124-1942">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="ed124-1943">Tog bort parameteruppsättningen GetSkusWithAccountParamSetName från Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="ed124-1943">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="ed124-1944">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="ed124-1944">Az.ContainerInstance</span></span>
- <span data-ttu-id="ed124-1945">Stöd för ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="ed124-1945">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="ed124-1946">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="ed124-1946">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="ed124-1947">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ed124-1947">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="ed124-1948">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ed124-1948">Az.DataLakeStore</span></span>
- <span data-ttu-id="ed124-1949">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ed124-1949">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="ed124-1950">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ed124-1950">Az.Monitor</span></span>
- <span data-ttu-id="ed124-1951">Döpte om Az.Insights till Az.Monitor och andra mindre icke-bakåtkompatibla ändringar. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ed124-1951">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="ed124-1952">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ed124-1952">Az.KeyVault</span></span>
- <span data-ttu-id="ed124-1953">Tog bort den inaktuella egenskapen PurgeDisabled från utdatatyper</span><span class="sxs-lookup"><span data-stu-id="ed124-1953">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="ed124-1954">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="ed124-1954">Az.MachineLearning</span></span>
- <span data-ttu-id="ed124-1955">Inkluderade cmdletarna från modulen Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="ed124-1955">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="ed124-1956">Az.Media</span><span class="sxs-lookup"><span data-stu-id="ed124-1956">Az.Media</span></span>
- <span data-ttu-id="ed124-1957">Tog bort inaktuella -Tags-alias från New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="ed124-1957">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="ed124-1958">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ed124-1958">Az.Network</span></span>
<span data-ttu-id="ed124-1959">Stöd har lagts till för konfiguration av RewriteRuleSets i Application Gateway</span><span class="sxs-lookup"><span data-stu-id="ed124-1959">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="ed124-1960">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="ed124-1960">New cmdlets added:</span></span>
        - <span data-ttu-id="ed124-1961">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ed124-1961">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="ed124-1962">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ed124-1962">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="ed124-1963">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ed124-1963">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="ed124-1964">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ed124-1964">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="ed124-1965">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ed124-1965">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="ed124-1966">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="ed124-1966">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="ed124-1967">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="ed124-1967">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="ed124-1968">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="ed124-1968">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="ed124-1969">Cmdletar har uppdaterats med den valfria parametern -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ed124-1969">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="ed124-1970">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ed124-1970">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="ed124-1971">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="ed124-1971">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="ed124-1972">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="ed124-1972">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="ed124-1973">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ed124-1973">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="ed124-1974">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="ed124-1974">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="ed124-1975">New-AzureRmApplicationGatewayUrlPathMapConfig har lagt till KeyVault-stöd för Application Gateway med Identity.</span><span class="sxs-lookup"><span data-stu-id="ed124-1975">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="ed124-1976">Cmdletar har uppdaterats med den valfria parametern -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="ed124-1976">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="ed124-1977">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="ed124-1977">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="ed124-1978">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="ed124-1978">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="ed124-1979">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="ed124-1979">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="ed124-1980">Cmdleten New-AzApplicationGateway har uppdaterats med den valfria parametern -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="ed124-1980">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="ed124-1981">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ed124-1981">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="ed124-1982">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ed124-1982">Az.OperationalInsights</span></span>
- <span data-ttu-id="ed124-1983">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ed124-1983">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="ed124-1984">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="ed124-1984">Az.Profile</span></span>
- <span data-ttu-id="ed124-1985">Modulnamnet har ändrats till Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ed124-1985">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="ed124-1986">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ed124-1986">Az.RecoveryServices</span></span>
- <span data-ttu-id="ed124-1987">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ed124-1987">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="ed124-1988">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ed124-1988">Az.Resources</span></span>
- <span data-ttu-id="ed124-1989">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ed124-1989">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="ed124-1990">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ed124-1990">Az.ServiceFabric</span></span>
- <span data-ttu-id="ed124-1991">Stöd för specificering av certifikat efter eget namn och tumavtryck</span><span class="sxs-lookup"><span data-stu-id="ed124-1991">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="ed124-1992">Information om fler icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ed124-1992">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="ed124-1993">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="ed124-1993">Az.SIgnalR</span></span>
- <span data-ttu-id="ed124-1994">Allmän tillgänglighet för PowerShell-cmdletar för SIgnalR</span><span class="sxs-lookup"><span data-stu-id="ed124-1994">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="ed124-1995">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ed124-1995">Az.Sql</span></span>
- <span data-ttu-id="ed124-1996">Lade till de nya identifieringstyperna Data_Exfiltration och Unsafe_Action i Threat Detection-cmdletar</span><span class="sxs-lookup"><span data-stu-id="ed124-1996">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="ed124-1997">Uppdaterade dokumentationsexempel för Sql Auditing-cmdletar</span><span class="sxs-lookup"><span data-stu-id="ed124-1997">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="ed124-1998">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ed124-1998">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="ed124-1999">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ed124-1999">Az.Storage</span></span>
- <span data-ttu-id="ed124-2000">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ed124-2000">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="ed124-2001">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ed124-2001">Az.Websites</span></span>
- <span data-ttu-id="ed124-2002">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ed124-2002">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="ed124-2003">0.7.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="ed124-2003">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="ed124-2004">Allmänt</span><span class="sxs-lookup"><span data-stu-id="ed124-2004">General</span></span>

* <span data-ttu-id="ed124-2005">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="ed124-2005">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="ed124-2006">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ed124-2006">Az.Compute</span></span>

* <span data-ttu-id="ed124-2007">Lade till stöd för UltraSSD och Galleriavbildningar i de enkla parameteruppsättningarna för `New-AzVm(ss)`-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="ed124-2007">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="ed124-2008">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ed124-2008">Az.DataLakeStore</span></span>

* <span data-ttu-id="ed124-2009">Åtgärdade avslutande snedstreck i domänen för adls-konto</span><span class="sxs-lookup"><span data-stu-id="ed124-2009">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="ed124-2010">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="ed124-2010">Az.FrontDoor</span></span>

* <span data-ttu-id="ed124-2011">Brutna länkar korrigerades</span><span class="sxs-lookup"><span data-stu-id="ed124-2011">Fixed some broken links</span></span>
    - <span data-ttu-id="ed124-2012">I artiklarna New-AzureRmFrontDoor och Set-AzureRmFrontDoor artiklar korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="ed124-2012">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="ed124-2013">I artikeln New-AzureRmFrontDoorManagedRuleObject korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="ed124-2013">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="ed124-2014">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ed124-2014">Az.RecoveryServices</span></span>

* <span data-ttu-id="ed124-2015">Lade till valideringar på klientsidan för Azure-filresurs med återställningsåtgärder.</span><span class="sxs-lookup"><span data-stu-id="ed124-2015">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="ed124-2016">Gjorde storageAccountName och storageAccountResourceGroupName valfritt för afs-återställning.</span><span class="sxs-lookup"><span data-stu-id="ed124-2016">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="ed124-2017">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ed124-2017">Az.Resources</span></span>

* <span data-ttu-id="ed124-2018">Korrigering för https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="ed124-2018">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="ed124-2019">Uppdaterade Get-AzureRmRoleAssignment så att prenumerationsomfattningen används om den anges vid begäran om klassiska administratörer.</span><span class="sxs-lookup"><span data-stu-id="ed124-2019">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="ed124-2020">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ed124-2020">Az.Sql</span></span>

* <span data-ttu-id="ed124-2021">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="ed124-2021">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="ed124-2022">Korrigerade ett problem med Get-AzureRmSqlDatabaseVulnerabilityAssessment med DotNet-kärna</span><span class="sxs-lookup"><span data-stu-id="ed124-2022">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="ed124-2023">Ändrade dokumentationen för hjälpmeddelanden som rör SQL Auditing-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="ed124-2023">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="ed124-2024">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ed124-2024">Az.Storage</span></span>

* <span data-ttu-id="ed124-2025">Lade till -EnableHierarchicalNamespace i New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ed124-2025">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="ed124-2026">Åtgärdade problemet med att cmdleten Copy File inte kunde återanvända källkontexten på målet om inte -DestContext angetts</span><span class="sxs-lookup"><span data-stu-id="ed124-2026">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="ed124-2027">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="ed124-2027">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="ed124-2028">Stöd för statisk webbplatskonfiguration</span><span class="sxs-lookup"><span data-stu-id="ed124-2028">Support Static Website configuration</span></span>
    - <span data-ttu-id="ed124-2029">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="ed124-2029">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="ed124-2030">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="ed124-2030">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="ed124-2031">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ed124-2031">Az.Websites</span></span>

* <span data-ttu-id="ed124-2032">Set-AzureRmWebApp och Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ed124-2032">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="ed124-2033">Ny parameter (-AzureStoragePath) har lagts till för att ange att Azure Storage-sökvägar ska monteras i containerappar i Windows och Linux.</span><span class="sxs-lookup"><span data-stu-id="ed124-2033">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="ed124-2034">Använder utdata från den nya cmdleten New-AzureRmWebAppAzureStoragePath som en parameter för att ange sökvägar för Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="ed124-2034">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="ed124-2035">0.6.1 – november 2018</span><span class="sxs-lookup"><span data-stu-id="ed124-2035">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="ed124-2036">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ed124-2036">Az.ApiManagement</span></span>
* <span data-ttu-id="ed124-2037">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="ed124-2037">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="ed124-2038">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ed124-2038">Az.Automation</span></span>
* <span data-ttu-id="ed124-2039">Swagger baserade Azure Automation-cmdletar</span><span class="sxs-lookup"><span data-stu-id="ed124-2039">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="ed124-2040">Cmdletar för Uppdateringshantering har lagts till</span><span class="sxs-lookup"><span data-stu-id="ed124-2040">Added Update Management cmdlets</span></span>
* <span data-ttu-id="ed124-2041">Cmdletar för källkontroll har lagts till</span><span class="sxs-lookup"><span data-stu-id="ed124-2041">Added Source Control cmdlets</span></span>
* <span data-ttu-id="ed124-2042">Remove-AzureRmAutomationHybridWorkerGroup-cmdlet har lagts till</span><span class="sxs-lookup"><span data-stu-id="ed124-2042">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="ed124-2043">Kommandot för DSC-registreringsnod har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="ed124-2043">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="ed124-2044">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ed124-2044">Az.Compute</span></span>
* <span data-ttu-id="ed124-2045">Problem med SystemAssigned-identitet har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="ed124-2045">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="ed124-2046">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="ed124-2046">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="ed124-2047">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="ed124-2047">Az.ContainerInstance</span></span>
* <span data-ttu-id="ed124-2048">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="ed124-2048">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="ed124-2049">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="ed124-2049">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="ed124-2050">uppdatera exempelbeskrivningen för marketplace-cmdletar</span><span class="sxs-lookup"><span data-stu-id="ed124-2050">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="ed124-2051">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ed124-2051">Az.Network</span></span>
* <span data-ttu-id="ed124-2052">Cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomErreller Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="ed124-2052">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="ed124-2053">ICMP tillbaka till stöd för Azure Firewall-nätverksprotokoll har lagts till</span><span class="sxs-lookup"><span data-stu-id="ed124-2053">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="ed124-2054">Uppdatera cmdlet Test-AzureRmNetworkWatcherConnectivity, lägga till verifiering av mål-id, adress och port.</span><span class="sxs-lookup"><span data-stu-id="ed124-2054">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="ed124-2055">Åtgärda problem med minnesanvändning i VirtualNetwork-karta</span><span class="sxs-lookup"><span data-stu-id="ed124-2055">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="ed124-2056">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="ed124-2056">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="ed124-2057">Åtgärda för att ändra principen för en skyddad fildelning.</span><span class="sxs-lookup"><span data-stu-id="ed124-2057">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="ed124-2058">Tidszonsprincipen har konverterats till versaler.</span><span class="sxs-lookup"><span data-stu-id="ed124-2058">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="ed124-2059">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="ed124-2059">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="ed124-2060">Exempel i New-AzureRmRecoveryServicesAsrProtectableItem har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="ed124-2060">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="ed124-2061">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="ed124-2061">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="ed124-2062">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="ed124-2062">Az.Relay</span></span>
* <span data-ttu-id="ed124-2063">Valfri parameter -KeyValue till New-AzureRmRelayKey cmdlet har lagts till, vilket gör det möjligt för användare att tillhandahålla KeyValue.</span><span class="sxs-lookup"><span data-stu-id="ed124-2063">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="ed124-2064">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ed124-2064">Az.Resources</span></span>
* <span data-ttu-id="ed124-2065">Uppdatera hjälpdokumentation för resursidentitet kopplad till parametrar i `New-AzureRmPolicyAssignment` och `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="ed124-2065">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="ed124-2066">Lägg till ett exempel för New-AzureRmPolicyDefinition som använder -Metadata</span><span class="sxs-lookup"><span data-stu-id="ed124-2066">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="ed124-2067">Korrigera så att skiftläge behålls i taggnycklar i NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="ed124-2067">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="ed124-2068">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ed124-2068">Az.ServiceFabric</span></span>
* <span data-ttu-id="ed124-2069">Lägg till utfasningsmeddelanden för kommande icke-kompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="ed124-2069">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="ed124-2070">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ed124-2070">Az.Sql</span></span>
* <span data-ttu-id="ed124-2071">Nya cmdletar för CRUD-åtgärder på Azure Sql Database-hanterad instans och Azure Sql-hanterad databas</span><span class="sxs-lookup"><span data-stu-id="ed124-2071">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="ed124-2072">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="ed124-2072">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="ed124-2073">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="ed124-2073">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="ed124-2074">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="ed124-2074">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="ed124-2075">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="ed124-2075">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="ed124-2076">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="ed124-2076">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="ed124-2077">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="ed124-2077">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="ed124-2078">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="ed124-2078">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="ed124-2079">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="ed124-2079">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="ed124-2080">Hantering av utökad granskningsprincip på en server eller en databas har aktiverats.</span><span class="sxs-lookup"><span data-stu-id="ed124-2080">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="ed124-2081">Ny parameter (PredicateExpression) har lagts till för att aktivera filtrering av granskningsloggar.</span><span class="sxs-lookup"><span data-stu-id="ed124-2081">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="ed124-2082">Cmdletar har ändrats så att de använder SQL-klienter i stället för äldre klienter.</span><span class="sxs-lookup"><span data-stu-id="ed124-2082">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="ed124-2083">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="ed124-2083">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="ed124-2084">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="ed124-2084">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="ed124-2085">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="ed124-2085">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="ed124-2086">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="ed124-2086">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="ed124-2087">Problem med att använda Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings med lagringskontots namnparameter har korrigerats</span><span class="sxs-lookup"><span data-stu-id="ed124-2087">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="ed124-2088">0.5.0 – november 2018</span><span class="sxs-lookup"><span data-stu-id="ed124-2088">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="ed124-2089">Allmänt</span><span class="sxs-lookup"><span data-stu-id="ed124-2089">General</span></span>
* <span data-ttu-id="ed124-2090">Lade till resurskompletterare till många kärn-cmdletar – dessa gör att du kan stega genom befintliga resursnamn med TABB vid interaktiva anrop till cmdletar</span><span class="sxs-lookup"><span data-stu-id="ed124-2090">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="ed124-2091">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="ed124-2091">Az.Profile</span></span>
* <span data-ttu-id="ed124-2092">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="ed124-2092">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="ed124-2093">Bytte namn på parametern TenantId i cmdleten Connect-AzAccount till Tenant och lade till ett alias för TenantId</span><span class="sxs-lookup"><span data-stu-id="ed124-2093">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="ed124-2094">Uppdaterade TenantId-beskrivningen för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="ed124-2094">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="ed124-2095">Åtgärda felmeddelande för misslyckad inloggning när du tillhandahåller klientdomän</span><span class="sxs-lookup"><span data-stu-id="ed124-2095">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="ed124-2096">Åtgärda problem med att kontextnamn hamnar i konflikt för konton utan prenumerationer i klientorganisationen</span><span class="sxs-lookup"><span data-stu-id="ed124-2096">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="ed124-2097">Åtgärda problem med DataLake-slutpunkter vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="ed124-2097">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="ed124-2098">Åtgärdade problem med att Disconnect-AzAccount kastades om den inte anslöts</span><span class="sxs-lookup"><span data-stu-id="ed124-2098">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="ed124-2099">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ed124-2099">Az.CognitiveServices</span></span>
* <span data-ttu-id="ed124-2100">Lade till åtgärden Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="ed124-2100">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ed124-2101">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ed124-2101">Az.Compute</span></span>
* <span data-ttu-id="ed124-2102">Lade till cmdletarna Add-AzVmssVMDataDisk och Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="ed124-2102">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="ed124-2103">Get-AzVMImage visar AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="ed124-2103">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="ed124-2104">Åtgärdade att värdena för alternativen SetAzVMChefExtension -BootstrapOptions och -JsonAttribute inte angavs i json-format.</span><span class="sxs-lookup"><span data-stu-id="ed124-2104">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ed124-2105">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ed124-2105">Az.DataLakeStore</span></span>
* <span data-ttu-id="ed124-2106">Uppdatera DataLake-paketet till 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="ed124-2106">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="ed124-2107">Lägg till standardsamtidighet för flertrådade åtgärder.</span><span class="sxs-lookup"><span data-stu-id="ed124-2107">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="ed124-2108">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="ed124-2108">Az.Insights</span></span>
* <span data-ttu-id="ed124-2109">Åtgärdade problem #7267 (autoskalningsområde)</span><span class="sxs-lookup"><span data-stu-id="ed124-2109">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="ed124-2110">Problem med att uppräknade parametrar inte ställdes in ordentligt när du skapade en ny autoskalningsregel (de ställdes alltid in med standardvärdet).</span><span class="sxs-lookup"><span data-stu-id="ed124-2110">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="ed124-2111">Åtgärdade problem #7513 [Insights] Set-AzDiagnosticSetting kräver uttrycklig specifikation av kategorier när inställningar skapas</span><span class="sxs-lookup"><span data-stu-id="ed124-2111">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="ed124-2112">Nu kräver inte cmdleten uttrycklig anvisning av kategorierna för att aktiveras under skapande, d.v.s. den fungerar enligt beskrivning</span><span class="sxs-lookup"><span data-stu-id="ed124-2112">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ed124-2113">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ed124-2113">Az.Network</span></span>
* <span data-ttu-id="ed124-2114">PeeringType ändrades till en obligatorisk parameter för följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="ed124-2114">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="ed124-2115">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="ed124-2115">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="ed124-2116">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="ed124-2116">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="ed124-2117">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="ed124-2117">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="ed124-2118">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="ed124-2118">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="ed124-2119">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="ed124-2119">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="ed124-2120">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="ed124-2120">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="ed124-2121">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="ed124-2121">Az.PolicyInsights</span></span>
* <span data-ttu-id="ed124-2122">Cmdletar för principreparation har lagts till</span><span class="sxs-lookup"><span data-stu-id="ed124-2122">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="ed124-2123">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ed124-2123">Az.Resources</span></span>
* <span data-ttu-id="ed124-2124">Korrigering för https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="ed124-2124">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="ed124-2125">Tillåt att resurser listas med parametern -ResourceId för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="ed124-2125">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="ed124-2126">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ed124-2126">Az.ServiceBus</span></span>
* <span data-ttu-id="ed124-2127">Skrivskyddad MigrationState-egenskap har lagts till i PSServiceBusMigrationConfigurationAttributes, som hjälper till att hålla koll på migreringstillståndet.</span><span class="sxs-lookup"><span data-stu-id="ed124-2127">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="ed124-2128">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ed124-2128">Az.ServiceFabric</span></span>
* <span data-ttu-id="ed124-2129">Åtgärda att lägga till certifikat till Linux-Vmss.</span><span class="sxs-lookup"><span data-stu-id="ed124-2129">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="ed124-2130">Åtgärdade Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="ed124-2130">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="ed124-2131">Använd rätt tumavtryck från nya certifikat (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="ed124-2131">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="ed124-2132">Visa undantag korrekt (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="ed124-2132">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="ed124-2133">Åtgärdade Update-AzServiceFabricDurability så att klusterkonfigurationen uppdateras innan Vmss-åtgärden CreateOrUpdate påbörjas.</span><span class="sxs-lookup"><span data-stu-id="ed124-2133">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="ed124-2134">0.4.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="ed124-2134">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="ed124-2135">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="ed124-2135">Az.Profile</span></span>
* <span data-ttu-id="ed124-2136">Åtgärdade problemet med Get-AzSubscription i CloudShell</span><span class="sxs-lookup"><span data-stu-id="ed124-2136">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="ed124-2137">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="ed124-2137">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ed124-2138">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ed124-2138">Az.Compute</span></span>
* <span data-ttu-id="ed124-2139">Nya storlekar lades till i listan över godkända VM-storlekar för vilka accelererat nätverk kommer att aktiveras vid användning av den enkla parameteruppsättningen för New-AzVm</span><span class="sxs-lookup"><span data-stu-id="ed124-2139">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="ed124-2140">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="ed124-2140">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ed124-2141">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ed124-2141">Az.DataLakeStore</span></span>
* <span data-ttu-id="ed124-2142">Lägger till stöd för regler för virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="ed124-2142">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="ed124-2143">Get-AzDataLakeStoreVirtualNetworkRule: Hämtar eller listar regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ed124-2143">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="ed124-2144">Add-AzDataLakeStoreVirtualNetworkRule: Lägger till en regel för virtuellt nätverk i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="ed124-2144">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="ed124-2145">Set-AzDataLakeStoreVirtualNetworkRule: Ändrar den angivna regeln för virtuellt nätverk i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="ed124-2145">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="ed124-2146">Remove-AzDataLakeStoreVirtualNetworkRule: Tar bort en regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ed124-2146">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ed124-2147">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ed124-2147">Az.Network</span></span>
* <span data-ttu-id="ed124-2148">Skicka protokollvärdet till serverdelen för att uppdatera cmdleten Test-AzNetworkWatcherConnectivity.</span><span class="sxs-lookup"><span data-stu-id="ed124-2148">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="ed124-2149">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="ed124-2149">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="ed124-2150">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ed124-2150">Az.Resources</span></span>
* <span data-ttu-id="ed124-2151">Åtgärdade problem där Get-AzRoleDefinition genererar ett oläsligt undantag (när standardprofilen inte innehåller någon prenumeration och ingen omfattning har angetts) genom att lägga till ett beskrivande undantag i scenariot.</span><span class="sxs-lookup"><span data-stu-id="ed124-2151">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="ed124-2152">Ställ in ”RoleDefinitionNameParameterSet” som standardparameteruppsättning.</span><span class="sxs-lookup"><span data-stu-id="ed124-2152">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="ed124-2153">0.3.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="ed124-2153">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="ed124-2154">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="ed124-2154">Azure.Storage</span></span>
* <span data-ttu-id="ed124-2155">Åtgärda fel där Kopiera blob/fil inte kopierar metadata när målplatsen har ett problem med metadata</span><span class="sxs-lookup"><span data-stu-id="ed124-2155">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="ed124-2156">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="ed124-2156">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="ed124-2157">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="ed124-2157">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="ed124-2158">Stöd för att hämta användningsinformation om en Storage-resurs för en specifik plats och för att lägga till ett varningsmeddelande för att hämta användningsinformation om en global Storage-resurs är inaktuellt.</span><span class="sxs-lookup"><span data-stu-id="ed124-2158">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="ed124-2159">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="ed124-2159">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="ed124-2160">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ed124-2160">Az.CognitiveServices</span></span>
* <span data-ttu-id="ed124-2161">Stöd för Get-AzCognitiveServicesAccountSkus utan ett befintligt konto.</span><span class="sxs-lookup"><span data-stu-id="ed124-2161">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ed124-2162">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ed124-2162">Az.Compute</span></span>
* <span data-ttu-id="ed124-2163">Åtgärdade fel där Get-AzVM -ResourceGroupName <rg> returnerar fler än 50 resultat om det behövs</span><span class="sxs-lookup"><span data-stu-id="ed124-2163">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="ed124-2164">Lade till ett exempel för SimpleParameterSet i hjälpen för cmdleten New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="ed124-2164">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="ed124-2165">Ett stavfel i förloppsmeddelandet för Azure Disk Encryption har korrigerats</span><span class="sxs-lookup"><span data-stu-id="ed124-2165">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="ed124-2166">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="ed124-2166">Az.DataFactoryV2</span></span>
* <span data-ttu-id="ed124-2167">ADF .Net SDK-versionen har uppdaterats till 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="ed124-2167">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ed124-2168">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ed124-2168">Az.Network</span></span>
* <span data-ttu-id="ed124-2169">Funktionalitet för NetworkProfile har lagts till.</span><span class="sxs-lookup"><span data-stu-id="ed124-2169">Added NetworkProfile functionality.</span></span> <span data-ttu-id="ed124-2170">nya cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="ed124-2170">new cmdlets added</span></span>
    - <span data-ttu-id="ed124-2171">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ed124-2171">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="ed124-2172">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ed124-2172">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="ed124-2173">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ed124-2173">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="ed124-2174">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ed124-2174">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="ed124-2175">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="ed124-2175">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="ed124-2176">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="ed124-2176">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="ed124-2177">Länk för tjänstassociering på modell för undernät har lagts till</span><span class="sxs-lookup"><span data-stu-id="ed124-2177">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="ed124-2178">Cmdletarna New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap och Remove-AzVirtualNetworkTap har lagts till</span><span class="sxs-lookup"><span data-stu-id="ed124-2178">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="ed124-2179">Cmdletarna Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig och Remove-AzNEtworkInterfaceTapConfig har lagts till</span><span class="sxs-lookup"><span data-stu-id="ed124-2179">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="ed124-2180">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="ed124-2180">Az.RedisCache</span></span>
* <span data-ttu-id="ed124-2181">Tillåt att alla strängar används som storleksparametrar framöver.</span><span class="sxs-lookup"><span data-stu-id="ed124-2181">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="ed124-2182">Lägg till P5 i popup-fönstret PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="ed124-2182">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="ed124-2183">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ed124-2183">Az.Resources</span></span>
* <span data-ttu-id="ed124-2184">Parametern -Mode som saknades i Set-AzPolicyDefinition har lagts till</span><span class="sxs-lookup"><span data-stu-id="ed124-2184">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="ed124-2185">Åtgärdade buggen för cmdleten Get-AzProviderOperation för åtgärder med ursprung som innehåller användare</span><span class="sxs-lookup"><span data-stu-id="ed124-2185">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="ed124-2186">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ed124-2186">Az.Sql</span></span>
* <span data-ttu-id="ed124-2187">Ett problem där vissa cmdletar för säkerhetskopiering inte kunde identifiera den aktuella azure-prenumerationen har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="ed124-2187">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ed124-2188">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ed124-2188">Az.Websites</span></span>
* <span data-ttu-id="ed124-2189">Ny cmdlet: Get-AzWebAppContainerContinuousDeploymentUrl – Hämtar webhook-URL:en för kontinuerlig distribution av container</span><span class="sxs-lookup"><span data-stu-id="ed124-2189">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="ed124-2190">Nya cmdletar: New-AzWebAppContainerPSSession och Enter-WebAppContainerPSSession – Startar en PowerShell-fjärrsession i en containerapp för windows</span><span class="sxs-lookup"><span data-stu-id="ed124-2190">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="ed124-2191">0.2.0 – september 2018</span><span class="sxs-lookup"><span data-stu-id="ed124-2191">0.2.0 - September 2018</span></span>
 <span data-ttu-id="ed124-2192">Första versionen</span><span class="sxs-lookup"><span data-stu-id="ed124-2192">Initial Release</span></span>