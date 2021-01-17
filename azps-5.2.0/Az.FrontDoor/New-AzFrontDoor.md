---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoor.md
ms.openlocfilehash: 3f08ada3dd485a1e18bb6f0a91037ba1df0b5f25
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98405216"
---
# <span data-ttu-id="92b5c-101">New-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="92b5c-101">New-AzFrontDoor</span></span>

## <span data-ttu-id="92b5c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="92b5c-102">SYNOPSIS</span></span>
<span data-ttu-id="92b5c-103">Skapa en ny laddnings sal Don för Azure front dörren</span><span class="sxs-lookup"><span data-stu-id="92b5c-103">Create a new Azure Front Door load balancer</span></span>

## <span data-ttu-id="92b5c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="92b5c-104">SYNTAX</span></span>

### <span data-ttu-id="92b5c-105">ByFieldsWithBackendPoolsSettingParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="92b5c-105">ByFieldsWithBackendPoolsSettingParameterSet (Default)</span></span>
```
New-AzFrontDoor -ResourceGroupName <String> -Name <String> -RoutingRule <PSRoutingRule[]>
 -BackendPool <PSBackendPool[]> -FrontendEndpoint <PSFrontendEndpoint[]>
 -LoadBalancingSetting <PSLoadBalancingSetting[]> -HealthProbeSetting <PSHealthProbeSetting[]>
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-BackendPoolsSetting <PSBackendPoolsSetting>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92b5c-106">ByFieldsWithCertificateNameCheckParameterSet</span><span class="sxs-lookup"><span data-stu-id="92b5c-106">ByFieldsWithCertificateNameCheckParameterSet</span></span>
```
New-AzFrontDoor -ResourceGroupName <String> -Name <String> -RoutingRule <PSRoutingRule[]>
 -BackendPool <PSBackendPool[]> -FrontendEndpoint <PSFrontendEndpoint[]>
 -LoadBalancingSetting <PSLoadBalancingSetting[]> -HealthProbeSetting <PSHealthProbeSetting[]>
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DisableCertificateNameCheck]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92b5c-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="92b5c-107">DESCRIPTION</span></span>
<span data-ttu-id="92b5c-108">Cmdleten **New-AzFrontDoor** skapar en ny Azure-startlucka i den angivna resurs gruppen under aktuell prenumeration</span><span class="sxs-lookup"><span data-stu-id="92b5c-108">The **New-AzFrontDoor** cmdlet creates a new Azure Front Door load balancer in the specified resource group under current subscription</span></span>

## <span data-ttu-id="92b5c-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="92b5c-109">EXAMPLES</span></span>

### <span data-ttu-id="92b5c-110">Exempel 1: skapa en front dörr baserat på angivna parametrar.</span><span class="sxs-lookup"><span data-stu-id="92b5c-110">Example 1: Create a Front Door based on given parameters.</span></span>
```powershell
PS C:\> New-AzFrontDoor -Name "frontDoor1" -ResourceGroupName "rg1" -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1 -BackendPoolsSetting $backendPoolsSetting1

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
Id                          : /subscriptions/{guid}/resourcegroups/rg1/providers/Microsoft.Network/frontdoors/frontdoor1
Name                        : frontdoor1
Type                        : Microsoft.Network/frontdoors
```

<span data-ttu-id="92b5c-111">Skapa en front dörr baserat på angivna parametrar.</span><span class="sxs-lookup"><span data-stu-id="92b5c-111">Create a Front Door based on given parameters.</span></span>

## <span data-ttu-id="92b5c-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="92b5c-112">PARAMETERS</span></span>

### <span data-ttu-id="92b5c-113">-BackendPool</span><span class="sxs-lookup"><span data-stu-id="92b5c-113">-BackendPool</span></span>
<span data-ttu-id="92b5c-114">Backendpools är tillgänglig för regel för routning.</span><span class="sxs-lookup"><span data-stu-id="92b5c-114">Backendpools available to routing rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPool[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92b5c-115">-BackendPoolsSetting</span><span class="sxs-lookup"><span data-stu-id="92b5c-115">-BackendPoolsSetting</span></span>
<span data-ttu-id="92b5c-116">Inställningar för alla backendPools</span><span class="sxs-lookup"><span data-stu-id="92b5c-116">Settings for all backendPools</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPoolsSetting
Parameter Sets: ByFieldsWithBackendPoolsSettingParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92b5c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92b5c-117">-DefaultProfile</span></span>
<span data-ttu-id="92b5c-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="92b5c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92b5c-119">-DisableCertificateNameCheck</span><span class="sxs-lookup"><span data-stu-id="92b5c-119">-DisableCertificateNameCheck</span></span>
<span data-ttu-id="92b5c-120">Om du vill inaktivera certifikat namns kontroll för HTTPS-begäranden till alla backend-pooler.</span><span class="sxs-lookup"><span data-stu-id="92b5c-120">Whether to disable certificate name check on HTTPS requests to all backend pools.</span></span> <span data-ttu-id="92b5c-121">Ingen effekt på icke-HTTPS-begäranden.</span><span class="sxs-lookup"><span data-stu-id="92b5c-121">No effect on non-HTTPS requests.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByFieldsWithCertificateNameCheckParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92b5c-122">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="92b5c-122">-EnabledState</span></span>
<span data-ttu-id="92b5c-123">EnabledState för belastnings utjämning för Last luckan.</span><span class="sxs-lookup"><span data-stu-id="92b5c-123">EnabledState of the Front Door load balancer.</span></span>
<span data-ttu-id="92b5c-124">Standardvärdet är aktiverat</span><span class="sxs-lookup"><span data-stu-id="92b5c-124">Default value is Enabled</span></span>

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

### <span data-ttu-id="92b5c-125">-FrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="92b5c-125">-FrontendEndpoint</span></span>
<span data-ttu-id="92b5c-126">Klient delens slut punkter är tillgängliga för regel för routning.</span><span class="sxs-lookup"><span data-stu-id="92b5c-126">Frontend endpoints available to routing rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92b5c-127">-HealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="92b5c-127">-HealthProbeSetting</span></span>
<span data-ttu-id="92b5c-128">Inställningar för hälso sökning som är kopplade till denna instans av front dörren.</span><span class="sxs-lookup"><span data-stu-id="92b5c-128">Health probe settings associated with this Front Door instance.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSHealthProbeSetting[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92b5c-129">-LoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="92b5c-129">-LoadBalancingSetting</span></span>
<span data-ttu-id="92b5c-130">Inställningar för belastnings utjämning som är kopplade till den här instansen.</span><span class="sxs-lookup"><span data-stu-id="92b5c-130">Load balancing settings associated with this Front Door instance.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSLoadBalancingSetting[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92b5c-131">-Namn</span><span class="sxs-lookup"><span data-stu-id="92b5c-131">-Name</span></span>
<span data-ttu-id="92b5c-132">Namn på främre dörren.</span><span class="sxs-lookup"><span data-stu-id="92b5c-132">Front Door name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92b5c-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92b5c-133">-ResourceGroupName</span></span>
<span data-ttu-id="92b5c-134">Namnet på den resurs grupp som ska skapas i.</span><span class="sxs-lookup"><span data-stu-id="92b5c-134">The resource group name that the Front Door will be created in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92b5c-135">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="92b5c-135">-RoutingRule</span></span>
<span data-ttu-id="92b5c-136">Routningsregler som är associerade med den här FrontDoor</span><span class="sxs-lookup"><span data-stu-id="92b5c-136">Routing rules associated with this FrontDoor</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRoutingRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92b5c-137">-Tagg</span><span class="sxs-lookup"><span data-stu-id="92b5c-137">-Tag</span></span>
<span data-ttu-id="92b5c-138">Taggarna som är kopplade till FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="92b5c-138">The tags associate with the FrontDoor.</span></span>

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

### <span data-ttu-id="92b5c-139">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="92b5c-139">-Confirm</span></span>
<span data-ttu-id="92b5c-140">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="92b5c-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92b5c-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92b5c-141">-WhatIf</span></span>
<span data-ttu-id="92b5c-142">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="92b5c-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92b5c-143">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="92b5c-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92b5c-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92b5c-144">CommonParameters</span></span>
<span data-ttu-id="92b5c-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92b5c-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92b5c-146">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="92b5c-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92b5c-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="92b5c-147">INPUTS</span></span>

### <span data-ttu-id="92b5c-148">Ingen</span><span class="sxs-lookup"><span data-stu-id="92b5c-148">None</span></span>
## <span data-ttu-id="92b5c-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="92b5c-149">OUTPUTS</span></span>

### <span data-ttu-id="92b5c-150">Microsoft. Azure. commands. FrontDoor. Models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="92b5c-150">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>
## <span data-ttu-id="92b5c-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="92b5c-151">NOTES</span></span>

## <span data-ttu-id="92b5c-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="92b5c-152">RELATED LINKS</span></span>

<span data-ttu-id="92b5c-153">[Get-AzFrontDoor](./Get-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md) 
 [Remove-AzFrontDoor](./Remove-AzFrontDoor.md) 
 [New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md) 
 [New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md) 
 [New-AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md) 
 [New-AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md) 
 [New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span><span class="sxs-lookup"><span data-stu-id="92b5c-153">[Get-AzFrontDoor](./Get-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)
[Remove-AzFrontDoor](./Remove-AzFrontDoor.md)
[New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md)
[New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md)
[New-AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md)
[New-AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md)
[New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span></span>