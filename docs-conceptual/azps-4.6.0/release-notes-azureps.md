---
title: Viktig information om Azure PowerShell
description: Lär dig mer om alla de senaste uppdateringarna för Azure PowerShell-modulerna.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 52129f31202a8ae04bf80988b5aa07b12fe081b8
ms.sourcegitcommit: 15f21c40dcb7610e2fbaaabf264ad925e4224500
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/22/2020
ms.locfileid: "90913388"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="a52f3-103">Viktig information om Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="a52f3-103">Azure PowerShell release notes</span></span>

## <a name="460---august-2020"></a><span data-ttu-id="a52f3-104">4.6.0 – augusti 2020</span><span class="sxs-lookup"><span data-stu-id="a52f3-104">4.6.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a52f3-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a52f3-105">Az.Accounts</span></span>
* <span data-ttu-id="a52f3-106">Alla offentliga molnmiljöer läses in när slutpunktsidentifieringen inte returnerar AzureCloud (standard) eller andra offentliga miljöer [#12633]</span><span class="sxs-lookup"><span data-stu-id="a52f3-106">Loaded all public cloud environments when discovery endpoint doesn't return default AzureCloud or other public environments [#12633]</span></span>
* <span data-ttu-id="a52f3-107">SubscriptionPolicies har exponerats i Get-AzSubscription [#12551]</span><span class="sxs-lookup"><span data-stu-id="a52f3-107">Exposed SubscriptionPolicies in 'Get-AzSubscription' [#12551]</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a52f3-108">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a52f3-108">Az.Automation</span></span>
* <span data-ttu-id="a52f3-109">Parametern -RunOn har lagts till i Set-AzAutomationWebhook för att ange en Hybrid Worker-grupp</span><span class="sxs-lookup"><span data-stu-id="a52f3-109">Added '-RunOn' parameters to 'Set-AzAutomationWebhook' to specify a Hybrid Worker Group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a52f3-110">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a52f3-110">Az.Compute</span></span>
* <span data-ttu-id="a52f3-111">Parametern -EncryptionAtHost har lagts till i New-AzVm, New-AzVmss, New-AzVMConfig, New-AzVmssConfig, Update-AzVM och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a52f3-111">Added '-EncryptionAtHost' parameter to 'New-AzVm', 'New-AzVmss', 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVM', and 'Update-AzVmss'</span></span>
* <span data-ttu-id="a52f3-112">SecurityProfile har lagts till i Get-AzVM och Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a52f3-112">Added 'SecurityProfile' to 'Get-AzVM' and 'Get-AzVmss' return object</span></span>
* <span data-ttu-id="a52f3-113">Växeln -InstanceView har lagts till som valfri parameter i Get-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="a52f3-113">Added '-InstanceView' switch as optional parameter to 'Get-AzHostGroup'</span></span>
* <span data-ttu-id="a52f3-114">En ny cmdlet, Invoke-AzVmPatchAssessment, har lagts till</span><span class="sxs-lookup"><span data-stu-id="a52f3-114">Added new cmdlet 'Invoke-AzVmPatchAssessment'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a52f3-115">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a52f3-115">Az.DataFactory</span></span>
* <span data-ttu-id="a52f3-116">Saknade egenskaper har lagts till i klassen PSPipelineRun.</span><span class="sxs-lookup"><span data-stu-id="a52f3-116">Added missing properties to PSPipelineRun class.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="a52f3-117">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a52f3-117">Az.HDInsight</span></span>
* <span data-ttu-id="a52f3-118">Stöd för att skapa kluster med funktionen för kryptering under överföring.</span><span class="sxs-lookup"><span data-stu-id="a52f3-118">Supported creating cluster with encryption at host feature.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a52f3-119">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a52f3-119">Az.KeyVault</span></span>
* <span data-ttu-id="a52f3-120">Varningsmeddelanden har lagts till för planering att inaktivera mjuk borttagning</span><span class="sxs-lookup"><span data-stu-id="a52f3-120">Added warning messages for planning to disable soft delete</span></span>
* <span data-ttu-id="a52f3-121">Varningsmeddelanden har lagts till för planering att ta bort attributet SecretValueText</span><span class="sxs-lookup"><span data-stu-id="a52f3-121">Added warning messages for planning to remove attribute SecretValueText</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="a52f3-122">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="a52f3-122">Az.Maintenance</span></span>
* <span data-ttu-id="a52f3-123">Valfria schemarelaterade fält har lagts till i New-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="a52f3-123">Added optional schedule related fields to 'New-AzMaintenanceConfiguration'</span></span>
* <span data-ttu-id="a52f3-124">En ny cmdlet har lagts till för Get-AzMaintenancePublicConfiguration</span><span class="sxs-lookup"><span data-stu-id="a52f3-124">Added new cmdlet for 'Get-AzMaintenancePublicConfiguration'</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="a52f3-125">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="a52f3-125">Az.ManagedServices</span></span>
* <span data-ttu-id="a52f3-126">Varningar har lagts till om icke-bakåtkompatibla ändringar för cmdletar för tilldelning och definition av hanterade tjänster</span><span class="sxs-lookup"><span data-stu-id="a52f3-126">Added breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a52f3-127">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a52f3-127">Az.Monitor</span></span>
* <span data-ttu-id="a52f3-128">Utökade parametern som angetts i Set-AzDiagnosticSetting för separering av aktivering av loggar och mått [#12482]</span><span class="sxs-lookup"><span data-stu-id="a52f3-128">Extended the parameter set in 'Set-AzDiagnosticSetting' for separation of Logs and Metrics enablement [#12482]</span></span>
* <span data-ttu-id="a52f3-129">Åtgärdat fel för Add-AzMetricAlertRuleV2 vid hämtning av måttavisering från pipelinen</span><span class="sxs-lookup"><span data-stu-id="a52f3-129">Fixed bug for 'Add-AzMetricAlertRuleV2' when getting metric alert from pipeline</span></span>

#### <a name="azresources"></a><span data-ttu-id="a52f3-130">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a52f3-130">Az.Resources</span></span>
* <span data-ttu-id="a52f3-131">Get-AzPolicyAlias-svaret har uppdaterats för att ta med information som anger om aliaset kan ändras eller inte av Azure Policy.</span><span class="sxs-lookup"><span data-stu-id="a52f3-131">Updated 'Get-AzPolicyAlias' response to include information indicating whether the alias is modifiable by Azure Policy.</span></span>
* <span data-ttu-id="a52f3-132">Skapade en ny cmdlet, set-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="a52f3-132">Created new cmdlet 'Set-AzRoleAssignment'</span></span>
* <span data-ttu-id="a52f3-133">Get-AzDeploymentManagementGroupWhatIfResult har lagts till för att hämta What-If-resultat för ARM-mall i hanteringsgruppsomfånget</span><span class="sxs-lookup"><span data-stu-id="a52f3-133">Added 'Get-AzDeploymentManagementGroupWhatIfResult' for getting ARM template What-If results at management Group scope</span></span>
* <span data-ttu-id="a52f3-134">En ny cmdlet, Get-AzTenantWhatIfResult, har lagts till för att hämta What-If-resultat för ARM-mall i klientorganisationsomfånget</span><span class="sxs-lookup"><span data-stu-id="a52f3-134">Added 'Get-AzTenantWhatIfResult' new cmdlet for getting ARM template What-If results at tenant scope</span></span>
* <span data-ttu-id="a52f3-135">-WhatIf och -Confirm har åsidosatts för New-AzManagementGroupDeployment och New-AzTenantDeployment för att använda What-If-resultat för ARM-mall</span><span class="sxs-lookup"><span data-stu-id="a52f3-135">Overrode '-WhatIf' and '-Confirm' for 'New-AzManagementGroupDeployment' and 'New-AzTenantDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="a52f3-136">Beteenden har åtgärdats för -WhatIf och -Confirm för nya cmdletar för distribution så att de stämmer överens med $WhatIfPreference och $ConfirmPreference.</span><span class="sxs-lookup"><span data-stu-id="a52f3-136">Fixed the behaviors of '-WhatIf' and '-Confirm' for new deployment cmdlets so they comply with $WhatIfPreference and $ConfirmPreference.</span></span>
* <span data-ttu-id="a52f3-137">Serialiseringsfel har åtgärdats för -TemplateObject och TemplateParameterObject [#1528] [#6292]</span><span class="sxs-lookup"><span data-stu-id="a52f3-137">Fixed serialization error for '-TemplateObject' and 'TemplateParameterObject' [#1528] [#6292]</span></span>
* <span data-ttu-id="a52f3-138">Attribut som medför icke-bakåtkompatibel ändring har lagts till i Get-AzResourceGroupDeploymentOperation för den kommande ändringen av utdatatyp</span><span class="sxs-lookup"><span data-stu-id="a52f3-138">Added breaking change attribute to 'Get-AzResourceGroupDeploymentOperation' for the upcoming output type change</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="a52f3-139">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="a52f3-139">Az.SignalR</span></span>
* <span data-ttu-id="a52f3-140">Fel i hjälpfilerna Restart-AzSignalR och Update-AzSignalR har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="a52f3-140">Fixed 'Restart-AzSignalR' and 'Update-AzSignalR' help files errors</span></span>
* <span data-ttu-id="a52f3-141">Cmdletarna Update-AzSignalRNetworkAcl och Set-AzSignalRUpstream har lagts till</span><span class="sxs-lookup"><span data-stu-id="a52f3-141">Added cmdlets 'Update-AzSignalRNetworkAcl', 'Set-AzSignalRUpstream'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a52f3-142">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a52f3-142">Az.Storage</span></span>
* <span data-ttu-id="a52f3-143">Stöd för blobfrågeacceleration</span><span class="sxs-lookup"><span data-stu-id="a52f3-143">Supported blob query acceleration</span></span>
    -  <span data-ttu-id="a52f3-144">Get-AzStorageBlobQueryResult</span><span class="sxs-lookup"><span data-stu-id="a52f3-144">'Get-AzStorageBlobQueryResult'</span></span>
    -  <span data-ttu-id="a52f3-145">New-AzStorageBlobQueryConfig</span><span class="sxs-lookup"><span data-stu-id="a52f3-145">'New-AzStorageBlobQueryConfig'</span></span>
* <span data-ttu-id="a52f3-146">Hjälpfil har lagts till, ytterligare beskrivning har lagts till och stavfel har korrigerats</span><span class="sxs-lookup"><span data-stu-id="a52f3-146">Updated help file, added more description, and fixed typo</span></span>
    -  <span data-ttu-id="a52f3-147">”Start-AzStorageBlobCopy”</span><span class="sxs-lookup"><span data-stu-id="a52f3-147">'Start-AzStorageBlobCopy'</span></span>
    -  <span data-ttu-id="a52f3-148">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="a52f3-148">'Get-AzDataLakeGen2Item'</span></span>
* <span data-ttu-id="a52f3-149">Problem med att ladda ned blob när relaterad underordnad katalog saknas har åtgärdats [#12592]</span><span class="sxs-lookup"><span data-stu-id="a52f3-149">Fixed download blob fail when related sub directory not exist [#12592]</span></span>
    -  <span data-ttu-id="a52f3-150">”Get-AzStorageBlobContent”</span><span class="sxs-lookup"><span data-stu-id="a52f3-150">'Get-AzStorageBlobContent'</span></span>
* <span data-ttu-id="a52f3-151">Replikeringsprincip för att ange, hämta, ta bort objekt på Storage-konton stöds</span><span class="sxs-lookup"><span data-stu-id="a52f3-151">Supported Set/Get/Remove Object Replication Policy on Storage accounts</span></span>
    - <span data-ttu-id="a52f3-152">New-AzStorageObjectReplicationPolicyRule</span><span class="sxs-lookup"><span data-stu-id="a52f3-152">'New-AzStorageObjectReplicationPolicyRule'</span></span>
    - <span data-ttu-id="a52f3-153">Set-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="a52f3-153">'Set-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="a52f3-154">Get-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="a52f3-154">'Get-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="a52f3-155">Remove-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="a52f3-155">'Remove-AzStorageObjectReplicationPolicy'</span></span>
* <span data-ttu-id="a52f3-156">Stöd har lagts till för att aktivera/inaktivera ChangeFeed i Blob Service för ett Storage-konto</span><span class="sxs-lookup"><span data-stu-id="a52f3-156">Supported enable/disable ChangeFeed on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="a52f3-157">”Update-AzStorageBlobServiceProperty”</span><span class="sxs-lookup"><span data-stu-id="a52f3-157">'Update-AzStorageBlobServiceProperty'</span></span>

## <a name="450---august-2020"></a><span data-ttu-id="a52f3-158">4.5.0 – augusti 2020</span><span class="sxs-lookup"><span data-stu-id="a52f3-158">4.5.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a52f3-159">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a52f3-159">Az.Accounts</span></span>
* <span data-ttu-id="a52f3-160">Uppdaterade ”Connect-AzAccount” så att det accepterar parametern ”MaxContextPopulation” [#9865]</span><span class="sxs-lookup"><span data-stu-id="a52f3-160">Updated 'Connect-AzAccount' to accept parameter 'MaxContextPopulation' [#9865]</span></span>
* <span data-ttu-id="a52f3-161">Uppdaterade SubscriptionClient-versionen till 2019-06-01 och visa klientdomäner [#9838]</span><span class="sxs-lookup"><span data-stu-id="a52f3-161">Updated SubscriptionClient version to 2019-06-01 and display tenant domains [#9838]</span></span>
* <span data-ttu-id="a52f3-162">Information om hemklientorganisation och managedBy-klientorganisation som stöds för prenumerationen</span><span class="sxs-lookup"><span data-stu-id="a52f3-162">Supported home tenant and managedBy tenant information of subscription</span></span>
* <span data-ttu-id="a52f3-163">Korrigerade modulnamn, versionsinformation i telemetridata</span><span class="sxs-lookup"><span data-stu-id="a52f3-163">Corrected module name, version info in telemetry data</span></span>
* <span data-ttu-id="a52f3-164">Justerade SqlDatabaseDnsSuffix och ServiceManagementUrl om miljöns slutpunkt för metadata returnerar ett inkompatibelt värde</span><span class="sxs-lookup"><span data-stu-id="a52f3-164">Adjusted SqlDatabaseDnsSuffix and ServiceManagementUrl if environment metadata endpoint returns incompatible value</span></span>

#### <a name="azaks"></a><span data-ttu-id="a52f3-165">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="a52f3-165">Az.Aks</span></span>
* <span data-ttu-id="a52f3-166">Tog bort ”ClientIdAndSecret” för ”ServicePrincipalIdAndSecret” och ställde in ”ClientIdAndSecret” som ett alias [#12381].</span><span class="sxs-lookup"><span data-stu-id="a52f3-166">Removed 'ClientIdAndSecret' to 'ServicePrincipalIdAndSecret' and set 'ClientIdAndSecret' as an alias [#12381].</span></span>
* <span data-ttu-id="a52f3-167">Tog bort ”Get-AzAks”/”New-AzAks”/”Remove-AzAks”/”Set-AzAks” för ”Get-AzAksCluster”/”New-AzAksCluster”/”Remove-AzAksCluster”/”Set-AzAksCluster” och ställde in de ursprungliga som alias [#12373].</span><span class="sxs-lookup"><span data-stu-id="a52f3-167">Removed 'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks' to 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster' and set the original ones as alias [#12373].</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="a52f3-168">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a52f3-168">Az.ApiManagement</span></span>
* <span data-ttu-id="a52f3-169">Lade till ny cmdlet: ”Add-AzApiManagementApiToGateway”.</span><span class="sxs-lookup"><span data-stu-id="a52f3-169">Added new 'Add-AzApiManagementApiToGateway' cmdlet.</span></span>
* <span data-ttu-id="a52f3-170">Lade till ny cmdlet: ”Get-AzApiManagementGateway”.</span><span class="sxs-lookup"><span data-stu-id="a52f3-170">Added new 'Get-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="a52f3-171">Lade till ny cmdlet: ”Get-AzApiManagementGatewayHostnameConfiguration”.</span><span class="sxs-lookup"><span data-stu-id="a52f3-171">Added new 'Get-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="a52f3-172">Lade till ny cmdlet: ”Get-AzApiManagementGatewayKey”.</span><span class="sxs-lookup"><span data-stu-id="a52f3-172">Added new 'Get-AzApiManagementGatewayKey' cmdlet.</span></span>
* <span data-ttu-id="a52f3-173">Lade till ny cmdlet: ”New-AzApiManagementGateway”.</span><span class="sxs-lookup"><span data-stu-id="a52f3-173">Added new 'New-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="a52f3-174">Lade till ny cmdlet: ”New-AzApiManagementGatewayHostnameConfiguration”.</span><span class="sxs-lookup"><span data-stu-id="a52f3-174">Added new 'New-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="a52f3-175">Lade till ny cmdlet: ”New-AzApiManagementResourceLocationObject”.</span><span class="sxs-lookup"><span data-stu-id="a52f3-175">Added new 'New-AzApiManagementResourceLocationObject' cmdlet.</span></span>
* <span data-ttu-id="a52f3-176">Lade till ny cmdlet: ”Remove-AzApiManagementApiFromGateway”.</span><span class="sxs-lookup"><span data-stu-id="a52f3-176">Added new 'Remove-AzApiManagementApiFromGateway' cmdlet.</span></span>
* <span data-ttu-id="a52f3-177">Lade till ny cmdlet: ”Remove-AzApiManagementGateway”.</span><span class="sxs-lookup"><span data-stu-id="a52f3-177">Added new 'Remove-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="a52f3-178">Lade till ny cmdlet: ”Remove-AzApiManagementGatewayHostnameConfiguration”.</span><span class="sxs-lookup"><span data-stu-id="a52f3-178">Added new 'Remove-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="a52f3-179">Lade till ny cmdlet: ”Update-AzApiManagementGateway”.</span><span class="sxs-lookup"><span data-stu-id="a52f3-179">Added new 'Update-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="a52f3-180">Lade till den nya valfria parametern [-GatewayId] till cmdleten ”Get-AzApiManagementApi”.</span><span class="sxs-lookup"><span data-stu-id="a52f3-180">Added new optional [-GatewayId] parameter to the 'Get-AzApiManagementApi' cmdlet.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="a52f3-181">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a52f3-181">Az.CognitiveServices</span></span>
* <span data-ttu-id="a52f3-182">Använde ”Neka” som standardåtgärd för NetworkRules.</span><span class="sxs-lookup"><span data-stu-id="a52f3-182">Used 'Deny' specifically as NetworkRules default action.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="a52f3-183">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="a52f3-183">Az.FrontDoor</span></span>
* <span data-ttu-id="a52f3-184">Åtgärdade ett problem där ett undantag uppstår när Enum.Parse försöker att tvinga ett null-värde till aktiverade eller inaktiverade uppräkningsvärden [#12344]</span><span class="sxs-lookup"><span data-stu-id="a52f3-184">Fixed an issue where an exception is being thrown when Enum.Parse tries to coerce a null value to an Enabled or Disabled enum values [#12344]</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="a52f3-185">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a52f3-185">Az.HDInsight</span></span>
* <span data-ttu-id="a52f3-186">Stöd för att skapa kluster med funktionen Kryptering under överföring.</span><span class="sxs-lookup"><span data-stu-id="a52f3-186">Supported creating cluster with encryption in transit feature.</span></span>
    - <span data-ttu-id="a52f3-187">Lägg till den nya parametern ”EncryptionInTransit” till cmdleten ”New-AzHDInsightCluster”</span><span class="sxs-lookup"><span data-stu-id="a52f3-187">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="a52f3-188">Lägg till den nya parametern ”EncryptionInTransit” till cmdleten ”New-AzHDInsightClusterConfig”</span><span class="sxs-lookup"><span data-stu-id="a52f3-188">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="a52f3-189">Stöd för att skapa kluster med funktionen privat länk:</span><span class="sxs-lookup"><span data-stu-id="a52f3-189">Supported creating cluster with private link feature:</span></span>
    - <span data-ttu-id="a52f3-190">Lägg till de nya parametrarna ”PublicNetworkAccessType” och ”OutboundPublicNetworkAccessType” till cmdleten ”New-AzHDInsightCluster”</span><span class="sxs-lookup"><span data-stu-id="a52f3-190">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="a52f3-191">Lägg till de nya parametrarna ”PublicNetworkAccessType” och ”OutboundPublicNetworkAccessType” till cmdleten ”New-AzHDInsightClusterConfig”</span><span class="sxs-lookup"><span data-stu-id="a52f3-191">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="a52f3-192">Returnerade information om det virtuella nätverket vid anrop till ”New-AzHDInsightCluster” eller ”Get-AzHDInsightCluster”</span><span class="sxs-lookup"><span data-stu-id="a52f3-192">Returned virtual network information when calling 'New-AzHDInsightCluster' or 'Get-AzHDInsightCluster'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a52f3-193">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a52f3-193">Az.Network</span></span>
* <span data-ttu-id="a52f3-194">Stöd har lagts till för parametern AddressPrefixType i ”Remove-AzExpressRouteCircuitConnectionConfig”</span><span class="sxs-lookup"><span data-stu-id="a52f3-194">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="a52f3-195">Lade till bakåtkompatibel ändringar: PeerAddressType-funktioner för privat peering i ”Remove-AzExpressRouteCircutPeeringConfig”.</span><span class="sxs-lookup"><span data-stu-id="a52f3-195">Added non-breaking changes: PeerAddressType functionality for Private Peering in 'Remove-AzExpressRouteCircutPeeringConfig'.</span></span>
* <span data-ttu-id="a52f3-196">Koden ändrades för att ignorera skiftläge för parametrarna AddressPrefixType och PeerAddressType.</span><span class="sxs-lookup"><span data-stu-id="a52f3-196">Code changed to ignore case for AddressPrefixType and PeerAddressType parameter.</span></span>
* <span data-ttu-id="a52f3-197">Ändrade varningsmeddelandet för ”New-AzLoadBalancerFrontendIpConfig”, ”New-AzPublicIpAddress” och ”New-AzPublicIpPrefix”.</span><span class="sxs-lookup"><span data-stu-id="a52f3-197">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="a52f3-198">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a52f3-198">Az.OperationalInsights</span></span>
* <span data-ttu-id="a52f3-199">Lade till alternativet ”-ForceDelete” för ”Remove-AzOperationalInsightsworkspace”</span><span class="sxs-lookup"><span data-stu-id="a52f3-199">Added '-ForceDelete' option for 'Remove-AzOperationalInsightsworkspace'</span></span>
* <span data-ttu-id="a52f3-200">Lade till ny cmdlet: ”Get-AzOperationalInsightsDeletedWorkspace”</span><span class="sxs-lookup"><span data-stu-id="a52f3-200">Added new cmdlet 'Get-AzOperationalInsightsDeletedWorkspace'</span></span>
* <span data-ttu-id="a52f3-201">Lade till ny cmdlet: ”Restore-AzOperationalInsightsWorkspace”</span><span class="sxs-lookup"><span data-stu-id="a52f3-201">Added new cmdlet 'Restore-AzOperationalInsightsWorkspace'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a52f3-202">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a52f3-202">Az.RecoveryServices</span></span>
* <span data-ttu-id="a52f3-203">Förbättrade sättet Azure Backup-containrar/objekt identifieras.</span><span class="sxs-lookup"><span data-stu-id="a52f3-203">Improved the Azure Backup container/item discovery experience.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a52f3-204">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a52f3-204">Az.Resources</span></span>
* <span data-ttu-id="a52f3-205">Lade till egenskaperna ”Condition”, ”ConditionVersion” och ”Description” till ”New-AzRoleAssignment”</span><span class="sxs-lookup"><span data-stu-id="a52f3-205">Added properties 'Condition', 'ConditionVersion' and 'Description' to 'New-AzRoleAssignment'</span></span>
    - <span data-ttu-id="a52f3-206">Detta omfattade alla relevanta ändringar av datamodellerna</span><span class="sxs-lookup"><span data-stu-id="a52f3-206">This included all the relevant changes to the data models</span></span>

#### <a name="azsql"></a><span data-ttu-id="a52f3-207">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a52f3-207">Az.Sql</span></span>
* <span data-ttu-id="a52f3-208">Korrigerade ett potentiellt fel med skiftlägesokänsliga servernamn i ”New-AzSqlServer” och ”Set-AzSqlServer”</span><span class="sxs-lookup"><span data-stu-id="a52f3-208">Fixed potential server name case insensitive error in 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="a52f3-209">Korrigerade att fel databasnamn returnerades vid ett befintligt databasfel i ”New-AzSqlDatabaseSecondary”</span><span class="sxs-lookup"><span data-stu-id="a52f3-209">Fixed wrong database name returned on existing database error in 'New-AzSqlDatabaseSecondary'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a52f3-210">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a52f3-210">Az.Storage</span></span>
* <span data-ttu-id="a52f3-211">Stöd för att skapa container/blob för SAS-token med de nya behörigheterna x, t</span><span class="sxs-lookup"><span data-stu-id="a52f3-211">Supported create container/blob Sas token with new permission x,t</span></span>
    -  <span data-ttu-id="a52f3-212">”New-AzStorageBlobSASToken”</span><span class="sxs-lookup"><span data-stu-id="a52f3-212">'New-AzStorageBlobSASToken'</span></span>
    -  <span data-ttu-id="a52f3-213">”New-AzStorageContainerSASToken”</span><span class="sxs-lookup"><span data-stu-id="a52f3-213">'New-AzStorageContainerSASToken'</span></span>
* <span data-ttu-id="a52f3-214">Stöd för att skapa konto för SAS-token med de nya behörigheterna x, t, f</span><span class="sxs-lookup"><span data-stu-id="a52f3-214">Supported create account Sas token with new permission x,t,f</span></span>
    -  <span data-ttu-id="a52f3-215">”New-AzStorageAccountSASToken”</span><span class="sxs-lookup"><span data-stu-id="a52f3-215">'New-AzStorageAccountSASToken'</span></span>
* <span data-ttu-id="a52f3-216">Stöd för att hämta förbrukning av enskild filresurs</span><span class="sxs-lookup"><span data-stu-id="a52f3-216">Supported get single file share usage</span></span>
    - <span data-ttu-id="a52f3-217">”Get-AzRmStorageShare”</span><span class="sxs-lookup"><span data-stu-id="a52f3-217">'Get-AzRmStorageShare'</span></span>

## <a name="440---july-2020"></a><span data-ttu-id="a52f3-218">4.4.0 – juli 2020</span><span class="sxs-lookup"><span data-stu-id="a52f3-218">4.4.0 - July 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a52f3-219">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a52f3-219">Az.Accounts</span></span>
* <span data-ttu-id="a52f3-220">En ny cmdlet, ”Invoke-AzRestMethod”, har lagts till</span><span class="sxs-lookup"><span data-stu-id="a52f3-220">Added new cmdlet 'Invoke-AzRestMethod'</span></span>
* <span data-ttu-id="a52f3-221">Ett problem åtgärdades som kan orsaka autentiseringsfel i scenarier med fler processer, t.ex. när flera Azure PowerShell-cmdletar körs med ”Start-Job” [#9448]</span><span class="sxs-lookup"><span data-stu-id="a52f3-221">Fixed an issue that may cause authentication errors in multi-process scenarios such as running multiple Azure PowerShell cmdlets using 'Start-Job' [#9448]</span></span>

#### <a name="azaks"></a><span data-ttu-id="a52f3-222">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="a52f3-222">Az.Aks</span></span>
* <span data-ttu-id="a52f3-223">Felet som gjorde att ”Get-AzAks” inte hämtade alla kluster har åtgärdats [#12296]</span><span class="sxs-lookup"><span data-stu-id="a52f3-223">Fixed bug 'Get-AzAks' doesn't get all clusters [#12296]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="a52f3-224">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a52f3-224">Az.AnalysisServices</span></span>
* <span data-ttu-id="a52f3-225">Projektreferensen till autentisering har tagits bort</span><span class="sxs-lookup"><span data-stu-id="a52f3-225">Removed project reference to Authentication</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a52f3-226">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a52f3-226">Az.Automation</span></span>
* <span data-ttu-id="a52f3-227">Problemet som gjorde att strängar med escape-tecken inte kunde konverteras till JSON-objekt har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="a52f3-227">Fixed the issue that string with escape chars cannot be converted into json object.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a52f3-228">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a52f3-228">Az.Compute</span></span>
* <span data-ttu-id="a52f3-229">En varning har lats till som visas när ”New-AzVmss” används utan den senaste avbildningsversionen</span><span class="sxs-lookup"><span data-stu-id="a52f3-229">Added warning when using 'New-AzVmss' without 'latest' image version</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a52f3-230">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a52f3-230">Az.DataFactory</span></span>
* <span data-ttu-id="a52f3-231">Globala parametrar har lagts till för Data Factory.</span><span class="sxs-lookup"><span data-stu-id="a52f3-231">Added global parameters to Data Factory.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="a52f3-232">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="a52f3-232">Az.EventGrid</span></span>
* <span data-ttu-id="a52f3-233">Modulen har uppdaterats så att API-version 2020-06-01 används.</span><span class="sxs-lookup"><span data-stu-id="a52f3-233">Updated to use the 2020-06-01 API version.</span></span>
* <span data-ttu-id="a52f3-234">Nya funktioner har lagts till:</span><span class="sxs-lookup"><span data-stu-id="a52f3-234">Added new features:</span></span>
    - <span data-ttu-id="a52f3-235">Indatamappning</span><span class="sxs-lookup"><span data-stu-id="a52f3-235">Input mapping</span></span>
    - <span data-ttu-id="a52f3-236">Schema för händelseleverans</span><span class="sxs-lookup"><span data-stu-id="a52f3-236">Event Delivery Schema</span></span>
    - <span data-ttu-id="a52f3-237">Private Link</span><span class="sxs-lookup"><span data-stu-id="a52f3-237">Private Link</span></span>
    - <span data-ttu-id="a52f3-238">Cloud Event V10 Schema</span><span class="sxs-lookup"><span data-stu-id="a52f3-238">Cloud Event V10 Schema</span></span>
    - <span data-ttu-id="a52f3-239">Service Bus-ämne som mål</span><span class="sxs-lookup"><span data-stu-id="a52f3-239">Service Bus Topic As Destination</span></span>
    - <span data-ttu-id="a52f3-240">Azure-funktion som mål</span><span class="sxs-lookup"><span data-stu-id="a52f3-240">Azure Function As Destination</span></span>
    - <span data-ttu-id="a52f3-241">Webhook-batchbearbetning</span><span class="sxs-lookup"><span data-stu-id="a52f3-241">WebHook Batching</span></span>
    - <span data-ttu-id="a52f3-242">Säker webhook (AAD-stöd)</span><span class="sxs-lookup"><span data-stu-id="a52f3-242">Secure webhook (AAD support)</span></span>
    - <span data-ttu-id="a52f3-243">IpFiltering</span><span class="sxs-lookup"><span data-stu-id="a52f3-243">IpFiltering</span></span>
* <span data-ttu-id="a52f3-244">Uppdaterade cmdletar:</span><span class="sxs-lookup"><span data-stu-id="a52f3-244">Updated cmdlets:</span></span>
    - <span data-ttu-id="a52f3-245">”New-AzEventGridSubscription”/”Update-AzEventGridSubscription”:</span><span class="sxs-lookup"><span data-stu-id="a52f3-245">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span></span>
        - <span data-ttu-id="a52f3-246">Lägg till nya valfria parametrar för att ge stöd för webhook-batchbearbetning.</span><span class="sxs-lookup"><span data-stu-id="a52f3-246">Add new optional parameters to support webhook batching.</span></span>
        - <span data-ttu-id="a52f3-247">Lägg till nya valfria parametrar för att ge stöd för skyddad webhook med AAD.</span><span class="sxs-lookup"><span data-stu-id="a52f3-247">Add new optional parameters to support secured webhook using AAD.</span></span>
        - <span data-ttu-id="a52f3-248">Lägg till ny enum (uppräkning) för EndpointType-parametern för att ge stöd för Azure-funktion och Service Bus-ämne som nya mål.</span><span class="sxs-lookup"><span data-stu-id="a52f3-248">Add new enum for EndpointType parameter to support azure function and service bus topic as new destinations.</span></span>
        - <span data-ttu-id="a52f3-249">Lägg till ny valfri parameter för leveransschema.</span><span class="sxs-lookup"><span data-stu-id="a52f3-249">Add new optional parameter for delivery schema.</span></span>
    - <span data-ttu-id="a52f3-250">”New-AzEventGridTopic”/”Update-AzEventGridTopic” och ”New-AzEventGridDomain”/”Update-AzEventGridDomain”:</span><span class="sxs-lookup"><span data-stu-id="a52f3-250">'New-AzEventGridTopic'/'Update-AzEventGridTopic' and 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span></span>
        - <span data-ttu-id="a52f3-251">Lägg till nya valfria parametrar för att ge stöd för IpFiltering.</span><span class="sxs-lookup"><span data-stu-id="a52f3-251">Add new optional parameters to support IpFiltering.</span></span>
    - <span data-ttu-id="a52f3-252">”New-AzEventGridTopic”/”New-AzEventGridDomain”:</span><span class="sxs-lookup"><span data-stu-id="a52f3-252">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span></span>
        - <span data-ttu-id="a52f3-253">Lägg till nya valfria parametrar för att ge stöd för indatamappning.</span><span class="sxs-lookup"><span data-stu-id="a52f3-253">Add new optional parameters to support Input mapping.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="a52f3-254">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="a52f3-254">Az.FrontDoor</span></span>
* <span data-ttu-id="a52f3-255">Modulen har uppdaterats så att API 2020-05-01 används</span><span class="sxs-lookup"><span data-stu-id="a52f3-255">Updated module to use API 2020-05-01</span></span>
* <span data-ttu-id="a52f3-256">Stöd för privat länk har lagts till för Storage-, KeyVault- och Web App Service-resurser</span><span class="sxs-lookup"><span data-stu-id="a52f3-256">Added Private link support for Storage, Keyvault and Web App Service resources</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="a52f3-257">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a52f3-257">Az.HDInsight</span></span>
* <span data-ttu-id="a52f3-258">Stöd för att skapa kluster med ADLSGen1/2-lagring i nationella moln.</span><span class="sxs-lookup"><span data-stu-id="a52f3-258">Supported creating cluster with ADLSGen1/2 storage in national clouds.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a52f3-259">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a52f3-259">Az.Monitor</span></span>
* <span data-ttu-id="a52f3-260">Bugg som orsakade fel med ”Get-AzDiagnosticSetting” när mått eller loggar var null har åtgärdats [#12272]</span><span class="sxs-lookup"><span data-stu-id="a52f3-260">Fixed bug for 'Get-AzDiagnosticSetting' when metrics or logs are null [#12272]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a52f3-261">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a52f3-261">Az.Network</span></span>
* <span data-ttu-id="a52f3-262">Parameterväxlingen i VWan HubVnet-anslutningar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="a52f3-262">Fixed parameters swap in VWan HubVnet connection</span></span>
* <span data-ttu-id="a52f3-263">Nya cmdletar har lagts till för platser för virtuella installationer i Azure-nätverk</span><span class="sxs-lookup"><span data-stu-id="a52f3-263">Added new cmdlets for Azure Network Virtual Appliance Sites</span></span>
    - <span data-ttu-id="a52f3-264">”Get-AzVirtualApplianceSite”</span><span class="sxs-lookup"><span data-stu-id="a52f3-264">'Get-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="a52f3-265">”New-AzVirtualApplianceSite”</span><span class="sxs-lookup"><span data-stu-id="a52f3-265">'New-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="a52f3-266">”Remove-AzVirtualApplianceSite”</span><span class="sxs-lookup"><span data-stu-id="a52f3-266">'Remove-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="a52f3-267">”Update-AzVirtualApplianceSite”</span><span class="sxs-lookup"><span data-stu-id="a52f3-267">'Update-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="a52f3-268">”New-AzOffice365PolicyProperty”</span><span class="sxs-lookup"><span data-stu-id="a52f3-268">'New-AzOffice365PolicyProperty'</span></span>
* <span data-ttu-id="a52f3-269">Nya cmdletar har lagts till för virtuella installationer i Azure-nätverk</span><span class="sxs-lookup"><span data-stu-id="a52f3-269">Added new cmdlets for Azure Network Virtual Appliance</span></span>
    - <span data-ttu-id="a52f3-270">”Get-AzNetworkVirtualAppliance”</span><span class="sxs-lookup"><span data-stu-id="a52f3-270">'Get-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="a52f3-271">”New-AzNetworkVirtualAppliance”</span><span class="sxs-lookup"><span data-stu-id="a52f3-271">'New-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="a52f3-272">”Remove-AzNetworkVirtualAppliance”</span><span class="sxs-lookup"><span data-stu-id="a52f3-272">'Remove-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="a52f3-273">”Update-AzNetworkVirtualAppliance”</span><span class="sxs-lookup"><span data-stu-id="a52f3-273">'Update-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="a52f3-274">”Get-AzNetworkVirtualApplianceSku”</span><span class="sxs-lookup"><span data-stu-id="a52f3-274">'Get-AzNetworkVirtualApplianceSku'</span></span>
    - <span data-ttu-id="a52f3-275">”New-AzVirtualApplianceSkuProperty”</span><span class="sxs-lookup"><span data-stu-id="a52f3-275">'New-AzVirtualApplianceSkuProperty'</span></span>
* <span data-ttu-id="a52f3-276">Application Gateway har introducerats i vanliga cmdletar för Private Link</span><span class="sxs-lookup"><span data-stu-id="a52f3-276">Onboarded Application Gateway to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="a52f3-277">StorageSync har introducerats i vanliga cmdletar för Private Link</span><span class="sxs-lookup"><span data-stu-id="a52f3-277">Onboarded StorageSync to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="a52f3-278">SignalR har introducerats i vanliga cmdletar för Private Link</span><span class="sxs-lookup"><span data-stu-id="a52f3-278">Onboarded SignalR to Private Link Common Cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a52f3-279">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a52f3-279">Az.RecoveryServices</span></span>
* <span data-ttu-id="a52f3-280">Projektreferensen till autentisering har tagits bort</span><span class="sxs-lookup"><span data-stu-id="a52f3-280">Removed project reference to Authentication</span></span>
* <span data-ttu-id="a52f3-281">Azure Backup-anpassade cmdletar gör text mer korrekt.</span><span class="sxs-lookup"><span data-stu-id="a52f3-281">Azure Backup tuned cmdlets help text to be more accurate.</span></span>
* <span data-ttu-id="a52f3-282">Stöd har lagts till som gör att Azure Backup kan hämta MAB-agentjobb med cmdleten ”Get-AzRecoveryServicesBackupJob”.</span><span class="sxs-lookup"><span data-stu-id="a52f3-282">Azure Backup added support for fetching MAB agent jobs using 'Get-AzRecoveryServicesBackupJob' cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a52f3-283">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a52f3-283">Az.Resources</span></span>
* <span data-ttu-id="a52f3-284">”Save-AzResourceGroupDeploymentTemplate” har uppdaterats för att använda SDK:n.</span><span class="sxs-lookup"><span data-stu-id="a52f3-284">Updated 'Save-AzResourceGroupDeploymentTemplate' to use the SDK.</span></span>
* <span data-ttu-id="a52f3-285">Cmdleten ”Unregister-AzResourceProvider” har lagts till.</span><span class="sxs-lookup"><span data-stu-id="a52f3-285">Added 'Unregister-AzResourceProvider' cmdlet.</span></span>

#### <a name="azsql"></a><span data-ttu-id="a52f3-286">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a52f3-286">Az.Sql</span></span>
* <span data-ttu-id="a52f3-287">Stöd har lagts till för SPN och gästanvändare i cmdleten ”Set-AzSqlInstanceActiveDirectoryAdministrator”</span><span class="sxs-lookup"><span data-stu-id="a52f3-287">Added support for Service principal and guest users in Set-AzSqlInstanceActiveDirectoryAdministrator cmdlet'</span></span>
* <span data-ttu-id="a52f3-288">En bugg har åtgärdats i cmdletar för dataklassificering.</span><span class="sxs-lookup"><span data-stu-id="a52f3-288">Fixed a bug in Data Classification cmdlets.'</span></span>
* <span data-ttu-id="a52f3-289">Stöd har lagts till för redundansväxling med Azure SQL Managed Instance: ”Invoke-AzSqlInstanceFailover”</span><span class="sxs-lookup"><span data-stu-id="a52f3-289">Added support for Azure SQL Managed Instance failover: 'Invoke-AzSqlInstanceFailover'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a52f3-290">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a52f3-290">Az.Storage</span></span>
* <span data-ttu-id="a52f3-291">Problemet som gjorde att UserAgent inte lades till för vissa cmdletar för dataplanet har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="a52f3-291">Fixed the issue that UserAgent is not added for some data plane cmdlets.</span></span>
* <span data-ttu-id="a52f3-292">Stöd har lagts till för att skapa/uppdatera Storage-konto med MinimumTlsVersion och AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="a52f3-292">Supported create/update Storage account with MinimumTlsVersion and AllowBlobPublicAccess</span></span>
    -  <span data-ttu-id="a52f3-293">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="a52f3-293">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="a52f3-294">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="a52f3-294">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="a52f3-295">Stöd har lagts till för att aktivera/inaktivera versionshantering i Blob Service för ett Storage-konto</span><span class="sxs-lookup"><span data-stu-id="a52f3-295">Support enable/disable versioning on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="a52f3-296">”Update-AzStorageBlobServiceProperty”</span><span class="sxs-lookup"><span data-stu-id="a52f3-296">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="a52f3-297">Stöd har lagts till för att visa blobar med blobversioner</span><span class="sxs-lookup"><span data-stu-id="a52f3-297">Support list blobs with blob versions</span></span>
    - <span data-ttu-id="a52f3-298">”Get-AzStorageBlob”</span><span class="sxs-lookup"><span data-stu-id="a52f3-298">'Get-AzStorageBlob'</span></span>
* <span data-ttu-id="a52f3-299">Stöd har lagts till för att hämta/ta bort enskilda ögonblicksbilder av blobar eller blobversioner</span><span class="sxs-lookup"><span data-stu-id="a52f3-299">Support get/remove single blob snapshot or blob version</span></span>
    - <span data-ttu-id="a52f3-300">”Get-AzStorageBlob”</span><span class="sxs-lookup"><span data-stu-id="a52f3-300">'Get-AzStorageBlob'</span></span>
    - <span data-ttu-id="a52f3-301">”Remove-AzStorageBlob”</span><span class="sxs-lookup"><span data-stu-id="a52f3-301">'Remove-AzStorageBlob'</span></span>
* <span data-ttu-id="a52f3-302">Stöd har lagts till för pipelines från blobobjekt genererade av Azure.Storage.Blobs V12</span><span class="sxs-lookup"><span data-stu-id="a52f3-302">Support pipeline from blob object generated from Azure.Storage.Blobs V12</span></span>
    - <span data-ttu-id="a52f3-303">”Get-AzStorageBlobContent”</span><span class="sxs-lookup"><span data-stu-id="a52f3-303">'Get-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="a52f3-304">”New-AzStorageBlobSASToken”</span><span class="sxs-lookup"><span data-stu-id="a52f3-304">'New-AzStorageBlobSASToken'</span></span>
    - <span data-ttu-id="a52f3-305">”Remove-AzStorageBlob”</span><span class="sxs-lookup"><span data-stu-id="a52f3-305">'Remove-AzStorageBlob'</span></span>
    - <span data-ttu-id="a52f3-306">”Set-AzStorageBlobContent”</span><span class="sxs-lookup"><span data-stu-id="a52f3-306">'Set-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="a52f3-307">”Start-AzStorageBlobCopy”</span><span class="sxs-lookup"><span data-stu-id="a52f3-307">'Start-AzStorageBlobCopy'</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="a52f3-308">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="a52f3-308">Az.StorageSync</span></span>
* <span data-ttu-id="a52f3-309">En ny version har lagts till för StorageSync SDK som körs mot ApiVersion 2020-03-01</span><span class="sxs-lookup"><span data-stu-id="a52f3-309">Added a new version StorageSync SDK targeting ApiVersion 2020-03-01</span></span>
* <span data-ttu-id="a52f3-310">En cmdlet för synkroniseringstjänsten för lagringsuppdatering har lagts till</span><span class="sxs-lookup"><span data-stu-id="a52f3-310">Added Update Storage Sync Service cmdlet</span></span>
    - <span data-ttu-id="a52f3-311">”Set-AzStorageSyncService”</span><span class="sxs-lookup"><span data-stu-id="a52f3-311">'Set-AzStorageSyncService'</span></span>
* <span data-ttu-id="a52f3-312">IncomingTrafficPolicy och PrivateEndpointConnections har lagts till för StorageSyncService-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="a52f3-312">Added IncomingTrafficPolicy and PrivateEndpointConnections to StorageSyncService cmdlets.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a52f3-313">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a52f3-313">Az.Websites</span></span>
* <span data-ttu-id="a52f3-314">Stöd har lagts till för att utföra åtgärder för platser som inte tillhör samma resursgrupp som App Services-planen</span><span class="sxs-lookup"><span data-stu-id="a52f3-314">Added support to perform operations for Slots not in the same resource group as the App Service Plan</span></span>

## <a name="430---june-2020"></a><span data-ttu-id="a52f3-315">4.3.0 – juni 2020</span><span class="sxs-lookup"><span data-stu-id="a52f3-315">4.3.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a52f3-316">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a52f3-316">Az.Accounts</span></span>
* <span data-ttu-id="a52f3-317">Stöd för identifiering av miljöinställning som standard och tillägg av miljön via ”Add-AzEnvironment”</span><span class="sxs-lookup"><span data-stu-id="a52f3-317">Supported discovering environment setting by default and adding environment via 'Add-AzEnvironment'</span></span>
* <span data-ttu-id="a52f3-318">Uppdatera förinlästa sammansättningar [#12024], [#11976]</span><span class="sxs-lookup"><span data-stu-id="a52f3-318">Update preloaded assemblies [#12024], [#11976]</span></span>
* <span data-ttu-id="a52f3-319">Uppdaterad Azure.Core-sammansättning</span><span class="sxs-lookup"><span data-stu-id="a52f3-319">Updated Azure.Core assembly</span></span>
* <span data-ttu-id="a52f3-320">Ett problem har åtgärdats som kan orsaka att ”Connect-AzAccount” misslyckas vid körning av flera trådar [#11201]</span><span class="sxs-lookup"><span data-stu-id="a52f3-320">Fixed an issue that may cause 'Connect-AzAccount' to fail in multi-threaded execution [#11201]</span></span>

#### <a name="azaks"></a><span data-ttu-id="a52f3-321">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="a52f3-321">Az.Aks</span></span>
* <span data-ttu-id="a52f3-322">Användning av gamla [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) ersattes med anrop till API:erna [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) och [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials)</span><span class="sxs-lookup"><span data-stu-id="a52f3-322">Replaced usage of old [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) with calls to [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) and [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials) APIs</span></span>

#### <a name="azbatch"></a><span data-ttu-id="a52f3-323">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="a52f3-323">Az.Batch</span></span>
* <span data-ttu-id="a52f3-324">Az.Batch har uppdaterats att använda ”Microsoft.Azure.Management.Batch” SDK till och med version 11.0.0.</span><span class="sxs-lookup"><span data-stu-id="a52f3-324">Updated Az.Batch to use 'Microsoft.Azure.Management.Batch' SDK version to 11.0.0</span></span>
* <span data-ttu-id="a52f3-325">Möjligheten att ange BatchAccount-identiteten har lagts till i cmdleten ”New-AzBatchAccount”</span><span class="sxs-lookup"><span data-stu-id="a52f3-325">Added the ability to set the BatchAccount Identity in the 'New-AzBatchAccount' cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="a52f3-326">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a52f3-326">Az.CognitiveServices</span></span>
* <span data-ttu-id="a52f3-327">Stöd för att visa kontofunktioner.</span><span class="sxs-lookup"><span data-stu-id="a52f3-327">Supported displaying account capabilities.</span></span>
* <span data-ttu-id="a52f3-328">Stöd för att ändra PublicNetworkAccess.</span><span class="sxs-lookup"><span data-stu-id="a52f3-328">Supported modifying PublicNetworkAccess.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a52f3-329">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a52f3-329">Az.Compute</span></span>
* <span data-ttu-id="a52f3-330">Parametern SimulateEviction har lagts till i cmdletarna set-AzVM och set-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="a52f3-330">Added SimulateEviction parameter to Set-AzVM and Set-AzVmssVM cmdlets.</span></span>
* <span data-ttu-id="a52f3-331">”Premium_LRS” har lagts till i argumentslutföraren för parametern StorageAccountType för cmdleten New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="a52f3-331">Added 'Premium_LRS' to the argument completer of StorageAccountType parameter for New-AzGalleryImageVersion cmdlet.</span></span>
* <span data-ttu-id="a52f3-332">Understatusar har lagts till i VMCustomScriptExtension [#11297]</span><span class="sxs-lookup"><span data-stu-id="a52f3-332">Added Substatuses to VMCustomScriptExtension [#11297]</span></span>
* <span data-ttu-id="a52f3-333">”Delete” har lagts till i argumentslutföraren för parametern EvictionPolicy för cmdletarna New-AzVM och New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="a52f3-333">Added 'Delete' to the argument completer of EvictionPolicy parameter for New-AzVM and New-AzVMConfig cmdlets.</span></span>
* <span data-ttu-id="a52f3-334">Åtgärdat namn för nytt VM-tillägg för SAP</span><span class="sxs-lookup"><span data-stu-id="a52f3-334">Fixed name of new VM Extension for SAP</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a52f3-335">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a52f3-335">Az.DataFactory</span></span>
* <span data-ttu-id="a52f3-336">ADF .Net SDK har uppdaterats till 4.9.0</span><span class="sxs-lookup"><span data-stu-id="a52f3-336">Updated ADF .Net SDK version to 4.9.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="a52f3-337">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a52f3-337">Az.EventHub</span></span>
* <span data-ttu-id="a52f3-338">Parametrar för hanterad identitet har lagts till i cmdletarna ”New-AzEventHubNamespace” och ”set-AzEventHubNamespace”</span><span class="sxs-lookup"><span data-stu-id="a52f3-338">Added Managed Identity parameters to 'New-AzEventHubNamespace' and 'Set-AzEventHubNamespace' cmdlets</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="a52f3-339">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="a52f3-339">Az.Functions</span></span>
* <span data-ttu-id="a52f3-340">Stöd har lagts till för att skapa PowerShell 7.0- och Java 11-funktionsappar</span><span class="sxs-lookup"><span data-stu-id="a52f3-340">Added support to create PowerShell 7.0 and Java 11 function apps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="a52f3-341">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a52f3-341">Az.HDInsight</span></span>
* <span data-ttu-id="a52f3-342">Stöd för listning av värdar och omstart för specifika värdar i HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="a52f3-342">Supported listing hosts and restart specific hosts of the HDInsight cluster.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="a52f3-343">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="a52f3-343">Az.HealthcareApis</span></span>
* <span data-ttu-id="a52f3-344">Uppdaterade SDK-versionen till 1.1.0</span><span class="sxs-lookup"><span data-stu-id="a52f3-344">Updated the SDK version to 1.1.0</span></span>
* <span data-ttu-id="a52f3-345">Stöd har lagts till för exportinställningar och hanterad identitet</span><span class="sxs-lookup"><span data-stu-id="a52f3-345">Added support for Export settings and Managed Identity</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a52f3-346">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a52f3-346">Az.Monitor</span></span>
* <span data-ttu-id="a52f3-347">Parameter för inmatningsobjekt har åtgärdats för ”Set-AzActivityLogAlert”</span><span class="sxs-lookup"><span data-stu-id="a52f3-347">Fixed input object parameter for 'Set-AzActivityLogAlert'</span></span>
* <span data-ttu-id="a52f3-348">Parametern ”InputObject” har åtgärdats för ”Set-AzActionGroup” [#10868]</span><span class="sxs-lookup"><span data-stu-id="a52f3-348">Fixed 'InputObject' parameter for 'Set-AzActionGroup' [#10868]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a52f3-349">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a52f3-349">Az.Network</span></span>
* <span data-ttu-id="a52f3-350">Stöd har lagts till för parametern AddressPrefixType i ”Remove-AzExpressRouteCircuitConnectionConfig”</span><span class="sxs-lookup"><span data-stu-id="a52f3-350">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="a52f3-351">Nya cmdletar har lagts till för Azure FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="a52f3-351">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="a52f3-352">”New-AzFirewallPolicyDnsSetting”</span><span class="sxs-lookup"><span data-stu-id="a52f3-352">'New-AzFirewallPolicyDnsSetting'</span></span>
    - <span data-ttu-id="a52f3-353">Stöd för mål-FQDN i nätverksregler för brandväggsprincip</span><span class="sxs-lookup"><span data-stu-id="a52f3-353">Support for Destination FQDN in Network Rules for Firewall Policy</span></span>
* <span data-ttu-id="a52f3-354">Stöd har lagts till för åtgärder i serverdelsadresspooler</span><span class="sxs-lookup"><span data-stu-id="a52f3-354">Added support for backend address pool operations</span></span>
    - <span data-ttu-id="a52f3-355">”New-AzLoadBalancerBackendAddressConfig”</span><span class="sxs-lookup"><span data-stu-id="a52f3-355">'New-AzLoadBalancerBackendAddressConfig'</span></span>
    - <span data-ttu-id="a52f3-356">”New-AzLoadBalancerBackendAddressPool”</span><span class="sxs-lookup"><span data-stu-id="a52f3-356">'New-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="a52f3-357">”Set-AzLoadBalancerBackendAddressPool”</span><span class="sxs-lookup"><span data-stu-id="a52f3-357">'Set-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="a52f3-358">”Remove-AzLoadBalancerBackendAddressPool”</span><span class="sxs-lookup"><span data-stu-id="a52f3-358">'Remove-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="a52f3-359">”Get-AzLoadBalancerBackendAddressPool”</span><span class="sxs-lookup"><span data-stu-id="a52f3-359">'Get-AzLoadBalancerBackendAddressPool'</span></span>
* <span data-ttu-id="a52f3-360">Namnvalidering har lagts till för ”New-AzIpGroup”</span><span class="sxs-lookup"><span data-stu-id="a52f3-360">Added name validation for 'New-AzIpGroup'</span></span>
* <span data-ttu-id="a52f3-361">Nya cmdletar har lagts till för Azure FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="a52f3-361">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="a52f3-362">”New-AzFirewallPolicyThreatIntelWhitelist”</span><span class="sxs-lookup"><span data-stu-id="a52f3-362">'New-AzFirewallPolicyThreatIntelWhitelist'</span></span>
* <span data-ttu-id="a52f3-363">Nedanstående kommandon för funktionen har uppdaterats: Konfiguration/borttagning av anpassade DNS-servrar på VirtualWan P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="a52f3-363">Updated below commands for feature: Custom dns servers set/remove on VirtualWan P2SVpnGateway.</span></span>
    - <span data-ttu-id="a52f3-364">New-AzP2sVpnGateway har uppdaterats: Den valfria parametern ”-CustomDnsServer” har lagts till för att kunder ska kunna ange att deras DNS-servrar ska konfigureras på P2SVpnGateway, som kan användas av punkt-till-plats-klienter.</span><span class="sxs-lookup"><span data-stu-id="a52f3-364">Updated New-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
    - <span data-ttu-id="a52f3-365">Update-AzP2sVpnGateway har uppdaterats: Den valfria parametern ”-CustomDnsServer” har lagts till för att kunder ska kunna ange att deras DNS-servrar ska konfigureras på P2SVpnGateway, som kan användas av punkt-till-plats-klienter.</span><span class="sxs-lookup"><span data-stu-id="a52f3-365">Updated Update-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
* <span data-ttu-id="a52f3-366">”Update-AzVpnGateway” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="a52f3-366">Updated 'Update-AzVpnGateway'</span></span>
    - <span data-ttu-id="a52f3-367">Den valfria parametern ”-BgpPeeringAddress” har lagts till för att kunder ska kunna ange sina anpassade BGP:er som ska konfigurerar på VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="a52f3-367">Added optional parameter '-BgpPeeringAddress' for customers to specify their custom bgps to set on VpnGateway.</span></span>
* <span data-ttu-id="a52f3-368">Ny cmdlet har lagts till för att stödja återställning av en VirtualHub-resurs routningsstatus:</span><span class="sxs-lookup"><span data-stu-id="a52f3-368">Added new cmdlet to support resetting the routing state of a VirtualHub resource:</span></span>
    - <span data-ttu-id="a52f3-369">”Reset-AzHubRouter”</span><span class="sxs-lookup"><span data-stu-id="a52f3-369">'Reset-AzHubRouter'</span></span>
* <span data-ttu-id="a52f3-370">Nedanstående saker har uppdaterats baserat på den senaste Swagger-ändringen för brandväggspolicyn</span><span class="sxs-lookup"><span data-stu-id="a52f3-370">Updated below things based on recent swagger change for Firewall Policy</span></span>
    - <span data-ttu-id="a52f3-371">Namn ändras för RuleGroup, RuleCollectionGroup och RuleType</span><span class="sxs-lookup"><span data-stu-id="a52f3-371">Changes names for RuleGroup, RuleCollectionGroup and RuleType</span></span>
    - <span data-ttu-id="a52f3-372">Stöd har lagts till för NAT-regelsamlingar för brandväggsprincip så att flera NAT-regelsamlingar stöds</span><span class="sxs-lookup"><span data-stu-id="a52f3-372">Added support for Firewall Policy NAT Rule Collections to support multiple NAT Rule Collection</span></span>
* <span data-ttu-id="a52f3-373">[Icke-bakåtkompatibel ändring] Den obligatoriska parametern ”SourceIpGroup” har lagts till för ”New-AzFirewallPolicyApplicationRule” och ”New-AzFirewallPolicyNetworkRule”.</span><span class="sxs-lookup"><span data-stu-id="a52f3-373">[Breaking Change] Added mandatory parameter 'SourceIpGroup' for 'New-AzFirewallPolicyApplicationRule' and 'New-AzFirewallPolicyNetworkRule'.</span></span>
* <span data-ttu-id="a52f3-374">[Icke-bakåtkompatibel ändring] ”New-AzFirewallPolicyApplicationRule” har åtgärdats, parametern ”SourceAddress” är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="a52f3-374">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="a52f3-375">[Icke-bakåtkompatibel ändring] ”New-AzFirewallPolicyApplicationRule” har åtgärdats, parametern ”SourceAddress” är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="a52f3-375">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="a52f3-376">[Icke-bakåtkompatibel ändring] Obligatoriska parametrar har tagits bort: ”TranslatedAddress”, ”TranslatedPort” för ”New-AzFirewallPolicyNatRuleCollection”.</span><span class="sxs-lookup"><span data-stu-id="a52f3-376">[Breaking Change] Removed mandatory parameters: 'TranslatedAddress', 'TranslatedPort' for 'New-AzFirewallPolicyNatRuleCollection'.</span></span>
* <span data-ttu-id="a52f3-377">Nya cmdletar har lagts till för att stödja PrivateLink på Application Gateway</span><span class="sxs-lookup"><span data-stu-id="a52f3-377">Added new cmdlets to support PrivateLink On Application Gateway</span></span>
    - <span data-ttu-id="a52f3-378">”New-AzApplicationGatewayPrivateLinkConfiguration”</span><span class="sxs-lookup"><span data-stu-id="a52f3-378">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="a52f3-379">”Get-AzApplicationGatewayPrivateLinkConfiguration”</span><span class="sxs-lookup"><span data-stu-id="a52f3-379">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="a52f3-380">”New-AzApplicationGatewayPrivateLinkConfiguration”</span><span class="sxs-lookup"><span data-stu-id="a52f3-380">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="a52f3-381">”Set-AzApplicationGatewayPrivateLinkConfiguration”</span><span class="sxs-lookup"><span data-stu-id="a52f3-381">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="a52f3-382">”Remove-AzApplicationGatewayPrivateLinkConfiguration”</span><span class="sxs-lookup"><span data-stu-id="a52f3-382">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="a52f3-383">”New-AzApplicationGatewayPrivateLinkIpConfiguration”</span><span class="sxs-lookup"><span data-stu-id="a52f3-383">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span></span>
* <span data-ttu-id="a52f3-384">Nya cmdletar har lagts till för VirtualHubs underordnade resurs HubRouteTables.</span><span class="sxs-lookup"><span data-stu-id="a52f3-384">Added new cmdlets for HubRouteTables child resource of VirtualHub.</span></span>
    - <span data-ttu-id="a52f3-385">”New-AzVHubRoute”</span><span class="sxs-lookup"><span data-stu-id="a52f3-385">'New-AzVHubRoute'</span></span>
    - <span data-ttu-id="a52f3-386">”New-AzVHubRouteTable”</span><span class="sxs-lookup"><span data-stu-id="a52f3-386">'New-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="a52f3-387">”Get-AzVHubRouteTable”</span><span class="sxs-lookup"><span data-stu-id="a52f3-387">'Get-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="a52f3-388">”Update-AzVHubRouteTable”</span><span class="sxs-lookup"><span data-stu-id="a52f3-388">'Update-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="a52f3-389">”Remove-AzVHubRouteTable”</span><span class="sxs-lookup"><span data-stu-id="a52f3-389">'Remove-AzVHubRouteTable'</span></span>
* <span data-ttu-id="a52f3-390">Befintliga cmdletar har uppdaterats för att stödja valfri RoutingConfiguration-indataparameter för anpassad routning i VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="a52f3-390">Updated existing cmdlets to support optional RoutingConfiguration input parameter for custom routing in VirtualWan.</span></span>
    - <span data-ttu-id="a52f3-391">”New-AzExpressRouteConnection”</span><span class="sxs-lookup"><span data-stu-id="a52f3-391">'New-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="a52f3-392">”Set-AzExpressRouteConnection”</span><span class="sxs-lookup"><span data-stu-id="a52f3-392">'Set-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="a52f3-393">”New-AzVirtualHubVnetConnection”</span><span class="sxs-lookup"><span data-stu-id="a52f3-393">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="a52f3-394">”Update-AzVirtualHubVnetConnection”</span><span class="sxs-lookup"><span data-stu-id="a52f3-394">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="a52f3-395">”New-AzVpnConnection”</span><span class="sxs-lookup"><span data-stu-id="a52f3-395">'New-AzVpnConnection'</span></span>
    - <span data-ttu-id="a52f3-396">”Update-AzVpnConnection”</span><span class="sxs-lookup"><span data-stu-id="a52f3-396">'Update-AzVpnConnection'</span></span>
    - <span data-ttu-id="a52f3-397">”New-AzP2sVpnGateway”</span><span class="sxs-lookup"><span data-stu-id="a52f3-397">'New-AzP2sVpnGateway'</span></span>
    - <span data-ttu-id="a52f3-398">”Update-AzP2sVpnGateway”</span><span class="sxs-lookup"><span data-stu-id="a52f3-398">'Update-AzP2sVpnGateway'</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="a52f3-399">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a52f3-399">Az.OperationalInsights</span></span>
* <span data-ttu-id="a52f3-400">Fast fel PSWorkspace implementerar inte IOperationalInsightsWorkspace [#12135]</span><span class="sxs-lookup"><span data-stu-id="a52f3-400">Fixed bug PSWorkspace doesn't implement IOperationalInsightsWorkspace [#12135]</span></span>
* <span data-ttu-id="a52f3-401">”pergb2018” har lagts till i uppsättningen med giltiga värden för parametern ”Sku” i ”Set-AzOperationalInsightsWorkspace”</span><span class="sxs-lookup"><span data-stu-id="a52f3-401">Added 'pergb2018' to valid value set of parameter 'Sku' in 'Set-AzOperationalInsightsWorkspace'</span></span> 
* <span data-ttu-id="a52f3-402">Alias ”FunctionParameters” lades till för parametern ”FunctionParameter” till</span><span class="sxs-lookup"><span data-stu-id="a52f3-402">Added alias 'FunctionParameters' for parameter 'FunctionParameter' to</span></span>
    - <span data-ttu-id="a52f3-403">”New-AzOperationalInsightsSavedSearch”</span><span class="sxs-lookup"><span data-stu-id="a52f3-403">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="a52f3-404">”Set-AzOperationalInsightsSavedSearch”</span><span class="sxs-lookup"><span data-stu-id="a52f3-404">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a52f3-405">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a52f3-405">Az.RecoveryServices</span></span>
* <span data-ttu-id="a52f3-406">Azure Backup har fått stöd för att hämta MAB-objekt.</span><span class="sxs-lookup"><span data-stu-id="a52f3-406">Azure Backup added support for fetching MAB items.</span></span>
* <span data-ttu-id="a52f3-407">Azure Site Recovery stöder disktypen ”StandardSSD_LRS”</span><span class="sxs-lookup"><span data-stu-id="a52f3-407">Azure Site Recovery supports disk type 'StandardSSD_LRS'</span></span>

#### <a name="azresources"></a><span data-ttu-id="a52f3-408">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a52f3-408">Az.Resources</span></span>
* <span data-ttu-id="a52f3-409">”UsageLocation”, ”GivenName”, ”Surname”, ”AccountEnabled”, ”MailNickname”, ”Mail” på ”PSADUser” lades till [#10526] [#10497]</span><span class="sxs-lookup"><span data-stu-id="a52f3-409">Added 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' on 'PSADUser' [#10526] [#10497]</span></span>
* <span data-ttu-id="a52f3-410">Problem med att ”-Mail” inte fungerar på ”Get-AzADUser” har åtgärdats [#11981]</span><span class="sxs-lookup"><span data-stu-id="a52f3-410">Fixed issue that '-Mail' doesn't work on 'Get-AzADUser' [#11981]</span></span>
* <span data-ttu-id="a52f3-411">Parametern ”-ExcludeChangeType” har lagts till i ”Get-AzDeploymentWhatIfResult” och ”Get-AzResourceGroupDeploymentWhatIfResult”</span><span class="sxs-lookup"><span data-stu-id="a52f3-411">Added '-ExcludeChangeType' parameter to 'Get-AzDeploymentWhatIfResult' and 'Get-AzResourceGroupDeploymentWhatIfResult'</span></span>
* <span data-ttu-id="a52f3-412">Parametern ”-WhatIfExcludeChangeType” har lagts till i ”New-AzDeployment” och ”New-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="a52f3-412">Added '-WhatIfExcludeChangeType' parameter to 'New-AzDeployment' and 'New-AzResourceGroupDeployment'</span></span>
* <span data-ttu-id="a52f3-413">Cmdletar för ”Test-Az\*Deployment” har uppdaterats för att visa bättre felmeddelanden</span><span class="sxs-lookup"><span data-stu-id="a52f3-413">Updated 'Test-Az\*Deployment' cmdlets to show better error messages</span></span>
* <span data-ttu-id="a52f3-414">Hjälpmeddelandet för parametern ”-Name” i distributionsskapande och What If-cmdletar</span><span class="sxs-lookup"><span data-stu-id="a52f3-414">Fixed help message for '-Name' parameter of deployment create and What-If cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="a52f3-415">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a52f3-415">Az.Sql</span></span>
* <span data-ttu-id="a52f3-416">Stöd för tjänsthuvudnamn har lagts till för administratörs-cmdlet för SQL Server Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="a52f3-416">Added support for service principal for Set SQL Server Azure Active Directory Admin cmdlet</span></span>
* <span data-ttu-id="a52f3-417">Synkroniseringsproblem i Data Classification-cmdletar har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="a52f3-417">Fixed sync issue in Data Classification cmdlets.</span></span>
* <span data-ttu-id="a52f3-418">Stöd för att söka efter användare via e-postadress på ”Set-AzSqlServerActiveDirectoryAdministrator” [#12192]</span><span class="sxs-lookup"><span data-stu-id="a52f3-418">Supported searching user by mail on 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a52f3-419">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a52f3-419">Az.Storage</span></span>
* <span data-ttu-id="a52f3-420">Skapa lagringskonto med RequireInfrastructureEncryption stöds</span><span class="sxs-lookup"><span data-stu-id="a52f3-420">Supported create Storage account with RequireInfrastructureEncryption</span></span>
    -  <span data-ttu-id="a52f3-421">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="a52f3-421">'New-AzStorageAccount'</span></span>
* <span data-ttu-id="a52f3-422">Logiken för inläsning av Azure.Core flyttades till Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a52f3-422">Moved the logic of loading Azure.Core to Az.Accounts</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a52f3-423">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a52f3-423">Az.Websites</span></span>
* <span data-ttu-id="a52f3-424">Skydd för att ta bort skapad webapp om återställningen misslyckades har lagts till i ”Restore-AzDeletedWebApp”</span><span class="sxs-lookup"><span data-stu-id="a52f3-424">Added safeguard to delete created webapp if restore failed in 'Restore-AzDeletedWebApp'</span></span>
* <span data-ttu-id="a52f3-425">”SourceWebApp.Location” har lagts till för ”New-AzWebApp” och ”New-AzWebAppSlot”</span><span class="sxs-lookup"><span data-stu-id="a52f3-425">Added 'SourceWebApp.Location' for 'New-AzWebApp' and 'New-AzWebAppSlot'</span></span>
* <span data-ttu-id="a52f3-426">Fel som förhindrade ändring av containerinställningar i ”Set-AzWebApp” och ”Set-AzWebAppSlot” har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="a52f3-426">Fixed bug that prevented changing Container settings in 'Set-AzWebApp' and 'Set-AzWebAppSlot'</span></span>
* <span data-ttu-id="a52f3-427">Ett fel för att hämta SiteConfig när -Name inte anges för Get-AzWebApp har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="a52f3-427">Fixed bug to get SiteConfig when -Name is not given for Get-AzWebApp</span></span>
* <span data-ttu-id="a52f3-428">Stöd har lagts till för att skapa ASP för Linux-appar</span><span class="sxs-lookup"><span data-stu-id="a52f3-428">Added a support to create ASP for Linux Apps</span></span>
* <span data-ttu-id="a52f3-429">Undantag har lagts till för kloning över resursgrupper</span><span class="sxs-lookup"><span data-stu-id="a52f3-429">Added exceptions for clone across resource groups</span></span>

## <a name="420---june-2020"></a><span data-ttu-id="a52f3-430">4.2.0 – juni 2020</span><span class="sxs-lookup"><span data-stu-id="a52f3-430">4.2.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a52f3-431">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a52f3-431">Az.Accounts</span></span>
* <span data-ttu-id="a52f3-432">Åtgärdade ett problem som kan få Az att hoppa över loggar i Azure Automation- eller PowerShell-jobb [#11492]</span><span class="sxs-lookup"><span data-stu-id="a52f3-432">Fixed an issue that may cause Az to skip logs in Azure Automation or PowerShell jobs [#11492]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="a52f3-433">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a52f3-433">Az.AnalysisServices</span></span>
* <span data-ttu-id="a52f3-434">Uppdaterad sammansättningsversion för dataplan-cmdletar</span><span class="sxs-lookup"><span data-stu-id="a52f3-434">Updated assembly version of data plane cmdlets</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="a52f3-435">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a52f3-435">Az.ApiManagement</span></span>
* <span data-ttu-id="a52f3-436">Uppdaterad sammansättningsversion för cmdletar för tjänsthantering</span><span class="sxs-lookup"><span data-stu-id="a52f3-436">Updated assembly version of service management cmdlets</span></span>

#### <a name="azbilling"></a><span data-ttu-id="a52f3-437">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="a52f3-437">Az.Billing</span></span>
* <span data-ttu-id="a52f3-438">Uppdaterad sammansättningsversion för förbrukningscmdletar</span><span class="sxs-lookup"><span data-stu-id="a52f3-438">Updated assembly version of consumption cmdlets</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="a52f3-439">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a52f3-439">Az.CognitiveServices</span></span>
* <span data-ttu-id="a52f3-440">Stöd för PrivateEndpoint- och PublicNetworkAccess-kontroll.</span><span class="sxs-lookup"><span data-stu-id="a52f3-440">Support PrivateEndpoint and PublicNetworkAccess control.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="a52f3-441">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a52f3-441">Az.DataFactory</span></span>
* <span data-ttu-id="a52f3-442">Uppdaterad sammansättningsversion för datafabrik V2-cmdletar</span><span class="sxs-lookup"><span data-stu-id="a52f3-442">Updated assembly version of data factory V2 cmdlets</span></span>

#### <a name="azdatashare"></a><span data-ttu-id="a52f3-443">Az.DataShare</span><span class="sxs-lookup"><span data-stu-id="a52f3-443">Az.DataShare</span></span>
* <span data-ttu-id="a52f3-444">Allmän tillgänglighet för modulen ”Az.DataShare”</span><span class="sxs-lookup"><span data-stu-id="a52f3-444">General availability of ''Az.DataShare'' module</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="a52f3-445">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="a52f3-445">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="a52f3-446">Allmän tillgänglighet för modulen ”Az.DesktopVirtualization”</span><span class="sxs-lookup"><span data-stu-id="a52f3-446">General availability of ''Az.DesktopVirtualization'' module</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="a52f3-447">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a52f3-447">Az.OperationalInsights</span></span>
* <span data-ttu-id="a52f3-448">Uppgraderad SDK till 0.21.0</span><span class="sxs-lookup"><span data-stu-id="a52f3-448">Upgraded SDK to 0.21.0</span></span>
* <span data-ttu-id="a52f3-449">Lade till valfria parametrar till</span><span class="sxs-lookup"><span data-stu-id="a52f3-449">Added optional parameters to</span></span> 
    - <span data-ttu-id="a52f3-450">”New-AzOperationalInsightsSavedSearch”</span><span class="sxs-lookup"><span data-stu-id="a52f3-450">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="a52f3-451">”Set-AzOperationalInsightsSavedSearch”</span><span class="sxs-lookup"><span data-stu-id="a52f3-451">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="a52f3-452">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a52f3-452">Az.PolicyInsights</span></span>
* <span data-ttu-id="a52f3-453">Korrigerade exempel 3 för ”Start-AzPolicyComplianceScan”</span><span class="sxs-lookup"><span data-stu-id="a52f3-453">Corrected example 3 for 'Start-AzPolicyComplianceScan'</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="a52f3-454">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="a52f3-454">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="a52f3-455">Uppdaterad sammansättningsversion för PowerBI-cmdletar</span><span class="sxs-lookup"><span data-stu-id="a52f3-455">Updated assembly version of PowerBI cmdlets</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="a52f3-456">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="a52f3-456">Az.PrivateDns</span></span>
* <span data-ttu-id="a52f3-457">Korrigerade formatering av utförlig utdatasträng för Remove-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="a52f3-457">Corrected verbose output string formatting for Remove-AzPrivateDnsRecordSet</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a52f3-458">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a52f3-458">Az.RecoveryServices</span></span>
* <span data-ttu-id="a52f3-459">Azure Site Recovery-stöd för att skapa en återställningsplan för replikering mellan zoner från xml-indata.</span><span class="sxs-lookup"><span data-stu-id="a52f3-459">Azure Site Recovery support for creating recovery plan for zone to zone replication from xml input.</span></span>
* <span data-ttu-id="a52f3-460">Uppdaterad sammansättningsversion för cmdletar för SiteRecovery och Backup</span><span class="sxs-lookup"><span data-stu-id="a52f3-460">Updated assembly version of SiteRecovery and Backup cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="a52f3-461">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a52f3-461">Az.Resources</span></span>
* <span data-ttu-id="a52f3-462">Lade till slutparameter för cmdletarna Get-AzDeploymentScriptLog och Save-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="a52f3-462">Added Tail parameter to Get-AzDeploymentScriptLog and Save-AzDeploymentScriptLog cmdlets</span></span>
* <span data-ttu-id="a52f3-463">Formaterad utdataegenskap så att den kan visas i cmdlet-utdata för Get-AzDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="a52f3-463">Formatted Output property and show it on the Get-AzDeploymentScript cmdlet output</span></span>
* <span data-ttu-id="a52f3-464">Bytte namn på parametern -DeploymentScriptInputObject till -DeploymentScriptObject</span><span class="sxs-lookup"><span data-stu-id="a52f3-464">Renamed -DeploymentScriptInputObject parameter to -DeploymentScriptObject</span></span>
* <span data-ttu-id="a52f3-465">Åtgärdade saknade fil/målnamn i cmdlet-meddelanden.</span><span class="sxs-lookup"><span data-stu-id="a52f3-465">Fixed missing file/target name in cmdlet messages.</span></span>
* <span data-ttu-id="a52f3-466">Uppdaterad sammansättningsversion för cmdletar för resurshanterare och taggar</span><span class="sxs-lookup"><span data-stu-id="a52f3-466">Updated assembly version of resource manager and tags cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="a52f3-467">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a52f3-467">Az.Sql</span></span>
* <span data-ttu-id="a52f3-468">Lade till UsePrivateLinkConnection till ”New-AzSqlSyncGroup”, ”Update-AzSqlSyncGroup”, ”New-AzSqlSyncMember” och ”Update-AzSqlSyncMember”</span><span class="sxs-lookup"><span data-stu-id="a52f3-468">Added UsePrivateLinkConnection to 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="a52f3-469">Lade till SyncMemberAzureDatabaseResourceId till ”New-AzSqlSyncMember” and ”Update-AzSqlSyncMember”</span><span class="sxs-lookup"><span data-stu-id="a52f3-469">Added SyncMemberAzureDatabaseResourceId to 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="a52f3-470">Lade till stöd för att söka efter gästanvändare för att ange administratörs-cmdlet för SQL Server Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="a52f3-470">Added Guest user lookup support to Set SQL Server Azure Active Directory Admin cmdlet</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a52f3-471">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a52f3-471">Az.Storage</span></span>
* <span data-ttu-id="a52f3-472">Uppdaterad sammansättningsversion för dataplan-cmdletar</span><span class="sxs-lookup"><span data-stu-id="a52f3-472">Updated assembly version of data plane cmdlets</span></span>

## <a name="410---may-2020"></a><span data-ttu-id="a52f3-473">4.1.0 – maj 2020</span><span class="sxs-lookup"><span data-stu-id="a52f3-473">4.1.0 - May 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="a52f3-474">Höjdpunkter sedan den senaste uppdateringen</span><span class="sxs-lookup"><span data-stu-id="a52f3-474">Highlights since the last release</span></span>
* <span data-ttu-id="a52f3-475">PowerShell-versioner som stöds: Windows PowerShell 5.1, PowerShell Core 6.2.4+ och PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="a52f3-475">Supported PowerShell versions: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>
* <span data-ttu-id="a52f3-476">Allmän tillgänglighet för Az.Functions</span><span class="sxs-lookup"><span data-stu-id="a52f3-476">General availability of Az.Functions</span></span> 
* <span data-ttu-id="a52f3-477">Nya stora uppdateringar har gjorts för Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources och Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a52f3-477">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources, and Az.Storage have major release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="a52f3-478">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a52f3-478">Az.Accounts</span></span>
* <span data-ttu-id="a52f3-479">”Add-AzEnvironment” och ”Set-AzEnvironment” har uppdaterats med stöd för parametrarna ”AzureSynapseAnalyticsEndpointResourceId” och ”AzureSynapseAnalyticsEndpointSuffix”</span><span class="sxs-lookup"><span data-stu-id="a52f3-479">Updated 'Add-AzEnvironment' and 'Set-AzEnvironment' to accept parameters 'AzureSynapseAnalyticsEndpointResourceId' and 'AzureSynapseAnalyticsEndpointSuffix'</span></span>
* <span data-ttu-id="a52f3-480">Azure.Core-relaterade sammansättningar har lagts till i Az.Accounts; PowerShell-plattformar som stöds är Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span><span class="sxs-lookup"><span data-stu-id="a52f3-480">Added Azure.Core related assemblies into Az.Accounts, supported PowerShell platforms include Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span></span>

#### <a name="azaks"></a><span data-ttu-id="a52f3-481">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="a52f3-481">Az.Aks</span></span>
* <span data-ttu-id="a52f3-482">API-versionen har uppgraderats till 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="a52f3-482">Upgraded API Version to 2019-10-01</span></span>
* <span data-ttu-id="a52f3-483">Stöds för att skapa AKS med hjälp av Windows-container</span><span class="sxs-lookup"><span data-stu-id="a52f3-483">Supported to create AKS using Windows container</span></span>
* <span data-ttu-id="a52f3-484">Nya cmdletar är tillgängliga: ”New-AzAksNodePool”, ”Update-AzAksNodePool”, ”Remove-AzAksNodePool”,        ”Get-AzAksNodePool”, ”Install-AzAksKubectl”, ”Get-AzAksVersion”</span><span class="sxs-lookup"><span data-stu-id="a52f3-484">Provided new cmdlets: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="a52f3-485">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a52f3-485">Az.ApiManagement</span></span>
* <span data-ttu-id="a52f3-486">Parametrarna ”New-AzApiManagement” och ”Set-AzApiManagement”: [-AssignIdentity] har bytt namn till [-SystemAssignedIdentity]</span><span class="sxs-lookup"><span data-stu-id="a52f3-486">'New-AzApiManagement' and 'Set-AzApiManagement': [-AssignIdentity] parameter renamed as [-SystemAssignedIdentity]</span></span>
* <span data-ttu-id="a52f3-487">”New-AzApiManagement” och ”Set-AzApiManagement”: En ny parameter har lagts till: [-UserAssignedIdentity <String[]>]</span><span class="sxs-lookup"><span data-stu-id="a52f3-487">'New-AzApiManagement' and 'Set-AzApiManagement': New parameter added: [-UserAssignedIdentity <String[]>]</span></span>
* <span data-ttu-id="a52f3-488">”Get-AzApiManagementProperty” har bytt namn till ”Get-AzApiManagementNamedValue”.</span><span class="sxs-lookup"><span data-stu-id="a52f3-488">'Get-AzApiManagementProperty': renamed as 'Get-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="a52f3-489">PropertyId-parametern har bytt namn till NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="a52f3-489">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="a52f3-490">”New-AzApiManagementProperty” har bytt namn till ”New-AzApiManagementNamedValue”.</span><span class="sxs-lookup"><span data-stu-id="a52f3-490">'New-AzApiManagementProperty': renamed as 'New-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="a52f3-491">PropertyId-parametern har bytt namn till NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="a52f3-491">PropertyId parameter renamed as NamedValueId.</span></span> 
* <span data-ttu-id="a52f3-492">”Set-AzApiManagementProperty” har bytt namn till ”Set-AzApiManagementNamedValue”.</span><span class="sxs-lookup"><span data-stu-id="a52f3-492">'Set-AzApiManagementProperty': renamed as 'Set-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="a52f3-493">PropertyId-parametern har bytt namn till NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="a52f3-493">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="a52f3-494">”Remove-AzApiManagementProperty” har bytt namn till ”Remove-AzApiManagementNamedValue”.</span><span class="sxs-lookup"><span data-stu-id="a52f3-494">'Remove-AzApiManagementProperty': renamed as 'Remove-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="a52f3-495">PropertyId-parametern har bytt namn till NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="a52f3-495">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="a52f3-496">Den nya cmdleten Get-AzApiManagementAuthorizationServerClientSecret gör att ”Get-AzApiManagementAuthorizationServer” inte längre returnerar klienthemligheter.</span><span class="sxs-lookup"><span data-stu-id="a52f3-496">Added new 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet and 'Get-AzApiManagementAuthorizationServer' will not return client secret anymore.</span></span>
* <span data-ttu-id="a52f3-497">Den nya cmdleten ”Get-AzApiManagementNamedValueSecretValue” gör att ”Get-AzApiManagementNamedValue” inte returnerar värdet för en hemlighet.</span><span class="sxs-lookup"><span data-stu-id="a52f3-497">Added new 'Get-AzApiManagementNamedValueSecretValue' cmdlet and 'Get-AzApiManagementNamedValue' will not return secret value.</span></span>
* <span data-ttu-id="a52f3-498">Den nya cmdleten ”Get-AzApiManagementOpenIdConnectProviderClientSecret” gör att ”Get-AzApiManagementOpenIdConnectProvider” inte längre returnerar klienthemligheter.</span><span class="sxs-lookup"><span data-stu-id="a52f3-498">Added new 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet and 'Get-AzApiManagementOpenIdConnectProvider' will not return client secret anymore.</span></span>
* <span data-ttu-id="a52f3-499">Den nya cmdleten ”Get-AzApiManagementSubscriptionKey” gör att ”Get-AzApiManagementSubscription” inte längre returnerar prenumerationsnycklar.</span><span class="sxs-lookup"><span data-stu-id="a52f3-499">Added new 'Get-AzApiManagementSubscriptionKey' cmdlet and 'Get-AzApiManagementSubscription' will not return subscription keys anymore.</span></span>
* <span data-ttu-id="a52f3-500">Den nya cmdleten ”Get-AzApiManagementTenantAccessSecret” gör att ”Get-AzApiManagementTenantAccess” inte längre returnerar nycklar.</span><span class="sxs-lookup"><span data-stu-id="a52f3-500">Added new 'Get-AzApiManagementTenantAccessSecret' cmdlet and 'Get-AzApiManagementTenantAccess' will not return keys anymore.</span></span>
* <span data-ttu-id="a52f3-501">Den nya cmdleten ”Get-AzApiManagementTenantGitAccessSecret” gör att ”Get-AzApiManagementTenantGitAccess” inte längre returnerar nycklar.</span><span class="sxs-lookup"><span data-stu-id="a52f3-501">Added new 'Get-AzApiManagementTenantGitAccessSecret' cmdlet and 'Get-AzApiManagementTenantGitAccess' will not return keys anymore.</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="a52f3-502">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="a52f3-502">Az.ApplicationInsights</span></span>
* <span data-ttu-id="a52f3-503">Tillagda parametrar: ”RetentionInDays” ”PublicNetworkAccessForIngestion” ”PublicNetworkAccessForQuery” för ”New-AzApplicationInsights”</span><span class="sxs-lookup"><span data-stu-id="a52f3-503">Added Parameters: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span></span>
* <span data-ttu-id="a52f3-504">Cmdleten ”Update-AzApplicationInsights” har skapats</span><span class="sxs-lookup"><span data-stu-id="a52f3-504">Created cmdlet 'Update-AzApplicationInsights'</span></span>
* <span data-ttu-id="a52f3-505">Cmdletar har skapats för länkat lagringskonto</span><span class="sxs-lookup"><span data-stu-id="a52f3-505">Created cmdlets for Linked Storage Account</span></span>

#### <a name="azbatch"></a><span data-ttu-id="a52f3-506">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="a52f3-506">Az.Batch</span></span>
* <span data-ttu-id="a52f3-507">Az.Batch har uppdaterats att använda ”Microsoft.Azure.Batch” SDK version 13.0.0 och ”Microsoft.Azure.Management.Batch” SDK version 9.0.0.</span><span class="sxs-lookup"><span data-stu-id="a52f3-507">Updated Az.Batch to use 'Microsoft.Azure.Batch' SDK version 13.0.0 and 'Microsoft.Azure.Management.Batch' SDK version 9.0.0.</span></span>
* <span data-ttu-id="a52f3-508">Nu kan du välja vilken typ av certifikat du lägger till genom att använda den nya parametern ”-CertificateKind” med ”New-AzBatchCertificate”.</span><span class="sxs-lookup"><span data-stu-id="a52f3-508">Added the ability to select the kind of certificate being added using the new '-CertificateKind' parameter to 'New-AzBatchCertificate'.</span></span>
* <span data-ttu-id="a52f3-509">Egenskapen ”ApplicationPackages” har tagits bort från ”PSApplication”, som tidigare alltid var ''.</span><span class="sxs-lookup"><span data-stu-id="a52f3-509">Removed 'ApplicationPackages' property from 'PSApplication' which was previously always ''.</span></span>
  - <span data-ttu-id="a52f3-510">Specifika paket i ett program kan nu hämtas med hjälp av ”Get-AzBatchApplicationPackage”.</span><span class="sxs-lookup"><span data-stu-id="a52f3-510">The specific packages inside of an application now can be retrieved using 'Get-AzBatchApplicationPackage'.</span></span> <span data-ttu-id="a52f3-511">Ett exempel: ”Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication”.</span><span class="sxs-lookup"><span data-stu-id="a52f3-511">For example: 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span></span>
* <span data-ttu-id="a52f3-512">Nu när du skapar en pool med hjälp av ”New-AzBatchPool” kan egenskapen ”VirtualMachineImageId” för ”PSImageReference” endast referera till en Shared Image Gallery-avbildning.</span><span class="sxs-lookup"><span data-stu-id="a52f3-512">When creating a pool using 'New-AzBatchPool', the 'VirtualMachineImageId' property of 'PSImageReference' can now only refer to a Shared Image Gallery image.</span></span>
* <span data-ttu-id="a52f3-513">När du skapar en pool med hjälp av ”New-AzBatchPool” kan poolen etableras utan en offentlig IP-adress med hjälp av den nya egenskapen ”PublicIPAddressConfiguration” för ”PSNetworkConfiguration”.</span><span class="sxs-lookup"><span data-stu-id="a52f3-513">When creating a pool using 'New-AzBatchPool', the pool can be provisioned without a public IP using the new 'PublicIPAddressConfiguration' property of 'PSNetworkConfiguration'.</span></span>
  - <span data-ttu-id="a52f3-514">Egenskapen ”PublicIPs” för ”PSNetworkConfiguration” har också flyttats till ”PSPublicIPAddressConfiguration”.</span><span class="sxs-lookup"><span data-stu-id="a52f3-514">The 'PublicIPs' property of 'PSNetworkConfiguration' has moved in to 'PSPublicIPAddressConfiguration' as well.</span></span> <span data-ttu-id="a52f3-515">Den här egenskapen kan bara anges om ”IPAddressProvisioningType” är ”UserManaged”.</span><span class="sxs-lookup"><span data-stu-id="a52f3-515">This property can only be specified if 'IPAddressProvisioningType' is 'UserManaged'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a52f3-516">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a52f3-516">Az.Compute</span></span>
* <span data-ttu-id="a52f3-517">Parametern HostId har lagts till för cmdleten ”Update-AzVM”t</span><span class="sxs-lookup"><span data-stu-id="a52f3-517">Added HostId parameter to 'Update-AzVM' cmdlet</span></span>
* <span data-ttu-id="a52f3-518">Hjälpdokumenten har uppdaterats för cmdletarna ”New-AzVMConfig”, ”New-AzVmssConfig”, ”Update-AzVmss”, ”Set-AzVMOperatingSystem” och ”Set-AzVmssOsProfile”.</span><span class="sxs-lookup"><span data-stu-id="a52f3-518">Updated Help documents for 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' and 'Set-AzVmssOsProfile' cmdlets.</span></span>
* <span data-ttu-id="a52f3-519">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="a52f3-519">Breaking changes</span></span>
    - <span data-ttu-id="a52f3-520">Parametern FilterExpression tas bort från cmdleten ”Get-AzVMImage”.</span><span class="sxs-lookup"><span data-stu-id="a52f3-520">FilterExpression parameter is removed from 'Get-AzVMImage' cmdlet.</span></span>
    - <span data-ttu-id="a52f3-521">Parametern AssignIdentity tas bort från cmdletarna ”New-AzVmssConfig”, ”New-AzVMConfig” och ”Update-AzVM”.</span><span class="sxs-lookup"><span data-stu-id="a52f3-521">AssignIdentity parameter is removed from 'New-AzVmssConfig', 'New-AzVMConfig' and 'Update-AzVM' cmdlets.</span></span>
    - <span data-ttu-id="a52f3-522">AutomaticRepairMaxInstanceRepairsPercent tas bort från cmdletarna ”New-AzVmssConfig” och ”Update-AzVmss”.</span><span class="sxs-lookup"><span data-stu-id="a52f3-522">AutomaticRepairMaxInstanceRepairsPercent is removed from 'New-AzVmssConfig' and 'Update-AzVmss' cmdlets.</span></span>
    - <span data-ttu-id="a52f3-523">Egenskaperna AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus och VirtualMachineScaleSetsColocationStatus tas bort från ProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="a52f3-523">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus and VirtualMachineScaleSetsColocationStatus properties are removed from ProximityPlacementGroup.</span></span>
    - <span data-ttu-id="a52f3-524">Egenskapen MaxInstanceRepairsPercent tas bort från AutomaticRepairsPolicy.</span><span class="sxs-lookup"><span data-stu-id="a52f3-524">MaxInstanceRepairsPercent property is removed from AutomaticRepairsPolicy.</span></span>
    - <span data-ttu-id="a52f3-525">Typerna AvailabilitySets, VirtualMachines och VirtualMachineScaleSets ändras från IList<SubResource> till IList<SubResourceWithColocationStatus>.</span><span class="sxs-lookup"><span data-stu-id="a52f3-525">The types of AvailabilitySets, VirtualMachines and VirtualMachineScaleSets are changed from IList<SubResource> to IList<SubResourceWithColocationStatus>.</span></span>
* <span data-ttu-id="a52f3-526">Beskrivningen för cmdleten ”Get-AzVM” har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="a52f3-526">Description for 'Get-AzVM' cmdlet has been updated to better describe it.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="a52f3-527">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a52f3-527">Az.DataFactory</span></span>
* <span data-ttu-id="a52f3-528">CRUD-stöd för egenskaper för dataflödeskörning  i hanterad IR.</span><span class="sxs-lookup"><span data-stu-id="a52f3-528">Supported CRUD of data flow runtime properties in Managed IR.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="a52f3-529">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="a52f3-529">Az.FrontDoor</span></span>
* <span data-ttu-id="a52f3-530">Nya cmdletar har lagts till för att skapa, uppdatera, hämta och ta bort (CRUD) Front Door-regelmotorobjekt</span><span class="sxs-lookup"><span data-stu-id="a52f3-530">Added new cmdlets for creation, update, retreival, and deletion of Front Door Rules Engine object</span></span>
* <span data-ttu-id="a52f3-531">Hjälp-cmdletar har lagts till för konstruktion av Front Door-regelmotorobjekt</span><span class="sxs-lookup"><span data-stu-id="a52f3-531">Added helper cmdlets for construction of Front Door Rules Engine object</span></span>
* <span data-ttu-id="a52f3-532">Regelmotorreferens har lagts till för Front Door-hanteringsregelobjekt.</span><span class="sxs-lookup"><span data-stu-id="a52f3-532">Added Rules Engine reference to Front Door Routing Rule object.</span></span>
* <span data-ttu-id="a52f3-533">Parametrar för Private Link har lagts till för Front Door-serverdelsobjekt</span><span class="sxs-lookup"><span data-stu-id="a52f3-533">Added Private Link parameters to Front Door Backend object</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="a52f3-534">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="a52f3-534">Az.Functions</span></span>
* <span data-ttu-id="a52f3-535">Allmän tillgänglighet för ”Az.Functions”-modulen</span><span class="sxs-lookup"><span data-stu-id="a52f3-535">General availability of ''Az.Functions'' module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="a52f3-536">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a52f3-536">Az.HDInsight</span></span>
* <span data-ttu-id="a52f3-537">Stöd för diskkryptering med kundhanterad nyckel.</span><span class="sxs-lookup"><span data-stu-id="a52f3-537">Supported Customer-managed key disk encryption.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="a52f3-538">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="a52f3-538">Az.HealthcareApis</span></span>
* <span data-ttu-id="a52f3-539">Åtkomstprinciper använder inte längre det aktiva huvudkontot som standard</span><span class="sxs-lookup"><span data-stu-id="a52f3-539">Access policies are no longer defaulted to the current principal</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a52f3-540">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a52f3-540">Az.IotHub</span></span>
* <span data-ttu-id="a52f3-541">En cmdlet har lagts till som anropar en fråga i en IoT-hubb för att hämta information med ett SQL-liknande språk.</span><span class="sxs-lookup"><span data-stu-id="a52f3-541">Added cmdlet to invoke a query in an IoT hub to retrieve information using a SQL-like language.</span></span>
* <span data-ttu-id="a52f3-542">Problemet som gjorde att ”Add-AzIotHubDevice” inte skapade en Edge-aktiverad enhet utan underordnade enheter har åtgärdats [#11597]</span><span class="sxs-lookup"><span data-stu-id="a52f3-542">Fix issue that 'Add-AzIotHubDevice' fails to create Edge Enabled Device without child devices [#11597]</span></span>
* <span data-ttu-id="a52f3-543">En cmdlet har lagts till för att generera SAS-token för en Iot-hubb, enhet eller modul.</span><span class="sxs-lookup"><span data-stu-id="a52f3-543">Added cmdlet to generate SAS token for Iot Hub, device or module.</span></span>
* <span data-ttu-id="a52f3-544">En cmdlet har lagts till för att anropa en måttfråga om konfiguration.</span><span class="sxs-lookup"><span data-stu-id="a52f3-544">Added cmdlet to invoke configuration metrics query.</span></span>
* <span data-ttu-id="a52f3-545">Hantera automatisk distribution av IoT Edge i stor skala.</span><span class="sxs-lookup"><span data-stu-id="a52f3-545">Manage IoT Edge automatic deployment at scale.</span></span> <span data-ttu-id="a52f3-546">Nya cmdlet:ar är:</span><span class="sxs-lookup"><span data-stu-id="a52f3-546">New cmdlets are:</span></span>
    - <span data-ttu-id="a52f3-547">”Add-AzIotHubDeployment”</span><span class="sxs-lookup"><span data-stu-id="a52f3-547">'Add-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="a52f3-548">”Get-AzIotHubDeployment”</span><span class="sxs-lookup"><span data-stu-id="a52f3-548">'Get-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="a52f3-549">”Remove-AzIotHubDeployment”</span><span class="sxs-lookup"><span data-stu-id="a52f3-549">'Remove-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="a52f3-550">”Set-AzIotHubDeployment”</span><span class="sxs-lookup"><span data-stu-id="a52f3-550">'Set-AzIotHubDeployment'</span></span>
* <span data-ttu-id="a52f3-551">En cmdlet har lagts till för att anropa en måttfråga om IoT Edge-distribution.</span><span class="sxs-lookup"><span data-stu-id="a52f3-551">Added cmdlet to invoke an IoT Edge deployment metrics query.</span></span>
* <span data-ttu-id="a52f3-552">En cmdlet har lagts till för att tillämpa konfigurationsinnehåll på den angivna gränsenheten.</span><span class="sxs-lookup"><span data-stu-id="a52f3-552">Added cmdlet to apply the configuration content to the specified edge device.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a52f3-553">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a52f3-553">Az.KeyVault</span></span>
* <span data-ttu-id="a52f3-554">Två alias har tagits bort: ”New-AzKeyVaultCertificateAdministratorDetails” och ”New-AzKeyVaultCertificateOrganizationDetails”</span><span class="sxs-lookup"><span data-stu-id="a52f3-554">Removed two aliases: 'New-AzKeyVaultCertificateAdministratorDetails' and 'New-AzKeyVaultCertificateOrganizationDetails'</span></span>
* <span data-ttu-id="a52f3-555">Nu är mjuk borttagning aktiverat som standard när ett nyckelvalv skapas</span><span class="sxs-lookup"><span data-stu-id="a52f3-555">Enabled soft delete by default when creating a key vault</span></span>
* <span data-ttu-id="a52f3-556">Nätverksregler kan ställas in för att styra åtkomsten från särskilda nätverksplatser när du skapar ett nyckelvalv</span><span class="sxs-lookup"><span data-stu-id="a52f3-556">Network rules can be set to govern the accessibility from specific network locations when creating a key vault</span></span>
* <span data-ttu-id="a52f3-557">Stöd för BYOK (Bring Your Own Key) har lagts till</span><span class="sxs-lookup"><span data-stu-id="a52f3-557">Added support to bring your own key (BYOK)</span></span>
    - <span data-ttu-id="a52f3-558">”Add-AzKeyVaultKey” stöder generering av en KeyExchange-nyckel</span><span class="sxs-lookup"><span data-stu-id="a52f3-558">'Add-AzKeyVaultKey' supports generating a key exchange key</span></span>
    - <span data-ttu-id="a52f3-559">”Get-AzKeyVaultKey” stöder nedladdning av en offentlig nyckel i PEM-format</span><span class="sxs-lookup"><span data-stu-id="a52f3-559">'Get-AzKeyVaultKey' supports downloading a public key in PEM format</span></span>
* <span data-ttu-id="a52f3-560">”KeyOps”-delen av hjälpdokumentet för ”Add-AzKeyVaultKey” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="a52f3-560">Updated the 'KeyOps' part of the help document of 'Add-AzKeyVaultKey'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a52f3-561">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a52f3-561">Az.Monitor</span></span>
* <span data-ttu-id="a52f3-562">Bugg för ”Set-AzDiagnosticSettings” har åtgärdats; kvarhållningsprincipen tillämpas inte på alla kategorier [#11589]</span><span class="sxs-lookup"><span data-stu-id="a52f3-562">Fixed bug for 'Set-AzDiagnosticSettings', retention policy won't apply to all categories [#11589]</span></span>
* <span data-ttu-id="a52f3-563">Stöd för WebTest-tillgänglighetskriterier för måttavisering V2</span><span class="sxs-lookup"><span data-stu-id="a52f3-563">Supported WebTest availability criteria for metric alert V2</span></span>
    - <span data-ttu-id="a52f3-564">”New-AzMetricAlertRuleV2Criteria”: ett alternativ för att skapa tillgänglighetskriterier för webbtest har lagts till</span><span class="sxs-lookup"><span data-stu-id="a52f3-564">'New-AzMetricAlertRuleV2Criteria': an option to create webtest availability criteria was added</span></span>
    - <span data-ttu-id="a52f3-565">”Add-AzMetricAlertRuleV2”: stöd för de nya tillgänglighetskriterierna för webbtest</span><span class="sxs-lookup"><span data-stu-id="a52f3-565">'Add-AzMetricAlertRuleV2': supports the new webtest availability criteria</span></span>
* <span data-ttu-id="a52f3-566">Redundant definition har tagits bort för RetentionPolicy i PSLogProfile [#7608]</span><span class="sxs-lookup"><span data-stu-id="a52f3-566">Removed redundant definition for RetentionPolicy in PSLogProfile [#7608]</span></span>
* <span data-ttu-id="a52f3-567">Redundanta egenskaper som definierats i PSEventData har tagits bort [#11353]</span><span class="sxs-lookup"><span data-stu-id="a52f3-567">Removed redundant properties difined in PSEventData [#11353]</span></span>
* <span data-ttu-id="a52f3-568">”Get-AzLog” har bytt namn till ”Get-AzActivityLog”</span><span class="sxs-lookup"><span data-stu-id="a52f3-568">Renamed 'Get-AzLog' to 'Get-AzActivityLog'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a52f3-569">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a52f3-569">Az.Network</span></span>
* <span data-ttu-id="a52f3-570">Attribut för icke-bakåtkompatibel ändring har lagts till för att meddela att standardbeteendet för zoner kommer att ändras</span><span class="sxs-lookup"><span data-stu-id="a52f3-570">Added breaking change attribute to notify that Zone default behaviour will be changed</span></span>
    - <span data-ttu-id="a52f3-571">”New-AzPublicIpAddress”</span><span class="sxs-lookup"><span data-stu-id="a52f3-571">'New-AzPublicIpAddress'</span></span>
    - <span data-ttu-id="a52f3-572">”New-AzPublicIpPrefix”</span><span class="sxs-lookup"><span data-stu-id="a52f3-572">'New-AzPublicIpPrefix'</span></span>
    - <span data-ttu-id="a52f3-573">”New-AzLoadBalancerFrontendIpConfig”</span><span class="sxs-lookup"><span data-stu-id="a52f3-573">'New-AzLoadBalancerFrontendIpConfig'</span></span>
* <span data-ttu-id="a52f3-574">Stöd har lagts till för en ny resurs på den översta nivån, SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="a52f3-574">Added support for a new top level resource SecurityPartnerProvider</span></span>
    - <span data-ttu-id="a52f3-575">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="a52f3-575">New cmdlets added:</span></span>
        - <span data-ttu-id="a52f3-576">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="a52f3-576">New-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="a52f3-577">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="a52f3-577">Remove-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="a52f3-578">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="a52f3-578">Get-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="a52f3-579">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="a52f3-579">Set-AzSecurityPartnerProvider</span></span>
* <span data-ttu-id="a52f3-580">”RequiredZoneNames” har lagts till för ”PSPrivateLinkResource” och ”GroupId” för ”PSPrivateEndpointConnection”</span><span class="sxs-lookup"><span data-stu-id="a52f3-580">Added 'RequiredZoneNames' on 'PSPrivateLinkResource' and 'GroupId' on 'PSPrivateEndpointConnection'</span></span>
* <span data-ttu-id="a52f3-581">Fel parametertyp för SuccessThresholdRoundTripTimeMs-parametern för New-AzNetworkWatcherConnectionMonitorTestConfigurationObject har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="a52f3-581">Fixed incorrect type of SuccessThresholdRoundTripTimeMs parameter for New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>
* <span data-ttu-id="a52f3-582">VirtualWan-cmdletar har uppdaterats för att ange AllowVnetToVnetTraffic-argumentets standardvärde till True.</span><span class="sxs-lookup"><span data-stu-id="a52f3-582">Updated VirtualWan cmdlets to set default value of AllowVnetToVnetTraffic argument to True.</span></span>
    - <span data-ttu-id="a52f3-583">”New-AzVirtualWan”</span><span class="sxs-lookup"><span data-stu-id="a52f3-583">'New-AzVirtualWan'</span></span>
    - <span data-ttu-id="a52f3-584">”Update-AzVirtualWan”</span><span class="sxs-lookup"><span data-stu-id="a52f3-584">'Update-AzVirtualWan'</span></span>
* <span data-ttu-id="a52f3-585">Nya cmdletar har lagts till för att stödja DNS-zongrupp för privat slutpunkt</span><span class="sxs-lookup"><span data-stu-id="a52f3-585">Added new cmdlets to support DNS zone group for private endpoint</span></span>
    - <span data-ttu-id="a52f3-586">”New-AzPrivateDnsZoneConfig”</span><span class="sxs-lookup"><span data-stu-id="a52f3-586">'New-AzPrivateDnsZoneConfig'</span></span>
    - <span data-ttu-id="a52f3-587">”Get-AzPrivateDnsZoneGroup”</span><span class="sxs-lookup"><span data-stu-id="a52f3-587">'Get-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="a52f3-588">”New-AzPrivateDnsZoneGroup”</span><span class="sxs-lookup"><span data-stu-id="a52f3-588">'New-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="a52f3-589">”Set-AzPrivateDnsZoneGroup”</span><span class="sxs-lookup"><span data-stu-id="a52f3-589">'Set-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="a52f3-590">”Remove-AzPrivateDnsZoneGroup”</span><span class="sxs-lookup"><span data-stu-id="a52f3-590">'Remove-AzPrivateDnsZoneGroup'</span></span>
* <span data-ttu-id="a52f3-591">Parametrarna ”DNSEnableProxy”, ”DNSRequireProxyForNetworkRules” och ”DNSServers” har lagts till för ”AzureFirewall”</span><span class="sxs-lookup"><span data-stu-id="a52f3-591">Added 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' and 'DNSServers' parameters to 'AzureFirewall'</span></span>
* <span data-ttu-id="a52f3-592">Parametrarna ”EnableDnsProxy”, ”DnsProxyNotRequiredForNetworkRule” och ”DnsServer” har lagts till för ”AzureFirewall”</span><span class="sxs-lookup"><span data-stu-id="a52f3-592">Added 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' and 'DnsServer' parameters to 'AzureFirewall'</span></span>
    - <span data-ttu-id="a52f3-593">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="a52f3-593">Updated cmdlet:</span></span>
        - <span data-ttu-id="a52f3-594">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="a52f3-594">New-AzFirewall</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="a52f3-595">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a52f3-595">Az.OperationalInsights</span></span>
* <span data-ttu-id="a52f3-596">Äldre kod har uppdaterats för att tillämpa ny genererad SDK</span><span class="sxs-lookup"><span data-stu-id="a52f3-596">Updated legacy code to apply new generated SDK</span></span>
* <span data-ttu-id="a52f3-597">Cmdletar har tagits bort på grund av föråldrade API:er</span><span class="sxs-lookup"><span data-stu-id="a52f3-597">Deleted cmdlets due to deprecated APIs</span></span>
    - <span data-ttu-id="a52f3-598">”Get-AzOperationalInsightsSavedSearchResult” (alias ”Get-AzOperationalInsightsSavedSearchResults”)</span><span class="sxs-lookup"><span data-stu-id="a52f3-598">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span></span>
    - <span data-ttu-id="a52f3-599">”Get-AzOperationalInsightsSearchResult” (alias ”Get-AzOperationalInsightsSearchResults”)</span><span class="sxs-lookup"><span data-stu-id="a52f3-599">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span></span>
    - <span data-ttu-id="a52f3-600">”Get-AzOperationalInsightsLinkTarget” (alias ”Get-AzOperationalInsightsLinkTargets”)</span><span class="sxs-lookup"><span data-stu-id="a52f3-600">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span></span>
* <span data-ttu-id="a52f3-601">Parametrar har lagts till för ”Set-AzOperationalInsightsWorkspace” och ”New-AzOperationalInsightsWorkspace”</span><span class="sxs-lookup"><span data-stu-id="a52f3-601">Added parameters for 'Set-AzOperationalInsightsWorkspace' and 'New-AzOperationalInsightsWorkspace'</span></span>
* <span data-ttu-id="a52f3-602">Cmdletar har skapats för länkat lagringskonto</span><span class="sxs-lookup"><span data-stu-id="a52f3-602">Created cmdlets for Linked Stoarge Account</span></span>
* <span data-ttu-id="a52f3-603">Cmdletar har skapats för kluster och länkad tjänst</span><span class="sxs-lookup"><span data-stu-id="a52f3-603">Created cmdlets for Clusters and Linked Service</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a52f3-604">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a52f3-604">Az.RecoveryServices</span></span>
* <span data-ttu-id="a52f3-605">Azure Site Recovery: Stöd har lagts till för att skydda VM-närhetsplaceringsgrupper för Azure till Azure-provider.</span><span class="sxs-lookup"><span data-stu-id="a52f3-605">Azure Site Recovery added support for protecting proximity placement group virtual machines for Azure to Azure provider.</span></span>
* <span data-ttu-id="a52f3-606">Azure Site Recovery: Stöd har lagts till för replikering mellan zoner.</span><span class="sxs-lookup"><span data-stu-id="a52f3-606">Azure Site Recovery added support for zone to zone replication.</span></span>
* <span data-ttu-id="a52f3-607">Azure Backup: Stöd har lagts till för långsiktig kvarhållning för Azure FileShare-återställningspunkter.</span><span class="sxs-lookup"><span data-stu-id="a52f3-607">Azure Backup Added Long term retention support for Azure FileShare Recovery Points.</span></span>
* <span data-ttu-id="a52f3-608">Azure Backup: Egenskaper för diskexkludering har lagts till för cmdlet-utdata från ”Get-AzRecoveryServicesBackupItem”.</span><span class="sxs-lookup"><span data-stu-id="a52f3-608">Azure Backup Added disk exclusion properties to 'Get-AzRecoveryServicesBackupItem' cmdlet output.</span></span>
* <span data-ttu-id="a52f3-609">En privat slutpunkt har lagts till för filen med valvets autentiseringsuppgifter för Site Recovery-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="a52f3-609">Added private endpoint for Vault credential file for site recovery service.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a52f3-610">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a52f3-610">Az.Resources</span></span>
* <span data-ttu-id="a52f3-611">En varning har lagts till om visningsfördröjning när en ny rolldefinition skapas</span><span class="sxs-lookup"><span data-stu-id="a52f3-611">Added message warning about view delay when creating a new Role Definition</span></span>
* <span data-ttu-id="a52f3-612">Princip-cmdletar har ändrats för utmatning av starkt typifierade objekt</span><span class="sxs-lookup"><span data-stu-id="a52f3-612">Changed policy cmdlets to output strongly-typed objects</span></span>
* <span data-ttu-id="a52f3-613">Parametern ”-TenantLevel” har tagits bort för användning med ”Get-AzResourceLock” [#11335]</span><span class="sxs-lookup"><span data-stu-id="a52f3-613">Removed '-TenantLevel' parameter used for on the 'Get-AzResourceLock' cmdlet [#11335]</span></span>
* <span data-ttu-id="a52f3-614">”Remove-AzResourceGroup -Id ResourceId” har åtgärdats [#9882]</span><span class="sxs-lookup"><span data-stu-id="a52f3-614">Fixed 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span></span>
* <span data-ttu-id="a52f3-615">En ny cmdlet har lagts till för att hämta What-If-resultat för ARM-mallar i omfånget för resursgrupper: ”Get-AzDeploymentResourceGroupWhatIfResult”</span><span class="sxs-lookup"><span data-stu-id="a52f3-615">Added new cmdlet for getting ARM template What-If results at resource group scope: 'Get-AzDeploymentResourceGroupWhatIfResult'</span></span>
* <span data-ttu-id="a52f3-616">En ny cmdlet har lagts till för att hämta What-If-resultat för ARM-mallar i prenumerationsomfånget: ”Get-AzDeploymentWhatIfResult”</span><span class="sxs-lookup"><span data-stu-id="a52f3-616">Added new cmdlet for getting ARM template What-If results at subscription scope: 'Get-AzDeploymentWhatIfResult'</span></span>
   - <span data-ttu-id="a52f3-617">Alias: ”Get-AzSubscriptionDeploymentWhatIf”</span><span class="sxs-lookup"><span data-stu-id="a52f3-617">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span></span>
* <span data-ttu-id="a52f3-618">Parametrarna ”-WhatIf” och ”-Confirm” har åsidosatts för ”New-AzDeployment” och ”New-AzResourceGroupDeployment” för att använda What-If-resultat för ARM-mallar</span><span class="sxs-lookup"><span data-stu-id="a52f3-618">Overrode '-WhatIf' and '-Confirm' parameters for 'New-AzDeployment' and 'New-AzResourceGroupDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="a52f3-619">Ett utfasningsmeddelande har lagts till för parametern ”ApiVersion” i distributions-cmdletar</span><span class="sxs-lookup"><span data-stu-id="a52f3-619">Added deprecation message for 'ApiVersion' parameter in deployment cmdlets</span></span>
* <span data-ttu-id="a52f3-620">En funktion har lagts till för att visa förbättrade felmeddelanden för distributionsfel</span><span class="sxs-lookup"><span data-stu-id="a52f3-620">Added capability to show improved error messages for deployment failures</span></span>
* <span data-ttu-id="a52f3-621">CorrelationId-loggning har lagts till för distributionsfel</span><span class="sxs-lookup"><span data-stu-id="a52f3-621">Added correlationId logging for deployment failures</span></span>
* <span data-ttu-id="a52f3-622">Egenskapen ”error” har lagts till i utdata från distributionsskript</span><span class="sxs-lookup"><span data-stu-id="a52f3-622">Added 'error' property to the deployment script output</span></span>
* <span data-ttu-id="a52f3-623">Nuget Microsoft.Azure.Management.ResourceManager har uppdaterats till ”3.7.1-preview”</span><span class="sxs-lookup"><span data-stu-id="a52f3-623">Updated nuget Microsoft.Azure.Management.ResourceManager to '3.7.1-preview'</span></span>
* <span data-ttu-id="a52f3-624">Specifika testfall har tagits bort då egenskapen Error i DeploymentValidateResult har ändrats till lässkyddad från nuget 3.7.1-preview</span><span class="sxs-lookup"><span data-stu-id="a52f3-624">Removed specific test cases as Error property in DeploymentValidateResult has changed to readonly from nuget 3.7.1-preview</span></span>
* <span data-ttu-id="a52f3-625">GenericResourceExpanded har flyttats från SDK ResourceManager 3.7.1-preview</span><span class="sxs-lookup"><span data-stu-id="a52f3-625">Brought GenericResourceExpanded from SDK ResourceManager 3.7.1-preview</span></span>
* <span data-ttu-id="a52f3-626">Stöd för taggar har lagts till för alla Get-cmdletar för distribution, samt</span><span class="sxs-lookup"><span data-stu-id="a52f3-626">Added tag support for all Get cmdlets for deployment, as well as</span></span>
    - <span data-ttu-id="a52f3-627">”New-AzDeployment”</span><span class="sxs-lookup"><span data-stu-id="a52f3-627">'New-AzDeployment'</span></span>
    - <span data-ttu-id="a52f3-628">”New-AzManagementGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="a52f3-628">'New-AzManagementGroupDeployment'</span></span>
    - <span data-ttu-id="a52f3-629">”New-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="a52f3-629">'New-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="a52f3-630">”New-AzTenantDeployment”</span><span class="sxs-lookup"><span data-stu-id="a52f3-630">'New-AzTenantDeployment'</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a52f3-631">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a52f3-631">Az.ServiceFabric</span></span>
* <span data-ttu-id="a52f3-632">En bugg har åtgärdats som gjorde att --SecretIdentifier fick fel tumavtryck för certifikat när ett certifikat lades till</span><span class="sxs-lookup"><span data-stu-id="a52f3-632">Fixed bug in add certificate using --SecretIdentifier that was getting the wrong certificate thumbprint</span></span>

#### <a name="azsql"></a><span data-ttu-id="a52f3-633">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a52f3-633">Az.Sql</span></span>
* <span data-ttu-id="a52f3-634">Förbättrade prestanda för:</span><span class="sxs-lookup"><span data-stu-id="a52f3-634">Enhance performance of:</span></span>
    - <span data-ttu-id="a52f3-635">”Set-AzSqlDatabaseSensitivityClassification”</span><span class="sxs-lookup"><span data-stu-id="a52f3-635">'Set-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="a52f3-636">”Set-AzSqlInstanceDatabaseSensitivityClassification”</span><span class="sxs-lookup"><span data-stu-id="a52f3-636">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="a52f3-637">”Remove-AzSqlDatabaseSensitivityClassification”</span><span class="sxs-lookup"><span data-stu-id="a52f3-637">'Remove-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="a52f3-638">”Remove-AzSqlInstanceDatabaseSensitivityClassification”</span><span class="sxs-lookup"><span data-stu-id="a52f3-638">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="a52f3-639">”Enable-AzSqlDatabaseSensitivityRecommendation”</span><span class="sxs-lookup"><span data-stu-id="a52f3-639">'Enable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="a52f3-640">”Enable-AzSqlInstanceDatabaseSensitivityRecommendation”</span><span class="sxs-lookup"><span data-stu-id="a52f3-640">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="a52f3-641">”Disable-AzSqlDatabaseSensitivityRecommendation”</span><span class="sxs-lookup"><span data-stu-id="a52f3-641">'Disable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="a52f3-642">”Disable-AzSqlInstanceDatabaseSensitivityRecommendation”</span><span class="sxs-lookup"><span data-stu-id="a52f3-642">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
* <span data-ttu-id="a52f3-643">Validering på klientsidan har tagits bort för parametern ”RetentionDays” från cmdleten ”Set-AzSqlDatabaseBackupShortTermRetentionPolicy”</span><span class="sxs-lookup"><span data-stu-id="a52f3-643">Removed client-side validation of 'RetentionDays' parameter from cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span>
* <span data-ttu-id="a52f3-644">Granskning av ett lagringskonto i Vnet; en bugg har åtgärdats som orsakade fel när en Storage Blob Data-deltagarroll skapades.</span><span class="sxs-lookup"><span data-stu-id="a52f3-644">Auditing to a storage account in Vnet, fixing a bug when creating a Storage Blob Data Contributor role.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a52f3-645">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a52f3-645">Az.Storage</span></span>
* <span data-ttu-id="a52f3-646">”-AsJob” har lagts till för att hämta/lista konto med cmdleten ”Get-AzStorageAccount”</span><span class="sxs-lookup"><span data-stu-id="a52f3-646">Added '-AsJob' to get/list account cmdlet 'Get-AzStorageAccount'</span></span>
* <span data-ttu-id="a52f3-647">Gör KeyVersion valfri när lagringskontot uppdateras med KeyvaultEncryption, för att ge stöd för automatisk nyckelrotation</span><span class="sxs-lookup"><span data-stu-id="a52f3-647">Make KeyVersion to optional when update Storage account with KeyvaultEncryption, to support key auto-rotation</span></span>
    - <span data-ttu-id="a52f3-648">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="a52f3-648">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="a52f3-649">Problemet med borttagning av Azure-filkatalog i pipeline har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="a52f3-649">Fixed remove Azure File Directory fail with pipeline</span></span>
    - <span data-ttu-id="a52f3-650">”Remove-AzStorageDirectory”</span><span class="sxs-lookup"><span data-stu-id="a52f3-650">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="a52f3-651">Åtgärdat [#9880]: Definitionen av DefaultAction-värdet för NetWorkRule har ändrats för konsekvens med Swagger.</span><span class="sxs-lookup"><span data-stu-id="a52f3-651">Fixed [#9880]: Change NetWorkRule DefaultAction value defination to align with swagger.</span></span>
    - <span data-ttu-id="a52f3-652">”Update-AzStorageAccountNetworkRuleSet”</span><span class="sxs-lookup"><span data-stu-id="a52f3-652">'Update-AzStorageAccountNetworkRuleSet'</span></span>
    - <span data-ttu-id="a52f3-653">”Get-AzStorageAccountNetworkRuleSet”</span><span class="sxs-lookup"><span data-stu-id="a52f3-653">'Get-AzStorageAccountNetworkRuleSet'</span></span>
* <span data-ttu-id="a52f3-654">Åtgärdat [#11624]: Hoppa över dubblettregler när NetworkRules läggs till, för att undvika serverfel</span><span class="sxs-lookup"><span data-stu-id="a52f3-654">Fixed [#11624]: Skip duplicated rules when add NetworkRules, to avoid server failure</span></span>
    - <span data-ttu-id="a52f3-655">”Add-AzStorageAccountNetworkRule”</span><span class="sxs-lookup"><span data-stu-id="a52f3-655">'Add-AzStorageAccountNetworkRule'</span></span>
* <span data-ttu-id="a52f3-656">Microsoft.Azure.Cosmos.Table SDK har uppgraderats till 1.0.7</span><span class="sxs-lookup"><span data-stu-id="a52f3-656">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.7</span></span>
* <span data-ttu-id="a52f3-657">Ett varningsmeddelande har lagts till för att påminna användaren om att lista igen med ContinuationToken när endast delobjekt returneras i listan med DataLake Gen2-objekt,</span><span class="sxs-lookup"><span data-stu-id="a52f3-657">Added a warning message to remind user to list again with ContinuationToken when only part items are returned in list DataLake Gen2 Items,</span></span>
    - <span data-ttu-id="a52f3-658">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="a52f3-658">'Get-AzDataLakeGen2ChildItem'</span></span>
* <span data-ttu-id="a52f3-659">Stöd för att skapa eller uppdatera lagringskonto med Azure Files Active Directory Domain Service-autentisering</span><span class="sxs-lookup"><span data-stu-id="a52f3-659">Supported to create or update Storage account with Azure Files Active Directory Domain Service Authentication</span></span>
    -  <span data-ttu-id="a52f3-660">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="a52f3-660">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="a52f3-661">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="a52f3-661">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="a52f3-662">Stöd för nya eller listade Kerberos-nycklar för lagringskontot</span><span class="sxs-lookup"><span data-stu-id="a52f3-662">Supported to new or list Kerberos keys of Storage account</span></span>
    -  <span data-ttu-id="a52f3-663">”New-AzStorageAccountKey”</span><span class="sxs-lookup"><span data-stu-id="a52f3-663">'New-AzStorageAccountKey'</span></span>
    -  <span data-ttu-id="a52f3-664">”Get-AzStorageAccountKey”</span><span class="sxs-lookup"><span data-stu-id="a52f3-664">'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="a52f3-665">Stöd för redundans med lagringskonto</span><span class="sxs-lookup"><span data-stu-id="a52f3-665">Supported failover Storage account</span></span>
    - <span data-ttu-id="a52f3-666">”Invoke-AzStorageAccountFailover”</span><span class="sxs-lookup"><span data-stu-id="a52f3-666">'Invoke-AzStorageAccountFailover'</span></span>
* <span data-ttu-id="a52f3-667">Hjälpen för ”Get-AzStorageBlobCopyState” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="a52f3-667">Updated help of 'Get-AzStorageBlobCopyState'</span></span>
* <span data-ttu-id="a52f3-668">Hjälpen för ”Get-AzStorageFileCopyState” och ”Start-AzStorageBlobCopy” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="a52f3-668">Updated help of 'Get-AzStorageFileCopyState' and 'Start-AzStorageBlobCopy'</span></span>
* <span data-ttu-id="a52f3-669">Lagringsklientbibliotek v12 har integrerats med Queue- och File-cmdletar</span><span class="sxs-lookup"><span data-stu-id="a52f3-669">Integrated Storage client library v12 to Queue and File cmdlets</span></span>
* <span data-ttu-id="a52f3-670">Utdatatypen har ändrats från CloudFile till AzureStorageFile; ursprungliga utdata blir en underordnad egenskap i den nya utmatningen</span><span class="sxs-lookup"><span data-stu-id="a52f3-670">Changed output type from CloudFile to AzureStorageFile, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="a52f3-671">”Get-AzStorageFile”</span><span class="sxs-lookup"><span data-stu-id="a52f3-671">'Get-AzStorageFile'</span></span>
    - <span data-ttu-id="a52f3-672">”Remove-AzStorageFile”</span><span class="sxs-lookup"><span data-stu-id="a52f3-672">'Remove-AzStorageFile'</span></span>
    - <span data-ttu-id="a52f3-673">”Get-AzStorageFileContent”</span><span class="sxs-lookup"><span data-stu-id="a52f3-673">'Get-AzStorageFileContent'</span></span>
    - <span data-ttu-id="a52f3-674">”Set-AzStorageFileContent”</span><span class="sxs-lookup"><span data-stu-id="a52f3-674">'Set-AzStorageFileContent'</span></span>
    - <span data-ttu-id="a52f3-675">”Start-AzStorageFileCopy”</span><span class="sxs-lookup"><span data-stu-id="a52f3-675">'Start-AzStorageFileCopy'</span></span>
* <span data-ttu-id="a52f3-676">Utdatatypen har ändrats från CloudFileDirectory till AzureStorageFileDirectory; ursprungliga utdata blir en underordnad egenskap i den nya utmatningen</span><span class="sxs-lookup"><span data-stu-id="a52f3-676">Changed output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="a52f3-677">”New-AzStorageDirectory”</span><span class="sxs-lookup"><span data-stu-id="a52f3-677">'New-AzStorageDirectory'</span></span>
    - <span data-ttu-id="a52f3-678">”Remove-AzStorageDirectory”</span><span class="sxs-lookup"><span data-stu-id="a52f3-678">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="a52f3-679">Utdatatypen har ändrats från CloudFileShare till AzureStorageFileShare; ursprungliga utdata blir en underordnad egenskap i den nya utmatningen</span><span class="sxs-lookup"><span data-stu-id="a52f3-679">Changed output type from CloudFileShare to AzureStorageFileShare, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="a52f3-680">”Get-AzStorageShare”</span><span class="sxs-lookup"><span data-stu-id="a52f3-680">'Get-AzStorageShare'</span></span>
    - <span data-ttu-id="a52f3-681">”New-AzStorageShare”</span><span class="sxs-lookup"><span data-stu-id="a52f3-681">'New-AzStorageShare'</span></span>
    - <span data-ttu-id="a52f3-682">”Remove-AzStorageShare”</span><span class="sxs-lookup"><span data-stu-id="a52f3-682">'Remove-AzStorageShare'</span></span>
* <span data-ttu-id="a52f3-683">Utdatatypen har ändrats från FileShareProperties till AzureStorageFileShare; ursprungliga utdata blir en underordnad egenskap i den nya utmatningen</span><span class="sxs-lookup"><span data-stu-id="a52f3-683">Changed output type from FileShareProperties to AzureStorageFileShare, the original output will become a sub child property of the new output</span></span>
    - <span data-ttu-id="a52f3-684">”Set-AzStorageShareQuota”</span><span class="sxs-lookup"><span data-stu-id="a52f3-684">'Set-AzStorageShareQuota'</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="a52f3-685">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="a52f3-685">Az.TrafficManager</span></span>
* <span data-ttu-id="a52f3-686">Felaktigt profilnamn har åtgärdats i utförliga utdata för ”DisableAzureTrafficManagerEndpoint”</span><span class="sxs-lookup"><span data-stu-id="a52f3-686">Fixed incorrect profile name in 'DisableAzureTrafficManagerEndpoint' verbose output</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a52f3-687">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a52f3-687">Az.Websites</span></span>
* <span data-ttu-id="a52f3-688">Stavfel har åtgärdats i hjälpen för ”Update-AzWebAppAccessRestrictionConfig”.</span><span class="sxs-lookup"><span data-stu-id="a52f3-688">Fixed typo on help of 'Update-AzWebAppAccessRestrictionConfig'.</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="a52f3-689">3.8.0 – April 2020</span><span class="sxs-lookup"><span data-stu-id="a52f3-689">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="a52f3-690">Höjdpunkter sedan den senaste uppdateringen</span><span class="sxs-lookup"><span data-stu-id="a52f3-690">Highlights since the last release</span></span>
* <span data-ttu-id="a52f3-691">PowerShell-versioner som Az.Storage stöder: Windows PowerShell 5.1, PowerShell Core 6.2.4+ och PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="a52f3-691">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="a52f3-692">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a52f3-692">Az.Accounts</span></span>
* <span data-ttu-id="a52f3-693">Uppdaterade URL:en för Azure PowerShell-enkäten i ”Resolve-AzError” [#11507]</span><span class="sxs-lookup"><span data-stu-id="a52f3-693">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="a52f3-694">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a52f3-694">Az.ApiManagement</span></span>
* <span data-ttu-id="a52f3-695">Lade till meddelande om icke-bakåtkompatibel ändring vid ändring i utdata för Azure File-cmdletar i en framtida version</span><span class="sxs-lookup"><span data-stu-id="a52f3-695">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="a52f3-696">"Set-AzApiManagementGroup" Uppdaterad dokumentation för att ange GroupId-parametern</span><span class="sxs-lookup"><span data-stu-id="a52f3-696">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="a52f3-697">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="a52f3-697">Az.Cdn</span></span>
* <span data-ttu-id="a52f3-698">Fast ChinaCDN-relaterad prissättning för SKU-visning</span><span class="sxs-lookup"><span data-stu-id="a52f3-698">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="a52f3-699">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a52f3-699">Az.CognitiveServices</span></span>
* <span data-ttu-id="a52f3-700">Identitet som stöds, kryptering, UserOwnedStorage</span><span class="sxs-lookup"><span data-stu-id="a52f3-700">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a52f3-701">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a52f3-701">Az.Compute</span></span>
* <span data-ttu-id="a52f3-702">Cmdleten ”Set-AzVmssOrchestrationServiceState” har lagts till.</span><span class="sxs-lookup"><span data-stu-id="a52f3-702">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="a52f3-703">”Get-AzVmss” med -InstanceView visar OrchestrationService-tillstånd.</span><span class="sxs-lookup"><span data-stu-id="a52f3-703">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a52f3-704">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a52f3-704">Az.IotHub</span></span>
* <span data-ttu-id="a52f3-705">Hantera den dubbla konfigurationen för IoT-enheter, nya cmdletar är:</span><span class="sxs-lookup"><span data-stu-id="a52f3-705">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="a52f3-706">'Get-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="a52f3-706">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="a52f3-707">'Update-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="a52f3-707">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="a52f3-708">En cmdlet har lagts till för att anropa direkt metod på en enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="a52f3-708">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="a52f3-709">Hantera dubbel konfiguration för IoT-enhetsmodul, nya cmdletar är:</span><span class="sxs-lookup"><span data-stu-id="a52f3-709">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="a52f3-710">'Get-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="a52f3-710">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="a52f3-711">'Update-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="a52f3-711">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="a52f3-712">Hantera IoT-automatisk konfiguration av enhetshantering i stor skala.</span><span class="sxs-lookup"><span data-stu-id="a52f3-712">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="a52f3-713">Nya cmdlet:ar är:</span><span class="sxs-lookup"><span data-stu-id="a52f3-713">New cmdlets are:</span></span>
    - <span data-ttu-id="a52f3-714">'Add-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="a52f3-714">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="a52f3-715">'Get-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="a52f3-715">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="a52f3-716">'Remove-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="a52f3-716">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="a52f3-717">'Set-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="a52f3-717">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="a52f3-718">En cmdlet har lagts till för att anropa en edge-modulmetod i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="a52f3-718">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a52f3-719">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a52f3-719">Az.KeyVault</span></span>
* <span data-ttu-id="a52f3-720">Har lagt till en ny cmdlet, "Update-AzKeyVault", som kan aktivera mjuk borttagning och rensning av skydd i ett valv</span><span class="sxs-lookup"><span data-stu-id="a52f3-720">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="a52f3-721">Har lagt till stöd i Microsoft.PowerShell.SecretManagement [#11178]</span><span class="sxs-lookup"><span data-stu-id="a52f3-721">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="a52f3-722">Åtgärdat fel i exemplen i 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span><span class="sxs-lookup"><span data-stu-id="a52f3-722">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="a52f3-723">Har lagt till stöd för privat slutpunkt</span><span class="sxs-lookup"><span data-stu-id="a52f3-723">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="a52f3-724">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="a52f3-724">Az.Maintenance</span></span>
* <span data-ttu-id="a52f3-725">Publicerar slutversion av underhålls-cmdletar för GA</span><span class="sxs-lookup"><span data-stu-id="a52f3-725">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a52f3-726">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a52f3-726">Az.Monitor</span></span>
* <span data-ttu-id="a52f3-727">Har lagt till cmdletar för privat länkomfång</span><span class="sxs-lookup"><span data-stu-id="a52f3-727">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="a52f3-728">'Get-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="a52f3-728">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="a52f3-729">'Remove-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="a52f3-729">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="a52f3-730">'New-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="a52f3-730">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="a52f3-731">'Update-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="a52f3-731">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="a52f3-732">'Get-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="a52f3-732">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="a52f3-733">'New-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="a52f3-733">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="a52f3-734">'Remove-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="a52f3-734">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a52f3-735">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a52f3-735">Az.Network</span></span>
* <span data-ttu-id="a52f3-736">Uppdaterade cmdletar för att aktivera anslutning på privat IP för Virtual Network Gateway.</span><span class="sxs-lookup"><span data-stu-id="a52f3-736">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="a52f3-737">'New-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="a52f3-737">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="a52f3-738">'Set-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="a52f3-738">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="a52f3-739">'New-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="a52f3-739">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="a52f3-740">'Set-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="a52f3-740">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="a52f3-741">Uppdaterade cmdletar för att aktivera FQDN-baserade LocalNetworkGateways och VpnSites</span><span class="sxs-lookup"><span data-stu-id="a52f3-741">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="a52f3-742">'New-AzLocalNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="a52f3-742">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="a52f3-743">'New-AzVpnSiteLink'</span><span class="sxs-lookup"><span data-stu-id="a52f3-743">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="a52f3-744">Stöd har lagts till för IPv6-adresstypen i ExpressRouteCircuitConnectionConfig (Global Reach)</span><span class="sxs-lookup"><span data-stu-id="a52f3-744">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="a52f3-745">Lade till 'Set-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="a52f3-745">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="a52f3-746">tillåter inställning av alla befintliga egenskaper inklusive IPv6CircuitConnectionProperties</span><span class="sxs-lookup"><span data-stu-id="a52f3-746">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="a52f3-747">Uppdaterade 'Add-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="a52f3-747">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="a52f3-748">Lade till en ytterligare valfri parameter, AddressPrefixType, för att specificera adresstypen för adressprefix</span><span class="sxs-lookup"><span data-stu-id="a52f3-748">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="a52f3-749">Uppdaterade cmdletar för att aktivera inställningen för DPD-timeout på Virtual Network Gateway-anslutningar.</span><span class="sxs-lookup"><span data-stu-id="a52f3-749">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="a52f3-750">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="a52f3-750">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="a52f3-751">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="a52f3-751">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="a52f3-752">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a52f3-752">Az.PolicyInsights</span></span>
* <span data-ttu-id="a52f3-753">Cmdleten "Start-AzPolicyComplianceScan" har lagts till för att utlösa genomsökningar av principefterlevnad</span><span class="sxs-lookup"><span data-stu-id="a52f3-753">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="a52f3-754">Principdefinition, uppsättningsdefinition och tilldelningsversioner har lagts till i "Get-AzPolicyState"-utdata</span><span class="sxs-lookup"><span data-stu-id="a52f3-754">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a52f3-755">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a52f3-755">Az.ServiceFabric</span></span>
* <span data-ttu-id="a52f3-756">Förbättrad kodformatering och användbarhet för "New-AzServiceFabricCluster"-exempel</span><span class="sxs-lookup"><span data-stu-id="a52f3-756">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="a52f3-757">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a52f3-757">Az.Sql</span></span>
* <span data-ttu-id="a52f3-758">Lade till cmdletarna "Get-AzSqlInstanceOperation" och "Stop-AzSqlInstanceOperation"</span><span class="sxs-lookup"><span data-stu-id="a52f3-758">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="a52f3-759">Stöd för granskning för ett lagringskonto i VNet.</span><span class="sxs-lookup"><span data-stu-id="a52f3-759">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a52f3-760">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a52f3-760">Az.Storage</span></span>
* <span data-ttu-id="a52f3-761">Lade till meddelande om icke-bakåtkompatibel ändring vid ändring i utdata för Azure File-cmdletar i en framtida version</span><span class="sxs-lookup"><span data-stu-id="a52f3-761">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="a52f3-762">Stöd för nya SkuName StandardGZRS, StandardRAGZRS när ett lagringskonto skapas/uppdateras</span><span class="sxs-lookup"><span data-stu-id="a52f3-762">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="a52f3-763">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="a52f3-763">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="a52f3-764">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="a52f3-764">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="a52f3-765">Stöd för DataLake Gen2</span><span class="sxs-lookup"><span data-stu-id="a52f3-765">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="a52f3-766">'New-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="a52f3-766">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="a52f3-767">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="a52f3-767">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="a52f3-768">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="a52f3-768">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="a52f3-769">'Move-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="a52f3-769">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="a52f3-770">'Set-AzDataLakeGen2ItemAclObject'</span><span class="sxs-lookup"><span data-stu-id="a52f3-770">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="a52f3-771">'Update-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="a52f3-771">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="a52f3-772">'Get-AzDataLakeGen2ItemContent'</span><span class="sxs-lookup"><span data-stu-id="a52f3-772">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="a52f3-773">'Remove-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="a52f3-773">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="a52f3-774">0.10.0-förhandsversion – April 2020</span><span class="sxs-lookup"><span data-stu-id="a52f3-774">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="a52f3-775">Allmänt</span><span class="sxs-lookup"><span data-stu-id="a52f3-775">General</span></span>
* <span data-ttu-id="a52f3-776">Az-moduler är nu tillgängliga i förhandsversion på Azure Stack Hub.</span><span class="sxs-lookup"><span data-stu-id="a52f3-776">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="a52f3-777">Därmed möjliggörs kompatibilitet för flera plattformar med Linux och macOs.</span><span class="sxs-lookup"><span data-stu-id="a52f3-777">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="a52f3-778">Azure Stack Hub stöder nu PowerShell Core med AZ-moduler. Mer information finns [här](https://aka.ms/az4AzureStack)</span><span class="sxs-lookup"><span data-stu-id="a52f3-778">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](https://aka.ms/az4AzureStack)</span></span>
* <span data-ttu-id="a52f3-779">Supportprofil för AZ-moduler 2019-03-01-hybrid:</span><span class="sxs-lookup"><span data-stu-id="a52f3-779">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="a52f3-780">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="a52f3-780">Az.Billing</span></span>
  - <span data-ttu-id="a52f3-781">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a52f3-781">Az.Compute</span></span>
  - <span data-ttu-id="a52f3-782">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="a52f3-782">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="a52f3-783">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a52f3-783">Az.EventHub</span></span>
  - <span data-ttu-id="a52f3-784">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a52f3-784">Az.IotHub</span></span>
  - <span data-ttu-id="a52f3-785">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a52f3-785">Az.KeyVault</span></span>
  - <span data-ttu-id="a52f3-786">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a52f3-786">Az.Monitor</span></span>
  - <span data-ttu-id="a52f3-787">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a52f3-787">Az.Network</span></span>
  - <span data-ttu-id="a52f3-788">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a52f3-788">Az.Resources</span></span>
  - <span data-ttu-id="a52f3-789">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a52f3-789">Az.Storage</span></span>
  - <span data-ttu-id="a52f3-790">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a52f3-790">Az.Websites</span></span>
* <span data-ttu-id="a52f3-791">Tre nya PowerShell-moduler för AZ har introducerats som fungerar med Azure Stack Hub, och de är Az.Databox, Az.IotHub och Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a52f3-791">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="a52f3-792">Kommandona är i princip oförändrade, med endast mindre ändringar som att AzureRM ändras till AZ</span><span class="sxs-lookup"><span data-stu-id="a52f3-792">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="a52f3-793">En uppdaterad länk till PowerShell-dokumentationen för Azure Stack Hub finns [här](https://aka.ms/InstallASHPowerShell)</span><span class="sxs-lookup"><span data-stu-id="a52f3-793">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](https://aka.ms/InstallASHPowerShell)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="a52f3-794">3.7.0 – mars 2020</span><span class="sxs-lookup"><span data-stu-id="a52f3-794">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a52f3-795">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a52f3-795">Az.Accounts</span></span>
* <span data-ttu-id="a52f3-796">Åtgärdade ”Get-AzTenant”/”Get-AzDefault”/”Set-AzDefault”-utlösning av NullReferenceException när du inte är inloggad [#10292]</span><span class="sxs-lookup"><span data-stu-id="a52f3-796">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a52f3-797">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a52f3-797">Az.Compute</span></span>
* <span data-ttu-id="a52f3-798">Följande parametrar har lagts till i cmdleten ”New-AzDiskConfig”:</span><span class="sxs-lookup"><span data-stu-id="a52f3-798">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="a52f3-799">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="a52f3-799">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="a52f3-800">Tillåten krypteringsegenskap till målparametern för cmdleten ”New-AzGalleryImageVersion”.</span><span class="sxs-lookup"><span data-stu-id="a52f3-800">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="a52f3-801">Åtgärdade tempDisk-problem för cmdletarna ”Set-AzVmss”-Reimage och ”Invoke-AzVMReimage”.</span><span class="sxs-lookup"><span data-stu-id="a52f3-801">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="a52f3-802">[#11354]</span><span class="sxs-lookup"><span data-stu-id="a52f3-802">[#11354]</span></span>
* <span data-ttu-id="a52f3-803">Stöd har lagts till i nedanstående cmdletar för nytt SAP-tillägg</span><span class="sxs-lookup"><span data-stu-id="a52f3-803">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="a52f3-804">”Set-AzVMAEMExtension”</span><span class="sxs-lookup"><span data-stu-id="a52f3-804">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="a52f3-805">”Get-AzVMAEMExtension”</span><span class="sxs-lookup"><span data-stu-id="a52f3-805">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="a52f3-806">”Remove-AzVMAEMExtension”</span><span class="sxs-lookup"><span data-stu-id="a52f3-806">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="a52f3-807">”Update-AzVMAEMExtension”</span><span class="sxs-lookup"><span data-stu-id="a52f3-807">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="a52f3-808">Åtgärdade fel i exempel på hjälpdokument</span><span class="sxs-lookup"><span data-stu-id="a52f3-808">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="a52f3-809">Visade det exakta strängvärdet för VM PowerState i tabellformat.</span><span class="sxs-lookup"><span data-stu-id="a52f3-809">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="a52f3-810">”New-AzVmssConfig”: den fasta serialiseringen av egenskapen AutomaticRepairs när SinglePlacementGroup är inaktiverad.</span><span class="sxs-lookup"><span data-stu-id="a52f3-810">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="a52f3-811">[#11257]</span><span class="sxs-lookup"><span data-stu-id="a52f3-811">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a52f3-812">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a52f3-812">Az.DataFactory</span></span>
* <span data-ttu-id="a52f3-813">ADF .Net SDK har uppdaterats till 4.8.0</span><span class="sxs-lookup"><span data-stu-id="a52f3-813">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="a52f3-814">Valfria parametrar har lagts till i kommandot ”Invoke-AzDataFactoryV2Pipeline” för att stödja omkörning</span><span class="sxs-lookup"><span data-stu-id="a52f3-814">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a52f3-815">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a52f3-815">Az.DataLakeStore</span></span>
* <span data-ttu-id="a52f3-816">Lade till beskrivning för icke-bakåtkompatibel ändring för ”Export-AzDataLakeStoreItem” och ”Import-AzDataLakeStoreItem”</span><span class="sxs-lookup"><span data-stu-id="a52f3-816">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="a52f3-817">Lade till alternativ för bytekodning för ”New-AzDataLakeStoreItem”, ”Add-AzDAtaLakeStoreItemContent” och ”Get-AzDAtaLakeStoreItemContent”</span><span class="sxs-lookup"><span data-stu-id="a52f3-817">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="a52f3-818">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a52f3-818">Az.HDInsight</span></span>
* <span data-ttu-id="a52f3-819">Stöd för att ange en minimal TLS-version som stöds när klustret skapas.</span><span class="sxs-lookup"><span data-stu-id="a52f3-819">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a52f3-820">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a52f3-820">Az.IotHub</span></span>
* <span data-ttu-id="a52f3-821">Stöd har lagts till för att hantera distribuerade inställningar per enhet.</span><span class="sxs-lookup"><span data-stu-id="a52f3-821">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="a52f3-822">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="a52f3-822">New Cmdlets are:</span></span>
    - <span data-ttu-id="a52f3-823">”Get-AzIotHubDistributedTracing”</span><span class="sxs-lookup"><span data-stu-id="a52f3-823">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="a52f3-824">”Set-AzIotHubDistributedTracing”</span><span class="sxs-lookup"><span data-stu-id="a52f3-824">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a52f3-825">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a52f3-825">Az.KeyVault</span></span>
* <span data-ttu-id="a52f3-826">Ändrade attribut för icke-bakåtkompatibel ändring lades till för ”New-AzKeyVault”</span><span class="sxs-lookup"><span data-stu-id="a52f3-826">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a52f3-827">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a52f3-827">Az.Monitor</span></span>
* <span data-ttu-id="a52f3-828">Uppdaterad dokumentation för ”New-AzScheduledQueryRuleLogMetricTrigger”</span><span class="sxs-lookup"><span data-stu-id="a52f3-828">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a52f3-829">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a52f3-829">Az.Network</span></span>
* <span data-ttu-id="a52f3-830">Uppdaterade cmdletar för att tillåta VirtualHubVnetConnections mellan klienter</span><span class="sxs-lookup"><span data-stu-id="a52f3-830">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="a52f3-831">”New-AzVirtualHubVnetConnection”</span><span class="sxs-lookup"><span data-stu-id="a52f3-831">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="a52f3-832">”Update-AzVirtualHubVnetConnection”</span><span class="sxs-lookup"><span data-stu-id="a52f3-832">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="a52f3-833">”New-AzVirtualHub”</span><span class="sxs-lookup"><span data-stu-id="a52f3-833">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="a52f3-834">”Update-AzVirtualHub”</span><span class="sxs-lookup"><span data-stu-id="a52f3-834">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="a52f3-835">SQL Management SDK-beroende har tagits bort</span><span class="sxs-lookup"><span data-stu-id="a52f3-835">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="a52f3-836">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a52f3-836">Az.PolicyInsights</span></span>
* <span data-ttu-id="a52f3-837">Förbättrade felmeddelanden</span><span class="sxs-lookup"><span data-stu-id="a52f3-837">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a52f3-838">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a52f3-838">Az.RecoveryServices</span></span>
* <span data-ttu-id="a52f3-839">Azure Site Recovery har lagt till stöd för återaktivering av skydd och uppdaterade VM-egenskaper för virtuella Azure-datorer med krypterad disk.</span><span class="sxs-lookup"><span data-stu-id="a52f3-839">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="a52f3-840">Lade till Azure Site Recovery VmwareToAzure-egenskaper för DR-övervakning</span><span class="sxs-lookup"><span data-stu-id="a52f3-840">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="a52f3-841">Azure Backup har lagt till stöd för att försöka uppdatera principuppdateringen för misslyckade objekt på nytt.</span><span class="sxs-lookup"><span data-stu-id="a52f3-841">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="a52f3-842">Azure Backup lagt till stöd för diskundantagsinställningar under säkerhetskopiering och återställning.</span><span class="sxs-lookup"><span data-stu-id="a52f3-842">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="a52f3-843">Azure Backup lagt till stöd för att återställa flera filer/mappar i AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="a52f3-843">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="a52f3-844">Azure Backup lade till support för användardefinierad Resourcegroup-support vid uppdatering av IaasVM-princip</span><span class="sxs-lookup"><span data-stu-id="a52f3-844">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="a52f3-845">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a52f3-845">Az.Resources</span></span>
* <span data-ttu-id="a52f3-846">Åtgärdade ”Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType” så att den använder den faktisk apiVersion av resurser i stället för standard-apiVersion [#11267]</span><span class="sxs-lookup"><span data-stu-id="a52f3-846">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="a52f3-847">Lade till correlationId-loggning för felscenarier</span><span class="sxs-lookup"><span data-stu-id="a52f3-847">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="a52f3-848">Liten dokumentationsändring för ”Get-AzResourceLock”.</span><span class="sxs-lookup"><span data-stu-id="a52f3-848">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="a52f3-849">Lade till exempel.</span><span class="sxs-lookup"><span data-stu-id="a52f3-849">Added example.</span></span>
* <span data-ttu-id="a52f3-850">Undantaget enkelt citattecken i parametervärde för ”Get-AzADUser” [#11317]</span><span class="sxs-lookup"><span data-stu-id="a52f3-850">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="a52f3-851">Nya cmdletar har lagts till för distributionsskript (”Get-AzDeploymentScript”, ”Get-AzDeploymentScriptLog”, ”Save-AzDeploymentScriptLog”, ”Remove-AzDeploymentScript”)</span><span class="sxs-lookup"><span data-stu-id="a52f3-851">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="a52f3-852">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a52f3-852">Az.Sql</span></span>
* <span data-ttu-id="a52f3-853">En läsbar sekundär parameter har lagts till i Invoke-AzSqlDatabaseFailover</span><span class="sxs-lookup"><span data-stu-id="a52f3-853">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="a52f3-854">Cmdleten Disable-AzSqlServerActiveDirectoryOnlyAuthentication har lagts till</span><span class="sxs-lookup"><span data-stu-id="a52f3-854">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="a52f3-855">Den sparade känslighet rangordningen när kolumner klassificeras i databasen.</span><span class="sxs-lookup"><span data-stu-id="a52f3-855">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="a52f3-856">Az.Support</span><span class="sxs-lookup"><span data-stu-id="a52f3-856">Az.Support</span></span>
* <span data-ttu-id="a52f3-857">Allmän tillgänglighet för ”Az.Support”-modulen</span><span class="sxs-lookup"><span data-stu-id="a52f3-857">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a52f3-858">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a52f3-858">Az.Websites</span></span>
* <span data-ttu-id="a52f3-859">Stöd har lagts till för att arbeta med trafikdirigeringsregler för webbappar under nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="a52f3-859">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="a52f3-860">”Get-AzWebAppTrafficRouting”</span><span class="sxs-lookup"><span data-stu-id="a52f3-860">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="a52f3-861">”Update-AzWebAppTrafficRouting”</span><span class="sxs-lookup"><span data-stu-id="a52f3-861">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="a52f3-862">”Add-AzWebAppTrafficRouting”</span><span class="sxs-lookup"><span data-stu-id="a52f3-862">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="a52f3-863">”Remove-AzWebAppTrafficRouting”</span><span class="sxs-lookup"><span data-stu-id="a52f3-863">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="a52f3-864">3.6.1 – mars 2020</span><span class="sxs-lookup"><span data-stu-id="a52f3-864">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a52f3-865">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a52f3-865">Az.Accounts</span></span>
* <span data-ttu-id="a52f3-866">Öppna sidan med Azure PowerShell-enkäten i ”Send-Feedback” [#11020]</span><span class="sxs-lookup"><span data-stu-id="a52f3-866">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="a52f3-867">Visa URL:en för Azure PowerShell-enkäten i ”Resolve-Error” [#11021]</span><span class="sxs-lookup"><span data-stu-id="a52f3-867">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="a52f3-868">Az-version har lagts till i UserAgent</span><span class="sxs-lookup"><span data-stu-id="a52f3-868">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="a52f3-869">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a52f3-869">Az.ApiManagement</span></span>
* <span data-ttu-id="a52f3-870">Stöd har lagts till för att hämta och konfigurera en anpassad domän på DeveloperPortal-slutpunkten [#11007]</span><span class="sxs-lookup"><span data-stu-id="a52f3-870">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="a52f3-871">”Export-AzApiManagementApi” Stöd har lagts till för att ladda ned API-definition i Json-format [#9987]</span><span class="sxs-lookup"><span data-stu-id="a52f3-871">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="a52f3-872">”Import-AzApiManagementApi” Stöd har lagts till för att importera OpenApi 3.0-definition från Json-dokument</span><span class="sxs-lookup"><span data-stu-id="a52f3-872">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="a52f3-873">”New-AzApiManagementIdentityProvider” och ”Set-AzApiManagementIdentityProvider” Stöd har lagts till för att konfigurera ”Signin Tenant” för AAD B2C-provider [#9784]</span><span class="sxs-lookup"><span data-stu-id="a52f3-873">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a52f3-874">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a52f3-874">Az.DataLakeStore</span></span>
* <span data-ttu-id="a52f3-875">En referens har uttryckligen lagts till för System.Buffers i csproj och psd1.</span><span class="sxs-lookup"><span data-stu-id="a52f3-875">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a52f3-876">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a52f3-876">Az.IotHub</span></span>
* <span data-ttu-id="a52f3-877">Lade till stöd för att hantera enheter i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="a52f3-877">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="a52f3-878">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="a52f3-878">New Cmdlets are:</span></span>
    - <span data-ttu-id="a52f3-879">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="a52f3-879">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="a52f3-880">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="a52f3-880">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="a52f3-881">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="a52f3-881">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="a52f3-882">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="a52f3-882">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="a52f3-883">Stöd har lagts till för att hantera moduler på en mål-IoT-enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="a52f3-883">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="a52f3-884">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="a52f3-884">New Cmdlets are:</span></span>
    - <span data-ttu-id="a52f3-885">”Add-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="a52f3-885">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="a52f3-886">”Get-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="a52f3-886">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="a52f3-887">”Remove-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="a52f3-887">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="a52f3-888">”Set-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="a52f3-888">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="a52f3-889">Cmdlet har lagts till för att hämta anslutningssträngen för en mål-IoT-enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="a52f3-889">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="a52f3-890">Cmdlet har lagts till för att hämta anslutningssträngen för en modul på en mål-IoT-enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="a52f3-890">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="a52f3-891">Stöd har lagts till för att hämta/ange en överordnad enhet för en IoT-enhet.</span><span class="sxs-lookup"><span data-stu-id="a52f3-891">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="a52f3-892">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="a52f3-892">New Cmdlets are:</span></span>
    - <span data-ttu-id="a52f3-893">”Get-AzIotHubDeviceParent”</span><span class="sxs-lookup"><span data-stu-id="a52f3-893">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="a52f3-894">”Set-AzIotHubDeviceParent”</span><span class="sxs-lookup"><span data-stu-id="a52f3-894">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="a52f3-895">Stöd har lagts till för att hantera en enhets överordnade och underordnade relationer.</span><span class="sxs-lookup"><span data-stu-id="a52f3-895">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a52f3-896">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a52f3-896">Az.Monitor</span></span>
* <span data-ttu-id="a52f3-897">Utdatavärdet har åtgärdats för ”Get-AzMetricDefinition” [#9714]</span><span class="sxs-lookup"><span data-stu-id="a52f3-897">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a52f3-898">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a52f3-898">Az.Network</span></span>
* <span data-ttu-id="a52f3-899">SQL Management SDK har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="a52f3-899">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="a52f3-900">Ett problem har åtgärdats med namngivningsskillnader i klassen PrivateLinkServiceConnectionState.</span><span class="sxs-lookup"><span data-stu-id="a52f3-900">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="a52f3-901">Fältet ActionsRequired mappar till ActionRequired.</span><span class="sxs-lookup"><span data-stu-id="a52f3-901">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="a52f3-902">PublicNetworkAccess har lagts till i ”New-AzSqlServer” och ”Set-AzSqlServer”</span><span class="sxs-lookup"><span data-stu-id="a52f3-902">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="a52f3-903">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a52f3-903">Az.Resources</span></span>
* <span data-ttu-id="a52f3-904">Null-referensfel har åtgärdats i ”Get-AzRoleAssignment”</span><span class="sxs-lookup"><span data-stu-id="a52f3-904">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="a52f3-905">Växlarna ”-Force” och ”-PassThru” är valfria i ”Remove-AzADGroup” [#10849]</span><span class="sxs-lookup"><span data-stu-id="a52f3-905">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="a52f3-906">Ett problem har åtgärdats som gjorde att ”MailNickname” inte returnerades i ”Remove-AzADGroup” [#11167]</span><span class="sxs-lookup"><span data-stu-id="a52f3-906">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="a52f3-907">Ett problem har åtgärdats som gjorde att pipe-åtgärden ”Remove-AzADGroup” inte fungerar [#11171]</span><span class="sxs-lookup"><span data-stu-id="a52f3-907">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="a52f3-908">Ett null-referensfel har åtgärdats i GetAzureRoleAssignmentCommand</span><span class="sxs-lookup"><span data-stu-id="a52f3-908">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="a52f3-909">Attribut för icke-bakåtkompatibla ändringar har lagts till för kommande ändringar i cmdlets för principer</span><span class="sxs-lookup"><span data-stu-id="a52f3-909">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="a52f3-910">”Get-AzResourceGroup” har uppdaterats för att utföra taggfiltrering för resursgrupper på serversidan</span><span class="sxs-lookup"><span data-stu-id="a52f3-910">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="a52f3-911">Utökade Tag-cmdlets stöder -ResourceId</span><span class="sxs-lookup"><span data-stu-id="a52f3-911">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="a52f3-912">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="a52f3-912">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="a52f3-913">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="a52f3-913">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="a52f3-914">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="a52f3-914">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="a52f3-915">Ny Tag-cmdlet har lagts till</span><span class="sxs-lookup"><span data-stu-id="a52f3-915">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="a52f3-916">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="a52f3-916">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="a52f3-917">Flyttade ScopedDeployment från SDK 3.3.0</span><span class="sxs-lookup"><span data-stu-id="a52f3-917">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="a52f3-918">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a52f3-918">Az.Sql</span></span>
* <span data-ttu-id="a52f3-919">PublicNetworkAccess har lagts till i ”New-AzSqlServer” och ”Set-AzSqlServer”</span><span class="sxs-lookup"><span data-stu-id="a52f3-919">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="a52f3-920">Stöd har lagts till för konfiguration av säkerhetskopiering för långsiktig kvarhållning för hanterade databaser</span><span class="sxs-lookup"><span data-stu-id="a52f3-920">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="a52f3-921">Hämta/ange LTR-princip på en hanterad databas</span><span class="sxs-lookup"><span data-stu-id="a52f3-921">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="a52f3-922">Hämta LTR-säkerhetskopior efter hanterad databas, hanterad instans eller plats</span><span class="sxs-lookup"><span data-stu-id="a52f3-922">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="a52f3-923">Ta bort en LTR-säkerhetskopia</span><span class="sxs-lookup"><span data-stu-id="a52f3-923">Remove an LTR backup</span></span>
    - <span data-ttu-id="a52f3-924">Återställa en LTR-säkerhetskopia för att skapa en ny hanterad databas</span><span class="sxs-lookup"><span data-stu-id="a52f3-924">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="a52f3-925">MinimalTlsVersion har lagts till för New-AzSqlServer och Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="a52f3-925">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="a52f3-926">MinimalTlsVersion har lagts till för New-AzSqlInstance och Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="a52f3-926">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="a52f3-927">SQL SDK-versionen för Az.Network har ändrats</span><span class="sxs-lookup"><span data-stu-id="a52f3-927">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a52f3-928">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a52f3-928">Az.Storage</span></span>
* <span data-ttu-id="a52f3-929">AllowProtectedAppendWrite stöds i ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="a52f3-929">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="a52f3-930">”Set-AzRmStorageContainerImmutabilityPolicy”</span><span class="sxs-lookup"><span data-stu-id="a52f3-930">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="a52f3-931">Varningsmeddelande har lagts till om icke-bakåtkompatibel ändring för ändring av typen AzureStorageTable i en senare version</span><span class="sxs-lookup"><span data-stu-id="a52f3-931">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="a52f3-932">”New-AzStorageTable”</span><span class="sxs-lookup"><span data-stu-id="a52f3-932">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="a52f3-933">”Get-AzStorageTable”</span><span class="sxs-lookup"><span data-stu-id="a52f3-933">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a52f3-934">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a52f3-934">Az.Websites</span></span>
* <span data-ttu-id="a52f3-935">Tag-parametern har lagts till för ”New-AzAppServicePlan” och ”Set-AzAppServicePlan”</span><span class="sxs-lookup"><span data-stu-id="a52f3-935">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="a52f3-936">Stoppa cmdlet-körning om ett undantag uppstår när en anpassad domän läggs till på en webbplats</span><span class="sxs-lookup"><span data-stu-id="a52f3-936">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="a52f3-937">Stöd har lagts till för att utföra åtgärder för App Services som inte tillhör samma resursgrupp som App Services-planen</span><span class="sxs-lookup"><span data-stu-id="a52f3-937">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="a52f3-938">Åtkomstbegränsning har tillämpats på WebApp/Function i olika resursgrupper</span><span class="sxs-lookup"><span data-stu-id="a52f3-938">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="a52f3-939">Ett problem har åtgärdats för att ange anpassade värdnamn för WebAppSlots</span><span class="sxs-lookup"><span data-stu-id="a52f3-939">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="a52f3-940">3.5.0 – februari 2020</span><span class="sxs-lookup"><span data-stu-id="a52f3-940">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="a52f3-941">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="a52f3-941">Highlights since the last major release</span></span>
* <span data-ttu-id="a52f3-942">Uppdaterade telemetri på klientsidan.</span><span class="sxs-lookup"><span data-stu-id="a52f3-942">Updated client side telemetry.</span></span>
* <span data-ttu-id="a52f3-943">Az.IotHub lade till cmdletar som stöd för att hantera enheter.</span><span class="sxs-lookup"><span data-stu-id="a52f3-943">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="a52f3-944">Az.SqlVirtualMachine lade till cmdletar för lyssningsfunktion för tillgänglighetsgrupp.</span><span class="sxs-lookup"><span data-stu-id="a52f3-944">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="a52f3-945">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a52f3-945">Az.Accounts</span></span>
* <span data-ttu-id="a52f3-946">Lade till SubscriptionId, TenantId och körningstid i data för telemetri på klientsidan</span><span class="sxs-lookup"><span data-stu-id="a52f3-946">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a52f3-947">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a52f3-947">Az.Automation</span></span>
* <span data-ttu-id="a52f3-948">Åtgärdade skrivfel i exempel 1 i referensdokumentation för ”New-AzAutomationSoftwareUpdateConfiguration”</span><span class="sxs-lookup"><span data-stu-id="a52f3-948">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="a52f3-949">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a52f3-949">Az.CognitiveServices</span></span>
* <span data-ttu-id="a52f3-950">Uppdaterade SDK till 7.0</span><span class="sxs-lookup"><span data-stu-id="a52f3-950">Updated SDK to 7.0</span></span>
* <span data-ttu-id="a52f3-951">Förbättrade felmeddelande vid serversvar om tom brödtext</span><span class="sxs-lookup"><span data-stu-id="a52f3-951">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a52f3-952">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a52f3-952">Az.Compute</span></span>
* <span data-ttu-id="a52f3-953">Tillät tomt värde för ProximityPlacementGroupId under uppdatering</span><span class="sxs-lookup"><span data-stu-id="a52f3-953">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="a52f3-954">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="a52f3-954">Az.FrontDoor</span></span>
* <span data-ttu-id="a52f3-955">Lade till cmdlet för att hämta hanterade regeldefinitioner som kan användas i WAF</span><span class="sxs-lookup"><span data-stu-id="a52f3-955">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a52f3-956">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a52f3-956">Az.IotHub</span></span>
* <span data-ttu-id="a52f3-957">Lade till stöd för att hantera enheter i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="a52f3-957">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="a52f3-958">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="a52f3-958">New Cmdlets are:</span></span>
    - <span data-ttu-id="a52f3-959">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="a52f3-959">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="a52f3-960">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="a52f3-960">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="a52f3-961">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="a52f3-961">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="a52f3-962">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="a52f3-962">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a52f3-963">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a52f3-963">Az.KeyVault</span></span>
* <span data-ttu-id="a52f3-964">Åtgärdade duplicerad text för Add-AzKeyVaultKey.md</span><span class="sxs-lookup"><span data-stu-id="a52f3-964">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a52f3-965">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a52f3-965">Az.Monitor</span></span>
* <span data-ttu-id="a52f3-966">Åtgärdade beskrivning av cmdleten Get-AzLog.</span><span class="sxs-lookup"><span data-stu-id="a52f3-966">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="a52f3-967">En ny parameter med namnet ActionGroupId har lagts till i kommandot ”New-AzMetricAlertRuleV2”.</span><span class="sxs-lookup"><span data-stu-id="a52f3-967">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="a52f3-968">Användaren kan ange ActionGroupId(string) eller ActionGroup(ActivityLogAlertActionGroup).</span><span class="sxs-lookup"><span data-stu-id="a52f3-968">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a52f3-969">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a52f3-969">Az.Network</span></span>
* <span data-ttu-id="a52f3-970">Lade till en extra parameteranteckning för parametern ”-EnableProxyProtocol” för cmdleten ”New-AzPrivateLinkService”.</span><span class="sxs-lookup"><span data-stu-id="a52f3-970">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="a52f3-971">Åtgärdade FilterData-exempel i Start-AzVirtualNetworkGatewayConnectionPacketCapture.md och Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="a52f3-971">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="a52f3-972">Lade till paketinsamlingsexempel för att samla in alla inre och yttre paket i Start-AzVirtualNetworkGatewayConnectionPacketCapture.md och Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="a52f3-972">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="a52f3-973">Lade till stöd för Azure-brandväggsprincip på VNet-brandväggar</span><span class="sxs-lookup"><span data-stu-id="a52f3-973">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="a52f3-974">Inga nya cmdletar har lagts till.</span><span class="sxs-lookup"><span data-stu-id="a52f3-974">No new cmdlets are added.</span></span> <span data-ttu-id="a52f3-975">Lättar begränsningen för brandväggsprincip på VNet-brandväggar</span><span class="sxs-lookup"><span data-stu-id="a52f3-975">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a52f3-976">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a52f3-976">Az.RecoveryServices</span></span>
* <span data-ttu-id="a52f3-977">Lade till stöd för Restore-as-files för SQL-databaser.</span><span class="sxs-lookup"><span data-stu-id="a52f3-977">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a52f3-978">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a52f3-978">Az.Resources</span></span>
* <span data-ttu-id="a52f3-979">Omstrukturerade cmdletar för malldistribution</span><span class="sxs-lookup"><span data-stu-id="a52f3-979">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="a52f3-980">Lade till nya cmdletar för att hantera distributioner i hanteringsgruppen: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a52f3-980">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="a52f3-981">Lade till nya cmdletar för att hantera distributioner i klientorganisationsområdet: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="a52f3-981">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="a52f3-982">Omstrukturerade \*-AzDeployment-cmdletar för att fungera specifikt i prenumerationsomfattningen</span><span class="sxs-lookup"><span data-stu-id="a52f3-982">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="a52f3-983">Skapade alias \*-AzSubscriptionDeployment för \*-AzDeployment-cmdletar</span><span class="sxs-lookup"><span data-stu-id="a52f3-983">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="a52f3-984">Åtgärdade ”Update-AzADApplication” när parametern ”AvailableToOtherTenants” inte har angetts</span><span class="sxs-lookup"><span data-stu-id="a52f3-984">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="a52f3-985">Tog bort ApplicationObjectWithoutCredentialParameterSet för att undvika AmbiguousParameterSetException.</span><span class="sxs-lookup"><span data-stu-id="a52f3-985">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="a52f3-986">Återskapade hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="a52f3-986">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="a52f3-987">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a52f3-987">Az.Sql</span></span>
* <span data-ttu-id="a52f3-988">Lade till stöd för återställning till tidpunkt mellan prenumerationer på hanterade instanser.</span><span class="sxs-lookup"><span data-stu-id="a52f3-988">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="a52f3-989">Lade till stöd för att ändra befintlig SQL Managed Instance-maskinvarugenerering</span><span class="sxs-lookup"><span data-stu-id="a52f3-989">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="a52f3-990">Åtgärdade ”Update-AzSqlServerVulnerabilityAssessmentSetting”-hjälpexempel: parameter/egenskapsutdata - EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="a52f3-990">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="a52f3-991">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="a52f3-991">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="a52f3-992">Lade till cmdletar för lyssningsfunktion för tillgänglighetsgrupp</span><span class="sxs-lookup"><span data-stu-id="a52f3-992">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="a52f3-993">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="a52f3-993">Az.StorageSync</span></span>
* <span data-ttu-id="a52f3-994">Uppdaterade teckenuppsättningar som stöds i ”Invoke-AzStorageSyncCompatibilityCheck”.</span><span class="sxs-lookup"><span data-stu-id="a52f3-994">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="a52f3-995">3.4.0 – februari 2020</span><span class="sxs-lookup"><span data-stu-id="a52f3-995">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="a52f3-996">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="a52f3-996">Highlights since the last major release</span></span>
* <span data-ttu-id="a52f3-997">Första Az.CosmosDB-versionen 0.1.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="a52f3-997">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="a52f3-998">Stöd för Az.Network ConnectionMonitor V2 har lagts till</span><span class="sxs-lookup"><span data-stu-id="a52f3-998">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="a52f3-999">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a52f3-999">Az.Accounts</span></span>
* <span data-ttu-id="a52f3-1000">Inaktivera automatisk sparande av kontext när AzureRmContext.json inte är tillgängligt</span><span class="sxs-lookup"><span data-stu-id="a52f3-1000">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="a52f3-1001">Uppdatera referensen till Azure Powershell Common till 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="a52f3-1001">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="a52f3-1002">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a52f3-1002">Az.ApiManagement</span></span>
* <span data-ttu-id="a52f3-1003">**Get-AzApiManagementApiSchema** Hämtning av Open-Api-schema som är associerat med ett API har åtgärdats   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="a52f3-1003">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="a52f3-1004">**New-AzApiManagementProduct**\* och **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="a52f3-1004">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="a52f3-1005">Åtgärda dokumentation för https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="a52f3-1005">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="a52f3-1006">**Set-AzApiManagementApi** Exempel för att visa hur ServiceUrl uppdateras med hjälp av cmdleten har lagts till</span><span class="sxs-lookup"><span data-stu-id="a52f3-1006">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a52f3-1007">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a52f3-1007">Az.Compute</span></span>
* <span data-ttu-id="a52f3-1008">Begränsa antalet VM-status till 100 för att undvika begränsning när Get-AzVM -Status utförs utan VM-namn.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1008">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="a52f3-1009">Lägg till cmdleten Update-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="a52f3-1009">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="a52f3-1010">Lägg till parametrarna EncryptionType och DiskEncryptionSetId i följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="a52f3-1010">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="a52f3-1011">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="a52f3-1011">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="a52f3-1012">Lägg till parametern ColocationStatus för cmdleten Get-AzProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1012">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a52f3-1013">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a52f3-1013">Az.DataFactory</span></span>
* <span data-ttu-id="a52f3-1014">Uppdatera ADF .Net SDK-versionen till 4.7.0</span><span class="sxs-lookup"><span data-stu-id="a52f3-1014">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="a52f3-1015">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="a52f3-1015">Az.DeploymentManager</span></span>
* <span data-ttu-id="a52f3-1016">Lägger till LIST-åtgärder för resurser</span><span class="sxs-lookup"><span data-stu-id="a52f3-1016">Adds LIST operations for resources</span></span>
* <span data-ttu-id="a52f3-1017">Lägger till funktion för att utföra åtgärder för hälsokontrollsteg</span><span class="sxs-lookup"><span data-stu-id="a52f3-1017">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="a52f3-1018">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a52f3-1018">Az.HDInsight</span></span>
* <span data-ttu-id="a52f3-1019">Åtgärda dokumentfel för New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1019">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a52f3-1020">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a52f3-1020">Az.KeyVault</span></span>
* <span data-ttu-id="a52f3-1021">Lägg till Name-alias för attributet VaultName så att Remove-AzureKeyVault stämmer överens med New-AzureKeyVault.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1021">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a52f3-1022">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a52f3-1022">Az.Network</span></span>
* <span data-ttu-id="a52f3-1023">Nytt exempel har lagts till i Set-AzNetworkWatcherConfigFlowLog.md för att demonstrera ett inaktiveringsscenario för Trafikanalys.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1023">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="a52f3-1024">Lägg till stöd för att tilldela konfiguration av hanterings-IP till Azure Firewall – ett dedikerat undernät och en offentlig IP som brandväggen använder för dess hanteringstrafik</span><span class="sxs-lookup"><span data-stu-id="a52f3-1024">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="a52f3-1025">Cmdleten New-AzFirewall har uppdaterats:</span><span class="sxs-lookup"><span data-stu-id="a52f3-1025">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="a52f3-1026">Parametern -ManagementPublicIpAddress (inte obligatorisk) som accepterar ett offentligt IP-adressobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="a52f3-1026">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="a52f3-1027">Metoden SetManagementIpConfiguration har lagts till för brandväggsobjekt – kräver ett undernät och en offentlig IP-adress som indata – undernätets namn måste vara ”AzureFirewallManagementSubnet”</span><span class="sxs-lookup"><span data-stu-id="a52f3-1027">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="a52f3-1028">Exempel för Get-AzNetworkSecurityGroup har korrigerats så att exempel visas för NSG:er i stället för nätverksgränssnitt.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1028">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="a52f3-1029">Ett skrivfel har åtgärdats i kommandot New-AzVpnSite som hindrade kompletteraren för resurs-ID från att fylla i en parameter.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1029">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="a52f3-1030">Stöd för Url-konfiguration i åtgärdsuppsättningen för omskrivningsregler i Application Gateway har lagts till</span><span class="sxs-lookup"><span data-stu-id="a52f3-1030">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="a52f3-1031">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="a52f3-1031">New cmdlets added:</span></span>
        - <span data-ttu-id="a52f3-1032">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="a52f3-1032">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="a52f3-1033">Cmdletar har uppdaterats med den valfria parametern -UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="a52f3-1033">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="a52f3-1034">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="a52f3-1034">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="a52f3-1035">Lägg till stöd för resurser för NetworkWatcher ConnectionMonitor version 2</span><span class="sxs-lookup"><span data-stu-id="a52f3-1035">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="a52f3-1036">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a52f3-1036">Az.PolicyInsights</span></span>
* <span data-ttu-id="a52f3-1037">Stöd för utvärdering av efterlevnad innan fastställande av vilken resurs som ska åtgärdas</span><span class="sxs-lookup"><span data-stu-id="a52f3-1037">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="a52f3-1038">Lägg till parametern ”-ResourceDiscoverMode” för Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="a52f3-1038">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="a52f3-1039">Lägg till cmdleten Get-AzPolicyMetadata för att hämta resurser för principmetadata</span><span class="sxs-lookup"><span data-stu-id="a52f3-1039">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="a52f3-1040">Get-AzPolicyState och Get-AzPolicyStateSummary för API-versionen 2019-10-01 har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="a52f3-1040">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a52f3-1041">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a52f3-1041">Az.RecoveryServices</span></span>
* <span data-ttu-id="a52f3-1042">Azure Site Recovery-stöd för att ta bort en replikerad disk.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1042">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="a52f3-1043">Tillagt Azure Backup-stöd för att lägga till taggar när ett Recovery Services-valv skapas.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1043">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a52f3-1044">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a52f3-1044">Az.Resources</span></span>
* <span data-ttu-id="a52f3-1045">Gör -Scope valfritt i cmdletarna \*-AzPolicyAssignment med standardinställning till kontextprenumeration</span><span class="sxs-lookup"><span data-stu-id="a52f3-1045">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="a52f3-1046">Lägg till exempel på att skapa ADServicePrincipal med lösenord och nyckelautentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="a52f3-1046">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="a52f3-1047">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a52f3-1047">Az.Sql</span></span>
<span data-ttu-id="a52f3-1048">Åtgärda cmdleten New-AzSqlDatabaseSecondary så att existensen PartnerDatabaseName kontrolleras i stället för existensen DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1048">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a52f3-1049">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a52f3-1049">Az.Storage</span></span>
* <span data-ttu-id="a52f3-1050">Stöd för angivning av krypteringsnyckeltyp för Tabell/kö i Skapa lagringskonto</span><span class="sxs-lookup"><span data-stu-id="a52f3-1050">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="a52f3-1051">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a52f3-1051">New-AzStorageAccount</span></span>
* <span data-ttu-id="a52f3-1052">Visa RequestId när StorageException inte har ExtendedErrorInformation</span><span class="sxs-lookup"><span data-stu-id="a52f3-1052">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="a52f3-1053">Åtgärda exempel 6 för cmdleten Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="a52f3-1053">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a52f3-1054">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a52f3-1054">Az.Websites</span></span>
* <span data-ttu-id="a52f3-1055">Set-AzWebapp och Set-AzWebappSlot stöder egenskaperna AlwaysOn, MinTls och FtpsState</span><span class="sxs-lookup"><span data-stu-id="a52f3-1055">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="a52f3-1056">Åtgärdar problemet där inställning av HttpsOnly samtidigt som AppservicePlan ändrades med det enskilda kommandot Set-AzWebApp återställde HttpsOnly till standardvärdet</span><span class="sxs-lookup"><span data-stu-id="a52f3-1056">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="a52f3-1057">3.3.0 – januari 2020</span><span class="sxs-lookup"><span data-stu-id="a52f3-1057">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a52f3-1058">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a52f3-1058">Az.Accounts</span></span>
* <span data-ttu-id="a52f3-1059">Nu stöder Add-AzEnvironment och Set-AzEnvironment parametrarna AzureAttestationServiceEndpointResourceId och AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="a52f3-1059">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="a52f3-1060">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="a52f3-1060">Az.Cdn</span></span>
* <span data-ttu-id="a52f3-1061">Information om felsvar visas i New-AzCdnEndpoint-cmdleten</span><span class="sxs-lookup"><span data-stu-id="a52f3-1061">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a52f3-1062">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a52f3-1062">Az.Compute</span></span>
* <span data-ttu-id="a52f3-1063">Set-AzVMCustomScriptExtension-cmdleten har åtgärdats för en virtuell dator med hanterad OD-disk som inte har någon operativsystemprofil.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1063">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="a52f3-1064">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="a52f3-1064">Az.ContainerInstance</span></span>
* <span data-ttu-id="a52f3-1065">Parameternamn som används med New-AzContainerGroup-exempel har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="a52f3-1065">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="a52f3-1066">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="a52f3-1066">Az.DataBoxEdge</span></span>
* <span data-ttu-id="a52f3-1067">Cmdleten ”Get-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="a52f3-1067">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="a52f3-1068">Hämta gränslagringscontainern</span><span class="sxs-lookup"><span data-stu-id="a52f3-1068">Get the Edge Storage Container</span></span>
* <span data-ttu-id="a52f3-1069">Cmdleten ”New-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="a52f3-1069">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="a52f3-1070">Skapa en ny gränslagringscontainer</span><span class="sxs-lookup"><span data-stu-id="a52f3-1070">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="a52f3-1071">Cmdleten ”Remove-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="a52f3-1071">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="a52f3-1072">Ta bort gränslagringscontainern</span><span class="sxs-lookup"><span data-stu-id="a52f3-1072">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="a52f3-1073">Cmdleten ”Invoke-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="a52f3-1073">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="a52f3-1074">Anropa åtgärd för att uppdatera data i gränslagringscontainer</span><span class="sxs-lookup"><span data-stu-id="a52f3-1074">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="a52f3-1075">Cmdleten ”Get-AzDataBoxEdgeStorageAccount” har lagts till</span><span class="sxs-lookup"><span data-stu-id="a52f3-1075">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="a52f3-1076">Hämta gränslagringskontot</span><span class="sxs-lookup"><span data-stu-id="a52f3-1076">Get the Edge Storage Account</span></span>
* <span data-ttu-id="a52f3-1077">Cmdleten ”New-AzDataBoxEdgeStorageAccount” har lagts till</span><span class="sxs-lookup"><span data-stu-id="a52f3-1077">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="a52f3-1078">Skapa ett nytt gränslagringskonto</span><span class="sxs-lookup"><span data-stu-id="a52f3-1078">Create new Edge Storage Account</span></span>
* <span data-ttu-id="a52f3-1079">Cmdleten ”Remove-AzDataBoxEdgeStorageAccount” har lagts till</span><span class="sxs-lookup"><span data-stu-id="a52f3-1079">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="a52f3-1080">Ta bort gränslagringskontot</span><span class="sxs-lookup"><span data-stu-id="a52f3-1080">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="a52f3-1081">Anropa cmdleten ”Invoke-AzDataBoxEdgeShare”</span><span class="sxs-lookup"><span data-stu-id="a52f3-1081">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="a52f3-1082">Anropa åtgärd för att uppdatera resursdata</span><span class="sxs-lookup"><span data-stu-id="a52f3-1082">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="a52f3-1083">Cmdleten ”Set-AzDataBoxEdgeStorageAccountCredential” har lagts till</span><span class="sxs-lookup"><span data-stu-id="a52f3-1083">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="a52f3-1084">Ange autentiseringsuppgifter för az databoxedge-lagringskonto</span><span class="sxs-lookup"><span data-stu-id="a52f3-1084">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a52f3-1085">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a52f3-1085">Az.DataFactory</span></span>
* <span data-ttu-id="a52f3-1086">Lägg till AutoUpdateETA-, LatestVersion-, PushedVersion-, TaskQueueId- och VersionStatus-egenskaper för Get-AzDataFactoryV2IntegrationRuntime-cmd</span><span class="sxs-lookup"><span data-stu-id="a52f3-1086">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="a52f3-1087">Uppdatera ADF .Net SDK-versionen till 4.6.0</span><span class="sxs-lookup"><span data-stu-id="a52f3-1087">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="a52f3-1088">Lägg till parametern ”PublicIPs” för ”Set-AzureRmDataFactoryV2IntegrationRuntime”-cmd så att Azure-SSIS IR kan skapas med statiska offentliga IP-adresser.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1088">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="a52f3-1089">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="a52f3-1089">Az.DevTestLabs</span></span>
* <span data-ttu-id="a52f3-1090">Ta bort den brutna länken i Get-AzDtlAllowedVMSizesPolicy.md</span><span class="sxs-lookup"><span data-stu-id="a52f3-1090">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="a52f3-1091">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a52f3-1091">Az.EventHub</span></span>
* <span data-ttu-id="a52f3-1092">Korrigering av problem 10634: Åtgärda referensen till null-objekt för eventhubnamespace-borttagning</span><span class="sxs-lookup"><span data-stu-id="a52f3-1092">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="a52f3-1093">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a52f3-1093">Az.HDInsight</span></span>
* <span data-ttu-id="a52f3-1094">Åtgärda Invoke-AzHDInsightHiveJob.md-fel.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1094">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="a52f3-1095">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="a52f3-1095">Az.MachineLearning</span></span>
* <span data-ttu-id="a52f3-1096">Nedanstående cmdletar har tagits bort eftersom MachineLearningCompute inte längre är tillgängligt</span><span class="sxs-lookup"><span data-stu-id="a52f3-1096">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="a52f3-1097">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="a52f3-1097">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="a52f3-1098">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="a52f3-1098">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="a52f3-1099">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="a52f3-1099">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="a52f3-1100">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="a52f3-1100">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="a52f3-1101">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="a52f3-1101">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="a52f3-1102">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="a52f3-1102">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="a52f3-1103">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="a52f3-1103">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a52f3-1104">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a52f3-1104">Az.Network</span></span>
* <span data-ttu-id="a52f3-1105">Uppgradera beroende av Microsoft.Azure.Management.Sql från 1.36-preview till 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="a52f3-1105">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a52f3-1106">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a52f3-1106">Az.RecoveryServices</span></span>
* <span data-ttu-id="a52f3-1107">Ändrat Azure Site Recovery-stöd för krypterade vilande data på virtuella datorer med hanterade diskar med kundhanterade nycklar för Azure till Azure-providern.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1107">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="a52f3-1108">Azure Site Recovery-stöd för att ange ID för diskkrypteringsuppsättning som valfri inmatning för aktivering av skydd för VMware till Azure.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1108">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="a52f3-1109">Azure Site Recovery-stöd för att ange ID för diskkrypteringsuppsättning som valfri inmatning på disknivå för aktivering av skydd för VMware till Azure.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1109">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="a52f3-1110">Azure Site Recovery-stöd för att uppdatera replikeringsskyddade objekt med mappning för diskkrypteringsuppsättning för HyperV till Azure.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1110">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a52f3-1111">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a52f3-1111">Az.Resources</span></span>
* <span data-ttu-id="a52f3-1112">Åtgärda ett fel i hjälpdokument för ”Remove-AzTag”.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1112">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="a52f3-1113">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a52f3-1113">Az.Sql</span></span>
* <span data-ttu-id="a52f3-1114">Åtgärda funktioner i cmdletar för att ange baslinjen för sårbarhetsbedömning för arbete med huvuddatabasen för Azure-databasen och begränsa den för systemdatabaser på hanterade instanser.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1114">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="a52f3-1115">Åtgärda ett fel när en redundansgrupp för en SQL-instans skapas</span><span class="sxs-lookup"><span data-stu-id="a52f3-1115">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="a52f3-1116">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="a52f3-1116">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="a52f3-1117">Lägg till DR som en ny giltig licenstyp</span><span class="sxs-lookup"><span data-stu-id="a52f3-1117">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a52f3-1118">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a52f3-1118">Az.Storage</span></span>
* <span data-ttu-id="a52f3-1119">Lägg till varningsmeddelande om icke-bakåtkompatibel ändring för DefaultAction-värdeändring i en framtida version</span><span class="sxs-lookup"><span data-stu-id="a52f3-1119">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="a52f3-1120">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="a52f3-1120">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="a52f3-1121">Stöd för att hämta lagringskontots senaste synkroniseringstid genom att köra get-AzureRMStorageAccount med parametern -IncludeGeoReplicationStats</span><span class="sxs-lookup"><span data-stu-id="a52f3-1121">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="a52f3-1122">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a52f3-1122">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="a52f3-1123">3.2.0 – December 2019</span><span class="sxs-lookup"><span data-stu-id="a52f3-1123">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="a52f3-1124">Allmänt</span><span class="sxs-lookup"><span data-stu-id="a52f3-1124">General</span></span>
* <span data-ttu-id="a52f3-1125">Uppdatera referenser i .psd1 för att använda relativa sökvägar för alla moduler</span><span class="sxs-lookup"><span data-stu-id="a52f3-1125">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="a52f3-1126">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a52f3-1126">Az.Accounts</span></span>
* <span data-ttu-id="a52f3-1127">Ange rätt UserAgent för telemetri på klientsidan för Az 4.0 preview</span><span class="sxs-lookup"><span data-stu-id="a52f3-1127">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="a52f3-1128">Visa användarvänligt felmeddelande när kontexten är null i Az 4.0 preview</span><span class="sxs-lookup"><span data-stu-id="a52f3-1128">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="a52f3-1129">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="a52f3-1129">Az.Batch</span></span>
* <span data-ttu-id="a52f3-1130">Korrigera problem [#10602](https://github.com/Azure/azure-powershell/issues/10602), där **New-AzBatchPool** skickade VirtualMachineConfiguration.ContainerConfiguration eller VirtualMachineConfiguration.DataDisks på ett felaktigt sätt till servern.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1130">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a52f3-1131">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a52f3-1131">Az.DataFactory</span></span>
* <span data-ttu-id="a52f3-1132">Uppdatera ADF .Net SDK-versionen till 4.5.0</span><span class="sxs-lookup"><span data-stu-id="a52f3-1132">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="a52f3-1133">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="a52f3-1133">Az.FrontDoor</span></span>
* <span data-ttu-id="a52f3-1134">Stöd har lagts till för undantag för hanterade regler för brandväggen för webbaserade program</span><span class="sxs-lookup"><span data-stu-id="a52f3-1134">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="a52f3-1135">Lägg till SocketAddr för automatisk komplettering</span><span class="sxs-lookup"><span data-stu-id="a52f3-1135">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="a52f3-1136">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="a52f3-1136">Az.HealthcareApis</span></span>
* <span data-ttu-id="a52f3-1137">Undantagshantering</span><span class="sxs-lookup"><span data-stu-id="a52f3-1137">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a52f3-1138">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a52f3-1138">Az.KeyVault</span></span>
* <span data-ttu-id="a52f3-1139">Åtgärdat fel vid åtkomst av värde som kanske inte har angetts</span><span class="sxs-lookup"><span data-stu-id="a52f3-1139">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="a52f3-1140">Hantering av ECC-certifikat (Elliptic Curve Cryptography)</span><span class="sxs-lookup"><span data-stu-id="a52f3-1140">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="a52f3-1141">Stöd har lagts till för att ange kurvan för certifikatprinciper</span><span class="sxs-lookup"><span data-stu-id="a52f3-1141">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a52f3-1142">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a52f3-1142">Az.Monitor</span></span>
* <span data-ttu-id="a52f3-1143">Lägger till valfritt argument i kommandot Lägg till diagnostikinställningar.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1143">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="a52f3-1144">Ett växelargument som om det finns visar att exporten till Log Analytics måste ske till ett fast schema (kallas även</span><span class="sxs-lookup"><span data-stu-id="a52f3-1144">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="a52f3-1145">dedikerad, datatyp)</span><span class="sxs-lookup"><span data-stu-id="a52f3-1145">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a52f3-1146">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a52f3-1146">Az.Network</span></span>
* <span data-ttu-id="a52f3-1147">Stöd för IpGroups i program-, NAT- och nätverksregler för Azure Firewall.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1147">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a52f3-1148">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a52f3-1148">Az.Resources</span></span>
* <span data-ttu-id="a52f3-1149">Åtgärda ett problem där malldistributionen inte kan läsa en mallparameter om dess namn står i konflikt med ett inbyggt parameternamn.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1149">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="a52f3-1150">Uppdaterade princip-cmdletar för att använda den nya API-versionen 2019-09-01 som introducerar grupperingsstöd inom principuppsättningsdefinitioner.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1150">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="a52f3-1151">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a52f3-1151">Az.Sql</span></span>
* <span data-ttu-id="a52f3-1152">Uppgraderad funktion för att skapa lagring i automatisk aktivering av sårbarhetsbedömning till StorageV2</span><span class="sxs-lookup"><span data-stu-id="a52f3-1152">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a52f3-1153">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a52f3-1153">Az.Storage</span></span>
* <span data-ttu-id="a52f3-1154">Stöd för generering av blob/container-identitetsbaserad SAS-token med lagringskontextbaserad på OAuth-autentisering</span><span class="sxs-lookup"><span data-stu-id="a52f3-1154">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="a52f3-1155">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="a52f3-1155">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="a52f3-1156">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="a52f3-1156">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="a52f3-1157">Stöd för återkallning av användardelegeringsnycklar för lagringskonto för att återkalla alla SAS-token</span><span class="sxs-lookup"><span data-stu-id="a52f3-1157">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="a52f3-1158">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="a52f3-1158">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="a52f3-1159">Uppgradera till Microsoft.Azure.Management.Storage 14.2.0 för att stödja den nya API-versionen 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1159">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="a52f3-1160">Stöd för QuotaGiB (resurskvot i Gibibye) för värden över 5120 i hanteringsplanet för cmdletar för filresurser och parameteraliaset. Quota har också lagts till för parametern ”QuotaGiB”.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1160">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="a52f3-1161">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="a52f3-1161">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="a52f3-1162">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="a52f3-1162">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="a52f3-1163">Lägg till parameteraliaset QuotaGiB i parametern Quota</span><span class="sxs-lookup"><span data-stu-id="a52f3-1163">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="a52f3-1164">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="a52f3-1164">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="a52f3-1165">Åtgärda problemet att Set-AzStorageContainerAcl kan rensa den lagrade åtkomstprincipen</span><span class="sxs-lookup"><span data-stu-id="a52f3-1165">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="a52f3-1166">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="a52f3-1166">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="a52f3-1167">3.1.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="a52f3-1167">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="a52f3-1168">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="a52f3-1168">Highlights since the last major release</span></span>
* <span data-ttu-id="a52f3-1169">Az.DataBoxEdge 1.0.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="a52f3-1169">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="a52f3-1170">Az.SqlVirtualMachine 1.0.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="a52f3-1170">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a52f3-1171">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a52f3-1171">Az.Compute</span></span>
* <span data-ttu-id="a52f3-1172">Funktion för att använda en virtuell dator igen</span><span class="sxs-lookup"><span data-stu-id="a52f3-1172">VM Reapply feature</span></span>
    - <span data-ttu-id="a52f3-1173">Lägg till parameter för att använda igen till cmdleten Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="a52f3-1173">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="a52f3-1174">Funktionen AutomaticRepairs i VM-skalningsuppsättningar:</span><span class="sxs-lookup"><span data-stu-id="a52f3-1174">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="a52f3-1175">Lägg till parametrarna EnableAutomaticRepair, AutomaticRepairGracePeriod och AutomaticRepairMaxInstanceRepairsPercent till följande cmdletar:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a52f3-1175">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="a52f3-1176">Stöd för galleriavbildningar i flera klientorganisationer för New-AzVM</span><span class="sxs-lookup"><span data-stu-id="a52f3-1176">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="a52f3-1177">Lägg till "Spot" till argumentslutföraren i prioritetsparametern i cmdletarna New-AzVM, New-AzVMConfig och New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a52f3-1177">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="a52f3-1178">Lägg till parametrarna DiskIOPSReadWrite och DiskMBpsReadWrite till cmdleten Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="a52f3-1178">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="a52f3-1179">Ändra parametern SourceImageId för cmdleten New-AzGalleryImageVersion till valfri</span><span class="sxs-lookup"><span data-stu-id="a52f3-1179">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="a52f3-1180">Lägg till parametrarna OSDiskImage och DataDiskImage till cmdleten New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="a52f3-1180">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="a52f3-1181">Lägg till parametern HyperVGeneration till cmdleten New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="a52f3-1181">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="a52f3-1182">Lägg till parametern SkipExtensionsOnOverprovisionedVMs till cmdletarna New-AzVmss, New-AzVmssConfig och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a52f3-1182">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="a52f3-1183">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="a52f3-1183">Az.DataBoxEdge</span></span>
* <span data-ttu-id="a52f3-1184">Cmdleten `Get-AzDataBoxEdgeOrder` har lagts till</span><span class="sxs-lookup"><span data-stu-id="a52f3-1184">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="a52f3-1185">Hämta ordning</span><span class="sxs-lookup"><span data-stu-id="a52f3-1185">Get the Order</span></span>
* <span data-ttu-id="a52f3-1186">Cmdleten `New-AzDataBoxEdgeOrder` har lagts till</span><span class="sxs-lookup"><span data-stu-id="a52f3-1186">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="a52f3-1187">Skapa ny ordning</span><span class="sxs-lookup"><span data-stu-id="a52f3-1187">Create new Order</span></span>
* <span data-ttu-id="a52f3-1188">Cmdleten `Remove-AzDataBoxEdgeOrder` har lagts till</span><span class="sxs-lookup"><span data-stu-id="a52f3-1188">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="a52f3-1189">Ta bort ordning</span><span class="sxs-lookup"><span data-stu-id="a52f3-1189">Remove the Order</span></span>
* <span data-ttu-id="a52f3-1190">Cmdleten `New-AzDataBoxEdgeShare` har ändrats</span><span class="sxs-lookup"><span data-stu-id="a52f3-1190">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="a52f3-1191">Nu skapas lokal filresurs</span><span class="sxs-lookup"><span data-stu-id="a52f3-1191">Now creates Local Share</span></span>
* <span data-ttu-id="a52f3-1192">Cmdleten `Set-AzDataBoxEdgeRole` har lagts till</span><span class="sxs-lookup"><span data-stu-id="a52f3-1192">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="a52f3-1193">Nu kan IotRole mappas till filresursen</span><span class="sxs-lookup"><span data-stu-id="a52f3-1193">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="a52f3-1194">Cmdleten `Invoke-AzDataBoxEdgeDevice` har lagts till</span><span class="sxs-lookup"><span data-stu-id="a52f3-1194">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="a52f3-1195">Anropa genomsökningsuppdatering, ladda ned uppdatering, installera uppdateringar på enheten</span><span class="sxs-lookup"><span data-stu-id="a52f3-1195">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="a52f3-1196">Cmdleten `Get-AzDataBoxEdgeTrigger` har lagts till</span><span class="sxs-lookup"><span data-stu-id="a52f3-1196">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="a52f3-1197">Hämtar information om utlösare</span><span class="sxs-lookup"><span data-stu-id="a52f3-1197">Gets the information about Triggers</span></span>
* <span data-ttu-id="a52f3-1198">Cmdleten `New-AzDataBoxEdgeTrigger` har lagts till</span><span class="sxs-lookup"><span data-stu-id="a52f3-1198">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="a52f3-1199">Skapa nya utlösare</span><span class="sxs-lookup"><span data-stu-id="a52f3-1199">Create new Triggers</span></span>
* <span data-ttu-id="a52f3-1200">Cmdleten `Remove-AzDataBoxEdgeTrigger` har lagts till</span><span class="sxs-lookup"><span data-stu-id="a52f3-1200">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="a52f3-1201">Ta bort utlösare</span><span class="sxs-lookup"><span data-stu-id="a52f3-1201">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a52f3-1202">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a52f3-1202">Az.DataFactory</span></span>
* <span data-ttu-id="a52f3-1203">Uppdatera ADF .Net SDK-versionen till 4.4.0</span><span class="sxs-lookup"><span data-stu-id="a52f3-1203">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="a52f3-1204">Lägg till parametern ExpressCustomSetup för kommandot Set-AzureRmDataFactoryV2IntegrationRuntime för att aktivera installationskonfigurationer och komponenter från tredje part utan anpassat konfigurationsskript.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1204">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a52f3-1205">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a52f3-1205">Az.DataLakeStore</span></span>
* <span data-ttu-id="a52f3-1206">Uppdatera dokumentation för Get-AzDataLakeStoreDeletedItem och Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="a52f3-1206">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="a52f3-1207">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a52f3-1207">Az.EventHub</span></span>
* <span data-ttu-id="a52f3-1208">Korrigering av problem #10301: Korrigera datumformat för SAS-token</span><span class="sxs-lookup"><span data-stu-id="a52f3-1208">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="a52f3-1209">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="a52f3-1209">Az.FrontDoor</span></span>
* <span data-ttu-id="a52f3-1210">Lägg till parametern MinimumTlsVersion till Enable-AzFrontDoorCustomDomainHttps och New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="a52f3-1210">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="a52f3-1211">Lägg till parametrarna HealthProbeMethod och EnabledState till New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="a52f3-1211">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="a52f3-1212">Lägg till en ny cmdlet för att skapa BackendPoolsSettings-objekt som passar i skapande/uppdatering av Front Door</span><span class="sxs-lookup"><span data-stu-id="a52f3-1212">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="a52f3-1213">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="a52f3-1213">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a52f3-1214">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a52f3-1214">Az.Network</span></span>
* <span data-ttu-id="a52f3-1215">Ändra alternativexemplen Start-AzVirtualNetworkGatewayConnectionPacketCapture.md och Start-AzVirtualnetworkGatewayPacketCapture.md för FilterData.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1215">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="a52f3-1216">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="a52f3-1216">Az.PrivateDns</span></span>
* <span data-ttu-id="a52f3-1217">Uppdaterade PrivateDns .NET SDK till version 1.0.0</span><span class="sxs-lookup"><span data-stu-id="a52f3-1217">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a52f3-1218">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a52f3-1218">Az.RecoveryServices</span></span>
* <span data-ttu-id="a52f3-1219">Stöd för att välja disktyp vid aktivering av skydd i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1219">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="a52f3-1220">Korrigering av bugg för åtgärdsredigering av återställningsplan i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1220">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="a52f3-1221">Återställningsstöd för att godkänna filestream-databaser i Azure Backup SQL.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1221">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="a52f3-1222">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="a52f3-1222">Az.RedisCache</span></span>
* <span data-ttu-id="a52f3-1223">Parametern MinimumTlsVersion har lagts till i cmdletarna New-AzRedisCache och Set-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1223">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="a52f3-1224">Dessutom har MinimumTlsVersion lagts till i utdata för cmdleten Get-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1224">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="a52f3-1225">Verifiering har lagts till på parametern -Size i cmdletarna Set-AzRedisCache och New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="a52f3-1225">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="a52f3-1226">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a52f3-1226">Az.Resources</span></span>
- <span data-ttu-id="a52f3-1227">Uppdaterade policy-cmdletar för att använda den nya API-versionen 2019-06-01 som har en ny EnforcementMode-egenskap i policytilldelningen.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1227">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="a52f3-1228">Uppdaterade hjälpexempel för skapandet av policydefinition</span><span class="sxs-lookup"><span data-stu-id="a52f3-1228">Updated create policy definition help example</span></span>
- <span data-ttu-id="a52f3-1229">Åtgärda bugg i Remove-AZADServicePrincipal -ServicePrincipalName, utlös null-referens när tjänstens huvudnamn inte hittas.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1229">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="a52f3-1230">Åtgärda bugg i New-AZADServicePrincipal, utlös null-referens när klientorganisationen inte har någon prenumeration.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1230">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="a52f3-1231">Ändra New-AzAdServicePrincipal för att endast lägga till autentiseringsuppgifter för det associerade programmet.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1231">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="a52f3-1232">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a52f3-1232">Az.Sql</span></span>
* <span data-ttu-id="a52f3-1233">Stöd har lagts till för databasen ReadReplicaCount.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1233">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="a52f3-1234">Korrigerade Set-AzSqlDatabase när zonredundans inte har angetts</span><span class="sxs-lookup"><span data-stu-id="a52f3-1234">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="a52f3-1235">3.0.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="a52f3-1235">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="a52f3-1236">Allmänt</span><span class="sxs-lookup"><span data-stu-id="a52f3-1236">General</span></span>
* <span data-ttu-id="a52f3-1237">Az. PrivateDns 1.0.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="a52f3-1237">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="a52f3-1238">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a52f3-1238">Az.Accounts</span></span>
* <span data-ttu-id="a52f3-1239">Lägg till ett utfasningsmeddelande för aliaset Resolve-error.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1239">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="a52f3-1240">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="a52f3-1240">Az.Advisor</span></span>
* <span data-ttu-id="a52f3-1241">Den nya kategorin Operational Excellence har lagts till i cmdleten Get-AzAdvisorRecommendation.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1241">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="a52f3-1242">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="a52f3-1242">Az.Batch</span></span>
* <span data-ttu-id="a52f3-1243">`CoreQuota` på `BatchAccountContext` har bytt namn till `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1243">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="a52f3-1244">Det finns även en ny `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1244">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="a52f3-1245">Detta påverkar **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1245">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="a52f3-1246">**New-AzBatchTask** `-ResourceFile`-parametern tar nu en samling `PSResourceFile`-objekt som kan skapas med hjälp av den nya cmdleten **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1246">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="a52f3-1247">Ny **New-AzBatchResourceFile**-cmdlet för att skapa `PSResourceFile`-objekt.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1247">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="a52f3-1248">Dessa kan tillhandahållas till **New-AzBatchTask** på `-ResourceFile`-parametern.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1248">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="a52f3-1249">Detta stöder två nya typer av resursfiler förutom det befintliga sättet med `HttpUrl`:</span><span class="sxs-lookup"><span data-stu-id="a52f3-1249">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="a52f3-1250">`AutoStorageContainerName`-baserade resursfiler laddar ned en hel container för automatisk lagring till Batch-noden.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1250">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="a52f3-1251">`StorageContainerUrl`-baserade resursfiler laddar ned containern som anges i webbadressen till Batch-noden.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1251">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="a52f3-1252">Tog bort egenskapen `ApplicationPackages` för `PSApplication` som returnerades av **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1252">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="a52f3-1253">Specifika paket i ett program kan nu hämtas med hjälp av **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1253">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="a52f3-1254">Till exempel: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1254">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="a52f3-1255">Bytt namn på `ApplicationId` till `ApplicationName` på **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** och **Set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1255">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="a52f3-1256">`ApplicationId` är nu ett alias för `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1256">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="a52f3-1257">Ny `PSWindowsUserConfiguration`-egenskap till `PSUserAccount` lades till.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1257">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="a52f3-1258">Bytte namn på `Version` till `Name` på `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1258">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="a52f3-1259">Bytte namn på `BlobSource` till `HttpUrl` på `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1259">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="a52f3-1260">Tog bort egenskapen `OSDisk` från `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1260">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="a52f3-1261">Tog bort **Set-AzBatchPoolOSVersion**.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1261">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="a52f3-1262">Den här åtgärden stöds inte längre.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1262">This operation is no longer supported.</span></span>
* <span data-ttu-id="a52f3-1263">`TargetOSVersion` har tagits bort från `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1263">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="a52f3-1264">Bytte namn på `CurrentOSVersion` till `OSVersion` på `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1264">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="a52f3-1265">`DataEgressGiB` och `DataIngressGiB` har tagits bort från `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1265">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="a52f3-1266">Tog bort **Get-AzBatchNodeAgentSku** och ersatte det med **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1266">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="a52f3-1267">**Get-AzBatchSupportedImage** returnerar samma data som **Get-AzBatchNodeAgentSku** men i ett mer användarvänligt format.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1267">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="a52f3-1268">Nya icke-verifierade avbildningar returneras nu också.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1268">New non-verified images are also now returned.</span></span> <span data-ttu-id="a52f3-1269">Ytterligare information om `Capabilities` och `BatchSupportEndOfLife` för varje avbildning inkluderas också.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1269">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="a52f3-1270">Lade till möjlighet att montera fjärrfilsystem på varje nod i en pool via den nya parametern `MountConfiguration` för **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1270">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="a52f3-1271">Har nu stöd för nätverkssäkerhetsregler som blockerar nätverksåtkomst till en pool baserat på källportens trafik.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1271">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="a52f3-1272">Detta görs via egenskapen `SourcePortRanges` på `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1272">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="a52f3-1273">När du kör en container stöder nu Batch körningen av uppgiften i arbetskatalogen för containern eller i arbetskatalogen för Batch-uppgiften.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1273">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="a52f3-1274">Detta styrs av egenskapen `WorkingDirectory` på `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1274">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="a52f3-1275">Lade till en funktion för att ange en samling av offentliga IP-adresser på `PSNetworkConfiguration` via den nya egenskapen `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1275">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="a52f3-1276">Detta garanterar att noderna i poolen har en IP-adress från listan över IP-adresser som tillhandahållits av användare.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1276">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="a52f3-1277">Om inget värde anges är standardvärdet för `WaitForSuccess` på `PSSTartTask` nu `$True` (var tidigare `$False`).</span><span class="sxs-lookup"><span data-stu-id="a52f3-1277">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="a52f3-1278">Om inget värde anges är standardvärdet för `Scope` på `PSAutoUserSpecification` nu `Pool` (var tidigare `Task` på Windows och `Pool` på Linux).</span><span class="sxs-lookup"><span data-stu-id="a52f3-1278">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="a52f3-1279">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="a52f3-1279">Az.Cdn</span></span>
* <span data-ttu-id="a52f3-1280">Introducerade UrlRewriteAction och CacheKeyQueryStringAction till RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1280">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="a52f3-1281">Åtgärdade flera buggar, som saknade indata för ”väljare” i cmdleten New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1281">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a52f3-1282">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a52f3-1282">Az.Compute</span></span>
* <span data-ttu-id="a52f3-1283">Funktion för diskkrypteringsuppsättning</span><span class="sxs-lookup"><span data-stu-id="a52f3-1283">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="a52f3-1284">Nya cmdletar:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="a52f3-1284">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="a52f3-1285">Parametern DiskEncryptionSetId har lagts till i följande cmdletar:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="a52f3-1285">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="a52f3-1286">Parametrarna DiskEncryptionSetId och EncryptionType har lagts till i följande cmdletar:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="a52f3-1286">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="a52f3-1287">Lägg till parametern PublicIPAddressVersion i New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="a52f3-1287">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="a52f3-1288">Flytta FileUris för anpassat skripttillägg från offentlig inställning till skyddad inställning</span><span class="sxs-lookup"><span data-stu-id="a52f3-1288">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="a52f3-1289">Lägg till ScaleInPolicy i cmdletarna New-AzVmss, New-AzVmssConfig och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a52f3-1289">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="a52f3-1290">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="a52f3-1290">Breaking changes</span></span>
    - <span data-ttu-id="a52f3-1291">Parametern UploadSizeInBytes används istället för DiskSizeGB för New-AzDiskConfig när CreateOption är Uppladdning</span><span class="sxs-lookup"><span data-stu-id="a52f3-1291">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="a52f3-1292">PublishingProfile.Source.ManagedImage.Id ersätts med StorageProfile.Source.Id i objektet GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="a52f3-1292">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a52f3-1293">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a52f3-1293">Az.DataFactory</span></span>
* <span data-ttu-id="a52f3-1294">Uppdatera ADF .Net SDK-versionen till 4.3.0</span><span class="sxs-lookup"><span data-stu-id="a52f3-1294">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a52f3-1295">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a52f3-1295">Az.DataLakeStore</span></span>
* <span data-ttu-id="a52f3-1296">Uppdatera ADLS SDK-version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) innehåller följande korrigeringar</span><span class="sxs-lookup"><span data-stu-id="a52f3-1296">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="a52f3-1297">Undvik att utlösa undantag när det inte går att deserialisera creationtime för inmatning av papperskorg eller katalog.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1297">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="a52f3-1298">Gör inställning tillgänglig per tidsgräns för förfrågan i adlsclient</span><span class="sxs-lookup"><span data-stu-id="a52f3-1298">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="a52f3-1299">Korrigera överföringen av ursprunglig syncflag för badoffset-återställning</span><span class="sxs-lookup"><span data-stu-id="a52f3-1299">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="a52f3-1300">Korrigera EnumerateDirectory för att hämta fortsättningstoken när svar har kontrollerats</span><span class="sxs-lookup"><span data-stu-id="a52f3-1300">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="a52f3-1301">Korrigera bugg i Concat</span><span class="sxs-lookup"><span data-stu-id="a52f3-1301">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="a52f3-1302">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="a52f3-1302">Az.FrontDoor</span></span>
* <span data-ttu-id="a52f3-1303">Åtgärdade diverse stavfel i modul</span><span class="sxs-lookup"><span data-stu-id="a52f3-1303">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="a52f3-1304">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a52f3-1304">Az.HDInsight</span></span>
* <span data-ttu-id="a52f3-1305">Korrigerade buggen att kunder får felet ”inte en giltig Base-64-sträng” vid användning av Get-AzHDInsightCluster för att hämta klustret med ADLSGen1-lagring.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1305">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="a52f3-1306">Lägg till en parameter med namnet ”ApplicationId” i de tre cmdletarna Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig och New-AzHDInsightCluster så att kunden kan tillhandahålla tjänstens huvudnamn för program-ID för åtkomst till Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1306">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="a52f3-1307">Ändrade Microsoft.Azure.Management.HDInsight från 2.1.0 till 5.1.0</span><span class="sxs-lookup"><span data-stu-id="a52f3-1307">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="a52f3-1308">Fem cmdletar har tagits bort:</span><span class="sxs-lookup"><span data-stu-id="a52f3-1308">Removed five cmdlets:</span></span>
    - <span data-ttu-id="a52f3-1309">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="a52f3-1309">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="a52f3-1310">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="a52f3-1310">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="a52f3-1311">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="a52f3-1311">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="a52f3-1312">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="a52f3-1312">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="a52f3-1313">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="a52f3-1313">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="a52f3-1314">Tre cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="a52f3-1314">Added three cmdlets:</span></span>
    - <span data-ttu-id="a52f3-1315">Get-AzHDInsightMonitoring som ersätter Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1315">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="a52f3-1316">Enable-AzHDInsightMonitoring som ersätter Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1316">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="a52f3-1317">Disable-AzHDInsightMonitoring som ersätter Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1317">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="a52f3-1318">Korrigerade cmdleten Get-AzHDInsightProperties för att stödja hämtning av funktionsinformation från en viss plats.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1318">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="a52f3-1319">Parameteruppsättningarna (Spark1 och Spark2) har tagits bort från Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1319">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="a52f3-1320">Lägg till exempel för cmdleten Add-AzHDInsightSecurityProfile till hjälpdokumenten.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1320">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="a52f3-1321">Ändrade utdatatyp för följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="a52f3-1321">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="a52f3-1322">Ändrade utdatatyp för Get-AzHDInsightProperties från CapabilitiesResponse till AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1322">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="a52f3-1323">Ändrade utdatatyp för Remove-AzHDInsightCluster från ClusterGetResponse till bool.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1323">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="a52f3-1324">Ändrade utdatatyp för Set-AzHDInsightGatewaySettings HttpConnectivitySettings till GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1324">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="a52f3-1325">Lade till testfall för vissa scenarier.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1325">Added some scenario test cases.</span></span>
* <span data-ttu-id="a52f3-1326">Ta bort vissa alias: Add-AzHDInsightConfigValues, Get-AzHDInsightProperties.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1326">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a52f3-1327">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a52f3-1327">Az.IotHub</span></span>
* <span data-ttu-id="a52f3-1328">Icke-bakåtkompatibla ändringar:</span><span class="sxs-lookup"><span data-stu-id="a52f3-1328">Breaking changes:</span></span>
    - <span data-ttu-id="a52f3-1329">Cmdleten Add-AzIotHubEventHubConsumerGroup har inte längre stöd för parametern EventHubEndpointName och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1329">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="a52f3-1330">Parameteruppsättningen __AllParameterSets för cmdleten Add-AzIotHubEventHubConsumerGroup har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1330">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="a52f3-1331">Cmdleten Get-AzIotHubEventHubConsumerGroup har inte längre stöd för parametern EventHubEndpointName och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1331">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="a52f3-1332">Parameteruppsättningen __AllParameterSets för cmdleten Get-AzIotHubEventHubConsumerGroup har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1332">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="a52f3-1333">Egenskapen OperationsMonitoringProperties av typen Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1333">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="a52f3-1334">Egenskapen OperationsMonitoringProperties av typen Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1334">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="a52f3-1335">Cmdleten New-AzIotHubExportDevice stöder inte längre aliaset New-AzIotHubExportDevices.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1335">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="a52f3-1336">Cmdleten New-AzIotHubImportDevice stöder inte längre aliaset New-AzIotHubImportDevices.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1336">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="a52f3-1337">Cmdleten Remove-AzIotHubEventHubConsumerGroup har inte längre stöd för parametern EventHubEndpointName och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1337">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="a52f3-1338">Parameteruppsättningen __AllParameterSets för cmdleten Remove-AzIotHubEventHubConsumerGroup har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1338">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="a52f3-1339">Cmdleten Set-AzIotHub har inte längre stöd för parametern OperationsMonitoringProperties och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1339">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="a52f3-1340">Parameteruppsättningen UpdateOperationsMonitoringProperties för cmdleten Set-AzIotHub har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1340">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a52f3-1341">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a52f3-1341">Az.RecoveryServices</span></span>
* <span data-ttu-id="a52f3-1342">Azure Site Recovery-stöd för att konfigurera nätverksresurser som NSG, offentliga IP-adresser och interna lastbalanserare för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1342">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="a52f3-1343">Azure Site Recovery-stöd för att skriva till hanterad disk för vMWare till Azure.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1343">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="a52f3-1344">Azure Site Recovery-stöd för NIC-reduktion för vMWare till Azure.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1344">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="a52f3-1345">Azure Site Recovery-stöd för accelererat nätverk för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1345">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="a52f3-1346">Azure Site Recovery-stöd för automatisk uppdatering av agent för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1346">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="a52f3-1347">Azure Site Recovery-stöd för Standard SSD för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1347">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="a52f3-1348">Azure Site Recovery-stöd för tvåstegskryptering i Azure Disk Encryption för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1348">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="a52f3-1349">Azure Site Recovery-stöd för att skydda nyligen tillagda diskar för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1349">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="a52f3-1350">En funktion för mjuk borttagning av virtuella datorer samt tester för mjuk borttagning har tagits bort</span><span class="sxs-lookup"><span data-stu-id="a52f3-1350">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="a52f3-1351">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a52f3-1351">Az.Resources</span></span>
* <span data-ttu-id="a52f3-1352">Uppdatera beroendesammansättning för Microsoft.Extensions.Caching.Memory från 1.1.1 till 2.2</span><span class="sxs-lookup"><span data-stu-id="a52f3-1352">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a52f3-1353">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a52f3-1353">Az.Network</span></span>
* <span data-ttu-id="a52f3-1354">Ändra alla cmdletar för PrivateEndpointConnection så att de stöder generiska tjänstleverantörer.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1354">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="a52f3-1355">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="a52f3-1355">Updated cmdlet:</span></span>
        - <span data-ttu-id="a52f3-1356">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a52f3-1356">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="a52f3-1357">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a52f3-1357">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="a52f3-1358">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a52f3-1358">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="a52f3-1359">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a52f3-1359">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="a52f3-1360">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a52f3-1360">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="a52f3-1361">Lägg till ny cmdlet för PrivateLinkResource så att det också stöder generiska tjänstleverantörer.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1361">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="a52f3-1362">Ny cmdlet:</span><span class="sxs-lookup"><span data-stu-id="a52f3-1362">New cmdlet:</span></span>
        - <span data-ttu-id="a52f3-1363">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="a52f3-1363">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="a52f3-1364">Lägg till nya fält och parametrar för funktionen Proxy Protocol V2.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1364">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="a52f3-1365">Lägg till egenskapen EnableProxyProtocol i PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="a52f3-1365">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="a52f3-1366">Lägg till egenskapen LinkIdentifier i PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a52f3-1366">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="a52f3-1367">Uppdaterade New-AzPrivateLinkService för att lägga till den nya valfria parametern EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1367">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="a52f3-1368">Korrigera felaktig beskrivning av parameter i referensdokumentationen för New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="a52f3-1368">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="a52f3-1369">Nya cmdletar som stöder Azure-brandväggsprincipen</span><span class="sxs-lookup"><span data-stu-id="a52f3-1369">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="a52f3-1370">Lägg till stöd för den underordnade resursen RouteTables för VirtualHub</span><span class="sxs-lookup"><span data-stu-id="a52f3-1370">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="a52f3-1371">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="a52f3-1371">New cmdlets added:</span></span>
        - <span data-ttu-id="a52f3-1372">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="a52f3-1372">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="a52f3-1373">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="a52f3-1373">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="a52f3-1374">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="a52f3-1374">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="a52f3-1375">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="a52f3-1375">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="a52f3-1376">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="a52f3-1376">Set-AzVirtualHub</span></span>
* <span data-ttu-id="a52f3-1377">Lägg till stöd för ny egenskaps-SKU för VirtualHub och VirtualWANType för VirtualWan</span><span class="sxs-lookup"><span data-stu-id="a52f3-1377">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="a52f3-1378">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="a52f3-1378">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="a52f3-1379">New-AzVirtualHub: lade till parameter-SKU</span><span class="sxs-lookup"><span data-stu-id="a52f3-1379">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="a52f3-1380">Update-AzVirtualHub: lade till parameter-SKU</span><span class="sxs-lookup"><span data-stu-id="a52f3-1380">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="a52f3-1381">New-AzVirtualWan: lade till parametern VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="a52f3-1381">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="a52f3-1382">Update-AzVirtualWan: lade till parametern VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="a52f3-1382">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="a52f3-1383">Lägg till stöd för egenskapen EnableInternetSecurity för HubVnetConnection, VpnConnection och ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="a52f3-1383">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="a52f3-1384">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="a52f3-1384">New cmdlets added:</span></span>
        - <span data-ttu-id="a52f3-1385">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="a52f3-1385">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="a52f3-1386">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="a52f3-1386">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="a52f3-1387">New-AzureRmVirtualHubVnetConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="a52f3-1387">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="a52f3-1388">New-AzureRmVpnConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="a52f3-1388">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="a52f3-1389">Update-AzureRmVpnConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="a52f3-1389">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="a52f3-1390">New-AzureRmExpressRouteConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="a52f3-1390">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="a52f3-1391">Set-AzureRmExpressRouteConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="a52f3-1391">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="a52f3-1392">Lägg till stöd för att konfigurera TopLevel WebApplicationFirewall-princip</span><span class="sxs-lookup"><span data-stu-id="a52f3-1392">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="a52f3-1393">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="a52f3-1393">New cmdlets added:</span></span>
        - <span data-ttu-id="a52f3-1394">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="a52f3-1394">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="a52f3-1395">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="a52f3-1395">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="a52f3-1396">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="a52f3-1396">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="a52f3-1397">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="a52f3-1397">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="a52f3-1398">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="a52f3-1398">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="a52f3-1399">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="a52f3-1399">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="a52f3-1400">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="a52f3-1400">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="a52f3-1401">New-AzApplicationGatewayFirewallPolicy: parametrarna PolicySetting, ManagedRule har lagts till</span><span class="sxs-lookup"><span data-stu-id="a52f3-1401">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="a52f3-1402">Stöd för operator för geomatchning har lagts till på CustomRule</span><span class="sxs-lookup"><span data-stu-id="a52f3-1402">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="a52f3-1403">Geomatchning har lagts till i operatorn på FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="a52f3-1403">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="a52f3-1404">Stöd har lagts till för brandväggsprinciperna perListener och perSite</span><span class="sxs-lookup"><span data-stu-id="a52f3-1404">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="a52f3-1405">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="a52f3-1405">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="a52f3-1406">New-AzApplicationGatewayHttpListener: parametrarna FirewallPolicy, FirewallPolicyId har lagts till</span><span class="sxs-lookup"><span data-stu-id="a52f3-1406">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="a52f3-1407">New-AzApplicationGatewayPathRuleConfig: parametrarna FirewallPolicy, FirewallPolicyId har lagts till</span><span class="sxs-lookup"><span data-stu-id="a52f3-1407">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="a52f3-1408">Åtgärdat så att nödvändigt undernät med namnet AzureBastionSubnet i PSBastion kan vara skiftlägesokänsligt</span><span class="sxs-lookup"><span data-stu-id="a52f3-1408">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="a52f3-1409">Stöd för mål-FQDN:er i nätverksregler och översatt FQDN i NAT-regler för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="a52f3-1409">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="a52f3-1410">Lägg till stöd för resursen RouteTables för IpGroup på den högsta nivån</span><span class="sxs-lookup"><span data-stu-id="a52f3-1410">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="a52f3-1411">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="a52f3-1411">New cmdlets added:</span></span>
        - <span data-ttu-id="a52f3-1412">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="a52f3-1412">New-AzIpGroup</span></span>
        - <span data-ttu-id="a52f3-1413">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="a52f3-1413">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="a52f3-1414">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="a52f3-1414">Get-AzIpGroup</span></span>
        - <span data-ttu-id="a52f3-1415">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="a52f3-1415">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a52f3-1416">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a52f3-1416">Az.ServiceFabric</span></span>
* <span data-ttu-id="a52f3-1417">Ta bort cmdleten Add-AzServiceFabricApplicationCertificate eftersom det här scenariot omfattas av Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1417">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="a52f3-1418">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a52f3-1418">Az.Sql</span></span>
* <span data-ttu-id="a52f3-1419">Stöd har lagts till för återställning av utelämnade databaser på hanterade instanser.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1419">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="a52f3-1420">Inaktuella gamla cmdletar för granskning från kod.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1420">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="a52f3-1421">Tog bort inaktuella alias:</span><span class="sxs-lookup"><span data-stu-id="a52f3-1421">Removed deprecated aliases:</span></span>
* <span data-ttu-id="a52f3-1422">Get-AzSqlDatabaseIndexRecommendations (använd Get-AzSqlDatabaseIndexRecommendation istället)</span><span class="sxs-lookup"><span data-stu-id="a52f3-1422">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="a52f3-1423">Get-AzSqlDatabaseRestorePoints (använd Get-AzSqlDatabaseRestorePoint istället)</span><span class="sxs-lookup"><span data-stu-id="a52f3-1423">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="a52f3-1424">Ta bort cmdleten Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="a52f3-1424">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="a52f3-1425">Ta bort alias för inaktuella cmdletar för inställningar för utvärdering av säkerhetsrisk</span><span class="sxs-lookup"><span data-stu-id="a52f3-1425">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="a52f3-1426">Inaktualisera cmdletar för inställningar för avancerad hotidentifiering</span><span class="sxs-lookup"><span data-stu-id="a52f3-1426">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="a52f3-1427">Lägga till cmdletar för att inaktivera och aktivera känslighetsrekommendationer på kolumner i en databas.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1427">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a52f3-1428">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a52f3-1428">Az.Storage</span></span>
* <span data-ttu-id="a52f3-1429">Stöd för att aktivera stora filresurser vid skapande eller uppdatering av lagringskonto</span><span class="sxs-lookup"><span data-stu-id="a52f3-1429">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="a52f3-1430">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a52f3-1430">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="a52f3-1431">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a52f3-1431">Set-AzStorageAccount</span></span>
* <span data-ttu-id="a52f3-1432">När du stänger/hämtar en filreferens kan du hoppa över kontrollen av huruvida indatasökvägen är en filkatalog eller en fil för att undvika problem med objekt som har status DeletePending</span><span class="sxs-lookup"><span data-stu-id="a52f3-1432">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="a52f3-1433">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="a52f3-1433">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="a52f3-1434">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="a52f3-1434">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="a52f3-1435">2.8.0 – oktober 2019</span><span class="sxs-lookup"><span data-stu-id="a52f3-1435">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="a52f3-1436">Allmänt</span><span class="sxs-lookup"><span data-stu-id="a52f3-1436">General</span></span>
* <span data-ttu-id="a52f3-1437">AZ. HealthcareApis 1.0.0-version</span><span class="sxs-lookup"><span data-stu-id="a52f3-1437">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="a52f3-1438">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a52f3-1438">Az.Accounts</span></span>
* <span data-ttu-id="a52f3-1439">Uppdatera telemetri och URL-omskrivning för genererade moduler, korrigera Windows-enhetstester.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1439">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="a52f3-1440">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a52f3-1440">Az.ApiManagement</span></span>
* <span data-ttu-id="a52f3-1441">**Set-AzApiManagementApi** – Tillagt stöd för att uppdatera Api till ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="a52f3-1441">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="a52f3-1442">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="a52f3-1442">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a52f3-1443">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a52f3-1443">Az.Automation</span></span>
* <span data-ttu-id="a52f3-1444">Åtgärdade cmdleten New-AzureAutomationSoftwareUpdateConfiguration för parametern för inställning av Linux-omstart.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1444">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="a52f3-1445">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="a52f3-1445">Az.Batch</span></span>
* <span data-ttu-id="a52f3-1446">**Get-AzBatchNodeAgentSku** är inaktuell och ersätts av **Get-AzBatchSupportImage** i version 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1446">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a52f3-1447">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a52f3-1447">Az.Compute</span></span>
* <span data-ttu-id="a52f3-1448">Lägg till parametrarna Priority, EvictionPolicy och MaxPrice till cmdletarna New-AzVM och New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a52f3-1448">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="a52f3-1449">Korrigera varningsmeddelande och hjälpdokument för cmdletarna Add-AzVMAdditionalUnattendContent och Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="a52f3-1449">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="a52f3-1450">Åtgärda – skipVmBackup-undantag för virtuella Linux-datorer med hanterade diskar för Set-AzVMDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1450">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="a52f3-1451">Åtgärda fel i uppdatera krypteringsinställningarna i set-AzVMDiskEncryptionExtension, scenario i två steg.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1451">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a52f3-1452">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a52f3-1452">Az.DataFactory</span></span>
* <span data-ttu-id="a52f3-1453">Lägga till CRUD-kommandon för ADF V2-dataflödet: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow och Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1453">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="a52f3-1454">Lägger till åtgärdskommandon för ADF V2-dataflödesfelsökningssession: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand och Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1454">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="a52f3-1455">Uppdatera ADF .Net SDK-versionen till 4.2.0</span><span class="sxs-lookup"><span data-stu-id="a52f3-1455">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a52f3-1456">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a52f3-1456">Az.DataLakeStore</span></span>
* <span data-ttu-id="a52f3-1457">Korrigera kontovalidering så att konton med ”-” kan skickas utan domän</span><span class="sxs-lookup"><span data-stu-id="a52f3-1457">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="a52f3-1458">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="a52f3-1458">Az.HealthcareApis</span></span>
* <span data-ttu-id="a52f3-1459">PowerShell-versionen har uppdaterats till 1.0.0</span><span class="sxs-lookup"><span data-stu-id="a52f3-1459">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="a52f3-1460">Uppdaterade SDK-versionen till 1.0.2</span><span class="sxs-lookup"><span data-stu-id="a52f3-1460">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="a52f3-1461">Uppdatera i tester för att referera till en ny SDK-version</span><span class="sxs-lookup"><span data-stu-id="a52f3-1461">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="a52f3-1462">Utdatastrukturen har uppdaterats från kapslad till förenklad.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1462">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a52f3-1463">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a52f3-1463">Az.IotHub</span></span>
* <span data-ttu-id="a52f3-1464">Lägg till ny routningskälla: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="a52f3-1464">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="a52f3-1465">Mindre felkorrigering: Get-AzIothub returnerar inte subscriptionId</span><span class="sxs-lookup"><span data-stu-id="a52f3-1465">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a52f3-1466">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a52f3-1466">Az.Monitor</span></span>
* <span data-ttu-id="a52f3-1467">Nya åtgärdsgruppsmottagare har lagts till för åtgärdsgrupp   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="a52f3-1467">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="a52f3-1468">Använd vanligt aviseringsschema som är aktiverat för mottagarna.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1468">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="a52f3-1469">Detta gäller inte för SMS, push för Azure-app, ITSM och röstmottagare</span><span class="sxs-lookup"><span data-stu-id="a52f3-1469">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="a52f3-1470">Webhooks har nu stöd för Azure Active Directory-autentisering.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1470">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a52f3-1471">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a52f3-1471">Az.Network</span></span>
* <span data-ttu-id="a52f3-1472">Lägg till ny cmdlet Get-AzAvailableServiceAlias som kan anropas för att hämta de alias som kan användas för tjänstslutpunktsprinciper.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1472">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="a52f3-1473">Stöd för tillägg av trafikväljare har lagts till i gatewayanslutningar för virtuella nätverk</span><span class="sxs-lookup"><span data-stu-id="a52f3-1473">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="a52f3-1474">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="a52f3-1474">New cmdlets added:</span></span>
        - <span data-ttu-id="a52f3-1475">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="a52f3-1475">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="a52f3-1476">Cmdletar har uppdaterats med valfri parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="a52f3-1476">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="a52f3-1477">Lägg till stöd för ESP- och AH-protokoll i konfiguration av nätverkssäkerhetsregler</span><span class="sxs-lookup"><span data-stu-id="a52f3-1477">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="a52f3-1478">Uppdaterade cmdletar:</span><span class="sxs-lookup"><span data-stu-id="a52f3-1478">Updated cmdlets:</span></span>
        - <span data-ttu-id="a52f3-1479">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a52f3-1479">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="a52f3-1480">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a52f3-1480">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="a52f3-1481">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a52f3-1481">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="a52f3-1482">Förbättra hanteringen av undantag i Cortex-cmdletar</span><span class="sxs-lookup"><span data-stu-id="a52f3-1482">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="a52f3-1483">Nya generationer och SKU:er för VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="a52f3-1483">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="a52f3-1484">Introducera nya generationer för VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1484">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="a52f3-1485">Introducera nya SKU:er med högt dataflöde för VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1485">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="a52f3-1486">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="a52f3-1486">Az.RedisCache</span></span>
* <span data-ttu-id="a52f3-1487">Uppdaterad referensdokumentation för ”set-AzRedisCache” för att inkludera saknade värden för parametern ”size”</span><span class="sxs-lookup"><span data-stu-id="a52f3-1487">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="a52f3-1488">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a52f3-1488">Az.Sql</span></span>
* <span data-ttu-id="a52f3-1489">Lägg till stöd för inställningen Active Directory administratör på den hanterade instansen</span><span class="sxs-lookup"><span data-stu-id="a52f3-1489">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a52f3-1490">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a52f3-1490">Az.Storage</span></span>
* <span data-ttu-id="a52f3-1491">Uppdatera Lagringsklientbibliotek till 11.1.0</span><span class="sxs-lookup"><span data-stu-id="a52f3-1491">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="a52f3-1492">Lista containrar med hanteringsplans-API, kommer att listas med NextPageLink</span><span class="sxs-lookup"><span data-stu-id="a52f3-1492">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="a52f3-1493">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="a52f3-1493">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="a52f3-1494">Lista lagringskonton från prenumerationen, kommer att listas med NextPageLink</span><span class="sxs-lookup"><span data-stu-id="a52f3-1494">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="a52f3-1495">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a52f3-1495">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="a52f3-1496">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="a52f3-1496">Az.StorageSync</span></span>
* <span data-ttu-id="a52f3-1497">Åtgärda problemet 9810 i Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1497">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a52f3-1498">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a52f3-1498">Az.Websites</span></span>
* <span data-ttu-id="a52f3-1499">Set-AzWebApp – uppdatering av ASP för en app misslyckades</span><span class="sxs-lookup"><span data-stu-id="a52f3-1499">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="a52f3-1500">2.7.0 – september 2019</span><span class="sxs-lookup"><span data-stu-id="a52f3-1500">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="a52f3-1501">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a52f3-1501">Az.ApiManagement</span></span>
* <span data-ttu-id="a52f3-1502">Uppdatera ”-Format”-parameterbeskrivningen i ”Set-AzApiManagementPolicy”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="a52f3-1502">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="a52f3-1503">Referenser för den föråldrade cmdleten ”Update-AzApiManagementDeployment” har tagits bort från referensdokumentationen.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1503">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="a52f3-1504">Använd ”Set-AzApiManagement” i stället.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1504">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a52f3-1505">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a52f3-1505">Az.Automation</span></span>
* <span data-ttu-id="a52f3-1506">Stavfel har korrigerats i exempel i referensdokumentationen för ”Register-AzAutomationDscNode”</span><span class="sxs-lookup"><span data-stu-id="a52f3-1506">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="a52f3-1507">Klargörande har lagts till om OS-begränsningar för Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="a52f3-1507">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="a52f3-1508">Null-referensundantag har korrigerats för -Wait-alternativet i Start-AzAutomationRunbook-cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1508">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a52f3-1509">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a52f3-1509">Az.Compute</span></span>
* <span data-ttu-id="a52f3-1510">Lägg till UploadSizeInBytes-parameter till New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="a52f3-1510">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="a52f3-1511">Lägg till Incremental-parameter till New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="a52f3-1511">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="a52f3-1512">Lägg till en funktion för virtuella datorer med låg prioritet:</span><span class="sxs-lookup"><span data-stu-id="a52f3-1512">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="a52f3-1513">MaxPrice-, EvictionPolicy- och Priority-parametrar har lagts till i New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1513">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="a52f3-1514">MaxPrice-parametern har lagts till i New-AzVmssConfig-, Update-AzVM- och Update-AzVmss-cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1514">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="a52f3-1515">Åtgärda problem med VM-referenser för Get-AzAvailabilitySet-cmdleten när alla tillgänglighetsuppsättningar i prenumerationen visas.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1515">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="a52f3-1516">Korrigera null-undantaget för Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1516">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="a52f3-1517">Korrigera VHD-metoden för sökning relativt till slut.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1517">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="a52f3-1518">Åtgärda UltraSSD-problem för New-AzVM och Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1518">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a52f3-1519">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a52f3-1519">Az.DataFactory</span></span>
* <span data-ttu-id="a52f3-1520">Lägger till 3 nya kommandon för ADF V2 – Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription och Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="a52f3-1520">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="a52f3-1521">ADF .Net SDK har uppdaterats till 4.1.3</span><span class="sxs-lookup"><span data-stu-id="a52f3-1521">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="a52f3-1522">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a52f3-1522">Az.HDInsight</span></span>
* <span data-ttu-id="a52f3-1523">Anrop för icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="a52f3-1523">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a52f3-1524">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a52f3-1524">Az.IotHub</span></span>
* <span data-ttu-id="a52f3-1525">Lägg till stöd för att anropa redundans för en IotHub till den geo-länkade katastrofåterställningsregionen.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1525">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="a52f3-1526">Lägg till stöd för att hantera meddelandeberikning för en IotHub.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1526">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="a52f3-1527">Nya cmdlet:ar är:</span><span class="sxs-lookup"><span data-stu-id="a52f3-1527">New cmdlets are:</span></span>
    - <span data-ttu-id="a52f3-1528">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="a52f3-1528">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="a52f3-1529">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="a52f3-1529">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="a52f3-1530">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="a52f3-1530">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="a52f3-1531">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="a52f3-1531">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a52f3-1532">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a52f3-1532">Az.Monitor</span></span>
* <span data-ttu-id="a52f3-1533">Pekar på den senaste Monitor SDK:n, dvs. 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="a52f3-1533">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="a52f3-1534">Lägger till bakåtkompatibla ändringar i Metrics-cmdletarna, dvs. enhetsuppräkningen stöder flera nya värden.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1534">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="a52f3-1535">Detta är skrivskyddade cmdletar, så det förekommer inga ändringar i inmatningen för cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1535">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="a52f3-1536">API-versionen för **ActionGroups**-begäranden är nu **2019-06-01**. Tidigare var den **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1536">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="a52f3-1537">Test av scenarier har uppdaterats för att anpassas till den här ändringen.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1537">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="a52f3-1538">Ett nytt obligatoriskt argument har lagts till för konstruktorerna för klasserna **EmailReceiver** och **WebhookReceiver** – ett booleskt värde med namnet **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1538">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="a52f3-1539">Värdet är för närvarande fast till **false** så att den här icke-bakåtkompatibla ändringen är dold från cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1539">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="a52f3-1540">**Obs!** Det här är en tillfällig ändring som måste verifieras av Alerts-teamet.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1540">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="a52f3-1541">Ordningen på argumenten för konstruktorn för klassen **Source** (relaterad till klassen **ScheduledQueryRuleSource**) har ändrats från den tidigare SDK:n.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1541">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="a52f3-1542">Den här ändringen krävde korrigering av två enhetstest: de kompilerades, men testerna skickades inte.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1542">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="a52f3-1543">Ordningen på argumenten för konstruktorn för klassen **AlertingAction** (relaterad till klassen **ScheduledQueryRuleSource**) har ändrats från den tidigare SDK:n.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1543">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="a52f3-1544">Den här ändringen krävde korrigering av två enhetstest: de kompilerades, men testerna skickades inte.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1544">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="a52f3-1545">Stöd för kriterier för dynamiskt tröskelvärde för måttavisering v2</span><span class="sxs-lookup"><span data-stu-id="a52f3-1545">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="a52f3-1546">New-AzMetricAlertRuleV2Criteria: skapar nu även kriterier för dynamiskt tröskelvärde</span><span class="sxs-lookup"><span data-stu-id="a52f3-1546">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="a52f3-1547">Add-AzMetricAlertRuleV2: accepterar nu även kriterier för dynamiskt tröskelvärde</span><span class="sxs-lookup"><span data-stu-id="a52f3-1547">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="a52f3-1548">Förbättringar i schemalagd frågeregel (SQR)</span><span class="sxs-lookup"><span data-stu-id="a52f3-1548">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="a52f3-1549">Cmdletar accepterar ”Location”-parameter i båda formaten, antingen platsen (t.ex. eastus) eller platsens visningsnamn (t.ex. USA, östra)</span><span class="sxs-lookup"><span data-stu-id="a52f3-1549">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="a52f3-1550">”Enabled”-parametern illustreras korrekt i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="a52f3-1550">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="a52f3-1551">Exempel för den valfria parametern ”ActionGroup” har lagts till</span><span class="sxs-lookup"><span data-stu-id="a52f3-1551">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="a52f3-1552">Förbättrade hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="a52f3-1552">Overall improved help files</span></span>
* <span data-ttu-id="a52f3-1553">Åtgärda bugg då omfattningstypen fastställs för ”Set-AzActionRule”</span><span class="sxs-lookup"><span data-stu-id="a52f3-1553">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a52f3-1554">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a52f3-1554">Az.Network</span></span>
* <span data-ttu-id="a52f3-1555">Korrigera felaktigt exempel i referensdokumentationen för ”New-AzApplicationGateway”</span><span class="sxs-lookup"><span data-stu-id="a52f3-1555">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="a52f3-1556">Lägg till anmärkning i ”Get-AzNetworkWatcherPacketCapture”-referensdokumentationen om hämtning av alla egenskaper för en paketinsamling</span><span class="sxs-lookup"><span data-stu-id="a52f3-1556">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="a52f3-1557">Exempel har korrigerats i ”Test-AzNetworkWatcherIPFlow”-referensdokumentationen för korrekt uppräkning av nätverkskort</span><span class="sxs-lookup"><span data-stu-id="a52f3-1557">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="a52f3-1558">Förbättrad tolkning av molnundantag för att visa eventuell ytterligare information</span><span class="sxs-lookup"><span data-stu-id="a52f3-1558">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="a52f3-1559">Förbättrad tolkning av molnundantag för att hantera ytterligare en typ av SDK-undantag</span><span class="sxs-lookup"><span data-stu-id="a52f3-1559">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="a52f3-1560">Felaktig mappning av säkerhetsregelmodeller har korrigerats</span><span class="sxs-lookup"><span data-stu-id="a52f3-1560">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="a52f3-1561">Egenskaper har lagts till för nätverksgränssnittet för funktionen Privat IP</span><span class="sxs-lookup"><span data-stu-id="a52f3-1561">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="a52f3-1562">Egenskapen ”PrivateEndpoint” har lagts till som en typ av PSResourceId till PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="a52f3-1562">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="a52f3-1563">Egenskapen ”PrivateLinkConnectionProperties” har lagts till som en typ av PSIpConfigurationConnectivityInformation till PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="a52f3-1563">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="a52f3-1564">Modellklassen PSIpConfigurationConnectivityInformation har lagts till</span><span class="sxs-lookup"><span data-stu-id="a52f3-1564">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="a52f3-1565">ApplicationRuleProtocolType ”mssql” har lagts till för Azure Firewall-resurs</span><span class="sxs-lookup"><span data-stu-id="a52f3-1565">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="a52f3-1566">MultiLink-stöd i virtuellt WAN</span><span class="sxs-lookup"><span data-stu-id="a52f3-1566">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="a52f3-1567">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="a52f3-1567">New cmdlets</span></span>
        - <span data-ttu-id="a52f3-1568">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="a52f3-1568">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="a52f3-1569">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="a52f3-1569">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="a52f3-1570">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="a52f3-1570">Updated cmdlet:</span></span>
        - <span data-ttu-id="a52f3-1571">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="a52f3-1571">New-VpnSite</span></span>
        - <span data-ttu-id="a52f3-1572">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="a52f3-1572">Update-VpnSite</span></span>
        - <span data-ttu-id="a52f3-1573">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="a52f3-1573">New-VpnConnection</span></span>
        - <span data-ttu-id="a52f3-1574">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="a52f3-1574">Update-VpnConnection</span></span>
* <span data-ttu-id="a52f3-1575">Dokument för vissa PowerShell-exempel har korrigerats så att Az-cmdletar används i stället för AzureRM-cmdletar</span><span class="sxs-lookup"><span data-stu-id="a52f3-1575">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a52f3-1576">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a52f3-1576">Az.RecoveryServices</span></span>
* <span data-ttu-id="a52f3-1577">Uppdatera AzureVMpolicy-objekt med ProtectedItemsCount-attribut</span><span class="sxs-lookup"><span data-stu-id="a52f3-1577">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="a52f3-1578">Ytterligare tester har lagts till för VM-princip och återställning av ursprungligt lagringskonto</span><span class="sxs-lookup"><span data-stu-id="a52f3-1578">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="a52f3-1579">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a52f3-1579">Az.Resources</span></span>
* <span data-ttu-id="a52f3-1580">Åtgärda fel där det inte gick att anropa New-AzRoleAssignment utan parametern Scope.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1580">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a52f3-1581">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a52f3-1581">Az.ServiceFabric</span></span>
* <span data-ttu-id="a52f3-1582">Stavfel har korrigerats i exempel för ”Update-AzServiceFabricReliability”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="a52f3-1582">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="a52f3-1583">Lägger till nya cmdletar för att hantera program och tjänster:</span><span class="sxs-lookup"><span data-stu-id="a52f3-1583">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="a52f3-1584">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="a52f3-1584">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="a52f3-1585">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="a52f3-1585">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="a52f3-1586">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="a52f3-1586">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="a52f3-1587">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="a52f3-1587">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="a52f3-1588">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="a52f3-1588">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="a52f3-1589">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="a52f3-1589">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="a52f3-1590">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="a52f3-1590">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="a52f3-1591">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="a52f3-1591">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="a52f3-1592">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="a52f3-1592">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="a52f3-1593">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="a52f3-1593">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="a52f3-1594">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="a52f3-1594">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="a52f3-1595">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="a52f3-1595">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="a52f3-1596">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="a52f3-1596">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="a52f3-1597">Service Fabric SDK har uppgraderats till version 1.2.0 som använder Service Fabric-resursprovidern med API-version 2019-03-01.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1597">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="a52f3-1598">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="a52f3-1598">Az.SignalR</span></span>
* <span data-ttu-id="a52f3-1599">Lägg till Update-, Restart-, CheckNameAvailability- och GetUsage-cmdletar</span><span class="sxs-lookup"><span data-stu-id="a52f3-1599">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="a52f3-1600">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a52f3-1600">Az.Sql</span></span>
* <span data-ttu-id="a52f3-1601">Uppdatera exempel i referensdokumentationen för ”Get-AzSqlElasticPool”</span><span class="sxs-lookup"><span data-stu-id="a52f3-1601">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="a52f3-1602">vCore-exempel för att skapa en elastisk pool (New-AzSqlElasticPool) har lagts till.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1602">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="a52f3-1603">Ta bort verifieringen av EmailAddresses och kontrollen som bekräftar att EmailAdmins inte är falskt när EmailAddresses är tomt i Set-AzSqlServerAdvancedThreatProtectionPolicy och Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="a52f3-1603">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="a52f3-1604">Server-/databasgranskningsinställningar kan tas bort när det finns flera diagnostikinställningar som aktiverar granskningskategorin.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1604">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="a52f3-1605">Åtgärda verifiering av e-postadresser i flera Sql Vulnerability Assessment-cmdletar (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting och Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="a52f3-1605">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a52f3-1606">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a52f3-1606">Az.Storage</span></span>
* <span data-ttu-id="a52f3-1607">Exempel i referensdokumentationen för ”Get-AzStorageAccountKey” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="a52f3-1607">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="a52f3-1608">Vid upp- och nedladdning av en Azure-fil kan SMB-egenskaperna för källfilen (t.ex. filattribut, tidpunkten då filen skapades och tidpunkten för den senaste skrivningen) sparas i målfilen</span><span class="sxs-lookup"><span data-stu-id="a52f3-1608">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="a52f3-1609">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="a52f3-1609">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="a52f3-1610">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="a52f3-1610">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="a52f3-1611">Korrigera problem med uppladdningen av blockblob med egenskaper/metadata för ImmutabilityPolicy i containrar.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1611">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="a52f3-1612">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="a52f3-1612">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="a52f3-1613">Stöd för hantering av Azure-filresurser med API för hanteringsplan</span><span class="sxs-lookup"><span data-stu-id="a52f3-1613">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="a52f3-1614">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="a52f3-1614">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="a52f3-1615">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="a52f3-1615">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="a52f3-1616">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="a52f3-1616">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="a52f3-1617">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="a52f3-1617">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a52f3-1618">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a52f3-1618">Az.Websites</span></span>
* <span data-ttu-id="a52f3-1619">Åtgärdar problemet där webapp-taggar togs bort när appen migrerades till nya ASP</span><span class="sxs-lookup"><span data-stu-id="a52f3-1619">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="a52f3-1620">Åtgärda Publish-AzureWebapp så att det fungerar i Linux och Windows</span><span class="sxs-lookup"><span data-stu-id="a52f3-1620">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="a52f3-1621">Uppdatera exempel i ”Get-AzWebAppPublishingProfile”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="a52f3-1621">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="a52f3-1622">2.6.0 – augusti 2019</span><span class="sxs-lookup"><span data-stu-id="a52f3-1622">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="a52f3-1623">Allmänt</span><span class="sxs-lookup"><span data-stu-id="a52f3-1623">General</span></span>
* <span data-ttu-id="a52f3-1624">Åtgärdade diverse skrivfel i flera moduler</span><span class="sxs-lookup"><span data-stu-id="a52f3-1624">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="a52f3-1625">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a52f3-1625">Az.Accounts</span></span>
* <span data-ttu-id="a52f3-1626">Stöd för användartilldelat MSI i Azure Functions-autentisering (#9479)</span><span class="sxs-lookup"><span data-stu-id="a52f3-1626">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="a52f3-1627">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="a52f3-1627">Az.Aks</span></span>
* <span data-ttu-id="a52f3-1628">Åtgärda problem med utdata för "Get-AzAks"</span><span class="sxs-lookup"><span data-stu-id="a52f3-1628">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="a52f3-1629">Mer information här: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="a52f3-1629">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="a52f3-1630">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a52f3-1630">Az.ApiManagement</span></span>
* <span data-ttu-id="a52f3-1631">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="a52f3-1631">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="a52f3-1632">Uppdatera .net-NuGet-versionen, som inte tillämpar begränsningar för productId, apiId och userId</span><span class="sxs-lookup"><span data-stu-id="a52f3-1632">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="a52f3-1633">**Get-AzApiManagementProduct** – Lade till stöd för frågekörning mot produkter via API.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1633">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="a52f3-1634">**New-AzApiManagementApiRevision** – Korrigering för problem där ApiRevisionDescription inte angavs vid skapande av ny API-revision https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="a52f3-1634">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="a52f3-1635">Åtgärdade skrivfel i modellen "PsApiManagementOAuth2AuthrozationServer" till "PsApiManagementOAuth2AuthorizationServer"</span><span class="sxs-lookup"><span data-stu-id="a52f3-1635">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="a52f3-1636">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="a52f3-1636">Az.Batch</span></span>
* <span data-ttu-id="a52f3-1637">Åtgärdade skrivfel i hjälpmeddelande och dokumentation till att skriva Windows med versaler</span><span class="sxs-lookup"><span data-stu-id="a52f3-1637">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="a52f3-1638">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="a52f3-1638">Az.Cdn</span></span>
* <span data-ttu-id="a52f3-1639">Åtgärdade skrivfel i CDN-modulens konverteringshjälp</span><span class="sxs-lookup"><span data-stu-id="a52f3-1639">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a52f3-1640">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a52f3-1640">Az.Compute</span></span>
* <span data-ttu-id="a52f3-1641">Lägg till VmssId i New-AzVMConfig-cmdleten</span><span class="sxs-lookup"><span data-stu-id="a52f3-1641">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="a52f3-1642">Lägg till parametrarna TerminateScheduledEvents och TerminateScheduledEventNotBeforeTimeoutInMinutes i New-AzVmssConfig och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a52f3-1642">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="a52f3-1643">Lägg till egenskapen HyperVGeneration till avbildningsobjekt för virtuell dator</span><span class="sxs-lookup"><span data-stu-id="a52f3-1643">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="a52f3-1644">Lägg till funktioner för Host och HostGroup</span><span class="sxs-lookup"><span data-stu-id="a52f3-1644">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="a52f3-1645">Nya cmdletar:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="a52f3-1645">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="a52f3-1646">HostId-parametern läggs till i New-AzVMConfig och New-AzVM</span><span class="sxs-lookup"><span data-stu-id="a52f3-1646">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="a52f3-1647">Uppdatera exempel i "Invoke-AzVMRunCommand"-dokumentationen till att använda rätt parameternamn</span><span class="sxs-lookup"><span data-stu-id="a52f3-1647">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="a52f3-1648">Uppdatera "-VolumeType"-beskrivningen i referensdokumentationen för "set-AzVMDiskEncryptionExtension" och "set-AzVmssDiskEncryptionExtension"</span><span class="sxs-lookup"><span data-stu-id="a52f3-1648">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a52f3-1649">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a52f3-1649">Az.DataFactory</span></span>
* <span data-ttu-id="a52f3-1650">Åtgärda skrivfel till att använda versaler för "Windows" i "New-AzDataFactoryEncryptValue"-dokumentationen</span><span class="sxs-lookup"><span data-stu-id="a52f3-1650">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="a52f3-1651">Uppdaterade ADF .Net SDK-versionen till 4.1.2</span><span class="sxs-lookup"><span data-stu-id="a52f3-1651">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="a52f3-1652">Lägg till parametrarna "DataProxyIntegrationRuntimeName", "DataProxyStagingLinkedServiceName" och "DataProxyStagingPath" för "Set-AzureRmDataFactoryV2IntegrationRuntime"-cmd för att aktivera konfiguration av lokalt installerad integrationskörning som en proxy för SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="a52f3-1652">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="a52f3-1653">Uppdaterade PSTriggerRun till att visa utlöst pipeline, meddelande och egenskaper samt PSActivityRun till att visa aktivitetstypen</span><span class="sxs-lookup"><span data-stu-id="a52f3-1653">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a52f3-1654">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a52f3-1654">Az.DataLakeStore</span></span>
* <span data-ttu-id="a52f3-1655">Korrigering av frysning av Get-DataLakeStoreDeletedItem för fel eller fjärrundantag.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1655">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="a52f3-1656">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a52f3-1656">Az.EventHub</span></span>
* <span data-ttu-id="a52f3-1657">Korrigering av problem #9658 : Skrivfel i parametern VirtualNteworkRule i Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="a52f3-1657">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="a52f3-1658">Korrigering av problem #9558 : Set-AzEventHubNamespace använder PATCH i stället för PUT</span><span class="sxs-lookup"><span data-stu-id="a52f3-1658">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="a52f3-1659">lade till parametern EnableKafka i Set-AzEventHubNamespace-cmdleten</span><span class="sxs-lookup"><span data-stu-id="a52f3-1659">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="a52f3-1660">Korrigering av problem #9786 : kan inte skapa en regel med Endast lyssna-behörighet</span><span class="sxs-lookup"><span data-stu-id="a52f3-1660">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="a52f3-1661">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="a52f3-1661">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="a52f3-1662">Åtgärdade skrivfel i dokumentation där "Azure" skrevs helt med gemener</span><span class="sxs-lookup"><span data-stu-id="a52f3-1662">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a52f3-1663">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a52f3-1663">Az.Monitor</span></span>
* <span data-ttu-id="a52f3-1664">Åtgärdade felaktigt parameternamn i hjälpdokumentationen</span><span class="sxs-lookup"><span data-stu-id="a52f3-1664">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a52f3-1665">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a52f3-1665">Az.Network</span></span>
* <span data-ttu-id="a52f3-1666">Uppdaterade New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="a52f3-1666">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="a52f3-1667">Gjorde parametern "PublicIpAddress" inaktuell eftersom den aldrig används på serversidan.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1667">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="a52f3-1668">Lade till den valfria parametern "Primary", som anger huruvida den aktuella IP-konfigurationen är den primära.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1668">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="a52f3-1669">Förbättrade hanteringen av felundantag för begärande från SDK – åtgärdar problemet att tidigare SDK-undantag inte hanteras på rätt sätt, vilket leder till att viktig felinformation inte visas</span><span class="sxs-lookup"><span data-stu-id="a52f3-1669">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="a52f3-1670">Justerade valideringslogiken för IPv6-IP-prefix till att kontrollera korrekt IPv6-prefixlängd.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1670">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="a52f3-1671">Uppdaterade Get-AzVirtualNetworkSubnetConfig: Lade till parameter som anges till get av undernätets resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1671">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="a52f3-1672">Uppdaterade beskrivningen av parametern Location för AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="a52f3-1672">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="a52f3-1673">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a52f3-1673">Az.OperationalInsights</span></span>
* <span data-ttu-id="a52f3-1674">Uppdaterade dokumentation för "New-AzOperationalInsightsLinuxSyslogDataSource"</span><span class="sxs-lookup"><span data-stu-id="a52f3-1674">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="a52f3-1675">Lade till exempel</span><span class="sxs-lookup"><span data-stu-id="a52f3-1675">Added example</span></span>
    - <span data-ttu-id="a52f3-1676">Uppdaterade beskrivningen av parametern "-Name"</span><span class="sxs-lookup"><span data-stu-id="a52f3-1676">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="a52f3-1677">Lade till ett exempel för New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="a52f3-1677">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="a52f3-1678">Ändrade beskrivningen av parametern -Name för New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="a52f3-1678">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a52f3-1679">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a52f3-1679">Az.RecoveryServices</span></span>
* <span data-ttu-id="a52f3-1680">Uppdatera "Get-AzRecoveryServicesBackupJobDetail.md"</span><span class="sxs-lookup"><span data-stu-id="a52f3-1680">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="a52f3-1681">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a52f3-1681">Az.Resources</span></span>
* <span data-ttu-id="a52f3-1682">Lägg till stöd för den nya API-versionen från 2019-05-10 för Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="a52f3-1682">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="a52f3-1683">Lägg till stöd för "copy.count = 0" för variabler, resurser och egenskaper</span><span class="sxs-lookup"><span data-stu-id="a52f3-1683">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="a52f3-1684">Resurser med "condition = false" eller "copy.count = 0" tas bort i complete-läget</span><span class="sxs-lookup"><span data-stu-id="a52f3-1684">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="a52f3-1685">Lägg till ett exempel på tilldelning av princip på prenumerationsnivå i hjälpdokumentationen</span><span class="sxs-lookup"><span data-stu-id="a52f3-1685">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="a52f3-1686">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a52f3-1686">Az.ServiceBus</span></span>
* <span data-ttu-id="a52f3-1687">Korrigering av problem #9658 : Skrivfel i parametern VirtualNetworkRule i set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="a52f3-1687">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="a52f3-1688">Korrigering av problem #9786 : kan inte skapa en regel med Endast lyssna-behörighet</span><span class="sxs-lookup"><span data-stu-id="a52f3-1688">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="a52f3-1689">Lade till det nya kommandot "Test-AzServiceBusNameAvailability" för att kontrollera namntillgängligheten för kö och ämne</span><span class="sxs-lookup"><span data-stu-id="a52f3-1689">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a52f3-1690">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a52f3-1690">Az.ServiceFabric</span></span>
* <span data-ttu-id="a52f3-1691">Åtgärda buggar med tillägg av nodtyps-cmdlet:</span><span class="sxs-lookup"><span data-stu-id="a52f3-1691">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="a52f3-1692">NullReferenceException-bugg när resursgrupp hade annan vmss som inte är relaterad till Service Fabric-klustret.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1692">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="a52f3-1693">Åtgärdar problemet: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="a52f3-1693">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="a52f3-1694">Åtgärda bugg där cmdleten misslyckades om virtualNetwork var i en annan resursgrupp än klustret.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1694">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="a52f3-1695">Åtgärdar problemet: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="a52f3-1695">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="a52f3-1696">AzServiceFabricApplicationCertificate-cmdleten görs inaktuell</span><span class="sxs-lookup"><span data-stu-id="a52f3-1696">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="a52f3-1697">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a52f3-1697">Az.Sql</span></span>
* <span data-ttu-id="a52f3-1698">Uppdatera dokumentation om gamla gransknings-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1698">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a52f3-1699">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a52f3-1699">Az.Storage</span></span>
* <span data-ttu-id="a52f3-1700">Uppdatera hjälpen för Get/Close-AzStorageFileHandle genom att lägga till fler scenarier i cmdlet-exempel och uppdatera parameterbeskrivningar</span><span class="sxs-lookup"><span data-stu-id="a52f3-1700">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="a52f3-1701">Stöd för StandardBlobTier i uppladdningsblob och kopieringsblob</span><span class="sxs-lookup"><span data-stu-id="a52f3-1701">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="a52f3-1702">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="a52f3-1702">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="a52f3-1703">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="a52f3-1703">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="a52f3-1704">Stöd för rehydratiseringsprioritet i kopieringsblob</span><span class="sxs-lookup"><span data-stu-id="a52f3-1704">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="a52f3-1705">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="a52f3-1705">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a52f3-1706">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a52f3-1706">Az.Websites</span></span>
* <span data-ttu-id="a52f3-1707">Lägg till klargöranden gällande parametern -AppSettings i Set-AzWebApp och Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a52f3-1707">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="a52f3-1708">2.5.0 – July 2019</span><span class="sxs-lookup"><span data-stu-id="a52f3-1708">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a52f3-1709">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a52f3-1709">Az.Accounts</span></span>
* <span data-ttu-id="a52f3-1710">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="a52f3-1710">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="a52f3-1711">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="a52f3-1711">Az.ApplicationInsights</span></span>
* <span data-ttu-id="a52f3-1712">Korrigera skrivfel i exempel i dokumentationen för Remove-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="a52f3-1712">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a52f3-1713">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a52f3-1713">Az.Automation</span></span>
* <span data-ttu-id="a52f3-1714">Korrigera skrivfel i resurssträng</span><span class="sxs-lookup"><span data-stu-id="a52f3-1714">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="a52f3-1715">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a52f3-1715">Az.CognitiveServices</span></span>
* <span data-ttu-id="a52f3-1716">Stöd för NetworkRuleSet har lagts till.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1716">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a52f3-1717">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a52f3-1717">Az.Compute</span></span>
* <span data-ttu-id="a52f3-1718">Lägg till saknade egenskaper (ComputerName, OsName, OsVersion och HyperVGeneration) för visningsobjekt i den virtuella datorinstansen.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1718">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="a52f3-1719">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a52f3-1719">Az.ContainerRegistry</span></span>
* <span data-ttu-id="a52f3-1720">Åtgärda skrivfel i Remove-AzContainerRegistryReplication för parametern Replication</span><span class="sxs-lookup"><span data-stu-id="a52f3-1720">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="a52f3-1721">Mer information finns här: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="a52f3-1721">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a52f3-1722">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a52f3-1722">Az.DataFactory</span></span>
* <span data-ttu-id="a52f3-1723">ADF .Net SDK-versionen har uppdaterats till 4.1.0</span><span class="sxs-lookup"><span data-stu-id="a52f3-1723">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="a52f3-1724">Korrigera skrivfel i dokumentationen för Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="a52f3-1724">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="a52f3-1725">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a52f3-1725">Az.EventHub</span></span>
* <span data-ttu-id="a52f3-1726">Ny cmmdlet har lagts till för att skapa SAS-token: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="a52f3-1726">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="a52f3-1727">verifierings- och felmeddelande har lagts till för authorizationrules-rättigheter om endast "hantera" har tilldelats</span><span class="sxs-lookup"><span data-stu-id="a52f3-1727">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a52f3-1728">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a52f3-1728">Az.KeyVault</span></span>
* <span data-ttu-id="a52f3-1729">Stöd har lagts till för att ange KeySize för certifikatprinciper</span><span class="sxs-lookup"><span data-stu-id="a52f3-1729">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="a52f3-1730">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="a52f3-1730">Az.LogicApp</span></span>
* <span data-ttu-id="a52f3-1731">Korrigering för Get-AzIntegrationAccountMap för att lista alla mappningstyper</span><span class="sxs-lookup"><span data-stu-id="a52f3-1731">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="a52f3-1732">Ny MapType-parameter har lagts till för filtrering</span><span class="sxs-lookup"><span data-stu-id="a52f3-1732">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="a52f3-1733">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="a52f3-1733">Az.ManagedServices</span></span>
* <span data-ttu-id="a52f3-1734">Stöd för API-versionen 2019-06-01 (GA) har lagts till</span><span class="sxs-lookup"><span data-stu-id="a52f3-1734">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a52f3-1735">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a52f3-1735">Az.Network</span></span>
* <span data-ttu-id="a52f3-1736">Lägg till stöd för privat slutpunkt och privat länktjänst</span><span class="sxs-lookup"><span data-stu-id="a52f3-1736">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="a52f3-1737">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="a52f3-1737">New cmdlets</span></span>
        - <span data-ttu-id="a52f3-1738">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="a52f3-1738">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="a52f3-1739">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="a52f3-1739">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="a52f3-1740">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a52f3-1740">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="a52f3-1741">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a52f3-1741">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="a52f3-1742">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a52f3-1742">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="a52f3-1743">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a52f3-1743">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="a52f3-1744">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="a52f3-1744">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="a52f3-1745">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="a52f3-1745">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="a52f3-1746">Nedanstående kommandon för funktionen har uppdaterats: Flaggan PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies på undernätet i VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a52f3-1746">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="a52f3-1747">Uppdaterade New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="a52f3-1747">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="a52f3-1748">Valfri parameter har lagts till – PrivateEndpointNetworkPoliciesFlag som konfigurerar huruvida nätverksprinciper ska tillämpas på en privat slutpunkt i det här undernätet.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1748">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="a52f3-1749">Valfri parameter har lagts till – PrivateLinkServiceNetworkPoliciesFlag som konfigurerar huruvida nätverksprinciper ska tillämpas på en privat länktjänst i det här undernätet.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1749">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="a52f3-1750">AzPrivateLinkService för cmdlet-parametern ServiceName har bytt namn till Name med aliaset ServiceName för bakåtkompatibilitet</span><span class="sxs-lookup"><span data-stu-id="a52f3-1750">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="a52f3-1751">Aktivera ICMP-protokoll för konfiguration av nätverkssäkerhetsregler</span><span class="sxs-lookup"><span data-stu-id="a52f3-1751">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="a52f3-1752">Uppdaterade cmdletar</span><span class="sxs-lookup"><span data-stu-id="a52f3-1752">Updated cmdlets</span></span>
        - <span data-ttu-id="a52f3-1753">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a52f3-1753">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="a52f3-1754">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a52f3-1754">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="a52f3-1755">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a52f3-1755">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="a52f3-1756">Lägg till ConnectionProtocolType (Ikev1/Ikev2) som en konfigurerbar parameter för New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="a52f3-1756">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="a52f3-1757">Lägg till PrivateIpAddressVersion i LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="a52f3-1757">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="a52f3-1758">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="a52f3-1758">Updated cmdlet:</span></span>
        - <span data-ttu-id="a52f3-1759">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="a52f3-1759">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="a52f3-1760">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="a52f3-1760">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="a52f3-1761">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="a52f3-1761">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="a52f3-1762">Uppdatering av Application Gateway-kommandot New-AzApplicationGatewayProbeConfig för stöd av anpassad port i Probe</span><span class="sxs-lookup"><span data-stu-id="a52f3-1762">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="a52f3-1763">Uppdaterade New-AzApplicationGatewayProbeConfig: Den valfria parametern Port som används för avsökning i serverdelen har lagts till.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1763">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="a52f3-1764">Denna parameter gäller för SKU:erna Standard_V2 och WAF_V2.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1764">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="a52f3-1765">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a52f3-1765">Az.OperationalInsights</span></span>
* <span data-ttu-id="a52f3-1766">Uppdaterade standardversionen för sparade sökningar till 1.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1766">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="a52f3-1767">Åtgärdade hantering av anpassad log null regex</span><span class="sxs-lookup"><span data-stu-id="a52f3-1767">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a52f3-1768">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a52f3-1768">Az.RecoveryServices</span></span>
* <span data-ttu-id="a52f3-1769">Uppdatera Get-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="a52f3-1769">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="a52f3-1770">Uppdatera Get-AzRecoveryServicesBackupContainer.md</span><span class="sxs-lookup"><span data-stu-id="a52f3-1770">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="a52f3-1771">Uppdatera Get-AzRecoveryServicesVault.md</span><span class="sxs-lookup"><span data-stu-id="a52f3-1771">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="a52f3-1772">Uppdatera Wait-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="a52f3-1772">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="a52f3-1773">Uppdatera Set-AzRecoveryServicesVaultContext.md</span><span class="sxs-lookup"><span data-stu-id="a52f3-1773">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="a52f3-1774">Uppdatera Get-AzRecoveryServicesBackupItem.md</span><span class="sxs-lookup"><span data-stu-id="a52f3-1774">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="a52f3-1775">Uppdatera Get-AzRecoveryServicesBackupRecoveryPoint.md</span><span class="sxs-lookup"><span data-stu-id="a52f3-1775">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="a52f3-1776">Uppdatera Restore-AzRecoveryServicesBackupItem.md</span><span class="sxs-lookup"><span data-stu-id="a52f3-1776">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="a52f3-1777">Uppdaterat tjänstanrop för avregistrering av container för Azure-filresurs</span><span class="sxs-lookup"><span data-stu-id="a52f3-1777">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="a52f3-1778">Uppdatera Set-AzRecoveryServicesAsrAlertSetting.md</span><span class="sxs-lookup"><span data-stu-id="a52f3-1778">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="a52f3-1779">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a52f3-1779">Az.Resources</span></span>
- <span data-ttu-id="a52f3-1780">Ta bort den cmdlet som saknas och som refereras i dokumentationen till New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a52f3-1780">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="a52f3-1781">Princip-cmdletar har uppdaterats så att de använder den nya API-versionen 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="a52f3-1781">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="a52f3-1782">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a52f3-1782">Az.ServiceBus</span></span>
* <span data-ttu-id="a52f3-1783">Ny cmmdlet har lagts till för att skapa SAS-token: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="a52f3-1783">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="a52f3-1784">verifierings- och felmeddelande har lagts till för authorizationrules-rättigheter om endast "hantera" har tilldelats</span><span class="sxs-lookup"><span data-stu-id="a52f3-1784">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="a52f3-1785">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a52f3-1785">Az.Sql</span></span>
* <span data-ttu-id="a52f3-1786">Åtgärda saknade exempel för Set-AzSqlDatabaseSecondary cmdlet</span><span class="sxs-lookup"><span data-stu-id="a52f3-1786">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="a52f3-1787">Åtgärda angivna återkommande genomsökningar för bedömning av säkerhetsrisk utan angivna e-postadresser</span><span class="sxs-lookup"><span data-stu-id="a52f3-1787">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="a52f3-1788">Korrigera ett skrivfel i ett varningsmeddelande.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1788">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a52f3-1789">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a52f3-1789">Az.Storage</span></span>
* <span data-ttu-id="a52f3-1790">Uppdatera exempel i referensdokumentationen för Get-AzStorageAccount så att rätt parameternamn används</span><span class="sxs-lookup"><span data-stu-id="a52f3-1790">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="a52f3-1791">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="a52f3-1791">Az.StorageSync</span></span>
* <span data-ttu-id="a52f3-1792">Lägger till cmdleten Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1792">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="a52f3-1793">Åtgärda problem 9551 så att TierFilesOlderThanDays föredras</span><span class="sxs-lookup"><span data-stu-id="a52f3-1793">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a52f3-1794">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a52f3-1794">Az.Websites</span></span>
* <span data-ttu-id="a52f3-1795">Åtgärdar ett fel där vissa SiteConfig-egenskaper inte returnerades av Get-AzWebApp och Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a52f3-1795">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="a52f3-1796">Lägger till en ny platsparameter för Get-AzDeletedWebApp och Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="a52f3-1796">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="a52f3-1797">Åtgärdar ett fel i kloning av webbapp-platser som använder New-AzWebApp-IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="a52f3-1797">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="a52f3-1798">2.4.0 – juli 2019</span><span class="sxs-lookup"><span data-stu-id="a52f3-1798">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a52f3-1799">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a52f3-1799">Az.Accounts</span></span>
* <span data-ttu-id="a52f3-1800">Lägg till stöd för profil-cmdletar</span><span class="sxs-lookup"><span data-stu-id="a52f3-1800">Add support for profile cmdlets</span></span>
* <span data-ttu-id="a52f3-1801">Lägg till stöd för miljöer och dataplaner i genererade cmdletar</span><span class="sxs-lookup"><span data-stu-id="a52f3-1801">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="a52f3-1802">Åtgärda bugg där fel slutpunkt i vissa fall användes för cmdletar för dataplaner i Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="a52f3-1802">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="a52f3-1803">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="a52f3-1803">Az.Advisor</span></span>
* <span data-ttu-id="a52f3-1804">GA-version av Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="a52f3-1804">GA release of Az.Advisor</span></span>
* <span data-ttu-id="a52f3-1805">Den här modulen ingår nu som en del av `Az`-sammanslagningsmodulen</span><span class="sxs-lookup"><span data-stu-id="a52f3-1805">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="a52f3-1806">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a52f3-1806">Az.ApiManagement</span></span>
* <span data-ttu-id="a52f3-1807">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="a52f3-1807">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="a52f3-1808">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="a52f3-1808">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="a52f3-1809">Stöd för att fråga prenumerationer efter användare och produkt har lagts till</span><span class="sxs-lookup"><span data-stu-id="a52f3-1809">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="a52f3-1810">Stöd för att fråga med hjälp av omfång ”/”, ”/apis”, ”/apis/echo-api” har lagts till</span><span class="sxs-lookup"><span data-stu-id="a52f3-1810">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="a52f3-1811">Korrigering av problem https://github.com/Azure/azure-powershell/issues/9307 och https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="a52f3-1811">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="a52f3-1812">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="a52f3-1812">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="a52f3-1813">Stöd för att ange ”ApiVersion” och ”ApiVersionSetId” när API:er importeras har lagts till</span><span class="sxs-lookup"><span data-stu-id="a52f3-1813">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a52f3-1814">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a52f3-1814">Az.Automation</span></span>
* <span data-ttu-id="a52f3-1815">Bugg med cmdleten Set-AzAutomationConnectionFieldValue för att hantera strängvärde har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1815">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a52f3-1816">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a52f3-1816">Az.Compute</span></span>
* <span data-ttu-id="a52f3-1817">Lägg till parametern HyperVGeneration i New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="a52f3-1817">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a52f3-1818">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a52f3-1818">Az.DataFactory</span></span>
* <span data-ttu-id="a52f3-1819">Uppdaterar utdata från ADF-cmdletar som hämtar aktivitetskörningar, hämtar pipelinekörningar och hämtar utlösarkörningar för stöd för Select-Object-pipe.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1819">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="a52f3-1820">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="a52f3-1820">Az.EventGrid</span></span>
* <span data-ttu-id="a52f3-1821">Korrigera stavfel i dokumentation om ”New-AzEventGridSubscription”</span><span class="sxs-lookup"><span data-stu-id="a52f3-1821">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a52f3-1822">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a52f3-1822">Az.IotHub</span></span>
* <span data-ttu-id="a52f3-1823">Lägg till stöd för att återskapa principnycklar för auktorisering.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1823">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a52f3-1824">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a52f3-1824">Az.Network</span></span>
* <span data-ttu-id="a52f3-1825">”RoutingPreference” har lagts till i offentliga IP-taggar</span><span class="sxs-lookup"><span data-stu-id="a52f3-1825">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="a52f3-1826">Förbättra exempel för referensdokumentation om ”Get-AzNetworkServiceTag”</span><span class="sxs-lookup"><span data-stu-id="a52f3-1826">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="a52f3-1827">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a52f3-1827">Az.PolicyInsights</span></span>
* <span data-ttu-id="a52f3-1828">Åtgärda problem med null-referens i Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="a52f3-1828">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="a52f3-1829">Mer information här: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="a52f3-1829">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="a52f3-1830">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a52f3-1830">Az.OperationalInsights</span></span>
* <span data-ttu-id="a52f3-1831">Modellen för CustomLog-datakälla som returneras i Get-AzOperationalInsightsDataSource har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="a52f3-1831">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a52f3-1832">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a52f3-1832">Az.RecoveryServices</span></span>
* <span data-ttu-id="a52f3-1833">Kommandot get-policy för IaaSVM:er har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="a52f3-1833">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="a52f3-1834">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a52f3-1834">Az.Resources</span></span>
    - <span data-ttu-id="a52f3-1835">Korrigera hjälptext för den översta parametern i Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="a52f3-1835">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="a52f3-1836">Lägg till växlingsstöd på klientsidan för Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="a52f3-1836">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="a52f3-1837">Lägg till nya parametrar för Set-AzPolicyAssignment, -PolicyParameters och -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="a52f3-1837">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="a52f3-1838">En mängd dokument- och exempeluppdateringar för Policy-cmdletar</span><span class="sxs-lookup"><span data-stu-id="a52f3-1838">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="a52f3-1839">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a52f3-1839">Az.ServiceBus</span></span>
* <span data-ttu-id="a52f3-1840">Korrigering av problem #4938 – New-AzureRmServiceBusQueue returnerar BadRequest vid konfiguration av MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="a52f3-1840">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="a52f3-1841">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a52f3-1841">Az.Sql</span></span>
* <span data-ttu-id="a52f3-1842">Lägg till cmdletar för instansredundansgrupper från förhandsversion till offentlig version</span><span class="sxs-lookup"><span data-stu-id="a52f3-1842">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="a52f3-1843">Stöd för granskning för Azure SQL Server\Database med nya cmdletar.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1843">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="a52f3-1844">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="a52f3-1844">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="a52f3-1845">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="a52f3-1845">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="a52f3-1846">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="a52f3-1846">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="a52f3-1847">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="a52f3-1847">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="a52f3-1848">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="a52f3-1848">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="a52f3-1849">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="a52f3-1849">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="a52f3-1850">Ta bort begränsningar för e-post från inställningarna för sårbarhetsbedömning</span><span class="sxs-lookup"><span data-stu-id="a52f3-1850">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a52f3-1851">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a52f3-1851">Az.Storage</span></span>
* <span data-ttu-id="a52f3-1852">Ändra två parametrar ”-IndexDocument” och ”-ErrorDocument404Path” från ”krävs” till ”valfri” i cmdlet:</span><span class="sxs-lookup"><span data-stu-id="a52f3-1852">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="a52f3-1853">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="a52f3-1853">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="a52f3-1854">Uppdatera hjälpen för Get-AzStorageBlobContent genom att lägga till ett exempel</span><span class="sxs-lookup"><span data-stu-id="a52f3-1854">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="a52f3-1855">Visa mer felinformation när cmdleten misslyckas med StorageException</span><span class="sxs-lookup"><span data-stu-id="a52f3-1855">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="a52f3-1856">Stöd för att skapa eller uppdatera lagringskonto med Azure Files AAD DS-autentisering</span><span class="sxs-lookup"><span data-stu-id="a52f3-1856">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="a52f3-1857">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a52f3-1857">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="a52f3-1858">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a52f3-1858">Set-AzStorageAccount</span></span>
* <span data-ttu-id="a52f3-1859">Stöd för att lista eller stänga filreferenser för en filresurs, filkatalog eller en fil</span><span class="sxs-lookup"><span data-stu-id="a52f3-1859">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="a52f3-1860">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="a52f3-1860">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="a52f3-1861">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="a52f3-1861">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="a52f3-1862">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="a52f3-1862">Az.StorageSync</span></span>
* <span data-ttu-id="a52f3-1863">Den här modulen ingår nu som en del av `Az`-sammanslagningsmodulen</span><span class="sxs-lookup"><span data-stu-id="a52f3-1863">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="a52f3-1864">2.3.2 – juni 2019</span><span class="sxs-lookup"><span data-stu-id="a52f3-1864">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a52f3-1865">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a52f3-1865">Az.Accounts</span></span>
* <span data-ttu-id="a52f3-1866">Åtgärda bugg med felaktiga webbadresser som i vissa fall användes för Functions-anrop</span><span class="sxs-lookup"><span data-stu-id="a52f3-1866">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="a52f3-1867">Mer information här: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="a52f3-1867">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="a52f3-1868">Åtgärda problem med alias från AzureRM i Az-cmdletar</span><span class="sxs-lookup"><span data-stu-id="a52f3-1868">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="a52f3-1869">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="a52f3-1869">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="a52f3-1870">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="a52f3-1870">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a52f3-1871">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a52f3-1871">Az.Compute</span></span>
* <span data-ttu-id="a52f3-1872">Parameteruppsättningarna New-AzVm och New-AzVmss accepterar nu parametern ”ProximityPlacementGroup”.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1872">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="a52f3-1873">Stavfel i referensdokumentationen för ”New-AzVM” har korrigerats</span><span class="sxs-lookup"><span data-stu-id="a52f3-1873">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="a52f3-1874">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="a52f3-1874">Az.Dns</span></span>
* <span data-ttu-id="a52f3-1875">Stavfel i hjälpexempel för ”Set-AzDnsZone” har korrigerats.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1875">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="a52f3-1876">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="a52f3-1876">Az.EventGrid</span></span>
* <span data-ttu-id="a52f3-1877">Har uppdaterats för att använda API-versionen 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1877">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="a52f3-1878">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="a52f3-1878">New cmdlets:</span></span>
    - <span data-ttu-id="a52f3-1879">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="a52f3-1879">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="a52f3-1880">Skapar en ny Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1880">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="a52f3-1881">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="a52f3-1881">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="a52f3-1882">Hämtar information om en Event Grid-domän eller hämtar en lista med alla Event Grid-domäner i den aktuella Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1882">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="a52f3-1883">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="a52f3-1883">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="a52f3-1884">Tar bort en Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1884">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="a52f3-1885">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="a52f3-1885">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="a52f3-1886">Återskapar nyckeln för delad åtkomst för en Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1886">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="a52f3-1887">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="a52f3-1887">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="a52f3-1888">Hämtar de nycklar för delad åtkomst som används för att publicera händelser till en Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1888">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="a52f3-1889">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="a52f3-1889">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="a52f3-1890">Skapar ett nytt Azure Event Grid-domänämne.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1890">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="a52f3-1891">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="a52f3-1891">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="a52f3-1892">Hämtar information om ett Event Grid-domänämne eller hämtar en lista med alla Event Grid-domänämnen under en specifik Event Grid-domän i nuvarande Azure</span><span class="sxs-lookup"><span data-stu-id="a52f3-1892">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="a52f3-1893">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="a52f3-1893">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="a52f3-1894">Tar bort ett befintligt Azure Event Grid-domänämne.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1894">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="a52f3-1895">Uppdaterade cmdletar:</span><span class="sxs-lookup"><span data-stu-id="a52f3-1895">Updated cmdlets:</span></span>
    - <span data-ttu-id="a52f3-1896">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="a52f3-1896">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="a52f3-1897">Lägg till nya obligatoriska parametrar för att stödja piping för den nya Event Grid-domänen och Event Grid-domänämnet för att göra det möjligt att skapa nya händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1897">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="a52f3-1898">Lägg till nya obligatoriska parametrar för att ange det nya Event Grid-domännamnet och/eller namnet på Event Grid-domänämnet för att göra det möjligt att skapa nya händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1898">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="a52f3-1899">Lägg till ny parameteruppsättningar för domäner och domänämnen för att göra det möjligt att återanvända befintliga parametrar (t.ex. EndPointType, SubjectBeginsWith osv).</span><span class="sxs-lookup"><span data-stu-id="a52f3-1899">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="a52f3-1900">Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="a52f3-1900">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="a52f3-1901">Förfallodatum för händelseprenumeration</span><span class="sxs-lookup"><span data-stu-id="a52f3-1901">Event subscription expiration date,</span></span>
            - <span data-ttu-id="a52f3-1902">Avancerade filterparametrar.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1902">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="a52f3-1903">Lägg till ny uppräkning för servicebusqueue som mål.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1903">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="a52f3-1904">Tillåt inte användning av ”Alla” i alternativet -IncludedEventType och ersätt det med</span><span class="sxs-lookup"><span data-stu-id="a52f3-1904">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="a52f3-1905">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="a52f3-1905">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="a52f3-1906">Lägg till ny valfria parametrar (Top, ODataQuery och NextLink) för att stödja sidnumrering och filtrering av resultat.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1906">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="a52f3-1907">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="a52f3-1907">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="a52f3-1908">Lägg till nya obligatoriska parametrar för att stödja piping för en Event Grid-domän och Event Grid-domänämnen för att göra det möjligt att ta bort befintliga händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1908">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="a52f3-1909">Lägg till nya obligatoriska parametrar för att ange Event Grid-domännamnet och/eller namnet på Event Grid-domänämnet för att göra det möjligt att ta bort befintliga händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1909">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="a52f3-1910">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="a52f3-1910">Az.FrontDoor</span></span>
* <span data-ttu-id="a52f3-1911">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="a52f3-1911">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="a52f3-1912">Lägg till stöd för transformeringar och nytt värde för automatisk komplettering för operatorer (RegEx)</span><span class="sxs-lookup"><span data-stu-id="a52f3-1912">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="a52f3-1913">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="a52f3-1913">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="a52f3-1914">Lägg till nya värden för automatisk komplettering</span><span class="sxs-lookup"><span data-stu-id="a52f3-1914">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a52f3-1915">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a52f3-1915">Az.Network</span></span>
* <span data-ttu-id="a52f3-1916">Lägg till stöd för resurs för virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="a52f3-1916">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="a52f3-1917">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="a52f3-1917">New cmdlets</span></span>
        - <span data-ttu-id="a52f3-1918">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="a52f3-1918">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="a52f3-1919">Lägg till AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="a52f3-1919">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="a52f3-1920">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="a52f3-1920">New cmdlets</span></span>
        - <span data-ttu-id="a52f3-1921">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="a52f3-1921">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="a52f3-1922">Lägg till PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="a52f3-1922">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="a52f3-1923">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="a52f3-1923">New cmdlets</span></span>
        - <span data-ttu-id="a52f3-1924">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="a52f3-1924">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="a52f3-1925">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="a52f3-1925">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="a52f3-1926">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="a52f3-1926">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="a52f3-1927">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="a52f3-1927">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="a52f3-1928">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a52f3-1928">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="a52f3-1929">Lägg till PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="a52f3-1929">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="a52f3-1930">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="a52f3-1930">New cmdlets</span></span>
        - <span data-ttu-id="a52f3-1931">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="a52f3-1931">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="a52f3-1932">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="a52f3-1932">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="a52f3-1933">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="a52f3-1933">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="a52f3-1934">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="a52f3-1934">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="a52f3-1935">Nedanstående kommandon för funktionen har uppdaterats: Flaggan UseLocalAzureIpAddress på VpnConnection</span><span class="sxs-lookup"><span data-stu-id="a52f3-1935">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="a52f3-1936">New-AzVpnConnection har uppdaterats: Den valfria parametern -UseLocalAzureIpAddress har lagts till för att visa att en lokal IP-adress i Azure ska användas som källadress när anslutningen initieras.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1936">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="a52f3-1937">Set-AzVpnConnection har uppdaterats: Den valfria parametern -UseLocalAzureIpAddress har lagts till för att visa att en lokal IP-adress i Azure ska användas som källadress när anslutningen initieras.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1937">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="a52f3-1938">Det skrivskyddade fältet PeeredConnections har lagts till i ExpressRoute-peering.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1938">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="a52f3-1939">Det skrivskyddade fältet GlobalReachEnabled har lagts till i ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1939">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="a52f3-1940">Ett attribut för icke-bakåtkompatibla ändringar har lagts till för att lyfta fram utfasning av fältet AllowGlobalReach i modellen ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a52f3-1940">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="a52f3-1941">Problem 8756 har åtgärdats: Fel vid användning av TargetListenerID med AzApplicationGatewayRedirectConfiguration-cmdletar</span><span class="sxs-lookup"><span data-stu-id="a52f3-1941">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="a52f3-1942">En bugg i New-AzApplicationGatewayPathRuleConfig som gjorde att regeluppsättningen för att återskapa inte kunde anges har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1942">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="a52f3-1943">Visningen av VirtualNetworkTaps i NetworkInterfaceIpConfiguration har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="a52f3-1943">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="a52f3-1944">Cortex Get-cmdletar för att visa en lista med alla delar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="a52f3-1944">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="a52f3-1945">Funktionen för att skapa VirtualHub-referenser för ExpressRouteGateways och VpnGateway har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="a52f3-1945">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="a52f3-1946">Stöd för tillgänglighetszoner i AzureFirewall och NatGateway har lagts till</span><span class="sxs-lookup"><span data-stu-id="a52f3-1946">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="a52f3-1947">Cmdleten Get-AzNetworkServiceTag har lagts till</span><span class="sxs-lookup"><span data-stu-id="a52f3-1947">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="a52f3-1948">Lägg till stöd för flera offentliga IP-adresser för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="a52f3-1948">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="a52f3-1949">Cmdleten New-AzFirewall har uppdaterats:</span><span class="sxs-lookup"><span data-stu-id="a52f3-1949">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="a52f3-1950">Parametern -PublicIpAddress som accepterar ett eller flera offentliga IP-adressobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="a52f3-1950">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="a52f3-1951">Parametern -VirtualNetwork som accepterar ett virtuellt nätverksobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="a52f3-1951">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="a52f3-1952">Metoderna AddPublicIpAddress och RemovePublicIpAddress har lagts till på brandväggsobjekt – dessa accepterar ett offentligt IP-adressobjekt som indata</span><span class="sxs-lookup"><span data-stu-id="a52f3-1952">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="a52f3-1953">Inaktuella parametrar -PublicIpName och -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="a52f3-1953">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="a52f3-1954">Nedanstående kommandon för funktionen har uppdaterats: Ange autentiseringsalternativ för VpnClient AAD till resurser för virtuella nätverksgatewayer.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1954">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="a52f3-1955">New-AzVirtualNetworkGateway har uppdaterats: De valfria parametrarna AadTenantUri, AadAudienceId och AadIssuerUri för att ange VpnClient AAD-autentiseringsalternativ på en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1955">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="a52f3-1956">Set-AzVirtualNetworkGateway har uppdaterats: De valfria parametrarna AadTenantUri, AadAudienceId och AadIssuerUri för att ange VpnClient AAD-autentiseringsalternativ på en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1956">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="a52f3-1957">Set-AzVirtualNetworkGateway har uppdaterats: Den valfria växelparametern RemoveAadAuthentication som tar bort VpnClient AAD-autentiseringsalternativ från en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1957">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="a52f3-1958">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a52f3-1958">Az.OperationalInsights</span></span>
* <span data-ttu-id="a52f3-1959">Aktivera prisnivån **pergb2018** i kommandot ”New-AzureRmOperationalInsightsWorkspace”</span><span class="sxs-lookup"><span data-stu-id="a52f3-1959">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="a52f3-1960">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a52f3-1960">Az.Resources</span></span>
* <span data-ttu-id="a52f3-1961">Stöd för ytterligare alternativ för att exportera en mall</span><span class="sxs-lookup"><span data-stu-id="a52f3-1961">Support for additional Template Export options</span></span>
    - <span data-ttu-id="a52f3-1962">Lägg till parametern ”-SkipResourceNameParameterization” till Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a52f3-1962">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="a52f3-1963">Lägg till parametern ”-SkipAllParameterization” till Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a52f3-1963">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="a52f3-1964">Lägg till parametern ”-Resource” till Export-AzResourceGroup för exporterad resursfiltrering</span><span class="sxs-lookup"><span data-stu-id="a52f3-1964">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a52f3-1965">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a52f3-1965">Az.ServiceFabric</span></span>
* <span data-ttu-id="a52f3-1966">Åtgärda att fel tumavtryck används vid tilläggning av certifikat i ByExistingKeyVault i vissa fall</span><span class="sxs-lookup"><span data-stu-id="a52f3-1966">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="a52f3-1967">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a52f3-1967">Az.Sql</span></span>
* <span data-ttu-id="a52f3-1968">Åtgärda suffix för lagringsslutpunkt i Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="a52f3-1968">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="a52f3-1969">Åtgärda att aktivering av Advanced Data Security åsidosätter Advanced Threat Protection-princip</span><span class="sxs-lookup"><span data-stu-id="a52f3-1969">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="a52f3-1970">Nya cmdletar för Management.Sql som gör att kunderna kan lägga till nycklar för transparent datakryptering (TDE) och ange TDE-skydd för hanterade instanser</span><span class="sxs-lookup"><span data-stu-id="a52f3-1970">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="a52f3-1971">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="a52f3-1971">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="a52f3-1972">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="a52f3-1972">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="a52f3-1973">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="a52f3-1973">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="a52f3-1974">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="a52f3-1974">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="a52f3-1975">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="a52f3-1975">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a52f3-1976">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a52f3-1976">Az.Storage</span></span>
* <span data-ttu-id="a52f3-1977">Stöd för typerna FileStorage och SkuName Premium_ZRS när lagringskonton skapas</span><span class="sxs-lookup"><span data-stu-id="a52f3-1977">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="a52f3-1978">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a52f3-1978">New-AzStorageAccount</span></span>
* <span data-ttu-id="a52f3-1979">Beskrivningen av cmdleten för bloboföränderlighet har förtydligats</span><span class="sxs-lookup"><span data-stu-id="a52f3-1979">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="a52f3-1980">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="a52f3-1980">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a52f3-1981">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a52f3-1981">Az.Websites</span></span>
* <span data-ttu-id="a52f3-1982">Optimerar Get-AzWebAppCertificate för att filtrera efter resursgrupp på servern i stället för klienten</span><span class="sxs-lookup"><span data-stu-id="a52f3-1982">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="a52f3-1983">Lägger till växlingsparametern -UseDisasterRecovery till Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="a52f3-1983">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="a52f3-1984">2.2.0 – juni 2019</span><span class="sxs-lookup"><span data-stu-id="a52f3-1984">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="a52f3-1985">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="a52f3-1985">Az.Cdn</span></span>
* <span data-ttu-id="a52f3-1986">Uppdaterade cmdletar för att ge stöd för rulesEngine-funktion baserat på API-version 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1986">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a52f3-1987">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a52f3-1987">Az.Compute</span></span>
* <span data-ttu-id="a52f3-1988">Lade till parameter `NoWait` som startar åtgärden och returnerar omedelbart, innan åtgärden har slutförts.</span><span class="sxs-lookup"><span data-stu-id="a52f3-1988">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="a52f3-1989">Uppdaterade cmdletar:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="a52f3-1989">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="a52f3-1990">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a52f3-1990">Az.EventHub</span></span>
* <span data-ttu-id="a52f3-1991">Korrigering för #9231 – Get-AzEventHubNamespace returnerar inga taggar</span><span class="sxs-lookup"><span data-stu-id="a52f3-1991">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="a52f3-1992">Korrigering för #9230 – Get-AzEventHubNamespace returnerar ResourceGroup istället för ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a52f3-1992">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a52f3-1993">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a52f3-1993">Az.Network</span></span>
* <span data-ttu-id="a52f3-1994">Uppdatera ResourceId och InputObject för NAT-gateway</span><span class="sxs-lookup"><span data-stu-id="a52f3-1994">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="a52f3-1995">Lägg till alias för ResourceId och InputObject</span><span class="sxs-lookup"><span data-stu-id="a52f3-1995">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="a52f3-1996">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a52f3-1996">Az.PolicyInsights</span></span>
* <span data-ttu-id="a52f3-1997">Åtgärda Null-referensproblem i Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="a52f3-1997">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a52f3-1998">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a52f3-1998">Az.RecoveryServices</span></span>
* <span data-ttu-id="a52f3-1999">Minsta kvarhållning för IaaSVM-policy i dagar ändrat till 7 från 1</span><span class="sxs-lookup"><span data-stu-id="a52f3-1999">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="a52f3-2000">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a52f3-2000">Az.ServiceBus</span></span>
* <span data-ttu-id="a52f3-2001">Korrigering för ärende #9182 – Get-AzServiceBusNamespace returnerar ResourceGroup istället för ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a52f3-2001">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a52f3-2002">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a52f3-2002">Az.ServiceFabric</span></span>
* <span data-ttu-id="a52f3-2003">Åtgärda stavfel i felmeddelandet för Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="a52f3-2003">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="a52f3-2004">Åtgärda saknat tecken i Service Fabric-kommandorader</span><span class="sxs-lookup"><span data-stu-id="a52f3-2004">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="a52f3-2005">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a52f3-2005">Az.Sql</span></span>
* <span data-ttu-id="a52f3-2006">Lägg till parametern DnsZonePartner för New-AzureSqlInstance-cmdlet för att ge stöd för AutoDr för hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2006">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="a52f3-2007">Avvecklar cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="a52f3-2007">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="a52f3-2008">Döp om cmdletar för hotidentifiering till Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="a52f3-2008">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="a52f3-2009">Parametrarna New-AzSqlInstance -StorageSizeInGB och -LicenseType är nu valfria.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2009">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a52f3-2010">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a52f3-2010">Az.Websites</span></span>
* <span data-ttu-id="a52f3-2011">åtgärdar problemet där användningen av Set-AzWebApp och Set-AzWebAppSlot med -WebApp-egenskap tog bort taggarna</span><span class="sxs-lookup"><span data-stu-id="a52f3-2011">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="a52f3-2012">2.1.0 – maj 2019</span><span class="sxs-lookup"><span data-stu-id="a52f3-2012">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="a52f3-2013">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a52f3-2013">Az.ApiManagement</span></span>
* <span data-ttu-id="a52f3-2014">Skapade nya cmdletar för att hantera diagnostik för global- och API-omfång</span><span class="sxs-lookup"><span data-stu-id="a52f3-2014">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="a52f3-2015">**Get-AzApiManagementDiagnostic** – Skaffa diagnostik konfigurerad för global- eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="a52f3-2015">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="a52f3-2016">**New-AzApiManagementDiagnostic** – Skapa ny diagnostik för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="a52f3-2016">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="a52f3-2017">**New-AzApiManagementHttpMessageDiagnostic** – Skapa diagnostikinställning om vilka rubriker som ska loggas och storleken på brödtextbyte</span><span class="sxs-lookup"><span data-stu-id="a52f3-2017">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="a52f3-2018">**New-AzApiManagementPipelineDiagnosticSetting** – Skapa diagnostikinställningar för inkommande/utgående HTTP-meddelanden till gatewayen.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2018">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="a52f3-2019">**New-AzApiManagementSamplingSetting** – Skapa samplinginställningar för begäranden/svar för en diagnostik</span><span class="sxs-lookup"><span data-stu-id="a52f3-2019">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="a52f3-2020">**Remove-AzApiManagementDiagnostic** – Ta bort en diagnostikenhet för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="a52f3-2020">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="a52f3-2021">**Set-AzApiManagementDiagnostic** – Uppdatera en diagnostikenhet för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="a52f3-2021">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="a52f3-2022">Skapade nya cmdletar för hantering av cacheminne i ApiManagement-tjänsten</span><span class="sxs-lookup"><span data-stu-id="a52f3-2022">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="a52f3-2023">**Get-AzApiManagementCache** – Hämta information om cacheminnet som anges av identifierare eller alla cacheminnen</span><span class="sxs-lookup"><span data-stu-id="a52f3-2023">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="a52f3-2024">**New-AzApiManagementCache** – Skapa ett nytt default-cacheminne eller cacheminne i en viss Azure-region</span><span class="sxs-lookup"><span data-stu-id="a52f3-2024">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="a52f3-2025">**Remove-AzApiManagementCache** – Ta bort ett cacheminne</span><span class="sxs-lookup"><span data-stu-id="a52f3-2025">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="a52f3-2026">**Remove-AzApiManagementCache** – Ta bort ett cacheminne</span><span class="sxs-lookup"><span data-stu-id="a52f3-2026">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="a52f3-2027">Skapade nya cmdletar för hantering av API-schema</span><span class="sxs-lookup"><span data-stu-id="a52f3-2027">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="a52f3-2028">**New-AzApiManagementSchema** – Skapa ett nytt schema för ett API</span><span class="sxs-lookup"><span data-stu-id="a52f3-2028">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="a52f3-2029">**Get-AzApiManagementSchema** – Hämta de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="a52f3-2029">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="a52f3-2030">**Remove-AzApiManagementSchema** – Ta bort de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="a52f3-2030">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="a52f3-2031">**Set-AzApiManagementSchema** – Uppdatera de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="a52f3-2031">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="a52f3-2032">Skapa ny cmdlet för att generera en användartoken.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2032">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="a52f3-2033">**New-AzApiManagementUserToken** – Skapa en ny användartoken som enligt standardinställning är giltig i 8 timmar. Token för GIT-användaren kan skapas med den här cmdleten./</span><span class="sxs-lookup"><span data-stu-id="a52f3-2033">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="a52f3-2034">Skapade en ny cmdlet för att hämta nätverksstatus</span><span class="sxs-lookup"><span data-stu-id="a52f3-2034">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="a52f3-2035">**Get-AzApiManagementNetworkStatus** – Hämta nätverksstatusanslutningen för resurserna som API Management-tjänsten är beroende av.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2035">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="a52f3-2036">Det här är användbart när du distribuerar ApiManagement-tjänsten i ett virtuellt nätverk och validerar om något beroende är brutet.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2036">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="a52f3-2037">Uppdaterade cmdlet **New-AzApiManagement** för att hantera ApiManagement-tjänsten</span><span class="sxs-lookup"><span data-stu-id="a52f3-2037">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="a52f3-2038">Lade till stöd för den nya SKU:n Consumption</span><span class="sxs-lookup"><span data-stu-id="a52f3-2038">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="a52f3-2039">Aktiverade stöd för att slå på flaggan EnableClientCertificate för SKU:n Consumption</span><span class="sxs-lookup"><span data-stu-id="a52f3-2039">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="a52f3-2040">Den nya cmdleten **New-AzApiManagementSslSetting** gör det möjligt att ställa in TLS/SSL-inställningen på ”Backend” och ”Frontend” (serverdel och klientdel).</span><span class="sxs-lookup"><span data-stu-id="a52f3-2040">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="a52f3-2041">Det här kan också användas till att konfigurera chiffer som 3DES och ServerProtocols som Http2 för Frontend för en ApiManagement-tjänst.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2041">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="a52f3-2042">Stöd har lagts till för att konfigurera värdnamnet DeveloperPortal på ApiManagement-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2042">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="a52f3-2043">Uppdaterade cmdletar **Get-AzApiManagementSsoToken** för att ta PsApiManagement-objekt som indata</span><span class="sxs-lookup"><span data-stu-id="a52f3-2043">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="a52f3-2044">Uppdaterad cmdleten för att visa infogade felmeddelanden</span><span class="sxs-lookup"><span data-stu-id="a52f3-2044">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="a52f3-2045">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Felkod: Felmeddelande av typen ValidationError: Ett eller flera fält innehåller felaktiga värden: Felinformation:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="a52f3-2045">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="a52f3-2046">Uppdaterade cmdlet **Export-AzApiManagementApi** för att exportera API:er i OpenApi 3.0-format</span><span class="sxs-lookup"><span data-stu-id="a52f3-2046">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="a52f3-2047">Uppdaterade cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="a52f3-2047">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="a52f3-2048">Importera API från dokumentspecifikationen OpenApi 3.0</span><span class="sxs-lookup"><span data-stu-id="a52f3-2048">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="a52f3-2049">Om du vill åsidosätta egenskapen PsApiManagementSchema specificerad i ett dokument (Swagger, Wadl, Wsdl, OpenApi).</span><span class="sxs-lookup"><span data-stu-id="a52f3-2049">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="a52f3-2050">Åsidosätta egenskapen ServiceUrl som specificeras i ett dokument.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2050">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="a52f3-2051">Uppdaterade cmdlet **Get-AzApiManagementPolicy** för att returnera policy i undantaget format av typen icke-XML med rawxml</span><span class="sxs-lookup"><span data-stu-id="a52f3-2051">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="a52f3-2052">Uppdaterade cmdlet **Set-AzApiManagementPolicy** för att godkänna policy i undantaget format av typen icke-XML med rawxml och XML undantaget med xml</span><span class="sxs-lookup"><span data-stu-id="a52f3-2052">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="a52f3-2053">Uppdaterad cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="a52f3-2053">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="a52f3-2054">Konfigurera API med OpenId auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2054">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="a52f3-2055">Skapa ett API i ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="a52f3-2055">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="a52f3-2056">Klona ett API med SourceApiId och SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2056">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="a52f3-2057">Möjlighet att konfigurera SubscriptionRequired i API-omfattningen.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2057">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="a52f3-2058">Uppdaterad cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="a52f3-2058">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="a52f3-2059">Konfigurera API med OpenId auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2059">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="a52f3-2060">Uppdatera ett API till ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="a52f3-2060">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="a52f3-2061">Möjlighet att konfigurera SubscriptionRequired i API-omfattningen.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2061">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="a52f3-2062">Uppdaterad cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="a52f3-2062">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="a52f3-2063">Klona en befintlig version med hjälp av SourceApiRevision (kopiera taggar, produkter, åtgärder och principer).</span><span class="sxs-lookup"><span data-stu-id="a52f3-2063">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="a52f3-2064">Den nya revisionen antar ApiId från den överordnade instansen.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2064">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="a52f3-2065">Tillhandahålla ApiRevisionDescription</span><span class="sxs-lookup"><span data-stu-id="a52f3-2065">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="a52f3-2066">Åsidosätta ServiceUrl vid kloning av ett API.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2066">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="a52f3-2067">Uppdaterad cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="a52f3-2067">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="a52f3-2068">Konfigurera AAD eller AADB2C med en Authority</span><span class="sxs-lookup"><span data-stu-id="a52f3-2068">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="a52f3-2069">Konfigurera SignupPolicy, SigninPolicy, ProfileEditingPolicy och PasswordResetPolicy</span><span class="sxs-lookup"><span data-stu-id="a52f3-2069">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="a52f3-2070">Uppdaterad cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="a52f3-2070">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="a52f3-2071">Kompensera för ny SubscriptonModel med Scope och UserId</span><span class="sxs-lookup"><span data-stu-id="a52f3-2071">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="a52f3-2072">Kompensera för gammal prenumerationsmodell med ProductId och UserId</span><span class="sxs-lookup"><span data-stu-id="a52f3-2072">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="a52f3-2073">Lägg till funktion för att aktivera AllowTracing på prenumerationsnivå.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2073">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="a52f3-2074">Uppdaterad cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="a52f3-2074">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="a52f3-2075">Kompensera för ny SubscriptonModel med Scope och UserId</span><span class="sxs-lookup"><span data-stu-id="a52f3-2075">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="a52f3-2076">Kompensera för gammal prenumerationsmodell med ProductId och UserId</span><span class="sxs-lookup"><span data-stu-id="a52f3-2076">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="a52f3-2077">Lägg till funktion för att aktivera AllowTracing på prenumerationsnivå.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2077">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="a52f3-2078">Uppdaterade följande cmdletar för att acceptera ResourceId som indata</span><span class="sxs-lookup"><span data-stu-id="a52f3-2078">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="a52f3-2079">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a52f3-2079">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="a52f3-2080">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="a52f3-2080">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="a52f3-2081">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="a52f3-2081">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="a52f3-2082">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="a52f3-2082">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="a52f3-2083">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="a52f3-2083">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="a52f3-2084">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="a52f3-2084">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="a52f3-2085">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="a52f3-2085">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="a52f3-2086">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="a52f3-2086">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="a52f3-2087">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="a52f3-2087">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="a52f3-2088">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="a52f3-2088">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="a52f3-2089">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="a52f3-2089">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="a52f3-2090">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="a52f3-2090">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a52f3-2091">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a52f3-2091">Az.Automation</span></span>
* <span data-ttu-id="a52f3-2092">Uppdaterade Get-AzAutomationJobOutputRecord för att hantera postvärden av typen JSON och Text.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2092">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="a52f3-2093">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="a52f3-2093">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="a52f3-2094">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="a52f3-2094">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="a52f3-2095">Ändrade beteende för Start-AzAutomationDscCompilationJob till att bara starta jobbet istället för att vänta på slutförandet.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2095">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="a52f3-2096">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="a52f3-2096">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="a52f3-2097">Korrigering för Get-AzAutomationDscNode när using -Name returnerar alla noder.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2097">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="a52f3-2098">Nu returnerar den endast den matchande noden.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2098">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a52f3-2099">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a52f3-2099">Az.Compute</span></span>
* <span data-ttu-id="a52f3-2100">Lägg till parametrarna ProtectFromScaleIn och ProtectFromScaleSetAction i cmdleten Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2100">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="a52f3-2101">Nu är standardinställningen att vimpelparametern New-AzVM använder en tillgänglig plats om USA, östra inte stöds</span><span class="sxs-lookup"><span data-stu-id="a52f3-2101">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a52f3-2102">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a52f3-2102">Az.DataLakeStore</span></span>
* <span data-ttu-id="a52f3-2103">Uppdatera ADLS-sdk för att använda httpclient, integrera dataplanstestning med Azure-ramverk</span><span class="sxs-lookup"><span data-stu-id="a52f3-2103">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a52f3-2104">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a52f3-2104">Az.Monitor</span></span>
* <span data-ttu-id="a52f3-2105">Korrigera felaktiga parameternamn i hjälpexempel</span><span class="sxs-lookup"><span data-stu-id="a52f3-2105">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a52f3-2106">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a52f3-2106">Az.Network</span></span>
* <span data-ttu-id="a52f3-2107">Lägg till flaggan DisableBgpRoutePropagation i utdata för effektiv routningstabell</span><span class="sxs-lookup"><span data-stu-id="a52f3-2107">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="a52f3-2108">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="a52f3-2108">Updated cmdlet:</span></span>
        - <span data-ttu-id="a52f3-2109">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="a52f3-2109">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="a52f3-2110">Åtgärda dubbelstreck i dokumentationen New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="a52f3-2110">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="a52f3-2111">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a52f3-2111">Az.Resources</span></span>
* <span data-ttu-id="a52f3-2112">Lägg till ny cmdlet Get-AzureRmDenyAssignment för att hämta tilldelningsnekanden</span><span class="sxs-lookup"><span data-stu-id="a52f3-2112">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="a52f3-2113">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a52f3-2113">Az.Sql</span></span>
* <span data-ttu-id="a52f3-2114">Döp om Advanced Threat Protection-cmdletar för Advanced Data Security och aktivera Vulnerability Assessment som standard</span><span class="sxs-lookup"><span data-stu-id="a52f3-2114">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="a52f3-2115">2.0.0 – maj 2019</span><span class="sxs-lookup"><span data-stu-id="a52f3-2115">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a52f3-2116">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a52f3-2116">Az.Accounts</span></span>
* <span data-ttu-id="a52f3-2117">Uppdatera autentiseringsbiblioteket för att åtgärda ADFS-problem med autentisering av användarnamn/lösenord</span><span class="sxs-lookup"><span data-stu-id="a52f3-2117">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="a52f3-2118">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a52f3-2118">Az.CognitiveServices</span></span>
* <span data-ttu-id="a52f3-2119">Visa endast Bing-ansvarsfriskrivning för Bing-sökningstjänster.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2119">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="a52f3-2120">Förbättra felmeddelande när det inte går att skapa konton.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2120">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a52f3-2121">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a52f3-2121">Az.Compute</span></span>
* <span data-ttu-id="a52f3-2122">Funktion för närhetsplaceringsgrupper.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2122">Proximity placement group feature.</span></span>
    - <span data-ttu-id="a52f3-2123">Följande nya cmdletar har lagts till:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="a52f3-2123">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="a52f3-2124">Den nya parametern ProximityPlacementGroupId har lagts till i följande cmdletar:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="a52f3-2124">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="a52f3-2125">Parametern StorageAccountType har lagts till i New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2125">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="a52f3-2126">TargetRegion för New-AzGalleryImageVersion kan innehålla StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2126">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="a52f3-2127">Växlingsparametern SkipShutdown har lagts till i Stop-AzVM och Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a52f3-2127">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="a52f3-2128">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="a52f3-2128">Breaking changes</span></span>
    - <span data-ttu-id="a52f3-2129">Set-AzVMBootDiagnostics har ändrats till Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2129">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="a52f3-2130">Export-AzLogAnalyticThrottledRequests har ändrats till Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2130">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="a52f3-2131">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="a52f3-2131">Az.DeploymentManager</span></span>
* <span data-ttu-id="a52f3-2132">De första allmänt tillgängliga versionerna av cmdletar för Distributionshanteraren i Azure</span><span class="sxs-lookup"><span data-stu-id="a52f3-2132">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="a52f3-2133">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="a52f3-2133">Az.Dns</span></span>
* <span data-ttu-id="a52f3-2134">Automatisk delegering av DNS för NameServer</span><span class="sxs-lookup"><span data-stu-id="a52f3-2134">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="a52f3-2135">Det överordnade zonnamnet kan användas som ytterligare valfri parameter i cmdleten för att skapa DNS-zoner.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2135">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="a52f3-2136">Lägger till NS-poster för en nyligen skapad underordnad zon i den överordnade zonen.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2136">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="a52f3-2137">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="a52f3-2137">Az.FrontDoor</span></span>
* <span data-ttu-id="a52f3-2138">De första allmänt tillgängliga versionerna av cmdletar för Azure FrontDoor</span><span class="sxs-lookup"><span data-stu-id="a52f3-2138">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="a52f3-2139">Byt namn på WAF-cmdletar så att de omfattar ”Waf”</span><span class="sxs-lookup"><span data-stu-id="a52f3-2139">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="a52f3-2140">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a52f3-2140">Az.HDInsight</span></span>
* <span data-ttu-id="a52f3-2141">Två cmdletar har tagits bort:</span><span class="sxs-lookup"><span data-stu-id="a52f3-2141">Removed two cmdlets:</span></span>
    - <span data-ttu-id="a52f3-2142">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="a52f3-2142">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="a52f3-2143">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="a52f3-2143">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="a52f3-2144">En ny cmdlet har lagts till, Set-AzHDInsightGatewayCredential, som ersätter Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="a52f3-2144">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="a52f3-2145">Uppdatera cmdleten Get-AzHDInsightJobOutput för att skilja mellan läsarrollen och HDInsight-operatörsrollen:</span><span class="sxs-lookup"><span data-stu-id="a52f3-2145">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="a52f3-2146">Användare med läsarrollen måste uttryckligen ange parametern ”DefaultStorageAccountKey”, annars uppstår fel.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2146">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="a52f3-2147">Användare med HDInsight-operatörsrollen påverkas inte.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2147">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a52f3-2148">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a52f3-2148">Az.Monitor</span></span>
* <span data-ttu-id="a52f3-2149">Nya cmdletar för SQR API (schemalagd frågeregel)</span><span class="sxs-lookup"><span data-stu-id="a52f3-2149">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="a52f3-2150">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="a52f3-2150">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="a52f3-2151">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="a52f3-2151">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="a52f3-2152">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="a52f3-2152">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="a52f3-2153">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="a52f3-2153">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="a52f3-2154">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="a52f3-2154">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="a52f3-2155">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="a52f3-2155">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="a52f3-2156">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="a52f3-2156">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="a52f3-2157">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="a52f3-2157">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="a52f3-2158">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="a52f3-2158">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="a52f3-2159">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="a52f3-2159">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="a52f3-2160">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="a52f3-2160">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="a52f3-2161">[Mer](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information om SQR API</span><span class="sxs-lookup"><span data-stu-id="a52f3-2161">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="a52f3-2162">Az.Monitor.md har uppdaterats för att omfatta cmdletar för måttbaserade aviseringsregler i GenV2 (inte klassiska)</span><span class="sxs-lookup"><span data-stu-id="a52f3-2162">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a52f3-2163">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a52f3-2163">Az.Network</span></span>
* <span data-ttu-id="a52f3-2164">Lägg till stöd för NAT Gateway-resurs</span><span class="sxs-lookup"><span data-stu-id="a52f3-2164">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="a52f3-2165">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="a52f3-2165">New cmdlets</span></span>
        - <span data-ttu-id="a52f3-2166">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="a52f3-2166">New-AzNatGateway</span></span>
        - <span data-ttu-id="a52f3-2167">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="a52f3-2167">Get-AzNatGateway</span></span>
        - <span data-ttu-id="a52f3-2168">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="a52f3-2168">Set-AzNatGateway</span></span>
        - <span data-ttu-id="a52f3-2169">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="a52f3-2169">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="a52f3-2170">Uppdaterade cmdletar</span><span class="sxs-lookup"><span data-stu-id="a52f3-2170">Updated cmdlets</span></span>
        - <span data-ttu-id="a52f3-2171">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="a52f3-2171">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="a52f3-2172">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="a52f3-2172">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="a52f3-2173">Nedanstående kommandon för funktionen har uppdaterats: Ange/ta bort anpassade vägar på Brooklyn Gateway.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2173">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="a52f3-2174">New-AzVirtualNetworkGateway har uppdaterats: Den valfria parametern -CustomRoute har lagts till för att ställa in adressprefix som anpassade vägar för att ange gateway.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2174">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="a52f3-2175">Set-AzVirtualNetworkGateway har uppdaterats: Den valfria parametern -CustomRoute har lagts till för att ange adressprefix som anpassade vägar för att ange gateway.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2175">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="a52f3-2176">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a52f3-2176">Az.PolicyInsights</span></span>
* <span data-ttu-id="a52f3-2177">Stöd för att fråga efter information om principutvärdering.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2177">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="a52f3-2178">Lägg till parametern ”-Expand” för Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2178">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="a52f3-2179">Stöd för -Expand PolicyEvaluationDetails.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2179">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a52f3-2180">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a52f3-2180">Az.RecoveryServices</span></span>
* <span data-ttu-id="a52f3-2181">Stöd för att dela prenumeration mellan Azure och Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2181">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="a52f3-2182">Markering av kommande icke-bakåtkompatibla ändringar för Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2182">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="a52f3-2183">Korrigering för återställningsplan och åtgärdsplan i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2183">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="a52f3-2184">Korrigering för mappning av uppdateringsnätverk i Azure Site Recovery för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2184">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="a52f3-2185">Korrigering för instruktioner för uppdateringsskydd i Azure Site Recovery för Azure till Azure för hanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2185">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="a52f3-2186">Andra mindre korrigeringar.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2186">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="a52f3-2187">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="a52f3-2187">Az.Relay</span></span>
* <span data-ttu-id="a52f3-2188">Korrigera stavfel i kundriktade meddelanden</span><span class="sxs-lookup"><span data-stu-id="a52f3-2188">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="a52f3-2189">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a52f3-2189">Az.ServiceBus</span></span>
* <span data-ttu-id="a52f3-2190">Nya cmdletar har lagts till för NetworkRuleSet för namnområden</span><span class="sxs-lookup"><span data-stu-id="a52f3-2190">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a52f3-2191">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a52f3-2191">Az.Storage</span></span>
* <span data-ttu-id="a52f3-2192">Uppgradera till lagringsklientbiblioteket 10.0.1 (namnområdet för alla objekt från detta SDK ändras från ”Microsoft.WindowsAzure.Storage. *till ”Microsoft.Azure.Storage.* ”)</span><span class="sxs-lookup"><span data-stu-id="a52f3-2192">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="a52f3-2193">Uppgradera till Microsoft.Azure.Management.Storage 11.0.0 för att stödja den nya API-versionen 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2193">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="a52f3-2194">Standardlagringskontot i Skapa lagringskonto ändras från ”Storage” till ”StorageV2”</span><span class="sxs-lookup"><span data-stu-id="a52f3-2194">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="a52f3-2195">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a52f3-2195">New-AzStorageAccount</span></span>
* <span data-ttu-id="a52f3-2196">Ändra lagringskontots cmdlet-utdata Sku.Name för att passa med indata-SkuName genom att lägga till ”-”. Till exempel ändras ”StandardLRS” till ”Standard_LRS”</span><span class="sxs-lookup"><span data-stu-id="a52f3-2196">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="a52f3-2197">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a52f3-2197">New-AzStorageAccount</span></span>
    - <span data-ttu-id="a52f3-2198">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a52f3-2198">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="a52f3-2199">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a52f3-2199">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a52f3-2200">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a52f3-2200">Az.Websites</span></span>
* <span data-ttu-id="a52f3-2201">Egenskapen ”typ” konfigureras nu för PSSite-objekt som returneras av Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a52f3-2201">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="a52f3-2202">Get-AzWebApp\*Metrics och Get-AzAppServicePlanMetrics markeras som inaktuella</span><span class="sxs-lookup"><span data-stu-id="a52f3-2202">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="a52f3-2203">1.8.0 – april 2019</span><span class="sxs-lookup"><span data-stu-id="a52f3-2203">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="a52f3-2204">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="a52f3-2204">Highlights since the last major release</span></span>
* <span data-ttu-id="a52f3-2205">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="a52f3-2205">General availability of `Az` module</span></span>
* <span data-ttu-id="a52f3-2206">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="a52f3-2206">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="a52f3-2207">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="a52f3-2207">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="a52f3-2208">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="a52f3-2208">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="a52f3-2209">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="a52f3-2209">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="a52f3-2210">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="a52f3-2210">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="a52f3-2211">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="a52f3-2211">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="a52f3-2212">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a52f3-2212">Az.Accounts</span></span>
* <span data-ttu-id="a52f3-2213">Uppdatera Uninstall-AzureRm för att ta bort moduler i Mac på ett korrekt sätt</span><span class="sxs-lookup"><span data-stu-id="a52f3-2213">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="a52f3-2214">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="a52f3-2214">Az.Batch</span></span>
* <span data-ttu-id="a52f3-2215">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2215">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="a52f3-2216">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="a52f3-2216">Az.Cdn</span></span>
* <span data-ttu-id="a52f3-2217">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2217">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="a52f3-2218">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a52f3-2218">Az.CognitiveServices</span></span>
* <span data-ttu-id="a52f3-2219">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2219">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a52f3-2220">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a52f3-2220">Az.Compute</span></span>
* <span data-ttu-id="a52f3-2221">Åtgärda problem med AEM-installationen om resurs-ID:n för diskar innehåller resourcegroups i gemener i resurs-ID:n</span><span class="sxs-lookup"><span data-stu-id="a52f3-2221">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="a52f3-2222">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2222">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="a52f3-2223">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="a52f3-2223">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a52f3-2224">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a52f3-2224">Az.DataFactory</span></span>
* <span data-ttu-id="a52f3-2225">Lägg till SsisProperties om NodeCount inte är null för hanterad integreringskörning.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2225">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a52f3-2226">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a52f3-2226">Az.DataLakeStore</span></span>
* <span data-ttu-id="a52f3-2227">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2227">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="a52f3-2228">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="a52f3-2228">Az.EventGrid</span></span>
* <span data-ttu-id="a52f3-2229">Hjälptexten för slutpunkten har uppdaterats för att visa att resurser ska skapas innan cmdletarna för att skapa/uppdatera händelseprenumerationer används.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2229">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="a52f3-2230">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a52f3-2230">Az.EventHub</span></span>
* <span data-ttu-id="a52f3-2231">Nya cmdletar har lagts till för NetworkRuleSet för namnområden</span><span class="sxs-lookup"><span data-stu-id="a52f3-2231">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="a52f3-2232">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a52f3-2232">Az.HDInsight</span></span>
* <span data-ttu-id="a52f3-2233">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2233">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a52f3-2234">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a52f3-2234">Az.IotHub</span></span>
* <span data-ttu-id="a52f3-2235">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2235">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a52f3-2236">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a52f3-2236">Az.KeyVault</span></span>
* <span data-ttu-id="a52f3-2237">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2237">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="a52f3-2238">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="a52f3-2238">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="a52f3-2239">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="a52f3-2239">Az.MachineLearning</span></span>
* <span data-ttu-id="a52f3-2240">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2240">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="a52f3-2241">Az.Media</span><span class="sxs-lookup"><span data-stu-id="a52f3-2241">Az.Media</span></span>
* <span data-ttu-id="a52f3-2242">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2242">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a52f3-2243">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a52f3-2243">Az.Monitor</span></span>
  * <span data-ttu-id="a52f3-2244">Nya cmdletar för måttbaserad aviseringsregel i GenV2 (inte klassisk)</span><span class="sxs-lookup"><span data-stu-id="a52f3-2244">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="a52f3-2245">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="a52f3-2245">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="a52f3-2246">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="a52f3-2246">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="a52f3-2247">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="a52f3-2247">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="a52f3-2248">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="a52f3-2248">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="a52f3-2249">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="a52f3-2249">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="a52f3-2250">Monitor SDK har uppdaterats till version 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="a52f3-2250">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a52f3-2251">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a52f3-2251">Az.Network</span></span>
* <span data-ttu-id="a52f3-2252">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2252">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="a52f3-2253">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="a52f3-2253">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="a52f3-2254">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="a52f3-2254">Az.NotificationHubs</span></span>
* <span data-ttu-id="a52f3-2255">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2255">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="a52f3-2256">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a52f3-2256">Az.OperationalInsights</span></span>
* <span data-ttu-id="a52f3-2257">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2257">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="a52f3-2258">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="a52f3-2258">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="a52f3-2259">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2259">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a52f3-2260">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a52f3-2260">Az.RecoveryServices</span></span>
* <span data-ttu-id="a52f3-2261">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2261">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="a52f3-2262">Tabellformatet för SQL i virtuella Azure-datorer har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="a52f3-2262">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="a52f3-2263">En alternativ metod för att hämta platser i AzureFileShare har lagts till</span><span class="sxs-lookup"><span data-stu-id="a52f3-2263">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="a52f3-2264">ScheduleRunDays i SchedulePolicy-objekt har uppdaterats enligt tidszon</span><span class="sxs-lookup"><span data-stu-id="a52f3-2264">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="a52f3-2265">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="a52f3-2265">Az.RedisCache</span></span>
* <span data-ttu-id="a52f3-2266">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2266">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a52f3-2267">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a52f3-2267">Az.Resources</span></span>
* <span data-ttu-id="a52f3-2268">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="a52f3-2268">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="a52f3-2269">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a52f3-2269">Az.Sql</span></span>
* <span data-ttu-id="a52f3-2270">Ersätt Monitor SDK-beroende med vanlig kod</span><span class="sxs-lookup"><span data-stu-id="a52f3-2270">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="a52f3-2271">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2271">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="a52f3-2272">Förbättrad process för klassificering av flera kolumner.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2272">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="a52f3-2273">Inkludera SKU-egenskaper (SKU-namn, serie, kapacitet) i svaret från Get-AzSqlServerServiceObjective och formatera som tabell som standard.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2273">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="a52f3-2274">Möjlighet att använda Get-AzSqlServerServiceObjective efter plats utan att behöva en redan befintlig server i regionen.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2274">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="a52f3-2275">Stöd för tidszonsparametern när hanterade instanser skapas.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2275">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="a52f3-2276">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="a52f3-2276">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a52f3-2277">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a52f3-2277">Az.Websites</span></span>
* <span data-ttu-id="a52f3-2278">åtgärdar Set-AzWebApp och Set-AzWebAppSlot så att de inte tar bort taggar vid körning</span><span class="sxs-lookup"><span data-stu-id="a52f3-2278">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="a52f3-2279">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2279">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="a52f3-2280">SDK för WebSites har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2280">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="a52f3-2281">Egenskapen AdminSiteName har tagits bort från PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2281">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="a52f3-2282">1.7.0 – april 2019</span><span class="sxs-lookup"><span data-stu-id="a52f3-2282">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="a52f3-2283">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="a52f3-2283">Highlights since the last major release</span></span>
* <span data-ttu-id="a52f3-2284">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="a52f3-2284">General availability of `Az` module</span></span>
* <span data-ttu-id="a52f3-2285">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="a52f3-2285">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="a52f3-2286">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="a52f3-2286">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="a52f3-2287">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="a52f3-2287">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="a52f3-2288">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="a52f3-2288">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="a52f3-2289">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="a52f3-2289">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="a52f3-2290">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="a52f3-2290">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="a52f3-2291">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a52f3-2291">Az.Accounts</span></span>
* <span data-ttu-id="a52f3-2292">Add-AzEnvironment och Set-AzEnvironment har uppdaterats för att godkänna parametern AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="a52f3-2292">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="a52f3-2293">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a52f3-2293">Az.AnalysisServices</span></span>
* <span data-ttu-id="a52f3-2294">ServiceClient används i cmdletar för dataplan och den ursprungliga autentiseringslogiken har tagits bort</span><span class="sxs-lookup"><span data-stu-id="a52f3-2294">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="a52f3-2295">Add-AzureASAccount används för omslutning av Connect-AzAccount för att undvika en icke-bakåtkompatibel ändring</span><span class="sxs-lookup"><span data-stu-id="a52f3-2295">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a52f3-2296">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a52f3-2296">Az.Automation</span></span>
* <span data-ttu-id="a52f3-2297">Buggen för cmdleten New-AzAutomationSoftwareUpdateConfiguration för inkluderingar har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2297">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="a52f3-2298">Nu bör parametern IncludedKbNumber och IncludedPackageNameMask fungera.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2298">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="a52f3-2299">Felkorrigering för dynamiska grupper i uppdateringshanteringen för azure automation</span><span class="sxs-lookup"><span data-stu-id="a52f3-2299">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a52f3-2300">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a52f3-2300">Az.Compute</span></span>
* <span data-ttu-id="a52f3-2301">Lägg till parametern HyperVGeneration i New-AzDiskConfig och New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="a52f3-2301">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="a52f3-2302">Tillåt att virtuella datorer skapas med galleribilder från andra klientorganisationer.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2302">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="a52f3-2303">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="a52f3-2303">Az.ContainerInstance</span></span>
* <span data-ttu-id="a52f3-2304">Ett problem har åtgärdats i parametern -Command för New-AzContainerGroup som lade till ett avslutande tomt argument</span><span class="sxs-lookup"><span data-stu-id="a52f3-2304">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a52f3-2305">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a52f3-2305">Az.DataFactory</span></span>
* <span data-ttu-id="a52f3-2306">ADF .Net SDK-versionen har uppdaterats till 3.0.2</span><span class="sxs-lookup"><span data-stu-id="a52f3-2306">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="a52f3-2307">Cmdleten Set-AzDataFactoryV2 har uppdaterats med extra parametrar för inställningar som rör RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2307">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a52f3-2308">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a52f3-2308">Az.Resources</span></span>
* <span data-ttu-id="a52f3-2309">Förbättra hanteringen av providrar för Get-AzResource när parametrarna -ResourceId eller -ResourceGroupName, -Name och -ResourceType tillhandahålls</span><span class="sxs-lookup"><span data-stu-id="a52f3-2309">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="a52f3-2310">Förbättra felhanteringen för ”Test-AzDeployment” och ”Test-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="a52f3-2310">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="a52f3-2311">Hantera fel utanför distributionsvalideringen och ta med dem i kommandoutdata istället</span><span class="sxs-lookup"><span data-stu-id="a52f3-2311">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="a52f3-2312">Mer information här: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="a52f3-2312">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="a52f3-2313">Lägg till växlingsparametern -IgnoreDynamicParameters till en uppsättning av cmdletar för distribution för att hoppa över fråga i skript och jobbscenarier</span><span class="sxs-lookup"><span data-stu-id="a52f3-2313">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="a52f3-2314">Mer information här: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="a52f3-2314">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="a52f3-2315">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a52f3-2315">Az.Sql</span></span>
* <span data-ttu-id="a52f3-2316">Stöd för dataklassificering av databaser.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2316">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a52f3-2317">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a52f3-2317">Az.Storage</span></span>
* <span data-ttu-id="a52f3-2318">Rapportera detaljfel när lagringskontext skapas med parametern -UseConnectedAccount, men utan inloggning på Azure-kontot</span><span class="sxs-lookup"><span data-stu-id="a52f3-2318">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="a52f3-2319">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="a52f3-2319">New-AzStorageContext</span></span>
* <span data-ttu-id="a52f3-2320">Stöd för att hantera Blob Service-egenskaper för ett angivet lagringskonto med API:et för hanteringsplan</span><span class="sxs-lookup"><span data-stu-id="a52f3-2320">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="a52f3-2321">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="a52f3-2321">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="a52f3-2322">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="a52f3-2322">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="a52f3-2323">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="a52f3-2323">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="a52f3-2324">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="a52f3-2324">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="a52f3-2325">Stöd för -AsJob-cmdletar för att ladda upp och ladda ned blobar och filer</span><span class="sxs-lookup"><span data-stu-id="a52f3-2325">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="a52f3-2326">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="a52f3-2326">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="a52f3-2327">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="a52f3-2327">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="a52f3-2328">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="a52f3-2328">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="a52f3-2329">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="a52f3-2329">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="a52f3-2330">1.6.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="a52f3-2330">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="a52f3-2331">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="a52f3-2331">Highlights since the last major release</span></span>
* <span data-ttu-id="a52f3-2332">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="a52f3-2332">General availability of `Az` module</span></span>
* <span data-ttu-id="a52f3-2333">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="a52f3-2333">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="a52f3-2334">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="a52f3-2334">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="a52f3-2335">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="a52f3-2335">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="a52f3-2336">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="a52f3-2336">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="a52f3-2337">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="a52f3-2337">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="a52f3-2338">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="a52f3-2338">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a52f3-2339">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a52f3-2339">Az.Automation</span></span>
* <span data-ttu-id="a52f3-2340">Azure Automation – ändring av uppdateringshantering för stöd för de nya funktionerna:</span><span class="sxs-lookup"><span data-stu-id="a52f3-2340">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="a52f3-2341">Dynamisk gruppering</span><span class="sxs-lookup"><span data-stu-id="a52f3-2341">Dynamic grouping</span></span>
    * <span data-ttu-id="a52f3-2342">För-/efterskrift</span><span class="sxs-lookup"><span data-stu-id="a52f3-2342">Pre-Post script</span></span>
    * <span data-ttu-id="a52f3-2343">Inställning för omstart</span><span class="sxs-lookup"><span data-stu-id="a52f3-2343">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a52f3-2344">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a52f3-2344">Az.Compute</span></span>
* <span data-ttu-id="a52f3-2345">Åtgärda problem med sökvägsmatchning i Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="a52f3-2345">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="a52f3-2346">Uppdatera Compute-klientbibliotek till 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2346">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a52f3-2347">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a52f3-2347">Az.KeyVault</span></span>
* <span data-ttu-id="a52f3-2348">Stöd för jokertecken för KeyVault-cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="a52f3-2348">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a52f3-2349">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a52f3-2349">Az.Network</span></span>
* <span data-ttu-id="a52f3-2350">Lägg till stöd för Threat Intelligence för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="a52f3-2350">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="a52f3-2351">Lägg till resurs för brandväggsprincip på översta nivå och anpassade regler för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="a52f3-2351">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a52f3-2352">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a52f3-2352">Az.RecoveryServices</span></span>
* <span data-ttu-id="a52f3-2353">SnapshotRetentionInDays har lagts till i Azure-principen för virtuella datorer för stöd av Instant RP</span><span class="sxs-lookup"><span data-stu-id="a52f3-2353">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="a52f3-2354">Pipe-stöd för avregistrering av container har lagts till</span><span class="sxs-lookup"><span data-stu-id="a52f3-2354">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="a52f3-2355">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a52f3-2355">Az.Resources</span></span>
* <span data-ttu-id="a52f3-2356">Uppdatera stöd för jokertecken för Get-AzResource och Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a52f3-2356">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="a52f3-2357">Uppdatera autentiseringsuppgifter som används vid allmänna anrop till ARM</span><span class="sxs-lookup"><span data-stu-id="a52f3-2357">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="a52f3-2358">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a52f3-2358">Az.Sql</span></span>
* <span data-ttu-id="a52f3-2359">Cmdlet-parametern (ExcludeDetectionType) för Hotidentifiering ändrades från DetectionType till sträng[] för att framtidssäkra den när nya DetectionTypes läggs till, och även för att stödja automatisk ifyllning.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2359">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a52f3-2360">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a52f3-2360">Az.Storage</span></span>
* <span data-ttu-id="a52f3-2361">Stöd för att hämta/ange/ta bort hanteringsprincip på ett lagringskonto</span><span class="sxs-lookup"><span data-stu-id="a52f3-2361">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="a52f3-2362">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="a52f3-2362">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="a52f3-2363">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="a52f3-2363">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="a52f3-2364">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="a52f3-2364">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="a52f3-2365">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="a52f3-2365">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="a52f3-2366">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="a52f3-2366">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="a52f3-2367">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="a52f3-2367">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a52f3-2368">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a52f3-2368">Az.Websites</span></span>
* <span data-ttu-id="a52f3-2369">Åtgärda fel med ARM-mall som avbryter kloning av alla platser med 'New-AzWebApp -IncludeSourceWebAppSlots'</span><span class="sxs-lookup"><span data-stu-id="a52f3-2369">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="a52f3-2370">1.5.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="a52f3-2370">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a52f3-2371">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a52f3-2371">Az.Accounts</span></span>
* <span data-ttu-id="a52f3-2372">Lägg till kommandot Register-AzModule för stöd för AutoRest-genererade cmdletar</span><span class="sxs-lookup"><span data-stu-id="a52f3-2372">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="a52f3-2373">Uppdatera exempel för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="a52f3-2373">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a52f3-2374">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a52f3-2374">Az.Automation</span></span>
* <span data-ttu-id="a52f3-2375">Problem med att hämta vissa månadsscheman i flera Azure Automation-cmdletar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="a52f3-2375">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="a52f3-2376">Åtgärda problem med att Get-AzAutomationDscNode bara returnerar de 20 översta noderna.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2376">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="a52f3-2377">Nu returneras alla noder</span><span class="sxs-lookup"><span data-stu-id="a52f3-2377">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="a52f3-2378">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="a52f3-2378">Az.Cdn</span></span>
* <span data-ttu-id="a52f3-2379">Nya Powershell-cmdletar för att aktivera/inaktivera anpassade domän-HTTPS har lagts till och de gamla har gjorts inaktuella</span><span class="sxs-lookup"><span data-stu-id="a52f3-2379">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a52f3-2380">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a52f3-2380">Az.Compute</span></span>
* <span data-ttu-id="a52f3-2381">Lägg till stöd för jokertecken för Get-cmdletar</span><span class="sxs-lookup"><span data-stu-id="a52f3-2381">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a52f3-2382">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a52f3-2382">Az.DataFactory</span></span>
* <span data-ttu-id="a52f3-2383">ADF .Net SDK-versionen har uppdaterats till 3.0.1</span><span class="sxs-lookup"><span data-stu-id="a52f3-2383">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="a52f3-2384">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="a52f3-2384">Az.LogicApp</span></span>
* <span data-ttu-id="a52f3-2385">Åtgärda problemet med att ListWorkflows endast hämtar den första sidan med resultat</span><span class="sxs-lookup"><span data-stu-id="a52f3-2385">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a52f3-2386">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a52f3-2386">Az.Network</span></span>
* <span data-ttu-id="a52f3-2387">Lägg till stöd för jokertecken för Network-cmdletar</span><span class="sxs-lookup"><span data-stu-id="a52f3-2387">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a52f3-2388">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a52f3-2388">Az.RecoveryServices</span></span>
* <span data-ttu-id="a52f3-2389">Stöd har lagts till för SQL Server i virtuella Azure-datorer</span><span class="sxs-lookup"><span data-stu-id="a52f3-2389">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="a52f3-2390">SDK-uppdatering</span><span class="sxs-lookup"><span data-stu-id="a52f3-2390">SDK Update</span></span>
* <span data-ttu-id="a52f3-2391">Get-ProtectableItem-incheckning i VMappContainer har tagits bort</span><span class="sxs-lookup"><span data-stu-id="a52f3-2391">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="a52f3-2392">Name och ServerName har lagts till som parametrar för Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="a52f3-2392">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="a52f3-2393">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a52f3-2393">Az.Resources</span></span>
* <span data-ttu-id="a52f3-2394">Lägg till parametern `-TemplateObject` i cmdletar för distribution</span><span class="sxs-lookup"><span data-stu-id="a52f3-2394">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="a52f3-2395">Mer information här: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="a52f3-2395">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="a52f3-2396">Åtgärda problem med piping av resultatet i `Get-AzResource` till `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="a52f3-2396">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="a52f3-2397">Mer information här: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="a52f3-2397">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="a52f3-2398">Åtgärda problem med ändring av JSON-datatyp när `Set-AzResource` körs</span><span class="sxs-lookup"><span data-stu-id="a52f3-2398">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="a52f3-2399">Mer information här: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="a52f3-2399">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="a52f3-2400">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a52f3-2400">Az.Sql</span></span>
* <span data-ttu-id="a52f3-2401">AuditingEndpointsCommunicator uppdateras.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2401">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="a52f3-2402">Åtgärdar beteendet hos ett gränsscenario när nya diagnostikinställningar skapas.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2402">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a52f3-2403">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a52f3-2403">Az.Storage</span></span>
* <span data-ttu-id="a52f3-2404">Stöd för BlockBlobStorage när Storage-konto skapas      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a52f3-2404">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="a52f3-2405">1.4.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="a52f3-2405">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="a52f3-2406">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a52f3-2406">Az.AnalysisServices</span></span>
* <span data-ttu-id="a52f3-2407">Inaktuell AddAzureASAccount-cmdlet</span><span class="sxs-lookup"><span data-stu-id="a52f3-2407">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a52f3-2408">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a52f3-2408">Az.Automation</span></span>
* <span data-ttu-id="a52f3-2409">Hjälpen för Import-AzAutomationDscNodeConfiguration har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="a52f3-2409">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="a52f3-2410">Konfigurationsnamnsvalidering har lagts till i cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="a52f3-2410">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="a52f3-2411">Förbättrad felhantering för cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="a52f3-2411">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="a52f3-2412">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a52f3-2412">Az.CognitiveServices</span></span>
* <span data-ttu-id="a52f3-2413">CustomSubdomainName har lagts till som en ny valfri parameter för New-AzCognitiveServicesAccount, som används för att ange underdomän för resursen.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2413">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a52f3-2414">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a52f3-2414">Az.Compute</span></span>
* <span data-ttu-id="a52f3-2415">Problemet med ID-parameteruppsättningar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="a52f3-2415">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="a52f3-2416">Get-AzVMExtension har uppdaterats så att alla installerade tillägg visas om parametern Name inte har angetts</span><span class="sxs-lookup"><span data-stu-id="a52f3-2416">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="a52f3-2417">Parametrarna Tag och ResourceId har lagts till i cmdleten Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="a52f3-2417">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="a52f3-2418">Get-AzVmssVM utan instans-ID och med InstanceView kan visa virtuella VMSS-datorer med instansvyn.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2418">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a52f3-2419">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a52f3-2419">Az.DataLakeStore</span></span>
* <span data-ttu-id="a52f3-2420">Cmdletar har lagts till för uppräkning och återställning av borttagna objekt i ADL</span><span class="sxs-lookup"><span data-stu-id="a52f3-2420">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="a52f3-2421">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a52f3-2421">Az.EventHub</span></span>
* <span data-ttu-id="a52f3-2422">Ny boolesk egenskap SkipEmptyArchives har lagts till i Skip Empty Archives i CaptureDescription-klassen i Eventhub</span><span class="sxs-lookup"><span data-stu-id="a52f3-2422">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a52f3-2423">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a52f3-2423">Az.KeyVault</span></span>
* <span data-ttu-id="a52f3-2424">Taggning i Set-AzKeyVaultSecret har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="a52f3-2424">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="a52f3-2425">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="a52f3-2425">Az.LogicApp</span></span>
* <span data-ttu-id="a52f3-2426">Grundläggande SKU har lagts till för Integrationskonton</span><span class="sxs-lookup"><span data-stu-id="a52f3-2426">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="a52f3-2427">XSLT 2.0, XSLT 3.0 och Flytande mappningstyper har lagts till</span><span class="sxs-lookup"><span data-stu-id="a52f3-2427">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="a52f3-2428">Nya cmdletar för integrationskontosammansättningar</span><span class="sxs-lookup"><span data-stu-id="a52f3-2428">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="a52f3-2429">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="a52f3-2429">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="a52f3-2430">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="a52f3-2430">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="a52f3-2431">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="a52f3-2431">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="a52f3-2432">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="a52f3-2432">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="a52f3-2433">Nya cmdletar för batchkonfiguration för integrationskonto</span><span class="sxs-lookup"><span data-stu-id="a52f3-2433">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="a52f3-2434">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="a52f3-2434">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="a52f3-2435">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="a52f3-2435">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="a52f3-2436">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="a52f3-2436">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="a52f3-2437">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="a52f3-2437">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="a52f3-2438">Logic App-SDK har uppdaterats till version 4.1.0</span><span class="sxs-lookup"><span data-stu-id="a52f3-2438">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a52f3-2439">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a52f3-2439">Az.Monitor</span></span>
* <span data-ttu-id="a52f3-2440">Hjälpen för Get-AzMetric har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="a52f3-2440">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a52f3-2441">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a52f3-2441">Az.Network</span></span>
* <span data-ttu-id="a52f3-2442">Hjälpexempel för Add-AzApplicationGatewayCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="a52f3-2442">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="a52f3-2443">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a52f3-2443">Az.OperationalInsights</span></span>
* <span data-ttu-id="a52f3-2444">Ytterligare stöd för datakällorna New och Get ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2444">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="a52f3-2445">Ny ApplicationInsights-typ har lagts till för att ge stöd för ”Get specific” och ”Get all” för ApplicationInsights-datakällor för angiven arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2445">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="a52f3-2446">Cmdleten New-AzOperationalInsightsApplicationInsightsDataSource har lagts till för att skapa datakälla med angivna parametrar för Application Insights-resurs: subscription Id, resourceGroupName och name.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2446">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a52f3-2447">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a52f3-2447">Az.Resources</span></span>
* <span data-ttu-id="a52f3-2448">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="a52f3-2448">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="a52f3-2449">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="a52f3-2449">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="a52f3-2450">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="a52f3-2450">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="a52f3-2451">Fel som gör att KeyCredentials inte kan skapas upprepade gånger har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="a52f3-2451">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="a52f3-2452">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a52f3-2452">Az.Sql</span></span>
* <span data-ttu-id="a52f3-2453">Lägg till stöd för hyperskalanivån för SQL DB</span><span class="sxs-lookup"><span data-stu-id="a52f3-2453">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="a52f3-2454">Ett fel har åtgärdats där återställningen kunde misslyckas på grund av onödiga inställningsegenskaper i restore-förfrågan</span><span class="sxs-lookup"><span data-stu-id="a52f3-2454">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a52f3-2455">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a52f3-2455">Az.Websites</span></span>
* <span data-ttu-id="a52f3-2456">Rätt exempel i Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="a52f3-2456">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="a52f3-2457">1.3.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="a52f3-2457">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a52f3-2458">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a52f3-2458">Az.Accounts</span></span>
* <span data-ttu-id="a52f3-2459">Uppdatera till den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="a52f3-2459">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="a52f3-2460">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a52f3-2460">Az.AnalysisServices</span></span>
<span data-ttu-id="a52f3-2461">Allmän tillgänglighet för Az.AnalysisServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2461">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a52f3-2462">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a52f3-2462">Az.Compute</span></span>
* <span data-ttu-id="a52f3-2463">AEM-tillägg: Lägg till stöd för UltraSSD-, P60-, P70- och P80-diskar</span><span class="sxs-lookup"><span data-stu-id="a52f3-2463">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="a52f3-2464">Uppdatera hjälpbeskrivning för Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="a52f3-2464">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="a52f3-2465">Uppdatera hjälpbeskrivning och exempel för Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="a52f3-2465">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a52f3-2466">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a52f3-2466">Az.RecoveryServices</span></span>
<span data-ttu-id="a52f3-2467">Allmän tillgänglighet för Az.RecoveryServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2467">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a52f3-2468">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a52f3-2468">Az.Resources</span></span>
* <span data-ttu-id="a52f3-2469">Korrigera taggar för resursgrupper</span><span class="sxs-lookup"><span data-stu-id="a52f3-2469">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="a52f3-2470">Mer information här: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="a52f3-2470">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="a52f3-2471">Åtgärda problem där `Get-AzureRmRoleAssignment` inte respekterar -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="a52f3-2471">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="a52f3-2472">Mer information här: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="a52f3-2472">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="a52f3-2473">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a52f3-2473">Az.Sql</span></span>
* <span data-ttu-id="a52f3-2474">Lägga till Get/Set-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="a52f3-2474">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="a52f3-2475">Åtgärda problem där ett nullref-undantag uppstår när du kör SQL-cmdletar och inte är inloggad på ett Azure-konto</span><span class="sxs-lookup"><span data-stu-id="a52f3-2475">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="a52f3-2476">Åtgärda nullref-undantag i Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="a52f3-2476">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="a52f3-2477">1.2.1 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="a52f3-2477">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a52f3-2478">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a52f3-2478">Az.Accounts</span></span>
* <span data-ttu-id="a52f3-2479">Version med rätt version av autentisering</span><span class="sxs-lookup"><span data-stu-id="a52f3-2479">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="a52f3-2480">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a52f3-2480">Az.AnalysisServices</span></span>
* <span data-ttu-id="a52f3-2481">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="a52f3-2481">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a52f3-2482">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a52f3-2482">Az.RecoveryServices</span></span>
* <span data-ttu-id="a52f3-2483">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="a52f3-2483">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="a52f3-2484">1.2.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="a52f3-2484">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a52f3-2485">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a52f3-2485">Az.Accounts</span></span>
* <span data-ttu-id="a52f3-2486">Lägga till interaktiv autentisering och autentisering med användarnamn/lösenord för endast Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="a52f3-2486">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="a52f3-2487">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="a52f3-2487">Update incorrect online help URLs</span></span>
* <span data-ttu-id="a52f3-2488">Lägga till varningsmeddelande i PS Core för Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="a52f3-2488">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="a52f3-2489">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="a52f3-2489">Az.Aks</span></span>
* <span data-ttu-id="a52f3-2490">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="a52f3-2490">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a52f3-2491">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a52f3-2491">Az.Automation</span></span>
* <span data-ttu-id="a52f3-2492">Stöd för Python 2-runbookflöden har lagts till</span><span class="sxs-lookup"><span data-stu-id="a52f3-2492">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="a52f3-2493">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="a52f3-2493">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="a52f3-2494">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="a52f3-2494">Az.Cdn</span></span>
* <span data-ttu-id="a52f3-2495">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="a52f3-2495">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a52f3-2496">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a52f3-2496">Az.Compute</span></span>
* <span data-ttu-id="a52f3-2497">Lägga till cmdleten Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="a52f3-2497">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="a52f3-2498">Lägga till TempDisk-parameter i Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a52f3-2498">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="a52f3-2499">Korrigera varningsmeddelande för New-AzVM</span><span class="sxs-lookup"><span data-stu-id="a52f3-2499">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="a52f3-2500">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a52f3-2500">Az.ContainerRegistry</span></span>
* <span data-ttu-id="a52f3-2501">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="a52f3-2501">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a52f3-2502">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a52f3-2502">Az.DataFactory</span></span>
* <span data-ttu-id="a52f3-2503">ADF .Net SDK-versionen har uppdaterats till 3.0.0</span><span class="sxs-lookup"><span data-stu-id="a52f3-2503">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a52f3-2504">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a52f3-2504">Az.DataLakeStore</span></span>
* <span data-ttu-id="a52f3-2505">Åtgärda problem med ADLS-slutpunkt vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="a52f3-2505">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="a52f3-2506">Mer information här: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="a52f3-2506">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="a52f3-2507">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="a52f3-2507">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a52f3-2508">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a52f3-2508">Az.IotHub</span></span>
* <span data-ttu-id="a52f3-2509">Lägga till kodningsformat i cmdleten Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2509">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a52f3-2510">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a52f3-2510">Az.KeyVault</span></span>
* <span data-ttu-id="a52f3-2511">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="a52f3-2511">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a52f3-2512">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a52f3-2512">Az.Network</span></span>
* <span data-ttu-id="a52f3-2513">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="a52f3-2513">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="a52f3-2514">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a52f3-2514">Az.Resources</span></span>
* <span data-ttu-id="a52f3-2515">Åtgärda felaktiga exempel i referensdokumentationen ”New-AzADAppCredential” och ”New-AzADSpCredential”</span><span class="sxs-lookup"><span data-stu-id="a52f3-2515">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="a52f3-2516">Åtgärda problem där sökvägen för parametern ”-TemplateFile” inte omvandlas innan cmdletarna för distribution i resursgruppen körs</span><span class="sxs-lookup"><span data-stu-id="a52f3-2516">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="a52f3-2517">Az.Resources: Korrigera dokumentationen om standardvärdet för New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="a52f3-2517">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="a52f3-2518">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="a52f3-2518">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="a52f3-2519">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="a52f3-2519">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="a52f3-2520">Åtgärda formateringsproblemet med objektet ”PSResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="a52f3-2520">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="a52f3-2521">Mer information här: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="a52f3-2521">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a52f3-2522">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a52f3-2522">Az.ServiceFabric</span></span>
* <span data-ttu-id="a52f3-2523">Återställ när ett certifikat läggs till i en Virtual Machine Scale Sets-modell men ett undantag genereras. Detta har gjorts för att åtgärda följande fel: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="a52f3-2523">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="a52f3-2524">Korrigera några felmeddelanden.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2524">Fix some error messages.</span></span>
* <span data-ttu-id="a52f3-2525">Korrigering av skapande av kluster med ARM-mall som är standard för New-AzServiceFabriCluster som inte fungerade med migrering till Az.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2525">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="a52f3-2526">Korrigering av tilläggning av kluster/programcertifikat så att endast VM Scale Sets som motsvarar klustret läggs till genom att kontrollera ID för klustret i tillägget.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2526">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="a52f3-2527">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="a52f3-2527">Az.SignalR</span></span>
* <span data-ttu-id="a52f3-2528">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="a52f3-2528">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="a52f3-2529">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a52f3-2529">Az.Sql</span></span>
* <span data-ttu-id="a52f3-2530">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="a52f3-2530">Update incorrect online help URLs</span></span>
* <span data-ttu-id="a52f3-2531">Uppdaterad parameterbeskrivning för LicenseType-parameter med möjliga värden</span><span class="sxs-lookup"><span data-stu-id="a52f3-2531">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="a52f3-2532">Korrigering för att uppdatera hanterad instansidentitet som inte fungerar när det är den enda uppdaterade egenskapen</span><span class="sxs-lookup"><span data-stu-id="a52f3-2532">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="a52f3-2533">Stöd för anpassad sortering på hanterad instans</span><span class="sxs-lookup"><span data-stu-id="a52f3-2533">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a52f3-2534">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a52f3-2534">Az.Storage</span></span>
* <span data-ttu-id="a52f3-2535">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="a52f3-2535">Update incorrect online help URLs</span></span>
* <span data-ttu-id="a52f3-2536">Tillhandahåll detaljerat felmeddelande när en användare försöker hämta/konfigurera klassisk loggning/mått på ett Premium Storage-konto eftersom Premium Storage-kontot inte har stöd för klassisk loggning/mått.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2536">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="a52f3-2537">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="a52f3-2537">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="a52f3-2538">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="a52f3-2538">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="a52f3-2539">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="a52f3-2539">Az.TrafficManager</span></span>
* <span data-ttu-id="a52f3-2540">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="a52f3-2540">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a52f3-2541">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a52f3-2541">Az.Websites</span></span>
* <span data-ttu-id="a52f3-2542">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="a52f3-2542">Update incorrect online help URLs</span></span>
* <span data-ttu-id="a52f3-2543">Korrigerar ”New-AzWebAppSSLBinding” så att certifikatet laddas upp till rätt resursgrupp och plats om appen finns i en ASE.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2543">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="a52f3-2544">Korrigerar ”New-AzWebAppSSLBinding” så att taggarna inte skrivs över på en bindning av ett SSL-certifikat till en app</span><span class="sxs-lookup"><span data-stu-id="a52f3-2544">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="a52f3-2545">1.1.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="a52f3-2545">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a52f3-2546">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a52f3-2546">Az.Accounts</span></span>
* <span data-ttu-id="a52f3-2547">Lade till omfattningen ”Lokal” till Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="a52f3-2547">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a52f3-2548">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a52f3-2548">Az.Compute</span></span>
* <span data-ttu-id="a52f3-2549">Namn är nu valfritt i ID-parametern för Restart/Start/Stop/Remove/Set-AzVM och Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="a52f3-2549">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="a52f3-2550">Uppdaterade beskrivningen av ID i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="a52f3-2550">Updated the description of ID in help files</span></span>
* <span data-ttu-id="a52f3-2551">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a52f3-2551">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a52f3-2552">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a52f3-2552">Az.DataLakeStore</span></span>
* <span data-ttu-id="a52f3-2553">Uppdatera sdk-versionen av dataplanet till 1.1.14 för SDK-korrigeringar.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2553">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="a52f3-2554">Korrigerade hanteringen av negativ accesstime och modificationtime för getfilestatus och liststatus; korrigera asynkront annulleringstoken</span><span class="sxs-lookup"><span data-stu-id="a52f3-2554">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="a52f3-2555">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="a52f3-2555">Az.EventGrid</span></span>
* <span data-ttu-id="a52f3-2556">Uppdaterat för användning av API-versionen 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2556">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="a52f3-2557">Uppdaterade följande cmdletar för att stödja nytt scenario i API-versionen 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="a52f3-2557">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="a52f3-2558">New-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="a52f3-2558">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="a52f3-2559">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="a52f3-2559">Event Time-To-Live,</span></span>
        - <span data-ttu-id="a52f3-2560">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="a52f3-2560">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="a52f3-2561">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2561">Dead letter endpoint.</span></span>
    - <span data-ttu-id="a52f3-2562">Update-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="a52f3-2562">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="a52f3-2563">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="a52f3-2563">Event Time-To-Live,</span></span>
        - <span data-ttu-id="a52f3-2564">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="a52f3-2564">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="a52f3-2565">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2565">Dead letter endpoint.</span></span>
* <span data-ttu-id="a52f3-2566">Lade till nya enum-värden (storageQueue och hybridConnection) för alternativet EndpointType i cmdletarna New-AzureRmEventGridSubscription och Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2566">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="a52f3-2567">Visa varningsmeddelanden om skapande eller uppdatering av händelseprenumerationen förväntas medföra manuell åtgärd från användaren.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2567">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a52f3-2568">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a52f3-2568">Az.IotHub</span></span>
* <span data-ttu-id="a52f3-2569">Har uppdaterats till den senaste versionen av SDK:n lotHub</span><span class="sxs-lookup"><span data-stu-id="a52f3-2569">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="a52f3-2570">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="a52f3-2570">Az.LogicApp</span></span>
* <span data-ttu-id="a52f3-2571">Get-AzLogicApp visar en lista över alla som inte har angivet namn</span><span class="sxs-lookup"><span data-stu-id="a52f3-2571">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="a52f3-2572">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a52f3-2572">Az.Resources</span></span>
* <span data-ttu-id="a52f3-2573">Åtgärdade problem med parameteruppsättningen när parametrarna -ODataQuery och -ResourceId anges för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="a52f3-2573">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="a52f3-2574">Mer information här: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="a52f3-2574">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="a52f3-2575">Åtgärdade hantering av parametern -Custom i New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a52f3-2575">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="a52f3-2576">Korrigerade stavfel i New-AzDeployment-dokumentationen</span><span class="sxs-lookup"><span data-stu-id="a52f3-2576">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="a52f3-2577">Gjorde parametern -MailNickname obligatorisk för New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="a52f3-2577">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="a52f3-2578">Mer information här: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="a52f3-2578">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="a52f3-2579">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="a52f3-2579">Az.SignalR</span></span>
* <span data-ttu-id="a52f3-2580">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a52f3-2580">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="a52f3-2581">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a52f3-2581">Az.Sql</span></span>
* <span data-ttu-id="a52f3-2582">Konverterade lagringshanteringsklientens beroende av den normala SDK-implementeringen.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2582">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a52f3-2583">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a52f3-2583">Az.Storage</span></span>
* <span data-ttu-id="a52f3-2584">Angav StorageAccountName för lagringskontext som det verkliga namnet på lagringskontot när det skapas med Sas Token, OAuth eller Anonymous</span><span class="sxs-lookup"><span data-stu-id="a52f3-2584">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="a52f3-2585">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="a52f3-2585">New-AzStorageContext</span></span>
* <span data-ttu-id="a52f3-2586">Skapade Sas Token för Blob Snapshot-objekt med parametern -FullUri, åtgärdade den returnerade URI:n så att den blir URI för ögonblicksbild</span><span class="sxs-lookup"><span data-stu-id="a52f3-2586">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="a52f3-2587">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="a52f3-2587">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a52f3-2588">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a52f3-2588">Az.Websites</span></span>
* <span data-ttu-id="a52f3-2589">Åtgärdade en bugg i datumparsningen i Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="a52f3-2589">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="a52f3-2590">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a52f3-2590">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="a52f3-2591">1.0.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="a52f3-2591">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="a52f3-2592">Allmänt</span><span class="sxs-lookup"><span data-stu-id="a52f3-2592">General</span></span>

- <span data-ttu-id="a52f3-2593">Allmän tillgänglighet för Az-modulen</span><span class="sxs-lookup"><span data-stu-id="a52f3-2593">General Availability of Az Module</span></span>
- <span data-ttu-id="a52f3-2594">Onlinehjälp för varje modul</span><span class="sxs-lookup"><span data-stu-id="a52f3-2594">Online help for each module</span></span>
- <span data-ttu-id="a52f3-2595">Mer information och en översikt finns på [Az-informationssidan](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="a52f3-2595">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="a52f3-2596">Information om hur du migrerar från AzureRM finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a52f3-2596">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="a52f3-2597">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a52f3-2597">Az.Accounts</span></span>
- <span data-ttu-id="a52f3-2598">Har ändrats från Az.Profile</span><span class="sxs-lookup"><span data-stu-id="a52f3-2598">Changed from Az.Profile</span></span>
- <span data-ttu-id="a52f3-2599">Fasta tabellformat för profil- och kontexttyper</span><span class="sxs-lookup"><span data-stu-id="a52f3-2599">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="a52f3-2600">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a52f3-2600">Az.ApiManagement</span></span>
- <span data-ttu-id="a52f3-2601">Korrigeringar för #7002</span><span class="sxs-lookup"><span data-stu-id="a52f3-2601">Fixes for #7002</span></span>
- <span data-ttu-id="a52f3-2602">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a52f3-2602">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="a52f3-2603">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="a52f3-2603">Az.Batch</span></span>
- <span data-ttu-id="a52f3-2604">Lade till möjligheten att se vilken version av Azure Batch Node Agent som körs på var och en av de virtuella datorerna i en pool, via den nya egenskapen `NodeAgentInformation` på `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2604">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="a52f3-2605">Standarden `Caching` för `PSDataDisk` är nu `ReadWrite` i stället för `None`.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2605">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="a52f3-2606">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a52f3-2606">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="a52f3-2607">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="a52f3-2607">Az.Billing</span></span>
- <span data-ttu-id="a52f3-2608">Kombinerar cmdletarna för fakturering, förbrukning och UsageAggregates. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a52f3-2608">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="a52f3-2609">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="a52f3-2609">Az.CognitivServices</span></span>
- <span data-ttu-id="a52f3-2610">Lade till kompletterare för SkuName och Typem som är tillgängliga i New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="a52f3-2610">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="a52f3-2611">Tog bort parameteruppsättningen GetSkusWithAccountParamSetName från Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="a52f3-2611">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="a52f3-2612">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="a52f3-2612">Az.ContainerInstance</span></span>
- <span data-ttu-id="a52f3-2613">Stöd för ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="a52f3-2613">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="a52f3-2614">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="a52f3-2614">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="a52f3-2615">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a52f3-2615">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="a52f3-2616">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a52f3-2616">Az.DataLakeStore</span></span>
- <span data-ttu-id="a52f3-2617">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a52f3-2617">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="a52f3-2618">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a52f3-2618">Az.Monitor</span></span>
- <span data-ttu-id="a52f3-2619">Döpte om Az.Insights till Az.Monitor och andra mindre icke-bakåtkompatibla ändringar. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a52f3-2619">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="a52f3-2620">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a52f3-2620">Az.KeyVault</span></span>
- <span data-ttu-id="a52f3-2621">Tog bort den inaktuella egenskapen PurgeDisabled från utdatatyper</span><span class="sxs-lookup"><span data-stu-id="a52f3-2621">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="a52f3-2622">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="a52f3-2622">Az.MachineLearning</span></span>
- <span data-ttu-id="a52f3-2623">Inkluderade cmdletarna från modulen Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="a52f3-2623">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="a52f3-2624">Az.Media</span><span class="sxs-lookup"><span data-stu-id="a52f3-2624">Az.Media</span></span>
- <span data-ttu-id="a52f3-2625">Tog bort inaktuella -Tags-alias från New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="a52f3-2625">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="a52f3-2626">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a52f3-2626">Az.Network</span></span>
<span data-ttu-id="a52f3-2627">Stöd har lagts till för konfiguration av RewriteRuleSets i Application Gateway</span><span class="sxs-lookup"><span data-stu-id="a52f3-2627">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="a52f3-2628">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="a52f3-2628">New cmdlets added:</span></span>
        - <span data-ttu-id="a52f3-2629">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a52f3-2629">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="a52f3-2630">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a52f3-2630">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="a52f3-2631">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a52f3-2631">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="a52f3-2632">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a52f3-2632">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="a52f3-2633">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a52f3-2633">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="a52f3-2634">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="a52f3-2634">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="a52f3-2635">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="a52f3-2635">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="a52f3-2636">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="a52f3-2636">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="a52f3-2637">Cmdletar har uppdaterats med den valfria parametern -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a52f3-2637">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="a52f3-2638">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a52f3-2638">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="a52f3-2639">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="a52f3-2639">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="a52f3-2640">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="a52f3-2640">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="a52f3-2641">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a52f3-2641">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="a52f3-2642">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="a52f3-2642">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="a52f3-2643">New-AzureRmApplicationGatewayUrlPathMapConfig har lagt till KeyVault-stöd för Application Gateway med Identity.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2643">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="a52f3-2644">Cmdletar har uppdaterats med den valfria parametern -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="a52f3-2644">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="a52f3-2645">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="a52f3-2645">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="a52f3-2646">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="a52f3-2646">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="a52f3-2647">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="a52f3-2647">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="a52f3-2648">Cmdleten New-AzApplicationGateway har uppdaterats med den valfria parametern -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="a52f3-2648">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="a52f3-2649">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a52f3-2649">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="a52f3-2650">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a52f3-2650">Az.OperationalInsights</span></span>
- <span data-ttu-id="a52f3-2651">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a52f3-2651">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="a52f3-2652">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="a52f3-2652">Az.Profile</span></span>
- <span data-ttu-id="a52f3-2653">Modulnamnet har ändrats till Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a52f3-2653">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="a52f3-2654">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a52f3-2654">Az.RecoveryServices</span></span>
- <span data-ttu-id="a52f3-2655">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a52f3-2655">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="a52f3-2656">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a52f3-2656">Az.Resources</span></span>
- <span data-ttu-id="a52f3-2657">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a52f3-2657">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="a52f3-2658">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a52f3-2658">Az.ServiceFabric</span></span>
- <span data-ttu-id="a52f3-2659">Stöd för specificering av certifikat efter eget namn och tumavtryck</span><span class="sxs-lookup"><span data-stu-id="a52f3-2659">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="a52f3-2660">Information om fler icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a52f3-2660">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="a52f3-2661">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="a52f3-2661">Az.SIgnalR</span></span>
- <span data-ttu-id="a52f3-2662">Allmän tillgänglighet för PowerShell-cmdletar för SIgnalR</span><span class="sxs-lookup"><span data-stu-id="a52f3-2662">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="a52f3-2663">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a52f3-2663">Az.Sql</span></span>
- <span data-ttu-id="a52f3-2664">Lade till de nya identifieringstyperna Data_Exfiltration och Unsafe_Action i Threat Detection-cmdletar</span><span class="sxs-lookup"><span data-stu-id="a52f3-2664">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="a52f3-2665">Uppdaterade dokumentationsexempel för Sql Auditing-cmdletar</span><span class="sxs-lookup"><span data-stu-id="a52f3-2665">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="a52f3-2666">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a52f3-2666">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="a52f3-2667">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a52f3-2667">Az.Storage</span></span>
- <span data-ttu-id="a52f3-2668">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a52f3-2668">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="a52f3-2669">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a52f3-2669">Az.Websites</span></span>
- <span data-ttu-id="a52f3-2670">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a52f3-2670">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="a52f3-2671">0.7.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="a52f3-2671">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="a52f3-2672">Allmänt</span><span class="sxs-lookup"><span data-stu-id="a52f3-2672">General</span></span>

* <span data-ttu-id="a52f3-2673">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="a52f3-2673">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="a52f3-2674">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a52f3-2674">Az.Compute</span></span>

* <span data-ttu-id="a52f3-2675">Lade till stöd för UltraSSD och Galleriavbildningar i de enkla parameteruppsättningarna för `New-AzVm(ss)`-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2675">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="a52f3-2676">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a52f3-2676">Az.DataLakeStore</span></span>

* <span data-ttu-id="a52f3-2677">Åtgärdade avslutande snedstreck i domänen för adls-konto</span><span class="sxs-lookup"><span data-stu-id="a52f3-2677">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="a52f3-2678">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="a52f3-2678">Az.FrontDoor</span></span>

* <span data-ttu-id="a52f3-2679">Brutna länkar korrigerades</span><span class="sxs-lookup"><span data-stu-id="a52f3-2679">Fixed some broken links</span></span>
    - <span data-ttu-id="a52f3-2680">I artiklarna New-AzureRmFrontDoor och Set-AzureRmFrontDoor artiklar korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2680">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="a52f3-2681">I artikeln New-AzureRmFrontDoorManagedRuleObject korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2681">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="a52f3-2682">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a52f3-2682">Az.RecoveryServices</span></span>

* <span data-ttu-id="a52f3-2683">Lade till valideringar på klientsidan för Azure-filresurs med återställningsåtgärder.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2683">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="a52f3-2684">Gjorde storageAccountName och storageAccountResourceGroupName valfritt för afs-återställning.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2684">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="a52f3-2685">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a52f3-2685">Az.Resources</span></span>

* <span data-ttu-id="a52f3-2686">Korrigering för https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="a52f3-2686">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="a52f3-2687">Uppdaterade Get-AzureRmRoleAssignment så att prenumerationsomfattningen används om den anges vid begäran om klassiska administratörer.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2687">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="a52f3-2688">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a52f3-2688">Az.Sql</span></span>

* <span data-ttu-id="a52f3-2689">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="a52f3-2689">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="a52f3-2690">Korrigerade ett problem med Get-AzureRmSqlDatabaseVulnerabilityAssessment med DotNet-kärna</span><span class="sxs-lookup"><span data-stu-id="a52f3-2690">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="a52f3-2691">Ändrade dokumentationen för hjälpmeddelanden som rör SQL Auditing-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2691">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="a52f3-2692">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a52f3-2692">Az.Storage</span></span>

* <span data-ttu-id="a52f3-2693">Lade till -EnableHierarchicalNamespace i New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a52f3-2693">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="a52f3-2694">Åtgärdade problemet med att cmdleten Copy File inte kunde återanvända källkontexten på målet om inte -DestContext angetts</span><span class="sxs-lookup"><span data-stu-id="a52f3-2694">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="a52f3-2695">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="a52f3-2695">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="a52f3-2696">Stöd för statisk webbplatskonfiguration</span><span class="sxs-lookup"><span data-stu-id="a52f3-2696">Support Static Website configuration</span></span>
    - <span data-ttu-id="a52f3-2697">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="a52f3-2697">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="a52f3-2698">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="a52f3-2698">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="a52f3-2699">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a52f3-2699">Az.Websites</span></span>

* <span data-ttu-id="a52f3-2700">Set-AzureRmWebApp och Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a52f3-2700">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="a52f3-2701">Ny parameter (-AzureStoragePath) har lagts till för att ange att Azure Storage-sökvägar ska monteras i containerappar i Windows och Linux.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2701">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="a52f3-2702">Använder utdata från den nya cmdleten New-AzureRmWebAppAzureStoragePath som en parameter för att ange sökvägar för Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2702">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="a52f3-2703">0.6.1 – november 2018</span><span class="sxs-lookup"><span data-stu-id="a52f3-2703">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="a52f3-2704">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a52f3-2704">Az.ApiManagement</span></span>
* <span data-ttu-id="a52f3-2705">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="a52f3-2705">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="a52f3-2706">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a52f3-2706">Az.Automation</span></span>
* <span data-ttu-id="a52f3-2707">Swagger baserade Azure Automation-cmdletar</span><span class="sxs-lookup"><span data-stu-id="a52f3-2707">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="a52f3-2708">Cmdletar för Uppdateringshantering har lagts till</span><span class="sxs-lookup"><span data-stu-id="a52f3-2708">Added Update Management cmdlets</span></span>
* <span data-ttu-id="a52f3-2709">Cmdletar för källkontroll har lagts till</span><span class="sxs-lookup"><span data-stu-id="a52f3-2709">Added Source Control cmdlets</span></span>
* <span data-ttu-id="a52f3-2710">Remove-AzureRmAutomationHybridWorkerGroup-cmdlet har lagts till</span><span class="sxs-lookup"><span data-stu-id="a52f3-2710">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="a52f3-2711">Kommandot för DSC-registreringsnod har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="a52f3-2711">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="a52f3-2712">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a52f3-2712">Az.Compute</span></span>
* <span data-ttu-id="a52f3-2713">Problem med SystemAssigned-identitet har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="a52f3-2713">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="a52f3-2714">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="a52f3-2714">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="a52f3-2715">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="a52f3-2715">Az.ContainerInstance</span></span>
* <span data-ttu-id="a52f3-2716">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="a52f3-2716">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="a52f3-2717">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="a52f3-2717">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="a52f3-2718">uppdatera exempelbeskrivningen för marketplace-cmdletar</span><span class="sxs-lookup"><span data-stu-id="a52f3-2718">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="a52f3-2719">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a52f3-2719">Az.Network</span></span>
* <span data-ttu-id="a52f3-2720">Cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomErreller Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="a52f3-2720">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="a52f3-2721">ICMP tillbaka till stöd för Azure Firewall-nätverksprotokoll har lagts till</span><span class="sxs-lookup"><span data-stu-id="a52f3-2721">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="a52f3-2722">Uppdatera cmdlet Test-AzureRmNetworkWatcherConnectivity, lägga till verifiering av mål-id, adress och port.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2722">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="a52f3-2723">Åtgärda problem med minnesanvändning i VirtualNetwork-karta</span><span class="sxs-lookup"><span data-stu-id="a52f3-2723">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="a52f3-2724">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="a52f3-2724">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="a52f3-2725">Åtgärda för att ändra principen för en skyddad fildelning.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2725">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="a52f3-2726">Tidszonsprincipen har konverterats till versaler.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2726">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="a52f3-2727">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="a52f3-2727">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="a52f3-2728">Exempel i New-AzureRmRecoveryServicesAsrProtectableItem har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="a52f3-2728">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="a52f3-2729">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="a52f3-2729">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="a52f3-2730">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="a52f3-2730">Az.Relay</span></span>
* <span data-ttu-id="a52f3-2731">Valfri parameter -KeyValue till New-AzureRmRelayKey cmdlet har lagts till, vilket gör det möjligt för användare att tillhandahålla KeyValue.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2731">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="a52f3-2732">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a52f3-2732">Az.Resources</span></span>
* <span data-ttu-id="a52f3-2733">Uppdatera hjälpdokumentation för resursidentitet kopplad till parametrar i `New-AzureRmPolicyAssignment` och `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="a52f3-2733">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="a52f3-2734">Lägg till ett exempel för New-AzureRmPolicyDefinition som använder -Metadata</span><span class="sxs-lookup"><span data-stu-id="a52f3-2734">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="a52f3-2735">Korrigera så att skiftläge behålls i taggnycklar i NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="a52f3-2735">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="a52f3-2736">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a52f3-2736">Az.ServiceFabric</span></span>
* <span data-ttu-id="a52f3-2737">Lägg till utfasningsmeddelanden för kommande icke-kompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="a52f3-2737">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="a52f3-2738">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a52f3-2738">Az.Sql</span></span>
* <span data-ttu-id="a52f3-2739">Nya cmdletar för CRUD-åtgärder på Azure Sql Database-hanterad instans och Azure Sql-hanterad databas</span><span class="sxs-lookup"><span data-stu-id="a52f3-2739">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="a52f3-2740">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="a52f3-2740">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="a52f3-2741">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="a52f3-2741">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="a52f3-2742">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="a52f3-2742">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="a52f3-2743">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="a52f3-2743">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="a52f3-2744">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="a52f3-2744">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="a52f3-2745">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="a52f3-2745">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="a52f3-2746">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="a52f3-2746">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="a52f3-2747">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="a52f3-2747">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="a52f3-2748">Hantering av utökad granskningsprincip på en server eller en databas har aktiverats.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2748">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="a52f3-2749">Ny parameter (PredicateExpression) har lagts till för att aktivera filtrering av granskningsloggar.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2749">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="a52f3-2750">Cmdletar har ändrats så att de använder SQL-klienter i stället för äldre klienter.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2750">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="a52f3-2751">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2751">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="a52f3-2752">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2752">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="a52f3-2753">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2753">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="a52f3-2754">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2754">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="a52f3-2755">Problem med att använda Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings med lagringskontots namnparameter har korrigerats</span><span class="sxs-lookup"><span data-stu-id="a52f3-2755">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="a52f3-2756">0.5.0 – november 2018</span><span class="sxs-lookup"><span data-stu-id="a52f3-2756">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="a52f3-2757">Allmänt</span><span class="sxs-lookup"><span data-stu-id="a52f3-2757">General</span></span>
* <span data-ttu-id="a52f3-2758">Lade till resurskompletterare till många kärn-cmdletar – dessa gör att du kan stega genom befintliga resursnamn med TABB vid interaktiva anrop till cmdletar</span><span class="sxs-lookup"><span data-stu-id="a52f3-2758">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="a52f3-2759">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="a52f3-2759">Az.Profile</span></span>
* <span data-ttu-id="a52f3-2760">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="a52f3-2760">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="a52f3-2761">Bytte namn på parametern TenantId i cmdleten Connect-AzAccount till Tenant och lade till ett alias för TenantId</span><span class="sxs-lookup"><span data-stu-id="a52f3-2761">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="a52f3-2762">Uppdaterade TenantId-beskrivningen för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="a52f3-2762">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="a52f3-2763">Åtgärda felmeddelande för misslyckad inloggning när du tillhandahåller klientdomän</span><span class="sxs-lookup"><span data-stu-id="a52f3-2763">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="a52f3-2764">Åtgärda problem med att kontextnamn hamnar i konflikt för konton utan prenumerationer i klientorganisationen</span><span class="sxs-lookup"><span data-stu-id="a52f3-2764">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="a52f3-2765">Åtgärda problem med DataLake-slutpunkter vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="a52f3-2765">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="a52f3-2766">Åtgärdade problem med att Disconnect-AzAccount kastades om den inte anslöts</span><span class="sxs-lookup"><span data-stu-id="a52f3-2766">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="a52f3-2767">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a52f3-2767">Az.CognitiveServices</span></span>
* <span data-ttu-id="a52f3-2768">Lade till åtgärden Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2768">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a52f3-2769">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a52f3-2769">Az.Compute</span></span>
* <span data-ttu-id="a52f3-2770">Lade till cmdletarna Add-AzVmssVMDataDisk och Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="a52f3-2770">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="a52f3-2771">Get-AzVMImage visar AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="a52f3-2771">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="a52f3-2772">Åtgärdade att värdena för alternativen SetAzVMChefExtension -BootstrapOptions och -JsonAttribute inte angavs i json-format.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2772">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a52f3-2773">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a52f3-2773">Az.DataLakeStore</span></span>
* <span data-ttu-id="a52f3-2774">Uppdatera DataLake-paketet till 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2774">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="a52f3-2775">Lägg till standardsamtidighet för flertrådade åtgärder.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2775">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="a52f3-2776">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="a52f3-2776">Az.Insights</span></span>
* <span data-ttu-id="a52f3-2777">Åtgärdade problem #7267 (autoskalningsområde)</span><span class="sxs-lookup"><span data-stu-id="a52f3-2777">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="a52f3-2778">Problem med att uppräknade parametrar inte ställdes in ordentligt när du skapade en ny autoskalningsregel (de ställdes alltid in med standardvärdet).</span><span class="sxs-lookup"><span data-stu-id="a52f3-2778">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="a52f3-2779">Åtgärdade problem #7513 [Insights] Set-AzDiagnosticSetting kräver uttrycklig specifikation av kategorier när inställningar skapas</span><span class="sxs-lookup"><span data-stu-id="a52f3-2779">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="a52f3-2780">Nu kräver inte cmdleten uttrycklig anvisning av kategorierna för att aktiveras under skapande, d.v.s. den fungerar enligt beskrivning</span><span class="sxs-lookup"><span data-stu-id="a52f3-2780">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a52f3-2781">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a52f3-2781">Az.Network</span></span>
* <span data-ttu-id="a52f3-2782">PeeringType ändrades till en obligatorisk parameter för följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="a52f3-2782">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="a52f3-2783">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="a52f3-2783">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="a52f3-2784">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="a52f3-2784">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="a52f3-2785">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="a52f3-2785">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="a52f3-2786">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="a52f3-2786">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="a52f3-2787">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="a52f3-2787">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="a52f3-2788">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="a52f3-2788">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="a52f3-2789">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a52f3-2789">Az.PolicyInsights</span></span>
* <span data-ttu-id="a52f3-2790">Cmdletar för principreparation har lagts till</span><span class="sxs-lookup"><span data-stu-id="a52f3-2790">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="a52f3-2791">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a52f3-2791">Az.Resources</span></span>
* <span data-ttu-id="a52f3-2792">Korrigering för https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="a52f3-2792">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="a52f3-2793">Tillåt att resurser listas med parametern -ResourceId för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="a52f3-2793">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="a52f3-2794">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a52f3-2794">Az.ServiceBus</span></span>
* <span data-ttu-id="a52f3-2795">Skrivskyddad MigrationState-egenskap har lagts till i PSServiceBusMigrationConfigurationAttributes, som hjälper till att hålla koll på migreringstillståndet.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2795">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a52f3-2796">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a52f3-2796">Az.ServiceFabric</span></span>
* <span data-ttu-id="a52f3-2797">Åtgärda att lägga till certifikat till Linux-Vmss.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2797">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="a52f3-2798">Åtgärdade Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="a52f3-2798">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="a52f3-2799">Använd rätt tumavtryck från nya certifikat (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="a52f3-2799">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="a52f3-2800">Visa undantag korrekt (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="a52f3-2800">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="a52f3-2801">Åtgärdade Update-AzServiceFabricDurability så att klusterkonfigurationen uppdateras innan Vmss-åtgärden CreateOrUpdate påbörjas.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2801">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="a52f3-2802">0.4.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="a52f3-2802">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="a52f3-2803">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="a52f3-2803">Az.Profile</span></span>
* <span data-ttu-id="a52f3-2804">Åtgärdade problemet med Get-AzSubscription i CloudShell</span><span class="sxs-lookup"><span data-stu-id="a52f3-2804">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="a52f3-2805">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="a52f3-2805">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a52f3-2806">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a52f3-2806">Az.Compute</span></span>
* <span data-ttu-id="a52f3-2807">Nya storlekar lades till i listan över godkända VM-storlekar för vilka accelererat nätverk kommer att aktiveras vid användning av den enkla parameteruppsättningen för New-AzVm</span><span class="sxs-lookup"><span data-stu-id="a52f3-2807">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="a52f3-2808">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2808">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a52f3-2809">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a52f3-2809">Az.DataLakeStore</span></span>
* <span data-ttu-id="a52f3-2810">Lägger till stöd för regler för virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="a52f3-2810">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="a52f3-2811">Get-AzDataLakeStoreVirtualNetworkRule: Hämtar eller listar regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2811">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="a52f3-2812">Add-AzDataLakeStoreVirtualNetworkRule: Lägger till en regel för virtuellt nätverk i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2812">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="a52f3-2813">Set-AzDataLakeStoreVirtualNetworkRule: Ändrar den angivna regeln för virtuellt nätverk i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2813">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="a52f3-2814">Remove-AzDataLakeStoreVirtualNetworkRule: Tar bort en regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2814">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a52f3-2815">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a52f3-2815">Az.Network</span></span>
* <span data-ttu-id="a52f3-2816">Skicka protokollvärdet till serverdelen för att uppdatera cmdleten Test-AzNetworkWatcherConnectivity.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2816">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="a52f3-2817">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2817">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a52f3-2818">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a52f3-2818">Az.Resources</span></span>
* <span data-ttu-id="a52f3-2819">Åtgärdade problem där Get-AzRoleDefinition genererar ett oläsligt undantag (när standardprofilen inte innehåller någon prenumeration och ingen omfattning har angetts) genom att lägga till ett beskrivande undantag i scenariot.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2819">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="a52f3-2820">Ställ in ”RoleDefinitionNameParameterSet” som standardparameteruppsättning.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2820">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="a52f3-2821">0.3.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="a52f3-2821">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="a52f3-2822">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="a52f3-2822">Azure.Storage</span></span>
* <span data-ttu-id="a52f3-2823">Åtgärda fel där Kopiera blob/fil inte kopierar metadata när målplatsen har ett problem med metadata</span><span class="sxs-lookup"><span data-stu-id="a52f3-2823">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="a52f3-2824">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="a52f3-2824">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="a52f3-2825">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="a52f3-2825">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="a52f3-2826">Stöd för att hämta användningsinformation om en Storage-resurs för en specifik plats och för att lägga till ett varningsmeddelande för att hämta användningsinformation om en global Storage-resurs är inaktuellt.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2826">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="a52f3-2827">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="a52f3-2827">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="a52f3-2828">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a52f3-2828">Az.CognitiveServices</span></span>
* <span data-ttu-id="a52f3-2829">Stöd för Get-AzCognitiveServicesAccountSkus utan ett befintligt konto.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2829">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a52f3-2830">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a52f3-2830">Az.Compute</span></span>
* <span data-ttu-id="a52f3-2831">Åtgärdade fel där Get-AzVM -ResourceGroupName <rg> returnerar fler än 50 resultat om det behövs</span><span class="sxs-lookup"><span data-stu-id="a52f3-2831">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="a52f3-2832">Lade till ett exempel för SimpleParameterSet i hjälpen för cmdleten New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2832">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="a52f3-2833">Ett stavfel i förloppsmeddelandet för Azure Disk Encryption har korrigerats</span><span class="sxs-lookup"><span data-stu-id="a52f3-2833">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="a52f3-2834">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="a52f3-2834">Az.DataFactoryV2</span></span>
* <span data-ttu-id="a52f3-2835">ADF .Net SDK-versionen har uppdaterats till 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2835">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a52f3-2836">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a52f3-2836">Az.Network</span></span>
* <span data-ttu-id="a52f3-2837">Funktionalitet för NetworkProfile har lagts till.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2837">Added NetworkProfile functionality.</span></span> <span data-ttu-id="a52f3-2838">nya cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="a52f3-2838">new cmdlets added</span></span>
    - <span data-ttu-id="a52f3-2839">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a52f3-2839">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="a52f3-2840">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a52f3-2840">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="a52f3-2841">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a52f3-2841">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="a52f3-2842">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a52f3-2842">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="a52f3-2843">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="a52f3-2843">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="a52f3-2844">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="a52f3-2844">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="a52f3-2845">Länk för tjänstassociering på modell för undernät har lagts till</span><span class="sxs-lookup"><span data-stu-id="a52f3-2845">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="a52f3-2846">Cmdletarna New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap och Remove-AzVirtualNetworkTap har lagts till</span><span class="sxs-lookup"><span data-stu-id="a52f3-2846">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="a52f3-2847">Cmdletarna Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig och Remove-AzNEtworkInterfaceTapConfig har lagts till</span><span class="sxs-lookup"><span data-stu-id="a52f3-2847">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="a52f3-2848">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="a52f3-2848">Az.RedisCache</span></span>
* <span data-ttu-id="a52f3-2849">Tillåt att alla strängar används som storleksparametrar framöver.</span><span class="sxs-lookup"><span data-stu-id="a52f3-2849">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="a52f3-2850">Lägg till P5 i popup-fönstret PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="a52f3-2850">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="a52f3-2851">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a52f3-2851">Az.Resources</span></span>
* <span data-ttu-id="a52f3-2852">Parametern -Mode som saknades i Set-AzPolicyDefinition har lagts till</span><span class="sxs-lookup"><span data-stu-id="a52f3-2852">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="a52f3-2853">Åtgärdade buggen för cmdleten Get-AzProviderOperation för åtgärder med ursprung som innehåller användare</span><span class="sxs-lookup"><span data-stu-id="a52f3-2853">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="a52f3-2854">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a52f3-2854">Az.Sql</span></span>
* <span data-ttu-id="a52f3-2855">Ett problem där vissa cmdletar för säkerhetskopiering inte kunde identifiera den aktuella azure-prenumerationen har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="a52f3-2855">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a52f3-2856">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a52f3-2856">Az.Websites</span></span>
* <span data-ttu-id="a52f3-2857">Ny cmdlet: Get-AzWebAppContainerContinuousDeploymentUrl – Hämtar webhook-URL:en för kontinuerlig distribution av container</span><span class="sxs-lookup"><span data-stu-id="a52f3-2857">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="a52f3-2858">Nya cmdletar: New-AzWebAppContainerPSSession och Enter-WebAppContainerPSSession – Startar en PowerShell-fjärrsession i en containerapp för windows</span><span class="sxs-lookup"><span data-stu-id="a52f3-2858">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="a52f3-2859">0.2.0 – september 2018</span><span class="sxs-lookup"><span data-stu-id="a52f3-2859">0.2.0 - September 2018</span></span>
 <span data-ttu-id="a52f3-2860">Första versionen</span><span class="sxs-lookup"><span data-stu-id="a52f3-2860">Initial Release</span></span>
