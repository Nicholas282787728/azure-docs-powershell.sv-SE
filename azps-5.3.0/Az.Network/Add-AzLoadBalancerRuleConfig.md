---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2AE5E9B8-7344-407B-9317-47709F10FCD8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 5965cd5e27c5e408f7b55ea5d181dc8670668168
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98522490"
---
# <span data-ttu-id="0d956-101">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0d956-101">Add-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="0d956-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0d956-102">SYNOPSIS</span></span>
<span data-ttu-id="0d956-103">Lägger till en regel konfiguration i en belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="0d956-103">Adds a rule configuration to a load balancer.</span></span>

## <span data-ttu-id="0d956-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0d956-104">SYNTAX</span></span>

### <span data-ttu-id="0d956-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="0d956-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d956-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="0d956-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d956-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0d956-107">DESCRIPTION</span></span>
<span data-ttu-id="0d956-108">Cmdleten **Add-AzLoadBalancerRuleConfig** lägger till en regel konfiguration i en Azure-belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="0d956-108">The **Add-AzLoadBalancerRuleConfig** cmdlet adds a rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="0d956-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0d956-109">EXAMPLES</span></span>

### <span data-ttu-id="0d956-110">Exempel 1: lägga till en regel konfiguration i en belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="0d956-110">Example 1: Add a rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\>$slb | Set-AzLoadBalancer
```

<span data-ttu-id="0d956-111">Det första kommandot får belastningsutjämnaren med namnet MyLoadBalancer och lagrar det sedan i variabeln $slb.</span><span class="sxs-lookup"><span data-stu-id="0d956-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="0d956-112">I det andra kommandot används pipeline-operatorn för att överföra belastningsutjämnaren i $slb till **Add-AzLoadBalancerRuleConfig**, som lägger till regel konfigurationen med namnet NewRule.</span><span class="sxs-lookup"><span data-stu-id="0d956-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzLoadBalancerRuleConfig**, which adds the rule configuration named NewRule.</span></span>
<span data-ttu-id="0d956-113">Det tredje kommandot uppdaterar belastningsutjämnaren i Azure med den nya regeln för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="0d956-113">The third command will update the load balancer in azure with the new Load Balancer Rule Config.</span></span>

## <span data-ttu-id="0d956-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0d956-114">PARAMETERS</span></span>

### <span data-ttu-id="0d956-115">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="0d956-115">-BackendAddressPool</span></span>
<span data-ttu-id="0d956-116">Anger Server delens adresspool för att associera med en regel konfiguration för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="0d956-116">Specifies the backend address pool to associate with a load balancer rule configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d956-117">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="0d956-117">-BackendAddressPoolId</span></span>
<span data-ttu-id="0d956-118">Anger ID för ett **BackendAddressPool** -objekt som ska kopplas till en regel konfiguration för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="0d956-118">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d956-119">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="0d956-119">-BackendPort</span></span>
<span data-ttu-id="0d956-120">Anger Server dels porten för trafik som matchas av en regel för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="0d956-120">Specifies the backend port for traffic that is matched by a load balancer rule configuration.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d956-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d956-121">-DefaultProfile</span></span>
<span data-ttu-id="0d956-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0d956-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d956-123">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="0d956-123">-DisableOutboundSNAT</span></span>
<span data-ttu-id="0d956-124">Konfigurerar SNAT för de virtuella datorerna i backend-poolen till att använda den publicIP-adress som anges i klient delen av regeln för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="0d956-124">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="0d956-125">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="0d956-125">-EnableFloatingIP</span></span>
<span data-ttu-id="0d956-126">Anger att denna cmdlet aktiverar en flytande IP-adress för en regel konfiguration.</span><span class="sxs-lookup"><span data-stu-id="0d956-126">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="0d956-127">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="0d956-127">-EnableTcpReset</span></span>
<span data-ttu-id="0d956-128">Ta emot dubbelriktad TCP-återställning i TCP-flödets tids gräns för inaktivitet eller oväntat upphör Ande.</span><span class="sxs-lookup"><span data-stu-id="0d956-128">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="0d956-129">Det här elementet används bara när protokollet är inställt på TCP.</span><span class="sxs-lookup"><span data-stu-id="0d956-129">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="0d956-130">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="0d956-130">-FrontendIpConfiguration</span></span>
<span data-ttu-id="0d956-131">Anger en lista över de front-IP-adresser som är associerade med en regel konfiguration för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="0d956-131">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d956-132">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="0d956-132">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="0d956-133">Anger ID för en front-IP-adresskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="0d956-133">Specifies the ID for a front-end IP address configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d956-134">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="0d956-134">-FrontendPort</span></span>
<span data-ttu-id="0d956-135">Anger front porten som matchas av en regel för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="0d956-135">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d956-136">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="0d956-136">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="0d956-137">Anger hur lång tid, i minuter, som status för konversationer ska behållas i belastningsutjämnaren.</span><span class="sxs-lookup"><span data-stu-id="0d956-137">Specifies the length of time, in minutes, that the state of conversations is maintained in the load balancer.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d956-138">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0d956-138">-LoadBalancer</span></span>
<span data-ttu-id="0d956-139">Anger ett **Loadbalancer** -objekt.</span><span class="sxs-lookup"><span data-stu-id="0d956-139">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="0d956-140">Denna cmdlet lägger till en regel konfiguration i belastningsutjämnaren som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="0d956-140">This cmdlet adds a rule configuration to the load balancer that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d956-141">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="0d956-141">-LoadDistribution</span></span>
<span data-ttu-id="0d956-142">Anger en belastnings fördelning.</span><span class="sxs-lookup"><span data-stu-id="0d956-142">Specifies a load distribution.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d956-143">-Namn</span><span class="sxs-lookup"><span data-stu-id="0d956-143">-Name</span></span>
<span data-ttu-id="0d956-144">Anger namnet på regeln för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="0d956-144">Specifies the name of the load balancer rule configuration.</span></span>

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

### <span data-ttu-id="0d956-145">-Sond</span><span class="sxs-lookup"><span data-stu-id="0d956-145">-Probe</span></span>
<span data-ttu-id="0d956-146">Anger en sond som associeras med en regel konfiguration för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="0d956-146">Specifies a probe to associate with a load balancer rule configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSProbe
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d956-147">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="0d956-147">-ProbeId</span></span>
<span data-ttu-id="0d956-148">Anger ID för den sond som ska kopplas till en regel konfiguration för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="0d956-148">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d956-149">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="0d956-149">-Protocol</span></span>
<span data-ttu-id="0d956-150">Anger det protokoll som matchas med en regel för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="0d956-150">Specifies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="0d956-151">De acceptabla värdena för denna parameter är: TCP eller UDP.</span><span class="sxs-lookup"><span data-stu-id="0d956-151">The acceptable values for this parameter are: Tcp or Udp.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d956-152">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0d956-152">-Confirm</span></span>
<span data-ttu-id="0d956-153">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0d956-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d956-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d956-154">-WhatIf</span></span>
<span data-ttu-id="0d956-155">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0d956-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0d956-156">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0d956-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d956-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d956-157">CommonParameters</span></span>
<span data-ttu-id="0d956-158">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d956-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d956-159">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d956-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d956-160">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0d956-160">INPUTS</span></span>

### <span data-ttu-id="0d956-161">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0d956-161">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="0d956-162">System. String</span><span class="sxs-lookup"><span data-stu-id="0d956-162">System.String</span></span>

### <span data-ttu-id="0d956-163">System. Int32</span><span class="sxs-lookup"><span data-stu-id="0d956-163">System.Int32</span></span>

### <span data-ttu-id="0d956-164">Microsoft. Azure. commands. Networks. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="0d956-164">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

### <span data-ttu-id="0d956-165">Microsoft. Azure. commands. Networks. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="0d956-165">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

### <span data-ttu-id="0d956-166">Microsoft. Azure. commands. Networks. Models. PSProbe</span><span class="sxs-lookup"><span data-stu-id="0d956-166">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="0d956-167">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0d956-167">OUTPUTS</span></span>

### <span data-ttu-id="0d956-168">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0d956-168">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="0d956-169">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0d956-169">NOTES</span></span>

## <span data-ttu-id="0d956-170">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0d956-170">RELATED LINKS</span></span>

[<span data-ttu-id="0d956-171">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0d956-171">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="0d956-172">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0d956-172">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="0d956-173">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0d956-173">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="0d956-174">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0d956-174">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="0d956-175">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0d956-175">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


