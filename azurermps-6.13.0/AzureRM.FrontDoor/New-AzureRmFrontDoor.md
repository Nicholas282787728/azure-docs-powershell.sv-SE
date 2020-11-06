---
<span data-ttu-id="634e5-101">extern hjälpfil: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml modulens namn: AzureRM. FrontDoor online-version: motsvarande URL ska vara följande: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoor schema: 2.0.0 content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoor.md original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoor.md</span><span class="sxs-lookup"><span data-stu-id="634e5-101">external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml Module Name: AzureRM.FrontDoor online version: The corresponding URL should be the following: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoor schema: 2.0.0 content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoor.md original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoor.md</span></span>
---

# <a name="new-azurermfrontdoor"></a><span data-ttu-id="634e5-102">New-AzureRmFrontDoor</span><span class="sxs-lookup"><span data-stu-id="634e5-102">New-AzureRmFrontDoor</span></span>

## <a name="synopsis"></a><span data-ttu-id="634e5-103">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="634e5-103">SYNOPSIS</span></span>
<span data-ttu-id="634e5-104">Skapa en ny laddnings sal Don för Azure front dörren</span><span class="sxs-lookup"><span data-stu-id="634e5-104">Create a new Azure Front Door load balancer</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <a name="syntax"></a><span data-ttu-id="634e5-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="634e5-105">SYNTAX</span></span>

```
New-AzureRmFrontDoor -ResourceGroupName <String> -Name <String> -RoutingRule <PSRoutingRule[]>
 -BackendPool <PSBackendPool[]> -FrontendEndpoint <PSFrontendEndpoint[]>
 -LoadBalancingSetting <PSLoadBalancingSetting[]> -HealthProbeSetting <PSHealthProbeSetting[]>
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <a name="description"></a><span data-ttu-id="634e5-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="634e5-106">DESCRIPTION</span></span>
<span data-ttu-id="634e5-107">Cmdleten **New-AzureRmFrontDoor** skapar en ny Azure-startlucka i den angivna resurs gruppen under aktuell prenumeration</span><span class="sxs-lookup"><span data-stu-id="634e5-107">The **New-AzureRmFrontDoor** cmdlet creates a new Azure Front Door load balancer in the specified resource group under current subscription</span></span>

## <a name="examples"></a><span data-ttu-id="634e5-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="634e5-108">EXAMPLES</span></span>

### <a name="example-1-create-a-front-door-based-on-given-parameters"></a><span data-ttu-id="634e5-109">Exempel 1: skapa en front dörr baserat på angivna parametrar.</span><span class="sxs-lookup"><span data-stu-id="634e5-109">Example 1: Create a Front Door based on given parameters.</span></span>
```powershell
PS C:\> New-AzureRmFrontDoor -Name "frontDoor1" -ResourceGroupName "rg1" -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

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
Id                    : /subscriptions/{guid}/resourcegroups/rg1/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

<span data-ttu-id="634e5-110">Skapa en front dörr baserat på angivna parametrar.</span><span class="sxs-lookup"><span data-stu-id="634e5-110">Create a Front Door based on given parameters.</span></span>

## <a name="parameters"></a><span data-ttu-id="634e5-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="634e5-111">PARAMETERS</span></span>

### <a name="-backendpool"></a><span data-ttu-id="634e5-112">-BackendPool</span><span class="sxs-lookup"><span data-stu-id="634e5-112">-BackendPool</span></span>
<span data-ttu-id="634e5-113">Backendpools är tillgänglig för regel för routning.</span><span class="sxs-lookup"><span data-stu-id="634e5-113">Backendpools available to routing rule.</span></span>

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

### <a name="-defaultprofile"></a><span data-ttu-id="634e5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="634e5-114">-DefaultProfile</span></span>
<span data-ttu-id="634e5-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="634e5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <a name="-enabledstate"></a><span data-ttu-id="634e5-116">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="634e5-116">-EnabledState</span></span>
<span data-ttu-id="634e5-117">EnabledState för belastnings utjämning för Last luckan.</span><span class="sxs-lookup"><span data-stu-id="634e5-117">EnabledState of the Front Door load balancer.</span></span>
<span data-ttu-id="634e5-118">Standardvärdet är aktiverat</span><span class="sxs-lookup"><span data-stu-id="634e5-118">Default value is Enabled</span></span>

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

### <a name="-frontendendpoint"></a><span data-ttu-id="634e5-119">-FrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="634e5-119">-FrontendEndpoint</span></span>
<span data-ttu-id="634e5-120">Klient delens slut punkter är tillgängliga för regel för routning.</span><span class="sxs-lookup"><span data-stu-id="634e5-120">Frontend endpoints available to routing rule.</span></span>

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

### <a name="-healthprobesetting"></a><span data-ttu-id="634e5-121">-HealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="634e5-121">-HealthProbeSetting</span></span>
<span data-ttu-id="634e5-122">Inställningar för hälso sökning som är kopplade till denna instans av front dörren.</span><span class="sxs-lookup"><span data-stu-id="634e5-122">Health probe settings associated with this Front Door instance.</span></span>

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

### <a name="-loadbalancingsetting"></a><span data-ttu-id="634e5-123">-LoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="634e5-123">-LoadBalancingSetting</span></span>
<span data-ttu-id="634e5-124">Inställningar för belastnings utjämning som är kopplade till den här instansen.</span><span class="sxs-lookup"><span data-stu-id="634e5-124">Load balancing settings associated with this Front Door instance.</span></span>

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

### <a name="-name"></a><span data-ttu-id="634e5-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="634e5-125">-Name</span></span>
<span data-ttu-id="634e5-126">Namn på främre dörren.</span><span class="sxs-lookup"><span data-stu-id="634e5-126">Front Door name.</span></span>

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

### <a name="-resourcegroupname"></a><span data-ttu-id="634e5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="634e5-127">-ResourceGroupName</span></span>
<span data-ttu-id="634e5-128">Namnet på den resurs grupp som ska skapas i.</span><span class="sxs-lookup"><span data-stu-id="634e5-128">The resource group name that the Front Door will be created in.</span></span>

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

### <a name="-routingrule"></a><span data-ttu-id="634e5-129">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="634e5-129">-RoutingRule</span></span>
<span data-ttu-id="634e5-130">Routningsregler som är associerade med den här FrontDoor</span><span class="sxs-lookup"><span data-stu-id="634e5-130">Routing rules associated with this FrontDoor</span></span>

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

### <a name="-tag"></a><span data-ttu-id="634e5-131">-Tagg</span><span class="sxs-lookup"><span data-stu-id="634e5-131">-Tag</span></span>
<span data-ttu-id="634e5-132">Taggarna som är kopplade till FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="634e5-132">The tags associate with the FrontDoor.</span></span>

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

### <a name="-confirm"></a><span data-ttu-id="634e5-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="634e5-133">-Confirm</span></span>
<span data-ttu-id="634e5-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="634e5-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <a name="-whatif"></a><span data-ttu-id="634e5-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="634e5-135">-WhatIf</span></span>
<span data-ttu-id="634e5-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="634e5-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="634e5-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="634e5-137">The cmdlet is not run.</span></span>

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

### <a name="commonparameters"></a><span data-ttu-id="634e5-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="634e5-138">CommonParameters</span></span>
<span data-ttu-id="634e5-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="634e5-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="634e5-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="634e5-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <a name="inputs"></a><span data-ttu-id="634e5-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="634e5-141">INPUTS</span></span>

### <a name="systemstring"></a><span data-ttu-id="634e5-142">System. String</span><span class="sxs-lookup"><span data-stu-id="634e5-142">System.String</span></span>

## <a name="outputs"></a><span data-ttu-id="634e5-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="634e5-143">OUTPUTS</span></span>

### <a name="microsoftazurecommandsfrontdoormodelspsfrontdoor"></a><span data-ttu-id="634e5-144">Microsoft. Azure. commands. FrontDoor. Models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="634e5-144">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

## <a name="notes"></a><span data-ttu-id="634e5-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="634e5-145">NOTES</span></span>

## <a name="related-links"></a><span data-ttu-id="634e5-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="634e5-146">RELATED LINKS</span></span>

<span data-ttu-id="634e5-147">[Get-AzureRmFrontDoor](./Get-AzureRmFrontDoor.md) 
 [Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md) 
 [Remove-AzureRmFrontDoor](./Remove-AzureRmFrontDoor.md) 
 [New-AzureRmFrontDoorRoutingRuleObject](./New-AzureRmFrontDoorRoutingRuleObject.md) 
 [New-AzureRmFrontDoorHealthProbeSettingObject](./New-AzureRmFrontHealthProbeSettingObject.md) 
 [New-AzureRmFrontDoorLoadBalancingSettingObject](./New-AzureRmFrontDoorLoadBalancingSettingObject.md) 
 [New-AzureRmFrontDoorFrontendEndpointObject](./New-AzureRmFrontDoorFrontendEndpointObject.md) 
 [New-AzureRmFrontDoorBackendPoolObject](./New-AzureRmFrontDoorBackendPoolObject.md)</span><span class="sxs-lookup"><span data-stu-id="634e5-147">[Get-AzureRmFrontDoor](./Get-AzureRmFrontDoor.md)
[Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)
[Remove-AzureRmFrontDoor](./Remove-AzureRmFrontDoor.md)
[New-AzureRmFrontDoorRoutingRuleObject](./New-AzureRmFrontDoorRoutingRuleObject.md)
[New-AzureRmFrontDoorHealthProbeSettingObject](./New-AzureRmFrontHealthProbeSettingObject.md)
[New-AzureRmFrontDoorLoadBalancingSettingObject](./New-AzureRmFrontDoorLoadBalancingSettingObject.md)
[New-AzureRmFrontDoorFrontendEndpointObject](./New-AzureRmFrontDoorFrontendEndpointObject.md)
[New-AzureRmFrontDoorBackendPoolObject](./New-AzureRmFrontDoorBackendPoolObject.md)</span></span>
