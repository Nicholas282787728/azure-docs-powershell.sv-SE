---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: 79a8442d28d6e04d4e6e013e536663a19faaf3f5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918827"
---
# <span data-ttu-id="24fc9-101">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="24fc9-101">Add-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="24fc9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="24fc9-102">SYNOPSIS</span></span>
<span data-ttu-id="24fc9-103">Lägger till en regel för utgående trafik till en belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="24fc9-103">Adds an outbound rule configuration to a load balancer.</span></span>

## <span data-ttu-id="24fc9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="24fc9-104">SYNTAX</span></span>

### <span data-ttu-id="24fc9-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="24fc9-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPool <PSBackendAddressPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24fc9-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="24fc9-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPoolId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24fc9-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="24fc9-107">DESCRIPTION</span></span>
<span data-ttu-id="24fc9-108">Cmdleten **Add-AzLoadBalancerOutboundRuleConfig** lägger till en regel för utgående trafik i en Azure-belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="24fc9-108">The **Add-AzLoadBalancerOutboundRuleConfig** cmdlet adds an outbound rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="24fc9-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="24fc9-109">EXAMPLES</span></span>

### <span data-ttu-id="24fc9-110">Exempel 1: lägga till en regel för utgående trafik till en belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="24fc9-110">Example 1: Add an outbound rule configuration to a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>$slb | Add-AzLoadBalancerOutboundRuleConfig -Name "NewRule" -Protocol "Tcp" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -BackendAddressPool $slb.BackendAddressPools[0]
```

<span data-ttu-id="24fc9-111">Det första kommandot får belastningsutjämnaren med namnet MyLoadBalancer och lagrar det sedan i variabeln $slb.</span><span class="sxs-lookup"><span data-stu-id="24fc9-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="24fc9-112">I det andra kommandot används pipeline-operatorn för att överföra belastningsutjämnaren i $slb till **Add-AzLoadBalancerOutboundRuleConfig** , som lägger till en regel för utgående trafik till belastningsutjämnaren.</span><span class="sxs-lookup"><span data-stu-id="24fc9-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzLoadBalancerOutboundRuleConfig** , which adds an outbound rule configuration to the load balancer.</span></span>

## <span data-ttu-id="24fc9-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="24fc9-113">PARAMETERS</span></span>

### <span data-ttu-id="24fc9-114">-AllocatedOutboundPort</span><span class="sxs-lookup"><span data-stu-id="24fc9-114">-AllocatedOutboundPort</span></span>
<span data-ttu-id="24fc9-115">Antalet utgående portar som ska användas för NAT.</span><span class="sxs-lookup"><span data-stu-id="24fc9-115">The number of outbound ports to be used for NAT.</span></span>

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

### <span data-ttu-id="24fc9-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="24fc9-116">-BackendAddressPool</span></span>
<span data-ttu-id="24fc9-117">En referens till en pool med DIP.</span><span class="sxs-lookup"><span data-stu-id="24fc9-117">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="24fc9-118">Utgående trafik bal anse ras slumpmässigt för IP i Server delen.</span><span class="sxs-lookup"><span data-stu-id="24fc9-118">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24fc9-119">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="24fc9-119">-BackendAddressPoolId</span></span>
<span data-ttu-id="24fc9-120">En referens till en pool med DIP.</span><span class="sxs-lookup"><span data-stu-id="24fc9-120">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="24fc9-121">Utgående trafik bal anse ras slumpmässigt för IP i Server delen.</span><span class="sxs-lookup"><span data-stu-id="24fc9-121">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24fc9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24fc9-122">-DefaultProfile</span></span>
<span data-ttu-id="24fc9-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="24fc9-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24fc9-124">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="24fc9-124">-EnableTcpReset</span></span>
<span data-ttu-id="24fc9-125">Ta emot dubbelriktad TCP-återställning i TCP-flödets tids gräns för inaktivitet eller oväntat upphör Ande.</span><span class="sxs-lookup"><span data-stu-id="24fc9-125">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span>
<span data-ttu-id="24fc9-126">Det här elementet används bara när protokollet är inställt på TCP.</span><span class="sxs-lookup"><span data-stu-id="24fc9-126">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="24fc9-127">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="24fc9-127">-FrontendIpConfiguration</span></span>
<span data-ttu-id="24fc9-128">Belastnings utjämningens IP-adresser för klient delen.</span><span class="sxs-lookup"><span data-stu-id="24fc9-128">The Frontend IP addresses of the load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSResourceId[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24fc9-129">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="24fc9-129">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="24fc9-130">Timeout för TCP-inaktiv anslutning</span><span class="sxs-lookup"><span data-stu-id="24fc9-130">The timeout for the TCP idle connection</span></span>

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

### <span data-ttu-id="24fc9-131">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="24fc9-131">-LoadBalancer</span></span>
<span data-ttu-id="24fc9-132">Referensen för belastnings Utjämnings resursen.</span><span class="sxs-lookup"><span data-stu-id="24fc9-132">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="24fc9-133">-Namn</span><span class="sxs-lookup"><span data-stu-id="24fc9-133">-Name</span></span>
<span data-ttu-id="24fc9-134">Namn på regeln för utgående trafik.</span><span class="sxs-lookup"><span data-stu-id="24fc9-134">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="24fc9-135">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="24fc9-135">-Protocol</span></span>
<span data-ttu-id="24fc9-136">Protokoll – TCP, UDP eller alla</span><span class="sxs-lookup"><span data-stu-id="24fc9-136">Protocol - TCP, UDP or All</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24fc9-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="24fc9-137">-Confirm</span></span>
<span data-ttu-id="24fc9-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="24fc9-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24fc9-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24fc9-139">-WhatIf</span></span>
<span data-ttu-id="24fc9-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="24fc9-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24fc9-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="24fc9-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24fc9-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24fc9-142">CommonParameters</span></span>
<span data-ttu-id="24fc9-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24fc9-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24fc9-144">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24fc9-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24fc9-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="24fc9-145">INPUTS</span></span>

### <span data-ttu-id="24fc9-146">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="24fc9-146">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="24fc9-147">System. Int32</span><span class="sxs-lookup"><span data-stu-id="24fc9-147">System.Int32</span></span>

### <span data-ttu-id="24fc9-148">System. String</span><span class="sxs-lookup"><span data-stu-id="24fc9-148">System.String</span></span>

### <span data-ttu-id="24fc9-149">Microsoft. Azure. commands. Network. Models. PSResourceId []</span><span class="sxs-lookup"><span data-stu-id="24fc9-149">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

### <span data-ttu-id="24fc9-150">Microsoft. Azure. commands. Networks. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="24fc9-150">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="24fc9-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="24fc9-151">OUTPUTS</span></span>

### <span data-ttu-id="24fc9-152">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="24fc9-152">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="24fc9-153">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="24fc9-153">NOTES</span></span>

## <span data-ttu-id="24fc9-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="24fc9-154">RELATED LINKS</span></span>

[<span data-ttu-id="24fc9-155">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="24fc9-155">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="24fc9-156">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="24fc9-156">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="24fc9-157">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="24fc9-157">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="24fc9-158">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="24fc9-158">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)
