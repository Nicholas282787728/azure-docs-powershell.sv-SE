---
title: Viktig information om Azure PowerShell
description: Lär dig mer om alla de senaste uppdateringarna för Azure PowerShell-modulerna.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 04e85c32b1af0bbdfb622973e0900724b8e3c8e3
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/01/2020
ms.locfileid: "89244236"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="f1219-103">Viktig information om Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="f1219-103">Azure PowerShell release notes</span></span>

## <a name="461---august-2020"></a><span data-ttu-id="f1219-104">4.6.1 – augusti 2020</span><span class="sxs-lookup"><span data-stu-id="f1219-104">4.6.1 - August 2020</span></span>
#### <a name="azcompute"></a><span data-ttu-id="f1219-105">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f1219-105">Az.Compute</span></span>
* <span data-ttu-id="f1219-106">Korrigerade EncryptionAtHost-parametern i New-AzVm för att ta bort standardvärdet FALSE [#12776]</span><span class="sxs-lookup"><span data-stu-id="f1219-106">Patched '-EncryptionAtHost' parameter in 'New-AzVm' to remove default value of false [#12776]</span></span>

## <a name="460---august-2020"></a><span data-ttu-id="f1219-107">4.6.0 – augusti 2020</span><span class="sxs-lookup"><span data-stu-id="f1219-107">4.6.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f1219-108">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f1219-108">Az.Accounts</span></span>
* <span data-ttu-id="f1219-109">Alla offentliga molnmiljöer läses in när slutpunktsidentifieringen inte returnerar AzureCloud (standard) eller andra offentliga miljöer [#12633]</span><span class="sxs-lookup"><span data-stu-id="f1219-109">Loaded all public cloud environments when discovery endpoint doesn't return default AzureCloud or other public environments [#12633]</span></span>
* <span data-ttu-id="f1219-110">SubscriptionPolicies har exponerats i Get-AzSubscription [#12551]</span><span class="sxs-lookup"><span data-stu-id="f1219-110">Exposed SubscriptionPolicies in 'Get-AzSubscription' [#12551]</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f1219-111">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f1219-111">Az.Automation</span></span>
* <span data-ttu-id="f1219-112">Parametern -RunOn har lagts till i Set-AzAutomationWebhook för att ange en Hybrid Worker-grupp</span><span class="sxs-lookup"><span data-stu-id="f1219-112">Added '-RunOn' parameters to 'Set-AzAutomationWebhook' to specify a Hybrid Worker Group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f1219-113">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f1219-113">Az.Compute</span></span>
* <span data-ttu-id="f1219-114">Parametern -EncryptionAtHost har lagts till i New-AzVm, New-AzVmss, New-AzVMConfig, New-AzVmssConfig, Update-AzVM och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f1219-114">Added '-EncryptionAtHost' parameter to 'New-AzVm', 'New-AzVmss', 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVM', and 'Update-AzVmss'</span></span>
* <span data-ttu-id="f1219-115">SecurityProfile har lagts till i Get-AzVM och Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f1219-115">Added 'SecurityProfile' to 'Get-AzVM' and 'Get-AzVmss' return object</span></span>
* <span data-ttu-id="f1219-116">Växeln -InstanceView har lagts till som valfri parameter i Get-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="f1219-116">Added '-InstanceView' switch as optional parameter to 'Get-AzHostGroup'</span></span>
* <span data-ttu-id="f1219-117">En ny cmdlet, Invoke-AzVmPatchAssessment, har lagts till</span><span class="sxs-lookup"><span data-stu-id="f1219-117">Added new cmdlet 'Invoke-AzVmPatchAssessment'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f1219-118">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f1219-118">Az.DataFactory</span></span>
* <span data-ttu-id="f1219-119">Saknade egenskaper har lagts till i klassen PSPipelineRun.</span><span class="sxs-lookup"><span data-stu-id="f1219-119">Added missing properties to PSPipelineRun class.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="f1219-120">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f1219-120">Az.HDInsight</span></span>
* <span data-ttu-id="f1219-121">Stöd för att skapa kluster med funktionen för kryptering under överföring.</span><span class="sxs-lookup"><span data-stu-id="f1219-121">Supported creating cluster with encryption at host feature.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f1219-122">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f1219-122">Az.KeyVault</span></span>
* <span data-ttu-id="f1219-123">Varningsmeddelanden har lagts till för planering att inaktivera mjuk borttagning</span><span class="sxs-lookup"><span data-stu-id="f1219-123">Added warning messages for planning to disable soft delete</span></span>
* <span data-ttu-id="f1219-124">Varningsmeddelanden har lagts till för planering att ta bort attributet SecretValueText</span><span class="sxs-lookup"><span data-stu-id="f1219-124">Added warning messages for planning to remove attribute SecretValueText</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="f1219-125">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="f1219-125">Az.Maintenance</span></span>
* <span data-ttu-id="f1219-126">Valfria schemarelaterade fält har lagts till i New-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="f1219-126">Added optional schedule related fields to 'New-AzMaintenanceConfiguration'</span></span>
* <span data-ttu-id="f1219-127">En ny cmdlet har lagts till för Get-AzMaintenancePublicConfiguration</span><span class="sxs-lookup"><span data-stu-id="f1219-127">Added new cmdlet for 'Get-AzMaintenancePublicConfiguration'</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="f1219-128">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="f1219-128">Az.ManagedServices</span></span>
* <span data-ttu-id="f1219-129">Varningar har lagts till om icke-bakåtkompatibla ändringar för cmdletar för tilldelning och definition av hanterade tjänster</span><span class="sxs-lookup"><span data-stu-id="f1219-129">Added breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f1219-130">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f1219-130">Az.Monitor</span></span>
* <span data-ttu-id="f1219-131">Utökade parametern som angetts i Set-AzDiagnosticSetting för separering av aktivering av loggar och mått [#12482]</span><span class="sxs-lookup"><span data-stu-id="f1219-131">Extended the parameter set in 'Set-AzDiagnosticSetting' for separation of Logs and Metrics enablement [#12482]</span></span>
* <span data-ttu-id="f1219-132">Åtgärdat fel för Add-AzMetricAlertRuleV2 vid hämtning av måttavisering från pipelinen</span><span class="sxs-lookup"><span data-stu-id="f1219-132">Fixed bug for 'Add-AzMetricAlertRuleV2' when getting metric alert from pipeline</span></span>

#### <a name="azresources"></a><span data-ttu-id="f1219-133">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f1219-133">Az.Resources</span></span>
* <span data-ttu-id="f1219-134">Get-AzPolicyAlias-svaret har uppdaterats för att ta med information som anger om aliaset kan ändras eller inte av Azure Policy.</span><span class="sxs-lookup"><span data-stu-id="f1219-134">Updated 'Get-AzPolicyAlias' response to include information indicating whether the alias is modifiable by Azure Policy.</span></span>
* <span data-ttu-id="f1219-135">Skapade en ny cmdlet, set-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="f1219-135">Created new cmdlet 'Set-AzRoleAssignment'</span></span>
* <span data-ttu-id="f1219-136">Get-AzDeploymentManagementGroupWhatIfResult har lagts till för att hämta What-If-resultat för ARM-mall i hanteringsgruppsomfånget</span><span class="sxs-lookup"><span data-stu-id="f1219-136">Added 'Get-AzDeploymentManagementGroupWhatIfResult' for getting ARM template What-If results at management Group scope</span></span>
* <span data-ttu-id="f1219-137">En ny cmdlet, Get-AzTenantWhatIfResult, har lagts till för att hämta What-If-resultat för ARM-mall i klientorganisationsomfånget</span><span class="sxs-lookup"><span data-stu-id="f1219-137">Added 'Get-AzTenantWhatIfResult' new cmdlet for getting ARM template What-If results at tenant scope</span></span>
* <span data-ttu-id="f1219-138">-WhatIf och -Confirm har åsidosatts för New-AzManagementGroupDeployment och New-AzTenantDeployment för att använda What-If-resultat för ARM-mall</span><span class="sxs-lookup"><span data-stu-id="f1219-138">Overrode '-WhatIf' and '-Confirm' for 'New-AzManagementGroupDeployment' and 'New-AzTenantDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="f1219-139">Beteenden har åtgärdats för -WhatIf och -Confirm för nya cmdletar för distribution så att de stämmer överens med False och</span><span class="sxs-lookup"><span data-stu-id="f1219-139">Fixed the behaviors of '-WhatIf' and '-Confirm' for new deployment cmdlets so they comply with False and</span></span> 
* <span data-ttu-id="f1219-140">Serialiseringsfel har åtgärdats för -TemplateObject och TemplateParameterObject [#1528] [#6292]</span><span class="sxs-lookup"><span data-stu-id="f1219-140">Fixed serialization error for '-TemplateObject' and 'TemplateParameterObject' [#1528] [#6292]</span></span>
* <span data-ttu-id="f1219-141">Attribut som medför icke-bakåtkompatibel ändring har lagts till i Get-AzResourceGroupDeploymentOperation för den kommande ändringen av utdatatyp</span><span class="sxs-lookup"><span data-stu-id="f1219-141">Added breaking change attribute to 'Get-AzResourceGroupDeploymentOperation' for the upcoming output type change</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="f1219-142">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="f1219-142">Az.SignalR</span></span>
* <span data-ttu-id="f1219-143">Fel i hjälpfilerna Restart-AzSignalR och Update-AzSignalR har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="f1219-143">Fixed 'Restart-AzSignalR' and 'Update-AzSignalR' help files errors</span></span>
* <span data-ttu-id="f1219-144">Cmdletarna Update-AzSignalRNetworkAcl och Set-AzSignalRUpstream har lagts till</span><span class="sxs-lookup"><span data-stu-id="f1219-144">Added cmdlets 'Update-AzSignalRNetworkAcl', 'Set-AzSignalRUpstream'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f1219-145">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f1219-145">Az.Storage</span></span>
* <span data-ttu-id="f1219-146">Stöd för blobfrågeacceleration</span><span class="sxs-lookup"><span data-stu-id="f1219-146">Supported blob query acceleration</span></span>
    -  <span data-ttu-id="f1219-147">Get-AzStorageBlobQueryResult</span><span class="sxs-lookup"><span data-stu-id="f1219-147">'Get-AzStorageBlobQueryResult'</span></span>
    -  <span data-ttu-id="f1219-148">New-AzStorageBlobQueryConfig</span><span class="sxs-lookup"><span data-stu-id="f1219-148">'New-AzStorageBlobQueryConfig'</span></span>
* <span data-ttu-id="f1219-149">Hjälpfil har lagts till, ytterligare beskrivning har lagts till och stavfel har korrigerats</span><span class="sxs-lookup"><span data-stu-id="f1219-149">Updated help file, added more description, and fixed typo</span></span>
    -  <span data-ttu-id="f1219-150">”Start-AzStorageBlobCopy”</span><span class="sxs-lookup"><span data-stu-id="f1219-150">'Start-AzStorageBlobCopy'</span></span>
    -  <span data-ttu-id="f1219-151">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="f1219-151">'Get-AzDataLakeGen2Item'</span></span>
* <span data-ttu-id="f1219-152">Problem med att ladda ned blob när relaterad underordnad katalog saknas har åtgärdats [#12592]</span><span class="sxs-lookup"><span data-stu-id="f1219-152">Fixed download blob fail when related sub directory not exist [#12592]</span></span>
    -  <span data-ttu-id="f1219-153">”Get-AzStorageBlobContent”</span><span class="sxs-lookup"><span data-stu-id="f1219-153">'Get-AzStorageBlobContent'</span></span>
* <span data-ttu-id="f1219-154">Replikeringsprincip för att ange, hämta, ta bort objekt på Storage-konton stöds</span><span class="sxs-lookup"><span data-stu-id="f1219-154">Supported Set/Get/Remove Object Replication Policy on Storage accounts</span></span>
    - <span data-ttu-id="f1219-155">New-AzStorageObjectReplicationPolicyRule</span><span class="sxs-lookup"><span data-stu-id="f1219-155">'New-AzStorageObjectReplicationPolicyRule'</span></span>
    - <span data-ttu-id="f1219-156">Set-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="f1219-156">'Set-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="f1219-157">Get-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="f1219-157">'Get-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="f1219-158">Remove-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="f1219-158">'Remove-AzStorageObjectReplicationPolicy'</span></span>
* <span data-ttu-id="f1219-159">Stöd har lagts till för att aktivera/inaktivera ChangeFeed i Blob Service för ett Storage-konto</span><span class="sxs-lookup"><span data-stu-id="f1219-159">Supported enable/disable ChangeFeed on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="f1219-160">”Update-AzStorageBlobServiceProperty”</span><span class="sxs-lookup"><span data-stu-id="f1219-160">'Update-AzStorageBlobServiceProperty'</span></span>

## <a name="450---august-2020"></a><span data-ttu-id="f1219-161">4.5.0 – augusti 2020</span><span class="sxs-lookup"><span data-stu-id="f1219-161">4.5.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f1219-162">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f1219-162">Az.Accounts</span></span>
* <span data-ttu-id="f1219-163">Uppdaterade ”Connect-AzAccount” så att det accepterar parametern ”MaxContextPopulation” [#9865]</span><span class="sxs-lookup"><span data-stu-id="f1219-163">Updated 'Connect-AzAccount' to accept parameter 'MaxContextPopulation' [#9865]</span></span>
* <span data-ttu-id="f1219-164">Uppdaterade SubscriptionClient-versionen till 2019-06-01 och visa klientdomäner [#9838]</span><span class="sxs-lookup"><span data-stu-id="f1219-164">Updated SubscriptionClient version to 2019-06-01 and display tenant domains [#9838]</span></span>
* <span data-ttu-id="f1219-165">Information om hemklientorganisation och managedBy-klientorganisation som stöds för prenumerationen</span><span class="sxs-lookup"><span data-stu-id="f1219-165">Supported home tenant and managedBy tenant information of subscription</span></span>
* <span data-ttu-id="f1219-166">Korrigerade modulnamn, versionsinformation i telemetridata</span><span class="sxs-lookup"><span data-stu-id="f1219-166">Corrected module name, version info in telemetry data</span></span>
* <span data-ttu-id="f1219-167">Justerade SqlDatabaseDnsSuffix och ServiceManagementUrl om miljöns slutpunkt för metadata returnerar ett inkompatibelt värde</span><span class="sxs-lookup"><span data-stu-id="f1219-167">Adjusted SqlDatabaseDnsSuffix and ServiceManagementUrl if environment metadata endpoint returns incompatible value</span></span>

#### <a name="azaks"></a><span data-ttu-id="f1219-168">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="f1219-168">Az.Aks</span></span>
* <span data-ttu-id="f1219-169">Tog bort ”ClientIdAndSecret” för ”ServicePrincipalIdAndSecret” och ställde in ”ClientIdAndSecret” som ett alias [#12381].</span><span class="sxs-lookup"><span data-stu-id="f1219-169">Removed 'ClientIdAndSecret' to 'ServicePrincipalIdAndSecret' and set 'ClientIdAndSecret' as an alias [#12381].</span></span>
* <span data-ttu-id="f1219-170">Tog bort ”Get-AzAks”/”New-AzAks”/”Remove-AzAks”/”Set-AzAks” för ”Get-AzAksCluster”/”New-AzAksCluster”/”Remove-AzAksCluster”/”Set-AzAksCluster” och ställde in de ursprungliga som alias [#12373].</span><span class="sxs-lookup"><span data-stu-id="f1219-170">Removed 'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks' to 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster' and set the original ones as alias [#12373].</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="f1219-171">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f1219-171">Az.ApiManagement</span></span>
* <span data-ttu-id="f1219-172">Lade till ny cmdlet: ”Add-AzApiManagementApiToGateway”.</span><span class="sxs-lookup"><span data-stu-id="f1219-172">Added new 'Add-AzApiManagementApiToGateway' cmdlet.</span></span>
* <span data-ttu-id="f1219-173">Lade till ny cmdlet: ”Get-AzApiManagementGateway”.</span><span class="sxs-lookup"><span data-stu-id="f1219-173">Added new 'Get-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="f1219-174">Lade till ny cmdlet: ”Get-AzApiManagementGatewayHostnameConfiguration”.</span><span class="sxs-lookup"><span data-stu-id="f1219-174">Added new 'Get-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="f1219-175">Lade till ny cmdlet: ”Get-AzApiManagementGatewayKey”.</span><span class="sxs-lookup"><span data-stu-id="f1219-175">Added new 'Get-AzApiManagementGatewayKey' cmdlet.</span></span>
* <span data-ttu-id="f1219-176">Lade till ny cmdlet: ”New-AzApiManagementGateway”.</span><span class="sxs-lookup"><span data-stu-id="f1219-176">Added new 'New-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="f1219-177">Lade till ny cmdlet: ”New-AzApiManagementGatewayHostnameConfiguration”.</span><span class="sxs-lookup"><span data-stu-id="f1219-177">Added new 'New-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="f1219-178">Lade till ny cmdlet: ”New-AzApiManagementResourceLocationObject”.</span><span class="sxs-lookup"><span data-stu-id="f1219-178">Added new 'New-AzApiManagementResourceLocationObject' cmdlet.</span></span>
* <span data-ttu-id="f1219-179">Lade till ny cmdlet: ”Remove-AzApiManagementApiFromGateway”.</span><span class="sxs-lookup"><span data-stu-id="f1219-179">Added new 'Remove-AzApiManagementApiFromGateway' cmdlet.</span></span>
* <span data-ttu-id="f1219-180">Lade till ny cmdlet: ”Remove-AzApiManagementGateway”.</span><span class="sxs-lookup"><span data-stu-id="f1219-180">Added new 'Remove-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="f1219-181">Lade till ny cmdlet: ”Remove-AzApiManagementGatewayHostnameConfiguration”.</span><span class="sxs-lookup"><span data-stu-id="f1219-181">Added new 'Remove-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="f1219-182">Lade till ny cmdlet: ”Update-AzApiManagementGateway”.</span><span class="sxs-lookup"><span data-stu-id="f1219-182">Added new 'Update-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="f1219-183">Lade till den nya valfria parametern [-GatewayId] till cmdleten ”Get-AzApiManagementApi”.</span><span class="sxs-lookup"><span data-stu-id="f1219-183">Added new optional [-GatewayId] parameter to the 'Get-AzApiManagementApi' cmdlet.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f1219-184">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f1219-184">Az.CognitiveServices</span></span>
* <span data-ttu-id="f1219-185">Använde ”Neka” som standardåtgärd för NetworkRules.</span><span class="sxs-lookup"><span data-stu-id="f1219-185">Used 'Deny' specifically as NetworkRules default action.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="f1219-186">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f1219-186">Az.FrontDoor</span></span>
* <span data-ttu-id="f1219-187">Åtgärdade ett problem där ett undantag uppstår när Enum.Parse försöker att tvinga ett null-värde till aktiverade eller inaktiverade uppräkningsvärden [#12344]</span><span class="sxs-lookup"><span data-stu-id="f1219-187">Fixed an issue where an exception is being thrown when Enum.Parse tries to coerce a null value to an Enabled or Disabled enum values [#12344]</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="f1219-188">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f1219-188">Az.HDInsight</span></span>
* <span data-ttu-id="f1219-189">Stöd för att skapa kluster med funktionen Kryptering under överföring.</span><span class="sxs-lookup"><span data-stu-id="f1219-189">Supported creating cluster with encryption in transit feature.</span></span>
    - <span data-ttu-id="f1219-190">Lägg till den nya parametern ”EncryptionInTransit” till cmdleten ”New-AzHDInsightCluster”</span><span class="sxs-lookup"><span data-stu-id="f1219-190">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="f1219-191">Lägg till den nya parametern ”EncryptionInTransit” till cmdleten ”New-AzHDInsightClusterConfig”</span><span class="sxs-lookup"><span data-stu-id="f1219-191">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="f1219-192">Stöd för att skapa kluster med funktionen privat länk:</span><span class="sxs-lookup"><span data-stu-id="f1219-192">Supported creating cluster with private link feature:</span></span>
    - <span data-ttu-id="f1219-193">Lägg till de nya parametrarna ”PublicNetworkAccessType” och ”OutboundPublicNetworkAccessType” till cmdleten ”New-AzHDInsightCluster”</span><span class="sxs-lookup"><span data-stu-id="f1219-193">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="f1219-194">Lägg till de nya parametrarna ”PublicNetworkAccessType” och ”OutboundPublicNetworkAccessType” till cmdleten ”New-AzHDInsightClusterConfig”</span><span class="sxs-lookup"><span data-stu-id="f1219-194">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="f1219-195">Returnerade information om det virtuella nätverket vid anrop till ”New-AzHDInsightCluster” eller ”Get-AzHDInsightCluster”</span><span class="sxs-lookup"><span data-stu-id="f1219-195">Returned virtual network information when calling 'New-AzHDInsightCluster' or 'Get-AzHDInsightCluster'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f1219-196">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f1219-196">Az.Network</span></span>
* <span data-ttu-id="f1219-197">Stöd har lagts till för parametern AddressPrefixType i ”Remove-AzExpressRouteCircuitConnectionConfig”</span><span class="sxs-lookup"><span data-stu-id="f1219-197">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="f1219-198">Lade till bakåtkompatibel ändringar: PeerAddressType-funktioner för privat peering i ”Remove-AzExpressRouteCircutPeeringConfig”.</span><span class="sxs-lookup"><span data-stu-id="f1219-198">Added non-breaking changes: PeerAddressType functionality for Private Peering in 'Remove-AzExpressRouteCircutPeeringConfig'.</span></span>
* <span data-ttu-id="f1219-199">Koden ändrades för att ignorera skiftläge för parametrarna AddressPrefixType och PeerAddressType.</span><span class="sxs-lookup"><span data-stu-id="f1219-199">Code changed to ignore case for AddressPrefixType and PeerAddressType parameter.</span></span>
* <span data-ttu-id="f1219-200">Ändrade varningsmeddelandet för ”New-AzLoadBalancerFrontendIpConfig”, ”New-AzPublicIpAddress” och ”New-AzPublicIpPrefix”.</span><span class="sxs-lookup"><span data-stu-id="f1219-200">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f1219-201">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f1219-201">Az.OperationalInsights</span></span>
* <span data-ttu-id="f1219-202">Lade till alternativet ”-ForceDelete” för ”Remove-AzOperationalInsightsworkspace”</span><span class="sxs-lookup"><span data-stu-id="f1219-202">Added '-ForceDelete' option for 'Remove-AzOperationalInsightsworkspace'</span></span>
* <span data-ttu-id="f1219-203">Lade till ny cmdlet: ”Get-AzOperationalInsightsDeletedWorkspace”</span><span class="sxs-lookup"><span data-stu-id="f1219-203">Added new cmdlet 'Get-AzOperationalInsightsDeletedWorkspace'</span></span>
* <span data-ttu-id="f1219-204">Lade till ny cmdlet: ”Restore-AzOperationalInsightsWorkspace”</span><span class="sxs-lookup"><span data-stu-id="f1219-204">Added new cmdlet 'Restore-AzOperationalInsightsWorkspace'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f1219-205">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f1219-205">Az.RecoveryServices</span></span>
* <span data-ttu-id="f1219-206">Förbättrade sättet Azure Backup-containrar/objekt identifieras.</span><span class="sxs-lookup"><span data-stu-id="f1219-206">Improved the Azure Backup container/item discovery experience.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f1219-207">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f1219-207">Az.Resources</span></span>
* <span data-ttu-id="f1219-208">Lade till egenskaperna ”Condition”, ”ConditionVersion” och ”Description” till ”New-AzRoleAssignment”</span><span class="sxs-lookup"><span data-stu-id="f1219-208">Added properties 'Condition', 'ConditionVersion' and 'Description' to 'New-AzRoleAssignment'</span></span>
    - <span data-ttu-id="f1219-209">Detta omfattade alla relevanta ändringar av datamodellerna</span><span class="sxs-lookup"><span data-stu-id="f1219-209">This included all the relevant changes to the data models</span></span>

#### <a name="azsql"></a><span data-ttu-id="f1219-210">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f1219-210">Az.Sql</span></span>
* <span data-ttu-id="f1219-211">Korrigerade ett potentiellt fel med skiftlägesokänsliga servernamn i ”New-AzSqlServer” och ”Set-AzSqlServer”</span><span class="sxs-lookup"><span data-stu-id="f1219-211">Fixed potential server name case insensitive error in 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="f1219-212">Korrigerade att fel databasnamn returnerades vid ett befintligt databasfel i ”New-AzSqlDatabaseSecondary”</span><span class="sxs-lookup"><span data-stu-id="f1219-212">Fixed wrong database name returned on existing database error in 'New-AzSqlDatabaseSecondary'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f1219-213">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f1219-213">Az.Storage</span></span>
* <span data-ttu-id="f1219-214">Stöd för att skapa container/blob för SAS-token med de nya behörigheterna x, t</span><span class="sxs-lookup"><span data-stu-id="f1219-214">Supported create container/blob Sas token with new permission x,t</span></span>
    -  <span data-ttu-id="f1219-215">”New-AzStorageBlobSASToken”</span><span class="sxs-lookup"><span data-stu-id="f1219-215">'New-AzStorageBlobSASToken'</span></span>
    -  <span data-ttu-id="f1219-216">”New-AzStorageContainerSASToken”</span><span class="sxs-lookup"><span data-stu-id="f1219-216">'New-AzStorageContainerSASToken'</span></span>
* <span data-ttu-id="f1219-217">Stöd för att skapa konto för SAS-token med de nya behörigheterna x, t, f</span><span class="sxs-lookup"><span data-stu-id="f1219-217">Supported create account Sas token with new permission x,t,f</span></span>
    -  <span data-ttu-id="f1219-218">”New-AzStorageAccountSASToken”</span><span class="sxs-lookup"><span data-stu-id="f1219-218">'New-AzStorageAccountSASToken'</span></span>
* <span data-ttu-id="f1219-219">Stöd för att hämta förbrukning av enskild filresurs</span><span class="sxs-lookup"><span data-stu-id="f1219-219">Supported get single file share usage</span></span>
    - <span data-ttu-id="f1219-220">”Get-AzRmStorageShare”</span><span class="sxs-lookup"><span data-stu-id="f1219-220">'Get-AzRmStorageShare'</span></span>

## <a name="440---july-2020"></a><span data-ttu-id="f1219-221">4.4.0 – juli 2020</span><span class="sxs-lookup"><span data-stu-id="f1219-221">4.4.0 - July 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f1219-222">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f1219-222">Az.Accounts</span></span>
* <span data-ttu-id="f1219-223">En ny cmdlet, ”Invoke-AzRestMethod”, har lagts till</span><span class="sxs-lookup"><span data-stu-id="f1219-223">Added new cmdlet 'Invoke-AzRestMethod'</span></span>
* <span data-ttu-id="f1219-224">Ett problem åtgärdades som kan orsaka autentiseringsfel i scenarier med fler processer, t.ex. när flera Azure PowerShell-cmdletar körs med ”Start-Job” [#9448]</span><span class="sxs-lookup"><span data-stu-id="f1219-224">Fixed an issue that may cause authentication errors in multi-process scenarios such as running multiple Azure PowerShell cmdlets using 'Start-Job' [#9448]</span></span>

#### <a name="azaks"></a><span data-ttu-id="f1219-225">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="f1219-225">Az.Aks</span></span>
* <span data-ttu-id="f1219-226">Felet som gjorde att ”Get-AzAks” inte hämtade alla kluster har åtgärdats [#12296]</span><span class="sxs-lookup"><span data-stu-id="f1219-226">Fixed bug 'Get-AzAks' doesn't get all clusters [#12296]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="f1219-227">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f1219-227">Az.AnalysisServices</span></span>
* <span data-ttu-id="f1219-228">Projektreferensen till autentisering har tagits bort</span><span class="sxs-lookup"><span data-stu-id="f1219-228">Removed project reference to Authentication</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f1219-229">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f1219-229">Az.Automation</span></span>
* <span data-ttu-id="f1219-230">Problemet som gjorde att strängar med escape-tecken inte kunde konverteras till JSON-objekt har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="f1219-230">Fixed the issue that string with escape chars cannot be converted into json object.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f1219-231">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f1219-231">Az.Compute</span></span>
* <span data-ttu-id="f1219-232">En varning har lats till som visas när ”New-AzVmss” används utan den senaste avbildningsversionen</span><span class="sxs-lookup"><span data-stu-id="f1219-232">Added warning when using 'New-AzVmss' without 'latest' image version</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f1219-233">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f1219-233">Az.DataFactory</span></span>
* <span data-ttu-id="f1219-234">Globala parametrar har lagts till för Data Factory.</span><span class="sxs-lookup"><span data-stu-id="f1219-234">Added global parameters to Data Factory.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="f1219-235">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="f1219-235">Az.EventGrid</span></span>
* <span data-ttu-id="f1219-236">Modulen har uppdaterats så att API-version 2020-06-01 används.</span><span class="sxs-lookup"><span data-stu-id="f1219-236">Updated to use the 2020-06-01 API version.</span></span>
* <span data-ttu-id="f1219-237">Nya funktioner har lagts till:</span><span class="sxs-lookup"><span data-stu-id="f1219-237">Added new features:</span></span>
    - <span data-ttu-id="f1219-238">Indatamappning</span><span class="sxs-lookup"><span data-stu-id="f1219-238">Input mapping</span></span>
    - <span data-ttu-id="f1219-239">Schema för händelseleverans</span><span class="sxs-lookup"><span data-stu-id="f1219-239">Event Delivery Schema</span></span>
    - <span data-ttu-id="f1219-240">Private Link</span><span class="sxs-lookup"><span data-stu-id="f1219-240">Private Link</span></span>
    - <span data-ttu-id="f1219-241">Cloud Event V10 Schema</span><span class="sxs-lookup"><span data-stu-id="f1219-241">Cloud Event V10 Schema</span></span>
    - <span data-ttu-id="f1219-242">Service Bus-ämne som mål</span><span class="sxs-lookup"><span data-stu-id="f1219-242">Service Bus Topic As Destination</span></span>
    - <span data-ttu-id="f1219-243">Azure-funktion som mål</span><span class="sxs-lookup"><span data-stu-id="f1219-243">Azure Function As Destination</span></span>
    - <span data-ttu-id="f1219-244">Webhook-batchbearbetning</span><span class="sxs-lookup"><span data-stu-id="f1219-244">WebHook Batching</span></span>
    - <span data-ttu-id="f1219-245">Säker webhook (AAD-stöd)</span><span class="sxs-lookup"><span data-stu-id="f1219-245">Secure webhook (AAD support)</span></span>
    - <span data-ttu-id="f1219-246">IpFiltering</span><span class="sxs-lookup"><span data-stu-id="f1219-246">IpFiltering</span></span>
* <span data-ttu-id="f1219-247">Uppdaterade cmdletar:</span><span class="sxs-lookup"><span data-stu-id="f1219-247">Updated cmdlets:</span></span>
    - <span data-ttu-id="f1219-248">”New-AzEventGridSubscription”/”Update-AzEventGridSubscription”:</span><span class="sxs-lookup"><span data-stu-id="f1219-248">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span></span>
        - <span data-ttu-id="f1219-249">Lägg till nya valfria parametrar för att ge stöd för webhook-batchbearbetning.</span><span class="sxs-lookup"><span data-stu-id="f1219-249">Add new optional parameters to support webhook batching.</span></span>
        - <span data-ttu-id="f1219-250">Lägg till nya valfria parametrar för att ge stöd för skyddad webhook med AAD.</span><span class="sxs-lookup"><span data-stu-id="f1219-250">Add new optional parameters to support secured webhook using AAD.</span></span>
        - <span data-ttu-id="f1219-251">Lägg till ny enum (uppräkning) för EndpointType-parametern för att ge stöd för Azure-funktion och Service Bus-ämne som nya mål.</span><span class="sxs-lookup"><span data-stu-id="f1219-251">Add new enum for EndpointType parameter to support azure function and service bus topic as new destinations.</span></span>
        - <span data-ttu-id="f1219-252">Lägg till ny valfri parameter för leveransschema.</span><span class="sxs-lookup"><span data-stu-id="f1219-252">Add new optional parameter for delivery schema.</span></span>
    - <span data-ttu-id="f1219-253">”New-AzEventGridTopic”/”Update-AzEventGridTopic” och ”New-AzEventGridDomain”/”Update-AzEventGridDomain”:</span><span class="sxs-lookup"><span data-stu-id="f1219-253">'New-AzEventGridTopic'/'Update-AzEventGridTopic' and 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span></span>
        - <span data-ttu-id="f1219-254">Lägg till nya valfria parametrar för att ge stöd för IpFiltering.</span><span class="sxs-lookup"><span data-stu-id="f1219-254">Add new optional parameters to support IpFiltering.</span></span>
    - <span data-ttu-id="f1219-255">”New-AzEventGridTopic”/”New-AzEventGridDomain”:</span><span class="sxs-lookup"><span data-stu-id="f1219-255">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span></span>
        - <span data-ttu-id="f1219-256">Lägg till nya valfria parametrar för att ge stöd för indatamappning.</span><span class="sxs-lookup"><span data-stu-id="f1219-256">Add new optional parameters to support Input mapping.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="f1219-257">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f1219-257">Az.FrontDoor</span></span>
* <span data-ttu-id="f1219-258">Modulen har uppdaterats så att API 2020-05-01 används</span><span class="sxs-lookup"><span data-stu-id="f1219-258">Updated module to use API 2020-05-01</span></span>
* <span data-ttu-id="f1219-259">Stöd för privat länk har lagts till för Storage-, KeyVault- och Web App Service-resurser</span><span class="sxs-lookup"><span data-stu-id="f1219-259">Added Private link support for Storage, Keyvault and Web App Service resources</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="f1219-260">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f1219-260">Az.HDInsight</span></span>
* <span data-ttu-id="f1219-261">Stöd för att skapa kluster med ADLSGen1/2-lagring i nationella moln.</span><span class="sxs-lookup"><span data-stu-id="f1219-261">Supported creating cluster with ADLSGen1/2 storage in national clouds.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f1219-262">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f1219-262">Az.Monitor</span></span>
* <span data-ttu-id="f1219-263">Bugg som orsakade fel med ”Get-AzDiagnosticSetting” när mått eller loggar var null har åtgärdats [#12272]</span><span class="sxs-lookup"><span data-stu-id="f1219-263">Fixed bug for 'Get-AzDiagnosticSetting' when metrics or logs are null [#12272]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f1219-264">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f1219-264">Az.Network</span></span>
* <span data-ttu-id="f1219-265">Parameterväxlingen i VWan HubVnet-anslutningar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="f1219-265">Fixed parameters swap in VWan HubVnet connection</span></span>
* <span data-ttu-id="f1219-266">Nya cmdletar har lagts till för platser för virtuella installationer i Azure-nätverk</span><span class="sxs-lookup"><span data-stu-id="f1219-266">Added new cmdlets for Azure Network Virtual Appliance Sites</span></span>
    - <span data-ttu-id="f1219-267">”Get-AzVirtualApplianceSite”</span><span class="sxs-lookup"><span data-stu-id="f1219-267">'Get-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="f1219-268">”New-AzVirtualApplianceSite”</span><span class="sxs-lookup"><span data-stu-id="f1219-268">'New-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="f1219-269">”Remove-AzVirtualApplianceSite”</span><span class="sxs-lookup"><span data-stu-id="f1219-269">'Remove-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="f1219-270">”Update-AzVirtualApplianceSite”</span><span class="sxs-lookup"><span data-stu-id="f1219-270">'Update-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="f1219-271">”New-AzOffice365PolicyProperty”</span><span class="sxs-lookup"><span data-stu-id="f1219-271">'New-AzOffice365PolicyProperty'</span></span>
* <span data-ttu-id="f1219-272">Nya cmdletar har lagts till för virtuella installationer i Azure-nätverk</span><span class="sxs-lookup"><span data-stu-id="f1219-272">Added new cmdlets for Azure Network Virtual Appliance</span></span>
    - <span data-ttu-id="f1219-273">”Get-AzNetworkVirtualAppliance”</span><span class="sxs-lookup"><span data-stu-id="f1219-273">'Get-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="f1219-274">”New-AzNetworkVirtualAppliance”</span><span class="sxs-lookup"><span data-stu-id="f1219-274">'New-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="f1219-275">”Remove-AzNetworkVirtualAppliance”</span><span class="sxs-lookup"><span data-stu-id="f1219-275">'Remove-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="f1219-276">”Update-AzNetworkVirtualAppliance”</span><span class="sxs-lookup"><span data-stu-id="f1219-276">'Update-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="f1219-277">”Get-AzNetworkVirtualApplianceSku”</span><span class="sxs-lookup"><span data-stu-id="f1219-277">'Get-AzNetworkVirtualApplianceSku'</span></span>
    - <span data-ttu-id="f1219-278">”New-AzVirtualApplianceSkuProperty”</span><span class="sxs-lookup"><span data-stu-id="f1219-278">'New-AzVirtualApplianceSkuProperty'</span></span>
* <span data-ttu-id="f1219-279">Application Gateway har introducerats i vanliga cmdletar för Private Link</span><span class="sxs-lookup"><span data-stu-id="f1219-279">Onboarded Application Gateway to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="f1219-280">StorageSync har introducerats i vanliga cmdletar för Private Link</span><span class="sxs-lookup"><span data-stu-id="f1219-280">Onboarded StorageSync to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="f1219-281">SignalR har introducerats i vanliga cmdletar för Private Link</span><span class="sxs-lookup"><span data-stu-id="f1219-281">Onboarded SignalR to Private Link Common Cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f1219-282">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f1219-282">Az.RecoveryServices</span></span>
* <span data-ttu-id="f1219-283">Projektreferensen till autentisering har tagits bort</span><span class="sxs-lookup"><span data-stu-id="f1219-283">Removed project reference to Authentication</span></span>
* <span data-ttu-id="f1219-284">Azure Backup-anpassade cmdletar gör text mer korrekt.</span><span class="sxs-lookup"><span data-stu-id="f1219-284">Azure Backup tuned cmdlets help text to be more accurate.</span></span>
* <span data-ttu-id="f1219-285">Stöd har lagts till som gör att Azure Backup kan hämta MAB-agentjobb med cmdleten ”Get-AzRecoveryServicesBackupJob”.</span><span class="sxs-lookup"><span data-stu-id="f1219-285">Azure Backup added support for fetching MAB agent jobs using 'Get-AzRecoveryServicesBackupJob' cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f1219-286">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f1219-286">Az.Resources</span></span>
* <span data-ttu-id="f1219-287">”Save-AzResourceGroupDeploymentTemplate” har uppdaterats för att använda SDK:n.</span><span class="sxs-lookup"><span data-stu-id="f1219-287">Updated 'Save-AzResourceGroupDeploymentTemplate' to use the SDK.</span></span>
* <span data-ttu-id="f1219-288">Cmdleten ”Unregister-AzResourceProvider” har lagts till.</span><span class="sxs-lookup"><span data-stu-id="f1219-288">Added 'Unregister-AzResourceProvider' cmdlet.</span></span>

#### <a name="azsql"></a><span data-ttu-id="f1219-289">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f1219-289">Az.Sql</span></span>
* <span data-ttu-id="f1219-290">Stöd har lagts till för SPN och gästanvändare i cmdleten ”Set-AzSqlInstanceActiveDirectoryAdministrator”</span><span class="sxs-lookup"><span data-stu-id="f1219-290">Added support for Service principal and guest users in Set-AzSqlInstanceActiveDirectoryAdministrator cmdlet'</span></span>
* <span data-ttu-id="f1219-291">En bugg har åtgärdats i cmdletar för dataklassificering.</span><span class="sxs-lookup"><span data-stu-id="f1219-291">Fixed a bug in Data Classification cmdlets.'</span></span>
* <span data-ttu-id="f1219-292">Stöd har lagts till för redundansväxling med Azure SQL Managed Instance: ”Invoke-AzSqlInstanceFailover”</span><span class="sxs-lookup"><span data-stu-id="f1219-292">Added support for Azure SQL Managed Instance failover: 'Invoke-AzSqlInstanceFailover'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f1219-293">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f1219-293">Az.Storage</span></span>
* <span data-ttu-id="f1219-294">Problemet som gjorde att UserAgent inte lades till för vissa cmdletar för dataplanet har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="f1219-294">Fixed the issue that UserAgent is not added for some data plane cmdlets.</span></span>
* <span data-ttu-id="f1219-295">Stöd har lagts till för att skapa/uppdatera Storage-konto med MinimumTlsVersion och AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="f1219-295">Supported create/update Storage account with MinimumTlsVersion and AllowBlobPublicAccess</span></span>
    -  <span data-ttu-id="f1219-296">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="f1219-296">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="f1219-297">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="f1219-297">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="f1219-298">Stöd har lagts till för att aktivera/inaktivera versionshantering i Blob Service för ett Storage-konto</span><span class="sxs-lookup"><span data-stu-id="f1219-298">Support enable/disable versioning on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="f1219-299">”Update-AzStorageBlobServiceProperty”</span><span class="sxs-lookup"><span data-stu-id="f1219-299">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="f1219-300">Stöd har lagts till för att visa blobar med blobversioner</span><span class="sxs-lookup"><span data-stu-id="f1219-300">Support list blobs with blob versions</span></span>
    - <span data-ttu-id="f1219-301">”Get-AzStorageBlob”</span><span class="sxs-lookup"><span data-stu-id="f1219-301">'Get-AzStorageBlob'</span></span>
* <span data-ttu-id="f1219-302">Stöd har lagts till för att hämta/ta bort enskilda ögonblicksbilder av blobar eller blobversioner</span><span class="sxs-lookup"><span data-stu-id="f1219-302">Support get/remove single blob snapshot or blob version</span></span>
    - <span data-ttu-id="f1219-303">”Get-AzStorageBlob”</span><span class="sxs-lookup"><span data-stu-id="f1219-303">'Get-AzStorageBlob'</span></span>
    - <span data-ttu-id="f1219-304">”Remove-AzStorageBlob”</span><span class="sxs-lookup"><span data-stu-id="f1219-304">'Remove-AzStorageBlob'</span></span>
* <span data-ttu-id="f1219-305">Stöd har lagts till för pipelines från blobobjekt genererade av Azure.Storage.Blobs V12</span><span class="sxs-lookup"><span data-stu-id="f1219-305">Support pipeline from blob object generated from Azure.Storage.Blobs V12</span></span>
    - <span data-ttu-id="f1219-306">”Get-AzStorageBlobContent”</span><span class="sxs-lookup"><span data-stu-id="f1219-306">'Get-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="f1219-307">”New-AzStorageBlobSASToken”</span><span class="sxs-lookup"><span data-stu-id="f1219-307">'New-AzStorageBlobSASToken'</span></span>
    - <span data-ttu-id="f1219-308">”Remove-AzStorageBlob”</span><span class="sxs-lookup"><span data-stu-id="f1219-308">'Remove-AzStorageBlob'</span></span>
    - <span data-ttu-id="f1219-309">”Set-AzStorageBlobContent”</span><span class="sxs-lookup"><span data-stu-id="f1219-309">'Set-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="f1219-310">”Start-AzStorageBlobCopy”</span><span class="sxs-lookup"><span data-stu-id="f1219-310">'Start-AzStorageBlobCopy'</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="f1219-311">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="f1219-311">Az.StorageSync</span></span>
* <span data-ttu-id="f1219-312">En ny version har lagts till för StorageSync SDK som körs mot ApiVersion 2020-03-01</span><span class="sxs-lookup"><span data-stu-id="f1219-312">Added a new version StorageSync SDK targeting ApiVersion 2020-03-01</span></span>
* <span data-ttu-id="f1219-313">En cmdlet för synkroniseringstjänsten för lagringsuppdatering har lagts till</span><span class="sxs-lookup"><span data-stu-id="f1219-313">Added Update Storage Sync Service cmdlet</span></span>
    - <span data-ttu-id="f1219-314">”Set-AzStorageSyncService”</span><span class="sxs-lookup"><span data-stu-id="f1219-314">'Set-AzStorageSyncService'</span></span>
* <span data-ttu-id="f1219-315">IncomingTrafficPolicy och PrivateEndpointConnections har lagts till för StorageSyncService-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="f1219-315">Added IncomingTrafficPolicy and PrivateEndpointConnections to StorageSyncService cmdlets.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f1219-316">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f1219-316">Az.Websites</span></span>
* <span data-ttu-id="f1219-317">Stöd har lagts till för att utföra åtgärder för platser som inte tillhör samma resursgrupp som App Services-planen</span><span class="sxs-lookup"><span data-stu-id="f1219-317">Added support to perform operations for Slots not in the same resource group as the App Service Plan</span></span>

## <a name="430---june-2020"></a><span data-ttu-id="f1219-318">4.3.0 – juni 2020</span><span class="sxs-lookup"><span data-stu-id="f1219-318">4.3.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f1219-319">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f1219-319">Az.Accounts</span></span>
* <span data-ttu-id="f1219-320">Stöd för identifiering av miljöinställning som standard och tillägg av miljön via ”Add-AzEnvironment”</span><span class="sxs-lookup"><span data-stu-id="f1219-320">Supported discovering environment setting by default and adding environment via 'Add-AzEnvironment'</span></span>
* <span data-ttu-id="f1219-321">Uppdatera förinlästa sammansättningar [#12024], [#11976]</span><span class="sxs-lookup"><span data-stu-id="f1219-321">Update preloaded assemblies [#12024], [#11976]</span></span>
* <span data-ttu-id="f1219-322">Uppdaterad Azure.Core-sammansättning</span><span class="sxs-lookup"><span data-stu-id="f1219-322">Updated Azure.Core assembly</span></span>
* <span data-ttu-id="f1219-323">Ett problem har åtgärdats som kan orsaka att ”Connect-AzAccount” misslyckas vid körning av flera trådar [#11201]</span><span class="sxs-lookup"><span data-stu-id="f1219-323">Fixed an issue that may cause 'Connect-AzAccount' to fail in multi-threaded execution [#11201]</span></span>

#### <a name="azaks"></a><span data-ttu-id="f1219-324">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="f1219-324">Az.Aks</span></span>
* <span data-ttu-id="f1219-325">Användning av gamla [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) ersattes med anrop till API:erna [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) och [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials)</span><span class="sxs-lookup"><span data-stu-id="f1219-325">Replaced usage of old [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) with calls to [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) and [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials) APIs</span></span>

#### <a name="azbatch"></a><span data-ttu-id="f1219-326">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="f1219-326">Az.Batch</span></span>
* <span data-ttu-id="f1219-327">Az.Batch har uppdaterats att använda ”Microsoft.Azure.Management.Batch” SDK till och med version 11.0.0.</span><span class="sxs-lookup"><span data-stu-id="f1219-327">Updated Az.Batch to use 'Microsoft.Azure.Management.Batch' SDK version to 11.0.0</span></span>
* <span data-ttu-id="f1219-328">Möjligheten att ange BatchAccount-identiteten har lagts till i cmdleten ”New-AzBatchAccount”</span><span class="sxs-lookup"><span data-stu-id="f1219-328">Added the ability to set the BatchAccount Identity in the 'New-AzBatchAccount' cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f1219-329">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f1219-329">Az.CognitiveServices</span></span>
* <span data-ttu-id="f1219-330">Stöd för att visa kontofunktioner.</span><span class="sxs-lookup"><span data-stu-id="f1219-330">Supported displaying account capabilities.</span></span>
* <span data-ttu-id="f1219-331">Stöd för att ändra PublicNetworkAccess.</span><span class="sxs-lookup"><span data-stu-id="f1219-331">Supported modifying PublicNetworkAccess.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f1219-332">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f1219-332">Az.Compute</span></span>
* <span data-ttu-id="f1219-333">Parametern SimulateEviction har lagts till i cmdletarna set-AzVM och set-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="f1219-333">Added SimulateEviction parameter to Set-AzVM and Set-AzVmssVM cmdlets.</span></span>
* <span data-ttu-id="f1219-334">”Premium_LRS” har lagts till i argumentslutföraren för parametern StorageAccountType för cmdleten New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="f1219-334">Added 'Premium_LRS' to the argument completer of StorageAccountType parameter for New-AzGalleryImageVersion cmdlet.</span></span>
* <span data-ttu-id="f1219-335">Understatusar har lagts till i VMCustomScriptExtension [#11297]</span><span class="sxs-lookup"><span data-stu-id="f1219-335">Added Substatuses to VMCustomScriptExtension [#11297]</span></span>
* <span data-ttu-id="f1219-336">”Delete” har lagts till i argumentslutföraren för parametern EvictionPolicy för cmdletarna New-AzVM och New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="f1219-336">Added 'Delete' to the argument completer of EvictionPolicy parameter for New-AzVM and New-AzVMConfig cmdlets.</span></span>
* <span data-ttu-id="f1219-337">Åtgärdat namn för nytt VM-tillägg för SAP</span><span class="sxs-lookup"><span data-stu-id="f1219-337">Fixed name of new VM Extension for SAP</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f1219-338">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f1219-338">Az.DataFactory</span></span>
* <span data-ttu-id="f1219-339">ADF .Net SDK har uppdaterats till 4.9.0</span><span class="sxs-lookup"><span data-stu-id="f1219-339">Updated ADF .Net SDK version to 4.9.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f1219-340">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f1219-340">Az.EventHub</span></span>
* <span data-ttu-id="f1219-341">Parametrar för hanterad identitet har lagts till i cmdletarna ”New-AzEventHubNamespace” och ”set-AzEventHubNamespace”</span><span class="sxs-lookup"><span data-stu-id="f1219-341">Added Managed Identity parameters to 'New-AzEventHubNamespace' and 'Set-AzEventHubNamespace' cmdlets</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="f1219-342">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="f1219-342">Az.Functions</span></span>
* <span data-ttu-id="f1219-343">Stöd har lagts till för att skapa PowerShell 7.0- och Java 11-funktionsappar</span><span class="sxs-lookup"><span data-stu-id="f1219-343">Added support to create PowerShell 7.0 and Java 11 function apps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="f1219-344">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f1219-344">Az.HDInsight</span></span>
* <span data-ttu-id="f1219-345">Stöd för listning av värdar och omstart för specifika värdar i HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="f1219-345">Supported listing hosts and restart specific hosts of the HDInsight cluster.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="f1219-346">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="f1219-346">Az.HealthcareApis</span></span>
* <span data-ttu-id="f1219-347">Uppdaterade SDK-versionen till 1.1.0</span><span class="sxs-lookup"><span data-stu-id="f1219-347">Updated the SDK version to 1.1.0</span></span>
* <span data-ttu-id="f1219-348">Stöd har lagts till för exportinställningar och hanterad identitet</span><span class="sxs-lookup"><span data-stu-id="f1219-348">Added support for Export settings and Managed Identity</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f1219-349">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f1219-349">Az.Monitor</span></span>
* <span data-ttu-id="f1219-350">Parameter för inmatningsobjekt har åtgärdats för ”Set-AzActivityLogAlert”</span><span class="sxs-lookup"><span data-stu-id="f1219-350">Fixed input object parameter for 'Set-AzActivityLogAlert'</span></span>
* <span data-ttu-id="f1219-351">Parametern ”InputObject” har åtgärdats för ”Set-AzActionGroup” [#10868]</span><span class="sxs-lookup"><span data-stu-id="f1219-351">Fixed 'InputObject' parameter for 'Set-AzActionGroup' [#10868]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f1219-352">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f1219-352">Az.Network</span></span>
* <span data-ttu-id="f1219-353">Stöd har lagts till för parametern AddressPrefixType i ”Remove-AzExpressRouteCircuitConnectionConfig”</span><span class="sxs-lookup"><span data-stu-id="f1219-353">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="f1219-354">Nya cmdletar har lagts till för Azure FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="f1219-354">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="f1219-355">”New-AzFirewallPolicyDnsSetting”</span><span class="sxs-lookup"><span data-stu-id="f1219-355">'New-AzFirewallPolicyDnsSetting'</span></span>
    - <span data-ttu-id="f1219-356">Stöd för mål-FQDN i nätverksregler för brandväggsprincip</span><span class="sxs-lookup"><span data-stu-id="f1219-356">Support for Destination FQDN in Network Rules for Firewall Policy</span></span>
* <span data-ttu-id="f1219-357">Stöd har lagts till för åtgärder i serverdelsadresspooler</span><span class="sxs-lookup"><span data-stu-id="f1219-357">Added support for backend address pool operations</span></span>
    - <span data-ttu-id="f1219-358">”New-AzLoadBalancerBackendAddressConfig”</span><span class="sxs-lookup"><span data-stu-id="f1219-358">'New-AzLoadBalancerBackendAddressConfig'</span></span>
    - <span data-ttu-id="f1219-359">”New-AzLoadBalancerBackendAddressPool”</span><span class="sxs-lookup"><span data-stu-id="f1219-359">'New-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="f1219-360">”Set-AzLoadBalancerBackendAddressPool”</span><span class="sxs-lookup"><span data-stu-id="f1219-360">'Set-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="f1219-361">”Remove-AzLoadBalancerBackendAddressPool”</span><span class="sxs-lookup"><span data-stu-id="f1219-361">'Remove-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="f1219-362">”Get-AzLoadBalancerBackendAddressPool”</span><span class="sxs-lookup"><span data-stu-id="f1219-362">'Get-AzLoadBalancerBackendAddressPool'</span></span>
* <span data-ttu-id="f1219-363">Namnvalidering har lagts till för ”New-AzIpGroup”</span><span class="sxs-lookup"><span data-stu-id="f1219-363">Added name validation for 'New-AzIpGroup'</span></span>
* <span data-ttu-id="f1219-364">Nya cmdletar har lagts till för Azure FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="f1219-364">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="f1219-365">”New-AzFirewallPolicyThreatIntelWhitelist”</span><span class="sxs-lookup"><span data-stu-id="f1219-365">'New-AzFirewallPolicyThreatIntelWhitelist'</span></span>
* <span data-ttu-id="f1219-366">Nedanstående kommandon för funktionen har uppdaterats: Konfiguration/borttagning av anpassade DNS-servrar på VirtualWan P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="f1219-366">Updated below commands for feature: Custom dns servers set/remove on VirtualWan P2SVpnGateway.</span></span>
    - <span data-ttu-id="f1219-367">New-AzP2sVpnGateway har uppdaterats: Den valfria parametern ”-CustomDnsServer” har lagts till för att kunder ska kunna ange att deras DNS-servrar ska konfigureras på P2SVpnGateway, som kan användas av punkt-till-plats-klienter.</span><span class="sxs-lookup"><span data-stu-id="f1219-367">Updated New-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
    - <span data-ttu-id="f1219-368">Update-AzP2sVpnGateway har uppdaterats: Den valfria parametern ”-CustomDnsServer” har lagts till för att kunder ska kunna ange att deras DNS-servrar ska konfigureras på P2SVpnGateway, som kan användas av punkt-till-plats-klienter.</span><span class="sxs-lookup"><span data-stu-id="f1219-368">Updated Update-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
* <span data-ttu-id="f1219-369">”Update-AzVpnGateway” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="f1219-369">Updated 'Update-AzVpnGateway'</span></span>
    - <span data-ttu-id="f1219-370">Den valfria parametern ”-BgpPeeringAddress” har lagts till för att kunder ska kunna ange sina anpassade BGP:er som ska konfigurerar på VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="f1219-370">Added optional parameter '-BgpPeeringAddress' for customers to specify their custom bgps to set on VpnGateway.</span></span>
* <span data-ttu-id="f1219-371">Ny cmdlet har lagts till för att stödja återställning av en VirtualHub-resurs routningsstatus:</span><span class="sxs-lookup"><span data-stu-id="f1219-371">Added new cmdlet to support resetting the routing state of a VirtualHub resource:</span></span>
    - <span data-ttu-id="f1219-372">”Reset-AzHubRouter”</span><span class="sxs-lookup"><span data-stu-id="f1219-372">'Reset-AzHubRouter'</span></span>
* <span data-ttu-id="f1219-373">Nedanstående saker har uppdaterats baserat på den senaste Swagger-ändringen för brandväggspolicyn</span><span class="sxs-lookup"><span data-stu-id="f1219-373">Updated below things based on recent swagger change for Firewall Policy</span></span>
    - <span data-ttu-id="f1219-374">Namn ändras för RuleGroup, RuleCollectionGroup och RuleType</span><span class="sxs-lookup"><span data-stu-id="f1219-374">Changes names for RuleGroup, RuleCollectionGroup and RuleType</span></span>
    - <span data-ttu-id="f1219-375">Stöd har lagts till för NAT-regelsamlingar för brandväggsprincip så att flera NAT-regelsamlingar stöds</span><span class="sxs-lookup"><span data-stu-id="f1219-375">Added support for Firewall Policy NAT Rule Collections to support multiple NAT Rule Collection</span></span>
* <span data-ttu-id="f1219-376">[Icke-bakåtkompatibel ändring] Den obligatoriska parametern ”SourceIpGroup” har lagts till för ”New-AzFirewallPolicyApplicationRule” och ”New-AzFirewallPolicyNetworkRule”.</span><span class="sxs-lookup"><span data-stu-id="f1219-376">[Breaking Change] Added mandatory parameter 'SourceIpGroup' for 'New-AzFirewallPolicyApplicationRule' and 'New-AzFirewallPolicyNetworkRule'.</span></span>
* <span data-ttu-id="f1219-377">[Icke-bakåtkompatibel ändring] ”New-AzFirewallPolicyApplicationRule” har åtgärdats, parametern ”SourceAddress” är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="f1219-377">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="f1219-378">[Icke-bakåtkompatibel ändring] ”New-AzFirewallPolicyApplicationRule” har åtgärdats, parametern ”SourceAddress” är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="f1219-378">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="f1219-379">[Icke-bakåtkompatibel ändring] Obligatoriska parametrar har tagits bort: ”TranslatedAddress”, ”TranslatedPort” för ”New-AzFirewallPolicyNatRuleCollection”.</span><span class="sxs-lookup"><span data-stu-id="f1219-379">[Breaking Change] Removed mandatory parameters: 'TranslatedAddress', 'TranslatedPort' for 'New-AzFirewallPolicyNatRuleCollection'.</span></span>
* <span data-ttu-id="f1219-380">Nya cmdletar har lagts till för att stödja PrivateLink på Application Gateway</span><span class="sxs-lookup"><span data-stu-id="f1219-380">Added new cmdlets to support PrivateLink On Application Gateway</span></span>
    - <span data-ttu-id="f1219-381">”New-AzApplicationGatewayPrivateLinkConfiguration”</span><span class="sxs-lookup"><span data-stu-id="f1219-381">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="f1219-382">”Get-AzApplicationGatewayPrivateLinkConfiguration”</span><span class="sxs-lookup"><span data-stu-id="f1219-382">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="f1219-383">”New-AzApplicationGatewayPrivateLinkConfiguration”</span><span class="sxs-lookup"><span data-stu-id="f1219-383">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="f1219-384">”Set-AzApplicationGatewayPrivateLinkConfiguration”</span><span class="sxs-lookup"><span data-stu-id="f1219-384">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="f1219-385">”Remove-AzApplicationGatewayPrivateLinkConfiguration”</span><span class="sxs-lookup"><span data-stu-id="f1219-385">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="f1219-386">”New-AzApplicationGatewayPrivateLinkIpConfiguration”</span><span class="sxs-lookup"><span data-stu-id="f1219-386">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span></span>
* <span data-ttu-id="f1219-387">Nya cmdletar har lagts till för VirtualHubs underordnade resurs HubRouteTables.</span><span class="sxs-lookup"><span data-stu-id="f1219-387">Added new cmdlets for HubRouteTables child resource of VirtualHub.</span></span>
    - <span data-ttu-id="f1219-388">”New-AzVHubRoute”</span><span class="sxs-lookup"><span data-stu-id="f1219-388">'New-AzVHubRoute'</span></span>
    - <span data-ttu-id="f1219-389">”New-AzVHubRouteTable”</span><span class="sxs-lookup"><span data-stu-id="f1219-389">'New-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="f1219-390">”Get-AzVHubRouteTable”</span><span class="sxs-lookup"><span data-stu-id="f1219-390">'Get-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="f1219-391">”Update-AzVHubRouteTable”</span><span class="sxs-lookup"><span data-stu-id="f1219-391">'Update-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="f1219-392">”Remove-AzVHubRouteTable”</span><span class="sxs-lookup"><span data-stu-id="f1219-392">'Remove-AzVHubRouteTable'</span></span>
* <span data-ttu-id="f1219-393">Befintliga cmdletar har uppdaterats för att stödja valfri RoutingConfiguration-indataparameter för anpassad routning i VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="f1219-393">Updated existing cmdlets to support optional RoutingConfiguration input parameter for custom routing in VirtualWan.</span></span>
    - <span data-ttu-id="f1219-394">”New-AzExpressRouteConnection”</span><span class="sxs-lookup"><span data-stu-id="f1219-394">'New-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="f1219-395">”Set-AzExpressRouteConnection”</span><span class="sxs-lookup"><span data-stu-id="f1219-395">'Set-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="f1219-396">”New-AzVirtualHubVnetConnection”</span><span class="sxs-lookup"><span data-stu-id="f1219-396">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="f1219-397">”Update-AzVirtualHubVnetConnection”</span><span class="sxs-lookup"><span data-stu-id="f1219-397">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="f1219-398">”New-AzVpnConnection”</span><span class="sxs-lookup"><span data-stu-id="f1219-398">'New-AzVpnConnection'</span></span>
    - <span data-ttu-id="f1219-399">”Update-AzVpnConnection”</span><span class="sxs-lookup"><span data-stu-id="f1219-399">'Update-AzVpnConnection'</span></span>
    - <span data-ttu-id="f1219-400">”New-AzP2sVpnGateway”</span><span class="sxs-lookup"><span data-stu-id="f1219-400">'New-AzP2sVpnGateway'</span></span>
    - <span data-ttu-id="f1219-401">”Update-AzP2sVpnGateway”</span><span class="sxs-lookup"><span data-stu-id="f1219-401">'Update-AzP2sVpnGateway'</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f1219-402">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f1219-402">Az.OperationalInsights</span></span>
* <span data-ttu-id="f1219-403">Fast fel PSWorkspace implementerar inte IOperationalInsightsWorkspace [#12135]</span><span class="sxs-lookup"><span data-stu-id="f1219-403">Fixed bug PSWorkspace doesn't implement IOperationalInsightsWorkspace [#12135]</span></span>
* <span data-ttu-id="f1219-404">”pergb2018” har lagts till i uppsättningen med giltiga värden för parametern ”Sku” i ”Set-AzOperationalInsightsWorkspace”</span><span class="sxs-lookup"><span data-stu-id="f1219-404">Added 'pergb2018' to valid value set of parameter 'Sku' in 'Set-AzOperationalInsightsWorkspace'</span></span> 
* <span data-ttu-id="f1219-405">Alias ”FunctionParameters” lades till för parametern ”FunctionParameter” till</span><span class="sxs-lookup"><span data-stu-id="f1219-405">Added alias 'FunctionParameters' for parameter 'FunctionParameter' to</span></span>
    - <span data-ttu-id="f1219-406">”New-AzOperationalInsightsSavedSearch”</span><span class="sxs-lookup"><span data-stu-id="f1219-406">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="f1219-407">”Set-AzOperationalInsightsSavedSearch”</span><span class="sxs-lookup"><span data-stu-id="f1219-407">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f1219-408">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f1219-408">Az.RecoveryServices</span></span>
* <span data-ttu-id="f1219-409">Azure Backup har fått stöd för att hämta MAB-objekt.</span><span class="sxs-lookup"><span data-stu-id="f1219-409">Azure Backup added support for fetching MAB items.</span></span>
* <span data-ttu-id="f1219-410">Azure Site Recovery stöder disktypen ”StandardSSD_LRS”</span><span class="sxs-lookup"><span data-stu-id="f1219-410">Azure Site Recovery supports disk type 'StandardSSD_LRS'</span></span>

#### <a name="azresources"></a><span data-ttu-id="f1219-411">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f1219-411">Az.Resources</span></span>
* <span data-ttu-id="f1219-412">”UsageLocation”, ”GivenName”, ”Surname”, ”AccountEnabled”, ”MailNickname”, ”Mail” på ”PSADUser” lades till [#10526] [#10497]</span><span class="sxs-lookup"><span data-stu-id="f1219-412">Added 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' on 'PSADUser' [#10526] [#10497]</span></span>
* <span data-ttu-id="f1219-413">Problem med att ”-Mail” inte fungerar på ”Get-AzADUser” har åtgärdats [#11981]</span><span class="sxs-lookup"><span data-stu-id="f1219-413">Fixed issue that '-Mail' doesn't work on 'Get-AzADUser' [#11981]</span></span>
* <span data-ttu-id="f1219-414">Parametern ”-ExcludeChangeType” har lagts till i ”Get-AzDeploymentWhatIfResult” och ”Get-AzResourceGroupDeploymentWhatIfResult”</span><span class="sxs-lookup"><span data-stu-id="f1219-414">Added '-ExcludeChangeType' parameter to 'Get-AzDeploymentWhatIfResult' and 'Get-AzResourceGroupDeploymentWhatIfResult'</span></span>
* <span data-ttu-id="f1219-415">Parametern ”-WhatIfExcludeChangeType” har lagts till i ”New-AzDeployment” och ”New-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="f1219-415">Added '-WhatIfExcludeChangeType' parameter to 'New-AzDeployment' and 'New-AzResourceGroupDeployment'</span></span>
* <span data-ttu-id="f1219-416">Cmdletar för ”Test-Az\*Deployment” har uppdaterats för att visa bättre felmeddelanden</span><span class="sxs-lookup"><span data-stu-id="f1219-416">Updated 'Test-Az\*Deployment' cmdlets to show better error messages</span></span>
* <span data-ttu-id="f1219-417">Hjälpmeddelandet för parametern ”-Name” i distributionsskapande och What If-cmdletar</span><span class="sxs-lookup"><span data-stu-id="f1219-417">Fixed help message for '-Name' parameter of deployment create and What-If cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="f1219-418">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f1219-418">Az.Sql</span></span>
* <span data-ttu-id="f1219-419">Stöd för tjänsthuvudnamn har lagts till för administratörs-cmdlet för SQL Server Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="f1219-419">Added support for service principal for Set SQL Server Azure Active Directory Admin cmdlet</span></span>
* <span data-ttu-id="f1219-420">Synkroniseringsproblem i Data Classification-cmdletar har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="f1219-420">Fixed sync issue in Data Classification cmdlets.</span></span>
* <span data-ttu-id="f1219-421">Stöd för att söka efter användare via e-postadress på ”Set-AzSqlServerActiveDirectoryAdministrator” [#12192]</span><span class="sxs-lookup"><span data-stu-id="f1219-421">Supported searching user by mail on 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f1219-422">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f1219-422">Az.Storage</span></span>
* <span data-ttu-id="f1219-423">Skapa lagringskonto med RequireInfrastructureEncryption stöds</span><span class="sxs-lookup"><span data-stu-id="f1219-423">Supported create Storage account with RequireInfrastructureEncryption</span></span>
    -  <span data-ttu-id="f1219-424">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="f1219-424">'New-AzStorageAccount'</span></span>
* <span data-ttu-id="f1219-425">Logiken för inläsning av Azure.Core flyttades till Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f1219-425">Moved the logic of loading Azure.Core to Az.Accounts</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f1219-426">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f1219-426">Az.Websites</span></span>
* <span data-ttu-id="f1219-427">Skydd för att ta bort skapad webapp om återställningen misslyckades har lagts till i ”Restore-AzDeletedWebApp”</span><span class="sxs-lookup"><span data-stu-id="f1219-427">Added safeguard to delete created webapp if restore failed in 'Restore-AzDeletedWebApp'</span></span>
* <span data-ttu-id="f1219-428">”SourceWebApp.Location” har lagts till för ”New-AzWebApp” och ”New-AzWebAppSlot”</span><span class="sxs-lookup"><span data-stu-id="f1219-428">Added 'SourceWebApp.Location' for 'New-AzWebApp' and 'New-AzWebAppSlot'</span></span>
* <span data-ttu-id="f1219-429">Fel som förhindrade ändring av containerinställningar i ”Set-AzWebApp” och ”Set-AzWebAppSlot” har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="f1219-429">Fixed bug that prevented changing Container settings in 'Set-AzWebApp' and 'Set-AzWebAppSlot'</span></span>
* <span data-ttu-id="f1219-430">Ett fel för att hämta SiteConfig när -Name inte anges för Get-AzWebApp har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="f1219-430">Fixed bug to get SiteConfig when -Name is not given for Get-AzWebApp</span></span>
* <span data-ttu-id="f1219-431">Stöd har lagts till för att skapa ASP för Linux-appar</span><span class="sxs-lookup"><span data-stu-id="f1219-431">Added a support to create ASP for Linux Apps</span></span>
* <span data-ttu-id="f1219-432">Undantag har lagts till för kloning över resursgrupper</span><span class="sxs-lookup"><span data-stu-id="f1219-432">Added exceptions for clone across resource groups</span></span>

## <a name="420---june-2020"></a><span data-ttu-id="f1219-433">4.2.0 – juni 2020</span><span class="sxs-lookup"><span data-stu-id="f1219-433">4.2.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f1219-434">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f1219-434">Az.Accounts</span></span>
* <span data-ttu-id="f1219-435">Åtgärdade ett problem som kan få Az att hoppa över loggar i Azure Automation- eller PowerShell-jobb [#11492]</span><span class="sxs-lookup"><span data-stu-id="f1219-435">Fixed an issue that may cause Az to skip logs in Azure Automation or PowerShell jobs [#11492]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="f1219-436">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f1219-436">Az.AnalysisServices</span></span>
* <span data-ttu-id="f1219-437">Uppdaterad sammansättningsversion för dataplan-cmdletar</span><span class="sxs-lookup"><span data-stu-id="f1219-437">Updated assembly version of data plane cmdlets</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="f1219-438">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f1219-438">Az.ApiManagement</span></span>
* <span data-ttu-id="f1219-439">Uppdaterad sammansättningsversion för cmdletar för tjänsthantering</span><span class="sxs-lookup"><span data-stu-id="f1219-439">Updated assembly version of service management cmdlets</span></span>

#### <a name="azbilling"></a><span data-ttu-id="f1219-440">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="f1219-440">Az.Billing</span></span>
* <span data-ttu-id="f1219-441">Uppdaterad sammansättningsversion för förbrukningscmdletar</span><span class="sxs-lookup"><span data-stu-id="f1219-441">Updated assembly version of consumption cmdlets</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f1219-442">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f1219-442">Az.CognitiveServices</span></span>
* <span data-ttu-id="f1219-443">Stöd för PrivateEndpoint- och PublicNetworkAccess-kontroll.</span><span class="sxs-lookup"><span data-stu-id="f1219-443">Support PrivateEndpoint and PublicNetworkAccess control.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="f1219-444">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f1219-444">Az.DataFactory</span></span>
* <span data-ttu-id="f1219-445">Uppdaterad sammansättningsversion för datafabrik V2-cmdletar</span><span class="sxs-lookup"><span data-stu-id="f1219-445">Updated assembly version of data factory V2 cmdlets</span></span>

#### <a name="azdatashare"></a><span data-ttu-id="f1219-446">Az.DataShare</span><span class="sxs-lookup"><span data-stu-id="f1219-446">Az.DataShare</span></span>
* <span data-ttu-id="f1219-447">Allmän tillgänglighet för modulen ”Az.DataShare”</span><span class="sxs-lookup"><span data-stu-id="f1219-447">General availability of ''Az.DataShare'' module</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="f1219-448">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="f1219-448">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="f1219-449">Allmän tillgänglighet för modulen ”Az.DesktopVirtualization”</span><span class="sxs-lookup"><span data-stu-id="f1219-449">General availability of ''Az.DesktopVirtualization'' module</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f1219-450">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f1219-450">Az.OperationalInsights</span></span>
* <span data-ttu-id="f1219-451">Uppgraderad SDK till 0.21.0</span><span class="sxs-lookup"><span data-stu-id="f1219-451">Upgraded SDK to 0.21.0</span></span>
* <span data-ttu-id="f1219-452">Lade till valfria parametrar till</span><span class="sxs-lookup"><span data-stu-id="f1219-452">Added optional parameters to</span></span> 
    - <span data-ttu-id="f1219-453">”New-AzOperationalInsightsSavedSearch”</span><span class="sxs-lookup"><span data-stu-id="f1219-453">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="f1219-454">”Set-AzOperationalInsightsSavedSearch”</span><span class="sxs-lookup"><span data-stu-id="f1219-454">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f1219-455">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f1219-455">Az.PolicyInsights</span></span>
* <span data-ttu-id="f1219-456">Korrigerade exempel 3 för ”Start-AzPolicyComplianceScan”</span><span class="sxs-lookup"><span data-stu-id="f1219-456">Corrected example 3 for 'Start-AzPolicyComplianceScan'</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="f1219-457">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="f1219-457">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="f1219-458">Uppdaterad sammansättningsversion för PowerBI-cmdletar</span><span class="sxs-lookup"><span data-stu-id="f1219-458">Updated assembly version of PowerBI cmdlets</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="f1219-459">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="f1219-459">Az.PrivateDns</span></span>
* <span data-ttu-id="f1219-460">Korrigerade formatering av utförlig utdatasträng för Remove-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="f1219-460">Corrected verbose output string formatting for Remove-AzPrivateDnsRecordSet</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f1219-461">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f1219-461">Az.RecoveryServices</span></span>
* <span data-ttu-id="f1219-462">Azure Site Recovery-stöd för att skapa en återställningsplan för replikering mellan zoner från xml-indata.</span><span class="sxs-lookup"><span data-stu-id="f1219-462">Azure Site Recovery support for creating recovery plan for zone to zone replication from xml input.</span></span>
* <span data-ttu-id="f1219-463">Uppdaterad sammansättningsversion för cmdletar för SiteRecovery och Backup</span><span class="sxs-lookup"><span data-stu-id="f1219-463">Updated assembly version of SiteRecovery and Backup cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="f1219-464">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f1219-464">Az.Resources</span></span>
* <span data-ttu-id="f1219-465">Lade till slutparameter för cmdletarna Get-AzDeploymentScriptLog och Save-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="f1219-465">Added Tail parameter to Get-AzDeploymentScriptLog and Save-AzDeploymentScriptLog cmdlets</span></span>
* <span data-ttu-id="f1219-466">Formaterad utdataegenskap så att den kan visas i cmdlet-utdata för Get-AzDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="f1219-466">Formatted Output property and show it on the Get-AzDeploymentScript cmdlet output</span></span>
* <span data-ttu-id="f1219-467">Bytte namn på parametern -DeploymentScriptInputObject till -DeploymentScriptObject</span><span class="sxs-lookup"><span data-stu-id="f1219-467">Renamed -DeploymentScriptInputObject parameter to -DeploymentScriptObject</span></span>
* <span data-ttu-id="f1219-468">Åtgärdade saknade fil/målnamn i cmdlet-meddelanden.</span><span class="sxs-lookup"><span data-stu-id="f1219-468">Fixed missing file/target name in cmdlet messages.</span></span>
* <span data-ttu-id="f1219-469">Uppdaterad sammansättningsversion för cmdletar för resurshanterare och taggar</span><span class="sxs-lookup"><span data-stu-id="f1219-469">Updated assembly version of resource manager and tags cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="f1219-470">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f1219-470">Az.Sql</span></span>
* <span data-ttu-id="f1219-471">Lade till UsePrivateLinkConnection till ”New-AzSqlSyncGroup”, ”Update-AzSqlSyncGroup”, ”New-AzSqlSyncMember” och ”Update-AzSqlSyncMember”</span><span class="sxs-lookup"><span data-stu-id="f1219-471">Added UsePrivateLinkConnection to 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="f1219-472">Lade till SyncMemberAzureDatabaseResourceId till ”New-AzSqlSyncMember” and ”Update-AzSqlSyncMember”</span><span class="sxs-lookup"><span data-stu-id="f1219-472">Added SyncMemberAzureDatabaseResourceId to 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="f1219-473">Lade till stöd för att söka efter gästanvändare för att ange administratörs-cmdlet för SQL Server Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="f1219-473">Added Guest user lookup support to Set SQL Server Azure Active Directory Admin cmdlet</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f1219-474">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f1219-474">Az.Storage</span></span>
* <span data-ttu-id="f1219-475">Uppdaterad sammansättningsversion för dataplan-cmdletar</span><span class="sxs-lookup"><span data-stu-id="f1219-475">Updated assembly version of data plane cmdlets</span></span>

## <a name="410---may-2020"></a><span data-ttu-id="f1219-476">4.1.0 – maj 2020</span><span class="sxs-lookup"><span data-stu-id="f1219-476">4.1.0 - May 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="f1219-477">Höjdpunkter sedan den senaste uppdateringen</span><span class="sxs-lookup"><span data-stu-id="f1219-477">Highlights since the last release</span></span>
* <span data-ttu-id="f1219-478">PowerShell-versioner som stöds: Windows PowerShell 5.1, PowerShell Core 6.2.4+ och PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="f1219-478">Supported PowerShell versions: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>
* <span data-ttu-id="f1219-479">Allmän tillgänglighet för Az.Functions</span><span class="sxs-lookup"><span data-stu-id="f1219-479">General availability of Az.Functions</span></span> 
* <span data-ttu-id="f1219-480">Nya stora uppdateringar har gjorts för Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources och Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f1219-480">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources, and Az.Storage have major release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f1219-481">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f1219-481">Az.Accounts</span></span>
* <span data-ttu-id="f1219-482">”Add-AzEnvironment” och ”Set-AzEnvironment” har uppdaterats med stöd för parametrarna ”AzureSynapseAnalyticsEndpointResourceId” och ”AzureSynapseAnalyticsEndpointSuffix”</span><span class="sxs-lookup"><span data-stu-id="f1219-482">Updated 'Add-AzEnvironment' and 'Set-AzEnvironment' to accept parameters 'AzureSynapseAnalyticsEndpointResourceId' and 'AzureSynapseAnalyticsEndpointSuffix'</span></span>
* <span data-ttu-id="f1219-483">Azure.Core-relaterade sammansättningar har lagts till i Az.Accounts; PowerShell-plattformar som stöds är Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span><span class="sxs-lookup"><span data-stu-id="f1219-483">Added Azure.Core related assemblies into Az.Accounts, supported PowerShell platforms include Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span></span>

#### <a name="azaks"></a><span data-ttu-id="f1219-484">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="f1219-484">Az.Aks</span></span>
* <span data-ttu-id="f1219-485">API-versionen har uppgraderats till 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="f1219-485">Upgraded API Version to 2019-10-01</span></span>
* <span data-ttu-id="f1219-486">Stöds för att skapa AKS med hjälp av Windows-container</span><span class="sxs-lookup"><span data-stu-id="f1219-486">Supported to create AKS using Windows container</span></span>
* <span data-ttu-id="f1219-487">Nya cmdletar är tillgängliga: ”New-AzAksNodePool”, ”Update-AzAksNodePool”, ”Remove-AzAksNodePool”,        ”Get-AzAksNodePool”, ”Install-AzAksKubectl”, ”Get-AzAksVersion”</span><span class="sxs-lookup"><span data-stu-id="f1219-487">Provided new cmdlets: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="f1219-488">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f1219-488">Az.ApiManagement</span></span>
* <span data-ttu-id="f1219-489">Parametrarna ”New-AzApiManagement” och ”Set-AzApiManagement”: [-AssignIdentity] har bytt namn till [-SystemAssignedIdentity]</span><span class="sxs-lookup"><span data-stu-id="f1219-489">'New-AzApiManagement' and 'Set-AzApiManagement': [-AssignIdentity] parameter renamed as [-SystemAssignedIdentity]</span></span>
* <span data-ttu-id="f1219-490">”New-AzApiManagement” och ”Set-AzApiManagement”: En ny parameter har lagts till: [-UserAssignedIdentity <String[]>]</span><span class="sxs-lookup"><span data-stu-id="f1219-490">'New-AzApiManagement' and 'Set-AzApiManagement': New parameter added: [-UserAssignedIdentity <String[]>]</span></span>
* <span data-ttu-id="f1219-491">”Get-AzApiManagementProperty” har bytt namn till ”Get-AzApiManagementNamedValue”.</span><span class="sxs-lookup"><span data-stu-id="f1219-491">'Get-AzApiManagementProperty': renamed as 'Get-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="f1219-492">PropertyId-parametern har bytt namn till NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="f1219-492">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="f1219-493">”New-AzApiManagementProperty” har bytt namn till ”New-AzApiManagementNamedValue”.</span><span class="sxs-lookup"><span data-stu-id="f1219-493">'New-AzApiManagementProperty': renamed as 'New-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="f1219-494">PropertyId-parametern har bytt namn till NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="f1219-494">PropertyId parameter renamed as NamedValueId.</span></span> 
* <span data-ttu-id="f1219-495">”Set-AzApiManagementProperty” har bytt namn till ”Set-AzApiManagementNamedValue”.</span><span class="sxs-lookup"><span data-stu-id="f1219-495">'Set-AzApiManagementProperty': renamed as 'Set-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="f1219-496">PropertyId-parametern har bytt namn till NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="f1219-496">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="f1219-497">”Remove-AzApiManagementProperty” har bytt namn till ”Remove-AzApiManagementNamedValue”.</span><span class="sxs-lookup"><span data-stu-id="f1219-497">'Remove-AzApiManagementProperty': renamed as 'Remove-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="f1219-498">PropertyId-parametern har bytt namn till NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="f1219-498">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="f1219-499">Den nya cmdleten Get-AzApiManagementAuthorizationServerClientSecret gör att ”Get-AzApiManagementAuthorizationServer” inte längre returnerar klienthemligheter.</span><span class="sxs-lookup"><span data-stu-id="f1219-499">Added new 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet and 'Get-AzApiManagementAuthorizationServer' will not return client secret anymore.</span></span>
* <span data-ttu-id="f1219-500">Den nya cmdleten ”Get-AzApiManagementNamedValueSecretValue” gör att ”Get-AzApiManagementNamedValue” inte returnerar värdet för en hemlighet.</span><span class="sxs-lookup"><span data-stu-id="f1219-500">Added new 'Get-AzApiManagementNamedValueSecretValue' cmdlet and 'Get-AzApiManagementNamedValue' will not return secret value.</span></span>
* <span data-ttu-id="f1219-501">Den nya cmdleten ”Get-AzApiManagementOpenIdConnectProviderClientSecret” gör att ”Get-AzApiManagementOpenIdConnectProvider” inte längre returnerar klienthemligheter.</span><span class="sxs-lookup"><span data-stu-id="f1219-501">Added new 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet and 'Get-AzApiManagementOpenIdConnectProvider' will not return client secret anymore.</span></span>
* <span data-ttu-id="f1219-502">Den nya cmdleten ”Get-AzApiManagementSubscriptionKey” gör att ”Get-AzApiManagementSubscription” inte längre returnerar prenumerationsnycklar.</span><span class="sxs-lookup"><span data-stu-id="f1219-502">Added new 'Get-AzApiManagementSubscriptionKey' cmdlet and 'Get-AzApiManagementSubscription' will not return subscription keys anymore.</span></span>
* <span data-ttu-id="f1219-503">Den nya cmdleten ”Get-AzApiManagementTenantAccessSecret” gör att ”Get-AzApiManagementTenantAccess” inte längre returnerar nycklar.</span><span class="sxs-lookup"><span data-stu-id="f1219-503">Added new 'Get-AzApiManagementTenantAccessSecret' cmdlet and 'Get-AzApiManagementTenantAccess' will not return keys anymore.</span></span>
* <span data-ttu-id="f1219-504">Den nya cmdleten ”Get-AzApiManagementTenantGitAccessSecret” gör att ”Get-AzApiManagementTenantGitAccess” inte längre returnerar nycklar.</span><span class="sxs-lookup"><span data-stu-id="f1219-504">Added new 'Get-AzApiManagementTenantGitAccessSecret' cmdlet and 'Get-AzApiManagementTenantGitAccess' will not return keys anymore.</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="f1219-505">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="f1219-505">Az.ApplicationInsights</span></span>
* <span data-ttu-id="f1219-506">Tillagda parametrar: ”RetentionInDays” ”PublicNetworkAccessForIngestion” ”PublicNetworkAccessForQuery” för ”New-AzApplicationInsights”</span><span class="sxs-lookup"><span data-stu-id="f1219-506">Added Parameters: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span></span>
* <span data-ttu-id="f1219-507">Cmdleten ”Update-AzApplicationInsights” har skapats</span><span class="sxs-lookup"><span data-stu-id="f1219-507">Created cmdlet 'Update-AzApplicationInsights'</span></span>
* <span data-ttu-id="f1219-508">Cmdletar har skapats för länkat lagringskonto</span><span class="sxs-lookup"><span data-stu-id="f1219-508">Created cmdlets for Linked Storage Account</span></span>

#### <a name="azbatch"></a><span data-ttu-id="f1219-509">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="f1219-509">Az.Batch</span></span>
* <span data-ttu-id="f1219-510">Az.Batch har uppdaterats att använda ”Microsoft.Azure.Batch” SDK version 13.0.0 och ”Microsoft.Azure.Management.Batch” SDK version 9.0.0.</span><span class="sxs-lookup"><span data-stu-id="f1219-510">Updated Az.Batch to use 'Microsoft.Azure.Batch' SDK version 13.0.0 and 'Microsoft.Azure.Management.Batch' SDK version 9.0.0.</span></span>
* <span data-ttu-id="f1219-511">Nu kan du välja vilken typ av certifikat du lägger till genom att använda den nya parametern ”-CertificateKind” med ”New-AzBatchCertificate”.</span><span class="sxs-lookup"><span data-stu-id="f1219-511">Added the ability to select the kind of certificate being added using the new '-CertificateKind' parameter to 'New-AzBatchCertificate'.</span></span>
* <span data-ttu-id="f1219-512">Egenskapen ”ApplicationPackages” har tagits bort från ”PSApplication”, som tidigare alltid var ''.</span><span class="sxs-lookup"><span data-stu-id="f1219-512">Removed 'ApplicationPackages' property from 'PSApplication' which was previously always ''.</span></span>
  - <span data-ttu-id="f1219-513">Specifika paket i ett program kan nu hämtas med hjälp av ”Get-AzBatchApplicationPackage”.</span><span class="sxs-lookup"><span data-stu-id="f1219-513">The specific packages inside of an application now can be retrieved using 'Get-AzBatchApplicationPackage'.</span></span> <span data-ttu-id="f1219-514">Ett exempel: ”Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication”.</span><span class="sxs-lookup"><span data-stu-id="f1219-514">For example: 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span></span>
* <span data-ttu-id="f1219-515">Nu när du skapar en pool med hjälp av ”New-AzBatchPool” kan egenskapen ”VirtualMachineImageId” för ”PSImageReference” endast referera till en Shared Image Gallery-avbildning.</span><span class="sxs-lookup"><span data-stu-id="f1219-515">When creating a pool using 'New-AzBatchPool', the 'VirtualMachineImageId' property of 'PSImageReference' can now only refer to a Shared Image Gallery image.</span></span>
* <span data-ttu-id="f1219-516">När du skapar en pool med hjälp av ”New-AzBatchPool” kan poolen etableras utan en offentlig IP-adress med hjälp av den nya egenskapen ”PublicIPAddressConfiguration” för ”PSNetworkConfiguration”.</span><span class="sxs-lookup"><span data-stu-id="f1219-516">When creating a pool using 'New-AzBatchPool', the pool can be provisioned without a public IP using the new 'PublicIPAddressConfiguration' property of 'PSNetworkConfiguration'.</span></span>
  - <span data-ttu-id="f1219-517">Egenskapen ”PublicIPs” för ”PSNetworkConfiguration” har också flyttats till ”PSPublicIPAddressConfiguration”.</span><span class="sxs-lookup"><span data-stu-id="f1219-517">The 'PublicIPs' property of 'PSNetworkConfiguration' has moved in to 'PSPublicIPAddressConfiguration' as well.</span></span> <span data-ttu-id="f1219-518">Den här egenskapen kan bara anges om ”IPAddressProvisioningType” är ”UserManaged”.</span><span class="sxs-lookup"><span data-stu-id="f1219-518">This property can only be specified if 'IPAddressProvisioningType' is 'UserManaged'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f1219-519">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f1219-519">Az.Compute</span></span>
* <span data-ttu-id="f1219-520">Parametern HostId har lagts till för cmdleten ”Update-AzVM”t</span><span class="sxs-lookup"><span data-stu-id="f1219-520">Added HostId parameter to 'Update-AzVM' cmdlet</span></span>
* <span data-ttu-id="f1219-521">Hjälpdokumenten har uppdaterats för cmdletarna ”New-AzVMConfig”, ”New-AzVmssConfig”, ”Update-AzVmss”, ”Set-AzVMOperatingSystem” och ”Set-AzVmssOsProfile”.</span><span class="sxs-lookup"><span data-stu-id="f1219-521">Updated Help documents for 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' and 'Set-AzVmssOsProfile' cmdlets.</span></span>
* <span data-ttu-id="f1219-522">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="f1219-522">Breaking changes</span></span>
    - <span data-ttu-id="f1219-523">Parametern FilterExpression tas bort från cmdleten ”Get-AzVMImage”.</span><span class="sxs-lookup"><span data-stu-id="f1219-523">FilterExpression parameter is removed from 'Get-AzVMImage' cmdlet.</span></span>
    - <span data-ttu-id="f1219-524">Parametern AssignIdentity tas bort från cmdletarna ”New-AzVmssConfig”, ”New-AzVMConfig” och ”Update-AzVM”.</span><span class="sxs-lookup"><span data-stu-id="f1219-524">AssignIdentity parameter is removed from 'New-AzVmssConfig', 'New-AzVMConfig' and 'Update-AzVM' cmdlets.</span></span>
    - <span data-ttu-id="f1219-525">AutomaticRepairMaxInstanceRepairsPercent tas bort från cmdletarna ”New-AzVmssConfig” och ”Update-AzVmss”.</span><span class="sxs-lookup"><span data-stu-id="f1219-525">AutomaticRepairMaxInstanceRepairsPercent is removed from 'New-AzVmssConfig' and 'Update-AzVmss' cmdlets.</span></span>
    - <span data-ttu-id="f1219-526">Egenskaperna AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus och VirtualMachineScaleSetsColocationStatus tas bort från ProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="f1219-526">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus and VirtualMachineScaleSetsColocationStatus properties are removed from ProximityPlacementGroup.</span></span>
    - <span data-ttu-id="f1219-527">Egenskapen MaxInstanceRepairsPercent tas bort från AutomaticRepairsPolicy.</span><span class="sxs-lookup"><span data-stu-id="f1219-527">MaxInstanceRepairsPercent property is removed from AutomaticRepairsPolicy.</span></span>
    - <span data-ttu-id="f1219-528">Typerna AvailabilitySets, VirtualMachines och VirtualMachineScaleSets ändras från IList<SubResource> till IList<SubResourceWithColocationStatus>.</span><span class="sxs-lookup"><span data-stu-id="f1219-528">The types of AvailabilitySets, VirtualMachines and VirtualMachineScaleSets are changed from IList<SubResource> to IList<SubResourceWithColocationStatus>.</span></span>
* <span data-ttu-id="f1219-529">Beskrivningen för cmdleten ”Get-AzVM” har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="f1219-529">Description for 'Get-AzVM' cmdlet has been updated to better describe it.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="f1219-530">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f1219-530">Az.DataFactory</span></span>
* <span data-ttu-id="f1219-531">CRUD-stöd för egenskaper för dataflödeskörning  i hanterad IR.</span><span class="sxs-lookup"><span data-stu-id="f1219-531">Supported CRUD of data flow runtime properties in Managed IR.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="f1219-532">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f1219-532">Az.FrontDoor</span></span>
* <span data-ttu-id="f1219-533">Nya cmdletar har lagts till för att skapa, uppdatera, hämta och ta bort (CRUD) Front Door-regelmotorobjekt</span><span class="sxs-lookup"><span data-stu-id="f1219-533">Added new cmdlets for creation, update, retreival, and deletion of Front Door Rules Engine object</span></span>
* <span data-ttu-id="f1219-534">Hjälp-cmdletar har lagts till för konstruktion av Front Door-regelmotorobjekt</span><span class="sxs-lookup"><span data-stu-id="f1219-534">Added helper cmdlets for construction of Front Door Rules Engine object</span></span>
* <span data-ttu-id="f1219-535">Regelmotorreferens har lagts till för Front Door-hanteringsregelobjekt.</span><span class="sxs-lookup"><span data-stu-id="f1219-535">Added Rules Engine reference to Front Door Routing Rule object.</span></span>
* <span data-ttu-id="f1219-536">Parametrar för Private Link har lagts till för Front Door-serverdelsobjekt</span><span class="sxs-lookup"><span data-stu-id="f1219-536">Added Private Link parameters to Front Door Backend object</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="f1219-537">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="f1219-537">Az.Functions</span></span>
* <span data-ttu-id="f1219-538">Allmän tillgänglighet för ”Az.Functions”-modulen</span><span class="sxs-lookup"><span data-stu-id="f1219-538">General availability of ''Az.Functions'' module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="f1219-539">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f1219-539">Az.HDInsight</span></span>
* <span data-ttu-id="f1219-540">Stöd för diskkryptering med kundhanterad nyckel.</span><span class="sxs-lookup"><span data-stu-id="f1219-540">Supported Customer-managed key disk encryption.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="f1219-541">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="f1219-541">Az.HealthcareApis</span></span>
* <span data-ttu-id="f1219-542">Åtkomstprinciper använder inte längre det aktiva huvudkontot som standard</span><span class="sxs-lookup"><span data-stu-id="f1219-542">Access policies are no longer defaulted to the current principal</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f1219-543">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f1219-543">Az.IotHub</span></span>
* <span data-ttu-id="f1219-544">En cmdlet har lagts till som anropar en fråga i en IoT-hubb för att hämta information med ett SQL-liknande språk.</span><span class="sxs-lookup"><span data-stu-id="f1219-544">Added cmdlet to invoke a query in an IoT hub to retrieve information using a SQL-like language.</span></span>
* <span data-ttu-id="f1219-545">Problemet som gjorde att ”Add-AzIotHubDevice” inte skapade en Edge-aktiverad enhet utan underordnade enheter har åtgärdats [#11597]</span><span class="sxs-lookup"><span data-stu-id="f1219-545">Fix issue that 'Add-AzIotHubDevice' fails to create Edge Enabled Device without child devices [#11597]</span></span>
* <span data-ttu-id="f1219-546">En cmdlet har lagts till för att generera SAS-token för en Iot-hubb, enhet eller modul.</span><span class="sxs-lookup"><span data-stu-id="f1219-546">Added cmdlet to generate SAS token for Iot Hub, device or module.</span></span>
* <span data-ttu-id="f1219-547">En cmdlet har lagts till för att anropa en måttfråga om konfiguration.</span><span class="sxs-lookup"><span data-stu-id="f1219-547">Added cmdlet to invoke configuration metrics query.</span></span>
* <span data-ttu-id="f1219-548">Hantera automatisk distribution av IoT Edge i stor skala.</span><span class="sxs-lookup"><span data-stu-id="f1219-548">Manage IoT Edge automatic deployment at scale.</span></span> <span data-ttu-id="f1219-549">Nya cmdlet:ar är:</span><span class="sxs-lookup"><span data-stu-id="f1219-549">New cmdlets are:</span></span>
    - <span data-ttu-id="f1219-550">”Add-AzIotHubDeployment”</span><span class="sxs-lookup"><span data-stu-id="f1219-550">'Add-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="f1219-551">”Get-AzIotHubDeployment”</span><span class="sxs-lookup"><span data-stu-id="f1219-551">'Get-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="f1219-552">”Remove-AzIotHubDeployment”</span><span class="sxs-lookup"><span data-stu-id="f1219-552">'Remove-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="f1219-553">”Set-AzIotHubDeployment”</span><span class="sxs-lookup"><span data-stu-id="f1219-553">'Set-AzIotHubDeployment'</span></span>
* <span data-ttu-id="f1219-554">En cmdlet har lagts till för att anropa en måttfråga om IoT Edge-distribution.</span><span class="sxs-lookup"><span data-stu-id="f1219-554">Added cmdlet to invoke an IoT Edge deployment metrics query.</span></span>
* <span data-ttu-id="f1219-555">En cmdlet har lagts till för att tillämpa konfigurationsinnehåll på den angivna gränsenheten.</span><span class="sxs-lookup"><span data-stu-id="f1219-555">Added cmdlet to apply the configuration content to the specified edge device.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f1219-556">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f1219-556">Az.KeyVault</span></span>
* <span data-ttu-id="f1219-557">Två alias har tagits bort: ”New-AzKeyVaultCertificateAdministratorDetails” och ”New-AzKeyVaultCertificateOrganizationDetails”</span><span class="sxs-lookup"><span data-stu-id="f1219-557">Removed two aliases: 'New-AzKeyVaultCertificateAdministratorDetails' and 'New-AzKeyVaultCertificateOrganizationDetails'</span></span>
* <span data-ttu-id="f1219-558">Nu är mjuk borttagning aktiverat som standard när ett nyckelvalv skapas</span><span class="sxs-lookup"><span data-stu-id="f1219-558">Enabled soft delete by default when creating a key vault</span></span>
* <span data-ttu-id="f1219-559">Nätverksregler kan ställas in för att styra åtkomsten från särskilda nätverksplatser när du skapar ett nyckelvalv</span><span class="sxs-lookup"><span data-stu-id="f1219-559">Network rules can be set to govern the accessibility from specific network locations when creating a key vault</span></span>
* <span data-ttu-id="f1219-560">Stöd för BYOK (Bring Your Own Key) har lagts till</span><span class="sxs-lookup"><span data-stu-id="f1219-560">Added support to bring your own key (BYOK)</span></span>
    - <span data-ttu-id="f1219-561">”Add-AzKeyVaultKey” stöder generering av en KeyExchange-nyckel</span><span class="sxs-lookup"><span data-stu-id="f1219-561">'Add-AzKeyVaultKey' supports generating a key exchange key</span></span>
    - <span data-ttu-id="f1219-562">”Get-AzKeyVaultKey” stöder nedladdning av en offentlig nyckel i PEM-format</span><span class="sxs-lookup"><span data-stu-id="f1219-562">'Get-AzKeyVaultKey' supports downloading a public key in PEM format</span></span>
* <span data-ttu-id="f1219-563">”KeyOps”-delen av hjälpdokumentet för ”Add-AzKeyVaultKey” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="f1219-563">Updated the 'KeyOps' part of the help document of 'Add-AzKeyVaultKey'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f1219-564">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f1219-564">Az.Monitor</span></span>
* <span data-ttu-id="f1219-565">Bugg för ”Set-AzDiagnosticSettings” har åtgärdats; kvarhållningsprincipen tillämpas inte på alla kategorier [#11589]</span><span class="sxs-lookup"><span data-stu-id="f1219-565">Fixed bug for 'Set-AzDiagnosticSettings', retention policy won't apply to all categories [#11589]</span></span>
* <span data-ttu-id="f1219-566">Stöd för WebTest-tillgänglighetskriterier för måttavisering V2</span><span class="sxs-lookup"><span data-stu-id="f1219-566">Supported WebTest availability criteria for metric alert V2</span></span>
    - <span data-ttu-id="f1219-567">”New-AzMetricAlertRuleV2Criteria”: ett alternativ för att skapa tillgänglighetskriterier för webbtest har lagts till</span><span class="sxs-lookup"><span data-stu-id="f1219-567">'New-AzMetricAlertRuleV2Criteria': an option to create webtest availability criteria was added</span></span>
    - <span data-ttu-id="f1219-568">”Add-AzMetricAlertRuleV2”: stöd för de nya tillgänglighetskriterierna för webbtest</span><span class="sxs-lookup"><span data-stu-id="f1219-568">'Add-AzMetricAlertRuleV2': supports the new webtest availability criteria</span></span>
* <span data-ttu-id="f1219-569">Redundant definition har tagits bort för RetentionPolicy i PSLogProfile [#7608]</span><span class="sxs-lookup"><span data-stu-id="f1219-569">Removed redundant definition for RetentionPolicy in PSLogProfile [#7608]</span></span>
* <span data-ttu-id="f1219-570">Redundanta egenskaper som definierats i PSEventData har tagits bort [#11353]</span><span class="sxs-lookup"><span data-stu-id="f1219-570">Removed redundant properties difined in PSEventData [#11353]</span></span>
* <span data-ttu-id="f1219-571">”Get-AzLog” har bytt namn till ”Get-AzActivityLog”</span><span class="sxs-lookup"><span data-stu-id="f1219-571">Renamed 'Get-AzLog' to 'Get-AzActivityLog'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f1219-572">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f1219-572">Az.Network</span></span>
* <span data-ttu-id="f1219-573">Attribut för icke-bakåtkompatibel ändring har lagts till för att meddela att standardbeteendet för zoner kommer att ändras</span><span class="sxs-lookup"><span data-stu-id="f1219-573">Added breaking change attribute to notify that Zone default behaviour will be changed</span></span>
    - <span data-ttu-id="f1219-574">”New-AzPublicIpAddress”</span><span class="sxs-lookup"><span data-stu-id="f1219-574">'New-AzPublicIpAddress'</span></span>
    - <span data-ttu-id="f1219-575">”New-AzPublicIpPrefix”</span><span class="sxs-lookup"><span data-stu-id="f1219-575">'New-AzPublicIpPrefix'</span></span>
    - <span data-ttu-id="f1219-576">”New-AzLoadBalancerFrontendIpConfig”</span><span class="sxs-lookup"><span data-stu-id="f1219-576">'New-AzLoadBalancerFrontendIpConfig'</span></span>
* <span data-ttu-id="f1219-577">Stöd har lagts till för en ny resurs på den översta nivån, SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="f1219-577">Added support for a new top level resource SecurityPartnerProvider</span></span>
    - <span data-ttu-id="f1219-578">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="f1219-578">New cmdlets added:</span></span>
        - <span data-ttu-id="f1219-579">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="f1219-579">New-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="f1219-580">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="f1219-580">Remove-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="f1219-581">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="f1219-581">Get-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="f1219-582">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="f1219-582">Set-AzSecurityPartnerProvider</span></span>
* <span data-ttu-id="f1219-583">”RequiredZoneNames” har lagts till för ”PSPrivateLinkResource” och ”GroupId” för ”PSPrivateEndpointConnection”</span><span class="sxs-lookup"><span data-stu-id="f1219-583">Added 'RequiredZoneNames' on 'PSPrivateLinkResource' and 'GroupId' on 'PSPrivateEndpointConnection'</span></span>
* <span data-ttu-id="f1219-584">Fel parametertyp för SuccessThresholdRoundTripTimeMs-parametern för New-AzNetworkWatcherConnectionMonitorTestConfigurationObject har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="f1219-584">Fixed incorrect type of SuccessThresholdRoundTripTimeMs parameter for New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>
* <span data-ttu-id="f1219-585">VirtualWan-cmdletar har uppdaterats för att ange AllowVnetToVnetTraffic-argumentets standardvärde till True.</span><span class="sxs-lookup"><span data-stu-id="f1219-585">Updated VirtualWan cmdlets to set default value of AllowVnetToVnetTraffic argument to True.</span></span>
    - <span data-ttu-id="f1219-586">”New-AzVirtualWan”</span><span class="sxs-lookup"><span data-stu-id="f1219-586">'New-AzVirtualWan'</span></span>
    - <span data-ttu-id="f1219-587">”Update-AzVirtualWan”</span><span class="sxs-lookup"><span data-stu-id="f1219-587">'Update-AzVirtualWan'</span></span>
* <span data-ttu-id="f1219-588">Nya cmdletar har lagts till för att stödja DNS-zongrupp för privat slutpunkt</span><span class="sxs-lookup"><span data-stu-id="f1219-588">Added new cmdlets to support DNS zone group for private endpoint</span></span>
    - <span data-ttu-id="f1219-589">”New-AzPrivateDnsZoneConfig”</span><span class="sxs-lookup"><span data-stu-id="f1219-589">'New-AzPrivateDnsZoneConfig'</span></span>
    - <span data-ttu-id="f1219-590">”Get-AzPrivateDnsZoneGroup”</span><span class="sxs-lookup"><span data-stu-id="f1219-590">'Get-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="f1219-591">”New-AzPrivateDnsZoneGroup”</span><span class="sxs-lookup"><span data-stu-id="f1219-591">'New-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="f1219-592">”Set-AzPrivateDnsZoneGroup”</span><span class="sxs-lookup"><span data-stu-id="f1219-592">'Set-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="f1219-593">”Remove-AzPrivateDnsZoneGroup”</span><span class="sxs-lookup"><span data-stu-id="f1219-593">'Remove-AzPrivateDnsZoneGroup'</span></span>
* <span data-ttu-id="f1219-594">Parametrarna ”DNSEnableProxy”, ”DNSRequireProxyForNetworkRules” och ”DNSServers” har lagts till för ”AzureFirewall”</span><span class="sxs-lookup"><span data-stu-id="f1219-594">Added 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' and 'DNSServers' parameters to 'AzureFirewall'</span></span>
* <span data-ttu-id="f1219-595">Parametrarna ”EnableDnsProxy”, ”DnsProxyNotRequiredForNetworkRule” och ”DnsServer” har lagts till för ”AzureFirewall”</span><span class="sxs-lookup"><span data-stu-id="f1219-595">Added 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' and 'DnsServer' parameters to 'AzureFirewall'</span></span>
    - <span data-ttu-id="f1219-596">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="f1219-596">Updated cmdlet:</span></span>
        - <span data-ttu-id="f1219-597">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="f1219-597">New-AzFirewall</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f1219-598">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f1219-598">Az.OperationalInsights</span></span>
* <span data-ttu-id="f1219-599">Äldre kod har uppdaterats för att tillämpa ny genererad SDK</span><span class="sxs-lookup"><span data-stu-id="f1219-599">Updated legacy code to apply new generated SDK</span></span>
* <span data-ttu-id="f1219-600">Cmdletar har tagits bort på grund av föråldrade API:er</span><span class="sxs-lookup"><span data-stu-id="f1219-600">Deleted cmdlets due to deprecated APIs</span></span>
    - <span data-ttu-id="f1219-601">”Get-AzOperationalInsightsSavedSearchResult” (alias ”Get-AzOperationalInsightsSavedSearchResults”)</span><span class="sxs-lookup"><span data-stu-id="f1219-601">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span></span>
    - <span data-ttu-id="f1219-602">”Get-AzOperationalInsightsSearchResult” (alias ”Get-AzOperationalInsightsSearchResults”)</span><span class="sxs-lookup"><span data-stu-id="f1219-602">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span></span>
    - <span data-ttu-id="f1219-603">”Get-AzOperationalInsightsLinkTarget” (alias ”Get-AzOperationalInsightsLinkTargets”)</span><span class="sxs-lookup"><span data-stu-id="f1219-603">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span></span>
* <span data-ttu-id="f1219-604">Parametrar har lagts till för ”Set-AzOperationalInsightsWorkspace” och ”New-AzOperationalInsightsWorkspace”</span><span class="sxs-lookup"><span data-stu-id="f1219-604">Added parameters for 'Set-AzOperationalInsightsWorkspace' and 'New-AzOperationalInsightsWorkspace'</span></span>
* <span data-ttu-id="f1219-605">Cmdletar har skapats för länkat lagringskonto</span><span class="sxs-lookup"><span data-stu-id="f1219-605">Created cmdlets for Linked Stoarge Account</span></span>
* <span data-ttu-id="f1219-606">Cmdletar har skapats för kluster och länkad tjänst</span><span class="sxs-lookup"><span data-stu-id="f1219-606">Created cmdlets for Clusters and Linked Service</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f1219-607">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f1219-607">Az.RecoveryServices</span></span>
* <span data-ttu-id="f1219-608">Azure Site Recovery: Stöd har lagts till för att skydda VM-närhetsplaceringsgrupper för Azure till Azure-provider.</span><span class="sxs-lookup"><span data-stu-id="f1219-608">Azure Site Recovery added support for protecting proximity placement group virtual machines for Azure to Azure provider.</span></span>
* <span data-ttu-id="f1219-609">Azure Site Recovery: Stöd har lagts till för replikering mellan zoner.</span><span class="sxs-lookup"><span data-stu-id="f1219-609">Azure Site Recovery added support for zone to zone replication.</span></span>
* <span data-ttu-id="f1219-610">Azure Backup: Stöd har lagts till för långsiktig kvarhållning för Azure FileShare-återställningspunkter.</span><span class="sxs-lookup"><span data-stu-id="f1219-610">Azure Backup Added Long term retention support for Azure FileShare Recovery Points.</span></span>
* <span data-ttu-id="f1219-611">Azure Backup: Egenskaper för diskexkludering har lagts till för cmdlet-utdata från ”Get-AzRecoveryServicesBackupItem”.</span><span class="sxs-lookup"><span data-stu-id="f1219-611">Azure Backup Added disk exclusion properties to 'Get-AzRecoveryServicesBackupItem' cmdlet output.</span></span>
* <span data-ttu-id="f1219-612">En privat slutpunkt har lagts till för filen med valvets autentiseringsuppgifter för Site Recovery-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="f1219-612">Added private endpoint for Vault credential file for site recovery service.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f1219-613">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f1219-613">Az.Resources</span></span>
* <span data-ttu-id="f1219-614">En varning har lagts till om visningsfördröjning när en ny rolldefinition skapas</span><span class="sxs-lookup"><span data-stu-id="f1219-614">Added message warning about view delay when creating a new Role Definition</span></span>
* <span data-ttu-id="f1219-615">Princip-cmdletar har ändrats för utmatning av starkt typifierade objekt</span><span class="sxs-lookup"><span data-stu-id="f1219-615">Changed policy cmdlets to output strongly-typed objects</span></span>
* <span data-ttu-id="f1219-616">Parametern ”-TenantLevel” har tagits bort för användning med ”Get-AzResourceLock” [#11335]</span><span class="sxs-lookup"><span data-stu-id="f1219-616">Removed '-TenantLevel' parameter used for on the 'Get-AzResourceLock' cmdlet [#11335]</span></span>
* <span data-ttu-id="f1219-617">”Remove-AzResourceGroup -Id ResourceId” har åtgärdats [#9882]</span><span class="sxs-lookup"><span data-stu-id="f1219-617">Fixed 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span></span>
* <span data-ttu-id="f1219-618">En ny cmdlet har lagts till för att hämta What-If-resultat för ARM-mallar i omfånget för resursgrupper: ”Get-AzDeploymentResourceGroupWhatIfResult”</span><span class="sxs-lookup"><span data-stu-id="f1219-618">Added new cmdlet for getting ARM template What-If results at resource group scope: 'Get-AzDeploymentResourceGroupWhatIfResult'</span></span>
* <span data-ttu-id="f1219-619">En ny cmdlet har lagts till för att hämta What-If-resultat för ARM-mallar i prenumerationsomfånget: ”Get-AzDeploymentWhatIfResult”</span><span class="sxs-lookup"><span data-stu-id="f1219-619">Added new cmdlet for getting ARM template What-If results at subscription scope: 'Get-AzDeploymentWhatIfResult'</span></span>
   - <span data-ttu-id="f1219-620">Alias: ”Get-AzSubscriptionDeploymentWhatIf”</span><span class="sxs-lookup"><span data-stu-id="f1219-620">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span></span>
* <span data-ttu-id="f1219-621">Parametrarna ”-WhatIf” och ”-Confirm” har åsidosatts för ”New-AzDeployment” och ”New-AzResourceGroupDeployment” för att använda What-If-resultat för ARM-mallar</span><span class="sxs-lookup"><span data-stu-id="f1219-621">Overrode '-WhatIf' and '-Confirm' parameters for 'New-AzDeployment' and 'New-AzResourceGroupDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="f1219-622">Ett utfasningsmeddelande har lagts till för parametern ”ApiVersion” i distributions-cmdletar</span><span class="sxs-lookup"><span data-stu-id="f1219-622">Added deprecation message for 'ApiVersion' parameter in deployment cmdlets</span></span>
* <span data-ttu-id="f1219-623">En funktion har lagts till för att visa förbättrade felmeddelanden för distributionsfel</span><span class="sxs-lookup"><span data-stu-id="f1219-623">Added capability to show improved error messages for deployment failures</span></span>
* <span data-ttu-id="f1219-624">CorrelationId-loggning har lagts till för distributionsfel</span><span class="sxs-lookup"><span data-stu-id="f1219-624">Added correlationId logging for deployment failures</span></span>
* <span data-ttu-id="f1219-625">Egenskapen ”error” har lagts till i utdata från distributionsskript</span><span class="sxs-lookup"><span data-stu-id="f1219-625">Added 'error' property to the deployment script output</span></span>
* <span data-ttu-id="f1219-626">Nuget Microsoft.Azure.Management.ResourceManager har uppdaterats till ”3.7.1-preview”</span><span class="sxs-lookup"><span data-stu-id="f1219-626">Updated nuget Microsoft.Azure.Management.ResourceManager to '3.7.1-preview'</span></span>
* <span data-ttu-id="f1219-627">Specifika testfall har tagits bort då egenskapen Error i DeploymentValidateResult har ändrats till lässkyddad från nuget 3.7.1-preview</span><span class="sxs-lookup"><span data-stu-id="f1219-627">Removed specific test cases as Error property in DeploymentValidateResult has changed to readonly from nuget 3.7.1-preview</span></span>
* <span data-ttu-id="f1219-628">GenericResourceExpanded har flyttats från SDK ResourceManager 3.7.1-preview</span><span class="sxs-lookup"><span data-stu-id="f1219-628">Brought GenericResourceExpanded from SDK ResourceManager 3.7.1-preview</span></span>
* <span data-ttu-id="f1219-629">Stöd för taggar har lagts till för alla Get-cmdletar för distribution, samt</span><span class="sxs-lookup"><span data-stu-id="f1219-629">Added tag support for all Get cmdlets for deployment, as well as</span></span>
    - <span data-ttu-id="f1219-630">”New-AzDeployment”</span><span class="sxs-lookup"><span data-stu-id="f1219-630">'New-AzDeployment'</span></span>
    - <span data-ttu-id="f1219-631">”New-AzManagementGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="f1219-631">'New-AzManagementGroupDeployment'</span></span>
    - <span data-ttu-id="f1219-632">”New-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="f1219-632">'New-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="f1219-633">”New-AzTenantDeployment”</span><span class="sxs-lookup"><span data-stu-id="f1219-633">'New-AzTenantDeployment'</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f1219-634">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f1219-634">Az.ServiceFabric</span></span>
* <span data-ttu-id="f1219-635">En bugg har åtgärdats som gjorde att --SecretIdentifier fick fel tumavtryck för certifikat när ett certifikat lades till</span><span class="sxs-lookup"><span data-stu-id="f1219-635">Fixed bug in add certificate using --SecretIdentifier that was getting the wrong certificate thumbprint</span></span>

#### <a name="azsql"></a><span data-ttu-id="f1219-636">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f1219-636">Az.Sql</span></span>
* <span data-ttu-id="f1219-637">Förbättrade prestanda för:</span><span class="sxs-lookup"><span data-stu-id="f1219-637">Enhance performance of:</span></span>
    - <span data-ttu-id="f1219-638">”Set-AzSqlDatabaseSensitivityClassification”</span><span class="sxs-lookup"><span data-stu-id="f1219-638">'Set-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="f1219-639">”Set-AzSqlInstanceDatabaseSensitivityClassification”</span><span class="sxs-lookup"><span data-stu-id="f1219-639">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="f1219-640">”Remove-AzSqlDatabaseSensitivityClassification”</span><span class="sxs-lookup"><span data-stu-id="f1219-640">'Remove-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="f1219-641">”Remove-AzSqlInstanceDatabaseSensitivityClassification”</span><span class="sxs-lookup"><span data-stu-id="f1219-641">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="f1219-642">”Enable-AzSqlDatabaseSensitivityRecommendation”</span><span class="sxs-lookup"><span data-stu-id="f1219-642">'Enable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="f1219-643">”Enable-AzSqlInstanceDatabaseSensitivityRecommendation”</span><span class="sxs-lookup"><span data-stu-id="f1219-643">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="f1219-644">”Disable-AzSqlDatabaseSensitivityRecommendation”</span><span class="sxs-lookup"><span data-stu-id="f1219-644">'Disable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="f1219-645">”Disable-AzSqlInstanceDatabaseSensitivityRecommendation”</span><span class="sxs-lookup"><span data-stu-id="f1219-645">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
* <span data-ttu-id="f1219-646">Validering på klientsidan har tagits bort för parametern ”RetentionDays” från cmdleten ”Set-AzSqlDatabaseBackupShortTermRetentionPolicy”</span><span class="sxs-lookup"><span data-stu-id="f1219-646">Removed client-side validation of 'RetentionDays' parameter from cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span>
* <span data-ttu-id="f1219-647">Granskning av ett lagringskonto i Vnet; en bugg har åtgärdats som orsakade fel när en Storage Blob Data-deltagarroll skapades.</span><span class="sxs-lookup"><span data-stu-id="f1219-647">Auditing to a storage account in Vnet, fixing a bug when creating a Storage Blob Data Contributor role.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f1219-648">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f1219-648">Az.Storage</span></span>
* <span data-ttu-id="f1219-649">”-AsJob” har lagts till för att hämta/lista konto med cmdleten ”Get-AzStorageAccount”</span><span class="sxs-lookup"><span data-stu-id="f1219-649">Added '-AsJob' to get/list account cmdlet 'Get-AzStorageAccount'</span></span>
* <span data-ttu-id="f1219-650">Gör KeyVersion valfri när lagringskontot uppdateras med KeyvaultEncryption, för att ge stöd för automatisk nyckelrotation</span><span class="sxs-lookup"><span data-stu-id="f1219-650">Make KeyVersion to optional when update Storage account with KeyvaultEncryption, to support key auto-rotation</span></span>
    - <span data-ttu-id="f1219-651">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="f1219-651">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="f1219-652">Problemet med borttagning av Azure-filkatalog i pipeline har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="f1219-652">Fixed remove Azure File Directory fail with pipeline</span></span>
    - <span data-ttu-id="f1219-653">”Remove-AzStorageDirectory”</span><span class="sxs-lookup"><span data-stu-id="f1219-653">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="f1219-654">Åtgärdat [#9880]: Definitionen av DefaultAction-värdet för NetWorkRule har ändrats för konsekvens med Swagger.</span><span class="sxs-lookup"><span data-stu-id="f1219-654">Fixed [#9880]: Change NetWorkRule DefaultAction value defination to align with swagger.</span></span>
    - <span data-ttu-id="f1219-655">”Update-AzStorageAccountNetworkRuleSet”</span><span class="sxs-lookup"><span data-stu-id="f1219-655">'Update-AzStorageAccountNetworkRuleSet'</span></span>
    - <span data-ttu-id="f1219-656">”Get-AzStorageAccountNetworkRuleSet”</span><span class="sxs-lookup"><span data-stu-id="f1219-656">'Get-AzStorageAccountNetworkRuleSet'</span></span>
* <span data-ttu-id="f1219-657">Åtgärdat [#11624]: Hoppa över dubblettregler när NetworkRules läggs till, för att undvika serverfel</span><span class="sxs-lookup"><span data-stu-id="f1219-657">Fixed [#11624]: Skip duplicated rules when add NetworkRules, to avoid server failure</span></span>
    - <span data-ttu-id="f1219-658">”Add-AzStorageAccountNetworkRule”</span><span class="sxs-lookup"><span data-stu-id="f1219-658">'Add-AzStorageAccountNetworkRule'</span></span>
* <span data-ttu-id="f1219-659">Microsoft.Azure.Cosmos.Table SDK har uppgraderats till 1.0.7</span><span class="sxs-lookup"><span data-stu-id="f1219-659">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.7</span></span>
* <span data-ttu-id="f1219-660">Ett varningsmeddelande har lagts till för att påminna användaren om att lista igen med ContinuationToken när endast delobjekt returneras i listan med DataLake Gen2-objekt,</span><span class="sxs-lookup"><span data-stu-id="f1219-660">Added a warning message to remind user to list again with ContinuationToken when only part items are returned in list DataLake Gen2 Items,</span></span>
    - <span data-ttu-id="f1219-661">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="f1219-661">'Get-AzDataLakeGen2ChildItem'</span></span>
* <span data-ttu-id="f1219-662">Stöd för att skapa eller uppdatera lagringskonto med Azure Files Active Directory Domain Service-autentisering</span><span class="sxs-lookup"><span data-stu-id="f1219-662">Supported to create or update Storage account with Azure Files Active Directory Domain Service Authentication</span></span>
    -  <span data-ttu-id="f1219-663">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="f1219-663">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="f1219-664">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="f1219-664">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="f1219-665">Stöd för nya eller listade Kerberos-nycklar för lagringskontot</span><span class="sxs-lookup"><span data-stu-id="f1219-665">Supported to new or list Kerberos keys of Storage account</span></span>
    -  <span data-ttu-id="f1219-666">”New-AzStorageAccountKey”</span><span class="sxs-lookup"><span data-stu-id="f1219-666">'New-AzStorageAccountKey'</span></span>
    -  <span data-ttu-id="f1219-667">”Get-AzStorageAccountKey”</span><span class="sxs-lookup"><span data-stu-id="f1219-667">'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="f1219-668">Stöd för redundans med lagringskonto</span><span class="sxs-lookup"><span data-stu-id="f1219-668">Supported failover Storage account</span></span>
    - <span data-ttu-id="f1219-669">”Invoke-AzStorageAccountFailover”</span><span class="sxs-lookup"><span data-stu-id="f1219-669">'Invoke-AzStorageAccountFailover'</span></span>
* <span data-ttu-id="f1219-670">Hjälpen för ”Get-AzStorageBlobCopyState” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="f1219-670">Updated help of 'Get-AzStorageBlobCopyState'</span></span>
* <span data-ttu-id="f1219-671">Hjälpen för ”Get-AzStorageFileCopyState” och ”Start-AzStorageBlobCopy” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="f1219-671">Updated help of 'Get-AzStorageFileCopyState' and 'Start-AzStorageBlobCopy'</span></span>
* <span data-ttu-id="f1219-672">Lagringsklientbibliotek v12 har integrerats med Queue- och File-cmdletar</span><span class="sxs-lookup"><span data-stu-id="f1219-672">Integrated Storage client library v12 to Queue and File cmdlets</span></span>
* <span data-ttu-id="f1219-673">Utdatatypen har ändrats från CloudFile till AzureStorageFile; ursprungliga utdata blir en underordnad egenskap i den nya utmatningen</span><span class="sxs-lookup"><span data-stu-id="f1219-673">Changed output type from CloudFile to AzureStorageFile, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="f1219-674">”Get-AzStorageFile”</span><span class="sxs-lookup"><span data-stu-id="f1219-674">'Get-AzStorageFile'</span></span>
    - <span data-ttu-id="f1219-675">”Remove-AzStorageFile”</span><span class="sxs-lookup"><span data-stu-id="f1219-675">'Remove-AzStorageFile'</span></span>
    - <span data-ttu-id="f1219-676">”Get-AzStorageFileContent”</span><span class="sxs-lookup"><span data-stu-id="f1219-676">'Get-AzStorageFileContent'</span></span>
    - <span data-ttu-id="f1219-677">”Set-AzStorageFileContent”</span><span class="sxs-lookup"><span data-stu-id="f1219-677">'Set-AzStorageFileContent'</span></span>
    - <span data-ttu-id="f1219-678">”Start-AzStorageFileCopy”</span><span class="sxs-lookup"><span data-stu-id="f1219-678">'Start-AzStorageFileCopy'</span></span>
* <span data-ttu-id="f1219-679">Utdatatypen har ändrats från CloudFileDirectory till AzureStorageFileDirectory; ursprungliga utdata blir en underordnad egenskap i den nya utmatningen</span><span class="sxs-lookup"><span data-stu-id="f1219-679">Changed output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="f1219-680">”New-AzStorageDirectory”</span><span class="sxs-lookup"><span data-stu-id="f1219-680">'New-AzStorageDirectory'</span></span>
    - <span data-ttu-id="f1219-681">”Remove-AzStorageDirectory”</span><span class="sxs-lookup"><span data-stu-id="f1219-681">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="f1219-682">Utdatatypen har ändrats från CloudFileShare till AzureStorageFileShare; ursprungliga utdata blir en underordnad egenskap i den nya utmatningen</span><span class="sxs-lookup"><span data-stu-id="f1219-682">Changed output type from CloudFileShare to AzureStorageFileShare, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="f1219-683">”Get-AzStorageShare”</span><span class="sxs-lookup"><span data-stu-id="f1219-683">'Get-AzStorageShare'</span></span>
    - <span data-ttu-id="f1219-684">”New-AzStorageShare”</span><span class="sxs-lookup"><span data-stu-id="f1219-684">'New-AzStorageShare'</span></span>
    - <span data-ttu-id="f1219-685">”Remove-AzStorageShare”</span><span class="sxs-lookup"><span data-stu-id="f1219-685">'Remove-AzStorageShare'</span></span>
* <span data-ttu-id="f1219-686">Utdatatypen har ändrats från FileShareProperties till AzureStorageFileShare; ursprungliga utdata blir en underordnad egenskap i den nya utmatningen</span><span class="sxs-lookup"><span data-stu-id="f1219-686">Changed output type from FileShareProperties to AzureStorageFileShare, the original output will become a sub child property of the new output</span></span>
    - <span data-ttu-id="f1219-687">”Set-AzStorageShareQuota”</span><span class="sxs-lookup"><span data-stu-id="f1219-687">'Set-AzStorageShareQuota'</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="f1219-688">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="f1219-688">Az.TrafficManager</span></span>
* <span data-ttu-id="f1219-689">Felaktigt profilnamn har åtgärdats i utförliga utdata för ”DisableAzureTrafficManagerEndpoint”</span><span class="sxs-lookup"><span data-stu-id="f1219-689">Fixed incorrect profile name in 'DisableAzureTrafficManagerEndpoint' verbose output</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f1219-690">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f1219-690">Az.Websites</span></span>
* <span data-ttu-id="f1219-691">Stavfel har åtgärdats i hjälpen för ”Update-AzWebAppAccessRestrictionConfig”.</span><span class="sxs-lookup"><span data-stu-id="f1219-691">Fixed typo on help of 'Update-AzWebAppAccessRestrictionConfig'.</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="f1219-692">3.8.0 – April 2020</span><span class="sxs-lookup"><span data-stu-id="f1219-692">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="f1219-693">Höjdpunkter sedan den senaste uppdateringen</span><span class="sxs-lookup"><span data-stu-id="f1219-693">Highlights since the last release</span></span>
* <span data-ttu-id="f1219-694">PowerShell-versioner som Az.Storage stöder: Windows PowerShell 5.1, PowerShell Core 6.2.4+ och PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="f1219-694">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f1219-695">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f1219-695">Az.Accounts</span></span>
* <span data-ttu-id="f1219-696">Uppdaterade URL:en för Azure PowerShell-enkäten i ”Resolve-AzError” [#11507]</span><span class="sxs-lookup"><span data-stu-id="f1219-696">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="f1219-697">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f1219-697">Az.ApiManagement</span></span>
* <span data-ttu-id="f1219-698">Lade till meddelande om icke-bakåtkompatibel ändring vid ändring i utdata för Azure File-cmdletar i en framtida version</span><span class="sxs-lookup"><span data-stu-id="f1219-698">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="f1219-699">"Set-AzApiManagementGroup" Uppdaterad dokumentation för att ange GroupId-parametern</span><span class="sxs-lookup"><span data-stu-id="f1219-699">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="f1219-700">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f1219-700">Az.Cdn</span></span>
* <span data-ttu-id="f1219-701">Fast ChinaCDN-relaterad prissättning för SKU-visning</span><span class="sxs-lookup"><span data-stu-id="f1219-701">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f1219-702">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f1219-702">Az.CognitiveServices</span></span>
* <span data-ttu-id="f1219-703">Identitet som stöds, kryptering, UserOwnedStorage</span><span class="sxs-lookup"><span data-stu-id="f1219-703">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f1219-704">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f1219-704">Az.Compute</span></span>
* <span data-ttu-id="f1219-705">Cmdleten ”Set-AzVmssOrchestrationServiceState” har lagts till.</span><span class="sxs-lookup"><span data-stu-id="f1219-705">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="f1219-706">”Get-AzVmss” med -InstanceView visar OrchestrationService-tillstånd.</span><span class="sxs-lookup"><span data-stu-id="f1219-706">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f1219-707">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f1219-707">Az.IotHub</span></span>
* <span data-ttu-id="f1219-708">Hantera den dubbla konfigurationen för IoT-enheter, nya cmdletar är:</span><span class="sxs-lookup"><span data-stu-id="f1219-708">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="f1219-709">'Get-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="f1219-709">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="f1219-710">'Update-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="f1219-710">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="f1219-711">En cmdlet har lagts till för att anropa direkt metod på en enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="f1219-711">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="f1219-712">Hantera dubbel konfiguration för IoT-enhetsmodul, nya cmdletar är:</span><span class="sxs-lookup"><span data-stu-id="f1219-712">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="f1219-713">'Get-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="f1219-713">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="f1219-714">'Update-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="f1219-714">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="f1219-715">Hantera IoT-automatisk konfiguration av enhetshantering i stor skala.</span><span class="sxs-lookup"><span data-stu-id="f1219-715">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="f1219-716">Nya cmdlet:ar är:</span><span class="sxs-lookup"><span data-stu-id="f1219-716">New cmdlets are:</span></span>
    - <span data-ttu-id="f1219-717">'Add-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="f1219-717">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="f1219-718">'Get-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="f1219-718">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="f1219-719">'Remove-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="f1219-719">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="f1219-720">'Set-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="f1219-720">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="f1219-721">En cmdlet har lagts till för att anropa en edge-modulmetod i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="f1219-721">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f1219-722">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f1219-722">Az.KeyVault</span></span>
* <span data-ttu-id="f1219-723">Har lagt till en ny cmdlet, "Update-AzKeyVault", som kan aktivera mjuk borttagning och rensning av skydd i ett valv</span><span class="sxs-lookup"><span data-stu-id="f1219-723">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="f1219-724">Har lagt till stöd i Microsoft.PowerShell.SecretManagement [#11178]</span><span class="sxs-lookup"><span data-stu-id="f1219-724">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="f1219-725">Åtgärdat fel i exemplen i 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span><span class="sxs-lookup"><span data-stu-id="f1219-725">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="f1219-726">Har lagt till stöd för privat slutpunkt</span><span class="sxs-lookup"><span data-stu-id="f1219-726">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="f1219-727">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="f1219-727">Az.Maintenance</span></span>
* <span data-ttu-id="f1219-728">Publicerar slutversion av underhålls-cmdletar för GA</span><span class="sxs-lookup"><span data-stu-id="f1219-728">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f1219-729">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f1219-729">Az.Monitor</span></span>
* <span data-ttu-id="f1219-730">Har lagt till cmdletar för privat länkomfång</span><span class="sxs-lookup"><span data-stu-id="f1219-730">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="f1219-731">'Get-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="f1219-731">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="f1219-732">'Remove-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="f1219-732">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="f1219-733">'New-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="f1219-733">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="f1219-734">'Update-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="f1219-734">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="f1219-735">'Get-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="f1219-735">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="f1219-736">'New-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="f1219-736">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="f1219-737">'Remove-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="f1219-737">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f1219-738">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f1219-738">Az.Network</span></span>
* <span data-ttu-id="f1219-739">Uppdaterade cmdletar för att aktivera anslutning på privat IP för Virtual Network Gateway.</span><span class="sxs-lookup"><span data-stu-id="f1219-739">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="f1219-740">'New-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="f1219-740">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="f1219-741">'Set-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="f1219-741">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="f1219-742">'New-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="f1219-742">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="f1219-743">'Set-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="f1219-743">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="f1219-744">Uppdaterade cmdletar för att aktivera FQDN-baserade LocalNetworkGateways och VpnSites</span><span class="sxs-lookup"><span data-stu-id="f1219-744">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="f1219-745">'New-AzLocalNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="f1219-745">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="f1219-746">'New-AzVpnSiteLink'</span><span class="sxs-lookup"><span data-stu-id="f1219-746">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="f1219-747">Stöd har lagts till för IPv6-adresstypen i ExpressRouteCircuitConnectionConfig (Global Reach)</span><span class="sxs-lookup"><span data-stu-id="f1219-747">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="f1219-748">Lade till 'Set-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="f1219-748">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="f1219-749">tillåter inställning av alla befintliga egenskaper inklusive IPv6CircuitConnectionProperties</span><span class="sxs-lookup"><span data-stu-id="f1219-749">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="f1219-750">Uppdaterade 'Add-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="f1219-750">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="f1219-751">Lade till en ytterligare valfri parameter, AddressPrefixType, för att specificera adresstypen för adressprefix</span><span class="sxs-lookup"><span data-stu-id="f1219-751">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="f1219-752">Uppdaterade cmdletar för att aktivera inställningen för DPD-timeout på Virtual Network Gateway-anslutningar.</span><span class="sxs-lookup"><span data-stu-id="f1219-752">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="f1219-753">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f1219-753">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="f1219-754">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f1219-754">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f1219-755">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f1219-755">Az.PolicyInsights</span></span>
* <span data-ttu-id="f1219-756">Cmdleten "Start-AzPolicyComplianceScan" har lagts till för att utlösa genomsökningar av principefterlevnad</span><span class="sxs-lookup"><span data-stu-id="f1219-756">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="f1219-757">Principdefinition, uppsättningsdefinition och tilldelningsversioner har lagts till i "Get-AzPolicyState"-utdata</span><span class="sxs-lookup"><span data-stu-id="f1219-757">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f1219-758">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f1219-758">Az.ServiceFabric</span></span>
* <span data-ttu-id="f1219-759">Förbättrad kodformatering och användbarhet för "New-AzServiceFabricCluster"-exempel</span><span class="sxs-lookup"><span data-stu-id="f1219-759">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="f1219-760">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f1219-760">Az.Sql</span></span>
* <span data-ttu-id="f1219-761">Lade till cmdletarna "Get-AzSqlInstanceOperation" och "Stop-AzSqlInstanceOperation"</span><span class="sxs-lookup"><span data-stu-id="f1219-761">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="f1219-762">Stöd för granskning för ett lagringskonto i VNet.</span><span class="sxs-lookup"><span data-stu-id="f1219-762">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f1219-763">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f1219-763">Az.Storage</span></span>
* <span data-ttu-id="f1219-764">Lade till meddelande om icke-bakåtkompatibel ändring vid ändring i utdata för Azure File-cmdletar i en framtida version</span><span class="sxs-lookup"><span data-stu-id="f1219-764">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="f1219-765">Stöd för nya SkuName StandardGZRS, StandardRAGZRS när ett lagringskonto skapas/uppdateras</span><span class="sxs-lookup"><span data-stu-id="f1219-765">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="f1219-766">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="f1219-766">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="f1219-767">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="f1219-767">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="f1219-768">Stöd för DataLake Gen2</span><span class="sxs-lookup"><span data-stu-id="f1219-768">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="f1219-769">'New-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="f1219-769">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="f1219-770">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="f1219-770">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="f1219-771">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="f1219-771">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="f1219-772">'Move-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="f1219-772">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="f1219-773">'Set-AzDataLakeGen2ItemAclObject'</span><span class="sxs-lookup"><span data-stu-id="f1219-773">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="f1219-774">'Update-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="f1219-774">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="f1219-775">'Get-AzDataLakeGen2ItemContent'</span><span class="sxs-lookup"><span data-stu-id="f1219-775">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="f1219-776">'Remove-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="f1219-776">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="f1219-777">0.10.0-förhandsversion – April 2020</span><span class="sxs-lookup"><span data-stu-id="f1219-777">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="f1219-778">Allmänt</span><span class="sxs-lookup"><span data-stu-id="f1219-778">General</span></span>
* <span data-ttu-id="f1219-779">Az-moduler är nu tillgängliga i förhandsversion på Azure Stack Hub.</span><span class="sxs-lookup"><span data-stu-id="f1219-779">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="f1219-780">Därmed möjliggörs kompatibilitet för flera plattformar med Linux och macOs.</span><span class="sxs-lookup"><span data-stu-id="f1219-780">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="f1219-781">Azure Stack Hub stöder nu PowerShell Core med AZ-moduler. Mer information finns [här](https://aka.ms/az4AzureStack)</span><span class="sxs-lookup"><span data-stu-id="f1219-781">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](https://aka.ms/az4AzureStack)</span></span>
* <span data-ttu-id="f1219-782">Supportprofil för AZ-moduler 2019-03-01-hybrid:</span><span class="sxs-lookup"><span data-stu-id="f1219-782">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="f1219-783">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="f1219-783">Az.Billing</span></span>
  - <span data-ttu-id="f1219-784">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f1219-784">Az.Compute</span></span>
  - <span data-ttu-id="f1219-785">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="f1219-785">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="f1219-786">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f1219-786">Az.EventHub</span></span>
  - <span data-ttu-id="f1219-787">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f1219-787">Az.IotHub</span></span>
  - <span data-ttu-id="f1219-788">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f1219-788">Az.KeyVault</span></span>
  - <span data-ttu-id="f1219-789">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f1219-789">Az.Monitor</span></span>
  - <span data-ttu-id="f1219-790">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f1219-790">Az.Network</span></span>
  - <span data-ttu-id="f1219-791">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f1219-791">Az.Resources</span></span>
  - <span data-ttu-id="f1219-792">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f1219-792">Az.Storage</span></span>
  - <span data-ttu-id="f1219-793">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f1219-793">Az.Websites</span></span>
* <span data-ttu-id="f1219-794">Tre nya PowerShell-moduler för AZ har introducerats som fungerar med Azure Stack Hub, och de är Az.Databox, Az.IotHub och Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f1219-794">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="f1219-795">Kommandona är i princip oförändrade, med endast mindre ändringar som att AzureRM ändras till AZ</span><span class="sxs-lookup"><span data-stu-id="f1219-795">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="f1219-796">En uppdaterad länk till PowerShell-dokumentationen för Azure Stack Hub finns [här](https://aka.ms/InstallASHPowerShell)</span><span class="sxs-lookup"><span data-stu-id="f1219-796">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](https://aka.ms/InstallASHPowerShell)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="f1219-797">3.7.0 – mars 2020</span><span class="sxs-lookup"><span data-stu-id="f1219-797">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f1219-798">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f1219-798">Az.Accounts</span></span>
* <span data-ttu-id="f1219-799">Åtgärdade ”Get-AzTenant”/”Get-AzDefault”/”Set-AzDefault”-utlösning av NullReferenceException när du inte är inloggad [#10292]</span><span class="sxs-lookup"><span data-stu-id="f1219-799">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f1219-800">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f1219-800">Az.Compute</span></span>
* <span data-ttu-id="f1219-801">Följande parametrar har lagts till i cmdleten ”New-AzDiskConfig”:</span><span class="sxs-lookup"><span data-stu-id="f1219-801">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="f1219-802">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="f1219-802">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="f1219-803">Tillåten krypteringsegenskap till målparametern för cmdleten ”New-AzGalleryImageVersion”.</span><span class="sxs-lookup"><span data-stu-id="f1219-803">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="f1219-804">Åtgärdade tempDisk-problem för cmdletarna ”Set-AzVmss”-Reimage och ”Invoke-AzVMReimage”.</span><span class="sxs-lookup"><span data-stu-id="f1219-804">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="f1219-805">[#11354]</span><span class="sxs-lookup"><span data-stu-id="f1219-805">[#11354]</span></span>
* <span data-ttu-id="f1219-806">Stöd har lagts till i nedanstående cmdletar för nytt SAP-tillägg</span><span class="sxs-lookup"><span data-stu-id="f1219-806">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="f1219-807">”Set-AzVMAEMExtension”</span><span class="sxs-lookup"><span data-stu-id="f1219-807">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="f1219-808">”Get-AzVMAEMExtension”</span><span class="sxs-lookup"><span data-stu-id="f1219-808">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="f1219-809">”Remove-AzVMAEMExtension”</span><span class="sxs-lookup"><span data-stu-id="f1219-809">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="f1219-810">”Update-AzVMAEMExtension”</span><span class="sxs-lookup"><span data-stu-id="f1219-810">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="f1219-811">Åtgärdade fel i exempel på hjälpdokument</span><span class="sxs-lookup"><span data-stu-id="f1219-811">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="f1219-812">Visade det exakta strängvärdet för VM PowerState i tabellformat.</span><span class="sxs-lookup"><span data-stu-id="f1219-812">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="f1219-813">”New-AzVmssConfig”: den fasta serialiseringen av egenskapen AutomaticRepairs när SinglePlacementGroup är inaktiverad.</span><span class="sxs-lookup"><span data-stu-id="f1219-813">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="f1219-814">[#11257]</span><span class="sxs-lookup"><span data-stu-id="f1219-814">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f1219-815">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f1219-815">Az.DataFactory</span></span>
* <span data-ttu-id="f1219-816">ADF .Net SDK har uppdaterats till 4.8.0</span><span class="sxs-lookup"><span data-stu-id="f1219-816">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="f1219-817">Valfria parametrar har lagts till i kommandot ”Invoke-AzDataFactoryV2Pipeline” för att stödja omkörning</span><span class="sxs-lookup"><span data-stu-id="f1219-817">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f1219-818">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f1219-818">Az.DataLakeStore</span></span>
* <span data-ttu-id="f1219-819">Lade till beskrivning för icke-bakåtkompatibel ändring för ”Export-AzDataLakeStoreItem” och ”Import-AzDataLakeStoreItem”</span><span class="sxs-lookup"><span data-stu-id="f1219-819">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="f1219-820">Lade till alternativ för bytekodning för ”New-AzDataLakeStoreItem”, ”Add-AzDAtaLakeStoreItemContent” och ”Get-AzDAtaLakeStoreItemContent”</span><span class="sxs-lookup"><span data-stu-id="f1219-820">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="f1219-821">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f1219-821">Az.HDInsight</span></span>
* <span data-ttu-id="f1219-822">Stöd för att ange en minimal TLS-version som stöds när klustret skapas.</span><span class="sxs-lookup"><span data-stu-id="f1219-822">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f1219-823">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f1219-823">Az.IotHub</span></span>
* <span data-ttu-id="f1219-824">Stöd har lagts till för att hantera distribuerade inställningar per enhet.</span><span class="sxs-lookup"><span data-stu-id="f1219-824">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="f1219-825">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="f1219-825">New Cmdlets are:</span></span>
    - <span data-ttu-id="f1219-826">”Get-AzIotHubDistributedTracing”</span><span class="sxs-lookup"><span data-stu-id="f1219-826">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="f1219-827">”Set-AzIotHubDistributedTracing”</span><span class="sxs-lookup"><span data-stu-id="f1219-827">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f1219-828">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f1219-828">Az.KeyVault</span></span>
* <span data-ttu-id="f1219-829">Ändrade attribut för icke-bakåtkompatibel ändring lades till för ”New-AzKeyVault”</span><span class="sxs-lookup"><span data-stu-id="f1219-829">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f1219-830">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f1219-830">Az.Monitor</span></span>
* <span data-ttu-id="f1219-831">Uppdaterad dokumentation för ”New-AzScheduledQueryRuleLogMetricTrigger”</span><span class="sxs-lookup"><span data-stu-id="f1219-831">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f1219-832">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f1219-832">Az.Network</span></span>
* <span data-ttu-id="f1219-833">Uppdaterade cmdletar för att tillåta VirtualHubVnetConnections mellan klienter</span><span class="sxs-lookup"><span data-stu-id="f1219-833">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="f1219-834">”New-AzVirtualHubVnetConnection”</span><span class="sxs-lookup"><span data-stu-id="f1219-834">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="f1219-835">”Update-AzVirtualHubVnetConnection”</span><span class="sxs-lookup"><span data-stu-id="f1219-835">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="f1219-836">”New-AzVirtualHub”</span><span class="sxs-lookup"><span data-stu-id="f1219-836">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="f1219-837">”Update-AzVirtualHub”</span><span class="sxs-lookup"><span data-stu-id="f1219-837">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="f1219-838">SQL Management SDK-beroende har tagits bort</span><span class="sxs-lookup"><span data-stu-id="f1219-838">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f1219-839">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f1219-839">Az.PolicyInsights</span></span>
* <span data-ttu-id="f1219-840">Förbättrade felmeddelanden</span><span class="sxs-lookup"><span data-stu-id="f1219-840">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f1219-841">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f1219-841">Az.RecoveryServices</span></span>
* <span data-ttu-id="f1219-842">Azure Site Recovery har lagt till stöd för återaktivering av skydd och uppdaterade VM-egenskaper för virtuella Azure-datorer med krypterad disk.</span><span class="sxs-lookup"><span data-stu-id="f1219-842">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="f1219-843">Lade till Azure Site Recovery VmwareToAzure-egenskaper för DR-övervakning</span><span class="sxs-lookup"><span data-stu-id="f1219-843">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="f1219-844">Azure Backup har lagt till stöd för att försöka uppdatera principuppdateringen för misslyckade objekt på nytt.</span><span class="sxs-lookup"><span data-stu-id="f1219-844">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="f1219-845">Azure Backup lagt till stöd för diskundantagsinställningar under säkerhetskopiering och återställning.</span><span class="sxs-lookup"><span data-stu-id="f1219-845">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="f1219-846">Azure Backup lagt till stöd för att återställa flera filer/mappar i AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="f1219-846">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="f1219-847">Azure Backup lade till support för användardefinierad Resourcegroup-support vid uppdatering av IaasVM-princip</span><span class="sxs-lookup"><span data-stu-id="f1219-847">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="f1219-848">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f1219-848">Az.Resources</span></span>
* <span data-ttu-id="f1219-849">Åtgärdade ”Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType” så att den använder den faktisk apiVersion av resurser i stället för standard-apiVersion [#11267]</span><span class="sxs-lookup"><span data-stu-id="f1219-849">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="f1219-850">Lade till correlationId-loggning för felscenarier</span><span class="sxs-lookup"><span data-stu-id="f1219-850">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="f1219-851">Liten dokumentationsändring för ”Get-AzResourceLock”.</span><span class="sxs-lookup"><span data-stu-id="f1219-851">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="f1219-852">Lade till exempel.</span><span class="sxs-lookup"><span data-stu-id="f1219-852">Added example.</span></span>
* <span data-ttu-id="f1219-853">Undantaget enkelt citattecken i parametervärde för ”Get-AzADUser” [#11317]</span><span class="sxs-lookup"><span data-stu-id="f1219-853">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="f1219-854">Nya cmdletar har lagts till för distributionsskript (”Get-AzDeploymentScript”, ”Get-AzDeploymentScriptLog”, ”Save-AzDeploymentScriptLog”, ”Remove-AzDeploymentScript”)</span><span class="sxs-lookup"><span data-stu-id="f1219-854">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="f1219-855">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f1219-855">Az.Sql</span></span>
* <span data-ttu-id="f1219-856">En läsbar sekundär parameter har lagts till i Invoke-AzSqlDatabaseFailover</span><span class="sxs-lookup"><span data-stu-id="f1219-856">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="f1219-857">Cmdleten Disable-AzSqlServerActiveDirectoryOnlyAuthentication har lagts till</span><span class="sxs-lookup"><span data-stu-id="f1219-857">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="f1219-858">Den sparade känslighet rangordningen när kolumner klassificeras i databasen.</span><span class="sxs-lookup"><span data-stu-id="f1219-858">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="f1219-859">Az.Support</span><span class="sxs-lookup"><span data-stu-id="f1219-859">Az.Support</span></span>
* <span data-ttu-id="f1219-860">Allmän tillgänglighet för ”Az.Support”-modulen</span><span class="sxs-lookup"><span data-stu-id="f1219-860">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f1219-861">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f1219-861">Az.Websites</span></span>
* <span data-ttu-id="f1219-862">Stöd har lagts till för att arbeta med trafikdirigeringsregler för webbappar under nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="f1219-862">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="f1219-863">”Get-AzWebAppTrafficRouting”</span><span class="sxs-lookup"><span data-stu-id="f1219-863">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="f1219-864">”Update-AzWebAppTrafficRouting”</span><span class="sxs-lookup"><span data-stu-id="f1219-864">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="f1219-865">”Add-AzWebAppTrafficRouting”</span><span class="sxs-lookup"><span data-stu-id="f1219-865">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="f1219-866">”Remove-AzWebAppTrafficRouting”</span><span class="sxs-lookup"><span data-stu-id="f1219-866">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="f1219-867">3.6.1 – mars 2020</span><span class="sxs-lookup"><span data-stu-id="f1219-867">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f1219-868">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f1219-868">Az.Accounts</span></span>
* <span data-ttu-id="f1219-869">Öppna sidan med Azure PowerShell-enkäten i ”Send-Feedback” [#11020]</span><span class="sxs-lookup"><span data-stu-id="f1219-869">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="f1219-870">Visa URL:en för Azure PowerShell-enkäten i ”Resolve-Error” [#11021]</span><span class="sxs-lookup"><span data-stu-id="f1219-870">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="f1219-871">Az-version har lagts till i UserAgent</span><span class="sxs-lookup"><span data-stu-id="f1219-871">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="f1219-872">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f1219-872">Az.ApiManagement</span></span>
* <span data-ttu-id="f1219-873">Stöd har lagts till för att hämta och konfigurera en anpassad domän på DeveloperPortal-slutpunkten [#11007]</span><span class="sxs-lookup"><span data-stu-id="f1219-873">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="f1219-874">”Export-AzApiManagementApi” Stöd har lagts till för att ladda ned API-definition i Json-format [#9987]</span><span class="sxs-lookup"><span data-stu-id="f1219-874">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="f1219-875">”Import-AzApiManagementApi” Stöd har lagts till för att importera OpenApi 3.0-definition från Json-dokument</span><span class="sxs-lookup"><span data-stu-id="f1219-875">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="f1219-876">”New-AzApiManagementIdentityProvider” och ”Set-AzApiManagementIdentityProvider” Stöd har lagts till för att konfigurera ”Signin Tenant” för AAD B2C-provider [#9784]</span><span class="sxs-lookup"><span data-stu-id="f1219-876">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f1219-877">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f1219-877">Az.DataLakeStore</span></span>
* <span data-ttu-id="f1219-878">En referens har uttryckligen lagts till för System.Buffers i csproj och psd1.</span><span class="sxs-lookup"><span data-stu-id="f1219-878">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f1219-879">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f1219-879">Az.IotHub</span></span>
* <span data-ttu-id="f1219-880">Lade till stöd för att hantera enheter i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="f1219-880">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="f1219-881">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="f1219-881">New Cmdlets are:</span></span>
    - <span data-ttu-id="f1219-882">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="f1219-882">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="f1219-883">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="f1219-883">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="f1219-884">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="f1219-884">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="f1219-885">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="f1219-885">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="f1219-886">Stöd har lagts till för att hantera moduler på en mål-IoT-enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="f1219-886">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="f1219-887">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="f1219-887">New Cmdlets are:</span></span>
    - <span data-ttu-id="f1219-888">”Add-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="f1219-888">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="f1219-889">”Get-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="f1219-889">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="f1219-890">”Remove-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="f1219-890">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="f1219-891">”Set-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="f1219-891">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="f1219-892">Cmdlet har lagts till för att hämta anslutningssträngen för en mål-IoT-enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="f1219-892">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="f1219-893">Cmdlet har lagts till för att hämta anslutningssträngen för en modul på en mål-IoT-enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="f1219-893">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="f1219-894">Stöd har lagts till för att hämta/ange en överordnad enhet för en IoT-enhet.</span><span class="sxs-lookup"><span data-stu-id="f1219-894">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="f1219-895">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="f1219-895">New Cmdlets are:</span></span>
    - <span data-ttu-id="f1219-896">”Get-AzIotHubDeviceParent”</span><span class="sxs-lookup"><span data-stu-id="f1219-896">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="f1219-897">”Set-AzIotHubDeviceParent”</span><span class="sxs-lookup"><span data-stu-id="f1219-897">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="f1219-898">Stöd har lagts till för att hantera en enhets överordnade och underordnade relationer.</span><span class="sxs-lookup"><span data-stu-id="f1219-898">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f1219-899">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f1219-899">Az.Monitor</span></span>
* <span data-ttu-id="f1219-900">Utdatavärdet har åtgärdats för ”Get-AzMetricDefinition” [#9714]</span><span class="sxs-lookup"><span data-stu-id="f1219-900">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f1219-901">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f1219-901">Az.Network</span></span>
* <span data-ttu-id="f1219-902">SQL Management SDK har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="f1219-902">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="f1219-903">Ett problem har åtgärdats med namngivningsskillnader i klassen PrivateLinkServiceConnectionState.</span><span class="sxs-lookup"><span data-stu-id="f1219-903">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="f1219-904">Fältet ActionsRequired mappar till ActionRequired.</span><span class="sxs-lookup"><span data-stu-id="f1219-904">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="f1219-905">PublicNetworkAccess har lagts till i ”New-AzSqlServer” och ”Set-AzSqlServer”</span><span class="sxs-lookup"><span data-stu-id="f1219-905">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="f1219-906">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f1219-906">Az.Resources</span></span>
* <span data-ttu-id="f1219-907">Null-referensfel har åtgärdats i ”Get-AzRoleAssignment”</span><span class="sxs-lookup"><span data-stu-id="f1219-907">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="f1219-908">Växlarna ”-Force” och ”-PassThru” är valfria i ”Remove-AzADGroup” [#10849]</span><span class="sxs-lookup"><span data-stu-id="f1219-908">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="f1219-909">Ett problem har åtgärdats som gjorde att ”MailNickname” inte returnerades i ”Remove-AzADGroup” [#11167]</span><span class="sxs-lookup"><span data-stu-id="f1219-909">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="f1219-910">Ett problem har åtgärdats som gjorde att pipe-åtgärden ”Remove-AzADGroup” inte fungerar [#11171]</span><span class="sxs-lookup"><span data-stu-id="f1219-910">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="f1219-911">Ett null-referensfel har åtgärdats i GetAzureRoleAssignmentCommand</span><span class="sxs-lookup"><span data-stu-id="f1219-911">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="f1219-912">Attribut för icke-bakåtkompatibla ändringar har lagts till för kommande ändringar i cmdlets för principer</span><span class="sxs-lookup"><span data-stu-id="f1219-912">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="f1219-913">”Get-AzResourceGroup” har uppdaterats för att utföra taggfiltrering för resursgrupper på serversidan</span><span class="sxs-lookup"><span data-stu-id="f1219-913">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="f1219-914">Utökade Tag-cmdlets stöder -ResourceId</span><span class="sxs-lookup"><span data-stu-id="f1219-914">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="f1219-915">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="f1219-915">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="f1219-916">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="f1219-916">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="f1219-917">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="f1219-917">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="f1219-918">Ny Tag-cmdlet har lagts till</span><span class="sxs-lookup"><span data-stu-id="f1219-918">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="f1219-919">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="f1219-919">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="f1219-920">Flyttade ScopedDeployment från SDK 3.3.0</span><span class="sxs-lookup"><span data-stu-id="f1219-920">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="f1219-921">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f1219-921">Az.Sql</span></span>
* <span data-ttu-id="f1219-922">PublicNetworkAccess har lagts till i ”New-AzSqlServer” och ”Set-AzSqlServer”</span><span class="sxs-lookup"><span data-stu-id="f1219-922">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="f1219-923">Stöd har lagts till för konfiguration av säkerhetskopiering för långsiktig kvarhållning för hanterade databaser</span><span class="sxs-lookup"><span data-stu-id="f1219-923">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="f1219-924">Hämta/ange LTR-princip på en hanterad databas</span><span class="sxs-lookup"><span data-stu-id="f1219-924">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="f1219-925">Hämta LTR-säkerhetskopior efter hanterad databas, hanterad instans eller plats</span><span class="sxs-lookup"><span data-stu-id="f1219-925">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="f1219-926">Ta bort en LTR-säkerhetskopia</span><span class="sxs-lookup"><span data-stu-id="f1219-926">Remove an LTR backup</span></span>
    - <span data-ttu-id="f1219-927">Återställa en LTR-säkerhetskopia för att skapa en ny hanterad databas</span><span class="sxs-lookup"><span data-stu-id="f1219-927">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="f1219-928">MinimalTlsVersion har lagts till för New-AzSqlServer och Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="f1219-928">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="f1219-929">MinimalTlsVersion har lagts till för New-AzSqlInstance och Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="f1219-929">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="f1219-930">SQL SDK-versionen för Az.Network har ändrats</span><span class="sxs-lookup"><span data-stu-id="f1219-930">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f1219-931">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f1219-931">Az.Storage</span></span>
* <span data-ttu-id="f1219-932">AllowProtectedAppendWrite stöds i ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="f1219-932">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="f1219-933">”Set-AzRmStorageContainerImmutabilityPolicy”</span><span class="sxs-lookup"><span data-stu-id="f1219-933">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="f1219-934">Varningsmeddelande har lagts till om icke-bakåtkompatibel ändring för ändring av typen AzureStorageTable i en senare version</span><span class="sxs-lookup"><span data-stu-id="f1219-934">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="f1219-935">”New-AzStorageTable”</span><span class="sxs-lookup"><span data-stu-id="f1219-935">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="f1219-936">”Get-AzStorageTable”</span><span class="sxs-lookup"><span data-stu-id="f1219-936">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f1219-937">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f1219-937">Az.Websites</span></span>
* <span data-ttu-id="f1219-938">Tag-parametern har lagts till för ”New-AzAppServicePlan” och ”Set-AzAppServicePlan”</span><span class="sxs-lookup"><span data-stu-id="f1219-938">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="f1219-939">Stoppa cmdlet-körning om ett undantag uppstår när en anpassad domän läggs till på en webbplats</span><span class="sxs-lookup"><span data-stu-id="f1219-939">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="f1219-940">Stöd har lagts till för att utföra åtgärder för App Services som inte tillhör samma resursgrupp som App Services-planen</span><span class="sxs-lookup"><span data-stu-id="f1219-940">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="f1219-941">Åtkomstbegränsning har tillämpats på WebApp/Function i olika resursgrupper</span><span class="sxs-lookup"><span data-stu-id="f1219-941">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="f1219-942">Ett problem har åtgärdats för att ange anpassade värdnamn för WebAppSlots</span><span class="sxs-lookup"><span data-stu-id="f1219-942">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="f1219-943">3.5.0 – februari 2020</span><span class="sxs-lookup"><span data-stu-id="f1219-943">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="f1219-944">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="f1219-944">Highlights since the last major release</span></span>
* <span data-ttu-id="f1219-945">Uppdaterade telemetri på klientsidan.</span><span class="sxs-lookup"><span data-stu-id="f1219-945">Updated client side telemetry.</span></span>
* <span data-ttu-id="f1219-946">Az.IotHub lade till cmdletar som stöd för att hantera enheter.</span><span class="sxs-lookup"><span data-stu-id="f1219-946">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="f1219-947">Az.SqlVirtualMachine lade till cmdletar för lyssningsfunktion för tillgänglighetsgrupp.</span><span class="sxs-lookup"><span data-stu-id="f1219-947">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f1219-948">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f1219-948">Az.Accounts</span></span>
* <span data-ttu-id="f1219-949">Lade till SubscriptionId, TenantId och körningstid i data för telemetri på klientsidan</span><span class="sxs-lookup"><span data-stu-id="f1219-949">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f1219-950">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f1219-950">Az.Automation</span></span>
* <span data-ttu-id="f1219-951">Åtgärdade skrivfel i exempel 1 i referensdokumentation för ”New-AzAutomationSoftwareUpdateConfiguration”</span><span class="sxs-lookup"><span data-stu-id="f1219-951">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f1219-952">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f1219-952">Az.CognitiveServices</span></span>
* <span data-ttu-id="f1219-953">Uppdaterade SDK till 7.0</span><span class="sxs-lookup"><span data-stu-id="f1219-953">Updated SDK to 7.0</span></span>
* <span data-ttu-id="f1219-954">Förbättrade felmeddelande vid serversvar om tom brödtext</span><span class="sxs-lookup"><span data-stu-id="f1219-954">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f1219-955">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f1219-955">Az.Compute</span></span>
* <span data-ttu-id="f1219-956">Tillät tomt värde för ProximityPlacementGroupId under uppdatering</span><span class="sxs-lookup"><span data-stu-id="f1219-956">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="f1219-957">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f1219-957">Az.FrontDoor</span></span>
* <span data-ttu-id="f1219-958">Lade till cmdlet för att hämta hanterade regeldefinitioner som kan användas i WAF</span><span class="sxs-lookup"><span data-stu-id="f1219-958">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f1219-959">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f1219-959">Az.IotHub</span></span>
* <span data-ttu-id="f1219-960">Lade till stöd för att hantera enheter i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="f1219-960">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="f1219-961">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="f1219-961">New Cmdlets are:</span></span>
    - <span data-ttu-id="f1219-962">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="f1219-962">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="f1219-963">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="f1219-963">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="f1219-964">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="f1219-964">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="f1219-965">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="f1219-965">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f1219-966">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f1219-966">Az.KeyVault</span></span>
* <span data-ttu-id="f1219-967">Åtgärdade duplicerad text för Add-AzKeyVaultKey.md</span><span class="sxs-lookup"><span data-stu-id="f1219-967">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f1219-968">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f1219-968">Az.Monitor</span></span>
* <span data-ttu-id="f1219-969">Åtgärdade beskrivning av cmdleten Get-AzLog.</span><span class="sxs-lookup"><span data-stu-id="f1219-969">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="f1219-970">En ny parameter med namnet ActionGroupId har lagts till i kommandot ”New-AzMetricAlertRuleV2”.</span><span class="sxs-lookup"><span data-stu-id="f1219-970">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="f1219-971">Användaren kan ange ActionGroupId(string) eller ActionGroup(ActivityLogAlertActionGroup).</span><span class="sxs-lookup"><span data-stu-id="f1219-971">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f1219-972">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f1219-972">Az.Network</span></span>
* <span data-ttu-id="f1219-973">Lade till en extra parameteranteckning för parametern ”-EnableProxyProtocol” för cmdleten ”New-AzPrivateLinkService”.</span><span class="sxs-lookup"><span data-stu-id="f1219-973">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="f1219-974">Åtgärdade FilterData-exempel i Start-AzVirtualNetworkGatewayConnectionPacketCapture.md och Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="f1219-974">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="f1219-975">Lade till paketinsamlingsexempel för att samla in alla inre och yttre paket i Start-AzVirtualNetworkGatewayConnectionPacketCapture.md och Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="f1219-975">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="f1219-976">Lade till stöd för Azure-brandväggsprincip på VNet-brandväggar</span><span class="sxs-lookup"><span data-stu-id="f1219-976">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="f1219-977">Inga nya cmdletar har lagts till.</span><span class="sxs-lookup"><span data-stu-id="f1219-977">No new cmdlets are added.</span></span> <span data-ttu-id="f1219-978">Lättar begränsningen för brandväggsprincip på VNet-brandväggar</span><span class="sxs-lookup"><span data-stu-id="f1219-978">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f1219-979">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f1219-979">Az.RecoveryServices</span></span>
* <span data-ttu-id="f1219-980">Lade till stöd för Restore-as-files för SQL-databaser.</span><span class="sxs-lookup"><span data-stu-id="f1219-980">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f1219-981">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f1219-981">Az.Resources</span></span>
* <span data-ttu-id="f1219-982">Omstrukturerade cmdletar för malldistribution</span><span class="sxs-lookup"><span data-stu-id="f1219-982">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="f1219-983">Lade till nya cmdletar för att hantera distributioner i hanteringsgruppen: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f1219-983">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="f1219-984">Lade till nya cmdletar för att hantera distributioner i klientorganisationsområdet: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="f1219-984">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="f1219-985">Omstrukturerade \*-AzDeployment-cmdletar för att fungera specifikt i prenumerationsomfattningen</span><span class="sxs-lookup"><span data-stu-id="f1219-985">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="f1219-986">Skapade alias \*-AzSubscriptionDeployment för \*-AzDeployment-cmdletar</span><span class="sxs-lookup"><span data-stu-id="f1219-986">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="f1219-987">Åtgärdade ”Update-AzADApplication” när parametern ”AvailableToOtherTenants” inte har angetts</span><span class="sxs-lookup"><span data-stu-id="f1219-987">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="f1219-988">Tog bort ApplicationObjectWithoutCredentialParameterSet för att undvika AmbiguousParameterSetException.</span><span class="sxs-lookup"><span data-stu-id="f1219-988">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="f1219-989">Återskapade hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="f1219-989">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="f1219-990">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f1219-990">Az.Sql</span></span>
* <span data-ttu-id="f1219-991">Lade till stöd för återställning till tidpunkt mellan prenumerationer på hanterade instanser.</span><span class="sxs-lookup"><span data-stu-id="f1219-991">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="f1219-992">Lade till stöd för att ändra befintlig SQL Managed Instance-maskinvarugenerering</span><span class="sxs-lookup"><span data-stu-id="f1219-992">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="f1219-993">Åtgärdade ”Update-AzSqlServerVulnerabilityAssessmentSetting”-hjälpexempel: parameter/egenskapsutdata - EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="f1219-993">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="f1219-994">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="f1219-994">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="f1219-995">Lade till cmdletar för lyssningsfunktion för tillgänglighetsgrupp</span><span class="sxs-lookup"><span data-stu-id="f1219-995">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="f1219-996">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="f1219-996">Az.StorageSync</span></span>
* <span data-ttu-id="f1219-997">Uppdaterade teckenuppsättningar som stöds i ”Invoke-AzStorageSyncCompatibilityCheck”.</span><span class="sxs-lookup"><span data-stu-id="f1219-997">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="f1219-998">3.4.0 – februari 2020</span><span class="sxs-lookup"><span data-stu-id="f1219-998">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="f1219-999">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="f1219-999">Highlights since the last major release</span></span>
* <span data-ttu-id="f1219-1000">Första Az.CosmosDB-versionen 0.1.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="f1219-1000">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="f1219-1001">Stöd för Az.Network ConnectionMonitor V2 har lagts till</span><span class="sxs-lookup"><span data-stu-id="f1219-1001">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f1219-1002">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f1219-1002">Az.Accounts</span></span>
* <span data-ttu-id="f1219-1003">Inaktivera automatisk sparande av kontext när AzureRmContext.json inte är tillgängligt</span><span class="sxs-lookup"><span data-stu-id="f1219-1003">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="f1219-1004">Uppdatera referensen till Azure Powershell Common till 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="f1219-1004">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="f1219-1005">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f1219-1005">Az.ApiManagement</span></span>
* <span data-ttu-id="f1219-1006">**Get-AzApiManagementApiSchema** Hämtning av Open-Api-schema som är associerat med ett API har åtgärdats   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="f1219-1006">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="f1219-1007">**New-AzApiManagementProduct**\* och **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="f1219-1007">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="f1219-1008">Åtgärda dokumentation för https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="f1219-1008">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="f1219-1009">**Set-AzApiManagementApi** Exempel för att visa hur ServiceUrl uppdateras med hjälp av cmdleten har lagts till</span><span class="sxs-lookup"><span data-stu-id="f1219-1009">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f1219-1010">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f1219-1010">Az.Compute</span></span>
* <span data-ttu-id="f1219-1011">Begränsa antalet VM-status till 100 för att undvika begränsning när Get-AzVM -Status utförs utan VM-namn.</span><span class="sxs-lookup"><span data-stu-id="f1219-1011">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="f1219-1012">Lägg till cmdleten Update-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="f1219-1012">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="f1219-1013">Lägg till parametrarna EncryptionType och DiskEncryptionSetId i följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="f1219-1013">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="f1219-1014">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="f1219-1014">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="f1219-1015">Lägg till parametern ColocationStatus för cmdleten Get-AzProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="f1219-1015">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f1219-1016">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f1219-1016">Az.DataFactory</span></span>
* <span data-ttu-id="f1219-1017">Uppdatera ADF .Net SDK-versionen till 4.7.0</span><span class="sxs-lookup"><span data-stu-id="f1219-1017">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="f1219-1018">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="f1219-1018">Az.DeploymentManager</span></span>
* <span data-ttu-id="f1219-1019">Lägger till LIST-åtgärder för resurser</span><span class="sxs-lookup"><span data-stu-id="f1219-1019">Adds LIST operations for resources</span></span>
* <span data-ttu-id="f1219-1020">Lägger till funktion för att utföra åtgärder för hälsokontrollsteg</span><span class="sxs-lookup"><span data-stu-id="f1219-1020">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="f1219-1021">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f1219-1021">Az.HDInsight</span></span>
* <span data-ttu-id="f1219-1022">Åtgärda dokumentfel för New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="f1219-1022">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f1219-1023">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f1219-1023">Az.KeyVault</span></span>
* <span data-ttu-id="f1219-1024">Lägg till Name-alias för attributet VaultName så att Remove-AzureKeyVault stämmer överens med New-AzureKeyVault.</span><span class="sxs-lookup"><span data-stu-id="f1219-1024">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f1219-1025">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f1219-1025">Az.Network</span></span>
* <span data-ttu-id="f1219-1026">Nytt exempel har lagts till i Set-AzNetworkWatcherConfigFlowLog.md för att demonstrera ett inaktiveringsscenario för Trafikanalys.</span><span class="sxs-lookup"><span data-stu-id="f1219-1026">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="f1219-1027">Lägg till stöd för att tilldela konfiguration av hanterings-IP till Azure Firewall – ett dedikerat undernät och en offentlig IP som brandväggen använder för dess hanteringstrafik</span><span class="sxs-lookup"><span data-stu-id="f1219-1027">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="f1219-1028">Cmdleten New-AzFirewall har uppdaterats:</span><span class="sxs-lookup"><span data-stu-id="f1219-1028">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="f1219-1029">Parametern -ManagementPublicIpAddress (inte obligatorisk) som accepterar ett offentligt IP-adressobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="f1219-1029">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="f1219-1030">Metoden SetManagementIpConfiguration har lagts till för brandväggsobjekt – kräver ett undernät och en offentlig IP-adress som indata – undernätets namn måste vara ”AzureFirewallManagementSubnet”</span><span class="sxs-lookup"><span data-stu-id="f1219-1030">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="f1219-1031">Exempel för Get-AzNetworkSecurityGroup har korrigerats så att exempel visas för NSG:er i stället för nätverksgränssnitt.</span><span class="sxs-lookup"><span data-stu-id="f1219-1031">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="f1219-1032">Ett skrivfel har åtgärdats i kommandot New-AzVpnSite som hindrade kompletteraren för resurs-ID från att fylla i en parameter.</span><span class="sxs-lookup"><span data-stu-id="f1219-1032">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="f1219-1033">Stöd för Url-konfiguration i åtgärdsuppsättningen för omskrivningsregler i Application Gateway har lagts till</span><span class="sxs-lookup"><span data-stu-id="f1219-1033">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="f1219-1034">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="f1219-1034">New cmdlets added:</span></span>
        - <span data-ttu-id="f1219-1035">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="f1219-1035">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="f1219-1036">Cmdletar har uppdaterats med den valfria parametern -UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="f1219-1036">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="f1219-1037">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="f1219-1037">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="f1219-1038">Lägg till stöd för resurser för NetworkWatcher ConnectionMonitor version 2</span><span class="sxs-lookup"><span data-stu-id="f1219-1038">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f1219-1039">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f1219-1039">Az.PolicyInsights</span></span>
* <span data-ttu-id="f1219-1040">Stöd för utvärdering av efterlevnad innan fastställande av vilken resurs som ska åtgärdas</span><span class="sxs-lookup"><span data-stu-id="f1219-1040">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="f1219-1041">Lägg till parametern ”-ResourceDiscoverMode” för Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="f1219-1041">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="f1219-1042">Lägg till cmdleten Get-AzPolicyMetadata för att hämta resurser för principmetadata</span><span class="sxs-lookup"><span data-stu-id="f1219-1042">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="f1219-1043">Get-AzPolicyState och Get-AzPolicyStateSummary för API-versionen 2019-10-01 har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="f1219-1043">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f1219-1044">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f1219-1044">Az.RecoveryServices</span></span>
* <span data-ttu-id="f1219-1045">Azure Site Recovery-stöd för att ta bort en replikerad disk.</span><span class="sxs-lookup"><span data-stu-id="f1219-1045">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="f1219-1046">Tillagt Azure Backup-stöd för att lägga till taggar när ett Recovery Services-valv skapas.</span><span class="sxs-lookup"><span data-stu-id="f1219-1046">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f1219-1047">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f1219-1047">Az.Resources</span></span>
* <span data-ttu-id="f1219-1048">Gör -Scope valfritt i cmdletarna \*-AzPolicyAssignment med standardinställning till kontextprenumeration</span><span class="sxs-lookup"><span data-stu-id="f1219-1048">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="f1219-1049">Lägg till exempel på att skapa ADServicePrincipal med lösenord och nyckelautentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="f1219-1049">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="f1219-1050">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f1219-1050">Az.Sql</span></span>
<span data-ttu-id="f1219-1051">Åtgärda cmdleten New-AzSqlDatabaseSecondary så att existensen PartnerDatabaseName kontrolleras i stället för existensen DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="f1219-1051">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f1219-1052">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f1219-1052">Az.Storage</span></span>
* <span data-ttu-id="f1219-1053">Stöd för angivning av krypteringsnyckeltyp för Tabell/kö i Skapa lagringskonto</span><span class="sxs-lookup"><span data-stu-id="f1219-1053">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="f1219-1054">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f1219-1054">New-AzStorageAccount</span></span>
* <span data-ttu-id="f1219-1055">Visa RequestId när StorageException inte har ExtendedErrorInformation</span><span class="sxs-lookup"><span data-stu-id="f1219-1055">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="f1219-1056">Åtgärda exempel 6 för cmdleten Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="f1219-1056">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f1219-1057">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f1219-1057">Az.Websites</span></span>
* <span data-ttu-id="f1219-1058">Set-AzWebapp och Set-AzWebappSlot stöder egenskaperna AlwaysOn, MinTls och FtpsState</span><span class="sxs-lookup"><span data-stu-id="f1219-1058">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="f1219-1059">Åtgärdar problemet där inställning av HttpsOnly samtidigt som AppservicePlan ändrades med det enskilda kommandot Set-AzWebApp återställde HttpsOnly till standardvärdet</span><span class="sxs-lookup"><span data-stu-id="f1219-1059">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="f1219-1060">3.3.0 – januari 2020</span><span class="sxs-lookup"><span data-stu-id="f1219-1060">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f1219-1061">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f1219-1061">Az.Accounts</span></span>
* <span data-ttu-id="f1219-1062">Nu stöder Add-AzEnvironment och Set-AzEnvironment parametrarna AzureAttestationServiceEndpointResourceId och AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="f1219-1062">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="f1219-1063">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f1219-1063">Az.Cdn</span></span>
* <span data-ttu-id="f1219-1064">Information om felsvar visas i New-AzCdnEndpoint-cmdleten</span><span class="sxs-lookup"><span data-stu-id="f1219-1064">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f1219-1065">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f1219-1065">Az.Compute</span></span>
* <span data-ttu-id="f1219-1066">Set-AzVMCustomScriptExtension-cmdleten har åtgärdats för en virtuell dator med hanterad OD-disk som inte har någon operativsystemprofil.</span><span class="sxs-lookup"><span data-stu-id="f1219-1066">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="f1219-1067">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="f1219-1067">Az.ContainerInstance</span></span>
* <span data-ttu-id="f1219-1068">Parameternamn som används med New-AzContainerGroup-exempel har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="f1219-1068">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="f1219-1069">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="f1219-1069">Az.DataBoxEdge</span></span>
* <span data-ttu-id="f1219-1070">Cmdleten ”Get-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="f1219-1070">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="f1219-1071">Hämta gränslagringscontainern</span><span class="sxs-lookup"><span data-stu-id="f1219-1071">Get the Edge Storage Container</span></span>
* <span data-ttu-id="f1219-1072">Cmdleten ”New-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="f1219-1072">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="f1219-1073">Skapa en ny gränslagringscontainer</span><span class="sxs-lookup"><span data-stu-id="f1219-1073">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="f1219-1074">Cmdleten ”Remove-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="f1219-1074">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="f1219-1075">Ta bort gränslagringscontainern</span><span class="sxs-lookup"><span data-stu-id="f1219-1075">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="f1219-1076">Cmdleten ”Invoke-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="f1219-1076">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="f1219-1077">Anropa åtgärd för att uppdatera data i gränslagringscontainer</span><span class="sxs-lookup"><span data-stu-id="f1219-1077">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="f1219-1078">Cmdleten ”Get-AzDataBoxEdgeStorageAccount” har lagts till</span><span class="sxs-lookup"><span data-stu-id="f1219-1078">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="f1219-1079">Hämta gränslagringskontot</span><span class="sxs-lookup"><span data-stu-id="f1219-1079">Get the Edge Storage Account</span></span>
* <span data-ttu-id="f1219-1080">Cmdleten ”New-AzDataBoxEdgeStorageAccount” har lagts till</span><span class="sxs-lookup"><span data-stu-id="f1219-1080">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="f1219-1081">Skapa ett nytt gränslagringskonto</span><span class="sxs-lookup"><span data-stu-id="f1219-1081">Create new Edge Storage Account</span></span>
* <span data-ttu-id="f1219-1082">Cmdleten ”Remove-AzDataBoxEdgeStorageAccount” har lagts till</span><span class="sxs-lookup"><span data-stu-id="f1219-1082">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="f1219-1083">Ta bort gränslagringskontot</span><span class="sxs-lookup"><span data-stu-id="f1219-1083">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="f1219-1084">Anropa cmdleten ”Invoke-AzDataBoxEdgeShare”</span><span class="sxs-lookup"><span data-stu-id="f1219-1084">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="f1219-1085">Anropa åtgärd för att uppdatera resursdata</span><span class="sxs-lookup"><span data-stu-id="f1219-1085">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="f1219-1086">Cmdleten ”Set-AzDataBoxEdgeStorageAccountCredential” har lagts till</span><span class="sxs-lookup"><span data-stu-id="f1219-1086">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="f1219-1087">Ange autentiseringsuppgifter för az databoxedge-lagringskonto</span><span class="sxs-lookup"><span data-stu-id="f1219-1087">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f1219-1088">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f1219-1088">Az.DataFactory</span></span>
* <span data-ttu-id="f1219-1089">Lägg till AutoUpdateETA-, LatestVersion-, PushedVersion-, TaskQueueId- och VersionStatus-egenskaper för Get-AzDataFactoryV2IntegrationRuntime-cmd</span><span class="sxs-lookup"><span data-stu-id="f1219-1089">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="f1219-1090">Uppdatera ADF .Net SDK-versionen till 4.6.0</span><span class="sxs-lookup"><span data-stu-id="f1219-1090">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="f1219-1091">Lägg till parametern ”PublicIPs” för ”Set-AzureRmDataFactoryV2IntegrationRuntime”-cmd så att Azure-SSIS IR kan skapas med statiska offentliga IP-adresser.</span><span class="sxs-lookup"><span data-stu-id="f1219-1091">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="f1219-1092">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="f1219-1092">Az.DevTestLabs</span></span>
* <span data-ttu-id="f1219-1093">Ta bort den brutna länken i Get-AzDtlAllowedVMSizesPolicy.md</span><span class="sxs-lookup"><span data-stu-id="f1219-1093">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f1219-1094">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f1219-1094">Az.EventHub</span></span>
* <span data-ttu-id="f1219-1095">Korrigering av problem 10634: Åtgärda referensen till null-objekt för eventhubnamespace-borttagning</span><span class="sxs-lookup"><span data-stu-id="f1219-1095">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="f1219-1096">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f1219-1096">Az.HDInsight</span></span>
* <span data-ttu-id="f1219-1097">Åtgärda Invoke-AzHDInsightHiveJob.md-fel.</span><span class="sxs-lookup"><span data-stu-id="f1219-1097">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="f1219-1098">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="f1219-1098">Az.MachineLearning</span></span>
* <span data-ttu-id="f1219-1099">Nedanstående cmdletar har tagits bort eftersom MachineLearningCompute inte längre är tillgängligt</span><span class="sxs-lookup"><span data-stu-id="f1219-1099">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="f1219-1100">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="f1219-1100">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="f1219-1101">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="f1219-1101">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="f1219-1102">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="f1219-1102">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="f1219-1103">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="f1219-1103">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="f1219-1104">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="f1219-1104">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="f1219-1105">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="f1219-1105">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="f1219-1106">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="f1219-1106">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f1219-1107">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f1219-1107">Az.Network</span></span>
* <span data-ttu-id="f1219-1108">Uppgradera beroende av Microsoft.Azure.Management.Sql från 1.36-preview till 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="f1219-1108">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f1219-1109">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f1219-1109">Az.RecoveryServices</span></span>
* <span data-ttu-id="f1219-1110">Ändrat Azure Site Recovery-stöd för krypterade vilande data på virtuella datorer med hanterade diskar med kundhanterade nycklar för Azure till Azure-providern.</span><span class="sxs-lookup"><span data-stu-id="f1219-1110">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="f1219-1111">Azure Site Recovery-stöd för att ange ID för diskkrypteringsuppsättning som valfri inmatning för aktivering av skydd för VMware till Azure.</span><span class="sxs-lookup"><span data-stu-id="f1219-1111">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="f1219-1112">Azure Site Recovery-stöd för att ange ID för diskkrypteringsuppsättning som valfri inmatning på disknivå för aktivering av skydd för VMware till Azure.</span><span class="sxs-lookup"><span data-stu-id="f1219-1112">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="f1219-1113">Azure Site Recovery-stöd för att uppdatera replikeringsskyddade objekt med mappning för diskkrypteringsuppsättning för HyperV till Azure.</span><span class="sxs-lookup"><span data-stu-id="f1219-1113">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f1219-1114">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f1219-1114">Az.Resources</span></span>
* <span data-ttu-id="f1219-1115">Åtgärda ett fel i hjälpdokument för ”Remove-AzTag”.</span><span class="sxs-lookup"><span data-stu-id="f1219-1115">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="f1219-1116">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f1219-1116">Az.Sql</span></span>
* <span data-ttu-id="f1219-1117">Åtgärda funktioner i cmdletar för att ange baslinjen för sårbarhetsbedömning för arbete med huvuddatabasen för Azure-databasen och begränsa den för systemdatabaser på hanterade instanser.</span><span class="sxs-lookup"><span data-stu-id="f1219-1117">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="f1219-1118">Åtgärda ett fel när en redundansgrupp för en SQL-instans skapas</span><span class="sxs-lookup"><span data-stu-id="f1219-1118">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="f1219-1119">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="f1219-1119">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="f1219-1120">Lägg till DR som en ny giltig licenstyp</span><span class="sxs-lookup"><span data-stu-id="f1219-1120">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f1219-1121">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f1219-1121">Az.Storage</span></span>
* <span data-ttu-id="f1219-1122">Lägg till varningsmeddelande om icke-bakåtkompatibel ändring för DefaultAction-värdeändring i en framtida version</span><span class="sxs-lookup"><span data-stu-id="f1219-1122">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="f1219-1123">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="f1219-1123">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="f1219-1124">Stöd för att hämta lagringskontots senaste synkroniseringstid genom att köra get-AzureRMStorageAccount med parametern -IncludeGeoReplicationStats</span><span class="sxs-lookup"><span data-stu-id="f1219-1124">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="f1219-1125">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f1219-1125">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="f1219-1126">3.2.0 – December 2019</span><span class="sxs-lookup"><span data-stu-id="f1219-1126">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="f1219-1127">Allmänt</span><span class="sxs-lookup"><span data-stu-id="f1219-1127">General</span></span>
* <span data-ttu-id="f1219-1128">Uppdatera referenser i .psd1 för att använda relativa sökvägar för alla moduler</span><span class="sxs-lookup"><span data-stu-id="f1219-1128">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f1219-1129">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f1219-1129">Az.Accounts</span></span>
* <span data-ttu-id="f1219-1130">Ange rätt UserAgent för telemetri på klientsidan för Az 4.0 preview</span><span class="sxs-lookup"><span data-stu-id="f1219-1130">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="f1219-1131">Visa användarvänligt felmeddelande när kontexten är null i Az 4.0 preview</span><span class="sxs-lookup"><span data-stu-id="f1219-1131">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="f1219-1132">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="f1219-1132">Az.Batch</span></span>
* <span data-ttu-id="f1219-1133">Korrigera problem [#10602](https://github.com/Azure/azure-powershell/issues/10602), där **New-AzBatchPool** skickade VirtualMachineConfiguration.ContainerConfiguration eller VirtualMachineConfiguration.DataDisks på ett felaktigt sätt till servern.</span><span class="sxs-lookup"><span data-stu-id="f1219-1133">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f1219-1134">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f1219-1134">Az.DataFactory</span></span>
* <span data-ttu-id="f1219-1135">Uppdatera ADF .Net SDK-versionen till 4.5.0</span><span class="sxs-lookup"><span data-stu-id="f1219-1135">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="f1219-1136">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f1219-1136">Az.FrontDoor</span></span>
* <span data-ttu-id="f1219-1137">Stöd har lagts till för undantag för hanterade regler för brandväggen för webbaserade program</span><span class="sxs-lookup"><span data-stu-id="f1219-1137">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="f1219-1138">Lägg till SocketAddr för automatisk komplettering</span><span class="sxs-lookup"><span data-stu-id="f1219-1138">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="f1219-1139">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="f1219-1139">Az.HealthcareApis</span></span>
* <span data-ttu-id="f1219-1140">Undantagshantering</span><span class="sxs-lookup"><span data-stu-id="f1219-1140">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f1219-1141">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f1219-1141">Az.KeyVault</span></span>
* <span data-ttu-id="f1219-1142">Åtgärdat fel vid åtkomst av värde som kanske inte har angetts</span><span class="sxs-lookup"><span data-stu-id="f1219-1142">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="f1219-1143">Hantering av ECC-certifikat (Elliptic Curve Cryptography)</span><span class="sxs-lookup"><span data-stu-id="f1219-1143">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="f1219-1144">Stöd har lagts till för att ange kurvan för certifikatprinciper</span><span class="sxs-lookup"><span data-stu-id="f1219-1144">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f1219-1145">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f1219-1145">Az.Monitor</span></span>
* <span data-ttu-id="f1219-1146">Lägger till valfritt argument i kommandot Lägg till diagnostikinställningar.</span><span class="sxs-lookup"><span data-stu-id="f1219-1146">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="f1219-1147">Ett växelargument som om det finns visar att exporten till Log Analytics måste ske till ett fast schema (kallas även</span><span class="sxs-lookup"><span data-stu-id="f1219-1147">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="f1219-1148">dedikerad, datatyp)</span><span class="sxs-lookup"><span data-stu-id="f1219-1148">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f1219-1149">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f1219-1149">Az.Network</span></span>
* <span data-ttu-id="f1219-1150">Stöd för IpGroups i program-, NAT- och nätverksregler för Azure Firewall.</span><span class="sxs-lookup"><span data-stu-id="f1219-1150">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f1219-1151">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f1219-1151">Az.Resources</span></span>
* <span data-ttu-id="f1219-1152">Åtgärda ett problem där malldistributionen inte kan läsa en mallparameter om dess namn står i konflikt med ett inbyggt parameternamn.</span><span class="sxs-lookup"><span data-stu-id="f1219-1152">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="f1219-1153">Uppdaterade princip-cmdletar för att använda den nya API-versionen 2019-09-01 som introducerar grupperingsstöd inom principuppsättningsdefinitioner.</span><span class="sxs-lookup"><span data-stu-id="f1219-1153">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="f1219-1154">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f1219-1154">Az.Sql</span></span>
* <span data-ttu-id="f1219-1155">Uppgraderad funktion för att skapa lagring i automatisk aktivering av sårbarhetsbedömning till StorageV2</span><span class="sxs-lookup"><span data-stu-id="f1219-1155">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f1219-1156">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f1219-1156">Az.Storage</span></span>
* <span data-ttu-id="f1219-1157">Stöd för generering av blob/container-identitetsbaserad SAS-token med lagringskontextbaserad på OAuth-autentisering</span><span class="sxs-lookup"><span data-stu-id="f1219-1157">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="f1219-1158">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="f1219-1158">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="f1219-1159">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="f1219-1159">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="f1219-1160">Stöd för återkallning av användardelegeringsnycklar för lagringskonto för att återkalla alla SAS-token</span><span class="sxs-lookup"><span data-stu-id="f1219-1160">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="f1219-1161">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="f1219-1161">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="f1219-1162">Uppgradera till Microsoft.Azure.Management.Storage 14.2.0 för att stödja den nya API-versionen 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="f1219-1162">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="f1219-1163">Stöd för QuotaGiB (resurskvot i Gibibye) för värden över 5120 i hanteringsplanet för cmdletar för filresurser och parameteraliaset. Quota har också lagts till för parametern ”QuotaGiB”.</span><span class="sxs-lookup"><span data-stu-id="f1219-1163">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="f1219-1164">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="f1219-1164">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="f1219-1165">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="f1219-1165">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="f1219-1166">Lägg till parameteraliaset QuotaGiB i parametern Quota</span><span class="sxs-lookup"><span data-stu-id="f1219-1166">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="f1219-1167">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="f1219-1167">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="f1219-1168">Åtgärda problemet att Set-AzStorageContainerAcl kan rensa den lagrade åtkomstprincipen</span><span class="sxs-lookup"><span data-stu-id="f1219-1168">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="f1219-1169">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="f1219-1169">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="f1219-1170">3.1.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="f1219-1170">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="f1219-1171">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="f1219-1171">Highlights since the last major release</span></span>
* <span data-ttu-id="f1219-1172">Az.DataBoxEdge 1.0.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="f1219-1172">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="f1219-1173">Az.SqlVirtualMachine 1.0.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="f1219-1173">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f1219-1174">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f1219-1174">Az.Compute</span></span>
* <span data-ttu-id="f1219-1175">Funktion för att använda en virtuell dator igen</span><span class="sxs-lookup"><span data-stu-id="f1219-1175">VM Reapply feature</span></span>
    - <span data-ttu-id="f1219-1176">Lägg till parameter för att använda igen till cmdleten Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="f1219-1176">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="f1219-1177">Funktionen AutomaticRepairs i VM-skalningsuppsättningar:</span><span class="sxs-lookup"><span data-stu-id="f1219-1177">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="f1219-1178">Lägg till parametrarna EnableAutomaticRepair, AutomaticRepairGracePeriod och AutomaticRepairMaxInstanceRepairsPercent till följande cmdletar:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f1219-1178">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="f1219-1179">Stöd för galleriavbildningar i flera klientorganisationer för New-AzVM</span><span class="sxs-lookup"><span data-stu-id="f1219-1179">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="f1219-1180">Lägg till "Spot" till argumentslutföraren i prioritetsparametern i cmdletarna New-AzVM, New-AzVMConfig och New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f1219-1180">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="f1219-1181">Lägg till parametrarna DiskIOPSReadWrite och DiskMBpsReadWrite till cmdleten Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="f1219-1181">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="f1219-1182">Ändra parametern SourceImageId för cmdleten New-AzGalleryImageVersion till valfri</span><span class="sxs-lookup"><span data-stu-id="f1219-1182">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="f1219-1183">Lägg till parametrarna OSDiskImage och DataDiskImage till cmdleten New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="f1219-1183">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="f1219-1184">Lägg till parametern HyperVGeneration till cmdleten New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="f1219-1184">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="f1219-1185">Lägg till parametern SkipExtensionsOnOverprovisionedVMs till cmdletarna New-AzVmss, New-AzVmssConfig och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f1219-1185">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="f1219-1186">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="f1219-1186">Az.DataBoxEdge</span></span>
* <span data-ttu-id="f1219-1187">Cmdleten `Get-AzDataBoxEdgeOrder` har lagts till</span><span class="sxs-lookup"><span data-stu-id="f1219-1187">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="f1219-1188">Hämta ordning</span><span class="sxs-lookup"><span data-stu-id="f1219-1188">Get the Order</span></span>
* <span data-ttu-id="f1219-1189">Cmdleten `New-AzDataBoxEdgeOrder` har lagts till</span><span class="sxs-lookup"><span data-stu-id="f1219-1189">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="f1219-1190">Skapa ny ordning</span><span class="sxs-lookup"><span data-stu-id="f1219-1190">Create new Order</span></span>
* <span data-ttu-id="f1219-1191">Cmdleten `Remove-AzDataBoxEdgeOrder` har lagts till</span><span class="sxs-lookup"><span data-stu-id="f1219-1191">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="f1219-1192">Ta bort ordning</span><span class="sxs-lookup"><span data-stu-id="f1219-1192">Remove the Order</span></span>
* <span data-ttu-id="f1219-1193">Cmdleten `New-AzDataBoxEdgeShare` har ändrats</span><span class="sxs-lookup"><span data-stu-id="f1219-1193">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="f1219-1194">Nu skapas lokal filresurs</span><span class="sxs-lookup"><span data-stu-id="f1219-1194">Now creates Local Share</span></span>
* <span data-ttu-id="f1219-1195">Cmdleten `Set-AzDataBoxEdgeRole` har lagts till</span><span class="sxs-lookup"><span data-stu-id="f1219-1195">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="f1219-1196">Nu kan IotRole mappas till filresursen</span><span class="sxs-lookup"><span data-stu-id="f1219-1196">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="f1219-1197">Cmdleten `Invoke-AzDataBoxEdgeDevice` har lagts till</span><span class="sxs-lookup"><span data-stu-id="f1219-1197">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="f1219-1198">Anropa genomsökningsuppdatering, ladda ned uppdatering, installera uppdateringar på enheten</span><span class="sxs-lookup"><span data-stu-id="f1219-1198">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="f1219-1199">Cmdleten `Get-AzDataBoxEdgeTrigger` har lagts till</span><span class="sxs-lookup"><span data-stu-id="f1219-1199">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="f1219-1200">Hämtar information om utlösare</span><span class="sxs-lookup"><span data-stu-id="f1219-1200">Gets the information about Triggers</span></span>
* <span data-ttu-id="f1219-1201">Cmdleten `New-AzDataBoxEdgeTrigger` har lagts till</span><span class="sxs-lookup"><span data-stu-id="f1219-1201">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="f1219-1202">Skapa nya utlösare</span><span class="sxs-lookup"><span data-stu-id="f1219-1202">Create new Triggers</span></span>
* <span data-ttu-id="f1219-1203">Cmdleten `Remove-AzDataBoxEdgeTrigger` har lagts till</span><span class="sxs-lookup"><span data-stu-id="f1219-1203">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="f1219-1204">Ta bort utlösare</span><span class="sxs-lookup"><span data-stu-id="f1219-1204">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f1219-1205">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f1219-1205">Az.DataFactory</span></span>
* <span data-ttu-id="f1219-1206">Uppdatera ADF .Net SDK-versionen till 4.4.0</span><span class="sxs-lookup"><span data-stu-id="f1219-1206">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="f1219-1207">Lägg till parametern ExpressCustomSetup för kommandot Set-AzureRmDataFactoryV2IntegrationRuntime för att aktivera installationskonfigurationer och komponenter från tredje part utan anpassat konfigurationsskript.</span><span class="sxs-lookup"><span data-stu-id="f1219-1207">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f1219-1208">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f1219-1208">Az.DataLakeStore</span></span>
* <span data-ttu-id="f1219-1209">Uppdatera dokumentation för Get-AzDataLakeStoreDeletedItem och Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="f1219-1209">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f1219-1210">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f1219-1210">Az.EventHub</span></span>
* <span data-ttu-id="f1219-1211">Korrigering av problem #10301: Korrigera datumformat för SAS-token</span><span class="sxs-lookup"><span data-stu-id="f1219-1211">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="f1219-1212">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f1219-1212">Az.FrontDoor</span></span>
* <span data-ttu-id="f1219-1213">Lägg till parametern MinimumTlsVersion till Enable-AzFrontDoorCustomDomainHttps och New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="f1219-1213">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="f1219-1214">Lägg till parametrarna HealthProbeMethod och EnabledState till New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="f1219-1214">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="f1219-1215">Lägg till en ny cmdlet för att skapa BackendPoolsSettings-objekt som passar i skapande/uppdatering av Front Door</span><span class="sxs-lookup"><span data-stu-id="f1219-1215">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="f1219-1216">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="f1219-1216">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f1219-1217">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f1219-1217">Az.Network</span></span>
* <span data-ttu-id="f1219-1218">Ändra alternativexemplen Start-AzVirtualNetworkGatewayConnectionPacketCapture.md och Start-AzVirtualnetworkGatewayPacketCapture.md för FilterData.</span><span class="sxs-lookup"><span data-stu-id="f1219-1218">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="f1219-1219">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="f1219-1219">Az.PrivateDns</span></span>
* <span data-ttu-id="f1219-1220">Uppdaterade PrivateDns .NET SDK till version 1.0.0</span><span class="sxs-lookup"><span data-stu-id="f1219-1220">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f1219-1221">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f1219-1221">Az.RecoveryServices</span></span>
* <span data-ttu-id="f1219-1222">Stöd för att välja disktyp vid aktivering av skydd i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="f1219-1222">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="f1219-1223">Korrigering av bugg för åtgärdsredigering av återställningsplan i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="f1219-1223">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="f1219-1224">Återställningsstöd för att godkänna filestream-databaser i Azure Backup SQL.</span><span class="sxs-lookup"><span data-stu-id="f1219-1224">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="f1219-1225">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="f1219-1225">Az.RedisCache</span></span>
* <span data-ttu-id="f1219-1226">Parametern MinimumTlsVersion har lagts till i cmdletarna New-AzRedisCache och Set-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="f1219-1226">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="f1219-1227">Dessutom har MinimumTlsVersion lagts till i utdata för cmdleten Get-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="f1219-1227">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="f1219-1228">Verifiering har lagts till på parametern -Size i cmdletarna Set-AzRedisCache och New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="f1219-1228">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="f1219-1229">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f1219-1229">Az.Resources</span></span>
- <span data-ttu-id="f1219-1230">Uppdaterade policy-cmdletar för att använda den nya API-versionen 2019-06-01 som har en ny EnforcementMode-egenskap i policytilldelningen.</span><span class="sxs-lookup"><span data-stu-id="f1219-1230">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="f1219-1231">Uppdaterade hjälpexempel för skapandet av policydefinition</span><span class="sxs-lookup"><span data-stu-id="f1219-1231">Updated create policy definition help example</span></span>
- <span data-ttu-id="f1219-1232">Åtgärda bugg i Remove-AZADServicePrincipal -ServicePrincipalName, utlös null-referens när tjänstens huvudnamn inte hittas.</span><span class="sxs-lookup"><span data-stu-id="f1219-1232">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="f1219-1233">Åtgärda bugg i New-AZADServicePrincipal, utlös null-referens när klientorganisationen inte har någon prenumeration.</span><span class="sxs-lookup"><span data-stu-id="f1219-1233">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="f1219-1234">Ändra New-AzAdServicePrincipal för att endast lägga till autentiseringsuppgifter för det associerade programmet.</span><span class="sxs-lookup"><span data-stu-id="f1219-1234">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="f1219-1235">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f1219-1235">Az.Sql</span></span>
* <span data-ttu-id="f1219-1236">Stöd har lagts till för databasen ReadReplicaCount.</span><span class="sxs-lookup"><span data-stu-id="f1219-1236">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="f1219-1237">Korrigerade Set-AzSqlDatabase när zonredundans inte har angetts</span><span class="sxs-lookup"><span data-stu-id="f1219-1237">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="f1219-1238">3.0.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="f1219-1238">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="f1219-1239">Allmänt</span><span class="sxs-lookup"><span data-stu-id="f1219-1239">General</span></span>
* <span data-ttu-id="f1219-1240">Az. PrivateDns 1.0.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="f1219-1240">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f1219-1241">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f1219-1241">Az.Accounts</span></span>
* <span data-ttu-id="f1219-1242">Lägg till ett utfasningsmeddelande för aliaset Resolve-error.</span><span class="sxs-lookup"><span data-stu-id="f1219-1242">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="f1219-1243">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="f1219-1243">Az.Advisor</span></span>
* <span data-ttu-id="f1219-1244">Den nya kategorin Operational Excellence har lagts till i cmdleten Get-AzAdvisorRecommendation.</span><span class="sxs-lookup"><span data-stu-id="f1219-1244">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="f1219-1245">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="f1219-1245">Az.Batch</span></span>
* <span data-ttu-id="f1219-1246">`CoreQuota` på `BatchAccountContext` har bytt namn till `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="f1219-1246">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="f1219-1247">Det finns även en ny `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="f1219-1247">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="f1219-1248">Detta påverkar **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="f1219-1248">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="f1219-1249">**New-AzBatchTask** `-ResourceFile`-parametern tar nu en samling `PSResourceFile`-objekt som kan skapas med hjälp av den nya cmdleten **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="f1219-1249">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="f1219-1250">Ny **New-AzBatchResourceFile**-cmdlet för att skapa `PSResourceFile`-objekt.</span><span class="sxs-lookup"><span data-stu-id="f1219-1250">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="f1219-1251">Dessa kan tillhandahållas till **New-AzBatchTask** på `-ResourceFile`-parametern.</span><span class="sxs-lookup"><span data-stu-id="f1219-1251">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="f1219-1252">Detta stöder två nya typer av resursfiler förutom det befintliga sättet med `HttpUrl`:</span><span class="sxs-lookup"><span data-stu-id="f1219-1252">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="f1219-1253">`AutoStorageContainerName`-baserade resursfiler laddar ned en hel container för automatisk lagring till Batch-noden.</span><span class="sxs-lookup"><span data-stu-id="f1219-1253">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="f1219-1254">`StorageContainerUrl`-baserade resursfiler laddar ned containern som anges i webbadressen till Batch-noden.</span><span class="sxs-lookup"><span data-stu-id="f1219-1254">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="f1219-1255">Tog bort egenskapen `ApplicationPackages` för `PSApplication` som returnerades av **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="f1219-1255">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="f1219-1256">Specifika paket i ett program kan nu hämtas med hjälp av **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="f1219-1256">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="f1219-1257">Till exempel: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="f1219-1257">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="f1219-1258">Bytt namn på `ApplicationId` till `ApplicationName` på **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** och **Set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="f1219-1258">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="f1219-1259">`ApplicationId` är nu ett alias för `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="f1219-1259">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="f1219-1260">Ny `PSWindowsUserConfiguration`-egenskap till `PSUserAccount` lades till.</span><span class="sxs-lookup"><span data-stu-id="f1219-1260">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="f1219-1261">Bytte namn på `Version` till `Name` på `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="f1219-1261">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="f1219-1262">Bytte namn på `BlobSource` till `HttpUrl` på `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="f1219-1262">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="f1219-1263">Tog bort egenskapen `OSDisk` från `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="f1219-1263">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="f1219-1264">Tog bort **Set-AzBatchPoolOSVersion**.</span><span class="sxs-lookup"><span data-stu-id="f1219-1264">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="f1219-1265">Den här åtgärden stöds inte längre.</span><span class="sxs-lookup"><span data-stu-id="f1219-1265">This operation is no longer supported.</span></span>
* <span data-ttu-id="f1219-1266">`TargetOSVersion` har tagits bort från `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="f1219-1266">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="f1219-1267">Bytte namn på `CurrentOSVersion` till `OSVersion` på `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="f1219-1267">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="f1219-1268">`DataEgressGiB` och `DataIngressGiB` har tagits bort från `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="f1219-1268">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="f1219-1269">Tog bort **Get-AzBatchNodeAgentSku** och ersatte det med **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="f1219-1269">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="f1219-1270">**Get-AzBatchSupportedImage** returnerar samma data som **Get-AzBatchNodeAgentSku** men i ett mer användarvänligt format.</span><span class="sxs-lookup"><span data-stu-id="f1219-1270">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="f1219-1271">Nya icke-verifierade avbildningar returneras nu också.</span><span class="sxs-lookup"><span data-stu-id="f1219-1271">New non-verified images are also now returned.</span></span> <span data-ttu-id="f1219-1272">Ytterligare information om `Capabilities` och `BatchSupportEndOfLife` för varje avbildning inkluderas också.</span><span class="sxs-lookup"><span data-stu-id="f1219-1272">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="f1219-1273">Lade till möjlighet att montera fjärrfilsystem på varje nod i en pool via den nya parametern `MountConfiguration` för **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="f1219-1273">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="f1219-1274">Har nu stöd för nätverkssäkerhetsregler som blockerar nätverksåtkomst till en pool baserat på källportens trafik.</span><span class="sxs-lookup"><span data-stu-id="f1219-1274">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="f1219-1275">Detta görs via egenskapen `SourcePortRanges` på `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="f1219-1275">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="f1219-1276">När du kör en container stöder nu Batch körningen av uppgiften i arbetskatalogen för containern eller i arbetskatalogen för Batch-uppgiften.</span><span class="sxs-lookup"><span data-stu-id="f1219-1276">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="f1219-1277">Detta styrs av egenskapen `WorkingDirectory` på `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="f1219-1277">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="f1219-1278">Lade till en funktion för att ange en samling av offentliga IP-adresser på `PSNetworkConfiguration` via den nya egenskapen `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="f1219-1278">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="f1219-1279">Detta garanterar att noderna i poolen har en IP-adress från listan över IP-adresser som tillhandahållits av användare.</span><span class="sxs-lookup"><span data-stu-id="f1219-1279">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="f1219-1280">Om inget värde anges är standardvärdet för `WaitForSuccess` på `PSSTartTask` nu `$True` (var tidigare `$False`).</span><span class="sxs-lookup"><span data-stu-id="f1219-1280">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="f1219-1281">Om inget värde anges är standardvärdet för `Scope` på `PSAutoUserSpecification` nu `Pool` (var tidigare `Task` på Windows och `Pool` på Linux).</span><span class="sxs-lookup"><span data-stu-id="f1219-1281">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="f1219-1282">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f1219-1282">Az.Cdn</span></span>
* <span data-ttu-id="f1219-1283">Introducerade UrlRewriteAction och CacheKeyQueryStringAction till RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="f1219-1283">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="f1219-1284">Åtgärdade flera buggar, som saknade indata för ”väljare” i cmdleten New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="f1219-1284">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f1219-1285">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f1219-1285">Az.Compute</span></span>
* <span data-ttu-id="f1219-1286">Funktion för diskkrypteringsuppsättning</span><span class="sxs-lookup"><span data-stu-id="f1219-1286">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="f1219-1287">Nya cmdletar:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="f1219-1287">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="f1219-1288">Parametern DiskEncryptionSetId har lagts till i följande cmdletar:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="f1219-1288">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="f1219-1289">Parametrarna DiskEncryptionSetId och EncryptionType har lagts till i följande cmdletar:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="f1219-1289">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="f1219-1290">Lägg till parametern PublicIPAddressVersion i New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="f1219-1290">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="f1219-1291">Flytta FileUris för anpassat skripttillägg från offentlig inställning till skyddad inställning</span><span class="sxs-lookup"><span data-stu-id="f1219-1291">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="f1219-1292">Lägg till ScaleInPolicy i cmdletarna New-AzVmss, New-AzVmssConfig och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f1219-1292">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="f1219-1293">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="f1219-1293">Breaking changes</span></span>
    - <span data-ttu-id="f1219-1294">Parametern UploadSizeInBytes används istället för DiskSizeGB för New-AzDiskConfig när CreateOption är Uppladdning</span><span class="sxs-lookup"><span data-stu-id="f1219-1294">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="f1219-1295">PublishingProfile.Source.ManagedImage.Id ersätts med StorageProfile.Source.Id i objektet GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="f1219-1295">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f1219-1296">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f1219-1296">Az.DataFactory</span></span>
* <span data-ttu-id="f1219-1297">Uppdatera ADF .Net SDK-versionen till 4.3.0</span><span class="sxs-lookup"><span data-stu-id="f1219-1297">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f1219-1298">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f1219-1298">Az.DataLakeStore</span></span>
* <span data-ttu-id="f1219-1299">Uppdatera ADLS SDK-version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) innehåller följande korrigeringar</span><span class="sxs-lookup"><span data-stu-id="f1219-1299">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="f1219-1300">Undvik att utlösa undantag när det inte går att deserialisera creationtime för inmatning av papperskorg eller katalog.</span><span class="sxs-lookup"><span data-stu-id="f1219-1300">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="f1219-1301">Gör inställning tillgänglig per tidsgräns för förfrågan i adlsclient</span><span class="sxs-lookup"><span data-stu-id="f1219-1301">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="f1219-1302">Korrigera överföringen av ursprunglig syncflag för badoffset-återställning</span><span class="sxs-lookup"><span data-stu-id="f1219-1302">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="f1219-1303">Korrigera EnumerateDirectory för att hämta fortsättningstoken när svar har kontrollerats</span><span class="sxs-lookup"><span data-stu-id="f1219-1303">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="f1219-1304">Korrigera bugg i Concat</span><span class="sxs-lookup"><span data-stu-id="f1219-1304">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="f1219-1305">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f1219-1305">Az.FrontDoor</span></span>
* <span data-ttu-id="f1219-1306">Åtgärdade diverse stavfel i modul</span><span class="sxs-lookup"><span data-stu-id="f1219-1306">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="f1219-1307">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f1219-1307">Az.HDInsight</span></span>
* <span data-ttu-id="f1219-1308">Korrigerade buggen att kunder får felet ”inte en giltig Base-64-sträng” vid användning av Get-AzHDInsightCluster för att hämta klustret med ADLSGen1-lagring.</span><span class="sxs-lookup"><span data-stu-id="f1219-1308">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="f1219-1309">Lägg till en parameter med namnet ”ApplicationId” i de tre cmdletarna Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig och New-AzHDInsightCluster så att kunden kan tillhandahålla tjänstens huvudnamn för program-ID för åtkomst till Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="f1219-1309">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="f1219-1310">Ändrade Microsoft.Azure.Management.HDInsight från 2.1.0 till 5.1.0</span><span class="sxs-lookup"><span data-stu-id="f1219-1310">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="f1219-1311">Fem cmdletar har tagits bort:</span><span class="sxs-lookup"><span data-stu-id="f1219-1311">Removed five cmdlets:</span></span>
    - <span data-ttu-id="f1219-1312">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="f1219-1312">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="f1219-1313">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="f1219-1313">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="f1219-1314">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="f1219-1314">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="f1219-1315">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="f1219-1315">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="f1219-1316">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="f1219-1316">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="f1219-1317">Tre cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="f1219-1317">Added three cmdlets:</span></span>
    - <span data-ttu-id="f1219-1318">Get-AzHDInsightMonitoring som ersätter Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="f1219-1318">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="f1219-1319">Enable-AzHDInsightMonitoring som ersätter Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="f1219-1319">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="f1219-1320">Disable-AzHDInsightMonitoring som ersätter Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="f1219-1320">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="f1219-1321">Korrigerade cmdleten Get-AzHDInsightProperties för att stödja hämtning av funktionsinformation från en viss plats.</span><span class="sxs-lookup"><span data-stu-id="f1219-1321">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="f1219-1322">Parameteruppsättningarna (Spark1 och Spark2) har tagits bort från Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="f1219-1322">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="f1219-1323">Lägg till exempel för cmdleten Add-AzHDInsightSecurityProfile till hjälpdokumenten.</span><span class="sxs-lookup"><span data-stu-id="f1219-1323">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="f1219-1324">Ändrade utdatatyp för följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="f1219-1324">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="f1219-1325">Ändrade utdatatyp för Get-AzHDInsightProperties från CapabilitiesResponse till AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="f1219-1325">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="f1219-1326">Ändrade utdatatyp för Remove-AzHDInsightCluster från ClusterGetResponse till bool.</span><span class="sxs-lookup"><span data-stu-id="f1219-1326">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="f1219-1327">Ändrade utdatatyp för Set-AzHDInsightGatewaySettings HttpConnectivitySettings till GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="f1219-1327">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="f1219-1328">Lade till testfall för vissa scenarier.</span><span class="sxs-lookup"><span data-stu-id="f1219-1328">Added some scenario test cases.</span></span>
* <span data-ttu-id="f1219-1329">Ta bort vissa alias: Add-AzHDInsightConfigValues, Get-AzHDInsightProperties.</span><span class="sxs-lookup"><span data-stu-id="f1219-1329">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f1219-1330">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f1219-1330">Az.IotHub</span></span>
* <span data-ttu-id="f1219-1331">Icke-bakåtkompatibla ändringar:</span><span class="sxs-lookup"><span data-stu-id="f1219-1331">Breaking changes:</span></span>
    - <span data-ttu-id="f1219-1332">Cmdleten Add-AzIotHubEventHubConsumerGroup har inte längre stöd för parametern EventHubEndpointName och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="f1219-1332">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="f1219-1333">Parameteruppsättningen __AllParameterSets för cmdleten Add-AzIotHubEventHubConsumerGroup har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="f1219-1333">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="f1219-1334">Cmdleten Get-AzIotHubEventHubConsumerGroup har inte längre stöd för parametern EventHubEndpointName och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="f1219-1334">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="f1219-1335">Parameteruppsättningen __AllParameterSets för cmdleten Get-AzIotHubEventHubConsumerGroup har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="f1219-1335">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="f1219-1336">Egenskapen OperationsMonitoringProperties av typen Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="f1219-1336">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="f1219-1337">Egenskapen OperationsMonitoringProperties av typen Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="f1219-1337">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="f1219-1338">Cmdleten New-AzIotHubExportDevice stöder inte längre aliaset New-AzIotHubExportDevices.</span><span class="sxs-lookup"><span data-stu-id="f1219-1338">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="f1219-1339">Cmdleten New-AzIotHubImportDevice stöder inte längre aliaset New-AzIotHubImportDevices.</span><span class="sxs-lookup"><span data-stu-id="f1219-1339">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="f1219-1340">Cmdleten Remove-AzIotHubEventHubConsumerGroup har inte längre stöd för parametern EventHubEndpointName och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="f1219-1340">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="f1219-1341">Parameteruppsättningen __AllParameterSets för cmdleten Remove-AzIotHubEventHubConsumerGroup har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="f1219-1341">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="f1219-1342">Cmdleten Set-AzIotHub har inte längre stöd för parametern OperationsMonitoringProperties och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="f1219-1342">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="f1219-1343">Parameteruppsättningen UpdateOperationsMonitoringProperties för cmdleten Set-AzIotHub har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="f1219-1343">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f1219-1344">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f1219-1344">Az.RecoveryServices</span></span>
* <span data-ttu-id="f1219-1345">Azure Site Recovery-stöd för att konfigurera nätverksresurser som NSG, offentliga IP-adresser och interna lastbalanserare för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="f1219-1345">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="f1219-1346">Azure Site Recovery-stöd för att skriva till hanterad disk för vMWare till Azure.</span><span class="sxs-lookup"><span data-stu-id="f1219-1346">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="f1219-1347">Azure Site Recovery-stöd för NIC-reduktion för vMWare till Azure.</span><span class="sxs-lookup"><span data-stu-id="f1219-1347">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="f1219-1348">Azure Site Recovery-stöd för accelererat nätverk för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="f1219-1348">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="f1219-1349">Azure Site Recovery-stöd för automatisk uppdatering av agent för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="f1219-1349">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="f1219-1350">Azure Site Recovery-stöd för Standard SSD för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="f1219-1350">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="f1219-1351">Azure Site Recovery-stöd för tvåstegskryptering i Azure Disk Encryption för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="f1219-1351">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="f1219-1352">Azure Site Recovery-stöd för att skydda nyligen tillagda diskar för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="f1219-1352">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="f1219-1353">En funktion för mjuk borttagning av virtuella datorer samt tester för mjuk borttagning har tagits bort</span><span class="sxs-lookup"><span data-stu-id="f1219-1353">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="f1219-1354">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f1219-1354">Az.Resources</span></span>
* <span data-ttu-id="f1219-1355">Uppdatera beroendesammansättning för Microsoft.Extensions.Caching.Memory från 1.1.1 till 2.2</span><span class="sxs-lookup"><span data-stu-id="f1219-1355">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f1219-1356">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f1219-1356">Az.Network</span></span>
* <span data-ttu-id="f1219-1357">Ändra alla cmdletar för PrivateEndpointConnection så att de stöder generiska tjänstleverantörer.</span><span class="sxs-lookup"><span data-stu-id="f1219-1357">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="f1219-1358">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="f1219-1358">Updated cmdlet:</span></span>
        - <span data-ttu-id="f1219-1359">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f1219-1359">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="f1219-1360">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f1219-1360">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="f1219-1361">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f1219-1361">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="f1219-1362">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f1219-1362">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="f1219-1363">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f1219-1363">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="f1219-1364">Lägg till ny cmdlet för PrivateLinkResource så att det också stöder generiska tjänstleverantörer.</span><span class="sxs-lookup"><span data-stu-id="f1219-1364">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="f1219-1365">Ny cmdlet:</span><span class="sxs-lookup"><span data-stu-id="f1219-1365">New cmdlet:</span></span>
        - <span data-ttu-id="f1219-1366">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="f1219-1366">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="f1219-1367">Lägg till nya fält och parametrar för funktionen Proxy Protocol V2.</span><span class="sxs-lookup"><span data-stu-id="f1219-1367">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="f1219-1368">Lägg till egenskapen EnableProxyProtocol i PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f1219-1368">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="f1219-1369">Lägg till egenskapen LinkIdentifier i PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f1219-1369">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="f1219-1370">Uppdaterade New-AzPrivateLinkService för att lägga till den nya valfria parametern EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="f1219-1370">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="f1219-1371">Korrigera felaktig beskrivning av parameter i referensdokumentationen för New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="f1219-1371">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="f1219-1372">Nya cmdletar som stöder Azure-brandväggsprincipen</span><span class="sxs-lookup"><span data-stu-id="f1219-1372">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="f1219-1373">Lägg till stöd för den underordnade resursen RouteTables för VirtualHub</span><span class="sxs-lookup"><span data-stu-id="f1219-1373">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="f1219-1374">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="f1219-1374">New cmdlets added:</span></span>
        - <span data-ttu-id="f1219-1375">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="f1219-1375">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="f1219-1376">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="f1219-1376">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="f1219-1377">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="f1219-1377">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="f1219-1378">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="f1219-1378">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="f1219-1379">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="f1219-1379">Set-AzVirtualHub</span></span>
* <span data-ttu-id="f1219-1380">Lägg till stöd för ny egenskaps-SKU för VirtualHub och VirtualWANType för VirtualWan</span><span class="sxs-lookup"><span data-stu-id="f1219-1380">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="f1219-1381">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="f1219-1381">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="f1219-1382">New-AzVirtualHub: lade till parameter-SKU</span><span class="sxs-lookup"><span data-stu-id="f1219-1382">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="f1219-1383">Update-AzVirtualHub: lade till parameter-SKU</span><span class="sxs-lookup"><span data-stu-id="f1219-1383">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="f1219-1384">New-AzVirtualWan: lade till parametern VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="f1219-1384">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="f1219-1385">Update-AzVirtualWan: lade till parametern VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="f1219-1385">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="f1219-1386">Lägg till stöd för egenskapen EnableInternetSecurity för HubVnetConnection, VpnConnection och ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="f1219-1386">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="f1219-1387">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="f1219-1387">New cmdlets added:</span></span>
        - <span data-ttu-id="f1219-1388">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="f1219-1388">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="f1219-1389">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="f1219-1389">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="f1219-1390">New-AzureRmVirtualHubVnetConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="f1219-1390">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="f1219-1391">New-AzureRmVpnConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="f1219-1391">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="f1219-1392">Update-AzureRmVpnConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="f1219-1392">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="f1219-1393">New-AzureRmExpressRouteConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="f1219-1393">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="f1219-1394">Set-AzureRmExpressRouteConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="f1219-1394">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="f1219-1395">Lägg till stöd för att konfigurera TopLevel WebApplicationFirewall-princip</span><span class="sxs-lookup"><span data-stu-id="f1219-1395">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="f1219-1396">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="f1219-1396">New cmdlets added:</span></span>
        - <span data-ttu-id="f1219-1397">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="f1219-1397">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="f1219-1398">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="f1219-1398">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="f1219-1399">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="f1219-1399">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="f1219-1400">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="f1219-1400">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="f1219-1401">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="f1219-1401">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="f1219-1402">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="f1219-1402">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="f1219-1403">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="f1219-1403">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="f1219-1404">New-AzApplicationGatewayFirewallPolicy: parametrarna PolicySetting, ManagedRule har lagts till</span><span class="sxs-lookup"><span data-stu-id="f1219-1404">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="f1219-1405">Stöd för operator för geomatchning har lagts till på CustomRule</span><span class="sxs-lookup"><span data-stu-id="f1219-1405">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="f1219-1406">Geomatchning har lagts till i operatorn på FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="f1219-1406">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="f1219-1407">Stöd har lagts till för brandväggsprinciperna perListener och perSite</span><span class="sxs-lookup"><span data-stu-id="f1219-1407">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="f1219-1408">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="f1219-1408">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="f1219-1409">New-AzApplicationGatewayHttpListener: parametrarna FirewallPolicy, FirewallPolicyId har lagts till</span><span class="sxs-lookup"><span data-stu-id="f1219-1409">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="f1219-1410">New-AzApplicationGatewayPathRuleConfig: parametrarna FirewallPolicy, FirewallPolicyId har lagts till</span><span class="sxs-lookup"><span data-stu-id="f1219-1410">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="f1219-1411">Åtgärdat så att nödvändigt undernät med namnet AzureBastionSubnet i PSBastion kan vara skiftlägesokänsligt</span><span class="sxs-lookup"><span data-stu-id="f1219-1411">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="f1219-1412">Stöd för mål-FQDN:er i nätverksregler och översatt FQDN i NAT-regler för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="f1219-1412">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="f1219-1413">Lägg till stöd för resursen RouteTables för IpGroup på den högsta nivån</span><span class="sxs-lookup"><span data-stu-id="f1219-1413">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="f1219-1414">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="f1219-1414">New cmdlets added:</span></span>
        - <span data-ttu-id="f1219-1415">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="f1219-1415">New-AzIpGroup</span></span>
        - <span data-ttu-id="f1219-1416">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="f1219-1416">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="f1219-1417">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="f1219-1417">Get-AzIpGroup</span></span>
        - <span data-ttu-id="f1219-1418">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="f1219-1418">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f1219-1419">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f1219-1419">Az.ServiceFabric</span></span>
* <span data-ttu-id="f1219-1420">Ta bort cmdleten Add-AzServiceFabricApplicationCertificate eftersom det här scenariot omfattas av Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="f1219-1420">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="f1219-1421">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f1219-1421">Az.Sql</span></span>
* <span data-ttu-id="f1219-1422">Stöd har lagts till för återställning av utelämnade databaser på hanterade instanser.</span><span class="sxs-lookup"><span data-stu-id="f1219-1422">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="f1219-1423">Inaktuella gamla cmdletar för granskning från kod.</span><span class="sxs-lookup"><span data-stu-id="f1219-1423">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="f1219-1424">Tog bort inaktuella alias:</span><span class="sxs-lookup"><span data-stu-id="f1219-1424">Removed deprecated aliases:</span></span>
* <span data-ttu-id="f1219-1425">Get-AzSqlDatabaseIndexRecommendations (använd Get-AzSqlDatabaseIndexRecommendation istället)</span><span class="sxs-lookup"><span data-stu-id="f1219-1425">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="f1219-1426">Get-AzSqlDatabaseRestorePoints (använd Get-AzSqlDatabaseRestorePoint istället)</span><span class="sxs-lookup"><span data-stu-id="f1219-1426">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="f1219-1427">Ta bort cmdleten Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="f1219-1427">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="f1219-1428">Ta bort alias för inaktuella cmdletar för inställningar för utvärdering av säkerhetsrisk</span><span class="sxs-lookup"><span data-stu-id="f1219-1428">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="f1219-1429">Inaktualisera cmdletar för inställningar för avancerad hotidentifiering</span><span class="sxs-lookup"><span data-stu-id="f1219-1429">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="f1219-1430">Lägga till cmdletar för att inaktivera och aktivera känslighetsrekommendationer på kolumner i en databas.</span><span class="sxs-lookup"><span data-stu-id="f1219-1430">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f1219-1431">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f1219-1431">Az.Storage</span></span>
* <span data-ttu-id="f1219-1432">Stöd för att aktivera stora filresurser vid skapande eller uppdatering av lagringskonto</span><span class="sxs-lookup"><span data-stu-id="f1219-1432">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="f1219-1433">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f1219-1433">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="f1219-1434">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f1219-1434">Set-AzStorageAccount</span></span>
* <span data-ttu-id="f1219-1435">När du stänger/hämtar en filreferens kan du hoppa över kontrollen av huruvida indatasökvägen är en filkatalog eller en fil för att undvika problem med objekt som har status DeletePending</span><span class="sxs-lookup"><span data-stu-id="f1219-1435">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="f1219-1436">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="f1219-1436">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="f1219-1437">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="f1219-1437">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="f1219-1438">2.8.0 – oktober 2019</span><span class="sxs-lookup"><span data-stu-id="f1219-1438">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="f1219-1439">Allmänt</span><span class="sxs-lookup"><span data-stu-id="f1219-1439">General</span></span>
* <span data-ttu-id="f1219-1440">AZ. HealthcareApis 1.0.0-version</span><span class="sxs-lookup"><span data-stu-id="f1219-1440">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f1219-1441">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f1219-1441">Az.Accounts</span></span>
* <span data-ttu-id="f1219-1442">Uppdatera telemetri och URL-omskrivning för genererade moduler, korrigera Windows-enhetstester.</span><span class="sxs-lookup"><span data-stu-id="f1219-1442">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="f1219-1443">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f1219-1443">Az.ApiManagement</span></span>
* <span data-ttu-id="f1219-1444">**Set-AzApiManagementApi** – Tillagt stöd för att uppdatera Api till ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="f1219-1444">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="f1219-1445">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="f1219-1445">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f1219-1446">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f1219-1446">Az.Automation</span></span>
* <span data-ttu-id="f1219-1447">Åtgärdade cmdleten New-AzureAutomationSoftwareUpdateConfiguration för parametern för inställning av Linux-omstart.</span><span class="sxs-lookup"><span data-stu-id="f1219-1447">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="f1219-1448">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="f1219-1448">Az.Batch</span></span>
* <span data-ttu-id="f1219-1449">**Get-AzBatchNodeAgentSku** är inaktuell och ersätts av **Get-AzBatchSupportImage** i version 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="f1219-1449">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f1219-1450">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f1219-1450">Az.Compute</span></span>
* <span data-ttu-id="f1219-1451">Lägg till parametrarna Priority, EvictionPolicy och MaxPrice till cmdletarna New-AzVM och New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f1219-1451">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="f1219-1452">Korrigera varningsmeddelande och hjälpdokument för cmdletarna Add-AzVMAdditionalUnattendContent och Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="f1219-1452">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="f1219-1453">Åtgärda – skipVmBackup-undantag för virtuella Linux-datorer med hanterade diskar för Set-AzVMDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="f1219-1453">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="f1219-1454">Åtgärda fel i uppdatera krypteringsinställningarna i set-AzVMDiskEncryptionExtension, scenario i två steg.</span><span class="sxs-lookup"><span data-stu-id="f1219-1454">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f1219-1455">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f1219-1455">Az.DataFactory</span></span>
* <span data-ttu-id="f1219-1456">Lägga till CRUD-kommandon för ADF V2-dataflödet: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow och Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="f1219-1456">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="f1219-1457">Lägger till åtgärdskommandon för ADF V2-dataflödesfelsökningssession: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand och Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="f1219-1457">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="f1219-1458">Uppdatera ADF .Net SDK-versionen till 4.2.0</span><span class="sxs-lookup"><span data-stu-id="f1219-1458">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f1219-1459">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f1219-1459">Az.DataLakeStore</span></span>
* <span data-ttu-id="f1219-1460">Korrigera kontovalidering så att konton med ”-” kan skickas utan domän</span><span class="sxs-lookup"><span data-stu-id="f1219-1460">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="f1219-1461">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="f1219-1461">Az.HealthcareApis</span></span>
* <span data-ttu-id="f1219-1462">PowerShell-versionen har uppdaterats till 1.0.0</span><span class="sxs-lookup"><span data-stu-id="f1219-1462">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="f1219-1463">Uppdaterade SDK-versionen till 1.0.2</span><span class="sxs-lookup"><span data-stu-id="f1219-1463">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="f1219-1464">Uppdatera i tester för att referera till en ny SDK-version</span><span class="sxs-lookup"><span data-stu-id="f1219-1464">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="f1219-1465">Utdatastrukturen har uppdaterats från kapslad till förenklad.</span><span class="sxs-lookup"><span data-stu-id="f1219-1465">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f1219-1466">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f1219-1466">Az.IotHub</span></span>
* <span data-ttu-id="f1219-1467">Lägg till ny routningskälla: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="f1219-1467">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="f1219-1468">Mindre felkorrigering: Get-AzIothub returnerar inte subscriptionId</span><span class="sxs-lookup"><span data-stu-id="f1219-1468">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f1219-1469">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f1219-1469">Az.Monitor</span></span>
* <span data-ttu-id="f1219-1470">Nya åtgärdsgruppsmottagare har lagts till för åtgärdsgrupp   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="f1219-1470">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="f1219-1471">Använd vanligt aviseringsschema som är aktiverat för mottagarna.</span><span class="sxs-lookup"><span data-stu-id="f1219-1471">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="f1219-1472">Detta gäller inte för SMS, push för Azure-app, ITSM och röstmottagare</span><span class="sxs-lookup"><span data-stu-id="f1219-1472">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="f1219-1473">Webhooks har nu stöd för Azure Active Directory-autentisering.</span><span class="sxs-lookup"><span data-stu-id="f1219-1473">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f1219-1474">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f1219-1474">Az.Network</span></span>
* <span data-ttu-id="f1219-1475">Lägg till ny cmdlet Get-AzAvailableServiceAlias som kan anropas för att hämta de alias som kan användas för tjänstslutpunktsprinciper.</span><span class="sxs-lookup"><span data-stu-id="f1219-1475">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="f1219-1476">Stöd för tillägg av trafikväljare har lagts till i gatewayanslutningar för virtuella nätverk</span><span class="sxs-lookup"><span data-stu-id="f1219-1476">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="f1219-1477">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="f1219-1477">New cmdlets added:</span></span>
        - <span data-ttu-id="f1219-1478">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="f1219-1478">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="f1219-1479">Cmdletar har uppdaterats med valfri parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f1219-1479">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="f1219-1480">Lägg till stöd för ESP- och AH-protokoll i konfiguration av nätverkssäkerhetsregler</span><span class="sxs-lookup"><span data-stu-id="f1219-1480">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="f1219-1481">Uppdaterade cmdletar:</span><span class="sxs-lookup"><span data-stu-id="f1219-1481">Updated cmdlets:</span></span>
        - <span data-ttu-id="f1219-1482">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f1219-1482">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="f1219-1483">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f1219-1483">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="f1219-1484">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f1219-1484">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="f1219-1485">Förbättra hanteringen av undantag i Cortex-cmdletar</span><span class="sxs-lookup"><span data-stu-id="f1219-1485">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="f1219-1486">Nya generationer och SKU:er för VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="f1219-1486">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="f1219-1487">Introducera nya generationer för VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="f1219-1487">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="f1219-1488">Introducera nya SKU:er med högt dataflöde för VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="f1219-1488">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="f1219-1489">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="f1219-1489">Az.RedisCache</span></span>
* <span data-ttu-id="f1219-1490">Uppdaterad referensdokumentation för ”set-AzRedisCache” för att inkludera saknade värden för parametern ”size”</span><span class="sxs-lookup"><span data-stu-id="f1219-1490">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="f1219-1491">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f1219-1491">Az.Sql</span></span>
* <span data-ttu-id="f1219-1492">Lägg till stöd för inställningen Active Directory administratör på den hanterade instansen</span><span class="sxs-lookup"><span data-stu-id="f1219-1492">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f1219-1493">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f1219-1493">Az.Storage</span></span>
* <span data-ttu-id="f1219-1494">Uppdatera Lagringsklientbibliotek till 11.1.0</span><span class="sxs-lookup"><span data-stu-id="f1219-1494">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="f1219-1495">Lista containrar med hanteringsplans-API, kommer att listas med NextPageLink</span><span class="sxs-lookup"><span data-stu-id="f1219-1495">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="f1219-1496">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="f1219-1496">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="f1219-1497">Lista lagringskonton från prenumerationen, kommer att listas med NextPageLink</span><span class="sxs-lookup"><span data-stu-id="f1219-1497">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="f1219-1498">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f1219-1498">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="f1219-1499">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="f1219-1499">Az.StorageSync</span></span>
* <span data-ttu-id="f1219-1500">Åtgärda problemet 9810 i Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="f1219-1500">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f1219-1501">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f1219-1501">Az.Websites</span></span>
* <span data-ttu-id="f1219-1502">Set-AzWebApp – uppdatering av ASP för en app misslyckades</span><span class="sxs-lookup"><span data-stu-id="f1219-1502">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="f1219-1503">2.7.0 – september 2019</span><span class="sxs-lookup"><span data-stu-id="f1219-1503">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="f1219-1504">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f1219-1504">Az.ApiManagement</span></span>
* <span data-ttu-id="f1219-1505">Uppdatera ”-Format”-parameterbeskrivningen i ”Set-AzApiManagementPolicy”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="f1219-1505">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="f1219-1506">Referenser för den föråldrade cmdleten ”Update-AzApiManagementDeployment” har tagits bort från referensdokumentationen.</span><span class="sxs-lookup"><span data-stu-id="f1219-1506">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="f1219-1507">Använd ”Set-AzApiManagement” i stället.</span><span class="sxs-lookup"><span data-stu-id="f1219-1507">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f1219-1508">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f1219-1508">Az.Automation</span></span>
* <span data-ttu-id="f1219-1509">Stavfel har korrigerats i exempel i referensdokumentationen för ”Register-AzAutomationDscNode”</span><span class="sxs-lookup"><span data-stu-id="f1219-1509">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="f1219-1510">Klargörande har lagts till om OS-begränsningar för Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="f1219-1510">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="f1219-1511">Null-referensundantag har korrigerats för -Wait-alternativet i Start-AzAutomationRunbook-cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f1219-1511">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f1219-1512">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f1219-1512">Az.Compute</span></span>
* <span data-ttu-id="f1219-1513">Lägg till UploadSizeInBytes-parameter till New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="f1219-1513">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="f1219-1514">Lägg till Incremental-parameter till New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="f1219-1514">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="f1219-1515">Lägg till en funktion för virtuella datorer med låg prioritet:</span><span class="sxs-lookup"><span data-stu-id="f1219-1515">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="f1219-1516">MaxPrice-, EvictionPolicy- och Priority-parametrar har lagts till i New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="f1219-1516">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="f1219-1517">MaxPrice-parametern har lagts till i New-AzVmssConfig-, Update-AzVM- och Update-AzVmss-cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="f1219-1517">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="f1219-1518">Åtgärda problem med VM-referenser för Get-AzAvailabilitySet-cmdleten när alla tillgänglighetsuppsättningar i prenumerationen visas.</span><span class="sxs-lookup"><span data-stu-id="f1219-1518">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="f1219-1519">Korrigera null-undantaget för Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="f1219-1519">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="f1219-1520">Korrigera VHD-metoden för sökning relativt till slut.</span><span class="sxs-lookup"><span data-stu-id="f1219-1520">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="f1219-1521">Åtgärda UltraSSD-problem för New-AzVM och Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="f1219-1521">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f1219-1522">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f1219-1522">Az.DataFactory</span></span>
* <span data-ttu-id="f1219-1523">Lägger till 3 nya kommandon för ADF V2 – Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription och Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="f1219-1523">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="f1219-1524">ADF .Net SDK har uppdaterats till 4.1.3</span><span class="sxs-lookup"><span data-stu-id="f1219-1524">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="f1219-1525">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f1219-1525">Az.HDInsight</span></span>
* <span data-ttu-id="f1219-1526">Anrop för icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="f1219-1526">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f1219-1527">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f1219-1527">Az.IotHub</span></span>
* <span data-ttu-id="f1219-1528">Lägg till stöd för att anropa redundans för en IotHub till den geo-länkade katastrofåterställningsregionen.</span><span class="sxs-lookup"><span data-stu-id="f1219-1528">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="f1219-1529">Lägg till stöd för att hantera meddelandeberikning för en IotHub.</span><span class="sxs-lookup"><span data-stu-id="f1219-1529">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="f1219-1530">Nya cmdlet:ar är:</span><span class="sxs-lookup"><span data-stu-id="f1219-1530">New cmdlets are:</span></span>
    - <span data-ttu-id="f1219-1531">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="f1219-1531">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="f1219-1532">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="f1219-1532">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="f1219-1533">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="f1219-1533">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="f1219-1534">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="f1219-1534">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f1219-1535">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f1219-1535">Az.Monitor</span></span>
* <span data-ttu-id="f1219-1536">Pekar på den senaste Monitor SDK:n, dvs. 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="f1219-1536">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="f1219-1537">Lägger till bakåtkompatibla ändringar i Metrics-cmdletarna, dvs. enhetsuppräkningen stöder flera nya värden.</span><span class="sxs-lookup"><span data-stu-id="f1219-1537">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="f1219-1538">Detta är skrivskyddade cmdletar, så det förekommer inga ändringar i inmatningen för cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="f1219-1538">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="f1219-1539">API-versionen för **ActionGroups**-begäranden är nu **2019-06-01**. Tidigare var den **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="f1219-1539">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="f1219-1540">Test av scenarier har uppdaterats för att anpassas till den här ändringen.</span><span class="sxs-lookup"><span data-stu-id="f1219-1540">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="f1219-1541">Ett nytt obligatoriskt argument har lagts till för konstruktorerna för klasserna **EmailReceiver** och **WebhookReceiver** – ett booleskt värde med namnet **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="f1219-1541">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="f1219-1542">Värdet är för närvarande fast till **false** så att den här icke-bakåtkompatibla ändringen är dold från cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="f1219-1542">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="f1219-1543">**Obs!** Det här är en tillfällig ändring som måste verifieras av Alerts-teamet.</span><span class="sxs-lookup"><span data-stu-id="f1219-1543">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="f1219-1544">Ordningen på argumenten för konstruktorn för klassen **Source** (relaterad till klassen **ScheduledQueryRuleSource**) har ändrats från den tidigare SDK:n.</span><span class="sxs-lookup"><span data-stu-id="f1219-1544">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="f1219-1545">Den här ändringen krävde korrigering av två enhetstest: de kompilerades, men testerna skickades inte.</span><span class="sxs-lookup"><span data-stu-id="f1219-1545">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="f1219-1546">Ordningen på argumenten för konstruktorn för klassen **AlertingAction** (relaterad till klassen **ScheduledQueryRuleSource**) har ändrats från den tidigare SDK:n.</span><span class="sxs-lookup"><span data-stu-id="f1219-1546">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="f1219-1547">Den här ändringen krävde korrigering av två enhetstest: de kompilerades, men testerna skickades inte.</span><span class="sxs-lookup"><span data-stu-id="f1219-1547">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="f1219-1548">Stöd för kriterier för dynamiskt tröskelvärde för måttavisering v2</span><span class="sxs-lookup"><span data-stu-id="f1219-1548">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="f1219-1549">New-AzMetricAlertRuleV2Criteria: skapar nu även kriterier för dynamiskt tröskelvärde</span><span class="sxs-lookup"><span data-stu-id="f1219-1549">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="f1219-1550">Add-AzMetricAlertRuleV2: accepterar nu även kriterier för dynamiskt tröskelvärde</span><span class="sxs-lookup"><span data-stu-id="f1219-1550">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="f1219-1551">Förbättringar i schemalagd frågeregel (SQR)</span><span class="sxs-lookup"><span data-stu-id="f1219-1551">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="f1219-1552">Cmdletar accepterar ”Location”-parameter i båda formaten, antingen platsen (t.ex. eastus) eller platsens visningsnamn (t.ex. USA, östra)</span><span class="sxs-lookup"><span data-stu-id="f1219-1552">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="f1219-1553">”Enabled”-parametern illustreras korrekt i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="f1219-1553">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="f1219-1554">Exempel för den valfria parametern ”ActionGroup” har lagts till</span><span class="sxs-lookup"><span data-stu-id="f1219-1554">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="f1219-1555">Förbättrade hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="f1219-1555">Overall improved help files</span></span>
* <span data-ttu-id="f1219-1556">Åtgärda bugg då omfattningstypen fastställs för ”Set-AzActionRule”</span><span class="sxs-lookup"><span data-stu-id="f1219-1556">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f1219-1557">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f1219-1557">Az.Network</span></span>
* <span data-ttu-id="f1219-1558">Korrigera felaktigt exempel i referensdokumentationen för ”New-AzApplicationGateway”</span><span class="sxs-lookup"><span data-stu-id="f1219-1558">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="f1219-1559">Lägg till anmärkning i ”Get-AzNetworkWatcherPacketCapture”-referensdokumentationen om hämtning av alla egenskaper för en paketinsamling</span><span class="sxs-lookup"><span data-stu-id="f1219-1559">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="f1219-1560">Exempel har korrigerats i ”Test-AzNetworkWatcherIPFlow”-referensdokumentationen för korrekt uppräkning av nätverkskort</span><span class="sxs-lookup"><span data-stu-id="f1219-1560">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="f1219-1561">Förbättrad tolkning av molnundantag för att visa eventuell ytterligare information</span><span class="sxs-lookup"><span data-stu-id="f1219-1561">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="f1219-1562">Förbättrad tolkning av molnundantag för att hantera ytterligare en typ av SDK-undantag</span><span class="sxs-lookup"><span data-stu-id="f1219-1562">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="f1219-1563">Felaktig mappning av säkerhetsregelmodeller har korrigerats</span><span class="sxs-lookup"><span data-stu-id="f1219-1563">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="f1219-1564">Egenskaper har lagts till för nätverksgränssnittet för funktionen Privat IP</span><span class="sxs-lookup"><span data-stu-id="f1219-1564">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="f1219-1565">Egenskapen ”PrivateEndpoint” har lagts till som en typ av PSResourceId till PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="f1219-1565">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="f1219-1566">Egenskapen ”PrivateLinkConnectionProperties” har lagts till som en typ av PSIpConfigurationConnectivityInformation till PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="f1219-1566">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="f1219-1567">Modellklassen PSIpConfigurationConnectivityInformation har lagts till</span><span class="sxs-lookup"><span data-stu-id="f1219-1567">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="f1219-1568">ApplicationRuleProtocolType ”mssql” har lagts till för Azure Firewall-resurs</span><span class="sxs-lookup"><span data-stu-id="f1219-1568">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="f1219-1569">MultiLink-stöd i virtuellt WAN</span><span class="sxs-lookup"><span data-stu-id="f1219-1569">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="f1219-1570">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="f1219-1570">New cmdlets</span></span>
        - <span data-ttu-id="f1219-1571">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="f1219-1571">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="f1219-1572">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="f1219-1572">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="f1219-1573">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="f1219-1573">Updated cmdlet:</span></span>
        - <span data-ttu-id="f1219-1574">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="f1219-1574">New-VpnSite</span></span>
        - <span data-ttu-id="f1219-1575">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="f1219-1575">Update-VpnSite</span></span>
        - <span data-ttu-id="f1219-1576">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="f1219-1576">New-VpnConnection</span></span>
        - <span data-ttu-id="f1219-1577">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="f1219-1577">Update-VpnConnection</span></span>
* <span data-ttu-id="f1219-1578">Dokument för vissa PowerShell-exempel har korrigerats så att Az-cmdletar används i stället för AzureRM-cmdletar</span><span class="sxs-lookup"><span data-stu-id="f1219-1578">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f1219-1579">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f1219-1579">Az.RecoveryServices</span></span>
* <span data-ttu-id="f1219-1580">Uppdatera AzureVMpolicy-objekt med ProtectedItemsCount-attribut</span><span class="sxs-lookup"><span data-stu-id="f1219-1580">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="f1219-1581">Ytterligare tester har lagts till för VM-princip och återställning av ursprungligt lagringskonto</span><span class="sxs-lookup"><span data-stu-id="f1219-1581">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="f1219-1582">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f1219-1582">Az.Resources</span></span>
* <span data-ttu-id="f1219-1583">Åtgärda fel där det inte gick att anropa New-AzRoleAssignment utan parametern Scope.</span><span class="sxs-lookup"><span data-stu-id="f1219-1583">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f1219-1584">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f1219-1584">Az.ServiceFabric</span></span>
* <span data-ttu-id="f1219-1585">Stavfel har korrigerats i exempel för ”Update-AzServiceFabricReliability”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="f1219-1585">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="f1219-1586">Lägger till nya cmdletar för att hantera program och tjänster:</span><span class="sxs-lookup"><span data-stu-id="f1219-1586">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="f1219-1587">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="f1219-1587">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="f1219-1588">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="f1219-1588">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="f1219-1589">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="f1219-1589">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="f1219-1590">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="f1219-1590">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="f1219-1591">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="f1219-1591">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="f1219-1592">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="f1219-1592">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="f1219-1593">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="f1219-1593">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="f1219-1594">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="f1219-1594">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="f1219-1595">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="f1219-1595">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="f1219-1596">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="f1219-1596">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="f1219-1597">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="f1219-1597">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="f1219-1598">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="f1219-1598">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="f1219-1599">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="f1219-1599">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="f1219-1600">Service Fabric SDK har uppgraderats till version 1.2.0 som använder Service Fabric-resursprovidern med API-version 2019-03-01.</span><span class="sxs-lookup"><span data-stu-id="f1219-1600">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="f1219-1601">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="f1219-1601">Az.SignalR</span></span>
* <span data-ttu-id="f1219-1602">Lägg till Update-, Restart-, CheckNameAvailability- och GetUsage-cmdletar</span><span class="sxs-lookup"><span data-stu-id="f1219-1602">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="f1219-1603">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f1219-1603">Az.Sql</span></span>
* <span data-ttu-id="f1219-1604">Uppdatera exempel i referensdokumentationen för ”Get-AzSqlElasticPool”</span><span class="sxs-lookup"><span data-stu-id="f1219-1604">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="f1219-1605">vCore-exempel för att skapa en elastisk pool (New-AzSqlElasticPool) har lagts till.</span><span class="sxs-lookup"><span data-stu-id="f1219-1605">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="f1219-1606">Ta bort verifieringen av EmailAddresses och kontrollen som bekräftar att EmailAdmins inte är falskt när EmailAddresses är tomt i Set-AzSqlServerAdvancedThreatProtectionPolicy och Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="f1219-1606">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="f1219-1607">Server-/databasgranskningsinställningar kan tas bort när det finns flera diagnostikinställningar som aktiverar granskningskategorin.</span><span class="sxs-lookup"><span data-stu-id="f1219-1607">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="f1219-1608">Åtgärda verifiering av e-postadresser i flera Sql Vulnerability Assessment-cmdletar (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting och Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="f1219-1608">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f1219-1609">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f1219-1609">Az.Storage</span></span>
* <span data-ttu-id="f1219-1610">Exempel i referensdokumentationen för ”Get-AzStorageAccountKey” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="f1219-1610">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="f1219-1611">Vid upp- och nedladdning av en Azure-fil kan SMB-egenskaperna för källfilen (t.ex. filattribut, tidpunkten då filen skapades och tidpunkten för den senaste skrivningen) sparas i målfilen</span><span class="sxs-lookup"><span data-stu-id="f1219-1611">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="f1219-1612">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="f1219-1612">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="f1219-1613">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="f1219-1613">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="f1219-1614">Korrigera problem med uppladdningen av blockblob med egenskaper/metadata för ImmutabilityPolicy i containrar.</span><span class="sxs-lookup"><span data-stu-id="f1219-1614">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="f1219-1615">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="f1219-1615">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="f1219-1616">Stöd för hantering av Azure-filresurser med API för hanteringsplan</span><span class="sxs-lookup"><span data-stu-id="f1219-1616">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="f1219-1617">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="f1219-1617">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="f1219-1618">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="f1219-1618">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="f1219-1619">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="f1219-1619">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="f1219-1620">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="f1219-1620">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f1219-1621">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f1219-1621">Az.Websites</span></span>
* <span data-ttu-id="f1219-1622">Åtgärdar problemet där webapp-taggar togs bort när appen migrerades till nya ASP</span><span class="sxs-lookup"><span data-stu-id="f1219-1622">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="f1219-1623">Åtgärda Publish-AzureWebapp så att det fungerar i Linux och Windows</span><span class="sxs-lookup"><span data-stu-id="f1219-1623">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="f1219-1624">Uppdatera exempel i ”Get-AzWebAppPublishingProfile”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="f1219-1624">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="f1219-1625">2.6.0 – augusti 2019</span><span class="sxs-lookup"><span data-stu-id="f1219-1625">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="f1219-1626">Allmänt</span><span class="sxs-lookup"><span data-stu-id="f1219-1626">General</span></span>
* <span data-ttu-id="f1219-1627">Åtgärdade diverse skrivfel i flera moduler</span><span class="sxs-lookup"><span data-stu-id="f1219-1627">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f1219-1628">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f1219-1628">Az.Accounts</span></span>
* <span data-ttu-id="f1219-1629">Stöd för användartilldelat MSI i Azure Functions-autentisering (#9479)</span><span class="sxs-lookup"><span data-stu-id="f1219-1629">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="f1219-1630">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="f1219-1630">Az.Aks</span></span>
* <span data-ttu-id="f1219-1631">Åtgärda problem med utdata för "Get-AzAks"</span><span class="sxs-lookup"><span data-stu-id="f1219-1631">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="f1219-1632">Mer information här: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="f1219-1632">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="f1219-1633">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f1219-1633">Az.ApiManagement</span></span>
* <span data-ttu-id="f1219-1634">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="f1219-1634">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="f1219-1635">Uppdatera .net-NuGet-versionen, som inte tillämpar begränsningar för productId, apiId och userId</span><span class="sxs-lookup"><span data-stu-id="f1219-1635">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="f1219-1636">**Get-AzApiManagementProduct** – Lade till stöd för frågekörning mot produkter via API.</span><span class="sxs-lookup"><span data-stu-id="f1219-1636">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="f1219-1637">**New-AzApiManagementApiRevision** – Korrigering för problem där ApiRevisionDescription inte angavs vid skapande av ny API-revision https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="f1219-1637">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="f1219-1638">Åtgärdade skrivfel i modellen "PsApiManagementOAuth2AuthrozationServer" till "PsApiManagementOAuth2AuthorizationServer"</span><span class="sxs-lookup"><span data-stu-id="f1219-1638">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="f1219-1639">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="f1219-1639">Az.Batch</span></span>
* <span data-ttu-id="f1219-1640">Åtgärdade skrivfel i hjälpmeddelande och dokumentation till att skriva Windows med versaler</span><span class="sxs-lookup"><span data-stu-id="f1219-1640">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="f1219-1641">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f1219-1641">Az.Cdn</span></span>
* <span data-ttu-id="f1219-1642">Åtgärdade skrivfel i CDN-modulens konverteringshjälp</span><span class="sxs-lookup"><span data-stu-id="f1219-1642">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f1219-1643">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f1219-1643">Az.Compute</span></span>
* <span data-ttu-id="f1219-1644">Lägg till VmssId i New-AzVMConfig-cmdleten</span><span class="sxs-lookup"><span data-stu-id="f1219-1644">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="f1219-1645">Lägg till parametrarna TerminateScheduledEvents och TerminateScheduledEventNotBeforeTimeoutInMinutes i New-AzVmssConfig och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f1219-1645">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="f1219-1646">Lägg till egenskapen HyperVGeneration till avbildningsobjekt för virtuell dator</span><span class="sxs-lookup"><span data-stu-id="f1219-1646">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="f1219-1647">Lägg till funktioner för Host och HostGroup</span><span class="sxs-lookup"><span data-stu-id="f1219-1647">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="f1219-1648">Nya cmdletar:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="f1219-1648">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="f1219-1649">HostId-parametern läggs till i New-AzVMConfig och New-AzVM</span><span class="sxs-lookup"><span data-stu-id="f1219-1649">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="f1219-1650">Uppdatera exempel i "Invoke-AzVMRunCommand"-dokumentationen till att använda rätt parameternamn</span><span class="sxs-lookup"><span data-stu-id="f1219-1650">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="f1219-1651">Uppdatera "-VolumeType"-beskrivningen i referensdokumentationen för "set-AzVMDiskEncryptionExtension" och "set-AzVmssDiskEncryptionExtension"</span><span class="sxs-lookup"><span data-stu-id="f1219-1651">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f1219-1652">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f1219-1652">Az.DataFactory</span></span>
* <span data-ttu-id="f1219-1653">Åtgärda skrivfel till att använda versaler för "Windows" i "New-AzDataFactoryEncryptValue"-dokumentationen</span><span class="sxs-lookup"><span data-stu-id="f1219-1653">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="f1219-1654">Uppdaterade ADF .Net SDK-versionen till 4.1.2</span><span class="sxs-lookup"><span data-stu-id="f1219-1654">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="f1219-1655">Lägg till parametrarna "DataProxyIntegrationRuntimeName", "DataProxyStagingLinkedServiceName" och "DataProxyStagingPath" för "Set-AzureRmDataFactoryV2IntegrationRuntime"-cmd för att aktivera konfiguration av lokalt installerad integrationskörning som en proxy för SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="f1219-1655">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="f1219-1656">Uppdaterade PSTriggerRun till att visa utlöst pipeline, meddelande och egenskaper samt PSActivityRun till att visa aktivitetstypen</span><span class="sxs-lookup"><span data-stu-id="f1219-1656">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f1219-1657">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f1219-1657">Az.DataLakeStore</span></span>
* <span data-ttu-id="f1219-1658">Korrigering av frysning av Get-DataLakeStoreDeletedItem för fel eller fjärrundantag.</span><span class="sxs-lookup"><span data-stu-id="f1219-1658">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f1219-1659">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f1219-1659">Az.EventHub</span></span>
* <span data-ttu-id="f1219-1660">Korrigering av problem #9658 : Skrivfel i parametern VirtualNteworkRule i Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="f1219-1660">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="f1219-1661">Korrigering av problem #9558 : Set-AzEventHubNamespace använder PATCH i stället för PUT</span><span class="sxs-lookup"><span data-stu-id="f1219-1661">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="f1219-1662">lade till parametern EnableKafka i Set-AzEventHubNamespace-cmdleten</span><span class="sxs-lookup"><span data-stu-id="f1219-1662">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="f1219-1663">Korrigering av problem #9786 : kan inte skapa en regel med Endast lyssna-behörighet</span><span class="sxs-lookup"><span data-stu-id="f1219-1663">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="f1219-1664">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="f1219-1664">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="f1219-1665">Åtgärdade skrivfel i dokumentation där "Azure" skrevs helt med gemener</span><span class="sxs-lookup"><span data-stu-id="f1219-1665">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f1219-1666">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f1219-1666">Az.Monitor</span></span>
* <span data-ttu-id="f1219-1667">Åtgärdade felaktigt parameternamn i hjälpdokumentationen</span><span class="sxs-lookup"><span data-stu-id="f1219-1667">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f1219-1668">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f1219-1668">Az.Network</span></span>
* <span data-ttu-id="f1219-1669">Uppdaterade New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="f1219-1669">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="f1219-1670">Gjorde parametern "PublicIpAddress" inaktuell eftersom den aldrig används på serversidan.</span><span class="sxs-lookup"><span data-stu-id="f1219-1670">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="f1219-1671">Lade till den valfria parametern "Primary", som anger huruvida den aktuella IP-konfigurationen är den primära.</span><span class="sxs-lookup"><span data-stu-id="f1219-1671">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="f1219-1672">Förbättrade hanteringen av felundantag för begärande från SDK – åtgärdar problemet att tidigare SDK-undantag inte hanteras på rätt sätt, vilket leder till att viktig felinformation inte visas</span><span class="sxs-lookup"><span data-stu-id="f1219-1672">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="f1219-1673">Justerade valideringslogiken för IPv6-IP-prefix till att kontrollera korrekt IPv6-prefixlängd.</span><span class="sxs-lookup"><span data-stu-id="f1219-1673">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="f1219-1674">Uppdaterade Get-AzVirtualNetworkSubnetConfig: Lade till parameter som anges till get av undernätets resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="f1219-1674">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="f1219-1675">Uppdaterade beskrivningen av parametern Location för AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="f1219-1675">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f1219-1676">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f1219-1676">Az.OperationalInsights</span></span>
* <span data-ttu-id="f1219-1677">Uppdaterade dokumentation för "New-AzOperationalInsightsLinuxSyslogDataSource"</span><span class="sxs-lookup"><span data-stu-id="f1219-1677">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="f1219-1678">Lade till exempel</span><span class="sxs-lookup"><span data-stu-id="f1219-1678">Added example</span></span>
    - <span data-ttu-id="f1219-1679">Uppdaterade beskrivningen av parametern "-Name"</span><span class="sxs-lookup"><span data-stu-id="f1219-1679">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="f1219-1680">Lade till ett exempel för New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="f1219-1680">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="f1219-1681">Ändrade beskrivningen av parametern -Name för New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="f1219-1681">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f1219-1682">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f1219-1682">Az.RecoveryServices</span></span>
* <span data-ttu-id="f1219-1683">Uppdatera "Get-AzRecoveryServicesBackupJobDetail.md"</span><span class="sxs-lookup"><span data-stu-id="f1219-1683">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="f1219-1684">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f1219-1684">Az.Resources</span></span>
* <span data-ttu-id="f1219-1685">Lägg till stöd för den nya API-versionen från 2019-05-10 för Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="f1219-1685">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="f1219-1686">Lägg till stöd för "copy.count = 0" för variabler, resurser och egenskaper</span><span class="sxs-lookup"><span data-stu-id="f1219-1686">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="f1219-1687">Resurser med "condition = false" eller "copy.count = 0" tas bort i complete-läget</span><span class="sxs-lookup"><span data-stu-id="f1219-1687">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="f1219-1688">Lägg till ett exempel på tilldelning av princip på prenumerationsnivå i hjälpdokumentationen</span><span class="sxs-lookup"><span data-stu-id="f1219-1688">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="f1219-1689">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f1219-1689">Az.ServiceBus</span></span>
* <span data-ttu-id="f1219-1690">Korrigering av problem #9658 : Skrivfel i parametern VirtualNetworkRule i set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="f1219-1690">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="f1219-1691">Korrigering av problem #9786 : kan inte skapa en regel med Endast lyssna-behörighet</span><span class="sxs-lookup"><span data-stu-id="f1219-1691">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="f1219-1692">Lade till det nya kommandot "Test-AzServiceBusNameAvailability" för att kontrollera namntillgängligheten för kö och ämne</span><span class="sxs-lookup"><span data-stu-id="f1219-1692">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f1219-1693">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f1219-1693">Az.ServiceFabric</span></span>
* <span data-ttu-id="f1219-1694">Åtgärda buggar med tillägg av nodtyps-cmdlet:</span><span class="sxs-lookup"><span data-stu-id="f1219-1694">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="f1219-1695">NullReferenceException-bugg när resursgrupp hade annan vmss som inte är relaterad till Service Fabric-klustret.</span><span class="sxs-lookup"><span data-stu-id="f1219-1695">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="f1219-1696">Åtgärdar problemet: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="f1219-1696">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="f1219-1697">Åtgärda bugg där cmdleten misslyckades om virtualNetwork var i en annan resursgrupp än klustret.</span><span class="sxs-lookup"><span data-stu-id="f1219-1697">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="f1219-1698">Åtgärdar problemet: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="f1219-1698">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="f1219-1699">AzServiceFabricApplicationCertificate-cmdleten görs inaktuell</span><span class="sxs-lookup"><span data-stu-id="f1219-1699">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="f1219-1700">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f1219-1700">Az.Sql</span></span>
* <span data-ttu-id="f1219-1701">Uppdatera dokumentation om gamla gransknings-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="f1219-1701">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f1219-1702">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f1219-1702">Az.Storage</span></span>
* <span data-ttu-id="f1219-1703">Uppdatera hjälpen för Get/Close-AzStorageFileHandle genom att lägga till fler scenarier i cmdlet-exempel och uppdatera parameterbeskrivningar</span><span class="sxs-lookup"><span data-stu-id="f1219-1703">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="f1219-1704">Stöd för StandardBlobTier i uppladdningsblob och kopieringsblob</span><span class="sxs-lookup"><span data-stu-id="f1219-1704">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="f1219-1705">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="f1219-1705">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="f1219-1706">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="f1219-1706">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="f1219-1707">Stöd för rehydratiseringsprioritet i kopieringsblob</span><span class="sxs-lookup"><span data-stu-id="f1219-1707">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="f1219-1708">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="f1219-1708">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f1219-1709">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f1219-1709">Az.Websites</span></span>
* <span data-ttu-id="f1219-1710">Lägg till klargöranden gällande parametern -AppSettings i Set-AzWebApp och Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f1219-1710">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="f1219-1711">2.5.0 – July 2019</span><span class="sxs-lookup"><span data-stu-id="f1219-1711">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f1219-1712">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f1219-1712">Az.Accounts</span></span>
* <span data-ttu-id="f1219-1713">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="f1219-1713">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="f1219-1714">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="f1219-1714">Az.ApplicationInsights</span></span>
* <span data-ttu-id="f1219-1715">Korrigera skrivfel i exempel i dokumentationen för Remove-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="f1219-1715">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f1219-1716">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f1219-1716">Az.Automation</span></span>
* <span data-ttu-id="f1219-1717">Korrigera skrivfel i resurssträng</span><span class="sxs-lookup"><span data-stu-id="f1219-1717">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f1219-1718">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f1219-1718">Az.CognitiveServices</span></span>
* <span data-ttu-id="f1219-1719">Stöd för NetworkRuleSet har lagts till.</span><span class="sxs-lookup"><span data-stu-id="f1219-1719">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f1219-1720">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f1219-1720">Az.Compute</span></span>
* <span data-ttu-id="f1219-1721">Lägg till saknade egenskaper (ComputerName, OsName, OsVersion och HyperVGeneration) för visningsobjekt i den virtuella datorinstansen.</span><span class="sxs-lookup"><span data-stu-id="f1219-1721">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="f1219-1722">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f1219-1722">Az.ContainerRegistry</span></span>
* <span data-ttu-id="f1219-1723">Åtgärda skrivfel i Remove-AzContainerRegistryReplication för parametern Replication</span><span class="sxs-lookup"><span data-stu-id="f1219-1723">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="f1219-1724">Mer information finns här: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="f1219-1724">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f1219-1725">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f1219-1725">Az.DataFactory</span></span>
* <span data-ttu-id="f1219-1726">ADF .Net SDK-versionen har uppdaterats till 4.1.0</span><span class="sxs-lookup"><span data-stu-id="f1219-1726">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="f1219-1727">Korrigera skrivfel i dokumentationen för Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="f1219-1727">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f1219-1728">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f1219-1728">Az.EventHub</span></span>
* <span data-ttu-id="f1219-1729">Ny cmmdlet har lagts till för att skapa SAS-token: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="f1219-1729">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="f1219-1730">verifierings- och felmeddelande har lagts till för authorizationrules-rättigheter om endast "hantera" har tilldelats</span><span class="sxs-lookup"><span data-stu-id="f1219-1730">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f1219-1731">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f1219-1731">Az.KeyVault</span></span>
* <span data-ttu-id="f1219-1732">Stöd har lagts till för att ange KeySize för certifikatprinciper</span><span class="sxs-lookup"><span data-stu-id="f1219-1732">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="f1219-1733">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="f1219-1733">Az.LogicApp</span></span>
* <span data-ttu-id="f1219-1734">Korrigering för Get-AzIntegrationAccountMap för att lista alla mappningstyper</span><span class="sxs-lookup"><span data-stu-id="f1219-1734">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="f1219-1735">Ny MapType-parameter har lagts till för filtrering</span><span class="sxs-lookup"><span data-stu-id="f1219-1735">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="f1219-1736">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="f1219-1736">Az.ManagedServices</span></span>
* <span data-ttu-id="f1219-1737">Stöd för API-versionen 2019-06-01 (GA) har lagts till</span><span class="sxs-lookup"><span data-stu-id="f1219-1737">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f1219-1738">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f1219-1738">Az.Network</span></span>
* <span data-ttu-id="f1219-1739">Lägg till stöd för privat slutpunkt och privat länktjänst</span><span class="sxs-lookup"><span data-stu-id="f1219-1739">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="f1219-1740">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="f1219-1740">New cmdlets</span></span>
        - <span data-ttu-id="f1219-1741">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f1219-1741">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="f1219-1742">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f1219-1742">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="f1219-1743">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f1219-1743">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="f1219-1744">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f1219-1744">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="f1219-1745">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f1219-1745">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="f1219-1746">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f1219-1746">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="f1219-1747">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="f1219-1747">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="f1219-1748">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f1219-1748">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="f1219-1749">Nedanstående kommandon för funktionen har uppdaterats: Flaggan PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies på undernätet i VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f1219-1749">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="f1219-1750">Uppdaterade New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="f1219-1750">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="f1219-1751">Valfri parameter har lagts till – PrivateEndpointNetworkPoliciesFlag som konfigurerar huruvida nätverksprinciper ska tillämpas på en privat slutpunkt i det här undernätet.</span><span class="sxs-lookup"><span data-stu-id="f1219-1751">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="f1219-1752">Valfri parameter har lagts till – PrivateLinkServiceNetworkPoliciesFlag som konfigurerar huruvida nätverksprinciper ska tillämpas på en privat länktjänst i det här undernätet.</span><span class="sxs-lookup"><span data-stu-id="f1219-1752">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="f1219-1753">AzPrivateLinkService för cmdlet-parametern ServiceName har bytt namn till Name med aliaset ServiceName för bakåtkompatibilitet</span><span class="sxs-lookup"><span data-stu-id="f1219-1753">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="f1219-1754">Aktivera ICMP-protokoll för konfiguration av nätverkssäkerhetsregler</span><span class="sxs-lookup"><span data-stu-id="f1219-1754">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="f1219-1755">Uppdaterade cmdletar</span><span class="sxs-lookup"><span data-stu-id="f1219-1755">Updated cmdlets</span></span>
        - <span data-ttu-id="f1219-1756">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f1219-1756">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="f1219-1757">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f1219-1757">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="f1219-1758">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f1219-1758">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="f1219-1759">Lägg till ConnectionProtocolType (Ikev1/Ikev2) som en konfigurerbar parameter för New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f1219-1759">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="f1219-1760">Lägg till PrivateIpAddressVersion i LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="f1219-1760">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="f1219-1761">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="f1219-1761">Updated cmdlet:</span></span>
        - <span data-ttu-id="f1219-1762">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f1219-1762">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="f1219-1763">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f1219-1763">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="f1219-1764">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f1219-1764">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="f1219-1765">Uppdatering av Application Gateway-kommandot New-AzApplicationGatewayProbeConfig för stöd av anpassad port i Probe</span><span class="sxs-lookup"><span data-stu-id="f1219-1765">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="f1219-1766">Uppdaterade New-AzApplicationGatewayProbeConfig: Den valfria parametern Port som används för avsökning i serverdelen har lagts till.</span><span class="sxs-lookup"><span data-stu-id="f1219-1766">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="f1219-1767">Denna parameter gäller för SKU:erna Standard_V2 och WAF_V2.</span><span class="sxs-lookup"><span data-stu-id="f1219-1767">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f1219-1768">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f1219-1768">Az.OperationalInsights</span></span>
* <span data-ttu-id="f1219-1769">Uppdaterade standardversionen för sparade sökningar till 1.</span><span class="sxs-lookup"><span data-stu-id="f1219-1769">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="f1219-1770">Åtgärdade hantering av anpassad log null regex</span><span class="sxs-lookup"><span data-stu-id="f1219-1770">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f1219-1771">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f1219-1771">Az.RecoveryServices</span></span>
* <span data-ttu-id="f1219-1772">Uppdatera Get-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="f1219-1772">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="f1219-1773">Uppdatera Get-AzRecoveryServicesBackupContainer.md</span><span class="sxs-lookup"><span data-stu-id="f1219-1773">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="f1219-1774">Uppdatera Get-AzRecoveryServicesVault.md</span><span class="sxs-lookup"><span data-stu-id="f1219-1774">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="f1219-1775">Uppdatera Wait-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="f1219-1775">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="f1219-1776">Uppdatera Set-AzRecoveryServicesVaultContext.md</span><span class="sxs-lookup"><span data-stu-id="f1219-1776">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="f1219-1777">Uppdatera Get-AzRecoveryServicesBackupItem.md</span><span class="sxs-lookup"><span data-stu-id="f1219-1777">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="f1219-1778">Uppdatera Get-AzRecoveryServicesBackupRecoveryPoint.md</span><span class="sxs-lookup"><span data-stu-id="f1219-1778">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="f1219-1779">Uppdatera Restore-AzRecoveryServicesBackupItem.md</span><span class="sxs-lookup"><span data-stu-id="f1219-1779">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="f1219-1780">Uppdaterat tjänstanrop för avregistrering av container för Azure-filresurs</span><span class="sxs-lookup"><span data-stu-id="f1219-1780">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="f1219-1781">Uppdatera Set-AzRecoveryServicesAsrAlertSetting.md</span><span class="sxs-lookup"><span data-stu-id="f1219-1781">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="f1219-1782">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f1219-1782">Az.Resources</span></span>
- <span data-ttu-id="f1219-1783">Ta bort den cmdlet som saknas och som refereras i dokumentationen till New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f1219-1783">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="f1219-1784">Princip-cmdletar har uppdaterats så att de använder den nya API-versionen 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="f1219-1784">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="f1219-1785">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f1219-1785">Az.ServiceBus</span></span>
* <span data-ttu-id="f1219-1786">Ny cmmdlet har lagts till för att skapa SAS-token: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="f1219-1786">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="f1219-1787">verifierings- och felmeddelande har lagts till för authorizationrules-rättigheter om endast "hantera" har tilldelats</span><span class="sxs-lookup"><span data-stu-id="f1219-1787">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="f1219-1788">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f1219-1788">Az.Sql</span></span>
* <span data-ttu-id="f1219-1789">Åtgärda saknade exempel för Set-AzSqlDatabaseSecondary cmdlet</span><span class="sxs-lookup"><span data-stu-id="f1219-1789">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="f1219-1790">Åtgärda angivna återkommande genomsökningar för bedömning av säkerhetsrisk utan angivna e-postadresser</span><span class="sxs-lookup"><span data-stu-id="f1219-1790">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="f1219-1791">Korrigera ett skrivfel i ett varningsmeddelande.</span><span class="sxs-lookup"><span data-stu-id="f1219-1791">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f1219-1792">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f1219-1792">Az.Storage</span></span>
* <span data-ttu-id="f1219-1793">Uppdatera exempel i referensdokumentationen för Get-AzStorageAccount så att rätt parameternamn används</span><span class="sxs-lookup"><span data-stu-id="f1219-1793">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="f1219-1794">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="f1219-1794">Az.StorageSync</span></span>
* <span data-ttu-id="f1219-1795">Lägger till cmdleten Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="f1219-1795">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="f1219-1796">Åtgärda problem 9551 så att TierFilesOlderThanDays föredras</span><span class="sxs-lookup"><span data-stu-id="f1219-1796">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f1219-1797">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f1219-1797">Az.Websites</span></span>
* <span data-ttu-id="f1219-1798">Åtgärdar ett fel där vissa SiteConfig-egenskaper inte returnerades av Get-AzWebApp och Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="f1219-1798">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="f1219-1799">Lägger till en ny platsparameter för Get-AzDeletedWebApp och Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="f1219-1799">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="f1219-1800">Åtgärdar ett fel i kloning av webbapp-platser som använder New-AzWebApp-IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="f1219-1800">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="f1219-1801">2.4.0 – juli 2019</span><span class="sxs-lookup"><span data-stu-id="f1219-1801">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f1219-1802">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f1219-1802">Az.Accounts</span></span>
* <span data-ttu-id="f1219-1803">Lägg till stöd för profil-cmdletar</span><span class="sxs-lookup"><span data-stu-id="f1219-1803">Add support for profile cmdlets</span></span>
* <span data-ttu-id="f1219-1804">Lägg till stöd för miljöer och dataplaner i genererade cmdletar</span><span class="sxs-lookup"><span data-stu-id="f1219-1804">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="f1219-1805">Åtgärda bugg där fel slutpunkt i vissa fall användes för cmdletar för dataplaner i Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="f1219-1805">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="f1219-1806">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="f1219-1806">Az.Advisor</span></span>
* <span data-ttu-id="f1219-1807">GA-version av Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="f1219-1807">GA release of Az.Advisor</span></span>
* <span data-ttu-id="f1219-1808">Den här modulen ingår nu som en del av `Az`-sammanslagningsmodulen</span><span class="sxs-lookup"><span data-stu-id="f1219-1808">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="f1219-1809">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f1219-1809">Az.ApiManagement</span></span>
* <span data-ttu-id="f1219-1810">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="f1219-1810">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="f1219-1811">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="f1219-1811">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="f1219-1812">Stöd för att fråga prenumerationer efter användare och produkt har lagts till</span><span class="sxs-lookup"><span data-stu-id="f1219-1812">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="f1219-1813">Stöd för att fråga med hjälp av omfång ”/”, ”/apis”, ”/apis/echo-api” har lagts till</span><span class="sxs-lookup"><span data-stu-id="f1219-1813">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="f1219-1814">Korrigering av problem https://github.com/Azure/azure-powershell/issues/9307 och https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="f1219-1814">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="f1219-1815">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="f1219-1815">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="f1219-1816">Stöd för att ange ”ApiVersion” och ”ApiVersionSetId” när API:er importeras har lagts till</span><span class="sxs-lookup"><span data-stu-id="f1219-1816">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f1219-1817">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f1219-1817">Az.Automation</span></span>
* <span data-ttu-id="f1219-1818">Bugg med cmdleten Set-AzAutomationConnectionFieldValue för att hantera strängvärde har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="f1219-1818">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f1219-1819">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f1219-1819">Az.Compute</span></span>
* <span data-ttu-id="f1219-1820">Lägg till parametern HyperVGeneration i New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="f1219-1820">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f1219-1821">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f1219-1821">Az.DataFactory</span></span>
* <span data-ttu-id="f1219-1822">Uppdaterar utdata från ADF-cmdletar som hämtar aktivitetskörningar, hämtar pipelinekörningar och hämtar utlösarkörningar för stöd för Select-Object-pipe.</span><span class="sxs-lookup"><span data-stu-id="f1219-1822">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="f1219-1823">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="f1219-1823">Az.EventGrid</span></span>
* <span data-ttu-id="f1219-1824">Korrigera stavfel i dokumentation om ”New-AzEventGridSubscription”</span><span class="sxs-lookup"><span data-stu-id="f1219-1824">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f1219-1825">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f1219-1825">Az.IotHub</span></span>
* <span data-ttu-id="f1219-1826">Lägg till stöd för att återskapa principnycklar för auktorisering.</span><span class="sxs-lookup"><span data-stu-id="f1219-1826">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f1219-1827">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f1219-1827">Az.Network</span></span>
* <span data-ttu-id="f1219-1828">”RoutingPreference” har lagts till i offentliga IP-taggar</span><span class="sxs-lookup"><span data-stu-id="f1219-1828">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="f1219-1829">Förbättra exempel för referensdokumentation om ”Get-AzNetworkServiceTag”</span><span class="sxs-lookup"><span data-stu-id="f1219-1829">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f1219-1830">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f1219-1830">Az.PolicyInsights</span></span>
* <span data-ttu-id="f1219-1831">Åtgärda problem med null-referens i Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="f1219-1831">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="f1219-1832">Mer information här: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="f1219-1832">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f1219-1833">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f1219-1833">Az.OperationalInsights</span></span>
* <span data-ttu-id="f1219-1834">Modellen för CustomLog-datakälla som returneras i Get-AzOperationalInsightsDataSource har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="f1219-1834">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f1219-1835">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f1219-1835">Az.RecoveryServices</span></span>
* <span data-ttu-id="f1219-1836">Kommandot get-policy för IaaSVM:er har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="f1219-1836">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="f1219-1837">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f1219-1837">Az.Resources</span></span>
    - <span data-ttu-id="f1219-1838">Korrigera hjälptext för den översta parametern i Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="f1219-1838">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="f1219-1839">Lägg till växlingsstöd på klientsidan för Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="f1219-1839">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="f1219-1840">Lägg till nya parametrar för Set-AzPolicyAssignment, -PolicyParameters och -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="f1219-1840">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="f1219-1841">En mängd dokument- och exempeluppdateringar för Policy-cmdletar</span><span class="sxs-lookup"><span data-stu-id="f1219-1841">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="f1219-1842">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f1219-1842">Az.ServiceBus</span></span>
* <span data-ttu-id="f1219-1843">Korrigering av problem #4938 – New-AzureRmServiceBusQueue returnerar BadRequest vid konfiguration av MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="f1219-1843">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="f1219-1844">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f1219-1844">Az.Sql</span></span>
* <span data-ttu-id="f1219-1845">Lägg till cmdletar för instansredundansgrupper från förhandsversion till offentlig version</span><span class="sxs-lookup"><span data-stu-id="f1219-1845">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="f1219-1846">Stöd för granskning för Azure SQL Server\Database med nya cmdletar.</span><span class="sxs-lookup"><span data-stu-id="f1219-1846">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="f1219-1847">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="f1219-1847">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="f1219-1848">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="f1219-1848">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="f1219-1849">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="f1219-1849">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="f1219-1850">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="f1219-1850">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="f1219-1851">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="f1219-1851">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="f1219-1852">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="f1219-1852">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="f1219-1853">Ta bort begränsningar för e-post från inställningarna för sårbarhetsbedömning</span><span class="sxs-lookup"><span data-stu-id="f1219-1853">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f1219-1854">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f1219-1854">Az.Storage</span></span>
* <span data-ttu-id="f1219-1855">Ändra två parametrar ”-IndexDocument” och ”-ErrorDocument404Path” från ”krävs” till ”valfri” i cmdlet:</span><span class="sxs-lookup"><span data-stu-id="f1219-1855">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="f1219-1856">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="f1219-1856">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="f1219-1857">Uppdatera hjälpen för Get-AzStorageBlobContent genom att lägga till ett exempel</span><span class="sxs-lookup"><span data-stu-id="f1219-1857">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="f1219-1858">Visa mer felinformation när cmdleten misslyckas med StorageException</span><span class="sxs-lookup"><span data-stu-id="f1219-1858">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="f1219-1859">Stöd för att skapa eller uppdatera lagringskonto med Azure Files AAD DS-autentisering</span><span class="sxs-lookup"><span data-stu-id="f1219-1859">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="f1219-1860">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f1219-1860">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="f1219-1861">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f1219-1861">Set-AzStorageAccount</span></span>
* <span data-ttu-id="f1219-1862">Stöd för att lista eller stänga filreferenser för en filresurs, filkatalog eller en fil</span><span class="sxs-lookup"><span data-stu-id="f1219-1862">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="f1219-1863">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="f1219-1863">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="f1219-1864">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="f1219-1864">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="f1219-1865">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="f1219-1865">Az.StorageSync</span></span>
* <span data-ttu-id="f1219-1866">Den här modulen ingår nu som en del av `Az`-sammanslagningsmodulen</span><span class="sxs-lookup"><span data-stu-id="f1219-1866">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="f1219-1867">2.3.2 – juni 2019</span><span class="sxs-lookup"><span data-stu-id="f1219-1867">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f1219-1868">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f1219-1868">Az.Accounts</span></span>
* <span data-ttu-id="f1219-1869">Åtgärda bugg med felaktiga webbadresser som i vissa fall användes för Functions-anrop</span><span class="sxs-lookup"><span data-stu-id="f1219-1869">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="f1219-1870">Mer information här: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="f1219-1870">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="f1219-1871">Åtgärda problem med alias från AzureRM i Az-cmdletar</span><span class="sxs-lookup"><span data-stu-id="f1219-1871">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="f1219-1872">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="f1219-1872">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="f1219-1873">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="f1219-1873">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f1219-1874">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f1219-1874">Az.Compute</span></span>
* <span data-ttu-id="f1219-1875">Parameteruppsättningarna New-AzVm och New-AzVmss accepterar nu parametern ”ProximityPlacementGroup”.</span><span class="sxs-lookup"><span data-stu-id="f1219-1875">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="f1219-1876">Stavfel i referensdokumentationen för ”New-AzVM” har korrigerats</span><span class="sxs-lookup"><span data-stu-id="f1219-1876">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="f1219-1877">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="f1219-1877">Az.Dns</span></span>
* <span data-ttu-id="f1219-1878">Stavfel i hjälpexempel för ”Set-AzDnsZone” har korrigerats.</span><span class="sxs-lookup"><span data-stu-id="f1219-1878">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="f1219-1879">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="f1219-1879">Az.EventGrid</span></span>
* <span data-ttu-id="f1219-1880">Har uppdaterats för att använda API-versionen 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="f1219-1880">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="f1219-1881">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="f1219-1881">New cmdlets:</span></span>
    - <span data-ttu-id="f1219-1882">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="f1219-1882">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="f1219-1883">Skapar en ny Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="f1219-1883">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="f1219-1884">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="f1219-1884">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="f1219-1885">Hämtar information om en Event Grid-domän eller hämtar en lista med alla Event Grid-domäner i den aktuella Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="f1219-1885">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="f1219-1886">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="f1219-1886">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="f1219-1887">Tar bort en Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="f1219-1887">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="f1219-1888">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="f1219-1888">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="f1219-1889">Återskapar nyckeln för delad åtkomst för en Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="f1219-1889">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="f1219-1890">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="f1219-1890">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="f1219-1891">Hämtar de nycklar för delad åtkomst som används för att publicera händelser till en Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="f1219-1891">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="f1219-1892">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="f1219-1892">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="f1219-1893">Skapar ett nytt Azure Event Grid-domänämne.</span><span class="sxs-lookup"><span data-stu-id="f1219-1893">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="f1219-1894">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="f1219-1894">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="f1219-1895">Hämtar information om ett Event Grid-domänämne eller hämtar en lista med alla Event Grid-domänämnen under en specifik Event Grid-domän i nuvarande Azure</span><span class="sxs-lookup"><span data-stu-id="f1219-1895">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="f1219-1896">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="f1219-1896">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="f1219-1897">Tar bort ett befintligt Azure Event Grid-domänämne.</span><span class="sxs-lookup"><span data-stu-id="f1219-1897">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="f1219-1898">Uppdaterade cmdletar:</span><span class="sxs-lookup"><span data-stu-id="f1219-1898">Updated cmdlets:</span></span>
    - <span data-ttu-id="f1219-1899">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="f1219-1899">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="f1219-1900">Lägg till nya obligatoriska parametrar för att stödja piping för den nya Event Grid-domänen och Event Grid-domänämnet för att göra det möjligt att skapa nya händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="f1219-1900">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="f1219-1901">Lägg till nya obligatoriska parametrar för att ange det nya Event Grid-domännamnet och/eller namnet på Event Grid-domänämnet för att göra det möjligt att skapa nya händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="f1219-1901">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="f1219-1902">Lägg till ny parameteruppsättningar för domäner och domänämnen för att göra det möjligt att återanvända befintliga parametrar (t.ex. EndPointType, SubjectBeginsWith osv).</span><span class="sxs-lookup"><span data-stu-id="f1219-1902">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="f1219-1903">Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="f1219-1903">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="f1219-1904">Förfallodatum för händelseprenumeration</span><span class="sxs-lookup"><span data-stu-id="f1219-1904">Event subscription expiration date,</span></span>
            - <span data-ttu-id="f1219-1905">Avancerade filterparametrar.</span><span class="sxs-lookup"><span data-stu-id="f1219-1905">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="f1219-1906">Lägg till ny uppräkning för servicebusqueue som mål.</span><span class="sxs-lookup"><span data-stu-id="f1219-1906">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="f1219-1907">Tillåt inte användning av ”Alla” i alternativet -IncludedEventType och ersätt det med</span><span class="sxs-lookup"><span data-stu-id="f1219-1907">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="f1219-1908">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="f1219-1908">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="f1219-1909">Lägg till ny valfria parametrar (Top, ODataQuery och NextLink) för att stödja sidnumrering och filtrering av resultat.</span><span class="sxs-lookup"><span data-stu-id="f1219-1909">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="f1219-1910">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="f1219-1910">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="f1219-1911">Lägg till nya obligatoriska parametrar för att stödja piping för en Event Grid-domän och Event Grid-domänämnen för att göra det möjligt att ta bort befintliga händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="f1219-1911">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="f1219-1912">Lägg till nya obligatoriska parametrar för att ange Event Grid-domännamnet och/eller namnet på Event Grid-domänämnet för att göra det möjligt att ta bort befintliga händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="f1219-1912">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="f1219-1913">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f1219-1913">Az.FrontDoor</span></span>
* <span data-ttu-id="f1219-1914">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="f1219-1914">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="f1219-1915">Lägg till stöd för transformeringar och nytt värde för automatisk komplettering för operatorer (RegEx)</span><span class="sxs-lookup"><span data-stu-id="f1219-1915">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="f1219-1916">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="f1219-1916">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="f1219-1917">Lägg till nya värden för automatisk komplettering</span><span class="sxs-lookup"><span data-stu-id="f1219-1917">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f1219-1918">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f1219-1918">Az.Network</span></span>
* <span data-ttu-id="f1219-1919">Lägg till stöd för resurs för virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="f1219-1919">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="f1219-1920">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="f1219-1920">New cmdlets</span></span>
        - <span data-ttu-id="f1219-1921">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="f1219-1921">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="f1219-1922">Lägg till AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="f1219-1922">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="f1219-1923">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="f1219-1923">New cmdlets</span></span>
        - <span data-ttu-id="f1219-1924">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="f1219-1924">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="f1219-1925">Lägg till PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f1219-1925">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="f1219-1926">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="f1219-1926">New cmdlets</span></span>
        - <span data-ttu-id="f1219-1927">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f1219-1927">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="f1219-1928">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f1219-1928">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="f1219-1929">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f1219-1929">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="f1219-1930">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="f1219-1930">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="f1219-1931">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f1219-1931">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="f1219-1932">Lägg till PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f1219-1932">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="f1219-1933">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="f1219-1933">New cmdlets</span></span>
        - <span data-ttu-id="f1219-1934">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f1219-1934">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="f1219-1935">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f1219-1935">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="f1219-1936">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f1219-1936">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="f1219-1937">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="f1219-1937">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="f1219-1938">Nedanstående kommandon för funktionen har uppdaterats: Flaggan UseLocalAzureIpAddress på VpnConnection</span><span class="sxs-lookup"><span data-stu-id="f1219-1938">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="f1219-1939">New-AzVpnConnection har uppdaterats: Den valfria parametern -UseLocalAzureIpAddress har lagts till för att visa att en lokal IP-adress i Azure ska användas som källadress när anslutningen initieras.</span><span class="sxs-lookup"><span data-stu-id="f1219-1939">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="f1219-1940">Set-AzVpnConnection har uppdaterats: Den valfria parametern -UseLocalAzureIpAddress har lagts till för att visa att en lokal IP-adress i Azure ska användas som källadress när anslutningen initieras.</span><span class="sxs-lookup"><span data-stu-id="f1219-1940">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="f1219-1941">Det skrivskyddade fältet PeeredConnections har lagts till i ExpressRoute-peering.</span><span class="sxs-lookup"><span data-stu-id="f1219-1941">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="f1219-1942">Det skrivskyddade fältet GlobalReachEnabled har lagts till i ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="f1219-1942">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="f1219-1943">Ett attribut för icke-bakåtkompatibla ändringar har lagts till för att lyfta fram utfasning av fältet AllowGlobalReach i modellen ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f1219-1943">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="f1219-1944">Problem 8756 har åtgärdats: Fel vid användning av TargetListenerID med AzApplicationGatewayRedirectConfiguration-cmdletar</span><span class="sxs-lookup"><span data-stu-id="f1219-1944">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="f1219-1945">En bugg i New-AzApplicationGatewayPathRuleConfig som gjorde att regeluppsättningen för att återskapa inte kunde anges har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="f1219-1945">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="f1219-1946">Visningen av VirtualNetworkTaps i NetworkInterfaceIpConfiguration har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="f1219-1946">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="f1219-1947">Cortex Get-cmdletar för att visa en lista med alla delar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="f1219-1947">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="f1219-1948">Funktionen för att skapa VirtualHub-referenser för ExpressRouteGateways och VpnGateway har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="f1219-1948">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="f1219-1949">Stöd för tillgänglighetszoner i AzureFirewall och NatGateway har lagts till</span><span class="sxs-lookup"><span data-stu-id="f1219-1949">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="f1219-1950">Cmdleten Get-AzNetworkServiceTag har lagts till</span><span class="sxs-lookup"><span data-stu-id="f1219-1950">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="f1219-1951">Lägg till stöd för flera offentliga IP-adresser för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="f1219-1951">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="f1219-1952">Cmdleten New-AzFirewall har uppdaterats:</span><span class="sxs-lookup"><span data-stu-id="f1219-1952">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="f1219-1953">Parametern -PublicIpAddress som accepterar ett eller flera offentliga IP-adressobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="f1219-1953">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="f1219-1954">Parametern -VirtualNetwork som accepterar ett virtuellt nätverksobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="f1219-1954">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="f1219-1955">Metoderna AddPublicIpAddress och RemovePublicIpAddress har lagts till på brandväggsobjekt – dessa accepterar ett offentligt IP-adressobjekt som indata</span><span class="sxs-lookup"><span data-stu-id="f1219-1955">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="f1219-1956">Inaktuella parametrar -PublicIpName och -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="f1219-1956">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="f1219-1957">Nedanstående kommandon för funktionen har uppdaterats: Ange autentiseringsalternativ för VpnClient AAD till resurser för virtuella nätverksgatewayer.</span><span class="sxs-lookup"><span data-stu-id="f1219-1957">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="f1219-1958">New-AzVirtualNetworkGateway har uppdaterats: De valfria parametrarna AadTenantUri, AadAudienceId och AadIssuerUri för att ange VpnClient AAD-autentiseringsalternativ på en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="f1219-1958">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="f1219-1959">Set-AzVirtualNetworkGateway har uppdaterats: De valfria parametrarna AadTenantUri, AadAudienceId och AadIssuerUri för att ange VpnClient AAD-autentiseringsalternativ på en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="f1219-1959">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="f1219-1960">Set-AzVirtualNetworkGateway har uppdaterats: Den valfria växelparametern RemoveAadAuthentication som tar bort VpnClient AAD-autentiseringsalternativ från en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="f1219-1960">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f1219-1961">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f1219-1961">Az.OperationalInsights</span></span>
* <span data-ttu-id="f1219-1962">Aktivera prisnivån **pergb2018** i kommandot ”New-AzureRmOperationalInsightsWorkspace”</span><span class="sxs-lookup"><span data-stu-id="f1219-1962">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="f1219-1963">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f1219-1963">Az.Resources</span></span>
* <span data-ttu-id="f1219-1964">Stöd för ytterligare alternativ för att exportera en mall</span><span class="sxs-lookup"><span data-stu-id="f1219-1964">Support for additional Template Export options</span></span>
    - <span data-ttu-id="f1219-1965">Lägg till parametern ”-SkipResourceNameParameterization” till Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f1219-1965">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="f1219-1966">Lägg till parametern ”-SkipAllParameterization” till Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f1219-1966">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="f1219-1967">Lägg till parametern ”-Resource” till Export-AzResourceGroup för exporterad resursfiltrering</span><span class="sxs-lookup"><span data-stu-id="f1219-1967">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f1219-1968">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f1219-1968">Az.ServiceFabric</span></span>
* <span data-ttu-id="f1219-1969">Åtgärda att fel tumavtryck används vid tilläggning av certifikat i ByExistingKeyVault i vissa fall</span><span class="sxs-lookup"><span data-stu-id="f1219-1969">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="f1219-1970">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f1219-1970">Az.Sql</span></span>
* <span data-ttu-id="f1219-1971">Åtgärda suffix för lagringsslutpunkt i Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="f1219-1971">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="f1219-1972">Åtgärda att aktivering av Advanced Data Security åsidosätter Advanced Threat Protection-princip</span><span class="sxs-lookup"><span data-stu-id="f1219-1972">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="f1219-1973">Nya cmdletar för Management.Sql som gör att kunderna kan lägga till nycklar för transparent datakryptering (TDE) och ange TDE-skydd för hanterade instanser</span><span class="sxs-lookup"><span data-stu-id="f1219-1973">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="f1219-1974">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="f1219-1974">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="f1219-1975">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="f1219-1975">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="f1219-1976">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="f1219-1976">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="f1219-1977">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="f1219-1977">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="f1219-1978">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="f1219-1978">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f1219-1979">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f1219-1979">Az.Storage</span></span>
* <span data-ttu-id="f1219-1980">Stöd för typerna FileStorage och SkuName Premium_ZRS när lagringskonton skapas</span><span class="sxs-lookup"><span data-stu-id="f1219-1980">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="f1219-1981">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f1219-1981">New-AzStorageAccount</span></span>
* <span data-ttu-id="f1219-1982">Beskrivningen av cmdleten för bloboföränderlighet har förtydligats</span><span class="sxs-lookup"><span data-stu-id="f1219-1982">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="f1219-1983">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="f1219-1983">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f1219-1984">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f1219-1984">Az.Websites</span></span>
* <span data-ttu-id="f1219-1985">Optimerar Get-AzWebAppCertificate för att filtrera efter resursgrupp på servern i stället för klienten</span><span class="sxs-lookup"><span data-stu-id="f1219-1985">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="f1219-1986">Lägger till växlingsparametern -UseDisasterRecovery till Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="f1219-1986">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="f1219-1987">2.2.0 – juni 2019</span><span class="sxs-lookup"><span data-stu-id="f1219-1987">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="f1219-1988">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f1219-1988">Az.Cdn</span></span>
* <span data-ttu-id="f1219-1989">Uppdaterade cmdletar för att ge stöd för rulesEngine-funktion baserat på API-version 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="f1219-1989">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f1219-1990">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f1219-1990">Az.Compute</span></span>
* <span data-ttu-id="f1219-1991">Lade till parameter `NoWait` som startar åtgärden och returnerar omedelbart, innan åtgärden har slutförts.</span><span class="sxs-lookup"><span data-stu-id="f1219-1991">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="f1219-1992">Uppdaterade cmdletar:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="f1219-1992">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f1219-1993">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f1219-1993">Az.EventHub</span></span>
* <span data-ttu-id="f1219-1994">Korrigering för #9231 – Get-AzEventHubNamespace returnerar inga taggar</span><span class="sxs-lookup"><span data-stu-id="f1219-1994">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="f1219-1995">Korrigering för #9230 – Get-AzEventHubNamespace returnerar ResourceGroup istället för ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1219-1995">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f1219-1996">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f1219-1996">Az.Network</span></span>
* <span data-ttu-id="f1219-1997">Uppdatera ResourceId och InputObject för NAT-gateway</span><span class="sxs-lookup"><span data-stu-id="f1219-1997">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="f1219-1998">Lägg till alias för ResourceId och InputObject</span><span class="sxs-lookup"><span data-stu-id="f1219-1998">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f1219-1999">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f1219-1999">Az.PolicyInsights</span></span>
* <span data-ttu-id="f1219-2000">Åtgärda Null-referensproblem i Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="f1219-2000">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f1219-2001">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f1219-2001">Az.RecoveryServices</span></span>
* <span data-ttu-id="f1219-2002">Minsta kvarhållning för IaaSVM-policy i dagar ändrat till 7 från 1</span><span class="sxs-lookup"><span data-stu-id="f1219-2002">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="f1219-2003">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f1219-2003">Az.ServiceBus</span></span>
* <span data-ttu-id="f1219-2004">Korrigering för ärende #9182 – Get-AzServiceBusNamespace returnerar ResourceGroup istället för ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1219-2004">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f1219-2005">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f1219-2005">Az.ServiceFabric</span></span>
* <span data-ttu-id="f1219-2006">Åtgärda stavfel i felmeddelandet för Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="f1219-2006">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="f1219-2007">Åtgärda saknat tecken i Service Fabric-kommandorader</span><span class="sxs-lookup"><span data-stu-id="f1219-2007">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="f1219-2008">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f1219-2008">Az.Sql</span></span>
* <span data-ttu-id="f1219-2009">Lägg till parametern DnsZonePartner för New-AzureSqlInstance-cmdlet för att ge stöd för AutoDr för hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="f1219-2009">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="f1219-2010">Avvecklar cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="f1219-2010">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="f1219-2011">Döp om cmdletar för hotidentifiering till Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="f1219-2011">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="f1219-2012">Parametrarna New-AzSqlInstance -StorageSizeInGB och -LicenseType är nu valfria.</span><span class="sxs-lookup"><span data-stu-id="f1219-2012">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f1219-2013">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f1219-2013">Az.Websites</span></span>
* <span data-ttu-id="f1219-2014">åtgärdar problemet där användningen av Set-AzWebApp och Set-AzWebAppSlot med -WebApp-egenskap tog bort taggarna</span><span class="sxs-lookup"><span data-stu-id="f1219-2014">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="f1219-2015">2.1.0 – maj 2019</span><span class="sxs-lookup"><span data-stu-id="f1219-2015">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="f1219-2016">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f1219-2016">Az.ApiManagement</span></span>
* <span data-ttu-id="f1219-2017">Skapade nya cmdletar för att hantera diagnostik för global- och API-omfång</span><span class="sxs-lookup"><span data-stu-id="f1219-2017">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="f1219-2018">**Get-AzApiManagementDiagnostic** – Skaffa diagnostik konfigurerad för global- eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="f1219-2018">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="f1219-2019">**New-AzApiManagementDiagnostic** – Skapa ny diagnostik för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="f1219-2019">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="f1219-2020">**New-AzApiManagementHttpMessageDiagnostic** – Skapa diagnostikinställning om vilka rubriker som ska loggas och storleken på brödtextbyte</span><span class="sxs-lookup"><span data-stu-id="f1219-2020">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="f1219-2021">**New-AzApiManagementPipelineDiagnosticSetting** – Skapa diagnostikinställningar för inkommande/utgående HTTP-meddelanden till gatewayen.</span><span class="sxs-lookup"><span data-stu-id="f1219-2021">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="f1219-2022">**New-AzApiManagementSamplingSetting** – Skapa samplinginställningar för begäranden/svar för en diagnostik</span><span class="sxs-lookup"><span data-stu-id="f1219-2022">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="f1219-2023">**Remove-AzApiManagementDiagnostic** – Ta bort en diagnostikenhet för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="f1219-2023">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="f1219-2024">**Set-AzApiManagementDiagnostic** – Uppdatera en diagnostikenhet för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="f1219-2024">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="f1219-2025">Skapade nya cmdletar för hantering av cacheminne i ApiManagement-tjänsten</span><span class="sxs-lookup"><span data-stu-id="f1219-2025">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="f1219-2026">**Get-AzApiManagementCache** – Hämta information om cacheminnet som anges av identifierare eller alla cacheminnen</span><span class="sxs-lookup"><span data-stu-id="f1219-2026">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="f1219-2027">**New-AzApiManagementCache** – Skapa ett nytt default-cacheminne eller cacheminne i en viss Azure-region</span><span class="sxs-lookup"><span data-stu-id="f1219-2027">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="f1219-2028">**Remove-AzApiManagementCache** – Ta bort ett cacheminne</span><span class="sxs-lookup"><span data-stu-id="f1219-2028">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="f1219-2029">**Remove-AzApiManagementCache** – Ta bort ett cacheminne</span><span class="sxs-lookup"><span data-stu-id="f1219-2029">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="f1219-2030">Skapade nya cmdletar för hantering av API-schema</span><span class="sxs-lookup"><span data-stu-id="f1219-2030">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="f1219-2031">**New-AzApiManagementSchema** – Skapa ett nytt schema för ett API</span><span class="sxs-lookup"><span data-stu-id="f1219-2031">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="f1219-2032">**Get-AzApiManagementSchema** – Hämta de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="f1219-2032">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="f1219-2033">**Remove-AzApiManagementSchema** – Ta bort de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="f1219-2033">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="f1219-2034">**Set-AzApiManagementSchema** – Uppdatera de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="f1219-2034">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="f1219-2035">Skapa ny cmdlet för att generera en användartoken.</span><span class="sxs-lookup"><span data-stu-id="f1219-2035">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="f1219-2036">**New-AzApiManagementUserToken** – Skapa en ny användartoken som enligt standardinställning är giltig i 8 timmar. Token för GIT-användaren kan skapas med den här cmdleten./</span><span class="sxs-lookup"><span data-stu-id="f1219-2036">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="f1219-2037">Skapade en ny cmdlet för att hämta nätverksstatus</span><span class="sxs-lookup"><span data-stu-id="f1219-2037">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="f1219-2038">**Get-AzApiManagementNetworkStatus** – Hämta nätverksstatusanslutningen för resurserna som API Management-tjänsten är beroende av.</span><span class="sxs-lookup"><span data-stu-id="f1219-2038">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="f1219-2039">Det här är användbart när du distribuerar ApiManagement-tjänsten i ett virtuellt nätverk och validerar om något beroende är brutet.</span><span class="sxs-lookup"><span data-stu-id="f1219-2039">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="f1219-2040">Uppdaterade cmdlet **New-AzApiManagement** för att hantera ApiManagement-tjänsten</span><span class="sxs-lookup"><span data-stu-id="f1219-2040">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="f1219-2041">Lade till stöd för den nya SKU:n Consumption</span><span class="sxs-lookup"><span data-stu-id="f1219-2041">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="f1219-2042">Aktiverade stöd för att slå på flaggan EnableClientCertificate för SKU:n Consumption</span><span class="sxs-lookup"><span data-stu-id="f1219-2042">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="f1219-2043">Den nya cmdleten **New-AzApiManagementSslSetting** gör det möjligt att ställa in TLS/SSL-inställningen på ”Backend” och ”Frontend” (serverdel och klientdel).</span><span class="sxs-lookup"><span data-stu-id="f1219-2043">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="f1219-2044">Det här kan också användas till att konfigurera chiffer som 3DES och ServerProtocols som Http2 för Frontend för en ApiManagement-tjänst.</span><span class="sxs-lookup"><span data-stu-id="f1219-2044">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="f1219-2045">Stöd har lagts till för att konfigurera värdnamnet DeveloperPortal på ApiManagement-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="f1219-2045">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="f1219-2046">Uppdaterade cmdletar **Get-AzApiManagementSsoToken** för att ta PsApiManagement-objekt som indata</span><span class="sxs-lookup"><span data-stu-id="f1219-2046">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="f1219-2047">Uppdaterad cmdleten för att visa infogade felmeddelanden</span><span class="sxs-lookup"><span data-stu-id="f1219-2047">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="f1219-2048">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Felkod: Felmeddelande av typen ValidationError: Ett eller flera fält innehåller felaktiga värden: Felinformation:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="f1219-2048">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="f1219-2049">Uppdaterade cmdlet **Export-AzApiManagementApi** för att exportera API:er i OpenApi 3.0-format</span><span class="sxs-lookup"><span data-stu-id="f1219-2049">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="f1219-2050">Uppdaterade cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="f1219-2050">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="f1219-2051">Importera API från dokumentspecifikationen OpenApi 3.0</span><span class="sxs-lookup"><span data-stu-id="f1219-2051">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="f1219-2052">Om du vill åsidosätta egenskapen PsApiManagementSchema specificerad i ett dokument (Swagger, Wadl, Wsdl, OpenApi).</span><span class="sxs-lookup"><span data-stu-id="f1219-2052">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="f1219-2053">Åsidosätta egenskapen ServiceUrl som specificeras i ett dokument.</span><span class="sxs-lookup"><span data-stu-id="f1219-2053">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="f1219-2054">Uppdaterade cmdlet **Get-AzApiManagementPolicy** för att returnera policy i undantaget format av typen icke-XML med rawxml</span><span class="sxs-lookup"><span data-stu-id="f1219-2054">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="f1219-2055">Uppdaterade cmdlet **Set-AzApiManagementPolicy** för att godkänna policy i undantaget format av typen icke-XML med rawxml och XML undantaget med xml</span><span class="sxs-lookup"><span data-stu-id="f1219-2055">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="f1219-2056">Uppdaterad cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="f1219-2056">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="f1219-2057">Konfigurera API med OpenId auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="f1219-2057">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="f1219-2058">Skapa ett API i ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="f1219-2058">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="f1219-2059">Klona ett API med SourceApiId och SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="f1219-2059">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="f1219-2060">Möjlighet att konfigurera SubscriptionRequired i API-omfattningen.</span><span class="sxs-lookup"><span data-stu-id="f1219-2060">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="f1219-2061">Uppdaterad cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="f1219-2061">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="f1219-2062">Konfigurera API med OpenId auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="f1219-2062">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="f1219-2063">Uppdatera ett API till ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="f1219-2063">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="f1219-2064">Möjlighet att konfigurera SubscriptionRequired i API-omfattningen.</span><span class="sxs-lookup"><span data-stu-id="f1219-2064">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="f1219-2065">Uppdaterad cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="f1219-2065">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="f1219-2066">Klona en befintlig version med hjälp av SourceApiRevision (kopiera taggar, produkter, åtgärder och principer).</span><span class="sxs-lookup"><span data-stu-id="f1219-2066">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="f1219-2067">Den nya revisionen antar ApiId från den överordnade instansen.</span><span class="sxs-lookup"><span data-stu-id="f1219-2067">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="f1219-2068">Tillhandahålla ApiRevisionDescription</span><span class="sxs-lookup"><span data-stu-id="f1219-2068">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="f1219-2069">Åsidosätta ServiceUrl vid kloning av ett API.</span><span class="sxs-lookup"><span data-stu-id="f1219-2069">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="f1219-2070">Uppdaterad cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="f1219-2070">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="f1219-2071">Konfigurera AAD eller AADB2C med en Authority</span><span class="sxs-lookup"><span data-stu-id="f1219-2071">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="f1219-2072">Konfigurera SignupPolicy, SigninPolicy, ProfileEditingPolicy och PasswordResetPolicy</span><span class="sxs-lookup"><span data-stu-id="f1219-2072">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="f1219-2073">Uppdaterad cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="f1219-2073">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="f1219-2074">Kompensera för ny SubscriptonModel med Scope och UserId</span><span class="sxs-lookup"><span data-stu-id="f1219-2074">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="f1219-2075">Kompensera för gammal prenumerationsmodell med ProductId och UserId</span><span class="sxs-lookup"><span data-stu-id="f1219-2075">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="f1219-2076">Lägg till funktion för att aktivera AllowTracing på prenumerationsnivå.</span><span class="sxs-lookup"><span data-stu-id="f1219-2076">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="f1219-2077">Uppdaterad cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="f1219-2077">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="f1219-2078">Kompensera för ny SubscriptonModel med Scope och UserId</span><span class="sxs-lookup"><span data-stu-id="f1219-2078">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="f1219-2079">Kompensera för gammal prenumerationsmodell med ProductId och UserId</span><span class="sxs-lookup"><span data-stu-id="f1219-2079">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="f1219-2080">Lägg till funktion för att aktivera AllowTracing på prenumerationsnivå.</span><span class="sxs-lookup"><span data-stu-id="f1219-2080">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="f1219-2081">Uppdaterade följande cmdletar för att acceptera ResourceId som indata</span><span class="sxs-lookup"><span data-stu-id="f1219-2081">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="f1219-2082">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f1219-2082">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="f1219-2083">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="f1219-2083">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="f1219-2084">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="f1219-2084">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="f1219-2085">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="f1219-2085">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="f1219-2086">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="f1219-2086">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="f1219-2087">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="f1219-2087">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="f1219-2088">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="f1219-2088">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="f1219-2089">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="f1219-2089">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="f1219-2090">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="f1219-2090">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="f1219-2091">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="f1219-2091">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="f1219-2092">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="f1219-2092">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="f1219-2093">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="f1219-2093">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f1219-2094">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f1219-2094">Az.Automation</span></span>
* <span data-ttu-id="f1219-2095">Uppdaterade Get-AzAutomationJobOutputRecord för att hantera postvärden av typen JSON och Text.</span><span class="sxs-lookup"><span data-stu-id="f1219-2095">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="f1219-2096">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="f1219-2096">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="f1219-2097">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="f1219-2097">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="f1219-2098">Ändrade beteende för Start-AzAutomationDscCompilationJob till att bara starta jobbet istället för att vänta på slutförandet.</span><span class="sxs-lookup"><span data-stu-id="f1219-2098">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="f1219-2099">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="f1219-2099">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="f1219-2100">Korrigering för Get-AzAutomationDscNode när using -Name returnerar alla noder.</span><span class="sxs-lookup"><span data-stu-id="f1219-2100">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="f1219-2101">Nu returnerar den endast den matchande noden.</span><span class="sxs-lookup"><span data-stu-id="f1219-2101">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f1219-2102">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f1219-2102">Az.Compute</span></span>
* <span data-ttu-id="f1219-2103">Lägg till parametrarna ProtectFromScaleIn och ProtectFromScaleSetAction i cmdleten Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="f1219-2103">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="f1219-2104">Nu är standardinställningen att vimpelparametern New-AzVM använder en tillgänglig plats om USA, östra inte stöds</span><span class="sxs-lookup"><span data-stu-id="f1219-2104">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f1219-2105">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f1219-2105">Az.DataLakeStore</span></span>
* <span data-ttu-id="f1219-2106">Uppdatera ADLS-sdk för att använda httpclient, integrera dataplanstestning med Azure-ramverk</span><span class="sxs-lookup"><span data-stu-id="f1219-2106">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f1219-2107">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f1219-2107">Az.Monitor</span></span>
* <span data-ttu-id="f1219-2108">Korrigera felaktiga parameternamn i hjälpexempel</span><span class="sxs-lookup"><span data-stu-id="f1219-2108">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f1219-2109">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f1219-2109">Az.Network</span></span>
* <span data-ttu-id="f1219-2110">Lägg till flaggan DisableBgpRoutePropagation i utdata för effektiv routningstabell</span><span class="sxs-lookup"><span data-stu-id="f1219-2110">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="f1219-2111">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="f1219-2111">Updated cmdlet:</span></span>
        - <span data-ttu-id="f1219-2112">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="f1219-2112">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="f1219-2113">Åtgärda dubbelstreck i dokumentationen New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f1219-2113">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="f1219-2114">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f1219-2114">Az.Resources</span></span>
* <span data-ttu-id="f1219-2115">Lägg till ny cmdlet Get-AzureRmDenyAssignment för att hämta tilldelningsnekanden</span><span class="sxs-lookup"><span data-stu-id="f1219-2115">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="f1219-2116">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f1219-2116">Az.Sql</span></span>
* <span data-ttu-id="f1219-2117">Döp om Advanced Threat Protection-cmdletar för Advanced Data Security och aktivera Vulnerability Assessment som standard</span><span class="sxs-lookup"><span data-stu-id="f1219-2117">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="f1219-2118">2.0.0 – maj 2019</span><span class="sxs-lookup"><span data-stu-id="f1219-2118">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f1219-2119">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f1219-2119">Az.Accounts</span></span>
* <span data-ttu-id="f1219-2120">Uppdatera autentiseringsbiblioteket för att åtgärda ADFS-problem med autentisering av användarnamn/lösenord</span><span class="sxs-lookup"><span data-stu-id="f1219-2120">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f1219-2121">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f1219-2121">Az.CognitiveServices</span></span>
* <span data-ttu-id="f1219-2122">Visa endast Bing-ansvarsfriskrivning för Bing-sökningstjänster.</span><span class="sxs-lookup"><span data-stu-id="f1219-2122">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="f1219-2123">Förbättra felmeddelande när det inte går att skapa konton.</span><span class="sxs-lookup"><span data-stu-id="f1219-2123">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f1219-2124">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f1219-2124">Az.Compute</span></span>
* <span data-ttu-id="f1219-2125">Funktion för närhetsplaceringsgrupper.</span><span class="sxs-lookup"><span data-stu-id="f1219-2125">Proximity placement group feature.</span></span>
    - <span data-ttu-id="f1219-2126">Följande nya cmdletar har lagts till:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="f1219-2126">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="f1219-2127">Den nya parametern ProximityPlacementGroupId har lagts till i följande cmdletar:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="f1219-2127">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="f1219-2128">Parametern StorageAccountType har lagts till i New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="f1219-2128">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="f1219-2129">TargetRegion för New-AzGalleryImageVersion kan innehålla StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="f1219-2129">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="f1219-2130">Växlingsparametern SkipShutdown har lagts till i Stop-AzVM och Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f1219-2130">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="f1219-2131">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="f1219-2131">Breaking changes</span></span>
    - <span data-ttu-id="f1219-2132">Set-AzVMBootDiagnostics har ändrats till Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="f1219-2132">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="f1219-2133">Export-AzLogAnalyticThrottledRequests har ändrats till Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="f1219-2133">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="f1219-2134">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="f1219-2134">Az.DeploymentManager</span></span>
* <span data-ttu-id="f1219-2135">De första allmänt tillgängliga versionerna av cmdletar för Distributionshanteraren i Azure</span><span class="sxs-lookup"><span data-stu-id="f1219-2135">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="f1219-2136">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="f1219-2136">Az.Dns</span></span>
* <span data-ttu-id="f1219-2137">Automatisk delegering av DNS för NameServer</span><span class="sxs-lookup"><span data-stu-id="f1219-2137">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="f1219-2138">Det överordnade zonnamnet kan användas som ytterligare valfri parameter i cmdleten för att skapa DNS-zoner.</span><span class="sxs-lookup"><span data-stu-id="f1219-2138">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="f1219-2139">Lägger till NS-poster för en nyligen skapad underordnad zon i den överordnade zonen.</span><span class="sxs-lookup"><span data-stu-id="f1219-2139">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="f1219-2140">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f1219-2140">Az.FrontDoor</span></span>
* <span data-ttu-id="f1219-2141">De första allmänt tillgängliga versionerna av cmdletar för Azure FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f1219-2141">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="f1219-2142">Byt namn på WAF-cmdletar så att de omfattar ”Waf”</span><span class="sxs-lookup"><span data-stu-id="f1219-2142">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="f1219-2143">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f1219-2143">Az.HDInsight</span></span>
* <span data-ttu-id="f1219-2144">Två cmdletar har tagits bort:</span><span class="sxs-lookup"><span data-stu-id="f1219-2144">Removed two cmdlets:</span></span>
    - <span data-ttu-id="f1219-2145">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="f1219-2145">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="f1219-2146">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="f1219-2146">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="f1219-2147">En ny cmdlet har lagts till, Set-AzHDInsightGatewayCredential, som ersätter Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="f1219-2147">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="f1219-2148">Uppdatera cmdleten Get-AzHDInsightJobOutput för att skilja mellan läsarrollen och HDInsight-operatörsrollen:</span><span class="sxs-lookup"><span data-stu-id="f1219-2148">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="f1219-2149">Användare med läsarrollen måste uttryckligen ange parametern ”DefaultStorageAccountKey”, annars uppstår fel.</span><span class="sxs-lookup"><span data-stu-id="f1219-2149">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="f1219-2150">Användare med HDInsight-operatörsrollen påverkas inte.</span><span class="sxs-lookup"><span data-stu-id="f1219-2150">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f1219-2151">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f1219-2151">Az.Monitor</span></span>
* <span data-ttu-id="f1219-2152">Nya cmdletar för SQR API (schemalagd frågeregel)</span><span class="sxs-lookup"><span data-stu-id="f1219-2152">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="f1219-2153">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="f1219-2153">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="f1219-2154">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="f1219-2154">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="f1219-2155">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="f1219-2155">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="f1219-2156">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="f1219-2156">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="f1219-2157">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="f1219-2157">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="f1219-2158">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="f1219-2158">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="f1219-2159">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="f1219-2159">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="f1219-2160">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="f1219-2160">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="f1219-2161">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="f1219-2161">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="f1219-2162">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="f1219-2162">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="f1219-2163">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="f1219-2163">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="f1219-2164">[Mer](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information om SQR API</span><span class="sxs-lookup"><span data-stu-id="f1219-2164">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="f1219-2165">Az.Monitor.md har uppdaterats för att omfatta cmdletar för måttbaserade aviseringsregler i GenV2 (inte klassiska)</span><span class="sxs-lookup"><span data-stu-id="f1219-2165">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f1219-2166">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f1219-2166">Az.Network</span></span>
* <span data-ttu-id="f1219-2167">Lägg till stöd för NAT Gateway-resurs</span><span class="sxs-lookup"><span data-stu-id="f1219-2167">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="f1219-2168">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="f1219-2168">New cmdlets</span></span>
        - <span data-ttu-id="f1219-2169">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="f1219-2169">New-AzNatGateway</span></span>
        - <span data-ttu-id="f1219-2170">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="f1219-2170">Get-AzNatGateway</span></span>
        - <span data-ttu-id="f1219-2171">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="f1219-2171">Set-AzNatGateway</span></span>
        - <span data-ttu-id="f1219-2172">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="f1219-2172">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="f1219-2173">Uppdaterade cmdletar</span><span class="sxs-lookup"><span data-stu-id="f1219-2173">Updated cmdlets</span></span>
        - <span data-ttu-id="f1219-2174">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="f1219-2174">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="f1219-2175">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="f1219-2175">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="f1219-2176">Nedanstående kommandon för funktionen har uppdaterats: Ange/ta bort anpassade vägar på Brooklyn Gateway.</span><span class="sxs-lookup"><span data-stu-id="f1219-2176">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="f1219-2177">New-AzVirtualNetworkGateway har uppdaterats: Den valfria parametern -CustomRoute har lagts till för att ställa in adressprefix som anpassade vägar för att ange gateway.</span><span class="sxs-lookup"><span data-stu-id="f1219-2177">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="f1219-2178">Set-AzVirtualNetworkGateway har uppdaterats: Den valfria parametern -CustomRoute har lagts till för att ange adressprefix som anpassade vägar för att ange gateway.</span><span class="sxs-lookup"><span data-stu-id="f1219-2178">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f1219-2179">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f1219-2179">Az.PolicyInsights</span></span>
* <span data-ttu-id="f1219-2180">Stöd för att fråga efter information om principutvärdering.</span><span class="sxs-lookup"><span data-stu-id="f1219-2180">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="f1219-2181">Lägg till parametern ”-Expand” för Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="f1219-2181">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="f1219-2182">Stöd för -Expand PolicyEvaluationDetails.</span><span class="sxs-lookup"><span data-stu-id="f1219-2182">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f1219-2183">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f1219-2183">Az.RecoveryServices</span></span>
* <span data-ttu-id="f1219-2184">Stöd för att dela prenumeration mellan Azure och Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="f1219-2184">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="f1219-2185">Markering av kommande icke-bakåtkompatibla ändringar för Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="f1219-2185">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="f1219-2186">Korrigering för återställningsplan och åtgärdsplan i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="f1219-2186">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="f1219-2187">Korrigering för mappning av uppdateringsnätverk i Azure Site Recovery för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="f1219-2187">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="f1219-2188">Korrigering för instruktioner för uppdateringsskydd i Azure Site Recovery för Azure till Azure för hanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="f1219-2188">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="f1219-2189">Andra mindre korrigeringar.</span><span class="sxs-lookup"><span data-stu-id="f1219-2189">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="f1219-2190">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="f1219-2190">Az.Relay</span></span>
* <span data-ttu-id="f1219-2191">Korrigera stavfel i kundriktade meddelanden</span><span class="sxs-lookup"><span data-stu-id="f1219-2191">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="f1219-2192">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f1219-2192">Az.ServiceBus</span></span>
* <span data-ttu-id="f1219-2193">Nya cmdletar har lagts till för NetworkRuleSet för namnområden</span><span class="sxs-lookup"><span data-stu-id="f1219-2193">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f1219-2194">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f1219-2194">Az.Storage</span></span>
* <span data-ttu-id="f1219-2195">Uppgradera till lagringsklientbiblioteket 10.0.1 (namnområdet för alla objekt från detta SDK ändras från ”Microsoft.WindowsAzure.Storage. *till ”Microsoft.Azure.Storage.* ”)</span><span class="sxs-lookup"><span data-stu-id="f1219-2195">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="f1219-2196">Uppgradera till Microsoft.Azure.Management.Storage 11.0.0 för att stödja den nya API-versionen 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="f1219-2196">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="f1219-2197">Standardlagringskontot i Skapa lagringskonto ändras från ”Storage” till ”StorageV2”</span><span class="sxs-lookup"><span data-stu-id="f1219-2197">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="f1219-2198">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f1219-2198">New-AzStorageAccount</span></span>
* <span data-ttu-id="f1219-2199">Ändra lagringskontots cmdlet-utdata Sku.Name för att passa med indata-SkuName genom att lägga till ”-”. Till exempel ändras ”StandardLRS” till ”Standard_LRS”</span><span class="sxs-lookup"><span data-stu-id="f1219-2199">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="f1219-2200">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f1219-2200">New-AzStorageAccount</span></span>
    - <span data-ttu-id="f1219-2201">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f1219-2201">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="f1219-2202">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f1219-2202">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f1219-2203">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f1219-2203">Az.Websites</span></span>
* <span data-ttu-id="f1219-2204">Egenskapen ”typ” konfigureras nu för PSSite-objekt som returneras av Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="f1219-2204">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="f1219-2205">Get-AzWebApp\*Metrics och Get-AzAppServicePlanMetrics markeras som inaktuella</span><span class="sxs-lookup"><span data-stu-id="f1219-2205">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="f1219-2206">1.8.0 – april 2019</span><span class="sxs-lookup"><span data-stu-id="f1219-2206">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="f1219-2207">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="f1219-2207">Highlights since the last major release</span></span>
* <span data-ttu-id="f1219-2208">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="f1219-2208">General availability of `Az` module</span></span>
* <span data-ttu-id="f1219-2209">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="f1219-2209">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="f1219-2210">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="f1219-2210">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="f1219-2211">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="f1219-2211">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="f1219-2212">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="f1219-2212">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="f1219-2213">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="f1219-2213">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="f1219-2214">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="f1219-2214">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f1219-2215">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f1219-2215">Az.Accounts</span></span>
* <span data-ttu-id="f1219-2216">Uppdatera Uninstall-AzureRm för att ta bort moduler i Mac på ett korrekt sätt</span><span class="sxs-lookup"><span data-stu-id="f1219-2216">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="f1219-2217">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="f1219-2217">Az.Batch</span></span>
* <span data-ttu-id="f1219-2218">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="f1219-2218">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="f1219-2219">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f1219-2219">Az.Cdn</span></span>
* <span data-ttu-id="f1219-2220">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="f1219-2220">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f1219-2221">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f1219-2221">Az.CognitiveServices</span></span>
* <span data-ttu-id="f1219-2222">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="f1219-2222">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f1219-2223">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f1219-2223">Az.Compute</span></span>
* <span data-ttu-id="f1219-2224">Åtgärda problem med AEM-installationen om resurs-ID:n för diskar innehåller resourcegroups i gemener i resurs-ID:n</span><span class="sxs-lookup"><span data-stu-id="f1219-2224">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="f1219-2225">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="f1219-2225">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f1219-2226">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="f1219-2226">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f1219-2227">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f1219-2227">Az.DataFactory</span></span>
* <span data-ttu-id="f1219-2228">Lägg till SsisProperties om NodeCount inte är null för hanterad integreringskörning.</span><span class="sxs-lookup"><span data-stu-id="f1219-2228">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f1219-2229">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f1219-2229">Az.DataLakeStore</span></span>
* <span data-ttu-id="f1219-2230">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="f1219-2230">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="f1219-2231">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="f1219-2231">Az.EventGrid</span></span>
* <span data-ttu-id="f1219-2232">Hjälptexten för slutpunkten har uppdaterats för att visa att resurser ska skapas innan cmdletarna för att skapa/uppdatera händelseprenumerationer används.</span><span class="sxs-lookup"><span data-stu-id="f1219-2232">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f1219-2233">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f1219-2233">Az.EventHub</span></span>
* <span data-ttu-id="f1219-2234">Nya cmdletar har lagts till för NetworkRuleSet för namnområden</span><span class="sxs-lookup"><span data-stu-id="f1219-2234">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="f1219-2235">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f1219-2235">Az.HDInsight</span></span>
* <span data-ttu-id="f1219-2236">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="f1219-2236">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f1219-2237">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f1219-2237">Az.IotHub</span></span>
* <span data-ttu-id="f1219-2238">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="f1219-2238">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f1219-2239">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f1219-2239">Az.KeyVault</span></span>
* <span data-ttu-id="f1219-2240">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="f1219-2240">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f1219-2241">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="f1219-2241">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="f1219-2242">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="f1219-2242">Az.MachineLearning</span></span>
* <span data-ttu-id="f1219-2243">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="f1219-2243">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="f1219-2244">Az.Media</span><span class="sxs-lookup"><span data-stu-id="f1219-2244">Az.Media</span></span>
* <span data-ttu-id="f1219-2245">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="f1219-2245">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f1219-2246">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f1219-2246">Az.Monitor</span></span>
  * <span data-ttu-id="f1219-2247">Nya cmdletar för måttbaserad aviseringsregel i GenV2 (inte klassisk)</span><span class="sxs-lookup"><span data-stu-id="f1219-2247">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="f1219-2248">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="f1219-2248">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="f1219-2249">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="f1219-2249">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="f1219-2250">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="f1219-2250">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="f1219-2251">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="f1219-2251">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="f1219-2252">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="f1219-2252">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="f1219-2253">Monitor SDK har uppdaterats till version 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="f1219-2253">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f1219-2254">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f1219-2254">Az.Network</span></span>
* <span data-ttu-id="f1219-2255">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="f1219-2255">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f1219-2256">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="f1219-2256">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="f1219-2257">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="f1219-2257">Az.NotificationHubs</span></span>
* <span data-ttu-id="f1219-2258">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="f1219-2258">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f1219-2259">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f1219-2259">Az.OperationalInsights</span></span>
* <span data-ttu-id="f1219-2260">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="f1219-2260">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="f1219-2261">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="f1219-2261">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="f1219-2262">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="f1219-2262">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f1219-2263">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f1219-2263">Az.RecoveryServices</span></span>
* <span data-ttu-id="f1219-2264">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="f1219-2264">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f1219-2265">Tabellformatet för SQL i virtuella Azure-datorer har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="f1219-2265">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="f1219-2266">En alternativ metod för att hämta platser i AzureFileShare har lagts till</span><span class="sxs-lookup"><span data-stu-id="f1219-2266">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="f1219-2267">ScheduleRunDays i SchedulePolicy-objekt har uppdaterats enligt tidszon</span><span class="sxs-lookup"><span data-stu-id="f1219-2267">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="f1219-2268">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="f1219-2268">Az.RedisCache</span></span>
* <span data-ttu-id="f1219-2269">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="f1219-2269">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f1219-2270">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f1219-2270">Az.Resources</span></span>
* <span data-ttu-id="f1219-2271">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="f1219-2271">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="f1219-2272">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f1219-2272">Az.Sql</span></span>
* <span data-ttu-id="f1219-2273">Ersätt Monitor SDK-beroende med vanlig kod</span><span class="sxs-lookup"><span data-stu-id="f1219-2273">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="f1219-2274">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="f1219-2274">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f1219-2275">Förbättrad process för klassificering av flera kolumner.</span><span class="sxs-lookup"><span data-stu-id="f1219-2275">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="f1219-2276">Inkludera SKU-egenskaper (SKU-namn, serie, kapacitet) i svaret från Get-AzSqlServerServiceObjective och formatera som tabell som standard.</span><span class="sxs-lookup"><span data-stu-id="f1219-2276">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="f1219-2277">Möjlighet att använda Get-AzSqlServerServiceObjective efter plats utan att behöva en redan befintlig server i regionen.</span><span class="sxs-lookup"><span data-stu-id="f1219-2277">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="f1219-2278">Stöd för tidszonsparametern när hanterade instanser skapas.</span><span class="sxs-lookup"><span data-stu-id="f1219-2278">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="f1219-2279">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="f1219-2279">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f1219-2280">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f1219-2280">Az.Websites</span></span>
* <span data-ttu-id="f1219-2281">åtgärdar Set-AzWebApp och Set-AzWebAppSlot så att de inte tar bort taggar vid körning</span><span class="sxs-lookup"><span data-stu-id="f1219-2281">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="f1219-2282">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="f1219-2282">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f1219-2283">SDK för WebSites har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="f1219-2283">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="f1219-2284">Egenskapen AdminSiteName har tagits bort från PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="f1219-2284">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="f1219-2285">1.7.0 – april 2019</span><span class="sxs-lookup"><span data-stu-id="f1219-2285">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="f1219-2286">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="f1219-2286">Highlights since the last major release</span></span>
* <span data-ttu-id="f1219-2287">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="f1219-2287">General availability of `Az` module</span></span>
* <span data-ttu-id="f1219-2288">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="f1219-2288">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="f1219-2289">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="f1219-2289">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="f1219-2290">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="f1219-2290">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="f1219-2291">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="f1219-2291">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="f1219-2292">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="f1219-2292">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="f1219-2293">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="f1219-2293">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f1219-2294">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f1219-2294">Az.Accounts</span></span>
* <span data-ttu-id="f1219-2295">Add-AzEnvironment och Set-AzEnvironment har uppdaterats för att godkänna parametern AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="f1219-2295">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="f1219-2296">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f1219-2296">Az.AnalysisServices</span></span>
* <span data-ttu-id="f1219-2297">ServiceClient används i cmdletar för dataplan och den ursprungliga autentiseringslogiken har tagits bort</span><span class="sxs-lookup"><span data-stu-id="f1219-2297">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="f1219-2298">Add-AzureASAccount används för omslutning av Connect-AzAccount för att undvika en icke-bakåtkompatibel ändring</span><span class="sxs-lookup"><span data-stu-id="f1219-2298">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f1219-2299">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f1219-2299">Az.Automation</span></span>
* <span data-ttu-id="f1219-2300">Buggen för cmdleten New-AzAutomationSoftwareUpdateConfiguration för inkluderingar har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="f1219-2300">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="f1219-2301">Nu bör parametern IncludedKbNumber och IncludedPackageNameMask fungera.</span><span class="sxs-lookup"><span data-stu-id="f1219-2301">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="f1219-2302">Felkorrigering för dynamiska grupper i uppdateringshanteringen för azure automation</span><span class="sxs-lookup"><span data-stu-id="f1219-2302">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f1219-2303">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f1219-2303">Az.Compute</span></span>
* <span data-ttu-id="f1219-2304">Lägg till parametern HyperVGeneration i New-AzDiskConfig och New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="f1219-2304">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="f1219-2305">Tillåt att virtuella datorer skapas med galleribilder från andra klientorganisationer.</span><span class="sxs-lookup"><span data-stu-id="f1219-2305">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="f1219-2306">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="f1219-2306">Az.ContainerInstance</span></span>
* <span data-ttu-id="f1219-2307">Ett problem har åtgärdats i parametern -Command för New-AzContainerGroup som lade till ett avslutande tomt argument</span><span class="sxs-lookup"><span data-stu-id="f1219-2307">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f1219-2308">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f1219-2308">Az.DataFactory</span></span>
* <span data-ttu-id="f1219-2309">ADF .Net SDK-versionen har uppdaterats till 3.0.2</span><span class="sxs-lookup"><span data-stu-id="f1219-2309">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="f1219-2310">Cmdleten Set-AzDataFactoryV2 har uppdaterats med extra parametrar för inställningar som rör RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="f1219-2310">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f1219-2311">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f1219-2311">Az.Resources</span></span>
* <span data-ttu-id="f1219-2312">Förbättra hanteringen av providrar för Get-AzResource när parametrarna -ResourceId eller -ResourceGroupName, -Name och -ResourceType tillhandahålls</span><span class="sxs-lookup"><span data-stu-id="f1219-2312">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="f1219-2313">Förbättra felhanteringen för ”Test-AzDeployment” och ”Test-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="f1219-2313">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="f1219-2314">Hantera fel utanför distributionsvalideringen och ta med dem i kommandoutdata istället</span><span class="sxs-lookup"><span data-stu-id="f1219-2314">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="f1219-2315">Mer information här: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="f1219-2315">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="f1219-2316">Lägg till växlingsparametern -IgnoreDynamicParameters till en uppsättning av cmdletar för distribution för att hoppa över fråga i skript och jobbscenarier</span><span class="sxs-lookup"><span data-stu-id="f1219-2316">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="f1219-2317">Mer information här: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="f1219-2317">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="f1219-2318">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f1219-2318">Az.Sql</span></span>
* <span data-ttu-id="f1219-2319">Stöd för dataklassificering av databaser.</span><span class="sxs-lookup"><span data-stu-id="f1219-2319">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f1219-2320">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f1219-2320">Az.Storage</span></span>
* <span data-ttu-id="f1219-2321">Rapportera detaljfel när lagringskontext skapas med parametern -UseConnectedAccount, men utan inloggning på Azure-kontot</span><span class="sxs-lookup"><span data-stu-id="f1219-2321">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="f1219-2322">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="f1219-2322">New-AzStorageContext</span></span>
* <span data-ttu-id="f1219-2323">Stöd för att hantera Blob Service-egenskaper för ett angivet lagringskonto med API:et för hanteringsplan</span><span class="sxs-lookup"><span data-stu-id="f1219-2323">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="f1219-2324">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="f1219-2324">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="f1219-2325">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="f1219-2325">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="f1219-2326">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="f1219-2326">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="f1219-2327">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="f1219-2327">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="f1219-2328">Stöd för -AsJob-cmdletar för att ladda upp och ladda ned blobar och filer</span><span class="sxs-lookup"><span data-stu-id="f1219-2328">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="f1219-2329">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="f1219-2329">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="f1219-2330">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="f1219-2330">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="f1219-2331">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="f1219-2331">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="f1219-2332">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="f1219-2332">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="f1219-2333">1.6.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="f1219-2333">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="f1219-2334">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="f1219-2334">Highlights since the last major release</span></span>
* <span data-ttu-id="f1219-2335">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="f1219-2335">General availability of `Az` module</span></span>
* <span data-ttu-id="f1219-2336">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="f1219-2336">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="f1219-2337">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="f1219-2337">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="f1219-2338">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="f1219-2338">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="f1219-2339">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="f1219-2339">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="f1219-2340">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="f1219-2340">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="f1219-2341">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="f1219-2341">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f1219-2342">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f1219-2342">Az.Automation</span></span>
* <span data-ttu-id="f1219-2343">Azure Automation – ändring av uppdateringshantering för stöd för de nya funktionerna:</span><span class="sxs-lookup"><span data-stu-id="f1219-2343">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="f1219-2344">Dynamisk gruppering</span><span class="sxs-lookup"><span data-stu-id="f1219-2344">Dynamic grouping</span></span>
    * <span data-ttu-id="f1219-2345">För-/efterskrift</span><span class="sxs-lookup"><span data-stu-id="f1219-2345">Pre-Post script</span></span>
    * <span data-ttu-id="f1219-2346">Inställning för omstart</span><span class="sxs-lookup"><span data-stu-id="f1219-2346">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f1219-2347">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f1219-2347">Az.Compute</span></span>
* <span data-ttu-id="f1219-2348">Åtgärda problem med sökvägsmatchning i Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="f1219-2348">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="f1219-2349">Uppdatera Compute-klientbibliotek till 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="f1219-2349">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f1219-2350">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f1219-2350">Az.KeyVault</span></span>
* <span data-ttu-id="f1219-2351">Stöd för jokertecken för KeyVault-cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="f1219-2351">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f1219-2352">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f1219-2352">Az.Network</span></span>
* <span data-ttu-id="f1219-2353">Lägg till stöd för Threat Intelligence för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="f1219-2353">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="f1219-2354">Lägg till resurs för brandväggsprincip på översta nivå och anpassade regler för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="f1219-2354">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f1219-2355">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f1219-2355">Az.RecoveryServices</span></span>
* <span data-ttu-id="f1219-2356">SnapshotRetentionInDays har lagts till i Azure-principen för virtuella datorer för stöd av Instant RP</span><span class="sxs-lookup"><span data-stu-id="f1219-2356">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="f1219-2357">Pipe-stöd för avregistrering av container har lagts till</span><span class="sxs-lookup"><span data-stu-id="f1219-2357">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="f1219-2358">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f1219-2358">Az.Resources</span></span>
* <span data-ttu-id="f1219-2359">Uppdatera stöd för jokertecken för Get-AzResource och Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f1219-2359">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="f1219-2360">Uppdatera autentiseringsuppgifter som används vid allmänna anrop till ARM</span><span class="sxs-lookup"><span data-stu-id="f1219-2360">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="f1219-2361">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f1219-2361">Az.Sql</span></span>
* <span data-ttu-id="f1219-2362">Cmdlet-parametern (ExcludeDetectionType) för Hotidentifiering ändrades från DetectionType till sträng[] för att framtidssäkra den när nya DetectionTypes läggs till, och även för att stödja automatisk ifyllning.</span><span class="sxs-lookup"><span data-stu-id="f1219-2362">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f1219-2363">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f1219-2363">Az.Storage</span></span>
* <span data-ttu-id="f1219-2364">Stöd för att hämta/ange/ta bort hanteringsprincip på ett lagringskonto</span><span class="sxs-lookup"><span data-stu-id="f1219-2364">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="f1219-2365">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="f1219-2365">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="f1219-2366">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="f1219-2366">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="f1219-2367">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="f1219-2367">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="f1219-2368">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="f1219-2368">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="f1219-2369">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="f1219-2369">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="f1219-2370">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="f1219-2370">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f1219-2371">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f1219-2371">Az.Websites</span></span>
* <span data-ttu-id="f1219-2372">Åtgärda fel med ARM-mall som avbryter kloning av alla platser med 'New-AzWebApp -IncludeSourceWebAppSlots'</span><span class="sxs-lookup"><span data-stu-id="f1219-2372">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="f1219-2373">1.5.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="f1219-2373">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f1219-2374">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f1219-2374">Az.Accounts</span></span>
* <span data-ttu-id="f1219-2375">Lägg till kommandot Register-AzModule för stöd för AutoRest-genererade cmdletar</span><span class="sxs-lookup"><span data-stu-id="f1219-2375">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="f1219-2376">Uppdatera exempel för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="f1219-2376">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f1219-2377">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f1219-2377">Az.Automation</span></span>
* <span data-ttu-id="f1219-2378">Problem med att hämta vissa månadsscheman i flera Azure Automation-cmdletar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="f1219-2378">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="f1219-2379">Åtgärda problem med att Get-AzAutomationDscNode bara returnerar de 20 översta noderna.</span><span class="sxs-lookup"><span data-stu-id="f1219-2379">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="f1219-2380">Nu returneras alla noder</span><span class="sxs-lookup"><span data-stu-id="f1219-2380">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="f1219-2381">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f1219-2381">Az.Cdn</span></span>
* <span data-ttu-id="f1219-2382">Nya Powershell-cmdletar för att aktivera/inaktivera anpassade domän-HTTPS har lagts till och de gamla har gjorts inaktuella</span><span class="sxs-lookup"><span data-stu-id="f1219-2382">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f1219-2383">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f1219-2383">Az.Compute</span></span>
* <span data-ttu-id="f1219-2384">Lägg till stöd för jokertecken för Get-cmdletar</span><span class="sxs-lookup"><span data-stu-id="f1219-2384">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f1219-2385">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f1219-2385">Az.DataFactory</span></span>
* <span data-ttu-id="f1219-2386">ADF .Net SDK-versionen har uppdaterats till 3.0.1</span><span class="sxs-lookup"><span data-stu-id="f1219-2386">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="f1219-2387">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="f1219-2387">Az.LogicApp</span></span>
* <span data-ttu-id="f1219-2388">Åtgärda problemet med att ListWorkflows endast hämtar den första sidan med resultat</span><span class="sxs-lookup"><span data-stu-id="f1219-2388">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f1219-2389">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f1219-2389">Az.Network</span></span>
* <span data-ttu-id="f1219-2390">Lägg till stöd för jokertecken för Network-cmdletar</span><span class="sxs-lookup"><span data-stu-id="f1219-2390">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f1219-2391">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f1219-2391">Az.RecoveryServices</span></span>
* <span data-ttu-id="f1219-2392">Stöd har lagts till för SQL Server i virtuella Azure-datorer</span><span class="sxs-lookup"><span data-stu-id="f1219-2392">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="f1219-2393">SDK-uppdatering</span><span class="sxs-lookup"><span data-stu-id="f1219-2393">SDK Update</span></span>
* <span data-ttu-id="f1219-2394">Get-ProtectableItem-incheckning i VMappContainer har tagits bort</span><span class="sxs-lookup"><span data-stu-id="f1219-2394">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="f1219-2395">Name och ServerName har lagts till som parametrar för Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="f1219-2395">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="f1219-2396">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f1219-2396">Az.Resources</span></span>
* <span data-ttu-id="f1219-2397">Lägg till parametern `-TemplateObject` i cmdletar för distribution</span><span class="sxs-lookup"><span data-stu-id="f1219-2397">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="f1219-2398">Mer information här: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="f1219-2398">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="f1219-2399">Åtgärda problem med piping av resultatet i `Get-AzResource` till `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="f1219-2399">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="f1219-2400">Mer information här: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="f1219-2400">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="f1219-2401">Åtgärda problem med ändring av JSON-datatyp när `Set-AzResource` körs</span><span class="sxs-lookup"><span data-stu-id="f1219-2401">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="f1219-2402">Mer information här: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="f1219-2402">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="f1219-2403">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f1219-2403">Az.Sql</span></span>
* <span data-ttu-id="f1219-2404">AuditingEndpointsCommunicator uppdateras.</span><span class="sxs-lookup"><span data-stu-id="f1219-2404">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="f1219-2405">Åtgärdar beteendet hos ett gränsscenario när nya diagnostikinställningar skapas.</span><span class="sxs-lookup"><span data-stu-id="f1219-2405">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f1219-2406">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f1219-2406">Az.Storage</span></span>
* <span data-ttu-id="f1219-2407">Stöd för BlockBlobStorage när Storage-konto skapas      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f1219-2407">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="f1219-2408">1.4.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="f1219-2408">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="f1219-2409">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f1219-2409">Az.AnalysisServices</span></span>
* <span data-ttu-id="f1219-2410">Inaktuell AddAzureASAccount-cmdlet</span><span class="sxs-lookup"><span data-stu-id="f1219-2410">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f1219-2411">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f1219-2411">Az.Automation</span></span>
* <span data-ttu-id="f1219-2412">Hjälpen för Import-AzAutomationDscNodeConfiguration har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="f1219-2412">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="f1219-2413">Konfigurationsnamnsvalidering har lagts till i cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="f1219-2413">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="f1219-2414">Förbättrad felhantering för cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="f1219-2414">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f1219-2415">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f1219-2415">Az.CognitiveServices</span></span>
* <span data-ttu-id="f1219-2416">CustomSubdomainName har lagts till som en ny valfri parameter för New-AzCognitiveServicesAccount, som används för att ange underdomän för resursen.</span><span class="sxs-lookup"><span data-stu-id="f1219-2416">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f1219-2417">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f1219-2417">Az.Compute</span></span>
* <span data-ttu-id="f1219-2418">Problemet med ID-parameteruppsättningar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="f1219-2418">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="f1219-2419">Get-AzVMExtension har uppdaterats så att alla installerade tillägg visas om parametern Name inte har angetts</span><span class="sxs-lookup"><span data-stu-id="f1219-2419">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="f1219-2420">Parametrarna Tag och ResourceId har lagts till i cmdleten Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="f1219-2420">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="f1219-2421">Get-AzVmssVM utan instans-ID och med InstanceView kan visa virtuella VMSS-datorer med instansvyn.</span><span class="sxs-lookup"><span data-stu-id="f1219-2421">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f1219-2422">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f1219-2422">Az.DataLakeStore</span></span>
* <span data-ttu-id="f1219-2423">Cmdletar har lagts till för uppräkning och återställning av borttagna objekt i ADL</span><span class="sxs-lookup"><span data-stu-id="f1219-2423">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f1219-2424">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f1219-2424">Az.EventHub</span></span>
* <span data-ttu-id="f1219-2425">Ny boolesk egenskap SkipEmptyArchives har lagts till i Skip Empty Archives i CaptureDescription-klassen i Eventhub</span><span class="sxs-lookup"><span data-stu-id="f1219-2425">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f1219-2426">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f1219-2426">Az.KeyVault</span></span>
* <span data-ttu-id="f1219-2427">Taggning i Set-AzKeyVaultSecret har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="f1219-2427">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="f1219-2428">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="f1219-2428">Az.LogicApp</span></span>
* <span data-ttu-id="f1219-2429">Grundläggande SKU har lagts till för Integrationskonton</span><span class="sxs-lookup"><span data-stu-id="f1219-2429">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="f1219-2430">XSLT 2.0, XSLT 3.0 och Flytande mappningstyper har lagts till</span><span class="sxs-lookup"><span data-stu-id="f1219-2430">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="f1219-2431">Nya cmdletar för integrationskontosammansättningar</span><span class="sxs-lookup"><span data-stu-id="f1219-2431">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="f1219-2432">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="f1219-2432">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="f1219-2433">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="f1219-2433">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="f1219-2434">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="f1219-2434">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="f1219-2435">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="f1219-2435">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="f1219-2436">Nya cmdletar för batchkonfiguration för integrationskonto</span><span class="sxs-lookup"><span data-stu-id="f1219-2436">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="f1219-2437">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="f1219-2437">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="f1219-2438">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="f1219-2438">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="f1219-2439">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="f1219-2439">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="f1219-2440">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="f1219-2440">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="f1219-2441">Logic App-SDK har uppdaterats till version 4.1.0</span><span class="sxs-lookup"><span data-stu-id="f1219-2441">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f1219-2442">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f1219-2442">Az.Monitor</span></span>
* <span data-ttu-id="f1219-2443">Hjälpen för Get-AzMetric har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="f1219-2443">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f1219-2444">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f1219-2444">Az.Network</span></span>
* <span data-ttu-id="f1219-2445">Hjälpexempel för Add-AzApplicationGatewayCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="f1219-2445">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f1219-2446">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f1219-2446">Az.OperationalInsights</span></span>
* <span data-ttu-id="f1219-2447">Ytterligare stöd för datakällorna New och Get ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="f1219-2447">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="f1219-2448">Ny ApplicationInsights-typ har lagts till för att ge stöd för ”Get specific” och ”Get all” för ApplicationInsights-datakällor för angiven arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="f1219-2448">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="f1219-2449">Cmdleten New-AzOperationalInsightsApplicationInsightsDataSource har lagts till för att skapa datakälla med angivna parametrar för Application Insights-resurs: subscription Id, resourceGroupName och name.</span><span class="sxs-lookup"><span data-stu-id="f1219-2449">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f1219-2450">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f1219-2450">Az.Resources</span></span>
* <span data-ttu-id="f1219-2451">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="f1219-2451">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="f1219-2452">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="f1219-2452">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="f1219-2453">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="f1219-2453">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="f1219-2454">Fel som gör att KeyCredentials inte kan skapas upprepade gånger har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="f1219-2454">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="f1219-2455">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f1219-2455">Az.Sql</span></span>
* <span data-ttu-id="f1219-2456">Lägg till stöd för hyperskalanivån för SQL DB</span><span class="sxs-lookup"><span data-stu-id="f1219-2456">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="f1219-2457">Ett fel har åtgärdats där återställningen kunde misslyckas på grund av onödiga inställningsegenskaper i restore-förfrågan</span><span class="sxs-lookup"><span data-stu-id="f1219-2457">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f1219-2458">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f1219-2458">Az.Websites</span></span>
* <span data-ttu-id="f1219-2459">Rätt exempel i Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="f1219-2459">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="f1219-2460">1.3.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="f1219-2460">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f1219-2461">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f1219-2461">Az.Accounts</span></span>
* <span data-ttu-id="f1219-2462">Uppdatera till den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="f1219-2462">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="f1219-2463">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f1219-2463">Az.AnalysisServices</span></span>
<span data-ttu-id="f1219-2464">Allmän tillgänglighet för Az.AnalysisServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="f1219-2464">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f1219-2465">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f1219-2465">Az.Compute</span></span>
* <span data-ttu-id="f1219-2466">AEM-tillägg: Lägg till stöd för UltraSSD-, P60-, P70- och P80-diskar</span><span class="sxs-lookup"><span data-stu-id="f1219-2466">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="f1219-2467">Uppdatera hjälpbeskrivning för Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="f1219-2467">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="f1219-2468">Uppdatera hjälpbeskrivning och exempel för Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="f1219-2468">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f1219-2469">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f1219-2469">Az.RecoveryServices</span></span>
<span data-ttu-id="f1219-2470">Allmän tillgänglighet för Az.RecoveryServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="f1219-2470">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f1219-2471">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f1219-2471">Az.Resources</span></span>
* <span data-ttu-id="f1219-2472">Korrigera taggar för resursgrupper</span><span class="sxs-lookup"><span data-stu-id="f1219-2472">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="f1219-2473">Mer information här: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="f1219-2473">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="f1219-2474">Åtgärda problem där `Get-AzureRmRoleAssignment` inte respekterar -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="f1219-2474">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="f1219-2475">Mer information här: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="f1219-2475">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="f1219-2476">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f1219-2476">Az.Sql</span></span>
* <span data-ttu-id="f1219-2477">Lägga till Get/Set-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="f1219-2477">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="f1219-2478">Åtgärda problem där ett nullref-undantag uppstår när du kör SQL-cmdletar och inte är inloggad på ett Azure-konto</span><span class="sxs-lookup"><span data-stu-id="f1219-2478">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="f1219-2479">Åtgärda nullref-undantag i Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="f1219-2479">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="f1219-2480">1.2.1 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="f1219-2480">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f1219-2481">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f1219-2481">Az.Accounts</span></span>
* <span data-ttu-id="f1219-2482">Version med rätt version av autentisering</span><span class="sxs-lookup"><span data-stu-id="f1219-2482">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="f1219-2483">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f1219-2483">Az.AnalysisServices</span></span>
* <span data-ttu-id="f1219-2484">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="f1219-2484">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f1219-2485">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f1219-2485">Az.RecoveryServices</span></span>
* <span data-ttu-id="f1219-2486">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="f1219-2486">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="f1219-2487">1.2.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="f1219-2487">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f1219-2488">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f1219-2488">Az.Accounts</span></span>
* <span data-ttu-id="f1219-2489">Lägga till interaktiv autentisering och autentisering med användarnamn/lösenord för endast Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="f1219-2489">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="f1219-2490">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="f1219-2490">Update incorrect online help URLs</span></span>
* <span data-ttu-id="f1219-2491">Lägga till varningsmeddelande i PS Core för Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="f1219-2491">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="f1219-2492">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="f1219-2492">Az.Aks</span></span>
* <span data-ttu-id="f1219-2493">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="f1219-2493">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f1219-2494">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f1219-2494">Az.Automation</span></span>
* <span data-ttu-id="f1219-2495">Stöd för Python 2-runbookflöden har lagts till</span><span class="sxs-lookup"><span data-stu-id="f1219-2495">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="f1219-2496">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="f1219-2496">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="f1219-2497">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f1219-2497">Az.Cdn</span></span>
* <span data-ttu-id="f1219-2498">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="f1219-2498">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f1219-2499">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f1219-2499">Az.Compute</span></span>
* <span data-ttu-id="f1219-2500">Lägga till cmdleten Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="f1219-2500">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="f1219-2501">Lägga till TempDisk-parameter i Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f1219-2501">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="f1219-2502">Korrigera varningsmeddelande för New-AzVM</span><span class="sxs-lookup"><span data-stu-id="f1219-2502">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="f1219-2503">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f1219-2503">Az.ContainerRegistry</span></span>
* <span data-ttu-id="f1219-2504">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="f1219-2504">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f1219-2505">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f1219-2505">Az.DataFactory</span></span>
* <span data-ttu-id="f1219-2506">ADF .Net SDK-versionen har uppdaterats till 3.0.0</span><span class="sxs-lookup"><span data-stu-id="f1219-2506">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f1219-2507">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f1219-2507">Az.DataLakeStore</span></span>
* <span data-ttu-id="f1219-2508">Åtgärda problem med ADLS-slutpunkt vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="f1219-2508">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="f1219-2509">Mer information här: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="f1219-2509">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="f1219-2510">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="f1219-2510">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f1219-2511">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f1219-2511">Az.IotHub</span></span>
* <span data-ttu-id="f1219-2512">Lägga till kodningsformat i cmdleten Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="f1219-2512">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f1219-2513">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f1219-2513">Az.KeyVault</span></span>
* <span data-ttu-id="f1219-2514">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="f1219-2514">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f1219-2515">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f1219-2515">Az.Network</span></span>
* <span data-ttu-id="f1219-2516">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="f1219-2516">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="f1219-2517">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f1219-2517">Az.Resources</span></span>
* <span data-ttu-id="f1219-2518">Åtgärda felaktiga exempel i referensdokumentationen ”New-AzADAppCredential” och ”New-AzADSpCredential”</span><span class="sxs-lookup"><span data-stu-id="f1219-2518">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="f1219-2519">Åtgärda problem där sökvägen för parametern ”-TemplateFile” inte omvandlas innan cmdletarna för distribution i resursgruppen körs</span><span class="sxs-lookup"><span data-stu-id="f1219-2519">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="f1219-2520">Az.Resources: Korrigera dokumentationen om standardvärdet för New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="f1219-2520">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="f1219-2521">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="f1219-2521">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="f1219-2522">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="f1219-2522">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="f1219-2523">Åtgärda formateringsproblemet med objektet ”PSResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="f1219-2523">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="f1219-2524">Mer information här: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="f1219-2524">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f1219-2525">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f1219-2525">Az.ServiceFabric</span></span>
* <span data-ttu-id="f1219-2526">Återställ när ett certifikat läggs till i en Virtual Machine Scale Sets-modell men ett undantag genereras. Detta har gjorts för att åtgärda följande fel: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="f1219-2526">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="f1219-2527">Korrigera några felmeddelanden.</span><span class="sxs-lookup"><span data-stu-id="f1219-2527">Fix some error messages.</span></span>
* <span data-ttu-id="f1219-2528">Korrigering av skapande av kluster med ARM-mall som är standard för New-AzServiceFabriCluster som inte fungerade med migrering till Az.</span><span class="sxs-lookup"><span data-stu-id="f1219-2528">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="f1219-2529">Korrigering av tilläggning av kluster/programcertifikat så att endast VM Scale Sets som motsvarar klustret läggs till genom att kontrollera ID för klustret i tillägget.</span><span class="sxs-lookup"><span data-stu-id="f1219-2529">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="f1219-2530">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="f1219-2530">Az.SignalR</span></span>
* <span data-ttu-id="f1219-2531">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="f1219-2531">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="f1219-2532">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f1219-2532">Az.Sql</span></span>
* <span data-ttu-id="f1219-2533">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="f1219-2533">Update incorrect online help URLs</span></span>
* <span data-ttu-id="f1219-2534">Uppdaterad parameterbeskrivning för LicenseType-parameter med möjliga värden</span><span class="sxs-lookup"><span data-stu-id="f1219-2534">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="f1219-2535">Korrigering för att uppdatera hanterad instansidentitet som inte fungerar när det är den enda uppdaterade egenskapen</span><span class="sxs-lookup"><span data-stu-id="f1219-2535">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="f1219-2536">Stöd för anpassad sortering på hanterad instans</span><span class="sxs-lookup"><span data-stu-id="f1219-2536">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f1219-2537">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f1219-2537">Az.Storage</span></span>
* <span data-ttu-id="f1219-2538">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="f1219-2538">Update incorrect online help URLs</span></span>
* <span data-ttu-id="f1219-2539">Tillhandahåll detaljerat felmeddelande när en användare försöker hämta/konfigurera klassisk loggning/mått på ett Premium Storage-konto eftersom Premium Storage-kontot inte har stöd för klassisk loggning/mått.</span><span class="sxs-lookup"><span data-stu-id="f1219-2539">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="f1219-2540">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="f1219-2540">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="f1219-2541">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="f1219-2541">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="f1219-2542">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="f1219-2542">Az.TrafficManager</span></span>
* <span data-ttu-id="f1219-2543">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="f1219-2543">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f1219-2544">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f1219-2544">Az.Websites</span></span>
* <span data-ttu-id="f1219-2545">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="f1219-2545">Update incorrect online help URLs</span></span>
* <span data-ttu-id="f1219-2546">Korrigerar ”New-AzWebAppSSLBinding” så att certifikatet laddas upp till rätt resursgrupp och plats om appen finns i en ASE.</span><span class="sxs-lookup"><span data-stu-id="f1219-2546">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="f1219-2547">Korrigerar ”New-AzWebAppSSLBinding” så att taggarna inte skrivs över på en bindning av ett SSL-certifikat till en app</span><span class="sxs-lookup"><span data-stu-id="f1219-2547">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="f1219-2548">1.1.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="f1219-2548">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f1219-2549">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f1219-2549">Az.Accounts</span></span>
* <span data-ttu-id="f1219-2550">Lade till omfattningen ”Lokal” till Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="f1219-2550">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f1219-2551">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f1219-2551">Az.Compute</span></span>
* <span data-ttu-id="f1219-2552">Namn är nu valfritt i ID-parametern för Restart/Start/Stop/Remove/Set-AzVM och Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="f1219-2552">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="f1219-2553">Uppdaterade beskrivningen av ID i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="f1219-2553">Updated the description of ID in help files</span></span>
* <span data-ttu-id="f1219-2554">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f1219-2554">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f1219-2555">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f1219-2555">Az.DataLakeStore</span></span>
* <span data-ttu-id="f1219-2556">Uppdatera sdk-versionen av dataplanet till 1.1.14 för SDK-korrigeringar.</span><span class="sxs-lookup"><span data-stu-id="f1219-2556">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="f1219-2557">Korrigerade hanteringen av negativ accesstime och modificationtime för getfilestatus och liststatus; korrigera asynkront annulleringstoken</span><span class="sxs-lookup"><span data-stu-id="f1219-2557">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="f1219-2558">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="f1219-2558">Az.EventGrid</span></span>
* <span data-ttu-id="f1219-2559">Uppdaterat för användning av API-versionen 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="f1219-2559">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="f1219-2560">Uppdaterade följande cmdletar för att stödja nytt scenario i API-versionen 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="f1219-2560">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="f1219-2561">New-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="f1219-2561">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="f1219-2562">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="f1219-2562">Event Time-To-Live,</span></span>
        - <span data-ttu-id="f1219-2563">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="f1219-2563">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="f1219-2564">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="f1219-2564">Dead letter endpoint.</span></span>
    - <span data-ttu-id="f1219-2565">Update-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="f1219-2565">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="f1219-2566">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="f1219-2566">Event Time-To-Live,</span></span>
        - <span data-ttu-id="f1219-2567">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="f1219-2567">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="f1219-2568">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="f1219-2568">Dead letter endpoint.</span></span>
* <span data-ttu-id="f1219-2569">Lade till nya enum-värden (storageQueue och hybridConnection) för alternativet EndpointType i cmdletarna New-AzureRmEventGridSubscription och Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="f1219-2569">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="f1219-2570">Visa varningsmeddelanden om skapande eller uppdatering av händelseprenumerationen förväntas medföra manuell åtgärd från användaren.</span><span class="sxs-lookup"><span data-stu-id="f1219-2570">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f1219-2571">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f1219-2571">Az.IotHub</span></span>
* <span data-ttu-id="f1219-2572">Har uppdaterats till den senaste versionen av SDK:n lotHub</span><span class="sxs-lookup"><span data-stu-id="f1219-2572">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="f1219-2573">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="f1219-2573">Az.LogicApp</span></span>
* <span data-ttu-id="f1219-2574">Get-AzLogicApp visar en lista över alla som inte har angivet namn</span><span class="sxs-lookup"><span data-stu-id="f1219-2574">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="f1219-2575">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f1219-2575">Az.Resources</span></span>
* <span data-ttu-id="f1219-2576">Åtgärdade problem med parameteruppsättningen när parametrarna -ODataQuery och -ResourceId anges för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="f1219-2576">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="f1219-2577">Mer information här: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="f1219-2577">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="f1219-2578">Åtgärdade hantering av parametern -Custom i New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f1219-2578">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="f1219-2579">Korrigerade stavfel i New-AzDeployment-dokumentationen</span><span class="sxs-lookup"><span data-stu-id="f1219-2579">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="f1219-2580">Gjorde parametern -MailNickname obligatorisk för New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="f1219-2580">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="f1219-2581">Mer information här: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="f1219-2581">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="f1219-2582">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="f1219-2582">Az.SignalR</span></span>
* <span data-ttu-id="f1219-2583">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f1219-2583">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="f1219-2584">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f1219-2584">Az.Sql</span></span>
* <span data-ttu-id="f1219-2585">Konverterade lagringshanteringsklientens beroende av den normala SDK-implementeringen.</span><span class="sxs-lookup"><span data-stu-id="f1219-2585">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f1219-2586">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f1219-2586">Az.Storage</span></span>
* <span data-ttu-id="f1219-2587">Angav StorageAccountName för lagringskontext som det verkliga namnet på lagringskontot när det skapas med Sas Token, OAuth eller Anonymous</span><span class="sxs-lookup"><span data-stu-id="f1219-2587">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="f1219-2588">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="f1219-2588">New-AzStorageContext</span></span>
* <span data-ttu-id="f1219-2589">Skapade Sas Token för Blob Snapshot-objekt med parametern -FullUri, åtgärdade den returnerade URI:n så att den blir URI för ögonblicksbild</span><span class="sxs-lookup"><span data-stu-id="f1219-2589">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="f1219-2590">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="f1219-2590">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f1219-2591">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f1219-2591">Az.Websites</span></span>
* <span data-ttu-id="f1219-2592">Åtgärdade en bugg i datumparsningen i Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="f1219-2592">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="f1219-2593">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f1219-2593">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="f1219-2594">1.0.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="f1219-2594">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="f1219-2595">Allmänt</span><span class="sxs-lookup"><span data-stu-id="f1219-2595">General</span></span>

- <span data-ttu-id="f1219-2596">Allmän tillgänglighet för Az-modulen</span><span class="sxs-lookup"><span data-stu-id="f1219-2596">General Availability of Az Module</span></span>
- <span data-ttu-id="f1219-2597">Onlinehjälp för varje modul</span><span class="sxs-lookup"><span data-stu-id="f1219-2597">Online help for each module</span></span>
- <span data-ttu-id="f1219-2598">Mer information och en översikt finns på [Az-informationssidan](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="f1219-2598">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="f1219-2599">Information om hur du migrerar från AzureRM finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f1219-2599">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="f1219-2600">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f1219-2600">Az.Accounts</span></span>
- <span data-ttu-id="f1219-2601">Har ändrats från Az.Profile</span><span class="sxs-lookup"><span data-stu-id="f1219-2601">Changed from Az.Profile</span></span>
- <span data-ttu-id="f1219-2602">Fasta tabellformat för profil- och kontexttyper</span><span class="sxs-lookup"><span data-stu-id="f1219-2602">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="f1219-2603">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f1219-2603">Az.ApiManagement</span></span>
- <span data-ttu-id="f1219-2604">Korrigeringar för #7002</span><span class="sxs-lookup"><span data-stu-id="f1219-2604">Fixes for #7002</span></span>
- <span data-ttu-id="f1219-2605">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f1219-2605">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="f1219-2606">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="f1219-2606">Az.Batch</span></span>
- <span data-ttu-id="f1219-2607">Lade till möjligheten att se vilken version av Azure Batch Node Agent som körs på var och en av de virtuella datorerna i en pool, via den nya egenskapen `NodeAgentInformation` på `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="f1219-2607">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="f1219-2608">Standarden `Caching` för `PSDataDisk` är nu `ReadWrite` i stället för `None`.</span><span class="sxs-lookup"><span data-stu-id="f1219-2608">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="f1219-2609">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f1219-2609">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="f1219-2610">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="f1219-2610">Az.Billing</span></span>
- <span data-ttu-id="f1219-2611">Kombinerar cmdletarna för fakturering, förbrukning och UsageAggregates. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f1219-2611">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="f1219-2612">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="f1219-2612">Az.CognitivServices</span></span>
- <span data-ttu-id="f1219-2613">Lade till kompletterare för SkuName och Typem som är tillgängliga i New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="f1219-2613">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="f1219-2614">Tog bort parameteruppsättningen GetSkusWithAccountParamSetName från Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="f1219-2614">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="f1219-2615">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="f1219-2615">Az.ContainerInstance</span></span>
- <span data-ttu-id="f1219-2616">Stöd för ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="f1219-2616">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="f1219-2617">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="f1219-2617">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="f1219-2618">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f1219-2618">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="f1219-2619">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f1219-2619">Az.DataLakeStore</span></span>
- <span data-ttu-id="f1219-2620">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f1219-2620">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="f1219-2621">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f1219-2621">Az.Monitor</span></span>
- <span data-ttu-id="f1219-2622">Döpte om Az.Insights till Az.Monitor och andra mindre icke-bakåtkompatibla ändringar. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f1219-2622">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="f1219-2623">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f1219-2623">Az.KeyVault</span></span>
- <span data-ttu-id="f1219-2624">Tog bort den inaktuella egenskapen PurgeDisabled från utdatatyper</span><span class="sxs-lookup"><span data-stu-id="f1219-2624">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="f1219-2625">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="f1219-2625">Az.MachineLearning</span></span>
- <span data-ttu-id="f1219-2626">Inkluderade cmdletarna från modulen Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="f1219-2626">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="f1219-2627">Az.Media</span><span class="sxs-lookup"><span data-stu-id="f1219-2627">Az.Media</span></span>
- <span data-ttu-id="f1219-2628">Tog bort inaktuella -Tags-alias från New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="f1219-2628">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="f1219-2629">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f1219-2629">Az.Network</span></span>
<span data-ttu-id="f1219-2630">Stöd har lagts till för konfiguration av RewriteRuleSets i Application Gateway</span><span class="sxs-lookup"><span data-stu-id="f1219-2630">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="f1219-2631">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="f1219-2631">New cmdlets added:</span></span>
        - <span data-ttu-id="f1219-2632">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f1219-2632">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="f1219-2633">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f1219-2633">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="f1219-2634">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f1219-2634">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="f1219-2635">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f1219-2635">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="f1219-2636">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f1219-2636">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="f1219-2637">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="f1219-2637">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="f1219-2638">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="f1219-2638">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="f1219-2639">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="f1219-2639">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="f1219-2640">Cmdletar har uppdaterats med den valfria parametern -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f1219-2640">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="f1219-2641">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f1219-2641">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="f1219-2642">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f1219-2642">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="f1219-2643">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f1219-2643">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="f1219-2644">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f1219-2644">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="f1219-2645">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="f1219-2645">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="f1219-2646">New-AzureRmApplicationGatewayUrlPathMapConfig har lagt till KeyVault-stöd för Application Gateway med Identity.</span><span class="sxs-lookup"><span data-stu-id="f1219-2646">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="f1219-2647">Cmdletar har uppdaterats med den valfria parametern -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="f1219-2647">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="f1219-2648">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f1219-2648">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="f1219-2649">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f1219-2649">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="f1219-2650">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f1219-2650">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="f1219-2651">Cmdleten New-AzApplicationGateway har uppdaterats med den valfria parametern -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="f1219-2651">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="f1219-2652">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f1219-2652">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="f1219-2653">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f1219-2653">Az.OperationalInsights</span></span>
- <span data-ttu-id="f1219-2654">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f1219-2654">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="f1219-2655">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="f1219-2655">Az.Profile</span></span>
- <span data-ttu-id="f1219-2656">Modulnamnet har ändrats till Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f1219-2656">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="f1219-2657">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f1219-2657">Az.RecoveryServices</span></span>
- <span data-ttu-id="f1219-2658">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f1219-2658">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="f1219-2659">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f1219-2659">Az.Resources</span></span>
- <span data-ttu-id="f1219-2660">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f1219-2660">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="f1219-2661">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f1219-2661">Az.ServiceFabric</span></span>
- <span data-ttu-id="f1219-2662">Stöd för specificering av certifikat efter eget namn och tumavtryck</span><span class="sxs-lookup"><span data-stu-id="f1219-2662">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="f1219-2663">Information om fler icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f1219-2663">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="f1219-2664">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="f1219-2664">Az.SIgnalR</span></span>
- <span data-ttu-id="f1219-2665">Allmän tillgänglighet för PowerShell-cmdletar för SIgnalR</span><span class="sxs-lookup"><span data-stu-id="f1219-2665">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="f1219-2666">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f1219-2666">Az.Sql</span></span>
- <span data-ttu-id="f1219-2667">Lade till de nya identifieringstyperna Data_Exfiltration och Unsafe_Action i Threat Detection-cmdletar</span><span class="sxs-lookup"><span data-stu-id="f1219-2667">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="f1219-2668">Uppdaterade dokumentationsexempel för Sql Auditing-cmdletar</span><span class="sxs-lookup"><span data-stu-id="f1219-2668">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="f1219-2669">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f1219-2669">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="f1219-2670">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f1219-2670">Az.Storage</span></span>
- <span data-ttu-id="f1219-2671">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f1219-2671">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="f1219-2672">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f1219-2672">Az.Websites</span></span>
- <span data-ttu-id="f1219-2673">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f1219-2673">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="f1219-2674">0.7.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="f1219-2674">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="f1219-2675">Allmänt</span><span class="sxs-lookup"><span data-stu-id="f1219-2675">General</span></span>

* <span data-ttu-id="f1219-2676">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="f1219-2676">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="f1219-2677">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f1219-2677">Az.Compute</span></span>

* <span data-ttu-id="f1219-2678">Lade till stöd för UltraSSD och Galleriavbildningar i de enkla parameteruppsättningarna för `New-AzVm(ss)`-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="f1219-2678">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="f1219-2679">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f1219-2679">Az.DataLakeStore</span></span>

* <span data-ttu-id="f1219-2680">Åtgärdade avslutande snedstreck i domänen för adls-konto</span><span class="sxs-lookup"><span data-stu-id="f1219-2680">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="f1219-2681">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f1219-2681">Az.FrontDoor</span></span>

* <span data-ttu-id="f1219-2682">Brutna länkar korrigerades</span><span class="sxs-lookup"><span data-stu-id="f1219-2682">Fixed some broken links</span></span>
    - <span data-ttu-id="f1219-2683">I artiklarna New-AzureRmFrontDoor och Set-AzureRmFrontDoor artiklar korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="f1219-2683">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="f1219-2684">I artikeln New-AzureRmFrontDoorManagedRuleObject korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="f1219-2684">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="f1219-2685">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f1219-2685">Az.RecoveryServices</span></span>

* <span data-ttu-id="f1219-2686">Lade till valideringar på klientsidan för Azure-filresurs med återställningsåtgärder.</span><span class="sxs-lookup"><span data-stu-id="f1219-2686">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="f1219-2687">Gjorde storageAccountName och storageAccountResourceGroupName valfritt för afs-återställning.</span><span class="sxs-lookup"><span data-stu-id="f1219-2687">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="f1219-2688">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f1219-2688">Az.Resources</span></span>

* <span data-ttu-id="f1219-2689">Korrigering för https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="f1219-2689">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="f1219-2690">Uppdaterade Get-AzureRmRoleAssignment så att prenumerationsomfattningen används om den anges vid begäran om klassiska administratörer.</span><span class="sxs-lookup"><span data-stu-id="f1219-2690">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="f1219-2691">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f1219-2691">Az.Sql</span></span>

* <span data-ttu-id="f1219-2692">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="f1219-2692">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="f1219-2693">Korrigerade ett problem med Get-AzureRmSqlDatabaseVulnerabilityAssessment med DotNet-kärna</span><span class="sxs-lookup"><span data-stu-id="f1219-2693">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="f1219-2694">Ändrade dokumentationen för hjälpmeddelanden som rör SQL Auditing-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="f1219-2694">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="f1219-2695">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f1219-2695">Az.Storage</span></span>

* <span data-ttu-id="f1219-2696">Lade till -EnableHierarchicalNamespace i New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f1219-2696">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="f1219-2697">Åtgärdade problemet med att cmdleten Copy File inte kunde återanvända källkontexten på målet om inte -DestContext angetts</span><span class="sxs-lookup"><span data-stu-id="f1219-2697">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="f1219-2698">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="f1219-2698">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="f1219-2699">Stöd för statisk webbplatskonfiguration</span><span class="sxs-lookup"><span data-stu-id="f1219-2699">Support Static Website configuration</span></span>
    - <span data-ttu-id="f1219-2700">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="f1219-2700">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="f1219-2701">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="f1219-2701">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="f1219-2702">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f1219-2702">Az.Websites</span></span>

* <span data-ttu-id="f1219-2703">Set-AzureRmWebApp och Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f1219-2703">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="f1219-2704">Ny parameter (-AzureStoragePath) har lagts till för att ange att Azure Storage-sökvägar ska monteras i containerappar i Windows och Linux.</span><span class="sxs-lookup"><span data-stu-id="f1219-2704">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="f1219-2705">Använder utdata från den nya cmdleten New-AzureRmWebAppAzureStoragePath som en parameter för att ange sökvägar för Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="f1219-2705">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="f1219-2706">0.6.1 – november 2018</span><span class="sxs-lookup"><span data-stu-id="f1219-2706">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="f1219-2707">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f1219-2707">Az.ApiManagement</span></span>
* <span data-ttu-id="f1219-2708">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="f1219-2708">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="f1219-2709">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f1219-2709">Az.Automation</span></span>
* <span data-ttu-id="f1219-2710">Swagger baserade Azure Automation-cmdletar</span><span class="sxs-lookup"><span data-stu-id="f1219-2710">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="f1219-2711">Cmdletar för Uppdateringshantering har lagts till</span><span class="sxs-lookup"><span data-stu-id="f1219-2711">Added Update Management cmdlets</span></span>
* <span data-ttu-id="f1219-2712">Cmdletar för källkontroll har lagts till</span><span class="sxs-lookup"><span data-stu-id="f1219-2712">Added Source Control cmdlets</span></span>
* <span data-ttu-id="f1219-2713">Remove-AzureRmAutomationHybridWorkerGroup-cmdlet har lagts till</span><span class="sxs-lookup"><span data-stu-id="f1219-2713">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="f1219-2714">Kommandot för DSC-registreringsnod har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="f1219-2714">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="f1219-2715">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f1219-2715">Az.Compute</span></span>
* <span data-ttu-id="f1219-2716">Problem med SystemAssigned-identitet har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="f1219-2716">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="f1219-2717">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="f1219-2717">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="f1219-2718">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="f1219-2718">Az.ContainerInstance</span></span>
* <span data-ttu-id="f1219-2719">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="f1219-2719">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="f1219-2720">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="f1219-2720">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="f1219-2721">uppdatera exempelbeskrivningen för marketplace-cmdletar</span><span class="sxs-lookup"><span data-stu-id="f1219-2721">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="f1219-2722">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f1219-2722">Az.Network</span></span>
* <span data-ttu-id="f1219-2723">Cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomErreller Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="f1219-2723">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="f1219-2724">ICMP tillbaka till stöd för Azure Firewall-nätverksprotokoll har lagts till</span><span class="sxs-lookup"><span data-stu-id="f1219-2724">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="f1219-2725">Uppdatera cmdlet Test-AzureRmNetworkWatcherConnectivity, lägga till verifiering av mål-id, adress och port.</span><span class="sxs-lookup"><span data-stu-id="f1219-2725">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="f1219-2726">Åtgärda problem med minnesanvändning i VirtualNetwork-karta</span><span class="sxs-lookup"><span data-stu-id="f1219-2726">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="f1219-2727">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="f1219-2727">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="f1219-2728">Åtgärda för att ändra principen för en skyddad fildelning.</span><span class="sxs-lookup"><span data-stu-id="f1219-2728">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="f1219-2729">Tidszonsprincipen har konverterats till versaler.</span><span class="sxs-lookup"><span data-stu-id="f1219-2729">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="f1219-2730">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="f1219-2730">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="f1219-2731">Exempel i New-AzureRmRecoveryServicesAsrProtectableItem har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="f1219-2731">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="f1219-2732">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="f1219-2732">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="f1219-2733">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="f1219-2733">Az.Relay</span></span>
* <span data-ttu-id="f1219-2734">Valfri parameter -KeyValue till New-AzureRmRelayKey cmdlet har lagts till, vilket gör det möjligt för användare att tillhandahålla KeyValue.</span><span class="sxs-lookup"><span data-stu-id="f1219-2734">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="f1219-2735">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f1219-2735">Az.Resources</span></span>
* <span data-ttu-id="f1219-2736">Uppdatera hjälpdokumentation för resursidentitet kopplad till parametrar i `New-AzureRmPolicyAssignment` och `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="f1219-2736">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="f1219-2737">Lägg till ett exempel för New-AzureRmPolicyDefinition som använder -Metadata</span><span class="sxs-lookup"><span data-stu-id="f1219-2737">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="f1219-2738">Korrigera så att skiftläge behålls i taggnycklar i NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="f1219-2738">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="f1219-2739">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f1219-2739">Az.ServiceFabric</span></span>
* <span data-ttu-id="f1219-2740">Lägg till utfasningsmeddelanden för kommande icke-kompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="f1219-2740">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="f1219-2741">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f1219-2741">Az.Sql</span></span>
* <span data-ttu-id="f1219-2742">Nya cmdletar för CRUD-åtgärder på Azure Sql Database-hanterad instans och Azure Sql-hanterad databas</span><span class="sxs-lookup"><span data-stu-id="f1219-2742">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="f1219-2743">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="f1219-2743">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="f1219-2744">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="f1219-2744">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="f1219-2745">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="f1219-2745">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="f1219-2746">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="f1219-2746">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="f1219-2747">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="f1219-2747">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="f1219-2748">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="f1219-2748">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="f1219-2749">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="f1219-2749">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="f1219-2750">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="f1219-2750">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="f1219-2751">Hantering av utökad granskningsprincip på en server eller en databas har aktiverats.</span><span class="sxs-lookup"><span data-stu-id="f1219-2751">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="f1219-2752">Ny parameter (PredicateExpression) har lagts till för att aktivera filtrering av granskningsloggar.</span><span class="sxs-lookup"><span data-stu-id="f1219-2752">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="f1219-2753">Cmdletar har ändrats så att de använder SQL-klienter i stället för äldre klienter.</span><span class="sxs-lookup"><span data-stu-id="f1219-2753">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="f1219-2754">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="f1219-2754">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="f1219-2755">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="f1219-2755">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="f1219-2756">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="f1219-2756">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="f1219-2757">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="f1219-2757">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="f1219-2758">Problem med att använda Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings med lagringskontots namnparameter har korrigerats</span><span class="sxs-lookup"><span data-stu-id="f1219-2758">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="f1219-2759">0.5.0 – november 2018</span><span class="sxs-lookup"><span data-stu-id="f1219-2759">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="f1219-2760">Allmänt</span><span class="sxs-lookup"><span data-stu-id="f1219-2760">General</span></span>
* <span data-ttu-id="f1219-2761">Lade till resurskompletterare till många kärn-cmdletar – dessa gör att du kan stega genom befintliga resursnamn med TABB vid interaktiva anrop till cmdletar</span><span class="sxs-lookup"><span data-stu-id="f1219-2761">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="f1219-2762">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="f1219-2762">Az.Profile</span></span>
* <span data-ttu-id="f1219-2763">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="f1219-2763">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="f1219-2764">Bytte namn på parametern TenantId i cmdleten Connect-AzAccount till Tenant och lade till ett alias för TenantId</span><span class="sxs-lookup"><span data-stu-id="f1219-2764">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="f1219-2765">Uppdaterade TenantId-beskrivningen för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="f1219-2765">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="f1219-2766">Åtgärda felmeddelande för misslyckad inloggning när du tillhandahåller klientdomän</span><span class="sxs-lookup"><span data-stu-id="f1219-2766">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="f1219-2767">Åtgärda problem med att kontextnamn hamnar i konflikt för konton utan prenumerationer i klientorganisationen</span><span class="sxs-lookup"><span data-stu-id="f1219-2767">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="f1219-2768">Åtgärda problem med DataLake-slutpunkter vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="f1219-2768">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="f1219-2769">Åtgärdade problem med att Disconnect-AzAccount kastades om den inte anslöts</span><span class="sxs-lookup"><span data-stu-id="f1219-2769">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="f1219-2770">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f1219-2770">Az.CognitiveServices</span></span>
* <span data-ttu-id="f1219-2771">Lade till åtgärden Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="f1219-2771">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f1219-2772">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f1219-2772">Az.Compute</span></span>
* <span data-ttu-id="f1219-2773">Lade till cmdletarna Add-AzVmssVMDataDisk och Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="f1219-2773">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="f1219-2774">Get-AzVMImage visar AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="f1219-2774">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="f1219-2775">Åtgärdade att värdena för alternativen SetAzVMChefExtension -BootstrapOptions och -JsonAttribute inte angavs i json-format.</span><span class="sxs-lookup"><span data-stu-id="f1219-2775">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f1219-2776">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f1219-2776">Az.DataLakeStore</span></span>
* <span data-ttu-id="f1219-2777">Uppdatera DataLake-paketet till 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="f1219-2777">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="f1219-2778">Lägg till standardsamtidighet för flertrådade åtgärder.</span><span class="sxs-lookup"><span data-stu-id="f1219-2778">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="f1219-2779">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="f1219-2779">Az.Insights</span></span>
* <span data-ttu-id="f1219-2780">Åtgärdade problem #7267 (autoskalningsområde)</span><span class="sxs-lookup"><span data-stu-id="f1219-2780">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="f1219-2781">Problem med att uppräknade parametrar inte ställdes in ordentligt när du skapade en ny autoskalningsregel (de ställdes alltid in med standardvärdet).</span><span class="sxs-lookup"><span data-stu-id="f1219-2781">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="f1219-2782">Åtgärdade problem #7513 [Insights] Set-AzDiagnosticSetting kräver uttrycklig specifikation av kategorier när inställningar skapas</span><span class="sxs-lookup"><span data-stu-id="f1219-2782">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="f1219-2783">Nu kräver inte cmdleten uttrycklig anvisning av kategorierna för att aktiveras under skapande, d.v.s. den fungerar enligt beskrivning</span><span class="sxs-lookup"><span data-stu-id="f1219-2783">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f1219-2784">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f1219-2784">Az.Network</span></span>
* <span data-ttu-id="f1219-2785">PeeringType ändrades till en obligatorisk parameter för följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="f1219-2785">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="f1219-2786">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="f1219-2786">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="f1219-2787">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="f1219-2787">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="f1219-2788">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="f1219-2788">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="f1219-2789">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="f1219-2789">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="f1219-2790">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="f1219-2790">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="f1219-2791">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="f1219-2791">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f1219-2792">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f1219-2792">Az.PolicyInsights</span></span>
* <span data-ttu-id="f1219-2793">Cmdletar för principreparation har lagts till</span><span class="sxs-lookup"><span data-stu-id="f1219-2793">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="f1219-2794">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f1219-2794">Az.Resources</span></span>
* <span data-ttu-id="f1219-2795">Korrigering för https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="f1219-2795">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="f1219-2796">Tillåt att resurser listas med parametern -ResourceId för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="f1219-2796">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="f1219-2797">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f1219-2797">Az.ServiceBus</span></span>
* <span data-ttu-id="f1219-2798">Skrivskyddad MigrationState-egenskap har lagts till i PSServiceBusMigrationConfigurationAttributes, som hjälper till att hålla koll på migreringstillståndet.</span><span class="sxs-lookup"><span data-stu-id="f1219-2798">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f1219-2799">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f1219-2799">Az.ServiceFabric</span></span>
* <span data-ttu-id="f1219-2800">Åtgärda att lägga till certifikat till Linux-Vmss.</span><span class="sxs-lookup"><span data-stu-id="f1219-2800">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="f1219-2801">Åtgärdade Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="f1219-2801">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="f1219-2802">Använd rätt tumavtryck från nya certifikat (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="f1219-2802">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="f1219-2803">Visa undantag korrekt (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="f1219-2803">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="f1219-2804">Åtgärdade Update-AzServiceFabricDurability så att klusterkonfigurationen uppdateras innan Vmss-åtgärden CreateOrUpdate påbörjas.</span><span class="sxs-lookup"><span data-stu-id="f1219-2804">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="f1219-2805">0.4.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="f1219-2805">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="f1219-2806">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="f1219-2806">Az.Profile</span></span>
* <span data-ttu-id="f1219-2807">Åtgärdade problemet med Get-AzSubscription i CloudShell</span><span class="sxs-lookup"><span data-stu-id="f1219-2807">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="f1219-2808">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="f1219-2808">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f1219-2809">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f1219-2809">Az.Compute</span></span>
* <span data-ttu-id="f1219-2810">Nya storlekar lades till i listan över godkända VM-storlekar för vilka accelererat nätverk kommer att aktiveras vid användning av den enkla parameteruppsättningen för New-AzVm</span><span class="sxs-lookup"><span data-stu-id="f1219-2810">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="f1219-2811">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="f1219-2811">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f1219-2812">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f1219-2812">Az.DataLakeStore</span></span>
* <span data-ttu-id="f1219-2813">Lägger till stöd för regler för virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="f1219-2813">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="f1219-2814">Get-AzDataLakeStoreVirtualNetworkRule: Hämtar eller listar regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f1219-2814">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="f1219-2815">Add-AzDataLakeStoreVirtualNetworkRule: Lägger till en regel för virtuellt nätverk i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="f1219-2815">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="f1219-2816">Set-AzDataLakeStoreVirtualNetworkRule: Ändrar den angivna regeln för virtuellt nätverk i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="f1219-2816">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="f1219-2817">Remove-AzDataLakeStoreVirtualNetworkRule: Tar bort en regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f1219-2817">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f1219-2818">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f1219-2818">Az.Network</span></span>
* <span data-ttu-id="f1219-2819">Skicka protokollvärdet till serverdelen för att uppdatera cmdleten Test-AzNetworkWatcherConnectivity.</span><span class="sxs-lookup"><span data-stu-id="f1219-2819">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="f1219-2820">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="f1219-2820">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f1219-2821">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f1219-2821">Az.Resources</span></span>
* <span data-ttu-id="f1219-2822">Åtgärdade problem där Get-AzRoleDefinition genererar ett oläsligt undantag (när standardprofilen inte innehåller någon prenumeration och ingen omfattning har angetts) genom att lägga till ett beskrivande undantag i scenariot.</span><span class="sxs-lookup"><span data-stu-id="f1219-2822">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="f1219-2823">Ställ in ”RoleDefinitionNameParameterSet” som standardparameteruppsättning.</span><span class="sxs-lookup"><span data-stu-id="f1219-2823">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="f1219-2824">0.3.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="f1219-2824">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="f1219-2825">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="f1219-2825">Azure.Storage</span></span>
* <span data-ttu-id="f1219-2826">Åtgärda fel där Kopiera blob/fil inte kopierar metadata när målplatsen har ett problem med metadata</span><span class="sxs-lookup"><span data-stu-id="f1219-2826">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="f1219-2827">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="f1219-2827">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="f1219-2828">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="f1219-2828">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="f1219-2829">Stöd för att hämta användningsinformation om en Storage-resurs för en specifik plats och för att lägga till ett varningsmeddelande för att hämta användningsinformation om en global Storage-resurs är inaktuellt.</span><span class="sxs-lookup"><span data-stu-id="f1219-2829">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="f1219-2830">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="f1219-2830">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f1219-2831">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f1219-2831">Az.CognitiveServices</span></span>
* <span data-ttu-id="f1219-2832">Stöd för Get-AzCognitiveServicesAccountSkus utan ett befintligt konto.</span><span class="sxs-lookup"><span data-stu-id="f1219-2832">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f1219-2833">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f1219-2833">Az.Compute</span></span>
* <span data-ttu-id="f1219-2834">Åtgärdade fel där Get-AzVM -ResourceGroupName <rg> returnerar fler än 50 resultat om det behövs</span><span class="sxs-lookup"><span data-stu-id="f1219-2834">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="f1219-2835">Lade till ett exempel för SimpleParameterSet i hjälpen för cmdleten New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="f1219-2835">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="f1219-2836">Ett stavfel i förloppsmeddelandet för Azure Disk Encryption har korrigerats</span><span class="sxs-lookup"><span data-stu-id="f1219-2836">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="f1219-2837">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="f1219-2837">Az.DataFactoryV2</span></span>
* <span data-ttu-id="f1219-2838">ADF .Net SDK-versionen har uppdaterats till 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="f1219-2838">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f1219-2839">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f1219-2839">Az.Network</span></span>
* <span data-ttu-id="f1219-2840">Funktionalitet för NetworkProfile har lagts till.</span><span class="sxs-lookup"><span data-stu-id="f1219-2840">Added NetworkProfile functionality.</span></span> <span data-ttu-id="f1219-2841">nya cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="f1219-2841">new cmdlets added</span></span>
    - <span data-ttu-id="f1219-2842">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f1219-2842">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="f1219-2843">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f1219-2843">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="f1219-2844">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f1219-2844">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="f1219-2845">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f1219-2845">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="f1219-2846">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="f1219-2846">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="f1219-2847">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="f1219-2847">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="f1219-2848">Länk för tjänstassociering på modell för undernät har lagts till</span><span class="sxs-lookup"><span data-stu-id="f1219-2848">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="f1219-2849">Cmdletarna New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap och Remove-AzVirtualNetworkTap har lagts till</span><span class="sxs-lookup"><span data-stu-id="f1219-2849">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="f1219-2850">Cmdletarna Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig och Remove-AzNEtworkInterfaceTapConfig har lagts till</span><span class="sxs-lookup"><span data-stu-id="f1219-2850">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="f1219-2851">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="f1219-2851">Az.RedisCache</span></span>
* <span data-ttu-id="f1219-2852">Tillåt att alla strängar används som storleksparametrar framöver.</span><span class="sxs-lookup"><span data-stu-id="f1219-2852">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="f1219-2853">Lägg till P5 i popup-fönstret PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="f1219-2853">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="f1219-2854">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f1219-2854">Az.Resources</span></span>
* <span data-ttu-id="f1219-2855">Parametern -Mode som saknades i Set-AzPolicyDefinition har lagts till</span><span class="sxs-lookup"><span data-stu-id="f1219-2855">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="f1219-2856">Åtgärdade buggen för cmdleten Get-AzProviderOperation för åtgärder med ursprung som innehåller användare</span><span class="sxs-lookup"><span data-stu-id="f1219-2856">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="f1219-2857">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f1219-2857">Az.Sql</span></span>
* <span data-ttu-id="f1219-2858">Ett problem där vissa cmdletar för säkerhetskopiering inte kunde identifiera den aktuella azure-prenumerationen har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="f1219-2858">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f1219-2859">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f1219-2859">Az.Websites</span></span>
* <span data-ttu-id="f1219-2860">Ny cmdlet: Get-AzWebAppContainerContinuousDeploymentUrl – Hämtar webhook-URL:en för kontinuerlig distribution av container</span><span class="sxs-lookup"><span data-stu-id="f1219-2860">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="f1219-2861">Nya cmdletar: New-AzWebAppContainerPSSession och Enter-WebAppContainerPSSession – Startar en PowerShell-fjärrsession i en containerapp för windows</span><span class="sxs-lookup"><span data-stu-id="f1219-2861">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="f1219-2862">0.2.0 – september 2018</span><span class="sxs-lookup"><span data-stu-id="f1219-2862">0.2.0 - September 2018</span></span>
 <span data-ttu-id="f1219-2863">Första versionen</span><span class="sxs-lookup"><span data-stu-id="f1219-2863">Initial Release</span></span>
