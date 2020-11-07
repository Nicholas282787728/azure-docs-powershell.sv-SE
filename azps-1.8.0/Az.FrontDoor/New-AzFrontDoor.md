---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoor.md
ms.openlocfilehash: cea5b69b279b6f7f7a8e783d4ed328237377c18f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916758"
---
# <span data-ttu-id="3d555-101">New-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="3d555-101">New-AzFrontDoor</span></span>

## <span data-ttu-id="3d555-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3d555-102">SYNOPSIS</span></span>
<span data-ttu-id="3d555-103">Skapa en ny laddnings sal Don för Azure front dörren</span><span class="sxs-lookup"><span data-stu-id="3d555-103">Create a new Azure Front Door load balancer</span></span>

## <span data-ttu-id="3d555-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3d555-104">SYNTAX</span></span>

```
New-AzFrontDoor -ResourceGroupName <String> -Name <String> -RoutingRule <PSRoutingRule[]>
 -BackendPool <PSBackendPool[]> -FrontendEndpoint <PSFrontendEndpoint[]>
 -LoadBalancingSetting <PSLoadBalancingSetting[]> -HealthProbeSetting <PSHealthProbeSetting[]>
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DisableCertificateNameCheck]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d555-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3d555-105">DESCRIPTION</span></span>
<span data-ttu-id="3d555-106">Cmdleten **New-AzFrontDoor** skapar en ny Azure-startlucka i den angivna resurs gruppen under aktuell prenumeration</span><span class="sxs-lookup"><span data-stu-id="3d555-106">The **New-AzFrontDoor** cmdlet creates a new Azure Front Door load balancer in the specified resource group under current subscription</span></span>

## <span data-ttu-id="3d555-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3d555-107">EXAMPLES</span></span>

### <span data-ttu-id="3d555-108">Exempel 1: skapa en front dörr baserat på angivna parametrar.</span><span class="sxs-lookup"><span data-stu-id="3d555-108">Example 1: Create a Front Door based on given parameters.</span></span>
```powershell
PS C:\> New-AzFrontDoor -Name "frontDoor1" -ResourceGroupName "rg1" -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

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
Id                          : /subscriptions/{guid}/resourcegroups/rg1/providers/Microsoft.Network/frontdoors/frontdoor1
Name                        : frontdoor1
Type                        : Microsoft.Network/frontdoors
```

<span data-ttu-id="3d555-109">Skapa en front dörr baserat på angivna parametrar.</span><span class="sxs-lookup"><span data-stu-id="3d555-109">Create a Front Door based on given parameters.</span></span>

## <span data-ttu-id="3d555-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3d555-110">PARAMETERS</span></span>

### <span data-ttu-id="3d555-111">-BackendPool</span><span class="sxs-lookup"><span data-stu-id="3d555-111">-BackendPool</span></span>
<span data-ttu-id="3d555-112">Backendpools är tillgänglig för regel för routning.</span><span class="sxs-lookup"><span data-stu-id="3d555-112">Backendpools available to routing rule.</span></span>

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

### <span data-ttu-id="3d555-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d555-113">-DefaultProfile</span></span>
<span data-ttu-id="3d555-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3d555-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d555-115">-DisableCertificateNameCheck</span><span class="sxs-lookup"><span data-stu-id="3d555-115">-DisableCertificateNameCheck</span></span>
<span data-ttu-id="3d555-116">Om du vill inaktivera certifikat namns kontroll för HTTPS-begäranden till alla backend-pooler.</span><span class="sxs-lookup"><span data-stu-id="3d555-116">Whether to disable certificate name check on HTTPS requests to all backend pools.</span></span> <span data-ttu-id="3d555-117">Ingen effekt på icke-HTTPS-begäranden.</span><span class="sxs-lookup"><span data-stu-id="3d555-117">No effect on non-HTTPS requests.</span></span>

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

### <span data-ttu-id="3d555-118">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="3d555-118">-EnabledState</span></span>
<span data-ttu-id="3d555-119">EnabledState för belastnings utjämning för Last luckan.</span><span class="sxs-lookup"><span data-stu-id="3d555-119">EnabledState of the Front Door load balancer.</span></span>
<span data-ttu-id="3d555-120">Standardvärdet är aktiverat</span><span class="sxs-lookup"><span data-stu-id="3d555-120">Default value is Enabled</span></span>

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

### <span data-ttu-id="3d555-121">-FrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="3d555-121">-FrontendEndpoint</span></span>
<span data-ttu-id="3d555-122">Klient delens slut punkter är tillgängliga för regel för routning.</span><span class="sxs-lookup"><span data-stu-id="3d555-122">Frontend endpoints available to routing rule.</span></span>

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

### <span data-ttu-id="3d555-123">-HealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="3d555-123">-HealthProbeSetting</span></span>
<span data-ttu-id="3d555-124">Inställningar för hälso sökning som är kopplade till denna instans av front dörren.</span><span class="sxs-lookup"><span data-stu-id="3d555-124">Health probe settings associated with this Front Door instance.</span></span>

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

### <span data-ttu-id="3d555-125">-LoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="3d555-125">-LoadBalancingSetting</span></span>
<span data-ttu-id="3d555-126">Inställningar för belastnings utjämning som är kopplade till den här instansen.</span><span class="sxs-lookup"><span data-stu-id="3d555-126">Load balancing settings associated with this Front Door instance.</span></span>

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

### <span data-ttu-id="3d555-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="3d555-127">-Name</span></span>
<span data-ttu-id="3d555-128">Namn på främre dörren.</span><span class="sxs-lookup"><span data-stu-id="3d555-128">Front Door name.</span></span>

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

### <span data-ttu-id="3d555-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d555-129">-ResourceGroupName</span></span>
<span data-ttu-id="3d555-130">Namnet på den resurs grupp som ska skapas i.</span><span class="sxs-lookup"><span data-stu-id="3d555-130">The resource group name that the Front Door will be created in.</span></span>

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

### <span data-ttu-id="3d555-131">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="3d555-131">-RoutingRule</span></span>
<span data-ttu-id="3d555-132">Routningsregler som är associerade med den här FrontDoor</span><span class="sxs-lookup"><span data-stu-id="3d555-132">Routing rules associated with this FrontDoor</span></span>

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

### <span data-ttu-id="3d555-133">-Tagg</span><span class="sxs-lookup"><span data-stu-id="3d555-133">-Tag</span></span>
<span data-ttu-id="3d555-134">Taggarna som är kopplade till FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="3d555-134">The tags associate with the FrontDoor.</span></span>

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

### <span data-ttu-id="3d555-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3d555-135">-Confirm</span></span>
<span data-ttu-id="3d555-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3d555-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d555-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d555-137">-WhatIf</span></span>
<span data-ttu-id="3d555-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3d555-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d555-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3d555-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d555-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d555-140">CommonParameters</span></span>
<span data-ttu-id="3d555-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d555-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d555-142">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3d555-142">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d555-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3d555-143">INPUTS</span></span>

### <span data-ttu-id="3d555-144">Ingen</span><span class="sxs-lookup"><span data-stu-id="3d555-144">None</span></span>

## <span data-ttu-id="3d555-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3d555-145">OUTPUTS</span></span>

### <span data-ttu-id="3d555-146">Microsoft. Azure. commands. FrontDoor. Models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="3d555-146">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

## <span data-ttu-id="3d555-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3d555-147">NOTES</span></span>

## <span data-ttu-id="3d555-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3d555-148">RELATED LINKS</span></span>

<span data-ttu-id="3d555-149">[Get-AzFrontDoor](./Get-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md) 
 [Remove-AzFrontDoor](./Remove-AzFrontDoor.md) 
 [New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md) 
 [New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md) 
 [New-AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md) 
 [New-AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md) 
 [New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span><span class="sxs-lookup"><span data-stu-id="3d555-149">[Get-AzFrontDoor](./Get-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)
[Remove-AzFrontDoor](./Remove-AzFrontDoor.md)
[New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md)
[New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md)
[New-AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md)
[New-AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md)
[New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span></span>