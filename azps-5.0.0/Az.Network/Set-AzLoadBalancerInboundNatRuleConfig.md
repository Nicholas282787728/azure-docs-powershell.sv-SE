---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 87818605-EFA6-422E-9ECD-0A0BF269DCFD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 68b3043b67580dcc781badb7c1891444e97e281f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270820"
---
# <span data-ttu-id="2fea2-101">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2fea2-101">Set-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="2fea2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2fea2-102">SYNOPSIS</span></span>
<span data-ttu-id="2fea2-103">Anger en inkommande NAT-regel för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="2fea2-103">Sets an inbound NAT rule configuration for a load balancer.</span></span>

## <span data-ttu-id="2fea2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2fea2-104">SYNTAX</span></span>

### <span data-ttu-id="2fea2-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="2fea2-105">SetByResource (Default)</span></span>
```
Set-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2fea2-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="2fea2-106">SetByResourceId</span></span>
```
Set-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2fea2-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2fea2-107">DESCRIPTION</span></span>
<span data-ttu-id="2fea2-108">Cmdleten **set-AzLoadBalancerInboundNatRuleConfig** anger en regel för inkommande NAT-regler (Network Address Translation) för en Azure-belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="2fea2-108">The **Set-AzLoadBalancerInboundNatRuleConfig** cmdlet sets an inbound network address translation (NAT) rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="2fea2-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2fea2-109">EXAMPLES</span></span>

### <span data-ttu-id="2fea2-110">Exempel 1: ändra konfigurationen för inkommande NAT-regler på en belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="2fea2-110">Example 1: Modify the inbound NAT rule configuration on a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
```

<span data-ttu-id="2fea2-111">Det första kommandot får belastningsutjämnaren med namnet MyLoadBalancer och lagrar det sedan i $slb variabel.</span><span class="sxs-lookup"><span data-stu-id="2fea2-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="2fea2-112">Det andra kommandot använder pipeline-operatorn för att överföra belastningsutjämnaren i $slb till Add-AzLoadBalancerInboundNatRuleConfig, vilket lägger till en inkommande NAT-regel.</span><span class="sxs-lookup"><span data-stu-id="2fea2-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule configuration to it.</span></span>
<span data-ttu-id="2fea2-113">Det tredje kommandot skickar belastningsutjämnaren till **set-AzLoadBalancerInboundNatRuleConfig** , som sparar och uppdaterar den inkommande NAT-regelns konfiguration.</span><span class="sxs-lookup"><span data-stu-id="2fea2-113">The third command passes the load balancer to **Set-AzLoadBalancerInboundNatRuleConfig** , which saves and updates the inbound NAT rule configuration.</span></span>
<span data-ttu-id="2fea2-114">Observera att regel konfigurationen har ställts in utan att aktivera flytande IP, som har Aktiver ATS med föregående kommando.</span><span class="sxs-lookup"><span data-stu-id="2fea2-114">Note that the rule configuration was set without enabling floating IP, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="2fea2-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2fea2-115">PARAMETERS</span></span>

### <span data-ttu-id="2fea2-116">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="2fea2-116">-BackendPort</span></span>
<span data-ttu-id="2fea2-117">Anger Server dels porten för trafik som matchas av denna regel konfiguration.</span><span class="sxs-lookup"><span data-stu-id="2fea2-117">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="2fea2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fea2-118">-DefaultProfile</span></span>
<span data-ttu-id="2fea2-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2fea2-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2fea2-120">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="2fea2-120">-EnableFloatingIP</span></span>
<span data-ttu-id="2fea2-121">Anger att denna cmdlet aktiverar en flytande IP-adress för en regel konfiguration.</span><span class="sxs-lookup"><span data-stu-id="2fea2-121">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="2fea2-122">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="2fea2-122">-EnableTcpReset</span></span>
<span data-ttu-id="2fea2-123">Ta emot dubbelriktad TCP-återställning i TCP-flödets tids gräns för inaktivitet eller oväntat upphör Ande.</span><span class="sxs-lookup"><span data-stu-id="2fea2-123">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="2fea2-124">Det här elementet används bara när protokollet är inställt på TCP.</span><span class="sxs-lookup"><span data-stu-id="2fea2-124">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="2fea2-125">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="2fea2-125">-FrontendIpConfiguration</span></span>
<span data-ttu-id="2fea2-126">Anger en lista med IP-adresser som ska kopplas till en inkommande NAT-regel.</span><span class="sxs-lookup"><span data-stu-id="2fea2-126">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="2fea2-127">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="2fea2-127">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="2fea2-128">Anger ID för en front-IP-adresskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="2fea2-128">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="2fea2-129">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="2fea2-129">-FrontendPort</span></span>
<span data-ttu-id="2fea2-130">Anger front porten som matchas av en regel för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="2fea2-130">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="2fea2-131">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="2fea2-131">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="2fea2-132">Anger hur lång tid, i minuter, som status för konversationer ska behållas i en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="2fea2-132">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="2fea2-133">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2fea2-133">-LoadBalancer</span></span>
<span data-ttu-id="2fea2-134">Anger en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="2fea2-134">Specifies a load balancer.</span></span>
<span data-ttu-id="2fea2-135">Denna cmdlet anger en inkommande NAT-regel för belastnings utjämning som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="2fea2-135">This cmdlet sets an inbound NAT rule configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="2fea2-136">-Namn</span><span class="sxs-lookup"><span data-stu-id="2fea2-136">-Name</span></span>
<span data-ttu-id="2fea2-137">Anger namnet på en inkommande NAT-regel.</span><span class="sxs-lookup"><span data-stu-id="2fea2-137">Specifies the name of an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="2fea2-138">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="2fea2-138">-Protocol</span></span>
<span data-ttu-id="2fea2-139">Anger det protokoll som matchas av en inkommande NAT-regel.</span><span class="sxs-lookup"><span data-stu-id="2fea2-139">Specifies the protocol that is matched by an inbound NAT rule configuration.</span></span>
<span data-ttu-id="2fea2-140">De acceptabla värdena för denna parameter är: TCP eller UDP.</span><span class="sxs-lookup"><span data-stu-id="2fea2-140">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="2fea2-141">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2fea2-141">-Confirm</span></span>
<span data-ttu-id="2fea2-142">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2fea2-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2fea2-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2fea2-143">-WhatIf</span></span>
<span data-ttu-id="2fea2-144">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2fea2-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2fea2-145">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2fea2-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2fea2-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fea2-146">CommonParameters</span></span>
<span data-ttu-id="2fea2-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fea2-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fea2-148">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fea2-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fea2-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2fea2-149">INPUTS</span></span>

### <span data-ttu-id="2fea2-150">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2fea2-150">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="2fea2-151">System. String</span><span class="sxs-lookup"><span data-stu-id="2fea2-151">System.String</span></span>

### <span data-ttu-id="2fea2-152">System. Int32</span><span class="sxs-lookup"><span data-stu-id="2fea2-152">System.Int32</span></span>

### <span data-ttu-id="2fea2-153">Microsoft. Azure. commands. Networks. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="2fea2-153">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="2fea2-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2fea2-154">OUTPUTS</span></span>

### <span data-ttu-id="2fea2-155">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2fea2-155">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="2fea2-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2fea2-156">NOTES</span></span>

## <span data-ttu-id="2fea2-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2fea2-157">RELATED LINKS</span></span>

[<span data-ttu-id="2fea2-158">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2fea2-158">Add-AzLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="2fea2-159">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2fea2-159">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="2fea2-160">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2fea2-160">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="2fea2-161">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2fea2-161">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="2fea2-162">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2fea2-162">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)


