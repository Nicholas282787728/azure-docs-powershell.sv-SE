---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2638B226-B974-43B6-ACC2-D67573CF6B56
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 11baabe406180e92a4a6af0f62b5e3b285e016b6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747726"
---
# <span data-ttu-id="af802-101">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="af802-101">Set-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="af802-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="af802-102">SYNOPSIS</span></span>
<span data-ttu-id="af802-103">Uppdaterar en regel konfiguration för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="af802-103">Updates a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="af802-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="af802-104">SYNTAX</span></span>

### <span data-ttu-id="af802-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="af802-105">SetByResource (Default)</span></span>
```
Set-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af802-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="af802-106">SetByResourceId</span></span>
```
Set-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af802-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="af802-107">DESCRIPTION</span></span>
<span data-ttu-id="af802-108">Cmdleten **set-AzLoadBalancerRuleConfig** uppdaterar en regel konfiguration för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="af802-108">The **Set-AzLoadBalancerRuleConfig** cmdlet updates a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="af802-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="af802-109">EXAMPLES</span></span>

### <span data-ttu-id="af802-110">Exempel 1: ändra en regel för belastnings Utjämnings regler</span><span class="sxs-lookup"><span data-stu-id="af802-110">Example 1: Modify a load balancing rule configuration</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
```

<span data-ttu-id="af802-111">Det första kommandot får belastningsutjämnaren med namnet MyLoadBalancer och lagrar det sedan i $slb variabel.</span><span class="sxs-lookup"><span data-stu-id="af802-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="af802-112">I det andra kommandot används pipeline-operatorn för att överföra belastningsutjämnaren i $slb till Add-AzLoadBalancerRuleConfig, som lägger till en regel som heter NewRule.</span><span class="sxs-lookup"><span data-stu-id="af802-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerRuleConfig, which adds a rule named NewRule to it.</span></span>
<span data-ttu-id="af802-113">Det tredje kommandot skickar belastningsutjämnaren till **set-AzLoadBalancerRuleConfig** , som anger den nya regel konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="af802-113">The third command passes the load balancer to **Set-AzLoadBalancerRuleConfig** , which sets the new rule configuration.</span></span>
<span data-ttu-id="af802-114">Observera att konfigurationen inte aktiverar en flytande IP-adress, som har Aktiver ATS av föregående kommando.</span><span class="sxs-lookup"><span data-stu-id="af802-114">Note that the configuration does not enable a floating IP address, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="af802-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="af802-115">PARAMETERS</span></span>

### <span data-ttu-id="af802-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="af802-116">-BackendAddressPool</span></span>
<span data-ttu-id="af802-117">Anger ett **BackendAddressPool** -objekt som ska kopplas till en regel för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="af802-117">Specifies a **BackendAddressPool** object to associate with a load balancer rule.</span></span>

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

### <span data-ttu-id="af802-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="af802-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="af802-119">Anger ID för ett **BackendAddressPool** -objekt som ska kopplas till en regel konfiguration för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="af802-119">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="af802-120">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="af802-120">-BackendPort</span></span>
<span data-ttu-id="af802-121">Anger Server dels porten för trafik som matchas av denna regel konfiguration.</span><span class="sxs-lookup"><span data-stu-id="af802-121">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="af802-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af802-122">-DefaultProfile</span></span>
<span data-ttu-id="af802-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="af802-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af802-124">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="af802-124">-DisableOutboundSNAT</span></span>
<span data-ttu-id="af802-125">Konfigurerar SNAT för de virtuella datorerna i backend-poolen till att använda den publicIP-adress som anges i klient delen av regeln för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="af802-125">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="af802-126">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="af802-126">-EnableFloatingIP</span></span>
<span data-ttu-id="af802-127">Anger att denna cmdlet aktiverar en flytande IP-adress för en regel konfiguration.</span><span class="sxs-lookup"><span data-stu-id="af802-127">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="af802-128">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="af802-128">-EnableTcpReset</span></span>
<span data-ttu-id="af802-129">Ta emot dubbelriktad TCP-återställning i TCP-flödets tids gräns för inaktivitet eller oväntat upphör Ande.</span><span class="sxs-lookup"><span data-stu-id="af802-129">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="af802-130">Det här elementet används bara när protokollet är inställt på TCP.</span><span class="sxs-lookup"><span data-stu-id="af802-130">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="af802-131">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="af802-131">-FrontendIpConfiguration</span></span>
<span data-ttu-id="af802-132">Anger en lista över de front-IP-adresser som är associerade med en regel konfiguration för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="af802-132">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="af802-133">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="af802-133">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="af802-134">Anger ID för en front-IP-adresskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="af802-134">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="af802-135">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="af802-135">-FrontendPort</span></span>
<span data-ttu-id="af802-136">Anger front porten som matchas av en regel för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="af802-136">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="af802-137">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="af802-137">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="af802-138">Anger hur lång tid, i minuter, som status för konversationer ska behållas i en belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="af802-138">Specifies the length of time, in minutes, for which the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="af802-139">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="af802-139">-LoadBalancer</span></span>
<span data-ttu-id="af802-140">Anger en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="af802-140">Specifies a load balancer.</span></span>
<span data-ttu-id="af802-141">Denna cmdlet uppdaterar en regel konfiguration för belastningsutjämnaren som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="af802-141">This cmdlet updates a rule configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="af802-142">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="af802-142">-LoadDistribution</span></span>
<span data-ttu-id="af802-143">Anger en belastnings fördelning.</span><span class="sxs-lookup"><span data-stu-id="af802-143">Specifies a load distribution.</span></span>
<span data-ttu-id="af802-144">De acceptabla värdena för den här parametern är: SourceIP och SourceIPProtocol.</span><span class="sxs-lookup"><span data-stu-id="af802-144">The acceptable values for this parameter are: SourceIP and SourceIPProtocol.</span></span>

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

### <span data-ttu-id="af802-145">-Namn</span><span class="sxs-lookup"><span data-stu-id="af802-145">-Name</span></span>
<span data-ttu-id="af802-146">Anger namnet på en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="af802-146">Specifies the name of a load balancer.</span></span>

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

### <span data-ttu-id="af802-147">-Sond</span><span class="sxs-lookup"><span data-stu-id="af802-147">-Probe</span></span>
<span data-ttu-id="af802-148">Anger en sond som associeras med en regel konfiguration för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="af802-148">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="af802-149">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="af802-149">-ProbeId</span></span>
<span data-ttu-id="af802-150">Anger ID för den sond som ska kopplas till en regel konfiguration för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="af802-150">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="af802-151">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="af802-151">-Protocol</span></span>
<span data-ttu-id="af802-152">Anger det protokoll som matchas med en regel för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="af802-152">Specifies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="af802-153">De acceptabla värdena för denna parameter är: TCP eller UDP.</span><span class="sxs-lookup"><span data-stu-id="af802-153">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="af802-154">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="af802-154">-Confirm</span></span>
<span data-ttu-id="af802-155">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="af802-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af802-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af802-156">-WhatIf</span></span>
<span data-ttu-id="af802-157">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="af802-157">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="af802-158">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="af802-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af802-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af802-159">CommonParameters</span></span>
<span data-ttu-id="af802-160">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af802-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af802-161">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af802-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af802-162">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="af802-162">INPUTS</span></span>

### <span data-ttu-id="af802-163">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="af802-163">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="af802-164">System. String</span><span class="sxs-lookup"><span data-stu-id="af802-164">System.String</span></span>

### <span data-ttu-id="af802-165">System. Int32</span><span class="sxs-lookup"><span data-stu-id="af802-165">System.Int32</span></span>

### <span data-ttu-id="af802-166">Microsoft. Azure. commands. Networks. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="af802-166">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

### <span data-ttu-id="af802-167">Microsoft. Azure. commands. Networks. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="af802-167">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

### <span data-ttu-id="af802-168">Microsoft. Azure. commands. Networks. Models. PSProbe</span><span class="sxs-lookup"><span data-stu-id="af802-168">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="af802-169">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="af802-169">OUTPUTS</span></span>

### <span data-ttu-id="af802-170">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="af802-170">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="af802-171">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="af802-171">NOTES</span></span>

## <span data-ttu-id="af802-172">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="af802-172">RELATED LINKS</span></span>

[<span data-ttu-id="af802-173">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="af802-173">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="af802-174">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="af802-174">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="af802-175">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="af802-175">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="af802-176">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="af802-176">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="af802-177">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="af802-177">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

