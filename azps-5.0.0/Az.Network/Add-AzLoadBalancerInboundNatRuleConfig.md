---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EE8F5D57-1ECE-4F23-9A5B-F226DD2C5ECB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 3c0ce9d5038cb63c70d8c0c5f093077dedfb9ad4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94325932"
---
# <span data-ttu-id="ae88d-101">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ae88d-101">Add-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="ae88d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ae88d-102">SYNOPSIS</span></span>
<span data-ttu-id="ae88d-103">Lägger till en inkommande NAT-regel i en belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="ae88d-103">Adds an inbound NAT rule configuration to a load balancer.</span></span>

## <span data-ttu-id="ae88d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ae88d-104">SYNTAX</span></span>

### <span data-ttu-id="ae88d-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="ae88d-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae88d-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="ae88d-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae88d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ae88d-107">DESCRIPTION</span></span>
<span data-ttu-id="ae88d-108">Cmdleten **Add-AzLoadBalancerInboundNatRuleConfig** lägger till en inkommande NAT-regel (Network Address Translation) för en Azure-belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="ae88d-108">The **Add-AzLoadBalancerInboundNatRuleConfig** cmdlet adds an inbound network address translation (NAT) rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="ae88d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ae88d-109">EXAMPLES</span></span>

### <span data-ttu-id="ae88d-110">Exempel 1: lägga till en inkommande NAT-regel i en belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="ae88d-110">Example 1: Add an inbound NAT rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
```

<span data-ttu-id="ae88d-111">Det första kommandot får belastningsutjämnaren med namnet MyloadBalancer och lagrar det sedan i variabeln $slb.</span><span class="sxs-lookup"><span data-stu-id="ae88d-111">The first command gets the load balancer named MyloadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="ae88d-112">I det andra kommandot används pipeline-operatorn för att överföra belastningsutjämnaren i $slb till **Add-AzLoadBalancerInboundNatRuleConfig** , som lägger till en regel för inkommande NAT-regler till belastningsutjämnaren.</span><span class="sxs-lookup"><span data-stu-id="ae88d-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzLoadBalancerInboundNatRuleConfig** , which adds an inbound NAT rule configuration to the load balancer.</span></span>

## <span data-ttu-id="ae88d-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ae88d-113">PARAMETERS</span></span>

### <span data-ttu-id="ae88d-114">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="ae88d-114">-BackendPort</span></span>
<span data-ttu-id="ae88d-115">Anger backend-porten för trafik som matchas av en regel konfiguration.</span><span class="sxs-lookup"><span data-stu-id="ae88d-115">Specifies the backend port for traffic matched by a rule configuration.</span></span>

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

### <span data-ttu-id="ae88d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae88d-116">-DefaultProfile</span></span>
<span data-ttu-id="ae88d-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ae88d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae88d-118">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="ae88d-118">-EnableFloatingIP</span></span>
<span data-ttu-id="ae88d-119">Anger att denna cmdlet aktiverar en flytande IP-adress för en regel konfiguration.</span><span class="sxs-lookup"><span data-stu-id="ae88d-119">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="ae88d-120">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="ae88d-120">-EnableTcpReset</span></span>
<span data-ttu-id="ae88d-121">Ta emot dubbelriktad TCP-återställning i TCP-flödets tids gräns för inaktivitet eller oväntat upphör Ande.</span><span class="sxs-lookup"><span data-stu-id="ae88d-121">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="ae88d-122">Det här elementet används bara när protokollet är inställt på TCP.</span><span class="sxs-lookup"><span data-stu-id="ae88d-122">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="ae88d-123">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="ae88d-123">-FrontendIpConfiguration</span></span>
<span data-ttu-id="ae88d-124">Anger en lista med IP-adresser som ska kopplas till en inkommande NAT-regel.</span><span class="sxs-lookup"><span data-stu-id="ae88d-124">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="ae88d-125">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="ae88d-125">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="ae88d-126">Anger ett ID för en front-IP-adresskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="ae88d-126">Specifies an ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="ae88d-127">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="ae88d-127">-FrontendPort</span></span>
<span data-ttu-id="ae88d-128">Anger front porten som matchas av en regel konfiguration.</span><span class="sxs-lookup"><span data-stu-id="ae88d-128">Specifies the front-end port that is matched by a rule configuration.</span></span>

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

### <span data-ttu-id="ae88d-129">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="ae88d-129">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="ae88d-130">Anger hur lång tid, i minuter, som status för konversationer ska behållas i en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="ae88d-130">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="ae88d-131">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ae88d-131">-LoadBalancer</span></span>
<span data-ttu-id="ae88d-132">Anger ett **Loadbalancer** -objekt.</span><span class="sxs-lookup"><span data-stu-id="ae88d-132">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="ae88d-133">Denna cmdlet lägger till en inkommande NAT-regel för belastnings utjämning som anges av den här parametern.</span><span class="sxs-lookup"><span data-stu-id="ae88d-133">This cmdlet adds an inbound NAT rule configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="ae88d-134">-Namn</span><span class="sxs-lookup"><span data-stu-id="ae88d-134">-Name</span></span>
<span data-ttu-id="ae88d-135">Anger namnet på den inkommande NAT-regelns konfiguration som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="ae88d-135">Specifies the name of the inbound NAT rule configuration to add.</span></span>

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

### <span data-ttu-id="ae88d-136">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="ae88d-136">-Protocol</span></span>
<span data-ttu-id="ae88d-137">Anger det protokoll som matchas av en inkommande NAT-regel.</span><span class="sxs-lookup"><span data-stu-id="ae88d-137">Specifies the protocol that is matched by an inbound NAT rule.</span></span>
<span data-ttu-id="ae88d-138">De acceptabla värdena för denna parameter är: TCP eller UDP.</span><span class="sxs-lookup"><span data-stu-id="ae88d-138">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="ae88d-139">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ae88d-139">-Confirm</span></span>
<span data-ttu-id="ae88d-140">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ae88d-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae88d-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae88d-141">-WhatIf</span></span>
<span data-ttu-id="ae88d-142">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ae88d-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ae88d-143">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ae88d-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae88d-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae88d-144">CommonParameters</span></span>
<span data-ttu-id="ae88d-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae88d-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae88d-146">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae88d-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae88d-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ae88d-147">INPUTS</span></span>

### <span data-ttu-id="ae88d-148">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ae88d-148">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="ae88d-149">System. String</span><span class="sxs-lookup"><span data-stu-id="ae88d-149">System.String</span></span>

### <span data-ttu-id="ae88d-150">System. Int32</span><span class="sxs-lookup"><span data-stu-id="ae88d-150">System.Int32</span></span>

### <span data-ttu-id="ae88d-151">Microsoft. Azure. commands. Networks. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ae88d-151">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="ae88d-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ae88d-152">OUTPUTS</span></span>

### <span data-ttu-id="ae88d-153">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ae88d-153">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="ae88d-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ae88d-154">NOTES</span></span>

## <span data-ttu-id="ae88d-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ae88d-155">RELATED LINKS</span></span>

[<span data-ttu-id="ae88d-156">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ae88d-156">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="ae88d-157">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ae88d-157">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="ae88d-158">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ae88d-158">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="ae88d-159">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ae88d-159">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="ae88d-160">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ae88d-160">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)

[<span data-ttu-id="ae88d-161">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ae88d-161">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


