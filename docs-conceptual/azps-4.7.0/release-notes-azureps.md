---
title: Viktig information om Azure PowerShell
description: Lär dig mer om alla de senaste uppdateringarna för Azure PowerShell-modulerna.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 98bae70dbd61c74aa92e69cb67afc89ebae23f70
ms.sourcegitcommit: 15f21c40dcb7610e2fbaaabf264ad925e4224500
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/22/2020
ms.locfileid: "90928617"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="a850c-103">Viktig information om Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="a850c-103">Azure PowerShell release notes</span></span>

## <a name="470---september-2020"></a><span data-ttu-id="a850c-104">4.7.0 – September 2020</span><span class="sxs-lookup"><span data-stu-id="a850c-104">4.7.0 - September 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a850c-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a850c-105">Az.Accounts</span></span>
* <span data-ttu-id="a850c-106">Formaterat kommande meddelanden om icke-bakåtkompatibel ändring</span><span class="sxs-lookup"><span data-stu-id="a850c-106">Formatted the upcoming breaking change messages</span></span>
* <span data-ttu-id="a850c-107">Uppdaterat Azure.Core till 1.4.1</span><span class="sxs-lookup"><span data-stu-id="a850c-107">Updated Azure.Core to 1.4.1</span></span>

#### <a name="azaks"></a><span data-ttu-id="a850c-108">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="a850c-108">Az.Aks</span></span>
* <span data-ttu-id="a850c-109">Valideringslogiken för parametern "New-AzAksCluster", "Set-AzAksCluster" och "New-AzAksNodePool" har lagts till på klientsidan.</span><span class="sxs-lookup"><span data-stu-id="a850c-109">Added client side parameter validation logic for 'New-AzAksCluster', 'Set-AzAksCluster' and 'New-AzAksNodePool'.</span></span> <span data-ttu-id="a850c-110">[#12372]</span><span class="sxs-lookup"><span data-stu-id="a850c-110">[#12372]</span></span>
* <span data-ttu-id="a850c-111">Stöd har lagts till för tillägg i "New-AzAksCluster".</span><span class="sxs-lookup"><span data-stu-id="a850c-111">Added support for add-ons in 'New-AzAksCluster'.</span></span> <span data-ttu-id="a850c-112">[#11239]</span><span class="sxs-lookup"><span data-stu-id="a850c-112">[#11239]</span></span>
* <span data-ttu-id="a850c-113">Cmdlet:arna "Enable-AzAksAddOn" och "Disable-AzAksAddOn" har lagts till för tillägg.</span><span class="sxs-lookup"><span data-stu-id="a850c-113">Added cmdlets 'Enable-AzAksAddOn' and 'Disable-AzAksAddOn' for add-ons.</span></span> <span data-ttu-id="a850c-114">[#11239]</span><span class="sxs-lookup"><span data-stu-id="a850c-114">[#11239]</span></span>
* <span data-ttu-id="a850c-115">Parametern "GenerateSshKey" har lagts till för "New-AzAksCluster".</span><span class="sxs-lookup"><span data-stu-id="a850c-115">Added parameter 'GenerateSshKey' for 'New-AzAksCluster'.</span></span> <span data-ttu-id="a850c-116">[#12371]</span><span class="sxs-lookup"><span data-stu-id="a850c-116">[#12371]</span></span>
* <span data-ttu-id="a850c-117">API-versionen har uppdaterats till 2020-06-01.</span><span class="sxs-lookup"><span data-stu-id="a850c-117">Updated api version to 2020-06-01.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="a850c-118">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a850c-118">Az.CognitiveServices</span></span>
* <span data-ttu-id="a850c-119">Visade ytterligare juridiska villkor för vissa API:er.</span><span class="sxs-lookup"><span data-stu-id="a850c-119">Showed additional legal terms for certain APIs.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a850c-120">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a850c-120">Az.Compute</span></span>
* <span data-ttu-id="a850c-121">Den valfria parametern "EncryptionType" har lagts till i "New-AzVmDiskEncryptionSetConfig"</span><span class="sxs-lookup"><span data-stu-id="a850c-121">Added the '-EncryptionType' optional parameter to 'New-AzVmDiskEncryptionSetConfig'</span></span>
* <span data-ttu-id="a850c-122">Nya cmdlet:ar för ny resurs typ: DiskAccess "Get-AzDiskAccess", "New-AzDiskAccess", "Get-AzDiskAccess"</span><span class="sxs-lookup"><span data-stu-id="a850c-122">New cmdlets for new resource type: DiskAccess 'Get-AzDiskAccess', 'New-AzDiskAccess', 'Get-AzDiskAccess'</span></span>
* <span data-ttu-id="a850c-123">De valfria parametrarna "-DiskAccessId" och "-NetworkAccessPolicy" har lagts till i "New-AzSnapshotConfig"</span><span class="sxs-lookup"><span data-stu-id="a850c-123">Added optional parameters '-DiskAccessId' and '-NetworkAccessPolicy' to 'New-AzSnapshotConfig'</span></span>
* <span data-ttu-id="a850c-124">De valfria parametrarna "-DiskAccessId" och "-NetworkAccessPolicy" har lagts till i "New-AzDiskConfig"</span><span class="sxs-lookup"><span data-stu-id="a850c-124">Added optional parameters '-DiskAccessId' and '-NetworkAccessPolicy' to 'New-AzDiskConfig'</span></span>
* <span data-ttu-id="a850c-125">PatchStatus-egenskapen har lagts till i VirtualMachine-instansvyn</span><span class="sxs-lookup"><span data-stu-id="a850c-125">Added 'PatchStatus' property to VirtualMachine Instance View</span></span>
* <span data-ttu-id="a850c-126">Egenskapen "VMHealth" har lagts till i den virtuella datorns instansvy, vilket är det returnerade objektet när "get-AzVm" anropas med "-Status"</span><span class="sxs-lookup"><span data-stu-id="a850c-126">Added 'VMHealth' property to the virtual machine's instance view, which is the returned object when 'Get-AzVm' is invoked with '-Status'</span></span>
* <span data-ttu-id="a850c-127">Fältet "AssignedHost" har lagts till i instansvyerna "Get-AzVM" och "Get-AzVmss".</span><span class="sxs-lookup"><span data-stu-id="a850c-127">Added 'AssignedHost' field to 'Get-AzVM' and 'Get-AzVmss' instance views.</span></span> <span data-ttu-id="a850c-128">I fältet visas resurs-ID för den virtuella datorinstansen</span><span class="sxs-lookup"><span data-stu-id="a850c-128">The field shows the resource id of the virtual machine instance</span></span>
* <span data-ttu-id="a850c-129">Den valfria parametern "-SupportAutomaticPlacement" har lagts till i "New-AzHostGroup"</span><span class="sxs-lookup"><span data-stu-id="a850c-129">Added optional parameter '-SupportAutomaticPlacement' to 'New-AzHostGroup'</span></span> 
* <span data-ttu-id="a850c-130">Parametern "-HostGroupId" har lagts till i "New-AzVm" och "New-AzVmss"</span><span class="sxs-lookup"><span data-stu-id="a850c-130">Added the '-HostGroupId' parameter to 'New-AzVm' and 'New-AzVmss'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a850c-131">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a850c-131">Az.DataFactory</span></span>
* <span data-ttu-id="a850c-132">ADF .Net SDK har uppdaterats till version 4.11.0</span><span class="sxs-lookup"><span data-stu-id="a850c-132">Updated ADF .Net SDK version to 4.11.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="a850c-133">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a850c-133">Az.EventHub</span></span>
* <span data-ttu-id="a850c-134">Nya kluster-cmdlet:ar – "New-AzEventHubCluster", "Set-AzEventHubCluster", "Get-AzEventHubCluster", "Remove-AzEventHubCluster", "Get-AzEventHubClustersAvailableRegions" har lagts till.</span><span class="sxs-lookup"><span data-stu-id="a850c-134">Added new Cluster cmdlets - 'New-AzEventHubCluster', 'Set-AzEventHubCluster', 'Get-AzEventHubCluster', 'Remove-AzEventHubCluster', 'Get-AzEventHubClustersAvailableRegions'.</span></span>
* <span data-ttu-id="a850c-135">Åtgärdat för ärende #10722 : Korrigering för tilldelning av enbart lyssning till AuthorizationRule-rättigheter.</span><span class="sxs-lookup"><span data-stu-id="a850c-135">Fixed for issue #10722 : Fix for assigning only 'Listen' to AuthorizationRule rights.</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="a850c-136">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="a850c-136">Az.Functions</span></span>
* <span data-ttu-id="a850c-137">Möjligheten att skapa v2-funktioner i regioner som inte stöder det har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="a850c-137">Removed the ability to create v2 Functions in regions that do not support it.</span></span>
* <span data-ttu-id="a850c-138">Föråldrad PowerShell 6.2.</span><span class="sxs-lookup"><span data-stu-id="a850c-138">Deprecated PowerShell 6.2.</span></span> <span data-ttu-id="a850c-139">En varning har lagts till när en användare skapar en PowerShell 6.2-funktionsapp som uppmanar till att skapa en PowerShell 7.0-funktionsapp i stället.</span><span class="sxs-lookup"><span data-stu-id="a850c-139">Added a warning for when a user creates a PowerShell 6.2 function app that advises them to create a PowerShell 7.0 function app instead.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="a850c-140">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a850c-140">Az.HDInsight</span></span>
* <span data-ttu-id="a850c-141">Stöd för att skapa kluster med automatisk skalningskonfiguration</span><span class="sxs-lookup"><span data-stu-id="a850c-141">Supported creating cluster with Autoscale configuration</span></span>
    - <span data-ttu-id="a850c-142">Lägg till den nya parametern "AutoscaleConfiguration" till cmdleten ”New-AzHDInsightCluster”</span><span class="sxs-lookup"><span data-stu-id="a850c-142">Add new parameter 'AutoscaleConfiguration' to the cmdlet 'New-AzHDInsightCluster'</span></span>
* <span data-ttu-id="a850c-143">Stöd för att använda automatisk skalningskonfiguration i kluster</span><span class="sxs-lookup"><span data-stu-id="a850c-143">Supported operating cluster's Autoscale configuration</span></span>
    - <span data-ttu-id="a850c-144">Lägg till ny cmdlet "Get-AzHDInsihgtClusterAutoscaleConfiguration"</span><span class="sxs-lookup"><span data-stu-id="a850c-144">Add new cmdlet 'Get-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="a850c-145">Lägg till ny cmdlet "New-AzHDInsihgtClusterAutoscaleConfiguration"</span><span class="sxs-lookup"><span data-stu-id="a850c-145">Add new cmdlet 'New-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="a850c-146">Lägg till ny cmdlet "Set-AzHDInsihgtClusterAutoscaleConfiguration"</span><span class="sxs-lookup"><span data-stu-id="a850c-146">Add new cmdlet 'Set-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="a850c-147">Lägg till ny cmdlet "Remove-AzHDInsihgtClusterAutoscaleConfiguration"</span><span class="sxs-lookup"><span data-stu-id="a850c-147">Add new cmdlet 'Remove-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="a850c-148">Lägg till ny cmdlet "New-AzHDInsihgtClusterAutoscaleScheduleCondition"</span><span class="sxs-lookup"><span data-stu-id="a850c-148">Add new cmdlet 'New-AzHDInsihgtClusterAutoscaleScheduleCondition'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a850c-149">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a850c-149">Az.KeyVault</span></span>
* <span data-ttu-id="a850c-150">Stöd har lagts till för RBAC-auktorisering [#10557]</span><span class="sxs-lookup"><span data-stu-id="a850c-150">Added support for RBAC authorization [#10557]</span></span>
* <span data-ttu-id="a850c-151">Förbättrad felhantering i "Set-AzKeyVaultAccessPolicy" [#4007]</span><span class="sxs-lookup"><span data-stu-id="a850c-151">Enhanced error handling in 'Set-AzKeyVaultAccessPolicy' [#4007]</span></span>

#### <a name="azkusto"></a><span data-ttu-id="a850c-152">Az.Kusto</span><span class="sxs-lookup"><span data-stu-id="a850c-152">Az.Kusto</span></span>
* <span data-ttu-id="a850c-153">Allmän tillgänglighet för "Az.Kusto"-modulen</span><span class="sxs-lookup"><span data-stu-id="a850c-153">General availability of 'Az.Kusto' module</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a850c-154">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a850c-154">Az.Network</span></span>
* <span data-ttu-id="a850c-155">[Viktig ändring] Uppdaterade nedanstående cmdlets för att justera resursens virtuella router och virtuella hubb</span><span class="sxs-lookup"><span data-stu-id="a850c-155">[Breaking Change] Updated below cmdlets to align resource virtual router and virtual hub</span></span>
    - <span data-ttu-id="a850c-156">"New-AzVirtualRouter":</span><span class="sxs-lookup"><span data-stu-id="a850c-156">'New-AzVirtualRouter':</span></span> 
        - <span data-ttu-id="a850c-157">Parametern-HostedSubnet har lagts till för att stödja underordnad resurs för IP-konfiguration</span><span class="sxs-lookup"><span data-stu-id="a850c-157">Added -HostedSubnet parameter to support IP configuration child resource</span></span>
        - <span data-ttu-id="a850c-158">-HostedGateway och -HostedGatewayId har tagits bort</span><span class="sxs-lookup"><span data-stu-id="a850c-158">deleted -HostedGateway and -HostedGatewayId</span></span>
    - <span data-ttu-id="a850c-159">'Get-AzVirtualRouter':</span><span class="sxs-lookup"><span data-stu-id="a850c-159">'Get-AzVirtualRouter':</span></span>
        - <span data-ttu-id="a850c-160">Parameteruppsättningen har lagts till på prenumerationsnivå</span><span class="sxs-lookup"><span data-stu-id="a850c-160">Added subscription level parameter set</span></span>
    - <span data-ttu-id="a850c-161">"Remove-AzVirtualRouter"</span><span class="sxs-lookup"><span data-stu-id="a850c-161">'Remove-AzVirtualRouter'</span></span>
    - <span data-ttu-id="a850c-162">"Add-AzVirtualRouterPeer"</span><span class="sxs-lookup"><span data-stu-id="a850c-162">'Add-AzVirtualRouterPeer'</span></span>
    - <span data-ttu-id="a850c-163">"Get-AzVirtualRouterPeer"</span><span class="sxs-lookup"><span data-stu-id="a850c-163">'Get-AzVirtualRouterPeer'</span></span>
    - <span data-ttu-id="a850c-164">"Remove-AzVirtualRouterPeer"</span><span class="sxs-lookup"><span data-stu-id="a850c-164">'Remove-AzVirtualRouterPeer'</span></span>
* <span data-ttu-id="a850c-165">Ny cmdlet har lagts till för Azure Express Route-port</span><span class="sxs-lookup"><span data-stu-id="a850c-165">Added new cmdlet for Azure Express Route Port</span></span>
    - <span data-ttu-id="a850c-166">"New-AzExpressRoutePortLOA"</span><span class="sxs-lookup"><span data-stu-id="a850c-166">'New-AzExpressRoutePortLOA'</span></span>
* <span data-ttu-id="a850c-167">Egenskapen RemoteBgpCommunities har lagts till i VirtualNetwork Peering-resursen</span><span class="sxs-lookup"><span data-stu-id="a850c-167">Added RemoteBgpCommunities property to the VirtualNetwork Peering Resource</span></span>
* <span data-ttu-id="a850c-168">Ändrade varningsmeddelandet för ”New-AzLoadBalancerFrontendIpConfig”, ”New-AzPublicIpAddress” och ”New-AzPublicIpPrefix”.</span><span class="sxs-lookup"><span data-stu-id="a850c-168">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>
* <span data-ttu-id="a850c-169">Lade till VpnGatewayIpConfigurations till "Get-AzVpnGateway"-utdata</span><span class="sxs-lookup"><span data-stu-id="a850c-169">Added VpnGatewayIpConfigurations to 'Get-AzVpnGateway' output</span></span>
* <span data-ttu-id="a850c-170">Åtgärdade bugg för "Set-AzApplicationGatewaySslCertificate" [#9488]</span><span class="sxs-lookup"><span data-stu-id="a850c-170">Fixed bug for 'Set-AzApplicationGatewaySslCertificate' [#9488]</span></span>
* <span data-ttu-id="a850c-171">Parametern "AllowActiveFTP" har lagts till i "AzureFirewall"</span><span class="sxs-lookup"><span data-stu-id="a850c-171">Added 'AllowActiveFTP' parameter to 'AzureFirewall'</span></span>
* <span data-ttu-id="a850c-172">Nedanstående kommandon för funktionen har uppdaterats: Aktivera konfiguration/borttagning för Internetsäkerhet på VirtualWan P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="a850c-172">Updated below commands for feature: Enable internet security set/remove on VirtualWan P2SVpnGateway.</span></span>
- <span data-ttu-id="a850c-173">"New-AzP2sVpnGateway" har uppdaterats": Den valfria växelparametern "EnableInternetSecurityFlag" har lagts till för kunder som anger värdet true för att aktivera Internetsäkerhet på P2SVpnGateway, som ska användas för plats-till-plats-klienter.</span><span class="sxs-lookup"><span data-stu-id="a850c-173">Updated 'New-AzP2sVpnGateway': Added optional switch parameter 'EnableInternetSecurityFlag' for customers to set true to enable internet security on P2SVpnGateway, which will be applied for Point to site clients.</span></span>
- <span data-ttu-id="a850c-174">"Update-AzP2sVpnGateway" har uppdaterats: De valfria växelparametrarna "EnableInternetSecurityFlag" eller "DisableInternetSecurityFlag" har lagts till för kunder som anger värdet true/false för att aktivera/inaktivera Internetsäkerhet på P2SVpnGateway, som ska användas för plats-till-plats-klienter.</span><span class="sxs-lookup"><span data-stu-id="a850c-174">Updated 'Update-AzP2sVpnGateway': Added optional switch parameters 'EnableInternetSecurityFlag' or 'DisableInternetSecurityFlag' for customers to set true/false to enable/disable internet security on P2SVpnGateway, which will be applied for Point to site clients.</span></span>
* <span data-ttu-id="a850c-175">Den nya cmdleten "Reset-AzP2sVpnGateway" har lagts till för att kunder ska kunna återställa/starta om sina VirtualWan-P2SVpnGateway för felsökning.</span><span class="sxs-lookup"><span data-stu-id="a850c-175">Added new cmdlet 'Reset-AzP2sVpnGateway' for customers to reset/reboot their VirtualWan P2SVpnGateway for troubleshooting.</span></span>
* <span data-ttu-id="a850c-176">Den nya cmdleten "Reset-AzVpnGateway" har lagts till för att kunder ska kunna återställa/starta om VirtualWan VpnGateway för felsökning.</span><span class="sxs-lookup"><span data-stu-id="a850c-176">Added new cmdlet 'Reset-AzVpnGateway' for customers to reset/reboot their VirtualWan VpnGateway for troubleshooting.</span></span>
* <span data-ttu-id="a850c-177">"Set-AzVirtualNetworkSubnetConfig" har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="a850c-177">Updated 'Set-AzVirtualNetworkSubnetConfig'</span></span>
    - <span data-ttu-id="a850c-178">Ange egenskaper för NSG och routningstabell för undernät till null om det anges explicit i parametrarna [#1548] [#9718]</span><span class="sxs-lookup"><span data-stu-id="a850c-178">Set NSG and Route Table properties of subnet to null if explicitly set in parameters [#1548][#9718]</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a850c-179">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a850c-179">Az.RecoveryServices</span></span>
* <span data-ttu-id="a850c-180">Åtgärdat borttagningstillståndet för säkerhetskopieringsobjekt.</span><span class="sxs-lookup"><span data-stu-id="a850c-180">Fixed the Delete State for workload Backup Items.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a850c-181">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a850c-181">Az.Resources</span></span>
* <span data-ttu-id="a850c-182">Lagt till saknad kontroll för Set-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="a850c-182">Added missing check for Set-AzRoleAssignment</span></span>
* <span data-ttu-id="a850c-183">Attribut som medför icke-bakåtkompatibel ändring har lagts till i parametern "SubscriptionId" i "Get-AzResourceGroupDeploymentOperation"</span><span class="sxs-lookup"><span data-stu-id="a850c-183">Added breaking change attribute to 'SubscriptionId' parameter of 'Get-AzResourceGroupDeploymentOperation'</span></span>
* <span data-ttu-id="a850c-184">Uppdaterat What-If-cmdlets i ARM-mall så att resursändringar av typen 'Ignorera' visas sist</span><span class="sxs-lookup"><span data-stu-id="a850c-184">Updated ARM template What-If cmdlets to show 'Ignore' resource changes last</span></span>
* <span data-ttu-id="a850c-185">Åtgärdat serialiseringsproblem med säkra parametrar och matrisparametrar för distributionscmdlets [#12773]</span><span class="sxs-lookup"><span data-stu-id="a850c-185">Fixed secure and array parameter serialization issues for deployment cmdlets [#12773]</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a850c-186">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a850c-186">Az.ServiceFabric</span></span>
* <span data-ttu-id="a850c-187">Nya cmdletar har lagts till för hanterade kluster och nodtyper:</span><span class="sxs-lookup"><span data-stu-id="a850c-187">Added new cmdlets for managed clusters and node types:</span></span>
    - <span data-ttu-id="a850c-188">"New-AzServiceFabricManagedCluster"</span><span class="sxs-lookup"><span data-stu-id="a850c-188">'New-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="a850c-189">"Get-AzServiceFabricManagedCluster"</span><span class="sxs-lookup"><span data-stu-id="a850c-189">'Get-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="a850c-190">"Set-AzServiceFabricManagedCluster"</span><span class="sxs-lookup"><span data-stu-id="a850c-190">'Set-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="a850c-191">"Remove-AzServiceFabricManagedCluster"</span><span class="sxs-lookup"><span data-stu-id="a850c-191">'Remove-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="a850c-192">"Add-AzServiceFabricManagedClusterClientCertificate"</span><span class="sxs-lookup"><span data-stu-id="a850c-192">'Add-AzServiceFabricManagedClusterClientCertificate'</span></span>
    - <span data-ttu-id="a850c-193">"Remove-AzServiceFabricManagedClusterClientCertificate"</span><span class="sxs-lookup"><span data-stu-id="a850c-193">'Remove-AzServiceFabricManagedClusterClientCertificate'</span></span>
    - <span data-ttu-id="a850c-194">"New-AzServiceFabricManagedNodeType"</span><span class="sxs-lookup"><span data-stu-id="a850c-194">'New-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="a850c-195">"Get-AzServiceFabricManagedNodeType"</span><span class="sxs-lookup"><span data-stu-id="a850c-195">'Get-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="a850c-196">"Set-AzServiceFabricManagedNodeType"</span><span class="sxs-lookup"><span data-stu-id="a850c-196">'Set-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="a850c-197">"Remove-AzServiceFabricManagedNodeType"</span><span class="sxs-lookup"><span data-stu-id="a850c-197">'Remove-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="a850c-198">"Add-AzServiceFabricManagedNodeTypeVMExtension"</span><span class="sxs-lookup"><span data-stu-id="a850c-198">'Add-AzServiceFabricManagedNodeTypeVMExtension'</span></span>
    - <span data-ttu-id="a850c-199">"Add-AzServiceFabricManagedNodeTypeVMSecret"</span><span class="sxs-lookup"><span data-stu-id="a850c-199">'Add-AzServiceFabricManagedNodeTypeVMSecret'</span></span>
    - <span data-ttu-id="a850c-200">"Remove-AzServiceFabricManagedNodeTypeVMExtension"</span><span class="sxs-lookup"><span data-stu-id="a850c-200">'Remove-AzServiceFabricManagedNodeTypeVMExtension'</span></span>
    - <span data-ttu-id="a850c-201">"Restart-AzServiceFabricManagedNodeTyp"</span><span class="sxs-lookup"><span data-stu-id="a850c-201">'Restart-AzServiceFabricManagedNodeTyp'</span></span>
* <span data-ttu-id="a850c-202">Service Fabric SDK har uppgraderats till version 1.2.0 som använder Service Fabric-resursprovidern med API-version 2020-03-01 för aktuell modell och 2020-01-01-förhandsversion för hanterade kluster.</span><span class="sxs-lookup"><span data-stu-id="a850c-202">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2020-03-01 for the current model and 2020-01-01-preview for managed clusters.</span></span>

#### <a name="azsql"></a><span data-ttu-id="a850c-203">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a850c-203">Az.Sql</span></span>
* <span data-ttu-id="a850c-204">BackupStorageRedundancy har lagts till i "New-AzSqlInstance" och "Get-AzSqlInstance"</span><span class="sxs-lookup"><span data-stu-id="a850c-204">Added BackupStorageRedundancy to 'New-AzSqlInstance' and 'Get-AzSqlInstance'</span></span>
* <span data-ttu-id="a850c-205">Cmdlet:en "Get-AzSqlServerActiveDirectoryOnlyAuthentication" har lagts till</span><span class="sxs-lookup"><span data-stu-id="a850c-205">Added cmdlet 'Get-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="a850c-206">Cmdlet:en "Enable-AzSqlServerActiveDirectoryOnlyAuthentication" har lagts till</span><span class="sxs-lookup"><span data-stu-id="a850c-206">Added cmdlet 'Enable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="a850c-207">Force-parametern har lagts till i "New-AzSqlInstance"</span><span class="sxs-lookup"><span data-stu-id="a850c-207">Added Force parameter to 'New-AzSqlInstance'</span></span>
* <span data-ttu-id="a850c-208">Cmdlet:ar för logguppspelningstjänst för hanterade databaser har lagts till</span><span class="sxs-lookup"><span data-stu-id="a850c-208">Added cmdlets for Managed Database Log Replay service</span></span>
    - <span data-ttu-id="a850c-209">"Start-AzSqlInstanceDatabaseLogReplay"</span><span class="sxs-lookup"><span data-stu-id="a850c-209">'Start-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="a850c-210">"Get-AzSqlInstanceDatabaseLogReplay"</span><span class="sxs-lookup"><span data-stu-id="a850c-210">'Get-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="a850c-211">"Complete-AzSqlInstanceDatabaseLogReplay"</span><span class="sxs-lookup"><span data-stu-id="a850c-211">'Complete-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="a850c-212">"Stop-AzSqlInstanceDatabaseLogReplay"</span><span class="sxs-lookup"><span data-stu-id="a850c-212">'Stop-AzSqlInstanceDatabaseLogReplay'</span></span>
* <span data-ttu-id="a850c-213">Cmdlet:en "Get-AzSqlInstanceActiveDirectoryOnlyAuthentication" har lagts till</span><span class="sxs-lookup"><span data-stu-id="a850c-213">Added cmdlet 'Get-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="a850c-214">Cmdlet:en "Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication" har lagts till</span><span class="sxs-lookup"><span data-stu-id="a850c-214">Added cmdlet 'Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="a850c-215">Cmdlet:en "Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication" har lagts till</span><span class="sxs-lookup"><span data-stu-id="a850c-215">Added cmdlet 'Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="a850c-216">Cmdletarna "New-AzSqlDatabaseImport" och "New-AzSqlDatabaseExport" har uppdaterats för att stödja funktioner för nätverksisolering</span><span class="sxs-lookup"><span data-stu-id="a850c-216">Updated cmdlets 'New-AzSqlDatabaseImport' and 'New-AzSqlDatabaseExport' to support network isolation functionality</span></span>
* <span data-ttu-id="a850c-217">Cmdleten "New-AzSqlDatabaseImportExisting" har lagts till</span><span class="sxs-lookup"><span data-stu-id="a850c-217">Added cmdlet 'New-AzSqlDatabaseImportExisting'</span></span>
* <span data-ttu-id="a850c-218">Uppdaterade databas-cmdlet:ar som stöder typspecifikation av lagringsenhet för säkerhetskopiering</span><span class="sxs-lookup"><span data-stu-id="a850c-218">Updated Databases cmdlets to support backup storage type specification</span></span>
* <span data-ttu-id="a850c-219">Force-parametern har lagts till i "New-AzSqlDatabase"</span><span class="sxs-lookup"><span data-stu-id="a850c-219">Added Force parameter to 'New-AzSqlDatabase'</span></span>
* <span data-ttu-id="a850c-220">Varning för BackupStorageRedundancy-konfiguration har lagts till i utvalda regioner i "New-AzSqlDatabase"</span><span class="sxs-lookup"><span data-stu-id="a850c-220">Added warning for BackupStorageRedundancy configuration in select regions in 'New-AzSqlDatabase'</span></span>
* <span data-ttu-id="a850c-221">Uppdaterade ActiveDirectoryOnlyAuthentication-cmdletar för server och instans så att de innehåller ResourceId och InputObject</span><span class="sxs-lookup"><span data-stu-id="a850c-221">Updated ActiveDirectoryOnlyAuthentication cmdlets for server and instance to include ResourceId and InputObject</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a850c-222">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a850c-222">Az.Storage</span></span>
* <span data-ttu-id="a850c-223">Åtgärdade fel vid uppladdning av blob genom uppgradering till Microsoft.Azure.Storage.DataMovement 2.0.0 [#12220]</span><span class="sxs-lookup"><span data-stu-id="a850c-223">Fixed upload blob fail by upgrade to Microsoft.Azure.Storage.DataMovement 2.0.0 [#12220]</span></span>
* <span data-ttu-id="a850c-224">Stöd för återställning baserat på tidpunkt</span><span class="sxs-lookup"><span data-stu-id="a850c-224">Supported Point In Time Restore</span></span>
    - <span data-ttu-id="a850c-225">"Enable-AzStorageBlobRestorePolicy"</span><span class="sxs-lookup"><span data-stu-id="a850c-225">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="a850c-226">"Disable-AzStorageBlobRestorePolicy"</span><span class="sxs-lookup"><span data-stu-id="a850c-226">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="a850c-227">"New-AzStorageBlobRangeToRestore"</span><span class="sxs-lookup"><span data-stu-id="a850c-227">'New-AzStorageBlobRangeToRestore'</span></span>
    - <span data-ttu-id="a850c-228">"Restore-AzStorageBlobRange"</span><span class="sxs-lookup"><span data-stu-id="a850c-228">'Restore-AzStorageBlobRange'</span></span>
* <span data-ttu-id="a850c-229">Stöd för att hämta status för blobåterställning genom att köra get-AzureRMStorageAccount med parametern -IncludeBlobRestoreStatus</span><span class="sxs-lookup"><span data-stu-id="a850c-229">Supported get blob restore status of Storage account by run get-AzureRMStorageAccount with parameter -IncludeBlobRestoreStatus</span></span> 
    - <span data-ttu-id="a850c-230">"Get-AzureRMStorageAccount"</span><span class="sxs-lookup"><span data-stu-id="a850c-230">'Get-AzureRMStorageAccount'</span></span>
* <span data-ttu-id="a850c-231">Meddelande om icke-bakåtkompatibel ändring för kommande ändring av cmdlet-utdata har lagts till</span><span class="sxs-lookup"><span data-stu-id="a850c-231">Added breaking change warning message for upcoming cmdlet output change</span></span>
    - <span data-ttu-id="a850c-232">"Get-AzStorageContainerStoredAccessPolicy"</span><span class="sxs-lookup"><span data-stu-id="a850c-232">'Get-AzStorageContainerStoredAccessPolicy'</span></span>
    - <span data-ttu-id="a850c-233">"Set-AzStorageContainerStoredAccessPolicy"</span><span class="sxs-lookup"><span data-stu-id="a850c-233">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
    - <span data-ttu-id="a850c-234">"Set-AzStorageAccountManagementPolicy"</span><span class="sxs-lookup"><span data-stu-id="a850c-234">'Set-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="a850c-235">"Get-AzStorageAccountManagementPolicy"</span><span class="sxs-lookup"><span data-stu-id="a850c-235">'Get-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="a850c-236">"Add-AzStorageAccountManagementPolicyAction"</span><span class="sxs-lookup"><span data-stu-id="a850c-236">'Add-AzStorageAccountManagementPolicyAction'</span></span>
    - <span data-ttu-id="a850c-237">"New-AzStorageAccountManagementPolicyRule"</span><span class="sxs-lookup"><span data-stu-id="a850c-237">'New-AzStorageAccountManagementPolicyRule'</span></span>
* <span data-ttu-id="a850c-238">Uppgraderade Microsoft.Azure.Cosmos.Table SDK till 1.0.8</span><span class="sxs-lookup"><span data-stu-id="a850c-238">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.8</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="a850c-239">Tack till våra community-deltagare</span><span class="sxs-lookup"><span data-stu-id="a850c-239">Thanks to our community contributors</span></span>
* <span data-ttu-id="a850c-240">Thomas Van Laere (@ThomVanL), Lägg till Dockerfile-alpine-3.10 (#12911)</span><span class="sxs-lookup"><span data-stu-id="a850c-240">Thomas Van Laere (@ThomVanL), Add Dockerfile-alpine-3.10 (#12911)</span></span> 
* <span data-ttu-id="a850c-241">Lohith Chowdary Chilukuri (@Lochiluk), Uppdatering av Remove-AzNetworkInterfaceIpConfig.md (#12807)</span><span class="sxs-lookup"><span data-stu-id="a850c-241">Lohith Chowdary Chilukuri (@Lochiluk), Update Remove-AzNetworkInterfaceIpConfig.md (#12807)</span></span> 
* <span data-ttu-id="a850c-242">Roberth Strand (@roberthstrand), Get-AzResourceGroup – Nytt exempel och rensning (#12828)</span><span class="sxs-lookup"><span data-stu-id="a850c-242">Roberth Strand (@roberthstrand), Get-AzResourceGroup - New example, and cleanup (#12828)</span></span> 
* <span data-ttu-id="a850c-243">Ravi Mishra (@inmishrar), uppdatering av Azure Web App-körningsstack till DOTNETCORE (#12833)</span><span class="sxs-lookup"><span data-stu-id="a850c-243">Ravi Mishra (@inmishrar), update Azure Web App runtime stack to DOTNETCORE (#12833)</span></span> 
* <span data-ttu-id="a850c-244">@jack-education, uppdaterat set-AzVirtualNetworkSubnetConfig för att tillåta att NSG och routningstabell tas bort från undernät (#12351)</span><span class="sxs-lookup"><span data-stu-id="a850c-244">@jack-education, Updated Set-AzVirtualNetworkSubnetConfig to allow NSG and Route Table to be removed from subnet (#12351)</span></span> 
* <span data-ttu-id="a850c-245">@hagop-globanet, uppdatering av Add-AzApplicationGatewayCustomError.md (#12784)</span><span class="sxs-lookup"><span data-stu-id="a850c-245">@hagop-globanet, Update Add-AzApplicationGatewayCustomError.md (#12784)</span></span> 
* <span data-ttu-id="a850c-246">Joshua Van Daalen (@greenSacrifice)</span><span class="sxs-lookup"><span data-stu-id="a850c-246">Joshua Van Daalen (@greenSacrifice)</span></span>
  * <span data-ttu-id="a850c-247">Uppdatering av stavning av egenskaper till egenskaper (#12821)</span><span class="sxs-lookup"><span data-stu-id="a850c-247">Update spelling of Property to Property (#12821)</span></span> 
  * <span data-ttu-id="a850c-248">Uppdatering av New-AzResourceLock.md-exempel (#12806)</span><span class="sxs-lookup"><span data-stu-id="a850c-248">Update New-AzResourceLock.md examples (#12806)</span></span>
* <span data-ttu-id="a850c-249">Eragon Riddle (@eragonriddle), korrigerat fältnamn för parameter i exemplet (#12825)</span><span class="sxs-lookup"><span data-stu-id="a850c-249">Eragon Riddle (@eragonriddle), Corrected parameter field name in the example (#12825)</span></span> 
* <span data-ttu-id="a850c-250">@rossifumax, åtgärdat skrivfel i New-AzConfigurationAssignment.md (#12701)</span><span class="sxs-lookup"><span data-stu-id="a850c-250">@rossifumax, Fix typo in New-AzConfigurationAssignment.md (#12701)</span></span>

## <a name="461---august-2020"></a><span data-ttu-id="a850c-251">4.6.1 – augusti 2020</span><span class="sxs-lookup"><span data-stu-id="a850c-251">4.6.1 - August 2020</span></span>
#### <a name="azcompute"></a><span data-ttu-id="a850c-252">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a850c-252">Az.Compute</span></span>
* <span data-ttu-id="a850c-253">Korrigerade EncryptionAtHost-parametern i New-AzVm för att ta bort standardvärdet FALSE [#12776]</span><span class="sxs-lookup"><span data-stu-id="a850c-253">Patched '-EncryptionAtHost' parameter in 'New-AzVm' to remove default value of false [#12776]</span></span>

## <a name="460---august-2020"></a><span data-ttu-id="a850c-254">4.6.0 – augusti 2020</span><span class="sxs-lookup"><span data-stu-id="a850c-254">4.6.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a850c-255">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a850c-255">Az.Accounts</span></span>
* <span data-ttu-id="a850c-256">Alla offentliga molnmiljöer läses in när slutpunktsidentifieringen inte returnerar AzureCloud (standard) eller andra offentliga miljöer [#12633]</span><span class="sxs-lookup"><span data-stu-id="a850c-256">Loaded all public cloud environments when discovery endpoint doesn't return default AzureCloud or other public environments [#12633]</span></span>
* <span data-ttu-id="a850c-257">SubscriptionPolicies har exponerats i Get-AzSubscription [#12551]</span><span class="sxs-lookup"><span data-stu-id="a850c-257">Exposed SubscriptionPolicies in 'Get-AzSubscription' [#12551]</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a850c-258">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a850c-258">Az.Automation</span></span>
* <span data-ttu-id="a850c-259">Parametern -RunOn har lagts till i Set-AzAutomationWebhook för att ange en Hybrid Worker-grupp</span><span class="sxs-lookup"><span data-stu-id="a850c-259">Added '-RunOn' parameters to 'Set-AzAutomationWebhook' to specify a Hybrid Worker Group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a850c-260">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a850c-260">Az.Compute</span></span>
* <span data-ttu-id="a850c-261">Parametern -EncryptionAtHost har lagts till i New-AzVm, New-AzVmss, New-AzVMConfig, New-AzVmssConfig, Update-AzVM och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a850c-261">Added '-EncryptionAtHost' parameter to 'New-AzVm', 'New-AzVmss', 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVM', and 'Update-AzVmss'</span></span>
* <span data-ttu-id="a850c-262">SecurityProfile har lagts till i Get-AzVM och Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a850c-262">Added 'SecurityProfile' to 'Get-AzVM' and 'Get-AzVmss' return object</span></span>
* <span data-ttu-id="a850c-263">Växeln -InstanceView har lagts till som valfri parameter i Get-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="a850c-263">Added '-InstanceView' switch as optional parameter to 'Get-AzHostGroup'</span></span>
* <span data-ttu-id="a850c-264">En ny cmdlet, Invoke-AzVmPatchAssessment, har lagts till</span><span class="sxs-lookup"><span data-stu-id="a850c-264">Added new cmdlet 'Invoke-AzVmPatchAssessment'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a850c-265">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a850c-265">Az.DataFactory</span></span>
* <span data-ttu-id="a850c-266">Saknade egenskaper har lagts till i klassen PSPipelineRun.</span><span class="sxs-lookup"><span data-stu-id="a850c-266">Added missing properties to PSPipelineRun class.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="a850c-267">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a850c-267">Az.HDInsight</span></span>
* <span data-ttu-id="a850c-268">Stöd för att skapa kluster med funktionen för kryptering under överföring.</span><span class="sxs-lookup"><span data-stu-id="a850c-268">Supported creating cluster with encryption at host feature.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a850c-269">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a850c-269">Az.KeyVault</span></span>
* <span data-ttu-id="a850c-270">Varningsmeddelanden har lagts till för planering att inaktivera mjuk borttagning</span><span class="sxs-lookup"><span data-stu-id="a850c-270">Added warning messages for planning to disable soft delete</span></span>
* <span data-ttu-id="a850c-271">Varningsmeddelanden har lagts till för planering att ta bort attributet SecretValueText</span><span class="sxs-lookup"><span data-stu-id="a850c-271">Added warning messages for planning to remove attribute SecretValueText</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="a850c-272">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="a850c-272">Az.Maintenance</span></span>
* <span data-ttu-id="a850c-273">Valfria schemarelaterade fält har lagts till i New-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="a850c-273">Added optional schedule related fields to 'New-AzMaintenanceConfiguration'</span></span>
* <span data-ttu-id="a850c-274">En ny cmdlet har lagts till för Get-AzMaintenancePublicConfiguration</span><span class="sxs-lookup"><span data-stu-id="a850c-274">Added new cmdlet for 'Get-AzMaintenancePublicConfiguration'</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="a850c-275">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="a850c-275">Az.ManagedServices</span></span>
* <span data-ttu-id="a850c-276">Varningar har lagts till om icke-bakåtkompatibla ändringar för cmdletar för tilldelning och definition av hanterade tjänster</span><span class="sxs-lookup"><span data-stu-id="a850c-276">Added breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a850c-277">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a850c-277">Az.Monitor</span></span>
* <span data-ttu-id="a850c-278">Utökade parametern som angetts i Set-AzDiagnosticSetting för separering av aktivering av loggar och mått [#12482]</span><span class="sxs-lookup"><span data-stu-id="a850c-278">Extended the parameter set in 'Set-AzDiagnosticSetting' for separation of Logs and Metrics enablement [#12482]</span></span>
* <span data-ttu-id="a850c-279">Åtgärdat fel för Add-AzMetricAlertRuleV2 vid hämtning av måttavisering från pipelinen</span><span class="sxs-lookup"><span data-stu-id="a850c-279">Fixed bug for 'Add-AzMetricAlertRuleV2' when getting metric alert from pipeline</span></span>

#### <a name="azresources"></a><span data-ttu-id="a850c-280">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a850c-280">Az.Resources</span></span>
* <span data-ttu-id="a850c-281">Get-AzPolicyAlias-svaret har uppdaterats för att ta med information som anger om aliaset kan ändras eller inte av Azure Policy.</span><span class="sxs-lookup"><span data-stu-id="a850c-281">Updated 'Get-AzPolicyAlias' response to include information indicating whether the alias is modifiable by Azure Policy.</span></span>
* <span data-ttu-id="a850c-282">Skapade en ny cmdlet, set-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="a850c-282">Created new cmdlet 'Set-AzRoleAssignment'</span></span>
* <span data-ttu-id="a850c-283">Get-AzDeploymentManagementGroupWhatIfResult har lagts till för att hämta What-If-resultat för ARM-mall i hanteringsgruppsomfånget</span><span class="sxs-lookup"><span data-stu-id="a850c-283">Added 'Get-AzDeploymentManagementGroupWhatIfResult' for getting ARM template What-If results at management Group scope</span></span>
* <span data-ttu-id="a850c-284">En ny cmdlet, Get-AzTenantWhatIfResult, har lagts till för att hämta What-If-resultat för ARM-mall i klientorganisationsomfånget</span><span class="sxs-lookup"><span data-stu-id="a850c-284">Added 'Get-AzTenantWhatIfResult' new cmdlet for getting ARM template What-If results at tenant scope</span></span>
* <span data-ttu-id="a850c-285">-WhatIf och -Confirm har åsidosatts för New-AzManagementGroupDeployment och New-AzTenantDeployment för att använda What-If-resultat för ARM-mall</span><span class="sxs-lookup"><span data-stu-id="a850c-285">Overrode '-WhatIf' and '-Confirm' for 'New-AzManagementGroupDeployment' and 'New-AzTenantDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="a850c-286">Beteenden har åtgärdats för -WhatIf och -Confirm för nya cmdletar för distribution så att de stämmer överens med False och</span><span class="sxs-lookup"><span data-stu-id="a850c-286">Fixed the behaviors of '-WhatIf' and '-Confirm' for new deployment cmdlets so they comply with False and</span></span> 
* <span data-ttu-id="a850c-287">Serialiseringsfel har åtgärdats för -TemplateObject och TemplateParameterObject [#1528] [#6292]</span><span class="sxs-lookup"><span data-stu-id="a850c-287">Fixed serialization error for '-TemplateObject' and 'TemplateParameterObject' [#1528] [#6292]</span></span>
* <span data-ttu-id="a850c-288">Attribut som medför icke-bakåtkompatibel ändring har lagts till i Get-AzResourceGroupDeploymentOperation för den kommande ändringen av utdatatyp</span><span class="sxs-lookup"><span data-stu-id="a850c-288">Added breaking change attribute to 'Get-AzResourceGroupDeploymentOperation' for the upcoming output type change</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="a850c-289">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="a850c-289">Az.SignalR</span></span>
* <span data-ttu-id="a850c-290">Fel i hjälpfilerna Restart-AzSignalR och Update-AzSignalR har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="a850c-290">Fixed 'Restart-AzSignalR' and 'Update-AzSignalR' help files errors</span></span>
* <span data-ttu-id="a850c-291">Cmdletarna Update-AzSignalRNetworkAcl och Set-AzSignalRUpstream har lagts till</span><span class="sxs-lookup"><span data-stu-id="a850c-291">Added cmdlets 'Update-AzSignalRNetworkAcl', 'Set-AzSignalRUpstream'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a850c-292">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a850c-292">Az.Storage</span></span>
* <span data-ttu-id="a850c-293">Stöd för blobfrågeacceleration</span><span class="sxs-lookup"><span data-stu-id="a850c-293">Supported blob query acceleration</span></span>
    -  <span data-ttu-id="a850c-294">Get-AzStorageBlobQueryResult</span><span class="sxs-lookup"><span data-stu-id="a850c-294">'Get-AzStorageBlobQueryResult'</span></span>
    -  <span data-ttu-id="a850c-295">New-AzStorageBlobQueryConfig</span><span class="sxs-lookup"><span data-stu-id="a850c-295">'New-AzStorageBlobQueryConfig'</span></span>
* <span data-ttu-id="a850c-296">Hjälpfil har lagts till, ytterligare beskrivning har lagts till och stavfel har korrigerats</span><span class="sxs-lookup"><span data-stu-id="a850c-296">Updated help file, added more description, and fixed typo</span></span>
    -  <span data-ttu-id="a850c-297">”Start-AzStorageBlobCopy”</span><span class="sxs-lookup"><span data-stu-id="a850c-297">'Start-AzStorageBlobCopy'</span></span>
    -  <span data-ttu-id="a850c-298">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="a850c-298">'Get-AzDataLakeGen2Item'</span></span>
* <span data-ttu-id="a850c-299">Problem med att ladda ned blob när relaterad underordnad katalog saknas har åtgärdats [#12592]</span><span class="sxs-lookup"><span data-stu-id="a850c-299">Fixed download blob fail when related sub directory not exist [#12592]</span></span>
    -  <span data-ttu-id="a850c-300">”Get-AzStorageBlobContent”</span><span class="sxs-lookup"><span data-stu-id="a850c-300">'Get-AzStorageBlobContent'</span></span>
* <span data-ttu-id="a850c-301">Replikeringsprincip för att ange, hämta, ta bort objekt på Storage-konton stöds</span><span class="sxs-lookup"><span data-stu-id="a850c-301">Supported Set/Get/Remove Object Replication Policy on Storage accounts</span></span>
    - <span data-ttu-id="a850c-302">New-AzStorageObjectReplicationPolicyRule</span><span class="sxs-lookup"><span data-stu-id="a850c-302">'New-AzStorageObjectReplicationPolicyRule'</span></span>
    - <span data-ttu-id="a850c-303">Set-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="a850c-303">'Set-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="a850c-304">Get-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="a850c-304">'Get-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="a850c-305">Remove-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="a850c-305">'Remove-AzStorageObjectReplicationPolicy'</span></span>
* <span data-ttu-id="a850c-306">Stöd har lagts till för att aktivera/inaktivera ChangeFeed i Blob Service för ett Storage-konto</span><span class="sxs-lookup"><span data-stu-id="a850c-306">Supported enable/disable ChangeFeed on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="a850c-307">”Update-AzStorageBlobServiceProperty”</span><span class="sxs-lookup"><span data-stu-id="a850c-307">'Update-AzStorageBlobServiceProperty'</span></span>

## <a name="450---august-2020"></a><span data-ttu-id="a850c-308">4.5.0 – augusti 2020</span><span class="sxs-lookup"><span data-stu-id="a850c-308">4.5.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a850c-309">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a850c-309">Az.Accounts</span></span>
* <span data-ttu-id="a850c-310">Uppdaterade ”Connect-AzAccount” så att det accepterar parametern ”MaxContextPopulation” [#9865]</span><span class="sxs-lookup"><span data-stu-id="a850c-310">Updated 'Connect-AzAccount' to accept parameter 'MaxContextPopulation' [#9865]</span></span>
* <span data-ttu-id="a850c-311">Uppdaterade SubscriptionClient-versionen till 2019-06-01 och visa klientdomäner [#9838]</span><span class="sxs-lookup"><span data-stu-id="a850c-311">Updated SubscriptionClient version to 2019-06-01 and display tenant domains [#9838]</span></span>
* <span data-ttu-id="a850c-312">Information om hemklientorganisation och managedBy-klientorganisation som stöds för prenumerationen</span><span class="sxs-lookup"><span data-stu-id="a850c-312">Supported home tenant and managedBy tenant information of subscription</span></span>
* <span data-ttu-id="a850c-313">Korrigerade modulnamn, versionsinformation i telemetridata</span><span class="sxs-lookup"><span data-stu-id="a850c-313">Corrected module name, version info in telemetry data</span></span>
* <span data-ttu-id="a850c-314">Justerade SqlDatabaseDnsSuffix och ServiceManagementUrl om miljöns slutpunkt för metadata returnerar ett inkompatibelt värde</span><span class="sxs-lookup"><span data-stu-id="a850c-314">Adjusted SqlDatabaseDnsSuffix and ServiceManagementUrl if environment metadata endpoint returns incompatible value</span></span>

#### <a name="azaks"></a><span data-ttu-id="a850c-315">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="a850c-315">Az.Aks</span></span>
* <span data-ttu-id="a850c-316">Tog bort ”ClientIdAndSecret” för ”ServicePrincipalIdAndSecret” och ställde in ”ClientIdAndSecret” som ett alias [#12381].</span><span class="sxs-lookup"><span data-stu-id="a850c-316">Removed 'ClientIdAndSecret' to 'ServicePrincipalIdAndSecret' and set 'ClientIdAndSecret' as an alias [#12381].</span></span>
* <span data-ttu-id="a850c-317">Tog bort ”Get-AzAks”/”New-AzAks”/”Remove-AzAks”/”Set-AzAks” för ”Get-AzAksCluster”/”New-AzAksCluster”/”Remove-AzAksCluster”/”Set-AzAksCluster” och ställde in de ursprungliga som alias [#12373].</span><span class="sxs-lookup"><span data-stu-id="a850c-317">Removed 'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks' to 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster' and set the original ones as alias [#12373].</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="a850c-318">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a850c-318">Az.ApiManagement</span></span>
* <span data-ttu-id="a850c-319">Lade till ny cmdlet: ”Add-AzApiManagementApiToGateway”.</span><span class="sxs-lookup"><span data-stu-id="a850c-319">Added new 'Add-AzApiManagementApiToGateway' cmdlet.</span></span>
* <span data-ttu-id="a850c-320">Lade till ny cmdlet: ”Get-AzApiManagementGateway”.</span><span class="sxs-lookup"><span data-stu-id="a850c-320">Added new 'Get-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="a850c-321">Lade till ny cmdlet: ”Get-AzApiManagementGatewayHostnameConfiguration”.</span><span class="sxs-lookup"><span data-stu-id="a850c-321">Added new 'Get-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="a850c-322">Lade till ny cmdlet: ”Get-AzApiManagementGatewayKey”.</span><span class="sxs-lookup"><span data-stu-id="a850c-322">Added new 'Get-AzApiManagementGatewayKey' cmdlet.</span></span>
* <span data-ttu-id="a850c-323">Lade till ny cmdlet: ”New-AzApiManagementGateway”.</span><span class="sxs-lookup"><span data-stu-id="a850c-323">Added new 'New-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="a850c-324">Lade till ny cmdlet: ”New-AzApiManagementGatewayHostnameConfiguration”.</span><span class="sxs-lookup"><span data-stu-id="a850c-324">Added new 'New-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="a850c-325">Lade till ny cmdlet: ”New-AzApiManagementResourceLocationObject”.</span><span class="sxs-lookup"><span data-stu-id="a850c-325">Added new 'New-AzApiManagementResourceLocationObject' cmdlet.</span></span>
* <span data-ttu-id="a850c-326">Lade till ny cmdlet: ”Remove-AzApiManagementApiFromGateway”.</span><span class="sxs-lookup"><span data-stu-id="a850c-326">Added new 'Remove-AzApiManagementApiFromGateway' cmdlet.</span></span>
* <span data-ttu-id="a850c-327">Lade till ny cmdlet: ”Remove-AzApiManagementGateway”.</span><span class="sxs-lookup"><span data-stu-id="a850c-327">Added new 'Remove-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="a850c-328">Lade till ny cmdlet: ”Remove-AzApiManagementGatewayHostnameConfiguration”.</span><span class="sxs-lookup"><span data-stu-id="a850c-328">Added new 'Remove-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="a850c-329">Lade till ny cmdlet: ”Update-AzApiManagementGateway”.</span><span class="sxs-lookup"><span data-stu-id="a850c-329">Added new 'Update-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="a850c-330">Lade till den nya valfria parametern [-GatewayId] till cmdleten ”Get-AzApiManagementApi”.</span><span class="sxs-lookup"><span data-stu-id="a850c-330">Added new optional [-GatewayId] parameter to the 'Get-AzApiManagementApi' cmdlet.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="a850c-331">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a850c-331">Az.CognitiveServices</span></span>
* <span data-ttu-id="a850c-332">Använde ”Neka” som standardåtgärd för NetworkRules.</span><span class="sxs-lookup"><span data-stu-id="a850c-332">Used 'Deny' specifically as NetworkRules default action.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="a850c-333">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="a850c-333">Az.FrontDoor</span></span>
* <span data-ttu-id="a850c-334">Åtgärdade ett problem där ett undantag uppstår när Enum.Parse försöker att tvinga ett null-värde till aktiverade eller inaktiverade uppräkningsvärden [#12344]</span><span class="sxs-lookup"><span data-stu-id="a850c-334">Fixed an issue where an exception is being thrown when Enum.Parse tries to coerce a null value to an Enabled or Disabled enum values [#12344]</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="a850c-335">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a850c-335">Az.HDInsight</span></span>
* <span data-ttu-id="a850c-336">Stöd för att skapa kluster med funktionen Kryptering under överföring.</span><span class="sxs-lookup"><span data-stu-id="a850c-336">Supported creating cluster with encryption in transit feature.</span></span>
    - <span data-ttu-id="a850c-337">Lägg till den nya parametern ”EncryptionInTransit” till cmdleten ”New-AzHDInsightCluster”</span><span class="sxs-lookup"><span data-stu-id="a850c-337">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="a850c-338">Lägg till den nya parametern ”EncryptionInTransit” till cmdleten ”New-AzHDInsightClusterConfig”</span><span class="sxs-lookup"><span data-stu-id="a850c-338">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="a850c-339">Stöd för att skapa kluster med funktionen privat länk:</span><span class="sxs-lookup"><span data-stu-id="a850c-339">Supported creating cluster with private link feature:</span></span>
    - <span data-ttu-id="a850c-340">Lägg till de nya parametrarna ”PublicNetworkAccessType” och ”OutboundPublicNetworkAccessType” till cmdleten ”New-AzHDInsightCluster”</span><span class="sxs-lookup"><span data-stu-id="a850c-340">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="a850c-341">Lägg till de nya parametrarna ”PublicNetworkAccessType” och ”OutboundPublicNetworkAccessType” till cmdleten ”New-AzHDInsightClusterConfig”</span><span class="sxs-lookup"><span data-stu-id="a850c-341">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="a850c-342">Returnerade information om det virtuella nätverket vid anrop till ”New-AzHDInsightCluster” eller ”Get-AzHDInsightCluster”</span><span class="sxs-lookup"><span data-stu-id="a850c-342">Returned virtual network information when calling 'New-AzHDInsightCluster' or 'Get-AzHDInsightCluster'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a850c-343">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a850c-343">Az.Network</span></span>
* <span data-ttu-id="a850c-344">Stöd har lagts till för parametern AddressPrefixType i ”Remove-AzExpressRouteCircuitConnectionConfig”</span><span class="sxs-lookup"><span data-stu-id="a850c-344">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="a850c-345">Lade till bakåtkompatibel ändringar: PeerAddressType-funktioner för privat peering i ”Remove-AzExpressRouteCircutPeeringConfig”.</span><span class="sxs-lookup"><span data-stu-id="a850c-345">Added non-breaking changes: PeerAddressType functionality for Private Peering in 'Remove-AzExpressRouteCircutPeeringConfig'.</span></span>
* <span data-ttu-id="a850c-346">Koden ändrades för att ignorera skiftläge för parametrarna AddressPrefixType och PeerAddressType.</span><span class="sxs-lookup"><span data-stu-id="a850c-346">Code changed to ignore case for AddressPrefixType and PeerAddressType parameter.</span></span>
* <span data-ttu-id="a850c-347">Ändrade varningsmeddelandet för ”New-AzLoadBalancerFrontendIpConfig”, ”New-AzPublicIpAddress” och ”New-AzPublicIpPrefix”.</span><span class="sxs-lookup"><span data-stu-id="a850c-347">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="a850c-348">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a850c-348">Az.OperationalInsights</span></span>
* <span data-ttu-id="a850c-349">Lade till alternativet ”-ForceDelete” för ”Remove-AzOperationalInsightsworkspace”</span><span class="sxs-lookup"><span data-stu-id="a850c-349">Added '-ForceDelete' option for 'Remove-AzOperationalInsightsworkspace'</span></span>
* <span data-ttu-id="a850c-350">Lade till ny cmdlet: ”Get-AzOperationalInsightsDeletedWorkspace”</span><span class="sxs-lookup"><span data-stu-id="a850c-350">Added new cmdlet 'Get-AzOperationalInsightsDeletedWorkspace'</span></span>
* <span data-ttu-id="a850c-351">Lade till ny cmdlet: ”Restore-AzOperationalInsightsWorkspace”</span><span class="sxs-lookup"><span data-stu-id="a850c-351">Added new cmdlet 'Restore-AzOperationalInsightsWorkspace'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a850c-352">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a850c-352">Az.RecoveryServices</span></span>
* <span data-ttu-id="a850c-353">Förbättrade sättet Azure Backup-containrar/objekt identifieras.</span><span class="sxs-lookup"><span data-stu-id="a850c-353">Improved the Azure Backup container/item discovery experience.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a850c-354">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a850c-354">Az.Resources</span></span>
* <span data-ttu-id="a850c-355">Lade till egenskaperna ”Condition”, ”ConditionVersion” och ”Description” till ”New-AzRoleAssignment”</span><span class="sxs-lookup"><span data-stu-id="a850c-355">Added properties 'Condition', 'ConditionVersion' and 'Description' to 'New-AzRoleAssignment'</span></span>
    - <span data-ttu-id="a850c-356">Detta omfattade alla relevanta ändringar av datamodellerna</span><span class="sxs-lookup"><span data-stu-id="a850c-356">This included all the relevant changes to the data models</span></span>

#### <a name="azsql"></a><span data-ttu-id="a850c-357">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a850c-357">Az.Sql</span></span>
* <span data-ttu-id="a850c-358">Korrigerade ett potentiellt fel med skiftlägesokänsliga servernamn i ”New-AzSqlServer” och ”Set-AzSqlServer”</span><span class="sxs-lookup"><span data-stu-id="a850c-358">Fixed potential server name case insensitive error in 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="a850c-359">Korrigerade att fel databasnamn returnerades vid ett befintligt databasfel i ”New-AzSqlDatabaseSecondary”</span><span class="sxs-lookup"><span data-stu-id="a850c-359">Fixed wrong database name returned on existing database error in 'New-AzSqlDatabaseSecondary'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a850c-360">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a850c-360">Az.Storage</span></span>
* <span data-ttu-id="a850c-361">Stöd för att skapa container/blob för SAS-token med de nya behörigheterna x, t</span><span class="sxs-lookup"><span data-stu-id="a850c-361">Supported create container/blob Sas token with new permission x,t</span></span>
    -  <span data-ttu-id="a850c-362">”New-AzStorageBlobSASToken”</span><span class="sxs-lookup"><span data-stu-id="a850c-362">'New-AzStorageBlobSASToken'</span></span>
    -  <span data-ttu-id="a850c-363">”New-AzStorageContainerSASToken”</span><span class="sxs-lookup"><span data-stu-id="a850c-363">'New-AzStorageContainerSASToken'</span></span>
* <span data-ttu-id="a850c-364">Stöd för att skapa konto för SAS-token med de nya behörigheterna x, t, f</span><span class="sxs-lookup"><span data-stu-id="a850c-364">Supported create account Sas token with new permission x,t,f</span></span>
    -  <span data-ttu-id="a850c-365">”New-AzStorageAccountSASToken”</span><span class="sxs-lookup"><span data-stu-id="a850c-365">'New-AzStorageAccountSASToken'</span></span>
* <span data-ttu-id="a850c-366">Stöd för att hämta förbrukning av enskild filresurs</span><span class="sxs-lookup"><span data-stu-id="a850c-366">Supported get single file share usage</span></span>
    - <span data-ttu-id="a850c-367">”Get-AzRmStorageShare”</span><span class="sxs-lookup"><span data-stu-id="a850c-367">'Get-AzRmStorageShare'</span></span>

## <a name="440---july-2020"></a><span data-ttu-id="a850c-368">4.4.0 – juli 2020</span><span class="sxs-lookup"><span data-stu-id="a850c-368">4.4.0 - July 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a850c-369">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a850c-369">Az.Accounts</span></span>
* <span data-ttu-id="a850c-370">En ny cmdlet, ”Invoke-AzRestMethod”, har lagts till</span><span class="sxs-lookup"><span data-stu-id="a850c-370">Added new cmdlet 'Invoke-AzRestMethod'</span></span>
* <span data-ttu-id="a850c-371">Ett problem åtgärdades som kan orsaka autentiseringsfel i scenarier med fler processer, t.ex. när flera Azure PowerShell-cmdletar körs med ”Start-Job” [#9448]</span><span class="sxs-lookup"><span data-stu-id="a850c-371">Fixed an issue that may cause authentication errors in multi-process scenarios such as running multiple Azure PowerShell cmdlets using 'Start-Job' [#9448]</span></span>

#### <a name="azaks"></a><span data-ttu-id="a850c-372">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="a850c-372">Az.Aks</span></span>
* <span data-ttu-id="a850c-373">Felet som gjorde att ”Get-AzAks” inte hämtade alla kluster har åtgärdats [#12296]</span><span class="sxs-lookup"><span data-stu-id="a850c-373">Fixed bug 'Get-AzAks' doesn't get all clusters [#12296]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="a850c-374">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a850c-374">Az.AnalysisServices</span></span>
* <span data-ttu-id="a850c-375">Projektreferensen till autentisering har tagits bort</span><span class="sxs-lookup"><span data-stu-id="a850c-375">Removed project reference to Authentication</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a850c-376">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a850c-376">Az.Automation</span></span>
* <span data-ttu-id="a850c-377">Problemet som gjorde att strängar med escape-tecken inte kunde konverteras till JSON-objekt har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="a850c-377">Fixed the issue that string with escape chars cannot be converted into json object.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a850c-378">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a850c-378">Az.Compute</span></span>
* <span data-ttu-id="a850c-379">En varning har lats till som visas när ”New-AzVmss” används utan den senaste avbildningsversionen</span><span class="sxs-lookup"><span data-stu-id="a850c-379">Added warning when using 'New-AzVmss' without 'latest' image version</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a850c-380">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a850c-380">Az.DataFactory</span></span>
* <span data-ttu-id="a850c-381">Globala parametrar har lagts till för Data Factory.</span><span class="sxs-lookup"><span data-stu-id="a850c-381">Added global parameters to Data Factory.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="a850c-382">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="a850c-382">Az.EventGrid</span></span>
* <span data-ttu-id="a850c-383">Modulen har uppdaterats så att API-version 2020-06-01 används.</span><span class="sxs-lookup"><span data-stu-id="a850c-383">Updated to use the 2020-06-01 API version.</span></span>
* <span data-ttu-id="a850c-384">Nya funktioner har lagts till:</span><span class="sxs-lookup"><span data-stu-id="a850c-384">Added new features:</span></span>
    - <span data-ttu-id="a850c-385">Indatamappning</span><span class="sxs-lookup"><span data-stu-id="a850c-385">Input mapping</span></span>
    - <span data-ttu-id="a850c-386">Schema för händelseleverans</span><span class="sxs-lookup"><span data-stu-id="a850c-386">Event Delivery Schema</span></span>
    - <span data-ttu-id="a850c-387">Private Link</span><span class="sxs-lookup"><span data-stu-id="a850c-387">Private Link</span></span>
    - <span data-ttu-id="a850c-388">Cloud Event V10 Schema</span><span class="sxs-lookup"><span data-stu-id="a850c-388">Cloud Event V10 Schema</span></span>
    - <span data-ttu-id="a850c-389">Service Bus-ämne som mål</span><span class="sxs-lookup"><span data-stu-id="a850c-389">Service Bus Topic As Destination</span></span>
    - <span data-ttu-id="a850c-390">Azure-funktion som mål</span><span class="sxs-lookup"><span data-stu-id="a850c-390">Azure Function As Destination</span></span>
    - <span data-ttu-id="a850c-391">Webhook-batchbearbetning</span><span class="sxs-lookup"><span data-stu-id="a850c-391">WebHook Batching</span></span>
    - <span data-ttu-id="a850c-392">Säker webhook (AAD-stöd)</span><span class="sxs-lookup"><span data-stu-id="a850c-392">Secure webhook (AAD support)</span></span>
    - <span data-ttu-id="a850c-393">IpFiltering</span><span class="sxs-lookup"><span data-stu-id="a850c-393">IpFiltering</span></span>
* <span data-ttu-id="a850c-394">Uppdaterade cmdletar:</span><span class="sxs-lookup"><span data-stu-id="a850c-394">Updated cmdlets:</span></span>
    - <span data-ttu-id="a850c-395">”New-AzEventGridSubscription”/”Update-AzEventGridSubscription”:</span><span class="sxs-lookup"><span data-stu-id="a850c-395">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span></span>
        - <span data-ttu-id="a850c-396">Lägg till nya valfria parametrar för att ge stöd för webhook-batchbearbetning.</span><span class="sxs-lookup"><span data-stu-id="a850c-396">Add new optional parameters to support webhook batching.</span></span>
        - <span data-ttu-id="a850c-397">Lägg till nya valfria parametrar för att ge stöd för skyddad webhook med AAD.</span><span class="sxs-lookup"><span data-stu-id="a850c-397">Add new optional parameters to support secured webhook using AAD.</span></span>
        - <span data-ttu-id="a850c-398">Lägg till ny enum (uppräkning) för EndpointType-parametern för att ge stöd för Azure-funktion och Service Bus-ämne som nya mål.</span><span class="sxs-lookup"><span data-stu-id="a850c-398">Add new enum for EndpointType parameter to support azure function and service bus topic as new destinations.</span></span>
        - <span data-ttu-id="a850c-399">Lägg till ny valfri parameter för leveransschema.</span><span class="sxs-lookup"><span data-stu-id="a850c-399">Add new optional parameter for delivery schema.</span></span>
    - <span data-ttu-id="a850c-400">”New-AzEventGridTopic”/”Update-AzEventGridTopic” och ”New-AzEventGridDomain”/”Update-AzEventGridDomain”:</span><span class="sxs-lookup"><span data-stu-id="a850c-400">'New-AzEventGridTopic'/'Update-AzEventGridTopic' and 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span></span>
        - <span data-ttu-id="a850c-401">Lägg till nya valfria parametrar för att ge stöd för IpFiltering.</span><span class="sxs-lookup"><span data-stu-id="a850c-401">Add new optional parameters to support IpFiltering.</span></span>
    - <span data-ttu-id="a850c-402">”New-AzEventGridTopic”/”New-AzEventGridDomain”:</span><span class="sxs-lookup"><span data-stu-id="a850c-402">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span></span>
        - <span data-ttu-id="a850c-403">Lägg till nya valfria parametrar för att ge stöd för indatamappning.</span><span class="sxs-lookup"><span data-stu-id="a850c-403">Add new optional parameters to support Input mapping.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="a850c-404">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="a850c-404">Az.FrontDoor</span></span>
* <span data-ttu-id="a850c-405">Modulen har uppdaterats så att API 2020-05-01 används</span><span class="sxs-lookup"><span data-stu-id="a850c-405">Updated module to use API 2020-05-01</span></span>
* <span data-ttu-id="a850c-406">Stöd för privat länk har lagts till för Storage-, KeyVault- och Web App Service-resurser</span><span class="sxs-lookup"><span data-stu-id="a850c-406">Added Private link support for Storage, Keyvault and Web App Service resources</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="a850c-407">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a850c-407">Az.HDInsight</span></span>
* <span data-ttu-id="a850c-408">Stöd för att skapa kluster med ADLSGen1/2-lagring i nationella moln.</span><span class="sxs-lookup"><span data-stu-id="a850c-408">Supported creating cluster with ADLSGen1/2 storage in national clouds.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a850c-409">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a850c-409">Az.Monitor</span></span>
* <span data-ttu-id="a850c-410">Bugg som orsakade fel med ”Get-AzDiagnosticSetting” när mått eller loggar var null har åtgärdats [#12272]</span><span class="sxs-lookup"><span data-stu-id="a850c-410">Fixed bug for 'Get-AzDiagnosticSetting' when metrics or logs are null [#12272]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a850c-411">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a850c-411">Az.Network</span></span>
* <span data-ttu-id="a850c-412">Parameterväxlingen i VWan HubVnet-anslutningar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="a850c-412">Fixed parameters swap in VWan HubVnet connection</span></span>
* <span data-ttu-id="a850c-413">Nya cmdletar har lagts till för platser för virtuella installationer i Azure-nätverk</span><span class="sxs-lookup"><span data-stu-id="a850c-413">Added new cmdlets for Azure Network Virtual Appliance Sites</span></span>
    - <span data-ttu-id="a850c-414">”Get-AzVirtualApplianceSite”</span><span class="sxs-lookup"><span data-stu-id="a850c-414">'Get-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="a850c-415">”New-AzVirtualApplianceSite”</span><span class="sxs-lookup"><span data-stu-id="a850c-415">'New-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="a850c-416">”Remove-AzVirtualApplianceSite”</span><span class="sxs-lookup"><span data-stu-id="a850c-416">'Remove-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="a850c-417">”Update-AzVirtualApplianceSite”</span><span class="sxs-lookup"><span data-stu-id="a850c-417">'Update-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="a850c-418">”New-AzOffice365PolicyProperty”</span><span class="sxs-lookup"><span data-stu-id="a850c-418">'New-AzOffice365PolicyProperty'</span></span>
* <span data-ttu-id="a850c-419">Nya cmdletar har lagts till för virtuella installationer i Azure-nätverk</span><span class="sxs-lookup"><span data-stu-id="a850c-419">Added new cmdlets for Azure Network Virtual Appliance</span></span>
    - <span data-ttu-id="a850c-420">”Get-AzNetworkVirtualAppliance”</span><span class="sxs-lookup"><span data-stu-id="a850c-420">'Get-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="a850c-421">”New-AzNetworkVirtualAppliance”</span><span class="sxs-lookup"><span data-stu-id="a850c-421">'New-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="a850c-422">”Remove-AzNetworkVirtualAppliance”</span><span class="sxs-lookup"><span data-stu-id="a850c-422">'Remove-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="a850c-423">”Update-AzNetworkVirtualAppliance”</span><span class="sxs-lookup"><span data-stu-id="a850c-423">'Update-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="a850c-424">”Get-AzNetworkVirtualApplianceSku”</span><span class="sxs-lookup"><span data-stu-id="a850c-424">'Get-AzNetworkVirtualApplianceSku'</span></span>
    - <span data-ttu-id="a850c-425">”New-AzVirtualApplianceSkuProperty”</span><span class="sxs-lookup"><span data-stu-id="a850c-425">'New-AzVirtualApplianceSkuProperty'</span></span>
* <span data-ttu-id="a850c-426">Application Gateway har introducerats i vanliga cmdletar för Private Link</span><span class="sxs-lookup"><span data-stu-id="a850c-426">Onboarded Application Gateway to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="a850c-427">StorageSync har introducerats i vanliga cmdletar för Private Link</span><span class="sxs-lookup"><span data-stu-id="a850c-427">Onboarded StorageSync to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="a850c-428">SignalR har introducerats i vanliga cmdletar för Private Link</span><span class="sxs-lookup"><span data-stu-id="a850c-428">Onboarded SignalR to Private Link Common Cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a850c-429">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a850c-429">Az.RecoveryServices</span></span>
* <span data-ttu-id="a850c-430">Projektreferensen till autentisering har tagits bort</span><span class="sxs-lookup"><span data-stu-id="a850c-430">Removed project reference to Authentication</span></span>
* <span data-ttu-id="a850c-431">Azure Backup-anpassade cmdletar gör text mer korrekt.</span><span class="sxs-lookup"><span data-stu-id="a850c-431">Azure Backup tuned cmdlets help text to be more accurate.</span></span>
* <span data-ttu-id="a850c-432">Stöd har lagts till som gör att Azure Backup kan hämta MAB-agentjobb med cmdleten ”Get-AzRecoveryServicesBackupJob”.</span><span class="sxs-lookup"><span data-stu-id="a850c-432">Azure Backup added support for fetching MAB agent jobs using 'Get-AzRecoveryServicesBackupJob' cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a850c-433">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a850c-433">Az.Resources</span></span>
* <span data-ttu-id="a850c-434">”Save-AzResourceGroupDeploymentTemplate” har uppdaterats för att använda SDK:n.</span><span class="sxs-lookup"><span data-stu-id="a850c-434">Updated 'Save-AzResourceGroupDeploymentTemplate' to use the SDK.</span></span>
* <span data-ttu-id="a850c-435">Cmdleten ”Unregister-AzResourceProvider” har lagts till.</span><span class="sxs-lookup"><span data-stu-id="a850c-435">Added 'Unregister-AzResourceProvider' cmdlet.</span></span>

#### <a name="azsql"></a><span data-ttu-id="a850c-436">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a850c-436">Az.Sql</span></span>
* <span data-ttu-id="a850c-437">Stöd har lagts till för SPN och gästanvändare i cmdleten ”Set-AzSqlInstanceActiveDirectoryAdministrator”</span><span class="sxs-lookup"><span data-stu-id="a850c-437">Added support for Service principal and guest users in Set-AzSqlInstanceActiveDirectoryAdministrator cmdlet'</span></span>
* <span data-ttu-id="a850c-438">En bugg har åtgärdats i cmdletar för dataklassificering.</span><span class="sxs-lookup"><span data-stu-id="a850c-438">Fixed a bug in Data Classification cmdlets.'</span></span>
* <span data-ttu-id="a850c-439">Stöd har lagts till för redundansväxling med Azure SQL Managed Instance: ”Invoke-AzSqlInstanceFailover”</span><span class="sxs-lookup"><span data-stu-id="a850c-439">Added support for Azure SQL Managed Instance failover: 'Invoke-AzSqlInstanceFailover'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a850c-440">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a850c-440">Az.Storage</span></span>
* <span data-ttu-id="a850c-441">Problemet som gjorde att UserAgent inte lades till för vissa cmdletar för dataplanet har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="a850c-441">Fixed the issue that UserAgent is not added for some data plane cmdlets.</span></span>
* <span data-ttu-id="a850c-442">Stöd har lagts till för att skapa/uppdatera Storage-konto med MinimumTlsVersion och AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="a850c-442">Supported create/update Storage account with MinimumTlsVersion and AllowBlobPublicAccess</span></span>
    -  <span data-ttu-id="a850c-443">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="a850c-443">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="a850c-444">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="a850c-444">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="a850c-445">Stöd har lagts till för att aktivera/inaktivera versionshantering i Blob Service för ett Storage-konto</span><span class="sxs-lookup"><span data-stu-id="a850c-445">Support enable/disable versioning on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="a850c-446">”Update-AzStorageBlobServiceProperty”</span><span class="sxs-lookup"><span data-stu-id="a850c-446">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="a850c-447">Stöd har lagts till för att visa blobar med blobversioner</span><span class="sxs-lookup"><span data-stu-id="a850c-447">Support list blobs with blob versions</span></span>
    - <span data-ttu-id="a850c-448">”Get-AzStorageBlob”</span><span class="sxs-lookup"><span data-stu-id="a850c-448">'Get-AzStorageBlob'</span></span>
* <span data-ttu-id="a850c-449">Stöd har lagts till för att hämta/ta bort enskilda ögonblicksbilder av blobar eller blobversioner</span><span class="sxs-lookup"><span data-stu-id="a850c-449">Support get/remove single blob snapshot or blob version</span></span>
    - <span data-ttu-id="a850c-450">”Get-AzStorageBlob”</span><span class="sxs-lookup"><span data-stu-id="a850c-450">'Get-AzStorageBlob'</span></span>
    - <span data-ttu-id="a850c-451">”Remove-AzStorageBlob”</span><span class="sxs-lookup"><span data-stu-id="a850c-451">'Remove-AzStorageBlob'</span></span>
* <span data-ttu-id="a850c-452">Stöd har lagts till för pipelines från blobobjekt genererade av Azure.Storage.Blobs V12</span><span class="sxs-lookup"><span data-stu-id="a850c-452">Support pipeline from blob object generated from Azure.Storage.Blobs V12</span></span>
    - <span data-ttu-id="a850c-453">”Get-AzStorageBlobContent”</span><span class="sxs-lookup"><span data-stu-id="a850c-453">'Get-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="a850c-454">”New-AzStorageBlobSASToken”</span><span class="sxs-lookup"><span data-stu-id="a850c-454">'New-AzStorageBlobSASToken'</span></span>
    - <span data-ttu-id="a850c-455">”Remove-AzStorageBlob”</span><span class="sxs-lookup"><span data-stu-id="a850c-455">'Remove-AzStorageBlob'</span></span>
    - <span data-ttu-id="a850c-456">”Set-AzStorageBlobContent”</span><span class="sxs-lookup"><span data-stu-id="a850c-456">'Set-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="a850c-457">”Start-AzStorageBlobCopy”</span><span class="sxs-lookup"><span data-stu-id="a850c-457">'Start-AzStorageBlobCopy'</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="a850c-458">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="a850c-458">Az.StorageSync</span></span>
* <span data-ttu-id="a850c-459">En ny version har lagts till för StorageSync SDK som körs mot ApiVersion 2020-03-01</span><span class="sxs-lookup"><span data-stu-id="a850c-459">Added a new version StorageSync SDK targeting ApiVersion 2020-03-01</span></span>
* <span data-ttu-id="a850c-460">En cmdlet för synkroniseringstjänsten för lagringsuppdatering har lagts till</span><span class="sxs-lookup"><span data-stu-id="a850c-460">Added Update Storage Sync Service cmdlet</span></span>
    - <span data-ttu-id="a850c-461">”Set-AzStorageSyncService”</span><span class="sxs-lookup"><span data-stu-id="a850c-461">'Set-AzStorageSyncService'</span></span>
* <span data-ttu-id="a850c-462">IncomingTrafficPolicy och PrivateEndpointConnections har lagts till för StorageSyncService-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="a850c-462">Added IncomingTrafficPolicy and PrivateEndpointConnections to StorageSyncService cmdlets.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a850c-463">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a850c-463">Az.Websites</span></span>
* <span data-ttu-id="a850c-464">Stöd har lagts till för att utföra åtgärder för platser som inte tillhör samma resursgrupp som App Services-planen</span><span class="sxs-lookup"><span data-stu-id="a850c-464">Added support to perform operations for Slots not in the same resource group as the App Service Plan</span></span>

## <a name="430---june-2020"></a><span data-ttu-id="a850c-465">4.3.0 – juni 2020</span><span class="sxs-lookup"><span data-stu-id="a850c-465">4.3.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a850c-466">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a850c-466">Az.Accounts</span></span>
* <span data-ttu-id="a850c-467">Stöd för identifiering av miljöinställning som standard och tillägg av miljön via ”Add-AzEnvironment”</span><span class="sxs-lookup"><span data-stu-id="a850c-467">Supported discovering environment setting by default and adding environment via 'Add-AzEnvironment'</span></span>
* <span data-ttu-id="a850c-468">Uppdatera förinlästa sammansättningar [#12024], [#11976]</span><span class="sxs-lookup"><span data-stu-id="a850c-468">Update preloaded assemblies [#12024], [#11976]</span></span>
* <span data-ttu-id="a850c-469">Uppdaterad Azure.Core-sammansättning</span><span class="sxs-lookup"><span data-stu-id="a850c-469">Updated Azure.Core assembly</span></span>
* <span data-ttu-id="a850c-470">Ett problem har åtgärdats som kan orsaka att ”Connect-AzAccount” misslyckas vid körning av flera trådar [#11201]</span><span class="sxs-lookup"><span data-stu-id="a850c-470">Fixed an issue that may cause 'Connect-AzAccount' to fail in multi-threaded execution [#11201]</span></span>

#### <a name="azaks"></a><span data-ttu-id="a850c-471">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="a850c-471">Az.Aks</span></span>
* <span data-ttu-id="a850c-472">Användning av gamla [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) ersattes med anrop till API:erna [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) och [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials)</span><span class="sxs-lookup"><span data-stu-id="a850c-472">Replaced usage of old [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) with calls to [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) and [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials) APIs</span></span>

#### <a name="azbatch"></a><span data-ttu-id="a850c-473">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="a850c-473">Az.Batch</span></span>
* <span data-ttu-id="a850c-474">Az.Batch har uppdaterats att använda ”Microsoft.Azure.Management.Batch” SDK till och med version 11.0.0.</span><span class="sxs-lookup"><span data-stu-id="a850c-474">Updated Az.Batch to use 'Microsoft.Azure.Management.Batch' SDK version to 11.0.0</span></span>
* <span data-ttu-id="a850c-475">Möjligheten att ange BatchAccount-identiteten har lagts till i cmdleten ”New-AzBatchAccount”</span><span class="sxs-lookup"><span data-stu-id="a850c-475">Added the ability to set the BatchAccount Identity in the 'New-AzBatchAccount' cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="a850c-476">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a850c-476">Az.CognitiveServices</span></span>
* <span data-ttu-id="a850c-477">Stöd för att visa kontofunktioner.</span><span class="sxs-lookup"><span data-stu-id="a850c-477">Supported displaying account capabilities.</span></span>
* <span data-ttu-id="a850c-478">Stöd för att ändra PublicNetworkAccess.</span><span class="sxs-lookup"><span data-stu-id="a850c-478">Supported modifying PublicNetworkAccess.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a850c-479">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a850c-479">Az.Compute</span></span>
* <span data-ttu-id="a850c-480">Parametern SimulateEviction har lagts till i cmdletarna set-AzVM och set-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="a850c-480">Added SimulateEviction parameter to Set-AzVM and Set-AzVmssVM cmdlets.</span></span>
* <span data-ttu-id="a850c-481">”Premium_LRS” har lagts till i argumentslutföraren för parametern StorageAccountType för cmdleten New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="a850c-481">Added 'Premium_LRS' to the argument completer of StorageAccountType parameter for New-AzGalleryImageVersion cmdlet.</span></span>
* <span data-ttu-id="a850c-482">Understatusar har lagts till i VMCustomScriptExtension [#11297]</span><span class="sxs-lookup"><span data-stu-id="a850c-482">Added Substatuses to VMCustomScriptExtension [#11297]</span></span>
* <span data-ttu-id="a850c-483">”Delete” har lagts till i argumentslutföraren för parametern EvictionPolicy för cmdletarna New-AzVM och New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="a850c-483">Added 'Delete' to the argument completer of EvictionPolicy parameter for New-AzVM and New-AzVMConfig cmdlets.</span></span>
* <span data-ttu-id="a850c-484">Åtgärdat namn för nytt VM-tillägg för SAP</span><span class="sxs-lookup"><span data-stu-id="a850c-484">Fixed name of new VM Extension for SAP</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a850c-485">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a850c-485">Az.DataFactory</span></span>
* <span data-ttu-id="a850c-486">ADF .Net SDK har uppdaterats till 4.9.0</span><span class="sxs-lookup"><span data-stu-id="a850c-486">Updated ADF .Net SDK version to 4.9.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="a850c-487">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a850c-487">Az.EventHub</span></span>
* <span data-ttu-id="a850c-488">Parametrar för hanterad identitet har lagts till i cmdletarna ”New-AzEventHubNamespace” och ”set-AzEventHubNamespace”</span><span class="sxs-lookup"><span data-stu-id="a850c-488">Added Managed Identity parameters to 'New-AzEventHubNamespace' and 'Set-AzEventHubNamespace' cmdlets</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="a850c-489">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="a850c-489">Az.Functions</span></span>
* <span data-ttu-id="a850c-490">Stöd har lagts till för att skapa PowerShell 7.0- och Java 11-funktionsappar</span><span class="sxs-lookup"><span data-stu-id="a850c-490">Added support to create PowerShell 7.0 and Java 11 function apps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="a850c-491">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a850c-491">Az.HDInsight</span></span>
* <span data-ttu-id="a850c-492">Stöd för listning av värdar och omstart för specifika värdar i HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="a850c-492">Supported listing hosts and restart specific hosts of the HDInsight cluster.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="a850c-493">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="a850c-493">Az.HealthcareApis</span></span>
* <span data-ttu-id="a850c-494">Uppdaterade SDK-versionen till 1.1.0</span><span class="sxs-lookup"><span data-stu-id="a850c-494">Updated the SDK version to 1.1.0</span></span>
* <span data-ttu-id="a850c-495">Stöd har lagts till för exportinställningar och hanterad identitet</span><span class="sxs-lookup"><span data-stu-id="a850c-495">Added support for Export settings and Managed Identity</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a850c-496">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a850c-496">Az.Monitor</span></span>
* <span data-ttu-id="a850c-497">Parameter för inmatningsobjekt har åtgärdats för ”Set-AzActivityLogAlert”</span><span class="sxs-lookup"><span data-stu-id="a850c-497">Fixed input object parameter for 'Set-AzActivityLogAlert'</span></span>
* <span data-ttu-id="a850c-498">Parametern ”InputObject” har åtgärdats för ”Set-AzActionGroup” [#10868]</span><span class="sxs-lookup"><span data-stu-id="a850c-498">Fixed 'InputObject' parameter for 'Set-AzActionGroup' [#10868]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a850c-499">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a850c-499">Az.Network</span></span>
* <span data-ttu-id="a850c-500">Stöd har lagts till för parametern AddressPrefixType i ”Remove-AzExpressRouteCircuitConnectionConfig”</span><span class="sxs-lookup"><span data-stu-id="a850c-500">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="a850c-501">Nya cmdletar har lagts till för Azure FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="a850c-501">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="a850c-502">”New-AzFirewallPolicyDnsSetting”</span><span class="sxs-lookup"><span data-stu-id="a850c-502">'New-AzFirewallPolicyDnsSetting'</span></span>
    - <span data-ttu-id="a850c-503">Stöd för mål-FQDN i nätverksregler för brandväggsprincip</span><span class="sxs-lookup"><span data-stu-id="a850c-503">Support for Destination FQDN in Network Rules for Firewall Policy</span></span>
* <span data-ttu-id="a850c-504">Stöd har lagts till för åtgärder i serverdelsadresspooler</span><span class="sxs-lookup"><span data-stu-id="a850c-504">Added support for backend address pool operations</span></span>
    - <span data-ttu-id="a850c-505">”New-AzLoadBalancerBackendAddressConfig”</span><span class="sxs-lookup"><span data-stu-id="a850c-505">'New-AzLoadBalancerBackendAddressConfig'</span></span>
    - <span data-ttu-id="a850c-506">”New-AzLoadBalancerBackendAddressPool”</span><span class="sxs-lookup"><span data-stu-id="a850c-506">'New-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="a850c-507">”Set-AzLoadBalancerBackendAddressPool”</span><span class="sxs-lookup"><span data-stu-id="a850c-507">'Set-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="a850c-508">”Remove-AzLoadBalancerBackendAddressPool”</span><span class="sxs-lookup"><span data-stu-id="a850c-508">'Remove-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="a850c-509">”Get-AzLoadBalancerBackendAddressPool”</span><span class="sxs-lookup"><span data-stu-id="a850c-509">'Get-AzLoadBalancerBackendAddressPool'</span></span>
* <span data-ttu-id="a850c-510">Namnvalidering har lagts till för ”New-AzIpGroup”</span><span class="sxs-lookup"><span data-stu-id="a850c-510">Added name validation for 'New-AzIpGroup'</span></span>
* <span data-ttu-id="a850c-511">Nya cmdletar har lagts till för Azure FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="a850c-511">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="a850c-512">”New-AzFirewallPolicyThreatIntelWhitelist”</span><span class="sxs-lookup"><span data-stu-id="a850c-512">'New-AzFirewallPolicyThreatIntelWhitelist'</span></span>
* <span data-ttu-id="a850c-513">Nedanstående kommandon för funktionen har uppdaterats: Konfiguration/borttagning av anpassade DNS-servrar på VirtualWan P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="a850c-513">Updated below commands for feature: Custom dns servers set/remove on VirtualWan P2SVpnGateway.</span></span>
    - <span data-ttu-id="a850c-514">New-AzP2sVpnGateway har uppdaterats: Den valfria parametern ”-CustomDnsServer” har lagts till för att kunder ska kunna ange att deras DNS-servrar ska konfigureras på P2SVpnGateway, som kan användas av punkt-till-plats-klienter.</span><span class="sxs-lookup"><span data-stu-id="a850c-514">Updated New-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
    - <span data-ttu-id="a850c-515">Update-AzP2sVpnGateway har uppdaterats: Den valfria parametern ”-CustomDnsServer” har lagts till för att kunder ska kunna ange att deras DNS-servrar ska konfigureras på P2SVpnGateway, som kan användas av punkt-till-plats-klienter.</span><span class="sxs-lookup"><span data-stu-id="a850c-515">Updated Update-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
* <span data-ttu-id="a850c-516">”Update-AzVpnGateway” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="a850c-516">Updated 'Update-AzVpnGateway'</span></span>
    - <span data-ttu-id="a850c-517">Den valfria parametern ”-BgpPeeringAddress” har lagts till för att kunder ska kunna ange sina anpassade BGP:er som ska konfigurerar på VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="a850c-517">Added optional parameter '-BgpPeeringAddress' for customers to specify their custom bgps to set on VpnGateway.</span></span>
* <span data-ttu-id="a850c-518">Ny cmdlet har lagts till för att stödja återställning av en VirtualHub-resurs routningsstatus:</span><span class="sxs-lookup"><span data-stu-id="a850c-518">Added new cmdlet to support resetting the routing state of a VirtualHub resource:</span></span>
    - <span data-ttu-id="a850c-519">”Reset-AzHubRouter”</span><span class="sxs-lookup"><span data-stu-id="a850c-519">'Reset-AzHubRouter'</span></span>
* <span data-ttu-id="a850c-520">Nedanstående saker har uppdaterats baserat på den senaste Swagger-ändringen för brandväggspolicyn</span><span class="sxs-lookup"><span data-stu-id="a850c-520">Updated below things based on recent swagger change for Firewall Policy</span></span>
    - <span data-ttu-id="a850c-521">Namn ändras för RuleGroup, RuleCollectionGroup och RuleType</span><span class="sxs-lookup"><span data-stu-id="a850c-521">Changes names for RuleGroup, RuleCollectionGroup and RuleType</span></span>
    - <span data-ttu-id="a850c-522">Stöd har lagts till för NAT-regelsamlingar för brandväggsprincip så att flera NAT-regelsamlingar stöds</span><span class="sxs-lookup"><span data-stu-id="a850c-522">Added support for Firewall Policy NAT Rule Collections to support multiple NAT Rule Collection</span></span>
* <span data-ttu-id="a850c-523">[Icke-bakåtkompatibel ändring] Den obligatoriska parametern ”SourceIpGroup” har lagts till för ”New-AzFirewallPolicyApplicationRule” och ”New-AzFirewallPolicyNetworkRule”.</span><span class="sxs-lookup"><span data-stu-id="a850c-523">[Breaking Change] Added mandatory parameter 'SourceIpGroup' for 'New-AzFirewallPolicyApplicationRule' and 'New-AzFirewallPolicyNetworkRule'.</span></span>
* <span data-ttu-id="a850c-524">[Icke-bakåtkompatibel ändring] ”New-AzFirewallPolicyApplicationRule” har åtgärdats, parametern ”SourceAddress” är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="a850c-524">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="a850c-525">[Icke-bakåtkompatibel ändring] ”New-AzFirewallPolicyApplicationRule” har åtgärdats, parametern ”SourceAddress” är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="a850c-525">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="a850c-526">[Icke-bakåtkompatibel ändring] Obligatoriska parametrar har tagits bort: ”TranslatedAddress”, ”TranslatedPort” för ”New-AzFirewallPolicyNatRuleCollection”.</span><span class="sxs-lookup"><span data-stu-id="a850c-526">[Breaking Change] Removed mandatory parameters: 'TranslatedAddress', 'TranslatedPort' for 'New-AzFirewallPolicyNatRuleCollection'.</span></span>
* <span data-ttu-id="a850c-527">Nya cmdletar har lagts till för att stödja PrivateLink på Application Gateway</span><span class="sxs-lookup"><span data-stu-id="a850c-527">Added new cmdlets to support PrivateLink On Application Gateway</span></span>
    - <span data-ttu-id="a850c-528">”New-AzApplicationGatewayPrivateLinkConfiguration”</span><span class="sxs-lookup"><span data-stu-id="a850c-528">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="a850c-529">”Get-AzApplicationGatewayPrivateLinkConfiguration”</span><span class="sxs-lookup"><span data-stu-id="a850c-529">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="a850c-530">”New-AzApplicationGatewayPrivateLinkConfiguration”</span><span class="sxs-lookup"><span data-stu-id="a850c-530">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="a850c-531">”Set-AzApplicationGatewayPrivateLinkConfiguration”</span><span class="sxs-lookup"><span data-stu-id="a850c-531">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="a850c-532">”Remove-AzApplicationGatewayPrivateLinkConfiguration”</span><span class="sxs-lookup"><span data-stu-id="a850c-532">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="a850c-533">”New-AzApplicationGatewayPrivateLinkIpConfiguration”</span><span class="sxs-lookup"><span data-stu-id="a850c-533">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span></span>
* <span data-ttu-id="a850c-534">Nya cmdletar har lagts till för VirtualHubs underordnade resurs HubRouteTables.</span><span class="sxs-lookup"><span data-stu-id="a850c-534">Added new cmdlets for HubRouteTables child resource of VirtualHub.</span></span>
    - <span data-ttu-id="a850c-535">”New-AzVHubRoute”</span><span class="sxs-lookup"><span data-stu-id="a850c-535">'New-AzVHubRoute'</span></span>
    - <span data-ttu-id="a850c-536">”New-AzVHubRouteTable”</span><span class="sxs-lookup"><span data-stu-id="a850c-536">'New-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="a850c-537">”Get-AzVHubRouteTable”</span><span class="sxs-lookup"><span data-stu-id="a850c-537">'Get-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="a850c-538">”Update-AzVHubRouteTable”</span><span class="sxs-lookup"><span data-stu-id="a850c-538">'Update-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="a850c-539">”Remove-AzVHubRouteTable”</span><span class="sxs-lookup"><span data-stu-id="a850c-539">'Remove-AzVHubRouteTable'</span></span>
* <span data-ttu-id="a850c-540">Befintliga cmdletar har uppdaterats för att stödja valfri RoutingConfiguration-indataparameter för anpassad routning i VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="a850c-540">Updated existing cmdlets to support optional RoutingConfiguration input parameter for custom routing in VirtualWan.</span></span>
    - <span data-ttu-id="a850c-541">”New-AzExpressRouteConnection”</span><span class="sxs-lookup"><span data-stu-id="a850c-541">'New-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="a850c-542">”Set-AzExpressRouteConnection”</span><span class="sxs-lookup"><span data-stu-id="a850c-542">'Set-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="a850c-543">”New-AzVirtualHubVnetConnection”</span><span class="sxs-lookup"><span data-stu-id="a850c-543">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="a850c-544">”Update-AzVirtualHubVnetConnection”</span><span class="sxs-lookup"><span data-stu-id="a850c-544">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="a850c-545">”New-AzVpnConnection”</span><span class="sxs-lookup"><span data-stu-id="a850c-545">'New-AzVpnConnection'</span></span>
    - <span data-ttu-id="a850c-546">”Update-AzVpnConnection”</span><span class="sxs-lookup"><span data-stu-id="a850c-546">'Update-AzVpnConnection'</span></span>
    - <span data-ttu-id="a850c-547">”New-AzP2sVpnGateway”</span><span class="sxs-lookup"><span data-stu-id="a850c-547">'New-AzP2sVpnGateway'</span></span>
    - <span data-ttu-id="a850c-548">”Update-AzP2sVpnGateway”</span><span class="sxs-lookup"><span data-stu-id="a850c-548">'Update-AzP2sVpnGateway'</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="a850c-549">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a850c-549">Az.OperationalInsights</span></span>
* <span data-ttu-id="a850c-550">Fast fel PSWorkspace implementerar inte IOperationalInsightsWorkspace [#12135]</span><span class="sxs-lookup"><span data-stu-id="a850c-550">Fixed bug PSWorkspace doesn't implement IOperationalInsightsWorkspace [#12135]</span></span>
* <span data-ttu-id="a850c-551">”pergb2018” har lagts till i uppsättningen med giltiga värden för parametern ”Sku” i ”Set-AzOperationalInsightsWorkspace”</span><span class="sxs-lookup"><span data-stu-id="a850c-551">Added 'pergb2018' to valid value set of parameter 'Sku' in 'Set-AzOperationalInsightsWorkspace'</span></span> 
* <span data-ttu-id="a850c-552">Alias ”FunctionParameters” lades till för parametern ”FunctionParameter” till</span><span class="sxs-lookup"><span data-stu-id="a850c-552">Added alias 'FunctionParameters' for parameter 'FunctionParameter' to</span></span>
    - <span data-ttu-id="a850c-553">”New-AzOperationalInsightsSavedSearch”</span><span class="sxs-lookup"><span data-stu-id="a850c-553">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="a850c-554">”Set-AzOperationalInsightsSavedSearch”</span><span class="sxs-lookup"><span data-stu-id="a850c-554">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a850c-555">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a850c-555">Az.RecoveryServices</span></span>
* <span data-ttu-id="a850c-556">Azure Backup har fått stöd för att hämta MAB-objekt.</span><span class="sxs-lookup"><span data-stu-id="a850c-556">Azure Backup added support for fetching MAB items.</span></span>
* <span data-ttu-id="a850c-557">Azure Site Recovery stöder disktypen ”StandardSSD_LRS”</span><span class="sxs-lookup"><span data-stu-id="a850c-557">Azure Site Recovery supports disk type 'StandardSSD_LRS'</span></span>

#### <a name="azresources"></a><span data-ttu-id="a850c-558">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a850c-558">Az.Resources</span></span>
* <span data-ttu-id="a850c-559">”UsageLocation”, ”GivenName”, ”Surname”, ”AccountEnabled”, ”MailNickname”, ”Mail” på ”PSADUser” lades till [#10526] [#10497]</span><span class="sxs-lookup"><span data-stu-id="a850c-559">Added 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' on 'PSADUser' [#10526] [#10497]</span></span>
* <span data-ttu-id="a850c-560">Problem med att ”-Mail” inte fungerar på ”Get-AzADUser” har åtgärdats [#11981]</span><span class="sxs-lookup"><span data-stu-id="a850c-560">Fixed issue that '-Mail' doesn't work on 'Get-AzADUser' [#11981]</span></span>
* <span data-ttu-id="a850c-561">Parametern ”-ExcludeChangeType” har lagts till i ”Get-AzDeploymentWhatIfResult” och ”Get-AzResourceGroupDeploymentWhatIfResult”</span><span class="sxs-lookup"><span data-stu-id="a850c-561">Added '-ExcludeChangeType' parameter to 'Get-AzDeploymentWhatIfResult' and 'Get-AzResourceGroupDeploymentWhatIfResult'</span></span>
* <span data-ttu-id="a850c-562">Parametern ”-WhatIfExcludeChangeType” har lagts till i ”New-AzDeployment” och ”New-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="a850c-562">Added '-WhatIfExcludeChangeType' parameter to 'New-AzDeployment' and 'New-AzResourceGroupDeployment'</span></span>
* <span data-ttu-id="a850c-563">Cmdletar för ”Test-Az\*Deployment” har uppdaterats för att visa bättre felmeddelanden</span><span class="sxs-lookup"><span data-stu-id="a850c-563">Updated 'Test-Az\*Deployment' cmdlets to show better error messages</span></span>
* <span data-ttu-id="a850c-564">Hjälpmeddelandet för parametern ”-Name” i distributionsskapande och What If-cmdletar</span><span class="sxs-lookup"><span data-stu-id="a850c-564">Fixed help message for '-Name' parameter of deployment create and What-If cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="a850c-565">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a850c-565">Az.Sql</span></span>
* <span data-ttu-id="a850c-566">Stöd för tjänsthuvudnamn har lagts till för administratörs-cmdlet för SQL Server Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="a850c-566">Added support for service principal for Set SQL Server Azure Active Directory Admin cmdlet</span></span>
* <span data-ttu-id="a850c-567">Synkroniseringsproblem i Data Classification-cmdletar har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="a850c-567">Fixed sync issue in Data Classification cmdlets.</span></span>
* <span data-ttu-id="a850c-568">Stöd för att söka efter användare via e-postadress på ”Set-AzSqlServerActiveDirectoryAdministrator” [#12192]</span><span class="sxs-lookup"><span data-stu-id="a850c-568">Supported searching user by mail on 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a850c-569">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a850c-569">Az.Storage</span></span>
* <span data-ttu-id="a850c-570">Skapa lagringskonto med RequireInfrastructureEncryption stöds</span><span class="sxs-lookup"><span data-stu-id="a850c-570">Supported create Storage account with RequireInfrastructureEncryption</span></span>
    -  <span data-ttu-id="a850c-571">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="a850c-571">'New-AzStorageAccount'</span></span>
* <span data-ttu-id="a850c-572">Logiken för inläsning av Azure.Core flyttades till Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a850c-572">Moved the logic of loading Azure.Core to Az.Accounts</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a850c-573">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a850c-573">Az.Websites</span></span>
* <span data-ttu-id="a850c-574">Skydd för att ta bort skapad webapp om återställningen misslyckades har lagts till i ”Restore-AzDeletedWebApp”</span><span class="sxs-lookup"><span data-stu-id="a850c-574">Added safeguard to delete created webapp if restore failed in 'Restore-AzDeletedWebApp'</span></span>
* <span data-ttu-id="a850c-575">”SourceWebApp.Location” har lagts till för ”New-AzWebApp” och ”New-AzWebAppSlot”</span><span class="sxs-lookup"><span data-stu-id="a850c-575">Added 'SourceWebApp.Location' for 'New-AzWebApp' and 'New-AzWebAppSlot'</span></span>
* <span data-ttu-id="a850c-576">Fel som förhindrade ändring av containerinställningar i ”Set-AzWebApp” och ”Set-AzWebAppSlot” har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="a850c-576">Fixed bug that prevented changing Container settings in 'Set-AzWebApp' and 'Set-AzWebAppSlot'</span></span>
* <span data-ttu-id="a850c-577">Ett fel för att hämta SiteConfig när -Name inte anges för Get-AzWebApp har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="a850c-577">Fixed bug to get SiteConfig when -Name is not given for Get-AzWebApp</span></span>
* <span data-ttu-id="a850c-578">Stöd har lagts till för att skapa ASP för Linux-appar</span><span class="sxs-lookup"><span data-stu-id="a850c-578">Added a support to create ASP for Linux Apps</span></span>
* <span data-ttu-id="a850c-579">Undantag har lagts till för kloning över resursgrupper</span><span class="sxs-lookup"><span data-stu-id="a850c-579">Added exceptions for clone across resource groups</span></span>

## <a name="420---june-2020"></a><span data-ttu-id="a850c-580">4.2.0 – juni 2020</span><span class="sxs-lookup"><span data-stu-id="a850c-580">4.2.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a850c-581">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a850c-581">Az.Accounts</span></span>
* <span data-ttu-id="a850c-582">Åtgärdade ett problem som kan få Az att hoppa över loggar i Azure Automation- eller PowerShell-jobb [#11492]</span><span class="sxs-lookup"><span data-stu-id="a850c-582">Fixed an issue that may cause Az to skip logs in Azure Automation or PowerShell jobs [#11492]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="a850c-583">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a850c-583">Az.AnalysisServices</span></span>
* <span data-ttu-id="a850c-584">Uppdaterad sammansättningsversion för dataplan-cmdletar</span><span class="sxs-lookup"><span data-stu-id="a850c-584">Updated assembly version of data plane cmdlets</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="a850c-585">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a850c-585">Az.ApiManagement</span></span>
* <span data-ttu-id="a850c-586">Uppdaterad sammansättningsversion för cmdletar för tjänsthantering</span><span class="sxs-lookup"><span data-stu-id="a850c-586">Updated assembly version of service management cmdlets</span></span>

#### <a name="azbilling"></a><span data-ttu-id="a850c-587">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="a850c-587">Az.Billing</span></span>
* <span data-ttu-id="a850c-588">Uppdaterad sammansättningsversion för förbrukningscmdletar</span><span class="sxs-lookup"><span data-stu-id="a850c-588">Updated assembly version of consumption cmdlets</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="a850c-589">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a850c-589">Az.CognitiveServices</span></span>
* <span data-ttu-id="a850c-590">Stöd för PrivateEndpoint- och PublicNetworkAccess-kontroll.</span><span class="sxs-lookup"><span data-stu-id="a850c-590">Support PrivateEndpoint and PublicNetworkAccess control.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="a850c-591">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a850c-591">Az.DataFactory</span></span>
* <span data-ttu-id="a850c-592">Uppdaterad sammansättningsversion för datafabrik V2-cmdletar</span><span class="sxs-lookup"><span data-stu-id="a850c-592">Updated assembly version of data factory V2 cmdlets</span></span>

#### <a name="azdatashare"></a><span data-ttu-id="a850c-593">Az.DataShare</span><span class="sxs-lookup"><span data-stu-id="a850c-593">Az.DataShare</span></span>
* <span data-ttu-id="a850c-594">Allmän tillgänglighet för modulen ”Az.DataShare”</span><span class="sxs-lookup"><span data-stu-id="a850c-594">General availability of ''Az.DataShare'' module</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="a850c-595">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="a850c-595">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="a850c-596">Allmän tillgänglighet för modulen ”Az.DesktopVirtualization”</span><span class="sxs-lookup"><span data-stu-id="a850c-596">General availability of ''Az.DesktopVirtualization'' module</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="a850c-597">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a850c-597">Az.OperationalInsights</span></span>
* <span data-ttu-id="a850c-598">Uppgraderad SDK till 0.21.0</span><span class="sxs-lookup"><span data-stu-id="a850c-598">Upgraded SDK to 0.21.0</span></span>
* <span data-ttu-id="a850c-599">Lade till valfria parametrar till</span><span class="sxs-lookup"><span data-stu-id="a850c-599">Added optional parameters to</span></span> 
    - <span data-ttu-id="a850c-600">”New-AzOperationalInsightsSavedSearch”</span><span class="sxs-lookup"><span data-stu-id="a850c-600">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="a850c-601">”Set-AzOperationalInsightsSavedSearch”</span><span class="sxs-lookup"><span data-stu-id="a850c-601">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="a850c-602">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a850c-602">Az.PolicyInsights</span></span>
* <span data-ttu-id="a850c-603">Korrigerade exempel 3 för ”Start-AzPolicyComplianceScan”</span><span class="sxs-lookup"><span data-stu-id="a850c-603">Corrected example 3 for 'Start-AzPolicyComplianceScan'</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="a850c-604">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="a850c-604">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="a850c-605">Uppdaterad sammansättningsversion för PowerBI-cmdletar</span><span class="sxs-lookup"><span data-stu-id="a850c-605">Updated assembly version of PowerBI cmdlets</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="a850c-606">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="a850c-606">Az.PrivateDns</span></span>
* <span data-ttu-id="a850c-607">Korrigerade formatering av utförlig utdatasträng för Remove-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="a850c-607">Corrected verbose output string formatting for Remove-AzPrivateDnsRecordSet</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a850c-608">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a850c-608">Az.RecoveryServices</span></span>
* <span data-ttu-id="a850c-609">Azure Site Recovery-stöd för att skapa en återställningsplan för replikering mellan zoner från xml-indata.</span><span class="sxs-lookup"><span data-stu-id="a850c-609">Azure Site Recovery support for creating recovery plan for zone to zone replication from xml input.</span></span>
* <span data-ttu-id="a850c-610">Uppdaterad sammansättningsversion för cmdletar för SiteRecovery och Backup</span><span class="sxs-lookup"><span data-stu-id="a850c-610">Updated assembly version of SiteRecovery and Backup cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="a850c-611">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a850c-611">Az.Resources</span></span>
* <span data-ttu-id="a850c-612">Lade till slutparameter för cmdletarna Get-AzDeploymentScriptLog och Save-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="a850c-612">Added Tail parameter to Get-AzDeploymentScriptLog and Save-AzDeploymentScriptLog cmdlets</span></span>
* <span data-ttu-id="a850c-613">Formaterad utdataegenskap så att den kan visas i cmdlet-utdata för Get-AzDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="a850c-613">Formatted Output property and show it on the Get-AzDeploymentScript cmdlet output</span></span>
* <span data-ttu-id="a850c-614">Bytte namn på parametern -DeploymentScriptInputObject till -DeploymentScriptObject</span><span class="sxs-lookup"><span data-stu-id="a850c-614">Renamed -DeploymentScriptInputObject parameter to -DeploymentScriptObject</span></span>
* <span data-ttu-id="a850c-615">Åtgärdade saknade fil/målnamn i cmdlet-meddelanden.</span><span class="sxs-lookup"><span data-stu-id="a850c-615">Fixed missing file/target name in cmdlet messages.</span></span>
* <span data-ttu-id="a850c-616">Uppdaterad sammansättningsversion för cmdletar för resurshanterare och taggar</span><span class="sxs-lookup"><span data-stu-id="a850c-616">Updated assembly version of resource manager and tags cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="a850c-617">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a850c-617">Az.Sql</span></span>
* <span data-ttu-id="a850c-618">Lade till UsePrivateLinkConnection till ”New-AzSqlSyncGroup”, ”Update-AzSqlSyncGroup”, ”New-AzSqlSyncMember” och ”Update-AzSqlSyncMember”</span><span class="sxs-lookup"><span data-stu-id="a850c-618">Added UsePrivateLinkConnection to 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="a850c-619">Lade till SyncMemberAzureDatabaseResourceId till ”New-AzSqlSyncMember” and ”Update-AzSqlSyncMember”</span><span class="sxs-lookup"><span data-stu-id="a850c-619">Added SyncMemberAzureDatabaseResourceId to 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="a850c-620">Lade till stöd för att söka efter gästanvändare för att ange administratörs-cmdlet för SQL Server Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="a850c-620">Added Guest user lookup support to Set SQL Server Azure Active Directory Admin cmdlet</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a850c-621">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a850c-621">Az.Storage</span></span>
* <span data-ttu-id="a850c-622">Uppdaterad sammansättningsversion för dataplan-cmdletar</span><span class="sxs-lookup"><span data-stu-id="a850c-622">Updated assembly version of data plane cmdlets</span></span>

## <a name="410---may-2020"></a><span data-ttu-id="a850c-623">4.1.0 – maj 2020</span><span class="sxs-lookup"><span data-stu-id="a850c-623">4.1.0 - May 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="a850c-624">Höjdpunkter sedan den senaste uppdateringen</span><span class="sxs-lookup"><span data-stu-id="a850c-624">Highlights since the last release</span></span>
* <span data-ttu-id="a850c-625">PowerShell-versioner som stöds: Windows PowerShell 5.1, PowerShell Core 6.2.4+ och PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="a850c-625">Supported PowerShell versions: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>
* <span data-ttu-id="a850c-626">Allmän tillgänglighet för Az.Functions</span><span class="sxs-lookup"><span data-stu-id="a850c-626">General availability of Az.Functions</span></span> 
* <span data-ttu-id="a850c-627">Nya stora uppdateringar har gjorts för Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources och Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a850c-627">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources, and Az.Storage have major release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="a850c-628">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a850c-628">Az.Accounts</span></span>
* <span data-ttu-id="a850c-629">”Add-AzEnvironment” och ”Set-AzEnvironment” har uppdaterats med stöd för parametrarna ”AzureSynapseAnalyticsEndpointResourceId” och ”AzureSynapseAnalyticsEndpointSuffix”</span><span class="sxs-lookup"><span data-stu-id="a850c-629">Updated 'Add-AzEnvironment' and 'Set-AzEnvironment' to accept parameters 'AzureSynapseAnalyticsEndpointResourceId' and 'AzureSynapseAnalyticsEndpointSuffix'</span></span>
* <span data-ttu-id="a850c-630">Azure.Core-relaterade sammansättningar har lagts till i Az.Accounts; PowerShell-plattformar som stöds är Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span><span class="sxs-lookup"><span data-stu-id="a850c-630">Added Azure.Core related assemblies into Az.Accounts, supported PowerShell platforms include Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span></span>

#### <a name="azaks"></a><span data-ttu-id="a850c-631">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="a850c-631">Az.Aks</span></span>
* <span data-ttu-id="a850c-632">API-versionen har uppgraderats till 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="a850c-632">Upgraded API Version to 2019-10-01</span></span>
* <span data-ttu-id="a850c-633">Stöds för att skapa AKS med hjälp av Windows-container</span><span class="sxs-lookup"><span data-stu-id="a850c-633">Supported to create AKS using Windows container</span></span>
* <span data-ttu-id="a850c-634">Nya cmdletar är tillgängliga: ”New-AzAksNodePool”, ”Update-AzAksNodePool”, ”Remove-AzAksNodePool”,        ”Get-AzAksNodePool”, ”Install-AzAksKubectl”, ”Get-AzAksVersion”</span><span class="sxs-lookup"><span data-stu-id="a850c-634">Provided new cmdlets: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="a850c-635">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a850c-635">Az.ApiManagement</span></span>
* <span data-ttu-id="a850c-636">Parametrarna ”New-AzApiManagement” och ”Set-AzApiManagement”: [-AssignIdentity] har bytt namn till [-SystemAssignedIdentity]</span><span class="sxs-lookup"><span data-stu-id="a850c-636">'New-AzApiManagement' and 'Set-AzApiManagement': [-AssignIdentity] parameter renamed as [-SystemAssignedIdentity]</span></span>
* <span data-ttu-id="a850c-637">”New-AzApiManagement” och ”Set-AzApiManagement”: En ny parameter har lagts till: [-UserAssignedIdentity <String[]>]</span><span class="sxs-lookup"><span data-stu-id="a850c-637">'New-AzApiManagement' and 'Set-AzApiManagement': New parameter added: [-UserAssignedIdentity <String[]>]</span></span>
* <span data-ttu-id="a850c-638">”Get-AzApiManagementProperty” har bytt namn till ”Get-AzApiManagementNamedValue”.</span><span class="sxs-lookup"><span data-stu-id="a850c-638">'Get-AzApiManagementProperty': renamed as 'Get-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="a850c-639">PropertyId-parametern har bytt namn till NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="a850c-639">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="a850c-640">”New-AzApiManagementProperty” har bytt namn till ”New-AzApiManagementNamedValue”.</span><span class="sxs-lookup"><span data-stu-id="a850c-640">'New-AzApiManagementProperty': renamed as 'New-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="a850c-641">PropertyId-parametern har bytt namn till NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="a850c-641">PropertyId parameter renamed as NamedValueId.</span></span> 
* <span data-ttu-id="a850c-642">”Set-AzApiManagementProperty” har bytt namn till ”Set-AzApiManagementNamedValue”.</span><span class="sxs-lookup"><span data-stu-id="a850c-642">'Set-AzApiManagementProperty': renamed as 'Set-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="a850c-643">PropertyId-parametern har bytt namn till NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="a850c-643">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="a850c-644">”Remove-AzApiManagementProperty” har bytt namn till ”Remove-AzApiManagementNamedValue”.</span><span class="sxs-lookup"><span data-stu-id="a850c-644">'Remove-AzApiManagementProperty': renamed as 'Remove-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="a850c-645">PropertyId-parametern har bytt namn till NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="a850c-645">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="a850c-646">Den nya cmdleten Get-AzApiManagementAuthorizationServerClientSecret gör att ”Get-AzApiManagementAuthorizationServer” inte längre returnerar klienthemligheter.</span><span class="sxs-lookup"><span data-stu-id="a850c-646">Added new 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet and 'Get-AzApiManagementAuthorizationServer' will not return client secret anymore.</span></span>
* <span data-ttu-id="a850c-647">Den nya cmdleten ”Get-AzApiManagementNamedValueSecretValue” gör att ”Get-AzApiManagementNamedValue” inte returnerar värdet för en hemlighet.</span><span class="sxs-lookup"><span data-stu-id="a850c-647">Added new 'Get-AzApiManagementNamedValueSecretValue' cmdlet and 'Get-AzApiManagementNamedValue' will not return secret value.</span></span>
* <span data-ttu-id="a850c-648">Den nya cmdleten ”Get-AzApiManagementOpenIdConnectProviderClientSecret” gör att ”Get-AzApiManagementOpenIdConnectProvider” inte längre returnerar klienthemligheter.</span><span class="sxs-lookup"><span data-stu-id="a850c-648">Added new 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet and 'Get-AzApiManagementOpenIdConnectProvider' will not return client secret anymore.</span></span>
* <span data-ttu-id="a850c-649">Den nya cmdleten ”Get-AzApiManagementSubscriptionKey” gör att ”Get-AzApiManagementSubscription” inte längre returnerar prenumerationsnycklar.</span><span class="sxs-lookup"><span data-stu-id="a850c-649">Added new 'Get-AzApiManagementSubscriptionKey' cmdlet and 'Get-AzApiManagementSubscription' will not return subscription keys anymore.</span></span>
* <span data-ttu-id="a850c-650">Den nya cmdleten ”Get-AzApiManagementTenantAccessSecret” gör att ”Get-AzApiManagementTenantAccess” inte längre returnerar nycklar.</span><span class="sxs-lookup"><span data-stu-id="a850c-650">Added new 'Get-AzApiManagementTenantAccessSecret' cmdlet and 'Get-AzApiManagementTenantAccess' will not return keys anymore.</span></span>
* <span data-ttu-id="a850c-651">Den nya cmdleten ”Get-AzApiManagementTenantGitAccessSecret” gör att ”Get-AzApiManagementTenantGitAccess” inte längre returnerar nycklar.</span><span class="sxs-lookup"><span data-stu-id="a850c-651">Added new 'Get-AzApiManagementTenantGitAccessSecret' cmdlet and 'Get-AzApiManagementTenantGitAccess' will not return keys anymore.</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="a850c-652">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="a850c-652">Az.ApplicationInsights</span></span>
* <span data-ttu-id="a850c-653">Tillagda parametrar: ”RetentionInDays” ”PublicNetworkAccessForIngestion” ”PublicNetworkAccessForQuery” för ”New-AzApplicationInsights”</span><span class="sxs-lookup"><span data-stu-id="a850c-653">Added Parameters: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span></span>
* <span data-ttu-id="a850c-654">Cmdleten ”Update-AzApplicationInsights” har skapats</span><span class="sxs-lookup"><span data-stu-id="a850c-654">Created cmdlet 'Update-AzApplicationInsights'</span></span>
* <span data-ttu-id="a850c-655">Cmdletar har skapats för länkat lagringskonto</span><span class="sxs-lookup"><span data-stu-id="a850c-655">Created cmdlets for Linked Storage Account</span></span>

#### <a name="azbatch"></a><span data-ttu-id="a850c-656">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="a850c-656">Az.Batch</span></span>
* <span data-ttu-id="a850c-657">Az.Batch har uppdaterats att använda ”Microsoft.Azure.Batch” SDK version 13.0.0 och ”Microsoft.Azure.Management.Batch” SDK version 9.0.0.</span><span class="sxs-lookup"><span data-stu-id="a850c-657">Updated Az.Batch to use 'Microsoft.Azure.Batch' SDK version 13.0.0 and 'Microsoft.Azure.Management.Batch' SDK version 9.0.0.</span></span>
* <span data-ttu-id="a850c-658">Nu kan du välja vilken typ av certifikat du lägger till genom att använda den nya parametern ”-CertificateKind” med ”New-AzBatchCertificate”.</span><span class="sxs-lookup"><span data-stu-id="a850c-658">Added the ability to select the kind of certificate being added using the new '-CertificateKind' parameter to 'New-AzBatchCertificate'.</span></span>
* <span data-ttu-id="a850c-659">Egenskapen ”ApplicationPackages” har tagits bort från ”PSApplication”, som tidigare alltid var ''.</span><span class="sxs-lookup"><span data-stu-id="a850c-659">Removed 'ApplicationPackages' property from 'PSApplication' which was previously always ''.</span></span>
  - <span data-ttu-id="a850c-660">Specifika paket i ett program kan nu hämtas med hjälp av ”Get-AzBatchApplicationPackage”.</span><span class="sxs-lookup"><span data-stu-id="a850c-660">The specific packages inside of an application now can be retrieved using 'Get-AzBatchApplicationPackage'.</span></span> <span data-ttu-id="a850c-661">Ett exempel: ”Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication”.</span><span class="sxs-lookup"><span data-stu-id="a850c-661">For example: 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span></span>
* <span data-ttu-id="a850c-662">Nu när du skapar en pool med hjälp av ”New-AzBatchPool” kan egenskapen ”VirtualMachineImageId” för ”PSImageReference” endast referera till en Shared Image Gallery-avbildning.</span><span class="sxs-lookup"><span data-stu-id="a850c-662">When creating a pool using 'New-AzBatchPool', the 'VirtualMachineImageId' property of 'PSImageReference' can now only refer to a Shared Image Gallery image.</span></span>
* <span data-ttu-id="a850c-663">När du skapar en pool med hjälp av ”New-AzBatchPool” kan poolen etableras utan en offentlig IP-adress med hjälp av den nya egenskapen ”PublicIPAddressConfiguration” för ”PSNetworkConfiguration”.</span><span class="sxs-lookup"><span data-stu-id="a850c-663">When creating a pool using 'New-AzBatchPool', the pool can be provisioned without a public IP using the new 'PublicIPAddressConfiguration' property of 'PSNetworkConfiguration'.</span></span>
  - <span data-ttu-id="a850c-664">Egenskapen ”PublicIPs” för ”PSNetworkConfiguration” har också flyttats till ”PSPublicIPAddressConfiguration”.</span><span class="sxs-lookup"><span data-stu-id="a850c-664">The 'PublicIPs' property of 'PSNetworkConfiguration' has moved in to 'PSPublicIPAddressConfiguration' as well.</span></span> <span data-ttu-id="a850c-665">Den här egenskapen kan bara anges om ”IPAddressProvisioningType” är ”UserManaged”.</span><span class="sxs-lookup"><span data-stu-id="a850c-665">This property can only be specified if 'IPAddressProvisioningType' is 'UserManaged'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a850c-666">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a850c-666">Az.Compute</span></span>
* <span data-ttu-id="a850c-667">Parametern HostId har lagts till för cmdleten ”Update-AzVM”t</span><span class="sxs-lookup"><span data-stu-id="a850c-667">Added HostId parameter to 'Update-AzVM' cmdlet</span></span>
* <span data-ttu-id="a850c-668">Hjälpdokumenten har uppdaterats för cmdletarna ”New-AzVMConfig”, ”New-AzVmssConfig”, ”Update-AzVmss”, ”Set-AzVMOperatingSystem” och ”Set-AzVmssOsProfile”.</span><span class="sxs-lookup"><span data-stu-id="a850c-668">Updated Help documents for 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' and 'Set-AzVmssOsProfile' cmdlets.</span></span>
* <span data-ttu-id="a850c-669">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="a850c-669">Breaking changes</span></span>
    - <span data-ttu-id="a850c-670">Parametern FilterExpression tas bort från cmdleten ”Get-AzVMImage”.</span><span class="sxs-lookup"><span data-stu-id="a850c-670">FilterExpression parameter is removed from 'Get-AzVMImage' cmdlet.</span></span>
    - <span data-ttu-id="a850c-671">Parametern AssignIdentity tas bort från cmdletarna ”New-AzVmssConfig”, ”New-AzVMConfig” och ”Update-AzVM”.</span><span class="sxs-lookup"><span data-stu-id="a850c-671">AssignIdentity parameter is removed from 'New-AzVmssConfig', 'New-AzVMConfig' and 'Update-AzVM' cmdlets.</span></span>
    - <span data-ttu-id="a850c-672">AutomaticRepairMaxInstanceRepairsPercent tas bort från cmdletarna ”New-AzVmssConfig” och ”Update-AzVmss”.</span><span class="sxs-lookup"><span data-stu-id="a850c-672">AutomaticRepairMaxInstanceRepairsPercent is removed from 'New-AzVmssConfig' and 'Update-AzVmss' cmdlets.</span></span>
    - <span data-ttu-id="a850c-673">Egenskaperna AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus och VirtualMachineScaleSetsColocationStatus tas bort från ProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="a850c-673">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus and VirtualMachineScaleSetsColocationStatus properties are removed from ProximityPlacementGroup.</span></span>
    - <span data-ttu-id="a850c-674">Egenskapen MaxInstanceRepairsPercent tas bort från AutomaticRepairsPolicy.</span><span class="sxs-lookup"><span data-stu-id="a850c-674">MaxInstanceRepairsPercent property is removed from AutomaticRepairsPolicy.</span></span>
    - <span data-ttu-id="a850c-675">Typerna AvailabilitySets, VirtualMachines och VirtualMachineScaleSets ändras från IList<SubResource> till IList<SubResourceWithColocationStatus>.</span><span class="sxs-lookup"><span data-stu-id="a850c-675">The types of AvailabilitySets, VirtualMachines and VirtualMachineScaleSets are changed from IList<SubResource> to IList<SubResourceWithColocationStatus>.</span></span>
* <span data-ttu-id="a850c-676">Beskrivningen för cmdleten ”Get-AzVM” har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="a850c-676">Description for 'Get-AzVM' cmdlet has been updated to better describe it.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="a850c-677">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a850c-677">Az.DataFactory</span></span>
* <span data-ttu-id="a850c-678">CRUD-stöd för egenskaper för dataflödeskörning  i hanterad IR.</span><span class="sxs-lookup"><span data-stu-id="a850c-678">Supported CRUD of data flow runtime properties in Managed IR.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="a850c-679">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="a850c-679">Az.FrontDoor</span></span>
* <span data-ttu-id="a850c-680">Nya cmdletar har lagts till för att skapa, uppdatera, hämta och ta bort (CRUD) Front Door-regelmotorobjekt</span><span class="sxs-lookup"><span data-stu-id="a850c-680">Added new cmdlets for creation, update, retreival, and deletion of Front Door Rules Engine object</span></span>
* <span data-ttu-id="a850c-681">Hjälp-cmdletar har lagts till för konstruktion av Front Door-regelmotorobjekt</span><span class="sxs-lookup"><span data-stu-id="a850c-681">Added helper cmdlets for construction of Front Door Rules Engine object</span></span>
* <span data-ttu-id="a850c-682">Regelmotorreferens har lagts till för Front Door-hanteringsregelobjekt.</span><span class="sxs-lookup"><span data-stu-id="a850c-682">Added Rules Engine reference to Front Door Routing Rule object.</span></span>
* <span data-ttu-id="a850c-683">Parametrar för Private Link har lagts till för Front Door-serverdelsobjekt</span><span class="sxs-lookup"><span data-stu-id="a850c-683">Added Private Link parameters to Front Door Backend object</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="a850c-684">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="a850c-684">Az.Functions</span></span>
* <span data-ttu-id="a850c-685">Allmän tillgänglighet för ”Az.Functions”-modulen</span><span class="sxs-lookup"><span data-stu-id="a850c-685">General availability of ''Az.Functions'' module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="a850c-686">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a850c-686">Az.HDInsight</span></span>
* <span data-ttu-id="a850c-687">Stöd för diskkryptering med kundhanterad nyckel.</span><span class="sxs-lookup"><span data-stu-id="a850c-687">Supported Customer-managed key disk encryption.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="a850c-688">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="a850c-688">Az.HealthcareApis</span></span>
* <span data-ttu-id="a850c-689">Åtkomstprinciper använder inte längre det aktiva huvudkontot som standard</span><span class="sxs-lookup"><span data-stu-id="a850c-689">Access policies are no longer defaulted to the current principal</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a850c-690">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a850c-690">Az.IotHub</span></span>
* <span data-ttu-id="a850c-691">En cmdlet har lagts till som anropar en fråga i en IoT-hubb för att hämta information med ett SQL-liknande språk.</span><span class="sxs-lookup"><span data-stu-id="a850c-691">Added cmdlet to invoke a query in an IoT hub to retrieve information using a SQL-like language.</span></span>
* <span data-ttu-id="a850c-692">Problemet som gjorde att ”Add-AzIotHubDevice” inte skapade en Edge-aktiverad enhet utan underordnade enheter har åtgärdats [#11597]</span><span class="sxs-lookup"><span data-stu-id="a850c-692">Fix issue that 'Add-AzIotHubDevice' fails to create Edge Enabled Device without child devices [#11597]</span></span>
* <span data-ttu-id="a850c-693">En cmdlet har lagts till för att generera SAS-token för en Iot-hubb, enhet eller modul.</span><span class="sxs-lookup"><span data-stu-id="a850c-693">Added cmdlet to generate SAS token for Iot Hub, device or module.</span></span>
* <span data-ttu-id="a850c-694">En cmdlet har lagts till för att anropa en måttfråga om konfiguration.</span><span class="sxs-lookup"><span data-stu-id="a850c-694">Added cmdlet to invoke configuration metrics query.</span></span>
* <span data-ttu-id="a850c-695">Hantera automatisk distribution av IoT Edge i stor skala.</span><span class="sxs-lookup"><span data-stu-id="a850c-695">Manage IoT Edge automatic deployment at scale.</span></span> <span data-ttu-id="a850c-696">Nya cmdlet:ar är:</span><span class="sxs-lookup"><span data-stu-id="a850c-696">New cmdlets are:</span></span>
    - <span data-ttu-id="a850c-697">”Add-AzIotHubDeployment”</span><span class="sxs-lookup"><span data-stu-id="a850c-697">'Add-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="a850c-698">”Get-AzIotHubDeployment”</span><span class="sxs-lookup"><span data-stu-id="a850c-698">'Get-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="a850c-699">”Remove-AzIotHubDeployment”</span><span class="sxs-lookup"><span data-stu-id="a850c-699">'Remove-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="a850c-700">”Set-AzIotHubDeployment”</span><span class="sxs-lookup"><span data-stu-id="a850c-700">'Set-AzIotHubDeployment'</span></span>
* <span data-ttu-id="a850c-701">En cmdlet har lagts till för att anropa en måttfråga om IoT Edge-distribution.</span><span class="sxs-lookup"><span data-stu-id="a850c-701">Added cmdlet to invoke an IoT Edge deployment metrics query.</span></span>
* <span data-ttu-id="a850c-702">En cmdlet har lagts till för att tillämpa konfigurationsinnehåll på den angivna gränsenheten.</span><span class="sxs-lookup"><span data-stu-id="a850c-702">Added cmdlet to apply the configuration content to the specified edge device.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a850c-703">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a850c-703">Az.KeyVault</span></span>
* <span data-ttu-id="a850c-704">Två alias har tagits bort: ”New-AzKeyVaultCertificateAdministratorDetails” och ”New-AzKeyVaultCertificateOrganizationDetails”</span><span class="sxs-lookup"><span data-stu-id="a850c-704">Removed two aliases: 'New-AzKeyVaultCertificateAdministratorDetails' and 'New-AzKeyVaultCertificateOrganizationDetails'</span></span>
* <span data-ttu-id="a850c-705">Nu är mjuk borttagning aktiverat som standard när ett nyckelvalv skapas</span><span class="sxs-lookup"><span data-stu-id="a850c-705">Enabled soft delete by default when creating a key vault</span></span>
* <span data-ttu-id="a850c-706">Nätverksregler kan ställas in för att styra åtkomsten från särskilda nätverksplatser när du skapar ett nyckelvalv</span><span class="sxs-lookup"><span data-stu-id="a850c-706">Network rules can be set to govern the accessibility from specific network locations when creating a key vault</span></span>
* <span data-ttu-id="a850c-707">Stöd för BYOK (Bring Your Own Key) har lagts till</span><span class="sxs-lookup"><span data-stu-id="a850c-707">Added support to bring your own key (BYOK)</span></span>
    - <span data-ttu-id="a850c-708">”Add-AzKeyVaultKey” stöder generering av en KeyExchange-nyckel</span><span class="sxs-lookup"><span data-stu-id="a850c-708">'Add-AzKeyVaultKey' supports generating a key exchange key</span></span>
    - <span data-ttu-id="a850c-709">”Get-AzKeyVaultKey” stöder nedladdning av en offentlig nyckel i PEM-format</span><span class="sxs-lookup"><span data-stu-id="a850c-709">'Get-AzKeyVaultKey' supports downloading a public key in PEM format</span></span>
* <span data-ttu-id="a850c-710">”KeyOps”-delen av hjälpdokumentet för ”Add-AzKeyVaultKey” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="a850c-710">Updated the 'KeyOps' part of the help document of 'Add-AzKeyVaultKey'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a850c-711">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a850c-711">Az.Monitor</span></span>
* <span data-ttu-id="a850c-712">Bugg för ”Set-AzDiagnosticSettings” har åtgärdats; kvarhållningsprincipen tillämpas inte på alla kategorier [#11589]</span><span class="sxs-lookup"><span data-stu-id="a850c-712">Fixed bug for 'Set-AzDiagnosticSettings', retention policy won't apply to all categories [#11589]</span></span>
* <span data-ttu-id="a850c-713">Stöd för WebTest-tillgänglighetskriterier för måttavisering V2</span><span class="sxs-lookup"><span data-stu-id="a850c-713">Supported WebTest availability criteria for metric alert V2</span></span>
    - <span data-ttu-id="a850c-714">”New-AzMetricAlertRuleV2Criteria”: ett alternativ för att skapa tillgänglighetskriterier för webbtest har lagts till</span><span class="sxs-lookup"><span data-stu-id="a850c-714">'New-AzMetricAlertRuleV2Criteria': an option to create webtest availability criteria was added</span></span>
    - <span data-ttu-id="a850c-715">”Add-AzMetricAlertRuleV2”: stöd för de nya tillgänglighetskriterierna för webbtest</span><span class="sxs-lookup"><span data-stu-id="a850c-715">'Add-AzMetricAlertRuleV2': supports the new webtest availability criteria</span></span>
* <span data-ttu-id="a850c-716">Redundant definition har tagits bort för RetentionPolicy i PSLogProfile [#7608]</span><span class="sxs-lookup"><span data-stu-id="a850c-716">Removed redundant definition for RetentionPolicy in PSLogProfile [#7608]</span></span>
* <span data-ttu-id="a850c-717">Redundanta egenskaper som definierats i PSEventData har tagits bort [#11353]</span><span class="sxs-lookup"><span data-stu-id="a850c-717">Removed redundant properties difined in PSEventData [#11353]</span></span>
* <span data-ttu-id="a850c-718">”Get-AzLog” har bytt namn till ”Get-AzActivityLog”</span><span class="sxs-lookup"><span data-stu-id="a850c-718">Renamed 'Get-AzLog' to 'Get-AzActivityLog'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a850c-719">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a850c-719">Az.Network</span></span>
* <span data-ttu-id="a850c-720">Attribut för icke-bakåtkompatibel ändring har lagts till för att meddela att standardbeteendet för zoner kommer att ändras</span><span class="sxs-lookup"><span data-stu-id="a850c-720">Added breaking change attribute to notify that Zone default behaviour will be changed</span></span>
    - <span data-ttu-id="a850c-721">”New-AzPublicIpAddress”</span><span class="sxs-lookup"><span data-stu-id="a850c-721">'New-AzPublicIpAddress'</span></span>
    - <span data-ttu-id="a850c-722">”New-AzPublicIpPrefix”</span><span class="sxs-lookup"><span data-stu-id="a850c-722">'New-AzPublicIpPrefix'</span></span>
    - <span data-ttu-id="a850c-723">”New-AzLoadBalancerFrontendIpConfig”</span><span class="sxs-lookup"><span data-stu-id="a850c-723">'New-AzLoadBalancerFrontendIpConfig'</span></span>
* <span data-ttu-id="a850c-724">Stöd har lagts till för en ny resurs på den översta nivån, SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="a850c-724">Added support for a new top level resource SecurityPartnerProvider</span></span>
    - <span data-ttu-id="a850c-725">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="a850c-725">New cmdlets added:</span></span>
        - <span data-ttu-id="a850c-726">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="a850c-726">New-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="a850c-727">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="a850c-727">Remove-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="a850c-728">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="a850c-728">Get-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="a850c-729">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="a850c-729">Set-AzSecurityPartnerProvider</span></span>
* <span data-ttu-id="a850c-730">”RequiredZoneNames” har lagts till för ”PSPrivateLinkResource” och ”GroupId” för ”PSPrivateEndpointConnection”</span><span class="sxs-lookup"><span data-stu-id="a850c-730">Added 'RequiredZoneNames' on 'PSPrivateLinkResource' and 'GroupId' on 'PSPrivateEndpointConnection'</span></span>
* <span data-ttu-id="a850c-731">Fel parametertyp för SuccessThresholdRoundTripTimeMs-parametern för New-AzNetworkWatcherConnectionMonitorTestConfigurationObject har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="a850c-731">Fixed incorrect type of SuccessThresholdRoundTripTimeMs parameter for New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>
* <span data-ttu-id="a850c-732">VirtualWan-cmdletar har uppdaterats för att ange AllowVnetToVnetTraffic-argumentets standardvärde till True.</span><span class="sxs-lookup"><span data-stu-id="a850c-732">Updated VirtualWan cmdlets to set default value of AllowVnetToVnetTraffic argument to True.</span></span>
    - <span data-ttu-id="a850c-733">”New-AzVirtualWan”</span><span class="sxs-lookup"><span data-stu-id="a850c-733">'New-AzVirtualWan'</span></span>
    - <span data-ttu-id="a850c-734">”Update-AzVirtualWan”</span><span class="sxs-lookup"><span data-stu-id="a850c-734">'Update-AzVirtualWan'</span></span>
* <span data-ttu-id="a850c-735">Nya cmdletar har lagts till för att stödja DNS-zongrupp för privat slutpunkt</span><span class="sxs-lookup"><span data-stu-id="a850c-735">Added new cmdlets to support DNS zone group for private endpoint</span></span>
    - <span data-ttu-id="a850c-736">”New-AzPrivateDnsZoneConfig”</span><span class="sxs-lookup"><span data-stu-id="a850c-736">'New-AzPrivateDnsZoneConfig'</span></span>
    - <span data-ttu-id="a850c-737">”Get-AzPrivateDnsZoneGroup”</span><span class="sxs-lookup"><span data-stu-id="a850c-737">'Get-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="a850c-738">”New-AzPrivateDnsZoneGroup”</span><span class="sxs-lookup"><span data-stu-id="a850c-738">'New-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="a850c-739">”Set-AzPrivateDnsZoneGroup”</span><span class="sxs-lookup"><span data-stu-id="a850c-739">'Set-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="a850c-740">”Remove-AzPrivateDnsZoneGroup”</span><span class="sxs-lookup"><span data-stu-id="a850c-740">'Remove-AzPrivateDnsZoneGroup'</span></span>
* <span data-ttu-id="a850c-741">Parametrarna ”DNSEnableProxy”, ”DNSRequireProxyForNetworkRules” och ”DNSServers” har lagts till för ”AzureFirewall”</span><span class="sxs-lookup"><span data-stu-id="a850c-741">Added 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' and 'DNSServers' parameters to 'AzureFirewall'</span></span>
* <span data-ttu-id="a850c-742">Parametrarna ”EnableDnsProxy”, ”DnsProxyNotRequiredForNetworkRule” och ”DnsServer” har lagts till för ”AzureFirewall”</span><span class="sxs-lookup"><span data-stu-id="a850c-742">Added 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' and 'DnsServer' parameters to 'AzureFirewall'</span></span>
    - <span data-ttu-id="a850c-743">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="a850c-743">Updated cmdlet:</span></span>
        - <span data-ttu-id="a850c-744">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="a850c-744">New-AzFirewall</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="a850c-745">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a850c-745">Az.OperationalInsights</span></span>
* <span data-ttu-id="a850c-746">Äldre kod har uppdaterats för att tillämpa ny genererad SDK</span><span class="sxs-lookup"><span data-stu-id="a850c-746">Updated legacy code to apply new generated SDK</span></span>
* <span data-ttu-id="a850c-747">Cmdletar har tagits bort på grund av föråldrade API:er</span><span class="sxs-lookup"><span data-stu-id="a850c-747">Deleted cmdlets due to deprecated APIs</span></span>
    - <span data-ttu-id="a850c-748">”Get-AzOperationalInsightsSavedSearchResult” (alias ”Get-AzOperationalInsightsSavedSearchResults”)</span><span class="sxs-lookup"><span data-stu-id="a850c-748">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span></span>
    - <span data-ttu-id="a850c-749">”Get-AzOperationalInsightsSearchResult” (alias ”Get-AzOperationalInsightsSearchResults”)</span><span class="sxs-lookup"><span data-stu-id="a850c-749">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span></span>
    - <span data-ttu-id="a850c-750">”Get-AzOperationalInsightsLinkTarget” (alias ”Get-AzOperationalInsightsLinkTargets”)</span><span class="sxs-lookup"><span data-stu-id="a850c-750">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span></span>
* <span data-ttu-id="a850c-751">Parametrar har lagts till för ”Set-AzOperationalInsightsWorkspace” och ”New-AzOperationalInsightsWorkspace”</span><span class="sxs-lookup"><span data-stu-id="a850c-751">Added parameters for 'Set-AzOperationalInsightsWorkspace' and 'New-AzOperationalInsightsWorkspace'</span></span>
* <span data-ttu-id="a850c-752">Cmdletar har skapats för länkat lagringskonto</span><span class="sxs-lookup"><span data-stu-id="a850c-752">Created cmdlets for Linked Stoarge Account</span></span>
* <span data-ttu-id="a850c-753">Cmdletar har skapats för kluster och länkad tjänst</span><span class="sxs-lookup"><span data-stu-id="a850c-753">Created cmdlets for Clusters and Linked Service</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a850c-754">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a850c-754">Az.RecoveryServices</span></span>
* <span data-ttu-id="a850c-755">Azure Site Recovery: Stöd har lagts till för att skydda VM-närhetsplaceringsgrupper för Azure till Azure-provider.</span><span class="sxs-lookup"><span data-stu-id="a850c-755">Azure Site Recovery added support for protecting proximity placement group virtual machines for Azure to Azure provider.</span></span>
* <span data-ttu-id="a850c-756">Azure Site Recovery: Stöd har lagts till för replikering mellan zoner.</span><span class="sxs-lookup"><span data-stu-id="a850c-756">Azure Site Recovery added support for zone to zone replication.</span></span>
* <span data-ttu-id="a850c-757">Azure Backup: Stöd har lagts till för långsiktig kvarhållning för Azure FileShare-återställningspunkter.</span><span class="sxs-lookup"><span data-stu-id="a850c-757">Azure Backup Added Long term retention support for Azure FileShare Recovery Points.</span></span>
* <span data-ttu-id="a850c-758">Azure Backup: Egenskaper för diskexkludering har lagts till för cmdlet-utdata från ”Get-AzRecoveryServicesBackupItem”.</span><span class="sxs-lookup"><span data-stu-id="a850c-758">Azure Backup Added disk exclusion properties to 'Get-AzRecoveryServicesBackupItem' cmdlet output.</span></span>
* <span data-ttu-id="a850c-759">En privat slutpunkt har lagts till för filen med valvets autentiseringsuppgifter för Site Recovery-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="a850c-759">Added private endpoint for Vault credential file for site recovery service.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a850c-760">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a850c-760">Az.Resources</span></span>
* <span data-ttu-id="a850c-761">En varning har lagts till om visningsfördröjning när en ny rolldefinition skapas</span><span class="sxs-lookup"><span data-stu-id="a850c-761">Added message warning about view delay when creating a new Role Definition</span></span>
* <span data-ttu-id="a850c-762">Princip-cmdletar har ändrats för utmatning av starkt typifierade objekt</span><span class="sxs-lookup"><span data-stu-id="a850c-762">Changed policy cmdlets to output strongly-typed objects</span></span>
* <span data-ttu-id="a850c-763">Parametern ”-TenantLevel” har tagits bort för användning med ”Get-AzResourceLock” [#11335]</span><span class="sxs-lookup"><span data-stu-id="a850c-763">Removed '-TenantLevel' parameter used for on the 'Get-AzResourceLock' cmdlet [#11335]</span></span>
* <span data-ttu-id="a850c-764">”Remove-AzResourceGroup -Id ResourceId” har åtgärdats [#9882]</span><span class="sxs-lookup"><span data-stu-id="a850c-764">Fixed 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span></span>
* <span data-ttu-id="a850c-765">En ny cmdlet har lagts till för att hämta What-If-resultat för ARM-mallar i omfånget för resursgrupper: ”Get-AzDeploymentResourceGroupWhatIfResult”</span><span class="sxs-lookup"><span data-stu-id="a850c-765">Added new cmdlet for getting ARM template What-If results at resource group scope: 'Get-AzDeploymentResourceGroupWhatIfResult'</span></span>
* <span data-ttu-id="a850c-766">En ny cmdlet har lagts till för att hämta What-If-resultat för ARM-mallar i prenumerationsomfånget: ”Get-AzDeploymentWhatIfResult”</span><span class="sxs-lookup"><span data-stu-id="a850c-766">Added new cmdlet for getting ARM template What-If results at subscription scope: 'Get-AzDeploymentWhatIfResult'</span></span>
   - <span data-ttu-id="a850c-767">Alias: ”Get-AzSubscriptionDeploymentWhatIf”</span><span class="sxs-lookup"><span data-stu-id="a850c-767">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span></span>
* <span data-ttu-id="a850c-768">Parametrarna ”-WhatIf” och ”-Confirm” har åsidosatts för ”New-AzDeployment” och ”New-AzResourceGroupDeployment” för att använda What-If-resultat för ARM-mallar</span><span class="sxs-lookup"><span data-stu-id="a850c-768">Overrode '-WhatIf' and '-Confirm' parameters for 'New-AzDeployment' and 'New-AzResourceGroupDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="a850c-769">Ett utfasningsmeddelande har lagts till för parametern ”ApiVersion” i distributions-cmdletar</span><span class="sxs-lookup"><span data-stu-id="a850c-769">Added deprecation message for 'ApiVersion' parameter in deployment cmdlets</span></span>
* <span data-ttu-id="a850c-770">En funktion har lagts till för att visa förbättrade felmeddelanden för distributionsfel</span><span class="sxs-lookup"><span data-stu-id="a850c-770">Added capability to show improved error messages for deployment failures</span></span>
* <span data-ttu-id="a850c-771">CorrelationId-loggning har lagts till för distributionsfel</span><span class="sxs-lookup"><span data-stu-id="a850c-771">Added correlationId logging for deployment failures</span></span>
* <span data-ttu-id="a850c-772">Egenskapen ”error” har lagts till i utdata från distributionsskript</span><span class="sxs-lookup"><span data-stu-id="a850c-772">Added 'error' property to the deployment script output</span></span>
* <span data-ttu-id="a850c-773">Nuget Microsoft.Azure.Management.ResourceManager har uppdaterats till ”3.7.1-preview”</span><span class="sxs-lookup"><span data-stu-id="a850c-773">Updated nuget Microsoft.Azure.Management.ResourceManager to '3.7.1-preview'</span></span>
* <span data-ttu-id="a850c-774">Specifika testfall har tagits bort då egenskapen Error i DeploymentValidateResult har ändrats till lässkyddad från nuget 3.7.1-preview</span><span class="sxs-lookup"><span data-stu-id="a850c-774">Removed specific test cases as Error property in DeploymentValidateResult has changed to readonly from nuget 3.7.1-preview</span></span>
* <span data-ttu-id="a850c-775">GenericResourceExpanded har flyttats från SDK ResourceManager 3.7.1-preview</span><span class="sxs-lookup"><span data-stu-id="a850c-775">Brought GenericResourceExpanded from SDK ResourceManager 3.7.1-preview</span></span>
* <span data-ttu-id="a850c-776">Stöd för taggar har lagts till för alla Get-cmdletar för distribution, samt</span><span class="sxs-lookup"><span data-stu-id="a850c-776">Added tag support for all Get cmdlets for deployment, as well as</span></span>
    - <span data-ttu-id="a850c-777">”New-AzDeployment”</span><span class="sxs-lookup"><span data-stu-id="a850c-777">'New-AzDeployment'</span></span>
    - <span data-ttu-id="a850c-778">”New-AzManagementGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="a850c-778">'New-AzManagementGroupDeployment'</span></span>
    - <span data-ttu-id="a850c-779">”New-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="a850c-779">'New-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="a850c-780">”New-AzTenantDeployment”</span><span class="sxs-lookup"><span data-stu-id="a850c-780">'New-AzTenantDeployment'</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a850c-781">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a850c-781">Az.ServiceFabric</span></span>
* <span data-ttu-id="a850c-782">En bugg har åtgärdats som gjorde att --SecretIdentifier fick fel tumavtryck för certifikat när ett certifikat lades till</span><span class="sxs-lookup"><span data-stu-id="a850c-782">Fixed bug in add certificate using --SecretIdentifier that was getting the wrong certificate thumbprint</span></span>

#### <a name="azsql"></a><span data-ttu-id="a850c-783">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a850c-783">Az.Sql</span></span>
* <span data-ttu-id="a850c-784">Förbättrade prestanda för:</span><span class="sxs-lookup"><span data-stu-id="a850c-784">Enhance performance of:</span></span>
    - <span data-ttu-id="a850c-785">”Set-AzSqlDatabaseSensitivityClassification”</span><span class="sxs-lookup"><span data-stu-id="a850c-785">'Set-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="a850c-786">”Set-AzSqlInstanceDatabaseSensitivityClassification”</span><span class="sxs-lookup"><span data-stu-id="a850c-786">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="a850c-787">”Remove-AzSqlDatabaseSensitivityClassification”</span><span class="sxs-lookup"><span data-stu-id="a850c-787">'Remove-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="a850c-788">”Remove-AzSqlInstanceDatabaseSensitivityClassification”</span><span class="sxs-lookup"><span data-stu-id="a850c-788">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="a850c-789">”Enable-AzSqlDatabaseSensitivityRecommendation”</span><span class="sxs-lookup"><span data-stu-id="a850c-789">'Enable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="a850c-790">”Enable-AzSqlInstanceDatabaseSensitivityRecommendation”</span><span class="sxs-lookup"><span data-stu-id="a850c-790">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="a850c-791">”Disable-AzSqlDatabaseSensitivityRecommendation”</span><span class="sxs-lookup"><span data-stu-id="a850c-791">'Disable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="a850c-792">”Disable-AzSqlInstanceDatabaseSensitivityRecommendation”</span><span class="sxs-lookup"><span data-stu-id="a850c-792">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
* <span data-ttu-id="a850c-793">Validering på klientsidan har tagits bort för parametern ”RetentionDays” från cmdleten ”Set-AzSqlDatabaseBackupShortTermRetentionPolicy”</span><span class="sxs-lookup"><span data-stu-id="a850c-793">Removed client-side validation of 'RetentionDays' parameter from cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span>
* <span data-ttu-id="a850c-794">Granskning av ett lagringskonto i Vnet; en bugg har åtgärdats som orsakade fel när en Storage Blob Data-deltagarroll skapades.</span><span class="sxs-lookup"><span data-stu-id="a850c-794">Auditing to a storage account in Vnet, fixing a bug when creating a Storage Blob Data Contributor role.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a850c-795">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a850c-795">Az.Storage</span></span>
* <span data-ttu-id="a850c-796">”-AsJob” har lagts till för att hämta/lista konto med cmdleten ”Get-AzStorageAccount”</span><span class="sxs-lookup"><span data-stu-id="a850c-796">Added '-AsJob' to get/list account cmdlet 'Get-AzStorageAccount'</span></span>
* <span data-ttu-id="a850c-797">Gör KeyVersion valfri när lagringskontot uppdateras med KeyvaultEncryption, för att ge stöd för automatisk nyckelrotation</span><span class="sxs-lookup"><span data-stu-id="a850c-797">Make KeyVersion to optional when update Storage account with KeyvaultEncryption, to support key auto-rotation</span></span>
    - <span data-ttu-id="a850c-798">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="a850c-798">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="a850c-799">Problemet med borttagning av Azure-filkatalog i pipeline har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="a850c-799">Fixed remove Azure File Directory fail with pipeline</span></span>
    - <span data-ttu-id="a850c-800">”Remove-AzStorageDirectory”</span><span class="sxs-lookup"><span data-stu-id="a850c-800">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="a850c-801">Åtgärdat [#9880]: Definitionen av DefaultAction-värdet för NetWorkRule har ändrats för konsekvens med Swagger.</span><span class="sxs-lookup"><span data-stu-id="a850c-801">Fixed [#9880]: Change NetWorkRule DefaultAction value defination to align with swagger.</span></span>
    - <span data-ttu-id="a850c-802">”Update-AzStorageAccountNetworkRuleSet”</span><span class="sxs-lookup"><span data-stu-id="a850c-802">'Update-AzStorageAccountNetworkRuleSet'</span></span>
    - <span data-ttu-id="a850c-803">”Get-AzStorageAccountNetworkRuleSet”</span><span class="sxs-lookup"><span data-stu-id="a850c-803">'Get-AzStorageAccountNetworkRuleSet'</span></span>
* <span data-ttu-id="a850c-804">Åtgärdat [#11624]: Hoppa över dubblettregler när NetworkRules läggs till, för att undvika serverfel</span><span class="sxs-lookup"><span data-stu-id="a850c-804">Fixed [#11624]: Skip duplicated rules when add NetworkRules, to avoid server failure</span></span>
    - <span data-ttu-id="a850c-805">”Add-AzStorageAccountNetworkRule”</span><span class="sxs-lookup"><span data-stu-id="a850c-805">'Add-AzStorageAccountNetworkRule'</span></span>
* <span data-ttu-id="a850c-806">Microsoft.Azure.Cosmos.Table SDK har uppgraderats till 1.0.7</span><span class="sxs-lookup"><span data-stu-id="a850c-806">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.7</span></span>
* <span data-ttu-id="a850c-807">Ett varningsmeddelande har lagts till för att påminna användaren om att lista igen med ContinuationToken när endast delobjekt returneras i listan med DataLake Gen2-objekt,</span><span class="sxs-lookup"><span data-stu-id="a850c-807">Added a warning message to remind user to list again with ContinuationToken when only part items are returned in list DataLake Gen2 Items,</span></span>
    - <span data-ttu-id="a850c-808">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="a850c-808">'Get-AzDataLakeGen2ChildItem'</span></span>
* <span data-ttu-id="a850c-809">Stöd för att skapa eller uppdatera lagringskonto med Azure Files Active Directory Domain Service-autentisering</span><span class="sxs-lookup"><span data-stu-id="a850c-809">Supported to create or update Storage account with Azure Files Active Directory Domain Service Authentication</span></span>
    -  <span data-ttu-id="a850c-810">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="a850c-810">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="a850c-811">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="a850c-811">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="a850c-812">Stöd för nya eller listade Kerberos-nycklar för lagringskontot</span><span class="sxs-lookup"><span data-stu-id="a850c-812">Supported to new or list Kerberos keys of Storage account</span></span>
    -  <span data-ttu-id="a850c-813">”New-AzStorageAccountKey”</span><span class="sxs-lookup"><span data-stu-id="a850c-813">'New-AzStorageAccountKey'</span></span>
    -  <span data-ttu-id="a850c-814">”Get-AzStorageAccountKey”</span><span class="sxs-lookup"><span data-stu-id="a850c-814">'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="a850c-815">Stöd för redundans med lagringskonto</span><span class="sxs-lookup"><span data-stu-id="a850c-815">Supported failover Storage account</span></span>
    - <span data-ttu-id="a850c-816">”Invoke-AzStorageAccountFailover”</span><span class="sxs-lookup"><span data-stu-id="a850c-816">'Invoke-AzStorageAccountFailover'</span></span>
* <span data-ttu-id="a850c-817">Hjälpen för ”Get-AzStorageBlobCopyState” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="a850c-817">Updated help of 'Get-AzStorageBlobCopyState'</span></span>
* <span data-ttu-id="a850c-818">Hjälpen för ”Get-AzStorageFileCopyState” och ”Start-AzStorageBlobCopy” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="a850c-818">Updated help of 'Get-AzStorageFileCopyState' and 'Start-AzStorageBlobCopy'</span></span>
* <span data-ttu-id="a850c-819">Lagringsklientbibliotek v12 har integrerats med Queue- och File-cmdletar</span><span class="sxs-lookup"><span data-stu-id="a850c-819">Integrated Storage client library v12 to Queue and File cmdlets</span></span>
* <span data-ttu-id="a850c-820">Utdatatypen har ändrats från CloudFile till AzureStorageFile; ursprungliga utdata blir en underordnad egenskap i den nya utmatningen</span><span class="sxs-lookup"><span data-stu-id="a850c-820">Changed output type from CloudFile to AzureStorageFile, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="a850c-821">”Get-AzStorageFile”</span><span class="sxs-lookup"><span data-stu-id="a850c-821">'Get-AzStorageFile'</span></span>
    - <span data-ttu-id="a850c-822">”Remove-AzStorageFile”</span><span class="sxs-lookup"><span data-stu-id="a850c-822">'Remove-AzStorageFile'</span></span>
    - <span data-ttu-id="a850c-823">”Get-AzStorageFileContent”</span><span class="sxs-lookup"><span data-stu-id="a850c-823">'Get-AzStorageFileContent'</span></span>
    - <span data-ttu-id="a850c-824">”Set-AzStorageFileContent”</span><span class="sxs-lookup"><span data-stu-id="a850c-824">'Set-AzStorageFileContent'</span></span>
    - <span data-ttu-id="a850c-825">”Start-AzStorageFileCopy”</span><span class="sxs-lookup"><span data-stu-id="a850c-825">'Start-AzStorageFileCopy'</span></span>
* <span data-ttu-id="a850c-826">Utdatatypen har ändrats från CloudFileDirectory till AzureStorageFileDirectory; ursprungliga utdata blir en underordnad egenskap i den nya utmatningen</span><span class="sxs-lookup"><span data-stu-id="a850c-826">Changed output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="a850c-827">”New-AzStorageDirectory”</span><span class="sxs-lookup"><span data-stu-id="a850c-827">'New-AzStorageDirectory'</span></span>
    - <span data-ttu-id="a850c-828">”Remove-AzStorageDirectory”</span><span class="sxs-lookup"><span data-stu-id="a850c-828">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="a850c-829">Utdatatypen har ändrats från CloudFileShare till AzureStorageFileShare; ursprungliga utdata blir en underordnad egenskap i den nya utmatningen</span><span class="sxs-lookup"><span data-stu-id="a850c-829">Changed output type from CloudFileShare to AzureStorageFileShare, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="a850c-830">”Get-AzStorageShare”</span><span class="sxs-lookup"><span data-stu-id="a850c-830">'Get-AzStorageShare'</span></span>
    - <span data-ttu-id="a850c-831">”New-AzStorageShare”</span><span class="sxs-lookup"><span data-stu-id="a850c-831">'New-AzStorageShare'</span></span>
    - <span data-ttu-id="a850c-832">”Remove-AzStorageShare”</span><span class="sxs-lookup"><span data-stu-id="a850c-832">'Remove-AzStorageShare'</span></span>
* <span data-ttu-id="a850c-833">Utdatatypen har ändrats från FileShareProperties till AzureStorageFileShare; ursprungliga utdata blir en underordnad egenskap i den nya utmatningen</span><span class="sxs-lookup"><span data-stu-id="a850c-833">Changed output type from FileShareProperties to AzureStorageFileShare, the original output will become a sub child property of the new output</span></span>
    - <span data-ttu-id="a850c-834">”Set-AzStorageShareQuota”</span><span class="sxs-lookup"><span data-stu-id="a850c-834">'Set-AzStorageShareQuota'</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="a850c-835">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="a850c-835">Az.TrafficManager</span></span>
* <span data-ttu-id="a850c-836">Felaktigt profilnamn har åtgärdats i utförliga utdata för ”DisableAzureTrafficManagerEndpoint”</span><span class="sxs-lookup"><span data-stu-id="a850c-836">Fixed incorrect profile name in 'DisableAzureTrafficManagerEndpoint' verbose output</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a850c-837">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a850c-837">Az.Websites</span></span>
* <span data-ttu-id="a850c-838">Stavfel har åtgärdats i hjälpen för ”Update-AzWebAppAccessRestrictionConfig”.</span><span class="sxs-lookup"><span data-stu-id="a850c-838">Fixed typo on help of 'Update-AzWebAppAccessRestrictionConfig'.</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="a850c-839">3.8.0 – April 2020</span><span class="sxs-lookup"><span data-stu-id="a850c-839">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="a850c-840">Höjdpunkter sedan den senaste uppdateringen</span><span class="sxs-lookup"><span data-stu-id="a850c-840">Highlights since the last release</span></span>
* <span data-ttu-id="a850c-841">PowerShell-versioner som Az.Storage stöder: Windows PowerShell 5.1, PowerShell Core 6.2.4+ och PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="a850c-841">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="a850c-842">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a850c-842">Az.Accounts</span></span>
* <span data-ttu-id="a850c-843">Uppdaterade URL:en för Azure PowerShell-enkäten i ”Resolve-AzError” [#11507]</span><span class="sxs-lookup"><span data-stu-id="a850c-843">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="a850c-844">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a850c-844">Az.ApiManagement</span></span>
* <span data-ttu-id="a850c-845">Lade till meddelande om icke-bakåtkompatibel ändring vid ändring i utdata för Azure File-cmdletar i en framtida version</span><span class="sxs-lookup"><span data-stu-id="a850c-845">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="a850c-846">"Set-AzApiManagementGroup" Uppdaterad dokumentation för att ange GroupId-parametern</span><span class="sxs-lookup"><span data-stu-id="a850c-846">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="a850c-847">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="a850c-847">Az.Cdn</span></span>
* <span data-ttu-id="a850c-848">Fast ChinaCDN-relaterad prissättning för SKU-visning</span><span class="sxs-lookup"><span data-stu-id="a850c-848">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="a850c-849">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a850c-849">Az.CognitiveServices</span></span>
* <span data-ttu-id="a850c-850">Identitet som stöds, kryptering, UserOwnedStorage</span><span class="sxs-lookup"><span data-stu-id="a850c-850">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a850c-851">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a850c-851">Az.Compute</span></span>
* <span data-ttu-id="a850c-852">Cmdleten ”Set-AzVmssOrchestrationServiceState” har lagts till.</span><span class="sxs-lookup"><span data-stu-id="a850c-852">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="a850c-853">”Get-AzVmss” med -InstanceView visar OrchestrationService-tillstånd.</span><span class="sxs-lookup"><span data-stu-id="a850c-853">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a850c-854">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a850c-854">Az.IotHub</span></span>
* <span data-ttu-id="a850c-855">Hantera den dubbla konfigurationen för IoT-enheter, nya cmdletar är:</span><span class="sxs-lookup"><span data-stu-id="a850c-855">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="a850c-856">'Get-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="a850c-856">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="a850c-857">'Update-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="a850c-857">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="a850c-858">En cmdlet har lagts till för att anropa direkt metod på en enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="a850c-858">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="a850c-859">Hantera dubbel konfiguration för IoT-enhetsmodul, nya cmdletar är:</span><span class="sxs-lookup"><span data-stu-id="a850c-859">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="a850c-860">'Get-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="a850c-860">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="a850c-861">'Update-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="a850c-861">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="a850c-862">Hantera IoT-automatisk konfiguration av enhetshantering i stor skala.</span><span class="sxs-lookup"><span data-stu-id="a850c-862">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="a850c-863">Nya cmdlet:ar är:</span><span class="sxs-lookup"><span data-stu-id="a850c-863">New cmdlets are:</span></span>
    - <span data-ttu-id="a850c-864">'Add-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="a850c-864">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="a850c-865">'Get-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="a850c-865">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="a850c-866">'Remove-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="a850c-866">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="a850c-867">'Set-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="a850c-867">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="a850c-868">En cmdlet har lagts till för att anropa en edge-modulmetod i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="a850c-868">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a850c-869">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a850c-869">Az.KeyVault</span></span>
* <span data-ttu-id="a850c-870">Har lagt till en ny cmdlet, "Update-AzKeyVault", som kan aktivera mjuk borttagning och rensning av skydd i ett valv</span><span class="sxs-lookup"><span data-stu-id="a850c-870">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="a850c-871">Har lagt till stöd i Microsoft.PowerShell.SecretManagement [#11178]</span><span class="sxs-lookup"><span data-stu-id="a850c-871">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="a850c-872">Åtgärdat fel i exemplen i 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span><span class="sxs-lookup"><span data-stu-id="a850c-872">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="a850c-873">Har lagt till stöd för privat slutpunkt</span><span class="sxs-lookup"><span data-stu-id="a850c-873">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="a850c-874">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="a850c-874">Az.Maintenance</span></span>
* <span data-ttu-id="a850c-875">Publicerar slutversion av underhålls-cmdletar för GA</span><span class="sxs-lookup"><span data-stu-id="a850c-875">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a850c-876">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a850c-876">Az.Monitor</span></span>
* <span data-ttu-id="a850c-877">Har lagt till cmdletar för privat länkomfång</span><span class="sxs-lookup"><span data-stu-id="a850c-877">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="a850c-878">'Get-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="a850c-878">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="a850c-879">'Remove-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="a850c-879">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="a850c-880">'New-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="a850c-880">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="a850c-881">'Update-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="a850c-881">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="a850c-882">'Get-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="a850c-882">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="a850c-883">'New-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="a850c-883">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="a850c-884">'Remove-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="a850c-884">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a850c-885">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a850c-885">Az.Network</span></span>
* <span data-ttu-id="a850c-886">Uppdaterade cmdletar för att aktivera anslutning på privat IP för Virtual Network Gateway.</span><span class="sxs-lookup"><span data-stu-id="a850c-886">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="a850c-887">'New-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="a850c-887">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="a850c-888">'Set-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="a850c-888">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="a850c-889">'New-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="a850c-889">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="a850c-890">'Set-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="a850c-890">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="a850c-891">Uppdaterade cmdletar för att aktivera FQDN-baserade LocalNetworkGateways och VpnSites</span><span class="sxs-lookup"><span data-stu-id="a850c-891">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="a850c-892">'New-AzLocalNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="a850c-892">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="a850c-893">'New-AzVpnSiteLink'</span><span class="sxs-lookup"><span data-stu-id="a850c-893">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="a850c-894">Stöd har lagts till för IPv6-adresstypen i ExpressRouteCircuitConnectionConfig (Global Reach)</span><span class="sxs-lookup"><span data-stu-id="a850c-894">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="a850c-895">Lade till 'Set-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="a850c-895">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="a850c-896">tillåter inställning av alla befintliga egenskaper inklusive IPv6CircuitConnectionProperties</span><span class="sxs-lookup"><span data-stu-id="a850c-896">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="a850c-897">Uppdaterade 'Add-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="a850c-897">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="a850c-898">Lade till en ytterligare valfri parameter, AddressPrefixType, för att specificera adresstypen för adressprefix</span><span class="sxs-lookup"><span data-stu-id="a850c-898">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="a850c-899">Uppdaterade cmdletar för att aktivera inställningen för DPD-timeout på Virtual Network Gateway-anslutningar.</span><span class="sxs-lookup"><span data-stu-id="a850c-899">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="a850c-900">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="a850c-900">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="a850c-901">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="a850c-901">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="a850c-902">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a850c-902">Az.PolicyInsights</span></span>
* <span data-ttu-id="a850c-903">Cmdleten "Start-AzPolicyComplianceScan" har lagts till för att utlösa genomsökningar av principefterlevnad</span><span class="sxs-lookup"><span data-stu-id="a850c-903">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="a850c-904">Principdefinition, uppsättningsdefinition och tilldelningsversioner har lagts till i "Get-AzPolicyState"-utdata</span><span class="sxs-lookup"><span data-stu-id="a850c-904">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a850c-905">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a850c-905">Az.ServiceFabric</span></span>
* <span data-ttu-id="a850c-906">Förbättrad kodformatering och användbarhet för "New-AzServiceFabricCluster"-exempel</span><span class="sxs-lookup"><span data-stu-id="a850c-906">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="a850c-907">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a850c-907">Az.Sql</span></span>
* <span data-ttu-id="a850c-908">Lade till cmdletarna "Get-AzSqlInstanceOperation" och "Stop-AzSqlInstanceOperation"</span><span class="sxs-lookup"><span data-stu-id="a850c-908">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="a850c-909">Stöd för granskning för ett lagringskonto i VNet.</span><span class="sxs-lookup"><span data-stu-id="a850c-909">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a850c-910">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a850c-910">Az.Storage</span></span>
* <span data-ttu-id="a850c-911">Lade till meddelande om icke-bakåtkompatibel ändring vid ändring i utdata för Azure File-cmdletar i en framtida version</span><span class="sxs-lookup"><span data-stu-id="a850c-911">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="a850c-912">Stöd för nya SkuName StandardGZRS, StandardRAGZRS när ett lagringskonto skapas/uppdateras</span><span class="sxs-lookup"><span data-stu-id="a850c-912">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="a850c-913">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="a850c-913">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="a850c-914">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="a850c-914">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="a850c-915">Stöd för DataLake Gen2</span><span class="sxs-lookup"><span data-stu-id="a850c-915">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="a850c-916">'New-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="a850c-916">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="a850c-917">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="a850c-917">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="a850c-918">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="a850c-918">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="a850c-919">'Move-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="a850c-919">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="a850c-920">'Set-AzDataLakeGen2ItemAclObject'</span><span class="sxs-lookup"><span data-stu-id="a850c-920">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="a850c-921">'Update-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="a850c-921">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="a850c-922">'Get-AzDataLakeGen2ItemContent'</span><span class="sxs-lookup"><span data-stu-id="a850c-922">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="a850c-923">'Remove-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="a850c-923">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="a850c-924">0.10.0-förhandsversion – April 2020</span><span class="sxs-lookup"><span data-stu-id="a850c-924">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="a850c-925">Allmänt</span><span class="sxs-lookup"><span data-stu-id="a850c-925">General</span></span>
* <span data-ttu-id="a850c-926">Az-moduler är nu tillgängliga i förhandsversion på Azure Stack Hub.</span><span class="sxs-lookup"><span data-stu-id="a850c-926">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="a850c-927">Därmed möjliggörs kompatibilitet för flera plattformar med Linux och macOs.</span><span class="sxs-lookup"><span data-stu-id="a850c-927">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="a850c-928">Azure Stack Hub stöder nu PowerShell Core med AZ-moduler. Mer information finns [här](https://aka.ms/az4AzureStack)</span><span class="sxs-lookup"><span data-stu-id="a850c-928">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](https://aka.ms/az4AzureStack)</span></span>
* <span data-ttu-id="a850c-929">Supportprofil för AZ-moduler 2019-03-01-hybrid:</span><span class="sxs-lookup"><span data-stu-id="a850c-929">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="a850c-930">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="a850c-930">Az.Billing</span></span>
  - <span data-ttu-id="a850c-931">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a850c-931">Az.Compute</span></span>
  - <span data-ttu-id="a850c-932">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="a850c-932">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="a850c-933">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a850c-933">Az.EventHub</span></span>
  - <span data-ttu-id="a850c-934">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a850c-934">Az.IotHub</span></span>
  - <span data-ttu-id="a850c-935">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a850c-935">Az.KeyVault</span></span>
  - <span data-ttu-id="a850c-936">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a850c-936">Az.Monitor</span></span>
  - <span data-ttu-id="a850c-937">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a850c-937">Az.Network</span></span>
  - <span data-ttu-id="a850c-938">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a850c-938">Az.Resources</span></span>
  - <span data-ttu-id="a850c-939">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a850c-939">Az.Storage</span></span>
  - <span data-ttu-id="a850c-940">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a850c-940">Az.Websites</span></span>
* <span data-ttu-id="a850c-941">Tre nya PowerShell-moduler för AZ har introducerats som fungerar med Azure Stack Hub, och de är Az.Databox, Az.IotHub och Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a850c-941">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="a850c-942">Kommandona är i princip oförändrade, med endast mindre ändringar som att AzureRM ändras till AZ</span><span class="sxs-lookup"><span data-stu-id="a850c-942">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="a850c-943">En uppdaterad länk till PowerShell-dokumentationen för Azure Stack Hub finns [här](https://aka.ms/InstallASHPowerShell)</span><span class="sxs-lookup"><span data-stu-id="a850c-943">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](https://aka.ms/InstallASHPowerShell)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="a850c-944">3.7.0 – mars 2020</span><span class="sxs-lookup"><span data-stu-id="a850c-944">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a850c-945">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a850c-945">Az.Accounts</span></span>
* <span data-ttu-id="a850c-946">Åtgärdade ”Get-AzTenant”/”Get-AzDefault”/”Set-AzDefault”-utlösning av NullReferenceException när du inte är inloggad [#10292]</span><span class="sxs-lookup"><span data-stu-id="a850c-946">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a850c-947">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a850c-947">Az.Compute</span></span>
* <span data-ttu-id="a850c-948">Följande parametrar har lagts till i cmdleten ”New-AzDiskConfig”:</span><span class="sxs-lookup"><span data-stu-id="a850c-948">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="a850c-949">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="a850c-949">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="a850c-950">Tillåten krypteringsegenskap till målparametern för cmdleten ”New-AzGalleryImageVersion”.</span><span class="sxs-lookup"><span data-stu-id="a850c-950">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="a850c-951">Åtgärdade tempDisk-problem för cmdletarna ”Set-AzVmss”-Reimage och ”Invoke-AzVMReimage”.</span><span class="sxs-lookup"><span data-stu-id="a850c-951">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="a850c-952">[#11354]</span><span class="sxs-lookup"><span data-stu-id="a850c-952">[#11354]</span></span>
* <span data-ttu-id="a850c-953">Stöd har lagts till i nedanstående cmdletar för nytt SAP-tillägg</span><span class="sxs-lookup"><span data-stu-id="a850c-953">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="a850c-954">”Set-AzVMAEMExtension”</span><span class="sxs-lookup"><span data-stu-id="a850c-954">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="a850c-955">”Get-AzVMAEMExtension”</span><span class="sxs-lookup"><span data-stu-id="a850c-955">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="a850c-956">”Remove-AzVMAEMExtension”</span><span class="sxs-lookup"><span data-stu-id="a850c-956">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="a850c-957">”Update-AzVMAEMExtension”</span><span class="sxs-lookup"><span data-stu-id="a850c-957">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="a850c-958">Åtgärdade fel i exempel på hjälpdokument</span><span class="sxs-lookup"><span data-stu-id="a850c-958">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="a850c-959">Visade det exakta strängvärdet för VM PowerState i tabellformat.</span><span class="sxs-lookup"><span data-stu-id="a850c-959">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="a850c-960">”New-AzVmssConfig”: den fasta serialiseringen av egenskapen AutomaticRepairs när SinglePlacementGroup är inaktiverad.</span><span class="sxs-lookup"><span data-stu-id="a850c-960">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="a850c-961">[#11257]</span><span class="sxs-lookup"><span data-stu-id="a850c-961">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a850c-962">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a850c-962">Az.DataFactory</span></span>
* <span data-ttu-id="a850c-963">ADF .Net SDK har uppdaterats till 4.8.0</span><span class="sxs-lookup"><span data-stu-id="a850c-963">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="a850c-964">Valfria parametrar har lagts till i kommandot ”Invoke-AzDataFactoryV2Pipeline” för att stödja omkörning</span><span class="sxs-lookup"><span data-stu-id="a850c-964">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a850c-965">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a850c-965">Az.DataLakeStore</span></span>
* <span data-ttu-id="a850c-966">Lade till beskrivning för icke-bakåtkompatibel ändring för ”Export-AzDataLakeStoreItem” och ”Import-AzDataLakeStoreItem”</span><span class="sxs-lookup"><span data-stu-id="a850c-966">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="a850c-967">Lade till alternativ för bytekodning för ”New-AzDataLakeStoreItem”, ”Add-AzDAtaLakeStoreItemContent” och ”Get-AzDAtaLakeStoreItemContent”</span><span class="sxs-lookup"><span data-stu-id="a850c-967">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="a850c-968">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a850c-968">Az.HDInsight</span></span>
* <span data-ttu-id="a850c-969">Stöd för att ange en minimal TLS-version som stöds när klustret skapas.</span><span class="sxs-lookup"><span data-stu-id="a850c-969">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a850c-970">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a850c-970">Az.IotHub</span></span>
* <span data-ttu-id="a850c-971">Stöd har lagts till för att hantera distribuerade inställningar per enhet.</span><span class="sxs-lookup"><span data-stu-id="a850c-971">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="a850c-972">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="a850c-972">New Cmdlets are:</span></span>
    - <span data-ttu-id="a850c-973">”Get-AzIotHubDistributedTracing”</span><span class="sxs-lookup"><span data-stu-id="a850c-973">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="a850c-974">”Set-AzIotHubDistributedTracing”</span><span class="sxs-lookup"><span data-stu-id="a850c-974">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a850c-975">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a850c-975">Az.KeyVault</span></span>
* <span data-ttu-id="a850c-976">Ändrade attribut för icke-bakåtkompatibel ändring lades till för ”New-AzKeyVault”</span><span class="sxs-lookup"><span data-stu-id="a850c-976">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a850c-977">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a850c-977">Az.Monitor</span></span>
* <span data-ttu-id="a850c-978">Uppdaterad dokumentation för ”New-AzScheduledQueryRuleLogMetricTrigger”</span><span class="sxs-lookup"><span data-stu-id="a850c-978">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a850c-979">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a850c-979">Az.Network</span></span>
* <span data-ttu-id="a850c-980">Uppdaterade cmdletar för att tillåta VirtualHubVnetConnections mellan klienter</span><span class="sxs-lookup"><span data-stu-id="a850c-980">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="a850c-981">”New-AzVirtualHubVnetConnection”</span><span class="sxs-lookup"><span data-stu-id="a850c-981">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="a850c-982">”Update-AzVirtualHubVnetConnection”</span><span class="sxs-lookup"><span data-stu-id="a850c-982">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="a850c-983">”New-AzVirtualHub”</span><span class="sxs-lookup"><span data-stu-id="a850c-983">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="a850c-984">”Update-AzVirtualHub”</span><span class="sxs-lookup"><span data-stu-id="a850c-984">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="a850c-985">SQL Management SDK-beroende har tagits bort</span><span class="sxs-lookup"><span data-stu-id="a850c-985">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="a850c-986">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a850c-986">Az.PolicyInsights</span></span>
* <span data-ttu-id="a850c-987">Förbättrade felmeddelanden</span><span class="sxs-lookup"><span data-stu-id="a850c-987">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a850c-988">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a850c-988">Az.RecoveryServices</span></span>
* <span data-ttu-id="a850c-989">Azure Site Recovery har lagt till stöd för återaktivering av skydd och uppdaterade VM-egenskaper för virtuella Azure-datorer med krypterad disk.</span><span class="sxs-lookup"><span data-stu-id="a850c-989">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="a850c-990">Lade till Azure Site Recovery VmwareToAzure-egenskaper för DR-övervakning</span><span class="sxs-lookup"><span data-stu-id="a850c-990">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="a850c-991">Azure Backup har lagt till stöd för att försöka uppdatera principuppdateringen för misslyckade objekt på nytt.</span><span class="sxs-lookup"><span data-stu-id="a850c-991">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="a850c-992">Azure Backup lagt till stöd för diskundantagsinställningar under säkerhetskopiering och återställning.</span><span class="sxs-lookup"><span data-stu-id="a850c-992">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="a850c-993">Azure Backup lagt till stöd för att återställa flera filer/mappar i AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="a850c-993">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="a850c-994">Azure Backup lade till support för användardefinierad Resourcegroup-support vid uppdatering av IaasVM-princip</span><span class="sxs-lookup"><span data-stu-id="a850c-994">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="a850c-995">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a850c-995">Az.Resources</span></span>
* <span data-ttu-id="a850c-996">Åtgärdade ”Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType” så att den använder den faktisk apiVersion av resurser i stället för standard-apiVersion [#11267]</span><span class="sxs-lookup"><span data-stu-id="a850c-996">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="a850c-997">Lade till correlationId-loggning för felscenarier</span><span class="sxs-lookup"><span data-stu-id="a850c-997">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="a850c-998">Liten dokumentationsändring för ”Get-AzResourceLock”.</span><span class="sxs-lookup"><span data-stu-id="a850c-998">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="a850c-999">Lade till exempel.</span><span class="sxs-lookup"><span data-stu-id="a850c-999">Added example.</span></span>
* <span data-ttu-id="a850c-1000">Undantaget enkelt citattecken i parametervärde för ”Get-AzADUser” [#11317]</span><span class="sxs-lookup"><span data-stu-id="a850c-1000">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="a850c-1001">Nya cmdletar har lagts till för distributionsskript (”Get-AzDeploymentScript”, ”Get-AzDeploymentScriptLog”, ”Save-AzDeploymentScriptLog”, ”Remove-AzDeploymentScript”)</span><span class="sxs-lookup"><span data-stu-id="a850c-1001">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="a850c-1002">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a850c-1002">Az.Sql</span></span>
* <span data-ttu-id="a850c-1003">En läsbar sekundär parameter har lagts till i Invoke-AzSqlDatabaseFailover</span><span class="sxs-lookup"><span data-stu-id="a850c-1003">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="a850c-1004">Cmdleten Disable-AzSqlServerActiveDirectoryOnlyAuthentication har lagts till</span><span class="sxs-lookup"><span data-stu-id="a850c-1004">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="a850c-1005">Den sparade känslighet rangordningen när kolumner klassificeras i databasen.</span><span class="sxs-lookup"><span data-stu-id="a850c-1005">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="a850c-1006">Az.Support</span><span class="sxs-lookup"><span data-stu-id="a850c-1006">Az.Support</span></span>
* <span data-ttu-id="a850c-1007">Allmän tillgänglighet för ”Az.Support”-modulen</span><span class="sxs-lookup"><span data-stu-id="a850c-1007">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a850c-1008">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a850c-1008">Az.Websites</span></span>
* <span data-ttu-id="a850c-1009">Stöd har lagts till för att arbeta med trafikdirigeringsregler för webbappar under nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="a850c-1009">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="a850c-1010">”Get-AzWebAppTrafficRouting”</span><span class="sxs-lookup"><span data-stu-id="a850c-1010">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="a850c-1011">”Update-AzWebAppTrafficRouting”</span><span class="sxs-lookup"><span data-stu-id="a850c-1011">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="a850c-1012">”Add-AzWebAppTrafficRouting”</span><span class="sxs-lookup"><span data-stu-id="a850c-1012">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="a850c-1013">”Remove-AzWebAppTrafficRouting”</span><span class="sxs-lookup"><span data-stu-id="a850c-1013">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="a850c-1014">3.6.1 – mars 2020</span><span class="sxs-lookup"><span data-stu-id="a850c-1014">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a850c-1015">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a850c-1015">Az.Accounts</span></span>
* <span data-ttu-id="a850c-1016">Öppna sidan med Azure PowerShell-enkäten i ”Send-Feedback” [#11020]</span><span class="sxs-lookup"><span data-stu-id="a850c-1016">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="a850c-1017">Visa URL:en för Azure PowerShell-enkäten i ”Resolve-Error” [#11021]</span><span class="sxs-lookup"><span data-stu-id="a850c-1017">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="a850c-1018">Az-version har lagts till i UserAgent</span><span class="sxs-lookup"><span data-stu-id="a850c-1018">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="a850c-1019">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a850c-1019">Az.ApiManagement</span></span>
* <span data-ttu-id="a850c-1020">Stöd har lagts till för att hämta och konfigurera en anpassad domän på DeveloperPortal-slutpunkten [#11007]</span><span class="sxs-lookup"><span data-stu-id="a850c-1020">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="a850c-1021">”Export-AzApiManagementApi” Stöd har lagts till för att ladda ned API-definition i Json-format [#9987]</span><span class="sxs-lookup"><span data-stu-id="a850c-1021">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="a850c-1022">”Import-AzApiManagementApi” Stöd har lagts till för att importera OpenApi 3.0-definition från Json-dokument</span><span class="sxs-lookup"><span data-stu-id="a850c-1022">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="a850c-1023">”New-AzApiManagementIdentityProvider” och ”Set-AzApiManagementIdentityProvider” Stöd har lagts till för att konfigurera ”Signin Tenant” för AAD B2C-provider [#9784]</span><span class="sxs-lookup"><span data-stu-id="a850c-1023">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a850c-1024">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a850c-1024">Az.DataLakeStore</span></span>
* <span data-ttu-id="a850c-1025">En referens har uttryckligen lagts till för System.Buffers i csproj och psd1.</span><span class="sxs-lookup"><span data-stu-id="a850c-1025">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a850c-1026">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a850c-1026">Az.IotHub</span></span>
* <span data-ttu-id="a850c-1027">Lade till stöd för att hantera enheter i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="a850c-1027">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="a850c-1028">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="a850c-1028">New Cmdlets are:</span></span>
    - <span data-ttu-id="a850c-1029">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="a850c-1029">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="a850c-1030">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="a850c-1030">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="a850c-1031">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="a850c-1031">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="a850c-1032">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="a850c-1032">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="a850c-1033">Stöd har lagts till för att hantera moduler på en mål-IoT-enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="a850c-1033">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="a850c-1034">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="a850c-1034">New Cmdlets are:</span></span>
    - <span data-ttu-id="a850c-1035">”Add-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="a850c-1035">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="a850c-1036">”Get-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="a850c-1036">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="a850c-1037">”Remove-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="a850c-1037">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="a850c-1038">”Set-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="a850c-1038">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="a850c-1039">Cmdlet har lagts till för att hämta anslutningssträngen för en mål-IoT-enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="a850c-1039">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="a850c-1040">Cmdlet har lagts till för att hämta anslutningssträngen för en modul på en mål-IoT-enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="a850c-1040">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="a850c-1041">Stöd har lagts till för att hämta/ange en överordnad enhet för en IoT-enhet.</span><span class="sxs-lookup"><span data-stu-id="a850c-1041">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="a850c-1042">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="a850c-1042">New Cmdlets are:</span></span>
    - <span data-ttu-id="a850c-1043">”Get-AzIotHubDeviceParent”</span><span class="sxs-lookup"><span data-stu-id="a850c-1043">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="a850c-1044">”Set-AzIotHubDeviceParent”</span><span class="sxs-lookup"><span data-stu-id="a850c-1044">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="a850c-1045">Stöd har lagts till för att hantera en enhets överordnade och underordnade relationer.</span><span class="sxs-lookup"><span data-stu-id="a850c-1045">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a850c-1046">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a850c-1046">Az.Monitor</span></span>
* <span data-ttu-id="a850c-1047">Utdatavärdet har åtgärdats för ”Get-AzMetricDefinition” [#9714]</span><span class="sxs-lookup"><span data-stu-id="a850c-1047">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a850c-1048">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a850c-1048">Az.Network</span></span>
* <span data-ttu-id="a850c-1049">SQL Management SDK har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="a850c-1049">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="a850c-1050">Ett problem har åtgärdats med namngivningsskillnader i klassen PrivateLinkServiceConnectionState.</span><span class="sxs-lookup"><span data-stu-id="a850c-1050">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="a850c-1051">Fältet ActionsRequired mappar till ActionRequired.</span><span class="sxs-lookup"><span data-stu-id="a850c-1051">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="a850c-1052">PublicNetworkAccess har lagts till i ”New-AzSqlServer” och ”Set-AzSqlServer”</span><span class="sxs-lookup"><span data-stu-id="a850c-1052">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="a850c-1053">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a850c-1053">Az.Resources</span></span>
* <span data-ttu-id="a850c-1054">Null-referensfel har åtgärdats i ”Get-AzRoleAssignment”</span><span class="sxs-lookup"><span data-stu-id="a850c-1054">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="a850c-1055">Växlarna ”-Force” och ”-PassThru” är valfria i ”Remove-AzADGroup” [#10849]</span><span class="sxs-lookup"><span data-stu-id="a850c-1055">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="a850c-1056">Ett problem har åtgärdats som gjorde att ”MailNickname” inte returnerades i ”Remove-AzADGroup” [#11167]</span><span class="sxs-lookup"><span data-stu-id="a850c-1056">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="a850c-1057">Ett problem har åtgärdats som gjorde att pipe-åtgärden ”Remove-AzADGroup” inte fungerar [#11171]</span><span class="sxs-lookup"><span data-stu-id="a850c-1057">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="a850c-1058">Ett null-referensfel har åtgärdats i GetAzureRoleAssignmentCommand</span><span class="sxs-lookup"><span data-stu-id="a850c-1058">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="a850c-1059">Attribut för icke-bakåtkompatibla ändringar har lagts till för kommande ändringar i cmdlets för principer</span><span class="sxs-lookup"><span data-stu-id="a850c-1059">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="a850c-1060">”Get-AzResourceGroup” har uppdaterats för att utföra taggfiltrering för resursgrupper på serversidan</span><span class="sxs-lookup"><span data-stu-id="a850c-1060">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="a850c-1061">Utökade Tag-cmdlets stöder -ResourceId</span><span class="sxs-lookup"><span data-stu-id="a850c-1061">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="a850c-1062">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="a850c-1062">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="a850c-1063">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="a850c-1063">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="a850c-1064">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="a850c-1064">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="a850c-1065">Ny Tag-cmdlet har lagts till</span><span class="sxs-lookup"><span data-stu-id="a850c-1065">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="a850c-1066">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="a850c-1066">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="a850c-1067">Flyttade ScopedDeployment från SDK 3.3.0</span><span class="sxs-lookup"><span data-stu-id="a850c-1067">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="a850c-1068">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a850c-1068">Az.Sql</span></span>
* <span data-ttu-id="a850c-1069">PublicNetworkAccess har lagts till i ”New-AzSqlServer” och ”Set-AzSqlServer”</span><span class="sxs-lookup"><span data-stu-id="a850c-1069">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="a850c-1070">Stöd har lagts till för konfiguration av säkerhetskopiering för långsiktig kvarhållning för hanterade databaser</span><span class="sxs-lookup"><span data-stu-id="a850c-1070">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="a850c-1071">Hämta/ange LTR-princip på en hanterad databas</span><span class="sxs-lookup"><span data-stu-id="a850c-1071">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="a850c-1072">Hämta LTR-säkerhetskopior efter hanterad databas, hanterad instans eller plats</span><span class="sxs-lookup"><span data-stu-id="a850c-1072">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="a850c-1073">Ta bort en LTR-säkerhetskopia</span><span class="sxs-lookup"><span data-stu-id="a850c-1073">Remove an LTR backup</span></span>
    - <span data-ttu-id="a850c-1074">Återställa en LTR-säkerhetskopia för att skapa en ny hanterad databas</span><span class="sxs-lookup"><span data-stu-id="a850c-1074">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="a850c-1075">MinimalTlsVersion har lagts till för New-AzSqlServer och Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="a850c-1075">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="a850c-1076">MinimalTlsVersion har lagts till för New-AzSqlInstance och Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="a850c-1076">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="a850c-1077">SQL SDK-versionen för Az.Network har ändrats</span><span class="sxs-lookup"><span data-stu-id="a850c-1077">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a850c-1078">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a850c-1078">Az.Storage</span></span>
* <span data-ttu-id="a850c-1079">AllowProtectedAppendWrite stöds i ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="a850c-1079">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="a850c-1080">”Set-AzRmStorageContainerImmutabilityPolicy”</span><span class="sxs-lookup"><span data-stu-id="a850c-1080">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="a850c-1081">Varningsmeddelande har lagts till om icke-bakåtkompatibel ändring för ändring av typen AzureStorageTable i en senare version</span><span class="sxs-lookup"><span data-stu-id="a850c-1081">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="a850c-1082">”New-AzStorageTable”</span><span class="sxs-lookup"><span data-stu-id="a850c-1082">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="a850c-1083">”Get-AzStorageTable”</span><span class="sxs-lookup"><span data-stu-id="a850c-1083">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a850c-1084">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a850c-1084">Az.Websites</span></span>
* <span data-ttu-id="a850c-1085">Tag-parametern har lagts till för ”New-AzAppServicePlan” och ”Set-AzAppServicePlan”</span><span class="sxs-lookup"><span data-stu-id="a850c-1085">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="a850c-1086">Stoppa cmdlet-körning om ett undantag uppstår när en anpassad domän läggs till på en webbplats</span><span class="sxs-lookup"><span data-stu-id="a850c-1086">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="a850c-1087">Stöd har lagts till för att utföra åtgärder för App Services som inte tillhör samma resursgrupp som App Services-planen</span><span class="sxs-lookup"><span data-stu-id="a850c-1087">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="a850c-1088">Åtkomstbegränsning har tillämpats på WebApp/Function i olika resursgrupper</span><span class="sxs-lookup"><span data-stu-id="a850c-1088">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="a850c-1089">Ett problem har åtgärdats för att ange anpassade värdnamn för WebAppSlots</span><span class="sxs-lookup"><span data-stu-id="a850c-1089">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="a850c-1090">3.5.0 – februari 2020</span><span class="sxs-lookup"><span data-stu-id="a850c-1090">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="a850c-1091">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="a850c-1091">Highlights since the last major release</span></span>
* <span data-ttu-id="a850c-1092">Uppdaterade telemetri på klientsidan.</span><span class="sxs-lookup"><span data-stu-id="a850c-1092">Updated client side telemetry.</span></span>
* <span data-ttu-id="a850c-1093">Az.IotHub lade till cmdletar som stöd för att hantera enheter.</span><span class="sxs-lookup"><span data-stu-id="a850c-1093">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="a850c-1094">Az.SqlVirtualMachine lade till cmdletar för lyssningsfunktion för tillgänglighetsgrupp.</span><span class="sxs-lookup"><span data-stu-id="a850c-1094">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="a850c-1095">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a850c-1095">Az.Accounts</span></span>
* <span data-ttu-id="a850c-1096">Lade till SubscriptionId, TenantId och körningstid i data för telemetri på klientsidan</span><span class="sxs-lookup"><span data-stu-id="a850c-1096">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a850c-1097">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a850c-1097">Az.Automation</span></span>
* <span data-ttu-id="a850c-1098">Åtgärdade skrivfel i exempel 1 i referensdokumentation för ”New-AzAutomationSoftwareUpdateConfiguration”</span><span class="sxs-lookup"><span data-stu-id="a850c-1098">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="a850c-1099">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a850c-1099">Az.CognitiveServices</span></span>
* <span data-ttu-id="a850c-1100">Uppdaterade SDK till 7.0</span><span class="sxs-lookup"><span data-stu-id="a850c-1100">Updated SDK to 7.0</span></span>
* <span data-ttu-id="a850c-1101">Förbättrade felmeddelande vid serversvar om tom brödtext</span><span class="sxs-lookup"><span data-stu-id="a850c-1101">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a850c-1102">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a850c-1102">Az.Compute</span></span>
* <span data-ttu-id="a850c-1103">Tillät tomt värde för ProximityPlacementGroupId under uppdatering</span><span class="sxs-lookup"><span data-stu-id="a850c-1103">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="a850c-1104">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="a850c-1104">Az.FrontDoor</span></span>
* <span data-ttu-id="a850c-1105">Lade till cmdlet för att hämta hanterade regeldefinitioner som kan användas i WAF</span><span class="sxs-lookup"><span data-stu-id="a850c-1105">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a850c-1106">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a850c-1106">Az.IotHub</span></span>
* <span data-ttu-id="a850c-1107">Lade till stöd för att hantera enheter i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="a850c-1107">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="a850c-1108">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="a850c-1108">New Cmdlets are:</span></span>
    - <span data-ttu-id="a850c-1109">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="a850c-1109">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="a850c-1110">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="a850c-1110">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="a850c-1111">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="a850c-1111">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="a850c-1112">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="a850c-1112">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a850c-1113">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a850c-1113">Az.KeyVault</span></span>
* <span data-ttu-id="a850c-1114">Åtgärdade duplicerad text för Add-AzKeyVaultKey.md</span><span class="sxs-lookup"><span data-stu-id="a850c-1114">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a850c-1115">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a850c-1115">Az.Monitor</span></span>
* <span data-ttu-id="a850c-1116">Åtgärdade beskrivning av cmdleten Get-AzLog.</span><span class="sxs-lookup"><span data-stu-id="a850c-1116">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="a850c-1117">En ny parameter med namnet ActionGroupId har lagts till i kommandot ”New-AzMetricAlertRuleV2”.</span><span class="sxs-lookup"><span data-stu-id="a850c-1117">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="a850c-1118">Användaren kan ange ActionGroupId(string) eller ActionGroup(ActivityLogAlertActionGroup).</span><span class="sxs-lookup"><span data-stu-id="a850c-1118">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a850c-1119">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a850c-1119">Az.Network</span></span>
* <span data-ttu-id="a850c-1120">Lade till en extra parameteranteckning för parametern ”-EnableProxyProtocol” för cmdleten ”New-AzPrivateLinkService”.</span><span class="sxs-lookup"><span data-stu-id="a850c-1120">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="a850c-1121">Åtgärdade FilterData-exempel i Start-AzVirtualNetworkGatewayConnectionPacketCapture.md och Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="a850c-1121">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="a850c-1122">Lade till paketinsamlingsexempel för att samla in alla inre och yttre paket i Start-AzVirtualNetworkGatewayConnectionPacketCapture.md och Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="a850c-1122">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="a850c-1123">Lade till stöd för Azure-brandväggsprincip på VNet-brandväggar</span><span class="sxs-lookup"><span data-stu-id="a850c-1123">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="a850c-1124">Inga nya cmdletar har lagts till.</span><span class="sxs-lookup"><span data-stu-id="a850c-1124">No new cmdlets are added.</span></span> <span data-ttu-id="a850c-1125">Lättar begränsningen för brandväggsprincip på VNet-brandväggar</span><span class="sxs-lookup"><span data-stu-id="a850c-1125">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a850c-1126">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a850c-1126">Az.RecoveryServices</span></span>
* <span data-ttu-id="a850c-1127">Lade till stöd för Restore-as-files för SQL-databaser.</span><span class="sxs-lookup"><span data-stu-id="a850c-1127">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a850c-1128">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a850c-1128">Az.Resources</span></span>
* <span data-ttu-id="a850c-1129">Omstrukturerade cmdletar för malldistribution</span><span class="sxs-lookup"><span data-stu-id="a850c-1129">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="a850c-1130">Lade till nya cmdletar för att hantera distributioner i hanteringsgruppen: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a850c-1130">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="a850c-1131">Lade till nya cmdletar för att hantera distributioner i klientorganisationsområdet: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="a850c-1131">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="a850c-1132">Omstrukturerade \*-AzDeployment-cmdletar för att fungera specifikt i prenumerationsomfattningen</span><span class="sxs-lookup"><span data-stu-id="a850c-1132">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="a850c-1133">Skapade alias \*-AzSubscriptionDeployment för \*-AzDeployment-cmdletar</span><span class="sxs-lookup"><span data-stu-id="a850c-1133">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="a850c-1134">Åtgärdade ”Update-AzADApplication” när parametern ”AvailableToOtherTenants” inte har angetts</span><span class="sxs-lookup"><span data-stu-id="a850c-1134">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="a850c-1135">Tog bort ApplicationObjectWithoutCredentialParameterSet för att undvika AmbiguousParameterSetException.</span><span class="sxs-lookup"><span data-stu-id="a850c-1135">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="a850c-1136">Återskapade hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="a850c-1136">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="a850c-1137">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a850c-1137">Az.Sql</span></span>
* <span data-ttu-id="a850c-1138">Lade till stöd för återställning till tidpunkt mellan prenumerationer på hanterade instanser.</span><span class="sxs-lookup"><span data-stu-id="a850c-1138">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="a850c-1139">Lade till stöd för att ändra befintlig SQL Managed Instance-maskinvarugenerering</span><span class="sxs-lookup"><span data-stu-id="a850c-1139">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="a850c-1140">Åtgärdade ”Update-AzSqlServerVulnerabilityAssessmentSetting”-hjälpexempel: parameter/egenskapsutdata - EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="a850c-1140">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="a850c-1141">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="a850c-1141">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="a850c-1142">Lade till cmdletar för lyssningsfunktion för tillgänglighetsgrupp</span><span class="sxs-lookup"><span data-stu-id="a850c-1142">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="a850c-1143">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="a850c-1143">Az.StorageSync</span></span>
* <span data-ttu-id="a850c-1144">Uppdaterade teckenuppsättningar som stöds i ”Invoke-AzStorageSyncCompatibilityCheck”.</span><span class="sxs-lookup"><span data-stu-id="a850c-1144">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="a850c-1145">3.4.0 – februari 2020</span><span class="sxs-lookup"><span data-stu-id="a850c-1145">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="a850c-1146">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="a850c-1146">Highlights since the last major release</span></span>
* <span data-ttu-id="a850c-1147">Första Az.CosmosDB-versionen 0.1.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="a850c-1147">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="a850c-1148">Stöd för Az.Network ConnectionMonitor V2 har lagts till</span><span class="sxs-lookup"><span data-stu-id="a850c-1148">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="a850c-1149">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a850c-1149">Az.Accounts</span></span>
* <span data-ttu-id="a850c-1150">Inaktivera automatisk sparande av kontext när AzureRmContext.json inte är tillgängligt</span><span class="sxs-lookup"><span data-stu-id="a850c-1150">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="a850c-1151">Uppdatera referensen till Azure Powershell Common till 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="a850c-1151">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="a850c-1152">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a850c-1152">Az.ApiManagement</span></span>
* <span data-ttu-id="a850c-1153">**Get-AzApiManagementApiSchema** Hämtning av Open-Api-schema som är associerat med ett API har åtgärdats   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="a850c-1153">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="a850c-1154">**New-AzApiManagementProduct**\* och **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="a850c-1154">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="a850c-1155">Åtgärda dokumentation för https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="a850c-1155">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="a850c-1156">**Set-AzApiManagementApi** Exempel för att visa hur ServiceUrl uppdateras med hjälp av cmdleten har lagts till</span><span class="sxs-lookup"><span data-stu-id="a850c-1156">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a850c-1157">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a850c-1157">Az.Compute</span></span>
* <span data-ttu-id="a850c-1158">Begränsa antalet VM-status till 100 för att undvika begränsning när Get-AzVM -Status utförs utan VM-namn.</span><span class="sxs-lookup"><span data-stu-id="a850c-1158">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="a850c-1159">Lägg till cmdleten Update-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="a850c-1159">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="a850c-1160">Lägg till parametrarna EncryptionType och DiskEncryptionSetId i följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="a850c-1160">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="a850c-1161">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="a850c-1161">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="a850c-1162">Lägg till parametern ColocationStatus för cmdleten Get-AzProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="a850c-1162">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a850c-1163">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a850c-1163">Az.DataFactory</span></span>
* <span data-ttu-id="a850c-1164">Uppdatera ADF .Net SDK-versionen till 4.7.0</span><span class="sxs-lookup"><span data-stu-id="a850c-1164">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="a850c-1165">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="a850c-1165">Az.DeploymentManager</span></span>
* <span data-ttu-id="a850c-1166">Lägger till LIST-åtgärder för resurser</span><span class="sxs-lookup"><span data-stu-id="a850c-1166">Adds LIST operations for resources</span></span>
* <span data-ttu-id="a850c-1167">Lägger till funktion för att utföra åtgärder för hälsokontrollsteg</span><span class="sxs-lookup"><span data-stu-id="a850c-1167">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="a850c-1168">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a850c-1168">Az.HDInsight</span></span>
* <span data-ttu-id="a850c-1169">Åtgärda dokumentfel för New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="a850c-1169">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a850c-1170">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a850c-1170">Az.KeyVault</span></span>
* <span data-ttu-id="a850c-1171">Lägg till Name-alias för attributet VaultName så att Remove-AzureKeyVault stämmer överens med New-AzureKeyVault.</span><span class="sxs-lookup"><span data-stu-id="a850c-1171">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a850c-1172">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a850c-1172">Az.Network</span></span>
* <span data-ttu-id="a850c-1173">Nytt exempel har lagts till i Set-AzNetworkWatcherConfigFlowLog.md för att demonstrera ett inaktiveringsscenario för Trafikanalys.</span><span class="sxs-lookup"><span data-stu-id="a850c-1173">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="a850c-1174">Lägg till stöd för att tilldela konfiguration av hanterings-IP till Azure Firewall – ett dedikerat undernät och en offentlig IP som brandväggen använder för dess hanteringstrafik</span><span class="sxs-lookup"><span data-stu-id="a850c-1174">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="a850c-1175">Cmdleten New-AzFirewall har uppdaterats:</span><span class="sxs-lookup"><span data-stu-id="a850c-1175">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="a850c-1176">Parametern -ManagementPublicIpAddress (inte obligatorisk) som accepterar ett offentligt IP-adressobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="a850c-1176">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="a850c-1177">Metoden SetManagementIpConfiguration har lagts till för brandväggsobjekt – kräver ett undernät och en offentlig IP-adress som indata – undernätets namn måste vara ”AzureFirewallManagementSubnet”</span><span class="sxs-lookup"><span data-stu-id="a850c-1177">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="a850c-1178">Exempel för Get-AzNetworkSecurityGroup har korrigerats så att exempel visas för NSG:er i stället för nätverksgränssnitt.</span><span class="sxs-lookup"><span data-stu-id="a850c-1178">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="a850c-1179">Ett skrivfel har åtgärdats i kommandot New-AzVpnSite som hindrade kompletteraren för resurs-ID från att fylla i en parameter.</span><span class="sxs-lookup"><span data-stu-id="a850c-1179">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="a850c-1180">Stöd för Url-konfiguration i åtgärdsuppsättningen för omskrivningsregler i Application Gateway har lagts till</span><span class="sxs-lookup"><span data-stu-id="a850c-1180">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="a850c-1181">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="a850c-1181">New cmdlets added:</span></span>
        - <span data-ttu-id="a850c-1182">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="a850c-1182">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="a850c-1183">Cmdletar har uppdaterats med den valfria parametern -UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="a850c-1183">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="a850c-1184">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="a850c-1184">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="a850c-1185">Lägg till stöd för resurser för NetworkWatcher ConnectionMonitor version 2</span><span class="sxs-lookup"><span data-stu-id="a850c-1185">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="a850c-1186">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a850c-1186">Az.PolicyInsights</span></span>
* <span data-ttu-id="a850c-1187">Stöd för utvärdering av efterlevnad innan fastställande av vilken resurs som ska åtgärdas</span><span class="sxs-lookup"><span data-stu-id="a850c-1187">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="a850c-1188">Lägg till parametern ”-ResourceDiscoverMode” för Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="a850c-1188">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="a850c-1189">Lägg till cmdleten Get-AzPolicyMetadata för att hämta resurser för principmetadata</span><span class="sxs-lookup"><span data-stu-id="a850c-1189">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="a850c-1190">Get-AzPolicyState och Get-AzPolicyStateSummary för API-versionen 2019-10-01 har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="a850c-1190">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a850c-1191">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a850c-1191">Az.RecoveryServices</span></span>
* <span data-ttu-id="a850c-1192">Azure Site Recovery-stöd för att ta bort en replikerad disk.</span><span class="sxs-lookup"><span data-stu-id="a850c-1192">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="a850c-1193">Tillagt Azure Backup-stöd för att lägga till taggar när ett Recovery Services-valv skapas.</span><span class="sxs-lookup"><span data-stu-id="a850c-1193">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a850c-1194">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a850c-1194">Az.Resources</span></span>
* <span data-ttu-id="a850c-1195">Gör -Scope valfritt i cmdletarna \*-AzPolicyAssignment med standardinställning till kontextprenumeration</span><span class="sxs-lookup"><span data-stu-id="a850c-1195">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="a850c-1196">Lägg till exempel på att skapa ADServicePrincipal med lösenord och nyckelautentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="a850c-1196">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="a850c-1197">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a850c-1197">Az.Sql</span></span>
<span data-ttu-id="a850c-1198">Åtgärda cmdleten New-AzSqlDatabaseSecondary så att existensen PartnerDatabaseName kontrolleras i stället för existensen DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="a850c-1198">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a850c-1199">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a850c-1199">Az.Storage</span></span>
* <span data-ttu-id="a850c-1200">Stöd för angivning av krypteringsnyckeltyp för Tabell/kö i Skapa lagringskonto</span><span class="sxs-lookup"><span data-stu-id="a850c-1200">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="a850c-1201">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a850c-1201">New-AzStorageAccount</span></span>
* <span data-ttu-id="a850c-1202">Visa RequestId när StorageException inte har ExtendedErrorInformation</span><span class="sxs-lookup"><span data-stu-id="a850c-1202">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="a850c-1203">Åtgärda exempel 6 för cmdleten Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="a850c-1203">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a850c-1204">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a850c-1204">Az.Websites</span></span>
* <span data-ttu-id="a850c-1205">Set-AzWebapp och Set-AzWebappSlot stöder egenskaperna AlwaysOn, MinTls och FtpsState</span><span class="sxs-lookup"><span data-stu-id="a850c-1205">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="a850c-1206">Åtgärdar problemet där inställning av HttpsOnly samtidigt som AppservicePlan ändrades med det enskilda kommandot Set-AzWebApp återställde HttpsOnly till standardvärdet</span><span class="sxs-lookup"><span data-stu-id="a850c-1206">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="a850c-1207">3.3.0 – januari 2020</span><span class="sxs-lookup"><span data-stu-id="a850c-1207">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a850c-1208">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a850c-1208">Az.Accounts</span></span>
* <span data-ttu-id="a850c-1209">Nu stöder Add-AzEnvironment och Set-AzEnvironment parametrarna AzureAttestationServiceEndpointResourceId och AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="a850c-1209">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="a850c-1210">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="a850c-1210">Az.Cdn</span></span>
* <span data-ttu-id="a850c-1211">Information om felsvar visas i New-AzCdnEndpoint-cmdleten</span><span class="sxs-lookup"><span data-stu-id="a850c-1211">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a850c-1212">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a850c-1212">Az.Compute</span></span>
* <span data-ttu-id="a850c-1213">Set-AzVMCustomScriptExtension-cmdleten har åtgärdats för en virtuell dator med hanterad OD-disk som inte har någon operativsystemprofil.</span><span class="sxs-lookup"><span data-stu-id="a850c-1213">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="a850c-1214">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="a850c-1214">Az.ContainerInstance</span></span>
* <span data-ttu-id="a850c-1215">Parameternamn som används med New-AzContainerGroup-exempel har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="a850c-1215">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="a850c-1216">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="a850c-1216">Az.DataBoxEdge</span></span>
* <span data-ttu-id="a850c-1217">Cmdleten ”Get-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="a850c-1217">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="a850c-1218">Hämta gränslagringscontainern</span><span class="sxs-lookup"><span data-stu-id="a850c-1218">Get the Edge Storage Container</span></span>
* <span data-ttu-id="a850c-1219">Cmdleten ”New-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="a850c-1219">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="a850c-1220">Skapa en ny gränslagringscontainer</span><span class="sxs-lookup"><span data-stu-id="a850c-1220">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="a850c-1221">Cmdleten ”Remove-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="a850c-1221">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="a850c-1222">Ta bort gränslagringscontainern</span><span class="sxs-lookup"><span data-stu-id="a850c-1222">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="a850c-1223">Cmdleten ”Invoke-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="a850c-1223">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="a850c-1224">Anropa åtgärd för att uppdatera data i gränslagringscontainer</span><span class="sxs-lookup"><span data-stu-id="a850c-1224">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="a850c-1225">Cmdleten ”Get-AzDataBoxEdgeStorageAccount” har lagts till</span><span class="sxs-lookup"><span data-stu-id="a850c-1225">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="a850c-1226">Hämta gränslagringskontot</span><span class="sxs-lookup"><span data-stu-id="a850c-1226">Get the Edge Storage Account</span></span>
* <span data-ttu-id="a850c-1227">Cmdleten ”New-AzDataBoxEdgeStorageAccount” har lagts till</span><span class="sxs-lookup"><span data-stu-id="a850c-1227">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="a850c-1228">Skapa ett nytt gränslagringskonto</span><span class="sxs-lookup"><span data-stu-id="a850c-1228">Create new Edge Storage Account</span></span>
* <span data-ttu-id="a850c-1229">Cmdleten ”Remove-AzDataBoxEdgeStorageAccount” har lagts till</span><span class="sxs-lookup"><span data-stu-id="a850c-1229">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="a850c-1230">Ta bort gränslagringskontot</span><span class="sxs-lookup"><span data-stu-id="a850c-1230">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="a850c-1231">Anropa cmdleten ”Invoke-AzDataBoxEdgeShare”</span><span class="sxs-lookup"><span data-stu-id="a850c-1231">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="a850c-1232">Anropa åtgärd för att uppdatera resursdata</span><span class="sxs-lookup"><span data-stu-id="a850c-1232">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="a850c-1233">Cmdleten ”Set-AzDataBoxEdgeStorageAccountCredential” har lagts till</span><span class="sxs-lookup"><span data-stu-id="a850c-1233">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="a850c-1234">Ange autentiseringsuppgifter för az databoxedge-lagringskonto</span><span class="sxs-lookup"><span data-stu-id="a850c-1234">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a850c-1235">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a850c-1235">Az.DataFactory</span></span>
* <span data-ttu-id="a850c-1236">Lägg till AutoUpdateETA-, LatestVersion-, PushedVersion-, TaskQueueId- och VersionStatus-egenskaper för Get-AzDataFactoryV2IntegrationRuntime-cmd</span><span class="sxs-lookup"><span data-stu-id="a850c-1236">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="a850c-1237">Uppdatera ADF .Net SDK-versionen till 4.6.0</span><span class="sxs-lookup"><span data-stu-id="a850c-1237">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="a850c-1238">Lägg till parametern ”PublicIPs” för ”Set-AzureRmDataFactoryV2IntegrationRuntime”-cmd så att Azure-SSIS IR kan skapas med statiska offentliga IP-adresser.</span><span class="sxs-lookup"><span data-stu-id="a850c-1238">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="a850c-1239">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="a850c-1239">Az.DevTestLabs</span></span>
* <span data-ttu-id="a850c-1240">Ta bort den brutna länken i Get-AzDtlAllowedVMSizesPolicy.md</span><span class="sxs-lookup"><span data-stu-id="a850c-1240">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="a850c-1241">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a850c-1241">Az.EventHub</span></span>
* <span data-ttu-id="a850c-1242">Korrigering av problem 10634: Åtgärda referensen till null-objekt för eventhubnamespace-borttagning</span><span class="sxs-lookup"><span data-stu-id="a850c-1242">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="a850c-1243">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a850c-1243">Az.HDInsight</span></span>
* <span data-ttu-id="a850c-1244">Åtgärda Invoke-AzHDInsightHiveJob.md-fel.</span><span class="sxs-lookup"><span data-stu-id="a850c-1244">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="a850c-1245">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="a850c-1245">Az.MachineLearning</span></span>
* <span data-ttu-id="a850c-1246">Nedanstående cmdletar har tagits bort eftersom MachineLearningCompute inte längre är tillgängligt</span><span class="sxs-lookup"><span data-stu-id="a850c-1246">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="a850c-1247">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="a850c-1247">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="a850c-1248">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="a850c-1248">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="a850c-1249">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="a850c-1249">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="a850c-1250">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="a850c-1250">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="a850c-1251">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="a850c-1251">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="a850c-1252">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="a850c-1252">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="a850c-1253">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="a850c-1253">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a850c-1254">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a850c-1254">Az.Network</span></span>
* <span data-ttu-id="a850c-1255">Uppgradera beroende av Microsoft.Azure.Management.Sql från 1.36-preview till 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="a850c-1255">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a850c-1256">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a850c-1256">Az.RecoveryServices</span></span>
* <span data-ttu-id="a850c-1257">Ändrat Azure Site Recovery-stöd för krypterade vilande data på virtuella datorer med hanterade diskar med kundhanterade nycklar för Azure till Azure-providern.</span><span class="sxs-lookup"><span data-stu-id="a850c-1257">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="a850c-1258">Azure Site Recovery-stöd för att ange ID för diskkrypteringsuppsättning som valfri inmatning för aktivering av skydd för VMware till Azure.</span><span class="sxs-lookup"><span data-stu-id="a850c-1258">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="a850c-1259">Azure Site Recovery-stöd för att ange ID för diskkrypteringsuppsättning som valfri inmatning på disknivå för aktivering av skydd för VMware till Azure.</span><span class="sxs-lookup"><span data-stu-id="a850c-1259">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="a850c-1260">Azure Site Recovery-stöd för att uppdatera replikeringsskyddade objekt med mappning för diskkrypteringsuppsättning för HyperV till Azure.</span><span class="sxs-lookup"><span data-stu-id="a850c-1260">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a850c-1261">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a850c-1261">Az.Resources</span></span>
* <span data-ttu-id="a850c-1262">Åtgärda ett fel i hjälpdokument för ”Remove-AzTag”.</span><span class="sxs-lookup"><span data-stu-id="a850c-1262">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="a850c-1263">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a850c-1263">Az.Sql</span></span>
* <span data-ttu-id="a850c-1264">Åtgärda funktioner i cmdletar för att ange baslinjen för sårbarhetsbedömning för arbete med huvuddatabasen för Azure-databasen och begränsa den för systemdatabaser på hanterade instanser.</span><span class="sxs-lookup"><span data-stu-id="a850c-1264">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="a850c-1265">Åtgärda ett fel när en redundansgrupp för en SQL-instans skapas</span><span class="sxs-lookup"><span data-stu-id="a850c-1265">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="a850c-1266">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="a850c-1266">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="a850c-1267">Lägg till DR som en ny giltig licenstyp</span><span class="sxs-lookup"><span data-stu-id="a850c-1267">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a850c-1268">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a850c-1268">Az.Storage</span></span>
* <span data-ttu-id="a850c-1269">Lägg till varningsmeddelande om icke-bakåtkompatibel ändring för DefaultAction-värdeändring i en framtida version</span><span class="sxs-lookup"><span data-stu-id="a850c-1269">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="a850c-1270">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="a850c-1270">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="a850c-1271">Stöd för att hämta lagringskontots senaste synkroniseringstid genom att köra get-AzureRMStorageAccount med parametern -IncludeGeoReplicationStats</span><span class="sxs-lookup"><span data-stu-id="a850c-1271">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="a850c-1272">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a850c-1272">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="a850c-1273">3.2.0 – December 2019</span><span class="sxs-lookup"><span data-stu-id="a850c-1273">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="a850c-1274">Allmänt</span><span class="sxs-lookup"><span data-stu-id="a850c-1274">General</span></span>
* <span data-ttu-id="a850c-1275">Uppdatera referenser i .psd1 för att använda relativa sökvägar för alla moduler</span><span class="sxs-lookup"><span data-stu-id="a850c-1275">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="a850c-1276">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a850c-1276">Az.Accounts</span></span>
* <span data-ttu-id="a850c-1277">Ange rätt UserAgent för telemetri på klientsidan för Az 4.0 preview</span><span class="sxs-lookup"><span data-stu-id="a850c-1277">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="a850c-1278">Visa användarvänligt felmeddelande när kontexten är null i Az 4.0 preview</span><span class="sxs-lookup"><span data-stu-id="a850c-1278">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="a850c-1279">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="a850c-1279">Az.Batch</span></span>
* <span data-ttu-id="a850c-1280">Korrigera problem [#10602](https://github.com/Azure/azure-powershell/issues/10602), där **New-AzBatchPool** skickade VirtualMachineConfiguration.ContainerConfiguration eller VirtualMachineConfiguration.DataDisks på ett felaktigt sätt till servern.</span><span class="sxs-lookup"><span data-stu-id="a850c-1280">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a850c-1281">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a850c-1281">Az.DataFactory</span></span>
* <span data-ttu-id="a850c-1282">Uppdatera ADF .Net SDK-versionen till 4.5.0</span><span class="sxs-lookup"><span data-stu-id="a850c-1282">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="a850c-1283">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="a850c-1283">Az.FrontDoor</span></span>
* <span data-ttu-id="a850c-1284">Stöd har lagts till för undantag för hanterade regler för brandväggen för webbaserade program</span><span class="sxs-lookup"><span data-stu-id="a850c-1284">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="a850c-1285">Lägg till SocketAddr för automatisk komplettering</span><span class="sxs-lookup"><span data-stu-id="a850c-1285">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="a850c-1286">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="a850c-1286">Az.HealthcareApis</span></span>
* <span data-ttu-id="a850c-1287">Undantagshantering</span><span class="sxs-lookup"><span data-stu-id="a850c-1287">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a850c-1288">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a850c-1288">Az.KeyVault</span></span>
* <span data-ttu-id="a850c-1289">Åtgärdat fel vid åtkomst av värde som kanske inte har angetts</span><span class="sxs-lookup"><span data-stu-id="a850c-1289">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="a850c-1290">Hantering av ECC-certifikat (Elliptic Curve Cryptography)</span><span class="sxs-lookup"><span data-stu-id="a850c-1290">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="a850c-1291">Stöd har lagts till för att ange kurvan för certifikatprinciper</span><span class="sxs-lookup"><span data-stu-id="a850c-1291">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a850c-1292">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a850c-1292">Az.Monitor</span></span>
* <span data-ttu-id="a850c-1293">Lägger till valfritt argument i kommandot Lägg till diagnostikinställningar.</span><span class="sxs-lookup"><span data-stu-id="a850c-1293">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="a850c-1294">Ett växelargument som om det finns visar att exporten till Log Analytics måste ske till ett fast schema (kallas även</span><span class="sxs-lookup"><span data-stu-id="a850c-1294">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="a850c-1295">dedikerad, datatyp)</span><span class="sxs-lookup"><span data-stu-id="a850c-1295">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a850c-1296">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a850c-1296">Az.Network</span></span>
* <span data-ttu-id="a850c-1297">Stöd för IpGroups i program-, NAT- och nätverksregler för Azure Firewall.</span><span class="sxs-lookup"><span data-stu-id="a850c-1297">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a850c-1298">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a850c-1298">Az.Resources</span></span>
* <span data-ttu-id="a850c-1299">Åtgärda ett problem där malldistributionen inte kan läsa en mallparameter om dess namn står i konflikt med ett inbyggt parameternamn.</span><span class="sxs-lookup"><span data-stu-id="a850c-1299">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="a850c-1300">Uppdaterade princip-cmdletar för att använda den nya API-versionen 2019-09-01 som introducerar grupperingsstöd inom principuppsättningsdefinitioner.</span><span class="sxs-lookup"><span data-stu-id="a850c-1300">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="a850c-1301">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a850c-1301">Az.Sql</span></span>
* <span data-ttu-id="a850c-1302">Uppgraderad funktion för att skapa lagring i automatisk aktivering av sårbarhetsbedömning till StorageV2</span><span class="sxs-lookup"><span data-stu-id="a850c-1302">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a850c-1303">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a850c-1303">Az.Storage</span></span>
* <span data-ttu-id="a850c-1304">Stöd för generering av blob/container-identitetsbaserad SAS-token med lagringskontextbaserad på OAuth-autentisering</span><span class="sxs-lookup"><span data-stu-id="a850c-1304">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="a850c-1305">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="a850c-1305">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="a850c-1306">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="a850c-1306">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="a850c-1307">Stöd för återkallning av användardelegeringsnycklar för lagringskonto för att återkalla alla SAS-token</span><span class="sxs-lookup"><span data-stu-id="a850c-1307">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="a850c-1308">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="a850c-1308">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="a850c-1309">Uppgradera till Microsoft.Azure.Management.Storage 14.2.0 för att stödja den nya API-versionen 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="a850c-1309">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="a850c-1310">Stöd för QuotaGiB (resurskvot i Gibibye) för värden över 5120 i hanteringsplanet för cmdletar för filresurser och parameteraliaset. Quota har också lagts till för parametern ”QuotaGiB”.</span><span class="sxs-lookup"><span data-stu-id="a850c-1310">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="a850c-1311">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="a850c-1311">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="a850c-1312">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="a850c-1312">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="a850c-1313">Lägg till parameteraliaset QuotaGiB i parametern Quota</span><span class="sxs-lookup"><span data-stu-id="a850c-1313">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="a850c-1314">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="a850c-1314">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="a850c-1315">Åtgärda problemet att Set-AzStorageContainerAcl kan rensa den lagrade åtkomstprincipen</span><span class="sxs-lookup"><span data-stu-id="a850c-1315">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="a850c-1316">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="a850c-1316">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="a850c-1317">3.1.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="a850c-1317">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="a850c-1318">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="a850c-1318">Highlights since the last major release</span></span>
* <span data-ttu-id="a850c-1319">Az.DataBoxEdge 1.0.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="a850c-1319">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="a850c-1320">Az.SqlVirtualMachine 1.0.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="a850c-1320">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a850c-1321">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a850c-1321">Az.Compute</span></span>
* <span data-ttu-id="a850c-1322">Funktion för att använda en virtuell dator igen</span><span class="sxs-lookup"><span data-stu-id="a850c-1322">VM Reapply feature</span></span>
    - <span data-ttu-id="a850c-1323">Lägg till parameter för att använda igen till cmdleten Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="a850c-1323">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="a850c-1324">Funktionen AutomaticRepairs i VM-skalningsuppsättningar:</span><span class="sxs-lookup"><span data-stu-id="a850c-1324">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="a850c-1325">Lägg till parametrarna EnableAutomaticRepair, AutomaticRepairGracePeriod och AutomaticRepairMaxInstanceRepairsPercent till följande cmdletar:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a850c-1325">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="a850c-1326">Stöd för galleriavbildningar i flera klientorganisationer för New-AzVM</span><span class="sxs-lookup"><span data-stu-id="a850c-1326">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="a850c-1327">Lägg till "Spot" till argumentslutföraren i prioritetsparametern i cmdletarna New-AzVM, New-AzVMConfig och New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a850c-1327">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="a850c-1328">Lägg till parametrarna DiskIOPSReadWrite och DiskMBpsReadWrite till cmdleten Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="a850c-1328">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="a850c-1329">Ändra parametern SourceImageId för cmdleten New-AzGalleryImageVersion till valfri</span><span class="sxs-lookup"><span data-stu-id="a850c-1329">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="a850c-1330">Lägg till parametrarna OSDiskImage och DataDiskImage till cmdleten New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="a850c-1330">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="a850c-1331">Lägg till parametern HyperVGeneration till cmdleten New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="a850c-1331">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="a850c-1332">Lägg till parametern SkipExtensionsOnOverprovisionedVMs till cmdletarna New-AzVmss, New-AzVmssConfig och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a850c-1332">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="a850c-1333">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="a850c-1333">Az.DataBoxEdge</span></span>
* <span data-ttu-id="a850c-1334">Cmdleten `Get-AzDataBoxEdgeOrder` har lagts till</span><span class="sxs-lookup"><span data-stu-id="a850c-1334">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="a850c-1335">Hämta ordning</span><span class="sxs-lookup"><span data-stu-id="a850c-1335">Get the Order</span></span>
* <span data-ttu-id="a850c-1336">Cmdleten `New-AzDataBoxEdgeOrder` har lagts till</span><span class="sxs-lookup"><span data-stu-id="a850c-1336">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="a850c-1337">Skapa ny ordning</span><span class="sxs-lookup"><span data-stu-id="a850c-1337">Create new Order</span></span>
* <span data-ttu-id="a850c-1338">Cmdleten `Remove-AzDataBoxEdgeOrder` har lagts till</span><span class="sxs-lookup"><span data-stu-id="a850c-1338">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="a850c-1339">Ta bort ordning</span><span class="sxs-lookup"><span data-stu-id="a850c-1339">Remove the Order</span></span>
* <span data-ttu-id="a850c-1340">Cmdleten `New-AzDataBoxEdgeShare` har ändrats</span><span class="sxs-lookup"><span data-stu-id="a850c-1340">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="a850c-1341">Nu skapas lokal filresurs</span><span class="sxs-lookup"><span data-stu-id="a850c-1341">Now creates Local Share</span></span>
* <span data-ttu-id="a850c-1342">Cmdleten `Set-AzDataBoxEdgeRole` har lagts till</span><span class="sxs-lookup"><span data-stu-id="a850c-1342">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="a850c-1343">Nu kan IotRole mappas till filresursen</span><span class="sxs-lookup"><span data-stu-id="a850c-1343">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="a850c-1344">Cmdleten `Invoke-AzDataBoxEdgeDevice` har lagts till</span><span class="sxs-lookup"><span data-stu-id="a850c-1344">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="a850c-1345">Anropa genomsökningsuppdatering, ladda ned uppdatering, installera uppdateringar på enheten</span><span class="sxs-lookup"><span data-stu-id="a850c-1345">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="a850c-1346">Cmdleten `Get-AzDataBoxEdgeTrigger` har lagts till</span><span class="sxs-lookup"><span data-stu-id="a850c-1346">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="a850c-1347">Hämtar information om utlösare</span><span class="sxs-lookup"><span data-stu-id="a850c-1347">Gets the information about Triggers</span></span>
* <span data-ttu-id="a850c-1348">Cmdleten `New-AzDataBoxEdgeTrigger` har lagts till</span><span class="sxs-lookup"><span data-stu-id="a850c-1348">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="a850c-1349">Skapa nya utlösare</span><span class="sxs-lookup"><span data-stu-id="a850c-1349">Create new Triggers</span></span>
* <span data-ttu-id="a850c-1350">Cmdleten `Remove-AzDataBoxEdgeTrigger` har lagts till</span><span class="sxs-lookup"><span data-stu-id="a850c-1350">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="a850c-1351">Ta bort utlösare</span><span class="sxs-lookup"><span data-stu-id="a850c-1351">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a850c-1352">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a850c-1352">Az.DataFactory</span></span>
* <span data-ttu-id="a850c-1353">Uppdatera ADF .Net SDK-versionen till 4.4.0</span><span class="sxs-lookup"><span data-stu-id="a850c-1353">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="a850c-1354">Lägg till parametern ExpressCustomSetup för kommandot Set-AzureRmDataFactoryV2IntegrationRuntime för att aktivera installationskonfigurationer och komponenter från tredje part utan anpassat konfigurationsskript.</span><span class="sxs-lookup"><span data-stu-id="a850c-1354">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a850c-1355">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a850c-1355">Az.DataLakeStore</span></span>
* <span data-ttu-id="a850c-1356">Uppdatera dokumentation för Get-AzDataLakeStoreDeletedItem och Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="a850c-1356">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="a850c-1357">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a850c-1357">Az.EventHub</span></span>
* <span data-ttu-id="a850c-1358">Korrigering av problem #10301: Korrigera datumformat för SAS-token</span><span class="sxs-lookup"><span data-stu-id="a850c-1358">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="a850c-1359">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="a850c-1359">Az.FrontDoor</span></span>
* <span data-ttu-id="a850c-1360">Lägg till parametern MinimumTlsVersion till Enable-AzFrontDoorCustomDomainHttps och New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="a850c-1360">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="a850c-1361">Lägg till parametrarna HealthProbeMethod och EnabledState till New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="a850c-1361">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="a850c-1362">Lägg till en ny cmdlet för att skapa BackendPoolsSettings-objekt som passar i skapande/uppdatering av Front Door</span><span class="sxs-lookup"><span data-stu-id="a850c-1362">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="a850c-1363">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="a850c-1363">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a850c-1364">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a850c-1364">Az.Network</span></span>
* <span data-ttu-id="a850c-1365">Ändra alternativexemplen Start-AzVirtualNetworkGatewayConnectionPacketCapture.md och Start-AzVirtualnetworkGatewayPacketCapture.md för FilterData.</span><span class="sxs-lookup"><span data-stu-id="a850c-1365">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="a850c-1366">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="a850c-1366">Az.PrivateDns</span></span>
* <span data-ttu-id="a850c-1367">Uppdaterade PrivateDns .NET SDK till version 1.0.0</span><span class="sxs-lookup"><span data-stu-id="a850c-1367">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a850c-1368">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a850c-1368">Az.RecoveryServices</span></span>
* <span data-ttu-id="a850c-1369">Stöd för att välja disktyp vid aktivering av skydd i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="a850c-1369">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="a850c-1370">Korrigering av bugg för åtgärdsredigering av återställningsplan i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="a850c-1370">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="a850c-1371">Återställningsstöd för att godkänna filestream-databaser i Azure Backup SQL.</span><span class="sxs-lookup"><span data-stu-id="a850c-1371">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="a850c-1372">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="a850c-1372">Az.RedisCache</span></span>
* <span data-ttu-id="a850c-1373">Parametern MinimumTlsVersion har lagts till i cmdletarna New-AzRedisCache och Set-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="a850c-1373">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="a850c-1374">Dessutom har MinimumTlsVersion lagts till i utdata för cmdleten Get-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="a850c-1374">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="a850c-1375">Verifiering har lagts till på parametern -Size i cmdletarna Set-AzRedisCache och New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="a850c-1375">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="a850c-1376">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a850c-1376">Az.Resources</span></span>
- <span data-ttu-id="a850c-1377">Uppdaterade policy-cmdletar för att använda den nya API-versionen 2019-06-01 som har en ny EnforcementMode-egenskap i policytilldelningen.</span><span class="sxs-lookup"><span data-stu-id="a850c-1377">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="a850c-1378">Uppdaterade hjälpexempel för skapandet av policydefinition</span><span class="sxs-lookup"><span data-stu-id="a850c-1378">Updated create policy definition help example</span></span>
- <span data-ttu-id="a850c-1379">Åtgärda bugg i Remove-AZADServicePrincipal -ServicePrincipalName, utlös null-referens när tjänstens huvudnamn inte hittas.</span><span class="sxs-lookup"><span data-stu-id="a850c-1379">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="a850c-1380">Åtgärda bugg i New-AZADServicePrincipal, utlös null-referens när klientorganisationen inte har någon prenumeration.</span><span class="sxs-lookup"><span data-stu-id="a850c-1380">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="a850c-1381">Ändra New-AzAdServicePrincipal för att endast lägga till autentiseringsuppgifter för det associerade programmet.</span><span class="sxs-lookup"><span data-stu-id="a850c-1381">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="a850c-1382">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a850c-1382">Az.Sql</span></span>
* <span data-ttu-id="a850c-1383">Stöd har lagts till för databasen ReadReplicaCount.</span><span class="sxs-lookup"><span data-stu-id="a850c-1383">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="a850c-1384">Korrigerade Set-AzSqlDatabase när zonredundans inte har angetts</span><span class="sxs-lookup"><span data-stu-id="a850c-1384">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="a850c-1385">3.0.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="a850c-1385">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="a850c-1386">Allmänt</span><span class="sxs-lookup"><span data-stu-id="a850c-1386">General</span></span>
* <span data-ttu-id="a850c-1387">Az. PrivateDns 1.0.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="a850c-1387">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="a850c-1388">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a850c-1388">Az.Accounts</span></span>
* <span data-ttu-id="a850c-1389">Lägg till ett utfasningsmeddelande för aliaset Resolve-error.</span><span class="sxs-lookup"><span data-stu-id="a850c-1389">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="a850c-1390">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="a850c-1390">Az.Advisor</span></span>
* <span data-ttu-id="a850c-1391">Den nya kategorin Operational Excellence har lagts till i cmdleten Get-AzAdvisorRecommendation.</span><span class="sxs-lookup"><span data-stu-id="a850c-1391">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="a850c-1392">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="a850c-1392">Az.Batch</span></span>
* <span data-ttu-id="a850c-1393">`CoreQuota` på `BatchAccountContext` har bytt namn till `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="a850c-1393">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="a850c-1394">Det finns även en ny `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="a850c-1394">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="a850c-1395">Detta påverkar **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="a850c-1395">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="a850c-1396">**New-AzBatchTask** `-ResourceFile`-parametern tar nu en samling `PSResourceFile`-objekt som kan skapas med hjälp av den nya cmdleten **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="a850c-1396">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="a850c-1397">Ny **New-AzBatchResourceFile**-cmdlet för att skapa `PSResourceFile`-objekt.</span><span class="sxs-lookup"><span data-stu-id="a850c-1397">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="a850c-1398">Dessa kan tillhandahållas till **New-AzBatchTask** på `-ResourceFile`-parametern.</span><span class="sxs-lookup"><span data-stu-id="a850c-1398">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="a850c-1399">Detta stöder två nya typer av resursfiler förutom det befintliga sättet med `HttpUrl`:</span><span class="sxs-lookup"><span data-stu-id="a850c-1399">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="a850c-1400">`AutoStorageContainerName`-baserade resursfiler laddar ned en hel container för automatisk lagring till Batch-noden.</span><span class="sxs-lookup"><span data-stu-id="a850c-1400">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="a850c-1401">`StorageContainerUrl`-baserade resursfiler laddar ned containern som anges i webbadressen till Batch-noden.</span><span class="sxs-lookup"><span data-stu-id="a850c-1401">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="a850c-1402">Tog bort egenskapen `ApplicationPackages` för `PSApplication` som returnerades av **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="a850c-1402">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="a850c-1403">Specifika paket i ett program kan nu hämtas med hjälp av **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="a850c-1403">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="a850c-1404">Till exempel: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="a850c-1404">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="a850c-1405">Bytt namn på `ApplicationId` till `ApplicationName` på **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** och **Set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="a850c-1405">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="a850c-1406">`ApplicationId` är nu ett alias för `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="a850c-1406">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="a850c-1407">Ny `PSWindowsUserConfiguration`-egenskap till `PSUserAccount` lades till.</span><span class="sxs-lookup"><span data-stu-id="a850c-1407">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="a850c-1408">Bytte namn på `Version` till `Name` på `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="a850c-1408">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="a850c-1409">Bytte namn på `BlobSource` till `HttpUrl` på `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="a850c-1409">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="a850c-1410">Tog bort egenskapen `OSDisk` från `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="a850c-1410">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="a850c-1411">Tog bort **Set-AzBatchPoolOSVersion**.</span><span class="sxs-lookup"><span data-stu-id="a850c-1411">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="a850c-1412">Den här åtgärden stöds inte längre.</span><span class="sxs-lookup"><span data-stu-id="a850c-1412">This operation is no longer supported.</span></span>
* <span data-ttu-id="a850c-1413">`TargetOSVersion` har tagits bort från `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="a850c-1413">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="a850c-1414">Bytte namn på `CurrentOSVersion` till `OSVersion` på `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="a850c-1414">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="a850c-1415">`DataEgressGiB` och `DataIngressGiB` har tagits bort från `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="a850c-1415">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="a850c-1416">Tog bort **Get-AzBatchNodeAgentSku** och ersatte det med **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="a850c-1416">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="a850c-1417">**Get-AzBatchSupportedImage** returnerar samma data som **Get-AzBatchNodeAgentSku** men i ett mer användarvänligt format.</span><span class="sxs-lookup"><span data-stu-id="a850c-1417">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="a850c-1418">Nya icke-verifierade avbildningar returneras nu också.</span><span class="sxs-lookup"><span data-stu-id="a850c-1418">New non-verified images are also now returned.</span></span> <span data-ttu-id="a850c-1419">Ytterligare information om `Capabilities` och `BatchSupportEndOfLife` för varje avbildning inkluderas också.</span><span class="sxs-lookup"><span data-stu-id="a850c-1419">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="a850c-1420">Lade till möjlighet att montera fjärrfilsystem på varje nod i en pool via den nya parametern `MountConfiguration` för **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="a850c-1420">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="a850c-1421">Har nu stöd för nätverkssäkerhetsregler som blockerar nätverksåtkomst till en pool baserat på källportens trafik.</span><span class="sxs-lookup"><span data-stu-id="a850c-1421">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="a850c-1422">Detta görs via egenskapen `SourcePortRanges` på `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="a850c-1422">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="a850c-1423">När du kör en container stöder nu Batch körningen av uppgiften i arbetskatalogen för containern eller i arbetskatalogen för Batch-uppgiften.</span><span class="sxs-lookup"><span data-stu-id="a850c-1423">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="a850c-1424">Detta styrs av egenskapen `WorkingDirectory` på `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="a850c-1424">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="a850c-1425">Lade till en funktion för att ange en samling av offentliga IP-adresser på `PSNetworkConfiguration` via den nya egenskapen `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="a850c-1425">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="a850c-1426">Detta garanterar att noderna i poolen har en IP-adress från listan över IP-adresser som tillhandahållits av användare.</span><span class="sxs-lookup"><span data-stu-id="a850c-1426">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="a850c-1427">Om inget värde anges är standardvärdet för `WaitForSuccess` på `PSSTartTask` nu `$True` (var tidigare `$False`).</span><span class="sxs-lookup"><span data-stu-id="a850c-1427">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="a850c-1428">Om inget värde anges är standardvärdet för `Scope` på `PSAutoUserSpecification` nu `Pool` (var tidigare `Task` på Windows och `Pool` på Linux).</span><span class="sxs-lookup"><span data-stu-id="a850c-1428">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="a850c-1429">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="a850c-1429">Az.Cdn</span></span>
* <span data-ttu-id="a850c-1430">Introducerade UrlRewriteAction och CacheKeyQueryStringAction till RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="a850c-1430">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="a850c-1431">Åtgärdade flera buggar, som saknade indata för ”väljare” i cmdleten New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="a850c-1431">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a850c-1432">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a850c-1432">Az.Compute</span></span>
* <span data-ttu-id="a850c-1433">Funktion för diskkrypteringsuppsättning</span><span class="sxs-lookup"><span data-stu-id="a850c-1433">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="a850c-1434">Nya cmdletar:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="a850c-1434">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="a850c-1435">Parametern DiskEncryptionSetId har lagts till i följande cmdletar:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="a850c-1435">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="a850c-1436">Parametrarna DiskEncryptionSetId och EncryptionType har lagts till i följande cmdletar:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="a850c-1436">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="a850c-1437">Lägg till parametern PublicIPAddressVersion i New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="a850c-1437">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="a850c-1438">Flytta FileUris för anpassat skripttillägg från offentlig inställning till skyddad inställning</span><span class="sxs-lookup"><span data-stu-id="a850c-1438">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="a850c-1439">Lägg till ScaleInPolicy i cmdletarna New-AzVmss, New-AzVmssConfig och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a850c-1439">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="a850c-1440">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="a850c-1440">Breaking changes</span></span>
    - <span data-ttu-id="a850c-1441">Parametern UploadSizeInBytes används istället för DiskSizeGB för New-AzDiskConfig när CreateOption är Uppladdning</span><span class="sxs-lookup"><span data-stu-id="a850c-1441">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="a850c-1442">PublishingProfile.Source.ManagedImage.Id ersätts med StorageProfile.Source.Id i objektet GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="a850c-1442">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a850c-1443">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a850c-1443">Az.DataFactory</span></span>
* <span data-ttu-id="a850c-1444">Uppdatera ADF .Net SDK-versionen till 4.3.0</span><span class="sxs-lookup"><span data-stu-id="a850c-1444">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a850c-1445">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a850c-1445">Az.DataLakeStore</span></span>
* <span data-ttu-id="a850c-1446">Uppdatera ADLS SDK-version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) innehåller följande korrigeringar</span><span class="sxs-lookup"><span data-stu-id="a850c-1446">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="a850c-1447">Undvik att utlösa undantag när det inte går att deserialisera creationtime för inmatning av papperskorg eller katalog.</span><span class="sxs-lookup"><span data-stu-id="a850c-1447">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="a850c-1448">Gör inställning tillgänglig per tidsgräns för förfrågan i adlsclient</span><span class="sxs-lookup"><span data-stu-id="a850c-1448">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="a850c-1449">Korrigera överföringen av ursprunglig syncflag för badoffset-återställning</span><span class="sxs-lookup"><span data-stu-id="a850c-1449">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="a850c-1450">Korrigera EnumerateDirectory för att hämta fortsättningstoken när svar har kontrollerats</span><span class="sxs-lookup"><span data-stu-id="a850c-1450">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="a850c-1451">Korrigera bugg i Concat</span><span class="sxs-lookup"><span data-stu-id="a850c-1451">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="a850c-1452">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="a850c-1452">Az.FrontDoor</span></span>
* <span data-ttu-id="a850c-1453">Åtgärdade diverse stavfel i modul</span><span class="sxs-lookup"><span data-stu-id="a850c-1453">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="a850c-1454">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a850c-1454">Az.HDInsight</span></span>
* <span data-ttu-id="a850c-1455">Korrigerade buggen att kunder får felet ”inte en giltig Base-64-sträng” vid användning av Get-AzHDInsightCluster för att hämta klustret med ADLSGen1-lagring.</span><span class="sxs-lookup"><span data-stu-id="a850c-1455">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="a850c-1456">Lägg till en parameter med namnet ”ApplicationId” i de tre cmdletarna Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig och New-AzHDInsightCluster så att kunden kan tillhandahålla tjänstens huvudnamn för program-ID för åtkomst till Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="a850c-1456">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="a850c-1457">Ändrade Microsoft.Azure.Management.HDInsight från 2.1.0 till 5.1.0</span><span class="sxs-lookup"><span data-stu-id="a850c-1457">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="a850c-1458">Fem cmdletar har tagits bort:</span><span class="sxs-lookup"><span data-stu-id="a850c-1458">Removed five cmdlets:</span></span>
    - <span data-ttu-id="a850c-1459">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="a850c-1459">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="a850c-1460">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="a850c-1460">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="a850c-1461">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="a850c-1461">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="a850c-1462">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="a850c-1462">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="a850c-1463">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="a850c-1463">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="a850c-1464">Tre cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="a850c-1464">Added three cmdlets:</span></span>
    - <span data-ttu-id="a850c-1465">Get-AzHDInsightMonitoring som ersätter Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="a850c-1465">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="a850c-1466">Enable-AzHDInsightMonitoring som ersätter Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="a850c-1466">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="a850c-1467">Disable-AzHDInsightMonitoring som ersätter Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="a850c-1467">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="a850c-1468">Korrigerade cmdleten Get-AzHDInsightProperties för att stödja hämtning av funktionsinformation från en viss plats.</span><span class="sxs-lookup"><span data-stu-id="a850c-1468">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="a850c-1469">Parameteruppsättningarna (Spark1 och Spark2) har tagits bort från Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="a850c-1469">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="a850c-1470">Lägg till exempel för cmdleten Add-AzHDInsightSecurityProfile till hjälpdokumenten.</span><span class="sxs-lookup"><span data-stu-id="a850c-1470">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="a850c-1471">Ändrade utdatatyp för följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="a850c-1471">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="a850c-1472">Ändrade utdatatyp för Get-AzHDInsightProperties från CapabilitiesResponse till AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="a850c-1472">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="a850c-1473">Ändrade utdatatyp för Remove-AzHDInsightCluster från ClusterGetResponse till bool.</span><span class="sxs-lookup"><span data-stu-id="a850c-1473">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="a850c-1474">Ändrade utdatatyp för Set-AzHDInsightGatewaySettings HttpConnectivitySettings till GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="a850c-1474">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="a850c-1475">Lade till testfall för vissa scenarier.</span><span class="sxs-lookup"><span data-stu-id="a850c-1475">Added some scenario test cases.</span></span>
* <span data-ttu-id="a850c-1476">Ta bort vissa alias: Add-AzHDInsightConfigValues, Get-AzHDInsightProperties.</span><span class="sxs-lookup"><span data-stu-id="a850c-1476">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a850c-1477">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a850c-1477">Az.IotHub</span></span>
* <span data-ttu-id="a850c-1478">Icke-bakåtkompatibla ändringar:</span><span class="sxs-lookup"><span data-stu-id="a850c-1478">Breaking changes:</span></span>
    - <span data-ttu-id="a850c-1479">Cmdleten Add-AzIotHubEventHubConsumerGroup har inte längre stöd för parametern EventHubEndpointName och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="a850c-1479">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="a850c-1480">Parameteruppsättningen __AllParameterSets för cmdleten Add-AzIotHubEventHubConsumerGroup har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="a850c-1480">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="a850c-1481">Cmdleten Get-AzIotHubEventHubConsumerGroup har inte längre stöd för parametern EventHubEndpointName och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="a850c-1481">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="a850c-1482">Parameteruppsättningen __AllParameterSets för cmdleten Get-AzIotHubEventHubConsumerGroup har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="a850c-1482">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="a850c-1483">Egenskapen OperationsMonitoringProperties av typen Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="a850c-1483">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="a850c-1484">Egenskapen OperationsMonitoringProperties av typen Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="a850c-1484">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="a850c-1485">Cmdleten New-AzIotHubExportDevice stöder inte längre aliaset New-AzIotHubExportDevices.</span><span class="sxs-lookup"><span data-stu-id="a850c-1485">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="a850c-1486">Cmdleten New-AzIotHubImportDevice stöder inte längre aliaset New-AzIotHubImportDevices.</span><span class="sxs-lookup"><span data-stu-id="a850c-1486">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="a850c-1487">Cmdleten Remove-AzIotHubEventHubConsumerGroup har inte längre stöd för parametern EventHubEndpointName och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="a850c-1487">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="a850c-1488">Parameteruppsättningen __AllParameterSets för cmdleten Remove-AzIotHubEventHubConsumerGroup har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="a850c-1488">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="a850c-1489">Cmdleten Set-AzIotHub har inte längre stöd för parametern OperationsMonitoringProperties och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="a850c-1489">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="a850c-1490">Parameteruppsättningen UpdateOperationsMonitoringProperties för cmdleten Set-AzIotHub har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="a850c-1490">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a850c-1491">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a850c-1491">Az.RecoveryServices</span></span>
* <span data-ttu-id="a850c-1492">Azure Site Recovery-stöd för att konfigurera nätverksresurser som NSG, offentliga IP-adresser och interna lastbalanserare för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="a850c-1492">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="a850c-1493">Azure Site Recovery-stöd för att skriva till hanterad disk för vMWare till Azure.</span><span class="sxs-lookup"><span data-stu-id="a850c-1493">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="a850c-1494">Azure Site Recovery-stöd för NIC-reduktion för vMWare till Azure.</span><span class="sxs-lookup"><span data-stu-id="a850c-1494">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="a850c-1495">Azure Site Recovery-stöd för accelererat nätverk för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="a850c-1495">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="a850c-1496">Azure Site Recovery-stöd för automatisk uppdatering av agent för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="a850c-1496">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="a850c-1497">Azure Site Recovery-stöd för Standard SSD för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="a850c-1497">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="a850c-1498">Azure Site Recovery-stöd för tvåstegskryptering i Azure Disk Encryption för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="a850c-1498">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="a850c-1499">Azure Site Recovery-stöd för att skydda nyligen tillagda diskar för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="a850c-1499">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="a850c-1500">En funktion för mjuk borttagning av virtuella datorer samt tester för mjuk borttagning har tagits bort</span><span class="sxs-lookup"><span data-stu-id="a850c-1500">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="a850c-1501">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a850c-1501">Az.Resources</span></span>
* <span data-ttu-id="a850c-1502">Uppdatera beroendesammansättning för Microsoft.Extensions.Caching.Memory från 1.1.1 till 2.2</span><span class="sxs-lookup"><span data-stu-id="a850c-1502">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a850c-1503">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a850c-1503">Az.Network</span></span>
* <span data-ttu-id="a850c-1504">Ändra alla cmdletar för PrivateEndpointConnection så att de stöder generiska tjänstleverantörer.</span><span class="sxs-lookup"><span data-stu-id="a850c-1504">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="a850c-1505">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="a850c-1505">Updated cmdlet:</span></span>
        - <span data-ttu-id="a850c-1506">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a850c-1506">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="a850c-1507">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a850c-1507">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="a850c-1508">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a850c-1508">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="a850c-1509">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a850c-1509">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="a850c-1510">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a850c-1510">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="a850c-1511">Lägg till ny cmdlet för PrivateLinkResource så att det också stöder generiska tjänstleverantörer.</span><span class="sxs-lookup"><span data-stu-id="a850c-1511">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="a850c-1512">Ny cmdlet:</span><span class="sxs-lookup"><span data-stu-id="a850c-1512">New cmdlet:</span></span>
        - <span data-ttu-id="a850c-1513">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="a850c-1513">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="a850c-1514">Lägg till nya fält och parametrar för funktionen Proxy Protocol V2.</span><span class="sxs-lookup"><span data-stu-id="a850c-1514">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="a850c-1515">Lägg till egenskapen EnableProxyProtocol i PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="a850c-1515">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="a850c-1516">Lägg till egenskapen LinkIdentifier i PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a850c-1516">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="a850c-1517">Uppdaterade New-AzPrivateLinkService för att lägga till den nya valfria parametern EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="a850c-1517">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="a850c-1518">Korrigera felaktig beskrivning av parameter i referensdokumentationen för New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="a850c-1518">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="a850c-1519">Nya cmdletar som stöder Azure-brandväggsprincipen</span><span class="sxs-lookup"><span data-stu-id="a850c-1519">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="a850c-1520">Lägg till stöd för den underordnade resursen RouteTables för VirtualHub</span><span class="sxs-lookup"><span data-stu-id="a850c-1520">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="a850c-1521">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="a850c-1521">New cmdlets added:</span></span>
        - <span data-ttu-id="a850c-1522">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="a850c-1522">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="a850c-1523">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="a850c-1523">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="a850c-1524">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="a850c-1524">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="a850c-1525">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="a850c-1525">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="a850c-1526">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="a850c-1526">Set-AzVirtualHub</span></span>
* <span data-ttu-id="a850c-1527">Lägg till stöd för ny egenskaps-SKU för VirtualHub och VirtualWANType för VirtualWan</span><span class="sxs-lookup"><span data-stu-id="a850c-1527">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="a850c-1528">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="a850c-1528">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="a850c-1529">New-AzVirtualHub: lade till parameter-SKU</span><span class="sxs-lookup"><span data-stu-id="a850c-1529">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="a850c-1530">Update-AzVirtualHub: lade till parameter-SKU</span><span class="sxs-lookup"><span data-stu-id="a850c-1530">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="a850c-1531">New-AzVirtualWan: lade till parametern VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="a850c-1531">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="a850c-1532">Update-AzVirtualWan: lade till parametern VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="a850c-1532">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="a850c-1533">Lägg till stöd för egenskapen EnableInternetSecurity för HubVnetConnection, VpnConnection och ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="a850c-1533">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="a850c-1534">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="a850c-1534">New cmdlets added:</span></span>
        - <span data-ttu-id="a850c-1535">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="a850c-1535">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="a850c-1536">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="a850c-1536">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="a850c-1537">New-AzureRmVirtualHubVnetConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="a850c-1537">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="a850c-1538">New-AzureRmVpnConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="a850c-1538">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="a850c-1539">Update-AzureRmVpnConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="a850c-1539">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="a850c-1540">New-AzureRmExpressRouteConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="a850c-1540">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="a850c-1541">Set-AzureRmExpressRouteConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="a850c-1541">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="a850c-1542">Lägg till stöd för att konfigurera TopLevel WebApplicationFirewall-princip</span><span class="sxs-lookup"><span data-stu-id="a850c-1542">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="a850c-1543">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="a850c-1543">New cmdlets added:</span></span>
        - <span data-ttu-id="a850c-1544">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="a850c-1544">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="a850c-1545">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="a850c-1545">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="a850c-1546">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="a850c-1546">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="a850c-1547">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="a850c-1547">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="a850c-1548">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="a850c-1548">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="a850c-1549">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="a850c-1549">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="a850c-1550">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="a850c-1550">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="a850c-1551">New-AzApplicationGatewayFirewallPolicy: parametrarna PolicySetting, ManagedRule har lagts till</span><span class="sxs-lookup"><span data-stu-id="a850c-1551">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="a850c-1552">Stöd för operator för geomatchning har lagts till på CustomRule</span><span class="sxs-lookup"><span data-stu-id="a850c-1552">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="a850c-1553">Geomatchning har lagts till i operatorn på FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="a850c-1553">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="a850c-1554">Stöd har lagts till för brandväggsprinciperna perListener och perSite</span><span class="sxs-lookup"><span data-stu-id="a850c-1554">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="a850c-1555">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="a850c-1555">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="a850c-1556">New-AzApplicationGatewayHttpListener: parametrarna FirewallPolicy, FirewallPolicyId har lagts till</span><span class="sxs-lookup"><span data-stu-id="a850c-1556">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="a850c-1557">New-AzApplicationGatewayPathRuleConfig: parametrarna FirewallPolicy, FirewallPolicyId har lagts till</span><span class="sxs-lookup"><span data-stu-id="a850c-1557">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="a850c-1558">Åtgärdat så att nödvändigt undernät med namnet AzureBastionSubnet i PSBastion kan vara skiftlägesokänsligt</span><span class="sxs-lookup"><span data-stu-id="a850c-1558">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="a850c-1559">Stöd för mål-FQDN:er i nätverksregler och översatt FQDN i NAT-regler för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="a850c-1559">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="a850c-1560">Lägg till stöd för resursen RouteTables för IpGroup på den högsta nivån</span><span class="sxs-lookup"><span data-stu-id="a850c-1560">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="a850c-1561">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="a850c-1561">New cmdlets added:</span></span>
        - <span data-ttu-id="a850c-1562">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="a850c-1562">New-AzIpGroup</span></span>
        - <span data-ttu-id="a850c-1563">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="a850c-1563">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="a850c-1564">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="a850c-1564">Get-AzIpGroup</span></span>
        - <span data-ttu-id="a850c-1565">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="a850c-1565">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a850c-1566">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a850c-1566">Az.ServiceFabric</span></span>
* <span data-ttu-id="a850c-1567">Ta bort cmdleten Add-AzServiceFabricApplicationCertificate eftersom det här scenariot omfattas av Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="a850c-1567">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="a850c-1568">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a850c-1568">Az.Sql</span></span>
* <span data-ttu-id="a850c-1569">Stöd har lagts till för återställning av utelämnade databaser på hanterade instanser.</span><span class="sxs-lookup"><span data-stu-id="a850c-1569">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="a850c-1570">Inaktuella gamla cmdletar för granskning från kod.</span><span class="sxs-lookup"><span data-stu-id="a850c-1570">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="a850c-1571">Tog bort inaktuella alias:</span><span class="sxs-lookup"><span data-stu-id="a850c-1571">Removed deprecated aliases:</span></span>
* <span data-ttu-id="a850c-1572">Get-AzSqlDatabaseIndexRecommendations (använd Get-AzSqlDatabaseIndexRecommendation istället)</span><span class="sxs-lookup"><span data-stu-id="a850c-1572">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="a850c-1573">Get-AzSqlDatabaseRestorePoints (använd Get-AzSqlDatabaseRestorePoint istället)</span><span class="sxs-lookup"><span data-stu-id="a850c-1573">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="a850c-1574">Ta bort cmdleten Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="a850c-1574">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="a850c-1575">Ta bort alias för inaktuella cmdletar för inställningar för utvärdering av säkerhetsrisk</span><span class="sxs-lookup"><span data-stu-id="a850c-1575">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="a850c-1576">Inaktualisera cmdletar för inställningar för avancerad hotidentifiering</span><span class="sxs-lookup"><span data-stu-id="a850c-1576">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="a850c-1577">Lägga till cmdletar för att inaktivera och aktivera känslighetsrekommendationer på kolumner i en databas.</span><span class="sxs-lookup"><span data-stu-id="a850c-1577">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a850c-1578">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a850c-1578">Az.Storage</span></span>
* <span data-ttu-id="a850c-1579">Stöd för att aktivera stora filresurser vid skapande eller uppdatering av lagringskonto</span><span class="sxs-lookup"><span data-stu-id="a850c-1579">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="a850c-1580">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a850c-1580">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="a850c-1581">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a850c-1581">Set-AzStorageAccount</span></span>
* <span data-ttu-id="a850c-1582">När du stänger/hämtar en filreferens kan du hoppa över kontrollen av huruvida indatasökvägen är en filkatalog eller en fil för att undvika problem med objekt som har status DeletePending</span><span class="sxs-lookup"><span data-stu-id="a850c-1582">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="a850c-1583">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="a850c-1583">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="a850c-1584">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="a850c-1584">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="a850c-1585">2.8.0 – oktober 2019</span><span class="sxs-lookup"><span data-stu-id="a850c-1585">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="a850c-1586">Allmänt</span><span class="sxs-lookup"><span data-stu-id="a850c-1586">General</span></span>
* <span data-ttu-id="a850c-1587">AZ. HealthcareApis 1.0.0-version</span><span class="sxs-lookup"><span data-stu-id="a850c-1587">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="a850c-1588">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a850c-1588">Az.Accounts</span></span>
* <span data-ttu-id="a850c-1589">Uppdatera telemetri och URL-omskrivning för genererade moduler, korrigera Windows-enhetstester.</span><span class="sxs-lookup"><span data-stu-id="a850c-1589">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="a850c-1590">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a850c-1590">Az.ApiManagement</span></span>
* <span data-ttu-id="a850c-1591">**Set-AzApiManagementApi** – Tillagt stöd för att uppdatera Api till ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="a850c-1591">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="a850c-1592">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="a850c-1592">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a850c-1593">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a850c-1593">Az.Automation</span></span>
* <span data-ttu-id="a850c-1594">Åtgärdade cmdleten New-AzureAutomationSoftwareUpdateConfiguration för parametern för inställning av Linux-omstart.</span><span class="sxs-lookup"><span data-stu-id="a850c-1594">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="a850c-1595">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="a850c-1595">Az.Batch</span></span>
* <span data-ttu-id="a850c-1596">**Get-AzBatchNodeAgentSku** är inaktuell och ersätts av **Get-AzBatchSupportImage** i version 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="a850c-1596">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a850c-1597">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a850c-1597">Az.Compute</span></span>
* <span data-ttu-id="a850c-1598">Lägg till parametrarna Priority, EvictionPolicy och MaxPrice till cmdletarna New-AzVM och New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a850c-1598">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="a850c-1599">Korrigera varningsmeddelande och hjälpdokument för cmdletarna Add-AzVMAdditionalUnattendContent och Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="a850c-1599">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="a850c-1600">Åtgärda – skipVmBackup-undantag för virtuella Linux-datorer med hanterade diskar för Set-AzVMDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="a850c-1600">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="a850c-1601">Åtgärda fel i uppdatera krypteringsinställningarna i set-AzVMDiskEncryptionExtension, scenario i två steg.</span><span class="sxs-lookup"><span data-stu-id="a850c-1601">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a850c-1602">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a850c-1602">Az.DataFactory</span></span>
* <span data-ttu-id="a850c-1603">Lägga till CRUD-kommandon för ADF V2-dataflödet: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow och Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="a850c-1603">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="a850c-1604">Lägger till åtgärdskommandon för ADF V2-dataflödesfelsökningssession: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand och Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="a850c-1604">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="a850c-1605">Uppdatera ADF .Net SDK-versionen till 4.2.0</span><span class="sxs-lookup"><span data-stu-id="a850c-1605">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a850c-1606">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a850c-1606">Az.DataLakeStore</span></span>
* <span data-ttu-id="a850c-1607">Korrigera kontovalidering så att konton med ”-” kan skickas utan domän</span><span class="sxs-lookup"><span data-stu-id="a850c-1607">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="a850c-1608">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="a850c-1608">Az.HealthcareApis</span></span>
* <span data-ttu-id="a850c-1609">PowerShell-versionen har uppdaterats till 1.0.0</span><span class="sxs-lookup"><span data-stu-id="a850c-1609">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="a850c-1610">Uppdaterade SDK-versionen till 1.0.2</span><span class="sxs-lookup"><span data-stu-id="a850c-1610">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="a850c-1611">Uppdatera i tester för att referera till en ny SDK-version</span><span class="sxs-lookup"><span data-stu-id="a850c-1611">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="a850c-1612">Utdatastrukturen har uppdaterats från kapslad till förenklad.</span><span class="sxs-lookup"><span data-stu-id="a850c-1612">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a850c-1613">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a850c-1613">Az.IotHub</span></span>
* <span data-ttu-id="a850c-1614">Lägg till ny routningskälla: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="a850c-1614">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="a850c-1615">Mindre felkorrigering: Get-AzIothub returnerar inte subscriptionId</span><span class="sxs-lookup"><span data-stu-id="a850c-1615">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a850c-1616">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a850c-1616">Az.Monitor</span></span>
* <span data-ttu-id="a850c-1617">Nya åtgärdsgruppsmottagare har lagts till för åtgärdsgrupp   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="a850c-1617">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="a850c-1618">Använd vanligt aviseringsschema som är aktiverat för mottagarna.</span><span class="sxs-lookup"><span data-stu-id="a850c-1618">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="a850c-1619">Detta gäller inte för SMS, push för Azure-app, ITSM och röstmottagare</span><span class="sxs-lookup"><span data-stu-id="a850c-1619">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="a850c-1620">Webhooks har nu stöd för Azure Active Directory-autentisering.</span><span class="sxs-lookup"><span data-stu-id="a850c-1620">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a850c-1621">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a850c-1621">Az.Network</span></span>
* <span data-ttu-id="a850c-1622">Lägg till ny cmdlet Get-AzAvailableServiceAlias som kan anropas för att hämta de alias som kan användas för tjänstslutpunktsprinciper.</span><span class="sxs-lookup"><span data-stu-id="a850c-1622">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="a850c-1623">Stöd för tillägg av trafikväljare har lagts till i gatewayanslutningar för virtuella nätverk</span><span class="sxs-lookup"><span data-stu-id="a850c-1623">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="a850c-1624">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="a850c-1624">New cmdlets added:</span></span>
        - <span data-ttu-id="a850c-1625">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="a850c-1625">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="a850c-1626">Cmdletar har uppdaterats med valfri parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="a850c-1626">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="a850c-1627">Lägg till stöd för ESP- och AH-protokoll i konfiguration av nätverkssäkerhetsregler</span><span class="sxs-lookup"><span data-stu-id="a850c-1627">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="a850c-1628">Uppdaterade cmdletar:</span><span class="sxs-lookup"><span data-stu-id="a850c-1628">Updated cmdlets:</span></span>
        - <span data-ttu-id="a850c-1629">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a850c-1629">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="a850c-1630">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a850c-1630">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="a850c-1631">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a850c-1631">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="a850c-1632">Förbättra hanteringen av undantag i Cortex-cmdletar</span><span class="sxs-lookup"><span data-stu-id="a850c-1632">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="a850c-1633">Nya generationer och SKU:er för VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="a850c-1633">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="a850c-1634">Introducera nya generationer för VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="a850c-1634">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="a850c-1635">Introducera nya SKU:er med högt dataflöde för VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="a850c-1635">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="a850c-1636">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="a850c-1636">Az.RedisCache</span></span>
* <span data-ttu-id="a850c-1637">Uppdaterad referensdokumentation för ”set-AzRedisCache” för att inkludera saknade värden för parametern ”size”</span><span class="sxs-lookup"><span data-stu-id="a850c-1637">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="a850c-1638">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a850c-1638">Az.Sql</span></span>
* <span data-ttu-id="a850c-1639">Lägg till stöd för inställningen Active Directory administratör på den hanterade instansen</span><span class="sxs-lookup"><span data-stu-id="a850c-1639">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a850c-1640">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a850c-1640">Az.Storage</span></span>
* <span data-ttu-id="a850c-1641">Uppdatera Lagringsklientbibliotek till 11.1.0</span><span class="sxs-lookup"><span data-stu-id="a850c-1641">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="a850c-1642">Lista containrar med hanteringsplans-API, kommer att listas med NextPageLink</span><span class="sxs-lookup"><span data-stu-id="a850c-1642">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="a850c-1643">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="a850c-1643">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="a850c-1644">Lista lagringskonton från prenumerationen, kommer att listas med NextPageLink</span><span class="sxs-lookup"><span data-stu-id="a850c-1644">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="a850c-1645">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a850c-1645">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="a850c-1646">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="a850c-1646">Az.StorageSync</span></span>
* <span data-ttu-id="a850c-1647">Åtgärda problemet 9810 i Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="a850c-1647">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a850c-1648">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a850c-1648">Az.Websites</span></span>
* <span data-ttu-id="a850c-1649">Set-AzWebApp – uppdatering av ASP för en app misslyckades</span><span class="sxs-lookup"><span data-stu-id="a850c-1649">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="a850c-1650">2.7.0 – september 2019</span><span class="sxs-lookup"><span data-stu-id="a850c-1650">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="a850c-1651">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a850c-1651">Az.ApiManagement</span></span>
* <span data-ttu-id="a850c-1652">Uppdatera ”-Format”-parameterbeskrivningen i ”Set-AzApiManagementPolicy”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="a850c-1652">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="a850c-1653">Referenser för den föråldrade cmdleten ”Update-AzApiManagementDeployment” har tagits bort från referensdokumentationen.</span><span class="sxs-lookup"><span data-stu-id="a850c-1653">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="a850c-1654">Använd ”Set-AzApiManagement” i stället.</span><span class="sxs-lookup"><span data-stu-id="a850c-1654">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a850c-1655">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a850c-1655">Az.Automation</span></span>
* <span data-ttu-id="a850c-1656">Stavfel har korrigerats i exempel i referensdokumentationen för ”Register-AzAutomationDscNode”</span><span class="sxs-lookup"><span data-stu-id="a850c-1656">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="a850c-1657">Klargörande har lagts till om OS-begränsningar för Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="a850c-1657">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="a850c-1658">Null-referensundantag har korrigerats för -Wait-alternativet i Start-AzAutomationRunbook-cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a850c-1658">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a850c-1659">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a850c-1659">Az.Compute</span></span>
* <span data-ttu-id="a850c-1660">Lägg till UploadSizeInBytes-parameter till New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="a850c-1660">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="a850c-1661">Lägg till Incremental-parameter till New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="a850c-1661">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="a850c-1662">Lägg till en funktion för virtuella datorer med låg prioritet:</span><span class="sxs-lookup"><span data-stu-id="a850c-1662">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="a850c-1663">MaxPrice-, EvictionPolicy- och Priority-parametrar har lagts till i New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="a850c-1663">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="a850c-1664">MaxPrice-parametern har lagts till i New-AzVmssConfig-, Update-AzVM- och Update-AzVmss-cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="a850c-1664">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="a850c-1665">Åtgärda problem med VM-referenser för Get-AzAvailabilitySet-cmdleten när alla tillgänglighetsuppsättningar i prenumerationen visas.</span><span class="sxs-lookup"><span data-stu-id="a850c-1665">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="a850c-1666">Korrigera null-undantaget för Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="a850c-1666">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="a850c-1667">Korrigera VHD-metoden för sökning relativt till slut.</span><span class="sxs-lookup"><span data-stu-id="a850c-1667">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="a850c-1668">Åtgärda UltraSSD-problem för New-AzVM och Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="a850c-1668">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a850c-1669">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a850c-1669">Az.DataFactory</span></span>
* <span data-ttu-id="a850c-1670">Lägger till 3 nya kommandon för ADF V2 – Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription och Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="a850c-1670">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="a850c-1671">ADF .Net SDK har uppdaterats till 4.1.3</span><span class="sxs-lookup"><span data-stu-id="a850c-1671">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="a850c-1672">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a850c-1672">Az.HDInsight</span></span>
* <span data-ttu-id="a850c-1673">Anrop för icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="a850c-1673">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a850c-1674">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a850c-1674">Az.IotHub</span></span>
* <span data-ttu-id="a850c-1675">Lägg till stöd för att anropa redundans för en IotHub till den geo-länkade katastrofåterställningsregionen.</span><span class="sxs-lookup"><span data-stu-id="a850c-1675">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="a850c-1676">Lägg till stöd för att hantera meddelandeberikning för en IotHub.</span><span class="sxs-lookup"><span data-stu-id="a850c-1676">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="a850c-1677">Nya cmdlet:ar är:</span><span class="sxs-lookup"><span data-stu-id="a850c-1677">New cmdlets are:</span></span>
    - <span data-ttu-id="a850c-1678">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="a850c-1678">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="a850c-1679">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="a850c-1679">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="a850c-1680">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="a850c-1680">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="a850c-1681">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="a850c-1681">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a850c-1682">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a850c-1682">Az.Monitor</span></span>
* <span data-ttu-id="a850c-1683">Pekar på den senaste Monitor SDK:n, dvs. 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="a850c-1683">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="a850c-1684">Lägger till bakåtkompatibla ändringar i Metrics-cmdletarna, dvs. enhetsuppräkningen stöder flera nya värden.</span><span class="sxs-lookup"><span data-stu-id="a850c-1684">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="a850c-1685">Detta är skrivskyddade cmdletar, så det förekommer inga ändringar i inmatningen för cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="a850c-1685">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="a850c-1686">API-versionen för **ActionGroups**-begäranden är nu **2019-06-01**. Tidigare var den **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="a850c-1686">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="a850c-1687">Test av scenarier har uppdaterats för att anpassas till den här ändringen.</span><span class="sxs-lookup"><span data-stu-id="a850c-1687">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="a850c-1688">Ett nytt obligatoriskt argument har lagts till för konstruktorerna för klasserna **EmailReceiver** och **WebhookReceiver** – ett booleskt värde med namnet **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="a850c-1688">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="a850c-1689">Värdet är för närvarande fast till **false** så att den här icke-bakåtkompatibla ändringen är dold från cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="a850c-1689">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="a850c-1690">**Obs!** Det här är en tillfällig ändring som måste verifieras av Alerts-teamet.</span><span class="sxs-lookup"><span data-stu-id="a850c-1690">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="a850c-1691">Ordningen på argumenten för konstruktorn för klassen **Source** (relaterad till klassen **ScheduledQueryRuleSource**) har ändrats från den tidigare SDK:n.</span><span class="sxs-lookup"><span data-stu-id="a850c-1691">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="a850c-1692">Den här ändringen krävde korrigering av två enhetstest: de kompilerades, men testerna skickades inte.</span><span class="sxs-lookup"><span data-stu-id="a850c-1692">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="a850c-1693">Ordningen på argumenten för konstruktorn för klassen **AlertingAction** (relaterad till klassen **ScheduledQueryRuleSource**) har ändrats från den tidigare SDK:n.</span><span class="sxs-lookup"><span data-stu-id="a850c-1693">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="a850c-1694">Den här ändringen krävde korrigering av två enhetstest: de kompilerades, men testerna skickades inte.</span><span class="sxs-lookup"><span data-stu-id="a850c-1694">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="a850c-1695">Stöd för kriterier för dynamiskt tröskelvärde för måttavisering v2</span><span class="sxs-lookup"><span data-stu-id="a850c-1695">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="a850c-1696">New-AzMetricAlertRuleV2Criteria: skapar nu även kriterier för dynamiskt tröskelvärde</span><span class="sxs-lookup"><span data-stu-id="a850c-1696">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="a850c-1697">Add-AzMetricAlertRuleV2: accepterar nu även kriterier för dynamiskt tröskelvärde</span><span class="sxs-lookup"><span data-stu-id="a850c-1697">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="a850c-1698">Förbättringar i schemalagd frågeregel (SQR)</span><span class="sxs-lookup"><span data-stu-id="a850c-1698">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="a850c-1699">Cmdletar accepterar ”Location”-parameter i båda formaten, antingen platsen (t.ex. eastus) eller platsens visningsnamn (t.ex. USA, östra)</span><span class="sxs-lookup"><span data-stu-id="a850c-1699">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="a850c-1700">”Enabled”-parametern illustreras korrekt i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="a850c-1700">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="a850c-1701">Exempel för den valfria parametern ”ActionGroup” har lagts till</span><span class="sxs-lookup"><span data-stu-id="a850c-1701">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="a850c-1702">Förbättrade hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="a850c-1702">Overall improved help files</span></span>
* <span data-ttu-id="a850c-1703">Åtgärda bugg då omfattningstypen fastställs för ”Set-AzActionRule”</span><span class="sxs-lookup"><span data-stu-id="a850c-1703">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a850c-1704">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a850c-1704">Az.Network</span></span>
* <span data-ttu-id="a850c-1705">Korrigera felaktigt exempel i referensdokumentationen för ”New-AzApplicationGateway”</span><span class="sxs-lookup"><span data-stu-id="a850c-1705">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="a850c-1706">Lägg till anmärkning i ”Get-AzNetworkWatcherPacketCapture”-referensdokumentationen om hämtning av alla egenskaper för en paketinsamling</span><span class="sxs-lookup"><span data-stu-id="a850c-1706">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="a850c-1707">Exempel har korrigerats i ”Test-AzNetworkWatcherIPFlow”-referensdokumentationen för korrekt uppräkning av nätverkskort</span><span class="sxs-lookup"><span data-stu-id="a850c-1707">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="a850c-1708">Förbättrad tolkning av molnundantag för att visa eventuell ytterligare information</span><span class="sxs-lookup"><span data-stu-id="a850c-1708">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="a850c-1709">Förbättrad tolkning av molnundantag för att hantera ytterligare en typ av SDK-undantag</span><span class="sxs-lookup"><span data-stu-id="a850c-1709">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="a850c-1710">Felaktig mappning av säkerhetsregelmodeller har korrigerats</span><span class="sxs-lookup"><span data-stu-id="a850c-1710">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="a850c-1711">Egenskaper har lagts till för nätverksgränssnittet för funktionen Privat IP</span><span class="sxs-lookup"><span data-stu-id="a850c-1711">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="a850c-1712">Egenskapen ”PrivateEndpoint” har lagts till som en typ av PSResourceId till PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="a850c-1712">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="a850c-1713">Egenskapen ”PrivateLinkConnectionProperties” har lagts till som en typ av PSIpConfigurationConnectivityInformation till PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="a850c-1713">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="a850c-1714">Modellklassen PSIpConfigurationConnectivityInformation har lagts till</span><span class="sxs-lookup"><span data-stu-id="a850c-1714">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="a850c-1715">ApplicationRuleProtocolType ”mssql” har lagts till för Azure Firewall-resurs</span><span class="sxs-lookup"><span data-stu-id="a850c-1715">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="a850c-1716">MultiLink-stöd i virtuellt WAN</span><span class="sxs-lookup"><span data-stu-id="a850c-1716">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="a850c-1717">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="a850c-1717">New cmdlets</span></span>
        - <span data-ttu-id="a850c-1718">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="a850c-1718">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="a850c-1719">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="a850c-1719">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="a850c-1720">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="a850c-1720">Updated cmdlet:</span></span>
        - <span data-ttu-id="a850c-1721">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="a850c-1721">New-VpnSite</span></span>
        - <span data-ttu-id="a850c-1722">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="a850c-1722">Update-VpnSite</span></span>
        - <span data-ttu-id="a850c-1723">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="a850c-1723">New-VpnConnection</span></span>
        - <span data-ttu-id="a850c-1724">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="a850c-1724">Update-VpnConnection</span></span>
* <span data-ttu-id="a850c-1725">Dokument för vissa PowerShell-exempel har korrigerats så att Az-cmdletar används i stället för AzureRM-cmdletar</span><span class="sxs-lookup"><span data-stu-id="a850c-1725">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a850c-1726">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a850c-1726">Az.RecoveryServices</span></span>
* <span data-ttu-id="a850c-1727">Uppdatera AzureVMpolicy-objekt med ProtectedItemsCount-attribut</span><span class="sxs-lookup"><span data-stu-id="a850c-1727">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="a850c-1728">Ytterligare tester har lagts till för VM-princip och återställning av ursprungligt lagringskonto</span><span class="sxs-lookup"><span data-stu-id="a850c-1728">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="a850c-1729">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a850c-1729">Az.Resources</span></span>
* <span data-ttu-id="a850c-1730">Åtgärda fel där det inte gick att anropa New-AzRoleAssignment utan parametern Scope.</span><span class="sxs-lookup"><span data-stu-id="a850c-1730">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a850c-1731">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a850c-1731">Az.ServiceFabric</span></span>
* <span data-ttu-id="a850c-1732">Stavfel har korrigerats i exempel för ”Update-AzServiceFabricReliability”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="a850c-1732">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="a850c-1733">Lägger till nya cmdletar för att hantera program och tjänster:</span><span class="sxs-lookup"><span data-stu-id="a850c-1733">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="a850c-1734">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="a850c-1734">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="a850c-1735">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="a850c-1735">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="a850c-1736">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="a850c-1736">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="a850c-1737">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="a850c-1737">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="a850c-1738">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="a850c-1738">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="a850c-1739">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="a850c-1739">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="a850c-1740">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="a850c-1740">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="a850c-1741">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="a850c-1741">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="a850c-1742">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="a850c-1742">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="a850c-1743">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="a850c-1743">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="a850c-1744">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="a850c-1744">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="a850c-1745">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="a850c-1745">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="a850c-1746">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="a850c-1746">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="a850c-1747">Service Fabric SDK har uppgraderats till version 1.2.0 som använder Service Fabric-resursprovidern med API-version 2019-03-01.</span><span class="sxs-lookup"><span data-stu-id="a850c-1747">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="a850c-1748">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="a850c-1748">Az.SignalR</span></span>
* <span data-ttu-id="a850c-1749">Lägg till Update-, Restart-, CheckNameAvailability- och GetUsage-cmdletar</span><span class="sxs-lookup"><span data-stu-id="a850c-1749">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="a850c-1750">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a850c-1750">Az.Sql</span></span>
* <span data-ttu-id="a850c-1751">Uppdatera exempel i referensdokumentationen för ”Get-AzSqlElasticPool”</span><span class="sxs-lookup"><span data-stu-id="a850c-1751">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="a850c-1752">vCore-exempel för att skapa en elastisk pool (New-AzSqlElasticPool) har lagts till.</span><span class="sxs-lookup"><span data-stu-id="a850c-1752">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="a850c-1753">Ta bort verifieringen av EmailAddresses och kontrollen som bekräftar att EmailAdmins inte är falskt när EmailAddresses är tomt i Set-AzSqlServerAdvancedThreatProtectionPolicy och Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="a850c-1753">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="a850c-1754">Server-/databasgranskningsinställningar kan tas bort när det finns flera diagnostikinställningar som aktiverar granskningskategorin.</span><span class="sxs-lookup"><span data-stu-id="a850c-1754">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="a850c-1755">Åtgärda verifiering av e-postadresser i flera Sql Vulnerability Assessment-cmdletar (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting och Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="a850c-1755">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a850c-1756">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a850c-1756">Az.Storage</span></span>
* <span data-ttu-id="a850c-1757">Exempel i referensdokumentationen för ”Get-AzStorageAccountKey” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="a850c-1757">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="a850c-1758">Vid upp- och nedladdning av en Azure-fil kan SMB-egenskaperna för källfilen (t.ex. filattribut, tidpunkten då filen skapades och tidpunkten för den senaste skrivningen) sparas i målfilen</span><span class="sxs-lookup"><span data-stu-id="a850c-1758">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="a850c-1759">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="a850c-1759">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="a850c-1760">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="a850c-1760">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="a850c-1761">Korrigera problem med uppladdningen av blockblob med egenskaper/metadata för ImmutabilityPolicy i containrar.</span><span class="sxs-lookup"><span data-stu-id="a850c-1761">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="a850c-1762">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="a850c-1762">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="a850c-1763">Stöd för hantering av Azure-filresurser med API för hanteringsplan</span><span class="sxs-lookup"><span data-stu-id="a850c-1763">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="a850c-1764">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="a850c-1764">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="a850c-1765">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="a850c-1765">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="a850c-1766">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="a850c-1766">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="a850c-1767">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="a850c-1767">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a850c-1768">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a850c-1768">Az.Websites</span></span>
* <span data-ttu-id="a850c-1769">Åtgärdar problemet där webapp-taggar togs bort när appen migrerades till nya ASP</span><span class="sxs-lookup"><span data-stu-id="a850c-1769">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="a850c-1770">Åtgärda Publish-AzureWebapp så att det fungerar i Linux och Windows</span><span class="sxs-lookup"><span data-stu-id="a850c-1770">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="a850c-1771">Uppdatera exempel i ”Get-AzWebAppPublishingProfile”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="a850c-1771">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="a850c-1772">2.6.0 – augusti 2019</span><span class="sxs-lookup"><span data-stu-id="a850c-1772">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="a850c-1773">Allmänt</span><span class="sxs-lookup"><span data-stu-id="a850c-1773">General</span></span>
* <span data-ttu-id="a850c-1774">Åtgärdade diverse skrivfel i flera moduler</span><span class="sxs-lookup"><span data-stu-id="a850c-1774">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="a850c-1775">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a850c-1775">Az.Accounts</span></span>
* <span data-ttu-id="a850c-1776">Stöd för användartilldelat MSI i Azure Functions-autentisering (#9479)</span><span class="sxs-lookup"><span data-stu-id="a850c-1776">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="a850c-1777">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="a850c-1777">Az.Aks</span></span>
* <span data-ttu-id="a850c-1778">Åtgärda problem med utdata för "Get-AzAks"</span><span class="sxs-lookup"><span data-stu-id="a850c-1778">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="a850c-1779">Mer information här: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="a850c-1779">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="a850c-1780">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a850c-1780">Az.ApiManagement</span></span>
* <span data-ttu-id="a850c-1781">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="a850c-1781">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="a850c-1782">Uppdatera .net-NuGet-versionen, som inte tillämpar begränsningar för productId, apiId och userId</span><span class="sxs-lookup"><span data-stu-id="a850c-1782">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="a850c-1783">**Get-AzApiManagementProduct** – Lade till stöd för frågekörning mot produkter via API.</span><span class="sxs-lookup"><span data-stu-id="a850c-1783">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="a850c-1784">**New-AzApiManagementApiRevision** – Korrigering för problem där ApiRevisionDescription inte angavs vid skapande av ny API-revision https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="a850c-1784">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="a850c-1785">Åtgärdade skrivfel i modellen "PsApiManagementOAuth2AuthrozationServer" till "PsApiManagementOAuth2AuthorizationServer"</span><span class="sxs-lookup"><span data-stu-id="a850c-1785">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="a850c-1786">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="a850c-1786">Az.Batch</span></span>
* <span data-ttu-id="a850c-1787">Åtgärdade skrivfel i hjälpmeddelande och dokumentation till att skriva Windows med versaler</span><span class="sxs-lookup"><span data-stu-id="a850c-1787">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="a850c-1788">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="a850c-1788">Az.Cdn</span></span>
* <span data-ttu-id="a850c-1789">Åtgärdade skrivfel i CDN-modulens konverteringshjälp</span><span class="sxs-lookup"><span data-stu-id="a850c-1789">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a850c-1790">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a850c-1790">Az.Compute</span></span>
* <span data-ttu-id="a850c-1791">Lägg till VmssId i New-AzVMConfig-cmdleten</span><span class="sxs-lookup"><span data-stu-id="a850c-1791">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="a850c-1792">Lägg till parametrarna TerminateScheduledEvents och TerminateScheduledEventNotBeforeTimeoutInMinutes i New-AzVmssConfig och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a850c-1792">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="a850c-1793">Lägg till egenskapen HyperVGeneration till avbildningsobjekt för virtuell dator</span><span class="sxs-lookup"><span data-stu-id="a850c-1793">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="a850c-1794">Lägg till funktioner för Host och HostGroup</span><span class="sxs-lookup"><span data-stu-id="a850c-1794">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="a850c-1795">Nya cmdletar:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="a850c-1795">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="a850c-1796">HostId-parametern läggs till i New-AzVMConfig och New-AzVM</span><span class="sxs-lookup"><span data-stu-id="a850c-1796">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="a850c-1797">Uppdatera exempel i "Invoke-AzVMRunCommand"-dokumentationen till att använda rätt parameternamn</span><span class="sxs-lookup"><span data-stu-id="a850c-1797">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="a850c-1798">Uppdatera "-VolumeType"-beskrivningen i referensdokumentationen för "set-AzVMDiskEncryptionExtension" och "set-AzVmssDiskEncryptionExtension"</span><span class="sxs-lookup"><span data-stu-id="a850c-1798">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a850c-1799">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a850c-1799">Az.DataFactory</span></span>
* <span data-ttu-id="a850c-1800">Åtgärda skrivfel till att använda versaler för "Windows" i "New-AzDataFactoryEncryptValue"-dokumentationen</span><span class="sxs-lookup"><span data-stu-id="a850c-1800">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="a850c-1801">Uppdaterade ADF .Net SDK-versionen till 4.1.2</span><span class="sxs-lookup"><span data-stu-id="a850c-1801">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="a850c-1802">Lägg till parametrarna "DataProxyIntegrationRuntimeName", "DataProxyStagingLinkedServiceName" och "DataProxyStagingPath" för "Set-AzureRmDataFactoryV2IntegrationRuntime"-cmd för att aktivera konfiguration av lokalt installerad integrationskörning som en proxy för SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="a850c-1802">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="a850c-1803">Uppdaterade PSTriggerRun till att visa utlöst pipeline, meddelande och egenskaper samt PSActivityRun till att visa aktivitetstypen</span><span class="sxs-lookup"><span data-stu-id="a850c-1803">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a850c-1804">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a850c-1804">Az.DataLakeStore</span></span>
* <span data-ttu-id="a850c-1805">Korrigering av frysning av Get-DataLakeStoreDeletedItem för fel eller fjärrundantag.</span><span class="sxs-lookup"><span data-stu-id="a850c-1805">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="a850c-1806">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a850c-1806">Az.EventHub</span></span>
* <span data-ttu-id="a850c-1807">Korrigering av problem #9658 : Skrivfel i parametern VirtualNteworkRule i Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="a850c-1807">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="a850c-1808">Korrigering av problem #9558 : Set-AzEventHubNamespace använder PATCH i stället för PUT</span><span class="sxs-lookup"><span data-stu-id="a850c-1808">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="a850c-1809">lade till parametern EnableKafka i Set-AzEventHubNamespace-cmdleten</span><span class="sxs-lookup"><span data-stu-id="a850c-1809">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="a850c-1810">Korrigering av problem #9786 : kan inte skapa en regel med Endast lyssna-behörighet</span><span class="sxs-lookup"><span data-stu-id="a850c-1810">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="a850c-1811">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="a850c-1811">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="a850c-1812">Åtgärdade skrivfel i dokumentation där "Azure" skrevs helt med gemener</span><span class="sxs-lookup"><span data-stu-id="a850c-1812">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a850c-1813">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a850c-1813">Az.Monitor</span></span>
* <span data-ttu-id="a850c-1814">Åtgärdade felaktigt parameternamn i hjälpdokumentationen</span><span class="sxs-lookup"><span data-stu-id="a850c-1814">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a850c-1815">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a850c-1815">Az.Network</span></span>
* <span data-ttu-id="a850c-1816">Uppdaterade New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="a850c-1816">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="a850c-1817">Gjorde parametern "PublicIpAddress" inaktuell eftersom den aldrig används på serversidan.</span><span class="sxs-lookup"><span data-stu-id="a850c-1817">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="a850c-1818">Lade till den valfria parametern "Primary", som anger huruvida den aktuella IP-konfigurationen är den primära.</span><span class="sxs-lookup"><span data-stu-id="a850c-1818">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="a850c-1819">Förbättrade hanteringen av felundantag för begärande från SDK – åtgärdar problemet att tidigare SDK-undantag inte hanteras på rätt sätt, vilket leder till att viktig felinformation inte visas</span><span class="sxs-lookup"><span data-stu-id="a850c-1819">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="a850c-1820">Justerade valideringslogiken för IPv6-IP-prefix till att kontrollera korrekt IPv6-prefixlängd.</span><span class="sxs-lookup"><span data-stu-id="a850c-1820">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="a850c-1821">Uppdaterade Get-AzVirtualNetworkSubnetConfig: Lade till parameter som anges till get av undernätets resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="a850c-1821">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="a850c-1822">Uppdaterade beskrivningen av parametern Location för AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="a850c-1822">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="a850c-1823">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a850c-1823">Az.OperationalInsights</span></span>
* <span data-ttu-id="a850c-1824">Uppdaterade dokumentation för "New-AzOperationalInsightsLinuxSyslogDataSource"</span><span class="sxs-lookup"><span data-stu-id="a850c-1824">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="a850c-1825">Lade till exempel</span><span class="sxs-lookup"><span data-stu-id="a850c-1825">Added example</span></span>
    - <span data-ttu-id="a850c-1826">Uppdaterade beskrivningen av parametern "-Name"</span><span class="sxs-lookup"><span data-stu-id="a850c-1826">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="a850c-1827">Lade till ett exempel för New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="a850c-1827">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="a850c-1828">Ändrade beskrivningen av parametern -Name för New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="a850c-1828">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a850c-1829">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a850c-1829">Az.RecoveryServices</span></span>
* <span data-ttu-id="a850c-1830">Uppdatera "Get-AzRecoveryServicesBackupJobDetail.md"</span><span class="sxs-lookup"><span data-stu-id="a850c-1830">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="a850c-1831">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a850c-1831">Az.Resources</span></span>
* <span data-ttu-id="a850c-1832">Lägg till stöd för den nya API-versionen från 2019-05-10 för Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="a850c-1832">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="a850c-1833">Lägg till stöd för "copy.count = 0" för variabler, resurser och egenskaper</span><span class="sxs-lookup"><span data-stu-id="a850c-1833">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="a850c-1834">Resurser med "condition = false" eller "copy.count = 0" tas bort i complete-läget</span><span class="sxs-lookup"><span data-stu-id="a850c-1834">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="a850c-1835">Lägg till ett exempel på tilldelning av princip på prenumerationsnivå i hjälpdokumentationen</span><span class="sxs-lookup"><span data-stu-id="a850c-1835">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="a850c-1836">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a850c-1836">Az.ServiceBus</span></span>
* <span data-ttu-id="a850c-1837">Korrigering av problem #9658 : Skrivfel i parametern VirtualNetworkRule i set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="a850c-1837">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="a850c-1838">Korrigering av problem #9786 : kan inte skapa en regel med Endast lyssna-behörighet</span><span class="sxs-lookup"><span data-stu-id="a850c-1838">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="a850c-1839">Lade till det nya kommandot "Test-AzServiceBusNameAvailability" för att kontrollera namntillgängligheten för kö och ämne</span><span class="sxs-lookup"><span data-stu-id="a850c-1839">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a850c-1840">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a850c-1840">Az.ServiceFabric</span></span>
* <span data-ttu-id="a850c-1841">Åtgärda buggar med tillägg av nodtyps-cmdlet:</span><span class="sxs-lookup"><span data-stu-id="a850c-1841">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="a850c-1842">NullReferenceException-bugg när resursgrupp hade annan vmss som inte är relaterad till Service Fabric-klustret.</span><span class="sxs-lookup"><span data-stu-id="a850c-1842">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="a850c-1843">Åtgärdar problemet: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="a850c-1843">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="a850c-1844">Åtgärda bugg där cmdleten misslyckades om virtualNetwork var i en annan resursgrupp än klustret.</span><span class="sxs-lookup"><span data-stu-id="a850c-1844">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="a850c-1845">Åtgärdar problemet: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="a850c-1845">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="a850c-1846">AzServiceFabricApplicationCertificate-cmdleten görs inaktuell</span><span class="sxs-lookup"><span data-stu-id="a850c-1846">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="a850c-1847">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a850c-1847">Az.Sql</span></span>
* <span data-ttu-id="a850c-1848">Uppdatera dokumentation om gamla gransknings-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="a850c-1848">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a850c-1849">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a850c-1849">Az.Storage</span></span>
* <span data-ttu-id="a850c-1850">Uppdatera hjälpen för Get/Close-AzStorageFileHandle genom att lägga till fler scenarier i cmdlet-exempel och uppdatera parameterbeskrivningar</span><span class="sxs-lookup"><span data-stu-id="a850c-1850">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="a850c-1851">Stöd för StandardBlobTier i uppladdningsblob och kopieringsblob</span><span class="sxs-lookup"><span data-stu-id="a850c-1851">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="a850c-1852">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="a850c-1852">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="a850c-1853">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="a850c-1853">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="a850c-1854">Stöd för rehydratiseringsprioritet i kopieringsblob</span><span class="sxs-lookup"><span data-stu-id="a850c-1854">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="a850c-1855">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="a850c-1855">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a850c-1856">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a850c-1856">Az.Websites</span></span>
* <span data-ttu-id="a850c-1857">Lägg till klargöranden gällande parametern -AppSettings i Set-AzWebApp och Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a850c-1857">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="a850c-1858">2.5.0 – July 2019</span><span class="sxs-lookup"><span data-stu-id="a850c-1858">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a850c-1859">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a850c-1859">Az.Accounts</span></span>
* <span data-ttu-id="a850c-1860">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="a850c-1860">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="a850c-1861">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="a850c-1861">Az.ApplicationInsights</span></span>
* <span data-ttu-id="a850c-1862">Korrigera skrivfel i exempel i dokumentationen för Remove-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="a850c-1862">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a850c-1863">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a850c-1863">Az.Automation</span></span>
* <span data-ttu-id="a850c-1864">Korrigera skrivfel i resurssträng</span><span class="sxs-lookup"><span data-stu-id="a850c-1864">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="a850c-1865">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a850c-1865">Az.CognitiveServices</span></span>
* <span data-ttu-id="a850c-1866">Stöd för NetworkRuleSet har lagts till.</span><span class="sxs-lookup"><span data-stu-id="a850c-1866">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a850c-1867">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a850c-1867">Az.Compute</span></span>
* <span data-ttu-id="a850c-1868">Lägg till saknade egenskaper (ComputerName, OsName, OsVersion och HyperVGeneration) för visningsobjekt i den virtuella datorinstansen.</span><span class="sxs-lookup"><span data-stu-id="a850c-1868">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="a850c-1869">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a850c-1869">Az.ContainerRegistry</span></span>
* <span data-ttu-id="a850c-1870">Åtgärda skrivfel i Remove-AzContainerRegistryReplication för parametern Replication</span><span class="sxs-lookup"><span data-stu-id="a850c-1870">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="a850c-1871">Mer information finns här: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="a850c-1871">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a850c-1872">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a850c-1872">Az.DataFactory</span></span>
* <span data-ttu-id="a850c-1873">ADF .Net SDK-versionen har uppdaterats till 4.1.0</span><span class="sxs-lookup"><span data-stu-id="a850c-1873">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="a850c-1874">Korrigera skrivfel i dokumentationen för Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="a850c-1874">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="a850c-1875">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a850c-1875">Az.EventHub</span></span>
* <span data-ttu-id="a850c-1876">Ny cmmdlet har lagts till för att skapa SAS-token: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="a850c-1876">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="a850c-1877">verifierings- och felmeddelande har lagts till för authorizationrules-rättigheter om endast "hantera" har tilldelats</span><span class="sxs-lookup"><span data-stu-id="a850c-1877">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a850c-1878">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a850c-1878">Az.KeyVault</span></span>
* <span data-ttu-id="a850c-1879">Stöd har lagts till för att ange KeySize för certifikatprinciper</span><span class="sxs-lookup"><span data-stu-id="a850c-1879">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="a850c-1880">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="a850c-1880">Az.LogicApp</span></span>
* <span data-ttu-id="a850c-1881">Korrigering för Get-AzIntegrationAccountMap för att lista alla mappningstyper</span><span class="sxs-lookup"><span data-stu-id="a850c-1881">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="a850c-1882">Ny MapType-parameter har lagts till för filtrering</span><span class="sxs-lookup"><span data-stu-id="a850c-1882">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="a850c-1883">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="a850c-1883">Az.ManagedServices</span></span>
* <span data-ttu-id="a850c-1884">Stöd för API-versionen 2019-06-01 (GA) har lagts till</span><span class="sxs-lookup"><span data-stu-id="a850c-1884">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a850c-1885">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a850c-1885">Az.Network</span></span>
* <span data-ttu-id="a850c-1886">Lägg till stöd för privat slutpunkt och privat länktjänst</span><span class="sxs-lookup"><span data-stu-id="a850c-1886">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="a850c-1887">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="a850c-1887">New cmdlets</span></span>
        - <span data-ttu-id="a850c-1888">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="a850c-1888">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="a850c-1889">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="a850c-1889">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="a850c-1890">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a850c-1890">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="a850c-1891">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a850c-1891">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="a850c-1892">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a850c-1892">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="a850c-1893">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a850c-1893">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="a850c-1894">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="a850c-1894">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="a850c-1895">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="a850c-1895">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="a850c-1896">Nedanstående kommandon för funktionen har uppdaterats: Flaggan PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies på undernätet i VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a850c-1896">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="a850c-1897">Uppdaterade New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="a850c-1897">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="a850c-1898">Valfri parameter har lagts till – PrivateEndpointNetworkPoliciesFlag som konfigurerar huruvida nätverksprinciper ska tillämpas på en privat slutpunkt i det här undernätet.</span><span class="sxs-lookup"><span data-stu-id="a850c-1898">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="a850c-1899">Valfri parameter har lagts till – PrivateLinkServiceNetworkPoliciesFlag som konfigurerar huruvida nätverksprinciper ska tillämpas på en privat länktjänst i det här undernätet.</span><span class="sxs-lookup"><span data-stu-id="a850c-1899">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="a850c-1900">AzPrivateLinkService för cmdlet-parametern ServiceName har bytt namn till Name med aliaset ServiceName för bakåtkompatibilitet</span><span class="sxs-lookup"><span data-stu-id="a850c-1900">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="a850c-1901">Aktivera ICMP-protokoll för konfiguration av nätverkssäkerhetsregler</span><span class="sxs-lookup"><span data-stu-id="a850c-1901">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="a850c-1902">Uppdaterade cmdletar</span><span class="sxs-lookup"><span data-stu-id="a850c-1902">Updated cmdlets</span></span>
        - <span data-ttu-id="a850c-1903">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a850c-1903">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="a850c-1904">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a850c-1904">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="a850c-1905">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a850c-1905">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="a850c-1906">Lägg till ConnectionProtocolType (Ikev1/Ikev2) som en konfigurerbar parameter för New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="a850c-1906">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="a850c-1907">Lägg till PrivateIpAddressVersion i LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="a850c-1907">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="a850c-1908">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="a850c-1908">Updated cmdlet:</span></span>
        - <span data-ttu-id="a850c-1909">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="a850c-1909">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="a850c-1910">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="a850c-1910">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="a850c-1911">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="a850c-1911">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="a850c-1912">Uppdatering av Application Gateway-kommandot New-AzApplicationGatewayProbeConfig för stöd av anpassad port i Probe</span><span class="sxs-lookup"><span data-stu-id="a850c-1912">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="a850c-1913">Uppdaterade New-AzApplicationGatewayProbeConfig: Den valfria parametern Port som används för avsökning i serverdelen har lagts till.</span><span class="sxs-lookup"><span data-stu-id="a850c-1913">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="a850c-1914">Denna parameter gäller för SKU:erna Standard_V2 och WAF_V2.</span><span class="sxs-lookup"><span data-stu-id="a850c-1914">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="a850c-1915">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a850c-1915">Az.OperationalInsights</span></span>
* <span data-ttu-id="a850c-1916">Uppdaterade standardversionen för sparade sökningar till 1.</span><span class="sxs-lookup"><span data-stu-id="a850c-1916">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="a850c-1917">Åtgärdade hantering av anpassad log null regex</span><span class="sxs-lookup"><span data-stu-id="a850c-1917">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a850c-1918">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a850c-1918">Az.RecoveryServices</span></span>
* <span data-ttu-id="a850c-1919">Uppdatera Get-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="a850c-1919">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="a850c-1920">Uppdatera Get-AzRecoveryServicesBackupContainer.md</span><span class="sxs-lookup"><span data-stu-id="a850c-1920">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="a850c-1921">Uppdatera Get-AzRecoveryServicesVault.md</span><span class="sxs-lookup"><span data-stu-id="a850c-1921">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="a850c-1922">Uppdatera Wait-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="a850c-1922">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="a850c-1923">Uppdatera Set-AzRecoveryServicesVaultContext.md</span><span class="sxs-lookup"><span data-stu-id="a850c-1923">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="a850c-1924">Uppdatera Get-AzRecoveryServicesBackupItem.md</span><span class="sxs-lookup"><span data-stu-id="a850c-1924">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="a850c-1925">Uppdatera Get-AzRecoveryServicesBackupRecoveryPoint.md</span><span class="sxs-lookup"><span data-stu-id="a850c-1925">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="a850c-1926">Uppdatera Restore-AzRecoveryServicesBackupItem.md</span><span class="sxs-lookup"><span data-stu-id="a850c-1926">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="a850c-1927">Uppdaterat tjänstanrop för avregistrering av container för Azure-filresurs</span><span class="sxs-lookup"><span data-stu-id="a850c-1927">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="a850c-1928">Uppdatera Set-AzRecoveryServicesAsrAlertSetting.md</span><span class="sxs-lookup"><span data-stu-id="a850c-1928">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="a850c-1929">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a850c-1929">Az.Resources</span></span>
- <span data-ttu-id="a850c-1930">Ta bort den cmdlet som saknas och som refereras i dokumentationen till New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a850c-1930">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="a850c-1931">Princip-cmdletar har uppdaterats så att de använder den nya API-versionen 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="a850c-1931">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="a850c-1932">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a850c-1932">Az.ServiceBus</span></span>
* <span data-ttu-id="a850c-1933">Ny cmmdlet har lagts till för att skapa SAS-token: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="a850c-1933">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="a850c-1934">verifierings- och felmeddelande har lagts till för authorizationrules-rättigheter om endast "hantera" har tilldelats</span><span class="sxs-lookup"><span data-stu-id="a850c-1934">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="a850c-1935">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a850c-1935">Az.Sql</span></span>
* <span data-ttu-id="a850c-1936">Åtgärda saknade exempel för Set-AzSqlDatabaseSecondary cmdlet</span><span class="sxs-lookup"><span data-stu-id="a850c-1936">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="a850c-1937">Åtgärda angivna återkommande genomsökningar för bedömning av säkerhetsrisk utan angivna e-postadresser</span><span class="sxs-lookup"><span data-stu-id="a850c-1937">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="a850c-1938">Korrigera ett skrivfel i ett varningsmeddelande.</span><span class="sxs-lookup"><span data-stu-id="a850c-1938">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a850c-1939">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a850c-1939">Az.Storage</span></span>
* <span data-ttu-id="a850c-1940">Uppdatera exempel i referensdokumentationen för Get-AzStorageAccount så att rätt parameternamn används</span><span class="sxs-lookup"><span data-stu-id="a850c-1940">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="a850c-1941">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="a850c-1941">Az.StorageSync</span></span>
* <span data-ttu-id="a850c-1942">Lägger till cmdleten Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="a850c-1942">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="a850c-1943">Åtgärda problem 9551 så att TierFilesOlderThanDays föredras</span><span class="sxs-lookup"><span data-stu-id="a850c-1943">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a850c-1944">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a850c-1944">Az.Websites</span></span>
* <span data-ttu-id="a850c-1945">Åtgärdar ett fel där vissa SiteConfig-egenskaper inte returnerades av Get-AzWebApp och Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a850c-1945">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="a850c-1946">Lägger till en ny platsparameter för Get-AzDeletedWebApp och Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="a850c-1946">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="a850c-1947">Åtgärdar ett fel i kloning av webbapp-platser som använder New-AzWebApp-IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="a850c-1947">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="a850c-1948">2.4.0 – juli 2019</span><span class="sxs-lookup"><span data-stu-id="a850c-1948">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a850c-1949">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a850c-1949">Az.Accounts</span></span>
* <span data-ttu-id="a850c-1950">Lägg till stöd för profil-cmdletar</span><span class="sxs-lookup"><span data-stu-id="a850c-1950">Add support for profile cmdlets</span></span>
* <span data-ttu-id="a850c-1951">Lägg till stöd för miljöer och dataplaner i genererade cmdletar</span><span class="sxs-lookup"><span data-stu-id="a850c-1951">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="a850c-1952">Åtgärda bugg där fel slutpunkt i vissa fall användes för cmdletar för dataplaner i Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="a850c-1952">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="a850c-1953">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="a850c-1953">Az.Advisor</span></span>
* <span data-ttu-id="a850c-1954">GA-version av Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="a850c-1954">GA release of Az.Advisor</span></span>
* <span data-ttu-id="a850c-1955">Den här modulen ingår nu som en del av `Az`-sammanslagningsmodulen</span><span class="sxs-lookup"><span data-stu-id="a850c-1955">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="a850c-1956">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a850c-1956">Az.ApiManagement</span></span>
* <span data-ttu-id="a850c-1957">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="a850c-1957">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="a850c-1958">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="a850c-1958">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="a850c-1959">Stöd för att fråga prenumerationer efter användare och produkt har lagts till</span><span class="sxs-lookup"><span data-stu-id="a850c-1959">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="a850c-1960">Stöd för att fråga med hjälp av omfång ”/”, ”/apis”, ”/apis/echo-api” har lagts till</span><span class="sxs-lookup"><span data-stu-id="a850c-1960">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="a850c-1961">Korrigering av problem https://github.com/Azure/azure-powershell/issues/9307 och https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="a850c-1961">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="a850c-1962">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="a850c-1962">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="a850c-1963">Stöd för att ange ”ApiVersion” och ”ApiVersionSetId” när API:er importeras har lagts till</span><span class="sxs-lookup"><span data-stu-id="a850c-1963">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a850c-1964">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a850c-1964">Az.Automation</span></span>
* <span data-ttu-id="a850c-1965">Bugg med cmdleten Set-AzAutomationConnectionFieldValue för att hantera strängvärde har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="a850c-1965">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a850c-1966">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a850c-1966">Az.Compute</span></span>
* <span data-ttu-id="a850c-1967">Lägg till parametern HyperVGeneration i New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="a850c-1967">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a850c-1968">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a850c-1968">Az.DataFactory</span></span>
* <span data-ttu-id="a850c-1969">Uppdaterar utdata från ADF-cmdletar som hämtar aktivitetskörningar, hämtar pipelinekörningar och hämtar utlösarkörningar för stöd för Select-Object-pipe.</span><span class="sxs-lookup"><span data-stu-id="a850c-1969">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="a850c-1970">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="a850c-1970">Az.EventGrid</span></span>
* <span data-ttu-id="a850c-1971">Korrigera stavfel i dokumentation om ”New-AzEventGridSubscription”</span><span class="sxs-lookup"><span data-stu-id="a850c-1971">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a850c-1972">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a850c-1972">Az.IotHub</span></span>
* <span data-ttu-id="a850c-1973">Lägg till stöd för att återskapa principnycklar för auktorisering.</span><span class="sxs-lookup"><span data-stu-id="a850c-1973">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a850c-1974">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a850c-1974">Az.Network</span></span>
* <span data-ttu-id="a850c-1975">”RoutingPreference” har lagts till i offentliga IP-taggar</span><span class="sxs-lookup"><span data-stu-id="a850c-1975">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="a850c-1976">Förbättra exempel för referensdokumentation om ”Get-AzNetworkServiceTag”</span><span class="sxs-lookup"><span data-stu-id="a850c-1976">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="a850c-1977">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a850c-1977">Az.PolicyInsights</span></span>
* <span data-ttu-id="a850c-1978">Åtgärda problem med null-referens i Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="a850c-1978">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="a850c-1979">Mer information här: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="a850c-1979">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="a850c-1980">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a850c-1980">Az.OperationalInsights</span></span>
* <span data-ttu-id="a850c-1981">Modellen för CustomLog-datakälla som returneras i Get-AzOperationalInsightsDataSource har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="a850c-1981">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a850c-1982">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a850c-1982">Az.RecoveryServices</span></span>
* <span data-ttu-id="a850c-1983">Kommandot get-policy för IaaSVM:er har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="a850c-1983">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="a850c-1984">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a850c-1984">Az.Resources</span></span>
    - <span data-ttu-id="a850c-1985">Korrigera hjälptext för den översta parametern i Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="a850c-1985">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="a850c-1986">Lägg till växlingsstöd på klientsidan för Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="a850c-1986">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="a850c-1987">Lägg till nya parametrar för Set-AzPolicyAssignment, -PolicyParameters och -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="a850c-1987">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="a850c-1988">En mängd dokument- och exempeluppdateringar för Policy-cmdletar</span><span class="sxs-lookup"><span data-stu-id="a850c-1988">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="a850c-1989">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a850c-1989">Az.ServiceBus</span></span>
* <span data-ttu-id="a850c-1990">Korrigering av problem #4938 – New-AzureRmServiceBusQueue returnerar BadRequest vid konfiguration av MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="a850c-1990">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="a850c-1991">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a850c-1991">Az.Sql</span></span>
* <span data-ttu-id="a850c-1992">Lägg till cmdletar för instansredundansgrupper från förhandsversion till offentlig version</span><span class="sxs-lookup"><span data-stu-id="a850c-1992">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="a850c-1993">Stöd för granskning för Azure SQL Server\Database med nya cmdletar.</span><span class="sxs-lookup"><span data-stu-id="a850c-1993">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="a850c-1994">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="a850c-1994">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="a850c-1995">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="a850c-1995">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="a850c-1996">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="a850c-1996">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="a850c-1997">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="a850c-1997">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="a850c-1998">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="a850c-1998">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="a850c-1999">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="a850c-1999">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="a850c-2000">Ta bort begränsningar för e-post från inställningarna för sårbarhetsbedömning</span><span class="sxs-lookup"><span data-stu-id="a850c-2000">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a850c-2001">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a850c-2001">Az.Storage</span></span>
* <span data-ttu-id="a850c-2002">Ändra två parametrar ”-IndexDocument” och ”-ErrorDocument404Path” från ”krävs” till ”valfri” i cmdlet:</span><span class="sxs-lookup"><span data-stu-id="a850c-2002">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="a850c-2003">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="a850c-2003">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="a850c-2004">Uppdatera hjälpen för Get-AzStorageBlobContent genom att lägga till ett exempel</span><span class="sxs-lookup"><span data-stu-id="a850c-2004">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="a850c-2005">Visa mer felinformation när cmdleten misslyckas med StorageException</span><span class="sxs-lookup"><span data-stu-id="a850c-2005">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="a850c-2006">Stöd för att skapa eller uppdatera lagringskonto med Azure Files AAD DS-autentisering</span><span class="sxs-lookup"><span data-stu-id="a850c-2006">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="a850c-2007">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a850c-2007">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="a850c-2008">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a850c-2008">Set-AzStorageAccount</span></span>
* <span data-ttu-id="a850c-2009">Stöd för att lista eller stänga filreferenser för en filresurs, filkatalog eller en fil</span><span class="sxs-lookup"><span data-stu-id="a850c-2009">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="a850c-2010">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="a850c-2010">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="a850c-2011">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="a850c-2011">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="a850c-2012">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="a850c-2012">Az.StorageSync</span></span>
* <span data-ttu-id="a850c-2013">Den här modulen ingår nu som en del av `Az`-sammanslagningsmodulen</span><span class="sxs-lookup"><span data-stu-id="a850c-2013">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="a850c-2014">2.3.2 – juni 2019</span><span class="sxs-lookup"><span data-stu-id="a850c-2014">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a850c-2015">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a850c-2015">Az.Accounts</span></span>
* <span data-ttu-id="a850c-2016">Åtgärda bugg med felaktiga webbadresser som i vissa fall användes för Functions-anrop</span><span class="sxs-lookup"><span data-stu-id="a850c-2016">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="a850c-2017">Mer information här: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="a850c-2017">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="a850c-2018">Åtgärda problem med alias från AzureRM i Az-cmdletar</span><span class="sxs-lookup"><span data-stu-id="a850c-2018">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="a850c-2019">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="a850c-2019">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="a850c-2020">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="a850c-2020">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a850c-2021">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a850c-2021">Az.Compute</span></span>
* <span data-ttu-id="a850c-2022">Parameteruppsättningarna New-AzVm och New-AzVmss accepterar nu parametern ”ProximityPlacementGroup”.</span><span class="sxs-lookup"><span data-stu-id="a850c-2022">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="a850c-2023">Stavfel i referensdokumentationen för ”New-AzVM” har korrigerats</span><span class="sxs-lookup"><span data-stu-id="a850c-2023">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="a850c-2024">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="a850c-2024">Az.Dns</span></span>
* <span data-ttu-id="a850c-2025">Stavfel i hjälpexempel för ”Set-AzDnsZone” har korrigerats.</span><span class="sxs-lookup"><span data-stu-id="a850c-2025">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="a850c-2026">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="a850c-2026">Az.EventGrid</span></span>
* <span data-ttu-id="a850c-2027">Har uppdaterats för att använda API-versionen 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="a850c-2027">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="a850c-2028">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="a850c-2028">New cmdlets:</span></span>
    - <span data-ttu-id="a850c-2029">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="a850c-2029">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="a850c-2030">Skapar en ny Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="a850c-2030">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="a850c-2031">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="a850c-2031">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="a850c-2032">Hämtar information om en Event Grid-domän eller hämtar en lista med alla Event Grid-domäner i den aktuella Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="a850c-2032">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="a850c-2033">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="a850c-2033">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="a850c-2034">Tar bort en Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="a850c-2034">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="a850c-2035">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="a850c-2035">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="a850c-2036">Återskapar nyckeln för delad åtkomst för en Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="a850c-2036">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="a850c-2037">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="a850c-2037">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="a850c-2038">Hämtar de nycklar för delad åtkomst som används för att publicera händelser till en Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="a850c-2038">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="a850c-2039">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="a850c-2039">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="a850c-2040">Skapar ett nytt Azure Event Grid-domänämne.</span><span class="sxs-lookup"><span data-stu-id="a850c-2040">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="a850c-2041">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="a850c-2041">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="a850c-2042">Hämtar information om ett Event Grid-domänämne eller hämtar en lista med alla Event Grid-domänämnen under en specifik Event Grid-domän i nuvarande Azure</span><span class="sxs-lookup"><span data-stu-id="a850c-2042">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="a850c-2043">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="a850c-2043">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="a850c-2044">Tar bort ett befintligt Azure Event Grid-domänämne.</span><span class="sxs-lookup"><span data-stu-id="a850c-2044">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="a850c-2045">Uppdaterade cmdletar:</span><span class="sxs-lookup"><span data-stu-id="a850c-2045">Updated cmdlets:</span></span>
    - <span data-ttu-id="a850c-2046">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="a850c-2046">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="a850c-2047">Lägg till nya obligatoriska parametrar för att stödja piping för den nya Event Grid-domänen och Event Grid-domänämnet för att göra det möjligt att skapa nya händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="a850c-2047">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="a850c-2048">Lägg till nya obligatoriska parametrar för att ange det nya Event Grid-domännamnet och/eller namnet på Event Grid-domänämnet för att göra det möjligt att skapa nya händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="a850c-2048">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="a850c-2049">Lägg till ny parameteruppsättningar för domäner och domänämnen för att göra det möjligt att återanvända befintliga parametrar (t.ex. EndPointType, SubjectBeginsWith osv).</span><span class="sxs-lookup"><span data-stu-id="a850c-2049">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="a850c-2050">Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="a850c-2050">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="a850c-2051">Förfallodatum för händelseprenumeration</span><span class="sxs-lookup"><span data-stu-id="a850c-2051">Event subscription expiration date,</span></span>
            - <span data-ttu-id="a850c-2052">Avancerade filterparametrar.</span><span class="sxs-lookup"><span data-stu-id="a850c-2052">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="a850c-2053">Lägg till ny uppräkning för servicebusqueue som mål.</span><span class="sxs-lookup"><span data-stu-id="a850c-2053">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="a850c-2054">Tillåt inte användning av ”Alla” i alternativet -IncludedEventType och ersätt det med</span><span class="sxs-lookup"><span data-stu-id="a850c-2054">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="a850c-2055">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="a850c-2055">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="a850c-2056">Lägg till ny valfria parametrar (Top, ODataQuery och NextLink) för att stödja sidnumrering och filtrering av resultat.</span><span class="sxs-lookup"><span data-stu-id="a850c-2056">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="a850c-2057">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="a850c-2057">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="a850c-2058">Lägg till nya obligatoriska parametrar för att stödja piping för en Event Grid-domän och Event Grid-domänämnen för att göra det möjligt att ta bort befintliga händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="a850c-2058">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="a850c-2059">Lägg till nya obligatoriska parametrar för att ange Event Grid-domännamnet och/eller namnet på Event Grid-domänämnet för att göra det möjligt att ta bort befintliga händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="a850c-2059">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="a850c-2060">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="a850c-2060">Az.FrontDoor</span></span>
* <span data-ttu-id="a850c-2061">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="a850c-2061">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="a850c-2062">Lägg till stöd för transformeringar och nytt värde för automatisk komplettering för operatorer (RegEx)</span><span class="sxs-lookup"><span data-stu-id="a850c-2062">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="a850c-2063">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="a850c-2063">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="a850c-2064">Lägg till nya värden för automatisk komplettering</span><span class="sxs-lookup"><span data-stu-id="a850c-2064">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a850c-2065">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a850c-2065">Az.Network</span></span>
* <span data-ttu-id="a850c-2066">Lägg till stöd för resurs för virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="a850c-2066">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="a850c-2067">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="a850c-2067">New cmdlets</span></span>
        - <span data-ttu-id="a850c-2068">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="a850c-2068">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="a850c-2069">Lägg till AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="a850c-2069">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="a850c-2070">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="a850c-2070">New cmdlets</span></span>
        - <span data-ttu-id="a850c-2071">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="a850c-2071">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="a850c-2072">Lägg till PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="a850c-2072">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="a850c-2073">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="a850c-2073">New cmdlets</span></span>
        - <span data-ttu-id="a850c-2074">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="a850c-2074">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="a850c-2075">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="a850c-2075">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="a850c-2076">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="a850c-2076">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="a850c-2077">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="a850c-2077">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="a850c-2078">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a850c-2078">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="a850c-2079">Lägg till PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="a850c-2079">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="a850c-2080">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="a850c-2080">New cmdlets</span></span>
        - <span data-ttu-id="a850c-2081">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="a850c-2081">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="a850c-2082">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="a850c-2082">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="a850c-2083">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="a850c-2083">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="a850c-2084">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="a850c-2084">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="a850c-2085">Nedanstående kommandon för funktionen har uppdaterats: Flaggan UseLocalAzureIpAddress på VpnConnection</span><span class="sxs-lookup"><span data-stu-id="a850c-2085">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="a850c-2086">New-AzVpnConnection har uppdaterats: Den valfria parametern -UseLocalAzureIpAddress har lagts till för att visa att en lokal IP-adress i Azure ska användas som källadress när anslutningen initieras.</span><span class="sxs-lookup"><span data-stu-id="a850c-2086">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="a850c-2087">Set-AzVpnConnection har uppdaterats: Den valfria parametern -UseLocalAzureIpAddress har lagts till för att visa att en lokal IP-adress i Azure ska användas som källadress när anslutningen initieras.</span><span class="sxs-lookup"><span data-stu-id="a850c-2087">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="a850c-2088">Det skrivskyddade fältet PeeredConnections har lagts till i ExpressRoute-peering.</span><span class="sxs-lookup"><span data-stu-id="a850c-2088">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="a850c-2089">Det skrivskyddade fältet GlobalReachEnabled har lagts till i ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="a850c-2089">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="a850c-2090">Ett attribut för icke-bakåtkompatibla ändringar har lagts till för att lyfta fram utfasning av fältet AllowGlobalReach i modellen ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a850c-2090">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="a850c-2091">Problem 8756 har åtgärdats: Fel vid användning av TargetListenerID med AzApplicationGatewayRedirectConfiguration-cmdletar</span><span class="sxs-lookup"><span data-stu-id="a850c-2091">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="a850c-2092">En bugg i New-AzApplicationGatewayPathRuleConfig som gjorde att regeluppsättningen för att återskapa inte kunde anges har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="a850c-2092">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="a850c-2093">Visningen av VirtualNetworkTaps i NetworkInterfaceIpConfiguration har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="a850c-2093">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="a850c-2094">Cortex Get-cmdletar för att visa en lista med alla delar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="a850c-2094">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="a850c-2095">Funktionen för att skapa VirtualHub-referenser för ExpressRouteGateways och VpnGateway har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="a850c-2095">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="a850c-2096">Stöd för tillgänglighetszoner i AzureFirewall och NatGateway har lagts till</span><span class="sxs-lookup"><span data-stu-id="a850c-2096">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="a850c-2097">Cmdleten Get-AzNetworkServiceTag har lagts till</span><span class="sxs-lookup"><span data-stu-id="a850c-2097">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="a850c-2098">Lägg till stöd för flera offentliga IP-adresser för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="a850c-2098">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="a850c-2099">Cmdleten New-AzFirewall har uppdaterats:</span><span class="sxs-lookup"><span data-stu-id="a850c-2099">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="a850c-2100">Parametern -PublicIpAddress som accepterar ett eller flera offentliga IP-adressobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="a850c-2100">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="a850c-2101">Parametern -VirtualNetwork som accepterar ett virtuellt nätverksobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="a850c-2101">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="a850c-2102">Metoderna AddPublicIpAddress och RemovePublicIpAddress har lagts till på brandväggsobjekt – dessa accepterar ett offentligt IP-adressobjekt som indata</span><span class="sxs-lookup"><span data-stu-id="a850c-2102">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="a850c-2103">Inaktuella parametrar -PublicIpName och -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="a850c-2103">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="a850c-2104">Nedanstående kommandon för funktionen har uppdaterats: Ange autentiseringsalternativ för VpnClient AAD till resurser för virtuella nätverksgatewayer.</span><span class="sxs-lookup"><span data-stu-id="a850c-2104">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="a850c-2105">New-AzVirtualNetworkGateway har uppdaterats: De valfria parametrarna AadTenantUri, AadAudienceId och AadIssuerUri för att ange VpnClient AAD-autentiseringsalternativ på en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="a850c-2105">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="a850c-2106">Set-AzVirtualNetworkGateway har uppdaterats: De valfria parametrarna AadTenantUri, AadAudienceId och AadIssuerUri för att ange VpnClient AAD-autentiseringsalternativ på en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="a850c-2106">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="a850c-2107">Set-AzVirtualNetworkGateway har uppdaterats: Den valfria växelparametern RemoveAadAuthentication som tar bort VpnClient AAD-autentiseringsalternativ från en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="a850c-2107">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="a850c-2108">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a850c-2108">Az.OperationalInsights</span></span>
* <span data-ttu-id="a850c-2109">Aktivera prisnivån **pergb2018** i kommandot ”New-AzureRmOperationalInsightsWorkspace”</span><span class="sxs-lookup"><span data-stu-id="a850c-2109">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="a850c-2110">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a850c-2110">Az.Resources</span></span>
* <span data-ttu-id="a850c-2111">Stöd för ytterligare alternativ för att exportera en mall</span><span class="sxs-lookup"><span data-stu-id="a850c-2111">Support for additional Template Export options</span></span>
    - <span data-ttu-id="a850c-2112">Lägg till parametern ”-SkipResourceNameParameterization” till Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a850c-2112">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="a850c-2113">Lägg till parametern ”-SkipAllParameterization” till Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a850c-2113">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="a850c-2114">Lägg till parametern ”-Resource” till Export-AzResourceGroup för exporterad resursfiltrering</span><span class="sxs-lookup"><span data-stu-id="a850c-2114">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a850c-2115">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a850c-2115">Az.ServiceFabric</span></span>
* <span data-ttu-id="a850c-2116">Åtgärda att fel tumavtryck används vid tilläggning av certifikat i ByExistingKeyVault i vissa fall</span><span class="sxs-lookup"><span data-stu-id="a850c-2116">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="a850c-2117">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a850c-2117">Az.Sql</span></span>
* <span data-ttu-id="a850c-2118">Åtgärda suffix för lagringsslutpunkt i Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="a850c-2118">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="a850c-2119">Åtgärda att aktivering av Advanced Data Security åsidosätter Advanced Threat Protection-princip</span><span class="sxs-lookup"><span data-stu-id="a850c-2119">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="a850c-2120">Nya cmdletar för Management.Sql som gör att kunderna kan lägga till nycklar för transparent datakryptering (TDE) och ange TDE-skydd för hanterade instanser</span><span class="sxs-lookup"><span data-stu-id="a850c-2120">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="a850c-2121">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="a850c-2121">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="a850c-2122">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="a850c-2122">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="a850c-2123">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="a850c-2123">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="a850c-2124">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="a850c-2124">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="a850c-2125">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="a850c-2125">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a850c-2126">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a850c-2126">Az.Storage</span></span>
* <span data-ttu-id="a850c-2127">Stöd för typerna FileStorage och SkuName Premium_ZRS när lagringskonton skapas</span><span class="sxs-lookup"><span data-stu-id="a850c-2127">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="a850c-2128">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a850c-2128">New-AzStorageAccount</span></span>
* <span data-ttu-id="a850c-2129">Beskrivningen av cmdleten för bloboföränderlighet har förtydligats</span><span class="sxs-lookup"><span data-stu-id="a850c-2129">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="a850c-2130">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="a850c-2130">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a850c-2131">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a850c-2131">Az.Websites</span></span>
* <span data-ttu-id="a850c-2132">Optimerar Get-AzWebAppCertificate för att filtrera efter resursgrupp på servern i stället för klienten</span><span class="sxs-lookup"><span data-stu-id="a850c-2132">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="a850c-2133">Lägger till växlingsparametern -UseDisasterRecovery till Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="a850c-2133">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="a850c-2134">2.2.0 – juni 2019</span><span class="sxs-lookup"><span data-stu-id="a850c-2134">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="a850c-2135">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="a850c-2135">Az.Cdn</span></span>
* <span data-ttu-id="a850c-2136">Uppdaterade cmdletar för att ge stöd för rulesEngine-funktion baserat på API-version 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="a850c-2136">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a850c-2137">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a850c-2137">Az.Compute</span></span>
* <span data-ttu-id="a850c-2138">Lade till parameter `NoWait` som startar åtgärden och returnerar omedelbart, innan åtgärden har slutförts.</span><span class="sxs-lookup"><span data-stu-id="a850c-2138">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="a850c-2139">Uppdaterade cmdletar:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="a850c-2139">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="a850c-2140">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a850c-2140">Az.EventHub</span></span>
* <span data-ttu-id="a850c-2141">Korrigering för #9231 – Get-AzEventHubNamespace returnerar inga taggar</span><span class="sxs-lookup"><span data-stu-id="a850c-2141">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="a850c-2142">Korrigering för #9230 – Get-AzEventHubNamespace returnerar ResourceGroup istället för ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a850c-2142">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a850c-2143">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a850c-2143">Az.Network</span></span>
* <span data-ttu-id="a850c-2144">Uppdatera ResourceId och InputObject för NAT-gateway</span><span class="sxs-lookup"><span data-stu-id="a850c-2144">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="a850c-2145">Lägg till alias för ResourceId och InputObject</span><span class="sxs-lookup"><span data-stu-id="a850c-2145">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="a850c-2146">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a850c-2146">Az.PolicyInsights</span></span>
* <span data-ttu-id="a850c-2147">Åtgärda Null-referensproblem i Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="a850c-2147">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a850c-2148">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a850c-2148">Az.RecoveryServices</span></span>
* <span data-ttu-id="a850c-2149">Minsta kvarhållning för IaaSVM-policy i dagar ändrat till 7 från 1</span><span class="sxs-lookup"><span data-stu-id="a850c-2149">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="a850c-2150">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a850c-2150">Az.ServiceBus</span></span>
* <span data-ttu-id="a850c-2151">Korrigering för ärende #9182 – Get-AzServiceBusNamespace returnerar ResourceGroup istället för ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a850c-2151">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a850c-2152">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a850c-2152">Az.ServiceFabric</span></span>
* <span data-ttu-id="a850c-2153">Åtgärda stavfel i felmeddelandet för Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="a850c-2153">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="a850c-2154">Åtgärda saknat tecken i Service Fabric-kommandorader</span><span class="sxs-lookup"><span data-stu-id="a850c-2154">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="a850c-2155">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a850c-2155">Az.Sql</span></span>
* <span data-ttu-id="a850c-2156">Lägg till parametern DnsZonePartner för New-AzureSqlInstance-cmdlet för att ge stöd för AutoDr för hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="a850c-2156">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="a850c-2157">Avvecklar cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="a850c-2157">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="a850c-2158">Döp om cmdletar för hotidentifiering till Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="a850c-2158">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="a850c-2159">Parametrarna New-AzSqlInstance -StorageSizeInGB och -LicenseType är nu valfria.</span><span class="sxs-lookup"><span data-stu-id="a850c-2159">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a850c-2160">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a850c-2160">Az.Websites</span></span>
* <span data-ttu-id="a850c-2161">åtgärdar problemet där användningen av Set-AzWebApp och Set-AzWebAppSlot med -WebApp-egenskap tog bort taggarna</span><span class="sxs-lookup"><span data-stu-id="a850c-2161">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="a850c-2162">2.1.0 – maj 2019</span><span class="sxs-lookup"><span data-stu-id="a850c-2162">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="a850c-2163">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a850c-2163">Az.ApiManagement</span></span>
* <span data-ttu-id="a850c-2164">Skapade nya cmdletar för att hantera diagnostik för global- och API-omfång</span><span class="sxs-lookup"><span data-stu-id="a850c-2164">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="a850c-2165">**Get-AzApiManagementDiagnostic** – Skaffa diagnostik konfigurerad för global- eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="a850c-2165">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="a850c-2166">**New-AzApiManagementDiagnostic** – Skapa ny diagnostik för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="a850c-2166">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="a850c-2167">**New-AzApiManagementHttpMessageDiagnostic** – Skapa diagnostikinställning om vilka rubriker som ska loggas och storleken på brödtextbyte</span><span class="sxs-lookup"><span data-stu-id="a850c-2167">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="a850c-2168">**New-AzApiManagementPipelineDiagnosticSetting** – Skapa diagnostikinställningar för inkommande/utgående HTTP-meddelanden till gatewayen.</span><span class="sxs-lookup"><span data-stu-id="a850c-2168">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="a850c-2169">**New-AzApiManagementSamplingSetting** – Skapa samplinginställningar för begäranden/svar för en diagnostik</span><span class="sxs-lookup"><span data-stu-id="a850c-2169">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="a850c-2170">**Remove-AzApiManagementDiagnostic** – Ta bort en diagnostikenhet för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="a850c-2170">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="a850c-2171">**Set-AzApiManagementDiagnostic** – Uppdatera en diagnostikenhet för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="a850c-2171">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="a850c-2172">Skapade nya cmdletar för hantering av cacheminne i ApiManagement-tjänsten</span><span class="sxs-lookup"><span data-stu-id="a850c-2172">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="a850c-2173">**Get-AzApiManagementCache** – Hämta information om cacheminnet som anges av identifierare eller alla cacheminnen</span><span class="sxs-lookup"><span data-stu-id="a850c-2173">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="a850c-2174">**New-AzApiManagementCache** – Skapa ett nytt default-cacheminne eller cacheminne i en viss Azure-region</span><span class="sxs-lookup"><span data-stu-id="a850c-2174">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="a850c-2175">**Remove-AzApiManagementCache** – Ta bort ett cacheminne</span><span class="sxs-lookup"><span data-stu-id="a850c-2175">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="a850c-2176">**Remove-AzApiManagementCache** – Ta bort ett cacheminne</span><span class="sxs-lookup"><span data-stu-id="a850c-2176">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="a850c-2177">Skapade nya cmdletar för hantering av API-schema</span><span class="sxs-lookup"><span data-stu-id="a850c-2177">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="a850c-2178">**New-AzApiManagementSchema** – Skapa ett nytt schema för ett API</span><span class="sxs-lookup"><span data-stu-id="a850c-2178">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="a850c-2179">**Get-AzApiManagementSchema** – Hämta de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="a850c-2179">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="a850c-2180">**Remove-AzApiManagementSchema** – Ta bort de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="a850c-2180">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="a850c-2181">**Set-AzApiManagementSchema** – Uppdatera de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="a850c-2181">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="a850c-2182">Skapa ny cmdlet för att generera en användartoken.</span><span class="sxs-lookup"><span data-stu-id="a850c-2182">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="a850c-2183">**New-AzApiManagementUserToken** – Skapa en ny användartoken som enligt standardinställning är giltig i 8 timmar. Token för GIT-användaren kan skapas med den här cmdleten./</span><span class="sxs-lookup"><span data-stu-id="a850c-2183">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="a850c-2184">Skapade en ny cmdlet för att hämta nätverksstatus</span><span class="sxs-lookup"><span data-stu-id="a850c-2184">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="a850c-2185">**Get-AzApiManagementNetworkStatus** – Hämta nätverksstatusanslutningen för resurserna som API Management-tjänsten är beroende av.</span><span class="sxs-lookup"><span data-stu-id="a850c-2185">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="a850c-2186">Det här är användbart när du distribuerar ApiManagement-tjänsten i ett virtuellt nätverk och validerar om något beroende är brutet.</span><span class="sxs-lookup"><span data-stu-id="a850c-2186">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="a850c-2187">Uppdaterade cmdlet **New-AzApiManagement** för att hantera ApiManagement-tjänsten</span><span class="sxs-lookup"><span data-stu-id="a850c-2187">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="a850c-2188">Lade till stöd för den nya SKU:n Consumption</span><span class="sxs-lookup"><span data-stu-id="a850c-2188">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="a850c-2189">Aktiverade stöd för att slå på flaggan EnableClientCertificate för SKU:n Consumption</span><span class="sxs-lookup"><span data-stu-id="a850c-2189">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="a850c-2190">Den nya cmdleten **New-AzApiManagementSslSetting** gör det möjligt att ställa in TLS/SSL-inställningen på ”Backend” och ”Frontend” (serverdel och klientdel).</span><span class="sxs-lookup"><span data-stu-id="a850c-2190">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="a850c-2191">Det här kan också användas till att konfigurera chiffer som 3DES och ServerProtocols som Http2 för Frontend för en ApiManagement-tjänst.</span><span class="sxs-lookup"><span data-stu-id="a850c-2191">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="a850c-2192">Stöd har lagts till för att konfigurera värdnamnet DeveloperPortal på ApiManagement-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="a850c-2192">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="a850c-2193">Uppdaterade cmdletar **Get-AzApiManagementSsoToken** för att ta PsApiManagement-objekt som indata</span><span class="sxs-lookup"><span data-stu-id="a850c-2193">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="a850c-2194">Uppdaterad cmdleten för att visa infogade felmeddelanden</span><span class="sxs-lookup"><span data-stu-id="a850c-2194">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="a850c-2195">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Felkod: Felmeddelande av typen ValidationError: Ett eller flera fält innehåller felaktiga värden: Felinformation:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="a850c-2195">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="a850c-2196">Uppdaterade cmdlet **Export-AzApiManagementApi** för att exportera API:er i OpenApi 3.0-format</span><span class="sxs-lookup"><span data-stu-id="a850c-2196">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="a850c-2197">Uppdaterade cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="a850c-2197">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="a850c-2198">Importera API från dokumentspecifikationen OpenApi 3.0</span><span class="sxs-lookup"><span data-stu-id="a850c-2198">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="a850c-2199">Om du vill åsidosätta egenskapen PsApiManagementSchema specificerad i ett dokument (Swagger, Wadl, Wsdl, OpenApi).</span><span class="sxs-lookup"><span data-stu-id="a850c-2199">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="a850c-2200">Åsidosätta egenskapen ServiceUrl som specificeras i ett dokument.</span><span class="sxs-lookup"><span data-stu-id="a850c-2200">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="a850c-2201">Uppdaterade cmdlet **Get-AzApiManagementPolicy** för att returnera policy i undantaget format av typen icke-XML med rawxml</span><span class="sxs-lookup"><span data-stu-id="a850c-2201">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="a850c-2202">Uppdaterade cmdlet **Set-AzApiManagementPolicy** för att godkänna policy i undantaget format av typen icke-XML med rawxml och XML undantaget med xml</span><span class="sxs-lookup"><span data-stu-id="a850c-2202">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="a850c-2203">Uppdaterad cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="a850c-2203">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="a850c-2204">Konfigurera API med OpenId auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="a850c-2204">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="a850c-2205">Skapa ett API i ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="a850c-2205">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="a850c-2206">Klona ett API med SourceApiId och SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="a850c-2206">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="a850c-2207">Möjlighet att konfigurera SubscriptionRequired i API-omfattningen.</span><span class="sxs-lookup"><span data-stu-id="a850c-2207">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="a850c-2208">Uppdaterad cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="a850c-2208">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="a850c-2209">Konfigurera API med OpenId auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="a850c-2209">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="a850c-2210">Uppdatera ett API till ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="a850c-2210">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="a850c-2211">Möjlighet att konfigurera SubscriptionRequired i API-omfattningen.</span><span class="sxs-lookup"><span data-stu-id="a850c-2211">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="a850c-2212">Uppdaterad cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="a850c-2212">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="a850c-2213">Klona en befintlig version med hjälp av SourceApiRevision (kopiera taggar, produkter, åtgärder och principer).</span><span class="sxs-lookup"><span data-stu-id="a850c-2213">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="a850c-2214">Den nya revisionen antar ApiId från den överordnade instansen.</span><span class="sxs-lookup"><span data-stu-id="a850c-2214">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="a850c-2215">Tillhandahålla ApiRevisionDescription</span><span class="sxs-lookup"><span data-stu-id="a850c-2215">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="a850c-2216">Åsidosätta ServiceUrl vid kloning av ett API.</span><span class="sxs-lookup"><span data-stu-id="a850c-2216">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="a850c-2217">Uppdaterad cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="a850c-2217">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="a850c-2218">Konfigurera AAD eller AADB2C med en Authority</span><span class="sxs-lookup"><span data-stu-id="a850c-2218">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="a850c-2219">Konfigurera SignupPolicy, SigninPolicy, ProfileEditingPolicy och PasswordResetPolicy</span><span class="sxs-lookup"><span data-stu-id="a850c-2219">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="a850c-2220">Uppdaterad cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="a850c-2220">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="a850c-2221">Kompensera för ny SubscriptonModel med Scope och UserId</span><span class="sxs-lookup"><span data-stu-id="a850c-2221">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="a850c-2222">Kompensera för gammal prenumerationsmodell med ProductId och UserId</span><span class="sxs-lookup"><span data-stu-id="a850c-2222">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="a850c-2223">Lägg till funktion för att aktivera AllowTracing på prenumerationsnivå.</span><span class="sxs-lookup"><span data-stu-id="a850c-2223">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="a850c-2224">Uppdaterad cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="a850c-2224">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="a850c-2225">Kompensera för ny SubscriptonModel med Scope och UserId</span><span class="sxs-lookup"><span data-stu-id="a850c-2225">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="a850c-2226">Kompensera för gammal prenumerationsmodell med ProductId och UserId</span><span class="sxs-lookup"><span data-stu-id="a850c-2226">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="a850c-2227">Lägg till funktion för att aktivera AllowTracing på prenumerationsnivå.</span><span class="sxs-lookup"><span data-stu-id="a850c-2227">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="a850c-2228">Uppdaterade följande cmdletar för att acceptera ResourceId som indata</span><span class="sxs-lookup"><span data-stu-id="a850c-2228">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="a850c-2229">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a850c-2229">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="a850c-2230">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="a850c-2230">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="a850c-2231">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="a850c-2231">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="a850c-2232">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="a850c-2232">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="a850c-2233">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="a850c-2233">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="a850c-2234">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="a850c-2234">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="a850c-2235">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="a850c-2235">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="a850c-2236">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="a850c-2236">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="a850c-2237">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="a850c-2237">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="a850c-2238">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="a850c-2238">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="a850c-2239">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="a850c-2239">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="a850c-2240">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="a850c-2240">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a850c-2241">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a850c-2241">Az.Automation</span></span>
* <span data-ttu-id="a850c-2242">Uppdaterade Get-AzAutomationJobOutputRecord för att hantera postvärden av typen JSON och Text.</span><span class="sxs-lookup"><span data-stu-id="a850c-2242">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="a850c-2243">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="a850c-2243">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="a850c-2244">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="a850c-2244">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="a850c-2245">Ändrade beteende för Start-AzAutomationDscCompilationJob till att bara starta jobbet istället för att vänta på slutförandet.</span><span class="sxs-lookup"><span data-stu-id="a850c-2245">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="a850c-2246">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="a850c-2246">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="a850c-2247">Korrigering för Get-AzAutomationDscNode när using -Name returnerar alla noder.</span><span class="sxs-lookup"><span data-stu-id="a850c-2247">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="a850c-2248">Nu returnerar den endast den matchande noden.</span><span class="sxs-lookup"><span data-stu-id="a850c-2248">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a850c-2249">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a850c-2249">Az.Compute</span></span>
* <span data-ttu-id="a850c-2250">Lägg till parametrarna ProtectFromScaleIn och ProtectFromScaleSetAction i cmdleten Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="a850c-2250">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="a850c-2251">Nu är standardinställningen att vimpelparametern New-AzVM använder en tillgänglig plats om USA, östra inte stöds</span><span class="sxs-lookup"><span data-stu-id="a850c-2251">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a850c-2252">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a850c-2252">Az.DataLakeStore</span></span>
* <span data-ttu-id="a850c-2253">Uppdatera ADLS-sdk för att använda httpclient, integrera dataplanstestning med Azure-ramverk</span><span class="sxs-lookup"><span data-stu-id="a850c-2253">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a850c-2254">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a850c-2254">Az.Monitor</span></span>
* <span data-ttu-id="a850c-2255">Korrigera felaktiga parameternamn i hjälpexempel</span><span class="sxs-lookup"><span data-stu-id="a850c-2255">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a850c-2256">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a850c-2256">Az.Network</span></span>
* <span data-ttu-id="a850c-2257">Lägg till flaggan DisableBgpRoutePropagation i utdata för effektiv routningstabell</span><span class="sxs-lookup"><span data-stu-id="a850c-2257">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="a850c-2258">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="a850c-2258">Updated cmdlet:</span></span>
        - <span data-ttu-id="a850c-2259">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="a850c-2259">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="a850c-2260">Åtgärda dubbelstreck i dokumentationen New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="a850c-2260">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="a850c-2261">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a850c-2261">Az.Resources</span></span>
* <span data-ttu-id="a850c-2262">Lägg till ny cmdlet Get-AzureRmDenyAssignment för att hämta tilldelningsnekanden</span><span class="sxs-lookup"><span data-stu-id="a850c-2262">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="a850c-2263">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a850c-2263">Az.Sql</span></span>
* <span data-ttu-id="a850c-2264">Döp om Advanced Threat Protection-cmdletar för Advanced Data Security och aktivera Vulnerability Assessment som standard</span><span class="sxs-lookup"><span data-stu-id="a850c-2264">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="a850c-2265">2.0.0 – maj 2019</span><span class="sxs-lookup"><span data-stu-id="a850c-2265">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a850c-2266">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a850c-2266">Az.Accounts</span></span>
* <span data-ttu-id="a850c-2267">Uppdatera autentiseringsbiblioteket för att åtgärda ADFS-problem med autentisering av användarnamn/lösenord</span><span class="sxs-lookup"><span data-stu-id="a850c-2267">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="a850c-2268">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a850c-2268">Az.CognitiveServices</span></span>
* <span data-ttu-id="a850c-2269">Visa endast Bing-ansvarsfriskrivning för Bing-sökningstjänster.</span><span class="sxs-lookup"><span data-stu-id="a850c-2269">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="a850c-2270">Förbättra felmeddelande när det inte går att skapa konton.</span><span class="sxs-lookup"><span data-stu-id="a850c-2270">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a850c-2271">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a850c-2271">Az.Compute</span></span>
* <span data-ttu-id="a850c-2272">Funktion för närhetsplaceringsgrupper.</span><span class="sxs-lookup"><span data-stu-id="a850c-2272">Proximity placement group feature.</span></span>
    - <span data-ttu-id="a850c-2273">Följande nya cmdletar har lagts till:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="a850c-2273">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="a850c-2274">Den nya parametern ProximityPlacementGroupId har lagts till i följande cmdletar:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="a850c-2274">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="a850c-2275">Parametern StorageAccountType har lagts till i New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="a850c-2275">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="a850c-2276">TargetRegion för New-AzGalleryImageVersion kan innehålla StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="a850c-2276">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="a850c-2277">Växlingsparametern SkipShutdown har lagts till i Stop-AzVM och Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a850c-2277">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="a850c-2278">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="a850c-2278">Breaking changes</span></span>
    - <span data-ttu-id="a850c-2279">Set-AzVMBootDiagnostics har ändrats till Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="a850c-2279">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="a850c-2280">Export-AzLogAnalyticThrottledRequests har ändrats till Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="a850c-2280">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="a850c-2281">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="a850c-2281">Az.DeploymentManager</span></span>
* <span data-ttu-id="a850c-2282">De första allmänt tillgängliga versionerna av cmdletar för Distributionshanteraren i Azure</span><span class="sxs-lookup"><span data-stu-id="a850c-2282">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="a850c-2283">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="a850c-2283">Az.Dns</span></span>
* <span data-ttu-id="a850c-2284">Automatisk delegering av DNS för NameServer</span><span class="sxs-lookup"><span data-stu-id="a850c-2284">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="a850c-2285">Det överordnade zonnamnet kan användas som ytterligare valfri parameter i cmdleten för att skapa DNS-zoner.</span><span class="sxs-lookup"><span data-stu-id="a850c-2285">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="a850c-2286">Lägger till NS-poster för en nyligen skapad underordnad zon i den överordnade zonen.</span><span class="sxs-lookup"><span data-stu-id="a850c-2286">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="a850c-2287">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="a850c-2287">Az.FrontDoor</span></span>
* <span data-ttu-id="a850c-2288">De första allmänt tillgängliga versionerna av cmdletar för Azure FrontDoor</span><span class="sxs-lookup"><span data-stu-id="a850c-2288">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="a850c-2289">Byt namn på WAF-cmdletar så att de omfattar ”Waf”</span><span class="sxs-lookup"><span data-stu-id="a850c-2289">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="a850c-2290">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a850c-2290">Az.HDInsight</span></span>
* <span data-ttu-id="a850c-2291">Två cmdletar har tagits bort:</span><span class="sxs-lookup"><span data-stu-id="a850c-2291">Removed two cmdlets:</span></span>
    - <span data-ttu-id="a850c-2292">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="a850c-2292">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="a850c-2293">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="a850c-2293">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="a850c-2294">En ny cmdlet har lagts till, Set-AzHDInsightGatewayCredential, som ersätter Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="a850c-2294">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="a850c-2295">Uppdatera cmdleten Get-AzHDInsightJobOutput för att skilja mellan läsarrollen och HDInsight-operatörsrollen:</span><span class="sxs-lookup"><span data-stu-id="a850c-2295">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="a850c-2296">Användare med läsarrollen måste uttryckligen ange parametern ”DefaultStorageAccountKey”, annars uppstår fel.</span><span class="sxs-lookup"><span data-stu-id="a850c-2296">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="a850c-2297">Användare med HDInsight-operatörsrollen påverkas inte.</span><span class="sxs-lookup"><span data-stu-id="a850c-2297">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a850c-2298">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a850c-2298">Az.Monitor</span></span>
* <span data-ttu-id="a850c-2299">Nya cmdletar för SQR API (schemalagd frågeregel)</span><span class="sxs-lookup"><span data-stu-id="a850c-2299">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="a850c-2300">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="a850c-2300">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="a850c-2301">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="a850c-2301">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="a850c-2302">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="a850c-2302">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="a850c-2303">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="a850c-2303">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="a850c-2304">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="a850c-2304">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="a850c-2305">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="a850c-2305">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="a850c-2306">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="a850c-2306">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="a850c-2307">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="a850c-2307">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="a850c-2308">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="a850c-2308">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="a850c-2309">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="a850c-2309">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="a850c-2310">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="a850c-2310">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="a850c-2311">[Mer](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information om SQR API</span><span class="sxs-lookup"><span data-stu-id="a850c-2311">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="a850c-2312">Az.Monitor.md har uppdaterats för att omfatta cmdletar för måttbaserade aviseringsregler i GenV2 (inte klassiska)</span><span class="sxs-lookup"><span data-stu-id="a850c-2312">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a850c-2313">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a850c-2313">Az.Network</span></span>
* <span data-ttu-id="a850c-2314">Lägg till stöd för NAT Gateway-resurs</span><span class="sxs-lookup"><span data-stu-id="a850c-2314">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="a850c-2315">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="a850c-2315">New cmdlets</span></span>
        - <span data-ttu-id="a850c-2316">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="a850c-2316">New-AzNatGateway</span></span>
        - <span data-ttu-id="a850c-2317">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="a850c-2317">Get-AzNatGateway</span></span>
        - <span data-ttu-id="a850c-2318">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="a850c-2318">Set-AzNatGateway</span></span>
        - <span data-ttu-id="a850c-2319">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="a850c-2319">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="a850c-2320">Uppdaterade cmdletar</span><span class="sxs-lookup"><span data-stu-id="a850c-2320">Updated cmdlets</span></span>
        - <span data-ttu-id="a850c-2321">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="a850c-2321">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="a850c-2322">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="a850c-2322">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="a850c-2323">Nedanstående kommandon för funktionen har uppdaterats: Ange/ta bort anpassade vägar på Brooklyn Gateway.</span><span class="sxs-lookup"><span data-stu-id="a850c-2323">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="a850c-2324">New-AzVirtualNetworkGateway har uppdaterats: Den valfria parametern -CustomRoute har lagts till för att ställa in adressprefix som anpassade vägar för att ange gateway.</span><span class="sxs-lookup"><span data-stu-id="a850c-2324">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="a850c-2325">Set-AzVirtualNetworkGateway har uppdaterats: Den valfria parametern -CustomRoute har lagts till för att ange adressprefix som anpassade vägar för att ange gateway.</span><span class="sxs-lookup"><span data-stu-id="a850c-2325">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="a850c-2326">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a850c-2326">Az.PolicyInsights</span></span>
* <span data-ttu-id="a850c-2327">Stöd för att fråga efter information om principutvärdering.</span><span class="sxs-lookup"><span data-stu-id="a850c-2327">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="a850c-2328">Lägg till parametern ”-Expand” för Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="a850c-2328">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="a850c-2329">Stöd för -Expand PolicyEvaluationDetails.</span><span class="sxs-lookup"><span data-stu-id="a850c-2329">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a850c-2330">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a850c-2330">Az.RecoveryServices</span></span>
* <span data-ttu-id="a850c-2331">Stöd för att dela prenumeration mellan Azure och Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="a850c-2331">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="a850c-2332">Markering av kommande icke-bakåtkompatibla ändringar för Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="a850c-2332">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="a850c-2333">Korrigering för återställningsplan och åtgärdsplan i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="a850c-2333">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="a850c-2334">Korrigering för mappning av uppdateringsnätverk i Azure Site Recovery för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="a850c-2334">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="a850c-2335">Korrigering för instruktioner för uppdateringsskydd i Azure Site Recovery för Azure till Azure för hanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="a850c-2335">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="a850c-2336">Andra mindre korrigeringar.</span><span class="sxs-lookup"><span data-stu-id="a850c-2336">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="a850c-2337">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="a850c-2337">Az.Relay</span></span>
* <span data-ttu-id="a850c-2338">Korrigera stavfel i kundriktade meddelanden</span><span class="sxs-lookup"><span data-stu-id="a850c-2338">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="a850c-2339">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a850c-2339">Az.ServiceBus</span></span>
* <span data-ttu-id="a850c-2340">Nya cmdletar har lagts till för NetworkRuleSet för namnområden</span><span class="sxs-lookup"><span data-stu-id="a850c-2340">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a850c-2341">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a850c-2341">Az.Storage</span></span>
* <span data-ttu-id="a850c-2342">Uppgradera till lagringsklientbiblioteket 10.0.1 (namnområdet för alla objekt från detta SDK ändras från ”Microsoft.WindowsAzure.Storage. *till ”Microsoft.Azure.Storage.* ”)</span><span class="sxs-lookup"><span data-stu-id="a850c-2342">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="a850c-2343">Uppgradera till Microsoft.Azure.Management.Storage 11.0.0 för att stödja den nya API-versionen 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="a850c-2343">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="a850c-2344">Standardlagringskontot i Skapa lagringskonto ändras från ”Storage” till ”StorageV2”</span><span class="sxs-lookup"><span data-stu-id="a850c-2344">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="a850c-2345">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a850c-2345">New-AzStorageAccount</span></span>
* <span data-ttu-id="a850c-2346">Ändra lagringskontots cmdlet-utdata Sku.Name för att passa med indata-SkuName genom att lägga till ”-”. Till exempel ändras ”StandardLRS” till ”Standard_LRS”</span><span class="sxs-lookup"><span data-stu-id="a850c-2346">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="a850c-2347">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a850c-2347">New-AzStorageAccount</span></span>
    - <span data-ttu-id="a850c-2348">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a850c-2348">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="a850c-2349">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a850c-2349">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a850c-2350">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a850c-2350">Az.Websites</span></span>
* <span data-ttu-id="a850c-2351">Egenskapen ”typ” konfigureras nu för PSSite-objekt som returneras av Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a850c-2351">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="a850c-2352">Get-AzWebApp\*Metrics och Get-AzAppServicePlanMetrics markeras som inaktuella</span><span class="sxs-lookup"><span data-stu-id="a850c-2352">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="a850c-2353">1.8.0 – april 2019</span><span class="sxs-lookup"><span data-stu-id="a850c-2353">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="a850c-2354">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="a850c-2354">Highlights since the last major release</span></span>
* <span data-ttu-id="a850c-2355">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="a850c-2355">General availability of `Az` module</span></span>
* <span data-ttu-id="a850c-2356">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="a850c-2356">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="a850c-2357">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="a850c-2357">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="a850c-2358">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="a850c-2358">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="a850c-2359">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="a850c-2359">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="a850c-2360">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="a850c-2360">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="a850c-2361">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="a850c-2361">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="a850c-2362">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a850c-2362">Az.Accounts</span></span>
* <span data-ttu-id="a850c-2363">Uppdatera Uninstall-AzureRm för att ta bort moduler i Mac på ett korrekt sätt</span><span class="sxs-lookup"><span data-stu-id="a850c-2363">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="a850c-2364">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="a850c-2364">Az.Batch</span></span>
* <span data-ttu-id="a850c-2365">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="a850c-2365">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="a850c-2366">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="a850c-2366">Az.Cdn</span></span>
* <span data-ttu-id="a850c-2367">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="a850c-2367">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="a850c-2368">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a850c-2368">Az.CognitiveServices</span></span>
* <span data-ttu-id="a850c-2369">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="a850c-2369">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a850c-2370">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a850c-2370">Az.Compute</span></span>
* <span data-ttu-id="a850c-2371">Åtgärda problem med AEM-installationen om resurs-ID:n för diskar innehåller resourcegroups i gemener i resurs-ID:n</span><span class="sxs-lookup"><span data-stu-id="a850c-2371">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="a850c-2372">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="a850c-2372">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="a850c-2373">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="a850c-2373">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a850c-2374">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a850c-2374">Az.DataFactory</span></span>
* <span data-ttu-id="a850c-2375">Lägg till SsisProperties om NodeCount inte är null för hanterad integreringskörning.</span><span class="sxs-lookup"><span data-stu-id="a850c-2375">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a850c-2376">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a850c-2376">Az.DataLakeStore</span></span>
* <span data-ttu-id="a850c-2377">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="a850c-2377">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="a850c-2378">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="a850c-2378">Az.EventGrid</span></span>
* <span data-ttu-id="a850c-2379">Hjälptexten för slutpunkten har uppdaterats för att visa att resurser ska skapas innan cmdletarna för att skapa/uppdatera händelseprenumerationer används.</span><span class="sxs-lookup"><span data-stu-id="a850c-2379">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="a850c-2380">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a850c-2380">Az.EventHub</span></span>
* <span data-ttu-id="a850c-2381">Nya cmdletar har lagts till för NetworkRuleSet för namnområden</span><span class="sxs-lookup"><span data-stu-id="a850c-2381">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="a850c-2382">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a850c-2382">Az.HDInsight</span></span>
* <span data-ttu-id="a850c-2383">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="a850c-2383">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a850c-2384">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a850c-2384">Az.IotHub</span></span>
* <span data-ttu-id="a850c-2385">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="a850c-2385">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a850c-2386">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a850c-2386">Az.KeyVault</span></span>
* <span data-ttu-id="a850c-2387">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="a850c-2387">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="a850c-2388">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="a850c-2388">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="a850c-2389">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="a850c-2389">Az.MachineLearning</span></span>
* <span data-ttu-id="a850c-2390">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="a850c-2390">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="a850c-2391">Az.Media</span><span class="sxs-lookup"><span data-stu-id="a850c-2391">Az.Media</span></span>
* <span data-ttu-id="a850c-2392">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="a850c-2392">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a850c-2393">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a850c-2393">Az.Monitor</span></span>
  * <span data-ttu-id="a850c-2394">Nya cmdletar för måttbaserad aviseringsregel i GenV2 (inte klassisk)</span><span class="sxs-lookup"><span data-stu-id="a850c-2394">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="a850c-2395">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="a850c-2395">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="a850c-2396">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="a850c-2396">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="a850c-2397">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="a850c-2397">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="a850c-2398">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="a850c-2398">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="a850c-2399">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="a850c-2399">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="a850c-2400">Monitor SDK har uppdaterats till version 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="a850c-2400">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a850c-2401">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a850c-2401">Az.Network</span></span>
* <span data-ttu-id="a850c-2402">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="a850c-2402">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="a850c-2403">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="a850c-2403">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="a850c-2404">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="a850c-2404">Az.NotificationHubs</span></span>
* <span data-ttu-id="a850c-2405">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="a850c-2405">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="a850c-2406">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a850c-2406">Az.OperationalInsights</span></span>
* <span data-ttu-id="a850c-2407">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="a850c-2407">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="a850c-2408">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="a850c-2408">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="a850c-2409">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="a850c-2409">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a850c-2410">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a850c-2410">Az.RecoveryServices</span></span>
* <span data-ttu-id="a850c-2411">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="a850c-2411">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="a850c-2412">Tabellformatet för SQL i virtuella Azure-datorer har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="a850c-2412">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="a850c-2413">En alternativ metod för att hämta platser i AzureFileShare har lagts till</span><span class="sxs-lookup"><span data-stu-id="a850c-2413">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="a850c-2414">ScheduleRunDays i SchedulePolicy-objekt har uppdaterats enligt tidszon</span><span class="sxs-lookup"><span data-stu-id="a850c-2414">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="a850c-2415">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="a850c-2415">Az.RedisCache</span></span>
* <span data-ttu-id="a850c-2416">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="a850c-2416">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a850c-2417">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a850c-2417">Az.Resources</span></span>
* <span data-ttu-id="a850c-2418">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="a850c-2418">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="a850c-2419">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a850c-2419">Az.Sql</span></span>
* <span data-ttu-id="a850c-2420">Ersätt Monitor SDK-beroende med vanlig kod</span><span class="sxs-lookup"><span data-stu-id="a850c-2420">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="a850c-2421">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="a850c-2421">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="a850c-2422">Förbättrad process för klassificering av flera kolumner.</span><span class="sxs-lookup"><span data-stu-id="a850c-2422">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="a850c-2423">Inkludera SKU-egenskaper (SKU-namn, serie, kapacitet) i svaret från Get-AzSqlServerServiceObjective och formatera som tabell som standard.</span><span class="sxs-lookup"><span data-stu-id="a850c-2423">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="a850c-2424">Möjlighet att använda Get-AzSqlServerServiceObjective efter plats utan att behöva en redan befintlig server i regionen.</span><span class="sxs-lookup"><span data-stu-id="a850c-2424">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="a850c-2425">Stöd för tidszonsparametern när hanterade instanser skapas.</span><span class="sxs-lookup"><span data-stu-id="a850c-2425">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="a850c-2426">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="a850c-2426">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a850c-2427">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a850c-2427">Az.Websites</span></span>
* <span data-ttu-id="a850c-2428">åtgärdar Set-AzWebApp och Set-AzWebAppSlot så att de inte tar bort taggar vid körning</span><span class="sxs-lookup"><span data-stu-id="a850c-2428">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="a850c-2429">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="a850c-2429">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="a850c-2430">SDK för WebSites har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="a850c-2430">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="a850c-2431">Egenskapen AdminSiteName har tagits bort från PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="a850c-2431">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="a850c-2432">1.7.0 – april 2019</span><span class="sxs-lookup"><span data-stu-id="a850c-2432">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="a850c-2433">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="a850c-2433">Highlights since the last major release</span></span>
* <span data-ttu-id="a850c-2434">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="a850c-2434">General availability of `Az` module</span></span>
* <span data-ttu-id="a850c-2435">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="a850c-2435">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="a850c-2436">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="a850c-2436">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="a850c-2437">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="a850c-2437">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="a850c-2438">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="a850c-2438">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="a850c-2439">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="a850c-2439">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="a850c-2440">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="a850c-2440">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="a850c-2441">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a850c-2441">Az.Accounts</span></span>
* <span data-ttu-id="a850c-2442">Add-AzEnvironment och Set-AzEnvironment har uppdaterats för att godkänna parametern AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="a850c-2442">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="a850c-2443">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a850c-2443">Az.AnalysisServices</span></span>
* <span data-ttu-id="a850c-2444">ServiceClient används i cmdletar för dataplan och den ursprungliga autentiseringslogiken har tagits bort</span><span class="sxs-lookup"><span data-stu-id="a850c-2444">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="a850c-2445">Add-AzureASAccount används för omslutning av Connect-AzAccount för att undvika en icke-bakåtkompatibel ändring</span><span class="sxs-lookup"><span data-stu-id="a850c-2445">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a850c-2446">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a850c-2446">Az.Automation</span></span>
* <span data-ttu-id="a850c-2447">Buggen för cmdleten New-AzAutomationSoftwareUpdateConfiguration för inkluderingar har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="a850c-2447">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="a850c-2448">Nu bör parametern IncludedKbNumber och IncludedPackageNameMask fungera.</span><span class="sxs-lookup"><span data-stu-id="a850c-2448">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="a850c-2449">Felkorrigering för dynamiska grupper i uppdateringshanteringen för azure automation</span><span class="sxs-lookup"><span data-stu-id="a850c-2449">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a850c-2450">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a850c-2450">Az.Compute</span></span>
* <span data-ttu-id="a850c-2451">Lägg till parametern HyperVGeneration i New-AzDiskConfig och New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="a850c-2451">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="a850c-2452">Tillåt att virtuella datorer skapas med galleribilder från andra klientorganisationer.</span><span class="sxs-lookup"><span data-stu-id="a850c-2452">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="a850c-2453">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="a850c-2453">Az.ContainerInstance</span></span>
* <span data-ttu-id="a850c-2454">Ett problem har åtgärdats i parametern -Command för New-AzContainerGroup som lade till ett avslutande tomt argument</span><span class="sxs-lookup"><span data-stu-id="a850c-2454">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a850c-2455">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a850c-2455">Az.DataFactory</span></span>
* <span data-ttu-id="a850c-2456">ADF .Net SDK-versionen har uppdaterats till 3.0.2</span><span class="sxs-lookup"><span data-stu-id="a850c-2456">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="a850c-2457">Cmdleten Set-AzDataFactoryV2 har uppdaterats med extra parametrar för inställningar som rör RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="a850c-2457">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a850c-2458">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a850c-2458">Az.Resources</span></span>
* <span data-ttu-id="a850c-2459">Förbättra hanteringen av providrar för Get-AzResource när parametrarna -ResourceId eller -ResourceGroupName, -Name och -ResourceType tillhandahålls</span><span class="sxs-lookup"><span data-stu-id="a850c-2459">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="a850c-2460">Förbättra felhanteringen för ”Test-AzDeployment” och ”Test-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="a850c-2460">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="a850c-2461">Hantera fel utanför distributionsvalideringen och ta med dem i kommandoutdata istället</span><span class="sxs-lookup"><span data-stu-id="a850c-2461">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="a850c-2462">Mer information här: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="a850c-2462">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="a850c-2463">Lägg till växlingsparametern -IgnoreDynamicParameters till en uppsättning av cmdletar för distribution för att hoppa över fråga i skript och jobbscenarier</span><span class="sxs-lookup"><span data-stu-id="a850c-2463">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="a850c-2464">Mer information här: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="a850c-2464">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="a850c-2465">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a850c-2465">Az.Sql</span></span>
* <span data-ttu-id="a850c-2466">Stöd för dataklassificering av databaser.</span><span class="sxs-lookup"><span data-stu-id="a850c-2466">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a850c-2467">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a850c-2467">Az.Storage</span></span>
* <span data-ttu-id="a850c-2468">Rapportera detaljfel när lagringskontext skapas med parametern -UseConnectedAccount, men utan inloggning på Azure-kontot</span><span class="sxs-lookup"><span data-stu-id="a850c-2468">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="a850c-2469">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="a850c-2469">New-AzStorageContext</span></span>
* <span data-ttu-id="a850c-2470">Stöd för att hantera Blob Service-egenskaper för ett angivet lagringskonto med API:et för hanteringsplan</span><span class="sxs-lookup"><span data-stu-id="a850c-2470">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="a850c-2471">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="a850c-2471">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="a850c-2472">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="a850c-2472">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="a850c-2473">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="a850c-2473">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="a850c-2474">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="a850c-2474">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="a850c-2475">Stöd för -AsJob-cmdletar för att ladda upp och ladda ned blobar och filer</span><span class="sxs-lookup"><span data-stu-id="a850c-2475">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="a850c-2476">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="a850c-2476">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="a850c-2477">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="a850c-2477">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="a850c-2478">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="a850c-2478">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="a850c-2479">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="a850c-2479">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="a850c-2480">1.6.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="a850c-2480">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="a850c-2481">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="a850c-2481">Highlights since the last major release</span></span>
* <span data-ttu-id="a850c-2482">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="a850c-2482">General availability of `Az` module</span></span>
* <span data-ttu-id="a850c-2483">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="a850c-2483">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="a850c-2484">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="a850c-2484">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="a850c-2485">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="a850c-2485">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="a850c-2486">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="a850c-2486">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="a850c-2487">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="a850c-2487">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="a850c-2488">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="a850c-2488">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a850c-2489">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a850c-2489">Az.Automation</span></span>
* <span data-ttu-id="a850c-2490">Azure Automation – ändring av uppdateringshantering för stöd för de nya funktionerna:</span><span class="sxs-lookup"><span data-stu-id="a850c-2490">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="a850c-2491">Dynamisk gruppering</span><span class="sxs-lookup"><span data-stu-id="a850c-2491">Dynamic grouping</span></span>
    * <span data-ttu-id="a850c-2492">För-/efterskrift</span><span class="sxs-lookup"><span data-stu-id="a850c-2492">Pre-Post script</span></span>
    * <span data-ttu-id="a850c-2493">Inställning för omstart</span><span class="sxs-lookup"><span data-stu-id="a850c-2493">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a850c-2494">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a850c-2494">Az.Compute</span></span>
* <span data-ttu-id="a850c-2495">Åtgärda problem med sökvägsmatchning i Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="a850c-2495">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="a850c-2496">Uppdatera Compute-klientbibliotek till 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="a850c-2496">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a850c-2497">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a850c-2497">Az.KeyVault</span></span>
* <span data-ttu-id="a850c-2498">Stöd för jokertecken för KeyVault-cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="a850c-2498">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a850c-2499">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a850c-2499">Az.Network</span></span>
* <span data-ttu-id="a850c-2500">Lägg till stöd för Threat Intelligence för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="a850c-2500">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="a850c-2501">Lägg till resurs för brandväggsprincip på översta nivå och anpassade regler för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="a850c-2501">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a850c-2502">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a850c-2502">Az.RecoveryServices</span></span>
* <span data-ttu-id="a850c-2503">SnapshotRetentionInDays har lagts till i Azure-principen för virtuella datorer för stöd av Instant RP</span><span class="sxs-lookup"><span data-stu-id="a850c-2503">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="a850c-2504">Pipe-stöd för avregistrering av container har lagts till</span><span class="sxs-lookup"><span data-stu-id="a850c-2504">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="a850c-2505">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a850c-2505">Az.Resources</span></span>
* <span data-ttu-id="a850c-2506">Uppdatera stöd för jokertecken för Get-AzResource och Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a850c-2506">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="a850c-2507">Uppdatera autentiseringsuppgifter som används vid allmänna anrop till ARM</span><span class="sxs-lookup"><span data-stu-id="a850c-2507">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="a850c-2508">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a850c-2508">Az.Sql</span></span>
* <span data-ttu-id="a850c-2509">Cmdlet-parametern (ExcludeDetectionType) för Hotidentifiering ändrades från DetectionType till sträng[] för att framtidssäkra den när nya DetectionTypes läggs till, och även för att stödja automatisk ifyllning.</span><span class="sxs-lookup"><span data-stu-id="a850c-2509">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a850c-2510">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a850c-2510">Az.Storage</span></span>
* <span data-ttu-id="a850c-2511">Stöd för att hämta/ange/ta bort hanteringsprincip på ett lagringskonto</span><span class="sxs-lookup"><span data-stu-id="a850c-2511">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="a850c-2512">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="a850c-2512">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="a850c-2513">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="a850c-2513">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="a850c-2514">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="a850c-2514">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="a850c-2515">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="a850c-2515">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="a850c-2516">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="a850c-2516">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="a850c-2517">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="a850c-2517">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a850c-2518">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a850c-2518">Az.Websites</span></span>
* <span data-ttu-id="a850c-2519">Åtgärda fel med ARM-mall som avbryter kloning av alla platser med 'New-AzWebApp -IncludeSourceWebAppSlots'</span><span class="sxs-lookup"><span data-stu-id="a850c-2519">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="a850c-2520">1.5.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="a850c-2520">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a850c-2521">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a850c-2521">Az.Accounts</span></span>
* <span data-ttu-id="a850c-2522">Lägg till kommandot Register-AzModule för stöd för AutoRest-genererade cmdletar</span><span class="sxs-lookup"><span data-stu-id="a850c-2522">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="a850c-2523">Uppdatera exempel för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="a850c-2523">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a850c-2524">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a850c-2524">Az.Automation</span></span>
* <span data-ttu-id="a850c-2525">Problem med att hämta vissa månadsscheman i flera Azure Automation-cmdletar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="a850c-2525">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="a850c-2526">Åtgärda problem med att Get-AzAutomationDscNode bara returnerar de 20 översta noderna.</span><span class="sxs-lookup"><span data-stu-id="a850c-2526">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="a850c-2527">Nu returneras alla noder</span><span class="sxs-lookup"><span data-stu-id="a850c-2527">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="a850c-2528">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="a850c-2528">Az.Cdn</span></span>
* <span data-ttu-id="a850c-2529">Nya Powershell-cmdletar för att aktivera/inaktivera anpassade domän-HTTPS har lagts till och de gamla har gjorts inaktuella</span><span class="sxs-lookup"><span data-stu-id="a850c-2529">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a850c-2530">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a850c-2530">Az.Compute</span></span>
* <span data-ttu-id="a850c-2531">Lägg till stöd för jokertecken för Get-cmdletar</span><span class="sxs-lookup"><span data-stu-id="a850c-2531">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a850c-2532">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a850c-2532">Az.DataFactory</span></span>
* <span data-ttu-id="a850c-2533">ADF .Net SDK-versionen har uppdaterats till 3.0.1</span><span class="sxs-lookup"><span data-stu-id="a850c-2533">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="a850c-2534">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="a850c-2534">Az.LogicApp</span></span>
* <span data-ttu-id="a850c-2535">Åtgärda problemet med att ListWorkflows endast hämtar den första sidan med resultat</span><span class="sxs-lookup"><span data-stu-id="a850c-2535">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a850c-2536">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a850c-2536">Az.Network</span></span>
* <span data-ttu-id="a850c-2537">Lägg till stöd för jokertecken för Network-cmdletar</span><span class="sxs-lookup"><span data-stu-id="a850c-2537">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a850c-2538">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a850c-2538">Az.RecoveryServices</span></span>
* <span data-ttu-id="a850c-2539">Stöd har lagts till för SQL Server i virtuella Azure-datorer</span><span class="sxs-lookup"><span data-stu-id="a850c-2539">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="a850c-2540">SDK-uppdatering</span><span class="sxs-lookup"><span data-stu-id="a850c-2540">SDK Update</span></span>
* <span data-ttu-id="a850c-2541">Get-ProtectableItem-incheckning i VMappContainer har tagits bort</span><span class="sxs-lookup"><span data-stu-id="a850c-2541">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="a850c-2542">Name och ServerName har lagts till som parametrar för Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="a850c-2542">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="a850c-2543">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a850c-2543">Az.Resources</span></span>
* <span data-ttu-id="a850c-2544">Lägg till parametern `-TemplateObject` i cmdletar för distribution</span><span class="sxs-lookup"><span data-stu-id="a850c-2544">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="a850c-2545">Mer information här: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="a850c-2545">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="a850c-2546">Åtgärda problem med piping av resultatet i `Get-AzResource` till `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="a850c-2546">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="a850c-2547">Mer information här: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="a850c-2547">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="a850c-2548">Åtgärda problem med ändring av JSON-datatyp när `Set-AzResource` körs</span><span class="sxs-lookup"><span data-stu-id="a850c-2548">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="a850c-2549">Mer information här: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="a850c-2549">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="a850c-2550">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a850c-2550">Az.Sql</span></span>
* <span data-ttu-id="a850c-2551">AuditingEndpointsCommunicator uppdateras.</span><span class="sxs-lookup"><span data-stu-id="a850c-2551">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="a850c-2552">Åtgärdar beteendet hos ett gränsscenario när nya diagnostikinställningar skapas.</span><span class="sxs-lookup"><span data-stu-id="a850c-2552">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a850c-2553">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a850c-2553">Az.Storage</span></span>
* <span data-ttu-id="a850c-2554">Stöd för BlockBlobStorage när Storage-konto skapas      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a850c-2554">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="a850c-2555">1.4.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="a850c-2555">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="a850c-2556">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a850c-2556">Az.AnalysisServices</span></span>
* <span data-ttu-id="a850c-2557">Inaktuell AddAzureASAccount-cmdlet</span><span class="sxs-lookup"><span data-stu-id="a850c-2557">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a850c-2558">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a850c-2558">Az.Automation</span></span>
* <span data-ttu-id="a850c-2559">Hjälpen för Import-AzAutomationDscNodeConfiguration har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="a850c-2559">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="a850c-2560">Konfigurationsnamnsvalidering har lagts till i cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="a850c-2560">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="a850c-2561">Förbättrad felhantering för cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="a850c-2561">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="a850c-2562">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a850c-2562">Az.CognitiveServices</span></span>
* <span data-ttu-id="a850c-2563">CustomSubdomainName har lagts till som en ny valfri parameter för New-AzCognitiveServicesAccount, som används för att ange underdomän för resursen.</span><span class="sxs-lookup"><span data-stu-id="a850c-2563">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a850c-2564">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a850c-2564">Az.Compute</span></span>
* <span data-ttu-id="a850c-2565">Problemet med ID-parameteruppsättningar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="a850c-2565">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="a850c-2566">Get-AzVMExtension har uppdaterats så att alla installerade tillägg visas om parametern Name inte har angetts</span><span class="sxs-lookup"><span data-stu-id="a850c-2566">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="a850c-2567">Parametrarna Tag och ResourceId har lagts till i cmdleten Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="a850c-2567">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="a850c-2568">Get-AzVmssVM utan instans-ID och med InstanceView kan visa virtuella VMSS-datorer med instansvyn.</span><span class="sxs-lookup"><span data-stu-id="a850c-2568">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a850c-2569">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a850c-2569">Az.DataLakeStore</span></span>
* <span data-ttu-id="a850c-2570">Cmdletar har lagts till för uppräkning och återställning av borttagna objekt i ADL</span><span class="sxs-lookup"><span data-stu-id="a850c-2570">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="a850c-2571">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a850c-2571">Az.EventHub</span></span>
* <span data-ttu-id="a850c-2572">Ny boolesk egenskap SkipEmptyArchives har lagts till i Skip Empty Archives i CaptureDescription-klassen i Eventhub</span><span class="sxs-lookup"><span data-stu-id="a850c-2572">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a850c-2573">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a850c-2573">Az.KeyVault</span></span>
* <span data-ttu-id="a850c-2574">Taggning i Set-AzKeyVaultSecret har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="a850c-2574">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="a850c-2575">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="a850c-2575">Az.LogicApp</span></span>
* <span data-ttu-id="a850c-2576">Grundläggande SKU har lagts till för Integrationskonton</span><span class="sxs-lookup"><span data-stu-id="a850c-2576">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="a850c-2577">XSLT 2.0, XSLT 3.0 och Flytande mappningstyper har lagts till</span><span class="sxs-lookup"><span data-stu-id="a850c-2577">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="a850c-2578">Nya cmdletar för integrationskontosammansättningar</span><span class="sxs-lookup"><span data-stu-id="a850c-2578">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="a850c-2579">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="a850c-2579">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="a850c-2580">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="a850c-2580">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="a850c-2581">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="a850c-2581">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="a850c-2582">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="a850c-2582">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="a850c-2583">Nya cmdletar för batchkonfiguration för integrationskonto</span><span class="sxs-lookup"><span data-stu-id="a850c-2583">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="a850c-2584">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="a850c-2584">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="a850c-2585">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="a850c-2585">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="a850c-2586">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="a850c-2586">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="a850c-2587">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="a850c-2587">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="a850c-2588">Logic App-SDK har uppdaterats till version 4.1.0</span><span class="sxs-lookup"><span data-stu-id="a850c-2588">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a850c-2589">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a850c-2589">Az.Monitor</span></span>
* <span data-ttu-id="a850c-2590">Hjälpen för Get-AzMetric har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="a850c-2590">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a850c-2591">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a850c-2591">Az.Network</span></span>
* <span data-ttu-id="a850c-2592">Hjälpexempel för Add-AzApplicationGatewayCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="a850c-2592">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="a850c-2593">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a850c-2593">Az.OperationalInsights</span></span>
* <span data-ttu-id="a850c-2594">Ytterligare stöd för datakällorna New och Get ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="a850c-2594">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="a850c-2595">Ny ApplicationInsights-typ har lagts till för att ge stöd för ”Get specific” och ”Get all” för ApplicationInsights-datakällor för angiven arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="a850c-2595">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="a850c-2596">Cmdleten New-AzOperationalInsightsApplicationInsightsDataSource har lagts till för att skapa datakälla med angivna parametrar för Application Insights-resurs: subscription Id, resourceGroupName och name.</span><span class="sxs-lookup"><span data-stu-id="a850c-2596">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a850c-2597">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a850c-2597">Az.Resources</span></span>
* <span data-ttu-id="a850c-2598">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="a850c-2598">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="a850c-2599">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="a850c-2599">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="a850c-2600">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="a850c-2600">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="a850c-2601">Fel som gör att KeyCredentials inte kan skapas upprepade gånger har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="a850c-2601">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="a850c-2602">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a850c-2602">Az.Sql</span></span>
* <span data-ttu-id="a850c-2603">Lägg till stöd för hyperskalanivån för SQL DB</span><span class="sxs-lookup"><span data-stu-id="a850c-2603">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="a850c-2604">Ett fel har åtgärdats där återställningen kunde misslyckas på grund av onödiga inställningsegenskaper i restore-förfrågan</span><span class="sxs-lookup"><span data-stu-id="a850c-2604">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a850c-2605">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a850c-2605">Az.Websites</span></span>
* <span data-ttu-id="a850c-2606">Rätt exempel i Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="a850c-2606">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="a850c-2607">1.3.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="a850c-2607">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a850c-2608">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a850c-2608">Az.Accounts</span></span>
* <span data-ttu-id="a850c-2609">Uppdatera till den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="a850c-2609">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="a850c-2610">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a850c-2610">Az.AnalysisServices</span></span>
<span data-ttu-id="a850c-2611">Allmän tillgänglighet för Az.AnalysisServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="a850c-2611">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a850c-2612">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a850c-2612">Az.Compute</span></span>
* <span data-ttu-id="a850c-2613">AEM-tillägg: Lägg till stöd för UltraSSD-, P60-, P70- och P80-diskar</span><span class="sxs-lookup"><span data-stu-id="a850c-2613">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="a850c-2614">Uppdatera hjälpbeskrivning för Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="a850c-2614">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="a850c-2615">Uppdatera hjälpbeskrivning och exempel för Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="a850c-2615">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a850c-2616">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a850c-2616">Az.RecoveryServices</span></span>
<span data-ttu-id="a850c-2617">Allmän tillgänglighet för Az.RecoveryServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="a850c-2617">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a850c-2618">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a850c-2618">Az.Resources</span></span>
* <span data-ttu-id="a850c-2619">Korrigera taggar för resursgrupper</span><span class="sxs-lookup"><span data-stu-id="a850c-2619">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="a850c-2620">Mer information här: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="a850c-2620">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="a850c-2621">Åtgärda problem där `Get-AzureRmRoleAssignment` inte respekterar -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="a850c-2621">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="a850c-2622">Mer information här: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="a850c-2622">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="a850c-2623">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a850c-2623">Az.Sql</span></span>
* <span data-ttu-id="a850c-2624">Lägga till Get/Set-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="a850c-2624">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="a850c-2625">Åtgärda problem där ett nullref-undantag uppstår när du kör SQL-cmdletar och inte är inloggad på ett Azure-konto</span><span class="sxs-lookup"><span data-stu-id="a850c-2625">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="a850c-2626">Åtgärda nullref-undantag i Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="a850c-2626">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="a850c-2627">1.2.1 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="a850c-2627">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a850c-2628">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a850c-2628">Az.Accounts</span></span>
* <span data-ttu-id="a850c-2629">Version med rätt version av autentisering</span><span class="sxs-lookup"><span data-stu-id="a850c-2629">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="a850c-2630">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a850c-2630">Az.AnalysisServices</span></span>
* <span data-ttu-id="a850c-2631">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="a850c-2631">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a850c-2632">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a850c-2632">Az.RecoveryServices</span></span>
* <span data-ttu-id="a850c-2633">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="a850c-2633">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="a850c-2634">1.2.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="a850c-2634">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a850c-2635">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a850c-2635">Az.Accounts</span></span>
* <span data-ttu-id="a850c-2636">Lägga till interaktiv autentisering och autentisering med användarnamn/lösenord för endast Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="a850c-2636">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="a850c-2637">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="a850c-2637">Update incorrect online help URLs</span></span>
* <span data-ttu-id="a850c-2638">Lägga till varningsmeddelande i PS Core för Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="a850c-2638">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="a850c-2639">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="a850c-2639">Az.Aks</span></span>
* <span data-ttu-id="a850c-2640">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="a850c-2640">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a850c-2641">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a850c-2641">Az.Automation</span></span>
* <span data-ttu-id="a850c-2642">Stöd för Python 2-runbookflöden har lagts till</span><span class="sxs-lookup"><span data-stu-id="a850c-2642">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="a850c-2643">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="a850c-2643">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="a850c-2644">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="a850c-2644">Az.Cdn</span></span>
* <span data-ttu-id="a850c-2645">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="a850c-2645">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a850c-2646">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a850c-2646">Az.Compute</span></span>
* <span data-ttu-id="a850c-2647">Lägga till cmdleten Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="a850c-2647">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="a850c-2648">Lägga till TempDisk-parameter i Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a850c-2648">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="a850c-2649">Korrigera varningsmeddelande för New-AzVM</span><span class="sxs-lookup"><span data-stu-id="a850c-2649">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="a850c-2650">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a850c-2650">Az.ContainerRegistry</span></span>
* <span data-ttu-id="a850c-2651">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="a850c-2651">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a850c-2652">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a850c-2652">Az.DataFactory</span></span>
* <span data-ttu-id="a850c-2653">ADF .Net SDK-versionen har uppdaterats till 3.0.0</span><span class="sxs-lookup"><span data-stu-id="a850c-2653">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a850c-2654">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a850c-2654">Az.DataLakeStore</span></span>
* <span data-ttu-id="a850c-2655">Åtgärda problem med ADLS-slutpunkt vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="a850c-2655">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="a850c-2656">Mer information här: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="a850c-2656">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="a850c-2657">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="a850c-2657">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a850c-2658">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a850c-2658">Az.IotHub</span></span>
* <span data-ttu-id="a850c-2659">Lägga till kodningsformat i cmdleten Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="a850c-2659">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a850c-2660">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a850c-2660">Az.KeyVault</span></span>
* <span data-ttu-id="a850c-2661">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="a850c-2661">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a850c-2662">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a850c-2662">Az.Network</span></span>
* <span data-ttu-id="a850c-2663">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="a850c-2663">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="a850c-2664">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a850c-2664">Az.Resources</span></span>
* <span data-ttu-id="a850c-2665">Åtgärda felaktiga exempel i referensdokumentationen ”New-AzADAppCredential” och ”New-AzADSpCredential”</span><span class="sxs-lookup"><span data-stu-id="a850c-2665">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="a850c-2666">Åtgärda problem där sökvägen för parametern ”-TemplateFile” inte omvandlas innan cmdletarna för distribution i resursgruppen körs</span><span class="sxs-lookup"><span data-stu-id="a850c-2666">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="a850c-2667">Az.Resources: Korrigera dokumentationen om standardvärdet för New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="a850c-2667">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="a850c-2668">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="a850c-2668">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="a850c-2669">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="a850c-2669">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="a850c-2670">Åtgärda formateringsproblemet med objektet ”PSResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="a850c-2670">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="a850c-2671">Mer information här: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="a850c-2671">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a850c-2672">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a850c-2672">Az.ServiceFabric</span></span>
* <span data-ttu-id="a850c-2673">Återställ när ett certifikat läggs till i en Virtual Machine Scale Sets-modell men ett undantag genereras. Detta har gjorts för att åtgärda följande fel: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="a850c-2673">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="a850c-2674">Korrigera några felmeddelanden.</span><span class="sxs-lookup"><span data-stu-id="a850c-2674">Fix some error messages.</span></span>
* <span data-ttu-id="a850c-2675">Korrigering av skapande av kluster med ARM-mall som är standard för New-AzServiceFabriCluster som inte fungerade med migrering till Az.</span><span class="sxs-lookup"><span data-stu-id="a850c-2675">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="a850c-2676">Korrigering av tilläggning av kluster/programcertifikat så att endast VM Scale Sets som motsvarar klustret läggs till genom att kontrollera ID för klustret i tillägget.</span><span class="sxs-lookup"><span data-stu-id="a850c-2676">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="a850c-2677">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="a850c-2677">Az.SignalR</span></span>
* <span data-ttu-id="a850c-2678">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="a850c-2678">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="a850c-2679">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a850c-2679">Az.Sql</span></span>
* <span data-ttu-id="a850c-2680">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="a850c-2680">Update incorrect online help URLs</span></span>
* <span data-ttu-id="a850c-2681">Uppdaterad parameterbeskrivning för LicenseType-parameter med möjliga värden</span><span class="sxs-lookup"><span data-stu-id="a850c-2681">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="a850c-2682">Korrigering för att uppdatera hanterad instansidentitet som inte fungerar när det är den enda uppdaterade egenskapen</span><span class="sxs-lookup"><span data-stu-id="a850c-2682">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="a850c-2683">Stöd för anpassad sortering på hanterad instans</span><span class="sxs-lookup"><span data-stu-id="a850c-2683">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a850c-2684">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a850c-2684">Az.Storage</span></span>
* <span data-ttu-id="a850c-2685">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="a850c-2685">Update incorrect online help URLs</span></span>
* <span data-ttu-id="a850c-2686">Tillhandahåll detaljerat felmeddelande när en användare försöker hämta/konfigurera klassisk loggning/mått på ett Premium Storage-konto eftersom Premium Storage-kontot inte har stöd för klassisk loggning/mått.</span><span class="sxs-lookup"><span data-stu-id="a850c-2686">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="a850c-2687">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="a850c-2687">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="a850c-2688">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="a850c-2688">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="a850c-2689">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="a850c-2689">Az.TrafficManager</span></span>
* <span data-ttu-id="a850c-2690">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="a850c-2690">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a850c-2691">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a850c-2691">Az.Websites</span></span>
* <span data-ttu-id="a850c-2692">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="a850c-2692">Update incorrect online help URLs</span></span>
* <span data-ttu-id="a850c-2693">Korrigerar ”New-AzWebAppSSLBinding” så att certifikatet laddas upp till rätt resursgrupp och plats om appen finns i en ASE.</span><span class="sxs-lookup"><span data-stu-id="a850c-2693">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="a850c-2694">Korrigerar ”New-AzWebAppSSLBinding” så att taggarna inte skrivs över på en bindning av ett SSL-certifikat till en app</span><span class="sxs-lookup"><span data-stu-id="a850c-2694">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="a850c-2695">1.1.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="a850c-2695">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a850c-2696">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a850c-2696">Az.Accounts</span></span>
* <span data-ttu-id="a850c-2697">Lade till omfattningen ”Lokal” till Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="a850c-2697">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a850c-2698">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a850c-2698">Az.Compute</span></span>
* <span data-ttu-id="a850c-2699">Namn är nu valfritt i ID-parametern för Restart/Start/Stop/Remove/Set-AzVM och Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="a850c-2699">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="a850c-2700">Uppdaterade beskrivningen av ID i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="a850c-2700">Updated the description of ID in help files</span></span>
* <span data-ttu-id="a850c-2701">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a850c-2701">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a850c-2702">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a850c-2702">Az.DataLakeStore</span></span>
* <span data-ttu-id="a850c-2703">Uppdatera sdk-versionen av dataplanet till 1.1.14 för SDK-korrigeringar.</span><span class="sxs-lookup"><span data-stu-id="a850c-2703">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="a850c-2704">Korrigerade hanteringen av negativ accesstime och modificationtime för getfilestatus och liststatus; korrigera asynkront annulleringstoken</span><span class="sxs-lookup"><span data-stu-id="a850c-2704">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="a850c-2705">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="a850c-2705">Az.EventGrid</span></span>
* <span data-ttu-id="a850c-2706">Uppdaterat för användning av API-versionen 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="a850c-2706">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="a850c-2707">Uppdaterade följande cmdletar för att stödja nytt scenario i API-versionen 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="a850c-2707">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="a850c-2708">New-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="a850c-2708">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="a850c-2709">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="a850c-2709">Event Time-To-Live,</span></span>
        - <span data-ttu-id="a850c-2710">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="a850c-2710">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="a850c-2711">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="a850c-2711">Dead letter endpoint.</span></span>
    - <span data-ttu-id="a850c-2712">Update-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="a850c-2712">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="a850c-2713">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="a850c-2713">Event Time-To-Live,</span></span>
        - <span data-ttu-id="a850c-2714">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="a850c-2714">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="a850c-2715">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="a850c-2715">Dead letter endpoint.</span></span>
* <span data-ttu-id="a850c-2716">Lade till nya enum-värden (storageQueue och hybridConnection) för alternativet EndpointType i cmdletarna New-AzureRmEventGridSubscription och Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="a850c-2716">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="a850c-2717">Visa varningsmeddelanden om skapande eller uppdatering av händelseprenumerationen förväntas medföra manuell åtgärd från användaren.</span><span class="sxs-lookup"><span data-stu-id="a850c-2717">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a850c-2718">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a850c-2718">Az.IotHub</span></span>
* <span data-ttu-id="a850c-2719">Har uppdaterats till den senaste versionen av SDK:n lotHub</span><span class="sxs-lookup"><span data-stu-id="a850c-2719">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="a850c-2720">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="a850c-2720">Az.LogicApp</span></span>
* <span data-ttu-id="a850c-2721">Get-AzLogicApp visar en lista över alla som inte har angivet namn</span><span class="sxs-lookup"><span data-stu-id="a850c-2721">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="a850c-2722">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a850c-2722">Az.Resources</span></span>
* <span data-ttu-id="a850c-2723">Åtgärdade problem med parameteruppsättningen när parametrarna -ODataQuery och -ResourceId anges för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="a850c-2723">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="a850c-2724">Mer information här: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="a850c-2724">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="a850c-2725">Åtgärdade hantering av parametern -Custom i New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a850c-2725">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="a850c-2726">Korrigerade stavfel i New-AzDeployment-dokumentationen</span><span class="sxs-lookup"><span data-stu-id="a850c-2726">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="a850c-2727">Gjorde parametern -MailNickname obligatorisk för New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="a850c-2727">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="a850c-2728">Mer information här: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="a850c-2728">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="a850c-2729">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="a850c-2729">Az.SignalR</span></span>
* <span data-ttu-id="a850c-2730">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a850c-2730">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="a850c-2731">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a850c-2731">Az.Sql</span></span>
* <span data-ttu-id="a850c-2732">Konverterade lagringshanteringsklientens beroende av den normala SDK-implementeringen.</span><span class="sxs-lookup"><span data-stu-id="a850c-2732">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a850c-2733">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a850c-2733">Az.Storage</span></span>
* <span data-ttu-id="a850c-2734">Angav StorageAccountName för lagringskontext som det verkliga namnet på lagringskontot när det skapas med Sas Token, OAuth eller Anonymous</span><span class="sxs-lookup"><span data-stu-id="a850c-2734">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="a850c-2735">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="a850c-2735">New-AzStorageContext</span></span>
* <span data-ttu-id="a850c-2736">Skapade Sas Token för Blob Snapshot-objekt med parametern -FullUri, åtgärdade den returnerade URI:n så att den blir URI för ögonblicksbild</span><span class="sxs-lookup"><span data-stu-id="a850c-2736">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="a850c-2737">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="a850c-2737">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a850c-2738">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a850c-2738">Az.Websites</span></span>
* <span data-ttu-id="a850c-2739">Åtgärdade en bugg i datumparsningen i Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="a850c-2739">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="a850c-2740">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a850c-2740">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="a850c-2741">1.0.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="a850c-2741">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="a850c-2742">Allmänt</span><span class="sxs-lookup"><span data-stu-id="a850c-2742">General</span></span>

- <span data-ttu-id="a850c-2743">Allmän tillgänglighet för Az-modulen</span><span class="sxs-lookup"><span data-stu-id="a850c-2743">General Availability of Az Module</span></span>
- <span data-ttu-id="a850c-2744">Onlinehjälp för varje modul</span><span class="sxs-lookup"><span data-stu-id="a850c-2744">Online help for each module</span></span>
- <span data-ttu-id="a850c-2745">Mer information och en översikt finns på [Az-informationssidan](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="a850c-2745">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="a850c-2746">Information om hur du migrerar från AzureRM finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a850c-2746">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="a850c-2747">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a850c-2747">Az.Accounts</span></span>
- <span data-ttu-id="a850c-2748">Har ändrats från Az.Profile</span><span class="sxs-lookup"><span data-stu-id="a850c-2748">Changed from Az.Profile</span></span>
- <span data-ttu-id="a850c-2749">Fasta tabellformat för profil- och kontexttyper</span><span class="sxs-lookup"><span data-stu-id="a850c-2749">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="a850c-2750">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a850c-2750">Az.ApiManagement</span></span>
- <span data-ttu-id="a850c-2751">Korrigeringar för #7002</span><span class="sxs-lookup"><span data-stu-id="a850c-2751">Fixes for #7002</span></span>
- <span data-ttu-id="a850c-2752">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a850c-2752">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="a850c-2753">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="a850c-2753">Az.Batch</span></span>
- <span data-ttu-id="a850c-2754">Lade till möjligheten att se vilken version av Azure Batch Node Agent som körs på var och en av de virtuella datorerna i en pool, via den nya egenskapen `NodeAgentInformation` på `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="a850c-2754">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="a850c-2755">Standarden `Caching` för `PSDataDisk` är nu `ReadWrite` i stället för `None`.</span><span class="sxs-lookup"><span data-stu-id="a850c-2755">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="a850c-2756">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a850c-2756">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="a850c-2757">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="a850c-2757">Az.Billing</span></span>
- <span data-ttu-id="a850c-2758">Kombinerar cmdletarna för fakturering, förbrukning och UsageAggregates. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a850c-2758">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="a850c-2759">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="a850c-2759">Az.CognitivServices</span></span>
- <span data-ttu-id="a850c-2760">Lade till kompletterare för SkuName och Typem som är tillgängliga i New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="a850c-2760">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="a850c-2761">Tog bort parameteruppsättningen GetSkusWithAccountParamSetName från Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="a850c-2761">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="a850c-2762">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="a850c-2762">Az.ContainerInstance</span></span>
- <span data-ttu-id="a850c-2763">Stöd för ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="a850c-2763">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="a850c-2764">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="a850c-2764">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="a850c-2765">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a850c-2765">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="a850c-2766">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a850c-2766">Az.DataLakeStore</span></span>
- <span data-ttu-id="a850c-2767">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a850c-2767">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="a850c-2768">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a850c-2768">Az.Monitor</span></span>
- <span data-ttu-id="a850c-2769">Döpte om Az.Insights till Az.Monitor och andra mindre icke-bakåtkompatibla ändringar. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a850c-2769">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="a850c-2770">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a850c-2770">Az.KeyVault</span></span>
- <span data-ttu-id="a850c-2771">Tog bort den inaktuella egenskapen PurgeDisabled från utdatatyper</span><span class="sxs-lookup"><span data-stu-id="a850c-2771">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="a850c-2772">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="a850c-2772">Az.MachineLearning</span></span>
- <span data-ttu-id="a850c-2773">Inkluderade cmdletarna från modulen Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="a850c-2773">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="a850c-2774">Az.Media</span><span class="sxs-lookup"><span data-stu-id="a850c-2774">Az.Media</span></span>
- <span data-ttu-id="a850c-2775">Tog bort inaktuella -Tags-alias från New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="a850c-2775">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="a850c-2776">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a850c-2776">Az.Network</span></span>
<span data-ttu-id="a850c-2777">Stöd har lagts till för konfiguration av RewriteRuleSets i Application Gateway</span><span class="sxs-lookup"><span data-stu-id="a850c-2777">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="a850c-2778">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="a850c-2778">New cmdlets added:</span></span>
        - <span data-ttu-id="a850c-2779">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a850c-2779">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="a850c-2780">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a850c-2780">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="a850c-2781">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a850c-2781">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="a850c-2782">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a850c-2782">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="a850c-2783">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a850c-2783">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="a850c-2784">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="a850c-2784">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="a850c-2785">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="a850c-2785">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="a850c-2786">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="a850c-2786">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="a850c-2787">Cmdletar har uppdaterats med den valfria parametern -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a850c-2787">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="a850c-2788">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a850c-2788">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="a850c-2789">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="a850c-2789">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="a850c-2790">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="a850c-2790">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="a850c-2791">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a850c-2791">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="a850c-2792">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="a850c-2792">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="a850c-2793">New-AzureRmApplicationGatewayUrlPathMapConfig har lagt till KeyVault-stöd för Application Gateway med Identity.</span><span class="sxs-lookup"><span data-stu-id="a850c-2793">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="a850c-2794">Cmdletar har uppdaterats med den valfria parametern -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="a850c-2794">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="a850c-2795">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="a850c-2795">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="a850c-2796">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="a850c-2796">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="a850c-2797">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="a850c-2797">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="a850c-2798">Cmdleten New-AzApplicationGateway har uppdaterats med den valfria parametern -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="a850c-2798">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="a850c-2799">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a850c-2799">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="a850c-2800">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a850c-2800">Az.OperationalInsights</span></span>
- <span data-ttu-id="a850c-2801">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a850c-2801">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="a850c-2802">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="a850c-2802">Az.Profile</span></span>
- <span data-ttu-id="a850c-2803">Modulnamnet har ändrats till Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a850c-2803">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="a850c-2804">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a850c-2804">Az.RecoveryServices</span></span>
- <span data-ttu-id="a850c-2805">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a850c-2805">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="a850c-2806">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a850c-2806">Az.Resources</span></span>
- <span data-ttu-id="a850c-2807">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a850c-2807">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="a850c-2808">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a850c-2808">Az.ServiceFabric</span></span>
- <span data-ttu-id="a850c-2809">Stöd för specificering av certifikat efter eget namn och tumavtryck</span><span class="sxs-lookup"><span data-stu-id="a850c-2809">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="a850c-2810">Information om fler icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a850c-2810">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="a850c-2811">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="a850c-2811">Az.SIgnalR</span></span>
- <span data-ttu-id="a850c-2812">Allmän tillgänglighet för PowerShell-cmdletar för SIgnalR</span><span class="sxs-lookup"><span data-stu-id="a850c-2812">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="a850c-2813">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a850c-2813">Az.Sql</span></span>
- <span data-ttu-id="a850c-2814">Lade till de nya identifieringstyperna Data_Exfiltration och Unsafe_Action i Threat Detection-cmdletar</span><span class="sxs-lookup"><span data-stu-id="a850c-2814">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="a850c-2815">Uppdaterade dokumentationsexempel för Sql Auditing-cmdletar</span><span class="sxs-lookup"><span data-stu-id="a850c-2815">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="a850c-2816">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a850c-2816">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="a850c-2817">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a850c-2817">Az.Storage</span></span>
- <span data-ttu-id="a850c-2818">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a850c-2818">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="a850c-2819">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a850c-2819">Az.Websites</span></span>
- <span data-ttu-id="a850c-2820">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a850c-2820">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="a850c-2821">0.7.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="a850c-2821">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="a850c-2822">Allmänt</span><span class="sxs-lookup"><span data-stu-id="a850c-2822">General</span></span>

* <span data-ttu-id="a850c-2823">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="a850c-2823">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="a850c-2824">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a850c-2824">Az.Compute</span></span>

* <span data-ttu-id="a850c-2825">Lade till stöd för UltraSSD och Galleriavbildningar i de enkla parameteruppsättningarna för `New-AzVm(ss)`-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="a850c-2825">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="a850c-2826">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a850c-2826">Az.DataLakeStore</span></span>

* <span data-ttu-id="a850c-2827">Åtgärdade avslutande snedstreck i domänen för adls-konto</span><span class="sxs-lookup"><span data-stu-id="a850c-2827">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="a850c-2828">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="a850c-2828">Az.FrontDoor</span></span>

* <span data-ttu-id="a850c-2829">Brutna länkar korrigerades</span><span class="sxs-lookup"><span data-stu-id="a850c-2829">Fixed some broken links</span></span>
    - <span data-ttu-id="a850c-2830">I artiklarna New-AzureRmFrontDoor och Set-AzureRmFrontDoor artiklar korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="a850c-2830">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="a850c-2831">I artikeln New-AzureRmFrontDoorManagedRuleObject korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="a850c-2831">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="a850c-2832">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a850c-2832">Az.RecoveryServices</span></span>

* <span data-ttu-id="a850c-2833">Lade till valideringar på klientsidan för Azure-filresurs med återställningsåtgärder.</span><span class="sxs-lookup"><span data-stu-id="a850c-2833">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="a850c-2834">Gjorde storageAccountName och storageAccountResourceGroupName valfritt för afs-återställning.</span><span class="sxs-lookup"><span data-stu-id="a850c-2834">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="a850c-2835">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a850c-2835">Az.Resources</span></span>

* <span data-ttu-id="a850c-2836">Korrigering för https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="a850c-2836">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="a850c-2837">Uppdaterade Get-AzureRmRoleAssignment så att prenumerationsomfattningen används om den anges vid begäran om klassiska administratörer.</span><span class="sxs-lookup"><span data-stu-id="a850c-2837">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="a850c-2838">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a850c-2838">Az.Sql</span></span>

* <span data-ttu-id="a850c-2839">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="a850c-2839">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="a850c-2840">Korrigerade ett problem med Get-AzureRmSqlDatabaseVulnerabilityAssessment med DotNet-kärna</span><span class="sxs-lookup"><span data-stu-id="a850c-2840">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="a850c-2841">Ändrade dokumentationen för hjälpmeddelanden som rör SQL Auditing-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="a850c-2841">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="a850c-2842">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a850c-2842">Az.Storage</span></span>

* <span data-ttu-id="a850c-2843">Lade till -EnableHierarchicalNamespace i New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a850c-2843">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="a850c-2844">Åtgärdade problemet med att cmdleten Copy File inte kunde återanvända källkontexten på målet om inte -DestContext angetts</span><span class="sxs-lookup"><span data-stu-id="a850c-2844">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="a850c-2845">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="a850c-2845">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="a850c-2846">Stöd för statisk webbplatskonfiguration</span><span class="sxs-lookup"><span data-stu-id="a850c-2846">Support Static Website configuration</span></span>
    - <span data-ttu-id="a850c-2847">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="a850c-2847">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="a850c-2848">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="a850c-2848">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="a850c-2849">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a850c-2849">Az.Websites</span></span>

* <span data-ttu-id="a850c-2850">Set-AzureRmWebApp och Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a850c-2850">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="a850c-2851">Ny parameter (-AzureStoragePath) har lagts till för att ange att Azure Storage-sökvägar ska monteras i containerappar i Windows och Linux.</span><span class="sxs-lookup"><span data-stu-id="a850c-2851">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="a850c-2852">Använder utdata från den nya cmdleten New-AzureRmWebAppAzureStoragePath som en parameter för att ange sökvägar för Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="a850c-2852">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="a850c-2853">0.6.1 – november 2018</span><span class="sxs-lookup"><span data-stu-id="a850c-2853">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="a850c-2854">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a850c-2854">Az.ApiManagement</span></span>
* <span data-ttu-id="a850c-2855">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="a850c-2855">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="a850c-2856">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a850c-2856">Az.Automation</span></span>
* <span data-ttu-id="a850c-2857">Swagger baserade Azure Automation-cmdletar</span><span class="sxs-lookup"><span data-stu-id="a850c-2857">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="a850c-2858">Cmdletar för Uppdateringshantering har lagts till</span><span class="sxs-lookup"><span data-stu-id="a850c-2858">Added Update Management cmdlets</span></span>
* <span data-ttu-id="a850c-2859">Cmdletar för källkontroll har lagts till</span><span class="sxs-lookup"><span data-stu-id="a850c-2859">Added Source Control cmdlets</span></span>
* <span data-ttu-id="a850c-2860">Remove-AzureRmAutomationHybridWorkerGroup-cmdlet har lagts till</span><span class="sxs-lookup"><span data-stu-id="a850c-2860">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="a850c-2861">Kommandot för DSC-registreringsnod har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="a850c-2861">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="a850c-2862">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a850c-2862">Az.Compute</span></span>
* <span data-ttu-id="a850c-2863">Problem med SystemAssigned-identitet har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="a850c-2863">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="a850c-2864">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="a850c-2864">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="a850c-2865">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="a850c-2865">Az.ContainerInstance</span></span>
* <span data-ttu-id="a850c-2866">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="a850c-2866">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="a850c-2867">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="a850c-2867">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="a850c-2868">uppdatera exempelbeskrivningen för marketplace-cmdletar</span><span class="sxs-lookup"><span data-stu-id="a850c-2868">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="a850c-2869">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a850c-2869">Az.Network</span></span>
* <span data-ttu-id="a850c-2870">Cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomErreller Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="a850c-2870">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="a850c-2871">ICMP tillbaka till stöd för Azure Firewall-nätverksprotokoll har lagts till</span><span class="sxs-lookup"><span data-stu-id="a850c-2871">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="a850c-2872">Uppdatera cmdlet Test-AzureRmNetworkWatcherConnectivity, lägga till verifiering av mål-id, adress och port.</span><span class="sxs-lookup"><span data-stu-id="a850c-2872">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="a850c-2873">Åtgärda problem med minnesanvändning i VirtualNetwork-karta</span><span class="sxs-lookup"><span data-stu-id="a850c-2873">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="a850c-2874">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="a850c-2874">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="a850c-2875">Åtgärda för att ändra principen för en skyddad fildelning.</span><span class="sxs-lookup"><span data-stu-id="a850c-2875">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="a850c-2876">Tidszonsprincipen har konverterats till versaler.</span><span class="sxs-lookup"><span data-stu-id="a850c-2876">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="a850c-2877">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="a850c-2877">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="a850c-2878">Exempel i New-AzureRmRecoveryServicesAsrProtectableItem har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="a850c-2878">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="a850c-2879">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="a850c-2879">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="a850c-2880">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="a850c-2880">Az.Relay</span></span>
* <span data-ttu-id="a850c-2881">Valfri parameter -KeyValue till New-AzureRmRelayKey cmdlet har lagts till, vilket gör det möjligt för användare att tillhandahålla KeyValue.</span><span class="sxs-lookup"><span data-stu-id="a850c-2881">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="a850c-2882">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a850c-2882">Az.Resources</span></span>
* <span data-ttu-id="a850c-2883">Uppdatera hjälpdokumentation för resursidentitet kopplad till parametrar i `New-AzureRmPolicyAssignment` och `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="a850c-2883">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="a850c-2884">Lägg till ett exempel för New-AzureRmPolicyDefinition som använder -Metadata</span><span class="sxs-lookup"><span data-stu-id="a850c-2884">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="a850c-2885">Korrigera så att skiftläge behålls i taggnycklar i NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="a850c-2885">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="a850c-2886">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a850c-2886">Az.ServiceFabric</span></span>
* <span data-ttu-id="a850c-2887">Lägg till utfasningsmeddelanden för kommande icke-kompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="a850c-2887">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="a850c-2888">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a850c-2888">Az.Sql</span></span>
* <span data-ttu-id="a850c-2889">Nya cmdletar för CRUD-åtgärder på Azure Sql Database-hanterad instans och Azure Sql-hanterad databas</span><span class="sxs-lookup"><span data-stu-id="a850c-2889">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="a850c-2890">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="a850c-2890">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="a850c-2891">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="a850c-2891">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="a850c-2892">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="a850c-2892">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="a850c-2893">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="a850c-2893">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="a850c-2894">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="a850c-2894">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="a850c-2895">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="a850c-2895">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="a850c-2896">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="a850c-2896">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="a850c-2897">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="a850c-2897">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="a850c-2898">Hantering av utökad granskningsprincip på en server eller en databas har aktiverats.</span><span class="sxs-lookup"><span data-stu-id="a850c-2898">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="a850c-2899">Ny parameter (PredicateExpression) har lagts till för att aktivera filtrering av granskningsloggar.</span><span class="sxs-lookup"><span data-stu-id="a850c-2899">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="a850c-2900">Cmdletar har ändrats så att de använder SQL-klienter i stället för äldre klienter.</span><span class="sxs-lookup"><span data-stu-id="a850c-2900">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="a850c-2901">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="a850c-2901">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="a850c-2902">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="a850c-2902">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="a850c-2903">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="a850c-2903">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="a850c-2904">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="a850c-2904">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="a850c-2905">Problem med att använda Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings med lagringskontots namnparameter har korrigerats</span><span class="sxs-lookup"><span data-stu-id="a850c-2905">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="a850c-2906">0.5.0 – november 2018</span><span class="sxs-lookup"><span data-stu-id="a850c-2906">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="a850c-2907">Allmänt</span><span class="sxs-lookup"><span data-stu-id="a850c-2907">General</span></span>
* <span data-ttu-id="a850c-2908">Lade till resurskompletterare till många kärn-cmdletar – dessa gör att du kan stega genom befintliga resursnamn med TABB vid interaktiva anrop till cmdletar</span><span class="sxs-lookup"><span data-stu-id="a850c-2908">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="a850c-2909">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="a850c-2909">Az.Profile</span></span>
* <span data-ttu-id="a850c-2910">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="a850c-2910">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="a850c-2911">Bytte namn på parametern TenantId i cmdleten Connect-AzAccount till Tenant och lade till ett alias för TenantId</span><span class="sxs-lookup"><span data-stu-id="a850c-2911">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="a850c-2912">Uppdaterade TenantId-beskrivningen för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="a850c-2912">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="a850c-2913">Åtgärda felmeddelande för misslyckad inloggning när du tillhandahåller klientdomän</span><span class="sxs-lookup"><span data-stu-id="a850c-2913">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="a850c-2914">Åtgärda problem med att kontextnamn hamnar i konflikt för konton utan prenumerationer i klientorganisationen</span><span class="sxs-lookup"><span data-stu-id="a850c-2914">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="a850c-2915">Åtgärda problem med DataLake-slutpunkter vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="a850c-2915">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="a850c-2916">Åtgärdade problem med att Disconnect-AzAccount kastades om den inte anslöts</span><span class="sxs-lookup"><span data-stu-id="a850c-2916">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="a850c-2917">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a850c-2917">Az.CognitiveServices</span></span>
* <span data-ttu-id="a850c-2918">Lade till åtgärden Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="a850c-2918">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a850c-2919">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a850c-2919">Az.Compute</span></span>
* <span data-ttu-id="a850c-2920">Lade till cmdletarna Add-AzVmssVMDataDisk och Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="a850c-2920">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="a850c-2921">Get-AzVMImage visar AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="a850c-2921">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="a850c-2922">Åtgärdade att värdena för alternativen SetAzVMChefExtension -BootstrapOptions och -JsonAttribute inte angavs i json-format.</span><span class="sxs-lookup"><span data-stu-id="a850c-2922">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a850c-2923">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a850c-2923">Az.DataLakeStore</span></span>
* <span data-ttu-id="a850c-2924">Uppdatera DataLake-paketet till 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="a850c-2924">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="a850c-2925">Lägg till standardsamtidighet för flertrådade åtgärder.</span><span class="sxs-lookup"><span data-stu-id="a850c-2925">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="a850c-2926">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="a850c-2926">Az.Insights</span></span>
* <span data-ttu-id="a850c-2927">Åtgärdade problem #7267 (autoskalningsområde)</span><span class="sxs-lookup"><span data-stu-id="a850c-2927">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="a850c-2928">Problem med att uppräknade parametrar inte ställdes in ordentligt när du skapade en ny autoskalningsregel (de ställdes alltid in med standardvärdet).</span><span class="sxs-lookup"><span data-stu-id="a850c-2928">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="a850c-2929">Åtgärdade problem #7513 [Insights] Set-AzDiagnosticSetting kräver uttrycklig specifikation av kategorier när inställningar skapas</span><span class="sxs-lookup"><span data-stu-id="a850c-2929">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="a850c-2930">Nu kräver inte cmdleten uttrycklig anvisning av kategorierna för att aktiveras under skapande, d.v.s. den fungerar enligt beskrivning</span><span class="sxs-lookup"><span data-stu-id="a850c-2930">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a850c-2931">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a850c-2931">Az.Network</span></span>
* <span data-ttu-id="a850c-2932">PeeringType ändrades till en obligatorisk parameter för följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="a850c-2932">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="a850c-2933">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="a850c-2933">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="a850c-2934">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="a850c-2934">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="a850c-2935">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="a850c-2935">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="a850c-2936">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="a850c-2936">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="a850c-2937">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="a850c-2937">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="a850c-2938">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="a850c-2938">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="a850c-2939">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a850c-2939">Az.PolicyInsights</span></span>
* <span data-ttu-id="a850c-2940">Cmdletar för principreparation har lagts till</span><span class="sxs-lookup"><span data-stu-id="a850c-2940">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="a850c-2941">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a850c-2941">Az.Resources</span></span>
* <span data-ttu-id="a850c-2942">Korrigering för https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="a850c-2942">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="a850c-2943">Tillåt att resurser listas med parametern -ResourceId för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="a850c-2943">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="a850c-2944">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a850c-2944">Az.ServiceBus</span></span>
* <span data-ttu-id="a850c-2945">Skrivskyddad MigrationState-egenskap har lagts till i PSServiceBusMigrationConfigurationAttributes, som hjälper till att hålla koll på migreringstillståndet.</span><span class="sxs-lookup"><span data-stu-id="a850c-2945">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a850c-2946">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a850c-2946">Az.ServiceFabric</span></span>
* <span data-ttu-id="a850c-2947">Åtgärda att lägga till certifikat till Linux-Vmss.</span><span class="sxs-lookup"><span data-stu-id="a850c-2947">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="a850c-2948">Åtgärdade Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="a850c-2948">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="a850c-2949">Använd rätt tumavtryck från nya certifikat (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="a850c-2949">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="a850c-2950">Visa undantag korrekt (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="a850c-2950">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="a850c-2951">Åtgärdade Update-AzServiceFabricDurability så att klusterkonfigurationen uppdateras innan Vmss-åtgärden CreateOrUpdate påbörjas.</span><span class="sxs-lookup"><span data-stu-id="a850c-2951">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="a850c-2952">0.4.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="a850c-2952">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="a850c-2953">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="a850c-2953">Az.Profile</span></span>
* <span data-ttu-id="a850c-2954">Åtgärdade problemet med Get-AzSubscription i CloudShell</span><span class="sxs-lookup"><span data-stu-id="a850c-2954">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="a850c-2955">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="a850c-2955">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a850c-2956">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a850c-2956">Az.Compute</span></span>
* <span data-ttu-id="a850c-2957">Nya storlekar lades till i listan över godkända VM-storlekar för vilka accelererat nätverk kommer att aktiveras vid användning av den enkla parameteruppsättningen för New-AzVm</span><span class="sxs-lookup"><span data-stu-id="a850c-2957">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="a850c-2958">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="a850c-2958">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a850c-2959">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a850c-2959">Az.DataLakeStore</span></span>
* <span data-ttu-id="a850c-2960">Lägger till stöd för regler för virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="a850c-2960">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="a850c-2961">Get-AzDataLakeStoreVirtualNetworkRule: Hämtar eller listar regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a850c-2961">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="a850c-2962">Add-AzDataLakeStoreVirtualNetworkRule: Lägger till en regel för virtuellt nätverk i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="a850c-2962">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="a850c-2963">Set-AzDataLakeStoreVirtualNetworkRule: Ändrar den angivna regeln för virtuellt nätverk i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="a850c-2963">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="a850c-2964">Remove-AzDataLakeStoreVirtualNetworkRule: Tar bort en regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a850c-2964">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a850c-2965">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a850c-2965">Az.Network</span></span>
* <span data-ttu-id="a850c-2966">Skicka protokollvärdet till serverdelen för att uppdatera cmdleten Test-AzNetworkWatcherConnectivity.</span><span class="sxs-lookup"><span data-stu-id="a850c-2966">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="a850c-2967">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="a850c-2967">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a850c-2968">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a850c-2968">Az.Resources</span></span>
* <span data-ttu-id="a850c-2969">Åtgärdade problem där Get-AzRoleDefinition genererar ett oläsligt undantag (när standardprofilen inte innehåller någon prenumeration och ingen omfattning har angetts) genom att lägga till ett beskrivande undantag i scenariot.</span><span class="sxs-lookup"><span data-stu-id="a850c-2969">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="a850c-2970">Ställ in ”RoleDefinitionNameParameterSet” som standardparameteruppsättning.</span><span class="sxs-lookup"><span data-stu-id="a850c-2970">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="a850c-2971">0.3.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="a850c-2971">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="a850c-2972">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="a850c-2972">Azure.Storage</span></span>
* <span data-ttu-id="a850c-2973">Åtgärda fel där Kopiera blob/fil inte kopierar metadata när målplatsen har ett problem med metadata</span><span class="sxs-lookup"><span data-stu-id="a850c-2973">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="a850c-2974">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="a850c-2974">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="a850c-2975">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="a850c-2975">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="a850c-2976">Stöd för att hämta användningsinformation om en Storage-resurs för en specifik plats och för att lägga till ett varningsmeddelande för att hämta användningsinformation om en global Storage-resurs är inaktuellt.</span><span class="sxs-lookup"><span data-stu-id="a850c-2976">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="a850c-2977">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="a850c-2977">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="a850c-2978">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a850c-2978">Az.CognitiveServices</span></span>
* <span data-ttu-id="a850c-2979">Stöd för Get-AzCognitiveServicesAccountSkus utan ett befintligt konto.</span><span class="sxs-lookup"><span data-stu-id="a850c-2979">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a850c-2980">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a850c-2980">Az.Compute</span></span>
* <span data-ttu-id="a850c-2981">Åtgärdade fel där Get-AzVM -ResourceGroupName <rg> returnerar fler än 50 resultat om det behövs</span><span class="sxs-lookup"><span data-stu-id="a850c-2981">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="a850c-2982">Lade till ett exempel för SimpleParameterSet i hjälpen för cmdleten New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="a850c-2982">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="a850c-2983">Ett stavfel i förloppsmeddelandet för Azure Disk Encryption har korrigerats</span><span class="sxs-lookup"><span data-stu-id="a850c-2983">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="a850c-2984">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="a850c-2984">Az.DataFactoryV2</span></span>
* <span data-ttu-id="a850c-2985">ADF .Net SDK-versionen har uppdaterats till 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="a850c-2985">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a850c-2986">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a850c-2986">Az.Network</span></span>
* <span data-ttu-id="a850c-2987">Funktionalitet för NetworkProfile har lagts till.</span><span class="sxs-lookup"><span data-stu-id="a850c-2987">Added NetworkProfile functionality.</span></span> <span data-ttu-id="a850c-2988">nya cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="a850c-2988">new cmdlets added</span></span>
    - <span data-ttu-id="a850c-2989">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a850c-2989">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="a850c-2990">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a850c-2990">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="a850c-2991">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a850c-2991">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="a850c-2992">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a850c-2992">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="a850c-2993">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="a850c-2993">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="a850c-2994">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="a850c-2994">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="a850c-2995">Länk för tjänstassociering på modell för undernät har lagts till</span><span class="sxs-lookup"><span data-stu-id="a850c-2995">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="a850c-2996">Cmdletarna New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap och Remove-AzVirtualNetworkTap har lagts till</span><span class="sxs-lookup"><span data-stu-id="a850c-2996">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="a850c-2997">Cmdletarna Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig och Remove-AzNEtworkInterfaceTapConfig har lagts till</span><span class="sxs-lookup"><span data-stu-id="a850c-2997">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="a850c-2998">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="a850c-2998">Az.RedisCache</span></span>
* <span data-ttu-id="a850c-2999">Tillåt att alla strängar används som storleksparametrar framöver.</span><span class="sxs-lookup"><span data-stu-id="a850c-2999">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="a850c-3000">Lägg till P5 i popup-fönstret PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="a850c-3000">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="a850c-3001">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a850c-3001">Az.Resources</span></span>
* <span data-ttu-id="a850c-3002">Parametern -Mode som saknades i Set-AzPolicyDefinition har lagts till</span><span class="sxs-lookup"><span data-stu-id="a850c-3002">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="a850c-3003">Åtgärdade buggen för cmdleten Get-AzProviderOperation för åtgärder med ursprung som innehåller användare</span><span class="sxs-lookup"><span data-stu-id="a850c-3003">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="a850c-3004">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a850c-3004">Az.Sql</span></span>
* <span data-ttu-id="a850c-3005">Ett problem där vissa cmdletar för säkerhetskopiering inte kunde identifiera den aktuella azure-prenumerationen har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="a850c-3005">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a850c-3006">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a850c-3006">Az.Websites</span></span>
* <span data-ttu-id="a850c-3007">Ny cmdlet: Get-AzWebAppContainerContinuousDeploymentUrl – Hämtar webhook-URL:en för kontinuerlig distribution av container</span><span class="sxs-lookup"><span data-stu-id="a850c-3007">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="a850c-3008">Nya cmdletar: New-AzWebAppContainerPSSession och Enter-WebAppContainerPSSession – Startar en PowerShell-fjärrsession i en containerapp för windows</span><span class="sxs-lookup"><span data-stu-id="a850c-3008">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="a850c-3009">0.2.0 – september 2018</span><span class="sxs-lookup"><span data-stu-id="a850c-3009">0.2.0 - September 2018</span></span>
 <span data-ttu-id="a850c-3010">Första versionen</span><span class="sxs-lookup"><span data-stu-id="a850c-3010">Initial Release</span></span>
