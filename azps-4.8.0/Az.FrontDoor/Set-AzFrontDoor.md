---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/set-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Set-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Set-AzFrontDoor.md
ms.openlocfilehash: 344041291f0d7f52aeebb0c968e99268ac042188
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260499"
---
# <span data-ttu-id="85be6-101">Set-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="85be6-101">Set-AzFrontDoor</span></span>

## <span data-ttu-id="85be6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="85be6-102">SYNOPSIS</span></span>
<span data-ttu-id="85be6-103">Uppdatera belastnings utjämning för en Last lucka</span><span class="sxs-lookup"><span data-stu-id="85be6-103">Update a Front Door load balancer</span></span>

## <span data-ttu-id="85be6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="85be6-104">SYNTAX</span></span>

### <span data-ttu-id="85be6-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="85be6-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzFrontDoor -ResourceGroupName <String> -Name <String> [-RoutingRule <PSRoutingRule[]>]
 [-BackendPool <PSBackendPool[]>] [-FrontendEndpoint <PSFrontendEndpoint[]>]
 [-LoadBalancingSetting <PSLoadBalancingSetting[]>] [-HealthProbeSetting <PSHealthProbeSetting[]>]
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85be6-106">ByFieldsWithCertificateNameCheckParameterSet</span><span class="sxs-lookup"><span data-stu-id="85be6-106">ByFieldsWithCertificateNameCheckParameterSet</span></span>
```
Set-AzFrontDoor -ResourceGroupName <String> -Name <String> [-RoutingRule <PSRoutingRule[]>]
 [-BackendPool <PSBackendPool[]>] [-FrontendEndpoint <PSFrontendEndpoint[]>]
 [-LoadBalancingSetting <PSLoadBalancingSetting[]>] [-HealthProbeSetting <PSHealthProbeSetting[]>]
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DisableCertificateNameCheck]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85be6-107">ByFieldsWithBackendPoolsSettingParameterSet</span><span class="sxs-lookup"><span data-stu-id="85be6-107">ByFieldsWithBackendPoolsSettingParameterSet</span></span>
```
Set-AzFrontDoor -ResourceGroupName <String> -Name <String> [-RoutingRule <PSRoutingRule[]>]
 [-BackendPool <PSBackendPool[]>] [-FrontendEndpoint <PSFrontendEndpoint[]>]
 [-LoadBalancingSetting <PSLoadBalancingSetting[]>] [-HealthProbeSetting <PSHealthProbeSetting[]>]
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] -BackendPoolsSetting <PSBackendPoolsSetting>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85be6-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="85be6-108">ByObjectParameterSet</span></span>
```
Set-AzFrontDoor -InputObject <PSFrontDoor> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85be6-109">ByObjectWithCertificateNameCheckParameterSet</span><span class="sxs-lookup"><span data-stu-id="85be6-109">ByObjectWithCertificateNameCheckParameterSet</span></span>
```
Set-AzFrontDoor -InputObject <PSFrontDoor> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 [-DisableCertificateNameCheck] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="85be6-110">ByObjectWithBackendPoolsSettingParameterSet</span><span class="sxs-lookup"><span data-stu-id="85be6-110">ByObjectWithBackendPoolsSettingParameterSet</span></span>
```
Set-AzFrontDoor -InputObject <PSFrontDoor> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 -BackendPoolsSetting <PSBackendPoolsSetting> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="85be6-111">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="85be6-111">ByResourceIdParameterSet</span></span>
```
Set-AzFrontDoor -ResourceId <String> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85be6-112">ByResourceIdWithCertificateNameCheckParameterSet</span><span class="sxs-lookup"><span data-stu-id="85be6-112">ByResourceIdWithCertificateNameCheckParameterSet</span></span>
```
Set-AzFrontDoor -ResourceId <String> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 [-DisableCertificateNameCheck] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="85be6-113">ByResourceIdWithBackendPoolsSettingParameterSet</span><span class="sxs-lookup"><span data-stu-id="85be6-113">ByResourceIdWithBackendPoolsSettingParameterSet</span></span>
```
Set-AzFrontDoor -ResourceId <String> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 -BackendPoolsSetting <PSBackendPoolsSetting> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="85be6-114">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="85be6-114">DESCRIPTION</span></span>
<span data-ttu-id="85be6-115">Cmdleten **set-AzFrontDoor** uppdaterar en belastningsutjämnare för Last luckan.</span><span class="sxs-lookup"><span data-stu-id="85be6-115">The **Set-AzFrontDoor** cmdlet updates a Front Door load balancer.</span></span> <span data-ttu-id="85be6-116">Om indataparametrarna inte anges används gamla parametrar från den befintliga främre dörren.</span><span class="sxs-lookup"><span data-stu-id="85be6-116">If input parameters are not provided, old parameters from the existing Front Door will be used.</span></span>

## <span data-ttu-id="85be6-117">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="85be6-117">EXAMPLES</span></span>

### <span data-ttu-id="85be6-118">Exempel 1: uppdatera en befintlig främre dörr med FrontDoorName och ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="85be6-118">Example 1: update an existing Front Door with FrontDoorName and ResourceGroupName.</span></span>
```powershell
PS C:\> Set-AzFrontDoor -Name "frontDoor1" -ResourceGroupName "resourceGroup1" -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1 -BackendPoolsSetting $backendPoolsSetting1

FriendlyName                : frontdoor1
RoutingRules                : {routingrule1}
BackendPools                : {backendpool1}
BackendPoolsSetting         : {backendPoolsSetting1}
EnforceCertificateNameCheck : {backendPoolsSetting1.EnforceCertificateNameCheck}
HealthProbeSettings         : {healthProbeSetting1}
LoadBalancingSettings       : {loadbalancingsetting1}
FrontendEndpoints           : {frontendendpoint1}
EnabledState                : Enabled
ResourceState               : Enabled
ProvisioningState           : Succeeded
Cname                       :
Tags                        : {tag1, tag2}
Id                          : /subscriptions/{guid}/resourcegroups/{guid}/providers/Microsoft.Network/frontdoors/frontdoor1
Name                        : frontdoor1
Type                        : Microsoft.Network/frontdoors
```

<span data-ttu-id="85be6-119">uppdatera en befintlig FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="85be6-119">update an existing FrontDoor.</span></span>

### <span data-ttu-id="85be6-120">Exempel 2: uppdatera en befintlig främre dörr med PSFrontDoor-objekt.</span><span class="sxs-lookup"><span data-stu-id="85be6-120">Example 2: update an existing Front Door with PSFrontDoor object.</span></span>
```powershell
PS C:\>  Set-AzFrontDoor -InputObject $frontDoor1 -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1 -BackendPoolsSetting $backendPoolsSetting1

FriendlyName                : frontdoor1
RoutingRules                : {routingrule1}
BackendPools                : {backendpool1}
BackendPoolsSetting         : {backendPoolsSetting1}
EnforceCertificateNameCheck : {backendPoolsSetting1.EnforceCertificateNameCheck}
HealthProbeSettings         : {healthProbeSetting1}
LoadBalancingSettings       : {loadbalancingsetting1}
FrontendEndpoints           : {frontendendpoint1}
EnabledState                : Enabled
ResourceState               : Enabled
ProvisioningState           : Succeeded
Cname                       :
Tags                        : {tag1, tag2}
Id                          : /subscriptions/{guid}/resourcegroups/{guid}/providers/Microsoft.Network/frontdoors/frontdoor1
Name                        : frontdoor1
Type                        : Microsoft.Network/frontdoor1
```

<span data-ttu-id="85be6-121">uppdatera en befintlig FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="85be6-121">update an existing FrontDoor.</span></span>

### <span data-ttu-id="85be6-122">Exempel 3: uppdatera en befintlig främre dörr med ResourceId</span><span class="sxs-lookup"><span data-stu-id="85be6-122">Example 3: update an existing Front Door with ResourceId</span></span>
```powershell
PS C:\>  Set-AzFrontDoor -ResourceId {resourceId} -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1 -BackendPoolsSetting $backendPoolsSetting1

FriendlyName                : frontdoor1
RoutingRules                : {routingrule1}
BackendPools                : {backendpool1}
BackendPoolsSetting         : {backendPoolsSetting1}
EnforceCertificateNameCheck : {backendPoolsSetting1.EnforceCertificateNameCheck}
HealthProbeSettings         : {healthProbeSetting1}
LoadBalancingSettings       : {loadbalancingsetting1}
FrontendEndpoints           : {frontendendpoint1}
EnabledState                : Enabled
ResourceState               : Enabled
ProvisioningState           : Succeeded
Cname                       :
Tags                        : {tag1, tag2}
Id                          : /subscriptions/{guid}/resourcegroups/{guid}/providers/Microsoft.Network/frontdoors/frontdoor1
Name                        : frontdoor1
Type                        : Microsoft.Network/frontdoor1
```

<span data-ttu-id="85be6-123">uppdatera en befintlig FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="85be6-123">update an existing FrontDoor.</span></span>

### <span data-ttu-id="85be6-124">Exempel 4: uppdatera BackendPoolSetting egenskapen EnforceCertificateNameCheck för en befintlig främre dörr med-DisableCertificateNameCheck switch parameter</span><span class="sxs-lookup"><span data-stu-id="85be6-124">Example 4: update BackendPoolSetting property EnforceCertificateNameCheck of an existing Front Door with -DisableCertificateNameCheck switch parameter</span></span>
<span data-ttu-id="85be6-125">Den främre dörren kan identifieras med FrontoorName och ResourceGroupName, PSFrontDoor-objekt eller ResourceId.</span><span class="sxs-lookup"><span data-stu-id="85be6-125">Front Door to be updated can be identified using FrontoorName and ResourceGroupName, PSFrontDoor object, or ResourceId.</span></span> <span data-ttu-id="85be6-126">(Se tre exempel till exempel) I exemplet nedan används objektet PSFrontDoor.</span><span class="sxs-lookup"><span data-stu-id="85be6-126">(See above 3 examples for example) The below example uses PSFrontDoor object.</span></span>

```powershell
PS C:\>  Set-AzFrontDoor -InputObject $frontDoor1 -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1 -DisableCertificateNameCheck

FriendlyName                : frontdoor1
RoutingRules                : {routingrule1}
BackendPools                : {backendpool1}
BackendPoolsSetting         : {PSBackendPoolsSetting object with EnforceCertificateNameCheck is set to Disabled}
EnforceCertificateNameCheck : Disabled
HealthProbeSettings         : {healthProbeSetting1}
LoadBalancingSettings       : {loadbalancingsetting1}
FrontendEndpoints           : {frontendendpoint1}
EnabledState                : Enabled
ResourceState               : Enabled
ProvisioningState           : Succeeded
Cname                       :
Tags                        : {tag1, tag2}
Id                          : /subscriptions/{guid}/resourcegroups/{guid}/providers/Microsoft.Network/frontdoors/frontdoor1
Name                        : frontdoor1
Type                        : Microsoft.Network/frontdoor1
```

<span data-ttu-id="85be6-127">uppdatera en befintlig FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="85be6-127">update an existing FrontDoor.</span></span>

## <span data-ttu-id="85be6-128">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="85be6-128">PARAMETERS</span></span>

### <span data-ttu-id="85be6-129">-BackendPool</span><span class="sxs-lookup"><span data-stu-id="85be6-129">-BackendPool</span></span>
<span data-ttu-id="85be6-130">Backendpools är tillgänglig för regel för routning.</span><span class="sxs-lookup"><span data-stu-id="85be6-130">Backendpools available to routing rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPool[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85be6-131">-BackendPoolsSetting</span><span class="sxs-lookup"><span data-stu-id="85be6-131">-BackendPoolsSetting</span></span>
<span data-ttu-id="85be6-132">Inställningar för alla backendPools.</span><span class="sxs-lookup"><span data-stu-id="85be6-132">Settings for all backendPools.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPoolsSetting
Parameter Sets: ByFieldsWithBackendPoolsSettingParameterSet, ByObjectWithBackendPoolsSettingParameterSet, ByResourceIdWithBackendPoolsSettingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85be6-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85be6-133">-DefaultProfile</span></span>
<span data-ttu-id="85be6-134">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="85be6-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85be6-135">-DisableCertificateNameCheck</span><span class="sxs-lookup"><span data-stu-id="85be6-135">-DisableCertificateNameCheck</span></span>
<span data-ttu-id="85be6-136">Om du vill inaktivera certifikat namns kontroll för HTTPS-begäranden till alla backend-pooler.</span><span class="sxs-lookup"><span data-stu-id="85be6-136">Whether to disable certificate name check on HTTPS requests to all backend pools.</span></span> <span data-ttu-id="85be6-137">Ingen effekt på icke-HTTPS-begäranden.</span><span class="sxs-lookup"><span data-stu-id="85be6-137">No effect on non-HTTPS requests.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByFieldsWithCertificateNameCheckParameterSet, ByObjectWithCertificateNameCheckParameterSet, ByResourceIdWithCertificateNameCheckParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85be6-138">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="85be6-138">-EnabledState</span></span>
<span data-ttu-id="85be6-139">Drift status för belastnings utjämning för Last luckan.</span><span class="sxs-lookup"><span data-stu-id="85be6-139">Operational status of the Front Door load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85be6-140">-FrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="85be6-140">-FrontendEndpoint</span></span>
<span data-ttu-id="85be6-141">Klient delens slut punkter är tillgängliga för regel för routning.</span><span class="sxs-lookup"><span data-stu-id="85be6-141">Frontend endpoints available to routing rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85be6-142">-HealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="85be6-142">-HealthProbeSetting</span></span>
<span data-ttu-id="85be6-143">Inställningar för hälso sökning som är kopplade till denna instans av front dörren.</span><span class="sxs-lookup"><span data-stu-id="85be6-143">Health probe settings associated with this Front Door instance.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSHealthProbeSetting[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85be6-144">-InputObject</span><span class="sxs-lookup"><span data-stu-id="85be6-144">-InputObject</span></span>
<span data-ttu-id="85be6-145">Objekt för front dörr att uppdatera.</span><span class="sxs-lookup"><span data-stu-id="85be6-145">The Front Door object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor
Parameter Sets: ByObjectParameterSet, ByObjectWithCertificateNameCheckParameterSet, ByObjectWithBackendPoolsSettingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="85be6-146">-LoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="85be6-146">-LoadBalancingSetting</span></span>
<span data-ttu-id="85be6-147">Inställningar för belastnings utjämning som är kopplade till den här instansen.</span><span class="sxs-lookup"><span data-stu-id="85be6-147">Load balancing settings associated with this Front Door instance.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSLoadBalancingSetting[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85be6-148">-Namn</span><span class="sxs-lookup"><span data-stu-id="85be6-148">-Name</span></span>
<span data-ttu-id="85be6-149">Namnet på den främre dörren som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="85be6-149">The name of the Front Door to update.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsWithCertificateNameCheckParameterSet, ByFieldsWithBackendPoolsSettingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85be6-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85be6-150">-ResourceGroupName</span></span>
<span data-ttu-id="85be6-151">Den resurs grupp som front dörren tillhör.</span><span class="sxs-lookup"><span data-stu-id="85be6-151">The resource group to which the Front Door belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsWithCertificateNameCheckParameterSet, ByFieldsWithBackendPoolsSettingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85be6-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="85be6-152">-ResourceId</span></span>
<span data-ttu-id="85be6-153">Resurs-ID för den främre dörren som ska uppdateras</span><span class="sxs-lookup"><span data-stu-id="85be6-153">Resource Id of the Front Door to update</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet, ByResourceIdWithCertificateNameCheckParameterSet, ByResourceIdWithBackendPoolsSettingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85be6-154">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="85be6-154">-RoutingRule</span></span>
<span data-ttu-id="85be6-155">Routningsregler som är associerade med den här FrontDoor</span><span class="sxs-lookup"><span data-stu-id="85be6-155">Routing rules associated with this FrontDoor</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRoutingRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85be6-156">-Tagg</span><span class="sxs-lookup"><span data-stu-id="85be6-156">-Tag</span></span>
<span data-ttu-id="85be6-157">Taggarna som är kopplade till FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="85be6-157">The tags associate with the FrontDoor.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85be6-158">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="85be6-158">-Confirm</span></span>
<span data-ttu-id="85be6-159">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="85be6-159">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85be6-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85be6-160">-WhatIf</span></span>
<span data-ttu-id="85be6-161">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="85be6-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85be6-162">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="85be6-162">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85be6-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85be6-163">CommonParameters</span></span>
<span data-ttu-id="85be6-164">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85be6-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85be6-165">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="85be6-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85be6-166">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="85be6-166">INPUTS</span></span>

### <span data-ttu-id="85be6-167">Microsoft. Azure. commands. FrontDoor. Models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="85be6-167">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>
### <span data-ttu-id="85be6-168">System. String</span><span class="sxs-lookup"><span data-stu-id="85be6-168">System.String</span></span>
## <span data-ttu-id="85be6-169">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="85be6-169">OUTPUTS</span></span>

### <span data-ttu-id="85be6-170">Microsoft. Azure. commands. FrontDoor. Models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="85be6-170">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>
## <span data-ttu-id="85be6-171">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="85be6-171">NOTES</span></span>

## <span data-ttu-id="85be6-172">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="85be6-172">RELATED LINKS</span></span>

<span data-ttu-id="85be6-173">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Get-AzFrontDoor](./Get-AzFrontDoor.md) 
 [Remove-AzFrontDoor](./Remove-AzFrontDoor.md) 
 [New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md) 
 [New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md) 
 [New-AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md) 
 [New-AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md) 
 [New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span><span class="sxs-lookup"><span data-stu-id="85be6-173">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Get-AzFrontDoor](./Get-AzFrontDoor.md)
[Remove-AzFrontDoor](./Remove-AzFrontDoor.md)
[New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md)
[New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md)
[New-AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md)
[New-AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md)
[New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span></span>
