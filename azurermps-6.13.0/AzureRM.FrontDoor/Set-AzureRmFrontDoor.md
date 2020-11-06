---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/set-azurermfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Set-AzureRmFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Set-AzureRmFrontDoor.md
ms.openlocfilehash: 250fa8a5638e1aa9d67d212fd45352c7756d2aef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572747"
---
# <span data-ttu-id="55c28-101">Set-AzureRmFrontDoor</span><span class="sxs-lookup"><span data-stu-id="55c28-101">Set-AzureRmFrontDoor</span></span>

## <span data-ttu-id="55c28-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="55c28-102">SYNOPSIS</span></span>
<span data-ttu-id="55c28-103">Uppdatera belastnings utjämning för en Last lucka</span><span class="sxs-lookup"><span data-stu-id="55c28-103">Update a Front Door load balancer</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55c28-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="55c28-104">SYNTAX</span></span>

### <span data-ttu-id="55c28-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="55c28-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzureRmFrontDoor -ResourceGroupName <String> -Name <String> [-RoutingRule <PSRoutingRule[]>]
 [-BackendPool <PSBackendPool[]>] [-FrontendEndpoint <PSFrontendEndpoint[]>]
 [-LoadBalancingSetting <PSLoadBalancingSetting[]>] [-HealthProbeSetting <PSHealthProbeSetting[]>]
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55c28-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="55c28-106">ByObjectParameterSet</span></span>
```
Set-AzureRmFrontDoor -InputObject <PSFrontDoor> [-RoutingRule <PSRoutingRule[]>]
 [-BackendPool <PSBackendPool[]>] [-FrontendEndpoint <PSFrontendEndpoint[]>]
 [-LoadBalancingSetting <PSLoadBalancingSetting[]>] [-HealthProbeSetting <PSHealthProbeSetting[]>]
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55c28-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="55c28-107">ResourceIdParameterSet</span></span>
```
Set-AzureRmFrontDoor -ResourceId <String> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55c28-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="55c28-108">DESCRIPTION</span></span>
<span data-ttu-id="55c28-109">Cmdleten **set-AzureRmFrontDoor** uppdaterar en belastningsutjämnare för Last luckan.</span><span class="sxs-lookup"><span data-stu-id="55c28-109">The **Set-AzureRmFrontDoor** cmdlet updates a Front Door load balancer.</span></span> <span data-ttu-id="55c28-110">Om indataparametrarna inte anges används gamla parametrar från den befintliga främre dörren.</span><span class="sxs-lookup"><span data-stu-id="55c28-110">If input parameters are not provided, old parameters from the existing Front Door will be used.</span></span>

## <span data-ttu-id="55c28-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="55c28-111">EXAMPLES</span></span>

### <span data-ttu-id="55c28-112">Exempel 1: uppdatera en befintlig främre dörr med FrontDoorName och ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="55c28-112">Example 1: update an existing Front Door with FrontDoorName and ResourceGroupName.</span></span>
```powershell
PS C:\> Set-AzureRmFrontDoor -Name "frontDoor1" -ResourceGroupName "resourceGroup1" -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

FriendlyName          : frontdoor1
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/{guid}/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

<span data-ttu-id="55c28-113">uppdatera en befintlig FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="55c28-113">update an existing FrontDoor.</span></span>

### <span data-ttu-id="55c28-114">Exempel 2: uppdatera en befintlig främre dörr med PSFrontDoor-objekt.</span><span class="sxs-lookup"><span data-stu-id="55c28-114">Example 2: update an existing Front Door with PSFrontDoor object.</span></span>
```powershell
PS C:\>  Set-AzureRmFrontDoor -InputObject $frontDoor1 -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

FriendlyName          : frontdoor1
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/{guid}/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

<span data-ttu-id="55c28-115">uppdatera en befintlig FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="55c28-115">update an existing FrontDoor.</span></span>

### <span data-ttu-id="55c28-116">Exempel 3: uppdatera en befintlig främre dörr med ResourceId</span><span class="sxs-lookup"><span data-stu-id="55c28-116">Example 3: update an existing Front Door with ResourceId</span></span>
```powershell
PS C:\>  Set-AzureRmFrontDoor -ResourceId {resourceId} -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

FriendlyName          : frontdoor1
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/{guid}/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

<span data-ttu-id="55c28-117">uppdatera en befintlig FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="55c28-117">update an existing FrontDoor.</span></span>

## <span data-ttu-id="55c28-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="55c28-118">PARAMETERS</span></span>

### <span data-ttu-id="55c28-119">-BackendPool</span><span class="sxs-lookup"><span data-stu-id="55c28-119">-BackendPool</span></span>
<span data-ttu-id="55c28-120">Backendpools är tillgänglig för regel för routning.</span><span class="sxs-lookup"><span data-stu-id="55c28-120">Backendpools available to routing rule.</span></span>

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

### <span data-ttu-id="55c28-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55c28-121">-DefaultProfile</span></span>
<span data-ttu-id="55c28-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="55c28-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55c28-123">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="55c28-123">-EnabledState</span></span>
<span data-ttu-id="55c28-124">Drift status för belastnings utjämning för Last luckan.</span><span class="sxs-lookup"><span data-stu-id="55c28-124">Operational status of the Front Door load balancer.</span></span>

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

### <span data-ttu-id="55c28-125">-FrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="55c28-125">-FrontendEndpoint</span></span>
<span data-ttu-id="55c28-126">Klient delens slut punkter är tillgängliga för regel för routning.</span><span class="sxs-lookup"><span data-stu-id="55c28-126">Frontend endpoints available to routing rule.</span></span>

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

### <span data-ttu-id="55c28-127">-HealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="55c28-127">-HealthProbeSetting</span></span>
<span data-ttu-id="55c28-128">Inställningar för hälso sökning som är kopplade till denna instans av front dörren.</span><span class="sxs-lookup"><span data-stu-id="55c28-128">Health probe settings associated with this Front Door instance.</span></span>

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

### <span data-ttu-id="55c28-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="55c28-129">-InputObject</span></span>
<span data-ttu-id="55c28-130">Objekt för front dörr att uppdatera.</span><span class="sxs-lookup"><span data-stu-id="55c28-130">The Front Door object to update.</span></span>

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

### <span data-ttu-id="55c28-131">-LoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="55c28-131">-LoadBalancingSetting</span></span>
<span data-ttu-id="55c28-132">Inställningar för belastnings utjämning som är kopplade till den här instansen.</span><span class="sxs-lookup"><span data-stu-id="55c28-132">Load balancing settings associated with this Front Door instance.</span></span>

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

### <span data-ttu-id="55c28-133">-Namn</span><span class="sxs-lookup"><span data-stu-id="55c28-133">-Name</span></span>
<span data-ttu-id="55c28-134">Namnet på den främre dörren som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="55c28-134">The name of the Front Door to update.</span></span>

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

### <span data-ttu-id="55c28-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55c28-135">-ResourceGroupName</span></span>
<span data-ttu-id="55c28-136">Den resurs grupp som front dörren tillhör.</span><span class="sxs-lookup"><span data-stu-id="55c28-136">The resource group to which the Front Door belongs.</span></span>

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

### <span data-ttu-id="55c28-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="55c28-137">-ResourceId</span></span>
<span data-ttu-id="55c28-138">Resurs-ID för den främre dörren som ska uppdateras</span><span class="sxs-lookup"><span data-stu-id="55c28-138">Resource Id of the Front Door to update</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55c28-139">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="55c28-139">-RoutingRule</span></span>
<span data-ttu-id="55c28-140">Routningsregler som är associerade med den här FrontDoor</span><span class="sxs-lookup"><span data-stu-id="55c28-140">Routing rules associated with this FrontDoor</span></span>

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

### <span data-ttu-id="55c28-141">-Tagg</span><span class="sxs-lookup"><span data-stu-id="55c28-141">-Tag</span></span>
<span data-ttu-id="55c28-142">Taggarna som är kopplade till FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="55c28-142">The tags associate with the FrontDoor.</span></span>

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

### <span data-ttu-id="55c28-143">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="55c28-143">-Confirm</span></span>
<span data-ttu-id="55c28-144">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="55c28-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55c28-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55c28-145">-WhatIf</span></span>
<span data-ttu-id="55c28-146">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="55c28-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55c28-147">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="55c28-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55c28-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55c28-148">CommonParameters</span></span>
<span data-ttu-id="55c28-149">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55c28-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55c28-150">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55c28-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55c28-151">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="55c28-151">INPUTS</span></span>

### <span data-ttu-id="55c28-152">Microsoft. Azure. commands. FrontDoor. Models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="55c28-152">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

### <span data-ttu-id="55c28-153">System. String</span><span class="sxs-lookup"><span data-stu-id="55c28-153">System.String</span></span>

## <span data-ttu-id="55c28-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="55c28-154">OUTPUTS</span></span>

### <span data-ttu-id="55c28-155">Microsoft. Azure. commands. FrontDoor. Models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="55c28-155">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

## <span data-ttu-id="55c28-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="55c28-156">NOTES</span></span>

## <span data-ttu-id="55c28-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="55c28-157">RELATED LINKS</span></span>

<span data-ttu-id="55c28-158">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md) 
 [Get-AzureRmFrontDoor](./Get-AzureRmFrontDoor.md) 
 [Remove-AzureRmFrontDoor](./Remove-AzureRmFrontDoor.md) 
 [New-AzureRmFrontDoorRoutingRuleObject](./New-AzureRmFrontDoorRoutingRuleObject.md) 
 [New-AzureRmFrontDoorHealthProbeSettingObject](./New-AzureRmFrontHealthProbeSettingObject.md) 
 [New-AzureRmFrontDoorLoadBalancingSettingObject](./New-AzureRmFrontDoorLoadBalancingSettingObject.md) 
 [New-AzureRmFrontDoorFrontendEndpointObject](./New-AzureRmFrontDoorFrontendEndpointObject.md) 
 [New-AzureRmFrontDoorBackendPoolObject](./New-AzureRmFrontDoorBackendPoolObject.md)</span><span class="sxs-lookup"><span data-stu-id="55c28-158">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md)
[Get-AzureRmFrontDoor](./Get-AzureRmFrontDoor.md)
[Remove-AzureRmFrontDoor](./Remove-AzureRmFrontDoor.md)
[New-AzureRmFrontDoorRoutingRuleObject](./New-AzureRmFrontDoorRoutingRuleObject.md)
[New-AzureRmFrontDoorHealthProbeSettingObject](./New-AzureRmFrontHealthProbeSettingObject.md)
[New-AzureRmFrontDoorLoadBalancingSettingObject](./New-AzureRmFrontDoorLoadBalancingSettingObject.md)
[New-AzureRmFrontDoorFrontendEndpointObject](./New-AzureRmFrontDoorFrontendEndpointObject.md)
[New-AzureRmFrontDoorBackendPoolObject](./New-AzureRmFrontDoorBackendPoolObject.md)</span></span>
