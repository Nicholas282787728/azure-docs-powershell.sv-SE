---
title: Viktig information om Azure PowerShell
description: Lär dig mer om alla de senaste uppdateringarna för Azure PowerShell-modulerna.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.openlocfilehash: 77cbbeb01f5c6fcbf0f61bfab3d3f63b74a53bc4
ms.sourcegitcommit: edfe63c6949cd59127028ac8a13bb4a8827d555c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/04/2020
ms.locfileid: "87566622"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="b4d0c-103">Viktig information om Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="b4d0c-103">Azure PowerShell release notes</span></span>

## <a name="450---august-2020"></a><span data-ttu-id="b4d0c-104">4.5.0 – augusti 2020</span><span class="sxs-lookup"><span data-stu-id="b4d0c-104">4.5.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b4d0c-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b4d0c-105">Az.Accounts</span></span>
* <span data-ttu-id="b4d0c-106">Uppdaterade ”Connect-AzAccount” så att det accepterar parametern ”MaxContextPopulation” [#9865]</span><span class="sxs-lookup"><span data-stu-id="b4d0c-106">Updated 'Connect-AzAccount' to accept parameter 'MaxContextPopulation' [#9865]</span></span>
* <span data-ttu-id="b4d0c-107">Uppdaterade SubscriptionClient-versionen till 2019-06-01 och visa klientdomäner [#9838]</span><span class="sxs-lookup"><span data-stu-id="b4d0c-107">Updated SubscriptionClient version to 2019-06-01 and display tenant domains [#9838]</span></span>
* <span data-ttu-id="b4d0c-108">Information om hemklientorganisation och managedBy-klientorganisation som stöds för prenumerationen</span><span class="sxs-lookup"><span data-stu-id="b4d0c-108">Supported home tenant and managedBy tenant information of subscription</span></span>
* <span data-ttu-id="b4d0c-109">Korrigerade modulnamn, versionsinformation i telemetridata</span><span class="sxs-lookup"><span data-stu-id="b4d0c-109">Corrected module name, version info in telemetry data</span></span>
* <span data-ttu-id="b4d0c-110">Justerade SqlDatabaseDnsSuffix och ServiceManagementUrl om miljöns slutpunkt för metadata returnerar ett inkompatibelt värde</span><span class="sxs-lookup"><span data-stu-id="b4d0c-110">Adjusted SqlDatabaseDnsSuffix and ServiceManagementUrl if environment metadata endpoint returns incompatible value</span></span>

#### <a name="azaks"></a><span data-ttu-id="b4d0c-111">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="b4d0c-111">Az.Aks</span></span>
* <span data-ttu-id="b4d0c-112">Tog bort ”ClientIdAndSecret” för ”ServicePrincipalIdAndSecret” och ställde in ”ClientIdAndSecret” som ett alias [#12381].</span><span class="sxs-lookup"><span data-stu-id="b4d0c-112">Removed 'ClientIdAndSecret' to 'ServicePrincipalIdAndSecret' and set 'ClientIdAndSecret' as an alias [#12381].</span></span>
* <span data-ttu-id="b4d0c-113">Tog bort ”Get-AzAks”/”New-AzAks”/”Remove-AzAks”/”Set-AzAks” för ”Get-AzAksCluster”/”New-AzAksCluster”/”Remove-AzAksCluster”/”Set-AzAksCluster” och ställde in de ursprungliga som alias [#12373].</span><span class="sxs-lookup"><span data-stu-id="b4d0c-113">Removed 'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks' to 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster' and set the original ones as alias [#12373].</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="b4d0c-114">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b4d0c-114">Az.ApiManagement</span></span>
* <span data-ttu-id="b4d0c-115">Lade till ny cmdlet: ”Add-AzApiManagementApiToGateway”.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-115">Added new 'Add-AzApiManagementApiToGateway' cmdlet.</span></span>
* <span data-ttu-id="b4d0c-116">Lade till ny cmdlet: ”Get-AzApiManagementGateway”.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-116">Added new 'Get-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="b4d0c-117">Lade till ny cmdlet: ”Get-AzApiManagementGatewayHostnameConfiguration”.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-117">Added new 'Get-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="b4d0c-118">Lade till ny cmdlet: ”Get-AzApiManagementGatewayKey”.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-118">Added new 'Get-AzApiManagementGatewayKey' cmdlet.</span></span>
* <span data-ttu-id="b4d0c-119">Lade till ny cmdlet: ”New-AzApiManagementGateway”.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-119">Added new 'New-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="b4d0c-120">Lade till ny cmdlet: ”New-AzApiManagementGatewayHostnameConfiguration”.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-120">Added new 'New-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="b4d0c-121">Lade till ny cmdlet: ”New-AzApiManagementResourceLocationObject”.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-121">Added new 'New-AzApiManagementResourceLocationObject' cmdlet.</span></span>
* <span data-ttu-id="b4d0c-122">Lade till ny cmdlet: ”Remove-AzApiManagementApiFromGateway”.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-122">Added new 'Remove-AzApiManagementApiFromGateway' cmdlet.</span></span>
* <span data-ttu-id="b4d0c-123">Lade till ny cmdlet: ”Remove-AzApiManagementGateway”.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-123">Added new 'Remove-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="b4d0c-124">Lade till ny cmdlet: ”Remove-AzApiManagementGatewayHostnameConfiguration”.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-124">Added new 'Remove-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="b4d0c-125">Lade till ny cmdlet: ”Update-AzApiManagementGateway”.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-125">Added new 'Update-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="b4d0c-126">Lade till den nya valfria parametern [-GatewayId] till cmdleten ”Get-AzApiManagementApi”.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-126">Added new optional [-GatewayId] parameter to the 'Get-AzApiManagementApi' cmdlet.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="b4d0c-127">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="b4d0c-127">Az.CognitiveServices</span></span>
* <span data-ttu-id="b4d0c-128">Använde ”Neka” som standardåtgärd för NetworkRules.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-128">Used 'Deny' specifically as NetworkRules default action.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="b4d0c-129">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="b4d0c-129">Az.FrontDoor</span></span>
* <span data-ttu-id="b4d0c-130">Åtgärdade ett problem där ett undantag uppstår när Enum.Parse försöker att tvinga ett null-värde till aktiverade eller inaktiverade uppräkningsvärden [#12344]</span><span class="sxs-lookup"><span data-stu-id="b4d0c-130">Fixed an issue where an exception is being thrown when Enum.Parse tries to coerce a null value to an Enabled or Disabled enum values [#12344]</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="b4d0c-131">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="b4d0c-131">Az.HDInsight</span></span>
* <span data-ttu-id="b4d0c-132">Stöd för att skapa kluster med funktionen Kryptering under överföring.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-132">Supported creating cluster with encryption in transit feature.</span></span>
    - <span data-ttu-id="b4d0c-133">Lägg till den nya parametern ”EncryptionInTransit” till cmdleten ”New-AzHDInsightCluster”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-133">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="b4d0c-134">Lägg till den nya parametern ”EncryptionInTransit” till cmdleten ”New-AzHDInsightClusterConfig”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-134">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="b4d0c-135">Stöd för att skapa kluster med funktionen privat länk:</span><span class="sxs-lookup"><span data-stu-id="b4d0c-135">Supported creating cluster with private link feature:</span></span>
    - <span data-ttu-id="b4d0c-136">Lägg till de nya parametrarna ”PublicNetworkAccessType” och ”OutboundPublicNetworkAccessType” till cmdleten ”New-AzHDInsightCluster”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-136">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="b4d0c-137">Lägg till de nya parametrarna ”PublicNetworkAccessType” och ”OutboundPublicNetworkAccessType” till cmdleten ”New-AzHDInsightClusterConfig”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-137">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="b4d0c-138">Returnerade information om det virtuella nätverket vid anrop till ”New-AzHDInsightCluster” eller ”Get-AzHDInsightCluster”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-138">Returned virtual network information when calling 'New-AzHDInsightCluster' or 'Get-AzHDInsightCluster'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b4d0c-139">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b4d0c-139">Az.Network</span></span>
* <span data-ttu-id="b4d0c-140">Stöd har lagts till för parametern AddressPrefixType i ”Remove-AzExpressRouteCircuitConnectionConfig”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-140">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="b4d0c-141">Lade till bakåtkompatibel ändringar: PeerAddressType-funktioner för privat peering i ”Remove-AzExpressRouteCircutPeeringConfig”.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-141">Added non-breaking changes: PeerAddressType functionality for Private Peering in 'Remove-AzExpressRouteCircutPeeringConfig'.</span></span>
* <span data-ttu-id="b4d0c-142">Koden ändrades för att ignorera skiftläge för parametrarna AddressPrefixType och PeerAddressType.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-142">Code changed to ignore case for AddressPrefixType and PeerAddressType parameter.</span></span>
* <span data-ttu-id="b4d0c-143">Ändrade varningsmeddelandet för ”New-AzLoadBalancerFrontendIpConfig”, ”New-AzPublicIpAddress” och ”New-AzPublicIpPrefix”.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-143">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="b4d0c-144">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="b4d0c-144">Az.OperationalInsights</span></span>
* <span data-ttu-id="b4d0c-145">Lade till alternativet ”-ForceDelete” för ”Remove-AzOperationalInsightsworkspace”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-145">Added '-ForceDelete' option for 'Remove-AzOperationalInsightsworkspace'</span></span>
* <span data-ttu-id="b4d0c-146">Lade till ny cmdlet: ”Get-AzOperationalInsightsDeletedWorkspace”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-146">Added new cmdlet 'Get-AzOperationalInsightsDeletedWorkspace'</span></span>
* <span data-ttu-id="b4d0c-147">Lade till ny cmdlet: ”Restore-AzOperationalInsightsWorkspace”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-147">Added new cmdlet 'Restore-AzOperationalInsightsWorkspace'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b4d0c-148">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b4d0c-148">Az.RecoveryServices</span></span>
* <span data-ttu-id="b4d0c-149">Förbättrade sättet Azure Backup-containrar/objekt identifieras.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-149">Improved the Azure Backup container/item discovery experience.</span></span>

#### <a name="azresources"></a><span data-ttu-id="b4d0c-150">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b4d0c-150">Az.Resources</span></span>
* <span data-ttu-id="b4d0c-151">Lade till egenskaperna ”Condition”, ”ConditionVersion” och ”Description” till ”New-AzRoleAssignment”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-151">Added properties 'Condition', 'ConditionVersion' and 'Description' to 'New-AzRoleAssignment'</span></span>
    - <span data-ttu-id="b4d0c-152">Detta omfattade alla relevanta ändringar av datamodellerna</span><span class="sxs-lookup"><span data-stu-id="b4d0c-152">This included all the relevant changes to the data models</span></span>

#### <a name="azsql"></a><span data-ttu-id="b4d0c-153">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b4d0c-153">Az.Sql</span></span>
* <span data-ttu-id="b4d0c-154">Korrigerade ett potentiellt fel med skiftlägesokänsliga servernamn i ”New-AzSqlServer” och ”Set-AzSqlServer”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-154">Fixed potential server name case insensitive error in 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="b4d0c-155">Korrigerade att fel databasnamn returnerades vid ett befintligt databasfel i ”New-AzSqlDatabaseSecondary”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-155">Fixed wrong database name returned on existing database error in 'New-AzSqlDatabaseSecondary'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b4d0c-156">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b4d0c-156">Az.Storage</span></span>
* <span data-ttu-id="b4d0c-157">Stöd för att skapa container/blob för SAS-token med de nya behörigheterna x, t</span><span class="sxs-lookup"><span data-stu-id="b4d0c-157">Supported create container/blob Sas token with new permission x,t</span></span>
    -  <span data-ttu-id="b4d0c-158">”New-AzStorageBlobSASToken”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-158">'New-AzStorageBlobSASToken'</span></span>
    -  <span data-ttu-id="b4d0c-159">”New-AzStorageContainerSASToken”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-159">'New-AzStorageContainerSASToken'</span></span>
* <span data-ttu-id="b4d0c-160">Stöd för att skapa konto för SAS-token med de nya behörigheterna x, t, f</span><span class="sxs-lookup"><span data-stu-id="b4d0c-160">Supported create account Sas token with new permission x,t,f</span></span>
    -  <span data-ttu-id="b4d0c-161">”New-AzStorageAccountSASToken”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-161">'New-AzStorageAccountSASToken'</span></span>
* <span data-ttu-id="b4d0c-162">Stöd för att hämta förbrukning av enskild filresurs</span><span class="sxs-lookup"><span data-stu-id="b4d0c-162">Supported get single file share usage</span></span>
    - <span data-ttu-id="b4d0c-163">”Get-AzRmStorageShare”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-163">'Get-AzRmStorageShare'</span></span>

## <a name="440---july-2020"></a><span data-ttu-id="b4d0c-164">4.4.0 – juli 2020</span><span class="sxs-lookup"><span data-stu-id="b4d0c-164">4.4.0 - July 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b4d0c-165">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b4d0c-165">Az.Accounts</span></span>
* <span data-ttu-id="b4d0c-166">En ny cmdlet, ”Invoke-AzRestMethod”, har lagts till</span><span class="sxs-lookup"><span data-stu-id="b4d0c-166">Added new cmdlet 'Invoke-AzRestMethod'</span></span>
* <span data-ttu-id="b4d0c-167">Ett problem åtgärdades som kan orsaka autentiseringsfel i scenarier med fler processer, t.ex. när flera Azure PowerShell-cmdletar körs med ”Start-Job” [#9448]</span><span class="sxs-lookup"><span data-stu-id="b4d0c-167">Fixed an issue that may cause authentication errors in multi-process scenarios such as running multiple Azure PowerShell cmdlets using 'Start-Job' [#9448]</span></span>

#### <a name="azaks"></a><span data-ttu-id="b4d0c-168">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="b4d0c-168">Az.Aks</span></span>
* <span data-ttu-id="b4d0c-169">Felet som gjorde att ”Get-AzAks” inte hämtade alla kluster har åtgärdats [#12296]</span><span class="sxs-lookup"><span data-stu-id="b4d0c-169">Fixed bug 'Get-AzAks' doesn't get all clusters [#12296]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="b4d0c-170">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="b4d0c-170">Az.AnalysisServices</span></span>
* <span data-ttu-id="b4d0c-171">Projektreferensen till autentisering har tagits bort</span><span class="sxs-lookup"><span data-stu-id="b4d0c-171">Removed project reference to Authentication</span></span>

#### <a name="azautomation"></a><span data-ttu-id="b4d0c-172">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b4d0c-172">Az.Automation</span></span>
* <span data-ttu-id="b4d0c-173">Problemet som gjorde att strängar med escape-tecken inte kunde konverteras till JSON-objekt har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-173">Fixed the issue that string with escape chars cannot be converted into json object.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b4d0c-174">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b4d0c-174">Az.Compute</span></span>
* <span data-ttu-id="b4d0c-175">En varning har lats till som visas när ”New-AzVmss” används utan den senaste avbildningsversionen</span><span class="sxs-lookup"><span data-stu-id="b4d0c-175">Added warning when using 'New-AzVmss' without 'latest' image version</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b4d0c-176">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b4d0c-176">Az.DataFactory</span></span>
* <span data-ttu-id="b4d0c-177">Globala parametrar har lagts till för Data Factory.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-177">Added global parameters to Data Factory.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="b4d0c-178">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="b4d0c-178">Az.EventGrid</span></span>
* <span data-ttu-id="b4d0c-179">Modulen har uppdaterats så att API-version 2020-06-01 används.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-179">Updated to use the 2020-06-01 API version.</span></span>
* <span data-ttu-id="b4d0c-180">Nya funktioner har lagts till:</span><span class="sxs-lookup"><span data-stu-id="b4d0c-180">Added new features:</span></span>
    - <span data-ttu-id="b4d0c-181">Indatamappning</span><span class="sxs-lookup"><span data-stu-id="b4d0c-181">Input mapping</span></span>
    - <span data-ttu-id="b4d0c-182">Schema för händelseleverans</span><span class="sxs-lookup"><span data-stu-id="b4d0c-182">Event Delivery Schema</span></span>
    - <span data-ttu-id="b4d0c-183">Private Link</span><span class="sxs-lookup"><span data-stu-id="b4d0c-183">Private Link</span></span>
    - <span data-ttu-id="b4d0c-184">Cloud Event V10 Schema</span><span class="sxs-lookup"><span data-stu-id="b4d0c-184">Cloud Event V10 Schema</span></span>
    - <span data-ttu-id="b4d0c-185">Service Bus-ämne som mål</span><span class="sxs-lookup"><span data-stu-id="b4d0c-185">Service Bus Topic As Destination</span></span>
    - <span data-ttu-id="b4d0c-186">Azure-funktion som mål</span><span class="sxs-lookup"><span data-stu-id="b4d0c-186">Azure Function As Destination</span></span>
    - <span data-ttu-id="b4d0c-187">Webhook-batchbearbetning</span><span class="sxs-lookup"><span data-stu-id="b4d0c-187">WebHook Batching</span></span>
    - <span data-ttu-id="b4d0c-188">Säker webhook (AAD-stöd)</span><span class="sxs-lookup"><span data-stu-id="b4d0c-188">Secure webhook (AAD support)</span></span>
    - <span data-ttu-id="b4d0c-189">IpFiltering</span><span class="sxs-lookup"><span data-stu-id="b4d0c-189">IpFiltering</span></span>
* <span data-ttu-id="b4d0c-190">Uppdaterade cmdletar:</span><span class="sxs-lookup"><span data-stu-id="b4d0c-190">Updated cmdlets:</span></span>
    - <span data-ttu-id="b4d0c-191">”New-AzEventGridSubscription”/”Update-AzEventGridSubscription”:</span><span class="sxs-lookup"><span data-stu-id="b4d0c-191">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span></span>
        - <span data-ttu-id="b4d0c-192">Lägg till nya valfria parametrar för att ge stöd för webhook-batchbearbetning.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-192">Add new optional parameters to support webhook batching.</span></span>
        - <span data-ttu-id="b4d0c-193">Lägg till nya valfria parametrar för att ge stöd för skyddad webhook med AAD.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-193">Add new optional parameters to support secured webhook using AAD.</span></span>
        - <span data-ttu-id="b4d0c-194">Lägg till ny enum (uppräkning) för EndpointType-parametern för att ge stöd för Azure-funktion och Service Bus-ämne som nya mål.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-194">Add new enum for EndpointType parameter to support azure function and service bus topic as new destinations.</span></span>
        - <span data-ttu-id="b4d0c-195">Lägg till ny valfri parameter för leveransschema.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-195">Add new optional parameter for delivery schema.</span></span>
    - <span data-ttu-id="b4d0c-196">”New-AzEventGridTopic”/”Update-AzEventGridTopic” och ”New-AzEventGridDomain”/”Update-AzEventGridDomain”:</span><span class="sxs-lookup"><span data-stu-id="b4d0c-196">'New-AzEventGridTopic'/'Update-AzEventGridTopic' and 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span></span>
        - <span data-ttu-id="b4d0c-197">Lägg till nya valfria parametrar för att ge stöd för IpFiltering.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-197">Add new optional parameters to support IpFiltering.</span></span>
    - <span data-ttu-id="b4d0c-198">”New-AzEventGridTopic”/”New-AzEventGridDomain”:</span><span class="sxs-lookup"><span data-stu-id="b4d0c-198">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span></span>
        - <span data-ttu-id="b4d0c-199">Lägg till nya valfria parametrar för att ge stöd för indatamappning.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-199">Add new optional parameters to support Input mapping.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="b4d0c-200">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="b4d0c-200">Az.FrontDoor</span></span>
* <span data-ttu-id="b4d0c-201">Modulen har uppdaterats så att API 2020-05-01 används</span><span class="sxs-lookup"><span data-stu-id="b4d0c-201">Updated module to use API 2020-05-01</span></span>
* <span data-ttu-id="b4d0c-202">Stöd för privat länk har lagts till för Storage-, KeyVault- och Web App Service-resurser</span><span class="sxs-lookup"><span data-stu-id="b4d0c-202">Added Private link support for Storage, Keyvault and Web App Service resources</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="b4d0c-203">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="b4d0c-203">Az.HDInsight</span></span>
* <span data-ttu-id="b4d0c-204">Stöd för att skapa kluster med ADLSGen1/2-lagring i nationella moln.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-204">Supported creating cluster with ADLSGen1/2 storage in national clouds.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="b4d0c-205">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b4d0c-205">Az.Monitor</span></span>
* <span data-ttu-id="b4d0c-206">Bugg som orsakade fel med ”Get-AzDiagnosticSetting” när mått eller loggar var null har åtgärdats [#12272]</span><span class="sxs-lookup"><span data-stu-id="b4d0c-206">Fixed bug for 'Get-AzDiagnosticSetting' when metrics or logs are null [#12272]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b4d0c-207">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b4d0c-207">Az.Network</span></span>
* <span data-ttu-id="b4d0c-208">Parameterväxlingen i VWan HubVnet-anslutningar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="b4d0c-208">Fixed parameters swap in VWan HubVnet connection</span></span>
* <span data-ttu-id="b4d0c-209">Nya cmdletar har lagts till för platser för virtuella installationer i Azure-nätverk</span><span class="sxs-lookup"><span data-stu-id="b4d0c-209">Added new cmdlets for Azure Network Virtual Appliance Sites</span></span>
    - <span data-ttu-id="b4d0c-210">”Get-AzVirtualApplianceSite”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-210">'Get-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="b4d0c-211">”New-AzVirtualApplianceSite”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-211">'New-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="b4d0c-212">”Remove-AzVirtualApplianceSite”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-212">'Remove-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="b4d0c-213">”Update-AzVirtualApplianceSite”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-213">'Update-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="b4d0c-214">”New-AzOffice365PolicyProperty”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-214">'New-AzOffice365PolicyProperty'</span></span>
* <span data-ttu-id="b4d0c-215">Nya cmdletar har lagts till för virtuella installationer i Azure-nätverk</span><span class="sxs-lookup"><span data-stu-id="b4d0c-215">Added new cmdlets for Azure Network Virtual Appliance</span></span>
    - <span data-ttu-id="b4d0c-216">”Get-AzNetworkVirtualAppliance”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-216">'Get-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="b4d0c-217">”New-AzNetworkVirtualAppliance”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-217">'New-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="b4d0c-218">”Remove-AzNetworkVirtualAppliance”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-218">'Remove-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="b4d0c-219">”Update-AzNetworkVirtualAppliance”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-219">'Update-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="b4d0c-220">”Get-AzNetworkVirtualApplianceSku”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-220">'Get-AzNetworkVirtualApplianceSku'</span></span>
    - <span data-ttu-id="b4d0c-221">”New-AzVirtualApplianceSkuProperty”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-221">'New-AzVirtualApplianceSkuProperty'</span></span>
* <span data-ttu-id="b4d0c-222">Application Gateway har introducerats i vanliga cmdletar för Private Link</span><span class="sxs-lookup"><span data-stu-id="b4d0c-222">Onboarded Application Gateway to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="b4d0c-223">StorageSync har introducerats i vanliga cmdletar för Private Link</span><span class="sxs-lookup"><span data-stu-id="b4d0c-223">Onboarded StorageSync to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="b4d0c-224">SignalR har introducerats i vanliga cmdletar för Private Link</span><span class="sxs-lookup"><span data-stu-id="b4d0c-224">Onboarded SignalR to Private Link Common Cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b4d0c-225">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b4d0c-225">Az.RecoveryServices</span></span>
* <span data-ttu-id="b4d0c-226">Projektreferensen till autentisering har tagits bort</span><span class="sxs-lookup"><span data-stu-id="b4d0c-226">Removed project reference to Authentication</span></span>
* <span data-ttu-id="b4d0c-227">Azure Backup-anpassade cmdletar gör text mer korrekt.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-227">Azure Backup tuned cmdlets help text to be more accurate.</span></span>
* <span data-ttu-id="b4d0c-228">Stöd har lagts till som gör att Azure Backup kan hämta MAB-agentjobb med cmdleten ”Get-AzRecoveryServicesBackupJob”.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-228">Azure Backup added support for fetching MAB agent jobs using 'Get-AzRecoveryServicesBackupJob' cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="b4d0c-229">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b4d0c-229">Az.Resources</span></span>
* <span data-ttu-id="b4d0c-230">”Save-AzResourceGroupDeploymentTemplate” har uppdaterats för att använda SDK:n.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-230">Updated 'Save-AzResourceGroupDeploymentTemplate' to use the SDK.</span></span>
* <span data-ttu-id="b4d0c-231">Cmdleten ”Unregister-AzResourceProvider” har lagts till.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-231">Added 'Unregister-AzResourceProvider' cmdlet.</span></span>

#### <a name="azsql"></a><span data-ttu-id="b4d0c-232">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b4d0c-232">Az.Sql</span></span>
* <span data-ttu-id="b4d0c-233">Stöd har lagts till för SPN och gästanvändare i cmdleten ”Set-AzSqlInstanceActiveDirectoryAdministrator”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-233">Added support for Service principal and guest users in Set-AzSqlInstanceActiveDirectoryAdministrator cmdlet'</span></span>
* <span data-ttu-id="b4d0c-234">En bugg har åtgärdats i cmdletar för dataklassificering.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-234">Fixed a bug in Data Classification cmdlets.'</span></span>
* <span data-ttu-id="b4d0c-235">Stöd har lagts till för redundansväxling med Azure SQL Managed Instance: ”Invoke-AzSqlInstanceFailover”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-235">Added support for Azure SQL Managed Instance failover: 'Invoke-AzSqlInstanceFailover'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b4d0c-236">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b4d0c-236">Az.Storage</span></span>
* <span data-ttu-id="b4d0c-237">Problemet som gjorde att UserAgent inte lades till för vissa cmdletar för dataplanet har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-237">Fixed the issue that UserAgent is not added for some data plane cmdlets.</span></span>
* <span data-ttu-id="b4d0c-238">Stöd har lagts till för att skapa/uppdatera Storage-konto med MinimumTlsVersion och AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="b4d0c-238">Supported create/update Storage account with MinimumTlsVersion and AllowBlobPublicAccess</span></span>
    -  <span data-ttu-id="b4d0c-239">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="b4d0c-239">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="b4d0c-240">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="b4d0c-240">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="b4d0c-241">Stöd har lagts till för att aktivera/inaktivera versionshantering i Blob Service för ett Storage-konto</span><span class="sxs-lookup"><span data-stu-id="b4d0c-241">Support enable/disable versioning on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="b4d0c-242">”Update-AzStorageBlobServiceProperty”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-242">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="b4d0c-243">Stöd har lagts till för att visa blobar med blobversioner</span><span class="sxs-lookup"><span data-stu-id="b4d0c-243">Support list blobs with blob versions</span></span>
    - <span data-ttu-id="b4d0c-244">”Get-AzStorageBlob”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-244">'Get-AzStorageBlob'</span></span>
* <span data-ttu-id="b4d0c-245">Stöd har lagts till för att hämta/ta bort enskilda ögonblicksbilder av blobar eller blobversioner</span><span class="sxs-lookup"><span data-stu-id="b4d0c-245">Support get/remove single blob snapshot or blob version</span></span>
    - <span data-ttu-id="b4d0c-246">”Get-AzStorageBlob”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-246">'Get-AzStorageBlob'</span></span>
    - <span data-ttu-id="b4d0c-247">”Remove-AzStorageBlob”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-247">'Remove-AzStorageBlob'</span></span>
* <span data-ttu-id="b4d0c-248">Stöd har lagts till för pipelines från blobobjekt genererade av Azure.Storage.Blobs V12</span><span class="sxs-lookup"><span data-stu-id="b4d0c-248">Support pipeline from blob object generated from Azure.Storage.Blobs V12</span></span>
    - <span data-ttu-id="b4d0c-249">”Get-AzStorageBlobContent”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-249">'Get-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="b4d0c-250">”New-AzStorageBlobSASToken”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-250">'New-AzStorageBlobSASToken'</span></span>
    - <span data-ttu-id="b4d0c-251">”Remove-AzStorageBlob”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-251">'Remove-AzStorageBlob'</span></span>
    - <span data-ttu-id="b4d0c-252">”Set-AzStorageBlobContent”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-252">'Set-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="b4d0c-253">”Start-AzStorageBlobCopy”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-253">'Start-AzStorageBlobCopy'</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="b4d0c-254">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="b4d0c-254">Az.StorageSync</span></span>
* <span data-ttu-id="b4d0c-255">En ny version har lagts till för StorageSync SDK som körs mot ApiVersion 2020-03-01</span><span class="sxs-lookup"><span data-stu-id="b4d0c-255">Added a new version StorageSync SDK targeting ApiVersion 2020-03-01</span></span>
* <span data-ttu-id="b4d0c-256">En cmdlet för synkroniseringstjänsten för lagringsuppdatering har lagts till</span><span class="sxs-lookup"><span data-stu-id="b4d0c-256">Added Update Storage Sync Service cmdlet</span></span>
    - <span data-ttu-id="b4d0c-257">”Set-AzStorageSyncService”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-257">'Set-AzStorageSyncService'</span></span>
* <span data-ttu-id="b4d0c-258">IncomingTrafficPolicy och PrivateEndpointConnections har lagts till för StorageSyncService-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-258">Added IncomingTrafficPolicy and PrivateEndpointConnections to StorageSyncService cmdlets.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b4d0c-259">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b4d0c-259">Az.Websites</span></span>
* <span data-ttu-id="b4d0c-260">Stöd har lagts till för att utföra åtgärder för platser som inte tillhör samma resursgrupp som App Services-planen</span><span class="sxs-lookup"><span data-stu-id="b4d0c-260">Added support to perform operations for Slots not in the same resource group as the App Service Plan</span></span>

## <a name="430---june-2020"></a><span data-ttu-id="b4d0c-261">4.3.0 – juni 2020</span><span class="sxs-lookup"><span data-stu-id="b4d0c-261">4.3.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b4d0c-262">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b4d0c-262">Az.Accounts</span></span>
* <span data-ttu-id="b4d0c-263">Stöd för identifiering av miljöinställning som standard och tillägg av miljön via ”Add-AzEnvironment”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-263">Supported discovering environment setting by default and adding environment via 'Add-AzEnvironment'</span></span>
* <span data-ttu-id="b4d0c-264">Uppdatera förinlästa sammansättningar [#12024], [#11976]</span><span class="sxs-lookup"><span data-stu-id="b4d0c-264">Update preloaded assemblies [#12024], [#11976]</span></span>
* <span data-ttu-id="b4d0c-265">Uppdaterad Azure.Core-sammansättning</span><span class="sxs-lookup"><span data-stu-id="b4d0c-265">Updated Azure.Core assembly</span></span>
* <span data-ttu-id="b4d0c-266">Ett problem har åtgärdats som kan orsaka att ”Connect-AzAccount” misslyckas vid körning av flera trådar [#11201]</span><span class="sxs-lookup"><span data-stu-id="b4d0c-266">Fixed an issue that may cause 'Connect-AzAccount' to fail in multi-threaded execution [#11201]</span></span>

#### <a name="azaks"></a><span data-ttu-id="b4d0c-267">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="b4d0c-267">Az.Aks</span></span>
* <span data-ttu-id="b4d0c-268">Användning av gamla [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) ersattes med anrop till API:erna [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) och [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials)</span><span class="sxs-lookup"><span data-stu-id="b4d0c-268">Replaced usage of old [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) with calls to [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) and [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials) APIs</span></span>

#### <a name="azbatch"></a><span data-ttu-id="b4d0c-269">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="b4d0c-269">Az.Batch</span></span>
* <span data-ttu-id="b4d0c-270">Az.Batch har uppdaterats att använda ”Microsoft.Azure.Management.Batch” SDK till och med version 11.0.0.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-270">Updated Az.Batch to use 'Microsoft.Azure.Management.Batch' SDK version to 11.0.0</span></span>
* <span data-ttu-id="b4d0c-271">Möjligheten att ange BatchAccount-identiteten har lagts till i cmdleten ”New-AzBatchAccount”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-271">Added the ability to set the BatchAccount Identity in the 'New-AzBatchAccount' cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="b4d0c-272">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="b4d0c-272">Az.CognitiveServices</span></span>
* <span data-ttu-id="b4d0c-273">Stöd för att visa kontofunktioner.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-273">Supported displaying account capabilities.</span></span>
* <span data-ttu-id="b4d0c-274">Stöd för att ändra PublicNetworkAccess.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-274">Supported modifying PublicNetworkAccess.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b4d0c-275">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b4d0c-275">Az.Compute</span></span>
* <span data-ttu-id="b4d0c-276">Parametern SimulateEviction har lagts till i cmdletarna set-AzVM och set-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-276">Added SimulateEviction parameter to Set-AzVM and Set-AzVmssVM cmdlets.</span></span>
* <span data-ttu-id="b4d0c-277">”Premium_LRS” har lagts till i argumentslutföraren för parametern StorageAccountType för cmdleten New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-277">Added 'Premium_LRS' to the argument completer of StorageAccountType parameter for New-AzGalleryImageVersion cmdlet.</span></span>
* <span data-ttu-id="b4d0c-278">Understatusar har lagts till i VMCustomScriptExtension [#11297]</span><span class="sxs-lookup"><span data-stu-id="b4d0c-278">Added Substatuses to VMCustomScriptExtension [#11297]</span></span>
* <span data-ttu-id="b4d0c-279">”Delete” har lagts till i argumentslutföraren för parametern EvictionPolicy för cmdletarna New-AzVM och New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-279">Added 'Delete' to the argument completer of EvictionPolicy parameter for New-AzVM and New-AzVMConfig cmdlets.</span></span>
* <span data-ttu-id="b4d0c-280">Åtgärdat namn för nytt VM-tillägg för SAP</span><span class="sxs-lookup"><span data-stu-id="b4d0c-280">Fixed name of new VM Extension for SAP</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b4d0c-281">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b4d0c-281">Az.DataFactory</span></span>
* <span data-ttu-id="b4d0c-282">ADF .Net SDK har uppdaterats till 4.9.0</span><span class="sxs-lookup"><span data-stu-id="b4d0c-282">Updated ADF .Net SDK version to 4.9.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="b4d0c-283">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="b4d0c-283">Az.EventHub</span></span>
* <span data-ttu-id="b4d0c-284">Parametrar för hanterad identitet har lagts till i cmdletarna ”New-AzEventHubNamespace” och ”set-AzEventHubNamespace”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-284">Added Managed Identity parameters to 'New-AzEventHubNamespace' and 'Set-AzEventHubNamespace' cmdlets</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="b4d0c-285">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="b4d0c-285">Az.Functions</span></span>
* <span data-ttu-id="b4d0c-286">Stöd har lagts till för att skapa PowerShell 7.0- och Java 11-funktionsappar</span><span class="sxs-lookup"><span data-stu-id="b4d0c-286">Added support to create PowerShell 7.0 and Java 11 function apps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="b4d0c-287">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="b4d0c-287">Az.HDInsight</span></span>
* <span data-ttu-id="b4d0c-288">Stöd för listning av värdar och omstart för specifika värdar i HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-288">Supported listing hosts and restart specific hosts of the HDInsight cluster.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="b4d0c-289">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="b4d0c-289">Az.HealthcareApis</span></span>
* <span data-ttu-id="b4d0c-290">Uppdaterade SDK-versionen till 1.1.0</span><span class="sxs-lookup"><span data-stu-id="b4d0c-290">Updated the SDK version to 1.1.0</span></span>
* <span data-ttu-id="b4d0c-291">Stöd har lagts till för exportinställningar och hanterad identitet</span><span class="sxs-lookup"><span data-stu-id="b4d0c-291">Added support for Export settings and Managed Identity</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="b4d0c-292">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b4d0c-292">Az.Monitor</span></span>
* <span data-ttu-id="b4d0c-293">Parameter för inmatningsobjekt har åtgärdats för ”Set-AzActivityLogAlert”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-293">Fixed input object parameter for 'Set-AzActivityLogAlert'</span></span>
* <span data-ttu-id="b4d0c-294">Parametern ”InputObject” har åtgärdats för ”Set-AzActionGroup” [#10868]</span><span class="sxs-lookup"><span data-stu-id="b4d0c-294">Fixed 'InputObject' parameter for 'Set-AzActionGroup' [#10868]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b4d0c-295">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b4d0c-295">Az.Network</span></span>
* <span data-ttu-id="b4d0c-296">Stöd har lagts till för parametern AddressPrefixType i ”Remove-AzExpressRouteCircuitConnectionConfig”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-296">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="b4d0c-297">Nya cmdletar har lagts till för Azure FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="b4d0c-297">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="b4d0c-298">”New-AzFirewallPolicyDnsSetting”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-298">'New-AzFirewallPolicyDnsSetting'</span></span>
    - <span data-ttu-id="b4d0c-299">Stöd för mål-FQDN i nätverksregler för brandväggsprincip</span><span class="sxs-lookup"><span data-stu-id="b4d0c-299">Support for Destination FQDN in Network Rules for Firewall Policy</span></span>
* <span data-ttu-id="b4d0c-300">Stöd har lagts till för åtgärder i serverdelsadresspooler</span><span class="sxs-lookup"><span data-stu-id="b4d0c-300">Added support for backend address pool operations</span></span>
    - <span data-ttu-id="b4d0c-301">”New-AzLoadBalancerBackendAddressConfig”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-301">'New-AzLoadBalancerBackendAddressConfig'</span></span>
    - <span data-ttu-id="b4d0c-302">”New-AzLoadBalancerBackendAddressPool”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-302">'New-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="b4d0c-303">”Set-AzLoadBalancerBackendAddressPool”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-303">'Set-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="b4d0c-304">”Remove-AzLoadBalancerBackendAddressPool”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-304">'Remove-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="b4d0c-305">”Get-AzLoadBalancerBackendAddressPool”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-305">'Get-AzLoadBalancerBackendAddressPool'</span></span>
* <span data-ttu-id="b4d0c-306">Namnvalidering har lagts till för ”New-AzIpGroup”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-306">Added name validation for 'New-AzIpGroup'</span></span>
* <span data-ttu-id="b4d0c-307">Nya cmdletar har lagts till för Azure FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="b4d0c-307">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="b4d0c-308">”New-AzFirewallPolicyThreatIntelWhitelist”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-308">'New-AzFirewallPolicyThreatIntelWhitelist'</span></span>
* <span data-ttu-id="b4d0c-309">Nedanstående kommandon för funktionen har uppdaterats: Konfiguration/borttagning av anpassade DNS-servrar på VirtualWan P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-309">Updated below commands for feature: Custom dns servers set/remove on VirtualWan P2SVpnGateway.</span></span>
    - <span data-ttu-id="b4d0c-310">New-AzP2sVpnGateway har uppdaterats: Den valfria parametern ”-CustomDnsServer” har lagts till för att kunder ska kunna ange att deras DNS-servrar ska konfigureras på P2SVpnGateway, som kan användas av punkt-till-plats-klienter.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-310">Updated New-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
    - <span data-ttu-id="b4d0c-311">Update-AzP2sVpnGateway har uppdaterats: Den valfria parametern ”-CustomDnsServer” har lagts till för att kunder ska kunna ange att deras DNS-servrar ska konfigureras på P2SVpnGateway, som kan användas av punkt-till-plats-klienter.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-311">Updated Update-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
* <span data-ttu-id="b4d0c-312">”Update-AzVpnGateway” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="b4d0c-312">Updated 'Update-AzVpnGateway'</span></span>
    - <span data-ttu-id="b4d0c-313">Den valfria parametern ”-BgpPeeringAddress” har lagts till för att kunder ska kunna ange sina anpassade BGP:er som ska konfigurerar på VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-313">Added optional parameter '-BgpPeeringAddress' for customers to specify their custom bgps to set on VpnGateway.</span></span>
* <span data-ttu-id="b4d0c-314">Ny cmdlet har lagts till för att stödja återställning av en VirtualHub-resurs routningsstatus:</span><span class="sxs-lookup"><span data-stu-id="b4d0c-314">Added new cmdlet to support resetting the routing state of a VirtualHub resource:</span></span>
    - <span data-ttu-id="b4d0c-315">”Reset-AzHubRouter”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-315">'Reset-AzHubRouter'</span></span>
* <span data-ttu-id="b4d0c-316">Nedanstående saker har uppdaterats baserat på den senaste Swagger-ändringen för brandväggspolicyn</span><span class="sxs-lookup"><span data-stu-id="b4d0c-316">Updated below things based on recent swagger change for Firewall Policy</span></span>
    - <span data-ttu-id="b4d0c-317">Namn ändras för RuleGroup, RuleCollectionGroup och RuleType</span><span class="sxs-lookup"><span data-stu-id="b4d0c-317">Changes names for RuleGroup, RuleCollectionGroup and RuleType</span></span>
    - <span data-ttu-id="b4d0c-318">Stöd har lagts till för NAT-regelsamlingar för brandväggsprincip så att flera NAT-regelsamlingar stöds</span><span class="sxs-lookup"><span data-stu-id="b4d0c-318">Added support for Firewall Policy NAT Rule Collections to support multiple NAT Rule Collection</span></span>
* <span data-ttu-id="b4d0c-319">[Icke-bakåtkompatibel ändring] Den obligatoriska parametern ”SourceIpGroup” har lagts till för ”New-AzFirewallPolicyApplicationRule” och ”New-AzFirewallPolicyNetworkRule”.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-319">[Breaking Change] Added mandatory parameter 'SourceIpGroup' for 'New-AzFirewallPolicyApplicationRule' and 'New-AzFirewallPolicyNetworkRule'.</span></span>
* <span data-ttu-id="b4d0c-320">[Icke-bakåtkompatibel ändring] ”New-AzFirewallPolicyApplicationRule” har åtgärdats, parametern ”SourceAddress” är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-320">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="b4d0c-321">[Icke-bakåtkompatibel ändring] ”New-AzFirewallPolicyApplicationRule” har åtgärdats, parametern ”SourceAddress” är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-321">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="b4d0c-322">[Icke-bakåtkompatibel ändring] Obligatoriska parametrar har tagits bort: ”TranslatedAddress”, ”TranslatedPort” för ”New-AzFirewallPolicyNatRuleCollection”.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-322">[Breaking Change] Removed mandatory parameters: 'TranslatedAddress', 'TranslatedPort' for 'New-AzFirewallPolicyNatRuleCollection'.</span></span>
* <span data-ttu-id="b4d0c-323">Nya cmdletar har lagts till för att stödja PrivateLink på Application Gateway</span><span class="sxs-lookup"><span data-stu-id="b4d0c-323">Added new cmdlets to support PrivateLink On Application Gateway</span></span>
    - <span data-ttu-id="b4d0c-324">”New-AzApplicationGatewayPrivateLinkConfiguration”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-324">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="b4d0c-325">”Get-AzApplicationGatewayPrivateLinkConfiguration”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-325">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="b4d0c-326">”New-AzApplicationGatewayPrivateLinkConfiguration”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-326">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="b4d0c-327">”Set-AzApplicationGatewayPrivateLinkConfiguration”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-327">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="b4d0c-328">”Remove-AzApplicationGatewayPrivateLinkConfiguration”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-328">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="b4d0c-329">”New-AzApplicationGatewayPrivateLinkIpConfiguration”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-329">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span></span>
* <span data-ttu-id="b4d0c-330">Nya cmdletar har lagts till för VirtualHubs underordnade resurs HubRouteTables.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-330">Added new cmdlets for HubRouteTables child resource of VirtualHub.</span></span>
    - <span data-ttu-id="b4d0c-331">”New-AzVHubRoute”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-331">'New-AzVHubRoute'</span></span>
    - <span data-ttu-id="b4d0c-332">”New-AzVHubRouteTable”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-332">'New-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="b4d0c-333">”Get-AzVHubRouteTable”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-333">'Get-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="b4d0c-334">”Update-AzVHubRouteTable”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-334">'Update-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="b4d0c-335">”Remove-AzVHubRouteTable”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-335">'Remove-AzVHubRouteTable'</span></span>
* <span data-ttu-id="b4d0c-336">Befintliga cmdletar har uppdaterats för att stödja valfri RoutingConfiguration-indataparameter för anpassad routning i VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-336">Updated existing cmdlets to support optional RoutingConfiguration input parameter for custom routing in VirtualWan.</span></span>
    - <span data-ttu-id="b4d0c-337">”New-AzExpressRouteConnection”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-337">'New-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="b4d0c-338">”Set-AzExpressRouteConnection”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-338">'Set-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="b4d0c-339">”New-AzVirtualHubVnetConnection”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-339">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="b4d0c-340">”Update-AzVirtualHubVnetConnection”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-340">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="b4d0c-341">”New-AzVpnConnection”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-341">'New-AzVpnConnection'</span></span>
    - <span data-ttu-id="b4d0c-342">”Update-AzVpnConnection”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-342">'Update-AzVpnConnection'</span></span>
    - <span data-ttu-id="b4d0c-343">”New-AzP2sVpnGateway”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-343">'New-AzP2sVpnGateway'</span></span>
    - <span data-ttu-id="b4d0c-344">”Update-AzP2sVpnGateway”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-344">'Update-AzP2sVpnGateway'</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="b4d0c-345">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="b4d0c-345">Az.OperationalInsights</span></span>
* <span data-ttu-id="b4d0c-346">Fast fel PSWorkspace implementerar inte IOperationalInsightsWorkspace [#12135]</span><span class="sxs-lookup"><span data-stu-id="b4d0c-346">Fixed bug PSWorkspace doesn't implement IOperationalInsightsWorkspace [#12135]</span></span>
* <span data-ttu-id="b4d0c-347">”pergb2018” har lagts till i uppsättningen med giltiga värden för parametern ”Sku” i ”Set-AzOperationalInsightsWorkspace”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-347">Added 'pergb2018' to valid value set of parameter 'Sku' in 'Set-AzOperationalInsightsWorkspace'</span></span> 
* <span data-ttu-id="b4d0c-348">Alias ”FunctionParameters” lades till för parametern ”FunctionParameter” till</span><span class="sxs-lookup"><span data-stu-id="b4d0c-348">Added alias 'FunctionParameters' for parameter 'FunctionParameter' to</span></span>
    - <span data-ttu-id="b4d0c-349">”New-AzOperationalInsightsSavedSearch”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-349">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="b4d0c-350">”Set-AzOperationalInsightsSavedSearch”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-350">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b4d0c-351">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b4d0c-351">Az.RecoveryServices</span></span>
* <span data-ttu-id="b4d0c-352">Azure Backup har fått stöd för att hämta MAB-objekt.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-352">Azure Backup added support for fetching MAB items.</span></span>
* <span data-ttu-id="b4d0c-353">Azure Site Recovery stöder disktypen ”StandardSSD_LRS”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-353">Azure Site Recovery supports disk type 'StandardSSD_LRS'</span></span>

#### <a name="azresources"></a><span data-ttu-id="b4d0c-354">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b4d0c-354">Az.Resources</span></span>
* <span data-ttu-id="b4d0c-355">”UsageLocation”, ”GivenName”, ”Surname”, ”AccountEnabled”, ”MailNickname”, ”Mail” på ”PSADUser” lades till [#10526] [#10497]</span><span class="sxs-lookup"><span data-stu-id="b4d0c-355">Added 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' on 'PSADUser' [#10526] [#10497]</span></span>
* <span data-ttu-id="b4d0c-356">Problem med att ”-Mail” inte fungerar på ”Get-AzADUser” har åtgärdats [#11981]</span><span class="sxs-lookup"><span data-stu-id="b4d0c-356">Fixed issue that '-Mail' doesn't work on 'Get-AzADUser' [#11981]</span></span>
* <span data-ttu-id="b4d0c-357">Parametern ”-ExcludeChangeType” har lagts till i ”Get-AzDeploymentWhatIfResult” och ”Get-AzResourceGroupDeploymentWhatIfResult”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-357">Added '-ExcludeChangeType' parameter to 'Get-AzDeploymentWhatIfResult' and 'Get-AzResourceGroupDeploymentWhatIfResult'</span></span>
* <span data-ttu-id="b4d0c-358">Parametern ”-WhatIfExcludeChangeType” har lagts till i ”New-AzDeployment” och ”New-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-358">Added '-WhatIfExcludeChangeType' parameter to 'New-AzDeployment' and 'New-AzResourceGroupDeployment'</span></span>
* <span data-ttu-id="b4d0c-359">Cmdletar för ”Test-Az\*Deployment” har uppdaterats för att visa bättre felmeddelanden</span><span class="sxs-lookup"><span data-stu-id="b4d0c-359">Updated 'Test-Az\*Deployment' cmdlets to show better error messages</span></span>
* <span data-ttu-id="b4d0c-360">Hjälpmeddelandet för parametern ”-Name” i distributionsskapande och What If-cmdletar</span><span class="sxs-lookup"><span data-stu-id="b4d0c-360">Fixed help message for '-Name' parameter of deployment create and What-If cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="b4d0c-361">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b4d0c-361">Az.Sql</span></span>
* <span data-ttu-id="b4d0c-362">Stöd för tjänsthuvudnamn har lagts till för administratörs-cmdlet för SQL Server Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="b4d0c-362">Added support for service principal for Set SQL Server Azure Active Directory Admin cmdlet</span></span>
* <span data-ttu-id="b4d0c-363">Synkroniseringsproblem i Data Classification-cmdletar har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-363">Fixed sync issue in Data Classification cmdlets.</span></span>
* <span data-ttu-id="b4d0c-364">Stöd för att söka efter användare via e-postadress på ”Set-AzSqlServerActiveDirectoryAdministrator” [#12192]</span><span class="sxs-lookup"><span data-stu-id="b4d0c-364">Supported searching user by mail on 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b4d0c-365">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b4d0c-365">Az.Storage</span></span>
* <span data-ttu-id="b4d0c-366">Skapa lagringskonto med RequireInfrastructureEncryption stöds</span><span class="sxs-lookup"><span data-stu-id="b4d0c-366">Supported create Storage account with RequireInfrastructureEncryption</span></span>
    -  <span data-ttu-id="b4d0c-367">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="b4d0c-367">'New-AzStorageAccount'</span></span>
* <span data-ttu-id="b4d0c-368">Logiken för inläsning av Azure.Core flyttades till Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b4d0c-368">Moved the logic of loading Azure.Core to Az.Accounts</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b4d0c-369">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b4d0c-369">Az.Websites</span></span>
* <span data-ttu-id="b4d0c-370">Skydd för att ta bort skapad webapp om återställningen misslyckades har lagts till i ”Restore-AzDeletedWebApp”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-370">Added safeguard to delete created webapp if restore failed in 'Restore-AzDeletedWebApp'</span></span>
* <span data-ttu-id="b4d0c-371">”SourceWebApp.Location” har lagts till för ”New-AzWebApp” och ”New-AzWebAppSlot”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-371">Added 'SourceWebApp.Location' for 'New-AzWebApp' and 'New-AzWebAppSlot'</span></span>
* <span data-ttu-id="b4d0c-372">Fel som förhindrade ändring av containerinställningar i ”Set-AzWebApp” och ”Set-AzWebAppSlot” har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="b4d0c-372">Fixed bug that prevented changing Container settings in 'Set-AzWebApp' and 'Set-AzWebAppSlot'</span></span>
* <span data-ttu-id="b4d0c-373">Ett fel för att hämta SiteConfig när -Name inte anges för Get-AzWebApp har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="b4d0c-373">Fixed bug to get SiteConfig when -Name is not given for Get-AzWebApp</span></span>
* <span data-ttu-id="b4d0c-374">Stöd har lagts till för att skapa ASP för Linux-appar</span><span class="sxs-lookup"><span data-stu-id="b4d0c-374">Added a support to create ASP for Linux Apps</span></span>
* <span data-ttu-id="b4d0c-375">Undantag har lagts till för kloning över resursgrupper</span><span class="sxs-lookup"><span data-stu-id="b4d0c-375">Added exceptions for clone across resource groups</span></span>

## <a name="420---june-2020"></a><span data-ttu-id="b4d0c-376">4.2.0 – juni 2020</span><span class="sxs-lookup"><span data-stu-id="b4d0c-376">4.2.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b4d0c-377">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b4d0c-377">Az.Accounts</span></span>
* <span data-ttu-id="b4d0c-378">Åtgärdade ett problem som kan få Az att hoppa över loggar i Azure Automation- eller PowerShell-jobb [#11492]</span><span class="sxs-lookup"><span data-stu-id="b4d0c-378">Fixed an issue that may cause Az to skip logs in Azure Automation or PowerShell jobs [#11492]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="b4d0c-379">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="b4d0c-379">Az.AnalysisServices</span></span>
* <span data-ttu-id="b4d0c-380">Uppdaterad sammansättningsversion för dataplan-cmdletar</span><span class="sxs-lookup"><span data-stu-id="b4d0c-380">Updated assembly version of data plane cmdlets</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="b4d0c-381">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b4d0c-381">Az.ApiManagement</span></span>
* <span data-ttu-id="b4d0c-382">Uppdaterad sammansättningsversion för cmdletar för tjänsthantering</span><span class="sxs-lookup"><span data-stu-id="b4d0c-382">Updated assembly version of service management cmdlets</span></span>

#### <a name="azbilling"></a><span data-ttu-id="b4d0c-383">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="b4d0c-383">Az.Billing</span></span>
* <span data-ttu-id="b4d0c-384">Uppdaterad sammansättningsversion för förbrukningscmdletar</span><span class="sxs-lookup"><span data-stu-id="b4d0c-384">Updated assembly version of consumption cmdlets</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="b4d0c-385">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="b4d0c-385">Az.CognitiveServices</span></span>
* <span data-ttu-id="b4d0c-386">Stöd för PrivateEndpoint- och PublicNetworkAccess-kontroll.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-386">Support PrivateEndpoint and PublicNetworkAccess control.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="b4d0c-387">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b4d0c-387">Az.DataFactory</span></span>
* <span data-ttu-id="b4d0c-388">Uppdaterad sammansättningsversion för datafabrik V2-cmdletar</span><span class="sxs-lookup"><span data-stu-id="b4d0c-388">Updated assembly version of data factory V2 cmdlets</span></span>

#### <a name="azdatashare"></a><span data-ttu-id="b4d0c-389">Az.DataShare</span><span class="sxs-lookup"><span data-stu-id="b4d0c-389">Az.DataShare</span></span>
* <span data-ttu-id="b4d0c-390">Allmän tillgänglighet för modulen ”Az.DataShare”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-390">General availability of ''Az.DataShare'' module</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="b4d0c-391">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="b4d0c-391">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="b4d0c-392">Allmän tillgänglighet för modulen ”Az.DesktopVirtualization”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-392">General availability of ''Az.DesktopVirtualization'' module</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="b4d0c-393">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="b4d0c-393">Az.OperationalInsights</span></span>
* <span data-ttu-id="b4d0c-394">Uppgraderad SDK till 0.21.0</span><span class="sxs-lookup"><span data-stu-id="b4d0c-394">Upgraded SDK to 0.21.0</span></span>
* <span data-ttu-id="b4d0c-395">Lade till valfria parametrar till</span><span class="sxs-lookup"><span data-stu-id="b4d0c-395">Added optional parameters to</span></span> 
    - <span data-ttu-id="b4d0c-396">”New-AzOperationalInsightsSavedSearch”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-396">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="b4d0c-397">”Set-AzOperationalInsightsSavedSearch”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-397">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="b4d0c-398">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="b4d0c-398">Az.PolicyInsights</span></span>
* <span data-ttu-id="b4d0c-399">Korrigerade exempel 3 för ”Start-AzPolicyComplianceScan”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-399">Corrected example 3 for 'Start-AzPolicyComplianceScan'</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="b4d0c-400">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="b4d0c-400">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="b4d0c-401">Uppdaterad sammansättningsversion för PowerBI-cmdletar</span><span class="sxs-lookup"><span data-stu-id="b4d0c-401">Updated assembly version of PowerBI cmdlets</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="b4d0c-402">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="b4d0c-402">Az.PrivateDns</span></span>
* <span data-ttu-id="b4d0c-403">Korrigerade formatering av utförlig utdatasträng för Remove-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="b4d0c-403">Corrected verbose output string formatting for Remove-AzPrivateDnsRecordSet</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b4d0c-404">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b4d0c-404">Az.RecoveryServices</span></span>
* <span data-ttu-id="b4d0c-405">Azure Site Recovery-stöd för att skapa en återställningsplan för replikering mellan zoner från xml-indata.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-405">Azure Site Recovery support for creating recovery plan for zone to zone replication from xml input.</span></span>
* <span data-ttu-id="b4d0c-406">Uppdaterad sammansättningsversion för cmdletar för SiteRecovery och Backup</span><span class="sxs-lookup"><span data-stu-id="b4d0c-406">Updated assembly version of SiteRecovery and Backup cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="b4d0c-407">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b4d0c-407">Az.Resources</span></span>
* <span data-ttu-id="b4d0c-408">Lade till slutparameter för cmdletarna Get-AzDeploymentScriptLog och Save-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="b4d0c-408">Added Tail parameter to Get-AzDeploymentScriptLog and Save-AzDeploymentScriptLog cmdlets</span></span>
* <span data-ttu-id="b4d0c-409">Formaterad utdataegenskap så att den kan visas i cmdlet-utdata för Get-AzDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="b4d0c-409">Formatted Output property and show it on the Get-AzDeploymentScript cmdlet output</span></span>
* <span data-ttu-id="b4d0c-410">Bytte namn på parametern -DeploymentScriptInputObject till -DeploymentScriptObject</span><span class="sxs-lookup"><span data-stu-id="b4d0c-410">Renamed -DeploymentScriptInputObject parameter to -DeploymentScriptObject</span></span>
* <span data-ttu-id="b4d0c-411">Åtgärdade saknade fil/målnamn i cmdlet-meddelanden.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-411">Fixed missing file/target name in cmdlet messages.</span></span>
* <span data-ttu-id="b4d0c-412">Uppdaterad sammansättningsversion för cmdletar för resurshanterare och taggar</span><span class="sxs-lookup"><span data-stu-id="b4d0c-412">Updated assembly version of resource manager and tags cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="b4d0c-413">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b4d0c-413">Az.Sql</span></span>
* <span data-ttu-id="b4d0c-414">Lade till UsePrivateLinkConnection till ”New-AzSqlSyncGroup”, ”Update-AzSqlSyncGroup”, ”New-AzSqlSyncMember” och ”Update-AzSqlSyncMember”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-414">Added UsePrivateLinkConnection to 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="b4d0c-415">Lade till SyncMemberAzureDatabaseResourceId till ”New-AzSqlSyncMember” and ”Update-AzSqlSyncMember”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-415">Added SyncMemberAzureDatabaseResourceId to 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="b4d0c-416">Lade till stöd för att söka efter gästanvändare för att ange administratörs-cmdlet för SQL Server Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="b4d0c-416">Added Guest user lookup support to Set SQL Server Azure Active Directory Admin cmdlet</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b4d0c-417">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b4d0c-417">Az.Storage</span></span>
* <span data-ttu-id="b4d0c-418">Uppdaterad sammansättningsversion för dataplan-cmdletar</span><span class="sxs-lookup"><span data-stu-id="b4d0c-418">Updated assembly version of data plane cmdlets</span></span>

## <a name="410---may-2020"></a><span data-ttu-id="b4d0c-419">4.1.0 – maj 2020</span><span class="sxs-lookup"><span data-stu-id="b4d0c-419">4.1.0 - May 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="b4d0c-420">Höjdpunkter sedan den senaste uppdateringen</span><span class="sxs-lookup"><span data-stu-id="b4d0c-420">Highlights since the last release</span></span>
* <span data-ttu-id="b4d0c-421">PowerShell-versioner som stöds: Windows PowerShell 5.1, PowerShell Core 6.2.4+ och PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="b4d0c-421">Supported PowerShell versions: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>
* <span data-ttu-id="b4d0c-422">Allmän tillgänglighet för Az.Functions</span><span class="sxs-lookup"><span data-stu-id="b4d0c-422">General availability of Az.Functions</span></span> 
* <span data-ttu-id="b4d0c-423">Nya stora uppdateringar har gjorts för Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources och Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b4d0c-423">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources, and Az.Storage have major release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="b4d0c-424">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b4d0c-424">Az.Accounts</span></span>
* <span data-ttu-id="b4d0c-425">”Add-AzEnvironment” och ”Set-AzEnvironment” har uppdaterats med stöd för parametrarna ”AzureSynapseAnalyticsEndpointResourceId” och ”AzureSynapseAnalyticsEndpointSuffix”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-425">Updated 'Add-AzEnvironment' and 'Set-AzEnvironment' to accept parameters 'AzureSynapseAnalyticsEndpointResourceId' and 'AzureSynapseAnalyticsEndpointSuffix'</span></span>
* <span data-ttu-id="b4d0c-426">Azure.Core-relaterade sammansättningar har lagts till i Az.Accounts; PowerShell-plattformar som stöds är Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span><span class="sxs-lookup"><span data-stu-id="b4d0c-426">Added Azure.Core related assemblies into Az.Accounts, supported PowerShell platforms include Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span></span>

#### <a name="azaks"></a><span data-ttu-id="b4d0c-427">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="b4d0c-427">Az.Aks</span></span>
* <span data-ttu-id="b4d0c-428">API-versionen har uppgraderats till 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="b4d0c-428">Upgraded API Version to 2019-10-01</span></span>
* <span data-ttu-id="b4d0c-429">Stöds för att skapa AKS med hjälp av Windows-container</span><span class="sxs-lookup"><span data-stu-id="b4d0c-429">Supported to create AKS using Windows container</span></span>
* <span data-ttu-id="b4d0c-430">Nya cmdletar är tillgängliga: ”New-AzAksNodePool”, ”Update-AzAksNodePool”, ”Remove-AzAksNodePool”,        ”Get-AzAksNodePool”, ”Install-AzAksKubectl”, ”Get-AzAksVersion”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-430">Provided new cmdlets: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="b4d0c-431">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b4d0c-431">Az.ApiManagement</span></span>
* <span data-ttu-id="b4d0c-432">Parametrarna ”New-AzApiManagement” och ”Set-AzApiManagement”: [-AssignIdentity] har bytt namn till [-SystemAssignedIdentity]</span><span class="sxs-lookup"><span data-stu-id="b4d0c-432">'New-AzApiManagement' and 'Set-AzApiManagement': [-AssignIdentity] parameter renamed as [-SystemAssignedIdentity]</span></span>
* <span data-ttu-id="b4d0c-433">”New-AzApiManagement” och ”Set-AzApiManagement”: En ny parameter har lagts till: [-UserAssignedIdentity <String[]>]</span><span class="sxs-lookup"><span data-stu-id="b4d0c-433">'New-AzApiManagement' and 'Set-AzApiManagement': New parameter added: [-UserAssignedIdentity <String[]>]</span></span>
* <span data-ttu-id="b4d0c-434">”Get-AzApiManagementProperty” har bytt namn till ”Get-AzApiManagementNamedValue”.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-434">'Get-AzApiManagementProperty': renamed as 'Get-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="b4d0c-435">PropertyId-parametern har bytt namn till NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-435">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="b4d0c-436">”New-AzApiManagementProperty” har bytt namn till ”New-AzApiManagementNamedValue”.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-436">'New-AzApiManagementProperty': renamed as 'New-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="b4d0c-437">PropertyId-parametern har bytt namn till NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-437">PropertyId parameter renamed as NamedValueId.</span></span> 
* <span data-ttu-id="b4d0c-438">”Set-AzApiManagementProperty” har bytt namn till ”Set-AzApiManagementNamedValue”.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-438">'Set-AzApiManagementProperty': renamed as 'Set-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="b4d0c-439">PropertyId-parametern har bytt namn till NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-439">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="b4d0c-440">”Remove-AzApiManagementProperty” har bytt namn till ”Remove-AzApiManagementNamedValue”.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-440">'Remove-AzApiManagementProperty': renamed as 'Remove-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="b4d0c-441">PropertyId-parametern har bytt namn till NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-441">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="b4d0c-442">Den nya cmdleten Get-AzApiManagementAuthorizationServerClientSecret gör att ”Get-AzApiManagementAuthorizationServer” inte längre returnerar klienthemligheter.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-442">Added new 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet and 'Get-AzApiManagementAuthorizationServer' will not return client secret anymore.</span></span>
* <span data-ttu-id="b4d0c-443">Den nya cmdleten ”Get-AzApiManagementNamedValueSecretValue” gör att ”Get-AzApiManagementNamedValue” inte returnerar värdet för en hemlighet.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-443">Added new 'Get-AzApiManagementNamedValueSecretValue' cmdlet and 'Get-AzApiManagementNamedValue' will not return secret value.</span></span>
* <span data-ttu-id="b4d0c-444">Den nya cmdleten ”Get-AzApiManagementOpenIdConnectProviderClientSecret” gör att ”Get-AzApiManagementOpenIdConnectProvider” inte längre returnerar klienthemligheter.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-444">Added new 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet and 'Get-AzApiManagementOpenIdConnectProvider' will not return client secret anymore.</span></span>
* <span data-ttu-id="b4d0c-445">Den nya cmdleten ”Get-AzApiManagementSubscriptionKey” gör att ”Get-AzApiManagementSubscription” inte längre returnerar prenumerationsnycklar.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-445">Added new 'Get-AzApiManagementSubscriptionKey' cmdlet and 'Get-AzApiManagementSubscription' will not return subscription keys anymore.</span></span>
* <span data-ttu-id="b4d0c-446">Den nya cmdleten ”Get-AzApiManagementTenantAccessSecret” gör att ”Get-AzApiManagementTenantAccess” inte längre returnerar nycklar.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-446">Added new 'Get-AzApiManagementTenantAccessSecret' cmdlet and 'Get-AzApiManagementTenantAccess' will not return keys anymore.</span></span>
* <span data-ttu-id="b4d0c-447">Den nya cmdleten ”Get-AzApiManagementTenantGitAccessSecret” gör att ”Get-AzApiManagementTenantGitAccess” inte längre returnerar nycklar.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-447">Added new 'Get-AzApiManagementTenantGitAccessSecret' cmdlet and 'Get-AzApiManagementTenantGitAccess' will not return keys anymore.</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="b4d0c-448">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="b4d0c-448">Az.ApplicationInsights</span></span>
* <span data-ttu-id="b4d0c-449">Tillagda parametrar: ”RetentionInDays” ”PublicNetworkAccessForIngestion” ”PublicNetworkAccessForQuery” för ”New-AzApplicationInsights”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-449">Added Parameters: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span></span>
* <span data-ttu-id="b4d0c-450">Cmdleten ”Update-AzApplicationInsights” har skapats</span><span class="sxs-lookup"><span data-stu-id="b4d0c-450">Created cmdlet 'Update-AzApplicationInsights'</span></span>
* <span data-ttu-id="b4d0c-451">Cmdletar har skapats för länkat lagringskonto</span><span class="sxs-lookup"><span data-stu-id="b4d0c-451">Created cmdlets for Linked Storage Account</span></span>

#### <a name="azbatch"></a><span data-ttu-id="b4d0c-452">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="b4d0c-452">Az.Batch</span></span>
* <span data-ttu-id="b4d0c-453">Az.Batch har uppdaterats att använda ”Microsoft.Azure.Batch” SDK version 13.0.0 och ”Microsoft.Azure.Management.Batch” SDK version 9.0.0.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-453">Updated Az.Batch to use 'Microsoft.Azure.Batch' SDK version 13.0.0 and 'Microsoft.Azure.Management.Batch' SDK version 9.0.0.</span></span>
* <span data-ttu-id="b4d0c-454">Nu kan du välja vilken typ av certifikat du lägger till genom att använda den nya parametern ”-CertificateKind” med ”New-AzBatchCertificate”.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-454">Added the ability to select the kind of certificate being added using the new '-CertificateKind' parameter to 'New-AzBatchCertificate'.</span></span>
* <span data-ttu-id="b4d0c-455">Egenskapen ”ApplicationPackages” har tagits bort från ”PSApplication”, som tidigare alltid var ''.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-455">Removed 'ApplicationPackages' property from 'PSApplication' which was previously always ''.</span></span>
  - <span data-ttu-id="b4d0c-456">Specifika paket i ett program kan nu hämtas med hjälp av ”Get-AzBatchApplicationPackage”.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-456">The specific packages inside of an application now can be retrieved using 'Get-AzBatchApplicationPackage'.</span></span> <span data-ttu-id="b4d0c-457">Ett exempel: ”Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication”.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-457">For example: 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span></span>
* <span data-ttu-id="b4d0c-458">Nu när du skapar en pool med hjälp av ”New-AzBatchPool” kan egenskapen ”VirtualMachineImageId” för ”PSImageReference” endast referera till en Shared Image Gallery-avbildning.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-458">When creating a pool using 'New-AzBatchPool', the 'VirtualMachineImageId' property of 'PSImageReference' can now only refer to a Shared Image Gallery image.</span></span>
* <span data-ttu-id="b4d0c-459">När du skapar en pool med hjälp av ”New-AzBatchPool” kan poolen etableras utan en offentlig IP-adress med hjälp av den nya egenskapen ”PublicIPAddressConfiguration” för ”PSNetworkConfiguration”.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-459">When creating a pool using 'New-AzBatchPool', the pool can be provisioned without a public IP using the new 'PublicIPAddressConfiguration' property of 'PSNetworkConfiguration'.</span></span>
  - <span data-ttu-id="b4d0c-460">Egenskapen ”PublicIPs” för ”PSNetworkConfiguration” har också flyttats till ”PSPublicIPAddressConfiguration”.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-460">The 'PublicIPs' property of 'PSNetworkConfiguration' has moved in to 'PSPublicIPAddressConfiguration' as well.</span></span> <span data-ttu-id="b4d0c-461">Den här egenskapen kan bara anges om ”IPAddressProvisioningType” är ”UserManaged”.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-461">This property can only be specified if 'IPAddressProvisioningType' is 'UserManaged'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b4d0c-462">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b4d0c-462">Az.Compute</span></span>
* <span data-ttu-id="b4d0c-463">Parametern HostId har lagts till för cmdleten ”Update-AzVM”t</span><span class="sxs-lookup"><span data-stu-id="b4d0c-463">Added HostId parameter to 'Update-AzVM' cmdlet</span></span>
* <span data-ttu-id="b4d0c-464">Hjälpdokumenten har uppdaterats för cmdletarna ”New-AzVMConfig”, ”New-AzVmssConfig”, ”Update-AzVmss”, ”Set-AzVMOperatingSystem” och ”Set-AzVmssOsProfile”.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-464">Updated Help documents for 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' and 'Set-AzVmssOsProfile' cmdlets.</span></span>
* <span data-ttu-id="b4d0c-465">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="b4d0c-465">Breaking changes</span></span>
    - <span data-ttu-id="b4d0c-466">Parametern FilterExpression tas bort från cmdleten ”Get-AzVMImage”.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-466">FilterExpression parameter is removed from 'Get-AzVMImage' cmdlet.</span></span>
    - <span data-ttu-id="b4d0c-467">Parametern AssignIdentity tas bort från cmdletarna ”New-AzVmssConfig”, ”New-AzVMConfig” och ”Update-AzVM”.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-467">AssignIdentity parameter is removed from 'New-AzVmssConfig', 'New-AzVMConfig' and 'Update-AzVM' cmdlets.</span></span>
    - <span data-ttu-id="b4d0c-468">AutomaticRepairMaxInstanceRepairsPercent tas bort från cmdletarna ”New-AzVmssConfig” och ”Update-AzVmss”.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-468">AutomaticRepairMaxInstanceRepairsPercent is removed from 'New-AzVmssConfig' and 'Update-AzVmss' cmdlets.</span></span>
    - <span data-ttu-id="b4d0c-469">Egenskaperna AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus och VirtualMachineScaleSetsColocationStatus tas bort från ProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-469">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus and VirtualMachineScaleSetsColocationStatus properties are removed from ProximityPlacementGroup.</span></span>
    - <span data-ttu-id="b4d0c-470">Egenskapen MaxInstanceRepairsPercent tas bort från AutomaticRepairsPolicy.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-470">MaxInstanceRepairsPercent property is removed from AutomaticRepairsPolicy.</span></span>
    - <span data-ttu-id="b4d0c-471">Typerna AvailabilitySets, VirtualMachines och VirtualMachineScaleSets ändras från IList<SubResource> till IList<SubResourceWithColocationStatus>.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-471">The types of AvailabilitySets, VirtualMachines and VirtualMachineScaleSets are changed from IList<SubResource> to IList<SubResourceWithColocationStatus>.</span></span>
* <span data-ttu-id="b4d0c-472">Beskrivningen för cmdleten ”Get-AzVM” har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-472">Description for 'Get-AzVM' cmdlet has been updated to better describe it.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="b4d0c-473">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b4d0c-473">Az.DataFactory</span></span>
* <span data-ttu-id="b4d0c-474">CRUD-stöd för egenskaper för dataflödeskörning  i hanterad IR.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-474">Supported CRUD of data flow runtime properties in Managed IR.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="b4d0c-475">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="b4d0c-475">Az.FrontDoor</span></span>
* <span data-ttu-id="b4d0c-476">Nya cmdletar har lagts till för att skapa, uppdatera, hämta och ta bort (CRUD) Front Door-regelmotorobjekt</span><span class="sxs-lookup"><span data-stu-id="b4d0c-476">Added new cmdlets for creation, update, retreival, and deletion of Front Door Rules Engine object</span></span>
* <span data-ttu-id="b4d0c-477">Hjälp-cmdletar har lagts till för konstruktion av Front Door-regelmotorobjekt</span><span class="sxs-lookup"><span data-stu-id="b4d0c-477">Added helper cmdlets for construction of Front Door Rules Engine object</span></span>
* <span data-ttu-id="b4d0c-478">Regelmotorreferens har lagts till för Front Door-hanteringsregelobjekt.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-478">Added Rules Engine reference to Front Door Routing Rule object.</span></span>
* <span data-ttu-id="b4d0c-479">Parametrar för Private Link har lagts till för Front Door-serverdelsobjekt</span><span class="sxs-lookup"><span data-stu-id="b4d0c-479">Added Private Link parameters to Front Door Backend object</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="b4d0c-480">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="b4d0c-480">Az.Functions</span></span>
* <span data-ttu-id="b4d0c-481">Allmän tillgänglighet för ”Az.Functions”-modulen</span><span class="sxs-lookup"><span data-stu-id="b4d0c-481">General availability of ''Az.Functions'' module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="b4d0c-482">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="b4d0c-482">Az.HDInsight</span></span>
* <span data-ttu-id="b4d0c-483">Stöd för diskkryptering med kundhanterad nyckel.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-483">Supported Customer-managed key disk encryption.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="b4d0c-484">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="b4d0c-484">Az.HealthcareApis</span></span>
* <span data-ttu-id="b4d0c-485">Åtkomstprinciper använder inte längre det aktiva huvudkontot som standard</span><span class="sxs-lookup"><span data-stu-id="b4d0c-485">Access policies are no longer defaulted to the current principal</span></span>

#### <a name="aziothub"></a><span data-ttu-id="b4d0c-486">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="b4d0c-486">Az.IotHub</span></span>
* <span data-ttu-id="b4d0c-487">En cmdlet har lagts till som anropar en fråga i en IoT-hubb för att hämta information med ett SQL-liknande språk.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-487">Added cmdlet to invoke a query in an IoT hub to retrieve information using a SQL-like language.</span></span>
* <span data-ttu-id="b4d0c-488">Problemet som gjorde att ”Add-AzIotHubDevice” inte skapade en Edge-aktiverad enhet utan underordnade enheter har åtgärdats [#11597]</span><span class="sxs-lookup"><span data-stu-id="b4d0c-488">Fix issue that 'Add-AzIotHubDevice' fails to create Edge Enabled Device without child devices [#11597]</span></span>
* <span data-ttu-id="b4d0c-489">En cmdlet har lagts till för att generera SAS-token för en Iot-hubb, enhet eller modul.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-489">Added cmdlet to generate SAS token for Iot Hub, device or module.</span></span>
* <span data-ttu-id="b4d0c-490">En cmdlet har lagts till för att anropa en måttfråga om konfiguration.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-490">Added cmdlet to invoke configuration metrics query.</span></span>
* <span data-ttu-id="b4d0c-491">Hantera automatisk distribution av IoT Edge i stor skala.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-491">Manage IoT Edge automatic deployment at scale.</span></span> <span data-ttu-id="b4d0c-492">Nya cmdlet:ar är:</span><span class="sxs-lookup"><span data-stu-id="b4d0c-492">New cmdlets are:</span></span>
    - <span data-ttu-id="b4d0c-493">”Add-AzIotHubDeployment”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-493">'Add-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="b4d0c-494">”Get-AzIotHubDeployment”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-494">'Get-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="b4d0c-495">”Remove-AzIotHubDeployment”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-495">'Remove-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="b4d0c-496">”Set-AzIotHubDeployment”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-496">'Set-AzIotHubDeployment'</span></span>
* <span data-ttu-id="b4d0c-497">En cmdlet har lagts till för att anropa en måttfråga om IoT Edge-distribution.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-497">Added cmdlet to invoke an IoT Edge deployment metrics query.</span></span>
* <span data-ttu-id="b4d0c-498">En cmdlet har lagts till för att tillämpa konfigurationsinnehåll på den angivna gränsenheten.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-498">Added cmdlet to apply the configuration content to the specified edge device.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="b4d0c-499">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b4d0c-499">Az.KeyVault</span></span>
* <span data-ttu-id="b4d0c-500">Två alias har tagits bort: ”New-AzKeyVaultCertificateAdministratorDetails” och ”New-AzKeyVaultCertificateOrganizationDetails”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-500">Removed two aliases: 'New-AzKeyVaultCertificateAdministratorDetails' and 'New-AzKeyVaultCertificateOrganizationDetails'</span></span>
* <span data-ttu-id="b4d0c-501">Nu är mjuk borttagning aktiverat som standard när ett nyckelvalv skapas</span><span class="sxs-lookup"><span data-stu-id="b4d0c-501">Enabled soft delete by default when creating a key vault</span></span>
* <span data-ttu-id="b4d0c-502">Nätverksregler kan ställas in för att styra åtkomsten från särskilda nätverksplatser när du skapar ett nyckelvalv</span><span class="sxs-lookup"><span data-stu-id="b4d0c-502">Network rules can be set to govern the accessibility from specific network locations when creating a key vault</span></span>
* <span data-ttu-id="b4d0c-503">Stöd för BYOK (Bring Your Own Key) har lagts till</span><span class="sxs-lookup"><span data-stu-id="b4d0c-503">Added support to bring your own key (BYOK)</span></span>
    - <span data-ttu-id="b4d0c-504">”Add-AzKeyVaultKey” stöder generering av en KeyExchange-nyckel</span><span class="sxs-lookup"><span data-stu-id="b4d0c-504">'Add-AzKeyVaultKey' supports generating a key exchange key</span></span>
    - <span data-ttu-id="b4d0c-505">”Get-AzKeyVaultKey” stöder nedladdning av en offentlig nyckel i PEM-format</span><span class="sxs-lookup"><span data-stu-id="b4d0c-505">'Get-AzKeyVaultKey' supports downloading a public key in PEM format</span></span>
* <span data-ttu-id="b4d0c-506">”KeyOps”-delen av hjälpdokumentet för ”Add-AzKeyVaultKey” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="b4d0c-506">Updated the 'KeyOps' part of the help document of 'Add-AzKeyVaultKey'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="b4d0c-507">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b4d0c-507">Az.Monitor</span></span>
* <span data-ttu-id="b4d0c-508">Bugg för ”Set-AzDiagnosticSettings” har åtgärdats; kvarhållningsprincipen tillämpas inte på alla kategorier [#11589]</span><span class="sxs-lookup"><span data-stu-id="b4d0c-508">Fixed bug for 'Set-AzDiagnosticSettings', retention policy won't apply to all categories [#11589]</span></span>
* <span data-ttu-id="b4d0c-509">Stöd för WebTest-tillgänglighetskriterier för måttavisering V2</span><span class="sxs-lookup"><span data-stu-id="b4d0c-509">Supported WebTest availability criteria for metric alert V2</span></span>
    - <span data-ttu-id="b4d0c-510">”New-AzMetricAlertRuleV2Criteria”: ett alternativ för att skapa tillgänglighetskriterier för webbtest har lagts till</span><span class="sxs-lookup"><span data-stu-id="b4d0c-510">'New-AzMetricAlertRuleV2Criteria': an option to create webtest availability criteria was added</span></span>
    - <span data-ttu-id="b4d0c-511">”Add-AzMetricAlertRuleV2”: stöd för de nya tillgänglighetskriterierna för webbtest</span><span class="sxs-lookup"><span data-stu-id="b4d0c-511">'Add-AzMetricAlertRuleV2': supports the new webtest availability criteria</span></span>
* <span data-ttu-id="b4d0c-512">Redundant definition har tagits bort för RetentionPolicy i PSLogProfile [#7608]</span><span class="sxs-lookup"><span data-stu-id="b4d0c-512">Removed redundant definition for RetentionPolicy in PSLogProfile [#7608]</span></span>
* <span data-ttu-id="b4d0c-513">Redundanta egenskaper som definierats i PSEventData har tagits bort [#11353]</span><span class="sxs-lookup"><span data-stu-id="b4d0c-513">Removed redundant properties difined in PSEventData [#11353]</span></span>
* <span data-ttu-id="b4d0c-514">”Get-AzLog” har bytt namn till ”Get-AzActivityLog”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-514">Renamed 'Get-AzLog' to 'Get-AzActivityLog'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b4d0c-515">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b4d0c-515">Az.Network</span></span>
* <span data-ttu-id="b4d0c-516">Attribut för icke-bakåtkompatibel ändring har lagts till för att meddela att standardbeteendet för zoner kommer att ändras</span><span class="sxs-lookup"><span data-stu-id="b4d0c-516">Added breaking change attribute to notify that Zone default behaviour will be changed</span></span>
    - <span data-ttu-id="b4d0c-517">”New-AzPublicIpAddress”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-517">'New-AzPublicIpAddress'</span></span>
    - <span data-ttu-id="b4d0c-518">”New-AzPublicIpPrefix”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-518">'New-AzPublicIpPrefix'</span></span>
    - <span data-ttu-id="b4d0c-519">”New-AzLoadBalancerFrontendIpConfig”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-519">'New-AzLoadBalancerFrontendIpConfig'</span></span>
* <span data-ttu-id="b4d0c-520">Stöd har lagts till för en ny resurs på den översta nivån, SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="b4d0c-520">Added support for a new top level resource SecurityPartnerProvider</span></span>
    - <span data-ttu-id="b4d0c-521">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="b4d0c-521">New cmdlets added:</span></span>
        - <span data-ttu-id="b4d0c-522">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="b4d0c-522">New-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="b4d0c-523">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="b4d0c-523">Remove-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="b4d0c-524">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="b4d0c-524">Get-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="b4d0c-525">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="b4d0c-525">Set-AzSecurityPartnerProvider</span></span>
* <span data-ttu-id="b4d0c-526">”RequiredZoneNames” har lagts till för ”PSPrivateLinkResource” och ”GroupId” för ”PSPrivateEndpointConnection”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-526">Added 'RequiredZoneNames' on 'PSPrivateLinkResource' and 'GroupId' on 'PSPrivateEndpointConnection'</span></span>
* <span data-ttu-id="b4d0c-527">Fel parametertyp för SuccessThresholdRoundTripTimeMs-parametern för New-AzNetworkWatcherConnectionMonitorTestConfigurationObject har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="b4d0c-527">Fixed incorrect type of SuccessThresholdRoundTripTimeMs parameter for New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>
* <span data-ttu-id="b4d0c-528">VirtualWan-cmdletar har uppdaterats för att ange AllowVnetToVnetTraffic-argumentets standardvärde till True.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-528">Updated VirtualWan cmdlets to set default value of AllowVnetToVnetTraffic argument to True.</span></span>
    - <span data-ttu-id="b4d0c-529">”New-AzVirtualWan”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-529">'New-AzVirtualWan'</span></span>
    - <span data-ttu-id="b4d0c-530">”Update-AzVirtualWan”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-530">'Update-AzVirtualWan'</span></span>
* <span data-ttu-id="b4d0c-531">Nya cmdletar har lagts till för att stödja DNS-zongrupp för privat slutpunkt</span><span class="sxs-lookup"><span data-stu-id="b4d0c-531">Added new cmdlets to support DNS zone group for private endpoint</span></span>
    - <span data-ttu-id="b4d0c-532">”New-AzPrivateDnsZoneConfig”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-532">'New-AzPrivateDnsZoneConfig'</span></span>
    - <span data-ttu-id="b4d0c-533">”Get-AzPrivateDnsZoneGroup”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-533">'Get-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="b4d0c-534">”New-AzPrivateDnsZoneGroup”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-534">'New-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="b4d0c-535">”Set-AzPrivateDnsZoneGroup”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-535">'Set-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="b4d0c-536">”Remove-AzPrivateDnsZoneGroup”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-536">'Remove-AzPrivateDnsZoneGroup'</span></span>
* <span data-ttu-id="b4d0c-537">Parametrarna ”DNSEnableProxy”, ”DNSRequireProxyForNetworkRules” och ”DNSServers” har lagts till för ”AzureFirewall”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-537">Added 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' and 'DNSServers' parameters to 'AzureFirewall'</span></span>
* <span data-ttu-id="b4d0c-538">Parametrarna ”EnableDnsProxy”, ”DnsProxyNotRequiredForNetworkRule” och ”DnsServer” har lagts till för ”AzureFirewall”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-538">Added 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' and 'DnsServer' parameters to 'AzureFirewall'</span></span>
    - <span data-ttu-id="b4d0c-539">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="b4d0c-539">Updated cmdlet:</span></span>
        - <span data-ttu-id="b4d0c-540">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="b4d0c-540">New-AzFirewall</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="b4d0c-541">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="b4d0c-541">Az.OperationalInsights</span></span>
* <span data-ttu-id="b4d0c-542">Äldre kod har uppdaterats för att tillämpa ny genererad SDK</span><span class="sxs-lookup"><span data-stu-id="b4d0c-542">Updated legacy code to apply new generated SDK</span></span>
* <span data-ttu-id="b4d0c-543">Cmdletar har tagits bort på grund av föråldrade API:er</span><span class="sxs-lookup"><span data-stu-id="b4d0c-543">Deleted cmdlets due to deprecated APIs</span></span>
    - <span data-ttu-id="b4d0c-544">”Get-AzOperationalInsightsSavedSearchResult” (alias ”Get-AzOperationalInsightsSavedSearchResults”)</span><span class="sxs-lookup"><span data-stu-id="b4d0c-544">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span></span>
    - <span data-ttu-id="b4d0c-545">”Get-AzOperationalInsightsSearchResult” (alias ”Get-AzOperationalInsightsSearchResults”)</span><span class="sxs-lookup"><span data-stu-id="b4d0c-545">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span></span>
    - <span data-ttu-id="b4d0c-546">”Get-AzOperationalInsightsLinkTarget” (alias ”Get-AzOperationalInsightsLinkTargets”)</span><span class="sxs-lookup"><span data-stu-id="b4d0c-546">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span></span>
* <span data-ttu-id="b4d0c-547">Parametrar har lagts till för ”Set-AzOperationalInsightsWorkspace” och ”New-AzOperationalInsightsWorkspace”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-547">Added parameters for 'Set-AzOperationalInsightsWorkspace' and 'New-AzOperationalInsightsWorkspace'</span></span>
* <span data-ttu-id="b4d0c-548">Cmdletar har skapats för länkat lagringskonto</span><span class="sxs-lookup"><span data-stu-id="b4d0c-548">Created cmdlets for Linked Stoarge Account</span></span>
* <span data-ttu-id="b4d0c-549">Cmdletar har skapats för kluster och länkad tjänst</span><span class="sxs-lookup"><span data-stu-id="b4d0c-549">Created cmdlets for Clusters and Linked Service</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b4d0c-550">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b4d0c-550">Az.RecoveryServices</span></span>
* <span data-ttu-id="b4d0c-551">Azure Site Recovery: Stöd har lagts till för att skydda VM-närhetsplaceringsgrupper för Azure till Azure-provider.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-551">Azure Site Recovery added support for protecting proximity placement group virtual machines for Azure to Azure provider.</span></span>
* <span data-ttu-id="b4d0c-552">Azure Site Recovery: Stöd har lagts till för replikering mellan zoner.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-552">Azure Site Recovery added support for zone to zone replication.</span></span>
* <span data-ttu-id="b4d0c-553">Azure Backup: Stöd har lagts till för långsiktig kvarhållning för Azure FileShare-återställningspunkter.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-553">Azure Backup Added Long term retention support for Azure FileShare Recovery Points.</span></span>
* <span data-ttu-id="b4d0c-554">Azure Backup: Egenskaper för diskexkludering har lagts till för cmdlet-utdata från ”Get-AzRecoveryServicesBackupItem”.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-554">Azure Backup Added disk exclusion properties to 'Get-AzRecoveryServicesBackupItem' cmdlet output.</span></span>
* <span data-ttu-id="b4d0c-555">En privat slutpunkt har lagts till för filen med valvets autentiseringsuppgifter för Site Recovery-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-555">Added private endpoint for Vault credential file for site recovery service.</span></span>

#### <a name="azresources"></a><span data-ttu-id="b4d0c-556">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b4d0c-556">Az.Resources</span></span>
* <span data-ttu-id="b4d0c-557">En varning har lagts till om visningsfördröjning när en ny rolldefinition skapas</span><span class="sxs-lookup"><span data-stu-id="b4d0c-557">Added message warning about view delay when creating a new Role Definition</span></span>
* <span data-ttu-id="b4d0c-558">Princip-cmdletar har ändrats för utmatning av starkt typifierade objekt</span><span class="sxs-lookup"><span data-stu-id="b4d0c-558">Changed policy cmdlets to output strongly-typed objects</span></span>
* <span data-ttu-id="b4d0c-559">Parametern ”-TenantLevel” har tagits bort för användning med ”Get-AzResourceLock” [#11335]</span><span class="sxs-lookup"><span data-stu-id="b4d0c-559">Removed '-TenantLevel' parameter used for on the 'Get-AzResourceLock' cmdlet [#11335]</span></span>
* <span data-ttu-id="b4d0c-560">”Remove-AzResourceGroup -Id ResourceId” har åtgärdats [#9882]</span><span class="sxs-lookup"><span data-stu-id="b4d0c-560">Fixed 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span></span>
* <span data-ttu-id="b4d0c-561">En ny cmdlet har lagts till för att hämta What-If-resultat för ARM-mallar i omfånget för resursgrupper: ”Get-AzDeploymentResourceGroupWhatIfResult”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-561">Added new cmdlet for getting ARM template What-If results at resource group scope: 'Get-AzDeploymentResourceGroupWhatIfResult'</span></span>
* <span data-ttu-id="b4d0c-562">En ny cmdlet har lagts till för att hämta What-If-resultat för ARM-mallar i prenumerationsomfånget: ”Get-AzDeploymentWhatIfResult”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-562">Added new cmdlet for getting ARM template What-If results at subscription scope: 'Get-AzDeploymentWhatIfResult'</span></span>
   - <span data-ttu-id="b4d0c-563">Alias: ”Get-AzSubscriptionDeploymentWhatIf”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-563">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span></span>
* <span data-ttu-id="b4d0c-564">Parametrarna ”-WhatIf” och ”-Confirm” har åsidosatts för ”New-AzDeployment” och ”New-AzResourceGroupDeployment” för att använda What-If-resultat för ARM-mallar</span><span class="sxs-lookup"><span data-stu-id="b4d0c-564">Overrode '-WhatIf' and '-Confirm' parameters for 'New-AzDeployment' and 'New-AzResourceGroupDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="b4d0c-565">Ett utfasningsmeddelande har lagts till för parametern ”ApiVersion” i distributions-cmdletar</span><span class="sxs-lookup"><span data-stu-id="b4d0c-565">Added deprecation message for 'ApiVersion' parameter in deployment cmdlets</span></span>
* <span data-ttu-id="b4d0c-566">En funktion har lagts till för att visa förbättrade felmeddelanden för distributionsfel</span><span class="sxs-lookup"><span data-stu-id="b4d0c-566">Added capability to show improved error messages for deployment failures</span></span>
* <span data-ttu-id="b4d0c-567">CorrelationId-loggning har lagts till för distributionsfel</span><span class="sxs-lookup"><span data-stu-id="b4d0c-567">Added correlationId logging for deployment failures</span></span>
* <span data-ttu-id="b4d0c-568">Egenskapen ”error” har lagts till i utdata från distributionsskript</span><span class="sxs-lookup"><span data-stu-id="b4d0c-568">Added 'error' property to the deployment script output</span></span>
* <span data-ttu-id="b4d0c-569">Nuget Microsoft.Azure.Management.ResourceManager har uppdaterats till ”3.7.1-preview”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-569">Updated nuget Microsoft.Azure.Management.ResourceManager to '3.7.1-preview'</span></span>
* <span data-ttu-id="b4d0c-570">Specifika testfall har tagits bort då egenskapen Error i DeploymentValidateResult har ändrats till lässkyddad från nuget 3.7.1-preview</span><span class="sxs-lookup"><span data-stu-id="b4d0c-570">Removed specific test cases as Error property in DeploymentValidateResult has changed to readonly from nuget 3.7.1-preview</span></span>
* <span data-ttu-id="b4d0c-571">GenericResourceExpanded har flyttats från SDK ResourceManager 3.7.1-preview</span><span class="sxs-lookup"><span data-stu-id="b4d0c-571">Brought GenericResourceExpanded from SDK ResourceManager 3.7.1-preview</span></span>
* <span data-ttu-id="b4d0c-572">Stöd för taggar har lagts till för alla Get-cmdletar för distribution, samt</span><span class="sxs-lookup"><span data-stu-id="b4d0c-572">Added tag support for all Get cmdlets for deployment, as well as</span></span>
    - <span data-ttu-id="b4d0c-573">”New-AzDeployment”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-573">'New-AzDeployment'</span></span>
    - <span data-ttu-id="b4d0c-574">”New-AzManagementGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-574">'New-AzManagementGroupDeployment'</span></span>
    - <span data-ttu-id="b4d0c-575">”New-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-575">'New-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="b4d0c-576">”New-AzTenantDeployment”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-576">'New-AzTenantDeployment'</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="b4d0c-577">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b4d0c-577">Az.ServiceFabric</span></span>
* <span data-ttu-id="b4d0c-578">En bugg har åtgärdats som gjorde att --SecretIdentifier fick fel tumavtryck för certifikat när ett certifikat lades till</span><span class="sxs-lookup"><span data-stu-id="b4d0c-578">Fixed bug in add certificate using --SecretIdentifier that was getting the wrong certificate thumbprint</span></span>

#### <a name="azsql"></a><span data-ttu-id="b4d0c-579">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b4d0c-579">Az.Sql</span></span>
* <span data-ttu-id="b4d0c-580">Förbättrade prestanda för:</span><span class="sxs-lookup"><span data-stu-id="b4d0c-580">Enhance performance of:</span></span>
    - <span data-ttu-id="b4d0c-581">”Set-AzSqlDatabaseSensitivityClassification”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-581">'Set-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="b4d0c-582">”Set-AzSqlInstanceDatabaseSensitivityClassification”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-582">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="b4d0c-583">”Remove-AzSqlDatabaseSensitivityClassification”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-583">'Remove-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="b4d0c-584">”Remove-AzSqlInstanceDatabaseSensitivityClassification”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-584">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="b4d0c-585">”Enable-AzSqlDatabaseSensitivityRecommendation”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-585">'Enable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="b4d0c-586">”Enable-AzSqlInstanceDatabaseSensitivityRecommendation”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-586">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="b4d0c-587">”Disable-AzSqlDatabaseSensitivityRecommendation”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-587">'Disable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="b4d0c-588">”Disable-AzSqlInstanceDatabaseSensitivityRecommendation”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-588">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
* <span data-ttu-id="b4d0c-589">Validering på klientsidan har tagits bort för parametern ”RetentionDays” från cmdleten ”Set-AzSqlDatabaseBackupShortTermRetentionPolicy”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-589">Removed client-side validation of 'RetentionDays' parameter from cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span>
* <span data-ttu-id="b4d0c-590">Granskning av ett lagringskonto i Vnet; en bugg har åtgärdats som orsakade fel när en Storage Blob Data-deltagarroll skapades.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-590">Auditing to a storage account in Vnet, fixing a bug when creating a Storage Blob Data Contributor role.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b4d0c-591">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b4d0c-591">Az.Storage</span></span>
* <span data-ttu-id="b4d0c-592">”-AsJob” har lagts till för att hämta/lista konto med cmdleten ”Get-AzStorageAccount”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-592">Added '-AsJob' to get/list account cmdlet 'Get-AzStorageAccount'</span></span>
* <span data-ttu-id="b4d0c-593">Gör KeyVersion valfri när lagringskontot uppdateras med KeyvaultEncryption, för att ge stöd för automatisk nyckelrotation</span><span class="sxs-lookup"><span data-stu-id="b4d0c-593">Make KeyVersion to optional when update Storage account with KeyvaultEncryption, to support key auto-rotation</span></span>
    - <span data-ttu-id="b4d0c-594">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="b4d0c-594">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="b4d0c-595">Problemet med borttagning av Azure-filkatalog i pipeline har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="b4d0c-595">Fixed remove Azure File Directory fail with pipeline</span></span>
    - <span data-ttu-id="b4d0c-596">”Remove-AzStorageDirectory”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-596">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="b4d0c-597">Åtgärdat [#9880]: Definitionen av DefaultAction-värdet för NetWorkRule har ändrats för konsekvens med Swagger.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-597">Fixed [#9880]: Change NetWorkRule DefaultAction value defination to align with swagger.</span></span>
    - <span data-ttu-id="b4d0c-598">”Update-AzStorageAccountNetworkRuleSet”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-598">'Update-AzStorageAccountNetworkRuleSet'</span></span>
    - <span data-ttu-id="b4d0c-599">”Get-AzStorageAccountNetworkRuleSet”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-599">'Get-AzStorageAccountNetworkRuleSet'</span></span>
* <span data-ttu-id="b4d0c-600">Åtgärdat [#11624]: Hoppa över dubblettregler när NetworkRules läggs till, för att undvika serverfel</span><span class="sxs-lookup"><span data-stu-id="b4d0c-600">Fixed [#11624]: Skip duplicated rules when add NetworkRules, to avoid server failure</span></span>
    - <span data-ttu-id="b4d0c-601">”Add-AzStorageAccountNetworkRule”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-601">'Add-AzStorageAccountNetworkRule'</span></span>
* <span data-ttu-id="b4d0c-602">Microsoft.Azure.Cosmos.Table SDK har uppgraderats till 1.0.7</span><span class="sxs-lookup"><span data-stu-id="b4d0c-602">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.7</span></span>
* <span data-ttu-id="b4d0c-603">Ett varningsmeddelande har lagts till för att påminna användaren om att lista igen med ContinuationToken när endast delobjekt returneras i listan med DataLake Gen2-objekt,</span><span class="sxs-lookup"><span data-stu-id="b4d0c-603">Added a warning message to remind user to list again with ContinuationToken when only part items are returned in list DataLake Gen2 Items,</span></span>
    - <span data-ttu-id="b4d0c-604">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="b4d0c-604">'Get-AzDataLakeGen2ChildItem'</span></span>
* <span data-ttu-id="b4d0c-605">Stöd för att skapa eller uppdatera lagringskonto med Azure Files Active Directory Domain Service-autentisering</span><span class="sxs-lookup"><span data-stu-id="b4d0c-605">Supported to create or update Storage account with Azure Files Active Directory Domain Service Authentication</span></span>
    -  <span data-ttu-id="b4d0c-606">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="b4d0c-606">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="b4d0c-607">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="b4d0c-607">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="b4d0c-608">Stöd för nya eller listade Kerberos-nycklar för lagringskontot</span><span class="sxs-lookup"><span data-stu-id="b4d0c-608">Supported to new or list Kerberos keys of Storage account</span></span>
    -  <span data-ttu-id="b4d0c-609">”New-AzStorageAccountKey”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-609">'New-AzStorageAccountKey'</span></span>
    -  <span data-ttu-id="b4d0c-610">”Get-AzStorageAccountKey”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-610">'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="b4d0c-611">Stöd för redundans med lagringskonto</span><span class="sxs-lookup"><span data-stu-id="b4d0c-611">Supported failover Storage account</span></span>
    - <span data-ttu-id="b4d0c-612">”Invoke-AzStorageAccountFailover”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-612">'Invoke-AzStorageAccountFailover'</span></span>
* <span data-ttu-id="b4d0c-613">Hjälpen för ”Get-AzStorageBlobCopyState” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="b4d0c-613">Updated help of 'Get-AzStorageBlobCopyState'</span></span>
* <span data-ttu-id="b4d0c-614">Hjälpen för ”Get-AzStorageFileCopyState” och ”Start-AzStorageBlobCopy” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="b4d0c-614">Updated help of 'Get-AzStorageFileCopyState' and 'Start-AzStorageBlobCopy'</span></span>
* <span data-ttu-id="b4d0c-615">Lagringsklientbibliotek v12 har integrerats med Queue- och File-cmdletar</span><span class="sxs-lookup"><span data-stu-id="b4d0c-615">Integrated Storage client library v12 to Queue and File cmdlets</span></span>
* <span data-ttu-id="b4d0c-616">Utdatatypen har ändrats från CloudFile till AzureStorageFile; ursprungliga utdata blir en underordnad egenskap i den nya utmatningen</span><span class="sxs-lookup"><span data-stu-id="b4d0c-616">Changed output type from CloudFile to AzureStorageFile, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="b4d0c-617">”Get-AzStorageFile”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-617">'Get-AzStorageFile'</span></span>
    - <span data-ttu-id="b4d0c-618">”Remove-AzStorageFile”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-618">'Remove-AzStorageFile'</span></span>
    - <span data-ttu-id="b4d0c-619">”Get-AzStorageFileContent”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-619">'Get-AzStorageFileContent'</span></span>
    - <span data-ttu-id="b4d0c-620">”Set-AzStorageFileContent”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-620">'Set-AzStorageFileContent'</span></span>
    - <span data-ttu-id="b4d0c-621">”Start-AzStorageFileCopy”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-621">'Start-AzStorageFileCopy'</span></span>
* <span data-ttu-id="b4d0c-622">Utdatatypen har ändrats från CloudFileDirectory till AzureStorageFileDirectory; ursprungliga utdata blir en underordnad egenskap i den nya utmatningen</span><span class="sxs-lookup"><span data-stu-id="b4d0c-622">Changed output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="b4d0c-623">”New-AzStorageDirectory”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-623">'New-AzStorageDirectory'</span></span>
    - <span data-ttu-id="b4d0c-624">”Remove-AzStorageDirectory”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-624">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="b4d0c-625">Utdatatypen har ändrats från CloudFileShare till AzureStorageFileShare; ursprungliga utdata blir en underordnad egenskap i den nya utmatningen</span><span class="sxs-lookup"><span data-stu-id="b4d0c-625">Changed output type from CloudFileShare to AzureStorageFileShare, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="b4d0c-626">”Get-AzStorageShare”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-626">'Get-AzStorageShare'</span></span>
    - <span data-ttu-id="b4d0c-627">”New-AzStorageShare”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-627">'New-AzStorageShare'</span></span>
    - <span data-ttu-id="b4d0c-628">”Remove-AzStorageShare”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-628">'Remove-AzStorageShare'</span></span>
* <span data-ttu-id="b4d0c-629">Utdatatypen har ändrats från FileShareProperties till AzureStorageFileShare; ursprungliga utdata blir en underordnad egenskap i den nya utmatningen</span><span class="sxs-lookup"><span data-stu-id="b4d0c-629">Changed output type from FileShareProperties to AzureStorageFileShare, the original output will become a sub child property of the new output</span></span>
    - <span data-ttu-id="b4d0c-630">”Set-AzStorageShareQuota”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-630">'Set-AzStorageShareQuota'</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="b4d0c-631">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="b4d0c-631">Az.TrafficManager</span></span>
* <span data-ttu-id="b4d0c-632">Felaktigt profilnamn har åtgärdats i utförliga utdata för ”DisableAzureTrafficManagerEndpoint”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-632">Fixed incorrect profile name in 'DisableAzureTrafficManagerEndpoint' verbose output</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b4d0c-633">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b4d0c-633">Az.Websites</span></span>
* <span data-ttu-id="b4d0c-634">Stavfel har åtgärdats i hjälpen för ”Update-AzWebAppAccessRestrictionConfig”.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-634">Fixed typo on help of 'Update-AzWebAppAccessRestrictionConfig'.</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="b4d0c-635">3.8.0 – April 2020</span><span class="sxs-lookup"><span data-stu-id="b4d0c-635">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="b4d0c-636">Höjdpunkter sedan den senaste uppdateringen</span><span class="sxs-lookup"><span data-stu-id="b4d0c-636">Highlights since the last release</span></span>
* <span data-ttu-id="b4d0c-637">PowerShell-versioner som Az.Storage stöder: Windows PowerShell 5.1, PowerShell Core 6.2.4+ och PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="b4d0c-637">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="b4d0c-638">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b4d0c-638">Az.Accounts</span></span>
* <span data-ttu-id="b4d0c-639">Uppdaterade URL:en för Azure PowerShell-enkäten i ”Resolve-AzError” [#11507]</span><span class="sxs-lookup"><span data-stu-id="b4d0c-639">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="b4d0c-640">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b4d0c-640">Az.ApiManagement</span></span>
* <span data-ttu-id="b4d0c-641">Lade till meddelande om icke-bakåtkompatibel ändring vid ändring i utdata för Azure File-cmdletar i en framtida version</span><span class="sxs-lookup"><span data-stu-id="b4d0c-641">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="b4d0c-642">"Set-AzApiManagementGroup" Uppdaterad dokumentation för att ange GroupId-parametern</span><span class="sxs-lookup"><span data-stu-id="b4d0c-642">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="b4d0c-643">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="b4d0c-643">Az.Cdn</span></span>
* <span data-ttu-id="b4d0c-644">Fast ChinaCDN-relaterad prissättning för SKU-visning</span><span class="sxs-lookup"><span data-stu-id="b4d0c-644">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="b4d0c-645">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="b4d0c-645">Az.CognitiveServices</span></span>
* <span data-ttu-id="b4d0c-646">Identitet som stöds, kryptering, UserOwnedStorage</span><span class="sxs-lookup"><span data-stu-id="b4d0c-646">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b4d0c-647">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b4d0c-647">Az.Compute</span></span>
* <span data-ttu-id="b4d0c-648">Cmdleten ”Set-AzVmssOrchestrationServiceState” har lagts till.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-648">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="b4d0c-649">”Get-AzVmss” med -InstanceView visar OrchestrationService-tillstånd.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-649">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="b4d0c-650">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="b4d0c-650">Az.IotHub</span></span>
* <span data-ttu-id="b4d0c-651">Hantera den dubbla konfigurationen för IoT-enheter, nya cmdletar är:</span><span class="sxs-lookup"><span data-stu-id="b4d0c-651">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="b4d0c-652">'Get-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="b4d0c-652">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="b4d0c-653">'Update-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="b4d0c-653">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="b4d0c-654">En cmdlet har lagts till för att anropa direkt metod på en enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-654">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="b4d0c-655">Hantera dubbel konfiguration för IoT-enhetsmodul, nya cmdletar är:</span><span class="sxs-lookup"><span data-stu-id="b4d0c-655">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="b4d0c-656">'Get-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="b4d0c-656">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="b4d0c-657">'Update-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="b4d0c-657">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="b4d0c-658">Hantera IoT-automatisk konfiguration av enhetshantering i stor skala.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-658">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="b4d0c-659">Nya cmdlet:ar är:</span><span class="sxs-lookup"><span data-stu-id="b4d0c-659">New cmdlets are:</span></span>
    - <span data-ttu-id="b4d0c-660">'Add-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="b4d0c-660">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="b4d0c-661">'Get-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="b4d0c-661">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="b4d0c-662">'Remove-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="b4d0c-662">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="b4d0c-663">'Set-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="b4d0c-663">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="b4d0c-664">En cmdlet har lagts till för att anropa en edge-modulmetod i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-664">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="b4d0c-665">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b4d0c-665">Az.KeyVault</span></span>
* <span data-ttu-id="b4d0c-666">Har lagt till en ny cmdlet, "Update-AzKeyVault", som kan aktivera mjuk borttagning och rensning av skydd i ett valv</span><span class="sxs-lookup"><span data-stu-id="b4d0c-666">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="b4d0c-667">Har lagt till stöd i Microsoft.PowerShell.SecretManagement [#11178]</span><span class="sxs-lookup"><span data-stu-id="b4d0c-667">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="b4d0c-668">Åtgärdat fel i exemplen i 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span><span class="sxs-lookup"><span data-stu-id="b4d0c-668">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="b4d0c-669">Har lagt till stöd för privat slutpunkt</span><span class="sxs-lookup"><span data-stu-id="b4d0c-669">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="b4d0c-670">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="b4d0c-670">Az.Maintenance</span></span>
* <span data-ttu-id="b4d0c-671">Publicerar slutversion av underhålls-cmdletar för GA</span><span class="sxs-lookup"><span data-stu-id="b4d0c-671">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="b4d0c-672">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b4d0c-672">Az.Monitor</span></span>
* <span data-ttu-id="b4d0c-673">Har lagt till cmdletar för privat länkomfång</span><span class="sxs-lookup"><span data-stu-id="b4d0c-673">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="b4d0c-674">'Get-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="b4d0c-674">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="b4d0c-675">'Remove-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="b4d0c-675">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="b4d0c-676">'New-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="b4d0c-676">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="b4d0c-677">'Update-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="b4d0c-677">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="b4d0c-678">'Get-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="b4d0c-678">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="b4d0c-679">'New-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="b4d0c-679">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="b4d0c-680">'Remove-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="b4d0c-680">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b4d0c-681">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b4d0c-681">Az.Network</span></span>
* <span data-ttu-id="b4d0c-682">Uppdaterade cmdletar för att aktivera anslutning på privat IP för Virtual Network Gateway.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-682">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="b4d0c-683">'New-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="b4d0c-683">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="b4d0c-684">'Set-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="b4d0c-684">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="b4d0c-685">'New-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="b4d0c-685">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="b4d0c-686">'Set-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="b4d0c-686">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="b4d0c-687">Uppdaterade cmdletar för att aktivera FQDN-baserade LocalNetworkGateways och VpnSites</span><span class="sxs-lookup"><span data-stu-id="b4d0c-687">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="b4d0c-688">'New-AzLocalNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="b4d0c-688">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="b4d0c-689">'New-AzVpnSiteLink'</span><span class="sxs-lookup"><span data-stu-id="b4d0c-689">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="b4d0c-690">Stöd har lagts till för IPv6-adresstypen i ExpressRouteCircuitConnectionConfig (Global Reach)</span><span class="sxs-lookup"><span data-stu-id="b4d0c-690">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="b4d0c-691">Lade till 'Set-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="b4d0c-691">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="b4d0c-692">tillåter inställning av alla befintliga egenskaper inklusive IPv6CircuitConnectionProperties</span><span class="sxs-lookup"><span data-stu-id="b4d0c-692">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="b4d0c-693">Uppdaterade 'Add-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="b4d0c-693">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="b4d0c-694">Lade till en ytterligare valfri parameter, AddressPrefixType, för att specificera adresstypen för adressprefix</span><span class="sxs-lookup"><span data-stu-id="b4d0c-694">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="b4d0c-695">Uppdaterade cmdletar för att aktivera inställningen för DPD-timeout på Virtual Network Gateway-anslutningar.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-695">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="b4d0c-696">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="b4d0c-696">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="b4d0c-697">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="b4d0c-697">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="b4d0c-698">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="b4d0c-698">Az.PolicyInsights</span></span>
* <span data-ttu-id="b4d0c-699">Cmdleten "Start-AzPolicyComplianceScan" har lagts till för att utlösa genomsökningar av principefterlevnad</span><span class="sxs-lookup"><span data-stu-id="b4d0c-699">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="b4d0c-700">Principdefinition, uppsättningsdefinition och tilldelningsversioner har lagts till i "Get-AzPolicyState"-utdata</span><span class="sxs-lookup"><span data-stu-id="b4d0c-700">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="b4d0c-701">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b4d0c-701">Az.ServiceFabric</span></span>
* <span data-ttu-id="b4d0c-702">Förbättrad kodformatering och användbarhet för "New-AzServiceFabricCluster"-exempel</span><span class="sxs-lookup"><span data-stu-id="b4d0c-702">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="b4d0c-703">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b4d0c-703">Az.Sql</span></span>
* <span data-ttu-id="b4d0c-704">Lade till cmdletarna "Get-AzSqlInstanceOperation" och "Stop-AzSqlInstanceOperation"</span><span class="sxs-lookup"><span data-stu-id="b4d0c-704">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="b4d0c-705">Stöd för granskning för ett lagringskonto i VNet.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-705">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b4d0c-706">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b4d0c-706">Az.Storage</span></span>
* <span data-ttu-id="b4d0c-707">Lade till meddelande om icke-bakåtkompatibel ändring vid ändring i utdata för Azure File-cmdletar i en framtida version</span><span class="sxs-lookup"><span data-stu-id="b4d0c-707">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="b4d0c-708">Stöd för nya SkuName StandardGZRS, StandardRAGZRS när ett lagringskonto skapas/uppdateras</span><span class="sxs-lookup"><span data-stu-id="b4d0c-708">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="b4d0c-709">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="b4d0c-709">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="b4d0c-710">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="b4d0c-710">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="b4d0c-711">Stöd för DataLake Gen2</span><span class="sxs-lookup"><span data-stu-id="b4d0c-711">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="b4d0c-712">'New-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="b4d0c-712">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="b4d0c-713">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="b4d0c-713">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="b4d0c-714">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="b4d0c-714">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="b4d0c-715">'Move-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="b4d0c-715">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="b4d0c-716">'Set-AzDataLakeGen2ItemAclObject'</span><span class="sxs-lookup"><span data-stu-id="b4d0c-716">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="b4d0c-717">'Update-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="b4d0c-717">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="b4d0c-718">'Get-AzDataLakeGen2ItemContent'</span><span class="sxs-lookup"><span data-stu-id="b4d0c-718">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="b4d0c-719">'Remove-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="b4d0c-719">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="b4d0c-720">0.10.0-förhandsversion – April 2020</span><span class="sxs-lookup"><span data-stu-id="b4d0c-720">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="b4d0c-721">Allmänt</span><span class="sxs-lookup"><span data-stu-id="b4d0c-721">General</span></span>
* <span data-ttu-id="b4d0c-722">Az-moduler är nu tillgängliga i förhandsversion på Azure Stack Hub.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-722">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="b4d0c-723">Därmed möjliggörs kompatibilitet för flera plattformar med Linux och macOs.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-723">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="b4d0c-724">Azure Stack Hub stöder nu PowerShell Core med AZ-moduler. Mer information finns [här](https://aka.ms/az4AzureStack)</span><span class="sxs-lookup"><span data-stu-id="b4d0c-724">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](https://aka.ms/az4AzureStack)</span></span>
* <span data-ttu-id="b4d0c-725">Supportprofil för AZ-moduler 2019-03-01-hybrid:</span><span class="sxs-lookup"><span data-stu-id="b4d0c-725">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="b4d0c-726">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="b4d0c-726">Az.Billing</span></span>
  - <span data-ttu-id="b4d0c-727">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b4d0c-727">Az.Compute</span></span>
  - <span data-ttu-id="b4d0c-728">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="b4d0c-728">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="b4d0c-729">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="b4d0c-729">Az.EventHub</span></span>
  - <span data-ttu-id="b4d0c-730">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="b4d0c-730">Az.IotHub</span></span>
  - <span data-ttu-id="b4d0c-731">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b4d0c-731">Az.KeyVault</span></span>
  - <span data-ttu-id="b4d0c-732">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b4d0c-732">Az.Monitor</span></span>
  - <span data-ttu-id="b4d0c-733">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b4d0c-733">Az.Network</span></span>
  - <span data-ttu-id="b4d0c-734">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b4d0c-734">Az.Resources</span></span>
  - <span data-ttu-id="b4d0c-735">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b4d0c-735">Az.Storage</span></span>
  - <span data-ttu-id="b4d0c-736">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b4d0c-736">Az.Websites</span></span>
* <span data-ttu-id="b4d0c-737">Tre nya PowerShell-moduler för AZ har introducerats som fungerar med Azure Stack Hub, och de är Az.Databox, Az.IotHub och Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="b4d0c-737">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="b4d0c-738">Kommandona är i princip oförändrade, med endast mindre ändringar som att AzureRM ändras till AZ</span><span class="sxs-lookup"><span data-stu-id="b4d0c-738">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="b4d0c-739">En uppdaterad länk till PowerShell-dokumentationen för Azure Stack Hub finns [här](https://aka.ms/InstallASHPowerShell)</span><span class="sxs-lookup"><span data-stu-id="b4d0c-739">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](https://aka.ms/InstallASHPowerShell)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="b4d0c-740">3.7.0 – mars 2020</span><span class="sxs-lookup"><span data-stu-id="b4d0c-740">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b4d0c-741">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b4d0c-741">Az.Accounts</span></span>
* <span data-ttu-id="b4d0c-742">Åtgärdade ”Get-AzTenant”/”Get-AzDefault”/”Set-AzDefault”-utlösning av NullReferenceException när du inte är inloggad [#10292]</span><span class="sxs-lookup"><span data-stu-id="b4d0c-742">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b4d0c-743">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b4d0c-743">Az.Compute</span></span>
* <span data-ttu-id="b4d0c-744">Följande parametrar har lagts till i cmdleten ”New-AzDiskConfig”:</span><span class="sxs-lookup"><span data-stu-id="b4d0c-744">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="b4d0c-745">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="b4d0c-745">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="b4d0c-746">Tillåten krypteringsegenskap till målparametern för cmdleten ”New-AzGalleryImageVersion”.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-746">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="b4d0c-747">Åtgärdade tempDisk-problem för cmdletarna ”Set-AzVmss”-Reimage och ”Invoke-AzVMReimage”.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-747">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="b4d0c-748">[#11354]</span><span class="sxs-lookup"><span data-stu-id="b4d0c-748">[#11354]</span></span>
* <span data-ttu-id="b4d0c-749">Stöd har lagts till i nedanstående cmdletar för nytt SAP-tillägg</span><span class="sxs-lookup"><span data-stu-id="b4d0c-749">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="b4d0c-750">”Set-AzVMAEMExtension”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-750">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="b4d0c-751">”Get-AzVMAEMExtension”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-751">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="b4d0c-752">”Remove-AzVMAEMExtension”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-752">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="b4d0c-753">”Update-AzVMAEMExtension”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-753">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="b4d0c-754">Åtgärdade fel i exempel på hjälpdokument</span><span class="sxs-lookup"><span data-stu-id="b4d0c-754">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="b4d0c-755">Visade det exakta strängvärdet för VM PowerState i tabellformat.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-755">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="b4d0c-756">”New-AzVmssConfig”: den fasta serialiseringen av egenskapen AutomaticRepairs när SinglePlacementGroup är inaktiverad.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-756">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="b4d0c-757">[#11257]</span><span class="sxs-lookup"><span data-stu-id="b4d0c-757">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b4d0c-758">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b4d0c-758">Az.DataFactory</span></span>
* <span data-ttu-id="b4d0c-759">ADF .Net SDK har uppdaterats till 4.8.0</span><span class="sxs-lookup"><span data-stu-id="b4d0c-759">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="b4d0c-760">Valfria parametrar har lagts till i kommandot ”Invoke-AzDataFactoryV2Pipeline” för att stödja omkörning</span><span class="sxs-lookup"><span data-stu-id="b4d0c-760">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b4d0c-761">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b4d0c-761">Az.DataLakeStore</span></span>
* <span data-ttu-id="b4d0c-762">Lade till beskrivning för icke-bakåtkompatibel ändring för ”Export-AzDataLakeStoreItem” och ”Import-AzDataLakeStoreItem”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-762">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="b4d0c-763">Lade till alternativ för bytekodning för ”New-AzDataLakeStoreItem”, ”Add-AzDAtaLakeStoreItemContent” och ”Get-AzDAtaLakeStoreItemContent”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-763">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="b4d0c-764">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="b4d0c-764">Az.HDInsight</span></span>
* <span data-ttu-id="b4d0c-765">Stöd för att ange en minimal TLS-version som stöds när klustret skapas.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-765">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="b4d0c-766">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="b4d0c-766">Az.IotHub</span></span>
* <span data-ttu-id="b4d0c-767">Stöd har lagts till för att hantera distribuerade inställningar per enhet.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-767">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="b4d0c-768">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="b4d0c-768">New Cmdlets are:</span></span>
    - <span data-ttu-id="b4d0c-769">”Get-AzIotHubDistributedTracing”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-769">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="b4d0c-770">”Set-AzIotHubDistributedTracing”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-770">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="b4d0c-771">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b4d0c-771">Az.KeyVault</span></span>
* <span data-ttu-id="b4d0c-772">Ändrade attribut för icke-bakåtkompatibel ändring lades till för ”New-AzKeyVault”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-772">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="b4d0c-773">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b4d0c-773">Az.Monitor</span></span>
* <span data-ttu-id="b4d0c-774">Uppdaterad dokumentation för ”New-AzScheduledQueryRuleLogMetricTrigger”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-774">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b4d0c-775">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b4d0c-775">Az.Network</span></span>
* <span data-ttu-id="b4d0c-776">Uppdaterade cmdletar för att tillåta VirtualHubVnetConnections mellan klienter</span><span class="sxs-lookup"><span data-stu-id="b4d0c-776">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="b4d0c-777">”New-AzVirtualHubVnetConnection”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-777">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="b4d0c-778">”Update-AzVirtualHubVnetConnection”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-778">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="b4d0c-779">”New-AzVirtualHub”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-779">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="b4d0c-780">”Update-AzVirtualHub”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-780">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="b4d0c-781">SQL Management SDK-beroende har tagits bort</span><span class="sxs-lookup"><span data-stu-id="b4d0c-781">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="b4d0c-782">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="b4d0c-782">Az.PolicyInsights</span></span>
* <span data-ttu-id="b4d0c-783">Förbättrade felmeddelanden</span><span class="sxs-lookup"><span data-stu-id="b4d0c-783">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b4d0c-784">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b4d0c-784">Az.RecoveryServices</span></span>
* <span data-ttu-id="b4d0c-785">Azure Site Recovery har lagt till stöd för återaktivering av skydd och uppdaterade VM-egenskaper för virtuella Azure-datorer med krypterad disk.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-785">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="b4d0c-786">Lade till Azure Site Recovery VmwareToAzure-egenskaper för DR-övervakning</span><span class="sxs-lookup"><span data-stu-id="b4d0c-786">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="b4d0c-787">Azure Backup har lagt till stöd för att försöka uppdatera principuppdateringen för misslyckade objekt på nytt.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-787">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="b4d0c-788">Azure Backup lagt till stöd för diskundantagsinställningar under säkerhetskopiering och återställning.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-788">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="b4d0c-789">Azure Backup lagt till stöd för att återställa flera filer/mappar i AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="b4d0c-789">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="b4d0c-790">Azure Backup lade till support för användardefinierad Resourcegroup-support vid uppdatering av IaasVM-princip</span><span class="sxs-lookup"><span data-stu-id="b4d0c-790">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="b4d0c-791">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b4d0c-791">Az.Resources</span></span>
* <span data-ttu-id="b4d0c-792">Åtgärdade ”Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType” så att den använder den faktisk apiVersion av resurser i stället för standard-apiVersion [#11267]</span><span class="sxs-lookup"><span data-stu-id="b4d0c-792">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="b4d0c-793">Lade till correlationId-loggning för felscenarier</span><span class="sxs-lookup"><span data-stu-id="b4d0c-793">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="b4d0c-794">Liten dokumentationsändring för ”Get-AzResourceLock”.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-794">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="b4d0c-795">Lade till exempel.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-795">Added example.</span></span>
* <span data-ttu-id="b4d0c-796">Undantaget enkelt citattecken i parametervärde för ”Get-AzADUser” [#11317]</span><span class="sxs-lookup"><span data-stu-id="b4d0c-796">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="b4d0c-797">Nya cmdletar har lagts till för distributionsskript (”Get-AzDeploymentScript”, ”Get-AzDeploymentScriptLog”, ”Save-AzDeploymentScriptLog”, ”Remove-AzDeploymentScript”)</span><span class="sxs-lookup"><span data-stu-id="b4d0c-797">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="b4d0c-798">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b4d0c-798">Az.Sql</span></span>
* <span data-ttu-id="b4d0c-799">En läsbar sekundär parameter har lagts till i Invoke-AzSqlDatabaseFailover</span><span class="sxs-lookup"><span data-stu-id="b4d0c-799">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="b4d0c-800">Cmdleten Disable-AzSqlServerActiveDirectoryOnlyAuthentication har lagts till</span><span class="sxs-lookup"><span data-stu-id="b4d0c-800">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="b4d0c-801">Den sparade känslighet rangordningen när kolumner klassificeras i databasen.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-801">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="b4d0c-802">Az.Support</span><span class="sxs-lookup"><span data-stu-id="b4d0c-802">Az.Support</span></span>
* <span data-ttu-id="b4d0c-803">Allmän tillgänglighet för ”Az.Support”-modulen</span><span class="sxs-lookup"><span data-stu-id="b4d0c-803">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b4d0c-804">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b4d0c-804">Az.Websites</span></span>
* <span data-ttu-id="b4d0c-805">Stöd har lagts till för att arbeta med trafikdirigeringsregler för webbappar under nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="b4d0c-805">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="b4d0c-806">”Get-AzWebAppTrafficRouting”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-806">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="b4d0c-807">”Update-AzWebAppTrafficRouting”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-807">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="b4d0c-808">”Add-AzWebAppTrafficRouting”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-808">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="b4d0c-809">”Remove-AzWebAppTrafficRouting”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-809">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="b4d0c-810">3.6.1 – mars 2020</span><span class="sxs-lookup"><span data-stu-id="b4d0c-810">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b4d0c-811">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b4d0c-811">Az.Accounts</span></span>
* <span data-ttu-id="b4d0c-812">Öppna sidan med Azure PowerShell-enkäten i ”Send-Feedback” [#11020]</span><span class="sxs-lookup"><span data-stu-id="b4d0c-812">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="b4d0c-813">Visa URL:en för Azure PowerShell-enkäten i ”Resolve-Error” [#11021]</span><span class="sxs-lookup"><span data-stu-id="b4d0c-813">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="b4d0c-814">Az-version har lagts till i UserAgent</span><span class="sxs-lookup"><span data-stu-id="b4d0c-814">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="b4d0c-815">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b4d0c-815">Az.ApiManagement</span></span>
* <span data-ttu-id="b4d0c-816">Stöd har lagts till för att hämta och konfigurera en anpassad domän på DeveloperPortal-slutpunkten [#11007]</span><span class="sxs-lookup"><span data-stu-id="b4d0c-816">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="b4d0c-817">”Export-AzApiManagementApi” Stöd har lagts till för att ladda ned API-definition i Json-format [#9987]</span><span class="sxs-lookup"><span data-stu-id="b4d0c-817">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="b4d0c-818">”Import-AzApiManagementApi” Stöd har lagts till för att importera OpenApi 3.0-definition från Json-dokument</span><span class="sxs-lookup"><span data-stu-id="b4d0c-818">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="b4d0c-819">”New-AzApiManagementIdentityProvider” och ”Set-AzApiManagementIdentityProvider” Stöd har lagts till för att konfigurera ”Signin Tenant” för AAD B2C-provider [#9784]</span><span class="sxs-lookup"><span data-stu-id="b4d0c-819">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b4d0c-820">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b4d0c-820">Az.DataLakeStore</span></span>
* <span data-ttu-id="b4d0c-821">En referens har uttryckligen lagts till för System.Buffers i csproj och psd1.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-821">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="b4d0c-822">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="b4d0c-822">Az.IotHub</span></span>
* <span data-ttu-id="b4d0c-823">Lade till stöd för att hantera enheter i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-823">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="b4d0c-824">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="b4d0c-824">New Cmdlets are:</span></span>
    - <span data-ttu-id="b4d0c-825">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="b4d0c-825">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="b4d0c-826">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="b4d0c-826">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="b4d0c-827">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="b4d0c-827">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="b4d0c-828">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="b4d0c-828">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="b4d0c-829">Stöd har lagts till för att hantera moduler på en mål-IoT-enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-829">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="b4d0c-830">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="b4d0c-830">New Cmdlets are:</span></span>
    - <span data-ttu-id="b4d0c-831">”Add-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-831">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="b4d0c-832">”Get-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-832">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="b4d0c-833">”Remove-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-833">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="b4d0c-834">”Set-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-834">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="b4d0c-835">Cmdlet har lagts till för att hämta anslutningssträngen för en mål-IoT-enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-835">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="b4d0c-836">Cmdlet har lagts till för att hämta anslutningssträngen för en modul på en mål-IoT-enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-836">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="b4d0c-837">Stöd har lagts till för att hämta/ange en överordnad enhet för en IoT-enhet.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-837">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="b4d0c-838">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="b4d0c-838">New Cmdlets are:</span></span>
    - <span data-ttu-id="b4d0c-839">”Get-AzIotHubDeviceParent”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-839">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="b4d0c-840">”Set-AzIotHubDeviceParent”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-840">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="b4d0c-841">Stöd har lagts till för att hantera en enhets överordnade och underordnade relationer.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-841">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="b4d0c-842">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b4d0c-842">Az.Monitor</span></span>
* <span data-ttu-id="b4d0c-843">Utdatavärdet har åtgärdats för ”Get-AzMetricDefinition” [#9714]</span><span class="sxs-lookup"><span data-stu-id="b4d0c-843">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b4d0c-844">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b4d0c-844">Az.Network</span></span>
* <span data-ttu-id="b4d0c-845">SQL Management SDK har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-845">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="b4d0c-846">Ett problem har åtgärdats med namngivningsskillnader i klassen PrivateLinkServiceConnectionState.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-846">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="b4d0c-847">Fältet ActionsRequired mappar till ActionRequired.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-847">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="b4d0c-848">PublicNetworkAccess har lagts till i ”New-AzSqlServer” och ”Set-AzSqlServer”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-848">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="b4d0c-849">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b4d0c-849">Az.Resources</span></span>
* <span data-ttu-id="b4d0c-850">Null-referensfel har åtgärdats i ”Get-AzRoleAssignment”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-850">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="b4d0c-851">Växlarna ”-Force” och ”-PassThru” är valfria i ”Remove-AzADGroup” [#10849]</span><span class="sxs-lookup"><span data-stu-id="b4d0c-851">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="b4d0c-852">Ett problem har åtgärdats som gjorde att ”MailNickname” inte returnerades i ”Remove-AzADGroup” [#11167]</span><span class="sxs-lookup"><span data-stu-id="b4d0c-852">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="b4d0c-853">Ett problem har åtgärdats som gjorde att pipe-åtgärden ”Remove-AzADGroup” inte fungerar [#11171]</span><span class="sxs-lookup"><span data-stu-id="b4d0c-853">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="b4d0c-854">Ett null-referensfel har åtgärdats i GetAzureRoleAssignmentCommand</span><span class="sxs-lookup"><span data-stu-id="b4d0c-854">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="b4d0c-855">Attribut för icke-bakåtkompatibla ändringar har lagts till för kommande ändringar i cmdlets för principer</span><span class="sxs-lookup"><span data-stu-id="b4d0c-855">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="b4d0c-856">”Get-AzResourceGroup” har uppdaterats för att utföra taggfiltrering för resursgrupper på serversidan</span><span class="sxs-lookup"><span data-stu-id="b4d0c-856">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="b4d0c-857">Utökade Tag-cmdlets stöder -ResourceId</span><span class="sxs-lookup"><span data-stu-id="b4d0c-857">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="b4d0c-858">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="b4d0c-858">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="b4d0c-859">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="b4d0c-859">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="b4d0c-860">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="b4d0c-860">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="b4d0c-861">Ny Tag-cmdlet har lagts till</span><span class="sxs-lookup"><span data-stu-id="b4d0c-861">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="b4d0c-862">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="b4d0c-862">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="b4d0c-863">Flyttade ScopedDeployment från SDK 3.3.0</span><span class="sxs-lookup"><span data-stu-id="b4d0c-863">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="b4d0c-864">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b4d0c-864">Az.Sql</span></span>
* <span data-ttu-id="b4d0c-865">PublicNetworkAccess har lagts till i ”New-AzSqlServer” och ”Set-AzSqlServer”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-865">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="b4d0c-866">Stöd har lagts till för konfiguration av säkerhetskopiering för långsiktig kvarhållning för hanterade databaser</span><span class="sxs-lookup"><span data-stu-id="b4d0c-866">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="b4d0c-867">Hämta/ange LTR-princip på en hanterad databas</span><span class="sxs-lookup"><span data-stu-id="b4d0c-867">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="b4d0c-868">Hämta LTR-säkerhetskopior efter hanterad databas, hanterad instans eller plats</span><span class="sxs-lookup"><span data-stu-id="b4d0c-868">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="b4d0c-869">Ta bort en LTR-säkerhetskopia</span><span class="sxs-lookup"><span data-stu-id="b4d0c-869">Remove an LTR backup</span></span>
    - <span data-ttu-id="b4d0c-870">Återställa en LTR-säkerhetskopia för att skapa en ny hanterad databas</span><span class="sxs-lookup"><span data-stu-id="b4d0c-870">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="b4d0c-871">MinimalTlsVersion har lagts till för New-AzSqlServer och Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="b4d0c-871">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="b4d0c-872">MinimalTlsVersion har lagts till för New-AzSqlInstance och Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="b4d0c-872">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="b4d0c-873">SQL SDK-versionen för Az.Network har ändrats</span><span class="sxs-lookup"><span data-stu-id="b4d0c-873">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b4d0c-874">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b4d0c-874">Az.Storage</span></span>
* <span data-ttu-id="b4d0c-875">AllowProtectedAppendWrite stöds i ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="b4d0c-875">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="b4d0c-876">”Set-AzRmStorageContainerImmutabilityPolicy”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-876">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="b4d0c-877">Varningsmeddelande har lagts till om icke-bakåtkompatibel ändring för ändring av typen AzureStorageTable i en senare version</span><span class="sxs-lookup"><span data-stu-id="b4d0c-877">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="b4d0c-878">”New-AzStorageTable”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-878">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="b4d0c-879">”Get-AzStorageTable”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-879">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b4d0c-880">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b4d0c-880">Az.Websites</span></span>
* <span data-ttu-id="b4d0c-881">Tag-parametern har lagts till för ”New-AzAppServicePlan” och ”Set-AzAppServicePlan”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-881">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="b4d0c-882">Stoppa cmdlet-körning om ett undantag uppstår när en anpassad domän läggs till på en webbplats</span><span class="sxs-lookup"><span data-stu-id="b4d0c-882">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="b4d0c-883">Stöd har lagts till för att utföra åtgärder för App Services som inte tillhör samma resursgrupp som App Services-planen</span><span class="sxs-lookup"><span data-stu-id="b4d0c-883">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="b4d0c-884">Åtkomstbegränsning har tillämpats på WebApp/Function i olika resursgrupper</span><span class="sxs-lookup"><span data-stu-id="b4d0c-884">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="b4d0c-885">Ett problem har åtgärdats för att ange anpassade värdnamn för WebAppSlots</span><span class="sxs-lookup"><span data-stu-id="b4d0c-885">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="b4d0c-886">3.5.0 – februari 2020</span><span class="sxs-lookup"><span data-stu-id="b4d0c-886">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="b4d0c-887">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="b4d0c-887">Highlights since the last major release</span></span>
* <span data-ttu-id="b4d0c-888">Uppdaterade telemetri på klientsidan.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-888">Updated client side telemetry.</span></span>
* <span data-ttu-id="b4d0c-889">Az.IotHub lade till cmdletar som stöd för att hantera enheter.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-889">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="b4d0c-890">Az.SqlVirtualMachine lade till cmdletar för lyssningsfunktion för tillgänglighetsgrupp.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-890">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="b4d0c-891">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b4d0c-891">Az.Accounts</span></span>
* <span data-ttu-id="b4d0c-892">Lade till SubscriptionId, TenantId och körningstid i data för telemetri på klientsidan</span><span class="sxs-lookup"><span data-stu-id="b4d0c-892">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="b4d0c-893">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b4d0c-893">Az.Automation</span></span>
* <span data-ttu-id="b4d0c-894">Åtgärdade skrivfel i exempel 1 i referensdokumentation för ”New-AzAutomationSoftwareUpdateConfiguration”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-894">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="b4d0c-895">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="b4d0c-895">Az.CognitiveServices</span></span>
* <span data-ttu-id="b4d0c-896">Uppdaterade SDK till 7.0</span><span class="sxs-lookup"><span data-stu-id="b4d0c-896">Updated SDK to 7.0</span></span>
* <span data-ttu-id="b4d0c-897">Förbättrade felmeddelande vid serversvar om tom brödtext</span><span class="sxs-lookup"><span data-stu-id="b4d0c-897">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b4d0c-898">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b4d0c-898">Az.Compute</span></span>
* <span data-ttu-id="b4d0c-899">Tillät tomt värde för ProximityPlacementGroupId under uppdatering</span><span class="sxs-lookup"><span data-stu-id="b4d0c-899">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="b4d0c-900">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="b4d0c-900">Az.FrontDoor</span></span>
* <span data-ttu-id="b4d0c-901">Lade till cmdlet för att hämta hanterade regeldefinitioner som kan användas i WAF</span><span class="sxs-lookup"><span data-stu-id="b4d0c-901">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="b4d0c-902">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="b4d0c-902">Az.IotHub</span></span>
* <span data-ttu-id="b4d0c-903">Lade till stöd för att hantera enheter i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-903">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="b4d0c-904">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="b4d0c-904">New Cmdlets are:</span></span>
    - <span data-ttu-id="b4d0c-905">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="b4d0c-905">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="b4d0c-906">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="b4d0c-906">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="b4d0c-907">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="b4d0c-907">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="b4d0c-908">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="b4d0c-908">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="b4d0c-909">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b4d0c-909">Az.KeyVault</span></span>
* <span data-ttu-id="b4d0c-910">Åtgärdade duplicerad text för Add-AzKeyVaultKey.md</span><span class="sxs-lookup"><span data-stu-id="b4d0c-910">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="b4d0c-911">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b4d0c-911">Az.Monitor</span></span>
* <span data-ttu-id="b4d0c-912">Åtgärdade beskrivning av cmdleten Get-AzLog.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-912">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="b4d0c-913">En ny parameter med namnet ActionGroupId har lagts till i kommandot ”New-AzMetricAlertRuleV2”.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-913">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="b4d0c-914">Användaren kan ange ActionGroupId(string) eller ActionGroup(ActivityLogAlertActionGroup).</span><span class="sxs-lookup"><span data-stu-id="b4d0c-914">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b4d0c-915">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b4d0c-915">Az.Network</span></span>
* <span data-ttu-id="b4d0c-916">Lade till en extra parameteranteckning för parametern ”-EnableProxyProtocol” för cmdleten ”New-AzPrivateLinkService”.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-916">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="b4d0c-917">Åtgärdade FilterData-exempel i Start-AzVirtualNetworkGatewayConnectionPacketCapture.md och Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-917">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="b4d0c-918">Lade till paketinsamlingsexempel för att samla in alla inre och yttre paket i Start-AzVirtualNetworkGatewayConnectionPacketCapture.md och Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-918">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="b4d0c-919">Lade till stöd för Azure-brandväggsprincip på VNet-brandväggar</span><span class="sxs-lookup"><span data-stu-id="b4d0c-919">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="b4d0c-920">Inga nya cmdletar har lagts till.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-920">No new cmdlets are added.</span></span> <span data-ttu-id="b4d0c-921">Lättar begränsningen för brandväggsprincip på VNet-brandväggar</span><span class="sxs-lookup"><span data-stu-id="b4d0c-921">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b4d0c-922">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b4d0c-922">Az.RecoveryServices</span></span>
* <span data-ttu-id="b4d0c-923">Lade till stöd för Restore-as-files för SQL-databaser.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-923">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="b4d0c-924">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b4d0c-924">Az.Resources</span></span>
* <span data-ttu-id="b4d0c-925">Omstrukturerade cmdletar för malldistribution</span><span class="sxs-lookup"><span data-stu-id="b4d0c-925">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="b4d0c-926">Lade till nya cmdletar för att hantera distributioner i hanteringsgruppen: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b4d0c-926">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="b4d0c-927">Lade till nya cmdletar för att hantera distributioner i klientorganisationsområdet: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="b4d0c-927">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="b4d0c-928">Omstrukturerade \*-AzDeployment-cmdletar för att fungera specifikt i prenumerationsomfattningen</span><span class="sxs-lookup"><span data-stu-id="b4d0c-928">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="b4d0c-929">Skapade alias \*-AzSubscriptionDeployment för \*-AzDeployment-cmdletar</span><span class="sxs-lookup"><span data-stu-id="b4d0c-929">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="b4d0c-930">Åtgärdade ”Update-AzADApplication” när parametern ”AvailableToOtherTenants” inte har angetts</span><span class="sxs-lookup"><span data-stu-id="b4d0c-930">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="b4d0c-931">Tog bort ApplicationObjectWithoutCredentialParameterSet för att undvika AmbiguousParameterSetException.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-931">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="b4d0c-932">Återskapade hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="b4d0c-932">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="b4d0c-933">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b4d0c-933">Az.Sql</span></span>
* <span data-ttu-id="b4d0c-934">Lade till stöd för återställning till tidpunkt mellan prenumerationer på hanterade instanser.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-934">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="b4d0c-935">Lade till stöd för att ändra befintlig SQL Managed Instance-maskinvarugenerering</span><span class="sxs-lookup"><span data-stu-id="b4d0c-935">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="b4d0c-936">Åtgärdade ”Update-AzSqlServerVulnerabilityAssessmentSetting”-hjälpexempel: parameter/egenskapsutdata - EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="b4d0c-936">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="b4d0c-937">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="b4d0c-937">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="b4d0c-938">Lade till cmdletar för lyssningsfunktion för tillgänglighetsgrupp</span><span class="sxs-lookup"><span data-stu-id="b4d0c-938">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="b4d0c-939">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="b4d0c-939">Az.StorageSync</span></span>
* <span data-ttu-id="b4d0c-940">Uppdaterade teckenuppsättningar som stöds i ”Invoke-AzStorageSyncCompatibilityCheck”.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-940">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="b4d0c-941">3.4.0 – februari 2020</span><span class="sxs-lookup"><span data-stu-id="b4d0c-941">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="b4d0c-942">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="b4d0c-942">Highlights since the last major release</span></span>
* <span data-ttu-id="b4d0c-943">Första Az.CosmosDB-versionen 0.1.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="b4d0c-943">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="b4d0c-944">Stöd för Az.Network ConnectionMonitor V2 har lagts till</span><span class="sxs-lookup"><span data-stu-id="b4d0c-944">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="b4d0c-945">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b4d0c-945">Az.Accounts</span></span>
* <span data-ttu-id="b4d0c-946">Inaktivera automatisk sparande av kontext när AzureRmContext.json inte är tillgängligt</span><span class="sxs-lookup"><span data-stu-id="b4d0c-946">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="b4d0c-947">Uppdatera referensen till Azure Powershell Common till 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="b4d0c-947">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="b4d0c-948">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b4d0c-948">Az.ApiManagement</span></span>
* <span data-ttu-id="b4d0c-949">**Get-AzApiManagementApiSchema** Hämtning av Open-Api-schema som är associerat med ett API har åtgärdats   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="b4d0c-949">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="b4d0c-950">**New-AzApiManagementProduct**\* och **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="b4d0c-950">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="b4d0c-951">Åtgärda dokumentation för https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="b4d0c-951">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="b4d0c-952">**Set-AzApiManagementApi** Exempel för att visa hur ServiceUrl uppdateras med hjälp av cmdleten har lagts till</span><span class="sxs-lookup"><span data-stu-id="b4d0c-952">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b4d0c-953">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b4d0c-953">Az.Compute</span></span>
* <span data-ttu-id="b4d0c-954">Begränsa antalet VM-status till 100 för att undvika begränsning när Get-AzVM -Status utförs utan VM-namn.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-954">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="b4d0c-955">Lägg till cmdleten Update-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="b4d0c-955">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="b4d0c-956">Lägg till parametrarna EncryptionType och DiskEncryptionSetId i följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="b4d0c-956">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="b4d0c-957">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="b4d0c-957">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="b4d0c-958">Lägg till parametern ColocationStatus för cmdleten Get-AzProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-958">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b4d0c-959">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b4d0c-959">Az.DataFactory</span></span>
* <span data-ttu-id="b4d0c-960">Uppdatera ADF .Net SDK-versionen till 4.7.0</span><span class="sxs-lookup"><span data-stu-id="b4d0c-960">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="b4d0c-961">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="b4d0c-961">Az.DeploymentManager</span></span>
* <span data-ttu-id="b4d0c-962">Lägger till LIST-åtgärder för resurser</span><span class="sxs-lookup"><span data-stu-id="b4d0c-962">Adds LIST operations for resources</span></span>
* <span data-ttu-id="b4d0c-963">Lägger till funktion för att utföra åtgärder för hälsokontrollsteg</span><span class="sxs-lookup"><span data-stu-id="b4d0c-963">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="b4d0c-964">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="b4d0c-964">Az.HDInsight</span></span>
* <span data-ttu-id="b4d0c-965">Åtgärda dokumentfel för New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-965">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="b4d0c-966">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b4d0c-966">Az.KeyVault</span></span>
* <span data-ttu-id="b4d0c-967">Lägg till Name-alias för attributet VaultName så att Remove-AzureKeyVault stämmer överens med New-AzureKeyVault.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-967">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b4d0c-968">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b4d0c-968">Az.Network</span></span>
* <span data-ttu-id="b4d0c-969">Nytt exempel har lagts till i Set-AzNetworkWatcherConfigFlowLog.md för att demonstrera ett inaktiveringsscenario för Trafikanalys.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-969">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="b4d0c-970">Lägg till stöd för att tilldela konfiguration av hanterings-IP till Azure Firewall – ett dedikerat undernät och en offentlig IP som brandväggen använder för dess hanteringstrafik</span><span class="sxs-lookup"><span data-stu-id="b4d0c-970">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="b4d0c-971">Cmdleten New-AzFirewall har uppdaterats:</span><span class="sxs-lookup"><span data-stu-id="b4d0c-971">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="b4d0c-972">Parametern -ManagementPublicIpAddress (inte obligatorisk) som accepterar ett offentligt IP-adressobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="b4d0c-972">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="b4d0c-973">Metoden SetManagementIpConfiguration har lagts till för brandväggsobjekt – kräver ett undernät och en offentlig IP-adress som indata – undernätets namn måste vara ”AzureFirewallManagementSubnet”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-973">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="b4d0c-974">Exempel för Get-AzNetworkSecurityGroup har korrigerats så att exempel visas för NSG:er i stället för nätverksgränssnitt.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-974">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="b4d0c-975">Ett skrivfel har åtgärdats i kommandot New-AzVpnSite som hindrade kompletteraren för resurs-ID från att fylla i en parameter.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-975">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="b4d0c-976">Stöd för Url-konfiguration i åtgärdsuppsättningen för omskrivningsregler i Application Gateway har lagts till</span><span class="sxs-lookup"><span data-stu-id="b4d0c-976">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="b4d0c-977">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="b4d0c-977">New cmdlets added:</span></span>
        - <span data-ttu-id="b4d0c-978">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="b4d0c-978">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="b4d0c-979">Cmdletar har uppdaterats med den valfria parametern -UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="b4d0c-979">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="b4d0c-980">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="b4d0c-980">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="b4d0c-981">Lägg till stöd för resurser för NetworkWatcher ConnectionMonitor version 2</span><span class="sxs-lookup"><span data-stu-id="b4d0c-981">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="b4d0c-982">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="b4d0c-982">Az.PolicyInsights</span></span>
* <span data-ttu-id="b4d0c-983">Stöd för utvärdering av efterlevnad innan fastställande av vilken resurs som ska åtgärdas</span><span class="sxs-lookup"><span data-stu-id="b4d0c-983">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="b4d0c-984">Lägg till parametern ”-ResourceDiscoverMode” för Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="b4d0c-984">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="b4d0c-985">Lägg till cmdleten Get-AzPolicyMetadata för att hämta resurser för principmetadata</span><span class="sxs-lookup"><span data-stu-id="b4d0c-985">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="b4d0c-986">Get-AzPolicyState och Get-AzPolicyStateSummary för API-versionen 2019-10-01 har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="b4d0c-986">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b4d0c-987">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b4d0c-987">Az.RecoveryServices</span></span>
* <span data-ttu-id="b4d0c-988">Azure Site Recovery-stöd för att ta bort en replikerad disk.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-988">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="b4d0c-989">Tillagt Azure Backup-stöd för att lägga till taggar när ett Recovery Services-valv skapas.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-989">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="b4d0c-990">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b4d0c-990">Az.Resources</span></span>
* <span data-ttu-id="b4d0c-991">Gör -Scope valfritt i cmdletarna \*-AzPolicyAssignment med standardinställning till kontextprenumeration</span><span class="sxs-lookup"><span data-stu-id="b4d0c-991">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="b4d0c-992">Lägg till exempel på att skapa ADServicePrincipal med lösenord och nyckelautentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="b4d0c-992">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="b4d0c-993">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b4d0c-993">Az.Sql</span></span>
<span data-ttu-id="b4d0c-994">Åtgärda cmdleten New-AzSqlDatabaseSecondary så att existensen PartnerDatabaseName kontrolleras i stället för existensen DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-994">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b4d0c-995">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b4d0c-995">Az.Storage</span></span>
* <span data-ttu-id="b4d0c-996">Stöd för angivning av krypteringsnyckeltyp för Tabell/kö i Skapa lagringskonto</span><span class="sxs-lookup"><span data-stu-id="b4d0c-996">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="b4d0c-997">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b4d0c-997">New-AzStorageAccount</span></span>
* <span data-ttu-id="b4d0c-998">Visa RequestId när StorageException inte har ExtendedErrorInformation</span><span class="sxs-lookup"><span data-stu-id="b4d0c-998">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="b4d0c-999">Åtgärda exempel 6 för cmdleten Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="b4d0c-999">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b4d0c-1000">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1000">Az.Websites</span></span>
* <span data-ttu-id="b4d0c-1001">Set-AzWebapp och Set-AzWebappSlot stöder egenskaperna AlwaysOn, MinTls och FtpsState</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1001">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="b4d0c-1002">Åtgärdar problemet där inställning av HttpsOnly samtidigt som AppservicePlan ändrades med det enskilda kommandot Set-AzWebApp återställde HttpsOnly till standardvärdet</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1002">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="b4d0c-1003">3.3.0 – januari 2020</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1003">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b4d0c-1004">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1004">Az.Accounts</span></span>
* <span data-ttu-id="b4d0c-1005">Nu stöder Add-AzEnvironment och Set-AzEnvironment parametrarna AzureAttestationServiceEndpointResourceId och AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1005">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="b4d0c-1006">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1006">Az.Cdn</span></span>
* <span data-ttu-id="b4d0c-1007">Information om felsvar visas i New-AzCdnEndpoint-cmdleten</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1007">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b4d0c-1008">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1008">Az.Compute</span></span>
* <span data-ttu-id="b4d0c-1009">Set-AzVMCustomScriptExtension-cmdleten har åtgärdats för en virtuell dator med hanterad OD-disk som inte har någon operativsystemprofil.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1009">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="b4d0c-1010">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1010">Az.ContainerInstance</span></span>
* <span data-ttu-id="b4d0c-1011">Parameternamn som används med New-AzContainerGroup-exempel har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1011">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="b4d0c-1012">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1012">Az.DataBoxEdge</span></span>
* <span data-ttu-id="b4d0c-1013">Cmdleten ”Get-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1013">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="b4d0c-1014">Hämta gränslagringscontainern</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1014">Get the Edge Storage Container</span></span>
* <span data-ttu-id="b4d0c-1015">Cmdleten ”New-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1015">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="b4d0c-1016">Skapa en ny gränslagringscontainer</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1016">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="b4d0c-1017">Cmdleten ”Remove-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1017">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="b4d0c-1018">Ta bort gränslagringscontainern</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1018">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="b4d0c-1019">Cmdleten ”Invoke-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1019">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="b4d0c-1020">Anropa åtgärd för att uppdatera data i gränslagringscontainer</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1020">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="b4d0c-1021">Cmdleten ”Get-AzDataBoxEdgeStorageAccount” har lagts till</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1021">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="b4d0c-1022">Hämta gränslagringskontot</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1022">Get the Edge Storage Account</span></span>
* <span data-ttu-id="b4d0c-1023">Cmdleten ”New-AzDataBoxEdgeStorageAccount” har lagts till</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1023">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="b4d0c-1024">Skapa ett nytt gränslagringskonto</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1024">Create new Edge Storage Account</span></span>
* <span data-ttu-id="b4d0c-1025">Cmdleten ”Remove-AzDataBoxEdgeStorageAccount” har lagts till</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1025">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="b4d0c-1026">Ta bort gränslagringskontot</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1026">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="b4d0c-1027">Anropa cmdleten ”Invoke-AzDataBoxEdgeShare”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1027">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="b4d0c-1028">Anropa åtgärd för att uppdatera resursdata</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1028">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="b4d0c-1029">Cmdleten ”Set-AzDataBoxEdgeStorageAccountCredential” har lagts till</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1029">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="b4d0c-1030">Ange autentiseringsuppgifter för az databoxedge-lagringskonto</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1030">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b4d0c-1031">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1031">Az.DataFactory</span></span>
* <span data-ttu-id="b4d0c-1032">Lägg till AutoUpdateETA-, LatestVersion-, PushedVersion-, TaskQueueId- och VersionStatus-egenskaper för Get-AzDataFactoryV2IntegrationRuntime-cmd</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1032">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="b4d0c-1033">Uppdatera ADF .Net SDK-versionen till 4.6.0</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1033">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="b4d0c-1034">Lägg till parametern ”PublicIPs” för ”Set-AzureRmDataFactoryV2IntegrationRuntime”-cmd så att Azure-SSIS IR kan skapas med statiska offentliga IP-adresser.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1034">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="b4d0c-1035">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1035">Az.DevTestLabs</span></span>
* <span data-ttu-id="b4d0c-1036">Ta bort den brutna länken i Get-AzDtlAllowedVMSizesPolicy.md</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1036">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="b4d0c-1037">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1037">Az.EventHub</span></span>
* <span data-ttu-id="b4d0c-1038">Korrigering av problem 10634: Åtgärda referensen till null-objekt för eventhubnamespace-borttagning</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1038">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="b4d0c-1039">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1039">Az.HDInsight</span></span>
* <span data-ttu-id="b4d0c-1040">Åtgärda Invoke-AzHDInsightHiveJob.md-fel.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1040">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="b4d0c-1041">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1041">Az.MachineLearning</span></span>
* <span data-ttu-id="b4d0c-1042">Nedanstående cmdletar har tagits bort eftersom MachineLearningCompute inte längre är tillgängligt</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1042">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="b4d0c-1043">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1043">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="b4d0c-1044">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1044">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="b4d0c-1045">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1045">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="b4d0c-1046">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1046">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="b4d0c-1047">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1047">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="b4d0c-1048">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1048">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="b4d0c-1049">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1049">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b4d0c-1050">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1050">Az.Network</span></span>
* <span data-ttu-id="b4d0c-1051">Uppgradera beroende av Microsoft.Azure.Management.Sql från 1.36-preview till 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1051">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b4d0c-1052">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1052">Az.RecoveryServices</span></span>
* <span data-ttu-id="b4d0c-1053">Ändrat Azure Site Recovery-stöd för krypterade vilande data på virtuella datorer med hanterade diskar med kundhanterade nycklar för Azure till Azure-providern.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1053">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="b4d0c-1054">Azure Site Recovery-stöd för att ange ID för diskkrypteringsuppsättning som valfri inmatning för aktivering av skydd för VMware till Azure.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1054">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="b4d0c-1055">Azure Site Recovery-stöd för att ange ID för diskkrypteringsuppsättning som valfri inmatning på disknivå för aktivering av skydd för VMware till Azure.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1055">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="b4d0c-1056">Azure Site Recovery-stöd för att uppdatera replikeringsskyddade objekt med mappning för diskkrypteringsuppsättning för HyperV till Azure.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1056">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="b4d0c-1057">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1057">Az.Resources</span></span>
* <span data-ttu-id="b4d0c-1058">Åtgärda ett fel i hjälpdokument för ”Remove-AzTag”.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1058">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="b4d0c-1059">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1059">Az.Sql</span></span>
* <span data-ttu-id="b4d0c-1060">Åtgärda funktioner i cmdletar för att ange baslinjen för sårbarhetsbedömning för arbete med huvuddatabasen för Azure-databasen och begränsa den för systemdatabaser på hanterade instanser.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1060">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="b4d0c-1061">Åtgärda ett fel när en redundansgrupp för en SQL-instans skapas</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1061">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="b4d0c-1062">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1062">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="b4d0c-1063">Lägg till DR som en ny giltig licenstyp</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1063">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b4d0c-1064">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1064">Az.Storage</span></span>
* <span data-ttu-id="b4d0c-1065">Lägg till varningsmeddelande om icke-bakåtkompatibel ändring för DefaultAction-värdeändring i en framtida version</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1065">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="b4d0c-1066">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1066">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="b4d0c-1067">Stöd för att hämta lagringskontots senaste synkroniseringstid genom att köra get-AzureRMStorageAccount med parametern -IncludeGeoReplicationStats</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1067">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="b4d0c-1068">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1068">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="b4d0c-1069">3.2.0 – December 2019</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1069">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="b4d0c-1070">Allmänt</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1070">General</span></span>
* <span data-ttu-id="b4d0c-1071">Uppdatera referenser i .psd1 för att använda relativa sökvägar för alla moduler</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1071">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="b4d0c-1072">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1072">Az.Accounts</span></span>
* <span data-ttu-id="b4d0c-1073">Ange rätt UserAgent för telemetri på klientsidan för Az 4.0 preview</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1073">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="b4d0c-1074">Visa användarvänligt felmeddelande när kontexten är null i Az 4.0 preview</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1074">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="b4d0c-1075">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1075">Az.Batch</span></span>
* <span data-ttu-id="b4d0c-1076">Korrigera problem [#10602](https://github.com/Azure/azure-powershell/issues/10602), där **New-AzBatchPool** skickade VirtualMachineConfiguration.ContainerConfiguration eller VirtualMachineConfiguration.DataDisks på ett felaktigt sätt till servern.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1076">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b4d0c-1077">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1077">Az.DataFactory</span></span>
* <span data-ttu-id="b4d0c-1078">Uppdatera ADF .Net SDK-versionen till 4.5.0</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1078">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="b4d0c-1079">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1079">Az.FrontDoor</span></span>
* <span data-ttu-id="b4d0c-1080">Stöd har lagts till för undantag för hanterade regler för brandväggen för webbaserade program</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1080">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="b4d0c-1081">Lägg till SocketAddr för automatisk komplettering</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1081">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="b4d0c-1082">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1082">Az.HealthcareApis</span></span>
* <span data-ttu-id="b4d0c-1083">Undantagshantering</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1083">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="b4d0c-1084">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1084">Az.KeyVault</span></span>
* <span data-ttu-id="b4d0c-1085">Åtgärdat fel vid åtkomst av värde som kanske inte har angetts</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1085">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="b4d0c-1086">Hantering av ECC-certifikat (Elliptic Curve Cryptography)</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1086">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="b4d0c-1087">Stöd har lagts till för att ange kurvan för certifikatprinciper</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1087">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="b4d0c-1088">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1088">Az.Monitor</span></span>
* <span data-ttu-id="b4d0c-1089">Lägger till valfritt argument i kommandot Lägg till diagnostikinställningar.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1089">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="b4d0c-1090">Ett växelargument som om det finns visar att exporten till Log Analytics måste ske till ett fast schema (kallas även</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1090">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="b4d0c-1091">dedikerad, datatyp)</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1091">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b4d0c-1092">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1092">Az.Network</span></span>
* <span data-ttu-id="b4d0c-1093">Stöd för IpGroups i program-, NAT- och nätverksregler för Azure Firewall.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1093">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="b4d0c-1094">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1094">Az.Resources</span></span>
* <span data-ttu-id="b4d0c-1095">Åtgärda ett problem där malldistributionen inte kan läsa en mallparameter om dess namn står i konflikt med ett inbyggt parameternamn.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1095">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="b4d0c-1096">Uppdaterade princip-cmdletar för att använda den nya API-versionen 2019-09-01 som introducerar grupperingsstöd inom principuppsättningsdefinitioner.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1096">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="b4d0c-1097">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1097">Az.Sql</span></span>
* <span data-ttu-id="b4d0c-1098">Uppgraderad funktion för att skapa lagring i automatisk aktivering av sårbarhetsbedömning till StorageV2</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1098">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b4d0c-1099">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1099">Az.Storage</span></span>
* <span data-ttu-id="b4d0c-1100">Stöd för generering av blob/container-identitetsbaserad SAS-token med lagringskontextbaserad på OAuth-autentisering</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1100">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="b4d0c-1101">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1101">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="b4d0c-1102">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1102">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="b4d0c-1103">Stöd för återkallning av användardelegeringsnycklar för lagringskonto för att återkalla alla SAS-token</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1103">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="b4d0c-1104">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1104">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="b4d0c-1105">Uppgradera till Microsoft.Azure.Management.Storage 14.2.0 för att stödja den nya API-versionen 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1105">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="b4d0c-1106">Stöd för QuotaGiB (resurskvot i Gibibye) för värden över 5120 i hanteringsplanet för cmdletar för filresurser och parameteraliaset. Quota har också lagts till för parametern ”QuotaGiB”.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1106">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="b4d0c-1107">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1107">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="b4d0c-1108">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1108">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="b4d0c-1109">Lägg till parameteraliaset QuotaGiB i parametern Quota</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1109">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="b4d0c-1110">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1110">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="b4d0c-1111">Åtgärda problemet att Set-AzStorageContainerAcl kan rensa den lagrade åtkomstprincipen</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1111">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="b4d0c-1112">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1112">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="b4d0c-1113">3.1.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1113">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="b4d0c-1114">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1114">Highlights since the last major release</span></span>
* <span data-ttu-id="b4d0c-1115">Az.DataBoxEdge 1.0.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1115">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="b4d0c-1116">Az.SqlVirtualMachine 1.0.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1116">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b4d0c-1117">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1117">Az.Compute</span></span>
* <span data-ttu-id="b4d0c-1118">Funktion för att använda en virtuell dator igen</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1118">VM Reapply feature</span></span>
    - <span data-ttu-id="b4d0c-1119">Lägg till parameter för att använda igen till cmdleten Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1119">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="b4d0c-1120">Funktionen AutomaticRepairs i VM-skalningsuppsättningar:</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1120">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="b4d0c-1121">Lägg till parametrarna EnableAutomaticRepair, AutomaticRepairGracePeriod och AutomaticRepairMaxInstanceRepairsPercent till följande cmdletar:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1121">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="b4d0c-1122">Stöd för galleriavbildningar i flera klientorganisationer för New-AzVM</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1122">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="b4d0c-1123">Lägg till "Spot" till argumentslutföraren i prioritetsparametern i cmdletarna New-AzVM, New-AzVMConfig och New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1123">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="b4d0c-1124">Lägg till parametrarna DiskIOPSReadWrite och DiskMBpsReadWrite till cmdleten Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1124">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="b4d0c-1125">Ändra parametern SourceImageId för cmdleten New-AzGalleryImageVersion till valfri</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1125">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="b4d0c-1126">Lägg till parametrarna OSDiskImage och DataDiskImage till cmdleten New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1126">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="b4d0c-1127">Lägg till parametern HyperVGeneration till cmdleten New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1127">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="b4d0c-1128">Lägg till parametern SkipExtensionsOnOverprovisionedVMs till cmdletarna New-AzVmss, New-AzVmssConfig och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1128">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="b4d0c-1129">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1129">Az.DataBoxEdge</span></span>
* <span data-ttu-id="b4d0c-1130">Cmdleten `Get-AzDataBoxEdgeOrder` har lagts till</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1130">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="b4d0c-1131">Hämta ordning</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1131">Get the Order</span></span>
* <span data-ttu-id="b4d0c-1132">Cmdleten `New-AzDataBoxEdgeOrder` har lagts till</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1132">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="b4d0c-1133">Skapa ny ordning</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1133">Create new Order</span></span>
* <span data-ttu-id="b4d0c-1134">Cmdleten `Remove-AzDataBoxEdgeOrder` har lagts till</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1134">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="b4d0c-1135">Ta bort ordning</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1135">Remove the Order</span></span>
* <span data-ttu-id="b4d0c-1136">Cmdleten `New-AzDataBoxEdgeShare` har ändrats</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1136">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="b4d0c-1137">Nu skapas lokal filresurs</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1137">Now creates Local Share</span></span>
* <span data-ttu-id="b4d0c-1138">Cmdleten `Set-AzDataBoxEdgeRole` har lagts till</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1138">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="b4d0c-1139">Nu kan IotRole mappas till filresursen</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1139">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="b4d0c-1140">Cmdleten `Invoke-AzDataBoxEdgeDevice` har lagts till</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1140">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="b4d0c-1141">Anropa genomsökningsuppdatering, ladda ned uppdatering, installera uppdateringar på enheten</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1141">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="b4d0c-1142">Cmdleten `Get-AzDataBoxEdgeTrigger` har lagts till</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1142">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="b4d0c-1143">Hämtar information om utlösare</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1143">Gets the information about Triggers</span></span>
* <span data-ttu-id="b4d0c-1144">Cmdleten `New-AzDataBoxEdgeTrigger` har lagts till</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1144">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="b4d0c-1145">Skapa nya utlösare</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1145">Create new Triggers</span></span>
* <span data-ttu-id="b4d0c-1146">Cmdleten `Remove-AzDataBoxEdgeTrigger` har lagts till</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1146">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="b4d0c-1147">Ta bort utlösare</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1147">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b4d0c-1148">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1148">Az.DataFactory</span></span>
* <span data-ttu-id="b4d0c-1149">Uppdatera ADF .Net SDK-versionen till 4.4.0</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1149">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="b4d0c-1150">Lägg till parametern ExpressCustomSetup för kommandot Set-AzureRmDataFactoryV2IntegrationRuntime för att aktivera installationskonfigurationer och komponenter från tredje part utan anpassat konfigurationsskript.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1150">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b4d0c-1151">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1151">Az.DataLakeStore</span></span>
* <span data-ttu-id="b4d0c-1152">Uppdatera dokumentation för Get-AzDataLakeStoreDeletedItem och Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1152">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="b4d0c-1153">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1153">Az.EventHub</span></span>
* <span data-ttu-id="b4d0c-1154">Korrigering av problem #10301: Korrigera datumformat för SAS-token</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1154">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="b4d0c-1155">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1155">Az.FrontDoor</span></span>
* <span data-ttu-id="b4d0c-1156">Lägg till parametern MinimumTlsVersion till Enable-AzFrontDoorCustomDomainHttps och New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1156">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="b4d0c-1157">Lägg till parametrarna HealthProbeMethod och EnabledState till New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1157">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="b4d0c-1158">Lägg till en ny cmdlet för att skapa BackendPoolsSettings-objekt som passar i skapande/uppdatering av Front Door</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1158">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="b4d0c-1159">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1159">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b4d0c-1160">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1160">Az.Network</span></span>
* <span data-ttu-id="b4d0c-1161">Ändra alternativexemplen Start-AzVirtualNetworkGatewayConnectionPacketCapture.md och Start-AzVirtualnetworkGatewayPacketCapture.md för FilterData.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1161">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="b4d0c-1162">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1162">Az.PrivateDns</span></span>
* <span data-ttu-id="b4d0c-1163">Uppdaterade PrivateDns .NET SDK till version 1.0.0</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1163">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b4d0c-1164">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1164">Az.RecoveryServices</span></span>
* <span data-ttu-id="b4d0c-1165">Stöd för att välja disktyp vid aktivering av skydd i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1165">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="b4d0c-1166">Korrigering av bugg för åtgärdsredigering av återställningsplan i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1166">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="b4d0c-1167">Återställningsstöd för att godkänna filestream-databaser i Azure Backup SQL.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1167">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="b4d0c-1168">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1168">Az.RedisCache</span></span>
* <span data-ttu-id="b4d0c-1169">Parametern MinimumTlsVersion har lagts till i cmdletarna New-AzRedisCache och Set-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1169">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="b4d0c-1170">Dessutom har MinimumTlsVersion lagts till i utdata för cmdleten Get-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1170">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="b4d0c-1171">Verifiering har lagts till på parametern -Size i cmdletarna Set-AzRedisCache och New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1171">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="b4d0c-1172">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1172">Az.Resources</span></span>
- <span data-ttu-id="b4d0c-1173">Uppdaterade policy-cmdletar för att använda den nya API-versionen 2019-06-01 som har en ny EnforcementMode-egenskap i policytilldelningen.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1173">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="b4d0c-1174">Uppdaterade hjälpexempel för skapandet av policydefinition</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1174">Updated create policy definition help example</span></span>
- <span data-ttu-id="b4d0c-1175">Åtgärda bugg i Remove-AZADServicePrincipal -ServicePrincipalName, utlös null-referens när tjänstens huvudnamn inte hittas.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1175">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="b4d0c-1176">Åtgärda bugg i New-AZADServicePrincipal, utlös null-referens när klientorganisationen inte har någon prenumeration.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1176">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="b4d0c-1177">Ändra New-AzAdServicePrincipal för att endast lägga till autentiseringsuppgifter för det associerade programmet.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1177">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="b4d0c-1178">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1178">Az.Sql</span></span>
* <span data-ttu-id="b4d0c-1179">Stöd har lagts till för databasen ReadReplicaCount.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1179">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="b4d0c-1180">Korrigerade Set-AzSqlDatabase när zonredundans inte har angetts</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1180">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="b4d0c-1181">3.0.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1181">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="b4d0c-1182">Allmänt</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1182">General</span></span>
* <span data-ttu-id="b4d0c-1183">Az. PrivateDns 1.0.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1183">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="b4d0c-1184">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1184">Az.Accounts</span></span>
* <span data-ttu-id="b4d0c-1185">Lägg till ett utfasningsmeddelande för aliaset Resolve-error.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1185">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="b4d0c-1186">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1186">Az.Advisor</span></span>
* <span data-ttu-id="b4d0c-1187">Den nya kategorin Operational Excellence har lagts till i cmdleten Get-AzAdvisorRecommendation.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1187">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="b4d0c-1188">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1188">Az.Batch</span></span>
* <span data-ttu-id="b4d0c-1189">`CoreQuota` på `BatchAccountContext` har bytt namn till `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1189">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="b4d0c-1190">Det finns även en ny `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1190">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="b4d0c-1191">Detta påverkar **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1191">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="b4d0c-1192">**New-AzBatchTask** `-ResourceFile`-parametern tar nu en samling `PSResourceFile`-objekt som kan skapas med hjälp av den nya cmdleten **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1192">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="b4d0c-1193">Ny **New-AzBatchResourceFile**-cmdlet för att skapa `PSResourceFile`-objekt.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1193">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="b4d0c-1194">Dessa kan tillhandahållas till **New-AzBatchTask** på `-ResourceFile`-parametern.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1194">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="b4d0c-1195">Detta stöder två nya typer av resursfiler förutom det befintliga sättet med `HttpUrl`:</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1195">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="b4d0c-1196">`AutoStorageContainerName`-baserade resursfiler laddar ned en hel container för automatisk lagring till Batch-noden.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1196">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="b4d0c-1197">`StorageContainerUrl`-baserade resursfiler laddar ned containern som anges i webbadressen till Batch-noden.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1197">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="b4d0c-1198">Tog bort egenskapen `ApplicationPackages` för `PSApplication` som returnerades av **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1198">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="b4d0c-1199">Specifika paket i ett program kan nu hämtas med hjälp av **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1199">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="b4d0c-1200">Till exempel: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1200">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="b4d0c-1201">Bytt namn på `ApplicationId` till `ApplicationName` på **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** och **Set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1201">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="b4d0c-1202">`ApplicationId` är nu ett alias för `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1202">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="b4d0c-1203">Ny `PSWindowsUserConfiguration`-egenskap till `PSUserAccount` lades till.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1203">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="b4d0c-1204">Bytte namn på `Version` till `Name` på `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1204">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="b4d0c-1205">Bytte namn på `BlobSource` till `HttpUrl` på `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1205">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="b4d0c-1206">Tog bort egenskapen `OSDisk` från `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1206">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="b4d0c-1207">Tog bort **Set-AzBatchPoolOSVersion**.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1207">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="b4d0c-1208">Den här åtgärden stöds inte längre.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1208">This operation is no longer supported.</span></span>
* <span data-ttu-id="b4d0c-1209">`TargetOSVersion` har tagits bort från `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1209">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="b4d0c-1210">Bytte namn på `CurrentOSVersion` till `OSVersion` på `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1210">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="b4d0c-1211">`DataEgressGiB` och `DataIngressGiB` har tagits bort från `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1211">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="b4d0c-1212">Tog bort **Get-AzBatchNodeAgentSku** och ersatte det med **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1212">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="b4d0c-1213">**Get-AzBatchSupportedImage** returnerar samma data som **Get-AzBatchNodeAgentSku** men i ett mer användarvänligt format.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1213">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="b4d0c-1214">Nya icke-verifierade avbildningar returneras nu också.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1214">New non-verified images are also now returned.</span></span> <span data-ttu-id="b4d0c-1215">Ytterligare information om `Capabilities` och `BatchSupportEndOfLife` för varje avbildning inkluderas också.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1215">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="b4d0c-1216">Lade till möjlighet att montera fjärrfilsystem på varje nod i en pool via den nya parametern `MountConfiguration` för **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1216">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="b4d0c-1217">Har nu stöd för nätverkssäkerhetsregler som blockerar nätverksåtkomst till en pool baserat på källportens trafik.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1217">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="b4d0c-1218">Detta görs via egenskapen `SourcePortRanges` på `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1218">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="b4d0c-1219">När du kör en container stöder nu Batch körningen av uppgiften i arbetskatalogen för containern eller i arbetskatalogen för Batch-uppgiften.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1219">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="b4d0c-1220">Detta styrs av egenskapen `WorkingDirectory` på `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1220">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="b4d0c-1221">Lade till en funktion för att ange en samling av offentliga IP-adresser på `PSNetworkConfiguration` via den nya egenskapen `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1221">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="b4d0c-1222">Detta garanterar att noderna i poolen har en IP-adress från listan över IP-adresser som tillhandahållits av användare.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1222">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="b4d0c-1223">Om inget värde anges är standardvärdet för `WaitForSuccess` på `PSSTartTask` nu `$True` (var tidigare `$False`).</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1223">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="b4d0c-1224">Om inget värde anges är standardvärdet för `Scope` på `PSAutoUserSpecification` nu `Pool` (var tidigare `Task` på Windows och `Pool` på Linux).</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1224">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="b4d0c-1225">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1225">Az.Cdn</span></span>
* <span data-ttu-id="b4d0c-1226">Introducerade UrlRewriteAction och CacheKeyQueryStringAction till RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1226">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="b4d0c-1227">Åtgärdade flera buggar, som saknade indata för ”väljare” i cmdleten New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1227">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b4d0c-1228">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1228">Az.Compute</span></span>
* <span data-ttu-id="b4d0c-1229">Funktion för diskkrypteringsuppsättning</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1229">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="b4d0c-1230">Nya cmdletar:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1230">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="b4d0c-1231">Parametern DiskEncryptionSetId har lagts till i följande cmdletar:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1231">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="b4d0c-1232">Parametrarna DiskEncryptionSetId och EncryptionType har lagts till i följande cmdletar:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1232">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="b4d0c-1233">Lägg till parametern PublicIPAddressVersion i New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1233">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="b4d0c-1234">Flytta FileUris för anpassat skripttillägg från offentlig inställning till skyddad inställning</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1234">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="b4d0c-1235">Lägg till ScaleInPolicy i cmdletarna New-AzVmss, New-AzVmssConfig och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1235">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="b4d0c-1236">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1236">Breaking changes</span></span>
    - <span data-ttu-id="b4d0c-1237">Parametern UploadSizeInBytes används istället för DiskSizeGB för New-AzDiskConfig när CreateOption är Uppladdning</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1237">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="b4d0c-1238">PublishingProfile.Source.ManagedImage.Id ersätts med StorageProfile.Source.Id i objektet GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1238">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b4d0c-1239">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1239">Az.DataFactory</span></span>
* <span data-ttu-id="b4d0c-1240">Uppdatera ADF .Net SDK-versionen till 4.3.0</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1240">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b4d0c-1241">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1241">Az.DataLakeStore</span></span>
* <span data-ttu-id="b4d0c-1242">Uppdatera ADLS SDK-version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) innehåller följande korrigeringar</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1242">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="b4d0c-1243">Undvik att utlösa undantag när det inte går att deserialisera creationtime för inmatning av papperskorg eller katalog.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1243">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="b4d0c-1244">Gör inställning tillgänglig per tidsgräns för förfrågan i adlsclient</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1244">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="b4d0c-1245">Korrigera överföringen av ursprunglig syncflag för badoffset-återställning</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1245">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="b4d0c-1246">Korrigera EnumerateDirectory för att hämta fortsättningstoken när svar har kontrollerats</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1246">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="b4d0c-1247">Korrigera bugg i Concat</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1247">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="b4d0c-1248">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1248">Az.FrontDoor</span></span>
* <span data-ttu-id="b4d0c-1249">Åtgärdade diverse stavfel i modul</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1249">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="b4d0c-1250">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1250">Az.HDInsight</span></span>
* <span data-ttu-id="b4d0c-1251">Korrigerade buggen att kunder får felet ”inte en giltig Base-64-sträng” vid användning av Get-AzHDInsightCluster för att hämta klustret med ADLSGen1-lagring.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1251">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="b4d0c-1252">Lägg till en parameter med namnet ”ApplicationId” i de tre cmdletarna Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig och New-AzHDInsightCluster så att kunden kan tillhandahålla tjänstens huvudnamn för program-ID för åtkomst till Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1252">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="b4d0c-1253">Ändrade Microsoft.Azure.Management.HDInsight från 2.1.0 till 5.1.0</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1253">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="b4d0c-1254">Fem cmdletar har tagits bort:</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1254">Removed five cmdlets:</span></span>
    - <span data-ttu-id="b4d0c-1255">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1255">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="b4d0c-1256">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1256">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="b4d0c-1257">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1257">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="b4d0c-1258">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1258">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="b4d0c-1259">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1259">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="b4d0c-1260">Tre cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1260">Added three cmdlets:</span></span>
    - <span data-ttu-id="b4d0c-1261">Get-AzHDInsightMonitoring som ersätter Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1261">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="b4d0c-1262">Enable-AzHDInsightMonitoring som ersätter Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1262">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="b4d0c-1263">Disable-AzHDInsightMonitoring som ersätter Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1263">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="b4d0c-1264">Korrigerade cmdleten Get-AzHDInsightProperties för att stödja hämtning av funktionsinformation från en viss plats.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1264">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="b4d0c-1265">Parameteruppsättningarna (Spark1 och Spark2) har tagits bort från Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1265">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="b4d0c-1266">Lägg till exempel för cmdleten Add-AzHDInsightSecurityProfile till hjälpdokumenten.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1266">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="b4d0c-1267">Ändrade utdatatyp för följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1267">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="b4d0c-1268">Ändrade utdatatyp för Get-AzHDInsightProperties från CapabilitiesResponse till AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1268">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="b4d0c-1269">Ändrade utdatatyp för Remove-AzHDInsightCluster från ClusterGetResponse till bool.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1269">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="b4d0c-1270">Ändrade utdatatyp för Set-AzHDInsightGatewaySettings HttpConnectivitySettings till GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1270">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="b4d0c-1271">Lade till testfall för vissa scenarier.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1271">Added some scenario test cases.</span></span>
* <span data-ttu-id="b4d0c-1272">Ta bort vissa alias: Add-AzHDInsightConfigValues, Get-AzHDInsightProperties.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1272">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="b4d0c-1273">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1273">Az.IotHub</span></span>
* <span data-ttu-id="b4d0c-1274">Icke-bakåtkompatibla ändringar:</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1274">Breaking changes:</span></span>
    - <span data-ttu-id="b4d0c-1275">Cmdleten Add-AzIotHubEventHubConsumerGroup har inte längre stöd för parametern EventHubEndpointName och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1275">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="b4d0c-1276">Parameteruppsättningen __AllParameterSets för cmdleten Add-AzIotHubEventHubConsumerGroup har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1276">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="b4d0c-1277">Cmdleten Get-AzIotHubEventHubConsumerGroup har inte längre stöd för parametern EventHubEndpointName och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1277">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="b4d0c-1278">Parameteruppsättningen __AllParameterSets för cmdleten Get-AzIotHubEventHubConsumerGroup har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1278">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="b4d0c-1279">Egenskapen OperationsMonitoringProperties av typen Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1279">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="b4d0c-1280">Egenskapen OperationsMonitoringProperties av typen Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1280">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="b4d0c-1281">Cmdleten New-AzIotHubExportDevice stöder inte längre aliaset New-AzIotHubExportDevices.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1281">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="b4d0c-1282">Cmdleten New-AzIotHubImportDevice stöder inte längre aliaset New-AzIotHubImportDevices.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1282">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="b4d0c-1283">Cmdleten Remove-AzIotHubEventHubConsumerGroup har inte längre stöd för parametern EventHubEndpointName och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1283">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="b4d0c-1284">Parameteruppsättningen __AllParameterSets för cmdleten Remove-AzIotHubEventHubConsumerGroup har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1284">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="b4d0c-1285">Cmdleten Set-AzIotHub har inte längre stöd för parametern OperationsMonitoringProperties och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1285">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="b4d0c-1286">Parameteruppsättningen UpdateOperationsMonitoringProperties för cmdleten Set-AzIotHub har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1286">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b4d0c-1287">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1287">Az.RecoveryServices</span></span>
* <span data-ttu-id="b4d0c-1288">Azure Site Recovery-stöd för att konfigurera nätverksresurser som NSG, offentliga IP-adresser och interna lastbalanserare för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1288">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="b4d0c-1289">Azure Site Recovery-stöd för att skriva till hanterad disk för vMWare till Azure.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1289">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="b4d0c-1290">Azure Site Recovery-stöd för NIC-reduktion för vMWare till Azure.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1290">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="b4d0c-1291">Azure Site Recovery-stöd för accelererat nätverk för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1291">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="b4d0c-1292">Azure Site Recovery-stöd för automatisk uppdatering av agent för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1292">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="b4d0c-1293">Azure Site Recovery-stöd för Standard SSD för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1293">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="b4d0c-1294">Azure Site Recovery-stöd för tvåstegskryptering i Azure Disk Encryption för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1294">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="b4d0c-1295">Azure Site Recovery-stöd för att skydda nyligen tillagda diskar för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1295">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="b4d0c-1296">En funktion för mjuk borttagning av virtuella datorer samt tester för mjuk borttagning har tagits bort</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1296">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="b4d0c-1297">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1297">Az.Resources</span></span>
* <span data-ttu-id="b4d0c-1298">Uppdatera beroendesammansättning för Microsoft.Extensions.Caching.Memory från 1.1.1 till 2.2</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1298">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b4d0c-1299">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1299">Az.Network</span></span>
* <span data-ttu-id="b4d0c-1300">Ändra alla cmdletar för PrivateEndpointConnection så att de stöder generiska tjänstleverantörer.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1300">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="b4d0c-1301">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1301">Updated cmdlet:</span></span>
        - <span data-ttu-id="b4d0c-1302">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1302">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="b4d0c-1303">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1303">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="b4d0c-1304">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1304">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="b4d0c-1305">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1305">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="b4d0c-1306">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1306">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="b4d0c-1307">Lägg till ny cmdlet för PrivateLinkResource så att det också stöder generiska tjänstleverantörer.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1307">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="b4d0c-1308">Ny cmdlet:</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1308">New cmdlet:</span></span>
        - <span data-ttu-id="b4d0c-1309">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1309">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="b4d0c-1310">Lägg till nya fält och parametrar för funktionen Proxy Protocol V2.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1310">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="b4d0c-1311">Lägg till egenskapen EnableProxyProtocol i PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1311">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="b4d0c-1312">Lägg till egenskapen LinkIdentifier i PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1312">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="b4d0c-1313">Uppdaterade New-AzPrivateLinkService för att lägga till den nya valfria parametern EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1313">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="b4d0c-1314">Korrigera felaktig beskrivning av parameter i referensdokumentationen för New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1314">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="b4d0c-1315">Nya cmdletar som stöder Azure-brandväggsprincipen</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1315">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="b4d0c-1316">Lägg till stöd för den underordnade resursen RouteTables för VirtualHub</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1316">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="b4d0c-1317">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1317">New cmdlets added:</span></span>
        - <span data-ttu-id="b4d0c-1318">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1318">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="b4d0c-1319">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1319">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="b4d0c-1320">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1320">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="b4d0c-1321">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1321">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="b4d0c-1322">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1322">Set-AzVirtualHub</span></span>
* <span data-ttu-id="b4d0c-1323">Lägg till stöd för ny egenskaps-SKU för VirtualHub och VirtualWANType för VirtualWan</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1323">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="b4d0c-1324">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1324">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="b4d0c-1325">New-AzVirtualHub: lade till parameter-SKU</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1325">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="b4d0c-1326">Update-AzVirtualHub: lade till parameter-SKU</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1326">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="b4d0c-1327">New-AzVirtualWan: lade till parametern VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1327">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="b4d0c-1328">Update-AzVirtualWan: lade till parametern VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1328">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="b4d0c-1329">Lägg till stöd för egenskapen EnableInternetSecurity för HubVnetConnection, VpnConnection och ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1329">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="b4d0c-1330">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1330">New cmdlets added:</span></span>
        - <span data-ttu-id="b4d0c-1331">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1331">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="b4d0c-1332">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1332">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="b4d0c-1333">New-AzureRmVirtualHubVnetConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1333">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="b4d0c-1334">New-AzureRmVpnConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1334">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="b4d0c-1335">Update-AzureRmVpnConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1335">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="b4d0c-1336">New-AzureRmExpressRouteConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1336">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="b4d0c-1337">Set-AzureRmExpressRouteConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1337">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="b4d0c-1338">Lägg till stöd för att konfigurera TopLevel WebApplicationFirewall-princip</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1338">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="b4d0c-1339">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1339">New cmdlets added:</span></span>
        - <span data-ttu-id="b4d0c-1340">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1340">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="b4d0c-1341">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1341">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="b4d0c-1342">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1342">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="b4d0c-1343">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1343">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="b4d0c-1344">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1344">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="b4d0c-1345">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1345">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="b4d0c-1346">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1346">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="b4d0c-1347">New-AzApplicationGatewayFirewallPolicy: parametrarna PolicySetting, ManagedRule har lagts till</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1347">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="b4d0c-1348">Stöd för operator för geomatchning har lagts till på CustomRule</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1348">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="b4d0c-1349">Geomatchning har lagts till i operatorn på FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1349">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="b4d0c-1350">Stöd har lagts till för brandväggsprinciperna perListener och perSite</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1350">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="b4d0c-1351">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1351">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="b4d0c-1352">New-AzApplicationGatewayHttpListener: parametrarna FirewallPolicy, FirewallPolicyId har lagts till</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1352">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="b4d0c-1353">New-AzApplicationGatewayPathRuleConfig: parametrarna FirewallPolicy, FirewallPolicyId har lagts till</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1353">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="b4d0c-1354">Åtgärdat så att nödvändigt undernät med namnet AzureBastionSubnet i PSBastion kan vara skiftlägesokänsligt</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1354">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="b4d0c-1355">Stöd för mål-FQDN:er i nätverksregler och översatt FQDN i NAT-regler för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1355">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="b4d0c-1356">Lägg till stöd för resursen RouteTables för IpGroup på den högsta nivån</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1356">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="b4d0c-1357">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1357">New cmdlets added:</span></span>
        - <span data-ttu-id="b4d0c-1358">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1358">New-AzIpGroup</span></span>
        - <span data-ttu-id="b4d0c-1359">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1359">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="b4d0c-1360">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1360">Get-AzIpGroup</span></span>
        - <span data-ttu-id="b4d0c-1361">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1361">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="b4d0c-1362">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1362">Az.ServiceFabric</span></span>
* <span data-ttu-id="b4d0c-1363">Ta bort cmdleten Add-AzServiceFabricApplicationCertificate eftersom det här scenariot omfattas av Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1363">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="b4d0c-1364">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1364">Az.Sql</span></span>
* <span data-ttu-id="b4d0c-1365">Stöd har lagts till för återställning av utelämnade databaser på hanterade instanser.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1365">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="b4d0c-1366">Inaktuella gamla cmdletar för granskning från kod.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1366">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="b4d0c-1367">Tog bort inaktuella alias:</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1367">Removed deprecated aliases:</span></span>
* <span data-ttu-id="b4d0c-1368">Get-AzSqlDatabaseIndexRecommendations (använd Get-AzSqlDatabaseIndexRecommendation istället)</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1368">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="b4d0c-1369">Get-AzSqlDatabaseRestorePoints (använd Get-AzSqlDatabaseRestorePoint istället)</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1369">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="b4d0c-1370">Ta bort cmdleten Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1370">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="b4d0c-1371">Ta bort alias för inaktuella cmdletar för inställningar för utvärdering av säkerhetsrisk</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1371">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="b4d0c-1372">Inaktualisera cmdletar för inställningar för avancerad hotidentifiering</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1372">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="b4d0c-1373">Lägga till cmdletar för att inaktivera och aktivera känslighetsrekommendationer på kolumner i en databas.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1373">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b4d0c-1374">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1374">Az.Storage</span></span>
* <span data-ttu-id="b4d0c-1375">Stöd för att aktivera stora filresurser vid skapande eller uppdatering av lagringskonto</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1375">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="b4d0c-1376">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1376">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="b4d0c-1377">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1377">Set-AzStorageAccount</span></span>
* <span data-ttu-id="b4d0c-1378">När du stänger/hämtar en filreferens kan du hoppa över kontrollen av huruvida indatasökvägen är en filkatalog eller en fil för att undvika problem med objekt som har status DeletePending</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1378">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="b4d0c-1379">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1379">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="b4d0c-1380">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1380">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="b4d0c-1381">2.8.0 – oktober 2019</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1381">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="b4d0c-1382">Allmänt</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1382">General</span></span>
* <span data-ttu-id="b4d0c-1383">AZ. HealthcareApis 1.0.0-version</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1383">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="b4d0c-1384">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1384">Az.Accounts</span></span>
* <span data-ttu-id="b4d0c-1385">Uppdatera telemetri och URL-omskrivning för genererade moduler, korrigera Windows-enhetstester.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1385">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="b4d0c-1386">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1386">Az.ApiManagement</span></span>
* <span data-ttu-id="b4d0c-1387">**Set-AzApiManagementApi** – Tillagt stöd för att uppdatera Api till ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1387">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="b4d0c-1388">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1388">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="b4d0c-1389">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1389">Az.Automation</span></span>
* <span data-ttu-id="b4d0c-1390">Åtgärdade cmdleten New-AzureAutomationSoftwareUpdateConfiguration för parametern för inställning av Linux-omstart.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1390">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="b4d0c-1391">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1391">Az.Batch</span></span>
* <span data-ttu-id="b4d0c-1392">**Get-AzBatchNodeAgentSku** är inaktuell och ersätts av **Get-AzBatchSupportImage** i version 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1392">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b4d0c-1393">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1393">Az.Compute</span></span>
* <span data-ttu-id="b4d0c-1394">Lägg till parametrarna Priority, EvictionPolicy och MaxPrice till cmdletarna New-AzVM och New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1394">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="b4d0c-1395">Korrigera varningsmeddelande och hjälpdokument för cmdletarna Add-AzVMAdditionalUnattendContent och Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1395">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="b4d0c-1396">Åtgärda – skipVmBackup-undantag för virtuella Linux-datorer med hanterade diskar för Set-AzVMDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1396">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="b4d0c-1397">Åtgärda fel i uppdatera krypteringsinställningarna i set-AzVMDiskEncryptionExtension, scenario i två steg.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1397">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b4d0c-1398">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1398">Az.DataFactory</span></span>
* <span data-ttu-id="b4d0c-1399">Lägga till CRUD-kommandon för ADF V2-dataflödet: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow och Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1399">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="b4d0c-1400">Lägger till åtgärdskommandon för ADF V2-dataflödesfelsökningssession: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand och Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1400">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="b4d0c-1401">Uppdatera ADF .Net SDK-versionen till 4.2.0</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1401">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b4d0c-1402">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1402">Az.DataLakeStore</span></span>
* <span data-ttu-id="b4d0c-1403">Korrigera kontovalidering så att konton med ”-” kan skickas utan domän</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1403">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="b4d0c-1404">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1404">Az.HealthcareApis</span></span>
* <span data-ttu-id="b4d0c-1405">PowerShell-versionen har uppdaterats till 1.0.0</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1405">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="b4d0c-1406">Uppdaterade SDK-versionen till 1.0.2</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1406">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="b4d0c-1407">Uppdatera i tester för att referera till en ny SDK-version</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1407">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="b4d0c-1408">Utdatastrukturen har uppdaterats från kapslad till förenklad.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1408">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="b4d0c-1409">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1409">Az.IotHub</span></span>
* <span data-ttu-id="b4d0c-1410">Lägg till ny routningskälla: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1410">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="b4d0c-1411">Mindre felkorrigering: Get-AzIothub returnerar inte subscriptionId</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1411">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="b4d0c-1412">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1412">Az.Monitor</span></span>
* <span data-ttu-id="b4d0c-1413">Nya åtgärdsgruppsmottagare har lagts till för åtgärdsgrupp   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1413">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="b4d0c-1414">Använd vanligt aviseringsschema som är aktiverat för mottagarna.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1414">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="b4d0c-1415">Detta gäller inte för SMS, push för Azure-app, ITSM och röstmottagare</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1415">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="b4d0c-1416">Webhooks har nu stöd för Azure Active Directory-autentisering.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1416">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b4d0c-1417">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1417">Az.Network</span></span>
* <span data-ttu-id="b4d0c-1418">Lägg till ny cmdlet Get-AzAvailableServiceAlias som kan anropas för att hämta de alias som kan användas för tjänstslutpunktsprinciper.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1418">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="b4d0c-1419">Stöd för tillägg av trafikväljare har lagts till i gatewayanslutningar för virtuella nätverk</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1419">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="b4d0c-1420">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1420">New cmdlets added:</span></span>
        - <span data-ttu-id="b4d0c-1421">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1421">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="b4d0c-1422">Cmdletar har uppdaterats med valfri parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1422">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="b4d0c-1423">Lägg till stöd för ESP- och AH-protokoll i konfiguration av nätverkssäkerhetsregler</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1423">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="b4d0c-1424">Uppdaterade cmdletar:</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1424">Updated cmdlets:</span></span>
        - <span data-ttu-id="b4d0c-1425">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1425">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="b4d0c-1426">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1426">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="b4d0c-1427">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1427">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="b4d0c-1428">Förbättra hanteringen av undantag i Cortex-cmdletar</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1428">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="b4d0c-1429">Nya generationer och SKU:er för VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1429">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="b4d0c-1430">Introducera nya generationer för VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1430">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="b4d0c-1431">Introducera nya SKU:er med högt dataflöde för VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1431">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="b4d0c-1432">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1432">Az.RedisCache</span></span>
* <span data-ttu-id="b4d0c-1433">Uppdaterad referensdokumentation för ”set-AzRedisCache” för att inkludera saknade värden för parametern ”size”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1433">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="b4d0c-1434">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1434">Az.Sql</span></span>
* <span data-ttu-id="b4d0c-1435">Lägg till stöd för inställningen Active Directory administratör på den hanterade instansen</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1435">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b4d0c-1436">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1436">Az.Storage</span></span>
* <span data-ttu-id="b4d0c-1437">Uppdatera Lagringsklientbibliotek till 11.1.0</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1437">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="b4d0c-1438">Lista containrar med hanteringsplans-API, kommer att listas med NextPageLink</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1438">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="b4d0c-1439">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1439">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="b4d0c-1440">Lista lagringskonton från prenumerationen, kommer att listas med NextPageLink</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1440">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="b4d0c-1441">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1441">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="b4d0c-1442">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1442">Az.StorageSync</span></span>
* <span data-ttu-id="b4d0c-1443">Åtgärda problemet 9810 i Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1443">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b4d0c-1444">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1444">Az.Websites</span></span>
* <span data-ttu-id="b4d0c-1445">Set-AzWebApp – uppdatering av ASP för en app misslyckades</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1445">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="b4d0c-1446">2.7.0 – september 2019</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1446">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="b4d0c-1447">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1447">Az.ApiManagement</span></span>
* <span data-ttu-id="b4d0c-1448">Uppdatera ”-Format”-parameterbeskrivningen i ”Set-AzApiManagementPolicy”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1448">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="b4d0c-1449">Referenser för den föråldrade cmdleten ”Update-AzApiManagementDeployment” har tagits bort från referensdokumentationen.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1449">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="b4d0c-1450">Använd ”Set-AzApiManagement” i stället.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1450">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="b4d0c-1451">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1451">Az.Automation</span></span>
* <span data-ttu-id="b4d0c-1452">Stavfel har korrigerats i exempel i referensdokumentationen för ”Register-AzAutomationDscNode”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1452">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="b4d0c-1453">Klargörande har lagts till om OS-begränsningar för Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1453">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="b4d0c-1454">Null-referensundantag har korrigerats för -Wait-alternativet i Start-AzAutomationRunbook-cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1454">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b4d0c-1455">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1455">Az.Compute</span></span>
* <span data-ttu-id="b4d0c-1456">Lägg till UploadSizeInBytes-parameter till New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1456">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="b4d0c-1457">Lägg till Incremental-parameter till New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1457">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="b4d0c-1458">Lägg till en funktion för virtuella datorer med låg prioritet:</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1458">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="b4d0c-1459">MaxPrice-, EvictionPolicy- och Priority-parametrar har lagts till i New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1459">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="b4d0c-1460">MaxPrice-parametern har lagts till i New-AzVmssConfig-, Update-AzVM- och Update-AzVmss-cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1460">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="b4d0c-1461">Åtgärda problem med VM-referenser för Get-AzAvailabilitySet-cmdleten när alla tillgänglighetsuppsättningar i prenumerationen visas.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1461">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="b4d0c-1462">Korrigera null-undantaget för Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1462">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="b4d0c-1463">Korrigera VHD-metoden för sökning relativt till slut.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1463">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="b4d0c-1464">Åtgärda UltraSSD-problem för New-AzVM och Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1464">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b4d0c-1465">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1465">Az.DataFactory</span></span>
* <span data-ttu-id="b4d0c-1466">Lägger till 3 nya kommandon för ADF V2 – Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription och Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1466">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="b4d0c-1467">ADF .Net SDK har uppdaterats till 4.1.3</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1467">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="b4d0c-1468">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1468">Az.HDInsight</span></span>
* <span data-ttu-id="b4d0c-1469">Anrop för icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1469">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="b4d0c-1470">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1470">Az.IotHub</span></span>
* <span data-ttu-id="b4d0c-1471">Lägg till stöd för att anropa redundans för en IotHub till den geo-länkade katastrofåterställningsregionen.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1471">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="b4d0c-1472">Lägg till stöd för att hantera meddelandeberikning för en IotHub.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1472">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="b4d0c-1473">Nya cmdlet:ar är:</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1473">New cmdlets are:</span></span>
    - <span data-ttu-id="b4d0c-1474">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1474">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="b4d0c-1475">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1475">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="b4d0c-1476">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1476">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="b4d0c-1477">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1477">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="b4d0c-1478">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1478">Az.Monitor</span></span>
* <span data-ttu-id="b4d0c-1479">Pekar på den senaste Monitor SDK:n, dvs. 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1479">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="b4d0c-1480">Lägger till bakåtkompatibla ändringar i Metrics-cmdletarna, dvs. enhetsuppräkningen stöder flera nya värden.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1480">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="b4d0c-1481">Detta är skrivskyddade cmdletar, så det förekommer inga ändringar i inmatningen för cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1481">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="b4d0c-1482">API-versionen för **ActionGroups**-begäranden är nu **2019-06-01**. Tidigare var den **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1482">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="b4d0c-1483">Test av scenarier har uppdaterats för att anpassas till den här ändringen.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1483">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="b4d0c-1484">Ett nytt obligatoriskt argument har lagts till för konstruktorerna för klasserna **EmailReceiver** och **WebhookReceiver** – ett booleskt värde med namnet **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1484">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="b4d0c-1485">Värdet är för närvarande fast till **false** så att den här icke-bakåtkompatibla ändringen är dold från cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1485">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="b4d0c-1486">**Obs!** Det här är en tillfällig ändring som måste verifieras av Alerts-teamet.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1486">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="b4d0c-1487">Ordningen på argumenten för konstruktorn för klassen **Source** (relaterad till klassen **ScheduledQueryRuleSource**) har ändrats från den tidigare SDK:n.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1487">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="b4d0c-1488">Den här ändringen krävde korrigering av två enhetstest: de kompilerades, men testerna skickades inte.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1488">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="b4d0c-1489">Ordningen på argumenten för konstruktorn för klassen **AlertingAction** (relaterad till klassen **ScheduledQueryRuleSource**) har ändrats från den tidigare SDK:n.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1489">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="b4d0c-1490">Den här ändringen krävde korrigering av två enhetstest: de kompilerades, men testerna skickades inte.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1490">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="b4d0c-1491">Stöd för kriterier för dynamiskt tröskelvärde för måttavisering v2</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1491">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="b4d0c-1492">New-AzMetricAlertRuleV2Criteria: skapar nu även kriterier för dynamiskt tröskelvärde</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1492">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="b4d0c-1493">Add-AzMetricAlertRuleV2: accepterar nu även kriterier för dynamiskt tröskelvärde</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1493">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="b4d0c-1494">Förbättringar i schemalagd frågeregel (SQR)</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1494">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="b4d0c-1495">Cmdletar accepterar ”Location”-parameter i båda formaten, antingen platsen (t.ex. eastus) eller platsens visningsnamn (t.ex. USA, östra)</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1495">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="b4d0c-1496">”Enabled”-parametern illustreras korrekt i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1496">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="b4d0c-1497">Exempel för den valfria parametern ”ActionGroup” har lagts till</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1497">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="b4d0c-1498">Förbättrade hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1498">Overall improved help files</span></span>
* <span data-ttu-id="b4d0c-1499">Åtgärda bugg då omfattningstypen fastställs för ”Set-AzActionRule”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1499">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b4d0c-1500">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1500">Az.Network</span></span>
* <span data-ttu-id="b4d0c-1501">Korrigera felaktigt exempel i referensdokumentationen för ”New-AzApplicationGateway”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1501">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="b4d0c-1502">Lägg till anmärkning i ”Get-AzNetworkWatcherPacketCapture”-referensdokumentationen om hämtning av alla egenskaper för en paketinsamling</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1502">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="b4d0c-1503">Exempel har korrigerats i ”Test-AzNetworkWatcherIPFlow”-referensdokumentationen för korrekt uppräkning av nätverkskort</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1503">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="b4d0c-1504">Förbättrad tolkning av molnundantag för att visa eventuell ytterligare information</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1504">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="b4d0c-1505">Förbättrad tolkning av molnundantag för att hantera ytterligare en typ av SDK-undantag</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1505">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="b4d0c-1506">Felaktig mappning av säkerhetsregelmodeller har korrigerats</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1506">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="b4d0c-1507">Egenskaper har lagts till för nätverksgränssnittet för funktionen Privat IP</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1507">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="b4d0c-1508">Egenskapen ”PrivateEndpoint” har lagts till som en typ av PSResourceId till PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1508">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="b4d0c-1509">Egenskapen ”PrivateLinkConnectionProperties” har lagts till som en typ av PSIpConfigurationConnectivityInformation till PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1509">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="b4d0c-1510">Modellklassen PSIpConfigurationConnectivityInformation har lagts till</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1510">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="b4d0c-1511">ApplicationRuleProtocolType ”mssql” har lagts till för Azure Firewall-resurs</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1511">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="b4d0c-1512">MultiLink-stöd i virtuellt WAN</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1512">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="b4d0c-1513">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1513">New cmdlets</span></span>
        - <span data-ttu-id="b4d0c-1514">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1514">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="b4d0c-1515">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1515">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="b4d0c-1516">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1516">Updated cmdlet:</span></span>
        - <span data-ttu-id="b4d0c-1517">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1517">New-VpnSite</span></span>
        - <span data-ttu-id="b4d0c-1518">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1518">Update-VpnSite</span></span>
        - <span data-ttu-id="b4d0c-1519">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1519">New-VpnConnection</span></span>
        - <span data-ttu-id="b4d0c-1520">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1520">Update-VpnConnection</span></span>
* <span data-ttu-id="b4d0c-1521">Dokument för vissa PowerShell-exempel har korrigerats så att Az-cmdletar används i stället för AzureRM-cmdletar</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1521">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b4d0c-1522">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1522">Az.RecoveryServices</span></span>
* <span data-ttu-id="b4d0c-1523">Uppdatera AzureVMpolicy-objekt med ProtectedItemsCount-attribut</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1523">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="b4d0c-1524">Ytterligare tester har lagts till för VM-princip och återställning av ursprungligt lagringskonto</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1524">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="b4d0c-1525">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1525">Az.Resources</span></span>
* <span data-ttu-id="b4d0c-1526">Åtgärda fel där det inte gick att anropa New-AzRoleAssignment utan parametern Scope.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1526">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="b4d0c-1527">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1527">Az.ServiceFabric</span></span>
* <span data-ttu-id="b4d0c-1528">Stavfel har korrigerats i exempel för ”Update-AzServiceFabricReliability”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1528">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="b4d0c-1529">Lägger till nya cmdletar för att hantera program och tjänster:</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1529">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="b4d0c-1530">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1530">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="b4d0c-1531">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1531">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="b4d0c-1532">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1532">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="b4d0c-1533">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1533">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="b4d0c-1534">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1534">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="b4d0c-1535">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1535">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="b4d0c-1536">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1536">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="b4d0c-1537">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1537">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="b4d0c-1538">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1538">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="b4d0c-1539">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1539">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="b4d0c-1540">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1540">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="b4d0c-1541">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1541">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="b4d0c-1542">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1542">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="b4d0c-1543">Service Fabric SDK har uppgraderats till version 1.2.0 som använder Service Fabric-resursprovidern med API-version 2019-03-01.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1543">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="b4d0c-1544">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1544">Az.SignalR</span></span>
* <span data-ttu-id="b4d0c-1545">Lägg till Update-, Restart-, CheckNameAvailability- och GetUsage-cmdletar</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1545">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="b4d0c-1546">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1546">Az.Sql</span></span>
* <span data-ttu-id="b4d0c-1547">Uppdatera exempel i referensdokumentationen för ”Get-AzSqlElasticPool”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1547">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="b4d0c-1548">vCore-exempel för att skapa en elastisk pool (New-AzSqlElasticPool) har lagts till.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1548">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="b4d0c-1549">Ta bort verifieringen av EmailAddresses och kontrollen som bekräftar att EmailAdmins inte är falskt när EmailAddresses är tomt i Set-AzSqlServerAdvancedThreatProtectionPolicy och Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1549">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="b4d0c-1550">Server-/databasgranskningsinställningar kan tas bort när det finns flera diagnostikinställningar som aktiverar granskningskategorin.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1550">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="b4d0c-1551">Åtgärda verifiering av e-postadresser i flera Sql Vulnerability Assessment-cmdletar (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting och Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1551">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b4d0c-1552">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1552">Az.Storage</span></span>
* <span data-ttu-id="b4d0c-1553">Exempel i referensdokumentationen för ”Get-AzStorageAccountKey” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1553">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="b4d0c-1554">Vid upp- och nedladdning av en Azure-fil kan SMB-egenskaperna för källfilen (t.ex. filattribut, tidpunkten då filen skapades och tidpunkten för den senaste skrivningen) sparas i målfilen</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1554">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="b4d0c-1555">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1555">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="b4d0c-1556">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1556">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="b4d0c-1557">Korrigera problem med uppladdningen av blockblob med egenskaper/metadata för ImmutabilityPolicy i containrar.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1557">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="b4d0c-1558">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1558">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="b4d0c-1559">Stöd för hantering av Azure-filresurser med API för hanteringsplan</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1559">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="b4d0c-1560">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1560">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="b4d0c-1561">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1561">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="b4d0c-1562">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1562">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="b4d0c-1563">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1563">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b4d0c-1564">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1564">Az.Websites</span></span>
* <span data-ttu-id="b4d0c-1565">Åtgärdar problemet där webapp-taggar togs bort när appen migrerades till nya ASP</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1565">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="b4d0c-1566">Åtgärda Publish-AzureWebapp så att det fungerar i Linux och Windows</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1566">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="b4d0c-1567">Uppdatera exempel i ”Get-AzWebAppPublishingProfile”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1567">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="b4d0c-1568">2.6.0 – augusti 2019</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1568">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="b4d0c-1569">Allmänt</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1569">General</span></span>
* <span data-ttu-id="b4d0c-1570">Åtgärdade diverse skrivfel i flera moduler</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1570">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="b4d0c-1571">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1571">Az.Accounts</span></span>
* <span data-ttu-id="b4d0c-1572">Stöd för användartilldelat MSI i Azure Functions-autentisering (#9479)</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1572">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="b4d0c-1573">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1573">Az.Aks</span></span>
* <span data-ttu-id="b4d0c-1574">Åtgärda problem med utdata för "Get-AzAks"</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1574">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="b4d0c-1575">Mer information här: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1575">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="b4d0c-1576">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1576">Az.ApiManagement</span></span>
* <span data-ttu-id="b4d0c-1577">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1577">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="b4d0c-1578">Uppdatera .net-NuGet-versionen, som inte tillämpar begränsningar för productId, apiId och userId</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1578">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="b4d0c-1579">**Get-AzApiManagementProduct** – Lade till stöd för frågekörning mot produkter via API.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1579">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="b4d0c-1580">**New-AzApiManagementApiRevision** – Korrigering för problem där ApiRevisionDescription inte angavs vid skapande av ny API-revision https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1580">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="b4d0c-1581">Åtgärdade skrivfel i modellen "PsApiManagementOAuth2AuthrozationServer" till "PsApiManagementOAuth2AuthorizationServer"</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1581">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="b4d0c-1582">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1582">Az.Batch</span></span>
* <span data-ttu-id="b4d0c-1583">Åtgärdade skrivfel i hjälpmeddelande och dokumentation till att skriva Windows med versaler</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1583">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="b4d0c-1584">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1584">Az.Cdn</span></span>
* <span data-ttu-id="b4d0c-1585">Åtgärdade skrivfel i CDN-modulens konverteringshjälp</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1585">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b4d0c-1586">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1586">Az.Compute</span></span>
* <span data-ttu-id="b4d0c-1587">Lägg till VmssId i New-AzVMConfig-cmdleten</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1587">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="b4d0c-1588">Lägg till parametrarna TerminateScheduledEvents och TerminateScheduledEventNotBeforeTimeoutInMinutes i New-AzVmssConfig och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1588">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="b4d0c-1589">Lägg till egenskapen HyperVGeneration till avbildningsobjekt för virtuell dator</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1589">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="b4d0c-1590">Lägg till funktioner för Host och HostGroup</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1590">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="b4d0c-1591">Nya cmdletar:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1591">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="b4d0c-1592">HostId-parametern läggs till i New-AzVMConfig och New-AzVM</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1592">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="b4d0c-1593">Uppdatera exempel i "Invoke-AzVMRunCommand"-dokumentationen till att använda rätt parameternamn</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1593">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="b4d0c-1594">Uppdatera "-VolumeType"-beskrivningen i referensdokumentationen för "set-AzVMDiskEncryptionExtension" och "set-AzVmssDiskEncryptionExtension"</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1594">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b4d0c-1595">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1595">Az.DataFactory</span></span>
* <span data-ttu-id="b4d0c-1596">Åtgärda skrivfel till att använda versaler för "Windows" i "New-AzDataFactoryEncryptValue"-dokumentationen</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1596">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="b4d0c-1597">Uppdaterade ADF .Net SDK-versionen till 4.1.2</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1597">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="b4d0c-1598">Lägg till parametrarna "DataProxyIntegrationRuntimeName", "DataProxyStagingLinkedServiceName" och "DataProxyStagingPath" för "Set-AzureRmDataFactoryV2IntegrationRuntime"-cmd för att aktivera konfiguration av lokalt installerad integrationskörning som en proxy för SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1598">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="b4d0c-1599">Uppdaterade PSTriggerRun till att visa utlöst pipeline, meddelande och egenskaper samt PSActivityRun till att visa aktivitetstypen</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1599">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b4d0c-1600">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1600">Az.DataLakeStore</span></span>
* <span data-ttu-id="b4d0c-1601">Korrigering av frysning av Get-DataLakeStoreDeletedItem för fel eller fjärrundantag.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1601">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="b4d0c-1602">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1602">Az.EventHub</span></span>
* <span data-ttu-id="b4d0c-1603">Korrigering av problem #9658 : Skrivfel i parametern VirtualNteworkRule i Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1603">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="b4d0c-1604">Korrigering av problem #9558 : Set-AzEventHubNamespace använder PATCH i stället för PUT</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1604">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="b4d0c-1605">lade till parametern EnableKafka i Set-AzEventHubNamespace-cmdleten</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1605">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="b4d0c-1606">Korrigering av problem #9786 : kan inte skapa en regel med Endast lyssna-behörighet</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1606">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="b4d0c-1607">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1607">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="b4d0c-1608">Åtgärdade skrivfel i dokumentation där "Azure" skrevs helt med gemener</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1608">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="b4d0c-1609">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1609">Az.Monitor</span></span>
* <span data-ttu-id="b4d0c-1610">Åtgärdade felaktigt parameternamn i hjälpdokumentationen</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1610">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b4d0c-1611">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1611">Az.Network</span></span>
* <span data-ttu-id="b4d0c-1612">Uppdaterade New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1612">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="b4d0c-1613">Gjorde parametern "PublicIpAddress" inaktuell eftersom den aldrig används på serversidan.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1613">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="b4d0c-1614">Lade till den valfria parametern "Primary", som anger huruvida den aktuella IP-konfigurationen är den primära.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1614">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="b4d0c-1615">Förbättrade hanteringen av felundantag för begärande från SDK – åtgärdar problemet att tidigare SDK-undantag inte hanteras på rätt sätt, vilket leder till att viktig felinformation inte visas</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1615">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="b4d0c-1616">Justerade valideringslogiken för IPv6-IP-prefix till att kontrollera korrekt IPv6-prefixlängd.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1616">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="b4d0c-1617">Uppdaterade Get-AzVirtualNetworkSubnetConfig: Lade till parameter som anges till get av undernätets resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1617">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="b4d0c-1618">Uppdaterade beskrivningen av parametern Location för AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1618">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="b4d0c-1619">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1619">Az.OperationalInsights</span></span>
* <span data-ttu-id="b4d0c-1620">Uppdaterade dokumentation för "New-AzOperationalInsightsLinuxSyslogDataSource"</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1620">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="b4d0c-1621">Lade till exempel</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1621">Added example</span></span>
    - <span data-ttu-id="b4d0c-1622">Uppdaterade beskrivningen av parametern "-Name"</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1622">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="b4d0c-1623">Lade till ett exempel för New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1623">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="b4d0c-1624">Ändrade beskrivningen av parametern -Name för New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1624">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b4d0c-1625">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1625">Az.RecoveryServices</span></span>
* <span data-ttu-id="b4d0c-1626">Uppdatera "Get-AzRecoveryServicesBackupJobDetail.md"</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1626">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="b4d0c-1627">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1627">Az.Resources</span></span>
* <span data-ttu-id="b4d0c-1628">Lägg till stöd för den nya API-versionen från 2019-05-10 för Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1628">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="b4d0c-1629">Lägg till stöd för "copy.count = 0" för variabler, resurser och egenskaper</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1629">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="b4d0c-1630">Resurser med "condition = false" eller "copy.count = 0" tas bort i complete-läget</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1630">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="b4d0c-1631">Lägg till ett exempel på tilldelning av princip på prenumerationsnivå i hjälpdokumentationen</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1631">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="b4d0c-1632">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1632">Az.ServiceBus</span></span>
* <span data-ttu-id="b4d0c-1633">Korrigering av problem #9658 : Skrivfel i parametern VirtualNetworkRule i set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1633">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="b4d0c-1634">Korrigering av problem #9786 : kan inte skapa en regel med Endast lyssna-behörighet</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1634">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="b4d0c-1635">Lade till det nya kommandot "Test-AzServiceBusNameAvailability" för att kontrollera namntillgängligheten för kö och ämne</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1635">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="b4d0c-1636">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1636">Az.ServiceFabric</span></span>
* <span data-ttu-id="b4d0c-1637">Åtgärda buggar med tillägg av nodtyps-cmdlet:</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1637">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="b4d0c-1638">NullReferenceException-bugg när resursgrupp hade annan vmss som inte är relaterad till Service Fabric-klustret.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1638">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="b4d0c-1639">Åtgärdar problemet: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1639">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="b4d0c-1640">Åtgärda bugg där cmdleten misslyckades om virtualNetwork var i en annan resursgrupp än klustret.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1640">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="b4d0c-1641">Åtgärdar problemet: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1641">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="b4d0c-1642">AzServiceFabricApplicationCertificate-cmdleten görs inaktuell</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1642">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="b4d0c-1643">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1643">Az.Sql</span></span>
* <span data-ttu-id="b4d0c-1644">Uppdatera dokumentation om gamla gransknings-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1644">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b4d0c-1645">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1645">Az.Storage</span></span>
* <span data-ttu-id="b4d0c-1646">Uppdatera hjälpen för Get/Close-AzStorageFileHandle genom att lägga till fler scenarier i cmdlet-exempel och uppdatera parameterbeskrivningar</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1646">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="b4d0c-1647">Stöd för StandardBlobTier i uppladdningsblob och kopieringsblob</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1647">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="b4d0c-1648">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1648">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="b4d0c-1649">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1649">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="b4d0c-1650">Stöd för rehydratiseringsprioritet i kopieringsblob</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1650">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="b4d0c-1651">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1651">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b4d0c-1652">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1652">Az.Websites</span></span>
* <span data-ttu-id="b4d0c-1653">Lägg till klargöranden gällande parametern -AppSettings i Set-AzWebApp och Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1653">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="b4d0c-1654">2.5.0 – July 2019</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1654">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b4d0c-1655">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1655">Az.Accounts</span></span>
* <span data-ttu-id="b4d0c-1656">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1656">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="b4d0c-1657">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1657">Az.ApplicationInsights</span></span>
* <span data-ttu-id="b4d0c-1658">Korrigera skrivfel i exempel i dokumentationen för Remove-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1658">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="b4d0c-1659">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1659">Az.Automation</span></span>
* <span data-ttu-id="b4d0c-1660">Korrigera skrivfel i resurssträng</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1660">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="b4d0c-1661">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1661">Az.CognitiveServices</span></span>
* <span data-ttu-id="b4d0c-1662">Stöd för NetworkRuleSet har lagts till.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1662">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b4d0c-1663">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1663">Az.Compute</span></span>
* <span data-ttu-id="b4d0c-1664">Lägg till saknade egenskaper (ComputerName, OsName, OsVersion och HyperVGeneration) för visningsobjekt i den virtuella datorinstansen.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1664">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="b4d0c-1665">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1665">Az.ContainerRegistry</span></span>
* <span data-ttu-id="b4d0c-1666">Åtgärda skrivfel i Remove-AzContainerRegistryReplication för parametern Replication</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1666">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="b4d0c-1667">Mer information finns här: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1667">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b4d0c-1668">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1668">Az.DataFactory</span></span>
* <span data-ttu-id="b4d0c-1669">ADF .Net SDK-versionen har uppdaterats till 4.1.0</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1669">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="b4d0c-1670">Korrigera skrivfel i dokumentationen för Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1670">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="b4d0c-1671">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1671">Az.EventHub</span></span>
* <span data-ttu-id="b4d0c-1672">Ny cmmdlet har lagts till för att skapa SAS-token: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1672">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="b4d0c-1673">verifierings- och felmeddelande har lagts till för authorizationrules-rättigheter om endast "hantera" har tilldelats</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1673">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="b4d0c-1674">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1674">Az.KeyVault</span></span>
* <span data-ttu-id="b4d0c-1675">Stöd har lagts till för att ange KeySize för certifikatprinciper</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1675">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="b4d0c-1676">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1676">Az.LogicApp</span></span>
* <span data-ttu-id="b4d0c-1677">Korrigering för Get-AzIntegrationAccountMap för att lista alla mappningstyper</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1677">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="b4d0c-1678">Ny MapType-parameter har lagts till för filtrering</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1678">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="b4d0c-1679">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1679">Az.ManagedServices</span></span>
* <span data-ttu-id="b4d0c-1680">Stöd för API-versionen 2019-06-01 (GA) har lagts till</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1680">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b4d0c-1681">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1681">Az.Network</span></span>
* <span data-ttu-id="b4d0c-1682">Lägg till stöd för privat slutpunkt och privat länktjänst</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1682">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="b4d0c-1683">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1683">New cmdlets</span></span>
        - <span data-ttu-id="b4d0c-1684">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1684">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="b4d0c-1685">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1685">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="b4d0c-1686">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1686">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="b4d0c-1687">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1687">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="b4d0c-1688">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1688">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="b4d0c-1689">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1689">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="b4d0c-1690">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1690">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="b4d0c-1691">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1691">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="b4d0c-1692">Nedanstående kommandon för funktionen har uppdaterats: Flaggan PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies på undernätet i VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1692">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="b4d0c-1693">Uppdaterade New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1693">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="b4d0c-1694">Valfri parameter har lagts till – PrivateEndpointNetworkPoliciesFlag som konfigurerar huruvida nätverksprinciper ska tillämpas på en privat slutpunkt i det här undernätet.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1694">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="b4d0c-1695">Valfri parameter har lagts till – PrivateLinkServiceNetworkPoliciesFlag som konfigurerar huruvida nätverksprinciper ska tillämpas på en privat länktjänst i det här undernätet.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1695">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="b4d0c-1696">AzPrivateLinkService för cmdlet-parametern ServiceName har bytt namn till Name med aliaset ServiceName för bakåtkompatibilitet</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1696">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="b4d0c-1697">Aktivera ICMP-protokoll för konfiguration av nätverkssäkerhetsregler</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1697">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="b4d0c-1698">Uppdaterade cmdletar</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1698">Updated cmdlets</span></span>
        - <span data-ttu-id="b4d0c-1699">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1699">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="b4d0c-1700">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1700">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="b4d0c-1701">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1701">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="b4d0c-1702">Lägg till ConnectionProtocolType (Ikev1/Ikev2) som en konfigurerbar parameter för New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1702">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="b4d0c-1703">Lägg till PrivateIpAddressVersion i LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1703">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="b4d0c-1704">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1704">Updated cmdlet:</span></span>
        - <span data-ttu-id="b4d0c-1705">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1705">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="b4d0c-1706">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1706">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="b4d0c-1707">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1707">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="b4d0c-1708">Uppdatering av Application Gateway-kommandot New-AzApplicationGatewayProbeConfig för stöd av anpassad port i Probe</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1708">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="b4d0c-1709">Uppdaterade New-AzApplicationGatewayProbeConfig: Den valfria parametern Port som används för avsökning i serverdelen har lagts till.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1709">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="b4d0c-1710">Denna parameter gäller för SKU:erna Standard_V2 och WAF_V2.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1710">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="b4d0c-1711">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1711">Az.OperationalInsights</span></span>
* <span data-ttu-id="b4d0c-1712">Uppdaterade standardversionen för sparade sökningar till 1.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1712">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="b4d0c-1713">Åtgärdade hantering av anpassad log null regex</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1713">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b4d0c-1714">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1714">Az.RecoveryServices</span></span>
* <span data-ttu-id="b4d0c-1715">Uppdatera Get-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1715">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="b4d0c-1716">Uppdatera Get-AzRecoveryServicesBackupContainer.md</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1716">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="b4d0c-1717">Uppdatera Get-AzRecoveryServicesVault.md</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1717">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="b4d0c-1718">Uppdatera Wait-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1718">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="b4d0c-1719">Uppdatera Set-AzRecoveryServicesVaultContext.md</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1719">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="b4d0c-1720">Uppdatera Get-AzRecoveryServicesBackupItem.md</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1720">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="b4d0c-1721">Uppdatera Get-AzRecoveryServicesBackupRecoveryPoint.md</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1721">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="b4d0c-1722">Uppdatera Restore-AzRecoveryServicesBackupItem.md</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1722">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="b4d0c-1723">Uppdaterat tjänstanrop för avregistrering av container för Azure-filresurs</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1723">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="b4d0c-1724">Uppdatera Set-AzRecoveryServicesAsrAlertSetting.md</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1724">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="b4d0c-1725">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1725">Az.Resources</span></span>
- <span data-ttu-id="b4d0c-1726">Ta bort den cmdlet som saknas och som refereras i dokumentationen till New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1726">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="b4d0c-1727">Princip-cmdletar har uppdaterats så att de använder den nya API-versionen 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1727">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="b4d0c-1728">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1728">Az.ServiceBus</span></span>
* <span data-ttu-id="b4d0c-1729">Ny cmmdlet har lagts till för att skapa SAS-token: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1729">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="b4d0c-1730">verifierings- och felmeddelande har lagts till för authorizationrules-rättigheter om endast "hantera" har tilldelats</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1730">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="b4d0c-1731">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1731">Az.Sql</span></span>
* <span data-ttu-id="b4d0c-1732">Åtgärda saknade exempel för Set-AzSqlDatabaseSecondary cmdlet</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1732">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="b4d0c-1733">Åtgärda angivna återkommande genomsökningar för bedömning av säkerhetsrisk utan angivna e-postadresser</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1733">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="b4d0c-1734">Korrigera ett skrivfel i ett varningsmeddelande.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1734">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b4d0c-1735">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1735">Az.Storage</span></span>
* <span data-ttu-id="b4d0c-1736">Uppdatera exempel i referensdokumentationen för Get-AzStorageAccount så att rätt parameternamn används</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1736">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="b4d0c-1737">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1737">Az.StorageSync</span></span>
* <span data-ttu-id="b4d0c-1738">Lägger till cmdleten Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1738">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="b4d0c-1739">Åtgärda problem 9551 så att TierFilesOlderThanDays föredras</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1739">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b4d0c-1740">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1740">Az.Websites</span></span>
* <span data-ttu-id="b4d0c-1741">Åtgärdar ett fel där vissa SiteConfig-egenskaper inte returnerades av Get-AzWebApp och Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1741">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="b4d0c-1742">Lägger till en ny platsparameter för Get-AzDeletedWebApp och Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1742">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="b4d0c-1743">Åtgärdar ett fel i kloning av webbapp-platser som använder New-AzWebApp-IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1743">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="b4d0c-1744">2.4.0 – juli 2019</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1744">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b4d0c-1745">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1745">Az.Accounts</span></span>
* <span data-ttu-id="b4d0c-1746">Lägg till stöd för profil-cmdletar</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1746">Add support for profile cmdlets</span></span>
* <span data-ttu-id="b4d0c-1747">Lägg till stöd för miljöer och dataplaner i genererade cmdletar</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1747">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="b4d0c-1748">Åtgärda bugg där fel slutpunkt i vissa fall användes för cmdletar för dataplaner i Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1748">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="b4d0c-1749">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1749">Az.Advisor</span></span>
* <span data-ttu-id="b4d0c-1750">GA-version av Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1750">GA release of Az.Advisor</span></span>
* <span data-ttu-id="b4d0c-1751">Den här modulen ingår nu som en del av `Az`-sammanslagningsmodulen</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1751">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="b4d0c-1752">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1752">Az.ApiManagement</span></span>
* <span data-ttu-id="b4d0c-1753">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1753">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="b4d0c-1754">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1754">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="b4d0c-1755">Stöd för att fråga prenumerationer efter användare och produkt har lagts till</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1755">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="b4d0c-1756">Stöd för att fråga med hjälp av omfång ”/”, ”/apis”, ”/apis/echo-api” har lagts till</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1756">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="b4d0c-1757">Korrigering av problem https://github.com/Azure/azure-powershell/issues/9307 och https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1757">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="b4d0c-1758">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1758">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="b4d0c-1759">Stöd för att ange ”ApiVersion” och ”ApiVersionSetId” när API:er importeras har lagts till</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1759">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="b4d0c-1760">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1760">Az.Automation</span></span>
* <span data-ttu-id="b4d0c-1761">Bugg med cmdleten Set-AzAutomationConnectionFieldValue för att hantera strängvärde har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1761">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b4d0c-1762">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1762">Az.Compute</span></span>
* <span data-ttu-id="b4d0c-1763">Lägg till parametern HyperVGeneration i New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1763">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b4d0c-1764">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1764">Az.DataFactory</span></span>
* <span data-ttu-id="b4d0c-1765">Uppdaterar utdata från ADF-cmdletar som hämtar aktivitetskörningar, hämtar pipelinekörningar och hämtar utlösarkörningar för stöd för Select-Object-pipe.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1765">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="b4d0c-1766">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1766">Az.EventGrid</span></span>
* <span data-ttu-id="b4d0c-1767">Korrigera stavfel i dokumentation om ”New-AzEventGridSubscription”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1767">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="b4d0c-1768">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1768">Az.IotHub</span></span>
* <span data-ttu-id="b4d0c-1769">Lägg till stöd för att återskapa principnycklar för auktorisering.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1769">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b4d0c-1770">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1770">Az.Network</span></span>
* <span data-ttu-id="b4d0c-1771">”RoutingPreference” har lagts till i offentliga IP-taggar</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1771">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="b4d0c-1772">Förbättra exempel för referensdokumentation om ”Get-AzNetworkServiceTag”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1772">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="b4d0c-1773">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1773">Az.PolicyInsights</span></span>
* <span data-ttu-id="b4d0c-1774">Åtgärda problem med null-referens i Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1774">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="b4d0c-1775">Mer information här: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1775">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="b4d0c-1776">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1776">Az.OperationalInsights</span></span>
* <span data-ttu-id="b4d0c-1777">Modellen för CustomLog-datakälla som returneras i Get-AzOperationalInsightsDataSource har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1777">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b4d0c-1778">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1778">Az.RecoveryServices</span></span>
* <span data-ttu-id="b4d0c-1779">Kommandot get-policy för IaaSVM:er har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1779">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="b4d0c-1780">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1780">Az.Resources</span></span>
    - <span data-ttu-id="b4d0c-1781">Korrigera hjälptext för den översta parametern i Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1781">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="b4d0c-1782">Lägg till växlingsstöd på klientsidan för Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1782">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="b4d0c-1783">Lägg till nya parametrar för Set-AzPolicyAssignment, -PolicyParameters och -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1783">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="b4d0c-1784">En mängd dokument- och exempeluppdateringar för Policy-cmdletar</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1784">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="b4d0c-1785">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1785">Az.ServiceBus</span></span>
* <span data-ttu-id="b4d0c-1786">Korrigering av problem #4938 – New-AzureRmServiceBusQueue returnerar BadRequest vid konfiguration av MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1786">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="b4d0c-1787">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1787">Az.Sql</span></span>
* <span data-ttu-id="b4d0c-1788">Lägg till cmdletar för instansredundansgrupper från förhandsversion till offentlig version</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1788">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="b4d0c-1789">Stöd för granskning för Azure SQL Server\Database med nya cmdletar.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1789">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="b4d0c-1790">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1790">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="b4d0c-1791">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1791">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="b4d0c-1792">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1792">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="b4d0c-1793">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1793">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="b4d0c-1794">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1794">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="b4d0c-1795">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1795">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="b4d0c-1796">Ta bort begränsningar för e-post från inställningarna för sårbarhetsbedömning</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1796">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b4d0c-1797">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1797">Az.Storage</span></span>
* <span data-ttu-id="b4d0c-1798">Ändra två parametrar ”-IndexDocument” och ”-ErrorDocument404Path” från ”krävs” till ”valfri” i cmdlet:</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1798">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="b4d0c-1799">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1799">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="b4d0c-1800">Uppdatera hjälpen för Get-AzStorageBlobContent genom att lägga till ett exempel</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1800">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="b4d0c-1801">Visa mer felinformation när cmdleten misslyckas med StorageException</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1801">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="b4d0c-1802">Stöd för att skapa eller uppdatera lagringskonto med Azure Files AAD DS-autentisering</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1802">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="b4d0c-1803">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1803">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="b4d0c-1804">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1804">Set-AzStorageAccount</span></span>
* <span data-ttu-id="b4d0c-1805">Stöd för att lista eller stänga filreferenser för en filresurs, filkatalog eller en fil</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1805">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="b4d0c-1806">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1806">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="b4d0c-1807">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1807">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="b4d0c-1808">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1808">Az.StorageSync</span></span>
* <span data-ttu-id="b4d0c-1809">Den här modulen ingår nu som en del av `Az`-sammanslagningsmodulen</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1809">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="b4d0c-1810">2.3.2 – juni 2019</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1810">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b4d0c-1811">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1811">Az.Accounts</span></span>
* <span data-ttu-id="b4d0c-1812">Åtgärda bugg med felaktiga webbadresser som i vissa fall användes för Functions-anrop</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1812">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="b4d0c-1813">Mer information här: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1813">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="b4d0c-1814">Åtgärda problem med alias från AzureRM i Az-cmdletar</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1814">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="b4d0c-1815">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1815">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="b4d0c-1816">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1816">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b4d0c-1817">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1817">Az.Compute</span></span>
* <span data-ttu-id="b4d0c-1818">Parameteruppsättningarna New-AzVm och New-AzVmss accepterar nu parametern ”ProximityPlacementGroup”.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1818">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="b4d0c-1819">Stavfel i referensdokumentationen för ”New-AzVM” har korrigerats</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1819">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="b4d0c-1820">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1820">Az.Dns</span></span>
* <span data-ttu-id="b4d0c-1821">Stavfel i hjälpexempel för ”Set-AzDnsZone” har korrigerats.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1821">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="b4d0c-1822">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1822">Az.EventGrid</span></span>
* <span data-ttu-id="b4d0c-1823">Har uppdaterats för att använda API-versionen 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1823">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="b4d0c-1824">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1824">New cmdlets:</span></span>
    - <span data-ttu-id="b4d0c-1825">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1825">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="b4d0c-1826">Skapar en ny Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1826">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="b4d0c-1827">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1827">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="b4d0c-1828">Hämtar information om en Event Grid-domän eller hämtar en lista med alla Event Grid-domäner i den aktuella Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1828">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="b4d0c-1829">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1829">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="b4d0c-1830">Tar bort en Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1830">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="b4d0c-1831">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1831">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="b4d0c-1832">Återskapar nyckeln för delad åtkomst för en Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1832">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="b4d0c-1833">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1833">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="b4d0c-1834">Hämtar de nycklar för delad åtkomst som används för att publicera händelser till en Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1834">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="b4d0c-1835">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1835">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="b4d0c-1836">Skapar ett nytt Azure Event Grid-domänämne.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1836">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="b4d0c-1837">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1837">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="b4d0c-1838">Hämtar information om ett Event Grid-domänämne eller hämtar en lista med alla Event Grid-domänämnen under en specifik Event Grid-domän i nuvarande Azure</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1838">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="b4d0c-1839">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1839">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="b4d0c-1840">Tar bort ett befintligt Azure Event Grid-domänämne.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1840">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="b4d0c-1841">Uppdaterade cmdletar:</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1841">Updated cmdlets:</span></span>
    - <span data-ttu-id="b4d0c-1842">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1842">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="b4d0c-1843">Lägg till nya obligatoriska parametrar för att stödja piping för den nya Event Grid-domänen och Event Grid-domänämnet för att göra det möjligt att skapa nya händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1843">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="b4d0c-1844">Lägg till nya obligatoriska parametrar för att ange det nya Event Grid-domännamnet och/eller namnet på Event Grid-domänämnet för att göra det möjligt att skapa nya händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1844">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="b4d0c-1845">Lägg till ny parameteruppsättningar för domäner och domänämnen för att göra det möjligt att återanvända befintliga parametrar (t.ex. EndPointType, SubjectBeginsWith osv).</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1845">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="b4d0c-1846">Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1846">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="b4d0c-1847">Förfallodatum för händelseprenumeration</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1847">Event subscription expiration date,</span></span>
            - <span data-ttu-id="b4d0c-1848">Avancerade filterparametrar.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1848">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="b4d0c-1849">Lägg till ny uppräkning för servicebusqueue som mål.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1849">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="b4d0c-1850">Tillåt inte användning av ”Alla” i alternativet -IncludedEventType och ersätt det med</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1850">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="b4d0c-1851">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1851">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="b4d0c-1852">Lägg till ny valfria parametrar (Top, ODataQuery och NextLink) för att stödja sidnumrering och filtrering av resultat.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1852">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="b4d0c-1853">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1853">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="b4d0c-1854">Lägg till nya obligatoriska parametrar för att stödja piping för en Event Grid-domän och Event Grid-domänämnen för att göra det möjligt att ta bort befintliga händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1854">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="b4d0c-1855">Lägg till nya obligatoriska parametrar för att ange Event Grid-domännamnet och/eller namnet på Event Grid-domänämnet för att göra det möjligt att ta bort befintliga händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1855">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="b4d0c-1856">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1856">Az.FrontDoor</span></span>
* <span data-ttu-id="b4d0c-1857">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1857">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="b4d0c-1858">Lägg till stöd för transformeringar och nytt värde för automatisk komplettering för operatorer (RegEx)</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1858">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="b4d0c-1859">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1859">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="b4d0c-1860">Lägg till nya värden för automatisk komplettering</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1860">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b4d0c-1861">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1861">Az.Network</span></span>
* <span data-ttu-id="b4d0c-1862">Lägg till stöd för resurs för virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1862">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="b4d0c-1863">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1863">New cmdlets</span></span>
        - <span data-ttu-id="b4d0c-1864">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1864">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="b4d0c-1865">Lägg till AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1865">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="b4d0c-1866">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1866">New cmdlets</span></span>
        - <span data-ttu-id="b4d0c-1867">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1867">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="b4d0c-1868">Lägg till PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1868">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="b4d0c-1869">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1869">New cmdlets</span></span>
        - <span data-ttu-id="b4d0c-1870">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1870">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="b4d0c-1871">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1871">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="b4d0c-1872">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1872">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="b4d0c-1873">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1873">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="b4d0c-1874">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1874">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="b4d0c-1875">Lägg till PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1875">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="b4d0c-1876">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1876">New cmdlets</span></span>
        - <span data-ttu-id="b4d0c-1877">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1877">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="b4d0c-1878">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1878">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="b4d0c-1879">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1879">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="b4d0c-1880">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1880">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="b4d0c-1881">Nedanstående kommandon för funktionen har uppdaterats: Flaggan UseLocalAzureIpAddress på VpnConnection</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1881">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="b4d0c-1882">New-AzVpnConnection har uppdaterats: Den valfria parametern -UseLocalAzureIpAddress har lagts till för att visa att en lokal IP-adress i Azure ska användas som källadress när anslutningen initieras.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1882">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="b4d0c-1883">Set-AzVpnConnection har uppdaterats: Den valfria parametern -UseLocalAzureIpAddress har lagts till för att visa att en lokal IP-adress i Azure ska användas som källadress när anslutningen initieras.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1883">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="b4d0c-1884">Det skrivskyddade fältet PeeredConnections har lagts till i ExpressRoute-peering.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1884">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="b4d0c-1885">Det skrivskyddade fältet GlobalReachEnabled har lagts till i ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1885">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="b4d0c-1886">Ett attribut för icke-bakåtkompatibla ändringar har lagts till för att lyfta fram utfasning av fältet AllowGlobalReach i modellen ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1886">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="b4d0c-1887">Problem 8756 har åtgärdats: Fel vid användning av TargetListenerID med AzApplicationGatewayRedirectConfiguration-cmdletar</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1887">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="b4d0c-1888">En bugg i New-AzApplicationGatewayPathRuleConfig som gjorde att regeluppsättningen för att återskapa inte kunde anges har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1888">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="b4d0c-1889">Visningen av VirtualNetworkTaps i NetworkInterfaceIpConfiguration har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1889">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="b4d0c-1890">Cortex Get-cmdletar för att visa en lista med alla delar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1890">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="b4d0c-1891">Funktionen för att skapa VirtualHub-referenser för ExpressRouteGateways och VpnGateway har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1891">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="b4d0c-1892">Stöd för tillgänglighetszoner i AzureFirewall och NatGateway har lagts till</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1892">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="b4d0c-1893">Cmdleten Get-AzNetworkServiceTag har lagts till</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1893">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="b4d0c-1894">Lägg till stöd för flera offentliga IP-adresser för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1894">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="b4d0c-1895">Cmdleten New-AzFirewall har uppdaterats:</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1895">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="b4d0c-1896">Parametern -PublicIpAddress som accepterar ett eller flera offentliga IP-adressobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1896">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="b4d0c-1897">Parametern -VirtualNetwork som accepterar ett virtuellt nätverksobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1897">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="b4d0c-1898">Metoderna AddPublicIpAddress och RemovePublicIpAddress har lagts till på brandväggsobjekt – dessa accepterar ett offentligt IP-adressobjekt som indata</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1898">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="b4d0c-1899">Inaktuella parametrar -PublicIpName och -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1899">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="b4d0c-1900">Nedanstående kommandon för funktionen har uppdaterats: Ange autentiseringsalternativ för VpnClient AAD till resurser för virtuella nätverksgatewayer.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1900">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="b4d0c-1901">New-AzVirtualNetworkGateway har uppdaterats: De valfria parametrarna AadTenantUri, AadAudienceId och AadIssuerUri för att ange VpnClient AAD-autentiseringsalternativ på en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1901">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="b4d0c-1902">Set-AzVirtualNetworkGateway har uppdaterats: De valfria parametrarna AadTenantUri, AadAudienceId och AadIssuerUri för att ange VpnClient AAD-autentiseringsalternativ på en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1902">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="b4d0c-1903">Set-AzVirtualNetworkGateway har uppdaterats: Den valfria växelparametern RemoveAadAuthentication som tar bort VpnClient AAD-autentiseringsalternativ från en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1903">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="b4d0c-1904">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1904">Az.OperationalInsights</span></span>
* <span data-ttu-id="b4d0c-1905">Aktivera prisnivån **pergb2018** i kommandot ”New-AzureRmOperationalInsightsWorkspace”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1905">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="b4d0c-1906">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1906">Az.Resources</span></span>
* <span data-ttu-id="b4d0c-1907">Stöd för ytterligare alternativ för att exportera en mall</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1907">Support for additional Template Export options</span></span>
    - <span data-ttu-id="b4d0c-1908">Lägg till parametern ”-SkipResourceNameParameterization” till Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1908">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="b4d0c-1909">Lägg till parametern ”-SkipAllParameterization” till Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1909">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="b4d0c-1910">Lägg till parametern ”-Resource” till Export-AzResourceGroup för exporterad resursfiltrering</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1910">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="b4d0c-1911">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1911">Az.ServiceFabric</span></span>
* <span data-ttu-id="b4d0c-1912">Åtgärda att fel tumavtryck används vid tilläggning av certifikat i ByExistingKeyVault i vissa fall</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1912">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="b4d0c-1913">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1913">Az.Sql</span></span>
* <span data-ttu-id="b4d0c-1914">Åtgärda suffix för lagringsslutpunkt i Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1914">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="b4d0c-1915">Åtgärda att aktivering av Advanced Data Security åsidosätter Advanced Threat Protection-princip</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1915">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="b4d0c-1916">Nya cmdletar för Management.Sql som gör att kunderna kan lägga till nycklar för transparent datakryptering (TDE) och ange TDE-skydd för hanterade instanser</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1916">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="b4d0c-1917">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1917">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="b4d0c-1918">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1918">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="b4d0c-1919">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1919">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="b4d0c-1920">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1920">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="b4d0c-1921">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1921">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b4d0c-1922">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1922">Az.Storage</span></span>
* <span data-ttu-id="b4d0c-1923">Stöd för typerna FileStorage och SkuName Premium_ZRS när lagringskonton skapas</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1923">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="b4d0c-1924">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1924">New-AzStorageAccount</span></span>
* <span data-ttu-id="b4d0c-1925">Beskrivningen av cmdleten för bloboföränderlighet har förtydligats</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1925">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="b4d0c-1926">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1926">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b4d0c-1927">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1927">Az.Websites</span></span>
* <span data-ttu-id="b4d0c-1928">Optimerar Get-AzWebAppCertificate för att filtrera efter resursgrupp på servern i stället för klienten</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1928">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="b4d0c-1929">Lägger till växlingsparametern -UseDisasterRecovery till Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1929">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="b4d0c-1930">2.2.0 – juni 2019</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1930">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="b4d0c-1931">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1931">Az.Cdn</span></span>
* <span data-ttu-id="b4d0c-1932">Uppdaterade cmdletar för att ge stöd för rulesEngine-funktion baserat på API-version 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1932">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b4d0c-1933">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1933">Az.Compute</span></span>
* <span data-ttu-id="b4d0c-1934">Lade till parameter `NoWait` som startar åtgärden och returnerar omedelbart, innan åtgärden har slutförts.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1934">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="b4d0c-1935">Uppdaterade cmdletar:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1935">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="b4d0c-1936">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1936">Az.EventHub</span></span>
* <span data-ttu-id="b4d0c-1937">Korrigering för #9231 – Get-AzEventHubNamespace returnerar inga taggar</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1937">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="b4d0c-1938">Korrigering för #9230 – Get-AzEventHubNamespace returnerar ResourceGroup istället för ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1938">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b4d0c-1939">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1939">Az.Network</span></span>
* <span data-ttu-id="b4d0c-1940">Uppdatera ResourceId och InputObject för NAT-gateway</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1940">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="b4d0c-1941">Lägg till alias för ResourceId och InputObject</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1941">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="b4d0c-1942">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1942">Az.PolicyInsights</span></span>
* <span data-ttu-id="b4d0c-1943">Åtgärda Null-referensproblem i Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1943">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b4d0c-1944">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1944">Az.RecoveryServices</span></span>
* <span data-ttu-id="b4d0c-1945">Minsta kvarhållning för IaaSVM-policy i dagar ändrat till 7 från 1</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1945">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="b4d0c-1946">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1946">Az.ServiceBus</span></span>
* <span data-ttu-id="b4d0c-1947">Korrigering för ärende #9182 – Get-AzServiceBusNamespace returnerar ResourceGroup istället för ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1947">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="b4d0c-1948">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1948">Az.ServiceFabric</span></span>
* <span data-ttu-id="b4d0c-1949">Åtgärda stavfel i felmeddelandet för Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1949">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="b4d0c-1950">Åtgärda saknat tecken i Service Fabric-kommandorader</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1950">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="b4d0c-1951">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1951">Az.Sql</span></span>
* <span data-ttu-id="b4d0c-1952">Lägg till parametern DnsZonePartner för New-AzureSqlInstance-cmdlet för att ge stöd för AutoDr för hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1952">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="b4d0c-1953">Avvecklar cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1953">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="b4d0c-1954">Döp om cmdletar för hotidentifiering till Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1954">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="b4d0c-1955">Parametrarna New-AzSqlInstance -StorageSizeInGB och -LicenseType är nu valfria.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1955">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b4d0c-1956">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1956">Az.Websites</span></span>
* <span data-ttu-id="b4d0c-1957">åtgärdar problemet där användningen av Set-AzWebApp och Set-AzWebAppSlot med -WebApp-egenskap tog bort taggarna</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1957">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="b4d0c-1958">2.1.0 – maj 2019</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1958">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="b4d0c-1959">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1959">Az.ApiManagement</span></span>
* <span data-ttu-id="b4d0c-1960">Skapade nya cmdletar för att hantera diagnostik för global- och API-omfång</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1960">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="b4d0c-1961">**Get-AzApiManagementDiagnostic** – Skaffa diagnostik konfigurerad för global- eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1961">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="b4d0c-1962">**New-AzApiManagementDiagnostic** – Skapa ny diagnostik för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1962">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="b4d0c-1963">**New-AzApiManagementHttpMessageDiagnostic** – Skapa diagnostikinställning om vilka rubriker som ska loggas och storleken på brödtextbyte</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1963">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="b4d0c-1964">**New-AzApiManagementPipelineDiagnosticSetting** – Skapa diagnostikinställningar för inkommande/utgående HTTP-meddelanden till gatewayen.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1964">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="b4d0c-1965">**New-AzApiManagementSamplingSetting** – Skapa samplinginställningar för begäranden/svar för en diagnostik</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1965">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="b4d0c-1966">**Remove-AzApiManagementDiagnostic** – Ta bort en diagnostikenhet för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1966">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="b4d0c-1967">**Set-AzApiManagementDiagnostic** – Uppdatera en diagnostikenhet för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1967">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="b4d0c-1968">Skapade nya cmdletar för hantering av cacheminne i ApiManagement-tjänsten</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1968">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="b4d0c-1969">**Get-AzApiManagementCache** – Hämta information om cacheminnet som anges av identifierare eller alla cacheminnen</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1969">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="b4d0c-1970">**New-AzApiManagementCache** – Skapa ett nytt default-cacheminne eller cacheminne i en viss Azure-region</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1970">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="b4d0c-1971">**Remove-AzApiManagementCache** – Ta bort ett cacheminne</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1971">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="b4d0c-1972">**Remove-AzApiManagementCache** – Ta bort ett cacheminne</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1972">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="b4d0c-1973">Skapade nya cmdletar för hantering av API-schema</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1973">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="b4d0c-1974">**New-AzApiManagementSchema** – Skapa ett nytt schema för ett API</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1974">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="b4d0c-1975">**Get-AzApiManagementSchema** – Hämta de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1975">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="b4d0c-1976">**Remove-AzApiManagementSchema** – Ta bort de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1976">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="b4d0c-1977">**Set-AzApiManagementSchema** – Uppdatera de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1977">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="b4d0c-1978">Skapa ny cmdlet för att generera en användartoken.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1978">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="b4d0c-1979">**New-AzApiManagementUserToken** – Skapa en ny användartoken som enligt standardinställning är giltig i 8 timmar. Token för GIT-användaren kan skapas med den här cmdleten./</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1979">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="b4d0c-1980">Skapade en ny cmdlet för att hämta nätverksstatus</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1980">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="b4d0c-1981">**Get-AzApiManagementNetworkStatus** – Hämta nätverksstatusanslutningen för resurserna som API Management-tjänsten är beroende av.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1981">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="b4d0c-1982">Det här är användbart när du distribuerar ApiManagement-tjänsten i ett virtuellt nätverk och validerar om något beroende är brutet.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1982">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="b4d0c-1983">Uppdaterade cmdlet **New-AzApiManagement** för att hantera ApiManagement-tjänsten</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1983">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="b4d0c-1984">Lade till stöd för den nya SKU:n Consumption</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1984">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="b4d0c-1985">Aktiverade stöd för att slå på flaggan EnableClientCertificate för SKU:n Consumption</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1985">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="b4d0c-1986">Den nya cmdleten **New-AzApiManagementSslSetting** gör det möjligt att ställa in TLS/SSL-inställningen på ”Backend” och ”Frontend” (serverdel och klientdel).</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1986">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="b4d0c-1987">Det här kan också användas till att konfigurera chiffer som 3DES och ServerProtocols som Http2 för Frontend för en ApiManagement-tjänst.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1987">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="b4d0c-1988">Stöd har lagts till för att konfigurera värdnamnet DeveloperPortal på ApiManagement-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1988">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="b4d0c-1989">Uppdaterade cmdletar **Get-AzApiManagementSsoToken** för att ta PsApiManagement-objekt som indata</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1989">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="b4d0c-1990">Uppdaterad cmdleten för att visa infogade felmeddelanden</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1990">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="b4d0c-1991">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Felkod: Felmeddelande av typen ValidationError: Ett eller flera fält innehåller felaktiga värden: Felinformation:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1991">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="b4d0c-1992">Uppdaterade cmdlet **Export-AzApiManagementApi** för att exportera API:er i OpenApi 3.0-format</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1992">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="b4d0c-1993">Uppdaterade cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1993">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="b4d0c-1994">Importera API från dokumentspecifikationen OpenApi 3.0</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1994">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="b4d0c-1995">Om du vill åsidosätta egenskapen PsApiManagementSchema specificerad i ett dokument (Swagger, Wadl, Wsdl, OpenApi).</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1995">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="b4d0c-1996">Åsidosätta egenskapen ServiceUrl som specificeras i ett dokument.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1996">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="b4d0c-1997">Uppdaterade cmdlet **Get-AzApiManagementPolicy** för att returnera policy i undantaget format av typen icke-XML med rawxml</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1997">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="b4d0c-1998">Uppdaterade cmdlet **Set-AzApiManagementPolicy** för att godkänna policy i undantaget format av typen icke-XML med rawxml och XML undantaget med xml</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1998">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="b4d0c-1999">Uppdaterad cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="b4d0c-1999">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="b4d0c-2000">Konfigurera API med OpenId auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2000">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="b4d0c-2001">Skapa ett API i ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2001">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="b4d0c-2002">Klona ett API med SourceApiId och SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2002">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="b4d0c-2003">Möjlighet att konfigurera SubscriptionRequired i API-omfattningen.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2003">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="b4d0c-2004">Uppdaterad cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2004">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="b4d0c-2005">Konfigurera API med OpenId auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2005">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="b4d0c-2006">Uppdatera ett API till ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2006">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="b4d0c-2007">Möjlighet att konfigurera SubscriptionRequired i API-omfattningen.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2007">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="b4d0c-2008">Uppdaterad cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2008">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="b4d0c-2009">Klona en befintlig version med hjälp av SourceApiRevision (kopiera taggar, produkter, åtgärder och principer).</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2009">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="b4d0c-2010">Den nya revisionen antar ApiId från den överordnade instansen.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2010">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="b4d0c-2011">Tillhandahålla ApiRevisionDescription</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2011">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="b4d0c-2012">Åsidosätta ServiceUrl vid kloning av ett API.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2012">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="b4d0c-2013">Uppdaterad cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2013">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="b4d0c-2014">Konfigurera AAD eller AADB2C med en Authority</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2014">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="b4d0c-2015">Konfigurera SignupPolicy, SigninPolicy, ProfileEditingPolicy och PasswordResetPolicy</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2015">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="b4d0c-2016">Uppdaterad cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2016">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="b4d0c-2017">Kompensera för ny SubscriptonModel med Scope och UserId</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2017">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="b4d0c-2018">Kompensera för gammal prenumerationsmodell med ProductId och UserId</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2018">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="b4d0c-2019">Lägg till funktion för att aktivera AllowTracing på prenumerationsnivå.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2019">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="b4d0c-2020">Uppdaterad cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2020">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="b4d0c-2021">Kompensera för ny SubscriptonModel med Scope och UserId</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2021">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="b4d0c-2022">Kompensera för gammal prenumerationsmodell med ProductId och UserId</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2022">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="b4d0c-2023">Lägg till funktion för att aktivera AllowTracing på prenumerationsnivå.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2023">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="b4d0c-2024">Uppdaterade följande cmdletar för att acceptera ResourceId som indata</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2024">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="b4d0c-2025">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2025">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="b4d0c-2026">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2026">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="b4d0c-2027">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2027">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="b4d0c-2028">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2028">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="b4d0c-2029">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2029">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="b4d0c-2030">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2030">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="b4d0c-2031">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2031">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="b4d0c-2032">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2032">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="b4d0c-2033">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2033">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="b4d0c-2034">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2034">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="b4d0c-2035">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2035">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="b4d0c-2036">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2036">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="b4d0c-2037">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2037">Az.Automation</span></span>
* <span data-ttu-id="b4d0c-2038">Uppdaterade Get-AzAutomationJobOutputRecord för att hantera postvärden av typen JSON och Text.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2038">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="b4d0c-2039">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2039">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="b4d0c-2040">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2040">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="b4d0c-2041">Ändrade beteende för Start-AzAutomationDscCompilationJob till att bara starta jobbet istället för att vänta på slutförandet.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2041">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="b4d0c-2042">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2042">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="b4d0c-2043">Korrigering för Get-AzAutomationDscNode när using -Name returnerar alla noder.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2043">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="b4d0c-2044">Nu returnerar den endast den matchande noden.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2044">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b4d0c-2045">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2045">Az.Compute</span></span>
* <span data-ttu-id="b4d0c-2046">Lägg till parametrarna ProtectFromScaleIn och ProtectFromScaleSetAction i cmdleten Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2046">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="b4d0c-2047">Nu är standardinställningen att vimpelparametern New-AzVM använder en tillgänglig plats om USA, östra inte stöds</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2047">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b4d0c-2048">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2048">Az.DataLakeStore</span></span>
* <span data-ttu-id="b4d0c-2049">Uppdatera ADLS-sdk för att använda httpclient, integrera dataplanstestning med Azure-ramverk</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2049">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="b4d0c-2050">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2050">Az.Monitor</span></span>
* <span data-ttu-id="b4d0c-2051">Korrigera felaktiga parameternamn i hjälpexempel</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2051">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b4d0c-2052">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2052">Az.Network</span></span>
* <span data-ttu-id="b4d0c-2053">Lägg till flaggan DisableBgpRoutePropagation i utdata för effektiv routningstabell</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2053">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="b4d0c-2054">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2054">Updated cmdlet:</span></span>
        - <span data-ttu-id="b4d0c-2055">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2055">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="b4d0c-2056">Åtgärda dubbelstreck i dokumentationen New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2056">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="b4d0c-2057">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2057">Az.Resources</span></span>
* <span data-ttu-id="b4d0c-2058">Lägg till ny cmdlet Get-AzureRmDenyAssignment för att hämta tilldelningsnekanden</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2058">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="b4d0c-2059">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2059">Az.Sql</span></span>
* <span data-ttu-id="b4d0c-2060">Döp om Advanced Threat Protection-cmdletar för Advanced Data Security och aktivera Vulnerability Assessment som standard</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2060">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="b4d0c-2061">2.0.0 – maj 2019</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2061">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b4d0c-2062">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2062">Az.Accounts</span></span>
* <span data-ttu-id="b4d0c-2063">Uppdatera autentiseringsbiblioteket för att åtgärda ADFS-problem med autentisering av användarnamn/lösenord</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2063">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="b4d0c-2064">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2064">Az.CognitiveServices</span></span>
* <span data-ttu-id="b4d0c-2065">Visa endast Bing-ansvarsfriskrivning för Bing-sökningstjänster.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2065">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="b4d0c-2066">Förbättra felmeddelande när det inte går att skapa konton.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2066">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b4d0c-2067">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2067">Az.Compute</span></span>
* <span data-ttu-id="b4d0c-2068">Funktion för närhetsplaceringsgrupper.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2068">Proximity placement group feature.</span></span>
    - <span data-ttu-id="b4d0c-2069">Följande nya cmdletar har lagts till:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2069">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="b4d0c-2070">Den nya parametern ProximityPlacementGroupId har lagts till i följande cmdletar:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2070">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="b4d0c-2071">Parametern StorageAccountType har lagts till i New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2071">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="b4d0c-2072">TargetRegion för New-AzGalleryImageVersion kan innehålla StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2072">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="b4d0c-2073">Växlingsparametern SkipShutdown har lagts till i Stop-AzVM och Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2073">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="b4d0c-2074">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2074">Breaking changes</span></span>
    - <span data-ttu-id="b4d0c-2075">Set-AzVMBootDiagnostics har ändrats till Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2075">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="b4d0c-2076">Export-AzLogAnalyticThrottledRequests har ändrats till Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2076">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="b4d0c-2077">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2077">Az.DeploymentManager</span></span>
* <span data-ttu-id="b4d0c-2078">De första allmänt tillgängliga versionerna av cmdletar för Distributionshanteraren i Azure</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2078">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="b4d0c-2079">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2079">Az.Dns</span></span>
* <span data-ttu-id="b4d0c-2080">Automatisk delegering av DNS för NameServer</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2080">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="b4d0c-2081">Det överordnade zonnamnet kan användas som ytterligare valfri parameter i cmdleten för att skapa DNS-zoner.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2081">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="b4d0c-2082">Lägger till NS-poster för en nyligen skapad underordnad zon i den överordnade zonen.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2082">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="b4d0c-2083">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2083">Az.FrontDoor</span></span>
* <span data-ttu-id="b4d0c-2084">De första allmänt tillgängliga versionerna av cmdletar för Azure FrontDoor</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2084">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="b4d0c-2085">Byt namn på WAF-cmdletar så att de omfattar ”Waf”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2085">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="b4d0c-2086">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2086">Az.HDInsight</span></span>
* <span data-ttu-id="b4d0c-2087">Två cmdletar har tagits bort:</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2087">Removed two cmdlets:</span></span>
    - <span data-ttu-id="b4d0c-2088">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2088">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="b4d0c-2089">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2089">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="b4d0c-2090">En ny cmdlet har lagts till, Set-AzHDInsightGatewayCredential, som ersätter Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2090">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="b4d0c-2091">Uppdatera cmdleten Get-AzHDInsightJobOutput för att skilja mellan läsarrollen och HDInsight-operatörsrollen:</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2091">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="b4d0c-2092">Användare med läsarrollen måste uttryckligen ange parametern ”DefaultStorageAccountKey”, annars uppstår fel.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2092">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="b4d0c-2093">Användare med HDInsight-operatörsrollen påverkas inte.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2093">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="b4d0c-2094">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2094">Az.Monitor</span></span>
* <span data-ttu-id="b4d0c-2095">Nya cmdletar för SQR API (schemalagd frågeregel)</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2095">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="b4d0c-2096">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2096">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="b4d0c-2097">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2097">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="b4d0c-2098">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2098">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="b4d0c-2099">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2099">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="b4d0c-2100">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2100">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="b4d0c-2101">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2101">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="b4d0c-2102">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2102">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="b4d0c-2103">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2103">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="b4d0c-2104">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2104">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="b4d0c-2105">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2105">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="b4d0c-2106">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2106">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="b4d0c-2107">[Mer](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information om SQR API</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2107">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="b4d0c-2108">Az.Monitor.md har uppdaterats för att omfatta cmdletar för måttbaserade aviseringsregler i GenV2 (inte klassiska)</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2108">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b4d0c-2109">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2109">Az.Network</span></span>
* <span data-ttu-id="b4d0c-2110">Lägg till stöd för NAT Gateway-resurs</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2110">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="b4d0c-2111">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2111">New cmdlets</span></span>
        - <span data-ttu-id="b4d0c-2112">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2112">New-AzNatGateway</span></span>
        - <span data-ttu-id="b4d0c-2113">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2113">Get-AzNatGateway</span></span>
        - <span data-ttu-id="b4d0c-2114">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2114">Set-AzNatGateway</span></span>
        - <span data-ttu-id="b4d0c-2115">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2115">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="b4d0c-2116">Uppdaterade cmdletar</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2116">Updated cmdlets</span></span>
        - <span data-ttu-id="b4d0c-2117">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2117">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="b4d0c-2118">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2118">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="b4d0c-2119">Nedanstående kommandon för funktionen har uppdaterats: Ange/ta bort anpassade vägar på Brooklyn Gateway.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2119">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="b4d0c-2120">New-AzVirtualNetworkGateway har uppdaterats: Den valfria parametern -CustomRoute har lagts till för att ställa in adressprefix som anpassade vägar för att ange gateway.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2120">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="b4d0c-2121">Set-AzVirtualNetworkGateway har uppdaterats: Den valfria parametern -CustomRoute har lagts till för att ange adressprefix som anpassade vägar för att ange gateway.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2121">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="b4d0c-2122">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2122">Az.PolicyInsights</span></span>
* <span data-ttu-id="b4d0c-2123">Stöd för att fråga efter information om principutvärdering.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2123">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="b4d0c-2124">Lägg till parametern ”-Expand” för Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2124">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="b4d0c-2125">Stöd för -Expand PolicyEvaluationDetails.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2125">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b4d0c-2126">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2126">Az.RecoveryServices</span></span>
* <span data-ttu-id="b4d0c-2127">Stöd för att dela prenumeration mellan Azure och Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2127">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="b4d0c-2128">Markering av kommande icke-bakåtkompatibla ändringar för Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2128">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="b4d0c-2129">Korrigering för återställningsplan och åtgärdsplan i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2129">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="b4d0c-2130">Korrigering för mappning av uppdateringsnätverk i Azure Site Recovery för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2130">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="b4d0c-2131">Korrigering för instruktioner för uppdateringsskydd i Azure Site Recovery för Azure till Azure för hanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2131">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="b4d0c-2132">Andra mindre korrigeringar.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2132">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="b4d0c-2133">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2133">Az.Relay</span></span>
* <span data-ttu-id="b4d0c-2134">Korrigera stavfel i kundriktade meddelanden</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2134">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="b4d0c-2135">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2135">Az.ServiceBus</span></span>
* <span data-ttu-id="b4d0c-2136">Nya cmdletar har lagts till för NetworkRuleSet för namnområden</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2136">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b4d0c-2137">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2137">Az.Storage</span></span>
* <span data-ttu-id="b4d0c-2138">Uppgradera till lagringsklientbiblioteket 10.0.1 (namnområdet för alla objekt från detta SDK ändras från ”Microsoft.WindowsAzure.Storage. *till ”Microsoft.Azure.Storage.* ”)</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2138">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="b4d0c-2139">Uppgradera till Microsoft.Azure.Management.Storage 11.0.0 för att stödja den nya API-versionen 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2139">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="b4d0c-2140">Standardlagringskontot i Skapa lagringskonto ändras från ”Storage” till ”StorageV2”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2140">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="b4d0c-2141">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2141">New-AzStorageAccount</span></span>
* <span data-ttu-id="b4d0c-2142">Ändra lagringskontots cmdlet-utdata Sku.Name för att passa med indata-SkuName genom att lägga till ”-”. Till exempel ändras ”StandardLRS” till ”Standard_LRS”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2142">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="b4d0c-2143">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2143">New-AzStorageAccount</span></span>
    - <span data-ttu-id="b4d0c-2144">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2144">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="b4d0c-2145">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2145">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b4d0c-2146">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2146">Az.Websites</span></span>
* <span data-ttu-id="b4d0c-2147">Egenskapen ”typ” konfigureras nu för PSSite-objekt som returneras av Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2147">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="b4d0c-2148">Get-AzWebApp\*Metrics och Get-AzAppServicePlanMetrics markeras som inaktuella</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2148">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="b4d0c-2149">1.8.0 – april 2019</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2149">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="b4d0c-2150">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2150">Highlights since the last major release</span></span>
* <span data-ttu-id="b4d0c-2151">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2151">General availability of `Az` module</span></span>
* <span data-ttu-id="b4d0c-2152">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2152">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="b4d0c-2153">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2153">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="b4d0c-2154">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2154">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="b4d0c-2155">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2155">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="b4d0c-2156">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2156">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="b4d0c-2157">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2157">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="b4d0c-2158">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2158">Az.Accounts</span></span>
* <span data-ttu-id="b4d0c-2159">Uppdatera Uninstall-AzureRm för att ta bort moduler i Mac på ett korrekt sätt</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2159">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="b4d0c-2160">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2160">Az.Batch</span></span>
* <span data-ttu-id="b4d0c-2161">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2161">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="b4d0c-2162">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2162">Az.Cdn</span></span>
* <span data-ttu-id="b4d0c-2163">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2163">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="b4d0c-2164">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2164">Az.CognitiveServices</span></span>
* <span data-ttu-id="b4d0c-2165">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2165">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b4d0c-2166">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2166">Az.Compute</span></span>
* <span data-ttu-id="b4d0c-2167">Åtgärda problem med AEM-installationen om resurs-ID:n för diskar innehåller resourcegroups i gemener i resurs-ID:n</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2167">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="b4d0c-2168">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2168">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="b4d0c-2169">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2169">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b4d0c-2170">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2170">Az.DataFactory</span></span>
* <span data-ttu-id="b4d0c-2171">Lägg till SsisProperties om NodeCount inte är null för hanterad integreringskörning.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2171">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b4d0c-2172">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2172">Az.DataLakeStore</span></span>
* <span data-ttu-id="b4d0c-2173">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2173">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="b4d0c-2174">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2174">Az.EventGrid</span></span>
* <span data-ttu-id="b4d0c-2175">Hjälptexten för slutpunkten har uppdaterats för att visa att resurser ska skapas innan cmdletarna för att skapa/uppdatera händelseprenumerationer används.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2175">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="b4d0c-2176">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2176">Az.EventHub</span></span>
* <span data-ttu-id="b4d0c-2177">Nya cmdletar har lagts till för NetworkRuleSet för namnområden</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2177">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="b4d0c-2178">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2178">Az.HDInsight</span></span>
* <span data-ttu-id="b4d0c-2179">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2179">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="b4d0c-2180">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2180">Az.IotHub</span></span>
* <span data-ttu-id="b4d0c-2181">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2181">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="b4d0c-2182">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2182">Az.KeyVault</span></span>
* <span data-ttu-id="b4d0c-2183">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2183">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="b4d0c-2184">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2184">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="b4d0c-2185">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2185">Az.MachineLearning</span></span>
* <span data-ttu-id="b4d0c-2186">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2186">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="b4d0c-2187">Az.Media</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2187">Az.Media</span></span>
* <span data-ttu-id="b4d0c-2188">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2188">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="b4d0c-2189">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2189">Az.Monitor</span></span>
  * <span data-ttu-id="b4d0c-2190">Nya cmdletar för måttbaserad aviseringsregel i GenV2 (inte klassisk)</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2190">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="b4d0c-2191">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2191">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="b4d0c-2192">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2192">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="b4d0c-2193">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2193">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="b4d0c-2194">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2194">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="b4d0c-2195">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2195">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="b4d0c-2196">Monitor SDK har uppdaterats till version 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2196">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b4d0c-2197">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2197">Az.Network</span></span>
* <span data-ttu-id="b4d0c-2198">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2198">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="b4d0c-2199">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2199">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="b4d0c-2200">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2200">Az.NotificationHubs</span></span>
* <span data-ttu-id="b4d0c-2201">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2201">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="b4d0c-2202">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2202">Az.OperationalInsights</span></span>
* <span data-ttu-id="b4d0c-2203">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2203">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="b4d0c-2204">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2204">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="b4d0c-2205">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2205">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b4d0c-2206">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2206">Az.RecoveryServices</span></span>
* <span data-ttu-id="b4d0c-2207">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2207">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="b4d0c-2208">Tabellformatet för SQL i virtuella Azure-datorer har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2208">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="b4d0c-2209">En alternativ metod för att hämta platser i AzureFileShare har lagts till</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2209">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="b4d0c-2210">ScheduleRunDays i SchedulePolicy-objekt har uppdaterats enligt tidszon</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2210">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="b4d0c-2211">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2211">Az.RedisCache</span></span>
* <span data-ttu-id="b4d0c-2212">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2212">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="b4d0c-2213">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2213">Az.Resources</span></span>
* <span data-ttu-id="b4d0c-2214">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2214">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="b4d0c-2215">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2215">Az.Sql</span></span>
* <span data-ttu-id="b4d0c-2216">Ersätt Monitor SDK-beroende med vanlig kod</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2216">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="b4d0c-2217">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2217">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="b4d0c-2218">Förbättrad process för klassificering av flera kolumner.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2218">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="b4d0c-2219">Inkludera SKU-egenskaper (SKU-namn, serie, kapacitet) i svaret från Get-AzSqlServerServiceObjective och formatera som tabell som standard.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2219">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="b4d0c-2220">Möjlighet att använda Get-AzSqlServerServiceObjective efter plats utan att behöva en redan befintlig server i regionen.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2220">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="b4d0c-2221">Stöd för tidszonsparametern när hanterade instanser skapas.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2221">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="b4d0c-2222">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2222">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b4d0c-2223">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2223">Az.Websites</span></span>
* <span data-ttu-id="b4d0c-2224">åtgärdar Set-AzWebApp och Set-AzWebAppSlot så att de inte tar bort taggar vid körning</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2224">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="b4d0c-2225">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2225">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="b4d0c-2226">SDK för WebSites har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2226">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="b4d0c-2227">Egenskapen AdminSiteName har tagits bort från PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2227">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="b4d0c-2228">1.7.0 – april 2019</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2228">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="b4d0c-2229">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2229">Highlights since the last major release</span></span>
* <span data-ttu-id="b4d0c-2230">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2230">General availability of `Az` module</span></span>
* <span data-ttu-id="b4d0c-2231">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2231">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="b4d0c-2232">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2232">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="b4d0c-2233">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2233">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="b4d0c-2234">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2234">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="b4d0c-2235">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2235">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="b4d0c-2236">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2236">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="b4d0c-2237">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2237">Az.Accounts</span></span>
* <span data-ttu-id="b4d0c-2238">Add-AzEnvironment och Set-AzEnvironment har uppdaterats för att godkänna parametern AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2238">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="b4d0c-2239">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2239">Az.AnalysisServices</span></span>
* <span data-ttu-id="b4d0c-2240">ServiceClient används i cmdletar för dataplan och den ursprungliga autentiseringslogiken har tagits bort</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2240">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="b4d0c-2241">Add-AzureASAccount används för omslutning av Connect-AzAccount för att undvika en icke-bakåtkompatibel ändring</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2241">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="b4d0c-2242">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2242">Az.Automation</span></span>
* <span data-ttu-id="b4d0c-2243">Buggen för cmdleten New-AzAutomationSoftwareUpdateConfiguration för inkluderingar har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2243">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="b4d0c-2244">Nu bör parametern IncludedKbNumber och IncludedPackageNameMask fungera.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2244">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="b4d0c-2245">Felkorrigering för dynamiska grupper i uppdateringshanteringen för azure automation</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2245">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b4d0c-2246">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2246">Az.Compute</span></span>
* <span data-ttu-id="b4d0c-2247">Lägg till parametern HyperVGeneration i New-AzDiskConfig och New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2247">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="b4d0c-2248">Tillåt att virtuella datorer skapas med galleribilder från andra klientorganisationer.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2248">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="b4d0c-2249">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2249">Az.ContainerInstance</span></span>
* <span data-ttu-id="b4d0c-2250">Ett problem har åtgärdats i parametern -Command för New-AzContainerGroup som lade till ett avslutande tomt argument</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2250">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b4d0c-2251">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2251">Az.DataFactory</span></span>
* <span data-ttu-id="b4d0c-2252">ADF .Net SDK-versionen har uppdaterats till 3.0.2</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2252">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="b4d0c-2253">Cmdleten Set-AzDataFactoryV2 har uppdaterats med extra parametrar för inställningar som rör RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2253">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="b4d0c-2254">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2254">Az.Resources</span></span>
* <span data-ttu-id="b4d0c-2255">Förbättra hanteringen av providrar för Get-AzResource när parametrarna -ResourceId eller -ResourceGroupName, -Name och -ResourceType tillhandahålls</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2255">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="b4d0c-2256">Förbättra felhanteringen för ”Test-AzDeployment” och ”Test-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2256">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="b4d0c-2257">Hantera fel utanför distributionsvalideringen och ta med dem i kommandoutdata istället</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2257">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="b4d0c-2258">Mer information här: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2258">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="b4d0c-2259">Lägg till växlingsparametern -IgnoreDynamicParameters till en uppsättning av cmdletar för distribution för att hoppa över fråga i skript och jobbscenarier</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2259">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="b4d0c-2260">Mer information här: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2260">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="b4d0c-2261">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2261">Az.Sql</span></span>
* <span data-ttu-id="b4d0c-2262">Stöd för dataklassificering av databaser.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2262">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b4d0c-2263">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2263">Az.Storage</span></span>
* <span data-ttu-id="b4d0c-2264">Rapportera detaljfel när lagringskontext skapas med parametern -UseConnectedAccount, men utan inloggning på Azure-kontot</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2264">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="b4d0c-2265">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2265">New-AzStorageContext</span></span>
* <span data-ttu-id="b4d0c-2266">Stöd för att hantera Blob Service-egenskaper för ett angivet lagringskonto med API:et för hanteringsplan</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2266">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="b4d0c-2267">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2267">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="b4d0c-2268">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2268">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="b4d0c-2269">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2269">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="b4d0c-2270">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2270">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="b4d0c-2271">Stöd för -AsJob-cmdletar för att ladda upp och ladda ned blobar och filer</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2271">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="b4d0c-2272">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2272">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="b4d0c-2273">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2273">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="b4d0c-2274">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2274">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="b4d0c-2275">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2275">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="b4d0c-2276">1.6.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2276">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="b4d0c-2277">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2277">Highlights since the last major release</span></span>
* <span data-ttu-id="b4d0c-2278">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2278">General availability of `Az` module</span></span>
* <span data-ttu-id="b4d0c-2279">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2279">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="b4d0c-2280">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2280">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="b4d0c-2281">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2281">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="b4d0c-2282">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2282">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="b4d0c-2283">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2283">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="b4d0c-2284">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2284">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="b4d0c-2285">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2285">Az.Automation</span></span>
* <span data-ttu-id="b4d0c-2286">Azure Automation – ändring av uppdateringshantering för stöd för de nya funktionerna:</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2286">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="b4d0c-2287">Dynamisk gruppering</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2287">Dynamic grouping</span></span>
    * <span data-ttu-id="b4d0c-2288">För-/efterskrift</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2288">Pre-Post script</span></span>
    * <span data-ttu-id="b4d0c-2289">Inställning för omstart</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2289">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b4d0c-2290">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2290">Az.Compute</span></span>
* <span data-ttu-id="b4d0c-2291">Åtgärda problem med sökvägsmatchning i Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2291">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="b4d0c-2292">Uppdatera Compute-klientbibliotek till 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2292">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="b4d0c-2293">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2293">Az.KeyVault</span></span>
* <span data-ttu-id="b4d0c-2294">Stöd för jokertecken för KeyVault-cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2294">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b4d0c-2295">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2295">Az.Network</span></span>
* <span data-ttu-id="b4d0c-2296">Lägg till stöd för Threat Intelligence för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2296">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="b4d0c-2297">Lägg till resurs för brandväggsprincip på översta nivå och anpassade regler för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2297">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b4d0c-2298">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2298">Az.RecoveryServices</span></span>
* <span data-ttu-id="b4d0c-2299">SnapshotRetentionInDays har lagts till i Azure-principen för virtuella datorer för stöd av Instant RP</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2299">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="b4d0c-2300">Pipe-stöd för avregistrering av container har lagts till</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2300">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="b4d0c-2301">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2301">Az.Resources</span></span>
* <span data-ttu-id="b4d0c-2302">Uppdatera stöd för jokertecken för Get-AzResource och Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2302">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="b4d0c-2303">Uppdatera autentiseringsuppgifter som används vid allmänna anrop till ARM</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2303">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="b4d0c-2304">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2304">Az.Sql</span></span>
* <span data-ttu-id="b4d0c-2305">Cmdlet-parametern (ExcludeDetectionType) för Hotidentifiering ändrades från DetectionType till sträng[] för att framtidssäkra den när nya DetectionTypes läggs till, och även för att stödja automatisk ifyllning.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2305">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b4d0c-2306">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2306">Az.Storage</span></span>
* <span data-ttu-id="b4d0c-2307">Stöd för att hämta/ange/ta bort hanteringsprincip på ett lagringskonto</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2307">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="b4d0c-2308">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2308">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="b4d0c-2309">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2309">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="b4d0c-2310">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2310">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="b4d0c-2311">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2311">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="b4d0c-2312">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2312">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="b4d0c-2313">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2313">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b4d0c-2314">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2314">Az.Websites</span></span>
* <span data-ttu-id="b4d0c-2315">Åtgärda fel med ARM-mall som avbryter kloning av alla platser med 'New-AzWebApp -IncludeSourceWebAppSlots'</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2315">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="b4d0c-2316">1.5.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2316">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b4d0c-2317">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2317">Az.Accounts</span></span>
* <span data-ttu-id="b4d0c-2318">Lägg till kommandot Register-AzModule för stöd för AutoRest-genererade cmdletar</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2318">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="b4d0c-2319">Uppdatera exempel för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2319">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="b4d0c-2320">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2320">Az.Automation</span></span>
* <span data-ttu-id="b4d0c-2321">Problem med att hämta vissa månadsscheman i flera Azure Automation-cmdletar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2321">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="b4d0c-2322">Åtgärda problem med att Get-AzAutomationDscNode bara returnerar de 20 översta noderna.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2322">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="b4d0c-2323">Nu returneras alla noder</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2323">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="b4d0c-2324">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2324">Az.Cdn</span></span>
* <span data-ttu-id="b4d0c-2325">Nya Powershell-cmdletar för att aktivera/inaktivera anpassade domän-HTTPS har lagts till och de gamla har gjorts inaktuella</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2325">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b4d0c-2326">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2326">Az.Compute</span></span>
* <span data-ttu-id="b4d0c-2327">Lägg till stöd för jokertecken för Get-cmdletar</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2327">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b4d0c-2328">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2328">Az.DataFactory</span></span>
* <span data-ttu-id="b4d0c-2329">ADF .Net SDK-versionen har uppdaterats till 3.0.1</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2329">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="b4d0c-2330">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2330">Az.LogicApp</span></span>
* <span data-ttu-id="b4d0c-2331">Åtgärda problemet med att ListWorkflows endast hämtar den första sidan med resultat</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2331">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b4d0c-2332">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2332">Az.Network</span></span>
* <span data-ttu-id="b4d0c-2333">Lägg till stöd för jokertecken för Network-cmdletar</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2333">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b4d0c-2334">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2334">Az.RecoveryServices</span></span>
* <span data-ttu-id="b4d0c-2335">Stöd har lagts till för SQL Server i virtuella Azure-datorer</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2335">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="b4d0c-2336">SDK-uppdatering</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2336">SDK Update</span></span>
* <span data-ttu-id="b4d0c-2337">Get-ProtectableItem-incheckning i VMappContainer har tagits bort</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2337">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="b4d0c-2338">Name och ServerName har lagts till som parametrar för Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2338">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="b4d0c-2339">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2339">Az.Resources</span></span>
* <span data-ttu-id="b4d0c-2340">Lägg till parametern `-TemplateObject` i cmdletar för distribution</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2340">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="b4d0c-2341">Mer information här: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2341">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="b4d0c-2342">Åtgärda problem med piping av resultatet i `Get-AzResource` till `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2342">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="b4d0c-2343">Mer information här: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2343">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="b4d0c-2344">Åtgärda problem med ändring av JSON-datatyp när `Set-AzResource` körs</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2344">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="b4d0c-2345">Mer information här: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2345">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="b4d0c-2346">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2346">Az.Sql</span></span>
* <span data-ttu-id="b4d0c-2347">AuditingEndpointsCommunicator uppdateras.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2347">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="b4d0c-2348">Åtgärdar beteendet hos ett gränsscenario när nya diagnostikinställningar skapas.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2348">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b4d0c-2349">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2349">Az.Storage</span></span>
* <span data-ttu-id="b4d0c-2350">Stöd för BlockBlobStorage när Storage-konto skapas      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2350">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="b4d0c-2351">1.4.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2351">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="b4d0c-2352">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2352">Az.AnalysisServices</span></span>
* <span data-ttu-id="b4d0c-2353">Inaktuell AddAzureASAccount-cmdlet</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2353">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="b4d0c-2354">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2354">Az.Automation</span></span>
* <span data-ttu-id="b4d0c-2355">Hjälpen för Import-AzAutomationDscNodeConfiguration har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2355">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="b4d0c-2356">Konfigurationsnamnsvalidering har lagts till i cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2356">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="b4d0c-2357">Förbättrad felhantering för cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2357">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="b4d0c-2358">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2358">Az.CognitiveServices</span></span>
* <span data-ttu-id="b4d0c-2359">CustomSubdomainName har lagts till som en ny valfri parameter för New-AzCognitiveServicesAccount, som används för att ange underdomän för resursen.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2359">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b4d0c-2360">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2360">Az.Compute</span></span>
* <span data-ttu-id="b4d0c-2361">Problemet med ID-parameteruppsättningar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2361">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="b4d0c-2362">Get-AzVMExtension har uppdaterats så att alla installerade tillägg visas om parametern Name inte har angetts</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2362">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="b4d0c-2363">Parametrarna Tag och ResourceId har lagts till i cmdleten Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2363">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="b4d0c-2364">Get-AzVmssVM utan instans-ID och med InstanceView kan visa virtuella VMSS-datorer med instansvyn.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2364">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b4d0c-2365">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2365">Az.DataLakeStore</span></span>
* <span data-ttu-id="b4d0c-2366">Cmdletar har lagts till för uppräkning och återställning av borttagna objekt i ADL</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2366">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="b4d0c-2367">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2367">Az.EventHub</span></span>
* <span data-ttu-id="b4d0c-2368">Ny boolesk egenskap SkipEmptyArchives har lagts till i Skip Empty Archives i CaptureDescription-klassen i Eventhub</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2368">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="b4d0c-2369">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2369">Az.KeyVault</span></span>
* <span data-ttu-id="b4d0c-2370">Taggning i Set-AzKeyVaultSecret har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2370">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="b4d0c-2371">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2371">Az.LogicApp</span></span>
* <span data-ttu-id="b4d0c-2372">Grundläggande SKU har lagts till för Integrationskonton</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2372">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="b4d0c-2373">XSLT 2.0, XSLT 3.0 och Flytande mappningstyper har lagts till</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2373">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="b4d0c-2374">Nya cmdletar för integrationskontosammansättningar</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2374">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="b4d0c-2375">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2375">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="b4d0c-2376">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2376">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="b4d0c-2377">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2377">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="b4d0c-2378">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2378">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="b4d0c-2379">Nya cmdletar för batchkonfiguration för integrationskonto</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2379">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="b4d0c-2380">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2380">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="b4d0c-2381">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2381">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="b4d0c-2382">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2382">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="b4d0c-2383">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2383">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="b4d0c-2384">Logic App-SDK har uppdaterats till version 4.1.0</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2384">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="b4d0c-2385">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2385">Az.Monitor</span></span>
* <span data-ttu-id="b4d0c-2386">Hjälpen för Get-AzMetric har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2386">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b4d0c-2387">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2387">Az.Network</span></span>
* <span data-ttu-id="b4d0c-2388">Hjälpexempel för Add-AzApplicationGatewayCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2388">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="b4d0c-2389">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2389">Az.OperationalInsights</span></span>
* <span data-ttu-id="b4d0c-2390">Ytterligare stöd för datakällorna New och Get ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2390">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="b4d0c-2391">Ny ApplicationInsights-typ har lagts till för att ge stöd för ”Get specific” och ”Get all” för ApplicationInsights-datakällor för angiven arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2391">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="b4d0c-2392">Cmdleten New-AzOperationalInsightsApplicationInsightsDataSource har lagts till för att skapa datakälla med angivna parametrar för Application Insights-resurs: subscription Id, resourceGroupName och name.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2392">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="b4d0c-2393">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2393">Az.Resources</span></span>
* <span data-ttu-id="b4d0c-2394">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2394">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="b4d0c-2395">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2395">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="b4d0c-2396">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2396">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="b4d0c-2397">Fel som gör att KeyCredentials inte kan skapas upprepade gånger har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2397">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="b4d0c-2398">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2398">Az.Sql</span></span>
* <span data-ttu-id="b4d0c-2399">Lägg till stöd för hyperskalanivån för SQL DB</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2399">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="b4d0c-2400">Ett fel har åtgärdats där återställningen kunde misslyckas på grund av onödiga inställningsegenskaper i restore-förfrågan</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2400">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b4d0c-2401">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2401">Az.Websites</span></span>
* <span data-ttu-id="b4d0c-2402">Rätt exempel i Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2402">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="b4d0c-2403">1.3.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2403">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b4d0c-2404">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2404">Az.Accounts</span></span>
* <span data-ttu-id="b4d0c-2405">Uppdatera till den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2405">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="b4d0c-2406">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2406">Az.AnalysisServices</span></span>
<span data-ttu-id="b4d0c-2407">Allmän tillgänglighet för Az.AnalysisServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2407">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b4d0c-2408">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2408">Az.Compute</span></span>
* <span data-ttu-id="b4d0c-2409">AEM-tillägg: Lägg till stöd för UltraSSD-, P60-, P70- och P80-diskar</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2409">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="b4d0c-2410">Uppdatera hjälpbeskrivning för Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2410">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="b4d0c-2411">Uppdatera hjälpbeskrivning och exempel för Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2411">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b4d0c-2412">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2412">Az.RecoveryServices</span></span>
<span data-ttu-id="b4d0c-2413">Allmän tillgänglighet för Az.RecoveryServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2413">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="b4d0c-2414">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2414">Az.Resources</span></span>
* <span data-ttu-id="b4d0c-2415">Korrigera taggar för resursgrupper</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2415">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="b4d0c-2416">Mer information här: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2416">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="b4d0c-2417">Åtgärda problem där `Get-AzureRmRoleAssignment` inte respekterar -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2417">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="b4d0c-2418">Mer information här: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2418">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="b4d0c-2419">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2419">Az.Sql</span></span>
* <span data-ttu-id="b4d0c-2420">Lägga till Get/Set-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2420">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="b4d0c-2421">Åtgärda problem där ett nullref-undantag uppstår när du kör SQL-cmdletar och inte är inloggad på ett Azure-konto</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2421">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="b4d0c-2422">Åtgärda nullref-undantag i Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2422">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="b4d0c-2423">1.2.1 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2423">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b4d0c-2424">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2424">Az.Accounts</span></span>
* <span data-ttu-id="b4d0c-2425">Version med rätt version av autentisering</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2425">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="b4d0c-2426">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2426">Az.AnalysisServices</span></span>
* <span data-ttu-id="b4d0c-2427">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2427">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b4d0c-2428">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2428">Az.RecoveryServices</span></span>
* <span data-ttu-id="b4d0c-2429">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2429">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="b4d0c-2430">1.2.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2430">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b4d0c-2431">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2431">Az.Accounts</span></span>
* <span data-ttu-id="b4d0c-2432">Lägga till interaktiv autentisering och autentisering med användarnamn/lösenord för endast Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2432">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="b4d0c-2433">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2433">Update incorrect online help URLs</span></span>
* <span data-ttu-id="b4d0c-2434">Lägga till varningsmeddelande i PS Core för Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2434">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="b4d0c-2435">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2435">Az.Aks</span></span>
* <span data-ttu-id="b4d0c-2436">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2436">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="b4d0c-2437">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2437">Az.Automation</span></span>
* <span data-ttu-id="b4d0c-2438">Stöd för Python 2-runbookflöden har lagts till</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2438">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="b4d0c-2439">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2439">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="b4d0c-2440">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2440">Az.Cdn</span></span>
* <span data-ttu-id="b4d0c-2441">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2441">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b4d0c-2442">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2442">Az.Compute</span></span>
* <span data-ttu-id="b4d0c-2443">Lägga till cmdleten Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2443">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="b4d0c-2444">Lägga till TempDisk-parameter i Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2444">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="b4d0c-2445">Korrigera varningsmeddelande för New-AzVM</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2445">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="b4d0c-2446">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2446">Az.ContainerRegistry</span></span>
* <span data-ttu-id="b4d0c-2447">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2447">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b4d0c-2448">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2448">Az.DataFactory</span></span>
* <span data-ttu-id="b4d0c-2449">ADF .Net SDK-versionen har uppdaterats till 3.0.0</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2449">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b4d0c-2450">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2450">Az.DataLakeStore</span></span>
* <span data-ttu-id="b4d0c-2451">Åtgärda problem med ADLS-slutpunkt vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2451">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="b4d0c-2452">Mer information här: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2452">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="b4d0c-2453">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2453">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="b4d0c-2454">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2454">Az.IotHub</span></span>
* <span data-ttu-id="b4d0c-2455">Lägga till kodningsformat i cmdleten Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2455">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="b4d0c-2456">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2456">Az.KeyVault</span></span>
* <span data-ttu-id="b4d0c-2457">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2457">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b4d0c-2458">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2458">Az.Network</span></span>
* <span data-ttu-id="b4d0c-2459">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2459">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="b4d0c-2460">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2460">Az.Resources</span></span>
* <span data-ttu-id="b4d0c-2461">Åtgärda felaktiga exempel i referensdokumentationen ”New-AzADAppCredential” och ”New-AzADSpCredential”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2461">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="b4d0c-2462">Åtgärda problem där sökvägen för parametern ”-TemplateFile” inte omvandlas innan cmdletarna för distribution i resursgruppen körs</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2462">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="b4d0c-2463">Az.Resources: Korrigera dokumentationen om standardvärdet för New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2463">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="b4d0c-2464">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2464">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="b4d0c-2465">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2465">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="b4d0c-2466">Åtgärda formateringsproblemet med objektet ”PSResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2466">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="b4d0c-2467">Mer information här: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2467">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="b4d0c-2468">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2468">Az.ServiceFabric</span></span>
* <span data-ttu-id="b4d0c-2469">Återställ när ett certifikat läggs till i en Virtual Machine Scale Sets-modell men ett undantag genereras. Detta har gjorts för att åtgärda följande fel: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2469">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="b4d0c-2470">Korrigera några felmeddelanden.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2470">Fix some error messages.</span></span>
* <span data-ttu-id="b4d0c-2471">Korrigering av skapande av kluster med ARM-mall som är standard för New-AzServiceFabriCluster som inte fungerade med migrering till Az.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2471">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="b4d0c-2472">Korrigering av tilläggning av kluster/programcertifikat så att endast VM Scale Sets som motsvarar klustret läggs till genom att kontrollera ID för klustret i tillägget.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2472">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="b4d0c-2473">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2473">Az.SignalR</span></span>
* <span data-ttu-id="b4d0c-2474">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2474">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="b4d0c-2475">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2475">Az.Sql</span></span>
* <span data-ttu-id="b4d0c-2476">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2476">Update incorrect online help URLs</span></span>
* <span data-ttu-id="b4d0c-2477">Uppdaterad parameterbeskrivning för LicenseType-parameter med möjliga värden</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2477">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="b4d0c-2478">Korrigering för att uppdatera hanterad instansidentitet som inte fungerar när det är den enda uppdaterade egenskapen</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2478">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="b4d0c-2479">Stöd för anpassad sortering på hanterad instans</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2479">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b4d0c-2480">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2480">Az.Storage</span></span>
* <span data-ttu-id="b4d0c-2481">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2481">Update incorrect online help URLs</span></span>
* <span data-ttu-id="b4d0c-2482">Tillhandahåll detaljerat felmeddelande när en användare försöker hämta/konfigurera klassisk loggning/mått på ett Premium Storage-konto eftersom Premium Storage-kontot inte har stöd för klassisk loggning/mått.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2482">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="b4d0c-2483">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2483">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="b4d0c-2484">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2484">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="b4d0c-2485">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2485">Az.TrafficManager</span></span>
* <span data-ttu-id="b4d0c-2486">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2486">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b4d0c-2487">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2487">Az.Websites</span></span>
* <span data-ttu-id="b4d0c-2488">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2488">Update incorrect online help URLs</span></span>
* <span data-ttu-id="b4d0c-2489">Korrigerar ”New-AzWebAppSSLBinding” så att certifikatet laddas upp till rätt resursgrupp och plats om appen finns i en ASE.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2489">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="b4d0c-2490">Korrigerar ”New-AzWebAppSSLBinding” så att taggarna inte skrivs över på en bindning av ett SSL-certifikat till en app</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2490">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="b4d0c-2491">1.1.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2491">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b4d0c-2492">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2492">Az.Accounts</span></span>
* <span data-ttu-id="b4d0c-2493">Lade till omfattningen ”Lokal” till Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2493">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b4d0c-2494">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2494">Az.Compute</span></span>
* <span data-ttu-id="b4d0c-2495">Namn är nu valfritt i ID-parametern för Restart/Start/Stop/Remove/Set-AzVM och Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2495">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="b4d0c-2496">Uppdaterade beskrivningen av ID i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2496">Updated the description of ID in help files</span></span>
* <span data-ttu-id="b4d0c-2497">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2497">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b4d0c-2498">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2498">Az.DataLakeStore</span></span>
* <span data-ttu-id="b4d0c-2499">Uppdatera sdk-versionen av dataplanet till 1.1.14 för SDK-korrigeringar.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2499">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="b4d0c-2500">Korrigerade hanteringen av negativ accesstime och modificationtime för getfilestatus och liststatus; korrigera asynkront annulleringstoken</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2500">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="b4d0c-2501">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2501">Az.EventGrid</span></span>
* <span data-ttu-id="b4d0c-2502">Uppdaterat för användning av API-versionen 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2502">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="b4d0c-2503">Uppdaterade följande cmdletar för att stödja nytt scenario i API-versionen 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2503">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="b4d0c-2504">New-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2504">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="b4d0c-2505">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2505">Event Time-To-Live,</span></span>
        - <span data-ttu-id="b4d0c-2506">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2506">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="b4d0c-2507">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2507">Dead letter endpoint.</span></span>
    - <span data-ttu-id="b4d0c-2508">Update-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2508">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="b4d0c-2509">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2509">Event Time-To-Live,</span></span>
        - <span data-ttu-id="b4d0c-2510">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2510">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="b4d0c-2511">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2511">Dead letter endpoint.</span></span>
* <span data-ttu-id="b4d0c-2512">Lade till nya enum-värden (storageQueue och hybridConnection) för alternativet EndpointType i cmdletarna New-AzureRmEventGridSubscription och Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2512">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="b4d0c-2513">Visa varningsmeddelanden om skapande eller uppdatering av händelseprenumerationen förväntas medföra manuell åtgärd från användaren.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2513">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="b4d0c-2514">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2514">Az.IotHub</span></span>
* <span data-ttu-id="b4d0c-2515">Har uppdaterats till den senaste versionen av SDK:n lotHub</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2515">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="b4d0c-2516">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2516">Az.LogicApp</span></span>
* <span data-ttu-id="b4d0c-2517">Get-AzLogicApp visar en lista över alla som inte har angivet namn</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2517">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="b4d0c-2518">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2518">Az.Resources</span></span>
* <span data-ttu-id="b4d0c-2519">Åtgärdade problem med parameteruppsättningen när parametrarna -ODataQuery och -ResourceId anges för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2519">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="b4d0c-2520">Mer information här: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2520">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="b4d0c-2521">Åtgärdade hantering av parametern -Custom i New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2521">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="b4d0c-2522">Korrigerade stavfel i New-AzDeployment-dokumentationen</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2522">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="b4d0c-2523">Gjorde parametern -MailNickname obligatorisk för New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2523">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="b4d0c-2524">Mer information här: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2524">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="b4d0c-2525">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2525">Az.SignalR</span></span>
* <span data-ttu-id="b4d0c-2526">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2526">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="b4d0c-2527">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2527">Az.Sql</span></span>
* <span data-ttu-id="b4d0c-2528">Konverterade lagringshanteringsklientens beroende av den normala SDK-implementeringen.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2528">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b4d0c-2529">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2529">Az.Storage</span></span>
* <span data-ttu-id="b4d0c-2530">Angav StorageAccountName för lagringskontext som det verkliga namnet på lagringskontot när det skapas med Sas Token, OAuth eller Anonymous</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2530">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="b4d0c-2531">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2531">New-AzStorageContext</span></span>
* <span data-ttu-id="b4d0c-2532">Skapade Sas Token för Blob Snapshot-objekt med parametern -FullUri, åtgärdade den returnerade URI:n så att den blir URI för ögonblicksbild</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2532">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="b4d0c-2533">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2533">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b4d0c-2534">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2534">Az.Websites</span></span>
* <span data-ttu-id="b4d0c-2535">Åtgärdade en bugg i datumparsningen i Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2535">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="b4d0c-2536">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2536">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="b4d0c-2537">1.0.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2537">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="b4d0c-2538">Allmänt</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2538">General</span></span>

- <span data-ttu-id="b4d0c-2539">Allmän tillgänglighet för Az-modulen</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2539">General Availability of Az Module</span></span>
- <span data-ttu-id="b4d0c-2540">Onlinehjälp för varje modul</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2540">Online help for each module</span></span>
- <span data-ttu-id="b4d0c-2541">Mer information och en översikt finns på [Az-informationssidan](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2541">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="b4d0c-2542">Information om hur du migrerar från AzureRM finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2542">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="b4d0c-2543">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2543">Az.Accounts</span></span>
- <span data-ttu-id="b4d0c-2544">Har ändrats från Az.Profile</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2544">Changed from Az.Profile</span></span>
- <span data-ttu-id="b4d0c-2545">Fasta tabellformat för profil- och kontexttyper</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2545">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="b4d0c-2546">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2546">Az.ApiManagement</span></span>
- <span data-ttu-id="b4d0c-2547">Korrigeringar för #7002</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2547">Fixes for #7002</span></span>
- <span data-ttu-id="b4d0c-2548">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2548">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="b4d0c-2549">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2549">Az.Batch</span></span>
- <span data-ttu-id="b4d0c-2550">Lade till möjligheten att se vilken version av Azure Batch Node Agent som körs på var och en av de virtuella datorerna i en pool, via den nya egenskapen `NodeAgentInformation` på `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2550">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="b4d0c-2551">Standarden `Caching` för `PSDataDisk` är nu `ReadWrite` i stället för `None`.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2551">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="b4d0c-2552">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2552">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="b4d0c-2553">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2553">Az.Billing</span></span>
- <span data-ttu-id="b4d0c-2554">Kombinerar cmdletarna för fakturering, förbrukning och UsageAggregates. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2554">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="b4d0c-2555">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2555">Az.CognitivServices</span></span>
- <span data-ttu-id="b4d0c-2556">Lade till kompletterare för SkuName och Typem som är tillgängliga i New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2556">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="b4d0c-2557">Tog bort parameteruppsättningen GetSkusWithAccountParamSetName från Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2557">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="b4d0c-2558">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2558">Az.ContainerInstance</span></span>
- <span data-ttu-id="b4d0c-2559">Stöd för ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2559">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="b4d0c-2560">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2560">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="b4d0c-2561">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2561">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="b4d0c-2562">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2562">Az.DataLakeStore</span></span>
- <span data-ttu-id="b4d0c-2563">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2563">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="b4d0c-2564">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2564">Az.Monitor</span></span>
- <span data-ttu-id="b4d0c-2565">Döpte om Az.Insights till Az.Monitor och andra mindre icke-bakåtkompatibla ändringar. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2565">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="b4d0c-2566">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2566">Az.KeyVault</span></span>
- <span data-ttu-id="b4d0c-2567">Tog bort den inaktuella egenskapen PurgeDisabled från utdatatyper</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2567">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="b4d0c-2568">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2568">Az.MachineLearning</span></span>
- <span data-ttu-id="b4d0c-2569">Inkluderade cmdletarna från modulen Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2569">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="b4d0c-2570">Az.Media</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2570">Az.Media</span></span>
- <span data-ttu-id="b4d0c-2571">Tog bort inaktuella -Tags-alias från New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2571">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="b4d0c-2572">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2572">Az.Network</span></span>
<span data-ttu-id="b4d0c-2573">Stöd har lagts till för konfiguration av RewriteRuleSets i Application Gateway</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2573">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="b4d0c-2574">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2574">New cmdlets added:</span></span>
        - <span data-ttu-id="b4d0c-2575">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2575">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="b4d0c-2576">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2576">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="b4d0c-2577">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2577">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="b4d0c-2578">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2578">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="b4d0c-2579">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2579">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="b4d0c-2580">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2580">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="b4d0c-2581">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2581">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="b4d0c-2582">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2582">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="b4d0c-2583">Cmdletar har uppdaterats med den valfria parametern -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2583">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="b4d0c-2584">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2584">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="b4d0c-2585">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2585">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="b4d0c-2586">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2586">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="b4d0c-2587">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2587">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="b4d0c-2588">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2588">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="b4d0c-2589">New-AzureRmApplicationGatewayUrlPathMapConfig har lagt till KeyVault-stöd för Application Gateway med Identity.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2589">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="b4d0c-2590">Cmdletar har uppdaterats med den valfria parametern -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2590">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="b4d0c-2591">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2591">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="b4d0c-2592">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2592">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="b4d0c-2593">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2593">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="b4d0c-2594">Cmdleten New-AzApplicationGateway har uppdaterats med den valfria parametern -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2594">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="b4d0c-2595">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2595">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="b4d0c-2596">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2596">Az.OperationalInsights</span></span>
- <span data-ttu-id="b4d0c-2597">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2597">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="b4d0c-2598">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2598">Az.Profile</span></span>
- <span data-ttu-id="b4d0c-2599">Modulnamnet har ändrats till Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2599">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="b4d0c-2600">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2600">Az.RecoveryServices</span></span>
- <span data-ttu-id="b4d0c-2601">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2601">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="b4d0c-2602">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2602">Az.Resources</span></span>
- <span data-ttu-id="b4d0c-2603">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2603">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="b4d0c-2604">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2604">Az.ServiceFabric</span></span>
- <span data-ttu-id="b4d0c-2605">Stöd för specificering av certifikat efter eget namn och tumavtryck</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2605">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="b4d0c-2606">Information om fler icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2606">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="b4d0c-2607">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2607">Az.SIgnalR</span></span>
- <span data-ttu-id="b4d0c-2608">Allmän tillgänglighet för PowerShell-cmdletar för SIgnalR</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2608">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="b4d0c-2609">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2609">Az.Sql</span></span>
- <span data-ttu-id="b4d0c-2610">Lade till de nya identifieringstyperna Data_Exfiltration och Unsafe_Action i Threat Detection-cmdletar</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2610">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="b4d0c-2611">Uppdaterade dokumentationsexempel för Sql Auditing-cmdletar</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2611">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="b4d0c-2612">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2612">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="b4d0c-2613">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2613">Az.Storage</span></span>
- <span data-ttu-id="b4d0c-2614">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2614">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="b4d0c-2615">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2615">Az.Websites</span></span>
- <span data-ttu-id="b4d0c-2616">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2616">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="b4d0c-2617">0.7.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2617">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="b4d0c-2618">Allmänt</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2618">General</span></span>

* <span data-ttu-id="b4d0c-2619">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2619">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="b4d0c-2620">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2620">Az.Compute</span></span>

* <span data-ttu-id="b4d0c-2621">Lade till stöd för UltraSSD och Galleriavbildningar i de enkla parameteruppsättningarna för `New-AzVm(ss)`-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2621">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="b4d0c-2622">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2622">Az.DataLakeStore</span></span>

* <span data-ttu-id="b4d0c-2623">Åtgärdade avslutande snedstreck i domänen för adls-konto</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2623">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="b4d0c-2624">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2624">Az.FrontDoor</span></span>

* <span data-ttu-id="b4d0c-2625">Brutna länkar korrigerades</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2625">Fixed some broken links</span></span>
    - <span data-ttu-id="b4d0c-2626">I artiklarna New-AzureRmFrontDoor och Set-AzureRmFrontDoor artiklar korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2626">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="b4d0c-2627">I artikeln New-AzureRmFrontDoorManagedRuleObject korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2627">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="b4d0c-2628">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2628">Az.RecoveryServices</span></span>

* <span data-ttu-id="b4d0c-2629">Lade till valideringar på klientsidan för Azure-filresurs med återställningsåtgärder.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2629">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="b4d0c-2630">Gjorde storageAccountName och storageAccountResourceGroupName valfritt för afs-återställning.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2630">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="b4d0c-2631">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2631">Az.Resources</span></span>

* <span data-ttu-id="b4d0c-2632">Korrigering för https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2632">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="b4d0c-2633">Uppdaterade Get-AzureRmRoleAssignment så att prenumerationsomfattningen används om den anges vid begäran om klassiska administratörer.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2633">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="b4d0c-2634">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2634">Az.Sql</span></span>

* <span data-ttu-id="b4d0c-2635">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2635">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="b4d0c-2636">Korrigerade ett problem med Get-AzureRmSqlDatabaseVulnerabilityAssessment med DotNet-kärna</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2636">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="b4d0c-2637">Ändrade dokumentationen för hjälpmeddelanden som rör SQL Auditing-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2637">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="b4d0c-2638">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2638">Az.Storage</span></span>

* <span data-ttu-id="b4d0c-2639">Lade till -EnableHierarchicalNamespace i New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2639">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="b4d0c-2640">Åtgärdade problemet med att cmdleten Copy File inte kunde återanvända källkontexten på målet om inte -DestContext angetts</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2640">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="b4d0c-2641">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2641">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="b4d0c-2642">Stöd för statisk webbplatskonfiguration</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2642">Support Static Website configuration</span></span>
    - <span data-ttu-id="b4d0c-2643">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2643">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="b4d0c-2644">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2644">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="b4d0c-2645">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2645">Az.Websites</span></span>

* <span data-ttu-id="b4d0c-2646">Set-AzureRmWebApp och Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2646">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="b4d0c-2647">Ny parameter (-AzureStoragePath) har lagts till för att ange att Azure Storage-sökvägar ska monteras i containerappar i Windows och Linux.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2647">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="b4d0c-2648">Använder utdata från den nya cmdleten New-AzureRmWebAppAzureStoragePath som en parameter för att ange sökvägar för Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2648">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="b4d0c-2649">0.6.1 – november 2018</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2649">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="b4d0c-2650">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2650">Az.ApiManagement</span></span>
* <span data-ttu-id="b4d0c-2651">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2651">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="b4d0c-2652">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2652">Az.Automation</span></span>
* <span data-ttu-id="b4d0c-2653">Swagger baserade Azure Automation-cmdletar</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2653">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="b4d0c-2654">Cmdletar för Uppdateringshantering har lagts till</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2654">Added Update Management cmdlets</span></span>
* <span data-ttu-id="b4d0c-2655">Cmdletar för källkontroll har lagts till</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2655">Added Source Control cmdlets</span></span>
* <span data-ttu-id="b4d0c-2656">Remove-AzureRmAutomationHybridWorkerGroup-cmdlet har lagts till</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2656">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="b4d0c-2657">Kommandot för DSC-registreringsnod har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2657">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="b4d0c-2658">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2658">Az.Compute</span></span>
* <span data-ttu-id="b4d0c-2659">Problem med SystemAssigned-identitet har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2659">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="b4d0c-2660">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2660">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="b4d0c-2661">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2661">Az.ContainerInstance</span></span>
* <span data-ttu-id="b4d0c-2662">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2662">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="b4d0c-2663">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2663">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="b4d0c-2664">uppdatera exempelbeskrivningen för marketplace-cmdletar</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2664">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="b4d0c-2665">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2665">Az.Network</span></span>
* <span data-ttu-id="b4d0c-2666">Cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomErreller Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2666">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="b4d0c-2667">ICMP tillbaka till stöd för Azure Firewall-nätverksprotokoll har lagts till</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2667">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="b4d0c-2668">Uppdatera cmdlet Test-AzureRmNetworkWatcherConnectivity, lägga till verifiering av mål-id, adress och port.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2668">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="b4d0c-2669">Åtgärda problem med minnesanvändning i VirtualNetwork-karta</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2669">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="b4d0c-2670">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2670">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="b4d0c-2671">Åtgärda för att ändra principen för en skyddad fildelning.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2671">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="b4d0c-2672">Tidszonsprincipen har konverterats till versaler.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2672">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="b4d0c-2673">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2673">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="b4d0c-2674">Exempel i New-AzureRmRecoveryServicesAsrProtectableItem har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2674">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="b4d0c-2675">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2675">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="b4d0c-2676">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2676">Az.Relay</span></span>
* <span data-ttu-id="b4d0c-2677">Valfri parameter -KeyValue till New-AzureRmRelayKey cmdlet har lagts till, vilket gör det möjligt för användare att tillhandahålla KeyValue.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2677">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="b4d0c-2678">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2678">Az.Resources</span></span>
* <span data-ttu-id="b4d0c-2679">Uppdatera hjälpdokumentation för resursidentitet kopplad till parametrar i `New-AzureRmPolicyAssignment` och `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2679">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="b4d0c-2680">Lägg till ett exempel för New-AzureRmPolicyDefinition som använder -Metadata</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2680">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="b4d0c-2681">Korrigera så att skiftläge behålls i taggnycklar i NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2681">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="b4d0c-2682">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2682">Az.ServiceFabric</span></span>
* <span data-ttu-id="b4d0c-2683">Lägg till utfasningsmeddelanden för kommande icke-kompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2683">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="b4d0c-2684">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2684">Az.Sql</span></span>
* <span data-ttu-id="b4d0c-2685">Nya cmdletar för CRUD-åtgärder på Azure Sql Database-hanterad instans och Azure Sql-hanterad databas</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2685">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="b4d0c-2686">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2686">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="b4d0c-2687">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2687">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="b4d0c-2688">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2688">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="b4d0c-2689">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2689">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="b4d0c-2690">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2690">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="b4d0c-2691">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2691">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="b4d0c-2692">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2692">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="b4d0c-2693">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2693">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="b4d0c-2694">Hantering av utökad granskningsprincip på en server eller en databas har aktiverats.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2694">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="b4d0c-2695">Ny parameter (PredicateExpression) har lagts till för att aktivera filtrering av granskningsloggar.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2695">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="b4d0c-2696">Cmdletar har ändrats så att de använder SQL-klienter i stället för äldre klienter.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2696">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="b4d0c-2697">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2697">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="b4d0c-2698">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2698">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="b4d0c-2699">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2699">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="b4d0c-2700">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2700">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="b4d0c-2701">Problem med att använda Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings med lagringskontots namnparameter har korrigerats</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2701">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="b4d0c-2702">0.5.0 – november 2018</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2702">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="b4d0c-2703">Allmänt</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2703">General</span></span>
* <span data-ttu-id="b4d0c-2704">Lade till resurskompletterare till många kärn-cmdletar – dessa gör att du kan stega genom befintliga resursnamn med TABB vid interaktiva anrop till cmdletar</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2704">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="b4d0c-2705">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2705">Az.Profile</span></span>
* <span data-ttu-id="b4d0c-2706">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2706">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="b4d0c-2707">Bytte namn på parametern TenantId i cmdleten Connect-AzAccount till Tenant och lade till ett alias för TenantId</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2707">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="b4d0c-2708">Uppdaterade TenantId-beskrivningen för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2708">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="b4d0c-2709">Åtgärda felmeddelande för misslyckad inloggning när du tillhandahåller klientdomän</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2709">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="b4d0c-2710">Åtgärda problem med att kontextnamn hamnar i konflikt för konton utan prenumerationer i klientorganisationen</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2710">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="b4d0c-2711">Åtgärda problem med DataLake-slutpunkter vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2711">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="b4d0c-2712">Åtgärdade problem med att Disconnect-AzAccount kastades om den inte anslöts</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2712">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="b4d0c-2713">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2713">Az.CognitiveServices</span></span>
* <span data-ttu-id="b4d0c-2714">Lade till åtgärden Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2714">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b4d0c-2715">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2715">Az.Compute</span></span>
* <span data-ttu-id="b4d0c-2716">Lade till cmdletarna Add-AzVmssVMDataDisk och Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2716">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="b4d0c-2717">Get-AzVMImage visar AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2717">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="b4d0c-2718">Åtgärdade att värdena för alternativen SetAzVMChefExtension -BootstrapOptions och -JsonAttribute inte angavs i json-format.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2718">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b4d0c-2719">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2719">Az.DataLakeStore</span></span>
* <span data-ttu-id="b4d0c-2720">Uppdatera DataLake-paketet till 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2720">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="b4d0c-2721">Lägg till standardsamtidighet för flertrådade åtgärder.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2721">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="b4d0c-2722">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2722">Az.Insights</span></span>
* <span data-ttu-id="b4d0c-2723">Åtgärdade problem #7267 (autoskalningsområde)</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2723">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="b4d0c-2724">Problem med att uppräknade parametrar inte ställdes in ordentligt när du skapade en ny autoskalningsregel (de ställdes alltid in med standardvärdet).</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2724">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="b4d0c-2725">Åtgärdade problem #7513 [Insights] Set-AzDiagnosticSetting kräver uttrycklig specifikation av kategorier när inställningar skapas</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2725">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="b4d0c-2726">Nu kräver inte cmdleten uttrycklig anvisning av kategorierna för att aktiveras under skapande, d.v.s. den fungerar enligt beskrivning</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2726">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b4d0c-2727">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2727">Az.Network</span></span>
* <span data-ttu-id="b4d0c-2728">PeeringType ändrades till en obligatorisk parameter för följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2728">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="b4d0c-2729">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2729">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="b4d0c-2730">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2730">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="b4d0c-2731">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2731">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="b4d0c-2732">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2732">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="b4d0c-2733">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2733">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="b4d0c-2734">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2734">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="b4d0c-2735">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2735">Az.PolicyInsights</span></span>
* <span data-ttu-id="b4d0c-2736">Cmdletar för principreparation har lagts till</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2736">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="b4d0c-2737">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2737">Az.Resources</span></span>
* <span data-ttu-id="b4d0c-2738">Korrigering för https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2738">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="b4d0c-2739">Tillåt att resurser listas med parametern -ResourceId för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2739">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="b4d0c-2740">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2740">Az.ServiceBus</span></span>
* <span data-ttu-id="b4d0c-2741">Skrivskyddad MigrationState-egenskap har lagts till i PSServiceBusMigrationConfigurationAttributes, som hjälper till att hålla koll på migreringstillståndet.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2741">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="b4d0c-2742">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2742">Az.ServiceFabric</span></span>
* <span data-ttu-id="b4d0c-2743">Åtgärda att lägga till certifikat till Linux-Vmss.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2743">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="b4d0c-2744">Åtgärdade Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2744">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="b4d0c-2745">Använd rätt tumavtryck från nya certifikat (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2745">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="b4d0c-2746">Visa undantag korrekt (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2746">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="b4d0c-2747">Åtgärdade Update-AzServiceFabricDurability så att klusterkonfigurationen uppdateras innan Vmss-åtgärden CreateOrUpdate påbörjas.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2747">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="b4d0c-2748">0.4.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2748">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="b4d0c-2749">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2749">Az.Profile</span></span>
* <span data-ttu-id="b4d0c-2750">Åtgärdade problemet med Get-AzSubscription i CloudShell</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2750">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="b4d0c-2751">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2751">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b4d0c-2752">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2752">Az.Compute</span></span>
* <span data-ttu-id="b4d0c-2753">Nya storlekar lades till i listan över godkända VM-storlekar för vilka accelererat nätverk kommer att aktiveras vid användning av den enkla parameteruppsättningen för New-AzVm</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2753">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="b4d0c-2754">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2754">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b4d0c-2755">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2755">Az.DataLakeStore</span></span>
* <span data-ttu-id="b4d0c-2756">Lägger till stöd för regler för virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2756">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="b4d0c-2757">Get-AzDataLakeStoreVirtualNetworkRule: Hämtar eller listar regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2757">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="b4d0c-2758">Add-AzDataLakeStoreVirtualNetworkRule: Lägger till en regel för virtuellt nätverk i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2758">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="b4d0c-2759">Set-AzDataLakeStoreVirtualNetworkRule: Ändrar den angivna regeln för virtuellt nätverk i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2759">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="b4d0c-2760">Remove-AzDataLakeStoreVirtualNetworkRule: Tar bort en regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2760">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b4d0c-2761">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2761">Az.Network</span></span>
* <span data-ttu-id="b4d0c-2762">Skicka protokollvärdet till serverdelen för att uppdatera cmdleten Test-AzNetworkWatcherConnectivity.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2762">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="b4d0c-2763">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2763">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="b4d0c-2764">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2764">Az.Resources</span></span>
* <span data-ttu-id="b4d0c-2765">Åtgärdade problem där Get-AzRoleDefinition genererar ett oläsligt undantag (när standardprofilen inte innehåller någon prenumeration och ingen omfattning har angetts) genom att lägga till ett beskrivande undantag i scenariot.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2765">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="b4d0c-2766">Ställ in ”RoleDefinitionNameParameterSet” som standardparameteruppsättning.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2766">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="b4d0c-2767">0.3.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2767">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="b4d0c-2768">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2768">Azure.Storage</span></span>
* <span data-ttu-id="b4d0c-2769">Åtgärda fel där Kopiera blob/fil inte kopierar metadata när målplatsen har ett problem med metadata</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2769">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="b4d0c-2770">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2770">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="b4d0c-2771">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2771">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="b4d0c-2772">Stöd för att hämta användningsinformation om en Storage-resurs för en specifik plats och för att lägga till ett varningsmeddelande för att hämta användningsinformation om en global Storage-resurs är inaktuellt.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2772">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="b4d0c-2773">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2773">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="b4d0c-2774">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2774">Az.CognitiveServices</span></span>
* <span data-ttu-id="b4d0c-2775">Stöd för Get-AzCognitiveServicesAccountSkus utan ett befintligt konto.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2775">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b4d0c-2776">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2776">Az.Compute</span></span>
* <span data-ttu-id="b4d0c-2777">Åtgärdade fel där Get-AzVM -ResourceGroupName <rg> returnerar fler än 50 resultat om det behövs</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2777">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="b4d0c-2778">Lade till ett exempel för SimpleParameterSet i hjälpen för cmdleten New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2778">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="b4d0c-2779">Ett stavfel i förloppsmeddelandet för Azure Disk Encryption har korrigerats</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2779">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="b4d0c-2780">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2780">Az.DataFactoryV2</span></span>
* <span data-ttu-id="b4d0c-2781">ADF .Net SDK-versionen har uppdaterats till 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2781">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b4d0c-2782">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2782">Az.Network</span></span>
* <span data-ttu-id="b4d0c-2783">Funktionalitet för NetworkProfile har lagts till.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2783">Added NetworkProfile functionality.</span></span> <span data-ttu-id="b4d0c-2784">nya cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2784">new cmdlets added</span></span>
    - <span data-ttu-id="b4d0c-2785">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2785">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="b4d0c-2786">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2786">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="b4d0c-2787">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2787">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="b4d0c-2788">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2788">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="b4d0c-2789">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2789">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="b4d0c-2790">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2790">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="b4d0c-2791">Länk för tjänstassociering på modell för undernät har lagts till</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2791">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="b4d0c-2792">Cmdletarna New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap och Remove-AzVirtualNetworkTap har lagts till</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2792">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="b4d0c-2793">Cmdletarna Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig och Remove-AzNEtworkInterfaceTapConfig har lagts till</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2793">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="b4d0c-2794">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2794">Az.RedisCache</span></span>
* <span data-ttu-id="b4d0c-2795">Tillåt att alla strängar används som storleksparametrar framöver.</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2795">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="b4d0c-2796">Lägg till P5 i popup-fönstret PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2796">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="b4d0c-2797">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2797">Az.Resources</span></span>
* <span data-ttu-id="b4d0c-2798">Parametern -Mode som saknades i Set-AzPolicyDefinition har lagts till</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2798">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="b4d0c-2799">Åtgärdade buggen för cmdleten Get-AzProviderOperation för åtgärder med ursprung som innehåller användare</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2799">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="b4d0c-2800">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2800">Az.Sql</span></span>
* <span data-ttu-id="b4d0c-2801">Ett problem där vissa cmdletar för säkerhetskopiering inte kunde identifiera den aktuella azure-prenumerationen har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2801">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b4d0c-2802">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2802">Az.Websites</span></span>
* <span data-ttu-id="b4d0c-2803">Ny cmdlet: Get-AzWebAppContainerContinuousDeploymentUrl – Hämtar webhook-URL:en för kontinuerlig distribution av container</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2803">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="b4d0c-2804">Nya cmdletar: New-AzWebAppContainerPSSession och Enter-WebAppContainerPSSession – Startar en PowerShell-fjärrsession i en containerapp för windows</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2804">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="b4d0c-2805">0.2.0 – september 2018</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2805">0.2.0 - September 2018</span></span>
 <span data-ttu-id="b4d0c-2806">Första versionen</span><span class="sxs-lookup"><span data-stu-id="b4d0c-2806">Initial Release</span></span>
