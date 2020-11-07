---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/set-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Set-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Set-AzFrontDoor.md
ms.openlocfilehash: 57f1bf57495e75167a1936799c24aff5e6387722
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916686"
---
# <span data-ttu-id="5e38a-101">Set-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="5e38a-101">Set-AzFrontDoor</span></span>

## <span data-ttu-id="5e38a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5e38a-102">SYNOPSIS</span></span>
<span data-ttu-id="5e38a-103">Uppdatera belastnings utjämning för en Last lucka</span><span class="sxs-lookup"><span data-stu-id="5e38a-103">Update a Front Door load balancer</span></span>

## <span data-ttu-id="5e38a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5e38a-104">SYNTAX</span></span>

### <span data-ttu-id="5e38a-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="5e38a-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzFrontDoor -ResourceGroupName <String> -Name <String> [-RoutingRule <PSRoutingRule[]>]
 [-BackendPool <PSBackendPool[]>] [-FrontendEndpoint <PSFrontendEndpoint[]>]
 [-LoadBalancingSetting <PSLoadBalancingSetting[]>] [-HealthProbeSetting <PSHealthProbeSetting[]>]
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DisableCertificateNameCheck]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e38a-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e38a-106">ByObjectParameterSet</span></span>
```
Set-AzFrontDoor -InputObject <PSFrontDoor> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 [-DisableCertificateNameCheck] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5e38a-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e38a-107">ByResourceIdParameterSet</span></span>
```
Set-AzFrontDoor -ResourceId <String> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 [-DisableCertificateNameCheck] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5e38a-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5e38a-108">DESCRIPTION</span></span>
<span data-ttu-id="5e38a-109">Cmdleten **set-AzFrontDoor** uppdaterar en belastningsutjämnare för Last luckan.</span><span class="sxs-lookup"><span data-stu-id="5e38a-109">The **Set-AzFrontDoor** cmdlet updates a Front Door load balancer.</span></span> <span data-ttu-id="5e38a-110">Om indataparametrarna inte anges används gamla parametrar från den befintliga främre dörren.</span><span class="sxs-lookup"><span data-stu-id="5e38a-110">If input parameters are not provided, old parameters from the existing Front Door will be used.</span></span>

## <span data-ttu-id="5e38a-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5e38a-111">EXAMPLES</span></span>

### <span data-ttu-id="5e38a-112">Exempel 1: uppdatera en befintlig främre dörr med FrontDoorName och ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="5e38a-112">Example 1: update an existing Front Door with FrontDoorName and ResourceGroupName.</span></span>
```powershell
PS C:\> Set-AzFrontDoor -Name "frontDoor1" -ResourceGroupName "resourceGroup1" -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

FriendlyName                : frontdoor1
RoutingRules                : {routingrule1}
BackendPools                : {backendpool1}
EnforceCertificateNameCheck : Enabled
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

<span data-ttu-id="5e38a-113">uppdatera en befintlig FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="5e38a-113">update an existing FrontDoor.</span></span>

### <span data-ttu-id="5e38a-114">Exempel 2: uppdatera en befintlig främre dörr med PSFrontDoor-objekt.</span><span class="sxs-lookup"><span data-stu-id="5e38a-114">Example 2: update an existing Front Door with PSFrontDoor object.</span></span>
```powershell
PS C:\>  Set-AzFrontDoor -InputObject $frontDoor1 -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

FriendlyName                : frontdoor1
RoutingRules                : {routingrule1}
BackendPools                : {backendpool1}
EnforceCertificateNameCheck : Enabled
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

<span data-ttu-id="5e38a-115">uppdatera en befintlig FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="5e38a-115">update an existing FrontDoor.</span></span>

### <span data-ttu-id="5e38a-116">Exempel 3: uppdatera en befintlig främre dörr med ResourceId</span><span class="sxs-lookup"><span data-stu-id="5e38a-116">Example 3: update an existing Front Door with ResourceId</span></span>
```powershell
PS C:\>  Set-AzFrontDoor -ResourceId {resourceId} -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

FriendlyName                : frontdoor1
RoutingRules                : {routingrule1}
BackendPools                : {backendpool1}
EnforceCertificateNameCheck : Enabled
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

<span data-ttu-id="5e38a-117">uppdatera en befintlig FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="5e38a-117">update an existing FrontDoor.</span></span>

## <span data-ttu-id="5e38a-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5e38a-118">PARAMETERS</span></span>

### <span data-ttu-id="5e38a-119">-BackendPool</span><span class="sxs-lookup"><span data-stu-id="5e38a-119">-BackendPool</span></span>
<span data-ttu-id="5e38a-120">Backendpools är tillgänglig för regel för routning.</span><span class="sxs-lookup"><span data-stu-id="5e38a-120">Backendpools available to routing rule.</span></span>

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

### <span data-ttu-id="5e38a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e38a-121">-DefaultProfile</span></span>
<span data-ttu-id="5e38a-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5e38a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e38a-123">-DisableCertificateNameCheck</span><span class="sxs-lookup"><span data-stu-id="5e38a-123">-DisableCertificateNameCheck</span></span>
<span data-ttu-id="5e38a-124">Om du vill inaktivera certifikat namns kontroll för HTTPS-begäranden till alla backend-pooler.</span><span class="sxs-lookup"><span data-stu-id="5e38a-124">Whether to disable certificate name check on HTTPS requests to all backend pools.</span></span> <span data-ttu-id="5e38a-125">Ingen effekt på icke-HTTPS-begäranden.</span><span class="sxs-lookup"><span data-stu-id="5e38a-125">No effect on non-HTTPS requests.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e38a-126">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="5e38a-126">-EnabledState</span></span>
<span data-ttu-id="5e38a-127">Drift status för belastnings utjämning för Last luckan.</span><span class="sxs-lookup"><span data-stu-id="5e38a-127">Operational status of the Front Door load balancer.</span></span>

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

### <span data-ttu-id="5e38a-128">-FrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="5e38a-128">-FrontendEndpoint</span></span>
<span data-ttu-id="5e38a-129">Klient delens slut punkter är tillgängliga för regel för routning.</span><span class="sxs-lookup"><span data-stu-id="5e38a-129">Frontend endpoints available to routing rule.</span></span>

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

### <span data-ttu-id="5e38a-130">-HealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="5e38a-130">-HealthProbeSetting</span></span>
<span data-ttu-id="5e38a-131">Inställningar för hälso sökning som är kopplade till denna instans av front dörren.</span><span class="sxs-lookup"><span data-stu-id="5e38a-131">Health probe settings associated with this Front Door instance.</span></span>

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

### <span data-ttu-id="5e38a-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5e38a-132">-InputObject</span></span>
<span data-ttu-id="5e38a-133">Objekt för front dörr att uppdatera.</span><span class="sxs-lookup"><span data-stu-id="5e38a-133">The Front Door object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5e38a-134">-LoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="5e38a-134">-LoadBalancingSetting</span></span>
<span data-ttu-id="5e38a-135">Inställningar för belastnings utjämning som är kopplade till den här instansen.</span><span class="sxs-lookup"><span data-stu-id="5e38a-135">Load balancing settings associated with this Front Door instance.</span></span>

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

### <span data-ttu-id="5e38a-136">-Namn</span><span class="sxs-lookup"><span data-stu-id="5e38a-136">-Name</span></span>
<span data-ttu-id="5e38a-137">Namnet på den främre dörren som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="5e38a-137">The name of the Front Door to update.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e38a-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e38a-138">-ResourceGroupName</span></span>
<span data-ttu-id="5e38a-139">Den resurs grupp som front dörren tillhör.</span><span class="sxs-lookup"><span data-stu-id="5e38a-139">The resource group to which the Front Door belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e38a-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5e38a-140">-ResourceId</span></span>
<span data-ttu-id="5e38a-141">Resurs-ID för den främre dörren som ska uppdateras</span><span class="sxs-lookup"><span data-stu-id="5e38a-141">Resource Id of the Front Door to update</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e38a-142">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="5e38a-142">-RoutingRule</span></span>
<span data-ttu-id="5e38a-143">Routningsregler som är associerade med den här FrontDoor</span><span class="sxs-lookup"><span data-stu-id="5e38a-143">Routing rules associated with this FrontDoor</span></span>

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

### <span data-ttu-id="5e38a-144">-Tagg</span><span class="sxs-lookup"><span data-stu-id="5e38a-144">-Tag</span></span>
<span data-ttu-id="5e38a-145">Taggarna som är kopplade till FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="5e38a-145">The tags associate with the FrontDoor.</span></span>

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

### <span data-ttu-id="5e38a-146">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5e38a-146">-Confirm</span></span>
<span data-ttu-id="5e38a-147">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5e38a-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e38a-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e38a-148">-WhatIf</span></span>
<span data-ttu-id="5e38a-149">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5e38a-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e38a-150">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5e38a-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e38a-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e38a-151">CommonParameters</span></span>
<span data-ttu-id="5e38a-152">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e38a-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e38a-153">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5e38a-153">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e38a-154">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5e38a-154">INPUTS</span></span>

### <span data-ttu-id="5e38a-155">Microsoft. Azure. commands. FrontDoor. Models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="5e38a-155">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

### <span data-ttu-id="5e38a-156">System. String</span><span class="sxs-lookup"><span data-stu-id="5e38a-156">System.String</span></span>

## <span data-ttu-id="5e38a-157">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5e38a-157">OUTPUTS</span></span>

### <span data-ttu-id="5e38a-158">Microsoft. Azure. commands. FrontDoor. Models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="5e38a-158">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

## <span data-ttu-id="5e38a-159">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5e38a-159">NOTES</span></span>

## <span data-ttu-id="5e38a-160">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5e38a-160">RELATED LINKS</span></span>

<span data-ttu-id="5e38a-161">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Get-AzFrontDoor](./Get-AzFrontDoor.md) 
 [Remove-AzFrontDoor](./Remove-AzFrontDoor.md) 
 [New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md) 
 [New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md) 
 [New-AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md) 
 [New-AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md) 
 [New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span><span class="sxs-lookup"><span data-stu-id="5e38a-161">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Get-AzFrontDoor](./Get-AzFrontDoor.md)
[Remove-AzFrontDoor](./Remove-AzFrontDoor.md)
[New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md)
[New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md)
[New-AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md)
[New-AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md)
[New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span></span>
